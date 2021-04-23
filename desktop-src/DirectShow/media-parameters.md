---
description: Параметры носителя
ms.assetid: 48b2bc2e-897d-4aa9-8a50-c2855a17dca5
title: Параметры носителя
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ce9276a3d38b9176458299bfd1a47057cac6236e
ms.sourcegitcommit: c16214e53680dc71d1c07111b51f72b82a4512d8
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/03/2021
ms.locfileid: "103914091"
---
# <a name="media-parameters"></a><span data-ttu-id="e5a25-103">Параметры носителя</span><span class="sxs-lookup"><span data-stu-id="e5a25-103">Media Parameters</span></span>

<span data-ttu-id="e5a25-104">Параметры мультимедиа позволяют приложению настраивать свойства объекта таким образом, чтобы они изменялись со временем математически детерминированным образом.</span><span class="sxs-lookup"><span data-stu-id="e5a25-104">Media parameters enable an application to configure an object's properties so that they change over time in a mathematically deterministic way.</span></span>

<span data-ttu-id="e5a25-105">Например, предположим, что звуковый инженер является сочетанием цифровой главной ленты и хочет применить незначительную задержку к разделу вокал для заполнения звука.</span><span class="sxs-lookup"><span data-stu-id="e5a25-105">For example, suppose that a sound engineer is mixing a digital master tape and wants to apply a slight delay to a vocal section, to fill out the sound.</span></span> <span data-ttu-id="e5a25-106">Результат будет жарринг, если задержка резко прерывается.</span><span class="sxs-lookup"><span data-stu-id="e5a25-106">The effect will be jarring if the delay cuts in abruptly.</span></span> <span data-ttu-id="e5a25-107">Вместо этого результат должен начинаться 100% сухой (без задержки), а задолженность или сухой набор будет постепенно увеличиваться, пока не достигнет нужного уровня.</span><span class="sxs-lookup"><span data-stu-id="e5a25-107">Instead, the effect should begin 100 percent dry (no delay), and the wet/dry mix should increase gradually until it reaches the desired level.</span></span> <span data-ttu-id="e5a25-108">Более того, этот переход должен соответствовать гладкой кривой или линейной прогрессии.</span><span class="sxs-lookup"><span data-stu-id="e5a25-108">Moreover, this transition should follow a smooth curve or linear progression.</span></span> <span data-ttu-id="e5a25-109">Для поддержки этого сценария DMO может предоставлять следующие интерфейсы:</span><span class="sxs-lookup"><span data-stu-id="e5a25-109">To support this scenario, a DMO can expose the following interfaces:</span></span>

-   <span data-ttu-id="e5a25-110">[**Имедиапараминфо**](/previous-versions/windows/desktop/api/Medparam/nn-medparam-imediaparaminfo) содержит методы для обнаружения сведений о поддерживаемых свойствах.</span><span class="sxs-lookup"><span data-stu-id="e5a25-110">[**IMediaParamInfo**](/previous-versions/windows/desktop/api/Medparam/nn-medparam-imediaparaminfo) contains methods for discovering information about the supported properties.</span></span> <span data-ttu-id="e5a25-111">Как правило, клиент вызывает эти методы перед началом потоковой передачи данных.</span><span class="sxs-lookup"><span data-stu-id="e5a25-111">Typically, the client will call these methods before it begins to stream data.</span></span>
-   <span data-ttu-id="e5a25-112">[**Имедиапарамс**](/previous-versions/windows/desktop/api/Medparam/nn-medparam-imediaparams) содержат методы для настройки кривых, которые будут следовать за параметром во время потоковой передачи.</span><span class="sxs-lookup"><span data-stu-id="e5a25-112">[**IMediaParams**](/previous-versions/windows/desktop/api/Medparam/nn-medparam-imediaparams) contain methods for setting the curves that a parameter will follow during streaming.</span></span>

<span data-ttu-id="e5a25-113">Эти интерфейсы предназначены в основном для дмос, но любой объект может их поддерживать.</span><span class="sxs-lookup"><span data-stu-id="e5a25-113">These interfaces are designed primarily for DMOs, but any object can support them.</span></span> <span data-ttu-id="e5a25-114">В этом разделе *параметр* Term ссылается на любое свойство, которое поддерживает эти два интерфейса.</span><span class="sxs-lookup"><span data-stu-id="e5a25-114">Within this section, the term *parameter* refers to any property that supports these two interfaces.</span></span>

<span data-ttu-id="e5a25-115">В этом разделе рассматриваются следующие вопросы.</span><span class="sxs-lookup"><span data-stu-id="e5a25-115">This section contains the following topics:</span></span>

-   [<span data-ttu-id="e5a25-116">Кривые параметров</span><span class="sxs-lookup"><span data-stu-id="e5a25-116">Parameter Curves</span></span>](parameter-curves.md)
-   [<span data-ttu-id="e5a25-117">Сведения о параметрах</span><span class="sxs-lookup"><span data-stu-id="e5a25-117">Parameter Information</span></span>](parameter-information.md)
-   [<span data-ttu-id="e5a25-118">Сегменты конверта</span><span class="sxs-lookup"><span data-stu-id="e5a25-118">Envelope Segments</span></span>](envelope-segments.md)
-   [<span data-ttu-id="e5a25-119">Вычисление значений параметров</span><span class="sxs-lookup"><span data-stu-id="e5a25-119">Calculating Parameter Values</span></span>](calculating-parameter-values.md)

## <a name="related-topics"></a><span data-ttu-id="e5a25-120">См. также</span><span class="sxs-lookup"><span data-stu-id="e5a25-120">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="e5a25-121">Объекты мультимедиа DirectX</span><span class="sxs-lookup"><span data-stu-id="e5a25-121">DirectX Media Objects</span></span>](directx-media-objects.md)
</dt> </dl>

 

 



