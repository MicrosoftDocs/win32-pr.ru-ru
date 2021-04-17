---
title: Структура CD3DX12_ROOT_PARAMETER (D3dx12. h)
description: Вспомогательная структура, позволяющая упростить инициализацию \_ структуры корневого \_ параметра D3D12.
ms.assetid: CDDF84D0-4E66-4CF2-999B-3F401E8DD17F
keywords:
- Структура CD3DX12_ROOT_PARAMETER
topic_type:
- apiref
api_name:
- CD3DX12_ROOT_PARAMETER
api_location:
- d3dx12.h
api_type:
- HeaderDef
ms.localizationpriority: low
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9099b0839b6b55676d5a8afdfb913948e70bbb7f
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/15/2021
ms.locfileid: "105713504"
---
# <a name="cd3dx12_root_parameter-structure"></a><span data-ttu-id="4d1a6-104">\_Структура корневого \_ параметра CD3DX12</span><span class="sxs-lookup"><span data-stu-id="4d1a6-104">CD3DX12\_ROOT\_PARAMETER structure</span></span>

<span data-ttu-id="4d1a6-105">Вспомогательная структура, позволяющая упростить инициализацию [**структуры \_ корневого \_ параметра D3D12**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_root_parameter) .</span><span class="sxs-lookup"><span data-stu-id="4d1a6-105">A helper structure to enable easy initialization of a [**D3D12\_ROOT\_PARAMETER**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_root_parameter) structure.</span></span>

## <a name="syntax"></a><span data-ttu-id="4d1a6-106">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="4d1a6-106">Syntax</span></span>


```C++
struct CD3DX12_ROOT_PARAMETER  : public D3D12_ROOT_PARAMETER{
       CD3DX12_ROOT_PARAMETER();
       explicit CD3DX12_ROOT_PARAMETER(const D3D12_ROOT_PARAMETER &o);
  void static inline InitAsDescriptorTable(D3D12_ROOT_PARAMETER &rootParam, UINT numDescriptorRanges, const D3D12_DESCRIPTOR_RANGE* pDescriptorRanges, D3D12_SHADER_VISIBILITY visibility = D3D12_SHADER_VISIBILITY_ALL);
  void static inline InitAsConstants(D3D12_ROOT_PARAMETER &rootParam, UINT num32BitValues, UINT shaderRegister, UINT registerSpace = 0, D3D12_SHADER_VISIBILITY visibility = D3D12_SHADER_VISIBILITY_ALL);
  void static inline InitAsConstantBufferView(D3D12_ROOT_PARAMETER &rootParam, UINT shaderRegister, UINT registerSpace = 0, D3D12_SHADER_VISIBILITY visibility = D3D12_SHADER_VISIBILITY_ALL);
  void static inline InitAsShaderResourceView(D3D12_ROOT_PARAMETER &rootParam, UINT shaderRegister, UINT registerSpace = 0, D3D12_SHADER_VISIBILITY visibility = D3D12_SHADER_VISIBILITY_ALL);
  void static inline InitAsUnorderedAccessView(D3D12_ROOT_PARAMETER &rootParam, UINT shaderRegister, UINT registerSpace = 0, D3D12_SHADER_VISIBILITY visibility = D3D12_SHADER_VISIBILITY_ALL);
  void inline InitAsDescriptorTable(UINT numDescriptorRanges, const D3D12_DESCRIPTOR_RANGE* pDescriptorRanges, D3D12_SHADER_VISIBILITY visibility = D3D12_SHADER_VISIBILITY_ALL);
  void inline InitAsConstants(UINT num32BitValues, UINT shaderRegister, UINT registerSpace = 0, D3D12_SHADER_VISIBILITY visibility = D3D12_SHADER_VISIBILITY_ALL);
  void inline InitAsConstantBufferView(UINT shaderRegister, UINT registerSpace = 0, D3D12_SHADER_VISIBILITY visibility = D3D12_SHADER_VISIBILITY_ALL);
  void inline InitAsShaderResourceView(UINT shaderRegister, UINT registerSpace = 0, D3D12_SHADER_VISIBILITY visibility = D3D12_SHADER_VISIBILITY_ALL);
  void inline InitAsUnorderedAccessView(UINT shaderRegister, UINT registerSpace = 0, D3D12_SHADER_VISIBILITY visibility = D3D12_SHADER_VISIBILITY_ALL);
};
```



