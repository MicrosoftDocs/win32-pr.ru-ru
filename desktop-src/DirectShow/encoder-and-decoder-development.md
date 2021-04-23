---
description: Разработка кодировщика и декодера
ms.assetid: 075aaf0f-63c6-4286-966e-fdc72d0acb6e
title: Разработка кодировщика и декодера
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: dbe45fc726338e33205831959986178f4527673a
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/06/2021
ms.locfileid: "104140022"
---
# <a name="encoder-and-decoder-development"></a><span data-ttu-id="043bd-103">Разработка кодировщика и декодера</span><span class="sxs-lookup"><span data-stu-id="043bd-103">Encoder and Decoder Development</span></span>

<span data-ttu-id="043bd-104">В этом разделе содержатся статьи о разработке кодировщиков и декодеров для DirectShow.</span><span class="sxs-lookup"><span data-stu-id="043bd-104">This section contains articles about encoder and decoder development for DirectShow.</span></span> <span data-ttu-id="043bd-105">Эти разделы не относятся к разработчикам приложений.</span><span class="sxs-lookup"><span data-stu-id="043bd-105">These topics are not relevant for application developers.</span></span>

<span data-ttu-id="043bd-106">Программный декодер, поддерживающий ускорение видео DirectX (ва), должен быть реализован как фильтр преобразования DirectShow.</span><span class="sxs-lookup"><span data-stu-id="043bd-106">A software decoder that supports DirectX Video Acceleration (VA) must be implemented as a DirectShow copy transform filter.</span></span> <span data-ttu-id="043bd-107">Если декодер не поддерживает DirectX ва, он также может быть реализован как объект мультимедиа DirectX (DMO).</span><span class="sxs-lookup"><span data-stu-id="043bd-107">If the decoder does not support DirectX VA, it can also be implemented as a DirectX Media Object (DMO).</span></span> <span data-ttu-id="043bd-108">Декодер, который подключается к модулю обработки видео, не должен быть реализован как фильтр переноса данных, так как это приведет к значительному снижению производительности.</span><span class="sxs-lookup"><span data-stu-id="043bd-108">A decoder that connects to a video renderer should not be implemented as a trans-in-place filter, because this will result in significant performance degradation.</span></span> <span data-ttu-id="043bd-109">Сведения о том, как написать фильтр преобразования «копия», см. в разделе [написание фильтров преобразования](writing-transform-filters.md).</span><span class="sxs-lookup"><span data-stu-id="043bd-109">For information on how to write a copy transform filter, see [Writing Transform Filters](writing-transform-filters.md).</span></span>

<span data-ttu-id="043bd-110">Программные кодировщики можно реализовать как фильтры преобразования или дмос.</span><span class="sxs-lookup"><span data-stu-id="043bd-110">Software encoders can be implemented as either transform filters or DMOs.</span></span> <span data-ttu-id="043bd-111">Кодировщики не используют DirectX ва, так как DirectX ва в настоящее время используется только для распаковки.</span><span class="sxs-lookup"><span data-stu-id="043bd-111">Encoders do not use DirectX VA, since DirectX VA currently is only used for decompression.</span></span> <span data-ttu-id="043bd-112">Спецификация API кодировщика, описанная в этом разделе, относится к аппаратным и программным кодировщикам.</span><span class="sxs-lookup"><span data-stu-id="043bd-112">The Encoder API specification described in this section is relevant for both hardware and software encoders.</span></span>

<span data-ttu-id="043bd-113">В этом разделе рассматриваются следующие вопросы.</span><span class="sxs-lookup"><span data-stu-id="043bd-113">This section contains the following topics:</span></span>

-   [<span data-ttu-id="043bd-114">API кодировщика</span><span class="sxs-lookup"><span data-stu-id="043bd-114">Encoder API</span></span>](encoder-api.md)
-   [<span data-ttu-id="043bd-115">Интерфейсы и спецификации декодера</span><span class="sxs-lookup"><span data-stu-id="043bd-115">Decoder Interfaces and Specifications</span></span>](decoder-interfaces-and-specifications.md)
-   [<span data-ttu-id="043bd-116">Параметры декодера для Windows Media Center Edition</span><span class="sxs-lookup"><span data-stu-id="043bd-116">Decoder Settings for Windows Media Center Edition</span></span>](decoder-settings-for-windows-media-center-edition.md)

## <a name="related-topics"></a><span data-ttu-id="043bd-117">См. также</span><span class="sxs-lookup"><span data-stu-id="043bd-117">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="043bd-118">Использование VMR для разработчиков фильтров DirectShow</span><span class="sxs-lookup"><span data-stu-id="043bd-118">Using the VMR for DirectShow Filter Developers</span></span>](using-the-vmr-for-directshow-filter-developers.md)
</dt> </dl>

 

 



