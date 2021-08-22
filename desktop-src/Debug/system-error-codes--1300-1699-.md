---
description: Описание кодов ошибок 1300-1699, определенных в файле заголовка WinError. h и предназначенных для разработчиков.
ms.assetid: 7b04a2ba-7bf9-4bff-93c8-cbb0060e069d
title: Коды системных ошибок (1300-1699) (WinError. h)
ms.topic: reference
ms.date: 07/18/2019
ms.openlocfilehash: 7aeb1c3642331db8ed3215d55a6d77e1e7b2a98c3859a5eb64a1d5b60350d24a
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119310924"
---
# <a name="system-error-codes-1300-1699"></a>Коды системных ошибок (1300-1699)

> [!NOTE]
> Эти сведения предназначены для разработчиков, которые отлаживать системные ошибки. для других ошибок, например проблем с Центр обновления Windows, на странице [коды ошибок](system-error-codes.md) содержится список ресурсов.

В следующем списке приведены [коды системных ошибок](system-error-codes.md) для ошибок 1300 – 1699. Они возвращаются функцией [**GetLastError**](/windows/win32/api/errhandlingapi/nf-errhandlingapi-getlasterror) при сбое множества функций. Чтобы получить текст описания ошибки в приложении, используйте функцию [**FormatMessage**](/windows/desktop/api/WinBase/nf-winbase-formatmessage) с флагом **формата \_ Message \_ из \_ System** .

<dl> <dt>

<span id="ERROR_NOT_ALL_ASSIGNED"></span><span id="error_not_all_assigned"></span>**Ошибка \_ не \_ \_ назначена всем**
</dt> <dd> <dl> <dt>

1300 (0x514)
</dt> <dt>



Не все привилегии или группы, на которые имеются ссылки, назначены вызывающему объекту.


</dt> </dl> </dd> <dt>

<span id="ERROR_SOME_NOT_MAPPED"></span><span id="error_some_not_mapped"></span>**Ошибка \_ \_ не \_ сопоставлена**
</dt> <dd> <dl> <dt>

1301 (0x515)
</dt> <dt>



Не было выполнено сопоставление между именами учетных записей и идентификаторами безопасности.


</dt> </dl> </dd> <dt>

<span id="ERROR_NO_QUOTAS_FOR_ACCOUNT"></span><span id="error_no_quotas_for_account"></span>**Ошибка при \_ отсутствии \_ квот \_ для \_ учетной записи**
</dt> <dd> <dl> <dt>

1302 (0x516)
</dt> <dt>



Для этой учетной записи не заданы ограничения системной квоты.


</dt> </dl> </dd> <dt>

<span id="ERROR_LOCAL_USER_SESSION_KEY"></span><span id="error_local_user_session_key"></span>**Ошибка \_ \_ \_ ключа сеанса локального пользователя \_**
</dt> <dd> <dl> <dt>

1303 (0x517)
</dt> <dt>



Ключ шифрования недоступен. Был возвращен хорошо известный ключ шифрования.


</dt> </dl> </dd> <dt>

<span id="ERROR_NULL_LM_PASSWORD"></span><span id="error_null_lm_password"></span>**Ошибка \_ null \_ \_ пароль LM**
</dt> <dd> <dl> <dt>

1304 (0x518)
</dt> <dt>



Пароль слишком сложен для преобразования в пароль LAN Manager. Возвращенный пароль LAN Manager является **пустой** строкой.


</dt> </dl> </dd> <dt>

<span id="ERROR_UNKNOWN_REVISION"></span><span id="error_unknown_revision"></span>**Ошибка \_ неизвестной \_ редакции**
</dt> <dd> <dl> <dt>

1305 (0x519)
</dt> <dt>



Неизвестный уровень редакции.


</dt> </dl> </dd> <dt>

<span id="ERROR_REVISION_MISMATCH"></span><span id="error_revision_mismatch"></span>**\_несоответствие редакции ошибки \_**
</dt> <dd> <dl> <dt>

1306 (0x51A)
</dt> <dt>



Указывает, что два уровня редакции несовместимы.


</dt> </dl> </dd> <dt>

<span id="ERROR_INVALID_OWNER"></span><span id="error_invalid_owner"></span>**Ошибка \_ недопустимого \_ владельца**
</dt> <dd> <dl> <dt>

1307 (0x51B)
</dt> <dt>



Этот идентификатор безопасности нельзя назначить в качестве владельца этого объекта.


</dt> </dl> </dd> <dt>

<span id="ERROR_INVALID_PRIMARY_GROUP"></span><span id="error_invalid_primary_group"></span>**Ошибка \_ недопустимой \_ основной \_ группы**
</dt> <dd> <dl> <dt>

1308 (0x51C)
</dt> <dt>



Этот идентификатор безопасности нельзя назначить в качестве основной группы объекта.


</dt> </dl> </dd> <dt>

<span id="ERROR_NO_IMPERSONATION_TOKEN"></span><span id="error_no_impersonation_token"></span>**Ошибка \_ без \_ \_ маркера олицетворения**
</dt> <dd> <dl> <dt>

1309 (0x51D)
</dt> <dt>



Предпринята попытка обработать токен олицетворения потоком, который в настоящее время не олицетворяет клиента.


</dt> </dl> </dd> <dt>

<span id="ERROR_CANT_DISABLE_MANDATORY"></span><span id="error_cant_disable_mandatory"></span>**ОШИБКА не \_ удается \_ Отключить \_ обязательный параметр**
</dt> <dd> <dl> <dt>

1310 (0x51E)
</dt> <dt>



Группа может быть отключена.


</dt> </dl> </dd> <dt>

<span id="ERROR_NO_LOGON_SERVERS"></span><span id="error_no_logon_servers"></span>**\_нет \_ серверов входа в систему \_**
</dt> <dd> <dl> <dt>

1311 (0x51F)
</dt> <dt>



В настоящее время нет доступных серверов входа для обслуживания запроса на вход.


</dt> </dl> </dd> <dt>

<span id="ERROR_NO_SUCH_LOGON_SESSION"></span><span id="error_no_such_logon_session"></span>**Ошибка \_ без \_ \_ сеанса входа в систему \_**
</dt> <dd> <dl> <dt>

1312 (0x520)
</dt> <dt>



A specified logon session does not exist. Возможно, он уже завершен.


</dt> </dl> </dd> <dt>

<span id="ERROR_NO_SUCH_PRIVILEGE"></span><span id="error_no_such_privilege"></span>**Ошибка \_ без \_ такой \_ привилегии**
</dt> <dd> <dl> <dt>

1313 (0x521)
</dt> <dt>



Указанное право доступа не существует.


</dt> </dl> </dd> <dt>

<span id="ERROR_PRIVILEGE_NOT_HELD"></span><span id="error_privilege_not_held"></span>**права на ошибку \_ \_ не \_ удерживаются**
</dt> <dd> <dl> <dt>

1314 (0x522)
</dt> <dt>



Клиент не располагает требуемыми правами доступа.


</dt> </dl> </dd> <dt>

<span id="ERROR_INVALID_ACCOUNT_NAME"></span><span id="error_invalid_account_name"></span>**Ошибка при \_ недопустимом \_ имени учетной записи \_**
</dt> <dd> <dl> <dt>

1315 (0x523)
</dt> <dt>



Указанное имя не является правильно сформированным именем учетной записи.


</dt> </dl> </dd> <dt>

<span id="ERROR_USER_EXISTS"></span><span id="error_user_exists"></span>**Ошибка \_ пользователь \_ существует**
</dt> <dd> <dl> <dt>

1316 (0x524)
</dt> <dt>



Указанная учетная запись уже существует.


</dt> </dl> </dd> <dt>

<span id="ERROR_NO_SUCH_USER"></span><span id="error_no_such_user"></span>**Ошибка \_ без \_ такого \_ пользователя**
</dt> <dd> <dl> <dt>

1317 (0x525)
</dt> <dt>



Указанная учетная запись не существует.


</dt> </dl> </dd> <dt>

<span id="ERROR_GROUP_EXISTS"></span><span id="error_group_exists"></span>**\_существует группа \_ ошибок**
</dt> <dd> <dl> <dt>

1318 (0x526)
</dt> <dt>



Указанная группа уже существует.


</dt> </dl> </dd> <dt>

<span id="ERROR_NO_SUCH_GROUP"></span><span id="error_no_such_group"></span>**Ошибка \_ нет \_ такой \_ группы**
</dt> <dd> <dl> <dt>

1319 (0x527)
</dt> <dt>



Указанная группа не существует.


</dt> </dl> </dd> <dt>

<span id="ERROR_MEMBER_IN_GROUP"></span><span id="error_member_in_group"></span>**\_элемент ошибки \_ в \_ группе**
</dt> <dd> <dl> <dt>

1320 (0x528)
</dt> <dt>



Либо указанная учетная запись пользователя уже является членом указанной группы, либо указанная группа не может быть удалена, так как она содержит элемент.


</dt> </dl> </dd> <dt>

<span id="ERROR_MEMBER_NOT_IN_GROUP"></span><span id="error_member_not_in_group"></span>**\_элемент ошибки \_ не входит \_ в \_ группу**
</dt> <dd> <dl> <dt>

1321 (0x529)
</dt> <dt>



Указанная учетная запись пользователя не является членом указанной учетной записи группы.


</dt> </dl> </dd> <dt>

<span id="ERROR_LAST_ADMIN"></span><span id="error_last_admin"></span>**Ошибка \_ последнего \_ администратора**
</dt> <dd> <dl> <dt>

1322 (0x52A)
</dt> <dt>



Эта операция запрещена, так как она может привести к отключению, удалению или невозможности входа в учетную запись администрирования.


</dt> </dl> </dd> <dt>

<span id="ERROR_WRONG_PASSWORD"></span><span id="error_wrong_password"></span>**ОШИБОЧный \_ \_ пароль**
</dt> <dd> <dl> <dt>

1323 (0x52B)
</dt> <dt>



Не удалось обновить пароль. В качестве текущего пароля указано неверное значение.


</dt> </dl> </dd> <dt>

<span id="ERROR_ILL_FORMED_PASSWORD"></span><span id="error_ill_formed_password"></span>**ОШИБКА с неправильным \_ \_ форматом \_ пароля**
</dt> <dd> <dl> <dt>

1324 (0x52C)
</dt> <dt>



Не удалось обновить пароль. Значение, указанное для нового пароля, содержит значения, недопустимые в паролях.


</dt> </dl> </dd> <dt>

<span id="ERROR_PASSWORD_RESTRICTION"></span><span id="error_password_restriction"></span>**\_ограничение на пароли об ошибках \_**
</dt> <dd> <dl> <dt>

1325 (0x52D)
</dt> <dt>



Не удалось обновить пароль. Значение, указанное для нового пароля, не соответствует требованиям домена к длине, сложности или истории.


</dt> </dl> </dd> <dt>

<span id="ERROR_LOGON_FAILURE"></span><span id="error_logon_failure"></span>**Ошибка \_ при входе в систему \_**
</dt> <dd> <dl> <dt>

