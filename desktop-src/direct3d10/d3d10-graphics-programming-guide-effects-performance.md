---
description: Вопросы производительности (Direct3D 10)
ms.assetid: 9f029be5-4ce0-46ca-909b-adaa980398e7
title: Вопросы производительности (Direct3D 10)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0ba2dbe00475efebdb6ff5d772b3eccd6cd4263a
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104072395"
---
# <a name="performance-considerations-direct3d-10"></a><span data-ttu-id="fb97a-103">Вопросы производительности (Direct3D 10)</span><span class="sxs-lookup"><span data-stu-id="fb97a-103">Performance Considerations (Direct3D 10)</span></span>

## <a name="using-effect-pools"></a><span data-ttu-id="fb97a-104">Использование пулов эффектов</span><span class="sxs-lookup"><span data-stu-id="fb97a-104">Using Effect Pools</span></span>

<span data-ttu-id="fb97a-105">Обычно конвейеры отрисовки используют несколько шейдеров для отображения различных типов объектов и специальных эффектов.</span><span class="sxs-lookup"><span data-stu-id="fb97a-105">It is common for rendering pipelines to use many shaders to render different object types and special effects.</span></span> <span data-ttu-id="fb97a-106">Шейдер — это смесь состояний, которые являются общими для всех шейдеров, таких как «мировая матрица» или «светлая», и другого состояния, характерного для каждого построителя текстуры, такого как рассеянный цвет объекта, или вычисление отраженного выделения.</span><span class="sxs-lookup"><span data-stu-id="fb97a-106">The shader are a mixture of states that a common among all the shaders such as a world matrix or a light position, and other state that is specific to each shader such as an object's diffuse color, or specular highlight calculation.</span></span> <span data-ttu-id="fb97a-107">Пул эффектов — это место в памяти для хранения состояния, которое используется во многих шейдерах, а также общие объекты устройств, такие как шейдеры, рендеринг объектов состояния и буферов констант.</span><span class="sxs-lookup"><span data-stu-id="fb97a-107">An effect pool is a place in memory to store state that is used across many shaders, as well as common device objects such as shaders, render state objects and constant buffers.</span></span> <span data-ttu-id="fb97a-108">Повышение производительности приводит к обновлению общего состояния один раз для всех шейдеров, которым требуется это состояние.</span><span class="sxs-lookup"><span data-stu-id="fb97a-108">The performance improvement results from updating the common state once for all the shaders that need that state.</span></span>

<span data-ttu-id="fb97a-109">Пул эффектов — это расположение общей памяти для состояния результата.</span><span class="sxs-lookup"><span data-stu-id="fb97a-109">An effect pool is a shared memory location for effect state.</span></span> <span data-ttu-id="fb97a-110">Пул создается аналогично результату. его можно создать из памяти (или файла или ресурса).</span><span class="sxs-lookup"><span data-stu-id="fb97a-110">A pool is created similarly to an effect; it can be created from memory (or a file or a resource).</span></span> <span data-ttu-id="fb97a-111">Это приводит к двум различным типам эффектов: глобальному эффекту, который не зависит от состояния в другом действии, и от дочернего эффекта, который зависит от состояния в другом действии.</span><span class="sxs-lookup"><span data-stu-id="fb97a-111">This leads to two different types of effects: a global effect that does not depend on state in other effect versus a child effect which depends on state in another effect.</span></span>

<span data-ttu-id="fb97a-112">Вы указываете, является ли результат глобальным (регистром по умолчанию) или дочерним (путем предоставления флага [ \_ \_ \_ дочернего \_ эффекты Compile D3D10](d3d10-effect.md) ) при создании результата.</span><span class="sxs-lookup"><span data-stu-id="fb97a-112">You specify whether an effect is a global effect (the default case) or a child effect (by supplying the [D3D10\_EFFECT\_COMPILE\_CHILD\_EFFECT](d3d10-effect.md) flag) when the effect is created.</span></span> <span data-ttu-id="fb97a-113">Глобальный результат может служить пулом эффектов. дочерний результат не может быть пулом эффектов.</span><span class="sxs-lookup"><span data-stu-id="fb97a-113">A global effect can serve as an effect pool; a child effect cannot be an effect pool.</span></span>

## <a name="related-topics"></a><span data-ttu-id="fb97a-114">См. также</span><span class="sxs-lookup"><span data-stu-id="fb97a-114">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="fb97a-115">Отрисовка результата</span><span class="sxs-lookup"><span data-stu-id="fb97a-115">Rendering an Effect</span></span>](d3d10-graphics-programming-guide-effects-render.md)
</dt> <dt>

[<span data-ttu-id="fb97a-116">Эффекты (Direct3D 10)</span><span class="sxs-lookup"><span data-stu-id="fb97a-116">Effects (Direct3D 10)</span></span>](d3d10-graphics-programming-guide-effects.md)
</dt> </dl>

 

 



