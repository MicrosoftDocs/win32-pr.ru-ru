---
title: Реализация фильтров брандмауэра для Teredo
description: Windows позволяет приложениям задавать параметр сокета, позволяющий приложениям указать явную цель получения трафика Teredo, передаваемого в брандмауэр узла с помощью платформы фильтрации Windows.
ms.assetid: 9e53e28c-e0e5-438d-b624-27d7bd65e4a3
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9fe854b210e6b07f0777a492d5c952f502e2f7c2b6c1c4b40497bad3a9e8248a
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119001816"
---
# <a name="implementing-firewall-filters-for-teredo"></a>Реализация фильтров брандмауэра для Teredo

Windows позволяет приложениям задавать параметр сокета, позволяющий приложениям указать явную цель получения трафика Teredo, передаваемого в брандмауэр узла с помощью платформы фильтрации Windows. в Windows параметр сокета для установки уровня защиты используется, чтобы приложение определяло, какой тип трафика он хочет получить. В частности, в сценариях, включающих трафик Teredo, указан параметр сокета [ \_ \_ уровня защиты IPv6](/windows/desktop/WinSock/ipv6-protection-level) . Рекомендуется, чтобы реализации брандмауэра узла поддерживали следующие фильтры для выборочного разрешения трафика Teredo для приложения, блокируя трафик по умолчанию для любого приложения без исключения.

## <a name="default-block-filter-for-edge-traversed-traffic"></a>Фильтр блокировки по умолчанию для трафика, обход которого проходит

брандмауэр узла всегда должен поддерживать фильтр блоков по умолчанию в рамках \_ уровня фильтрации проверки подлинности \_ приема ale \_ \_ версии 6 для трафика, соответствующего указанному **типу интерфейса Tunnel** и **Tunnel условий Teredo** . При реализации этот фильтр указывает на наличие в системе брандмауэра узла, поддерживающего обход узлов. Этот фильтр просматривается как контракт API между брандмауэром узла и Windows. По умолчанию этот фильтр блокирует трафик с обходом по границе любого приложения.

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
> Классы "Доставка", "Прибытие" и "следующий прыжок" условий интерфейса используются для управления моделью слабого узла и переадресацией пакетов между интерфейсами. В приведенном выше примере используется класс Delivery. Ознакомьтесь [с условиями фильтрации, доступными на каждом слое фильтрации](/windows/desktop/FWP/filtering-conditions-available-at-each-filtering-layer) в документации по пакету SDK для платформы WFP, так как ваша структура безопасности должна учитывать все случаи.

 

## <a name="allow-filter-for-exempt-applications"></a>Разрешить фильтр для исключений приложений

Если приложение не получает трафик Teredo на сокете прослушивания, то фильтр разрешения должен быть реализован в \_ слое проверки подлинности ALE \_ РКВ \_ Accept \_ V6 на брандмауэре узла. Важно отметить, что в зависимости от того, как пользователь или приложение настраивает исключение, брандмауэр узла может включать параметр сокета.

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

## <a name="dormancy-callout-filter"></a>Фильтр выноски максимальным периодом ожидания

служба Teredo в Windows реализует модель максимальным периодом ожидания. В любой момент времени, если ни одно из приложений не прослушивает сокеты UDP или TCP с включенным обходом узлов, служба переходит в неактивное состояние. Чтобы механизм максимальным периодом ожидания работал, брандмауэр узла должен поддерживать фильтр выноски для каждого исключаемого приложения, указанного в \_ слое фильтрации уровня проверки подлинности ALE \_ \_ V6 для TCP, и \_ \_ уровень фильтрации назначения ресурсов ALE \_ V6 для приложений на основе UDP. В следующем примере показана максимальным периодом ожиданияная выноска для приложения **TCP** .

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

 

 