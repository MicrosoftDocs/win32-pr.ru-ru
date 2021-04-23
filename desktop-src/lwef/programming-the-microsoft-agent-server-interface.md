---
title: Программирование интерфейса сервера Microsoft Agent
description: Программирование интерфейса сервера Microsoft Agent
ms.assetid: d1f9feb1-afcf-45a5-8ebf-7200c5963f70
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d9699a102884eeab5079e25aaa39fb6942c5f4ef
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/16/2019
ms.locfileid: "104067229"
---
# <a name="programming-the-microsoft-agent-server-interface"></a><span data-ttu-id="d43b9-103">Программирование интерфейса сервера Microsoft Agent</span><span class="sxs-lookup"><span data-stu-id="d43b9-103">Programming the Microsoft Agent Server Interface</span></span>

<span data-ttu-id="d43b9-104">\[Microsoft Agent является устаревшим в Windows 7 и может быть недоступен в последующих версиях Windows.\]</span><span class="sxs-lookup"><span data-stu-id="d43b9-104">\[Microsoft Agent is deprecated as of Windows 7, and may be unavailable in subsequent versions of Windows.\]</span></span>

<span data-ttu-id="d43b9-105">Microsoft Agent предоставляет службы, позволяющие программировать анимированные символы из приложения.</span><span class="sxs-lookup"><span data-stu-id="d43b9-105">Microsoft Agent provides services that enable you to program animated characters from an application.</span></span> <span data-ttu-id="d43b9-106">Эти службы реализуются как сервер OLE Automation.</span><span class="sxs-lookup"><span data-stu-id="d43b9-106">These services are implemented as an OLE Automation server.</span></span> <span data-ttu-id="d43b9-107">OLE Automation позволяет приложению управлять объектом другого приложения программным способом.</span><span class="sxs-lookup"><span data-stu-id="d43b9-107">OLE Automation enables an application to control another application's object programmatically.</span></span> <span data-ttu-id="d43b9-108">В этом документе предполагается понимание модели COM и OLE.</span><span class="sxs-lookup"><span data-stu-id="d43b9-108">This document assumes an understanding of the Component Object Model (COM) and OLE.</span></span> <span data-ttu-id="d43b9-109">Дополнительные сведения об этих службах см. в разделе [Общие сведения о интерфейсе программирования](microsoft-agent-programming-interface-overview.md).</span><span class="sxs-lookup"><span data-stu-id="d43b9-109">For an introduction of these services, see the [Programming Interface Overview](microsoft-agent-programming-interface-overview.md).</span></span>

-   [<span data-ttu-id="d43b9-110">Добавление функциональных возможностей агента Microsoft Agent в приложение</span><span class="sxs-lookup"><span data-stu-id="d43b9-110">Adding Microsoft Agent Functionality to Your Application</span></span>](adding-microsoft-agent-functionality-to-your-application.md)
-   [<span data-ttu-id="d43b9-111">Загрузка данных символов и анимации</span><span class="sxs-lookup"><span data-stu-id="d43b9-111">Loading Character and Animation Data</span></span>](loading-character-and-animation-data.md)
-   [<span data-ttu-id="d43b9-112">Создание приемника уведомлений</span><span class="sxs-lookup"><span data-stu-id="d43b9-112">Creating a Notification Sink</span></span>](creating-a-notification-sink.md)
-   [<span data-ttu-id="d43b9-113">Доступ к службам с помощью Java</span><span class="sxs-lookup"><span data-stu-id="d43b9-113">Accessing Services Using Java</span></span>](accessing-services-using-java.md)
-   [<span data-ttu-id="d43b9-114">Доступ к голосовым службам</span><span class="sxs-lookup"><span data-stu-id="d43b9-114">Accessing Speech Services</span></span>](accessing-speech-services.md)
-   [<span data-ttu-id="d43b9-115">Ссылки</span><span class="sxs-lookup"><span data-stu-id="d43b9-115">Reference</span></span>](reference.md)

 

 




