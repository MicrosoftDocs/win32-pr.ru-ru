---
description: Создает матрицу с использованием указанных смещений.
ms.assetid: 1cb713d5-b994-4496-a506-89451be09fb2
title: Функция D3DXMatrixTranslation (D3dx9math. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXMatrixTranslation
api_type:
- LibDef
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 9c74d56eaa0e41bc6ce9060ff291885a8a5c05a5
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/15/2021
ms.locfileid: "104354783"
---
# <a name="d3dxmatrixtranslation-function-d3dx9mathh"></a><span data-ttu-id="0052d-103">Функция D3DXMatrixTranslation (D3dx9math. h)</span><span class="sxs-lookup"><span data-stu-id="0052d-103">D3DXMatrixTranslation function (D3dx9math.h)</span></span>

<span data-ttu-id="0052d-104">Создает матрицу с использованием указанных смещений.</span><span class="sxs-lookup"><span data-stu-id="0052d-104">Builds a matrix using the specified offsets.</span></span>

## <a name="syntax"></a><span data-ttu-id="0052d-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="0052d-105">Syntax</span></span>


```C++
D3DXMATRIX* D3DXMatrixTranslation(
  _Inout_ D3DXMATRIX *pOut,
  _In_    FLOAT      x,
  _In_    FLOAT      y,
  _In_    FLOAT      z
);
```



## <a name="parameters"></a><span data-ttu-id="0052d-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="0052d-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="0052d-107">*тоска* \[ в, out\]</span><span class="sxs-lookup"><span data-stu-id="0052d-107">*pOut* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="0052d-108">Тип: **[ **D3DXMATRIX**](d3dxmatrix.md)\***</span><span class="sxs-lookup"><span data-stu-id="0052d-108">Type: **[**D3DXMATRIX**](d3dxmatrix.md)\***</span></span>

<span data-ttu-id="0052d-109">Указатель на структуру [**D3DXMATRIX**](d3dxmatrix.md) , которая является результатом операции.</span><span class="sxs-lookup"><span data-stu-id="0052d-109">Pointer to the [**D3DXMATRIX**](d3dxmatrix.md) structure that is the result of the operation.</span></span>

</dd> <dt>

<span data-ttu-id="0052d-110">*x* \[ в\]</span><span class="sxs-lookup"><span data-stu-id="0052d-110">*x* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="0052d-111">Тип: **[ **float**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="0052d-111">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="0052d-112">Смещение координаты X.</span><span class="sxs-lookup"><span data-stu-id="0052d-112">X-coordinate offset.</span></span>

</dd> <dt>

<span data-ttu-id="0052d-113">*y* \[ в\]</span><span class="sxs-lookup"><span data-stu-id="0052d-113">*y* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="0052d-114">Тип: **[ **float**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="0052d-114">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="0052d-115">Смещение координаты Y.</span><span class="sxs-lookup"><span data-stu-id="0052d-115">Y-coordinate offset.</span></span>

</dd> <dt>

<span data-ttu-id="0052d-116">*z* \[ в\]</span><span class="sxs-lookup"><span data-stu-id="0052d-116">*z* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="0052d-117">Тип: **[ **float**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="0052d-117">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="0052d-118">Смещение координаты Z.</span><span class="sxs-lookup"><span data-stu-id="0052d-118">Z-coordinate offset.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="0052d-119">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="0052d-119">Return value</span></span>

<span data-ttu-id="0052d-120">Тип: **[ **D3DXMATRIX**](d3dxmatrix.md)\***</span><span class="sxs-lookup"><span data-stu-id="0052d-120">Type: **[**D3DXMATRIX**](d3dxmatrix.md)\***</span></span>

<span data-ttu-id="0052d-121">Указатель на структуру [**D3DXMATRIX**](d3dxmatrix.md) , содержащую преобразованную матрицу преобразования.</span><span class="sxs-lookup"><span data-stu-id="0052d-121">Pointer to a [**D3DXMATRIX**](d3dxmatrix.md) structure that contains a translated transformation matrix.</span></span>

## <a name="remarks"></a><span data-ttu-id="0052d-122">Комментарии</span><span class="sxs-lookup"><span data-stu-id="0052d-122">Remarks</span></span>

<span data-ttu-id="0052d-123">Возвращаемое значение для этой функции совпадает со значением, возвращаемым в параметре *тоска* .</span><span class="sxs-lookup"><span data-stu-id="0052d-123">The return value for this function is the same value returned in the *pOut* parameter.</span></span> <span data-ttu-id="0052d-124">Таким образом, D3DXMATRIXTranslation можно использовать в качестве параметра для другой функции.</span><span class="sxs-lookup"><span data-stu-id="0052d-124">In this way, the D3DXMATRIXTranslation can be used as a parameter for another function.</span></span>

## <a name="requirements"></a><span data-ttu-id="0052d-125">Требования</span><span class="sxs-lookup"><span data-stu-id="0052d-125">Requirements</span></span>



| <span data-ttu-id="0052d-126">Требование</span><span class="sxs-lookup"><span data-stu-id="0052d-126">Requirement</span></span> | <span data-ttu-id="0052d-127">Значение</span><span class="sxs-lookup"><span data-stu-id="0052d-127">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="0052d-128">Header</span><span class="sxs-lookup"><span data-stu-id="0052d-128">Header</span></span><br/>  | <dl> <span data-ttu-id="0052d-129"><dt>D3dx9math. h</dt></span><span class="sxs-lookup"><span data-stu-id="0052d-129"><dt>D3dx9math.h</dt></span></span> </dl> |
| <span data-ttu-id="0052d-130">Библиотека</span><span class="sxs-lookup"><span data-stu-id="0052d-130">Library</span></span><br/> | <dl> <span data-ttu-id="0052d-131"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="0052d-131"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="0052d-132">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="0052d-132">See also</span></span>

<dl> <dt>

[<span data-ttu-id="0052d-133">Математические функции</span><span class="sxs-lookup"><span data-stu-id="0052d-133">Math Functions</span></span>](dx9-graphics-reference-d3dx-functions-math.md)
</dt> </dl>

 

 
