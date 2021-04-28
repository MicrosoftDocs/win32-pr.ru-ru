---
title: TraceLogging
description: TraceLogging
ms.assetid: c516424a-9eba-4b56-80de-8c713fd3461a
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b7bd83c608d2ac98fdccce760c851496af80c217
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2021
ms.locfileid: "108116722"
---
# <a name="tracelogging"></a><span data-ttu-id="76c60-103">TraceLogging</span><span class="sxs-lookup"><span data-stu-id="76c60-103">TraceLogging</span></span>

## <a name="purpose"></a><span data-ttu-id="76c60-104">Цель</span><span class="sxs-lookup"><span data-stu-id="76c60-104">Purpose</span></span>

<span data-ttu-id="76c60-105">Трацелоггинг — это новая платформа трассировки событий Windows 10 для приложений пользовательского режима и драйверов режима ядра.</span><span class="sxs-lookup"><span data-stu-id="76c60-105">TraceLogging is the new Windows 10 event tracing framework for user-mode applications and kernel-mode drivers.</span></span> <span data-ttu-id="76c60-106">Трацелоггинг строится на трассировке событий Windows (ETW) и предоставляет упрощенный способ инструментирования кода.</span><span class="sxs-lookup"><span data-stu-id="76c60-106">TraceLogging builds on Event Tracing for Windows (ETW) and provides a simplified way to instrument code.</span></span>

