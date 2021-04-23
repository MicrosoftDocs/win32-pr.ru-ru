---
title: Структура CD3DX12_ROOT_DESCRIPTOR_TABLE (D3dx12. h)
description: Вспомогательная структура, позволяющая упростить инициализацию \_ \_ структуры таблицы дескрипторов D3D12 root \_ .
ms.assetid: 154B4C50-4E94-471C-A44E-F120A84F007C
keywords:
- Структура CD3DX12_ROOT_DESCRIPTOR_TABLE
topic_type:
- apiref
api_name:
- CD3DX12_ROOT_DESCRIPTOR_TABLE
api_location:
- d3dx12.h
api_type:
- HeaderDef
ms.localizationpriority: low
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f675624526a959e6cf92172383b12590c36fc408
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/15/2021
ms.locfileid: "105713505"
---
# <a name="cd3dx12_root_descriptor_table-structure"></a><span data-ttu-id="c6522-104">\_ \_ Структура таблицы дескрипторов CD3DX12 root \_</span><span class="sxs-lookup"><span data-stu-id="c6522-104">CD3DX12\_ROOT\_DESCRIPTOR\_TABLE structure</span></span>

<span data-ttu-id="c6522-105">Вспомогательная структура, позволяющая упростить инициализацию [**структуры \_ \_ \_ таблицы дескрипторов D3D12 root**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_root_descriptor_table) .</span><span class="sxs-lookup"><span data-stu-id="c6522-105">A helper structure to enable easy initialization of a [**D3D12\_ROOT\_DESCRIPTOR\_TABLE**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_root_descriptor_table) structure.</span></span>

## <a name="syntax"></a><span data-ttu-id="c6522-106">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="c6522-106">Syntax</span></span>


```C++
struct CD3DX12_ROOT_DESCRIPTOR_TABLE  : public D3D12_ROOT_DESCRIPTOR_TABLE{
       CD3DX12_ROOT_DESCRIPTOR_TABLE();
       explicit CD3DX12_ROOT_DESCRIPTOR_TABLE(const D3D12_ROOT_DESCRIPTOR_TABLE &o);
       CD3DX12_ROOT_DESCRIPTOR_TABLE(UINT numDescriptorRanges, const D3D12_DESCRIPTOR_RANGE* _pDescriptorRanges);
  void inline Init(UINT numDescriptorRanges, const D3D12_DESCRIPTOR_RANGE* _pDescriptorRanges);
  void static inline Init(D3D12_ROOT_DESCRIPTOR_TABLE &rootDescriptorTable, UINT numDescriptorRanges, const D3D12_DESCRIPTOR_RANGE* _pDescriptorRanges);
};
```



## <a name="members"></a><span data-ttu-id="c6522-107">Члены</span><span class="sxs-lookup"><span data-stu-id="c6522-107">Members</span></span>

<dl> <dt>

<span data-ttu-id="c6522-108">**CD3DX12 \_ корневая \_ Таблица дескрипторов \_ ()**</span><span class="sxs-lookup"><span data-stu-id="c6522-108">**CD3DX12\_ROOT\_DESCRIPTOR\_TABLE()**</span></span>
</dt> <dd>

<span data-ttu-id="c6522-109">Создает новый, неинициализированный экземпляр \_ \_ таблицы дескриптора CD3DX12 root \_ .</span><span class="sxs-lookup"><span data-stu-id="c6522-109">Creates a new, uninitialized, instance of a CD3DX12\_ROOT\_DESCRIPTOR\_TABLE.</span></span>

</dd> <dt>

<span data-ttu-id="c6522-110">**явная CD3DX12 \_ корневая \_ Таблица дескрипторов \_ (const \_ D3D12 \_ Таблица дескрипторов корня \_ &o)**</span><span class="sxs-lookup"><span data-stu-id="c6522-110">**explicit CD3DX12\_ROOT\_DESCRIPTOR\_TABLE(const D3D12\_ROOT\_DESCRIPTOR\_TABLE &o)**</span></span>
</dt> <dd>

<span data-ttu-id="c6522-111">Создает новый экземпляр CD3DX12 \_ корневой \_ таблицы дескрипторов \_ , инициализируемый содержимым другой структуры [**\_ \_ \_ таблицы дескриптора root D3D12**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_root_descriptor_table) .</span><span class="sxs-lookup"><span data-stu-id="c6522-111">Creates a new instance of a CD3DX12\_ROOT\_DESCRIPTOR\_TABLE, initialized with the contents of another [**D3D12\_ROOT\_DESCRIPTOR\_TABLE**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_root_descriptor_table) structure.</span></span>

</dd> <dt>

<span data-ttu-id="c6522-112">**CD3DX12 \_ корневая \_ Таблица дескрипторов \_ (uint нумдескрипторранжес, константный \_ диапазон дескрипторов D3D12 \_ \* \_ пдескрипторранжес)**</span><span class="sxs-lookup"><span data-stu-id="c6522-112">**CD3DX12\_ROOT\_DESCRIPTOR\_TABLE(UINT numDescriptorRanges, const D3D12\_DESCRIPTOR\_RANGE\* \_pDescriptorRanges)**</span></span>
</dt> <dd>

