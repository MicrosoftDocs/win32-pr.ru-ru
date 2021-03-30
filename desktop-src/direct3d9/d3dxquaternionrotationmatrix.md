---
description: Создает кватернион на основе матрицы вращения.
ms.assetid: 4fafb1aa-5d6f-46e6-84b1-e0bac22952d2
title: Функция D3DXQuaternionRotationMatrix (D3dx9math. h)
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
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 0a9513c9aededdd06080db97aac78278986244b9
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/15/2021
ms.locfileid: "104354640"
---
# <a name="d3dxquaternionrotationmatrix-function-d3dx9mathh"></a><span data-ttu-id="32659-103">Функция D3DXQuaternionRotationMatrix (D3dx9math. h)</span><span class="sxs-lookup"><span data-stu-id="32659-103">D3DXQuaternionRotationMatrix function (D3dx9math.h)</span></span>

<span data-ttu-id="32659-104">Создает кватернион на основе матрицы вращения.</span><span class="sxs-lookup"><span data-stu-id="32659-104">Builds a quaternion from a rotation matrix.</span></span>

## <a name="syntax"></a><span data-ttu-id="32659-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="32659-105">Syntax</span></span>


```C++
D3DXQUATERNION* D3DXQuaternionRotationMatrix(
  _Inout_       D3DXQUATERNION *pOut,
  _In_    const D3DXMATRIX     *pM
);
```



## <a name="parameters"></a><span data-ttu-id="32659-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="32659-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="32659-107">*тоска* \[ в, out\]</span><span class="sxs-lookup"><span data-stu-id="32659-107">*pOut* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="32659-108">Тип: **[ **D3DXQUATERNION**](d3dxquaternion.md)\***</span><span class="sxs-lookup"><span data-stu-id="32659-108">Type: **[**D3DXQUATERNION**](d3dxquaternion.md)\***</span></span>

<span data-ttu-id="32659-109">Указатель на структуру [**D3DXQUATERNION**](d3dxquaternion.md) , которая является результатом операции.</span><span class="sxs-lookup"><span data-stu-id="32659-109">Pointer to the [**D3DXQUATERNION**](d3dxquaternion.md) structure that is the result of the operation.</span></span>

</dd> <dt>

<span data-ttu-id="32659-110">*PM* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="32659-110">*pM* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="32659-111">Тип: **const [**D3DXMATRIX**](d3dxmatrix.md) \***</span><span class="sxs-lookup"><span data-stu-id="32659-111">Type: **const [**D3DXMATRIX**](d3dxmatrix.md)\***</span></span>

<span data-ttu-id="32659-112">Указатель на исходную структуру [**D3DXMATRIX**](d3dxmatrix.md) .</span><span class="sxs-lookup"><span data-stu-id="32659-112">Pointer to the source [**D3DXMATRIX**](d3dxmatrix.md) structure.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="32659-113">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="32659-113">Return value</span></span>

<span data-ttu-id="32659-114">Тип: **[ **D3DXQUATERNION**](d3dxquaternion.md)\***</span><span class="sxs-lookup"><span data-stu-id="32659-114">Type: **[**D3DXQUATERNION**](d3dxquaternion.md)\***</span></span>

<span data-ttu-id="32659-115">Указатель на структуру [**D3DXQUATERNION**](d3dxquaternion.md) , построенную из матрицы вращения.</span><span class="sxs-lookup"><span data-stu-id="32659-115">Pointer to the [**D3DXQUATERNION**](d3dxquaternion.md) structure built from a rotation matrix.</span></span>

## <a name="remarks"></a><span data-ttu-id="32659-116">Комментарии</span><span class="sxs-lookup"><span data-stu-id="32659-116">Remarks</span></span>

<span data-ttu-id="32659-117">Возвращаемое значение для этой функции совпадает со значением, возвращаемым в параметре *тоска* .</span><span class="sxs-lookup"><span data-stu-id="32659-117">The return value for this function is the same value returned in the *pOut* parameter.</span></span> <span data-ttu-id="32659-118">Таким образом, функция **D3DXQuaternionRotationMatrix** может использоваться в качестве параметра для другой функции.</span><span class="sxs-lookup"><span data-stu-id="32659-118">In this way, the **D3DXQuaternionRotationMatrix** function can be used as a parameter for another function.</span></span>

<span data-ttu-id="32659-119">Используйте [**D3DXQuaternionNormalize**](d3dxquaternionnormalize.md) для любых входных данных кватернион, которые еще не нормализованы.</span><span class="sxs-lookup"><span data-stu-id="32659-119">Use [**D3DXQuaternionNormalize**](d3dxquaternionnormalize.md) for any quaternion input that is not already normalized.</span></span>

## <a name="requirements"></a><span data-ttu-id="32659-120">Требования</span><span class="sxs-lookup"><span data-stu-id="32659-120">Requirements</span></span>



| <span data-ttu-id="32659-121">Требование</span><span class="sxs-lookup"><span data-stu-id="32659-121">Requirement</span></span> | <span data-ttu-id="32659-122">Значение</span><span class="sxs-lookup"><span data-stu-id="32659-122">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="32659-123">Header</span><span class="sxs-lookup"><span data-stu-id="32659-123">Header</span></span><br/>  | <dl> <span data-ttu-id="32659-124"><dt>D3dx9math. h</dt></span><span class="sxs-lookup"><span data-stu-id="32659-124"><dt>D3dx9math.h</dt></span></span> </dl> |
| <span data-ttu-id="32659-125">Библиотека</span><span class="sxs-lookup"><span data-stu-id="32659-125">Library</span></span><br/> | <dl> <span data-ttu-id="32659-126"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="32659-126"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="32659-127">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="32659-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="32659-128">Математические функции</span><span class="sxs-lookup"><span data-stu-id="32659-128">Math Functions</span></span>](dx9-graphics-reference-d3dx-functions-math.md)
</dt> <dt>

[<span data-ttu-id="32659-129">**D3DXQuaternionRotationAxis**</span><span class="sxs-lookup"><span data-stu-id="32659-129">**D3DXQuaternionRotationAxis**</span></span>](d3dxquaternionrotationaxis.md)
</dt> <dt>

[<span data-ttu-id="32659-130">**D3DXQuaternionRotationYawPitchRoll**</span><span class="sxs-lookup"><span data-stu-id="32659-130">**D3DXQuaternionRotationYawPitchRoll**</span></span>](d3dxquaternionrotationyawpitchroll.md)
</dt> </dl>

 

 




