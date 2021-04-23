---
title: Структура CD3DX12_PIPELINE_STATE_STREAM_IB_STRIP_CUT_VALUE (D3dx12. h)
description: Вспомогательная структура, используемая для описания значения вырезания полосы буфера индексов в виде одного объекта, подходящего для описания потока.
ms.assetid: AF8F0919-4601-4A95-832A-5E1DA0304939
keywords:
- Структура CD3DX12_PIPELINE_STATE_STREAM_IB_STRIP_CUT_VALUE
topic_type:
- apiref
api_name:
- CD3DX12_PIPELINE_STATE_STREAM_IB_STRIP_CUT_VALUE
api_location:
- d3dx12.h
api_type:
- HeaderDef
ms.localizationpriority: low
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 86c14924828c924b3bbbca3bb1a5f822437ec4c9
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/15/2021
ms.locfileid: "105651543"
---
# <a name="cd3dx12_pipeline_state_stream_ib_strip_cut_value-structure"></a><span data-ttu-id="1e5b3-104">\_ \_ \_ \_ \_ \_ Структура значения ВЫРЕЗАНного потока состояния \_ конвейера CD3DX12</span><span class="sxs-lookup"><span data-stu-id="1e5b3-104">CD3DX12\_PIPELINE\_STATE\_STREAM\_IB\_STRIP\_CUT\_VALUE structure</span></span>

<span data-ttu-id="1e5b3-105">Вспомогательная структура, используемая для описания значения вырезания полосы буфера индексов в виде одного объекта, подходящего для описания потока.</span><span class="sxs-lookup"><span data-stu-id="1e5b3-105">A helper structure used to describe the index buffer strip cut value as a single object suitable for a stream description.</span></span>

## <a name="syntax"></a><span data-ttu-id="1e5b3-106">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="1e5b3-106">Syntax</span></span>


```C++
struct CD3DX12_PIPELINE_STATE_STREAM_IB_STRIP_CUT_VALUE {
                                                   CD3DX12_PIPELINE_STATE_STREAM_IB_STRIP_CUT_VALUE;
                                                   CD3DX12_PIPELINE_STATE_STREAM_IB_STRIP_CUT_VALUE(D3D12_INDEX_BUFFER_STRIP_CUT_VALUE const &i);
  CD3DX12_PIPELINE_STATE_STREAM_IB_STRIP_CUT_VALUE operator=(D3D12_INDEX_BUFFER_STRIP_CUT_VALUE const& i);
                                                   operator D3D12_INDEX_BUFFER_STRIP_CUT_VALUE() const;
};
```



## <a name="members"></a><span data-ttu-id="1e5b3-107">Члены</span><span class="sxs-lookup"><span data-stu-id="1e5b3-107">Members</span></span>

<dl> <dt>

<span data-ttu-id="1e5b3-108">**\_Поток состояния конвейера CD3DX12. \_ \_ \_ \_ \_ вырезание значения чередования \_**</span><span class="sxs-lookup"><span data-stu-id="1e5b3-108">**CD3DX12\_PIPELINE\_STATE\_STREAM\_IB\_STRIP\_CUT\_VALUE**</span></span>
</dt> <dd>

<span data-ttu-id="1e5b3-109">Создает новый, неинициализированный экземпляр \_ потока состояния конвейера CD3DX12, \_ \_ \_ \_ \_ вырезаемого значения полосы \_ .</span><span class="sxs-lookup"><span data-stu-id="1e5b3-109">Creates a new, uninitialized, instance of a CD3DX12\_PIPELINE\_STATE\_STREAM\_IB\_STRIP\_CUT\_VALUE.</span></span>

</dd> <dt>

<span data-ttu-id="1e5b3-110">**\_Поток состояния конвейера CD3DX12 \_ \_ \_ \_ \_ : вырезание значения вырезания \_ ( \_ буфер D3D12 индексов \_ \_ \_ вырезанное \_ значение const &i)**</span><span class="sxs-lookup"><span data-stu-id="1e5b3-110">**CD3DX12\_PIPELINE\_STATE\_STREAM\_IB\_STRIP\_CUT\_VALUE(D3D12\_INDEX\_BUFFER\_STRIP\_CUT\_VALUE const &i)**</span></span>
</dt> <dd>

<span data-ttu-id="1e5b3-111">Создает новый экземпляр \_ потока состояний конвейера CD3DX12, который приводит к \_ \_ \_ \_ \_ сокращению значения вырезания чередования \_ , инициализированного с типом подобъекта типа **\_ \_ подобъекта состояния конвейера D3D12 область \_ \_ \_ \_ \_ \_ вырезания** и данные подобъекта, скопированные из *i*, область [**\_ буфера D3D12 индексов \_ \_ \_ вырезанная структура \_ значения**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_index_buffer_strip_cut_value) .</span><span class="sxs-lookup"><span data-stu-id="1e5b3-111">Creates a new instance of a CD3DX12\_PIPELINE\_STATE\_STREAM\_IB\_STRIP\_CUT\_VALUE, initialized with a subobject type of **D3D12\_PIPELINE\_STATE\_SUBOBJECT\_TYPE\_IB\_STRIP\_CUT\_VALUE** and subobject data copied from *i*, a [**D3D12\_INDEX\_BUFFER\_STRIP\_CUT\_VALUE**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_index_buffer_strip_cut_value) structure.</span></span>

