---
title: Структура CD3DX12_HEAP_DESC (D3dx12. h)
description: Вспомогательная структура, позволяющая упростить инициализацию структуры D3D12 в \_ куче \_ .
ms.assetid: 38E0BA60-2BB0-4AC1-870A-10AB16E4C6E6
keywords:
- Структура CD3DX12_HEAP_DESC
topic_type:
- apiref
api_name:
- CD3DX12_HEAP_DESC
api_location:
- d3dx12.h
api_type:
- HeaderDef
ms.localizationpriority: low
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ae5b2537d2571355f26c46f03aed3489fb2b6069
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/15/2021
ms.locfileid: "105703678"
---
# <a name="cd3dx12_heap_desc-structure"></a><span data-ttu-id="f844d-104">\_Структура CD3DX12 кучи \_</span><span class="sxs-lookup"><span data-stu-id="f844d-104">CD3DX12\_HEAP\_DESC structure</span></span>

<span data-ttu-id="f844d-105">Вспомогательная структура, позволяющая упростить инициализацию структуры [**D3D12 в \_ куче \_**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_heap_desc) .</span><span class="sxs-lookup"><span data-stu-id="f844d-105">A helper structure to enable easy initialization of a [**D3D12\_HEAP\_DESC**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_heap_desc) structure.</span></span>

## <a name="syntax"></a><span data-ttu-id="f844d-106">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="f844d-106">Syntax</span></span>


```C++
struct CD3DX12_HEAP_DESC  : public D3D12_HEAP_DESC{
   CD3DX12_HEAP_DESC();
   explicit CD3DX12_HEAP_DESC(const D3D12_HEAP_DESC &o);
   CD3DX12_HEAP_DESC(UINT64 size, D3D12_HEAP_PROPERTIES properties, UINT64 alignment = 0, D3D12_HEAP_FLAGS flags = D3D12_HEAP_FLAG_NONE);
   CD3DX12_HEAP_DESC(UINT64 size, D3D12_HEAP_TYPE type, UINT64 alignment = 0, D3D12_HEAP_FLAGS flags = D3D12_HEAP_FLAG_NONE);
   CD3DX12_HEAP_DESC(UINT64 size, D3D12_CPU_PAGE_PROPERTY cpuPageProperty, D3D12_MEMORY_POOL memoryPoolPreference, UINT64 alignment = 0, D3D12_HEAP_FLAGS flags = D3D12_HEAP_FLAG_NONE);
   CD3DX12_HEAP_DESC(const D3D12_RESOURCE_ALLOCATION_INFO& resAllocInfo, D3D12_HEAP_PROPERTIES properties, D3D12_HEAP_FLAGS flags = D3D12_HEAP_FLAG_NONE);
   CD3DX12_HEAP_DESC(const D3D12_RESOURCE_ALLOCATION_INFO& resAllocInfo, D3D12_HEAP_TYPE type, D3D12_HEAP_FLAGS flags = D3D12_HEAP_FLAG_NONE);
   CD3DX12_HEAP_DESC(const D3D12_RESOURCE_ALLOCATION_INFO& resAllocInfo, D3D12_CPU_PAGE_PROPERTY cpuPageProperty, D3D12_MEMORY_POOL memoryPoolPreference, D3D12_HEAP_FLAGS flags = D3D12_HEAP_FLAG_NONE);
   operator const D3D12_HEAP_DESC&() const;
};
```



## <a name="members"></a><span data-ttu-id="f844d-107">Члены</span><span class="sxs-lookup"><span data-stu-id="f844d-107">Members</span></span>

<dl> <dt>

<span data-ttu-id="f844d-108">**CD3DX12 \_ heap \_ DESC ()**</span><span class="sxs-lookup"><span data-stu-id="f844d-108">**CD3DX12\_HEAP\_DESC()**</span></span>
</dt> <dd>

<span data-ttu-id="f844d-109">Создает новый, не инициализированный экземпляр CD3DX12 \_ кучи \_ DESC.</span><span class="sxs-lookup"><span data-stu-id="f844d-109">Creates a new, uninitialized, instance of a CD3DX12\_HEAP\_DESC.</span></span>

</dd> <dt>

