---
title: Запросы возможностей
description: 'Приложение может обнаружить уровень поддержки привязки ресурсов и многие другие функции с помощью вызова ID3D12Device \: \: чеккфеатуресуппорт.'
ms.assetid: ECBAF8EF-5D91-46D8-9D6E-A7FA4203B9F8
ms.date: 11/26/2018
ms.localizationpriority: high
ms.topic: article
ms.openlocfilehash: eaf451f91d51cfa6e900f328898c3418f0974a2d
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "104548950"
---
# <a name="capability-querying"></a><span data-ttu-id="32fc6-103">Запросы возможностей</span><span class="sxs-lookup"><span data-stu-id="32fc6-103">Capability querying</span></span>

<span data-ttu-id="32fc6-104">Приложение может обнаружить уровень поддержки привязки ресурсов (а также уровень поддержки многих других функций) с помощью вызова [**ID3D12Device:: чеккфеатуресуппорт**](/windows/desktop/api/d3d12/nf-d3d12-id3d12device-checkfeaturesupport).</span><span class="sxs-lookup"><span data-stu-id="32fc6-104">Your application can discover the level of support for resource binding (as well as the level of support for many other features), with a call to [**ID3D12Device::CheckFeatureSupport**](/windows/desktop/api/d3d12/nf-d3d12-id3d12device-checkfeaturesupport).</span></span>

## <a name="how-to-query-for-the-resource-binding-tier"></a><span data-ttu-id="32fc6-105">Запрос уровня привязки ресурсов</span><span class="sxs-lookup"><span data-stu-id="32fc6-105">How to query for the resource binding tier</span></span>

<span data-ttu-id="32fc6-106">В первом примере основное внимание уделяется привязке ресурсов.</span><span class="sxs-lookup"><span data-stu-id="32fc6-106">This first example focuses on resource binding.</span></span> <span data-ttu-id="32fc6-107">Каждый уровень привязки ресурсов является надмножеством более низких уровней функциональности, поэтому код, работающий на данном уровне, работает на любом более высоком уровне.</span><span class="sxs-lookup"><span data-stu-id="32fc6-107">Each resource binding tier is a superset of lower tiers in functionality, so code that works on a given tier works unchanged on any higher tier.</span></span>

<span data-ttu-id="32fc6-108">Уровни привязки ресурсов являются константами в перечислении [**D3D12_RESOURCE_BINDING_TIER**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_resource_binding_tier) .</span><span class="sxs-lookup"><span data-stu-id="32fc6-108">The resource binding tiers are constants in the [**D3D12_RESOURCE_BINDING_TIER**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_resource_binding_tier) enumeration.</span></span>

<span data-ttu-id="32fc6-109">Чтобы запросить уровень привязки ресурсов, используйте следующий код.</span><span class="sxs-lookup"><span data-stu-id="32fc6-109">To query for the resource binding tier, use code such as this.</span></span> <span data-ttu-id="32fc6-110">Этот пример кода демонстрирует общий шаблон для запроса любого из различных видов поддержки функций.</span><span class="sxs-lookup"><span data-stu-id="32fc6-110">This code example demonstrates the general pattern for querying for any of the various kinds of feature support.</span></span>

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

<span data-ttu-id="32fc6-111">Обратите внимание, что любая передаваемая Перечисляемая константа (в данном случае [**D3D12_FEATURE_D3D12_OPTIONS**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_feature)) имеет соответствующую структуру данных, которая получает сведения об этой функции или наборе функций (в данном случае [**D3D12_FEATURE_DATA_D3D12_OPTIONS**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_feature_data_d3d12_options)).</span><span class="sxs-lookup"><span data-stu-id="32fc6-111">Note that any enumerated constant that you pass ([**D3D12_FEATURE_D3D12_OPTIONS**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_feature), in this case) has a corresponding data structure that receives info about that feature or set of features ([**D3D12_FEATURE_DATA_D3D12_OPTIONS**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_feature_data_d3d12_options), in this case).</span></span> <span data-ttu-id="32fc6-112">Всегда передавайте указатель на структуру, которая соответствует переданной перечисленной константе.</span><span class="sxs-lookup"><span data-stu-id="32fc6-112">Always pass a pointer to the structure that matches the enumerated constant that you pass.</span></span>

