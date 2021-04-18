---
description: Возвращает определитель матрицы.
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
ms.openlocfilehash: 11b1092427b12c33d8c34c9f1bbd5e09cf1ccf2d
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/15/2021
ms.locfileid: "105713923"
---
# <a name="d3dxmatrixdeterminant-function-d3dx10mathh"></a><span data-ttu-id="c0172-103">Функция D3DXMatrixDeterminant (D3DX10Math. h)</span><span class="sxs-lookup"><span data-stu-id="c0172-103">D3DXMatrixDeterminant function (D3DX10Math.h)</span></span>

<span data-ttu-id="c0172-104">Возвращает определитель матрицы.</span><span class="sxs-lookup"><span data-stu-id="c0172-104">Returns the determinant of a matrix.</span></span>

## <a name="syntax"></a><span data-ttu-id="c0172-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="c0172-105">Syntax</span></span>


```C++
FLOAT D3DXMatrixDeterminant(
  _In_ const D3DXMATRIX *pM
);
```



## <a name="parameters"></a><span data-ttu-id="c0172-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="c0172-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="c0172-107">*PM* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="c0172-107">*pM* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="c0172-108">Тип: **const [**D3DXMATRIX**](../direct3d9/d3dxmatrix.md) \***</span><span class="sxs-lookup"><span data-stu-id="c0172-108">Type: **const [**D3DXMATRIX**](../direct3d9/d3dxmatrix.md)\***</span></span>

<span data-ttu-id="c0172-109">Указатель на исходную структуру D3DXMATRIX.</span><span class="sxs-lookup"><span data-stu-id="c0172-109">Pointer to the source D3DXMATRIX structure.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="c0172-110">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="c0172-110">Return value</span></span>

<span data-ttu-id="c0172-111">Тип: **[ **float**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="c0172-111">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="c0172-112">Возвращает определитель матрицы.</span><span class="sxs-lookup"><span data-stu-id="c0172-112">Returns the determinant of the matrix.</span></span>

## <a name="requirements"></a><span data-ttu-id="c0172-113">Требования</span><span class="sxs-lookup"><span data-stu-id="c0172-113">Requirements</span></span>



| <span data-ttu-id="c0172-114">Требование</span><span class="sxs-lookup"><span data-stu-id="c0172-114">Requirement</span></span> | <span data-ttu-id="c0172-115">Значение</span><span class="sxs-lookup"><span data-stu-id="c0172-115">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="c0172-116">Header</span><span class="sxs-lookup"><span data-stu-id="c0172-116">Header</span></span><br/>  | <dl> <span data-ttu-id="c0172-117"><dt>D3DX10Math. h</dt></span><span class="sxs-lookup"><span data-stu-id="c0172-117"><dt>D3DX10Math.h</dt></span></span> </dl> |
| <span data-ttu-id="c0172-118">Библиотека</span><span class="sxs-lookup"><span data-stu-id="c0172-118">Library</span></span><br/> | <dl> <span data-ttu-id="c0172-119"><dt>D3DX10. lib</dt></span><span class="sxs-lookup"><span data-stu-id="c0172-119"><dt>D3DX10.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="c0172-120">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="c0172-120">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c0172-121">Математические функции</span><span class="sxs-lookup"><span data-stu-id="c0172-121">Math Functions</span></span>](d3d10-graphics-reference-d3dx10-functions-math.md)
</dt> </dl>

 

 
