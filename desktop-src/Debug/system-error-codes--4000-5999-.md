---
description: Описание кодов ошибок 4000-5999, определенных в файле заголовка WinError. h и предназначенных для разработчиков.
ms.assetid: 1d2f7160-6322-4c75-abbc-4a882bbdf7ce
title: Коды системных ошибок (4000-5999) (WinError. h)
ms.topic: reference
ms.date: 07/18/2019
ms.openlocfilehash: bfd39042489f2a92ff2eb13df92a22e392c5405e
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104141614"
---
# <a name="system-error-codes-4000-5999"></a>Коды системных ошибок (4000-5999)

> [!NOTE]
> Эти сведения предназначены для разработчиков, которые отлаживать системные ошибки. Для других ошибок, например проблем с Центр обновления Windows, на странице [коды ошибок](system-error-codes.md) содержится список ресурсов.

В следующем списке приведены [коды системных ошибок](system-error-codes.md) для ошибок 4000 – 5999. Они возвращаются функцией [**GetLastError**](/windows/win32/api/errhandlingapi/nf-errhandlingapi-getlasterror) при сбое множества функций. Чтобы получить текст описания ошибки в приложении, используйте функцию [**FormatMessage**](/windows/desktop/api/WinBase/nf-winbase-formatmessage) с флагом **формата \_ Message \_ из \_ System** .

<dl> <dt>

<span id="ERROR_WINS_INTERNAL"></span><span id="error_wins_internal"></span>**\_Внутренняя ошибка WINS \_**
</dt> <dd> <dl> <dt>

4000 (0xFA0)
</dt> <dt>



При обработке команды произошла ошибка WINS.


</dt> </dl> </dd> <dt>

<span id="ERROR_CAN_NOT_DEL_LOCAL_WINS"></span><span id="error_can_not_del_local_wins"></span>**Ошибка \_ не может быть \_ \_ Del \_ локальную \_ службу WINS**
</dt> <dd> <dl> <dt>

4001 (0xFA1)
</dt> <dt>



Невозможно удалить локальный WINS-сервер.


</dt> </dl> </dd> <dt>

<span id="ERROR_STATIC_INIT"></span><span id="error_static_init"></span>**Ошибка при \_ статической \_ инициализации**
</dt> <dd> <dl> <dt>

4002 (0xFA2)
</dt> <dt>



Не удалось выполнить импорт из файла.


</dt> </dl> </dd> <dt>

<span id="ERROR_INC_BACKUP"></span><span id="error_inc_backup"></span>**\_Архив ошибок Inc \_**
</dt> <dd> <dl> <dt>

4003 (0xFA3)
</dt> <dt>



Сбой резервного копирования. Было ли выполнено полное резервное копирование ранее?


</dt> </dl> </dd> <dt>

<span id="ERROR_FULL_BACKUP"></span><span id="error_full_backup"></span>**Ошибка \_ полной \_ архивации**
</dt> <dd> <dl> <dt>

4004 (0xFA4)
</dt> <dt>



Сбой резервного копирования. Проверьте каталог, в котором выполняется резервное копирование базы данных.


</dt> </dl> </dd> <dt>

<span id="ERROR_REC_NON_EXISTENT"></span><span id="error_rec_non_existent"></span>**Ошибка \_ REC \_ не \_ существует**
</dt> <dd> <dl> <dt>

4005 (0xFA5)
</dt> <dt>



Имя не существует в базе данных WINS.


</dt> </dl> </dd> <dt>

<span id="ERROR_RPL_NOT_ALLOWED"></span><span id="error_rpl_not_allowed"></span>**Ошибка \_ RPL \_ не \_ разрешена**
</dt> <dd> <dl> <dt>

4006 (0xFA6)
</dt> <dt>



Репликация с ненастроенным партнером не разрешена.


</dt> </dl> </dd> <dt>

<span id="PEERDIST_ERROR_CONTENTINFO_VERSION_UNSUPPORTED"></span><span id="peerdist_error_contentinfo_version_unsupported"></span>**\_Ошибка \_ контентинфо \_ версия \_ не поддерживается**
</dt> <dd> <dl> <dt>

4050 (0xFD2)
</dt> <dt>



Версия предоставляемых сведений о содержимом не поддерживается.


</dt> </dl> </dd> <dt>

<span id="PEERDIST_ERROR_CANNOT_PARSE_CONTENTINFO"></span><span id="peerdist_error_cannot_parse_contentinfo"></span>**\_Ошибка в \_ удалось \_ проанализировать \_ контентинфо**
</dt> <dd> <dl> <dt>

4051 (0xFD3)
</dt> <dt>



Указанная информация о содержимом неправильно сформирована.


</dt> </dl> </dd> <dt>

<span id="PEERDIST_ERROR_MISSING_DATA"></span><span id="peerdist_error_missing_data"></span>**Ошибка в сведениях о том, что \_ \_ \_ данные отсутствуют**
</dt> <dd> <dl> <dt>

4052 (0xFD4)
</dt> <dt>



Запрошенные данные не могут быть найдены в локальных и одноранговых кэшах.


</dt> </dl> </dd> <dt>

<span id="PEERDIST_ERROR_NO_MORE"></span><span id="peerdist_error_no_more"></span>**Ошибка в некотором сообщении о наличии \_ \_ \_**
</dt> <dd> <dl> <dt>

4053 (0xFD5)
</dt> <dt>



Дополнительные данные недоступны или не требуются.


</dt> </dl> </dd> <dt>

<span id="PEERDIST_ERROR_NOT_INITIALIZED"></span><span id="peerdist_error_not_initialized"></span>**ошибка, которая \_ \_ не была \_ инициализирована.**
</dt> <dd> <dl> <dt>

4054 (0xFD6)
</dt> <dt>



Предоставленный объект не был инициализирован.


</dt> </dl> </dd> <dt>

<span id="PEERDIST_ERROR_ALREADY_INITIALIZED"></span><span id="peerdist_error_already_initialized"></span>**ошибка, которая \_ \_ уже \_ инициализирована, не выполнена**
</dt> <dd> <dl> <dt>

4055 (0xFD7)
</dt> <dt>



Предоставленный объект уже инициализирован.


</dt> </dl> </dd> <dt>

<span id="PEERDIST_ERROR_SHUTDOWN_IN_PROGRESS"></span><span id="peerdist_error_shutdown_in_progress"></span>**\_ \_ выполняется завершение работы \_ с ошибкой в списке \_**
</dt> <dd> <dl> <dt>

4056 (0xFD8)
</dt> <dt>



Операция завершения работы уже выполняется.


</dt> </dl> </dd> <dt>

<span id="PEERDIST_ERROR_INVALIDATED"></span><span id="peerdist_error_invalidated"></span>**ошибка, которая \_ \_ стала недействительной**
</dt> <dd> <dl> <dt>

4057 (0xFD9)
</dt> <dt>



Предоставленный объект уже недействителен.


</dt> </dl> </dd> <dt>

<span id="PEERDIST_ERROR_ALREADY_EXISTS"></span><span id="peerdist_error_already_exists"></span>**\_возникла ошибка, которая \_ уже \_ существует**
</dt> <dd> <dl> <dt>

4058 (0xFDA)
</dt> <dt>



Элемент уже существует и не был заменен.


</dt> </dl> </dd> <dt>

<span id="PEERDIST_ERROR_OPERATION_NOTFOUND"></span><span id="peerdist_error_operation_notfound"></span>**\_Ошибка \_ NotFound, операция \_**
</dt> <dd> <dl> <dt>

4059 (0xFDB)
</dt> <dt>



Невозможно отменить запрошенную операцию, так как она уже завершена.


</dt> </dl> </dd> <dt>

<span id="PEERDIST_ERROR_ALREADY_COMPLETED"></span><span id="peerdist_error_already_completed"></span>**ошибка, которая \_ \_ уже \_ завершена**
</dt> <dd> <dl> <dt>

4060 (0xFDC)
</dt> <dt>



Невозможно выполнить операцию запрошена, так как она уже была выполнена.


</dt> </dl> </dd> <dt>

<span id="PEERDIST_ERROR_OUT_OF_BOUNDS"></span><span id="peerdist_error_out_of_bounds"></span>**\_Ошибка \_ \_ , \_ связанная с нехваткой границ**
</dt> <dd> <dl> <dt>

4061 (0xFDD)
</dt> <dt>



Операция обратилась к данным за границами допустимых данных.


</dt> </dl> </dd> <dt>

<span id="PEERDIST_ERROR_VERSION_UNSUPPORTED"></span><span id="peerdist_error_version_unsupported"></span>**\_версия ошибки, которую \_ \_ не поддерживает, не поддерживается**
</dt> <dd> <dl> <dt>

4062 (0xFDE)
</dt> <dt>



Запрошенная версия не поддерживается.


</dt> </dl> </dd> <dt>

<span id="PEERDIST_ERROR_INVALID_CONFIGURATION"></span><span id="peerdist_error_invalid_configuration"></span>**ошибка, которая является \_ \_ недопустимой \_ конфигурацией**
</dt> <dd> <dl> <dt>

4063 (0xFDF)
</dt> <dt>



Недопустимое значение конфигурации.


</dt> </dl> </dd> <dt>

<span id="PEERDIST_ERROR_NOT_LICENSED"></span><span id="peerdist_error_not_licensed"></span>**Ошибка продукта, которая \_ \_ не \_ лицензирована**
</dt> <dd> <dl> <dt>

4064 (0xFE0)
</dt> <dt>



Номер SKU не лицензирован.


</dt> </dl> </dd> <dt>

<span id="PEERDIST_ERROR_SERVICE_UNAVAILABLE"></span><span id="peerdist_error_service_unavailable"></span>**\_Служба ошибок в \_ пакетах обновления \_ недоступна**
</dt> <dd> <dl> <dt>

4065 (0xFE1)
</dt> <dt>



Служба, которая по-прежнему инициализируется, будет доступна в ближайшее время.


</dt> </dl> </dd> <dt>

<span id="PEERDIST_ERROR_TRUST_FAILURE"></span><span id="peerdist_error_trust_failure"></span>**\_ \_ сбой при доверии для ошибки, \_**
</dt> <dd> <dl> <dt>

4066 (0xFE2)
</dt> <dt>



Связь с одним или несколькими компьютерами будет временно заблокирована из-за последних ошибок.


</dt> </dl> </dd> <dt>

<span id="ERROR_DHCP_ADDRESS_CONFLICT"></span><span id="error_dhcp_address_conflict"></span>**Ошибка \_ при \_ конфликте DHCP-адресов \_**
</dt> <dd> <dl> <dt>

4100 (0x1004)
</dt> <dt>



DHCP-клиент получил IP-адрес, который уже используется в сети. Локальный интерфейс будет отключен до тех пор, пока DHCP-клиент не сможет получить новый адрес.


</dt> </dl> </dd> <dt>

<span id="ERROR_WMI_GUID_NOT_FOUND"></span><span id="error_wmi_guid_not_found"></span>**Ошибка \_ \_ GUID WMI \_ не \_ найден**
</dt> <dd> <dl> <dt>

4200 (0x1068)
</dt> <dt>



Переданный идентификатор GUID не распознан поставщиком данных WMI как допустимый.


</dt> </dl> </dd> <dt>

<span id="ERROR_WMI_INSTANCE_NOT_FOUND"></span><span id="error_wmi_instance_not_found"></span>**экземпляр WMI об ОШИБКе \_ \_ \_ не \_ найден**
</dt> <dd> <dl> <dt>

4201 (0x1069)
</dt> <dt>



Переданное имя экземпляра не было распознано поставщиком данных WMI как допустимое.


</dt> </dl> </dd> <dt>

<span id="ERROR_WMI_ITEMID_NOT_FOUND"></span><span id="error_wmi_itemid_not_found"></span>**ОШИБКА с \_ WMI \_ ITEMID \_ не \_ найден**
</dt> <dd> <dl> <dt>

4202 (0x106A)
</dt> <dt>



Переданный идентификатор элемента данных не распознан поставщиком данных WMI как допустимый.


</dt> </dl> </dd> <dt>

<span id="ERROR_WMI_TRY_AGAIN"></span><span id="error_wmi_try_again"></span>**Ошибка \_ WMI \_ \_ Повторная попытка**
</dt> <dd> <dl> <dt>

4203 (0x106B)
</dt> <dt>



Не удалось выполнить запрос WMI и повторить попытку.


</dt> </dl> </dd> <dt>

<span id="ERROR_WMI_DP_NOT_FOUND"></span><span id="error_wmi_dp_not_found"></span>**Ошибка \_ " \_ точка распространения WMI \_ не \_ найдена"**
</dt> <dd> <dl> <dt>

4204 (0x106C)
</dt> <dt>



Не удалось найти поставщик данных WMI.


</dt> </dl> </dd> <dt>

<span id="ERROR_WMI_UNRESOLVED_INSTANCE_REF"></span><span id="error_wmi_unresolved_instance_ref"></span>**Ошибка \_ \_ ссылки на неразрешенный \_ экземпляр WMI \_**
</dt> <dd> <dl> <dt>

4205 (0x106D)
</dt> <dt>



Поставщик данных WMI ссылается на набор экземпляров, который не был зарегистрирован.


</dt> </dl> </dd> <dt>

<span id="ERROR_WMI_ALREADY_ENABLED"></span><span id="error_wmi_already_enabled"></span>**Ошибка \_ WMI \_ уже \_ включена**
</dt> <dd> <dl> <dt>

4206 (0x106E)
</dt> <dt>



Блок данных WMI или уведомление о событии уже включены.


</dt> </dl> </dd> <dt>

<span id="ERROR_WMI_GUID_DISCONNECTED"></span><span id="error_wmi_guid_disconnected"></span>**Ошибка \_ при \_ \_ отключении GUID WMI**
</dt> <dd> <dl> <dt>

4207 (0x106F)
</dt> <dt>



Блок данных WMI больше не доступен.


</dt> </dl> </dd> <dt>

<span id="ERROR_WMI_SERVER_UNAVAILABLE"></span><span id="error_wmi_server_unavailable"></span>**Ошибка \_ \_ Сервер WMI \_ недоступен**
</dt> <dd> <dl> <dt>

4208 (0x1070)
</dt> <dt>



Служба данных WMI недоступна.


</dt> </dl> </dd> <dt>

<span id="ERROR_WMI_DP_FAILED"></span><span id="error_wmi_dp_failed"></span>**Ошибка \_ WMI \_ DP \_ при сбое**
</dt> <dd> <dl> <dt>

