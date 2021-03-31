---
title: Флаги условий фильтрации (Фвптипес. h)
description: Флаги условий фильтрации платформы фильтрации Windows (WFP) представлены битовыми битами.
ms.assetid: fe879479-331d-42ef-ac2f-634f0c13c21d
topic_type:
- apiref
api_name:
- FWP_CONDITION_FLAG_IS_LOOPBACK
- FWP_CONDITION_FLAG_IS_IPSEC_SECURED
- FWP_CONDITION_FLAG_IS_REAUTHORIZE
- FWP_CONDITION_FLAG_IS_WILDCARD_BIND
- FWP_CONDITION_FLAG_IS_RAW_ENDPOINT
- FWP_CONDITION_FLAG_IS_FRAGMENT
- FWP_CONDITION_FLAG_IS_FRAGMENT_GROUP
- FWP_CONDITION_FLAG_IS_IPSEC_NATT_RECLASSIFY
- FWP_CONDITION_FLAG_REQUIRES_ALE_CLASSIFY
- FWP_CONDITION_FLAG_IS_IMPLICIT_BIND
- FWP_CONDITION_FLAG_IS_REASSEMBLED
- FWP_CONDITION_FLAG_IS_NAME_APP_SPECIFIED
- FWP_CONDITION_FLAG_IS_PROMISCUOUS
- FWP_CONDITION_FLAG_IS_AUTH_FW
- FWP_CONDITION_FLAG_IS_RECLASSIFY
- FWP_CONDITION_FLAG_IS_PROXY_CONNECTION
- FWP_CONDITION_FLAG_IS_APPCONTAINER_LOOPBACK
- FWP_CONDITION_FLAG_IS_NON_APPCONTAINER_LOOPBACK
- FWP_CONDITION_FLAG_IS_RESERVED
- FWP_CONDITION_FLAG_IS_HONORING_POLICY_AUTHORIZE
- FWP_CONDITION_REAUTHORIZE_REASON_POLICY_CHANGE
- FWP_CONDITION_REAUTHORIZE_REASON_NEW_ARRIVAL_INTERFACE
- FWP_CONDITION_REAUTHORIZE_REASON_NEW_NEXTHOP_INTERFACE
- FWP_CONDITION_REAUTHORIZE_REASON_PROFILE_CROSSING
- FWP_CONDITION_REAUTHORIZE_REASON_CLASSIFY_COMPLETION
- FWP_CONDITION_REAUTHORIZE_REASON_IPSEC_PROPERTIES_CHANGED
- FWP_CONDITION_REAUTHORIZE_REASON_MID_STREAM_INSPECTION
- FWP_CONDITION_REAUTHORIZE_REASON_SOCKET_PROPERTY_CHANGED
- FWP_CONDITION_REAUTHORIZE_REASON_NEW_INBOUND_MCAST_BCAST_PACKET
- FWP_CONDITION_SOCKET_PROPERTY_FLAG_IS_SYSTEM_PORT_RPC
- FWP_CONDITION_SOCKET_PROPERTY_FLAG_ALLOW_EDGE_TRAFFIC
- FWP_CONDITION_SOCKET_PROPERTY_FLAG_DENY_EDGE_TRAFFIC
- FWP_CONDITION_L2_IS_NATIVE_ETHERNET
- FWP_CONDITION_L2_IS_WIFI
- FWP_CONDITION_L2_IS_MOBILE_BROADBAND
- FWP_CONDITION_L2_IS_WIFI_DIRECT_DATA
- FWP_CONDITION_L2_IS_VM2VM
- FWP_CONDITION_L2_IS_MALFORMED_PACKET
- FWP_CONDITION_L2_IS_IP_FRAGMENT_GROUP
- FWP_CONDITION_L2_IF_CONNECTOR_PRESENT
api_location:
- fwptypes.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6c88fa56f37332d52ed31f5ef042c5064a82ac4d
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "103803514"
---
# <a name="filtering-condition-flags"></a>Флаги условия фильтрации

Флаги условий фильтрации платформы фильтрации Windows (WFP) представлены битовыми битами.

Эти флаги и слои фильтрации, где их можно использовать, определяются следующим образом.

<dl> <dt>

<span id="FWP_CONDITION_FLAG_IS_LOOPBACK"></span><span id="fwp_condition_flag_is_loopback"></span>**\_флаг условия \_ FWP \_ — \_ замыкание на себя**
</dt> <dd> <dl> <dt>



Проверяет, является ли сетевой трафик замыканием на себя.

