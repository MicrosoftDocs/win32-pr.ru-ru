---
title: Структура CD3DX12_SUBRESOURCE_TILING (D3dx12. h)
description: Вспомогательная структура, позволяющая легко инициализировать \_ \_ структуру разбиения подресурсов D3D12.
ms.assetid: 102E5E25-300B-40F2-A953-E40AD7EE61AD
keywords:
- Структура CD3DX12_SUBRESOURCE_TILING
topic_type:
- apiref
api_name:
- CD3DX12_SUBRESOURCE_TILING
api_location:
- d3dx12.h
api_type:
- HeaderDef
ms.localizationpriority: low
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 07677c8a8367f58016a0236cf0b5558b852bef01
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/15/2021
ms.locfileid: "105713499"
---
# <a name="cd3dx12_subresource_tiling-structure"></a><span data-ttu-id="8f546-104">\_ \_ Структура разбиения ПОДресурсов CD3DX12</span><span class="sxs-lookup"><span data-stu-id="8f546-104">CD3DX12\_SUBRESOURCE\_TILING structure</span></span>

<span data-ttu-id="8f546-105">Вспомогательная структура, позволяющая легко инициализировать структуру [**\_ \_ разбиения подресурсов D3D12**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_subresource_tiling) .</span><span class="sxs-lookup"><span data-stu-id="8f546-105">A helper structure to enable easy initialization of a [**D3D12\_SUBRESOURCE\_TILING**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_subresource_tiling) structure.</span></span>

## <a name="syntax"></a><span data-ttu-id="8f546-106">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="8f546-106">Syntax</span></span>


```C++
struct CD3DX12_SUBRESOURCE_TILING  : public D3D12_SUBRESOURCE_TILING{
   CD3DX12_SUBRESOURCE_TILING();
   explicit CD3DX12_SUBRESOURCE_TILING(const D3D12_SUBRESOURCE_TILING &o);
   CD3DX12_SUBRESOURCE_TILING(UINT widthInTiles, UINT16 heightInTiles, UINT16 depthInTiles, UINT startTileIndexInOverallResource);
   operator const D3D12_SUBRESOURCE_TILING&() const;
};
```



## <a name="members"></a><span data-ttu-id="8f546-107">Члены</span><span class="sxs-lookup"><span data-stu-id="8f546-107">Members</span></span>

<dl> <dt>

<span data-ttu-id="8f546-108">**\_Разбиение ПОДРЕСУРСОВ CD3DX12 \_ ()**</span><span class="sxs-lookup"><span data-stu-id="8f546-108">**CD3DX12\_SUBRESOURCE\_TILING()**</span></span>
</dt> <dd>

<span data-ttu-id="8f546-109">Создает новый, неинициализированный экземпляр \_ ПОДресурса CD3DX12 \_ .</span><span class="sxs-lookup"><span data-stu-id="8f546-109">Creates a new, uninitialized, instance of a CD3DX12\_SUBRESOURCE\_TILING.</span></span>

</dd> <dt>

<span data-ttu-id="8f546-110">**прямое \_ разбиение ПОДРЕСУРСОВ CD3DX12 \_ (const D3D12 \_ подресурсов \_ &o)**</span><span class="sxs-lookup"><span data-stu-id="8f546-110">**explicit CD3DX12\_SUBRESOURCE\_TILING(const D3D12\_SUBRESOURCE\_TILING &o)**</span></span>
</dt> <dd>

<span data-ttu-id="8f546-111">Создает новый экземпляр подкласса CD3DX12 \_ \_ , инициализируемый с помощью содержимого другой структуры подмассива [**D3D12 \_ \_**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_subresource_tiling) .</span><span class="sxs-lookup"><span data-stu-id="8f546-111">Creates a new instance of a CD3DX12\_SUBRESOURCE\_TILING, initialized with the contents of another [**D3D12\_SUBRESOURCE\_TILING**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_subresource_tiling) structure.</span></span>

</dd> <dt>

<span data-ttu-id="8f546-112">**\_Разбиение ПОДРЕСУРСОВ CD3DX12 \_ (uint ВИДСИНТИЛЕС, UInt16 ХЕИГХТИНТИЛЕС, UINT16 ДЕПСИНТИЛЕС, uint старттилеиндексиновераллресаурце)**</span><span class="sxs-lookup"><span data-stu-id="8f546-112">**CD3DX12\_SUBRESOURCE\_TILING(UINT widthInTiles, UINT16 heightInTiles, UINT16 depthInTiles, UINT startTileIndexInOverallResource)**</span></span>
</dt> <dd>

<span data-ttu-id="8f546-113">Создает новый экземпляр \_ ПОДРЕСУРСА CD3DX12 \_ , инициализируя следующие параметры:</span><span class="sxs-lookup"><span data-stu-id="8f546-113">Creates a new instance of a CD3DX12\_SUBRESOURCE\_TILING, initializing the following parameters:</span></span>

<span data-ttu-id="8f546-114">UINT Видсинтилес</span><span class="sxs-lookup"><span data-stu-id="8f546-114">UINT widthInTiles</span></span>

<span data-ttu-id="8f546-115">UINT16 Хеигхтинтилес</span><span class="sxs-lookup"><span data-stu-id="8f546-115">UINT16 heightInTiles</span></span>

<span data-ttu-id="8f546-116">UINT16 Депсинтилес</span><span class="sxs-lookup"><span data-stu-id="8f546-116">UINT16 depthInTiles</span></span>

<span data-ttu-id="8f546-117">UINT Старттилеиндексиновераллресаурце</span><span class="sxs-lookup"><span data-stu-id="8f546-117">UINT startTileIndexInOverallResource</span></span>

</dd> <dt>

<span data-ttu-id="8f546-118">**D3D12 "operator const" \_ \_ разбиение подресурсов& () const**</span><span class="sxs-lookup"><span data-stu-id="8f546-118">**operator const D3D12\_SUBRESOURCE\_TILING&() const**</span></span>
</dt> <dd>

<span data-ttu-id="8f546-119">Определяет & оператором передачи по ссылке для типа родительской структуры.</span><span class="sxs-lookup"><span data-stu-id="8f546-119">Defines the & pass-by-reference operator for the parent structure type.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="8f546-120">Требования</span><span class="sxs-lookup"><span data-stu-id="8f546-120">Requirements</span></span>



| <span data-ttu-id="8f546-121">Требование</span><span class="sxs-lookup"><span data-stu-id="8f546-121">Requirement</span></span> | <span data-ttu-id="8f546-122">Значение</span><span class="sxs-lookup"><span data-stu-id="8f546-122">Value</span></span> |
|-------------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="8f546-123">Header</span><span class="sxs-lookup"><span data-stu-id="8f546-123">Header</span></span><br/> | <dl> <span data-ttu-id="8f546-124"><dt>D3dx12. h</dt></span><span class="sxs-lookup"><span data-stu-id="8f546-124"><dt>D3dx12.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="8f546-125">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="8f546-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="8f546-126">**\_Разбиение ПОДРЕСУРСОВ D3D12 \_**</span><span class="sxs-lookup"><span data-stu-id="8f546-126">**D3D12\_SUBRESOURCE\_TILING**</span></span>](/windows/desktop/api/d3d12/ns-d3d12-d3d12_subresource_tiling)
</dt> <dt>

[<span data-ttu-id="8f546-127">Вспомогательные структуры для D3D12</span><span class="sxs-lookup"><span data-stu-id="8f546-127">Helper Structures for D3D12</span></span>](helper-structures-for-d3d12.md)
</dt> </dl>

 

 





