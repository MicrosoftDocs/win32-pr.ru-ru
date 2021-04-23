---
description: Закрытый сеанс трассировки событий — это сеанс трассировки пользовательского режима, который выполняется в том же процессе, что и его поставщики трассировки событий&\# 8212; частный сеанс и поставщики, которые он включает, должны находиться в одном процессе.
ms.assetid: fb6a3899-194e-4cb7-b9e5-a7ff85fb7891
title: Настройка и запуск закрытого сеанса ведения журнала
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 15ef13728bfb3516197ab153cf90b301d5930ff2
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104497712"
---
# <a name="configuring-and-starting-a-private-logger-session"></a><span data-ttu-id="11729-103">Настройка и запуск закрытого сеанса ведения журнала</span><span class="sxs-lookup"><span data-stu-id="11729-103">Configuring and Starting a Private Logger Session</span></span>

<span data-ttu-id="11729-104">Закрытый сеанс трассировки событий — это сеанс трассировки пользовательского режима, который выполняется в том же процессе, что и его поставщики трассировки событий — частный сеанс и поставщики, которые он включает, должны находиться в одном процессе.</span><span class="sxs-lookup"><span data-stu-id="11729-104">A private event tracing session is a user-mode event tracing session that runs in the same process as its event trace providers—the private session and the providers that it enables must all be in the same process.</span></span> <span data-ttu-id="11729-105">Преимуществом использования закрытого сеанса является то, что частный сеанс не учитывает максимум 64 сеансов трассировки событий, выполняемых одновременно.</span><span class="sxs-lookup"><span data-stu-id="11729-105">The benefit of using a private session is that the private session does not count against the maximum of 64 event tracing sessions executing simultaneously.</span></span>

<span data-ttu-id="11729-106">Настройка и запуск частного сеанса аналогичны запуску обычного сеанса трассировки событий.</span><span class="sxs-lookup"><span data-stu-id="11729-106">Configuring and starting a private session is similar to starting a normal event trace session.</span></span> <span data-ttu-id="11729-107">Разница заключается в том, что элемент **вноде. GUID** структуры [**\_ \_ свойств трассировки событий**](/windows/win32/api/evntrace/ns-evntrace-event_trace_properties) должен содержать **идентификатор GUID** поставщика, а не сеанса, а поставщик должен уже зарегистрировать идентификатор GUID.</span><span class="sxs-lookup"><span data-stu-id="11729-107">The difference is that **Wnode.Guid** member of the [**EVENT\_TRACE\_PROPERTIES**](/windows/win32/api/evntrace/ns-evntrace-event_trace_properties) structure must contain the **GUID** of the provider, not the session, and the provider must have already registered the GUID.</span></span> <span data-ttu-id="11729-108">Обратите внимание, что, если вы также настроили \_ функцию трассировки событий " \_ частный" \_ в \_ режиме ведения журнала, можно использовать другой **идентификатор GUID** для сеанса и поставщика.</span><span class="sxs-lookup"><span data-stu-id="11729-108">Note that if you also set the EVENT\_TRACE\_PRIVATE\_IN\_PROC logging mode, you can use a different **GUID** for the session and provider.</span></span> <span data-ttu-id="11729-109">Дополнительные сведения о запуске обычного сеанса трассировки событий см. в разделе [Настройка и запуск сеанса трассировки событий](configuring-and-starting-an-event-tracing-session.md).</span><span class="sxs-lookup"><span data-stu-id="11729-109">For details on starting a normal event trace session, see [Configuring and Starting an Event Tracing Session](configuring-and-starting-an-event-tracing-session.md).</span></span>

<span data-ttu-id="11729-110">Обратите внимание, что нельзя запускать, прекращать или сбрасывать закрытый сеанс трассировки из DllMain; Это необходимо сделать в подпрограммых инициализации и финализации библиотеки DLL.</span><span class="sxs-lookup"><span data-stu-id="11729-110">Note that you cannot start, stop, or flush a private trace session from DllMain; you should do so in the initialization and finalization routines of the DLL.</span></span>

