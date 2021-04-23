---
title: Структура CD3DX12_ROOT_PARAMETER1 (D3dx12. h)
description: Вспомогательная структура, позволяющая легко инициализировать структуру D3D12 \_ root \_ параметр1.
ms.assetid: CDE0C02E-0112-4FD9-A4A2-36E8C326715C
keywords:
- Структура CD3DX12_ROOT_PARAMETER1
topic_type:
- apiref
api_name:
- CD3DX12_ROOT_PARAMETER1
api_location:
- d3dx12.h
api_type:
- HeaderDef
ms.localizationpriority: low
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0d582016b26df0d57f7792afd30fc4fcbf3ba97b
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/15/2021
ms.locfileid: "105713968"
---
# <a name="cd3dx12_root_parameter1-structure"></a><span data-ttu-id="2450f-104">\_Корневая \_ Структура параметр1 CD3DX12</span><span class="sxs-lookup"><span data-stu-id="2450f-104">CD3DX12\_ROOT\_PARAMETER1 structure</span></span>

<span data-ttu-id="2450f-105">Вспомогательная структура, позволяющая легко инициализировать структуру [**D3D12 \_ root \_ параметр1**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_root_parameter1) .</span><span class="sxs-lookup"><span data-stu-id="2450f-105">A helper structure to enable easy initialization of a [**D3D12\_ROOT\_PARAMETER1**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_root_parameter1) structure.</span></span>

## <a name="syntax"></a><span data-ttu-id="2450f-106">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="2450f-106">Syntax</span></span>


```C++
struct CD3DX12_ROOT_PARAMETER1  : public D3D12_ROOT_PARAMETER1{
       CD3DX12_ROOT_PARAMETER1();
       explicit CD3DX12_ROOT_PARAMETER1(const D3D12_ROOT_PARAMETER1 &o);
  void static inline InitAsDescriptorTable(D3D12_ROOT_PARAMETER1 &rootParam, UINT numDescriptorRanges, const D3D12_DESCRIPTOR_RANGE1* pDescriptorRanges, D3D12_SHADER_VISIBILITY visibility = D3D12_SHADER_VISIBILITY_ALL);
  void static inline InitAsConstants(D3D12_ROOT_PARAMETER1 &rootParam, UINT num32BitValues, UINT shaderRegister, UINT registerSpace = 0, D3D12_SHADER_VISIBILITY visibility = D3D12_SHADER_VISIBILITY_ALL);
  void static inline InitAsConstantBufferView(D3D12_ROOT_PARAMETER1 &rootParam, UINT shaderRegister, UINT registerSpace = 0, D3D12_ROOT_DESCRIPTOR_FLAGS flags = D3D12_ROOT_DESCRIPTOR_FLAG_NONE, D3D12_SHADER_VISIBILITY visibility = D3D12_SHADER_VISIBILITY_ALL);
  void static inline InitAsShaderResourceView(D3D12_ROOT_PARAMETER1 &rootParam, UINT shaderRegister, UINT registerSpace = 0, D3D12_ROOT_DESCRIPTOR_FLAGS flags = D3D12_ROOT_DESCRIPTOR_FLAG_NONE, D3D12_SHADER_VISIBILITY visibility = D3D12_SHADER_VISIBILITY_ALL);
  void static inline InitAsUnorderedAccessView(D3D12_ROOT_PARAMETER1 &rootParam, UINT shaderRegister, UINT registerSpace = 0, D3D12_ROOT_DESCRIPTOR_FLAGS flags = D3D12_ROOT_DESCRIPTOR_FLAG_NONE, D3D12_SHADER_VISIBILITY visibility = D3D12_SHADER_VISIBILITY_ALL);
  void inline InitAsDescriptorTable(UINT numDescriptorRanges, const D3D12_DESCRIPTOR_RANGE1* pDescriptorRanges, D3D12_SHADER_VISIBILITY visibility = D3D12_SHADER_VISIBILITY_ALL);
  void inline InitAsConstants(UINT num32BitValues, UINT shaderRegister, UINT registerSpace = 0, D3D12_SHADER_VISIBILITY visibility = D3D12_SHADER_VISIBILITY_ALL);
  void inline InitAsConstantBufferView(UINT shaderRegister, UINT registerSpace = 0, D3D12_ROOT_DESCRIPTOR_FLAGS flags = D3D12_ROOT_DESCRIPTOR_FLAG_NONE, D3D12_SHADER_VISIBILITY visibility = D3D12_SHADER_VISIBILITY_ALL);
  void inline InitAsShaderResourceView(UINT shaderRegister, UINT registerSpace = 0, D3D12_ROOT_DESCRIPTOR_FLAGS flags = D3D12_ROOT_DESCRIPTOR_FLAG_NONE, D3D12_SHADER_VISIBILITY visibility = D3D12_SHADER_VISIBILITY_ALL);
  void inline InitAsUnorderedAccessView(UINT shaderRegister, UINT registerSpace = 0, D3D12_ROOT_DESCRIPTOR_FLAGS flags = D3D12_ROOT_DESCRIPTOR_FLAG_NONE, D3D12_SHADER_VISIBILITY visibility = D3D12_SHADER_VISIBILITY_ALL);
};
```



