---
title: Структура CD3DX12_PIPELINE_STATE_STREAM_DS (D3dx12. h)
description: Вспомогательная структура, используемая для описания шейдера домена как одного объекта, подходящего для описания потока.
ms.assetid: 42F8B7C1-B754-4B07-BF04-DBF450A942E6
keywords:
- Структура CD3DX12_PIPELINE_STATE_STREAM_DS
topic_type:
- apiref
api_name:
- CD3DX12_PIPELINE_STATE_STREAM_DS
api_location:
- d3dx12.h
api_type:
- HeaderDef
ms.localizationpriority: low
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: dbae1d75894e1fb8ffaa5bf95a45cc1eb3b2d9f2
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/15/2021
ms.locfileid: "105647809"
---
# <a name="cd3dx12_pipeline_state_stream_ds-structure"></a><span data-ttu-id="1081b-104">\_ \_ \_ Структура DS потока состояния конвейера CD3DX12 \_</span><span class="sxs-lookup"><span data-stu-id="1081b-104">CD3DX12\_PIPELINE\_STATE\_STREAM\_DS structure</span></span>

<span data-ttu-id="1081b-105">Вспомогательная структура, используемая для описания шейдера домена как одного объекта, подходящего для описания потока.</span><span class="sxs-lookup"><span data-stu-id="1081b-105">A helper structure used to describe a domain shader as a single object suitable for a stream description.</span></span>

## <a name="syntax"></a><span data-ttu-id="1081b-106">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="1081b-106">Syntax</span></span>


```C++
struct CD3DX12_PIPELINE_STATE_STREAM_DS {
                                   CD3DX12_PIPELINE_STATE_STREAM_DS;
                                   CD3DX12_PIPELINE_STATE_STREAM_DS(D3D12_SHADER_BYTECODE const &i);
  CD3DX12_PIPELINE_STATE_STREAM_DS operator=(D3D12_SHADER_BYTECODE const& i);
                                   operator D3D12_SHADER_BYTECODE() const;
};
```



## <a name="members"></a><span data-ttu-id="1081b-107">Члены</span><span class="sxs-lookup"><span data-stu-id="1081b-107">Members</span></span>

<dl> <dt>

<span data-ttu-id="1081b-108">**\_ \_ \_ DS потока состояния конвейера CD3DX12 \_**</span><span class="sxs-lookup"><span data-stu-id="1081b-108">**CD3DX12\_PIPELINE\_STATE\_STREAM\_DS**</span></span>
</dt> <dd>

<span data-ttu-id="1081b-109">Создает новый, неинициализированный экземпляр \_ потока состояния конвейера CD3DX12 \_ \_ \_ .</span><span class="sxs-lookup"><span data-stu-id="1081b-109">Creates a new, uninitialized, instance of a CD3DX12\_PIPELINE\_STATE\_STREAM\_DS.</span></span>

</dd> <dt>

<span data-ttu-id="1081b-110">**\_ \_ DS потока состояния конвейера CD3DX12 \_ \_ ( \_ байт-код шейдера D3D12 \_ &i)**</span><span class="sxs-lookup"><span data-stu-id="1081b-110">**CD3DX12\_PIPELINE\_STATE\_STREAM\_DS(D3D12\_SHADER\_BYTECODE const &i)**</span></span>
</dt> <dd>

<span data-ttu-id="1081b-111">Создает новый экземпляр \_ потока состояния конвейера CD3DX12 \_ \_ \_ , инициализируемый с типом подобъекта для типа **\_ \_ \_ подобъекта состояния \_ \_ конвейера D3D12 данные DS** и подобъекта, скопированные из *i*, структура [**байт- \_ \_ кода шейдера D3D12**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_shader_bytecode) .</span><span class="sxs-lookup"><span data-stu-id="1081b-111">Creates a new instance of a CD3DX12\_PIPELINE\_STATE\_STREAM\_DS, initialized with a subobject type of **D3D12\_PIPELINE\_STATE\_SUBOBJECT\_TYPE\_DS** and subobject data copied from *i*, a [**D3D12\_SHADER\_BYTECODE**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_shader_bytecode) structure.</span></span>

