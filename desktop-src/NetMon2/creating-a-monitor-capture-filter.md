---
description: Создание фильтра записи, работающего с сетевой монитор, является пять-шаговым процессом.
ms.assetid: 04be791c-43c5-44c2-8ab0-799a99974bf6
title: Создание фильтра записи монитора
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 097a8276bd6a1f311b343787b3f06175d9b7091f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "105673641"
---
# <a name="creating-a-monitor-capture-filter"></a><span data-ttu-id="1d37e-103">Создание фильтра записи монитора</span><span class="sxs-lookup"><span data-stu-id="1d37e-103">Creating a Monitor Capture Filter</span></span>

<span data-ttu-id="1d37e-104">Создание фильтра записи, который работает с сетевой монитор, состоит из пяти шагов:</span><span class="sxs-lookup"><span data-stu-id="1d37e-104">Creating a capture filter that works with Network Monitor is a five-step process:</span></span>

-   [<span data-ttu-id="1d37e-105">Настройка ETYPE или SAP Filter</span><span class="sxs-lookup"><span data-stu-id="1d37e-105">Setting the Etype or SAP Filter</span></span>](writing-etypesap-filter-portion.md)
-   [<span data-ttu-id="1d37e-106">Идет запись фильтра АДДРЕССТАБЛЕ</span><span class="sxs-lookup"><span data-stu-id="1d37e-106">Writing ADDRESSTABLE Filter</span></span>](writing-addresstable-filter-portion.md)
-   [<span data-ttu-id="1d37e-107">Написание фильтра ПАТТЕРНМАТЧ</span><span class="sxs-lookup"><span data-stu-id="1d37e-107">Writing the PATTERNMATCH Filter</span></span>](writing-the-patternmatch-filter.md)
-   [<span data-ttu-id="1d37e-108">Обрезка рамки</span><span class="sxs-lookup"><span data-stu-id="1d37e-108">Clipping a Frame</span></span>](clipping-a-frame.md)
-   [<span data-ttu-id="1d37e-109">Реализация кода фильтра записи</span><span class="sxs-lookup"><span data-stu-id="1d37e-109">Implementing the Capture Filter Code</span></span>](implementing-the-capture-filter-code.md)

<span data-ttu-id="1d37e-110">[*Фильтр записи*](c.md) — это ряд дополнений к большому двоичному объекту НПП, который выбирает, какие кадры передаются обратно на монитор.</span><span class="sxs-lookup"><span data-stu-id="1d37e-110">A [*capture filter*](c.md) is a series of additions to the NPP BLOB that selects which frames are passed back to the monitor.</span></span> <span data-ttu-id="1d37e-111">Если монитор не изменяет большой двоичный объект НПП, НПП перейдет в неизбирательный режим и отправит весь сетевой трафик монитору.</span><span class="sxs-lookup"><span data-stu-id="1d37e-111">If a monitor does not alter the NPP BLOB, then the NPP will go into promiscuous mode and send all network traffic to the monitor.</span></span> <span data-ttu-id="1d37e-112">НПП наиболее эффективен, если может сократить объем данных, передаваемых в драйвер, поэтому монитор должен создать фильтр записи.</span><span class="sxs-lookup"><span data-stu-id="1d37e-112">The NPP is most efficient if it can reduce the data handed up to a driver, so a monitor should create a capture filter.</span></span> <span data-ttu-id="1d37e-113">Монитор задает фильтр записи, записывая в большой двоичный объект НПП в вызове функции [доконфигуре](imonitor-doconfigure.md) .</span><span class="sxs-lookup"><span data-stu-id="1d37e-113">A monitor sets its capture filter by writing to the NPP BLOB in the call to the [DoConfigure](imonitor-doconfigure.md) function.</span></span> <span data-ttu-id="1d37e-114">Затем МКСВК вызывает НПП с большим двоичным объектом НПП.</span><span class="sxs-lookup"><span data-stu-id="1d37e-114">The MCSVC then calls the NPP with the NPP BLOB.</span></span> <span data-ttu-id="1d37e-115">Дополнительные сведения о фильтре записи, [поставщиках сетевых пакетов](network-packet-providers.md) в нппс и [сетевой монитор больших двоичных](network-monitor-blobs.md) объектах в функциях BLOB-объектов см. в разделе [фильтры записи](capture-filters.md) .</span><span class="sxs-lookup"><span data-stu-id="1d37e-115">See [Capture Filters](capture-filters.md) for more details on the capture filter, [Network Packet Providers](network-packet-providers.md) on NPPs, and [Network Monitor Blobs](network-monitor-blobs.md) on BLOB functions.</span></span>

 

 