## <a name="members"></a><span data-ttu-id="2450f-107">Члены</span><span class="sxs-lookup"><span data-stu-id="2450f-107">Members</span></span>

<dl> <dt>

<span data-ttu-id="2450f-108">**\_Корневой элемент \_ параметр1 CD3DX12 ()**</span><span class="sxs-lookup"><span data-stu-id="2450f-108">**CD3DX12\_ROOT\_PARAMETER1()**</span></span>
</dt> <dd>

<span data-ttu-id="2450f-109">Создает новый, неинициализированный экземпляр CD3DX12 \_ корневого элемента \_ параметр1.</span><span class="sxs-lookup"><span data-stu-id="2450f-109">Creates a new, uninitialized, instance of a CD3DX12\_ROOT\_PARAMETER1.</span></span>

</dd> <dt>

<span data-ttu-id="2450f-110">**явный CD3DX12 \_ root \_ параметр1 (const D3D12 \_ root \_ параметр1 &o)**</span><span class="sxs-lookup"><span data-stu-id="2450f-110">**explicit CD3DX12\_ROOT\_PARAMETER1(const D3D12\_ROOT\_PARAMETER1 &o)**</span></span>
</dt> <dd>

<span data-ttu-id="2450f-111">Создает новый экземпляр CD3DX12 \_ root \_ параметр1, инициализируемый с помощью содержимого другой [**\_ корневой структуры \_ параметр1 D3D12**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_root_parameter1) .</span><span class="sxs-lookup"><span data-stu-id="2450f-111">Creates a new instance of a CD3DX12\_ROOT\_PARAMETER1, initialized with the contents of another [**D3D12\_ROOT\_PARAMETER1**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_root_parameter1) structure.</span></span>

</dd> <dt>

<span data-ttu-id="2450f-112">**static Inline Инитасдескриптортабле (D3D12 \_ root \_ параметр1 &РУТПАРАМ, uint нумдескрипторранжес, const D3D12 \_ дескриптор \_ высокое \* пдескрипторранжес, D3D12 видимость \_ видимости шейдера \_ = D3D12 \_ видимость шейдера \_ \_ )**</span><span class="sxs-lookup"><span data-stu-id="2450f-112">**static inline InitAsDescriptorTable(D3D12\_ROOT\_PARAMETER1 &rootParam, UINT numDescriptorRanges, const D3D12\_DESCRIPTOR\_RANGE1\* pDescriptorRanges, D3D12\_SHADER\_VISIBILITY visibility = D3D12\_SHADER\_VISIBILITY\_ALL)**</span></span>
</dt> <dd>

<span data-ttu-id="2450f-113">Задает функцию, которая инициализирует следующие параметры:</span><span class="sxs-lookup"><span data-stu-id="2450f-113">Specifies a function that initializes the following parameters:</span></span>

<span data-ttu-id="2450f-114">[**D3D12 \_ КОРНЕВой элемент \_ параметр1**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_root_parameter1) &рутпарам</span><span class="sxs-lookup"><span data-stu-id="2450f-114">[**D3D12\_ROOT\_PARAMETER1**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_root_parameter1) &rootParam</span></span>

