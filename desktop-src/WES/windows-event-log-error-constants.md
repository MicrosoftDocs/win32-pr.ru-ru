---
title: Windows Константы ошибок журнала событий (WinError. h)
description: ниже приведены коды ошибок, которые Windows определяет журнал событий.
ms.assetid: 889ea4ae-dede-45d5-9293-cec85d81f010
topic_type:
- apiref
api_name:
- ERROR_EVT_INVALID_CHANNEL_PATH
- ERROR_EVT_INVALID_QUERY
- ERROR_EVT_PUBLISHER_METADATA_NOT_FOUND
- ERROR_EVT_EVENT_TEMPLATE_NOT_FOUND
- ERROR_EVT_INVALID_PUBLISHER_NAME
- ERROR_EVT_INVALID_EVENT_DATA
- ERROR_EVT_CHANNEL_NOT_FOUND
- ERROR_EVT_MALFORMED_XML_TEXT
- ERROR_EVT_SUBSCRIPTION_TO_DIRECT_CHANNEL
- ERROR_EVT_CONFIGURATION_ERROR
- ERROR_EVT_QUERY_RESULT_STALE
- ERROR_EVT_QUERY_RESULT_INVALID_POSITION
- ERROR_EVT_NON_VALIDATING_MSXML
- ERROR_EVT_FILTER_ALREADYSCOPED
- ERROR_EVT_FILTER_NOTELTSET
- ERROR_EVT_FILTER_INVARG
- ERROR_EVT_FILTER_INVTEST
- ERROR_EVT_FILTER_INVTYPE
- ERROR_EVT_FILTER_PARSEERR
- ERROR_EVT_FILTER_UNSUPPORTEDOP
- ERROR_EVT_FILTER_UNEXPECTEDTOKEN
- ERROR_EVT_INVALID_OPERATION_OVER_ENABLED_DIRECT_CHANNEL
- ERROR_EVT_INVALID_CHANNEL_PROPERTY_VALUE
- ERROR_EVT_INVALID_PUBLISHER_PROPERTY_VALUE
- ERROR_EVT_CHANNEL_CANNOT_ACTIVATE
- ERROR_EVT_FILTER_TOO_COMPLEX
- ERROR_EVT_MESSAGE_NOT_FOUND
- ERROR_EVT_MESSAGE_ID_NOT_FOUND
- ERROR_EVT_UNRESOLVED_VALUE_INSERT
- ERROR_EVT_UNRESOLVED_PARAMETER_INSERT
- ERROR_EVT_MAX_INSERTS_REACHED
- ERROR_EVT_EVENT_DEFINITION_NOT_FOUND
- ERROR_EVT_MESSAGE_LOCALE_NOT_FOUND
- ERROR_EVT_VERSION_TOO_OLD
- ERROR_EVT_VERSION_TOO_NEW
- ERROR_EVT_CANNOT_OPEN_CHANNEL_OF_QUERY
- ERROR_EVT_PUBLISHER_DISABLED
- ERROR_EVT_FILTER_OUT_OF_RANGE
api_location:
- WinError.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e0f6f0bd3e2805c02dad78c064b56a443bfbb596cf42f25e9b52ac7ba584f123
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "120031944"
---
# <a name="windows-event-log-error-constants"></a>Windows Константы ошибок журнала событий

ниже приведены коды ошибок, которые Windows определяет журнал событий.

<dl> <dt>

<span id="ERROR_EVT_INVALID_CHANNEL_PATH"></span><span id="error_evt_invalid_channel_path"></span>**Ошибка \_ evt \_ недопустимого \_ \_ пути канала**
</dt> <dd> <dl> <dt>

15 000
</dt> <dt>



Указан недопустимый путь к каналу.


</dt> </dl> </dd> <dt>

<span id="ERROR_EVT_INVALID_QUERY"></span><span id="error_evt_invalid_query"></span>**Ошибка \_ \_ недопустимого \_ запроса evt**
</dt> <dd> <dl> <dt>

