---
title: Структура CD3DX12_PIPELINE_STATE_STREAM_NODE_MASK (D3dx12. h)
description: Вспомогательная структура, используемая для описания маски узла в виде одного объекта, подходящего для описания потока.
ms.assetid: 5C770D9A-D692-46CF-8D60-EE5EB04998C8
keywords:
- Структура CD3DX12_PIPELINE_STATE_STREAM_NODE_MASK
topic_type:
- apiref
api_name:
- CD3DX12_PIPELINE_STATE_STREAM_NODE_MASK
api_location:
- d3dx12.h
api_type:
- HeaderDef
ms.localizationpriority: low
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f9c364ecd20459d8c20bdd3d30b969cc3b9ae46d
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/15/2021
ms.locfileid: "105651541"
---
# <a name="cd3dx12_pipeline_state_stream_node_mask-structure"></a><span data-ttu-id="11ceb-104">\_ \_ \_ \_ Структура маски узла потока состояния конвейера CD3DX12 \_</span><span class="sxs-lookup"><span data-stu-id="11ceb-104">CD3DX12\_PIPELINE\_STATE\_STREAM\_NODE\_MASK structure</span></span>

<span data-ttu-id="11ceb-105">Вспомогательная структура, используемая для описания маски узла в виде одного объекта, подходящего для описания потока.</span><span class="sxs-lookup"><span data-stu-id="11ceb-105">A helper structure used to describe a node mask as a single object suitable for a stream description.</span></span>

## <a name="syntax"></a><span data-ttu-id="11ceb-106">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="11ceb-106">Syntax</span></span>


```C++
struct CD3DX12_PIPELINE_STATE_STREAM_NODE_MASK {
                                          CD3DX12_PIPELINE_STATE_STREAM_NODE_MASK;
                                          CD3DX12_PIPELINE_STATE_STREAM_NODE_MASK(UINT const &i);
  CD3DX12_PIPELINE_STATE_STREAM_NODE_MASK operator=(UINT const& i);
                                          operator UINT() const;
};
```



## <a name="members"></a><span data-ttu-id="11ceb-107">Члены</span><span class="sxs-lookup"><span data-stu-id="11ceb-107">Members</span></span>

<dl> <dt>

<span data-ttu-id="11ceb-108">**\_ \_ \_ \_ Маска узла потока состояния конвейера CD3DX12 \_**</span><span class="sxs-lookup"><span data-stu-id="11ceb-108">**CD3DX12\_PIPELINE\_STATE\_STREAM\_NODE\_MASK**</span></span>
</dt> <dd>

<span data-ttu-id="11ceb-109">Создает новый, неинициализированный экземпляр \_ \_ \_ маски узла потока состояния конвейера CD3DX12 \_ \_ .</span><span class="sxs-lookup"><span data-stu-id="11ceb-109">Creates a new, uninitialized, instance of a CD3DX12\_PIPELINE\_STATE\_STREAM\_NODE\_MASK.</span></span>

</dd> <dt>

<span data-ttu-id="11ceb-110">**CD3DX12 \_ \_ \_ Маска узла потока состояния конвейера \_ \_ (uint const &i)**</span><span class="sxs-lookup"><span data-stu-id="11ceb-110">**CD3DX12\_PIPELINE\_STATE\_STREAM\_NODE\_MASK(UINT const &i)**</span></span>
</dt> <dd>

<span data-ttu-id="11ceb-111">Создает новый экземпляр \_ \_ маски узла потока состояния конвейера \_ CD3DX12 \_ \_ , инициализированный с типом подобъекта для типа **\_ \_ подобъекта состояния конвейера D3D12 " \_ \_ \_ \_ Маска узла** " и "данные подобъекта", скопированные из *i*, маску узла **uint** .</span><span class="sxs-lookup"><span data-stu-id="11ceb-111">Creates a new instance of a CD3DX12\_PIPELINE\_STATE\_STREAM\_NODE\_MASK, initialized with a subobject type of **D3D12\_PIPELINE\_STATE\_SUBOBJECT\_TYPE\_NODE\_MASK** and subobject data copied from *i*, a **UINT** node mask.</span></span>

