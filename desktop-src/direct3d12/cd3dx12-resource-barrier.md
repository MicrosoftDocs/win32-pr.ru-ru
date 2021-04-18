---
title: Структура CD3DX12_RESOURCE_BARRIER (D3dx12. h)
description: Вспомогательная структура, позволяющая легко инициализировать \_ \_ структуру барьера ресурсов D3D12.
ms.assetid: 89E0F38C-8802-46E6-9583-95C5D853CD99
keywords:
- Структура CD3DX12_RESOURCE_BARRIER
topic_type:
- apiref
api_name:
- CD3DX12_RESOURCE_BARRIER
api_location:
- d3dx12.h
api_type:
- HeaderDef
ms.localizationpriority: low
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8eaa9b19a8bc7dcebba5982313bb362dbcee6157
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/15/2021
ms.locfileid: "105713978"
---
# <a name="cd3dx12_resource_barrier-structure"></a><span data-ttu-id="1b69f-104">\_ \_ Структура барьера ресурсов CD3DX12</span><span class="sxs-lookup"><span data-stu-id="1b69f-104">CD3DX12\_RESOURCE\_BARRIER structure</span></span>

<span data-ttu-id="1b69f-105">Вспомогательная структура, позволяющая легко инициализировать структуру [**\_ \_ барьера ресурсов D3D12**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_resource_barrier) .</span><span class="sxs-lookup"><span data-stu-id="1b69f-105">A helper structure to enable easy initialization of a [**D3D12\_RESOURCE\_BARRIER**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_resource_barrier) structure.</span></span>

## <a name="syntax"></a><span data-ttu-id="1b69f-106">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="1b69f-106">Syntax</span></span>


```C++
struct CD3DX12_RESOURCE_BARRIER  : public D3D12_RESOURCE_BARRIER{
                           CD3DX12_RESOURCE_BARRIER();
                           explicit CD3DX12_RESOURCE_BARRIER(const D3D12_RESOURCE_BARRIER &o);
  CD3DX12_RESOURCE_BARRIER static inline Transition(ID3D12Resource* pResource, D3D12_RESOURCE_STATES stateBefore, D3D12_RESOURCE_STATES stateAfter, UINT subresource = D3D12_RESOURCE_BARRIER_ALL_SUBRESOURCES, D3D12_RESOURCE_BARRIER_FLAGS flags = D3D12_RESOURCE_BARRIER_FLAG_NONE);
  CD3DX12_RESOURCE_BARRIER static inline Aliasing(ID3D12Resource* pResourceBefore, ID3D12Resource* pResourceAfter);
  CD3DX12_RESOURCE_BARRIER static inline UAV(ID3D12Resource* pResource);
                           operator const D3D12_RESOURCE_BARRIER&() const;
};
```



## <a name="members"></a><span data-ttu-id="1b69f-107">Члены</span><span class="sxs-lookup"><span data-stu-id="1b69f-107">Members</span></span>

<dl> <dt>

<span data-ttu-id="1b69f-108">**\_Барьер ресурсов CD3DX12 \_ ()**</span><span class="sxs-lookup"><span data-stu-id="1b69f-108">**CD3DX12\_RESOURCE\_BARRIER()**</span></span>
</dt> <dd>

<span data-ttu-id="1b69f-109">Создает новый, неинициализированный экземпляр \_ \_ барьера ресурсов CD3DX12.</span><span class="sxs-lookup"><span data-stu-id="1b69f-109">Creates a new, uninitialized, instance of a CD3DX12\_RESOURCE\_BARRIER.</span></span>

</dd> <dt>

<span data-ttu-id="1b69f-110">**явное CD3DX12 \_ Resource \_ барьер (const D3D12 \_ Resource \_ барьер &o)**</span><span class="sxs-lookup"><span data-stu-id="1b69f-110">**explicit CD3DX12\_RESOURCE\_BARRIER(const D3D12\_RESOURCE\_BARRIER &o)**</span></span>
</dt> <dd>

