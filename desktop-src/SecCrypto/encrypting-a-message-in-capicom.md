---
description: Эта подпрограммы принимает строку, которая будет зашифрована, строку пароля, которая будет использоваться для создания ключа шифрования, и имя файла, в который будет записано зашифрованное сообщение.
ms.assetid: 9ad3199a-bca1-4990-80da-80744e349047
title: Шифрование сообщения в CAPICOM
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8039586736c09673644cacc90759e8d5f25b6e1a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "105664136"
---
# <a name="encrypting-a-message-in-capicom"></a>Шифрование сообщения в CAPICOM

\[CAPICOM — это 32-разрядный компонент, доступный для использования в следующих операционных системах: Windows Server 2008, Windows Vista и Windows XP. Вместо этого используйте платформа .NET Framework для реализации функций безопасности. Дополнительные сведения см. [в разделе альтернативы использованию элемента CAPICOM](alternatives-to-using-capicom.md).\]

Эта подпрограммы принимает строку, которая будет зашифрована, строку пароля, которая будет использоваться для создания ключа шифрования, и имя файла, в который будет записано зашифрованное сообщение. Все параметры передаются в подпрограммы по значениям. Чтобы расшифровать сообщение, необходимо использовать ту же строку пароля. Если пароль потерян, текст не может быть расшифрован. Конфиденциальность сообщения будет потеряна, если непредусмотренный получатель получит доступ к паролю.

> [!Note]  
> CAPICOM не поддерживает \# тип содержимого EncryptedData, но использует нестандартную структуру ASN для EncryptedData. В результате только CAPICOM может расшифровать объект CAPICOM EncryptedData.

 

При любой ошибке CAPICOM возвращается отрицательное десятичное значение свойства **Err. Number** . Дополнительные сведения см. в [**разделе \_ \_ код ошибки CAPICOM**](capicom-error-code.md). Сведения о положительных десятичных значениях **Err. Number** см. в файле Winerror. h.


```VB
Sub EncryptMessage(ByVal TobeEncrypted As String, ByVal hidden _
    As String, ByVal filename As String)

    On Error GoTo ErrorHandler

    ' Declare and initialize an EncryptedData object.
    ' Algorithm.Name and KeyLength do not need to be set.

    Dim message As New EncryptedData
    message.Content = Tobeencrypted
    message.SetSecret(hidden)
    ' Optionally, the encryption algorithm and key length can be set.
    ' If these properties are not set, the default algorithm and key 
    ' length are used.
    ' Information about the algorithm and key length is saved with 
    ' the encrypted string and the individual decrypting the message
    ' does not need to set these properties.

    message.Algorithm.Name = CAPICOM_ENCRYPTION_ALGORITHM_DES

    ' Declare the string that will hold the encrypted message.

    Dim encryptedmessage As String

    ' Encrypt the message storing the result in the encryptedmessage
    ' string.
    encryptedmessage = message.Encrypt

    ' Optionally, check the length of the encrypted string to 
    ' make sure that the encrypt method worked. 

    If Len(encryptedmessage) < 1 Then
        MsgBox("no message encrypted. ")
    Else
        MsgBox(" Message is " & Len(encryptedmessage) & " characters")

        ' Open an output file and write the encrypted message to the
        ' file. The file is not opened if there is no message
        ' to write.
    Open filename For Output As #1
    Write #1, encryptedmessage
    Close #1
        MsgBox("Encrypted message written to file ")
    End If

    ' Release the EncryptedData object.
    message = Nothing

    Exit Sub

ErrorHandler:
    If Err.Number > 0 Then
        MsgBox("Visual Basic error found:" & Err.Description)
    Else
        MsgBox("CAPICOM error found : " & Err.Number)
    End If
End Sub
```



 

 



