---
title: Структура CD3DX12_VERSIONED_ROOT_SIGNATURE_DESC (D3dx12. h)
description: Вспомогательная структура, позволяющая упростить инициализацию структуры D3D12 с \_ версией \_ корневой \_ подписи \_ .
ms.assetid: 4505C1CE-CAA5-4092-B990-75740A2B194C
keywords:
- Структура CD3DX12_VERSIONED_ROOT_SIGNATURE_DESC
topic_type:
- apiref
api_name:
- CD3DX12_VERSIONED_ROOT_SIGNATURE_DESC
api_location:
- d3dx12.h
api_type:
- HeaderDef
ms.localizationpriority: low
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 695b60fef5aba124ce4e6f2ff729fdb9362c7b2c
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/15/2021
ms.locfileid: "105713496"
---
# <a name="cd3dx12_versioned_root_signature_desc-structure"></a><span data-ttu-id="5abda-104">\_ \_ Структура CD3DX12 корневой \_ сигнатуры с управлением версиями \_</span><span class="sxs-lookup"><span data-stu-id="5abda-104">CD3DX12\_VERSIONED\_ROOT\_SIGNATURE\_DESC structure</span></span>

<span data-ttu-id="5abda-105">Вспомогательная структура, позволяющая упростить инициализацию структуры [**D3D12 с \_ версией \_ корневой \_ подписи \_**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_versioned_root_signature_desc) .</span><span class="sxs-lookup"><span data-stu-id="5abda-105">A helper structure to enable easy initialization of a [**D3D12\_VERSIONED\_ROOT\_SIGNATURE\_DESC**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_versioned_root_signature_desc) structure.</span></span>

## <a name="syntax"></a><span data-ttu-id="5abda-106">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="5abda-106">Syntax</span></span>


```C++
struct CD3DX12_VERSIONED_ROOT_SIGNATURE_DESC  : public D3D12_VERSIONED_ROOT_SIGNATURE_DESC{
       CD3DX12_VERSIONED_ROOT_SIGNATURE_DESC();
       explicit CD3DX12_VERSIONED_ROOT_SIGNATURE_DESC(const D3D12_VERSIONED_ROOT_SIGNATURE_DESC &o);
       explicit CD3DX12_VERSIONED_ROOT_SIGNATURE_DESC(const D3D12_ROOT_SIGNATURE_DESC &o);
       explicit CD3DX12_VERSIONED_ROOT_SIGNATURE_DESC(const D3D12_ROOT_SIGNATURE_DESC1 &o);
       CD3DX12_VERSIONED_ROOT_SIGNATURE_DESC(UINT numParameters, const D3D12_ROOT_PARAMETER* _pParameters, UINT numStaticSamplers = 0, const D3D12_STATIC_SAMPLER_DESC* _pStaticSamplers = NULL, D3D12_ROOT_SIGNATURE_FLAGS flags = D3D12_ROOT_SIGNATURE_FLAG_NONE);
       CD3DX12_VERSIONED_ROOT_SIGNATURE_DESC(UINT numParameters, const D3D12_ROOT_PARAMETER1* _pParameters, UINT numStaticSamplers = 0, const D3D12_STATIC_SAMPLER_DESC* _pStaticSamplers = NULL, D3D12_ROOT_SIGNATURE_FLAGS flags = D3D12_ROOT_SIGNATURE_FLAG_NONE);
       CD3DX12_VERSIONED_ROOT_SIGNATURE_DESC(CD3DX12_DEFAULT);
  void inline Init_1_0(UINT numParameters, const D3D12_ROOT_PARAMETER* _pParameters, UINT numStaticSamplers = 0, const D3D12_STATIC_SAMPLER_DESC* _pStaticSamplers = NULL, D3D12_ROOT_SIGNATURE_FLAGS flags = D3D12_ROOT_SIGNATURE_FLAG_NONE);
  void static inline Init_1_0(D3D12_VERSIONED_ROOT_SIGNATURE_DESC &desc, UINT numParameters, const D3D12_ROOT_PARAMETER* _pParameters, UINT numStaticSamplers = 0, const D3D12_STATIC_SAMPLER_DESC* _pStaticSamplers = NULL, D3D12_ROOT_SIGNATURE_FLAGS flags = D3D12_ROOT_SIGNATURE_FLAG_NONE);
  void inline Init_1_1(UINT numParameters, const D3D12_ROOT_PARAMETER1* _pParameters, UINT numStaticSamplers = 0, const D3D12_STATIC_SAMPLER_DESC* _pStaticSamplers = NULL, D3D12_ROOT_SIGNATURE_FLAGS flags = D3D12_ROOT_SIGNATURE_FLAG_NONE);
  void static inline Init_1_1(D3D12_VERSIONED_ROOT_SIGNATURE_DESC &desc, UINT numParameters, const D3D12_ROOT_PARAMETER1* _pParameters, UINT numStaticSamplers = 0, const D3D12_STATIC_SAMPLER_DESC* _pStaticSamplers = NULL, D3D12_ROOT_SIGNATURE_FLAGS flags = D3D12_ROOT_SIGNATURE_FLAG_NONE);
};
```



