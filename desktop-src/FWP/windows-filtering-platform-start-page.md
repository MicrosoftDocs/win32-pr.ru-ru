---
title: Платформа фильтрации Windows
description: Платформа фильтрации Windows (WFP) — это набор API-интерфейсов и системных служб, которые предоставляют платформу для создания приложений фильтрации по сети.
ms.assetid: 0436f559-20e6-4199-8391-10eb7d85df23
keywords:
- Платформа фильтрации Windows
- Начальная страница платформы фильтрации Windows, начальная страница
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5cf63f995b44be607977dd0c70c6c91eed024e81
ms.sourcegitcommit: 773fa6257ead6c74154ad3cf46d21e49adc900aa
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/09/2020
ms.locfileid: "105661787"
---
# <a name="windows-filtering-platform"></a><span data-ttu-id="09b3f-105">Платформа фильтрации Windows</span><span class="sxs-lookup"><span data-stu-id="09b3f-105">Windows Filtering Platform</span></span>

## <a name="purpose"></a><span data-ttu-id="09b3f-106">Назначение</span><span class="sxs-lookup"><span data-stu-id="09b3f-106">Purpose</span></span>

<span data-ttu-id="09b3f-107">Платформа фильтрации Windows (WFP) — это набор API-интерфейсов и системных служб, которые предоставляют платформу для создания приложений фильтрации по сети.</span><span class="sxs-lookup"><span data-stu-id="09b3f-107">Windows Filtering Platform (WFP) is a set of API and system services that provide a platform for creating network filtering applications.</span></span> <span data-ttu-id="09b3f-108">API WFP позволяет разработчикам писать код, взаимодействующий с пакетной обработкой, которая выполняется на нескольких уровнях в сетевом стеке операционной системы.</span><span class="sxs-lookup"><span data-stu-id="09b3f-108">The WFP API allows developers to write code that interacts with the packet processing that takes place at several layers in the networking stack of the operating system.</span></span> <span data-ttu-id="09b3f-109">Сетевые данные можно фильтровать, а также изменять до достижения места назначения.</span><span class="sxs-lookup"><span data-stu-id="09b3f-109">Network data can be filtered and also modified before it reaches its destination.</span></span>

<span data-ttu-id="09b3f-110">Предоставляя более простую платформу разработки, WFP предназначена для замены предыдущих технологий фильтрации пакетов, таких как фильтры TDI (TDI), фильтров интерфейсов сетевого драйвера (NDIS) и Winsock Layer Service Provider (LSP).</span><span class="sxs-lookup"><span data-stu-id="09b3f-110">By providing a simpler development platform, WFP is designed to replace previous packet filtering technologies such as Transport Driver Interface (TDI) filters, Network Driver Interface Specification (NDIS) filters, and Winsock Layered Service Providers (LSP).</span></span> <span data-ttu-id="09b3f-111">Начиная с Windows Server 2008 и Windows Vista, обработчик брандмауэра и драйверы обработчика фильтров недоступны. приложения, использующие эти драйверы, должны использовать WFP.</span><span class="sxs-lookup"><span data-stu-id="09b3f-111">Starting in Windows Server 2008 and Windows Vista, the firewall hook and the filter hook drivers are not available; applications that were using these drivers should use WFP instead.</span></span>

<span data-ttu-id="09b3f-112">С помощью API платформы WFP разработчики могут реализовывать брандмауэры, системы обнаружения вторжений, антивирусные программы, средства мониторинга сети и родительские элементы управления.</span><span class="sxs-lookup"><span data-stu-id="09b3f-112">With the WFP API, developers can implement firewalls, intrusion detection systems, antivirus programs, network monitoring tools, and parental controls.</span></span> <span data-ttu-id="09b3f-113">WFP интегрируется с и обеспечивает поддержку функций брандмауэра, таких как проверка подлинности связи и динамическая настройка брандмауэра, на основе использования приложениями API сокетов (политика на основе приложений).</span><span class="sxs-lookup"><span data-stu-id="09b3f-113">WFP integrates with and provides support for firewall features such as authenticated communication and dynamic firewall configuration based on applications' use of sockets API (application-based policy).</span></span> <span data-ttu-id="09b3f-114">WFP также предоставляет инфраструктуру для управления политиками IPsec, уведомлений об изменениях, диагностики сети и фильтрации с отслеживанием состояния.</span><span class="sxs-lookup"><span data-stu-id="09b3f-114">WFP also provides infrastructure for IPsec policy management, change notifications, network diagnostics, and stateful filtering.</span></span>

