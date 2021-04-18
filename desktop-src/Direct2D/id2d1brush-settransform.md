---
title: Методы Сеттрансформ ID2D1Brush (D2d1 \_ 1. h)
description: Задает преобразование, применяемое к кисти.
ms.assetid: 57afadc1-88c9-4a5b-a83f-63c4c69182a7
keywords:
- Методы Сеттрансформ Direct2D
topic_type:
- apiref
api_location:
- D2d1.dll
api_type:
- DllExport
ms.date: 07/02/2019
ms.topic: reference
ms.openlocfilehash: 89d0da76368fac2d2335cabda1f6d0a6130b499f
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105679979"
---
# <a name="id2d1brushsettransform-methods"></a><span data-ttu-id="6c35a-104">Методы ID2D1Brush:: Сеттрансформ</span><span class="sxs-lookup"><span data-stu-id="6c35a-104">ID2D1Brush::SetTransform methods</span></span>

<span data-ttu-id="6c35a-105">Задает преобразование, применяемое к кисти.</span><span class="sxs-lookup"><span data-stu-id="6c35a-105">Sets the transformation applied to the brush.</span></span>

### <a name="overload-list"></a><span data-ttu-id="6c35a-106">Список перегрузок</span><span class="sxs-lookup"><span data-stu-id="6c35a-106">Overload list</span></span>



| <span data-ttu-id="6c35a-107">Метод</span><span class="sxs-lookup"><span data-stu-id="6c35a-107">Method</span></span>                                                                                       | <span data-ttu-id="6c35a-108">Описание</span><span class="sxs-lookup"><span data-stu-id="6c35a-108">Description</span></span>                                              |
|:---------------------------------------------------------------------------------------------|:---------------------------------------------------------|
| <span data-ttu-id="6c35a-109">[**Сеттрансформ (D2D1 \_ Matrix \_ 3X2 \_ F&)**](/windows/win32/api/d2d1/nf-d2d1-id2d1brush-settransform(constd2d1_matrix_3x2_f_))</span><span class="sxs-lookup"><span data-stu-id="6c35a-109">[**SetTransform(D2D1\_MATRIX\_3X2\_F&)**](/windows/win32/api/d2d1/nf-d2d1-id2d1brush-settransform(constd2d1_matrix_3x2_f_))</span></span>  | <span data-ttu-id="6c35a-110">Задает преобразование, применяемое к кисти.</span><span class="sxs-lookup"><span data-stu-id="6c35a-110">Sets the transformation applied to the brush.</span></span><br/> |
| <span data-ttu-id="6c35a-111">[**Сеттрансформ (D2D1 \_ Matrix \_ 3X2 \_ F \* )**](/windows/win32/api/d2d1/nf-d2d1-id2d1brush-settransform(constd2d1_matrix_3x2_f))</span><span class="sxs-lookup"><span data-stu-id="6c35a-111">[**SetTransform(D2D1\_MATRIX\_3X2\_F\*)**](/windows/win32/api/d2d1/nf-d2d1-id2d1brush-settransform(constd2d1_matrix_3x2_f))</span></span> | <span data-ttu-id="6c35a-112">Задает преобразование, применяемое к кисти.</span><span class="sxs-lookup"><span data-stu-id="6c35a-112">Sets the transformation applied to the brush.</span></span><br/> |



## <a name="remarks"></a><span data-ttu-id="6c35a-113">Комментарии</span><span class="sxs-lookup"><span data-stu-id="6c35a-113">Remarks</span></span>

<span data-ttu-id="6c35a-114">При рисовании с помощью кисти она рисуется в пространстве координат целевого объекта отрисовки.</span><span class="sxs-lookup"><span data-stu-id="6c35a-114">When you paint with a brush, it paints in the coordinate space of the render target.</span></span> <span data-ttu-id="6c35a-115">Кисти не размещаются автоматически, чтобы они совпадали с закрашиваемым объектом; по умолчанию они начинают рисовать в источнике (0, 0) целевого объекта отрисовки.</span><span class="sxs-lookup"><span data-stu-id="6c35a-115">Brushes do not automatically position themselves to align with the object being painted; by default, they begin painting at the origin (0, 0) of the render target.</span></span>

