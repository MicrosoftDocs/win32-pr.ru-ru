---
title: Определение того, поддерживает ли удаленный компьютер протокол WS-Management
description: Можно использовать сеанс. Identify или IWSManSession. Определите методы, чтобы определить, имеет ли удаленный компьютер службу, поддерживающую протокол WS-Management.
ms.assetid: 4d11ac02-fa8b-45d7-bceb-a18f561bc928
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: af82284b38b2a101c767766d44eb975ff7e1dadc
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/16/2019
ms.locfileid: "105700565"
---
# <a name="detecting-whether-a-remote-computer-supports-ws-management-protocol"></a><span data-ttu-id="83704-103">Определение того, поддерживает ли удаленный компьютер протокол WS-Management</span><span class="sxs-lookup"><span data-stu-id="83704-103">Detecting Whether a Remote Computer Supports WS-Management Protocol</span></span>

<span data-ttu-id="83704-104">Можно использовать [**сеанс. Identify**](session-identify.md) или [**IWSManSession. Определите**](/windows/desktop/api/WSManDisp/nf-wsmandisp-iwsmansession-identify) методы, чтобы определить, имеет ли удаленный компьютер службу, поддерживающую протокол WS-Management.</span><span class="sxs-lookup"><span data-stu-id="83704-104">You can use the [**Session.Identify**](session-identify.md) or [**IWSManSession.Identify**](/windows/desktop/api/WSManDisp/nf-wsmandisp-iwsmansession-identify) methods to determine if the remote computer has a service that supports the WS-Management protocol.</span></span>

<span data-ttu-id="83704-105">Если служба протокола WS-Management настроена на удаленном компьютере и ожидает передачи запросов, служба может обнаружить запрос на выявление в заголовке с помощью следующего XML-кода.</span><span class="sxs-lookup"><span data-stu-id="83704-105">If a WS-Management protocol service is configured on the remote computer and is listening for requests, the service can detect an Identify request by the following XML in the header.</span></span>


```XML
xmlns:wsmid="https://schemas.dmtf.org/wbem/wsman/identity/1/wsmanidentity"
```



<span data-ttu-id="83704-106">Служба протокола WS-Management, которая получает запрос, возвращает сведения, содержащиеся в следующем списке, в тексте сообщения:</span><span class="sxs-lookup"><span data-stu-id="83704-106">The WS-Management protocol service that receives the request returns the information, contained in the following list, in the body of the message:</span></span>

-   <span data-ttu-id="83704-107">Версия протокола WS-Management.</span><span class="sxs-lookup"><span data-stu-id="83704-107">The WS-Management protocol version.</span></span> <span data-ttu-id="83704-108">Например, https://schemas.dmtf.org/wbem/wsman/1/wsman.</span><span class="sxs-lookup"><span data-stu-id="83704-108">For example, "https://schemas.dmtf.org/wbem/wsman/1/wsman".</span></span>
-   <span data-ttu-id="83704-109">Поставщик продукта, например «корпорация Майкрософт».</span><span class="sxs-lookup"><span data-stu-id="83704-109">The product vendor, for example, "Microsoft Corporation".</span></span>
-   <span data-ttu-id="83704-110">Версия продукта.</span><span class="sxs-lookup"><span data-stu-id="83704-110">The product version.</span></span> <span data-ttu-id="83704-111">Если запрос отправляется с помощью **всманфлагусеноаусентикатион** в параметре *flags* , сведения о версии продукта не возвращаются.</span><span class="sxs-lookup"><span data-stu-id="83704-111">If the request is sent with **WSManFlagUseNoAuthentication** in the *flags* parameter, then no product version information is returned.</span></span> <span data-ttu-id="83704-112">Если запрос отправляется либо с проверкой подлинности по умолчанию, либо с помощью указанного другого режима проверки подлинности, то могут возвращаться сведения о версии продукта.</span><span class="sxs-lookup"><span data-stu-id="83704-112">If the request is sent with either the default authentication in effect or with another authentication mode specified, then the product version information can be returned.</span></span>

<span data-ttu-id="83704-113">Запрос на обнаружение того, имеется ли на удаленном компьютере настроенная и слушающая WS-Management Служба протокола может быть выполнена в начале скрипта с другими операциями.</span><span class="sxs-lookup"><span data-stu-id="83704-113">The request to detect whether the remote computer has a configured and listening WS-Management protocol service can be performed at the beginning of a script with other operations.</span></span> <span data-ttu-id="83704-114">Это позволит проверить, что конечный компьютер или компьютеры могут отвечать на дальнейшие запросы WS-Management протоколов.</span><span class="sxs-lookup"><span data-stu-id="83704-114">This will verify that the target computer or computers can respond to further WS-Management protocol requests.</span></span> <span data-ttu-id="83704-115">Проверку также можно выполнить в отдельном сценарии.</span><span class="sxs-lookup"><span data-stu-id="83704-115">The verification also can be done in a separate script.</span></span>

<span data-ttu-id="83704-116">**Обнаружение службы протокола WS-Management**</span><span class="sxs-lookup"><span data-stu-id="83704-116">**To detect a WS-Management protocol service**</span></span>

1.  <span data-ttu-id="83704-117">Создайте объект [**WSMan**](wsman.md) .</span><span class="sxs-lookup"><span data-stu-id="83704-117">Create a [**WSMan**](wsman.md) object.</span></span>

    ```VB
    Set objWsman = CreateObject("Wsman.Automation")
    ```

    