## <a name="how-to-query-for-any-feature-level"></a><span data-ttu-id="32fc6-113">Как запросить любой уровень функций</span><span class="sxs-lookup"><span data-stu-id="32fc6-113">How to query for any feature level</span></span>

<span data-ttu-id="32fc6-114">Так же как и уровень привязки ресурсов, существует множество других функций, уровень поддержки которых можно запросить, используя тот же шаблон, который приведен в приведенном выше примере кода.</span><span class="sxs-lookup"><span data-stu-id="32fc6-114">As well as the resource binding tier, there are many other features whose level of support you can query for using the same pattern shown in the code example above.</span></span> <span data-ttu-id="32fc6-115">Вы просто передаете другую константу из перечисления [**D3D12_FEATURE**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_feature) в [**ID3D12Device:: чеккфеатуресуппорт**](/windows/desktop/api/d3d12/nf-d3d12-id3d12device-checkfeaturesupport) (чтобы сообщить API, какую функцию следует запрашивать информацию о поддержке), и передаете указатель на экземпляр соответствующей структуры (для получения запрошенной информации).</span><span class="sxs-lookup"><span data-stu-id="32fc6-115">You just pass a different constant from the [**D3D12_FEATURE**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_feature) enumeration to [**ID3D12Device::CheckFeatureSupport**](/windows/desktop/api/d3d12/nf-d3d12-id3d12device-checkfeaturesupport) (to tell the API what feature to request support information on), and you pass a pointer to an instance of the matching structure (in which to receive the requested info).</span></span>