<span data-ttu-id="6c35a-116">Можно «переместить» градиент, определенный [**ID2D1LinearGradientBrush**](/windows/win32/api/d2d1/nn-d2d1-id2d1lineargradientbrush) , в целевую область, задав его начальную и конечную точки.</span><span class="sxs-lookup"><span data-stu-id="6c35a-116">You can "move" the gradient defined by an [**ID2D1LinearGradientBrush**](/windows/win32/api/d2d1/nn-d2d1-id2d1lineargradientbrush) to a target area by setting its start point and end point.</span></span> <span data-ttu-id="6c35a-117">Аналогичным образом можно переместить градиент, определенный [**ID2D1RadialGradientBrush**](/windows/win32/api/d2d1/nn-d2d1-id2d1radialgradientbrush) , изменив его центр и радиусы.</span><span class="sxs-lookup"><span data-stu-id="6c35a-117">Likewise, you can move the gradient defined by an [**ID2D1RadialGradientBrush**](/windows/win32/api/d2d1/nn-d2d1-id2d1radialgradientbrush) by changing its center and radii.</span></span>

<span data-ttu-id="6c35a-118">Чтобы согласовать содержимое [**ID2D1BitmapBrush**](/windows/win32/api/d2d1/nn-d2d1-id2d1bitmapbrush) с закрашиваемой областью, можно использовать метод **сеттрансформ** для преобразования растрового изображения в нужное место.</span><span class="sxs-lookup"><span data-stu-id="6c35a-118">To align the content of an [**ID2D1BitmapBrush**](/windows/win32/api/d2d1/nn-d2d1-id2d1bitmapbrush) to the area being painted, you can use the **SetTransform** method to translate the bitmap to the desired location.</span></span> <span data-ttu-id="6c35a-119">Это преобразование влияет только на кисть. Он не влияет на содержимое, рисуемое целевым объектом рендеринга.</span><span class="sxs-lookup"><span data-stu-id="6c35a-119">This transform only affects the brush; it does not affect any other content drawn by the render target.</span></span>

<span data-ttu-id="6c35a-120">На следующих иллюстрациях показан результат использования [**ID2D1BitmapBrush**](/windows/win32/api/d2d1/nn-d2d1-id2d1bitmapbrush) для заполнения прямоугольника, расположенного в (100, 100).</span><span class="sxs-lookup"><span data-stu-id="6c35a-120">The following illustrations show the effect of using an [**ID2D1BitmapBrush**](/windows/win32/api/d2d1/nn-d2d1-id2d1bitmapbrush) to fill a rectangle located at (100, 100).</span></span> <span data-ttu-id="6c35a-121">На рисунке слева показан результат заполнения прямоугольника без преобразования кисти: точечный рисунок отображается в источнике целевого объекта рендеринга.</span><span class="sxs-lookup"><span data-stu-id="6c35a-121">The illustration on the left illustration shows the result of filling the rectangle without transforming the brush: the bitmap is drawn at the render target's origin.</span></span> <span data-ttu-id="6c35a-122">В результате в прямоугольнике появляется только часть точечного рисунка.</span><span class="sxs-lookup"><span data-stu-id="6c35a-122">As a result, only a portion of the bitmap appears in the rectangle.</span></span>

<span data-ttu-id="6c35a-123">На рисунке справа показан результат преобразования [**ID2D1BitmapBrush**](/windows/win32/api/d2d1/nn-d2d1-id2d1bitmapbrush) , чтобы его содержимое было смещено на 50 пикселей вправо и 50 пикселей вниз.</span><span class="sxs-lookup"><span data-stu-id="6c35a-123">The illustration on the right shows the result of transforming the [**ID2D1BitmapBrush**](/windows/win32/api/d2d1/nn-d2d1-id2d1bitmapbrush) so that its content is shifted 50 pixels to the right and 50 pixels down.</span></span> <span data-ttu-id="6c35a-124">Теперь точечный рисунок заполняет прямоугольник.</span><span class="sxs-lookup"><span data-stu-id="6c35a-124">The bitmap now fills the rectangle.</span></span>

![Иллюстрация двух квадратов, одна закрашена растровым изображением без преобразованной кисти, а другая — преобразованной кистью](images/brushes-ovw-transform.png)

## <a name="examples"></a><span data-ttu-id="6c35a-126">Примеры</span><span class="sxs-lookup"><span data-stu-id="6c35a-126">Examples</span></span>