## <a name="members"></a><span data-ttu-id="4d1a6-107">Члены</span><span class="sxs-lookup"><span data-stu-id="4d1a6-107">Members</span></span>

<dl> <dt>

<span data-ttu-id="4d1a6-108">**\_Параметр CD3DX12 root \_ ()**</span><span class="sxs-lookup"><span data-stu-id="4d1a6-108">**CD3DX12\_ROOT\_PARAMETER()**</span></span>
</dt> <dd>

<span data-ttu-id="4d1a6-109">Создает новый, неинициализированный экземпляр \_ параметра CD3DX12 root \_ .</span><span class="sxs-lookup"><span data-stu-id="4d1a6-109">Creates a new, uninitialized, instance of a CD3DX12\_ROOT\_PARAMETER.</span></span>

</dd> <dt>

<span data-ttu-id="4d1a6-110">**явный \_ параметр CD3DX12 root \_ (const D3D12 \_ корневой \_ параметр &o)**</span><span class="sxs-lookup"><span data-stu-id="4d1a6-110">**explicit CD3DX12\_ROOT\_PARAMETER(const D3D12\_ROOT\_PARAMETER &o)**</span></span>
</dt> <dd>

<span data-ttu-id="4d1a6-111">Создает новый экземпляр \_ корневого \_ параметра CD3DX12, инициализируемый с помощью содержимого другой структуры [**\_ корневого \_ параметра D3D12**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_root_parameter) .</span><span class="sxs-lookup"><span data-stu-id="4d1a6-111">Creates a new instance of a CD3DX12\_ROOT\_PARAMETER, initialized with the contents of another [**D3D12\_ROOT\_PARAMETER**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_root_parameter) structure.</span></span>

</dd> <dt>

<span data-ttu-id="4d1a6-112">**static Inline Инитасдескриптортабле (D3D12 \_ root \_ Parameter &РУТПАРАМ, uint нумдескрипторранжес, const D3D12 \_ , диапазон дескрипторов \_ \* пдескрипторранжес, D3D12 видимость \_ видимости шейдеров \_ = D3D12 \_ видимость шейдера \_ \_ )**</span><span class="sxs-lookup"><span data-stu-id="4d1a6-112">**static inline InitAsDescriptorTable(D3D12\_ROOT\_PARAMETER &rootParam, UINT numDescriptorRanges, const D3D12\_DESCRIPTOR\_RANGE\* pDescriptorRanges, D3D12\_SHADER\_VISIBILITY visibility = D3D12\_SHADER\_VISIBILITY\_ALL)**</span></span>
</dt> <dd>

<span data-ttu-id="4d1a6-113">Задает функцию, которая инициализирует следующие параметры:</span><span class="sxs-lookup"><span data-stu-id="4d1a6-113">Specifies a function that initializes the following parameters:</span></span>

<span data-ttu-id="4d1a6-114">[**D3D12 \_ \_Параметр ROOT**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_root_parameter) &рутпарам</span><span class="sxs-lookup"><span data-stu-id="4d1a6-114">[**D3D12\_ROOT\_PARAMETER**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_root_parameter) &rootParam</span></span>

<span data-ttu-id="4d1a6-115">UINT Нумдескрипторранжес</span><span class="sxs-lookup"><span data-stu-id="4d1a6-115">UINT numDescriptorRanges</span></span>

<span data-ttu-id="4d1a6-116">[**D3D12 \_ Пдескрипторранжес \_ диапазона дескрипторов**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_descriptor_range) \*</span><span class="sxs-lookup"><span data-stu-id="4d1a6-116">[**D3D12\_DESCRIPTOR\_RANGE**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_descriptor_range)\* pDescriptorRanges</span></span>

