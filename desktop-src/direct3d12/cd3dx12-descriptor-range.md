---
title: Структура CD3DX12_DESCRIPTOR_RANGE (D3dx12. h)
description: Вспомогательная структура, позволяющая упростить инициализацию \_ структуры диапазона дескрипторов D3D12 \_ .
ms.assetid: F066ECA5-5E52-4483-B773-B43C5F12809B
keywords:
- Структура CD3DX12_DESCRIPTOR_RANGE
topic_type:
- apiref
api_name:
- CD3DX12_DESCRIPTOR_RANGE
api_location:
- d3dx12.h
api_type:
- HeaderDef
ms.localizationpriority: low
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b511af1766daaefa7f92d33b71841b3a69c99927
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/15/2021
ms.locfileid: "105647816"
---
# <a name="cd3dx12_descriptor_range-structure"></a><span data-ttu-id="5213c-104">\_Структура диапазона дескрипторов CD3DX12 \_</span><span class="sxs-lookup"><span data-stu-id="5213c-104">CD3DX12\_DESCRIPTOR\_RANGE structure</span></span>

<span data-ttu-id="5213c-105">Вспомогательная структура, позволяющая упростить инициализацию [**структуры \_ \_ диапазона дескрипторов D3D12**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_descriptor_range) .</span><span class="sxs-lookup"><span data-stu-id="5213c-105">A helper structure to enable easy initialization of a [**D3D12\_DESCRIPTOR\_RANGE**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_descriptor_range) structure.</span></span>

## <a name="syntax"></a><span data-ttu-id="5213c-106">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="5213c-106">Syntax</span></span>


```C++
struct CD3DX12_DESCRIPTOR_RANGE  : public D3D12_DESCRIPTOR_RANGE{
       CD3DX12_DESCRIPTOR_RANGE();
       explicit CD3DX12_DESCRIPTOR_RANGE(const D3D12_DESCRIPTOR_RANGE &o);
       CD3DX12_DESCRIPTOR_RANGE(D3D12_DESCRIPTOR_RANGE_TYPE rangeType, UINT numDescriptors, UINT baseShaderRegister, UINT registerSpace = 0, UINT offsetInDescriptorsFromTableStart = D3D12_DESCRIPTOR_RANGE_OFFSET_APPEND);
  void inline Init(D3D12_DESCRIPTOR_RANGE_TYPE rangeType, UINT numDescriptors, UINT baseShaderRegister, UINT registerSpace = 0, UINT offsetInDescriptorsFromTableStart = D3D12_DESCRIPTOR_RANGE_OFFSET_APPEND);
  void static inline Init(D3D12_DESCRIPTOR_RANGE &range, D3D12_DESCRIPTOR_RANGE_TYPE rangeType, UINT numDescriptors, UINT baseShaderRegister, UINT registerSpace = 0, UINT offsetInDescriptorsFromTableStart = D3D12_DESCRIPTOR_RANGE_OFFSET_APPEND);
};
```



## <a name="members"></a><span data-ttu-id="5213c-107">Члены</span><span class="sxs-lookup"><span data-stu-id="5213c-107">Members</span></span>

<dl> <dt>

<span data-ttu-id="5213c-108">**\_Диапазон дескрипторов CD3DX12 \_ ()**</span><span class="sxs-lookup"><span data-stu-id="5213c-108">**CD3DX12\_DESCRIPTOR\_RANGE()**</span></span>
</dt> <dd>

<span data-ttu-id="5213c-109">Создает новый, неинициализированный экземпляр \_ диапазона дескрипторов D3DX12 \_ .</span><span class="sxs-lookup"><span data-stu-id="5213c-109">Creates a new, uninitialized, instance of a D3DX12\_DESCRIPTOR\_RANGE.</span></span>

</dd> <dt>

<span data-ttu-id="5213c-110">**явный \_ диапазон дескрипторов CD3DX12 \_ (константный \_ диапазон дескрипторов D3D12 \_ &o)**</span><span class="sxs-lookup"><span data-stu-id="5213c-110">**explicit CD3DX12\_DESCRIPTOR\_RANGE(const D3D12\_DESCRIPTOR\_RANGE &o)**</span></span>
</dt> <dd>

<span data-ttu-id="5213c-111">Создает новый экземпляр \_ диапазона дескрипторов D3DX12 \_ , инициализируемый с помощью содержимого другой структуры [**\_ \_ диапазона дескрипторов D3D12**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_descriptor_range) .</span><span class="sxs-lookup"><span data-stu-id="5213c-111">Creates a new instance of a D3DX12\_DESCRIPTOR\_RANGE, initialized with the contents of another [**D3D12\_DESCRIPTOR\_RANGE**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_descriptor_range) structure.</span></span>

