---
title: Перечисление МПНОТИФИ (Мпклиент. h)
description: Возможные уведомления обратного вызова.
ms.assetid: CCD0CD89-2C6E-453F-9437-E6ED87AD9F29
keywords:
- мпнотифи перечисления устаревших компонентов среды Windows
- Windows компонентов среды устаревшего указателя перечисления пмпнотифи
topic_type:
- apiref
api_name:
- MPNOTIFY
api_location:
- MpClient.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ed62a9f868aa39cbc0cfc7702afc99849005a22106892696eca857ffb20673af
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "118747792"
---
# <a name="mpnotify-enumeration"></a>Перечисление МПНОТИФИ

Возможные уведомления обратного вызова.

## <a name="syntax"></a>Синтаксис


```C++
typedef enum tagMPNOTIFY { 
  MPNOTIFY_NONE,
  MPNOTIFY_CALL_START,
  MPNOTIFY_CALL_COMPLETE,
  MPNOTIFY_INTERNAL_FAILURE,
  MPNOTIFY_STATUS_SERVICE_START,
  MPNOTIFY_STATUS_SERVICE_RUNNING,
  MPNOTIFY_STATUS_SERVICE_STOP,
  MPNOTIFY_STATUS_COMPONENT,
  MPNOTIFY_STATUS_CHANGE,
  MPNOTIFY_STATUS_COMPONENT_CONFIGURATION,
  MPNOTIFY_STATUS_EXPIRATION_CHANGE,
  MPNOTIFY_STATUS_OFFLINE_SCAN_CHANGE,
  MPNOTIFY_SCAN_START,
  MPNOTIFY_SCAN_PAUSED,
  MPNOTIFY_SCAN_RESUMED,
  MPNOTIFY_SCAN_CANCEL,
  MPNOTIFY_SCAN_COMPLETE,
  MPNOTIFY_SCAN_PROGRESS,
  MPNOTIFY_SCAN_ERROR,
  MPNOTIFY_SCAN_INFECTED,
  MPNOTIFY_SCAN_MEMORYSTART,
  MPNOTIFY_SCAN_MEMORYCOMPLETE,
  MPNOTIFY_SCAN_SFC_BUILD_START,
  MPNOTIFY_SCAN_SFC_BUILD_COMPLETE,
  MPNOTIFY_SCAN_FASTPATH_START,
  MPNOTIFY_SCAN_FASTPATH_COMPLETE,
  MPNOTIFY_SCAN_FASTPATH_PROGRESS,
  MPNOTIFY_CLEAN_START,
  MPNOTIFY_CLEAN_COMPLETE,
  MPNOTIFY_CLEAN_RESTOREPOINT_START,
  MPNOTIFY_CLEAN_RESTOREPOINT_SUCCEEDED,
  MPNOTIFY_CLEAN_RESTOREPOINT_FAILED,
  MPNOTIFY_CLEAN_THREAT_START,
  MPNOTIFY_CLEAN_THREAT_SUCCEEDED,
  MPNOTIFY_CLEAN_THREAT_FAILED,
  MPNOTIFY_CLEAN_RESOURCE_SUCCEEDED,
  MPNOTIFY_CLEAN_RESOURCE_FAILED,
  MPNOTIFY_CLEAN_THREAT_COMPLETE,
  MPNOTIFY_PRECHECK_START,
  MPNOTIFY_PRECHECK_COMPLETE,
  MPNOTIFY_PRECHECK_RESOURCE_BLOCKED,
  MPNOTIFY_THREAT_DETECTED,
  MPNOTIFY_THREAT_MODIFIED,
  MPNOTIFY_THREAT_CLEAN_SUCCEEDED,
  MPNOTIFY_THREAT_CLEAN_FAILED,
  MPNOTIFY_THREAT_ABANDONED,
  MPNOTIFY_THREAT_CLEAN_EVENT_START,
  MPNOTIFY_THREAT_CLEAN_EVENT_COMPLETE,
  MPNOTIFY_SIGUPDATE_START,
  MPNOTIFY_SIGUPDATE_SEARCH_START,
  MPNOTIFY_SIGUPDATE_SEARCH_COMPLETE,
  MPNOTIFY_SIGUPDATE_SOFTWARE_UPDATE_AVAILABLE,
  MPNOTIFY_SIGUPDATE_DOWNLOAD_START,
  MPNOTIFY_SIGUPDATE_DOWNLOAD_PROGRESS,
  MPNOTIFY_SIGUPDATE_DOWNLOAD_COMPLETE,
  MPNOTIFY_SIGUPDATE_INSTALL_START,
  MPNOTIFY_SIGUPDATE_INSTALL_PROGRESS,
  MPNOTIFY_SIGUPDATE_INSTALL_COMPLETE,
  MPNOTIFY_SIGUPDATE_REBOOT_REQUIRED,
  MPNOTIFY_SIGUPDATE_REQUEST_PROCESSED,
  MPNOTIFY_SIGUPDATE_COMPLETE,
  MPNOTIFY_SAMPLE_START,
  MPNOTIFY_SAMPLE_COMPLETE,
  MPNOTIFY_SAMPLE_ITEM_START,
  MPNOTIFY_SAMPLE_ITEM_SUCCEEDED,
  MPNOTIFY_SAMPLE_ITEM_FAILED,
  MPNOTIFY_RESERVED_DATA,
  MPNOTIFY_FASTPATH_SIG_ADDED,
  MPNOTIFY_FASTPATH_SIG_REMOVED,
  MPNOTIFY_NIS_PRIVATE,
  MPNOTIFY_HEALTH_CHANGE,
  MPNOTIFY_HEALTH_RECOVERY,
  MPNOTIFY_HEALTH_START,
  MPNOTIFY_ENDOFLIFE_CHANGE,
  MPNOTIFY_MALWARETOAST_DATA
} MPNOTIFY, *PMPNOTIFY;
```



