---
title: Типизированное представление неупорядоченного доступа (UAV) загружается
description: Неупорядоченная типизированная Загрузка представления доступа (UAV) — это способность шейдера считывать из UAV с определенным \_ форматом DXGI.
ms.assetid: 6106D15E-EAF6-4583-B4F2-7CC7EE30DE15
ms.localizationpriority: high
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4adfd7511590a43b7f87507c5a1e0a2a87c925b0
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "104548962"
---
# <a name="typed-unordered-access-view-uav-loads"></a>Типизированное представление неупорядоченного доступа (UAV) загружается

Неупорядоченная типизированная Загрузка представления доступа (UAV) — это способность шейдера считывать из UAV с определенным [**\_ форматом DXGI**](/windows/desktop/api/dxgiformat/ne-dxgiformat-dxgi_format).

-   [Обзор](#overview)
-   [Поддерживаемые форматы и вызовы API](#supported-formats-and-api-calls)
-   [Использование типизированных UAV загрузок из HLSL](#using-typed-uav-loads-from-hlsl)
-   [Использование UNORM и СНОРМ типизированных UAV загружается из HLSL](#using-unorm-and-snorm-typed-uav-loads-from-hlsl)
-   [Связанные темы](#related-topics)

## <a name="overview"></a>Обзор

Представление неупорядоченного доступа (UAV) — это представление неупорядоченного ресурса доступа (которое может включать буферы, текстуры и массивы текстур, но без множественной выборки). UAV позволяет временно неупорядоченный доступ на чтение и запись из нескольких потоков. Это означает, что этот тип ресурса может быть считан и записан одновременно несколькими потоками без создания конфликтов памяти. Такой одновременный доступ обрабатывается с помощью [атомарных функций](/windows/desktop/direct3d11/direct3d-11-advanced-stages-cs-atomic-functions).

D3D12 (и D3D 11.3) расширяет список форматов, которые можно использовать с типизированными загрузкой UAV.

## <a name="supported-formats-and-api-calls"></a>Поддерживаемые форматы и вызовы API

Ранее в следующих трех форматах поддерживалась типизированная UAV Загрузка и они требовались для оборудования D3D 11.0. Они поддерживаются для всех устройств D3D 11.3 и D3D12.

-   R32 \_ float
-   R32 \_ uint
-   R32 \_ Синт

Следующие форматы поддерживаются как наборы на оборудовании D3D12 или D3D 11.3, поэтому, если поддерживается любой из них, поддерживаются все.

-   R32G32B32A32 \_ float
-   R32G32B32A32 \_ uint
-   R32G32B32A32 \_ Синт
-   R16G16B16A16 \_ float
-   R16G16B16A16 \_ uint
-   R16G16B16A16 \_ Синт
-   R8G8B8A8 \_ UNORM
-   R8G8B8A8 \_ uint
-   R8G8B8A8 \_ Синт
-   R16 \_ float
-   R16 \_ uint
-   R16 \_ Синт
-   R8 \_ UNORM
-   R8 \_ uint
-   R8 \_ Синт

Следующие форматы поддерживаются по желанию и по отдельности на оборудовании D3D12 и D3D 11.3, поэтому один запрос должен быть сделан в каждом формате для проверки поддержки.

-   R16G16B16A16 \_ UNORM
-   R16G16B16A16 \_ снорм
-   R32G32 \_ float
-   R32G32 \_ uint
-   R32G32 \_ Синт
-   R10G10B10A2 \_ UNORM
-   R10G10B10A2 \_ uint
-   R11G11B10 \_ float
-   R8G8B8A8 \_ снорм
-   R16G16 \_ float
-   R16G16 \_ UNORM
-   R16G16 \_ uint
-   R16G16 \_ снорм
-   R16G16 \_ Синт
-   R8G8 \_ UNORM
-   R8G8 \_ uint
-   R8G8 \_ снорм
-   R8G8 \_ Синт
-   R16 \_ UNORM
-   R16 \_ снорм
-   R8 \_ снорм
-   A8 \_ UNORM
-   B5G6R5 \_ UNORM
-   B5G5R5A1 \_ UNORM
-   B4G4R4A4 \_ UNORM

Чтобы определить поддержку для любых дополнительных форматов, вызовите [**чеккфеатуресуппорт**](/windows/desktop/api/d3d12/nf-d3d12-id3d12device-checkfeaturesupport) с параметром [**D3D12 \_ Data Features \_ \_ D3D12 \_**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_feature_data_d3d12_options) Structure в качестве первого параметра (см. статью о [запросах возможностей](capability-querying.md)). Поле *типедуавлоададдитионалформатс* будет установлено, если поддерживается список "Поддерживаемые как наборы" выше. Выполните второй вызов **чеккфеатуресуппорт**, используя структуру [**\_ \_ \_ \_ поддержки формата данных о функциях D3D12**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_feature_data_format_support) (проверка возвращаемой структуры по D3D12 \_ Format \_ SUPPORT2 \_ UAV \_ типизированный \_ элемент Load в [**D3D12 \_ Format \_ SUPPORT2**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_format_support2) enum), чтобы определить поддержку в списке необязательных поддерживаемых форматов, например:

``` syntax
D3D12_FEATURE_DATA_D3D12_OPTIONS FeatureData;
ZeroMemory(&FeatureData, sizeof(FeatureData));
HRESULT hr = pDevice->CheckFeatureSupport(D3D12_FEATURE_D3D12_OPTIONS, &FeatureData, sizeof(FeatureData));
if (SUCCEEDED(hr))
{
    // TypedUAVLoadAdditionalFormats contains a Boolean that tells you whether the feature is supported or not
    if (FeatureData.TypedUAVLoadAdditionalFormats)
    {
        // Can assume “all-or-nothing” subset is supported (e.g. R32G32B32A32_FLOAT)
        // Cannot assume other formats are supported, so we check:
        D3D12_FEATURE_DATA_FORMAT_SUPPORT FormatSupport = {DXGI_FORMAT_R32G32_FLOAT, D3D12_FORMAT_SUPPORT1_NONE, D3D12_FORMAT_SUPPORT2_NONE};
        hr = pDevice->CheckFeatureSupport(D3D12_FEATURE_FORMAT_SUPPORT, &FormatSupport, sizeof(FormatSupport));
        if (SUCCEEDED(hr) && (FormatSupport.Support2 & D3D12_FORMAT_SUPPORT2_UAV_TYPED_LOAD) != 0)
        {
            // DXGI_FORMAT_R32G32_FLOAT supports UAV Typed Load!
        }
    }
}
```

## <a name="using-typed-uav-loads-from-hlsl"></a>Использование типизированных UAV загрузок из HLSL

Для типизированного Уавс в качестве флага HLSL для \_ шейдера D3D \_ требуется \_ типизированная \_ UAV \_ загрузить \_ Дополнительные \_ форматы.

Ниже приведен пример кода шейдера для обработки типизированной UAV нагрузки:

``` syntax
RWTexture2D<float4> uav1;
uint2 coord;
float4 main() : SV_Target
{
  return uav1.Load(coord);
}
```

## <a name="using-unorm-and-snorm-typed-uav-loads-from-hlsl"></a>Использование UNORM и СНОРМ типизированных UAV загружается из HLSL

При использовании типизированных UAV загрузок для чтения из ресурса UNORM или СНОРМ необходимо правильно объявить тип элемента объекта HLSL в значение `unorm` или `snorm` . Он задается как неопределенное поведение для несоответствия типа элемента, объявленного в HLSL, с базовым типом данных ресурса. Например, если используется типизированная UAV загружается в буферный ресурс с R8 \_ UNORM Data, необходимо объявить тип элемента следующим образом `unorm float` :

``` syntax
RWBuffer<unorm float> uav;
```

## <a name="related-topics"></a>Связанные темы

<dl> <dt>

[Отрисовка](rendering.md)
</dt> <dt>

[Привязка ресурсов](resource-binding.md)
</dt> <dt>

[Привязка ресурсов в HLSL](resource-binding-in-hlsl.md)
</dt> <dt>

[Модель шейдера 5,1](/windows/desktop/direct3dhlsl/shader-model-5-1)
</dt> <dt>

[Указание корневых подписей в HLSL](specifying-root-signatures-in-hlsl.md)
</dt> </dl>

 

 