---
description: Фильтр кодека WST
ms.assetid: 0a06acbf-b842-4ab6-bcf9-d2d006301d83
title: Фильтр кодека WST
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 338db987986a5f4706c144907d122eec3a0615a9
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "104349795"
---
# <a name="wst-codec-filter"></a><span data-ttu-id="f2f14-103">Фильтр кодека WST</span><span class="sxs-lookup"><span data-stu-id="f2f14-103">WST Codec Filter</span></span>

> [!IMPORTANT]
> <span data-ttu-id="f2f14-104">Этот компонент был удален из Windows Vista и более поздних операционных систем.</span><span class="sxs-lookup"><span data-stu-id="f2f14-104">This component has been removed from Windows Vista and later operating systems.</span></span> <span data-ttu-id="f2f14-105">Он доступен для использования в операционных системах Microsoft Windows 2000, Windows XP и Windows Server 2003.</span><span class="sxs-lookup"><span data-stu-id="f2f14-105">It is available for use in the Microsoft Windows 2000, Windows XP, and Windows Server 2003 operating systems.</span></span>

 

<span data-ttu-id="f2f14-106">Начиная с Windows Vista этот фильтр заменяется фильтром Вбикодек, который описан в документации по технологиям Microsoft TV.</span><span class="sxs-lookup"><span data-stu-id="f2f14-106">Starting in Windows Vista, this filter is replaced by the VBICodec filter, which is documented in the Microsoft TV Technologies documentation.</span></span>

<span data-ttu-id="f2f14-107">Стандартный телетекст (WST) — это Европейский стандарт для передачи данных с помощью ВБИ для аналоговых телевизионных сигналов PAL.</span><span class="sxs-lookup"><span data-stu-id="f2f14-107">World Standard Teletext (WST) is the European standard for data transmission using VBI on PAL analog television signals.</span></span> <span data-ttu-id="f2f14-108">В этом стандарте предоставляются как субтитры, так и службы данных.</span><span class="sxs-lookup"><span data-stu-id="f2f14-108">Both captioning and data services are provided using this standard.</span></span> <span data-ttu-id="f2f14-109">Кодек WST — это фильтр режима ядра, который получает необработанные образцы ВБИ и, при необходимости, декодированные примеры телетекста из фильтра записи через фильтр [преобразователя tee/Sink-to-Sink](tee-sink-to-sink-converter.md) .</span><span class="sxs-lookup"><span data-stu-id="f2f14-109">The WST Codec is a kernel-mode filter that receives raw VBI samples and, optionally, decoded Teletext samples from the Capture Filter via the [Tee/Sink-to-Sink Converter](tee-sink-to-sink-converter.md) filter.</span></span> <span data-ttu-id="f2f14-110">Этот кодек декодирует и (или) дублирует некодированные и исправленные данные телетекста с ошибками для фильтра [WST](wst-decoder-filter.md) .</span><span class="sxs-lookup"><span data-stu-id="f2f14-110">This codec decodes and/or duplicates the decoded and forward-error-corrected Teletext data for the [WST Decoder](wst-decoder-filter.md) filter.</span></span> <span data-ttu-id="f2f14-111">Кодек WST соответствует фильтру декодера CC для передач NTSC.</span><span class="sxs-lookup"><span data-stu-id="f2f14-111">The WST Codec corresponds to the CC Decoder filter for NTSC transmissions.</span></span> <span data-ttu-id="f2f14-112">Декодер WST соответствует [строке 21 декодера](line-21-decoder-filter.md) для NTSC; Эти фильтры создают точечные рисунки, которые отправляются в микшер наложения или модуль подготовки видео для микширования.</span><span class="sxs-lookup"><span data-stu-id="f2f14-112">The WST Decoder corresponds to the [Line 21 Decoder](line-21-decoder-filter.md) for NTSC; these filters create the bitmaps that are sent to the Overlay Mixer or the Video Mixing Renderer.</span></span>

<span data-ttu-id="f2f14-113">Этот фильтр имеет два входных ПИН-кода: ВБИ и ХВКК.</span><span class="sxs-lookup"><span data-stu-id="f2f14-113">This filter has two input pins, VBI and HWCC.</span></span> <span data-ttu-id="f2f14-114">ПИН-код ВБИ используется для необработанных данных ВБИ, а ПИН-код ХВКК используется в том случае, когда в оборудовании, используемом фильтром записи, выполняется декодирование ВБИ.</span><span class="sxs-lookup"><span data-stu-id="f2f14-114">The VBI pin is used for raw VBI data, and the HWCC pin is used when the VBI decoding is performed in hardware by the capture filter.</span></span> <span data-ttu-id="f2f14-115">Когда данные поступают на ХВКК ПИН-код, кодек WST работает в режиме сквозного подключения и отправляет данные непосредственно в декодер WST, не обрабатывая его каким-либо образом.</span><span class="sxs-lookup"><span data-stu-id="f2f14-115">When the data is received on the HWCC pin, the WST Codec operates in "pass-through" mode, and sends the data directly to the WST Decoder without processing it in any way.</span></span> <span data-ttu-id="f2f14-116">Если фильтр записи предоставляет ПИН-код ХВКК, он должен быть напрямую подключен к соответствующему ПИН-коду WST.</span><span class="sxs-lookup"><span data-stu-id="f2f14-116">If the capture filter exposes an HWCC pin, it must be connected directly to the corresponding pin on the WST Codec.</span></span>

<span data-ttu-id="f2f14-117">Фильтр "WST кодек" отображается в категории фильтра "ВБИ кодеки WDM Streaming"**( \_ кскатегори \_ вбикодек**).</span><span class="sxs-lookup"><span data-stu-id="f2f14-117">The WST Codec filter appears in the "WDM Streaming VBI Codecs" filter category (**AM\_KSCATEGORY\_VBICODEC**).</span></span>

<span data-ttu-id="f2f14-118">Так как это фильтр режима ядра, приложения не могут создать его напрямую с помощью **CoCreateInstance**.</span><span class="sxs-lookup"><span data-stu-id="f2f14-118">Because this is a kernel-mode filter, applications cannot create it directly using **CoCreateInstance**.</span></span> <span data-ttu-id="f2f14-119">Вместо этого используйте [перечислитель системных устройств](system-device-enumerator.md).</span><span class="sxs-lookup"><span data-stu-id="f2f14-119">Instead, use the [System Device Enumerator](system-device-enumerator.md).</span></span> <span data-ttu-id="f2f14-120">Дополнительные сведения см. в разделе [Создание фильтров Kernel-Mode](creating-kernel-mode-filters.md).</span><span class="sxs-lookup"><span data-stu-id="f2f14-120">For more information, see [Creating Kernel-Mode Filters](creating-kernel-mode-filters.md).</span></span>

## <a name="related-topics"></a><span data-ttu-id="f2f14-121">См. также</span><span class="sxs-lookup"><span data-stu-id="f2f14-121">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="f2f14-122">Фильтры DirectShow</span><span class="sxs-lookup"><span data-stu-id="f2f14-122">DirectShow Filters</span></span>](directshow-filters.md)
</dt> <dt>

[<span data-ttu-id="f2f14-123">Просмотр стандартного телетекста в мире</span><span class="sxs-lookup"><span data-stu-id="f2f14-123">Viewing World Standard Teletext</span></span>](viewing-world-standard-teletext.md)
</dt> </dl>

 

 