<span data-ttu-id="2450f-115">UINT Нумдескрипторранжес</span><span class="sxs-lookup"><span data-stu-id="2450f-115">UINT numDescriptorRanges</span></span>

<span data-ttu-id="2450f-116">const [**D3D12 \_ дескриптор \_ высокое**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_descriptor_range1) \* пдескрипторранжес</span><span class="sxs-lookup"><span data-stu-id="2450f-116">const [**D3D12\_DESCRIPTOR\_RANGE1**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_descriptor_range1)\* pDescriptorRanges</span></span>

<span data-ttu-id="2450f-117">[**D3D12 \_ Видимость \_ видимости шейдера**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_shader_visibility) = D3D12 \_ \_ видимость шейдера \_</span><span class="sxs-lookup"><span data-stu-id="2450f-117">[**D3D12\_SHADER\_VISIBILITY**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_shader_visibility) visibility = D3D12\_SHADER\_VISIBILITY\_ALL</span></span>

</dd> <dt>

<span data-ttu-id="2450f-118">**static Inline Инитасконстантс (D3D12 \_ root \_ параметр1 &РУТПАРАМ, uint NUM32BITVALUES, uint ШАДЕРРЕГИСТЕР, uint регистерспаце = 0, D3D12 \_ ШЕЙДЕР видимости \_ = D3D12 \_ видимость шейдера \_ \_ )**</span><span class="sxs-lookup"><span data-stu-id="2450f-118">**static inline InitAsConstants(D3D12\_ROOT\_PARAMETER1 &rootParam, UINT num32BitValues, UINT shaderRegister, UINT registerSpace = 0, D3D12\_SHADER\_VISIBILITY visibility = D3D12\_SHADER\_VISIBILITY\_ALL)**</span></span>
</dt> <dd>

<span data-ttu-id="2450f-119">Задает функцию, которая инициализирует следующие параметры:</span><span class="sxs-lookup"><span data-stu-id="2450f-119">Specifies a function that initializes the following parameters:</span></span>

<span data-ttu-id="2450f-120">[**D3D12 \_ КОРНЕВой элемент \_ параметр1**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_root_parameter1) &рутпарам</span><span class="sxs-lookup"><span data-stu-id="2450f-120">[**D3D12\_ROOT\_PARAMETER1**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_root_parameter1) &rootParam</span></span>

<span data-ttu-id="2450f-121">UINT num32BitValues</span><span class="sxs-lookup"><span data-stu-id="2450f-121">UINT num32BitValues</span></span>

<span data-ttu-id="2450f-122">UINT Шадеррегистер</span><span class="sxs-lookup"><span data-stu-id="2450f-122">UINT shaderRegister</span></span>

<span data-ttu-id="2450f-123">UINT Регистерспаце = 0</span><span class="sxs-lookup"><span data-stu-id="2450f-123">UINT registerSpace = 0</span></span>

<span data-ttu-id="2450f-124">[**D3D12 \_ Видимость \_ видимости шейдера**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_shader_visibility) = D3D12 \_ \_ видимость шейдера \_</span><span class="sxs-lookup"><span data-stu-id="2450f-124">[**D3D12\_SHADER\_VISIBILITY**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_shader_visibility) visibility = D3D12\_SHADER\_VISIBILITY\_ALL</span></span>

</dd> <dt>

<span data-ttu-id="2450f-125">**static Inline Инитасконстантбуффервиев (D3D12 \_ root \_ параметр1 &РУТПАРАМ, uint ШАДЕРРЕГИСТЕР, uint регистерспаце = 0, D3D12 флаги \_ flags root-дескриптора \_ \_ = D3D12 \_ корневого \_ дескриптора " \_ \_ нет", D3D12 видимость \_ видимости шейдеров \_ = D3D12 \_ видимость шейдеров \_ \_ )**</span><span class="sxs-lookup"><span data-stu-id="2450f-125">**static inline InitAsConstantBufferView(D3D12\_ROOT\_PARAMETER1 &rootParam, UINT shaderRegister, UINT registerSpace = 0, D3D12\_ROOT\_DESCRIPTOR\_FLAGS flags = D3D12\_ROOT\_DESCRIPTOR\_FLAG\_NONE, D3D12\_SHADER\_VISIBILITY visibility = D3D12\_SHADER\_VISIBILITY\_ALL)**</span></span>
</dt> <dd>