## <a name="members"></a><span data-ttu-id="5abda-107">Члены</span><span class="sxs-lookup"><span data-stu-id="5abda-107">Members</span></span>

<dl> <dt>

<span data-ttu-id="5abda-108">**CD3DX12 \_ \_ корневая \_ сигнатура с версиями \_ ()**</span><span class="sxs-lookup"><span data-stu-id="5abda-108">**CD3DX12\_VERSIONED\_ROOT\_SIGNATURE\_DESC()**</span></span>
</dt> <dd>

<span data-ttu-id="5abda-109">Создает новый, неинициализированный экземпляр CD3DX12 \_ \_ корневой подписи с версией \_ \_ .</span><span class="sxs-lookup"><span data-stu-id="5abda-109">Creates a new, uninitialized, instance of a CD3DX12\_VERSIONED\_ROOT\_SIGNATURE\_DESC.</span></span>

</dd> <dt>

<span data-ttu-id="5abda-110">**явная CD3DX12 \_ версия \_ корневой \_ подписи \_ DESC (const D3D12 \_ \_ корневая \_ подпись \_ DESC &o)**</span><span class="sxs-lookup"><span data-stu-id="5abda-110">**explicit CD3DX12\_VERSIONED\_ROOT\_SIGNATURE\_DESC(const D3D12\_VERSIONED\_ROOT\_SIGNATURE\_DESC &o)**</span></span>
</dt> <dd>

<span data-ttu-id="5abda-111">Создает новый экземпляр CD3DX12 \_ \_ корневой \_ подписи \_ с версией, инициализированной с содержимым структуры [**\_ \_ корневой \_ подписи \_ с версией D3D12**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_versioned_root_signature_desc) .</span><span class="sxs-lookup"><span data-stu-id="5abda-111">Creates a new instance of a CD3DX12\_VERSIONED\_ROOT\_SIGNATURE\_DESC, initialized with the contents of a [**D3D12\_VERSIONED\_ROOT\_SIGNATURE\_DESC**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_versioned_root_signature_desc) structure.</span></span>

</dd> <dt>

<span data-ttu-id="5abda-112">**Explicit CD3DX12 \_ \_ корневая \_ подпись \_ DESC (const D3D12 \_ корневая \_ подпись \_ DESC &o)**</span><span class="sxs-lookup"><span data-stu-id="5abda-112">**explicit CD3DX12\_VERSIONED\_ROOT\_SIGNATURE\_DESC(const D3D12\_ROOT\_SIGNATURE\_DESC &o)**</span></span>
</dt> <dd>

<span data-ttu-id="5abda-113">Создает новый экземпляр CD3DX12 \_ \_ корневой \_ подписи \_ с версией, инициализированной с содержимым структуры [**D3D12 \_ корневой \_ сигнатуры \_**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_root_signature_desc) .</span><span class="sxs-lookup"><span data-stu-id="5abda-113">Creates a new instance of a CD3DX12\_VERSIONED\_ROOT\_SIGNATURE\_DESC, initialized with the contents of a [**D3D12\_ROOT\_SIGNATURE\_DESC**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_root_signature_desc) structure.</span></span>

