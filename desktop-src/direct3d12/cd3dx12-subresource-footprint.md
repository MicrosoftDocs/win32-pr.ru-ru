---
title: Структура CD3DX12_SUBRESOURCE_FOOTPRINT (D3dx12. h)
description: Вспомогательная структура, позволяющая упростить инициализацию \_ структуры, занимаемой ПОДресурсом D3D12 \_ .
ms.assetid: 17266FB0-41B5-4A70-A896-206B54F5E76F
keywords:
- Структура CD3DX12_SUBRESOURCE_FOOTPRINT
topic_type:
- apiref
api_name:
- CD3DX12_SUBRESOURCE_FOOTPRINT
api_location:
- d3dx12.h
api_type:
- HeaderDef
ms.localizationpriority: low
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ab58e9a007d736222d9525d7a064456a1a9a7f14
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/15/2021
ms.locfileid: "105713502"
---
# <a name="cd3dx12_subresource_footprint-structure"></a><span data-ttu-id="dfbf3-104">\_Структура для ПОДресурсов CD3DX12 \_</span><span class="sxs-lookup"><span data-stu-id="dfbf3-104">CD3DX12\_SUBRESOURCE\_FOOTPRINT structure</span></span>

<span data-ttu-id="dfbf3-105">Вспомогательная структура, позволяющая упростить инициализацию структуры, [**\_ \_ ЗАНИМАЕМой подресурсом D3D12**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_subresource_footprint) .</span><span class="sxs-lookup"><span data-stu-id="dfbf3-105">A helper structure to enable easy initialization of a [**D3D12\_SUBRESOURCE\_FOOTPRINT**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_subresource_footprint) structure.</span></span>

## <a name="syntax"></a><span data-ttu-id="dfbf3-106">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="dfbf3-106">Syntax</span></span>


```C++
struct CD3DX12_SUBRESOURCE_FOOTPRINT  : public D3D12_SUBRESOURCE_FOOTPRINT{
   CD3DX12_SUBRESOURCE_FOOTPRINT();
   explicit CD3DX12_SUBRESOURCE_FOOTPRINT(const D3D12_SUBRESOURCE_FOOTPRINT &o);
   CD3DX12_SUBRESOURCE_FOOTPRINT(DXGI_FORMAT format, UINT width, UINT height, UINT depth, UINT rowPitch);
   explicit CD3DX12_SUBRESOURCE_FOOTPRINT(const D3D12_RESOURCE_DESC& resDesc, UINT rowPitch);
   operator const D3D12_SUBRESOURCE_FOOTPRINT&() const;
};
```



## <a name="members"></a><span data-ttu-id="dfbf3-107">Члены</span><span class="sxs-lookup"><span data-stu-id="dfbf3-107">Members</span></span>

<dl> <dt>

<span data-ttu-id="dfbf3-108">**\_Объем ПОДРЕСУРСОВ CD3DX12 \_ ()**</span><span class="sxs-lookup"><span data-stu-id="dfbf3-108">**CD3DX12\_SUBRESOURCE\_FOOTPRINT()**</span></span>
</dt> <dd>

<span data-ttu-id="dfbf3-109">Создает новый, неинициализированный экземпляр CD3DX12 \_ ПОДресурса \_ .</span><span class="sxs-lookup"><span data-stu-id="dfbf3-109">Creates a new, uninitialized, instance of a CD3DX12\_SUBRESOURCE\_FOOTPRINT.</span></span>

</dd> <dt>

<span data-ttu-id="dfbf3-110">**явное CD3DX12 \_ ПОДресурсного \_ пространства (D3D12 \_ \_ &o)**</span><span class="sxs-lookup"><span data-stu-id="dfbf3-110">**explicit CD3DX12\_SUBRESOURCE\_FOOTPRINT(const D3D12\_SUBRESOURCE\_FOOTPRINT &o)**</span></span>
</dt> <dd>

<span data-ttu-id="dfbf3-111">Создает новый экземпляр \_ ПОДресурса CD3DX12 \_ , который инициализируется с помощью содержимого другой структуры, [**\_ \_ занимаемой подресурсом D3D12**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_subresource_footprint) .</span><span class="sxs-lookup"><span data-stu-id="dfbf3-111">Creates a new instance of a CD3DX12\_SUBRESOURCE\_FOOTPRINT, initialized with the contents of another [**D3D12\_SUBRESOURCE\_FOOTPRINT**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_subresource_footprint) structure.</span></span>

</dd> <dt>

<span data-ttu-id="dfbf3-112">**CD3DX12 \_ подресурсов \_ ( \_ Формат формата DXGI, ширина UINT, высота UINT, глубина uint, uint ровпитч)**</span><span class="sxs-lookup"><span data-stu-id="dfbf3-112">**CD3DX12\_SUBRESOURCE\_FOOTPRINT(DXGI\_FORMAT format, UINT width, UINT height, UINT depth, UINT rowPitch)**</span></span>
</dt> <dd>

