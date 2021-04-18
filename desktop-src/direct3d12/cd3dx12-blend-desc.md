---
title: Структура CD3DX12_BLEND_DESC (D3dx12. h)
description: Вспомогательная структура, позволяющая легко инициализировать структуру D3D12 \_ Blend \_ DESC.
ms.assetid: D37BB62E-904B-4953-9119-21F3B37570C0
keywords:
- Структура CD3DX12_BLEND_DESC
topic_type:
- apiref
api_name:
- CD3DX12_BLEND_DESC
api_location:
- d3dx12.h
api_type:
- HeaderDef
ms.localizationpriority: low
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ddb88ce003f74251c3ce34a2ca47ae2fb55f892d
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/15/2021
ms.locfileid: "105703683"
---
# <a name="cd3dx12_blend_desc-structure"></a><span data-ttu-id="28f54-104">\_ \_ Структура DESC CD3DX12 Blend</span><span class="sxs-lookup"><span data-stu-id="28f54-104">CD3DX12\_BLEND\_DESC structure</span></span>

<span data-ttu-id="28f54-105">Вспомогательная структура, позволяющая легко инициализировать структуру [**D3D12 \_ Blend \_ DESC**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_blend_desc) .</span><span class="sxs-lookup"><span data-stu-id="28f54-105">A helper structure to enable easy initialization of a [**D3D12\_BLEND\_DESC**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_blend_desc) structure.</span></span>

## <a name="syntax"></a><span data-ttu-id="28f54-106">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="28f54-106">Syntax</span></span>


```C++
struct CD3DX12_BLEND_DESC  : public D3D12_BLEND_DESC{
   CD3DX12_BLEND_DESC();
   explicit CD3DX12_BLEND_DESC(const D3D12_BLEND_DESC& o);
   explicit CD3DX12_BLEND_DESC(CD3DX12_DEFAULT);
   ~CD3DX12_BLEND_DESC();
   operator const D3D12_BLEND_DESC&() const;
};
```



## <a name="members"></a><span data-ttu-id="28f54-107">Члены</span><span class="sxs-lookup"><span data-stu-id="28f54-107">Members</span></span>

<dl> <dt>

<span data-ttu-id="28f54-108">**CD3DX12 \_ Blend \_ DESC ()**</span><span class="sxs-lookup"><span data-stu-id="28f54-108">**CD3DX12\_BLEND\_DESC()**</span></span>
</dt> <dd>

<span data-ttu-id="28f54-109">Создает новый, неинициализированный экземпляр экземпляра CD3DX12 \_ Blend \_ DESC.</span><span class="sxs-lookup"><span data-stu-id="28f54-109">Creates a new, uninitialized, instance of a CD3DX12\_BLEND\_DESC.</span></span>

</dd> <dt>

<span data-ttu-id="28f54-110">**явное CD3DX12 \_ Blend \_ DESC (const D3D12 \_ Blend \_ DESC& o)**</span><span class="sxs-lookup"><span data-stu-id="28f54-110">**explicit CD3DX12\_BLEND\_DESC(const D3D12\_BLEND\_DESC& o)**</span></span>
</dt> <dd>

<span data-ttu-id="28f54-111">Создает новый экземпляр CD3DX12 \_ Blend \_ DESC, инициализированный с содержимым другой структуры [**D3D12 \_ Blend \_**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_blend_desc) .</span><span class="sxs-lookup"><span data-stu-id="28f54-111">Creates a new instance of a CD3DX12\_BLEND\_DESC, initialized with the contents of another [**D3D12\_BLEND\_DESC**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_blend_desc) structure.</span></span>

</dd> <dt>

<span data-ttu-id="28f54-112">**явное CD3DX12 \_ Blend \_ DESC (CD3DX12 \_ по умолчанию)**</span><span class="sxs-lookup"><span data-stu-id="28f54-112">**explicit CD3DX12\_BLEND\_DESC(CD3DX12\_DEFAULT)**</span></span>
</dt> <dd>

<span data-ttu-id="28f54-113">Создает новый экземпляр CD3DX12 \_ Blend \_ DESC, инициализируемый параметрами по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="28f54-113">Creates a new instance of a CD3DX12\_BLEND\_DESC, initialized with default parameters.</span></span>