</dd> <dt>

<span data-ttu-id="5abda-114">**явная CD3DX12 \_ \_ корневая \_ подпись \_ DESC (const D3D12 \_ root \_ Signature \_ DESC1 &o)**</span><span class="sxs-lookup"><span data-stu-id="5abda-114">**explicit CD3DX12\_VERSIONED\_ROOT\_SIGNATURE\_DESC(const D3D12\_ROOT\_SIGNATURE\_DESC1 &o)**</span></span>
</dt> <dd>

<span data-ttu-id="5abda-115">Создает новый экземпляр CD3DX12 \_ \_ корневой \_ подписи \_ с версией, инициализированной с содержимым [**D3D12 \_ корневой структуры \_ сигнатуры \_ DESC1**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_root_signature_desc1) .</span><span class="sxs-lookup"><span data-stu-id="5abda-115">Creates a new instance of a CD3DX12\_VERSIONED\_ROOT\_SIGNATURE\_DESC, initialized with the contents of a [**D3D12\_ROOT\_SIGNATURE\_DESC1**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_root_signature_desc1) structure.</span></span>

</dd> <dt>

<span data-ttu-id="5abda-116">**CD3DX12 \_ версия \_ корневой \_ сигнатуры \_ DESC (uint нумпараметерс, const D3D12 \_ корневой \_ параметр \* \_ ППАРАМЕТЕРС, uint нумстатиксамплерс = 0, const D3D12 СТАТИЧЕСКАЯ выборка \_ \_ \_ DESC \* \_ пстатиксамплерс = null, D3D12 флаги флагов корневой сигнатуры \_ \_ \_ = D3D12 \_ корневая \_ подпись, \_ флаг \_ None)**</span><span class="sxs-lookup"><span data-stu-id="5abda-116">**CD3DX12\_VERSIONED\_ROOT\_SIGNATURE\_DESC(UINT numParameters, const D3D12\_ROOT\_PARAMETER\* \_pParameters, UINT numStaticSamplers = 0, const D3D12\_STATIC\_SAMPLER\_DESC\* \_pStaticSamplers = NULL, D3D12\_ROOT\_SIGNATURE\_FLAGS flags = D3D12\_ROOT\_SIGNATURE\_FLAG\_NONE)**</span></span>
</dt> <dd>

<span data-ttu-id="5abda-117">Создает новый экземпляр CD3DX12 \_ \_ корневой подписи с версией \_ \_ , инициализируя следующие параметры:</span><span class="sxs-lookup"><span data-stu-id="5abda-117">Creates a new instance of a CD3DX12\_VERSIONED\_ROOT\_SIGNATURE\_DESC, initializing the following parameters:</span></span>

<span data-ttu-id="5abda-118">UINT Нумпараметерс</span><span class="sxs-lookup"><span data-stu-id="5abda-118">UINT numParameters</span></span>

<span data-ttu-id="5abda-119">const [**D3D12 \_ \_ параметр root**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_root_parameter) \* \_ ппараметерс</span><span class="sxs-lookup"><span data-stu-id="5abda-119">const [**D3D12\_ROOT\_PARAMETER**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_root_parameter)\* \_pParameters</span></span>

<span data-ttu-id="5abda-120">UINT Нумстатиксамплерс = 0</span><span class="sxs-lookup"><span data-stu-id="5abda-120">UINT numStaticSamplers = 0</span></span>

<span data-ttu-id="5abda-121">const [**D3D12 \_ static \_ образец \_ DESC**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_static_sampler_desc) \* \_ пстатиксамплерс = null</span><span class="sxs-lookup"><span data-stu-id="5abda-121">const [**D3D12\_STATIC\_SAMPLER\_DESC**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_static_sampler_desc)\* \_pStaticSamplers = NULL</span></span>

