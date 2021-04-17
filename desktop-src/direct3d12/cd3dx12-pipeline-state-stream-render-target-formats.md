---
title: Структура CD3DX12_PIPELINE_STATE_STREAM_RENDER_TARGET_FORMATS (D3dx12. h)
description: Вспомогательная структура, используемая для описания форматов целевого объекта отрисовки в виде одного объекта, подходящего для описания потока.
ms.assetid: 8C5C2279-7985-41B6-87EA-ABB0007DAFD4
keywords:
- Структура CD3DX12_PIPELINE_STATE_STREAM_RENDER_TARGET_FORMATS
topic_type:
- apiref
api_name:
- CD3DX12_PIPELINE_STATE_STREAM_RENDER_TARGET_FORMATS
api_location:
- d3dx12.h
api_type:
- HeaderDef
ms.localizationpriority: low
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5a64f051ba56edf176c87bbc99551cd974fc3a43
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/15/2021
ms.locfileid: "105694092"
---
# <a name="cd3dx12_pipeline_state_stream_render_target_formats-structure"></a><span data-ttu-id="48bde-104">\_ \_ \_ \_ \_ Структура форматов целевого объекта подготовки потока состояния конвейера CD3DX12 \_</span><span class="sxs-lookup"><span data-stu-id="48bde-104">CD3DX12\_PIPELINE\_STATE\_STREAM\_RENDER\_TARGET\_FORMATS structure</span></span>

<span data-ttu-id="48bde-105">Вспомогательная структура, используемая для описания форматов целевого объекта отрисовки в виде одного объекта, подходящего для описания потока.</span><span class="sxs-lookup"><span data-stu-id="48bde-105">A helper structure used to describe the render target formats as a single object suitable for a stream description.</span></span>

## <a name="syntax"></a><span data-ttu-id="48bde-106">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="48bde-106">Syntax</span></span>


```C++
struct CD3DX12_PIPELINE_STATE_STREAM_RENDER_TARGET_FORMATS {
                                                      CD3DX12_PIPELINE_STATE_STREAM_RENDER_TARGET_FORMATS;
                                                      CD3DX12_PIPELINE_STATE_STREAM_RENDER_TARGET_FORMATS(D3D12_RT_FORMAT_ARRAY const &i);
  CD3DX12_PIPELINE_STATE_STREAM_RENDER_TARGET_FORMATS operator=(D3D12_RT_FORMAT_ARRAY const& i);
                                                      operator D3D12_RT_FORMAT_ARRAY() const;
};
```



## <a name="members"></a><span data-ttu-id="48bde-107">Члены</span><span class="sxs-lookup"><span data-stu-id="48bde-107">Members</span></span>

<dl> <dt>

<span data-ttu-id="48bde-108">**\_ \_ \_ \_ \_ Форматы целевого объекта подготовки потока состояния конвейера CD3DX12 \_**</span><span class="sxs-lookup"><span data-stu-id="48bde-108">**CD3DX12\_PIPELINE\_STATE\_STREAM\_RENDER\_TARGET\_FORMATS**</span></span>
</dt> <dd>

<span data-ttu-id="48bde-109">Создает новый, неинициализированный экземпляр \_ потока состояния конвейера CD3DX12, \_ \_ \_ предназначенный для подготовки к просмотру \_ целевых \_ форматов.</span><span class="sxs-lookup"><span data-stu-id="48bde-109">Creates a new, uninitialized, instance of a CD3DX12\_PIPELINE\_STATE\_STREAM\_RENDER\_TARGET\_FORMATS.</span></span>

</dd> <dt>

<span data-ttu-id="48bde-110">**\_ \_ \_ Форматы целевого объекта подготовки потока состояния конвейера CD3DX12 \_ \_ \_ ( \_ \_ \_ константа D3D12 массива формата RT &i)**</span><span class="sxs-lookup"><span data-stu-id="48bde-110">**CD3DX12\_PIPELINE\_STATE\_STREAM\_RENDER\_TARGET\_FORMATS(D3D12\_RT\_FORMAT\_ARRAY const &i)**</span></span>
</dt> <dd>

<span data-ttu-id="48bde-111">Создает новый экземпляр \_ потока состояния конвейера CD3DX12 \_ для \_ \_ подготовки к просмотру \_ целевых форматов \_ , инициализированных с типом подобъекта типа **\_ подобъекта состояния конвейера D3D12, для \_ \_ \_ \_ отображения \_ целевых \_ форматов** и данных подобъектов, скопированных из *i*, структуры [**\_ \_ \_ массива формата D3D12 RT**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_rt_format_array) .</span><span class="sxs-lookup"><span data-stu-id="48bde-111">Creates a new instance of a CD3DX12\_PIPELINE\_STATE\_STREAM\_RENDER\_TARGET\_FORMATS, initialized with a subobject type of **D3D12\_PIPELINE\_STATE\_SUBOBJECT\_TYPE\_RENDER\_TARGET\_FORMATS** and subobject data copied from *i*, a [**D3D12\_RT\_FORMAT\_ARRAY**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_rt_format_array) structure.</span></span>