<span data-ttu-id="4d1a6-117">участие [**D3D12 \_ Видимость \_ видимости шейдера**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_shader_visibility) = D3D12 \_ \_ видимость шейдера \_</span><span class="sxs-lookup"><span data-stu-id="4d1a6-117">(opt) [**D3D12\_SHADER\_VISIBILITY**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_shader_visibility) visibility = D3D12\_SHADER\_VISIBILITY\_ALL</span></span>

</dd> <dt>

<span data-ttu-id="4d1a6-118">**static Inline Инитасконстантс (D3D12 \_ root \_ Parameter &РУТПАРАМ, uint NUM32BITVALUES, uint ШАДЕРРЕГИСТЕР, uint регистерспаце = 0, видимость D3D12 \_ шейдера видимости \_ = D3D12 \_ видимость шейдера \_ \_ )**</span><span class="sxs-lookup"><span data-stu-id="4d1a6-118">**static inline InitAsConstants(D3D12\_ROOT\_PARAMETER &rootParam, UINT num32BitValues, UINT shaderRegister, UINT registerSpace = 0, D3D12\_SHADER\_VISIBILITY visibility = D3D12\_SHADER\_VISIBILITY\_ALL)**</span></span>
</dt> <dd>

<span data-ttu-id="4d1a6-119">Задает функцию, которая инициализирует следующие параметры:</span><span class="sxs-lookup"><span data-stu-id="4d1a6-119">Specifies a function that initializes the following parameters:</span></span>

<span data-ttu-id="4d1a6-120">[**D3D12 \_ \_Параметр ROOT**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_root_parameter) &рутпарам</span><span class="sxs-lookup"><span data-stu-id="4d1a6-120">[**D3D12\_ROOT\_PARAMETER**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_root_parameter) &rootParam</span></span>

<span data-ttu-id="4d1a6-121">UINT num32BitValues</span><span class="sxs-lookup"><span data-stu-id="4d1a6-121">UINT num32BitValues</span></span>

<span data-ttu-id="4d1a6-122">UINT Шадеррегистер</span><span class="sxs-lookup"><span data-stu-id="4d1a6-122">UINT shaderRegister</span></span>

<span data-ttu-id="4d1a6-123">участие UINT Регистерспаце = 0</span><span class="sxs-lookup"><span data-stu-id="4d1a6-123">(opt) UINT registerSpace = 0</span></span>

<span data-ttu-id="4d1a6-124">участие [**D3D12 \_ Видимость \_ видимости шейдера**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_shader_visibility) = D3D12 \_ \_ видимость шейдера \_</span><span class="sxs-lookup"><span data-stu-id="4d1a6-124">(opt) [**D3D12\_SHADER\_VISIBILITY**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_shader_visibility) visibility = D3D12\_SHADER\_VISIBILITY\_ALL</span></span>

</dd> <dt>

<span data-ttu-id="4d1a6-125">**static Inline Инитасконстантбуффервиев (D3D12 \_ root, \_ параметр &РУТПАРАМ, uint ШАДЕРРЕГИСТЕР, uint регистерспаце = 0, D3D12 \_ ШЕЙДЕР видимость \_ = D3D12 \_ видимость шейдера \_ \_ )**</span><span class="sxs-lookup"><span data-stu-id="4d1a6-125">**static inline InitAsConstantBufferView(D3D12\_ROOT\_PARAMETER &rootParam, UINT shaderRegister, UINT registerSpace = 0, D3D12\_SHADER\_VISIBILITY visibility = D3D12\_SHADER\_VISIBILITY\_ALL)**</span></span>
</dt> <dd>

<span data-ttu-id="4d1a6-126">Задает функцию, которая инициализирует следующие параметры:</span><span class="sxs-lookup"><span data-stu-id="4d1a6-126">Specifies a function that initializes the following parameters:</span></span>