<span data-ttu-id="2450f-126">Задает функцию, которая инициализирует следующие параметры:</span><span class="sxs-lookup"><span data-stu-id="2450f-126">Specifies a function that initializes the following parameters:</span></span>

<span data-ttu-id="2450f-127">[**D3D12 \_ КОРНЕВой элемент \_ параметр1**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_root_parameter1) &рутпарам</span><span class="sxs-lookup"><span data-stu-id="2450f-127">[**D3D12\_ROOT\_PARAMETER1**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_root_parameter1) &rootParam</span></span>

<span data-ttu-id="2450f-128">UINT Шадеррегистер</span><span class="sxs-lookup"><span data-stu-id="2450f-128">UINT shaderRegister</span></span>

<span data-ttu-id="2450f-129">UINT Регистерспаце = 0</span><span class="sxs-lookup"><span data-stu-id="2450f-129">UINT registerSpace = 0</span></span>

<span data-ttu-id="2450f-130">[**D3D12 \_ Флаги флагов КОРНЕВого \_ дескриптора \_**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_root_descriptor_flags) = D3D12 \_ корневого \_ дескриптора \_ \_ None</span><span class="sxs-lookup"><span data-stu-id="2450f-130">[**D3D12\_ROOT\_DESCRIPTOR\_FLAGS**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_root_descriptor_flags) flags = D3D12\_ROOT\_DESCRIPTOR\_FLAG\_NONE</span></span>

<span data-ttu-id="2450f-131">[**D3D12 \_ Видимость \_ видимости шейдера**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_shader_visibility) = D3D12 \_ \_ видимость шейдера \_</span><span class="sxs-lookup"><span data-stu-id="2450f-131">[**D3D12\_SHADER\_VISIBILITY**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_shader_visibility) visibility = D3D12\_SHADER\_VISIBILITY\_ALL</span></span>

</dd> <dt>

<span data-ttu-id="2450f-132">**static Inline Инитасшадерресаурцевиев (D3D12 \_ root \_ параметр1 &РУТПАРАМ, uint ШАДЕРРЕГИСТЕР, uint регистерспаце = 0, D3D12 флаги \_ flags root-дескриптора \_ \_ = D3D12 \_ корневого \_ дескриптора " \_ \_ нет", D3D12 видимость \_ видимости шейдеров \_ = D3D12 \_ видимость шейдеров \_ \_ )**</span><span class="sxs-lookup"><span data-stu-id="2450f-132">**static inline InitAsShaderResourceView(D3D12\_ROOT\_PARAMETER1 &rootParam, UINT shaderRegister, UINT registerSpace = 0, D3D12\_ROOT\_DESCRIPTOR\_FLAGS flags = D3D12\_ROOT\_DESCRIPTOR\_FLAG\_NONE, D3D12\_SHADER\_VISIBILITY visibility = D3D12\_SHADER\_VISIBILITY\_ALL)**</span></span>
</dt> <dd>

<span data-ttu-id="2450f-133">Задает функцию, которая инициализирует следующие параметры:</span><span class="sxs-lookup"><span data-stu-id="2450f-133">Specifies a function that initializes the following parameters:</span></span>

<span data-ttu-id="2450f-134">[**D3D12 \_ КОРНЕВой элемент \_ параметр1**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_root_parameter1) &рутпарам</span><span class="sxs-lookup"><span data-stu-id="2450f-134">[**D3D12\_ROOT\_PARAMETER1**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_root_parameter1) &rootParam</span></span>

<span data-ttu-id="2450f-135">UINT Шадеррегистер</span><span class="sxs-lookup"><span data-stu-id="2450f-135">UINT shaderRegister</span></span>