1326 (0x52E)
</dt> <dt>



Неправильное имя пользователя или пароль.


</dt> </dl> </dd> <dt>

<span id="ERROR_ACCOUNT_RESTRICTION"></span><span id="error_account_restriction"></span>**\_ограничение учетной записи об ошибках \_**
</dt> <dd> <dl> <dt>

1327 (0x52F)
</dt> <dt>



Ограничения учетной записи запрещают вход пользователя в систему. Например, пустые пароли не допускаются, время входа ограничено или применяется ограничение политики.


</dt> </dl> </dd> <dt>

<span id="ERROR_INVALID_LOGON_HOURS"></span><span id="error_invalid_logon_hours"></span>**Ошибка \_ недопустимых \_ \_ часов входа**
</dt> <dd> <dl> <dt>

1328 (0x530)
</dt> <dt>



В вашей учетной записи есть ограничения по времени, которые не позволяют войти в систему прямо сейчас.


</dt> </dl> </dd> <dt>

<span id="ERROR_INVALID_WORKSTATION"></span><span id="error_invalid_workstation"></span>**Ошибка \_ недопустимой \_ рабочей станции**
</dt> <dd> <dl> <dt>

1329 (0x531)
</dt> <dt>



Этому пользователю запрещено входить на этот компьютер.


</dt> </dl> </dd> <dt>

<span id="ERROR_PASSWORD_EXPIRED"></span><span id="error_password_expired"></span>**\_ \_ срок действия пароля истек**
</dt> <dd> <dl> <dt>

1330 (0x532)
</dt> <dt>



Срок действия пароля для этой учетной записи истек.


</dt> </dl> </dd> <dt>

<span id="ERROR_ACCOUNT_DISABLED"></span><span id="error_account_disabled"></span>**\_учетная запись ошибок \_ отключена**
</dt> <dd> <dl> <dt>

1331 (0x533)
</dt> <dt>



Этот пользователь не может войти в систему, так как эта учетная запись в настоящее время отключена.


</dt> </dl> </dd> <dt>

<span id="ERROR_NONE_MAPPED"></span><span id="error_none_mapped"></span>**Ошибка " \_ нет \_ сопоставления"**
</dt> <dd> <dl> <dt>

1332 (0x534)
</dt> <dt>



Сопоставление между именами учетных записей и идентификаторами безопасности не выполнялось.


</dt> </dl> </dd> <dt>

<span id="ERROR_TOO_MANY_LUIDS_REQUESTED"></span><span id="error_too_many_luids_requested"></span>**Ошибка \_ слишком \_ много \_ \_ запрошенных LUID**
</dt> <dd> <dl> <dt>

1333 (0x535)
</dt> <dt>



Слишком много локальных идентификаторов пользователей (LUID) запрошено за один раз.


</dt> </dl> </dd> <dt>

<span id="ERROR_LUIDS_EXHAUSTED"></span><span id="error_luids_exhausted"></span>**Ошибка \_ LUID \_ исчерпана**
</dt> <dd> <dl> <dt>

1334 (0x536)
</dt> <dt>



Больше нет доступных идентификаторов локальных пользователей (LUID).


</dt> </dl> </dd> <dt>

<span id="ERROR_INVALID_SUB_AUTHORITY"></span><span id="error_invalid_sub_authority"></span>**Ошибка \_ недопустимого \_ \_ подцентра**
</dt> <dd> <dl> <dt>

1335 (0x537)
</dt> <dt>



Часть подавтора идентификатора безопасности недопустима для этого конкретного использования.


</dt> </dl> </dd> <dt>

<span id="ERROR_INVALID_ACL"></span><span id="error_invalid_acl"></span>**Ошибка \_ недопустимого \_ ACL**
</dt> <dd> <dl> <dt>

1336 (0x538)
</dt> <dt>



Недопустимая структура списка управления доступом (ACL).


</dt> </dl> </dd> <dt>

<span id="ERROR_INVALID_SID"></span><span id="error_invalid_sid"></span>**Ошибка \_ недопустимого \_ sid**
</dt> <dd> <dl> <dt>

1337 (0x539)
</dt> <dt>



Недопустимая структура идентификатора безопасности.


</dt> </dl> </dd> <dt>

<span id="ERROR_INVALID_SECURITY_DESCR"></span><span id="error_invalid_security_descr"></span>**Ошибка \_ недопустимых \_ \_ Descr безопасности**
</dt> <dd> <dl> <dt>

1338 (0x53A)
</dt> <dt>



Недопустимая структура дескриптора безопасности.


</dt> </dl> </dd> <dt>

<span id="ERROR_BAD_INHERITANCE_ACL"></span><span id="error_bad_inheritance_acl"></span>**Ошибка при \_ неправильном \_ ACL наследования \_**
</dt> <dd> <dl> <dt>

1340 (0x53C)
</dt> <dt>



Не удалось построить наследуемый список управления доступом (ACL) или запись управления доступом (ACE).


</dt> </dl> </dd> <dt>

<span id="ERROR_SERVER_DISABLED"></span><span id="error_server_disabled"></span>**\_сервер ошибок \_ отключен**
</dt> <dd> <dl> <dt>

1341 (0x53D)
</dt> <dt>



Сервер в настоящее время отключен.


</dt> </dl> </dd> <dt>

<span id="ERROR_SERVER_NOT_DISABLED"></span><span id="error_server_not_disabled"></span>**\_сервер ошибок \_ не \_ отключен**
</dt> <dd> <dl> <dt>

1342 (0x53E)
</dt> <dt>



Сервер в настоящее время включен.


</dt> </dl> </dd> <dt>

<span id="ERROR_INVALID_ID_AUTHORITY"></span><span id="error_invalid_id_authority"></span>**Ошибка при \_ недопустимом \_ \_ центре идентификации**
</dt> <dd> <dl> <dt>

1343 (0x53F)
</dt> <dt>



Предоставлено недопустимое значение для центра идентификации.


</dt> </dl> </dd> <dt>

<span id="ERROR_ALLOTTED_SPACE_EXCEEDED"></span><span id="error_allotted_space_exceeded"></span>**\_превышено выделенное место для ошибки \_ \_**
</dt> <dd> <dl> <dt>

1344 (0x540)
</dt> <dt>



Больше нет доступной памяти для обновлений сведений о безопасности.


</dt> </dl> </dd> <dt>

<span id="ERROR_INVALID_GROUP_ATTRIBUTES"></span><span id="error_invalid_group_attributes"></span>**Ошибка \_ недопустимых \_ \_ атрибутов группы**
</dt> <dd> <dl> <dt>

1345 (0x541)
</dt> <dt>



Указанные атрибуты недопустимы или несовместимы с атрибутами группы в целом.


</dt> </dl> </dd> <dt>

<span id="ERROR_BAD_IMPERSONATION_LEVEL"></span><span id="error_bad_impersonation_level"></span>**Ошибка \_ неверного \_ уровня олицетворения \_**
</dt> <dd> <dl> <dt>

1346 (0x542)
</dt> <dt>



Либо не обеспечен необходимый уровень олицетворения, либо уровень олицетворения недопустим.


</dt> </dl> </dd> <dt>

<span id="ERROR_CANT_OPEN_ANONYMOUS"></span><span id="error_cant_open_anonymous"></span>**ОШИБКА не \_ удается \_ открыть \_ анонимную**
</dt> <dd> <dl> <dt>

1347 (0x543)
</dt> <dt>



Не удается открыть маркер безопасности анонимного уровня.


</dt> </dl> </dd> <dt>

<span id="ERROR_BAD_VALIDATION_CLASS"></span><span id="error_bad_validation_class"></span>**Ошибка \_ неправильного \_ \_ класса проверки**
</dt> <dd> <dl> <dt>

1348 (0x544)
</dt> <dt>



Запрошен недопустимый класс сведений о проверке.


</dt> </dl> </dd> <dt>

<span id="ERROR_BAD_TOKEN_TYPE"></span><span id="error_bad_token_type"></span>**Ошибка \_ неправильного \_ типа токена \_**
</dt> <dd> <dl> <dt>

1349 (0x545)
</dt> <dt>



Тип токена не подходит для использования при его использовании.


</dt> </dl> </dd> <dt>

<span id="ERROR_NO_SECURITY_ON_OBJECT"></span><span id="error_no_security_on_object"></span>**Ошибка \_ \_ при отсутствии безопасности \_ для \_ объекта**
</dt> <dd> <dl> <dt>

1350 (0x546)
</dt> <dt>



Не удалось выполнить операцию безопасности для объекта, который не имеет связанной безопасности.


</dt> </dl> </dd> <dt>

<span id="ERROR_CANT_ACCESS_DOMAIN_INFO"></span><span id="error_cant_access_domain_info"></span>**ОШИБКА не \_ удается \_ получить доступ к \_ \_ сведениям о домене**
</dt> <dd> <dl> <dt>

1351 (0x547)
</dt> <dt>



Не удалось прочитать сведения о конфигурации из контроллера домена, так как компьютер недоступен или доступ запрещен.


</dt> </dl> </dd> <dt>

<span id="ERROR_INVALID_SERVER_STATE"></span><span id="error_invalid_server_state"></span>**Ошибка \_ недопустимого \_ \_ состояния сервера**
</dt> <dd> <dl> <dt>

1352 (0x548)
</dt> <dt>



Диспетчеру учетных записей безопасности (SAM) или локальному администратору безопасности (LSA) находилось в неправильном состоянии выполнить операцию безопасности.


</dt> </dl> </dd> <dt>

<span id="ERROR_INVALID_DOMAIN_STATE"></span><span id="error_invalid_domain_state"></span>**Ошибка \_ недопустимого \_ \_ состояния домена**
</dt> <dd> <dl> <dt>

1353 (0x549)
</dt> <dt>



Домен находился в неправильном состоянии для выполнения операции безопасности.


</dt> </dl> </dd> <dt>

<span id="ERROR_INVALID_DOMAIN_ROLE"></span><span id="error_invalid_domain_role"></span>**Ошибка \_ недопустимой \_ \_ роли домена**
</dt> <dd> <dl> <dt>

1354 (0x54A)
</dt> <dt>



Эта операция разрешена только для основного контроллера домена.


</dt> </dl> </dd> <dt>

<span id="ERROR_NO_SUCH_DOMAIN"></span><span id="error_no_such_domain"></span>**Ошибка \_ без \_ такого \_ домена**
</dt> <dd> <dl> <dt>

1355 (0x54B)
</dt> <dt>



Указанный домен не существует, или к нему не удалось подключиться.


</dt> </dl> </dd> <dt>

<span id="ERROR_DOMAIN_EXISTS"></span><span id="error_domain_exists"></span>**\_домен ошибок \_ существует**
</dt> <dd> <dl> <dt>

1356 (0x54C)
</dt> <dt>



Указанный домен уже существует.


</dt> </dl> </dd> <dt>

