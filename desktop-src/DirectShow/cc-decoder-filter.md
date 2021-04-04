---
description: Фильтр декодера CC
ms.assetid: 57ef75f6-411c-4b1f-b0dc-ac293ebc0b9c
title: Фильтр декодера CC
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d93995207e4f1a397db28f743d1f972b871b0553
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/06/2021
ms.locfileid: "103989975"
---
# <a name="cc-decoder-filter"></a><span data-ttu-id="027c4-103">Фильтр декодера CC</span><span class="sxs-lookup"><span data-stu-id="027c4-103">CC Decoder Filter</span></span>

> [!IMPORTANT]
> <span data-ttu-id="027c4-104">Этот компонент был удален из Windows Vista и более поздних операционных систем.</span><span class="sxs-lookup"><span data-stu-id="027c4-104">This component has been removed from Windows Vista and later operating systems.</span></span> <span data-ttu-id="027c4-105">Он доступен для использования в операционных системах Microsoft Windows 2000, Windows XP и Windows Server 2003.</span><span class="sxs-lookup"><span data-stu-id="027c4-105">It is available for use in the Microsoft Windows 2000, Windows XP, and Windows Server 2003 operating systems.</span></span>

 

<span data-ttu-id="027c4-106">Декодер ВБИ для копии — это фильтр класса потока в режиме ядра.</span><span class="sxs-lookup"><span data-stu-id="027c4-106">The CC VBI Decoder is a kernel-mode stream class filter.</span></span> <span data-ttu-id="027c4-107">Он отображается в Графедит в категории "кодеки WDM Streaming ВБИ".</span><span class="sxs-lookup"><span data-stu-id="027c4-107">It appears in GraphEdit under the "WDM Streaming VBI Codecs" category.</span></span> <span data-ttu-id="027c4-108">Он принимает образцы звуковых форм, доставляемые фильтром записи и доставляет декодированные данные с закрытым субтитром в [строку 21 декодера](line-21-decoder-filter.md) и (или) заинтересованным приложениям.</span><span class="sxs-lookup"><span data-stu-id="027c4-108">It accepts sample waveforms delivered by a capture filter and delivers decoded closed-captioning data to the [Line 21 Decoder](line-21-decoder-filter.md) and/or to interested applications.</span></span>

<span data-ttu-id="027c4-109">Этот фильтр имеет два входных ПИН-кода: ВБИ и ХВКК.</span><span class="sxs-lookup"><span data-stu-id="027c4-109">This filter has two input pins, VBI and HWCC.</span></span> <span data-ttu-id="027c4-110">ПИН-код ВБИ используется для необработанных данных ВБИ, а ПИН-код ХВКК используется в том случае, когда в оборудовании, используемом фильтром записи, выполняется декодирование ВБИ.</span><span class="sxs-lookup"><span data-stu-id="027c4-110">The VBI pin is used for raw VBI data, and the HWCC pin is used when the VBI decoding is performed in hardware by the capture filter.</span></span> <span data-ttu-id="027c4-111">Когда данные поступают на ХВКК ПИН-код, декодер CC работает в режиме сквозной передачи и отправляет данные непосредственно в строку 21, не обрабатывая их каким-либо образом.</span><span class="sxs-lookup"><span data-stu-id="027c4-111">When the data is received on the HWCC pin, the CC Decoder operates in "pass-through" mode, and sends the data directly to the Line 21 Decoder without processing it in any way.</span></span> <span data-ttu-id="027c4-112">Если фильтр записи предоставляет ПИН-код ХВКК, он должен быть напрямую подключен к соответствующему ПИН-коду в декодере CC.</span><span class="sxs-lookup"><span data-stu-id="027c4-112">If the capture filter exposes an HWCC pin, it must be connected directly to the corresponding pin on the CC Decoder.</span></span> <span data-ttu-id="027c4-113">Категория закрепления — **это \_ пиннаме \_ \_ запись копии видео**.</span><span class="sxs-lookup"><span data-stu-id="027c4-113">The pin category is **PINNAME\_VIDEO\_CC\_CAPTURE**.</span></span>

<span data-ttu-id="027c4-114">Декодер CC имеет до восьми выходных закрепления, каждый из которых может выбирать собственные строки и подпотоки.</span><span class="sxs-lookup"><span data-stu-id="027c4-114">The CC Decoder has up to eight output pins, each of which can select their own lines and substreams.</span></span> <span data-ttu-id="027c4-115">Первый выходной ПИН-код подключен к декодеру Line-21.</span><span class="sxs-lookup"><span data-stu-id="027c4-115">The first output pin is connected to the Line-21 Decoder.</span></span>

<span data-ttu-id="027c4-116">Фильтр декодера CC отображается в категории фильтра "ВБИ кодеки WDM Streaming" (**\_ кскатегори \_ вбикодек**).</span><span class="sxs-lookup"><span data-stu-id="027c4-116">The CC Decoder filter appears in the "WDM Streaming VBI Codecs" filter category (**AM\_KSCATEGORY\_VBICODEC**).</span></span>

<span data-ttu-id="027c4-117">Так как это фильтр режима ядра, приложения не могут создать его напрямую с помощью **CoCreateInstance**.</span><span class="sxs-lookup"><span data-stu-id="027c4-117">Because this is a kernel-mode filter, applications cannot create it directly using **CoCreateInstance**.</span></span> <span data-ttu-id="027c4-118">Вместо этого используйте [перечислитель системных устройств](system-device-enumerator.md).</span><span class="sxs-lookup"><span data-stu-id="027c4-118">Instead, use the [System Device Enumerator](system-device-enumerator.md).</span></span> <span data-ttu-id="027c4-119">Дополнительные сведения см. в разделе [Создание фильтров Kernel-Mode](creating-kernel-mode-filters.md).</span><span class="sxs-lookup"><span data-stu-id="027c4-119">For more information, see [Creating Kernel-Mode Filters](creating-kernel-mode-filters.md).</span></span>

## <a name="related-topics"></a><span data-ttu-id="027c4-120">См. также</span><span class="sxs-lookup"><span data-stu-id="027c4-120">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="027c4-121">Фильтры DirectShow</span><span class="sxs-lookup"><span data-stu-id="027c4-121">DirectShow Filters</span></span>](directshow-filters.md)
</dt> <dt>

[<span data-ttu-id="027c4-122">Просмотр скрытых субтитров</span><span class="sxs-lookup"><span data-stu-id="027c4-122">Viewing Closed Captions</span></span>](viewing-closed-captions.md)
</dt> </dl>

 

 



