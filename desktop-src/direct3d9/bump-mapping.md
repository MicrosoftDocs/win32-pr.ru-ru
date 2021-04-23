---
description: Сопоставление рельефов — это особая форма сопоставления в виде зеркального или рассеянного окружения, которая имитирует отражения объектов с тонкой мозаикой, не требуя очень высоких значений в виде многоугольников.
ms.assetid: 3e195e4f-3fa9-43c4-b2e5-42a6b3aaccf2
title: Отображение рельефа (Direct3D 9)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b9dba4621568f595eae965941168ad6930e183f7
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104142361"
---
# <a name="bump-mapping-direct3d-9"></a><span data-ttu-id="2e999-103">Отображение рельефа (Direct3D 9)</span><span class="sxs-lookup"><span data-stu-id="2e999-103">Bump Mapping (Direct3D 9)</span></span>

<span data-ttu-id="2e999-104">Сопоставление рельефов — это особая форма сопоставления в виде зеркального или рассеянного окружения, которая имитирует отражения объектов с тонкой мозаикой, не требуя очень высоких значений в виде многоугольников.</span><span class="sxs-lookup"><span data-stu-id="2e999-104">Bump mapping is a special form of specular or diffuse environment mapping that simulates the reflections of finely tessellated objects without requiring extremely high polygon counts.</span></span> <span data-ttu-id="2e999-105">Сопоставление выпуклости, реализованное с помощью Direct3D, можно точно описать как пертурбатион координат текстуры на основе текстурных или диффузных карт, так как вы предоставляете сведения о контуре выпуклости с точки зрения разностных значений, которые система применяет к координатам текстуры и координаты v карты среды на следующей стадии текстуры.</span><span class="sxs-lookup"><span data-stu-id="2e999-105">Bump mapping implemented by Direct3D can be accurately described as per-pixel texture coordinate perturbation of specular or diffuse environment maps, because you provide information about the contour of the bump map in terms of delta values, which the system applies to the u and v texture coordinates of an environment map in the next texture stage.</span></span> <span data-ttu-id="2e999-106">Разностные значения кодируются в формате пикселей поверхности на карте выпуклости (см. раздел [неровные форматы пикселей на карте](bump-map-pixel-formats.md)).</span><span class="sxs-lookup"><span data-stu-id="2e999-106">The delta values are encoded in the pixel format of the bump map surface (see [Bump Map Pixel Formats](bump-map-pixel-formats.md)).</span></span>

<span data-ttu-id="2e999-107">В сопоставлении рельефов используется смешение нескольких текстур.</span><span class="sxs-lookup"><span data-stu-id="2e999-107">Bump mapping relies on blending multiple textures.</span></span> <span data-ttu-id="2e999-108">Это означает, что устройство должно поддерживать по крайней мере два этапа смешивания. один для схемы выпуклости, а другой для схемы среды.</span><span class="sxs-lookup"><span data-stu-id="2e999-108">This means the device must support at least two blending stages; one for the bump map and another for an environment map.</span></span> <span data-ttu-id="2e999-109">Для применения дополнительной базовой текстурной гиперкарты требуется минимум три этапа смешения текстур, что является наиболее распространенным вариантом.</span><span class="sxs-lookup"><span data-stu-id="2e999-109">A minimum of three texture blending stages are required to apply an additional base texture map, which is the most common case.</span></span> <span data-ttu-id="2e999-110">На следующей диаграмме показаны связи между базовой текстурой, картой выпуклости и картой среды в каскадном смешении текстур.</span><span class="sxs-lookup"><span data-stu-id="2e999-110">The following diagram shows the relationships between the base texture, the bump map, and the environment map in the texture blending cascade.</span></span>

![Диаграмма каскадного смешения текстур](images/bumpmap-tcascade.png)

<span data-ttu-id="2e999-112">Необходимо соответствующим образом подготовить этапы текстуры, чтобы включить сопоставление выпуклостей.</span><span class="sxs-lookup"><span data-stu-id="2e999-112">You must prepare the texture stages appropriately to enable bump mapping.</span></span> <span data-ttu-id="2e999-113">В следующих разделах описывается назначение выпуклости и приводятся сведения о том, как его можно использовать в приложениях:</span><span class="sxs-lookup"><span data-stu-id="2e999-113">The following topics introduce bump mapping, and provide details about how you can use it in your applications:</span></span>

-   [<span data-ttu-id="2e999-114">Форматы пикселей выпуклого отображения</span><span class="sxs-lookup"><span data-stu-id="2e999-114">Bump Map Pixel Formats</span></span>](bump-map-pixel-formats.md)
-   [<span data-ttu-id="2e999-115">Формулы сопоставления рельефов</span><span class="sxs-lookup"><span data-stu-id="2e999-115">Bump Mapping Formulas</span></span>](bump-mapping-formulas.md)
-   [<span data-ttu-id="2e999-116">Использование сопоставления выпуклости</span><span class="sxs-lookup"><span data-stu-id="2e999-116">Using Bump Mapping</span></span>](using-bump-mapping.md)

<span data-ttu-id="2e999-117">Direct3D изначально не поддерживает карты высоты; они просто представляют собой удобный формат для хранения и визуализации данных профиля.</span><span class="sxs-lookup"><span data-stu-id="2e999-117">Direct3D does not natively support height maps; they are merely a convenient format in which to store and visualize contour data.</span></span> <span data-ttu-id="2e999-118">Приложение может хранить данные профиля в любом формате или даже создавать карту выпуклости процедур.</span><span class="sxs-lookup"><span data-stu-id="2e999-118">Your application can store contour information in any format, or even generate a procedural bump map.</span></span>

## <a name="related-topics"></a><span data-ttu-id="2e999-119">См. также</span><span class="sxs-lookup"><span data-stu-id="2e999-119">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="2e999-120">Конвейер пикселей</span><span class="sxs-lookup"><span data-stu-id="2e999-120">Pixel Pipeline</span></span>](pixel-pipeline.md)
</dt> </dl>

 

 



