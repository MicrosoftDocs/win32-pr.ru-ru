---
description: Добавление тумана в трехмерную сцену может улучшить реальный уровень, предоставить амбианце или задать настроение, а также скрыть артефакты, которые иногда возникают при появление в представлении удаленных геометрических объектов.
ms.assetid: 42045e96-43aa-4cec-82b5-0b46a7d5097b
title: Туман (Direct3D 9)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 44b9ed234bef0f3dea76baa98390f25e9b2003a6
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/06/2021
ms.locfileid: "105710583"
---
# <a name="fog-direct3d-9"></a><span data-ttu-id="2b22d-103">Туман (Direct3D 9)</span><span class="sxs-lookup"><span data-stu-id="2b22d-103">Fog (Direct3D 9)</span></span>

<span data-ttu-id="2b22d-104">Добавление тумана в трехмерную сцену может улучшить реальный уровень, предоставить амбианце или задать настроение, а также скрыть артефакты, которые иногда возникают при появление в представлении удаленных геометрических объектов.</span><span class="sxs-lookup"><span data-stu-id="2b22d-104">Adding fog to a 3D scene can enhance realism, provide ambiance or set a mood, and obscure artifacts sometimes caused when distant geometry comes into view.</span></span> <span data-ttu-id="2b22d-105">Direct3D поддерживает две модели тумана, пиксельный туман и вершинный туман, каждый из которых имеет свои собственные функции и интерфейс программирования.</span><span class="sxs-lookup"><span data-stu-id="2b22d-105">Direct3D supports two fog models, pixel fog and vertex fog, each with its own features and programming interface.</span></span>

<span data-ttu-id="2b22d-106">По сути, туман реализуется путем смешения цвета объектов в сцене с выбранным цветом тумана на основе глубины объекта в сцене или его расстояния от точки зрения.</span><span class="sxs-lookup"><span data-stu-id="2b22d-106">Essentially, fog is implemented by blending the color of objects in a scene with a chosen fog color based on the depth of an object in a scene or its distance from the viewpoint.</span></span> <span data-ttu-id="2b22d-107">По мере того, как объекты расширяются более отдаленными, их исходный цвет смешивается с выбранным цветом тумана, создавая иллюзию того, что объект все больше скрывается маленькими частицами, плавающими в сцене.</span><span class="sxs-lookup"><span data-stu-id="2b22d-107">As objects grow more distant, their original color blends more and more with the chosen fog color, creating the illusion that the object is being increasingly obscured by tiny particles floating in the scene.</span></span> <span data-ttu-id="2b22d-108">На следующем рисунке показана сцена, отображаемая без тумана, и похожая сцена, визуализированная с поддержкой тумана.</span><span class="sxs-lookup"><span data-stu-id="2b22d-108">The following illustration shows a scene rendered without fog, and a similar scene rendered with fog enabled.</span></span>

![Иллюстрация той же сцены с туманом и без него](images/fogcomp.png)

<span data-ttu-id="2b22d-110">На этом рисунке сцена слева имеет четкий горизонт, помимо которого ни один из пейзажей не виден, несмотря на то, что он будет виден в реальном мире.</span><span class="sxs-lookup"><span data-stu-id="2b22d-110">In this illustration, the scene on the left has a clear horizon, beyond which no scenery is visible, even though it would be visible in the real world.</span></span> <span data-ttu-id="2b22d-111">Сцена справа скрывает горизонт, используя цвет тумана, идентичный цвету фона, что делает многоугольники плавной.</span><span class="sxs-lookup"><span data-stu-id="2b22d-111">The scene on the right obscures the horizon by using a fog color identical to the background color, making polygons appear to fade into the distance.</span></span> <span data-ttu-id="2b22d-112">Объединив дискретные эффекты тумана с помощью художественной сцены, вы можете добавить настроение и сгладить цвет объектов в сцене.</span><span class="sxs-lookup"><span data-stu-id="2b22d-112">By combining discrete fog effects with creative scene design you can add mood and soften the color of objects in a scene.</span></span>

