---
title: Методы Креатетрансформеджеометри ID2D1Factory (D2d1. h)
description: Преобразует указанную геометрию и сохраняет результат в виде объекта ID2D1TransformedGeometry.
ms.assetid: 71f26200-0f35-49d7-951d-2962768d16bc
keywords:
- Методы Креатетрансформеджеометри Direct2D
topic_type:
- apiref
api_location:
- D2d1.dll
api_type:
- DllExport
ms.date: 07/02/2019
ms.topic: reference
ms.openlocfilehash: 5da3b548c3118209c915714e03fe9e4061c77e96
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105675103"
---
# <a name="id2d1factorycreatetransformedgeometry-methods"></a><span data-ttu-id="d925b-104">Методы ID2D1Factory:: Креатетрансформеджеометри</span><span class="sxs-lookup"><span data-stu-id="d925b-104">ID2D1Factory::CreateTransformedGeometry methods</span></span>

<span data-ttu-id="d925b-105">Преобразует указанную геометрию и сохраняет результат в виде объекта [**ID2D1TransformedGeometry**](/previous-versions/windows/desktop/legacy/dd371304(v=vs.85)) .</span><span class="sxs-lookup"><span data-stu-id="d925b-105">Transforms the specified geometry and stores the result as an [**ID2D1TransformedGeometry**](/previous-versions/windows/desktop/legacy/dd371304(v=vs.85)) object.</span></span>

### <a name="overload-list"></a><span data-ttu-id="d925b-106">Список перегрузок</span><span class="sxs-lookup"><span data-stu-id="d925b-106">Overload list</span></span>



