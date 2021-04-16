---
description: Фильтр записи — это элемент приложения НПП, который указывает драйверу сетевой монитор (Nmnt.sys), какие кадры сетевых данных должны храниться и какие кадры игнорировать.
ms.assetid: 6ab17e18-bd97-42a8-b569-b205ac19ffd1
title: О фильтрах записи
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7226bb7dc5bc214ab2e09504cc232e1bf591840f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "105663034"
---
# <a name="about-capture-filters"></a><span data-ttu-id="6b83f-103">О фильтрах записи</span><span class="sxs-lookup"><span data-stu-id="6b83f-103">About Capture Filters</span></span>

<span data-ttu-id="6b83f-104">Фильтр записи — это элемент приложения НПП, который указывает драйверу сетевой монитор (Nmnt.sys), какие кадры сетевых данных должны храниться и какие кадры игнорировать.</span><span class="sxs-lookup"><span data-stu-id="6b83f-104">A capture filter is an element of an NPP application that instructs the Network Monitor driver (Nmnt.sys) which frames of network data to retain and which frames to ignore.</span></span> <span data-ttu-id="6b83f-105">Преимущество настройки фильтра записи более эффективно.</span><span class="sxs-lookup"><span data-stu-id="6b83f-105">The advantage of setting a capture filter is greater efficiency.</span></span> <span data-ttu-id="6b83f-106">Не нужно изучать захваченные кадры; драйвер сетевой монитор изучает их.</span><span class="sxs-lookup"><span data-stu-id="6b83f-106">You do not have to examine captured frames; the Network Monitor driver examines them.</span></span> <span data-ttu-id="6b83f-107">Этот подход исключает копирование кадров, что обеспечивает преимущество использования памяти.</span><span class="sxs-lookup"><span data-stu-id="6b83f-107">This approach eliminates frame copying, which provides a memory use advantage.</span></span>

## <a name="capture-filter-structure"></a><span data-ttu-id="6b83f-108">Структура фильтра записи</span><span class="sxs-lookup"><span data-stu-id="6b83f-108">Capture Filter Structure</span></span>

<span data-ttu-id="6b83f-109">Фильтры записи состоят из трех элементов:</span><span class="sxs-lookup"><span data-stu-id="6b83f-109">Capture filters consist of three elements:</span></span>

-   <span data-ttu-id="6b83f-110">Параметры ETYPE/SAP</span><span class="sxs-lookup"><span data-stu-id="6b83f-110">Etype/SAP settings</span></span>
-   <span data-ttu-id="6b83f-111">Адрес</span><span class="sxs-lookup"><span data-stu-id="6b83f-111">Address</span></span>
-   <span data-ttu-id="6b83f-112">Соответствие шаблону</span><span class="sxs-lookup"><span data-stu-id="6b83f-112">Pattern match</span></span>

<span data-ttu-id="6b83f-113">Вместе эти элементы логически оценивают, какие кадры включить или исключить, во время работы приложения НПП.</span><span class="sxs-lookup"><span data-stu-id="6b83f-113">Together, these elements logically evaluate which frames to include, or exclude, during the operation of an NPP application.</span></span> <span data-ttu-id="6b83f-114">Фильтр записи предоставляет комплексные совпадения и исключения элементов Frame в приложение НПП.</span><span class="sxs-lookup"><span data-stu-id="6b83f-114">The capture filter supplies complex matches and exclusions of frame elements to the NPP application.</span></span>

<span data-ttu-id="6b83f-115">Сетевой монитор реализует фильтр записи через структуру данных, [**каптурефилтер**](the-capturefilter-structure.md), передается в НПП, а затем передается драйверу сетевой монитор при запуске записи.</span><span class="sxs-lookup"><span data-stu-id="6b83f-115">Network Monitor implements the capture filter through a data structure, [**CAPTUREFILTER**](the-capturefilter-structure.md), passed to the NPP and then passed on to the Network Monitor driver when the capture starts.</span></span>

<span data-ttu-id="6b83f-116">Дополнительные сведения об операциях НПП и больших двоичных объектов см. в разделе [поставщики сетевых пакетов](network-packet-providers.md) и [сетевой монитор большие двоичные объекты](network-monitor-blobs.md).</span><span class="sxs-lookup"><span data-stu-id="6b83f-116">For more information about NPP operations and BLOB functionality, see [Network Packet Providers](network-packet-providers.md) and [Network Monitor BLOBS](network-monitor-blobs.md).</span></span>

 

 



