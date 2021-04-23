---
description: Выполняет интерполяцию между двумя кватернионами, используя сферическую линейную интерполяцию.
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
ms.openlocfilehash: 07f673d33b8f105e808fbae380a06942e2a69be4
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/15/2021
ms.locfileid: "104081900"
---
# <a name="d3dxquaternionslerp-function-d3dx10mathh"></a><span data-ttu-id="e2c9a-103">Функция D3DXQuaternionSlerp (D3DX10Math. h)</span><span class="sxs-lookup"><span data-stu-id="e2c9a-103">D3DXQuaternionSlerp function (D3DX10Math.h)</span></span>

<span data-ttu-id="e2c9a-104">Выполняет интерполяцию между двумя кватернионами, используя сферическую линейную интерполяцию.</span><span class="sxs-lookup"><span data-stu-id="e2c9a-104">Interpolates between two quaternions, using spherical linear interpolation.</span></span>

## <a name="syntax"></a><span data-ttu-id="e2c9a-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="e2c9a-105">Syntax</span></span>


```C++
D3DXQUATERNION* D3DXQuaternionSlerp(
  _Inout_       D3DXQUATERNION *pOut,
  _In_    const D3DXQUATERNION *pQ1,
  _In_    const D3DXQUATERNION *pQ2,
  _In_          FLOAT          t
);
```



## <a name="parameters"></a><span data-ttu-id="e2c9a-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="e2c9a-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="e2c9a-107">*тоска* \[ в, out\]</span><span class="sxs-lookup"><span data-stu-id="e2c9a-107">*pOut* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="e2c9a-108">Тип: **[ **D3DXQUATERNION**](../direct3d9/d3dxquaternion.md)\***</span><span class="sxs-lookup"><span data-stu-id="e2c9a-108">Type: **[**D3DXQUATERNION**](../direct3d9/d3dxquaternion.md)\***</span></span>

<span data-ttu-id="e2c9a-109">Указатель на [**D3DXQUATERNION**](d3d10-d3dxquaternion.md) , который является результатом операции.</span><span class="sxs-lookup"><span data-stu-id="e2c9a-109">Pointer to the [**D3DXQUATERNION**](d3d10-d3dxquaternion.md) that is the result of the operation.</span></span>

</dd> <dt>

<span data-ttu-id="e2c9a-110">*pQ1* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="e2c9a-110">*pQ1* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="e2c9a-111">Тип: **const [**D3DXQUATERNION**](../direct3d9/d3dxquaternion.md) \***</span><span class="sxs-lookup"><span data-stu-id="e2c9a-111">Type: **const [**D3DXQUATERNION**](../direct3d9/d3dxquaternion.md)\***</span></span>

<span data-ttu-id="e2c9a-112">Указатель на исходную структуру D3DXQUATERNION.</span><span class="sxs-lookup"><span data-stu-id="e2c9a-112">Pointer to a source D3DXQUATERNION structure.</span></span>

</dd> <dt>

<span data-ttu-id="e2c9a-113">*pQ2* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="e2c9a-113">*pQ2* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="e2c9a-114">Тип: **const [**D3DXQUATERNION**](../direct3d9/d3dxquaternion.md) \***</span><span class="sxs-lookup"><span data-stu-id="e2c9a-114">Type: **const [**D3DXQUATERNION**](../direct3d9/d3dxquaternion.md)\***</span></span>

<span data-ttu-id="e2c9a-115">Указатель на исходную структуру D3DXQUATERNION.</span><span class="sxs-lookup"><span data-stu-id="e2c9a-115">Pointer to a source D3DXQUATERNION structure.</span></span>

</dd> <dt>

<span data-ttu-id="e2c9a-116">*t* \[ в\]</span><span class="sxs-lookup"><span data-stu-id="e2c9a-116">*t* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="e2c9a-117">Тип: **[ **float**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="e2c9a-117">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="e2c9a-118">Параметр, который указывает, насколько проинтерполируются между кватернионми.</span><span class="sxs-lookup"><span data-stu-id="e2c9a-118">Parameter that indicates how far to interpolate between the quaternions.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="e2c9a-119">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="e2c9a-119">Return value</span></span>

<span data-ttu-id="e2c9a-120">Тип: **[ **D3DXQUATERNION**](../direct3d9/d3dxquaternion.md)\***</span><span class="sxs-lookup"><span data-stu-id="e2c9a-120">Type: **[**D3DXQUATERNION**](../direct3d9/d3dxquaternion.md)\***</span></span>

<span data-ttu-id="e2c9a-121">Указатель на структуру D3DXQUATERNION, которая является результатом интерполяции.</span><span class="sxs-lookup"><span data-stu-id="e2c9a-121">Pointer to a D3DXQUATERNION structure that is the result of the interpolation.</span></span>

## <a name="remarks"></a><span data-ttu-id="e2c9a-122">Комментарии</span><span class="sxs-lookup"><span data-stu-id="e2c9a-122">Remarks</span></span>

<span data-ttu-id="e2c9a-123">Возвращаемое значение для этой функции совпадает со значением, возвращаемым в параметре тоска.</span><span class="sxs-lookup"><span data-stu-id="e2c9a-123">The return value for this function is the same value returned in the pOut parameter.</span></span> <span data-ttu-id="e2c9a-124">Таким образом, функция D3DXQuaternionSlerp может использоваться в качестве параметра для другой функции.</span><span class="sxs-lookup"><span data-stu-id="e2c9a-124">In this way, the D3DXQuaternionSlerp function can be used as a parameter for another function.</span></span>

<span data-ttu-id="e2c9a-125">Используйте [**D3DXQuaternionNormalize**](d3d10-d3dxquaternionnormalize.md) для любых входных данных кватернион, которые еще не нормализованы.</span><span class="sxs-lookup"><span data-stu-id="e2c9a-125">Use [**D3DXQuaternionNormalize**](d3d10-d3dxquaternionnormalize.md) for any quaternion input that is not already normalized.</span></span>

## <a name="requirements"></a><span data-ttu-id="e2c9a-126">Требования</span><span class="sxs-lookup"><span data-stu-id="e2c9a-126">Requirements</span></span>



| <span data-ttu-id="e2c9a-127">Требование</span><span class="sxs-lookup"><span data-stu-id="e2c9a-127">Requirement</span></span> | <span data-ttu-id="e2c9a-128">Значение</span><span class="sxs-lookup"><span data-stu-id="e2c9a-128">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="e2c9a-129">Header</span><span class="sxs-lookup"><span data-stu-id="e2c9a-129">Header</span></span><br/>  | <dl> <span data-ttu-id="e2c9a-130"><dt>D3DX10Math. h</dt></span><span class="sxs-lookup"><span data-stu-id="e2c9a-130"><dt>D3DX10Math.h</dt></span></span> </dl> |
| <span data-ttu-id="e2c9a-131">Библиотека</span><span class="sxs-lookup"><span data-stu-id="e2c9a-131">Library</span></span><br/> | <dl> <span data-ttu-id="e2c9a-132"><dt>D3DX10. lib</dt></span><span class="sxs-lookup"><span data-stu-id="e2c9a-132"><dt>D3DX10.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="e2c9a-133">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="e2c9a-133">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e2c9a-134">Математические функции</span><span class="sxs-lookup"><span data-stu-id="e2c9a-134">Math Functions</span></span>](d3d10-graphics-reference-d3dx10-functions-math.md)
</dt> </dl>

 

 
