---
title: Структура CD3DX12_TILE_REGION_SIZE (D3dx12. h)
description: Вспомогательная структура, позволяющая упростить инициализацию \_ \_ структуры размера области мозаики D3D12 \_ .
ms.assetid: 07D2D8DE-C35C-48EE-8E9E-36545B60C594
keywords:
- Структура CD3DX12_TILE_REGION_SIZE
topic_type:
- apiref
api_name:
- CD3DX12_TILE_REGION_SIZE
api_location:
- d3dx12.h
api_type:
- HeaderDef
ms.localizationpriority: low
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 40f64046f2a7efa32af8b43adbcf7349f43b6ec3
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/15/2021
ms.locfileid: "105703672"
---
# <a name="cd3dx12_tile_region_size-structure"></a><span data-ttu-id="78c1c-104">\_ \_ Структура размера области плитки CD3DX12 \_</span><span class="sxs-lookup"><span data-stu-id="78c1c-104">CD3DX12\_TILE\_REGION\_SIZE structure</span></span>

<span data-ttu-id="78c1c-105">Вспомогательная структура, позволяющая упростить инициализацию [**структуры \_ \_ \_ размера области мозаики D3D12**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_tile_region_size) .</span><span class="sxs-lookup"><span data-stu-id="78c1c-105">A helper structure to enable easy initialization of a [**D3D12\_TILE\_REGION\_SIZE**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_tile_region_size) structure.</span></span>

## <a name="syntax"></a><span data-ttu-id="78c1c-106">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="78c1c-106">Syntax</span></span>


```C++
struct CD3DX12_TILE_REGION_SIZE  : public D3D12_TILE_REGION_SIZE{
   CD3DX12_TILE_REGION_SIZE();
   explicit CD3DX12_TILE_REGION_SIZE(const D3D12_TILE_REGION_SIZE &o);
   CD3DX12_TILE_REGION_SIZE(UINT numTiles, BOOL useBox, UINT width, UINT16 height, UINT16 depth);
   operator const D3D12_TILE_REGION_SIZE&() const;
};
```



## <a name="members"></a><span data-ttu-id="78c1c-107">Члены</span><span class="sxs-lookup"><span data-stu-id="78c1c-107">Members</span></span>

<dl> <dt>

<span data-ttu-id="78c1c-108">**\_ \_ Размер области плитки CD3DX12 \_ ()**</span><span class="sxs-lookup"><span data-stu-id="78c1c-108">**CD3DX12\_TILE\_REGION\_SIZE()**</span></span>
</dt> <dd>

<span data-ttu-id="78c1c-109">Создает новый, неинициализированный экземпляр CD3DX12 \_ \_ размера области мозаики \_ .</span><span class="sxs-lookup"><span data-stu-id="78c1c-109">Creates a new, uninitialized, instance of a CD3DX12\_TILE\_REGION\_SIZE.</span></span>

</dd> <dt>

<span data-ttu-id="78c1c-110">**явный \_ \_ Размер области плитки CD3DX12 \_ (const D3D12 \_ \_ область плитки \_ Размер &o)**</span><span class="sxs-lookup"><span data-stu-id="78c1c-110">**explicit CD3DX12\_TILE\_REGION\_SIZE(const D3D12\_TILE\_REGION\_SIZE &o)**</span></span>
</dt> <dd>

<span data-ttu-id="78c1c-111">Создает новый экземпляр CD3DX12 \_ размера области мозаики \_ \_ , инициализируемый содержимым другой структуры [**\_ \_ \_ размера области плитки D3D12**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_tile_region_size) .</span><span class="sxs-lookup"><span data-stu-id="78c1c-111">Creates a new instance of a CD3DX12\_TILE\_REGION\_SIZE, initialized with the contents of another [**D3D12\_TILE\_REGION\_SIZE**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_tile_region_size) structure.</span></span>

</dd> <dt>

<span data-ttu-id="78c1c-112">**\_ \_ Размер области плитки CD3DX12 \_ (uint Нумтилес, bool УСЕБОКС, ширина uint, высота UINT16, глубина UInt16)**</span><span class="sxs-lookup"><span data-stu-id="78c1c-112">**CD3DX12\_TILE\_REGION\_SIZE(UINT numTiles, BOOL useBox, UINT width, UINT16 height, UINT16 depth)**</span></span>
</dt> <dd>

<span data-ttu-id="78c1c-113">Создает новый экземпляр \_ \_ размера области плитки CD3DX12 \_ , инициализируя следующие параметры:</span><span class="sxs-lookup"><span data-stu-id="78c1c-113">Creates a new instance of a CD3DX12\_TILE\_REGION\_SIZE, initializing the following parameters:</span></span>

<span data-ttu-id="78c1c-114">UINT Нумтилес</span><span class="sxs-lookup"><span data-stu-id="78c1c-114">UINT numTiles</span></span>

<span data-ttu-id="78c1c-115">BOOL Усебокс</span><span class="sxs-lookup"><span data-stu-id="78c1c-115">BOOL useBox</span></span>

<span data-ttu-id="78c1c-116">Ширина UINT</span><span class="sxs-lookup"><span data-stu-id="78c1c-116">UINT width</span></span>

<span data-ttu-id="78c1c-117">Высота UINT16</span><span class="sxs-lookup"><span data-stu-id="78c1c-117">UINT16 height</span></span>

<span data-ttu-id="78c1c-118">Глубина UINT16</span><span class="sxs-lookup"><span data-stu-id="78c1c-118">UINT16 depth</span></span>

</dd> <dt>

<span data-ttu-id="78c1c-119">**D3D12 \_ () размер области плитки оператора const константы \_ \_& () const**</span><span class="sxs-lookup"><span data-stu-id="78c1c-119">**operator const D3D12\_TILE\_REGION\_SIZE&() const**</span></span>
</dt> <dd>

<span data-ttu-id="78c1c-120">Определяет & оператором передачи по ссылке для типа родительской структуры.</span><span class="sxs-lookup"><span data-stu-id="78c1c-120">Defines the & pass-by-reference operator for the parent structure type.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="78c1c-121">Требования</span><span class="sxs-lookup"><span data-stu-id="78c1c-121">Requirements</span></span>



| <span data-ttu-id="78c1c-122">Требование</span><span class="sxs-lookup"><span data-stu-id="78c1c-122">Requirement</span></span> | <span data-ttu-id="78c1c-123">Значение</span><span class="sxs-lookup"><span data-stu-id="78c1c-123">Value</span></span> |
|-------------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="78c1c-124">Header</span><span class="sxs-lookup"><span data-stu-id="78c1c-124">Header</span></span><br/> | <dl> <span data-ttu-id="78c1c-125"><dt>D3dx12. h</dt></span><span class="sxs-lookup"><span data-stu-id="78c1c-125"><dt>D3dx12.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="78c1c-126">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="78c1c-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="78c1c-127">**\_ \_ Размер области плитки \_ D3D12**</span><span class="sxs-lookup"><span data-stu-id="78c1c-127">**D3D12\_TILE\_REGION\_SIZE**</span></span>](/windows/desktop/api/d3d12/ns-d3d12-d3d12_tile_region_size)
</dt> <dt>

[<span data-ttu-id="78c1c-128">Вспомогательные структуры для D3D12</span><span class="sxs-lookup"><span data-stu-id="78c1c-128">Helper Structures for D3D12</span></span>](helper-structures-for-d3d12.md)
</dt> </dl>

 

 





