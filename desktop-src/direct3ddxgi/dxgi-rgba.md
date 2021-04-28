---
description: Структура DXGI_RGBA — представляет значение цвета с альфа-составляющей, которое используется для прозрачности.
ms.assetid: 5F9DDDC1-644E-4DA2-8E3D-F157789809E7
title: Структура DXGI_RGBA (Дксгитипе. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- DXGI_RGBA
api_type:
- HeaderDef
api_location:
- DXGItype.h
ms.openlocfilehash: b0447d6470401d4136fbfd36f6d9c089e331b14b
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2021
ms.locfileid: "108114272"
---
# <a name="dxgi_rgba-structure"></a><span data-ttu-id="838ab-103">\_Структура RGBA DXGI</span><span class="sxs-lookup"><span data-stu-id="838ab-103">DXGI\_RGBA structure</span></span>

<span data-ttu-id="838ab-104">Представляет значение цвета с альфа-составляющей, используемой для прозрачности.</span><span class="sxs-lookup"><span data-stu-id="838ab-104">Represents a color value with alpha, which is used for transparency.</span></span>

## <a name="syntax"></a><span data-ttu-id="838ab-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="838ab-105">Syntax</span></span>


```C++
typedef struct _DXGI_RGBA {
  float r;
  float g;
  float b;
  float a;
} DXGI_RGBA;
```



## <a name="members"></a><span data-ttu-id="838ab-106">Члены</span><span class="sxs-lookup"><span data-stu-id="838ab-106">Members</span></span>

<dl> <dt>

<span data-ttu-id="838ab-107">**r**</span><span class="sxs-lookup"><span data-stu-id="838ab-107">**r**</span></span>
</dt> <dd>

<span data-ttu-id="838ab-108">Значение с плавающей запятой, указывающее красный компонент цвета.</span><span class="sxs-lookup"><span data-stu-id="838ab-108">Floating-point value that specifies the red component of a color.</span></span> <span data-ttu-id="838ab-109">Обычно это значение находится в диапазоне от 0,0 до 1,0.</span><span class="sxs-lookup"><span data-stu-id="838ab-109">This value generally is in the range from 0.0 through 1.0.</span></span> <span data-ttu-id="838ab-110">Значение 0,0 указывает на полное отсутствие красного компонента, а значение 1,0 означает, что красный элемент полностью представлен.</span><span class="sxs-lookup"><span data-stu-id="838ab-110">A value of 0.0 indicates the complete absence of the red component, while a value of 1.0 indicates that red is fully present.</span></span>

</dd> <dt>

<span data-ttu-id="838ab-111">**g**</span><span class="sxs-lookup"><span data-stu-id="838ab-111">**g**</span></span>
</dt> <dd>

<span data-ttu-id="838ab-112">Значение с плавающей запятой, указывающее зеленый компонент цвета.</span><span class="sxs-lookup"><span data-stu-id="838ab-112">Floating-point value that specifies the green component of a color.</span></span> <span data-ttu-id="838ab-113">Обычно это значение находится в диапазоне от 0,0 до 1,0.</span><span class="sxs-lookup"><span data-stu-id="838ab-113">This value generally is in the range from 0.0 through 1.0.</span></span> <span data-ttu-id="838ab-114">Значение 0,0 указывает на полное отсутствие зеленого компонента, а значение 1,0 указывает на то, что зеленый объект имеется.</span><span class="sxs-lookup"><span data-stu-id="838ab-114">A value of 0.0 indicates the complete absence of the green component, while a value of 1.0 indicates that green is fully present.</span></span>

</dd> <dt>

<span data-ttu-id="838ab-115">**b**</span><span class="sxs-lookup"><span data-stu-id="838ab-115">**b**</span></span>
</dt> <dd>

<span data-ttu-id="838ab-116">Значение с плавающей запятой, указывающее синий компонент цвета.</span><span class="sxs-lookup"><span data-stu-id="838ab-116">Floating-point value that specifies the blue component of a color.</span></span> <span data-ttu-id="838ab-117">Обычно это значение находится в диапазоне от 0,0 до 1,0.</span><span class="sxs-lookup"><span data-stu-id="838ab-117">This value generally is in the range from 0.0 through 1.0.</span></span> <span data-ttu-id="838ab-118">Значение 0,0 указывает на полное отсутствие синего компонента, а значение 1,0 указывает на то, что синий цвет имеется.</span><span class="sxs-lookup"><span data-stu-id="838ab-118">A value of 0.0 indicates the complete absence of the blue component, while a value of 1.0 indicates that blue is fully present.</span></span>

</dd> <dt>

<span data-ttu-id="838ab-119">**конкретного**</span><span class="sxs-lookup"><span data-stu-id="838ab-119">**a**</span></span>
</dt> <dd>

<span data-ttu-id="838ab-120">Значение с плавающей запятой, указывающее альфа-компонент цвета.</span><span class="sxs-lookup"><span data-stu-id="838ab-120">Floating-point value that specifies the alpha component of a color.</span></span> <span data-ttu-id="838ab-121">Обычно это значение находится в диапазоне от 0,0 до 1,0.</span><span class="sxs-lookup"><span data-stu-id="838ab-121">This value generally is in the range from 0.0 through 1.0.</span></span> <span data-ttu-id="838ab-122">Значение 0,0 означает полностью прозрачное, а значение 1,0 — полностью непрозрачный.</span><span class="sxs-lookup"><span data-stu-id="838ab-122">A value of 0.0 indicates fully transparent, while a value of 1.0 indicates fully opaque.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="838ab-123">Remarks</span><span class="sxs-lookup"><span data-stu-id="838ab-123">Remarks</span></span>

<span data-ttu-id="838ab-124">Членам этой структуры можно присвоить значения вне диапазона от 0 до 1, чтобы реализовать необычные эффекты.</span><span class="sxs-lookup"><span data-stu-id="838ab-124">You can set the members of this structure to values outside the range of 0 through 1 to implement some unusual effects.</span></span> <span data-ttu-id="838ab-125">Значения больше 1 создают сильные лампочки, которые обычно заменяют сцену.</span><span class="sxs-lookup"><span data-stu-id="838ab-125">Values greater than 1 produce strong lights that tend to wash out a scene.</span></span> <span data-ttu-id="838ab-126">Отрицательные значения создают темные огни, которые фактически удаляют свет из сцены.</span><span class="sxs-lookup"><span data-stu-id="838ab-126">Negative values produce dark lights that actually remove light from a scene.</span></span>

<span data-ttu-id="838ab-127">Тип заголовка Дксгитипе. h определяет RGBA для **DXGI \_** в виде псевдонима [**D3DCOLORVALUE**](d3dcolorvalue.md), как показано ниже.</span><span class="sxs-lookup"><span data-stu-id="838ab-127">The DXGItype.h header type-defines **DXGI\_RGBA** as an alias of [**D3DCOLORVALUE**](d3dcolorvalue.md), as follows:</span></span>


```
typedef D3DCOLORVALUE DXGI_RGBA;
```



<span data-ttu-id="838ab-128">Можно использовать **\_ RGBA для DXGI** с [**\_ \_ режимом**](/windows/desktop/api/DXGI1_2/ne-dxgi1_2-dxgi_alpha_mode) [**IDXGISwapChain1:: сетбаккграундколор**](/windows/desktop/api/DXGI1_2/nf-dxgi1_2-idxgiswapchain1-setbackgroundcolor), [**IDXGISwapChain1:: жетбаккграундколор**](/windows/desktop/api/DXGI1_2/nf-dxgi1_2-idxgiswapchain1-getbackgroundcolor)и DXGI Alpha.</span><span class="sxs-lookup"><span data-stu-id="838ab-128">You can use **DXGI\_RGBA** with [**IDXGISwapChain1::SetBackgroundColor**](/windows/desktop/api/DXGI1_2/nf-dxgi1_2-idxgiswapchain1-setbackgroundcolor), [**IDXGISwapChain1::GetBackgroundColor**](/windows/desktop/api/DXGI1_2/nf-dxgi1_2-idxgiswapchain1-getbackgroundcolor), and [**DXGI\_ALPHA\_MODE**](/windows/desktop/api/DXGI1_2/ne-dxgi1_2-dxgi_alpha_mode).</span></span>

## <a name="requirements"></a><span data-ttu-id="838ab-129">Требования</span><span class="sxs-lookup"><span data-stu-id="838ab-129">Requirements</span></span>



| <span data-ttu-id="838ab-130">Требование</span><span class="sxs-lookup"><span data-stu-id="838ab-130">Requirement</span></span> | <span data-ttu-id="838ab-131">Значение</span><span class="sxs-lookup"><span data-stu-id="838ab-131">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="838ab-132">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="838ab-132">Minimum supported client</span></span><br/> | <span data-ttu-id="838ab-133">Windows 8 и обновление платформы для приложений Windows 7 \[ классических приложений \| UWP\]</span><span class="sxs-lookup"><span data-stu-id="838ab-133">Windows 8 and Platform Update for Windows 7 \[desktop apps \| UWP apps\]</span></span><br/>                        |
| <span data-ttu-id="838ab-134">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="838ab-134">Minimum supported server</span></span><br/> | <span data-ttu-id="838ab-135">Windows Server 2012 и обновление платформы для приложений Windows Server 2008 R2 \[ Desktop приложения \| UWP\]</span><span class="sxs-lookup"><span data-stu-id="838ab-135">Windows Server 2012 and Platform Update for Windows Server 2008 R2 \[desktop apps \| UWP apps\]</span></span><br/> |
| <span data-ttu-id="838ab-136">Header</span><span class="sxs-lookup"><span data-stu-id="838ab-136">Header</span></span><br/>                   | <dl> <span data-ttu-id="838ab-137"><dt>Дксгитипе. h</dt></span><span class="sxs-lookup"><span data-stu-id="838ab-137"><dt>DXGItype.h</dt></span></span> </dl>                      |



## <a name="see-also"></a><span data-ttu-id="838ab-138">См. также</span><span class="sxs-lookup"><span data-stu-id="838ab-138">See also</span></span>

<dl> <dt>

[<span data-ttu-id="838ab-139">Структуры DXGI</span><span class="sxs-lookup"><span data-stu-id="838ab-139">DXGI Structures</span></span>](d3d10-graphics-reference-dxgi-structures.md)
</dt> <dt>

[<span data-ttu-id="838ab-140">**D3DCOLORVALUE**</span><span class="sxs-lookup"><span data-stu-id="838ab-140">**D3DCOLORVALUE**</span></span>](d3dcolorvalue.md)
</dt> <dt>

[<span data-ttu-id="838ab-141">**D3DCOLORVALUE (в Direct3D 9)**</span><span class="sxs-lookup"><span data-stu-id="838ab-141">**D3DCOLORVALUE (in Direct3D 9)**</span></span>](../direct3d9/d3dcolorvalue.md)
</dt> </dl>

 

 
