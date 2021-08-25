---
title: Запросы возможностей
description: 'Приложение может обнаружить уровень поддержки привязки ресурсов и многие другие функции с помощью вызова ID3D12Device \: \: чеккфеатуресуппорт.'
ms.assetid: ECBAF8EF-5D91-46D8-9D6E-A7FA4203B9F8
ms.date: 11/26/2018
ms.localizationpriority: high
ms.topic: article
ms.openlocfilehash: a99174515883f8995167a7b866ab1ef8b77b56f7a0be2bb83f960abd06e47713
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119851404"
---
# <a name="capability-querying"></a>Запросы возможностей

Приложение может обнаружить уровень поддержки привязки ресурсов (а также уровень поддержки многих других функций) с помощью вызова [**ID3D12Device:: чеккфеатуресуппорт**](/windows/desktop/api/d3d12/nf-d3d12-id3d12device-checkfeaturesupport).

## <a name="how-to-query-for-the-resource-binding-tier"></a>Запрос уровня привязки ресурсов

В первом примере основное внимание уделяется привязке ресурсов. Каждый уровень привязки ресурсов является надмножеством более низких уровней функциональности, поэтому код, работающий на данном уровне, работает на любом более высоком уровне.

Уровни привязки ресурсов являются константами в перечислении [**D3D12_RESOURCE_BINDING_TIER**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_resource_binding_tier) .

Чтобы запросить уровень привязки ресурсов, используйте следующий код. Этот пример кода демонстрирует общий шаблон для запроса любого из различных видов поддержки функций.

```cppwinrt
D3D12_RESOURCE_BINDING_TIER get_resource_binding_tier(::ID3D12Device* pIDevice)
{
    D3D12_FEATURE_DATA_D3D12_OPTIONS featureSupport{};
    winrt::check_hresult(
        pIDevice->CheckFeatureSupport(D3D12_FEATURE_D3D12_OPTIONS, &featureSupport, sizeof(featureSupport))
    );

    switch (featureSupport.ResourceBindingTier)
    {
    case D3D12_RESOURCE_BINDING_TIER_1:
        // Tier 1 is supported.
        break;

    case D3D12_RESOURCE_BINDING_TIER_2:
        // Tiers 1 and 2 are supported.
        break;

    case D3D12_RESOURCE_BINDING_TIER_3:
        // Tiers 1, 2, and 3 are supported.
        break;
    }

    return featureSupport.ResourceBindingTier;
}
```

Обратите внимание, что любая передаваемая Перечисляемая константа (в данном случае [**D3D12_FEATURE_D3D12_OPTIONS**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_feature)) имеет соответствующую структуру данных, которая получает сведения об этой функции или наборе функций (в данном случае [**D3D12_FEATURE_DATA_D3D12_OPTIONS**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_feature_data_d3d12_options)). Всегда передавайте указатель на структуру, которая соответствует переданной перечисленной константе.

## <a name="how-to-query-for-any-feature-level"></a>Как запросить любой уровень функций

Так же как и уровень привязки ресурсов, существует множество других функций, уровень поддержки которых можно запросить, используя тот же шаблон, который приведен в приведенном выше примере кода. Вы просто передаете другую константу из перечисления [**D3D12_FEATURE**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_feature) в [**ID3D12Device:: чеккфеатуресуппорт**](/windows/desktop/api/d3d12/nf-d3d12-id3d12device-checkfeaturesupport) (чтобы сообщить API, какую функцию следует запрашивать информацию о поддержке), и передаете указатель на экземпляр соответствующей структуры (для получения запрошенной информации).