15001
</dt> <dt>



Указан недопустимый запрос.


</dt> </dl> </dd> <dt>

<span id="ERROR_EVT_PUBLISHER_METADATA_NOT_FOUND"></span><span id="error_evt_publisher_metadata_not_found"></span>**Ошибка \_ \_ \_ \_ не найдены метаданные издателя \_ evt**
</dt> <dd> <dl> <dt>

15002
</dt> <dt>



Не удается найти метаданные поставщика в ресурсе.


</dt> </dl> </dd> <dt>

<span id="ERROR_EVT_EVENT_TEMPLATE_NOT_FOUND"></span><span id="error_evt_event_template_not_found"></span>**\_ \_ шаблон событий Error \_ evt \_ не \_ найден**
</dt> <dd> <dl> <dt>

15003
</dt> <dt>



Не удается найти шаблон для определения события в ресурсе.


</dt> </dl> </dd> <dt>

<span id="ERROR_EVT_INVALID_PUBLISHER_NAME"></span><span id="error_evt_invalid_publisher_name"></span>**Ошибка \_ evt \_ недопустимое \_ \_ имя издателя**
</dt> <dd> <dl> <dt>

15004
</dt> <dt>



Указано недопустимое имя поставщика.


</dt> </dl> </dd> <dt>

<span id="ERROR_EVT_INVALID_EVENT_DATA"></span><span id="error_evt_invalid_event_data"></span>**Ошибка \_ evt " \_ недопустимые \_ \_ данные события"**
</dt> <dd> <dl> <dt>

15005
</dt> <dt>



Данные события, вызванные поставщиком, несовместимы с определением шаблона события в манифесте поставщика.


</dt> </dl> </dd> <dt>

<span id="ERROR_EVT_CHANNEL_NOT_FOUND"></span><span id="error_evt_channel_not_found"></span>**\_канал ошибки \_ evt \_ не \_ найден**
</dt> <dd> <dl> <dt>

15007
</dt> <dt>



Не удается найти указанный канал. Проверьте конфигурацию канала.


</dt> </dl> </dd> <dt>

<span id="ERROR_EVT_MALFORMED_XML_TEXT"></span><span id="error_evt_malformed_xml_text"></span>**Ошибка \_ evt \_ неправильно сформированный \_ XML- \_ текст**
</dt> <dd> <dl> <dt>

15008
</dt> <dt>



Указанный XML-текст имеет неправильный формат. Для получения дополнительных сведений вызовите функцию [**евтжетекстендедстатус**](/windows/desktop/api/WinEvt/nf-winevt-evtgetextendedstatus) .


</dt> </dl> </dd> <dt>

<span id="ERROR_EVT_SUBSCRIPTION_TO_DIRECT_CHANNEL"></span><span id="error_evt_subscription_to_direct_channel"></span>**Ошибка \_ при \_ подписке evt \_ на \_ прямой \_ канал**
</dt> <dd> <dl> <dt>

15009
</dt> <dt>



Нельзя подписываться на аналитический или отладочный канал; события для аналитического или отладочного канала попадают непосредственно в файл журнала и не могут быть подписаны на.


</dt> </dl> </dd> <dt>

<span id="ERROR_EVT_CONFIGURATION_ERROR"></span><span id="error_evt_configuration_error"></span>**Ошибка \_ \_ конфигурации evt \_**
</dt> <dd> <dl> <dt>

15010
</dt> <dt>



Произошла ошибка конфигурации.


</dt> </dl> </dd> <dt>

<span id="ERROR_EVT_QUERY_RESULT_STALE"></span><span id="error_evt_query_result_stale"></span>**\_ \_ \_ неактуальный результат \_ запроса "ошибка evt"**
</dt> <dd> <dl> <dt>

15011
</dt> <dt>



Недопустимый результат запроса. Это может быть вызвано очисткой или перебором журнала после создания результата запроса. Освободите объект результата запроса и повторите запрос.


