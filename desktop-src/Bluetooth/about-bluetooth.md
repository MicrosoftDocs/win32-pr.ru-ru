---
title: Об Bluetooth
description: Bluetooth — это стандартный промышленный протокол, обеспечивающий беспроводное подключение для множества устройств, включая компьютеры, принтеры, мобильные телефоны и карманные устройства.
ms.assetid: 424168a1-e55c-4947-9a80-8594b4d83bbd
keywords:
- Bluetooth, описание
- Bluetooth Bluetooth, сведения
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4b704bb3245adcd75948f7f9fbb411697c7c45f0
ms.sourcegitcommit: 3e70ae762629e244028b437420ed50b5850db4e3
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 02/20/2020
ms.locfileid: "104069615"
---
# <a name="about-bluetooth"></a><span data-ttu-id="e916f-105">Об Bluetooth</span><span class="sxs-lookup"><span data-stu-id="e916f-105">About Bluetooth</span></span>

<span data-ttu-id="e916f-106">Bluetooth — это стандартный промышленный протокол, обеспечивающий беспроводное подключение для множества устройств, включая компьютеры, принтеры, мобильные телефоны и карманные устройства.</span><span class="sxs-lookup"><span data-stu-id="e916f-106">Bluetooth is an industry-standard protocol that enables wireless connectivity for a multitude of devices, including computers, printers, mobile phones, and handheld devices.</span></span>

<span data-ttu-id="e916f-107">К основным функциям Bluetooth относятся:</span><span class="sxs-lookup"><span data-stu-id="e916f-107">Key Bluetooth features include:</span></span>

