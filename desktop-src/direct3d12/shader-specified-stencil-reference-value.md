---
title: Заданное значение ссылки на набор элементов в шейдере (графика Direct3D 12)
description: Включение шейдера пикселей для вывода значения ссылки на набор элементов вместо использования указанного API-интерфейса обеспечивает очень точный контроль над операциями с набором элементов.
ms.assetid: F58B1930-F12E-4FA4-A15C-A3C2B8705033
ms.localizationpriority: high
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f6a8b7697cc06594b3e2ffc717cbded9e6832129
ms.sourcegitcommit: 8fa6614b715bddf14648cce36d2df22e5232801a
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/10/2020
ms.locfileid: "104548987"
---
# <a name="shader-specified-stencil-reference-value-direct3d-12-graphics"></a><span data-ttu-id="adcc5-103">Заданное значение ссылки на набор элементов в шейдере (графика Direct3D 12)</span><span class="sxs-lookup"><span data-stu-id="adcc5-103">Shader Specified Stencil Reference Value (Direct3D 12 Graphics)</span></span>

<span data-ttu-id="adcc5-104">Включение шейдера пикселей для вывода значения ссылки на набор элементов вместо использования указанного API-интерфейса обеспечивает очень точный контроль над операциями с набором элементов.</span><span class="sxs-lookup"><span data-stu-id="adcc5-104">Enabling pixel shaders to output the Stencil Reference Value, rather than using the API-specified one, enables a very fine granular control over stencil operations.</span></span>

<span data-ttu-id="adcc5-105">Значение ссылки на набор элементов обычно задается методом [**ID3D12GraphicsCommandList:: омсетстенЦилреф**](/windows/desktop/api/d3d12/nf-d3d12-id3d12graphicscommandlist-omsetstencilref) .</span><span class="sxs-lookup"><span data-stu-id="adcc5-105">The Stencil Reference Value is normally specified by the [**ID3D12GraphicsCommandList::OMSetStencilRef**](/windows/desktop/api/d3d12/nf-d3d12-id3d12graphicscommandlist-omsetstencilref) method.</span></span> <span data-ttu-id="adcc5-106">Этот метод задает значение ссылки на набор элементов на уровне детализации.</span><span class="sxs-lookup"><span data-stu-id="adcc5-106">This method sets the stencil reference value on a per-draw granularity.</span></span> <span data-ttu-id="adcc5-107">Однако это значение может быть перезаписано шейдером пикселей.</span><span class="sxs-lookup"><span data-stu-id="adcc5-107">However, this value can be overwritten by the pixel shader.</span></span>

<span data-ttu-id="adcc5-108">Эта функция D3D12 (и D3D 11.3) позволяет разработчикам считывать и использовать значение ссылки на набор элементов (*SV \_ стенЦилреф*), выводимое из шейдера пикселей, что позволяет выполнять детализацию по пикселям или образцам.</span><span class="sxs-lookup"><span data-stu-id="adcc5-108">This D3D12 (and D3D11.3) feature enables developers to read and use the Stencil Reference Value (*SV\_StencilRef*) that is output from a pixel shader, enabling a per-pixel or per-sample granularity.</span></span>

<span data-ttu-id="adcc5-109">Заданное значение шейдера заменяет значение ссылки, заданное API, для этого вызова. Это означает, что изменение влияет как на тест шаблона, так и при выполнении операции с набором элементов D3D12 \_ набор элементов, \_ \_ заменяя (один член из [**D3D12 \_ набора \_**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_stencil_op)элементов), для записи ссылочного значения в буфер шаблона.</span><span class="sxs-lookup"><span data-stu-id="adcc5-109">The shader specified value replaces the API-specified reference value for that invocation, which means the change affects both the stencil test, and when the stencil operation D3D12\_STENCIL\_OP\_REPLACE (one member of [**D3D12\_STENCIL\_OP**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_stencil_op)) is used to write the reference value to the stencil buffer.</span></span>

<span data-ttu-id="adcc5-110">Эта функция необязательна в D3D12 и 11.3 D3D.</span><span class="sxs-lookup"><span data-stu-id="adcc5-110">This feature is optional in both D3D12 and D3D11.3.</span></span> <span data-ttu-id="adcc5-111">Чтобы проверить поддержку, проверьте логическое поле *псспеЦифиедстенЦилрефсуппортед* в [**\_ \_ \_ \_ параметре D3D12 данных функции D3D12**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_feature_data_d3d12_options) с помощью [**чеккфеатуресуппорт**](/windows/desktop/api/d3d12/nf-d3d12-id3d12device-checkfeaturesupport).</span><span class="sxs-lookup"><span data-stu-id="adcc5-111">To test for its support, check the *PSSpecifiedStencilRefSupported* boolean field of [**D3D12\_FEATURE\_DATA\_D3D12\_OPTIONS**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_feature_data_d3d12_options) using [**CheckFeatureSupport**](/windows/desktop/api/d3d12/nf-d3d12-id3d12device-checkfeaturesupport).</span></span>

<span data-ttu-id="adcc5-112">Ниже приведен пример использования *SV \_ стенЦилреф* в построителе пикселей.</span><span class="sxs-lookup"><span data-stu-id="adcc5-112">Here is an example of the use of *SV\_StencilRef* in a pixel shader:</span></span>

``` syntax
uint main2(float4 c : COORD) : SV_StencilRef
{
    return uint(c.x);
}
```

## <a name="related-topics"></a><span data-ttu-id="adcc5-113">Связанные темы</span><span class="sxs-lookup"><span data-stu-id="adcc5-113">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="adcc5-114">Отрисовка</span><span class="sxs-lookup"><span data-stu-id="adcc5-114">Rendering</span></span>](rendering.md)
</dt> <dt>

[<span data-ttu-id="adcc5-115">Привязка ресурсов в HLSL</span><span class="sxs-lookup"><span data-stu-id="adcc5-115">Resource Binding in HLSL</span></span>](resource-binding-in-hlsl.md)
</dt> <dt>

[<span data-ttu-id="adcc5-116">Модель шейдера 5,1</span><span class="sxs-lookup"><span data-stu-id="adcc5-116">Shader Model 5.1</span></span>](/windows/desktop/direct3dhlsl/shader-model-5-1)
</dt> <dt>

[<span data-ttu-id="adcc5-117">Указание корневых подписей в HLSL</span><span class="sxs-lookup"><span data-stu-id="adcc5-117">Specifying Root Signatures in HLSL</span></span>](specifying-root-signatures-in-hlsl.md)
</dt> </dl>

 

 