4209 (0x1071)
</dt> <dt>



Поставщику данных WMI не удалось выполнить запрос.


</dt> </dl> </dd> <dt>

<span id="ERROR_WMI_INVALID_MOF"></span><span id="error_wmi_invalid_mof"></span>**Ошибка \_ WMI- \_ Недопустимый \_ MOF**
</dt> <dd> <dl> <dt>

4210 (0x1072)
</dt> <dt>



Сведения об WMI MOF недопустимы.


</dt> </dl> </dd> <dt>

<span id="ERROR_WMI_INVALID_REGINFO"></span><span id="error_wmi_invalid_reginfo"></span>**Ошибка \_ WMI \_ Недопустимая \_ регинфо**
</dt> <dd> <dl> <dt>

4211 (0x1073)
</dt> <dt>



Недопустимые сведения о регистрации WMI.


</dt> </dl> </dd> <dt>

<span id="ERROR_WMI_ALREADY_DISABLED"></span><span id="error_wmi_already_disabled"></span>**Ошибка \_ WMI \_ уже \_ отключена**
</dt> <dd> <dl> <dt>

4212 (0x1074)
</dt> <dt>



Блок данных WMI или уведомление о событии уже отключены.


</dt> </dl> </dd> <dt>

<span id="ERROR_WMI_READ_ONLY"></span><span id="error_wmi_read_only"></span>**Ошибка \_ \_ только для чтения WMI \_**
</dt> <dd> <dl> <dt>

4213 (0x1075)
</dt> <dt>



Элемент данных или блок данных WMI доступен только для чтения.


</dt> </dl> </dd> <dt>

<span id="ERROR_WMI_SET_FAILURE"></span><span id="error_wmi_set_failure"></span>**Ошибка \_ \_ при установке \_ WMI**
</dt> <dd> <dl> <dt>

4214 (0x1076)
</dt> <dt>



Не удалось изменить элемент данных или блок данных WMI.


</dt> </dl> </dd> <dt>

<span id="ERROR_NOT_APPCONTAINER"></span><span id="error_not_appcontainer"></span>**Ошибка \_ не является \_ APPCONTAINER**
</dt> <dd> <dl> <dt>

4250 (0x109A)
</dt> <dt>



Эта операция допустима только в контексте контейнера приложения.


</dt> </dl> </dd> <dt>

<span id="ERROR_APPCONTAINER_REQUIRED"></span><span id="error_appcontainer_required"></span>**\_требуется ошибка APPCONTAINER \_**
</dt> <dd> <dl> <dt>

4251 (0x109B)
</dt> <dt>



Это приложение может выполняться только в контексте контейнера приложения.


</dt> </dl> </dd> <dt>

<span id="ERROR_NOT_SUPPORTED_IN_APPCONTAINER"></span><span id="error_not_supported_in_appcontainer"></span>**Ошибка \_ не \_ поддерживается \_ в \_ APPCONTAINER**
</dt> <dd> <dl> <dt>

4252 (0x109C)
</dt> <dt>



Эта функция не поддерживается в контексте контейнера приложения.


</dt> </dl> </dd> <dt>

<span id="ERROR_INVALID_PACKAGE_SID_LENGTH"></span><span id="error_invalid_package_sid_length"></span>**Ошибка \_ Недопустимая \_ \_ Длина идентификатора безопасности пакета \_**
</dt> <dd> <dl> <dt>

4253 (0x109D)
</dt> <dt>



Длина переданного идентификатора SID не является допустимой для идентификаторов безопасности контейнера приложений.


</dt> </dl> </dd> <dt>

<span id="ERROR_INVALID_MEDIA"></span><span id="error_invalid_media"></span>**Ошибка \_ недопустимого \_ носителя**
</dt> <dd> <dl> <dt>

4300 (0x10CC)
</dt> <dt>



Идентификатор носителя не представляет допустимый носитель.


</dt> </dl> </dd> <dt>

<span id="ERROR_INVALID_LIBRARY"></span><span id="error_invalid_library"></span>**Ошибка \_ недопустимой \_ библиотеки**
</dt> <dd> <dl> <dt>

4301 (0x10CD)
</dt> <dt>



Идентификатор библиотеки не представляет допустимую библиотеку.


</dt> </dl> </dd> <dt>

<span id="ERROR_INVALID_MEDIA_POOL"></span><span id="error_invalid_media_pool"></span>**Ошибка \_ недопустимого \_ \_ пула носителей**
</dt> <dd> <dl> <dt>

4302 (0x10CE)
</dt> <dt>



Идентификатор пула носителей не представляет допустимый пул носителей.


</dt> </dl> </dd> <dt>

<span id="ERROR_DRIVE_MEDIA_MISMATCH"></span><span id="error_drive_media_mismatch"></span>**Ошибка \_ при \_ \_ несоответствии носителя**
</dt> <dd> <dl> <dt>

4303 (0x10CF)
</dt> <dt>



Диск и носитель не совместимы или существуют в разных библиотеках.


</dt> </dl> </dd> <dt>

<span id="ERROR_MEDIA_OFFLINE"></span><span id="error_media_offline"></span>**Ошибка \_ мультимедиа в \_ автономном режиме**
</dt> <dd> <dl> <dt>

4304 (0x10D0)
</dt> <dt>



Носитель в данный момент находится в автономной библиотеке и должен быть подключен к сети для выполнения этой операции.


</dt> </dl> </dd> <dt>

<span id="ERROR_LIBRARY_OFFLINE"></span><span id="error_library_offline"></span>**\_Библиотека ошибок \_ вне сети**
</dt> <dd> <dl> <dt>

4305 (0x10D1)
</dt> <dt>



Невозможно выполнить операцию для автономной библиотеки.


</dt> </dl> </dd> <dt>

<span id="ERROR_EMPTY"></span><span id="error_empty"></span>**Ошибка \_ пуста**
</dt> <dd> <dl> <dt>

4306 (0x10D2)
</dt> <dt>



Библиотека, диск или пул носителей пусты.


</dt> </dl> </dd> <dt>

<span id="ERROR_NOT_EMPTY"></span><span id="error_not_empty"></span>**Ошибка \_ не \_ пуста**
</dt> <dd> <dl> <dt>

4307 (0x10D3)
</dt> <dt>



Для выполнения этой операции Библиотека, диск или пул носителей должны быть пустыми.


</dt> </dl> </dd> <dt>

<span id="ERROR_MEDIA_UNAVAILABLE"></span><span id="error_media_unavailable"></span>**\_носитель ошибок \_ недоступен**
</dt> <dd> <dl> <dt>

4308 (0x10D4)
</dt> <dt>



В этом пуле носителей или библиотеке нет доступных носителей.


</dt> </dl> </dd> <dt>

<span id="ERROR_RESOURCE_DISABLED"></span><span id="error_resource_disabled"></span>**ресурс об ОШИБКе \_ \_ отключен**
</dt> <dd> <dl> <dt>

4309 (0x10D5)
</dt> <dt>



Ресурс, необходимый для этой операции, отключен.


</dt> </dl> </dd> <dt>

<span id="ERROR_INVALID_CLEANER"></span><span id="error_invalid_cleaner"></span>**Ошибка \_ неправильной \_ очистки**
</dt> <dd> <dl> <dt>

4310 (0x10D6)
</dt> <dt>



Идентификатор носителя не представляет допустимый очиститель.


</dt> </dl> </dd> <dt>

<span id="ERROR_UNABLE_TO_CLEAN"></span><span id="error_unable_to_clean"></span>**\_не удалось \_ \_ очистить**
</dt> <dd> <dl> <dt>

4311 (0x10D7)
</dt> <dt>



Диск не может быть очищен или не поддерживает очистку.


</dt> </dl> </dd> <dt>

<span id="ERROR_OBJECT_NOT_FOUND"></span><span id="error_object_not_found"></span>**\_объект ошибки \_ не \_ найден**
</dt> <dd> <dl> <dt>

4312 (0x10D8)
</dt> <dt>



Идентификатор объекта не представляет допустимый объект.


</dt> </dl> </dd> <dt>

<span id="ERROR_DATABASE_FAILURE"></span><span id="error_database_failure"></span>**Ошибка \_ базы данных при ошибке \_**
</dt> <dd> <dl> <dt>

4313 (0x10D9)
</dt> <dt>



Не удается выполнить чтение из базы данных или запись в нее.


</dt> </dl> </dd> <dt>

<span id="ERROR_DATABASE_FULL"></span><span id="error_database_full"></span>**\_база данных с ошибкой \_ заполнена**
</dt> <dd> <dl> <dt>

4314 (0x10DA)
</dt> <dt>



База данных заполнена.


</dt> </dl> </dd> <dt>

<span id="ERROR_MEDIA_INCOMPATIBLE"></span><span id="error_media_incompatible"></span>**несовместимость носителя с ОШИБКАми \_ \_**
</dt> <dd> <dl> <dt>

4315 (0x10DB)
</dt> <dt>



Носитель не совместим с устройством или пулом носителей.


</dt> </dl> </dd> <dt>

<span id="ERROR_RESOURCE_NOT_PRESENT"></span><span id="error_resource_not_present"></span>**\_ресурс ошибки \_ отсутствует \_**
</dt> <dd> <dl> <dt>

4316 (0x10DC)
</dt> <dt>



Ресурс, необходимый для этой операции, не существует.


</dt> </dl> </dd> <dt>

<span id="ERROR_INVALID_OPERATION"></span><span id="error_invalid_operation"></span>**Ошибка \_ недопустимой \_ операции**
</dt> <dd> <dl> <dt>

4317 (0x10DD)
</dt> <dt>



Недопустимый идентификатор операции.


</dt> </dl> </dd> <dt>

<span id="ERROR_MEDIA_NOT_AVAILABLE"></span><span id="error_media_not_available"></span>**\_носитель ошибок \_ \_ недоступен**
</dt> <dd> <dl> <dt>

4318 (0x10DE)
</dt> <dt>



Носитель не подключен или готов к использованию.


</dt> </dl> </dd> <dt>

<span id="ERROR_DEVICE_NOT_AVAILABLE"></span><span id="error_device_not_available"></span>**устройство с ОШИБКАми \_ \_ \_ недоступно**
</dt> <dd> <dl> <dt>

4319 (0x10DF)
</dt> <dt>



Устройство не готово к использованию.


</dt> </dl> </dd> <dt>

<span id="ERROR_REQUEST_REFUSED"></span><span id="error_request_refused"></span>**запрос на ошибку \_ \_ отклонен**
</dt> <dd> <dl> <dt>

4320 (0x10E0)
</dt> <dt>



Оператор или администратор отклонили запрос.


</dt> </dl> </dd> <dt>

<span id="ERROR_INVALID_DRIVE_OBJECT"></span><span id="error_invalid_drive_object"></span>**Ошибка в \_ недопустимом \_ \_ объекте диска**
</dt> <dd> <dl> <dt>

4321 (0x10E1)
</dt> <dt>



Идентификатор диска не представляет допустимый диск.


</dt> </dl> </dd> <dt>

<span id="ERROR_LIBRARY_FULL"></span><span id="error_library_full"></span>**\_Библиотека ошибок \_ заполнена**
</dt> <dd> <dl> <dt>

4322 (0x10E2)
</dt> <dt>



Библиотека заполнена. Нет слота, доступной для использования.


</dt> </dl> </dd> <dt>

<span id="ERROR_MEDIUM_NOT_ACCESSIBLE"></span><span id="error_medium_not_accessible"></span>**Ошибка \_ : средний уровень \_ \_ недоступен**
</dt> <dd> <dl> <dt>

4323 (0x10E3)
</dt> <dt>



Транспорту не удается получить доступ к носителю.


</dt> </dl> </dd> <dt>

<span id="ERROR_UNABLE_TO_LOAD_MEDIUM"></span><span id="error_unable_to_load_medium"></span>**\_не удалось \_ \_ загрузить \_ носитель**
</dt> <dd> <dl> <dt>

4324 (0x10E4)
</dt> <dt>



Не удалось загрузить носитель в диск.


</dt> </dl> </dd> <dt>

<span id="ERROR_UNABLE_TO_INVENTORY_DRIVE"></span><span id="error_unable_to_inventory_drive"></span>**Ошибка \_ при \_ \_ инвентаризации \_ диска**
</dt> <dd> <dl> <dt>

4325 (0x10E5)
</dt> <dt>



Не удалось получить состояние диска.


</dt> </dl> </dd> <dt>

<span id="ERROR_UNABLE_TO_INVENTORY_SLOT"></span><span id="error_unable_to_inventory_slot"></span>**Ошибка \_ не удалось выполнить \_ \_ инвентаризацию \_ слота**
</dt> <dd> <dl> <dt>

4326 (0x10E6)
</dt> <dt>



Не удалось получить состояние слота.


</dt> </dl> </dd> <dt>

<span id="ERROR_UNABLE_TO_INVENTORY_TRANSPORT"></span><span id="error_unable_to_inventory_transport"></span>**Ошибка \_ при \_ \_ инвентаризации \_ транспорта**
</dt> <dd> <dl> <dt>

4327 (0x10E7)
</dt> <dt>



Не удалось получить сведения о состоянии транспорта.


</dt> </dl> </dd> <dt>

<span id="ERROR_TRANSPORT_FULL"></span><span id="error_transport_full"></span>**\_полный транспорт \_ ошибок**
</dt> <dd> <dl> <dt>

4328 (0x10E8)
</dt> <dt>



Невозможно использовать транспорт, так как он уже используется.


</dt> </dl> </dd> <dt>

<span id="ERROR_CONTROLLING_IEPORT"></span><span id="error_controlling_ieport"></span>**Ошибка \_ управления \_ IEPORT**
</dt> <dd> <dl> <dt>

4329 (0x10E9)
</dt> <dt>



Не удается открыть или закрыть порт вставки и извлечения.


</dt> </dl> </dd> <dt>

<span id="ERROR_UNABLE_TO_EJECT_MOUNTED_MEDIA"></span><span id="error_unable_to_eject_mounted_media"></span>**Ошибка \_ не \_ удалось \_ извлечь \_ подключенный \_ носитель**
</dt> <dd> <dl> <dt>

4330 (0x10EA)
</dt> <dt>



Не удалось извлечь носитель, так как он находится на диске.


</dt> </dl> </dd> <dt>

