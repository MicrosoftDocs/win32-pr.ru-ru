---
title: Структура CD3DX12_DEPTH_STENCIL_DESC1 (D3dx12. h)
description: Вспомогательная структура, позволяющая легко инициализировать \_ \_ структуру DESC1 шаблона глубины D3D12 \_ .
ms.assetid: 8EB008F9-212D-486E-9C62-D7BA9D3C6807
keywords:
- Структура CD3DX12_DEPTH_STENCIL_DESC1
topic_type:
- apiref
api_name:
- CD3DX12_DEPTH_STENCIL_DESC1
api_location:
- d3dx12.h
api_type:
- HeaderDef
ms.localizationpriority: low
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 976c05ec4f3ca85ccfcebb6a13dbe408ba05c64e
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/15/2021
ms.locfileid: "105647817"
---
# <a name="cd3dx12_depth_stencil_desc1-structure"></a><span data-ttu-id="3a0b5-104">\_ \_ Структура DESC1 набора элементов глубины CD3DX12 \_</span><span class="sxs-lookup"><span data-stu-id="3a0b5-104">CD3DX12\_DEPTH\_STENCIL\_DESC1 structure</span></span>

<span data-ttu-id="3a0b5-105">Вспомогательная структура, позволяющая легко инициализировать структуру [**\_ \_ \_ DESC1 шаблона глубины D3D12**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_depth_stencil_desc1) .</span><span class="sxs-lookup"><span data-stu-id="3a0b5-105">A helper structure to enable easy initialization of a [**D3D12\_DEPTH\_STENCIL\_DESC1**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_depth_stencil_desc1) structure.</span></span>

## <a name="syntax"></a><span data-ttu-id="3a0b5-106">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="3a0b5-106">Syntax</span></span>


```C++
struct CD3DX12_DEPTH_STENCIL_DESC1  : public D3D12_DEPTH_STENCIL_DESC1{
  CD3DX12_DEPTH_STENCIL_DESC1 CD3DX12_DEPTH_STENCIL_DESC1();
  CD3DX12_DEPTH_STENCIL_DESC1 explicit CD3DX12_DEPTH_STENCIL_DESC1(const D3D12_DEPTH_STENCIL_DESC1& o);
  CD3DX12_DEPTH_STENCIL_DESC1 explicit CD3DX12_DEPTH_STENCIL_DESC1(const D3D12_DEPTH_STENCIL_DESC& o);
  CD3DX12_DEPTH_STENCIL_DESC1 explicit CD3DX12_DEPTH_STENCIL_DESC1(CD3DX12_DEFAULT);
  CD3DX12_DEPTH_STENCIL_DESC1 explicit CD3DX12_DEPTH_STENCIL_DESC1(BOOL depthEnable, D3D12_DEPTH_WRITE_MASK depthWriteMask, D3D12_COMPARISON_FUNC depthFunc, BOOL stencilEnable, UINT8 stencilReadMask, UINT8 stencilWriteMask, D3D12_STENCIL_OP frontStencilFailOp, D3D12_STENCIL_OP frontStencilDepthFailOp, D3D12_STENCIL_OP frontStencilPassOp, D3D12_COMPARISON_FUNC frontStencilFunc, D3D12_STENCIL_OP backStencilFailOp, D3D12_STENCIL_OP backStencilDepthFailOp, D3D12_STENCIL_OP backStencilPassOp, D3D12_COMPARISON_FUNC backStencilFunc, BOOL depthBoundsTestEnable);
                              ~CD3DX12_DEPTH_STENCIL_DESC1();
                              operator const D3D12_DEPTH_STENCIL_DESC1&() const;
                              operator const D3D12_DEPTH_STENCIL_DESC() const;
};
```



## <a name="members"></a><span data-ttu-id="3a0b5-107">Члены</span><span class="sxs-lookup"><span data-stu-id="3a0b5-107">Members</span></span>

<dl> <dt>

<span data-ttu-id="3a0b5-108">**CD3DX12 \_ \_ трафарет \_ DESC1 ()**</span><span class="sxs-lookup"><span data-stu-id="3a0b5-108">**CD3DX12\_DEPTH\_STENCIL\_DESC1()**</span></span>
</dt> <dd>

