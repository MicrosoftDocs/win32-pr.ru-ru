---
title: Структура CD3DX12_PIPELINE_STATE_STREAM_INPUT_LAYOUT (D3dx12. h)
description: Вспомогательная структура, используемая для описания входного макета в виде одного объекта, подходящего для описания потока.
ms.assetid: CEAD9FA6-4FB0-492E-9E81-8C4900A1FBC5
keywords:
- Структура CD3DX12_PIPELINE_STATE_STREAM_INPUT_LAYOUT
topic_type:
- apiref
api_name:
- CD3DX12_PIPELINE_STATE_STREAM_INPUT_LAYOUT
api_location:
- d3dx12.h
api_type:
- HeaderDef
ms.localizationpriority: low
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6ba382552d700ddddee02cdc1343936e6bcf6837
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/15/2021
ms.locfileid: "105651542"
---
# <a name="cd3dx12_pipeline_state_stream_input_layout-structure"></a><span data-ttu-id="87522-104">\_ \_ \_ \_ \_ Структура входной структуры потока состояния конвейера CD3DX12</span><span class="sxs-lookup"><span data-stu-id="87522-104">CD3DX12\_PIPELINE\_STATE\_STREAM\_INPUT\_LAYOUT structure</span></span>

<span data-ttu-id="87522-105">Вспомогательная структура, используемая для описания входного макета в виде одного объекта, подходящего для описания потока.</span><span class="sxs-lookup"><span data-stu-id="87522-105">A helper structure used to describe an input layout as a single object suitable for a stream description.</span></span>

## <a name="syntax"></a><span data-ttu-id="87522-106">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="87522-106">Syntax</span></span>


```C++
struct CD3DX12_PIPELINE_STATE_STREAM_INPUT_LAYOUT {
                                             CD3DX12_PIPELINE_STATE_STREAM_INPUT_LAYOUT;
                                             CD3DX12_PIPELINE_STATE_STREAM_INPUT_LAYOUT(D3D12_INPUT_LAYOUT_DESC const &i);
  CD3DX12_PIPELINE_STATE_STREAM_INPUT_LAYOUT operator=(D3D12_INPUT_LAYOUT_DESC const& i);
                                             operator D3D12_INPUT_LAYOUT_DESC() const;
};
```



## <a name="members"></a><span data-ttu-id="87522-107">Члены</span><span class="sxs-lookup"><span data-stu-id="87522-107">Members</span></span>

<dl> <dt>

<span data-ttu-id="87522-108">**\_ \_ \_ \_ Схема ввода потока состояния конвейера CD3DX12 \_**</span><span class="sxs-lookup"><span data-stu-id="87522-108">**CD3DX12\_PIPELINE\_STATE\_STREAM\_INPUT\_LAYOUT**</span></span>
</dt> <dd>

<span data-ttu-id="87522-109">Создает новый, неинициализированный экземпляр \_ \_ \_ \_ входного макета потока состояния конвейера CD3DX12 \_ .</span><span class="sxs-lookup"><span data-stu-id="87522-109">Creates a new, uninitialized, instance of a CD3DX12\_PIPELINE\_STATE\_STREAM\_INPUT\_LAYOUT.</span></span>

</dd> <dt>

<span data-ttu-id="87522-110">**\_ \_ Схема ввода потока состояния конвейера CD3DX12 \_ \_ \_ (D3D12 \_ входной \_ Макет структуры данных \_ const &i)**</span><span class="sxs-lookup"><span data-stu-id="87522-110">**CD3DX12\_PIPELINE\_STATE\_STREAM\_INPUT\_LAYOUT(D3D12\_INPUT\_LAYOUT\_DESC const &i)**</span></span>
</dt> <dd>

<span data-ttu-id="87522-111">Создает новый экземпляр \_ \_ \_ схемы входного потока состояния конвейера \_ CD3DX12 \_ , инициализированный с типом подобъекта для типа **\_ \_ подобъекта состояния конвейера D3D12 \_ \_ \_ \_ структура входных** данных и подобъектами, скопированными из *i*, [**D3D12 \_ ввода структуры входного \_ макета \_**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_input_layout_desc) .</span><span class="sxs-lookup"><span data-stu-id="87522-111">Creates a new instance of a CD3DX12\_PIPELINE\_STATE\_STREAM\_INPUT\_LAYOUT, initialized with a subobject type of **D3D12\_PIPELINE\_STATE\_SUBOBJECT\_TYPE\_INPUT\_LAYOUT** and subobject data copied from *i*, a [**D3D12\_INPUT\_LAYOUT\_DESC**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_input_layout_desc) structure.</span></span>

