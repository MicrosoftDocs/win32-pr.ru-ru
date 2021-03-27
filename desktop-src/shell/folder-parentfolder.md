---
description: Содержит объект родительской папки.
ms.assetid: b832948c-f599-4ada-8760-9280b86abfed
title: Свойство Folder. Парентфолдер (Шлдисп. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Folder.ParentFolder
api_type:
- COM
api_location:
- Shell32.dll
ms.openlocfilehash: 200d8f8c931bd81015f52226bed5a4e584951e20
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "103998458"
---
# <a name="folderparentfolder-property"></a>Свойство Folder. Парентфолдер

Содержит объект родительской [**папки**](folder.md) .

Это свойство доступно только для чтения.

## <a name="syntax"></a>Синтаксис


```JScript
ParentFolder = Folder.ParentFolder
```



## <a name="property-value"></a>Значение свойства

Ссылка на объект Парентфолдер.

## <a name="remarks"></a>Примечания

> [!Note]  
> Не все методы реализуются для всех папок. Например, метод [**PARSENAME**](folder-parsename.md) не реализован для папки панели управления ( \_ элементы управления CSID). При попытке вызвать нереализованный метод возникнет ошибка 0x800A01BD (Decimal 445).

 

## <a name="examples"></a>Примеры

В следующем примере показано правильное использование **парентфолдер** для JScript, VBScript и Visual Basic.

Присутствовал


```JScript
<script language="JScript">
    function fnFolderParentFolderJ()
    {
        var objShell    = new ActiveXObject("shell.application");
        var objFolder;
        var ssfPROGRAMS = 2;
        
        objFolder = objShell.NameSpace(ssfPROGRAMS);
        if (objFolder != null)
        {
            var objParentFolder;
                
            objParentFolder = objFolder.ParentFolder;
            if (objParentFolder != null)
            {
                alert(objParentFolder.Title);
            }
        }
    }
</script>
```



Сценариев


```VB
<script language="VBScript">
    function fnFolderParentFolderVB()
        dim objShell
        
        set objShell = CreateObject("shell.application")
        if (not objShell is nothing) then
            dim objFolder
            dim ssfPROGRAMS
            
            ssfPROGRAMS = 2
            set objFolder = objShell.NameSpace(ssfPROGRAMS)
            if (not objFolder is nothing) then
                dim objParentFolder
                        
                set objParentFolder = objFolder.ParentFolder
                if (not objParentFolder is nothing) then
                    alert(objParentFolder.Title)
                end if
                set objParentFolder = nothing
            end if
            set objFolder = nothing
        end if
        set objShell = nothing
    end function
 </script>
```



Visual Basic:


```VB
Private Sub fnFolderParentFolderVB()
    Dim objShell    As Shell
    Dim objFolder   As Folder
    Dim ssfPROGRAMS As Long
            
    ssfPROGRAMS = 2
    Set objShell = New Shell
    Set objFolder = objShell.NameSpace(ssfPROGRAMS)
    If (Not objFolder Is Nothing) Then
        Dim objParentFolder As Folder
                
        Set objParentFolder = objFolder.ParentFolder
        If (Not objParentFolder Is Nothing) Then
            Debug.Print objParentFolder.Title
        End If
        Set objParentFolder = Nothing
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



 

 




