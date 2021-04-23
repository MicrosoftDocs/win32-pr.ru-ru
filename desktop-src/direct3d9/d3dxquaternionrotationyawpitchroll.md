---
description: Создает кватернион с заданными значения нутации, шагом и рулоном.
ms.assetid: be4a3bd5-114b-4652-8e0a-e51338317c16
title: Функция D3DXQuaternionRotationYawPitchRoll (D3dx9math. h)
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
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 4d0df60149643db0d9243afe57e394320f81d08c
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/15/2021
ms.locfileid: "105703773"
---
# <a name="d3dxquaternionrotationyawpitchroll-function-d3dx9mathh"></a><span data-ttu-id="c7c92-103">Функция D3DXQuaternionRotationYawPitchRoll (D3dx9math. h)</span><span class="sxs-lookup"><span data-stu-id="c7c92-103">D3DXQuaternionRotationYawPitchRoll function (D3dx9math.h)</span></span>

<span data-ttu-id="c7c92-104">Создает кватернион с заданными значения нутации, шагом и рулоном.</span><span class="sxs-lookup"><span data-stu-id="c7c92-104">Builds a quaternion with the given yaw, pitch, and roll.</span></span>

## <a name="syntax"></a><span data-ttu-id="c7c92-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="c7c92-105">Syntax</span></span>


```C++
D3DXQUATERNION* D3DXQuaternionRotationYawPitchRoll(
  _Inout_ D3DXQUATERNION *pOut,
  _In_    FLOAT          Yaw,
  _In_    FLOAT          Pitch,
  _In_    FLOAT          Roll
);
```



## <a name="parameters"></a><span data-ttu-id="c7c92-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="c7c92-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="c7c92-107">*тоска* \[ в, out\]</span><span class="sxs-lookup"><span data-stu-id="c7c92-107">*pOut* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="c7c92-108">Тип: **[ **D3DXQUATERNION**](d3dxquaternion.md)\***</span><span class="sxs-lookup"><span data-stu-id="c7c92-108">Type: **[**D3DXQUATERNION**](d3dxquaternion.md)\***</span></span>

<span data-ttu-id="c7c92-109">Указатель на структуру [**D3DXQUATERNION**](d3dxquaternion.md) , которая является результатом операции.</span><span class="sxs-lookup"><span data-stu-id="c7c92-109">Pointer to the [**D3DXQUATERNION**](d3dxquaternion.md) structure that is the result of the operation.</span></span>

</dd> <dt>

<span data-ttu-id="c7c92-110">*Значения нутации* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="c7c92-110">*Yaw* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="c7c92-111">Тип: **[ **float**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="c7c92-111">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="c7c92-112">Значения нутации вокруг оси y (в радианах).</span><span class="sxs-lookup"><span data-stu-id="c7c92-112">Yaw around the y-axis, in radians.</span></span>

</dd> <dt>

<span data-ttu-id="c7c92-113">*Шаг* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="c7c92-113">*Pitch* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="c7c92-114">Тип: **[ **float**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="c7c92-114">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="c7c92-115">Шаг вокруг оси x в радианах.</span><span class="sxs-lookup"><span data-stu-id="c7c92-115">Pitch around the x-axis, in radians.</span></span>

</dd> <dt>

<span data-ttu-id="c7c92-116">*Рулон* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="c7c92-116">*Roll* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="c7c92-117">Тип: **[ **float**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="c7c92-117">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="c7c92-118">Поворот вокруг оси z в радианах.</span><span class="sxs-lookup"><span data-stu-id="c7c92-118">Roll around the z-axis, in radians.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="c7c92-119">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="c7c92-119">Return value</span></span>

<span data-ttu-id="c7c92-120">Тип: **[ **D3DXQUATERNION**](d3dxquaternion.md)\***</span><span class="sxs-lookup"><span data-stu-id="c7c92-120">Type: **[**D3DXQUATERNION**](d3dxquaternion.md)\***</span></span>

<span data-ttu-id="c7c92-121">Указатель на структуру [**D3DXQUATERNION**](d3dxquaternion.md) с указанными значения нутации, шагом и рулоном.</span><span class="sxs-lookup"><span data-stu-id="c7c92-121">Pointer to a [**D3DXQUATERNION**](d3dxquaternion.md) structure with the specified yaw, pitch, and roll.</span></span>

## <a name="remarks"></a><span data-ttu-id="c7c92-122">Комментарии</span><span class="sxs-lookup"><span data-stu-id="c7c92-122">Remarks</span></span>

<span data-ttu-id="c7c92-123">Возвращаемое значение для этой функции совпадает со значением, возвращаемым в параметре *тоска* .</span><span class="sxs-lookup"><span data-stu-id="c7c92-123">The return value for this function is the same value returned in the *pOut* parameter.</span></span> <span data-ttu-id="c7c92-124">Таким образом, функция **D3DXQuaternionRotationYawPitchRoll** может использоваться в качестве параметра для другой функции.</span><span class="sxs-lookup"><span data-stu-id="c7c92-124">In this way, the **D3DXQuaternionRotationYawPitchRoll** function can be used as a parameter for another function.</span></span>

<span data-ttu-id="c7c92-125">Используйте [**D3DXQuaternionNormalize**](d3dxquaternionnormalize.md) для любых входных данных кватернион, которые еще не нормализованы.</span><span class="sxs-lookup"><span data-stu-id="c7c92-125">Use [**D3DXQuaternionNormalize**](d3dxquaternionnormalize.md) for any quaternion input that is not already normalized.</span></span>

## <a name="requirements"></a><span data-ttu-id="c7c92-126">Требования</span><span class="sxs-lookup"><span data-stu-id="c7c92-126">Requirements</span></span>



| <span data-ttu-id="c7c92-127">Требование</span><span class="sxs-lookup"><span data-stu-id="c7c92-127">Requirement</span></span> | <span data-ttu-id="c7c92-128">Значение</span><span class="sxs-lookup"><span data-stu-id="c7c92-128">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="c7c92-129">Header</span><span class="sxs-lookup"><span data-stu-id="c7c92-129">Header</span></span><br/>  | <dl> <span data-ttu-id="c7c92-130"><dt>D3dx9math. h</dt></span><span class="sxs-lookup"><span data-stu-id="c7c92-130"><dt>D3dx9math.h</dt></span></span> </dl> |
| <span data-ttu-id="c7c92-131">Библиотека</span><span class="sxs-lookup"><span data-stu-id="c7c92-131">Library</span></span><br/> | <dl> <span data-ttu-id="c7c92-132"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="c7c92-132"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="c7c92-133">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="c7c92-133">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c7c92-134">Математические функции</span><span class="sxs-lookup"><span data-stu-id="c7c92-134">Math Functions</span></span>](dx9-graphics-reference-d3dx-functions-math.md)
</dt> <dt>

[<span data-ttu-id="c7c92-135">**D3DXQuaternionRotationAxis**</span><span class="sxs-lookup"><span data-stu-id="c7c92-135">**D3DXQuaternionRotationAxis**</span></span>](d3dxquaternionrotationaxis.md)
</dt> <dt>

[<span data-ttu-id="c7c92-136">**D3DXQuaternionRotationMatrix**</span><span class="sxs-lookup"><span data-stu-id="c7c92-136">**D3DXQuaternionRotationMatrix**</span></span>](d3dxquaternionrotationmatrix.md)
</dt> </dl>

 

 
