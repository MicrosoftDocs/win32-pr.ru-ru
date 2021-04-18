---
title: Структура CD3DX12_ROOT_CONSTANTS (D3dx12. h)
description: Вспомогательная структура, позволяющая упростить инициализацию \_ структуры корневых \_ констант D3D12.
ms.assetid: 2F517DCE-BC0C-4678-9C25-D826036F99A8
keywords:
- Структура CD3DX12_ROOT_CONSTANTS
topic_type:
- apiref
api_name:
- CD3DX12_ROOT_CONSTANTS
api_location:
- d3dx12.h
api_type:
- HeaderDef
ms.localizationpriority: low
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a7a1f81a429b083400adad60f316cc90c4ede1d9
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/15/2021
ms.locfileid: "105713510"
---
# <a name="cd3dx12_root_constants-structure"></a><span data-ttu-id="2cd2d-104">\_Структура корневых \_ констант CD3DX12</span><span class="sxs-lookup"><span data-stu-id="2cd2d-104">CD3DX12\_ROOT\_CONSTANTS structure</span></span>

<span data-ttu-id="2cd2d-105">Вспомогательная структура, позволяющая упростить инициализацию [**структуры \_ корневых \_ констант D3D12**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_root_constants) .</span><span class="sxs-lookup"><span data-stu-id="2cd2d-105">A helper structure to enable easy initialization of a [**D3D12\_ROOT\_CONSTANTS**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_root_constants) structure.</span></span>

## <a name="syntax"></a><span data-ttu-id="2cd2d-106">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="2cd2d-106">Syntax</span></span>


```C++
struct CD3DX12_ROOT_CONSTANTS  : public D3D12_ROOT_CONSTANTS{
       CD3DX12_ROOT_CONSTANTS();
       explicit CD3DX12_ROOT_CONSTANTS(const D3D12_ROOT_CONSTANTS &o);
       CD3DX12_ROOT_CONSTANTS(UINT num32BitValues, UINT shaderRegister, UINT registerSpace = 0);
  void inline Init(UINT num32BitValues, UINT shaderRegister, UINT registerSpace = 0);
  void static inline Init(D3D12_ROOT_CONSTANTS &rootConstants, UINT num32BitValues, UINT shaderRegister, UINT registerSpace = 0);
};
```



## <a name="members"></a><span data-ttu-id="2cd2d-107">Члены</span><span class="sxs-lookup"><span data-stu-id="2cd2d-107">Members</span></span>

<dl> <dt>

<span data-ttu-id="2cd2d-108">**\_ \_ Константы CD3DX12 root ()**</span><span class="sxs-lookup"><span data-stu-id="2cd2d-108">**CD3DX12\_ROOT\_CONSTANTS()**</span></span>
</dt> <dd>

<span data-ttu-id="2cd2d-109">Создает новый, неинициализированный экземпляр \_ \_ константы CD3DX12 root.</span><span class="sxs-lookup"><span data-stu-id="2cd2d-109">Creates a new, uninitialized, instance of a CD3DX12\_ROOT\_CONSTANTS.</span></span>

</dd> <dt>

<span data-ttu-id="2cd2d-110">**явные \_ \_ константы CD3DX12 (const D3D12 \_ root \_ константы &o)**</span><span class="sxs-lookup"><span data-stu-id="2cd2d-110">**explicit CD3DX12\_ROOT\_CONSTANTS(const D3D12\_ROOT\_CONSTANTS &o)**</span></span>
</dt> <dd>

<span data-ttu-id="2cd2d-111">Создает новый экземпляр \_ \_ константы CD3DX12 root, который инициализируется содержимым другой структуры [**\_ \_ констант D3D12 root**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_root_constants) .</span><span class="sxs-lookup"><span data-stu-id="2cd2d-111">Creates a new instance of a CD3DX12\_ROOT\_CONSTANTS, initialized with the contents of another [**D3D12\_ROOT\_CONSTANTS**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_root_constants) structure.</span></span>

</dd> <dt>

<span data-ttu-id="2cd2d-112">**\_ \_ Константы CD3DX12 root (uint NUM32BITVALUES, uint ШАДЕРРЕГИСТЕР, uint регистерспаце = 0)**</span><span class="sxs-lookup"><span data-stu-id="2cd2d-112">**CD3DX12\_ROOT\_CONSTANTS(UINT num32BitValues, UINT shaderRegister, UINT registerSpace = 0)**</span></span>
</dt> <dd>

<span data-ttu-id="2cd2d-113">Создает новый экземпляр \_ \_ константы CD3DX12 root, инициализируя следующие параметры:</span><span class="sxs-lookup"><span data-stu-id="2cd2d-113">Creates a new instance of a CD3DX12\_ROOT\_CONSTANTS, initializing the following parameters:</span></span>

<span data-ttu-id="2cd2d-114">UINT num32BitValues</span><span class="sxs-lookup"><span data-stu-id="2cd2d-114">UINT num32BitValues</span></span>

