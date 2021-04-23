---
description: Аналоговые телевизоры
ms.assetid: 9f2c18ec-3684-42a8-a3df-5f8827b27642
title: Аналоговые телевизоры
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 33af8ba94831afed59d783598dbf6bc0eaee0ec6
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/06/2021
ms.locfileid: "104139819"
---
# <a name="analog-television"></a><span data-ttu-id="6f53a-103">Аналоговые телевизоры</span><span class="sxs-lookup"><span data-stu-id="6f53a-103">Analog Television</span></span>

<span data-ttu-id="6f53a-104">Аналоговый телевизор отличается от других сценариев записи видео несколькими способами:</span><span class="sxs-lookup"><span data-stu-id="6f53a-104">Analog television differs from other video capture scenarios in several ways:</span></span>

-   <span data-ttu-id="6f53a-105">Плата тюнера подстраивается к аналоговому сигналу, который затем поддается цифре.</span><span class="sxs-lookup"><span data-stu-id="6f53a-105">The tuner card tunes to an analog signal, which is then digitized.</span></span>
-   <span data-ttu-id="6f53a-106">Звук переносится в аналоговый сигнал.</span><span class="sxs-lookup"><span data-stu-id="6f53a-106">Audio is carried in the analog signal.</span></span> <span data-ttu-id="6f53a-107">То, как звук достигает звуковой карты, зависит от оборудования.</span><span class="sxs-lookup"><span data-stu-id="6f53a-107">How the audio reaches the sound card varies depending on the hardware.</span></span>
-   <span data-ttu-id="6f53a-108">Сигнал может содержать дополнительные данные в вертикальном интервале (ВБИ), например скрытые субтитры (CC), Стандартный телетекст (WST) и расширенные службы данных (XDS).</span><span class="sxs-lookup"><span data-stu-id="6f53a-108">The signal may contain additional data in the vertical blanking interval (VBI), such as closed captions (CC), World Standard Teletext (WST), and extended data services (XDS).</span></span>

<span data-ttu-id="6f53a-109">На следующей диаграмме показан типичный граф фильтра для просмотра телепередач.</span><span class="sxs-lookup"><span data-stu-id="6f53a-109">The following diagram shows a typical filter graph for television preview.</span></span>

![Граф аналогового телевидения](images/vidcap06.png)

-   <span data-ttu-id="6f53a-111">Фильтр [ТВ-тюнера](tv-tuner-filter.md) управляет настройкой.</span><span class="sxs-lookup"><span data-stu-id="6f53a-111">The [TV Tuner](tv-tuner-filter.md) filter controls tuning.</span></span>
-   <span data-ttu-id="6f53a-112">Фильтр [телевизионных аудио](tv-audio-filter.md) управляет обкодированием звука.</span><span class="sxs-lookup"><span data-stu-id="6f53a-112">The [TV Audio](tv-audio-filter.md) filter controls the audio decoding.</span></span>
-   <span data-ttu-id="6f53a-113">Если в карточке тюнера имеется более одного физического ввода, то фильтр [аналогового микшера видео](analog-video-crossbar-filter.md) позволяет приложению выбрать, какие входные данные декодированы и готовы к просмотру.</span><span class="sxs-lookup"><span data-stu-id="6f53a-113">If the tuner card has more than one physical input, the [Analog Video Crossbar](analog-video-crossbar-filter.md) filter enables the application to select which input is decoded and rendered.</span></span>
-   <span data-ttu-id="6f53a-114">Фильтр [записи видео WDM](wdm-video-capture-filter.md) предоставляет оцифрованный поток видео.</span><span class="sxs-lookup"><span data-stu-id="6f53a-114">The [WDM Video Capture](wdm-video-capture-filter.md) filter delivers the digitized video stream.</span></span>

<span data-ttu-id="6f53a-115">Построитель диаграмм для записи автоматически вставляет все фильтры, необходимые для вышестоящего потока, из фильтра записи.</span><span class="sxs-lookup"><span data-stu-id="6f53a-115">The Capture Graph Builder automatically inserts any filters that are required upstream from the capture filter.</span></span>

<span data-ttu-id="6f53a-116">В этом разделе рассматриваются следующие вопросы.</span><span class="sxs-lookup"><span data-stu-id="6f53a-116">This section contains the following topics:</span></span>

-   [<span data-ttu-id="6f53a-117">Настройка аналогового телевидения</span><span class="sxs-lookup"><span data-stu-id="6f53a-117">Analog Television Tuning</span></span>](analog-television-tuning.md)
-   [<span data-ttu-id="6f53a-118">Аналоговый телевизор</span><span class="sxs-lookup"><span data-stu-id="6f53a-118">Analog Television Audio</span></span>](analog-television-audio.md)
-   [<span data-ttu-id="6f53a-119">Субтитры и телетекст</span><span class="sxs-lookup"><span data-stu-id="6f53a-119">Closed Captions and Teletext</span></span>](closed-captions-and-teletext.md)

## <a name="related-topics"></a><span data-ttu-id="6f53a-120">См. также</span><span class="sxs-lookup"><span data-stu-id="6f53a-120">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="6f53a-121">Видеозапись</span><span class="sxs-lookup"><span data-stu-id="6f53a-121">Video Capture</span></span>](video-capture.md)
</dt> </dl>

 

 



