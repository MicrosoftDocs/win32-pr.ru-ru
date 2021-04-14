---
title: Структура CD3DX12_DESCRIPTOR_RANGE1 (D3dx12. h)
description: Вспомогательная структура, позволяющая легко инициализировать \_ структуру высокое дескриптора D3D12 \_ .
ms.assetid: 9D073158-5907-4D1C-8D75-72B304277DAD
keywords:
- Структура CD3DX12_DESCRIPTOR_RANGE1
topic_type:
- apiref
api_name:
- CD3DX12_DESCRIPTOR_RANGE1
api_location:
- d3dx12.h
api_type:
- HeaderDef
ms.localizationpriority: low
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6386d8094d573fba9cd3af44b0148215ee621e2f
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/15/2021
ms.locfileid: "105647815"
---
# <a name="cd3dx12_descriptor_range1-structure"></a><span data-ttu-id="37e27-104">\_Структура высокое дескриптора CD3DX12 \_</span><span class="sxs-lookup"><span data-stu-id="37e27-104">CD3DX12\_DESCRIPTOR\_RANGE1 structure</span></span>

<span data-ttu-id="37e27-105">Вспомогательная структура, позволяющая легко инициализировать структуру [**\_ \_ высокое дескриптора D3D12**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_descriptor_range1) .</span><span class="sxs-lookup"><span data-stu-id="37e27-105">A helper structure to enable easy initialization of a [**D3D12\_DESCRIPTOR\_RANGE1**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_descriptor_range1) structure.</span></span>

## <a name="syntax"></a><span data-ttu-id="37e27-106">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="37e27-106">Syntax</span></span>


```C++
struct CD3DX12_DESCRIPTOR_RANGE1  : public D3D12_DESCRIPTOR_RANGE1{
       CD3DX12_DESCRIPTOR_RANGE1();
       explicit CD3DX12_DESCRIPTOR_RANGE1(const D3D12_DESCRIPTOR_RANGE1 &o);
       CD3DX12_DESCRIPTOR_RANGE1(D3D12_DESCRIPTOR_RANGE_TYPE rangeType, UINT numDescriptors, UINT baseShaderRegister, UINT registerSpace = 0, D3D12_DESCRIPTOR_RANGE_FLAGS flags = D3D12_DESCRIPTOR_RANGE_FLAG_NONE, UINT offsetInDescriptorsFromTableStart = D3D12_DESCRIPTOR_RANGE_OFFSET_APPEND);
  void inline Init(D3D12_DESCRIPTOR_RANGE_TYPE rangeType, UINT numDescriptors, UINT baseShaderRegister, UINT registerSpace = 0, D3D12_DESCRIPTOR_RANGE_FLAGS flags = D3D12_DESCRIPTOR_RANGE_FLAG_NONE, UINT offsetInDescriptorsFromTableStart = D3D12_DESCRIPTOR_RANGE_OFFSET_APPEND);
  void static inline Init(D3D12_DESCRIPTOR_RANGE1 &range, D3D12_DESCRIPTOR_RANGE_TYPE rangeType, UINT numDescriptors, UINT baseShaderRegister, UINT registerSpace = 0, D3D12_DESCRIPTOR_RANGE_FLAGS flags = D3D12_DESCRIPTOR_RANGE_FLAG_NONE, UINT offsetInDescriptorsFromTableStart = D3D12_DESCRIPTOR_RANGE_OFFSET_APPEND);
};
```



## <a name="members"></a><span data-ttu-id="37e27-107">Члены</span><span class="sxs-lookup"><span data-stu-id="37e27-107">Members</span></span>

<dl> <dt>

<span data-ttu-id="37e27-108">**\_Высокое дескриптора CD3DX12 \_ ()**</span><span class="sxs-lookup"><span data-stu-id="37e27-108">**CD3DX12\_DESCRIPTOR\_RANGE1()**</span></span>
</dt> <dd>

<span data-ttu-id="37e27-109">Создает новый, неинициализированный экземпляр CD3DX12 \_ дескриптора \_ высокое.</span><span class="sxs-lookup"><span data-stu-id="37e27-109">Creates a new, uninitialized, instance of a CD3DX12\_DESCRIPTOR\_RANGE1.</span></span>

