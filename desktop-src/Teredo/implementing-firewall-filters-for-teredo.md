---
title: Реализация фильтров брандмауэра для Teredo
description: Windows позволяет приложениям задать параметр сокета, позволяющий приложениям указать явную намерение получить трафик Teredo, отправляемый в брандмауэр узла через платформу фильтрации Windows.
ms.assetid: 9e53e28c-e0e5-438d-b624-27d7bd65e4a3
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0f24d4351f10a3b37f2bf63c952e81883d97b781
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "103792942"
---
# <a name="implementing-firewall-filters-for-teredo"></a><span data-ttu-id="64cb4-103">Реализация фильтров брандмауэра для Teredo</span><span class="sxs-lookup"><span data-stu-id="64cb4-103">Implementing Firewall Filters for Teredo</span></span>

<span data-ttu-id="64cb4-104">Windows позволяет приложениям задать параметр сокета, позволяющий приложениям указать явную намерение получить трафик Teredo, отправляемый в брандмауэр узла через платформу фильтрации Windows.</span><span class="sxs-lookup"><span data-stu-id="64cb4-104">Windows allows applications to set a socket option that allows applications to indicate an explicit intent to receive Teredo traffic sent to the host firewall via the Windows Filtering Platform.</span></span> <span data-ttu-id="64cb4-105">В Windows параметр сокета для установки уровня защиты используется, чтобы приложение определяло, какой тип трафика он хочет получить.</span><span class="sxs-lookup"><span data-stu-id="64cb4-105">In Windows, a socket option for setting a protection level is used to allow an application to define what type of traffic it is willing to receive.</span></span> <span data-ttu-id="64cb4-106">В частности, в сценариях, включающих трафик Teredo, указан параметр сокета [ \_ \_ уровня защиты IPv6](/windows/desktop/WinSock/ipv6-protection-level) .</span><span class="sxs-lookup"><span data-stu-id="64cb4-106">More specifically, in scenarios involving Teredo traffic, the [IPV6\_PROTECTION\_LEVEL](/windows/desktop/WinSock/ipv6-protection-level) socket option is specified.</span></span> <span data-ttu-id="64cb4-107">Рекомендуется, чтобы реализации брандмауэра узла поддерживали следующие фильтры для выборочного разрешения трафика Teredo для приложения, блокируя трафик по умолчанию для любого приложения без исключения.</span><span class="sxs-lookup"><span data-stu-id="64cb4-107">It is recommended that host firewall implementations maintain the following filters to selectively allow Teredo traffic for an application, while blocking traffic by default for any application without an exemption.</span></span>

## <a name="default-block-filter-for-edge-traversed-traffic"></a><span data-ttu-id="64cb4-108">Фильтр блокировки по умолчанию для трафика, обход которого проходит</span><span class="sxs-lookup"><span data-stu-id="64cb4-108">Default Block Filter for Edge Traversed Traffic</span></span>

<span data-ttu-id="64cb4-109">Брандмауэр узла всегда должен поддерживать фильтр блоков по умолчанию в рамках \_ уровня фильтрации проверки подлинности \_ приема ALE \_ \_ версии 6 для трафика, соответствующего указанному **типу интерфейса туннель** и **типы туннеля Teredo** .</span><span class="sxs-lookup"><span data-stu-id="64cb4-109">A host firewall must always maintain a default block filter within the ALE\_AUTH\_RECV\_ACCEPT\_V6 filtering layer for traffic matching the specified **Interface Type Tunnel** and **Tunnel Type Teredo** conditions.</span></span> <span data-ttu-id="64cb4-110">При реализации этот фильтр указывает на наличие в системе брандмауэра узла, поддерживающего обход узлов.</span><span class="sxs-lookup"><span data-stu-id="64cb4-110">When implemented, this filter indicates the presence of an edge traversal aware host firewall in the system.</span></span> <span data-ttu-id="64cb4-111">Этот фильтр просматривается как контракт API между брандмауэром узла и Windows.</span><span class="sxs-lookup"><span data-stu-id="64cb4-111">This filter is viewed as an API contract between the host firewall and Windows.</span></span> <span data-ttu-id="64cb4-112">По умолчанию этот фильтр блокирует трафик с обходом по границе любого приложения.</span><span class="sxs-lookup"><span data-stu-id="64cb4-112">By default, this filter will block edge traversed traffic to any application.</span></span>

