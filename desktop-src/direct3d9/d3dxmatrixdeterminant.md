---
description: Возвращает определитель матрицы.
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
ms.openlocfilehash: 53d90d70e75ba4bb92dbed3abe7ee06eae1ae6e4
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/15/2021
ms.locfileid: "104354210"
---
# <a name="d3dxmatrixdeterminant-function-d3dx9mathh"></a><span data-ttu-id="f641a-103">Функция D3DXMatrixDeterminant (D3dx9math. h)</span><span class="sxs-lookup"><span data-stu-id="f641a-103">D3DXMatrixDeterminant function (D3dx9math.h)</span></span>

<span data-ttu-id="f641a-104">Возвращает определитель матрицы.</span><span class="sxs-lookup"><span data-stu-id="f641a-104">Returns the determinant of a matrix.</span></span>

## <a name="syntax"></a><span data-ttu-id="f641a-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="f641a-105">Syntax</span></span>


```C++
FLOAT D3DXMatrixDeterminant(
  _In_ const D3DXMATRIX *pM
);
```



## <a name="parameters"></a><span data-ttu-id="f641a-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="f641a-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="f641a-107">*PM* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="f641a-107">*pM* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="f641a-108">Тип: **const [**D3DXMATRIX**](d3dxmatrix.md) \***</span><span class="sxs-lookup"><span data-stu-id="f641a-108">Type: **const [**D3DXMATRIX**](d3dxmatrix.md)\***</span></span>

<span data-ttu-id="f641a-109">Указатель на исходную структуру [**D3DXMATRIX**](d3dxmatrix.md) .</span><span class="sxs-lookup"><span data-stu-id="f641a-109">Pointer to the source [**D3DXMATRIX**](d3dxmatrix.md) structure.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="f641a-110">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="f641a-110">Return value</span></span>

<span data-ttu-id="f641a-111">Тип: **[ **float**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="f641a-111">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="f641a-112">Возвращает определитель матрицы.</span><span class="sxs-lookup"><span data-stu-id="f641a-112">Returns the determinant of the matrix.</span></span>

## <a name="requirements"></a><span data-ttu-id="f641a-113">Требования</span><span class="sxs-lookup"><span data-stu-id="f641a-113">Requirements</span></span>



| <span data-ttu-id="f641a-114">Требование</span><span class="sxs-lookup"><span data-stu-id="f641a-114">Requirement</span></span> | <span data-ttu-id="f641a-115">Значение</span><span class="sxs-lookup"><span data-stu-id="f641a-115">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="f641a-116">Header</span><span class="sxs-lookup"><span data-stu-id="f641a-116">Header</span></span><br/>  | <dl> <span data-ttu-id="f641a-117"><dt>D3dx9math. h</dt></span><span class="sxs-lookup"><span data-stu-id="f641a-117"><dt>D3dx9math.h</dt></span></span> </dl> |
| <span data-ttu-id="f641a-118">Библиотека</span><span class="sxs-lookup"><span data-stu-id="f641a-118">Library</span></span><br/> | <dl> <span data-ttu-id="f641a-119"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="f641a-119"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="f641a-120">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="f641a-120">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f641a-121">Математические функции</span><span class="sxs-lookup"><span data-stu-id="f641a-121">Math Functions</span></span>](dx9-graphics-reference-d3dx-functions-math.md)
</dt> </dl>

 

 
