---
title: Определение фильтров
description: Поставщик может определять фильтры, которые сеанс использует для фильтрации событий на основе данных событий.
ms.assetid: b43912af-0e9c-414b-b3fa-03e7e35e493c
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 61dd2a21b9c4e01ebc4a32a160b24022c79197b0
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "104134442"
---
# <a name="defining-filters"></a><span data-ttu-id="14559-103">Определение фильтров</span><span class="sxs-lookup"><span data-stu-id="14559-103">Defining Filters</span></span>

<span data-ttu-id="14559-104">Поставщик может определять фильтры, которые сеанс использует для фильтрации событий на основе данных событий.</span><span class="sxs-lookup"><span data-stu-id="14559-104">A provider can define filters that a session uses to filter events based on event data.</span></span> <span data-ttu-id="14559-105">При использовании уровня и ключевых слов ETW определяет, записывается ли событие в журнал.</span><span class="sxs-lookup"><span data-stu-id="14559-105">With level and keywords, ETW determines whether the event is written to the log.</span></span> <span data-ttu-id="14559-106">Однако при использовании фильтров поставщик использует критерии фильтрации данных, которые передаются сеансом управления (см. функцию [*енаблекаллбакк*](/windows/desktop/api/evntprov/nc-evntprov-penablecallback) ), чтобы определить, записывает ли событие в этот сеанс.</span><span class="sxs-lookup"><span data-stu-id="14559-106">However, with filters, the provider uses the filter data criteria that the controlling session passes to it (see the [*EnableCallback*](/windows/desktop/api/evntprov/nc-evntprov-penablecallback) function) to determine whether it writes the event to that session.</span></span> <span data-ttu-id="14559-107">Фильтры применяются только в том случае, если сеанс трассировки ETW включает ваш поставщик.</span><span class="sxs-lookup"><span data-stu-id="14559-107">The filters are applicable only when an ETW tracing session enables your provider.</span></span>

<span data-ttu-id="14559-108">Обычно поставщики просто пишут события, а сеанс определяет типы событий, которые требуется использовать на уровне и ключевые слова.</span><span class="sxs-lookup"><span data-stu-id="14559-108">Typically, providers just write events, and the session identifies the types of events that it wants using level and keywords.</span></span> <span data-ttu-id="14559-109">Если поставщик определил фильтр данных для типа события, он может использовать его для фильтрации событий для этого типа событий на основе данных события (семантика фильтра определяется поставщиком).</span><span class="sxs-lookup"><span data-stu-id="14559-109">If the provider defined a data filter for an event type, the session could use it to filter out events for that event type based on the event data (the semantics of the filter is defined by the provider).</span></span> <span data-ttu-id="14559-110">Например, если поставщик создает события обработки, можно определить фильтр данных, который фильтрует события процесса на основе идентификатора процесса.</span><span class="sxs-lookup"><span data-stu-id="14559-110">For example, if your provider generates process events, you could define a data filter that filtered process events based on a process identifier.</span></span> <span data-ttu-id="14559-111">Затем сеанс может передать идентификатор процесса в качестве фильтра данных поставщику и получить только события обработки для этого идентификатора процесса.</span><span class="sxs-lookup"><span data-stu-id="14559-111">The session could then pass a process identifier as filter data to the provider and receive only process events for that process identifier.</span></span>

<span data-ttu-id="14559-112">В следующем примере показано, как использовать элемент **Filter** для определения фильтра.</span><span class="sxs-lookup"><span data-stu-id="14559-112">The following example shows how to use the **filter** element to define a filter.</span></span> <span data-ttu-id="14559-113">Необходимо указать атрибуты **имени** и **значения** фильтра; другие атрибуты являются необязательными.</span><span class="sxs-lookup"><span data-stu-id="14559-113">You must specify the filter's **name** and **value** attributes; the other attributes are optional.</span></span> <span data-ttu-id="14559-114">Атрибут **tid** является обязательным, если фильтр требует, чтобы сеанс продавал данные фильтра.</span><span class="sxs-lookup"><span data-stu-id="14559-114">The **tid** attribute is required if the filter requires that the session pass filter data.</span></span>


```XML
<instrumentationManifest
    xmlns="http://schemas.microsoft.com/win/2004/08/events" 
    xmlns:win="http://manifests.microsoft.com/win/2004/08/windows/events"
    xmlns:xs="http://www.w3.org/2001/XMLSchema"
    >

    <instrumentation>
        <events>
            <provider name="Microsoft-Windows-SampleProvider"
                guid="{1db28f2e-8f80-4027-8c5a-a11f7f10f62d}"
                symbol="PROVIDER_GUID"
                resourceFileName="<path to the exe or dll that contains the metadata resources>"
                messageFileName="<path to the exe or dll that contains the string resources>"
                message="$(string.Provider.Name)">

                . . .

                <filters>
                    <filter name="Pid"
                            value="1"
                            tid="t1"
                            symbol="FILTER_PID"/>
                </filters>

                <templates>
                    <template tid="t1">
                        <data name="Pid" inType="win:UInt32"/>
                    </template>
                </templates>

                . . .

            </provider>
        </events>
    </instrumentation>

    <localization>
        <resources culture="en-US">
            <stringTable>
                <string id="Provider.Name" value="Sample Provider"/>
            </stringTable>
        </resources>
    </localization>

</instrumentationManifest>
```