<span data-ttu-id="4d1a6-127">[**D3D12 \_ \_Параметр ROOT**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_root_parameter) &рутпарам</span><span class="sxs-lookup"><span data-stu-id="4d1a6-127">[**D3D12\_ROOT\_PARAMETER**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_root_parameter) &rootParam</span></span>

<span data-ttu-id="4d1a6-128">UINT Шадеррегистер</span><span class="sxs-lookup"><span data-stu-id="4d1a6-128">UINT shaderRegister</span></span>

<span data-ttu-id="4d1a6-129">участие UINT Регистерспаце = 0</span><span class="sxs-lookup"><span data-stu-id="4d1a6-129">(opt) UINT registerSpace = 0</span></span>

<span data-ttu-id="4d1a6-130">участие [**D3D12 \_ Видимость \_ видимости шейдера**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_shader_visibility) = D3D12 \_ \_ видимость шейдера \_</span><span class="sxs-lookup"><span data-stu-id="4d1a6-130">(opt) [**D3D12\_SHADER\_VISIBILITY**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_shader_visibility) visibility = D3D12\_SHADER\_VISIBILITY\_ALL</span></span>

</dd> <dt>

<span data-ttu-id="4d1a6-131">**static Inline Инитасшадерресаурцевиев (D3D12 \_ root, \_ параметр &РУТПАРАМ, uint ШАДЕРРЕГИСТЕР, uint регистерспаце = 0, D3D12 \_ ШЕЙДЕР видимость \_ = D3D12 \_ видимость шейдера \_ \_ )**</span><span class="sxs-lookup"><span data-stu-id="4d1a6-131">**static inline InitAsShaderResourceView(D3D12\_ROOT\_PARAMETER &rootParam, UINT shaderRegister, UINT registerSpace = 0, D3D12\_SHADER\_VISIBILITY visibility = D3D12\_SHADER\_VISIBILITY\_ALL)**</span></span>
</dt> <dd>

<span data-ttu-id="4d1a6-132">Задает функцию, которая инициализирует следующие параметры:</span><span class="sxs-lookup"><span data-stu-id="4d1a6-132">Specifies a function that initializes the following parameters:</span></span>

<span data-ttu-id="4d1a6-133">[**D3D12 \_ \_Параметр ROOT**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_root_parameter) &рутпарам</span><span class="sxs-lookup"><span data-stu-id="4d1a6-133">[**D3D12\_ROOT\_PARAMETER**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_root_parameter) &rootParam</span></span>

<span data-ttu-id="4d1a6-134">UINT Шадеррегистер</span><span class="sxs-lookup"><span data-stu-id="4d1a6-134">UINT shaderRegister</span></span>

<span data-ttu-id="4d1a6-135">участие UINT Регистерспаце = 0</span><span class="sxs-lookup"><span data-stu-id="4d1a6-135">(opt) UINT registerSpace = 0</span></span>

<span data-ttu-id="4d1a6-136">участие [**D3D12 \_ Видимость \_ видимости шейдера**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_shader_visibility) = D3D12 \_ \_ видимость шейдера \_</span><span class="sxs-lookup"><span data-stu-id="4d1a6-136">(opt) [**D3D12\_SHADER\_VISIBILITY**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_shader_visibility) visibility = D3D12\_SHADER\_VISIBILITY\_ALL</span></span>

</dd> <dt>

<span data-ttu-id="4d1a6-137">**static Inline Инитасунордередакцессвиев (D3D12 \_ root, \_ параметр &РУТПАРАМ, uint ШАДЕРРЕГИСТЕР, uint регистерспаце = 0, D3D12 \_ ШЕЙДЕР видимость \_ = D3D12 \_ видимость шейдера \_ \_ )**</span><span class="sxs-lookup"><span data-stu-id="4d1a6-137">**static inline InitAsUnorderedAccessView(D3D12\_ROOT\_PARAMETER &rootParam, UINT shaderRegister, UINT registerSpace = 0, D3D12\_SHADER\_VISIBILITY visibility = D3D12\_SHADER\_VISIBILITY\_ALL)**</span></span>
</dt> <dd>

