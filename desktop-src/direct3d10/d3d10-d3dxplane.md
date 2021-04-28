---
description: Структура D3DXPLANE (D3DX10Math. h) — описывает плоскость.
ms.assetid: c6da7343-a4f3-4cac-855b-14bd70c0d3c2
title: Структура D3DXPLANE (D3DX10Math. h)
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
- D3DX10Math.h
ms.openlocfilehash: 440246fb47a851f9f5339c72a484a2cb59e8f662
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2021
ms.locfileid: "108103332"
---
# <a name="d3dxplane-structure-d3dx10mathh"></a><span data-ttu-id="0a876-103">Структура D3DXPLANE (D3DX10Math. h)</span><span class="sxs-lookup"><span data-stu-id="0a876-103">D3DXPLANE structure (D3DX10Math.h)</span></span>

<span data-ttu-id="0a876-104">Описывает плоскость.</span><span class="sxs-lookup"><span data-stu-id="0a876-104">Describes a plane.</span></span>

## <a name="syntax"></a><span data-ttu-id="0a876-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="0a876-105">Syntax</span></span>


```C++
typedef struct D3DXPLANE {
  FLOAT a;
  FLOAT b;
  FLOAT c;
  FLOAT d;
} D3DXPLANE, *LPD3DXPLANE;
```



## <a name="members"></a><span data-ttu-id="0a876-106">Члены</span><span class="sxs-lookup"><span data-stu-id="0a876-106">Members</span></span>

<dl> <dt>

<span data-ttu-id="0a876-107">**конкретного**</span><span class="sxs-lookup"><span data-stu-id="0a876-107">**a**</span></span>
</dt> <dd>

<span data-ttu-id="0a876-108">Тип: **[ **float**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="0a876-108">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="0a876-109">Коэффициент обтравочной плоскости в уравнении общей плоскости.</span><span class="sxs-lookup"><span data-stu-id="0a876-109">The a coefficient of the clipping plane in the general plane equation.</span></span> <span data-ttu-id="0a876-110">См. заметки.</span><span class="sxs-lookup"><span data-stu-id="0a876-110">See Remarks.</span></span>

</dd> <dt>

<span data-ttu-id="0a876-111">**b**</span><span class="sxs-lookup"><span data-stu-id="0a876-111">**b**</span></span>
</dt> <dd>

<span data-ttu-id="0a876-112">Тип: **[ **float**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="0a876-112">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="0a876-113">Коэффициент b плоскости обрезки в уравнении общей плоскости.</span><span class="sxs-lookup"><span data-stu-id="0a876-113">The b coefficient of the clipping plane in the general plane equation.</span></span> <span data-ttu-id="0a876-114">См. заметки.</span><span class="sxs-lookup"><span data-stu-id="0a876-114">See Remarks.</span></span>

</dd> <dt>

<span data-ttu-id="0a876-115">**c**</span><span class="sxs-lookup"><span data-stu-id="0a876-115">**c**</span></span>
</dt> <dd>

<span data-ttu-id="0a876-116">Тип: **[ **float**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="0a876-116">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="0a876-117">Коэффициент на c для плоскости обрезки в уравнении общей плоскости.</span><span class="sxs-lookup"><span data-stu-id="0a876-117">The c coefficient of the clipping plane in the general plane equation.</span></span> <span data-ttu-id="0a876-118">См. заметки.</span><span class="sxs-lookup"><span data-stu-id="0a876-118">See Remarks.</span></span>

</dd> <dt>

<span data-ttu-id="0a876-119">**d**</span><span class="sxs-lookup"><span data-stu-id="0a876-119">**d**</span></span>
</dt> <dd>

<span data-ttu-id="0a876-120">Тип: **[ **float**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="0a876-120">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="0a876-121">Коэффициент d плоскости обрезки в уравнении общей плоскости.</span><span class="sxs-lookup"><span data-stu-id="0a876-121">The d coefficient of the clipping plane in the general plane equation.</span></span> <span data-ttu-id="0a876-122">См. заметки.</span><span class="sxs-lookup"><span data-stu-id="0a876-122">See Remarks.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="0a876-123">Remarks</span><span class="sxs-lookup"><span data-stu-id="0a876-123">Remarks</span></span>

<span data-ttu-id="0a876-124">Члены структуры **D3DXPLANE** имеют форму уравнения «общая плоскость».</span><span class="sxs-lookup"><span data-stu-id="0a876-124">The members of the **D3DXPLANE** structure take the form of the general plane equation.</span></span> <span data-ttu-id="0a876-125">Они помещаются в уравнение общей плоскости, чтобы AX + by + CZ + DW = 0.</span><span class="sxs-lookup"><span data-stu-id="0a876-125">They fit into the general plane equation so that ax + by + cz + dw = 0.</span></span>

## <a name="requirements"></a><span data-ttu-id="0a876-126">Требования</span><span class="sxs-lookup"><span data-stu-id="0a876-126">Requirements</span></span>



| <span data-ttu-id="0a876-127">Требование</span><span class="sxs-lookup"><span data-stu-id="0a876-127">Requirement</span></span> | <span data-ttu-id="0a876-128">Значение</span><span class="sxs-lookup"><span data-stu-id="0a876-128">Value</span></span> |
|-------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="0a876-129">Header</span><span class="sxs-lookup"><span data-stu-id="0a876-129">Header</span></span><br/> | <dl> <span data-ttu-id="0a876-130"><dt>D3DX10Math. h</dt></span><span class="sxs-lookup"><span data-stu-id="0a876-130"><dt>D3DX10Math.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="0a876-131">См. также</span><span class="sxs-lookup"><span data-stu-id="0a876-131">See also</span></span>

<dl> <dt>

[<span data-ttu-id="0a876-132">Структуры D3DX</span><span class="sxs-lookup"><span data-stu-id="0a876-132">D3DX Structures</span></span>](d3d10-graphics-reference-d3dx10-structures.md)
</dt> </dl>

 

 