<span data-ttu-id="09b3f-115">Платформа фильтрации Windows — это платформа разработки, а не брандмауэр.</span><span class="sxs-lookup"><span data-stu-id="09b3f-115">Windows Filtering Platform is a development platform and not a firewall itself.</span></span> <span data-ttu-id="09b3f-116">Приложение брандмауэра, встроенное в Windows Vista, Windows Server 2008 и более поздние операционные системы брандмауэр Windows с повышенной безопасностью (WFAS), реализуется с помощью WFP.</span><span class="sxs-lookup"><span data-stu-id="09b3f-116">The firewall application that is built into Windows Vista, Windows Server 2008, and later operating systems   Windows Firewall with Advanced Security (WFAS)   is implemented using WFP.</span></span> <span data-ttu-id="09b3f-117">Поэтому приложения, разработанные с помощью API WFP или [API WFAS](/previous-versions/windows/desktop/ics/windows-firewall-with-advanced-security-reference) , используют общую логику арбитража фильтрации, встроенную в WFP.</span><span class="sxs-lookup"><span data-stu-id="09b3f-117">Therefore, applications developed with the WFP API or the [WFAS API](/previous-versions/windows/desktop/ics/windows-firewall-with-advanced-security-reference) use the common filtering arbitration logic that is built into WFP.</span></span>

<span data-ttu-id="09b3f-118">API WFP состоит из API пользовательского режима и API режима ядра.</span><span class="sxs-lookup"><span data-stu-id="09b3f-118">The WFP API consists of a user-mode API and a kernel-mode API.</span></span> <span data-ttu-id="09b3f-119">В этом разделе приводится обзор всей платформы WFP и подробно описывается только часть интерфейса API WFP в пользовательском режиме.</span><span class="sxs-lookup"><span data-stu-id="09b3f-119">This section provides an overview of the entire WFP and describes in detail only the user-mode portion of the WFP API.</span></span> <span data-ttu-id="09b3f-120">Подробное описание API WFP в режиме ядра см. в интерактивной справке по [комплекту драйверов для Windows](/windows-hardware/drivers/network/windows-filtering-platform-callout-drivers2) .</span><span class="sxs-lookup"><span data-stu-id="09b3f-120">For a detailed description of the kernel-mode WFP API, see the [Windows Driver Kit](/windows-hardware/drivers/network/windows-filtering-platform-callout-drivers2) online help.</span></span>

## <a name="developer-audience"></a><span data-ttu-id="09b3f-121">Аудитория разработчиков</span><span class="sxs-lookup"><span data-stu-id="09b3f-121">Developer audience</span></span>

<span data-ttu-id="09b3f-122">API платформы фильтрации Windows предназначен для использования программистами, использующими программное обеспечение для разработки на C/C++.</span><span class="sxs-lookup"><span data-stu-id="09b3f-122">The Windows Filtering Platform API is designed for use by programmers using C/C++ development software.</span></span> <span data-ttu-id="09b3f-123">Программисты должны быть знакомы с основными понятиями и структурой работы с сетью, использующими компоненты пользовательского режима и режима ядра.</span><span class="sxs-lookup"><span data-stu-id="09b3f-123">Programmers should be familiar with networking concepts and design of systems using user-mode and kernel-mode components.</span></span>

## <a name="run-time-requirements"></a><span data-ttu-id="09b3f-124">Требования к среде выполнения</span><span class="sxs-lookup"><span data-stu-id="09b3f-124">Run-time requirements</span></span>

<span data-ttu-id="09b3f-125">Платформа фильтрации Windows поддерживается на клиентах под управлением Windows Vista и более поздних версий, а также на серверах под управлением Windows Server 2008 и более поздних версий.</span><span class="sxs-lookup"><span data-stu-id="09b3f-125">The Windows Filtering Platform is supported on clients running Windows Vista and later, and on servers running Windows Server 2008 and later.</span></span> <span data-ttu-id="09b3f-126">Сведения о требованиях среды выполнения для определенного программного элемента см. в разделе требования на странице справки для этого элемента.</span><span class="sxs-lookup"><span data-stu-id="09b3f-126">For information about the run-time requirements for a specific programming element, see the Requirements section of the reference page for that element.</span></span>





 

## <a name="in-this-section"></a><span data-ttu-id="09b3f-127">В этом разделе</span><span class="sxs-lookup"><span data-stu-id="09b3f-127">In this section</span></span>



