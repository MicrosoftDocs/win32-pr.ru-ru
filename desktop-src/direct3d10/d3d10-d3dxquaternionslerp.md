---
description: Функция D3DXQuaternionSlerp (D3DX10Math. h) — выполняет интерполяцию между двумя кватернионами с использованием сферической линейной интерполяции.
ms.assetid: 487e1df1-bf20-49cb-ad14-61fcf1300904
title: Функция D3DXQuaternionSlerp (D3DX10Math. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXQuaternionSlerp
api_type:
- LibDef
api_location:
- D3DX10.lib
- D3DX10.dll
ms.openlocfilehash: 04cd3d82e4ca4e3f3357ab0114b57602f7e8a543
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2021
ms.locfileid: "108103122"
---
# <a name="d3dxquaternionslerp-function-d3dx10mathh"></a><span data-ttu-id="f2053-103">Функция D3DXQuaternionSlerp (D3DX10Math. h)</span><span class="sxs-lookup"><span data-stu-id="f2053-103">D3DXQuaternionSlerp function (D3DX10Math.h)</span></span>

<span data-ttu-id="f2053-104">Выполняет интерполяцию между двумя кватернионами, используя сферическую линейную интерполяцию.</span><span class="sxs-lookup"><span data-stu-id="f2053-104">Interpolates between two quaternions, using spherical linear interpolation.</span></span>

## <a name="syntax"></a><span data-ttu-id="f2053-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="f2053-105">Syntax</span></span>


```C++
D3DXQUATERNION* D3DXQuaternionSlerp(
  _Inout_       D3DXQUATERNION *pOut,
  _In_    const D3DXQUATERNION *pQ1,
  _In_    const D3DXQUATERNION *pQ2,
  _In_          FLOAT          t
);
```



## <a name="parameters"></a><span data-ttu-id="f2053-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="f2053-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="f2053-107">*тоска* \[ в, out\]</span><span class="sxs-lookup"><span data-stu-id="f2053-107">*pOut* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="f2053-108">Тип: **[ **D3DXQUATERNION**](../direct3d9/d3dxquaternion.md)\***</span><span class="sxs-lookup"><span data-stu-id="f2053-108">Type: **[**D3DXQUATERNION**](../direct3d9/d3dxquaternion.md)\***</span></span>

<span data-ttu-id="f2053-109">Указатель на [**D3DXQUATERNION**](d3d10-d3dxquaternion.md) , который является результатом операции.</span><span class="sxs-lookup"><span data-stu-id="f2053-109">Pointer to the [**D3DXQUATERNION**](d3d10-d3dxquaternion.md) that is the result of the operation.</span></span>

</dd> <dt>

<span data-ttu-id="f2053-110">*pQ1* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="f2053-110">*pQ1* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="f2053-111">Тип: **const [**D3DXQUATERNION**](../direct3d9/d3dxquaternion.md) \***</span><span class="sxs-lookup"><span data-stu-id="f2053-111">Type: **const [**D3DXQUATERNION**](../direct3d9/d3dxquaternion.md)\***</span></span>

<span data-ttu-id="f2053-112">Указатель на исходную структуру D3DXQUATERNION.</span><span class="sxs-lookup"><span data-stu-id="f2053-112">Pointer to a source D3DXQUATERNION structure.</span></span>

</dd> <dt>

<span data-ttu-id="f2053-113">*pQ2* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="f2053-113">*pQ2* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="f2053-114">Тип: **const [**D3DXQUATERNION**](../direct3d9/d3dxquaternion.md) \***</span><span class="sxs-lookup"><span data-stu-id="f2053-114">Type: **const [**D3DXQUATERNION**](../direct3d9/d3dxquaternion.md)\***</span></span>

<span data-ttu-id="f2053-115">Указатель на исходную структуру D3DXQUATERNION.</span><span class="sxs-lookup"><span data-stu-id="f2053-115">Pointer to a source D3DXQUATERNION structure.</span></span>

</dd> <dt>

<span data-ttu-id="f2053-116">*t* \[ в\]</span><span class="sxs-lookup"><span data-stu-id="f2053-116">*t* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="f2053-117">Тип: **[ **float**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="f2053-117">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="f2053-118">Параметр, который указывает, насколько проинтерполируются между кватернионми.</span><span class="sxs-lookup"><span data-stu-id="f2053-118">Parameter that indicates how far to interpolate between the quaternions.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="f2053-119">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="f2053-119">Return value</span></span>

<span data-ttu-id="f2053-120">Тип: **[ **D3DXQUATERNION**](../direct3d9/d3dxquaternion.md)\***</span><span class="sxs-lookup"><span data-stu-id="f2053-120">Type: **[**D3DXQUATERNION**](../direct3d9/d3dxquaternion.md)\***</span></span>

<span data-ttu-id="f2053-121">Указатель на структуру D3DXQUATERNION, которая является результатом интерполяции.</span><span class="sxs-lookup"><span data-stu-id="f2053-121">Pointer to a D3DXQUATERNION structure that is the result of the interpolation.</span></span>

## <a name="remarks"></a><span data-ttu-id="f2053-122">Remarks</span><span class="sxs-lookup"><span data-stu-id="f2053-122">Remarks</span></span>

<span data-ttu-id="f2053-123">Возвращаемое значение для этой функции совпадает со значением, возвращаемым в параметре тоска.</span><span class="sxs-lookup"><span data-stu-id="f2053-123">The return value for this function is the same value returned in the pOut parameter.</span></span> <span data-ttu-id="f2053-124">Таким образом, функция D3DXQuaternionSlerp может использоваться в качестве параметра для другой функции.</span><span class="sxs-lookup"><span data-stu-id="f2053-124">In this way, the D3DXQuaternionSlerp function can be used as a parameter for another function.</span></span>

<span data-ttu-id="f2053-125">Используйте [**D3DXQuaternionNormalize**](d3d10-d3dxquaternionnormalize.md) для любых входных данных кватернион, которые еще не нормализованы.</span><span class="sxs-lookup"><span data-stu-id="f2053-125">Use [**D3DXQuaternionNormalize**](d3d10-d3dxquaternionnormalize.md) for any quaternion input that is not already normalized.</span></span>

## <a name="requirements"></a><span data-ttu-id="f2053-126">Требования</span><span class="sxs-lookup"><span data-stu-id="f2053-126">Requirements</span></span>



| <span data-ttu-id="f2053-127">Требование</span><span class="sxs-lookup"><span data-stu-id="f2053-127">Requirement</span></span> | <span data-ttu-id="f2053-128">Значение</span><span class="sxs-lookup"><span data-stu-id="f2053-128">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="f2053-129">Header</span><span class="sxs-lookup"><span data-stu-id="f2053-129">Header</span></span><br/>  | <dl> <span data-ttu-id="f2053-130"><dt>D3DX10Math. h</dt></span><span class="sxs-lookup"><span data-stu-id="f2053-130"><dt>D3DX10Math.h</dt></span></span> </dl> |
| <span data-ttu-id="f2053-131">Библиотека</span><span class="sxs-lookup"><span data-stu-id="f2053-131">Library</span></span><br/> | <dl> <span data-ttu-id="f2053-132"><dt>D3DX10. lib</dt></span><span class="sxs-lookup"><span data-stu-id="f2053-132"><dt>D3DX10.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="f2053-133">См. также</span><span class="sxs-lookup"><span data-stu-id="f2053-133">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f2053-134">Математические функции</span><span class="sxs-lookup"><span data-stu-id="f2053-134">Math Functions</span></span>](d3d10-graphics-reference-d3dx10-functions-math.md)
</dt> </dl>

 

 
