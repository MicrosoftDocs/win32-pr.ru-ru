---
title: Структура CD3DX12_PIPELINE_STATE_STREAM_PRIMITIVE_TOPOLOGY (D3dx12. h)
description: Вспомогательная структура, используемая для описания топологии примитивов в виде одного объекта, подходящего для описания потока.
ms.assetid: 7DC73B75-2B8D-4DAB-A0AA-6DF6F4039093
keywords:
- Структура CD3DX12_PIPELINE_STATE_STREAM_PRIMITIVE_TOPOLOGY
topic_type:
- apiref
api_name:
- CD3DX12_PIPELINE_STATE_STREAM_PRIMITIVE_TOPOLOGY
api_location:
- d3dx12.h
api_type:
- HeaderDef
ms.localizationpriority: low
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e597da8ea1ed4a4291142065e8e06f89d2664e03
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/15/2021
ms.locfileid: "105694097"
---
# <a name="cd3dx12_pipeline_state_stream_primitive_topology-structure"></a><span data-ttu-id="29415-104">\_ \_ \_ \_ Структура топологии примитива потока состояния конвейера CD3DX12 \_</span><span class="sxs-lookup"><span data-stu-id="29415-104">CD3DX12\_PIPELINE\_STATE\_STREAM\_PRIMITIVE\_TOPOLOGY structure</span></span>

<span data-ttu-id="29415-105">Вспомогательная структура, используемая для описания топологии примитивов в виде одного объекта, подходящего для описания потока.</span><span class="sxs-lookup"><span data-stu-id="29415-105">A helper structure used to describe the primitive topology as a single object suitable for a stream description.</span></span>

## <a name="syntax"></a><span data-ttu-id="29415-106">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="29415-106">Syntax</span></span>


```C++
struct CD3DX12_PIPELINE_STATE_STREAM_PRIMITIVE_TOPOLOGY {
                                                   CD3DX12_PIPELINE_STATE_STREAM_PRIMITIVE_TOPOLOGY;
                                                   CD3DX12_PIPELINE_STATE_STREAM_PRIMITIVE_TOPOLOGY(D3D12_PRIMITIVE_TOPOLOGY_TYPE const &i);
  CD3DX12_PIPELINE_STATE_STREAM_PRIMITIVE_TOPOLOGY operator=(D3D12_PRIMITIVE_TOPOLOGY_TYPE const& i);
                                                   operator D3D12_PRIMITIVE_TOPOLOGY_TYPE() const;
};
```



## <a name="members"></a><span data-ttu-id="29415-107">Члены</span><span class="sxs-lookup"><span data-stu-id="29415-107">Members</span></span>

<dl> <dt>

<span data-ttu-id="29415-108">**\_ \_ \_ \_ Топология примитива потока состояния конвейера CD3DX12 \_**</span><span class="sxs-lookup"><span data-stu-id="29415-108">**CD3DX12\_PIPELINE\_STATE\_STREAM\_PRIMITIVE\_TOPOLOGY**</span></span>
</dt> <dd>

<span data-ttu-id="29415-109">Создает новый, неинициализированный экземпляр \_ \_ \_ \_ топологии примитива потока состояния конвейера CD3DX12 \_ .</span><span class="sxs-lookup"><span data-stu-id="29415-109">Creates a new, uninitialized, instance of a CD3DX12\_PIPELINE\_STATE\_STREAM\_PRIMITIVE\_TOPOLOGY.</span></span>

</dd> <dt>

<span data-ttu-id="29415-110">**\_ \_ \_ Топология примитива потока состояния конвейера CD3DX12 \_ \_ (тип D3D12- \_ примитива \_ \_ типа "const" &i)**</span><span class="sxs-lookup"><span data-stu-id="29415-110">**CD3DX12\_PIPELINE\_STATE\_STREAM\_PRIMITIVE\_TOPOLOGY(D3D12\_PRIMITIVE\_TOPOLOGY\_TYPE const &i)**</span></span>
</dt> <dd>

<span data-ttu-id="29415-111">Создает новый экземпляр \_ \_ \_ топологии примитива потока состояния конвейера \_ CD3DX12 \_ , инициализированный с типом подобъекта для типа **\_ \_ \_ подобъекта \_ типа \_ \_ подобъекта состояния конвейера D3D12** и данными подобъекта, скопированными из *i*, структурой [**\_ \_ \_ типа примитивной топологии D3D12**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_primitive_topology_type) .</span><span class="sxs-lookup"><span data-stu-id="29415-111">Creates a new instance of a CD3DX12\_PIPELINE\_STATE\_STREAM\_PRIMITIVE\_TOPOLOGY, initialized with a subobject type of **D3D12\_PIPELINE\_STATE\_SUBOBJECT\_TYPE\_PRIMITIVE\_TOPOLOGY** and subobject data copied from *i*, a [**D3D12\_PRIMITIVE\_TOPOLOGY\_TYPE**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_primitive_topology_type) structure.</span></span>

