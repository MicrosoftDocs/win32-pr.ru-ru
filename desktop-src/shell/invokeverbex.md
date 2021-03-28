---
description: Выполняет команду для элемента оболочки.
ms.assetid: aac3f338-6074-4b1f-9b2f-e6206db52419
title: Шеллфолдеритем. Инвокевербекс, метод (Шлдисп. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ShellFolderItem.InvokeVerbEx
api_type:
- COM
api_location:
- Shell32.dll
ms.openlocfilehash: 627c2b40869ac9c509dcd645ec259de7db118235
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104984740"
---
# <a name="shellfolderiteminvokeverbex-method"></a>Шеллфолдеритем. Инвокевербекс, метод

Выполняет команду для элемента оболочки.

## <a name="syntax"></a>Синтаксис


```JScript
iRetVal = ShellFolderItem.InvokeVerbEx(
  [ vVerb ],
  [ vArgs ]
)
```



## <a name="parameters"></a>Параметры

<dl> <dt>

*вверб* \[ в необязательное\]
</dt> <dd>

Тип: **Variant**

**Значение типа Variant** , содержащее строку команды, соответствующую выполняемой команде. Оно должно быть одним из значений, возвращаемых свойством [**Name**](folderitemverb-name.md) элемента. Если команда не указана, выполняется команда по умолчанию.

</dd> <dt>

*варгс* \[ в необязательное\]
</dt> <dd>

Тип: **Variant**

**Вариант** , состоящий из строки с одним или несколькими аргументами команды, заданной параметром *вверб*. Формат этой строки зависит от конкретной команды.

</dd> </dl>

## <a name="remarks"></a>Примечания

Глагол — это строка, используемая для указания конкретного действия, которое поддерживает элемент. Как правило, вызов команды запускает связанное приложение. Например, вызов команды **Open** для TXT-файла обычно открывает файл в текстовом редакторе, обычно Microsoft Notepad. Объект [**фолдеритемвербс**](folderitemverbs.md) представляет коллекцию команд, связанных с элементом. Дальнейшее обсуждение глаголов см. в разделе [Запуск приложений](launch.md).

Этот метод аналогичен [**инвокеверб**](folderitem-invokeverb.md), но он позволяет задавать аргументы для команды, а также саму команду.

## <a name="examples"></a>Примеры

В следующих примерах показано правильное использование этого метода в JScript, VBScript и Visual Basic.

Присутствовал


```JScript
<script language="JScript">
    function fnFolderItem2InvokeVerbExJ()
    {
        var objShell = new ActiveXObject("shell.application");
        var objFolder2;
        var ssfWINDOWS = 36;
        
        objFolder2 = objShell.NameSpace(ssfWINDOWS);
        if (objFolder2 != null)
        {
            var objFolderItem;
            
            objFolderItem = objFolder2.ParseName("NOTEPAD.EXE");
            if (objFolderItem != null)
            {
                objFolderItem.InvokeVerbEx("open", "c:\\autoexec.bat");
            }
        }
    }
</script>
```



Сценариев


```VB
<script language="VBScript">
    function fnFolderItemInvokeVerbExVB()
        dim objShell
        
        set objShell = CreateObject("shell.application")
        if (not objShell is nothing) then
            dim objFolder2
            dim ssfWINDOWS
                
            ssfWINDOWS = 36
            set objFolder2 = objShell.NameSpace(ssfWINDOWS)
            if (not objFolder2 is nothing) then
                dim objFolderItem
                        
                set objFolderItem = objFolder2.Self
                if (not objFolderItem is nothing) then
                    objFolderItem.InvokeVerbEx()
                end if
                set objFolderItem = nothing
            end if
            set objFolder2 = nothing
        end if
        set objShell = nothing
    end function
 </script>
```



Visual Basic:


```VB
Private Sub fnFolderItem2InvokeVerbExVB()
    Dim objShell   As Shell
    Dim objFolder2 As Folder2
    Dim ssfWINDOWS As Long
    
    ssfWINDOWS = 36
    Set objShell = New Shell
    Set objFolder2 = objShell.NameSpace(ssfWINDOWS)
        If (Not objFolder2 Is Nothing) Then
            Dim objFolderItem2 As Object
            
            Set objFolderItem2 = objFolder2.ParseName("NOTEPAD.EXE")
                If (Not objFolderItem2 Is Nothing) Then
                    objFolderItem2.InvokeVerbEx ("open")
                Else
                    'FolderItem object returned nothing.
                End If
            Set objFolderItem2 = Nothing
        Else
            'Folder object returned nothing.
        End If
    Set objFolder2 = Nothing
    Set objShell = Nothing
End Sub
```



## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Windows 2000 Professional, только для \[ классических приложений Windows XP\]<br/>                                        |
| Минимальная версия сервера<br/> | \[Только для настольных приложений Windows Server 2003\]<br/>                                                          |
| Header<br/>                   | <dl> <dt>Шлдисп. h</dt> </dl>                          |
| IDL<br/>                      | <dl> <dt>Шлдисп. idl</dt> </dl>                        |
| DLL<br/>                      | <dl> <dt>Shell32.dll (версия 5,0 или более поздняя)</dt> </dl> |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[**шеллфолдеритем**](shellfolderitem-object.md)
</dt> <dt>

[**инвокеверб**](folderitem-invokeverb.md)
</dt> </dl>

 

 




