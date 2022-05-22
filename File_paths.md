<a href="README.md">Back to Appendix</a>

# Determine the current directory

```
Console.WriteLine(Directory.GetCurrentDirectory());
```

# Work with special directories

```
string docPath = Environment.GetFolderPath(Environment.SpecialFolder.MyDocuments);
```

# Work with paths

## Special path characters

To help you use the correct character, the ```Path``` class contains the ```DirectorySeparatorChar``` field.

```
Console.WriteLine($"stores{Path.DirectorySeparatorChar}201");

// returns:
// stores\201 on Windows
//
// stores/201 on macOS
```

## Join paths

The ```Path``` class works with the concept of file and folder paths, which are just strings. You can use the Path class to automatically build correct paths for specific operating systems.

```
Console.WriteLine(Path.Combine("stores","201")); // outputs: stores/201
```

## Determine filename extensions

The ```Path``` class can also tell you the extension of a filename. If you have a file and you want to know if it's a JSON file, you can use the ```Path.GetExtension``` function.

```
Console.WriteLine(Path.GetExtension("sales.json")); // outputs: .json
```

## Get everything you need to know about a file or path

The ```Path``` class contains many different methods that do various things. You can get the most information about a directory or a file by using the ```DirectoryInfo``` or ```FileInfo``` classes, respectively.

```
string fileName = $"stores{Path.DirectorySeparatorChar}201{Path.DirectorySeparatorChar}sales{Path.DirectorySeparatorChar}sales.json";

FileInfo info = new FileInfo(fileName);

Console.WriteLine($"Full Name: {info.FullName}{Environment.NewLine}Directory: {info.Directory}{Environment.NewLine}Extension: {info.Extension}{Environment.NewLine}Create Date: {info.CreationTime}"); // And many more
```



