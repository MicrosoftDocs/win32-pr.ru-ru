---
description: Функция D3DXMatrixDeterminant (D3DX10Math. h) — Возвращает определитель матрицы.
ms.assetid: b0155c91-1554-42ef-b219-c6cdd2a905b5
title: Функция D3DXMatrixDeterminant (D3DX10Math. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXMatrixDeterminant
api_type:
- LibDef
api_location:
- D3DX10.lib
- D3DX10.dll
ms.openlocfilehash: 894db23a3079c1344c97cab00642cbbc0953450d
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2021
ms.locfileid: "108103462"
---
# <a name="d3dxmatrixdeterminant-function-d3dx10mathh"></a><span data-ttu-id="e3b1e-103">Функция D3DXMatrixDeterminant (D3DX10Math. h)</span><span class="sxs-lookup"><span data-stu-id="e3b1e-103">D3DXMatrixDeterminant function (D3DX10Math.h)</span></span>

<span data-ttu-id="e3b1e-104">Возвращает определитель матрицы.</span><span class="sxs-lookup"><span data-stu-id="e3b1e-104">Returns the determinant of a matrix.</span></span>

## <a name="syntax"></a><span data-ttu-id="e3b1e-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="e3b1e-105">Syntax</span></span>


```C++
FLOAT D3DXMatrixDeterminant(
  _In_ const D3DXMATRIX *pM
);
```



## <a name="parameters"></a><span data-ttu-id="e3b1e-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="e3b1e-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="e3b1e-107">*PM* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="e3b1e-107">*pM* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="e3b1e-108">Тип: **const [**D3DXMATRIX**](../direct3d9/d3dxmatrix.md) \***</span><span class="sxs-lookup"><span data-stu-id="e3b1e-108">Type: **const [**D3DXMATRIX**](../direct3d9/d3dxmatrix.md)\***</span></span>

<span data-ttu-id="e3b1e-109">Указатель на исходную структуру D3DXMATRIX.</span><span class="sxs-lookup"><span data-stu-id="e3b1e-109">Pointer to the source D3DXMATRIX structure.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="e3b1e-110">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="e3b1e-110">Return value</span></span>

<span data-ttu-id="e3b1e-111">Тип: **[ **float**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="e3b1e-111">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="e3b1e-112">Возвращает определитель матрицы.</span><span class="sxs-lookup"><span data-stu-id="e3b1e-112">Returns the determinant of the matrix.</span></span>

## <a name="requirements"></a><span data-ttu-id="e3b1e-113">Требования</span><span class="sxs-lookup"><span data-stu-id="e3b1e-113">Requirements</span></span>



| <span data-ttu-id="e3b1e-114">Требование</span><span class="sxs-lookup"><span data-stu-id="e3b1e-114">Requirement</span></span> | <span data-ttu-id="e3b1e-115">Значение</span><span class="sxs-lookup"><span data-stu-id="e3b1e-115">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="e3b1e-116">Header</span><span class="sxs-lookup"><span data-stu-id="e3b1e-116">Header</span></span><br/>  | <dl> <span data-ttu-id="e3b1e-117"><dt>D3DX10Math. h</dt></span><span class="sxs-lookup"><span data-stu-id="e3b1e-117"><dt>D3DX10Math.h</dt></span></span> </dl> |
| <span data-ttu-id="e3b1e-118">Библиотека</span><span class="sxs-lookup"><span data-stu-id="e3b1e-118">Library</span></span><br/> | <dl> <span data-ttu-id="e3b1e-119"><dt>D3DX10. lib</dt></span><span class="sxs-lookup"><span data-stu-id="e3b1e-119"><dt>D3DX10.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="e3b1e-120">См. также</span><span class="sxs-lookup"><span data-stu-id="e3b1e-120">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e3b1e-121">Математические функции</span><span class="sxs-lookup"><span data-stu-id="e3b1e-121">Math Functions</span></span>](d3d10-graphics-reference-d3dx10-functions-math.md)
</dt> </dl>

 

 
