---
description: Создает матрицу с заданными значения нутации, шагом и рулоном.
ms.assetid: efaab508-34ed-4373-a8d0-3bc459d75f39
title: Функция D3DXMatrixRotationYawPitchRoll (D3dx9math. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXMatrixRotationYawPitchRoll
api_type:
- LibDef
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 2a8d6a531592ce49342dae0d0ecd6b3ace995bf5
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/15/2021
ms.locfileid: "104273703"
---
# <a name="d3dxmatrixrotationyawpitchroll-function-d3dx9mathh"></a><span data-ttu-id="1eb64-103">Функция D3DXMatrixRotationYawPitchRoll (D3dx9math. h)</span><span class="sxs-lookup"><span data-stu-id="1eb64-103">D3DXMatrixRotationYawPitchRoll function (D3dx9math.h)</span></span>

<span data-ttu-id="1eb64-104">Создает матрицу с заданными значения нутации, шагом и рулоном.</span><span class="sxs-lookup"><span data-stu-id="1eb64-104">Builds a matrix with a specified yaw, pitch, and roll.</span></span>

## <a name="syntax"></a><span data-ttu-id="1eb64-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="1eb64-105">Syntax</span></span>


```C++
D3DXMATRIX* D3DXMatrixRotationYawPitchRoll(
  _Inout_ D3DXMATRIX *pOut,
  _In_    FLOAT      Yaw,
  _In_    FLOAT      Pitch,
  _In_    FLOAT      Roll
);
```



## <a name="parameters"></a><span data-ttu-id="1eb64-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="1eb64-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="1eb64-107">*тоска* \[ в, out\]</span><span class="sxs-lookup"><span data-stu-id="1eb64-107">*pOut* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="1eb64-108">Тип: **[ **D3DXMATRIX**](d3dxmatrix.md)\***</span><span class="sxs-lookup"><span data-stu-id="1eb64-108">Type: **[**D3DXMATRIX**](d3dxmatrix.md)\***</span></span>

<span data-ttu-id="1eb64-109">Указатель на структуру [**D3DXMATRIX**](d3dxmatrix.md) , которая является результатом операции.</span><span class="sxs-lookup"><span data-stu-id="1eb64-109">Pointer to the [**D3DXMATRIX**](d3dxmatrix.md) structure that is the result of the operation.</span></span>

</dd> <dt>

<span data-ttu-id="1eb64-110">*Значения нутации* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="1eb64-110">*Yaw* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="1eb64-111">Тип: **[ **float**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="1eb64-111">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="1eb64-112">Значения нутации вокруг оси y (в радианах).</span><span class="sxs-lookup"><span data-stu-id="1eb64-112">Yaw around the y-axis, in radians.</span></span>

</dd> <dt>

<span data-ttu-id="1eb64-113">*Шаг* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="1eb64-113">*Pitch* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="1eb64-114">Тип: **[ **float**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="1eb64-114">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="1eb64-115">Шаг вокруг оси x в радианах.</span><span class="sxs-lookup"><span data-stu-id="1eb64-115">Pitch around the x-axis, in radians.</span></span>

</dd> <dt>

<span data-ttu-id="1eb64-116">*Рулон* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="1eb64-116">*Roll* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="1eb64-117">Тип: **[ **float**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="1eb64-117">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="1eb64-118">Поворот вокруг оси z в радианах.</span><span class="sxs-lookup"><span data-stu-id="1eb64-118">Roll around the z-axis, in radians.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="1eb64-119">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="1eb64-119">Return value</span></span>

<span data-ttu-id="1eb64-120">Тип: **[ **D3DXMATRIX**](d3dxmatrix.md)\***</span><span class="sxs-lookup"><span data-stu-id="1eb64-120">Type: **[**D3DXMATRIX**](d3dxmatrix.md)\***</span></span>

<span data-ttu-id="1eb64-121">Указатель на структуру [**D3DXMATRIX**](d3dxmatrix.md) с указанными значения нутации, шагом и рулоном.</span><span class="sxs-lookup"><span data-stu-id="1eb64-121">Pointer to a [**D3DXMATRIX**](d3dxmatrix.md) structure with the specified yaw, pitch, and roll.</span></span>

## <a name="remarks"></a><span data-ttu-id="1eb64-122">Комментарии</span><span class="sxs-lookup"><span data-stu-id="1eb64-122">Remarks</span></span>

<span data-ttu-id="1eb64-123">Возвращаемое значение для этой функции совпадает со значением, возвращаемым в параметре *тоска* .</span><span class="sxs-lookup"><span data-stu-id="1eb64-123">The return value for this function is the same value returned in the *pOut* parameter.</span></span> <span data-ttu-id="1eb64-124">Таким образом, функция **D3DXMatrixRotationYawPitchRoll** может использоваться в качестве параметра для другой функции.</span><span class="sxs-lookup"><span data-stu-id="1eb64-124">In this way, the **D3DXMatrixRotationYawPitchRoll** function can be used as a parameter for another function.</span></span>

<span data-ttu-id="1eb64-125">Порядок преобразований первый, затем шаг, затем значения нутации.</span><span class="sxs-lookup"><span data-stu-id="1eb64-125">The order of transformations is roll first, then pitch, then yaw.</span></span> <span data-ttu-id="1eb64-126">Относительно локальной оси координат объекта, это эквивалентно повороту вокруг оси z, за которым следует поворот по оси x, затем поворот вокруг оси y, как показано на следующем рисунке.</span><span class="sxs-lookup"><span data-stu-id="1eb64-126">Relative to the object's local coordinate axis, this is equivalent to rotation around the z-axis, followed by rotation around the x-axis, followed by rotation around the y-axis, as shown in the following illustration.</span></span>

![Иллюстрация «рулона», «тон» и «значения нутацииа» в качестве поворотов вокруг трех осей](images/pitchyawroll.png)

## <a name="requirements"></a><span data-ttu-id="1eb64-128">Требования</span><span class="sxs-lookup"><span data-stu-id="1eb64-128">Requirements</span></span>



| <span data-ttu-id="1eb64-129">Требование</span><span class="sxs-lookup"><span data-stu-id="1eb64-129">Requirement</span></span> | <span data-ttu-id="1eb64-130">Значение</span><span class="sxs-lookup"><span data-stu-id="1eb64-130">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="1eb64-131">Header</span><span class="sxs-lookup"><span data-stu-id="1eb64-131">Header</span></span><br/>  | <dl> <span data-ttu-id="1eb64-132"><dt>D3dx9math. h</dt></span><span class="sxs-lookup"><span data-stu-id="1eb64-132"><dt>D3dx9math.h</dt></span></span> </dl> |
| <span data-ttu-id="1eb64-133">Библиотека</span><span class="sxs-lookup"><span data-stu-id="1eb64-133">Library</span></span><br/> | <dl> <span data-ttu-id="1eb64-134"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="1eb64-134"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="1eb64-135">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="1eb64-135">See also</span></span>

<dl> <dt>

[<span data-ttu-id="1eb64-136">Математические функции</span><span class="sxs-lookup"><span data-stu-id="1eb64-136">Math Functions</span></span>](dx9-graphics-reference-d3dx-functions-math.md)
</dt> <dt>

[<span data-ttu-id="1eb64-137">**D3DXMatrixRotationAxis**</span><span class="sxs-lookup"><span data-stu-id="1eb64-137">**D3DXMatrixRotationAxis**</span></span>](d3dxmatrixrotationaxis.md)
</dt> <dt>

[<span data-ttu-id="1eb64-138">**D3DXMatrixRotationQuaternion**</span><span class="sxs-lookup"><span data-stu-id="1eb64-138">**D3DXMatrixRotationQuaternion**</span></span>](d3dxmatrixrotationquaternion.md)
</dt> <dt>

[<span data-ttu-id="1eb64-139">**D3DXMatrixRotationX**</span><span class="sxs-lookup"><span data-stu-id="1eb64-139">**D3DXMatrixRotationX**</span></span>](d3dxmatrixrotationx.md)
</dt> <dt>

[<span data-ttu-id="1eb64-140">**D3DXMatrixRotationY**</span><span class="sxs-lookup"><span data-stu-id="1eb64-140">**D3DXMatrixRotationY**</span></span>](d3dxmatrixrotationy.md)
</dt> <dt>

[<span data-ttu-id="1eb64-141">**D3DXMatrixRotationZ**</span><span class="sxs-lookup"><span data-stu-id="1eb64-141">**D3DXMatrixRotationZ**</span></span>](d3dxmatrixrotationz.md)
</dt> </dl>

 

 
