---
title: Значения ошибок регистрации MDM (Мдмрегистратион. h)
description: Следующие значения ошибок связаны с регистрацией MDM.
ms.assetid: 1f42ed5e-e221-47ec-a019-ed06c05d55d0
topic_type:
- apiref
api_name:
- E_DATATYPE_MISMATCH
- MREGISTER_E_DEVICE_MESSAGE_FORMAT_ERROR
- MENROLL_E_DEVICE_MESSAGE_FORMAT_ERROR
- MREGISTER_E_DEVICE_AUTHENTICATION_ERROR
- MENROLL_E_DEVICE_AUTHENTICATION_ERROR
- MREGISTER_E_DEVICE_AUTHORIZATION_ERROR
- MENROLL_E_DEVICE_AUTHORIZATION_ERROR
- MREGISTER_E_DEVICE_CERTIFCATEREQUEST_ERROR
- MENROLL_E_DEVICE_CERTIFCATEREQUEST_ERROR
- MREGISTER_E_DEVICE_CONFIGMGRSERVER_ERROR
- MENROLL_E_DEVICE_CONFIGMGRSERVER_ERROR
- MREGISTER_E_DEVICE_INTERNALSERVICE_ERROR
- MENROLL_E_DEVICE_INTERNALSERVICE_ERROR
- MREGISTER_E_DEVICE_INVALIDSECURITY_ERROR
- MENROLL_E_DEVICE_INVALIDSECURITY_ERROR
- MREGISTER_E_DEVICE_UNKNOWN_ERROR
- MENROLL_E_DEVICE_UNKNOWN_ERROR
- MREGISTER_E_REGISTRATION_IN_PROGRESS
- MENROLL_E_ENROLLMENT_IN_PROGRESS
- MREGISTER_E_DEVICE_ALREADY_REGISTERED
- MENROLL_E_DEVICE_ALREADY_ENROLLED
- MREGISTER_E_DEVICE_NOT_REGISTERED
- MENROLL_E_DEVICE_NOT_ENROLLED
- MREGISTER_E_DISCOVERY_REDIRECTED
- MREGISTER_E_DEVICE_NOT_AD_REGISTERED_ERROR
- MENROLL_E_DISCOVERY_SEC_CERT_DATE_INVALID
- MREGISTER_E_DISCOVERY_FAILED
- MENROLL_E_PASSWORD_NEEDED
- MENROLL_E_WAB_ERROR
- MENROLL_E_CONNECTIVITY
- MENROLL_S_ENROLLMENT_SUSPENDED
- MENROLL_E_INVALIDSSLCERT
- MENROLL_E_DEVICECAPREACHED
- MENROLL_E_DEVICENOTSUPPORTED
- MENROLL_E_NOTSUPPORTED
- MREGISTER_E_NOTELIGIBLETORENEW
- MENROLL_E_INMAINTENANCE
- MENROLL_E_USERLICENSE
- MENROLL_E_ENROLLMENTDATAINVALID
- MENROLL_E_INSECUREREDIRECT
- MENROLL_E_PLATFORM_WRONG_STATE
- MENROLL_E_PLATFORM_LICENSE_ERROR
- MENROLL_E_PLATFORM_UNKNOWN_ERROR
- MENROLL_E_PROV_CSP_CERTSTORE
- MENROLL_E_PROV_CSP_W7
- MENROLL_E_PROV_CSP_DMCLIENT
- MENROLL_E_PROV_CSP_PFW
- MENROLL_E_PROV_CSP_MISC
- MENROLL_E_PROV_UNKNOWN
- MENROLL_E_PROV_SSLCERTNOTFOUND
- MENROLL_E_PROV_CSP_APPMGMT
- MENROLL_E_DEVICE_MANAGEMENT_BLOCKED
- MENROLL_E_CERTPOLICY_PRIVATEKEYCREATION_FAILED
- MENROLL_E_CERTAUTH_FAILED_TO_FIND_CERT
- MENROLL_E_EMPTY_MESSAGE
- MENROLL_E_USER_CANCELED
- MENROLL_E_MDM_NOT_CONFIGURED
api_location:
- MDMRegistration.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: cb62977a48400866e9fa8829696c884e58e54325
ms.sourcegitcommit: f848119a8faa29b27585f4df53f6e50ee9666684
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 05/27/2021
ms.locfileid: "110548989"
---
# <a name="mdm-registration-error-values"></a>Значения ошибок регистрации MDM

