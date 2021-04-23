---
title: Структура CD3DX12_PIPELINE_STATE_STREAM_DEPTH_STENCIL (D3dx12. h)
description: Вспомогательная структура, используемая для описания описания трафарета глубины в виде одного объекта, подходящего для описания потока. | Структура CD3DX12_PIPELINE_STATE_STREAM_DEPTH_STENCIL (D3dx12. h)
ms.assetid: 4FB54EA5-FCC6-4B64-A747-27DFE4C1D2DC
keywords:
- Структура CD3DX12_PIPELINE_STATE_STREAM_DEPTH_STENCIL
topic_type:
- apiref
api_name:
- CD3DX12_PIPELINE_STATE_STREAM_DEPTH_STENCIL
api_location:
- d3dx12.h
api_type:
- HeaderDef
ms.localizationpriority: low
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: cb24779aeff950bd213ce18774f55493777df9c9
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/15/2021
ms.locfileid: "105674679"
---
# <a name="cd3dx12_pipeline_state_stream_depth_stencil-structure"></a><span data-ttu-id="f6fce-105">\_ \_ \_ \_ \_ Структура набора элементов глубины потока состояния конвейера CD3DX12</span><span class="sxs-lookup"><span data-stu-id="f6fce-105">CD3DX12\_PIPELINE\_STATE\_STREAM\_DEPTH\_STENCIL structure</span></span>

<span data-ttu-id="f6fce-106">Вспомогательная структура, используемая для описания описания трафарета глубины в виде одного объекта, подходящего для описания потока.</span><span class="sxs-lookup"><span data-stu-id="f6fce-106">A helper structure used to describe a depth stencil description as a single object suitable for a stream description.</span></span>

## <a name="syntax"></a><span data-ttu-id="f6fce-107">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="f6fce-107">Syntax</span></span>


```C++
struct CD3DX12_PIPELINE_STATE_STREAM_DEPTH_STENCIL {
                                              CD3DX12_PIPELINE_STATE_STREAM_DEPTH_STENCIL;
                                              CD3DX12_PIPELINE_STATE_STREAM_DEPTH_STENCIL(CD3DX12_DEPTH_STENCIL_DESC const &i);
  CD3DX12_PIPELINE_STATE_STREAM_DEPTH_STENCIL operator=(CD3DX12_DEPTH_STENCIL_DESC const& i);
                                              operator CD3DX12_DEPTH_STENCIL_DESC() const;
};
```



## <a name="members"></a><span data-ttu-id="f6fce-108">Члены</span><span class="sxs-lookup"><span data-stu-id="f6fce-108">Members</span></span>

<dl> <dt>

<span data-ttu-id="f6fce-109">**\_ \_ \_ \_ Трафарет глубины потока состояния конвейера CD3DX12 \_**</span><span class="sxs-lookup"><span data-stu-id="f6fce-109">**CD3DX12\_PIPELINE\_STATE\_STREAM\_DEPTH\_STENCIL**</span></span>
</dt> <dd>

<span data-ttu-id="f6fce-110">Создает новый, неинициализированный экземпляр \_ \_ \_ \_ набора элементов глубины потока состояния конвейера CD3DX12 \_ .</span><span class="sxs-lookup"><span data-stu-id="f6fce-110">Creates a new, uninitialized, instance of a CD3DX12\_PIPELINE\_STATE\_STREAM\_DEPTH\_STENCIL.</span></span>

</dd> <dt>

<span data-ttu-id="f6fce-111">**\_ \_ Трафарет глубины потока состояния конвейера CD3DX12 \_ \_ \_ ( \_ набор элементов глубины CD3DX12, \_ \_ появляющееся константой DESC &i)**</span><span class="sxs-lookup"><span data-stu-id="f6fce-111">**CD3DX12\_PIPELINE\_STATE\_STREAM\_DEPTH\_STENCIL(CD3DX12\_DEPTH\_STENCIL\_DESC const &i)**</span></span>
</dt> <dd>

<span data-ttu-id="f6fce-112">Создает новый экземпляр \_ \_ \_ трафарета глубины потока состояния конвейера \_ CD3DX12 \_ , инициализированный с типом подобъекта для типа **\_ контейнера \_ \_ \_ \_ глубины \_ конвейера "состояние** подобъекта", и данные подобъекта, скопированные из *i*, структура [**\_ \_ трафарета \_ глубины CD3DX12**](cd3dx12-depth-stencil-desc.md) .</span><span class="sxs-lookup"><span data-stu-id="f6fce-112">Creates a new instance of a CD3DX12\_PIPELINE\_STATE\_STREAM\_DEPTH\_STENCIL, initialized with a subobject type of **D3D12\_PIPELINE\_STATE\_SUBOBJECT\_TYPE\_DEPTH\_STENCIL** and subobject data copied from *i*, a [**CD3DX12\_DEPTH\_STENCIL\_DESC**](cd3dx12-depth-stencil-desc.md) structure.</span></span>