- <span data-ttu-id="32fc6-116">Передайте **D3D12_FEATURE_ARCHITECTURE** и [**D3D12_FEATURE_DATA_ARCHITECTURE**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_feature_data_architecture).</span><span class="sxs-lookup"><span data-stu-id="32fc6-116">Pass **D3D12_FEATURE_ARCHITECTURE** and [**D3D12_FEATURE_DATA_ARCHITECTURE**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_feature_data_architecture).</span></span>
- <span data-ttu-id="32fc6-117">Передайте **D3D12_FEATURE_ARCHITECTURE1** и [**D3D12_FEATURE_DATA_ARCHITECTURE1**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_feature_data_architecture1).</span><span class="sxs-lookup"><span data-stu-id="32fc6-117">Pass **D3D12_FEATURE_ARCHITECTURE1** and [**D3D12_FEATURE_DATA_ARCHITECTURE1**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_feature_data_architecture1).</span></span>
- <span data-ttu-id="32fc6-118">Передайте **D3D12_FEATURE_COMMAND_QUEUE_PRIORITY** и [**D3D12_FEATURE_DATA_COMMAND_QUEUE_PRIORITY**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_feature_data_command_queue_priority).</span><span class="sxs-lookup"><span data-stu-id="32fc6-118">Pass **D3D12_FEATURE_COMMAND_QUEUE_PRIORITY** and [**D3D12_FEATURE_DATA_COMMAND_QUEUE_PRIORITY**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_feature_data_command_queue_priority).</span></span>
- <span data-ttu-id="32fc6-119">Передайте **D3D12_FEATURE_CROSS_NODE** и [**D3D12_FEATURE_DATA_CROSS_NODE**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_feature_data_cross_node).</span><span class="sxs-lookup"><span data-stu-id="32fc6-119">Pass **D3D12_FEATURE_CROSS_NODE** and [**D3D12_FEATURE_DATA_CROSS_NODE**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_feature_data_cross_node).</span></span>
- <span data-ttu-id="32fc6-120">Передайте **D3D12_FEATURE_D3D12_OPTIONS** и [**D3D12_FEATURE_DATA_D3D12_OPTIONS**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_feature_data_d3d12_options).</span><span class="sxs-lookup"><span data-stu-id="32fc6-120">Pass **D3D12_FEATURE_D3D12_OPTIONS** and [**D3D12_FEATURE_DATA_D3D12_OPTIONS**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_feature_data_d3d12_options).</span></span>
- <span data-ttu-id="32fc6-121">Передайте **D3D12_FEATURE_D3D12_OPTIONS1** и [**D3D12_FEATURE_DATA_D3D12_OPTIONS1**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_feature_data_d3d12_options1).</span><span class="sxs-lookup"><span data-stu-id="32fc6-121">Pass **D3D12_FEATURE_D3D12_OPTIONS1** and [**D3D12_FEATURE_DATA_D3D12_OPTIONS1**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_feature_data_d3d12_options1).</span></span>
- <span data-ttu-id="32fc6-122">Передайте **D3D12_FEATURE_D3D12_OPTIONS2** и [**D3D12_FEATURE_DATA_D3D12_OPTIONS2**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_feature_data_d3d12_options2).</span><span class="sxs-lookup"><span data-stu-id="32fc6-122">Pass **D3D12_FEATURE_D3D12_OPTIONS2** and [**D3D12_FEATURE_DATA_D3D12_OPTIONS2**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_feature_data_d3d12_options2).</span></span>
- <span data-ttu-id="32fc6-123">Передайте **D3D12_FEATURE_D3D12_OPTIONS3** и [**D3D12_FEATURE_DATA_D3D12_OPTIONS3**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_feature_data_d3d12_options3).</span><span class="sxs-lookup"><span data-stu-id="32fc6-123">Pass **D3D12_FEATURE_D3D12_OPTIONS3** and [**D3D12_FEATURE_DATA_D3D12_OPTIONS3**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_feature_data_d3d12_options3).</span></span>
- <span data-ttu-id="32fc6-124">Передайте **D3D12_FEATURE_D3D12_OPTIONS4** и [**D3D12_FEATURE_DATA_D3D12_OPTIONS4**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_feature_data_d3d12_options4).</span><span class="sxs-lookup"><span data-stu-id="32fc6-124">Pass **D3D12_FEATURE_D3D12_OPTIONS4** and [**D3D12_FEATURE_DATA_D3D12_OPTIONS4**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_feature_data_d3d12_options4).</span></span>
- <span data-ttu-id="32fc6-125">Передайте **D3D12_FEATURE_D3D12_OPTIONS5** и [**D3D12_FEATURE_DATA_D3D12_OPTIONS5**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_feature_data_d3d12_options5).</span><span class="sxs-lookup"><span data-stu-id="32fc6-125">Pass **D3D12_FEATURE_D3D12_OPTIONS5** and [**D3D12_FEATURE_DATA_D3D12_OPTIONS5**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_feature_data_d3d12_options5).</span></span>
- <span data-ttu-id="32fc6-126">Передайте **D3D12_FEATURE_EXISTING_HEAPS** и [**D3D12_FEATURE_DATA_EXISTING_HEAPS**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_feature_data_existing_heaps).</span><span class="sxs-lookup"><span data-stu-id="32fc6-126">Pass **D3D12_FEATURE_EXISTING_HEAPS** and [**D3D12_FEATURE_DATA_EXISTING_HEAPS**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_feature_data_existing_heaps).</span></span>
- <span data-ttu-id="32fc6-127">Передайте **D3D12_FEATURE_FEATURE_LEVELS** и [**D3D12_FEATURE_DATA_FEATURE_LEVELS**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_feature_data_feature_levels).</span><span class="sxs-lookup"><span data-stu-id="32fc6-127">Pass **D3D12_FEATURE_FEATURE_LEVELS** and [**D3D12_FEATURE_DATA_FEATURE_LEVELS**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_feature_data_feature_levels).</span></span>
- <span data-ttu-id="32fc6-128">Передайте **D3D12_FEATURE_FORMAT_INFO** и [**D3D12_FEATURE_DATA_FORMAT_INFO**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_feature_data_format_info).</span><span class="sxs-lookup"><span data-stu-id="32fc6-128">Pass **D3D12_FEATURE_FORMAT_INFO** and [**D3D12_FEATURE_DATA_FORMAT_INFO**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_feature_data_format_info).</span></span>
- <span data-ttu-id="32fc6-129">Передайте **D3D12_FEATURE_FORMAT_SUPPORT** и [**D3D12_FEATURE_DATA_FORMAT_SUPPORT**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_feature_data_format_support).</span><span class="sxs-lookup"><span data-stu-id="32fc6-129">Pass **D3D12_FEATURE_FORMAT_SUPPORT** and [**D3D12_FEATURE_DATA_FORMAT_SUPPORT**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_feature_data_format_support).</span></span>
- <span data-ttu-id="32fc6-130">Передайте **D3D12_FEATURE_GPU_VIRTUAL_ADDRESS_SUPPORT** и [**D3D12_FEATURE_DATA_GPU_VIRTUAL_ADDRESS_SUPPORT**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_feature_data_gpu_virtual_address_support).</span><span class="sxs-lookup"><span data-stu-id="32fc6-130">Pass **D3D12_FEATURE_GPU_VIRTUAL_ADDRESS_SUPPORT** and [**D3D12_FEATURE_DATA_GPU_VIRTUAL_ADDRESS_SUPPORT**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_feature_data_gpu_virtual_address_support).</span></span>
- <span data-ttu-id="32fc6-131">Передайте **D3D12_FEATURE_MULTISAMPLE_QUALITY_LEVELS** и [**D3D12_FEATURE_DATA_MULTISAMPLE_QUALITY_LEVELS**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_feature_data_multisample_quality_levels).</span><span class="sxs-lookup"><span data-stu-id="32fc6-131">Pass **D3D12_FEATURE_MULTISAMPLE_QUALITY_LEVELS** and [**D3D12_FEATURE_DATA_MULTISAMPLE_QUALITY_LEVELS**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_feature_data_multisample_quality_levels).</span></span>
- <span data-ttu-id="32fc6-132">Передайте **D3D12_FEATURE_PROTECTED_RESOURCE_SESSION_SUPPORT** и [**D3D12_FEATURE_DATA_PROTECTED_RESOURCE_SESSION_SUPPORT**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_feature_data_protected_resource_session_support).</span><span class="sxs-lookup"><span data-stu-id="32fc6-132">Pass **D3D12_FEATURE_PROTECTED_RESOURCE_SESSION_SUPPORT** and [**D3D12_FEATURE_DATA_PROTECTED_RESOURCE_SESSION_SUPPORT**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_feature_data_protected_resource_session_support).</span></span>
- <span data-ttu-id="32fc6-133">Передайте **D3D12_FEATURE_ROOT_SIGNATURE** и [**D3D12_FEATURE_DATA_ROOT_SIGNATURE**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_feature_data_root_signature).</span><span class="sxs-lookup"><span data-stu-id="32fc6-133">Pass **D3D12_FEATURE_ROOT_SIGNATURE** and [**D3D12_FEATURE_DATA_ROOT_SIGNATURE**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_feature_data_root_signature).</span></span>
- <span data-ttu-id="32fc6-134">Передайте **D3D12_FEATURE_SERIALIZATION** и [**D3D12_FEATURE_DATA_SERIALIZATION**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_feature_data_serialization).</span><span class="sxs-lookup"><span data-stu-id="32fc6-134">Pass **D3D12_FEATURE_SERIALIZATION** and [**D3D12_FEATURE_DATA_SERIALIZATION**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_feature_data_serialization).</span></span>
- <span data-ttu-id="32fc6-135">Передайте **D3D12_FEATURE_SHADER_CACHE** и [**D3D12_FEATURE_DATA_SHADER_CACHE**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_feature_data_shader_cache).</span><span class="sxs-lookup"><span data-stu-id="32fc6-135">Pass **D3D12_FEATURE_SHADER_CACHE** and [**D3D12_FEATURE_DATA_SHADER_CACHE**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_feature_data_shader_cache).</span></span>
- <span data-ttu-id="32fc6-136">Передайте **D3D12_FEATURE_SHADER_MODEL** и [**D3D12_FEATURE_DATA_SHADER_MODEL**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_feature_data_shader_model).</span><span class="sxs-lookup"><span data-stu-id="32fc6-136">Pass **D3D12_FEATURE_SHADER_MODEL** and [**D3D12_FEATURE_DATA_SHADER_MODEL**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_feature_data_shader_model).</span></span>