``` syntax
   filter.layerKey  = FWPM_LAYER_ALE_AUTH_RECV_ACCEPT_V6;
   filter.action.type = FWP_ACTION_BLOCK;
   filter.subLayerKey = FWPM_SUBLAYER_EDGE_TRAVERSAL;
   filter.weight.type = FWP_UINT64;
   filter.weight.uint64 = 0;
   filter.flags = 0;
   filter.numFilterConditions = 2; // Or 3 depending on including the loopback condition
   filter.filterCondition = filterConditions;
   filter.displayData.name  = L"Teredo Edge Traversal Default Block";
   filter.displayData.description = L"Teredo Edge Traversal Default Block Filter.";

   // Match Interface type tunnel
   filterConditions[0].fieldKey = FWPM_CONDITION_INTERFACE_TYPE;
   filterConditions[0].matchType = FWP_MATCH_EQUAL;
   filterConditions[0].conditionValue.type = FWP_UINT32;
   filterConditions[0].conditionValue.uint32 = IF_TYPE_TUNNEL;

   // Match tunnel type Teredo
   filterConditions[1].fieldKey = FWPM_CONDITION_TUNNEL_TYPE;
   filterConditions[1].matchType = FWP_MATCH_EQUAL;
   filterConditions[1].conditionValue.type = FWP_UINT32;
   filterConditions[1].conditionValue.uint32 = TUNNEL_TYPE_TEREDO;

   // Having this condition is OPTIONAL, including this will automatically exempt 
   // loopback traffic to receive Teredo.
   filterConditions[2].fieldKey = FWPM_CONDITION_FLAGS;
   filterConditions[2].matchType = FWP_MATCH_FLAGS_NONE_SET;
   filterConditions[2].conditionValue.type = FWP_UINT32;
   filterConditions[2].conditionValue.uint32 = FWP_CONDITION_FLAG_IS_LOOPBACK;
```

> [!Note]  
> <span data-ttu-id="64cb4-113">Классы "Доставка", "Прибытие" и "следующий прыжок" условий интерфейса используются для управления моделью слабого узла и переадресацией пакетов между интерфейсами.</span><span class="sxs-lookup"><span data-stu-id="64cb4-113">The 'Delivery', 'Arrival', and 'Next Hop' classes of interface conditions are used to control a weak-host model and packet forwarding across interfaces.</span></span> <span data-ttu-id="64cb4-114">В приведенном выше примере используется класс Delivery.</span><span class="sxs-lookup"><span data-stu-id="64cb4-114">The example above utilizes the 'Delivery' class.</span></span> <span data-ttu-id="64cb4-115">Ознакомьтесь [с условиями фильтрации, доступными на каждом слое фильтрации](/windows/desktop/FWP/filtering-conditions-available-at-each-filtering-layer) в документации по пакету SDK для платформы WFP, так как ваша структура безопасности должна учитывать все случаи.</span><span class="sxs-lookup"><span data-stu-id="64cb4-115">Please review [Filtering Conditions Available at Each Filtering Layer](/windows/desktop/FWP/filtering-conditions-available-at-each-filtering-layer) in the WFP SDK documentation, as your security design must take each case into consideration.</span></span>

 

## <a name="allow-filter-for-exempt-applications"></a><span data-ttu-id="64cb4-116">Разрешить фильтр для исключений приложений</span><span class="sxs-lookup"><span data-stu-id="64cb4-116">Allow Filter for Exempt Applications</span></span>