<span id="ERROR_CLEANER_SLOT_SET"></span><span id="error_cleaner_slot_set"></span>**Ошибка \_ очистки \_ набора слотов \_**
</dt> <dd> <dl> <dt>

4331 (0x10EB)
</dt> <dt>



Слот очистителя уже зарезервирован.


</dt> </dl> </dd> <dt>

<span id="ERROR_CLEANER_SLOT_NOT_SET"></span><span id="error_cleaner_slot_not_set"></span>**Ошибка \_ очистки \_ слота \_ не \_ задана**
</dt> <dd> <dl> <dt>

4332 (0x10EC)
</dt> <dt>



Слот очистителя не зарезервирован.


</dt> </dl> </dd> <dt>

<span id="ERROR_CLEANER_CARTRIDGE_SPENT"></span><span id="error_cleaner_cartridge_spent"></span>**Ошибка \_ чистящего \_ картриджа очистки \_**
</dt> <dd> <dl> <dt>

4333 (0x10ED)
</dt> <dt>



Чистящая кассета выполнила максимальное число чистых дисков.


</dt> </dl> </dd> <dt>

<span id="ERROR_UNEXPECTED_OMID"></span><span id="error_unexpected_omid"></span>**произошла \_ непредвиденная ошибка \_ Omid**
</dt> <dd> <dl> <dt>

4334 (0x10EE)
</dt> <dt>



Непредвиденный идентификатор на носителе.


</dt> </dl> </dd> <dt>

<span id="ERROR_CANT_DELETE_LAST_ITEM"></span><span id="error_cant_delete_last_item"></span>**ОШИБКА не \_ удается \_ удалить \_ последний \_ элемент**
</dt> <dd> <dl> <dt>

4335 (0x10EF)
</dt> <dt>



Не удается удалить последний оставшийся элемент в этой группе или ресурсе.


</dt> </dl> </dd> <dt>

<span id="ERROR_MESSAGE_EXCEEDS_MAX_SIZE"></span><span id="error_message_exceeds_max_size"></span>**сообщение об ОШИБКе \_ \_ превышает \_ максимальный \_ Размер**
</dt> <dd> <dl> <dt>

4336 (0x10F0)
</dt> <dt>



Указанное сообщение превышает максимальный размер, допустимый для этого параметра.


</dt> </dl> </dd> <dt>

<span id="ERROR_VOLUME_CONTAINS_SYS_FILES"></span><span id="error_volume_contains_sys_files"></span>**\_том ошибок \_ содержит \_ sys \_ файлов**
</dt> <dd> <dl> <dt>

4337 (0x10F1)
</dt> <dt>



Том содержит системные или файлы подкачки.


</dt> </dl> </dd> <dt>

<span id="ERROR_INDIGENOUS_TYPE"></span><span id="error_indigenous_type"></span>**\_тип ошибки местных \_**
</dt> <dd> <dl> <dt>

4338 (0x10F2)
</dt> <dt>



Невозможно удалить тип носителя из этой библиотеки, так как по крайней мере один диск в библиотеке сообщает, что он поддерживает этот тип носителя.


</dt> </dl> </dd> <dt>

<span id="ERROR_NO_SUPPORTING_DRIVES"></span><span id="error_no_supporting_drives"></span>**Ошибка \_ не \_ поддерживает \_ диски**
</dt> <dd> <dl> <dt>

4339 (0x10F3)
</dt> <dt>



Этот автономный носитель не может быть подключен к этой системе, так как не существует включенных дисков, которые можно использовать.


</dt> </dl> </dd> <dt>

<span id="ERROR_CLEANER_CARTRIDGE_INSTALLED"></span><span id="error_cleaner_cartridge_installed"></span>**Ошибка \_ при \_ установке чистящего картриджа \_**
</dt> <dd> <dl> <dt>

4340 (0x10F4)
</dt> <dt>



В ленточной библиотеке имеется чистящий картридж.


</dt> </dl> </dd> <dt>

<span id="ERROR_IEPORT_FULL"></span><span id="error_ieport_full"></span>**Ошибка \_ IEPORT \_ Full**
</dt> <dd> <dl> <dt>

4341 (0x10F5)
</dt> <dt>



Невозможно использовать порт вставки и извлечения, так как он не пуст.


</dt> </dl> </dd> <dt>

<span id="ERROR_FILE_OFFLINE"></span><span id="error_file_offline"></span>**\_файл ошибок \_ вне сети**
</dt> <dd> <dl> <dt>

4350 (0x10FE)
</dt> <dt>



Этот файл сейчас недоступен для использования на этом компьютере.


</dt> </dl> </dd> <dt>

<span id="ERROR_REMOTE_STORAGE_NOT_ACTIVE"></span><span id="error_remote_storage_not_active"></span>**Ошибка " \_ Удаленное \_ хранилище \_ не \_ активно"**
</dt> <dd> <dl> <dt>

4351 (0x10FF)
</dt> <dt>



Служба внешнего хранилища в настоящее время неработоспособна.


</dt> </dl> </dd> <dt>

<span id="ERROR_REMOTE_STORAGE_MEDIA_ERROR"></span><span id="error_remote_storage_media_error"></span>**Ошибка \_ \_ носителя удаленного \_ хранилища \_**
</dt> <dd> <dl> <dt>

4352 (0x1100)
</dt> <dt>



Служба внешнего хранилища обнаружила ошибку носителя.


</dt> </dl> </dd> <dt>

<span id="ERROR_NOT_A_REPARSE_POINT"></span><span id="error_not_a_reparse_point"></span>**Ошибка \_ не \_ является \_ точкой повторного \_ анализа**
</dt> <dd> <dl> <dt>

4390 (0x1126)
</dt> <dt>



Файл или каталог не является точкой повторного анализа.


</dt> </dl> </dd> <dt>

<span id="ERROR_REPARSE_ATTRIBUTE_CONFLICT"></span><span id="error_reparse_attribute_conflict"></span>**Ошибка \_ при \_ конфликте атрибутов повторного анализа \_**
</dt> <dd> <dl> <dt>

4391 (0x1127)
</dt> <dt>



Невозможно задать атрибут точки повторной обработки, так как он конфликтует с существующим атрибутом.


</dt> </dl> </dd> <dt>

<span id="ERROR_INVALID_REPARSE_DATA"></span><span id="error_invalid_reparse_data"></span>**Ошибка \_ недопустимых \_ данных повторного анализа \_**
</dt> <dd> <dl> <dt>

4392 (0x1128)
</dt> <dt>



Данные в буфере точки повторной обработки недопустимы.


</dt> </dl> </dd> <dt>

<span id="ERROR_REPARSE_TAG_INVALID"></span><span id="error_reparse_tag_invalid"></span>**\_Недопустимый тег повторного анализа ошибок \_ \_**
</dt> <dd> <dl> <dt>

4393 (0x1129)
</dt> <dt>



В буфере точки повторной обработки указан недопустимый тег.


</dt> </dl> </dd> <dt>

<span id="ERROR_REPARSE_TAG_MISMATCH"></span><span id="error_reparse_tag_mismatch"></span>**Ошибка \_ при \_ несоответствии тегов при повторном анализе \_**
</dt> <dd> <dl> <dt>

4394 (0x112A)
</dt> <dt>



Обнаружено несоответствие между тегом, указанным в запросе, и тегом, который присутствует в точке повторного анализа.


</dt> </dl> </dd> <dt>

<span id="ERROR_APP_DATA_NOT_FOUND"></span><span id="error_app_data_not_found"></span>**\_ \_ \_ не \_ найдены данные приложения об ошибках**
</dt> <dd> <dl> <dt>

4400 (0x1130)
</dt> <dt>



Не найдены данные быстрого кэширования.


</dt> </dl> </dd> <dt>

<span id="ERROR_APP_DATA_EXPIRED"></span><span id="error_app_data_expired"></span>**Ошибка \_ при \_ \_ истечении срока действия данных приложения**
</dt> <dd> <dl> <dt>

4401 (0x1131)
</dt> <dt>



Срок действия данных быстрого кэширования истек.


</dt> </dl> </dd> <dt>

<span id="ERROR_APP_DATA_CORRUPT"></span><span id="error_app_data_corrupt"></span>**ОШИБКИ \_ в \_ данных приложения \_ повреждены**
</dt> <dd> <dl> <dt>

4402 (0x1132)
</dt> <dt>



Данные быстрого кэширования повреждены.


</dt> </dl> </dd> <dt>

<span id="ERROR_APP_DATA_LIMIT_EXCEEDED"></span><span id="error_app_data_limit_exceeded"></span>**\_ \_ \_ превышен предел данных приложения \_ об ошибках**
</dt> <dd> <dl> <dt>

4403 (0x1133)
</dt> <dt>



Данные быстрого кэширования превысили максимальный размер и не могут быть обновлены.


</dt> </dl> </dd> <dt>

<span id="ERROR_APP_DATA_REBOOT_REQUIRED"></span><span id="error_app_data_reboot_required"></span>**Ошибка \_ при \_ \_ перезагрузке данных приложения \_**
</dt> <dd> <dl> <dt>

4404 (0x1134)
</dt> <dt>



Быстрый кэш был восстановлен и требует перезагрузки, пока его невозможно будет обновить.


</dt> </dl> </dd> <dt>

<span id="ERROR_SECUREBOOT_ROLLBACK_DETECTED"></span><span id="error_secureboot_rollback_detected"></span>**\_ \_ обнаружена ошибка безопасной загрузки отката \_**
</dt> <dd> <dl> <dt>

4420 (0x1144)
</dt> <dt>



При безопасной загрузке обнаружен откат защищенных данных.


</dt> </dl> </dd> <dt>

<span id="ERROR_SECUREBOOT_POLICY_VIOLATION"></span><span id="error_secureboot_policy_violation"></span>**Ошибка \_ безопасной загрузки \_ \_ нарушение политики**
</dt> <dd> <dl> <dt>

4421 (0x1145)
</dt> <dt>



Значение защищено политикой безопасной загрузки и не может быть изменено или удалено.


</dt> </dl> </dd> <dt>

<span id="ERROR_SECUREBOOT_INVALID_POLICY"></span><span id="error_secureboot_invalid_policy"></span>**Ошибка \_ безопасной загрузки \_ Недопустимая \_ Политика**
</dt> <dd> <dl> <dt>

4422 (0x1146)
</dt> <dt>



Недопустимая политика безопасной загрузки.


</dt> </dl> </dd> <dt>

<span id="ERROR_SECUREBOOT_POLICY_PUBLISHER_NOT_FOUND"></span><span id="error_secureboot_policy_publisher_not_found"></span>**Ошибка \_ безопасной загрузки \_ политики \_ \_ не \_ найдена**
</dt> <dd> <dl> <dt>

4423 (0x1147)
</dt> <dt>



Новая политика безопасной загрузки не содержала текущий издатель в списке обновлений.


</dt> </dl> </dd> <dt>

<span id="ERROR_SECUREBOOT_POLICY_NOT_SIGNED"></span><span id="error_secureboot_policy_not_signed"></span>**Ошибка \_ безопасной загрузки. \_ политика \_ не \_ подписана**
</dt> <dd> <dl> <dt>

4424 (0x1148)
</dt> <dt>



Политика безопасной загрузки либо не подписана, либо подписана недоверенным подписывающий.


</dt> </dl> </dd> <dt>

<span id="ERROR_SECUREBOOT_NOT_ENABLED"></span><span id="error_secureboot_not_enabled"></span>**Ошибка \_ безопасной загрузки \_ не \_ включена**
</dt> <dd> <dl> <dt>

4425 (0x1149)
</dt> <dt>



Безопасная загрузка не включена на этом компьютере.


</dt> </dl> </dd> <dt>

<span id="ERROR_SECUREBOOT_FILE_REPLACED"></span><span id="error_secureboot_file_replaced"></span>**Ошибка \_ при \_ \_ замене файла безопасной загрузки**
</dt> <dd> <dl> <dt>

4426 (0x114A)
</dt> <dt>



Для безопасной загрузки необходимо, чтобы определенные файлы и драйверы не были заменены другими файлами или драйверами.


</dt> </dl> </dd> <dt>

<span id="ERROR_OFFLOAD_READ_FLT_NOT_SUPPORTED"></span><span id="error_offload_read_flt_not_supported"></span>**Ошибка \_ разгрузки \_ Read \_ ФЛТ \_ не \_ поддерживается**
</dt> <dd> <dl> <dt>

4440 (0x1158)
</dt> <dt>



Операция чтения копии разгрузки не поддерживается фильтром.


</dt> </dl> </dd> <dt>

<span id="ERROR_OFFLOAD_WRITE_FLT_NOT_SUPPORTED"></span><span id="error_offload_write_flt_not_supported"></span>**Ошибка \_ разгрузки \_ записи \_ ФЛТ \_ не \_ поддерживается**
</dt> <dd> <dl> <dt>

4441 (0x1159)
</dt> <dt>



Операция записи для разгрузки копий не поддерживается фильтром.


</dt> </dl> </dd> <dt>

<span id="ERROR_OFFLOAD_READ_FILE_NOT_SUPPORTED"></span><span id="error_offload_read_file_not_supported"></span>**Ошибка \_ разгрузки \_ чтения \_ файла \_ не \_ поддерживается**
</dt> <dd> <dl> <dt>

4442 (0x115A)
</dt> <dt>



Операция чтения копии разгрузки для файла не поддерживается.


</dt> </dl> </dd> <dt>

<span id="ERROR_OFFLOAD_WRITE_FILE_NOT_SUPPORTED"></span><span id="error_offload_write_file_not_supported"></span>**Ошибка \_ разгрузки \_ \_ файла записи \_ не \_ поддерживается**
</dt> <dd> <dl> <dt>

4443 (0x115B)
</dt> <dt>



Операция записи разгрузки копирования не поддерживается для этого файла.


</dt> </dl> </dd> <dt>

<span id="ERROR_VOLUME_NOT_SIS_ENABLED"></span><span id="error_volume_not_sis_enabled"></span>**\_том ошибки \_ не \_ \_ включен SIS**
</dt> <dd> <dl> <dt>

4500 (0x1194)
</dt> <dt>



Хранилище единственных экземпляров недоступно на этом томе.


</dt> </dl> </dd> <dt>

<span id="ERROR_DEPENDENT_RESOURCE_EXISTS"></span><span id="error_dependent_resource_exists"></span>**\_существует ресурс, зависящий от ошибки \_ \_**
</dt> <dd> <dl> <dt>

