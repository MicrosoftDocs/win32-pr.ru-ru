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
# <a name="receiving-the-returned-certificate"></a>Получение возвращенного сертификата

Когда центр сертификации (ЦС) проверил сведения об удостоверении инициатора запроса и удовлетворен, что он является владельцем закрытого ключа и что данные об этом инициаторе являются точными, ЦС формирует сертификат X. 509, подписывает его, упаковывает в него все необходимые сертификаты (например, собственный сертификат ЦС) в сообщении и отправляет сообщение инициатору запроса. Сообщение может быть \# сообщением PKCS 7 или запросом CMC (шаблоны v2 выводят ответ CMC).

Принимающее приложение передает сообщение в Управление регистрацией сертификата. После этого Управление регистрацией сертификата открывает сообщение и извлекает сертификаты. Пользователю предлагается диалоговое окно с вопросом, будет ли пользователь принимать самозаверяющие сертификаты в корневом хранилище. Если пользователь принимает корневой сертификат, остальные сертификаты (за исключением сертификата инициатора запроса) помещаются в хранилище CA. Сертификат инициатора запроса помещается в хранилище сертификатов, указанное инициатором запроса, в свойстве [**мисторенаме**](/windows/win32/api/xenroll/nf-xenroll-icenroll-get_mystorename) .

В следующем примере показано, как использовать Visual Basic Scripting Edition (VBScript) и HTML на веб-странице для получения и хранения возвращенных сертификатов.


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



 

 
