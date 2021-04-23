---
title: Структура CD3DX12_TILED_RESOURCE_COORDINATE (D3dx12. h)
description: Вспомогательная структура, позволяющая легко инициализировать \_ структуру координат D3D12 мозаичного \_ ресурса \_ .
ms.assetid: B337ED04-E2C6-4B89-80F1-92C0854A6AF2
keywords:
- Структура CD3DX12_TILED_RESOURCE_COORDINATE
topic_type:
- apiref
api_name:
- CD3DX12_TILED_RESOURCE_COORDINATE
api_location:
- d3dx12.h
api_type:
- HeaderDef
ms.localizationpriority: low
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 281afeab8d1172e9cae749512612129dd001161b
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/15/2021
ms.locfileid: "105703666"
---
# <a name="cd3dx12_tiled_resource_coordinate-structure"></a><span data-ttu-id="52c2b-104">\_ \_ Структура координат мозаичного ресурса CD3DX12 \_</span><span class="sxs-lookup"><span data-stu-id="52c2b-104">CD3DX12\_TILED\_RESOURCE\_COORDINATE structure</span></span>

<span data-ttu-id="52c2b-105">Вспомогательная структура, позволяющая легко инициализировать структуру [**\_ \_ \_ координат D3D12 мозаичного ресурса**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_tiled_resource_coordinate) .</span><span class="sxs-lookup"><span data-stu-id="52c2b-105">A helper structure to enable easy initialization of a [**D3D12\_TILED\_RESOURCE\_COORDINATE**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_tiled_resource_coordinate) structure.</span></span>

## <a name="syntax"></a><span data-ttu-id="52c2b-106">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="52c2b-106">Syntax</span></span>


```C++
struct CD3DX12_TILED_RESOURCE_COORDINATE  : public D3D12_TILED_RESOURCE_COORDINATE{
   CD3DX12_TILED_RESOURCE_COORDINATE();
   explicit CD3DX12_TILED_RESOURCE_COORDINATE(const D3D12_TILED_RESOURCE_COORDINATE &o);
   CD3DX12_TILED_RESOURCE_COORDINATE(UINT x, UINT y, UINT z, UINT subresource);
   operator const D3D12_TILED_RESOURCE_COORDINATE&() const;
};
```



## <a name="members"></a><span data-ttu-id="52c2b-107">Члены</span><span class="sxs-lookup"><span data-stu-id="52c2b-107">Members</span></span>

<dl> <dt>

<span data-ttu-id="52c2b-108">**CD3DX12 \_ Мозаичное \_ \_ координата ресурса ()**</span><span class="sxs-lookup"><span data-stu-id="52c2b-108">**CD3DX12\_TILED\_RESOURCE\_COORDINATE()**</span></span>
</dt> <dd>

<span data-ttu-id="52c2b-109">Создает новый, неинициализированный экземпляр \_ координаты CD3DX12 мозаичного \_ ресурса \_ .</span><span class="sxs-lookup"><span data-stu-id="52c2b-109">Creates a new, uninitialized, instance of a CD3DX12\_TILED\_RESOURCE\_COORDINATE.</span></span>

</dd> <dt>

<span data-ttu-id="52c2b-110">**явная CD3DX12 \_ \_ координата мозаичного ресурса \_ (const D3D12 \_ мозаичная \_ \_ координата ресурса &o)**</span><span class="sxs-lookup"><span data-stu-id="52c2b-110">**explicit CD3DX12\_TILED\_RESOURCE\_COORDINATE(const D3D12\_TILED\_RESOURCE\_COORDINATE &o)**</span></span>
</dt> <dd>

<span data-ttu-id="52c2b-111">Создает новый экземпляр \_ \_ координатного мозаичного ресурса CD3DX12 \_ , инициализируемый с помощью содержимого другой [**D3D12 \_ мозаичной структуры \_ \_ координат ресурсов**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_tiled_resource_coordinate) .</span><span class="sxs-lookup"><span data-stu-id="52c2b-111">Creates a new instance of a CD3DX12\_TILED\_RESOURCE\_COORDINATE, initialized with the contents of another [**D3D12\_TILED\_RESOURCE\_COORDINATE**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_tiled_resource_coordinate) structure.</span></span>

</dd> <dt>

<span data-ttu-id="52c2b-112">**CD3DX12 \_ мозаичная \_ \_ координата ресурса (UINT x, UINT y, uint z, подресурсе uint)**</span><span class="sxs-lookup"><span data-stu-id="52c2b-112">**CD3DX12\_TILED\_RESOURCE\_COORDINATE(UINT x, UINT y, UINT z, UINT subresource)**</span></span>
</dt> <dd>

<span data-ttu-id="52c2b-113">Создает новый экземпляр \_ координат ресурсов мозаичного заполнения \_ CD3DX12 \_ , инициализируя следующие параметры:</span><span class="sxs-lookup"><span data-stu-id="52c2b-113">Creates a new instance of a CD3DX12\_TILED\_RESOURCE\_COORDINATE, initializing the following parameters:</span></span>

<span data-ttu-id="52c2b-114">UINT x</span><span class="sxs-lookup"><span data-stu-id="52c2b-114">UINT x</span></span>

<span data-ttu-id="52c2b-115">UINT y</span><span class="sxs-lookup"><span data-stu-id="52c2b-115">UINT y</span></span>

<span data-ttu-id="52c2b-116">UINT z</span><span class="sxs-lookup"><span data-stu-id="52c2b-116">UINT z</span></span>

<span data-ttu-id="52c2b-117">Подресурс UINT</span><span class="sxs-lookup"><span data-stu-id="52c2b-117">UINT subresource</span></span>

</dd> <dt>

<span data-ttu-id="52c2b-118">**Константа "оператор Const D3D12" \_ координата незаполненного \_ ресурса \_& () const**</span><span class="sxs-lookup"><span data-stu-id="52c2b-118">**operator const D3D12\_TILED\_RESOURCE\_COORDINATE&() const**</span></span>
</dt> <dd>

<span data-ttu-id="52c2b-119">Определяет & оператором передачи по ссылке для типа родительской структуры.</span><span class="sxs-lookup"><span data-stu-id="52c2b-119">Defines the & pass-by-reference operator for the parent structure type.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="52c2b-120">Требования</span><span class="sxs-lookup"><span data-stu-id="52c2b-120">Requirements</span></span>



| <span data-ttu-id="52c2b-121">Требование</span><span class="sxs-lookup"><span data-stu-id="52c2b-121">Requirement</span></span> | <span data-ttu-id="52c2b-122">Значение</span><span class="sxs-lookup"><span data-stu-id="52c2b-122">Value</span></span> |
|-------------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="52c2b-123">Header</span><span class="sxs-lookup"><span data-stu-id="52c2b-123">Header</span></span><br/> | <dl> <span data-ttu-id="52c2b-124"><dt>D3dx12. h</dt></span><span class="sxs-lookup"><span data-stu-id="52c2b-124"><dt>D3dx12.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="52c2b-125">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="52c2b-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="52c2b-126">**\_ \_ Координата мозаичного ресурса D3D12 \_**</span><span class="sxs-lookup"><span data-stu-id="52c2b-126">**D3D12\_TILED\_RESOURCE\_COORDINATE**</span></span>](/windows/desktop/api/d3d12/ns-d3d12-d3d12_tiled_resource_coordinate)
</dt> <dt>

[<span data-ttu-id="52c2b-127">Вспомогательные структуры для D3D12</span><span class="sxs-lookup"><span data-stu-id="52c2b-127">Helper Structures for D3D12</span></span>](helper-structures-for-d3d12.md)
</dt> </dl>

 

 





