---
title: Структура CD3DX12_RANGE_UINT64 (D3dx12. h)
description: Вспомогательная структура, позволяющая легко инициализировать структуру D3D12 \_ диапазона \_ UINT64.
ms.assetid: 789A2C46-B7D4-462E-9C10-69FD63D27491
keywords:
- Структура CD3DX12_RANGE_UINT64
topic_type:
- apiref
api_name:
- CD3DX12_RANGE_UINT64
api_location:
- d3dx12.h
api_type:
- HeaderDef
ms.localizationpriority: low
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 89c408197afb1254cae922c402939f6f169708d4
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/15/2021
ms.locfileid: "105713981"
---
# <a name="cd3dx12_range_uint64-structure"></a><span data-ttu-id="a10ad-104">\_ \_ Структура UINT64 диапазона CD3DX12</span><span class="sxs-lookup"><span data-stu-id="a10ad-104">CD3DX12\_RANGE\_UINT64 structure</span></span>

<span data-ttu-id="a10ad-105">Вспомогательная структура, позволяющая легко инициализировать структуру [**D3D12 \_ диапазона \_ UINT64**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_range_uint64) .</span><span class="sxs-lookup"><span data-stu-id="a10ad-105">A helper structure to enable easy initialization of a [**D3D12\_RANGE\_UINT64**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_range_uint64) structure.</span></span>

## <a name="syntax"></a><span data-ttu-id="a10ad-106">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="a10ad-106">Syntax</span></span>


```C++
struct CD3DX12_RANGE_UINT64  : public D3D12_RANGE_UINT64{
  CD3DX12_RANGE_UINT64 CD3DX12_RANGE_UINT64();
  CD3DX12_RANGE_UINT64 explicit CD3DX12_RANGE_UINT64(const D3D12_RANGE_UINT64 &o);
  CD3DX12_RANGE_UINT64 CD3DX12_RANGE_UINT64(UINT64 begin, UINT64 end);
                       operator const D3D12_RANGE_UINT64&() const;
};
```



## <a name="members"></a><span data-ttu-id="a10ad-107">Члены</span><span class="sxs-lookup"><span data-stu-id="a10ad-107">Members</span></span>

<dl> <dt>

<span data-ttu-id="a10ad-108">**CD3DX12 \_ диапазона \_ UINT64 ()**</span><span class="sxs-lookup"><span data-stu-id="a10ad-108">**CD3DX12\_RANGE\_UINT64()**</span></span>
</dt> <dd>

<span data-ttu-id="a10ad-109">Создает новый, неинициализированный экземпляр класса \_ UINT64 диапазона CD3DX12 \_ .</span><span class="sxs-lookup"><span data-stu-id="a10ad-109">Creates a new, uninitialized, instance of a CD3DX12\_RANGE\_UINT64.</span></span>

</dd> <dt>

<span data-ttu-id="a10ad-110">**явный CD3DX12 \_ диапазон \_ UInt64 (константа D3D12 \_ Range \_ UInt64 &o)**</span><span class="sxs-lookup"><span data-stu-id="a10ad-110">**explicit CD3DX12\_RANGE\_UINT64(const D3D12\_RANGE\_UINT64 &o)**</span></span>
</dt> <dd>

<span data-ttu-id="a10ad-111">Создает новый экземпляр CD3DX12 \_ диапазона \_ UInt64, инициализируемый значениями, скопированными из структуры [**\_ \_ UINT64 диапазона D3D12**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_range_uint64) .</span><span class="sxs-lookup"><span data-stu-id="a10ad-111">Creates a new instance of a CD3DX12\_RANGE\_UINT64, initialized with values copied from a [**D3D12\_RANGE\_UINT64**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_range_uint64) structure.</span></span>

</dd> <dt>

<span data-ttu-id="a10ad-112">**CD3DX12 \_ диапазона \_ UInt64 (начало UInt64, окончание UInt64)**</span><span class="sxs-lookup"><span data-stu-id="a10ad-112">**CD3DX12\_RANGE\_UINT64(UINT64 begin, UINT64 end)**</span></span>
</dt> <dd>

<span data-ttu-id="a10ad-113">Создает новый экземпляр CD3DX12 \_ \_ трафарета глубины \_ DESC1, инициализируемый значениями, передаваемыми в списке параметров.</span><span class="sxs-lookup"><span data-stu-id="a10ad-113">Creates a new instance of a CD3DX12\_DEPTH\_STENCIL\_DESC1, initialized with the values passed in the parameter list.</span></span>

</dd> <dt>

<span data-ttu-id="a10ad-114">**Константа оператора const D3D12 \_ Range \_ UINT64& () const**</span><span class="sxs-lookup"><span data-stu-id="a10ad-114">**operator const D3D12\_RANGE\_UINT64&() const**</span></span>
</dt> <dd>

<span data-ttu-id="a10ad-115">Неявное преобразование в \_ структуру D3D12 диапазона \_ UINT64.</span><span class="sxs-lookup"><span data-stu-id="a10ad-115">Implicit conversion to a D3D12\_RANGE\_UINT64 structure.</span></span> <span data-ttu-id="a10ad-116">Так как D3D12 \_ Range \_ UInt64 является базовым типом \_ UInt64 CD3DX12 Range \_ , объект просто возвращается в виде константы D3D12 \_ диапазона \_ UInt64 на саму себя.</span><span class="sxs-lookup"><span data-stu-id="a10ad-116">Because D3D12\_RANGE\_UINT64 is the underlying type of CD3DX12\_RANGE\_UINT64, the object is simply returned as a const D3D12\_RANGE\_UINT64 reference to itself.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="a10ad-117">Требования</span><span class="sxs-lookup"><span data-stu-id="a10ad-117">Requirements</span></span>



| <span data-ttu-id="a10ad-118">Требование</span><span class="sxs-lookup"><span data-stu-id="a10ad-118">Requirement</span></span> | <span data-ttu-id="a10ad-119">Значение</span><span class="sxs-lookup"><span data-stu-id="a10ad-119">Value</span></span> |
|-------------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="a10ad-120">Header</span><span class="sxs-lookup"><span data-stu-id="a10ad-120">Header</span></span><br/> | <dl> <span data-ttu-id="a10ad-121"><dt>D3dx12. h</dt></span><span class="sxs-lookup"><span data-stu-id="a10ad-121"><dt>D3dx12.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="a10ad-122">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="a10ad-122">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a10ad-123">Вспомогательные структуры для D3D12</span><span class="sxs-lookup"><span data-stu-id="a10ad-123">Helper Structures for D3D12</span></span>](helper-structures-for-d3d12.md)
</dt> <dt>

[<span data-ttu-id="a10ad-124">**\_UINT64 диапазона \_ D3D12**</span><span class="sxs-lookup"><span data-stu-id="a10ad-124">**D3D12\_RANGE\_UINT64**</span></span>](/windows/desktop/api/d3d12/ns-d3d12-d3d12_range_uint64)
</dt> </dl>

 

 





