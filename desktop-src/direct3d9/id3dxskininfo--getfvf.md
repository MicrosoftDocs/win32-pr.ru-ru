---
description: 'Метод ID3DXSkinInfo:: Жетфвф — получает значение фиксированной вершины функции.'
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
ms.openlocfilehash: 3415f86f778fbb6fb3592927277e399584bc49a9
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2021
ms.locfileid: "108107162"
---
# <a name="id3dxskininfogetfvf-method"></a><span data-ttu-id="d4232-103">Метод ID3DXSkinInfo:: Жетфвф</span><span class="sxs-lookup"><span data-stu-id="d4232-103">ID3DXSkinInfo::GetFVF method</span></span>

<span data-ttu-id="d4232-104">Возвращает значение фиксированной вершины функции.</span><span class="sxs-lookup"><span data-stu-id="d4232-104">Gets the fixed function vertex value.</span></span>

## <a name="syntax"></a><span data-ttu-id="d4232-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="d4232-105">Syntax</span></span>


```C++
DWORD GetFVF();
```



## <a name="parameters"></a><span data-ttu-id="d4232-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="d4232-106">Parameters</span></span>

<span data-ttu-id="d4232-107">Этот метод не имеет параметров.</span><span class="sxs-lookup"><span data-stu-id="d4232-107">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="d4232-108">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="d4232-108">Return value</span></span>

<span data-ttu-id="d4232-109">Тип: **[ **DWORD**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="d4232-109">Type: **[**DWORD**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="d4232-110">Возвращает коды гибких форматов вершин (ФВФ).</span><span class="sxs-lookup"><span data-stu-id="d4232-110">Returns the flexible vertex format (FVF) codes.</span></span>

## <a name="remarks"></a><span data-ttu-id="d4232-111">Remarks</span><span class="sxs-lookup"><span data-stu-id="d4232-111">Remarks</span></span>

<span data-ttu-id="d4232-112">Этот метод может возвращать значение 0, если формат вершин не может быть напрямую сопоставлен с кодом ФВФ.</span><span class="sxs-lookup"><span data-stu-id="d4232-112">This method can return 0 if the vertex format cannot be mapped directly to an FVF code.</span></span> <span data-ttu-id="d4232-113">Это произойдет для сетки, созданной из объявления вершины, которая не имеет тех же порядка и элементов, которые поддерживаются кодами ФВФ.</span><span class="sxs-lookup"><span data-stu-id="d4232-113">This will occur for a mesh created from a vertex declaration that doesn't have the same order and elements supported by the FVF codes.</span></span>

## <a name="requirements"></a><span data-ttu-id="d4232-114">Требования</span><span class="sxs-lookup"><span data-stu-id="d4232-114">Requirements</span></span>



| <span data-ttu-id="d4232-115">Требование</span><span class="sxs-lookup"><span data-stu-id="d4232-115">Requirement</span></span> | <span data-ttu-id="d4232-116">Значение</span><span class="sxs-lookup"><span data-stu-id="d4232-116">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="d4232-117">Header</span><span class="sxs-lookup"><span data-stu-id="d4232-117">Header</span></span><br/>  | <dl> <span data-ttu-id="d4232-118"><dt>D3DX9Mesh. h</dt></span><span class="sxs-lookup"><span data-stu-id="d4232-118"><dt>D3DX9Mesh.h</dt></span></span> </dl> |
| <span data-ttu-id="d4232-119">Библиотека</span><span class="sxs-lookup"><span data-stu-id="d4232-119">Library</span></span><br/> | <dl> <span data-ttu-id="d4232-120"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="d4232-120"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="d4232-121">См. также</span><span class="sxs-lookup"><span data-stu-id="d4232-121">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d4232-122">ID3DXSkinInfo</span><span class="sxs-lookup"><span data-stu-id="d4232-122">ID3DXSkinInfo</span></span>](id3dxskininfo.md)
</dt> <dt>

[<span data-ttu-id="d4232-123">**ID3DXSkinInfo:: Сетфвф**</span><span class="sxs-lookup"><span data-stu-id="d4232-123">**ID3DXSkinInfo::SetFVF**</span></span>](id3dxskininfo--setfvf.md)
</dt> </dl>

 

 
