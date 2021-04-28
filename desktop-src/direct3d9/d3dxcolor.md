---
description: Структура D3DXCOLOR (D3dx9math. h) — описывает значения цвета.
ms.assetid: 53d3176a-f727-498e-8bea-0e30e0a1c66e
title: Структура D3DXCOLOR (D3dx9math. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXCOLOR
api_type:
- HeaderDef
api_location:
- d3dx9math.h
ms.openlocfilehash: 58b02abc49b695169674a2579b73dc2359801a73
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2021
ms.locfileid: "108115932"
---
# <a name="d3dxcolor-structure-d3dx9mathh"></a><span data-ttu-id="205bf-103">Структура D3DXCOLOR (D3dx9math. h)</span><span class="sxs-lookup"><span data-stu-id="205bf-103">D3DXCOLOR structure (D3dx9math.h)</span></span>

<span data-ttu-id="205bf-104">Описывает значения цвета.</span><span class="sxs-lookup"><span data-stu-id="205bf-104">Describes color values.</span></span>

## <a name="syntax"></a><span data-ttu-id="205bf-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="205bf-105">Syntax</span></span>


```C++
typedef struct D3DXCOLOR {
  FLOAT r;
  FLOAT g;
  FLOAT b;
  FLOAT a;
} D3DXCOLOR, *LPD3DXCOLOR;
```



## <a name="members"></a><span data-ttu-id="205bf-106">Члены</span><span class="sxs-lookup"><span data-stu-id="205bf-106">Members</span></span>

<dl> <dt>

<span data-ttu-id="205bf-107">**r**</span><span class="sxs-lookup"><span data-stu-id="205bf-107">**r**</span></span>
</dt> <dd>

<span data-ttu-id="205bf-108">Тип: **[ **float**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="205bf-108">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="205bf-109">Красный компонент цвета.</span><span class="sxs-lookup"><span data-stu-id="205bf-109">Red component of the color.</span></span>

</dd> <dt>

<span data-ttu-id="205bf-110">**g**</span><span class="sxs-lookup"><span data-stu-id="205bf-110">**g**</span></span>
</dt> <dd>

<span data-ttu-id="205bf-111">Тип: **[ **float**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="205bf-111">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="205bf-112">Зеленый компонент цвета.</span><span class="sxs-lookup"><span data-stu-id="205bf-112">Green component of the color.</span></span>

</dd> <dt>

<span data-ttu-id="205bf-113">**b**</span><span class="sxs-lookup"><span data-stu-id="205bf-113">**b**</span></span>
</dt> <dd>

<span data-ttu-id="205bf-114">Тип: **[ **float**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="205bf-114">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="205bf-115">Синий компонент цвета.</span><span class="sxs-lookup"><span data-stu-id="205bf-115">Blue component of the color.</span></span>

</dd> <dt>

<span data-ttu-id="205bf-116">**конкретного**</span><span class="sxs-lookup"><span data-stu-id="205bf-116">**a**</span></span>
</dt> <dd>

<span data-ttu-id="205bf-117">Тип: **[ **float**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="205bf-117">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="205bf-118">Альфа-компонент цвета.</span><span class="sxs-lookup"><span data-stu-id="205bf-118">Alpha component of the color.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="205bf-119">Remarks</span><span class="sxs-lookup"><span data-stu-id="205bf-119">Remarks</span></span>

<span data-ttu-id="205bf-120">Программисты C++ могут воспользоваться преимуществами перегрузки операторов и приведения типов с [**расширениями D3DXCOLOR**](d3dxcolor-extensions.md), которые реализуют перегруженные конструкторы, а также операторы присваивания, унарные и бинарные (включая равенство).</span><span class="sxs-lookup"><span data-stu-id="205bf-120">C++ programmers can take advantage of operator overloading and type casting with the [**D3DXCOLOR Extensions**](d3dxcolor-extensions.md), which implement overloaded constructors, as well as assignment, unary, and binary (including equality) operators.</span></span>

## <a name="requirements"></a><span data-ttu-id="205bf-121">Требования</span><span class="sxs-lookup"><span data-stu-id="205bf-121">Requirements</span></span>



| <span data-ttu-id="205bf-122">Требование</span><span class="sxs-lookup"><span data-stu-id="205bf-122">Requirement</span></span> | <span data-ttu-id="205bf-123">Значение</span><span class="sxs-lookup"><span data-stu-id="205bf-123">Value</span></span> |
|-------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="205bf-124">Header</span><span class="sxs-lookup"><span data-stu-id="205bf-124">Header</span></span><br/> | <dl> <span data-ttu-id="205bf-125"><dt>D3dx9math. h</dt></span><span class="sxs-lookup"><span data-stu-id="205bf-125"><dt>D3dx9math.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="205bf-126">См. также</span><span class="sxs-lookup"><span data-stu-id="205bf-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="205bf-127">Структуры D3DX</span><span class="sxs-lookup"><span data-stu-id="205bf-127">D3DX Structures</span></span>](dx9-graphics-reference-d3dx-structures.md)
</dt> </dl>

 

 
