---
description: Системтрацепровидер — это поставщик ядра с предопределенным набором событий ядра, поддерживаемых в Windows 7, Windows Server 2008 R2 и более поздних версиях.
ms.assetid: 6808EC45-C8C3-45D7-9E4C-337F6A4CF9C8
title: Настройка и запуск сеанса Системтрацепровидер
ms.topic: article
ms.date: 06/02/2021
ms.openlocfilehash: 66e9d672a7c8e6358c2a92e7661e0d4e2a5878ab
ms.sourcegitcommit: cb87082135319cbdc5df541e3071eebb83a58972
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/04/2021
ms.locfileid: "111386744"
---
# <a name="configuring-and-starting-a-systemtraceprovider-session"></a><span data-ttu-id="ef624-103">Настройка и запуск сеанса Системтрацепровидер</span><span class="sxs-lookup"><span data-stu-id="ef624-103">Configuring and Starting a SystemTraceProvider Session</span></span>

<span data-ttu-id="ef624-104">Системтрацепровидер — это поставщик ядра с предопределенным набором событий ядра, поддерживаемых в Windows 7, Windows Server 2008 R2 и более поздних версиях.</span><span class="sxs-lookup"><span data-stu-id="ef624-104">The SystemTraceProvider is a kernel provider with a predefined sets of kernel events supported on Windows 7, Windows Server 2008 R2, and later.</span></span> <span data-ttu-id="ef624-105">В Windows 7 и Windows Server 2008 R2 Системтрацепровидер можно было использовать только для сеанса ведения журнала ядра NT.</span><span class="sxs-lookup"><span data-stu-id="ef624-105">On Windows 7 and Windows Server 2008 R2, the SystemTraceProvider could only be used for the NT Kernel Logger session.</span></span>

<span data-ttu-id="ef624-106">В Windows 8, Windows Server 2012 и более поздних версий Системтрацепровидер можно мультиплексировать до восьми сеансов ведения журнала.</span><span class="sxs-lookup"><span data-stu-id="ef624-106">On Windows 8, Windows Server 2012, and later, the SystemTraceProvider can be multiplexed for up to 8 logger sessions.</span></span> <span data-ttu-id="ef624-107">Первые два слота для сеансов ведения журнала зарезервированы для журнала ядра NT и циклического средства ведения журнала контекста ядра.</span><span class="sxs-lookup"><span data-stu-id="ef624-107">The first two slots for logger sessions are reserved for the NT Kernel Logger and the Circular Kernel Context Logger .</span></span>

<span data-ttu-id="ef624-108">Дополнительные сведения об использовании сеанса ведения журнала ядра NT в качестве поставщика трассировки см. в разделе [Настройка и запуск сеанса ведения журнала ядра NT](configuring-and-starting-the-nt-kernel-logger-session.md).</span><span class="sxs-lookup"><span data-stu-id="ef624-108">For more information on using the NT Kernel Logger session as a trace provider, see [Configuring and Starting the NT Kernel Logger Session](configuring-and-starting-the-nt-kernel-logger-session.md).</span></span>

<span data-ttu-id="ef624-109">В Windows 10 SDK Build 20348 и более поздних версий Системтрацепровидер можно настроить с помощью отдельных поставщиков системы, которыми можно управлять с помощью [EnableTraceEx2](/windows/win32/api/evntrace/nf-evntrace-enabletraceex2) , таких как стандартные трассировки событий для поставщиков событий Windows.</span><span class="sxs-lookup"><span data-stu-id="ef624-109">On Windows 10 SDK build 20348 and later, the SystemTraceProvider can be configured via separate System Providers, which can be controlled with [EnableTraceEx2](/windows/win32/api/evntrace/nf-evntrace-enabletraceex2) like standard Event Tracing for Windows event providers.</span></span> <span data-ttu-id="ef624-110">Полный список поставщиков систем, ключевых слов и соответствующих устаревших флагов и групп см. в разделе [поставщики систем](system-providers.md) .</span><span class="sxs-lookup"><span data-stu-id="ef624-110">For a full list of system providers, keywords, and corresponding legacy flags and groups, see [System Providers](system-providers.md)</span></span>

