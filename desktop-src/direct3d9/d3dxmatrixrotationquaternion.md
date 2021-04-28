---
description: Функция D3DXMatrixRotationQuaternion (D3dx9math. h) — создает матрицу вращения из кватерниона.
ms.assetid: e590058c-772b-4eef-aab0-a12bb04c299a
title: Функция D3DXMatrixRotationQuaternion (D3dx9math. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXMatrixRotationQuaternion
api_type:
- LibDef
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 4b30de0c45c8d78b2e07d6ff57a4e94b9753298a
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2021
ms.locfileid: "108118202"
---
# <a name="d3dxmatrixrotationquaternion-function-d3dx9mathh"></a><span data-ttu-id="4fbf1-103">Функция D3DXMatrixRotationQuaternion (D3dx9math. h)</span><span class="sxs-lookup"><span data-stu-id="4fbf1-103">D3DXMatrixRotationQuaternion function (D3dx9math.h)</span></span>

<span data-ttu-id="4fbf1-104">Строит матрицу вращения из кватерниона.</span><span class="sxs-lookup"><span data-stu-id="4fbf1-104">Builds a rotation matrix from a quaternion.</span></span>

## <a name="syntax"></a><span data-ttu-id="4fbf1-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="4fbf1-105">Syntax</span></span>


```C++
D3DXMATRIX* D3DXMatrixRotationQuaternion(
  _Inout_       D3DXMATRIX     *pOut,
  _In_    const D3DXQUATERNION *pQ
);
```



## <a name="parameters"></a><span data-ttu-id="4fbf1-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="4fbf1-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="4fbf1-107">*тоска* \[ в, out\]</span><span class="sxs-lookup"><span data-stu-id="4fbf1-107">*pOut* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="4fbf1-108">Тип: **[ **D3DXMATRIX**](d3dxmatrix.md)\***</span><span class="sxs-lookup"><span data-stu-id="4fbf1-108">Type: **[**D3DXMATRIX**](d3dxmatrix.md)\***</span></span>

<span data-ttu-id="4fbf1-109">Указатель на структуру [**D3DXMATRIX**](d3dxmatrix.md) , которая является результатом операции.</span><span class="sxs-lookup"><span data-stu-id="4fbf1-109">Pointer to the [**D3DXMATRIX**](d3dxmatrix.md) structure that is the result of the operation.</span></span>

</dd> <dt>

<span data-ttu-id="4fbf1-110">*pQ* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="4fbf1-110">*pQ* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="4fbf1-111">Тип: **const [**D3DXQUATERNION**](d3dxquaternion.md) \***</span><span class="sxs-lookup"><span data-stu-id="4fbf1-111">Type: **const [**D3DXQUATERNION**](d3dxquaternion.md)\***</span></span>

<span data-ttu-id="4fbf1-112">Указатель на исходную структуру [**D3DXQUATERNION**](d3dxquaternion.md) .</span><span class="sxs-lookup"><span data-stu-id="4fbf1-112">Pointer to the source [**D3DXQUATERNION**](d3dxquaternion.md) structure.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="4fbf1-113">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="4fbf1-113">Return value</span></span>

<span data-ttu-id="4fbf1-114">Тип: **[ **D3DXMATRIX**](d3dxmatrix.md)\***</span><span class="sxs-lookup"><span data-stu-id="4fbf1-114">Type: **[**D3DXMATRIX**](d3dxmatrix.md)\***</span></span>

<span data-ttu-id="4fbf1-115">Указатель на структуру [**D3DXMATRIX**](d3dxmatrix.md) , построенную из исходного кватерниона.</span><span class="sxs-lookup"><span data-stu-id="4fbf1-115">Pointer to a [**D3DXMATRIX**](d3dxmatrix.md) structure built from the source quaternion.</span></span>

## <a name="remarks"></a><span data-ttu-id="4fbf1-116">Remarks</span><span class="sxs-lookup"><span data-stu-id="4fbf1-116">Remarks</span></span>

<span data-ttu-id="4fbf1-117">Возвращаемое значение для этой функции совпадает со значением, возвращаемым в параметре *тоска* .</span><span class="sxs-lookup"><span data-stu-id="4fbf1-117">The return value for this function is the same value returned in the *pOut* parameter.</span></span> <span data-ttu-id="4fbf1-118">Таким образом, функция **D3DXMatrixRotationQuaternion** может использоваться в качестве параметра для другой функции.</span><span class="sxs-lookup"><span data-stu-id="4fbf1-118">In this way, the **D3DXMatrixRotationQuaternion** function can be used as a parameter for another function.</span></span>

<span data-ttu-id="4fbf1-119">Сведения о вычислении значений кватерниона из вектора направления (x, y, z) и угла вращения см. в разделе [**D3DXQUATERNION**](d3dxquaternion.md).</span><span class="sxs-lookup"><span data-stu-id="4fbf1-119">For information about how to calculate quaternion values from a direction vector ( x, y, z ) and an angle of rotation, see [**D3DXQUATERNION**](d3dxquaternion.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="4fbf1-120">Требования</span><span class="sxs-lookup"><span data-stu-id="4fbf1-120">Requirements</span></span>



| <span data-ttu-id="4fbf1-121">Требование</span><span class="sxs-lookup"><span data-stu-id="4fbf1-121">Requirement</span></span> | <span data-ttu-id="4fbf1-122">Значение</span><span class="sxs-lookup"><span data-stu-id="4fbf1-122">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="4fbf1-123">Header</span><span class="sxs-lookup"><span data-stu-id="4fbf1-123">Header</span></span><br/>  | <dl> <span data-ttu-id="4fbf1-124"><dt>D3dx9math. h</dt></span><span class="sxs-lookup"><span data-stu-id="4fbf1-124"><dt>D3dx9math.h</dt></span></span> </dl> |
| <span data-ttu-id="4fbf1-125">Библиотека</span><span class="sxs-lookup"><span data-stu-id="4fbf1-125">Library</span></span><br/> | <dl> <span data-ttu-id="4fbf1-126"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="4fbf1-126"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="4fbf1-127">См. также</span><span class="sxs-lookup"><span data-stu-id="4fbf1-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="4fbf1-128">Математические функции</span><span class="sxs-lookup"><span data-stu-id="4fbf1-128">Math Functions</span></span>](dx9-graphics-reference-d3dx-functions-math.md)
</dt> <dt>

[<span data-ttu-id="4fbf1-129">**D3DXMatrixRotationAxis**</span><span class="sxs-lookup"><span data-stu-id="4fbf1-129">**D3DXMatrixRotationAxis**</span></span>](d3dxmatrixrotationaxis.md)
</dt> <dt>

[<span data-ttu-id="4fbf1-130">**D3DXMatrixRotationX**</span><span class="sxs-lookup"><span data-stu-id="4fbf1-130">**D3DXMatrixRotationX**</span></span>](d3dxmatrixrotationx.md)
</dt> <dt>

[<span data-ttu-id="4fbf1-131">**D3DXMatrixRotationY**</span><span class="sxs-lookup"><span data-stu-id="4fbf1-131">**D3DXMatrixRotationY**</span></span>](d3dxmatrixrotationy.md)
</dt> <dt>

[<span data-ttu-id="4fbf1-132">**D3DXMatrixRotationYawPitchRoll**</span><span class="sxs-lookup"><span data-stu-id="4fbf1-132">**D3DXMatrixRotationYawPitchRoll**</span></span>](d3dxmatrixrotationyawpitchroll.md)
</dt> <dt>

[<span data-ttu-id="4fbf1-133">**D3DXMatrixRotationZ**</span><span class="sxs-lookup"><span data-stu-id="4fbf1-133">**D3DXMatrixRotationZ**</span></span>](d3dxmatrixrotationz.md)
</dt> </dl>

 

 




