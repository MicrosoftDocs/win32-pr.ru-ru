---
description: Поворачивает кватернион по произвольной оси.
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
ms.openlocfilehash: 7974a1199c468ac762042ae41af59f5a3b66bafd
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/15/2021
ms.locfileid: "105703733"
---
# <a name="d3dxquaternionrotationaxis-function-d3dx9mathh"></a><span data-ttu-id="9baef-103">Функция D3DXQuaternionRotationAxis (D3dx9math. h)</span><span class="sxs-lookup"><span data-stu-id="9baef-103">D3DXQuaternionRotationAxis function (D3dx9math.h)</span></span>

<span data-ttu-id="9baef-104">Поворачивает кватернион по произвольной оси.</span><span class="sxs-lookup"><span data-stu-id="9baef-104">Rotates a quaternion about an arbitrary axis.</span></span>

## <a name="syntax"></a><span data-ttu-id="9baef-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="9baef-105">Syntax</span></span>


```C++
D3DXQUATERNION* D3DXQuaternionRotationAxis(
  _Inout_       D3DXQUATERNION *pOut,
  _In_    const D3DXVECTOR3    *pV,
  _In_          FLOAT          Angle
);
```



## <a name="parameters"></a><span data-ttu-id="9baef-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="9baef-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="9baef-107">*тоска* \[ в, out\]</span><span class="sxs-lookup"><span data-stu-id="9baef-107">*pOut* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="9baef-108">Тип: **[ **D3DXQUATERNION**](d3dxquaternion.md)\***</span><span class="sxs-lookup"><span data-stu-id="9baef-108">Type: **[**D3DXQUATERNION**](d3dxquaternion.md)\***</span></span>

<span data-ttu-id="9baef-109">Указатель на структуру [**D3DXQUATERNION**](d3dxquaternion.md) , которая является результатом операции.</span><span class="sxs-lookup"><span data-stu-id="9baef-109">Pointer to the [**D3DXQUATERNION**](d3dxquaternion.md) structure that is the result of the operation.</span></span>

</dd> <dt>

<span data-ttu-id="9baef-110">*ПС* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="9baef-110">*pV* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="9baef-111">Тип: **const [**D3DXVECTOR3**](d3dxvector3.md) \***</span><span class="sxs-lookup"><span data-stu-id="9baef-111">Type: **const [**D3DXVECTOR3**](d3dxvector3.md)\***</span></span>

<span data-ttu-id="9baef-112">Указатель на структуру [**D3DXVECTOR3**](d3dxvector3.md) , определяющую ось, для которой необходимо повернуть кватернион.</span><span class="sxs-lookup"><span data-stu-id="9baef-112">Pointer to the [**D3DXVECTOR3**](d3dxvector3.md) structure that identifies the axis about which to rotate the quaternion.</span></span>

</dd> <dt>

<span data-ttu-id="9baef-113">*Угол* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="9baef-113">*Angle* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="9baef-114">Тип: **[ **float**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="9baef-114">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="9baef-115">Угол поворота в радианах.</span><span class="sxs-lookup"><span data-stu-id="9baef-115">Angle of rotation, in radians.</span></span> <span data-ttu-id="9baef-116">Углы измеряются по часовой стрелке, если смотреть вдоль оси поворота в направлении начала координат.</span><span class="sxs-lookup"><span data-stu-id="9baef-116">Angles are measured clockwise when looking along the rotation axis toward the origin.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="9baef-117">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="9baef-117">Return value</span></span>

<span data-ttu-id="9baef-118">Тип: **[ **D3DXQUATERNION**](d3dxquaternion.md)\***</span><span class="sxs-lookup"><span data-stu-id="9baef-118">Type: **[**D3DXQUATERNION**](d3dxquaternion.md)\***</span></span>

<span data-ttu-id="9baef-119">Указатель на структуру [**D3DXQUATERNION**](d3dxquaternion.md) , повернутую вокруг указанной оси.</span><span class="sxs-lookup"><span data-stu-id="9baef-119">Pointer to a [**D3DXQUATERNION**](d3dxquaternion.md) structure rotated around the specified axis.</span></span>

## <a name="remarks"></a><span data-ttu-id="9baef-120">Комментарии</span><span class="sxs-lookup"><span data-stu-id="9baef-120">Remarks</span></span>

<span data-ttu-id="9baef-121">Возвращаемое значение для этой функции совпадает со значением, возвращаемым в параметре *тоска* .</span><span class="sxs-lookup"><span data-stu-id="9baef-121">The return value for this function is the same value returned in the *pOut* parameter.</span></span> <span data-ttu-id="9baef-122">Таким образом, функция **D3DXQuaternionRotationAxis** может использоваться в качестве параметра для другой функции.</span><span class="sxs-lookup"><span data-stu-id="9baef-122">In this way, the **D3DXQuaternionRotationAxis** function can be used as a parameter for another function.</span></span>

<span data-ttu-id="9baef-123">Используйте [**D3DXQuaternionNormalize**](d3dxquaternionnormalize.md) для любых входных данных кватернион, которые еще не нормализованы.</span><span class="sxs-lookup"><span data-stu-id="9baef-123">Use [**D3DXQuaternionNormalize**](d3dxquaternionnormalize.md) for any quaternion input that is not already normalized.</span></span>

## <a name="requirements"></a><span data-ttu-id="9baef-124">Требования</span><span class="sxs-lookup"><span data-stu-id="9baef-124">Requirements</span></span>



| <span data-ttu-id="9baef-125">Требование</span><span class="sxs-lookup"><span data-stu-id="9baef-125">Requirement</span></span> | <span data-ttu-id="9baef-126">Значение</span><span class="sxs-lookup"><span data-stu-id="9baef-126">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="9baef-127">Header</span><span class="sxs-lookup"><span data-stu-id="9baef-127">Header</span></span><br/>  | <dl> <span data-ttu-id="9baef-128"><dt>D3dx9math. h</dt></span><span class="sxs-lookup"><span data-stu-id="9baef-128"><dt>D3dx9math.h</dt></span></span> </dl> |
| <span data-ttu-id="9baef-129">Библиотека</span><span class="sxs-lookup"><span data-stu-id="9baef-129">Library</span></span><br/> | <dl> <span data-ttu-id="9baef-130"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="9baef-130"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="9baef-131">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="9baef-131">See also</span></span>

<dl> <dt>

[<span data-ttu-id="9baef-132">Математические функции</span><span class="sxs-lookup"><span data-stu-id="9baef-132">Math Functions</span></span>](dx9-graphics-reference-d3dx-functions-math.md)
</dt> <dt>

[<span data-ttu-id="9baef-133">**D3DXQuaternionRotationMatrix**</span><span class="sxs-lookup"><span data-stu-id="9baef-133">**D3DXQuaternionRotationMatrix**</span></span>](d3dxquaternionrotationmatrix.md)
</dt> <dt>

[<span data-ttu-id="9baef-134">**D3DXQuaternionRotationYawPitchRoll**</span><span class="sxs-lookup"><span data-stu-id="9baef-134">**D3DXQuaternionRotationYawPitchRoll**</span></span>](d3dxquaternionrotationyawpitchroll.md)
</dt> </dl>

 

 
