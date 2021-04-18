---
description: Выполняет интерполяцию между двумя кватернионами, используя сферическую линейную интерполяцию.
ms.assetid: 94a989c8-fa6b-4852-9aa3-e55ad814ffd7
title: Функция D3DXQuaternionSlerp (D3dx9math. h)
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
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: f0f43e22ddc46007c6f589dfc5fd8b45aa885643
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/15/2021
ms.locfileid: "105713617"
---
# <a name="d3dxquaternionslerp-function-d3dx9mathh"></a><span data-ttu-id="a3853-103">Функция D3DXQuaternionSlerp (D3dx9math. h)</span><span class="sxs-lookup"><span data-stu-id="a3853-103">D3DXQuaternionSlerp function (D3dx9math.h)</span></span>

<span data-ttu-id="a3853-104">Выполняет интерполяцию между двумя кватернионами, используя сферическую линейную интерполяцию.</span><span class="sxs-lookup"><span data-stu-id="a3853-104">Interpolates between two quaternions, using spherical linear interpolation.</span></span>

## <a name="syntax"></a><span data-ttu-id="a3853-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="a3853-105">Syntax</span></span>


```C++
D3DXQUATERNION* D3DXQuaternionSlerp(
  _Inout_       D3DXQUATERNION *pOut,
  _In_    const D3DXQUATERNION *pQ1,
  _In_    const D3DXQUATERNION *pQ2,
  _In_          FLOAT          t
);
```



## <a name="parameters"></a><span data-ttu-id="a3853-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="a3853-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="a3853-107">*тоска* \[ в, out\]</span><span class="sxs-lookup"><span data-stu-id="a3853-107">*pOut* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="a3853-108">Тип: **[ **D3DXQUATERNION**](d3dxquaternion.md)\***</span><span class="sxs-lookup"><span data-stu-id="a3853-108">Type: **[**D3DXQUATERNION**](d3dxquaternion.md)\***</span></span>

<span data-ttu-id="a3853-109">Указатель на структуру [**D3DXQUATERNION**](d3dxquaternion.md) , которая является результатом операции.</span><span class="sxs-lookup"><span data-stu-id="a3853-109">Pointer to the [**D3DXQUATERNION**](d3dxquaternion.md) structure that is the result of the operation.</span></span>

</dd> <dt>

<span data-ttu-id="a3853-110">*pQ1* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="a3853-110">*pQ1* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="a3853-111">Тип: **const [**D3DXQUATERNION**](d3dxquaternion.md) \***</span><span class="sxs-lookup"><span data-stu-id="a3853-111">Type: **const [**D3DXQUATERNION**](d3dxquaternion.md)\***</span></span>

<span data-ttu-id="a3853-112">Указатель на исходную структуру [**D3DXQUATERNION**](d3dxquaternion.md) .</span><span class="sxs-lookup"><span data-stu-id="a3853-112">Pointer to a source [**D3DXQUATERNION**](d3dxquaternion.md) structure.</span></span>

</dd> <dt>

<span data-ttu-id="a3853-113">*pQ2* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="a3853-113">*pQ2* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="a3853-114">Тип: **const [**D3DXQUATERNION**](d3dxquaternion.md) \***</span><span class="sxs-lookup"><span data-stu-id="a3853-114">Type: **const [**D3DXQUATERNION**](d3dxquaternion.md)\***</span></span>

<span data-ttu-id="a3853-115">Указатель на исходную структуру [**D3DXQUATERNION**](d3dxquaternion.md) .</span><span class="sxs-lookup"><span data-stu-id="a3853-115">Pointer to a source [**D3DXQUATERNION**](d3dxquaternion.md) structure.</span></span>

</dd> <dt>

<span data-ttu-id="a3853-116">*t* \[ в\]</span><span class="sxs-lookup"><span data-stu-id="a3853-116">*t* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="a3853-117">Тип: **[ **float**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="a3853-117">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="a3853-118">Параметр, который указывает, насколько проинтерполируются между кватернионми.</span><span class="sxs-lookup"><span data-stu-id="a3853-118">Parameter that indicates how far to interpolate between the quaternions.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="a3853-119">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="a3853-119">Return value</span></span>

<span data-ttu-id="a3853-120">Тип: **[ **D3DXQUATERNION**](d3dxquaternion.md)\***</span><span class="sxs-lookup"><span data-stu-id="a3853-120">Type: **[**D3DXQUATERNION**](d3dxquaternion.md)\***</span></span>

<span data-ttu-id="a3853-121">Указатель на структуру [**D3DXQUATERNION**](d3dxquaternion.md) , которая является результатом интерполяции.</span><span class="sxs-lookup"><span data-stu-id="a3853-121">Pointer to a [**D3DXQUATERNION**](d3dxquaternion.md) structure that is the result of the interpolation.</span></span>

## <a name="remarks"></a><span data-ttu-id="a3853-122">Комментарии</span><span class="sxs-lookup"><span data-stu-id="a3853-122">Remarks</span></span>

<span data-ttu-id="a3853-123">Возвращаемое значение для этой функции совпадает со значением, возвращаемым в параметре *тоска* .</span><span class="sxs-lookup"><span data-stu-id="a3853-123">The return value for this function is the same value returned in the *pOut* parameter.</span></span> <span data-ttu-id="a3853-124">Таким образом, функция **D3DXQuaternionSlerp** может использоваться в качестве параметра для другой функции.</span><span class="sxs-lookup"><span data-stu-id="a3853-124">In this way, the **D3DXQuaternionSlerp** function can be used as a parameter for another function.</span></span>

<span data-ttu-id="a3853-125">Используйте [**D3DXQuaternionNormalize**](d3dxquaternionnormalize.md) для любых входных данных кватернион, которые еще не нормализованы.</span><span class="sxs-lookup"><span data-stu-id="a3853-125">Use [**D3DXQuaternionNormalize**](d3dxquaternionnormalize.md) for any quaternion input that is not already normalized.</span></span>

## <a name="requirements"></a><span data-ttu-id="a3853-126">Требования</span><span class="sxs-lookup"><span data-stu-id="a3853-126">Requirements</span></span>



| <span data-ttu-id="a3853-127">Требование</span><span class="sxs-lookup"><span data-stu-id="a3853-127">Requirement</span></span> | <span data-ttu-id="a3853-128">Значение</span><span class="sxs-lookup"><span data-stu-id="a3853-128">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="a3853-129">Header</span><span class="sxs-lookup"><span data-stu-id="a3853-129">Header</span></span><br/>  | <dl> <span data-ttu-id="a3853-130"><dt>D3dx9math. h</dt></span><span class="sxs-lookup"><span data-stu-id="a3853-130"><dt>D3dx9math.h</dt></span></span> </dl> |
| <span data-ttu-id="a3853-131">Библиотека</span><span class="sxs-lookup"><span data-stu-id="a3853-131">Library</span></span><br/> | <dl> <span data-ttu-id="a3853-132"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="a3853-132"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="a3853-133">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="a3853-133">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a3853-134">Математические функции</span><span class="sxs-lookup"><span data-stu-id="a3853-134">Math Functions</span></span>](dx9-graphics-reference-d3dx-functions-math.md)
</dt> </dl>

 

 