Следующие значения ошибок связаны с регистрацией MDM.

<dl> <dt>

<span id="E_DATATYPE_MISMATCH"></span><span id="e_datatype_mismatch"></span>**\_несоответствие типов данных E \_**
</dt> <dd> <dl> <dt>

0x8007065d
</dt> <dt>



Тип данных не соответствует ожидаемому типу данных.


</dt> </dl> </dd> <dt>

<span id="MREGISTER_E_DEVICE_MESSAGE_FORMAT_ERROR"></span><span id="mregister_e_device_message_format_error"></span>**\_ \_ \_ \_ Ошибка формата сообщения устройства мрегистер E \_**
</dt> <dd> <dl> <dt>

0x80190001
</dt> <dt>



Недопустимая схема, ошибка формата сообщения от сервера.


</dt> </dl> </dd> <dt>

<span id="MENROLL_E_DEVICE_MESSAGE_FORMAT_ERROR"></span><span id="menroll_e_device_message_format_error"></span>**\_ \_ \_ \_ Ошибка формата сообщения устройства менролл E \_**
</dt> <dd> <dl> <dt>

0x80180001
</dt> <dt>



Недопустимая схема, ошибка формата сообщения от сервера.

**Windows 8.1:** Эта константа недоступна до Windows 10.


</dt> </dl> </dd> <dt>

<span id="MREGISTER_E_DEVICE_AUTHENTICATION_ERROR"></span><span id="mregister_e_device_authentication_error"></span>**\_ \_ \_ Ошибка проверки подлинности устройства мрегистер E \_**
</dt> <dd> <dl> <dt>

0x80190002
</dt> <dt>



Серверу не удалось проверить подлинность пользователя.


</dt> </dl> </dd> <dt>

<span id="MENROLL_E_DEVICE_AUTHENTICATION_ERROR"></span><span id="menroll_e_device_authentication_error"></span>**\_ \_ \_ Ошибка проверки подлинности устройства менролл E \_**
</dt> <dd> <dl> <dt>

0x80180002
</dt> <dt>



Серверу не удалось проверить подлинность пользователя.

**Windows 8.1:** Эта константа недоступна до Windows 10.


</dt> </dl> </dd> <dt>

<span id="MREGISTER_E_DEVICE_AUTHORIZATION_ERROR"></span><span id="mregister_e_device_authorization_error"></span>**\_ \_ \_ Ошибка авторизации устройства мрегистер \_ E**
</dt> <dd> <dl> <dt>

0x80190003
</dt> <dt>



У пользователя нет права на регистрацию.


</dt> </dl> </dd> <dt>

<span id="MENROLL_E_DEVICE_AUTHORIZATION_ERROR"></span><span id="menroll_e_device_authorization_error"></span>**\_ \_ \_ Ошибка авторизации устройства менролл \_ E**
</dt> <dd> <dl> <dt>

0x80180003
</dt> <dt>



У пользователя нет права на регистрацию.

**Windows 8.1:** Эта константа недоступна до Windows 10.


</dt> </dl> </dd> <dt>

<span id="MREGISTER_E_DEVICE_CERTIFCATEREQUEST_ERROR"></span><span id="mregister_e_device_certifcaterequest_error"></span>**\_ \_ Ошибка цертифкатерекуест для устройства мрегистер E \_ \_**
</dt> <dd> <dl> <dt>

0x80190004
</dt> <dt>



У пользователя нет разрешений на шаблон сертификата, или центр сертификации недоступен.


