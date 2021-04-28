---
description: 'Метод ID3DXBaseMesh:: Жетфвф — получает значение фиксированной вершины функции.'
ms.assetid: ed56ff2d-0366-426c-9f9a-7d1a7c5d1a7c
title: 'Метод ID3DXBaseMesh:: Жетфвф (D3DX9Mesh. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXBaseMesh.GetFVF
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 4e37db51238137d67ba6e060ecfafb7d1361727e
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2021
ms.locfileid: "108115442"
---
# <a name="id3dxbasemeshgetfvf-method"></a><span data-ttu-id="a7d8d-103">Метод ID3DXBaseMesh:: Жетфвф</span><span class="sxs-lookup"><span data-stu-id="a7d8d-103">ID3DXBaseMesh::GetFVF method</span></span>

<span data-ttu-id="a7d8d-104">Возвращает значение фиксированной вершины функции.</span><span class="sxs-lookup"><span data-stu-id="a7d8d-104">Gets the fixed function vertex value.</span></span>

## <a name="syntax"></a><span data-ttu-id="a7d8d-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="a7d8d-105">Syntax</span></span>


```C++
DWORD GetFVF();
```



## <a name="parameters"></a><span data-ttu-id="a7d8d-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="a7d8d-106">Parameters</span></span>

<span data-ttu-id="a7d8d-107">Этот метод не имеет параметров.</span><span class="sxs-lookup"><span data-stu-id="a7d8d-107">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="a7d8d-108">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="a7d8d-108">Return value</span></span>

<span data-ttu-id="a7d8d-109">Тип: **[ **DWORD**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="a7d8d-109">Type: **[**DWORD**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="a7d8d-110">Возвращает коды гибких форматов вершин (ФВФ).</span><span class="sxs-lookup"><span data-stu-id="a7d8d-110">Returns the flexible vertex format (FVF) codes.</span></span>

## <a name="remarks"></a><span data-ttu-id="a7d8d-111">Remarks</span><span class="sxs-lookup"><span data-stu-id="a7d8d-111">Remarks</span></span>

<span data-ttu-id="a7d8d-112">Этот метод может возвращать значение 0, если формат вершин не может быть напрямую сопоставлен с кодом ФВФ.</span><span class="sxs-lookup"><span data-stu-id="a7d8d-112">This method can return 0 if the vertex format cannot be mapped directly to an FVF code.</span></span> <span data-ttu-id="a7d8d-113">Это произойдет для сетки, созданной из объявления вершины, которая не имеет тех же порядка и элементов, которые поддерживаются кодами ФВФ.</span><span class="sxs-lookup"><span data-stu-id="a7d8d-113">This will occur for a mesh created from a vertex declaration that doesn't have the same order and elements supported by the FVF codes.</span></span>

## <a name="requirements"></a><span data-ttu-id="a7d8d-114">Требования</span><span class="sxs-lookup"><span data-stu-id="a7d8d-114">Requirements</span></span>



| <span data-ttu-id="a7d8d-115">Требование</span><span class="sxs-lookup"><span data-stu-id="a7d8d-115">Requirement</span></span> | <span data-ttu-id="a7d8d-116">Значение</span><span class="sxs-lookup"><span data-stu-id="a7d8d-116">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="a7d8d-117">Header</span><span class="sxs-lookup"><span data-stu-id="a7d8d-117">Header</span></span><br/>  | <dl> <span data-ttu-id="a7d8d-118"><dt>D3DX9Mesh. h</dt></span><span class="sxs-lookup"><span data-stu-id="a7d8d-118"><dt>D3DX9Mesh.h</dt></span></span> </dl> |
| <span data-ttu-id="a7d8d-119">Библиотека</span><span class="sxs-lookup"><span data-stu-id="a7d8d-119">Library</span></span><br/> | <dl> <span data-ttu-id="a7d8d-120"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="a7d8d-120"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="a7d8d-121">См. также</span><span class="sxs-lookup"><span data-stu-id="a7d8d-121">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a7d8d-122">ID3DXBaseMesh</span><span class="sxs-lookup"><span data-stu-id="a7d8d-122">ID3DXBaseMesh</span></span>](id3dxbasemesh.md)
</dt> </dl>

 

 
