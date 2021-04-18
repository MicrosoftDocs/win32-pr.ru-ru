---
description: Возвращает размер вершины в объявлении вершины.
ms.assetid: a2524f96-103e-43ab-bdcb-b99e7402fd89
title: Функция D3DXGetDeclVertexSize (D3DX9Mesh. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXGetDeclVertexSize
api_type:
- LibDef
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: c962064faa61dc7045b0111c5efbf1d1bea9fd40
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/15/2021
ms.locfileid: "105713675"
---
# <a name="d3dxgetdeclvertexsize-function"></a><span data-ttu-id="e4afa-103">Функция D3DXGetDeclVertexSize</span><span class="sxs-lookup"><span data-stu-id="e4afa-103">D3DXGetDeclVertexSize function</span></span>

<span data-ttu-id="e4afa-104">Возвращает размер вершины в объявлении вершины.</span><span class="sxs-lookup"><span data-stu-id="e4afa-104">Returns the size of a vertex from the vertex declaration.</span></span>

## <a name="syntax"></a><span data-ttu-id="e4afa-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="e4afa-105">Syntax</span></span>


```C++
UINT D3DXGetDeclVertexSize(
  _In_ const D3DVERTEXELEMENT9 *pDecl,
  _In_       DWORD             Stream
);
```



## <a name="parameters"></a><span data-ttu-id="e4afa-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="e4afa-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="e4afa-107">*пдекл* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="e4afa-107">*pDecl* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="e4afa-108">Тип: **const [**D3DVERTEXELEMENT9**](d3dvertexelement9.md) \***</span><span class="sxs-lookup"><span data-stu-id="e4afa-108">Type: **const [**D3DVERTEXELEMENT9**](d3dvertexelement9.md)\***</span></span>

<span data-ttu-id="e4afa-109">Указатель на объявление вершины.</span><span class="sxs-lookup"><span data-stu-id="e4afa-109">A pointer to the vertex declaration.</span></span> <span data-ttu-id="e4afa-110">См. [**D3DVERTEXELEMENT9**](d3dvertexelement9.md).</span><span class="sxs-lookup"><span data-stu-id="e4afa-110">See [**D3DVERTEXELEMENT9**](d3dvertexelement9.md).</span></span>

</dd> <dt>

<span data-ttu-id="e4afa-111">*Потоковая передача* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="e4afa-111">*Stream* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="e4afa-112">Тип: **[ **DWORD**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="e4afa-112">Type: **[**DWORD**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="e4afa-113">Индекс потока, начинающийся с нуля.</span><span class="sxs-lookup"><span data-stu-id="e4afa-113">The zero-based stream index.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="e4afa-114">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="e4afa-114">Return value</span></span>

<span data-ttu-id="e4afa-115">Тип: **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="e4afa-115">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="e4afa-116">Размер объявления вершины в байтах.</span><span class="sxs-lookup"><span data-stu-id="e4afa-116">The vertex declaration size, in bytes.</span></span>

## <a name="requirements"></a><span data-ttu-id="e4afa-117">Требования</span><span class="sxs-lookup"><span data-stu-id="e4afa-117">Requirements</span></span>



| <span data-ttu-id="e4afa-118">Требование</span><span class="sxs-lookup"><span data-stu-id="e4afa-118">Requirement</span></span> | <span data-ttu-id="e4afa-119">Значение</span><span class="sxs-lookup"><span data-stu-id="e4afa-119">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="e4afa-120">Header</span><span class="sxs-lookup"><span data-stu-id="e4afa-120">Header</span></span><br/>  | <dl> <span data-ttu-id="e4afa-121"><dt>D3DX9Mesh. h</dt></span><span class="sxs-lookup"><span data-stu-id="e4afa-121"><dt>D3DX9Mesh.h</dt></span></span> </dl> |
| <span data-ttu-id="e4afa-122">Библиотека</span><span class="sxs-lookup"><span data-stu-id="e4afa-122">Library</span></span><br/> | <dl> <span data-ttu-id="e4afa-123"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="e4afa-123"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="e4afa-124">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="e4afa-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e4afa-125">Функции сетки</span><span class="sxs-lookup"><span data-stu-id="e4afa-125">Mesh Functions</span></span>](dx9-graphics-reference-d3dx-functions-mesh.md)
</dt> </dl>

 

 