## <a name="constants"></a>Константы

<dl> <dt>

<span id="MPNOTIFY_NONE"></span><span id="mpnotify_none"></span>**МПНОТИФИ \_ None**
</dt> <dd></dd> <dt>

<span id="MPNOTIFY_CALL_START"></span><span id="mpnotify_call_start"></span>**\_Начало вызова \_ мпнотифи**
</dt> <dd>

Начало вызова уведомления.

</dd> <dt>

<span id="MPNOTIFY_CALL_COMPLETE"></span><span id="mpnotify_call_complete"></span>**\_вызов мпнотифи \_ завершен**
</dt> <dd>

Вызов уведомления завершен.

</dd> <dt>

<span id="MPNOTIFY_INTERNAL_FAILURE"></span><span id="mpnotify_internal_failure"></span>**\_внутренний \_ сбой мпнотифи**
</dt> <dd>

Общий внутренний сбой.

</dd> <dt>

<span id="MPNOTIFY_STATUS_SERVICE_START"></span><span id="mpnotify_status_service_start"></span>**\_ \_ Запуск службы состояния \_ мпнотифи**
</dt> <dd>

Служба защиты от вредоносных программ запущена.

</dd> <dt>

<span id="MPNOTIFY_STATUS_SERVICE_RUNNING"></span><span id="mpnotify_status_service_running"></span>**\_Служба состояния \_ мпнотифи \_ запущена**
</dt> <dd>

Служба защиты от вредоносных программ запущена.

</dd> <dt>

<span id="MPNOTIFY_STATUS_SERVICE_STOP"></span><span id="mpnotify_status_service_stop"></span>**\_ \_ Завершение службы состояния \_ мпнотифи**
</dt> <dd>

Служба защиты от вредоносных программ остановлена.

</dd> <dt>

<span id="MPNOTIFY_STATUS_COMPONENT"></span><span id="mpnotify_status_component"></span>**\_компонент состояния \_ мпнотифи**
</dt> <dd>

Состояние конкретного компонента: включить или отключить.

</dd> <dt>

<span id="MPNOTIFY_STATUS_CHANGE"></span><span id="mpnotify_status_change"></span>**\_изменение состояния \_ мпнотифи**
</dt> <dd>

Изменено общее состояние продукта. Вызовите [**мпманажерстатускуерекс**](mpmanagerstatusqueryex.md) , чтобы получить текущее состояние.

