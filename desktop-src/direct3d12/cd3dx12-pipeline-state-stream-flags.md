---
title: Структура CD3DX12_PIPELINE_STATE_STREAM_FLAGS (D3dx12. h)
description: Вспомогательная структура, используемая для описания флагов состояния конвейера в виде одного объекта, подходящего для описания потока.
ms.assetid: EF67936B-315A-4B3F-9E07-7CF4C5EE47CF
keywords:
- Структура CD3DX12_PIPELINE_STATE_STREAM_FLAGS
topic_type:
- apiref
api_name:
- CD3DX12_PIPELINE_STATE_STREAM_FLAGS
api_location:
- d3dx12.h
api_type:
- HeaderDef
ms.localizationpriority: low
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 034f4a63c774ca41f28fbe9e6c2945fddee47c4f
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/15/2021
ms.locfileid: "105647891"
---
# <a name="cd3dx12_pipeline_state_stream_flags-structure"></a><span data-ttu-id="58f20-104">\_ \_ \_ \_ Структура флагов потока состояния конвейера CD3DX12</span><span class="sxs-lookup"><span data-stu-id="58f20-104">CD3DX12\_PIPELINE\_STATE\_STREAM\_FLAGS structure</span></span>

<span data-ttu-id="58f20-105">Вспомогательная структура, используемая для описания флагов состояния конвейера в виде одного объекта, подходящего для описания потока.</span><span class="sxs-lookup"><span data-stu-id="58f20-105">A helper structure used to describe pipeline state flags as a single object suitable for a stream description.</span></span>

## <a name="syntax"></a><span data-ttu-id="58f20-106">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="58f20-106">Syntax</span></span>


```C++
struct CD3DX12_PIPELINE_STATE_STREAM_FLAGS {
                                      CD3DX12_PIPELINE_STATE_STREAM_FLAGS;
                                      CD3DX12_PIPELINE_STATE_STREAM_FLAGS(D3D12_PIPELINE_STATE_FLAGS const &i);
  CD3DX12_PIPELINE_STATE_STREAM_FLAGS operator=(D3D12_PIPELINE_STATE_FLAGS const& i);
                                      operator D3D12_PIPELINE_STATE_FLAGS() const;
};
```



## <a name="members"></a><span data-ttu-id="58f20-107">Члены</span><span class="sxs-lookup"><span data-stu-id="58f20-107">Members</span></span>

<dl> <dt>

<span data-ttu-id="58f20-108">**\_ \_ \_ Флаги потока состояния конвейера CD3DX12 \_**</span><span class="sxs-lookup"><span data-stu-id="58f20-108">**CD3DX12\_PIPELINE\_STATE\_STREAM\_FLAGS**</span></span>
</dt> <dd>

<span data-ttu-id="58f20-109">Создает новый, неинициализированный экземпляр \_ \_ \_ флагов потока состояния конвейера CD3DX12 \_ .</span><span class="sxs-lookup"><span data-stu-id="58f20-109">Creates a new, uninitialized, instance of a CD3DX12\_PIPELINE\_STATE\_STREAM\_FLAGS.</span></span>

</dd> <dt>

<span data-ttu-id="58f20-110">**\_ \_ Флаги потока состояния конвейера CD3DX12 \_ \_ ( \_ \_ флаги состояния конвейера D3D12 \_ const &i)**</span><span class="sxs-lookup"><span data-stu-id="58f20-110">**CD3DX12\_PIPELINE\_STATE\_STREAM\_FLAGS(D3D12\_PIPELINE\_STATE\_FLAGS const &i)**</span></span>
</dt> <dd>

<span data-ttu-id="58f20-111">Создает новый экземпляр \_ \_ флагов потока состояния конвейера \_ CD3DX12 \_ , которые инициализируются с типом подобъекта **\_ \_ \_ \_ \_ флагов типа подобъекта состояния конвейера D3D12** и данными подобъектов, скопированными из *i*, структурой [**\_ \_ \_ флагов состояния конвейера D3D12**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_pipeline_state_flags) .</span><span class="sxs-lookup"><span data-stu-id="58f20-111">Creates a new instance of a CD3DX12\_PIPELINE\_STATE\_STREAM\_FLAGS, initialized with a subobject type of **D3D12\_PIPELINE\_STATE\_SUBOBJECT\_TYPE\_FLAGS** and subobject data copied from *i*, a [**D3D12\_PIPELINE\_STATE\_FLAGS**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_pipeline_state_flags) structure.</span></span>

