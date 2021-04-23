---
description: Описывает кватернион.
ms.assetid: 3d88ed17-5b0a-46d5-8fe6-d66e1fa26c13
title: Структура D3DXQUATERNION (D3dx9math. h)
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
- d3dx9math.h
ms.openlocfilehash: 59d3f147e8eb233b9197394bad738d19d9ceba5d
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/15/2021
ms.locfileid: "105703737"
---
# <a name="d3dxquaternion-structure-d3dx9mathh"></a><span data-ttu-id="be063-103">Структура D3DXQUATERNION (D3dx9math. h)</span><span class="sxs-lookup"><span data-stu-id="be063-103">D3DXQUATERNION structure (D3dx9math.h)</span></span>

<span data-ttu-id="be063-104">Описывает кватернион.</span><span class="sxs-lookup"><span data-stu-id="be063-104">Describes a quaternion.</span></span>

## <a name="syntax"></a><span data-ttu-id="be063-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="be063-105">Syntax</span></span>


```C++
typedef struct D3DXQUATERNION {
  FLOAT x;
  FLOAT y;
  FLOAT z;
  FLOAT w;
} D3DXQUATERNION, *LPD3DXQUATERNION;
```



## <a name="members"></a><span data-ttu-id="be063-106">Члены</span><span class="sxs-lookup"><span data-stu-id="be063-106">Members</span></span>

<dl> <dt>

<span data-ttu-id="be063-107">**x**</span><span class="sxs-lookup"><span data-stu-id="be063-107">**x**</span></span>
</dt> <dd>

<span data-ttu-id="be063-108">Тип: **[ **float**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="be063-108">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="be063-109">Компонент x.</span><span class="sxs-lookup"><span data-stu-id="be063-109">The x-component.</span></span>

</dd> <dt>

<span data-ttu-id="be063-110">**y**</span><span class="sxs-lookup"><span data-stu-id="be063-110">**y**</span></span>
</dt> <dd>

<span data-ttu-id="be063-111">Тип: **[ **float**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="be063-111">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="be063-112">Компонент y.</span><span class="sxs-lookup"><span data-stu-id="be063-112">The y-component.</span></span>

</dd> <dt>

<span data-ttu-id="be063-113">**гармошкой**</span><span class="sxs-lookup"><span data-stu-id="be063-113">**z**</span></span>
</dt> <dd>

<span data-ttu-id="be063-114">Тип: **[ **float**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="be063-114">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="be063-115">Компонент z.</span><span class="sxs-lookup"><span data-stu-id="be063-115">The z-component.</span></span>

</dd> <dt>

<span data-ttu-id="be063-116">**w**</span><span class="sxs-lookup"><span data-stu-id="be063-116">**w**</span></span>
</dt> <dd>

<span data-ttu-id="be063-117">Тип: **[ **float**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="be063-117">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="be063-118">Компонент w-Component.</span><span class="sxs-lookup"><span data-stu-id="be063-118">The w-component.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="be063-119">Комментарии</span><span class="sxs-lookup"><span data-stu-id="be063-119">Remarks</span></span>

<span data-ttu-id="be063-120">Кватернион добавляет четвертый элемент к \[ значениям x, y, z \] , определяющим вектор, что приводит к произвольным векторам 4d.</span><span class="sxs-lookup"><span data-stu-id="be063-120">Quaternions add a fourth element to the \[ x, y, z\] values that define a vector, resulting in arbitrary 4D vectors.</span></span> <span data-ttu-id="be063-121">Однако ниже показано, как каждый элемент единичного кватерниона связан с поворотом по оси (где q представляет единицу кватерниона (x, y, z, w), ось нормализована, а тета — желаемый поворот CCW по оси):</span><span class="sxs-lookup"><span data-stu-id="be063-121">However, the following illustrates how each element of a unit quaternion relates to an axis-angle rotation (where q represents a unit quaternion (x, y, z, w), axis is normalized, and theta is the desired CCW rotation about the axis):</span></span>


```
q.x = sin(theta/2) * axis.x
q.y = sin(theta/2) * axis.y
q.z = sin(theta/2) * axis.z
q.w = cos(theta/2)
```



<span data-ttu-id="be063-122">Программисты C++ могут воспользоваться преимуществами перегрузки операторов и приведения типов с помощью [**расширений D3DXQUATERNION**](d3dxquaternion-extensions.md), реализующих перегруженные конструкторы и операторы присваивания, унарные и бинарные (включая равенство).</span><span class="sxs-lookup"><span data-stu-id="be063-122">C++ programmers can take advantage of operator overloading and type casting with the [**D3DXQUATERNION Extensions**](d3dxquaternion-extensions.md), which implement overloaded constructors and assignment, unary, and binary (including equality) operators.</span></span>

## <a name="requirements"></a><span data-ttu-id="be063-123">Требования</span><span class="sxs-lookup"><span data-stu-id="be063-123">Requirements</span></span>



| <span data-ttu-id="be063-124">Требование</span><span class="sxs-lookup"><span data-stu-id="be063-124">Requirement</span></span> | <span data-ttu-id="be063-125">Значение</span><span class="sxs-lookup"><span data-stu-id="be063-125">Value</span></span> |
|-------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="be063-126">Header</span><span class="sxs-lookup"><span data-stu-id="be063-126">Header</span></span><br/> | <dl> <span data-ttu-id="be063-127"><dt>D3dx9math. h</dt></span><span class="sxs-lookup"><span data-stu-id="be063-127"><dt>D3dx9math.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="be063-128">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="be063-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="be063-129">Структуры D3DX</span><span class="sxs-lookup"><span data-stu-id="be063-129">D3DX Structures</span></span>](dx9-graphics-reference-d3dx-structures.md)
</dt> <dt>

[<span data-ttu-id="be063-130">Векторы, вершины и кватернион (Direct3D 9)</span><span class="sxs-lookup"><span data-stu-id="be063-130">Vectors, Vertices, and Quaternions (Direct3D 9)</span></span>](vectors--vertices--and-quaternions.md)
</dt> </dl>

 

 
