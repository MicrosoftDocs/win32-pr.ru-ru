---
title: Структура CD3DX12_ROOT_SIGNATURE_DESC (D3dx12. h)
description: Вспомогательная структура, позволяющая упростить инициализацию \_ структуры D3D12 корневой \_ подписи \_ .
ms.assetid: A3B820C1-51E8-4E35-A67F-2C4BE82A6B7F
keywords:
- Структура CD3DX12_ROOT_SIGNATURE_DESC
topic_type:
- apiref
api_name:
- CD3DX12_ROOT_SIGNATURE_DESC
api_location:
- d3dx12.h
api_type:
- HeaderDef
ms.localizationpriority: low
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7f89f9cd0f5ad9be08af1fa9c2556ebfbd4fcff1
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/15/2021
ms.locfileid: "105713967"
---
# <a name="cd3dx12_root_signature_desc-structure"></a><span data-ttu-id="19843-104">\_ \_ Структура описания корневой подписи CD3DX12 \_</span><span class="sxs-lookup"><span data-stu-id="19843-104">CD3DX12\_ROOT\_SIGNATURE\_DESC structure</span></span>

<span data-ttu-id="19843-105">Вспомогательная структура, позволяющая упростить инициализацию структуры [**D3D12 \_ корневой \_ подписи \_**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_root_signature_desc) .</span><span class="sxs-lookup"><span data-stu-id="19843-105">A helper structure to enable easy initialization of a [**D3D12\_ROOT\_SIGNATURE\_DESC**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_root_signature_desc) structure.</span></span>

## <a name="syntax"></a><span data-ttu-id="19843-106">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="19843-106">Syntax</span></span>


```C++
struct CD3DX12_ROOT_SIGNATURE_DESC  : public D3D12_ROOT_SIGNATURE_DESC{
       CD3DX12_ROOT_SIGNATURE_DESC();
       explicit CD3DX12_ROOT_SIGNATURE_DESC(const D3D12_ROOT_SIGNATURE_DESC &o);
       CD3DX12_ROOT_SIGNATURE_DESC(UINT numParameters, const D3D12_ROOT_PARAMETER* _pParameters, UINT numStaticSamplers = 0, const D3D12_STATIC_SAMPLER_DESC* _pStaticSamplers = NULL, D3D12_ROOT_SIGNATURE_FLAGS flags = D3D12_ROOT_SIGNATURE_FLAG_NONE);
       CD3DX12_ROOT_SIGNATURE_DESC(CD3DX12_DEFAULT);
  void inline Init(UINT numParameters, const D3D12_ROOT_PARAMETER* _pParameters, UINT numStaticSamplers = 0, const D3D12_STATIC_SAMPLER_DESC* _pStaticSamplers = NULL, D3D12_ROOT_SIGNATURE_FLAGS flags = D3D12_ROOT_SIGNATURE_FLAG_NONE);
  void static inline Init(D3D12_ROOT_SIGNATURE_DESC &desc, UINT numParameters, const D3D12_ROOT_PARAMETER* _pParameters, UINT numStaticSamplers = 0, const D3D12_STATIC_SAMPLER_DESC* _pStaticSamplers = NULL, D3D12_ROOT_SIGNATURE_FLAGS flags = D3D12_ROOT_SIGNATURE_FLAG_NONE);
};
```



## <a name="members"></a><span data-ttu-id="19843-107">Члены</span><span class="sxs-lookup"><span data-stu-id="19843-107">Members</span></span>

<dl> <dt>

<span data-ttu-id="19843-108">**CD3DX12 \_ корневая \_ сигнатура \_ ()**</span><span class="sxs-lookup"><span data-stu-id="19843-108">**CD3DX12\_ROOT\_SIGNATURE\_DESC()**</span></span>
</dt> <dd>

<span data-ttu-id="19843-109">Создает новый, неинициализированный экземпляр CD3DX12 \_ корневой \_ подписи \_ .</span><span class="sxs-lookup"><span data-stu-id="19843-109">Creates a new, uninitialized, instance of a CD3DX12\_ROOT\_SIGNATURE\_DESC.</span></span>

</dd> <dt>