</dt> </dl> </dd> <dt>

<span id="MENROLL_E_DEVICE_CERTIFCATEREQUEST_ERROR"></span><span id="menroll_e_device_certifcaterequest_error"></span>**\_ \_ Ошибка цертифкатерекуест для устройства менролл E \_ \_**
</dt> <dd> <dl> <dt>

0x80180004
</dt> <dt>



У пользователя нет разрешений на шаблон сертификата, или центр сертификации недоступен.

**Windows 8.1:** Эта константа недоступна до Windows 10.


</dt> </dl> </dd> <dt>

<span id="MREGISTER_E_DEVICE_CONFIGMGRSERVER_ERROR"></span><span id="mregister_e_device_configmgrserver_error"></span>**\_ \_ Ошибка конфигмгрсервер для устройства мрегистер E \_ \_**
</dt> <dd> <dl> <dt>

0x80190005
</dt> <dt>



Произошел сбой на сервере управления, например ошибка доступа к базе данных.


</dt> </dl> </dd> <dt>

<span id="MENROLL_E_DEVICE_CONFIGMGRSERVER_ERROR"></span><span id="menroll_e_device_configmgrserver_error"></span>**\_ \_ Ошибка конфигмгрсервер для устройства менролл E \_ \_**
</dt> <dd> <dl> <dt>

0x80180005
</dt> <dt>



Произошел сбой на сервере управления, например ошибка доступа к базе данных.

**Windows 8.1:** Эта константа недоступна до Windows 10.


</dt> </dl> </dd> <dt>

<span id="MREGISTER_E_DEVICE_INTERNALSERVICE_ERROR"></span><span id="mregister_e_device_internalservice_error"></span>**\_ \_ Ошибка интерналсервице для устройства мрегистер E \_ \_**
</dt> <dd> <dl> <dt>

0x80190006
</dt> <dt>



На сервере возникло необработанное исключение.


</dt> </dl> </dd> <dt>

<span id="MENROLL_E_DEVICE_INTERNALSERVICE_ERROR"></span><span id="menroll_e_device_internalservice_error"></span>**\_ \_ Ошибка интерналсервице для устройства менролл E \_ \_**
</dt> <dd> <dl> <dt>

0x80180006
</dt> <dt>



На сервере возникло необработанное исключение.

**Windows 8.1:** Эта константа недоступна до Windows 10.


</dt> </dl> </dd> <dt>

<span id="MREGISTER_E_DEVICE_INVALIDSECURITY_ERROR"></span><span id="mregister_e_device_invalidsecurity_error"></span>**\_ \_ Ошибка инвалидсекурити для устройства мрегистер E \_ \_**
</dt> <dd> <dl> <dt>

0x80190007
</dt> <dt>



На сервере возникло необработанное исключение.


</dt> </dl> </dd> <dt>

<span id="MENROLL_E_DEVICE_INVALIDSECURITY_ERROR"></span><span id="menroll_e_device_invalidsecurity_error"></span>**\_ \_ Ошибка инвалидсекурити для устройства менролл E \_ \_**
</dt> <dd> <dl> <dt>

0x80180007
</dt> <dt>



На сервере возникло необработанное исключение.

**Windows 8.1:** Эта константа недоступна до Windows 10.


</dt> </dl> </dd> <dt>

<span id="MREGISTER_E_DEVICE_UNKNOWN_ERROR"></span><span id="mregister_e_device_unknown_error"></span>**\_ \_ \_ неизвестная \_ ошибка устройства мрегистер E**
</dt> <dd> <dl> <dt>

0x80190008
</dt> <dt>



Неизвестная ошибка сервера.


</dt> </dl> </dd> <dt>

<span id="MENROLL_E_DEVICE_UNKNOWN_ERROR"></span><span id="menroll_e_device_unknown_error"></span>**\_ \_ \_ неизвестная \_ ошибка устройства менролл E**
</dt> <dd> <dl> <dt>

