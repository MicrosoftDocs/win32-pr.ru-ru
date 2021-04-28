---
description: Функция D3DXQuaternionRotationYawPitchRoll (D3DX10Math. h) — создает кватернион с заданными значения нутации, шагом и рулоном.
ms.assetid: c929d9d4-b9cb-4de6-86c1-26fec3617846
title: Функция D3DXQuaternionRotationYawPitchRoll (D3DX10Math. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXQuaternionRotationYawPitchRoll
api_type:
- LibDef
api_location:
- D3DX10.lib
- D3DX10.dll
ms.openlocfilehash: cefcf9a927cee0d8f7c83ff42ae6ca4fc699bb09
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2021
ms.locfileid: "108108752"
---
# <a name="d3dxquaternionrotationyawpitchroll-function-d3dx10mathh"></a><span data-ttu-id="e5940-103">Функция D3DXQuaternionRotationYawPitchRoll (D3DX10Math. h)</span><span class="sxs-lookup"><span data-stu-id="e5940-103">D3DXQuaternionRotationYawPitchRoll function (D3DX10Math.h)</span></span>

<span data-ttu-id="e5940-104">Создает кватернион с заданными значения нутации, шагом и рулоном.</span><span class="sxs-lookup"><span data-stu-id="e5940-104">Builds a quaternion with the given yaw, pitch, and roll.</span></span>

## <a name="syntax"></a><span data-ttu-id="e5940-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="e5940-105">Syntax</span></span>


```C++
D3DXQUATERNION* D3DXQuaternionRotationYawPitchRoll(
  _Inout_ D3DXQUATERNION *pOut,
  _In_    FLOAT          Yaw,
  _In_    FLOAT          Pitch,
  _In_    FLOAT          Roll
);
```



## <a name="parameters"></a><span data-ttu-id="e5940-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="e5940-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="e5940-107">*тоска* \[ в, out\]</span><span class="sxs-lookup"><span data-stu-id="e5940-107">*pOut* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="e5940-108">Тип: **[ **D3DXQUATERNION**](../direct3d9/d3dxquaternion.md)\***</span><span class="sxs-lookup"><span data-stu-id="e5940-108">Type: **[**D3DXQUATERNION**](../direct3d9/d3dxquaternion.md)\***</span></span>

<span data-ttu-id="e5940-109">Указатель на [**D3DXQUATERNION**](d3d10-d3dxquaternion.md) , который является результатом операции.</span><span class="sxs-lookup"><span data-stu-id="e5940-109">Pointer to the [**D3DXQUATERNION**](d3d10-d3dxquaternion.md) that is the result of the operation.</span></span>

</dd> <dt>

<span data-ttu-id="e5940-110">*Значения нутации* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="e5940-110">*Yaw* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="e5940-111">Тип: **[ **float**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="e5940-111">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="e5940-112">Значения нутации вокруг оси y (в радианах).</span><span class="sxs-lookup"><span data-stu-id="e5940-112">Yaw around the y-axis, in radians.</span></span>

</dd> <dt>

<span data-ttu-id="e5940-113">*Шаг* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="e5940-113">*Pitch* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="e5940-114">Тип: **[ **float**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="e5940-114">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="e5940-115">Шаг вокруг оси x в радианах.</span><span class="sxs-lookup"><span data-stu-id="e5940-115">Pitch around the x-axis, in radians.</span></span>

</dd> <dt>

<span data-ttu-id="e5940-116">*Рулон* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="e5940-116">*Roll* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="e5940-117">Тип: **[ **float**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="e5940-117">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="e5940-118">Поворот вокруг оси z в радианах.</span><span class="sxs-lookup"><span data-stu-id="e5940-118">Roll around the z-axis, in radians.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="e5940-119">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="e5940-119">Return value</span></span>

<span data-ttu-id="e5940-120">Тип: **[ **D3DXQUATERNION**](../direct3d9/d3dxquaternion.md)\***</span><span class="sxs-lookup"><span data-stu-id="e5940-120">Type: **[**D3DXQUATERNION**](../direct3d9/d3dxquaternion.md)\***</span></span>

<span data-ttu-id="e5940-121">Указатель на структуру D3DXQUATERNION с указанными значения нутации, шагом и рулоном.</span><span class="sxs-lookup"><span data-stu-id="e5940-121">Pointer to a D3DXQUATERNION structure with the specified yaw, pitch, and roll.</span></span>

## <a name="remarks"></a><span data-ttu-id="e5940-122">Remarks</span><span class="sxs-lookup"><span data-stu-id="e5940-122">Remarks</span></span>

<span data-ttu-id="e5940-123">Возвращаемое значение для этой функции совпадает со значением, возвращаемым в параметре тоска.</span><span class="sxs-lookup"><span data-stu-id="e5940-123">The return value for this function is the same value returned in the pOut parameter.</span></span> <span data-ttu-id="e5940-124">Таким образом, функция D3DXQuaternionRotationYawPitchRoll может использоваться в качестве параметра для другой функции.</span><span class="sxs-lookup"><span data-stu-id="e5940-124">In this way, the D3DXQuaternionRotationYawPitchRoll function can be used as a parameter for another function.</span></span>

<span data-ttu-id="e5940-125">Используйте [**D3DXQuaternionNormalize**](d3d10-d3dxquaternionnormalize.md) для любых входных данных кватернион, которые еще не нормализованы.</span><span class="sxs-lookup"><span data-stu-id="e5940-125">Use [**D3DXQuaternionNormalize**](d3d10-d3dxquaternionnormalize.md) for any quaternion input that is not already normalized.</span></span>

## <a name="requirements"></a><span data-ttu-id="e5940-126">Требования</span><span class="sxs-lookup"><span data-stu-id="e5940-126">Requirements</span></span>



| <span data-ttu-id="e5940-127">Требование</span><span class="sxs-lookup"><span data-stu-id="e5940-127">Requirement</span></span> | <span data-ttu-id="e5940-128">Значение</span><span class="sxs-lookup"><span data-stu-id="e5940-128">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="e5940-129">Header</span><span class="sxs-lookup"><span data-stu-id="e5940-129">Header</span></span><br/>  | <dl> <span data-ttu-id="e5940-130"><dt>D3DX10Math. h</dt></span><span class="sxs-lookup"><span data-stu-id="e5940-130"><dt>D3DX10Math.h</dt></span></span> </dl> |
| <span data-ttu-id="e5940-131">Библиотека</span><span class="sxs-lookup"><span data-stu-id="e5940-131">Library</span></span><br/> | <dl> <span data-ttu-id="e5940-132"><dt>D3DX10. lib</dt></span><span class="sxs-lookup"><span data-stu-id="e5940-132"><dt>D3DX10.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="e5940-133">См. также</span><span class="sxs-lookup"><span data-stu-id="e5940-133">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e5940-134">Математические функции</span><span class="sxs-lookup"><span data-stu-id="e5940-134">Math Functions</span></span>](d3d10-graphics-reference-d3dx10-functions-math.md)
</dt> </dl>

 

 
