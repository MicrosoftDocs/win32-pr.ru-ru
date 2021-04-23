---
description: Системтрацепровидер — это поставщик ядра с предопределенным набором событий ядра, поддерживаемых в Windows 7, Windows Server 2008 R2 и более поздних версиях.
ms.assetid: 6808EC45-C8C3-45D7-9E4C-337F6A4CF9C8
title: Настройка и запуск сеанса Системтрацепровидер
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b718269801a7677572e7bb5b74cd8b89d3711e3e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104984516"
---
# <a name="configuring-and-starting-a-systemtraceprovider-session"></a><span data-ttu-id="e0c42-103">Настройка и запуск сеанса Системтрацепровидер</span><span class="sxs-lookup"><span data-stu-id="e0c42-103">Configuring and Starting a SystemTraceProvider Session</span></span>

<span data-ttu-id="e0c42-104">Системтрацепровидер — это поставщик ядра с предопределенным набором событий ядра, поддерживаемых в Windows 7, Windows Server 2008 R2 и более поздних версиях.</span><span class="sxs-lookup"><span data-stu-id="e0c42-104">The SystemTraceProvider is a kernel provider with a predefined sets of kernel events supported on Windows 7, Windows Server 2008 R2, and later.</span></span> <span data-ttu-id="e0c42-105">В Windows 7 и Windows Server 2008 R2 Системтрацепровидер можно было использовать только для сеанса ведения журнала ядра NT.</span><span class="sxs-lookup"><span data-stu-id="e0c42-105">On Windows 7 and Windows Server 2008 R2, the SystemTraceProvider could only be used for the NT Kernel Logger session.</span></span>

<span data-ttu-id="e0c42-106">В Windows 8, Windows Server 2012 и более поздних версий Системтрацепровидер можно мультиплексировать до восьми сеансов ведения журнала.</span><span class="sxs-lookup"><span data-stu-id="e0c42-106">On Windows 8, Windows Server 2012, and later, the SystemTraceProvider can be multiplexed for up to 8 logger sessions.</span></span> <span data-ttu-id="e0c42-107">Первые два слота для сеансов ведения журнала зарезервированы для журнала ядра NT и циклического средства ведения журнала контекста ядра.</span><span class="sxs-lookup"><span data-stu-id="e0c42-107">The first two slots for logger sessions are reserved for the NT Kernel Logger and the Circular Kernel Context Logger .</span></span>

<span data-ttu-id="e0c42-108">Дополнительные сведения об использовании сеанса ведения журнала ядра NT в качестве поставщика трассировки см. в разделе [Настройка и запуск сеанса ведения журнала ядра NT](configuring-and-starting-the-nt-kernel-logger-session.md).</span><span class="sxs-lookup"><span data-stu-id="e0c42-108">For more information on using the NT Kernel Logger session as a trace provider, see [Configuring and Starting the NT Kernel Logger Session](configuring-and-starting-the-nt-kernel-logger-session.md).</span></span>

<span data-ttu-id="e0c42-109">Чтобы разрешить Системтрацепровидер запуск сеанса, отличного от средства ведения журнала ядра NT, выполните следующую команду.</span><span class="sxs-lookup"><span data-stu-id="e0c42-109">To enable the SystemTraceProvider to start a session other than the NT Kernel Logger, execute the following command.</span></span>

<span data-ttu-id="e0c42-110">**tracelog-Start MySession-f c: \\ Kernel1. ETL-ЕФЛАГ proc \_ Thread + Loader + ксвитч**</span><span class="sxs-lookup"><span data-stu-id="e0c42-110">**tracelog -start MySession -f c:\\Kernel1.etl -eflag PROC\_THREAD+LOADER+CSWITCH**</span></span>

<span data-ttu-id="e0c42-111">Чтобы программно включить Системтрацепровидер для запуска сеанса, отличного от средства ведения журнала ядра NT, выполните следующие действия.</span><span class="sxs-lookup"><span data-stu-id="e0c42-111">To programmatically enable the SystemTraceProvider to start a session other than the NT Kernel Logger, use the following steps.</span></span>

-   <span data-ttu-id="e0c42-112">Определите имя частного средства ведения журнала.</span><span class="sxs-lookup"><span data-stu-id="e0c42-112">Define a private logger name.</span></span>

    <span data-ttu-id="e0c42-113">**\#Определение частного \_ имени регистратора \_ L "некоторые частные сеансы трассировки"**</span><span class="sxs-lookup"><span data-stu-id="e0c42-113">**\#define PRIVATE\_LOGGER\_NAME L”Some Private Trace Session”**</span></span>

