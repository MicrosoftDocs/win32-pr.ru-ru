---
description: Функция D3DXQuaternionRotationAxis (D3DX10Math. h) — поворачивает кватернион по произвольной оси.
ms.assetid: 9673ef89-458f-4a25-960e-8f03179e78ba
title: Функция D3DXQuaternionRotationAxis (D3DX10Math. h)
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
- D3DX10.lib
- D3DX10.dll
ms.openlocfilehash: 509df80023427a20125e1b5603e85424851a640e
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2021
ms.locfileid: "108108772"
---
# <a name="d3dxquaternionrotationaxis-function-d3dx10mathh"></a><span data-ttu-id="87b76-103">Функция D3DXQuaternionRotationAxis (D3DX10Math. h)</span><span class="sxs-lookup"><span data-stu-id="87b76-103">D3DXQuaternionRotationAxis function (D3DX10Math.h)</span></span>

<span data-ttu-id="87b76-104">Поворачивает кватернион по произвольной оси.</span><span class="sxs-lookup"><span data-stu-id="87b76-104">Rotates a quaternion about an arbitrary axis.</span></span>

## <a name="syntax"></a><span data-ttu-id="87b76-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="87b76-105">Syntax</span></span>


```C++
D3DXQUATERNION* D3DXQuaternionRotationAxis(
  _Inout_       D3DXQUATERNION *pOut,
  _In_    const D3DXVECTOR3    *pV,
  _In_          FLOAT          Angle
);
```



## <a name="parameters"></a><span data-ttu-id="87b76-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="87b76-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="87b76-107">*тоска* \[ в, out\]</span><span class="sxs-lookup"><span data-stu-id="87b76-107">*pOut* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="87b76-108">Тип: **[ **D3DXQUATERNION**](../direct3d9/d3dxquaternion.md)\***</span><span class="sxs-lookup"><span data-stu-id="87b76-108">Type: **[**D3DXQUATERNION**](../direct3d9/d3dxquaternion.md)\***</span></span>

<span data-ttu-id="87b76-109">Указатель на [**D3DXQUATERNION**](d3d10-d3dxquaternion.md) , который является результатом операции.</span><span class="sxs-lookup"><span data-stu-id="87b76-109">Pointer to the [**D3DXQUATERNION**](d3d10-d3dxquaternion.md) that is the result of the operation.</span></span>

</dd> <dt>

<span data-ttu-id="87b76-110">*ПС* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="87b76-110">*pV* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="87b76-111">Тип: **const [**D3DXVECTOR3**](../direct3d9/d3dxvector3.md) \***</span><span class="sxs-lookup"><span data-stu-id="87b76-111">Type: **const [**D3DXVECTOR3**](../direct3d9/d3dxvector3.md)\***</span></span>

<span data-ttu-id="87b76-112">Указатель на [**D3DXVECTOR3**](d3d10-d3dxvector3.md) , определяющий ось, для которой необходимо повернуть кватернион.</span><span class="sxs-lookup"><span data-stu-id="87b76-112">Pointer to the [**D3DXVECTOR3**](d3d10-d3dxvector3.md) that identifies the axis about which to rotate the quaternion.</span></span>

</dd> <dt>

<span data-ttu-id="87b76-113">*Угол* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="87b76-113">*Angle* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="87b76-114">Тип: **[ **float**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="87b76-114">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="87b76-115">Угол поворота в радианах.</span><span class="sxs-lookup"><span data-stu-id="87b76-115">Angle of rotation, in radians.</span></span> <span data-ttu-id="87b76-116">Углы измеряются по часовой стрелке, если смотреть вдоль оси поворота в направлении начала координат.</span><span class="sxs-lookup"><span data-stu-id="87b76-116">Angles are measured clockwise when looking along the rotation axis toward the origin.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="87b76-117">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="87b76-117">Return value</span></span>

<span data-ttu-id="87b76-118">Тип: **[ **D3DXQUATERNION**](../direct3d9/d3dxquaternion.md)\***</span><span class="sxs-lookup"><span data-stu-id="87b76-118">Type: **[**D3DXQUATERNION**](../direct3d9/d3dxquaternion.md)\***</span></span>

<span data-ttu-id="87b76-119">Указатель на структуру D3DXQUATERNION, повернутую вокруг указанной оси.</span><span class="sxs-lookup"><span data-stu-id="87b76-119">Pointer to a D3DXQUATERNION structure rotated around the specified axis.</span></span>

## <a name="remarks"></a><span data-ttu-id="87b76-120">Remarks</span><span class="sxs-lookup"><span data-stu-id="87b76-120">Remarks</span></span>

<span data-ttu-id="87b76-121">Возвращаемое значение для этой функции совпадает со значением, возвращаемым в параметре тоска.</span><span class="sxs-lookup"><span data-stu-id="87b76-121">The return value for this function is the same value returned in the pOut parameter.</span></span> <span data-ttu-id="87b76-122">Таким образом, функция D3DXQuaternionRotationAxis может использоваться в качестве параметра для другой функции.</span><span class="sxs-lookup"><span data-stu-id="87b76-122">In this way, the D3DXQuaternionRotationAxis function can be used as a parameter for another function.</span></span>

<span data-ttu-id="87b76-123">Используйте [**D3DXQuaternionNormalize**](d3d10-d3dxquaternionnormalize.md) для любых входных данных кватернион, которые еще не нормализованы.</span><span class="sxs-lookup"><span data-stu-id="87b76-123">Use [**D3DXQuaternionNormalize**](d3d10-d3dxquaternionnormalize.md) for any quaternion input that is not already normalized.</span></span>

## <a name="requirements"></a><span data-ttu-id="87b76-124">Требования</span><span class="sxs-lookup"><span data-stu-id="87b76-124">Requirements</span></span>



| <span data-ttu-id="87b76-125">Требование</span><span class="sxs-lookup"><span data-stu-id="87b76-125">Requirement</span></span> | <span data-ttu-id="87b76-126">Значение</span><span class="sxs-lookup"><span data-stu-id="87b76-126">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="87b76-127">Header</span><span class="sxs-lookup"><span data-stu-id="87b76-127">Header</span></span><br/>  | <dl> <span data-ttu-id="87b76-128"><dt>D3DX10Math. h</dt></span><span class="sxs-lookup"><span data-stu-id="87b76-128"><dt>D3DX10Math.h</dt></span></span> </dl> |
| <span data-ttu-id="87b76-129">Библиотека</span><span class="sxs-lookup"><span data-stu-id="87b76-129">Library</span></span><br/> | <dl> <span data-ttu-id="87b76-130"><dt>D3DX10. lib</dt></span><span class="sxs-lookup"><span data-stu-id="87b76-130"><dt>D3DX10.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="87b76-131">См. также</span><span class="sxs-lookup"><span data-stu-id="87b76-131">See also</span></span>

<dl> <dt>

[<span data-ttu-id="87b76-132">Математические функции</span><span class="sxs-lookup"><span data-stu-id="87b76-132">Math Functions</span></span>](d3d10-graphics-reference-d3dx10-functions-math.md)
</dt> </dl>

 

 
