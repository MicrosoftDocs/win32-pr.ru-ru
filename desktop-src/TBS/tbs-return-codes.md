---
title: Коды возврата TBS (TBS. h)
description: TBS использует следующие коды для указания результата вызова функции.
ms.assetid: a3888263-aa00-4b31-b51d-c6d448c1edb7
topic_type:
- apiref
api_name:
- TBS_SUCCESS
- TBS_E_INTERNAL_ERROR
- TBS_E_BAD_PARAMETER
- TBS_E_INVALID_OUTPUT_POINTER
- TBS_E_INVALID_CONTEXT
- TBS_E_INSUFFICIENT_BUFFER
- TBS_E_IOERROR
- TBS_E_INVALID_CONTEXT_PARAM
- TBS_E_SERVICE_NOT_RUNNING
- TBS_E_TOO_MANY_TBS_CONTEXTS
- TBS_E_TOO_MANY_RESOURCES
- TBS_E_SERVICE_START_PENDING
- TBS_E_PPI_NOT_SUPPORTED
- TBS_E_COMMAND_CANCELED
- TBS_E_BUFFER_TOO_LARGE
- TBS_E_TPM_NOT_FOUND
- TBS_E_SERVICE_DISABLED
- TBS_E_NO_EVENT_LOG
- TBS_E_ACCESS_DENIED
- TBS_E_PROVISIONING_NOT_ALLOWED
- TBS_E_PPI_FUNCTION_UNSUPPORTED
- TBS_E_OWNERAUTH_NOT_FOUND
- TBS_E_PROVISIONING_INCOMPLETE
api_location:
- Tbs.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a0271c323e4ea300f45817aa59d4f5f9779f9981
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104415576"
---
# <a name="tbs-return-codes"></a>Коды возврата TBS

TBS использует следующие коды для указания результата вызова функции.



