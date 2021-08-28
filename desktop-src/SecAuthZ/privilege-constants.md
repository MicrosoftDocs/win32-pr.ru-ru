---
Description: Привилегии определяют тип системных операций, которые может выполнять учетная запись пользователя. Администратор назначает привилегии учетным записям пользователей и групп. Все привилегии пользователей включают пользователей, предоставленных пользователю, и группам, к которым он принадлежит.
ms.assetid: 973796a6-bc2e-4e64-92db-5e17b9c25460
title: Константы прав доступа (Winnt. h)
ms.topic: reference
ms.custom: snippet-project
ms.date: 07/27/2020
ms.openlocfilehash: 5da0a0e6f9ad3b0559fdf2d8e375e6d25e7d2fdf
ms.sourcegitcommit: 9b5faa61c38b2d0c432b7f2dbee8c127b0e28a7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/19/2021
ms.locfileid: "122475750"
---
# <a name="privilege-constants-authorization"></a>Константы прав доступа (авторизация)

Привилегии определяют тип системных операций, которые может выполнять учетная запись пользователя. Администратор назначает привилегии учетным записям пользователей и групп. Привилегии каждого пользователя включают в себя пользователей, предоставленных пользователю, и группам, к которым принадлежит пользователь.

Функции, которые получают и корректируют привилегии в [*маркере доступа*](/windows/desktop/SecGloss/a-gly) , используют тип [*локально уникальный идентификатор*](/windows/desktop/SecGloss/l-gly) (LUID) для идентификации привилегий. Используйте функцию [**LookupPrivilegeValue**](/windows/desktop/api/Winbase/nf-winbase-lookupprivilegevaluea) , чтобы определить [**LUID**](/windows/desktop/api/Winnt/ns-winnt-luid) в локальной системе, соответствующий константе прав. Используйте функцию [**лукуппривилеженаме**](/windows/desktop/api/Winbase/nf-winbase-lookupprivilegenamea) для преобразования **LUID** в соответствующую строковую константу.

Операционная система представляет привилегию, используя строку, следующую за "право пользователя" в столбце Описание в следующей таблице. операционная система отображает строки прав пользователя в столбце **политика** узла **назначение прав пользователя** в локальной системе безопасности Параметры оснастки консоли управления майкрософт (MMC).

## <a name="example"></a>Пример

