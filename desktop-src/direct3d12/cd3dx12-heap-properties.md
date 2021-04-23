---
title: Структура CD3DX12_HEAP_PROPERTIES (D3dx12. h)
description: Вспомогательная структура, позволяющая легко инициализировать \_ \_ структуру свойств кучи D3D12.
ms.assetid: AC759F25-D643-412D-AA83-3A2C040BE64B
keywords:
- Структура CD3DX12_HEAP_PROPERTIES
topic_type:
- apiref
api_name:
- CD3DX12_HEAP_PROPERTIES
api_location:
- d3dx12.h
api_type:
- HeaderDef
ms.localizationpriority: low
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 90cc5f5cee6bf70aad064396589aad8a483f2c50
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/15/2021
ms.locfileid: "105694104"
---
# <a name="cd3dx12_heap_properties-structure"></a><span data-ttu-id="6f25f-104">\_ \_ Структура свойств кучи CD3DX12</span><span class="sxs-lookup"><span data-stu-id="6f25f-104">CD3DX12\_HEAP\_PROPERTIES structure</span></span>

<span data-ttu-id="6f25f-105">Вспомогательная структура, позволяющая легко инициализировать структуру [**\_ \_ свойств кучи D3D12**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_heap_properties) .</span><span class="sxs-lookup"><span data-stu-id="6f25f-105">A helper structure to enable easy initialization of a [**D3D12\_HEAP\_PROPERTIES**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_heap_properties) structure.</span></span>

## <a name="syntax"></a><span data-ttu-id="6f25f-106">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="6f25f-106">Syntax</span></span>


```C++
struct CD3DX12_HEAP_PROPERTIES  : public D3D12_HEAP_PROPERTIES{
       CD3DX12_HEAP_PROPERTIES();
       explicit CD3DX12_HEAP_PROPERTIES(const D3D12_HEAP_PROPERTIES &o);
       CD3DX12_HEAP_PROPERTIES(D3D12_CPU_PAGE_PROPERTY cpuPageProperty, D3D12_MEMORY_POOL memoryPoolPreference, UINT creationNodeMask = 1, UINT nodeMask = 1);
       explicit CD3DX12_HEAP_PROPERTIES(D3D12_HEAP_TYPE type, UINT creationNodeMask = 1, UINT nodeMask = 1);
       operator const D3D12_HEAP_PROPERTIES&() const;
  bool inline operator==( const D3D12_HEAP_PROPERTIES& l, const D3D12_HEAP_PROPERTIES& r );
  bool inline operator!=( const D3D12_HEAP_PROPERTIES& l, const D3D12_HEAP_PROPERTIES& r );
};
```



## <a name="members"></a><span data-ttu-id="6f25f-107">Члены</span><span class="sxs-lookup"><span data-stu-id="6f25f-107">Members</span></span>

<dl> <dt>

<span data-ttu-id="6f25f-108">**\_Свойства КУЧИ CD3DX12 \_ ()**</span><span class="sxs-lookup"><span data-stu-id="6f25f-108">**CD3DX12\_HEAP\_PROPERTIES()**</span></span>
</dt> <dd>

<span data-ttu-id="6f25f-109">Создает новый, неинициализированный экземпляр \_ свойств КУЧИ CD3DX12 \_ .</span><span class="sxs-lookup"><span data-stu-id="6f25f-109">Creates a new, uninitialized, instance of a CD3DX12\_HEAP\_PROPERTIES.</span></span>

</dd> <dt>

<span data-ttu-id="6f25f-110">**явные \_ Свойства КУЧИ CD3DX12 \_ (свойства const D3D12 \_ кучи \_ &o)**</span><span class="sxs-lookup"><span data-stu-id="6f25f-110">**explicit CD3DX12\_HEAP\_PROPERTIES(const D3D12\_HEAP\_PROPERTIES &o)**</span></span>
</dt> <dd>