0x80180008
</dt> <dt>



Неизвестная ошибка сервера.

**Windows 8.1:** Эта константа недоступна до Windows 10.


</dt> </dl> </dd> <dt>

<span id="MREGISTER_E_REGISTRATION_IN_PROGRESS"></span><span id="mregister_e_registration_in_progress"></span>**\_ \_ выполняется регистрация мрегистер \_ E \_**
</dt> <dd> <dl> <dt>

0x80190009
</dt> <dt>



В настоящее время выполняется другая операция регистрации.


</dt> </dl> </dd> <dt>

<span id="MENROLL_E_ENROLLMENT_IN_PROGRESS"></span><span id="menroll_e_enrollment_in_progress"></span>**\_ \_ идет регистрация менролл E \_ \_**
</dt> <dd> <dl> <dt>

0x80180009
</dt> <dt>



В настоящее время выполняется другая операция регистрации.

**Windows 8.1:** Эта константа недоступна до Windows 10.


</dt> </dl> </dd> <dt>

<span id="MREGISTER_E_DEVICE_ALREADY_REGISTERED"></span><span id="mregister_e_device_already_registered"></span>**\_устройство мрегистер \_ E \_ уже \_ зарегистрировано**
</dt> <dd> <dl> <dt>

0x8019000A
</dt> <dt>



Больше не используется.

**Windows 8.1:** Устройство уже зарегистрировано.


</dt> </dl> </dd> <dt>

<span id="MENROLL_E_DEVICE_ALREADY_ENROLLED"></span><span id="menroll_e_device_already_enrolled"></span>**\_устройство менролл \_ E \_ уже \_ зарегистрировано**
</dt> <dd> <dl> <dt>

0x8018000A
</dt> <dt>



Устройство уже зарегистрировано.

**Windows 8.1:** Эта константа недоступна до Windows 10.


</dt> </dl> </dd> <dt>

<span id="MREGISTER_E_DEVICE_NOT_REGISTERED"></span><span id="mregister_e_device_not_registered"></span>**\_устройство мрегистер \_ E \_ не \_ зарегистрировано**
</dt> <dd> <dl> <dt>

0x8019000B
</dt> <dt>



Больше не используется.

**Windows 8.1:** Устройство не зарегистрировано.


</dt> </dl> </dd> <dt>

<span id="MENROLL_E_DEVICE_NOT_ENROLLED"></span><span id="menroll_e_device_not_enrolled"></span>**\_устройство менролл \_ E \_ не \_ зарегистрировано**
</dt> <dd> <dl> <dt>

0x8018000B
</dt> <dt>



Устройство не зарегистрировано.

**Windows 8.1:** Эта константа недоступна до Windows 10.


</dt> </dl> </dd> <dt>

<span id="MREGISTER_E_DISCOVERY_REDIRECTED"></span><span id="mregister_e_discovery_redirected"></span>**\_Перенаправление \_ обнаружения мрегистер E \_**
</dt> <dd> <dl> <dt>

0x8019000C
</dt> <dt>



Больше не используется.

**Windows 8.1:** Требуется перенаправление.


</dt> </dl> </dd> <dt>

<span id="MREGISTER_E_DEVICE_NOT_AD_REGISTERED_ERROR"></span><span id="mregister_e_device_not_ad_registered_error"></span>**МРЕГИСТЕР \_ E \_ устройство \_ не \_ \_ зарегистрировано \_ Ошибка AD**
</dt> <dd> <dl> <dt>

0x8019000D
</dt> <dt>



Больше не используется.

**Windows 8.1:** Устройство не зарегистрировано в Active Directory.


</dt> </dl> </dd> <dt>

<span id="MENROLL_E_DISCOVERY_SEC_CERT_DATE_INVALID"></span><span id="menroll_e_discovery_sec_cert_date_invalid"></span>**\_ \_ \_ \_ \_ Недопустимая дата сертификата обнаружения менролл E в секунду \_**
</dt> <dd> <dl> <dt>

