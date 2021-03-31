---
description: Управление параметрами тумана осуществляется с помощью состояний отрисовки устройства.
ms.assetid: a3c5f439-6937-4ba9-991f-5a4154447cf9
title: Параметры тумана (Direct3D 9)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a03104df36aba0868c15ccc0b8ddc78d1352bef7
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/06/2021
ms.locfileid: "103894525"
---
# <a name="fog-parameters-direct3d-9"></a><span data-ttu-id="2c0fa-103">Параметры тумана (Direct3D 9)</span><span class="sxs-lookup"><span data-stu-id="2c0fa-103">Fog Parameters (Direct3D 9)</span></span>

<span data-ttu-id="2c0fa-104">Управление параметрами тумана осуществляется с помощью состояний отрисовки устройства.</span><span class="sxs-lookup"><span data-stu-id="2c0fa-104">Fog parameters are controlled through device render states.</span></span> <span data-ttu-id="2c0fa-105">Типы пиксельных и вершинных туманов поддерживают все формулы тумана, появившиеся в [формулах тумана (Direct3D 9)](fog-formulas.md).</span><span class="sxs-lookup"><span data-stu-id="2c0fa-105">Both pixel and vertex fog types support all the fog formulas introduced in [Fog Formulas (Direct3D 9)](fog-formulas.md).</span></span> <span data-ttu-id="2c0fa-106">Перечисляемый тип [**D3DFOGMODE**](./d3dfogmode.md) определяет константы, которые можно использовать для определения формулы тумана, которую должен использовать Microsoft Direct3D.</span><span class="sxs-lookup"><span data-stu-id="2c0fa-106">The [**D3DFOGMODE**](./d3dfogmode.md) enumerated type defines constants that you can use to identify the fog formula you want Microsoft Direct3D to use.</span></span> <span data-ttu-id="2c0fa-107">\_Состояние отображения D3DRS фогтаблемоде управляет режимом тумана, который Direct3D использует для пиксельных туманов, а \_ состояние отображения D3DRS фогвертексмоде — режим для вершинного тумана.</span><span class="sxs-lookup"><span data-stu-id="2c0fa-107">The D3DRS\_FOGTABLEMODE render state controls the fog mode that Direct3D uses for pixel fog, and the D3DRS\_FOGVERTEXMODE render state controls the mode for vertex fog.</span></span>

<span data-ttu-id="2c0fa-108">При использовании линейной формулы тумана начальное и конечное расстояния задаются с помощью D3DRS \_ фогстарт и D3DRS \_ фоженд Rendering States.</span><span class="sxs-lookup"><span data-stu-id="2c0fa-108">When using the linear fog formula, you set the starting and ending distances through the D3DRS\_FOGSTART and D3DRS\_FOGEND render states.</span></span> <span data-ttu-id="2c0fa-109">Сведения о том, как система интерпретирует эти значения, зависит от типа тумана, используемого приложением-пиксельным или вершинным туманом, и при использовании пиксельного тумана, если используется глубина, основанная на z или w.</span><span class="sxs-lookup"><span data-stu-id="2c0fa-109">How the system interprets these values depends on the type of fog your application uses - pixel or vertex fog - and, when using pixel fog, if z-based or w-based depth is being used.</span></span> <span data-ttu-id="2c0fa-110">В следующей таблице перечислены типы туманов и их начальные и конечные единицы.</span><span class="sxs-lookup"><span data-stu-id="2c0fa-110">The following table summarizes fog types and their start and end units.</span></span>



| <span data-ttu-id="2c0fa-111">Тип тумана</span><span class="sxs-lookup"><span data-stu-id="2c0fa-111">Fog type</span></span>  | <span data-ttu-id="2c0fa-112">Единицы начала и окончания тумана</span><span class="sxs-lookup"><span data-stu-id="2c0fa-112">Fog start/end units</span></span>      |
|-----------|--------------------------|
| <span data-ttu-id="2c0fa-113">Пиксель (Z)</span><span class="sxs-lookup"><span data-stu-id="2c0fa-113">Pixel (Z)</span></span> | <span data-ttu-id="2c0fa-114">Пространство устройства \[ 0,0, 1,0\]</span><span class="sxs-lookup"><span data-stu-id="2c0fa-114">Device space \[0.0,1.0\]</span></span> |
| <span data-ttu-id="2c0fa-115">Пиксель (W)</span><span class="sxs-lookup"><span data-stu-id="2c0fa-115">Pixel (W)</span></span> | <span data-ttu-id="2c0fa-116">Место на камере</span><span class="sxs-lookup"><span data-stu-id="2c0fa-116">Camera space</span></span>             |
| <span data-ttu-id="2c0fa-117">Вершина</span><span class="sxs-lookup"><span data-stu-id="2c0fa-117">Vertex</span></span>    | <span data-ttu-id="2c0fa-118">Место на камере</span><span class="sxs-lookup"><span data-stu-id="2c0fa-118">Camera space</span></span>             |



 

<span data-ttu-id="2c0fa-119">\_Состояние отрисовки D3DRS фогденсити управляет плотностью тумана, применяемой при включенной формуле экспоненциального тумана.</span><span class="sxs-lookup"><span data-stu-id="2c0fa-119">The D3DRS\_FOGDENSITY render state controls the fog density applied when an exponential fog formula is enabled.</span></span> <span data-ttu-id="2c0fa-120">Плотность тумана по сути является весовым фактором, от 0,0 до 1,0 (включительно), которое масштабирует значение расстояния в экспоненте.</span><span class="sxs-lookup"><span data-stu-id="2c0fa-120">Fog density is essentially a weighting factor, ranging from 0.0 to 1.0 (inclusive), that scales the distance value in the exponent.</span></span>

<span data-ttu-id="2c0fa-121">Цвет, используемый системой для смешения тумана, управляется через \_ состояние рендеринга устройства D3DRS фогколор.</span><span class="sxs-lookup"><span data-stu-id="2c0fa-121">The color that the system uses for fog blending is controlled through the D3DRS\_FOGCOLOR device render state.</span></span> <span data-ttu-id="2c0fa-122">Дополнительные сведения см. в разделе [Цвет тумана (Direct3D 9)](fog-color.md) и [смешение тумана (Direct3D 9)](fog-blending.md).</span><span class="sxs-lookup"><span data-stu-id="2c0fa-122">For more information, see [Fog Color (Direct3D 9)](fog-color.md) and [Fog Blending (Direct3D 9)](fog-blending.md).</span></span>

## <a name="related-topics"></a><span data-ttu-id="2c0fa-123">См. также</span><span class="sxs-lookup"><span data-stu-id="2c0fa-123">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="2c0fa-124">Типы туманов</span><span class="sxs-lookup"><span data-stu-id="2c0fa-124">Fog Types</span></span>](fog-types.md)
</dt> </dl>

 

 
