---
description: Выполняет команду для элемента.
ms.assetid: 569bdc88-15ef-4d08-923c-4f41e5ae5a38
title: FolderItem. Инвокеверб, метод (Шлдисп. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- FolderItem.InvokeVerb
api_type:
- COM
api_location:
- Shell32.dll
ms.openlocfilehash: 1f6c45c67bd8863b6cf1169670a4d087f29e4441c48592f850a683af5ef0bc1d
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "120111794"
---
# <a name="folderiteminvokeverb-method"></a>FolderItem. Инвокеверб, метод

Выполняет команду для элемента.

## <a name="syntax"></a>Синтаксис


```JScript
FolderItem.InvokeVerb(
  [ vVerb ]
)
```



## <a name="parameters"></a>Параметры

<dl> <dt>

*вверб* \[ в необязательное\]
</dt> <dd>

Тип: **Variant**

Строка, указывающая выполняемую команду. Это должно быть одно из значений, возвращаемых свойством [**FolderItemVerb.Name**](folderitemverb-name.md) элемента. Если команда не указана, будет вызвана команда по умолчанию.

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Этот метод не возвращает значение.

## <a name="remarks"></a>Remarks

Глагол — это строка, используемая для указания конкретного действия, которое поддерживает элемент. Вызов глагола эквивалентен выбору команды из контекстного меню элемента. Как правило, вызов команды запускает связанное приложение. например, при вызове команды "открыть" в .txtном файле файл открывается в текстовом редакторе, обычно Microsoft Блокнот. Дополнительные сведения о командах см. в статье [Запуск приложений](launch.md) .

Объект [**фолдеритемвербс**](folderitemverbs.md) представляет коллекцию команд, связанных с элементом. Глагол по умолчанию может различаться для различных элементов, но обычно это "Open".

## <a name="examples"></a>Примеры

в следующем примере используется **инвокеверб** для вызова глагола по умолчанию (в данном случае "open") в папке Windows. правильное использование отображается для JScript, VBScript и Visual Basic.

JScript:


```JScript
<script language="JScript">
    function fnFolderItemInvokeVerbJ()
    {
        var objShell = new ActiveXObject("shell.application");
        var objFolder2;
        var ssfWINDOWS = 36;
        
        objFolder2 = objShell.NameSpace(ssfWINDOWS);
        if (objFolder2 != null)
        {
            var objFolderItem;
            
            objFolderItem = objFolder2.Self;
            if (objFolderItem != null)
            {
                var szReturn;
                
                objFolderItem.InvokeVerb();
            }
        }
    }
</script>
```



Сценариев


```VB
<script language="VBScript">
    function fnFolderItemInvokeVerbVB()
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
                    dim szReturn
                                
                    objFolderItem.InvokeVerb()
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
Private Sub fnFolderItemInvokeVerbVB()
    Dim objShell   As Shell
    Dim objFolder2 As Folder2
    Dim ssfWINDOWS As Long
    
    ssfWINDOWS = 36
    Set objShell = New Shell
    Set objFolder2 = objShell.NameSpace(ssfWINDOWS)
        If (Not objFolder2 Is Nothing) Then
            Dim objFolderItem As FolderItem
            
            Set objFolderItem = objFolder2.Self
                If (Not objFolderItem Is Nothing) Then
                    Dim szReturn As String
                    
                    objFolderItem.InvokeVerb
                Else
                    'FolderItem object returned nothing.
                End If
            Set objFolderItem = Nothing
        Else
            'Folder object returned nothing.
        End If
    Set objFolder2 = Nothing
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

[**FolderItem**](folderitem.md)
</dt> <dt>

[**Команды**](folderitem-verbs.md)
</dt> <dt>

[**доит**](folderitemverb-doit.md)
</dt> </dl>

 

 




