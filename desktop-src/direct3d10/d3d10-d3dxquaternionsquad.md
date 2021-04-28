---
description: Функция D3DXQuaternionSquad (D3DX10Math. h) — выполняет интерполяцию между кватернионми, используя сферическую куадрангле интерполяцию.
ms.assetid: ba953731-4372-4b32-942b-23abfe479704
title: Функция D3DXQuaternionSquad (D3DX10Math. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXQuaternionSquad
api_type:
- LibDef
api_location:
- D3DX10.lib
- D3DX10.dll
ms.openlocfilehash: 9671b2a161124228c264da7eac0a2aa3a915ff95
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2021
ms.locfileid: "108108762"
---
# <a name="d3dxquaternionsquad-function-d3dx10mathh"></a><span data-ttu-id="d62f7-103">Функция D3DXQuaternionSquad (D3DX10Math. h)</span><span class="sxs-lookup"><span data-stu-id="d62f7-103">D3DXQuaternionSquad function (D3DX10Math.h)</span></span>

<span data-ttu-id="d62f7-104">Интерполяция между кватернионми с использованием сферической куадрангле интерполяции.</span><span class="sxs-lookup"><span data-stu-id="d62f7-104">Interpolates between quaternions, using spherical quadrangle interpolation.</span></span>

## <a name="syntax"></a><span data-ttu-id="d62f7-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="d62f7-105">Syntax</span></span>


```C++
D3DXQUATERNION* D3DXQuaternionSquad(
  _Inout_       D3DXQUATERNION *pOut,
  _In_    const D3DXQUATERNION *pQ1,
  _In_    const D3DXQUATERNION *pA,
  _In_    const D3DXQUATERNION *pB,
  _In_    const D3DXQUATERNION *pC,
  _In_          FLOAT          t
);
```



## <a name="parameters"></a><span data-ttu-id="d62f7-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="d62f7-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="d62f7-107">*тоска* \[ в, out\]</span><span class="sxs-lookup"><span data-stu-id="d62f7-107">*pOut* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="d62f7-108">Тип: **[ **D3DXQUATERNION**](../direct3d9/d3dxquaternion.md)\***</span><span class="sxs-lookup"><span data-stu-id="d62f7-108">Type: **[**D3DXQUATERNION**](../direct3d9/d3dxquaternion.md)\***</span></span>

<span data-ttu-id="d62f7-109">Указатель на [**D3DXQUATERNION**](d3d10-d3dxquaternion.md) , который является результатом операции.</span><span class="sxs-lookup"><span data-stu-id="d62f7-109">Pointer to the [**D3DXQUATERNION**](d3d10-d3dxquaternion.md) that is the result of the operation.</span></span>

</dd> <dt>

<span data-ttu-id="d62f7-110">*pQ1* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="d62f7-110">*pQ1* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="d62f7-111">Тип: **const [**D3DXQUATERNION**](../direct3d9/d3dxquaternion.md) \***</span><span class="sxs-lookup"><span data-stu-id="d62f7-111">Type: **const [**D3DXQUATERNION**](../direct3d9/d3dxquaternion.md)\***</span></span>

<span data-ttu-id="d62f7-112">Указатель на исходную структуру D3DXQUATERNION.</span><span class="sxs-lookup"><span data-stu-id="d62f7-112">Pointer to a source D3DXQUATERNION structure.</span></span>

</dd> <dt>

<span data-ttu-id="d62f7-113">*PA* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="d62f7-113">*pA* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="d62f7-114">Тип: **const [**D3DXQUATERNION**](../direct3d9/d3dxquaternion.md) \***</span><span class="sxs-lookup"><span data-stu-id="d62f7-114">Type: **const [**D3DXQUATERNION**](../direct3d9/d3dxquaternion.md)\***</span></span>

<span data-ttu-id="d62f7-115">Указатель на исходную структуру D3DXQUATERNION.</span><span class="sxs-lookup"><span data-stu-id="d62f7-115">Pointer to a source D3DXQUATERNION structure.</span></span>

</dd> <dt>

<span data-ttu-id="d62f7-116">*Pb* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="d62f7-116">*pB* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="d62f7-117">Тип: **const [**D3DXQUATERNION**](../direct3d9/d3dxquaternion.md) \***</span><span class="sxs-lookup"><span data-stu-id="d62f7-117">Type: **const [**D3DXQUATERNION**](../direct3d9/d3dxquaternion.md)\***</span></span>

<span data-ttu-id="d62f7-118">Указатель на исходную структуру D3DXQUATERNION.</span><span class="sxs-lookup"><span data-stu-id="d62f7-118">Pointer to a source D3DXQUATERNION structure.</span></span>

</dd> <dt>

<span data-ttu-id="d62f7-119">*ПК* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="d62f7-119">*pC* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="d62f7-120">Тип: **const [**D3DXQUATERNION**](../direct3d9/d3dxquaternion.md) \***</span><span class="sxs-lookup"><span data-stu-id="d62f7-120">Type: **const [**D3DXQUATERNION**](../direct3d9/d3dxquaternion.md)\***</span></span>

<span data-ttu-id="d62f7-121">Указатель на исходную структуру D3DXQUATERNION.</span><span class="sxs-lookup"><span data-stu-id="d62f7-121">Pointer to a source D3DXQUATERNION structure.</span></span>

</dd> <dt>

<span data-ttu-id="d62f7-122">*t* \[ в\]</span><span class="sxs-lookup"><span data-stu-id="d62f7-122">*t* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="d62f7-123">Тип: **[ **float**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="d62f7-123">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="d62f7-124">Параметр, который указывает, насколько проинтерполируются между кватернионми.</span><span class="sxs-lookup"><span data-stu-id="d62f7-124">Parameter that indicates how far to interpolate between the quaternions.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="d62f7-125">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="d62f7-125">Return value</span></span>

<span data-ttu-id="d62f7-126">Тип: **[ **D3DXQUATERNION**](../direct3d9/d3dxquaternion.md)\***</span><span class="sxs-lookup"><span data-stu-id="d62f7-126">Type: **[**D3DXQUATERNION**](../direct3d9/d3dxquaternion.md)\***</span></span>

<span data-ttu-id="d62f7-127">Указатель на структуру D3DXQUATERNION, которая является результатом сферической куадрангле интерполяции.</span><span class="sxs-lookup"><span data-stu-id="d62f7-127">Pointer to a D3DXQUATERNION structure that is the result of the spherical quadrangle interpolation.</span></span>

## <a name="remarks"></a><span data-ttu-id="d62f7-128">Remarks</span><span class="sxs-lookup"><span data-stu-id="d62f7-128">Remarks</span></span>

<span data-ttu-id="d62f7-129">Эта функция использует следующую последовательность сферческих операций интерполяции:</span><span class="sxs-lookup"><span data-stu-id="d62f7-129">This function uses the following sequence of spherical linear interpolation operations:</span></span>


```
Slerp(Slerp(pQ1, pC, t), Slerp(pA, pB, t), 2t(1 - t))
```



<span data-ttu-id="d62f7-130">Возвращаемое значение для этой функции совпадает со значением, возвращаемым в параметре тоска.</span><span class="sxs-lookup"><span data-stu-id="d62f7-130">The return value for this function is the same value returned in the pOut parameter.</span></span> <span data-ttu-id="d62f7-131">Таким образом, функция D3DXQuaternionSquad может использоваться в качестве параметра для другой функции.</span><span class="sxs-lookup"><span data-stu-id="d62f7-131">In this way, the D3DXQuaternionSquad function can be used as a parameter for another function.</span></span>

<span data-ttu-id="d62f7-132">Используйте [**D3DXQuaternionNormalize**](d3d10-d3dxquaternionnormalize.md) для любых входных данных кватернион, которые еще не нормализованы.</span><span class="sxs-lookup"><span data-stu-id="d62f7-132">Use [**D3DXQuaternionNormalize**](d3d10-d3dxquaternionnormalize.md) for any quaternion input that is not already normalized.</span></span>

## <a name="requirements"></a><span data-ttu-id="d62f7-133">Требования</span><span class="sxs-lookup"><span data-stu-id="d62f7-133">Requirements</span></span>



| <span data-ttu-id="d62f7-134">Требование</span><span class="sxs-lookup"><span data-stu-id="d62f7-134">Requirement</span></span> | <span data-ttu-id="d62f7-135">Значение</span><span class="sxs-lookup"><span data-stu-id="d62f7-135">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="d62f7-136">Header</span><span class="sxs-lookup"><span data-stu-id="d62f7-136">Header</span></span><br/>  | <dl> <span data-ttu-id="d62f7-137"><dt>D3DX10Math. h</dt></span><span class="sxs-lookup"><span data-stu-id="d62f7-137"><dt>D3DX10Math.h</dt></span></span> </dl> |
| <span data-ttu-id="d62f7-138">Библиотека</span><span class="sxs-lookup"><span data-stu-id="d62f7-138">Library</span></span><br/> | <dl> <span data-ttu-id="d62f7-139"><dt>D3DX10. lib</dt></span><span class="sxs-lookup"><span data-stu-id="d62f7-139"><dt>D3DX10.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="d62f7-140">См. также</span><span class="sxs-lookup"><span data-stu-id="d62f7-140">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d62f7-141">Математические функции</span><span class="sxs-lookup"><span data-stu-id="d62f7-141">Math Functions</span></span>](d3d10-graphics-reference-d3dx10-functions-math.md)
</dt> </dl>

 

 