</dd> <dt>

<span data-ttu-id="f6fce-113">**operator = (CD3DX12 \_ \_ набор элементов глубины, \_ const& i)**</span><span class="sxs-lookup"><span data-stu-id="f6fce-113">**operator=(CD3DX12\_DEPTH\_STENCIL\_DESC const& i)**</span></span>
</dt> <dd>

<span data-ttu-id="f6fce-114">Оператор присваивания копирования.</span><span class="sxs-lookup"><span data-stu-id="f6fce-114">Copy-assignment operator.</span></span>

</dd> <dt>

<span data-ttu-id="f6fce-115">**\_ \_ константа CD3DX12 шаблона глубины набора элементов \_ "оператор"**</span><span class="sxs-lookup"><span data-stu-id="f6fce-115">**operator CD3DX12\_DEPTH\_STENCIL\_DESC() const**</span></span>
</dt> <dd>

<span data-ttu-id="f6fce-116">Неявное преобразование в структуру [**CD3DX12 \_ \_ набора элементов \_ глубины**](cd3dx12-depth-stencil-desc.md) .</span><span class="sxs-lookup"><span data-stu-id="f6fce-116">Implicit conversion to a [**CD3DX12\_DEPTH\_STENCIL\_DESC**](cd3dx12-depth-stencil-desc.md) structure.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="f6fce-117">Комментарии</span><span class="sxs-lookup"><span data-stu-id="f6fce-117">Remarks</span></span>

<span data-ttu-id="f6fce-118">\_ \_ \_ Набор элементов глубины потока состояния конвейера CD3DX12 \_ \_ является СПЕЦИАЛИЗАЦИей typedef [**шаблона \_ \_ \_ \_ подобъекта потока состояния конвейера CD3DX12**](cd3dx12-pipeline-state-stream-subobject.md) и определяется следующим образом:</span><span class="sxs-lookup"><span data-stu-id="f6fce-118">CD3DX12\_PIPELINE\_STATE\_STREAM\_DEPTH\_STENCIL is a typedef specialization of the [**CD3DX12\_PIPELINE\_STATE\_STREAM\_SUBOBJECT**](cd3dx12-pipeline-state-stream-subobject.md) template, and is defined as follows:</span></span>


```C++
typedef CD3DX12_PIPELINE_STATE_STREAM_SUBOBJECT<CD3DX12_DEPTH_STENCIL_DESC, D3D12_PIPELINE_STATE_SUBOBJECT_TYPE_DEPTH_STENCIL, CD3DX12_DEFAULT>
    CD3DX12_PIPELINE_STATE_STREAM_DEPTH_STENCIL;
          
```



## <a name="requirements"></a><span data-ttu-id="f6fce-119">Требования</span><span class="sxs-lookup"><span data-stu-id="f6fce-119">Requirements</span></span>



| <span data-ttu-id="f6fce-120">Требование</span><span class="sxs-lookup"><span data-stu-id="f6fce-120">Requirement</span></span> | <span data-ttu-id="f6fce-121">Значение</span><span class="sxs-lookup"><span data-stu-id="f6fce-121">Value</span></span> |
|-------------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="f6fce-122">Header</span><span class="sxs-lookup"><span data-stu-id="f6fce-122">Header</span></span><br/> | <dl> <span data-ttu-id="f6fce-123"><dt>D3dx12. h</dt></span><span class="sxs-lookup"><span data-stu-id="f6fce-123"><dt>D3dx12.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="f6fce-124">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="f6fce-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f6fce-125">Вспомогательные структуры для D3D12</span><span class="sxs-lookup"><span data-stu-id="f6fce-125">Helper Structures for D3D12</span></span>](helper-structures-for-d3d12.md)
</dt> <dt>

[<span data-ttu-id="f6fce-126">**\_Подобъект \_ потока состояния КОНВЕЙЕРа CD3DX12 \_ \_**</span><span class="sxs-lookup"><span data-stu-id="f6fce-126">**CD3DX12\_PIPELINE\_STATE\_STREAM\_SUBOBJECT**</span></span>](cd3dx12-pipeline-state-stream-subobject.md)
</dt> <dt>

[<span data-ttu-id="f6fce-127">**\_ \_ \_ Тип подобъекта состояния конвейера D3D12 \_**</span><span class="sxs-lookup"><span data-stu-id="f6fce-127">**D3D12\_PIPELINE\_STATE\_SUBOBJECT\_TYPE**</span></span>](/windows/desktop/api/d3d12/ne-d3d12-d3d12_pipeline_state_subobject_type)
</dt> </dl>

 