</dd> <dt>

<span data-ttu-id="37e27-110">**явный \_ дескриптор CD3DX12 \_ высокое (const D3D12 \_ дескриптор \_ высокое &o)**</span><span class="sxs-lookup"><span data-stu-id="37e27-110">**explicit CD3DX12\_DESCRIPTOR\_RANGE1(const D3D12\_DESCRIPTOR\_RANGE1 &o)**</span></span>
</dt> <dd>

<span data-ttu-id="37e27-111">Создает новый экземпляр \_ дескриптора CD3DX12 \_ высокое, инициализируемый с помощью содержимого другой [**D3D12 \_ дескриптора \_ высокое**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_descriptor_range1) .</span><span class="sxs-lookup"><span data-stu-id="37e27-111">Creates a new instance of a CD3DX12\_DESCRIPTOR\_RANGE1, initialized with the contents of another [**D3D12\_DESCRIPTOR\_RANGE1**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_descriptor_range1) structure.</span></span>

</dd> <dt>

<span data-ttu-id="37e27-112">**CD3DX12 \_ дескриптор \_ высокое (D3D12 \_ - \_ диапазон дескрипторов \_ РАНЖЕТИПЕ, uint НУМДЕСКРИПТОРС, uint басешадеррегистер, uint регистерспаце = 0, флаги \_ ДИАПАЗОНов D3D12 дескрипторов \_ \_ : D3D12 \_ \_ \_ \_ \_ \_ \_ \_**</span><span class="sxs-lookup"><span data-stu-id="37e27-112">**CD3DX12\_DESCRIPTOR\_RANGE1(D3D12\_DESCRIPTOR\_RANGE\_TYPE rangeType, UINT numDescriptors, UINT baseShaderRegister, UINT registerSpace = 0, D3D12\_DESCRIPTOR\_RANGE\_FLAGS flags = D3D12\_DESCRIPTOR\_RANGE\_FLAG\_NONE, UINT offsetInDescriptorsFromTableStart = D3D12\_DESCRIPTOR\_RANGE\_OFFSET\_APPEND)**</span></span>
</dt> <dd>

<span data-ttu-id="37e27-113">Создает новый экземпляр \_ дескриптора CD3DX12 \_ высокое, инициализируя следующие параметры:</span><span class="sxs-lookup"><span data-stu-id="37e27-113">Creates a new instance of a CD3DX12\_DESCRIPTOR\_RANGE1, initializing the following parameters:</span></span>

<span data-ttu-id="37e27-114">[**D3D12 \_ Ранжетипе \_ \_ тип диапазона дескрипторов**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_descriptor_range_type)</span><span class="sxs-lookup"><span data-stu-id="37e27-114">[**D3D12\_DESCRIPTOR\_RANGE\_TYPE**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_descriptor_range_type) rangeType</span></span>

<span data-ttu-id="37e27-115">UINT Нумдескрипторс</span><span class="sxs-lookup"><span data-stu-id="37e27-115">UINT numDescriptors</span></span>

<span data-ttu-id="37e27-116">UINT Басешадеррегистер</span><span class="sxs-lookup"><span data-stu-id="37e27-116">UINT baseShaderRegister</span></span>

<span data-ttu-id="37e27-117">UINT Регистерспаце = 0</span><span class="sxs-lookup"><span data-stu-id="37e27-117">UINT registerSpace = 0</span></span>

<span data-ttu-id="37e27-118">[**D3D12 \_ Флаги флагов \_ \_ диапазона дескрипторов**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_descriptor_range_flags) = \_ \_ \_ значение флага диапазона дескрипторов D3D12 \_ None</span><span class="sxs-lookup"><span data-stu-id="37e27-118">[**D3D12\_DESCRIPTOR\_RANGE\_FLAGS**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_descriptor_range_flags) flags = D3D12\_DESCRIPTOR\_RANGE\_FLAG\_NONE</span></span>

<span data-ttu-id="37e27-119">UINT Оффсетиндескрипторсфромтаблестарт = \_ \_ \_ Добавление смещения диапазона дескрипторов D3D12 \_</span><span class="sxs-lookup"><span data-stu-id="37e27-119">UINT offsetInDescriptorsFromTableStart = D3D12\_DESCRIPTOR\_RANGE\_OFFSET\_APPEND</span></span>

</dd> <dt>

<span data-ttu-id="37e27-120">**Inline init (D3D12- \_ диапазон дескрипторов \_ \_ Ранжетипе, UINT Нумдескрипторс, UINT Басешадеррегистер, uint регистерспаце = 0, флаги \_ флагов диапазона дескрипторов D3D12 = " \_ \_ \_ \_ \_ \_ нет", uint D3D12 = \_ оффсетиндескрипторсфромтаблестарт \_ смещение диапазона дескрипторов ( \_ \_ append))**</span><span class="sxs-lookup"><span data-stu-id="37e27-120">**inline Init(D3D12\_DESCRIPTOR\_RANGE\_TYPE rangeType, UINT numDescriptors, UINT baseShaderRegister, UINT registerSpace = 0, D3D12\_DESCRIPTOR\_RANGE\_FLAGS flags = D3D12\_DESCRIPTOR\_RANGE\_FLAG\_NONE, UINT offsetInDescriptorsFromTableStart = D3D12\_DESCRIPTOR\_RANGE\_OFFSET\_APPEND)**</span></span>
</dt> <dd>

<span data-ttu-id="37e27-121">Задает функцию, которая инициализирует следующие параметры:</span><span class="sxs-lookup"><span data-stu-id="37e27-121">Specifies a function that initializes the following parameters:</span></span>

<span data-ttu-id="37e27-122">[**D3D12 \_ Ранжетипе \_ \_ тип диапазона дескрипторов**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_descriptor_range_type)</span><span class="sxs-lookup"><span data-stu-id="37e27-122">[**D3D12\_DESCRIPTOR\_RANGE\_TYPE**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_descriptor_range_type) rangeType</span></span>

<span data-ttu-id="37e27-123">UINT Нумдескрипторс</span><span class="sxs-lookup"><span data-stu-id="37e27-123">UINT numDescriptors</span></span>

<span data-ttu-id="37e27-124">UINT Басешадеррегистер</span><span class="sxs-lookup"><span data-stu-id="37e27-124">UINT baseShaderRegister</span></span>

<span data-ttu-id="37e27-125">UINT Регистерспаце = 0</span><span class="sxs-lookup"><span data-stu-id="37e27-125">UINT registerSpace = 0</span></span>

<span data-ttu-id="37e27-126">[**D3D12 \_ Флаги флагов \_ \_ диапазона дескрипторов**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_descriptor_range_flags) = \_ \_ \_ значение флага диапазона дескрипторов D3D12 \_ None</span><span class="sxs-lookup"><span data-stu-id="37e27-126">[**D3D12\_DESCRIPTOR\_RANGE\_FLAGS**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_descriptor_range_flags) flags = D3D12\_DESCRIPTOR\_RANGE\_FLAG\_NONE</span></span>

<span data-ttu-id="37e27-127">UINT Оффсетиндескрипторсфромтаблестарт = \_ \_ \_ Добавление смещения диапазона дескрипторов D3D12 \_</span><span class="sxs-lookup"><span data-stu-id="37e27-127">UINT offsetInDescriptorsFromTableStart = D3D12\_DESCRIPTOR\_RANGE\_OFFSET\_APPEND</span></span>

</dd> <dt>

<span data-ttu-id="37e27-128">**статический встроенный метод init (D3D12 \_ дескриптора \_ высокое &Range, \_ D3D12 \_ диапазоны дескрипторов \_ РАНЖЕТИПЕ, uint НУМДЕСКРИПТОРС, uint басешадеррегистер, uint регистерспаце = 0, D3D12 флагов \_ диапазона дескрипторов \_ \_ = D3D12 \_ \_ ФЛАГа диапазона дескрипторов \_ \_ None, uint оффсетиндескрипторсфромтаблестарт = D3D12, \_ \_ Добавление смещения диапазона дескрипторов \_ \_ )**</span><span class="sxs-lookup"><span data-stu-id="37e27-128">**static inline Init(D3D12\_DESCRIPTOR\_RANGE1 &range, D3D12\_DESCRIPTOR\_RANGE\_TYPE rangeType, UINT numDescriptors, UINT baseShaderRegister, UINT registerSpace = 0, D3D12\_DESCRIPTOR\_RANGE\_FLAGS flags = D3D12\_DESCRIPTOR\_RANGE\_FLAG\_NONE, UINT offsetInDescriptorsFromTableStart = D3D12\_DESCRIPTOR\_RANGE\_OFFSET\_APPEND)**</span></span>
</dt> <dd>

<span data-ttu-id="37e27-129">Задает функцию, которая инициализирует следующие параметры:</span><span class="sxs-lookup"><span data-stu-id="37e27-129">Specifies a function that initializes the following parameters:</span></span>

<span data-ttu-id="37e27-130">[**D3D12 \_ \_Высокое дескриптора**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_descriptor_range1) &диапазон</span><span class="sxs-lookup"><span data-stu-id="37e27-130">[**D3D12\_DESCRIPTOR\_RANGE1**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_descriptor_range1) &range</span></span>

<span data-ttu-id="37e27-131">[**D3D12 \_ Ранжетипе \_ \_ тип диапазона дескрипторов**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_descriptor_range_type)</span><span class="sxs-lookup"><span data-stu-id="37e27-131">[**D3D12\_DESCRIPTOR\_RANGE\_TYPE**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_descriptor_range_type) rangeType</span></span>

<span data-ttu-id="37e27-132">UINT Нумдескрипторс</span><span class="sxs-lookup"><span data-stu-id="37e27-132">UINT numDescriptors</span></span>

<span data-ttu-id="37e27-133">UINT Басешадеррегистер</span><span class="sxs-lookup"><span data-stu-id="37e27-133">UINT baseShaderRegister</span></span>

<span data-ttu-id="37e27-134">UINT Регистерспаце = 0</span><span class="sxs-lookup"><span data-stu-id="37e27-134">UINT registerSpace = 0</span></span>

<span data-ttu-id="37e27-135">[**D3D12 \_ Флаги флагов \_ \_ диапазона дескрипторов**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_descriptor_range_flags) = \_ \_ \_ значение флага диапазона дескрипторов D3D12 \_ None</span><span class="sxs-lookup"><span data-stu-id="37e27-135">[**D3D12\_DESCRIPTOR\_RANGE\_FLAGS**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_descriptor_range_flags) flags = D3D12\_DESCRIPTOR\_RANGE\_FLAG\_NONE</span></span>

<span data-ttu-id="37e27-136">UINT Оффсетиндескрипторсфромтаблестарт = \_ \_ \_ Добавление смещения диапазона дескрипторов D3D12 \_</span><span class="sxs-lookup"><span data-stu-id="37e27-136">UINT offsetInDescriptorsFromTableStart = D3D12\_DESCRIPTOR\_RANGE\_OFFSET\_APPEND</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="37e27-137">Требования</span><span class="sxs-lookup"><span data-stu-id="37e27-137">Requirements</span></span>



| <span data-ttu-id="37e27-138">Требование</span><span class="sxs-lookup"><span data-stu-id="37e27-138">Requirement</span></span> | <span data-ttu-id="37e27-139">Значение</span><span class="sxs-lookup"><span data-stu-id="37e27-139">Value</span></span> |
|-------------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="37e27-140">Header</span><span class="sxs-lookup"><span data-stu-id="37e27-140">Header</span></span><br/> | <dl> <span data-ttu-id="37e27-141"><dt>D3dx12. h</dt></span><span class="sxs-lookup"><span data-stu-id="37e27-141"><dt>D3dx12.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="37e27-142">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="37e27-142">See also</span></span>

<dl> <dt>

[<span data-ttu-id="37e27-143">**\_Высокое дескриптора D3D12 \_**</span><span class="sxs-lookup"><span data-stu-id="37e27-143">**D3D12\_DESCRIPTOR\_RANGE1**</span></span>](/windows/desktop/api/d3d12/ns-d3d12-d3d12_descriptor_range1)
</dt> <dt>

[<span data-ttu-id="37e27-144">Вспомогательные структуры для D3D12</span><span class="sxs-lookup"><span data-stu-id="37e27-144">Helper Structures for D3D12</span></span>](helper-structures-for-d3d12.md)
</dt> </dl>

 

 