</dd> <dt>

<span data-ttu-id="48bde-112">**operator = (D3D12 \_ \_ массива формата RT \_ const& i)**</span><span class="sxs-lookup"><span data-stu-id="48bde-112">**operator=(D3D12\_RT\_FORMAT\_ARRAY const& i)**</span></span>
</dt> <dd>

<span data-ttu-id="48bde-113">Оператор присваивания копирования.</span><span class="sxs-lookup"><span data-stu-id="48bde-113">Copy-assignment operator.</span></span>

</dd> <dt>

<span data-ttu-id="48bde-114">**\_ \_ const-оператор D3D12 массив формата RT \_ () константа**</span><span class="sxs-lookup"><span data-stu-id="48bde-114">**operator D3D12\_RT\_FORMAT\_ARRAY() const**</span></span>
</dt> <dd>

<span data-ttu-id="48bde-115">Неявное преобразование в структуру [**\_ \_ \_ массива формата D3D12 RT**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_rt_format_array) .</span><span class="sxs-lookup"><span data-stu-id="48bde-115">Implicit conversion to a [**D3D12\_RT\_FORMAT\_ARRAY**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_rt_format_array) structure.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="48bde-116">Комментарии</span><span class="sxs-lookup"><span data-stu-id="48bde-116">Remarks</span></span>

<span data-ttu-id="48bde-117">\_ \_ \_ Форматы целевого объекта подготовки потока состояния конвейера CD3DX12 \_ \_ \_ представляют собой специализацию typedef шаблона [**\_ \_ \_ \_ подобъекта потока состояния конвейера CD3DX12**](cd3dx12-pipeline-state-stream-subobject.md) и определяется следующим образом:</span><span class="sxs-lookup"><span data-stu-id="48bde-117">CD3DX12\_PIPELINE\_STATE\_STREAM\_RENDER\_TARGET\_FORMATS is a typedef specialization of the [**CD3DX12\_PIPELINE\_STATE\_STREAM\_SUBOBJECT**](cd3dx12-pipeline-state-stream-subobject.md) template, and is defined as follows:</span></span>


```C++
typedef CD3DX12_PIPELINE_STATE_STREAM_SUBOBJECT<D3D12_RT_FORMAT_ARRAY, D3D12_PIPELINE_STATE_SUBOBJECT_TYPE_RENDER_TARGET_FORMATS>
    CD3DX12_PIPELINE_STATE_STREAM_RENDER_TARGET_FORMATS;
          
```



## <a name="requirements"></a><span data-ttu-id="48bde-118">Требования</span><span class="sxs-lookup"><span data-stu-id="48bde-118">Requirements</span></span>



| <span data-ttu-id="48bde-119">Требование</span><span class="sxs-lookup"><span data-stu-id="48bde-119">Requirement</span></span> | <span data-ttu-id="48bde-120">Значение</span><span class="sxs-lookup"><span data-stu-id="48bde-120">Value</span></span> |
|-------------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="48bde-121">Header</span><span class="sxs-lookup"><span data-stu-id="48bde-121">Header</span></span><br/> | <dl> <span data-ttu-id="48bde-122"><dt>D3dx12. h</dt></span><span class="sxs-lookup"><span data-stu-id="48bde-122"><dt>D3dx12.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="48bde-123">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="48bde-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="48bde-124">Вспомогательные структуры для D3D12</span><span class="sxs-lookup"><span data-stu-id="48bde-124">Helper Structures for D3D12</span></span>](helper-structures-for-d3d12.md)
</dt> <dt>

[<span data-ttu-id="48bde-125">**\_Подобъект \_ потока состояния КОНВЕЙЕРа CD3DX12 \_ \_**</span><span class="sxs-lookup"><span data-stu-id="48bde-125">**CD3DX12\_PIPELINE\_STATE\_STREAM\_SUBOBJECT**</span></span>](cd3dx12-pipeline-state-stream-subobject.md)
</dt> <dt>

[<span data-ttu-id="48bde-126">**\_ \_ \_ Тип подобъекта состояния конвейера D3D12 \_**</span><span class="sxs-lookup"><span data-stu-id="48bde-126">**D3D12\_PIPELINE\_STATE\_SUBOBJECT\_TYPE**</span></span>](/windows/desktop/api/d3d12/ne-d3d12-d3d12_pipeline_state_subobject_type)
</dt> </dl>

 

