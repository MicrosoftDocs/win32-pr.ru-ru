---
title: Структура CD3DX12_SUBRESOURCE_RANGE_UINT64 (D3dx12. h)
description: Вспомогательная структура, позволяющая упростить инициализацию \_ структуры диапазона ПОДРЕСУРСОВ D3D12 \_ \_ .
ms.assetid: 607A60ED-98D2-4A77-9A7A-6B54342EA101
keywords:
- Структура CD3DX12_SUBRESOURCE_RANGE_UINT64
topic_type:
- apiref
api_name:
- CD3DX12_SUBRESOURCE_RANGE_UINT64
api_location:
- d3dx12.h
api_type:
- HeaderDef
ms.localizationpriority: low
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2aea83d993c0c7b58ded8d0b92374d1dcbacdcc8
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/15/2021
ms.locfileid: "105713500"
---
# <a name="cd3dx12_subresource_range_uint64-structure"></a><span data-ttu-id="c01a0-104">\_ \_ Структура UINT64 диапазона ПОДресурсов CD3DX12 \_</span><span class="sxs-lookup"><span data-stu-id="c01a0-104">CD3DX12\_SUBRESOURCE\_RANGE\_UINT64 structure</span></span>

<span data-ttu-id="c01a0-105">Вспомогательная структура, позволяющая упростить инициализацию [**структуры \_ \_ диапазона \_ подресурсов D3D12**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_subresource_range_uint64) .</span><span class="sxs-lookup"><span data-stu-id="c01a0-105">A helper structure to enable easy initialization of a [**D3D12\_SUBRESOURCE\_RANGE\_UINT64**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_subresource_range_uint64) structure.</span></span>

## <a name="syntax"></a><span data-ttu-id="c01a0-106">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="c01a0-106">Syntax</span></span>


```C++
struct CD3DX12_SUBRESOURCE_RANGE_UINT64  : public D3D12_SUBRESOURCE_RANGE_UINT64{
  CD3DX12_SUBRESOURCE_RANGE_UINT64 CD3DX12_SUBRESOURCE_RANGE_UINT64();
  CD3DX12_SUBRESOURCE_RANGE_UINT64 explicit CD3DX12_SUBRESOURCE_RANGE_UINT64(const D3D12_SUBRESOURCE_RANGE_UINT64 &o);
  CD3DX12_SUBRESOURCE_RANGE_UINT64 CD3DX12_SUBRESOURCE_RANGE_UINT64(UINT subresource, const D3D12_RANGE_UINT64& range);
  CD3DX12_SUBRESOURCE_RANGE_UINT64 CD3DX12_SUBRESOURCE_RANGE_UINT64(UINT subresource, UINT64 begin, UINT64 end);
                                   operator const D3D12_SUBRESOURCE_RANGE_UINT64&() const;
};
```



## <a name="members"></a><span data-ttu-id="c01a0-107">Члены</span><span class="sxs-lookup"><span data-stu-id="c01a0-107">Members</span></span>

<dl> <dt>

<span data-ttu-id="c01a0-108">**\_UINT64 диапазона ПОДРЕСУРСОВ CD3DX12 \_ \_ ()**</span><span class="sxs-lookup"><span data-stu-id="c01a0-108">**CD3DX12\_SUBRESOURCE\_RANGE\_UINT64()**</span></span>
</dt> <dd>

<span data-ttu-id="c01a0-109">Создает новый, неинициализированный экземпляр значения \_ UINT64 диапазона ПОДРЕСУРСОВ CD3DX12 \_ \_ .</span><span class="sxs-lookup"><span data-stu-id="c01a0-109">Creates a new, uninitialized, instance of a CD3DX12\_SUBRESOURCE\_RANGE\_UINT64.</span></span>

</dd> <dt>

<span data-ttu-id="c01a0-110">**явный CD3DX12 \_ диапазон ПОДресурсов, \_ \_ UInt64 (константа D3D12 \_ диапазон подресурсов, \_ \_ UInt64 &o)**</span><span class="sxs-lookup"><span data-stu-id="c01a0-110">**explicit CD3DX12\_SUBRESOURCE\_RANGE\_UINT64(const D3D12\_SUBRESOURCE\_RANGE\_UINT64 &o)**</span></span>
</dt> <dd>

<span data-ttu-id="c01a0-111">Создает новый экземпляр класса CD3DX12 \_ \_ с диапазоном \_ UInt64, инициализируемый значениями, скопированными из структуры [**\_ \_ \_ UINT64 диапазона подресурсов D3D12**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_subresource_range_uint64) .</span><span class="sxs-lookup"><span data-stu-id="c01a0-111">Creates a new instance of a CD3DX12\_SUBRESOURCE\_RANGE\_UINT64, initialized with values copied from a [**D3D12\_SUBRESOURCE\_RANGE\_UINT64**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_subresource_range_uint64) structure.</span></span>

