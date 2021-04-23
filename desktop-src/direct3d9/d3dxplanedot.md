---
description: Вычисление точки в плоскости и вектора 4D.
ms.assetid: e6232ca8-52cc-472d-8bdb-4f8dfc520d4f
title: Функция D3DXPlaneDot (D3dx9math. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXPlaneDot
api_type:
- LibDef
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: b6f33e591df364151a7090e5b4a9dd0773f5788a
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/15/2021
ms.locfileid: "105713464"
---
# <a name="d3dxplanedot-function"></a><span data-ttu-id="e6f09-103">Функция D3DXPlaneDot</span><span class="sxs-lookup"><span data-stu-id="e6f09-103">D3DXPlaneDot function</span></span>

<span data-ttu-id="e6f09-104">Вычисление точки в плоскости и вектора 4D.</span><span class="sxs-lookup"><span data-stu-id="e6f09-104">Computes the dot product of a plane and a 4D vector.</span></span>

## <a name="syntax"></a><span data-ttu-id="e6f09-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="e6f09-105">Syntax</span></span>


```C++
FLOAT D3DXPlaneDot(
  _In_ const D3DXPLANE   *pP,
  _In_ const D3DXVECTOR4 *pV
);
```



## <a name="parameters"></a><span data-ttu-id="e6f09-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="e6f09-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="e6f09-107">*PP* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="e6f09-107">*pP* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="e6f09-108">Тип: **const [**D3DXPLANE**](d3dxplane.md) \***</span><span class="sxs-lookup"><span data-stu-id="e6f09-108">Type: **const [**D3DXPLANE**](d3dxplane.md)\***</span></span>

<span data-ttu-id="e6f09-109">Указатель на исходную структуру [**D3DXPLANE**](d3dxplane.md) .</span><span class="sxs-lookup"><span data-stu-id="e6f09-109">Pointer to a source [**D3DXPLANE**](d3dxplane.md) structure.</span></span>

</dd> <dt>

<span data-ttu-id="e6f09-110">*ПС* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="e6f09-110">*pV* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="e6f09-111">Тип: **const [**D3DXVECTOR4**](d3dxvector4.md) \***</span><span class="sxs-lookup"><span data-stu-id="e6f09-111">Type: **const [**D3DXVECTOR4**](d3dxvector4.md)\***</span></span>

<span data-ttu-id="e6f09-112">Указатель на структуру [**D3DXVECTOR4**](d3dxvector4.md) .</span><span class="sxs-lookup"><span data-stu-id="e6f09-112">Pointer to a [**D3DXVECTOR4**](d3dxvector4.md) structure.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="e6f09-113">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="e6f09-113">Return value</span></span>

<span data-ttu-id="e6f09-114">Тип: **[ **float**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="e6f09-114">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="e6f09-115">Скалярное произведение плоскости и вектора 4D.</span><span class="sxs-lookup"><span data-stu-id="e6f09-115">The dot product of the plane and 4D vector.</span></span>

## <a name="remarks"></a><span data-ttu-id="e6f09-116">Комментарии</span><span class="sxs-lookup"><span data-stu-id="e6f09-116">Remarks</span></span>

<span data-ttu-id="e6f09-117">В плоскости (a, b, c, d) и 4D Vector (x, y, z, w) возвращаемое значение этой функции равно \* x + b \* y + c \* z + d \* w.</span><span class="sxs-lookup"><span data-stu-id="e6f09-117">Given a plane (a, b, c, d) and a 4D vector (x, y, z, w) the return value of this function is a\*x + b\*y + c\*z + d\*w.</span></span> <span data-ttu-id="e6f09-118">Функция **D3DXPlaneDot** полезна для определения связи плоскости с однородным координатами.</span><span class="sxs-lookup"><span data-stu-id="e6f09-118">The **D3DXPlaneDot** function is useful for determining the plane's relationship with a homogeneous coordinate.</span></span> <span data-ttu-id="e6f09-119">Например, эта функция может использоваться для определения того, находится ли определенная Координата на определенной плоскости или на какой стороне определенной плоскости лежит определенная координата.</span><span class="sxs-lookup"><span data-stu-id="e6f09-119">For example, this function could be used to determine if a particular coordinate is on a particular plane, or on which side of a particular plane a particular coordinate lies.</span></span>

## <a name="requirements"></a><span data-ttu-id="e6f09-120">Требования</span><span class="sxs-lookup"><span data-stu-id="e6f09-120">Requirements</span></span>



| <span data-ttu-id="e6f09-121">Требование</span><span class="sxs-lookup"><span data-stu-id="e6f09-121">Requirement</span></span> | <span data-ttu-id="e6f09-122">Значение</span><span class="sxs-lookup"><span data-stu-id="e6f09-122">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="e6f09-123">Header</span><span class="sxs-lookup"><span data-stu-id="e6f09-123">Header</span></span><br/>  | <dl> <span data-ttu-id="e6f09-124"><dt>D3dx9math. h</dt></span><span class="sxs-lookup"><span data-stu-id="e6f09-124"><dt>D3dx9math.h</dt></span></span> </dl> |
| <span data-ttu-id="e6f09-125">Библиотека</span><span class="sxs-lookup"><span data-stu-id="e6f09-125">Library</span></span><br/> | <dl> <span data-ttu-id="e6f09-126"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="e6f09-126"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="e6f09-127">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="e6f09-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e6f09-128">Математические функции</span><span class="sxs-lookup"><span data-stu-id="e6f09-128">Math Functions</span></span>](dx9-graphics-reference-d3dx-functions-math.md)
</dt> <dt>

[<span data-ttu-id="e6f09-129">**D3DXPlaneDotCoord**</span><span class="sxs-lookup"><span data-stu-id="e6f09-129">**D3DXPlaneDotCoord**</span></span>](d3dxplanedotcoord.md)
</dt> <dt>

[<span data-ttu-id="e6f09-130">**D3DXPlaneDotNormal**</span><span class="sxs-lookup"><span data-stu-id="e6f09-130">**D3DXPlaneDotNormal**</span></span>](d3dxplanedotnormal.md)
</dt> </dl>

 

 