</dd> <dt>

<span id="MPNOTIFY_STATUS_COMPONENT_CONFIGURATION"></span><span id="mpnotify_status_component_configuration"></span>**\_ \_ Конфигурация компонента состояния \_ мпнотифи**
</dt> <dd>

Конфигурация определенного компонента изменилась.

</dd> <dt>

<span id="MPNOTIFY_STATUS_EXPIRATION_CHANGE"></span><span id="mpnotify_status_expiration_change"></span>**\_ \_ изменение срока действия состояния \_ мпнотифи**
</dt> <dd>

Состояние срока действия продукта изменилось.

</dd> <dt>

<span id="MPNOTIFY_STATUS_OFFLINE_SCAN_CHANGE"></span><span id="mpnotify_status_offline_scan_change"></span>**\_ \_ Изменение автономной \_ проверки \_ состояния мпнотифи**
</dt> <dd>

Состояние "требуется Автономная проверка" изменилось.

</dd> <dt>

<span id="MPNOTIFY_SCAN_START"></span><span id="mpnotify_scan_start"></span>**\_Начало СКАНИРОВАНИЯ \_ мпнотифи**
</dt> <dd>

Сканирование начато.

</dd> <dt>

<span id="MPNOTIFY_SCAN_PAUSED"></span><span id="mpnotify_scan_paused"></span>**МПНОТИФИ \_ сканирование \_ приостановлено**
</dt> <dd>

Сканирование приостановлено.

</dd> <dt>

<span id="MPNOTIFY_SCAN_RESUMED"></span><span id="mpnotify_scan_resumed"></span>**\_сканирование мпнотифи \_ возобновлено**
</dt> <dd>

Сканирование возобновлено.

</dd> <dt>

<span id="MPNOTIFY_SCAN_CANCEL"></span><span id="mpnotify_scan_cancel"></span>**\_Отмена СКАНИРОВАНИЯ \_ мпнотифи**
</dt> <dd>

Сканирование отменено.

</dd> <dt>

<span id="MPNOTIFY_SCAN_COMPLETE"></span><span id="mpnotify_scan_complete"></span>**\_сканирование мпнотифи \_ завершено**
</dt> <dd>

Сканирование завершено.

</dd> <dt>

<span id="MPNOTIFY_SCAN_PROGRESS"></span><span id="mpnotify_scan_progress"></span>**\_ \_ ход выполнения сканирования мпнотифи**
</dt> <dd>

Уведомление о ходе выполнения для конкретного проверяемого ресурса.

</dd> <dt>

<span id="MPNOTIFY_SCAN_ERROR"></span><span id="mpnotify_scan_error"></span>**\_Ошибка СКАНИРОВАНИЯ \_ мпнотифи**
</dt> <dd>

Не удалось проверить конкретный ресурс. Сканирование по-прежнему будет продолжаться.

</dd> <dt>

<span id="MPNOTIFY_SCAN_INFECTED"></span><span id="mpnotify_scan_infected"></span>**МПНОТИФИ \_ сканирование с \_ заражением**
</dt> <dd>

Проверка обнаружила зараженный ресурс.

</dd> <dt>

<span id="MPNOTIFY_SCAN_MEMORYSTART"></span><span id="mpnotify_scan_memorystart"></span>**МПНОТИФИ \_ Scan \_ мемористарт**
</dt> <dd>

Ход проверки для уведомления части сканирования памяти, запущенной при проверке системы.

</dd> <dt>

<span id="MPNOTIFY_SCAN_MEMORYCOMPLETE"></span><span id="mpnotify_scan_memorycomplete"></span>**МПНОТИФИ \_ Scan \_ меморикомплете**
</dt> <dd>

Ход сканирования для уведомления части сканирования памяти, выполненной в ходе проверки системы.

</dd> <dt>

<span id="MPNOTIFY_SCAN_SFC_BUILD_START"></span><span id="mpnotify_scan_sfc_build_start"></span>**\_ \_ \_ Начало сборки SFC мпнотифи \_ Scan**
</dt> <dd>

Ход выполнения проверки для уведомления о запуске сборки SFC.

</dd> <dt>