2.  <span data-ttu-id="83704-118">Определите, должен ли запрос отправляться с проверкой подлинности или без проверки подлинности и соответствующим образом установите параметр *flags* в вызове [**WSMan. CreateSession**](wsman-createsession.md).</span><span class="sxs-lookup"><span data-stu-id="83704-118">Determine whether the request should be sent authenticated or unauthenticated and set the *flags* parameter accordingly in the call to [**WSMan.CreateSession**](wsman-createsession.md).</span></span>

    ```VB
    set objSession = objWsman.CreateSession("Remote1", _
       objWsman.SessionFlagUseNoAuthentication)
    ```

    

3.  <span data-ttu-id="83704-119">Вызовите [**сеанс. Identify**](session-identify.md).</span><span class="sxs-lookup"><span data-stu-id="83704-119">Call [**Session.Identify**](session-identify.md).</span></span>

    ```VB
    objSession.Identify
    ```

    

## <a name="examples"></a><span data-ttu-id="83704-120">Примеры</span><span class="sxs-lookup"><span data-stu-id="83704-120">Examples</span></span>

<span data-ttu-id="83704-121">Следующий пример кода VBScript отправляет на удаленный компьютер с именем "Remote1" запрос на выявление без проверки подлинности в том же домене.</span><span class="sxs-lookup"><span data-stu-id="83704-121">The following VBScript code example sends an unauthenticated Identify request to the remote computer named "Remote1" in the same domain.</span></span>


```VB
set objWsman = CreateObject("Wsman.Automation")
set objSession = objWsman.CreateSession("Remote1", _
  objWsman.SessionFlagUseNoAuthentication)
WScript.Echo objSession.Identify
```



<span data-ttu-id="83704-122">Следующий ответ показывает код XML, возвращаемый удаленным компьютером.</span><span class="sxs-lookup"><span data-stu-id="83704-122">The following response shows the XML returned by the remote computer.</span></span> <span data-ttu-id="83704-123">Версия протокола WS-Management (" https://schemas.dmtf.org/wbem/wsman/1/wsman.xsd ") и поставщик операционной системы ("Корпорация Майкрософт") указаны в возвращенном XML.</span><span class="sxs-lookup"><span data-stu-id="83704-123">The WS-Management protocol version ("https://schemas.dmtf.org/wbem/wsman/1/wsman.xsd") and the operating system vendor ("Microsoft Corporation") are specified in the returned XML.</span></span> <span data-ttu-id="83704-124">Так как сообщение отправляется без проверки подлинности, версия продукта не возвращается службой служба удаленного управления Windows.</span><span class="sxs-lookup"><span data-stu-id="83704-124">Because the message is sent unauthenticated, the product version is not returned by the Windows Remote Management service.</span></span>


```XML
<wsmid:IdentifyResponse xmlns:wsmid=
    "https://schemas.dmtf.org/wbem/wsman/identity/1/wsmanidentity.xsd">
<wsmid:ProtocolVersion>https://schemas.dmtf.org/wbem/wsman/1/wsman.xsd
    </wsmid:ProtocolVersion>
<wsmid:ProductVendor>Microsoft Corporation</wsmid:ProductVendor>
<wsmid:ProductVersion>OS: 0.0.0 SP: 0.0 Stack:1.0</wsmid:ProductVersion>
</wsmid:IdentifyResponse>
```



<span data-ttu-id="83704-125">Следующий пример кода VBScript отправляет на удаленный компьютер запрос на выявление проверки подлинности.</span><span class="sxs-lookup"><span data-stu-id="83704-125">The following VBScript code example sends an authenticated Identify request to the remote computer.</span></span>


```VB
set ObjWSMan = CreateObject("Wsman.Automation")
set objSession = WSMan.CreateSession("Remote1", _
  objWSMan.SessionFlagUseKerberos)
WScript.Echo objSession.Identify
```



<span data-ttu-id="83704-126">Поскольку запрос был отправлен с проверкой подлинности, возвращаются сведения о версии.</span><span class="sxs-lookup"><span data-stu-id="83704-126">Because the request was sent with authentication, the version information is returned.</span></span>


```XML
<wsmid:IdentifyResponse xmlns:wsmid=
    "https://schemas.dmtf.org/wbem/wsman/identity/1/wsmanidentity.xsd">
<wsmid:ProtocolVersion>https://schemas.dmtf.org/wbem/wsman/1/wsman.xsd
    </wsmid:ProtocolVersion>
<wsmid:ProductVendor>Microsoft Corporation</wsmid:ProductVendor>
<wsmid:ProductVersion>OS: 6.0.5384 SP: 0.0 Stack:1.0</wsmid:ProductVersion>
</wsmid:IdentifyResponse>
```



## <a name="related-topics"></a><span data-ttu-id="83704-127">См. также</span><span class="sxs-lookup"><span data-stu-id="83704-127">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="83704-128">О служба удаленного управления Windows</span><span class="sxs-lookup"><span data-stu-id="83704-128">About Windows Remote Management</span></span>](about-windows-remote-management.md)
</dt> <dt>

[<span data-ttu-id="83704-129">Использование служба удаленного управления Windows</span><span class="sxs-lookup"><span data-stu-id="83704-129">Using Windows Remote Management</span></span>](using-windows-remote-management.md)
</dt> <dt>

[<span data-ttu-id="83704-130">Справочник по служба удаленного управления Windows</span><span class="sxs-lookup"><span data-stu-id="83704-130">Windows Remote Management Reference</span></span>](windows-remote-management-reference.md)
</dt> </dl>

 

 