</dd> <dt>

<span data-ttu-id="5213c-112">**\_Диапазон дескрипторов CD3DX12 \_ ( \_ тип диапазона дескрипторов D3D12 \_ \_ ранжетипе, uint НУМДЕСКРИПТОРС, uint басешадеррегистер, UINT Регистерспаце = 0, uint оффсетиндескрипторсфромтаблестарт = D3D12, \_ \_ Добавление смещения диапазона дескрипторов \_ \_ )**</span><span class="sxs-lookup"><span data-stu-id="5213c-112">**CD3DX12\_DESCRIPTOR\_RANGE(D3D12\_DESCRIPTOR\_RANGE\_TYPE rangeType, UINT numDescriptors, UINT baseShaderRegister, UINT registerSpace = 0, UINT offsetInDescriptorsFromTableStart = D3D12\_DESCRIPTOR\_RANGE\_OFFSET\_APPEND)**</span></span>
</dt> <dd>

<span data-ttu-id="5213c-113">Создает новый экземпляр \_ диапазона дескрипторов D3DX12 \_ , инициализируя следующие параметры:</span><span class="sxs-lookup"><span data-stu-id="5213c-113">Creates a new instance of a D3DX12\_DESCRIPTOR\_RANGE, initializing the following parameters:</span></span>

<span data-ttu-id="5213c-114">[**D3D12 \_ Ранжетипе \_ \_ тип диапазона дескрипторов**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_descriptor_range_type)</span><span class="sxs-lookup"><span data-stu-id="5213c-114">[**D3D12\_DESCRIPTOR\_RANGE\_TYPE**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_descriptor_range_type) rangeType</span></span>

<span data-ttu-id="5213c-115">UINT Нумдескрипторс</span><span class="sxs-lookup"><span data-stu-id="5213c-115">UINT numDescriptors</span></span>

<span data-ttu-id="5213c-116">UINT Басешадеррегистер</span><span class="sxs-lookup"><span data-stu-id="5213c-116">UINT baseShaderRegister</span></span>

<span data-ttu-id="5213c-117">UINT Регистерспаце = 0</span><span class="sxs-lookup"><span data-stu-id="5213c-117">UINT registerSpace = 0</span></span>

<span data-ttu-id="5213c-118">UINT Оффсетиндескрипторсфромтаблестарт = \_ \_ \_ Добавление смещения диапазона дескрипторов D3D12 \_</span><span class="sxs-lookup"><span data-stu-id="5213c-118">UINT offsetInDescriptorsFromTableStart = D3D12\_DESCRIPTOR\_RANGE\_OFFSET\_APPEND</span></span>

</dd> <dt>

<span data-ttu-id="5213c-119">**Inline init (D3D12- \_ \_ тип диапазона дескрипторов \_ Ранжетипе, UINT Нумдескрипторс, UINT Басешадеррегистер, uint регистерспаце = 0, uint оффсетиндескрипторсфромтаблестарт = D3D12, \_ \_ Добавление смещения диапазона дескрипторов \_ \_ )**</span><span class="sxs-lookup"><span data-stu-id="5213c-119">**inline Init(D3D12\_DESCRIPTOR\_RANGE\_TYPE rangeType, UINT numDescriptors, UINT baseShaderRegister, UINT registerSpace = 0, UINT offsetInDescriptorsFromTableStart = D3D12\_DESCRIPTOR\_RANGE\_OFFSET\_APPEND)**</span></span>
</dt> <dd>

<span data-ttu-id="5213c-120">Задает функцию, которая инициализирует следующие параметры:</span><span class="sxs-lookup"><span data-stu-id="5213c-120">Specifies a function that initializes the following parameters:</span></span>

<span data-ttu-id="5213c-121">[**D3D12 \_ Ранжетипе \_ \_ тип диапазона дескрипторов**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_descriptor_range_type)</span><span class="sxs-lookup"><span data-stu-id="5213c-121">[**D3D12\_DESCRIPTOR\_RANGE\_TYPE**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_descriptor_range_type) rangeType</span></span>

<span data-ttu-id="5213c-122">UINT Нумдескрипторс</span><span class="sxs-lookup"><span data-stu-id="5213c-122">UINT numDescriptors</span></span>

<span data-ttu-id="5213c-123">UINT Басешадеррегистер</span><span class="sxs-lookup"><span data-stu-id="5213c-123">UINT baseShaderRegister</span></span>

<span data-ttu-id="5213c-124">UINT Регистерспаце = 0</span><span class="sxs-lookup"><span data-stu-id="5213c-124">UINT registerSpace = 0</span></span>

