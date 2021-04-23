---
title: D2D1_COLOR_F (D2DBaseTypes. h)
description: Описывает красный, зеленый, синий и альфа-компоненты цвета. | D2D1_COLOR_F (D2DBaseTypes. h)
ms.assetid: 564d4f41-2da7-49ed-b85a-d1070d662b40
keywords:
- D2D1_COLOR_F
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 78f12c4c833d7f73946b2309673dff8f3dd11395
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/09/2021
ms.locfileid: "105674607"
---
# <a name="d2d1_color_f"></a><span data-ttu-id="eaf41-105">D2D1 \_ Color \_ F</span><span class="sxs-lookup"><span data-stu-id="eaf41-105">D2D1\_COLOR\_F</span></span>

<span data-ttu-id="eaf41-106">Описывает красный, зеленый, синий и альфа-компоненты цвета.</span><span class="sxs-lookup"><span data-stu-id="eaf41-106">Describes the red, green, blue, and alpha components of a color.</span></span>


```C++
typedef D2D_COLOR_F D2D1_COLOR_F;
```



## <a name="remarks"></a><span data-ttu-id="eaf41-107">Комментарии</span><span class="sxs-lookup"><span data-stu-id="eaf41-107">Remarks</span></span>

<span data-ttu-id="eaf41-108">**D2D1 \_ ЦВЕТ \_ f** — это определение типа [**D2D для \_ цвета \_ f**](d2d-color-f.md), который сам по себе является typedef для [D3DCOLORVALUE](../direct3d9/d3dcolorvalue.md).</span><span class="sxs-lookup"><span data-stu-id="eaf41-108">**D2D1\_COLOR\_F** is a typedef for [**D2D\_COLOR\_F**](d2d-color-f.md), which is itself a typedef for [D3DCOLORVALUE](../direct3d9/d3dcolorvalue.md).</span></span> <span data-ttu-id="eaf41-109">Дополнительные сведения о членах, предоставляемых **D2D1 \_ Color \_ F**, см. в разделе [D3DCOLORVALUE](../direct3d9/d3dcolorvalue.md).</span><span class="sxs-lookup"><span data-stu-id="eaf41-109">For information about the members provided by **D2D1\_COLOR\_F**, see [D3DCOLORVALUE](../direct3d9/d3dcolorvalue.md).</span></span>

<span data-ttu-id="eaf41-110">Класс [**колорф**](/windows/win32/api/d2d1helper/nl-d2d1helper-colorf) предоставляет набор предопределенных цветов и вспомогательных функций для определения цветов.</span><span class="sxs-lookup"><span data-stu-id="eaf41-110">The [**ColorF**](/windows/win32/api/d2d1helper/nl-d2d1helper-colorf) class provides a set of predefined colors and helper functions for defining colors.</span></span> <span data-ttu-id="eaf41-111">Дополнительные сведения см. в справочнике по [**колорф**](/windows/win32/api/d2d1helper/nl-d2d1helper-colorf) .</span><span class="sxs-lookup"><span data-stu-id="eaf41-111">For more information, see the [**ColorF**](/windows/win32/api/d2d1helper/nl-d2d1helper-colorf) reference.</span></span>

## <a name="examples"></a><span data-ttu-id="eaf41-112">Примеры</span><span class="sxs-lookup"><span data-stu-id="eaf41-112">Examples</span></span>

<span data-ttu-id="eaf41-113">В следующем примере класс [**колорф**](/windows/win32/api/d2d1helper/nl-d2d1helper-colorf) используется для указания стандартного цвета (черного) при создании [**ID2D1SolidColorBrush**](/windows/win32/api/d2d1/nn-d2d1-id2d1solidcolorbrush).</span><span class="sxs-lookup"><span data-stu-id="eaf41-113">The following example uses the [**ColorF**](/windows/win32/api/d2d1helper/nl-d2d1helper-colorf) class to specify a predefined color (black) when creating an [**ID2D1SolidColorBrush**](/windows/win32/api/d2d1/nn-d2d1-id2d1solidcolorbrush).</span></span>


