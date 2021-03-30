---
description: Возвращает значение фиксированной вершины функции.
ms.assetid: 9b80c4b9-2e5b-4965-99b9-ad6c459ef413
title: 'Метод ID3DXSkinInfo:: Жетфвф (D3DX9Mesh. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXSkinInfo.GetFVF
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 6d48cd9cea6efd6cb43e6da6877a7aaf42909c71
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/15/2021
ms.locfileid: "104354070"
---
# <a name="id3dxskininfogetfvf-method"></a><span data-ttu-id="eb103-103">Метод ID3DXSkinInfo:: Жетфвф</span><span class="sxs-lookup"><span data-stu-id="eb103-103">ID3DXSkinInfo::GetFVF method</span></span>

<span data-ttu-id="eb103-104">Возвращает значение фиксированной вершины функции.</span><span class="sxs-lookup"><span data-stu-id="eb103-104">Gets the fixed function vertex value.</span></span>

## <a name="syntax"></a><span data-ttu-id="eb103-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="eb103-105">Syntax</span></span>


```C++
DWORD GetFVF();
```



## <a name="parameters"></a><span data-ttu-id="eb103-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="eb103-106">Parameters</span></span>

<span data-ttu-id="eb103-107">Этот метод не имеет параметров.</span><span class="sxs-lookup"><span data-stu-id="eb103-107">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="eb103-108">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="eb103-108">Return value</span></span>

<span data-ttu-id="eb103-109">Тип: **[ **DWORD**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="eb103-109">Type: **[**DWORD**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="eb103-110">Возвращает коды гибких форматов вершин (ФВФ).</span><span class="sxs-lookup"><span data-stu-id="eb103-110">Returns the flexible vertex format (FVF) codes.</span></span>

## <a name="remarks"></a><span data-ttu-id="eb103-111">Комментарии</span><span class="sxs-lookup"><span data-stu-id="eb103-111">Remarks</span></span>

<span data-ttu-id="eb103-112">Этот метод может возвращать значение 0, если формат вершин не может быть напрямую сопоставлен с кодом ФВФ.</span><span class="sxs-lookup"><span data-stu-id="eb103-112">This method can return 0 if the vertex format cannot be mapped directly to an FVF code.</span></span> <span data-ttu-id="eb103-113">Это произойдет для сетки, созданной из объявления вершины, которая не имеет тех же порядка и элементов, которые поддерживаются кодами ФВФ.</span><span class="sxs-lookup"><span data-stu-id="eb103-113">This will occur for a mesh created from a vertex declaration that doesn't have the same order and elements supported by the FVF codes.</span></span>

## <a name="requirements"></a><span data-ttu-id="eb103-114">Требования</span><span class="sxs-lookup"><span data-stu-id="eb103-114">Requirements</span></span>



| <span data-ttu-id="eb103-115">Требование</span><span class="sxs-lookup"><span data-stu-id="eb103-115">Requirement</span></span> | <span data-ttu-id="eb103-116">Значение</span><span class="sxs-lookup"><span data-stu-id="eb103-116">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="eb103-117">Header</span><span class="sxs-lookup"><span data-stu-id="eb103-117">Header</span></span><br/>  | <dl> <span data-ttu-id="eb103-118"><dt>D3DX9Mesh. h</dt></span><span class="sxs-lookup"><span data-stu-id="eb103-118"><dt>D3DX9Mesh.h</dt></span></span> </dl> |
| <span data-ttu-id="eb103-119">Библиотека</span><span class="sxs-lookup"><span data-stu-id="eb103-119">Library</span></span><br/> | <dl> <span data-ttu-id="eb103-120"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="eb103-120"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="eb103-121">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="eb103-121">See also</span></span>

<dl> <dt>

[<span data-ttu-id="eb103-122">ID3DXSkinInfo</span><span class="sxs-lookup"><span data-stu-id="eb103-122">ID3DXSkinInfo</span></span>](id3dxskininfo.md)
</dt> <dt>

[<span data-ttu-id="eb103-123">**ID3DXSkinInfo:: Сетфвф**</span><span class="sxs-lookup"><span data-stu-id="eb103-123">**ID3DXSkinInfo::SetFVF**</span></span>](id3dxskininfo--setfvf.md)
</dt> </dl>

 

 
