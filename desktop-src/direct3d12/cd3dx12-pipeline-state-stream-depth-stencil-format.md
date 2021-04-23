---
title: Структура CD3DX12_PIPELINE_STATE_STREAM_DEPTH_STENCIL_FORMAT (D3dx12. h)
description: Вспомогательная структура, используемая для описания формата трафарета глубины в виде одного объекта, подходящего для описания потока.
ms.assetid: 512DB46E-D8F0-482B-9174-C786FB91AFD2
keywords:
- Структура CD3DX12_PIPELINE_STATE_STREAM_DEPTH_STENCIL_FORMAT
topic_type:
- apiref
api_name:
- CD3DX12_PIPELINE_STATE_STREAM_DEPTH_STENCIL_FORMAT
api_location:
- d3dx12.h
api_type:
- HeaderDef
ms.localizationpriority: low
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8dc7ae2703ac80ac155c04d42624a081723288bf
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/15/2021
ms.locfileid: "105647813"
---
# <a name="cd3dx12_pipeline_state_stream_depth_stencil_format-structure"></a><span data-ttu-id="cd085-104">\_ \_ \_ \_ \_ Структура формата трафарета глубины потока состояния конвейера CD3DX12 \_</span><span class="sxs-lookup"><span data-stu-id="cd085-104">CD3DX12\_PIPELINE\_STATE\_STREAM\_DEPTH\_STENCIL\_FORMAT structure</span></span>

<span data-ttu-id="cd085-105">Вспомогательная структура, используемая для описания формата трафарета глубины в виде одного объекта, подходящего для описания потока.</span><span class="sxs-lookup"><span data-stu-id="cd085-105">A helper structure used to describe the depth stencil format as a single object suitable for a stream description.</span></span>

## <a name="syntax"></a><span data-ttu-id="cd085-106">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="cd085-106">Syntax</span></span>


```C++
struct CD3DX12_PIPELINE_STATE_STREAM_DEPTH_STENCIL_FORMAT {
                                                     CD3DX12_PIPELINE_STATE_STREAM_DEPTH_STENCIL_FORMAT;
                                                     CD3DX12_PIPELINE_STATE_STREAM_DEPTH_STENCIL_FORMAT(DXGI_FORMAT const &i);
  CD3DX12_PIPELINE_STATE_STREAM_DEPTH_STENCIL_FORMAT operator=(DXGI_FORMAT const& i);
                                                     operator DXGI_FORMAT() const;
};
```



## <a name="members"></a><span data-ttu-id="cd085-107">Члены</span><span class="sxs-lookup"><span data-stu-id="cd085-107">Members</span></span>

<dl> <dt>

<span data-ttu-id="cd085-108">**\_ \_ \_ \_ \_ Формат трафарета глубины потока состояния конвейера CD3DX12 \_**</span><span class="sxs-lookup"><span data-stu-id="cd085-108">**CD3DX12\_PIPELINE\_STATE\_STREAM\_DEPTH\_STENCIL\_FORMAT**</span></span>
</dt> <dd>

<span data-ttu-id="cd085-109">Создает новый, неинициализированный экземпляр \_ \_ \_ \_ \_ формата трафарета глубины потока состояния конвейера CD3DX12 \_ .</span><span class="sxs-lookup"><span data-stu-id="cd085-109">Creates a new, uninitialized, instance of a CD3DX12\_PIPELINE\_STATE\_STREAM\_DEPTH\_STENCIL\_FORMAT.</span></span>

</dd> <dt>

<span data-ttu-id="cd085-110">**\_ \_ \_ Формат трафарета глубины потока состояния конвейера CD3DX12 \_ \_ \_ ( \_ константа формата DXGI const &i)**</span><span class="sxs-lookup"><span data-stu-id="cd085-110">**CD3DX12\_PIPELINE\_STATE\_STREAM\_DEPTH\_STENCIL\_FORMAT(DXGI\_FORMAT const &i)**</span></span>
</dt> <dd>

<span data-ttu-id="cd085-111">Создает новый экземпляр \_ \_ \_ формата трафарета глубины потока состояния конвейера CD3DX12 \_ \_ \_ , инициализированного с типом подобъекта типа **\_ \_ подобъекта состояния конвейера D3D12 \_ \_ \_ \_ \_ Формат трафарета глубины** и данные подобъекта, скопированные из *i*, перечисление в [**\_ формате DXGI**](/windows/desktop/api/dxgiformat/ne-dxgiformat-dxgi_format) .</span><span class="sxs-lookup"><span data-stu-id="cd085-111">Creates a new instance of a CD3DX12\_PIPELINE\_STATE\_STREAM\_DEPTH\_STENCIL\_FORMAT, initialized with a subobject type of **D3D12\_PIPELINE\_STATE\_SUBOBJECT\_TYPE\_DEPTH\_STENCIL\_FORMAT** and subobject data copied from *i*, a [**DXGI\_FORMAT**](/windows/desktop/api/dxgiformat/ne-dxgiformat-dxgi_format) enumeration.</span></span>