<span data-ttu-id="2cd2d-115">UINT Шадеррегистер</span><span class="sxs-lookup"><span data-stu-id="2cd2d-115">UINT shaderRegister</span></span>

<span data-ttu-id="2cd2d-116">участие UINT Регистерспаце = 0</span><span class="sxs-lookup"><span data-stu-id="2cd2d-116">(opt) UINT registerSpace = 0</span></span>

</dd> <dt>

<span data-ttu-id="2cd2d-117">**Inline init (UINT num32BitValues, UINT Шадеррегистер, UINT Регистерспаце = 0)**</span><span class="sxs-lookup"><span data-stu-id="2cd2d-117">**inline Init(UINT num32BitValues, UINT shaderRegister, UINT registerSpace = 0)**</span></span>
</dt> <dd>

<span data-ttu-id="2cd2d-118">Задает функцию, которая инициализирует следующие параметры:</span><span class="sxs-lookup"><span data-stu-id="2cd2d-118">Specifies a function that initializes the following parameters:</span></span>

<span data-ttu-id="2cd2d-119">UINT num32BitValues</span><span class="sxs-lookup"><span data-stu-id="2cd2d-119">UINT num32BitValues</span></span>

<span data-ttu-id="2cd2d-120">UINT Шадеррегистер</span><span class="sxs-lookup"><span data-stu-id="2cd2d-120">UINT shaderRegister</span></span>

<span data-ttu-id="2cd2d-121">участие UINT Регистерспаце = 0</span><span class="sxs-lookup"><span data-stu-id="2cd2d-121">(opt) UINT registerSpace = 0</span></span>

</dd> <dt>

<span data-ttu-id="2cd2d-122">**Статическая встроенная init (D3D12 \_ root- \_ константы &РУТКОНСТАНТС, uint NUM32BITVALUES, uint ШАДЕРРЕГИСТЕР, uint регистерспаце = 0)**</span><span class="sxs-lookup"><span data-stu-id="2cd2d-122">**static inline Init(D3D12\_ROOT\_CONSTANTS &rootConstants, UINT num32BitValues, UINT shaderRegister, UINT registerSpace = 0)**</span></span>
</dt> <dd>

<span data-ttu-id="2cd2d-123">Задает функцию, которая инициализирует следующие параметры:</span><span class="sxs-lookup"><span data-stu-id="2cd2d-123">Specifies a function that initializes the following parameters:</span></span>

<span data-ttu-id="2cd2d-124">[**D3D12 \_ КОРНЕВые \_ константы**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_root_constants) &рутконстантс</span><span class="sxs-lookup"><span data-stu-id="2cd2d-124">[**D3D12\_ROOT\_CONSTANTS**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_root_constants) &rootConstants</span></span>

<span data-ttu-id="2cd2d-125">UINT num32BitValues</span><span class="sxs-lookup"><span data-stu-id="2cd2d-125">UINT num32BitValues</span></span>

<span data-ttu-id="2cd2d-126">UINT Шадеррегистер</span><span class="sxs-lookup"><span data-stu-id="2cd2d-126">UINT shaderRegister</span></span>

<span data-ttu-id="2cd2d-127">участие UINT Регистерспаце = 0</span><span class="sxs-lookup"><span data-stu-id="2cd2d-127">(opt) UINT registerSpace = 0</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="2cd2d-128">Требования</span><span class="sxs-lookup"><span data-stu-id="2cd2d-128">Requirements</span></span>



| <span data-ttu-id="2cd2d-129">Требование</span><span class="sxs-lookup"><span data-stu-id="2cd2d-129">Requirement</span></span> | <span data-ttu-id="2cd2d-130">Значение</span><span class="sxs-lookup"><span data-stu-id="2cd2d-130">Value</span></span> |
|-------------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="2cd2d-131">Header</span><span class="sxs-lookup"><span data-stu-id="2cd2d-131">Header</span></span><br/> | <dl> <span data-ttu-id="2cd2d-132"><dt>D3dx12. h</dt></span><span class="sxs-lookup"><span data-stu-id="2cd2d-132"><dt>D3dx12.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="2cd2d-133">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="2cd2d-133">See also</span></span>

<dl> <dt>

[<span data-ttu-id="2cd2d-134">**\_ \_ Константы D3D12 root**</span><span class="sxs-lookup"><span data-stu-id="2cd2d-134">**D3D12\_ROOT\_CONSTANTS**</span></span>](/windows/desktop/api/d3d12/ns-d3d12-d3d12_root_constants)
</dt> <dt>

[<span data-ttu-id="2cd2d-135">Вспомогательные структуры для D3D12</span><span class="sxs-lookup"><span data-stu-id="2cd2d-135">Helper Structures for D3D12</span></span>](helper-structures-for-d3d12.md)
</dt> </dl>

 

 