Фильтрация слоев:

-   ФВПМ \_ Layer \_ Inbound \_ иппаккет \_ V {4 \| 6}
-   ФВПМ \_ уровень \_ исходящей \_ иппаккет \_ V {4 \| 6}
-   ФВПМ \_ уровень \_ входящего \_ транспорта \_ V {4 \| 6}
-   \_Исходящий \_ транспорт уровня фвпм \_ \_ V {4 \| 6}
-   \_Поток уровня \_ фвпм \_ {v4 \| 6}
    > [!Note]  
    > Доступно только в Windows Server 2008, Windows Vista с пакетом обновления 1 (SP1) и более поздних версиях.

     

-   \_ \_ Ошибка входящего ICMP уровня фвпм \_ \_ \_ V {4 \| 6}
    > [!Note]  
    > Доступно только в Windows Server 2008, Windows Vista с пакетом обновления 1 (SP1) и более поздних версиях.

     

-   \_Исходящая \_ \_ Ошибка ICMP уровня фвпм \_ \_ V {4 \| 6}
    > [!Note]  
    > Доступно только в Windows Server 2008, Windows Vista с пакетом обновления 1 (SP1) и более поздних версиях.

     

-   \_ \_ \_ Проверка подлинности на уровне фвпм для проверки \_ \_ приема recv \_ V {4 \| 6}
-   \_ \_ \_ Проверка подлинности ALE уровня фвпм для \_ подключения \_ V {4 \| 6}
    > [!Note]  
    > Доступно только в Windows Server 2008, Windows Vista с пакетом обновления 1 (SP1) и более поздних версиях.

     

-   \_ \_ Установлен поток ALE уровня фвпм \_ \_ \_ V {4 \| 6}
    > [!Note]  
    > Доступно только в Windows Server 2008, Windows Vista с пакетом обновления 1 (SP1) и более поздних версиях.

     


</dt> </dl> </dd> <dt>

<span id="FWP_CONDITION_FLAG_IS_IPSEC_SECURED"></span><span id="fwp_condition_flag_is_ipsec_secured"></span>**\_флаг условия \_ FWP \_ \_ защищен IPsec \_**
</dt> <dd> <dl> <dt>



Проверяет, защищен ли сетевой трафик протоколом IPsec.

Фильтрация слоев:

-   ФВПМ \_ Layer \_ Inbound \_ иппаккет \_ V {4 \| 6}
-   ФВПМ \_ уровень \_ входящего \_ транспорта \_ V {4 \| 6}
-   \_ \_ \_ Проверка подлинности на уровне фвпм для проверки \_ \_ приема recv \_ V {4 \| 6}
-   \_ \_ \_ Проверка подлинности ALE уровня фвпм для \_ подключения \_ V {4 \| 6}


</dt> </dl> </dd> <dt>

<span id="FWP_CONDITION_FLAG_IS_REAUTHORIZE"></span><span id="fwp_condition_flag_is_reauthorize"></span>**\_флаг условия FWP — повторная \_ \_ \_ авторизация**
</dt> <dd> <dl> <dt>



Проверяет изменение политики в отличие от нового соединения.

Фильтрация слоев:

-   \_ \_ \_ Проверка подлинности на уровне фвпм для проверки \_ \_ приема recv \_ V {4 \| 6}
-   \_ \_ \_ Проверка подлинности ALE уровня фвпм для \_ подключения \_ V {4 \| 6}


</dt> </dl> </dd> <dt>

<span id="FWP_CONDITION_FLAG_IS_WILDCARD_BIND"></span><span id="fwp_condition_flag_is_wildcard_bind"></span>**\_флаг условия \_ FWP \_ является \_ привязкой с подстановочными знаками \_**
</dt> <dd> <dl> <dt>



Проверяет, указал ли приложение адрес с подстановочными знаками при привязке к адресу локальной сети.

Слой фильтрации:

-   \_ \_ Назначение ресурса ALE уровня фвпм \_ \_ \_ V {4 \| 6}


</dt> </dl> </dd> <dt>

<span id="FWP_CONDITION_FLAG_IS_RAW_ENDPOINT"></span><span id="fwp_condition_flag_is_raw_endpoint"></span>**\_флаг условия \_ FWP \_ — \_ необработанная \_ Конечная точка**
</dt> <dd> <dl> <dt>



Проверяет, является ли локальная конечная точка, отправляющей и принимающая трафик, конечной точкой необработанных данных.

Фильтрация слоев:

-   ФВПМ \_ уровень \_ входящего \_ транспорта \_ V {4 \| 6}
    > [!Note]  
    > Доступно только в Windows Server 2008, Windows Vista с пакетом обновления 1 (SP1) и более поздних версиях.

     

-   \_Исходящий \_ транспорт уровня фвпм \_ \_ V {4 \| 6}
    > [!Note]  
    > Доступно только в Windows Server 2008, Windows Vista с пакетом обновления 1 (SP1) и более поздних версиях.

     

-   \_ \_ Данные ДАТАГРАММ уровня \_ фвпм \_ {v4 \| 6}
    > [!Note]  
    > Доступно только в Windows Server 2008, Windows Vista с пакетом обновления 1 (SP1) и более поздних версиях.

     

-   \_ \_ Назначение ресурса ALE уровня фвпм \_ \_ \_ V {4 \| 6}
-   \_ \_ \_ Проверка подлинности на уровне фвпм для проверки \_ \_ приема recv \_ V {4 \| 6}
-   \_ \_ \_ Проверка подлинности ALE уровня фвпм для \_ подключения \_ V {4 \| 6}


</dt> </dl> </dd> <dt>

<span id="FWP_CONDITION_FLAG_IS_FRAGMENT"></span><span id="fwp_condition_flag_is_fragment"></span>**\_флаг условия \_ FWP \_ — \_ фрагмент**
</dt> <dd> <dl> <dt>



Проверяет, является ли \_ \_ Структура списка буферных списков, передаваемой драйверу выноски, ФРАГМЕНТОМ IP-пакетов.

Фильтрация слоев:

-   ФВПМ \_ Layer \_ Inbound \_ иппаккет \_ V {4 \| 6}
-   ФВПМ \_ уровень \_ входящего \_ иппаккет \_ V {4 \| 6} \_ Отмена


</dt> </dl> </dd> <dt>

<span id="FWP_CONDITION_FLAG_IS_FRAGMENT_GROUP"></span><span id="fwp_condition_flag_is_fragment_group"></span>**\_флаг условия \_ FWP \_ — \_ Группа фрагментов \_**
</dt> <dd> <dl> <dt>



Проверяет, была ли \_ \_ Структура списка буферных списков, переданная в драйвер выноски, описывает связанный список фрагментов пакетов.

Слой фильтрации:

-   ФВПМ \_ Layer \_ ипфорвард \_ V {4 \| 6}


</dt> </dl> </dd> <dt>

<span id="FWP_CONDITION_FLAG_IS_IPSEC_NATT_RECLASSIFY"></span><span id="fwp_condition_flag_is_ipsec_natt_reclassify"></span>**\_флаг условия \_ FWP \_ — \_ \_ \_ переклассификация IPSec Натт**
</dt> <dd> <dl> <dt>



Указывает, что один и тот же пакет перераспределяется на транспортном уровне, когда оболочка IPsec NAT преобразует значение удаленного порта.


</dt> </dl> </dd> <dt>

<span id="FWP_CONDITION_FLAG_REQUIRES_ALE_CLASSIFY"></span><span id="fwp_condition_flag_requires_ale_classify"></span>**\_флаг условия \_ FWP \_ требует \_ \_ классификации ALE**
</dt> <dd> <dl> <dt>



Указывает, что пакет будет переклассифицирован на уровне получения/принятия ALE.


</dt> </dl> </dd> <dt>

<span id="FWP_CONDITION_FLAG_IS_IMPLICIT_BIND"></span><span id="fwp_condition_flag_is_implicit_bind"></span>**\_флаг условия \_ FWP \_ является \_ неявной \_ привязкой**
</dt> <dd> <dl> <dt>



Проверяет, выполняет ли сокеты Windows неявную привязку.

Доступно только в Windows Vista и Windows Server 2008.


</dt> </dl> </dd> <dt>

<span id="FWP_CONDITION_FLAG_IS_REASSEMBLED"></span><span id="fwp_condition_flag_is_reassembled"></span>**\_флаг условия \_ FWP \_ \_ собран**
</dt> <dd> <dl> <dt>



Проверяет, был ли пакет собран.

> [!Note]  
> Доступно только в Windows Server 2008, Windows Vista с пакетом обновления 1 (SP1) и более поздних версиях.

 

Слой фильтрации:

-   ФВПМ \_ Layer \_ Inbound \_ иппаккет \_ V {4 \| 6}


</dt> </dl> </dd> <dt>