<span data-ttu-id="2b22d-113">Direct3D предоставляет два способа добавления тумана в сцену: пиксельный туман и вершинный туман с именем для применения эффектов тумана.</span><span class="sxs-lookup"><span data-stu-id="2b22d-113">Direct3D provides two ways to add fog to a scene: pixel fog and vertex fog, named for how the fog effects are applied.</span></span> <span data-ttu-id="2b22d-114">Дополнительные сведения см. в разделе [Pixel туман (Direct3D 9)](pixel-fog.md) и [вершинный туман (Direct3D 9)](vertex-fog.md).</span><span class="sxs-lookup"><span data-stu-id="2b22d-114">For details, see [Pixel Fog (Direct3D 9)](pixel-fog.md) and [Vertex Fog (Direct3D 9)](vertex-fog.md).</span></span> <span data-ttu-id="2b22d-115">Вкратце, пиксельный туман (также называемый Table туман) реализован в драйвере устройства, а вершинный туман — в подсистеме освещения Direct3D.</span><span class="sxs-lookup"><span data-stu-id="2b22d-115">In short, pixel fog - also called table fog - is implemented in the device driver and vertex fog is implemented in the Direct3D lighting engine.</span></span> <span data-ttu-id="2b22d-116">Приложение может реализовать туман с шейдером вершин и одновременно при необходимости пиксельный туман.</span><span class="sxs-lookup"><span data-stu-id="2b22d-116">An application can implement fog with a vertex shader, and pixel fog simultaneously if desired.</span></span>

> [!Note]  
> <span data-ttu-id="2b22d-117">Независимо от того, используется ли пиксельный или вершинный туман, приложение должно предоставить соответствующую матрицу проекции, чтобы обеспечить правильное применение эффектов тумана.</span><span class="sxs-lookup"><span data-stu-id="2b22d-117">Regardless of whether you use pixel or vertex fog, your application must provide a compliant projection matrix to ensure that fog effects are properly applied.</span></span> <span data-ttu-id="2b22d-118">Это ограничение применяется даже к приложениям, которые не используют механизм преобразования и освещения Direct3D.</span><span class="sxs-lookup"><span data-stu-id="2b22d-118">This restriction applies even to applications that do not use the Direct3D transformation and lighting engine.</span></span> <span data-ttu-id="2b22d-119">Дополнительные сведения о том, как можно указать соответствующую матрицу, см. в разделе [преобразование проекции (Direct3D 9)](projection-transform.md).</span><span class="sxs-lookup"><span data-stu-id="2b22d-119">For additional details about how you can provide an appropriate matrix, see [Projection Transform (Direct3D 9)](projection-transform.md).</span></span>

 

<span data-ttu-id="2b22d-120">В следующих разделах представлены сведения о тумане и представлена информация об использовании различных функций тумана в приложениях Direct3D.</span><span class="sxs-lookup"><span data-stu-id="2b22d-120">The following topics introduce fog and present information about using various fog features in Direct3D applications.</span></span>

-   [<span data-ttu-id="2b22d-121">Формулы тумана (Direct3D 9)</span><span class="sxs-lookup"><span data-stu-id="2b22d-121">Fog Formulas (Direct3D 9)</span></span>](fog-formulas.md)
-   [<span data-ttu-id="2b22d-122">Параметры тумана (Direct3D 9)</span><span class="sxs-lookup"><span data-stu-id="2b22d-122">Fog Parameters (Direct3D 9)</span></span>](fog-parameters.md)
-   [<span data-ttu-id="2b22d-123">Смешение тумана (Direct3D 9)</span><span class="sxs-lookup"><span data-stu-id="2b22d-123">Fog Blending (Direct3D 9)</span></span>](fog-blending.md)
-   [<span data-ttu-id="2b22d-124">Цвет тумана (Direct3D 9)</span><span class="sxs-lookup"><span data-stu-id="2b22d-124">Fog Color (Direct3D 9)</span></span>](fog-color.md)
-   [<span data-ttu-id="2b22d-125">Вершинный туман (Direct3D 9)</span><span class="sxs-lookup"><span data-stu-id="2b22d-125">Vertex Fog (Direct3D 9)</span></span>](vertex-fog.md)
-   [<span data-ttu-id="2b22d-126">Пиксельный туман (Direct3D 9)</span><span class="sxs-lookup"><span data-stu-id="2b22d-126">Pixel Fog (Direct3D 9)</span></span>](pixel-fog.md)

<span data-ttu-id="2b22d-127">Смешение тумана управляется состояниями отрисовки; Он не является частью программируемого конвейера пикселей.</span><span class="sxs-lookup"><span data-stu-id="2b22d-127">Fog blending is controlled by render states; it is not part of the programmable pixel pipeline.</span></span>

## <a name="related-topics"></a><span data-ttu-id="2b22d-128">См. также</span><span class="sxs-lookup"><span data-stu-id="2b22d-128">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="2b22d-129">Визуализация Direct3D</span><span class="sxs-lookup"><span data-stu-id="2b22d-129">Direct3D Rendering</span></span>](direct3d-rendering.md)
</dt> </dl>

 

 



