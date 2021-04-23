---
description: Описывает статистику, которую можно получить из кодека Windows Media.
ms.assetid: 86c029af-e0fb-436a-b758-3f7d10c8bdeb
title: Получение статистики кодировки (Microsoft Media Foundation)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 92fb298b35e9cd4114d1a5ba2f5badfad36c09c7
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "103808063"
---
# <a name="getting-encoding-statistics-microsoft-media-foundation"></a><span data-ttu-id="79cef-103">Получение статистики кодировки (Microsoft Media Foundation)</span><span class="sxs-lookup"><span data-stu-id="79cef-103">Getting Encoding Statistics (Microsoft Media Foundation)</span></span>

<span data-ttu-id="79cef-104">Сведения о том, что происходит в сеансе кодирования, обычно немедленно доступны в виде кодов ошибок, возвращаемых при обработке образцов.</span><span class="sxs-lookup"><span data-stu-id="79cef-104">Information about what is happening in an encoding session is generally immediately available in the form of error codes returned when processing samples.</span></span> <span data-ttu-id="79cef-105">Однако есть некоторые статистические данные, которые можно получить из кодека о различных аспектах кодирования.</span><span class="sxs-lookup"><span data-stu-id="79cef-105">However, there are some statistics that you can retrieve from the codec about various encoding aspects.</span></span>

## <a name="video-frame-information"></a><span data-ttu-id="79cef-106">Сведения о кадре видео</span><span class="sxs-lookup"><span data-stu-id="79cef-106">Video Frame Information</span></span>

<span data-ttu-id="79cef-107">Некоторые статистические данные о видео, которые можно извлекать с учетом количества кадров, обрабатываемых кодировщиком.</span><span class="sxs-lookup"><span data-stu-id="79cef-107">Some video statistics that you can retrieve deal with the number of frames processed by the encoder.</span></span> <span data-ttu-id="79cef-108">Существует три свойства номера кадра, которые можно прочитать из видеокодировщика:</span><span class="sxs-lookup"><span data-stu-id="79cef-108">There are three frame number properties that you can read from the video encoder:</span></span>

-   <span data-ttu-id="79cef-109">[Мфпкэй \_ ТОТАЛФРАМЕС](mfpkey-totalframesproperty.md) — это число кадров, обрабатываемых во входном потоке DMO.</span><span class="sxs-lookup"><span data-stu-id="79cef-109">[MFPKEY\_TOTALFRAMES](mfpkey-totalframesproperty.md) is the number of frames processed through the input stream of the DMO.</span></span>
-   <span data-ttu-id="79cef-110">[Мфпкэй \_ КОДЕДФРАМЕС](mfpkey-codedframesproperty.md) — число закодированных кадров.</span><span class="sxs-lookup"><span data-stu-id="79cef-110">[MFPKEY\_CODEDFRAMES](mfpkey-codedframesproperty.md) is the number of frames encoded.</span></span> <span data-ttu-id="79cef-111">Вычитая это значение из общего числа переданных кадров, можно определить, сколько кадров было удалено.</span><span class="sxs-lookup"><span data-stu-id="79cef-111">By subtracting this value from the total number of frames passed, you can determine how many frames were dropped.</span></span>
-   <span data-ttu-id="79cef-112">[Мфпкэй \_ ЗЕРОБИТЕФРАМЕС](mfpkey-zerobyteframesproperty.md) — число кадров, не закодированных, так как уже включено Дублированное содержимое.</span><span class="sxs-lookup"><span data-stu-id="79cef-112">[MFPKEY\_ZEROBYTEFRAMES](mfpkey-zerobyteframesproperty.md) is the number of frames not encoded because they duplicated content already included.</span></span> <span data-ttu-id="79cef-113">Это значение не вычитается из числа кодированных кадров, сообщаемых DMO.</span><span class="sxs-lookup"><span data-stu-id="79cef-113">This value is not subtracted from the number of coded frames reported by the DMO.</span></span>