5001 (0x1389)
</dt> <dt>



Операция не может быть завершена, так как другие ресурсы зависят от этого ресурса.


</dt> </dl> </dd> <dt>

<span id="ERROR_DEPENDENCY_NOT_FOUND"></span><span id="error_dependency_not_found"></span>**\_зависимость ошибок \_ не \_ найдена**
</dt> <dd> <dl> <dt>

5002 (0x138A)
</dt> <dt>



Не удается найти зависимость ресурса кластера.


</dt> </dl> </dd> <dt>

<span id="ERROR_DEPENDENCY_ALREADY_EXISTS"></span><span id="error_dependency_already_exists"></span>**\_зависимость ошибок \_ уже \_ существует**
</dt> <dd> <dl> <dt>

5003 (0x138B)
</dt> <dt>



Невозможно сделать ресурс кластера зависимым от указанного ресурса, так как он уже является зависимым.


</dt> </dl> </dd> <dt>

<span id="ERROR_RESOURCE_NOT_ONLINE"></span><span id="error_resource_not_online"></span>**\_ресурс ошибки \_ не в \_ сети**
</dt> <dd> <dl> <dt>

5004 (0x138C)
</dt> <dt>



Ресурс кластера находится вне сети.


</dt> </dl> </dd> <dt>

<span id="ERROR_HOST_NODE_NOT_AVAILABLE"></span><span id="error_host_node_not_available"></span>**\_узел узла \_ ошибок \_ \_ недоступен**
</dt> <dd> <dl> <dt>

5005 (0x138D)
</dt> <dt>



Узел кластера недоступен для этой операции.


</dt> </dl> </dd> <dt>

<span id="ERROR_RESOURCE_NOT_AVAILABLE"></span><span id="error_resource_not_available"></span>**\_ресурс ошибки \_ \_ недоступен**
</dt> <dd> <dl> <dt>

5006 (0x138E)
</dt> <dt>



Ресурс кластера недоступен.


</dt> </dl> </dd> <dt>

<span id="ERROR_RESOURCE_NOT_FOUND"></span><span id="error_resource_not_found"></span>**ресурс об ОШИБКе \_ \_ не \_ найден**
</dt> <dd> <dl> <dt>

5007 (0x138F)
</dt> <dt>



Не удалось найти ресурс кластера.


</dt> </dl> </dd> <dt>

<span id="ERROR_SHUTDOWN_CLUSTER"></span><span id="error_shutdown_cluster"></span>**Ошибка при \_ завершении работы \_ кластера**
</dt> <dd> <dl> <dt>

5008 (0x1390)
</dt> <dt>



Идет завершение работы кластера.


</dt> </dl> </dd> <dt>

<span id="ERROR_CANT_EVICT_ACTIVE_NODE"></span><span id="error_cant_evict_active_node"></span>**ОШИБКА не \_ удается \_ исключить \_ Активный \_ узел**
</dt> <dd> <dl> <dt>

5009 (0x1391)
</dt> <dt>



Узел кластера не может быть удален из кластера, если узел не работает или является последним узлом.


</dt> </dl> </dd> <dt>

<span id="ERROR_OBJECT_ALREADY_EXISTS"></span><span id="error_object_already_exists"></span>**\_объект ошибки \_ уже \_ существует**
</dt> <dd> <dl> <dt>

5010 (0x1392)
</dt> <dt>



Объект уже существует.


</dt> </dl> </dd> <dt>

<span id="ERROR_OBJECT_IN_LIST"></span><span id="error_object_in_list"></span>**\_объект Error \_ в \_ списке**
</dt> <dd> <dl> <dt>

5011 (0x1393)
</dt> <dt>



Объект уже находится в списке.


</dt> </dl> </dd> <dt>

<span id="ERROR_GROUP_NOT_AVAILABLE"></span><span id="error_group_not_available"></span>**\_Группа ошибок \_ \_ недоступна**
</dt> <dd> <dl> <dt>

5012 (0x1394)
</dt> <dt>



Группа кластеров недоступна для новых запросов.


</dt> </dl> </dd> <dt>

<span id="ERROR_GROUP_NOT_FOUND"></span><span id="error_group_not_found"></span>**\_Группа ошибок \_ не \_ найдена**
</dt> <dd> <dl> <dt>

5013 (0x1395)
</dt> <dt>



Не удалось найти группу кластеров.


</dt> </dl> </dd> <dt>

<span id="ERROR_GROUP_NOT_ONLINE"></span><span id="error_group_not_online"></span>**\_Группа ошибок \_ не в \_ сети**
</dt> <dd> <dl> <dt>

5014 (0x1396)
</dt> <dt>



Не удалось выполнить операцию, так как кластерная группа не находится в режиме "в сети".


</dt> </dl> </dd> <dt>

<span id="ERROR_HOST_NODE_NOT_RESOURCE_OWNER"></span><span id="error_host_node_not_resource_owner"></span>**Ошибка \_ " \_ узел узла \_ не является \_ \_ владельцем ресурса"**
</dt> <dd> <dl> <dt>

5015 (0x1397)
</dt> <dt>



Не удалось выполнить операцию, так как указанный узел кластера не является владельцем ресурса, или узел не является возможным владельцем ресурса.


</dt> </dl> </dd> <dt>

<span id="ERROR_HOST_NODE_NOT_GROUP_OWNER"></span><span id="error_host_node_not_group_owner"></span>**Ошибка \_ " \_ узел узла \_ не является \_ \_ владельцем группы"**
</dt> <dd> <dl> <dt>

5016 (0x1398)
</dt> <dt>



Не удалось выполнить операцию, так как указанный узел кластера не является и не может стать владельцем этой группы.


</dt> </dl> </dd> <dt>

<span id="ERROR_RESMON_CREATE_FAILED"></span><span id="error_resmon_create_failed"></span>**Ошибка \_ \_ при создании \_ ресмон**
</dt> <dd> <dl> <dt>

5017 (0x1399)
</dt> <dt>



Не удалось создать ресурс кластера в указанном мониторе ресурсов.


</dt> </dl> </dd> <dt>

<span id="ERROR_RESMON_ONLINE_FAILED"></span><span id="error_resmon_online_failed"></span>**Ошибка \_ ресмон в \_ сети \_**
</dt> <dd> <dl> <dt>

5018 (0x139A)
</dt> <dt>



Монитору ресурсов не удалось перевести ресурс кластера в режим "в сети".


</dt> </dl> </dd> <dt>

<span id="ERROR_RESOURCE_ONLINE"></span><span id="error_resource_online"></span>**ресурс ошибки в \_ \_ сети**
</dt> <dd> <dl> <dt>

5019 (0x139B)
</dt> <dt>



Не удалось выполнить операцию, так как ресурс кластера находится в режиме "в сети".


</dt> </dl> </dd> <dt>

<span id="ERROR_QUORUM_RESOURCE"></span><span id="error_quorum_resource"></span>**ресурс с ошибкой \_ кворума \_**
</dt> <dd> <dl> <dt>

5020 (0x139C)
</dt> <dt>



Ресурс кластера не может быть удален или переведен в автономный режим, так как он является ресурсом кворума.


</dt> </dl> </dd> <dt>

<span id="ERROR_NOT_QUORUM_CAPABLE"></span><span id="error_not_quorum_capable"></span>**Ошибка \_ не \_ \_ поддерживает кворум**
</dt> <dd> <dl> <dt>

5021 (0x139D)
</dt> <dt>



Кластеру не удалось сделать указанный ресурс ресурсом кворума, так как он не может быть ресурсом кворума.


</dt> </dl> </dd> <dt>

<span id="ERROR_CLUSTER_SHUTTING_DOWN"></span><span id="error_cluster_shutting_down"></span>**Ошибка \_ при \_ завершении работы кластера \_**
</dt> <dd> <dl> <dt>

5022 (0x139E)
</dt> <dt>



Завершается работа программного обеспечения кластера.


</dt> </dl> </dd> <dt>

<span id="ERROR_INVALID_STATE"></span><span id="error_invalid_state"></span>**Ошибка \_ недопустимого \_ состояния**
</dt> <dd> <dl> <dt>

5023 (0x139F)
</dt> <dt>



Группа или ресурс находятся в неправильном состоянии для выполнения запрошенной операции.


</dt> </dl> </dd> <dt>

<span id="ERROR_RESOURCE_PROPERTIES_STORED"></span><span id="error_resource_properties_stored"></span>**\_свойства ресурса \_ ошибки \_ сохранены**
</dt> <dd> <dl> <dt>

5024 (0x13A0)
</dt> <dt>



Свойства были сохранены, но не все изменения вступят в силу до того, как ресурс вновь перейдет в оперативный режим.


</dt> </dl> </dd> <dt>

<span id="ERROR_NOT_QUORUM_CLASS"></span><span id="error_not_quorum_class"></span>**Ошибка \_ не \_ является \_ классом кворума**
</dt> <dd> <dl> <dt>

5025 (0x13A1)
</dt> <dt>



Кластеру не удалось сделать указанный ресурс ресурсом кворума, так как он не принадлежит к общему классу хранилища.


</dt> </dl> </dd> <dt>

<span id="ERROR_CORE_RESOURCE"></span><span id="error_core_resource"></span>**\_ресурс ядра \_ ошибки**
</dt> <dd> <dl> <dt>

5026 (0x13A2)
</dt> <dt>



Не удалось удалить ресурс кластера, так как он является основным ресурсом.


</dt> </dl> </dd> <dt>

<span id="ERROR_QUORUM_RESOURCE_ONLINE_FAILED"></span><span id="error_quorum_resource_online_failed"></span>**\_сбой ресурса кворума "ошибка в \_ \_ сети \_ "**
</dt> <dd> <dl> <dt>

5027 (0x13A3)
</dt> <dt>



Не удалось подключить ресурс кворума к сети.


</dt> </dl> </dd> <dt>

<span id="ERROR_QUORUMLOG_OPEN_FAILED"></span><span id="error_quorumlog_open_failed"></span>**Ошибка \_ \_ при открытии \_ куорумлог**
</dt> <dd> <dl> <dt>

5028 (0x13A4)
</dt> <dt>



Не удалось успешно создать или присоединить журнал кворума.


</dt> </dl> </dd> <dt>

<span id="ERROR_CLUSTERLOG_CORRUPT"></span><span id="error_clusterlog_corrupt"></span>**Ошибка \_ CLUSTERLOG \_ повреждена**
</dt> <dd> <dl> <dt>

5029 (0x13A5)
</dt> <dt>



Журнал кластера поврежден.


</dt> </dl> </dd> <dt>

<span id="ERROR_CLUSTERLOG_RECORD_EXCEEDS_MAXSIZE"></span><span id="error_clusterlog_record_exceeds_maxsize"></span>**Ошибка \_ \_ записи CLUSTERLOG \_ превышает \_ MAXSIZE**
</dt> <dd> <dl> <dt>

5030 (0x13A6)
</dt> <dt>



Запись не может быть записана в журнал кластера, так как она превышает максимальный размер.


</dt> </dl> </dd> <dt>

<span id="ERROR_CLUSTERLOG_EXCEEDS_MAXSIZE"></span><span id="error_clusterlog_exceeds_maxsize"></span>**Ошибка \_ CLUSTERLOG \_ превышает \_ MAXSIZE**
</dt> <dd> <dl> <dt>

5031 (0x13A7)
</dt> <dt>



Размер журнала кластера превышает максимальный.


</dt> </dl> </dd> <dt>

<span id="ERROR_CLUSTERLOG_CHKPOINT_NOT_FOUND"></span><span id="error_clusterlog_chkpoint_not_found"></span>**Ошибка \_ CLUSTERLOG \_ чкпоинт \_ не \_ найдена**
</dt> <dd> <dl> <dt>

5032 (0x13A8)
</dt> <dt>



В журнале кластера не найдена запись контрольной точки.


</dt> </dl> </dd> <dt>

<span id="ERROR_CLUSTERLOG_NOT_ENOUGH_SPACE"></span><span id="error_clusterlog_not_enough_space"></span>**Ошибка \_ CLUSTERLOG \_ \_ недостаточно \_ места**
</dt> <dd> <dl> <dt>

5033 (0x13A9)
</dt> <dt>



Минимально необходимое для ведения журнала место на диске недоступно.


</dt> </dl> </dd> <dt>

<span id="ERROR_QUORUM_OWNER_ALIVE"></span><span id="error_quorum_owner_alive"></span>**Ошибка \_ в \_ активном владельце кворума \_**
</dt> <dd> <dl> <dt>

5034 (0x13AA)
</dt> <dt>



Узлу кластера не удалось получить управление ресурсом кворума, так как владельцем ресурса является другой активный узел.


</dt> </dl> </dd> <dt>

<span id="ERROR_NETWORK_NOT_AVAILABLE"></span><span id="error_network_not_available"></span>**\_сеть ошибок \_ \_ недоступна**
</dt> <dd> <dl> <dt>

5035 (0x13AB)
</dt> <dt>



Сеть кластера недоступна для этой операции.


</dt> </dl> </dd> <dt>

<span id="ERROR_NODE_NOT_AVAILABLE"></span><span id="error_node_not_available"></span>**\_узел ошибки \_ \_ недоступен**
</dt> <dd> <dl> <dt>

5036 (0x13AC)
</dt> <dt>



Узел кластера недоступен для этой операции.


</dt> </dl> </dd> <dt>

<span id="ERROR_ALL_NODES_NOT_AVAILABLE"></span><span id="error_all_nodes_not_available"></span>**Ошибка \_ все \_ узлы \_ \_ недоступны**
</dt> <dd> <dl> <dt>

5037 (0x13AD)
</dt> <dt>



Для выполнения этой операции должны быть установлены все узлы кластера.


</dt> </dl> </dd> <dt>

<span id="ERROR_RESOURCE_FAILED"></span><span id="error_resource_failed"></span>**\_сбой ресурса "ошибка" \_**
</dt> <dd> <dl> <dt>

5038 (0x13AE)
</dt> <dt>



сбой ресурса кластера.


</dt> </dl> </dd> <dt>

<span id="ERROR_CLUSTER_INVALID_NODE"></span><span id="error_cluster_invalid_node"></span>**\_ \_ Недопустимый \_ узел кластера ошибок**
</dt> <dd> <dl> <dt>

5039 (0x13AF)
</dt> <dt>



Недопустимый узел кластера.


</dt> </dl> </dd> <dt>

