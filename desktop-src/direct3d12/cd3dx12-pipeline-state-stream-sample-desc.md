---
title: Структура CD3DX12_PIPELINE_STATE_STREAM_SAMPLE_DESC (D3dx12. h)
description: Вспомогательная структура, используемая для описания образца описания как одного объекта, подходящего для описания потока.
ms.assetid: D84C5373-AC0F-430A-97A1-6125611869B2
keywords:
- Структура CD3DX12_PIPELINE_STATE_STREAM_SAMPLE_DESC
topic_type:
- apiref
api_name:
- CD3DX12_PIPELINE_STATE_STREAM_SAMPLE_DESC
api_location:
- d3dx12.h
api_type:
- HeaderDef
ms.localizationpriority: low
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5fea786dc0429da28f9c26f0203b06059aff1c17
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/15/2021
ms.locfileid: "105694313"
---
# <a name="cd3dx12_pipeline_state_stream_sample_desc-structure"></a><span data-ttu-id="3990b-104">\_ \_ \_ \_ Структура примера потока состояния конвейера CD3DX12 \_</span><span class="sxs-lookup"><span data-stu-id="3990b-104">CD3DX12\_PIPELINE\_STATE\_STREAM\_SAMPLE\_DESC structure</span></span>

<span data-ttu-id="3990b-105">Вспомогательная структура, используемая для описания образца описания как одного объекта, подходящего для описания потока.</span><span class="sxs-lookup"><span data-stu-id="3990b-105">A helper structure used to describe a sample description as a single object suitable for a stream description.</span></span>

## <a name="syntax"></a><span data-ttu-id="3990b-106">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="3990b-106">Syntax</span></span>


```C++
struct CD3DX12_PIPELINE_STATE_STREAM_SAMPLE_DESC {
                                            CD3DX12_PIPELINE_STATE_STREAM_SAMPLE_DESC;
                                            CD3DX12_PIPELINE_STATE_STREAM_SAMPLE_DESC(DXGI_SAMPLE_DESC const &i);
  CD3DX12_PIPELINE_STATE_STREAM_SAMPLE_DESC operator=(DXGI_SAMPLE_DESC const& i);
                                            operator DXGI_SAMPLE_DESC() const;
};
```



## <a name="members"></a><span data-ttu-id="3990b-107">Члены</span><span class="sxs-lookup"><span data-stu-id="3990b-107">Members</span></span>

<dl> <dt>

<span data-ttu-id="3990b-108">**\_ \_ \_ \_ Пример DESC потока состояния конвейера CD3DX12 \_**</span><span class="sxs-lookup"><span data-stu-id="3990b-108">**CD3DX12\_PIPELINE\_STATE\_STREAM\_SAMPLE\_DESC**</span></span>
</dt> <dd>

<span data-ttu-id="3990b-109">Создает новый, неинициализированный экземпляр \_ \_ примера потока состояния конвейера CD3DX12 \_ \_ \_ .</span><span class="sxs-lookup"><span data-stu-id="3990b-109">Creates a new, uninitialized, instance of a CD3DX12\_PIPELINE\_STATE\_STREAM\_SAMPLE\_DESC.</span></span>

</dd> <dt>

<span data-ttu-id="3990b-110">**\_ \_ Пример DESC потока состояния конвейера CD3DX12 \_ \_ \_ ( \_ пример тестовой среды DXGI \_ const &i)**</span><span class="sxs-lookup"><span data-stu-id="3990b-110">**CD3DX12\_PIPELINE\_STATE\_STREAM\_SAMPLE\_DESC(DXGI\_SAMPLE\_DESC const &i)**</span></span>
</dt> <dd>

