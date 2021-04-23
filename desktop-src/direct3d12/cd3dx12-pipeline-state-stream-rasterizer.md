---
title: Структура CD3DX12_PIPELINE_STATE_STREAM_RASTERIZER (D3dx12. h)
description: Вспомогательная структура, используемая для описания описания средства развертки в виде одного объекта, подходящего для описания потока.
ms.assetid: 650C2DA3-63FB-44D1-BE9A-E21E13DA24DB
keywords:
- Структура CD3DX12_PIPELINE_STATE_STREAM_RASTERIZER
topic_type:
- apiref
api_name:
- CD3DX12_PIPELINE_STATE_STREAM_RASTERIZER
api_location:
- d3dx12.h
api_type:
- HeaderDef
ms.localizationpriority: low
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f656ad354430b00e757ece0aa2ce482de1f06e2e
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/15/2021
ms.locfileid: "105694093"
---
# <a name="cd3dx12_pipeline_state_stream_rasterizer-structure"></a><span data-ttu-id="7ad01-104">Структура средства программной \_ \_ \_ прорисовки потока состояния конвейера CD3DX12 \_</span><span class="sxs-lookup"><span data-stu-id="7ad01-104">CD3DX12\_PIPELINE\_STATE\_STREAM\_RASTERIZER structure</span></span>

<span data-ttu-id="7ad01-105">Вспомогательная структура, используемая для описания описания средства развертки в виде одного объекта, подходящего для описания потока.</span><span class="sxs-lookup"><span data-stu-id="7ad01-105">A helper structure used to describe a rasterizer description as a single object suitable for a stream description.</span></span>

## <a name="syntax"></a><span data-ttu-id="7ad01-106">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="7ad01-106">Syntax</span></span>


```C++
struct CD3DX12_PIPELINE_STATE_STREAM_RASTERIZER {
                                           CD3DX12_PIPELINE_STATE_STREAM_RASTERIZER;
                                           CD3DX12_PIPELINE_STATE_STREAM_RASTERIZER(CD3DX12_RASTERIZER_DESC const &i);
  CD3DX12_PIPELINE_STATE_STREAM_RASTERIZER operator=(CD3DX12_RASTERIZER_DESC const& i);
                                           operator CD3DX12_RASTERIZER_DESC() const;
};
```



## <a name="members"></a><span data-ttu-id="7ad01-107">Члены</span><span class="sxs-lookup"><span data-stu-id="7ad01-107">Members</span></span>

<dl> <dt>

<span data-ttu-id="7ad01-108">**Средство программной \_ \_ \_ прорисовки потока состояния конвейера CD3DX12 \_**</span><span class="sxs-lookup"><span data-stu-id="7ad01-108">**CD3DX12\_PIPELINE\_STATE\_STREAM\_RASTERIZER**</span></span>
</dt> <dd>

<span data-ttu-id="7ad01-109">Создает новый, неинициализированный экземпляр средства программной \_ \_ прорисовки потока состояния конвейера CD3DX12 \_ \_ .</span><span class="sxs-lookup"><span data-stu-id="7ad01-109">Creates a new, uninitialized, instance of a CD3DX12\_PIPELINE\_STATE\_STREAM\_RASTERIZER.</span></span>

</dd> <dt>

<span data-ttu-id="7ad01-110">**Средство программной \_ \_ прорисовки потока состояния конвейера CD3DX12 (CD3DX12 средство программной \_ \_ \_ прорисовки \_ DESC const &i)**</span><span class="sxs-lookup"><span data-stu-id="7ad01-110">**CD3DX12\_PIPELINE\_STATE\_STREAM\_RASTERIZER(CD3DX12\_RASTERIZER\_DESC const &i)**</span></span>
</dt> <dd>

<span data-ttu-id="7ad01-111">Создает новый экземпляр средства программной \_ \_ прорисовки потока состояния конвейера CD3DX12, инициализированного с типом подобъекта для типа подобъекта \_ \_ **\_ \_ состояния \_ \_ \_ конвейера D3D12** и данными подобъекта, скопированными из *i*, структурой [**\_ \_ DESC средства прорисовки CD3DX12**](cd3dx12-rasterizer-desc.md) .</span><span class="sxs-lookup"><span data-stu-id="7ad01-111">Creates a new instance of a CD3DX12\_PIPELINE\_STATE\_STREAM\_RASTERIZER, initialized with a subobject type of **D3D12\_PIPELINE\_STATE\_SUBOBJECT\_TYPE\_RASTERIZER** and subobject data copied from *i*, a [**CD3DX12\_RASTERIZER\_DESC**](cd3dx12-rasterizer-desc.md) structure.</span></span>

