---
title: Структура CD3DX12_PIPELINE_STATE_STREAM_ROOT_SIGNATURE (D3dx12. h)
description: Вспомогательная структура, используемая для описания корневой подписи в виде одного объекта, подходящего для описания потока.
ms.assetid: 351A78DC-9BDE-43B4-9A72-D65EE15CA441
keywords:
- Структура CD3DX12_PIPELINE_STATE_STREAM_ROOT_SIGNATURE
topic_type:
- apiref
api_name:
- CD3DX12_PIPELINE_STATE_STREAM_ROOT_SIGNATURE
api_location:
- d3dx12.h
api_type:
- HeaderDef
ms.localizationpriority: low
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 61a97402fa267693de23ed2085b3d41973dc409e
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/15/2021
ms.locfileid: "105694314"
---
# <a name="cd3dx12_pipeline_state_stream_root_signature-structure"></a><span data-ttu-id="8b4a4-104">\_ \_ \_ \_ Структура подписи корневого потока состояния конвейера CD3DX12 \_</span><span class="sxs-lookup"><span data-stu-id="8b4a4-104">CD3DX12\_PIPELINE\_STATE\_STREAM\_ROOT\_SIGNATURE structure</span></span>

<span data-ttu-id="8b4a4-105">Вспомогательная структура, используемая для описания корневой подписи в виде одного объекта, подходящего для описания потока.</span><span class="sxs-lookup"><span data-stu-id="8b4a4-105">A helper structure used to describe the root signature as a single object suitable for a stream description.</span></span>

## <a name="syntax"></a><span data-ttu-id="8b4a4-106">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="8b4a4-106">Syntax</span></span>


```C++
struct CD3DX12_PIPELINE_STATE_STREAM_ROOT_SIGNATURE {
                                               CD3DX12_PIPELINE_STATE_STREAM_ROOT_SIGNATURE;
                                               CD3DX12_PIPELINE_STATE_STREAM_ROOT_SIGNATURE(ID3D12RootSignature* const &i);
  CD3DX12_PIPELINE_STATE_STREAM_ROOT_SIGNATURE operator=(ID3D12RootSignature* const& i);
                                               operator ID3D12RootSignature*() const;
};
```



## <a name="members"></a><span data-ttu-id="8b4a4-107">Члены</span><span class="sxs-lookup"><span data-stu-id="8b4a4-107">Members</span></span>

<dl> <dt>

<span data-ttu-id="8b4a4-108">**\_ \_ \_ \_ Корневая подпись потока состояния конвейера CD3DX12 \_**</span><span class="sxs-lookup"><span data-stu-id="8b4a4-108">**CD3DX12\_PIPELINE\_STATE\_STREAM\_ROOT\_SIGNATURE**</span></span>
</dt> <dd>

<span data-ttu-id="8b4a4-109">Создает новый, неинициализированный экземпляр \_ \_ \_ \_ корневой подписи потока состояния конвейера CD3DX12 \_ .</span><span class="sxs-lookup"><span data-stu-id="8b4a4-109">Creates a new, uninitialized, instance of a CD3DX12\_PIPELINE\_STATE\_STREAM\_ROOT\_SIGNATURE.</span></span>

</dd> <dt>

<span data-ttu-id="8b4a4-110">**\_ \_ Корневая подпись потока состояния конвейера CD3DX12 \_ \_ \_ (ID3D12RootSignature \* const &i)**</span><span class="sxs-lookup"><span data-stu-id="8b4a4-110">**CD3DX12\_PIPELINE\_STATE\_STREAM\_ROOT\_SIGNATURE(ID3D12RootSignature\* const &i)**</span></span>
</dt> <dd>

<span data-ttu-id="8b4a4-111">Создает новый экземпляр \_ \_ \_ корневой сигнатуры потока состояния конвейера CD3DX12 \_ \_ , инициализированный с типом подобъекта для **типа \_ \_ подобъекта состояния конвейера D3D12 \_ \_ \_ корневая \_ подпись** и данные подобъекта, скопированные из *i*, структуры [**ID3D12RootSignature**](/windows/desktop/api/d3d12/nn-d3d12-id3d12rootsignature) .</span><span class="sxs-lookup"><span data-stu-id="8b4a4-111">Creates a new instance of a CD3DX12\_PIPELINE\_STATE\_STREAM\_ROOT\_SIGNATURE, initialized with a subobject type of **D3D12\_PIPELINE\_STATE\_SUBOBJECT\_TYPE\_ROOT\_SIGNATURE** and subobject data copied from *i*, a [**ID3D12RootSignature**](/windows/desktop/api/d3d12/nn-d3d12-id3d12rootsignature) structure.</span></span>

