---
title: Структура CD3DX12_RT_FORMAT_ARRAY (D3dx12. h)
description: Вспомогательная структура, позволяющая легко инициализировать \_ \_ структуру массива формата D3D12 RT \_ .
ms.assetid: E890DD33-599F-4B20-BD15-2734867788E5
keywords:
- Структура CD3DX12_RT_FORMAT_ARRAY
topic_type:
- apiref
api_name:
- CD3DX12_RT_FORMAT_ARRAY
api_location:
- d3dx12.h
api_type:
- HeaderDef
ms.localizationpriority: low
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c05b7ae9e51d2d6b2a43f45dc83bda2074f6b734
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/15/2021
ms.locfileid: "105713966"
---
# <a name="cd3dx12_rt_format_array-structure"></a><span data-ttu-id="6d4ce-104">\_ \_ Структура массива формата CD3DX12 RT \_</span><span class="sxs-lookup"><span data-stu-id="6d4ce-104">CD3DX12\_RT\_FORMAT\_ARRAY structure</span></span>

<span data-ttu-id="6d4ce-105">Вспомогательная структура, позволяющая легко инициализировать структуру [**\_ \_ \_ массива формата D3D12 RT**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_rt_format_array) .</span><span class="sxs-lookup"><span data-stu-id="6d4ce-105">A helper structure to enable easy initialization of a [**D3D12\_RT\_FORMAT\_ARRAY**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_rt_format_array) structure.</span></span>

## <a name="syntax"></a><span data-ttu-id="6d4ce-106">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="6d4ce-106">Syntax</span></span>


```C++
struct CD3DX12_RT_FORMAT_ARRAY  : public D3D12_RT_FORMAT_ARRAY{
  CD3DX12_RT_FORMAT_ARRAY CD3DX12_RT_FORMAT_ARRAY();
  CD3DX12_RT_FORMAT_ARRAY explicit CD3DX12_RT_FORMAT_ARRAY(const D3D12_RT_FORMAT_ARRAY& o);
  CD3DX12_RT_FORMAT_ARRAY explicit CD3DX12_RT_FORMAT_ARRAY(const DXGI_FORMAT* pFormats, UINT NumFormats);
                          operator const D3D12_RT_FORMAT_ARRAY&() const;
};
```



## <a name="members"></a><span data-ttu-id="6d4ce-107">Члены</span><span class="sxs-lookup"><span data-stu-id="6d4ce-107">Members</span></span>

<dl> <dt>

<span data-ttu-id="6d4ce-108">**\_ \_ Массив формата CD3DX12 RT \_ ()**</span><span class="sxs-lookup"><span data-stu-id="6d4ce-108">**CD3DX12\_RT\_FORMAT\_ARRAY()**</span></span>
</dt> <dd>

<span data-ttu-id="6d4ce-109">Создает новый, неинициализированный экземпляр \_ \_ массива формата CD3DX12 RT \_ .</span><span class="sxs-lookup"><span data-stu-id="6d4ce-109">Creates a new, uninitialized, instance of a CD3DX12\_RT\_FORMAT\_ARRAY.</span></span>

</dd> <dt>

<span data-ttu-id="6d4ce-110">**явный \_ \_ массив формата CD3DX12 RT \_ (const D3D12 \_ \_ массив формата RT \_& o)**</span><span class="sxs-lookup"><span data-stu-id="6d4ce-110">**explicit CD3DX12\_RT\_FORMAT\_ARRAY(const D3D12\_RT\_FORMAT\_ARRAY& o)**</span></span>
</dt> <dd>

<span data-ttu-id="6d4ce-111">Создает новый экземпляр \_ \_ массива формата CD3DX12 RT \_ , инициализируемый значениями, скопированными из структуры [**\_ \_ \_ массива формата RT D3D12**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_rt_format_array) .</span><span class="sxs-lookup"><span data-stu-id="6d4ce-111">Creates a new instance of a CD3DX12\_RT\_FORMAT\_ARRAY, initialized with values copied from a [**D3D12\_RT\_FORMAT\_ARRAY**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_rt_format_array) structure.</span></span>

</dd> <dt>