<span data-ttu-id="f844d-110">**явная \_ куча CD3DX12 \_ DESC (const D3D12 \_ heap \_ DESC &o)**</span><span class="sxs-lookup"><span data-stu-id="f844d-110">**explicit CD3DX12\_HEAP\_DESC(const D3D12\_HEAP\_DESC &o)**</span></span>
</dt> <dd>

<span data-ttu-id="f844d-111">Создает новый экземпляр CD3DX12 \_ кучи \_ DESC, инициализируемый с содержимым другой структуры [**\_ кучи \_ D3D12**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_heap_desc) .</span><span class="sxs-lookup"><span data-stu-id="f844d-111">Creates a new instance of a CD3DX12\_HEAP\_DESC, initialized with the contents of another [**D3D12\_HEAP\_DESC**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_heap_desc) structure.</span></span>

</dd> <dt>

<span data-ttu-id="f844d-112">**CD3DX12 \_ heap \_ DESC (размер UInt64, свойства \_ кучи D3D12 \_ , выравнивание UINT64 = 0, \_ \_ Флаги флагов D3D12 кучи = \_ D3D12 \_ куча \_ None)**</span><span class="sxs-lookup"><span data-stu-id="f844d-112">**CD3DX12\_HEAP\_DESC(UINT64 size, D3D12\_HEAP\_PROPERTIES properties, UINT64 alignment = 0, D3D12\_HEAP\_FLAGS flags = D3D12\_HEAP\_FLAG\_NONE)**</span></span>
</dt> <dd>

<span data-ttu-id="f844d-113">Создает новый экземпляр CD3DX12 \_ кучи \_ DESC, инициализируя следующие параметры:</span><span class="sxs-lookup"><span data-stu-id="f844d-113">Creates a new instance of a CD3DX12\_HEAP\_DESC, initializing the following parameters:</span></span>

<span data-ttu-id="f844d-114">Размер UINT64</span><span class="sxs-lookup"><span data-stu-id="f844d-114">UINT64 size</span></span>

<span data-ttu-id="f844d-115">[**D3D12 \_ Свойства \_ кучи**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_heap_properties)</span><span class="sxs-lookup"><span data-stu-id="f844d-115">[**D3D12\_HEAP\_PROPERTIES**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_heap_properties) properties</span></span>

<span data-ttu-id="f844d-116">участие UINT64 выравнивание = 0</span><span class="sxs-lookup"><span data-stu-id="f844d-116">(opt) UINT64 alignment = 0</span></span>

<span data-ttu-id="f844d-117">участие [**D3D12 \_ Флаги \_ флагов кучи**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_heap_flags) = D3D12 \_ куча \_ \_ нет</span><span class="sxs-lookup"><span data-stu-id="f844d-117">(opt) [**D3D12\_HEAP\_FLAGS**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_heap_flags) flags = D3D12\_HEAP\_FLAG\_NONE</span></span>

</dd> <dt>

