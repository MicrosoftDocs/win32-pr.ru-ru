---
description: Функция D3DXMatrixDeterminant (D3dx9math. h) — Возвращает определитель матрицы.
ms.assetid: 711ba616-4c90-41d1-b9d5-0893b3e47284
title: Функция D3DXMatrixDeterminant (D3dx9math. h)
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
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 8d54651e11f1b3de02803d9ea123ca7eff24d7a5
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2021
ms.locfileid: "108098172"
---
# <a name="d3dxmatrixdeterminant-function-d3dx9mathh"></a><span data-ttu-id="d8d25-103">Функция D3DXMatrixDeterminant (D3dx9math. h)</span><span class="sxs-lookup"><span data-stu-id="d8d25-103">D3DXMatrixDeterminant function (D3dx9math.h)</span></span>

<span data-ttu-id="d8d25-104">Возвращает определитель матрицы.</span><span class="sxs-lookup"><span data-stu-id="d8d25-104">Returns the determinant of a matrix.</span></span>

## <a name="syntax"></a><span data-ttu-id="d8d25-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="d8d25-105">Syntax</span></span>


```C++
FLOAT D3DXMatrixDeterminant(
  _In_ const D3DXMATRIX *pM
);
```



## <a name="parameters"></a><span data-ttu-id="d8d25-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="d8d25-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="d8d25-107">*PM* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="d8d25-107">*pM* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="d8d25-108">Тип: **const [**D3DXMATRIX**](d3dxmatrix.md) \***</span><span class="sxs-lookup"><span data-stu-id="d8d25-108">Type: **const [**D3DXMATRIX**](d3dxmatrix.md)\***</span></span>

<span data-ttu-id="d8d25-109">Указатель на исходную структуру [**D3DXMATRIX**](d3dxmatrix.md) .</span><span class="sxs-lookup"><span data-stu-id="d8d25-109">Pointer to the source [**D3DXMATRIX**](d3dxmatrix.md) structure.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="d8d25-110">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="d8d25-110">Return value</span></span>

<span data-ttu-id="d8d25-111">Тип: **[ **float**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="d8d25-111">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="d8d25-112">Возвращает определитель матрицы.</span><span class="sxs-lookup"><span data-stu-id="d8d25-112">Returns the determinant of the matrix.</span></span>

## <a name="requirements"></a><span data-ttu-id="d8d25-113">Требования</span><span class="sxs-lookup"><span data-stu-id="d8d25-113">Requirements</span></span>



| <span data-ttu-id="d8d25-114">Требование</span><span class="sxs-lookup"><span data-stu-id="d8d25-114">Requirement</span></span> | <span data-ttu-id="d8d25-115">Значение</span><span class="sxs-lookup"><span data-stu-id="d8d25-115">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="d8d25-116">Header</span><span class="sxs-lookup"><span data-stu-id="d8d25-116">Header</span></span><br/>  | <dl> <span data-ttu-id="d8d25-117"><dt>D3dx9math. h</dt></span><span class="sxs-lookup"><span data-stu-id="d8d25-117"><dt>D3dx9math.h</dt></span></span> </dl> |
| <span data-ttu-id="d8d25-118">Библиотека</span><span class="sxs-lookup"><span data-stu-id="d8d25-118">Library</span></span><br/> | <dl> <span data-ttu-id="d8d25-119"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="d8d25-119"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="d8d25-120">См. также</span><span class="sxs-lookup"><span data-stu-id="d8d25-120">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d8d25-121">Математические функции</span><span class="sxs-lookup"><span data-stu-id="d8d25-121">Math Functions</span></span>](dx9-graphics-reference-d3dx-functions-math.md)
</dt> </dl>

 

 