<span data-ttu-id="5213c-125">UINT Оффсетиндескрипторсфромтаблестарт = \_ \_ \_ Добавление смещения диапазона дескрипторов D3D12 \_</span><span class="sxs-lookup"><span data-stu-id="5213c-125">UINT offsetInDescriptorsFromTableStart = D3D12\_DESCRIPTOR\_RANGE\_OFFSET\_APPEND</span></span>

</dd> <dt>

<span data-ttu-id="5213c-126">**static Inline init (диапазон D3D12- \_ дескрипторов &, диапазон дескрипторов \_ D3D12, \_ \_ \_ тип РАНЖЕТИПЕ, uint НУМДЕСКРИПТОРС, uint басешадеррегистер, UINT Регистерспаце = 0, uint оффсетиндескрипторсфромтаблестарт = D3D12 \_ смещение диапазона дескрипторов ( \_ \_ \_ append))**</span><span class="sxs-lookup"><span data-stu-id="5213c-126">**static inline Init(D3D12\_DESCRIPTOR\_RANGE &range, D3D12\_DESCRIPTOR\_RANGE\_TYPE rangeType, UINT numDescriptors, UINT baseShaderRegister, UINT registerSpace = 0, UINT offsetInDescriptorsFromTableStart = D3D12\_DESCRIPTOR\_RANGE\_OFFSET\_APPEND)**</span></span>
</dt> <dd>

<span data-ttu-id="5213c-127">Задает функцию, которая инициализирует следующие параметры:</span><span class="sxs-lookup"><span data-stu-id="5213c-127">Specifies a function that initializes the following parameters:</span></span>

<span data-ttu-id="5213c-128">[**D3D12 \_ Диапазон \_ дескрипторов**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_descriptor_range) &диапазона</span><span class="sxs-lookup"><span data-stu-id="5213c-128">[**D3D12\_DESCRIPTOR\_RANGE**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_descriptor_range) &range</span></span>

<span data-ttu-id="5213c-129">[**D3D12 \_ Ранжетипе \_ \_ тип диапазона дескрипторов**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_descriptor_range_type)</span><span class="sxs-lookup"><span data-stu-id="5213c-129">[**D3D12\_DESCRIPTOR\_RANGE\_TYPE**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_descriptor_range_type) rangeType</span></span>

<span data-ttu-id="5213c-130">UINT Нумдескрипторс</span><span class="sxs-lookup"><span data-stu-id="5213c-130">UINT numDescriptors</span></span>

<span data-ttu-id="5213c-131">UINT Басешадеррегистер</span><span class="sxs-lookup"><span data-stu-id="5213c-131">UINT baseShaderRegister</span></span>

<span data-ttu-id="5213c-132">UINT Регистерспаце = 0</span><span class="sxs-lookup"><span data-stu-id="5213c-132">UINT registerSpace = 0</span></span>

<span data-ttu-id="5213c-133">UINT Оффсетиндескрипторсфромтаблестарт = \_ \_ \_ Добавление смещения диапазона дескрипторов D3D12 \_</span><span class="sxs-lookup"><span data-stu-id="5213c-133">UINT offsetInDescriptorsFromTableStart = D3D12\_DESCRIPTOR\_RANGE\_OFFSET\_APPEND</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="5213c-134">Требования</span><span class="sxs-lookup"><span data-stu-id="5213c-134">Requirements</span></span>



| <span data-ttu-id="5213c-135">Требование</span><span class="sxs-lookup"><span data-stu-id="5213c-135">Requirement</span></span> | <span data-ttu-id="5213c-136">Значение</span><span class="sxs-lookup"><span data-stu-id="5213c-136">Value</span></span> |
|-------------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="5213c-137">Header</span><span class="sxs-lookup"><span data-stu-id="5213c-137">Header</span></span><br/> | <dl> <span data-ttu-id="5213c-138"><dt>D3dx12. h</dt></span><span class="sxs-lookup"><span data-stu-id="5213c-138"><dt>D3dx12.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="5213c-139">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="5213c-139">See also</span></span>

<dl> <dt>

[<span data-ttu-id="5213c-140">**\_Диапазон дескрипторов D3D12 \_**</span><span class="sxs-lookup"><span data-stu-id="5213c-140">**D3D12\_DESCRIPTOR\_RANGE**</span></span>](/windows/desktop/api/d3d12/ns-d3d12-d3d12_descriptor_range)
</dt> <dt>

[<span data-ttu-id="5213c-141">Вспомогательные структуры для D3D12</span><span class="sxs-lookup"><span data-stu-id="5213c-141">Helper Structures for D3D12</span></span>](helper-structures-for-d3d12.md)
</dt> </dl>

 

 





