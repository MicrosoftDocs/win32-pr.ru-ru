---
title: Структура CD3DX12_TEXTURE_COPY_LOCATION (D3dx12. h)
description: Вспомогательная структура, позволяющая легко инициализировать \_ \_ структуру расположения копирования текстуры D3D12 \_ .
ms.assetid: 8BA93729-2FFB-4C09-88B0-779049BAF385
keywords:
- Структура CD3DX12_TEXTURE_COPY_LOCATION
topic_type:
- apiref
api_name:
- CD3DX12_TEXTURE_COPY_LOCATION
api_location:
- d3dx12.h
api_type:
- HeaderDef
ms.localizationpriority: low
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f5143137f92e38662660588dd89a527f59644126
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/15/2021
ms.locfileid: "105703673"
---
# <a name="cd3dx12_texture_copy_location-structure"></a><span data-ttu-id="93471-104">\_ \_ Структура расположения для копирования текстур CD3DX12 \_</span><span class="sxs-lookup"><span data-stu-id="93471-104">CD3DX12\_TEXTURE\_COPY\_LOCATION structure</span></span>

<span data-ttu-id="93471-105">Вспомогательная структура, позволяющая легко инициализировать структуру [**\_ \_ \_ расположения копирования текстуры D3D12**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_texture_copy_location) .</span><span class="sxs-lookup"><span data-stu-id="93471-105">A helper structure to enable easy initialization of a [**D3D12\_TEXTURE\_COPY\_LOCATION**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_texture_copy_location) structure.</span></span>

## <a name="syntax"></a><span data-ttu-id="93471-106">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="93471-106">Syntax</span></span>


```C++
struct CD3DX12_TEXTURE_COPY_LOCATION  : public D3D12_TEXTURE_COPY_LOCATION{
   CD3DX12_TEXTURE_COPY_LOCATION();
   explicit CD3DX12_TEXTURE_COPY_LOCATION(const D3D12_TEXTURE_COPY_LOCATION &o);
   CD3DX12_TEXTURE_COPY_LOCATION(ID3D12Resource* pRes);
   CD3DX12_TEXTURE_COPY_LOCATION(ID3D12Resource* pRes, D3D12_PLACED_SUBRESOURCE_FOOTPRINT const& Footprint);
   CD3DX12_TEXTURE_COPY_LOCATION(ID3D12Resource* pRes, UINT Sub);
};
```



## <a name="members"></a><span data-ttu-id="93471-107">Члены</span><span class="sxs-lookup"><span data-stu-id="93471-107">Members</span></span>

<dl> <dt>

<span data-ttu-id="93471-108">**\_ \_ Расположение копирования текстуры CD3DX12 \_ ()**</span><span class="sxs-lookup"><span data-stu-id="93471-108">**CD3DX12\_TEXTURE\_COPY\_LOCATION()**</span></span>
</dt> <dd>

<span data-ttu-id="93471-109">Создает новый, неинициализированный экземпляр \_ расположения для копирования текстуры CD3DX12 \_ \_ .</span><span class="sxs-lookup"><span data-stu-id="93471-109">Creates a new, uninitialized, instance of a CD3DX12\_TEXTURE\_COPY\_LOCATION.</span></span>

</dd> <dt>

<span data-ttu-id="93471-110">**явное \_ \_ Расположение копии текстуры CD3DX12 \_ (константа D3D12 \_ \_ Расположение копирования текстуры \_ &o)**</span><span class="sxs-lookup"><span data-stu-id="93471-110">**explicit CD3DX12\_TEXTURE\_COPY\_LOCATION(const D3D12\_TEXTURE\_COPY\_LOCATION &o)**</span></span>
</dt> <dd>

<span data-ttu-id="93471-111">Создает новый экземпляр \_ расположения для копирования текстуры CD3DX12 \_ \_ , который инициализируется с содержимым другой структуры [**\_ \_ \_ расположения D3D12 текстуры**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_texture_copy_location) .</span><span class="sxs-lookup"><span data-stu-id="93471-111">Creates a new instance of a CD3DX12\_TEXTURE\_COPY\_LOCATION, initialized with the contents of another [**D3D12\_TEXTURE\_COPY\_LOCATION**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_texture_copy_location) structure.</span></span>

</dd> <dt>

<span data-ttu-id="93471-112">**\_ \_ Расположение копии текстуры CD3DX12 \_ (ID3D12Resource \* прес)**</span><span class="sxs-lookup"><span data-stu-id="93471-112">**CD3DX12\_TEXTURE\_COPY\_LOCATION(ID3D12Resource\* pRes)**</span></span>
</dt> <dd>

<span data-ttu-id="93471-113">Создает новый экземпляр \_ расположения для копирования текстуры CD3DX12 \_ \_ , инициализируя следующие параметры:</span><span class="sxs-lookup"><span data-stu-id="93471-113">Creates a new instance of a CD3DX12\_TEXTURE\_COPY\_LOCATION, initializing the following parameters:</span></span>