<span data-ttu-id="3a0b5-109">Создает новый, неинициализированный экземпляр CD3DX12 \_ \_ трафарета глубины \_ DESC1.</span><span class="sxs-lookup"><span data-stu-id="3a0b5-109">Creates a new, uninitialized, instance of a CD3DX12\_DEPTH\_STENCIL\_DESC1.</span></span>

</dd> <dt>

<span data-ttu-id="3a0b5-110">**Explicit CD3DX12 \_ \_ трафарет \_ DESC1 (const D3D12 \_ трафарет глубины \_ \_ DESC1& o)**</span><span class="sxs-lookup"><span data-stu-id="3a0b5-110">**explicit CD3DX12\_DEPTH\_STENCIL\_DESC1(const D3D12\_DEPTH\_STENCIL\_DESC1& o)**</span></span>
</dt> <dd>

<span data-ttu-id="3a0b5-111">Создает новый экземпляр CD3DX12 \_ \_ трафарета глубины \_ DESC1, инициализируемый значениями, скопированными из структуры [**\_ \_ \_ DESC1 набора элементов глубины D3D12**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_depth_stencil_desc1) .</span><span class="sxs-lookup"><span data-stu-id="3a0b5-111">Creates a new instance of a CD3DX12\_DEPTH\_STENCIL\_DESC1, initialized with values copied from a [**D3D12\_DEPTH\_STENCIL\_DESC1**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_depth_stencil_desc1) structure.</span></span>

</dd> <dt>

<span data-ttu-id="3a0b5-112">**явный CD3DX12 \_ \_ трафарет \_ DESC1 (const D3D12 \_ трафарет глубины \_ , \_ DESC& o)**</span><span class="sxs-lookup"><span data-stu-id="3a0b5-112">**explicit CD3DX12\_DEPTH\_STENCIL\_DESC1(const D3D12\_DEPTH\_STENCIL\_DESC& o)**</span></span>
</dt> <dd>

<span data-ttu-id="3a0b5-113">Создает новый экземпляр CD3DX12 \_ \_ трафарета глубины \_ DESC1, инициализируемый значениями, скопированными из структуры [**\_ \_ набора элементов \_ глубины D3D12**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_depth_stencil_desc)</span><span class="sxs-lookup"><span data-stu-id="3a0b5-113">Creates a new instance of a CD3DX12\_DEPTH\_STENCIL\_DESC1, initialized with values copied from a [**D3D12\_DEPTH\_STENCIL\_DESC**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_depth_stencil_desc) structure</span></span>

<span data-ttu-id="3a0b5-114">а дополнительный элемент **депсбаундстестенабле** имеет значение **false**.</span><span class="sxs-lookup"><span data-stu-id="3a0b5-114">and the additional **DepthBoundsTestEnable** member set to **FALSE**.</span></span>

</dd> <dt>

<span data-ttu-id="3a0b5-115">**явное \_ CD3DX12 \_ шаблона глубины \_ DESC1 ( \_ по умолчанию CD3DX12)**</span><span class="sxs-lookup"><span data-stu-id="3a0b5-115">**explicit CD3DX12\_DEPTH\_STENCIL\_DESC1(CD3DX12\_DEFAULT)**</span></span>
</dt> <dd>

<span data-ttu-id="3a0b5-116">Создает новый экземпляр CD3DX12 \_ \_ трафарета глубины \_ DESC1, который инициализируется с состоянием по умолчанию, предписанным D3DX12:</span><span class="sxs-lookup"><span data-stu-id="3a0b5-116">Creates a new instance of a CD3DX12\_DEPTH\_STENCIL\_DESC1, initialized with the default state prescribed by D3DX12:</span></span>

``` syntax
        DepthEnable = TRUE;
        DepthWriteMask = D3D12_DEPTH_WRITE_MASK_ALL;
        DepthFunc = D3D12_COMPARISON_FUNC_LESS;
        StencilEnable = FALSE;
        StencilReadMask = D3D12_DEFAULT_STENCIL_READ_MASK;
        StencilWriteMask = D3D12_DEFAULT_STENCIL_WRITE_MASK;
        const D3D12_DEPTH_STENCILOP_DESC defaultStencilOp =
        { D3D12_STENCIL_OP_KEEP, D3D12_STENCIL_OP_KEEP, D3D12_STENCIL_OP_KEEP, D3D12_COMPARISON_FUNC_ALWAYS };
        FrontFace = defaultStencilOp;
        BackFace = defaultStencilOp;
    DepthBoundsTestEnable = FALSE;
          
```

