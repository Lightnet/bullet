# Bullet

[Bullet Physics](https://github.com/bulletphysics) wrapper for Heaps

Supports both HashLink and JS output thanks to [WebIDL](https://github.com/ncannasse/webidl)

## Compilation

Note: 32 bit build hashlink is not working on window 10 last checked 1.11.

Download hashlink as well sub library and build 64bit. Make sure it run correctly else the bullet errors. Hashlink 32bit error will show module errors. (if upgrade to vs2017)

https://github.com/HaxeFoundation/hashlink

```
HaxeToolkit\haxe
HaxeToolkit\haxe\hashlink <- src / build
HaxeToolkit\haxe\lib
```

Download https://github.com/HeapsIO/bullet to 

```
HaxeToolkit\haxe\hashlink
HaxeToolkit\haxe\lib
HaxeToolkit\haxe\lib\bullet <- default for haxelib to read for import "haxelib git bullet https://github.com/HeapsIO/bullet"
HaxeToolkit\haxe\lib\bulletmod <- compile path build look for hashlink folder.
```
Reason for two folder is one bullet.sln compiler path for hashlash on path dir and other is need to haxelib config for import read correct path.


https://github.com/bulletphysics/bullet3/releases get the bullet3 2.87 version.

```
HaxeToolkit\haxe\lib\bulletmod <- compile
HaxeToolkit\haxe\lib\bulletmod\src\bullet <- bullet3 2.87 version src file
```

install make

https://chocolatey.org/packages/make


https://github.com/ncannasse/webidl

haxelib git webidl https://github.com/ncannasse/webidl

Note you might get error on the webidl. Used the git update version.

command run
```
make genhl
```
Note if there no error that good.


open bullet.sln and select release and x64. Once compile the file name "bullet.hdll" copy or move to where hl.exe.
```
HaxeToolkit\haxe\lib\bulletmod\x64\Release

```

Requires having hashlink one level upper than bullet directory, such as:

```
/hashlink
/libs
   /bullet
		/git
			
   /bulletmnod/src/bullet
```