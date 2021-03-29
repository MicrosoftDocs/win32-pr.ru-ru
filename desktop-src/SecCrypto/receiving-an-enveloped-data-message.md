---
description: Чтобы расшифровать запечатанное сообщение, получатель соответствует сертификату из хранилища My, имеющему доступный закрытый ключ с сертификатом в сообщении в конверте.
ms.assetid: 536f9977-102c-4df9-9d07-97b4b434b845
title: Получение сообщения с упакованными данными
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9d32276193e8fd03904aed1ad626cd3ed241c654
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "103912820"
---
# <a name="receiving-an-enveloped-data-message"></a><span data-ttu-id="3f629-103">Получение сообщения с упакованными данными</span><span class="sxs-lookup"><span data-stu-id="3f629-103">Receiving an Enveloped Data Message</span></span>

<span data-ttu-id="3f629-104">\[CAPICOM — это 32-разрядный компонент, доступный для использования в следующих операционных системах: Windows Server 2008, Windows Vista и Windows XP.</span><span class="sxs-lookup"><span data-stu-id="3f629-104">\[CAPICOM is a 32-bit only component that is available for use in the following operating systems: Windows Server 2008, Windows Vista, and Windows XP.</span></span> <span data-ttu-id="3f629-105">Вместо этого используйте платформа .NET Framework для реализации функций безопасности.</span><span class="sxs-lookup"><span data-stu-id="3f629-105">Instead, use the .NET Framework to implement security features.</span></span> <span data-ttu-id="3f629-106">Дополнительные сведения см. [в разделе альтернативы использованию элемента CAPICOM](alternatives-to-using-capicom.md).\]</span><span class="sxs-lookup"><span data-stu-id="3f629-106">For more information, see [Alternatives to Using CAPICOM](alternatives-to-using-capicom.md).\]</span></span>

<span data-ttu-id="3f629-107">Чтобы расшифровать запечатанное сообщение, получатель соответствует [*сертификату*](../secgloss/c-gly.md) из хранилища My, имеющему доступный закрытый ключ с сертификатом в сообщении в конверте.</span><span class="sxs-lookup"><span data-stu-id="3f629-107">To decrypt an enveloped message, the recipient matches a [*certificate*](../secgloss/c-gly.md) from the My store that has an available private key with a certificate in the enveloped message.</span></span> <span data-ttu-id="3f629-108">Если совпадение найдено, зашифрованный ключ, связанный с этим сертификатом, расшифровывается, и для расшифровки запечатанного сообщения используется расшифрованный ключ.</span><span class="sxs-lookup"><span data-stu-id="3f629-108">If a match is found, the encrypted key associated with that certificate is decrypted and that decrypted key is used to decrypt the enveloped message.</span></span> <span data-ttu-id="3f629-109">Получатель сообщения, у которого нет совпадающего сертификата с доступным закрытым ключом, не может расшифровать сообщение.</span><span class="sxs-lookup"><span data-stu-id="3f629-109">A message recipient that does not have a matching certificate with an available private key cannot decrypt the message.</span></span>

<span data-ttu-id="3f629-110">В приведенном ниже примере имя файла передается в подпрограммы, открывается этот файл, а сообщение с оболочкой считывается в.</span><span class="sxs-lookup"><span data-stu-id="3f629-110">In the example that follows, a file name is passed into the subroutine, that file is opened and an enveloped message is read in.</span></span> <span data-ttu-id="3f629-111">После этого сообщение с оболочкой расшифровывается.</span><span class="sxs-lookup"><span data-stu-id="3f629-111">The enveloped message is then decrypted.</span></span> <span data-ttu-id="3f629-112">Этапы сопоставления сертификата пользователя с сертификатом в запечатанном сообщении, расшифровки ключа шифрования и, наконец, расшифровки сообщения, выполняются в фоновом режиме.</span><span class="sxs-lookup"><span data-stu-id="3f629-112">The steps of matching a user certificate with a certificate in the enveloped message, of decrypting the encryption key, and finally of decrypting the message are all done behind the scenes.</span></span> <span data-ttu-id="3f629-113">Если сопоставление сертификата не найдено или происходит сбой расшифровки, возникает ошибка.</span><span class="sxs-lookup"><span data-stu-id="3f629-113">An error is raised if a certificate match is not found or if the decryption fails.</span></span>

<span data-ttu-id="3f629-114">При любой ошибке CAPICOM возвращается отрицательное десятичное значение **Err. Number** .</span><span class="sxs-lookup"><span data-stu-id="3f629-114">On any CAPICOM error, a negative decimal value of **Err.Number** is returned.</span></span> <span data-ttu-id="3f629-115">Дополнительные сведения см. в [**разделе \_ \_ код ошибки CAPICOM**](capicom-error-code.md).</span><span class="sxs-lookup"><span data-stu-id="3f629-115">For more information, see [**CAPICOM\_ERROR\_CODE**](capicom-error-code.md).</span></span> <span data-ttu-id="3f629-116">Сведения о положительных десятичных значениях **Err. Number** см. в файле Winerror. h.</span><span class="sxs-lookup"><span data-stu-id="3f629-116">For information about positive decimal values of **Err.Number**, see Winerror.h.</span></span>


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



 

 