<span data-ttu-id="dfbf3-113">Создает новый экземпляр \_ ПОДресурса CD3DX12, который задается при \_ инициализации следующих параметров:</span><span class="sxs-lookup"><span data-stu-id="dfbf3-113">Creates a new instance of a CD3DX12\_SUBRESOURCE\_FOOTPRINT, initializing the following parameters:</span></span>

<span data-ttu-id="dfbf3-114">[**DXGI \_ Формат формата**](/windows/desktop/api/dxgiformat/ne-dxgiformat-dxgi_format)</span><span class="sxs-lookup"><span data-stu-id="dfbf3-114">[**DXGI\_FORMAT**](/windows/desktop/api/dxgiformat/ne-dxgiformat-dxgi_format) format</span></span>

<span data-ttu-id="dfbf3-115">Ширина UINT</span><span class="sxs-lookup"><span data-stu-id="dfbf3-115">UINT width</span></span>

<span data-ttu-id="dfbf3-116">Высота UINT</span><span class="sxs-lookup"><span data-stu-id="dfbf3-116">UINT height</span></span>

<span data-ttu-id="dfbf3-117">Глубина UINT</span><span class="sxs-lookup"><span data-stu-id="dfbf3-117">UINT depth</span></span>

<span data-ttu-id="dfbf3-118">UINT Ровпитч</span><span class="sxs-lookup"><span data-stu-id="dfbf3-118">UINT rowPitch</span></span>

</dd> <dt>

<span data-ttu-id="dfbf3-119">**явное CD3DX12 ресурсов \_ \_ (const D3D12 \_ Resource \_ DESC& ресдеск, uint ровпитч)**</span><span class="sxs-lookup"><span data-stu-id="dfbf3-119">**explicit CD3DX12\_SUBRESOURCE\_FOOTPRINT(const D3D12\_RESOURCE\_DESC& resDesc, UINT rowPitch)**</span></span>
</dt> <dd>

<span data-ttu-id="dfbf3-120">Создает новый экземпляр \_ ПОДресурса CD3DX12, который задается при \_ инициализации следующих параметров:</span><span class="sxs-lookup"><span data-stu-id="dfbf3-120">Creates a new instance of a CD3DX12\_SUBRESOURCE\_FOOTPRINT, initializing the following parameters:</span></span>

<span data-ttu-id="dfbf3-121">[**D3D12 \_ RESOURCE \_ DESC**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_resource_desc)& ресдеск</span><span class="sxs-lookup"><span data-stu-id="dfbf3-121">[**D3D12\_RESOURCE\_DESC**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_resource_desc)& resDesc</span></span>

<span data-ttu-id="dfbf3-122">UINT Ровпитч</span><span class="sxs-lookup"><span data-stu-id="dfbf3-122">UINT rowPitch</span></span>

</dd> <dt>

<span data-ttu-id="dfbf3-123">**\_константа оператора const D3D12 \_& () const**</span><span class="sxs-lookup"><span data-stu-id="dfbf3-123">**operator const D3D12\_SUBRESOURCE\_FOOTPRINT&() const**</span></span>
</dt> <dd>

<span data-ttu-id="dfbf3-124">Определяет & оператором передачи по ссылке для типа родительской структуры.</span><span class="sxs-lookup"><span data-stu-id="dfbf3-124">Defines the & pass-by-reference operator for the parent structure type.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="dfbf3-125">Требования</span><span class="sxs-lookup"><span data-stu-id="dfbf3-125">Requirements</span></span>



| <span data-ttu-id="dfbf3-126">Требование</span><span class="sxs-lookup"><span data-stu-id="dfbf3-126">Requirement</span></span> | <span data-ttu-id="dfbf3-127">Значение</span><span class="sxs-lookup"><span data-stu-id="dfbf3-127">Value</span></span> |
|-------------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="dfbf3-128">Header</span><span class="sxs-lookup"><span data-stu-id="dfbf3-128">Header</span></span><br/> | <dl> <span data-ttu-id="dfbf3-129"><dt>D3dx12. h</dt></span><span class="sxs-lookup"><span data-stu-id="dfbf3-129"><dt>D3dx12.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="dfbf3-130">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="dfbf3-130">See also</span></span>

<dl> <dt>

[<span data-ttu-id="dfbf3-131">**\_Объем ПОДРЕСУРСОВ \_ D3D12**</span><span class="sxs-lookup"><span data-stu-id="dfbf3-131">**D3D12\_SUBRESOURCE\_FOOTPRINT**</span></span>](/windows/desktop/api/d3d12/ns-d3d12-d3d12_subresource_footprint)
</dt> <dt>

[<span data-ttu-id="dfbf3-132">Вспомогательные структуры для D3D12</span><span class="sxs-lookup"><span data-stu-id="dfbf3-132">Helper Structures for D3D12</span></span>](helper-structures-for-d3d12.md)
</dt> </dl>

 