## <a name="in-this-section"></a><span data-ttu-id="76c60-107">В этом разделе</span><span class="sxs-lookup"><span data-stu-id="76c60-107">In this section</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="76c60-108">Раздел</span><span class="sxs-lookup"><span data-stu-id="76c60-108">Topic</span></span></th>
<th><span data-ttu-id="76c60-109">Описание</span><span class="sxs-lookup"><span data-stu-id="76c60-109">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="76c60-110"><a href="trace-logging-about.md">О Трацелоггинг</a></span><span class="sxs-lookup"><span data-stu-id="76c60-110"><a href="trace-logging-about.md">About TraceLogging</a></span></span><br/></td>
<td><span data-ttu-id="76c60-111">Трацелоггинг — это новая трассировка событий Windows 10 для приложений пользовательского режима и драйверов режима ядра.</span><span class="sxs-lookup"><span data-stu-id="76c60-111">TraceLogging is the new Windows 10 event tracing for user-mode applications and kernel-mode drivers.</span></span> <span data-ttu-id="76c60-112">Трацелоггинг — это формат для самостоятельного описания трассировки событий Windows (ETW).</span><span class="sxs-lookup"><span data-stu-id="76c60-112">TraceLogging is a format for self-describing Event Tracing for Windows (ETW).</span></span> <span data-ttu-id="76c60-113">Трацелоггинг строится на трассировке событий Windows (ETW) и предоставляет упрощенный способ инструментирования кода.</span><span class="sxs-lookup"><span data-stu-id="76c60-113">TraceLogging builds on Event Tracing for Windows (ETW) and provides a simplified way to instrument code.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="76c60-114"><a href="tracelogging-using-tracelogging.md">Использование Трацелоггинг</a></span><span class="sxs-lookup"><span data-stu-id="76c60-114"><a href="tracelogging-using-tracelogging.md">Using TraceLogging</a></span></span><br/></td>
<td><span data-ttu-id="76c60-115">В следующих разделах приводятся краткие инструкции по Трацелоггинг для машинного и управляемого кода с примерами.</span><span class="sxs-lookup"><span data-stu-id="76c60-115">The following topics provide a TraceLogging quick start for native and managed code, with examples.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="76c60-116"><a href="trace-logging-reference.md">Справочник по Трацелоггинг</a></span><span class="sxs-lookup"><span data-stu-id="76c60-116"><a href="trace-logging-reference.md">TraceLogging Reference</a></span></span><br/></td>
<td><span data-ttu-id="76c60-117">В следующих разделах содержатся сведения о собственном API Трацелоггинг.</span><span class="sxs-lookup"><span data-stu-id="76c60-117">The following topics provide information about the native TraceLogging API.</span></span><br/> <span data-ttu-id="76c60-118">Трацелоггинг строится на трассировке событий Windows (ETW) и предоставляет упрощенный способ инструментирования кода.</span><span class="sxs-lookup"><span data-stu-id="76c60-118">TraceLogging builds on Event Tracing for Windows (ETW) and provides a simplified way to instrument code.</span></span> <span data-ttu-id="76c60-119">Трацелоггинг позволяет включать структурированные данные с событиями, сопоставлять события и не требует отдельного XML-файла манифеста инструментирования.</span><span class="sxs-lookup"><span data-stu-id="76c60-119">TraceLogging allows you to include structured data with events, correlate events, and does not require a separate instrumentation manifest XML file.</span></span><br/> <span data-ttu-id="76c60-120"><span class="underline">Для разработчиков WinRT</span></span><span class="sxs-lookup"><span data-stu-id="76c60-120"><span class="underline">For WinRT developers</span></span></span><br/>
<ul>
<li><span data-ttu-id="76c60-121"><a href="/uwp/api/Windows.Foundation.Diagnostics.LoggingChannel"><strong>LoggingChannel</strong></a> был расширен в Windows 10 для записи в журнал событий трассировки событий Windows (ETW) без необходимости манифеста.</span><span class="sxs-lookup"><span data-stu-id="76c60-121"><a href="/uwp/api/Windows.Foundation.Diagnostics.LoggingChannel"><strong>LoggingChannel</strong></a> has been extended in Windows 10 to log self-describing Event Tracing for Windows (ETW) events without the need for a manifest.</span></span></li>
<li><span data-ttu-id="76c60-122"><a href="/windows/win32/api/traceloggingactivity/nl-traceloggingactivity-traceloggingactivity"><strong>Логгингактивити</strong></a> был расширен в Windows 10 для предоставления методов запуска и отмены действия, которые обеспечивают управление форматом и содержимым событий запуска и завершения.</span><span class="sxs-lookup"><span data-stu-id="76c60-122"><a href="/windows/win32/api/traceloggingactivity/nl-traceloggingactivity-traceloggingactivity"><strong>LoggingActivity</strong></a> has been extended in Windows 10 to provide activity start and stop methods that provide control over the format and contents of the Start and Stop events.</span></span> <span data-ttu-id="76c60-123">Кроме того, действия могут быть вложенными.</span><span class="sxs-lookup"><span data-stu-id="76c60-123">Additionally, activities can be nested.</span></span></li>
</ul><span data-ttu-id="76c60-124">
<span class="underline">Для разработчиков управляемого кода (Microsoft .NET Framework)</span></span><span class="sxs-lookup"><span data-stu-id="76c60-124">
<span class="underline">For managed code (Microsoft .NET Framework) developers</span></span></span><br/>
<ul>
<li><span data-ttu-id="76c60-125">Класс <a href="/dotnet/api/system.diagnostics.tracing.eventsource">EventSource</a> , поставляемый с предыдущими версиями платформа .NET Framework, уже поддерживает запись событий ETW без необходимости в манифесте.</span><span class="sxs-lookup"><span data-stu-id="76c60-125">The <a href="/dotnet/api/system.diagnostics.tracing.eventsource">EventSource</a> class that shipped with previous versions of the .NET Framework already supports writing ETW events without the need for a manifest.</span></span> <span data-ttu-id="76c60-126">Однако разработчикам требовалось использовать EventSource в качестве базового класса и добавлять атрибуты и методы в производный класс, который был автоматически включен в манифест ETW.</span><span class="sxs-lookup"><span data-stu-id="76c60-126">However, developers were required to use EventSource as a base class and add attributes and methods to the derived class that were turned into an ETW manifest automatically.</span></span> <span data-ttu-id="76c60-127">Теперь разработчики не должны быть производными от EventSource и вместо этого могут использовать EventSource непосредственно для регистрации событий с самоописанием, не требующих манифеста.</span><span class="sxs-lookup"><span data-stu-id="76c60-127">Now, developers do not have to derive from EventSource and can instead use EventSource directly to log self-describing events that do not require a manifest.</span></span></li>
</ul><span data-ttu-id="76c60-128">
<span class="underline">Для разработчиков C/C++</span></span><span class="sxs-lookup"><span data-stu-id="76c60-128">
<span class="underline">For C/C++ developers</span></span></span><br/>
<ul>
<li><span data-ttu-id="76c60-129">Трацелоггингпровидер. h — рекомендуемый API для разработчиков C/C++ в режиме пользователя или ядра.</span><span class="sxs-lookup"><span data-stu-id="76c60-129">TraceLoggingProvider.h is the recommended API for C/C++ developers in user or kernel mode.</span></span> <span data-ttu-id="76c60-130">Этот API плохо подходит для использования в динамических сценариях (сценариях), таких как JavaScript.</span><span class="sxs-lookup"><span data-stu-id="76c60-130">This API is not well suited for use in dynamic (scripted) scenarios such as Javascript.</span></span> <span data-ttu-id="76c60-131">Следующие ссылки описывают API C/C++.</span><span class="sxs-lookup"><span data-stu-id="76c60-131">The following links describe the C/C++ API.</span></span></li>
</ul></td>
</tr>
</tbody>
</table>



 

## <a name="developer-audience"></a><span data-ttu-id="76c60-132">Аудитория разработчиков</span><span class="sxs-lookup"><span data-stu-id="76c60-132">Developer audience</span></span>

<span data-ttu-id="76c60-133">Трацелоггинг предназначен для использования разработчиками приложений пользовательского режима и разработчиками драйверов в режиме ядра, которые хотят добавить трассировку в свой код.</span><span class="sxs-lookup"><span data-stu-id="76c60-133">TraceLogging is designed for use by user-mode application developers and kernel-mode driver developers who want to add tracing to their code.</span></span>

