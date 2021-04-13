---
title: Коды ошибок WFP (Winerror.h)
description: (WFP) коды ошибок.
ms.assetid: 11f3085a-f044-4a78-b47a-59b9086562bf
topic_type:
- apiref
api_name:
- FWP_E_CALLOUT_NOT_FOUND
- FWP_E_CONDITION_NOT_FOUND
- FWP_E_FILTER_NOT_FOUND
- FWP_E_LAYER_NOT_FOUND
- FWP_E_PROVIDER_NOT_FOUND
- FWP_E_PROVIDER_CONTEXT_NOT_FOUND
- FWP_E_SUBLAYER_NOT_FOUND
- FWP_E_NOT_FOUND
- FWP_E_ALREADY_EXISTS
- FWP_E_IN_USE
- FWP_E_DYNAMIC_SESSION_IN_PROGRESS
- FWP_E_WRONG_SESSION
- FWP_E_NO_TXN_IN_PROGRESS
- FWP_E_TXN_IN_PROGRESS
- FWP_E_TXN_ABORTED
- FWP_E_SESSION_ABORTED
- FWP_E_INCOMPATIBLE_TXN
- FWP_E_TIMEOUT
- FWP_E_NET_EVENTS_DISABLED
- FWP_E_INCOMPATIBLE_LAYER
- FWP_E_KM_CLIENTS_ONLY
- FWP_E_LIFETIME_MISMATCH
- FWP_E_BUILTIN_OBJECT
- FWP_E_TOO_MANY_CALLOUTS
- FWP_E_NOTIFICATION_DROPPED
- FWP_E_TRAFFIC_MISMATCH
- FWP_E_INCOMPATIBLE_SA_STATE
- FWP_E_NULL_POINTER
- FWP_E_INVALID_ENUMERATOR
- FWP_E_INVALID_FLAGS
- FWP_E_INVALID_NET_MASK
- FWP_E_INVALID_RANGE
- FWP_E_INVALID_INTERVAL
- FWP_E_ZERO_LENGTH_ARRAY
- FWP_E_NULL_DISPLAY_NAME
- FWP_E_INVALID_ACTION_TYPE
- FWP_E_INVALID_WEIGHT
- FWP_E_MATCH_TYPE_MISMATCH
- FWP_E_TYPE_MISMATCH
- FWP_E_OUT_OF_BOUNDS
- FWP_E_RESERVED
- FWP_E_DUPLICATE_CONDITION
- FWP_E_DUPLICATE_KEYMOD
- FWP_E_ACTION_INCOMPATIBLE_WITH_LAYER
- FWP_E_ACTION_INCOMPATIBLE_WITH_SUBLAYER
- FWP_E_CONTEXT_INCOMPATIBLE_WITH_LAYER
- FWP_E_CONTEXT_INCOMPATIBLE_WITH_CALLOUT
- FWP_E_INCOMPATIBLE_AUTH_METHOD
- FWP_E_INCOMPATIBLE_DH_GROUP
- FWP_E_EM_NOT_SUPPORTED
- FWP_E_NEVER_MATCH
- FWP_E_PROVIDER_CONTEXT_MISMATCH
- FWP_E_INVALID_PARAMETER
- FWP_E_TOO_MANY_SUBLAYERS
- FWP_E_CALLOUT_NOTIFICATION_FAILED
- FWP_E_INVALID_AUTH_TRANSFORM
- FWP_E_INVALID_CIPHER_TRANSFORM
api_location:
- winerror.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4a0e7ee1ab0364a31f136f0c0cdbf87f459225b1
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104491727"
---
# <a name="wfp-error-codes"></a>Коды ошибок WFP

Коды ошибок, характерные для платформы фильтрации Windows (WFP), приведены ниже.

<dl> <dt>

<span id="FWP_E_CALLOUT_NOT_FOUND"></span><span id="fwp_e_callout_not_found"></span>**\_ \_ выноска FWP \_ не \_ найдена**
</dt> <dd> <dl> <dt>