<span data-ttu-id="6f25f-111">Создает новый экземпляр \_ свойств КУЧИ CD3DX12 \_ , инициализируемый с содержимым другой структуры [**\_ \_ свойств кучи D3D12**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_heap_properties) .</span><span class="sxs-lookup"><span data-stu-id="6f25f-111">Creates a new instance of a CD3DX12\_HEAP\_PROPERTIES, initialized with the contents of another [**D3D12\_HEAP\_PROPERTIES**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_heap_properties) structure.</span></span>

</dd> <dt>

<span data-ttu-id="6f25f-112">**\_Свойства КУЧИ CD3DX12 \_ ( \_ свойство страницы ЦП D3D12 \_ \_ Кпупажепроперти, D3D12 \_ \_ пула памяти МЕМОРИПУЛПРЕФЕРЕНЦЕ, uint креатионнодемаск = 1, uint нодемаск = 1)**</span><span class="sxs-lookup"><span data-stu-id="6f25f-112">**CD3DX12\_HEAP\_PROPERTIES(D3D12\_CPU\_PAGE\_PROPERTY cpuPageProperty, D3D12\_MEMORY\_POOL memoryPoolPreference, UINT creationNodeMask = 1, UINT nodeMask = 1)**</span></span>
</dt> <dd>

<span data-ttu-id="6f25f-113">Создает новый экземпляр \_ свойств КУЧИ CD3DX12 \_ , инициализируя следующие параметры:</span><span class="sxs-lookup"><span data-stu-id="6f25f-113">Creates a new instance of a CD3DX12\_HEAP\_PROPERTIES, initializing the following parameters:</span></span>

<span data-ttu-id="6f25f-114">[**D3D12 \_ \_ \_ Свойство страницы ЦП**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_cpu_page_property) кпупажепроперти</span><span class="sxs-lookup"><span data-stu-id="6f25f-114">[**D3D12\_CPU\_PAGE\_PROPERTY**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_cpu_page_property) cpuPageProperty</span></span>

<span data-ttu-id="6f25f-115">[**D3D12 \_ Меморипулпреференце \_ пула памяти**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_memory_pool)</span><span class="sxs-lookup"><span data-stu-id="6f25f-115">[**D3D12\_MEMORY\_POOL**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_memory_pool) memoryPoolPreference</span></span>

<span data-ttu-id="6f25f-116">участие UINT Креатионнодемаск = 1</span><span class="sxs-lookup"><span data-stu-id="6f25f-116">(opt) UINT creationNodeMask = 1</span></span>

<span data-ttu-id="6f25f-117">участие UINT Нодемаск = 1</span><span class="sxs-lookup"><span data-stu-id="6f25f-117">(opt) UINT nodeMask = 1</span></span>

</dd> <dt>

<span data-ttu-id="6f25f-118">**явные \_ Свойства КУЧИ CD3DX12 \_ ( \_ тип КУЧИ D3D12 \_ , uint КРЕАТИОННОДЕМАСК = 1, uint нодемаск = 1)**</span><span class="sxs-lookup"><span data-stu-id="6f25f-118">**explicit CD3DX12\_HEAP\_PROPERTIES(D3D12\_HEAP\_TYPE type, UINT creationNodeMask = 1, UINT nodeMask = 1)**</span></span>
</dt> <dd>

<span data-ttu-id="6f25f-119">Создает новый экземпляр \_ свойств КУЧИ CD3DX12 \_ , инициализируя следующие параметры:</span><span class="sxs-lookup"><span data-stu-id="6f25f-119">Creates a new instance of a CD3DX12\_HEAP\_PROPERTIES, initializing the following parameters:</span></span>

<span data-ttu-id="6f25f-120">[**D3D12 \_ Тип \_ типа кучи**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_heap_type)</span><span class="sxs-lookup"><span data-stu-id="6f25f-120">[**D3D12\_HEAP\_TYPE**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_heap_type) type</span></span>

<span data-ttu-id="6f25f-121">участие UINT Креатионнодемаск = 1</span><span class="sxs-lookup"><span data-stu-id="6f25f-121">(opt) UINT creationNodeMask = 1</span></span>

