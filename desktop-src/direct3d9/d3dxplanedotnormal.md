---
description: Вычисление точки в плоскости и трехмерном векторе. Предполагается, что параметр w вектора имеет значение 0.
ms.assetid: 7aba1e94-6531-4c07-83b0-6100805e8bbd
title: Функция D3DXPlaneDotNormal (D3dx9math. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXPlaneDotNormal
api_type:
- LibDef
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 28903fc8ce0073e4014ae6ce75df636222ce32f0
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/15/2021
ms.locfileid: "105713459"
---
# <a name="d3dxplanedotnormal-function"></a><span data-ttu-id="987b7-104">Функция D3DXPlaneDotNormal</span><span class="sxs-lookup"><span data-stu-id="987b7-104">D3DXPlaneDotNormal function</span></span>

<span data-ttu-id="987b7-105">Вычисление точки в плоскости и трехмерном векторе.</span><span class="sxs-lookup"><span data-stu-id="987b7-105">Computes the dot product of a plane and a 3D vector.</span></span> <span data-ttu-id="987b7-106">Предполагается, что параметр w вектора имеет значение 0.</span><span class="sxs-lookup"><span data-stu-id="987b7-106">The w parameter of the vector is assumed to be 0.</span></span>

## <a name="syntax"></a><span data-ttu-id="987b7-107">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="987b7-107">Syntax</span></span>


```C++
FLOAT D3DXPlaneDotNormal(
  _In_ const D3DXPLANE   *pP,
  _In_ const D3DXVECTOR3 *pV
);
```



## <a name="parameters"></a><span data-ttu-id="987b7-108">Параметры</span><span class="sxs-lookup"><span data-stu-id="987b7-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="987b7-109">*PP* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="987b7-109">*pP* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="987b7-110">Тип: **const [**D3DXPLANE**](d3dxplane.md) \***</span><span class="sxs-lookup"><span data-stu-id="987b7-110">Type: **const [**D3DXPLANE**](d3dxplane.md)\***</span></span>

<span data-ttu-id="987b7-111">Указатель на исходную структуру [**D3DXPLANE**](d3dxplane.md) .</span><span class="sxs-lookup"><span data-stu-id="987b7-111">Pointer to a source [**D3DXPLANE**](d3dxplane.md) structure.</span></span>

</dd> <dt>

<span data-ttu-id="987b7-112">*ПС* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="987b7-112">*pV* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="987b7-113">Тип: **const [**D3DXVECTOR3**](d3dxvector3.md) \***</span><span class="sxs-lookup"><span data-stu-id="987b7-113">Type: **const [**D3DXVECTOR3**](d3dxvector3.md)\***</span></span>

<span data-ttu-id="987b7-114">Указатель на исходную структуру [**D3DXVECTOR3**](d3dxvector3.md) .</span><span class="sxs-lookup"><span data-stu-id="987b7-114">Pointer to a source [**D3DXVECTOR3**](d3dxvector3.md) structure.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="987b7-115">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="987b7-115">Return value</span></span>

<span data-ttu-id="987b7-116">Тип: **[ **float**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="987b7-116">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="987b7-117">Скалярное произведение плоскости и трехмерного вектора.</span><span class="sxs-lookup"><span data-stu-id="987b7-117">The dot product of the plane and 3D vector.</span></span>

## <a name="remarks"></a><span data-ttu-id="987b7-118">Комментарии</span><span class="sxs-lookup"><span data-stu-id="987b7-118">Remarks</span></span>

<span data-ttu-id="987b7-119">При наличии плоскости (a, b, c, d) и трехмерного вектора (x, y, z) возвращаемое значение этой функции является \* x + b \* y + c \* z + d \* 0.</span><span class="sxs-lookup"><span data-stu-id="987b7-119">Given a plane (a, b, c, d) and a 3D vector (x, y, z) the return value of this function is a\*x + b\*y + c\*z + d\*0.</span></span> <span data-ttu-id="987b7-120">Функция **D3DXPlaneDotNormal** полезна для вычисления угла нормали плоскости и другой нормальной.</span><span class="sxs-lookup"><span data-stu-id="987b7-120">The **D3DXPlaneDotNormal** function is useful for calculating the angle between the normal of the plane, and another normal.</span></span>

## <a name="requirements"></a><span data-ttu-id="987b7-121">Требования</span><span class="sxs-lookup"><span data-stu-id="987b7-121">Requirements</span></span>



| <span data-ttu-id="987b7-122">Требование</span><span class="sxs-lookup"><span data-stu-id="987b7-122">Requirement</span></span> | <span data-ttu-id="987b7-123">Значение</span><span class="sxs-lookup"><span data-stu-id="987b7-123">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="987b7-124">Header</span><span class="sxs-lookup"><span data-stu-id="987b7-124">Header</span></span><br/>  | <dl> <span data-ttu-id="987b7-125"><dt>D3dx9math. h</dt></span><span class="sxs-lookup"><span data-stu-id="987b7-125"><dt>D3dx9math.h</dt></span></span> </dl> |
| <span data-ttu-id="987b7-126">Библиотека</span><span class="sxs-lookup"><span data-stu-id="987b7-126">Library</span></span><br/> | <dl> <span data-ttu-id="987b7-127"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="987b7-127"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="987b7-128">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="987b7-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="987b7-129">Математические функции</span><span class="sxs-lookup"><span data-stu-id="987b7-129">Math Functions</span></span>](dx9-graphics-reference-d3dx-functions-math.md)
</dt> <dt>

[<span data-ttu-id="987b7-130">**D3DXPlaneDot**</span><span class="sxs-lookup"><span data-stu-id="987b7-130">**D3DXPlaneDot**</span></span>](d3dxplanedot.md)
</dt> <dt>

[<span data-ttu-id="987b7-131">**D3DXPlaneDotCoord**</span><span class="sxs-lookup"><span data-stu-id="987b7-131">**D3DXPlaneDotCoord**</span></span>](d3dxplanedotcoord.md)
</dt> </dl>

 

 