<span data-ttu-id="c6522-113">Создает новый экземпляр CD3DX12 \_ корневой \_ таблицы дескрипторов \_ , инициализируя следующие параметры:</span><span class="sxs-lookup"><span data-stu-id="c6522-113">Creates a new instance of a CD3DX12\_ROOT\_DESCRIPTOR\_TABLE, initializing the following parameters:</span></span>

<span data-ttu-id="c6522-114">UINT Нумдескрипторранжес</span><span class="sxs-lookup"><span data-stu-id="c6522-114">UINT numDescriptorRanges</span></span>

<span data-ttu-id="c6522-115">[**D3D12 \_ Пдескрипторранжес \_ диапазона дескрипторов**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_descriptor_range) \* \_</span><span class="sxs-lookup"><span data-stu-id="c6522-115">[**D3D12\_DESCRIPTOR\_RANGE**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_descriptor_range)\* \_pDescriptorRanges</span></span>

</dd> <dt>

<span data-ttu-id="c6522-116">**Inline init (UINT Нумдескрипторранжес, const D3D12 \_ \_ диапазон дескрипторов \* \_ пдескрипторранжес)**</span><span class="sxs-lookup"><span data-stu-id="c6522-116">**inline Init(UINT numDescriptorRanges, const D3D12\_DESCRIPTOR\_RANGE\* \_pDescriptorRanges)**</span></span>
</dt> <dd>

<span data-ttu-id="c6522-117">Задает функцию, которая инициализирует следующие параметры:</span><span class="sxs-lookup"><span data-stu-id="c6522-117">Specifies a function that initializes the following parameters:</span></span>

<span data-ttu-id="c6522-118">UINT Нумдескрипторранжес</span><span class="sxs-lookup"><span data-stu-id="c6522-118">UINT numDescriptorRanges</span></span>

<span data-ttu-id="c6522-119">[**D3D12 \_ Пдескрипторранжес \_ диапазона дескрипторов**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_descriptor_range) \* \_</span><span class="sxs-lookup"><span data-stu-id="c6522-119">[**D3D12\_DESCRIPTOR\_RANGE**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_descriptor_range)\* \_pDescriptorRanges</span></span>

</dd> <dt>

<span data-ttu-id="c6522-120">**Статическая встроенная init (D3D12 \_ \_ , таблица дескрипторов root \_ &Рутдескриптортабле, uint НУМДЕСКРИПТОРРАНЖЕС, const D3D12 \_ диапазон дескрипторов \_ \* \_ пдескрипторранжес)**</span><span class="sxs-lookup"><span data-stu-id="c6522-120">**static inline Init(D3D12\_ROOT\_DESCRIPTOR\_TABLE &rootDescriptorTable, UINT numDescriptorRanges, const D3D12\_DESCRIPTOR\_RANGE\* \_pDescriptorRanges)**</span></span>
</dt> <dd>

<span data-ttu-id="c6522-121">Задает функцию, которая инициализирует следующие параметры:</span><span class="sxs-lookup"><span data-stu-id="c6522-121">Specifies a function that initializes the following parameters:</span></span>

<span data-ttu-id="c6522-122">[**D3D12 \_ \_ \_ Таблица дескрипторов root**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_root_descriptor_table) &рутдескриптортабле</span><span class="sxs-lookup"><span data-stu-id="c6522-122">[**D3D12\_ROOT\_DESCRIPTOR\_TABLE**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_root_descriptor_table) &rootDescriptorTable</span></span>

<span data-ttu-id="c6522-123">UINT Нумдескрипторранжес</span><span class="sxs-lookup"><span data-stu-id="c6522-123">UINT numDescriptorRanges</span></span>

<span data-ttu-id="c6522-124">[**D3D12 \_ Пдескрипторранжес \_ диапазона дескрипторов**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_descriptor_range) \* \_</span><span class="sxs-lookup"><span data-stu-id="c6522-124">[**D3D12\_DESCRIPTOR\_RANGE**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_descriptor_range)\* \_pDescriptorRanges</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="c6522-125">Требования</span><span class="sxs-lookup"><span data-stu-id="c6522-125">Requirements</span></span>



| <span data-ttu-id="c6522-126">Требование</span><span class="sxs-lookup"><span data-stu-id="c6522-126">Requirement</span></span> | <span data-ttu-id="c6522-127">Значение</span><span class="sxs-lookup"><span data-stu-id="c6522-127">Value</span></span> |
|-------------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="c6522-128">Header</span><span class="sxs-lookup"><span data-stu-id="c6522-128">Header</span></span><br/> | <dl> <span data-ttu-id="c6522-129"><dt>D3dx12. h</dt></span><span class="sxs-lookup"><span data-stu-id="c6522-129"><dt>D3dx12.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="c6522-130">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="c6522-130">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c6522-131">**D3D12 \_ корневая \_ Таблица дескрипторов \_**</span><span class="sxs-lookup"><span data-stu-id="c6522-131">**D3D12\_ROOT\_DESCRIPTOR\_TABLE**</span></span>](/windows/desktop/api/d3d12/ns-d3d12-d3d12_root_descriptor_table)
</dt> <dt>

[<span data-ttu-id="c6522-132">Вспомогательные структуры для D3D12</span><span class="sxs-lookup"><span data-stu-id="c6522-132">Helper Structures for D3D12</span></span>](helper-structures-for-d3d12.md)
</dt> </dl>

 

 





