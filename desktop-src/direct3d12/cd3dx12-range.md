---
title: Структура CD3DX12_RANGE (D3dx12. h)
description: Вспомогательная структура, позволяющая упростить инициализацию \_ структуры диапазона D3D12.
ms.assetid: 5D5192BF-D14C-487B-A214-F8428E82AF0E
keywords:
- Структура CD3DX12_RANGE
topic_type:
- apiref
api_name:
- CD3DX12_RANGE
api_location:
- d3dx12.h
api_type:
- HeaderDef
ms.localizationpriority: low
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 66b6b92cd24a981d48252f5ad457f7ac0320e2d7
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/15/2021
ms.locfileid: "105713980"
---
# <a name="cd3dx12_range-structure"></a><span data-ttu-id="34a84-104">\_Структура диапазона CD3DX12</span><span class="sxs-lookup"><span data-stu-id="34a84-104">CD3DX12\_RANGE structure</span></span>

<span data-ttu-id="34a84-105">Вспомогательная структура, позволяющая упростить инициализацию [**структуры \_ диапазона D3D12**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_range) .</span><span class="sxs-lookup"><span data-stu-id="34a84-105">A helper structure to enable easy initialization of a [**D3D12\_RANGE**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_range) structure.</span></span>

## <a name="syntax"></a><span data-ttu-id="34a84-106">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="34a84-106">Syntax</span></span>


```C++
struct CD3DX12_RANGE  : public D3D12_RANGE{
   CD3DX12_RANGE();
   explicit CD3DX12_RANGE(const D3D12_RANGE &o);
   CD3DX12_RANGE(SIZE_T begin, SIZE_T end);
   operator const D3D12_RANGE&() const;
};
```



## <a name="members"></a><span data-ttu-id="34a84-107">Члены</span><span class="sxs-lookup"><span data-stu-id="34a84-107">Members</span></span>

<dl> <dt>

<span data-ttu-id="34a84-108">**CD3DX12 \_ Range ()**</span><span class="sxs-lookup"><span data-stu-id="34a84-108">**CD3DX12\_RANGE()**</span></span>
</dt> <dd>

<span data-ttu-id="34a84-109">Создает новый, неинициализированный экземпляр \_ диапазона CD3DX12.</span><span class="sxs-lookup"><span data-stu-id="34a84-109">Creates a new, uninitialized, instance of a CD3DX12\_RANGE.</span></span>

</dd> <dt>

<span data-ttu-id="34a84-110">**явный \_ диапазон CD3DX12 (константа D3D12 \_ Range &o)**</span><span class="sxs-lookup"><span data-stu-id="34a84-110">**explicit CD3DX12\_RANGE(const D3D12\_RANGE &o)**</span></span>
</dt> <dd>

<span data-ttu-id="34a84-111">Создает новый экземпляр \_ диапазона CD3DX12, инициализируемый содержимым другой структуры [**\_ диапазона D3D12**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_range) .</span><span class="sxs-lookup"><span data-stu-id="34a84-111">Creates a new instance of a CD3DX12\_RANGE, initialized with the contents of another [**D3D12\_RANGE**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_range) structure.</span></span>

</dd> <dt>

<span data-ttu-id="34a84-112">**\_Диапазон CD3DX12 (размер \_ t, конец и размер \_ t)**</span><span class="sxs-lookup"><span data-stu-id="34a84-112">**CD3DX12\_RANGE(SIZE\_T begin, SIZE\_T end)**</span></span>
</dt> <dd>

<span data-ttu-id="34a84-113">Создает новый экземпляр \_ диапазона CD3DX12, инициализируя следующие параметры:</span><span class="sxs-lookup"><span data-stu-id="34a84-113">Creates a new instance of a CD3DX12\_RANGE, initializing the following parameters:</span></span>

<span data-ttu-id="34a84-114">РАЗМЕР \_ T начало</span><span class="sxs-lookup"><span data-stu-id="34a84-114">SIZE\_T begin</span></span>

<span data-ttu-id="34a84-115">РАЗМЕР \_ T в конце</span><span class="sxs-lookup"><span data-stu-id="34a84-115">SIZE\_T end</span></span>

</dd> <dt>

<span data-ttu-id="34a84-116">**Константа оператора const D3D12 \_ RANGE& () const**</span><span class="sxs-lookup"><span data-stu-id="34a84-116">**operator const D3D12\_RANGE&() const**</span></span>
</dt> <dd>

<span data-ttu-id="34a84-117">Определяет & оператором передачи по ссылке для типа родительской структуры.</span><span class="sxs-lookup"><span data-stu-id="34a84-117">Defines the & pass-by-reference operator for the parent structure type.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="34a84-118">Требования</span><span class="sxs-lookup"><span data-stu-id="34a84-118">Requirements</span></span>



| <span data-ttu-id="34a84-119">Требование</span><span class="sxs-lookup"><span data-stu-id="34a84-119">Requirement</span></span> | <span data-ttu-id="34a84-120">Значение</span><span class="sxs-lookup"><span data-stu-id="34a84-120">Value</span></span> |
|-------------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="34a84-121">Header</span><span class="sxs-lookup"><span data-stu-id="34a84-121">Header</span></span><br/> | <dl> <span data-ttu-id="34a84-122"><dt>D3dx12. h</dt></span><span class="sxs-lookup"><span data-stu-id="34a84-122"><dt>D3dx12.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="34a84-123">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="34a84-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="34a84-124">**\_Диапазон D3D12**</span><span class="sxs-lookup"><span data-stu-id="34a84-124">**D3D12\_RANGE**</span></span>](/windows/desktop/api/d3d12/ns-d3d12-d3d12_range)
</dt> <dt>

[<span data-ttu-id="34a84-125">Вспомогательные структуры для D3D12</span><span class="sxs-lookup"><span data-stu-id="34a84-125">Helper Structures for D3D12</span></span>](helper-structures-for-d3d12.md)
</dt> </dl>

 

 