<span id="ERROR_CLUSTER_NODE_EXISTS"></span><span id="error_cluster_node_exists"></span>**\_узел кластера \_ ошибок \_ существует**
</dt> <dd> <dl> <dt>

5040 (0x13B0)
</dt> <dt>



Узел кластера уже существует.


</dt> </dl> </dd> <dt>

<span id="ERROR_CLUSTER_JOIN_IN_PROGRESS"></span><span id="error_cluster_join_in_progress"></span>**Ошибка \_ \_ при присоединении кластера \_ \_**
</dt> <dd> <dl> <dt>

5041 (0x13B1)
</dt> <dt>



Узел находится в процессе присоединения к кластеру.


</dt> </dl> </dd> <dt>

<span id="ERROR_CLUSTER_NODE_NOT_FOUND"></span><span id="error_cluster_node_not_found"></span>**\_узел кластера \_ ошибок \_ не \_ найден**
</dt> <dd> <dl> <dt>

5042 (0x13B2)
</dt> <dt>



Узел кластера не найден.


</dt> </dl> </dd> <dt>

<span id="ERROR_CLUSTER_LOCAL_NODE_NOT_FOUND"></span><span id="error_cluster_local_node_not_found"></span>**\_ \_ \_ \_ не найден локальный узел кластера \_ ошибок**
</dt> <dd> <dl> <dt>

5043 (0x13B3)
</dt> <dt>



Сведения о локальном узле кластера не найдены.


</dt> </dl> </dd> <dt>

<span id="ERROR_CLUSTER_NETWORK_EXISTS"></span><span id="error_cluster_network_exists"></span>**\_существует ошибка \_ сети \_ кластера**
</dt> <dd> <dl> <dt>

5044 (0x13B4)
</dt> <dt>



Сеть кластера уже существует.


</dt> </dl> </dd> <dt>

<span id="ERROR_CLUSTER_NETWORK_NOT_FOUND"></span><span id="error_cluster_network_not_found"></span>**Ошибка \_ \_ сети кластера \_ не \_ найдена**
</dt> <dd> <dl> <dt>

5045 (0x13B5)
</dt> <dt>



Сеть кластера не найдена.


</dt> </dl> </dd> <dt>

<span id="ERROR_CLUSTER_NETINTERFACE_EXISTS"></span><span id="error_cluster_netinterface_exists"></span>**\_нетинтерфаце кластера \_ ошибок \_ существует**
</dt> <dd> <dl> <dt>

5046 (0x13B6)
</dt> <dt>



Сетевой интерфейс кластера уже существует.


</dt> </dl> </dd> <dt>

<span id="ERROR_CLUSTER_NETINTERFACE_NOT_FOUND"></span><span id="error_cluster_netinterface_not_found"></span>**Ошибка \_ кластера \_ нетинтерфаце \_ не \_ найдена**
</dt> <dd> <dl> <dt>

5047 (0x13B7)
</dt> <dt>



Не удалось найти сетевой интерфейс кластера.


</dt> </dl> </dd> <dt>

<span id="ERROR_CLUSTER_INVALID_REQUEST"></span><span id="error_cluster_invalid_request"></span>**\_ \_ Недопустимый \_ запрос кластера ошибок**
</dt> <dd> <dl> <dt>

5048 (0x13B8)
</dt> <dt>



Запрос кластера недопустим для этого объекта.


</dt> </dl> </dd> <dt>

<span id="ERROR_CLUSTER_INVALID_NETWORK_PROVIDER"></span><span id="error_cluster_invalid_network_provider"></span>**кластер ошибок — \_ \_ Недопустимый \_ \_ поставщик сети**
</dt> <dd> <dl> <dt>

5049 (0x13B9)
</dt> <dt>



Недопустимый поставщик сети кластеров.


</dt> </dl> </dd> <dt>

<span id="ERROR_CLUSTER_NODE_DOWN"></span><span id="error_cluster_node_down"></span>**Ошибка \_ \_ отключения узла \_ кластера**
</dt> <dd> <dl> <dt>

5050 (0x13BA)
</dt> <dt>



Узел кластера не работает.


</dt> </dl> </dd> <dt>

<span id="ERROR_CLUSTER_NODE_UNREACHABLE"></span><span id="error_cluster_node_unreachable"></span>**\_узел кластера \_ ошибок \_ недоступен**
</dt> <dd> <dl> <dt>

5051 (0x13BB)
</dt> <dt>



Узел кластера недоступен.


</dt> </dl> </dd> <dt>

<span id="ERROR_CLUSTER_NODE_NOT_MEMBER"></span><span id="error_cluster_node_not_member"></span>**Ошибка \_ узла кластера, \_ \_ не \_ входящего в группу**
</dt> <dd> <dl> <dt>

5052 (0x13BC)
</dt> <dt>



Узел кластера не является членом кластера.


</dt> </dl> </dd> <dt>

<span id="ERROR_CLUSTER_JOIN_NOT_IN_PROGRESS"></span><span id="error_cluster_join_not_in_progress"></span>**Ошибка \_ \_ Присоединение к кластеру \_ не \_ \_ выполняется**
</dt> <dd> <dl> <dt>

5053 (0x13BD)
</dt> <dt>



Операция присоединение к кластеру не выполняется.


</dt> </dl> </dd> <dt>

<span id="ERROR_CLUSTER_INVALID_NETWORK"></span><span id="error_cluster_invalid_network"></span>**\_ \_ недействительная \_ сеть кластера ошибок**
</dt> <dd> <dl> <dt>

5054 (0x13BE)
</dt> <dt>



Недопустимая сеть кластера.


</dt> </dl> </dd> <dt>

<span id="ERROR_CLUSTER_NODE_UP"></span><span id="error_cluster_node_up"></span>**\_узел кластера \_ ошибок \_**
</dt> <dd> <dl> <dt>

5056 (0x13C0)
</dt> <dt>



Узел кластера работает.


</dt> </dl> </dd> <dt>

<span id="ERROR_CLUSTER_IPADDR_IN_USE"></span><span id="error_cluster_ipaddr_in_use"></span>**\_используется кластер \_ ошибок \_ reduce \_**
</dt> <dd> <dl> <dt>

5057 (0x13C1)
</dt> <dt>



IP-адрес кластера уже используется.


</dt> </dl> </dd> <dt>

<span id="ERROR_CLUSTER_NODE_NOT_PAUSED"></span><span id="error_cluster_node_not_paused"></span>**\_узел кластера \_ ошибок \_ не \_ приостановлен**
</dt> <dd> <dl> <dt>

5058 (0x13C2)
</dt> <dt>



Узел кластера не приостановлен.


</dt> </dl> </dd> <dt>

<span id="ERROR_CLUSTER_NO_SECURITY_CONTEXT"></span><span id="error_cluster_no_security_context"></span>**\_кластер ошибок \_ без \_ \_ контекста безопасности**
</dt> <dd> <dl> <dt>

5059 (0x13C3)
</dt> <dt>



Контекст безопасности кластера недоступен.


</dt> </dl> </dd> <dt>

<span id="ERROR_CLUSTER_NETWORK_NOT_INTERNAL"></span><span id="error_cluster_network_not_internal"></span>**Ошибка \_ сети кластера, \_ \_ не \_ внутренней**
</dt> <dd> <dl> <dt>

5060 (0x13C4)
</dt> <dt>



Сеть кластера не настроена для взаимодействия с внутренним кластером.


</dt> </dl> </dd> <dt>

<span id="ERROR_CLUSTER_NODE_ALREADY_UP"></span><span id="error_cluster_node_already_up"></span>**\_узел кластера \_ ошибок \_ уже \_ включен**
</dt> <dd> <dl> <dt>

5061 (0x13C5)
</dt> <dt>



Узел кластера уже включен.


</dt> </dl> </dd> <dt>

<span id="ERROR_CLUSTER_NODE_ALREADY_DOWN"></span><span id="error_cluster_node_already_down"></span>**\_узел кластера \_ ошибок \_ уже \_ отключен**
</dt> <dd> <dl> <dt>

5062 (0x13C6)
</dt> <dt>



Узел кластера уже отключен.


</dt> </dl> </dd> <dt>

<span id="ERROR_CLUSTER_NETWORK_ALREADY_ONLINE"></span><span id="error_cluster_network_already_online"></span>**Ошибка \_ \_ сети кластера \_ уже в \_ сети**
</dt> <dd> <dl> <dt>

5063 (0x13C7)
</dt> <dt>



Сеть кластера уже подключена.


</dt> </dl> </dd> <dt>

<span id="ERROR_CLUSTER_NETWORK_ALREADY_OFFLINE"></span><span id="error_cluster_network_already_offline"></span>**Ошибка \_ \_ сети кластера \_ уже \_ вне сети**
</dt> <dd> <dl> <dt>

5064 (0x13C8)
</dt> <dt>



Сеть кластера уже находится в автономном режиме.


</dt> </dl> </dd> <dt>

<span id="ERROR_CLUSTER_NODE_ALREADY_MEMBER"></span><span id="error_cluster_node_already_member"></span>**\_узел кластера \_ ошибок \_ уже является \_ членом**
</dt> <dd> <dl> <dt>

5065 (0x13C9)
</dt> <dt>



Узел кластера уже является членом кластера.


</dt> </dl> </dd> <dt>

<span id="ERROR_CLUSTER_LAST_INTERNAL_NETWORK"></span><span id="error_cluster_last_internal_network"></span>**\_ \_ Последняя \_ Внутренняя сеть кластера \_ ошибок**
</dt> <dd> <dl> <dt>

5066 (0x13CA)
</dt> <dt>



Только сеть кластера настроена для внутреннего взаимодействия между двумя или более активными узлами кластера. Возможность внутренней связи не может быть удалена из сети.


</dt> </dl> </dd> <dt>

<span id="ERROR_CLUSTER_NETWORK_HAS_DEPENDENTS"></span><span id="error_cluster_network_has_dependents"></span>**Ошибка \_ \_ сеть кластера \_ \_ зависит от**
</dt> <dd> <dl> <dt>

5067 (0x13CB)
</dt> <dt>



Один или несколько ресурсов кластера зависят от сети для предоставления клиентам услуг. Возможность клиентского доступа не может быть удалена из сети.


</dt> </dl> </dd> <dt>

<span id="ERROR_INVALID_OPERATION_ON_QUORUM"></span><span id="error_invalid_operation_on_quorum"></span>**Ошибка \_ недопустимой \_ операции \_ с \_ кворумом**
</dt> <dd> <dl> <dt>

5068 (0x13CC)
</dt> <dt>



Эта операция не может быть выполнена для ресурса кластера, так как он является ресурсом кворума. Вы не можете перевести ресурс кворума в автономный режим или изменить список возможных владельцев.


</dt> </dl> </dd> <dt>

<span id="ERROR_DEPENDENCY_NOT_ALLOWED"></span><span id="error_dependency_not_allowed"></span>**\_зависимость ошибок \_ не \_ разрешена**
</dt> <dd> <dl> <dt>

5069 (0x13CD)
</dt> <dt>



Ресурс кворума кластера не может иметь никаких зависимостей.


</dt> </dl> </dd> <dt>

<span id="ERROR_CLUSTER_NODE_PAUSED"></span><span id="error_cluster_node_paused"></span>**Ошибка \_ при \_ \_ остановке узла кластера**
</dt> <dd> <dl> <dt>

5070 (0x13CE)
</dt> <dt>



Узел кластера приостановлен.


</dt> </dl> </dd> <dt>

<span id="ERROR_NODE_CANT_HOST_RESOURCE"></span><span id="error_node_cant_host_resource"></span>**узел ошибки не \_ \_ удается \_ разместить \_ ресурс**
</dt> <dd> <dl> <dt>

5071 (0x13CF)
</dt> <dt>



Не удается перевести ресурс кластера в режим "в сети". Узлу владельца не удается запустить этот ресурс.


</dt> </dl> </dd> <dt>

<span id="ERROR_CLUSTER_NODE_NOT_READY"></span><span id="error_cluster_node_not_ready"></span>**\_узел кластера \_ ошибок \_ не \_ готов**
</dt> <dd> <dl> <dt>

5072 (0x13D0)
</dt> <dt>



Узел кластера не готов к выполнению запрошенной операции.


</dt> </dl> </dd> <dt>

<span id="ERROR_CLUSTER_NODE_SHUTTING_DOWN"></span><span id="error_cluster_node_shutting_down"></span>**Ошибка \_ при \_ \_ завершении работы узла кластера \_**
</dt> <dd> <dl> <dt>

5073 (0x13D1)
</dt> <dt>



Узел кластера завершает работу.


</dt> </dl> </dd> <dt>

<span id="ERROR_CLUSTER_JOIN_ABORTED"></span><span id="error_cluster_join_aborted"></span>**Ошибка \_ при \_ присоединении к кластеру \_**
</dt> <dd> <dl> <dt>

5074 (0x13D2)
</dt> <dt>



Операция присоединение к кластеру прервана.


</dt> </dl> </dd> <dt>

<span id="ERROR_CLUSTER_INCOMPATIBLE_VERSIONS"></span><span id="error_cluster_incompatible_versions"></span>**\_ \_ несовместимые версии кластера с ошибками \_**
</dt> <dd> <dl> <dt>

5075 (0x13D3)
</dt> <dt>



Сбой операции присоединения к кластеру из-за несовместимых версий программного обеспечения между соединяемым узлом и его спонсором.


</dt> </dl> </dd> <dt>

<span id="ERROR_CLUSTER_MAXNUM_OF_RESOURCES_EXCEEDED"></span><span id="error_cluster_maxnum_of_resources_exceeded"></span>**\_ \_ превышено МАКСНУМ кластера ошибок \_ для \_ ресурсов \_**
</dt> <dd> <dl> <dt>

5076 (0x13D4)
</dt> <dt>



Невозможно создать этот ресурс, так как в кластере достигнуто ограничение на количество ресурсов, которое он может отслеживать.


</dt> </dl> </dd> <dt>

<span id="ERROR_CLUSTER_SYSTEM_CONFIG_CHANGED"></span><span id="error_cluster_system_config_changed"></span>**Ошибка \_ при \_ \_ изменении конфигурации \_ системы кластера**
</dt> <dd> <dl> <dt>

5077 (0x13D5)
</dt> <dt>



Конфигурация системы изменилась во время выполнения операции присоединением к кластеру или формой. Операция объединения или формы прервана.


</dt> </dl> </dd> <dt>

