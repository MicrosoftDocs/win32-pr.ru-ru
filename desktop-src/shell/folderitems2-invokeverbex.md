---
description: Выполняет команду для коллекции объектов FolderItem. Этот метод является расширением метода Инвокеверб, что позволяет дополнительно управлять операцией с помощью набора флагов.
ms.assetid: 2c02985d-8877-4a02-a232-6aeb1716928c
title: FolderItems2. Инвокевербекс, метод (Шлдисп. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- FolderItems2.InvokeVerbEx
api_type:
- COM
api_location:
- Shell32.dll
ms.openlocfilehash: 94d62de132a61bb357acac77aea41d2278ba1eb4453afa826ac32be90095ab25
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "117860153"
---
# <a name="folderitems2invokeverbex-method"></a>FolderItems2. Инвокевербекс, метод

Выполняет команду для коллекции объектов [**FolderItem**](folderitem.md) . Этот метод является расширением метода [**инвокеверб**](folderitem-invokeverb.md) , что позволяет дополнительно управлять операцией с помощью набора флагов.

## <a name="syntax"></a>Синтаксис


```JScript
iRetVal = FolderItems2.InvokeVerbEx(
  [ vVerb ],
  [ vArgs ]
)
```



## <a name="parameters"></a>Параметры

<dl> <dt>

*вверб* \[ в необязательное\]
</dt> <dd>

Тип: **Variant**

**Вариант** со строкой команды, соответствующей выполняемой команде. Если команда не указана, выполняется команда по умолчанию.

</dd> <dt>

*варгс* \[ в необязательное\]
</dt> <dd>

Тип: **Variant**

**Вариант** , состоящий из строки с одним или несколькими аргументами команды, заданной параметром *вверб*. Формат этой строки зависит от конкретной команды.

</dd> </dl>

## <a name="remarks"></a>Remarks

Глагол — это строка, используемая для указания конкретного действия, связанного с элементом или коллекцией элементов. Как правило, вызов команды запускает связанное приложение. например, вызов команды **open** для файла .txt обычно открывает файл в текстовом редакторе, обычно Microsoft Блокнот. Дальнейшее обсуждение глаголов см. в разделе [Запуск приложений](launch.md).

## <a name="examples"></a>Примеры

В следующем примере **инвокевербекс** используется для вызова глагола по умолчанию ("Open") на **Мой компьютер**. правильное использование отображается для JScript, VBScript и Visual Basic.

JScript:


```JScript
<script language="JScript">
    function fnFolderItems2InvokeVerbExJ()
    {
        var objShell  = new ActiveXObject("shell.application");
        var objFolder;
        var ssfDRIVES = 17;
        
        objFolder = objShell.NameSpace(ssfDRIVES);
        if (objFolder != null)
        {
            var objFolderItems2;
            
            objFolderItems2 = objFolder.Items();
            if (objFolderItems2 != null)
            {
                objFolderItems2.InvokeVerbEx();
            }
        }
    }
</script>
```



Сценариев


```VB
<script language="VBScript">
    function fnFolderItems2InvokeVerbExVB()
        dim objShell
        
        set objShell = CreateObject("shell.application")
        if (not objShell is nothing) then
            dim objFolder
            dim ssfDRIVES
                
            ssfWINDOWS = 17
            set objFolder = objShell.NameSpace(ssfWINDOWS)
            if (not objFolder is nothing) then
                dim objFolderItems2
                        
                set objFolderItems2 = objFolder.Items()
                if (not objFolderItems2 is nothing) then
                    objFolderItems2.InvokeVerbEx
                end if
                set objFolderItems2 = nothing
            end if
            set objFolder = nothing
        end if
        set objShell = nothing
    end function
</script>
```



Visual Basic:


```VB
Private Sub fnFolderItems2InvokeVerbExVB()
    Dim objShell      As Shell
    Dim objFolder     As Folder2
    Dim ssfDRIVES     As Long
    
    ssfDRIVES = 17
    Set objShell = New Shell
    Set objFolder = objShell.NameSpace(ssfDRIVES)
        If (Not objFolder Is Nothing) Then
            Dim objFolderItems2 As FolderItems
            
            Set objFolderItems2 = objFolder.Items
                If (Not objFolderItems2 Is Nothing) Then
                    objFolderItems2.InvokeVerbEx
                End If
            Set objFolderItems2 = Nothing
        End If
    Set objFolder = Nothing
    Set objShell = Nothing
End Sub
```



## <a name="requirements"></a>Requirements (Требования)



| Требование | Значение |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Windows 2000 Professional, только для \[ настольных приложений Windows XP\]<br/>                                        |
| Минимальная версия сервера<br/> | Windows Только для \[ настольных приложений сервера 2003\]<br/>                                                          |
| Header<br/>                   | <dl> <dt>Шлдисп. h</dt> </dl>                          |
| IDL<br/>                      | <dl> <dt>Шлдисп. idl</dt> </dl>                        |
| DLL<br/>                      | <dl> <dt>Shell32.dll (версия 5,0 или более поздняя)</dt> </dl> |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[**FolderItems2**](folderitems2-object.md)
</dt> <dt>

[**инвокеверб**](folderitem-invokeverb.md)
</dt> </dl>

 

 




