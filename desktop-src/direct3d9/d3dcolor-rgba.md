---
description: Инициализирует цвет с заданными значениями красного, зеленого, синего и альфа-канала.
ms.assetid: 87d322f1-4a26-42fd-a1c3-7be220cecf0f
title: Макрос D3DCOLOR_RGBA (D3d9types. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DCOLOR_RGBA
api_type:
- HeaderDef
api_location:
- D3d9types.h
ms.openlocfilehash: c5047f29a9afbe5bb18db213f90e559b5e11d273
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/15/2021
ms.locfileid: "105647831"
---
# <a name="d3dcolor_rgba-macro"></a><span data-ttu-id="be0d4-103">\_Макрос D3DCOLOR RGBA</span><span class="sxs-lookup"><span data-stu-id="be0d4-103">D3DCOLOR\_RGBA macro</span></span>

<span data-ttu-id="be0d4-104">Инициализирует цвет с заданными значениями красного, зеленого, синего и альфа-канала.</span><span class="sxs-lookup"><span data-stu-id="be0d4-104">Initializes a color with the supplied red, green, blue, and alpha values.</span></span>

## <a name="syntax"></a><span data-ttu-id="be0d4-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="be0d4-105">Syntax</span></span>


```C++
D3DCOLOR D3DCOLOR_RGBA(
   int r,
   int g,
   int b,
   int a
);
```



## <a name="parameters"></a><span data-ttu-id="be0d4-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="be0d4-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="be0d4-107">*r*</span><span class="sxs-lookup"><span data-stu-id="be0d4-107">*r*</span></span> 
</dt> <dd>

<span data-ttu-id="be0d4-108">Красный компонент цвета.</span><span class="sxs-lookup"><span data-stu-id="be0d4-108">Red component of the color.</span></span> <span data-ttu-id="be0d4-109">Это значение должно находиться в диапазоне от 0 до 255.</span><span class="sxs-lookup"><span data-stu-id="be0d4-109">This value must be in the range 0 through 255.</span></span>

</dd> <dt>

<span data-ttu-id="be0d4-110">*g*</span><span class="sxs-lookup"><span data-stu-id="be0d4-110">*g*</span></span> 
</dt> <dd>

<span data-ttu-id="be0d4-111">Зеленый компонент цвета.</span><span class="sxs-lookup"><span data-stu-id="be0d4-111">Green component of the color.</span></span> <span data-ttu-id="be0d4-112">Это значение должно находиться в диапазоне от 0 до 255.</span><span class="sxs-lookup"><span data-stu-id="be0d4-112">This value must be in the range 0 through 255.</span></span>

</dd> <dt>

<span data-ttu-id="be0d4-113">*b*</span><span class="sxs-lookup"><span data-stu-id="be0d4-113">*b*</span></span> 
</dt> <dd>

<span data-ttu-id="be0d4-114">Синий компонент цвета.</span><span class="sxs-lookup"><span data-stu-id="be0d4-114">Blue component of the color.</span></span> <span data-ttu-id="be0d4-115">Это значение должно находиться в диапазоне от 0 до 255.</span><span class="sxs-lookup"><span data-stu-id="be0d4-115">This value must be in the range 0 through 255.</span></span>

</dd> <dt>

<span data-ttu-id="be0d4-116">*конкретного*</span><span class="sxs-lookup"><span data-stu-id="be0d4-116">*a*</span></span> 
</dt> <dd>

<span data-ttu-id="be0d4-117">Альфа-компонент цвета.</span><span class="sxs-lookup"><span data-stu-id="be0d4-117">Alpha component of the color.</span></span> <span data-ttu-id="be0d4-118">Это значение должно находиться в диапазоне от 0 до 255.</span><span class="sxs-lookup"><span data-stu-id="be0d4-118">This value must be in the range 0 through 255.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="be0d4-119">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="be0d4-119">Return value</span></span>

<span data-ttu-id="be0d4-120">Возвращает значение [**D3DCOLOR**](d3dcolor.md) , соответствующее указанным значениям RGBA.</span><span class="sxs-lookup"><span data-stu-id="be0d4-120">Returns the [**D3DCOLOR**](d3dcolor.md) value that corresponds to the supplied RGBA values.</span></span>

## <a name="requirements"></a><span data-ttu-id="be0d4-121">Требования</span><span class="sxs-lookup"><span data-stu-id="be0d4-121">Requirements</span></span>



| <span data-ttu-id="be0d4-122">Требование</span><span class="sxs-lookup"><span data-stu-id="be0d4-122">Requirement</span></span> | <span data-ttu-id="be0d4-123">Значение</span><span class="sxs-lookup"><span data-stu-id="be0d4-123">Value</span></span> |
|-------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="be0d4-124">Header</span><span class="sxs-lookup"><span data-stu-id="be0d4-124">Header</span></span><br/> | <dl> <span data-ttu-id="be0d4-125"><dt>D3d9types. h</dt></span><span class="sxs-lookup"><span data-stu-id="be0d4-125"><dt>D3d9types.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="be0d4-126">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="be0d4-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="be0d4-127">Макросы</span><span class="sxs-lookup"><span data-stu-id="be0d4-127">Macros</span></span>](dx9-graphics-reference-d3d-macros.md)
</dt> <dt>

[<span data-ttu-id="be0d4-128">**D3DCOLOR \_ ARGB**</span><span class="sxs-lookup"><span data-stu-id="be0d4-128">**D3DCOLOR\_ARGB**</span></span>](d3dcolor-argb.md)
</dt> <dt>

[<span data-ttu-id="be0d4-129">**D3DCOLOR \_ ксргб**</span><span class="sxs-lookup"><span data-stu-id="be0d4-129">**D3DCOLOR\_XRGB**</span></span>](d3dcolor-xrgb.md)
</dt> </dl>

 

 




