---
description: Строит правовинтовую матрицу перспективной проекции на основании поля зрения.
ms.assetid: a75e6666-e6c0-4a54-bc88-835fa012542f
title: Функция D3DXMatrixPerspectiveFovRH (D3DX10Math. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXMatrixPerspectiveFovRH
api_type:
- LibDef
api_location:
- D3DX10.lib
- D3DX10.dll
ms.openlocfilehash: baad02b5840af8e244cd562def4aeb8f9ac2988a
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/15/2021
ms.locfileid: "104000440"
---
# <a name="d3dxmatrixperspectivefovrh-function-d3dx10mathh"></a><span data-ttu-id="4bc67-103">Функция D3DXMatrixPerspectiveFovRH (D3DX10Math. h)</span><span class="sxs-lookup"><span data-stu-id="4bc67-103">D3DXMatrixPerspectiveFovRH function (D3DX10Math.h)</span></span>

<span data-ttu-id="4bc67-104">Строит правовинтовую матрицу перспективной проекции на основании поля зрения.</span><span class="sxs-lookup"><span data-stu-id="4bc67-104">Builds a right-handed perspective projection matrix based on a field of view.</span></span>

## <a name="syntax"></a><span data-ttu-id="4bc67-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="4bc67-105">Syntax</span></span>


```C++
D3DXMATRIX* D3DXMatrixPerspectiveFovRH(
  _Inout_ D3DXMATRIX *pOut,
  _In_    FLOAT      fovy,
  _In_    FLOAT      Aspect,
  _In_    FLOAT      zn,
  _In_    FLOAT      zf
);
```



## <a name="parameters"></a><span data-ttu-id="4bc67-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="4bc67-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="4bc67-107">*тоска* \[ в, out\]</span><span class="sxs-lookup"><span data-stu-id="4bc67-107">*pOut* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="4bc67-108">Тип: **[ **D3DXMATRIX**](../direct3d9/d3dxmatrix.md)\***</span><span class="sxs-lookup"><span data-stu-id="4bc67-108">Type: **[**D3DXMATRIX**](../direct3d9/d3dxmatrix.md)\***</span></span>

<span data-ttu-id="4bc67-109">Указатель на структуру [**D3DXMATRIX**](d3d10-d3dxmatrix.md) , которая является результатом операции.</span><span class="sxs-lookup"><span data-stu-id="4bc67-109">Pointer to the [**D3DXMATRIX**](d3d10-d3dxmatrix.md) structure that is the result of the operation.</span></span>

</dd> <dt>

<span data-ttu-id="4bc67-110">*ФОВИ* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="4bc67-110">*fovy* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="4bc67-111">Тип: **[ **float**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="4bc67-111">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="4bc67-112">Поле представления в направлении y (в радианах).</span><span class="sxs-lookup"><span data-stu-id="4bc67-112">Field of view in the y direction, in radians.</span></span>

</dd> <dt>

<span data-ttu-id="4bc67-113">*Аспект* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="4bc67-113">*Aspect* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="4bc67-114">Тип: **[ **float**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="4bc67-114">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="4bc67-115">Пропорции, определенные как ширина представления, деленная на высоту.</span><span class="sxs-lookup"><span data-stu-id="4bc67-115">Aspect ratio, defined as view space width divided by height.</span></span>

</dd> <dt>

<span data-ttu-id="4bc67-116">*ЗН* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="4bc67-116">*zn* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="4bc67-117">Тип: **[ **float**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="4bc67-117">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="4bc67-118">Z-значение ближней плоскости просмотра.</span><span class="sxs-lookup"><span data-stu-id="4bc67-118">Z-value of the near view-plane.</span></span>

</dd> <dt>

<span data-ttu-id="4bc67-119">*ЗФ* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="4bc67-119">*zf* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="4bc67-120">Тип: **[ **float**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="4bc67-120">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="4bc67-121">Z-значение дальней плоскости просмотра.</span><span class="sxs-lookup"><span data-stu-id="4bc67-121">Z-value of the far view-plane.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="4bc67-122">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="4bc67-122">Return value</span></span>

<span data-ttu-id="4bc67-123">Тип: **[ **D3DXMATRIX**](../direct3d9/d3dxmatrix.md)\***</span><span class="sxs-lookup"><span data-stu-id="4bc67-123">Type: **[**D3DXMATRIX**](../direct3d9/d3dxmatrix.md)\***</span></span>

<span data-ttu-id="4bc67-124">Указатель на структуру D3DXMATRIX, которая является матрицей с правой стороны проекций.</span><span class="sxs-lookup"><span data-stu-id="4bc67-124">Pointer to a D3DXMATRIX structure that is a right-handed perspective projection matrix.</span></span>

## <a name="remarks"></a><span data-ttu-id="4bc67-125">Комментарии</span><span class="sxs-lookup"><span data-stu-id="4bc67-125">Remarks</span></span>

<span data-ttu-id="4bc67-126">Возвращаемое значение для этой функции совпадает со значением, возвращаемым в параметре тоска.</span><span class="sxs-lookup"><span data-stu-id="4bc67-126">The return value for this function is the same value returned in the pOut parameter.</span></span> <span data-ttu-id="4bc67-127">Таким образом, функция D3DXMatrixPerspectiveFovRH может использоваться в качестве параметра для другой функции.</span><span class="sxs-lookup"><span data-stu-id="4bc67-127">In this way, the D3DXMatrixPerspectiveFovRH function can be used as a parameter for another function.</span></span>

<span data-ttu-id="4bc67-128">Эта функция вычислит возвращаемую матрицу, как показано ниже.</span><span class="sxs-lookup"><span data-stu-id="4bc67-128">This function computes the returned matrix as shown.</span></span>


```
xScale     0          0              0
0        yScale       0              0
0          0      zf/(zn-zf)        -1
0          0      zn*zf/(zn-zf)      0
where:
yScale = cot(fovY/2)
    
xScale = yScale / aspect ratio
```



## <a name="requirements"></a><span data-ttu-id="4bc67-129">Требования</span><span class="sxs-lookup"><span data-stu-id="4bc67-129">Requirements</span></span>



| <span data-ttu-id="4bc67-130">Требование</span><span class="sxs-lookup"><span data-stu-id="4bc67-130">Requirement</span></span> | <span data-ttu-id="4bc67-131">Значение</span><span class="sxs-lookup"><span data-stu-id="4bc67-131">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="4bc67-132">Header</span><span class="sxs-lookup"><span data-stu-id="4bc67-132">Header</span></span><br/>  | <dl> <span data-ttu-id="4bc67-133"><dt>D3DX10Math. h</dt></span><span class="sxs-lookup"><span data-stu-id="4bc67-133"><dt>D3DX10Math.h</dt></span></span> </dl> |
| <span data-ttu-id="4bc67-134">Библиотека</span><span class="sxs-lookup"><span data-stu-id="4bc67-134">Library</span></span><br/> | <dl> <span data-ttu-id="4bc67-135"><dt>D3DX10. lib</dt></span><span class="sxs-lookup"><span data-stu-id="4bc67-135"><dt>D3DX10.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="4bc67-136">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="4bc67-136">See also</span></span>

<dl> <dt>

[<span data-ttu-id="4bc67-137">Математические функции</span><span class="sxs-lookup"><span data-stu-id="4bc67-137">Math Functions</span></span>](d3d10-graphics-reference-d3dx10-functions-math.md)
</dt> </dl>

 

 
