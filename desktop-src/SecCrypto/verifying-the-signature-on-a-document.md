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
# <a name="verifying-the-signature-on-a-document"></a>Проверка подписи документа

\[CAPICOM — это 32-разрядный компонент, доступный для использования в следующих операционных системах: Windows Server 2008, Windows Vista и Windows XP. Вместо этого используйте платформа .NET Framework для реализации функций безопасности. Дополнительные сведения см. [в разделе альтернативы использованию элемента CAPICOM](alternatives-to-using-capicom.md).\]

При получении подписанного документа можно проверить допустимость подписи или подписей. Подпись можно проверить для:

-   Срок действия хэша подписи
-   Срок действия сертификата подписи

[*Хэш*](../secgloss/h-gly.md) подписи расшифровывается с помощью [*открытого ключа*](../secgloss/p-gly.md) , найденного в [*сертификате*](../secgloss/c-gly.md)подписывания, который входит в состав подписи. Если Расшифрованная подпись соответствует новому хэшу исходного документа, то подпись была создана владельцем закрытого ключа, связанного с открытым ключом, используемым для расшифровки хэша. Кроме того, документ, на котором основана подпись, гарантированно не будет изменяться после создания подписи.

Сертификат, который предоставил открытый ключ и удостоверение, может также проверяться на допустимость, включая такие проблемы, как подтверждение отзыва сертификата, срок действия сертификата или сертификат, выданный издателем доверенного сертификата.

В следующем примере проверяется, что содержимое, подписанное и объект **сигнеддата** , считывается из файла, а подпись и срок действия сертификата, используемого для создания подписи, проверяются.

> [!Note]  
> Если подпись недействительна или сертификат подписан недопустимым, возникает исключение, и программа проверки должна справиться с исключением. При любой ошибке CAPICOM возвращается отрицательное десятичное значение **Err. Number** . Дополнительные сведения см. в [**разделе \_ \_ код ошибки CAPICOM**](capicom-error-code.md). Сведения о положительных десятичных значениях **Err. Number** см. в файле Winerror. h.

 


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



 

 
