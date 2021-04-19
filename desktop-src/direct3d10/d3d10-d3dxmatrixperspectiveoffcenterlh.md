---
description: Создает настроенную левую матрицу проекции с левой стороны.
ms.assetid: 73616fcc-1799-4e65-92b9-2d8f500c326e
title: Функция D3DXMatrixPerspectiveOffCenterLH (D3DX10Math. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXMatrixPerspectiveOffCenterLH
api_type:
- LibDef
api_location:
- D3DX10.lib
- D3DX10.dll
ms.openlocfilehash: 2fb289c0dff148850b8174ccb04a3e3fbfa79d92
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/15/2021
ms.locfileid: "105720966"
---
# <a name="d3dxmatrixperspectiveoffcenterlh-function-d3dx10mathh"></a><span data-ttu-id="028fc-103">Функция D3DXMatrixPerspectiveOffCenterLH (D3DX10Math. h)</span><span class="sxs-lookup"><span data-stu-id="028fc-103">D3DXMatrixPerspectiveOffCenterLH function (D3DX10Math.h)</span></span>

<span data-ttu-id="028fc-104">Создает настроенную левую матрицу проекции с левой стороны.</span><span class="sxs-lookup"><span data-stu-id="028fc-104">Builds a customized, left-handed perspective projection matrix.</span></span>

## <a name="syntax"></a><span data-ttu-id="028fc-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="028fc-105">Syntax</span></span>


```C++
D3DXMATRIX* D3DXMatrixPerspectiveOffCenterLH(
  _Inout_ D3DXMATRIX *pOut,
  _In_    FLOAT      l,
  _In_    FLOAT      r,
  _In_    FLOAT      b,
  _In_    FLOAT      t,
  _In_    FLOAT      zn,
  _In_    FLOAT      zf
);
```



## <a name="parameters"></a><span data-ttu-id="028fc-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="028fc-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="028fc-107">*тоска* \[ в, out\]</span><span class="sxs-lookup"><span data-stu-id="028fc-107">*pOut* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="028fc-108">Тип: **[ **D3DXMATRIX**](../direct3d9/d3dxmatrix.md)\***</span><span class="sxs-lookup"><span data-stu-id="028fc-108">Type: **[**D3DXMATRIX**](../direct3d9/d3dxmatrix.md)\***</span></span>

<span data-ttu-id="028fc-109">Указатель на структуру [**D3DXMATRIX**](d3d10-d3dxmatrix.md) , которая является результатом операции.</span><span class="sxs-lookup"><span data-stu-id="028fc-109">Pointer to the [**D3DXMATRIX**](d3d10-d3dxmatrix.md) structure that is the result of the operation.</span></span>

</dd> <dt>

<span data-ttu-id="028fc-110">*l* \[ в\]</span><span class="sxs-lookup"><span data-stu-id="028fc-110">*l* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="028fc-111">Тип: **[ **float**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="028fc-111">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="028fc-112">Минимальное значение x для представления объема.</span><span class="sxs-lookup"><span data-stu-id="028fc-112">Minimum x-value of the view volume.</span></span>

</dd> <dt>

<span data-ttu-id="028fc-113">*r* \[ в\]</span><span class="sxs-lookup"><span data-stu-id="028fc-113">*r* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="028fc-114">Тип: **[ **float**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="028fc-114">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="028fc-115">Максимальное значение x-значения для представления объема.</span><span class="sxs-lookup"><span data-stu-id="028fc-115">Maximum x-value of the view volume.</span></span>

</dd> <dt>

<span data-ttu-id="028fc-116">*б* \[ в\]</span><span class="sxs-lookup"><span data-stu-id="028fc-116">*b* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="028fc-117">Тип: **[ **float**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="028fc-117">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="028fc-118">Минимальное значение y для представления объема.</span><span class="sxs-lookup"><span data-stu-id="028fc-118">Minimum y-value of the view volume.</span></span>

</dd> <dt>

<span data-ttu-id="028fc-119">*t* \[ в\]</span><span class="sxs-lookup"><span data-stu-id="028fc-119">*t* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="028fc-120">Тип: **[ **float**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="028fc-120">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="028fc-121">Максимальное значение y для представления объема.</span><span class="sxs-lookup"><span data-stu-id="028fc-121">Maximum y-value of the view volume.</span></span>

</dd> <dt>

<span data-ttu-id="028fc-122">*ЗН* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="028fc-122">*zn* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="028fc-123">Тип: **[ **float**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="028fc-123">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="028fc-124">Минимальное z-значение отображаемого объема.</span><span class="sxs-lookup"><span data-stu-id="028fc-124">Minimum z-value of the view volume.</span></span>

</dd> <dt>

<span data-ttu-id="028fc-125">*ЗФ* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="028fc-125">*zf* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="028fc-126">Тип: **[ **float**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="028fc-126">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="028fc-127">Максимальное z-значение отображаемого объема.</span><span class="sxs-lookup"><span data-stu-id="028fc-127">Maximum z-value of the view volume.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="028fc-128">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="028fc-128">Return value</span></span>

<span data-ttu-id="028fc-129">Тип: **[ **D3DXMATRIX**](../direct3d9/d3dxmatrix.md)\***</span><span class="sxs-lookup"><span data-stu-id="028fc-129">Type: **[**D3DXMATRIX**](../direct3d9/d3dxmatrix.md)\***</span></span>

<span data-ttu-id="028fc-130">Указатель на структуру D3DXMATRIX, которая является настраиваемой матрицей проекции слева.</span><span class="sxs-lookup"><span data-stu-id="028fc-130">Pointer to a D3DXMATRIX structure that is a customized, left-handed perspective projection matrix.</span></span>

## <a name="remarks"></a><span data-ttu-id="028fc-131">Комментарии</span><span class="sxs-lookup"><span data-stu-id="028fc-131">Remarks</span></span>

<span data-ttu-id="028fc-132">Все параметры функции D3DXMatrixPerspectiveOffCenterLH — это расстояния в пространстве камеры.</span><span class="sxs-lookup"><span data-stu-id="028fc-132">All the parameters of the D3DXMatrixPerspectiveOffCenterLH function are distances in camera space.</span></span> <span data-ttu-id="028fc-133">Параметры описывают размеры представления объема.</span><span class="sxs-lookup"><span data-stu-id="028fc-133">The parameters describe the dimensions of the view volume.</span></span>

<span data-ttu-id="028fc-134">Возвращаемое значение для этой функции совпадает со значением, возвращаемым в параметре тоска.</span><span class="sxs-lookup"><span data-stu-id="028fc-134">The return value for this function is the same value returned in the pOut parameter.</span></span> <span data-ttu-id="028fc-135">Таким образом, функция D3DXMatrixPerspectiveOffCenterLH может использоваться в качестве параметра для другой функции.</span><span class="sxs-lookup"><span data-stu-id="028fc-135">In this way, the D3DXMatrixPerspectiveOffCenterLH function can be used as a parameter for another function.</span></span>

<span data-ttu-id="028fc-136">Эта функция использует следующую формулу для вычисления возвращаемой матрицы.</span><span class="sxs-lookup"><span data-stu-id="028fc-136">This function uses the following formula to compute the returned matrix.</span></span>


```
2*zn/(r-l)   0            0              0
0            2*zn/(t-b)   0              0
(l+r)/(l-r)  (t+b)/(b-t)  zf/(zf-zn)     1
0            0            zn*zf/(zn-zf)  0
```



## <a name="requirements"></a><span data-ttu-id="028fc-137">Требования</span><span class="sxs-lookup"><span data-stu-id="028fc-137">Requirements</span></span>



| <span data-ttu-id="028fc-138">Требование</span><span class="sxs-lookup"><span data-stu-id="028fc-138">Requirement</span></span> | <span data-ttu-id="028fc-139">Значение</span><span class="sxs-lookup"><span data-stu-id="028fc-139">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="028fc-140">Header</span><span class="sxs-lookup"><span data-stu-id="028fc-140">Header</span></span><br/>  | <dl> <span data-ttu-id="028fc-141"><dt>D3DX10Math. h</dt></span><span class="sxs-lookup"><span data-stu-id="028fc-141"><dt>D3DX10Math.h</dt></span></span> </dl> |
| <span data-ttu-id="028fc-142">Библиотека</span><span class="sxs-lookup"><span data-stu-id="028fc-142">Library</span></span><br/> | <dl> <span data-ttu-id="028fc-143"><dt>D3DX10. lib</dt></span><span class="sxs-lookup"><span data-stu-id="028fc-143"><dt>D3DX10.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="028fc-144">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="028fc-144">See also</span></span>

<dl> <dt>

[<span data-ttu-id="028fc-145">Математические функции</span><span class="sxs-lookup"><span data-stu-id="028fc-145">Math Functions</span></span>](d3d10-graphics-reference-d3dx10-functions-math.md)
</dt> </dl>

 

 
