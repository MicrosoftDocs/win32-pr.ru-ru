---
description: Во время отрисовки конвейер интерполирует данные вершины в каждом треугольнике.
ms.assetid: 6fa05e56-c4cd-4623-abe9-2b1c8bbc644b
title: Интерполяция треугольника (Direct3D 9)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 405cbecd6123145d412a3e7f58f727bdf5b5a3e8
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/06/2021
ms.locfileid: "105701157"
---
# <a name="triangle-interpolation-direct3d-9"></a><span data-ttu-id="b71d1-103">Интерполяция треугольника (Direct3D 9)</span><span class="sxs-lookup"><span data-stu-id="b71d1-103">Triangle Interpolation (Direct3D 9)</span></span>

<span data-ttu-id="b71d1-104">Во время отрисовки конвейер интерполирует данные вершины в каждом треугольнике.</span><span class="sxs-lookup"><span data-stu-id="b71d1-104">During rendering, the pipeline interpolates vertex data across each triangle.</span></span> <span data-ttu-id="b71d1-105">Данные вершин могут быть широким набором данных и могут включать (но не ограничены): рассеянный цвет, отражающий цвет, рассеяние альфа-канала (непрозрачность треугольника), отражающая альфа-фактор и коэффициент тумана (взятый из отражения альфа для фиксированного конвейера вершин и из регистра тумана для программируемого конвейера).</span><span class="sxs-lookup"><span data-stu-id="b71d1-105">Vertex data can be a broad variety of data and can include (but is not limited to): diffuse color, specular color, diffuse alpha (triangle opacity), specular alpha, and a fog factor (taken from specular alpha for fixed function vertex pipeline and from fog register for programmable vertex pipeline).</span></span> <span data-ttu-id="b71d1-106">Данные вершин определяются с помощью [объявления вершины (Direct3D 9)](vertex-declaration.md).</span><span class="sxs-lookup"><span data-stu-id="b71d1-106">The vertex data is defined by the [Vertex Declaration (Direct3D 9)](vertex-declaration.md).</span></span>

<span data-ttu-id="b71d1-107">Для некоторых данных вершин интерполяция зависит от текущего режима заливки, как показано в следующей таблице.</span><span class="sxs-lookup"><span data-stu-id="b71d1-107">For some vertex data, the interpolation is dependent on the current shading mode, as shown in the following table.</span></span>



| <span data-ttu-id="b71d1-108">Режим затенения</span><span class="sxs-lookup"><span data-stu-id="b71d1-108">Shading mode</span></span> | <span data-ttu-id="b71d1-109">Описание</span><span class="sxs-lookup"><span data-stu-id="b71d1-109">Description</span></span>                                                                                                                                                                 |
|--------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="b71d1-110">плоский</span><span class="sxs-lookup"><span data-stu-id="b71d1-110">Flat</span></span>         | <span data-ttu-id="b71d1-111">В режиме плоского затенения интерполируется только коэффициент затуманивания.</span><span class="sxs-lookup"><span data-stu-id="b71d1-111">Only the fog factor is interpolated in flat shade mode.</span></span> <span data-ttu-id="b71d1-112">Для всех остальных интерполированных значений цвет первой вершины в треугольнике применяется ко всей поверхности.</span><span class="sxs-lookup"><span data-stu-id="b71d1-112">For all other interpolated values, the color of the first vertex in the triangle is applied across the entire face.</span></span> |
| <span data-ttu-id="b71d1-113">Затенение по методу Гуро</span><span class="sxs-lookup"><span data-stu-id="b71d1-113">Gouraud</span></span>      | <span data-ttu-id="b71d1-114">Линейная интерполяция выполняется между всеми тремя вершинами.</span><span class="sxs-lookup"><span data-stu-id="b71d1-114">Linear interpolation is performed between all three vertices.</span></span>                                                                                                               |



 

<span data-ttu-id="b71d1-115">Рассеянный цвет и отражающий цвет обрабатываются по-разному в зависимости от цветовой модели.</span><span class="sxs-lookup"><span data-stu-id="b71d1-115">The diffuse color and specular color are treated differently, depending on the color model.</span></span> <span data-ttu-id="b71d1-116">В цветовой модели RGB система использует при интерполяции компоненты красного, зеленого и синего цветов.</span><span class="sxs-lookup"><span data-stu-id="b71d1-116">In the RGB color model, the system uses the red, green, and blue color components in the interpolation.</span></span>

<span data-ttu-id="b71d1-117">Альфа-компонент цвета рассматривается как отдельное интерполированное значение, так как драйверы устройств могут реализовывать прозрачность двумя способами: путем смешивания текстур или путем создания контурных изображений ("рисования пунктиром").</span><span class="sxs-lookup"><span data-stu-id="b71d1-117">The alpha component of a color is treated as a separate interpolated value because device drivers can implement transparency in two different ways: by using texture blending or by using stippling.</span></span>

<span data-ttu-id="b71d1-118">Используйте элемент Шадекапс структуры [**D3DCAPS9**](/windows/desktop/api/D3D9Caps/ns-d3d9caps-d3dcaps9) , чтобы определить, какие формы интерполяции поддерживает текущий драйвер устройства.</span><span class="sxs-lookup"><span data-stu-id="b71d1-118">Use the ShadeCaps member of the [**D3DCAPS9**](/windows/desktop/api/D3D9Caps/ns-d3d9caps-d3dcaps9) structure to determine what forms of interpolation the current device driver supports.</span></span>

## <a name="related-topics"></a><span data-ttu-id="b71d1-119">См. также</span><span class="sxs-lookup"><span data-stu-id="b71d1-119">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="b71d1-120">Системы координат и геометрия</span><span class="sxs-lookup"><span data-stu-id="b71d1-120">Coordinate Systems and Geometry</span></span>](coordinate-systems-and-geometry.md)
</dt> </dl>

 

 