```C++
hr = m_pRenderTarget->CreateSolidColorBrush(
    D2D1::ColorF(D2D1::ColorF::Black, 1.0f),
    &m_pBlackBrush
    );
```



<span data-ttu-id="eaf41-114">В следующем примере класс [**колорф**](/windows/win32/api/d2d1helper/nl-d2d1helper-colorf) используется для указания цвета с помощью красного, зеленого, синего и альфа-значения.</span><span class="sxs-lookup"><span data-stu-id="eaf41-114">The following example uses the [**ColorF**](/windows/win32/api/d2d1helper/nl-d2d1helper-colorf) class to specify a color using red, green, blue, and alpha values.</span></span>


```C++
ID2D1SolidColorBrush *pGridBrush = NULL;
hr = pCompatibleRenderTarget->CreateSolidColorBrush(
    D2D1::ColorF(D2D1::ColorF(0.93f, 0.94f, 0.96f, 1.0f)),
    &pGridBrush
    );
```



## <a name="requirements"></a><span data-ttu-id="eaf41-115">Требования</span><span class="sxs-lookup"><span data-stu-id="eaf41-115">Requirements</span></span>



| <span data-ttu-id="eaf41-116">Требование</span><span class="sxs-lookup"><span data-stu-id="eaf41-116">Requirement</span></span> | <span data-ttu-id="eaf41-117">Значение</span><span class="sxs-lookup"><span data-stu-id="eaf41-117">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="eaf41-118">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="eaf41-118">Minimum supported client</span></span><br/> | <span data-ttu-id="eaf41-119">Windows 7, Windows Vista с пакетом обновления 2 (SP2) и обновлением платформы для \[ классических приложений Windows Vista \| приложения UWP\]</span><span class="sxs-lookup"><span data-stu-id="eaf41-119">Windows 7, Windows Vista with SP2 and Platform Update for Windows Vista \[desktop apps \| UWP apps\]</span></span><br/>                          |
| <span data-ttu-id="eaf41-120">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="eaf41-120">Minimum supported server</span></span><br/> | <span data-ttu-id="eaf41-121">Windows Server 2008 R2, Windows Server 2008 с пакетом обновления 2 (SP2) и обновление платформы для Windows Server 2008 классические \[ приложения \| UWP\]</span><span class="sxs-lookup"><span data-stu-id="eaf41-121">Windows Server 2008 R2, Windows Server 2008 with SP2 and Platform Update for Windows Server 2008 \[desktop apps \| UWP apps\]</span></span><br/> |
| <span data-ttu-id="eaf41-122">Минимальный поддерживаемый телефон</span><span class="sxs-lookup"><span data-stu-id="eaf41-122">Minimum supported phone</span></span><br/>  | <span data-ttu-id="eaf41-123">Windows Phone 8,1 \[ Windows Phone Silverlight 8,1 и среда выполнения Windows приложения\]</span><span class="sxs-lookup"><span data-stu-id="eaf41-123">Windows Phone 8.1 \[Windows Phone Silverlight 8.1 and Windows Runtime apps\]</span></span><br/>                                                  |
| <span data-ttu-id="eaf41-124">Header</span><span class="sxs-lookup"><span data-stu-id="eaf41-124">Header</span></span><br/>                   | <dl> <span data-ttu-id="eaf41-125"><dt>D2DBaseTypes. h (включение D2d1. h)</dt></span><span class="sxs-lookup"><span data-stu-id="eaf41-125"><dt>D2DBaseTypes.h (include D2d1.h)</dt></span></span> </dl>                               |



## <a name="see-also"></a><span data-ttu-id="eaf41-126">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="eaf41-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="eaf41-127">D3DCOLORVALUE</span><span class="sxs-lookup"><span data-stu-id="eaf41-127">D3DCOLORVALUE</span></span>](../direct3d9/d3dcolorvalue.md)
</dt> <dt>

[<span data-ttu-id="eaf41-128">**колорф**</span><span class="sxs-lookup"><span data-stu-id="eaf41-128">**ColorF**</span></span>](/windows/win32/api/d2d1helper/nl-d2d1helper-colorf)
</dt> </dl>

 