</dd> <dt>

<span data-ttu-id="1081b-112">**operator = (D3D12ный байт-код \_ шейдера \_ "i"& i)**</span><span class="sxs-lookup"><span data-stu-id="1081b-112">**operator=(D3D12\_SHADER\_BYTECODE const& i)**</span></span>
</dt> <dd>

<span data-ttu-id="1081b-113">Оператор присваивания копирования.</span><span class="sxs-lookup"><span data-stu-id="1081b-113">Copy-assignment operator.</span></span>

</dd> <dt>

<span data-ttu-id="1081b-114">**\_константа-код шейдера оператора D3D12 \_ () const**</span><span class="sxs-lookup"><span data-stu-id="1081b-114">**operator D3D12\_SHADER\_BYTECODE() const**</span></span>
</dt> <dd>

<span data-ttu-id="1081b-115">Неявное преобразование в структуру [**\_ байт- \_ кода шейдера D3D12**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_shader_bytecode) .</span><span class="sxs-lookup"><span data-stu-id="1081b-115">Implicit conversion to a [**D3D12\_SHADER\_BYTECODE**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_shader_bytecode) structure.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="1081b-116">Комментарии</span><span class="sxs-lookup"><span data-stu-id="1081b-116">Remarks</span></span>

<span data-ttu-id="1081b-117">\_Поток состояния конвейера CD3DX12 \_ \_ \_ является специализацией typedef шаблона [**\_ \_ \_ \_ подобъекта потока состояния конвейера CD3DX12**](cd3dx12-pipeline-state-stream-subobject.md) и определяется следующим образом:</span><span class="sxs-lookup"><span data-stu-id="1081b-117">CD3DX12\_PIPELINE\_STATE\_STREAM\_DS is a typedef specialization of the [**CD3DX12\_PIPELINE\_STATE\_STREAM\_SUBOBJECT**](cd3dx12-pipeline-state-stream-subobject.md) template, and is defined as follows:</span></span>


```C++
typedef CD3DX12_PIPELINE_STATE_STREAM_SUBOBJECT<D3D12_SHADER_BYTECODE, D3D12_PIPELINE_STATE_SUBOBJECT_TYPE_DS>
    CD3DX12_PIPELINE_STATE_STREAM_DS;
          
```



## <a name="requirements"></a><span data-ttu-id="1081b-118">Требования</span><span class="sxs-lookup"><span data-stu-id="1081b-118">Requirements</span></span>



| <span data-ttu-id="1081b-119">Требование</span><span class="sxs-lookup"><span data-stu-id="1081b-119">Requirement</span></span> | <span data-ttu-id="1081b-120">Значение</span><span class="sxs-lookup"><span data-stu-id="1081b-120">Value</span></span> |
|-------------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="1081b-121">Header</span><span class="sxs-lookup"><span data-stu-id="1081b-121">Header</span></span><br/> | <dl> <span data-ttu-id="1081b-122"><dt>D3dx12. h</dt></span><span class="sxs-lookup"><span data-stu-id="1081b-122"><dt>D3dx12.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="1081b-123">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="1081b-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="1081b-124">Вспомогательные структуры для D3D12</span><span class="sxs-lookup"><span data-stu-id="1081b-124">Helper Structures for D3D12</span></span>](helper-structures-for-d3d12.md)
</dt> <dt>

[<span data-ttu-id="1081b-125">**\_Подобъект \_ потока состояния КОНВЕЙЕРа CD3DX12 \_ \_**</span><span class="sxs-lookup"><span data-stu-id="1081b-125">**CD3DX12\_PIPELINE\_STATE\_STREAM\_SUBOBJECT**</span></span>](cd3dx12-pipeline-state-stream-subobject.md)
</dt> <dt>

[<span data-ttu-id="1081b-126">**\_ \_ \_ Тип подобъекта состояния конвейера D3D12 \_**</span><span class="sxs-lookup"><span data-stu-id="1081b-126">**D3D12\_PIPELINE\_STATE\_SUBOBJECT\_TYPE**</span></span>](/windows/desktop/api/d3d12/ne-d3d12-d3d12_pipeline_state_subobject_type)
</dt> </dl>

 