<span data-ttu-id="6f25f-122">участие UINT Нодемаск = 1</span><span class="sxs-lookup"><span data-stu-id="6f25f-122">(opt) UINT nodeMask = 1</span></span>

</dd> <dt>

<span data-ttu-id="6f25f-123">**Константа operator const D3D12 \_ \_ свойства кучи& () const**</span><span class="sxs-lookup"><span data-stu-id="6f25f-123">**operator const D3D12\_HEAP\_PROPERTIES&() const**</span></span>
</dt> <dd>

<span data-ttu-id="6f25f-124">Определяет & оператором передачи по ссылке для типа родительской структуры.</span><span class="sxs-lookup"><span data-stu-id="6f25f-124">Defines the & pass-by-reference operator for the parent structure type.</span></span>

</dd> <dt>

<span data-ttu-id="6f25f-125">**встроенный оператор = = (const D3D12 \_ Свойства кучи \_& l, константные \_ свойства кучи D3D12 \_& r)**</span><span class="sxs-lookup"><span data-stu-id="6f25f-125">**inline operator==( const D3D12\_HEAP\_PROPERTIES& l, const D3D12\_HEAP\_PROPERTIES& r )**</span></span>
</dt> <dd>

<span data-ttu-id="6f25f-126">Проверяет на равенство между указанными \_ \_ экземплярами свойств кучи D3D12 на основе равенства всех полей элементов.</span><span class="sxs-lookup"><span data-stu-id="6f25f-126">Tests for equality between the specified D3D12\_HEAP\_PROPERTIES instances, based on equality of all member fields.</span></span>

</dd> <dt>

<span data-ttu-id="6f25f-127">**встроенный оператор! = (const D3D12 \_ Свойства кучи \_& l, константные \_ свойства кучи D3D12 \_& r)**</span><span class="sxs-lookup"><span data-stu-id="6f25f-127">**inline operator!=( const D3D12\_HEAP\_PROPERTIES& l, const D3D12\_HEAP\_PROPERTIES& r )**</span></span>
</dt> <dd>

<span data-ttu-id="6f25f-128">Проверяет наличие неравенства между указанными \_ \_ экземплярами свойств кучи D3D12.</span><span class="sxs-lookup"><span data-stu-id="6f25f-128">Tests for inequality between the specified D3D12\_HEAP\_PROPERTIES instances.</span></span> <span data-ttu-id="6f25f-129">Реализуется путем взятия обратного значения **оператора = =** value.</span><span class="sxs-lookup"><span data-stu-id="6f25f-129">Implemented by taking the inverse of the **operator==** value.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="6f25f-130">Требования</span><span class="sxs-lookup"><span data-stu-id="6f25f-130">Requirements</span></span>



| <span data-ttu-id="6f25f-131">Требование</span><span class="sxs-lookup"><span data-stu-id="6f25f-131">Requirement</span></span> | <span data-ttu-id="6f25f-132">Значение</span><span class="sxs-lookup"><span data-stu-id="6f25f-132">Value</span></span> |
|-------------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="6f25f-133">Header</span><span class="sxs-lookup"><span data-stu-id="6f25f-133">Header</span></span><br/> | <dl> <span data-ttu-id="6f25f-134"><dt>D3dx12. h</dt></span><span class="sxs-lookup"><span data-stu-id="6f25f-134"><dt>D3dx12.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="6f25f-135">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="6f25f-135">See also</span></span>

<dl> <dt>

[<span data-ttu-id="6f25f-136">**\_Свойства КУЧИ \_ D3D12**</span><span class="sxs-lookup"><span data-stu-id="6f25f-136">**D3D12\_HEAP\_PROPERTIES**</span></span>](/windows/desktop/api/d3d12/ns-d3d12-d3d12_heap_properties)
</dt> <dt>

[<span data-ttu-id="6f25f-137">Вспомогательные структуры для D3D12</span><span class="sxs-lookup"><span data-stu-id="6f25f-137">Helper Structures for D3D12</span></span>](helper-structures-for-d3d12.md)
</dt> </dl>

 

 