<span id="FWP_CONDITION_FLAG_IS_NAME_APP_SPECIFIED"></span><span id="fwp_condition_flag_is_name_app_specified"></span>**\_флаг условия \_ FWP \_ \_ указан как имя \_ приложения \_**
</dt> <dd> <dl> <dt>



Проверяет, было ли имя однорангового компьютера, к которому ожидается подключение, получено через API, например [**всасетсоккетпиртаржетнаме**](/windows/desktop/api/ws2tcpip/nf-ws2tcpip-wsasetsocketpeertargetname) , и не получено через эвристику кэширования.

> [!Note]  
> Доступно только в Windows Server 2008 R2, Windows 7 и более поздних версиях.

 

Слой фильтрации:

-   \_ \_ \_ Проверка подлинности ALE уровня фвпм для \_ подключения \_ V {4 \| 6}


</dt> </dl> </dd> <dt>

<span id="FWP_CONDITION_FLAG_IS_PROMISCUOUS"></span><span id="fwp_condition_flag_is_promiscuous"></span>**\_флаг условия \_ FWP \_ \_ неизбирательен**
</dt> <dd> <dl> <dt>



Зарезервировано.


</dt> </dl> </dd> <dt>

<span id="FWP_CONDITION_FLAG_IS_AUTH_FW"></span><span id="fwp_condition_flag_is_auth_fw"></span>**\_флаг условия \_ FWP \_ — \_ встроенное по проверки подлинности \_**
</dt> <dd> <dl> <dt>



Проверяет, является ли подключение сквозной проверкой подлинности, даже если отдельные пакеты не были проверены.

> [!Note]  
> Доступно только в Windows Server 2008 R2, Windows 7 и более поздних версиях.

 

Слой фильтрации:

-   \_ \_ \_ Проверка подлинности ALE уровня фвпм для \_ подключения \_ V {4 \| 6}
-   \_ \_ \_ Проверка подлинности на уровне фвпм для проверки \_ \_ приема recv \_ V {4 \| 6}


</dt> </dl> </dd> <dt>

<span id="FWP_CONDITION_FLAG_IS_RECLASSIFY"></span><span id="fwp_condition_flag_is_reclassify"></span>**\_флаг условия \_ FWP \_ \_ реклассификации**
</dt> <dd> <dl> <dt>



Проверяет, реклассифицировать ли обработчик фильтрации предыдущий запрос на привязку или прослушивание.

> [!Note]  
> Доступно только в Windows Server 2008 R2, Windows 7 и более поздних версиях.

 

Слой фильтрации:

-   \_ \_ \_ Прослушивание проверки подлинности ALE уровня фвпм \_ \_ V {4 \| 6}
-   \_ \_ Назначение ресурса ALE уровня фвпм \_ \_ \_ V {4 \| 6}


</dt> </dl> </dd> <dt>

<span id="FWP_CONDITION_FLAG_IS_PROXY_CONNECTION"></span><span id="fwp_condition_flag_is_proxy_connection"></span>**\_флаг условия \_ FWP \_ является \_ прокси- \_ соединением**
</dt> <dd> <dl> <dt>



Проверяет, использует ли соединение прокси-сервер.

> [!Note]  
> Доступно только в Windows 8 и Windows Server 2012.

 


</dt> </dl> </dd> <dt>

<span id="FWP_CONDITION_FLAG_IS_APPCONTAINER_LOOPBACK"></span><span id="fwp_condition_flag_is_appcontainer_loopback"></span>**\_флаг условия \_ FWP \_ — \_ это \_ замыкание APPCONTAINER**
</dt> <dd> <dl> <dt>



Проверяет, является ли сетевой трафик трафиком замыкания на себя контейнера приложений.

> [!Note]  
> Доступно только в Windows 8 и Windows Server 2012.

 


</dt> </dl> </dd> <dt>

<span id="FWP_CONDITION_FLAG_IS_NON_APPCONTAINER_LOOPBACK"></span><span id="fwp_condition_flag_is_non_appcontainer_loopback"></span>**\_флаг условия \_ FWP \_ не \_ является \_ \_ замыканием APPCONTAINER**
</dt> <dd> <dl> <dt>



Проверяет, является ли сетевой трафик трафиком о замыкании на себя для контейнера без приложений.

> [!Note]  
> Доступно только в Windows 8 и Windows Server 2012.

 


</dt> </dl> </dd> <dt>

<span id="FWP_CONDITION_FLAG_IS_RESERVED"></span><span id="fwp_condition_flag_is_reserved"></span>**\_флаг условия \_ FWP \_ \_ зарезервирован**
</dt> <dd> <dl> <dt>



