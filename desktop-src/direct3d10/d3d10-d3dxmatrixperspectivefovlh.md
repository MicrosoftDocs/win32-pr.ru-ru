---
description: Функция D3DXMatrixPerspectiveFovLH (D3DX10Math. h) — формирует матрицу левой проекции перспективы на основе поля представления.
ms.assetid: 35ee12d6-0a58-4b00-ac8f-82f82215f02e
title: Функция D3DXMatrixPerspectiveFovLH (D3DX10Math. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXMatrixPerspectiveFovLH
api_type:
- LibDef
api_location:
- D3DX10.lib
- D3DX10.dll
ms.openlocfilehash: cea1bec170664993332b1cde1de375c416209209
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2021
ms.locfileid: "108113092"
---
# <a name="d3dxmatrixperspectivefovlh-function-d3dx10mathh"></a><span data-ttu-id="cc3bd-103">Функция D3DXMatrixPerspectiveFovLH (D3DX10Math. h)</span><span class="sxs-lookup"><span data-stu-id="cc3bd-103">D3DXMatrixPerspectiveFovLH function (D3DX10Math.h)</span></span>

<span data-ttu-id="cc3bd-104">Строит левовинтовую матрицу перспективной проекции на основании поля зрения.</span><span class="sxs-lookup"><span data-stu-id="cc3bd-104">Builds a left-handed perspective projection matrix based on a field of view.</span></span>

## <a name="syntax"></a><span data-ttu-id="cc3bd-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="cc3bd-105">Syntax</span></span>


```C++
D3DXMATRIX* D3DXMatrixPerspectiveFovLH(
  _Inout_ D3DXMATRIX *pOut,
  _In_    FLOAT      fovy,
  _In_    FLOAT      Aspect,
  _In_    FLOAT      zn,
  _In_    FLOAT      zf
);
```



## <a name="parameters"></a><span data-ttu-id="cc3bd-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="cc3bd-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="cc3bd-107">*тоска* \[ в, out\]</span><span class="sxs-lookup"><span data-stu-id="cc3bd-107">*pOut* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="cc3bd-108">Тип: **[ **D3DXMATRIX**](../direct3d9/d3dxmatrix.md)\***</span><span class="sxs-lookup"><span data-stu-id="cc3bd-108">Type: **[**D3DXMATRIX**](../direct3d9/d3dxmatrix.md)\***</span></span>

<span data-ttu-id="cc3bd-109">Указатель на структуру [**D3DXMATRIX**](d3d10-d3dxmatrix.md) , которая является результатом операции.</span><span class="sxs-lookup"><span data-stu-id="cc3bd-109">Pointer to the [**D3DXMATRIX**](d3d10-d3dxmatrix.md) structure that is the result of the operation.</span></span>

</dd> <dt>

<span data-ttu-id="cc3bd-110">*ФОВИ* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="cc3bd-110">*fovy* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="cc3bd-111">Тип: **[ **float**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="cc3bd-111">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="cc3bd-112">Поле представления в направлении y (в радианах).</span><span class="sxs-lookup"><span data-stu-id="cc3bd-112">Field of view in the y direction, in radians.</span></span>

</dd> <dt>

<span data-ttu-id="cc3bd-113">*Аспект* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="cc3bd-113">*Aspect* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="cc3bd-114">Тип: **[ **float**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="cc3bd-114">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="cc3bd-115">Пропорции, определенные как ширина представления, деленная на высоту.</span><span class="sxs-lookup"><span data-stu-id="cc3bd-115">Aspect ratio, defined as view space width divided by height.</span></span>

</dd> <dt>

<span data-ttu-id="cc3bd-116">*ЗН* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="cc3bd-116">*zn* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="cc3bd-117">Тип: **[ **float**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="cc3bd-117">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="cc3bd-118">Z-значение ближней плоскости просмотра.</span><span class="sxs-lookup"><span data-stu-id="cc3bd-118">Z-value of the near view-plane.</span></span>

</dd> <dt>

<span data-ttu-id="cc3bd-119">*ЗФ* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="cc3bd-119">*zf* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="cc3bd-120">Тип: **[ **float**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="cc3bd-120">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="cc3bd-121">Z-значение дальней плоскости просмотра.</span><span class="sxs-lookup"><span data-stu-id="cc3bd-121">Z-value of the far view-plane.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="cc3bd-122">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="cc3bd-122">Return value</span></span>

<span data-ttu-id="cc3bd-123">Тип: **[ **D3DXMATRIX**](../direct3d9/d3dxmatrix.md)\***</span><span class="sxs-lookup"><span data-stu-id="cc3bd-123">Type: **[**D3DXMATRIX**](../direct3d9/d3dxmatrix.md)\***</span></span>

<span data-ttu-id="cc3bd-124">Указатель на структуру D3DXMATRIX, которая является матрицей перспективной проекции влево.</span><span class="sxs-lookup"><span data-stu-id="cc3bd-124">Pointer to a D3DXMATRIX structure that is a left-handed perspective projection matrix.</span></span>

## <a name="remarks"></a><span data-ttu-id="cc3bd-125">Remarks</span><span class="sxs-lookup"><span data-stu-id="cc3bd-125">Remarks</span></span>

<span data-ttu-id="cc3bd-126">Возвращаемое значение для этой функции совпадает со значением, возвращаемым в параметре тоска.</span><span class="sxs-lookup"><span data-stu-id="cc3bd-126">The return value for this function is the same value returned in the pOut parameter.</span></span> <span data-ttu-id="cc3bd-127">Таким образом, функция D3DXMatrixPerspectiveFovLH может использоваться в качестве параметра для другой функции.</span><span class="sxs-lookup"><span data-stu-id="cc3bd-127">In this way, the D3DXMatrixPerspectiveFovLH function can be used as a parameter for another function.</span></span>

<span data-ttu-id="cc3bd-128">Эта функция вычислит возвращаемую матрицу, как показано ниже.</span><span class="sxs-lookup"><span data-stu-id="cc3bd-128">This function computes the returned matrix as shown:</span></span>


```
xScale     0          0               0
0        yScale       0               0
0          0       zf/(zf-zn)         1
0          0       -zn*zf/(zf-zn)     0
where:
yScale = cot(fovY/2)

xScale = yScale / aspect ratio
```



## <a name="requirements"></a><span data-ttu-id="cc3bd-129">Требования</span><span class="sxs-lookup"><span data-stu-id="cc3bd-129">Requirements</span></span>



| <span data-ttu-id="cc3bd-130">Требование</span><span class="sxs-lookup"><span data-stu-id="cc3bd-130">Requirement</span></span> | <span data-ttu-id="cc3bd-131">Значение</span><span class="sxs-lookup"><span data-stu-id="cc3bd-131">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="cc3bd-132">Header</span><span class="sxs-lookup"><span data-stu-id="cc3bd-132">Header</span></span><br/>  | <dl> <span data-ttu-id="cc3bd-133"><dt>D3DX10Math. h</dt></span><span class="sxs-lookup"><span data-stu-id="cc3bd-133"><dt>D3DX10Math.h</dt></span></span> </dl> |
| <span data-ttu-id="cc3bd-134">Библиотека</span><span class="sxs-lookup"><span data-stu-id="cc3bd-134">Library</span></span><br/> | <dl> <span data-ttu-id="cc3bd-135"><dt>D3DX10. lib</dt></span><span class="sxs-lookup"><span data-stu-id="cc3bd-135"><dt>D3DX10.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="cc3bd-136">См. также</span><span class="sxs-lookup"><span data-stu-id="cc3bd-136">See also</span></span>

<dl> <dt>

[<span data-ttu-id="cc3bd-137">Математические функции</span><span class="sxs-lookup"><span data-stu-id="cc3bd-137">Math Functions</span></span>](d3d10-graphics-reference-d3dx10-functions-math.md)
</dt> </dl>

 

 