| <span data-ttu-id="d925b-107">Метод</span><span class="sxs-lookup"><span data-stu-id="d925b-107">Method</span></span>                                                                                                                                                                                                                  | <span data-ttu-id="d925b-108">Описание</span><span class="sxs-lookup"><span data-stu-id="d925b-108">Description</span></span>                                                                                                                                    |
|:------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:-----------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="d925b-109">[**Креатетрансформеджеометри (ID2D1Geometry \* , \_ Матрица D2D \_ 3X2 \_ F \* , ID2D1TransformedGeometry \* \* )**](/previous-versions/windows/desktop/legacy/dd371304(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="d925b-109">[**CreateTransformedGeometry(ID2D1Geometry\*,D2D\_MATRIX\_3X2\_F\*,ID2D1TransformedGeometry\*\*)**](/previous-versions/windows/desktop/legacy/dd371304(v=vs.85))</span></span> | <span data-ttu-id="d925b-110">Преобразует указанную геометрию и сохраняет результат в виде объекта [**ID2D1TransformedGeometry**](/previous-versions/windows/desktop/legacy/dd371304(v=vs.85)) .</span><span class="sxs-lookup"><span data-stu-id="d925b-110">Transforms the specified geometry and stores the result as an [**ID2D1TransformedGeometry**](/previous-versions/windows/desktop/legacy/dd371304(v=vs.85)) object.</span></span> <br/> |
| <span data-ttu-id="d925b-111">[**Креатетрансформеджеометри (ID2D1Geometry \* , \_ Матрица D2D \_ 3X2 \_ F&, ID2D1TransformedGeometry \* \* )**](/windows/win32/api/d2d1/nf-d2d1-id2d1factory-createtransformedgeometry(id2d1geometry_constd2d1_matrix_3x2_f__id2d1transformedgeometry))</span><span class="sxs-lookup"><span data-stu-id="d925b-111">[**CreateTransformedGeometry(ID2D1Geometry\*,D2D\_MATRIX\_3X2\_F&,ID2D1TransformedGeometry\*\*)**](/windows/win32/api/d2d1/nf-d2d1-id2d1factory-createtransformedgeometry(id2d1geometry_constd2d1_matrix_3x2_f__id2d1transformedgeometry))</span></span>  | <span data-ttu-id="d925b-112">Преобразует указанную геометрию и сохраняет результат в виде объекта [**ID2D1TransformedGeometry**](/previous-versions/windows/desktop/legacy/dd371304(v=vs.85)) .</span><span class="sxs-lookup"><span data-stu-id="d925b-112">Transforms the specified geometry and stores the result as an [**ID2D1TransformedGeometry**](/previous-versions/windows/desktop/legacy/dd371304(v=vs.85)) object.</span></span> <br/> |



## <a name="remarks"></a><span data-ttu-id="d925b-113">Комментарии</span><span class="sxs-lookup"><span data-stu-id="d925b-113">Remarks</span></span>

<span data-ttu-id="d925b-114">Как и другие ресурсы, преобразованная геометрия наследует пространство ресурсов и политику потоков фабрики, создавшей ее.</span><span class="sxs-lookup"><span data-stu-id="d925b-114">Like other resources, a transformed geometry inherits the resource space and threading policy of the factory that created it.</span></span> <span data-ttu-id="d925b-115">Этот объект является неизменяемым.</span><span class="sxs-lookup"><span data-stu-id="d925b-115">This object is immutable.</span></span>

<span data-ttu-id="d925b-116">При обводке преобразованной геометрии с помощью метода [**DrawGeometry**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-drawgeometry) на толщину штриха не влияет преобразование, применяемое к геометрии.</span><span class="sxs-lookup"><span data-stu-id="d925b-116">When stroking a transformed geometry with the [**DrawGeometry**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-drawgeometry) method, the stroke width is not affected by the transform applied to the geometry.</span></span> <span data-ttu-id="d925b-117">Ширина штриха зависит только от универсального преобразования.</span><span class="sxs-lookup"><span data-stu-id="d925b-117">The stroke width is only affected by the world transform.</span></span>

## <a name="examples"></a><span data-ttu-id="d925b-118">Примеры</span><span class="sxs-lookup"><span data-stu-id="d925b-118">Examples</span></span>

<span data-ttu-id="d925b-119">В следующем примере создается [**ID2D1RectangleGeometry**](/windows/win32/api/d2d1/nf-d2d1-id2d1factory-createrectanglegeometry(constd2d1_rect_f_id2d1rectanglegeometry)), а затем рисуется без его преобразования.</span><span class="sxs-lookup"><span data-stu-id="d925b-119">The following example creates an [**ID2D1RectangleGeometry**](/windows/win32/api/d2d1/nf-d2d1-id2d1factory-createrectanglegeometry(constd2d1_rect_f_id2d1rectanglegeometry)), then draws it without transforming it.</span></span> <span data-ttu-id="d925b-120">Он создает выходные данные, показанные на следующем рисунке.</span><span class="sxs-lookup"><span data-stu-id="d925b-120">It produces the output shown in the following illustration.</span></span>

![Иллюстрация прямоугольника](images/transformedgeometry2-step1.png)


```C++
hr = m_pD2DFactory->CreateRectangleGeometry(
    D2D1::RectF(150.f, 150.f, 200.f, 200.f),
    &m_pRectangleGeometry
    );
```



<span data-ttu-id="d925b-122">В следующем примере используется целевой объект отрисовки для масштабирования геометрии по коэффициенту 3, после чего рисуется.</span><span class="sxs-lookup"><span data-stu-id="d925b-122">The next example uses the render target to scale the geometry by a factor of 3, then draws it.</span></span> <span data-ttu-id="d925b-123">На следующем рисунке показан результат рисования прямоугольника без преобразования и преобразования. Обратите внимание, что после преобразования штрих становится толще, несмотря на то, что толщина штриха равна 1.</span><span class="sxs-lookup"><span data-stu-id="d925b-123">The following illustration shows the result of drawing the rectangle without the transform and with the transform; notices that the stroke is thicker after the transform, even though the stroke thickness is 1.</span></span>

![Рисунок меньшего прямоугольника внутри более крупного прямоугольника с толстой обводкой](images/transformedgeometry2-step2.png)


```C++
// Transform the render target, then draw the rectangle geometry again.
m_pRenderTarget->SetTransform(
    D2D1::Matrix3x2F::Scale(
        D2D1::SizeF(3.f, 3.f),
        D2D1::Point2F(175.f, 175.f))
    );

m_pRenderTarget->DrawGeometry(m_pRectangleGeometry, m_pBlackBrush, 1);
```



<span data-ttu-id="d925b-125">В следующем примере используется метод **креатетрансформеджеометри** для масштабирования геометрии по коэффициенту 3, после чего рисуется.</span><span class="sxs-lookup"><span data-stu-id="d925b-125">The next example uses the **CreateTransformedGeometry** method to scale the geometry by a factor of 3, then draws it.</span></span> <span data-ttu-id="d925b-126">Он создает выходные данные, показанные на следующем рисунке.</span><span class="sxs-lookup"><span data-stu-id="d925b-126">It produces the output shown in the following illustration.</span></span> <span data-ttu-id="d925b-127">Обратите внимание, что, хотя размер прямоугольника больше, его штрих не увеличился.</span><span class="sxs-lookup"><span data-stu-id="d925b-127">Notice that, although the rectangle is larger, its stroke hasn't increased.</span></span>

![Иллюстрация прямоугольника меньшего размера внутри более крупного прямоугольника с одинаковой обводкой](images/transformedgeometry2-step3.png)


```C++
 // Create a geometry that is a scaled version
 // of m_pRectangleGeometry.
 // The new geometry is scaled by a factory of 3
 // from the center of the geometry, (35, 35).

 hr = m_pD2DFactory->CreateTransformedGeometry(
     m_pRectangleGeometry,
     D2D1::Matrix3x2F::Scale(
         D2D1::SizeF(3.f, 3.f),
         D2D1::Point2F(175.f, 175.f)),
     &m_pTransformedGeometry
     );


// Replace the previous render target transform.
m_pRenderTarget->SetTransform(D2D1::Matrix3x2F::Identity());

// Draw the transformed geometry.
m_pRenderTarget->DrawGeometry(m_pTransformedGeometry, m_pBlackBrush, 1);
```





## <a name="requirements"></a><span data-ttu-id="d925b-129">Требования</span><span class="sxs-lookup"><span data-stu-id="d925b-129">Requirements</span></span>



| <span data-ttu-id="d925b-130">Требование</span><span class="sxs-lookup"><span data-stu-id="d925b-130">Requirement</span></span> | <span data-ttu-id="d925b-131">Значение</span><span class="sxs-lookup"><span data-stu-id="d925b-131">Value</span></span> |
|--------------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="d925b-132">Header</span><span class="sxs-lookup"><span data-stu-id="d925b-132">Header</span></span><br/>  | <dl> <span data-ttu-id="d925b-133"><dt>D2d1. h</dt></span><span class="sxs-lookup"><span data-stu-id="d925b-133"><dt>D2d1.h</dt></span></span> </dl>   |
| <span data-ttu-id="d925b-134">Библиотека</span><span class="sxs-lookup"><span data-stu-id="d925b-134">Library</span></span><br/> | <dl> <span data-ttu-id="d925b-135"><dt>D2d1. lib</dt></span><span class="sxs-lookup"><span data-stu-id="d925b-135"><dt>D2d1.lib</dt></span></span> </dl> |
| <span data-ttu-id="d925b-136">DLL</span><span class="sxs-lookup"><span data-stu-id="d925b-136">DLL</span></span><br/>     | <dl> <span data-ttu-id="d925b-137"><dt>D2d1.dll</dt></span><span class="sxs-lookup"><span data-stu-id="d925b-137"><dt>D2d1.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="d925b-138">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="d925b-138">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d925b-139">**ID2D1Factory**</span><span class="sxs-lookup"><span data-stu-id="d925b-139">**ID2D1Factory**</span></span>](/windows/win32/api/d2d1/nn-d2d1-id2d1factory)
</dt> </dl>
