---
title: Структура CD3DX12_RESOURCE_ALLOCATION_INFO (D3dx12. h)
description: Вспомогательная структура, позволяющая легко инициализировать \_ \_ структуру сведений о выделении ресурсов D3D12 \_ .
ms.assetid: 81FC8D0E-2C15-42D3-9E06-1FE193F707C6
keywords:
- Структура CD3DX12_RESOURCE_ALLOCATION_INFO
topic_type:
- apiref
api_name:
- CD3DX12_RESOURCE_ALLOCATION_INFO
api_location:
- d3dx12.h
api_type:
- HeaderDef
ms.localizationpriority: low
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 08542c7460b2fadf381f85dc271167258e31fb46
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/15/2021
ms.locfileid: "105713514"
---
# <a name="cd3dx12_resource_allocation_info-structure"></a><span data-ttu-id="7c8cf-104">\_ \_ Структура сведений о выделении ресурсов CD3DX12 \_</span><span class="sxs-lookup"><span data-stu-id="7c8cf-104">CD3DX12\_RESOURCE\_ALLOCATION\_INFO structure</span></span>

<span data-ttu-id="7c8cf-105">Вспомогательная структура, позволяющая легко инициализировать структуру [**\_ \_ \_ сведений о выделении ресурсов D3D12**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_resource_allocation_info) .</span><span class="sxs-lookup"><span data-stu-id="7c8cf-105">A helper structure to enable easy initialization of a [**D3D12\_RESOURCE\_ALLOCATION\_INFO**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_resource_allocation_info) structure.</span></span>

## <a name="syntax"></a><span data-ttu-id="7c8cf-106">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="7c8cf-106">Syntax</span></span>


```C++
struct CD3DX12_RESOURCE_ALLOCATION_INFO  : public D3D12_RESOURCE_ALLOCATION_INFO{
   CD3DX12_RESOURCE_ALLOCATION_INFO();
   explicit CD3DX12_RESOURCE_ALLOCATION_INFO(const D3D12_RESOURCE_ALLOCATION_INFO& o);
   CD3DX12_RESOURCE_ALLOCATION_INFO(UINT64 size, UINT64 alignment);
   operator const D3D12_RESOURCE_ALLOCATION_INFO&() const;
};
```



## <a name="members"></a><span data-ttu-id="7c8cf-107">Члены</span><span class="sxs-lookup"><span data-stu-id="7c8cf-107">Members</span></span>

<dl> <dt>

<span data-ttu-id="7c8cf-108">**\_ \_ Сведения о выделении ресурсов CD3DX12 \_ ()**</span><span class="sxs-lookup"><span data-stu-id="7c8cf-108">**CD3DX12\_RESOURCE\_ALLOCATION\_INFO()**</span></span>
</dt> <dd>

<span data-ttu-id="7c8cf-109">Создает новый, неинициализированный экземпляр \_ \_ сведений о выделении ресурсов CD3DX12 \_ .</span><span class="sxs-lookup"><span data-stu-id="7c8cf-109">Creates a new, uninitialized, instance of a CD3DX12\_RESOURCE\_ALLOCATION\_INFO.</span></span>

</dd> <dt>

<span data-ttu-id="7c8cf-110">**явные \_ \_ сведения о выделении ресурсов CD3DX12 \_ (const D3D12 \_ \_ сведения о выделении ресурсов \_& o)**</span><span class="sxs-lookup"><span data-stu-id="7c8cf-110">**explicit CD3DX12\_RESOURCE\_ALLOCATION\_INFO(const D3D12\_RESOURCE\_ALLOCATION\_INFO& o)**</span></span>
</dt> <dd>

<span data-ttu-id="7c8cf-111">Создает новый экземпляр \_ \_ сведений о выделении ресурсов CD3DX12 \_ , инициализируемый с помощью содержимого другой структуры [**\_ \_ \_ сведений о выделении ресурсов D3D12**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_resource_allocation_info) .</span><span class="sxs-lookup"><span data-stu-id="7c8cf-111">Creates a new instance of a CD3DX12\_RESOURCE\_ALLOCATION\_INFO, initialized with the contents of another [**D3D12\_RESOURCE\_ALLOCATION\_INFO**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_resource_allocation_info) structure.</span></span>

</dd> <dt>

<span data-ttu-id="7c8cf-112">**\_ \_ Сведения о выделении ресурсов CD3DX12 \_ (размер UINT64, выравнивание UInt64)**</span><span class="sxs-lookup"><span data-stu-id="7c8cf-112">**CD3DX12\_RESOURCE\_ALLOCATION\_INFO(UINT64 size, UINT64 alignment)**</span></span>
</dt> <dd>

<span data-ttu-id="7c8cf-113">Создает новый экземпляр \_ \_ сведений о выделении ресурсов CD3DX12 \_ , инициализируя следующие параметры:</span><span class="sxs-lookup"><span data-stu-id="7c8cf-113">Creates a new instance of a CD3DX12\_RESOURCE\_ALLOCATION\_INFO, initializing the following parameters:</span></span>

<span data-ttu-id="7c8cf-114">Размер UINT64</span><span class="sxs-lookup"><span data-stu-id="7c8cf-114">UINT64 size</span></span>

<span data-ttu-id="7c8cf-115">Выравнивание UINT64</span><span class="sxs-lookup"><span data-stu-id="7c8cf-115">UINT64 alignment</span></span>

</dd> <dt>

<span data-ttu-id="7c8cf-116">**Квалификатор operator const \_ D3D12 \_ сведения о выделении ресурсов \_& () const**</span><span class="sxs-lookup"><span data-stu-id="7c8cf-116">**operator const D3D12\_RESOURCE\_ALLOCATION\_INFO&() const**</span></span>
</dt> <dd>

<span data-ttu-id="7c8cf-117">Определяет & оператором передачи по ссылке для типа родительской структуры.</span><span class="sxs-lookup"><span data-stu-id="7c8cf-117">Defines the & pass-by-reference operator for the parent structure type.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="7c8cf-118">Требования</span><span class="sxs-lookup"><span data-stu-id="7c8cf-118">Requirements</span></span>



| <span data-ttu-id="7c8cf-119">Требование</span><span class="sxs-lookup"><span data-stu-id="7c8cf-119">Requirement</span></span> | <span data-ttu-id="7c8cf-120">Значение</span><span class="sxs-lookup"><span data-stu-id="7c8cf-120">Value</span></span> |
|-------------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="7c8cf-121">Header</span><span class="sxs-lookup"><span data-stu-id="7c8cf-121">Header</span></span><br/> | <dl> <span data-ttu-id="7c8cf-122"><dt>D3dx12. h</dt></span><span class="sxs-lookup"><span data-stu-id="7c8cf-122"><dt>D3dx12.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="7c8cf-123">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="7c8cf-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="7c8cf-124">**\_ \_ Сведения о выделении ресурсов D3D12 \_**</span><span class="sxs-lookup"><span data-stu-id="7c8cf-124">**D3D12\_RESOURCE\_ALLOCATION\_INFO**</span></span>](/windows/desktop/api/d3d12/ns-d3d12-d3d12_resource_allocation_info)
</dt> <dt>

[<span data-ttu-id="7c8cf-125">Вспомогательные структуры для D3D12</span><span class="sxs-lookup"><span data-stu-id="7c8cf-125">Helper Structures for D3D12</span></span>](helper-structures-for-d3d12.md)
</dt> </dl>

 

 





