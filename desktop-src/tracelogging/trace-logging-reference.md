---
title: Справочник по Трацелоггинг
description: В следующих разделах содержатся сведения о собственном API Трацелоггинг. Трацелоггинг строится на трассировке событий Windows (ETW) и предоставляет упрощенный способ инструментирования кода.
ms.assetid: 9E3F2140-DDB0-4C30-B7D0-A81F11823AA6
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 71d81874e7aeb1a0618716b00d225d215c382ee1
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "104413584"
---
# <a name="tracelogging-reference"></a><span data-ttu-id="325c5-103">Справочник по Трацелоггинг</span><span class="sxs-lookup"><span data-stu-id="325c5-103">TraceLogging Reference</span></span>

<span data-ttu-id="325c5-104">В следующих разделах содержатся сведения о собственном API Трацелоггинг.</span><span class="sxs-lookup"><span data-stu-id="325c5-104">The following topics provide information about the native TraceLogging API.</span></span>

<span data-ttu-id="325c5-105">Трацелоггинг строится на трассировке событий Windows (ETW) и предоставляет упрощенный способ инструментирования кода.</span><span class="sxs-lookup"><span data-stu-id="325c5-105">TraceLogging builds on Event Tracing for Windows (ETW) and provides a simplified way to instrument code.</span></span> <span data-ttu-id="325c5-106">Трацелоггинг позволяет включать структурированные данные с событиями, сопоставлять события и не требует отдельного XML-файла манифеста инструментирования.</span><span class="sxs-lookup"><span data-stu-id="325c5-106">TraceLogging allows you to include structured data with events, correlate events, and does not require a separate instrumentation manifest XML file.</span></span>

<span data-ttu-id="325c5-107"><span class="underline">Для разработчиков WinRT</span></span><span class="sxs-lookup"><span data-stu-id="325c5-107"><span class="underline">For WinRT developers</span></span></span>

-   <span data-ttu-id="325c5-108">[**LoggingChannel**](/uwp/api/Windows.Foundation.Diagnostics.LoggingChannel) был расширен в Windows 10 для записи в журнал событий трассировки событий Windows (ETW) без необходимости манифеста.</span><span class="sxs-lookup"><span data-stu-id="325c5-108">[**LoggingChannel**](/uwp/api/Windows.Foundation.Diagnostics.LoggingChannel) has been extended in Windows 10 to log self-describing Event Tracing for Windows (ETW) events without the need for a manifest.</span></span>
-   <span data-ttu-id="325c5-109">[**Логгингактивити**](/windows/win32/api/traceloggingactivity/nl-traceloggingactivity-traceloggingactivity) был расширен в Windows 10 для предоставления методов запуска и отмены действия, которые обеспечивают управление форматом и содержимым событий запуска и завершения.</span><span class="sxs-lookup"><span data-stu-id="325c5-109">[**LoggingActivity**](/windows/win32/api/traceloggingactivity/nl-traceloggingactivity-traceloggingactivity) has been extended in Windows 10 to provide activity start and stop methods that provide control over the format and contents of the Start and Stop events.</span></span> <span data-ttu-id="325c5-110">Кроме того, действия могут быть вложенными.</span><span class="sxs-lookup"><span data-stu-id="325c5-110">Additionally, activities can be nested.</span></span>

<span data-ttu-id="325c5-111"><span class="underline">Для разработчиков управляемого кода (Microsoft .NET Framework)</span></span><span class="sxs-lookup"><span data-stu-id="325c5-111"><span class="underline">For managed code (Microsoft .NET Framework) developers</span></span></span>