<span data-ttu-id="93471-114">[**ID3D12Resource**](/windows/desktop/api/d3d12/nn-d3d12-id3d12resource) \* прес</span><span class="sxs-lookup"><span data-stu-id="93471-114">[**ID3D12Resource**](/windows/desktop/api/d3d12/nn-d3d12-id3d12resource)\* pRes</span></span>

</dd> <dt>

<span data-ttu-id="93471-115">**\_Расположение для \_ копирования текстур CD3DX12 \_ (ID3D12RESOURCE \* прес, D3D12 \_ размещенного в \_ подресурсе \_& объемы памяти)**</span><span class="sxs-lookup"><span data-stu-id="93471-115">**CD3DX12\_TEXTURE\_COPY\_LOCATION(ID3D12Resource\* pRes, D3D12\_PLACED\_SUBRESOURCE\_FOOTPRINT const& Footprint)**</span></span>
</dt> <dd>

<span data-ttu-id="93471-116">Создает новый экземпляр \_ расположения для копирования текстуры CD3DX12 \_ \_ , инициализируя следующие параметры:</span><span class="sxs-lookup"><span data-stu-id="93471-116">Creates a new instance of a CD3DX12\_TEXTURE\_COPY\_LOCATION, initializing the following parameters:</span></span>

<span data-ttu-id="93471-117">[**ID3D12Resource**](/windows/desktop/api/d3d12/nn-d3d12-id3d12resource) \* прес</span><span class="sxs-lookup"><span data-stu-id="93471-117">[**ID3D12Resource**](/windows/desktop/api/d3d12/nn-d3d12-id3d12resource)\* pRes</span></span>

<span data-ttu-id="93471-118">[**D3D12 \_ При РАЗМЕЩЕНии в \_ ПОДресурсе \_**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_placed_subresource_footprint)& объемы константы</span><span class="sxs-lookup"><span data-stu-id="93471-118">[**D3D12\_PLACED\_SUBRESOURCE\_FOOTPRINT**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_placed_subresource_footprint) const& Footprint</span></span>

</dd> <dt>

<span data-ttu-id="93471-119">**\_ \_ Расположение копии текстуры CD3DX12 \_ (ID3D12Resource \* прес, подсистема uint)**</span><span class="sxs-lookup"><span data-stu-id="93471-119">**CD3DX12\_TEXTURE\_COPY\_LOCATION(ID3D12Resource\* pRes, UINT Sub)**</span></span>
</dt> <dd>

<span data-ttu-id="93471-120">Создает новый экземпляр \_ расположения для копирования текстуры CD3DX12 \_ \_ , инициализируя следующие параметры:</span><span class="sxs-lookup"><span data-stu-id="93471-120">Creates a new instance of a CD3DX12\_TEXTURE\_COPY\_LOCATION, initializing the following parameters:</span></span>

<span data-ttu-id="93471-121">[**ID3D12Resource**](/windows/desktop/api/d3d12/nn-d3d12-id3d12resource) \* прес</span><span class="sxs-lookup"><span data-stu-id="93471-121">[**ID3D12Resource**](/windows/desktop/api/d3d12/nn-d3d12-id3d12resource)\* pRes</span></span>

<span data-ttu-id="93471-122">Подсистема UINT</span><span class="sxs-lookup"><span data-stu-id="93471-122">UINT Sub</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="93471-123">Требования</span><span class="sxs-lookup"><span data-stu-id="93471-123">Requirements</span></span>



| <span data-ttu-id="93471-124">Требование</span><span class="sxs-lookup"><span data-stu-id="93471-124">Requirement</span></span> | <span data-ttu-id="93471-125">Значение</span><span class="sxs-lookup"><span data-stu-id="93471-125">Value</span></span> |
|-------------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="93471-126">Header</span><span class="sxs-lookup"><span data-stu-id="93471-126">Header</span></span><br/> | <dl> <span data-ttu-id="93471-127"><dt>D3dx12. h</dt></span><span class="sxs-lookup"><span data-stu-id="93471-127"><dt>D3dx12.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="93471-128">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="93471-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="93471-129">**\_ \_ Расположение копии текстуры \_ D3D12**</span><span class="sxs-lookup"><span data-stu-id="93471-129">**D3D12\_TEXTURE\_COPY\_LOCATION**</span></span>](/windows/desktop/api/d3d12/ns-d3d12-d3d12_texture_copy_location)
</dt> <dt>

[<span data-ttu-id="93471-130">Вспомогательные структуры для D3D12</span><span class="sxs-lookup"><span data-stu-id="93471-130">Helper Structures for D3D12</span></span>](helper-structures-for-d3d12.md)
</dt> </dl>

 

 





