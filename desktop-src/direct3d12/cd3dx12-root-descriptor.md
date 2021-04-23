---
title: Структура CD3DX12_ROOT_DESCRIPTOR (D3dx12. h)
description: Вспомогательная структура, позволяющая упростить инициализацию \_ \_ структуры дескриптора корня D3D12.
ms.assetid: DB05BAB7-DD30-4EC7-8D66-C0B2D8DD7BAC
keywords:
- Структура CD3DX12_ROOT_DESCRIPTOR
topic_type:
- apiref
api_name:
- CD3DX12_ROOT_DESCRIPTOR
api_location:
- d3dx12.h
api_type:
- HeaderDef
ms.localizationpriority: low
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 710064436e0287b570700ff5812b728ca62be56d
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/15/2021
ms.locfileid: "105713972"
---
# <a name="cd3dx12_root_descriptor-structure"></a><span data-ttu-id="58995-104">\_ \_ Структура дескриптора корня CD3DX12</span><span class="sxs-lookup"><span data-stu-id="58995-104">CD3DX12\_ROOT\_DESCRIPTOR structure</span></span>

<span data-ttu-id="58995-105">Вспомогательная структура, позволяющая упростить инициализацию [**структуры \_ \_ дескриптора корня D3D12**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_root_descriptor) .</span><span class="sxs-lookup"><span data-stu-id="58995-105">A helper structure to enable easy initialization of a [**D3D12\_ROOT\_DESCRIPTOR**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_root_descriptor) structure.</span></span>

## <a name="syntax"></a><span data-ttu-id="58995-106">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="58995-106">Syntax</span></span>


```C++
struct CD3DX12_ROOT_DESCRIPTOR  : public D3D12_ROOT_DESCRIPTOR{
       CD3DX12_ROOT_DESCRIPTOR();
       explicit CD3DX12_ROOT_DESCRIPTOR(const D3D12_ROOT_DESCRIPTOR &o);
       CD3DX12_ROOT_DESCRIPTOR(UINT shaderRegister, UINT registerSpace = 0);
  void inline Init(UINT shaderRegister, UINT registerSpace = 0);
  void static inline Init(D3D12_ROOT_DESCRIPTOR &table, UINT shaderRegister, UINT registerSpace = 0);
};
```



## <a name="members"></a><span data-ttu-id="58995-107">Члены</span><span class="sxs-lookup"><span data-stu-id="58995-107">Members</span></span>

<dl> <dt>

<span data-ttu-id="58995-108">**\_Корневой \_ дескриптор CD3DX12 ()**</span><span class="sxs-lookup"><span data-stu-id="58995-108">**CD3DX12\_ROOT\_DESCRIPTOR()**</span></span>
</dt> <dd>

<span data-ttu-id="58995-109">Создает новый, неинициализированный экземпляр \_ \_ дескриптора CD3DX12 root.</span><span class="sxs-lookup"><span data-stu-id="58995-109">Creates a new, uninitialized, instance of a CD3DX12\_ROOT\_DESCRIPTOR.</span></span>

</dd> <dt>

<span data-ttu-id="58995-110">**явный CD3DX12 \_ корневого \_ дескриптора (const D3D12 \_ root \_ дескриптора &o)**</span><span class="sxs-lookup"><span data-stu-id="58995-110">**explicit CD3DX12\_ROOT\_DESCRIPTOR(const D3D12\_ROOT\_DESCRIPTOR &o)**</span></span>
</dt> <dd>

<span data-ttu-id="58995-111">Создает новый экземпляр \_ \_ дескриптора root CD3DX12, инициализированного с содержимым другой структуры [**\_ \_ дескриптора root D3D12**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_root_descriptor) .</span><span class="sxs-lookup"><span data-stu-id="58995-111">Creates a new instance of a CD3DX12\_ROOT\_DESCRIPTOR, initialized with the contents of another [**D3D12\_ROOT\_DESCRIPTOR**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_root_descriptor) structure.</span></span>

</dd> <dt>

<span data-ttu-id="58995-112">**\_Корневой \_ дескриптор CD3DX12 (uint ШАДЕРРЕГИСТЕР, uint регистерспаце = 0)**</span><span class="sxs-lookup"><span data-stu-id="58995-112">**CD3DX12\_ROOT\_DESCRIPTOR(UINT shaderRegister, UINT registerSpace = 0)**</span></span>
</dt> <dd>

