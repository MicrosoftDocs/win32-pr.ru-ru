---
title: Структура CD3DX12_ROOT_DESCRIPTOR_TABLE1 (D3dx12. h)
description: Вспомогательная структура, позволяющая упростить инициализацию \_ \_ структуры Table1 корневого дескриптора D3D12 \_ .
ms.assetid: 82AC1948-92AA-4A4D-B443-717E9BF3046D
keywords:
- Структура CD3DX12_ROOT_DESCRIPTOR_TABLE1
topic_type:
- apiref
api_name:
- CD3DX12_ROOT_DESCRIPTOR_TABLE1
api_location:
- d3dx12.h
api_type:
- HeaderDef
ms.localizationpriority: low
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5e3538e5e1e199fdb6f8c7473af4996ccd7b7f1f
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/15/2021
ms.locfileid: "105713974"
---
# <a name="cd3dx12_root_descriptor_table1-structure"></a><span data-ttu-id="0cc1f-104">\_ \_ Структура Table1 корневого ДЕСКРИПТОРа CD3DX12 \_</span><span class="sxs-lookup"><span data-stu-id="0cc1f-104">CD3DX12\_ROOT\_DESCRIPTOR\_TABLE1 structure</span></span>

<span data-ttu-id="0cc1f-105">Вспомогательная структура, позволяющая упростить инициализацию [**структуры \_ \_ \_ Table1 корневого дескриптора D3D12**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_root_descriptor_table1) .</span><span class="sxs-lookup"><span data-stu-id="0cc1f-105">A helper structure to enable easy initialization of a [**D3D12\_ROOT\_DESCRIPTOR\_TABLE1**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_root_descriptor_table1) structure.</span></span>

## <a name="syntax"></a><span data-ttu-id="0cc1f-106">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="0cc1f-106">Syntax</span></span>


```C++
struct CD3DX12_ROOT_DESCRIPTOR_TABLE1  : public D3D12_ROOT_DESCRIPTOR_TABLE1{
       CD3DX12_ROOT_DESCRIPTOR_TABLE1();
       explicit CD3DX12_ROOT_DESCRIPTOR_TABLE1(const D3D12_ROOT_DESCRIPTOR_TABLE1 &o);
       CD3DX12_ROOT_DESCRIPTOR_TABLE1(UINT numDescriptorRanges, const D3D12_DESCRIPTOR_RANGE1* _pDescriptorRanges);
  void inline Init(UINT numDescriptorRanges, const D3D12_DESCRIPTOR_RANGE1* _pDescriptorRanges);
  void static inline Init(D3D12_ROOT_DESCRIPTOR_TABLE1 &rootDescriptorTable, UINT numDescriptorRanges, const D3D12_DESCRIPTOR_RANGE1* _pDescriptorRanges);
};
```



## <a name="members"></a><span data-ttu-id="0cc1f-107">Члены</span><span class="sxs-lookup"><span data-stu-id="0cc1f-107">Members</span></span>

<dl> <dt>

<span data-ttu-id="0cc1f-108">**\_Корневой \_ дескриптор CD3DX12 \_ Table1 ()**</span><span class="sxs-lookup"><span data-stu-id="0cc1f-108">**CD3DX12\_ROOT\_DESCRIPTOR\_TABLE1()**</span></span>
</dt> <dd>

<span data-ttu-id="0cc1f-109">Создает новый, неинициализированный экземпляр CD3DX12 \_ корневого \_ дескриптора \_ Table1.</span><span class="sxs-lookup"><span data-stu-id="0cc1f-109">Creates a new, uninitialized, instance of a CD3DX12\_ROOT\_DESCRIPTOR\_TABLE1.</span></span>

</dd> <dt>

<span data-ttu-id="0cc1f-110">**явный CD3DX12 \_ корневого \_ дескриптора \_ Table1 (const D3D12 \_ root \_ дескриптора \_ Table1 &o)**</span><span class="sxs-lookup"><span data-stu-id="0cc1f-110">**explicit CD3DX12\_ROOT\_DESCRIPTOR\_TABLE1(const D3D12\_ROOT\_DESCRIPTOR\_TABLE1 &o)**</span></span>
</dt> <dd>

<span data-ttu-id="0cc1f-111">Создает новый экземпляр CD3DX12 \_ корневого \_ дескриптора \_ Table1, инициализированного с содержимым другой структуры [**D3D12 \_ корневого \_ дескриптора \_ Table1**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_root_descriptor_table1) .</span><span class="sxs-lookup"><span data-stu-id="0cc1f-111">Creates a new instance of a CD3DX12\_ROOT\_DESCRIPTOR\_TABLE1, initialized with the contents of another [**D3D12\_ROOT\_DESCRIPTOR\_TABLE1**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_root_descriptor_table1) structure.</span></span>

</dd> <dt>

<span data-ttu-id="0cc1f-112">**CD3DX12 \_ root \_ дескриптора \_ Table1 (uint НУМДЕСКРИПТОРРАНЖЕС, const D3D12 \_ дескриптор \_ высокое \* \_ пдескрипторранжес)**</span><span class="sxs-lookup"><span data-stu-id="0cc1f-112">**CD3DX12\_ROOT\_DESCRIPTOR\_TABLE1(UINT numDescriptorRanges, const D3D12\_DESCRIPTOR\_RANGE1\* \_pDescriptorRanges)**</span></span>
</dt> <dd>

