---
title: Структура CD3DX12_PIPELINE_STATE_STREAM_CACHED_PSO (D3dx12. h)
description: Вспомогательная структура, используемая для описания кэшированного PSO в виде одного объекта, подходящего для описания потока.
ms.assetid: 86CDC60A-275D-4B71-BE6D-C863C72E9C05
keywords:
- Структура CD3DX12_PIPELINE_STATE_STREAM_CACHED_PSO
topic_type:
- apiref
api_name:
- CD3DX12_PIPELINE_STATE_STREAM_CACHED_PSO
api_location:
- d3dx12.h
api_type:
- HeaderDef
ms.localizationpriority: low
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 78ddb223dfd2baa7bc6bee1b5a36950fc47d65d0
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/15/2021
ms.locfileid: "105694105"
---
# <a name="cd3dx12_pipeline_state_stream_cached_pso-structure"></a><span data-ttu-id="aaee0-104">\_ \_ \_ \_ Структура PSO кэшированного потока состояния конвейера CD3DX12 \_</span><span class="sxs-lookup"><span data-stu-id="aaee0-104">CD3DX12\_PIPELINE\_STATE\_STREAM\_CACHED\_PSO structure</span></span>

<span data-ttu-id="aaee0-105">Вспомогательная структура, используемая для описания кэшированного PSO в виде одного объекта, подходящего для описания потока.</span><span class="sxs-lookup"><span data-stu-id="aaee0-105">A helper structure used to describe a cached PSO as a single object suitable for a stream description.</span></span>

## <a name="syntax"></a><span data-ttu-id="aaee0-106">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="aaee0-106">Syntax</span></span>


```C++
struct CD3DX12_PIPELINE_STATE_STREAM_CACHED_PSO {
                                           CD3DX12_PIPELINE_STATE_STREAM_CACHED_PSO;
                                           CD3DX12_PIPELINE_STATE_STREAM_CACHED_PSO(D3D12_CACHED_PIPELINE_STATE const &i);
  CD3DX12_PIPELINE_STATE_STREAM_CACHED_PSO operator=(D3D12_CACHED_PIPELINE_STATE const& i);
                                           operator D3D12_CACHED_PIPELINE_STATE() const;
};
```



## <a name="members"></a><span data-ttu-id="aaee0-107">Члены</span><span class="sxs-lookup"><span data-stu-id="aaee0-107">Members</span></span>

<dl> <dt>

<span data-ttu-id="aaee0-108">**\_Поток состояния конвейера CD3DX12, \_ \_ \_ кэшированный \_ PSO**</span><span class="sxs-lookup"><span data-stu-id="aaee0-108">**CD3DX12\_PIPELINE\_STATE\_STREAM\_CACHED\_PSO**</span></span>
</dt> <dd>

<span data-ttu-id="aaee0-109">Создает новый, неинициализированный экземпляр \_ потока состояния конвейера CD3DX12, \_ \_ \_ кэшированного \_ PSO.</span><span class="sxs-lookup"><span data-stu-id="aaee0-109">Creates a new, uninitialized, instance of a CD3DX12\_PIPELINE\_STATE\_STREAM\_CACHED\_PSO.</span></span>

</dd> <dt>

<span data-ttu-id="aaee0-110">**\_Поток состояния конвейера CD3DX12, \_ \_ \_ кэшированный \_ PSO (D3D12 \_ кэшированного \_ состояния конвейера, \_ const &i)**</span><span class="sxs-lookup"><span data-stu-id="aaee0-110">**CD3DX12\_PIPELINE\_STATE\_STREAM\_CACHED\_PSO(D3D12\_CACHED\_PIPELINE\_STATE const &i)**</span></span>
</dt> <dd>

<span data-ttu-id="aaee0-111">Создает новый экземпляр \_ потока состояния конвейера CD3DX12 \_ \_ \_ с кэшированием \_ PSO, инициализированный с типом ПОДобъекта типа **\_ \_ подобъекта состояния конвейера D3D12 \_ \_ \_ кэшированные \_ PSO** и данные подобъектов, скопированные из *i*, структуры [**\_ \_ \_ состояния конвейера с кэшированием D3D12**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_cached_pipeline_state) .</span><span class="sxs-lookup"><span data-stu-id="aaee0-111">Creates a new instance of a CD3DX12\_PIPELINE\_STATE\_STREAM\_CACHED\_PSO, initialized with a subobject type of **D3D12\_PIPELINE\_STATE\_SUBOBJECT\_TYPE\_CACHED\_PSO** and subobject data copied from *i*, a [**D3D12\_CACHED\_PIPELINE\_STATE**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_cached_pipeline_state) structure.</span></span>

