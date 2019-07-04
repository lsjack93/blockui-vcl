# Block User Interface for VCL Projects (Delphi)
![Delphi Supported Versions](https://img.shields.io/badge/Delphi%20Supported%20Versions-XE3..10.3%20Rio-blue.svg)
![Platforms](https://img.shields.io/badge/Platforms-Win32%20and%20Win64-red.svg)

This package allows you to lock and unlock the user interface in a simple way.

## Prerequisites
 * `[Optional]` For ease I recommend using the Boss for installation
   * [**Boss**](https://github.com/HashLoad/boss) - Dependency Manager for Delphi
 
### Installation using Boss (dependency manager for Delphi applications)
```
boss install github.com/viniciussanchez/blockui-vcl
```

### Manual Installation
Add the following folders to your project, in *Project > Options > Resource Compiler > Directories and Conditionals > Include file search path*
```
../blockui-vcl/src
```

### Getting Started
You need to use VCL.BlockUI.Intf and VCL.BlockUI 
```pascal
uses VCL.BlockUI.Intf, VCL.BlockUI;
```

#### How it works?
```pascal
var
  BlockUI: IBlockUI;
begin
  BlockUI := TBlockUI.Create;
  >> Your code
end;
``` 

In the Create method you can tell which component you want to block:

```pascal
BlockUI := TBlockUI.Create(Your component);
``` 

If not reported any component, the default is Application.MainForm