<span data-ttu-id="1b69f-111">Создает новый экземпляр \_ \_ барьера ресурсов CD3DX12, инициализированного с содержимым другого [**\_ \_ барьера ресурсов D3D12**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_resource_barrier).</span><span class="sxs-lookup"><span data-stu-id="1b69f-111">Creates a new instance of a CD3DX12\_RESOURCE\_BARRIER, initialized with the contents of another [**D3D12\_RESOURCE\_BARRIER**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_resource_barrier).</span></span>

</dd> <dt>

<span data-ttu-id="1b69f-112">**статический встроенный переход (ID3D12Resource \* , D3D12, \_ состояния ресурсов, \_ статебефоре, D3D12 \_ состояний ресурсов \_ статеафтер, uint Resources = D3D12 \_ Resource \_ барьер \_ все \_ подресурсы, D3D12 флаги \_ \_ \_ flags барьера = D3D12 \_ Resource барьер Flag \_ \_ \_ None)**</span><span class="sxs-lookup"><span data-stu-id="1b69f-112">**static inline Transition(ID3D12Resource\* pResource, D3D12\_RESOURCE\_STATES stateBefore, D3D12\_RESOURCE\_STATES stateAfter, UINT subresource = D3D12\_RESOURCE\_BARRIER\_ALL\_SUBRESOURCES, D3D12\_RESOURCE\_BARRIER\_FLAGS flags = D3D12\_RESOURCE\_BARRIER\_FLAG\_NONE)**</span></span>
</dt> <dd>

<span data-ttu-id="1b69f-113">Переходы между состояниями ресурсов с использованием следующих параметров:</span><span class="sxs-lookup"><span data-stu-id="1b69f-113">Transitions between resource states, using the following parameters:</span></span>

<span data-ttu-id="1b69f-114">[**ID3D12Resource**](/windows/desktop/api/d3d12/nn-d3d12-id3d12resource) \* исходный код</span><span class="sxs-lookup"><span data-stu-id="1b69f-114">[**ID3D12Resource**](/windows/desktop/api/d3d12/nn-d3d12-id3d12resource)\* pResource</span></span>

<span data-ttu-id="1b69f-115">[**D3D12 \_ Статебефоре \_ состояния ресурсов**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_resource_states)</span><span class="sxs-lookup"><span data-stu-id="1b69f-115">[**D3D12\_RESOURCE\_STATES**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_resource_states) stateBefore</span></span>

<span data-ttu-id="1b69f-116">[**D3D12 \_ Статеафтер \_ состояния ресурсов**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_resource_states)</span><span class="sxs-lookup"><span data-stu-id="1b69f-116">[**D3D12\_RESOURCE\_STATES**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_resource_states) stateAfter</span></span>

<span data-ttu-id="1b69f-117">участие Подресурс UINT = [ **D3D12 \_ Resource \_ барьер \_ все \_ подресурсы**](constants.md)</span><span class="sxs-lookup"><span data-stu-id="1b69f-117">(opt) UINT subresource = [**D3D12\_RESOURCE\_BARRIER\_ALL\_SUBRESOURCES**](constants.md)</span></span>

<span data-ttu-id="1b69f-118">участие [**D3D12 \_ Флаги \_ \_ флагов Resource барьера**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_resource_barrier_flags) = D3D12 \_ Resource \_ барьер \_ \_ None</span><span class="sxs-lookup"><span data-stu-id="1b69f-118">(opt) [**D3D12\_RESOURCE\_BARRIER\_FLAGS**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_resource_barrier_flags) flags = D3D12\_RESOURCE\_BARRIER\_FLAG\_NONE</span></span>

</dd> <dt>

<span data-ttu-id="1b69f-119">**статическое встроенное Присвоение псевдонимов (ID3D12Resource \* пресаурцебефоре, ID3D12Resource \* пресаурцеафтер)**</span><span class="sxs-lookup"><span data-stu-id="1b69f-119">**static inline Aliasing(ID3D12Resource\* pResourceBefore, ID3D12Resource\* pResourceAfter)**</span></span>
</dt> <dd>