</dd> <dt>

<span data-ttu-id="8b4a4-112">**оператор = (ID3D12RootSignature \* const& i)**</span><span class="sxs-lookup"><span data-stu-id="8b4a4-112">**operator=(ID3D12RootSignature\* const& i)**</span></span>
</dt> <dd>

<span data-ttu-id="8b4a4-113">Оператор присваивания копирования.</span><span class="sxs-lookup"><span data-stu-id="8b4a4-113">Copy-assignment operator.</span></span>

</dd> <dt>

<span data-ttu-id="8b4a4-114">**const оператора ID3D12RootSignature \* ()**</span><span class="sxs-lookup"><span data-stu-id="8b4a4-114">**operator ID3D12RootSignature\*() const**</span></span>
</dt> <dd>

<span data-ttu-id="8b4a4-115">Неявное преобразование в указатель структуры [**ID3D12RootSignature**](/windows/desktop/api/d3d12/nn-d3d12-id3d12rootsignature) .</span><span class="sxs-lookup"><span data-stu-id="8b4a4-115">Implicit conversion to a [**ID3D12RootSignature**](/windows/desktop/api/d3d12/nn-d3d12-id3d12rootsignature) structure pointer.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="8b4a4-116">Комментарии</span><span class="sxs-lookup"><span data-stu-id="8b4a4-116">Remarks</span></span>

<span data-ttu-id="8b4a4-117">\_ \_ \_ Корневая сигнатура потока состояния конвейера CD3DX12 \_ \_ является СПЕЦИАЛИЗАЦИей typedef [**шаблона \_ \_ \_ \_ подобъекта потока состояния конвейера CD3DX12**](cd3dx12-pipeline-state-stream-subobject.md) и определяется следующим образом:</span><span class="sxs-lookup"><span data-stu-id="8b4a4-117">CD3DX12\_PIPELINE\_STATE\_STREAM\_ROOT\_SIGNATURE is a typedef specialization of the [**CD3DX12\_PIPELINE\_STATE\_STREAM\_SUBOBJECT**](cd3dx12-pipeline-state-stream-subobject.md) template, and is defined as follows:</span></span>


```C++
typedef CD3DX12_PIPELINE_STATE_STREAM_SUBOBJECT<ID3D12RootSignature*, D3D12_PIPELINE_STATE_SUBOBJECT_TYPE_ROOT_SIGNATURE>
    CD3DX12_PIPELINE_STATE_STREAM_ROOT_SIGNATURE;
          
```



## <a name="requirements"></a><span data-ttu-id="8b4a4-118">Требования</span><span class="sxs-lookup"><span data-stu-id="8b4a4-118">Requirements</span></span>



| <span data-ttu-id="8b4a4-119">Требование</span><span class="sxs-lookup"><span data-stu-id="8b4a4-119">Requirement</span></span> | <span data-ttu-id="8b4a4-120">Значение</span><span class="sxs-lookup"><span data-stu-id="8b4a4-120">Value</span></span> |
|-------------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="8b4a4-121">Header</span><span class="sxs-lookup"><span data-stu-id="8b4a4-121">Header</span></span><br/> | <dl> <span data-ttu-id="8b4a4-122"><dt>D3dx12. h</dt></span><span class="sxs-lookup"><span data-stu-id="8b4a4-122"><dt>D3dx12.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="8b4a4-123">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="8b4a4-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="8b4a4-124">Вспомогательные структуры для D3D12</span><span class="sxs-lookup"><span data-stu-id="8b4a4-124">Helper Structures for D3D12</span></span>](helper-structures-for-d3d12.md)
</dt> <dt>

[<span data-ttu-id="8b4a4-125">**\_Подобъект \_ потока состояния КОНВЕЙЕРа CD3DX12 \_ \_**</span><span class="sxs-lookup"><span data-stu-id="8b4a4-125">**CD3DX12\_PIPELINE\_STATE\_STREAM\_SUBOBJECT**</span></span>](cd3dx12-pipeline-state-stream-subobject.md)
</dt> <dt>

[<span data-ttu-id="8b4a4-126">**\_ \_ \_ Тип подобъекта состояния конвейера D3D12 \_**</span><span class="sxs-lookup"><span data-stu-id="8b4a4-126">**D3D12\_PIPELINE\_STATE\_SUBOBJECT\_TYPE**</span></span>](/windows/desktop/api/d3d12/ne-d3d12-d3d12_pipeline_state_subobject_type)
</dt> </dl>

 