</dd> <dt>

<span data-ttu-id="1e5b3-112">**operator = (D3D12 \_ Индекс \_ \_ полоса \_ вырезание \_ значения const& i)**</span><span class="sxs-lookup"><span data-stu-id="1e5b3-112">**operator=(D3D12\_INDEX\_BUFFER\_STRIP\_CUT\_VALUE const& i)**</span></span>
</dt> <dd>

<span data-ttu-id="1e5b3-113">Оператор присваивания копирования.</span><span class="sxs-lookup"><span data-stu-id="1e5b3-113">Copy-assignment operator.</span></span>

</dd> <dt>

<span data-ttu-id="1e5b3-114">**Оператор D3D12 \_ Индекс \_ \_ полоса \_ вырезанного \_ значения () const**</span><span class="sxs-lookup"><span data-stu-id="1e5b3-114">**operator D3D12\_INDEX\_BUFFER\_STRIP\_CUT\_VALUE() const**</span></span>
</dt> <dd>

<span data-ttu-id="1e5b3-115">Неявное преобразование в структуру [**\_ буфера D3D12 индекса \_ \_ полосы \_ вырезания \_ значений**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_index_buffer_strip_cut_value) .</span><span class="sxs-lookup"><span data-stu-id="1e5b3-115">Implicit conversion to a [**D3D12\_INDEX\_BUFFER\_STRIP\_CUT\_VALUE**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_index_buffer_strip_cut_value) structure.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="1e5b3-116">Комментарии</span><span class="sxs-lookup"><span data-stu-id="1e5b3-116">Remarks</span></span>

<span data-ttu-id="1e5b3-117">\_ \_ \_ Значение вырезания потока состояния конвейера CD3DX12 \_ \_ \_ \_ является специализацией typedef шаблона [**\_ \_ \_ \_ подобъекта потока состояния конвейера CD3DX12**](cd3dx12-pipeline-state-stream-subobject.md) и определяется следующим образом:</span><span class="sxs-lookup"><span data-stu-id="1e5b3-117">CD3DX12\_PIPELINE\_STATE\_STREAM\_IB\_STRIP\_CUT\_VALUE is a typedef specialization of the [**CD3DX12\_PIPELINE\_STATE\_STREAM\_SUBOBJECT**](cd3dx12-pipeline-state-stream-subobject.md) template, and is defined as follows:</span></span>


```C++
typedef CD3DX12_PIPELINE_STATE_STREAM_SUBOBJECT<D3D12_INDEX_BUFFER_STRIP_CUT_VALUE, D3D12_PIPELINE_STATE_SUBOBJECT_TYPE_IB_STRIP_CUT_VALUE>
    CD3DX12_PIPELINE_STATE_STREAM_IB_STRIP_CUT_VALUE;
          
```



## <a name="requirements"></a><span data-ttu-id="1e5b3-118">Требования</span><span class="sxs-lookup"><span data-stu-id="1e5b3-118">Requirements</span></span>



| <span data-ttu-id="1e5b3-119">Требование</span><span class="sxs-lookup"><span data-stu-id="1e5b3-119">Requirement</span></span> | <span data-ttu-id="1e5b3-120">Значение</span><span class="sxs-lookup"><span data-stu-id="1e5b3-120">Value</span></span> |
|-------------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="1e5b3-121">Header</span><span class="sxs-lookup"><span data-stu-id="1e5b3-121">Header</span></span><br/> | <dl> <span data-ttu-id="1e5b3-122"><dt>D3dx12. h</dt></span><span class="sxs-lookup"><span data-stu-id="1e5b3-122"><dt>D3dx12.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="1e5b3-123">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="1e5b3-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="1e5b3-124">Вспомогательные структуры для D3D12</span><span class="sxs-lookup"><span data-stu-id="1e5b3-124">Helper Structures for D3D12</span></span>](helper-structures-for-d3d12.md)
</dt> <dt>

[<span data-ttu-id="1e5b3-125">**\_Подобъект \_ потока состояния КОНВЕЙЕРа CD3DX12 \_ \_**</span><span class="sxs-lookup"><span data-stu-id="1e5b3-125">**CD3DX12\_PIPELINE\_STATE\_STREAM\_SUBOBJECT**</span></span>](cd3dx12-pipeline-state-stream-subobject.md)
</dt> <dt>

[<span data-ttu-id="1e5b3-126">**\_ \_ \_ Тип подобъекта состояния конвейера D3D12 \_**</span><span class="sxs-lookup"><span data-stu-id="1e5b3-126">**D3D12\_PIPELINE\_STATE\_SUBOBJECT\_TYPE**</span></span>](/windows/desktop/api/d3d12/ne-d3d12-d3d12_pipeline_state_subobject_type)
</dt> </dl>

 

