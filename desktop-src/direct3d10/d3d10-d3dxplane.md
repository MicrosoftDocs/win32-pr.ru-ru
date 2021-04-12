---
description: Описывает плоскость.
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
ms.openlocfilehash: 9949aec16e90a53e01e536255c20f442052bb98b
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/15/2021
ms.locfileid: "104355653"
---
# <a name="d3dxplane-structure-d3dx10mathh"></a><span data-ttu-id="064bc-103">Структура D3DXPLANE (D3DX10Math. h)</span><span class="sxs-lookup"><span data-stu-id="064bc-103">D3DXPLANE structure (D3DX10Math.h)</span></span>

<span data-ttu-id="064bc-104">Описывает плоскость.</span><span class="sxs-lookup"><span data-stu-id="064bc-104">Describes a plane.</span></span>

## <a name="syntax"></a><span data-ttu-id="064bc-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="064bc-105">Syntax</span></span>


```C++
typedef struct D3DXPLANE {
  FLOAT a;
  FLOAT b;
  FLOAT c;
  FLOAT d;
} D3DXPLANE, *LPD3DXPLANE;
```



## <a name="members"></a><span data-ttu-id="064bc-106">Члены</span><span class="sxs-lookup"><span data-stu-id="064bc-106">Members</span></span>

<dl> <dt>

<span data-ttu-id="064bc-107">**конкретного**</span><span class="sxs-lookup"><span data-stu-id="064bc-107">**a**</span></span>
</dt> <dd>

<span data-ttu-id="064bc-108">Тип: **[ **float**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="064bc-108">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="064bc-109">Коэффициент обтравочной плоскости в уравнении общей плоскости.</span><span class="sxs-lookup"><span data-stu-id="064bc-109">The a coefficient of the clipping plane in the general plane equation.</span></span> <span data-ttu-id="064bc-110">См. заметки.</span><span class="sxs-lookup"><span data-stu-id="064bc-110">See Remarks.</span></span>

</dd> <dt>

<span data-ttu-id="064bc-111">**b**</span><span class="sxs-lookup"><span data-stu-id="064bc-111">**b**</span></span>
</dt> <dd>

<span data-ttu-id="064bc-112">Тип: **[ **float**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="064bc-112">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="064bc-113">Коэффициент b плоскости обрезки в уравнении общей плоскости.</span><span class="sxs-lookup"><span data-stu-id="064bc-113">The b coefficient of the clipping plane in the general plane equation.</span></span> <span data-ttu-id="064bc-114">См. заметки.</span><span class="sxs-lookup"><span data-stu-id="064bc-114">See Remarks.</span></span>

</dd> <dt>

<span data-ttu-id="064bc-115">**c**</span><span class="sxs-lookup"><span data-stu-id="064bc-115">**c**</span></span>
</dt> <dd>

<span data-ttu-id="064bc-116">Тип: **[ **float**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="064bc-116">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="064bc-117">Коэффициент на c для плоскости обрезки в уравнении общей плоскости.</span><span class="sxs-lookup"><span data-stu-id="064bc-117">The c coefficient of the clipping plane in the general plane equation.</span></span> <span data-ttu-id="064bc-118">См. заметки.</span><span class="sxs-lookup"><span data-stu-id="064bc-118">See Remarks.</span></span>

</dd> <dt>

<span data-ttu-id="064bc-119">**d**</span><span class="sxs-lookup"><span data-stu-id="064bc-119">**d**</span></span>
</dt> <dd>

<span data-ttu-id="064bc-120">Тип: **[ **float**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="064bc-120">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="064bc-121">Коэффициент d плоскости обрезки в уравнении общей плоскости.</span><span class="sxs-lookup"><span data-stu-id="064bc-121">The d coefficient of the clipping plane in the general plane equation.</span></span> <span data-ttu-id="064bc-122">См. заметки.</span><span class="sxs-lookup"><span data-stu-id="064bc-122">See Remarks.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="064bc-123">Комментарии</span><span class="sxs-lookup"><span data-stu-id="064bc-123">Remarks</span></span>

<span data-ttu-id="064bc-124">Члены структуры **D3DXPLANE** имеют форму уравнения «общая плоскость».</span><span class="sxs-lookup"><span data-stu-id="064bc-124">The members of the **D3DXPLANE** structure take the form of the general plane equation.</span></span> <span data-ttu-id="064bc-125">Они помещаются в уравнение общей плоскости, чтобы AX + by + CZ + DW = 0.</span><span class="sxs-lookup"><span data-stu-id="064bc-125">They fit into the general plane equation so that ax + by + cz + dw = 0.</span></span>

## <a name="requirements"></a><span data-ttu-id="064bc-126">Требования</span><span class="sxs-lookup"><span data-stu-id="064bc-126">Requirements</span></span>



| <span data-ttu-id="064bc-127">Требование</span><span class="sxs-lookup"><span data-stu-id="064bc-127">Requirement</span></span> | <span data-ttu-id="064bc-128">Значение</span><span class="sxs-lookup"><span data-stu-id="064bc-128">Value</span></span> |
|-------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="064bc-129">Header</span><span class="sxs-lookup"><span data-stu-id="064bc-129">Header</span></span><br/> | <dl> <span data-ttu-id="064bc-130"><dt>D3DX10Math. h</dt></span><span class="sxs-lookup"><span data-stu-id="064bc-130"><dt>D3DX10Math.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="064bc-131">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="064bc-131">See also</span></span>

<dl> <dt>

[<span data-ttu-id="064bc-132">Структуры D3DX</span><span class="sxs-lookup"><span data-stu-id="064bc-132">D3DX Structures</span></span>](d3d10-graphics-reference-d3dx10-structures.md)
</dt> </dl>

 

 
