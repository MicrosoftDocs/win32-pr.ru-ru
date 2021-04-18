---
title: Методы Креатеградиентстопколлектион ID2D1RenderTarget (D2d1 \_ 1. h)
description: Создает объект ID2D1GradientStopCollection из указанного массива элементов D2D1 \_ градиента \_ .
ms.assetid: 674ffba5-18c5-46bf-8813-d8d13e5ba903
keywords:
- Методы Креатеградиентстопколлектион Direct2D
topic_type:
- apiref
api_location:
- D2d1.dll
api_type:
- DllExport
ms.date: 07/02/2019
ms.topic: reference
ms.openlocfilehash: 4a298414d1a84b03d81c80e308113d8731369040
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105685280"
---
# <a name="id2d1rendertargetcreategradientstopcollection-methods"></a><span data-ttu-id="5d88d-104">Методы ID2D1RenderTarget:: Креатеградиентстопколлектион</span><span class="sxs-lookup"><span data-stu-id="5d88d-104">ID2D1RenderTarget::CreateGradientStopCollection methods</span></span>

<span data-ttu-id="5d88d-105">Создает объект [**ID2D1GradientStopCollection**](/windows/win32/api/d2d1/nn-d2d1-id2d1gradientstopcollection) из указанного массива элементов [**D2D1 \_ градиента \_**](/windows/win32/api/d2d1/ns-d2d1-d2d1_gradient_stop) .</span><span class="sxs-lookup"><span data-stu-id="5d88d-105">Creates an [**ID2D1GradientStopCollection**](/windows/win32/api/d2d1/nn-d2d1-id2d1gradientstopcollection) from the specified array of [**D2D1\_GRADIENT\_STOP**](/windows/win32/api/d2d1/ns-d2d1-d2d1_gradient_stop) structures.</span></span>

### <a name="overload-list"></a><span data-ttu-id="5d88d-106">Список перегрузок</span><span class="sxs-lookup"><span data-stu-id="5d88d-106">Overload list</span></span>