</dt> </dl> </dd> <dt>

<span id="ERROR_EVT_QUERY_RESULT_INVALID_POSITION"></span><span id="error_evt_query_result_invalid_position"></span>**ошибочное \_ \_ \_ значение результата \_ запроса \_ "ошибка evt"**
</dt> <dd> <dl> <dt>

15012
</dt> <dt>



Курсор для результата запроса не указывает на допустимую позицию.


</dt> </dl> </dd> <dt>

<span id="ERROR_EVT_NON_VALIDATING_MSXML"></span><span id="error_evt_non_validating_msxml"></span>**Ошибка \_ EVT, \_ не \_ проверяя \_ MSXML**
</dt> <dd> <dl> <dt>

15013
</dt> <dt>



зарегистрированный синтаксический анализатор MSXML не поддерживает проверку.


</dt> </dl> </dd> <dt>

<span id="ERROR_EVT_FILTER_ALREADYSCOPED"></span><span id="error_evt_filter_alreadyscoped"></span>**Ошибка \_ evt \_ Filter \_ алреадископед**
</dt> <dd> <dl> <dt>

15014
</dt> <dt>



За выражением может следовать изменение операции Scope только в том случае, если результатом вычисления выражения является набор узлов и он еще не является частью какого-либо другого изменения операции с областью действия.


</dt> </dl> </dd> <dt>

<span id="ERROR_EVT_FILTER_NOTELTSET"></span><span id="error_evt_filter_noteltset"></span>**Ошибка \_ evt \_ Filter \_ нотелтсет**
</dt> <dd> <dl> <dt>

15015
</dt> <dt>



Невозможно выполнить шаг с термином, который не представляет набор элементов.


</dt> </dl> </dd> <dt>

<span id="ERROR_EVT_FILTER_INVARG"></span><span id="error_evt_filter_invarg"></span>**Ошибка \_ evt \_ Filter \_ инварг**
</dt> <dd> <dl> <dt>

15016
</dt> <dt>



Аргументы в левой части бинарного оператора должны быть либо атрибутами, либо узлами, либо переменными, а аргументы в правой части должны быть константами.


</dt> </dl> </dd> <dt>

<span id="ERROR_EVT_FILTER_INVTEST"></span><span id="error_evt_filter_invtest"></span>**Ошибка \_ evt \_ Filter \_ инвтест**
</dt> <dd> <dl> <dt>

15017
</dt> <dt>



Операция шага должна затрагивать либо проверку узла, либо, в случае предиката, выражение алгебраические, для которого необходимо проверить каждый узел в наборе узлов, определяемый предыдущим набором узлов.


</dt> </dl> </dd> <dt>

<span id="ERROR_EVT_FILTER_INVTYPE"></span><span id="error_evt_filter_invtype"></span>**Ошибка \_ evt \_ Filter \_ инвтипе**
</dt> <dd> <dl> <dt>

15018
</dt> <dt>



Этот тип данных не поддерживается.


</dt> </dl> </dd> <dt>

<span id="ERROR_EVT_FILTER_PARSEERR"></span><span id="error_evt_filter_parseerr"></span>**Ошибка \_ evt \_ Filter \_ парсирр**
</dt> <dd> <dl> <dt>

15019
</dt> <dt>



В указанной позиции произошла синтаксическая ошибка.


</dt> </dl> </dd> <dt>

<span id="ERROR_EVT_FILTER_UNSUPPORTEDOP"></span><span id="error_evt_filter_unsupportedop"></span>**Ошибка \_ evt \_ Filter \_ унсуппортедоп**
</dt> <dd> <dl> <dt>

15020
</dt> <dt>



Этот оператор не поддерживается этой реализацией фильтра.


</dt> </dl> </dd> <dt>

<span id="ERROR_EVT_FILTER_UNEXPECTEDTOKEN"></span><span id="error_evt_filter_unexpectedtoken"></span>**Ошибка \_ evt \_ Filter \_ унекспектедтокен**
</dt> <dd> <dl> <dt>

