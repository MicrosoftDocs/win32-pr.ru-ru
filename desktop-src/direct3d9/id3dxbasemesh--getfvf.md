---
description: Возвращает значение фиксированной вершины функции.
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
ms.openlocfilehash: 7ee76292c30b3dfb0a2e38b060f50ef643ae07ae
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/15/2021
ms.locfileid: "104000402"
---
# <a name="id3dxbasemeshgetfvf-method"></a><span data-ttu-id="162bb-103">Метод ID3DXBaseMesh:: Жетфвф</span><span class="sxs-lookup"><span data-stu-id="162bb-103">ID3DXBaseMesh::GetFVF method</span></span>

<span data-ttu-id="162bb-104">Возвращает значение фиксированной вершины функции.</span><span class="sxs-lookup"><span data-stu-id="162bb-104">Gets the fixed function vertex value.</span></span>

## <a name="syntax"></a><span data-ttu-id="162bb-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="162bb-105">Syntax</span></span>


```C++
DWORD GetFVF();
```



## <a name="parameters"></a><span data-ttu-id="162bb-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="162bb-106">Parameters</span></span>

<span data-ttu-id="162bb-107">Этот метод не имеет параметров.</span><span class="sxs-lookup"><span data-stu-id="162bb-107">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="162bb-108">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="162bb-108">Return value</span></span>

<span data-ttu-id="162bb-109">Тип: **[ **DWORD**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="162bb-109">Type: **[**DWORD**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="162bb-110">Возвращает коды гибких форматов вершин (ФВФ).</span><span class="sxs-lookup"><span data-stu-id="162bb-110">Returns the flexible vertex format (FVF) codes.</span></span>

## <a name="remarks"></a><span data-ttu-id="162bb-111">Комментарии</span><span class="sxs-lookup"><span data-stu-id="162bb-111">Remarks</span></span>

<span data-ttu-id="162bb-112">Этот метод может возвращать значение 0, если формат вершин не может быть напрямую сопоставлен с кодом ФВФ.</span><span class="sxs-lookup"><span data-stu-id="162bb-112">This method can return 0 if the vertex format cannot be mapped directly to an FVF code.</span></span> <span data-ttu-id="162bb-113">Это произойдет для сетки, созданной из объявления вершины, которая не имеет тех же порядка и элементов, которые поддерживаются кодами ФВФ.</span><span class="sxs-lookup"><span data-stu-id="162bb-113">This will occur for a mesh created from a vertex declaration that doesn't have the same order and elements supported by the FVF codes.</span></span>

## <a name="requirements"></a><span data-ttu-id="162bb-114">Требования</span><span class="sxs-lookup"><span data-stu-id="162bb-114">Requirements</span></span>



| <span data-ttu-id="162bb-115">Требование</span><span class="sxs-lookup"><span data-stu-id="162bb-115">Requirement</span></span> | <span data-ttu-id="162bb-116">Значение</span><span class="sxs-lookup"><span data-stu-id="162bb-116">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="162bb-117">Header</span><span class="sxs-lookup"><span data-stu-id="162bb-117">Header</span></span><br/>  | <dl> <span data-ttu-id="162bb-118"><dt>D3DX9Mesh. h</dt></span><span class="sxs-lookup"><span data-stu-id="162bb-118"><dt>D3DX9Mesh.h</dt></span></span> </dl> |
| <span data-ttu-id="162bb-119">Библиотека</span><span class="sxs-lookup"><span data-stu-id="162bb-119">Library</span></span><br/> | <dl> <span data-ttu-id="162bb-120"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="162bb-120"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="162bb-121">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="162bb-121">See also</span></span>

<dl> <dt>

[<span data-ttu-id="162bb-122">ID3DXBaseMesh</span><span class="sxs-lookup"><span data-stu-id="162bb-122">ID3DXBaseMesh</span></span>](id3dxbasemesh.md)
</dt> </dl>

 

 
