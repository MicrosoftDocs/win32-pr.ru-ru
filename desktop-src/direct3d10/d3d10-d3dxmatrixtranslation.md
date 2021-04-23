---
description: Создание матрицы перевода.
ms.assetid: a3565a06-22af-4ded-8835-da4c7ae81805
title: Функция D3DXMatrixTranslation (D3DX10Math. h)
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
- D3DX10.lib
- D3DX10.dll
ms.openlocfilehash: 7abf55e5b51091de5d823ba837cdc8ad51e3940b
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/15/2021
ms.locfileid: "105720959"
---
# <a name="d3dxmatrixtranslation-function-d3dx10mathh"></a><span data-ttu-id="92df4-103">Функция D3DXMatrixTranslation (D3DX10Math. h)</span><span class="sxs-lookup"><span data-stu-id="92df4-103">D3DXMatrixTranslation function (D3DX10Math.h)</span></span>

<span data-ttu-id="92df4-104">Создание матрицы перевода.</span><span class="sxs-lookup"><span data-stu-id="92df4-104">Create a translation matrix.</span></span>

## <a name="syntax"></a><span data-ttu-id="92df4-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="92df4-105">Syntax</span></span>


```C++
D3DXMATRIX* D3DXMatrixTranslation(
  _Inout_ D3DXMATRIX *pOut,
  _In_    FLOAT      x,
  _In_    FLOAT      y,
  _In_    FLOAT      z
);
```



## <a name="parameters"></a><span data-ttu-id="92df4-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="92df4-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="92df4-107">*тоска* \[ в, out\]</span><span class="sxs-lookup"><span data-stu-id="92df4-107">*pOut* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="92df4-108">Тип: **[ **D3DXMATRIX**](../direct3d9/d3dxmatrix.md)\***</span><span class="sxs-lookup"><span data-stu-id="92df4-108">Type: **[**D3DXMATRIX**](../direct3d9/d3dxmatrix.md)\***</span></span>

<span data-ttu-id="92df4-109">Матрица, которая станет матрицей перевода.</span><span class="sxs-lookup"><span data-stu-id="92df4-109">The matrix that will become a translation matrix.</span></span> <span data-ttu-id="92df4-110">См. [**D3DXMATRIX**](d3d10-d3dxmatrix.md).</span><span class="sxs-lookup"><span data-stu-id="92df4-110">See [**D3DXMATRIX**](d3d10-d3dxmatrix.md).</span></span>

</dd> <dt>

<span data-ttu-id="92df4-111">*x* \[ в\]</span><span class="sxs-lookup"><span data-stu-id="92df4-111">*x* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="92df4-112">Тип: **[ **float**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="92df4-112">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="92df4-113">Компонент x перевода.</span><span class="sxs-lookup"><span data-stu-id="92df4-113">The x-component of the translation.</span></span>

</dd> <dt>

<span data-ttu-id="92df4-114">*y* \[ в\]</span><span class="sxs-lookup"><span data-stu-id="92df4-114">*y* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="92df4-115">Тип: **[ **float**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="92df4-115">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="92df4-116">Компонент y перевода.</span><span class="sxs-lookup"><span data-stu-id="92df4-116">The y-component of the translation.</span></span>

</dd> <dt>

<span data-ttu-id="92df4-117">*z* \[ в\]</span><span class="sxs-lookup"><span data-stu-id="92df4-117">*z* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="92df4-118">Тип: **[ **float**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="92df4-118">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="92df4-119">Z-компонент перевода.</span><span class="sxs-lookup"><span data-stu-id="92df4-119">The z-component of the translation.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="92df4-120">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="92df4-120">Return value</span></span>

<span data-ttu-id="92df4-121">Тип: **[ **D3DXMATRIX**](../direct3d9/d3dxmatrix.md)\***</span><span class="sxs-lookup"><span data-stu-id="92df4-121">Type: **[**D3DXMATRIX**](../direct3d9/d3dxmatrix.md)\***</span></span>

<span data-ttu-id="92df4-122">Матрица трансляции.</span><span class="sxs-lookup"><span data-stu-id="92df4-122">The translation matrix.</span></span>

## <a name="requirements"></a><span data-ttu-id="92df4-123">Требования</span><span class="sxs-lookup"><span data-stu-id="92df4-123">Requirements</span></span>



| <span data-ttu-id="92df4-124">Требование</span><span class="sxs-lookup"><span data-stu-id="92df4-124">Requirement</span></span> | <span data-ttu-id="92df4-125">Значение</span><span class="sxs-lookup"><span data-stu-id="92df4-125">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="92df4-126">Header</span><span class="sxs-lookup"><span data-stu-id="92df4-126">Header</span></span><br/>  | <dl> <span data-ttu-id="92df4-127"><dt>D3DX10Math. h</dt></span><span class="sxs-lookup"><span data-stu-id="92df4-127"><dt>D3DX10Math.h</dt></span></span> </dl> |
| <span data-ttu-id="92df4-128">Библиотека</span><span class="sxs-lookup"><span data-stu-id="92df4-128">Library</span></span><br/> | <dl> <span data-ttu-id="92df4-129"><dt>D3DX10. lib</dt></span><span class="sxs-lookup"><span data-stu-id="92df4-129"><dt>D3DX10.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="92df4-130">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="92df4-130">See also</span></span>

<dl> <dt>

[<span data-ttu-id="92df4-131">Математические функции</span><span class="sxs-lookup"><span data-stu-id="92df4-131">Math Functions</span></span>](d3d10-graphics-reference-d3dx10-functions-math.md)
</dt> </dl>

 

 