<span data-ttu-id="64cb4-117">Если приложение не получает трафик Teredo на сокете прослушивания, то фильтр разрешения должен быть реализован в \_ слое проверки подлинности ALE \_ РКВ \_ Accept \_ V6 на брандмауэре узла.</span><span class="sxs-lookup"><span data-stu-id="64cb4-117">If an application is exempt from receiving Teredo traffic on a listening socket, a permit filter must be implemented within the ALE\_AUTH\_RCV\_ACCEPT\_V6 filtering layer on the host firewall.</span></span> <span data-ttu-id="64cb4-118">Важно отметить, что в зависимости от того, как пользователь или приложение настраивает исключение, брандмауэр узла может включать параметр сокета.</span><span class="sxs-lookup"><span data-stu-id="64cb4-118">It is important to note that depending on how the exemption is configured by the user or application, the host firewall can include a socket option.</span></span>

``` syntax
   filter.layerKey   = FWPM_LAYER_ALE_AUTH_RCV_ACCEPT_V6;
   filter.action.type = FWP_ACTION_PERMIT;
   filter.subLayerKey = FWPM_SUBLAYER_EDGE_TRAVERSAL;
   filter.weight.type = FWP_UINT64;   
   filter.weight.uint64= 1; // Use a weight higher than the default block
   filter.flags = 0;
   filter.numFilterConditions = 3; // Or 4 depending on the socket option based condition
   filter.filterCondition = filterConditions;
   filter.displayData.name = L"Teredo Edge Traversal Allow Application A";
   filter.displayData.description = L"Teredo Edge Traversal Allow Application A Filter.";

   filterConditions[0].fieldKey = FWPM_CONDITION_INTERFACE_TYPE;
   filterConditions[0].matchType = FWP_MATCH_EQUAL;
   filterConditions[0].conditionValue.type = FWP_UINT32;
   filterConditions[0].conditionValue.uint32 = IF_TYPE_TUNNEL;

   filterConditions[1].fieldKey = FWPM_CONDITION_TUNNEL_TYPE;
   filterConditions[1].matchType = FWP_MATCH_EQUAL;
   filterConditions[1].conditionValue.type = FWP_UINT32;
   filterConditions[1].conditionValue.uint32 = TUNNEL_TYPE_TEREDO;

   FWP_BYTE_BLOB byteBlob = {0};
   filterConditions[2].fieldKey = FWPM_CONDITION_ALE_APP_ID;
   filterConditions[2].matchType = FWP_MATCH_EQUAL;
   filterConditions[2].conditionValue.type = FWP_BYTE_BLOB_TYPE;
   filterConditions[2].conditionValue.byteBlob = &byteBlob;
   filterConditions[2].conditionValue.byteBlob->data = (uint8 *) wszApplicationA;
   filterConditions[2].conditionValue.byteBlob->size = (wcslen(wszApplicationA) + 1)*sizeof(wchar_t);

   // This filter scopes to exemption to ONLY IF the socket option is set, in other words
   // application has explicitly opted in to receive Teredo traffic
   filterConditions[3].fieldKey = FWPM_CONDITION_ALE_SIO_FIREWALL_SOCKET_PROPERTY;
   filterConditions[3].matchType = FWP_MATCH_FLAGS_ALL_SET;
   filterConditions[3].conditionValue.type = FWP_UINT32;
   filterConditions[3].conditionValue.uint32 = FWP_CONDITION_SOCKET_PROPERTY_FLAG_ALLOW_EDGE_TRAFFIC;
```

## <a name="dormancy-callout-filter"></a><span data-ttu-id="64cb4-119">Фильтр выноски максимальным периодом ожидания</span><span class="sxs-lookup"><span data-stu-id="64cb4-119">Dormancy Callout Filter</span></span>