<span data-ttu-id="2450f-136">UINT Регистерспаце = 0</span><span class="sxs-lookup"><span data-stu-id="2450f-136">UINT registerSpace = 0</span></span>

<span data-ttu-id="2450f-137">[**D3D12 \_ Флаги флагов КОРНЕВого \_ дескриптора \_**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_root_descriptor_flags) = D3D12 \_ корневого \_ дескриптора \_ \_ None</span><span class="sxs-lookup"><span data-stu-id="2450f-137">[**D3D12\_ROOT\_DESCRIPTOR\_FLAGS**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_root_descriptor_flags) flags = D3D12\_ROOT\_DESCRIPTOR\_FLAG\_NONE</span></span>

<span data-ttu-id="2450f-138">[**D3D12 \_ Видимость \_ видимости шейдера**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_shader_visibility) = D3D12 \_ \_ видимость шейдера \_</span><span class="sxs-lookup"><span data-stu-id="2450f-138">[**D3D12\_SHADER\_VISIBILITY**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_shader_visibility) visibility = D3D12\_SHADER\_VISIBILITY\_ALL</span></span>

</dd> <dt>

<span data-ttu-id="2450f-139">**static Inline Инитасунордередакцессвиев (D3D12 \_ root \_ параметр1 &РУТПАРАМ, uint ШАДЕРРЕГИСТЕР, uint регистерспаце = 0, D3D12 флаги \_ flags root-дескриптора \_ \_ = D3D12 \_ корневого \_ дескриптора " \_ \_ нет", D3D12 видимость \_ видимости шейдеров \_ = D3D12 \_ видимость шейдеров \_ \_ )**</span><span class="sxs-lookup"><span data-stu-id="2450f-139">**static inline InitAsUnorderedAccessView(D3D12\_ROOT\_PARAMETER1 &rootParam, UINT shaderRegister, UINT registerSpace = 0, D3D12\_ROOT\_DESCRIPTOR\_FLAGS flags = D3D12\_ROOT\_DESCRIPTOR\_FLAG\_NONE, D3D12\_SHADER\_VISIBILITY visibility = D3D12\_SHADER\_VISIBILITY\_ALL)**</span></span>
</dt> <dd>

<span data-ttu-id="2450f-140">Задает функцию, которая инициализирует следующие параметры:</span><span class="sxs-lookup"><span data-stu-id="2450f-140">Specifies a function that initializes the following parameters:</span></span>

<span data-ttu-id="2450f-141">[**D3D12 \_ КОРНЕВой элемент \_ параметр1**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_root_parameter1) &рутпарам</span><span class="sxs-lookup"><span data-stu-id="2450f-141">[**D3D12\_ROOT\_PARAMETER1**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_root_parameter1) &rootParam</span></span>

<span data-ttu-id="2450f-142">UINT Шадеррегистер</span><span class="sxs-lookup"><span data-stu-id="2450f-142">UINT shaderRegister</span></span>

<span data-ttu-id="2450f-143">UINT Регистерспаце = 0</span><span class="sxs-lookup"><span data-stu-id="2450f-143">UINT registerSpace = 0</span></span>

<span data-ttu-id="2450f-144">[**D3D12 \_ Флаги флагов КОРНЕВого \_ дескриптора \_**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_root_descriptor_flags) = D3D12 \_ корневого \_ дескриптора \_ \_ None</span><span class="sxs-lookup"><span data-stu-id="2450f-144">[**D3D12\_ROOT\_DESCRIPTOR\_FLAGS**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_root_descriptor_flags) flags = D3D12\_ROOT\_DESCRIPTOR\_FLAG\_NONE</span></span>

<span data-ttu-id="2450f-145">[**D3D12 \_ Видимость \_ видимости шейдера**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_shader_visibility) = D3D12 \_ \_ видимость шейдера \_</span><span class="sxs-lookup"><span data-stu-id="2450f-145">[**D3D12\_SHADER\_VISIBILITY**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_shader_visibility) visibility = D3D12\_SHADER\_VISIBILITY\_ALL</span></span>

</dd> <dt>

