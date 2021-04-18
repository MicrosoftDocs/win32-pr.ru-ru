---
description: Сведения о свойствах режима экрана.
ms.assetid: df9d12b9-7acb-435b-9d54-0b095c871f0e
title: Структура D3DDISPLAYMODEEX (D3d9types. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DDISPLAYMODEEX
api_type:
- HeaderDef
api_location:
- d3d9types.h
ms.openlocfilehash: 5906b6b23cc83e6d2379f0c5923b08b220285708
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/15/2021
ms.locfileid: "105694117"
---
# <a name="d3ddisplaymodeex-structure"></a><span data-ttu-id="3ef07-103">Структура D3DDISPLAYMODEEX</span><span class="sxs-lookup"><span data-stu-id="3ef07-103">D3DDISPLAYMODEEX structure</span></span>

<span data-ttu-id="3ef07-104">Сведения о свойствах режима экрана.</span><span class="sxs-lookup"><span data-stu-id="3ef07-104">Information about the properties of a display mode.</span></span>

## <a name="syntax"></a><span data-ttu-id="3ef07-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="3ef07-105">Syntax</span></span>


```C++
typedef struct {
  UINT                Size;
  UINT                Width;
  UINT                Height;
  UINT                RefreshRate;
  D3DFORMAT           Format;
  D3DSCANLINEORDERING ScanLineOrdering;
} D3DDISPLAYMODEEX;
```



## <a name="members"></a><span data-ttu-id="3ef07-106">Члены</span><span class="sxs-lookup"><span data-stu-id="3ef07-106">Members</span></span>

<dl> <dt>

<span data-ttu-id="3ef07-107">**Размер**</span><span class="sxs-lookup"><span data-stu-id="3ef07-107">**Size**</span></span>
</dt> <dd>

<span data-ttu-id="3ef07-108">Тип: **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="3ef07-108">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="3ef07-109">Размер этой структуры.</span><span class="sxs-lookup"><span data-stu-id="3ef07-109">The size of this structure.</span></span> <span data-ttu-id="3ef07-110">Для этого параметра всегда должно быть задано значение sizeof (D3DDISPLAYMODEEX).</span><span class="sxs-lookup"><span data-stu-id="3ef07-110">This should always be set to sizeof(D3DDISPLAYMODEEX).</span></span>

</dd> <dt>

<span data-ttu-id="3ef07-111">**Width**</span><span class="sxs-lookup"><span data-stu-id="3ef07-111">**Width**</span></span>
</dt> <dd>

<span data-ttu-id="3ef07-112">Тип: **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="3ef07-112">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="3ef07-113">Ширина режима экрана.</span><span class="sxs-lookup"><span data-stu-id="3ef07-113">Width of the display mode.</span></span>

</dd> <dt>

<span data-ttu-id="3ef07-114">**Height**</span><span class="sxs-lookup"><span data-stu-id="3ef07-114">**Height**</span></span>
</dt> <dd>

<span data-ttu-id="3ef07-115">Тип: **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="3ef07-115">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="3ef07-116">Высота режима экрана.</span><span class="sxs-lookup"><span data-stu-id="3ef07-116">Height of the display mode.</span></span>

</dd> <dt>

<span data-ttu-id="3ef07-117">**рефрешрате**</span><span class="sxs-lookup"><span data-stu-id="3ef07-117">**RefreshRate**</span></span>
</dt> <dd>

<span data-ttu-id="3ef07-118">Тип: **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="3ef07-118">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="3ef07-119">Частота обновления режима экрана.</span><span class="sxs-lookup"><span data-stu-id="3ef07-119">Refresh rate of the display mode.</span></span>

</dd> <dt>

<span data-ttu-id="3ef07-120">**Формат**</span><span class="sxs-lookup"><span data-stu-id="3ef07-120">**Format**</span></span>
</dt> <dd>

<span data-ttu-id="3ef07-121">Тип: **[D3DFORMAT](d3dformat.md)**</span><span class="sxs-lookup"><span data-stu-id="3ef07-121">Type: **[D3DFORMAT](d3dformat.md)**</span></span>

</dd> <dd>

<span data-ttu-id="3ef07-122">Формат режима экрана.</span><span class="sxs-lookup"><span data-stu-id="3ef07-122">Format of the display mode.</span></span> <span data-ttu-id="3ef07-123">См. [D3DFORMAT](d3dformat.md).</span><span class="sxs-lookup"><span data-stu-id="3ef07-123">See [D3DFORMAT](d3dformat.md).</span></span>

</dd> <dt>

<span data-ttu-id="3ef07-124">**сканлинеордеринг**</span><span class="sxs-lookup"><span data-stu-id="3ef07-124">**ScanLineOrdering**</span></span>
</dt> <dd>

<span data-ttu-id="3ef07-125">Тип: **[ **D3DSCANLINEORDERING**](./d3dscanlineordering.md)**</span><span class="sxs-lookup"><span data-stu-id="3ef07-125">Type: **[**D3DSCANLINEORDERING**](./d3dscanlineordering.md)**</span></span>

</dd> <dd>

<span data-ttu-id="3ef07-126">Указывает, является ли порядок сканлине прогрессивным или чередованием.</span><span class="sxs-lookup"><span data-stu-id="3ef07-126">Indicates whether the scanline order is progressive or interlaced.</span></span> <span data-ttu-id="3ef07-127">См. [**D3DSCANLINEORDERING**](./d3dscanlineordering.md).</span><span class="sxs-lookup"><span data-stu-id="3ef07-127">See [**D3DSCANLINEORDERING**](./d3dscanlineordering.md).</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="3ef07-128">Комментарии</span><span class="sxs-lookup"><span data-stu-id="3ef07-128">Remarks</span></span>

<span data-ttu-id="3ef07-129">Эта структура используется в различных методах для создания устройств Direct3D 9Ex и управления ими ([**IDirect3DDevice9Ex**](/windows/desktop/api/d3d9/nn-d3d9-idirect3ddevice9ex)) и цепочек переключений ([**IDirect3DSwapChain9Ex**](/windows/desktop/api/d3d9/nn-d3d9-idirect3dswapchain9ex)).</span><span class="sxs-lookup"><span data-stu-id="3ef07-129">This structure is used in various methods to create and manage Direct3D 9Ex devices ([**IDirect3DDevice9Ex**](/windows/desktop/api/d3d9/nn-d3d9-idirect3ddevice9ex)) and swapchains ([**IDirect3DSwapChain9Ex**](/windows/desktop/api/d3d9/nn-d3d9-idirect3dswapchain9ex)).</span></span>

## <a name="requirements"></a><span data-ttu-id="3ef07-130">Требования</span><span class="sxs-lookup"><span data-stu-id="3ef07-130">Requirements</span></span>



| <span data-ttu-id="3ef07-131">Требование</span><span class="sxs-lookup"><span data-stu-id="3ef07-131">Requirement</span></span> | <span data-ttu-id="3ef07-132">Значение</span><span class="sxs-lookup"><span data-stu-id="3ef07-132">Value</span></span> |
|-------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="3ef07-133">Header</span><span class="sxs-lookup"><span data-stu-id="3ef07-133">Header</span></span><br/> | <dl> <span data-ttu-id="3ef07-134"><dt>D3d9types. h</dt></span><span class="sxs-lookup"><span data-stu-id="3ef07-134"><dt>D3d9types.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="3ef07-135">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="3ef07-135">See also</span></span>

<dl> <dt>

[<span data-ttu-id="3ef07-136">Структуры Direct3D</span><span class="sxs-lookup"><span data-stu-id="3ef07-136">Direct3D Structures</span></span>](dx9-graphics-reference-d3d-structures.md)
</dt> </dl>

 

 
