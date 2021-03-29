---
description: Эта подпрограммы принимает строку пароля, которая используется для создания ключа шифрования сеанса, и имя файла, из которого будет прочитано зашифрованное сообщение. Все параметры передаются в подпрограммы по значениям.
ms.assetid: 70f23d93-2bca-419b-9de7-e52ce4fb1350
title: Расшифровка сообщения в CAPICOM
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ba984bad7d9289eaf89725e9598a4330f16b49ab
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "105647357"
---
# <a name="decrypting-a-message-in-capicom"></a><span data-ttu-id="3bddd-104">Расшифровка сообщения в CAPICOM</span><span class="sxs-lookup"><span data-stu-id="3bddd-104">Decrypting a Message in CAPICOM</span></span>

<span data-ttu-id="3bddd-105">\[CAPICOM — это 32-разрядный компонент, доступный для использования в следующих операционных системах: Windows Server 2008, Windows Vista и Windows XP.</span><span class="sxs-lookup"><span data-stu-id="3bddd-105">\[CAPICOM is a 32-bit only component that is available for use in the following operating systems: Windows Server 2008, Windows Vista, and Windows XP.</span></span> <span data-ttu-id="3bddd-106">Вместо этого используйте платформа .NET Framework для реализации функций безопасности.</span><span class="sxs-lookup"><span data-stu-id="3bddd-106">Instead, use the .NET Framework to implement security features.</span></span> <span data-ttu-id="3bddd-107">Дополнительные сведения см. [в разделе альтернативы использованию элемента CAPICOM](alternatives-to-using-capicom.md).\]</span><span class="sxs-lookup"><span data-stu-id="3bddd-107">For more information, see [Alternatives to Using CAPICOM](alternatives-to-using-capicom.md).\]</span></span>

<span data-ttu-id="3bddd-108">Эта подпрограммы принимает строку пароля, которая используется для создания ключа шифрования сеанса, и имя файла, из которого будет прочитано зашифрованное сообщение.</span><span class="sxs-lookup"><span data-stu-id="3bddd-108">This subroutine take a password string to be used to generate a session encryption key, and the name of a file from which an encrypted message will be read.</span></span> <span data-ttu-id="3bddd-109">Все параметры передаются в подпрограммы по значениям.</span><span class="sxs-lookup"><span data-stu-id="3bddd-109">All parameters are passed into the subroutine by values.</span></span>

> [!Note]  
> <span data-ttu-id="3bddd-110">CAPICOM не поддерживает \# тип содержимого EncryptedData, но использует нестандартную структуру ASN для EncryptedData.</span><span class="sxs-lookup"><span data-stu-id="3bddd-110">CAPICOM does not support the PKCS \#7 EncryptedData content type but uses a nonstandard ASN structure for EncryptedData.</span></span> <span data-ttu-id="3bddd-111">Таким образом, только CAPICOM может расшифровать объект CAPICOM EncryptedData.</span><span class="sxs-lookup"><span data-stu-id="3bddd-111">Therefore, only CAPICOM can decrypt a CAPICOM EncryptedData object.</span></span>

 

<span data-ttu-id="3bddd-112">Если расшифровка не удалась, значение **Err. Number** проверяется, чтобы определить, была ли ошибка вызвана использованием пароля, который не соответствует паролю, используемому для шифрования сообщения.</span><span class="sxs-lookup"><span data-stu-id="3bddd-112">If decryption fails, the **Err.Number** value is checked to determine whether the error was caused by the use of a password that did not match the password used to encrypt the message.</span></span> <span data-ttu-id="3bddd-113">В этом случае возвращается ошибка "не превышать \_ Допустимые \_ данные".</span><span class="sxs-lookup"><span data-stu-id="3bddd-113">In this case, the NTE\_BAD\_DATA error is returned.</span></span>

<span data-ttu-id="3bddd-114">При любой ошибке CAPICOM возвращается отрицательное десятичное значение **Err. Number** .</span><span class="sxs-lookup"><span data-stu-id="3bddd-114">On any CAPICOM error, a negative decimal value of **Err.Number** is returned.</span></span> <span data-ttu-id="3bddd-115">Дополнительные сведения см. в [**разделе \_ \_ код ошибки CAPICOM**](capicom-error-code.md).</span><span class="sxs-lookup"><span data-stu-id="3bddd-115">For more information, see [**CAPICOM\_ERROR\_CODE**](capicom-error-code.md).</span></span> <span data-ttu-id="3bddd-116">Сведения о положительных десятичных значениях **Err. Number** см. в файле Winerror. h.</span><span class="sxs-lookup"><span data-stu-id="3bddd-116">For information about positive decimal values of **Err.Number**, see Winerror.h.</span></span>


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



 

 