<span id="ERROR_DOMAIN_LIMIT_EXCEEDED"></span><span id="error_domain_limit_exceeded"></span>**\_ \_ превышен предел для домена с ошибками \_**
</dt> <dd> <dl> <dt>

1357 (0x54D)
</dt> <dt>



Предпринята попытка превысить предельное число доменов на сервер.


</dt> </dl> </dd> <dt>

<span id="ERROR_INTERNAL_DB_CORRUPTION"></span><span id="error_internal_db_corruption"></span>**Ошибка \_ внутреннего \_ повреждения базы данных \_**
</dt> <dd> <dl> <dt>

1358 (0x54E)
</dt> <dt>



Не удалось завершить запрошенную операцию из-за катастрофического сбоя носителя или повреждения структуры данных на диске.


</dt> </dl> </dd> <dt>

<span id="ERROR_INTERNAL_ERROR"></span><span id="error_internal_error"></span>**ПРОИЗОШЛа \_ Внутренняя \_ Ошибка**
</dt> <dd> <dl> <dt>

1359 (0x54F)
</dt> <dt>



Внутренняя ошибка.


</dt> </dl> </dd> <dt>

<span id="ERROR_GENERIC_NOT_MAPPED"></span><span id="error_generic_not_mapped"></span>**Ошибка \_ Generic \_ не \_ сопоставлена**
</dt> <dd> <dl> <dt>

1360 (0x550)
</dt> <dt>



Универсальные типы доступа содержались в маске доступа, которая должна быть уже сопоставлена с неуниверсальными типами.


</dt> </dl> </dd> <dt>

<span id="ERROR_BAD_DESCRIPTOR_FORMAT"></span><span id="error_bad_descriptor_format"></span>**Ошибка в \_ неправильном \_ формате дескриптора \_**
</dt> <dd> <dl> <dt>

1361 (0x551)
</dt> <dt>



Неправильный формат дескриптора безопасности (абсолютный или автономный).


</dt> </dl> </dd> <dt>

<span id="ERROR_NOT_LOGON_PROCESS"></span><span id="error_not_logon_process"></span>**Ошибка \_ при \_ входе в \_ процесс**
</dt> <dd> <dl> <dt>

1362 (0x552)
</dt> <dt>



Запрошенное действие ограничено только процессами входа в систему. Вызывающий процесс не зарегистрирован в качестве процесса входа в систему.


</dt> </dl> </dd> <dt>

<span id="ERROR_LOGON_SESSION_EXISTS"></span><span id="error_logon_session_exists"></span>**\_ \_ существует сеанс с ошибкой входа \_**
</dt> <dd> <dl> <dt>

1363 (0x553)
</dt> <dt>



Невозможно запустить новый сеанс входа с уже используемым ИДЕНТИФИКАТОРом.


</dt> </dl> </dd> <dt>

<span id="ERROR_NO_SUCH_PACKAGE"></span><span id="error_no_such_package"></span>**Ошибка \_ \_ : такой \_ пакет отсутствует**
</dt> <dd> <dl> <dt>

1364 (0x554)
</dt> <dt>



Указанный пакет проверки подлинности неизвестен.


</dt> </dl> </dd> <dt>

<span id="ERROR_BAD_LOGON_SESSION_STATE"></span><span id="error_bad_logon_session_state"></span>**Ошибка при \_ неправильном \_ \_ состоянии сеанса входа \_**
</dt> <dd> <dl> <dt>

1365 (0x555)
</dt> <dt>



Сеанс входа в систему не находится в состоянии, соответствующем запрошенной операции.


</dt> </dl> </dd> <dt>

<span id="ERROR_LOGON_SESSION_COLLISION"></span><span id="error_logon_session_collision"></span>**Ошибка \_ при \_ \_ конфликте сеанса входа**
</dt> <dd> <dl> <dt>

1366 (0x556)
</dt> <dt>



Идентификатор сеанса входа уже используется.


</dt> </dl> </dd> <dt>

<span id="ERROR_INVALID_LOGON_TYPE"></span><span id="error_invalid_logon_type"></span>**Ошибка \_ недопустимого \_ \_ типа входа**
</dt> <dd> <dl> <dt>

1367 (0x557)
</dt> <dt>



Запрос на вход в систему содержал недопустимое значение типа входа.


</dt> </dl> </dd> <dt>

<span id="ERROR_CANNOT_IMPERSONATE"></span><span id="error_cannot_impersonate"></span>**Ошибка \_ не может \_ олицетворить**
</dt> <dd> <dl> <dt>

1368 (0x558)
</dt> <dt>



Невозможно выполнить олицетворение с помощью именованного канала, пока данные не считаны из этого канала.


</dt> </dl> </dd> <dt>

<span id="ERROR_RXACT_INVALID_STATE"></span><span id="error_rxact_invalid_state"></span>**Ошибка \_ рксакт \_ недопустимое \_ состояние**
</dt> <dd> <dl> <dt>

1369 (0x559)
</dt> <dt>



Состояние транзакции поддерева реестра несовместимо с запрошенной операцией.


</dt> </dl> </dd> <dt>

<span id="ERROR_RXACT_COMMIT_FAILURE"></span><span id="error_rxact_commit_failure"></span>**Ошибка \_ \_ при фиксации рксакт \_**
</dt> <dd> <dl> <dt>

1370 (0x55A)
</dt> <dt>



Обнаружено повреждение внутренней базы данных безопасности.


</dt> </dl> </dd> <dt>

<span id="ERROR_SPECIAL_ACCOUNT"></span><span id="error_special_account"></span>**\_Специальная \_ учетная запись ошибки**
</dt> <dd> <dl> <dt>

1371 (0x55B)
</dt> <dt>



Невозможно выполнить эту операцию с встроенными учетными записями.


</dt> </dl> </dd> <dt>

<span id="ERROR_SPECIAL_GROUP"></span><span id="error_special_group"></span>**\_Специальная \_ Группа ошибок**
</dt> <dd> <dl> <dt>

1372 (0x55C)
</dt> <dt>



Невозможно выполнить эту операцию с этой встроенной специальной группой.


</dt> </dl> </dd> <dt>

<span id="ERROR_SPECIAL_USER"></span><span id="error_special_user"></span>**\_Специальный \_ пользователь ошибок**
</dt> <dd> <dl> <dt>

1373 (0x55D)
</dt> <dt>



Невозможно выполнить эту операцию с этим встроенным пользователем.


</dt> </dl> </dd> <dt>

<span id="ERROR_MEMBERS_PRIMARY_GROUP"></span><span id="error_members_primary_group"></span>**\_ \_ Основная группа участников \_ с ошибками**
</dt> <dd> <dl> <dt>

1374 (0x55E)
</dt> <dt>



Невозможно удалить пользователя из группы, так как эта группа в настоящее время является основной группой пользователя.


</dt> </dl> </dd> <dt>

<span id="ERROR_TOKEN_ALREADY_IN_USE"></span><span id="error_token_already_in_use"></span>**\_маркер ошибки \_ уже \_ \_ используется**
</dt> <dd> <dl> <dt>

1375 (0x55F)
</dt> <dt>



Токен уже используется в качестве основного токена.


</dt> </dl> </dd> <dt>

<span id="ERROR_NO_SUCH_ALIAS"></span><span id="error_no_such_alias"></span>**Ошибка \_ без \_ \_ псевдонима**
</dt> <dd> <dl> <dt>

1376 (0x560)
</dt> <dt>



Указанная локальная группа не существует.


</dt> </dl> </dd> <dt>

<span id="ERROR_MEMBER_NOT_IN_ALIAS"></span><span id="error_member_not_in_alias"></span>**\_элемент ошибки \_ не \_ в \_ псевдониме**
</dt> <dd> <dl> <dt>

1377 (0x561)
</dt> <dt>



Указанное имя учетной записи не является членом группы.


</dt> </dl> </dd> <dt>

<span id="ERROR_MEMBER_IN_ALIAS"></span><span id="error_member_in_alias"></span>**\_элемент ошибки \_ в \_ псевдониме**
</dt> <dd> <dl> <dt>

1378 (0x562)
</dt> <dt>



Указанное имя учетной записи уже является членом группы.


</dt> </dl> </dd> <dt>

<span id="ERROR_ALIAS_EXISTS"></span><span id="error_alias_exists"></span>**\_псевдоним ошибки \_ существует**
</dt> <dd> <dl> <dt>

1379 (0x563)
</dt> <dt>



Указанная локальная группа уже существует.


</dt> </dl> </dd> <dt>

<span id="ERROR_LOGON_NOT_GRANTED"></span><span id="error_logon_not_granted"></span>**Ошибка \_ входа в систему \_ не \_ предоставлена**
</dt> <dd> <dl> <dt>

1380 (0x564)
</dt> <dt>



Ошибка входа в систему: пользователю не был предоставлен запрошенный тип входа на этом компьютере.


</dt> </dl> </dd> <dt>

<span id="ERROR_TOO_MANY_SECRETS"></span><span id="error_too_many_secrets"></span>**Ошибка \_ слишком \_ много \_ секретов**
</dt> <dd> <dl> <dt>

1381 (0x565)
</dt> <dt>



Превышено максимальное число секретов, которые могут храниться в одной системе.


</dt> </dl> </dd> <dt>

<span id="ERROR_SECRET_TOO_LONG"></span><span id="error_secret_too_long"></span>**\_секретный код ошибки \_ слишком \_ длинный**
</dt> <dd> <dl> <dt>

1382 (0x566)
</dt> <dt>



Длина секрета превышает максимально допустимую.


</dt> </dl> </dd> <dt>

<span id="ERROR_INTERNAL_DB_ERROR"></span><span id="error_internal_db_error"></span>**Ошибка \_ внутренней \_ ошибки базы данных \_**
</dt> <dd> <dl> <dt>

1383 (0x567)
</dt> <dt>



Локальная база данных центра безопасности содержит внутреннюю несогласованность.


</dt> </dl> </dd> <dt>

<span id="ERROR_TOO_MANY_CONTEXT_IDS"></span><span id="error_too_many_context_ids"></span>**Ошибка \_ слишком \_ много \_ \_ идентификаторов контекста**
</dt> <dd> <dl> <dt>

1384 (0x568)
</dt> <dt>



Во время попытки входа в систему контекст безопасности пользователя накапливает слишком много идентификаторов безопасности.


</dt> </dl> </dd> <dt>

<span id="ERROR_LOGON_TYPE_NOT_GRANTED"></span><span id="error_logon_type_not_granted"></span>**\_тип ошибки \_ входа \_ не \_ предоставлен**
</dt> <dd> <dl> <dt>

1385 (0x569)
</dt> <dt>



Ошибка входа в систему: пользователю не был предоставлен запрошенный тип входа на этом компьютере.


</dt> </dl> </dd> <dt>

<span id="ERROR_NT_CROSS_ENCRYPTION_REQUIRED"></span><span id="error_nt_cross_encryption_required"></span>**Ошибка \_ при \_ перекрестном \_ шифровании NT \_**
</dt> <dd> <dl> <dt>