| <span data-ttu-id="09b3f-128">Раздел</span><span class="sxs-lookup"><span data-stu-id="09b3f-128">Topic</span></span>                                                                                               | <span data-ttu-id="09b3f-129">Описание</span><span class="sxs-lookup"><span data-stu-id="09b3f-129">Description</span></span>                                                                                       |
|-----------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="09b3f-130">Новые возможности платформы фильтрации Windows</span><span class="sxs-lookup"><span data-stu-id="09b3f-130">What's New in Windows Filtering Platform</span></span>](what-s-new-in-windows-filtering-platform.md)<br/> | <span data-ttu-id="09b3f-131">Сведения о новых функциях и интерфейсах API в платформе фильтрации Windows.</span><span class="sxs-lookup"><span data-stu-id="09b3f-131">Information on new features and APIs in Windows Filtering Platform.</span></span><br/>                    |
| [<span data-ttu-id="09b3f-132">О платформе фильтрации Windows</span><span class="sxs-lookup"><span data-stu-id="09b3f-132">About Windows Filtering Platform</span></span>](about-windows-filtering-platform.md)<br/>                 | <span data-ttu-id="09b3f-133">Обзор платформы фильтрации Windows.</span><span class="sxs-lookup"><span data-stu-id="09b3f-133">An overview of Windows Filtering Platform.</span></span><br/>                                             |
| [<span data-ttu-id="09b3f-134">Использование платформы фильтрации Windows</span><span class="sxs-lookup"><span data-stu-id="09b3f-134">Using Windows Filtering Platform</span></span>](using-windows-filtering-platform.md)<br/>                 | <span data-ttu-id="09b3f-135">Пример кода с использованием API платформы фильтрации Windows.</span><span class="sxs-lookup"><span data-stu-id="09b3f-135">Example code using the Windows Filtering Platform API.</span></span> <br/>                                |
| [<span data-ttu-id="09b3f-136">Справочник по API платформы фильтрации Windows</span><span class="sxs-lookup"><span data-stu-id="09b3f-136">Windows Filtering Platform API Reference</span></span>](fwp-reference.md)<br/>                            | <span data-ttu-id="09b3f-137">Документация по функциям, структурам и константам платформы фильтрации Windows.</span><span class="sxs-lookup"><span data-stu-id="09b3f-137">Documentation for the Windows Filtering Platform functions, structures, and constants.</span></span><br/> |



 

## <a name="additional-resources"></a><span data-ttu-id="09b3f-138">Дополнительные ресурсы</span><span class="sxs-lookup"><span data-stu-id="09b3f-138">Additional resources</span></span>

<span data-ttu-id="09b3f-139">Чтобы задать вопросы и обсудить использование API WFP, посетите [форум по платформе фильтрации Windows](https://social.msdn.microsoft.com/forums/wfp/threads/).</span><span class="sxs-lookup"><span data-stu-id="09b3f-139">To ask questions and have discussions about using the WFP API, visit the [Windows Filtering Platform Forum](https://social.msdn.microsoft.com/forums/wfp/threads/).</span></span>

## <a name="related-topics"></a><span data-ttu-id="09b3f-140">См. также</span><span class="sxs-lookup"><span data-stu-id="09b3f-140">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="09b3f-141">API платформы фильтрации Windows в режиме ядра — руководство по проектированию</span><span class="sxs-lookup"><span data-stu-id="09b3f-141">Kernel-Mode Windows Filtering Platform API - Design Guide</span></span>](/windows-hardware/drivers/network/windows-filtering-platform-callout-drivers2)
</dt> <dt>

[<span data-ttu-id="09b3f-142">Справочник по API платформы фильтрации Windows в режиме ядра</span><span class="sxs-lookup"><span data-stu-id="09b3f-142">Kernel-Mode Windows Filtering Platform API - Reference</span></span>](/windows-hardware/drivers/ddi/_netvista/)
</dt> <dt>

[<span data-ttu-id="09b3f-143">Брандмауэр Windows в режиме повышенной безопасности</span><span class="sxs-lookup"><span data-stu-id="09b3f-143">Windows Firewall with Advanced Security</span></span>](/previous-versions/windows/desktop/ics/windows-firewall-advanced-security-start-page)
</dt> <dt>

[<span data-ttu-id="09b3f-144">Расширяемый вспомогательный класс диагностики WFP</span><span class="sxs-lookup"><span data-stu-id="09b3f-144">WFP Diagnostics Extensible Helper Class</span></span>](/windows/desktop/NDF/windows-filtering-platform-extensible-helper-class)
</dt> <dt>

[<span data-ttu-id="09b3f-145">Расширения безопасных сокетов Winsock</span><span class="sxs-lookup"><span data-stu-id="09b3f-145">Winsock Secure Socket Extensions</span></span>](/windows/desktop/WinSock/winsock-secure-socket-extensions)
</dt> </dl>

 