<span data-ttu-id="4d1a6-138">Задает функцию, которая инициализирует следующие параметры:</span><span class="sxs-lookup"><span data-stu-id="4d1a6-138">Specifies a function that initializes the following parameters:</span></span>

<span data-ttu-id="4d1a6-139">[**D3D12 \_ \_Параметр ROOT**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_root_parameter) &рутпарам</span><span class="sxs-lookup"><span data-stu-id="4d1a6-139">[**D3D12\_ROOT\_PARAMETER**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_root_parameter) &rootParam</span></span>

<span data-ttu-id="4d1a6-140">UINT Шадеррегистер</span><span class="sxs-lookup"><span data-stu-id="4d1a6-140">UINT shaderRegister</span></span>

<span data-ttu-id="4d1a6-141">участие UINT Регистерспаце = 0</span><span class="sxs-lookup"><span data-stu-id="4d1a6-141">(opt) UINT registerSpace = 0</span></span>

<span data-ttu-id="4d1a6-142">участие [**D3D12 \_ Видимость \_ видимости шейдера**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_shader_visibility) = D3D12 \_ \_ видимость шейдера \_</span><span class="sxs-lookup"><span data-stu-id="4d1a6-142">(opt) [**D3D12\_SHADER\_VISIBILITY**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_shader_visibility) visibility = D3D12\_SHADER\_VISIBILITY\_ALL</span></span>

</dd> <dt>

<span data-ttu-id="4d1a6-143">**Inline Инитасдескриптортабле (UINT Нумдескрипторранжес, const D3D12 \_ \_ диапазон дескрипторов \* ПДЕСКРИПТОРРАНЖЕС, \_ видимость D3D12 шейдера видимости \_ = D3D12 \_ \_ видимость шейдера \_ )**</span><span class="sxs-lookup"><span data-stu-id="4d1a6-143">**inline InitAsDescriptorTable(UINT numDescriptorRanges, const D3D12\_DESCRIPTOR\_RANGE\* pDescriptorRanges, D3D12\_SHADER\_VISIBILITY visibility = D3D12\_SHADER\_VISIBILITY\_ALL)**</span></span>
</dt> <dd>

<span data-ttu-id="4d1a6-144">Задает функцию, которая инициализирует следующие параметры:</span><span class="sxs-lookup"><span data-stu-id="4d1a6-144">Specifies a function that initializes the following parameters:</span></span>

<span data-ttu-id="4d1a6-145">UINT Нумдескрипторранжес</span><span class="sxs-lookup"><span data-stu-id="4d1a6-145">UINT numDescriptorRanges</span></span>

<span data-ttu-id="4d1a6-146">[**D3D12 \_ Пдескрипторранжес \_ диапазона дескрипторов**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_descriptor_range) \*</span><span class="sxs-lookup"><span data-stu-id="4d1a6-146">[**D3D12\_DESCRIPTOR\_RANGE**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_descriptor_range)\* pDescriptorRanges</span></span>

<span data-ttu-id="4d1a6-147">участие [**D3D12 \_ Видимость \_ видимости шейдера**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_shader_visibility) = D3D12 \_ \_ видимость шейдера \_</span><span class="sxs-lookup"><span data-stu-id="4d1a6-147">(opt) [**D3D12\_SHADER\_VISIBILITY**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_shader_visibility) visibility = D3D12\_SHADER\_VISIBILITY\_ALL</span></span>

</dd> <dt>

<span data-ttu-id="4d1a6-148">**Inline Инитасконстантс (UINT num32BitValues, UINT Шадеррегистер, UINT Регистерспаце = 0, видимость D3D12 \_ шейдер видимости \_ = D3D12 \_ видимость шейдера \_ \_ )**</span><span class="sxs-lookup"><span data-stu-id="4d1a6-148">**inline InitAsConstants(UINT num32BitValues, UINT shaderRegister, UINT registerSpace = 0, D3D12\_SHADER\_VISIBILITY visibility = D3D12\_SHADER\_VISIBILITY\_ALL)**</span></span>
</dt> <dd>

