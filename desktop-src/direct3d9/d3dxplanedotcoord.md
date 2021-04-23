---
description: Вычисление точки в плоскости и трехмерном векторе. Параметр w вектора предполагается равным 1.
ms.assetid: 634de6bc-b631-493d-a7a6-292a3c3253d6
title: Функция D3DXPlaneDotCoord (D3dx9math. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXPlaneDotCoord
api_type:
- LibDef
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 99ee9db7df541dcf74867b828a73ede80f11e22b
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/15/2021
ms.locfileid: "104273698"
---
# <a name="d3dxplanedotcoord-function"></a><span data-ttu-id="7ea07-104">Функция D3DXPlaneDotCoord</span><span class="sxs-lookup"><span data-stu-id="7ea07-104">D3DXPlaneDotCoord function</span></span>

<span data-ttu-id="7ea07-105">Вычисление точки в плоскости и трехмерном векторе.</span><span class="sxs-lookup"><span data-stu-id="7ea07-105">Computes the dot product of a plane and a 3D vector.</span></span> <span data-ttu-id="7ea07-106">Параметр w вектора предполагается равным 1.</span><span class="sxs-lookup"><span data-stu-id="7ea07-106">The w parameter of the vector is assumed to be 1.</span></span>

## <a name="syntax"></a><span data-ttu-id="7ea07-107">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="7ea07-107">Syntax</span></span>


```C++
FLOAT D3DXPlaneDotCoord(
  _In_ const D3DXPLANE   *pP,
  _In_ const D3DXVECTOR3 *pV
);
```



## <a name="parameters"></a><span data-ttu-id="7ea07-108">Параметры</span><span class="sxs-lookup"><span data-stu-id="7ea07-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="7ea07-109">*PP* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="7ea07-109">*pP* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="7ea07-110">Тип: **const [**D3DXPLANE**](d3dxplane.md) \***</span><span class="sxs-lookup"><span data-stu-id="7ea07-110">Type: **const [**D3DXPLANE**](d3dxplane.md)\***</span></span>

<span data-ttu-id="7ea07-111">Указатель на исходную структуру [**D3DXPLANE**](d3dxplane.md) .</span><span class="sxs-lookup"><span data-stu-id="7ea07-111">Pointer to a source [**D3DXPLANE**](d3dxplane.md) structure.</span></span>

</dd> <dt>

<span data-ttu-id="7ea07-112">*ПС* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="7ea07-112">*pV* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="7ea07-113">Тип: **const [**D3DXVECTOR3**](d3dxvector3.md) \***</span><span class="sxs-lookup"><span data-stu-id="7ea07-113">Type: **const [**D3DXVECTOR3**](d3dxvector3.md)\***</span></span>

<span data-ttu-id="7ea07-114">Указатель на исходную структуру [**D3DXVECTOR3**](d3dxvector3.md) .</span><span class="sxs-lookup"><span data-stu-id="7ea07-114">Pointer to a source [**D3DXVECTOR3**](d3dxvector3.md) structure.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="7ea07-115">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="7ea07-115">Return value</span></span>

<span data-ttu-id="7ea07-116">Тип: **[ **float**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="7ea07-116">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="7ea07-117">Скалярное произведение плоскости и трехмерного вектора.</span><span class="sxs-lookup"><span data-stu-id="7ea07-117">The dot product of the plane and 3D vector.</span></span>

## <a name="remarks"></a><span data-ttu-id="7ea07-118">Комментарии</span><span class="sxs-lookup"><span data-stu-id="7ea07-118">Remarks</span></span>

<span data-ttu-id="7ea07-119">При наличии плоскости (a, b, c, d) и трехмерного вектора (x, y, z) возвращаемое значение этой функции является \* x + b \* y + c \* z + d \* 1.</span><span class="sxs-lookup"><span data-stu-id="7ea07-119">Given a plane (a, b, c, d) and a 3D vector (x, y, z) the return value of this function is a\*x + b\*y + c\*z + d\*1.</span></span> <span data-ttu-id="7ea07-120">Функция **D3DXPlaneDotCoord** полезна для определения связи плоскости с координатами в трехмерном пространстве.</span><span class="sxs-lookup"><span data-stu-id="7ea07-120">The **D3DXPlaneDotCoord** function is useful for determining the plane's relationship with a coordinate in 3D space.</span></span>

## <a name="requirements"></a><span data-ttu-id="7ea07-121">Требования</span><span class="sxs-lookup"><span data-stu-id="7ea07-121">Requirements</span></span>



| <span data-ttu-id="7ea07-122">Требование</span><span class="sxs-lookup"><span data-stu-id="7ea07-122">Requirement</span></span> | <span data-ttu-id="7ea07-123">Значение</span><span class="sxs-lookup"><span data-stu-id="7ea07-123">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="7ea07-124">Header</span><span class="sxs-lookup"><span data-stu-id="7ea07-124">Header</span></span><br/>  | <dl> <span data-ttu-id="7ea07-125"><dt>D3dx9math. h</dt></span><span class="sxs-lookup"><span data-stu-id="7ea07-125"><dt>D3dx9math.h</dt></span></span> </dl> |
| <span data-ttu-id="7ea07-126">Библиотека</span><span class="sxs-lookup"><span data-stu-id="7ea07-126">Library</span></span><br/> | <dl> <span data-ttu-id="7ea07-127"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="7ea07-127"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="7ea07-128">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="7ea07-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="7ea07-129">Математические функции</span><span class="sxs-lookup"><span data-stu-id="7ea07-129">Math Functions</span></span>](dx9-graphics-reference-d3dx-functions-math.md)
</dt> <dt>

[<span data-ttu-id="7ea07-130">**D3DXPlaneDot**</span><span class="sxs-lookup"><span data-stu-id="7ea07-130">**D3DXPlaneDot**</span></span>](d3dxplanedot.md)
</dt> <dt>

[<span data-ttu-id="7ea07-131">**D3DXPlaneDotNormal**</span><span class="sxs-lookup"><span data-stu-id="7ea07-131">**D3DXPlaneDotNormal**</span></span>](d3dxplanedotnormal.md)
</dt> </dl>

 

 
