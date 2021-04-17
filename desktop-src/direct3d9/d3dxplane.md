---
description: Описывает плоскость.
ms.assetid: ffca4650-9788-4559-8f6b-a4e5db29ce55
title: Структура D3DXPLANE (D3dx9math. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXPLANE
api_type:
- HeaderDef
api_location:
- d3dx9math.h
ms.openlocfilehash: 260f9555313aea3443f0728f2b50189228429803
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/15/2021
ms.locfileid: "105713463"
---
# <a name="d3dxplane-structure-d3dx9mathh"></a><span data-ttu-id="d70fe-103">Структура D3DXPLANE (D3dx9math. h)</span><span class="sxs-lookup"><span data-stu-id="d70fe-103">D3DXPLANE structure (D3dx9math.h)</span></span>

<span data-ttu-id="d70fe-104">Описывает плоскость.</span><span class="sxs-lookup"><span data-stu-id="d70fe-104">Describes a plane.</span></span>

## <a name="syntax"></a><span data-ttu-id="d70fe-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="d70fe-105">Syntax</span></span>


```C++
typedef struct D3DXPLANE {
  FLOAT a;
  FLOAT b;
  FLOAT c;
  FLOAT d;
} D3DXPLANE, *LPD3DXPLANE;
```



## <a name="members"></a><span data-ttu-id="d70fe-106">Члены</span><span class="sxs-lookup"><span data-stu-id="d70fe-106">Members</span></span>

<dl> <dt>

<span data-ttu-id="d70fe-107">**конкретного**</span><span class="sxs-lookup"><span data-stu-id="d70fe-107">**a**</span></span>
</dt> <dd>

<span data-ttu-id="d70fe-108">Тип: **[ **float**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="d70fe-108">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="d70fe-109">Коэффициент обтравочной плоскости в уравнении общей плоскости.</span><span class="sxs-lookup"><span data-stu-id="d70fe-109">The a coefficient of the clipping plane in the general plane equation.</span></span> <span data-ttu-id="d70fe-110">См. заметки.</span><span class="sxs-lookup"><span data-stu-id="d70fe-110">See Remarks.</span></span>

</dd> <dt>

<span data-ttu-id="d70fe-111">**b**</span><span class="sxs-lookup"><span data-stu-id="d70fe-111">**b**</span></span>
</dt> <dd>

<span data-ttu-id="d70fe-112">Тип: **[ **float**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="d70fe-112">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="d70fe-113">Коэффициент b плоскости обрезки в уравнении общей плоскости.</span><span class="sxs-lookup"><span data-stu-id="d70fe-113">The b coefficient of the clipping plane in the general plane equation.</span></span> <span data-ttu-id="d70fe-114">См. заметки.</span><span class="sxs-lookup"><span data-stu-id="d70fe-114">See Remarks.</span></span>

</dd> <dt>

<span data-ttu-id="d70fe-115">**c**</span><span class="sxs-lookup"><span data-stu-id="d70fe-115">**c**</span></span>
</dt> <dd>

<span data-ttu-id="d70fe-116">Тип: **[ **float**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="d70fe-116">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="d70fe-117">Коэффициент на c для плоскости обрезки в уравнении общей плоскости.</span><span class="sxs-lookup"><span data-stu-id="d70fe-117">The c coefficient of the clipping plane in the general plane equation.</span></span> <span data-ttu-id="d70fe-118">См. заметки.</span><span class="sxs-lookup"><span data-stu-id="d70fe-118">See Remarks.</span></span>

</dd> <dt>

<span data-ttu-id="d70fe-119">**d**</span><span class="sxs-lookup"><span data-stu-id="d70fe-119">**d**</span></span>
</dt> <dd>

<span data-ttu-id="d70fe-120">Тип: **[ **float**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="d70fe-120">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="d70fe-121">Коэффициент d плоскости обрезки в уравнении общей плоскости.</span><span class="sxs-lookup"><span data-stu-id="d70fe-121">The d coefficient of the clipping plane in the general plane equation.</span></span> <span data-ttu-id="d70fe-122">См. заметки.</span><span class="sxs-lookup"><span data-stu-id="d70fe-122">See Remarks.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="d70fe-123">Комментарии</span><span class="sxs-lookup"><span data-stu-id="d70fe-123">Remarks</span></span>

<span data-ttu-id="d70fe-124">Члены структуры **D3DXPLANE** имеют форму уравнения «общая плоскость».</span><span class="sxs-lookup"><span data-stu-id="d70fe-124">The members of the **D3DXPLANE** structure take the form of the general plane equation.</span></span> <span data-ttu-id="d70fe-125">Они помещаются в уравнение общей **плоскости, чтобы x**+ **b** y + **c** z + **d** w = 0.</span><span class="sxs-lookup"><span data-stu-id="d70fe-125">They fit into the general plane equation so that **a** x + **b** y + **c** z + **d** w = 0.</span></span>

<span data-ttu-id="d70fe-126">Программисты C++ могут воспользоваться преимуществами перегрузки операторов и приведения типов с [**расширениями D3DXPLANE**](d3dxplane-extensions.md) , которые реализуют перегруженные конструкторы и операторы присваивания, унарные и бинарные (включая равенство).</span><span class="sxs-lookup"><span data-stu-id="d70fe-126">C++ programmers can take advantage of operator overloading and type casting with the [**D3DXPLANE Extensions**](d3dxplane-extensions.md) which implement overloaded constructors and assignment, unary, and binary (including equality) operators.</span></span>

## <a name="requirements"></a><span data-ttu-id="d70fe-127">Требования</span><span class="sxs-lookup"><span data-stu-id="d70fe-127">Requirements</span></span>



| <span data-ttu-id="d70fe-128">Требование</span><span class="sxs-lookup"><span data-stu-id="d70fe-128">Requirement</span></span> | <span data-ttu-id="d70fe-129">Значение</span><span class="sxs-lookup"><span data-stu-id="d70fe-129">Value</span></span> |
|-------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="d70fe-130">Header</span><span class="sxs-lookup"><span data-stu-id="d70fe-130">Header</span></span><br/> | <dl> <span data-ttu-id="d70fe-131"><dt>D3dx9math. h</dt></span><span class="sxs-lookup"><span data-stu-id="d70fe-131"><dt>D3dx9math.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="d70fe-132">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="d70fe-132">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d70fe-133">Структуры D3DX</span><span class="sxs-lookup"><span data-stu-id="d70fe-133">D3DX Structures</span></span>](dx9-graphics-reference-d3dx-structures.md)
</dt> </dl>

 

 