Зарезервировано.


</dt> </dl> </dd> <dt>

<span id="FWP_CONDITION_FLAG_IS_HONORING_POLICY_AUTHORIZE"></span><span id="fwp_condition_flag_is_honoring_policy_authorize"></span>**\_флаг условия \_ FWP \_ \_ учитывает \_ политику \_ авторизации**
</dt> <dd> <dl> <dt>



Указывает, что текущая классификация выполняется для того, чтобы соответствовать намерениям перенаправленного приложения Магазина Windows подключиться к указанному узлу. Такая классификация будет содержать те же значения классификатора полей, что и если приложение никогда не перенаправлялось. Флаг также указывает, что будущая классификация будет вызываться для сопоставления с действующим перенаправленным назначением. Если приложение перенаправляется в прокси-службу для проверки, это также означает, что в прокси-подключении будет вызываться следующая классификация. Драйверы выноски обычно разрешают эту классификацию.

> [!Note]  
> Доступно только в Windows 8 и Windows Server 2012.

 

Слой фильтрации:

-   \_ \_ \_ Проверка подлинности ALE уровня фвпм для \_ подключения \_ V {4 \| 6}


</dt> </dl> </dd> </dl>

Следующие флаги указывают причину повторной авторизации ранее авторизованного подключения. Эти флаги и слои фильтрации, где их можно использовать, определяются следующим образом.

> [!Note]  
> Эти условия фильтрации доступны только в Windows Server 2008 R2, Windows 7 и более поздних версиях.

 

<dl> <dt>

<span id="FWP_CONDITION_REAUTHORIZE_REASON_POLICY_CHANGE"></span><span id="fwp_condition_reauthorize_reason_policy_change"></span>**\_ \_ \_ \_ изменение политики по причине ПОВТОРНОй авторизации условия FWP \_**
</dt> <dd> <dl> <dt>



Указывает, что соединение было повторно создано из-за добавления или удаления фильтров.

Слой фильтрации:

-   \_ \_ \_ Проверка подлинности ALE уровня фвпм для \_ подключения \_ V {4 \| 6}
-   \_ \_ \_ Проверка подлинности на уровне фвпм для проверки \_ \_ приема recv \_ V {4 \| 6}


</dt> </dl> </dd> <dt>

<span id="FWP_CONDITION_REAUTHORIZE_REASON_NEW_ARRIVAL_INTERFACE"></span><span id="fwp_condition_reauthorize_reason_new_arrival_interface"></span>**FWP \_ условия повторной \_ авторизации — \_ \_ новый \_ \_ интерфейс прибытия**
</dt> <dd> <dl> <dt>



Указывает, что пакет был получен из неизвестного интерфейса.

Слой фильтрации:

-   \_ \_ \_ Проверка подлинности ALE уровня фвпм для \_ подключения \_ V {4 \| 6}
-   \_ \_ \_ Проверка подлинности на уровне фвпм для проверки \_ \_ приема recv \_ V {4 \| 6}


</dt> </dl> </dd> <dt>

<span id="FWP_CONDITION_REAUTHORIZE_REASON_NEW_NEXTHOP_INTERFACE"></span><span id="fwp_condition_reauthorize_reason_new_nexthop_interface"></span>**FWP \_ условия повторной \_ авторизации, \_ Причина \_ нового \_ \_ интерфейса NEXTHOP**
</dt> <dd> <dl> <dt>



Указывает, что пакет будет относиться к неизвестному интерфейсу.

Слой фильтрации:

-   \_ \_ \_ Проверка подлинности ALE уровня фвпм для \_ подключения \_ V {4 \| 6}
-   \_ \_ \_ Проверка подлинности на уровне фвпм для проверки \_ \_ приема recv \_ V {4 \| 6}


</dt> </dl> </dd> <dt>

<span id="FWP_CONDITION_REAUTHORIZE_REASON_PROFILE_CROSSING"></span><span id="fwp_condition_reauthorize_reason_profile_crossing"></span>**\_пересечение \_ \_ \_ профиля причины \_ FWP условия авторизации**
</dt> <dd> <dl> <dt>



Указывает, что пакет прошел через интерфейсы более чем одной категории сети.

Слой фильтрации:

-   \_ \_ \_ Проверка подлинности ALE уровня фвпм для \_ подключения \_ V {4 \| 6}
-   \_ \_ \_ Проверка подлинности на уровне фвпм для проверки \_ \_ приема recv \_ V {4 \| 6}