<span data-ttu-id="64cb4-120">Служба Teredo в Windows реализует модель максимальным периодом ожидания.</span><span class="sxs-lookup"><span data-stu-id="64cb4-120">The Teredo service in Windows implements a dormancy model.</span></span> <span data-ttu-id="64cb4-121">В любой момент времени, если ни одно из приложений не прослушивает сокеты UDP или TCP с включенным обходом узлов, служба переходит в неактивное состояние.</span><span class="sxs-lookup"><span data-stu-id="64cb4-121">At any given time, if no applications are listening on a UDP or TCP socket with edge traversal enabled, the service moves to a dormant state.</span></span> <span data-ttu-id="64cb4-122">Чтобы механизм максимальным периодом ожидания работал, брандмауэр узла должен поддерживать фильтр выноски для каждого исключаемого приложения, указанного в \_ слое фильтрации уровня проверки подлинности ALE \_ \_ V6 для TCP, и \_ \_ уровень фильтрации назначения ресурсов ALE \_ V6 для приложений на основе UDP.</span><span class="sxs-lookup"><span data-stu-id="64cb4-122">For the dormancy mechanism to work, the host firewall must maintain a callout filter for each exempt application specified within the ALE\_AUTH\_LISTEN\_V6 filtering layer for TCP, and ALE\_RESOURCE\_ASSIGNMENT\_V6 filtering layer for UDP based applications.</span></span> <span data-ttu-id="64cb4-123">В следующем примере показана максимальным периодом ожиданияная выноска для приложения **TCP** .</span><span class="sxs-lookup"><span data-stu-id="64cb4-123">The following sample below demonstrates a dormancy callout for a **TCP** application.</span></span>

``` syntax
   filter.layerKey = FWPM_LAYER_ALE_AUTH_LISTEN_V6;
   // Use FWPM_LAYER_ALE_RESOURCE_ASSIGNMENT_V6 for UDP based exemption

   filter.action.type = FWP_ACTION_CALLOUT_TERMINATING;
   filter.action.calloutKey = FWPM_CALLOUT_EDGE_TRAVERSAL_ALE_LISTEN_V6;
   // Use FWPM_CALLOUT_EDGE_TRAVERSAL_ALE_RESOURCE_ASSIGNMENT_V6 for UDP based exemption

   filter.subLayerKey = FWPM_SUBLAYER_EDGE_TRAVERSAL;
   filter.weight.type = FWP_UINT64;   
   filter.weight.uint64 = 1;
   filter.flags = 0;
   filter.numFilterConditions = 1; // 2 if including the socket option based condition 
   filter.filterCondition = filterConditions;
   filter.displayData.name = L"Teredo Edge Traversal dormancy callout for app A";
   filter.displayData.description = L"Teredo Edge Traversal dormancy callout filter for A.";

   FWP_BYTE_BLOB byteBlob = {0};
   filterConditions[0].fieldKey = FWPM_CONDITION_ALE_APP_ID;
   filterConditions[0].matchType = FWP_MATCH_EQUAL;
   filterConditions[0].conditionValue.type = FWP_BYTE_BLOB_TYPE;
   filterConditions[0].conditionValue.byteBlob = &byteBlob;
   filterConditions[0].conditionValue.byteBlob->data = (uint8 *)wszApplicationA;
   filterConditions[0].conditionValue.byteBlob->size = (wcslen(wszApplicationA) + 1)*sizeof(wchar_t);

   // This filter scopes to exemption to ONLY IF the socket option is set, in other words
   // application has explicitly opted in to receive Teredo traffic
   filterConditions[1].fieldKey = FWPM_CONDITION_ALE_SIO_FIREWALL_SOCKET_PROPERTY;
   filterConditions[1].matchType = FWP_MATCH_FLAGS_ALL_SET;
   filterConditions[1].conditionValue.type = FWP_UINT32;
   filterConditions[1].conditionValue.uint32 = FWP_CONDITION_SOCKET_PROPERTY_FLAG_ALLOW_EDGE_TRAFFIC;
```

 

 