## <a name="enable-a-systemtraceprovider-session"></a><span data-ttu-id="ef624-111">Включение сеанса Системтрацепровидер</span><span class="sxs-lookup"><span data-stu-id="ef624-111">Enable a SystemTraceProvider session</span></span>

<span data-ttu-id="ef624-112">Чтобы разрешить Системтрацепровидер запуск сеанса, отличного от средства ведения журнала ядра NT, выполните следующую команду:</span><span class="sxs-lookup"><span data-stu-id="ef624-112">To enable the SystemTraceProvider to start a session other than the NT Kernel Logger, execute the following command:</span></span>

<span data-ttu-id="ef624-113">**tracelog-Start MySession-f c: \\ Kernel1. ETL-ЕФЛАГ proc \_ Thread + Loader + ксвитч**</span><span class="sxs-lookup"><span data-stu-id="ef624-113">**tracelog -start MySession -f c:\\Kernel1.etl -eflag PROC\_THREAD+LOADER+CSWITCH**</span></span>

<span data-ttu-id="ef624-114">Чтобы программно включить Системтрацепровидер для запуска сеанса, отличного от средства ведения журнала ядра NT, выполните следующие действия.</span><span class="sxs-lookup"><span data-stu-id="ef624-114">To programmatically enable the SystemTraceProvider to start a session other than the NT Kernel Logger, use the following steps.</span></span>

-   <span data-ttu-id="ef624-115">Определите имя частного средства ведения журнала.</span><span class="sxs-lookup"><span data-stu-id="ef624-115">Define a private logger name.</span></span>

    <span data-ttu-id="ef624-116">**\#Определение частного \_ имени регистратора \_ L "некоторые частные сеансы трассировки"**</span><span class="sxs-lookup"><span data-stu-id="ef624-116">**\#define PRIVATE\_LOGGER\_NAME L”Some Private Trace Session”**</span></span>

-   <span data-ttu-id="ef624-117">На контроллере установите следующие элементы структуры [**\_ \_ свойств трассировки событий**](/windows/win32/api/evntrace/ns-evntrace-event_trace_properties) .</span><span class="sxs-lookup"><span data-stu-id="ef624-117">At the controller, set the following members of the [**EVENT\_TRACE\_PROPERTIES**](/windows/win32/api/evntrace/ns-evntrace-event_trace_properties) structure.</span></span>

    <span data-ttu-id="ef624-118">Задайте  для логфилемоде **\_ \_ \_ \_ режим системного журнала отслеживания событий**.</span><span class="sxs-lookup"><span data-stu-id="ef624-118">Set **LogFileMode** to **EVENT\_TRACE\_SYSTEM\_LOGGER\_MODE**.</span></span>

    <span data-ttu-id="ef624-119">Задайте для **логжернаме** закрытое средство ведения журнала **вместо \_ \_ имени средства ведения журнала ядра**.</span><span class="sxs-lookup"><span data-stu-id="ef624-119">Set **LoggerName** to private logger, instead of **KERNEL\_LOGGER\_NAME**.</span></span>

    <span data-ttu-id="ef624-120">Убедитесь, что элемент **вноде. GUID** структуры [**\_ \_ свойств трассировки событий**](/windows/win32/api/evntrace/ns-evntrace-event_trace_properties) не имеет значение **системтрацеконтролгуид**.</span><span class="sxs-lookup"><span data-stu-id="ef624-120">Make sure the **Wnode.Guid** member of the [**EVENT\_TRACE\_PROPERTIES**](/windows/win32/api/evntrace/ns-evntrace-event_trace_properties) structure is not set to **SystemTraceControlGuid**.</span></span> <span data-ttu-id="ef624-121">Для этого элемента необходимо назначить новый **идентификатор GUID** .</span><span class="sxs-lookup"><span data-stu-id="ef624-121">You must assign a new **GUID** to this member.</span></span>