## <a name="hardware-support-for-dxgi-formats"></a><span data-ttu-id="32fc6-137">Поддержка оборудования для форматов DXGI</span><span class="sxs-lookup"><span data-stu-id="32fc6-137">Hardware support for DXGI Formats</span></span>

<span data-ttu-id="32fc6-138">Сведения о просмотре таблиц форматов DXGI и аппаратных компонентов см. в этих разделах.</span><span class="sxs-lookup"><span data-stu-id="32fc6-138">To view tables of DXGI formats and hardware features, refer to these topics.</span></span>

- [<span data-ttu-id="32fc6-139">Поддержка формата DXGI для оборудования уровня компонентов Direct3D 12,1</span><span class="sxs-lookup"><span data-stu-id="32fc6-139">DXGI Format Support for Direct3D Feature Level 12.1 Hardware</span></span>](/windows/desktop/direct3ddxgi/hardware-support-for-direct3d-12-1-formats)
- [<span data-ttu-id="32fc6-140">Поддержка формата DXGI для оборудования уровня компонентов Direct3D 12,0</span><span class="sxs-lookup"><span data-stu-id="32fc6-140">DXGI Format Support for Direct3D Feature Level 12.0 Hardware</span></span>](/windows/desktop/direct3ddxgi/hardware-support-for-direct3d-12-0-formats)
- [<span data-ttu-id="32fc6-141">Поддержка формата DXGI для оборудования уровня компонентов Direct3D 11,1</span><span class="sxs-lookup"><span data-stu-id="32fc6-141">DXGI Format Support for Direct3D Feature Level 11.1 Hardware</span></span>](/windows/desktop/direct3ddxgi/format-support-for-direct3d-11-1-feature-level-hardware)
- [<span data-ttu-id="32fc6-142">Поддержка формата DXGI для оборудования уровня компонентов Direct3D 11,0</span><span class="sxs-lookup"><span data-stu-id="32fc6-142">DXGI Format Support for Direct3D Feature Level 11.0 Hardware</span></span>](/windows/desktop/direct3ddxgi/format-support-for-direct3d-11-0-feature-level-hardware)
- <span data-ttu-id="32fc6-143">[Аппаратная поддержка форматов Direct3D 10Level9](/previous-versions//ff471324(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="32fc6-143">[Hardware Support for Direct3D 10Level9 Formats](/previous-versions//ff471324(v=vs.85))</span></span>
- <span data-ttu-id="32fc6-144">[Аппаратная поддержка форматов Direct3D 10,1](/previous-versions//cc627091(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="32fc6-144">[Hardware Support for Direct3D 10.1 Formats](/previous-versions//cc627091(v=vs.85))</span></span>
- <span data-ttu-id="32fc6-145">[Поддержка оборудования для форматов Direct3D 10](/previous-versions//cc627090(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="32fc6-145">[Hardware Support for Direct3D 10 Formats](/previous-versions//cc627090(v=vs.85))</span></span>

## <a name="related-topics"></a><span data-ttu-id="32fc6-146">Связанные темы</span><span class="sxs-lookup"><span data-stu-id="32fc6-146">Related topics</span></span>

* [<span data-ttu-id="32fc6-147">Привязка ресурсов в Direct3D 12</span><span class="sxs-lookup"><span data-stu-id="32fc6-147">Resource binding in Direct3D 12</span></span>](resource-binding.md)
* [<span data-ttu-id="32fc6-148">Уровни компонентов оборудования</span><span class="sxs-lookup"><span data-stu-id="32fc6-148">Hardware feature levels</span></span>](hardware-feature-levels.md)
* [<span data-ttu-id="32fc6-149">Корневые подписи</span><span class="sxs-lookup"><span data-stu-id="32fc6-149">Root signatures</span></span>](root-signatures.md)