<span id="MPNOTIFY_SCAN_SFC_BUILD_COMPLETE"></span><span id="mpnotify_scan_sfc_build_complete"></span>**\_ \_ Сборка SFC мпнотифи \_ Scan \_ завершена**
</dt> <dd>

Ход выполнения проверки для уведомления о завершении сборки SFC.

</dd> <dt>

<span id="MPNOTIFY_SCAN_FASTPATH_START"></span><span id="mpnotify_scan_fastpath_start"></span>**\_Запуск мпнотифи Scan \_ фастпас \_**
</dt> <dd>

Начато сканирование фастпас SpyNet.

</dd> <dt>

<span id="MPNOTIFY_SCAN_FASTPATH_COMPLETE"></span><span id="mpnotify_scan_fastpath_complete"></span>**МПНОТИФИ \_ сканирование \_ фастпас \_ завершено**
</dt> <dd>

Проверка фастпас SpyNet завершена.

</dd> <dt>

<span id="MPNOTIFY_SCAN_FASTPATH_PROGRESS"></span><span id="mpnotify_scan_fastpath_progress"></span>**\_ \_ ход выполнения мпнотифи сканирования фастпас \_**
</dt> <dd>

Уведомление о ходе повторного сканирования фастпас, которое используется внутренне и преобразуется в **\_ \_ ход выполнения сканирования мпнотифи** для внешних.

</dd> <dt>

<span id="MPNOTIFY_CLEAN_START"></span><span id="mpnotify_clean_start"></span>**\_Начало очистки \_ мпнотифи**
</dt> <dd>

Очистка запущена.

</dd> <dt>

<span id="MPNOTIFY_CLEAN_COMPLETE"></span><span id="mpnotify_clean_complete"></span>**\_Очистка мпнотифи \_ завершена**
</dt> <dd>

Очистка завершена.

</dd> <dt>

<span id="MPNOTIFY_CLEAN_RESTOREPOINT_START"></span><span id="mpnotify_clean_restorepoint_start"></span>**\_Начало очистки \_ ресторепоинт \_ мпнотифи**
</dt> <dd>

Запущено создание точки восстановления системы.

</dd> <dt>

<span id="MPNOTIFY_CLEAN_RESTOREPOINT_SUCCEEDED"></span><span id="mpnotify_clean_restorepoint_succeeded"></span>**МПНОТИФИ \_ Clean \_ ресторепоинт \_ выполнен**
</dt> <dd>

Точка восстановления системы успешно создана.

</dd> <dt>

<span id="MPNOTIFY_CLEAN_RESTOREPOINT_FAILED"></span><span id="mpnotify_clean_restorepoint_failed"></span>**\_сбой мпнотифи Clean \_ ресторепоинт \_**
</dt> <dd>

Не удалось создать точку восстановления системы.

</dd> <dt>

<span id="MPNOTIFY_CLEAN_THREAT_START"></span><span id="mpnotify_clean_threat_start"></span>**\_Запуск мпнотифи очистки \_ угрозы \_**
</dt> <dd>

Для определенной угрозы запускается очистка.

</dd> <dt>

<span id="MPNOTIFY_CLEAN_THREAT_SUCCEEDED"></span><span id="mpnotify_clean_threat_succeeded"></span>**МПНОТИФИ \_ чистая \_ угроза \_ успешной**
</dt> <dd>

Очистка для определенной угрозы прошла.

</dd> <dt>

<span id="MPNOTIFY_CLEAN_THREAT_FAILED"></span><span id="mpnotify_clean_threat_failed"></span>**\_сбой чистой \_ угрозы \_ мпнотифи**
</dt> <dd>

Произошел сбой при очистке определенной угрозы. **Ошибка при \_ Код ошибки пакета управления " \_ \_ не \_ найден** " указывает на то, что угроза не найдена (и не была неудачной).

</dd> <dt>

<span id="MPNOTIFY_CLEAN_RESOURCE_SUCCEEDED"></span><span id="mpnotify_clean_resource_succeeded"></span>**Очистка МПНОТИФИного \_ \_ ресурса \_ прошла**
</dt> <dd>

Очистка для определенного ресурса прошла.

</dd> <dt>

