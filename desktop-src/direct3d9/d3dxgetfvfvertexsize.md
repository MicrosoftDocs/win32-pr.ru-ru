---
description: Возвращает размер вершины для гибкого формата вершин (ФВФ).
ms.assetid: 9d8e2b1f-0ec8-46ab-8492-2cadd700225e
title: Функция D3DXGetFVFVertexSize (D3dx9mesh. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXGetFVFVertexSize
api_type:
- LibDef
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: cd5dbe5a58faf385d6f9f50f2fcb4a01a7c01dc5
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/15/2021
ms.locfileid: "105713672"
---
# <a name="d3dxgetfvfvertexsize-function"></a><span data-ttu-id="13cb4-103">Функция D3DXGetFVFVertexSize</span><span class="sxs-lookup"><span data-stu-id="13cb4-103">D3DXGetFVFVertexSize function</span></span>

<span data-ttu-id="13cb4-104">Возвращает размер вершины для гибкого формата вершин (ФВФ).</span><span class="sxs-lookup"><span data-stu-id="13cb4-104">Returns the size of a vertex for a flexible vertex format (FVF).</span></span>

## <a name="syntax"></a><span data-ttu-id="13cb4-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="13cb4-105">Syntax</span></span>


```C++
UINT D3DXGetFVFVertexSize(
  _In_ DWORD FVF
);
```



## <a name="parameters"></a><span data-ttu-id="13cb4-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="13cb4-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="13cb4-107">*Фвф* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="13cb4-107">*FVF* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="13cb4-108">Тип: **[ **DWORD**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="13cb4-108">Type: **[**DWORD**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="13cb4-109">ФВФ для запроса.</span><span class="sxs-lookup"><span data-stu-id="13cb4-109">FVF to be queried.</span></span> <span data-ttu-id="13cb4-110">Сочетание [D3DFVF](d3dfvf.md).</span><span class="sxs-lookup"><span data-stu-id="13cb4-110">A combination of [D3DFVF](d3dfvf.md).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="13cb4-111">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="13cb4-111">Return value</span></span>

<span data-ttu-id="13cb4-112">Тип: **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="13cb4-112">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="13cb4-113">Размер вершины ФВФ в байтах.</span><span class="sxs-lookup"><span data-stu-id="13cb4-113">The FVF vertex size, in bytes.</span></span>

## <a name="requirements"></a><span data-ttu-id="13cb4-114">Требования</span><span class="sxs-lookup"><span data-stu-id="13cb4-114">Requirements</span></span>



| <span data-ttu-id="13cb4-115">Требование</span><span class="sxs-lookup"><span data-stu-id="13cb4-115">Requirement</span></span> | <span data-ttu-id="13cb4-116">Значение</span><span class="sxs-lookup"><span data-stu-id="13cb4-116">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="13cb4-117">Header</span><span class="sxs-lookup"><span data-stu-id="13cb4-117">Header</span></span><br/>  | <dl> <span data-ttu-id="13cb4-118"><dt>D3dx9mesh. h</dt></span><span class="sxs-lookup"><span data-stu-id="13cb4-118"><dt>D3dx9mesh.h</dt></span></span> </dl> |
| <span data-ttu-id="13cb4-119">Библиотека</span><span class="sxs-lookup"><span data-stu-id="13cb4-119">Library</span></span><br/> | <dl> <span data-ttu-id="13cb4-120"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="13cb4-120"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="13cb4-121">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="13cb4-121">See also</span></span>

<dl> <dt>

[<span data-ttu-id="13cb4-122">Функции сетки</span><span class="sxs-lookup"><span data-stu-id="13cb4-122">Mesh Functions</span></span>](dx9-graphics-reference-d3dx-functions-mesh.md)
</dt> </dl>

 

 