<span id="ERROR_CLUSTER_RESOURCE_TYPE_NOT_FOUND"></span><span id="error_cluster_resource_type_not_found"></span>**\_ \_ тип ресурса кластера \_ ошибок \_ не \_ найден**
</dt> <dd> <dl> <dt>

5078 (0x13D6)
</dt> <dt>



Указанный тип ресурса не найден.


</dt> </dl> </dd> <dt>

<span id="ERROR_CLUSTER_RESTYPE_NOT_SUPPORTED"></span><span id="error_cluster_restype_not_supported"></span>**Ошибка \_ кластера \_ рестипе \_ не \_ поддерживается**
</dt> <dd> <dl> <dt>

5079 (0x13D7)
</dt> <dt>



Указанный узел не поддерживает ресурс этого типа. Это может быть вызвано несоответствием версий или отсутствием DLL-библиотеки ресурсов на этом узле.


</dt> </dl> </dd> <dt>

<span id="ERROR_CLUSTER_RESNAME_NOT_FOUND"></span><span id="error_cluster_resname_not_found"></span>**Ошибка \_ кластера \_ реснаме \_ не \_ найдена**
</dt> <dd> <dl> <dt>

5080 (0x13D8)
</dt> <dt>



Указанное имя ресурса не поддерживается этой БИБЛИОТЕКой ресурсов. Это может быть вызвано неправильным (или измененным) именем, переданным в БИБЛИОТЕКУ ресурсов.


</dt> </dl> </dd> <dt>

<span id="ERROR_CLUSTER_NO_RPC_PACKAGES_REGISTERED"></span><span id="error_cluster_no_rpc_packages_registered"></span>**\_кластер ошибок \_ не \_ \_ \_ зарегистрированы пакеты RPC**
</dt> <dd> <dl> <dt>

5081 (0x13D9)
</dt> <dt>



Не удалось зарегистрировать пакет проверки подлинности на сервере RPC.


</dt> </dl> </dd> <dt>

<span id="ERROR_CLUSTER_OWNER_NOT_IN_PREFLIST"></span><span id="error_cluster_owner_not_in_preflist"></span>**Ошибка \_ владельца кластера, \_ \_ не \_ \_ префлист**
</dt> <dd> <dl> <dt>

5082 (0x13DA)
</dt> <dt>



Невозможно перевести группу в режим «в сети», так как владелец группы не находится в списке предпочтительных для группы. Чтобы изменить узел владельца для группы, переместите группу.


</dt> </dl> </dd> <dt>

<span id="ERROR_CLUSTER_DATABASE_SEQMISMATCH"></span><span id="error_cluster_database_seqmismatch"></span>**Ошибка \_ при \_ секмисматч базы данных кластера \_**
</dt> <dd> <dl> <dt>

5083 (0x13DB)
</dt> <dt>



Не удалось выполнить операцию JOIN, так как порядковый номер базы данных кластера изменился или несовместим с узлом-блокировкой. Это может произойти во время операции объединения, если база данных кластера была изменена во время объединения.


</dt> </dl> </dd> <dt>

<span id="ERROR_RESMON_INVALID_STATE"></span><span id="error_resmon_invalid_state"></span>**Ошибка \_ ресмон \_ недопустимое \_ состояние**
</dt> <dd> <dl> <dt>

5084 (0x13DC)
</dt> <dt>



Монитор ресурсов не позволит выполнить операцию сбоя, пока ресурс находится в текущем состоянии. Это может произойти, если ресурс находится в состоянии ожидания.


</dt> </dl> </dd> <dt>

<span id="ERROR_CLUSTER_GUM_NOT_LOCKER"></span><span id="error_cluster_gum_not_locker"></span>**Ошибка \_ кластера \_ переполняется \_ не является \_ блокировкой**
</dt> <dd> <dl> <dt>

5085 (0x13DD)
</dt> <dt>



Код, не являющийся блокировкой, получил запрос на резервирование блокировки для выполнения глобальных обновлений.


</dt> </dl> </dd> <dt>

<span id="ERROR_QUORUM_DISK_NOT_FOUND"></span><span id="error_quorum_disk_not_found"></span>**\_диск кворума ошибок \_ \_ не \_ найден**
</dt> <dd> <dl> <dt>

5086 (0x13DE)
</dt> <dt>



Не удалось найти диск кворума службой кластеров.


</dt> </dl> </dd> <dt>

<span id="ERROR_DATABASE_BACKUP_CORRUPT"></span><span id="error_database_backup_corrupt"></span>**Ошибка \_ \_ резервного копирования базы данных \_**
</dt> <dd> <dl> <dt>

5087 (0x13DF)
</dt> <dt>



Возможно, повреждена резервная копия базы данных кластера.


</dt> </dl> </dd> <dt>

<span id="ERROR_CLUSTER_NODE_ALREADY_HAS_DFS_ROOT"></span><span id="error_cluster_node_already_has_dfs_root"></span>**\_узел кластера \_ ошибок \_ уже \_ имеет \_ \_ корень DFS**
</dt> <dd> <dl> <dt>

5088 (0x13E0)
</dt> <dt>



Корень DFS уже существует на этом узле кластера.


</dt> </dl> </dd> <dt>

<span id="ERROR_RESOURCE_PROPERTY_UNCHANGEABLE"></span><span id="error_resource_property_unchangeable"></span>**\_ \_ неизменяемое свойство ресурса ошибки \_**
</dt> <dd> <dl> <dt>

5089 (0x13E1)
</dt> <dt>



Сбой при изменении свойства ресурса, так как он конфликтует с другим существующим свойством.


</dt> </dl> </dd> <dt>

<span id="ERROR_CLUSTER_MEMBERSHIP_INVALID_STATE"></span><span id="error_cluster_membership_invalid_state"></span>**Ошибка \_ " \_ \_ недопустимое \_ состояние членства в кластере"**
</dt> <dd> <dl> <dt>

5890 (0x1702)
</dt> <dt>



Предпринята попытка выполнить операцию, которая несовместима с текущим состоянием членства узла.


</dt> </dl> </dd> <dt>

<span id="ERROR_CLUSTER_QUORUMLOG_NOT_FOUND"></span><span id="error_cluster_quorumlog_not_found"></span>**Ошибка \_ кластера \_ куорумлог \_ не \_ найдена**
</dt> <dd> <dl> <dt>

5891 (0x1703)
</dt> <dt>



Ресурс кворума не содержит журнал кворума.


</dt> </dl> </dd> <dt>

<span id="ERROR_CLUSTER_MEMBERSHIP_HALT"></span><span id="error_cluster_membership_halt"></span>**Ошибка \_ при \_ остановке членства в кластере \_**
</dt> <dd> <dl> <dt>

5892 (0x1704)
</dt> <dt>



Подсистема членства запросила завершение работы службы кластеров на этом узле.


</dt> </dl> </dd> <dt>

<span id="ERROR_CLUSTER_INSTANCE_ID_MISMATCH"></span><span id="error_cluster_instance_id_mismatch"></span>**Ошибка \_ при \_ \_ несоответствии идентификатора экземпляра кластера \_**
</dt> <dd> <dl> <dt>

5893 (0x1705)
</dt> <dt>



Не удалось выполнить операцию соединения, так как идентификатор экземпляра кластера присоединенного узла не совпадает с ИДЕНТИФИКАТОРом экземпляра кластера спонсорского узла.


</dt> </dl> </dd> <dt>

<span id="ERROR_CLUSTER_NETWORK_NOT_FOUND_FOR_IP"></span><span id="error_cluster_network_not_found_for_ip"></span>**\_ \_ \_ \_ \_ для \_ IP-адреса не найдена сеть кластера с ошибками**
</dt> <dd> <dl> <dt>

5894 (0x1706)
</dt> <dt>



Не удалось найти соответствующую сеть кластера для указанного IP-адреса.


</dt> </dl> </dd> <dt>

<span id="ERROR_CLUSTER_PROPERTY_DATA_TYPE_MISMATCH"></span><span id="error_cluster_property_data_type_mismatch"></span>**\_несоответствие \_ \_ типов данных \_ свойства \_ кластера ошибок**
</dt> <dd> <dl> <dt>

5895 (0x1707)
</dt> <dt>



Фактический тип данных свойства не соответствует ожидаемому типу данных свойства.


</dt> </dl> </dd> <dt>

<span id="ERROR_CLUSTER_EVICT_WITHOUT_CLEANUP"></span><span id="error_cluster_evict_without_cleanup"></span>**\_кластер ошибок \_ исключить \_ без \_ очистки**
</dt> <dd> <dl> <dt>

5896 (0x1708)
</dt> <dt>



Узел кластера успешно удален из кластера, но узел не был очищен. Чтобы определить, какие шаги очистки завершились сбоем и как выполнить восстановление, просмотрите журнал событий приложения отказоустойчивой кластеризации с помощью Просмотр событий.


</dt> </dl> </dd> <dt>

<span id="ERROR_CLUSTER_PARAMETER_MISMATCH"></span><span id="error_cluster_parameter_mismatch"></span>**Ошибка \_ при \_ \_ несоответствии параметров кластера**
</dt> <dd> <dl> <dt>

5897 (0x1709)
</dt> <dt>



Два или более значений параметров, указанных для свойств ресурса, конфликтуют.


</dt> </dl> </dd> <dt>

<span id="ERROR_NODE_CANNOT_BE_CLUSTERED"></span><span id="error_node_cannot_be_clustered"></span>**\_узел ошибки \_ не может \_ быть \_ кластеризованным**
</dt> <dd> <dl> <dt>

5898 (0x170A)
</dt> <dt>



Этот компьютер невозможно сделать членом кластера.


</dt> </dl> </dd> <dt>

<span id="ERROR_CLUSTER_WRONG_OS_VERSION"></span><span id="error_cluster_wrong_os_version"></span>**Ошибка \_ кластера \_ неправильной \_ \_ версии ОС**
</dt> <dd> <dl> <dt>

5899 (0x170B)
</dt> <dt>



Этот компьютер невозможно сделать членом кластера, так как на нем не установлена правильная версия Windows.


</dt> </dl> </dd> <dt>

<span id="ERROR_CLUSTER_CANT_CREATE_DUP_CLUSTER_NAME"></span><span id="error_cluster_cant_create_dup_cluster_name"></span>**кластер ошибок не \_ \_ удается \_ создать \_ \_ имя кластера DUP \_**
</dt> <dd> <dl> <dt>

5900 (0x170C)
</dt> <dt>



Невозможно создать кластер с указанным именем кластера, так как это имя кластера уже используется. Укажите другое имя для кластера.


</dt> </dl> </dd> <dt>

<span id="ERROR_CLUSCFG_ALREADY_COMMITTED"></span><span id="error_cluscfg_already_committed"></span>**Ошибка \_ клускфг \_ уже \_ зафиксирована**
</dt> <dd> <dl> <dt>

5901 (0x170D)
</dt> <dt>



Действие конфигурации кластера уже зафиксировано.


</dt> </dl> </dd> <dt>

<span id="ERROR_CLUSCFG_ROLLBACK_FAILED"></span><span id="error_cluscfg_rollback_failed"></span>**Ошибка \_ \_ при откате клускфг \_**
</dt> <dd> <dl> <dt>

5902 (0x170E)
</dt> <dt>



Не удалось выполнить откат действия конфигурации кластера.


</dt> </dl> </dd> <dt>

<span id="ERROR_CLUSCFG_SYSTEM_DISK_DRIVE_LETTER_CONFLICT"></span><span id="error_cluscfg_system_disk_drive_letter_conflict"></span>**Ошибка \_ клускфг \_ . \_ \_ \_ \_ конфликт букв диска системного диска**
</dt> <dd> <dl> <dt>

5903 (0x170F)
</dt> <dt>



Буква диска, назначенная системному диску на одном узле, конфликтует с буквой диска, назначенной диску на другом узле.


</dt> </dl> </dd> <dt>

<span id="ERROR_CLUSTER_OLD_VERSION"></span><span id="error_cluster_old_version"></span>**\_ \_ старая версия кластера \_ ошибок**
</dt> <dd> <dl> <dt>

5904 (0x1710)
</dt> <dt>



Один или несколько узлов в кластере работают под управлением версии Windows, которая не поддерживает эту операцию.


</dt> </dl> </dd> <dt>

<span id="ERROR_CLUSTER_MISMATCHED_COMPUTER_ACCT_NAME"></span><span id="error_cluster_mismatched_computer_acct_name"></span>**Ошибка \_ \_ несоответствие \_ имени учетной ошибки компьютера кластера \_ \_**
</dt> <dd> <dl> <dt>

5905 (0x1711)
</dt> <dt>



Имя соответствующей учетной записи компьютера не соответствует сетевому имени для этого ресурса.


</dt> </dl> </dd> <dt>

<span id="ERROR_CLUSTER_NO_NET_ADAPTERS"></span><span id="error_cluster_no_net_adapters"></span>**\_кластер ошибок \_ нет \_ сетевых \_ адаптеров**
</dt> <dd> <dl> <dt>

5906 (0x1712)
</dt> <dt>



Нет доступных сетевых адаптеров.


</dt> </dl> </dd> <dt>

<span id="ERROR_CLUSTER_POISONED"></span><span id="error_cluster_poisoned"></span>**\_кластер ошибок \_ поврежден**
</dt> <dd> <dl> <dt>

5907 (0x1713)
</dt> <dt>



Узел кластера поврежден.


</dt> </dl> </dd> <dt>

<span id="ERROR_CLUSTER_GROUP_MOVING"></span><span id="error_cluster_group_moving"></span>**Ошибка \_ при \_ перемещении группы кластеров \_**
</dt> <dd> <dl> <dt>

5908 (0x1714)
</dt> <dt>



Группе не удалось принять запрос, так как он перемещается на другой узел.


</dt> </dl> </dd> <dt>

<span id="ERROR_CLUSTER_RESOURCE_TYPE_BUSY"></span><span id="error_cluster_resource_type_busy"></span>**\_ \_ тип ресурса кластера \_ ошибок \_ занят**
</dt> <dd> <dl> <dt>

5909 (0x1715)
</dt> <dt>



Тип ресурса не может принять запрос, так как он слишком занят выполнением другой операции.


</dt> </dl> </dd> <dt>

<span id="ERROR_RESOURCE_CALL_TIMED_OUT"></span><span id="error_resource_call_timed_out"></span>**\_ \_ \_ истекло время ожидания при ВЫЗОВЕ ресурса при ошибке \_**
</dt> <dd> <dl> <dt>