</dt> </dl> </dd> <dt>

<span id="FWP_CONDITION_REAUTHORIZE_REASON_CLASSIFY_COMPLETION"></span><span id="fwp_condition_reauthorize_reason_classify_completion"></span>**FWP \_ условия повторной \_ авторизации \_ причины \_ \_ завершения классификации**
</dt> <dd> <dl> <dt>



Указывает, что теперь разрешено выполнение ранее удерживаемого подключения.

Слой фильтрации:

-   \_ \_ \_ Проверка подлинности ALE уровня фвпм для \_ подключения \_ V {4 \| 6}
-   \_ \_ \_ Проверка подлинности на уровне фвпм для проверки \_ \_ приема recv \_ V {4 \| 6}


</dt> </dl> </dd> <dt>

<span id="FWP_CONDITION_REAUTHORIZE_REASON_IPSEC_PROPERTIES_CHANGED"></span><span id="fwp_condition_reauthorize_reason_ipsec_properties_changed"></span>**FWP \_ условия повторной \_ авторизации \_ причины \_ \_ изменения свойств IPSec \_**
</dt> <dd> <dl> <dt>



Указывает, что свойства IPsec изменились или что соединение было изменено с открытого текста на безопасное соединение.

Слой фильтрации:

-   \_ \_ \_ Проверка подлинности ALE уровня фвпм для \_ подключения \_ V {4 \| 6}
-   \_ \_ \_ Проверка подлинности на уровне фвпм для проверки \_ \_ приема recv \_ V {4 \| 6}


</dt> </dl> </dd> <dt>

<span id="FWP_CONDITION_REAUTHORIZE_REASON_MID_STREAM_INSPECTION"></span><span id="fwp_condition_reauthorize_reason_mid_stream_inspection"></span>**FWP \_ условия повторной \_ авторизации \_ Причина \_ средней \_ \_ проверки потока**
</dt> <dd> <dl> <dt>



Указывает, что ранее установленное подключение TCP проверяется.

Слой фильтрации:

-   \_ \_ \_ Проверка подлинности ALE уровня фвпм для \_ подключения \_ V {4 \| 6}
-   \_ \_ \_ Проверка подлинности на уровне фвпм для проверки \_ \_ приема recv \_ V {4 \| 6}


</dt> </dl> </dd> <dt>

<span id="FWP_CONDITION_REAUTHORIZE_REASON_SOCKET_PROPERTY_CHANGED"></span><span id="fwp_condition_reauthorize_reason_socket_property_changed"></span>**\_ \_ \_ \_ изменено свойство сокета причины \_ \_ повторной авторизации FWP**
</dt> <dd> <dl> <dt>



Указывает, что свойства сокета были установлены после авторизации и установления соединения.

Слой фильтрации:

-   \_ \_ \_ Проверка подлинности ALE уровня фвпм для \_ подключения \_ V {4 \| 6}
-   \_ \_ \_ Проверка подлинности на уровне фвпм для проверки \_ \_ приема recv \_ V {4 \| 6}


</dt> </dl> </dd> <dt>

<span id="FWP_CONDITION_REAUTHORIZE_REASON_NEW_INBOUND_MCAST_BCAST_PACKET"></span><span id="fwp_condition_reauthorize_reason_new_inbound_mcast_bcast_packet"></span>**FWP \_ условия повторно \_ авторизовать \_ \_ новый \_ входящий \_ \_ пакет бкаст мкаст \_**
</dt> <dd> <dl> <dt>



Указывает, что новые Входящие многоадресные или широковещательные пакеты допускают повторную авторизацию в \_ \_ выносках приема на получение Ale.

Слой фильтрации:

-   \_ \_ \_ Проверка подлинности на уровне фвпм для проверки \_ \_ приема recv \_ V {4 \| 6}


</dt> </dl> </dd> </dl>

Следующие флаги задают свойства сокета, которые связаны с тем, требуется ли приложению получать трафик обхода по периметру. Эти флаги и слои фильтрации, где их можно использовать, определяются следующим образом.

> [!Note]  
> Эти условия фильтрации доступны только в Windows Server 2008 R2, Windows 7 и более поздних версиях.

 

<dl> <dt>

<span id="FWP_CONDITION_SOCKET_PROPERTY_FLAG_IS_SYSTEM_PORT_RPC"></span><span id="fwp_condition_socket_property_flag_is_system_port_rpc"></span>**\_ \_ флаг свойства сокета FWP условия \_ \_ \_ является \_ системным \_ портом \_ RPC**
</dt> <dd> <dl> <dt>