<span data-ttu-id="79cef-114">В любое время во время кодирования можно считывать свойства кадров видео.</span><span class="sxs-lookup"><span data-stu-id="79cef-114">You can read video frame properties at any time during encoding.</span></span> <span data-ttu-id="79cef-115">Это может быть полезно при определении пригодности параметров кодировки для содержимого. Если между итоговыми кадрами и закодированными кадрами существует большая разница, сжатое содержимое может не соответствовать требованиям к качеству.</span><span class="sxs-lookup"><span data-stu-id="79cef-115">This can be useful in determining if the encoding settings are appropriate for your content; if there is a large difference between total frames and coded frames, the compressed content might not meet your quality requirements.</span></span> <span data-ttu-id="79cef-116">После завершения кодирования можно прочитать окончательные значения.</span><span class="sxs-lookup"><span data-stu-id="79cef-116">You can read the final values after you finish encoding.</span></span>

## <a name="vbr-buffer-statistics"></a><span data-ttu-id="79cef-117">Статистика буфера VBR</span><span class="sxs-lookup"><span data-stu-id="79cef-117">VBR Buffer Statistics</span></span>

<span data-ttu-id="79cef-118">В зависимости от используемого режима кодировки некоторые или все параметры буфера могут быть определены во время кодирования (например, скорость потока с частотой, определяемая качеством, не известна до кодирования содержимого).</span><span class="sxs-lookup"><span data-stu-id="79cef-118">Depending upon the encoding mode used, some or all of the buffer settings may be determined during encoding (for example, the bit rate of quality based VBR is not known until the content is encoded).</span></span> <span data-ttu-id="79cef-119">Существует четыре свойства буфера VBR, которые можно получить с помощью метода **ипропертибаг:: Read** :</span><span class="sxs-lookup"><span data-stu-id="79cef-119">There are four VBR buffer properties that you can get using the **IPropertyBag::Read** method:</span></span>

-   <span data-ttu-id="79cef-120">[Мфпкэй \_ РАВГ](mfpkey-ravgproperty.md) — это средняя скорость потока содержимого VBR.</span><span class="sxs-lookup"><span data-stu-id="79cef-120">[MFPKEY\_RAVG](mfpkey-ravgproperty.md) is the average bit rate of the VBR content.</span></span>
-   <span data-ttu-id="79cef-121">[Мфпкэй \_ БАВГ](mfpkey-bavgproperty.md) — это окно буфера для средней скорости потока.</span><span class="sxs-lookup"><span data-stu-id="79cef-121">[MFPKEY\_BAVG](mfpkey-bavgproperty.md) is the buffer window for the average bit rate.</span></span>
-   <span data-ttu-id="79cef-122">[Мфпкэй \_ РМАКС](mfpkey-rmaxproperty.md) — это Пиковая скорость содержимого VBR.</span><span class="sxs-lookup"><span data-stu-id="79cef-122">[MFPKEY\_RMAX](mfpkey-rmaxproperty.md) is the peak bit rate of the VBR content.</span></span>
-   <span data-ttu-id="79cef-123">[Мфпкэй \_ БМАКС](mfpkey-bmaxproperty.md) — пиковое окно буфера.</span><span class="sxs-lookup"><span data-stu-id="79cef-123">[MFPKEY\_BMAX](mfpkey-bmaxproperty.md) is the peak buffer window.</span></span>

<span data-ttu-id="79cef-124">После начала обработки образцов не следует считывать какие бы то ни было свойства VBR, пока не завершится кодирование потока.</span><span class="sxs-lookup"><span data-stu-id="79cef-124">After you begin processing samples, you should not read any of the VBR properties until you are finished encoding the stream.</span></span> <span data-ttu-id="79cef-125">В противном случае кодировщик интерпретирует запрос как сигнал о завершении кодирования.</span><span class="sxs-lookup"><span data-stu-id="79cef-125">If you do, the encoder interprets your request as a signal that the encoding is complete.</span></span> <span data-ttu-id="79cef-126">Следующий пример, который вы обрабатываете, рассматривается как новый сеанс кодирования.</span><span class="sxs-lookup"><span data-stu-id="79cef-126">The next sample that you process is treated as a new encoding session.</span></span>

## <a name="related-topics"></a><span data-ttu-id="79cef-127">См. также</span><span class="sxs-lookup"><span data-stu-id="79cef-127">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="79cef-128">Кодеки Windows Media</span><span class="sxs-lookup"><span data-stu-id="79cef-128">Windows Media Codecs</span></span>](windows-media-codecs.md)
</dt> </dl>

 

 



