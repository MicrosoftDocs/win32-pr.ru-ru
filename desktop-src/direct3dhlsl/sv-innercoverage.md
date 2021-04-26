---
title: SV_InnerCoverage
description: ОКП \_ инпутковераже представляет неполную оценочную информацию о растеризации (т. е. гарантируется, что точка полностью охватывается).
ms.assetid: 5BB3C3FB-E5ED-4395-B389-300DE67C984B
keywords:
- SV_InnerCoverage HLSL
topic_type:
- apiref
api_name:
- SV_InnerCoverage
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e1ac278f0524446b5171ef278e169fbe7c3a082f
ms.sourcegitcommit: b6fe9acffad983c14864b8fe0296f6025cb1f961
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/26/2021
ms.locfileid: "107996971"
---
# <a name="sv_innercoverage"></a><span data-ttu-id="7416e-104">ОКП \_ иннерковераже</span><span class="sxs-lookup"><span data-stu-id="7416e-104">SV\_InnerCoverage</span></span>

<span data-ttu-id="7416e-105">ОКП \_ инпутковераже представляет неполную оценочную информацию о растеризации (т. е. гарантируется, что точка полностью охватывается).</span><span class="sxs-lookup"><span data-stu-id="7416e-105">SV\_InputCoverage represents underestimated conservative rasterization information (i.e. whether a pixel is guaranteed-to-be-fully covered).</span></span>

## <a name="type"></a><span data-ttu-id="7416e-106">Тип</span><span class="sxs-lookup"><span data-stu-id="7416e-106">Type</span></span>



|      |
|------|
| <span data-ttu-id="7416e-107">Тип</span><span class="sxs-lookup"><span data-stu-id="7416e-107">Type</span></span> |
| <span data-ttu-id="7416e-108">uint</span><span class="sxs-lookup"><span data-stu-id="7416e-108">uint</span></span> |



 

## <a name="remarks"></a><span data-ttu-id="7416e-109">Примечания</span><span class="sxs-lookup"><span data-stu-id="7416e-109">Remarks</span></span>

<span data-ttu-id="7416e-110">Это значение, созданное системой, является обязательным для поддержки уровня 3 и доступно только на этом уровне.</span><span class="sxs-lookup"><span data-stu-id="7416e-110">This system generated value is required for tier 3 support, and is only available in that tier.</span></span> <span data-ttu-id="7416e-111">Эти входные данные являются взаимоисключающими с покрытием "ОКП" \_ . они не могут использоваться одновременно.</span><span class="sxs-lookup"><span data-stu-id="7416e-111">This input is mutually exclusive with SV\_Coverage - both cannot be used.</span></span>

<span data-ttu-id="7416e-112">Чтобы получить доступ к SV \_ иннерковераже, он должен быть объявлен как отдельный компонент из одного из входных регистров шейдера пикселей.</span><span class="sxs-lookup"><span data-stu-id="7416e-112">To access SV\_InnerCoverage, it must be declared as a single component out of one of the pixel shader input registers.</span></span> <span data-ttu-id="7416e-113">Режим интерполяции в объявлении должен быть константой (интерполяция не применяется).</span><span class="sxs-lookup"><span data-stu-id="7416e-113">The interpolation mode on the declaration must be constant (interpolation does not apply).</span></span>

<span data-ttu-id="7416e-114">Консервативная растрирование доступна как в D3D 11.3, так и в D3D12.</span><span class="sxs-lookup"><span data-stu-id="7416e-114">Conservative rasterization is available in both D3D11.3 and D3D12.</span></span> <span data-ttu-id="7416e-115">Перейдите к</span><span class="sxs-lookup"><span data-stu-id="7416e-115">Refer to:</span></span>

-   [<span data-ttu-id="7416e-116">11.3а в D3D, консервативная растрирование</span><span class="sxs-lookup"><span data-stu-id="7416e-116">D3D11.3 Conservative Rasterization</span></span>](/windows/desktop/direct3d11/conservative-rasterization)
-   [<span data-ttu-id="7416e-117">D3D12 консервативная растрирование</span><span class="sxs-lookup"><span data-stu-id="7416e-117">D3D12 Conservative Rasterization</span></span>](/windows/desktop/direct3d12/conservative-rasterization)

## <a name="see-also"></a><span data-ttu-id="7416e-118">См. также</span><span class="sxs-lookup"><span data-stu-id="7416e-118">See also</span></span>

<dl> <dt>

[<span data-ttu-id="7416e-119">Модель шейдера 5</span><span class="sxs-lookup"><span data-stu-id="7416e-119">Shader Model 5</span></span>](d3d11-graphics-reference-sm5.md)
</dt> <dt>

[<span data-ttu-id="7416e-120">Системные значения модели шейдеров 5,1</span><span class="sxs-lookup"><span data-stu-id="7416e-120">Shader Model 5.1 System Values</span></span>](shader-model-5-1-system-values.md)
</dt> </dl>

 

 
