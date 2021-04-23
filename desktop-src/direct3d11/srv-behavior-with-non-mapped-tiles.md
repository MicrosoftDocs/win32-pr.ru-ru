---
title: Поведение SRV с несопоставленными плитками
description: Поведение операций чтения представления ресурса шейдера (SRV), включающих несопоставленные плитки, зависит от уровня поддержки оборудования.
ms.assetid: 9B720BEE-AB0C-4B75-92AD-3F382A107D48
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3e086a4db869c3204fc560e64002ba04e8bd8ba9
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/16/2019
ms.locfileid: "104252742"
---
# <a name="srv-behavior-with-non-mapped-tiles"></a><span data-ttu-id="2abbd-103">Поведение SRV с несопоставленными плитками</span><span class="sxs-lookup"><span data-stu-id="2abbd-103">SRV behavior with non-mapped tiles</span></span>

<span data-ttu-id="2abbd-104">Поведение операций чтения представления ресурса шейдера (SRV), включающих несопоставленные плитки, зависит от уровня поддержки оборудования.</span><span class="sxs-lookup"><span data-stu-id="2abbd-104">Behavior of shader resource view (SRV) reads that involve non-mapped tiles depends on the level of hardware support.</span></span> <span data-ttu-id="2abbd-105">Сведения о разбиении требований см. в разделе режим чтения для [мозаичных ресурсов компоненты](tiled-resources-features-tiers.md).</span><span class="sxs-lookup"><span data-stu-id="2abbd-105">For a breakdown of requirements, see read behavior for [Tiled resources features tiers](tiled-resources-features-tiers.md).</span></span> <span data-ttu-id="2abbd-106">В этом разделе описывается идеальное поведение, для которого требуется [уровень 2](tier-2.md).</span><span class="sxs-lookup"><span data-stu-id="2abbd-106">This section summarizes the ideal behavior, which [Tier 2](tier-2.md) requires.</span></span>

<span data-ttu-id="2abbd-107">Рассмотрим операцию по фильтрации текстуры, которая считывает данные из набора текселей в SRV.</span><span class="sxs-lookup"><span data-stu-id="2abbd-107">Consider a texture filter operation that reads from a set of texels in an SRV.</span></span> <span data-ttu-id="2abbd-108">Текселя, которые входят в несопоставленные плитки, дают 0 во всех неотсутствующих компонентах формата (и значение по умолчанию для отсутствующих компонент) в общей операции фильтрации помимо добавлений от сопоставленных текселей.</span><span class="sxs-lookup"><span data-stu-id="2abbd-108">Texels that fall on non-mapped tiles contribute 0 in all non-missing components of the format (and the default for missing components) into the overall filter operation alongside contributions from mapped texels.</span></span> <span data-ttu-id="2abbd-109">Текселя взвешиваются и объединяются вместе независимо от того, откуда поступили данные: из сопоставленных или несопоставленных плиток.</span><span class="sxs-lookup"><span data-stu-id="2abbd-109">The texels are all weighted and combined together independent of whether the data came from mapped or non-mapped tiles.</span></span>

<span data-ttu-id="2abbd-110">Некоторые аппаратные устройства первого поколения уровня [2](tier-2.md) не соответствуют этим требованиям к спецификации и возвращают 0 со значениями по умолчанию, описанными выше как общий результат фильтра, если любой пикселей текстуры (с ненулевым весом) попадает на несопоставленные плитки.</span><span class="sxs-lookup"><span data-stu-id="2abbd-110">Some first generation [Tier 2](tier-2.md) level hardware does not meet this spec requirement and returns the 0 with defaults described preceding as the overall filter result if any texels (with nonzero weight) fall on non-mapped tiles.</span></span> <span data-ttu-id="2abbd-111">Другому оборудованию не будет разрешено игнорировать требование по включению всех текселей (с ненулевым весом) в фильтр.</span><span class="sxs-lookup"><span data-stu-id="2abbd-111">No other hardware will be allowed to miss the requirement to include all (nonzero weight) texels in the filter.</span></span>

## <a name="related-topics"></a><span data-ttu-id="2abbd-112">См. также</span><span class="sxs-lookup"><span data-stu-id="2abbd-112">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="2abbd-113">Доступ конвейера к мозаичным ресурсам</span><span class="sxs-lookup"><span data-stu-id="2abbd-113">Pipeline access to tiled resources</span></span>](pipeline-access-to-tiled-resources.md)
</dt> </dl>

 

 