<span data-ttu-id="11729-111">Из Windows 8.1 к Windows 10, версия 1607, полезные данные события, область действия и фильтры анализа стека могут использоваться функцией [**EnableTraceEx2**](/windows/win32/api/evntrace/nf-evntrace-enabletraceex2) , а [**параметры включения \_ трассировки \_**](/windows/win32/api/evntrace/ns-evntrace-enable_trace_parameters) и [**\_ \_ дескриптора фильтра событий**](/windows/desktop/api/Evntprov/ns-evntprov-event_filter_descriptor) — для фильтрации конкретных условий в сеансе ведения журнала.</span><span class="sxs-lookup"><span data-stu-id="11729-111">From Windows 8.1 to Windows 10, version 1607, event payload, scope, and stack walk filters can be used by the [**EnableTraceEx2**](/windows/win32/api/evntrace/nf-evntrace-enabletraceex2) function and the [**ENABLE\_TRACE\_PARAMETERS**](/windows/win32/api/evntrace/ns-evntrace-enable_trace_parameters) and [**EVENT\_FILTER\_DESCRIPTOR**](/windows/desktop/api/Evntprov/ns-evntprov-event_filter_descriptor) structures to filter on specific conditions in a logger session.</span></span> <span data-ttu-id="11729-112">Дополнительные сведения о фильтрах полезных данных событий см. в статьях функции [**тдхкреатепайлоадфилтер**](/windows/desktop/api/Tdh/nf-tdh-tdhcreatepayloadfilter)и [**тдхаггрегатепайлоадфилтерс**](/windows/desktop/api/Tdh/nf-tdh-tdhaggregatepayloadfilters) , а также структуры [**\_ \_ предикатов**](/windows/desktop/api/Tdh/ns-tdh-payload_filter_predicate) **включения \_ трассировки \_**, **\_ \_ дескриптора фильтра событий** и фильтра полезных данных.</span><span class="sxs-lookup"><span data-stu-id="11729-112">For more information on event payload filters, see the [**TdhCreatePayloadFilter**](/windows/desktop/api/Tdh/nf-tdh-tdhcreatepayloadfilter), and [**TdhAggregatePayloadFilters**](/windows/desktop/api/Tdh/nf-tdh-tdhaggregatepayloadfilters) functions and the **ENABLE\_TRACE\_PARAMETERS**, **EVENT\_FILTER\_DESCRIPTOR**, and [**PAYLOAD\_FILTER\_PREDICATE**](/windows/desktop/api/Tdh/ns-tdh-payload_filter_predicate) structures.</span></span>

