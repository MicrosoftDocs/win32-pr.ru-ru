---
description: Эта документация предназначена для приложений пользовательского режима, которые хотят использовать ETW. Сведения об инструментировании драйверов устройств, выполняемых в режиме ядра, см. в разделе Трассировка программного обеспечения WPP и добавление трассировки событий для Kernel-Mode драйверов в наборе драйверов Windows (WDK).
ms.assetid: 3de69436-671b-46a2-8d92-4eb3af2a4233
title: Трассировка событий
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9802635fffddfea79c979534771605af13949d69
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "104349325"
---
# <a name="event-tracing"></a><span data-ttu-id="72f8f-104">Трассировка событий</span><span class="sxs-lookup"><span data-stu-id="72f8f-104">Event Tracing</span></span>

## <a name="purpose"></a><span data-ttu-id="72f8f-105">Назначение</span><span class="sxs-lookup"><span data-stu-id="72f8f-105">Purpose</span></span>

<span data-ttu-id="72f8f-106">Трассировка событий для Windows (ETW) предоставляет программистам приложений возможность запускать и прекращать сеансы трассировки событий, инструментировать приложение для предоставления событий трассировки и использовать события трассировки.</span><span class="sxs-lookup"><span data-stu-id="72f8f-106">Event Tracing for Windows (ETW) provides application programmers the ability to start and stop event tracing sessions, instrument an application to provide trace events, and consume trace events.</span></span> <span data-ttu-id="72f8f-107">События трассировки содержат заголовок события и определяемые поставщиком данные, описывающие текущее состояние приложения или операции.</span><span class="sxs-lookup"><span data-stu-id="72f8f-107">Trace events contain an event header and provider-defined data that describes the current state of an application or operation.</span></span> <span data-ttu-id="72f8f-108">События можно использовать для отладки приложения и выполнения анализа емкости и производительности.</span><span class="sxs-lookup"><span data-stu-id="72f8f-108">You can use the events to debug an application and perform capacity and performance analysis.</span></span>

<span data-ttu-id="72f8f-109">Эта документация предназначена для приложений пользовательского режима, которые хотят использовать ETW.</span><span class="sxs-lookup"><span data-stu-id="72f8f-109">This documentation is for user-mode applications that want to use ETW.</span></span> <span data-ttu-id="72f8f-110">Сведения об инструментировании драйверов устройств, выполняемых в режиме ядра, см. в разделе [Трассировка программного обеспечения WPP](/windows-hardware/drivers/devtest/wpp-software-tracing) и [Добавление трассировки событий для Kernel-Mode драйверов](/windows-hardware/drivers/devtest/event-tracing-for-windows--etw-) в наборе драйверов Windows (WDK).</span><span class="sxs-lookup"><span data-stu-id="72f8f-110">For information about instrumenting device drivers that run in kernel mode, see [WPP Software Tracing](/windows-hardware/drivers/devtest/wpp-software-tracing) and [Adding Event Tracing to Kernel-Mode Drivers](/windows-hardware/drivers/devtest/event-tracing-for-windows--etw-) in the Windows Driver Kit (WDK).</span></span>

## <a name="where-applicable"></a><span data-ttu-id="72f8f-111">Где применимо</span><span class="sxs-lookup"><span data-stu-id="72f8f-111">Where applicable</span></span>

<span data-ttu-id="72f8f-112">Используйте ETW, если требуется инструментировать приложение, записывать события пользователя или ядра в файл журнала и использовать события из файла журнала или в режиме реального времени.</span><span class="sxs-lookup"><span data-stu-id="72f8f-112">Use ETW when you want to instrument your application, log user or kernel events to a log file, and consume events from a log file or in real time.</span></span>

## <a name="developer-audience"></a><span data-ttu-id="72f8f-113">Аудитория разработчиков</span><span class="sxs-lookup"><span data-stu-id="72f8f-113">Developer audience</span></span>

<span data-ttu-id="72f8f-114">Трассировка событий Windows разработана для разработчиков на C и C++, которые пишут приложения пользовательского режима.</span><span class="sxs-lookup"><span data-stu-id="72f8f-114">ETW is designed for C and C++ developers who write user-mode applications.</span></span>

## <a name="run-time-requirements"></a><span data-ttu-id="72f8f-115">Требования к среде выполнения</span><span class="sxs-lookup"><span data-stu-id="72f8f-115">Run-time requirements</span></span>

