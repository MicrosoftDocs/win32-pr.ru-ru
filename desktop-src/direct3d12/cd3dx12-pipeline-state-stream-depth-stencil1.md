---
title: Структура CD3DX12_PIPELINE_STATE_STREAM_DEPTH_STENCIL1 (D3dx12. h)
description: Вспомогательная структура, используемая для описания описания трафарета глубины в виде одного объекта, подходящего для описания потока. | Структура CD3DX12_PIPELINE_STATE_STREAM_DEPTH_STENCIL1 (D3dx12. h)
ms.assetid: 7D3554D9-610D-43B5-94F0-68167E966A86
keywords:
- Структура CD3DX12_PIPELINE_STATE_STREAM_DEPTH_STENCIL1
topic_type:
- apiref
api_name:
- CD3DX12_PIPELINE_STATE_STREAM_DEPTH_STENCIL1
api_location:
- d3dx12.h
api_type:
- HeaderDef
ms.localizationpriority: low
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ee95e9e37ad1dfced119848c76f071564aaa9435
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/15/2021
ms.locfileid: "105647810"
---
# <a name="cd3dx12_pipeline_state_stream_depth_stencil1-structure"></a><span data-ttu-id="7c54b-105">\_ \_ \_ \_ Структура STENCIL1 глубины потока состояния конвейера CD3DX12 \_</span><span class="sxs-lookup"><span data-stu-id="7c54b-105">CD3DX12\_PIPELINE\_STATE\_STREAM\_DEPTH\_STENCIL1 structure</span></span>

<span data-ttu-id="7c54b-106">Вспомогательная структура, используемая для описания описания трафарета глубины в виде одного объекта, подходящего для описания потока.</span><span class="sxs-lookup"><span data-stu-id="7c54b-106">A helper structure used to describe a depth stencil description as a single object suitable for a stream description.</span></span>

## <a name="syntax"></a><span data-ttu-id="7c54b-107">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="7c54b-107">Syntax</span></span>


```C++
struct CD3DX12_PIPELINE_STATE_STREAM_DEPTH_STENCIL1 {
                                               CD3DX12_PIPELINE_STATE_STREAM_DEPTH_STENCIL1;
                                               CD3DX12_PIPELINE_STATE_STREAM_DEPTH_STENCIL1(CD3DX12_DEPTH_STENCIL_DESC1 const &i);
  CD3DX12_PIPELINE_STATE_STREAM_DEPTH_STENCIL1 operator=(CD3DX12_DEPTH_STENCIL_DESC1 const& i);
                                               operator CD3DX12_DEPTH_STENCIL_DESC1() const;
};
```



## <a name="members"></a><span data-ttu-id="7c54b-108">Члены</span><span class="sxs-lookup"><span data-stu-id="7c54b-108">Members</span></span>

<dl> <dt>

<span data-ttu-id="7c54b-109">**\_ \_ Глубина потока состояния конвейера CD3DX12 \_ \_ \_ STENCIL1**</span><span class="sxs-lookup"><span data-stu-id="7c54b-109">**CD3DX12\_PIPELINE\_STATE\_STREAM\_DEPTH\_STENCIL1**</span></span>
</dt> <dd>

<span data-ttu-id="7c54b-110">Создает новый, неинициализированный экземпляр CD3DX12 \_ \_ глубины потока состояния конвейера \_ \_ \_ STENCIL1.</span><span class="sxs-lookup"><span data-stu-id="7c54b-110">Creates a new, uninitialized, instance of a CD3DX12\_PIPELINE\_STATE\_STREAM\_DEPTH\_STENCIL1.</span></span>

</dd> <dt>

<span data-ttu-id="7c54b-111">**\_ \_ Глубина потока состояния конвейера CD3DX12 \_ \_ \_ STENCIL1 ( \_ \_ набор элементов глубины CD3DX12 \_ DESC1 const &i)**</span><span class="sxs-lookup"><span data-stu-id="7c54b-111">**CD3DX12\_PIPELINE\_STATE\_STREAM\_DEPTH\_STENCIL1(CD3DX12\_DEPTH\_STENCIL\_DESC1 const &i)**</span></span>
</dt> <dd>

<span data-ttu-id="7c54b-112">Создает новый экземпляр CD3DX12 \_ \_ глубины потока состояния конвейера \_ \_ \_ (STENCIL1), инициализируемый с типом подобъекта для типа **\_ \_ \_ \_ \_ вложенного \_ объекта состояния конвейера D3D12** , который копируется STENCIL1 и данные подобъектов, скопированные из *i*, CD3DX12 структуру [**\_ \_ набора элементов \_ глубины**](cd3dx12-depth-stencil-desc1.md) DESC1.</span><span class="sxs-lookup"><span data-stu-id="7c54b-112">Creates a new instance of a CD3DX12\_PIPELINE\_STATE\_STREAM\_DEPTH\_STENCIL1, initialized with a subobject type of **D3D12\_PIPELINE\_STATE\_SUBOBJECT\_TYPE\_DEPTH\_STENCIL1** and subobject data copied from *i*, a [**CD3DX12\_DEPTH\_STENCIL\_DESC1**](cd3dx12-depth-stencil-desc1.md) structure.</span></span>

