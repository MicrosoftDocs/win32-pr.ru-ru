---
description: Перемещает элемент или элементы в эту папку.
ms.assetid: 07723dc1-5d9d-4f32-ab18-52617b0988c4
title: Метод Folder. Мовехере (Шлдисп. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Folder.MoveHere
api_type:
- COM
api_location:
- Shell32.dll
ms.openlocfilehash: da6590d63f4a3c79252e25f3625c0ee75b146b6d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "103808033"
---
# <a name="foldermovehere-method"></a>Folder. Мовехере, метод

Перемещает элемент или элементы в эту папку.

## <a name="syntax"></a>Синтаксис


```JScript
Folder.MoveHere(
  vItem,
  [ vOptions ]
)
```



## <a name="parameters"></a>Параметры

<dl> <dt>

*витем* \[ окне\]
</dt> <dd>

Тип: **Variant**

Перемещаемый элемент или элементы. Это может быть строка, представляющая имя файла, объект [**FolderItem**](folderitem.md) или объект [**фолдеритемс**](folderitems.md) .

</dd> <dt>

*воптионс* \[ в необязательное\]
</dt> <dd>

Тип: **Variant**

Параметры для операции перемещения. Это значение может быть нулевым или иметь сочетание следующих значений. Эти значения основаны на флагах, определенных для использования с элементом **ффлагс** структуры C++ [**шфилеопструкт**](/windows/desktop/api/Shellapi/ns-shellapi-shfileopstructa) . Эти флаги не определены для Visual Basic, VBScript или JScript, поэтому их необходимо определить самостоятельно или использовать их числовые эквиваленты.

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



 (9182)


</dt> <dd>

[Версия 5,0.](versions.md) Не переносите подключенные файлы как группу. Переместить только указанные файлы.

</dd> </dl> </dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Этот метод не возвращает значение.

## <a name="remarks"></a>Примечания

> [!Note]  
> Не все методы реализуются для всех папок. Например, метод [**PARSENAME**](folder-parsename.md) не реализован для папки панели управления ( \_ элементы управления CSID). При попытке вызвать нереализованный метод возникнет ошибка 0x800A01BD (Decimal 445).

 

## <a name="examples"></a>Примеры

В следующем примере **мовехере** используется для перемещения файла Temp.txt из корневого каталога диска c в папку c: \\ Windows. Правильное использование показано в JScript, VBScript и Visual Basic.

Присутствовал


```JScript
<script language="JScript">
    var FOF_NOCONFIRMATION = 16;

    function fnFolderObjectMoveHereJ()
    {
        var objShell  = new ActiveXObject("shell.application");
        var objFolder = new Object;
        
        objFolder = objShell.NameSpace("C:\\WINDOWS");
        if (objFolder != null)
        {
            objFolder.MoveHere ("C:\\temp.txt", FOF_NOCONFIRMATION);
        }
    }
</script>
```



Сценариев


```VB
<script language="VBScript">
    private const FOF_NOCONFIRMATION = 16
    
    function fnFolderObjectMoveHereVB()
        dim objShell
        dim objFolder

        set objShell = CreateObject("shell.application")
        set objFolder = objShell.NameSpace("C:\WINDOWS")

        if (not objFolder is nothing) then
            objFolder.MoveHere "C:\temp.txt", FOF_NOCONFIRMATION
        end if

        set objFolder = nothing
        set objShell = nothing
    end function
</script>
```



Visual Basic:


```VB
Private Const FOF_NOCONFIRMATION = &H10

Private Sub btnMoveHere_Click()
    Dim objShell  As Shell
    Dim objFolder As Folder

    Set objShell = New Shell
    Set objFolder = objShell.NameSpace("C:\WINDOWS")

    If (Not objFolder Is Nothing) Then
        objFolder.MoveHere "c:\temp.txt", FOF_NOCONFIRMATION
    End If

    Set objFolder = Nothing
    Set objShell = Nothing
End Sub
```



## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------------------------|----------------------------------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Windows 2000 Professional, только для \[ классических приложений Windows XP\]<br/>                                         |
| Минимальная версия сервера<br/> | Windows 2000 Server \[только классические приложения\]<br/>                                                           |
| Заголовок<br/>                   | <dl> <dt>Шлдисп. h</dt> </dl>                           |
| IDL<br/>                      | <dl> <dt>Шлдисп. idl</dt> </dl>                         |
| DLL<br/>                      | <dl> <dt>Shell32.dll (версия 4,71 или более поздняя)</dt> </dl> |



 

 




