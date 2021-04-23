---
description: Тип формата VideoInfo2
ms.assetid: edd2013a-f0c5-4176-ba3a-a3af719ce31d
title: Тип формата VideoInfo2
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 74b0f435e0e2a1b5b1d948c42a881f19300a9c6f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "105683072"
---
# <a name="videoinfo2-format-type"></a><span data-ttu-id="dae35-103">Тип формата VideoInfo2</span><span class="sxs-lookup"><span data-stu-id="dae35-103">VideoInfo2 Format Type</span></span>

<span data-ttu-id="dae35-104">Предпочитаемый тип носителя для предварительного просмотра может быть типом с форматом [**VIDEOINFOHEADER2**](/previous-versions/windows/desktop/api/dvdmedia/ns-dvdmedia-videoinfoheader2) .</span><span class="sxs-lookup"><span data-stu-id="dae35-104">A preview pin's preferred media type might be a type with a [**VIDEOINFOHEADER2**](/previous-versions/windows/desktop/api/dvdmedia/ns-dvdmedia-videoinfoheader2) format.</span></span> <span data-ttu-id="dae35-105">Эта структура формата поддерживает специальные функции, такие как чередование изображений и пропорций изображения.</span><span class="sxs-lookup"><span data-stu-id="dae35-105">This format structure supports special features such as interlaced video and picture aspect ratios.</span></span>

<span data-ttu-id="dae35-106">VMR-7 и VMR-9 поддерживают [**VIDEOINFOHEADER2**](/previous-versions/windows/desktop/api/dvdmedia/ns-dvdmedia-videoinfoheader2) напрямую.</span><span class="sxs-lookup"><span data-stu-id="dae35-106">The VMR-7 and the VMR-9 both support [**VIDEOINFOHEADER2**](/previous-versions/windows/desktop/api/dvdmedia/ns-dvdmedia-videoinfoheader2) directly.</span></span> <span data-ttu-id="dae35-107">При подключении VMR к декодеру они будут согласовывать оптимальный формат.</span><span class="sxs-lookup"><span data-stu-id="dae35-107">When you connect the VMR to the decoder, they will negotiate the best format.</span></span> <span data-ttu-id="dae35-108">Однако старый фильтр модуля подготовки отчетов не поддерживает **VIDEOINFOHEADER2**.</span><span class="sxs-lookup"><span data-stu-id="dae35-108">The older Video Renderer filter, however, does not support **VIDEOINFOHEADER2**.</span></span> <span data-ttu-id="dae35-109">Чтобы использовать типы форматов **VIDEOINFOHEADER2** с фильтром модуля подготовки отчетов, необходимо вставить фильтр [микшера наложения](overlay-mixer-filter.md) на диаграмму.</span><span class="sxs-lookup"><span data-stu-id="dae35-109">To use **VIDEOINFOHEADER2** format types with the Video Renderer filter, you must insert the [Overlay Mixer](overlay-mixer-filter.md) filter into the graph.</span></span>

1.  <span data-ttu-id="dae35-110">Перечислите предпочтительные типы носителей в закреплениях вывода фильтра декодера с помощью метода [**Ипин:: енуммедиатипес**](/windows/desktop/api/Strmif/nf-strmif-ipin-enummediatypes) .</span><span class="sxs-lookup"><span data-stu-id="dae35-110">Enumerate the preferred media types on the decoder filter's output pin, using the [**IPin::EnumMediaTypes**](/windows/desktop/api/Strmif/nf-strmif-ipin-enummediatypes) method.</span></span>
2.  <span data-ttu-id="dae35-111">Проверьте первый тип носителя в последовательности перечисления.</span><span class="sxs-lookup"><span data-stu-id="dae35-111">Check the first media type in the enumeration sequence.</span></span>
3.  <span data-ttu-id="dae35-112">Если используется формат формата **\_ VideoInfo2**, подключите выходной закрепление к микшеру наложения.</span><span class="sxs-lookup"><span data-stu-id="dae35-112">If the format type is **FORMAT\_VideoInfo2**, connect the output pin to the Overlay Mixer.</span></span> <span data-ttu-id="dae35-113">Затем подключите микшер наложения к модулю подготовки видео.</span><span class="sxs-lookup"><span data-stu-id="dae35-113">Then connect the Overlay Mixer to the video renderer.</span></span> <span data-ttu-id="dae35-114">(См. раздел [Контакты порта видео](video-port-pins.md).)</span><span class="sxs-lookup"><span data-stu-id="dae35-114">(See [Video Port Pins](video-port-pins.md).)</span></span>

<span data-ttu-id="dae35-115">Если вы не следите за этими функциями, не нужно использовать микшер наложения.</span><span class="sxs-lookup"><span data-stu-id="dae35-115">If you do not care about these features, you do not have to use the Overlay Mixer.</span></span> <span data-ttu-id="dae35-116">Подключите декодер непосредственно к модулю визуализации видео, и он подключится к формату [**видеоинфохеадер**](/previous-versions/windows/desktop/api/amvideo/ns-amvideo-videoinfoheader) .</span><span class="sxs-lookup"><span data-stu-id="dae35-116">Connect the decoder directly to the Video Renderer, and it will connect with a [**VIDEOINFOHEADER**](/previous-versions/windows/desktop/api/amvideo/ns-amvideo-videoinfoheader) format instead.</span></span>

## <a name="related-topics"></a><span data-ttu-id="dae35-117">См. также</span><span class="sxs-lookup"><span data-stu-id="dae35-117">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="dae35-118">Разделы, посвященные расширенному записи</span><span class="sxs-lookup"><span data-stu-id="dae35-118">Advanced Capture Topics</span></span>](advanced-capture-topics.md)
</dt> <dt>

[<span data-ttu-id="dae35-119">Использование микшера наложения в видеозаписи</span><span class="sxs-lookup"><span data-stu-id="dae35-119">Using the Overlay Mixer in Video Capture</span></span>](using-the-overlay-mixer-in-video-capture.md)
</dt> </dl>

 

 