5910 (0x1716)
</dt> <dt>



Истекло время ожидания вызова библиотеки DLL ресурсов кластера.


</dt> </dl> </dd> <dt>

<span id="ERROR_INVALID_CLUSTER_IPV6_ADDRESS"></span><span id="error_invalid_cluster_ipv6_address"></span>**Ошибка \_ недопустимого \_ \_ IPv6- \_ адреса кластера**
</dt> <dd> <dl> <dt>

5911 (0x1717)
</dt> <dt>



Недопустимый адрес для ресурса IPv6-адреса. Требуется глобальный IPv6-адрес, который должен соответствовать сети кластера. Адреса совместимости запрещены.


</dt> </dl> </dd> <dt>

<span id="ERROR_CLUSTER_INTERNAL_INVALID_FUNCTION"></span><span id="error_cluster_internal_invalid_function"></span>**Ошибка \_ при \_ внутренней \_ недопустимой \_ функции кластера**
</dt> <dd> <dl> <dt>

5912 (0x1718)
</dt> <dt>



Произошла внутренняя ошибка кластера. Предпринята попытка вызова недопустимой функции.


</dt> </dl> </dd> <dt>

<span id="ERROR_CLUSTER_PARAMETER_OUT_OF_BOUNDS"></span><span id="error_cluster_parameter_out_of_bounds"></span>**\_параметр кластера ошибок вне допустимых \_ \_ \_ \_ границ**
</dt> <dd> <dl> <dt>

5913 (0x1719)
</dt> <dt>



Значение параметра выходит за пределы допустимого диапазона.


</dt> </dl> </dd> <dt>

<span id="ERROR_CLUSTER_PARTIAL_SEND"></span><span id="error_cluster_partial_send"></span>**Ошибка \_ \_ частичной \_ отправки кластера**
</dt> <dd> <dl> <dt>

5914 (0x171A)
</dt> <dt>



Произошла сетевая ошибка при отправке данных на другой узел в кластере. Количество переданных байтов было меньше, чем требовалось.


</dt> </dl> </dd> <dt>

<span id="ERROR_CLUSTER_REGISTRY_INVALID_FUNCTION"></span><span id="error_cluster_registry_invalid_function"></span>**Ошибка \_ \_ \_ недопустимая функция реестра кластера \_**
</dt> <dd> <dl> <dt>

5915 (0x171B)
</dt> <dt>



Предпринята попытка выполнить недопустимую операцию реестра кластера.


</dt> </dl> </dd> <dt>

<span id="ERROR_CLUSTER_INVALID_STRING_TERMINATION"></span><span id="error_cluster_invalid_string_termination"></span>**кластер ошибок " \_ \_ недопустимое \_ \_ Завершение строки"**
</dt> <dd> <dl> <dt>

5916 (0x171C)
</dt> <dt>



Входная строка символов не завершена должным образом.


</dt> </dl> </dd> <dt>

<span id="ERROR_CLUSTER_INVALID_STRING_FORMAT"></span><span id="error_cluster_invalid_string_format"></span>**\_ \_ Недопустимый \_ Формат строки кластера ошибок \_**
</dt> <dd> <dl> <dt>

5917 (0x171D)
</dt> <dt>



Входная строка символов имеет недопустимый формат для данных, которые он представляет.


</dt> </dl> </dd> <dt>

<span id="ERROR_CLUSTER_DATABASE_TRANSACTION_IN_PROGRESS"></span><span id="error_cluster_database_transaction_in_progress"></span>**Ошибка \_ \_ \_ \_ при выполнении транзакции базы данных кластера \_**
</dt> <dd> <dl> <dt>

5918 (0x171E)
</dt> <dt>



Произошла внутренняя ошибка кластера. Предпринята попытка транзакции базы данных кластера, пока транзакция уже выполняется.


</dt> </dl> </dd> <dt>

<span id="ERROR_CLUSTER_DATABASE_TRANSACTION_NOT_IN_PROGRESS"></span><span id="error_cluster_database_transaction_not_in_progress"></span>**Ошибка \_ \_ \_ \_ \_ при \_ выполнении транзакции базы данных кластера**
</dt> <dd> <dl> <dt>

5919 (0x171F)
</dt> <dt>



Произошла внутренняя ошибка кластера. Предпринята попытка зафиксировать транзакцию базы данных кластера, пока не выполнялась транзакция.


</dt> </dl> </dd> <dt>

<span id="ERROR_CLUSTER_NULL_DATA"></span><span id="error_cluster_null_data"></span>**Ошибка в \_ кластере \_ \_ данных null**
</dt> <dd> <dl> <dt>

5920 (0x1720)
</dt> <dt>



Произошла внутренняя ошибка кластера. Данные не были должным образом инициализированы.


</dt> </dl> </dd> <dt>

<span id="ERROR_CLUSTER_PARTIAL_READ"></span><span id="error_cluster_partial_read"></span>**Ошибка \_ при \_ частичном \_ чтении кластера**
</dt> <dd> <dl> <dt>

5921 (0x1721)
</dt> <dt>



Произошла ошибка при чтении из потока данных. Возвращено непредвиденное число байтов.


</dt> </dl> </dd> <dt>

<span id="ERROR_CLUSTER_PARTIAL_WRITE"></span><span id="error_cluster_partial_write"></span>**Ошибка \_ \_ частичной записи в кластере \_**
</dt> <dd> <dl> <dt>

5922 (0x1722)
</dt> <dt>



Произошла ошибка при записи в поток данных. Не удалось записать требуемое число байтов.


</dt> </dl> </dd> <dt>

<span id="ERROR_CLUSTER_CANT_DESERIALIZE_DATA"></span><span id="error_cluster_cant_deserialize_data"></span>**кластер ошибок не \_ \_ удается \_ десериализовать \_ данные**
</dt> <dd> <dl> <dt>

5923 (0x1723)
</dt> <dt>



Произошла ошибка при десериализации потока данных кластера.


</dt> </dl> </dd> <dt>

<span id="ERROR_DEPENDENT_RESOURCE_PROPERTY_CONFLICT"></span><span id="error_dependent_resource_property_conflict"></span>**\_ \_ \_ конфликт свойств ресурса, ЗАВИСИМого от ошибки \_**
</dt> <dd> <dl> <dt>

5924 (0x1724)
</dt> <dt>



Одно или несколько значений свойств для этого ресурса конфликтуют с одним или несколькими значениями свойств, связанными с зависимыми ресурсами.


</dt> </dl> </dd> <dt>

<span id="ERROR_CLUSTER_NO_QUORUM"></span><span id="error_cluster_no_quorum"></span>**\_кластер ошибок \_ без \_ кворума**
</dt> <dd> <dl> <dt>

5925 (0x1725)
</dt> <dt>



Отсутствует кворум узлов кластера для формирования кластера.


</dt> </dl> </dd> <dt>

<span id="ERROR_CLUSTER_INVALID_IPV6_NETWORK"></span><span id="error_cluster_invalid_ipv6_network"></span>**\_Кластер ошибок \_ -Недопустимая \_ \_ сеть IPv6**
</dt> <dd> <dl> <dt>

5926 (0x1726)
</dt> <dt>



Сеть кластера недопустима для ресурса IPv6-адреса или не соответствует заданному адресу.


</dt> </dl> </dd> <dt>

<span id="ERROR_CLUSTER_INVALID_IPV6_TUNNEL_NETWORK"></span><span id="error_cluster_invalid_ipv6_tunnel_network"></span>**\_Кластер ошибок \_ Недопустимая \_ \_ туннельная \_ сеть IPv6**
</dt> <dd> <dl> <dt>

5927 (0x1727)
</dt> <dt>



Сеть кластера недопустима для ресурса туннеля IPv6. Проверьте конфигурацию ресурса IP-адреса, от которого зависит туннельный ресурс IPv6.


</dt> </dl> </dd> <dt>

<span id="ERROR_QUORUM_NOT_ALLOWED_IN_THIS_GROUP"></span><span id="error_quorum_not_allowed_in_this_group"></span>**\_ \_ \_ \_ в \_ этой \_ группе не допускается использование кворума "ошибка"**
</dt> <dd> <dl> <dt>

5928 (0x1728)
</dt> <dt>



Ресурс кворума не может находиться в доступной группе хранения.


</dt> </dl> </dd> <dt>

<span id="ERROR_DEPENDENCY_TREE_TOO_COMPLEX"></span><span id="error_dependency_tree_too_complex"></span>**\_дерево зависимостей \_ ошибок \_ слишком \_ сложное**
</dt> <dd> <dl> <dt>

5929 (0x1729)
</dt> <dt>



Зависимости для этого ресурса имеют слишком глубокий уровень вложенности.


</dt> </dl> </dd> <dt>

<span id="ERROR_EXCEPTION_IN_RESOURCE_CALL"></span><span id="error_exception_in_resource_call"></span>**Ошибка \_ исключения \_ в \_ \_ вызове ресурса**
</dt> <dd> <dl> <dt>

5930 (0x172A)
</dt> <dt>



Вызов библиотеки DLL ресурсов вызвал необработанное исключение.


</dt> </dl> </dd> <dt>

<span id="ERROR_CLUSTER_RHS_FAILED_INITIALIZATION"></span><span id="error_cluster_rhs_failed_initialization"></span>**Ошибка \_ \_ \_ при инициализации "сбой кластера RHS" \_**
</dt> <dd> <dl> <dt>

5931 (0x172B)
</dt> <dt>



Не удалось инициализировать процесс RHS.


</dt> </dl> </dd> <dt>

<span id="ERROR_CLUSTER_NOT_INSTALLED"></span><span id="error_cluster_not_installed"></span>**\_кластер ошибок \_ не \_ установлен**
</dt> <dd> <dl> <dt>

5932 (0x172C)
</dt> <dt>



Компонент отказоустойчивой кластеризации не установлен на этом узле.


</dt> </dl> </dd> <dt>

<span id="ERROR_CLUSTER_RESOURCES_MUST_BE_ONLINE_ON_THE_SAME_NODE"></span><span id="error_cluster_resources_must_be_online_on_the_same_node"></span>**\_ресурсы кластера \_ ошибок \_ должны \_ находиться \_ в \_ сети \_ на \_ одном \_ узле**
</dt> <dd> <dl> <dt>

5933 (0x172D)
</dt> <dt>



Для этой операции ресурсы должны находиться в сети на одном узле.


</dt> </dl> </dd> <dt>

<span id="ERROR_CLUSTER_MAX_NODES_IN_CLUSTER"></span><span id="error_cluster_max_nodes_in_cluster"></span>**\_ \_ Максимальное количество узлов кластера с ошибками \_ \_ в \_ кластере**
</dt> <dd> <dl> <dt>

5934 (0x172E)
</dt> <dt>



Невозможно добавить новый узел, так как этот кластер уже находится на максимальном количестве узлов.


</dt> </dl> </dd> <dt>

<span id="ERROR_CLUSTER_TOO_MANY_NODES"></span><span id="error_cluster_too_many_nodes"></span>**Ошибка \_ кластера \_ слишком \_ большого количества \_ узлов**
</dt> <dd> <dl> <dt>

5935 (0x172F)
</dt> <dt>



Невозможно создать этот кластер, так как указанное число узлов превышает максимально допустимое значение.


</dt> </dl> </dd> <dt>

<span id="ERROR_CLUSTER_OBJECT_ALREADY_USED"></span><span id="error_cluster_object_already_used"></span>**\_объект кластера \_ ошибок \_ уже \_ используется**
</dt> <dd> <dl> <dt>

5936 (0x1730)
</dt> <dt>



Попытка использовать указанное имя кластера завершилась сбоем, так как в домене уже существует включенный объект компьютера с данным именем.


</dt> </dl> </dd> <dt>

<span id="ERROR_NONCORE_GROUPS_FOUND"></span><span id="error_noncore_groups_found"></span>**\_ \_ обнаружены неключевые группы ошибок \_**
</dt> <dd> <dl> <dt>

5937 (0x1731)
</dt> <dt>



Этот кластер не может быть уничтожен. Она содержит неосновные группы приложений, которые необходимо удалить перед уничтожением кластера.


</dt> </dl> </dd> <dt>

<span id="ERROR_FILE_SHARE_RESOURCE_CONFLICT"></span><span id="error_file_share_resource_conflict"></span>**Ошибка \_ при \_ \_ конфликте ресурсов общего файлового ресурса \_**
</dt> <dd> <dl> <dt>

5938 (0x1732)
</dt> <dt>



Общая папка, связанная с ресурсом-свидетелем файлового ресурса, не может размещаться в этом кластере или на любом из его узлов.


</dt> </dl> </dd> <dt>

<span id="ERROR_CLUSTER_EVICT_INVALID_REQUEST"></span><span id="error_cluster_evict_invalid_request"></span>**кластер ошибок " \_ \_ исключить \_ Недопустимый \_ запрос"**
</dt> <dd> <dl> <dt>

5939 (0x1733)
</dt> <dt>



В данный момент вытеснение этого узла недопустимо. Из-за превышения требований к кворуму операция вытеснения узла приведет к завершению работы кластера. Если это последний узел в кластере, следует использовать команду уничтожения кластера.


</dt> </dl> </dd> <dt>

<span id="ERROR_CLUSTER_SINGLETON_RESOURCE"></span><span id="error_cluster_singleton_resource"></span>**Ошибка \_ \_ SINGLETON — \_ ресурс кластера**
</dt> <dd> <dl> <dt>

5940 (0x1734)
</dt> <dt>



В кластере допускается только один экземпляр этого типа ресурсов.


</dt> </dl> </dd> <dt>

<span id="ERROR_CLUSTER_GROUP_SINGLETON_RESOURCE"></span><span id="error_cluster_group_singleton_resource"></span>**Ошибка \_ \_ \_ одноэлементного \_ ресурса группы кластера**
</dt> <dd> <dl> <dt>

5941 (0x1735)
</dt> <dt>



Для каждой группы ресурсов допускается только один экземпляр этого типа ресурса.


</dt> </dl> </dd> <dt>

<span id="ERROR_CLUSTER_RESOURCE_PROVIDER_FAILED"></span><span id="error_cluster_resource_provider_failed"></span>**Ошибка \_ \_ \_ \_ при попытке поставщика ресурсов кластера**
</dt> <dd> <dl> <dt>

5942 (0x1736)
</dt> <dt>