</dd> <dt>

<span data-ttu-id="3a0b5-117">**явный CD3DX12 \_ \_ трафарет \_ DESC1 (bool депсенабле, D3D12- \_ \_ маска записи \_ , депсвритемаск, D3D12 \_ Сравнение \_ Func ДЕПСФУНК, bool СТЕНЦИЛЕНАБЛЕ, UINT8 СтенЦилреадмаск, UINT8 стенЦилвритемаск, D3D12 \_ трафарет \_ Op frontStencilFailOp, D3D12 \_ трафарет \_ Op \_ \_ \_ \_ \_ \_ \_ \_ \_ \_ \_ \_ frontStencilDepthFailOp, D3D12 трафарет Op frontStencilPassOp, D3D12-, frontStencilFunc, D3D12 наборов элементов**</span><span class="sxs-lookup"><span data-stu-id="3a0b5-117">**explicit CD3DX12\_DEPTH\_STENCIL\_DESC1(BOOL depthEnable, D3D12\_DEPTH\_WRITE\_MASK depthWriteMask, D3D12\_COMPARISON\_FUNC depthFunc, BOOL stencilEnable, UINT8 stencilReadMask, UINT8 stencilWriteMask, D3D12\_STENCIL\_OP frontStencilFailOp, D3D12\_STENCIL\_OP frontStencilDepthFailOp, D3D12\_STENCIL\_OP frontStencilPassOp, D3D12\_COMPARISON\_FUNC frontStencilFunc, D3D12\_STENCIL\_OP backStencilFailOp, D3D12\_STENCIL\_OP backStencilDepthFailOp, D3D12\_STENCIL\_OP backStencilPassOp, D3D12\_COMPARISON\_FUNC backStencilFunc, BOOL depthBoundsTestEnable)**</span></span>
</dt> <dd>

<span data-ttu-id="3a0b5-118">Создает новый экземпляр CD3DX12 \_ \_ трафарета глубины \_ DESC1, инициализируемый значениями, передаваемыми в списке параметров.</span><span class="sxs-lookup"><span data-stu-id="3a0b5-118">Creates a new instance of a CD3DX12\_DEPTH\_STENCIL\_DESC1, initialized with the values passed in the parameter list.</span></span>

</dd> <dt>

<span data-ttu-id="3a0b5-119">**~ CD3DX12 \_ \_ трафарет \_ DESC1 ()**</span><span class="sxs-lookup"><span data-stu-id="3a0b5-119">**~CD3DX12\_DEPTH\_STENCIL\_DESC1()**</span></span>
</dt> <dd>

<span data-ttu-id="3a0b5-120">Уничтожает экземпляр D3DX12 \_ \_ трафарета глубины \_ DESC1.</span><span class="sxs-lookup"><span data-stu-id="3a0b5-120">Destroys an instance of a D3DX12\_DEPTH\_STENCIL\_DESC1.</span></span>

</dd> <dt>

<span data-ttu-id="3a0b5-121">**const const D3D12 \_ \_ шаблона глубины \_ DESC1& () константа**</span><span class="sxs-lookup"><span data-stu-id="3a0b5-121">**operator const D3D12\_DEPTH\_STENCIL\_DESC1&() const**</span></span>
</dt> <dd>

<span data-ttu-id="3a0b5-122">Неявное преобразование в \_ \_ структуру DESC1 шаблона глубины D3D12 \_ .</span><span class="sxs-lookup"><span data-stu-id="3a0b5-122">Implicit conversion to a D3D12\_DEPTH\_STENCIL\_DESC1 structure.</span></span> <span data-ttu-id="3a0b5-123">Так как \_ D3D12 \_ \_ DESC1 трафарет является базовым типом CD3DX12 \_ \_ набора элементов глубины \_ DESC1, он просто возвращается в виде const D3D12 \_ \_ шаблона глубины \_ DESC1 ссылкой на самого себя.</span><span class="sxs-lookup"><span data-stu-id="3a0b5-123">Because D3D12\_DEPTH\_STENCIL\_DESC1 is the underlying type of CD3DX12\_DEPTH\_STENCIL\_DESC1, the object is simply returned as a const D3D12\_DEPTH\_STENCIL\_DESC1 reference to itself.</span></span>

</dd> <dt>

<span data-ttu-id="3a0b5-124">**const const D3D12 \_ \_ шаблона глубины \_ "оператор"**</span><span class="sxs-lookup"><span data-stu-id="3a0b5-124">**operator const D3D12\_DEPTH\_STENCIL\_DESC() const**</span></span>
</dt> <dd>

<span data-ttu-id="3a0b5-125">Неявное преобразование в \_ \_ значение структуры D3D12 в трафарете глубины \_ .</span><span class="sxs-lookup"><span data-stu-id="3a0b5-125">Implicit conversion to a D3D12\_DEPTH\_STENCIL\_DESC structure value.</span></span> <span data-ttu-id="3a0b5-126">Поскольку D3D12 \_ \_ в наборе элементов глубины не \_ является базовым типом \_ CD3DX12 \_ DESC1 трафарета глубины \_ , \_ создается новый \_ экземпляр набора элементов глубины D3D12, который \_ возвращается по значению.</span><span class="sxs-lookup"><span data-stu-id="3a0b5-126">Because D3D12\_DEPTH\_STENCIL\_DESC is not the underlying type of CD3DX12\_DEPTH\_STENCIL\_DESC1, a new D3D12\_DEPTH\_STENCIL\_DESC instance is created and returned by value.</span></span> <span data-ttu-id="3a0b5-127">Обратите внимание, что D3D12 в \_ \_ наборе элементов глубины не \_ включает элемент **депсбаундстестенабле** , поэтому это значение теряется при преобразовании.</span><span class="sxs-lookup"><span data-stu-id="3a0b5-127">Note that D3D12\_DEPTH\_STENCIL\_DESC does not include the **DepthBoundsTestEnable** member, so this value is lost in the conversion.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="3a0b5-128">Требования</span><span class="sxs-lookup"><span data-stu-id="3a0b5-128">Requirements</span></span>



| <span data-ttu-id="3a0b5-129">Требование</span><span class="sxs-lookup"><span data-stu-id="3a0b5-129">Requirement</span></span> | <span data-ttu-id="3a0b5-130">Значение</span><span class="sxs-lookup"><span data-stu-id="3a0b5-130">Value</span></span> |
|-------------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="3a0b5-131">Header</span><span class="sxs-lookup"><span data-stu-id="3a0b5-131">Header</span></span><br/> | <dl> <span data-ttu-id="3a0b5-132"><dt>D3dx12. h</dt></span><span class="sxs-lookup"><span data-stu-id="3a0b5-132"><dt>D3dx12.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="3a0b5-133">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="3a0b5-133">See also</span></span>

<dl> <dt>

[<span data-ttu-id="3a0b5-134">Вспомогательные структуры для D3D12</span><span class="sxs-lookup"><span data-stu-id="3a0b5-134">Helper Structures for D3D12</span></span>](helper-structures-for-d3d12.md)
</dt> <dt>

[<span data-ttu-id="3a0b5-135">**D3D12 \_ \_ трафарета глубины \_ DESC1**</span><span class="sxs-lookup"><span data-stu-id="3a0b5-135">**D3D12\_DEPTH\_STENCIL\_DESC1**</span></span>](/windows/desktop/api/d3d12/ns-d3d12-d3d12_depth_stencil_desc1)
</dt> <dt>

[<span data-ttu-id="3a0b5-136">**D3D12 \_ \_ трафарета \_ глубины**</span><span class="sxs-lookup"><span data-stu-id="3a0b5-136">**D3D12\_DEPTH\_STENCIL\_DESC**</span></span>](/windows/desktop/api/d3d12/ns-d3d12-d3d12_depth_stencil_desc)
</dt> </dl>

 

 