0x8018000D
</dt> <dt>



Во время обнаружения недопустимая дата сертификата в секунду.

**Windows 8.1:** Эта константа недоступна до Windows 10.


</dt> </dl> </dd> <dt>

<span id="MREGISTER_E_DISCOVERY_FAILED"></span><span id="mregister_e_discovery_failed"></span>**\_ \_ сбой обнаружения мрегистер \_ E**
</dt> <dd> <dl> <dt>

0x8019000E
</dt> <dt>



Больше не используется.

**Windows 8.1:** Сбой обнаружения; требуется перенаправление.


</dt> </dl> </dd> <dt>

<span id="MENROLL_E_PASSWORD_NEEDED"></span><span id="menroll_e_password_needed"></span>**\_ \_ требуется пароль менролл \_ E**
</dt> <dd> <dl> <dt>

0x8018000E
</dt> <dt>



Требуется пароль, но он не был указан.

**Windows 8.1:** Эта константа недоступна до Windows 10.


</dt> </dl> </dd> <dt>

<span id="MENROLL_E_WAB_ERROR"></span><span id="menroll_e_wab_error"></span>**МЕНРОЛЛ \_ E \_ , \_ Ошибка wab**
</dt> <dd> <dl> <dt>

0x8018000F
</dt> <dt>



Во время регистрации WAB произошла ошибка.

**Windows 8.1:** Эта константа недоступна до Windows 10.


</dt> </dl> </dd> <dt>

<span id="MENROLL_E_CONNECTIVITY"></span><span id="menroll_e_connectivity"></span>**\_Подключение менролл E \_**
</dt> <dd> <dl> <dt>

0x80180010
</dt> <dt>



Произошла сетевая ошибка, например DNS или время ожидания сети.

**Windows 8.1:** Эта константа недоступна до Windows 10.


</dt> </dl> </dd> <dt>

<span id="MENROLL_S_ENROLLMENT_SUSPENDED"></span><span id="menroll_s_enrollment_suspended"></span>**\_Регистрация менролл \_ \_ приостановлена**
</dt> <dd> <dl> <dt>

0x00180011
</dt> <dt>



Регистрация приостановлена. Больше не поддерживается.

**Windows 8.1:** Эта константа недоступна до Windows 10.


</dt> </dl> </dd> <dt>

<span id="MENROLL_E_INVALIDSSLCERT"></span><span id="menroll_e_invalidsslcert"></span>**МЕНРОЛЛ \_ E \_ инвалидсслцерт**
</dt> <dd> <dl> <dt>

0x80180012
</dt> <dt>



Недопустимый SSL-сертификат.

**Windows 8.1:** Эта константа недоступна до Windows 10.


</dt> </dl> </dd> <dt>

<span id="MENROLL_E_DEVICECAPREACHED"></span><span id="menroll_e_devicecapreached"></span>**МЕНРОЛЛ \_ E \_ DEVICECAPREACHED**
</dt> <dd> <dl> <dt>

0x80180013
</dt> <dt>



Пользователь уже зарегистрировал слишком много устройств. Удалите или отменяйте регистрацию старых, чтобы устранить эту ошибку. Обратите внимание, что пользователь может устранить эту ошибку без помощи администратора.

**Windows 8.1:** Эта константа недоступна до Windows 10.


</dt> </dl> </dd> <dt>

<span id="MENROLL_E_DEVICENOTSUPPORTED"></span><span id="menroll_e_devicenotsupported"></span>**МЕНРОЛЛ \_ E \_ девиценотсуппортед**
</dt> <dd> <dl> <dt>

кодом 0x80180014
</dt> <dt>



Определенная платформа (например, Windows) или версия не поддерживается. Общее исправление этой ошибки — обновление устройства.

**Windows 8.1:** Эта константа недоступна до Windows 10.


</dt> </dl> </dd> <dt>