0x80320001
</dt> <dt>



Выноска не существует.


</dt> </dl> </dd> <dt>

<span id="FWP_E_CONDITION_NOT_FOUND"></span><span id="fwp_e_condition_not_found"></span>**\_условие FWP \_ E \_ не \_ Найдено**
</dt> <dd> <dl> <dt>

0x80320002
</dt> <dt>



Условие фильтра не существует.


</dt> </dl> </dd> <dt>

<span id="FWP_E_FILTER_NOT_FOUND"></span><span id="fwp_e_filter_not_found"></span>**\_Фильтр FWP \_ E \_ не \_ найден**
</dt> <dd> <dl> <dt>

0x80320003
</dt> <dt>



Фильтр не существует.


</dt> </dl> </dd> <dt>

<span id="FWP_E_LAYER_NOT_FOUND"></span><span id="fwp_e_layer_not_found"></span>**\_слой FWP \_ E \_ не \_ найден**
</dt> <dd> <dl> <dt>

0x80320004
</dt> <dt>



Слой не существует.


</dt> </dl> </dd> <dt>

<span id="FWP_E_PROVIDER_NOT_FOUND"></span><span id="fwp_e_provider_not_found"></span>**\_поставщик FWP \_ E \_ не \_ найден**
</dt> <dd> <dl> <dt>

0x80320005
</dt> <dt>



Поставщик не существует.


</dt> </dl> </dd> <dt>

<span id="FWP_E_PROVIDER_CONTEXT_NOT_FOUND"></span><span id="fwp_e_provider_context_not_found"></span>**\_ \_ \_ \_ не \_ найден контекст поставщика FWP E**
</dt> <dd> <dl> <dt>

0x80320006
</dt> <dt>



Контекст поставщика не существует.


</dt> </dl> </dd> <dt>

<span id="FWP_E_SUBLAYER_NOT_FOUND"></span><span id="fwp_e_sublayer_not_found"></span>**подслой FWP \_ E \_ \_ не \_ найден**
</dt> <dd> <dl> <dt>

0x80320007
</dt> <dt>



Подуровень не существует.


</dt> </dl> </dd> <dt>

<span id="FWP_E_NOT_FOUND"></span><span id="fwp_e_not_found"></span>**FWP \_ E \_ не \_ найден**
</dt> <dd> <dl> <dt>

0x80320008
</dt> <dt>



Объект не существует.

Функции [ипсексаконтекст \* ](fwp-ipsec-functions.md) возвращают эту ошибку, если идентификатор контекста SA не найден.


</dt> </dl> </dd> <dt>

<span id="FWP_E_ALREADY_EXISTS"></span><span id="fwp_e_already_exists"></span>**FWP \_ E \_ уже \_ существует**
</dt> <dd> <dl> <dt>

0x80320009
</dt> <dt>



Объект с таким GUID или LUID уже существует.


</dt> </dl> </dd> <dt>

<span id="FWP_E_IN_USE"></span><span id="fwp_e_in_use"></span>**\_используется FWP \_ E \_**
</dt> <dd> <dl> <dt>

0x8032000A
</dt> <dt>



На объект ссылаются другие объекты, поэтому его нельзя удалить.


</dt> </dl> </dd> <dt>

<span id="FWP_E_DYNAMIC_SESSION_IN_PROGRESS"></span><span id="fwp_e_dynamic_session_in_progress"></span>**\_ \_ \_ выполняется динамический сеанс \_ \_ FWP E**
</dt> <dd> <dl> <dt>

0x8032000B
</dt> <dt>



В динамическом сеансе вызов не разрешен.


</dt> </dl> </dd> <dt>

<span id="FWP_E_WRONG_SESSION"></span><span id="fwp_e_wrong_session"></span>**FWP \_ \_ неверного \_ сеанса**
</dt> <dd> <dl> <dt>

0x8032000C
</dt> <dt>



Вызов был сделан из неверного сеанса, поэтому его невозможно завершить.