<span data-ttu-id="5abda-122">[**D3D12 \_ Флаги \_ \_ ФЛАГов корневой подписи**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_root_signature_flags) = D3D12 \_ корневой \_ подписи \_ \_ нет</span><span class="sxs-lookup"><span data-stu-id="5abda-122">[**D3D12\_ROOT\_SIGNATURE\_FLAGS**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_root_signature_flags) flags = D3D12\_ROOT\_SIGNATURE\_FLAG\_NONE</span></span>

</dd> <dt>

<span data-ttu-id="5abda-123">**CD3DX12 \_ с версией \_ корневой \_ сигнатуры \_ DESC (uint нумпараметерс, const D3D12 \_ root \_ параметр1 \* \_ ППАРАМЕТЕРС, uint нумстатиксамплерс = 0, const D3D12 \_ static \_ образец DESC пстатиксамплерс = null, D3D12 флаги флагов корневой сигнатуры \_ \* \_ \_ \_ \_ = D3D12 \_ корневая \_ подпись, \_ флаг \_ None)**</span><span class="sxs-lookup"><span data-stu-id="5abda-123">**CD3DX12\_VERSIONED\_ROOT\_SIGNATURE\_DESC(UINT numParameters, const D3D12\_ROOT\_PARAMETER1\* \_pParameters, UINT numStaticSamplers = 0, const D3D12\_STATIC\_SAMPLER\_DESC\* \_pStaticSamplers = NULL, D3D12\_ROOT\_SIGNATURE\_FLAGS flags = D3D12\_ROOT\_SIGNATURE\_FLAG\_NONE)**</span></span>
</dt> <dd>

<span data-ttu-id="5abda-124">Создает новый экземпляр CD3DX12 \_ \_ корневой подписи с версией \_ \_ , инициализируя следующие параметры:</span><span class="sxs-lookup"><span data-stu-id="5abda-124">Creates a new instance of a CD3DX12\_VERSIONED\_ROOT\_SIGNATURE\_DESC, initializing the following parameters:</span></span>

<span data-ttu-id="5abda-125">UINT Нумпараметерс</span><span class="sxs-lookup"><span data-stu-id="5abda-125">UINT numParameters</span></span>

<span data-ttu-id="5abda-126">const [**D3D12 \_ root \_ параметр1**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_root_parameter1) \* \_ ппараметерс</span><span class="sxs-lookup"><span data-stu-id="5abda-126">const [**D3D12\_ROOT\_PARAMETER1**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_root_parameter1)\* \_pParameters</span></span>

<span data-ttu-id="5abda-127">UINT Нумстатиксамплерс = 0</span><span class="sxs-lookup"><span data-stu-id="5abda-127">UINT numStaticSamplers = 0</span></span>

<span data-ttu-id="5abda-128">const [**D3D12 \_ static \_ образец \_ DESC**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_static_sampler_desc) \* \_ пстатиксамплерс = null</span><span class="sxs-lookup"><span data-stu-id="5abda-128">const [**D3D12\_STATIC\_SAMPLER\_DESC**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_static_sampler_desc)\* \_pStaticSamplers = NULL</span></span>

<span data-ttu-id="5abda-129">[**D3D12 \_ Флаги \_ \_ ФЛАГов корневой подписи**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_root_signature_flags) = D3D12 \_ корневой \_ подписи \_ \_ нет</span><span class="sxs-lookup"><span data-stu-id="5abda-129">[**D3D12\_ROOT\_SIGNATURE\_FLAGS**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_root_signature_flags) flags = D3D12\_ROOT\_SIGNATURE\_FLAG\_NONE</span></span>

</dd> <dt>

<span data-ttu-id="5abda-130">**CD3DX12 \_ \_ корневая \_ сигнатура с версиями \_ (CD3DX12 \_ по умолчанию)**</span><span class="sxs-lookup"><span data-stu-id="5abda-130">**CD3DX12\_VERSIONED\_ROOT\_SIGNATURE\_DESC(CD3DX12\_DEFAULT)**</span></span>
</dt> <dd>