</dd> <dt>

<span data-ttu-id="cd085-112">**operator = ( \_ константа формата DXGI& i)**</span><span class="sxs-lookup"><span data-stu-id="cd085-112">**operator=(DXGI\_FORMAT const& i)**</span></span>
</dt> <dd>

<span data-ttu-id="cd085-113">Оператор присваивания копирования.</span><span class="sxs-lookup"><span data-stu-id="cd085-113">Copy-assignment operator.</span></span>

</dd> <dt>

<span data-ttu-id="cd085-114">**Оператор \_ Format DXGI () const**</span><span class="sxs-lookup"><span data-stu-id="cd085-114">**operator DXGI\_FORMAT() const**</span></span>
</dt> <dd>

<span data-ttu-id="cd085-115">Неявное преобразование в перечисление [**\_ формата DXGI**](/windows/desktop/api/dxgiformat/ne-dxgiformat-dxgi_format) .</span><span class="sxs-lookup"><span data-stu-id="cd085-115">Implicit conversion to a [**DXGI\_FORMAT**](/windows/desktop/api/dxgiformat/ne-dxgiformat-dxgi_format) enumeration.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="cd085-116">Комментарии</span><span class="sxs-lookup"><span data-stu-id="cd085-116">Remarks</span></span>

<span data-ttu-id="cd085-117">\_ \_ \_ Формат трафарета глубины потока состояния конвейера CD3DX12 \_ \_ \_ является специализацией typedef [**шаблона \_ \_ \_ \_ подобъекта потока состояния конвейера CD3DX12**](cd3dx12-pipeline-state-stream-subobject.md) и определяется следующим образом:</span><span class="sxs-lookup"><span data-stu-id="cd085-117">CD3DX12\_PIPELINE\_STATE\_STREAM\_DEPTH\_STENCIL\_FORMAT is a typedef specialization of the [**CD3DX12\_PIPELINE\_STATE\_STREAM\_SUBOBJECT**](cd3dx12-pipeline-state-stream-subobject.md) template, and is defined as follows:</span></span>


```C++
typedef CD3DX12_PIPELINE_STATE_STREAM_SUBOBJECT<DXGI_FORMAT, D3D12_PIPELINE_STATE_SUBOBJECT_TYPE_DEPTH_STENCIL_FORMAT>
    CD3DX12_PIPELINE_STATE_STREAM_DEPTH_STENCIL_FORMAT;
          
```



## <a name="requirements"></a><span data-ttu-id="cd085-118">Требования</span><span class="sxs-lookup"><span data-stu-id="cd085-118">Requirements</span></span>



| <span data-ttu-id="cd085-119">Требование</span><span class="sxs-lookup"><span data-stu-id="cd085-119">Requirement</span></span> | <span data-ttu-id="cd085-120">Значение</span><span class="sxs-lookup"><span data-stu-id="cd085-120">Value</span></span> |
|-------------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="cd085-121">Header</span><span class="sxs-lookup"><span data-stu-id="cd085-121">Header</span></span><br/> | <dl> <span data-ttu-id="cd085-122"><dt>D3dx12. h</dt></span><span class="sxs-lookup"><span data-stu-id="cd085-122"><dt>D3dx12.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="cd085-123">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="cd085-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="cd085-124">Вспомогательные структуры для D3D12</span><span class="sxs-lookup"><span data-stu-id="cd085-124">Helper Structures for D3D12</span></span>](helper-structures-for-d3d12.md)
</dt> <dt>

[<span data-ttu-id="cd085-125">**\_Подобъект \_ потока состояния КОНВЕЙЕРа CD3DX12 \_ \_**</span><span class="sxs-lookup"><span data-stu-id="cd085-125">**CD3DX12\_PIPELINE\_STATE\_STREAM\_SUBOBJECT**</span></span>](cd3dx12-pipeline-state-stream-subobject.md)
</dt> <dt>

[<span data-ttu-id="cd085-126">**\_ \_ \_ Тип подобъекта состояния конвейера D3D12 \_**</span><span class="sxs-lookup"><span data-stu-id="cd085-126">**D3D12\_PIPELINE\_STATE\_SUBOBJECT\_TYPE**</span></span>](/windows/desktop/api/d3d12/ne-d3d12-d3d12_pipeline_state_subobject_type)
</dt> </dl>

 