```cpp
BOOL EnablePrivilege()
{
    LUID PrivilegeRequired ;
    BOOL bRes = FALSE;
  
    bRes = LookupPrivilegeValue(NULL, SE_DEBUG_NAME, &PrivilegeRequired);

    // ...

    return bRes;
}
```
пример из [Windows классических примеров](https://github.com/microsoft/Windows-classic-samples/blob/1d363ff4bd17d8e20415b92e2ee989d615cc0d91/Samples/ManagementInfrastructure/cpp/Process/Provider/WindowsProcess.c) на GitHub.

## <a name="constants"></a>Константы



| Константа/значение | Описание | 
|----------------|-------------|
| <span id="SE_ASSIGNPRIMARYTOKEN_NAME"></span><span id="se_assignprimarytoken_name"></span><dl>Текст <dt><strong>SE_ASSIGNPRIMARYTOKEN_NAME</strong></dt><dt>("SeAssignPrimaryTokenPrivilege")</dt></dl> | Требуется для назначения <a href="/windows/desktop/SecGloss/p-gly"><em>первичного маркера</em></a> процесса. <br /> Право пользователя. Замените маркер уровня процесса.<br /> | 
| <span id="SE_AUDIT_NAME"></span><span id="se_audit_name"></span><dl>Текст <dt><strong>SE_AUDIT_NAME</strong></dt><dt>("SeAuditPrivilege")</dt></dl> | Требуется для создания записей журнала аудита. Предоставьте эту привилегию для защиты серверов. <br /> Право пользователя: создание аудитов безопасности.<br /> | 
| <span id="SE_BACKUP_NAME"></span><span id="se_backup_name"></span><dl>Текст <dt><strong>SE_BACKUP_NAME</strong></dt><dt>("себаккуппривилеже")</dt></dl> | Требуется для выполнения операций резервного копирования. Эта привилегия заставляет систему предоставлять все разрешения на чтение любому файлу независимо от <a href="/windows/desktop/SecGloss/a-gly"><em>списка управления доступом</em></a> (ACL), указанного для файла. Любой запрос на доступ, отличный от Read, по-прежнему оценивается с помощью ACL. Эта привилегия необходима для функций <a href="/windows/desktop/api/winreg/nf-winreg-regsavekeya"><strong>регсавекэй</strong></a> и <a href="/windows/desktop/api/winreg/nf-winreg-regsavekeyexa"><strong>регсавекэйекс</strong></a>. Если эта привилегия удерживается, предоставляются следующие права доступа:<br /><ul><li>READ_CONTROL</li><li>ACCESS_SYSTEM_SECURITY</li><li>FILE_GENERIC_READ</li><li>FILE_TRAVERSE</li></ul>Право пользователя. Резервное копирование файлов и каталогов.<br />если файл находится на съемном диске и включен параметр «аудит съемных служба хранилища», SE_SECURITY_NAME требуется ACCESS_SYSTEM_SECURITY. | 
| <span id="SE_CHANGE_NOTIFY_NAME"></span><span id="se_change_notify_name"></span><dl>Текст <dt><strong>SE_CHANGE_NOTIFY_NAME</strong></dt><dt>("SeChangeNotifyPrivilege")</dt></dl> | Требуется для получения уведомлений об изменениях в файлах или каталогах. Эта привилегия также приводит к тому, что система пропускает все проверки доступа для обхода. Он включен по умолчанию для всех пользователей. <br /> Право пользователя: обход перекрестной проверки.<br /> | 
| <span id="SE_CREATE_GLOBAL_NAME"></span><span id="se_create_global_name"></span><dl>Текст <dt><strong>SE_CREATE_GLOBAL_NAME</strong></dt><dt>("секреатеглобалпривилеже")</dt></dl> | Требуется для создания именованных объектов сопоставления файлов в глобальном пространстве имен во время сеансов служб терминалов. Эта привилегия включена по умолчанию для администраторов, служб и учетных записей локальной системы.<br /> Право пользователя: создание глобальных объектов.<br /> | 
| <span id="SE_CREATE_PAGEFILE_NAME"></span><span id="se_create_pagefile_name"></span><dl>Текст <dt><strong>SE_CREATE_PAGEFILE_NAME</strong></dt><dt>("секреатепажефилепривилеже")</dt></dl> | Требуется для создания файла подкачки. <br /> Право пользователя. Создайте файл подкачки.<br /> | 
| <span id="SE_CREATE_PERMANENT_NAME"></span><span id="se_create_permanent_name"></span><dl>Текст <dt><strong>SE_CREATE_PERMANENT_NAME</strong></dt><dt>("секреатеперманентпривилеже")</dt></dl> | Требуется для создания постоянного объекта. <br /> Право пользователя: создание постоянных общих объектов.<br /> | 
| <span id="SE_CREATE_SYMBOLIC_LINK_NAME"></span><span id="se_create_symbolic_link_name"></span><dl>Текст <dt><strong>SE_CREATE_SYMBOLIC_LINK_NAME</strong></dt><dt>("секреатесимболиклинкпривилеже")</dt></dl> | Требуется для создания символьной ссылки.<br /> Право пользователя: создание символьных ссылок.<br /> | 
| <span id="SE_CREATE_TOKEN_NAME"></span><span id="se_create_token_name"></span><dl>Текст <dt><strong>SE_CREATE_TOKEN_NAME</strong></dt><dt>("секреатетокенпривилеже")</dt></dl> | Требуется для создания основного маркера. <br /> Право пользователя: Создайте объект маркера.<br /> Эту привилегию нельзя добавить к учетной записи пользователя с помощью политики "создать объект токена". кроме того, эту привилегию нельзя добавить в собственный процесс с помощью Windows api. <strong>Windows Server 2003 и Windows XP с пакетом обновления 1 (SP1) и более ранними версиями:</strong> Windows интерфейсы api могут добавить эту привилегию в принадлежащие процессу.<br /><br /> | 
| <span id="SE_DEBUG_NAME"></span><span id="se_debug_name"></span><dl>Текст <dt><strong>SE_DEBUG_NAME</strong></dt><dt>("SeDebugPrivilege")</dt></dl> | Требуется для отладки и корректировки памяти процесса, принадлежащего другой учетной записи. <br /> Право пользователя: Отладка программ.<br /> | 
| <span id="SE_DELEGATE_SESSION_USER_IMPERSONATE_NAME"></span><span id="se_delegate_session_user_impersonate_name"></span><dl>Текст <dt><strong>SE_DELEGATE_SESSION_USER_IMPERSONATE_NAME</strong></dt><dt>("седелегатесессионусеримперсонатепривилеже")</dt></dl> | Требуется для получения маркера олицетворения для другого пользователя в том же сеансе. <br /> Право пользователя: олицетворять других пользователей.<br /> | 
| <span id="SE_ENABLE_DELEGATION_NAME"></span><span id="se_enable_delegation_name"></span><dl>Текст <dt><strong>SE_ENABLE_DELEGATION_NAME</strong></dt><dt>("SeEnableDelegationPrivilege")</dt></dl> | Требуется для пометки учетных записей пользователей и компьютеров в качестве доверенных для делегирования.<br /> Право пользователя: разрешение доверенных учетных записей компьютера и пользователя для делегирования.<br /> | 
| <span id="SE_IMPERSONATE_NAME"></span><span id="se_impersonate_name"></span><dl>Текст <dt><strong>SE_IMPERSONATE_NAME</strong></dt><dt>("SeImpersonatePrivilege")</dt></dl> | Требуется для олицетворения.<br /> Право пользователя: олицетворять клиента после проверки подлинности.<br /> | 
| <span id="SE_INC_BASE_PRIORITY_NAME"></span><span id="se_inc_base_priority_name"></span><dl>Текст <dt><strong>SE_INC_BASE_PRIORITY_NAME</strong></dt><dt>("SeIncreaseBasePriorityPrivilege")</dt></dl> | Требуется для увеличения базового приоритета процесса. <br /> Право пользователя: Увеличьте приоритет планирования.<br /> | 
| <span id="SE_INCREASE_QUOTA_NAME"></span><span id="se_increase_quota_name"></span><dl>Текст <dt><strong>SE_INCREASE_QUOTA_NAME</strong></dt><dt>("SeIncreaseQuotaPrivilege")</dt></dl> | Требуется для увеличения квоты, назначенной процессу. <br /> Право пользователя: Настройте квоты памяти для процесса.<br /> | 
| <span id="SE_INC_WORKING_SET_NAME"></span><span id="se_inc_working_set_name"></span><dl>Текст <dt><strong>SE_INC_WORKING_SET_NAME</strong></dt><dt>("SeIncreaseWorkingSetPrivilege")</dt></dl> | Требуется для выделения большего объема памяти для приложений, выполняемых в контексте пользователей.<br /> Право пользователя: Увеличьте рабочий набор процесса.<br /> | 
| <span id="SE_LOAD_DRIVER_NAME"></span><span id="se_load_driver_name"></span><dl>Текст <dt><strong>SE_LOAD_DRIVER_NAME</strong></dt><dt>("селоаддриверпривилеже")</dt></dl> | Требуется для загрузки или выгрузки драйвера устройства. <br /> Право пользователя: Загрузка и выгрузка драйверов устройств.<br /> | 
| <span id="SE_LOCK_MEMORY_NAME"></span><span id="se_lock_memory_name"></span><dl>Текст <dt><strong>SE_LOCK_MEMORY_NAME</strong></dt><dt>("SeLockMemoryPrivilege")</dt></dl> | Требуется для блокировки физических страниц в памяти. <br /> Право пользователя: Блокировка страниц в памяти.<br /> | 
| <span id="SE_MACHINE_ACCOUNT_NAME"></span><span id="se_machine_account_name"></span><dl>Текст <dt><strong>SE_MACHINE_ACCOUNT_NAME</strong></dt><dt>("семачинеаккаунтпривилеже")</dt></dl> | Требуется для создания учетной записи компьютера. <br /> Право пользователя: Добавление рабочих станций в домен.<br /> | 
| <span id="SE_MANAGE_VOLUME_NAME"></span><span id="se_manage_volume_name"></span><dl>Текст <dt><strong>SE_MANAGE_VOLUME_NAME</strong></dt><dt>("семанажеволумепривилеже")</dt></dl> | Требуется для включения привилегий управления томами. <br /> Право пользователя: Управление файлами на томе.<br /> | 
| <span id="SE_PROF_SINGLE_PROCESS_NAME"></span><span id="se_prof_single_process_name"></span><dl>Текст <dt><strong>SE_PROF_SINGLE_PROCESS_NAME</strong></dt><dt>("сепрофилесинглепроцесспривилеже")</dt></dl> | Требуется для сбора данных профилирования для одного процесса. <br /> Право пользователя: Профилирование отдельного процесса.<br /> | 
| <span id="SE_RELABEL_NAME"></span><span id="se_relabel_name"></span><dl>Текст <dt><strong>SE_RELABEL_NAME</strong></dt><dt>("серелабелпривилеже")</dt></dl> | Требуется для изменения обязательного уровня целостности объекта.<br /> Право пользователя: изменение метки объекта.<br /> | 
| <span id="SE_REMOTE_SHUTDOWN_NAME"></span><span id="se_remote_shutdown_name"></span><dl>Текст <dt><strong>SE_REMOTE_SHUTDOWN_NAME</strong></dt><dt>("серемотешутдовнпривилеже")</dt></dl> | Требуется для завершения работы системы с помощью сетевого запроса. <br /> Право пользователя: принудительное завершение работы из удаленной системы.<br /> | 
| <span id="SE_RESTORE_NAME"></span><span id="se_restore_name"></span><dl>Текст <dt><strong>SE_RESTORE_NAME</strong></dt><dt>("сересторепривилеже")</dt></dl> | Требуется для выполнения операций восстановления. Эта привилегия заставляет систему предоставлять все элементы управления доступом на запись в любой файл независимо от списка ACL, указанного для файла. Любой запрос на доступ, отличный от Write, по-прежнему оценивается с помощью ACL. Кроме того, эта привилегия позволяет задать любой допустимый идентификатор безопасности пользователя или группы в качестве владельца файла. Эта привилегия необходима для функции <a href="/windows/desktop/api/winreg/nf-winreg-regloadkeya"><strong>реглоадкэй</strong></a> . Если эта привилегия удерживается, предоставляются следующие права доступа:<br /><ul><li>WRITE_DAC</li><li>WRITE_OWNER</li><li>ACCESS_SYSTEM_SECURITY</li><li>FILE_GENERIC_WRITE</li><li>FILE_ADD_FILE</li><li>FILE_ADD_SUBDIRECTORY</li><li>DELETE</li></ul>Право пользователя: восстановление файлов и каталогов.<br />если файл находится на съемном диске и включен параметр «аудит съемных служба хранилища», SE_SECURITY_NAME требуется ACCESS_SYSTEM_SECURITY.<br /> | 
| <span id="SE_SECURITY_NAME"></span><span id="se_security_name"></span><dl><dt><strong>SE_SECURITY_NAME</strong></dt><dt>текст ("SeSecurityPrivilege")</dt></dl> | Требуется для выполнения ряда функций, связанных с безопасностью, таких как контроль и просмотр сообщений аудита. Эта привилегия определяет владельца в качестве оператора безопасности. <br /> Право пользователя: Управление аудитом и журналом безопасности.<br /> | 
| <span id="SE_SHUTDOWN_NAME"></span><span id="se_shutdown_name"></span><dl>Текст <dt><strong>SE_SHUTDOWN_NAME</strong></dt><dt>("сешутдовнпривилеже")</dt></dl> | Требуется для завершения работы локальной системы. <br /> Право пользователя: завершение работы системы.<br /> | 
| <span id="SE_SYNC_AGENT_NAME"></span><span id="se_sync_agent_name"></span><dl>Текст <dt><strong>SE_SYNC_AGENT_NAME</strong></dt><dt>("сесинкажентпривилеже")</dt></dl> | Требуется для контроллера домена, чтобы использовать службы синхронизации каталогов <a href="/windows/desktop/SecGloss/l-gly"><em>Lightweight Directory Access</em></a> . Эта привилегия позволяет владельцу читать все объекты и свойства в каталоге независимо от защиты объектов и свойств. По умолчанию он назначается учетным записям администратора и LocalSystem на контроллерах домена. <br /> Право пользователя: Синхронизация данных службы каталогов.<br /> | 
| <span id="SE_SYSTEM_ENVIRONMENT_NAME"></span><span id="se_system_environment_name"></span><dl>Текст <dt><strong>SE_SYSTEM_ENVIRONMENT_NAME</strong></dt><dt>("сесистеменвиронментпривилеже")</dt></dl> | Требуется для изменения энергонезависимого ОЗУ систем, использующих этот тип памяти для хранения сведений о конфигурации. <br /> Право пользователя: изменение значений среды встроенного по.<br /> | 
| <span id="SE_SYSTEM_PROFILE_NAME"></span><span id="se_system_profile_name"></span><dl>Текст <dt><strong>SE_SYSTEM_PROFILE_NAME</strong></dt><dt>("сесистемпрофилепривилеже")</dt></dl> | Требуется для сбора данных профилирования для всей системы. <br /> Право пользователя: Профилирование производительности системы.<br /> | 
| <span id="SE_SYSTEMTIME_NAME"></span><span id="se_systemtime_name"></span><dl>Текст <dt><strong>SE_SYSTEMTIME_NAME</strong></dt><dt>("сесистемтимепривилеже")</dt></dl> | Требуется для изменения системного времени. <br /> Право пользователя: изменение системного времени.<br /> | 
| <span id="SE_TAKE_OWNERSHIP_NAME"></span><span id="se_take_ownership_name"></span><dl>Текст <dt><strong>SE_TAKE_OWNERSHIP_NAME</strong></dt><dt>("сетакеовнершиппривилеже")</dt></dl> | Требуется, чтобы стать владельцем объекта без предоставления избирательного доступа. Эта привилегия позволяет задать значение Owner только для тех значений, которые владелец может назначить в качестве владельца объекта. <br /> Право пользователя: стать владельцем файлов или других объектов.<br /> | 
| <span id="SE_TCB_NAME"></span><span id="se_tcb_name"></span><dl>Текст <dt><strong>SE_TCB_NAME</strong></dt><dt>("SeTcbPrivilege")</dt></dl> | Эта привилегия определяет владельца как часть базы доверенного компьютера. Этой привилегии обладают некоторые доверенные защищенные подсистемы. <br /> Право пользователя: работа в составе операционной системы.<br /> | 
| <span id="SE_TIME_ZONE_NAME"></span><span id="se_time_zone_name"></span><dl>Текст <dt><strong>SE_TIME_ZONE_NAME</strong></dt><dt>("сетимезонепривилеже")</dt></dl> | Требуется для настройки часового пояса, связанного с внутренним часами компьютера.<br /> Право пользователя: изменение часового пояса.<br /> | 
| <span id="SE_TRUSTED_CREDMAN_ACCESS_NAME"></span><span id="se_trusted_credman_access_name"></span><dl>Текст <dt><strong>SE_TRUSTED_CREDMAN_ACCESS_NAME</strong></dt><dt>("сетрустедкредманакцесспривилеже")</dt></dl> | Требуется для доступа к диспетчеру учетных данных в качестве доверенного вызывающего объекта.<br /> Право пользователя: доступ к диспетчеру учетных данных как к доверенному вызывающему объекту.<br /> | 
| <span id="SE_UNDOCK_NAME"></span><span id="se_undock_name"></span><dl>Текст <dt><strong>SE_UNDOCK_NAME</strong></dt><dt>("сеундоккпривилеже")</dt></dl> | Требуется для открепления ноутбука.<br /> Право пользователя: Удаление компьютера из стыковочного узла.<br /> | 
| <span id="SE_UNSOLICITED_INPUT_NAME"></span><span id="se_unsolicited_input_name"></span><dl>Текст <dt><strong>SE_UNSOLICITED_INPUT_NAME</strong></dt><dt>("сеунсолиЦитединпутпривилеже")</dt></dl> | Требуется для чтения незапрошенных входных данных с устройства <a href="/windows/desktop/SecGloss/t-gly"><em>терминала</em></a> .<br /> Право пользователя: неприменимо.<br /> | 




## <a name="remarks"></a>Комментарии

Константы прав определены как строки в Winnt. h. например, \_ \_ константа имени аудита SE определяется как "SeAuditPrivilege".

## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------------------------|------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Windows \[Только классические приложения XP\]<br/>                                        |
| Минимальная версия сервера<br/> | Windows Только для \[ настольных приложений сервера 2003\]<br/>                               |
| Заголовок<br/>                   | <dl> <dt>Файл Winnt. h</dt> </dl> |



## <a name="see-also"></a>См. также

<dl> <dt>

[Привилегии](privileges.md)
</dt> </dl>