<span data-ttu-id="19843-110">**явная CD3DX12 \_ корневая \_ подпись \_ DESC (const D3D12 \_ корневая \_ подпись \_ DESC &o)**</span><span class="sxs-lookup"><span data-stu-id="19843-110">**explicit CD3DX12\_ROOT\_SIGNATURE\_DESC(const D3D12\_ROOT\_SIGNATURE\_DESC &o)**</span></span>
</dt> <dd>

<span data-ttu-id="19843-111">Создает новый экземпляр CD3DX12 \_ корневой \_ подписи \_ (desc), инициализируемый с помощью содержимого другой [**\_ корневой структуры \_ сигнатуры \_ D3D12**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_root_signature_desc) .</span><span class="sxs-lookup"><span data-stu-id="19843-111">Creates a new instance of a CD3DX12\_ROOT\_SIGNATURE\_DESC, initialized with the contents of another [**D3D12\_ROOT\_SIGNATURE\_DESC**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_root_signature_desc) structure.</span></span>

</dd> <dt>

<span data-ttu-id="19843-112">**CD3DX12 \_ корневая \_ сигнатура \_ (uint НУМПАРАМЕТЕРС, const D3D12 \_ корневой \_ параметр \* \_ ппараметерс, uint нумстатиксамплерс = 0, const D3D12 статическая ВЫБОРка \_ \_ \_ DESC \* \_ пстатиксамплерс = null, D3D12 флаги флагов \_ корневой сигнатуры \_ \_ = D3D12 \_ корневая \_ подпись, \_ флаг \_ None)**</span><span class="sxs-lookup"><span data-stu-id="19843-112">**CD3DX12\_ROOT\_SIGNATURE\_DESC(UINT numParameters, const D3D12\_ROOT\_PARAMETER\* \_pParameters, UINT numStaticSamplers = 0, const D3D12\_STATIC\_SAMPLER\_DESC\* \_pStaticSamplers = NULL, D3D12\_ROOT\_SIGNATURE\_FLAGS flags = D3D12\_ROOT\_SIGNATURE\_FLAG\_NONE)**</span></span>
</dt> <dd>

<span data-ttu-id="19843-113">Создает новый экземпляр CD3DX12 \_ корневой \_ подписи \_ , инициализируя следующие параметры:</span><span class="sxs-lookup"><span data-stu-id="19843-113">Creates a new instance of a CD3DX12\_ROOT\_SIGNATURE\_DESC, initializing the following parameters:</span></span>

<span data-ttu-id="19843-114">UINT Нумпараметерс</span><span class="sxs-lookup"><span data-stu-id="19843-114">UINT numParameters</span></span>

<span data-ttu-id="19843-115">[**D3D12 \_ Корневой \_ параметр**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_root_parameter) \* \_ ппараметерс</span><span class="sxs-lookup"><span data-stu-id="19843-115">[**D3D12\_ROOT\_PARAMETER**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_root_parameter)\* \_pParameters</span></span>

<span data-ttu-id="19843-116">участие UINT Нумстатиксамплерс = 0</span><span class="sxs-lookup"><span data-stu-id="19843-116">(opt) UINT numStaticSamplers = 0</span></span>

<span data-ttu-id="19843-117">участие [**D3D12 \_ Статическая \_ проба \_ DESC**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_static_sampler_desc) \* \_ пстатиксамплерс = null</span><span class="sxs-lookup"><span data-stu-id="19843-117">(opt) [**D3D12\_STATIC\_SAMPLER\_DESC**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_static_sampler_desc)\* \_pStaticSamplers = NULL</span></span>

<span data-ttu-id="19843-118">участие [**D3D12 \_ Флаги \_ \_ ФЛАГов корневой подписи**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_root_signature_flags) = D3D12 \_ корневой \_ подписи \_ \_ нет</span><span class="sxs-lookup"><span data-stu-id="19843-118">(opt) [**D3D12\_ROOT\_SIGNATURE\_FLAGS**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_root_signature_flags) flags = D3D12\_ROOT\_SIGNATURE\_FLAG\_NONE</span></span>

</dd> <dt>

