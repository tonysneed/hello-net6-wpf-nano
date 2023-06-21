# Hello .NET 6 with WPF in Docker on Nano Server

Demo of running a .NET Core console app with WPF in Docker on Nano Server

## Console App Using WPF on .NET 6

1. Create a WPF Library for .NET Core.
2. Convert to a console app.
   - Edit .csproj file to add `<OutputType>Exe</OutputType>`
3. Add `Program` class with static `Main` method.
4. Import `System.Windows.Media.Media3D` namespace, use 3D geometry.

## Dependency on dwrite.dll

For WPF to run on Windows Nano Server, you must edit the Dockerfile to copy drwite.dll to the Windows/System32 directory.

```dockerfile
COPY DWrite.dll /Windows/System32
```