</dd> <dt>

<span data-ttu-id="7ad01-112">**operator = (CD3DX12 средство программной \_ прорисовки \_ DESC const& i)**</span><span class="sxs-lookup"><span data-stu-id="7ad01-112">**operator=(CD3DX12\_RASTERIZER\_DESC const& i)**</span></span>
</dt> <dd>

<span data-ttu-id="7ad01-113">Оператор присваивания копирования.</span><span class="sxs-lookup"><span data-stu-id="7ad01-113">Copy-assignment operator.</span></span>

</dd> <dt>

<span data-ttu-id="7ad01-114">**const CD3DX12 "оператор средства \_ растеризации \_ DESC ()"**</span><span class="sxs-lookup"><span data-stu-id="7ad01-114">**operator CD3DX12\_RASTERIZER\_DESC() const**</span></span>
</dt> <dd>

<span data-ttu-id="7ad01-115">Неявное преобразование в структуру CD3DX12 средства программной [**\_ прорисовки \_**](cd3dx12-rasterizer-desc.md) .</span><span class="sxs-lookup"><span data-stu-id="7ad01-115">Implicit conversion to a [**CD3DX12\_RASTERIZER\_DESC**](cd3dx12-rasterizer-desc.md) structure.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="7ad01-116">Комментарии</span><span class="sxs-lookup"><span data-stu-id="7ad01-116">Remarks</span></span>

<span data-ttu-id="7ad01-117">Средство программной \_ \_ прорисовки потока состояния конвейера CD3DX12 \_ \_ является специализацией typedef шаблона [**\_ \_ \_ \_ подобъекта потока состояния конвейера CD3DX12**](cd3dx12-pipeline-state-stream-subobject.md) и определяется следующим образом:</span><span class="sxs-lookup"><span data-stu-id="7ad01-117">CD3DX12\_PIPELINE\_STATE\_STREAM\_RASTERIZER is a typedef specialization of the [**CD3DX12\_PIPELINE\_STATE\_STREAM\_SUBOBJECT**](cd3dx12-pipeline-state-stream-subobject.md) template, and is defined as follows:</span></span>


```C++
typedef CD3DX12_PIPELINE_STATE_STREAM_SUBOBJECT<CD3DX12_RASTERIZER_DESC, D3D12_PIPELINE_STATE_SUBOBJECT_TYPE_RASTERIZER, CD3DX12_DEFAULT>
    CD3DX12_PIPELINE_STATE_STREAM_RASTERIZER;
          
```



## <a name="requirements"></a><span data-ttu-id="7ad01-118">Требования</span><span class="sxs-lookup"><span data-stu-id="7ad01-118">Requirements</span></span>



| <span data-ttu-id="7ad01-119">Требование</span><span class="sxs-lookup"><span data-stu-id="7ad01-119">Requirement</span></span> | <span data-ttu-id="7ad01-120">Значение</span><span class="sxs-lookup"><span data-stu-id="7ad01-120">Value</span></span> |
|-------------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="7ad01-121">Header</span><span class="sxs-lookup"><span data-stu-id="7ad01-121">Header</span></span><br/> | <dl> <span data-ttu-id="7ad01-122"><dt>D3dx12. h</dt></span><span class="sxs-lookup"><span data-stu-id="7ad01-122"><dt>D3dx12.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="7ad01-123">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="7ad01-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="7ad01-124">Вспомогательные структуры для D3D12</span><span class="sxs-lookup"><span data-stu-id="7ad01-124">Helper Structures for D3D12</span></span>](helper-structures-for-d3d12.md)
</dt> <dt>

[<span data-ttu-id="7ad01-125">**\_Подобъект \_ потока состояния КОНВЕЙЕРа CD3DX12 \_ \_**</span><span class="sxs-lookup"><span data-stu-id="7ad01-125">**CD3DX12\_PIPELINE\_STATE\_STREAM\_SUBOBJECT**</span></span>](cd3dx12-pipeline-state-stream-subobject.md)
</dt> <dt>

[<span data-ttu-id="7ad01-126">**\_ \_ \_ Тип подобъекта состояния конвейера D3D12 \_**</span><span class="sxs-lookup"><span data-stu-id="7ad01-126">**D3D12\_PIPELINE\_STATE\_SUBOBJECT\_TYPE**</span></span>](/windows/desktop/api/d3d12/ne-d3d12-d3d12_pipeline_state_subobject_type)
</dt> </dl>

 