<span data-ttu-id="19843-119">**CD3DX12 \_ корневая \_ сигнатура \_ (CD3DX12 \_ по умолчанию)**</span><span class="sxs-lookup"><span data-stu-id="19843-119">**CD3DX12\_ROOT\_SIGNATURE\_DESC(CD3DX12\_DEFAULT)**</span></span>
</dt> <dd>

<span data-ttu-id="19843-120">Создает новый экземпляр CD3DX12 \_ корневой \_ подписи \_ , инициализированный параметрами по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="19843-120">Creates a new instance of a CD3DX12\_ROOT\_SIGNATURE\_DESC, initialized with default parameters.</span></span>

``` syntax
CD3DX12_ROOT_SIGNATURE_DESC(0,NULL,0,NULL,D3D12_ROOT_SIGNATURE_FLAG_NONE)
```

</dd> <dt>

<span data-ttu-id="19843-121">**Inline init (UINT Нумпараметерс, const D3D12 \_ root, \_ параметр \* \_ ппараметерс, uint нумстатиксамплерс = 0, const D3D12 \_ статическая выборка \_ \_ DESC \* \_ пстатиксамплерс = null, флаги флагов \_ корневой \_ подписи \_ = D3D12 \_ корневой \_ подписи \_ \_ None)**</span><span class="sxs-lookup"><span data-stu-id="19843-121">**inline Init(UINT numParameters, const D3D12\_ROOT\_PARAMETER\* \_pParameters, UINT numStaticSamplers = 0, const D3D12\_STATIC\_SAMPLER\_DESC\* \_pStaticSamplers = NULL, D3D12\_ROOT\_SIGNATURE\_FLAGS flags = D3D12\_ROOT\_SIGNATURE\_FLAG\_NONE)**</span></span>
</dt> <dd>

<span data-ttu-id="19843-122">Задает функцию, которая инициализирует следующие параметры:</span><span class="sxs-lookup"><span data-stu-id="19843-122">Specifies a function that initializes the following parameters:</span></span>

<span data-ttu-id="19843-123">UINT Нумпараметерс</span><span class="sxs-lookup"><span data-stu-id="19843-123">UINT numParameters</span></span>

<span data-ttu-id="19843-124">[**D3D12 \_ Корневой \_ параметр**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_root_parameter) \* \_ ппараметерс</span><span class="sxs-lookup"><span data-stu-id="19843-124">[**D3D12\_ROOT\_PARAMETER**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_root_parameter)\* \_pParameters</span></span>

<span data-ttu-id="19843-125">участие UINT Нумстатиксамплерс = 0</span><span class="sxs-lookup"><span data-stu-id="19843-125">(opt) UINT numStaticSamplers = 0</span></span>

<span data-ttu-id="19843-126">участие [**D3D12 \_ Статическая \_ проба \_ DESC**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_static_sampler_desc) \* \_ пстатиксамплерс = null</span><span class="sxs-lookup"><span data-stu-id="19843-126">(opt) [**D3D12\_STATIC\_SAMPLER\_DESC**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_static_sampler_desc)\* \_pStaticSamplers = NULL</span></span>

<span data-ttu-id="19843-127">участие [**D3D12 \_ Флаги \_ \_ ФЛАГов корневой подписи**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_root_signature_flags) = D3D12 \_ корневой \_ подписи \_ \_ нет</span><span class="sxs-lookup"><span data-stu-id="19843-127">(opt) [**D3D12\_ROOT\_SIGNATURE\_FLAGS**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_root_signature_flags) flags = D3D12\_ROOT\_SIGNATURE\_FLAG\_NONE</span></span>

</dd> <dt>