<span data-ttu-id="2450f-146">**Inline Инитасдескриптортабле (UINT Нумдескрипторранжес, const D3D12 \_ дескриптор \_ высокое \* пдескрипторранжес, D3D12 видимость \_ видимости шейдера \_ = D3D12 \_ видимость шейдера \_ \_ )**</span><span class="sxs-lookup"><span data-stu-id="2450f-146">**inline InitAsDescriptorTable(UINT numDescriptorRanges, const D3D12\_DESCRIPTOR\_RANGE1\* pDescriptorRanges, D3D12\_SHADER\_VISIBILITY visibility = D3D12\_SHADER\_VISIBILITY\_ALL)**</span></span>
</dt> <dd>

<span data-ttu-id="2450f-147">Задает функцию, которая инициализирует следующие параметры:</span><span class="sxs-lookup"><span data-stu-id="2450f-147">Specifies a function that initializes the following parameters:</span></span>

<span data-ttu-id="2450f-148">UINT Нумдескрипторранжес</span><span class="sxs-lookup"><span data-stu-id="2450f-148">UINT numDescriptorRanges</span></span>

<span data-ttu-id="2450f-149">const [**D3D12 \_ дескриптор \_ высокое**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_descriptor_range1) \* пдескрипторранжес</span><span class="sxs-lookup"><span data-stu-id="2450f-149">const [**D3D12\_DESCRIPTOR\_RANGE1**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_descriptor_range1)\* pDescriptorRanges</span></span>

<span data-ttu-id="2450f-150">[**D3D12 \_ Видимость \_ видимости шейдера**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_shader_visibility) = D3D12 \_ \_ видимость шейдера \_</span><span class="sxs-lookup"><span data-stu-id="2450f-150">[**D3D12\_SHADER\_VISIBILITY**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_shader_visibility) visibility = D3D12\_SHADER\_VISIBILITY\_ALL</span></span>

</dd> <dt>

<span data-ttu-id="2450f-151">**Inline Инитасконстантс (UINT num32BitValues, UINT Шадеррегистер, UINT Регистерспаце = 0, видимость D3D12 \_ шейдер видимости \_ = D3D12 \_ видимость шейдера \_ \_ )**</span><span class="sxs-lookup"><span data-stu-id="2450f-151">**inline InitAsConstants(UINT num32BitValues, UINT shaderRegister, UINT registerSpace = 0, D3D12\_SHADER\_VISIBILITY visibility = D3D12\_SHADER\_VISIBILITY\_ALL)**</span></span>
</dt> <dd>

<span data-ttu-id="2450f-152">Задает функцию, которая инициализирует следующие параметры:</span><span class="sxs-lookup"><span data-stu-id="2450f-152">Specifies a function that initializes the following parameters:</span></span>

<span data-ttu-id="2450f-153">UINT num32BitValues</span><span class="sxs-lookup"><span data-stu-id="2450f-153">UINT num32BitValues</span></span>

<span data-ttu-id="2450f-154">UINT Шадеррегистер</span><span class="sxs-lookup"><span data-stu-id="2450f-154">UINT shaderRegister</span></span>

<span data-ttu-id="2450f-155">UINT Регистерспаце = 0</span><span class="sxs-lookup"><span data-stu-id="2450f-155">UINT registerSpace = 0</span></span>

<span data-ttu-id="2450f-156">[**D3D12 \_ Видимость \_ видимости шейдера**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_shader_visibility) = D3D12 \_ \_ видимость шейдера \_</span><span class="sxs-lookup"><span data-stu-id="2450f-156">[**D3D12\_SHADER\_VISIBILITY**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_shader_visibility) visibility = D3D12\_SHADER\_VISIBILITY\_ALL</span></span>

</dd> <dt>

<span data-ttu-id="2450f-157">**Inline Инитасконстантбуффервиев (UINT Шадеррегистер, UINT Регистерспаце = 0, D3D12 флаги \_ flags в корневом \_ дескрипторе \_ = D3D12 \_ флаг корневого \_ дескриптора \_ \_ нет, D3D12 видимость \_ видимости шейдеров \_ = D3D12 \_ видимость шейдера \_ \_ )**</span><span class="sxs-lookup"><span data-stu-id="2450f-157">**inline InitAsConstantBufferView(UINT shaderRegister, UINT registerSpace = 0, D3D12\_ROOT\_DESCRIPTOR\_FLAGS flags = D3D12\_ROOT\_DESCRIPTOR\_FLAG\_NONE, D3D12\_SHADER\_VISIBILITY visibility = D3D12\_SHADER\_VISIBILITY\_ALL)**</span></span>
</dt> <dd>

