---
description: Запросы событий используются временными потребителями событий, событиями постоянных потребителей и поставщиками событий. Потребители событий используют запросы событий для указания интересующих событий, а поставщики событий используют запросы для указания предоставляемых ими событий.
ms.assetid: 851ad9bd-2604-4988-8de0-8d29b5300b21
ms.tgt_platform: multiple
title: Получение уведомлений о событиях
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 43873c03155f2186f9d3a9a3daff9b8e322e511f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "105647260"
---
# <a name="receiving-event-notifications"></a><span data-ttu-id="47c6d-104">Получение уведомлений о событиях</span><span class="sxs-lookup"><span data-stu-id="47c6d-104">Receiving Event Notifications</span></span>

<span data-ttu-id="47c6d-105">Запросы событий используются временными потребителями событий, событиями постоянных потребителей и поставщиками событий.</span><span class="sxs-lookup"><span data-stu-id="47c6d-105">Event queries are used by temporary event consumers, permanent event consumers, and event providers.</span></span> <span data-ttu-id="47c6d-106">Потребители событий используют запросы событий для указания интересующих событий, а поставщики событий используют запросы для указания предоставляемых ими событий.</span><span class="sxs-lookup"><span data-stu-id="47c6d-106">Event consumers use event queries to specify events of interest, and event providers use the queries to specify the events that they provide.</span></span>

<span data-ttu-id="47c6d-107">[Временные потребители](receiving-events-for-the-duration-of-your-application.md) размещают запросы в вызовах метода [**IWbemServices:: ексекнотификатионкуери**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-execnotificationquery) или [**IWbemServices:: ExecNotificationQueryAsync**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-execnotificationqueryasync) .</span><span class="sxs-lookup"><span data-stu-id="47c6d-107">[Temporary consumers](receiving-events-for-the-duration-of-your-application.md) place queries in calls to the [**IWbemServices::ExecNotificationQuery**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-execnotificationquery) or [**IWbemServices::ExecNotificationQueryAsync**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-execnotificationqueryasync) method.</span></span> <span data-ttu-id="47c6d-108">[Постоянные потребители событий](receiving-events-at-all-times.md) размещают запросы в свойстве **Query** экземпляра класса System [**\_ \_ EventFilter**](--eventfilter.md) .</span><span class="sxs-lookup"><span data-stu-id="47c6d-108">[Permanent event consumers](receiving-events-at-all-times.md) place queries in the **Query** property of an instance of the [**\_\_EventFilter**](--eventfilter.md) system class.</span></span>

<span data-ttu-id="47c6d-109">[Поставщики событий](writing-an-event-provider.md) используют запросы событий для регистрации для поддержки одного или нескольких типов событий.</span><span class="sxs-lookup"><span data-stu-id="47c6d-109">[Event providers](writing-an-event-provider.md) use event queries to register to support one or more types of events.</span></span> <span data-ttu-id="47c6d-110">Они размещают запросы в свойстве **евенткуерилист** экземпляра класса System [**\_ \_ евентпровидеррегистратион**](--eventproviderregistration.md) .</span><span class="sxs-lookup"><span data-stu-id="47c6d-110">They place queries in the **EventQueryList** property of an instance of the [**\_\_EventProviderRegistration**](--eventproviderregistration.md) system class.</span></span> <span data-ttu-id="47c6d-111">Все поставщики событий создают экземпляр **\_ \_ евентпровидеррегистратион** для регистрации в инструментарий управления Windows (WMI) (WMI).</span><span class="sxs-lookup"><span data-stu-id="47c6d-111">All event providers create an **\_\_EventProviderRegistration** instance to register with Windows Management Instrumentation (WMI).</span></span> <span data-ttu-id="47c6d-112">Дополнительные сведения см. в разделе [Регистрация поставщика событий](registering-an-event-provider.md).</span><span class="sxs-lookup"><span data-stu-id="47c6d-112">For more information, see [Registering an Event Provider](registering-an-event-provider.md).</span></span>

<span data-ttu-id="47c6d-113">Потребители и поставщики событий используют [инструкцию SELECT](select-statement-for-event-queries.md) и связанное предложение WHERE для запросов событий, а также разнообразные расширения, специфичные для язык запросов WMI (WQL).</span><span class="sxs-lookup"><span data-stu-id="47c6d-113">Event consumers and providers use the [SELECT statement](select-statement-for-event-queries.md) and a related WHERE clause for event queries, plus a variety of extensions specific to the WMI Query Language (WQL).</span></span> <span data-ttu-id="47c6d-114">Расширения используются для защиты пользователей от перегрузки с помощью уведомлений, которые часто являются полезными.</span><span class="sxs-lookup"><span data-stu-id="47c6d-114">The extensions are used to protect consumers from being flooded with notifications that occur too frequently to be useful.</span></span>

<span data-ttu-id="47c6d-115">Потребители, не требующие уведомления каждый раз, когда происходит событие, могут указать следующие предложения в своих запросах:</span><span class="sxs-lookup"><span data-stu-id="47c6d-115">Consumers that do not require notification each time an event occurs can specify the following clauses in their queries:</span></span>

-   <span data-ttu-id="47c6d-116">[Внутри](within-clause.md) предложения</span><span class="sxs-lookup"><span data-stu-id="47c6d-116">[WITHIN](within-clause.md) clause</span></span>
-   <span data-ttu-id="47c6d-117">[Group, предложение](group-clause.md)</span><span class="sxs-lookup"><span data-stu-id="47c6d-117">[GROUP](group-clause.md) clause</span></span>
-   <span data-ttu-id="47c6d-118">[HAVING](having-clause.md) , предложение</span><span class="sxs-lookup"><span data-stu-id="47c6d-118">[HAVING](having-clause.md) clause</span></span>

<span data-ttu-id="47c6d-119">Предложения внутри и HAVING влияют на время событий, а предложение GROUP вызывает отправку репрезентативного события вместо часто возникающего события.</span><span class="sxs-lookup"><span data-stu-id="47c6d-119">The WITHIN and HAVING clauses affect the timing of events, and the GROUP clause causes a representative event to be sent in place of a frequently occurring event.</span></span>

 

 



