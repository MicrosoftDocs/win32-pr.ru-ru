---
description: Создает кватернион на основе матрицы вращения.
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
ms.openlocfilehash: 1caccf47e03388ffb85f2e12a5d0203f3fe839bd
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/15/2021
ms.locfileid: "104273916"
---
# <a name="d3dxquaternionrotationmatrix-function-d3dx10mathh"></a><span data-ttu-id="1eaab-103">Функция D3DXQuaternionRotationMatrix (D3DX10Math. h)</span><span class="sxs-lookup"><span data-stu-id="1eaab-103">D3DXQuaternionRotationMatrix function (D3DX10Math.h)</span></span>

<span data-ttu-id="1eaab-104">Создает кватернион на основе матрицы вращения.</span><span class="sxs-lookup"><span data-stu-id="1eaab-104">Builds a quaternion from a rotation matrix.</span></span>

## <a name="syntax"></a><span data-ttu-id="1eaab-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="1eaab-105">Syntax</span></span>


```C++
D3DXQUATERNION* D3DXQuaternionRotationMatrix(
  _Inout_       D3DXQUATERNION *pOut,
  _In_    const D3DXMATRIX     *pM
);
```



## <a name="parameters"></a><span data-ttu-id="1eaab-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="1eaab-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="1eaab-107">*тоска* \[ в, out\]</span><span class="sxs-lookup"><span data-stu-id="1eaab-107">*pOut* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="1eaab-108">Тип: **[ **D3DXQUATERNION**](../direct3d9/d3dxquaternion.md)\***</span><span class="sxs-lookup"><span data-stu-id="1eaab-108">Type: **[**D3DXQUATERNION**](../direct3d9/d3dxquaternion.md)\***</span></span>

<span data-ttu-id="1eaab-109">Указатель на [**D3DXQUATERNION**](d3d10-d3dxquaternion.md) , который является результатом операции.</span><span class="sxs-lookup"><span data-stu-id="1eaab-109">Pointer to the [**D3DXQUATERNION**](d3d10-d3dxquaternion.md) that is the result of the operation.</span></span>

</dd> <dt>

<span data-ttu-id="1eaab-110">*PM* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="1eaab-110">*pM* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="1eaab-111">Тип: **const [**D3DXMATRIX**](../direct3d9/d3dxmatrix.md) \***</span><span class="sxs-lookup"><span data-stu-id="1eaab-111">Type: **const [**D3DXMATRIX**](../direct3d9/d3dxmatrix.md)\***</span></span>

<span data-ttu-id="1eaab-112">Указатель на исходную структуру [**D3DXMATRIX**](d3d10-d3dxmatrix.md) .</span><span class="sxs-lookup"><span data-stu-id="1eaab-112">Pointer to the source [**D3DXMATRIX**](d3d10-d3dxmatrix.md) structure.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="1eaab-113">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="1eaab-113">Return value</span></span>

<span data-ttu-id="1eaab-114">Тип: **[ **D3DXQUATERNION**](../direct3d9/d3dxquaternion.md)\***</span><span class="sxs-lookup"><span data-stu-id="1eaab-114">Type: **[**D3DXQUATERNION**](../direct3d9/d3dxquaternion.md)\***</span></span>

<span data-ttu-id="1eaab-115">Указатель на структуру D3DXQUATERNION, построенную из матрицы вращения.</span><span class="sxs-lookup"><span data-stu-id="1eaab-115">Pointer to the D3DXQUATERNION structure built from a rotation matrix.</span></span>

## <a name="remarks"></a><span data-ttu-id="1eaab-116">Комментарии</span><span class="sxs-lookup"><span data-stu-id="1eaab-116">Remarks</span></span>

<span data-ttu-id="1eaab-117">Возвращаемое значение для этой функции совпадает со значением, возвращаемым в параметре тоска.</span><span class="sxs-lookup"><span data-stu-id="1eaab-117">The return value for this function is the same value returned in the pOut parameter.</span></span> <span data-ttu-id="1eaab-118">Таким образом, функция D3DXQuaternionRotationMatrix может использоваться в качестве параметра для другой функции.</span><span class="sxs-lookup"><span data-stu-id="1eaab-118">In this way, the D3DXQuaternionRotationMatrix function can be used as a parameter for another function.</span></span>

<span data-ttu-id="1eaab-119">Используйте [**D3DXQuaternionNormalize**](d3d10-d3dxquaternionnormalize.md) для любых входных данных кватернион, которые еще не нормализованы.</span><span class="sxs-lookup"><span data-stu-id="1eaab-119">Use [**D3DXQuaternionNormalize**](d3d10-d3dxquaternionnormalize.md) for any quaternion input that is not already normalized.</span></span>

## <a name="requirements"></a><span data-ttu-id="1eaab-120">Требования</span><span class="sxs-lookup"><span data-stu-id="1eaab-120">Requirements</span></span>



| <span data-ttu-id="1eaab-121">Требование</span><span class="sxs-lookup"><span data-stu-id="1eaab-121">Requirement</span></span> | <span data-ttu-id="1eaab-122">Значение</span><span class="sxs-lookup"><span data-stu-id="1eaab-122">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="1eaab-123">Header</span><span class="sxs-lookup"><span data-stu-id="1eaab-123">Header</span></span><br/>  | <dl> <span data-ttu-id="1eaab-124"><dt>D3DX10Math. h</dt></span><span class="sxs-lookup"><span data-stu-id="1eaab-124"><dt>D3DX10Math.h</dt></span></span> </dl> |
| <span data-ttu-id="1eaab-125">Библиотека</span><span class="sxs-lookup"><span data-stu-id="1eaab-125">Library</span></span><br/> | <dl> <span data-ttu-id="1eaab-126"><dt>D3DX10. lib</dt></span><span class="sxs-lookup"><span data-stu-id="1eaab-126"><dt>D3DX10.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="1eaab-127">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="1eaab-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="1eaab-128">Математические функции</span><span class="sxs-lookup"><span data-stu-id="1eaab-128">Math Functions</span></span>](d3d10-graphics-reference-d3dx10-functions-math.md)
</dt> </dl>

 

 