<span data-ttu-id="2450f-158">Задает функцию, которая инициализирует следующие параметры:</span><span class="sxs-lookup"><span data-stu-id="2450f-158">Specifies a function that initializes the following parameters:</span></span>

<span data-ttu-id="2450f-159">UINT Шадеррегистер</span><span class="sxs-lookup"><span data-stu-id="2450f-159">UINT shaderRegister</span></span>

<span data-ttu-id="2450f-160">UINT Регистерспаце = 0</span><span class="sxs-lookup"><span data-stu-id="2450f-160">UINT registerSpace = 0</span></span>

<span data-ttu-id="2450f-161">[**D3D12 \_ Флаги флагов КОРНЕВого \_ дескриптора \_**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_root_descriptor_flags) = D3D12 \_ корневого \_ дескриптора \_ \_ None</span><span class="sxs-lookup"><span data-stu-id="2450f-161">[**D3D12\_ROOT\_DESCRIPTOR\_FLAGS**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_root_descriptor_flags) flags = D3D12\_ROOT\_DESCRIPTOR\_FLAG\_NONE</span></span>

<span data-ttu-id="2450f-162">[**D3D12 \_ Видимость \_ видимости шейдера**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_shader_visibility) = D3D12 \_ \_ видимость шейдера \_</span><span class="sxs-lookup"><span data-stu-id="2450f-162">[**D3D12\_SHADER\_VISIBILITY**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_shader_visibility) visibility = D3D12\_SHADER\_VISIBILITY\_ALL</span></span>

</dd> <dt>

<span data-ttu-id="2450f-163">**Inline Инитасшадерресаурцевиев (UINT Шадеррегистер, UINT Регистерспаце = 0, D3D12 флаги \_ flags в корневом \_ дескрипторе \_ = D3D12 \_ флаг корневого \_ дескриптора \_ \_ нет, D3D12 видимость \_ видимости шейдеров \_ = D3D12 \_ видимость шейдера \_ \_ )**</span><span class="sxs-lookup"><span data-stu-id="2450f-163">**inline InitAsShaderResourceView(UINT shaderRegister, UINT registerSpace = 0, D3D12\_ROOT\_DESCRIPTOR\_FLAGS flags = D3D12\_ROOT\_DESCRIPTOR\_FLAG\_NONE, D3D12\_SHADER\_VISIBILITY visibility = D3D12\_SHADER\_VISIBILITY\_ALL)**</span></span>
</dt> <dd>

<span data-ttu-id="2450f-164">Задает функцию, которая инициализирует следующие параметры:</span><span class="sxs-lookup"><span data-stu-id="2450f-164">Specifies a function that initializes the following parameters:</span></span>

<span data-ttu-id="2450f-165">UINT Шадеррегистер</span><span class="sxs-lookup"><span data-stu-id="2450f-165">UINT shaderRegister</span></span>

<span data-ttu-id="2450f-166">UINT Регистерспаце = 0</span><span class="sxs-lookup"><span data-stu-id="2450f-166">UINT registerSpace = 0</span></span>

<span data-ttu-id="2450f-167">[**D3D12 \_ Флаги флагов КОРНЕВого \_ дескриптора \_**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_root_descriptor_flags) = D3D12 \_ корневого \_ дескриптора \_ \_ None</span><span class="sxs-lookup"><span data-stu-id="2450f-167">[**D3D12\_ROOT\_DESCRIPTOR\_FLAGS**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_root_descriptor_flags) flags = D3D12\_ROOT\_DESCRIPTOR\_FLAG\_NONE</span></span>