| <span data-ttu-id="5d88d-107">Метод</span><span class="sxs-lookup"><span data-stu-id="5d88d-107">Method</span></span>                                                                                                                                                                                                                                                               | <span data-ttu-id="5d88d-108">Описание</span><span class="sxs-lookup"><span data-stu-id="5d88d-108">Description</span></span>                                                                                                                                                                                                                           |
|:---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="5d88d-109">[**Креатеградиентстопколлектион (D2D1 \_ градиента \_ \* , D2D1 \_ гамма, \_ режим расширенного развертывания D2D1 \_ , ID2D1GradientStopCollection \* \* )**](id2d1rendertarget-creategradientstopcollection-ptr-d2d1-gradient-stop-d2d1-gamma-d2d1-extend-mode-ptr-ptr-https://msdn.microsoft.com/library/Dd316783(v=VS.85).aspx)</span><span class="sxs-lookup"><span data-stu-id="5d88d-109">[**CreateGradientStopCollection(D2D1\_GRADIENT\_STOP\*,D2D1\_GAMMA,D2D1\_EXTEND\_MODE,ID2D1GradientStopCollection\*\*)**](id2d1rendertarget-creategradientstopcollection-ptr-d2d1-gradient-stop-d2d1-gamma-d2d1-extend-mode-ptr-ptr-https://msdn.microsoft.com/library/Dd316783(v=VS.85).aspx)</span></span> | <span data-ttu-id="5d88d-110">Создает [**ID2D1GradientStopCollection**](/windows/win32/api/d2d1/nn-d2d1-id2d1gradientstopcollection) из указанных ограничителей градиента, гаммы интерполяции цвета и режима расширения.</span><span class="sxs-lookup"><span data-stu-id="5d88d-110">Creates an [**ID2D1GradientStopCollection**](/windows/win32/api/d2d1/nn-d2d1-id2d1gradientstopcollection) from the specified gradient stops, color interpolation gamma, and extend mode.</span></span> <br/>                                                              |
| <span data-ttu-id="5d88d-111">[**Креатеградиентстопколлектион (D2D1 \_ градиента \_ \* , ID2D1GradientStopCollection \* \* )**](id2d1rendertarget-creategradientstopcollection-ptr-d2d1-gradient-stop-ptr-ptr-https://msdn.microsoft.com/library/Dd316783(v=VS.85).aspx)</span><span class="sxs-lookup"><span data-stu-id="5d88d-111">[**CreateGradientStopCollection(D2D1\_GRADIENT\_STOP\*,ID2D1GradientStopCollection\*\*)**](id2d1rendertarget-creategradientstopcollection-ptr-d2d1-gradient-stop-ptr-ptr-https://msdn.microsoft.com/library/Dd316783(v=VS.85).aspx)</span></span>                                                            | <span data-ttu-id="5d88d-112">Создает объект [**ID2D1GradientStopCollection**](/windows/win32/api/d2d1/nn-d2d1-id2d1gradientstopcollection) на основе заданных ограничителей градиента, который использует гамму гаммы [**D2D1 \_ \_ 2 \_ 2**](/windows/win32/api/d2d1/ne-d2d1-d2d1_gamma) для интерполяции цвета и режим расширения среза.</span><span class="sxs-lookup"><span data-stu-id="5d88d-112">Creates an [**ID2D1GradientStopCollection**](/windows/win32/api/d2d1/nn-d2d1-id2d1gradientstopcollection) from the specified gradient stops that uses the [**D2D1\_GAMMA\_2\_2**](/windows/win32/api/d2d1/ne-d2d1-d2d1_gamma) color interpolation gamma and the clamp extend mode.</span></span><br/> |



## <a name="examples"></a><span data-ttu-id="5d88d-113">Примеры</span><span class="sxs-lookup"><span data-stu-id="5d88d-113">Examples</span></span>

<span data-ttu-id="5d88d-114">В следующем примере создается массив ограничителей градиента, а затем он используется для создания [**ID2D1GradientStopCollection**](/windows/win32/api/d2d1/nn-d2d1-id2d1gradientstopcollection).</span><span class="sxs-lookup"><span data-stu-id="5d88d-114">The following example creates an array of gradient stops, then uses them to create an [**ID2D1GradientStopCollection**](/windows/win32/api/d2d1/nn-d2d1-id2d1gradientstopcollection).</span></span>


```C++
// Create an array of gradient stops to put in the gradient stop
// collection that will be used in the gradient brush.
ID2D1GradientStopCollection *pGradientStops = NULL;

D2D1_GRADIENT_STOP gradientStops[2];
gradientStops[0].color = D2D1::ColorF(D2D1::ColorF::Yellow, 1);
gradientStops[0].position = 0.0f;
gradientStops[1].color = D2D1::ColorF(D2D1::ColorF::ForestGreen, 1);
gradientStops[1].position = 1.0f;
// Create the ID2D1GradientStopCollection from a previously
// declared array of D2D1_GRADIENT_STOP structs.
hr = m_pRenderTarget->CreateGradientStopCollection(
    gradientStops,
    2,
    D2D1_GAMMA_2_2,
    D2D1_EXTEND_MODE_CLAMP,
    &pGradientStops
    );
```



<span data-ttu-id="5d88d-115">В следующем примере кода используется [**ID2D1GradientStopCollection**](/windows/win32/api/d2d1/nn-d2d1-id2d1gradientstopcollection) для создания [**ID2D1LinearGradientBrush**](/windows/win32/api/d2d1/nn-d2d1-id2d1lineargradientbrush).</span><span class="sxs-lookup"><span data-stu-id="5d88d-115">The next code example uses the [**ID2D1GradientStopCollection**](/windows/win32/api/d2d1/nn-d2d1-id2d1gradientstopcollection) to create an [**ID2D1LinearGradientBrush**](/windows/win32/api/d2d1/nn-d2d1-id2d1lineargradientbrush).</span></span>


```C++
// The line that determines the direction of the gradient starts at
// the upper-left corner of the square and ends at the lower-right corner.

if (SUCCEEDED(hr))
{
    hr = m_pRenderTarget->CreateLinearGradientBrush(
        D2D1::LinearGradientBrushProperties(
            D2D1::Point2F(0, 0),
            D2D1::Point2F(150, 150)),
        pGradientStops,
        &m_pLinearGradientBrush
        );
}
```



## <a name="requirements"></a><span data-ttu-id="5d88d-116">Требования</span><span class="sxs-lookup"><span data-stu-id="5d88d-116">Requirements</span></span>



| <span data-ttu-id="5d88d-117">Требование</span><span class="sxs-lookup"><span data-stu-id="5d88d-117">Requirement</span></span> | <span data-ttu-id="5d88d-118">Значение</span><span class="sxs-lookup"><span data-stu-id="5d88d-118">Value</span></span> |
|--------------------|-------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="5d88d-119">Header</span><span class="sxs-lookup"><span data-stu-id="5d88d-119">Header</span></span><br/>  | <dl> <span data-ttu-id="5d88d-120"><dt>D2d1 \_ 1. h (включение D2d1. h)</dt></span><span class="sxs-lookup"><span data-stu-id="5d88d-120"><dt>D2d1\_1.h (include D2d1.h)</dt></span></span> </dl> |
| <span data-ttu-id="5d88d-121">Библиотека</span><span class="sxs-lookup"><span data-stu-id="5d88d-121">Library</span></span><br/> | <dl> <span data-ttu-id="5d88d-122"><dt>D2d1. lib</dt></span><span class="sxs-lookup"><span data-stu-id="5d88d-122"><dt>D2d1.lib</dt></span></span> </dl>                   |
| <span data-ttu-id="5d88d-123">DLL</span><span class="sxs-lookup"><span data-stu-id="5d88d-123">DLL</span></span><br/>     | <dl> <span data-ttu-id="5d88d-124"><dt>D2d1.dll</dt></span><span class="sxs-lookup"><span data-stu-id="5d88d-124"><dt>D2d1.dll</dt></span></span> </dl>                   |



## <a name="see-also"></a><span data-ttu-id="5d88d-125">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="5d88d-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="5d88d-126">**ID2D1RenderTarget**</span><span class="sxs-lookup"><span data-stu-id="5d88d-126">**ID2D1RenderTarget**</span></span>](/windows/win32/api/d2d1/nn-d2d1-id2d1rendertarget)
</dt> <dt>

[<span data-ttu-id="5d88d-127">**D2D1 \_ градиента \_**</span><span class="sxs-lookup"><span data-stu-id="5d88d-127">**D2D1\_GRADIENT\_STOP**</span></span>](/windows/win32/api/d2d1/ns-d2d1-d2d1_gradient_stop)
</dt> <dt>

[<span data-ttu-id="5d88d-128">Создание кисти линейного градиента</span><span class="sxs-lookup"><span data-stu-id="5d88d-128">How to Create a Linear Gradient Brush</span></span>](how-to-create-a-linear-gradient-brush.md)
</dt> <dt>

[<span data-ttu-id="5d88d-129">Создание кисти радиального градиента</span><span class="sxs-lookup"><span data-stu-id="5d88d-129">How to Create a Radial Gradient Brush</span></span>](how-to-create-a-radial-gradient-brush.md)
</dt> <dt>

[<span data-ttu-id="5d88d-130">Обзор кистей</span><span class="sxs-lookup"><span data-stu-id="5d88d-130">Brushes Overview</span></span>](direct2d-brushes-overview.md)
</dt> </dl>