Указывает, что приложение взаимодействует с динамическим портом RPC.

Слой фильтрации:

-   \_ \_ \_ Прослушивание проверки подлинности ALE уровня фвпм \_ \_ V {4 \| 6}
-   \_ \_ Назначение ресурса ALE уровня фвпм \_ \_ \_ V {4 \| 6}


</dt> </dl> </dd> <dt>

<span id="FWP_CONDITION_SOCKET_PROPERTY_FLAG_ALLOW_EDGE_TRAFFIC"></span><span id="fwp_condition_socket_property_flag_allow_edge_traffic"></span>**\_ \_ флаг свойства сокета FWP условия \_ \_ \_ разрешения \_ пограничных \_ данных**
</dt> <dd> <dl> <dt>



Указывает, что приложению требуется получить трафик, относящийся к обходу узлов.

Слой фильтрации:

-   \_ \_ \_ Прослушивание проверки подлинности ALE уровня фвпм \_ \_ V {4 \| 6}
-   \_ \_ Назначение ресурса ALE уровня фвпм \_ \_ \_ V {4 \| 6}


</dt> </dl> </dd> <dt>

<span id="FWP_CONDITION_SOCKET_PROPERTY_FLAG_DENY_EDGE_TRAFFIC"></span><span id="fwp_condition_socket_property_flag_deny_edge_traffic"></span>**\_ \_ флаг свойства сокета FWP условия \_ \_ \_ запрета \_ пограничных \_ данных**
</dt> <dd> <dl> <dt>



Указывает, что приложению не требуется получение или обработка трафика, относящегося к обходу пограничной сети.

Слой фильтрации:

-   \_ \_ \_ Прослушивание проверки подлинности ALE уровня фвпм \_ \_ V {4 \| 6}
-   \_ \_ Назначение ресурса ALE уровня фвпм \_ \_ \_ V {4 \| 6}


</dt> </dl> </dd> </dl>

Следующие флаги указывают сведения о соединении, связанные с фильтрацией L2.

> [!Note]  
> Эти условия фильтрации доступны только в Windows 8 и Windows Server 2012.

 

<dl> <dt>

<span id="FWP_CONDITION_L2_IS_NATIVE_ETHERNET"></span><span id="fwp_condition_l2_is_native_ethernet"></span>**\_Условие FWP \_ L2 \_ — \_ собственная \_ сеть Ethernet**
</dt> <dd> <dl> <dt>



Указывает, что соединение является собственным Ethernet.

Слой фильтрации:

-   ФВПМ \_ Layer \_ входящего трафика \_ Mac \_ Frame \_ Ethernet
-   \_ \_ \_ \_ машинный кадр входящего Mac-кадра \_ уровня фвпм
-   \_ \_ \_ \_ Ethernet-кадр исходящего уровня фвпм \_
-   \_ \_ \_ машинный кадр исходящего Mac-уровня \_ фвпм \_


</dt> </dl> </dd> <dt>

<span id="FWP_CONDITION_L2_IS_WIFI"></span><span id="fwp_condition_l2_is_wifi"></span>**\_Условие FWP \_ L2 \_ — \_ Wi-Fi**
</dt> <dd> <dl> <dt>



Указывает, что подключение является Wi-Fi.

Слой фильтрации:

-   ФВПМ \_ Layer \_ входящего трафика \_ Mac \_ Frame \_ Ethernet
-   \_ \_ \_ \_ машинный кадр входящего Mac-кадра \_ уровня фвпм
-   \_ \_ \_ \_ Ethernet-кадр исходящего уровня фвпм \_
-   \_ \_ \_ машинный кадр исходящего Mac-уровня \_ фвпм \_


</dt> </dl> </dd> <dt>

<span id="FWP_CONDITION_L2_IS_MOBILE_BROADBAND"></span><span id="fwp_condition_l2_is_mobile_broadband"></span>**\_Условие FWP \_ L2 \_ — \_ мобильное \_ широкополосное подключение**
</dt> <dd> <dl> <dt>



Указывает, что подключение является мобильным широкополосным.

Слой фильтрации:

-   ФВПМ \_ Layer \_ входящего трафика \_ Mac \_ Frame \_ Ethernet
-   \_ \_ \_ \_ машинный кадр входящего Mac-кадра \_ уровня фвпм
-   \_ \_ \_ \_ Ethernet-кадр исходящего уровня фвпм \_
-   \_ \_ \_ машинный кадр исходящего Mac-уровня \_ фвпм \_