1386 (0x56A)
</dt> <dt>



Для изменения пароля пользователя требуется перекрестно зашифрованный пароль.


</dt> </dl> </dd> <dt>

<span id="ERROR_NO_SUCH_MEMBER"></span><span id="error_no_such_member"></span>**Ошибка \_ без \_ такого \_ участника**
</dt> <dd> <dl> <dt>

1387 (0x56B)
</dt> <dt>



Не удалось добавить или удалить элемент из локальной группы, так как элемент не существует.


</dt> </dl> </dd> <dt>

<span id="ERROR_INVALID_MEMBER"></span><span id="error_invalid_member"></span>**Ошибка \_ недопустимого \_ члена**
</dt> <dd> <dl> <dt>

1388 (0x56C)
</dt> <dt>



Не удалось добавить нового члена в локальную группу, так как у него неправильный тип учетной записи.


</dt> </dl> </dd> <dt>

<span id="ERROR_TOO_MANY_SIDS"></span><span id="error_too_many_sids"></span>**Ошибка \_ слишком \_ большого числа \_ идентификаторов безопасности**
</dt> <dd> <dl> <dt>

1389 (0x56D)
</dt> <dt>



Указано слишком много идентификаторов безопасности.


</dt> </dl> </dd> <dt>

<span id="ERROR_LM_CROSS_ENCRYPTION_REQUIRED"></span><span id="error_lm_cross_encryption_required"></span>**Ошибка \_ при \_ перекрестном \_ шифровании LM \_**
</dt> <dd> <dl> <dt>

1390 (0x56E)
</dt> <dt>



Для изменения этого пароля пользователя требуется перекрестно зашифрованный пароль.


</dt> </dl> </dd> <dt>

<span id="ERROR_NO_INHERITANCE"></span><span id="error_no_inheritance"></span>**Ошибка \_ без \_ наследования**
</dt> <dd> <dl> <dt>

1391 (0x56F)
</dt> <dt>



Указывает, что список ACL не содержит наследуемых компонентов.


</dt> </dl> </dd> <dt>

<span id="ERROR_FILE_CORRUPT"></span><span id="error_file_corrupt"></span>**\_файл ошибок \_ поврежден**
</dt> <dd> <dl> <dt>

1392 (0x570)
</dt> <dt>



Файл или каталог поврежден и не читается.


</dt> </dl> </dd> <dt>

<span id="ERROR_DISK_CORRUPT"></span><span id="error_disk_corrupt"></span>**диск с ошибкой \_ \_ поврежден**
</dt> <dd> <dl> <dt>

1393 (0x571)
</dt> <dt>



Структура диска повреждена и недоступна для чтения.


</dt> </dl> </dd> <dt>

<span id="ERROR_NO_USER_SESSION_KEY"></span><span id="error_no_user_session_key"></span>**Ошибка \_ без \_ \_ ключа сеанса \_ пользователя**
</dt> <dd> <dl> <dt>

1394 (0x572)
</dt> <dt>



Для указанного сеанса входа в систему не существует ключа сеанса пользователя.


</dt> </dl> </dd> <dt>

<span id="ERROR_LICENSE_QUOTA_EXCEEDED"></span><span id="error_license_quota_exceeded"></span>**\_ \_ превышена квота лицензии на ошибку \_**
</dt> <dd> <dl> <dt>

1395 (0x573)
</dt> <dt>



Служба, к которой осуществляется доступ, лицензирована для определенного числа подключений. В настоящее время невозможно установить больше подключений, так как служба уже может принять такое количество подключений.


</dt> </dl> </dd> <dt>

<span id="ERROR_WRONG_TARGET_NAME"></span><span id="error_wrong_target_name"></span>**Ошибка \_ неправильного \_ имени целевого объекта \_**
</dt> <dd> <dl> <dt>

1396 (0x574)
</dt> <dt>



Неверное имя целевой учетной записи.


</dt> </dl> </dd> <dt>

<span id="ERROR_MUTUAL_AUTH_FAILED"></span><span id="error_mutual_auth_failed"></span>**Ошибка \_ взаимной \_ проверки подлинности \_**
</dt> <dd> <dl> <dt>

1397 (0x575)
</dt> <dt>



Сбой взаимной проверки подлинности. Пароль сервера устарел на контроллере домена.


</dt> </dl> </dd> <dt>

<span id="ERROR_TIME_SKEW"></span><span id="error_time_skew"></span>**\_ \_ Отклонение времени ошибки**
</dt> <dd> <dl> <dt>

1398 (0x576)
</dt> <dt>



Между клиентом и сервером существует разница между временем и (или) датой.


</dt> </dl> </dd> <dt>

<span id="ERROR_CURRENT_DOMAIN_NOT_ALLOWED"></span><span id="error_current_domain_not_allowed"></span>**Ошибка \_ текущего \_ домена \_ не \_ разрешена**
</dt> <dd> <dl> <dt>

1399 (0x577)
</dt> <dt>



Эта операция не может быть выполнена в текущем домене.


</dt> </dl> </dd> <dt>

<span id="ERROR_INVALID_WINDOW_HANDLE"></span><span id="error_invalid_window_handle"></span>**Ошибка \_ неправильного \_ \_ обработчика окна**
</dt> <dd> <dl> <dt>

1400 (0x578)
</dt> <dt>



Недопустимый маркер окна.


</dt> </dl> </dd> <dt>

<span id="ERROR_INVALID_MENU_HANDLE"></span><span id="error_invalid_menu_handle"></span>**Ошибка \_ недопустимого \_ \_ маркера меню**
</dt> <dd> <dl> <dt>

1401 (0x579)
</dt> <dt>



Недопустимый маркер меню.


</dt> </dl> </dd> <dt>

<span id="ERROR_INVALID_CURSOR_HANDLE"></span><span id="error_invalid_cursor_handle"></span>**Ошибка \_ недопустимого \_ \_ маркера курсора**
</dt> <dd> <dl> <dt>

1402 (0x57A)
</dt> <dt>



Недопустимый маркер курсора.


</dt> </dl> </dd> <dt>

<span id="ERROR_INVALID_ACCEL_HANDLE"></span><span id="error_invalid_accel_handle"></span>**Ошибка \_ недопустимого \_ \_ обработчика обращений**
</dt> <dd> <dl> <dt>

1403 (0x57B)
</dt> <dt>



Недопустимый маркер таблицы ускорителя.


</dt> </dl> </dd> <dt>

<span id="ERROR_INVALID_HOOK_HANDLE"></span><span id="error_invalid_hook_handle"></span>**Ошибка \_ недопустимого обработчика \_ обработчика \_**
</dt> <dd> <dl> <dt>

1404 (0x57C)
</dt> <dt>



Недопустимый обработчик обработчика.


</dt> </dl> </dd> <dt>

<span id="ERROR_INVALID_DWP_HANDLE"></span><span id="error_invalid_dwp_handle"></span>**Ошибка при \_ недопустимом \_ \_ обработчике DWP**
</dt> <dd> <dl> <dt>

1405 (0x57D)
</dt> <dt>



Недопустимый указатель на структуру расположения с несколькими окнами.


</dt> </dl> </dd> <dt>

<span id="ERROR_TLW_WITH_WSCHILD"></span><span id="error_tlw_with_wschild"></span>**Ошибка \_ ТЛВ \_ с \_ всчилд**
</dt> <dd> <dl> <dt>

1406 (0x57E)
</dt> <dt>



Не удается создать дочернее окно верхнего уровня.


</dt> </dl> </dd> <dt>

<span id="ERROR_CANNOT_FIND_WND_CLASS"></span><span id="error_cannot_find_wnd_class"></span>**Ошибка \_ не \_ удается \_ найти \_ класс ВНД**
</dt> <dd> <dl> <dt>

1407 (0x57F)
</dt> <dt>



Не удается найти класс окна.


</dt> </dl> </dd> <dt>

<span id="ERROR_WINDOW_OF_OTHER_THREAD"></span><span id="error_window_of_other_thread"></span>**\_окно ошибок \_ \_ другого \_ потока**
</dt> <dd> <dl> <dt>

1408 (0x580)
</dt> <dt>



Недопустимое окно; Он принадлежит другому потоку.


</dt> </dl> </dd> <dt>

<span id="ERROR_HOTKEY_ALREADY_REGISTERED"></span><span id="error_hotkey_already_registered"></span>**\_горячая клавиша ошибки \_ уже \_ зарегистрирована**
</dt> <dd> <dl> <dt>

1409 (0X581)
</dt> <dt>



Горячая клавиша уже зарегистрирована.


</dt> </dl> </dd> <dt>

<span id="ERROR_CLASS_ALREADY_EXISTS"></span><span id="error_class_already_exists"></span>**\_класс Error \_ уже \_ существует**
</dt> <dd> <dl> <dt>

1410 (0x582)
</dt> <dt>



Класс уже существует.


</dt> </dl> </dd> <dt>

<span id="ERROR_CLASS_DOES_NOT_EXIST"></span><span id="error_class_does_not_exist"></span>**\_класс Error \_ \_ не \_ существует**
</dt> <dd> <dl> <dt>

1411 (0x583)
</dt> <dt>



Класс не существует.


</dt> </dl> </dd> <dt>

<span id="ERROR_CLASS_HAS_WINDOWS"></span><span id="error_class_has_windows"></span>**\_класс Error \_ содержит \_ Windows**
</dt> <dd> <dl> <dt>

1412 (0x584)
</dt> <dt>



Класс по-прежнему имеет открытые окна.


</dt> </dl> </dd> <dt>

<span id="ERROR_INVALID_INDEX"></span><span id="error_invalid_index"></span>**Ошибка \_ недопустимого \_ индекса**
</dt> <dd> <dl> <dt>

1413 (0x585)
</dt> <dt>



Недопустимый индекс.


</dt> </dl> </dd> <dt>

<span id="ERROR_INVALID_ICON_HANDLE"></span><span id="error_invalid_icon_handle"></span>**Ошибка \_ неправильного \_ \_ маркера значка**
</dt> <dd> <dl> <dt>

1414 (0x586)
</dt> <dt>



Недопустимый маркер значка.


</dt> </dl> </dd> <dt>

<span id="ERROR_PRIVATE_DIALOG_INDEX"></span><span id="error_private_dialog_index"></span>**Ошибка при \_ закрытии \_ индекса диалогового окна \_**
</dt> <dd> <dl> <dt>

1415 (0x587)
</dt> <dt>



Использование закрытых слов в ДИАЛОГовых окнах.


</dt> </dl> </dd> <dt>

<span id="ERROR_LISTBOX_ID_NOT_FOUND"></span><span id="error_listbox_id_not_found"></span>**\_идентификатор списка \_ ошибок \_ не \_ найден**
</dt> <dd> <dl> <dt>

1416 (0x588)
</dt> <dt>



Идентификатор списка не найден.


</dt> </dl> </dd> <dt>

