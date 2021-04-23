---
description: Строит матрицу вращения из кватерниона.
ms.assetid: dcbf8696-b959-4475-a250-6094dd5fe358
title: Функция D3DXMatrixRotationQuaternion (D3DX10Math. h)
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
- D3DX10.lib
- D3DX10.dll
ms.openlocfilehash: 44cd4a5982b322c2d207263fb490c898ed9fa76e
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/15/2021
ms.locfileid: "105720941"
---
# <a name="d3dxmatrixrotationquaternion-function-d3dx10mathh"></a><span data-ttu-id="facb9-103">Функция D3DXMatrixRotationQuaternion (D3DX10Math. h)</span><span class="sxs-lookup"><span data-stu-id="facb9-103">D3DXMatrixRotationQuaternion function (D3DX10Math.h)</span></span>

<span data-ttu-id="facb9-104">Строит матрицу вращения из кватерниона.</span><span class="sxs-lookup"><span data-stu-id="facb9-104">Builds a rotation matrix from a quaternion.</span></span>

## <a name="syntax"></a><span data-ttu-id="facb9-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="facb9-105">Syntax</span></span>


```C++
D3DXMATRIX* D3DXMatrixRotationQuaternion(
  _Inout_       D3DXMATRIX     *pOut,
  _In_    const D3DXQUATERNION *pQ
);
```



## <a name="parameters"></a><span data-ttu-id="facb9-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="facb9-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="facb9-107">*тоска* \[ в, out\]</span><span class="sxs-lookup"><span data-stu-id="facb9-107">*pOut* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="facb9-108">Тип: **[ **D3DXMATRIX**](../direct3d9/d3dxmatrix.md)\***</span><span class="sxs-lookup"><span data-stu-id="facb9-108">Type: **[**D3DXMATRIX**](../direct3d9/d3dxmatrix.md)\***</span></span>

<span data-ttu-id="facb9-109">Указатель на структуру [**D3DXMATRIX**](d3d10-d3dxmatrix.md) , которая является результатом операции.</span><span class="sxs-lookup"><span data-stu-id="facb9-109">Pointer to the [**D3DXMATRIX**](d3d10-d3dxmatrix.md) structure that is the result of the operation.</span></span>

</dd> <dt>

<span data-ttu-id="facb9-110">*pQ* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="facb9-110">*pQ* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="facb9-111">Тип: **const [**D3DXQUATERNION**](../direct3d9/d3dxquaternion.md) \***</span><span class="sxs-lookup"><span data-stu-id="facb9-111">Type: **const [**D3DXQUATERNION**](../direct3d9/d3dxquaternion.md)\***</span></span>

<span data-ttu-id="facb9-112">Указатель на исходную структуру D3DXQUATERNION.</span><span class="sxs-lookup"><span data-stu-id="facb9-112">Pointer to the source D3DXQUATERNION structure.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="facb9-113">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="facb9-113">Return value</span></span>

<span data-ttu-id="facb9-114">Тип: **[ **D3DXMATRIX**](../direct3d9/d3dxmatrix.md)\***</span><span class="sxs-lookup"><span data-stu-id="facb9-114">Type: **[**D3DXMATRIX**](../direct3d9/d3dxmatrix.md)\***</span></span>

<span data-ttu-id="facb9-115">Указатель на структуру D3DXMATRIX, построенную из исходного кватерниона.</span><span class="sxs-lookup"><span data-stu-id="facb9-115">Pointer to a D3DXMATRIX structure built from the source quaternion.</span></span>

## <a name="remarks"></a><span data-ttu-id="facb9-116">Комментарии</span><span class="sxs-lookup"><span data-stu-id="facb9-116">Remarks</span></span>

<span data-ttu-id="facb9-117">Возвращаемое значение для этой функции совпадает со значением, возвращаемым в параметре тоска.</span><span class="sxs-lookup"><span data-stu-id="facb9-117">The return value for this function is the same value returned in the pOut parameter.</span></span> <span data-ttu-id="facb9-118">Таким образом, функция D3DXMatrixRotationQuaternion может использоваться в качестве параметра для другой функции.</span><span class="sxs-lookup"><span data-stu-id="facb9-118">In this way, the D3DXMatrixRotationQuaternion function can be used as a parameter for another function.</span></span>

<span data-ttu-id="facb9-119">Сведения о вычислении значений кватерниона из вектора направления (x, y, z) и угла вращения см. в разделе [**D3DXQUATERNION**](d3d10-d3dxquaternion.md).</span><span class="sxs-lookup"><span data-stu-id="facb9-119">For information about how to calculate quaternion values from a direction vector ( x, y, z ) and an angle of rotation, see [**D3DXQUATERNION**](d3d10-d3dxquaternion.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="facb9-120">Требования</span><span class="sxs-lookup"><span data-stu-id="facb9-120">Requirements</span></span>



| <span data-ttu-id="facb9-121">Требование</span><span class="sxs-lookup"><span data-stu-id="facb9-121">Requirement</span></span> | <span data-ttu-id="facb9-122">Значение</span><span class="sxs-lookup"><span data-stu-id="facb9-122">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="facb9-123">Header</span><span class="sxs-lookup"><span data-stu-id="facb9-123">Header</span></span><br/>  | <dl> <span data-ttu-id="facb9-124"><dt>D3DX10Math. h</dt></span><span class="sxs-lookup"><span data-stu-id="facb9-124"><dt>D3DX10Math.h</dt></span></span> </dl> |
| <span data-ttu-id="facb9-125">Библиотека</span><span class="sxs-lookup"><span data-stu-id="facb9-125">Library</span></span><br/> | <dl> <span data-ttu-id="facb9-126"><dt>D3DX10. lib</dt></span><span class="sxs-lookup"><span data-stu-id="facb9-126"><dt>D3DX10.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="facb9-127">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="facb9-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="facb9-128">Математические функции</span><span class="sxs-lookup"><span data-stu-id="facb9-128">Math Functions</span></span>](d3d10-graphics-reference-d3dx10-functions-math.md)
</dt> </dl>

 

 
