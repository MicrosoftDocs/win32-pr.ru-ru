---
description: Выбор аудиокодека
ms.assetid: 37f3582c-c718-42ae-b887-d7d31ee853e9
title: Выбор аудиокодека (Microsoft Media Foundation)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a04b16dc0c6e65356f7d7e74b85b0671c2b41369
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104262819"
---
# <a name="choosing-an-audio-codec-microsoft-media-foundation"></a><span data-ttu-id="3e77e-103">Выбор аудиокодека (Microsoft Media Foundation)</span><span class="sxs-lookup"><span data-stu-id="3e77e-103">Choosing an Audio Codec (Microsoft Media Foundation)</span></span>

<span data-ttu-id="3e77e-104">[**Кодировщик Windows Media Audio**](windowsmediaaudioencoder.md) предоставляет три категории кодирования звука, как показано в следующей таблице.</span><span class="sxs-lookup"><span data-stu-id="3e77e-104">The [**Windows Media Audio Encoder**](windowsmediaaudioencoder.md) provides three categories of audio encoding as shown in the following table.</span></span>



| <span data-ttu-id="3e77e-105">Категория</span><span class="sxs-lookup"><span data-stu-id="3e77e-105">Category</span></span>                         | <span data-ttu-id="3e77e-106">Назначение</span><span class="sxs-lookup"><span data-stu-id="3e77e-106">Purpose</span></span>                                                    |
|----------------------------------|------------------------------------------------------------|
| <span data-ttu-id="3e77e-107">Windows Media Audio Standard</span><span class="sxs-lookup"><span data-stu-id="3e77e-107">Windows Media Audio Standard</span></span>     | <span data-ttu-id="3e77e-108">Универсальное сжатие звука.</span><span class="sxs-lookup"><span data-stu-id="3e77e-108">General-purpose compression of audio.</span></span>                      |
| <span data-ttu-id="3e77e-109">Windows Media Audio Professional</span><span class="sxs-lookup"><span data-stu-id="3e77e-109">Windows Media Audio Professional</span></span> | <span data-ttu-id="3e77e-110">Сжатие звука с несколькими каналами и высокой четкости.</span><span class="sxs-lookup"><span data-stu-id="3e77e-110">Compressing multi-channel and high-definition audio.</span></span>       |
| <span data-ttu-id="3e77e-111">Windows Media Audio без потерь</span><span class="sxs-lookup"><span data-stu-id="3e77e-111">Windows Media Audio Lossless</span></span>     | <span data-ttu-id="3e77e-112">Сжатие звука без потери исходных данных.</span><span class="sxs-lookup"><span data-stu-id="3e77e-112">Compressing audio without losing any of the original data.</span></span> |



 

<span data-ttu-id="3e77e-113">Стандартная категория обеспечивает кодирование звука общего назначения, пригодное для различных сценариев воспроизведения.</span><span class="sxs-lookup"><span data-stu-id="3e77e-113">The Standard category provides general-purpose audio encoding suitable for a variety of playback scenarios.</span></span> <span data-ttu-id="3e77e-114">Например, он может сжимать звук с низкой скоростью для потоковой передачи по сети с ограниченной пропускной способностью или для отрисовки на портативных устройствах.</span><span class="sxs-lookup"><span data-stu-id="3e77e-114">For example, it can compress audio to a low bit rate for streaming over a network with limited bandwidth, or for rendering on portable devices.</span></span> <span data-ttu-id="3e77e-115">На другом конце шкалы он может создать сжатое аудио содержимое для высокого качества воспроизведения.</span><span class="sxs-lookup"><span data-stu-id="3e77e-115">On the other end of the scale, it can produce compressed audio content for high-quality playback.</span></span> <span data-ttu-id="3e77e-116">Выделение стандартных алгоритмов кодирования — музыка, но они подходят и для других сложных звуковых материалов.</span><span class="sxs-lookup"><span data-stu-id="3e77e-116">The emphasis of the Standard encoding algorithms is on music, but they are suitable for other complex audio content as well.</span></span> <span data-ttu-id="3e77e-117">Стандартная категория должна иметь значение по умолчанию для звукового содержимого.</span><span class="sxs-lookup"><span data-stu-id="3e77e-117">The Standard category should be your default for audio content.</span></span> <span data-ttu-id="3e77e-118">Для удовлетворения конкретных потребностей следует использовать категории "профессиональная" и "без потерь".</span><span class="sxs-lookup"><span data-stu-id="3e77e-118">The Professional and Lossless categories should be used to meet specific needs.</span></span>

<span data-ttu-id="3e77e-119">Отдельный кодировщик, [**голосовой кодировщик Windows Media**](windowsmediaaudiovoiceencoder.md), обеспечивает сжатие речи.</span><span class="sxs-lookup"><span data-stu-id="3e77e-119">A separate encoder, the [**Windows Media Voice Encoder**](windowsmediaaudiovoiceencoder.md), provides compression of speech.</span></span>

## <a name="related-topics"></a><span data-ttu-id="3e77e-120">См. также</span><span class="sxs-lookup"><span data-stu-id="3e77e-120">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="3e77e-121">Работа с аудио</span><span class="sxs-lookup"><span data-stu-id="3e77e-121">Working with Audio</span></span>](workingwithaudio.md)
</dt> </dl>

 

 



