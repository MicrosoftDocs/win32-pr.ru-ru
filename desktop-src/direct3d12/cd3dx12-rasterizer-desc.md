---
title: Структура CD3DX12_RASTERIZER_DESC (D3dx12. h)
description: Вспомогательная структура, позволяющая легко инициализировать структуру D3D12 средства программной \_ прорисовки \_ .
ms.assetid: 28AA8256-1CAF-484F-B219-0F0461BA947C
keywords:
- Структура CD3DX12_RASTERIZER_DESC
topic_type:
- apiref
api_name:
- CD3DX12_RASTERIZER_DESC
api_location:
- d3dx12.h
api_type:
- HeaderDef
ms.localizationpriority: low
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 078b9e92d25cb5309b4cd97d35586192a37eed90
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/15/2021
ms.locfileid: "105713516"
---
# <a name="cd3dx12_rasterizer_desc-structure"></a><span data-ttu-id="c853f-104">Структура CD3DX12 средства программной \_ прорисовки \_</span><span class="sxs-lookup"><span data-stu-id="c853f-104">CD3DX12\_RASTERIZER\_DESC structure</span></span>

<span data-ttu-id="c853f-105">Вспомогательная структура, позволяющая легко инициализировать структуру D3D12 средства программной [**\_ прорисовки \_**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_rasterizer_desc) .</span><span class="sxs-lookup"><span data-stu-id="c853f-105">A helper structure to enable easy initialization of a [**D3D12\_RASTERIZER\_DESC**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_rasterizer_desc) structure.</span></span>

## <a name="syntax"></a><span data-ttu-id="c853f-106">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="c853f-106">Syntax</span></span>


```C++
struct CD3DX12_RASTERIZER_DESC  : public D3D12_RASTERIZER_DESC{
   CD3DX12_RASTERIZER_DESC();
   explicit CD3DX12_RASTERIZER_DESC(const D3D12_RASTERIZER_DESC& o);
   explicit CD3DX12_RASTERIZER_DESC(CD3DX12_DEFAULT);
   explicit CD3DX12_RASTERIZER_DESC(D3D12_FILL_MODE fillMode, D3D12_CULL_MODE cullMode, BOOL frontCounterClockwise, INT depthBias, FLOAT depthBiasClamp, FLOAT slopeScaledDepthBias, BOOL depthClipEnable, BOOL multisampleEnable, BOOL antialiasedLineEnable, UINT forcedSampleCount, D3D12_CONSERVATIVE_RASTERIZATION_MODE conservativeRaster);
   ~CD3DX12_RASTERIZER_DESC();
   operator const D3D12_RASTERIZER_DESC&() const;
};
```



## <a name="members"></a><span data-ttu-id="c853f-107">Члены</span><span class="sxs-lookup"><span data-stu-id="c853f-107">Members</span></span>

<dl> <dt>

<span data-ttu-id="c853f-108">**CD3DX12 средство программной \_ прорисовки \_ DESC ()**</span><span class="sxs-lookup"><span data-stu-id="c853f-108">**CD3DX12\_RASTERIZER\_DESC()**</span></span>
</dt> <dd>

<span data-ttu-id="c853f-109">Создает новый, неинициализированный экземпляр экземпляра средства создания программной \_ прорисовки CD3DX12 \_ DESC.</span><span class="sxs-lookup"><span data-stu-id="c853f-109">Creates a new, uninitialized, instance of a CD3DX12\_RASTERIZER\_DESC.</span></span>

</dd> <dt>

<span data-ttu-id="c853f-110">**явный CD3DX12 средство программной \_ прорисовки \_ DESC (const D3D12 средство \_ прорисовки \_ DESC& o)**</span><span class="sxs-lookup"><span data-stu-id="c853f-110">**explicit CD3DX12\_RASTERIZER\_DESC(const D3D12\_RASTERIZER\_DESC& o)**</span></span>
</dt> <dd>

<span data-ttu-id="c853f-111">Создает новый экземпляр CD3DX12 средства \_ прорисовки \_ DESC, инициализированного с содержимым другой структуры средства [**\_ прорисовки D3D12 ( \_ DESC**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_rasterizer_desc) ).</span><span class="sxs-lookup"><span data-stu-id="c853f-111">Creates a new instance of a CD3DX12\_RASTERIZER\_DESC, initialized with the contents of another [**D3D12\_RASTERIZER\_DESC**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_rasterizer_desc) structure.</span></span>

