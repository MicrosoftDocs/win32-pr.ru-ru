---
description: Чтобы расшифровать запечатанное сообщение, получатель соответствует сертификату из хранилища My, имеющему доступный закрытый ключ с сертификатом в сообщении в конверте.
ms.assetid: 536f9977-102c-4df9-9d07-97b4b434b845
title: Получение сообщения с упакованными данными
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 831413825040dd9ba4e297108e11d6e397dc6097ddc369eb802d9fe220aae783
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "117975568"
---
# <a name="receiving-an-enveloped-data-message"></a>Получение сообщения с упакованными данными

\[CAPICOM — это 32-разрядный компонент, доступный для использования в следующих операционных системах: Windows Server 2008, Windows Vista и Windows XP. вместо этого используйте платформа .NET Framework для реализации функций безопасности. Дополнительные сведения см. [в разделе альтернативы использованию элемента CAPICOM](alternatives-to-using-capicom.md).\]

Чтобы расшифровать запечатанное сообщение, получатель соответствует [*сертификату*](../secgloss/c-gly.md) из хранилища My, имеющему доступный закрытый ключ с сертификатом в сообщении в конверте. Если совпадение найдено, зашифрованный ключ, связанный с этим сертификатом, расшифровывается, и для расшифровки запечатанного сообщения используется расшифрованный ключ. Получатель сообщения, у которого нет совпадающего сертификата с доступным закрытым ключом, не может расшифровать сообщение.

В приведенном ниже примере имя файла передается в подпрограммы, открывается этот файл, а сообщение с оболочкой считывается в. После этого сообщение с оболочкой расшифровывается. Этапы сопоставления сертификата пользователя с сертификатом в запечатанном сообщении, расшифровки ключа шифрования и, наконец, расшифровки сообщения, выполняются в фоновом режиме. Если сопоставление сертификата не найдено или происходит сбой расшифровки, возникает ошибка.

При любой ошибке CAPICOM возвращается отрицательное десятичное значение **Err. Number** . Дополнительные сведения см. в [**разделе \_ \_ код ошибки CAPICOM**](capicom-error-code.md). Сведения о положительных десятичных значениях **Err. Number** см. в файле Winerror. h.


```VB
Sub ReceiveMessage(ByVal InFile As String)
On Error GoTo ErrorHandler

'Declare an EnvelopedData object

Dim Envmessage As New EnvelopedData

'Declare a string variable to hold the encrypted message.

Dim Encrypted As String

' Open an input file and read in the encrypted message
Open InFile For Input As #1
Input #1, Encrypted
Close #1

' If the length of the input string is greater than 0, 
' an encrypted message string is available. Decrypt the message.
' Note: to decrypt the message, a certificate with access to
' a user's private key must be available, and that certificate must
' match one of the certificates in the Recipients collection of 
' certificates.
If Len(Encrypted) > 0 Then
    ' Receive and decrypt the message
    Envmessage.Decrypt encrypted
    
    ' Display the decrypted message.
    MsgBox Envmessage.Content
Else
    MsgBox "No enveloped message was read in."
End If
' Release the EncryptedData object.
Set Envmessage = Nothing
Exit Sub

ErrorHandler:
If Err.Number > 0 Then
    MsgBox "Visual Basic error found:" & Err.Description
Else
    MsgBox "CAPICOM error found : " & Err.Number
End If
End Sub
```



 

 
