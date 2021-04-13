---
description: Инициализирует цвет, используя значения (a, y, u, v).
ms.assetid: 47b65aab-511a-44c1-ab94-973bc2da7e04
title: Макрос D3DCOLOR_AYUV (D3d9types. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DCOLOR_AYUV
api_type:
- HeaderDef
api_location:
- D3d9types.h
ms.openlocfilehash: 62a34e94fbdc6c47ed034a46bdae6e9b32a7c95d
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/15/2021
ms.locfileid: "105647832"
---
# <a name="d3dcolor_ayuv-macro"></a><span data-ttu-id="809cd-103">\_Макрос D3DCOLOR айув</span><span class="sxs-lookup"><span data-stu-id="809cd-103">D3DCOLOR\_AYUV macro</span></span>

<span data-ttu-id="809cd-104">Инициализирует цвет, используя значения (a, y, u, v).</span><span class="sxs-lookup"><span data-stu-id="809cd-104">Initializes a color using the (a,y,u,v) values.</span></span>

## <a name="syntax"></a><span data-ttu-id="809cd-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="809cd-105">Syntax</span></span>


```C++
D3DCOLOR D3DCOLOR_AYUV(
   int a,
   int y,
   int u,
   int v
);
```



## <a name="parameters"></a><span data-ttu-id="809cd-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="809cd-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="809cd-107">*конкретного*</span><span class="sxs-lookup"><span data-stu-id="809cd-107">*a*</span></span> 
</dt> <dd>

<span data-ttu-id="809cd-108">Альфа-компонент цвета.</span><span class="sxs-lookup"><span data-stu-id="809cd-108">Alpha component of the color.</span></span> <span data-ttu-id="809cd-109">Это значение должно находиться в диапазоне от 0 до 255.</span><span class="sxs-lookup"><span data-stu-id="809cd-109">This value must be in the range 0 through 255.</span></span>

</dd> <dt>

<span data-ttu-id="809cd-110">*y*</span><span class="sxs-lookup"><span data-stu-id="809cd-110">*y*</span></span> 
</dt> <dd>

<span data-ttu-id="809cd-111">Компонент освещенности цвета.</span><span class="sxs-lookup"><span data-stu-id="809cd-111">Luminance component of the color.</span></span> <span data-ttu-id="809cd-112">Это значение должно находиться в диапазоне от 0 до 255.</span><span class="sxs-lookup"><span data-stu-id="809cd-112">This value must be in the range 0 through 255.</span></span>

</dd> <dt>

<span data-ttu-id="809cd-113">*u*</span><span class="sxs-lookup"><span data-stu-id="809cd-113">*u*</span></span> 
</dt> <dd>

<span data-ttu-id="809cd-114">Синяя яркость цвета.</span><span class="sxs-lookup"><span data-stu-id="809cd-114">Blue brightness of the color.</span></span> <span data-ttu-id="809cd-115">Это значение должно находиться в диапазоне от 0 до 255.</span><span class="sxs-lookup"><span data-stu-id="809cd-115">This value must be in the range 0 through 255.</span></span>

</dd> <dt>

<span data-ttu-id="809cd-116">*3,3*</span><span class="sxs-lookup"><span data-stu-id="809cd-116">*v*</span></span> 
</dt> <dd>

<span data-ttu-id="809cd-117">Красная яркость цвета.</span><span class="sxs-lookup"><span data-stu-id="809cd-117">Red brightness of the color.</span></span> <span data-ttu-id="809cd-118">Это значение должно находиться в диапазоне от 0 до 255.</span><span class="sxs-lookup"><span data-stu-id="809cd-118">This value must be in the range 0 through 255.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="809cd-119">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="809cd-119">Return value</span></span>

<span data-ttu-id="809cd-120">Возвращает значение [D3DCOLOR](d3dcolor.md) , соответствующее указанным значениям ARGB.</span><span class="sxs-lookup"><span data-stu-id="809cd-120">Returns the [D3DCOLOR](d3dcolor.md) value that corresponds to the supplied ARGB values.</span></span>

## <a name="remarks"></a><span data-ttu-id="809cd-121">Комментарии</span><span class="sxs-lookup"><span data-stu-id="809cd-121">Remarks</span></span>

<span data-ttu-id="809cd-122">Цвет RGB можно уменьшить до 16 бит на пиксель путем преобразования в цветовые различия и цвета в следующих уравнениях:</span><span class="sxs-lookup"><span data-stu-id="809cd-122">An RGB color can be reduced to 16 bits per pixel by conversion to luminance and color differences with the following equations:</span></span>


```C++
y (luminance) = 0.299*red + 0.587*green + 0.114*blue
u = blue - luminance
v = red - luminance 
```



## <a name="requirements"></a><span data-ttu-id="809cd-123">Требования</span><span class="sxs-lookup"><span data-stu-id="809cd-123">Requirements</span></span>



| <span data-ttu-id="809cd-124">Требование</span><span class="sxs-lookup"><span data-stu-id="809cd-124">Requirement</span></span> | <span data-ttu-id="809cd-125">Значение</span><span class="sxs-lookup"><span data-stu-id="809cd-125">Value</span></span> |
|-------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="809cd-126">Header</span><span class="sxs-lookup"><span data-stu-id="809cd-126">Header</span></span><br/> | <dl> <span data-ttu-id="809cd-127"><dt>D3d9types. h</dt></span><span class="sxs-lookup"><span data-stu-id="809cd-127"><dt>D3d9types.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="809cd-128">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="809cd-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="809cd-129">Макросы</span><span class="sxs-lookup"><span data-stu-id="809cd-129">Macros</span></span>](dx9-graphics-reference-d3d-macros.md)
</dt> <dt>

[<span data-ttu-id="809cd-130">**D3DCOLOR \_ ARGB**</span><span class="sxs-lookup"><span data-stu-id="809cd-130">**D3DCOLOR\_ARGB**</span></span>](d3dcolor-argb.md)
</dt> <dt>

[<span data-ttu-id="809cd-131">**D3DCOLOR \_ ксюв**</span><span class="sxs-lookup"><span data-stu-id="809cd-131">**D3DCOLOR\_XYUV**</span></span>](d3dcolor-xyuv.md)
</dt> </dl>

 

 