</dd> <dt>

<span data-ttu-id="c01a0-112">**CD3DX12 диапазона \_ подресурсов \_ \_ ("подресурс uint", константа D3D12 \_ диапазона \_ UInt64&)**</span><span class="sxs-lookup"><span data-stu-id="c01a0-112">**CD3DX12\_SUBRESOURCE\_RANGE\_UINT64(UINT subresource, const D3D12\_RANGE\_UINT64& range)**</span></span>
</dt> <dd>

<span data-ttu-id="c01a0-113">Создает новый экземпляр CD3DX12 \_ \_ трафарета глубины \_ DESC1, инициализируемый значениями, передаваемыми в списке параметров.</span><span class="sxs-lookup"><span data-stu-id="c01a0-113">Creates a new instance of a CD3DX12\_DEPTH\_STENCIL\_DESC1, initialized with the values passed in the parameter list.</span></span>

</dd> <dt>

<span data-ttu-id="c01a0-114">**\_UINT64 диапазона ПОДРЕСУРСОВ CD3DX12 \_ \_ (подресурс uint, начало UINT64, конец UInt64)**</span><span class="sxs-lookup"><span data-stu-id="c01a0-114">**CD3DX12\_SUBRESOURCE\_RANGE\_UINT64(UINT subresource, UINT64 begin, UINT64 end)**</span></span>
</dt> <dd>

<span data-ttu-id="c01a0-115">Создает новый экземпляр CD3DX12 \_ \_ трафарета глубины \_ DESC1, инициализируемый значениями, передаваемыми в списке параметров.</span><span class="sxs-lookup"><span data-stu-id="c01a0-115">Creates a new instance of a CD3DX12\_DEPTH\_STENCIL\_DESC1, initialized with the values passed in the parameter list.</span></span>

</dd> <dt>

<span data-ttu-id="c01a0-116">**Константа оператора const D3D12 \_ диапазон подресурсов \_ \_ UINT64& () const**</span><span class="sxs-lookup"><span data-stu-id="c01a0-116">**operator const D3D12\_SUBRESOURCE\_RANGE\_UINT64&() const**</span></span>
</dt> <dd>

<span data-ttu-id="c01a0-117">Неявное преобразование в \_ структуру D3D12 \_ диапазона подресурсов \_ .</span><span class="sxs-lookup"><span data-stu-id="c01a0-117">Implicit conversion to a D3D12\_SUBRESOURCE\_RANGE\_UINT64 structure.</span></span> <span data-ttu-id="c01a0-118">Так как D3D12 \_ диапазона подресурсов \_ \_ является базовым типом для \_ диапазона CD3DX12 \_ \_ , то объект просто возвращается в виде константы D3D12 \_ \_ трафарета глубины \_ DESC1 ссылку на себя.</span><span class="sxs-lookup"><span data-stu-id="c01a0-118">Because D3D12\_SUBRESOURCE\_RANGE\_UINT64 is the underlying type of CD3DX12\_SUBRESOURCE\_RANGE\_UINT64, the object is simply returned as a const D3D12\_DEPTH\_STENCIL\_DESC1 reference to itself.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="c01a0-119">Требования</span><span class="sxs-lookup"><span data-stu-id="c01a0-119">Requirements</span></span>



| <span data-ttu-id="c01a0-120">Требование</span><span class="sxs-lookup"><span data-stu-id="c01a0-120">Requirement</span></span> | <span data-ttu-id="c01a0-121">Значение</span><span class="sxs-lookup"><span data-stu-id="c01a0-121">Value</span></span> |
|-------------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="c01a0-122">Header</span><span class="sxs-lookup"><span data-stu-id="c01a0-122">Header</span></span><br/> | <dl> <span data-ttu-id="c01a0-123"><dt>D3dx12. h</dt></span><span class="sxs-lookup"><span data-stu-id="c01a0-123"><dt>D3dx12.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="c01a0-124">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="c01a0-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c01a0-125">Вспомогательные структуры для D3D12</span><span class="sxs-lookup"><span data-stu-id="c01a0-125">Helper Structures for D3D12</span></span>](helper-structures-for-d3d12.md)
</dt> <dt>

[<span data-ttu-id="c01a0-126">**\_UINT64 диапазона ПОДРЕСУРСОВ D3D12 \_ \_**</span><span class="sxs-lookup"><span data-stu-id="c01a0-126">**D3D12\_SUBRESOURCE\_RANGE\_UINT64**</span></span>](/windows/desktop/api/d3d12/ns-d3d12-d3d12_subresource_range_uint64)
</dt> </dl>

 

 





