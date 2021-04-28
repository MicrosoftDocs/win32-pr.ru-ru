---
description: Функция D3DXMatrixMultiply (D3DX10Math. h) — Определяет произведение двух матриц.
ms.assetid: d15cd680-0e19-4353-9eee-73933663960e
title: Функция D3DXMatrixMultiply (D3DX10Math. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXMatrixMultiply
api_type:
- LibDef
api_location:
- D3DX10.lib
- D3DX10.dll
ms.openlocfilehash: 89e103d441648643be0176ca34f72f6175c11213
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2021
ms.locfileid: "108113132"
---
# <a name="d3dxmatrixmultiply-function-d3dx10mathh"></a><span data-ttu-id="50279-103">Функция D3DXMatrixMultiply (D3DX10Math. h)</span><span class="sxs-lookup"><span data-stu-id="50279-103">D3DXMatrixMultiply function (D3DX10Math.h)</span></span>

<span data-ttu-id="50279-104">Определяет произведение двух матриц.</span><span class="sxs-lookup"><span data-stu-id="50279-104">Determines the product of two matrices.</span></span>

## <a name="syntax"></a><span data-ttu-id="50279-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="50279-105">Syntax</span></span>


```C++
D3DXMATRIX* D3DXMatrixMultiply(
  _Inout_       D3DXMATRIX *pOut,
  _In_    const D3DXMATRIX *pM1,
  _In_    const D3DXMATRIX *pM2
);
```



## <a name="parameters"></a><span data-ttu-id="50279-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="50279-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="50279-107">*тоска* \[ в, out\]</span><span class="sxs-lookup"><span data-stu-id="50279-107">*pOut* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="50279-108">Тип: **[ **D3DXMATRIX**](../direct3d9/d3dxmatrix.md)\***</span><span class="sxs-lookup"><span data-stu-id="50279-108">Type: **[**D3DXMATRIX**](../direct3d9/d3dxmatrix.md)\***</span></span>

<span data-ttu-id="50279-109">Указатель на структуру [**D3DXMATRIX**](d3d10-d3dxmatrix.md) , которая является результатом операции.</span><span class="sxs-lookup"><span data-stu-id="50279-109">Pointer to the [**D3DXMATRIX**](d3d10-d3dxmatrix.md) structure that is the result of the operation.</span></span>

</dd> <dt>

<span data-ttu-id="50279-110">*pM1* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="50279-110">*pM1* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="50279-111">Тип: **const [**D3DXMATRIX**](../direct3d9/d3dxmatrix.md) \***</span><span class="sxs-lookup"><span data-stu-id="50279-111">Type: **const [**D3DXMATRIX**](../direct3d9/d3dxmatrix.md)\***</span></span>

<span data-ttu-id="50279-112">Указатель на исходную структуру D3DXMATRIX (с левой стороны).</span><span class="sxs-lookup"><span data-stu-id="50279-112">Pointer to a source D3DXMATRIX structure (left hand side).</span></span>

</dd> <dt>

<span data-ttu-id="50279-113">*pM2* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="50279-113">*pM2* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="50279-114">Тип: **const [**D3DXMATRIX**](../direct3d9/d3dxmatrix.md) \***</span><span class="sxs-lookup"><span data-stu-id="50279-114">Type: **const [**D3DXMATRIX**](../direct3d9/d3dxmatrix.md)\***</span></span>

<span data-ttu-id="50279-115">Указатель на исходную структуру D3DXMATRIX (правую часть).</span><span class="sxs-lookup"><span data-stu-id="50279-115">Pointer to a source D3DXMATRIX structure (right hand side).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="50279-116">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="50279-116">Return value</span></span>

<span data-ttu-id="50279-117">Тип: **[ **D3DXMATRIX**](../direct3d9/d3dxmatrix.md)\***</span><span class="sxs-lookup"><span data-stu-id="50279-117">Type: **[**D3DXMATRIX**](../direct3d9/d3dxmatrix.md)\***</span></span>

<span data-ttu-id="50279-118">Указатель на структуру D3DXMATRIX, которая является произведением двух матриц.</span><span class="sxs-lookup"><span data-stu-id="50279-118">Pointer to a D3DXMATRIX structure that is the product of two matrices.</span></span>

## <a name="remarks"></a><span data-ttu-id="50279-119">Remarks</span><span class="sxs-lookup"><span data-stu-id="50279-119">Remarks</span></span>

<span data-ttu-id="50279-120">Результат представляет преобразование M1, за которым следует преобразование m2 (out = M1 \* m2).</span><span class="sxs-lookup"><span data-stu-id="50279-120">The result represents the transformation M1 followed by the transformation M2 (Out = M1 \* M2).</span></span>

<span data-ttu-id="50279-121">Возвращаемое значение для этой функции совпадает со значением, возвращаемым в параметре тоска.</span><span class="sxs-lookup"><span data-stu-id="50279-121">The return value for this function is the same value returned in the pOut parameter.</span></span> <span data-ttu-id="50279-122">Таким образом, функция D3DXMatrixMultiply может использоваться в качестве параметра для другой функции.</span><span class="sxs-lookup"><span data-stu-id="50279-122">In this way, the D3DXMatrixMultiply function can be used as a parameter for another function.</span></span>

## <a name="requirements"></a><span data-ttu-id="50279-123">Требования</span><span class="sxs-lookup"><span data-stu-id="50279-123">Requirements</span></span>



| <span data-ttu-id="50279-124">Требование</span><span class="sxs-lookup"><span data-stu-id="50279-124">Requirement</span></span> | <span data-ttu-id="50279-125">Значение</span><span class="sxs-lookup"><span data-stu-id="50279-125">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="50279-126">Header</span><span class="sxs-lookup"><span data-stu-id="50279-126">Header</span></span><br/>  | <dl> <span data-ttu-id="50279-127"><dt>D3DX10Math. h</dt></span><span class="sxs-lookup"><span data-stu-id="50279-127"><dt>D3DX10Math.h</dt></span></span> </dl> |
| <span data-ttu-id="50279-128">Библиотека</span><span class="sxs-lookup"><span data-stu-id="50279-128">Library</span></span><br/> | <dl> <span data-ttu-id="50279-129"><dt>D3DX10. lib</dt></span><span class="sxs-lookup"><span data-stu-id="50279-129"><dt>D3DX10.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="50279-130">См. также</span><span class="sxs-lookup"><span data-stu-id="50279-130">See also</span></span>

<dl> <dt>

[<span data-ttu-id="50279-131">Математические функции</span><span class="sxs-lookup"><span data-stu-id="50279-131">Math Functions</span></span>](d3d10-graphics-reference-d3dx10-functions-math.md)
</dt> </dl>

 

 