| <span data-ttu-id="28f54-114">Состояние</span><span class="sxs-lookup"><span data-stu-id="28f54-114">State</span></span>                                   | <span data-ttu-id="28f54-115">Значение по умолчанию</span><span class="sxs-lookup"><span data-stu-id="28f54-115">Default Value</span></span>                    |
|-----------------------------------------|----------------------------------|
| <span data-ttu-id="28f54-116">алфатоковеражеенабле</span><span class="sxs-lookup"><span data-stu-id="28f54-116">AlphaToCoverageEnable</span></span>                   | <span data-ttu-id="28f54-117">**FALSE**</span><span class="sxs-lookup"><span data-stu-id="28f54-117">**FALSE**</span></span>                        |
| <span data-ttu-id="28f54-118">индепендентбленденабле</span><span class="sxs-lookup"><span data-stu-id="28f54-118">IndependentBlendEnable</span></span>                  | <span data-ttu-id="28f54-119">**FALSE**</span><span class="sxs-lookup"><span data-stu-id="28f54-119">**FALSE**</span></span>                        |
| <span data-ttu-id="28f54-120">Рендертаржет \[ 0 \] . бленденабле</span><span class="sxs-lookup"><span data-stu-id="28f54-120">RenderTarget\[0\].BlendEnable</span></span>           | <span data-ttu-id="28f54-121">**FALSE**</span><span class="sxs-lookup"><span data-stu-id="28f54-121">**FALSE**</span></span>                        |
| <span data-ttu-id="28f54-122">Рендертаржет \[ 0 \] . логикопенабле</span><span class="sxs-lookup"><span data-stu-id="28f54-122">RenderTarget\[0\].LogicOpEnable</span></span>         | <span data-ttu-id="28f54-123">**FALSE**</span><span class="sxs-lookup"><span data-stu-id="28f54-123">**FALSE**</span></span>                        |
| <span data-ttu-id="28f54-124">Рендертаржет \[ 0 \] . сркбленд</span><span class="sxs-lookup"><span data-stu-id="28f54-124">RenderTarget\[0\].SrcBlend</span></span>              | <span data-ttu-id="28f54-125">D3D12 \_ Blend ( \_ один)</span><span class="sxs-lookup"><span data-stu-id="28f54-125">D3D12\_BLEND\_ONE</span></span>                |
| <span data-ttu-id="28f54-126">Рендертаржет \[ 0 \] . дестбленд</span><span class="sxs-lookup"><span data-stu-id="28f54-126">RenderTarget\[0\].DestBlend</span></span>             | <span data-ttu-id="28f54-127">D3D12 \_ Blend \_ 0</span><span class="sxs-lookup"><span data-stu-id="28f54-127">D3D12\_BLEND\_ZERO</span></span>               |
| <span data-ttu-id="28f54-128">Рендертаржет \[ 0 \] . блендоп</span><span class="sxs-lookup"><span data-stu-id="28f54-128">RenderTarget\[0\].BlendOp</span></span>               | <span data-ttu-id="28f54-129">\_Добавление D3D12 Blend \_ Op \_</span><span class="sxs-lookup"><span data-stu-id="28f54-129">D3D12\_BLEND\_OP\_ADD</span></span>            |
| <span data-ttu-id="28f54-130">Рендертаржет \[ 0 \] . сркблендалфа</span><span class="sxs-lookup"><span data-stu-id="28f54-130">RenderTarget\[0\].SrcBlendAlpha</span></span>         | <span data-ttu-id="28f54-131">D3D12 \_ Blend ( \_ один)</span><span class="sxs-lookup"><span data-stu-id="28f54-131">D3D12\_BLEND\_ONE</span></span>                |
| <span data-ttu-id="28f54-132">Рендертаржет \[ 0 \] . дестблендалфа</span><span class="sxs-lookup"><span data-stu-id="28f54-132">RenderTarget\[0\].DestBlendAlpha</span></span>        | <span data-ttu-id="28f54-133">D3D12 \_ Blend \_ 0</span><span class="sxs-lookup"><span data-stu-id="28f54-133">D3D12\_BLEND\_ZERO</span></span>               |
| <span data-ttu-id="28f54-134">Рендертаржет \[ 0 \] . блендопалфа</span><span class="sxs-lookup"><span data-stu-id="28f54-134">RenderTarget\[0\].BlendOpAlpha</span></span>          | <span data-ttu-id="28f54-135">\_Добавление D3D12 Blend \_ Op \_</span><span class="sxs-lookup"><span data-stu-id="28f54-135">D3D12\_BLEND\_OP\_ADD</span></span>            |
| <span data-ttu-id="28f54-136">Рендертаржет \[ 0 \] . логикоп</span><span class="sxs-lookup"><span data-stu-id="28f54-136">RenderTarget\[0\].LogicOp</span></span>               | <span data-ttu-id="28f54-137">D3D12 \_ Logic \_ Op \_</span><span class="sxs-lookup"><span data-stu-id="28f54-137">D3D12\_LOGIC\_OP\_NOOP</span></span>           |
| <span data-ttu-id="28f54-138">Рендертаржет \[ 0 \] . рендертаржетвритемаск</span><span class="sxs-lookup"><span data-stu-id="28f54-138">RenderTarget\[0\].RenderTargetWriteMask</span></span> | <span data-ttu-id="28f54-139">D3D12 \_ Цвет \_ записи \_ включить \_ все</span><span class="sxs-lookup"><span data-stu-id="28f54-139">D3D12\_COLOR\_WRITE\_ENABLE\_ALL</span></span> |



 