</dd> <dt>

<span data-ttu-id="29415-112">**operator = (D3D12 \_ \_ тип топологии примитива \_ типа "const"& i)**</span><span class="sxs-lookup"><span data-stu-id="29415-112">**operator=(D3D12\_PRIMITIVE\_TOPOLOGY\_TYPE const& i)**</span></span>
</dt> <dd>

<span data-ttu-id="29415-113">Оператор присваивания копирования.</span><span class="sxs-lookup"><span data-stu-id="29415-113">Copy-assignment operator.</span></span>

</dd> <dt>

<span data-ttu-id="29415-114">**\_ \_ константа operator D3D12 \_ тип-примитив () const**</span><span class="sxs-lookup"><span data-stu-id="29415-114">**operator D3D12\_PRIMITIVE\_TOPOLOGY\_TYPE() const**</span></span>
</dt> <dd>

<span data-ttu-id="29415-115">Неявное преобразование в структуру [**типа D3D12- \_ примитивной \_ топологии \_**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_primitive_topology_type) .</span><span class="sxs-lookup"><span data-stu-id="29415-115">Implicit conversion to a [**D3D12\_PRIMITIVE\_TOPOLOGY\_TYPE**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_primitive_topology_type) structure.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="29415-116">Комментарии</span><span class="sxs-lookup"><span data-stu-id="29415-116">Remarks</span></span>

<span data-ttu-id="29415-117">\_ \_ \_ Топология примитива потока состояния конвейера CD3DX12 \_ \_ является СПЕЦИАЛИЗАЦИей typedef шаблона [**\_ \_ \_ \_ подобъекта потока состояния конвейера CD3DX12**](cd3dx12-pipeline-state-stream-subobject.md) и определяется следующим образом:</span><span class="sxs-lookup"><span data-stu-id="29415-117">CD3DX12\_PIPELINE\_STATE\_STREAM\_PRIMITIVE\_TOPOLOGY is a typedef specialization of the [**CD3DX12\_PIPELINE\_STATE\_STREAM\_SUBOBJECT**](cd3dx12-pipeline-state-stream-subobject.md) template, and is defined as follows:</span></span>


```C++
typedef CD3DX12_PIPELINE_STATE_STREAM_SUBOBJECT<D3D12_PRIMITIVE_TOPOLOGY_TYPE, D3D12_PIPELINE_STATE_SUBOBJECT_TYPE_PRIMITIVE_TOPOLOGY>
    CD3DX12_PIPELINE_STATE_STREAM_PRIMITIVE_TOPOLOGY;
          
```



## <a name="requirements"></a><span data-ttu-id="29415-118">Требования</span><span class="sxs-lookup"><span data-stu-id="29415-118">Requirements</span></span>



| <span data-ttu-id="29415-119">Требование</span><span class="sxs-lookup"><span data-stu-id="29415-119">Requirement</span></span> | <span data-ttu-id="29415-120">Значение</span><span class="sxs-lookup"><span data-stu-id="29415-120">Value</span></span> |
|-------------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="29415-121">Header</span><span class="sxs-lookup"><span data-stu-id="29415-121">Header</span></span><br/> | <dl> <span data-ttu-id="29415-122"><dt>D3dx12. h</dt></span><span class="sxs-lookup"><span data-stu-id="29415-122"><dt>D3dx12.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="29415-123">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="29415-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="29415-124">Вспомогательные структуры для D3D12</span><span class="sxs-lookup"><span data-stu-id="29415-124">Helper Structures for D3D12</span></span>](helper-structures-for-d3d12.md)
</dt> <dt>

[<span data-ttu-id="29415-125">**\_Подобъект \_ потока состояния КОНВЕЙЕРа CD3DX12 \_ \_**</span><span class="sxs-lookup"><span data-stu-id="29415-125">**CD3DX12\_PIPELINE\_STATE\_STREAM\_SUBOBJECT**</span></span>](cd3dx12-pipeline-state-stream-subobject.md)
</dt> <dt>

[<span data-ttu-id="29415-126">**\_ \_ \_ Тип подобъекта состояния конвейера D3D12 \_**</span><span class="sxs-lookup"><span data-stu-id="29415-126">**D3D12\_PIPELINE\_STATE\_SUBOBJECT\_TYPE**</span></span>](/windows/desktop/api/d3d12/ne-d3d12-d3d12_pipeline_state_subobject_type)
</dt> </dl>

 