</dd> <dt>

<span data-ttu-id="c853f-112">**явное CD3DX12 средство программной \_ прорисовки \_ DESC (CD3DX12 \_ по умолчанию)**</span><span class="sxs-lookup"><span data-stu-id="c853f-112">**explicit CD3DX12\_RASTERIZER\_DESC(CD3DX12\_DEFAULT)**</span></span>
</dt> <dd>

<span data-ttu-id="c853f-113">Создает новый экземпляр CD3DX12 средства \_ прорисовки \_ DESC, инициализируемый параметрами по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="c853f-113">Creates a new instance of a CD3DX12\_RASTERIZER\_DESC, initialized with default parameters.</span></span>

``` syntax
        FillMode = D3D12_FILL_MODE_SOLID;  
        CullMode = D3D12_CULL_MODE_BACK;  
        FrontCounterClockwise = FALSE;  
        DepthBias = D3D12_DEFAULT_DEPTH_BIAS;  
        DepthBiasClamp = D3D12_DEFAULT_DEPTH_BIAS_CLAMP;  
        SlopeScaledDepthBias = D3D12_DEFAULT_SLOPE_SCALED_DEPTH_BIAS;  
        DepthClipEnable = TRUE;  
        MultisampleEnable = FALSE;  
        AntialiasedLineEnable = FALSE;  
        ForcedSampleCount = 0;  
        ConservativeRaster = D3D12_CONSERVATIVE_RASTERIZATION_MODE_OFF;  
```

</dd> <dt>

<span data-ttu-id="c853f-114">**Explicit CD3DX12, \_ \_ DESC, \_ \_ ФИЛЛМОДЕ, D3D12 режим D3D12, \_ \_ Куллмоде, bool Фронткаунтерклокквисе, int Депсбиас, float Депсбиаскламп, float Слопескаледдепсбиас, BOOL depthClipEnable, bool MultisampleEnable, bool antialiasedLineEnable, uint forcedSampleCount, D3D12 \_ консервативный \_ \_ режим растрирования conservativeRaster)**</span><span class="sxs-lookup"><span data-stu-id="c853f-114">**explicit CD3DX12\_RASTERIZER\_DESC(D3D12\_FILL\_MODE fillMode, D3D12\_CULL\_MODE cullMode, BOOL frontCounterClockwise, INT depthBias, FLOAT depthBiasClamp, FLOAT slopeScaledDepthBias, BOOL depthClipEnable, BOOL multisampleEnable, BOOL antialiasedLineEnable, UINT forcedSampleCount, D3D12\_CONSERVATIVE\_RASTERIZATION\_MODE conservativeRaster)**</span></span>
</dt> <dd>

<span data-ttu-id="c853f-115">Создает новый экземпляр CD3DX12 средства создания программной \_ прорисовки \_ DESC, инициализируя следующие параметры:</span><span class="sxs-lookup"><span data-stu-id="c853f-115">Creates a new instance of a CD3DX12\_RASTERIZER\_DESC, initializing the following parameters:</span></span>

<span data-ttu-id="c853f-116">[**D3D12 \_ Филлмоде \_ режима заполнения**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_fill_mode)</span><span class="sxs-lookup"><span data-stu-id="c853f-116">[**D3D12\_FILL\_MODE**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_fill_mode) fillMode</span></span>

<span data-ttu-id="c853f-117">[**D3D12 \_ Куллмоде \_ режима отбора**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_cull_mode)</span><span class="sxs-lookup"><span data-stu-id="c853f-117">[**D3D12\_CULL\_MODE**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_cull_mode) cullMode</span></span>

<span data-ttu-id="c853f-118">BOOL Фронткаунтерклокквисе</span><span class="sxs-lookup"><span data-stu-id="c853f-118">BOOL frontCounterClockwise</span></span>

<span data-ttu-id="c853f-119">INT Депсбиас</span><span class="sxs-lookup"><span data-stu-id="c853f-119">INT depthBias</span></span>

