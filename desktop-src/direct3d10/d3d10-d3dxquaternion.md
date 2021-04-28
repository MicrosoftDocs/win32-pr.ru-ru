---
description: Структура D3DXQUATERNION (D3DX10Math. h) — описывает кватернион.
ms.assetid: e6cb45b2-3132-4315-b02d-a3dfc444f8cc
title: Структура D3DXQUATERNION (D3DX10Math. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXQUATERNION
api_type:
- HeaderDef
api_location:
- D3DX10Math.h
ms.openlocfilehash: dac880607cf482b409c407b43992747af4aa39a9
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2021
ms.locfileid: "108103252"
---
# <a name="d3dxquaternion-structure-d3dx10mathh"></a><span data-ttu-id="fce55-103">Структура D3DXQUATERNION (D3DX10Math. h)</span><span class="sxs-lookup"><span data-stu-id="fce55-103">D3DXQUATERNION structure (D3DX10Math.h)</span></span>

<span data-ttu-id="fce55-104">Описывает кватернион.</span><span class="sxs-lookup"><span data-stu-id="fce55-104">Describes a quaternion.</span></span>

## <a name="syntax"></a><span data-ttu-id="fce55-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="fce55-105">Syntax</span></span>


```C++
typedef struct D3DXQUATERNION {
  FLOAT x;
  FLOAT y;
  FLOAT z;
  FLOAT w;
} D3DXQUATERNION, *LPD3DXQUATERNION;
```



## <a name="members"></a><span data-ttu-id="fce55-106">Члены</span><span class="sxs-lookup"><span data-stu-id="fce55-106">Members</span></span>

<dl> <dt>

<span data-ttu-id="fce55-107">**x**</span><span class="sxs-lookup"><span data-stu-id="fce55-107">**x**</span></span>
</dt> <dd>

<span data-ttu-id="fce55-108">Тип: **[ **float**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="fce55-108">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="fce55-109">Компонент x.</span><span class="sxs-lookup"><span data-stu-id="fce55-109">The x-component.</span></span>

</dd> <dt>

<span data-ttu-id="fce55-110">**y**</span><span class="sxs-lookup"><span data-stu-id="fce55-110">**y**</span></span>
</dt> <dd>

<span data-ttu-id="fce55-111">Тип: **[ **float**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="fce55-111">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="fce55-112">Компонент y.</span><span class="sxs-lookup"><span data-stu-id="fce55-112">The y-component.</span></span>

</dd> <dt>

<span data-ttu-id="fce55-113">**z**</span><span class="sxs-lookup"><span data-stu-id="fce55-113">**z**</span></span>
</dt> <dd>

<span data-ttu-id="fce55-114">Тип: **[ **float**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="fce55-114">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="fce55-115">Компонент z.</span><span class="sxs-lookup"><span data-stu-id="fce55-115">The z-component.</span></span>

</dd> <dt>

<span data-ttu-id="fce55-116">**w**</span><span class="sxs-lookup"><span data-stu-id="fce55-116">**w**</span></span>
</dt> <dd>

<span data-ttu-id="fce55-117">Тип: **[ **float**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="fce55-117">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="fce55-118">Компонент w-Component.</span><span class="sxs-lookup"><span data-stu-id="fce55-118">The w-component.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="fce55-119">Remarks</span><span class="sxs-lookup"><span data-stu-id="fce55-119">Remarks</span></span>

<span data-ttu-id="fce55-120">Кватернион добавляет четвертый элемент к \[ значениям x, y, z \] , определяющим вектор, что приводит к произвольным векторам 4d.</span><span class="sxs-lookup"><span data-stu-id="fce55-120">Quaternions add a fourth element to the \[ x, y, z\] values that define a vector, resulting in arbitrary 4D vectors.</span></span> <span data-ttu-id="fce55-121">Однако ниже показано, как каждый элемент единичного кватерниона связан с поворотом по оси (где q представляет единицу кватерниона (x, y, z, w), ось нормализована, а тета — желаемый поворот CCW по оси):</span><span class="sxs-lookup"><span data-stu-id="fce55-121">However, the following illustrates how each element of a unit quaternion relates to an axis-angle rotation (where q represents a unit quaternion (x, y, z, w), axis is normalized, and theta is the desired CCW rotation about the axis):</span></span>


```
q.x = sin(theta/2) * axis.x
q.y = sin(theta/2) * axis.y
q.z = sin(theta/2) * axis.z
q.w = cos(theta/2)
```



## <a name="requirements"></a><span data-ttu-id="fce55-122">Требования</span><span class="sxs-lookup"><span data-stu-id="fce55-122">Requirements</span></span>



| <span data-ttu-id="fce55-123">Требование</span><span class="sxs-lookup"><span data-stu-id="fce55-123">Requirement</span></span> | <span data-ttu-id="fce55-124">Значение</span><span class="sxs-lookup"><span data-stu-id="fce55-124">Value</span></span> |
|-------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="fce55-125">Header</span><span class="sxs-lookup"><span data-stu-id="fce55-125">Header</span></span><br/> | <dl> <span data-ttu-id="fce55-126"><dt>D3DX10Math. h</dt></span><span class="sxs-lookup"><span data-stu-id="fce55-126"><dt>D3DX10Math.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="fce55-127">См. также</span><span class="sxs-lookup"><span data-stu-id="fce55-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="fce55-128">Структуры D3DX</span><span class="sxs-lookup"><span data-stu-id="fce55-128">D3DX Structures</span></span>](d3d10-graphics-reference-d3dx10-structures.md)
</dt> </dl>

 

 
