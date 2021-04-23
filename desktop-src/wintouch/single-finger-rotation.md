---
title: Вращение Single-Finger
description: В этом разделе объясняется, как повернуть объект с помощью точки вращения.
ms.assetid: b9c19009-8ac0-4168-bf26-393280fc589f
keywords:
- Касание Windows, поворот
- Касание Windows, манипуляции
- Касание Windows, однонаправленный поворот на один палец
- Касание Windows, поворот точек вращения
- манипуляции, вращение
- поворот, точки вращения
- вращение, одиночный палец
- жесты, вращение одним пальцем
- вращение одним пальцем
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 93d74263f502749e2aaf942c4bbec5aa0a284e76
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/16/2019
ms.locfileid: "103887975"
---
# <a name="single-finger-rotation"></a><span data-ttu-id="3ac84-112">Вращение Single-Finger</span><span class="sxs-lookup"><span data-stu-id="3ac84-112">Single-Finger Rotation</span></span>

<span data-ttu-id="3ac84-113">В этом разделе объясняется, как повернуть объект с помощью точки вращения.</span><span class="sxs-lookup"><span data-stu-id="3ac84-113">This section explains how to rotate an object using a pivot point.</span></span>

<span data-ttu-id="3ac84-114">На следующем рисунке показан поворот с одним пальцем.</span><span class="sxs-lookup"><span data-stu-id="3ac84-114">The following image illustrates single-finger rotation.</span></span>

![Иллюстрация, демонстрирующая два типа поворота одного пальца: вокруг центра или вокруг края](images/sfrotation.png)

<span data-ttu-id="3ac84-116">В примере а объект поворачивается вокруг центральной точки объекта с помощью жеста поворота.</span><span class="sxs-lookup"><span data-stu-id="3ac84-116">In example A, the object is rotated around the center point of the object by using the rotation gesture.</span></span> <span data-ttu-id="3ac84-117">В примере б объект поворачивается путем перемещения одного пальца вокруг края объекта.</span><span class="sxs-lookup"><span data-stu-id="3ac84-117">In example B, the object is rotated by moving a single finger around the edge of the object.</span></span> <span data-ttu-id="3ac84-118">Обработчик манипуляции включает этот поворот, используя значения «точка вращения» и «сведения о радиусе».</span><span class="sxs-lookup"><span data-stu-id="3ac84-118">The manipulation processor enables this rotation by using pivot point and pivot radius values.</span></span> <span data-ttu-id="3ac84-119">На следующем рисунке показаны компоненты ротации с одним пальцем.</span><span class="sxs-lookup"><span data-stu-id="3ac84-119">The following image illustrates the components of single-finger rotation.</span></span>

![Иллюстрация, демонстрирующая компоненты однопальцного вращения: пивотпоинткс, пивотпоинти и пивотрадиус](images/sfrotation-components.png)

<span data-ttu-id="3ac84-121">После установки значений [**пивотпоинткс**](/windows/desktop/api/manipulations/nf-manipulations-imanipulationprocessor-get_pivotpointx), [**пивотпоинти**](/windows/desktop/api/manipulations/nf-manipulations-imanipulationprocessor-get_pivotpointy)и [**пивотрадиус**](/windows/desktop/api/manipulations/nf-manipulations-imanipulationprocessor-get_pivotradius) в последующих сообщениях преобразования будет использоваться поворот.</span><span class="sxs-lookup"><span data-stu-id="3ac84-121">After you set the [**PivotPointX**](/windows/desktop/api/manipulations/nf-manipulations-imanipulationprocessor-get_pivotpointx), [**PivotPointY**](/windows/desktop/api/manipulations/nf-manipulations-imanipulationprocessor-get_pivotpointy), and [**PivotRadius**](/windows/desktop/api/manipulations/nf-manipulations-imanipulationprocessor-get_pivotradius) values, subsequent translation messages will incorporate rotation.</span></span> <span data-ttu-id="3ac84-122">Чем больше значение радиуса вращения, тем больше изменений в x и y должно быть поворот объекта.</span><span class="sxs-lookup"><span data-stu-id="3ac84-122">The larger the pivot radius, the greater the change in x and y must be to rotate the object.</span></span> <span data-ttu-id="3ac84-123">В следующем коде показано, как можно задать эти значения в обработчике манипуляции.</span><span class="sxs-lookup"><span data-stu-id="3ac84-123">The following code shows how these values could be set in the manipulation processor.</span></span>


