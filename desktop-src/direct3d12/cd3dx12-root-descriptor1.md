---
title: Структура CD3DX12_ROOT_DESCRIPTOR1 (D3dx12. h)
description: Вспомогательная структура, позволяющая легко инициализировать D3D12 \_ корневую \_ структуру DESCRIPTOR1.
ms.assetid: 664822BF-5C27-4541-953F-219894547A6C
keywords:
- Структура CD3DX12_ROOT_DESCRIPTOR1
topic_type:
- apiref
api_name:
- CD3DX12_ROOT_DESCRIPTOR1
api_location:
- d3dx12.h
api_type:
- HeaderDef
ms.localizationpriority: low
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 66cb64509c82c11180ca3e1d2937dff5d077897d
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/15/2021
ms.locfileid: "105713969"
---
# <a name="cd3dx12_root_descriptor1-structure"></a><span data-ttu-id="1fd1e-104">CD3DX12 \_ корневая \_ Структура DESCRIPTOR1</span><span class="sxs-lookup"><span data-stu-id="1fd1e-104">CD3DX12\_ROOT\_DESCRIPTOR1 structure</span></span>

<span data-ttu-id="1fd1e-105">Вспомогательная структура, позволяющая легко инициализировать [**D3D12 \_ корневую структуру \_ DESCRIPTOR1**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_root_descriptor1) .</span><span class="sxs-lookup"><span data-stu-id="1fd1e-105">A helper structure to enable easy initialization of a [**D3D12\_ROOT\_DESCRIPTOR1**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_root_descriptor1) structure.</span></span>

## <a name="syntax"></a><span data-ttu-id="1fd1e-106">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="1fd1e-106">Syntax</span></span>


```C++
struct CD3DX12_ROOT_DESCRIPTOR1  : public D3D12_ROOT_DESCRIPTOR1{
       CD3DX12_ROOT_DESCRIPTOR1();
       explicit CD3DX12_ROOT_DESCRIPTOR1(const D3D12_ROOT_DESCRIPTOR1 &o);
       CD3DX12_ROOT_DESCRIPTOR1(UINT shaderRegister, UINT registerSpace = 0, D3D12_ROOT_DESCRIPTOR_FLAGS flags = D3D12_ROOT_DESCRIPTOR_FLAG_NONE);
  void inline Init(UINT shaderRegister, UINT registerSpace = 0, D3D12_ROOT_DESCRIPTOR_FLAGS flags = D3D12_ROOT_DESCRIPTOR_FLAG_NONE);
  void static inline Init(D3D12_ROOT_DESCRIPTOR1 &table, UINT shaderRegister, UINT registerSpace = 0, D3D12_ROOT_DESCRIPTOR_FLAGS flags = D3D12_ROOT_DESCRIPTOR_FLAG_NONE);
};
```



## <a name="members"></a><span data-ttu-id="1fd1e-107">Члены</span><span class="sxs-lookup"><span data-stu-id="1fd1e-107">Members</span></span>

<dl> <dt>

<span data-ttu-id="1fd1e-108">**CD3DX12 \_ root \_ DESCRIPTOR1 ()**</span><span class="sxs-lookup"><span data-stu-id="1fd1e-108">**CD3DX12\_ROOT\_DESCRIPTOR1()**</span></span>
</dt> <dd>

<span data-ttu-id="1fd1e-109">Создает новый, неинициализированный экземпляр экземпляра CD3DX12 \_ root \_ DESCRIPTOR1.</span><span class="sxs-lookup"><span data-stu-id="1fd1e-109">Creates a new, uninitialized, instance of a CD3DX12\_ROOT\_DESCRIPTOR1.</span></span>

</dd> <dt>

<span data-ttu-id="1fd1e-110">**явное CD3DX12 \_ корневой \_ DESCRIPTOR1 (const D3D12 \_ root \_ DESCRIPTOR1 &o)**</span><span class="sxs-lookup"><span data-stu-id="1fd1e-110">**explicit CD3DX12\_ROOT\_DESCRIPTOR1(const D3D12\_ROOT\_DESCRIPTOR1 &o)**</span></span>
</dt> <dd>