<span data-ttu-id="c853f-120">Депсбиаскламп с плавающей запятой</span><span class="sxs-lookup"><span data-stu-id="c853f-120">FLOAT depthBiasClamp</span></span>

<span data-ttu-id="c853f-121">Слопескаледдепсбиас с плавающей запятой</span><span class="sxs-lookup"><span data-stu-id="c853f-121">FLOAT slopeScaledDepthBias</span></span>

<span data-ttu-id="c853f-122">BOOL Депсклипенабле</span><span class="sxs-lookup"><span data-stu-id="c853f-122">BOOL depthClipEnable</span></span>

<span data-ttu-id="c853f-123">BOOL Мултисамплинабле</span><span class="sxs-lookup"><span data-stu-id="c853f-123">BOOL multisampleEnable</span></span>

<span data-ttu-id="c853f-124">BOOL Антиалиаседлининабле</span><span class="sxs-lookup"><span data-stu-id="c853f-124">BOOL antialiasedLineEnable</span></span>

<span data-ttu-id="c853f-125">UINT Форцедсамплекаунт</span><span class="sxs-lookup"><span data-stu-id="c853f-125">UINT forcedSampleCount</span></span>

<span data-ttu-id="c853f-126">[**D3D12 \_ КОНСЕРВАТИВНый \_ \_ режим растрирования**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_conservative_rasterization_mode) консервативерастер</span><span class="sxs-lookup"><span data-stu-id="c853f-126">[**D3D12\_CONSERVATIVE\_RASTERIZATION\_MODE**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_conservative_rasterization_mode) conservativeRaster</span></span>

</dd> <dt>

<span data-ttu-id="c853f-127">**~ CD3DX12ное средство программной \_ прорисовки \_ DESC ()**</span><span class="sxs-lookup"><span data-stu-id="c853f-127">**~CD3DX12\_RASTERIZER\_DESC()**</span></span>
</dt> <dd>

<span data-ttu-id="c853f-128">Уничтожает экземпляр CD3DX12 средства \_ прорисовки данных \_ DESC.</span><span class="sxs-lookup"><span data-stu-id="c853f-128">Destroys an instance of a CD3DX12\_RASTERIZER\_DESC.</span></span>

</dd> <dt>

<span data-ttu-id="c853f-129">**Оператор const D3D12 средство программной \_ прорисовки \_ DESC& () const**</span><span class="sxs-lookup"><span data-stu-id="c853f-129">**operator const D3D12\_RASTERIZER\_DESC&() const**</span></span>
</dt> <dd>

<span data-ttu-id="c853f-130">Определяет & оператором передачи по ссылке для типа родительской структуры.</span><span class="sxs-lookup"><span data-stu-id="c853f-130">Defines the & pass-by-reference operator for the parent structure type.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="c853f-131">Требования</span><span class="sxs-lookup"><span data-stu-id="c853f-131">Requirements</span></span>



| <span data-ttu-id="c853f-132">Требование</span><span class="sxs-lookup"><span data-stu-id="c853f-132">Requirement</span></span> | <span data-ttu-id="c853f-133">Значение</span><span class="sxs-lookup"><span data-stu-id="c853f-133">Value</span></span> |
|-------------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="c853f-134">Header</span><span class="sxs-lookup"><span data-stu-id="c853f-134">Header</span></span><br/> | <dl> <span data-ttu-id="c853f-135"><dt>D3dx12. h</dt></span><span class="sxs-lookup"><span data-stu-id="c853f-135"><dt>D3dx12.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="c853f-136">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="c853f-136">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c853f-137">**D3D12 средство программной \_ прорисовки \_ DESC**</span><span class="sxs-lookup"><span data-stu-id="c853f-137">**D3D12\_RASTERIZER\_DESC**</span></span>](/windows/desktop/api/d3d12/ns-d3d12-d3d12_rasterizer_desc)
</dt> <dt>

[<span data-ttu-id="c853f-138">Вспомогательные структуры для D3D12</span><span class="sxs-lookup"><span data-stu-id="c853f-138">Helper Structures for D3D12</span></span>](helper-structures-for-d3d12.md)
</dt> </dl>

 

 





