---
title: Структура CD3DX12_PACKED_MIP_INFO (D3dx12. h)
description: Вспомогательная структура, позволяющая легко инициализировать D3D12 \_ упакованную \_ \_ информационную структуру MIP.
ms.assetid: B3549D78-C354-48FC-A012-1F835DBD585E
keywords:
- Структура CD3DX12_PACKED_MIP_INFO
topic_type:
- apiref
api_name:
- CD3DX12_PACKED_MIP_INFO
api_location:
- d3dx12.h
api_type:
- HeaderDef
ms.localizationpriority: low
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0f4565bbac6189cffc5358213437463b4abc0322
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/15/2021
ms.locfileid: "105703677"
---
# <a name="cd3dx12_packed_mip_info-structure"></a><span data-ttu-id="37071-104">CD3DX12 \_ упакованная \_ \_ информационная структура MIP</span><span class="sxs-lookup"><span data-stu-id="37071-104">CD3DX12\_PACKED\_MIP\_INFO structure</span></span>

<span data-ttu-id="37071-105">Вспомогательная структура, позволяющая легко инициализировать [**D3D12 \_ упакованную \_ \_ информационную структуру MIP**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_packed_mip_info) .</span><span class="sxs-lookup"><span data-stu-id="37071-105">A helper structure to enable easy initialization of a [**D3D12\_PACKED\_MIP\_INFO**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_packed_mip_info) structure.</span></span>

## <a name="syntax"></a><span data-ttu-id="37071-106">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="37071-106">Syntax</span></span>


```C++
struct CD3DX12_PACKED_MIP_INFO  : public D3D12_PACKED_MIP_INFO{
   CD3DX12_PACKED_MIP_INFO();
   explicit CD3DX12_PACKED_MIP_INFO(const D3D12_PACKED_MIP_INFO &o);
   CD3DX12_PACKED_MIP_INFO(UINT8 numStandardMips, UINT8 numPackedMips, UINT numTilesForPackedMips, UINT startTileIndexInOverallResource);
   operator const D3D12_PACKED_MIP_INFO&() const;
};
```



## <a name="members"></a><span data-ttu-id="37071-107">Члены</span><span class="sxs-lookup"><span data-stu-id="37071-107">Members</span></span>

<dl> <dt>

<span data-ttu-id="37071-108">**CD3DX12 \_ Упакованные \_ MIP \_ info ()**</span><span class="sxs-lookup"><span data-stu-id="37071-108">**CD3DX12\_PACKED\_MIP\_INFO()**</span></span>
</dt> <dd>

<span data-ttu-id="37071-109">Создает новый, неинициализированный экземпляр CD3DX12 \_ \_ \_ сведений о MIP.</span><span class="sxs-lookup"><span data-stu-id="37071-109">Creates a new, uninitialized, instance of a CD3DX12\_PACKED\_MIP\_INFO.</span></span>

</dd> <dt>

<span data-ttu-id="37071-110">**явные CD3DX12 \_ Упакованные \_ \_ сведения о MIP (const D3D12 \_ упакованный \_ MIP \_ info &o)**</span><span class="sxs-lookup"><span data-stu-id="37071-110">**explicit CD3DX12\_PACKED\_MIP\_INFO(const D3D12\_PACKED\_MIP\_INFO &o)**</span></span>
</dt> <dd>

<span data-ttu-id="37071-111">Создает новый экземпляр CD3DX12 \_ упакованной \_ \_ информации MIP, инициализированной с содержимым другой [**D3D12 \_ упакованной структуры \_ \_ сведений MIP**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_packed_mip_info) .</span><span class="sxs-lookup"><span data-stu-id="37071-111">Creates a new instance of a CD3DX12\_PACKED\_MIP\_INFO, initialized with the contents of another [**D3D12\_PACKED\_MIP\_INFO**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_packed_mip_info) structure.</span></span>

</dd> <dt>

<span data-ttu-id="37071-112">**CD3DX12 \_ Упакованные \_ \_ сведения о MIP (UINT8 Нумстандардмипс, UINT8 Нумпаккедмипс, UINT Нумтилесфорпаккедмипс, uint старттилеиндексиновераллресаурце)**</span><span class="sxs-lookup"><span data-stu-id="37071-112">**CD3DX12\_PACKED\_MIP\_INFO(UINT8 numStandardMips, UINT8 numPackedMips, UINT numTilesForPackedMips, UINT startTileIndexInOverallResource)**</span></span>
</dt> <dd>

<span data-ttu-id="37071-113">Создает новый экземпляр CD3DX12 \_ упакованных \_ \_ сведений о MIP, инициализируя следующие параметры:</span><span class="sxs-lookup"><span data-stu-id="37071-113">Creates a new instance of a CD3DX12\_PACKED\_MIP\_INFO, initializing the following parameters:</span></span>

<span data-ttu-id="37071-114">UINT8 Нумстандардмипс</span><span class="sxs-lookup"><span data-stu-id="37071-114">UINT8 numStandardMips</span></span>

<span data-ttu-id="37071-115">UINT8 Нумпаккедмипс</span><span class="sxs-lookup"><span data-stu-id="37071-115">UINT8 numPackedMips</span></span>

<span data-ttu-id="37071-116">UINT Нумтилесфорпаккедмипс</span><span class="sxs-lookup"><span data-stu-id="37071-116">UINT numTilesForPackedMips</span></span>

<span data-ttu-id="37071-117">UINT Старттилеиндексиновераллресаурце</span><span class="sxs-lookup"><span data-stu-id="37071-117">UINT startTileIndexInOverallResource</span></span>

</dd> <dt>

<span data-ttu-id="37071-118">**Оператор const D3D12 \_ Упакованные \_ MIP \_ info& () const**</span><span class="sxs-lookup"><span data-stu-id="37071-118">**operator const D3D12\_PACKED\_MIP\_INFO&() const**</span></span>
</dt> <dd>

<span data-ttu-id="37071-119">Определяет & оператором передачи по ссылке для типа родительской структуры.</span><span class="sxs-lookup"><span data-stu-id="37071-119">Defines the & pass-by-reference operator for the parent structure type.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="37071-120">Требования</span><span class="sxs-lookup"><span data-stu-id="37071-120">Requirements</span></span>



| <span data-ttu-id="37071-121">Требование</span><span class="sxs-lookup"><span data-stu-id="37071-121">Requirement</span></span> | <span data-ttu-id="37071-122">Значение</span><span class="sxs-lookup"><span data-stu-id="37071-122">Value</span></span> |
|-------------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="37071-123">Header</span><span class="sxs-lookup"><span data-stu-id="37071-123">Header</span></span><br/> | <dl> <span data-ttu-id="37071-124"><dt>D3dx12. h</dt></span><span class="sxs-lookup"><span data-stu-id="37071-124"><dt>D3dx12.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="37071-125">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="37071-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="37071-126">**\_ \_ Сведения о упакованных MIP D3D12 \_**</span><span class="sxs-lookup"><span data-stu-id="37071-126">**D3D12\_PACKED\_MIP\_INFO**</span></span>](/windows/desktop/api/d3d12/ns-d3d12-d3d12_packed_mip_info)
</dt> <dt>

[<span data-ttu-id="37071-127">Вспомогательные структуры для D3D12</span><span class="sxs-lookup"><span data-stu-id="37071-127">Helper Structures for D3D12</span></span>](helper-structures-for-d3d12.md)
</dt> </dl>

 

 