-   <span data-ttu-id="ef624-122">На потребителе установите для элемента **логжернаме** структуры [**\_ \_ журнала событий трассировки**](/windows/win32/api/evntrace/ns-evntrace-event_trace_logfilea) значение этого частного средства ведения журнала.</span><span class="sxs-lookup"><span data-stu-id="ef624-122">At the consumer, set the **LoggerName** member of the [**EVENT\_TRACE\_LOGFILE**](/windows/win32/api/evntrace/ns-evntrace-event_trace_logfilea) structure to this private logger.</span></span>

> [!Note]  
> <span data-ttu-id="ef624-123">Если вы хотите, чтобы у пользователей, не являющихся администраторами, или в службе, не поддерживающей TCB, можно было запустить сеанс трассировки профилирования с помощью Системтрацепровидер от имени сторонних приложений, необходимо предоставить привилегию профиля пользователя, а затем добавить этого пользователя в **идентификатор GUID** сеанса (созданный для сеанса ведения журнала) и **идентификатор GUID** поставщика трассировки системы, чтобы включить поставщик трассировки системы.</span><span class="sxs-lookup"><span data-stu-id="ef624-123">If you want a non-administrators or a non-TCB process to be able to start a profiling trace session using the SystemTraceProvider on behalf of third party applications, then you need to grant the user profile privilege and then add this user to both the session **GUID** (created for the logger session) and the system trace provider **GUID** to enable the system trace provider.</span></span> <span data-ttu-id="ef624-124">Дополнительные сведения см. в описании функции [**евентакцессконтрол**](/windows/desktop/api/Evntcons/nf-evntcons-eventaccesscontrol) .</span><span class="sxs-lookup"><span data-stu-id="ef624-124">For more information, see the [**EventAccessControl**](/windows/desktop/api/Evntcons/nf-evntcons-eventaccesscontrol) function.</span></span>

 

## <a name="related-topics"></a><span data-ttu-id="ef624-125">Связанные темы</span><span class="sxs-lookup"><span data-stu-id="ef624-125">Related topics</span></span>

[<span data-ttu-id="ef624-126">Настройка и запуск закрытого сеанса ведения журнала</span><span class="sxs-lookup"><span data-stu-id="ef624-126">Configuring and Starting a Private Logger Session</span></span>](configuring-and-starting-a-private-logger-session.md)

[<span data-ttu-id="ef624-127">Настройка и запуск сеанса авторегистратора</span><span class="sxs-lookup"><span data-stu-id="ef624-127">Configuring and Starting an AutoLogger Session</span></span>](configuring-and-starting-an-autologger-session.md)

[<span data-ttu-id="ef624-128">Настройка и запуск сеанса трассировки событий</span><span class="sxs-lookup"><span data-stu-id="ef624-128">Configuring and Starting an Event Tracing Session</span></span>](configuring-and-starting-an-event-tracing-session.md)

[<span data-ttu-id="ef624-129">Настройка и запуск сеанса ведения журнала ядра NT</span><span class="sxs-lookup"><span data-stu-id="ef624-129">Configuring and Starting the NT Kernel Logger Session</span></span>](configuring-and-starting-the-nt-kernel-logger-session.md)

[<span data-ttu-id="ef624-130">Поставщики систем</span><span class="sxs-lookup"><span data-stu-id="ef624-130">System Providers</span></span>](system-providers.md)

[<span data-ttu-id="ef624-131">Обновление сеанса трассировки событий</span><span class="sxs-lookup"><span data-stu-id="ef624-131">Updating an Event Tracing Session</span></span>](updating-an-event-tracing-session.md)

 

 
