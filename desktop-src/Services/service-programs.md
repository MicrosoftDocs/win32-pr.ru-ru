---
description: Программа службы содержит исполняемый код для одной или нескольких служб.
ms.assetid: 697db543-6149-46ac-add3-c8c6ca3aadbe
title: Служебные программы
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7b5e78574f46549956325bc19ffb6d51f4a114ff
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "103912804"
---
# <a name="service-programs"></a><span data-ttu-id="72c05-103">Служебные программы</span><span class="sxs-lookup"><span data-stu-id="72c05-103">Service Programs</span></span>

<span data-ttu-id="72c05-104">*Программа службы* содержит исполняемый код для одной или нескольких служб.</span><span class="sxs-lookup"><span data-stu-id="72c05-104">A *service program* contains executable code for one or more services.</span></span> <span data-ttu-id="72c05-105">Программа службы, созданная с помощью собственного процесса Win32 типа "служба типов \_ \_ \_ ", содержит код только для одной службы.</span><span class="sxs-lookup"><span data-stu-id="72c05-105">A service program created with the type SERVICE\_WIN32\_OWN\_PROCESS contains the code for only one service.</span></span> <span data-ttu-id="72c05-106">Служебная программа, созданная с помощью \_ \_ общего процесса Win32 для службы типов \_ , содержит код для более чем одной службы, что позволяет им совместно использовать код.</span><span class="sxs-lookup"><span data-stu-id="72c05-106">A service program created with the type SERVICE\_WIN32\_SHARE\_PROCESS contains code for more than one service, enabling them to share code.</span></span> <span data-ttu-id="72c05-107">Примером служебной программы, выполняющей эту процедуру, является основной процесс службы, Svchost.exe, в котором размещаются внутренние службы Windows.</span><span class="sxs-lookup"><span data-stu-id="72c05-107">An example of a service program that does this is the generic service host process, Svchost.exe, which hosts internal Windows services.</span></span> <span data-ttu-id="72c05-108">Обратите внимание, что Svchost.exe зарезервировано для использования операционной системой и не должна использоваться службами, отличными от Windows.</span><span class="sxs-lookup"><span data-stu-id="72c05-108">Note that Svchost.exe is reserved for use by the operating system and should not be used by non-Windows services.</span></span> <span data-ttu-id="72c05-109">Вместо этого разработчики должны реализовать собственные программы размещения служб.</span><span class="sxs-lookup"><span data-stu-id="72c05-109">Instead, developers should implement their own service hosting programs.</span></span>

<span data-ttu-id="72c05-110">Служебную программу можно настроить для выполнения в контексте учетной записи пользователя из встроенного (локального), первичного или доверенного домена.</span><span class="sxs-lookup"><span data-stu-id="72c05-110">A service program can be configured to execute in the context of a user account from either the built-in (local), primary, or trusted domain.</span></span> <span data-ttu-id="72c05-111">Его также можно настроить для запуска в особой [учетной записи пользователя службы](service-user-accounts.md).</span><span class="sxs-lookup"><span data-stu-id="72c05-111">It can also be configured to run in a special [service user account](service-user-accounts.md).</span></span>

<span data-ttu-id="72c05-112">В следующих разделах описываются требования к интерфейсу [диспетчера управления службами](service-control-manager.md) (SCM), которые должна включать программа службы.</span><span class="sxs-lookup"><span data-stu-id="72c05-112">The following topics describe the interface requirements of the [service control manager](service-control-manager.md) (SCM) that a service program must include:</span></span>

-   [<span data-ttu-id="72c05-113">Точка входа службы</span><span class="sxs-lookup"><span data-stu-id="72c05-113">Service Entry Point</span></span>](service-entry-point.md)
-   [<span data-ttu-id="72c05-114">Функция ServiceMain службы</span><span class="sxs-lookup"><span data-stu-id="72c05-114">Service ServiceMain Function</span></span>](service-servicemain-function.md)
-   [<span data-ttu-id="72c05-115">Функция обработчика управления службой</span><span class="sxs-lookup"><span data-stu-id="72c05-115">Service Control Handler Function</span></span>](service-control-handler-function.md)

<span data-ttu-id="72c05-116">Эти разделы не применяются к службам драйверов.</span><span class="sxs-lookup"><span data-stu-id="72c05-116">These topics do not apply to driver services.</span></span> <span data-ttu-id="72c05-117">Требования к интерфейсу служб драйверов см. в разделе Windows Driver Kit (WDK).</span><span class="sxs-lookup"><span data-stu-id="72c05-117">For interface requirements of driver services, see the Windows Driver Kit (WDK).</span></span>

<span data-ttu-id="72c05-118">Служба работает как фоновый процесс, который может повлиять на производительность системы, скорость реагирования, эффективность энергопотребления и безопасность.</span><span class="sxs-lookup"><span data-stu-id="72c05-118">A service runs as a background process that can affect system performance, responsiveness, energy efficiency, and security.</span></span> <span data-ttu-id="72c05-119">Рекомендации по оптимизации служб см. в статье [Разработка эффективных фоновых процессов для Windows](/windows-hardware/drivers/kernel/implementing-power-management).</span><span class="sxs-lookup"><span data-stu-id="72c05-119">For service optimization guidelines, see [Developing Efficient Background Processes for Windows](/windows-hardware/drivers/kernel/implementing-power-management).</span></span> <span data-ttu-id="72c05-120">В следующих разделах описываются дополнительные вопросы программирования:</span><span class="sxs-lookup"><span data-stu-id="72c05-120">The following topics describe additional programming considerations:</span></span>

-   [<span data-ttu-id="72c05-121">Переходы состояния службы</span><span class="sxs-lookup"><span data-stu-id="72c05-121">Service State Transitions</span></span>](service-status-transitions.md)
-   [<span data-ttu-id="72c05-122">Получение событий в службе</span><span class="sxs-lookup"><span data-stu-id="72c05-122">Receiving Events in a Service</span></span>](receiving-events-in-a-service.md)
-   [<span data-ttu-id="72c05-123">Многопоточные службы</span><span class="sxs-lookup"><span data-stu-id="72c05-123">Multithreaded Services</span></span>](multithreaded-services.md)
-   [<span data-ttu-id="72c05-124">Службы и реестр</span><span class="sxs-lookup"><span data-stu-id="72c05-124">Services and the Registry</span></span>](services-and-the-registry.md)
-   [<span data-ttu-id="72c05-125">Службы и перенаправленные диски</span><span class="sxs-lookup"><span data-stu-id="72c05-125">Services and Redirected Drives</span></span>](services-and-redirected-drives.md)
-   [<span data-ttu-id="72c05-126">События триггера службы</span><span class="sxs-lookup"><span data-stu-id="72c05-126">Service Trigger Events</span></span>](service-trigger-events.md)

<span data-ttu-id="72c05-127">Обратите внимание, что если служебная программа функционирует как RPC Server, она должна использовать динамические конечные точки и взаимную проверку подлинности.</span><span class="sxs-lookup"><span data-stu-id="72c05-127">Note that if the service program functions as an RPC server, it should use dynamic endpoints and mutual authentication.</span></span>

 

 