- Передайте **D3D12_FEATURE_ARCHITECTURE** и [**D3D12_FEATURE_DATA_ARCHITECTURE**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_feature_data_architecture).
- Передайте **D3D12_FEATURE_ARCHITECTURE1** и [**D3D12_FEATURE_DATA_ARCHITECTURE1**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_feature_data_architecture1).
- Передайте **D3D12_FEATURE_COMMAND_QUEUE_PRIORITY** и [**D3D12_FEATURE_DATA_COMMAND_QUEUE_PRIORITY**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_feature_data_command_queue_priority).
- Передайте **D3D12_FEATURE_CROSS_NODE** и [**D3D12_FEATURE_DATA_CROSS_NODE**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_feature_data_cross_node).
- Передайте **D3D12_FEATURE_D3D12_OPTIONS** и [**D3D12_FEATURE_DATA_D3D12_OPTIONS**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_feature_data_d3d12_options).
- Передайте **D3D12_FEATURE_D3D12_OPTIONS1** и [**D3D12_FEATURE_DATA_D3D12_OPTIONS1**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_feature_data_d3d12_options1).
- Передайте **D3D12_FEATURE_D3D12_OPTIONS2** и [**D3D12_FEATURE_DATA_D3D12_OPTIONS2**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_feature_data_d3d12_options2).
- Передайте **D3D12_FEATURE_D3D12_OPTIONS3** и [**D3D12_FEATURE_DATA_D3D12_OPTIONS3**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_feature_data_d3d12_options3).
- Передайте **D3D12_FEATURE_D3D12_OPTIONS4** и [**D3D12_FEATURE_DATA_D3D12_OPTIONS4**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_feature_data_d3d12_options4).
- Передайте **D3D12_FEATURE_D3D12_OPTIONS5** и [**D3D12_FEATURE_DATA_D3D12_OPTIONS5**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_feature_data_d3d12_options5).
- Передайте **D3D12_FEATURE_EXISTING_HEAPS** и [**D3D12_FEATURE_DATA_EXISTING_HEAPS**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_feature_data_existing_heaps).
- Передайте **D3D12_FEATURE_FEATURE_LEVELS** и [**D3D12_FEATURE_DATA_FEATURE_LEVELS**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_feature_data_feature_levels).
- Передайте **D3D12_FEATURE_FORMAT_INFO** и [**D3D12_FEATURE_DATA_FORMAT_INFO**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_feature_data_format_info).
- Передайте **D3D12_FEATURE_FORMAT_SUPPORT** и [**D3D12_FEATURE_DATA_FORMAT_SUPPORT**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_feature_data_format_support).
- Передайте **D3D12_FEATURE_GPU_VIRTUAL_ADDRESS_SUPPORT** и [**D3D12_FEATURE_DATA_GPU_VIRTUAL_ADDRESS_SUPPORT**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_feature_data_gpu_virtual_address_support).
- Передайте **D3D12_FEATURE_MULTISAMPLE_QUALITY_LEVELS** и [**D3D12_FEATURE_DATA_MULTISAMPLE_QUALITY_LEVELS**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_feature_data_multisample_quality_levels).
- Передайте **D3D12_FEATURE_PROTECTED_RESOURCE_SESSION_SUPPORT** и [**D3D12_FEATURE_DATA_PROTECTED_RESOURCE_SESSION_SUPPORT**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_feature_data_protected_resource_session_support).
- Передайте **D3D12_FEATURE_ROOT_SIGNATURE** и [**D3D12_FEATURE_DATA_ROOT_SIGNATURE**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_feature_data_root_signature).
- Передайте **D3D12_FEATURE_SERIALIZATION** и [**D3D12_FEATURE_DATA_SERIALIZATION**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_feature_data_serialization).
- Передайте **D3D12_FEATURE_SHADER_CACHE** и [**D3D12_FEATURE_DATA_SHADER_CACHE**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_feature_data_shader_cache).
- Передайте **D3D12_FEATURE_SHADER_MODEL** и [**D3D12_FEATURE_DATA_SHADER_MODEL**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_feature_data_shader_model).

## <a name="hardware-support-for-dxgi-formats"></a>Поддержка оборудования для форматов DXGI

Сведения о просмотре таблиц форматов DXGI и аппаратных компонентов см. в этих разделах.

- [Поддержка формата DXGI для оборудования уровня компонентов Direct3D 12,1](/windows/desktop/direct3ddxgi/hardware-support-for-direct3d-12-1-formats)
- [Поддержка формата DXGI для оборудования уровня компонентов Direct3D 12,0](/windows/desktop/direct3ddxgi/hardware-support-for-direct3d-12-0-formats)
- [Поддержка формата DXGI для оборудования уровня компонентов Direct3D 11,1](/windows/desktop/direct3ddxgi/format-support-for-direct3d-11-1-feature-level-hardware)
- [Поддержка формата DXGI для оборудования уровня компонентов Direct3D 11,0](/windows/desktop/direct3ddxgi/format-support-for-direct3d-11-0-feature-level-hardware)
- [Аппаратная поддержка форматов Direct3D 10Level9](/previous-versions//ff471324(v=vs.85))
- [Аппаратная поддержка форматов Direct3D 10,1](/previous-versions//cc627091(v=vs.85))
- [Поддержка оборудования для форматов Direct3D 10](/previous-versions//cc627090(v=vs.85))

## <a name="related-topics"></a>Связанные темы

* [Привязка ресурсов в Direct3D 12](resource-binding.md)
* [Уровни компонентов оборудования](hardware-feature-levels.md)
* [Корневые подписи](root-signatures.md)