</dd> <dt>

<span data-ttu-id="7c54b-113">**operator = (CD3DX12 \_ \_ набор элементов глубины \_ DESC1 const& i)**</span><span class="sxs-lookup"><span data-stu-id="7c54b-113">**operator=(CD3DX12\_DEPTH\_STENCIL\_DESC1 const& i)**</span></span>
</dt> <dd>

<span data-ttu-id="7c54b-114">Оператор присваивания копирования.</span><span class="sxs-lookup"><span data-stu-id="7c54b-114">Copy-assignment operator.</span></span>

</dd> <dt>

<span data-ttu-id="7c54b-115">**\_ \_ константа CD3DX12 шаблона глубины \_ DESC1 () const**</span><span class="sxs-lookup"><span data-stu-id="7c54b-115">**operator CD3DX12\_DEPTH\_STENCIL\_DESC1() const**</span></span>
</dt> <dd>

<span data-ttu-id="7c54b-116">Неявное преобразование в структуру [**\_ \_ \_ DESC1 шаблона глубины CD3DX12**](cd3dx12-depth-stencil-desc1.md) .</span><span class="sxs-lookup"><span data-stu-id="7c54b-116">Implicit conversion to a [**CD3DX12\_DEPTH\_STENCIL\_DESC1**](cd3dx12-depth-stencil-desc1.md) structure.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="7c54b-117">Комментарии</span><span class="sxs-lookup"><span data-stu-id="7c54b-117">Remarks</span></span>

<span data-ttu-id="7c54b-118">\_ \_ Глубина потока состояния конвейера CD3DX12 \_ \_ \_ STENCIL1 является СПЕЦИАЛИЗАЦИей typedef шаблона [**\_ \_ \_ \_ подобъекта потока состояния конвейера CD3DX12**](cd3dx12-pipeline-state-stream-subobject.md) и определяется следующим образом:</span><span class="sxs-lookup"><span data-stu-id="7c54b-118">CD3DX12\_PIPELINE\_STATE\_STREAM\_DEPTH\_STENCIL1 is a typedef specialization of the [**CD3DX12\_PIPELINE\_STATE\_STREAM\_SUBOBJECT**](cd3dx12-pipeline-state-stream-subobject.md) template, and is defined as follows:</span></span>


```C++
typedef CD3DX12_PIPELINE_STATE_STREAM_SUBOBJECT<CD3DX12_DEPTH_STENCIL_DESC1, D3D12_PIPELINE_STATE_SUBOBJECT_TYPE_DEPTH_STENCIL1, CD3DX12_DEFAULT>
    CD3DX12_PIPELINE_STATE_STREAM_DEPTH_STENCIL1;
          
```



## <a name="requirements"></a><span data-ttu-id="7c54b-119">Требования</span><span class="sxs-lookup"><span data-stu-id="7c54b-119">Requirements</span></span>



| <span data-ttu-id="7c54b-120">Требование</span><span class="sxs-lookup"><span data-stu-id="7c54b-120">Requirement</span></span> | <span data-ttu-id="7c54b-121">Значение</span><span class="sxs-lookup"><span data-stu-id="7c54b-121">Value</span></span> |
|-------------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="7c54b-122">Header</span><span class="sxs-lookup"><span data-stu-id="7c54b-122">Header</span></span><br/> | <dl> <span data-ttu-id="7c54b-123"><dt>D3dx12. h</dt></span><span class="sxs-lookup"><span data-stu-id="7c54b-123"><dt>D3dx12.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="7c54b-124">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="7c54b-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="7c54b-125">Вспомогательные структуры для D3D12</span><span class="sxs-lookup"><span data-stu-id="7c54b-125">Helper Structures for D3D12</span></span>](helper-structures-for-d3d12.md)
</dt> <dt>

[<span data-ttu-id="7c54b-126">**\_Подобъект \_ потока состояния КОНВЕЙЕРа CD3DX12 \_ \_**</span><span class="sxs-lookup"><span data-stu-id="7c54b-126">**CD3DX12\_PIPELINE\_STATE\_STREAM\_SUBOBJECT**</span></span>](cd3dx12-pipeline-state-stream-subobject.md)
</dt> <dt>

[<span data-ttu-id="7c54b-127">**\_ \_ \_ Тип подобъекта состояния конвейера D3D12 \_**</span><span class="sxs-lookup"><span data-stu-id="7c54b-127">**D3D12\_PIPELINE\_STATE\_SUBOBJECT\_TYPE**</span></span>](/windows/desktop/api/d3d12/ne-d3d12-d3d12_pipeline_state_subobject_type)
</dt> </dl>

 