<span data-ttu-id="11729-113">Начиная с Windows 10, версия 1703, пользователи с низким уровнем привилегий теперь могут запускать закрытый сеанс ведения журнала в запущенных процессах.</span><span class="sxs-lookup"><span data-stu-id="11729-113">Starting with Windows 10, version 1703, low privilege users can now start a private logger session in processes they started.</span></span> <span data-ttu-id="11729-114">Перед включением или запуском закрытого сеанса поставщик больше не должен регистрироваться, что означает, что поставщик является "предварительно включенным", как и у поставщиков сеансов, не являющихся частными.</span><span class="sxs-lookup"><span data-stu-id="11729-114">The provider no longer needs to be registered prior to enabling or starting the private session, meaning the provider is "pre-enabled" similar to how non-private session providers are.</span></span> <span data-ttu-id="11729-115">Для отдельного процесса существует ограничение в 8 общесистемных служебных средств ведения журнала.</span><span class="sxs-lookup"><span data-stu-id="11729-115">There is a limit of 8 system wide private loggers to an individual process.</span></span> <span data-ttu-id="11729-116">Для повышения производительности в межпроцессных сценариях рекомендуется использовать фильтрацию для интерфейсов API сеанса (включая [**контролтраце**](/windows/win32/api/evntrace/nf-evntrace-controltracea), [**куеритраце**](/windows/win32/api/evntrace/nf-evntrace-querytrace), [**старттраце**](/windows/win32/api/evntrace/nf-evntrace-starttracea)и [**стоптраце**](/windows/win32/api/evntrace/nf-evntrace-stoptrace)) при запуске закрытого частного средства ведения журнала.</span><span class="sxs-lookup"><span data-stu-id="11729-116">For increased performance in cross process scenarios, it's recommended to use filtering for session APIs (including [**ControlTrace**](/windows/win32/api/evntrace/nf-evntrace-controltracea), [**QueryTrace**](/windows/win32/api/evntrace/nf-evntrace-querytrace), [**StartTrace**](/windows/win32/api/evntrace/nf-evntrace-starttracea), and [**StopTrace**](/windows/win32/api/evntrace/nf-evntrace-stoptrace)) when starting a system wide private logger.</span></span> <span data-ttu-id="11729-117">Обратите внимание, что одни и те же фильтры должны передаваться всем API-интерфейсам сеанса.</span><span class="sxs-lookup"><span data-stu-id="11729-117">Note that the same filters should be passed to all session APIs.</span></span> <span data-ttu-id="11729-118">Дополнительные сведения о фильтрах см. в разделе [**\_ Свойства трассировки событий \_ \_ версии 2**](/windows/win32/api/evntrace/ns-evntrace-event_trace_properties_v2).</span><span class="sxs-lookup"><span data-stu-id="11729-118">For more information about filters, see [**EVENT\_TRACE\_PROPERTIES\_V2**](/windows/win32/api/evntrace/ns-evntrace-event_trace_properties_v2).</span></span>

<span data-ttu-id="11729-119">Дополнительные сведения о запуске сеанса трассировки событий см. в разделе [Настройка и запуск сеанса трассировки событий](configuring-and-starting-an-event-tracing-session.md).</span><span class="sxs-lookup"><span data-stu-id="11729-119">For details on starting an event tracing session, see [Configuring and Starting an Event Tracing Session](configuring-and-starting-an-event-tracing-session.md).</span></span>

<span data-ttu-id="11729-120">Дополнительные сведения о запуске сеанса ведения журнала ядра NT см. в разделе [Настройка и запуск сеанса ведения журнала ядра NT](configuring-and-starting-the-nt-kernel-logger-session.md).</span><span class="sxs-lookup"><span data-stu-id="11729-120">For details on starting an NT Kernel Logger session, see [Configuring and Starting the NT Kernel Logger Session](configuring-and-starting-the-nt-kernel-logger-session.md).</span></span>

<span data-ttu-id="11729-121">Дополнительные сведения о запуске глобального сеанса ведения журнала см. в разделе [Настройка и запуск глобального сеанса ведения журнала](configuring-and-starting-the-global-logger-session.md).</span><span class="sxs-lookup"><span data-stu-id="11729-121">For details on starting a Global Logger session, see [Configuring and Starting a Global Logger Session](configuring-and-starting-the-global-logger-session.md).</span></span>

<span data-ttu-id="11729-122">Дополнительные сведения о запуске сеанса авторегистратора см. в разделе [Настройка и запуск сеанса авторегистратора](configuring-and-starting-an-autologger-session.md).</span><span class="sxs-lookup"><span data-stu-id="11729-122">For details on starting an AutoLogger session, see [Configuring and Starting an AutoLogger Session](configuring-and-starting-an-autologger-session.md).</span></span>

## <a name="related-topics"></a><span data-ttu-id="11729-123">См. также</span><span class="sxs-lookup"><span data-stu-id="11729-123">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="11729-124">Настройка и запуск сеанса Системтрацепровидер</span><span class="sxs-lookup"><span data-stu-id="11729-124">Configuring and Starting a SystemTraceProvider Session</span></span>](configuring-and-starting-a-systemtraceprovider-session.md)
</dt> <dt>

