---
description: Инициализирует цвет с помощью значений (y, u, v).
ms.assetid: e3091eaf-8639-428c-8dd8-6feeb7d7776e
title: Макрос D3DCOLOR_XYUV (D3d9types. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DCOLOR_XYUV
api_type:
- HeaderDef
api_location:
- D3d9types.h
ms.openlocfilehash: 12d539e44528c5e54a54209763e4cbe262cd16f7
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/15/2021
ms.locfileid: "103914704"
---
# <a name="d3dcolor_xyuv-macro"></a><span data-ttu-id="5006d-103">\_Макрос D3DCOLOR ксюв</span><span class="sxs-lookup"><span data-stu-id="5006d-103">D3DCOLOR\_XYUV macro</span></span>

<span data-ttu-id="5006d-104">Инициализирует цвет с помощью значений (y, u, v).</span><span class="sxs-lookup"><span data-stu-id="5006d-104">Initializes a color with the (y, u, v) values.</span></span>

## <a name="syntax"></a><span data-ttu-id="5006d-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="5006d-105">Syntax</span></span>


```C++
D3DCOLOR D3DCOLOR_XYUV(
   int y,
   int u,
   int v
);
```



## <a name="parameters"></a><span data-ttu-id="5006d-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="5006d-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="5006d-107">*y*</span><span class="sxs-lookup"><span data-stu-id="5006d-107">*y*</span></span> 
</dt> <dd>

<span data-ttu-id="5006d-108">Компонент освещенности цвета.</span><span class="sxs-lookup"><span data-stu-id="5006d-108">Luminance component of the color.</span></span> <span data-ttu-id="5006d-109">Это значение должно находиться в диапазоне от 0 до 255.</span><span class="sxs-lookup"><span data-stu-id="5006d-109">This value must be in the range 0 through 255.</span></span>

</dd> <dt>

<span data-ttu-id="5006d-110">*u*</span><span class="sxs-lookup"><span data-stu-id="5006d-110">*u*</span></span> 
</dt> <dd>

<span data-ttu-id="5006d-111">Синяя яркость цвета.</span><span class="sxs-lookup"><span data-stu-id="5006d-111">Blue brightness of the color.</span></span> <span data-ttu-id="5006d-112">Это значение должно находиться в диапазоне от 0 до 255.</span><span class="sxs-lookup"><span data-stu-id="5006d-112">This value must be in the range 0 through 255.</span></span>

</dd> <dt>

<span data-ttu-id="5006d-113">*3,3*</span><span class="sxs-lookup"><span data-stu-id="5006d-113">*v*</span></span> 
</dt> <dd>

<span data-ttu-id="5006d-114">Красная яркость цвета.</span><span class="sxs-lookup"><span data-stu-id="5006d-114">Red brightness of the color.</span></span> <span data-ttu-id="5006d-115">Это значение должно находиться в диапазоне от 0 до 255.</span><span class="sxs-lookup"><span data-stu-id="5006d-115">This value must be in the range 0 through 255.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="5006d-116">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="5006d-116">Return value</span></span>

<span data-ttu-id="5006d-117">Возвращает значение [**D3DCOLOR**](d3dcolor.md) , соответствующее указанным значениям (y, u, v).</span><span class="sxs-lookup"><span data-stu-id="5006d-117">Returns the [**D3DCOLOR**](d3dcolor.md) value that corresponds to the supplied (y, u, v) values.</span></span>

## <a name="remarks"></a><span data-ttu-id="5006d-118">Комментарии</span><span class="sxs-lookup"><span data-stu-id="5006d-118">Remarks</span></span>

<span data-ttu-id="5006d-119">Цвет RGB можно уменьшить до 16 бит на пиксель путем преобразования в цветовые различия и цвета в следующих уравнениях:</span><span class="sxs-lookup"><span data-stu-id="5006d-119">An RGB color can be reduced to 16 bits per pixel by conversion to luminance and color differences with the following equations:</span></span>


```C++
y (luminance) = 0.299*red + 0.587*green + 0.114*blue
u = blue - luminance
v = red - luminance 
```



## <a name="requirements"></a><span data-ttu-id="5006d-120">Требования</span><span class="sxs-lookup"><span data-stu-id="5006d-120">Requirements</span></span>



| <span data-ttu-id="5006d-121">Требование</span><span class="sxs-lookup"><span data-stu-id="5006d-121">Requirement</span></span> | <span data-ttu-id="5006d-122">Значение</span><span class="sxs-lookup"><span data-stu-id="5006d-122">Value</span></span> |
|-------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="5006d-123">Header</span><span class="sxs-lookup"><span data-stu-id="5006d-123">Header</span></span><br/> | <dl> <span data-ttu-id="5006d-124"><dt>D3d9types. h</dt></span><span class="sxs-lookup"><span data-stu-id="5006d-124"><dt>D3d9types.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="5006d-125">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="5006d-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="5006d-126">Макросы</span><span class="sxs-lookup"><span data-stu-id="5006d-126">Macros</span></span>](dx9-graphics-reference-d3d-macros.md)
</dt> <dt>

[<span data-ttu-id="5006d-127">**D3DCOLOR \_ ARGB**</span><span class="sxs-lookup"><span data-stu-id="5006d-127">**D3DCOLOR\_ARGB**</span></span>](d3dcolor-argb.md)
</dt> <dt>

[<span data-ttu-id="5006d-128">**D3DCOLOR \_ айув**</span><span class="sxs-lookup"><span data-stu-id="5006d-128">**D3DCOLOR\_AYUV**</span></span>](d3dcolor-ayuv.md)
</dt> </dl>

 

 