</dt> </dl> </dd> <dt>

<span id="FWP_E_NO_TXN_IN_PROGRESS"></span><span id="fwp_e_no_txn_in_progress"></span>**FWP \_ е \_ \_ транзакция не \_ \_ выполняется**
</dt> <dd> <dl> <dt>

0x8032000D
</dt> <dt>



Вызов должен быть выполнен в явной транзакции.


</dt> </dl> </dd> <dt>

<span id="FWP_E_TXN_IN_PROGRESS"></span><span id="fwp_e_txn_in_progress"></span>**\_выполняется FWP E \_ транзакция \_ \_**
</dt> <dd> <dl> <dt>

0x8032000E
</dt> <dt>



Вызов не разрешен в явной транзакции.


</dt> </dl> </dd> <dt>

<span id="FWP_E_TXN_ABORTED"></span><span id="fwp_e_txn_aborted"></span>**FWP \_ E \_ транзакция \_ прервано**
</dt> <dd> <dl> <dt>

0x8032000F
</dt> <dt>



Явная транзакция была принудительно отменена.


</dt> </dl> </dd> <dt>

<span id="FWP_E_SESSION_ABORTED"></span><span id="fwp_e_session_aborted"></span>**\_сеанс FWP \_ E \_ прерван**
</dt> <dd> <dl> <dt>

0x80320010
</dt> <dt>



Сеанс был отменен.

Необходимо закрыть этот обработчик, вызвав [**FwpmEngineClose0**](/windows/desktop/api/Fwpmu/nf-fwpmu-fwpmengineclose0), несмотря на то, что он больше не является допустимым; в противном случае состояние на стороне клиента будет утечкой. Новый сеанс должен быть создан путем вызова [**FwpmEngineOpen0**](/windows/desktop/api/Fwpmu/nf-fwpmu-fwpmengineopen0).


</dt> </dl> </dd> <dt>

<span id="FWP_E_INCOMPATIBLE_TXN"></span><span id="fwp_e_incompatible_txn"></span>**FWP \_ E \_ несовместимый \_ транзакция**
</dt> <dd> <dl> <dt>

0x80320011
</dt> <dt>



Вызов не разрешен из транзакции, доступной только для чтения.


</dt> </dl> </dd> <dt>

<span id="FWP_E_TIMEOUT"></span><span id="fwp_e_timeout"></span>**FWP \_ E \_ timeout**
</dt> <dd> <dl> <dt>

0x80320012
</dt> <dt>



Истекло время ожидания вызова при ожидании получения блокировки транзакции.


</dt> </dl> </dd> <dt>

<span id="FWP_E_NET_EVENTS_DISABLED"></span><span id="fwp_e_net_events_disabled"></span>**\_ \_ \_ Отключенные события FWP E NET \_**
</dt> <dd> <dl> <dt>

0x80320013
</dt> <dt>



Сбор событий диагностики сети отключен.


</dt> </dl> </dd> <dt>

<span id="FWP_E_INCOMPATIBLE_LAYER"></span><span id="fwp_e_incompatible_layer"></span>**\_ \_ несовместимый слой FWP \_ E**
</dt> <dd> <dl> <dt>

0x80320014
</dt> <dt>



Операция не поддерживается указанным слоем.


</dt> </dl> </dd> <dt>

<span id="FWP_E_KM_CLIENTS_ONLY"></span><span id="fwp_e_km_clients_only"></span>**\_ \_ \_ только клиенты FWP км \_**
</dt> <dd> <dl> <dt>

0x80320015
</dt> <dt>



Вызов разрешен только для вызывающих методов режима ядра.


</dt> </dl> </dd> <dt>

<span id="FWP_E_LIFETIME_MISMATCH"></span><span id="fwp_e_lifetime_mismatch"></span>**\_несоответствие \_ времени существования FWP E \_**
</dt> <dd> <dl> <dt>

0x80320016
</dt> <dt>



Вызов попытался связать два объекта с несовместимыми временами существования.

