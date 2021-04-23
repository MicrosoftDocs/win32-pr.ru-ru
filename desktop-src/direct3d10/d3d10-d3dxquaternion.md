---
description: Описывает кватернион.
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
ms.openlocfilehash: 405e48c99d7298708af193016930a8defdf9d600
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/15/2021
ms.locfileid: "104355330"
---
# <a name="d3dxquaternion-structure-d3dx10mathh"></a><span data-ttu-id="28c5a-103">Структура D3DXQUATERNION (D3DX10Math. h)</span><span class="sxs-lookup"><span data-stu-id="28c5a-103">D3DXQUATERNION structure (D3DX10Math.h)</span></span>

<span data-ttu-id="28c5a-104">Описывает кватернион.</span><span class="sxs-lookup"><span data-stu-id="28c5a-104">Describes a quaternion.</span></span>

## <a name="syntax"></a><span data-ttu-id="28c5a-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="28c5a-105">Syntax</span></span>


```C++
typedef struct D3DXQUATERNION {
  FLOAT x;
  FLOAT y;
  FLOAT z;
  FLOAT w;
} D3DXQUATERNION, *LPD3DXQUATERNION;
```



## <a name="members"></a><span data-ttu-id="28c5a-106">Члены</span><span class="sxs-lookup"><span data-stu-id="28c5a-106">Members</span></span>

<dl> <dt>

<span data-ttu-id="28c5a-107">**x**</span><span class="sxs-lookup"><span data-stu-id="28c5a-107">**x**</span></span>
</dt> <dd>

<span data-ttu-id="28c5a-108">Тип: **[ **float**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="28c5a-108">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="28c5a-109">Компонент x.</span><span class="sxs-lookup"><span data-stu-id="28c5a-109">The x-component.</span></span>

</dd> <dt>

<span data-ttu-id="28c5a-110">**y**</span><span class="sxs-lookup"><span data-stu-id="28c5a-110">**y**</span></span>
</dt> <dd>

<span data-ttu-id="28c5a-111">Тип: **[ **float**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="28c5a-111">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="28c5a-112">Компонент y.</span><span class="sxs-lookup"><span data-stu-id="28c5a-112">The y-component.</span></span>

</dd> <dt>

<span data-ttu-id="28c5a-113">**гармошкой**</span><span class="sxs-lookup"><span data-stu-id="28c5a-113">**z**</span></span>
</dt> <dd>

<span data-ttu-id="28c5a-114">Тип: **[ **float**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="28c5a-114">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="28c5a-115">Компонент z.</span><span class="sxs-lookup"><span data-stu-id="28c5a-115">The z-component.</span></span>

</dd> <dt>

<span data-ttu-id="28c5a-116">**w**</span><span class="sxs-lookup"><span data-stu-id="28c5a-116">**w**</span></span>
</dt> <dd>

<span data-ttu-id="28c5a-117">Тип: **[ **float**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="28c5a-117">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="28c5a-118">Компонент w-Component.</span><span class="sxs-lookup"><span data-stu-id="28c5a-118">The w-component.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="28c5a-119">Комментарии</span><span class="sxs-lookup"><span data-stu-id="28c5a-119">Remarks</span></span>

<span data-ttu-id="28c5a-120">Кватернион добавляет четвертый элемент к \[ значениям x, y, z \] , определяющим вектор, что приводит к произвольным векторам 4d.</span><span class="sxs-lookup"><span data-stu-id="28c5a-120">Quaternions add a fourth element to the \[ x, y, z\] values that define a vector, resulting in arbitrary 4D vectors.</span></span> <span data-ttu-id="28c5a-121">Однако ниже показано, как каждый элемент единичного кватерниона связан с поворотом по оси (где q представляет единицу кватерниона (x, y, z, w), ось нормализована, а тета — желаемый поворот CCW по оси):</span><span class="sxs-lookup"><span data-stu-id="28c5a-121">However, the following illustrates how each element of a unit quaternion relates to an axis-angle rotation (where q represents a unit quaternion (x, y, z, w), axis is normalized, and theta is the desired CCW rotation about the axis):</span></span>


```
q.x = sin(theta/2) * axis.x
q.y = sin(theta/2) * axis.y
q.z = sin(theta/2) * axis.z
q.w = cos(theta/2)
```



## <a name="requirements"></a><span data-ttu-id="28c5a-122">Требования</span><span class="sxs-lookup"><span data-stu-id="28c5a-122">Requirements</span></span>



| <span data-ttu-id="28c5a-123">Требование</span><span class="sxs-lookup"><span data-stu-id="28c5a-123">Requirement</span></span> | <span data-ttu-id="28c5a-124">Значение</span><span class="sxs-lookup"><span data-stu-id="28c5a-124">Value</span></span> |
|-------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="28c5a-125">Header</span><span class="sxs-lookup"><span data-stu-id="28c5a-125">Header</span></span><br/> | <dl> <span data-ttu-id="28c5a-126"><dt>D3DX10Math. h</dt></span><span class="sxs-lookup"><span data-stu-id="28c5a-126"><dt>D3DX10Math.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="28c5a-127">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="28c5a-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="28c5a-128">Структуры D3DX</span><span class="sxs-lookup"><span data-stu-id="28c5a-128">D3DX Structures</span></span>](d3d10-graphics-reference-d3dx10-structures.md)
</dt> </dl>

 

 