<span id="MPNOTIFY_CLEAN_RESOURCE_FAILED"></span><span id="mpnotify_clean_resource_failed"></span>**\_сбой очистки \_ ресурса \_ мпнотифи**
</dt> <dd>

Произошел сбой при очистке определенного ресурса.

</dd> <dt>

<span id="MPNOTIFY_CLEAN_THREAT_COMPLETE"></span><span id="mpnotify_clean_threat_complete"></span>**МПНОТИФИ \_ Чистка \_ угрозы \_ завершена**
</dt> <dd>

Очистка для определенной угрозы завершена.

</dd> <dt>

<span id="MPNOTIFY_PRECHECK_START"></span><span id="mpnotify_precheck_start"></span>**\_Начало ПРЕДПРОВЕРКИ \_ мпнотифи**
</dt> <dd>

Запущена чистая предпроверка.

</dd> <dt>

<span id="MPNOTIFY_PRECHECK_COMPLETE"></span><span id="mpnotify_precheck_complete"></span>**\_ПРЕДПРОВЕРКА мпнотифи \_ завершена**
</dt> <dd>

Чистая проверка завершена.

</dd> <dt>

<span id="MPNOTIFY_PRECHECK_RESOURCE_BLOCKED"></span><span id="mpnotify_precheck_resource_blocked"></span>**\_ресурс ПРЕДПРОВЕРКИ \_ мпнотифи \_ заблокирован**
</dt> <dd>

Очистка предпроверки обнаружила заблокированный ресурс.

</dd> <dt>

<span id="MPNOTIFY_THREAT_DETECTED"></span><span id="mpnotify_threat_detected"></span>**\_ \_ обнаружена угроза мпнотифи**
</dt> <dd>

В системе обнаружена новая угроза.

</dd> <dt>

<span id="MPNOTIFY_THREAT_MODIFIED"></span><span id="mpnotify_threat_modified"></span>**\_ \_ изменена угроза мпнотифи**
</dt> <dd>

Сведения об угрозе изменены. Например, добавлен новый ресурс.

</dd> <dt>

<span id="MPNOTIFY_THREAT_CLEAN_SUCCEEDED"></span><span id="mpnotify_threat_clean_succeeded"></span>**\_Очистка угрозы \_ мпнотифи \_ прошла**
</dt> <dd>

Действие очистки для угрозы установлено.

</dd> <dt>

<span id="MPNOTIFY_THREAT_CLEAN_FAILED"></span><span id="mpnotify_threat_clean_failed"></span>**\_ \_ сбой очистки угрозы \_ мпнотифи**
</dt> <dd>

Сбой действия очистки для угрозы. **Ошибка при \_ Код ошибки пакета управления " \_ \_ не \_ найден** " указывает на то, что угроза не найдена (и не была неудачной).

</dd> <dt>

<span id="MPNOTIFY_THREAT_ABANDONED"></span><span id="mpnotify_threat_abandoned"></span>**\_ \_ прекращение угрозы мпнотифи**
</dt> <dd>

Не выполнено исправление до остановки службы.

</dd> <dt>

<span id="MPNOTIFY_THREAT_CLEAN_EVENT_START"></span><span id="mpnotify_threat_clean_event_start"></span>**\_ \_ \_ Начало события очистки мпнотифи \_ THREAT**
</dt> <dd>

Начато действие очистки.

</dd> <dt>

<span id="MPNOTIFY_THREAT_CLEAN_EVENT_COMPLETE"></span><span id="mpnotify_threat_clean_event_complete"></span>**\_ \_ событие очистки угрозы \_ мпнотифи \_ завершено**
</dt> <dd>

Действие очистки завершено.

</dd> <dt>

<span id="MPNOTIFY_SIGUPDATE_START"></span><span id="mpnotify_sigupdate_start"></span>**\_Начало СИГУПДАТЕ \_ мпнотифи**
</dt> <dd>

Обновление сигнатуры запущено.

</dd> <dt>

<span id="MPNOTIFY_SIGUPDATE_SEARCH_START"></span><span id="mpnotify_sigupdate_search_start"></span>**\_ \_ Начало поиска мпнотифи \_ сигупдате**
</dt> <dd>

