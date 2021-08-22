---
title: Загружаются неупорядоченные представления доступа
description: Подробнее о типизированной нагрузке неупорядоченного представления доступа (UAV) в Direct3D 11. Типизированная нагрузка UAV — это способность шейдера считывать из UAV с определенным DXGI_FORMAT.
ms.assetid: BA72BF21-8621-461D-8677-9DFB7D5BC6AA
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7389ba850c68129509ca6b6a835f949dd92f5541382d9fdc2243611d409ca2a0
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119124062"
---
# <a name="typed-unordered-access-view-loads"></a>Загружаются неупорядоченные представления доступа

Неупорядоченная типизированная Загрузка представления доступа (UAV) — это способность шейдера считывать из UAV с определенным \_ форматом DXGI.

-   [Обзор](#overview)
-   [Поддерживаемые форматы и вызовы API](#supported-formats-and-api-calls)
-   [Использование типизированных UAV загрузок из HLSL](#using-typed-uav-loads-from-hlsl)
-   [Связанные темы](#related-topics)

## <a name="overview"></a>Обзор

Представление неупорядоченного доступа (UAV) — это представление неупорядоченного ресурса доступа (которое может включать буферы, текстуры и массивы текстур, но без множественной выборки). UAV позволяет временно неупорядоченный доступ на чтение и запись из нескольких потоков. Это означает, что этот тип ресурса может быть считан и записан одновременно несколькими потоками без создания конфликтов памяти. Такой одновременный доступ обрабатывается с помощью [атомарных функций](/windows/desktop/direct3d11/direct3d-11-advanced-stages-cs-atomic-functions).

D3D12 и D3D 11.3 раскрывает список форматов, которые можно использовать с типизированными загрузкой UAV.

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
-   8G8 \_ Синт
-   R16 \_ UNORM
-   R16 \_ снорм
-   R8 \_ снорм
-   A8 \_ UNORM
-   B5G6R5 \_ UNORM
-   B5G5R5A1 \_ UNORM
-   B4G4R4A4 \_ UNORM

Чтобы определить поддержку для любых дополнительных форматов, вызовите [**ID3D11Device:: чеккфеатуресуппорт**](/windows/desktop/api/D3D11/nf-d3d11-id3d11device-checkfeaturesupport) с [**функцией D3D11 \_ \_ Data \_ D3D11 \_ OPTIONS2**](/windows/desktop/api/D3D11/ns-d3d11-d3d11_feature_data_d3d11_options2) Structure в качестве первого параметра. `TypedUAVLoadAdditionalFormats`Бит будет установлен, если поддерживается список "Поддерживаемые как наборы" выше. Выполните второй вызов **чеккфеатуресуппорт**, используя структуру [**\_ \_ SUPPORT2 D3D11 Data \_ \_ Format**](/windows/desktop/api/D3D11/ns-d3d11-d3d11_feature_data_format_support2) (проверка возвращаемой структуры по формату D3D12 \_ \_ SUPPORT2 UAV, \_ \_ типизированному \_ члену D3D11 [**\_ Format \_**](/windows/desktop/api/D3D11/ne-d3d11-d3d11_format_support2) SUPPORT2 enum), чтобы определить поддержку в списке поддерживаемых форматов выше, например:

``` syntax
D3D11_FEATURE_DATA_D3D11_OPTIONS2 FeatureData;
ZeroMemory(&FeatureData, sizeof(FeatureData));
HRESULT hr = pDevice->CheckFeatureSupport(D3D11_FEATURE_D3D11_OPTIONS2, &FeatureData, sizeof(FeatureData));
if (SUCCEEDED(hr))
{
    // TypedUAVLoadAdditionalFormats contains a Boolean that tells you whether the feature is supported or not
    if (FeatureData.TypedUAVLoadAdditionalFormats)
    {
        // Can assume “all-or-nothing” subset is supported (e.g. R32G32B32A32_FLOAT)
        // Can not assume other formats are supported, so we check:
        D3D11_FEATURE_DATA_FORMAT_SUPPORT2 FormatSupport;
        ZeroMemory(&FormatSupport, sizeof(FormatSupport));
        FormatSupport.InFormat = DXGI_FORMAT_R32G32_FLOAT;
        hr = pDevice->CheckFeatureSupport(D3D11_FEATURE_FORMAT_SUPPORT2, &FormatSupport, sizeof(FormatSupport));
        if (SUCCEEDED(hr) && (FormatSupport.OutFormatSupport2 & D3D11_FORMAT_SUPPORT2_UAV_TYPED_LOAD) != 0)
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

## <a name="related-topics"></a>Связанные темы

<dl> <dt>

[Функции Direct3D 11,3](direct3d-11-3-features.md)
</dt> <dt>

[Модель шейдера 5,1](/windows/desktop/direct3dhlsl/shader-model-5-1)
</dt> </dl>

 

 