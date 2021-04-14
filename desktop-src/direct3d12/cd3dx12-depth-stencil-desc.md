---
title: Структура CD3DX12_DEPTH_STENCIL_DESC (D3dx12. h)
description: Вспомогательная структура, позволяющая упростить инициализацию \_ \_ структуры набора элементов глубины D3D12 \_ .
ms.assetid: D3DB04C3-4564-45A4-830A-E63B8D308B33
keywords:
- Структура CD3DX12_DEPTH_STENCIL_DESC
topic_type:
- apiref
api_name:
- CD3DX12_DEPTH_STENCIL_DESC
api_location:
- d3dx12.h
api_type:
- HeaderDef
ms.localizationpriority: low
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2f36a071251a12c4d27d06586775c01759b88d38
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/15/2021
ms.locfileid: "105647820"
---
# <a name="cd3dx12_depth_stencil_desc-structure"></a><span data-ttu-id="1fa4e-104">CD3DX12 \_ \_ Структура набора элементов глубины \_</span><span class="sxs-lookup"><span data-stu-id="1fa4e-104">CD3DX12\_DEPTH\_STENCIL\_DESC structure</span></span>

<span data-ttu-id="1fa4e-105">Вспомогательная структура, позволяющая упростить инициализацию [**структуры \_ \_ набора элементов \_ глубины D3D12**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_depth_stencil_desc) .</span><span class="sxs-lookup"><span data-stu-id="1fa4e-105">A helper structure to enable easy initialization of a [**D3D12\_DEPTH\_STENCIL\_DESC**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_depth_stencil_desc) structure.</span></span>

## <a name="syntax"></a><span data-ttu-id="1fa4e-106">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="1fa4e-106">Syntax</span></span>


```C++
struct CD3DX12_DEPTH_STENCIL_DESC  : public D3D12_DEPTH_STENCIL_DESC{
   CD3DX12_DEPTH_STENCIL_DESC();
   explicit CD3DX12_DEPTH_STENCIL_DESC(const D3D12_DEPTH_STENCIL_DESC& o);
   explicit CD3DX12_DEPTH_STENCIL_DESC(CD3DX12_DEFAULT);
   explicit CD3DX12_DEPTH_STENCIL_DESC(BOOL depthEnable, D3D12_DEPTH_WRITE_MASK depthWriteMask, D3D12_COMPARISON_FUNC depthFunc, BOOL stencilEnable, UINT8 stencilReadMask, UINT8 stencilWriteMask, D3D12_STENCIL_OP frontStencilFailOp, D3D12_STENCIL_OP frontStencilDepthFailOp, D3D12_STENCIL_OP frontStencilPassOp, D3D12_COMPARISON_FUNC frontStencilFunc, D3D12_STENCIL_OP backStencilFailOp, D3D12_STENCIL_OP backStencilDepthFailOp, D3D12_STENCIL_OP backStencilPassOp, D3D12_COMPARISON_FUNC backStencilFunc);
   ~CD3DX12_DEPTH_STENCIL_DESC();
   operator const D3D12_DEPTH_STENCIL_DESC&() const;
};
```



## <a name="members"></a><span data-ttu-id="1fa4e-107">Члены</span><span class="sxs-lookup"><span data-stu-id="1fa4e-107">Members</span></span>

<dl> <dt>

<span data-ttu-id="1fa4e-108">**CD3DX12 \_ \_ трафарета глубины \_ ()**</span><span class="sxs-lookup"><span data-stu-id="1fa4e-108">**CD3DX12\_DEPTH\_STENCIL\_DESC()**</span></span>
</dt> <dd>

<span data-ttu-id="1fa4e-109">Создает новый, неинициализированный экземпляр \_ \_ набора элементов глубины D3DX12 \_ DESC.</span><span class="sxs-lookup"><span data-stu-id="1fa4e-109">Creates a new, uninitialized, instance of a D3DX12\_DEPTH\_STENCIL\_DESC.</span></span>

</dd> <dt>

<span data-ttu-id="1fa4e-110">**CD3DX12 \_ \_ "DESC" явное описание трафарета глубины \_ (const D3D12 \_ \_ набор элементов глубины \_& o)**</span><span class="sxs-lookup"><span data-stu-id="1fa4e-110">**explicit CD3DX12\_DEPTH\_STENCIL\_DESC(const D3D12\_DEPTH\_STENCIL\_DESC& o)**</span></span>
</dt> <dd>

<span data-ttu-id="1fa4e-111">Создает новый экземпляр D3DX12 \_ \_ трафарета глубины \_ , инициализированный с содержимым другой структуры [**\_ \_ трафарета \_ глубины D3D12**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_depth_stencil_desc) .</span><span class="sxs-lookup"><span data-stu-id="1fa4e-111">Creates a new instance of a D3DX12\_DEPTH\_STENCIL\_DESC, initialized with the contents of another [**D3D12\_DEPTH\_STENCIL\_DESC**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_depth_stencil_desc) structure.</span></span>