```C++
HRESULT STDMETHODCALLTYPE CManipulationEventSink::ManipulationDelta( 
    /* [in] */ FLOAT x,
    /* [in] */ FLOAT y)
{
    m_cStartedEventCount ++;

    // Set the pivot point to the object's center and then set the radius 
    // to the distance from the center to the edge of the object.
    m_pManip->put_PivotPointX(m_objectRef->xPos);
    m_pManip->put_PivotPointY(m_objectRef->yPos);
    
    float fPivotRadius = (FLOAT)(sqrt(pow(m_dObj->get_Width()/2, 2) + pow(m_dObj->get_Height()/2, 2)))*0.4f;
    
    m_pManip->put_PivotRadius(fPivotRadius);
  

    return S_OK;
}    
     
```



<span data-ttu-id="3ac84-124">В предыдущем примере расстояние до края объекта (с масштабированием до 40 процентов) используется в качестве радиуса сведения.</span><span class="sxs-lookup"><span data-stu-id="3ac84-124">In the previous example, the distance to the edge of the object (scaled to 40 percent) is used as the pivot radius.</span></span> <span data-ttu-id="3ac84-125">Поскольку учитывается размер объекта, это вычисление допустимо для каждого разностного объекта.</span><span class="sxs-lookup"><span data-stu-id="3ac84-125">Because the object size is taken into consideration, this calculation is valid for every object delta.</span></span> <span data-ttu-id="3ac84-126">По мере масштабирования объекта радиус вращения растет.</span><span class="sxs-lookup"><span data-stu-id="3ac84-126">As the object scales, the pivot radius grows.</span></span> <span data-ttu-id="3ac84-127">Это значение и значения Center x и y объекта передаются обработчику манипуляции для поворота объекта вокруг точки вращения.</span><span class="sxs-lookup"><span data-stu-id="3ac84-127">This value and the object's center x and y values are passed to the manipulation processor to rotate the object around the pivot point.</span></span>

> [!Note]  
> <span data-ttu-id="3ac84-128">Значение [**пивотрадиус**](/windows/desktop/api/manipulations/nf-manipulations-imanipulationprocessor-get_pivotradius) никогда не должно быть между 0,0 и 1,0.</span><span class="sxs-lookup"><span data-stu-id="3ac84-128">The [**PivotRadius**](/windows/desktop/api/manipulations/nf-manipulations-imanipulationprocessor-get_pivotradius) value should never be between 0.0 and 1.0.</span></span>

 

## <a name="related-topics"></a><span data-ttu-id="3ac84-129">См. также</span><span class="sxs-lookup"><span data-stu-id="3ac84-129">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="3ac84-130">Манипуляции</span><span class="sxs-lookup"><span data-stu-id="3ac84-130">Manipulations</span></span>](getting-started-with-manipulations.md)
</dt> <dt>

[<span data-ttu-id="3ac84-131">**пивотрадиус**</span><span class="sxs-lookup"><span data-stu-id="3ac84-131">**PivotRadius**</span></span>](/windows/desktop/api/manipulations/nf-manipulations-imanipulationprocessor-get_pivotradius)
</dt> <dt>

[<span data-ttu-id="3ac84-132">**пивотпоинткс**</span><span class="sxs-lookup"><span data-stu-id="3ac84-132">**PivotPointX**</span></span>](/windows/desktop/api/manipulations/nf-manipulations-imanipulationprocessor-get_pivotpointx)
</dt> <dt>

[<span data-ttu-id="3ac84-133">**пивотпоинти**</span><span class="sxs-lookup"><span data-stu-id="3ac84-133">**PivotPointY**</span></span>](/windows/desktop/api/manipulations/nf-manipulations-imanipulationprocessor-get_pivotpointy)
</dt> </dl>

 

 




