---
title: ID2D1RenderTarget Сеттрансформ методы
description: Применяет указанное преобразование к целевому объекту прорисовки, заменяя существующее преобразование. Все последующие операции рисования происходят в преобразованном пространстве.
ms.assetid: 04799366-6458-40ff-a2fb-5d227eab041d
keywords:
- Методы Сеттрансформ Direct2D
topic_type:
- apiref
api_location:
- D2d1.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
api_name: ''
ms.openlocfilehash: 8310bf9e5c97beb3ea3cf3b2a9a513f606079a18
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105658097"
---
# <a name="id2d1rendertargetsettransform-methods"></a><span data-ttu-id="54d37-105">Методы ID2D1RenderTarget:: Сеттрансформ</span><span class="sxs-lookup"><span data-stu-id="54d37-105">ID2D1RenderTarget::SetTransform methods</span></span>

<span data-ttu-id="54d37-106">Применяет указанное преобразование к целевому объекту прорисовки, заменяя существующее преобразование.</span><span class="sxs-lookup"><span data-stu-id="54d37-106">Applies the specified transform to the render target, replacing the existing transformation.</span></span> <span data-ttu-id="54d37-107">Все последующие операции рисования происходят в преобразованном пространстве.</span><span class="sxs-lookup"><span data-stu-id="54d37-107">All subsequent drawing operations occur in the transformed space.</span></span>

### <a name="overload-list"></a><span data-ttu-id="54d37-108">Список перегрузок</span><span class="sxs-lookup"><span data-stu-id="54d37-108">Overload list</span></span>



| <span data-ttu-id="54d37-109">Метод</span><span class="sxs-lookup"><span data-stu-id="54d37-109">Method</span></span>                                                                                              | <span data-ttu-id="54d37-110">Описание</span><span class="sxs-lookup"><span data-stu-id="54d37-110">Description</span></span>                                                                                                                                                                |
|:----------------------------------------------------------------------------------------------------|:---------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="54d37-111">[**Сеттрансформ (D2D1 \_ Matrix \_ 3X2 \_ F&)**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-settransform(constd2d1_matrix_3x2_f_))</span><span class="sxs-lookup"><span data-stu-id="54d37-111">[**SetTransform(D2D1\_MATRIX\_3X2\_F&)**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-settransform(constd2d1_matrix_3x2_f_))</span></span>  | <span data-ttu-id="54d37-112">Применяет указанное преобразование к целевому объекту прорисовки, заменяя существующее преобразование.</span><span class="sxs-lookup"><span data-stu-id="54d37-112">Applies the specified transform to the render target, replacing the existing transformation.</span></span> <span data-ttu-id="54d37-113">Все последующие операции рисования происходят в преобразованном пространстве.</span><span class="sxs-lookup"><span data-stu-id="54d37-113">All subsequent drawing operations occur in the transformed space.</span></span> <br/> |
| <span data-ttu-id="54d37-114">[**Сеттрансформ (D2D1 \_ Matrix \_ 3X2 \_ F \* )**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-settransform(constd2d1_matrix_3x2_f))</span><span class="sxs-lookup"><span data-stu-id="54d37-114">[**SetTransform(D2D1\_MATRIX\_3X2\_F\*)**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-settransform(constd2d1_matrix_3x2_f))</span></span> | <span data-ttu-id="54d37-115">Применяет указанное преобразование к целевому объекту прорисовки, заменяя существующее преобразование.</span><span class="sxs-lookup"><span data-stu-id="54d37-115">Applies the specified transform to the render target, replacing the existing transformation.</span></span> <span data-ttu-id="54d37-116">Все последующие операции рисования происходят в преобразованном пространстве.</span><span class="sxs-lookup"><span data-stu-id="54d37-116">All subsequent drawing operations occur in the transformed space.</span></span><br/>  |



## <a name="examples"></a><span data-ttu-id="54d37-117">Примеры</span><span class="sxs-lookup"><span data-stu-id="54d37-117">Examples</span></span>