<span data-ttu-id="5abda-131">Создает новый экземпляр CD3DX12 \_ \_ корневой \_ подписи \_ с версией, инициализированной с параметрами по умолчанию:</span><span class="sxs-lookup"><span data-stu-id="5abda-131">Creates a new instance of a CD3DX12\_VERSIONED\_ROOT\_SIGNATURE\_DESC, initialized with the default parameters:</span></span>

<span data-ttu-id="5abda-132">UINT Нумпараметерс = 0</span><span class="sxs-lookup"><span data-stu-id="5abda-132">UINT numParameters = 0</span></span>

<span data-ttu-id="5abda-133">const [**D3D12 \_ root \_ параметр1**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_root_parameter1) \* \_ ппараметерс = null</span><span class="sxs-lookup"><span data-stu-id="5abda-133">const [**D3D12\_ROOT\_PARAMETER1**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_root_parameter1)\* \_pParameters = NULL</span></span>

<span data-ttu-id="5abda-134">UINT Нумстатиксамплерс = 0</span><span class="sxs-lookup"><span data-stu-id="5abda-134">UINT numStaticSamplers = 0</span></span>

<span data-ttu-id="5abda-135">const [**D3D12 \_ static \_ образец \_ DESC**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_static_sampler_desc) \* \_ пстатиксамплерс = null</span><span class="sxs-lookup"><span data-stu-id="5abda-135">const [**D3D12\_STATIC\_SAMPLER\_DESC**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_static_sampler_desc)\* \_pStaticSamplers = NULL</span></span>

<span data-ttu-id="5abda-136">[**D3D12 \_ Флаги \_ \_ ФЛАГов корневой подписи**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_root_signature_flags) = D3D12 \_ корневой \_ подписи \_ \_ нет</span><span class="sxs-lookup"><span data-stu-id="5abda-136">[**D3D12\_ROOT\_SIGNATURE\_FLAGS**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_root_signature_flags) flags = D3D12\_ROOT\_SIGNATURE\_FLAG\_NONE</span></span>

</dd> <dt>

<span data-ttu-id="5abda-137">**Встроенная инициализация \_ 1 \_ 0 (uint нумпараметерс, const D3D12 \_ root, \_ параметр \* \_ ппараметерс, uint нумстатиксамплерс = 0, const D3D12 СТАТИЧЕСКАЯ выборка DESC пстатиксамплерс = null, флаги флагов корневой \_ \_ \_ \* \_ \_ \_ сигнатуры \_ : D3D12 \_ флаг корневой \_ подписи \_ \_ None)**</span><span class="sxs-lookup"><span data-stu-id="5abda-137">**inline Init\_1\_0(UINT numParameters, const D3D12\_ROOT\_PARAMETER\* \_pParameters, UINT numStaticSamplers = 0, const D3D12\_STATIC\_SAMPLER\_DESC\* \_pStaticSamplers = NULL, D3D12\_ROOT\_SIGNATURE\_FLAGS flags = D3D12\_ROOT\_SIGNATURE\_FLAG\_NONE)**</span></span>
</dt> <dd>

<span data-ttu-id="5abda-138">Задает функцию, которая инициализирует следующие параметры:</span><span class="sxs-lookup"><span data-stu-id="5abda-138">Specifies a function that initializes the following parameters:</span></span>

<span data-ttu-id="5abda-139">UINT Нумпараметерс</span><span class="sxs-lookup"><span data-stu-id="5abda-139">UINT numParameters</span></span>

<span data-ttu-id="5abda-140">const [**D3D12 \_ \_ параметр root**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_root_parameter) \* \_ ппараметерс</span><span class="sxs-lookup"><span data-stu-id="5abda-140">const [**D3D12\_ROOT\_PARAMETER**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_root_parameter)\* \_pParameters</span></span>

<span data-ttu-id="5abda-141">UINT Нумстатиксамплерс = 0</span><span class="sxs-lookup"><span data-stu-id="5abda-141">UINT numStaticSamplers = 0</span></span>