</dd> <dt>

<span data-ttu-id="11ceb-112">**operator = (Конст const& i)**</span><span class="sxs-lookup"><span data-stu-id="11ceb-112">**operator=(UINT const& i)**</span></span>
</dt> <dd>

<span data-ttu-id="11ceb-113">Оператор присваивания копирования.</span><span class="sxs-lookup"><span data-stu-id="11ceb-113">Copy-assignment operator.</span></span>

</dd> <dt>

<span data-ttu-id="11ceb-114">**const оператора UINT ()**</span><span class="sxs-lookup"><span data-stu-id="11ceb-114">**operator UINT() const**</span></span>
</dt> <dd>

<span data-ttu-id="11ceb-115">Неявное преобразование в маску узла **uint** .</span><span class="sxs-lookup"><span data-stu-id="11ceb-115">Implicit conversion to a **UINT** node mask.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="11ceb-116">Комментарии</span><span class="sxs-lookup"><span data-stu-id="11ceb-116">Remarks</span></span>

<span data-ttu-id="11ceb-117">\_ \_ Маска узла потока состояния конвейера CD3DX12 \_ \_ \_ является СПЕЦИАЛИЗАЦИей typedef шаблона [**\_ \_ \_ \_ подобъекта потока состояния конвейера CD3DX12**](cd3dx12-pipeline-state-stream-subobject.md) и определяется следующим образом:</span><span class="sxs-lookup"><span data-stu-id="11ceb-117">CD3DX12\_PIPELINE\_STATE\_STREAM\_NODE\_MASK is a typedef specialization of the [**CD3DX12\_PIPELINE\_STATE\_STREAM\_SUBOBJECT**](cd3dx12-pipeline-state-stream-subobject.md) template, and is defined as follows:</span></span>


```C++
typedef CD3DX12_PIPELINE_STATE_STREAM_SUBOBJECT<UINT, D3D12_PIPELINE_STATE_SUBOBJECT_TYPE_NODE_MASK>
    CD3DX12_PIPELINE_STATE_STREAM_NODE_MASK;
          
```



## <a name="requirements"></a><span data-ttu-id="11ceb-118">Требования</span><span class="sxs-lookup"><span data-stu-id="11ceb-118">Requirements</span></span>



| <span data-ttu-id="11ceb-119">Требование</span><span class="sxs-lookup"><span data-stu-id="11ceb-119">Requirement</span></span> | <span data-ttu-id="11ceb-120">Значение</span><span class="sxs-lookup"><span data-stu-id="11ceb-120">Value</span></span> |
|-------------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="11ceb-121">Header</span><span class="sxs-lookup"><span data-stu-id="11ceb-121">Header</span></span><br/> | <dl> <span data-ttu-id="11ceb-122"><dt>D3dx12. h</dt></span><span class="sxs-lookup"><span data-stu-id="11ceb-122"><dt>D3dx12.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="11ceb-123">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="11ceb-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="11ceb-124">Вспомогательные структуры для D3D12</span><span class="sxs-lookup"><span data-stu-id="11ceb-124">Helper Structures for D3D12</span></span>](helper-structures-for-d3d12.md)
</dt> <dt>

[<span data-ttu-id="11ceb-125">**\_Подобъект \_ потока состояния КОНВЕЙЕРа CD3DX12 \_ \_**</span><span class="sxs-lookup"><span data-stu-id="11ceb-125">**CD3DX12\_PIPELINE\_STATE\_STREAM\_SUBOBJECT**</span></span>](cd3dx12-pipeline-state-stream-subobject.md)
</dt> <dt>

[<span data-ttu-id="11ceb-126">**\_ \_ \_ Тип подобъекта состояния конвейера D3D12 \_**</span><span class="sxs-lookup"><span data-stu-id="11ceb-126">**D3D12\_PIPELINE\_STATE\_SUBOBJECT\_TYPE**</span></span>](/windows/desktop/api/d3d12/ne-d3d12-d3d12_pipeline_state_subobject_type)
</dt> </dl>

 