Дополнительные сведения о времени существования объектов и ассоциации объектов см. в разделе [Управление объектами](object-management.md) .


</dt> </dl> </dd> <dt>

<span id="FWP_E_BUILTIN_OBJECT"></span><span id="fwp_e_builtin_object"></span>**\_ \_ встроенный объект FWP E \_**
</dt> <dd> <dl> <dt>

0x80320017
</dt> <dt>



Объект является встроенным, поэтому его нельзя удалить.


</dt> </dl> </dd> <dt>

<span id="FWP_E_TOO_MANY_CALLOUTS"></span><span id="fwp_e_too_many_callouts"></span>**FWP \_ \_ слишком \_ много \_ выносок**
</dt> <dd> <dl> <dt>

0x80320018
</dt> <dt>



Достигнуто максимальное число выносок.

В большинстве случаев 100 000 выноски могут быть зарегистрированы одновременно.


</dt> </dl> </dd> <dt>

<span id="FWP_E_NOTIFICATION_DROPPED"></span><span id="fwp_e_notification_dropped"></span>**FWP \_ \_ уведомления \_ удалено**
</dt> <dd> <dl> <dt>

0x80320019
</dt> <dt>



Не удалось доставить уведомление, так как достигнута максимальная емкость очереди сообщений.


</dt> </dl> </dd> <dt>

<span id="FWP_E_TRAFFIC_MISMATCH"></span><span id="fwp_e_traffic_mismatch"></span>**\_несоответствие \_ трафика FWP E \_**
</dt> <dd> <dl> <dt>

0x8032001A
</dt> <dt>



Параметры сетевого трафика не соответствуют контексту сопоставления безопасности.

[**IPsecSaContextGetSpi0**](/windows/desktop/api/Fwpmu/nf-fwpmu-ipsecsacontextgetspi0) можно вызывать несколько раз, но вызывающий объект должен указать один и тот же [**\_ TRAFFIC0 IPSec**](/windows/desktop/api/Ipsectypes/ns-ipsectypes-ipsec_traffic0) каждый раз. Эта ошибка возвращается, если последующий вызов предоставляет другой **\_ TRAFFIC0 IPSec**.


</dt> </dl> </dd> <dt>

<span id="FWP_E_INCOMPATIBLE_SA_STATE"></span><span id="fwp_e_incompatible_sa_state"></span>**FWP \_ E \_ несовместимое \_ \_ состояние SA**
</dt> <dd> <dl> <dt>

0x8032001B
</dt> <dt>



Вызов не разрешен для текущего состояния сопоставления безопасности (SA).

Функции контекста SA должны вызываться в определенном порядке:

-   [**IPsecSaContextCreate0**](/windows/desktop/api/Fwpmu/nf-fwpmu-ipsecsacontextcreate0)
-   [**IPsecSaContextGetSpi0**](/windows/desktop/api/Fwpmu/nf-fwpmu-ipsecsacontextgetspi0)
-   [**IPsecSaContextAddInbound0**](/windows/desktop/api/Fwpmu/nf-fwpmu-ipsecsacontextaddinbound0)
-   [**IPsecSaContextAddOutbound0**](/windows/desktop/api/Fwpmu/nf-fwpmu-ipsecsacontextaddoutbound0)

Эта ошибка возвращается, если они вызываются неупорядоченно.


</dt> </dl> </dd> <dt>

<span id="FWP_E_NULL_POINTER"></span><span id="fwp_e_null_pointer"></span>**FWP \_ \_ указатель null \_**
</dt> <dd> <dl> <dt>

0x8032001C
</dt> <dt>



Обязательный указатель имеет значение null.


</dt> </dl> </dd> <dt>

<span id="FWP_E_INVALID_ENUMERATOR"></span><span id="fwp_e_invalid_enumerator"></span>**FWP \_ E \_ Недопустимый \_ перечислитель**
</dt> <dd> <dl> <dt>

0x8032001D
</dt> <dt>



Значение перечислителя в структуре выходит за пределы допустимого диапазона.