[<span data-ttu-id="11729-125">Настройка и запуск сеанса авторегистратора</span><span class="sxs-lookup"><span data-stu-id="11729-125">Configuring and Starting an AutoLogger Session</span></span>](configuring-and-starting-an-autologger-session.md)
</dt> <dt>

[<span data-ttu-id="11729-126">Настройка и запуск сеанса трассировки событий</span><span class="sxs-lookup"><span data-stu-id="11729-126">Configuring and Starting an Event Tracing Session</span></span>](configuring-and-starting-an-event-tracing-session.md)
</dt> <dt>

[<span data-ttu-id="11729-127">Настройка и запуск сеанса ведения журнала ядра NT</span><span class="sxs-lookup"><span data-stu-id="11729-127">Configuring and Starting the NT Kernel Logger Session</span></span>](configuring-and-starting-the-nt-kernel-logger-session.md)
</dt> <dt>

[<span data-ttu-id="11729-128">**EnableTraceEx2**</span><span class="sxs-lookup"><span data-stu-id="11729-128">**EnableTraceEx2**</span></span>](/windows/win32/api/evntrace/nf-evntrace-enabletraceex2)
</dt> <dt>

[<span data-ttu-id="11729-129">**ВКЛЮЧИТЬ \_ \_ Параметры трассировки**</span><span class="sxs-lookup"><span data-stu-id="11729-129">**ENABLE\_TRACE\_PARAMETERS**</span></span>](/windows/win32/api/evntrace/ns-evntrace-enable_trace_parameters)
</dt> <dt>

[<span data-ttu-id="11729-130">**\_Свойства трассировки \_ событий**</span><span class="sxs-lookup"><span data-stu-id="11729-130">**EVENT\_TRACE\_PROPERTIES**</span></span>](/windows/win32/api/evntrace/ns-evntrace-event_trace_properties)
</dt> <dt>

[<span data-ttu-id="11729-131">**\_Свойства трассировки \_ событий \_ версии 2**</span><span class="sxs-lookup"><span data-stu-id="11729-131">**EVENT\_TRACE\_PROPERTIES\_V2**</span></span>](/windows/win32/api/evntrace/ns-evntrace-event_trace_properties_v2)
</dt> <dt>

[<span data-ttu-id="11729-132">**\_дескриптор фильтра \_ событий**</span><span class="sxs-lookup"><span data-stu-id="11729-132">**EVENT\_FILTER\_DESCRIPTOR**</span></span>](/windows/desktop/api/Evntprov/ns-evntprov-event_filter_descriptor)
</dt> <dt>

[<span data-ttu-id="11729-133">**\_предикат фильтра полезных данных \_**</span><span class="sxs-lookup"><span data-stu-id="11729-133">**PAYLOAD\_FILTER\_PREDICATE**</span></span>](/windows/desktop/api/Tdh/ns-tdh-payload_filter_predicate)
</dt> <dt>

[<span data-ttu-id="11729-134">**тдхаггрегатепайлоадфилтерс**</span><span class="sxs-lookup"><span data-stu-id="11729-134">**TdhAggregatePayloadFilters**</span></span>](/windows/desktop/api/Tdh/nf-tdh-tdhaggregatepayloadfilters)
</dt> <dt>

[<span data-ttu-id="11729-135">**тдхкреатепайлоадфилтер**</span><span class="sxs-lookup"><span data-stu-id="11729-135">**TdhCreatePayloadFilter**</span></span>](/windows/desktop/api/Tdh/nf-tdh-tdhcreatepayloadfilter)
</dt> <dt>

[<span data-ttu-id="11729-136">Обновление сеанса трассировки событий</span><span class="sxs-lookup"><span data-stu-id="11729-136">Updating an Event Tracing Session</span></span>](updating-an-event-tracing-session.md)
</dt> </dl>

 

 