<span data-ttu-id="0cc1f-113">Создает новый экземпляр CD3DX12 \_ корневого \_ дескриптора \_ Table1, инициализируя следующие параметры:</span><span class="sxs-lookup"><span data-stu-id="0cc1f-113">Creates a new instance of a CD3DX12\_ROOT\_DESCRIPTOR\_TABLE1, initializing the following parameters:</span></span>

<span data-ttu-id="0cc1f-114">UINT Нумдескрипторранжес</span><span class="sxs-lookup"><span data-stu-id="0cc1f-114">UINT numDescriptorRanges</span></span>

<span data-ttu-id="0cc1f-115">const [**D3D12 \_ дескриптор \_ высокое**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_descriptor_range1) \* \_ пдескрипторранжес</span><span class="sxs-lookup"><span data-stu-id="0cc1f-115">const [**D3D12\_DESCRIPTOR\_RANGE1**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_descriptor_range1)\* \_pDescriptorRanges</span></span>

</dd> <dt>

<span data-ttu-id="0cc1f-116">**Inline init (UINT Нумдескрипторранжес, const D3D12 \_ дескриптора \_ высокое \* \_ пдескрипторранжес)**</span><span class="sxs-lookup"><span data-stu-id="0cc1f-116">**inline Init(UINT numDescriptorRanges, const D3D12\_DESCRIPTOR\_RANGE1\* \_pDescriptorRanges)**</span></span>
</dt> <dd>

<span data-ttu-id="0cc1f-117">Задает функцию, которая инициализирует следующие параметры:</span><span class="sxs-lookup"><span data-stu-id="0cc1f-117">Specifies a function that initializes the following parameters:</span></span>

<span data-ttu-id="0cc1f-118">UINT Нумдескрипторранжес</span><span class="sxs-lookup"><span data-stu-id="0cc1f-118">UINT numDescriptorRanges</span></span>

<span data-ttu-id="0cc1f-119">const [**D3D12 \_ дескриптор \_ высокое**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_descriptor_range1) \* \_ пдескрипторранжес</span><span class="sxs-lookup"><span data-stu-id="0cc1f-119">const [**D3D12\_DESCRIPTOR\_RANGE1**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_descriptor_range1)\* \_pDescriptorRanges</span></span>

</dd> <dt>

<span data-ttu-id="0cc1f-120">**статический встроенный метод init (D3D12 \_ root \_ дескриптора \_ Table1 &Рутдескриптортабле, uint НУМДЕСКРИПТОРРАНЖЕС, const D3D12 \_ дескриптор \_ высокое \* \_ пдескрипторранжес)**</span><span class="sxs-lookup"><span data-stu-id="0cc1f-120">**static inline Init(D3D12\_ROOT\_DESCRIPTOR\_TABLE1 &rootDescriptorTable, UINT numDescriptorRanges, const D3D12\_DESCRIPTOR\_RANGE1\* \_pDescriptorRanges)**</span></span>
</dt> <dd>

<span data-ttu-id="0cc1f-121">Задает функцию, которая инициализирует следующие параметры:</span><span class="sxs-lookup"><span data-stu-id="0cc1f-121">Specifies a function that initializes the following parameters:</span></span>

<span data-ttu-id="0cc1f-122">[**D3D12 \_ КОРНЕВой \_ дескриптор \_ Table1**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_root_descriptor_table1) &рутдескриптортабле</span><span class="sxs-lookup"><span data-stu-id="0cc1f-122">[**D3D12\_ROOT\_DESCRIPTOR\_TABLE1**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_root_descriptor_table1) &rootDescriptorTable</span></span>

<span data-ttu-id="0cc1f-123">UINT Нумдескрипторранжес</span><span class="sxs-lookup"><span data-stu-id="0cc1f-123">UINT numDescriptorRanges</span></span>

<span data-ttu-id="0cc1f-124">const [**D3D12 \_ дескриптор \_ высокое**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_descriptor_range1) \* \_ пдескрипторранжес</span><span class="sxs-lookup"><span data-stu-id="0cc1f-124">const [**D3D12\_DESCRIPTOR\_RANGE1**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_descriptor_range1)\* \_pDescriptorRanges</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="0cc1f-125">Требования</span><span class="sxs-lookup"><span data-stu-id="0cc1f-125">Requirements</span></span>



| <span data-ttu-id="0cc1f-126">Требование</span><span class="sxs-lookup"><span data-stu-id="0cc1f-126">Requirement</span></span> | <span data-ttu-id="0cc1f-127">Значение</span><span class="sxs-lookup"><span data-stu-id="0cc1f-127">Value</span></span> |
|-------------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="0cc1f-128">Header</span><span class="sxs-lookup"><span data-stu-id="0cc1f-128">Header</span></span><br/> | <dl> <span data-ttu-id="0cc1f-129"><dt>D3dx12. h</dt></span><span class="sxs-lookup"><span data-stu-id="0cc1f-129"><dt>D3dx12.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="0cc1f-130">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="0cc1f-130">See also</span></span>

<dl> <dt>

[<span data-ttu-id="0cc1f-131">**\_Корневой \_ дескриптор D3D12 \_ Таблица1**</span><span class="sxs-lookup"><span data-stu-id="0cc1f-131">**D3D12\_ROOT\_DESCRIPTOR\_TABLE1**</span></span>](/windows/desktop/api/d3d12/ns-d3d12-d3d12_root_descriptor_table1)
</dt> <dt>

[<span data-ttu-id="0cc1f-132">Вспомогательные структуры для D3D12</span><span class="sxs-lookup"><span data-stu-id="0cc1f-132">Helper Structures for D3D12</span></span>](helper-structures-for-d3d12.md)
</dt> </dl>

 

 