</dt> </dl> </dd> <dt>

<span id="FWP_E_INVALID_FLAGS"></span><span id="fwp_e_invalid_flags"></span>**FWP \_ E \_ недопустимые \_ Флаги**
</dt> <dd> <dl> <dt>

0x8032001E
</dt> <dt>



Поле flags содержит недопустимое значение.


</dt> </dl> </dd> <dt>

<span id="FWP_E_INVALID_NET_MASK"></span><span id="fwp_e_invalid_net_mask"></span>**FWP \_ E \_ Недопустимая \_ Сетевая \_ Маска**
</dt> <dd> <dl> <dt>

0x8032001F
</dt> <dt>



Недопустимая маска сети.


</dt> </dl> </dd> <dt>

<span id="FWP_E_INVALID_RANGE"></span><span id="fwp_e_invalid_range"></span>**FWP \_ E \_ Недопустимый \_ диапазон**
</dt> <dd> <dl> <dt>

0x80320020
</dt> <dt>



Недопустимая структура [**\_ RANGE0 FWP**](/windows/desktop/api/Fwptypes/ns-fwptypes-fwp_range0) .


</dt> </dl> </dd> <dt>

<span id="FWP_E_INVALID_INTERVAL"></span><span id="fwp_e_invalid_interval"></span>**FWP \_ E — \_ Недопустимый \_ интервал**
</dt> <dd> <dl> <dt>

0x80320021
</dt> <dt>



Недопустимый интервал времени.


</dt> </dl> </dd> <dt>

<span id="FWP_E_ZERO_LENGTH_ARRAY"></span><span id="fwp_e_zero_length_array"></span>**FWP \_ \_ массив нулевой \_ длины \_**
</dt> <dd> <dl> <dt>

0x80320022
</dt> <dt>



Массив, который должен содержать хотя бы один элемент, имеет нулевую длину.


</dt> </dl> </dd> <dt>

<span id="FWP_E_NULL_DISPLAY_NAME"></span><span id="fwp_e_null_display_name"></span>**FWP \_ E \_ , \_ отображаемое \_ имя null**
</dt> <dd> <dl> <dt>

0x80320023
</dt> <dt>



Поле **displayData.Name** не может иметь значение null.


</dt> </dl> </dd> <dt>

<span id="FWP_E_INVALID_ACTION_TYPE"></span><span id="fwp_e_invalid_action_type"></span>**FWP \_ E \_ Недопустимый \_ \_ тип действия**
</dt> <dd> <dl> <dt>

0x80320024
</dt> <dt>



Тип действия не является допустимым типом действия для фильтра.


</dt> </dl> </dd> <dt>

<span id="FWP_E_INVALID_WEIGHT"></span><span id="fwp_e_invalid_weight"></span>**FWP \_ E \_ Недопустимый \_ вес**
</dt> <dd> <dl> <dt>

0x80320025
</dt> <dt>



Недопустимый вес фильтра.

Дополнительные сведения см. в разделе [назначение веса фильтра](filter-weight-assignment.md) .


</dt> </dl> </dd> <dt>

<span id="FWP_E_MATCH_TYPE_MISMATCH"></span><span id="fwp_e_match_type_mismatch"></span>**\_несоответствие \_ типа сопоставления FWP E \_ \_**
</dt> <dd> <dl> <dt>

0x80320026
</dt> <dt>



Условие фильтра содержит тип соответствия, несовместимый с операндами.

Дополнительные сведения см. в разделе [**FWP \_ Match \_ Type**](/windows/desktop/api/Fwptypes/ne-fwptypes-fwp_match_type) .


</dt> </dl> </dd> <dt>

<span id="FWP_E_TYPE_MISMATCH"></span><span id="fwp_e_type_mismatch"></span>**\_несоответствие \_ типов FWP E \_**
</dt> <dd> <dl> <dt>

0x80320027
</dt> <dt>