</dt> </dl> </dd> <dt>

<span id="FWP_CONDITION_L2_IS_WIFI_DIRECT_DATA"></span><span id="fwp_condition_l2_is_wifi_direct_data"></span>**\_Условие FWP \_ L2 \_ — \_ \_ прямые \_ данные WiFi**
</dt> <dd> <dl> <dt>



Указывает, что соединение Wi-Fi напрямую.

Слой фильтрации:

-   ФВПМ \_ Layer \_ входящего трафика \_ Mac \_ Frame \_ Ethernet
-   \_ \_ \_ \_ машинный кадр входящего Mac-кадра \_ уровня фвпм
-   \_ \_ \_ \_ Ethernet-кадр исходящего уровня фвпм \_
-   \_ \_ \_ машинный кадр исходящего Mac-уровня \_ фвпм \_


</dt> </dl> </dd> <dt>

<span id="FWP_CONDITION_L2_IS_VM2VM"></span><span id="fwp_condition_l2_is_vm2vm"></span>**\_Условие FWP \_ L2 \_ — \_ VM2VM**
</dt> <dd> <dl> <dt>



Указывает, что соединение установлено между виртуальными машинами.

Слой фильтрации:

-   ФВПМ \_ Layer \_ входящего трафика \_ Mac \_ Frame \_ Ethernet
-   \_ \_ \_ \_ машинный кадр входящего Mac-кадра \_ уровня фвпм
-   \_ \_ \_ \_ Ethernet-кадр исходящего уровня фвпм \_
-   \_ \_ \_ машинный кадр исходящего Mac-уровня \_ фвпм \_


</dt> </dl> </dd> <dt>

<span id="FWP_CONDITION_L2_IS_MALFORMED_PACKET"></span><span id="fwp_condition_l2_is_malformed_packet"></span>**\_Условие FWP \_ L2 \_ имеет \_ неправильный формат \_ пакета**
</dt> <dd> <dl> <dt>



Указывает, что пакет выглядит неправильно.

Слой фильтрации:

-   ФВПМ \_ Layer \_ входящего трафика \_ Mac \_ Frame \_ Ethernet
-   \_ \_ \_ \_ машинный кадр входящего Mac-кадра \_ уровня фвпм
-   \_ \_ \_ \_ Ethernet-кадр исходящего уровня фвпм \_
-   \_ \_ \_ машинный кадр исходящего Mac-уровня \_ фвпм \_


</dt> </dl> </dd> <dt>

<span id="FWP_CONDITION_L2_IS_IP_FRAGMENT_GROUP"></span><span id="fwp_condition_l2_is_ip_fragment_group"></span>**\_Условие FWP \_ L2 \_ — \_ \_ Группа фрагментов IP-адресов \_**
</dt> <dd> <dl> <dt>



Указывает группу фрагментов IP-пакетов.

Слой фильтрации:

-   ФВПМ \_ Layer \_ входящего трафика \_ Mac \_ Frame \_ Ethernet
-   \_ \_ \_ \_ машинный кадр входящего Mac-кадра \_ уровня фвпм
-   \_ \_ \_ \_ Ethernet-кадр исходящего уровня фвпм \_
-   \_ \_ \_ машинный кадр исходящего Mac-уровня \_ фвпм \_


</dt> </dl> </dd> <dt>

<span id="FWP_CONDITION_L2_IF_CONNECTOR_PRESENT"></span><span id="fwp_condition_l2_if_connector_present"></span>**\_Условие FWP \_ L2 \_ , \_ Если \_ имеется соединитель**
</dt> <dd> <dl> <dt>



Указывает, что имеется соединитель.

Слой фильтрации:

-   ФВПМ \_ Layer \_ входящего трафика \_ Mac \_ Frame \_ Ethernet
-   \_ \_ \_ \_ машинный кадр входящего Mac-кадра \_ уровня фвпм
-   \_ \_ \_ \_ Ethernet-кадр исходящего уровня фвпм \_
-   \_ \_ \_ машинный кадр исходящего Mac-уровня \_ фвпм \_


</dt> </dl> </dd> </dl>

## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Только для \[ классических приложений Windows Vista\]<br/>                                        |
| Минимальная версия сервера<br/> | \[Только для настольных приложений Windows Server 2008\]<br/>                                  |
| Header<br/>                   | <dl> <dt>Фвптипес. h</dt> </dl> |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[**Фильтрация идентификаторов слоя**](management-filtering-layer-identifiers-.md)
</dt> </dl>

 

