---
description: Инициализирует цвет с заданными значениями красного, зеленого, синего и альфа-точечных чисел.
ms.assetid: 61825e33-4150-47cd-97f2-2144434a45e2
title: Макрос D3DCOLOR_COLORVALUE (D3d9types. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DCOLOR_COLORVALUE
api_type:
- HeaderDef
api_location:
- D3d9types.h
ms.openlocfilehash: 3d5bb780a5999d8931335da1e9f49ad8af88dc12
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/15/2021
ms.locfileid: "103820964"
---
# <a name="d3dcolor_colorvalue-macro"></a><span data-ttu-id="ddefd-103">\_Макрос D3DCOLOR колорвалуе</span><span class="sxs-lookup"><span data-stu-id="ddefd-103">D3DCOLOR\_COLORVALUE macro</span></span>

<span data-ttu-id="ddefd-104">Инициализирует цвет с заданными значениями красного, зеленого, синего и альфа-точечных чисел.</span><span class="sxs-lookup"><span data-stu-id="ddefd-104">Initializes a color with the supplied red, green, blue, and alpha floating-point values.</span></span>

## <a name="syntax"></a><span data-ttu-id="ddefd-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="ddefd-105">Syntax</span></span>


```C++
D3DCOLOR D3DCOLOR_COLORVALUE(
   float r,
   float g,
   float b,
   float a
);
```



## <a name="parameters"></a><span data-ttu-id="ddefd-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="ddefd-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="ddefd-107">*r*</span><span class="sxs-lookup"><span data-stu-id="ddefd-107">*r*</span></span> 
</dt> <dd>

<span data-ttu-id="ddefd-108">Красный компонент цвета.</span><span class="sxs-lookup"><span data-stu-id="ddefd-108">Red component of the color.</span></span> <span data-ttu-id="ddefd-109">Это значение должно быть значением с плавающей запятой в диапазоне от 0,0 до 1,0.</span><span class="sxs-lookup"><span data-stu-id="ddefd-109">This value must be a floating-point value in the range 0.0 through 1.0.</span></span>

</dd> <dt>

<span data-ttu-id="ddefd-110">*g*</span><span class="sxs-lookup"><span data-stu-id="ddefd-110">*g*</span></span> 
</dt> <dd>

<span data-ttu-id="ddefd-111">Зеленый компонент цвета.</span><span class="sxs-lookup"><span data-stu-id="ddefd-111">Green component of the color.</span></span> <span data-ttu-id="ddefd-112">Это значение должно быть значением с плавающей запятой в диапазоне от 0,0 до 1,0.</span><span class="sxs-lookup"><span data-stu-id="ddefd-112">This value must be a floating-point value in the range 0.0 through 1.0.</span></span>

</dd> <dt>

<span data-ttu-id="ddefd-113">*b*</span><span class="sxs-lookup"><span data-stu-id="ddefd-113">*b*</span></span> 
</dt> <dd>

<span data-ttu-id="ddefd-114">Синий компонент цвета.</span><span class="sxs-lookup"><span data-stu-id="ddefd-114">Blue component of the color.</span></span> <span data-ttu-id="ddefd-115">Это значение должно быть значением с плавающей запятой в диапазоне от 0,0 до 1,0.</span><span class="sxs-lookup"><span data-stu-id="ddefd-115">This value must be a floating-point value in the range 0.0 through 1.0.</span></span>

</dd> <dt>

<span data-ttu-id="ddefd-116">*конкретного*</span><span class="sxs-lookup"><span data-stu-id="ddefd-116">*a*</span></span> 
</dt> <dd>

<span data-ttu-id="ddefd-117">Альфа-компонент цвета.</span><span class="sxs-lookup"><span data-stu-id="ddefd-117">Alpha component of the color.</span></span> <span data-ttu-id="ddefd-118">Это значение должно быть значением с плавающей запятой в диапазоне от 0,0 до 1,0.</span><span class="sxs-lookup"><span data-stu-id="ddefd-118">This value must be a floating-point value in the range 0.0 through 1.0.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="ddefd-119">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="ddefd-119">Return value</span></span>

<span data-ttu-id="ddefd-120">Возвращает значение [**D3DCOLOR**](d3dcolor.md) , соответствующее указанным значениям RGBA.</span><span class="sxs-lookup"><span data-stu-id="ddefd-120">Returns the [**D3DCOLOR**](d3dcolor.md) value that corresponds to the supplied RGBA values.</span></span>

## <a name="requirements"></a><span data-ttu-id="ddefd-121">Требования</span><span class="sxs-lookup"><span data-stu-id="ddefd-121">Requirements</span></span>



| <span data-ttu-id="ddefd-122">Требование</span><span class="sxs-lookup"><span data-stu-id="ddefd-122">Requirement</span></span> | <span data-ttu-id="ddefd-123">Значение</span><span class="sxs-lookup"><span data-stu-id="ddefd-123">Value</span></span> |
|-------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="ddefd-124">Header</span><span class="sxs-lookup"><span data-stu-id="ddefd-124">Header</span></span><br/> | <dl> <span data-ttu-id="ddefd-125"><dt>D3d9types. h</dt></span><span class="sxs-lookup"><span data-stu-id="ddefd-125"><dt>D3d9types.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="ddefd-126">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="ddefd-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ddefd-127">Макросы</span><span class="sxs-lookup"><span data-stu-id="ddefd-127">Macros</span></span>](dx9-graphics-reference-d3d-macros.md)
</dt> </dl>

 

 