<span id="MENROLL_E_NOTSUPPORTED"></span><span id="menroll_e_notsupported"></span>**МЕНРОЛЛ \_ E \_ NOTSUPPORTED**
</dt> <dd> <dl> <dt>

0x80180015
</dt> <dt>



Обычно управление мобильными устройствами не поддерживается для этого устройства — пользователь может вызвать администратора, но маловероятно, чтобы устранить эту проблему.

**Windows 8.1:** Эта константа недоступна до Windows 10.


</dt> </dl> </dd> <dt>

<span id="MREGISTER_E_NOTELIGIBLETORENEW"></span><span id="mregister_e_noteligibletorenew"></span>**МРЕГИСТЕР \_ E \_ нотелигиблеторенев**
</dt> <dd> <dl> <dt>

0x80180016
</dt> <dt>



Устройство пытается продлить, но сервер отклонил запрос. Проверка времени на устройстве. Пользователь может устранить эту ошибку путем повторной регистрации.

**Windows 8.1:** Эта константа недоступна до Windows 10.


</dt> </dl> </dd> <dt>

<span id="MENROLL_E_INMAINTENANCE"></span><span id="menroll_e_inmaintenance"></span>**МЕНРОЛЛ \_ E \_**
</dt> <dd> <dl> <dt>

0x80180017
</dt> <dt>



Учетная запись находится в состоянии обслуживания; Повторите попытку позже. Пользователь может повторить попытку позже. Однако пользователь может выбрать вызов администратора для определения расписания обслуживания.

**Windows 8.1:** Эта константа недоступна до Windows 10.


</dt> </dl> </dd> <dt>

<span id="MENROLL_E_USERLICENSE"></span><span id="menroll_e_userlicense"></span>**МЕНРОЛЛ \_ E \_ усерлиценсе**
</dt> <dd> <dl> <dt>

0x80180018
</dt> <dt>



Лицензия пользователя находится в неисправном состоянии, блокирующем регистрацию. пользователь должен будет вызвать администратор.

**Windows 8.1:** Эта константа недоступна до Windows 10.


</dt> </dl> </dd> <dt>

<span id="MENROLL_E_ENROLLMENTDATAINVALID"></span><span id="menroll_e_enrollmentdatainvalid"></span>**МЕНРОЛЛ \_ E \_ енроллментдатаинвалид**
</dt> <dd> <dl> <dt>

0x80180019
</dt> <dt>



Сервер отклонил данные регистрации. возможно, сервер настроен неправильно.

**Windows 8.1:** Эта константа недоступна до Windows 10.


</dt> </dl> </dd> <dt>

<span id="MENROLL_E_INSECUREREDIRECT"></span><span id="menroll_e_insecureredirect"></span>**МЕНРОЛЛ \_ E \_ инсекурередирект**
</dt> <dd> <dl> <dt>

0x8018001A
</dt> <dt>



Сервер запросил HTTP, а не HTTPS, но он не был принят.

**Windows 8.1:** Эта константа недоступна до Windows 10.


</dt> </dl> </dd> <dt>

<span id="MENROLL_E_PLATFORM_WRONG_STATE"></span><span id="menroll_e_platform_wrong_state"></span>**\_ \_ \_ неправильное \_ состояние платформы менролл E**
</dt> <dd> <dl> <dt>

0x8018001B
</dt> <dt>



Попытка выполнить недопустимую операцию, например повторная регистрация одного и того же устройства дважды или Отмена регистрации неизвестного устройства.

**Windows 8.1:** Эта константа недоступна до Windows 10.


</dt> </dl> </dd> <dt>

<span id="MENROLL_E_PLATFORM_LICENSE_ERROR"></span><span id="menroll_e_platform_license_error"></span>**\_ \_ \_ Ошибка лицензии платформы менролл \_ E**
</dt> <dd> <dl> <dt>

0x8018001C
</dt> <dt>



Версия Windows, установленная на клиенте, не поддерживает этот тип регистрации.

**Windows 8.1:** Эта константа недоступна до Windows 10.