<span id="ERROR_NO_WILDCARD_CHARACTERS"></span><span id="error_no_wildcard_characters"></span>**Ошибка \_ без \_ подстановочных \_ знаков**
</dt> <dd> <dl> <dt>

1417 (0x589)
</dt> <dt>



Подстановочные знаки не найдены.


</dt> </dl> </dd> <dt>

<span id="ERROR_CLIPBOARD_NOT_OPEN"></span><span id="error_clipboard_not_open"></span>**\_буфер обмена ошибок \_ не \_ открыт**
</dt> <dd> <dl> <dt>

1418 (0x58A)
</dt> <dt>



В потоке не открыт буфер обмена.


</dt> </dl> </dd> <dt>

<span id="ERROR_HOTKEY_NOT_REGISTERED"></span><span id="error_hotkey_not_registered"></span>**\_ \_ не \_ зарегистрировано сочетание клавиш для ошибки**
</dt> <dd> <dl> <dt>

1419 (0x58B)
</dt> <dt>



Горячая клавиша не зарегистрирована.


</dt> </dl> </dd> <dt>

<span id="ERROR_WINDOW_NOT_DIALOG"></span><span id="error_window_not_dialog"></span>**окно "ошибка" \_ \_ не \_ диалоговое окно**
</dt> <dd> <dl> <dt>

1420 (0x58C)
</dt> <dt>



Окно не является допустимым окном диалогового окна.


</dt> </dl> </dd> <dt>

<span id="ERROR_CONTROL_ID_NOT_FOUND"></span><span id="error_control_id_not_found"></span>**\_идентификатор управления ошибками \_ \_ не \_ найден**
</dt> <dd> <dl> <dt>

1421 (0x58D)
</dt> <dt>



Идентификатор элемента управления не найден.


</dt> </dl> </dd> <dt>

<span id="ERROR_INVALID_COMBOBOX_MESSAGE"></span><span id="error_invalid_combobox_message"></span>**Ошибка \_ недопустимого \_ \_ сообщения ComboBox**
</dt> <dd> <dl> <dt>

1422 (0x58E)
</dt> <dt>



Недопустимое сообщение для поля со списком, так как оно не имеет элемента управления "поле ввода".


</dt> </dl> </dd> <dt>

<span id="ERROR_WINDOW_NOT_COMBOBOX"></span><span id="error_window_not_combobox"></span>**\_окно ошибок \_ не \_ ComboBox**
</dt> <dd> <dl> <dt>

1423 (0x58F)
</dt> <dt>



Окно не является полем со списком.


</dt> </dl> </dd> <dt>

<span id="ERROR_INVALID_EDIT_HEIGHT"></span><span id="error_invalid_edit_height"></span>**Ошибка \_ при \_ изменении \_ высоты**
</dt> <dd> <dl> <dt>

1424 (0x590)
</dt> <dt>



Высота должна быть меньше 256.


</dt> </dl> </dd> <dt>

<span id="ERROR_DC_NOT_FOUND"></span><span id="error_dc_not_found"></span>**Ошибка \_ DC \_ не \_ найдена**
</dt> <dd> <dl> <dt>

1425 (0x591)
</dt> <dt>



Недопустимый обработчик контекста устройства (DC).


</dt> </dl> </dd> <dt>

<span id="ERROR_INVALID_HOOK_FILTER"></span><span id="error_invalid_hook_filter"></span>**Ошибка \_ недопустимого \_ фильтра обработчика \_**
</dt> <dd> <dl> <dt>

1426 (0x592)
</dt> <dt>



Недопустимый тип процедуры обработчика.


</dt> </dl> </dd> <dt>

<span id="ERROR_INVALID_FILTER_PROC"></span><span id="error_invalid_filter_proc"></span>**Ошибка при \_ неправильной \_ \_ процедуре фильтра**
</dt> <dd> <dl> <dt>

1427 (0x593)
</dt> <dt>



Недопустимая процедура обработчика.


</dt> </dl> </dd> <dt>

<span id="ERROR_HOOK_NEEDS_HMOD"></span><span id="error_hook_needs_hmod"></span>**для \_ обработчика ошибок \_ требуются \_ хмод**
</dt> <dd> <dl> <dt>

1428 (0x594)
</dt> <dt>



Невозможно задать нелокальный обработчик без обработчика модуля.


</dt> </dl> </dd> <dt>

<span id="ERROR_GLOBAL_ONLY_HOOK"></span><span id="error_global_only_hook"></span>**Ошибка \_ \_ только глобального \_ ловушки**
</dt> <dd> <dl> <dt>

1429 (0x595)
</dt> <dt>



Эту процедуру-обработчик можно установить только глобально.


</dt> </dl> </dd> <dt>

<span id="ERROR_JOURNAL_HOOK_SET"></span><span id="error_journal_hook_set"></span>**\_ \_ набор обработчиков журнала ошибок \_**
</dt> <dd> <dl> <dt>

1430 (0x596)
</dt> <dt>



Процедура обработчика журнала уже установлена.


</dt> </dl> </dd> <dt>

<span id="ERROR_HOOK_NOT_INSTALLED"></span><span id="error_hook_not_installed"></span>**\_обработчик ошибок \_ не \_ установлен**
</dt> <dd> <dl> <dt>

1431 (0x597)
</dt> <dt>



Процедура-обработчик не установлена.


</dt> </dl> </dd> <dt>

<span id="ERROR_INVALID_LB_MESSAGE"></span><span id="error_invalid_lb_message"></span>**Ошибка \_ недопустимого \_ сообщения о балансировке нагрузки \_**
</dt> <dd> <dl> <dt>

1432 (0x598)
</dt> <dt>



Недопустимое сообщение для списка с одним выбором.


</dt> </dl> </dd> <dt>

<span id="ERROR_SETCOUNT_ON_BAD_LB"></span><span id="error_setcount_on_bad_lb"></span>**Ошибка \_ сеткаунт \_ при \_ плохой \_ балансировке нагрузки**
</dt> <dd> <dl> <dt>

1433 (0x599)
</dt> <dt>



Балансировка нагрузки \_ сеткаунт, отправленная в список не ленивых.


</dt> </dl> </dd> <dt>

<span id="ERROR_LB_WITHOUT_TABSTOPS"></span><span id="error_lb_without_tabstops"></span>**Ошибка при \_ балансировке нагрузки \_ без \_ табуляцию**
</dt> <dd> <dl> <dt>

1434 (0x59A)
</dt> <dt>



Это окно списка не поддерживает позиции табуляции.


</dt> </dl> </dd> <dt>

<span id="ERROR_DESTROY_OBJECT_OF_OTHER_THREAD"></span><span id="error_destroy_object_of_other_thread"></span>**Ошибка \_ при \_ удалении \_ объекта \_ другого \_ потока**
</dt> <dd> <dl> <dt>

1435 (0x59B)
</dt> <dt>



Невозможно уничтожить объект, созданный другим потоком.


</dt> </dl> </dd> <dt>

<span id="ERROR_CHILD_WINDOW_MENU"></span><span id="error_child_window_menu"></span>**\_меню дочернего \_ окна ошибок \_**
</dt> <dd> <dl> <dt>

1436 (0x59C)
</dt> <dt>



Дочерние окна не могут иметь меню.


</dt> </dl> </dd> <dt>

<span id="ERROR_NO_SYSTEM_MENU"></span><span id="error_no_system_menu"></span>**Ошибка \_ нет \_ системного \_ меню**
</dt> <dd> <dl> <dt>

1437 (0x59D)
</dt> <dt>



Окно не имеет системного меню.


</dt> </dl> </dd> <dt>

<span id="ERROR_INVALID_MSGBOX_STYLE"></span><span id="error_invalid_msgbox_style"></span>**Ошибка \_ недопустимого \_ \_ стиля MSGBOX**
</dt> <dd> <dl> <dt>

1438 (0x59E)
</dt> <dt>



Недопустимый стиль окна сообщения.


</dt> </dl> </dd> <dt>

<span id="ERROR_INVALID_SPI_VALUE"></span><span id="error_invalid_spi_value"></span>**Ошибка \_ недопустимого \_ \_ значения SPI**
</dt> <dd> <dl> <dt>

1439 (0x59F)
</dt> <dt>



Недопустимый параметр на уровне системы (SPI \_ \* ).


</dt> </dl> </dd> <dt>

<span id="ERROR_SCREEN_ALREADY_LOCKED"></span><span id="error_screen_already_locked"></span>**\_экран ошибок \_ уже \_ заблокирован**
</dt> <dd> <dl> <dt>

1440 (0x5A0)
</dt> <dt>



Экран уже заблокирован.


</dt> </dl> </dd> <dt>

<span id="ERROR_HWNDS_HAVE_DIFF_PARENT"></span><span id="error_hwnds_have_diff_parent"></span>**\_HWND ошибки \_ имеют \_ \_ родительский элемент diff**
</dt> <dd> <dl> <dt>

1441 (0x5A1)
</dt> <dt>



Все дескрипторы окон в структуре расположения с несколькими окнами должны иметь один и тот же родительский элемент.


</dt> </dl> </dd> <dt>

<span id="ERROR_NOT_CHILD_WINDOW"></span><span id="error_not_child_window"></span>**Ошибка \_ не \_ дочернего \_ окна**
</dt> <dd> <dl> <dt>

1442 (0x5A2)
</dt> <dt>



Окно не является дочерним окном.


</dt> </dl> </dd> <dt>

<span id="ERROR_INVALID_GW_COMMAND"></span><span id="error_invalid_gw_command"></span>**Ошибка \_ недопустимой \_ \_ команды GW**
</dt> <dd> <dl> <dt>

1443 (0x5A3)
</dt> <dt>



Недопустимая \_ \* команда GW.


</dt> </dl> </dd> <dt>

<span id="ERROR_INVALID_THREAD_ID"></span><span id="error_invalid_thread_id"></span>**Ошибка \_ недопустимого \_ \_ идентификатора потока**
</dt> <dd> <dl> <dt>

1444 (0x5A4)
</dt> <dt>



Недопустимый идентификатор потока.


</dt> </dl> </dd> <dt>

<span id="ERROR_NON_MDICHILD_WINDOW"></span><span id="error_non_mdichild_window"></span>**ОШИБКА, \_ не \_ мдичилд \_ окно**
</dt> <dd> <dl> <dt>

1445 (0x5A5)
</dt> <dt>



Невозможно обработать сообщение из окна, которое не является окном многодокументного интерфейса (MDI).


</dt> </dl> </dd> <dt>

<span id="ERROR_POPUP_ALREADY_ACTIVE"></span><span id="error_popup_already_active"></span>**\_всплывающее окно ошибки \_ уже \_ активно**
</dt> <dd> <dl> <dt>

1446 (0x5A6)
</dt> <dt>



Всплывающее меню уже активно.


</dt> </dl> </dd> <dt>

<span id="ERROR_NO_SCROLLBARS"></span><span id="error_no_scrollbars"></span>**Ошибка \_ без \_ полос прокрутки**
</dt> <dd> <dl> <dt>

