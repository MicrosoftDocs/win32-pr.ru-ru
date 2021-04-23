---
title: Структура CD3DX12_TILE_SHAPE (D3dx12. h)
description: Вспомогательная структура, позволяющая легко инициализировать \_ структуру фигур мозаики D3D12 \_ .
ms.assetid: 0A5963F1-8CE5-4B03-B69F-83B2B801CC21
keywords:
- Структура CD3DX12_TILE_SHAPE
topic_type:
- apiref
api_name:
- CD3DX12_TILE_SHAPE
api_location:
- d3dx12.h
api_type:
- HeaderDef
ms.localizationpriority: low
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 998a14e1bd4898d83d049ea50bc056abaeb68544
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/15/2021
ms.locfileid: "105703670"
---
# <a name="cd3dx12_tile_shape-structure"></a><span data-ttu-id="a8b02-104">\_Структура фигур мозаики CD3DX12 \_</span><span class="sxs-lookup"><span data-stu-id="a8b02-104">CD3DX12\_TILE\_SHAPE structure</span></span>

<span data-ttu-id="a8b02-105">Вспомогательная структура, позволяющая легко инициализировать структуру [**\_ \_ фигур мозаики D3D12**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_tile_shape) .</span><span class="sxs-lookup"><span data-stu-id="a8b02-105">A helper structure to enable easy initialization of a [**D3D12\_TILE\_SHAPE**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_tile_shape) structure.</span></span>

## <a name="syntax"></a><span data-ttu-id="a8b02-106">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="a8b02-106">Syntax</span></span>


```C++
struct CD3DX12_TILE_SHAPE  : public D3D12_TILE_SHAPE{
   CD3DX12_TILE_SHAPE();
   explicit CD3DX12_TILE_SHAPE(const D3D12_TILE_SHAPE &o);
   CD3DX12_TILE_SHAPE(UINT widthInTexels, UINT heightInTexels, UINT depthInTexels);
   operator const D3D12_TILE_SHAPE&() const;
};
```



## <a name="members"></a><span data-ttu-id="a8b02-107">Члены</span><span class="sxs-lookup"><span data-stu-id="a8b02-107">Members</span></span>

<dl> <dt>

<span data-ttu-id="a8b02-108">**\_Фигура плитки CD3DX12 \_ ()**</span><span class="sxs-lookup"><span data-stu-id="a8b02-108">**CD3DX12\_TILE\_SHAPE()**</span></span>
</dt> <dd>

<span data-ttu-id="a8b02-109">Создает новый, неинициализированный экземпляр \_ фигуры мозаики CD3DX12 \_ .</span><span class="sxs-lookup"><span data-stu-id="a8b02-109">Creates a new, uninitialized, instance of a CD3DX12\_TILE\_SHAPE.</span></span>

</dd> <dt>

<span data-ttu-id="a8b02-110">**явная \_ фигура CD3DX12 \_ (элемент const D3D12 \_ , \_ фигура плитки &o)**</span><span class="sxs-lookup"><span data-stu-id="a8b02-110">**explicit CD3DX12\_TILE\_SHAPE(const D3D12\_TILE\_SHAPE &o)**</span></span>
</dt> <dd>

<span data-ttu-id="a8b02-111">Создает новый экземпляр \_ фигуры мозаики CD3DX12 \_ , инициализируемый с помощью содержимого другой структуры [**\_ \_ фигур плитки D3D12**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_tile_shape) .</span><span class="sxs-lookup"><span data-stu-id="a8b02-111">Creates a new instance of a CD3DX12\_TILE\_SHAPE, initialized with the contents of another [**D3D12\_TILE\_SHAPE**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_tile_shape) structure.</span></span>

</dd> <dt>

<span data-ttu-id="a8b02-112">**\_Фигура плитки CD3DX12 \_ (uint ВИДСИНТЕКСЕЛС, uint ХЕИГХТИНТЕКСЕЛС, uint депсинтекселс)**</span><span class="sxs-lookup"><span data-stu-id="a8b02-112">**CD3DX12\_TILE\_SHAPE(UINT widthInTexels, UINT heightInTexels, UINT depthInTexels)**</span></span>
</dt> <dd>

<span data-ttu-id="a8b02-113">Создает новый экземпляр \_ фигуры плитки CD3DX12 \_ , инициализируя следующие параметры:</span><span class="sxs-lookup"><span data-stu-id="a8b02-113">Creates a new instance of a CD3DX12\_TILE\_SHAPE, initializing the following parameters:</span></span>

<span data-ttu-id="a8b02-114">UINT Видсинтекселс</span><span class="sxs-lookup"><span data-stu-id="a8b02-114">UINT widthInTexels</span></span>

<span data-ttu-id="a8b02-115">UINT Хеигхтинтекселс</span><span class="sxs-lookup"><span data-stu-id="a8b02-115">UINT heightInTexels</span></span>

<span data-ttu-id="a8b02-116">UINT Депсинтекселс</span><span class="sxs-lookup"><span data-stu-id="a8b02-116">UINT depthInTexels</span></span>

</dd> <dt>

<span data-ttu-id="a8b02-117">**\_фигурная плитка оператора const D3D12 \_& () const**</span><span class="sxs-lookup"><span data-stu-id="a8b02-117">**operator const D3D12\_TILE\_SHAPE&() const**</span></span>
</dt> <dd>

<span data-ttu-id="a8b02-118">Определяет & оператором передачи по ссылке для типа родительской структуры.</span><span class="sxs-lookup"><span data-stu-id="a8b02-118">Defines the & pass-by-reference operator for the parent structure type.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="a8b02-119">Требования</span><span class="sxs-lookup"><span data-stu-id="a8b02-119">Requirements</span></span>



| <span data-ttu-id="a8b02-120">Требование</span><span class="sxs-lookup"><span data-stu-id="a8b02-120">Requirement</span></span> | <span data-ttu-id="a8b02-121">Значение</span><span class="sxs-lookup"><span data-stu-id="a8b02-121">Value</span></span> |
|-------------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="a8b02-122">Header</span><span class="sxs-lookup"><span data-stu-id="a8b02-122">Header</span></span><br/> | <dl> <span data-ttu-id="a8b02-123"><dt>D3dx12. h</dt></span><span class="sxs-lookup"><span data-stu-id="a8b02-123"><dt>D3dx12.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="a8b02-124">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="a8b02-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a8b02-125">**\_Фигура плитки \_ D3D12**</span><span class="sxs-lookup"><span data-stu-id="a8b02-125">**D3D12\_TILE\_SHAPE**</span></span>](/windows/desktop/api/d3d12/ns-d3d12-d3d12_tile_shape)
</dt> <dt>

[<span data-ttu-id="a8b02-126">Вспомогательные структуры для D3D12</span><span class="sxs-lookup"><span data-stu-id="a8b02-126">Helper Structures for D3D12</span></span>](helper-structures-for-d3d12.md)
</dt> </dl>

 

 





