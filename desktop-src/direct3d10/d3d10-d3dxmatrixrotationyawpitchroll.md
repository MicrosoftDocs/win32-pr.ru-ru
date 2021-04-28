---
description: Функция D3DXMatrixRotationYawPitchRoll (D3DX10Math. h) — создает матрицу с указанными значения нутации, шагом и рулоном.
ms.assetid: a3ef2b57-275f-484a-88fc-aaa5e470717c
title: Функция D3DXMatrixRotationYawPitchRoll (D3DX10Math. h)
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
- D3DX10.lib
- D3DX10.dll
ms.openlocfilehash: ae00865c45878159dbf86a6f829e9d1cf50337e3
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2021
ms.locfileid: "108108952"
---
# <a name="d3dxmatrixrotationyawpitchroll-function-d3dx10mathh"></a><span data-ttu-id="1ff50-103">Функция D3DXMatrixRotationYawPitchRoll (D3DX10Math. h)</span><span class="sxs-lookup"><span data-stu-id="1ff50-103">D3DXMatrixRotationYawPitchRoll function (D3DX10Math.h)</span></span>

<span data-ttu-id="1ff50-104">Создает матрицу с заданными значения нутации, шагом и рулоном.</span><span class="sxs-lookup"><span data-stu-id="1ff50-104">Builds a matrix with a specified yaw, pitch, and roll.</span></span>

## <a name="syntax"></a><span data-ttu-id="1ff50-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="1ff50-105">Syntax</span></span>


```C++
D3DXMATRIX* D3DXMatrixRotationYawPitchRoll(
  _Inout_ D3DXMATRIX *pOut,
  _In_    FLOAT      Yaw,
  _In_    FLOAT      Pitch,
  _In_    FLOAT      Roll
);
```



## <a name="parameters"></a><span data-ttu-id="1ff50-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="1ff50-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="1ff50-107">*тоска* \[ в, out\]</span><span class="sxs-lookup"><span data-stu-id="1ff50-107">*pOut* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="1ff50-108">Тип: **[ **D3DXMATRIX**](../direct3d9/d3dxmatrix.md)\***</span><span class="sxs-lookup"><span data-stu-id="1ff50-108">Type: **[**D3DXMATRIX**](../direct3d9/d3dxmatrix.md)\***</span></span>

<span data-ttu-id="1ff50-109">Указатель на структуру [**D3DXMATRIX**](d3d10-d3dxmatrix.md) , которая является результатом операции.</span><span class="sxs-lookup"><span data-stu-id="1ff50-109">Pointer to the [**D3DXMATRIX**](d3d10-d3dxmatrix.md) structure that is the result of the operation.</span></span>

</dd> <dt>

