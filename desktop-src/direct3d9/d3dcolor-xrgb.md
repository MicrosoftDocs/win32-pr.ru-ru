---
description: Инициализирует цвет с переданными значениями красного, зеленого и синего.
ms.assetid: 832a4a78-c166-4e45-a907-57730da1c2c8
title: Макрос D3DCOLOR_XRGB (D3d9types. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DCOLOR_XRGB
api_type:
- HeaderDef
api_location:
- D3d9types.h
ms.openlocfilehash: 4932e34979b0913f27874e57cfa881f18fb16364
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/15/2021
ms.locfileid: "104424349"
---
# <a name="d3dcolor_xrgb-macro"></a><span data-ttu-id="4758c-103">\_Макрос D3DCOLOR ксргб</span><span class="sxs-lookup"><span data-stu-id="4758c-103">D3DCOLOR\_XRGB macro</span></span>

<span data-ttu-id="4758c-104">Инициализирует цвет с переданными значениями красного, зеленого и синего.</span><span class="sxs-lookup"><span data-stu-id="4758c-104">Initializes a color with the supplied red, green, and blue values.</span></span>

## <a name="syntax"></a><span data-ttu-id="4758c-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="4758c-105">Syntax</span></span>


```C++
D3DCOLOR D3DCOLOR_XRGB(
   int r,
   int g,
   int b
);
```



## <a name="parameters"></a><span data-ttu-id="4758c-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="4758c-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="4758c-107">*r*</span><span class="sxs-lookup"><span data-stu-id="4758c-107">*r*</span></span> 
</dt> <dd>

<span data-ttu-id="4758c-108">Красный компонент цвета.</span><span class="sxs-lookup"><span data-stu-id="4758c-108">Red component of the color.</span></span> <span data-ttu-id="4758c-109">Это значение должно находиться в диапазоне от 0 до 255.</span><span class="sxs-lookup"><span data-stu-id="4758c-109">This value must be in the range 0 through 255.</span></span>

</dd> <dt>

<span data-ttu-id="4758c-110">*g*</span><span class="sxs-lookup"><span data-stu-id="4758c-110">*g*</span></span> 
</dt> <dd>

<span data-ttu-id="4758c-111">Зеленый компонент цвета.</span><span class="sxs-lookup"><span data-stu-id="4758c-111">Green component of the color.</span></span> <span data-ttu-id="4758c-112">Это значение должно находиться в диапазоне от 0 до 255.</span><span class="sxs-lookup"><span data-stu-id="4758c-112">This value must be in the range 0 through 255.</span></span>

</dd> <dt>

<span data-ttu-id="4758c-113">*b*</span><span class="sxs-lookup"><span data-stu-id="4758c-113">*b*</span></span> 
</dt> <dd>

<span data-ttu-id="4758c-114">Синий компонент цвета.</span><span class="sxs-lookup"><span data-stu-id="4758c-114">Blue component of the color.</span></span> <span data-ttu-id="4758c-115">Это значение должно находиться в диапазоне от 0 до 255.</span><span class="sxs-lookup"><span data-stu-id="4758c-115">This value must be in the range 0 through 255.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="4758c-116">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="4758c-116">Return value</span></span>

<span data-ttu-id="4758c-117">Возвращает значение [**D3DCOLOR**](d3dcolor.md) , соответствующее указанным значениям RGB.</span><span class="sxs-lookup"><span data-stu-id="4758c-117">Returns the [**D3DCOLOR**](d3dcolor.md) value that corresponds to the supplied RGB values.</span></span>

## <a name="requirements"></a><span data-ttu-id="4758c-118">Требования</span><span class="sxs-lookup"><span data-stu-id="4758c-118">Requirements</span></span>



| <span data-ttu-id="4758c-119">Требование</span><span class="sxs-lookup"><span data-stu-id="4758c-119">Requirement</span></span> | <span data-ttu-id="4758c-120">Значение</span><span class="sxs-lookup"><span data-stu-id="4758c-120">Value</span></span> |
|-------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="4758c-121">Header</span><span class="sxs-lookup"><span data-stu-id="4758c-121">Header</span></span><br/> | <dl> <span data-ttu-id="4758c-122"><dt>D3d9types. h</dt></span><span class="sxs-lookup"><span data-stu-id="4758c-122"><dt>D3d9types.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="4758c-123">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="4758c-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="4758c-124">Макросы</span><span class="sxs-lookup"><span data-stu-id="4758c-124">Macros</span></span>](dx9-graphics-reference-d3d-macros.md)
</dt> <dt>

[<span data-ttu-id="4758c-125">**D3DCOLOR \_ ARGB**</span><span class="sxs-lookup"><span data-stu-id="4758c-125">**D3DCOLOR\_ARGB**</span></span>](d3dcolor-argb.md)
</dt> <dt>

[<span data-ttu-id="4758c-126">**D3DCOLOR \_ RGBA**</span><span class="sxs-lookup"><span data-stu-id="4758c-126">**D3DCOLOR\_RGBA**</span></span>](d3dcolor-rgba.md)
</dt> </dl>

 

 




