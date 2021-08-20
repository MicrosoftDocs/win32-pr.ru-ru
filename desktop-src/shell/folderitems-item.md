---
description: Извлекает объект FolderItem для указанного элемента в коллекции.
ms.assetid: 164f823d-12d9-4950-a881-63837c53760d
title: Метод Фолдеритемс. Item (Шлдисп. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- FolderItems.Item
api_type:
- COM
api_location:
- Shell32.dll
ms.openlocfilehash: e246a1ada6cdf9935ae2ce9f8ca2a0ae25ced8ea08db8e98fef59a8fbc66ef40
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "117679478"
---
# <a name="folderitemsitem-method"></a>Фолдеритемс. Item, метод

Извлекает объект [**FolderItem**](folderitem.md) для указанного элемента в коллекции.

## <a name="syntax"></a>Синтаксис


```JScript
FolderItems.Item(
  [ iIndex ]
)
```



## <a name="parameters"></a>Параметры

<dl> <dt>

*ииндекс* \[ в необязательное\]
</dt> <dd>

Тип: **Variant**

Начинающийся с нуля индекс извлекаемого элемента. Это значение должно быть меньше значения свойства [**Count**](folderitems-count.md) .

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Ссылка на объект [**FolderItem**](folderitem.md) .

## <a name="examples"></a>Примеры

в следующем примере **элемент** используется для получения объекта [**FolderItem**](folderitem.md) , представляющего файл Notepad.exe, который находится в папке Windows. правильное использование отображается для JScript, VBScript и Visual Basic.

JScript:


```JScript
<script language="JScript">
    function fnFolderItemsItemJ()
    {
        var objShell = new ActiveXObject("shell.application");
        var objFolder;
        var ssfWINDOWS = 36;
        
        objFolder = objShell.NameSpace(ssfWINDOWS);
        if (objFolder != null)
        {
            var objFolderItems;
            
            objFolderItems = objFolder.Items();
            if (objFolderItems != null)
            {
                var objFolderItem;
                
                objFolderItem = objFolderItems.Item(objFolderItems.Count - 1);
                alert(objFolderItem.Name);
            }
        }
    }
</script>
```



Сценариев


```VB
<script language="VBScript">
    function fnFolderItemsItemVB()
        dim objShell
        
        set objShell = CreateObject("shell.application")
        if (not objShell is nothing) then
            dim objFolder
            dim ssfWINDOWS
                
            ssfWINDOWS = 36
            set objFolder = objShell.NameSpace(ssfWINDOWS)
            if (not objFolder is nothing) then
                dim objFolderItems
                        
                set objFolderItems = objFolder.Items()
                if (not objFolderItems is nothing) then
                    dim objFolderItem
                    
                    set objFolderItem = objFolderItems.Item
                        if (not objFolderItem is nothing) then
                            alert(objFolderItem.Name)
                        end if
                    set objFolderItem = nothing
                end if
                set objFolderItems = nothing
            end if
            set objFolder = nothing
        end if
        set objShell = nothing
    end function
</script>
```



Visual Basic:


```VB
Private Sub fnFolderItemsItemVB()
    Dim objShell   As Shell
    Dim objFolder  As Folder
    Dim ssfWINDOWS As Long
    
    ssfWINDOWS = 36
    Set objShell = New Shell
    Set objFolder = objShell.NameSpace(ssfWINDOWS)
        If (Not objFolder Is Nothing) Then
            Dim objFolderItems As FolderItems
            
            Set objFolderItems = objFolder.Items
                If (Not objFolderItems Is Nothing) Then
                    Dim objFolderItem As FolderItem
                    
                    Set objFolderItem = objFolderItems.Item("NOTEPAD.EXE")
                        If (Not objFolderItem Is Nothing) Then
                            Debug.Print objFolderItem.Path
                        End If
                    Set objFolderItem = Nothing
                End If
            Set objFolderItems = Nothing
        End If
    Set objFolder = Nothing
    Set objShell = Nothing
End Sub
```



## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------------------------|----------------------------------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Windows 2000 Professional, только для \[ настольных приложений Windows XP\]<br/>                                         |
| Минимальная версия сервера<br/> | Windows 2000 Server \[только классические приложения\]<br/>                                                           |
| Заголовок<br/>                   | <dl> <dt>Шлдисп. h</dt> </dl>                           |
| IDL<br/>                      | <dl> <dt>Шлдисп. idl</dt> </dl>                         |
| DLL<br/>                      | <dl> <dt>Shell32.dll (версия 4,71 или более поздняя)</dt> </dl> |



## <a name="see-also"></a>См. также

<dl> <dt>

[**фолдеритемс**](folderitems.md)
</dt> </dl>

 

 