Поиск обновлений начат.

</dd> <dt>

<span id="MPNOTIFY_SIGUPDATE_SEARCH_COMPLETE"></span><span id="mpnotify_sigupdate_search_complete"></span>**\_Поиск мпнотифи \_ сигупдате \_ завершен**
</dt> <dd>

Поиск обновлений завершен.

</dd> <dt>

<span id="MPNOTIFY_SIGUPDATE_SOFTWARE_UPDATE_AVAILABLE"></span><span id="mpnotify_sigupdate_software_update_available"></span>**\_ \_ Доступно обновление программного обеспечения мпнотифи сигупдате \_ \_**
</dt> <dd>

Доступно обновление программного обеспечения.

</dd> <dt>

<span id="MPNOTIFY_SIGUPDATE_DOWNLOAD_START"></span><span id="mpnotify_sigupdate_download_start"></span>**\_ \_ Начало загрузки сигупдате \_ мпнотифи**
</dt> <dd>

Загрузка начата.

</dd> <dt>

<span id="MPNOTIFY_SIGUPDATE_DOWNLOAD_PROGRESS"></span><span id="mpnotify_sigupdate_download_progress"></span>**\_ \_ ход загрузки сигупдате \_ мпнотифи**
</dt> <dd>

Идет скачивание. Данные обратного вызова содержат сведения о ходе выполнения.

</dd> <dt>

<span id="MPNOTIFY_SIGUPDATE_DOWNLOAD_COMPLETE"></span><span id="mpnotify_sigupdate_download_complete"></span>**\_скачивание СИГУПДАТЕ \_ мпнотифи \_ завершено**
</dt> <dd>

Скачивание завершено.

</dd> <dt>

<span id="MPNOTIFY_SIGUPDATE_INSTALL_START"></span><span id="mpnotify_sigupdate_install_start"></span>**\_ \_ Запуск установки мпнотифи \_ сигупдате**
</dt> <dd>

Установка запущена.

</dd> <dt>

<span id="MPNOTIFY_SIGUPDATE_INSTALL_PROGRESS"></span><span id="mpnotify_sigupdate_install_progress"></span>**\_ \_ Ход установки мпнотифи \_ сигупдате**
</dt> <dd>

Выполняется установка. Данные обратного вызова содержат сведения о ходе выполнения.

</dd> <dt>

<span id="MPNOTIFY_SIGUPDATE_INSTALL_COMPLETE"></span><span id="mpnotify_sigupdate_install_complete"></span>**\_Установка СИГУПДАТЕ \_ мпнотифи \_ завершена**
</dt> <dd>

Установка завершена.

</dd> <dt>

<span id="MPNOTIFY_SIGUPDATE_REBOOT_REQUIRED"></span><span id="mpnotify_sigupdate_reboot_required"></span>**\_ \_ требуется перезагрузка сигупдате мпнотифи \_**
</dt> <dd>

Для обновления требуется перезагрузка.

</dd> <dt>

<span id="MPNOTIFY_SIGUPDATE_REQUEST_PROCESSED"></span><span id="mpnotify_sigupdate_request_processed"></span>**\_запрос СИГУПДАТЕ \_ мпнотифи \_ обработан**
</dt> <dd>

Служба обработала запрос на обновление сигнатуры. В данных обратного вызова параметру HRESULT присвоено **значение** "сбой" или "успешно".

</dd> <dt>

<span id="MPNOTIFY_SIGUPDATE_COMPLETE"></span><span id="mpnotify_sigupdate_complete"></span>**МПНОТИФИ \_ сигупдате \_ завершен**
</dt> <dd>

Обновление завершено. **С \_ FALSE** — состояние означает, что обновления не были нужны.

</dd> <dt>

<span id="MPNOTIFY_SAMPLE_START"></span><span id="mpnotify_sample_start"></span>**\_Начало образца \_ мпнотифи**
</dt> <dd>

Начало отправки образца.

</dd> <dt>

<span id="MPNOTIFY_SAMPLE_COMPLETE"></span><span id="mpnotify_sample_complete"></span>**\_Пример мпнотифи \_ завершен**
</dt> <dd>

Отправка образца завершена.

</dd> <dt>