<span data-ttu-id="3990b-111">Создает новый экземпляр \_ \_ примера потока состояния конвейера CD3DX12 \_ \_ \_ , инициализированного с типом ПОДобъекта типа **\_ \_ подобъекта состояния конвейера D3D12 \_ \_ \_ образец \_ DESC** и данные подобъекта, скопированные из *i*, [**\_ пример \_ DESC**](https://www.bing.com/search?q=**DXGI\_SAMPLE\_DESC**) структуры для DXGI.</span><span class="sxs-lookup"><span data-stu-id="3990b-111">Creates a new instance of a CD3DX12\_PIPELINE\_STATE\_STREAM\_SAMPLE\_DESC, initialized with a subobject type of **D3D12\_PIPELINE\_STATE\_SUBOBJECT\_TYPE\_SAMPLE\_DESC** and subobject data copied from *i*, a [**DXGI\_SAMPLE\_DESC**](https://www.bing.com/search?q=**DXGI\_SAMPLE\_DESC**) structure.</span></span>

</dd> <dt>

<span data-ttu-id="3990b-112">**operator = (пример примера в DXGI " \_ \_ const"& i)**</span><span class="sxs-lookup"><span data-stu-id="3990b-112">**operator=(DXGI\_SAMPLE\_DESC const& i)**</span></span>
</dt> <dd>

<span data-ttu-id="3990b-113">Оператор присваивания копирования.</span><span class="sxs-lookup"><span data-stu-id="3990b-113">Copy-assignment operator.</span></span>

</dd> <dt>

<span data-ttu-id="3990b-114">**оператор " \_ пример \_ DESC" для оператора DXGI () const**</span><span class="sxs-lookup"><span data-stu-id="3990b-114">**operator DXGI\_SAMPLE\_DESC() const**</span></span>
</dt> <dd>

<span data-ttu-id="3990b-115">Неявное преобразование в структуру [**\_ \_ DESC образца**](https://www.bing.com/search?q=**DXGI\_SAMPLE\_DESC**) в виде DXGI.</span><span class="sxs-lookup"><span data-stu-id="3990b-115">Implicit conversion to a [**DXGI\_SAMPLE\_DESC**](https://www.bing.com/search?q=**DXGI\_SAMPLE\_DESC**) structure.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="3990b-116">Комментарии</span><span class="sxs-lookup"><span data-stu-id="3990b-116">Remarks</span></span>

<span data-ttu-id="3990b-117">\_ \_ Пример DESC потока состояния конвейера CD3DX12 \_ \_ \_ является СПЕЦИАЛИЗАЦИей typedef шаблона [**\_ \_ \_ \_ подобъекта потока состояния конвейера CD3DX12**](cd3dx12-pipeline-state-stream-subobject.md) и определяется следующим образом:</span><span class="sxs-lookup"><span data-stu-id="3990b-117">CD3DX12\_PIPELINE\_STATE\_STREAM\_SAMPLE\_DESC is a typedef specialization of the [**CD3DX12\_PIPELINE\_STATE\_STREAM\_SUBOBJECT**](cd3dx12-pipeline-state-stream-subobject.md) template, and is defined as follows:</span></span>


```C++
typedef CD3DX12_PIPELINE_STATE_STREAM_SUBOBJECT<DXGI_SAMPLE_DESC, D3D12_PIPELINE_STATE_SUBOBJECT_TYPE_SAMPLE_DESC>
    CD3DX12_PIPELINE_STATE_STREAM_SAMPLE_DESC;
          
```



## <a name="requirements"></a><span data-ttu-id="3990b-118">Требования</span><span class="sxs-lookup"><span data-stu-id="3990b-118">Requirements</span></span>



| <span data-ttu-id="3990b-119">Требование</span><span class="sxs-lookup"><span data-stu-id="3990b-119">Requirement</span></span> | <span data-ttu-id="3990b-120">Значение</span><span class="sxs-lookup"><span data-stu-id="3990b-120">Value</span></span> |
|-------------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="3990b-121">Header</span><span class="sxs-lookup"><span data-stu-id="3990b-121">Header</span></span><br/> | <dl> <span data-ttu-id="3990b-122"><dt>D3dx12. h</dt></span><span class="sxs-lookup"><span data-stu-id="3990b-122"><dt>D3dx12.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="3990b-123">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="3990b-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="3990b-124">Вспомогательные структуры для D3D12</span><span class="sxs-lookup"><span data-stu-id="3990b-124">Helper Structures for D3D12</span></span>](helper-structures-for-d3d12.md)
</dt> <dt>

[<span data-ttu-id="3990b-125">**\_Подобъект \_ потока состояния КОНВЕЙЕРа CD3DX12 \_ \_**</span><span class="sxs-lookup"><span data-stu-id="3990b-125">**CD3DX12\_PIPELINE\_STATE\_STREAM\_SUBOBJECT**</span></span>](cd3dx12-pipeline-state-stream-subobject.md)
</dt> <dt>

[<span data-ttu-id="3990b-126">**\_ \_ \_ Тип подобъекта состояния конвейера D3D12 \_**</span><span class="sxs-lookup"><span data-stu-id="3990b-126">**D3D12\_PIPELINE\_STATE\_SUBOBJECT\_TYPE**</span></span>](/windows/desktop/api/d3d12/ne-d3d12-d3d12_pipeline_state_subobject_type)
</dt> </dl>

 

