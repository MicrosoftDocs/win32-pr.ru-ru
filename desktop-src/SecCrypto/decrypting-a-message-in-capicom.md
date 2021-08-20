---
description: Эта подпрограммы принимает строку пароля, которая используется для создания ключа шифрования сеанса, и имя файла, из которого будет прочитано зашифрованное сообщение. Все параметры передаются в подпрограммы по значениям.
ms.assetid: 70f23d93-2bca-419b-9de7-e52ce4fb1350
title: Расшифровка сообщения в CAPICOM
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 744878378fbe2791e66151e451029be8adde2435b451d540196a1082c4e005f3
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "117767762"
---
# <a name="decrypting-a-message-in-capicom"></a>Расшифровка сообщения в CAPICOM

\[CAPICOM — это 32-разрядный компонент, доступный для использования в следующих операционных системах: Windows Server 2008, Windows Vista и Windows XP. вместо этого используйте платформа .NET Framework для реализации функций безопасности. Дополнительные сведения см. [в разделе альтернативы использованию элемента CAPICOM](alternatives-to-using-capicom.md).\]

Эта подпрограммы принимает строку пароля, которая используется для создания ключа шифрования сеанса, и имя файла, из которого будет прочитано зашифрованное сообщение. Все параметры передаются в подпрограммы по значениям.

> [!Note]  
> CAPICOM не поддерживает \# тип содержимого EncryptedData, но использует нестандартную структуру ASN для EncryptedData. Таким образом, только CAPICOM может расшифровать объект CAPICOM EncryptedData.

 

Если расшифровка не удалась, значение **Err. Number** проверяется, чтобы определить, была ли ошибка вызвана использованием пароля, который не соответствует паролю, используемому для шифрования сообщения. В этом случае возвращается ошибка "не превышать \_ Допустимые \_ данные".

При любой ошибке CAPICOM возвращается отрицательное десятичное значение **Err. Number** . Дополнительные сведения см. в [**разделе \_ \_ код ошибки CAPICOM**](capicom-error-code.md). Сведения о положительных десятичных значениях **Err. Number** см. в файле Winerror. h.


```VB
Sub DecryptMessage(ByVal hidden As String, ByVal filename As String)
On Error goto ErrorHandler

'Declare an EncryptedData object

Dim message As New EncryptedData

'Declare a string variable to hold the encrypted message.
Dim encrypted As String

' Open an input file and read in the encrypted message
Open filename For Input As #1
Input #1, encrypted
Close #1

' If a message was read in (the length of the input string is 
' greater than 0), set the password and decrypt the message.
If Len(encrypted) > 0 then
    ' Set the password used to generate the key
    ' used to decrypt the message. If the password
    ' not the same as the password used when the message
    ' was encrypted, decryption will fail.
    ' The algorithm name and key length set in the encrypting
    ' process are automatically used to decrypt the message. 
    message.SetSecret hidden
    message.Decrypt encrypted
    ' Display the decrypted message.
    MsgBox message.Content
else
    msgbox "No encrypted message was read in.
endif

' Release the EncryptedData object and exit the subroutine.
Set message = Nothing
Exit Sub

ErrorHandler:
If Err.Number > 0 Then
    MsgBox "Visual Basic error found:" & Err.Description
Else
'    Check for a bad password error.
    If Err.Number = -2146893819 Then
        MsgBox "Error. The password may not be correct."
    Else
        MsgBox "CAPICOM error found : " & Err.Number
    End If
End If
End Sub
```



 

 



