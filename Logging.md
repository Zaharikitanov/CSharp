<a href="README.md">Back to Appendix</a>

# Write information to output windows

- System.Console
  - Always enabled and always writes to the console.
  - Useful for information that your customer might need to see in the release.
  - Because it's the simplest approach, it's often used for ad-hoc temporary debugging. This debug code is often never checked in to source control.
- System.Diagnostics.Trace
  - Only enabled when ```TRACE``` is defined.
  - Writes to attached Listeners, by default, the DefaultTraceListener.
  - Use this API when you create logs that will be enabled in most builds.
- System.Diagnostics.Debug
  - Only enabled when ```DEBUG``` is defined (when in debug mode).
  - Writes to an attached debugger.
  - Use this API when you create logs that will be enabled only in debug builds.

```
Console.WriteLine("This message is readable by the end user.");
Trace.WriteLine("This is a trace message when tracing the app.");
Debug.WriteLine("This is a debug message just for developers.");
```

## Define TRACE and DEBUG constants

```
<PropertyGroup Condition="'$(Configuration)|$(Platform)'=='Debug|AnyCPU'">
    <DefineConstants>DEBUG;TRACE</DefineConstants>
</PropertyGroup>
<PropertyGroup Condition="'$(Configuration)|$(Platform)'=='Release|AnyCPU'">
    <DefineConstants>TRACE</DefineConstants>
</PropertyGroup>
```