<span data-ttu-id="19843-128">**Статическая встроенная init (D3D12 \_ корневая \_ подпись \_ DESC &DESC, uint НУМПАРАМЕТЕРС, const D3D12 \_ корневой \_ параметр \* \_ ппараметерс, uint нумстатиксамплерс = 0, const D3D12 статическая ВЫБОРка \_ \_ \_ DESC \* \_ пстатиксамплерс = null, D3D12 флаги флагов \_ \_ \_ \_ корневой подписи = D3D12 корневая \_ подпись \_ \_ None)**</span><span class="sxs-lookup"><span data-stu-id="19843-128">**static inline Init(D3D12\_ROOT\_SIGNATURE\_DESC &desc, UINT numParameters, const D3D12\_ROOT\_PARAMETER\* \_pParameters, UINT numStaticSamplers = 0, const D3D12\_STATIC\_SAMPLER\_DESC\* \_pStaticSamplers = NULL, D3D12\_ROOT\_SIGNATURE\_FLAGS flags = D3D12\_ROOT\_SIGNATURE\_FLAG\_NONE)**</span></span>
</dt> <dd>

<span data-ttu-id="19843-129">Задает функцию, которая инициализирует следующие параметры:</span><span class="sxs-lookup"><span data-stu-id="19843-129">Specifies a function that initializes the following parameters:</span></span>

<span data-ttu-id="19843-130">[**D3D12 \_ Корневая \_ сигнатура \_ DESC**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_root_signature_desc) &DESC</span><span class="sxs-lookup"><span data-stu-id="19843-130">[**D3D12\_ROOT\_SIGNATURE\_DESC**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_root_signature_desc) &desc</span></span>

<span data-ttu-id="19843-131">UINT Нумпараметерс</span><span class="sxs-lookup"><span data-stu-id="19843-131">UINT numParameters</span></span>

<span data-ttu-id="19843-132">[**D3D12 \_ Корневой \_ параметр**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_root_parameter) \* \_ ппараметерс</span><span class="sxs-lookup"><span data-stu-id="19843-132">[**D3D12\_ROOT\_PARAMETER**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_root_parameter)\* \_pParameters</span></span>

<span data-ttu-id="19843-133">участие UINT Нумстатиксамплерс = 0</span><span class="sxs-lookup"><span data-stu-id="19843-133">(opt) UINT numStaticSamplers = 0</span></span>

<span data-ttu-id="19843-134">участие [**D3D12 \_ Статическая \_ проба \_ DESC**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_static_sampler_desc) \* \_ пстатиксамплерс = null</span><span class="sxs-lookup"><span data-stu-id="19843-134">(opt) [**D3D12\_STATIC\_SAMPLER\_DESC**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_static_sampler_desc)\* \_pStaticSamplers = NULL</span></span>

<span data-ttu-id="19843-135">участие [**D3D12 \_ Флаги \_ \_ ФЛАГов корневой подписи**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_root_signature_flags) = D3D12 \_ корневой \_ подписи \_ \_ нет</span><span class="sxs-lookup"><span data-stu-id="19843-135">(opt) [**D3D12\_ROOT\_SIGNATURE\_FLAGS**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_root_signature_flags) flags = D3D12\_ROOT\_SIGNATURE\_FLAG\_NONE</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="19843-136">Требования</span><span class="sxs-lookup"><span data-stu-id="19843-136">Requirements</span></span>



| <span data-ttu-id="19843-137">Требование</span><span class="sxs-lookup"><span data-stu-id="19843-137">Requirement</span></span> | <span data-ttu-id="19843-138">Значение</span><span class="sxs-lookup"><span data-stu-id="19843-138">Value</span></span> |
|-------------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="19843-139">Header</span><span class="sxs-lookup"><span data-stu-id="19843-139">Header</span></span><br/> | <dl> <span data-ttu-id="19843-140"><dt>D3dx12. h</dt></span><span class="sxs-lookup"><span data-stu-id="19843-140"><dt>D3dx12.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="19843-141">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="19843-141">See also</span></span>

<dl> <dt>

[<span data-ttu-id="19843-142">**\_DESC корневой \_ подписи D3D12 \_**</span><span class="sxs-lookup"><span data-stu-id="19843-142">**D3D12\_ROOT\_SIGNATURE\_DESC**</span></span>](/windows/desktop/api/d3d12/ns-d3d12-d3d12_root_signature_desc)
</dt> <dt>

[<span data-ttu-id="19843-143">Вспомогательные структуры для D3D12</span><span class="sxs-lookup"><span data-stu-id="19843-143">Helper Structures for D3D12</span></span>](helper-structures-for-d3d12.md)
</dt> </dl>

 

 