<span data-ttu-id="72f8f-116">ETW входит в состав Microsoft Windows 2000 и более поздних версий.</span><span class="sxs-lookup"><span data-stu-id="72f8f-116">ETW is included in Microsoft Windows 2000 and later.</span></span> <span data-ttu-id="72f8f-117">Сведения о том, какие операционные системы требуются для использования определенной функции, см. в разделе "требования" документации по функции.</span><span class="sxs-lookup"><span data-stu-id="72f8f-117">For information about which operating systems are required to use a particular function, see the Requirements section of the documentation for the function.</span></span>

## <a name="process-etw-traces-in-net-code"></a><span data-ttu-id="72f8f-118">Обработка трассировок трассировки событий Windows в коде .NET</span><span class="sxs-lookup"><span data-stu-id="72f8f-118">Process ETW traces in .NET code</span></span>

<span data-ttu-id="72f8f-119">Вы можете использовать [API .NET трацепроцессинг](https://www.nuget.org/packages/Microsoft.Windows.EventTracing.Processing.All) для анализа трассировок трассировки событий Windows для приложений и других программных компонентов.</span><span class="sxs-lookup"><span data-stu-id="72f8f-119">You can use the [.NET TraceProcessing API](https://www.nuget.org/packages/Microsoft.Windows.EventTracing.Processing.All) to analyze ETW traces for your applications and other software components.</span></span> <span data-ttu-id="72f8f-120">Этот API внутренне используется в корпорации Майкрософт для анализа данных ETW, созданных в системе разработки Windows, а также для включения нескольких таблиц в [анализаторе производительности Windows](/windows-hardware/test/wpt/windows-performance-analyzer).</span><span class="sxs-lookup"><span data-stu-id="72f8f-120">This API is used internally at Microsoft to analyze ETW data produced the Windows engineering system, and it is also used to power several tables in [Windows Performance Analyzer](/windows-hardware/test/wpt/windows-performance-analyzer).</span></span> <span data-ttu-id="72f8f-121">Этот API доступен в виде пакета NuGet.</span><span class="sxs-lookup"><span data-stu-id="72f8f-121">This API is available as a NuGet package.</span></span>

<span data-ttu-id="72f8f-122">Дополнительные сведения см. в [этой статье](/windows/apps/trace-processing/overview).</span><span class="sxs-lookup"><span data-stu-id="72f8f-122">For more information, see [this article](/windows/apps/trace-processing/overview).</span></span>

## <a name="in-this-section"></a><span data-ttu-id="72f8f-123">В этом разделе</span><span class="sxs-lookup"><span data-stu-id="72f8f-123">In this section</span></span>



| <span data-ttu-id="72f8f-124">Раздел</span><span class="sxs-lookup"><span data-stu-id="72f8f-124">Topic</span></span>                                                                     | <span data-ttu-id="72f8f-125">Описание</span><span class="sxs-lookup"><span data-stu-id="72f8f-125">Description</span></span>                                                                        |
|---------------------------------------------------------------------------|------------------------------------------------------------------------------------|
| [<span data-ttu-id="72f8f-126">Новые возможности трассировки событий</span><span class="sxs-lookup"><span data-stu-id="72f8f-126">What's New in Event Tracing</span></span>](what-s-new-in-event-tracing.md)<br/> | <span data-ttu-id="72f8f-127">Новые функции, добавленные в трассировку событий в каждом выпуске.</span><span class="sxs-lookup"><span data-stu-id="72f8f-127">New features that were added to Event Tracing in each release.</span></span><br/>          |
| [<span data-ttu-id="72f8f-128">Сведения о трассировке событий</span><span class="sxs-lookup"><span data-stu-id="72f8f-128">About Event Tracing</span></span>](about-event-tracing.md)<br/>                 | <span data-ttu-id="72f8f-129">Общие сведения о трассировке событий.</span><span class="sxs-lookup"><span data-stu-id="72f8f-129">General information about Event Tracing.</span></span><br/>                                |
| [<span data-ttu-id="72f8f-130">Использование трассировки событий</span><span class="sxs-lookup"><span data-stu-id="72f8f-130">Using Event Tracing</span></span>](using-event-tracing.md)<br/>                 | <span data-ttu-id="72f8f-131">Разделы, связанные с задачами, в которых описывается использование API ETW.</span><span class="sxs-lookup"><span data-stu-id="72f8f-131">Task-related topics that describe how to use the ETW API.</span></span><br/>               |
| [<span data-ttu-id="72f8f-132">Справочник по трассировке событий</span><span class="sxs-lookup"><span data-stu-id="72f8f-132">Event Tracing Reference</span></span>](event-tracing-reference.md)<br/>         | <span data-ttu-id="72f8f-133">Подробное описание функций ETW и других программных элементов.</span><span class="sxs-lookup"><span data-stu-id="72f8f-133">Detailed descriptions of ETW functions and other programming elements.</span></span> <br/> |



 

 

 
