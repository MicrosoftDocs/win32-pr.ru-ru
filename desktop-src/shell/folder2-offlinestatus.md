---
description: Содержит автономное состояние папки.
ms.assetid: b50b130d-0675-49b5-b730-f67ea1c71d8c
title: Свойство folder2. Оффлинестатус (Шлдисп. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Folder2.OfflineStatus
api_type:
- COM
api_location:
- Shell32.dll
ms.openlocfilehash: a2664a99fb103b41bd3b5040b3876b0cb92b8f9c010f420f93af7eb62a6f32bd
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "117860251"
---
# <a name="folder2offlinestatus-property"></a>Folder2. Оффлинестатус, свойство

Содержит автономное состояние папки.

Это свойство доступно только для чтения.

## <a name="syntax"></a>Синтаксис


```JScript
iOfflineStatus = Folder2.OfflineStatus
```



## <a name="property-value"></a>Значение свойства

**Целое число** , заданное в качестве одного из следующих значений.

<dt>



 (OFS \_ ДИРТИКАЧЕ)


</dt> <dd>

Сервер находится в режиме "в сети" с несинхронизированными изменениями.

</dd> <dt>



 (OFS \_ Активный


</dt> <dd>

Автономное кэширование не включено для этой папки.

</dd> <dt>



 (OFS \_ РАБОТА


</dt> <dd>

Сервер находится в автономном режиме.

</dd> <dt>



 (OFS \_ СОБРАНИЯ


</dt> <dd>

Сервер находится в режиме "в сети".

</dd> <dt>



 (OFS \_ СЕРВЕРБАКК)


</dt> <dd>

Сервер находится в автономном режиме, но может быть достигнут.

</dd> </dl>

## <a name="remarks"></a>Remarks

> [!Note]  
> Для правильной работы **оффлинестатус** необходимо включить автономные файлы с помощью параметров папки. Если параметр автономные файлы не включен, свойство возвращает значение **OFS \_ Inactive**.

 

## <a name="examples"></a>Примеры

в следующем примере показано правильное использование **оффлинестатус** для JScript, VBScript и Visual Basic.

JScript:


```JScript
<script language="JScript">
    function fnOfflineStatusJ()
    {
        var objShell   = new ActiveXObject("shell.application");
        var objFolder2 = new Object;
        
        objFolder2 = objShell.NameSpace("\\\\server\\share\\folder");
        if (objFolder2 != null)
        {
            var nReturn;

            nReturn = objFolder2.OfflineStatus;
        }
    }
</script>
```



Сценариев


```VB
<script language="VBScript">
    function fnOfflineStatusVB()
        dim objShell
        dim objFolder2
       
        set objShell = CreateObject("shell.application")
        set objFolder2 = objShell.NameSpace("\\server\share\folder")

        if (not objFolder2 is nothing) then
            dim nReturn

            nReturn = objFolder2.OfflineStatus
        end if

        set objFolder = nothing
        set objShell = nothing
    end function
</script>
```



Visual Basic:


```VB
Private Sub fnOfflineStatusVB()
    Dim objShell   As Shell
    Dim objFolder2 As Folder2
    
    Set objShell = New Shell
    Set objFolder2 = objShell.NameSpace("\\server\share\folder")

    If (Not objFolder2 Is Nothing) Then
        Dim nReturn As Integer
        
        nReturn = objFolder2.OfflineStatus()
    End If

    Set objFolder2 = Nothing
    Set objShell = Nothing
End Sub
```



## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Windows 2000 Professional, только для \[ настольных приложений Windows XP\]<br/>                                        |
| Минимальная версия сервера<br/> | Windows Только для \[ настольных приложений сервера 2003\]<br/>                                                          |
| Header<br/>                   | <dl> <dt>Шлдисп. h</dt> </dl>                          |
| IDL<br/>                      | <dl> <dt>Шлдисп. idl</dt> </dl>                        |
| DLL<br/>                      | <dl> <dt>Shell32.dll (версия 5,0 или более поздняя)</dt> </dl> |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[**Folder2**](folder2-object.md)
</dt> <dt>

[**Папка**](folder.md)
</dt> </dl>

 

 




