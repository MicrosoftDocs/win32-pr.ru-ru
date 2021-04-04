---
description: Инструментарий WMI предоставляет набор классов для устранения неполадок, которые сценарии и приложения могут использовать для получения сведений о внутреннем состоянии WMI во время операций WMI Core и provider.
ms.assetid: 631e0cce-0e83-42e5-a381-e96b1f70d6f9
ms.tgt_platform: multiple
title: Классы устранения неполадок WMI
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 65b3972ba59c80a1495916ab24a72f6e93bef8e6
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "103999555"
---
# <a name="wmi-troubleshooting-classes"></a><span data-ttu-id="df027-103">Классы устранения неполадок WMI</span><span class="sxs-lookup"><span data-stu-id="df027-103">WMI Troubleshooting Classes</span></span>

<span data-ttu-id="df027-104">Инструментарий WMI предоставляет набор классов для устранения неполадок, которые сценарии и приложения могут использовать для получения сведений о внутреннем состоянии WMI во время операций WMI Core и provider.</span><span class="sxs-lookup"><span data-stu-id="df027-104">WMI supplies a set of troubleshooting classes that scripts and applications can use to get information about WMI internal state during WMI core and provider operations.</span></span> <span data-ttu-id="df027-105">Дополнительные сведения об устранении неполадок WMI см. в разделе [Устранение неполадок WMI](wmi-troubleshooting.md) и [Настройка поставщика и устранение неполадок](provider-configuration-and-troubleshooting-classes.md).</span><span class="sxs-lookup"><span data-stu-id="df027-105">For more information about WMI troubleshooting, see [WMI Troubleshooting](wmi-troubleshooting.md) and [Provider Configuration and Troubleshooting Classes](provider-configuration-and-troubleshooting-classes.md).</span></span>

<span data-ttu-id="df027-106">Инструментарий WMI имеет несколько основных классов устранения неполадок для WMI Core и операций поставщика:</span><span class="sxs-lookup"><span data-stu-id="df027-106">WMI has several basic troubleshooting classes for WMI core and provider operations:</span></span>

-   [<span data-ttu-id="df027-107">**\_ \_ Счетчики MSFT события**</span><span class="sxs-lookup"><span data-stu-id="df027-107">**MSFT\_WmiProvider\_Counters**</span></span>](/previous-versions/windows/desktop/wmisystemprov/msft-wmiprovider-counters)

    <span data-ttu-id="df027-108">На каждой системе компьютера обнаружен только один из этих классов.</span><span class="sxs-lookup"><span data-stu-id="df027-108">Only one of these classes is found on each computer system.</span></span> <span data-ttu-id="df027-109">Он предоставляет счетчики различных операций поставщика в этой системе.</span><span class="sxs-lookup"><span data-stu-id="df027-109">It provides counts of various kind of provider operations on that system.</span></span>

-   [<span data-ttu-id="df027-110">**MSFT \_ вмиселфевент**</span><span class="sxs-lookup"><span data-stu-id="df027-110">**MSFT\_WmiSelfEvent**</span></span>](/previous-versions/windows/desktop/wmisystemprov/msft-wmiselfevent)

    <span data-ttu-id="df027-111">Классы устранения неполадок событий являются производными от [**MSFT \_ вмиселфевент**](/previous-versions/windows/desktop/wmisystemprov/msft-wmiselfevent).</span><span class="sxs-lookup"><span data-stu-id="df027-111">The event troubleshooting classes derive from [**MSFT\_WmiSelfEvent**](/previous-versions/windows/desktop/wmisystemprov/msft-wmiselfevent).</span></span> <span data-ttu-id="df027-112">Запросы этого класса возвращают экземпляры классов событий, таких как [**MSFT \_ Вмисреадпулкреатед**](/previous-versions/windows/desktop/wmisystemprov/msft-wmithreadpoolcreated) или [**MSFT \_ события \_ креатеинстанцеенумасинцевент \_ POST**](/previous-versions/windows/desktop/wmisystemprov/msft-wmiprovider-createinstanceenumasyncevent-post).</span><span class="sxs-lookup"><span data-stu-id="df027-112">Queries of this class return instances of event classes such as [**MSFT\_WmiThreadPoolCreated**](/previous-versions/windows/desktop/wmisystemprov/msft-wmithreadpoolcreated) or [**MSFT\_WmiProvider\_CreateInstanceEnumAsyncEvent\_Post**](/previous-versions/windows/desktop/wmisystemprov/msft-wmiprovider-createinstanceenumasyncevent-post).</span></span>

    <span data-ttu-id="df027-113">В следующем списке приведены ссылки на различные категории классов событий, производных от [**MSFT \_ вмиселфевент**](/previous-versions/windows/desktop/wmisystemprov/msft-wmiselfevent):</span><span class="sxs-lookup"><span data-stu-id="df027-113">The following list provides links to different categories of event classes derived from [**MSFT\_WmiSelfEvent**](/previous-versions/windows/desktop/wmisystemprov/msft-wmiselfevent):</span></span>

    -   [<span data-ttu-id="df027-114">Классы устранения неполадок событий поставщика</span><span class="sxs-lookup"><span data-stu-id="df027-114">Provider Event Troubleshooting Classes</span></span>](provider-event-troubleshooting-classes.md)
    -   [<span data-ttu-id="df027-115">Классы устранения неполадок Консумерпровидер</span><span class="sxs-lookup"><span data-stu-id="df027-115">ConsumerProvider Troubleshooting Classes</span></span>](consumerprovider-troubleshooting-classes.md)
    -   [<span data-ttu-id="df027-116">Классы устранения неполадок событий службы WMI</span><span class="sxs-lookup"><span data-stu-id="df027-116">WMI Service Event Troubleshooting Classes</span></span>](wmi-service-event-troubleshooting-classes.md)

## <a name="related-topics"></a><span data-ttu-id="df027-117">См. также</span><span class="sxs-lookup"><span data-stu-id="df027-117">Related topics</span></span>

<dl> <dt>

<span data-ttu-id="df027-118">[Устранение неполадок WMI](wmi-troubleshooting.md).</span><span class="sxs-lookup"><span data-stu-id="df027-118">[WMI Troubleshooting](wmi-troubleshooting.md)</span></span>
</dt> <dt>

[<span data-ttu-id="df027-119">Получение события WMI</span><span class="sxs-lookup"><span data-stu-id="df027-119">Receiving a WMI Event</span></span>](receiving-a-wmi-event.md)
</dt> </dl>

 

 