-   <span data-ttu-id="e0c42-114">На контроллере установите следующие элементы структуры [**\_ \_ свойств трассировки событий**](/windows/win32/api/evntrace/ns-evntrace-event_trace_properties) .</span><span class="sxs-lookup"><span data-stu-id="e0c42-114">At the controller, set the following members of the [**EVENT\_TRACE\_PROPERTIES**](/windows/win32/api/evntrace/ns-evntrace-event_trace_properties) structure.</span></span>

    <span data-ttu-id="e0c42-115">Задайте  для логфилемоде **\_ \_ \_ \_ режим системного журнала отслеживания событий**.</span><span class="sxs-lookup"><span data-stu-id="e0c42-115">Set **LogFileMode** to **EVENT\_TRACE\_SYSTEM\_LOGGER\_MODE**.</span></span>

    <span data-ttu-id="e0c42-116">Задайте для **логжернаме** закрытое средство ведения журнала **вместо \_ \_ имени средства ведения журнала ядра**.</span><span class="sxs-lookup"><span data-stu-id="e0c42-116">Set **LoggerName** to private logger, instead of **KERNEL\_LOGGER\_NAME**.</span></span>

    <span data-ttu-id="e0c42-117">Убедитесь, что элемент **вноде. GUID** структуры [**\_ \_ свойств трассировки событий**](/windows/win32/api/evntrace/ns-evntrace-event_trace_properties) не имеет значение **системтрацеконтролгуид**.</span><span class="sxs-lookup"><span data-stu-id="e0c42-117">Make sure the **Wnode.Guid** member of the [**EVENT\_TRACE\_PROPERTIES**](/windows/win32/api/evntrace/ns-evntrace-event_trace_properties) structure is not set to **SystemTraceControlGuid**.</span></span> <span data-ttu-id="e0c42-118">Для этого элемента необходимо назначить новый **идентификатор GUID** .</span><span class="sxs-lookup"><span data-stu-id="e0c42-118">You must assign a new **GUID** to this member.</span></span>

-   <span data-ttu-id="e0c42-119">На потребителе установите для элемента **логжернаме** структуры [**\_ \_ журнала событий трассировки**](/windows/win32/api/evntrace/ns-evntrace-event_trace_logfilea) значение этого частного средства ведения журнала.</span><span class="sxs-lookup"><span data-stu-id="e0c42-119">At the consumer, set the **LoggerName** member of the [**EVENT\_TRACE\_LOGFILE**](/windows/win32/api/evntrace/ns-evntrace-event_trace_logfilea) structure to this private logger.</span></span>

> [!Note]  
> <span data-ttu-id="e0c42-120">Если вы хотите, чтобы у пользователей, не являющихся администраторами, или в службе, не поддерживающей TCB, можно было запустить сеанс трассировки профилирования с помощью Системтрацепровидер от имени сторонних приложений, необходимо предоставить привилегию профиля пользователя, а затем добавить этого пользователя в **идентификатор GUID** сеанса (созданный для сеанса ведения журнала) и **идентификатор GUID** поставщика трассировки системы, чтобы включить поставщик трассировки системы.</span><span class="sxs-lookup"><span data-stu-id="e0c42-120">If you want a non-administrators or a non-TCB process to be able to start a profiling trace session using the SystemTraceProvider on behalf of third party applications, then you need to grant the user profile privilege and then add this user to both the session **GUID** (created for the logger session) and the system trace provider **GUID** to enable the system trace provider.</span></span> <span data-ttu-id="e0c42-121">Дополнительные сведения см. в описании функции [**евентакцессконтрол**](/windows/desktop/api/Evntcons/nf-evntcons-eventaccesscontrol) .</span><span class="sxs-lookup"><span data-stu-id="e0c42-121">For more information, see the [**EventAccessControl**](/windows/desktop/api/Evntcons/nf-evntcons-eventaccesscontrol) function.</span></span>

 

## <a name="related-topics"></a><span data-ttu-id="e0c42-122">См. также</span><span class="sxs-lookup"><span data-stu-id="e0c42-122">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="e0c42-123">Настройка и запуск закрытого сеанса ведения журнала</span><span class="sxs-lookup"><span data-stu-id="e0c42-123">Configuring and Starting a Private Logger Session</span></span>](configuring-and-starting-a-private-logger-session.md)
</dt> <dt>

[<span data-ttu-id="e0c42-124">Настройка и запуск сеанса авторегистратора</span><span class="sxs-lookup"><span data-stu-id="e0c42-124">Configuring and Starting an AutoLogger Session</span></span>](configuring-and-starting-an-autologger-session.md)
</dt> <dt>

[<span data-ttu-id="e0c42-125">Настройка и запуск сеанса трассировки событий</span><span class="sxs-lookup"><span data-stu-id="e0c42-125">Configuring and Starting an Event Tracing Session</span></span>](configuring-and-starting-an-event-tracing-session.md)
</dt> <dt>

[<span data-ttu-id="e0c42-126">Настройка и запуск сеанса ведения журнала ядра NT</span><span class="sxs-lookup"><span data-stu-id="e0c42-126">Configuring and Starting the NT Kernel Logger Session</span></span>](configuring-and-starting-the-nt-kernel-logger-session.md)
</dt> <dt>

[<span data-ttu-id="e0c42-127">Обновление сеанса трассировки событий</span><span class="sxs-lookup"><span data-stu-id="e0c42-127">Updating an Event Tracing Session</span></span>](updating-an-event-tracing-session.md)
</dt> </dl>

 

 