</dd> <dt>

<span data-ttu-id="1fa4e-112">**DESC явного CD3DX12 в \_ \_ наборе элементов глубины \_ ( \_ по умолчанию CD3DX12)**</span><span class="sxs-lookup"><span data-stu-id="1fa4e-112">**explicit CD3DX12\_DEPTH\_STENCIL\_DESC(CD3DX12\_DEFAULT)**</span></span>
</dt> <dd>

<span data-ttu-id="1fa4e-113">Создает новый экземпляр D3DX12 \_ \_ трафарета глубины \_ , инициализированный параметрами по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="1fa4e-113">Creates a new instance of a D3DX12\_DEPTH\_STENCIL\_DESC, initialized with default parameters.</span></span>

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
```

</dd> <dt>

<span data-ttu-id="1fa4e-114">**явная CD3DX12 \_ \_ набор элементов глубины \_ (bool депсенабле, D3D12 \_ \_ маска записи, \_ депсвритемаск, D3D12 \_ Сравнение \_ Func ДЕПСФУНК, bool СТЕНЦИЛЕНАБЛЕ, UINT8 СтенЦилреадмаск, UINT8 стенЦилвритемаск, D3D12 \_ трафарет \_ Op frontStencilFailOp, D3D12 \_ трафарет \_ Op \_ \_ \_ \_ \_ \_ \_ \_ \_ \_ \_ \_ frontStencilDepthFailOp, D3D12 набор элементов frontStencilPassOp, D3D12 frontStencilFunc D3D12, backStencilFailOp трафарет D3D12 backStencilDepthFailOp, трафарет Func D3D12)**</span><span class="sxs-lookup"><span data-stu-id="1fa4e-114">**explicit CD3DX12\_DEPTH\_STENCIL\_DESC(BOOL depthEnable, D3D12\_DEPTH\_WRITE\_MASK depthWriteMask, D3D12\_COMPARISON\_FUNC depthFunc, BOOL stencilEnable, UINT8 stencilReadMask, UINT8 stencilWriteMask, D3D12\_STENCIL\_OP frontStencilFailOp, D3D12\_STENCIL\_OP frontStencilDepthFailOp, D3D12\_STENCIL\_OP frontStencilPassOp, D3D12\_COMPARISON\_FUNC frontStencilFunc, D3D12\_STENCIL\_OP backStencilFailOp, D3D12\_STENCIL\_OP backStencilDepthFailOp, D3D12\_STENCIL\_OP backStencilPassOp, D3D12\_COMPARISON\_FUNC backStencilFunc)**</span></span>
</dt> <dd>

<span data-ttu-id="1fa4e-115">Создает новый экземпляр D3DX12 \_ \_ набора элементов глубины \_ , инициализируя следующие параметры:</span><span class="sxs-lookup"><span data-stu-id="1fa4e-115">Creates a new instance of a D3DX12\_DEPTH\_STENCIL\_DESC, initializing the following parameters:</span></span>

<span data-ttu-id="1fa4e-116">BOOL Депсенабле</span><span class="sxs-lookup"><span data-stu-id="1fa4e-116">BOOL depthEnable</span></span>

<span data-ttu-id="1fa4e-117">[**D3D12 \_ Депсвритемаск \_ \_ маска записи глубины**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_depth_write_mask)</span><span class="sxs-lookup"><span data-stu-id="1fa4e-117">[**D3D12\_DEPTH\_WRITE\_MASK**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_depth_write_mask) depthWriteMask</span></span>

<span data-ttu-id="1fa4e-118">[**D3D12 \_ Сравнение \_ Func**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_comparison_func) депсфунк</span><span class="sxs-lookup"><span data-stu-id="1fa4e-118">[**D3D12\_COMPARISON\_FUNC**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_comparison_func) depthFunc</span></span>

<span data-ttu-id="1fa4e-119">BOOL СтенЦиленабле</span><span class="sxs-lookup"><span data-stu-id="1fa4e-119">BOOL stencilEnable</span></span>

<span data-ttu-id="1fa4e-120">UINT8 СтенЦилреадмаск</span><span class="sxs-lookup"><span data-stu-id="1fa4e-120">UINT8 stencilReadMask</span></span>

<span data-ttu-id="1fa4e-121">UINT8 СтенЦилвритемаск</span><span class="sxs-lookup"><span data-stu-id="1fa4e-121">UINT8 stencilWriteMask</span></span>

<span data-ttu-id="1fa4e-122">[**D3D12 \_ ФронтстенЦилфаилоп \_ с набором элементов**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_stencil_op)</span><span class="sxs-lookup"><span data-stu-id="1fa4e-122">[**D3D12\_STENCIL\_OP**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_stencil_op) frontStencilFailOp</span></span>

<span data-ttu-id="1fa4e-123">[**D3D12 \_ ФронтстенЦилдепсфаилоп \_ с набором элементов**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_stencil_op)</span><span class="sxs-lookup"><span data-stu-id="1fa4e-123">[**D3D12\_STENCIL\_OP**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_stencil_op) frontStencilDepthFailOp</span></span>

<span data-ttu-id="1fa4e-124">[**D3D12 \_ ФронтстенЦилпассоп \_ с набором элементов**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_stencil_op)</span><span class="sxs-lookup"><span data-stu-id="1fa4e-124">[**D3D12\_STENCIL\_OP**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_stencil_op) frontStencilPassOp</span></span>

<span data-ttu-id="1fa4e-125">[**D3D12 \_ Сравнение \_ Func**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_comparison_func) фронтстенЦилфунк</span><span class="sxs-lookup"><span data-stu-id="1fa4e-125">[**D3D12\_COMPARISON\_FUNC**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_comparison_func) frontStencilFunc</span></span>

<span data-ttu-id="1fa4e-126">[**D3D12 \_ БаккстенЦилфаилоп \_ с набором элементов**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_stencil_op)</span><span class="sxs-lookup"><span data-stu-id="1fa4e-126">[**D3D12\_STENCIL\_OP**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_stencil_op) backStencilFailOp</span></span>

<span data-ttu-id="1fa4e-127">[**D3D12 \_ БаккстенЦилдепсфаилоп \_ с набором элементов**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_stencil_op)</span><span class="sxs-lookup"><span data-stu-id="1fa4e-127">[**D3D12\_STENCIL\_OP**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_stencil_op) backStencilDepthFailOp</span></span>

<span data-ttu-id="1fa4e-128">[**D3D12 \_ БаккстенЦилпассоп \_ с набором элементов**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_stencil_op)</span><span class="sxs-lookup"><span data-stu-id="1fa4e-128">[**D3D12\_STENCIL\_OP**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_stencil_op) backStencilPassOp</span></span>

<span data-ttu-id="1fa4e-129">[**D3D12 \_ Сравнение \_ Func**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_comparison_func) баккстенЦилфунк</span><span class="sxs-lookup"><span data-stu-id="1fa4e-129">[**D3D12\_COMPARISON\_FUNC**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_comparison_func) backStencilFunc</span></span>

</dd> <dt>

<span data-ttu-id="1fa4e-130">**~ CD3DX12 \_ \_ трафарет \_ DESC ()**</span><span class="sxs-lookup"><span data-stu-id="1fa4e-130">**~CD3DX12\_DEPTH\_STENCIL\_DESC()**</span></span>
</dt> <dd>

<span data-ttu-id="1fa4e-131">Уничтожает экземпляр \_ \_ набора элементов глубины CD3DX12 \_ DESC.</span><span class="sxs-lookup"><span data-stu-id="1fa4e-131">Destroys an instance of a CD3DX12\_DEPTH\_STENCIL\_DESC.</span></span>

</dd> <dt>

<span data-ttu-id="1fa4e-132">**Константа "operator const D3D12 \_ \_ \_ -трафарет DESC& () const"**</span><span class="sxs-lookup"><span data-stu-id="1fa4e-132">**operator const D3D12\_DEPTH\_STENCIL\_DESC&() const**</span></span>
</dt> <dd>

<span data-ttu-id="1fa4e-133">Определяет & оператором передачи по ссылке для типа родительской структуры.</span><span class="sxs-lookup"><span data-stu-id="1fa4e-133">Defines the & pass-by-reference operator for the parent structure type.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="1fa4e-134">Требования</span><span class="sxs-lookup"><span data-stu-id="1fa4e-134">Requirements</span></span>



| <span data-ttu-id="1fa4e-135">Требование</span><span class="sxs-lookup"><span data-stu-id="1fa4e-135">Requirement</span></span> | <span data-ttu-id="1fa4e-136">Значение</span><span class="sxs-lookup"><span data-stu-id="1fa4e-136">Value</span></span> |
|-------------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="1fa4e-137">Header</span><span class="sxs-lookup"><span data-stu-id="1fa4e-137">Header</span></span><br/> | <dl> <span data-ttu-id="1fa4e-138"><dt>D3dx12. h</dt></span><span class="sxs-lookup"><span data-stu-id="1fa4e-138"><dt>D3dx12.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="1fa4e-139">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="1fa4e-139">See also</span></span>

<dl> <dt>

[<span data-ttu-id="1fa4e-140">**D3D12 \_ \_ трафарета \_ глубины**</span><span class="sxs-lookup"><span data-stu-id="1fa4e-140">**D3D12\_DEPTH\_STENCIL\_DESC**</span></span>](/windows/desktop/api/d3d12/ns-d3d12-d3d12_depth_stencil_desc)
</dt> <dt>

[<span data-ttu-id="1fa4e-141">Вспомогательные структуры для D3D12</span><span class="sxs-lookup"><span data-stu-id="1fa4e-141">Helper Structures for D3D12</span></span>](helper-structures-for-d3d12.md)
</dt> </dl>

 

 