<span data-ttu-id="1fd1e-111">Создает новый экземпляр CD3DX12 \_ root \_ DESCRIPTOR1, который инициализируется с содержимым другой [**D3D12 \_ корневой структуры \_ DESCRIPTOR1**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_root_descriptor1) .</span><span class="sxs-lookup"><span data-stu-id="1fd1e-111">Creates a new instance of a CD3DX12\_ROOT\_DESCRIPTOR1, initialized with the contents of another [**D3D12\_ROOT\_DESCRIPTOR1**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_root_descriptor1) structure.</span></span>

</dd> <dt>

<span data-ttu-id="1fd1e-112">**CD3DX12 \_ root \_ DESCRIPTOR1 (uint ШАДЕРРЕГИСТЕР, uint регистерспаце = 0, D3D12 флаги \_ \_ \_ flags root-дескриптора = D3D12 \_ корневой \_ \_ флага \_ None)**</span><span class="sxs-lookup"><span data-stu-id="1fd1e-112">**CD3DX12\_ROOT\_DESCRIPTOR1(UINT shaderRegister, UINT registerSpace = 0, D3D12\_ROOT\_DESCRIPTOR\_FLAGS flags = D3D12\_ROOT\_DESCRIPTOR\_FLAG\_NONE)**</span></span>
</dt> <dd>

<span data-ttu-id="1fd1e-113">Создает новый экземпляр CD3DX12 \_ root \_ DESCRIPTOR1, инициализируя следующие параметры:</span><span class="sxs-lookup"><span data-stu-id="1fd1e-113">Creates a new instance of a CD3DX12\_ROOT\_DESCRIPTOR1, initializing the following parameters:</span></span>

<span data-ttu-id="1fd1e-114">UINT Шадеррегистер</span><span class="sxs-lookup"><span data-stu-id="1fd1e-114">UINT shaderRegister</span></span>

<span data-ttu-id="1fd1e-115">UINT Регистерспаце = 0</span><span class="sxs-lookup"><span data-stu-id="1fd1e-115">UINT registerSpace = 0</span></span>

<span data-ttu-id="1fd1e-116">[**D3D12 \_ Флаги флагов КОРНЕВого \_ дескриптора \_**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_root_descriptor_flags) = D3D12 \_ корневого \_ дескриптора \_ \_ None</span><span class="sxs-lookup"><span data-stu-id="1fd1e-116">[**D3D12\_ROOT\_DESCRIPTOR\_FLAGS**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_root_descriptor_flags) flags = D3D12\_ROOT\_DESCRIPTOR\_FLAG\_NONE</span></span>

</dd> <dt>

<span data-ttu-id="1fd1e-117">**Inline init (UINT Шадеррегистер, UINT Регистерспаце = 0, D3D12 flags \_ root \_ дескриптора флаг \_ = D3D12 \_ корневого \_ дескриптора \_ \_ None)**</span><span class="sxs-lookup"><span data-stu-id="1fd1e-117">**inline Init(UINT shaderRegister, UINT registerSpace = 0, D3D12\_ROOT\_DESCRIPTOR\_FLAGS flags = D3D12\_ROOT\_DESCRIPTOR\_FLAG\_NONE)**</span></span>
</dt> <dd>

<span data-ttu-id="1fd1e-118">Задает функцию, которая инициализирует следующие параметры:</span><span class="sxs-lookup"><span data-stu-id="1fd1e-118">Specifies a function that initializes the following parameters:</span></span>

<span data-ttu-id="1fd1e-119">UINT Шадеррегистер</span><span class="sxs-lookup"><span data-stu-id="1fd1e-119">UINT shaderRegister</span></span>

<span data-ttu-id="1fd1e-120">UINT Регистерспаце = 0</span><span class="sxs-lookup"><span data-stu-id="1fd1e-120">UINT registerSpace = 0</span></span>