<span data-ttu-id="2450f-168">[**D3D12 \_ Видимость \_ видимости шейдера**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_shader_visibility) = D3D12 \_ \_ видимость шейдера \_</span><span class="sxs-lookup"><span data-stu-id="2450f-168">[**D3D12\_SHADER\_VISIBILITY**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_shader_visibility) visibility = D3D12\_SHADER\_VISIBILITY\_ALL</span></span>

</dd> <dt>

<span data-ttu-id="2450f-169">**Inline Инитасунордередакцессвиев (UINT Шадеррегистер, UINT Регистерспаце = 0, D3D12 флаги \_ flags в корневом \_ дескрипторе \_ = D3D12 \_ флаг корневого \_ дескриптора \_ \_ нет, D3D12 видимость \_ видимости шейдеров \_ = D3D12 \_ видимость шейдера \_ \_ )**</span><span class="sxs-lookup"><span data-stu-id="2450f-169">**inline InitAsUnorderedAccessView(UINT shaderRegister, UINT registerSpace = 0, D3D12\_ROOT\_DESCRIPTOR\_FLAGS flags = D3D12\_ROOT\_DESCRIPTOR\_FLAG\_NONE, D3D12\_SHADER\_VISIBILITY visibility = D3D12\_SHADER\_VISIBILITY\_ALL)**</span></span>
</dt> <dd>

<span data-ttu-id="2450f-170">Задает функцию, которая инициализирует следующие параметры:</span><span class="sxs-lookup"><span data-stu-id="2450f-170">Specifies a function that initializes the following parameters:</span></span>

<span data-ttu-id="2450f-171">UINT Шадеррегистер</span><span class="sxs-lookup"><span data-stu-id="2450f-171">UINT shaderRegister</span></span>

<span data-ttu-id="2450f-172">UINT Регистерспаце = 0</span><span class="sxs-lookup"><span data-stu-id="2450f-172">UINT registerSpace = 0</span></span>

<span data-ttu-id="2450f-173">[**D3D12 \_ Флаги флагов КОРНЕВого \_ дескриптора \_**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_root_descriptor_flags) = D3D12 \_ корневого \_ дескриптора \_ \_ None</span><span class="sxs-lookup"><span data-stu-id="2450f-173">[**D3D12\_ROOT\_DESCRIPTOR\_FLAGS**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_root_descriptor_flags) flags = D3D12\_ROOT\_DESCRIPTOR\_FLAG\_NONE</span></span>

<span data-ttu-id="2450f-174">[**D3D12 \_ Видимость \_ видимости шейдера**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_shader_visibility) = D3D12 \_ \_ видимость шейдера \_</span><span class="sxs-lookup"><span data-stu-id="2450f-174">[**D3D12\_SHADER\_VISIBILITY**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_shader_visibility) visibility = D3D12\_SHADER\_VISIBILITY\_ALL</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="2450f-175">Требования</span><span class="sxs-lookup"><span data-stu-id="2450f-175">Requirements</span></span>



| <span data-ttu-id="2450f-176">Требование</span><span class="sxs-lookup"><span data-stu-id="2450f-176">Requirement</span></span> | <span data-ttu-id="2450f-177">Значение</span><span class="sxs-lookup"><span data-stu-id="2450f-177">Value</span></span> |
|-------------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="2450f-178">Header</span><span class="sxs-lookup"><span data-stu-id="2450f-178">Header</span></span><br/> | <dl> <span data-ttu-id="2450f-179"><dt>D3dx12. h</dt></span><span class="sxs-lookup"><span data-stu-id="2450f-179"><dt>D3dx12.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="2450f-180">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="2450f-180">See also</span></span>

<dl> <dt>

[<span data-ttu-id="2450f-181">**\_Корневой элемент \_ параметр1 D3D12**</span><span class="sxs-lookup"><span data-stu-id="2450f-181">**D3D12\_ROOT\_PARAMETER1**</span></span>](/windows/desktop/api/d3d12/ns-d3d12-d3d12_root_parameter1)
</dt> <dt>

[<span data-ttu-id="2450f-182">Вспомогательные структуры для D3D12</span><span class="sxs-lookup"><span data-stu-id="2450f-182">Helper Structures for D3D12</span></span>](helper-structures-for-d3d12.md)
</dt> </dl>

 

 