</dt> </dl> </dd> <dt>

<span id="MENROLL_E_PLATFORM_UNKNOWN_ERROR"></span><span id="menroll_e_platform_unknown_error"></span>**\_ \_ \_ неизвестная \_ Ошибка платформы менролл E**
</dt> <dd> <dl> <dt>

0x8018001D
</dt> <dt>



На клиенте произошла неизвестная ошибка.

**Windows 8.1:** Эта константа недоступна до Windows 10.


</dt> </dl> </dd> <dt>

<span id="MENROLL_E_PROV_CSP_CERTSTORE"></span><span id="menroll_e_prov_csp_certstore"></span>**МЕНРОЛЛ \_ E \_ Prov \_ CSP \_ цертсторе**
</dt> <dd> <dl> <dt>

0x8018001E
</dt> <dt>



Сбой подготовки в CSP хранилища сертификатов.

**Windows 8.1:** Эта константа недоступна до Windows 10.


</dt> </dl> </dd> <dt>

<span id="MENROLL_E_PROV_CSP_W7"></span><span id="menroll_e_prov_csp_w7"></span>**МЕНРОЛЛ \_ E \_ Prov \_ CSP \_ W7**
</dt> <dd> <dl> <dt>

0x8018001F
</dt> <dt>



Сбой подготовки в W7/Дмакк CPP.

**Windows 8.1:** Эта константа недоступна до Windows 10.


</dt> </dl> </dd> <dt>

<span id="MENROLL_E_PROV_CSP_DMCLIENT"></span><span id="menroll_e_prov_csp_dmclient"></span>**МЕНРОЛЛ \_ E \_ Prov \_ CSP \_ DMCLIENT**
</dt> <dd> <dl> <dt>

0x80180020
</dt> <dt>



Сбой подготовки в CSP клиента DM.

**Windows 8.1:** Эта константа недоступна до Windows 10.


</dt> </dl> </dd> <dt>

<span id="MENROLL_E_PROV_CSP_PFW"></span><span id="menroll_e_prov_csp_pfw"></span>**МЕНРОЛЛ \_ E \_ Prov \_ CSP \_ пфв**
</dt> <dd> <dl> <dt>

0x80180021
</dt> <dt>



Сбой подготовки в CSP для работы Passport for Network.

**Windows 8.1:** Эта константа недоступна до Windows 10.


</dt> </dl> </dd> <dt>

<span id="MENROLL_E_PROV_CSP_MISC"></span><span id="menroll_e_prov_csp_misc"></span>**МЕНРОЛЛ \_ E \_ Prov \_ . \_ Прочее**
</dt> <dd> <dl> <dt>

0x80180022
</dt> <dt>



Сбой подготовки в CSP, не указанном выше.

**Windows 8.1:** Эта константа недоступна до Windows 10.


</dt> </dl> </dd> <dt>

<span id="MENROLL_E_PROV_UNKNOWN"></span><span id="menroll_e_prov_unknown"></span>**Неизвестный МЕНРОЛЛ \_ E \_ Prov \_**
</dt> <dd> <dl> <dt>

0x80180023
</dt> <dt>



Сбой подготовки, но не указан конкретный CSP.

**Windows 8.1:** Эта константа недоступна до Windows 10.


</dt> </dl> </dd> <dt>

<span id="MENROLL_E_PROV_SSLCERTNOTFOUND"></span><span id="menroll_e_prov_sslcertnotfound"></span>**МЕНРОЛЛ \_ E \_ Prov \_ сслцертнотфаунд**
</dt> <dd> <dl> <dt>

0x80180024
</dt> <dt>



При попытке привязки открытого сертификата или закрытого ключа общедоступный сертификат не был найден: при попытке привязки открытого сертификата или закрытого ключа или при поиске полезных данных подготовки (возможно, нацеленных на неправильное хранилище).

**Windows 8.1:** Эта константа недоступна до Windows 10.


</dt> </dl> </dd> <dt>