<span data-ttu-id="f844d-118">**CD3DX12 \_ heap \_ DESC (размер UInt64, \_ \_ тип типа КУЧИ D3D12, выравнивание UINT64 = 0, D3D12 флаги { \_ heap \_ = \_ D3D12 \_ кучи \_ None)**</span><span class="sxs-lookup"><span data-stu-id="f844d-118">**CD3DX12\_HEAP\_DESC(UINT64 size, D3D12\_HEAP\_TYPE type, UINT64 alignment = 0, D3D12\_HEAP\_FLAGS flags = D3D12\_HEAP\_FLAG\_NONE)**</span></span>
</dt> <dd>

<span data-ttu-id="f844d-119">Создает новый экземпляр CD3DX12 \_ кучи \_ DESC, инициализируя следующие параметры:</span><span class="sxs-lookup"><span data-stu-id="f844d-119">Creates a new instance of a CD3DX12\_HEAP\_DESC, initializing the following parameters:</span></span>

<span data-ttu-id="f844d-120">Размер UINT64</span><span class="sxs-lookup"><span data-stu-id="f844d-120">UINT64 size</span></span>

<span data-ttu-id="f844d-121">[**D3D12 \_ Тип \_ типа кучи**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_heap_type)</span><span class="sxs-lookup"><span data-stu-id="f844d-121">[**D3D12\_HEAP\_TYPE**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_heap_type) type</span></span>

<span data-ttu-id="f844d-122">участие UINT64 выравнивание = 0</span><span class="sxs-lookup"><span data-stu-id="f844d-122">(opt) UINT64 alignment = 0</span></span>

<span data-ttu-id="f844d-123">участие [**D3D12 \_ Флаги \_ флагов кучи**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_heap_flags) = D3D12 \_ куча \_ \_ нет</span><span class="sxs-lookup"><span data-stu-id="f844d-123">(opt) [**D3D12\_HEAP\_FLAGS**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_heap_flags) flags = D3D12\_HEAP\_FLAG\_NONE</span></span>

</dd> <dt>

<span data-ttu-id="f844d-124">**CD3DX12 \_ heap \_ DESC (размер UINT64, \_ \_ свойство страницы ЦП D3D12 \_ Кпупажепроперти, D3D12 \_ \_ пула памяти МЕМОРИПУЛПРЕФЕРЕНЦЕ, выравнивание UINT64 = 0, D3D12 флаги \_ flags в куче \_ = D3D12 \_ \_ флаг кучи \_ None)**</span><span class="sxs-lookup"><span data-stu-id="f844d-124">**CD3DX12\_HEAP\_DESC(UINT64 size, D3D12\_CPU\_PAGE\_PROPERTY cpuPageProperty, D3D12\_MEMORY\_POOL memoryPoolPreference, UINT64 alignment = 0, D3D12\_HEAP\_FLAGS flags = D3D12\_HEAP\_FLAG\_NONE)**</span></span>
</dt> <dd>

<span data-ttu-id="f844d-125">Создает новый экземпляр CD3DX12 \_ кучи \_ DESC, инициализируя следующие параметры:</span><span class="sxs-lookup"><span data-stu-id="f844d-125">Creates a new instance of a CD3DX12\_HEAP\_DESC, initializing the following parameters:</span></span>

<span data-ttu-id="f844d-126">Размер UINT64</span><span class="sxs-lookup"><span data-stu-id="f844d-126">UINT64 size</span></span>

<span data-ttu-id="f844d-127">[**D3D12 \_ \_ \_ Свойство страницы ЦП**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_cpu_page_property) кпупажепроперти</span><span class="sxs-lookup"><span data-stu-id="f844d-127">[**D3D12\_CPU\_PAGE\_PROPERTY**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_cpu_page_property) cpuPageProperty</span></span>

<span data-ttu-id="f844d-128">[**D3D12 \_ Меморипулпреференце \_ пула памяти**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_memory_pool)</span><span class="sxs-lookup"><span data-stu-id="f844d-128">[**D3D12\_MEMORY\_POOL**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_memory_pool) memoryPoolPreference</span></span>

<span data-ttu-id="f844d-129">участие UINT64 выравнивание = 0</span><span class="sxs-lookup"><span data-stu-id="f844d-129">(opt) UINT64 alignment = 0</span></span>

<span data-ttu-id="f844d-130">участие [**D3D12 \_ Флаги \_ флагов кучи**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_heap_flags) = D3D12 \_ куча \_ \_ нет</span><span class="sxs-lookup"><span data-stu-id="f844d-130">(opt) [**D3D12\_HEAP\_FLAGS**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_heap_flags) flags = D3D12\_HEAP\_FLAG\_NONE</span></span>

</dd> <dt>

<span data-ttu-id="f844d-131">**CD3DX12 \_ heap \_ DESC (const D3D12 \_ \_ сведения о выделении ресурсов \_& ресаллоЦинфо, СВОЙСТВАх D3D12 \_ кучи, D3D12 флаги \_ \_ \_ флагов кучи = D3D12 \_ heap \_ флаг \_ None)**</span><span class="sxs-lookup"><span data-stu-id="f844d-131">**CD3DX12\_HEAP\_DESC(const D3D12\_RESOURCE\_ALLOCATION\_INFO& resAllocInfo, D3D12\_HEAP\_PROPERTIES properties, D3D12\_HEAP\_FLAGS flags = D3D12\_HEAP\_FLAG\_NONE)**</span></span>
</dt> <dd>

<span data-ttu-id="f844d-132">Создает новый экземпляр CD3DX12 \_ кучи \_ DESC, инициализируя следующие параметры:</span><span class="sxs-lookup"><span data-stu-id="f844d-132">Creates a new instance of a CD3DX12\_HEAP\_DESC, initializing the following parameters:</span></span>

<span data-ttu-id="f844d-133">[**D3D12 \_ \_ \_ Сведения о выделении ресурсов**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_resource_allocation_info)& ресаллоЦинфо</span><span class="sxs-lookup"><span data-stu-id="f844d-133">[**D3D12\_RESOURCE\_ALLOCATION\_INFO**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_resource_allocation_info)& resAllocInfo</span></span>

<span data-ttu-id="f844d-134">[**D3D12 \_ Свойства \_ кучи**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_heap_properties)</span><span class="sxs-lookup"><span data-stu-id="f844d-134">[**D3D12\_HEAP\_PROPERTIES**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_heap_properties) properties</span></span>

<span data-ttu-id="f844d-135">участие [**D3D12 \_ Флаги \_ флагов кучи**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_heap_flags) = D3D12 \_ куча \_ \_ нет</span><span class="sxs-lookup"><span data-stu-id="f844d-135">(opt) [**D3D12\_HEAP\_FLAGS**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_heap_flags) flags = D3D12\_HEAP\_FLAG\_NONE</span></span>

</dd> <dt>

<span data-ttu-id="f844d-136">**CD3DX12 \_ heap \_ DESC (const D3D12 \_ \_ сведения о выделении ресурсов \_& РЕСАЛЛОЦИНФО, тип \_ типа кучи D3D12 \_ , D3D12 флаги \_ \_ флагов кучи = D3D12 \_ heap \_ флаг \_ None)**</span><span class="sxs-lookup"><span data-stu-id="f844d-136">**CD3DX12\_HEAP\_DESC(const D3D12\_RESOURCE\_ALLOCATION\_INFO& resAllocInfo, D3D12\_HEAP\_TYPE type, D3D12\_HEAP\_FLAGS flags = D3D12\_HEAP\_FLAG\_NONE)**</span></span>
</dt> <dd>

<span data-ttu-id="f844d-137">Создает новый экземпляр CD3DX12 \_ кучи \_ DESC, инициализируя следующие параметры:</span><span class="sxs-lookup"><span data-stu-id="f844d-137">Creates a new instance of a CD3DX12\_HEAP\_DESC, initializing the following parameters:</span></span>

<span data-ttu-id="f844d-138">[**D3D12 \_ \_ \_ Сведения о выделении ресурсов**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_resource_allocation_info)& ресаллоЦинфо</span><span class="sxs-lookup"><span data-stu-id="f844d-138">[**D3D12\_RESOURCE\_ALLOCATION\_INFO**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_resource_allocation_info)& resAllocInfo</span></span>

<span data-ttu-id="f844d-139">[**D3D12 \_ Тип \_ типа кучи**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_heap_type)</span><span class="sxs-lookup"><span data-stu-id="f844d-139">[**D3D12\_HEAP\_TYPE**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_heap_type) type</span></span>

<span data-ttu-id="f844d-140">участие [**D3D12 \_ Флаги \_ флагов кучи**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_heap_flags) = D3D12 \_ куча \_ \_ нет</span><span class="sxs-lookup"><span data-stu-id="f844d-140">(opt) [**D3D12\_HEAP\_FLAGS**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_heap_flags) flags = D3D12\_HEAP\_FLAG\_NONE</span></span>

</dd> <dt>

<span data-ttu-id="f844d-141">**CD3DX12 \_ heap \_ DESC (const D3D12 \_ \_ сведения о выделении ресурсов \_& ресаллоЦинфо, D3D12 \_ \_ Свойства страницы ЦП \_ кпупажепроперти, D3D12 \_ пула памяти меморипулпреференце, флаги флагов D3D12 кучи \_ , \_ \_ flags = D3D12 \_ heap \_ флаг \_ None)**</span><span class="sxs-lookup"><span data-stu-id="f844d-141">**CD3DX12\_HEAP\_DESC(const D3D12\_RESOURCE\_ALLOCATION\_INFO& resAllocInfo, D3D12\_CPU\_PAGE\_PROPERTY cpuPageProperty, D3D12\_MEMORY\_POOL memoryPoolPreference, D3D12\_HEAP\_FLAGS flags = D3D12\_HEAP\_FLAG\_NONE)**</span></span>
</dt> <dd>

<span data-ttu-id="f844d-142">Создает новый экземпляр CD3DX12 \_ кучи \_ DESC, инициализируя следующие параметры:</span><span class="sxs-lookup"><span data-stu-id="f844d-142">Creates a new instance of a CD3DX12\_HEAP\_DESC, initializing the following parameters:</span></span>

<span data-ttu-id="f844d-143">[**D3D12 \_ \_ \_ Сведения о выделении ресурсов**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_resource_allocation_info)& ресаллоЦинфо</span><span class="sxs-lookup"><span data-stu-id="f844d-143">[**D3D12\_RESOURCE\_ALLOCATION\_INFO**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_resource_allocation_info)& resAllocInfo</span></span>

<span data-ttu-id="f844d-144">[**D3D12 \_ \_ \_ Свойство страницы ЦП**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_cpu_page_property) кпупажепроперти</span><span class="sxs-lookup"><span data-stu-id="f844d-144">[**D3D12\_CPU\_PAGE\_PROPERTY**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_cpu_page_property) cpuPageProperty</span></span>

<span data-ttu-id="f844d-145">[**D3D12 \_ Меморипулпреференце \_ пула памяти**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_memory_pool)</span><span class="sxs-lookup"><span data-stu-id="f844d-145">[**D3D12\_MEMORY\_POOL**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_memory_pool) memoryPoolPreference</span></span>

<span data-ttu-id="f844d-146">участие [**D3D12 \_ Флаги \_ флагов кучи**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_heap_flags) = D3D12 \_ куча \_ \_ нет</span><span class="sxs-lookup"><span data-stu-id="f844d-146">(opt) [**D3D12\_HEAP\_FLAGS**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_heap_flags) flags = D3D12\_HEAP\_FLAG\_NONE</span></span>

</dd> <dt>

<span data-ttu-id="f844d-147">**const константа D3D12 \_& heap для оператора const \_**</span><span class="sxs-lookup"><span data-stu-id="f844d-147">**operator const D3D12\_HEAP\_DESC&() const**</span></span>
</dt> <dd>

<span data-ttu-id="f844d-148">Определяет & оператором передачи по ссылке для \_ \_ типа структуры кучи CD3DX12.</span><span class="sxs-lookup"><span data-stu-id="f844d-148">Defines the & pass-by-reference operator for the CD3DX12\_HEAP\_DESC structure type.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="f844d-149">Требования</span><span class="sxs-lookup"><span data-stu-id="f844d-149">Requirements</span></span>



| <span data-ttu-id="f844d-150">Требование</span><span class="sxs-lookup"><span data-stu-id="f844d-150">Requirement</span></span> | <span data-ttu-id="f844d-151">Значение</span><span class="sxs-lookup"><span data-stu-id="f844d-151">Value</span></span> |
|-------------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="f844d-152">Header</span><span class="sxs-lookup"><span data-stu-id="f844d-152">Header</span></span><br/> | <dl> <span data-ttu-id="f844d-153"><dt>D3dx12. h</dt></span><span class="sxs-lookup"><span data-stu-id="f844d-153"><dt>D3dx12.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="f844d-154">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="f844d-154">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f844d-155">**\_DESC КУЧИ \_ D3D12**</span><span class="sxs-lookup"><span data-stu-id="f844d-155">**D3D12\_HEAP\_DESC**</span></span>](/windows/desktop/api/d3d12/ns-d3d12-d3d12_heap_desc)
</dt> <dt>

[<span data-ttu-id="f844d-156">Вспомогательные структуры для D3D12</span><span class="sxs-lookup"><span data-stu-id="f844d-156">Helper Structures for D3D12</span></span>](helper-structures-for-d3d12.md)
</dt> </dl>

 

 





