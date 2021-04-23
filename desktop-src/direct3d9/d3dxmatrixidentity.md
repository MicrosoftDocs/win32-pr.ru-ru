---
description: Создает матрицу идентификаторов.
ms.assetid: 0dd6d4fb-284c-4d01-9a85-63aa08e71723
title: Функция D3DXMatrixIdentity (D3dx9math. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXMatrixIdentity
api_type:
- LibDef
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 10dffa12a379754006ca65d1239be96632a68b93
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/15/2021
ms.locfileid: "104000310"
---
# <a name="d3dxmatrixidentity-function"></a><span data-ttu-id="b6370-103">Функция D3DXMatrixIdentity</span><span class="sxs-lookup"><span data-stu-id="b6370-103">D3DXMatrixIdentity function</span></span>

<span data-ttu-id="b6370-104">Создает матрицу идентификаторов.</span><span class="sxs-lookup"><span data-stu-id="b6370-104">Creates an identity matrix.</span></span>

## <a name="syntax"></a><span data-ttu-id="b6370-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="b6370-105">Syntax</span></span>


```C++
D3DXMATRIX* D3DXMatrixIdentity(
  _Inout_ D3DXMATRIX *pOut
);
```



## <a name="parameters"></a><span data-ttu-id="b6370-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="b6370-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="b6370-107">*тоска* \[ в, out\]</span><span class="sxs-lookup"><span data-stu-id="b6370-107">*pOut* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="b6370-108">Тип: **[ **D3DXMATRIX**](d3dxmatrix.md)\***</span><span class="sxs-lookup"><span data-stu-id="b6370-108">Type: **[**D3DXMATRIX**](d3dxmatrix.md)\***</span></span>

<span data-ttu-id="b6370-109">Указатель на структуру [**D3DXMATRIX**](d3dxmatrix.md) , которая является результатом операции.</span><span class="sxs-lookup"><span data-stu-id="b6370-109">Pointer to the [**D3DXMATRIX**](d3dxmatrix.md) structure that is the result of the operation.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="b6370-110">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="b6370-110">Return value</span></span>

<span data-ttu-id="b6370-111">Тип: **[ **D3DXMATRIX**](d3dxmatrix.md)\***</span><span class="sxs-lookup"><span data-stu-id="b6370-111">Type: **[**D3DXMATRIX**](d3dxmatrix.md)\***</span></span>

<span data-ttu-id="b6370-112">Указатель на структуру [**D3DXMATRIX**](d3dxmatrix.md) , которая является матрицей идентификаторов.</span><span class="sxs-lookup"><span data-stu-id="b6370-112">Pointer to a [**D3DXMATRIX**](d3dxmatrix.md) structure that is the identity matrix.</span></span>

## <a name="remarks"></a><span data-ttu-id="b6370-113">Комментарии</span><span class="sxs-lookup"><span data-stu-id="b6370-113">Remarks</span></span>

<span data-ttu-id="b6370-114">Матрица идентификаторов — это матрица, в которой все коэффициенты равны 0, за исключением \[ 1, 1 \] \[ 2, 2 \] \[ 3, 3 \] \[ 4 и 4 \] коэффициентов, для которых задано значение 1.</span><span class="sxs-lookup"><span data-stu-id="b6370-114">The identity matrix is a matrix in which all coefficients are 0 except the \[1,1\]\[2,2\]\[3,3\]\[4,4\] coefficients, which are set to 1.</span></span> <span data-ttu-id="b6370-115">Матрица идентификации является особой в том, что при применении к вершинам они не меняются.</span><span class="sxs-lookup"><span data-stu-id="b6370-115">The identity matrix is special in that when it is applied to vertices, they are unchanged.</span></span> <span data-ttu-id="b6370-116">Матрица идентификации используется в качестве начальной точки для матриц, которые будут изменять значения вершин для создания поворотов, переводов и других преобразований, которые могут быть представлены матрицей 4 X4.</span><span class="sxs-lookup"><span data-stu-id="b6370-116">The identity matrix is used as the starting point for matrices that will modify vertex values to create rotations, translations, and any other transformations that can be represented by a 4 x4 matrix.</span></span>

<span data-ttu-id="b6370-117">Возвращаемое значение для этой функции совпадает со значением, возвращаемым в параметре *тоска* .</span><span class="sxs-lookup"><span data-stu-id="b6370-117">The return value for this function is the same value returned in the *pOut* parameter.</span></span> <span data-ttu-id="b6370-118">Таким образом, функция **D3DXMatrixIdentity** может использоваться в качестве параметра для другой функции.</span><span class="sxs-lookup"><span data-stu-id="b6370-118">In this way, the **D3DXMatrixIdentity** function can be used as a parameter for another function.</span></span>

## <a name="requirements"></a><span data-ttu-id="b6370-119">Требования</span><span class="sxs-lookup"><span data-stu-id="b6370-119">Requirements</span></span>



| <span data-ttu-id="b6370-120">Требование</span><span class="sxs-lookup"><span data-stu-id="b6370-120">Requirement</span></span> | <span data-ttu-id="b6370-121">Значение</span><span class="sxs-lookup"><span data-stu-id="b6370-121">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="b6370-122">Header</span><span class="sxs-lookup"><span data-stu-id="b6370-122">Header</span></span><br/>  | <dl> <span data-ttu-id="b6370-123"><dt>D3dx9math. h</dt></span><span class="sxs-lookup"><span data-stu-id="b6370-123"><dt>D3dx9math.h</dt></span></span> </dl> |
| <span data-ttu-id="b6370-124">Библиотека</span><span class="sxs-lookup"><span data-stu-id="b6370-124">Library</span></span><br/> | <dl> <span data-ttu-id="b6370-125"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="b6370-125"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="b6370-126">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="b6370-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b6370-127">Математические функции</span><span class="sxs-lookup"><span data-stu-id="b6370-127">Math Functions</span></span>](dx9-graphics-reference-d3dx-functions-math.md)
</dt> <dt>

[<span data-ttu-id="b6370-128">**D3DXMatrixIsIdentity**</span><span class="sxs-lookup"><span data-stu-id="b6370-128">**D3DXMatrixIsIdentity**</span></span>](d3dxmatrixisidentity.md)
</dt> </dl>

 

 