<span data-ttu-id="4d1a6-149">Задает функцию, которая инициализирует следующие параметры:</span><span class="sxs-lookup"><span data-stu-id="4d1a6-149">Specifies a function that initializes the following parameters:</span></span>

<span data-ttu-id="4d1a6-150">UINT num32BitValues</span><span class="sxs-lookup"><span data-stu-id="4d1a6-150">UINT num32BitValues</span></span>

<span data-ttu-id="4d1a6-151">UINT Шадеррегистер</span><span class="sxs-lookup"><span data-stu-id="4d1a6-151">UINT shaderRegister</span></span>

<span data-ttu-id="4d1a6-152">участие UINT Регистерспаце = 0</span><span class="sxs-lookup"><span data-stu-id="4d1a6-152">(opt) UINT registerSpace = 0</span></span>

<span data-ttu-id="4d1a6-153">участие [**D3D12 \_ Видимость \_ видимости шейдера**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_shader_visibility) = D3D12 \_ \_ видимость шейдера \_</span><span class="sxs-lookup"><span data-stu-id="4d1a6-153">(opt) [**D3D12\_SHADER\_VISIBILITY**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_shader_visibility) visibility = D3D12\_SHADER\_VISIBILITY\_ALL</span></span>

</dd> <dt>

<span data-ttu-id="4d1a6-154">**Inline Инитасконстантбуффервиев (UINT Шадеррегистер, UINT Регистерспаце = 0, D3D12 видимость \_ видимости шейдера \_ = D3D12 \_ видимость шейдера \_ \_ )**</span><span class="sxs-lookup"><span data-stu-id="4d1a6-154">**inline InitAsConstantBufferView(UINT shaderRegister, UINT registerSpace = 0, D3D12\_SHADER\_VISIBILITY visibility = D3D12\_SHADER\_VISIBILITY\_ALL)**</span></span>
</dt> <dd>

<span data-ttu-id="4d1a6-155">Задает функцию, которая инициализирует следующие параметры:</span><span class="sxs-lookup"><span data-stu-id="4d1a6-155">Specifies a function that initializes the following parameters:</span></span>

<span data-ttu-id="4d1a6-156">UINT Шадеррегистер</span><span class="sxs-lookup"><span data-stu-id="4d1a6-156">UINT shaderRegister</span></span>

<span data-ttu-id="4d1a6-157">участие UINT Регистерспаце = 0</span><span class="sxs-lookup"><span data-stu-id="4d1a6-157">(opt) UINT registerSpace = 0</span></span>

<span data-ttu-id="4d1a6-158">участие [**D3D12 \_ Видимость \_ видимости шейдера**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_shader_visibility) = D3D12 \_ \_ видимость шейдера \_</span><span class="sxs-lookup"><span data-stu-id="4d1a6-158">(opt) [**D3D12\_SHADER\_VISIBILITY**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_shader_visibility) visibility = D3D12\_SHADER\_VISIBILITY\_ALL</span></span>

</dd> <dt>

<span data-ttu-id="4d1a6-159">**Inline Инитасшадерресаурцевиев (UINT Шадеррегистер, UINT Регистерспаце = 0, D3D12 видимость \_ видимости шейдера \_ = D3D12 \_ видимость шейдера \_ \_ )**</span><span class="sxs-lookup"><span data-stu-id="4d1a6-159">**inline InitAsShaderResourceView(UINT shaderRegister, UINT registerSpace = 0, D3D12\_SHADER\_VISIBILITY visibility = D3D12\_SHADER\_VISIBILITY\_ALL)**</span></span>
</dt> <dd>

<span data-ttu-id="4d1a6-160">Задает функцию, которая инициализирует следующие параметры:</span><span class="sxs-lookup"><span data-stu-id="4d1a6-160">Specifies a function that initializes the following parameters:</span></span>

