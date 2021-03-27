---
title: Поведение UAV с несопоставленными плитками
description: Поведение операций чтения и записи представлений неупорядоченного доступа (UAV) зависит от уровня поддержки оборудования.
ms.assetid: 26C40D1F-983B-4E5B-99F3-FD4E47BE1D7D
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9a9909f8faecd3345761ae26e60835c77aae9ab3
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/16/2019
ms.locfileid: "103986229"
---
# <a name="uav-behavior-with-non-mapped-tiles"></a><span data-ttu-id="2de91-103">Поведение UAV с несопоставленными плитками</span><span class="sxs-lookup"><span data-stu-id="2de91-103">UAV behavior with non-mapped tiles</span></span>

<span data-ttu-id="2de91-104">Поведение операций чтения и записи представлений неупорядоченного доступа (UAV) зависит от уровня поддержки оборудования.</span><span class="sxs-lookup"><span data-stu-id="2de91-104">Behavior of unordered access view (UAV) reads and writes depends on the level of hardware support.</span></span> <span data-ttu-id="2de91-105">Сведения о разбиении требований см. в разделе Общее поведение операций чтения и записи для [мозаичных ресурсов](tiled-resources-features-tiers.md).</span><span class="sxs-lookup"><span data-stu-id="2de91-105">For a breakdown of requirements, see overall read and write behavior for [Tiled resources features tiers](tiled-resources-features-tiers.md).</span></span> <span data-ttu-id="2de91-106">В этом разделе описывается идеальное поведение.</span><span class="sxs-lookup"><span data-stu-id="2de91-106">This section summarizes the ideal behavior.</span></span>

<span data-ttu-id="2de91-107">Операции шейдера, выполняющие чтение из несопоставленной плитки в UAV, возвращают 0 во всех присутствующих компонентах формата и значение по умолчанию для отсутствующих компонентов.</span><span class="sxs-lookup"><span data-stu-id="2de91-107">Shader operations that read from a non-mapped tile in a UAV return 0 in all non-missing components of the format, and the default for missing components.</span></span>

<span data-ttu-id="2de91-108">В результате операций шейдера, пытающихся выполнить запись в несопоставленную плитку, в несопоставленную область ничего не записывается (тогда как запись в сопоставленную область происходит).</span><span class="sxs-lookup"><span data-stu-id="2de91-108">Shader operations that attempt to write to a non-mapped tile cause nothing to be written to the non-mapped area (while writes to a mapped area proceed).</span></span> <span data-ttu-id="2de91-109">Такое идеальное определение обработки записи не требуется для [второго уровня](tier-2.md). Операции записи в несопоставленные плитки могут оказаться в кэше, откуда данные могут взять последующие операции чтения.</span><span class="sxs-lookup"><span data-stu-id="2de91-109">This ideal definition for write handling is not required by [Tier 2](tier-2.md); writes to non-mapped tiles can end up in a cache that subsequent reads could pick up.</span></span>

## <a name="related-topics"></a><span data-ttu-id="2de91-110">См. также</span><span class="sxs-lookup"><span data-stu-id="2de91-110">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="2de91-111">Доступ конвейера к мозаичным ресурсам</span><span class="sxs-lookup"><span data-stu-id="2de91-111">Pipeline access to tiled resources</span></span>](pipeline-access-to-tiled-resources.md)
</dt> </dl>

 

 




