---
description: Управление скоростью
ms.assetid: 6529859f-cfb6-4983-a489-bcc2f04e721f
title: Управление скоростью
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8f484a0469d96578ca1bb7e1d661d7e2319bd8bd
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "105711410"
---
# <a name="rate-control"></a><span data-ttu-id="62583-103">Управление скоростью</span><span class="sxs-lookup"><span data-stu-id="62583-103">Rate Control</span></span>

<span data-ttu-id="62583-104">[Сеанс мультимедиа](media-session.md) поддерживает изменение скорости воспроизведения, которое приложение может использовать для реализации таких функций воспроизведения, как перемотка вперед и назад.</span><span class="sxs-lookup"><span data-stu-id="62583-104">The [Media Session](media-session.md) supports changing the playback rate, which an application can use to implement playback features such as fast-forward and rewind.</span></span> <span data-ttu-id="62583-105">В этом разделе описывается, как приложения могут изменять скорость воспроизведения при использовании сеанса мультимедиа.</span><span class="sxs-lookup"><span data-stu-id="62583-105">This section describes how applications can change the playback rate while using the Media Session.</span></span>

<span data-ttu-id="62583-106">Сведения о поддержке управления частотой в собственных компонентах конвейера см. в разделе [Реализация управления скоростью](implementing-rate-control.md).</span><span class="sxs-lookup"><span data-stu-id="62583-106">For information about supporting rate control in your own pipeline components, see [Implementing Rate Control](implementing-rate-control.md).</span></span>

<span data-ttu-id="62583-107">Этот раздел содержит следующие подразделы.</span><span class="sxs-lookup"><span data-stu-id="62583-107">This section contains the following topics.</span></span>



| <span data-ttu-id="62583-108">Раздел</span><span class="sxs-lookup"><span data-stu-id="62583-108">Topic</span></span>                                                                                                      | <span data-ttu-id="62583-109">Описание</span><span class="sxs-lookup"><span data-stu-id="62583-109">Description</span></span>                                                            |
|------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------|
| [<span data-ttu-id="62583-110">Сведения об управлении скоростью</span><span class="sxs-lookup"><span data-stu-id="62583-110">About Rate Control</span></span>](about-rate-control.md)                                                               | <span data-ttu-id="62583-111">Предоставляет общий обзор управления скоростью.</span><span class="sxs-lookup"><span data-stu-id="62583-111">Gives a general overview of rate control.</span></span>                              |
| [<span data-ttu-id="62583-112">Определение поддерживаемых ставок</span><span class="sxs-lookup"><span data-stu-id="62583-112">How to Determine Supported Rates</span></span>](how-to-determine-supported-rates.md)                                   | <span data-ttu-id="62583-113">Как найти самые быстрые и самые медленные Поддерживаемые скорости воспроизведения.</span><span class="sxs-lookup"><span data-stu-id="62583-113">How to find the fastest and slowest supported playback rates.</span></span>          |
| [<span data-ttu-id="62583-114">Установка скорости воспроизведения в сеансе мультимедиа</span><span class="sxs-lookup"><span data-stu-id="62583-114">How to Set the Playback Rate on the Media Session</span></span>](how-to-set-the-playback-rate-on-the-media-session.md) | <span data-ttu-id="62583-115">Изменение скорости воспроизведения.</span><span class="sxs-lookup"><span data-stu-id="62583-115">How to change the playback rate.</span></span>                                       |
| [<span data-ttu-id="62583-116">Как выполнить очистку</span><span class="sxs-lookup"><span data-stu-id="62583-116">How to Perform Scrubbing</span></span>](how-to-perform-scrubbing.md)                                                   | <span data-ttu-id="62583-117">Пошаговый шаг за один кадр видео.</span><span class="sxs-lookup"><span data-stu-id="62583-117">How to step one video frame at a time.</span></span>                                 |
| [<span data-ttu-id="62583-118">Реализация управления скоростью</span><span class="sxs-lookup"><span data-stu-id="62583-118">Implementing Rate Control</span></span>](implementing-rate-control.md)                                                 | <span data-ttu-id="62583-119">Поддержка скорости воспроизведения переменных в пользовательском компоненте конвейера.</span><span class="sxs-lookup"><span data-stu-id="62583-119">How to support variable playback rates in a custom pipeline component.</span></span> |



 

## <a name="related-topics"></a><span data-ttu-id="62583-120">См. также</span><span class="sxs-lookup"><span data-stu-id="62583-120">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="62583-121">Сеанс мультимедиа</span><span class="sxs-lookup"><span data-stu-id="62583-121">Media Session</span></span>](media-session.md)
</dt> <dt>

[<span data-ttu-id="62583-122">Поиск, быстрая переадресация и обратная игра</span><span class="sxs-lookup"><span data-stu-id="62583-122">Seeking, Fast Forward, and Reverse Play</span></span>](seeking--fast-forward--and-reverse-play.md)
</dt> </dl>

 

 