| Константа/значение                                                                                                                                                                                                                                                                                   | Описание                                                                                                                                                                                                                                |
|:-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="TBS_SUCCESS"></span><span id="tbs_success"></span><dl> <dt>**TBS \_ УСПЕШНО**</dt> <dt>0 (0x0)</dt> </dl>                                                                             | Функция выполнена успешно.<br/>                                                                                                                                                                                                         |
| <span id="TBS_E_INTERNAL_ERROR"></span><span id="tbs_e_internal_error"></span><dl> <dt>**TBS \_ E \_ Внутренняя \_ Ошибка**</dt> <dt>2150121473 (0x80284001)</dt> </dl>                                | Внутренняя программная ошибка.<br/>                                                                                                                                                                                            |
| <span id="TBS_E_BAD_PARAMETER"></span><span id="tbs_e_bad_parameter"></span><dl> <dt>**TBS \_ \_Неправильный \_ параметр**</dt> <dt>2150121474 (0x80284002)</dt> </dl>                                   | Одно или несколько значений параметров недопустимы.<br/>                                                                                                                                                                                     |
| <span id="TBS_E_INVALID_OUTPUT_POINTER"></span><span id="tbs_e_invalid_output_pointer"></span><dl> <dt>**TBS \_ \_Недопустимый \_ \_ указатель вывода**</dt> <dt>2150121475 (0x80284003)</dt> </dl>       | Указан недопустимый указатель на выход.<br/>                                                                                                                                                                                              |
| <span id="TBS_E_INVALID_CONTEXT"></span><span id="tbs_e_invalid_context"></span><dl> <dt>**TBS \_ \_Недопустимый \_ контекст**</dt> <dt>2150121476 (0x80284004)</dt> </dl>                             | Указанный обработчик контекста не ссылается на допустимый контекст.<br/>                                                                                                                                                                 |
| <span id="TBS_E_INSUFFICIENT_BUFFER"></span><span id="tbs_e_insufficient_buffer"></span><dl> <dt>**TBS \_ \_Недостаточный \_ размер буфера**</dt> <dt>2150121477 (0x80284005)</dt> </dl>                 | Указанный выходной буфер слишком мал.<br/>                                                                                                                                                                                       |
| <span id="TBS_E_IOERROR"></span><span id="tbs_e_ioerror"></span><dl> <dt>**TBS \_ E \_ иоеррор**</dt> <dt>2150121478 (0x80284006)</dt> </dl>                                                      | Произошла ошибка при обмене данными с доверенным платформенным модулем.<br/>                                                                                                                                                                             |
| <span id="TBS_E_INVALID_CONTEXT_PARAM"></span><span id="tbs_e_invalid_context_param"></span><dl> <dt>**TBS \_ \_Недопустимый \_ \_ параметр контекста**</dt> <dt>2150121479 (0x80284007)</dt> </dl>          | При попытке создать контекст TBS был передан недопустимый параметр контекста.<br/>                                                                                                                                       |
| <span id="TBS_E_SERVICE_NOT_RUNNING"></span><span id="tbs_e_service_not_running"></span><dl> <dt>**TBS \_ \_Служба E \_ не \_ работает**</dt> <dt>2150121480 (0x80284008)</dt> </dl>                | Служба TBS не запущена и не может быть запущена.<br/>                                                                                                                                                                        |
| <span id="TBS_E_TOO_MANY_TBS_CONTEXTS"></span><span id="tbs_e_too_many_tbs_contexts"></span><dl> <dt>**TBS \_ \_Слишком \_ много \_ \_ контекстов TBS**</dt> <dt>2150121481 (0x80284009)</dt> </dl>         | Не удалось создать новый контекст, так как открыто слишком много контекстов.<br/>                                                                                                                                                    |
| <span id="TBS_E_TOO_MANY_RESOURCES"></span><span id="tbs_e_too_many_resources"></span><dl> <dt>**TBS \_ \_Слишком \_ много \_ ресурсов**</dt> в <dt>2150121482 (0x8028400A)</dt> </dl>                   | Не удалось создать новый виртуальный ресурс, так как открыто слишком много виртуальных ресурсов.<br/>                                                                                                                                  |
| <span id="TBS_E_SERVICE_START_PENDING"></span><span id="tbs_e_service_start_pending"></span><dl> <dt>**TBS \_ \_ \_ \_ Ожидаемый запуск службы электронной почты**</dt> <dt>2150121483 (0x8028400B)</dt> </dl>          | Служба TBS запущена, но еще не запущена.<br/>                                                                                                                                                                        |
| <span id="TBS_E_PPI_NOT_SUPPORTED"></span><span id="tbs_e_ppi_not_supported"></span><dl> <dt>**TBS \_ E \_ PPI \_ не \_ поддерживается**</dt> <dt>2150121484 (0x8028400C)</dt> </dl>                      | Интерфейс физического присутствия не поддерживается.<br/>                                                                                                                                                                               |
| <span id="TBS_E_COMMAND_CANCELED"></span><span id="tbs_e_command_canceled"></span><dl> <dt>**TBS \_ \_Команда E \_ отменена**</dt> <dt>2150121485 (0x8028400D)</dt> </dl>                          | Команда была отменена.<br/>                                                                                                                                                                                                       |
| <span id="TBS_E_BUFFER_TOO_LARGE"></span><span id="tbs_e_buffer_too_large"></span><dl> <dt>**TBS \_ \_Буфер E \_ слишком \_ большой**</dt> <dt>2150121486 (0x8028400E)</dt> </dl>                         | Слишком большой входной или выходной буфер.<br/>                                                                                                                                                                                        |
| <span id="TBS_E_TPM_NOT_FOUND"></span><span id="tbs_e_tpm_not_found"></span><dl> <dt>**TBS \_ Электронная \_ доверенный платформенный модуль \_ не \_ найден**</dt> <dt>2150121487 (0x8028400F)</dt> </dl>                                  | На этом компьютере не удается найти совместимое устройство безопасности доверенный платформенный модуль (TPM) (доверенный платформенный модуль).<br/>                                                                                                                                    |
| <span id="TBS_E_SERVICE_DISABLED"></span><span id="tbs_e_service_disabled"></span><dl> <dt>**TBS \_ Электронная \_ Служба E \_ отключена**</dt> <dt>2150121488 (0x80284010)</dt> </dl>                          | Служба TBS отключена.<br/>                                                                                                                                                                                              |
| <span id="TBS_E_NO_EVENT_LOG"></span><span id="tbs_e_no_event_log"></span><dl> <dt>**TBS \_ E \_ нет \_ \_ журнала событий**</dt> <dt>2150121489 (0x80284011)</dt> </dl>                                     | Журнал событий TBS недоступен.<br/>                                                                                                                                                                                             |
| <span id="TBS_E_ACCESS_DENIED"></span><span id="tbs_e_access_denied"></span><dl> <dt>**TBS \_ \_Доступ к E \_ запрещен**</dt> <dt>2150121490 (0x80284012)</dt> </dl>                                   | Вызывающий объект не имеет необходимых прав для выполнения запрошенной операции.<br/>                                                                                                                                             |
| <span id="TBS_E_PROVISIONING_NOT_ALLOWED"></span><span id="tbs_e_provisioning_not_allowed"></span><dl> <dt>**TBS \_ \_Подготовка E \_ не \_ разрешена**</dt> <dt>2150121491 (0x80284013)</dt> </dl> | Действие подготовки TPM не разрешено указанными флагами.<br/>                                                                                                                                                              |
| <span id="TBS_E_PPI_FUNCTION_UNSUPPORTED"></span><span id="tbs_e_ppi_function_unsupported"></span><dl> <dt>**TBS \_ Функция "E \_ PPI" \_ \_ не поддерживается**</dt> <dt>2150121492 (0x80284014)</dt> </dl> | Интерфейс физического присутствия этого встроенного по не поддерживает запрошенный метод.<br/>                                                                                                                                         |
| <span id="TBS_E_OWNERAUTH_NOT_FOUND"></span><span id="tbs_e_ownerauth_not_found"></span><dl> <dt>**TBS \_ E \_ овнераус \_ не \_ Найдено**</dt> <dt>2150121493 (0x80284015)</dt> </dl>                | Запрошенное значение Овнераус доверенного платформенного модуля не найдено.<br/>                                                                                                                                                                                |
| <span id="TBS_E_PROVISIONING_INCOMPLETE"></span><span id="tbs_e_provisioning_incomplete"></span><dl> <dt>**TBS \_ \_ \_ Незавершенная подготовка E**</dt> <dt>2150121493 (0x80284015)</dt> </dl>     | Подготовка доверенного платформенного модуля не завершена. Чтобы получить дополнительные сведения о завершении подготовки, вызовите метод [**WMI \_ TPM Win32**](/windows/desktop/SecProv/win32-tpm) для подготовки доверенного платформенного модуля ("подготовка") и проверьте возвращенные сведения.<br/> |



## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------------------------|----------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Только для \[ классических приложений Windows Vista\]<br/>                                   |
| Минимальная версия сервера<br/> | \[Только для настольных приложений Windows Server 2008\]<br/>                             |
| Header<br/>                   | <dl> <dt>TBS. h</dt> </dl> |



 