<span data-ttu-id="54d37-118">В следующем примере метод **сеттрансформ** используется для применения вращения к целевому объекту прорисовки.</span><span class="sxs-lookup"><span data-stu-id="54d37-118">The following example uses the **SetTransform** method to apply a rotation to the render target.</span></span> <span data-ttu-id="54d37-119">Полный пример см. в разделе [вращение объекта](how-to-rotate.md).</span><span class="sxs-lookup"><span data-stu-id="54d37-119">For the complete example, see [How to Rotate an Object](how-to-rotate.md).</span></span>


```C++
// Apply the rotation transform to the render target.
m_pRenderTarget->SetTransform(
    D2D1::Matrix3x2F::Rotation(
        45.0f,
        D2D1::Point2F(468.0f, 331.5f))
    );
```



<span data-ttu-id="54d37-120">Дополнительные примеры, показывающие, как преобразовать целевой объект прорисовки, см. [в разделе Масштабирование объекта](how-to-scale.md), [как наклон объекта](how-to-skew.md)и [Преобразование объекта](how-to-translate.md).</span><span class="sxs-lookup"><span data-stu-id="54d37-120">For additional examples showing how to transform a render target, see [How to Scale an Object](how-to-scale.md), [How to Skew an Object](how-to-skew.md), and [How to Translate an Object](how-to-translate.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="54d37-121">Требования</span><span class="sxs-lookup"><span data-stu-id="54d37-121">Requirements</span></span>



| <span data-ttu-id="54d37-122">Требование</span><span class="sxs-lookup"><span data-stu-id="54d37-122">Requirement</span></span> | <span data-ttu-id="54d37-123">Значение</span><span class="sxs-lookup"><span data-stu-id="54d37-123">Value</span></span> |
|--------------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="54d37-124">Библиотека</span><span class="sxs-lookup"><span data-stu-id="54d37-124">Library</span></span><br/> | <dl> <span data-ttu-id="54d37-125"><dt>D2d1. lib</dt></span><span class="sxs-lookup"><span data-stu-id="54d37-125"><dt>D2d1.lib</dt></span></span> </dl> |
| <span data-ttu-id="54d37-126">DLL</span><span class="sxs-lookup"><span data-stu-id="54d37-126">DLL</span></span><br/>     | <dl> <span data-ttu-id="54d37-127"><dt>D2d1.dll</dt></span><span class="sxs-lookup"><span data-stu-id="54d37-127"><dt>D2d1.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="54d37-128">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="54d37-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="54d37-129">**ID2D1RenderTarget**</span><span class="sxs-lookup"><span data-stu-id="54d37-129">**ID2D1RenderTarget**</span></span>](/windows/win32/api/d2d1/nn-d2d1-id2d1rendertarget)
</dt> <dt>

[<span data-ttu-id="54d37-130">Общие сведения о преобразованиях</span><span class="sxs-lookup"><span data-stu-id="54d37-130">Transforms Overview</span></span>](direct2d-transforms-overview.md)
</dt> <dt>

[<span data-ttu-id="54d37-131">Поворот объекта</span><span class="sxs-lookup"><span data-stu-id="54d37-131">How to Rotate an Object</span></span>](how-to-rotate.md)
</dt> <dt>

[<span data-ttu-id="54d37-132">Масштабирование объекта</span><span class="sxs-lookup"><span data-stu-id="54d37-132">How to Scale an Object</span></span>](how-to-scale.md)
</dt> <dt>

[<span data-ttu-id="54d37-133">Как наклон объекта</span><span class="sxs-lookup"><span data-stu-id="54d37-133">How to Skew an Object</span></span>](how-to-skew.md)
</dt> <dt>

[<span data-ttu-id="54d37-134">Преобразование объекта</span><span class="sxs-lookup"><span data-stu-id="54d37-134">How to Translate an Object</span></span>](how-to-translate.md)
</dt> <dt>

[<span data-ttu-id="54d37-135">Применение нескольких преобразований к объекту</span><span class="sxs-lookup"><span data-stu-id="54d37-135">How to Apply Multiple Transforms to an Object</span></span>](how-to-apply-multiple-transforms.md)
</dt> </dl>

 

