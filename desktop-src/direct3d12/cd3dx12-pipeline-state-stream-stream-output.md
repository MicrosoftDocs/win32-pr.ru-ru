---
title: Структура CD3DX12_PIPELINE_STATE_STREAM_STREAM_OUTPUT (D3dx12. h)
description: Вспомогательная структура, используемая для описания выходного описания потока в виде одного объекта, подходящего для описания потока.
ms.assetid: CC7E1E76-CD44-4D70-A5B8-7C2B6210468E
keywords:
- Структура CD3DX12_PIPELINE_STATE_STREAM_STREAM_OUTPUT
topic_type:
- apiref
api_name:
- CD3DX12_PIPELINE_STATE_STREAM_STREAM_OUTPUT
api_location:
- d3dx12.h
api_type:
- HeaderDef
ms.localizationpriority: low
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: acc8f7bf059c4eee72b0b22abfc424ee82ffd2dc
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/15/2021
ms.locfileid: "105713521"
---
# <a name="cd3dx12_pipeline_state_stream_stream_output-structure"></a><span data-ttu-id="5ca32-104">\_ \_ \_ \_ Выходная структура потока состояния конвейера CD3DX12 \_</span><span class="sxs-lookup"><span data-stu-id="5ca32-104">CD3DX12\_PIPELINE\_STATE\_STREAM\_STREAM\_OUTPUT structure</span></span>

<span data-ttu-id="5ca32-105">Вспомогательная структура, используемая для описания выходного описания потока в виде одного объекта, подходящего для описания потока.</span><span class="sxs-lookup"><span data-stu-id="5ca32-105">A helper structure used to describe the stream output description as a single object suitable for a stream description.</span></span>

## <a name="syntax"></a><span data-ttu-id="5ca32-106">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="5ca32-106">Syntax</span></span>


```C++
struct CD3DX12_PIPELINE_STATE_STREAM_STREAM_OUTPUT {
                                              CD3DX12_PIPELINE_STATE_STREAM_STREAM_OUTPUT;
                                              CD3DX12_PIPELINE_STATE_STREAM_STREAM_OUTPUT(D3D12_STREAM_OUTPUT_DESC const &i);
  CD3DX12_PIPELINE_STATE_STREAM_STREAM_OUTPUT operator=(D3D12_STREAM_OUTPUT_DESC const& i);
                                              operator D3D12_STREAM_OUTPUT_DESC() const;
};
```



## <a name="members"></a><span data-ttu-id="5ca32-107">Члены</span><span class="sxs-lookup"><span data-stu-id="5ca32-107">Members</span></span>

<dl> <dt>

<span data-ttu-id="5ca32-108">**\_ \_ \_ \_ Выходные данные потока состояния конвейера \_ CD3DX12**</span><span class="sxs-lookup"><span data-stu-id="5ca32-108">**CD3DX12\_PIPELINE\_STATE\_STREAM\_STREAM\_OUTPUT**</span></span>
</dt> <dd>

<span data-ttu-id="5ca32-109">Создает новый, неинициализированный экземпляр потока \_ вывода потока состояния конвейера \_ CD3DX12 \_ \_ \_ .</span><span class="sxs-lookup"><span data-stu-id="5ca32-109">Creates a new, uninitialized, instance of a CD3DX12\_PIPELINE\_STATE\_STREAM\_STREAM\_OUTPUT.</span></span>

</dd> <dt>

<span data-ttu-id="5ca32-110">**Потоковая передача потока \_ состояния конвейера CD3DX12 \_ \_ \_ \_ ( \_ потоковая передача D3D12 \_ OUTPUT \_ const &i)**</span><span class="sxs-lookup"><span data-stu-id="5ca32-110">**CD3DX12\_PIPELINE\_STATE\_STREAM\_STREAM\_OUTPUT(D3D12\_STREAM\_OUTPUT\_DESC const &i)**</span></span>
</dt> <dd>

<span data-ttu-id="5ca32-111">Создает новый экземпляр потокового вывода потока \_ состояния конвейера CD3DX12 \_ \_ \_ \_ , инициализированного с типом подобъекта потока данных **о \_ \_ \_ \_ типе \_ \_ подобъекта состояния конвейера D3D12** и данных подобъекта, скопированных из *i*, [**\_ \_ выходную структуру вывода \_ потока D3D12**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_stream_output_desc) .</span><span class="sxs-lookup"><span data-stu-id="5ca32-111">Creates a new instance of a CD3DX12\_PIPELINE\_STATE\_STREAM\_STREAM\_OUTPUT, initialized with a subobject type of **D3D12\_PIPELINE\_STATE\_SUBOBJECT\_TYPE\_STREAM\_OUTPUT** and subobject data copied from *i*, a [**D3D12\_STREAM\_OUTPUT\_DESC**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_stream_output_desc) structure.</span></span>

