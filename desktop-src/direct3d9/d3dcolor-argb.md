---
description: Инициализирует цвет с заданными значениями альфа, красного, зеленого и синего.
ms.assetid: e862ba1b-fdcf-4058-8835-e58b4fc5e21a
title: Макрос D3DCOLOR_ARGB (D3d9types. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DCOLOR_ARGB
api_type:
- HeaderDef
api_location:
- D3d9types.h
ms.openlocfilehash: bd0138c435c15c0c2ac026487471554e0edf0afa
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/15/2021
ms.locfileid: "104354423"
---
# <a name="d3dcolor_argb-macro"></a><span data-ttu-id="102d8-103">D3DCOLOR \_ ARGB, макрос</span><span class="sxs-lookup"><span data-stu-id="102d8-103">D3DCOLOR\_ARGB macro</span></span>

<span data-ttu-id="102d8-104">Инициализирует цвет с заданными значениями альфа, красного, зеленого и синего.</span><span class="sxs-lookup"><span data-stu-id="102d8-104">Initializes a color with the supplied alpha, red, green, and blue values.</span></span>

## <a name="syntax"></a><span data-ttu-id="102d8-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="102d8-105">Syntax</span></span>


```C++
D3DCOLOR D3DCOLOR_ARGB(
   int a,
   int r,
   int g,
   int b
);
```



## <a name="parameters"></a><span data-ttu-id="102d8-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="102d8-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="102d8-107">*конкретного*</span><span class="sxs-lookup"><span data-stu-id="102d8-107">*a*</span></span> 
</dt> <dd>

<span data-ttu-id="102d8-108">Альфа-компонент цвета.</span><span class="sxs-lookup"><span data-stu-id="102d8-108">Alpha component of the color.</span></span> <span data-ttu-id="102d8-109">Это значение должно находиться в диапазоне от 0 до 255.</span><span class="sxs-lookup"><span data-stu-id="102d8-109">This value must be in the range 0 through 255.</span></span>

</dd> <dt>

<span data-ttu-id="102d8-110">*r*</span><span class="sxs-lookup"><span data-stu-id="102d8-110">*r*</span></span> 
</dt> <dd>

<span data-ttu-id="102d8-111">Красный компонент цвета.</span><span class="sxs-lookup"><span data-stu-id="102d8-111">Red component of the color.</span></span> <span data-ttu-id="102d8-112">Это значение должно находиться в диапазоне от 0 до 255.</span><span class="sxs-lookup"><span data-stu-id="102d8-112">This value must be in the range 0 through 255.</span></span>

</dd> <dt>

<span data-ttu-id="102d8-113">*g*</span><span class="sxs-lookup"><span data-stu-id="102d8-113">*g*</span></span> 
</dt> <dd>

<span data-ttu-id="102d8-114">Зеленый компонент цвета.</span><span class="sxs-lookup"><span data-stu-id="102d8-114">Green component of the color.</span></span> <span data-ttu-id="102d8-115">Это значение должно находиться в диапазоне от 0 до 255.</span><span class="sxs-lookup"><span data-stu-id="102d8-115">This value must be in the range 0 through 255.</span></span>

</dd> <dt>

<span data-ttu-id="102d8-116">*b*</span><span class="sxs-lookup"><span data-stu-id="102d8-116">*b*</span></span> 
</dt> <dd>

<span data-ttu-id="102d8-117">Синий компонент цвета.</span><span class="sxs-lookup"><span data-stu-id="102d8-117">Blue component of the color.</span></span> <span data-ttu-id="102d8-118">Это значение должно находиться в диапазоне от 0 до 255.</span><span class="sxs-lookup"><span data-stu-id="102d8-118">This value must be in the range 0 through 255.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="102d8-119">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="102d8-119">Return value</span></span>

<span data-ttu-id="102d8-120">Возвращает значение [D3DCOLOR](d3dcolor.md) , соответствующее указанным значениям ARGB.</span><span class="sxs-lookup"><span data-stu-id="102d8-120">Returns the [D3DCOLOR](d3dcolor.md) value that corresponds to the supplied ARGB values.</span></span>

## <a name="requirements"></a><span data-ttu-id="102d8-121">Требования</span><span class="sxs-lookup"><span data-stu-id="102d8-121">Requirements</span></span>



| <span data-ttu-id="102d8-122">Требование</span><span class="sxs-lookup"><span data-stu-id="102d8-122">Requirement</span></span> | <span data-ttu-id="102d8-123">Значение</span><span class="sxs-lookup"><span data-stu-id="102d8-123">Value</span></span> |
|-------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="102d8-124">Header</span><span class="sxs-lookup"><span data-stu-id="102d8-124">Header</span></span><br/> | <dl> <span data-ttu-id="102d8-125"><dt>D3d9types. h</dt></span><span class="sxs-lookup"><span data-stu-id="102d8-125"><dt>D3d9types.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="102d8-126">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="102d8-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="102d8-127">Макросы</span><span class="sxs-lookup"><span data-stu-id="102d8-127">Macros</span></span>](dx9-graphics-reference-d3d-macros.md)
</dt> <dt>

[<span data-ttu-id="102d8-128">**D3DCOLOR \_ RGBA**</span><span class="sxs-lookup"><span data-stu-id="102d8-128">**D3DCOLOR\_RGBA**</span></span>](d3dcolor-rgba.md)
</dt> <dt>

[<span data-ttu-id="102d8-129">**D3DCOLOR \_ ксргб**</span><span class="sxs-lookup"><span data-stu-id="102d8-129">**D3DCOLOR\_XRGB**</span></span>](d3dcolor-xrgb.md)
</dt> </dl>

 

 