-   <span data-ttu-id="325c5-112">Класс [EventSource](/dotnet/api/system.diagnostics.tracing.eventsource) , поставляемый с предыдущими версиями платформа .NET Framework, уже поддерживает запись событий ETW без необходимости в манифесте.</span><span class="sxs-lookup"><span data-stu-id="325c5-112">The [EventSource](/dotnet/api/system.diagnostics.tracing.eventsource) class that shipped with previous versions of the .NET Framework already supports writing ETW events without the need for a manifest.</span></span> <span data-ttu-id="325c5-113">Однако разработчикам требовалось использовать EventSource в качестве базового класса и добавлять атрибуты и методы в производный класс, который был автоматически включен в манифест ETW.</span><span class="sxs-lookup"><span data-stu-id="325c5-113">However, developers were required to use EventSource as a base class and add attributes and methods to the derived class that were turned into an ETW manifest automatically.</span></span> <span data-ttu-id="325c5-114">Теперь разработчики не должны быть производными от EventSource и вместо этого могут использовать EventSource непосредственно для регистрации событий с самоописанием, не требующих манифеста.</span><span class="sxs-lookup"><span data-stu-id="325c5-114">Now, developers do not have to derive from EventSource and can instead use EventSource directly to log self-describing events that do not require a manifest.</span></span>

<span data-ttu-id="325c5-115"><span class="underline">Для разработчиков C/C++</span></span><span class="sxs-lookup"><span data-stu-id="325c5-115"><span class="underline">For C/C++ developers</span></span></span>

-   <span data-ttu-id="325c5-116">Трацелоггингпровидер. h — рекомендуемый API для разработчиков C/C++ в режиме пользователя или ядра.</span><span class="sxs-lookup"><span data-stu-id="325c5-116">TraceLoggingProvider.h is the recommended API for C/C++ developers in user or kernel mode.</span></span> <span data-ttu-id="325c5-117">Этот API плохо подходит для использования в динамических сценариях (сценариях), таких как JavaScript.</span><span class="sxs-lookup"><span data-stu-id="325c5-117">This API is not well suited for use in dynamic (scripted) scenarios such as Javascript.</span></span> <span data-ttu-id="325c5-118">Следующие ссылки описывают API C/C++.</span><span class="sxs-lookup"><span data-stu-id="325c5-118">The following links describe the C/C++ API.</span></span>

<!-- -->

-   [<span data-ttu-id="325c5-119">Классы</span><span class="sxs-lookup"><span data-stu-id="325c5-119">Classes</span></span>](trace-logging-classes.md)
-   [<span data-ttu-id="325c5-120">Функции</span><span class="sxs-lookup"><span data-stu-id="325c5-120">Functions</span></span>](trace-logging-functions.md)
-   [<span data-ttu-id="325c5-121">Макросы</span><span class="sxs-lookup"><span data-stu-id="325c5-121">Macros</span></span>](trace-logging-macros.md)

<span data-ttu-id="325c5-122">Обратите внимание, что значение WINVER повлияет на то, как Трацелоггингпровидер. h ведет себя.</span><span class="sxs-lookup"><span data-stu-id="325c5-122">Note that the value of WINVER will impact the way TraceLoggingProvider.h behaves.</span></span>

-   <span data-ttu-id="325c5-123">Если параметр WINVER не установлен перед включением <Windows. h>, то <Windows. h> установит для WINVER значение по умолчанию, соответствующее версии пакета SDK.</span><span class="sxs-lookup"><span data-stu-id="325c5-123">If WINVER is not set before including <windows.h>, then <windows.h> will set WINVER to a default value corresponding to the SDK version.</span></span>
-   <span data-ttu-id="325c5-124">При использовании Трацелоггингпровидер. h с параметром WINVER, равным 0x0602 (Windows 8) или более поздней версии, программа не будет работать в Windows Vista или Windows 7.</span><span class="sxs-lookup"><span data-stu-id="325c5-124">Using TraceLoggingProvider.h with WINVER set to 0x0602 (Windows 8) or higher, the program will not run on Windows Vista or Windows 7.</span></span>
-   <span data-ttu-id="325c5-125">При использовании Трацелоггингпровидер. h с параметром WINVER, имеющим значение 0x0600 (Windows Vista) или 0x0601 (Windows 7), программа будет настроена на совместимость и будет работать с указанными версиями Windows.</span><span class="sxs-lookup"><span data-stu-id="325c5-125">Using TraceLoggingProvider.h with WINVER set to 0x0600 (Windows Vista) or 0x0601 (Windows 7), the program will be configured for compatibility and will work on the specified versions of Windows.</span></span>

 

 