</dd> <dt>

<span data-ttu-id="87522-112">**operator = (D3D12 \_ входной \_ Макет структуры \_ const& i)**</span><span class="sxs-lookup"><span data-stu-id="87522-112">**operator=(D3D12\_INPUT\_LAYOUT\_DESC const& i)**</span></span>
</dt> <dd>

<span data-ttu-id="87522-113">Оператор присваивания копирования.</span><span class="sxs-lookup"><span data-stu-id="87522-113">Copy-assignment operator.</span></span>

</dd> <dt>

<span data-ttu-id="87522-114">**\_константа D3D12 входного макета оператора operator \_ \_ () const**</span><span class="sxs-lookup"><span data-stu-id="87522-114">**operator D3D12\_INPUT\_LAYOUT\_DESC() const**</span></span>
</dt> <dd>

<span data-ttu-id="87522-115">Неявное преобразование в структуру [**D3D12 \_ входных данных \_ макета \_**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_input_layout_desc) .</span><span class="sxs-lookup"><span data-stu-id="87522-115">Implicit conversion to a [**D3D12\_INPUT\_LAYOUT\_DESC**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_input_layout_desc) structure.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="87522-116">Комментарии</span><span class="sxs-lookup"><span data-stu-id="87522-116">Remarks</span></span>

<span data-ttu-id="87522-117">\_ \_ Схема ввода потока состояния конвейера CD3DX12 \_ \_ \_ является СПЕЦИАЛИЗАЦИей typedef шаблона [**\_ \_ \_ \_ подобъекта потока состояния конвейера CD3DX12**](cd3dx12-pipeline-state-stream-subobject.md) и определяется следующим образом:</span><span class="sxs-lookup"><span data-stu-id="87522-117">CD3DX12\_PIPELINE\_STATE\_STREAM\_INPUT\_LAYOUT is a typedef specialization of the [**CD3DX12\_PIPELINE\_STATE\_STREAM\_SUBOBJECT**](cd3dx12-pipeline-state-stream-subobject.md) template, and is defined as follows:</span></span>


```C++
typedef CD3DX12_PIPELINE_STATE_STREAM_SUBOBJECT<D3D12_INPUT_LAYOUT_DESC, D3D12_PIPELINE_STATE_SUBOBJECT_TYPE_INPUT_LAYOUT>
    CD3DX12_PIPELINE_STATE_STREAM_INPUT_LAYOUT;
          
```



## <a name="requirements"></a><span data-ttu-id="87522-118">Требования</span><span class="sxs-lookup"><span data-stu-id="87522-118">Requirements</span></span>



| <span data-ttu-id="87522-119">Требование</span><span class="sxs-lookup"><span data-stu-id="87522-119">Requirement</span></span> | <span data-ttu-id="87522-120">Значение</span><span class="sxs-lookup"><span data-stu-id="87522-120">Value</span></span> |
|-------------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="87522-121">Header</span><span class="sxs-lookup"><span data-stu-id="87522-121">Header</span></span><br/> | <dl> <span data-ttu-id="87522-122"><dt>D3dx12. h</dt></span><span class="sxs-lookup"><span data-stu-id="87522-122"><dt>D3dx12.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="87522-123">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="87522-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="87522-124">Вспомогательные структуры для D3D12</span><span class="sxs-lookup"><span data-stu-id="87522-124">Helper Structures for D3D12</span></span>](helper-structures-for-d3d12.md)
</dt> <dt>

[<span data-ttu-id="87522-125">**\_Подобъект \_ потока состояния КОНВЕЙЕРа CD3DX12 \_ \_**</span><span class="sxs-lookup"><span data-stu-id="87522-125">**CD3DX12\_PIPELINE\_STATE\_STREAM\_SUBOBJECT**</span></span>](cd3dx12-pipeline-state-stream-subobject.md)
</dt> <dt>

[<span data-ttu-id="87522-126">**\_ \_ \_ Тип подобъекта состояния конвейера D3D12 \_**</span><span class="sxs-lookup"><span data-stu-id="87522-126">**D3D12\_PIPELINE\_STATE\_SUBOBJECT\_TYPE**</span></span>](/windows/desktop/api/d3d12/ne-d3d12-d3d12_pipeline_state_subobject_type)
</dt> </dl>

 