</dd> <dt>

<span data-ttu-id="58f20-112">**operator = (D3D12 \_ \_ флаги состояния конвейера \_ "const"& i)**</span><span class="sxs-lookup"><span data-stu-id="58f20-112">**operator=(D3D12\_PIPELINE\_STATE\_FLAGS const& i)**</span></span>
</dt> <dd>

<span data-ttu-id="58f20-113">Оператор присваивания копирования.</span><span class="sxs-lookup"><span data-stu-id="58f20-113">Copy-assignment operator.</span></span>

</dd> <dt>

<span data-ttu-id="58f20-114">**\_флаг состояния конвейера оператора D3D12 \_ \_ () const**</span><span class="sxs-lookup"><span data-stu-id="58f20-114">**operator D3D12\_PIPELINE\_STATE\_FLAGS() const**</span></span>
</dt> <dd>

<span data-ttu-id="58f20-115">Неявное преобразование в структуру [**\_ \_ \_ флагов состояния конвейера D3D12**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_pipeline_state_flags) .</span><span class="sxs-lookup"><span data-stu-id="58f20-115">Implicit conversion to a [**D3D12\_PIPELINE\_STATE\_FLAGS**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_pipeline_state_flags) structure.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="58f20-116">Комментарии</span><span class="sxs-lookup"><span data-stu-id="58f20-116">Remarks</span></span>

<span data-ttu-id="58f20-117">\_ \_ Флаги потока состояния конвейера CD3DX12 \_ \_ являются специализацией typedef [**шаблона \_ \_ \_ \_ подобъекта потока состояния конвейера CD3DX12**](cd3dx12-pipeline-state-stream-subobject.md) и определяются следующим образом:</span><span class="sxs-lookup"><span data-stu-id="58f20-117">CD3DX12\_PIPELINE\_STATE\_STREAM\_FLAGS is a typedef specialization of the [**CD3DX12\_PIPELINE\_STATE\_STREAM\_SUBOBJECT**](cd3dx12-pipeline-state-stream-subobject.md) template, and is defined as follows:</span></span>


```C++
typedef CD3DX12_PIPELINE_STATE_STREAM_SUBOBJECT<D3D12_PIPELINE_STATE_FLAGS, D3D12_PIPELINE_STATE_SUBOBJECT_TYPE_FLAGS>
    CD3DX12_PIPELINE_STATE_STREAM_FLAGS;
          
```



## <a name="requirements"></a><span data-ttu-id="58f20-118">Требования</span><span class="sxs-lookup"><span data-stu-id="58f20-118">Requirements</span></span>



| <span data-ttu-id="58f20-119">Требование</span><span class="sxs-lookup"><span data-stu-id="58f20-119">Requirement</span></span> | <span data-ttu-id="58f20-120">Значение</span><span class="sxs-lookup"><span data-stu-id="58f20-120">Value</span></span> |
|-------------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="58f20-121">Header</span><span class="sxs-lookup"><span data-stu-id="58f20-121">Header</span></span><br/> | <dl> <span data-ttu-id="58f20-122"><dt>D3dx12. h</dt></span><span class="sxs-lookup"><span data-stu-id="58f20-122"><dt>D3dx12.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="58f20-123">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="58f20-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="58f20-124">Вспомогательные структуры для D3D12</span><span class="sxs-lookup"><span data-stu-id="58f20-124">Helper Structures for D3D12</span></span>](helper-structures-for-d3d12.md)
</dt> <dt>

[<span data-ttu-id="58f20-125">**\_Подобъект \_ потока состояния КОНВЕЙЕРа CD3DX12 \_ \_**</span><span class="sxs-lookup"><span data-stu-id="58f20-125">**CD3DX12\_PIPELINE\_STATE\_STREAM\_SUBOBJECT**</span></span>](cd3dx12-pipeline-state-stream-subobject.md)
</dt> <dt>

[<span data-ttu-id="58f20-126">**\_ \_ \_ Тип подобъекта состояния конвейера D3D12 \_**</span><span class="sxs-lookup"><span data-stu-id="58f20-126">**D3D12\_PIPELINE\_STATE\_SUBOBJECT\_TYPE**</span></span>](/windows/desktop/api/d3d12/ne-d3d12-d3d12_pipeline_state_subobject_type)
</dt> </dl>

 