</dd> <dt>

<span data-ttu-id="5ca32-112">**operator = (D3D12 \_ поток \_ вывода Output \_ const,& i)**</span><span class="sxs-lookup"><span data-stu-id="5ca32-112">**operator=(D3D12\_STREAM\_OUTPUT\_DESC const& i)**</span></span>
</dt> <dd>

<span data-ttu-id="5ca32-113">Оператор присваивания копирования.</span><span class="sxs-lookup"><span data-stu-id="5ca32-113">Copy-assignment operator.</span></span>

</dd> <dt>

<span data-ttu-id="5ca32-114">**Оператор D3D12 \_ потока \_ OUTPUT \_ () const**</span><span class="sxs-lookup"><span data-stu-id="5ca32-114">**operator D3D12\_STREAM\_OUTPUT\_DESC() const**</span></span>
</dt> <dd>

<span data-ttu-id="5ca32-115">Неявное преобразование в структуру [**\_ \_ вывода \_ потока D3D12**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_stream_output_desc) .</span><span class="sxs-lookup"><span data-stu-id="5ca32-115">Implicit conversion to a [**D3D12\_STREAM\_OUTPUT\_DESC**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_stream_output_desc) structure.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="5ca32-116">Комментарии</span><span class="sxs-lookup"><span data-stu-id="5ca32-116">Remarks</span></span>

<span data-ttu-id="5ca32-117">\_Выходной поток потока состояния конвейера CD3DX12 \_ \_ \_ \_ является СПЕЦИАЛИЗАЦИей typedef шаблона [**\_ \_ \_ \_ подобъекта потока состояния конвейера CD3DX12**](cd3dx12-pipeline-state-stream-subobject.md) и определяется следующим образом:</span><span class="sxs-lookup"><span data-stu-id="5ca32-117">CD3DX12\_PIPELINE\_STATE\_STREAM\_STREAM\_OUTPUT is a typedef specialization of the [**CD3DX12\_PIPELINE\_STATE\_STREAM\_SUBOBJECT**](cd3dx12-pipeline-state-stream-subobject.md) template, and is defined as follows:</span></span>


```C++
typedef CD3DX12_PIPELINE_STATE_STREAM_SUBOBJECT<D3D12_STREAM_OUTPUT_DESC, D3D12_PIPELINE_STATE_SUBOBJECT_TYPE_STREAM_OUTPUT>
    CD3DX12_PIPELINE_STATE_STREAM_STREAM_OUTPUT;
          
```



## <a name="requirements"></a><span data-ttu-id="5ca32-118">Требования</span><span class="sxs-lookup"><span data-stu-id="5ca32-118">Requirements</span></span>



| <span data-ttu-id="5ca32-119">Требование</span><span class="sxs-lookup"><span data-stu-id="5ca32-119">Requirement</span></span> | <span data-ttu-id="5ca32-120">Значение</span><span class="sxs-lookup"><span data-stu-id="5ca32-120">Value</span></span> |
|-------------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="5ca32-121">Header</span><span class="sxs-lookup"><span data-stu-id="5ca32-121">Header</span></span><br/> | <dl> <span data-ttu-id="5ca32-122"><dt>D3dx12. h</dt></span><span class="sxs-lookup"><span data-stu-id="5ca32-122"><dt>D3dx12.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="5ca32-123">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="5ca32-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="5ca32-124">Вспомогательные структуры для D3D12</span><span class="sxs-lookup"><span data-stu-id="5ca32-124">Helper Structures for D3D12</span></span>](helper-structures-for-d3d12.md)
</dt> <dt>

[<span data-ttu-id="5ca32-125">**\_Подобъект \_ потока состояния КОНВЕЙЕРа CD3DX12 \_ \_**</span><span class="sxs-lookup"><span data-stu-id="5ca32-125">**CD3DX12\_PIPELINE\_STATE\_STREAM\_SUBOBJECT**</span></span>](cd3dx12-pipeline-state-stream-subobject.md)
</dt> <dt>

[<span data-ttu-id="5ca32-126">**\_ \_ \_ Тип подобъекта состояния конвейера D3D12 \_**</span><span class="sxs-lookup"><span data-stu-id="5ca32-126">**D3D12\_PIPELINE\_STATE\_SUBOBJECT\_TYPE**</span></span>](/windows/desktop/api/d3d12/ne-d3d12-d3d12_pipeline_state_subobject_type)
</dt> </dl>

 

