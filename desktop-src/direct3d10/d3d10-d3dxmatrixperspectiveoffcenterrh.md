---
description: Создает настраиваемую, правую матрицу перспективной проекции.
ms.assetid: 51509bfc-2f49-4ba7-8918-3c44d857d4b2
title: Функция D3DXMatrixPerspectiveOffCenterRH (D3DX10Math. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXMatrixPerspectiveOffCenterRH
api_type:
- LibDef
api_location:
- D3DX10.lib
- D3DX10.dll
ms.openlocfilehash: 54fc98658d5466acd69d3245af7488c40cd352c5
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/15/2021
ms.locfileid: "104081925"
---
# <a name="d3dxmatrixperspectiveoffcenterrh-function-d3dx10mathh"></a><span data-ttu-id="f222d-103">Функция D3DXMatrixPerspectiveOffCenterRH (D3DX10Math. h)</span><span class="sxs-lookup"><span data-stu-id="f222d-103">D3DXMatrixPerspectiveOffCenterRH function (D3DX10Math.h)</span></span>

<span data-ttu-id="f222d-104">Создает настраиваемую, правую матрицу перспективной проекции.</span><span class="sxs-lookup"><span data-stu-id="f222d-104">Builds a customized, right-handed perspective projection matrix.</span></span>

## <a name="syntax"></a><span data-ttu-id="f222d-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="f222d-105">Syntax</span></span>


```C++
D3DXMATRIX* D3DXMatrixPerspectiveOffCenterRH(
  _Inout_ D3DXMATRIX *pOut,
  _In_    FLOAT      l,
  _In_    FLOAT      r,
  _In_    FLOAT      b,
  _In_    FLOAT      t,
  _In_    FLOAT      zn,
  _In_    FLOAT      zf
);
```



## <a name="parameters"></a><span data-ttu-id="f222d-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="f222d-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="f222d-107">*тоска* \[ в, out\]</span><span class="sxs-lookup"><span data-stu-id="f222d-107">*pOut* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="f222d-108">Тип: **[ **D3DXMATRIX**](../direct3d9/d3dxmatrix.md)\***</span><span class="sxs-lookup"><span data-stu-id="f222d-108">Type: **[**D3DXMATRIX**](../direct3d9/d3dxmatrix.md)\***</span></span>

<span data-ttu-id="f222d-109">Указатель на структуру [**D3DXMATRIX**](d3d10-d3dxmatrix.md) , которая является результатом операции.</span><span class="sxs-lookup"><span data-stu-id="f222d-109">Pointer to the [**D3DXMATRIX**](d3d10-d3dxmatrix.md) structure that is the result of the operation.</span></span>

</dd> <dt>

<span data-ttu-id="f222d-110">*l* \[ в\]</span><span class="sxs-lookup"><span data-stu-id="f222d-110">*l* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="f222d-111">Тип: **[ **float**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="f222d-111">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="f222d-112">Минимальное значение x для представления объема.</span><span class="sxs-lookup"><span data-stu-id="f222d-112">Minimum x-value of the view volume.</span></span>

</dd> <dt>

<span data-ttu-id="f222d-113">*r* \[ в\]</span><span class="sxs-lookup"><span data-stu-id="f222d-113">*r* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="f222d-114">Тип: **[ **float**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="f222d-114">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="f222d-115">Максимальное значение x-значения для представления объема.</span><span class="sxs-lookup"><span data-stu-id="f222d-115">Maximum x-value of the view volume.</span></span>

</dd> <dt>

<span data-ttu-id="f222d-116">*б* \[ в\]</span><span class="sxs-lookup"><span data-stu-id="f222d-116">*b* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="f222d-117">Тип: **[ **float**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="f222d-117">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="f222d-118">Минимальное значение y для представления объема.</span><span class="sxs-lookup"><span data-stu-id="f222d-118">Minimum y-value of the view volume.</span></span>

</dd> <dt>

<span data-ttu-id="f222d-119">*t* \[ в\]</span><span class="sxs-lookup"><span data-stu-id="f222d-119">*t* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="f222d-120">Тип: **[ **float**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="f222d-120">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="f222d-121">Максимальное значение y для представления объема.</span><span class="sxs-lookup"><span data-stu-id="f222d-121">Maximum y-value of the view volume.</span></span>

</dd> <dt>

<span data-ttu-id="f222d-122">*ЗН* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="f222d-122">*zn* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="f222d-123">Тип: **[ **float**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="f222d-123">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="f222d-124">Минимальное z-значение отображаемого объема.</span><span class="sxs-lookup"><span data-stu-id="f222d-124">Minimum z-value of the view volume.</span></span>

</dd> <dt>

<span data-ttu-id="f222d-125">*ЗФ* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="f222d-125">*zf* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="f222d-126">Тип: **[ **float**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="f222d-126">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="f222d-127">Максимальное z-значение отображаемого объема.</span><span class="sxs-lookup"><span data-stu-id="f222d-127">Maximum z-value of the view volume.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="f222d-128">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="f222d-128">Return value</span></span>

<span data-ttu-id="f222d-129">Тип: **[ **D3DXMATRIX**](../direct3d9/d3dxmatrix.md)\***</span><span class="sxs-lookup"><span data-stu-id="f222d-129">Type: **[**D3DXMATRIX**](../direct3d9/d3dxmatrix.md)\***</span></span>

<span data-ttu-id="f222d-130">Указатель на структуру D3DXMATRIX, которая представляет собой настраиваемую, правую матрицу проекции с правой стороны.</span><span class="sxs-lookup"><span data-stu-id="f222d-130">Pointer to a D3DXMATRIX structure that is a customized, right-handed perspective projection matrix.</span></span>

## <a name="remarks"></a><span data-ttu-id="f222d-131">Комментарии</span><span class="sxs-lookup"><span data-stu-id="f222d-131">Remarks</span></span>

<span data-ttu-id="f222d-132">Все параметры функции D3DXMatrixPerspectiveOffCenterRH — это расстояния в пространстве камеры.</span><span class="sxs-lookup"><span data-stu-id="f222d-132">All the parameters of the D3DXMatrixPerspectiveOffCenterRH function are distances in camera space.</span></span> <span data-ttu-id="f222d-133">Параметры описывают размеры представления объема.</span><span class="sxs-lookup"><span data-stu-id="f222d-133">The parameters describe the dimensions of the view volume.</span></span>

<span data-ttu-id="f222d-134">Возвращаемое значение для этой функции совпадает со значением, возвращаемым в параметре тоска.</span><span class="sxs-lookup"><span data-stu-id="f222d-134">The return value for this function is the same value returned in the pOut parameter.</span></span> <span data-ttu-id="f222d-135">Таким образом, функция D3DXMatrixPerspectiveOffCenterRH может использоваться в качестве параметра для другой функции.</span><span class="sxs-lookup"><span data-stu-id="f222d-135">In this way, the D3DXMatrixPerspectiveOffCenterRH function can be used as a parameter for another function.</span></span>

<span data-ttu-id="f222d-136">Эта функция использует следующую формулу для вычисления возвращаемой матрицы.</span><span class="sxs-lookup"><span data-stu-id="f222d-136">This function uses the following formula to compute the returned matrix.</span></span>


```
2*zn/(r-l)   0            0                0
0            2*zn/(t-b)   0                0
(l+r)/(r-l)  (t+b)/(t-b)  zf/(zn-zf)      -1
0            0            zn*zf/(zn-zf)    0
```



## <a name="requirements"></a><span data-ttu-id="f222d-137">Требования</span><span class="sxs-lookup"><span data-stu-id="f222d-137">Requirements</span></span>



| <span data-ttu-id="f222d-138">Требование</span><span class="sxs-lookup"><span data-stu-id="f222d-138">Requirement</span></span> | <span data-ttu-id="f222d-139">Значение</span><span class="sxs-lookup"><span data-stu-id="f222d-139">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="f222d-140">Header</span><span class="sxs-lookup"><span data-stu-id="f222d-140">Header</span></span><br/>  | <dl> <span data-ttu-id="f222d-141"><dt>D3DX10Math. h</dt></span><span class="sxs-lookup"><span data-stu-id="f222d-141"><dt>D3DX10Math.h</dt></span></span> </dl> |
| <span data-ttu-id="f222d-142">Библиотека</span><span class="sxs-lookup"><span data-stu-id="f222d-142">Library</span></span><br/> | <dl> <span data-ttu-id="f222d-143"><dt>D3DX10. lib</dt></span><span class="sxs-lookup"><span data-stu-id="f222d-143"><dt>D3DX10.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="f222d-144">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="f222d-144">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f222d-145">Математические функции</span><span class="sxs-lookup"><span data-stu-id="f222d-145">Math Functions</span></span>](d3d10-graphics-reference-d3dx10-functions-math.md)
</dt> </dl>

 

 
