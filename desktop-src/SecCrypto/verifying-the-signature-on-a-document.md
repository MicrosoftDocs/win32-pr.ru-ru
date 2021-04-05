---
description: При получении подписанного документа можно проверить допустимость подписи или подписей.
ms.assetid: 088915d8-768c-4378-a9dd-9347a428aff9
title: Проверка подписи документа
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6f2886edcb9629011ddf1a0b5fb45a12a11f0556
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "103910068"
---
# <a name="verifying-the-signature-on-a-document"></a><span data-ttu-id="fae68-103">Проверка подписи документа</span><span class="sxs-lookup"><span data-stu-id="fae68-103">Verifying the Signature on a Document</span></span>

<span data-ttu-id="fae68-104">\[CAPICOM — это 32-разрядный компонент, доступный для использования в следующих операционных системах: Windows Server 2008, Windows Vista и Windows XP.</span><span class="sxs-lookup"><span data-stu-id="fae68-104">\[CAPICOM is a 32-bit only component that is available for use in the following operating systems: Windows Server 2008, Windows Vista, and Windows XP.</span></span> <span data-ttu-id="fae68-105">Вместо этого используйте платформа .NET Framework для реализации функций безопасности.</span><span class="sxs-lookup"><span data-stu-id="fae68-105">Instead, use the .NET Framework to implement security features.</span></span> <span data-ttu-id="fae68-106">Дополнительные сведения см. [в разделе альтернативы использованию элемента CAPICOM](alternatives-to-using-capicom.md).\]</span><span class="sxs-lookup"><span data-stu-id="fae68-106">For more information, see [Alternatives to Using CAPICOM](alternatives-to-using-capicom.md).\]</span></span>

<span data-ttu-id="fae68-107">При получении подписанного документа можно проверить допустимость подписи или подписей.</span><span class="sxs-lookup"><span data-stu-id="fae68-107">When a signed document is received, the validity of the signature or signatures can be checked.</span></span> <span data-ttu-id="fae68-108">Подпись можно проверить для:</span><span class="sxs-lookup"><span data-stu-id="fae68-108">A signature can be checked for:</span></span>

-   <span data-ttu-id="fae68-109">Срок действия хэша подписи</span><span class="sxs-lookup"><span data-stu-id="fae68-109">Validity of the signature hash</span></span>
-   <span data-ttu-id="fae68-110">Срок действия сертификата подписи</span><span class="sxs-lookup"><span data-stu-id="fae68-110">Validity of the signer's certificate</span></span>

<span data-ttu-id="fae68-111">[*Хэш*](../secgloss/h-gly.md) подписи расшифровывается с помощью [*открытого ключа*](../secgloss/p-gly.md) , найденного в [*сертификате*](../secgloss/c-gly.md)подписывания, который входит в состав подписи.</span><span class="sxs-lookup"><span data-stu-id="fae68-111">The signature [*hash*](../secgloss/h-gly.md) is decrypted using the [*public key*](../secgloss/p-gly.md) of the signer found on the signer's [*certificate*](../secgloss/c-gly.md), included as part of the signature.</span></span> <span data-ttu-id="fae68-112">Если Расшифрованная подпись соответствует новому хэшу исходного документа, то подпись была создана владельцем закрытого ключа, связанного с открытым ключом, используемым для расшифровки хэша.</span><span class="sxs-lookup"><span data-stu-id="fae68-112">If the decrypted signature matches a new hash of the original document, the signature was created by the owner of the private key associated with the public key used to decrypt the hash.</span></span> <span data-ttu-id="fae68-113">Кроме того, документ, на котором основана подпись, гарантированно не будет изменяться после создания подписи.</span><span class="sxs-lookup"><span data-stu-id="fae68-113">In addition, the document that the signature is based on is guaranteed not to have been changed after the signature was created.</span></span>

<span data-ttu-id="fae68-114">Сертификат, который предоставил открытый ключ и удостоверение, может также проверяться на допустимость, включая такие проблемы, как подтверждение отзыва сертификата, срок действия сертификата или сертификат, выданный издателем доверенного сертификата.</span><span class="sxs-lookup"><span data-stu-id="fae68-114">The certificate that provided the public key and the identity of the signer can also be checked for validity including such issues as whether the certificate has been revoked, whether the certificate is out of date, or whether the certificate was issued by a trusted certificate issuer.</span></span>

<span data-ttu-id="fae68-115">В следующем примере проверяется, что содержимое, подписанное и объект **сигнеддата** , считывается из файла, а подпись и срок действия сертификата, используемого для создания подписи, проверяются.</span><span class="sxs-lookup"><span data-stu-id="fae68-115">In the following example, the content signed and the **SignedData** object are read in from a file and the signature and the validity of the certificate used to create the signature are checked.</span></span>

> [!Note]  
> <span data-ttu-id="fae68-116">Если подпись недействительна или сертификат подписан недопустимым, возникает исключение, и программа проверки должна справиться с исключением.</span><span class="sxs-lookup"><span data-stu-id="fae68-116">If the signature is not cryptographically valid or the certificate of the signer is not valid, an exception is raised and the verifying program must handle the exception.</span></span> <span data-ttu-id="fae68-117">При любой ошибке CAPICOM возвращается отрицательное десятичное значение **Err. Number** .</span><span class="sxs-lookup"><span data-stu-id="fae68-117">On any CAPICOM error, a negative decimal value of **Err.Number** is returned.</span></span> <span data-ttu-id="fae68-118">Дополнительные сведения см. в [**разделе \_ \_ код ошибки CAPICOM**](capicom-error-code.md).</span><span class="sxs-lookup"><span data-stu-id="fae68-118">For more information, see [**CAPICOM\_ERROR\_CODE**](capicom-error-code.md).</span></span> <span data-ttu-id="fae68-119">Сведения о положительных десятичных значениях **Err. Number** см. в файле Winerror. h.</span><span class="sxs-lookup"><span data-stu-id="fae68-119">For information about positive decimal values of **Err.Number**, see Winerror.h.</span></span>

 


```VB
Sub VerifySig(ByVal FileToVerify As String, ByVal FileBase As String)
On Error GoTo ErrorHandler

Dim sdContent As String
Dim sdCheck As String
Dim mySD As SignedData
Set mySD = New SignedData

' Open a file and read the signature.
Open FileToVerify For Input As #1
Input #1, sdCheck
Close #1

' Open a file and input the plaintext content that was signed.
Open FileBase For Input As #2
Input #2, sdContent
Close #1

' Set the detached content upon which the signature is based.
mySD.Content = sdContent

' Verify the detached signature.
On Error Resume Next
    mySD.Verify sdCheck, True
If Err.Number <> 0 Then
    MsgBox "Signature verification failed. " & Err.Description
Else
    MsgBox "Verification complete."
End If

' Release the SignedData object.
Set mySD = Nothing

Exit Sub
ErrorHandler:
    If Err.Number > 0 Then
        MsgBox "Visual Basic error found: " & Err.Description
    Else
        MsgBox "CAPICOM error found: " & Hex(Err.Number)
    End If
End Sub

```



 

 