<span data-ttu-id="4d1a6-161">UINT Шадеррегистер</span><span class="sxs-lookup"><span data-stu-id="4d1a6-161">UINT shaderRegister</span></span>

<span data-ttu-id="4d1a6-162">участие UINT Регистерспаце = 0</span><span class="sxs-lookup"><span data-stu-id="4d1a6-162">(opt) UINT registerSpace = 0</span></span>

<span data-ttu-id="4d1a6-163">участие [**D3D12 \_ Видимость \_ видимости шейдера**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_shader_visibility) = D3D12 \_ \_ видимость шейдера \_</span><span class="sxs-lookup"><span data-stu-id="4d1a6-163">(opt) [**D3D12\_SHADER\_VISIBILITY**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_shader_visibility) visibility = D3D12\_SHADER\_VISIBILITY\_ALL</span></span>

</dd> <dt>

<span data-ttu-id="4d1a6-164">**Inline Инитасунордередакцессвиев (UINT Шадеррегистер, UINT Регистерспаце = 0, D3D12 видимость \_ видимости шейдера \_ = D3D12 \_ видимость шейдера \_ \_ )**</span><span class="sxs-lookup"><span data-stu-id="4d1a6-164">**inline InitAsUnorderedAccessView(UINT shaderRegister, UINT registerSpace = 0, D3D12\_SHADER\_VISIBILITY visibility = D3D12\_SHADER\_VISIBILITY\_ALL)**</span></span>
</dt> <dd>

<span data-ttu-id="4d1a6-165">Задает функцию, которая инициализирует следующие параметры:</span><span class="sxs-lookup"><span data-stu-id="4d1a6-165">Specifies a function that initializes the following parameters:</span></span>

<span data-ttu-id="4d1a6-166">UINT Шадеррегистер</span><span class="sxs-lookup"><span data-stu-id="4d1a6-166">UINT shaderRegister</span></span>

<span data-ttu-id="4d1a6-167">участие UINT Регистерспаце = 0</span><span class="sxs-lookup"><span data-stu-id="4d1a6-167">(opt) UINT registerSpace = 0</span></span>

<span data-ttu-id="4d1a6-168">участие [**D3D12 \_ Видимость \_ видимости шейдера**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_shader_visibility) = D3D12 \_ \_ видимость шейдера \_</span><span class="sxs-lookup"><span data-stu-id="4d1a6-168">(opt) [**D3D12\_SHADER\_VISIBILITY**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_shader_visibility) visibility = D3D12\_SHADER\_VISIBILITY\_ALL</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="4d1a6-169">Требования</span><span class="sxs-lookup"><span data-stu-id="4d1a6-169">Requirements</span></span>



| <span data-ttu-id="4d1a6-170">Требование</span><span class="sxs-lookup"><span data-stu-id="4d1a6-170">Requirement</span></span> | <span data-ttu-id="4d1a6-171">Значение</span><span class="sxs-lookup"><span data-stu-id="4d1a6-171">Value</span></span> |
|-------------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="4d1a6-172">Header</span><span class="sxs-lookup"><span data-stu-id="4d1a6-172">Header</span></span><br/> | <dl> <span data-ttu-id="4d1a6-173"><dt>D3dx12. h</dt></span><span class="sxs-lookup"><span data-stu-id="4d1a6-173"><dt>D3dx12.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="4d1a6-174">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="4d1a6-174">See also</span></span>

<dl> <dt>

[<span data-ttu-id="4d1a6-175">**\_Корневой \_ параметр D3D12**</span><span class="sxs-lookup"><span data-stu-id="4d1a6-175">**D3D12\_ROOT\_PARAMETER**</span></span>](/windows/desktop/api/d3d12/ns-d3d12-d3d12_root_parameter)
</dt> <dt>

[<span data-ttu-id="4d1a6-176">Вспомогательные структуры для D3D12</span><span class="sxs-lookup"><span data-stu-id="4d1a6-176">Helper Structures for D3D12</span></span>](helper-structures-for-d3d12.md)
</dt> </dl>

 

 