<span data-ttu-id="6d4ce-112">**явный \_ \_ массив формата CD3DX12 RT \_ (const \_ ПФОРМАТС формата DXGI \* , uint нумформатс)**</span><span class="sxs-lookup"><span data-stu-id="6d4ce-112">**explicit CD3DX12\_RT\_FORMAT\_ARRAY(const DXGI\_FORMAT\* pFormats, UINT NumFormats)**</span></span>
</dt> <dd>

<span data-ttu-id="6d4ce-113">Создает новый экземпляр \_ \_ массива формата CD3DX12 RT \_ , инициализируемый значениями, передаваемыми в списке параметров.</span><span class="sxs-lookup"><span data-stu-id="6d4ce-113">Creates a new instance of a CD3DX12\_RT\_FORMAT\_ARRAY, initialized with the values passed in the parameter list.</span></span> <span data-ttu-id="6d4ce-114">Содержимое массива, заданного параметром *пформатс* , копируется в массив элементов **ртформатс**.</span><span class="sxs-lookup"><span data-stu-id="6d4ce-114">Contents of the array specified by the *pFormats* parameter are copied into the member array **RTFormats**.</span></span> <span data-ttu-id="6d4ce-115">Предполагается, что массив, заданный параметром *пформатс* , имеет тот же размер, что и **ртформатс**.</span><span class="sxs-lookup"><span data-stu-id="6d4ce-115">The array specified by *pFormats* is assumed to have the same size as **RTFormats**.</span></span>

</dd> <dt>

<span data-ttu-id="6d4ce-116">**Константа Array const D3D12 \_ \_ формата RT \_& () const**</span><span class="sxs-lookup"><span data-stu-id="6d4ce-116">**operator const D3D12\_RT\_FORMAT\_ARRAY&() const**</span></span>
</dt> <dd>

<span data-ttu-id="6d4ce-117">Неявное преобразование в структуру [**\_ \_ \_ массива формата D3D12 RT**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_rt_format_array) .</span><span class="sxs-lookup"><span data-stu-id="6d4ce-117">Implicit conversion to a [**D3D12\_RT\_FORMAT\_ARRAY**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_rt_format_array) structure.</span></span> <span data-ttu-id="6d4ce-118">Поскольку \_ \_ массив формата D3D12 RT \_ является базовым типом CD3DX12 \_ \_ DESC1 трафарета глубины \_ , объект просто возвращается как \_ ссылка на массив формата const D3D12 \_ RT \_ .</span><span class="sxs-lookup"><span data-stu-id="6d4ce-118">Because D3D12\_RT\_FORMAT\_ARRAY is the underlying type of CD3DX12\_DEPTH\_STENCIL\_DESC1, the object is simply returned as a const D3D12\_RT\_FORMAT\_ARRAY reference to itself.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="6d4ce-119">Требования</span><span class="sxs-lookup"><span data-stu-id="6d4ce-119">Requirements</span></span>



| <span data-ttu-id="6d4ce-120">Требование</span><span class="sxs-lookup"><span data-stu-id="6d4ce-120">Requirement</span></span> | <span data-ttu-id="6d4ce-121">Значение</span><span class="sxs-lookup"><span data-stu-id="6d4ce-121">Value</span></span> |
|-------------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="6d4ce-122">Header</span><span class="sxs-lookup"><span data-stu-id="6d4ce-122">Header</span></span><br/> | <dl> <span data-ttu-id="6d4ce-123"><dt>D3dx12. h</dt></span><span class="sxs-lookup"><span data-stu-id="6d4ce-123"><dt>D3dx12.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="6d4ce-124">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="6d4ce-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="6d4ce-125">Вспомогательные структуры для D3D12</span><span class="sxs-lookup"><span data-stu-id="6d4ce-125">Helper Structures for D3D12</span></span>](helper-structures-for-d3d12.md)
</dt> <dt>

[<span data-ttu-id="6d4ce-126">**\_ \_ Массив формата D3D12 \_ RT**</span><span class="sxs-lookup"><span data-stu-id="6d4ce-126">**D3D12\_RT\_FORMAT\_ARRAY**</span></span>](/windows/desktop/api/d3d12/ns-d3d12-d3d12_rt_format_array)
</dt> </dl>

 

 





