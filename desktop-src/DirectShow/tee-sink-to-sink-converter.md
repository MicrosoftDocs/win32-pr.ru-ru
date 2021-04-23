---
description: Преобразователь tee/Sink-to-Sink
ms.assetid: 8ee5e20c-f37a-4a9b-9382-2ed94333c6ec
title: Преобразователь tee/Sink-to-Sink
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9cf85e3eb58f601273ff352a3878d352ca0f0d5a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "105674163"
---
# <a name="teesink-to-sink-converter"></a><span data-ttu-id="678c3-103">Преобразователь tee/Sink-to-Sink</span><span class="sxs-lookup"><span data-stu-id="678c3-103">Tee/Sink-to-Sink Converter</span></span>

<span data-ttu-id="678c3-104">Преобразователь tee/Sink-to-Sink — это фильтр на основе Кспрокси в режиме ядра.</span><span class="sxs-lookup"><span data-stu-id="678c3-104">The Tee/Sink-to-Sink Converter is a kernel-mode, KsProxy-based filter.</span></span> <span data-ttu-id="678c3-105">Он используется в аналоговых графах фильтра видео, где данные ВБИ подготавливаются к просмотру или записи.</span><span class="sxs-lookup"><span data-stu-id="678c3-105">It is used in analog video television filter graphs where VBI data is being rendered or captured.</span></span> <span data-ttu-id="678c3-106">Фильтр подключен к [фильтру записи видео WDM](wdm-video-capture-filter.md) и предоставляет эффективные средства для дублирования потоков данных в режиме ядра без дорогостоящих переходов между режимами ядра и пользователя.</span><span class="sxs-lookup"><span data-stu-id="678c3-106">The filter is connected upstream to the [WDM Video Capture Filter](wdm-video-capture-filter.md) and provides an efficient means to duplicate streams of data within kernel mode without the expensive transitions between kernel and user mode.</span></span> <span data-ttu-id="678c3-107">Он доставляет каждый полученный блок данных во все выходные сигналы, а нисходящий кодек отвечает за поиск конкретных ВБИ данных для декодирования.</span><span class="sxs-lookup"><span data-stu-id="678c3-107">It delivers each received data block to all output pins, and the downstream codec is responsible for finding the specific VBI data to decode.</span></span>

<span data-ttu-id="678c3-108">Преобразователь tee/Sink-to-Sink отображается в категории фильтра "WDM Streaming tee/Splitter Devices" ( \_ \_ Разделитель кскатегори).</span><span class="sxs-lookup"><span data-stu-id="678c3-108">The Tee/Sink-to-Sink Converter appears in the "WDM Streaming Tee/Splitter Devices" filter category (AM\_KSCATEGORY\_SPLITTER).</span></span>

<span data-ttu-id="678c3-109">Так как это фильтр режима ядра, приложения не могут создать его напрямую с помощью [**CoCreateInstance**](/windows/win32/api/combaseapi/nf-combaseapi-cocreateinstance).</span><span class="sxs-lookup"><span data-stu-id="678c3-109">Because this is a kernel-mode filter, applications cannot create it directly using [**CoCreateInstance**](/windows/win32/api/combaseapi/nf-combaseapi-cocreateinstance).</span></span> <span data-ttu-id="678c3-110">Вместо этого используйте [перечислитель системных устройств](system-device-enumerator.md).</span><span class="sxs-lookup"><span data-stu-id="678c3-110">Instead, use the [System Device Enumerator](system-device-enumerator.md).</span></span> <span data-ttu-id="678c3-111">Дополнительные сведения см. в разделе [Создание фильтров Kernel-Mode](creating-kernel-mode-filters.md).</span><span class="sxs-lookup"><span data-stu-id="678c3-111">For more information, see [Creating Kernel-Mode Filters](creating-kernel-mode-filters.md).</span></span>

## <a name="related-topics"></a><span data-ttu-id="678c3-112">См. также</span><span class="sxs-lookup"><span data-stu-id="678c3-112">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="678c3-113">Фильтры DirectShow</span><span class="sxs-lookup"><span data-stu-id="678c3-113">DirectShow Filters</span></span>](directshow-filters.md)
</dt> </dl>

 

 