-   <span data-ttu-id="e916f-108">Экономичный и экономичный протокол с низким энергопотреблением, обеспечивающий поддержку стандартных отраслевых стандартов и принятие решений по всему миру.</span><span class="sxs-lookup"><span data-stu-id="e916f-108">A low-cost, low-power consumption wireless protocol with industry-standard support and worldwide acceptance.</span></span>
-   <span data-ttu-id="e916f-109">Определенный и знакомый программный интерфейс, который разработчики могут использовать для быстрой разработки приложений или работы с ними.</span><span class="sxs-lookup"><span data-stu-id="e916f-109">A defined and familiar programming interface that developers can use to quickly develop or port applications.</span></span>
-   <span data-ttu-id="e916f-110">Официальный веб-узел и единая для отрасли организация, которая описывает, способствует и стандартизует технологию Bluetooth.</span><span class="sxs-lookup"><span data-stu-id="e916f-110">An official Web site and an industry-wide cooperative organization that explains, promotes, and standardizes Bluetooth technology.</span></span> <span data-ttu-id="e916f-111">Дополнительные сведения см. в разделе [www.Bluetooth.com](https://www.bluetooth.com/).</span><span class="sxs-lookup"><span data-stu-id="e916f-111">For more information, see [www.bluetooth.com](https://www.bluetooth.com/).</span></span>

<span data-ttu-id="e916f-112">Bluetooth в Windows предоставляет основные службы, аналогичные тем, которые предоставляются протоколом управления передачей (TCP-компонент TCP/IP).</span><span class="sxs-lookup"><span data-stu-id="e916f-112">Bluetooth on Windows provides core services that are similar to those exposed by Transmission Control Protocol (the TCP part of TCP/IP).</span></span> <span data-ttu-id="e916f-113">Как и многие сетевые протоколы и службы, подключение Bluetooth и перенос данных запрограммированы с помощью вызовов функций Windows Sockets, используя общие методики программирования Windows Sockets и определенные модули Bluetooth.</span><span class="sxs-lookup"><span data-stu-id="e916f-113">Like many networking protocols and services, Bluetooth connectivity and data transfer are programmed through Windows Sockets function calls, using common Windows Sockets programming techniques and specific Bluetooth extensions.</span></span> <span data-ttu-id="e916f-114">Однако, так как между проводной, фиксированной и беспроводной сетью существуют значительные различия, Bluetooth предоставляет такие расширения, как обнаружение службы, устройства и уведомление, которые позволяют приложениям правильно работать в беспроводной среде.</span><span class="sxs-lookup"><span data-stu-id="e916f-114">However, because significant differences exist between a wired, fixed network and a wireless ad-hoc network, Bluetooth provides extensions such as service/device discovery and notification that enable applications to operate properly in the wireless environment.</span></span> <span data-ttu-id="e916f-115">Эти расширения также Pave способ простого переноса на аналогичные технологии, такие как IrDA или будущие Беспроводные транспорта.</span><span class="sxs-lookup"><span data-stu-id="e916f-115">These extensions also pave the way for simple porting to similar technologies, such as IrDA, or future wireless transports.</span></span>

<span data-ttu-id="e916f-116">Корпорация Майкрософт обеспечивает поддержку Bluetooth в Windows XP с пакетом обновления 1 (SP1) и более поздних версий, в Windows XP Embedded с пакетом обновления 2 (SP2) и на Windows CE.</span><span class="sxs-lookup"><span data-stu-id="e916f-116">Microsoft provides support for Bluetooth on Windows XP with Service Pack 1 (SP1) and later, on Windows XP Embedded with Service Pack 2, and on Windows CE.</span></span> <span data-ttu-id="e916f-117">Приложения Bluetooth, работающие в Windows XP, должны иметь возможность работать в образе времени выполнения на основе Windows XP Embedded, который включает необходимые зависимости.</span><span class="sxs-lookup"><span data-stu-id="e916f-117">Bluetooth applications that run on Windows XP should be able to run on a Windows XP Embedded-based run-time image that includes the required dependencies.</span></span> <span data-ttu-id="e916f-118">Дополнительные сведения о Windows XP Embedded см. в справочной документации по Windows XP Embedded на сайте MSDN.</span><span class="sxs-lookup"><span data-stu-id="e916f-118">For more information about Windows XP Embedded, see the Windows XP Embedded Help documentation on MSDN.</span></span> <span data-ttu-id="e916f-119">Дополнительные сведения о Windows CE программировании см. в пакете SDK для Windows CE.</span><span class="sxs-lookup"><span data-stu-id="e916f-119">For more information about Windows CE programming, consult the Windows CE SDK.</span></span>

<span data-ttu-id="e916f-120">Корпорация Майкрософт предлагает два подхода к программированию Bluetooth в Windows:</span><span class="sxs-lookup"><span data-stu-id="e916f-120">Microsoft provides two approaches for programming Bluetooth on Windows:</span></span>

-   <span data-ttu-id="e916f-121">Использование интерфейса сокетов Windows</span><span class="sxs-lookup"><span data-stu-id="e916f-121">Using the Windows Sockets interface</span></span>
-   <span data-ttu-id="e916f-122">Управление устройствами напрямую с помощью интерфейсов Bluetooth, не поддерживающих сокеты</span><span class="sxs-lookup"><span data-stu-id="e916f-122">Managing devices directly by using nonsocket Bluetooth interfaces</span></span>

<span data-ttu-id="e916f-123">В этом разделе содержатся общие сведения о обоих подходах в следующих разделах.</span><span class="sxs-lookup"><span data-stu-id="e916f-123">This section provides overview information about both of these approaches in the following topics.</span></span> <span data-ttu-id="e916f-124">Дополнительные сведения об использовании элементов API сокетов Windows для программирования Bluetooth см. в разделе [программирование Bluetooth с помощью сокетов Windows](bluetooth-programming-with-windows-sockets.md).</span><span class="sxs-lookup"><span data-stu-id="e916f-124">For more information about using Windows Sockets API elements to program Bluetooth, see [Bluetooth Programming with Windows Sockets](bluetooth-programming-with-windows-sockets.md).</span></span>



| <span data-ttu-id="e916f-125">Section</span><span class="sxs-lookup"><span data-stu-id="e916f-125">Section</span></span>                                                                                | <span data-ttu-id="e916f-126">Содержимое</span><span class="sxs-lookup"><span data-stu-id="e916f-126">Content</span></span>                                                           |
|----------------------------------------------------------------------------------------|-------------------------------------------------------------------|
| [<span data-ttu-id="e916f-127">Поддержка сокетов Windows для Bluetooth</span><span class="sxs-lookup"><span data-stu-id="e916f-127">Windows Sockets Support for Bluetooth</span></span>](windows-sockets-support-for-bluetooth.md)     | <span data-ttu-id="e916f-128">Описывает связь между сокетами Bluetooth и Windows.</span><span class="sxs-lookup"><span data-stu-id="e916f-128">Describes the relationship between Bluetooth and Windows Sockets.</span></span> |
| [<span data-ttu-id="e916f-129">Управление устройствами и службами Bluetooth</span><span class="sxs-lookup"><span data-stu-id="e916f-129">Managing Bluetooth Devices and Services</span></span>](managing-bluetooth-devices-and-services.md) | <span data-ttu-id="e916f-130">Описание управления устройствами и службами Bluetooth.</span><span class="sxs-lookup"><span data-stu-id="e916f-130">Describes how to manage Bluetooth devices and services.</span></span>           |



 

 

 