<span data-ttu-id="58995-113">Создает новый экземпляр \_ корневого \_ дескриптора CD3DX12, инициализируя следующие параметры:</span><span class="sxs-lookup"><span data-stu-id="58995-113">Creates a new instance of a CD3DX12\_ROOT\_DESCRIPTOR, initializing the following parameters:</span></span>

<span data-ttu-id="58995-114">UINT Шадеррегистер</span><span class="sxs-lookup"><span data-stu-id="58995-114">UINT shaderRegister</span></span>

<span data-ttu-id="58995-115">участие UINT Регистерспаце = 0</span><span class="sxs-lookup"><span data-stu-id="58995-115">(opt) UINT registerSpace = 0</span></span>

</dd> <dt>

<span data-ttu-id="58995-116">**Inline init (UINT Шадеррегистер, UINT Регистерспаце = 0)**</span><span class="sxs-lookup"><span data-stu-id="58995-116">**inline Init(UINT shaderRegister, UINT registerSpace = 0)**</span></span>
</dt> <dd>

<span data-ttu-id="58995-117">Задает функцию, которая инициализирует следующие параметры:</span><span class="sxs-lookup"><span data-stu-id="58995-117">Specifies a function that initializes the following parameters:</span></span>

<span data-ttu-id="58995-118">UINT Шадеррегистер</span><span class="sxs-lookup"><span data-stu-id="58995-118">UINT shaderRegister</span></span>

<span data-ttu-id="58995-119">участие UINT Регистерспаце = 0</span><span class="sxs-lookup"><span data-stu-id="58995-119">(opt) UINT registerSpace = 0</span></span>

</dd> <dt>

<span data-ttu-id="58995-120">**static Inline init (D3D12 \_ root \_ дескриптора таблицы &, uint ШАДЕРРЕГИСТЕР, uint регистерспаце = 0)**</span><span class="sxs-lookup"><span data-stu-id="58995-120">**static inline Init(D3D12\_ROOT\_DESCRIPTOR &table, UINT shaderRegister, UINT registerSpace = 0)**</span></span>
</dt> <dd>

<span data-ttu-id="58995-121">Задает функцию, которая инициализирует следующие параметры:</span><span class="sxs-lookup"><span data-stu-id="58995-121">Specifies a function that initializes the following parameters:</span></span>

<span data-ttu-id="58995-122">[**D3D12 \_ Таблица &КОРНЕВого \_ дескриптора**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_root_descriptor)</span><span class="sxs-lookup"><span data-stu-id="58995-122">[**D3D12\_ROOT\_DESCRIPTOR**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_root_descriptor) &table</span></span>

<span data-ttu-id="58995-123">UINT Шадеррегистер</span><span class="sxs-lookup"><span data-stu-id="58995-123">UINT shaderRegister</span></span>

<span data-ttu-id="58995-124">участие UINT Регистерспаце = 0</span><span class="sxs-lookup"><span data-stu-id="58995-124">(opt) UINT registerSpace = 0</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="58995-125">Требования</span><span class="sxs-lookup"><span data-stu-id="58995-125">Requirements</span></span>



| <span data-ttu-id="58995-126">Требование</span><span class="sxs-lookup"><span data-stu-id="58995-126">Requirement</span></span> | <span data-ttu-id="58995-127">Значение</span><span class="sxs-lookup"><span data-stu-id="58995-127">Value</span></span> |
|-------------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="58995-128">Header</span><span class="sxs-lookup"><span data-stu-id="58995-128">Header</span></span><br/> | <dl> <span data-ttu-id="58995-129"><dt>D3dx12. h</dt></span><span class="sxs-lookup"><span data-stu-id="58995-129"><dt>D3dx12.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="58995-130">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="58995-130">See also</span></span>

<dl> <dt>

[<span data-ttu-id="58995-131">**\_Дескриптор корня \_ D3D12**</span><span class="sxs-lookup"><span data-stu-id="58995-131">**D3D12\_ROOT\_DESCRIPTOR**</span></span>](/windows/desktop/api/d3d12/ns-d3d12-d3d12_root_descriptor)
</dt> <dt>

[<span data-ttu-id="58995-132">Вспомогательные структуры для D3D12</span><span class="sxs-lookup"><span data-stu-id="58995-132">Helper Structures for D3D12</span></span>](helper-structures-for-d3d12.md)
</dt> </dl>

 

 





