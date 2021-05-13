---
description: Копирует элемент или элементы в папку.
title: Метод Folder. Копихере (Шлдисп. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Folder.CopyHere
api_type:
- COM
api_location:
- Shell32.dll
ms.assetid: 22bf1b4c-f242-4c52-b094-c5339bb35d02
ms.openlocfilehash: 1466e5d01715c0c820cbc7cd9809c51e4963ec56
ms.sourcegitcommit: 3caaa3c92dcb1ef12f84464d14ce6262e65e988e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 05/12/2021
ms.locfileid: "109842145"
---
# <a name="foldercopyhere-method"></a>Folder. Копихере, метод

Копирует элемент или элементы в папку.

## <a name="syntax"></a>Синтаксис


```JScript
Folder.CopyHere(
  vItem,
  [ vOptions ]
)
```



## <a name="parameters"></a>Параметры

<dl> <dt>

*витем* 
</dt> <dd>

Тип: **Variant**

Копируемый элемент или элементы. Это может быть строка, представляющая имя файла, объект [**FolderItem**](folderitem.md) или объект [**фолдеритемс**](folderitems.md) .

</dd> <dt>

*воптионс* \[ используемых\]
</dt> <dd>

Тип: **Variant**

Параметры для операции копирования. Это значение может быть нулевым или иметь сочетание следующих значений. Эти значения основаны на флагах, определенных для использования с элементом **ффлагс** структуры C++ [**шфилеопструкт**](/windows/desktop/api/Shellapi/ns-shellapi-shfileopstructa) . Каждое пространство имен оболочки должно предоставлять собственную реализацию этих флагов, и каждое пространство имен может игнорировать некоторые или даже все эти флаги. Эти флаги не определяются по имени для Visual Basic, VBScript или JScript, поэтому их необходимо определить самостоятельно или использовать их числовые эквиваленты.

> [!Note]  
> В некоторых случаях, например сжатых ZIP-файлах, некоторые флаги параметров могут игнорироваться конструкцией.

 

<dt>



 (4)


</dt> <dd>

Не отображать диалоговое окно хода выполнения.

</dd> <dt>



 (8)


</dt> <dd>

Если файл с таким именем уже существует, присвойте файлу новое имя в операции перемещения, копирования или переименования.

</dd> <dt>



 (16)


</dt> <dd>

Ответьте "Да для всех" для любого отображаемого диалогового окна.

</dd> <dt>



 (64)


</dt> <dd>

По возможности сохраняйте сведения об отмене.

</dd> <dt>



 (128)


</dt> <dd>

Выполнить операцию с файлами следует только в том случае, если указано имя файла с подстановочным знаком ( \* . \* ).

</dd> <dt>



 (256)


</dt> <dd>

Отображает диалоговое окно хода выполнения, но не отображает имена файлов.

</dd> <dt>



 (512)


</dt> <dd>

Не подтверждайте создание нового каталога, если для операции требуется создать один.

</dd> <dt>



 (1024)


</dt> <dd>

Не отображать пользовательский интерфейс при возникновении ошибки.

</dd> <dt>



 (2048)


</dt> <dd>

[Версия 4,71.](versions.md) Не копируйте атрибуты безопасности файла.

</dd> <dt>



 (4096)


</dt> <dd>

Работают только в локальном каталоге. Не работают рекурсивно в подкаталогах.

</dd> <dt>



 (8192)


</dt> <dd>

[Версия 5,0.](versions.md) Не копируйте подключенные файлы в группу. Копировать только указанные файлы.

</dd> </dl> </dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Этот метод не возвращает значение.

## <a name="remarks"></a>Remarks

В вызывающей программе не выдается уведомление о том, что копирование завершено.

> [!Note]  
> Не все методы реализуются для всех папок. Например, метод [**PARSENAME**](folder-parsename.md) не реализован для папки панели управления ( \_ элементы управления CSID). При попытке вызвать нереализованный метод возникнет ошибка 0x800A01BD (Decimal 445).

 

## <a name="examples"></a>Примеры

В следующем примере используется **копихере** для копирования файла Autoexec.bat из корневого каталога в каталог C: \\ Windows. Правильное использование показано в JScript, VBScript и Visual Basic.

Присутствовал


```JScript
<script language="JScript">
    function fnCopyHereJ()
    {
        var objShell = new ActiveXObject("shell.application");
        var objFolder = new Object;
        
        objFolder = objShell.NameSpace("C:\\WINDOWS");
        if (objFolder != null)
        {
            objFolder.CopyHere("C:\\AUTOEXEC.BAT");
        }
    }
 </script>
```



Сценариев


```VB
<script language="VBScript">
    function fnCopyHereVB()
        dim objShell
        dim objFolder
        
        set objShell = CreateObject("shell.application")
        set objFolder = objShell.NameSpace("C:\WINDOWS")
 
        if not objFolder is nothing then
            objFolder.CopyHere("C:\AUTOEXEC.BAT")
        end if
 
        set objShell = nothing
        set objFolder = nothing
    end function
</script>
```



Visual Basic:


```VB
Private Sub btnCopyHere_Click()
    Dim objShell  As Shell
    Dim objFolder As Folder
    
    Set objShell = New Shell
    Set objFolder = objShell.NameSpace("C:\WINDOWS")
 
    If (Not objFolder Is Nothing) Then
        objFolder.CopyHere ("C:\AUTOEXEC.BAT")
    End If
 
    Set objFolder = Nothing
    Set objShell = Nothing
End Sub
```



## <a name="requirements"></a>Requirements (Требования)



| Требование | Значение |
|-------------------------------------|----------------------------------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Windows 2000 Professional, только для \[ классических приложений Windows XP\]<br/>                                         |
| Минимальная версия сервера<br/> | Windows 2000 Server \[только классические приложения\]<br/>                                                           |
| Заголовок<br/>                   | <dl> <dt>Шлдисп. h</dt> </dl>                           |
| IDL<br/>                      | <dl> <dt>Шлдисп. idl</dt> </dl>                         |
| DLL<br/>                      | <dl> <dt>Shell32.dll (версия 4,71 или более поздняя)</dt> </dl> |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[**Папка**](folder.md)
</dt> </dl>

 

 