15021
</dt> <dt>



Обнаружена непредвиденная лексема.


</dt> </dl> </dd> <dt>

<span id="ERROR_EVT_INVALID_OPERATION_OVER_ENABLED_DIRECT_CHANNEL"></span><span id="error_evt_invalid_operation_over_enabled_direct_channel"></span>**Ошибка \_ evt \_ недопустимой \_ операции \_ через \_ включенный \_ прямой \_ канал**
</dt> <dd> <dl> <dt>

15022
</dt> <dt>



Запрошенную операцию нельзя выполнить через включенный аналитический или отладочный канал. Перед выполнением запрошенной операции необходимо отключить канал.


</dt> </dl> </dd> <dt>

<span id="ERROR_EVT_INVALID_CHANNEL_PROPERTY_VALUE"></span><span id="error_evt_invalid_channel_property_value"></span>**Ошибка \_ evt \_ недопустимое \_ \_ значение свойства канала \_**
</dt> <dd> <dl> <dt>

15023
</dt> <dt>



Свойство канала содержит недопустимое значение. Тип значения может быть недопустимым, значение может находиться вне допустимого диапазона, либо значение не может быть обновлено или не поддерживается для этого типа канала.


</dt> </dl> </dd> <dt>

<span id="ERROR_EVT_INVALID_PUBLISHER_PROPERTY_VALUE"></span><span id="error_evt_invalid_publisher_property_value"></span>**Ошибка \_ evt \_ недопустимое \_ \_ значение свойства издателя \_**
</dt> <dd> <dl> <dt>

15024
</dt> <dt>



Свойство Provider содержит недопустимое значение. Тип значения может быть недопустимым, значение может находиться вне допустимого диапазона, либо значение не может быть обновлено или не поддерживается для данного типа поставщика.


</dt> </dl> </dd> <dt>

<span id="ERROR_EVT_CHANNEL_CANNOT_ACTIVATE"></span><span id="error_evt_channel_cannot_activate"></span>**Ошибка \_ при \_ \_ активации канала \_ evt**
</dt> <dd> <dl> <dt>

15025
</dt> <dt>



Не удалось активировать канал.


</dt> </dl> </dd> <dt>

<span id="ERROR_EVT_FILTER_TOO_COMPLEX"></span><span id="error_evt_filter_too_complex"></span>**\_ \_ \_ слишком \_ сложный фильтр evt ошибки**
</dt> <dd> <dl> <dt>

15026
</dt> <dt>



Выражение XPath превысило поддерживаемую сложность. Упростите выражение или разделите его на два или более простых выражения.


</dt> </dl> </dd> <dt>

<span id="ERROR_EVT_MESSAGE_NOT_FOUND"></span><span id="error_evt_message_not_found"></span>**сообщение с ошибкой \_ evt \_ \_ не \_ Найдено**
</dt> <dd> <dl> <dt>

15027
</dt> <dt>



Ресурс сообщения существует, но сообщение не найдено в строке или таблице сообщений.


</dt> </dl> </dd> <dt>

<span id="ERROR_EVT_MESSAGE_ID_NOT_FOUND"></span><span id="error_evt_message_id_not_found"></span>**\_ \_ идентификатор сообщения ошибки \_ evt \_ не \_ найден**
</dt> <dd> <dl> <dt>

15028
</dt> <dt>



Не удается найти идентификатор сообщения.


</dt> </dl> </dd> <dt>

<span id="ERROR_EVT_UNRESOLVED_VALUE_INSERT"></span><span id="error_evt_unresolved_value_insert"></span>**Ошибка \_ EVT, \_ неразрешенное \_ значение \_ INSERT**
</dt> <dd> <dl> <dt>

15029
</dt> <dt>



Не удается найти строку подстановки для индекса вставки.


</dt> </dl> </dd> <dt>