<span data-ttu-id="1ff50-110">*Значения нутации* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="1ff50-110">*Yaw* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="1ff50-111">Тип: **[ **float**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="1ff50-111">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="1ff50-112">Значения нутации вокруг оси y (в радианах).</span><span class="sxs-lookup"><span data-stu-id="1ff50-112">Yaw around the y-axis, in radians.</span></span>

</dd> <dt>

<span data-ttu-id="1ff50-113">*Шаг* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="1ff50-113">*Pitch* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="1ff50-114">Тип: **[ **float**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="1ff50-114">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="1ff50-115">Шаг вокруг оси x в радианах.</span><span class="sxs-lookup"><span data-stu-id="1ff50-115">Pitch around the x-axis, in radians.</span></span>

</dd> <dt>

<span data-ttu-id="1ff50-116">*Рулон* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="1ff50-116">*Roll* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="1ff50-117">Тип: **[ **float**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="1ff50-117">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="1ff50-118">Поворот вокруг оси z в радианах.</span><span class="sxs-lookup"><span data-stu-id="1ff50-118">Roll around the z-axis, in radians.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="1ff50-119">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="1ff50-119">Return value</span></span>

<span data-ttu-id="1ff50-120">Тип: **[ **D3DXMATRIX**](../direct3d9/d3dxmatrix.md)\***</span><span class="sxs-lookup"><span data-stu-id="1ff50-120">Type: **[**D3DXMATRIX**](../direct3d9/d3dxmatrix.md)\***</span></span>

<span data-ttu-id="1ff50-121">Указатель на структуру D3DXMATRIX с указанными значения нутации, шагом и рулоном.</span><span class="sxs-lookup"><span data-stu-id="1ff50-121">Pointer to a D3DXMATRIX structure with the specified yaw, pitch, and roll.</span></span>

## <a name="remarks"></a><span data-ttu-id="1ff50-122">Remarks</span><span class="sxs-lookup"><span data-stu-id="1ff50-122">Remarks</span></span>

<span data-ttu-id="1ff50-123">Возвращаемое значение для этой функции совпадает со значением, возвращаемым в параметре тоска.</span><span class="sxs-lookup"><span data-stu-id="1ff50-123">The return value for this function is the same value returned in the pOut parameter.</span></span> <span data-ttu-id="1ff50-124">Таким образом, функция D3DXMatrixRotationYawPitchRoll может использоваться в качестве параметра для другой функции.</span><span class="sxs-lookup"><span data-stu-id="1ff50-124">In this way, the D3DXMatrixRotationYawPitchRoll function can be used as a parameter for another function.</span></span>

<span data-ttu-id="1ff50-125">Порядок преобразований первый, затем шаг, затем значения нутации.</span><span class="sxs-lookup"><span data-stu-id="1ff50-125">The order of transformations is roll first, then pitch, then yaw.</span></span> <span data-ttu-id="1ff50-126">Относительно локальной оси координат объекта, это эквивалентно повороту вокруг оси z, за которым следует поворот по оси x, затем поворот вокруг оси y, как показано на следующем рисунке.</span><span class="sxs-lookup"><span data-stu-id="1ff50-126">Relative to the object's local coordinate axis, this is equivalent to rotation around the z-axis, followed by rotation around the x-axis, followed by rotation around the y-axis, as shown in the following illustration.</span></span>

![Иллюстрация «рулона», «тон» и «значения нутацииа» в качестве поворотов вокруг трех осей](images/pitchyawroll.png)

## <a name="requirements"></a><span data-ttu-id="1ff50-128">Требования</span><span class="sxs-lookup"><span data-stu-id="1ff50-128">Requirements</span></span>



| <span data-ttu-id="1ff50-129">Требование</span><span class="sxs-lookup"><span data-stu-id="1ff50-129">Requirement</span></span> | <span data-ttu-id="1ff50-130">Значение</span><span class="sxs-lookup"><span data-stu-id="1ff50-130">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="1ff50-131">Header</span><span class="sxs-lookup"><span data-stu-id="1ff50-131">Header</span></span><br/>  | <dl> <span data-ttu-id="1ff50-132"><dt>D3DX10Math. h</dt></span><span class="sxs-lookup"><span data-stu-id="1ff50-132"><dt>D3DX10Math.h</dt></span></span> </dl> |
| <span data-ttu-id="1ff50-133">Библиотека</span><span class="sxs-lookup"><span data-stu-id="1ff50-133">Library</span></span><br/> | <dl> <span data-ttu-id="1ff50-134"><dt>D3DX10. lib</dt></span><span class="sxs-lookup"><span data-stu-id="1ff50-134"><dt>D3DX10.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="1ff50-135">См. также</span><span class="sxs-lookup"><span data-stu-id="1ff50-135">See also</span></span>

<dl> <dt>

[<span data-ttu-id="1ff50-136">Математические функции</span><span class="sxs-lookup"><span data-stu-id="1ff50-136">Math Functions</span></span>](d3d10-graphics-reference-d3dx10-functions-math.md)
</dt> </dl>

 

 
