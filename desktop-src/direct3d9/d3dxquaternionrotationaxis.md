---
description: Функция D3DXQuaternionRotationAxis (D3dx9math. h) — поворачивает кватернион по произвольной оси.
ms.assetid: 9ff0fe2c-54d6-482c-84e1-f38e3c57d8dd
title: Функция D3DXQuaternionRotationAxis (D3dx9math. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXQuaternionRotationAxis
api_type:
- LibDef
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: a5cbbdc3603b5e2eb7a03f592d44fa88f07ef015
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2021
ms.locfileid: "108118022"
---
# <a name="d3dxquaternionrotationaxis-function-d3dx9mathh"></a><span data-ttu-id="c4024-103">Функция D3DXQuaternionRotationAxis (D3dx9math. h)</span><span class="sxs-lookup"><span data-stu-id="c4024-103">D3DXQuaternionRotationAxis function (D3dx9math.h)</span></span>

<span data-ttu-id="c4024-104">Поворачивает кватернион по произвольной оси.</span><span class="sxs-lookup"><span data-stu-id="c4024-104">Rotates a quaternion about an arbitrary axis.</span></span>

## <a name="syntax"></a><span data-ttu-id="c4024-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="c4024-105">Syntax</span></span>


```C++
D3DXQUATERNION* D3DXQuaternionRotationAxis(
  _Inout_       D3DXQUATERNION *pOut,
  _In_    const D3DXVECTOR3    *pV,
  _In_          FLOAT          Angle
);
```



## <a name="parameters"></a><span data-ttu-id="c4024-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="c4024-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="c4024-107">*тоска* \[ в, out\]</span><span class="sxs-lookup"><span data-stu-id="c4024-107">*pOut* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="c4024-108">Тип: **[ **D3DXQUATERNION**](d3dxquaternion.md)\***</span><span class="sxs-lookup"><span data-stu-id="c4024-108">Type: **[**D3DXQUATERNION**](d3dxquaternion.md)\***</span></span>

<span data-ttu-id="c4024-109">Указатель на структуру [**D3DXQUATERNION**](d3dxquaternion.md) , которая является результатом операции.</span><span class="sxs-lookup"><span data-stu-id="c4024-109">Pointer to the [**D3DXQUATERNION**](d3dxquaternion.md) structure that is the result of the operation.</span></span>

</dd> <dt>

<span data-ttu-id="c4024-110">*ПС* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="c4024-110">*pV* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="c4024-111">Тип: **const [**D3DXVECTOR3**](d3dxvector3.md) \***</span><span class="sxs-lookup"><span data-stu-id="c4024-111">Type: **const [**D3DXVECTOR3**](d3dxvector3.md)\***</span></span>

<span data-ttu-id="c4024-112">Указатель на структуру [**D3DXVECTOR3**](d3dxvector3.md) , определяющую ось, для которой необходимо повернуть кватернион.</span><span class="sxs-lookup"><span data-stu-id="c4024-112">Pointer to the [**D3DXVECTOR3**](d3dxvector3.md) structure that identifies the axis about which to rotate the quaternion.</span></span>

</dd> <dt>

<span data-ttu-id="c4024-113">*Угол* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="c4024-113">*Angle* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="c4024-114">Тип: **[ **float**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="c4024-114">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="c4024-115">Угол поворота в радианах.</span><span class="sxs-lookup"><span data-stu-id="c4024-115">Angle of rotation, in radians.</span></span> <span data-ttu-id="c4024-116">Углы измеряются по часовой стрелке, если смотреть вдоль оси поворота в направлении начала координат.</span><span class="sxs-lookup"><span data-stu-id="c4024-116">Angles are measured clockwise when looking along the rotation axis toward the origin.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="c4024-117">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="c4024-117">Return value</span></span>

<span data-ttu-id="c4024-118">Тип: **[ **D3DXQUATERNION**](d3dxquaternion.md)\***</span><span class="sxs-lookup"><span data-stu-id="c4024-118">Type: **[**D3DXQUATERNION**](d3dxquaternion.md)\***</span></span>

<span data-ttu-id="c4024-119">Указатель на структуру [**D3DXQUATERNION**](d3dxquaternion.md) , повернутую вокруг указанной оси.</span><span class="sxs-lookup"><span data-stu-id="c4024-119">Pointer to a [**D3DXQUATERNION**](d3dxquaternion.md) structure rotated around the specified axis.</span></span>

## <a name="remarks"></a><span data-ttu-id="c4024-120">Remarks</span><span class="sxs-lookup"><span data-stu-id="c4024-120">Remarks</span></span>

<span data-ttu-id="c4024-121">Возвращаемое значение для этой функции совпадает со значением, возвращаемым в параметре *тоска* .</span><span class="sxs-lookup"><span data-stu-id="c4024-121">The return value for this function is the same value returned in the *pOut* parameter.</span></span> <span data-ttu-id="c4024-122">Таким образом, функция **D3DXQuaternionRotationAxis** может использоваться в качестве параметра для другой функции.</span><span class="sxs-lookup"><span data-stu-id="c4024-122">In this way, the **D3DXQuaternionRotationAxis** function can be used as a parameter for another function.</span></span>

<span data-ttu-id="c4024-123">Используйте [**D3DXQuaternionNormalize**](d3dxquaternionnormalize.md) для любых входных данных кватернион, которые еще не нормализованы.</span><span class="sxs-lookup"><span data-stu-id="c4024-123">Use [**D3DXQuaternionNormalize**](d3dxquaternionnormalize.md) for any quaternion input that is not already normalized.</span></span>

## <a name="requirements"></a><span data-ttu-id="c4024-124">Требования</span><span class="sxs-lookup"><span data-stu-id="c4024-124">Requirements</span></span>



| <span data-ttu-id="c4024-125">Требование</span><span class="sxs-lookup"><span data-stu-id="c4024-125">Requirement</span></span> | <span data-ttu-id="c4024-126">Значение</span><span class="sxs-lookup"><span data-stu-id="c4024-126">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="c4024-127">Header</span><span class="sxs-lookup"><span data-stu-id="c4024-127">Header</span></span><br/>  | <dl> <span data-ttu-id="c4024-128"><dt>D3dx9math. h</dt></span><span class="sxs-lookup"><span data-stu-id="c4024-128"><dt>D3dx9math.h</dt></span></span> </dl> |
| <span data-ttu-id="c4024-129">Библиотека</span><span class="sxs-lookup"><span data-stu-id="c4024-129">Library</span></span><br/> | <dl> <span data-ttu-id="c4024-130"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="c4024-130"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="c4024-131">См. также</span><span class="sxs-lookup"><span data-stu-id="c4024-131">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c4024-132">Математические функции</span><span class="sxs-lookup"><span data-stu-id="c4024-132">Math Functions</span></span>](dx9-graphics-reference-d3dx-functions-math.md)
</dt> <dt>

[<span data-ttu-id="c4024-133">**D3DXQuaternionRotationMatrix**</span><span class="sxs-lookup"><span data-stu-id="c4024-133">**D3DXQuaternionRotationMatrix**</span></span>](d3dxquaternionrotationmatrix.md)
</dt> <dt>

[<span data-ttu-id="c4024-134">**D3DXQuaternionRotationYawPitchRoll**</span><span class="sxs-lookup"><span data-stu-id="c4024-134">**D3DXQuaternionRotationYawPitchRoll**</span></span>](d3dxquaternionrotationyawpitchroll.md)
</dt> </dl>

 

 