1447 (0x5A7)
</dt> <dt>



Окно не имеет полос прокрутки.


</dt> </dl> </dd> <dt>

<span id="ERROR_INVALID_SCROLLBAR_RANGE"></span><span id="error_invalid_scrollbar_range"></span>**Ошибка \_ недопустимого \_ диапазона полосы прокрутки \_**
</dt> <dd> <dl> <dt>

1448 (0x5A8)
</dt> <dt>



Диапазон полосы прокрутки не может быть больше МАКСЛОНГ.


</dt> </dl> </dd> <dt>

<span id="ERROR_INVALID_SHOWWIN_COMMAND"></span><span id="error_invalid_showwin_command"></span>**Ошибка \_ недопустимой \_ \_ команды шоввин**
</dt> <dd> <dl> <dt>

1449 (0x5A9)
</dt> <dt>



Невозможно отобразить или удалить окно указанным способом.


</dt> </dl> </dd> <dt>

<span id="ERROR_NO_SYSTEM_RESOURCES"></span><span id="error_no_system_resources"></span>**\_нет \_ системных \_ ресурсов**
</dt> <dd> <dl> <dt>

1450 (0x5AA)
</dt> <dt>



Недостаточно системных ресурсов для завершения запрошенной службы.


</dt> </dl> </dd> <dt>

<span id="ERROR_NONPAGED_SYSTEM_RESOURCES"></span><span id="error_nonpaged_system_resources"></span>**ОШИБКИ \_ НЕстраничных \_ системных \_ ресурсов**
</dt> <dd> <dl> <dt>

1451 (0x5AB)
</dt> <dt>



Недостаточно системных ресурсов для завершения запрошенной службы.


</dt> </dl> </dd> <dt>

<span id="ERROR_PAGED_SYSTEM_RESOURCES"></span><span id="error_paged_system_resources"></span>**ОШИБКИ в \_ \_ системных \_ ресурсах**
</dt> <dd> <dl> <dt>

1452 (0x5AC)
</dt> <dt>



Недостаточно системных ресурсов для завершения запрошенной службы.


</dt> </dl> </dd> <dt>

<span id="ERROR_WORKING_SET_QUOTA"></span><span id="error_working_set_quota"></span>**Ошибка \_ в \_ \_ квоте рабочего набора**
</dt> <dd> <dl> <dt>

1453 (0x5AD)
</dt> <dt>



Недостаточно квоты для завершения запрошенной службы.


</dt> </dl> </dd> <dt>

<span id="ERROR_PAGEFILE_QUOTA"></span><span id="error_pagefile_quota"></span>**\_Квота файла подкачки с ошибками \_**
</dt> <dd> <dl> <dt>

1454 (0x5AE)
</dt> <dt>



Недостаточно квоты для завершения запрошенной службы.


</dt> </dl> </dd> <dt>

<span id="ERROR_COMMITMENT_LIMIT"></span><span id="error_commitment_limit"></span>**\_лимит обязательств по ошибке \_**
</dt> <dd> <dl> <dt>

1455 (0x5AF)
</dt> <dt>



Файл подкачки слишком мал для завершения этой операции.


</dt> </dl> </dd> <dt>

<span id="ERROR_MENU_ITEM_NOT_FOUND"></span><span id="error_menu_item_not_found"></span>**пункт меню "ошибка" \_ \_ \_ не \_ найден**
</dt> <dd> <dl> <dt>

1456 (0x5B0)
</dt> <dt>



Не удалось найти пункт меню.


</dt> </dl> </dd> <dt>

<span id="ERROR_INVALID_KEYBOARD_HANDLE"></span><span id="error_invalid_keyboard_handle"></span>**Ошибка \_ недопустимого \_ \_ маркера клавиатуры**
</dt> <dd> <dl> <dt>

1457 (0x5B1)
</dt> <dt>



Недопустимый маркер раскладки клавиатуры.


</dt> </dl> </dd> <dt>

<span id="ERROR_HOOK_TYPE_NOT_ALLOWED"></span><span id="error_hook_type_not_allowed"></span>**\_тип обработчика ошибок \_ \_ не \_ разрешен**
</dt> <dd> <dl> <dt>

1458 (0x5B2)
</dt> <dt>



Тип обработчика не разрешен.


</dt> </dl> </dd> <dt>

<span id="ERROR_REQUIRES_INTERACTIVE_WINDOWSTATION"></span><span id="error_requires_interactive_windowstation"></span>**для ошибки \_ требуется \_ Interactive \_ виндовстатион**
</dt> <dd> <dl> <dt>

1459 (0x5B3)
</dt> <dt>



Для этой операции требуется интерактивная Командная станция.


</dt> </dl> </dd> <dt>

<span id="ERROR_TIMEOUT"></span><span id="error_timeout"></span>**\_время ожидания ошибки**
</dt> <dd> <dl> <dt>

1460 (0x5B4)
</dt> <dt>



Эта операция возвращена, так как истек период ожидания.


</dt> </dl> </dd> <dt>

<span id="ERROR_INVALID_MONITOR_HANDLE"></span><span id="error_invalid_monitor_handle"></span>**Ошибка \_ неправильного \_ \_ обработчика монитора**
</dt> <dd> <dl> <dt>

1461 (0x5B5)
</dt> <dt>



Недопустимый обработчик монитора.


</dt> </dl> </dd> <dt>

<span id="ERROR_INCORRECT_SIZE"></span><span id="error_incorrect_size"></span>**Ошибка \_ неправильного \_ размера**
</dt> <dd> <dl> <dt>

1462 (0x5B6)
</dt> <dt>



Недопустимый аргумент размера.


</dt> </dl> </dd> <dt>

<span id="ERROR_SYMLINK_CLASS_DISABLED"></span><span id="error_symlink_class_disabled"></span>**Ошибка \_ символьную ссылку, \_ класс \_ отключен**
</dt> <dd> <dl> <dt>

1463 (0x5B7)
</dt> <dt>



Невозможно проследить символьную ссылку, так как ее тип отключен.


</dt> </dl> </dd> <dt>

<span id="ERROR_SYMLINK_NOT_SUPPORTED"></span><span id="error_symlink_not_supported"></span>**Ошибка \_ символьную ссылку \_ не \_ поддерживается**
</dt> <dd> <dl> <dt>

1464 (0x5B8)
</dt> <dt>



Это приложение не поддерживает текущую операцию с символической ссылкой.


</dt> </dl> </dd> <dt>

<span id="ERROR_XML_PARSE_ERROR"></span><span id="error_xml_parse_error"></span>**Ошибка \_ \_ синтаксического анализа XML-кода ошибки \_**
</dt> <dd> <dl> <dt>

1465 (0x5B9)
</dt> <dt>



Windows не удалось выполнить синтаксический анализ запрошенных XML-данных.


</dt> </dl> </dd> <dt>

<span id="ERROR_XMLDSIG_ERROR"></span><span id="error_xmldsig_error"></span>**Ошибка \_ XMLDSIG \_**
</dt> <dd> <dl> <dt>

1466 (0x5BA)
</dt> <dt>



При обработке цифровой подписи XML произошла ошибка.


</dt> </dl> </dd> <dt>

<span id="ERROR_RESTART_APPLICATION"></span><span id="error_restart_application"></span>**Ошибка при \_ перезапуске \_ приложения**
</dt> <dd> <dl> <dt>

1467 (0x5BB)
</dt> <dt>



Это приложение необходимо перезапустить.


</dt> </dl> </dd> <dt>

<span id="ERROR_WRONG_COMPARTMENT"></span><span id="error_wrong_compartment"></span>**Ошибка \_ неверной \_ Секции**
</dt> <dd> <dl> <dt>

1468 (0x5BC)
</dt> <dt>



Вызывающий объект сделал запрос на подключение в неверном сегменте маршрутизации.


</dt> </dl> </dd> <dt>

<span id="ERROR_AUTHIP_FAILURE"></span><span id="error_authip_failure"></span>**Ошибка \_ AUTHIP \_**
</dt> <dd> <dl> <dt>

1469 (0x5BD)
</dt> <dt>



Сбой AuthIP при попытке подключения к удаленному узлу.


</dt> </dl> </dd> <dt>

<span id="ERROR_NO_NVRAM_RESOURCES"></span><span id="error_no_nvram_resources"></span>**Ошибка \_ при \_ отсутствии \_ ресурсов NVRAM**
</dt> <dd> <dl> <dt>

1470 (0x5BE)
</dt> <dt>



Недостаточно ресурсов NVRAM для завершения запрошенной службы. Может потребоваться перезагрузка.


</dt> </dl> </dd> <dt>

<span id="ERROR_NOT_GUI_PROCESS"></span><span id="error_not_gui_process"></span>**Ошибка \_ при \_ обработке графического пользовательского интерфейса \_**
</dt> <dd> <dl> <dt>

1471 (0x5BF)
</dt> <dt>



Не удалось завершить запрошенную операцию, поскольку указанный процесс не является процессом графического пользовательского интерфейса.


</dt> </dl> </dd> <dt>

<span id="ERROR_EVENTLOG_FILE_CORRUPT"></span><span id="error_eventlog_file_corrupt"></span>**\_файл журнала \_ ошибок \_ поврежден**
</dt> <dd> <dl> <dt>

1500 (0x5DC)
</dt> <dt>



Файл журнала событий поврежден.


</dt> </dl> </dd> <dt>

<span id="ERROR_EVENTLOG_CANT_START"></span><span id="error_eventlog_cant_start"></span>**не \_ \_ удается \_ запустить журнал событий ошибок**
</dt> <dd> <dl> <dt>

1501 (0x5DD)
</dt> <dt>



Не удалось открыть файл журнала событий, поэтому служба ведения журнала событий не запустилась.


</dt> </dl> </dd> <dt>

<span id="ERROR_LOG_FILE_FULL"></span><span id="error_log_file_full"></span>**\_ \_ переполнение файла журнала ошибок \_**
</dt> <dd> <dl> <dt>

1502 (0x5DE)
</dt> <dt>



Файл журнала событий заполнен.


</dt> </dl> </dd> <dt>

<span id="ERROR_EVENTLOG_FILE_CHANGED"></span><span id="error_eventlog_file_changed"></span>**\_файл журнала \_ ошибок \_ изменен**
</dt> <dd> <dl> <dt>

1503 (0x5DF)
</dt> <dt>



Файл журнала событий изменился между операциями чтения.


</dt> </dl> </dd> <dt>

<span id="ERROR_INVALID_TASK_NAME"></span><span id="error_invalid_task_name"></span>**Ошибка \_ недопустимое \_ \_ имя задачи**
</dt> <dd> <dl> <dt>

1550 (0x60E)
</dt> <dt>



Указано недопустимое имя задачи.


</dt> </dl> </dd> <dt>

<span id="ERROR_INVALID_TASK_INDEX"></span><span id="error_invalid_task_index"></span>**Ошибка при \_ недопустимом \_ \_ индексе задачи**
</dt> <dd> <dl> <dt>