<span data-ttu-id="1b69f-120">Создает псевдонимы для ресурса до и после перехода барьера.</span><span class="sxs-lookup"><span data-stu-id="1b69f-120">Creates aliases for the resource before and after the barrier transition.</span></span> <span data-ttu-id="1b69f-121">Параметры</span><span class="sxs-lookup"><span data-stu-id="1b69f-121">Parameters:</span></span>

<span data-ttu-id="1b69f-122">[**ID3D12Resource**](/windows/desktop/api/d3d12/nn-d3d12-id3d12resource) \* пресаурцебефоре</span><span class="sxs-lookup"><span data-stu-id="1b69f-122">[**ID3D12Resource**](/windows/desktop/api/d3d12/nn-d3d12-id3d12resource)\* pResourceBefore</span></span>

<span data-ttu-id="1b69f-123">[**ID3D12Resource**](/windows/desktop/api/d3d12/nn-d3d12-id3d12resource) \* пресаурцеафтер</span><span class="sxs-lookup"><span data-stu-id="1b69f-123">[**ID3D12Resource**](/windows/desktop/api/d3d12/nn-d3d12-id3d12resource)\* pResourceAfter</span></span>

</dd> <dt>

<span data-ttu-id="1b69f-124">**static Inline UAV ( \* Исходный код ID3D12Resource)**</span><span class="sxs-lookup"><span data-stu-id="1b69f-124">**static inline UAV(ID3D12Resource\* pResource)**</span></span>
</dt> <dd>

<span data-ttu-id="1b69f-125">Создает неупорядоченный доступ к представлению (UAV) для ресурса.</span><span class="sxs-lookup"><span data-stu-id="1b69f-125">Creates an unordered-access-view (UAV) for the resource.</span></span> <span data-ttu-id="1b69f-126">Параметры</span><span class="sxs-lookup"><span data-stu-id="1b69f-126">Parameters:</span></span>

<span data-ttu-id="1b69f-127">[**ID3D12Resource**](/windows/desktop/api/d3d12/nn-d3d12-id3d12resource) \* исходный код</span><span class="sxs-lookup"><span data-stu-id="1b69f-127">[**ID3D12Resource**](/windows/desktop/api/d3d12/nn-d3d12-id3d12resource)\* pResource</span></span>

</dd> <dt>

<span data-ttu-id="1b69f-128">**Константа D3D12 \_ Resource \_ барьера для оператора const& () const**</span><span class="sxs-lookup"><span data-stu-id="1b69f-128">**operator const D3D12\_RESOURCE\_BARRIER&() const**</span></span>
</dt> <dd>

<span data-ttu-id="1b69f-129">Определяет & оператором передачи по ссылке для типа родительской структуры.</span><span class="sxs-lookup"><span data-stu-id="1b69f-129">Defines the & pass-by-reference operator for the parent structure type.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="1b69f-130">Требования</span><span class="sxs-lookup"><span data-stu-id="1b69f-130">Requirements</span></span>



| <span data-ttu-id="1b69f-131">Требование</span><span class="sxs-lookup"><span data-stu-id="1b69f-131">Requirement</span></span> | <span data-ttu-id="1b69f-132">Значение</span><span class="sxs-lookup"><span data-stu-id="1b69f-132">Value</span></span> |
|-------------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="1b69f-133">Header</span><span class="sxs-lookup"><span data-stu-id="1b69f-133">Header</span></span><br/> | <dl> <span data-ttu-id="1b69f-134"><dt>D3dx12. h</dt></span><span class="sxs-lookup"><span data-stu-id="1b69f-134"><dt>D3dx12.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="1b69f-135">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="1b69f-135">See also</span></span>

<dl> <dt>

[<span data-ttu-id="1b69f-136">**\_Барьер ресурсов \_ D3D12**</span><span class="sxs-lookup"><span data-stu-id="1b69f-136">**D3D12\_RESOURCE\_BARRIER**</span></span>](/windows/desktop/api/d3d12/ns-d3d12-d3d12_resource_barrier)
</dt> <dt>

[<span data-ttu-id="1b69f-137">Вспомогательные структуры для D3D12</span><span class="sxs-lookup"><span data-stu-id="1b69f-137">Helper Structures for D3D12</span></span>](helper-structures-for-d3d12.md)
</dt> </dl>

 

 