</dd> <dt>

<span data-ttu-id="28f54-140">**~ CD3DX12 \_ Blend \_ DESC ()**</span><span class="sxs-lookup"><span data-stu-id="28f54-140">**~CD3DX12\_BLEND\_DESC()**</span></span>
</dt> <dd>

<span data-ttu-id="28f54-141">Уничтожает экземпляр CD3DX12 \_ Blend \_ DESC.</span><span class="sxs-lookup"><span data-stu-id="28f54-141">Destroys an instance of a CD3DX12\_BLEND\_DESC.</span></span>

</dd> <dt>

<span data-ttu-id="28f54-142">**Константа operator const D3D12 \_ Blend \_ DESC& () const**</span><span class="sxs-lookup"><span data-stu-id="28f54-142">**operator const D3D12\_BLEND\_DESC&() const**</span></span>
</dt> <dd>

<span data-ttu-id="28f54-143">Определяет & оператором передачи по ссылке для типа родительской структуры.</span><span class="sxs-lookup"><span data-stu-id="28f54-143">Defines the & pass-by-reference operator for the parent structure type.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="28f54-144">Требования</span><span class="sxs-lookup"><span data-stu-id="28f54-144">Requirements</span></span>



| <span data-ttu-id="28f54-145">Требование</span><span class="sxs-lookup"><span data-stu-id="28f54-145">Requirement</span></span> | <span data-ttu-id="28f54-146">Значение</span><span class="sxs-lookup"><span data-stu-id="28f54-146">Value</span></span> |
|-------------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="28f54-147">Header</span><span class="sxs-lookup"><span data-stu-id="28f54-147">Header</span></span><br/> | <dl> <span data-ttu-id="28f54-148"><dt>D3dx12. h</dt></span><span class="sxs-lookup"><span data-stu-id="28f54-148"><dt>D3dx12.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="28f54-149">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="28f54-149">See also</span></span>

<dl> <dt>

[<span data-ttu-id="28f54-150">**D3D12 \_ Blend, \_ DESC**</span><span class="sxs-lookup"><span data-stu-id="28f54-150">**D3D12\_BLEND\_DESC**</span></span>](/windows/desktop/api/d3d12/ns-d3d12-d3d12_blend_desc)
</dt> <dt>

[<span data-ttu-id="28f54-151">Вспомогательные структуры для D3D12</span><span class="sxs-lookup"><span data-stu-id="28f54-151">Helper Structures for D3D12</span></span>](helper-structures-for-d3d12.md)
</dt> </dl>

 

 