<span data-ttu-id="1fd1e-121">[**D3D12 \_ Флаги флагов КОРНЕВого \_ дескриптора \_**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_root_descriptor_flags) = D3D12 \_ корневого \_ дескриптора \_ \_ None</span><span class="sxs-lookup"><span data-stu-id="1fd1e-121">[**D3D12\_ROOT\_DESCRIPTOR\_FLAGS**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_root_descriptor_flags) flags = D3D12\_ROOT\_DESCRIPTOR\_FLAG\_NONE</span></span>

</dd> <dt>

<span data-ttu-id="1fd1e-122">**Статическая встроенная инициализация (D3D12 \_ root \_ DESCRIPTOR1 &таблица, uint ШАДЕРРЕГИСТЕР, uint регистерспаце = 0, D3D12 флаги \_ \_ битового дескриптора [- \_ D3D12 \_ корневого \_ дескриптора \_ \_ None)**</span><span class="sxs-lookup"><span data-stu-id="1fd1e-122">**static inline Init(D3D12\_ROOT\_DESCRIPTOR1 &table, UINT shaderRegister, UINT registerSpace = 0, D3D12\_ROOT\_DESCRIPTOR\_FLAGS flags = D3D12\_ROOT\_DESCRIPTOR\_FLAG\_NONE)**</span></span>
</dt> <dd>

<span data-ttu-id="1fd1e-123">Задает функцию, которая инициализирует следующие параметры:</span><span class="sxs-lookup"><span data-stu-id="1fd1e-123">Specifies a function that initializes the following parameters:</span></span>

<span data-ttu-id="1fd1e-124">[**D3D12 \_ Корневая \_ DESCRIPTOR1**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_root_descriptor1) &таблица</span><span class="sxs-lookup"><span data-stu-id="1fd1e-124">[**D3D12\_ROOT\_DESCRIPTOR1**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_root_descriptor1) &table</span></span>

<span data-ttu-id="1fd1e-125">UINT Шадеррегистер</span><span class="sxs-lookup"><span data-stu-id="1fd1e-125">UINT shaderRegister</span></span>

<span data-ttu-id="1fd1e-126">UINT Регистерспаце = 0</span><span class="sxs-lookup"><span data-stu-id="1fd1e-126">UINT registerSpace = 0</span></span>

<span data-ttu-id="1fd1e-127">[**D3D12 \_ Флаги флагов КОРНЕВого \_ дескриптора \_**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_root_descriptor_flags) = D3D12 \_ корневого \_ дескриптора \_ \_ None</span><span class="sxs-lookup"><span data-stu-id="1fd1e-127">[**D3D12\_ROOT\_DESCRIPTOR\_FLAGS**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_root_descriptor_flags) flags = D3D12\_ROOT\_DESCRIPTOR\_FLAG\_NONE</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="1fd1e-128">Требования</span><span class="sxs-lookup"><span data-stu-id="1fd1e-128">Requirements</span></span>



| <span data-ttu-id="1fd1e-129">Требование</span><span class="sxs-lookup"><span data-stu-id="1fd1e-129">Requirement</span></span> | <span data-ttu-id="1fd1e-130">Значение</span><span class="sxs-lookup"><span data-stu-id="1fd1e-130">Value</span></span> |
|-------------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="1fd1e-131">Header</span><span class="sxs-lookup"><span data-stu-id="1fd1e-131">Header</span></span><br/> | <dl> <span data-ttu-id="1fd1e-132"><dt>D3dx12. h</dt></span><span class="sxs-lookup"><span data-stu-id="1fd1e-132"><dt>D3dx12.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="1fd1e-133">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="1fd1e-133">See also</span></span>

<dl> <dt>

[<span data-ttu-id="1fd1e-134">**\_Корневой \_ DESCRIPTOR1 D3D12**</span><span class="sxs-lookup"><span data-stu-id="1fd1e-134">**D3D12\_ROOT\_DESCRIPTOR1**</span></span>](/windows/desktop/api/d3d12/ns-d3d12-d3d12_root_descriptor1)
</dt> <dt>

[<span data-ttu-id="1fd1e-135">Вспомогательные структуры для D3D12</span><span class="sxs-lookup"><span data-stu-id="1fd1e-135">Helper Structures for D3D12</span></span>](helper-structures-for-d3d12.md)
</dt> </dl>

 

 





