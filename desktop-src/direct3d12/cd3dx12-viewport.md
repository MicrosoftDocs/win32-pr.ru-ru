---
title: Структура CD3DX12_VIEWPORT (D3dx12. h)
description: Вспомогательная структура, позволяющая упростить инициализацию \_ структуры окна просмотра D3D12.
ms.assetid: 1A824F54-596B-450E-A191-B60FBBBB60ED
keywords:
- Структура CD3DX12_VIEWPORT
topic_type:
- apiref
api_name:
- CD3DX12_VIEWPORT
api_location:
- d3dx12.h
api_type:
- HeaderDef
ms.localizationpriority: low
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: da29adc50b62bd645070d9667bec1e5c7ce7ab15
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/15/2021
ms.locfileid: "105713965"
---
# <a name="cd3dx12_viewport-structure"></a><span data-ttu-id="516ab-104">\_Структура окна просмотра CD3DX12</span><span class="sxs-lookup"><span data-stu-id="516ab-104">CD3DX12\_VIEWPORT structure</span></span>

<span data-ttu-id="516ab-105">\[Некоторые сведения относятся к предварительно выпущенному продукту, который может быть значительно изменен перед коммерческой выпуском.</span><span class="sxs-lookup"><span data-stu-id="516ab-105">\[Some information relates to pre-released product which may be substantially modified before it's commercially released.</span></span> <span data-ttu-id="516ab-106">Майкрософт не дает никаких гарантий, явных или подразумеваемых, в отношении предоставленной здесь информации.\]</span><span class="sxs-lookup"><span data-stu-id="516ab-106">Microsoft makes no warranties, express or implied, with respect to the information provided here.\]</span></span>

<span data-ttu-id="516ab-107">Вспомогательная структура, позволяющая упростить инициализацию [**структуры \_ окна просмотра D3D12**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_viewport) .</span><span class="sxs-lookup"><span data-stu-id="516ab-107">A helper structure to enable easy initialization of a [**D3D12\_VIEWPORT**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_viewport) structure.</span></span>

## <a name="syntax"></a><span data-ttu-id="516ab-108">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="516ab-108">Syntax</span></span>


```C++
struct CD3DX12_VIEWPORT  : public D3D12_VIEWPORT{
   CD3DX12_VIEWPORT();
   explicit CD3DX12_VIEWPORT(const D3D12_VIEWPORT& o);
   explicit CD3DX12_VIEWPORT(FLOAT topLeftX, FLOAT topLeftY, FLOAT width, FLOAT height, FLOAT minDepth = D3D12_MIN_DEPTH, FLOAT maxDepth = D3D12_MAX_DEPTH);
   explicit CD3DX12_VIEWPORT(ID3D12Resource* pResource, UINT mipSlice = 0, FLOAT topLeftX = 0.0f, FLOAT topLeftY = 0.0f, FLOAT minDepth = D3D12_MIN_DEPTH, FLOAT maxDepth = D3D12_MAX_DEPTH);
   ~CD3DX12_VIEWPORT();
   operator const D3D12_VIEWPORT&() const;
};
```



## <a name="members"></a><span data-ttu-id="516ab-109">Члены</span><span class="sxs-lookup"><span data-stu-id="516ab-109">Members</span></span>

<dl> <dt>

<span data-ttu-id="516ab-110">**\_Окно просмотра CD3DX12 ()**</span><span class="sxs-lookup"><span data-stu-id="516ab-110">**CD3DX12\_VIEWPORT()**</span></span>
</dt> <dd>

<span data-ttu-id="516ab-111">Создает новый, неинициализированный экземпляр \_ окна просмотра CD3DX12.</span><span class="sxs-lookup"><span data-stu-id="516ab-111">Creates a new, uninitialized, instance of a CD3DX12\_VIEWPORT.</span></span>

</dd> <dt>

<span data-ttu-id="516ab-112">**явное \_ окно просмотра CD3DX12 (const D3D12 \_ окно просмотра& o)**</span><span class="sxs-lookup"><span data-stu-id="516ab-112">**explicit CD3DX12\_VIEWPORT(const D3D12\_VIEWPORT& o)**</span></span>
</dt> <dd>

<span data-ttu-id="516ab-113">Создает новый экземпляр \_ окна просмотра CD3DX12, инициализируя следующие параметры:</span><span class="sxs-lookup"><span data-stu-id="516ab-113">Creates a new instance of a CD3DX12\_VIEWPORT, initializing the following parameters:</span></span>

<span data-ttu-id="516ab-114">\_окно просмотра const D3D12& o</span><span class="sxs-lookup"><span data-stu-id="516ab-114">const D3D12\_VIEWPORT& o</span></span>

</dd> <dt>

<span data-ttu-id="516ab-115">**явное \_ окно просмотра CD3DX12 (float топлефткс, float топлефти, Width float, float с плавающей запятой, float миндепс = D3D12 \_ min \_ Depth, float MaxDepth = D3D12 \_ Максимальная \_ глубина)**</span><span class="sxs-lookup"><span data-stu-id="516ab-115">**explicit CD3DX12\_VIEWPORT(FLOAT topLeftX, FLOAT topLeftY, FLOAT width, FLOAT height, FLOAT minDepth = D3D12\_MIN\_DEPTH, FLOAT maxDepth = D3D12\_MAX\_DEPTH)**</span></span>
</dt> <dd>

<span data-ttu-id="516ab-116">Создает новый экземпляр \_ окна просмотра CD3DX12, инициализируя следующие параметры:</span><span class="sxs-lookup"><span data-stu-id="516ab-116">Creates a new instance of a CD3DX12\_VIEWPORT, initializing the following parameters:</span></span>

<span data-ttu-id="516ab-117">Топлефткс с плавающей запятой</span><span class="sxs-lookup"><span data-stu-id="516ab-117">FLOAT topLeftX</span></span>

<span data-ttu-id="516ab-118">Топлефти с плавающей запятой</span><span class="sxs-lookup"><span data-stu-id="516ab-118">FLOAT topLeftY</span></span>

<span data-ttu-id="516ab-119">Ширина плавающей запятой</span><span class="sxs-lookup"><span data-stu-id="516ab-119">FLOAT width</span></span>

<span data-ttu-id="516ab-120">Высота с плавающей запятой</span><span class="sxs-lookup"><span data-stu-id="516ab-120">FLOAT height</span></span>

<span data-ttu-id="516ab-121">FLOAT Миндепс = \_ Минимальная \_ глубина D3D12</span><span class="sxs-lookup"><span data-stu-id="516ab-121">FLOAT minDepth = D3D12\_MIN\_DEPTH</span></span>

<span data-ttu-id="516ab-122">FLOAT maxDepth = \_ Максимальная \_ глубина D3D12</span><span class="sxs-lookup"><span data-stu-id="516ab-122">FLOAT maxDepth = D3D12\_MAX\_DEPTH</span></span>

</dd> <dt>

<span data-ttu-id="516ab-123">**явное \_ окно просмотра CD3DX12 (тип данных ID3D12Resource, тип данных \* , uint мипслице = 0, float топлефткс = 0,0 f, float топлефти = 0,0 f, float МИНДЕПС = D3D12 \_ min \_ , float MaxDepth = D3D12 \_ Max \_ Depth)**</span><span class="sxs-lookup"><span data-stu-id="516ab-123">**explicit CD3DX12\_VIEWPORT(ID3D12Resource\* pResource, UINT mipSlice = 0, FLOAT topLeftX = 0.0f, FLOAT topLeftY = 0.0f, FLOAT minDepth = D3D12\_MIN\_DEPTH, FLOAT maxDepth = D3D12\_MAX\_DEPTH)**</span></span>
</dt> <dd>

<span data-ttu-id="516ab-124">Создает новый экземпляр \_ окна просмотра CD3DX12, инициализируя следующие параметры:</span><span class="sxs-lookup"><span data-stu-id="516ab-124">Creates a new instance of a CD3DX12\_VIEWPORT, initializing the following parameters:</span></span>

<span data-ttu-id="516ab-125">\*Исходный ID3D12Resource</span><span class="sxs-lookup"><span data-stu-id="516ab-125">ID3D12Resource\* pResource</span></span>

<span data-ttu-id="516ab-126">UINT Мипслице = 0</span><span class="sxs-lookup"><span data-stu-id="516ab-126">UINT mipSlice = 0</span></span>

<span data-ttu-id="516ab-127">FLOAT Топлефткс = 0,0 f</span><span class="sxs-lookup"><span data-stu-id="516ab-127">FLOAT topLeftX = 0.0f</span></span>

<span data-ttu-id="516ab-128">FLOAT Топлефти = 0,0 f</span><span class="sxs-lookup"><span data-stu-id="516ab-128">FLOAT topLeftY = 0.0f</span></span>

<span data-ttu-id="516ab-129">FLOAT Миндепс = \_ Минимальная \_ глубина D3D12</span><span class="sxs-lookup"><span data-stu-id="516ab-129">FLOAT minDepth = D3D12\_MIN\_DEPTH</span></span>

<span data-ttu-id="516ab-130">FLOAT maxDepth = \_ Максимальная \_ глубина D3D12</span><span class="sxs-lookup"><span data-stu-id="516ab-130">FLOAT maxDepth = D3D12\_MAX\_DEPTH</span></span>

</dd> <dt>

<span data-ttu-id="516ab-131">**\_Окно просмотра ~ CD3DX12 ()**</span><span class="sxs-lookup"><span data-stu-id="516ab-131">**~CD3DX12\_VIEWPORT()**</span></span>
</dt> <dd>

<span data-ttu-id="516ab-132">Уничтожает экземпляр \_ окна просмотра D3DX12.</span><span class="sxs-lookup"><span data-stu-id="516ab-132">Destroys an instance of a D3DX12\_VIEWPORT.</span></span>

</dd> <dt>

<span data-ttu-id="516ab-133">**окно "operator const D3D12" \_ окна просмотра& () const**</span><span class="sxs-lookup"><span data-stu-id="516ab-133">**operator const D3D12\_VIEWPORT&() const**</span></span>
</dt> <dd>

<span data-ttu-id="516ab-134">Определяет & оператором передачи по ссылке для типа родительской структуры.</span><span class="sxs-lookup"><span data-stu-id="516ab-134">Defines the & pass-by-reference operator for the parent structure type.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="516ab-135">Требования</span><span class="sxs-lookup"><span data-stu-id="516ab-135">Requirements</span></span>



| <span data-ttu-id="516ab-136">Требование</span><span class="sxs-lookup"><span data-stu-id="516ab-136">Requirement</span></span> | <span data-ttu-id="516ab-137">Значение</span><span class="sxs-lookup"><span data-stu-id="516ab-137">Value</span></span> |
|-------------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="516ab-138">Header</span><span class="sxs-lookup"><span data-stu-id="516ab-138">Header</span></span><br/> | <dl> <span data-ttu-id="516ab-139"><dt>D3dx12. h</dt></span><span class="sxs-lookup"><span data-stu-id="516ab-139"><dt>D3dx12.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="516ab-140">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="516ab-140">See also</span></span>

<dl> <dt>

[<span data-ttu-id="516ab-141">**\_Окно просмотра D3D12**</span><span class="sxs-lookup"><span data-stu-id="516ab-141">**D3D12\_VIEWPORT**</span></span>](/windows/desktop/api/d3d12/ns-d3d12-d3d12_viewport)
</dt> <dt>

[<span data-ttu-id="516ab-142">Вспомогательные структуры для D3D12</span><span class="sxs-lookup"><span data-stu-id="516ab-142">Helper Structures for D3D12</span></span>](helper-structures-for-d3d12.md)
</dt> </dl>

 

 