Не удалось перевести ресурс в режим "в сети" из-за сбоя одного или нескольких ресурсов поставщика.


</dt> </dl> </dd> <dt>

<span id="ERROR_CLUSTER_RESOURCE_CONFIGURATION_ERROR"></span><span id="error_cluster_resource_configuration_error"></span>**Ошибка \_ \_ конфигурации ресурса \_ кластера \_ ошибок**
</dt> <dd> <dl> <dt>

5943 (0x1737)
</dt> <dt>



Ресурс указал, что он не может быть подключен к сети на любом узле.


</dt> </dl> </dd> <dt>

<span id="ERROR_CLUSTER_GROUP_BUSY"></span><span id="error_cluster_group_busy"></span>**Группа "ошибка \_ кластера \_ \_ занята"**
</dt> <dd> <dl> <dt>

5944 (0x1738)
</dt> <dt>



В настоящее время невозможно выполнить текущую операцию в этой группе.


</dt> </dl> </dd> <dt>

<span id="ERROR_CLUSTER_NOT_SHARED_VOLUME"></span><span id="error_cluster_not_shared_volume"></span>**\_кластер ошибок \_ не является \_ общим \_ томом**
</dt> <dd> <dl> <dt>

5945 (0x1739)
</dt> <dt>



Каталог или файл не расположены на общем томе кластера.


</dt> </dl> </dd> <dt>

<span id="ERROR_CLUSTER_INVALID_SECURITY_DESCRIPTOR"></span><span id="error_cluster_invalid_security_descriptor"></span>**\_ \_ Недопустимый \_ дескриптор безопасности кластера ошибок \_**
</dt> <dd> <dl> <dt>

5946 (0x173A)
</dt> <dt>



Дескриптор безопасности не отвечает требованиям кластера.


</dt> </dl> </dd> <dt>

<span id="ERROR_CLUSTER_SHARED_VOLUMES_IN_USE"></span><span id="error_cluster_shared_volumes_in_use"></span>**\_ \_ Общие тома кластера \_ ошибок \_ \_ используются**
</dt> <dd> <dl> <dt>

5947 (0x173B)
</dt> <dt>



В кластере настроен один или несколько ресурсов общих томов. Эти ресурсы необходимо переместить в Доступное хранилище, чтобы обеспечить успешную работу.


</dt> </dl> </dd> <dt>

<span id="ERROR_CLUSTER_USE_SHARED_VOLUMES_API"></span><span id="error_cluster_use_shared_volumes_api"></span>**\_ \_ использование \_ \_ API общих ТОМОВ \_ в кластере ошибок**
</dt> <dd> <dl> <dt>

5948 (0x173C)
</dt> <dt>



Этой группе или ресурсу нельзя управлять напрямую. Используйте интерфейсы API общего тома для выполнения требуемой операции.


</dt> </dl> </dd> <dt>

<span id="ERROR_CLUSTER_BACKUP_IN_PROGRESS"></span><span id="error_cluster_backup_in_progress"></span>**\_ \_ выполняется резервное копирование кластера \_ ошибок \_**
</dt> <dd> <dl> <dt>

5949 (0x173D)
</dt> <dt>



Выполняется резервное копирование. Перед повторным выполнением этой операции дождитесь завершения резервного копирования.


</dt> </dl> </dd> <dt>

<span id="ERROR_NON_CSV_PATH"></span><span id="error_non_csv_path"></span>**Ошибка \_ не \_ CSV- \_ путь**
</dt> <dd> <dl> <dt>

5950 (0x173E)
</dt> <dt>



Путь не принадлежит к общему тому кластера.


</dt> </dl> </dd> <dt>

<span id="ERROR_CSV_VOLUME_NOT_LOCAL"></span><span id="error_csv_volume_not_local"></span>**Ошибка \_ тома CSV, \_ \_ не \_ локального**
</dt> <dd> <dl> <dt>

5951 (0x173F)
</dt> <dt>



Общий том кластера не подключен к этому узлу локально.


</dt> </dl> </dd> <dt>

<span id="ERROR_CLUSTER_WATCHDOG_TERMINATING"></span><span id="error_cluster_watchdog_terminating"></span>**Ошибка \_ при \_ прерывании наблюдения за кластером \_**
</dt> <dd> <dl> <dt>

5952 (0x1740)
</dt> <dt>



Модуль наблюдения за кластером завершает работу.


</dt> </dl> </dd> <dt>

<span id="ERROR_CLUSTER_RESOURCE_VETOED_MOVE_INCOMPATIBLE_NODES"></span><span id="error_cluster_resource_vetoed_move_incompatible_nodes"></span>**Ошибка \_ ресурс кластера с \_ \_ ЗАПРЕТом \_ перемещения \_ несовместимые \_ узлы**
</dt> <dd> <dl> <dt>

5953 (0x1741)
</dt> <dt>



Ресурс запретил перемещение между двумя узлами, так как они несовместимы.


</dt> </dl> </dd> <dt>

<span id="ERROR_CLUSTER_INVALID_NODE_WEIGHT"></span><span id="error_cluster_invalid_node_weight"></span>**\_ \_ Недопустимый \_ вес узла в кластере ошибок \_**
</dt> <dd> <dl> <dt>

5954 (0x1742)
</dt> <dt>



Запрос является недопустимым либо из-за того, что вес узла не может быть изменен, пока кластер находится в режиме кворума "только диск" или если изменение веса узла привело к нарушению минимальных требований кворума кластера.


</dt> </dl> </dd> <dt>

<span id="ERROR_CLUSTER_RESOURCE_VETOED_CALL"></span><span id="error_cluster_resource_vetoed_call"></span>**Ошибка \_ при \_ \_ \_ вызове незаблокированного ресурса кластера**
</dt> <dd> <dl> <dt>

5955 (0x1743)
</dt> <dt>



Ресурс запретил вызов.


</dt> </dl> </dd> <dt>

<span id="ERROR_RESMON_SYSTEM_RESOURCES_LACKING"></span><span id="error_resmon_system_resources_lacking"></span>**Ошибка \_ ресмон \_ . \_ \_ нехватка системных ресурсов**
</dt> <dd> <dl> <dt>

5956 (0x1744)
</dt> <dt>



Не удалось запустить или запустить ресурс, поскольку ему не удалось зарезервировать достаточные системные ресурсы.


</dt> </dl> </dd> <dt>

<span id="ERROR_CLUSTER_RESOURCE_VETOED_MOVE_NOT_ENOUGH_RESOURCES_ON_DESTINATION"></span><span id="error_cluster_resource_vetoed_move_not_enough_resources_on_destination"></span>**Ошибка \_ " \_ ресурс кластера \_ запрещен" \_ Перемещение \_ не \_ хватает \_ ресурсов \_ в \_ месте назначения**
</dt> <dd> <dl> <dt>

5957 (0x1745)
</dt> <dt>



Ресурс запретил перемещение между двумя узлами, так как в настоящее время в целевом объекте недостаточно ресурсов для завершения операции.


</dt> </dl> </dd> <dt>

<span id="ERROR_CLUSTER_RESOURCE_VETOED_MOVE_NOT_ENOUGH_RESOURCES_ON_SOURCE"></span><span id="error_cluster_resource_vetoed_move_not_enough_resources_on_source"></span>**Ошибка \_ " \_ ресурс кластера \_ запрещен" \_ Перемещение \_ не \_ хватает \_ ресурсов \_ в \_ источнике**
</dt> <dd> <dl> <dt>

5958 (0x1746)
</dt> <dt>



Ресурс запретил перемещение между двумя узлами, так как в настоящее время в источнике недостаточно ресурсов для завершения операции.


</dt> </dl> </dd> <dt>

<span id="ERROR_CLUSTER_GROUP_QUEUED"></span><span id="error_cluster_group_queued"></span>**\_Группа кластера \_ ошибок \_ в очереди**
</dt> <dd> <dl> <dt>

5959 (0x1747)
</dt> <dt>



Не удается выполнить запрошенную операцию, так как группа поставлена в очередь для операции.


</dt> </dl> </dd> <dt>

<span id="ERROR_CLUSTER_RESOURCE_LOCKED_STATUS"></span><span id="error_cluster_resource_locked_status"></span>**\_ \_ \_ состояние блокировки ресурса кластера \_ ошибок**
</dt> <dd> <dl> <dt>

5960 (0x1748)
</dt> <dt>



Запрошенная операция не может быть завершена, так как ресурс заблокирован.


</dt> </dl> </dd> <dt>

<span id="ERROR_CLUSTER_SHARED_VOLUME_FAILOVER_NOT_ALLOWED"></span><span id="error_cluster_shared_volume_failover_not_allowed"></span>**Ошибка \_ \_ \_ \_ отработки отказа общего тома кластера \_ не \_ разрешена**
</dt> <dd> <dl> <dt>

5961 (0x1749)
</dt> <dt>



Ресурс не может быть перемещен на другой узел, так как общий том кластера запретил операцию.


</dt> </dl> </dd> <dt>

<span id="ERROR_CLUSTER_NODE_DRAIN_IN_PROGRESS"></span><span id="error_cluster_node_drain_in_progress"></span>**Ошибка \_ \_ \_ \_ при выполнении очистки узла \_ кластера**
</dt> <dd> <dl> <dt>

5962 (0x174A)
</dt> <dt>



Очистка узла уже выполняется.

Это значение также называется " **Ошибка \_ \_ узла кластера \_ эвакуации \_ \_** "


</dt> </dl> </dd> <dt>

<span id="ERROR_CLUSTER_DISK_NOT_CONNECTED"></span><span id="error_cluster_disk_not_connected"></span>**Ошибка \_ " \_ диск кластера \_ не \_ подключен"**
</dt> <dd> <dl> <dt>

5963 (0x174B)
</dt> <dt>



Кластерное хранилище не подключено к узлу.


</dt> </dl> </dd> <dt>

<span id="ERROR_DISK_NOT_CSV_CAPABLE"></span><span id="error_disk_not_csv_capable"></span>**\_диск ошибок \_ не \_ \_ поддерживает CSV**
</dt> <dd> <dl> <dt>

5964 (0x174C)
</dt> <dt>



Диск не настроен таким образом, чтобы его можно было использовать с CSV. Диски CSV должны иметь по крайней мере один раздел, отформатированный с помощью NTFS.


</dt> </dl> </dd> <dt>

<span id="ERROR_RESOURCE_NOT_IN_AVAILABLE_STORAGE"></span><span id="error_resource_not_in_available_storage"></span>**\_ресурс ошибки \_ не \_ в \_ доступном \_ хранилище**
</dt> <dd> <dl> <dt>

5965 (0x174D)
</dt> <dt>



Для выполнения этого действия ресурс должен быть частью доступной группы хранения.


</dt> </dl> </dd> <dt>

<span id="ERROR_CLUSTER_SHARED_VOLUME_REDIRECTED"></span><span id="error_cluster_shared_volume_redirected"></span>**\_ \_ общий том кластера \_ ошибок \_ перенаправлен**
</dt> <dd> <dl> <dt>

5966 (0x174E)
</dt> <dt>



CSVFS не удалось выполнить операцию, так как том находится в перенаправленном режиме.


</dt> </dl> </dd> <dt>

<span id="ERROR_CLUSTER_SHARED_VOLUME_NOT_REDIRECTED"></span><span id="error_cluster_shared_volume_not_redirected"></span>**\_ \_ общий том кластера \_ ошибок \_ не \_ перенаправлен**
</dt> <dd> <dl> <dt>

5967 (0x174F)
</dt> <dt>



CSVFS не удалось выполнить операцию, так как том не находится в перенаправленном режиме.


</dt> </dl> </dd> <dt>

<span id="ERROR_CLUSTER_CANNOT_RETURN_PROPERTIES"></span><span id="error_cluster_cannot_return_properties"></span>**\_кластер ошибок \_ не может \_ возвращать \_ Свойства**
</dt> <dd> <dl> <dt>

5968 (0x1750)
</dt> <dt>



В настоящее время невозможно вернуть свойства кластера.


</dt> </dl> </dd> <dt>

<span id="ERROR_CLUSTER_RESOURCE_CONTAINS_UNSUPPORTED_DIFF_AREA_FOR_SHARED_VOLUMES"></span><span id="error_cluster_resource_contains_unsupported_diff_area_for_shared_volumes"></span>**\_ресурс кластера \_ ошибок \_ содержит \_ неподдерживаемую \_ \_ область копирования \_ для \_ общих \_ томов**
</dt> <dd> <dl> <dt>

5969 (0x1751)
</dt> <dt>



Ресурс "кластерный диск" содержит область копирования моментальных снимков программного обеспечения, которая не поддерживается для общих томов кластера.


</dt> </dl> </dd> <dt>

<span id="ERROR_CLUSTER_RESOURCE_IS_IN_MAINTENANCE_MODE"></span><span id="error_cluster_resource_is_in_maintenance_mode"></span>**Ошибка \_ \_ ресурса кластера \_ \_ в \_ режиме обслуживания \_**
</dt> <dd> <dl> <dt>

5970 (0x1752)
</dt> <dt>



Невозможно завершить операцию, так как ресурс находится в режиме обслуживания.


</dt> </dl> </dd> <dt>

<span id="ERROR_CLUSTER_AFFINITY_CONFLICT"></span><span id="error_cluster_affinity_conflict"></span>**Ошибка \_ при \_ конфликте сходства кластера \_**
</dt> <dd> <dl> <dt>

5971 (0x1753)
</dt> <dt>



Не удается завершить операцию из-за конфликтов сходства кластера.


</dt> </dl> </dd> <dt>

<span id="ERROR_CLUSTER_RESOURCE_IS_REPLICA_VIRTUAL_MACHINE"></span><span id="error_cluster_resource_is_replica_virtual_machine"></span>**\_ресурс кластера \_ ошибок \_ — \_ реплика \_ виртуальной \_ машины**
</dt> <dd> <dl> <dt>

5972 (0x1754)
</dt> <dt>



Невозможно выполнить операцию, так как ресурс является репликой виртуальной машины.


</dt> </dl> </dd> </dl>


## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Только для \[ классических приложений Windows XP\]<br/>                                           |
| Минимальная версия сервера<br/> | \[Только для настольных приложений Windows Server 2003\]<br/>                                  |
| Header<br/>                   | <dl> <dt>WinError. h</dt> </dl> |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[Коды системных ошибок](system-error-codes.md)
</dt> </dl>

 

 




