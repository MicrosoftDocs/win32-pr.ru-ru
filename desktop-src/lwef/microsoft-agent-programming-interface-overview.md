---
title: Обзор интерфейса программирования Microsoft Agent
description: Обзор интерфейса программирования Microsoft Agent
ms.assetid: 8709441b-9739-4f11-a2de-40a5f5eefb72
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ad89249e064eb89d37f497fb79cb8982c79cb83c
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/16/2019
ms.locfileid: "103888451"
---
# <a name="microsoft-agent-programming-interface-overview"></a><span data-ttu-id="72e37-103">Обзор интерфейса программирования Microsoft Agent</span><span class="sxs-lookup"><span data-stu-id="72e37-103">Microsoft Agent Programming Interface Overview</span></span>

<span data-ttu-id="72e37-104">\[Microsoft Agent является устаревшим в Windows 7 и может быть недоступен в последующих версиях Windows.\]</span><span class="sxs-lookup"><span data-stu-id="72e37-104">\[Microsoft Agent is deprecated as of Windows 7, and may be unavailable in subsequent versions of Windows.\]</span></span>

<span data-ttu-id="72e37-105">API Microsoft Agent предоставляет службы, поддерживающие отображение и анимацию анимированных символов.</span><span class="sxs-lookup"><span data-stu-id="72e37-105">The Microsoft Agent API provides services that support the display and animation of animated characters.</span></span> <span data-ttu-id="72e37-106">Microsoft Agent, реализованный как сервер автоматизации OLE (модель \[ COM \] ), позволяет использовать несколько приложений, называемых клиентами или клиентскими приложениями, для размещения и доступа к своим анимациям, входным и выходным службам одновременно.</span><span class="sxs-lookup"><span data-stu-id="72e37-106">Implemented as an OLE Automation (Component Object Model \[COM\]) server, Microsoft Agent enables multiple applications, called clients or client applications, to host and access its animation, input, and output services at the same time.</span></span> <span data-ttu-id="72e37-107">Клиент может быть любым приложением, которое подключается к COM-интерфейсам Microsoft Agent.</span><span class="sxs-lookup"><span data-stu-id="72e37-107">A client can be any application that connects to the Microsoft Agent's COM interfaces.</span></span>

<span data-ttu-id="72e37-108">Как сервер COM, Microsoft Agent автоматически запускается, только если клиентское приложение использует интерфейсы COM и запросы для подключения к нему.</span><span class="sxs-lookup"><span data-stu-id="72e37-108">As a COM server, Microsoft Agent automatically starts up only when a client application uses the COM interfaces and requests to connect to it.</span></span> <span data-ttu-id="72e37-109">Она остается работающей, пока все клиенты не закрывают свои подключения.</span><span class="sxs-lookup"><span data-stu-id="72e37-109">It remains running until all clients close their connections.</span></span> <span data-ttu-id="72e37-110">Если подключенных клиентов не осталось, Microsoft Agent автоматически завершает работу.</span><span class="sxs-lookup"><span data-stu-id="72e37-110">When no connected clients remain, Microsoft Agent automatically exits.</span></span>

<span data-ttu-id="72e37-111">Хотя COM-интерфейсы Microsoft Agent можно вызывать напрямую, Microsoft Agent также включает элемент управления Microsoft ActiveX.</span><span class="sxs-lookup"><span data-stu-id="72e37-111">Although you can call Microsoft Agent's COM interfaces directly, Microsoft Agent also includes a Microsoft ActiveX control.</span></span> <span data-ttu-id="72e37-112">Этот элемент управления упрощает доступ к службам Microsoft Agent с языков программирования, поддерживающих интерфейс элементов управления ActiveX.</span><span class="sxs-lookup"><span data-stu-id="72e37-112">This control makes it easy to access Microsoft Agent's services from programming languages that support the ActiveX control interface.</span></span>

<span data-ttu-id="72e37-113">В дополнение к поддержке автономных программ, написанных для Windows, агент может быть включен в скрипт для поддержки веб-страниц при условии, что браузер поддерживает интерфейс ActiveX.</span><span class="sxs-lookup"><span data-stu-id="72e37-113">In addition to supporting stand-alone programs written for Windows, Agent can be scripted to support webpages, provided that the browser supports the ActiveX interface.</span></span> <span data-ttu-id="72e37-114">Microsoft Internet Explorer включает поддержку ActiveX, а также языки сценариев, которые можно использовать для программирования агента.</span><span class="sxs-lookup"><span data-stu-id="72e37-114">Microsoft Internet Explorer includes support for ActiveX as well as scripting languages that you can use to program Agent.</span></span> <span data-ttu-id="72e37-115">Если вы не используете Internet Explorer, обратитесь к поставщику или поставщику по поводу поддержки ActiveX в браузере.</span><span class="sxs-lookup"><span data-stu-id="72e37-115">If you are not using Internet Explorer, consult with your vendor or supplier about the browser's support for ActiveX.</span></span>

<span data-ttu-id="72e37-116">Ниже приведены краткие сведения об интерфейсах программирования для программного обеспечения агента Майкрософт.</span><span class="sxs-lookup"><span data-stu-id="72e37-116">The following information provides a brief overview of the programming interfaces for the Microsoft Agent software.</span></span>

-   [<span data-ttu-id="72e37-117">Службы анимации</span><span class="sxs-lookup"><span data-stu-id="72e37-117">Animation Services</span></span>](animation-services.md)
-   [<span data-ttu-id="72e37-118">Входные службы</span><span class="sxs-lookup"><span data-stu-id="72e37-118">Input Services</span></span>](input-services.md)
-   [<span data-ttu-id="72e37-119">Окно "Voice Commands"</span><span class="sxs-lookup"><span data-stu-id="72e37-119">The Voice Commands Window</span></span>](the-voice-commands-window.md)
-   [<span data-ttu-id="72e37-120">Службы вывода</span><span class="sxs-lookup"><span data-stu-id="72e37-120">Output Services</span></span>](output-services.md)

 

 




