---
title: Коды ошибок клиента (Винбио \_ Err. h)
description: Коды ошибок, определенные в \_ файле заголовка винбио Err. h.
ms.assetid: fc1565d2-43f1-45cd-ab84-4e557cf78107
topic_type:
- apiref
api_name:
- WINBIO_E_UNSUPPORTED_FACTOR
- WINBIO_E_INVALID_UNIT
- WINBIO_E_UNKNOWN_ID
- WINBIO_E_CANCELED
- WINBIO_E_NO_MATCH
- WINBIO_E_CAPTURE_ABORTED
- WINBIO_E_ENROLLMENT_IN_PROGRESS
- WINBIO_E_BAD_CAPTURE
- WINBIO_E_INVALID_CONTROL_CODE
- WINBIO_E_DATA_COLLECTION_IN_PROGRESS
- WINBIO_E_UNSUPPORTED_DATA_FORMAT
- WINBIO_E_UNSUPPORTED_DATA_TYPE
- WINBIO_E_UNSUPPORTED_PURPOSE
- WINBIO_E_INVALID_DEVICE_STATE
- WINBIO_E_DEVICE_BUSY
- WINBIO_E_DATABASE_CANT_CREATE
- WINBIO_E_DATABASE_CANT_OPEN
- WINBIO_E_DATABASE_CANT_CLOSE
- WINBIO_E_DATABASE_CANT_ERASE
- WINBIO_E_DATABASE_CANT_FIND
- WINBIO_E_DATABASE_ALREADY_EXISTS
- WINBIO_E_DATABASE_FULL
- WINBIO_E_DATABASE_LOCKED
- WINBIO_E_DATABASE_CORRUPTED
- WINBIO_E_DATABASE_NO_SUCH_RECORD
- WINBIO_E_DUPLICATE_ENROLLMENT
- WINBIO_E_DATABASE_READ_ERROR
- WINBIO_E_DATABASE_WRITE_ERROR
- WINBIO_E_DATABASE_NO_RESULTS
- WINBIO_E_DATABASE_NO_MORE_RECORDS
- WINBIO_E_DATABASE_EOF
- WINBIO_E_DATABASE_BAD_INDEX_VECTOR
- WINBIO_E_INCORRECT_BSP
- WINBIO_E_INCORRECT_SENSOR_POOL
- WINBIO_E_NO_CAPTURE_DATA
- WINBIO_E_INVALID_SENSOR_MODE
- WINBIO_E_LOCK_VIOLATION
- WINBIO_E_DUPLICATE_TEMPLATE
- WINBIO_E_INVALID_OPERATION
- WINBIO_E_SESSION_BUSY
- WINBIO_E_CRED_PROV_DISABLED
- WINBIO_E_CRED_PROV_NO_CREDENTIAL
- WINBIO_E_DISABLED
- WINBIO_E_CONFIGURATION_FAILURE
- WINBIO_E_SENSOR_UNAVAILABLE
- WINBIO_E_SAS_ENABLED
- WINBIO_E_DEVICE_FAILURE
- WINBIO_E_FAST_USER_SWITCH_DISABLED
- WINBIO_E_NOT_ACTIVE_CONSOLE
- WINBIO_E_EVENT_MONITOR_ACTIVE
- WINBIO_E_INVALID_PROPERTY_TYPE
- WINBIO_E_INVALID_PROPERTY_ID
- WINBIO_E_UNSUPPORTED_PROPERTY
- WINBIO_E_ADAPTER_INTEGRITY_FAILURE
- WINBIO_I_MORE_DATA
api_location:
- Winbio_err.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: bcb8450b85eaa6c49b66a3a86789c126cc04b9a661a7e4c5074784f8cba6bf72
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119993844"
---
# <a name="client-error-codes"></a>Коды ошибок клиента

Следующие коды ошибок определены в \_ файле заголовка винбио Err. h.



