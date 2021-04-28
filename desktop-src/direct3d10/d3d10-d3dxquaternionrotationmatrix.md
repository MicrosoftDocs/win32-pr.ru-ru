---
description: Функция D3DXQuaternionRotationMatrix (D3DX10Math. h) — создает кватернион на основе матрицы вращения.
ms.assetid: 316bf3e0-32ff-4e5e-b771-99f7eea2e27c
title: Функция D3DXQuaternionRotationMatrix (D3DX10Math. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXQuaternionRotationMatrix
api_type:
- LibDef
api_location:
- D3DX10.lib
- D3DX10.dll
ms.openlocfilehash: cb923c135d436b36fe032d344366fdee687d27a0
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2021
ms.locfileid: "108103152"
---
# <a name="d3dxquaternionrotationmatrix-function-d3dx10mathh"></a><span data-ttu-id="fa600-103">Функция D3DXQuaternionRotationMatrix (D3DX10Math. h)</span><span class="sxs-lookup"><span data-stu-id="fa600-103">D3DXQuaternionRotationMatrix function (D3DX10Math.h)</span></span>

<span data-ttu-id="fa600-104">Создает кватернион на основе матрицы вращения.</span><span class="sxs-lookup"><span data-stu-id="fa600-104">Builds a quaternion from a rotation matrix.</span></span>

## <a name="syntax"></a><span data-ttu-id="fa600-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="fa600-105">Syntax</span></span>


```C++
D3DXQUATERNION* D3DXQuaternionRotationMatrix(
  _Inout_       D3DXQUATERNION *pOut,
  _In_    const D3DXMATRIX     *pM
);
```



## <a name="parameters"></a><span data-ttu-id="fa600-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="fa600-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="fa600-107">*тоска* \[ в, out\]</span><span class="sxs-lookup"><span data-stu-id="fa600-107">*pOut* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="fa600-108">Тип: **[ **D3DXQUATERNION**](../direct3d9/d3dxquaternion.md)\***</span><span class="sxs-lookup"><span data-stu-id="fa600-108">Type: **[**D3DXQUATERNION**](../direct3d9/d3dxquaternion.md)\***</span></span>

<span data-ttu-id="fa600-109">Указатель на [**D3DXQUATERNION**](d3d10-d3dxquaternion.md) , который является результатом операции.</span><span class="sxs-lookup"><span data-stu-id="fa600-109">Pointer to the [**D3DXQUATERNION**](d3d10-d3dxquaternion.md) that is the result of the operation.</span></span>

</dd> <dt>

<span data-ttu-id="fa600-110">*PM* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="fa600-110">*pM* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="fa600-111">Тип: **const [**D3DXMATRIX**](../direct3d9/d3dxmatrix.md) \***</span><span class="sxs-lookup"><span data-stu-id="fa600-111">Type: **const [**D3DXMATRIX**](../direct3d9/d3dxmatrix.md)\***</span></span>

<span data-ttu-id="fa600-112">Указатель на исходную структуру [**D3DXMATRIX**](d3d10-d3dxmatrix.md) .</span><span class="sxs-lookup"><span data-stu-id="fa600-112">Pointer to the source [**D3DXMATRIX**](d3d10-d3dxmatrix.md) structure.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="fa600-113">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="fa600-113">Return value</span></span>

<span data-ttu-id="fa600-114">Тип: **[ **D3DXQUATERNION**](../direct3d9/d3dxquaternion.md)\***</span><span class="sxs-lookup"><span data-stu-id="fa600-114">Type: **[**D3DXQUATERNION**](../direct3d9/d3dxquaternion.md)\***</span></span>

<span data-ttu-id="fa600-115">Указатель на структуру D3DXQUATERNION, построенную из матрицы вращения.</span><span class="sxs-lookup"><span data-stu-id="fa600-115">Pointer to the D3DXQUATERNION structure built from a rotation matrix.</span></span>

## <a name="remarks"></a><span data-ttu-id="fa600-116">Remarks</span><span class="sxs-lookup"><span data-stu-id="fa600-116">Remarks</span></span>

<span data-ttu-id="fa600-117">Возвращаемое значение для этой функции совпадает со значением, возвращаемым в параметре тоска.</span><span class="sxs-lookup"><span data-stu-id="fa600-117">The return value for this function is the same value returned in the pOut parameter.</span></span> <span data-ttu-id="fa600-118">Таким образом, функция D3DXQuaternionRotationMatrix может использоваться в качестве параметра для другой функции.</span><span class="sxs-lookup"><span data-stu-id="fa600-118">In this way, the D3DXQuaternionRotationMatrix function can be used as a parameter for another function.</span></span>

<span data-ttu-id="fa600-119">Используйте [**D3DXQuaternionNormalize**](d3d10-d3dxquaternionnormalize.md) для любых входных данных кватернион, которые еще не нормализованы.</span><span class="sxs-lookup"><span data-stu-id="fa600-119">Use [**D3DXQuaternionNormalize**](d3d10-d3dxquaternionnormalize.md) for any quaternion input that is not already normalized.</span></span>

## <a name="requirements"></a><span data-ttu-id="fa600-120">Требования</span><span class="sxs-lookup"><span data-stu-id="fa600-120">Requirements</span></span>



| <span data-ttu-id="fa600-121">Требование</span><span class="sxs-lookup"><span data-stu-id="fa600-121">Requirement</span></span> | <span data-ttu-id="fa600-122">Значение</span><span class="sxs-lookup"><span data-stu-id="fa600-122">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="fa600-123">Header</span><span class="sxs-lookup"><span data-stu-id="fa600-123">Header</span></span><br/>  | <dl> <span data-ttu-id="fa600-124"><dt>D3DX10Math. h</dt></span><span class="sxs-lookup"><span data-stu-id="fa600-124"><dt>D3DX10Math.h</dt></span></span> </dl> |
| <span data-ttu-id="fa600-125">Библиотека</span><span class="sxs-lookup"><span data-stu-id="fa600-125">Library</span></span><br/> | <dl> <span data-ttu-id="fa600-126"><dt>D3DX10. lib</dt></span><span class="sxs-lookup"><span data-stu-id="fa600-126"><dt>D3DX10.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="fa600-127">См. также</span><span class="sxs-lookup"><span data-stu-id="fa600-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="fa600-128">Математические функции</span><span class="sxs-lookup"><span data-stu-id="fa600-128">Math Functions</span></span>](d3d10-graphics-reference-d3dx10-functions-math.md)
</dt> </dl>

 

 