<span data-ttu-id="6c35a-127">В следующем примере кода показано, как создать преобразование, показанное на схеме справа на предыдущем рисунке.</span><span class="sxs-lookup"><span data-stu-id="6c35a-127">The following code examples show how to create the transformation shown in the right diagram in the preceding illustration.</span></span> <span data-ttu-id="6c35a-128">Сначала примените перевод к [**ID2D1BitmapBrush**](/windows/win32/api/d2d1/nn-d2d1-id2d1bitmapbrush), переместив кисть 50 пикселей вправо вдоль оси x и 50 пикселей вниз по оси y.</span><span class="sxs-lookup"><span data-stu-id="6c35a-128">First apply a translation to the [**ID2D1BitmapBrush**](/windows/win32/api/d2d1/nn-d2d1-id2d1bitmapbrush), moving the brush 50 pixels right along the x-axis and 50 pixels down along the y-axis.</span></span> <span data-ttu-id="6c35a-129">Затем используйте **ID2D1BitmapBrush** для заполнения прямоугольника с верхним левым углом в (100, 100) и правом нижнем углу в (200, 200).</span><span class="sxs-lookup"><span data-stu-id="6c35a-129">Then use the **ID2D1BitmapBrush** to fill the rectangle that has the upper-left corner at (100, 100) and the lower-right corner at (200, 200).</span></span>


```C++
// Create the bitmap to be used by the bitmap brush.
if (SUCCEEDED(hr))
{
    hr = LoadResourceBitmap(
        m_pRenderTarget,
        m_pWICFactory,
        L"FERN",
        L"Image",
        &amp;m_pBitmap
        );
   
}
```




```C++
if (SUCCEEDED(hr))
{
    hr = m_pRenderTarget->CreateBitmapBrush(
        m_pBitmap,
        &amp;m_pBitmapBrush
        );
}
```




```C++
D2D1_RECT_F rcTransformedBrushRect = D2D1::RectF(100, 100, 200, 200);



 // Demonstrate the effect of transforming a bitmap brush.
 m_pBitmapBrush->SetTransform(
     D2D1::Matrix3x2F::Translation(D2D1::SizeF(50,50))
     );

 // To see the content of the rcTransformedBrushRect, comment
 // out this statement.
 m_pRenderTarget->FillRectangle(
     &rcTransformedBrushRect, 
     m_pBitmapBrush
     );

 m_pRenderTarget-&gt;DrawRectangle(rcTransformedBrushRect, m_pBlackBrush, 1, NULL);
```





## <a name="requirements"></a><span data-ttu-id="6c35a-130">Требования</span><span class="sxs-lookup"><span data-stu-id="6c35a-130">Requirements</span></span>



| <span data-ttu-id="6c35a-131">Требование</span><span class="sxs-lookup"><span data-stu-id="6c35a-131">Requirement</span></span> | <span data-ttu-id="6c35a-132">Значение</span><span class="sxs-lookup"><span data-stu-id="6c35a-132">Value</span></span> |
|--------------------|-------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="6c35a-133">Header</span><span class="sxs-lookup"><span data-stu-id="6c35a-133">Header</span></span><br/>  | <dl> <span data-ttu-id="6c35a-134"><dt>D2d1 \_ 1. h (включение D2d1. h)</dt></span><span class="sxs-lookup"><span data-stu-id="6c35a-134"><dt>D2d1\_1.h (include D2d1.h)</dt></span></span> </dl> |
| <span data-ttu-id="6c35a-135">Библиотека</span><span class="sxs-lookup"><span data-stu-id="6c35a-135">Library</span></span><br/> | <dl> <span data-ttu-id="6c35a-136"><dt>D2d1. lib</dt></span><span class="sxs-lookup"><span data-stu-id="6c35a-136"><dt>D2d1.lib</dt></span></span> </dl>                   |
| <span data-ttu-id="6c35a-137">DLL</span><span class="sxs-lookup"><span data-stu-id="6c35a-137">DLL</span></span><br/>     | <dl> <span data-ttu-id="6c35a-138"><dt>D2d1.dll</dt></span><span class="sxs-lookup"><span data-stu-id="6c35a-138"><dt>D2d1.dll</dt></span></span> </dl>                   |



## <a name="see-also"></a><span data-ttu-id="6c35a-139">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="6c35a-139">See also</span></span>

<dl> <dt>

[<span data-ttu-id="6c35a-140">Обзор кистей</span><span class="sxs-lookup"><span data-stu-id="6c35a-140">Brushes Overview</span></span>](direct2d-brushes-overview.md)
</dt> <dt>

[<span data-ttu-id="6c35a-141">**ID2D1Brush**</span><span class="sxs-lookup"><span data-stu-id="6c35a-141">**ID2D1Brush**</span></span>](/windows/win32/api/d2d1/nn-d2d1-id2d1brush)
</dt> </dl>

<span data-ttu-id="6c35a-142">�</span><span class="sxs-lookup"><span data-stu-id="6c35a-142">�</span></span>

<span data-ttu-id="6c35a-143">�</span><span class="sxs-lookup"><span data-stu-id="6c35a-143">�</span></span>
