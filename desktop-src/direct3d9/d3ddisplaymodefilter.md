---
description: Задает типы режимов вывода для фильтрации.
ms.assetid: 4a03d0f0-dec5-4209-8c99-b58cc13064f5
title: Структура D3DDISPLAYMODEFILTER (D3d9types. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DDISPLAYMODEFILTER
api_type:
- HeaderDef
api_location:
- d3d9types.h
ms.openlocfilehash: b60c283405bead7b2618b91d6de76158841ff27f
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/15/2021
ms.locfileid: "104354463"
---
# <a name="d3ddisplaymodefilter-structure"></a><span data-ttu-id="a0e02-103">Структура D3DDISPLAYMODEFILTER</span><span class="sxs-lookup"><span data-stu-id="a0e02-103">D3DDISPLAYMODEFILTER structure</span></span>

<span data-ttu-id="a0e02-104">Задает типы режимов вывода для фильтрации.</span><span class="sxs-lookup"><span data-stu-id="a0e02-104">Specifies types of display modes to filter out.</span></span>

## <a name="syntax"></a><span data-ttu-id="a0e02-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="a0e02-105">Syntax</span></span>


```C++
typedef struct {
  UINT                Size;
  D3DFORMAT           Format;
  D3DSCANLINEORDERING ScanLineOrdering;
} D3DDISPLAYMODEFILTER;
```



## <a name="members"></a><span data-ttu-id="a0e02-106">Члены</span><span class="sxs-lookup"><span data-stu-id="a0e02-106">Members</span></span>

<dl> <dt>

<span data-ttu-id="a0e02-107">**Размер**</span><span class="sxs-lookup"><span data-stu-id="a0e02-107">**Size**</span></span>
</dt> <dd>

<span data-ttu-id="a0e02-108">Тип: **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="a0e02-108">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="a0e02-109">Размер этой структуры.</span><span class="sxs-lookup"><span data-stu-id="a0e02-109">The size of this structure.</span></span> <span data-ttu-id="a0e02-110">Для этого параметра всегда должно быть задано значение sizeof (D3DDISPLAYMODEFILTER).</span><span class="sxs-lookup"><span data-stu-id="a0e02-110">This should always be set to sizeof(D3DDISPLAYMODEFILTER).</span></span>

</dd> <dt>

<span data-ttu-id="a0e02-111">**Формат**</span><span class="sxs-lookup"><span data-stu-id="a0e02-111">**Format**</span></span>
</dt> <dd>

<span data-ttu-id="a0e02-112">Тип: **[D3DFORMAT](d3dformat.md)**</span><span class="sxs-lookup"><span data-stu-id="a0e02-112">Type: **[D3DFORMAT](d3dformat.md)**</span></span>

</dd> <dd>

<span data-ttu-id="a0e02-113">Формат режима экрана для фильтрации. См. [D3DFORMAT](d3dformat.md).</span><span class="sxs-lookup"><span data-stu-id="a0e02-113">The display mode format to filter out. See [D3DFORMAT](d3dformat.md).</span></span>

</dd> <dt>

<span data-ttu-id="a0e02-114">**сканлинеордеринг**</span><span class="sxs-lookup"><span data-stu-id="a0e02-114">**ScanLineOrdering**</span></span>
</dt> <dd>

<span data-ttu-id="a0e02-115">Тип: **[ **D3DSCANLINEORDERING**](./d3dscanlineordering.md)**</span><span class="sxs-lookup"><span data-stu-id="a0e02-115">Type: **[**D3DSCANLINEORDERING**](./d3dscanlineordering.md)**</span></span>

</dd> <dd>

<span data-ttu-id="a0e02-116">Является ли порядок сканлине чередованием или прогрессивным.</span><span class="sxs-lookup"><span data-stu-id="a0e02-116">Whether the scanline ordering is interlaced or progressive.</span></span> <span data-ttu-id="a0e02-117">См. [**D3DSCANLINEORDERING**](./d3dscanlineordering.md).</span><span class="sxs-lookup"><span data-stu-id="a0e02-117">See [**D3DSCANLINEORDERING**](./d3dscanlineordering.md).</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="a0e02-118">Требования</span><span class="sxs-lookup"><span data-stu-id="a0e02-118">Requirements</span></span>



| <span data-ttu-id="a0e02-119">Требование</span><span class="sxs-lookup"><span data-stu-id="a0e02-119">Requirement</span></span> | <span data-ttu-id="a0e02-120">Значение</span><span class="sxs-lookup"><span data-stu-id="a0e02-120">Value</span></span> |
|-------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="a0e02-121">Header</span><span class="sxs-lookup"><span data-stu-id="a0e02-121">Header</span></span><br/> | <dl> <span data-ttu-id="a0e02-122"><dt>D3d9types. h</dt></span><span class="sxs-lookup"><span data-stu-id="a0e02-122"><dt>D3d9types.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="a0e02-123">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="a0e02-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a0e02-124">Структуры Direct3D</span><span class="sxs-lookup"><span data-stu-id="a0e02-124">Direct3D Structures</span></span>](dx9-graphics-reference-d3d-structures.md)
</dt> </dl>

 

 
