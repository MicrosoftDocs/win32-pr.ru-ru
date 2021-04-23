---
title: Заданное значение ссылки на набор элементов в шейдере (графика Direct3D 11)
description: Включение шейдера пикселей для вывода значения ссылки на набор элементов вместо использования указанного API-интерфейса обеспечивает очень точный контроль над операциями с набором элементов.
ms.assetid: 6E336623-9746-4872-ADC1-C5489F53D7AE
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 65a089ec8ab56a1cf00021f97bb40cf86fe42f04
ms.sourcegitcommit: 8fa6614b715bddf14648cce36d2df22e5232801a
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/10/2020
ms.locfileid: "104340005"
---
# <a name="shader-specified-stencil-reference-value-direct3d-11-graphics"></a><span data-ttu-id="fb51f-103">Заданное значение ссылки на набор элементов в шейдере (графика Direct3D 11)</span><span class="sxs-lookup"><span data-stu-id="fb51f-103">Shader Specified Stencil Reference Value (Direct3D 11 Graphics)</span></span>

<span data-ttu-id="fb51f-104">Включение шейдера пикселей для вывода значения ссылки на набор элементов вместо использования указанного API-интерфейса обеспечивает очень точный контроль над операциями с набором элементов.</span><span class="sxs-lookup"><span data-stu-id="fb51f-104">Enabling pixel shaders to output the Stencil Reference Value, rather than using the API-specified one, enables a very fine granular control over stencil operations.</span></span>

<span data-ttu-id="fb51f-105">Заданное значение шейдера заменяет значение *ссылки на набор элементов* , ЗАданное API, для этого вызова. Это означает, что изменение влияет как на тест шаблона, так и при замене набора элементов D3D11 трафарета "трафарет" \_ \_ \_ (один член из [**D3D11 \_ набора \_**](/windows/desktop/api/D3D11/ne-d3d11-d3d11_stencil_op)элементов) используется для записи ссылочного значения в буфер шаблона.</span><span class="sxs-lookup"><span data-stu-id="fb51f-105">The shader specified value replaces the API-specified *Stencil Reference Value* for that invocation, which means the change affects both the stencil test, and when stencil op D3D11\_STENCIL\_OP\_REPLACE (one member of [**D3D11\_STENCIL\_OP**](/windows/desktop/api/D3D11/ne-d3d11-d3d11_stencil_op)) is used to write the reference value to the stencil buffer.</span></span>

<span data-ttu-id="fb51f-106">В более ранних версиях D3D11 значение ссылки на набор элементов может быть задано только методом [**ссылку ID3D11DeviceContext:: омсетдепсстенЦилстате**](/windows/desktop/api/D3D11/nf-d3d11-id3d11devicecontext-omsetdepthstencilstate) .</span><span class="sxs-lookup"><span data-stu-id="fb51f-106">In earlier versions of D3D11, the Stencil Reference Value can only be specified by the [**ID3D11DeviceContext::OMSetDepthStencilState**](/windows/desktop/api/D3D11/nf-d3d11-id3d11devicecontext-omsetdepthstencilstate) method.</span></span> <span data-ttu-id="fb51f-107">Это означает, что это значение может быть определено только для детализации по отрисовке.</span><span class="sxs-lookup"><span data-stu-id="fb51f-107">This means that this value can only be defined on a per-draw granularity.</span></span> <span data-ttu-id="fb51f-108">Эта функция D3D 11.3 позволяет разработчикам считывать и использовать значение ссылки на набор элементов ( `SV_StencilRef` ), выводимое из шейдера пикселей, что означает, что его можно указать на уровне гранулярности на пиксель или выборку.</span><span class="sxs-lookup"><span data-stu-id="fb51f-108">This D3D11.3 feature enables developers to read and use the Stencil Reference Value (`SV_StencilRef`) that is output from a pixel shader, meaning that it can be specified on a per-pixel or per-sample granularity.</span></span>

<span data-ttu-id="fb51f-109">Эта функция необязательна в D3D 11.3.</span><span class="sxs-lookup"><span data-stu-id="fb51f-109">This feature is optional in D3D11.3.</span></span> <span data-ttu-id="fb51f-110">Чтобы проверить его поддержку, проверьте `PSSpecifiedStencilRefSupported` логическое поле [**D3D11 \_ \_ данных функции \_ D3D11 \_ OPTIONS2**](/windows/desktop/api/D3D11/ns-d3d11-d3d11_feature_data_d3d11_options2) с помощью [**ID3D11Device:: чеккфеатуресуппорт**](/windows/desktop/api/D3D11/nf-d3d11-id3d11device-checkfeaturesupport) .</span><span class="sxs-lookup"><span data-stu-id="fb51f-110">To test for its support, check the `PSSpecifiedStencilRefSupported` boolean field of [**D3D11\_FEATURE\_DATA\_D3D11\_OPTIONS2**](/windows/desktop/api/D3D11/ns-d3d11-d3d11_feature_data_d3d11_options2) using [**ID3D11Device::CheckFeatureSupport**](/windows/desktop/api/D3D11/nf-d3d11-id3d11device-checkfeaturesupport)</span></span>

<span data-ttu-id="fb51f-111">Ниже приведен пример использования `SV_StencilRef` в шейдере пикселей.</span><span class="sxs-lookup"><span data-stu-id="fb51f-111">Here is an example of the use of `SV_StencilRef` in a pixel shader:</span></span>

``` syntax
uint main2(float4 c : COORD) : SV_StencilRef
{
    return uint(c.x);
}
```

## <a name="related-topics"></a><span data-ttu-id="fb51f-112">См. также</span><span class="sxs-lookup"><span data-stu-id="fb51f-112">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="fb51f-113">Функции Direct3D 11,3</span><span class="sxs-lookup"><span data-stu-id="fb51f-113">Direct3D 11.3 Features</span></span>](direct3d-11-3-features.md)
</dt> <dt>

[<span data-ttu-id="fb51f-114">Модель шейдера 5,1</span><span class="sxs-lookup"><span data-stu-id="fb51f-114">Shader Model 5.1</span></span>](/windows/desktop/direct3dhlsl/shader-model-5-1)
</dt> </dl>

 

 