<span data-ttu-id="5abda-142">const [**D3D12 \_ static \_ образец \_ DESC**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_static_sampler_desc) \* \_ пстатиксамплерс = null</span><span class="sxs-lookup"><span data-stu-id="5abda-142">const [**D3D12\_STATIC\_SAMPLER\_DESC**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_static_sampler_desc)\* \_pStaticSamplers = NULL</span></span>

<span data-ttu-id="5abda-143">[**D3D12 \_ Флаги \_ \_ ФЛАГов корневой подписи**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_root_signature_flags) = D3D12 \_ корневой \_ подписи \_ \_ нет</span><span class="sxs-lookup"><span data-stu-id="5abda-143">[**D3D12\_ROOT\_SIGNATURE\_FLAGS**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_root_signature_flags) flags = D3D12\_ROOT\_SIGNATURE\_FLAG\_NONE</span></span>

</dd> <dt>

<span data-ttu-id="5abda-144">**Статическая встроенная инициализация \_ 1 \_ 0 (D3D12 \_ \_ с версией root \_ \_ , DESC &DESC, uint нумпараметерс, const D3D12 \_ корневой \_ параметр \* \_ ппараметерс, uint нумстатиксамплерс = 0, const D3D12 статическая выборка \_ \_ \_ DESC \* \_ пстатиксамплерс = null, D3D12 корневой метки флагов \_ \_ \_ = D3D12 \_ флаг корневой \_ подписи \_ \_ None)**</span><span class="sxs-lookup"><span data-stu-id="5abda-144">**static inline Init\_1\_0(D3D12\_VERSIONED\_ROOT\_SIGNATURE\_DESC &desc, UINT numParameters, const D3D12\_ROOT\_PARAMETER\* \_pParameters, UINT numStaticSamplers = 0, const D3D12\_STATIC\_SAMPLER\_DESC\* \_pStaticSamplers = NULL, D3D12\_ROOT\_SIGNATURE\_FLAGS flags = D3D12\_ROOT\_SIGNATURE\_FLAG\_NONE)**</span></span>
</dt> <dd>

<span data-ttu-id="5abda-145">Задает функцию, которая инициализирует следующие параметры:</span><span class="sxs-lookup"><span data-stu-id="5abda-145">Specifies a function that initializes the following parameters:</span></span>

<span data-ttu-id="5abda-146">[**D3D12 \_ ВЕРСИЯ \_ корневой \_ сигнатуры \_ DESC**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_versioned_root_signature_desc) &DESC</span><span class="sxs-lookup"><span data-stu-id="5abda-146">[**D3D12\_VERSIONED\_ROOT\_SIGNATURE\_DESC**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_versioned_root_signature_desc) &desc</span></span>

<span data-ttu-id="5abda-147">UINT Нумпараметерс</span><span class="sxs-lookup"><span data-stu-id="5abda-147">UINT numParameters</span></span>

<span data-ttu-id="5abda-148">const [**D3D12 \_ \_ параметр root**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_root_parameter) \* \_ ппараметерс</span><span class="sxs-lookup"><span data-stu-id="5abda-148">const [**D3D12\_ROOT\_PARAMETER**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_root_parameter)\* \_pParameters</span></span>

<span data-ttu-id="5abda-149">UINT Нумстатиксамплерс = 0</span><span class="sxs-lookup"><span data-stu-id="5abda-149">UINT numStaticSamplers = 0</span></span>

<span data-ttu-id="5abda-150">const [**D3D12 \_ static \_ образец \_ DESC**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_static_sampler_desc) \* \_ пстатиксамплерс = null</span><span class="sxs-lookup"><span data-stu-id="5abda-150">const [**D3D12\_STATIC\_SAMPLER\_DESC**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_static_sampler_desc)\* \_pStaticSamplers = NULL</span></span>