Структура [**\_ VALUE0 FWP**](/windows/desktop/api/Fwptypes/ns-fwptypes-fwp_value0) или [**фвпм \_ условие \_ VALUE0**](/windows/desktop/api/Fwptypes/ns-fwptypes-fwp_condition_value0) имеет неверный тип.


</dt> </dl> </dd> <dt>

<span id="FWP_E_OUT_OF_BOUNDS"></span><span id="fwp_e_out_of_bounds"></span>**FWP \_ из \_ \_ \_ границ**
</dt> <dd> <dl> <dt>

0x80320028
</dt> <dt>



Целочисленное значение находится за пределами допустимого диапазона.


</dt> </dl> </dd> <dt>

<span id="FWP_E_RESERVED"></span><span id="fwp_e_reserved"></span>**FWP \_ е \_ зарезервировано**
</dt> <dd> <dl> <dt>

0x80320029
</dt> <dt>



Зарезервированное поле не равно нулю.


</dt> </dl> </dd> <dt>

<span id="FWP_E_DUPLICATE_CONDITION"></span><span id="fwp_e_duplicate_condition"></span>**FWP \_ , \_ повторяющееся \_ условие**
</dt> <dd> <dl> <dt>

0x8032002A
</dt> <dt>



Фильтр не может содержать несколько условий, работающих с одним полем.


</dt> </dl> </dd> <dt>

<span id="FWP_E_DUPLICATE_KEYMOD"></span><span id="fwp_e_duplicate_keymod"></span>**FWP \_ E \_ дубликат \_ кэймод**
</dt> <dd> <dl> <dt>

0x8032002B
</dt> <dt>



Политика не может содержать один и тот же модуль ключа более одного раза.


</dt> </dl> </dd> <dt>

<span id="FWP_E_ACTION_INCOMPATIBLE_WITH_LAYER"></span><span id="fwp_e_action_incompatible_with_layer"></span>**FWP \_ \_ действие \_ несовместимо \_ с \_ слоем**
</dt> <dd> <dl> <dt>

0x8032002C
</dt> <dt>



Тип действия несовместим с уровнем.


</dt> </dl> </dd> <dt>

<span id="FWP_E_ACTION_INCOMPATIBLE_WITH_SUBLAYER"></span><span id="fwp_e_action_incompatible_with_sublayer"></span>**FWP \_ \_ действие \_ несовместимо \_ с \_ подслоем**
</dt> <dd> <dl> <dt>

0x8032002D
</dt> <dt>



Тип действия несовместим с подслоем.


</dt> </dl> </dd> <dt>

<span id="FWP_E_CONTEXT_INCOMPATIBLE_WITH_LAYER"></span><span id="fwp_e_context_incompatible_with_layer"></span>**\_контекст FWP \_ E \_ несовместим \_ с \_ слоем**
</dt> <dd> <dl> <dt>

0x8032002E
</dt> <dt>



Необработанный контекст или контекст поставщика несовместим с уровнем.


</dt> </dl> </dd> <dt>

<span id="FWP_E_CONTEXT_INCOMPATIBLE_WITH_CALLOUT"></span><span id="fwp_e_context_incompatible_with_callout"></span>**\_контекст FWP \_ E \_ несовместим \_ с \_ выноской**
</dt> <dd> <dl> <dt>

0x8032002F
</dt> <dt>



Необработанный контекст или контекст поставщика несовместим с вызываемым.


</dt> </dl> </dd> <dt>

<span id="FWP_E_INCOMPATIBLE_AUTH_METHOD"></span><span id="fwp_e_incompatible_auth_method"></span>**FWP \_ E \_ несовместимый \_ метод проверки подлинности \_**
</dt> <dd> <dl> <dt>

0x80320030
</dt> <dt>



Метод проверки подлинности несовместим с типом политики.


</dt> </dl> </dd> <dt>

<span id="FWP_E_INCOMPATIBLE_DH_GROUP"></span><span id="fwp_e_incompatible_dh_group"></span>**FWP \_ E \_ несовместимая \_ Группа Диффи-Хелмана \_**
</dt> <dd> <dl> <dt>

