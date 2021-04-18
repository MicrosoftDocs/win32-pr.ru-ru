---
description: Новые сегменты
ms.assetid: 6c470b38-481f-4e52-93b8-eb6b343dcefc
title: Новые сегменты
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5438cb3b457ed8ea0f77bd2ac1dcc5d6d2c72698
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/06/2021
ms.locfileid: "105682184"
---
# <a name="new-segments"></a><span data-ttu-id="eaa29-103">Новые сегменты</span><span class="sxs-lookup"><span data-stu-id="eaa29-103">New Segments</span></span>

<span data-ttu-id="eaa29-104">*Сегмент* — это группа образцов мультимедиа, использующих общее время начала, время окончания и скорость воспроизведения.</span><span class="sxs-lookup"><span data-stu-id="eaa29-104">A *segment* is a group of media samples that share a common start time, stop time, and playback rate.</span></span> <span data-ttu-id="eaa29-105">Метод [**Ипин:: невсегмент**](/windows/desktop/api/Strmif/nf-strmif-ipin-newsegment) сигнализирует о начале нового сегмента.</span><span class="sxs-lookup"><span data-stu-id="eaa29-105">The [**IPin::NewSegment**](/windows/desktop/api/Strmif/nf-strmif-ipin-newsegment) method signals the start of a new segment.</span></span> <span data-ttu-id="eaa29-106">Он позволяет исходному фильтру уведомлять нисходящие фильтры о том, что сведения о времени и частоте изменились.</span><span class="sxs-lookup"><span data-stu-id="eaa29-106">It provides a way for a source filter to inform downstream filters that the time and rate information has changed.</span></span> <span data-ttu-id="eaa29-107">Например, если фильтр источника выполняет поиск новой точки в потоке, он вызывает **невсегмент** с новым временем начала.</span><span class="sxs-lookup"><span data-stu-id="eaa29-107">For example, if the source filter seeks to a new point in the stream, it calls **NewSegment** with the new start time.</span></span>

<span data-ttu-id="eaa29-108">Некоторые нисходящие фильтры используют сведения о сегменте при обработке образцов.</span><span class="sxs-lookup"><span data-stu-id="eaa29-108">Some downstream filters use the segment information when they process samples.</span></span> <span data-ttu-id="eaa29-109">Например, в формате, использующем сжатие по кадрам, если время окончания попадает в разностный кадр, фильтру источника может потребоваться отправить дополнительные выборки после времени окончания.</span><span class="sxs-lookup"><span data-stu-id="eaa29-109">For example, in a format that uses interframe compression, if the stop time falls on a delta frame, the source filter may need to send additional samples after the stop time.</span></span> <span data-ttu-id="eaa29-110">Это позволяет декодеру декодировать окончательный разностный кадр.</span><span class="sxs-lookup"><span data-stu-id="eaa29-110">This enables the decoder to decode the final delta frame.</span></span> <span data-ttu-id="eaa29-111">Чтобы определить правильный окончательный кадр, декодер обозначает время окончания сегмента.</span><span class="sxs-lookup"><span data-stu-id="eaa29-111">To determine the correct final frame, the decoder refers to the segment stop time.</span></span> <span data-ttu-id="eaa29-112">В качестве другого примера можно использовать частоту сегментов, а также частоту дискретизации для создания правильных звуковых выходных данных.</span><span class="sxs-lookup"><span data-stu-id="eaa29-112">As another example, audio renderers use the segment rate along with the audio sampling rate to generate the correct audio output.</span></span>

<span data-ttu-id="eaa29-113">В модели отправки фильтр источника инициирует вызов **невсегмент** .</span><span class="sxs-lookup"><span data-stu-id="eaa29-113">In the push model, the source filter initiates the **NewSegment** call.</span></span> <span data-ttu-id="eaa29-114">В модели извлечения это выполняется фильтром анализатора.</span><span class="sxs-lookup"><span data-stu-id="eaa29-114">In the pull model, this is done by the parser filter.</span></span> <span data-ttu-id="eaa29-115">В любом случае фильтр вызывает **невсегмент** для входного ПИН-кода, который распространяет вызов к следующему фильтру, пока вызов не достигнет модуля подготовки отчетов.</span><span class="sxs-lookup"><span data-stu-id="eaa29-115">In either case, the filter calls **NewSegment** on the downstream input pin, which propagates the call to the next filter, until the call reaches the renderer.</span></span> <span data-ttu-id="eaa29-116">Фильтры должны сериализовать вызовы **невсегмент** с другими вызовами потоковой передачи, например [**Имеминпутпин:: Receive**](/windows/desktop/api/Strmif/nf-strmif-imeminputpin-receive).</span><span class="sxs-lookup"><span data-stu-id="eaa29-116">Filters must serialize **NewSegment** calls with other streaming calls, such as [**IMemInputPin::Receive**](/windows/desktop/api/Strmif/nf-strmif-imeminputpin-receive).</span></span>

<span data-ttu-id="eaa29-117">Время потока сбрасывается в ноль после каждого нового сегмента.</span><span class="sxs-lookup"><span data-stu-id="eaa29-117">Stream time resets to zero after each new segment.</span></span> <span data-ttu-id="eaa29-118">Метки времени для выборок, доставленных после начала сегмента с нуля.</span><span class="sxs-lookup"><span data-stu-id="eaa29-118">Time stamps on samples delivered after the segment start from zero.</span></span>

 

 



