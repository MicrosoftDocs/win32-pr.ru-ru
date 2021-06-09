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
ms.openlocfilehash: 168f90c17c9e6837d696ebb6dac8f39dc6dfb366
ms.sourcegitcommit: adba238660d8a5f4fe98fc6f5d105d56aac3a400
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/09/2021
ms.locfileid: "111826628"
---
# <a name="sv_innercoverage"></a><span data-ttu-id="28dbb-104">ОКП \_ иннерковераже</span><span class="sxs-lookup"><span data-stu-id="28dbb-104">SV\_InnerCoverage</span></span>

<span data-ttu-id="28dbb-105">ОКП \_ инпутковераже представляет неполную оценочную информацию о растеризации (т. е. гарантируется, что точка полностью охватывается).</span><span class="sxs-lookup"><span data-stu-id="28dbb-105">SV\_InputCoverage represents underestimated conservative rasterization information (i.e. whether a pixel is guaranteed-to-be-fully covered).</span></span>

## <a name="type"></a><span data-ttu-id="28dbb-106">Тип</span><span class="sxs-lookup"><span data-stu-id="28dbb-106">Type</span></span>



| <span data-ttu-id="28dbb-107">Тип</span><span class="sxs-lookup"><span data-stu-id="28dbb-107">Type</span></span>     |
|------|
| <span data-ttu-id="28dbb-108">uint</span><span class="sxs-lookup"><span data-stu-id="28dbb-108">uint</span></span> |



 

## <a name="remarks"></a><span data-ttu-id="28dbb-109">Remarks</span><span class="sxs-lookup"><span data-stu-id="28dbb-109">Remarks</span></span>

<span data-ttu-id="28dbb-110">Это значение, созданное системой, является обязательным для поддержки уровня 3 и доступно только на этом уровне.</span><span class="sxs-lookup"><span data-stu-id="28dbb-110">This system generated value is required for tier 3 support, and is only available in that tier.</span></span> <span data-ttu-id="28dbb-111">Эти входные данные являются взаимоисключающими с покрытием "ОКП" \_ . они не могут использоваться одновременно.</span><span class="sxs-lookup"><span data-stu-id="28dbb-111">This input is mutually exclusive with SV\_Coverage - both cannot be used.</span></span>

<span data-ttu-id="28dbb-112">Чтобы получить доступ к SV \_ иннерковераже, он должен быть объявлен как отдельный компонент из одного из входных регистров шейдера пикселей.</span><span class="sxs-lookup"><span data-stu-id="28dbb-112">To access SV\_InnerCoverage, it must be declared as a single component out of one of the pixel shader input registers.</span></span> <span data-ttu-id="28dbb-113">Режим интерполяции в объявлении должен быть константой (интерполяция не применяется).</span><span class="sxs-lookup"><span data-stu-id="28dbb-113">The interpolation mode on the declaration must be constant (interpolation does not apply).</span></span>

<span data-ttu-id="28dbb-114">Консервативная растрирование доступна как в D3D 11.3, так и в D3D12.</span><span class="sxs-lookup"><span data-stu-id="28dbb-114">Conservative rasterization is available in both D3D11.3 and D3D12.</span></span> <span data-ttu-id="28dbb-115">Перейдите к</span><span class="sxs-lookup"><span data-stu-id="28dbb-115">Refer to:</span></span>

-   [<span data-ttu-id="28dbb-116">11.3а в D3D, консервативная растрирование</span><span class="sxs-lookup"><span data-stu-id="28dbb-116">D3D11.3 Conservative Rasterization</span></span>](/windows/desktop/direct3d11/conservative-rasterization)
-   [<span data-ttu-id="28dbb-117">D3D12 консервативная растрирование</span><span class="sxs-lookup"><span data-stu-id="28dbb-117">D3D12 Conservative Rasterization</span></span>](/windows/desktop/direct3d12/conservative-rasterization)

## <a name="see-also"></a><span data-ttu-id="28dbb-118">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="28dbb-118">See also</span></span>

<dl> <dt>

[<span data-ttu-id="28dbb-119">Модель шейдера 5</span><span class="sxs-lookup"><span data-stu-id="28dbb-119">Shader Model 5</span></span>](d3d11-graphics-reference-sm5.md)
</dt> <dt>

[<span data-ttu-id="28dbb-120">Системные значения модели шейдеров 5,1</span><span class="sxs-lookup"><span data-stu-id="28dbb-120">Shader Model 5.1 System Values</span></span>](shader-model-5-1-system-values.md)
</dt> </dl>

 

 