1551 (0x60F)
</dt> <dt>



Указан недопустимый индекс задачи.


</dt> </dl> </dd> <dt>

<span id="ERROR_THREAD_ALREADY_IN_TASK"></span><span id="error_thread_already_in_task"></span>**\_поток ошибок \_ уже \_ в \_ задаче**
</dt> <dd> <dl> <dt>

1552 (0x610)
</dt> <dt>



Указанный поток уже присоединяется к задаче.


</dt> </dl> </dd> <dt>

<span id="ERROR_INSTALL_SERVICE_FAILURE"></span><span id="error_install_service_failure"></span>**Ошибка \_ при установке ошибки \_ службы \_**
</dt> <dd> <dl> <dt>

1601 (0x641)
</dt> <dt>



не удалось получить доступ к службе установщик Windows. это может произойти, если установщик Windows неправильно установлен. Обратитесь за помощью в службу поддержки.


</dt> </dl> </dd> <dt>

<span id="ERROR_INSTALL_USEREXIT"></span><span id="error_install_userexit"></span>**Ошибка при \_ установке \_ усерексит**
</dt> <dd> <dl> <dt>

1602 (0x642)
</dt> <dt>



Установка отменена пользователем.


</dt> </dl> </dd> <dt>

<span id="ERROR_INSTALL_FAILURE"></span><span id="error_install_failure"></span>**Ошибка \_ \_ при установке**
</dt> <dd> <dl> <dt>

1603 (0x643)
</dt> <dt>



Неустранимая ошибка при установке.


</dt> </dl> </dd> <dt>

<span id="ERROR_INSTALL_SUSPEND"></span><span id="error_install_suspend"></span>**Ошибка при \_ установке \_ приостановки**
</dt> <dd> <dl> <dt>

1604 (0x644)
</dt> <dt>



Установка приостановлена, не завершена.


</dt> </dl> </dd> <dt>

<span id="ERROR_UNKNOWN_PRODUCT"></span><span id="error_unknown_product"></span>**Ошибка \_ неизвестного \_ продукта**
</dt> <dd> <dl> <dt>

1605 (0x645)
</dt> <dt>



Это действие допустимо только для продуктов, установленных в настоящий момент.


</dt> </dl> </dd> <dt>

<span id="ERROR_UNKNOWN_FEATURE"></span><span id="error_unknown_feature"></span>**Ошибка \_ неизвестного \_ компонента**
</dt> <dd> <dl> <dt>

1606 (0x646)
</dt> <dt>



Идентификатор компонента не зарегистрирован.


</dt> </dl> </dd> <dt>

<span id="ERROR_UNKNOWN_COMPONENT"></span><span id="error_unknown_component"></span>**Ошибка \_ неизвестного \_ компонента**
</dt> <dd> <dl> <dt>

1607 (0x647)
</dt> <dt>



Идентификатор компонента не зарегистрирован.


</dt> </dl> </dd> <dt>

<span id="ERROR_UNKNOWN_PROPERTY"></span><span id="error_unknown_property"></span>**Ошибка \_ неизвестного \_ Свойства**
</dt> <dd> <dl> <dt>

1608 (0x648)
</dt> <dt>



Неизвестное свойство.


</dt> </dl> </dd> <dt>

<span id="ERROR_INVALID_HANDLE_STATE"></span><span id="error_invalid_handle_state"></span>**Ошибка \_ недопустимого \_ состояния обработчика \_**
</dt> <dd> <dl> <dt>

1609 (0x649)
</dt> <dt>



Недопустимое состояние обработчика.


</dt> </dl> </dd> <dt>

<span id="ERROR_BAD_CONFIGURATION"></span><span id="error_bad_configuration"></span>**Ошибка \_ неправильной \_ конфигурации**
</dt> <dd> <dl> <dt>

1610 (0x64A)
</dt> <dt>



Данные конфигурации для этого продукта повреждены. Обратитесь в службу поддержки.


</dt> </dl> </dd> <dt>

<span id="ERROR_INDEX_ABSENT"></span><span id="error_index_absent"></span>**\_отсутствует индекс \_ ошибки**
</dt> <dd> <dl> <dt>

1611 (0x64B)
</dt> <dt>



Отсутствует квалификатор компонента.


</dt> </dl> </dd> <dt>

<span id="ERROR_INSTALL_SOURCE_ABSENT"></span><span id="error_install_source_absent"></span>**Ошибка \_ \_ \_ отсутствия источника установки**
</dt> <dd> <dl> <dt>

1612 (0x64C)
</dt> <dt>



Источник установки для этого продукта недоступен. Убедитесь, что источник существует и к нему есть доступ.


</dt> </dl> </dd> <dt>

<span id="ERROR_INSTALL_PACKAGE_VERSION"></span><span id="error_install_package_version"></span>**Ошибка \_ при \_ установке \_ версии пакета**
</dt> <dd> <dl> <dt>

1613 (0x64D)
</dt> <dt>



этот установочный пакет не может быть установлен службой установщик Windows. необходимо установить пакет обновления Windows, содержащий более новую версию службы установщик Windows.


</dt> </dl> </dd> <dt>

<span id="ERROR_PRODUCT_UNINSTALLED"></span><span id="error_product_uninstalled"></span>**При \_ удалении продукта произошла ошибка \_**
</dt> <dd> <dl> <dt>

1614 (0x64E)
</dt> <dt>



Удаление продукта.


</dt> </dl> </dd> <dt>

<span id="ERROR_BAD_QUERY_SYNTAX"></span><span id="error_bad_query_syntax"></span>**Ошибка \_ неправильного \_ \_ синтаксиса запроса**
</dt> <dd> <dl> <dt>

1615 (0x64F)
</dt> <dt>



недопустимый или неподдерживаемый синтаксис запроса SQL.


</dt> </dl> </dd> <dt>

<span id="ERROR_INVALID_FIELD"></span><span id="error_invalid_field"></span>**Ошибка \_ недопустимого \_ поля**
</dt> <dd> <dl> <dt>

1616 (0x650)
</dt> <dt>



Поле записи не существует.


</dt> </dl> </dd> <dt>

<span id="ERROR_DEVICE_REMOVED"></span><span id="error_device_removed"></span>**устройство с ошибкой \_ \_ удалено**
</dt> <dd> <dl> <dt>

1617 (0x651)
</dt> <dt>



Устройство удалено.


</dt> </dl> </dd> <dt>

<span id="ERROR_INSTALL_ALREADY_RUNNING"></span><span id="error_install_already_running"></span>**Ошибка \_ установки \_ уже \_ запущена**
</dt> <dd> <dl> <dt>

1618 (0x652)
</dt> <dt>



Уже выполняется другая установка. Завершите эту установку, прежде чем продолжить установку.


</dt> </dl> </dd> <dt>

<span id="ERROR_INSTALL_PACKAGE_OPEN_FAILED"></span><span id="error_install_package_open_failed"></span>**Ошибка \_ \_ при установке \_ пакета \_ не удалось открыть**
</dt> <dd> <dl> <dt>

1619 (0x653)
</dt> <dt>



Не удалось открыть этот установочный пакет. убедитесь, что пакет существует и к нему есть доступ, или обратитесь к поставщику приложения, чтобы убедиться, что это допустимый пакет установщик Windows.


</dt> </dl> </dd> <dt>

<span id="ERROR_INSTALL_PACKAGE_INVALID"></span><span id="error_install_package_invalid"></span>**Ошибка при \_ установке \_ пакета \_**
</dt> <dd> <dl> <dt>

1620 (0x654)
</dt> <dt>



Не удалось открыть этот установочный пакет. обратитесь к поставщику приложения, чтобы убедиться, что это допустимый пакет установщик Windows.


</dt> </dl> </dd> <dt>

<span id="ERROR_INSTALL_UI_FAILURE"></span><span id="error_install_ui_failure"></span>**Ошибка \_ \_ при установке пользовательского интерфейса \_**
</dt> <dd> <dl> <dt>

1621 (0x655)
</dt> <dt>



произошла ошибка при запуске пользовательского интерфейса службы установщик Windows. Обратитесь в службу поддержки.


</dt> </dl> </dd> <dt>

<span id="ERROR_INSTALL_LOG_FAILURE"></span><span id="error_install_log_failure"></span>**Ошибка \_ при установке ошибки \_ журнала \_**
</dt> <dd> <dl> <dt>

1622 (0x656)
</dt> <dt>



ошибка при открытии файла журнала установки. Убедитесь, что указанное расположение файла журнала существует и что вы можете записать в него.


</dt> </dl> </dd> <dt>

<span id="ERROR_INSTALL_LANGUAGE_UNSUPPORTED"></span><span id="error_install_language_unsupported"></span>**Ошибка при \_ установке \_ языка \_ не поддерживается**
</dt> <dd> <dl> <dt>

1623 (0x657)
</dt> <dt>



Язык этого установочного пакета не поддерживается в вашей системе.


</dt> </dl> </dd> <dt>

<span id="ERROR_INSTALL_TRANSFORM_FAILURE"></span><span id="error_install_transform_failure"></span>**Ошибка \_ \_ при установке преобразования \_**
</dt> <dd> <dl> <dt>

1624 (0x658)
</dt> <dt>



Ошибка при применении преобразований. Убедитесь, что указаны допустимые пути преобразования.


</dt> </dl> </dd> <dt>

<span id="ERROR_INSTALL_PACKAGE_REJECTED"></span><span id="error_install_package_rejected"></span>**Ошибка при \_ установке \_ пакета \_**
</dt> <dd> <dl> <dt>

1625 (0x659)
</dt> <dt>



Эта установка запрещена системной политикой. Обратитесь к системному администратору.


</dt> </dl> </dd> <dt>

<span id="ERROR_FUNCTION_NOT_CALLED"></span><span id="error_function_not_called"></span>**\_функция ERROR \_ не \_ вызвана**
</dt> <dd> <dl> <dt>

1626 (0x65A)
</dt> <dt>



Не удалось выполнить функцию.


</dt> </dl> </dd> <dt>

<span id="ERROR_FUNCTION_FAILED"></span><span id="error_function_failed"></span>**Ошибка \_ \_ при выполнении функции**
</dt> <dd> <dl> <dt>

1627 (0x65B)
</dt> <dt>



Сбой функции во время выполнения.


</dt> </dl> </dd> <dt>

<span id="ERROR_INVALID_TABLE"></span><span id="error_invalid_table"></span>**Ошибка \_ недопустимой \_ таблицы**
</dt> <dd> <dl> <dt>

1628 (0x65C)
</dt> <dt>



Указана недопустимая или неизвестная таблица.


</dt> </dl> </dd> <dt>

<span id="ERROR_DATATYPE_MISMATCH"></span><span id="error_datatype_mismatch"></span>**\_несоответствие типов данных ошибок \_**
</dt> <dd> <dl> <dt>

1629 (0x65D)
</dt> <dt>



Указан неверный тип данных.


