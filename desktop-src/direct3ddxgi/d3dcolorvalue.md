---
description: Представляет значение цвета с альфа-составляющей, используемой для прозрачности.
ms.assetid: 27A86A10-FC0E-421E-BEA7-2DEB539849BB
title: Структура D3DCOLORVALUE (Дксгитипе. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DCOLORVALUE
api_type:
- HeaderDef
api_location:
- dxgitype.h
ms.openlocfilehash: 2b7d768af9e471f3183c6a400622c2b0e0719a2f
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/15/2021
ms.locfileid: "104354760"
---
# <a name="d3dcolorvalue-structure-dxgitypeh"></a><span data-ttu-id="10c31-103">Структура D3DCOLORVALUE (Дксгитипе. h)</span><span class="sxs-lookup"><span data-stu-id="10c31-103">D3DCOLORVALUE structure (Dxgitype.h)</span></span>

<span data-ttu-id="10c31-104">Представляет значение цвета с альфа-составляющей, используемой для прозрачности.</span><span class="sxs-lookup"><span data-stu-id="10c31-104">Represents a color value with alpha, which is used for transparency.</span></span>

## <a name="syntax"></a><span data-ttu-id="10c31-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="10c31-105">Syntax</span></span>


```C++
typedef struct _D3DCOLORVALUE {
  float r;
  float g;
  float b;
  float a;
} D3DCOLORVALUE;
```



## <a name="members"></a><span data-ttu-id="10c31-106">Члены</span><span class="sxs-lookup"><span data-stu-id="10c31-106">Members</span></span>

<dl> <dt>

<span data-ttu-id="10c31-107">**r**</span><span class="sxs-lookup"><span data-stu-id="10c31-107">**r**</span></span>
</dt> <dd>

<span data-ttu-id="10c31-108">Значение с плавающей запятой, указывающее красный компонент цвета.</span><span class="sxs-lookup"><span data-stu-id="10c31-108">Floating-point value that specifies the red component of a color.</span></span> <span data-ttu-id="10c31-109">Обычно это значение находится в диапазоне от 0,0 до 1,0.</span><span class="sxs-lookup"><span data-stu-id="10c31-109">This value generally is in the range from 0.0 through 1.0.</span></span> <span data-ttu-id="10c31-110">Значение 0,0 указывает на полное отсутствие красного компонента, а значение 1,0 означает, что красный элемент полностью представлен.</span><span class="sxs-lookup"><span data-stu-id="10c31-110">A value of 0.0 indicates the complete absence of the red component, while a value of 1.0 indicates that red is fully present.</span></span>

</dd> <dt>

<span data-ttu-id="10c31-111">**g**</span><span class="sxs-lookup"><span data-stu-id="10c31-111">**g**</span></span>
</dt> <dd>

<span data-ttu-id="10c31-112">Значение с плавающей запятой, указывающее зеленый компонент цвета.</span><span class="sxs-lookup"><span data-stu-id="10c31-112">Floating-point value that specifies the green component of a color.</span></span> <span data-ttu-id="10c31-113">Обычно это значение находится в диапазоне от 0,0 до 1,0.</span><span class="sxs-lookup"><span data-stu-id="10c31-113">This value generally is in the range from 0.0 through 1.0.</span></span> <span data-ttu-id="10c31-114">Значение 0,0 указывает на полное отсутствие зеленого компонента, а значение 1,0 указывает на то, что зеленый объект имеется.</span><span class="sxs-lookup"><span data-stu-id="10c31-114">A value of 0.0 indicates the complete absence of the green component, while a value of 1.0 indicates that green is fully present.</span></span>

</dd> <dt>

<span data-ttu-id="10c31-115">**b**</span><span class="sxs-lookup"><span data-stu-id="10c31-115">**b**</span></span>
</dt> <dd>

<span data-ttu-id="10c31-116">Значение с плавающей запятой, указывающее синий компонент цвета.</span><span class="sxs-lookup"><span data-stu-id="10c31-116">Floating-point value that specifies the blue component of a color.</span></span> <span data-ttu-id="10c31-117">Обычно это значение находится в диапазоне от 0,0 до 1,0.</span><span class="sxs-lookup"><span data-stu-id="10c31-117">This value generally is in the range from 0.0 through 1.0.</span></span> <span data-ttu-id="10c31-118">Значение 0,0 указывает на полное отсутствие синего компонента, а значение 1,0 указывает на то, что синий цвет имеется.</span><span class="sxs-lookup"><span data-stu-id="10c31-118">A value of 0.0 indicates the complete absence of the blue component, while a value of 1.0 indicates that blue is fully present.</span></span>

</dd> <dt>

<span data-ttu-id="10c31-119">**конкретного**</span><span class="sxs-lookup"><span data-stu-id="10c31-119">**a**</span></span>
</dt> <dd>

<span data-ttu-id="10c31-120">Значение с плавающей запятой, указывающее альфа-компонент цвета.</span><span class="sxs-lookup"><span data-stu-id="10c31-120">Floating-point value that specifies the alpha component of a color.</span></span> <span data-ttu-id="10c31-121">Обычно это значение находится в диапазоне от 0,0 до 1,0.</span><span class="sxs-lookup"><span data-stu-id="10c31-121">This value generally is in the range from 0.0 through 1.0.</span></span> <span data-ttu-id="10c31-122">Значение 0,0 означает полностью прозрачное, а значение 1,0 — полностью непрозрачный.</span><span class="sxs-lookup"><span data-stu-id="10c31-122">A value of 0.0 indicates fully transparent, while a value of 1.0 indicates fully opaque.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="10c31-123">Комментарии</span><span class="sxs-lookup"><span data-stu-id="10c31-123">Remarks</span></span>

<span data-ttu-id="10c31-124">Членам этой структуры можно присвоить значения вне диапазона от 0 до 1, чтобы реализовать необычные эффекты.</span><span class="sxs-lookup"><span data-stu-id="10c31-124">You can set the members of this structure to values outside the range of 0 through 1 to implement some unusual effects.</span></span> <span data-ttu-id="10c31-125">Значения больше 1 создают сильные лампочки, которые обычно заменяют сцену.</span><span class="sxs-lookup"><span data-stu-id="10c31-125">Values greater than 1 produce strong lights that tend to wash out a scene.</span></span> <span data-ttu-id="10c31-126">Отрицательные значения создают темные огни, которые фактически удаляют свет из сцены.</span><span class="sxs-lookup"><span data-stu-id="10c31-126">Negative values produce dark lights that actually remove light from a scene.</span></span>

<span data-ttu-id="10c31-127">Тип заголовка Дксгитипе. h определяет RGBA для [**DXGI \_**](dxgi-rgba.md) в виде псевдонима **D3DCOLORVALUE**, как показано ниже.</span><span class="sxs-lookup"><span data-stu-id="10c31-127">The DXGItype.h header type-defines [**DXGI\_RGBA**](dxgi-rgba.md) as an alias of **D3DCOLORVALUE**, as follows:</span></span>


```
typedef D3DCOLORVALUE DXGI_RGBA;
```



<span data-ttu-id="10c31-128">Вы можете использовать D3DCOLORVALUE или [**\_ RGBA для DXGI**](dxgi-rgba.md) с [**IDXGISwapChain1:: сетбаккграундколор**](/windows/desktop/api/DXGI1_2/nf-dxgi1_2-idxgiswapchain1-setbackgroundcolor), [**IDXGISwapChain1:: жетбаккграундколор**](/windows/desktop/api/DXGI1_2/nf-dxgi1_2-idxgiswapchain1-getbackgroundcolor)и [**\_ \_ режимом альфа Alpha**](/windows/desktop/api/DXGI1_2/ne-dxgi1_2-dxgi_alpha_mode).</span><span class="sxs-lookup"><span data-stu-id="10c31-128">You can use D3DCOLORVALUE or [**DXGI\_RGBA**](dxgi-rgba.md) with [**IDXGISwapChain1::SetBackgroundColor**](/windows/desktop/api/DXGI1_2/nf-dxgi1_2-idxgiswapchain1-setbackgroundcolor), [**IDXGISwapChain1::GetBackgroundColor**](/windows/desktop/api/DXGI1_2/nf-dxgi1_2-idxgiswapchain1-getbackgroundcolor), and [**DXGI\_ALPHA\_MODE**](/windows/desktop/api/DXGI1_2/ne-dxgi1_2-dxgi_alpha_mode).</span></span>

## <a name="requirements"></a><span data-ttu-id="10c31-129">Требования</span><span class="sxs-lookup"><span data-stu-id="10c31-129">Requirements</span></span>



| <span data-ttu-id="10c31-130">Требование</span><span class="sxs-lookup"><span data-stu-id="10c31-130">Requirement</span></span> | <span data-ttu-id="10c31-131">Значение</span><span class="sxs-lookup"><span data-stu-id="10c31-131">Value</span></span> |
|-------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="10c31-132">Header</span><span class="sxs-lookup"><span data-stu-id="10c31-132">Header</span></span><br/> | <dl> <span data-ttu-id="10c31-133"><dt>Дксгитипе. h</dt></span><span class="sxs-lookup"><span data-stu-id="10c31-133"><dt>Dxgitype.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="10c31-134">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="10c31-134">See also</span></span>

<dl> <dt>

[<span data-ttu-id="10c31-135">Структуры DXGI</span><span class="sxs-lookup"><span data-stu-id="10c31-135">DXGI Structures</span></span>](d3d10-graphics-reference-dxgi-structures.md)
</dt> <dt>

[<span data-ttu-id="10c31-136">**RGBA для DXGI \_**</span><span class="sxs-lookup"><span data-stu-id="10c31-136">**DXGI\_RGBA**</span></span>](dxgi-rgba.md)
</dt> </dl>

 

 