0x80320031L
</dt> <dt>



Группа Diffie-Hellman несовместима с типом политики.


</dt> </dl> </dd> <dt>

<span id="FWP_E_EM_NOT_SUPPORTED"></span><span id="fwp_e_em_not_supported"></span>**FWP \_ E \_ EM \_ не \_ поддерживается**
</dt> <dd> <dl> <dt>

0x80320032
</dt> <dt>



Политика IKE не может содержать политику расширенного режима.


</dt> </dl> </dd> <dt>

<span id="FWP_E_NEVER_MATCH"></span><span id="fwp_e_never_match"></span>**FWP \_ е \_ никогда не \_ соответствует**
</dt> <dd> <dl> <dt>

0x80320033
</dt> <dt>



Шаблон перечисления или подписка никогда не будут сопоставляться ни с одним из объектов.


</dt> </dl> </dd> <dt>

<span id="FWP_E_PROVIDER_CONTEXT_MISMATCH"></span><span id="fwp_e_provider_context_mismatch"></span>**\_несоответствие \_ контекста поставщика FWP E \_ \_**
</dt> <dd> <dl> <dt>

0x80320034
</dt> <dt>



Неправильный тип контекста поставщика.


</dt> </dl> </dd> <dt>

<span id="FWP_E_INVALID_PARAMETER"></span><span id="fwp_e_invalid_parameter"></span>**FWP \_ E \_ Недопустимый \_ параметр**
</dt> <dd> <dl> <dt>

0x80320035
</dt> <dt>



Неправильный параметр".

Возможные причины этой ошибки:

-   [**FwpmIPsecTunnelAdd0**](/windows/desktop/api/Fwpmu/nf-fwpmu-fwpmipsectunneladd0) был вызван без задания флага **\_ туннеля фвпм \_ \_ в качестве \_ точки \_** и с условиями, отличными от локального или удаленного адреса.
-   Недопустимая строка в Юникоде или строка в Юникоде, которая содержит непечатаемые символы.


</dt> </dl> </dd> <dt>

<span id="FWP_E_TOO_MANY_SUBLAYERS"></span><span id="fwp_e_too_many_sublayers"></span>**FWP \_ , \_ слишком \_ много \_ подуровней**
</dt> <dd> <dl> <dt>

0x80320036
</dt> <dt>



Достигнуто максимальное число подслоев.

WFP поддерживает не более 2 6 подуровней.


</dt> </dl> </dd> <dt>

<span id="FWP_E_CALLOUT_NOTIFICATION_FAILED"></span><span id="fwp_e_callout_notification_failed"></span>**\_ \_ \_ не удалось отправить уведомление на выноску FWP \_**
</dt> <dd> <dl> <dt>

0x80320037
</dt> <dt>



Функция уведомления для вызова вернула ошибку.


</dt> </dl> </dd> <dt>

<span id="FWP_E_INVALID_AUTH_TRANSFORM"></span><span id="fwp_e_invalid_auth_transform"></span>**FWP \_ E \_ недопустимое \_ Преобразование проверки подлинности \_**
</dt> <dd> <dl> <dt>

0x80320038
</dt> <dt>



Недопустимое преобразование проверки подлинности IPsec.


</dt> </dl> </dd> <dt>

<span id="FWP_E_INVALID_CIPHER_TRANSFORM"></span><span id="fwp_e_invalid_cipher_transform"></span>**FWP \_ E \_ недопустимое \_ преобразование шифра \_**
</dt> <dd> <dl> <dt>

0x80320039
</dt> <dt>



Недопустимое преобразование шифра IPsec.


</dt> </dl> </dd> </dl>

## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Только для \[ классических приложений Windows Vista\]<br/>                                        |
| Минимальная версия сервера<br/> | \[Только для настольных приложений Windows Server 2008\]<br/>                                  |
| Header<br/>                   | <dl> <dt>Winerror. h</dt> </dl> |



 

 