| Константа/значение                                                                                                                                                                                                                                                                                         | Описание                                                                                                       |
|:-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:------------------------------------------------------------------------------------------------------------------|
| <span id="WINBIO_E_UNSUPPORTED_FACTOR"></span><span id="winbio_e_unsupported_factor"></span><dl> <dt>**Винбио \_ \_НЕподдерживаемый \_ фактор**</dt> <dt>0x80098001</dt> </dl>                              | Указанный биометрический фактор не поддерживается.<br/>                                                       |
| <span id="WINBIO_E_INVALID_UNIT"></span><span id="winbio_e_invalid_unit"></span><dl> <dt>**Винбио \_ E \_ Недопустимая \_ единица**</dt> <dt>0x80098002</dt> </dl>                                                | ИДЕНТИФИКАЦИОНный номер единицы не соответствует допустимому биометрической устройству.<br/>                                    |
| <span id="WINBIO_E_UNKNOWN_ID"></span><span id="winbio_e_unknown_id"></span><dl> <dt>**Винбио \_ \_Неизвестный \_ идентификатор E**</dt> <dt>0x80098003</dt> </dl>                                                      | Образец биометрической метрики не соответствует ни одному известному удостоверению.<br/>                                                |
| <span id="WINBIO_E_CANCELED"></span><span id="winbio_e_canceled"></span><dl> <dt>**Винбио \_ E \_ отменено**</dt> <dt>0x80098004</dt> </dl>                                                             | Биометрическая операция была отменена до ее завершения.<br/>                                         |
| <span id="WINBIO_E_NO_MATCH"></span><span id="winbio_e_no_match"></span><dl> <dt>**Винбио \_ E \_ без \_ соответствия**</dt> <dt>0x80098005</dt> </dl>                                                            | Образец биометрической метрики не соответствует указанному удостоверению или подразделу.<br/>                              |
| <span id="WINBIO_E_CAPTURE_ABORTED"></span><span id="winbio_e_capture_aborted"></span><dl> <dt>**Винбио \_ \_Запись 0x80098006 \_ прервана**</dt> <dt></dt> </dl>                                       | Не удалось записать образец биометрической метрики, так как операция записи была прервана.<br/>                    |
| <span id="WINBIO_E_ENROLLMENT_IN_PROGRESS"></span><span id="winbio_e_enrollment_in_progress"></span><dl> <dt>**Винбио \_ \_Регистрация \_ в \_ ходе выполнения**</dt> <dt>0x80098007</dt> </dl>                 | Не удалось запустить транзакцию регистрации, так как уже выполняется другая регистрация.<br/>      |
| <span id="WINBIO_E_BAD_CAPTURE"></span><span id="winbio_e_bad_capture"></span><dl> <dt>**Винбио \_ \_Неправильная \_ запись**</dt> <dt>0x80098008</dt> </dl>                                                   | Захваченный пример не может использоваться для дальнейших биометрических операций.<br/>                                   |
| <span id="WINBIO_E_INVALID_CONTROL_CODE"></span><span id="winbio_e_invalid_control_code"></span><dl> <dt>**Винбио \_ \_Недопустимый \_ \_ код элемента управления E**</dt> <dt>0x80098009</dt> </dl>                       | Биометрический модуль не поддерживает указанный код управления единицей.<br/>                                   |
| <span id="WINBIO_E_DATA_COLLECTION_IN_PROGRESS"></span><span id="winbio_e_data_collection_in_progress"></span><dl> <dt>**Винбио \_ \_ \_ \_ \_ Идет сбор данных**</dt> <dt>0x8009800B</dt> </dl> | Операция сбора данных, ожидающих обработки, уже выполняется.<br/>                                            |
| <span id="WINBIO_E_UNSUPPORTED_DATA_FORMAT"></span><span id="winbio_e_unsupported_data_format"></span><dl> <dt>**Винбио \_ \_НЕподдерживаемый \_ \_ Формат данных**</dt> <dt>0x8009800C</dt> </dl>              | Драйвер биометрического датчика не поддерживает запрошенный формат данных.<br/>                                |
| <span id="WINBIO_E_UNSUPPORTED_DATA_TYPE"></span><span id="winbio_e_unsupported_data_type"></span><dl> <dt>**Винбио \_ \_НЕподдерживаемый \_ \_ тип данных**</dt> <dt>0x8009800D</dt> </dl>                    | Драйвер биометрического датчика не поддерживает запрошенный тип данных.<br/>                                  |
| <span id="WINBIO_E_UNSUPPORTED_PURPOSE"></span><span id="winbio_e_unsupported_purpose"></span><dl> <dt>**Винбио \_ \_НЕподдерживаемая \_ Цель**</dt> <dt>0x8009800E</dt> </dl>                           | Драйвер биометрического датчика не поддерживает запрошенную цель данных.<br/>                               |
| <span id="WINBIO_E_INVALID_DEVICE_STATE"></span><span id="winbio_e_invalid_device_state"></span><dl> <dt>**Винбио \_ E \_ недопустимое \_ \_ состояние устройства**</dt> <dt>0x8009800F</dt> </dl>                       | Биометрическая единица находится в неправильном состоянии для выполнения указанной операции.<br/>                      |
| <span id="WINBIO_E_DEVICE_BUSY"></span><span id="winbio_e_device_busy"></span><dl> <dt>**Винбио \_ Электронное \_ устройство \_ занято**</dt> <dt>0x80098010</dt> </dl>                                                   | Не удалось выполнить операцию, так как устройство датчика занято.<br/>                               |
| <span id="WINBIO_E_DATABASE_CANT_CREATE"></span><span id="winbio_e_database_cant_create"></span><dl> <dt>**Винбио \_ \_База данных E не \_ удается \_ создать**</dt> <dt>0x80098011</dt> </dl>                       | Адаптеру хранилища не удалось создать новую базу данных.<br/>                                             |
| <span id="WINBIO_E_DATABASE_CANT_OPEN"></span><span id="winbio_e_database_cant_open"></span><dl> <dt>**Винбио \_ Электронная \_ база данных не \_ удается \_ Открыть**</dt> <dt>0x80098012</dt> </dl>                             | Адаптеру хранилища не удалось открыть существующую базу данных.<br/>                                         |
| <span id="WINBIO_E_DATABASE_CANT_CLOSE"></span><span id="winbio_e_database_cant_close"></span><dl> <dt>**Винбио \_ \_База данных E не \_ удается \_ Закрыть**</dt> <dt>0x80098013</dt> </dl>                          | Адаптеру хранилища не удалось закрыть базу данных.<br/>                                                  |
| <span id="WINBIO_E_DATABASE_CANT_ERASE"></span><span id="winbio_e_database_cant_erase"></span><dl> <dt>**Винбио \_ База данных "E" не \_ \_ удается \_ стереть**</dt> <dt>0x80098014</dt> </dl>                          | Адаптеру хранилища не удалось стереть базу данных.<br/>                                                  |
| <span id="WINBIO_E_DATABASE_CANT_FIND"></span><span id="winbio_e_database_cant_find"></span><dl> <dt>**Винбио \_ Электронная \_ база данных не \_ удается \_ найти**</dt> <dt>0x80098015</dt> </dl>                             | Адаптеру хранилища не удалось найти базу данных.<br/>                                                   |
| <span id="WINBIO_E_DATABASE_ALREADY_EXISTS"></span><span id="winbio_e_database_already_exists"></span><dl> <dt>**Винбио \_ \_База данных E \_ уже \_ существует**</dt> <dt>0x80098016</dt> </dl>              | Адаптеру хранилища не удалось создать базу данных, поскольку указанная база данных уже существует.<br/>   |
| <span id="WINBIO_E_DATABASE_FULL"></span><span id="winbio_e_database_full"></span><dl> <dt>**Винбио \_ Электронная \_ база данных \_ Full**</dt> <dt>0x80098018</dt> </dl>                                             | Адаптеру хранилища не удалось добавить запись в базу данных, так как база данных заполнена.<br/>         |
| <span id="WINBIO_E_DATABASE_LOCKED"></span><span id="winbio_e_database_locked"></span><dl> <dt>**Винбио \_ Электронная \_ база данных \_ заблокирована**</dt> <dt>0x80098019</dt> </dl>                                       | База данных заблокирована, и ее содержимое недоступно.<br/>                                              |
| <span id="WINBIO_E_DATABASE_CORRUPTED"></span><span id="winbio_e_database_corrupted"></span><dl> <dt>**Винбио \_ \_База данных \_ 0x8009801A повреждена**</dt> <dt></dt> </dl>                              | Содержимое базы данных стало поврежденным и недоступным.<br/>                               |
| <span id="WINBIO_E_DATABASE_NO_SUCH_RECORD"></span><span id="winbio_e_database_no_such_record"></span><dl> <dt>**Винбио \_ У \_ базы данных E \_ нет \_ такой \_ записи**</dt> <dt>0x8009801B</dt> </dl>             | Не было удалено ни одной записи, так как указанный идентификатор и вспомогательный фактор отсутствуют в базе данных.<br/> |
| <span id="WINBIO_E_DUPLICATE_ENROLLMENT"></span><span id="winbio_e_duplicate_enrollment"></span><dl> <dt>**Винбио \_ 0x8009801C \_ \_ регистрации дубликатов**</dt> <dt></dt> </dl>                        | Указанный идентификатор и его подфакторы уже зарегистрированы в базе данных.<br/>                            |
| <span id="WINBIO_E_DATABASE_READ_ERROR"></span><span id="winbio_e_database_read_error"></span><dl> <dt>**Винбио \_ E \_ \_ \_ Ошибка чтения базы данных**</dt> <dt>0x8009801D</dt> </dl>                          | Произошла ошибка при попытке чтения из базы данных.<br/>                                              |
| <span id="WINBIO_E_DATABASE_WRITE_ERROR"></span><span id="winbio_e_database_write_error"></span><dl> <dt>**Винбио \_ Электронная \_ \_ \_ Ошибка записи в базу данных**</dt> <dt>0x8009801E</dt> </dl>                       | При попытке записи в базу данных возникла ошибка.<br/>                                               |
| <span id="WINBIO_E_DATABASE_NO_RESULTS"></span><span id="winbio_e_database_no_results"></span><dl> <dt>**Винбио \_ \_База данных \_ без \_ результатов**</dt> <dt>0x8009801F</dt> </dl>                          | Нет записей в базе данных, соответствующих запросу.<br/>                                                          |
| <span id="WINBIO_E_DATABASE_NO_MORE_RECORDS"></span><span id="winbio_e_database_no_more_records"></span><dl> <dt>**Винбио \_ \_База данных E больше \_ не содержит \_ \_ записей**</dt> <dt>0x80098020</dt> </dl>          | Получены все записи из последнего запроса к базе данных.<br/>                                   |
| <span id="WINBIO_E_DATABASE_EOF"></span><span id="winbio_e_database_eof"></span><dl> <dt>**Винбио \_ Электронная \_ база \_ данных**</dt> <dt>0x80098021</dt> EOF </dl>                                                | Операция базы данных неожиданно обнаружила конец файла.<br/>                                     |
| <span id="WINBIO_E_DATABASE_BAD_INDEX_VECTOR"></span><span id="winbio_e_database_bad_index_vector"></span><dl> <dt>**Винбио \_ \_База данных с \_ неправильным \_ \_ вектором индекса**</dt> <dt>0x80098022</dt> </dl>       | Не удалось выполнить операцию базы данных из-за неправильно сформированного вектора индекса.<br/>                                           |
| <span id="WINBIO_E_INCORRECT_BSP"></span><span id="winbio_e_incorrect_bsp"></span><dl> <dt>**Винбио \_ \_Неверный \_**</dt> <dt>0x80098024</dt> BSP </dl>                                             | Биометрическая единица не принадлежит указанному поставщику услуг.<br/>                                  |
| <span id="WINBIO_E_INCORRECT_SENSOR_POOL"></span><span id="winbio_e_incorrect_sensor_pool"></span><dl> <dt>**Винбио \_ \_Неверный \_ 0x80098025 \_ пула датчиков**</dt> <dt></dt> </dl>                    | Биометрический модуль не принадлежит указанному пулу датчика.<br/>                                       |
| <span id="WINBIO_E_NO_CAPTURE_DATA"></span><span id="winbio_e_no_capture_data"></span><dl> <dt>**Винбио \_ E \_ без \_ записи \_**</dt> <dt>0x80098026</dt> данных </dl>                                      | Буфер записи адаптера датчика пуст.<br/>                                                            |
| <span id="WINBIO_E_INVALID_SENSOR_MODE"></span><span id="winbio_e_invalid_sensor_mode"></span><dl> <dt>**Винбио \_ \_Недопустимый \_ \_ режим датчика**</dt> <dt>0x80098027</dt> </dl>                          | Адаптер датчика не поддерживает режим датчика, указанный в конфигурации.<br/>                    |
| <span id="WINBIO_E_LOCK_VIOLATION"></span><span id="winbio_e_lock_violation"></span><dl> <dt>**Винбио \_ 0x8009802A \_ \_ нарушение блокировки**</dt> <dt></dt> </dl>                                          | Не удается выполнить запрошенную операцию из-за конфликта блокировки.<br/>                                 |
| <span id="WINBIO_E_DUPLICATE_TEMPLATE"></span><span id="winbio_e_duplicate_template"></span><dl> <dt>**Винбио \_ \_Дублировать \_ шаблон**</dt> <dt>0x8009802B</dt> </dl>                              | Данные в биометрических шаблоне соответствуют другому шаблону, уже находящегося в базе данных.<br/>             |
| <span id="WINBIO_E_INVALID_OPERATION"></span><span id="winbio_e_invalid_operation"></span><dl> <dt>**Винбио \_ E \_ Недопустимая \_ Операция**</dt> <dt>0x8009802C</dt> </dl>                                 | Запрошенная операция недопустима для текущего состояния сеанса или биометрического модуля.<br/>       |
| <span id="WINBIO_E_SESSION_BUSY"></span><span id="winbio_e_session_busy"></span><dl> <dt>**Винбио \_ \_Сеанс E \_ занят**</dt> <dt>0x8009802D</dt> </dl>                                                | Сеанс не может начать новую операцию, так как уже выполняется другая операция.<br/>             |
| <span id="WINBIO_E_CRED_PROV_DISABLED"></span><span id="winbio_e_cred_prov_disabled"></span><dl> <dt>**Винбио \_ E \_ cred \_ Prov \_ disabled**</dt> <dt>0x80098030</dt> </dl>                             | В параметрах системной политики отключен поставщик биометрических учетных данных.<br/>                                |
| <span id="WINBIO_E_CRED_PROV_NO_CREDENTIAL"></span><span id="winbio_e_cred_prov_no_credential"></span><dl> <dt>**Винбио \_ E \_ cred \_ Prov \_ без \_ учетных данных**</dt> <dt>0x80098031</dt> </dl>             | Запрошенные учетные данные не найдены.<br/>                                                                |
| <span id="WINBIO_E_DISABLED"></span><span id="winbio_e_disabled"></span><dl> <dt>**Винбио \_ E \_ disabled**</dt> <dt>0x80098032</dt> </dl>                                                             | В параметрах системной политики отключена биометрическая служба.<br/>                                            |
| <span id="WINBIO_E_CONFIGURATION_FAILURE"></span><span id="winbio_e_configuration_failure"></span><dl> <dt>**Винбио \_ \_ \_ Ошибка конфигурации**</dt> <dt>0x80098033</dt> </dl>                     | Не удалось настроить биометрический модуль.<br/>                                                            |
| <span id="WINBIO_E_SENSOR_UNAVAILABLE"></span><span id="winbio_e_sensor_unavailable"></span><dl> <dt>**Винбио \_ \_Датчик E \_ недоступен**</dt> <dt>0x80098034</dt> </dl>                              | Не удается создать частный пул, так как один или несколько биометрических единиц недоступны.<br/>                |
| <span id="WINBIO_E_SAS_ENABLED"></span><span id="winbio_e_sas_enabled"></span><dl> <dt>**Винбио \_ 0x80098035 \_ с \_ поддержкой SAS**</dt> <dt></dt> </dl>                                                   | Для входа требуется последовательность безопасного внимания (CTRL-ALT-DELETE).<br/>                                   |
| <span id="WINBIO_E_DEVICE_FAILURE"></span><span id="winbio_e_device_failure"></span><dl> <dt>**Винбио \_ 0x80098036 \_ \_ ошибок устройства E**</dt> <dt></dt> </dl>                                          | Сбой биометрического датчика.<br/>                                                                         |
| <span id="WINBIO_E_FAST_USER_SWITCH_DISABLED"></span><span id="winbio_e_fast_user_switch_disabled"></span><dl> <dt>**Винбио \_ E \_ FAST \_ пользовательский \_ коммутатор \_ отключен**</dt> <dt>0x80098037</dt> </dl>       | >быстрое переключение пользователей отключено.<br/>                                                                   |
| <span id="WINBIO_E_NOT_ACTIVE_CONSOLE"></span><span id="winbio_e_not_active_console"></span><dl> <dt>**Винбио \_ \_Неактивный \_ \_ консольный**</dt> <dt>0x80098038</dt> </dl>                             | Не удается открыть пул датчиков системы из сеансов клиента сервера терминалов.<br/>                          |
| <span id="WINBIO_E_EVENT_MONITOR_ACTIVE"></span><span id="winbio_e_event_monitor_active"></span><dl> <dt>**Винбио \_ Монитор событий "E" \_ \_ \_ Active**</dt> <dt>0x80098039</dt> </dl>                      | С указанным сеансом уже связан активный монитор событий.<br/>                        |
| <span id="WINBIO_E_INVALID_PROPERTY_TYPE"></span><span id="winbio_e_invalid_property_type"></span><dl> <dt>**Винбио \_ \_Недопустимый \_ \_ тип свойства**</dt> <dt>0x8009803A</dt> </dl>                    | Указанное значение не является допустимым типом свойства.<br/>                                                      |
| <span id="WINBIO_E_INVALID_PROPERTY_ID"></span><span id="winbio_e_invalid_property_id"></span><dl> <dt>**Винбио \_ E \_ Недопустимый \_ \_ идентификатор свойства**</dt> <dt>0x8009803B</dt> </dl>                          | Указанное значение не является допустимым ИДЕНТИФИКАТОРом свойства.<br/>                                                        |
| <span id="WINBIO_E_UNSUPPORTED_PROPERTY"></span><span id="winbio_e_unsupported_property"></span><dl> <dt>**Винбио \_ E \_ НЕподдерживаемое \_ свойство**</dt> <dt>0x8009803C</dt> </dl>                        | Биометрический модуль не поддерживает указанное свойство.<br/>                                            |
| <span id="WINBIO_E_ADAPTER_INTEGRITY_FAILURE"></span><span id="winbio_e_adapter_integrity_failure"></span><dl> <dt>**Винбио \_ \_ \_ \_ Ошибка целостности адаптера E**</dt> <dt>0x8009803D</dt> </dl>        | Адаптер не прошел проверку целостности.<br/>                                                          |
| <span id="WINBIO_I_MORE_DATA"></span><span id="winbio_i_more_data"></span><dl> <dt>**Винбио \_ \_Дополнительные \_ данные**</dt> <dt>0x00090001</dt> </dl>                                                         | Для текущего шаблона регистрации требуется еще один пример.<br/>                                          |



## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------------------------|------------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | только Windows 7 \[ настольных приложений\]<br/>                                               |
| Минимальная версия сервера<br/> | Windows \[Только для настольных приложений сервера 2008 R2\]<br/>                                  |
| Заголовок<br/>                   | <dl> <dt>Винбио \_ Err. h</dt> </dl> |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[Константы клиентского приложения](client-application-constants.md)
</dt> </dl>

 

 