<span id="MENROLL_E_PROV_CSP_APPMGMT"></span><span id="menroll_e_prov_csp_appmgmt"></span>**МЕНРОЛЛ \_ E \_ Prov \_ CSP \_ аппмгмт**
</dt> <dd> <dl> <dt>

0x80180025
</dt> <dt>



Сбой подготовки в CSP Ентерприсеаппманажемент.

> [!Note]  
> Эта константа недоступна до Windows 10, версия 1709.

 


</dt> </dl> </dd> <dt>

<span id="MENROLL_E_DEVICE_MANAGEMENT_BLOCKED"></span><span id="menroll_e_device_management_blocked"></span>**\_ \_ Управление устройством менролл \_ \_ заблокировано**
</dt> <dd> <dl> <dt>

0x80180026
</dt> <dt>



Управление мобильными устройствами (MDM) было заблокировано, возможно, с помощью групповая политика или функции [**сетманажедекстерналли**](/windows/desktop/api/MDMRegistration/nf-mdmregistration-setmanagedexternally) .

> [!Note]  
> Эта константа недоступна до Windows 10, версия 1709.

 


</dt> </dl> </dd> <dt>

<span id="MENROLL_E_CERTPOLICY_PRIVATEKEYCREATION_FAILED"></span><span id="menroll_e_certpolicy_privatekeycreation_failed"></span>**\_ \_ \_ сбой приватекэйкреатион цертполици \_ менролл**
</dt> <dd> <dl> <dt>

0x80180027
</dt> <dt>



Не удалось создать закрытый ключ.

> [!Note]  
> Эта константа недоступна до Windows 10, версия 1709.

 


</dt> </dl> </dd> <dt>

<span id="MENROLL_E_CERTAUTH_FAILED_TO_FIND_CERT"></span><span id="menroll_e_certauth_failed_to_find_cert"></span>**МЕНРОЛЛ \_ E \_ цертаус \_ не \_ удалось \_ найти \_ сертификат**
</dt> <dd> <dl> <dt>

0x80180028
</dt> <dt>



Запрошена проверка подлинности сертификата, но не удалось найти сертификат для использования.

> [!Note]  
> Эта константа недоступна до Windows 10, версия 1709.

 


</dt> </dl> </dd> <dt>

<span id="MENROLL_E_EMPTY_MESSAGE"></span><span id="menroll_e_empty_message"></span>**МЕНРОЛЛ \_ е \_ пустое \_ сообщение**
</dt> <dd> <dl> <dt>

0x80180029
</dt> <dt>



Сервер ответил HTTP 200, но сообщение было пустым.

> [!Note]  
> Эта константа недоступна до Windows 10, версия 1709.

 


</dt> </dl> </dd> <dt>

<span id="MENROLL_E_USER_CANCELED_"></span><span id="menroll_e_user_canceled_"></span>**\_Отмена менролл \_ пользователем \_** 
</dt> <dd> <dl> <dt>

0x80180030
</dt> <dt>



Пользователь отменил операцию.

> [!Note]  
> Эта константа недоступна до Windows 10, версия 1709.

 


</dt> </dl> </dd> <dt>

<span id="MENROLL_E_MDM_NOT_CONFIGURED"></span><span id="menroll_e_mdm_not_configured"></span>**МЕНРОЛЛ \_ . \_ \_ не \_ настроено MDM**
</dt> <dd> <dl> <dt>

0x80180031
</dt> <dt>



Управление мобильными устройствами (MDM) не настроено.

> [!Note]  
> Эта константа недоступна до Windows 10, версия 1709.

 


</dt> </dl> </dd> </dl>

## <a name="requirements"></a>Требования

| Требование | Применение |
|-------------------------------------|----------------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Windows 8.1<br/>                                                                       |
| Минимальная версия сервера<br/> | Ни одна версия не поддерживается<br/>                                                                    |
| Заголовок<br/>                   | <dl> <dt>Мдмрегистратион. h</dt> </dl> |



 

 