<span id="ERROR_EVT_UNRESOLVED_PARAMETER_INSERT"></span><span id="error_evt_unresolved_parameter_insert"></span>**Ошибка \_ EVT, \_ неразрешенная \_ \_ Вставка параметра**
</dt> <dd> <dl> <dt>

15030
</dt> <dt>



Не удается найти строку описания для ссылки на параметр (%1).


</dt> </dl> </dd> <dt>

<span id="ERROR_EVT_MAX_INSERTS_REACHED"></span><span id="error_evt_max_inserts_reached"></span>**\_ \_ \_ достигнуто максимальное число вставок \_ ошибок evt**
</dt> <dd> <dl> <dt>

15031
</dt> <dt>



Достигнуто максимальное число замен.


</dt> </dl> </dd> <dt>

<span id="ERROR_EVT_EVENT_DEFINITION_NOT_FOUND"></span><span id="error_evt_event_definition_not_found"></span>**\_Определение события "ошибка evt" \_ \_ \_ не \_ Найдено**
</dt> <dd> <dl> <dt>

15032
</dt> <dt>



Не удается найти определение события для идентификатора события.


</dt> </dl> </dd> <dt>

<span id="ERROR_EVT_MESSAGE_LOCALE_NOT_FOUND"></span><span id="error_evt_message_locale_not_found"></span>**\_ \_ \_ \_ не удалось найти языковой стандарт сообщений \_ с ошибкой evt**
</dt> <dd> <dl> <dt>

15033
</dt> <dt>



Ресурс, зависящий от локали, для требуемого сообщения отсутствует.


</dt> </dl> </dd> <dt>

<span id="ERROR_EVT_VERSION_TOO_OLD"></span><span id="error_evt_version_too_old"></span>**\_ \_ \_ слишком \_ старая версия evt**
</dt> <dd> <dl> <dt>

15034
</dt> <dt>



Ресурс слишком старый, чтобы быть совместимым.


</dt> </dl> </dd> <dt>

<span id="ERROR_EVT_VERSION_TOO_NEW"></span><span id="error_evt_version_too_new"></span>**\_ \_ \_ слишком \_ Новая версия ошибки evt**
</dt> <dd> <dl> <dt>

15035
</dt> <dt>



Ресурс слишком новый для совместимости.


</dt> </dl> </dd> <dt>

<span id="ERROR_EVT_CANNOT_OPEN_CHANNEL_OF_QUERY"></span><span id="error_evt_cannot_open_channel_of_query"></span>**Ошибка \_ evt \_ не \_ удается \_ открыть \_ канал \_ запроса**
</dt> <dd> <dl> <dt>

15036
</dt> <dt>



Невозможно открыть канал по указанному индексу запроса.


</dt> </dl> </dd> <dt>

<span id="ERROR_EVT_PUBLISHER_DISABLED"></span><span id="error_evt_publisher_disabled"></span>**Ошибка \_ " \_ Издатель evt \_ отключен"**
</dt> <dd> <dl> <dt>

15037
</dt> <dt>



Поставщик отключен, и его ресурсы недоступны. Это может произойти при удалении или обновлении поставщика.


</dt> </dl> </dd> <dt>

<span id="ERROR_EVT_FILTER_OUT_OF_RANGE"></span><span id="error_evt_filter_out_of_range"></span>**ОШИБОЧный \_ \_ Фильтр evt \_ за пределами \_ \_ диапазона**
</dt> <dd> <dl> <dt>

15038
</dt> <dt>



Попытка создать числовой тип, который находится за пределами допустимого диапазона.


</dt> </dl> </dd> </dl>

## <a name="requirements"></a>Requirements (Требования)



| Требование | Значение |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Windows \[Только классические приложения Vista\]<br/>                                        |
| Минимальная версия сервера<br/> | Windows Только для \[ настольных приложений сервера 2008\]<br/>                                  |
| Заголовок<br/>                   | <dl> <dt>WinError. h</dt> </dl> |



 

 