<span id="MPNOTIFY_SAMPLE_ITEM_START"></span><span id="mpnotify_sample_item_start"></span>**\_Начало образца \_ элемента \_ мпнотифи**
</dt> <dd>

Начато отправку указанного примера элемента. Индекс образца элемента доступен в [**\_ данных мпсампле**](mpsample-data.md).

</dd> <dt>

<span id="MPNOTIFY_SAMPLE_ITEM_SUCCEEDED"></span><span id="mpnotify_sample_item_succeeded"></span>**\_образец \_ элемента мпнотифи \_**
</dt> <dd>

Отправка указанного примера элемента прошла.

</dd> <dt>

<span id="MPNOTIFY_SAMPLE_ITEM_FAILED"></span><span id="mpnotify_sample_item_failed"></span>**\_сбой образца \_ элемента \_ мпнотифи**
</dt> <dd>

Не удалось отправить конкретный образец элемента. Код ошибки доступен в [**\_ данных мпкаллбакк**](mpcallback-data.md).

</dd> <dt>

<span id="MPNOTIFY_RESERVED_DATA"></span><span id="mpnotify_reserved_data"></span>**МПНОТИФИ \_ зарезервированные \_ данные**
</dt> <dd>

Внутренние зарезервированные данные.

</dd> <dt>

<span id="MPNOTIFY_FASTPATH_SIG_ADDED"></span><span id="mpnotify_fastpath_sig_added"></span>**\_ \_ ДОБАВЛЕНА подпись мпнотифи \_ фастпас**
</dt> <dd>

Сигнатура Фастпас либо добавила, либо отключила подпись.

</dd> <dt>

<span id="MPNOTIFY_FASTPATH_SIG_REMOVED"></span><span id="mpnotify_fastpath_sig_removed"></span>**\_удален мпнотифи фастпас \_ SIG \_**
</dt> <dd>

Удалена подпись Фастпас.

</dd> <dt>

<span id="MPNOTIFY_NIS_PRIVATE"></span><span id="mpnotify_nis_private"></span>**\_частный мпнотифи NIS \_**
</dt> <dd>

Частный нотифкатионс NIS. Ни один партнер не должен зарегистрироваться для этого.

</dd> <dt>

<span id="MPNOTIFY_HEALTH_CHANGE"></span><span id="mpnotify_health_change"></span>**\_изменение работоспособности мпнотифи \_**
</dt> <dd>

Служба AM перешла в новое состояние.

</dd> <dt>

<span id="MPNOTIFY_HEALTH_RECOVERY"></span><span id="mpnotify_health_recovery"></span>**\_восстановление работоспособности мпнотифи \_**
</dt> <dd>

Служба AM восстановлена из состояния.

</dd> <dt>

<span id="MPNOTIFY_HEALTH_START"></span><span id="mpnotify_health_start"></span>**\_Начало работоспособности мпнотифи \_**
</dt> <dd>

Служба AM инициализировала работоспособность системы.

</dd> <dt>

<span id="MPNOTIFY_ENDOFLIFE_CHANGE"></span><span id="mpnotify_endoflife_change"></span>**\_изменение мпнотифи ендофлифе \_**
</dt> <dd>

Изменились даты окончания срока действия для службы AM.

</dd> <dt>

<span id="MPNOTIFY_MALWARETOAST_DATA"></span><span id="mpnotify_malwaretoast_data"></span>**МПНОТИФИ \_ малваретоаст \_ данные**
</dt> <dd>

В службе AM обнаружены вредоносные программы, которые могли привести к изменению критических параметров на компьютере.

</dd> </dl>

## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Windows 8 \[ только классические приложения\]<br/>                                            |
| Минимальная версия сервера<br/> | Windows Server 2012 \[ только классические приложения\]<br/>                                  |
| Header<br/>                   | <dl> <dt>Мпклиент. h</dt> </dl> |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[**мпманажерстатускуерекс**](mpmanagerstatusqueryex.md)
</dt> <dt>

[**\_данные мпкаллбакк**](mpcallback-data.md)
</dt> <dt>

[**\_данные мпсампле**](mpsample-data.md)
</dt> </dl>

 

 





