---
description: Объясняет, как приложение получает сертификат.
ms.assetid: 7f87dcf5-b434-4f63-abcd-6873831d22bc
title: Получение возвращенного сертификата
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 73853250c581e460360f5490defc0c94e76e5be3
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "105684329"
---
# <a name="receiving-the-returned-certificate"></a><span data-ttu-id="64182-103">Получение возвращенного сертификата</span><span class="sxs-lookup"><span data-stu-id="64182-103">Receiving the Returned Certificate</span></span>

<span data-ttu-id="64182-104">Когда центр сертификации (ЦС) проверил сведения об удостоверении инициатора запроса и удовлетворен, что он является владельцем закрытого ключа и что данные об этом инициаторе являются точными, ЦС формирует сертификат X. 509, подписывает его, упаковывает в него все необходимые сертификаты (например, собственный сертификат ЦС) в сообщении и отправляет сообщение инициатору запроса.</span><span class="sxs-lookup"><span data-stu-id="64182-104">When the certification authority (CA) has verified the requester's identity information and is satisfied that the requester is the owner of the private key and that the data about that requester is accurate, the CA constructs an X.509 certificate, signs it, packages it with any other needed certificates (such as the CA's own certificate) in a message, and sends the message to the requester.</span></span> <span data-ttu-id="64182-105">Сообщение может быть \# сообщением PKCS 7 или запросом CMC (шаблоны v2 выводят ответ CMC).</span><span class="sxs-lookup"><span data-stu-id="64182-105">The message can be a PKCS \#7 message or a CMC response (V2 templates result in a CMC response).</span></span>

<span data-ttu-id="64182-106">Принимающее приложение передает сообщение в Управление регистрацией сертификата.</span><span class="sxs-lookup"><span data-stu-id="64182-106">The receiving application passes the message to the Certificate Enrollment Control.</span></span> <span data-ttu-id="64182-107">После этого Управление регистрацией сертификата открывает сообщение и извлекает сертификаты.</span><span class="sxs-lookup"><span data-stu-id="64182-107">The Certificate Enrollment Control then opens the message and extracts the certificates.</span></span> <span data-ttu-id="64182-108">Пользователю предлагается диалоговое окно с вопросом, будет ли пользователь принимать самозаверяющие сертификаты в корневом хранилище.</span><span class="sxs-lookup"><span data-stu-id="64182-108">The user is prompted with a dialog box asking whether the user will accept self-signed certificates in the "Root" store.</span></span> <span data-ttu-id="64182-109">Если пользователь принимает корневой сертификат, остальные сертификаты (за исключением сертификата инициатора запроса) помещаются в хранилище CA.</span><span class="sxs-lookup"><span data-stu-id="64182-109">If the user accepts the root certificate, the rest of the certificates (except for the requester's certificate) are placed in the "CA" store.</span></span> <span data-ttu-id="64182-110">Сертификат инициатора запроса помещается в хранилище сертификатов, указанное инициатором запроса, в свойстве [**мисторенаме**](/windows/win32/api/xenroll/nf-xenroll-icenroll-get_mystorename) .</span><span class="sxs-lookup"><span data-stu-id="64182-110">The requester's certificate is placed in the certificate store specified by the requester in the [**MyStoreName**](/windows/win32/api/xenroll/nf-xenroll-icenroll-get_mystorename) property.</span></span>

<span data-ttu-id="64182-111">В следующем примере показано, как использовать Visual Basic Scripting Edition (VBScript) и HTML на веб-странице для получения и хранения возвращенных сертификатов.</span><span class="sxs-lookup"><span data-stu-id="64182-111">The following example shows how to use the Visual Basic Scripting Edition (VBScript) and HTML in a webpage to receive and store the returned certificates.</span></span>


```VB
<HTML>
<TITLE>Certificate Enrollment Acceptance HTML Page
</TITLE>

<OBJECT  classid="clsid:127698E4-E730-4E5C-A2b1-21490A70C8A1"
    CODEBASE="xenroll.dll"
    id=IControl >
</OBJECT>

<SCRIPT language="VBScript">

<!--

Option Explicit 

'Accept the certificate subroutine.

Sub AcceptCertSub

On Error Resume Next

' Get the issued certificate.
' The following value, "PKCS7", represents the received message. 
' Actually, this value must be supplied through the design of
' the receiving application.
' A possible implementation is as follows: after using 
' ICertRequest.Submit to submit the PKCS #10, call 
' ICertRequest.GetLastStatus to confirm successful certificate 
' creation, and then call ICertRequest.GetCertificate to retrieve 
' the certificate.

document.result.result.value = "PKCS7"

    Call IControl.AcceptPKCS7(document.result.result.value)

    If err.Number = 0 Then
        navigate "..\done.htm"
    Else
        Alert "Error: " & Hex(err)
    End If

    End sub

    ' Decline the certificate sub-routine.
    Sub NoAcceptCertSub
    navigate "..\notdone.htm"
    End sub
-->
</SCRIPT>
</BODY>
</HTML>
```



 

 