</dt> </dl> </dd> <dt>

<span id="ERROR_UNSUPPORTED_TYPE"></span><span id="error_unsupported_type"></span>**\_НЕподдерживаемый \_ тип ошибки**
</dt> <dd> <dl> <dt>

1630 (0x65E)
</dt> <dt>



Данные этого типа не поддерживаются.


</dt> </dl> </dd> <dt>

<span id="ERROR_CREATE_FAILED"></span><span id="error_create_failed"></span>**Ошибка \_ при создании ошибки \_**
</dt> <dd> <dl> <dt>

1631 (0x65F)
</dt> <dt>



не удалось запустить службу установщик Windows. Обратитесь в службу поддержки.


</dt> </dl> </dd> <dt>

<span id="ERROR_INSTALL_TEMP_UNWRITABLE"></span><span id="error_install_temp_unwritable"></span>**Ошибка при \_ установке \_ временного \_ недоступного для записи**
</dt> <dd> <dl> <dt>

1632 (0x660)
</dt> <dt>



Временная папка находится на диске, который полон или недоступен. Освободите место на диске или убедитесь, что у вас есть разрешение на запись во временную папку.


</dt> </dl> </dd> <dt>

<span id="ERROR_INSTALL_PLATFORM_UNSUPPORTED"></span><span id="error_install_platform_unsupported"></span>**Ошибка при \_ установке \_ платформы \_ не поддерживается**
</dt> <dd> <dl> <dt>

1633 (0x661)
</dt> <dt>



Этот установочный пакет не поддерживается этим типом процессора. Обратитесь к поставщику продукта.


</dt> </dl> </dd> <dt>

<span id="ERROR_INSTALL_NOTUSED"></span><span id="error_install_notused"></span>**Ошибка при \_ установке \_ нотусед**
</dt> <dd> <dl> <dt>

1634 (0x662)
</dt> <dt>



Компонент не используется на этом компьютере.


</dt> </dl> </dd> <dt>

<span id="ERROR_PATCH_PACKAGE_OPEN_FAILED"></span><span id="error_patch_package_open_failed"></span>**\_ \_ \_ сбой при открытии пакета исправления ошибок \_**
</dt> <dd> <dl> <dt>

1635 (0x663)
</dt> <dt>



Не удалось открыть этот пакет обновления. убедитесь, что пакет обновления существует и к нему есть доступ, или обратитесь к поставщику приложения, чтобы убедиться, что это допустимый установщик Windows пакет обновления.


</dt> </dl> </dd> <dt>

<span id="ERROR_PATCH_PACKAGE_INVALID"></span><span id="error_patch_package_invalid"></span>**\_ \_ Недопустимый пакет исправления ошибки \_**
</dt> <dd> <dl> <dt>

1636 (0x664)
</dt> <dt>



Не удалось открыть этот пакет обновления. обратитесь к поставщику приложения, чтобы убедиться, что это допустимый установщик Windows пакет обновления.


</dt> </dl> </dd> <dt>

<span id="ERROR_PATCH_PACKAGE_UNSUPPORTED"></span><span id="error_patch_package_unsupported"></span>**\_пакет ИСПРАВЛЕНИЙ \_ ошибок \_ не поддерживается**
</dt> <dd> <dl> <dt>

1637 (0x665)
</dt> <dt>



этот пакет обновления не может быть обработан службой установщик Windows. необходимо установить пакет обновления Windows, содержащий более новую версию службы установщик Windows.


</dt> </dl> </dd> <dt>

<span id="ERROR_PRODUCT_VERSION"></span><span id="error_product_version"></span>**\_версия продукта \_ ошибки**
</dt> <dd> <dl> <dt>

1638 (0x666)
</dt> <dt>



Уже установлена другая версия этого продукта. Установка этой версии невозможна. Чтобы настроить или удалить существующую версию продукта, используйте оснастку "Установка и удаление программ" на панели управления.


</dt> </dl> </dd> <dt>

<span id="ERROR_INVALID_COMMAND_LINE"></span><span id="error_invalid_command_line"></span>**Ошибка \_ Недопустимая \_ Командная \_ строка**
</dt> <dd> <dl> <dt>

1639 (0x667)
</dt> <dt>



Недопустимый аргумент командной строки. подробные сведения о командной строке см. в установщик Windows пакете SDK.


</dt> </dl> </dd> <dt>

<span id="ERROR_INSTALL_REMOTE_DISALLOWED"></span><span id="error_install_remote_disallowed"></span>**Ошибка \_ при \_ установке \_ запрещенного удаленного**
</dt> <dd> <dl> <dt>

1640 (0x668)
</dt> <dt>



Только администраторы имеют разрешение на добавление, удаление или настройку серверного программного обеспечения во время удаленного сеанса служб терминалов. Если вы хотите установить или настроить программное обеспечение на сервере, обратитесь к администратору сети.


</dt> </dl> </dd> <dt>

<span id="ERROR_SUCCESS_REBOOT_INITIATED"></span><span id="error_success_reboot_initiated"></span>**Ошибка \_ при \_ перезагрузке при успешном \_ запуске**
</dt> <dd> <dl> <dt>

1641 (0x669)
</dt> <dt>



Запрошенная операция успешно завершена. Система будет перезапущена, чтобы изменения вступили в силу.


</dt> </dl> </dd> <dt>

<span id="ERROR_PATCH_TARGET_NOT_FOUND"></span><span id="error_patch_target_not_found"></span>**\_цель исправления \_ ошибок \_ не \_ найдена**
</dt> <dd> <dl> <dt>

1642 (0x66A)
</dt> <dt>



не удается установить обновление службой установщик Windows, так как возможно, программа, которая будет обновлена, отсутствует, или обновление может обновить другую версию программы. Убедитесь, что обновляемая программа существует на компьютере и что у вас есть правильное обновление.


</dt> </dl> </dd> <dt>

<span id="ERROR_PATCH_PACKAGE_REJECTED"></span><span id="error_patch_package_rejected"></span>**\_пакет исправления \_ ошибок \_ отклонен**
</dt> <dd> <dl> <dt>

1643 (0x66B)
</dt> <dt>



Пакет обновления не разрешен политикой ограниченного использования программ.


</dt> </dl> </dd> <dt>

<span id="ERROR_INSTALL_TRANSFORM_REJECTED"></span><span id="error_install_transform_rejected"></span>**Ошибка при \_ установке \_ преобразования \_ отклонено**
</dt> <dd> <dl> <dt>

1644 (0x66C)
</dt> <dt>



Одна или несколько настроек не разрешены политикой ограниченного использования программ.


</dt> </dl> </dd> <dt>

<span id="ERROR_INSTALL_REMOTE_PROHIBITED"></span><span id="error_install_remote_prohibited"></span>**Ошибка при \_ установке \_ удаленного \_ запрещенного**
</dt> <dd> <dl> <dt>

1645 (0x66D)
</dt> <dt>



установщик Windows не допускают установки из подключение к удаленному рабочему столу.


</dt> </dl> </dd> <dt>

<span id="ERROR_PATCH_REMOVAL_UNSUPPORTED"></span><span id="error_patch_removal_unsupported"></span>**\_Удаление исправления \_ ошибки \_ не поддерживается**
</dt> <dd> <dl> <dt>

1646 (0x66E)
</dt> <dt>



Удаление пакета обновления не поддерживается.


</dt> </dl> </dd> <dt>

<span id="ERROR_UNKNOWN_PATCH"></span><span id="error_unknown_patch"></span>**Ошибка \_ неизвестного \_ исправления**
</dt> <dd> <dl> <dt>

1647 (0x66F)
</dt> <dt>



Обновление не применяется к этому продукту.


</dt> </dl> </dd> <dt>

<span id="ERROR_PATCH_NO_SEQUENCE"></span><span id="error_patch_no_sequence"></span>**\_исправление ошибки \_ без \_ последовательности**
</dt> <dd> <dl> <dt>

1648 (0x670)
</dt> <dt>



Не удалось найти допустимую последовательность для набора обновлений.


</dt> </dl> </dd> <dt>

<span id="ERROR_PATCH_REMOVAL_DISALLOWED"></span><span id="error_patch_removal_disallowed"></span>**\_Удаление исправления \_ ошибки \_ запрещено**
</dt> <dd> <dl> <dt>

1649 (0x671)
</dt> <dt>



Удаление обновления запрещено политикой.


</dt> </dl> </dd> <dt>

<span id="ERROR_INVALID_PATCH_XML"></span><span id="error_invalid_patch_xml"></span>**Ошибка \_ недопустимого \_ \_ XML-файла исправления**
</dt> <dd> <dl> <dt>

1650 (0x672)
</dt> <dt>



XML-данные обновления недопустимы.


</dt> </dl> </dd> <dt>

<span id="ERROR_PATCH_MANAGED_ADVERTISED_PRODUCT"></span><span id="error_patch_managed_advertised_product"></span>**Ошибка при \_ исправлении \_ управляемого \_ объявленного \_ продукта**
</dt> <dd> <dl> <dt>

1651 (0x673)
</dt> <dt>



Windows Установщик не позволяет обновлять управляемые объявленные продукты. Перед применением обновления необходимо установить по крайней мере один компонент продукта.


</dt> </dl> </dd> <dt>

<span id="ERROR_INSTALL_SERVICE_SAFEBOOT"></span><span id="error_install_service_safeboot"></span>**Ошибка при \_ установке \_ службы \_ SAFEBOOT**
</dt> <dd> <dl> <dt>

1652 (0x674)
</dt> <dt>



служба установщик Windows недоступна в режиме Сейф. повторите попытку, когда компьютер не находится в Сейфном режиме, или воспользуйтесь восстановлением системы, чтобы вернуть компьютер к предыдущему работоспособному состоянию.


</dt> </dl> </dd> <dt>

<span id="ERROR_FAIL_FAST_EXCEPTION"></span><span id="error_fail_fast_exception"></span>**ошибка \_ \_ FAST \_ исключения**
</dt> <dd> <dl> <dt>

1653 (0x675)
</dt> <dt>



Произошло исключение с быстрым сбоем. Обработчики исключений не будут вызываться, и процесс будет завершен немедленно.


</dt> </dl> </dd> <dt>

<span id="ERROR_INSTALL_REJECTED"></span><span id="error_install_rejected"></span>**Ошибка при \_ установке \_**
</dt> <dd> <dl> <dt>

1654 (0x676)
</dt> <dt>



Приложение, которое вы пытаетесь запустить, не поддерживается в этой версии Windows.


</dt> </dl> </dd> </dl>

## <a name="requirements"></a>Requirements (Требования)



| Требование | Значение |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Windows \[Только классические приложения XP\]<br/>                                           |
| Минимальная версия сервера<br/> | Windows Только для \[ настольных приложений сервера 2003\]<br/>                                  |
| Header<br/>                   | <dl> <dt>WinError. h</dt> </dl> |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[Коды системных ошибок](system-error-codes.md)
</dt> </dl>

 

 