<span data-ttu-id="5abda-151">[**D3D12 \_ Флаги \_ \_ ФЛАГов корневой подписи**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_root_signature_flags) = D3D12 \_ корневой \_ подписи \_ \_ нет</span><span class="sxs-lookup"><span data-stu-id="5abda-151">[**D3D12\_ROOT\_SIGNATURE\_FLAGS**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_root_signature_flags) flags = D3D12\_ROOT\_SIGNATURE\_FLAG\_NONE</span></span>

</dd> <dt>

<span data-ttu-id="5abda-152">**Встроенная инициализация \_ 1 \_ 1 (uint нумпараметерс, const D3D12 \_ root \_ параметр1 \* \_ ппараметерс, uint нумстатиксамплерс = 0, const D3D12 СТАТИЧЕСКАЯ выборка DESC пстатиксамплерс = null, флаги флагов корневой \_ \_ \_ \* \_ \_ \_ подписи \_ : D3D12 \_ флаг корневой \_ подписи \_ \_ None)**</span><span class="sxs-lookup"><span data-stu-id="5abda-152">**inline Init\_1\_1(UINT numParameters, const D3D12\_ROOT\_PARAMETER1\* \_pParameters, UINT numStaticSamplers = 0, const D3D12\_STATIC\_SAMPLER\_DESC\* \_pStaticSamplers = NULL, D3D12\_ROOT\_SIGNATURE\_FLAGS flags = D3D12\_ROOT\_SIGNATURE\_FLAG\_NONE)**</span></span>
</dt> <dd>

<span data-ttu-id="5abda-153">Задает функцию, которая инициализирует следующие параметры:</span><span class="sxs-lookup"><span data-stu-id="5abda-153">Specifies a function that initializes the following parameters:</span></span>

<span data-ttu-id="5abda-154">UINT Нумпараметерс</span><span class="sxs-lookup"><span data-stu-id="5abda-154">UINT numParameters</span></span>

<span data-ttu-id="5abda-155">const [**D3D12 \_ root \_ параметр1**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_root_parameter1) \* \_ ппараметерс</span><span class="sxs-lookup"><span data-stu-id="5abda-155">const [**D3D12\_ROOT\_PARAMETER1**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_root_parameter1)\* \_pParameters</span></span>

<span data-ttu-id="5abda-156">UINT Нумстатиксамплерс = 0</span><span class="sxs-lookup"><span data-stu-id="5abda-156">UINT numStaticSamplers = 0</span></span>

<span data-ttu-id="5abda-157">const [**D3D12 \_ static \_ образец \_ DESC**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_static_sampler_desc) \* \_ пстатиксамплерс = null</span><span class="sxs-lookup"><span data-stu-id="5abda-157">const [**D3D12\_STATIC\_SAMPLER\_DESC**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_static_sampler_desc)\* \_pStaticSamplers = NULL</span></span>

<span data-ttu-id="5abda-158">[**D3D12 \_ Флаги \_ \_ ФЛАГов корневой подписи**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_root_signature_flags) = D3D12 \_ корневой \_ подписи \_ \_ нет</span><span class="sxs-lookup"><span data-stu-id="5abda-158">[**D3D12\_ROOT\_SIGNATURE\_FLAGS**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_root_signature_flags) flags = D3D12\_ROOT\_SIGNATURE\_FLAG\_NONE</span></span>

</dd> <dt>

<span data-ttu-id="5abda-159">**Статическая встроенная инициализация \_ 1 \_ 1 (D3D12 \_ \_ с версией корневой \_ сигнатуры \_ DESC &DESC, uint нумпараметерс, const D3D12 \_ root \_ параметр1 \* \_ ппараметерс, uint нумстатиксамплерс = 0, const D3D12 \_ static \_ образец \_ DESC \* \_ пстатиксамплерс = null, D3D12 корневой подписи флаги \_ \_ \_ = D3D12 \_ флаг корневой \_ подписи \_ \_ None)**</span><span class="sxs-lookup"><span data-stu-id="5abda-159">**static inline Init\_1\_1(D3D12\_VERSIONED\_ROOT\_SIGNATURE\_DESC &desc, UINT numParameters, const D3D12\_ROOT\_PARAMETER1\* \_pParameters, UINT numStaticSamplers = 0, const D3D12\_STATIC\_SAMPLER\_DESC\* \_pStaticSamplers = NULL, D3D12\_ROOT\_SIGNATURE\_FLAGS flags = D3D12\_ROOT\_SIGNATURE\_FLAG\_NONE)**</span></span>
</dt> <dd>