</dd> <dt>

<span data-ttu-id="aaee0-112">**operator = (D3D12 \_ кэшированного \_ состояния конвейера \_ const& i)**</span><span class="sxs-lookup"><span data-stu-id="aaee0-112">**operator=(D3D12\_CACHED\_PIPELINE\_STATE const& i)**</span></span>
</dt> <dd>

<span data-ttu-id="aaee0-113">Оператор присваивания копирования.</span><span class="sxs-lookup"><span data-stu-id="aaee0-113">Copy-assignment operator.</span></span>

</dd> <dt>

<span data-ttu-id="aaee0-114">**\_константа "оператор D3D12 кэшированное \_ состояние конвейера \_ ()"**</span><span class="sxs-lookup"><span data-stu-id="aaee0-114">**operator D3D12\_CACHED\_PIPELINE\_STATE() const**</span></span>
</dt> <dd>

<span data-ttu-id="aaee0-115">Неявное преобразование в структуру [**\_ \_ \_ состояния кэшированного конвейера D3D12**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_cached_pipeline_state) .</span><span class="sxs-lookup"><span data-stu-id="aaee0-115">Implicit conversion to a [**D3D12\_CACHED\_PIPELINE\_STATE**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_cached_pipeline_state) structure.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="aaee0-116">Комментарии</span><span class="sxs-lookup"><span data-stu-id="aaee0-116">Remarks</span></span>

<span data-ttu-id="aaee0-117">\_Поток состояния конвейера CD3DX12 \_ \_ \_ , кэшированный \_ PSO, является СПЕЦИАЛИЗАЦИей typedef шаблона [**\_ \_ \_ \_ подобъекта потока состояния конвейера CD3DX12**](cd3dx12-pipeline-state-stream-subobject.md) и определяется следующим образом:</span><span class="sxs-lookup"><span data-stu-id="aaee0-117">CD3DX12\_PIPELINE\_STATE\_STREAM\_CACHED\_PSO is a typedef specialization of the [**CD3DX12\_PIPELINE\_STATE\_STREAM\_SUBOBJECT**](cd3dx12-pipeline-state-stream-subobject.md) template, and is defined as follows:</span></span>


```C++
typedef CD3DX12_PIPELINE_STATE_STREAM_SUBOBJECT<D3D12_CACHED_PIPELINE_STATE, D3D12_PIPELINE_STATE_SUBOBJECT_TYPE_CACHED_PSO>
    CD3DX12_PIPELINE_STATE_STREAM_CACHED_PSO;
          
```



## <a name="requirements"></a><span data-ttu-id="aaee0-118">Требования</span><span class="sxs-lookup"><span data-stu-id="aaee0-118">Requirements</span></span>



| <span data-ttu-id="aaee0-119">Требование</span><span class="sxs-lookup"><span data-stu-id="aaee0-119">Requirement</span></span> | <span data-ttu-id="aaee0-120">Значение</span><span class="sxs-lookup"><span data-stu-id="aaee0-120">Value</span></span> |
|-------------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="aaee0-121">Header</span><span class="sxs-lookup"><span data-stu-id="aaee0-121">Header</span></span><br/> | <dl> <span data-ttu-id="aaee0-122"><dt>D3dx12. h</dt></span><span class="sxs-lookup"><span data-stu-id="aaee0-122"><dt>D3dx12.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="aaee0-123">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="aaee0-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="aaee0-124">Вспомогательные структуры для D3D12</span><span class="sxs-lookup"><span data-stu-id="aaee0-124">Helper Structures for D3D12</span></span>](helper-structures-for-d3d12.md)
</dt> <dt>

[<span data-ttu-id="aaee0-125">**\_Подобъект \_ потока состояния КОНВЕЙЕРа CD3DX12 \_ \_**</span><span class="sxs-lookup"><span data-stu-id="aaee0-125">**CD3DX12\_PIPELINE\_STATE\_STREAM\_SUBOBJECT**</span></span>](cd3dx12-pipeline-state-stream-subobject.md)
</dt> <dt>

[<span data-ttu-id="aaee0-126">**\_ \_ \_ Тип подобъекта состояния конвейера D3D12 \_**</span><span class="sxs-lookup"><span data-stu-id="aaee0-126">**D3D12\_PIPELINE\_STATE\_SUBOBJECT\_TYPE**</span></span>](/windows/desktop/api/d3d12/ne-d3d12-d3d12_pipeline_state_subobject_type)
</dt> </dl>

 