<span data-ttu-id="5abda-160">Задает функцию, которая инициализирует следующие параметры:</span><span class="sxs-lookup"><span data-stu-id="5abda-160">Specifies a function that initializes the following parameters:</span></span>

<span data-ttu-id="5abda-161">[**D3D12 \_ ВЕРСИЯ \_ корневой \_ сигнатуры \_ DESC**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_versioned_root_signature_desc) &DESC</span><span class="sxs-lookup"><span data-stu-id="5abda-161">[**D3D12\_VERSIONED\_ROOT\_SIGNATURE\_DESC**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_versioned_root_signature_desc) &desc</span></span>

<span data-ttu-id="5abda-162">UINT Нумпараметерс</span><span class="sxs-lookup"><span data-stu-id="5abda-162">UINT numParameters</span></span>

<span data-ttu-id="5abda-163">const [**D3D12 \_ root \_ параметр1**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_root_parameter1) \* \_ ппараметерс</span><span class="sxs-lookup"><span data-stu-id="5abda-163">const [**D3D12\_ROOT\_PARAMETER1**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_root_parameter1)\* \_pParameters</span></span>

<span data-ttu-id="5abda-164">UINT Нумстатиксамплерс = 0</span><span class="sxs-lookup"><span data-stu-id="5abda-164">UINT numStaticSamplers = 0</span></span>

<span data-ttu-id="5abda-165">const [**D3D12 \_ static \_ образец \_ DESC**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_static_sampler_desc) \* \_ пстатиксамплерс = null</span><span class="sxs-lookup"><span data-stu-id="5abda-165">const [**D3D12\_STATIC\_SAMPLER\_DESC**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_static_sampler_desc)\* \_pStaticSamplers = NULL</span></span>

<span data-ttu-id="5abda-166">[**D3D12 \_ Флаги \_ \_ ФЛАГов корневой подписи**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_root_signature_flags) = D3D12 \_ корневой \_ подписи \_ \_ нет</span><span class="sxs-lookup"><span data-stu-id="5abda-166">[**D3D12\_ROOT\_SIGNATURE\_FLAGS**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_root_signature_flags) flags = D3D12\_ROOT\_SIGNATURE\_FLAG\_NONE</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="5abda-167">Требования</span><span class="sxs-lookup"><span data-stu-id="5abda-167">Requirements</span></span>



| <span data-ttu-id="5abda-168">Требование</span><span class="sxs-lookup"><span data-stu-id="5abda-168">Requirement</span></span> | <span data-ttu-id="5abda-169">Значение</span><span class="sxs-lookup"><span data-stu-id="5abda-169">Value</span></span> |
|-------------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="5abda-170">Header</span><span class="sxs-lookup"><span data-stu-id="5abda-170">Header</span></span><br/> | <dl> <span data-ttu-id="5abda-171"><dt>D3dx12. h</dt></span><span class="sxs-lookup"><span data-stu-id="5abda-171"><dt>D3dx12.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="5abda-172">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="5abda-172">See also</span></span>

<dl> <dt>

[<span data-ttu-id="5abda-173">**D3D12 \_ \_ корневая \_ сигнатура с \_ версией**</span><span class="sxs-lookup"><span data-stu-id="5abda-173">**D3D12\_VERSIONED\_ROOT\_SIGNATURE\_DESC**</span></span>](/windows/desktop/api/d3d12/ns-d3d12-d3d12_versioned_root_signature_desc)
</dt> <dt>

[<span data-ttu-id="5abda-174">Вспомогательные структуры для D3D12</span><span class="sxs-lookup"><span data-stu-id="5abda-174">Helper Structures for D3D12</span></span>](helper-structures-for-d3d12.md)
</dt> </dl>

 

 





