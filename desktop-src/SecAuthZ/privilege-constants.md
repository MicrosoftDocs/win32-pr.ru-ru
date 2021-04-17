---
Description: Привилегии определяют тип системных операций, которые может выполнять учетная запись пользователя. Администратор назначает привилегии учетным записям пользователей и групп. Все привилегии пользователей включают пользователей, предоставленных пользователю, и группам, к которым он принадлежит.
ms.assetid: 973796a6-bc2e-4e64-92db-5e17b9c25460
title: Константы прав доступа (Winnt. h)
ms.topic: reference
ms.custom: snippet-project
ms.date: 07/27/2020
ms.openlocfilehash: 801eccb2f42ccf27b45bc5628a32cee3de994bfe
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105652143"
---
# <a name="privilege-constants-authorization"></a>Константы прав доступа (авторизация)

Привилегии определяют тип системных операций, которые может выполнять учетная запись пользователя. Администратор назначает привилегии учетным записям пользователей и групп. Привилегии каждого пользователя включают в себя пользователей, предоставленных пользователю, и группам, к которым принадлежит пользователь.

Функции, которые получают и корректируют привилегии в [*маркере доступа*](/windows/desktop/SecGloss/a-gly) , используют тип [*локально уникальный идентификатор*](/windows/desktop/SecGloss/l-gly) (LUID) для идентификации привилегий. Используйте функцию [**LookupPrivilegeValue**](/windows/desktop/api/Winbase/nf-winbase-lookupprivilegevaluea) , чтобы определить [**LUID**](/windows/desktop/api/Winnt/ns-winnt-luid) в локальной системе, соответствующий константе прав. Используйте функцию [**лукуппривилеженаме**](/windows/desktop/api/Winbase/nf-winbase-lookupprivilegenamea) для преобразования **LUID** в соответствующую строковую константу.

Операционная система представляет привилегию, используя строку, следующую за "право пользователя" в столбце Описание в следующей таблице. Операционная система отображает строки прав пользователя в столбце **Политика** узла **Назначение прав пользователя** в оснастке "Локальные параметры безопасности" консоли управления Microsoft (MMC).

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
Пример из [классической выборки Windows](https://github.com/microsoft/Windows-classic-samples/blob/1d363ff4bd17d8e20415b92e2ee989d615cc0d91/Samples/ManagementInfrastructure/cpp/Process/Provider/WindowsProcess.c) на сайте GitHub.

## <a name="constants"></a>Константы


<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th style="text-align: left;">Константа/значение</th>
<th style="text-align: left;">Описание</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td style="text-align: left;"><span id="SE_ASSIGNPRIMARYTOKEN_NAME"></span><span id="se_assignprimarytoken_name"></span><dl> <dt><strong></strong></dt> <dt>Текст SE_ASSIGNPRIMARYTOKEN_NAME ( &quot; SeAssignPrimaryTokenPrivilege &quot; )</dt> </dl></td>
<td style="text-align: left;">Требуется для назначения <a href="/windows/desktop/SecGloss/p-gly"><em>первичного маркера</em></a> процесса. <br/> Право пользователя. Замените маркер уровня процесса.<br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="SE_AUDIT_NAME"></span><span id="se_audit_name"></span><dl> <dt><strong></strong></dt> <dt>Текст SE_AUDIT_NAME ( &quot; SeAuditPrivilege &quot; )</dt> </dl></td>
<td style="text-align: left;">Требуется для создания записей журнала аудита. Предоставьте эту привилегию для защиты серверов. <br/> Право пользователя: создание аудитов безопасности.<br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="SE_BACKUP_NAME"></span><span id="se_backup_name"></span><dl> <dt><strong></strong></dt> <dt>Текст SE_BACKUP_NAME ( &quot; себаккуппривилеже &quot; )</dt> </dl></td>
<td style="text-align: left;">Требуется для выполнения операций резервного копирования. Эта привилегия заставляет систему предоставлять все разрешения на чтение любому файлу независимо от <a href="/windows/desktop/SecGloss/a-gly"><em>списка управления доступом</em></a> (ACL), указанного для файла. Любой запрос на доступ, отличный от Read, по-прежнему оценивается с помощью ACL. Эта привилегия необходима для функций <a href="/windows/desktop/api/winreg/nf-winreg-regsavekeya"><strong>регсавекэй</strong></a> и <a href="/windows/desktop/api/winreg/nf-winreg-regsavekeyexa"><strong>регсавекэйекс</strong></a>. Если эта привилегия удерживается, предоставляются следующие права доступа:<br/>
<ul>
<li>READ_CONTROL</li>
<li>ACCESS_SYSTEM_SECURITY</li>
<li>FILE_GENERIC_READ</li>
<li>FILE_TRAVERSE</li>
</ul>
Право пользователя. Резервное копирование файлов и каталогов.<br/>Если файл находится на съемном диске и включен параметр "аудит съемных носителей", SE_SECURITY_NAME должен иметь ACCESS_SYSTEM_SECURITY.</td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="SE_CHANGE_NOTIFY_NAME"></span><span id="se_change_notify_name"></span><dl> <dt><strong></strong></dt> <dt>Текст SE_CHANGE_NOTIFY_NAME ( &quot; SeChangeNotifyPrivilege &quot; )</dt> </dl></td>
<td style="text-align: left;">Требуется для получения уведомлений об изменениях в файлах или каталогах. Эта привилегия также приводит к тому, что система пропускает все проверки доступа для обхода. Он включен по умолчанию для всех пользователей. <br/> Право пользователя: обход перекрестной проверки.<br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="SE_CREATE_GLOBAL_NAME"></span><span id="se_create_global_name"></span><dl> <dt><strong></strong></dt> <dt>Текст SE_CREATE_GLOBAL_NAME ( &quot; секреатеглобалпривилеже &quot; )</dt> </dl></td>
<td style="text-align: left;">Требуется для создания именованных объектов сопоставления файлов в глобальном пространстве имен во время сеансов служб терминалов. Эта привилегия включена по умолчанию для администраторов, служб и учетных записей локальной системы.<br/> Право пользователя: создание глобальных объектов.<br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="SE_CREATE_PAGEFILE_NAME"></span><span id="se_create_pagefile_name"></span><dl> <dt><strong></strong></dt> <dt>Текст SE_CREATE_PAGEFILE_NAME ( &quot; секреатепажефилепривилеже &quot; )</dt> </dl></td>
<td style="text-align: left;">Требуется для создания файла подкачки. <br/> Право пользователя. Создайте файл подкачки.<br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="SE_CREATE_PERMANENT_NAME"></span><span id="se_create_permanent_name"></span><dl> <dt><strong></strong></dt> <dt>Текст SE_CREATE_PERMANENT_NAME ( &quot; секреатеперманентпривилеже &quot; )</dt> </dl></td>
<td style="text-align: left;">Требуется для создания постоянного объекта. <br/> Право пользователя: создание постоянных общих объектов.<br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="SE_CREATE_SYMBOLIC_LINK_NAME"></span><span id="se_create_symbolic_link_name"></span><dl> <dt><strong></strong></dt> <dt>Текст SE_CREATE_SYMBOLIC_LINK_NAME ( &quot; секреатесимболиклинкпривилеже &quot; )</dt> </dl></td>
<td style="text-align: left;">Требуется для создания символьной ссылки.<br/> Право пользователя: создание символьных ссылок.<br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="SE_CREATE_TOKEN_NAME"></span><span id="se_create_token_name"></span><dl> <dt><strong></strong></dt> <dt>Текст SE_CREATE_TOKEN_NAME ( &quot; секреатетокенпривилеже &quot; )</dt> </dl></td>
<td style="text-align: left;">Требуется для создания основного маркера. <br/> Право пользователя: Создайте объект маркера.<br/> Эту привилегию нельзя добавить к учетной записи пользователя с помощью &quot; политики создания объекта маркера &quot; . Кроме того, эту привилегию нельзя добавить в собственный процесс с помощью API-интерфейсов Windows. <strong>Windows Server 2003 и Windows XP с пакетом обновления 1 (SP1) и более ранними версиями:</strong> Интерфейсы API Windows могут добавлять эту привилегию к принадлежащему процессу.<br/> <br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="SE_DEBUG_NAME"></span><span id="se_debug_name"></span><dl> <dt><strong></strong></dt> <dt>Текст SE_DEBUG_NAME ( &quot; SeDebugPrivilege &quot; )</dt> </dl></td>
<td style="text-align: left;">Требуется для отладки и корректировки памяти процесса, принадлежащего другой учетной записи. <br/> Право пользователя: Отладка программ.<br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="SE_DELEGATE_SESSION_USER_IMPERSONATE_NAME"></span><span id="se_delegate_session_user_impersonate_name"></span><dl> <dt><strong></strong></dt> <dt>Текст SE_DELEGATE_SESSION_USER_IMPERSONATE_NAME ( &quot; седелегатесессионусеримперсонатепривилеже &quot; )</dt> </dl></td>
<td style="text-align: left;">Требуется для получения маркера олицетворения для другого пользователя в том же сеансе. <br/> Право пользователя: олицетворять других пользователей.<br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="SE_ENABLE_DELEGATION_NAME"></span><span id="se_enable_delegation_name"></span><dl> <dt><strong></strong></dt> <dt>Текст SE_ENABLE_DELEGATION_NAME ( &quot; SeEnableDelegationPrivilege &quot; )</dt> </dl></td>
<td style="text-align: left;">Требуется для пометки учетных записей пользователей и компьютеров в качестве доверенных для делегирования.<br/> Право пользователя: разрешение доверенных учетных записей компьютера и пользователя для делегирования.<br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="SE_IMPERSONATE_NAME"></span><span id="se_impersonate_name"></span><dl> <dt><strong></strong></dt> <dt>Текст SE_IMPERSONATE_NAME ( &quot; SeImpersonatePrivilege &quot; )</dt> </dl></td>
<td style="text-align: left;">Требуется для олицетворения.<br/> Право пользователя: олицетворять клиента после проверки подлинности.<br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="SE_INC_BASE_PRIORITY_NAME"></span><span id="se_inc_base_priority_name"></span><dl> <dt><strong></strong></dt> <dt>Текст SE_INC_BASE_PRIORITY_NAME ( &quot; SeIncreaseBasePriorityPrivilege &quot; )</dt> </dl></td>
<td style="text-align: left;">Требуется для увеличения базового приоритета процесса. <br/> Право пользователя: Увеличьте приоритет планирования.<br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="SE_INCREASE_QUOTA_NAME"></span><span id="se_increase_quota_name"></span><dl> <dt><strong></strong></dt> <dt>Текст SE_INCREASE_QUOTA_NAME ( &quot; SeIncreaseQuotaPrivilege &quot; )</dt> </dl></td>
<td style="text-align: left;">Требуется для увеличения квоты, назначенной процессу. <br/> Право пользователя: Настройте квоты памяти для процесса.<br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="SE_INC_WORKING_SET_NAME"></span><span id="se_inc_working_set_name"></span><dl> <dt><strong></strong></dt> <dt>Текст SE_INC_WORKING_SET_NAME ( &quot; SeIncreaseWorkingSetPrivilege &quot; )</dt> </dl></td>
<td style="text-align: left;">Требуется для выделения большего объема памяти для приложений, выполняемых в контексте пользователей.<br/> Право пользователя: Увеличьте рабочий набор процесса.<br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="SE_LOAD_DRIVER_NAME"></span><span id="se_load_driver_name"></span><dl> <dt><strong></strong></dt> <dt>Текст SE_LOAD_DRIVER_NAME ( &quot; селоаддриверпривилеже &quot; )</dt> </dl></td>
<td style="text-align: left;">Требуется для загрузки или выгрузки драйвера устройства. <br/> Право пользователя: Загрузка и выгрузка драйверов устройств.<br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="SE_LOCK_MEMORY_NAME"></span><span id="se_lock_memory_name"></span><dl> <dt><strong></strong></dt> <dt>Текст SE_LOCK_MEMORY_NAME ( &quot; SeLockMemoryPrivilege &quot; )</dt> </dl></td>
<td style="text-align: left;">Требуется для блокировки физических страниц в памяти. <br/> Право пользователя: Блокировка страниц в памяти.<br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="SE_MACHINE_ACCOUNT_NAME"></span><span id="se_machine_account_name"></span><dl> <dt><strong></strong></dt> <dt>Текст SE_MACHINE_ACCOUNT_NAME ( &quot; семачинеаккаунтпривилеже &quot; )</dt> </dl></td>
<td style="text-align: left;">Требуется для создания учетной записи компьютера. <br/> Право пользователя: Добавление рабочих станций в домен.<br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="SE_MANAGE_VOLUME_NAME"></span><span id="se_manage_volume_name"></span><dl> <dt><strong></strong></dt> <dt>Текст SE_MANAGE_VOLUME_NAME ( &quot; семанажеволумепривилеже &quot; )</dt> </dl></td>
<td style="text-align: left;">Требуется для включения привилегий управления томами. <br/> Право пользователя: Управление файлами на томе.<br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="SE_PROF_SINGLE_PROCESS_NAME"></span><span id="se_prof_single_process_name"></span><dl> <dt><strong></strong></dt> <dt>Текст SE_PROF_SINGLE_PROCESS_NAME ( &quot; сепрофилесинглепроцесспривилеже &quot; )</dt> </dl></td>
<td style="text-align: left;">Требуется для сбора данных профилирования для одного процесса. <br/> Право пользователя: Профилирование отдельного процесса.<br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="SE_RELABEL_NAME"></span><span id="se_relabel_name"></span><dl> <dt><strong></strong></dt> <dt>Текст SE_RELABEL_NAME ( &quot; серелабелпривилеже &quot; )</dt> </dl></td>
<td style="text-align: left;">Требуется для изменения обязательного уровня целостности объекта.<br/> Право пользователя: изменение метки объекта.<br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="SE_REMOTE_SHUTDOWN_NAME"></span><span id="se_remote_shutdown_name"></span><dl> <dt><strong></strong></dt> <dt>Текст SE_REMOTE_SHUTDOWN_NAME ( &quot; серемотешутдовнпривилеже &quot; )</dt> </dl></td>
<td style="text-align: left;">Требуется для завершения работы системы с помощью сетевого запроса. <br/> Право пользователя: принудительное завершение работы из удаленной системы.<br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="SE_RESTORE_NAME"></span><span id="se_restore_name"></span><dl> <dt><strong></strong></dt> <dt>Текст SE_RESTORE_NAME ( &quot; сересторепривилеже &quot; )</dt> </dl></td>
<td style="text-align: left;">Требуется для выполнения операций восстановления. Эта привилегия заставляет систему предоставлять все элементы управления доступом на запись в любой файл независимо от списка ACL, указанного для файла. Любой запрос на доступ, отличный от Write, по-прежнему оценивается с помощью ACL. Кроме того, эта привилегия позволяет задать любой допустимый идентификатор безопасности пользователя или группы в качестве владельца файла. Эта привилегия необходима для функции <a href="/windows/desktop/api/winreg/nf-winreg-regsavekeya"><strong>реглоадкэй</strong></a> . Если эта привилегия удерживается, предоставляются следующие права доступа:<br/>
<ul>
<li>WRITE_DAC</li>
<li>WRITE_OWNER</li>
<li>ACCESS_SYSTEM_SECURITY</li>
<li>FILE_GENERIC_WRITE</li>
<li>FILE_ADD_FILE</li>
<li>FILE_ADD_SUBDIRECTORY</li>
<li>DELETE</li>
</ul>
Право пользователя: восстановление файлов и каталогов.<br/>Если файл находится на съемном диске и включен параметр "аудит съемных носителей", SE_SECURITY_NAME должен иметь ACCESS_SYSTEM_SECURITY.<br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="SE_SECURITY_NAME"></span><span id="se_security_name"></span><dl> <dt><strong></strong></dt> <dt>Текст SE_SECURITY_NAME ( &quot; SeSecurityPrivilege &quot; )</dt> </dl></td>
<td style="text-align: left;">Требуется для выполнения ряда функций, связанных с безопасностью, таких как контроль и просмотр сообщений аудита. Эта привилегия определяет владельца в качестве оператора безопасности. <br/> Право пользователя: Управление аудитом и журналом безопасности.<br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="SE_SHUTDOWN_NAME"></span><span id="se_shutdown_name"></span><dl> <dt><strong></strong></dt> <dt>Текст SE_SHUTDOWN_NAME ( &quot; сешутдовнпривилеже &quot; )</dt> </dl></td>
<td style="text-align: left;">Требуется для завершения работы локальной системы. <br/> Право пользователя: завершение работы системы.<br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="SE_SYNC_AGENT_NAME"></span><span id="se_sync_agent_name"></span><dl> <dt><strong></strong></dt> <dt>Текст SE_SYNC_AGENT_NAME ( &quot; сесинкажентпривилеже &quot; )</dt> </dl></td>
<td style="text-align: left;">Требуется для контроллера домена, чтобы использовать службы синхронизации каталогов <a href="/windows/desktop/SecGloss/l-gly"><em>Lightweight Directory Access</em></a> . Эта привилегия позволяет владельцу читать все объекты и свойства в каталоге независимо от защиты объектов и свойств. По умолчанию он назначается учетным записям администратора и LocalSystem на контроллерах домена. <br/> Право пользователя: Синхронизация данных службы каталогов.<br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="SE_SYSTEM_ENVIRONMENT_NAME"></span><span id="se_system_environment_name"></span><dl> <dt><strong></strong></dt> <dt>Текст SE_SYSTEM_ENVIRONMENT_NAME ( &quot; сесистеменвиронментпривилеже &quot; )</dt> </dl></td>
<td style="text-align: left;">Требуется для изменения энергонезависимого ОЗУ систем, использующих этот тип памяти для хранения сведений о конфигурации. <br/> Право пользователя: изменение значений среды встроенного по.<br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="SE_SYSTEM_PROFILE_NAME"></span><span id="se_system_profile_name"></span><dl> <dt><strong></strong></dt> <dt>Текст SE_SYSTEM_PROFILE_NAME ( &quot; сесистемпрофилепривилеже &quot; )</dt> </dl></td>
<td style="text-align: left;">Требуется для сбора данных профилирования для всей системы. <br/> Право пользователя: Профилирование производительности системы.<br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="SE_SYSTEMTIME_NAME"></span><span id="se_systemtime_name"></span><dl> <dt><strong></strong></dt> <dt>Текст SE_SYSTEMTIME_NAME ( &quot; сесистемтимепривилеже &quot; )</dt> </dl></td>
<td style="text-align: left;">Требуется для изменения системного времени. <br/> Право пользователя: изменение системного времени.<br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="SE_TAKE_OWNERSHIP_NAME"></span><span id="se_take_ownership_name"></span><dl> <dt><strong></strong></dt> <dt>Текст SE_TAKE_OWNERSHIP_NAME ( &quot; сетакеовнершиппривилеже &quot; )</dt> </dl></td>
<td style="text-align: left;">Требуется, чтобы стать владельцем объекта без предоставления избирательного доступа. Эта привилегия позволяет задать значение Owner только для тех значений, которые владелец может назначить в качестве владельца объекта. <br/> Право пользователя: стать владельцем файлов или других объектов.<br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="SE_TCB_NAME"></span><span id="se_tcb_name"></span><dl> <dt><strong></strong></dt> <dt>Текст SE_TCB_NAME ( &quot; SeTcbPrivilege &quot; )</dt> </dl></td>
<td style="text-align: left;">Эта привилегия определяет владельца как часть базы доверенного компьютера. Этой привилегии обладают некоторые доверенные защищенные подсистемы. <br/> Право пользователя: работа в составе операционной системы.<br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="SE_TIME_ZONE_NAME"></span><span id="se_time_zone_name"></span><dl> <dt><strong></strong></dt> <dt>Текст SE_TIME_ZONE_NAME ( &quot; сетимезонепривилеже &quot; )</dt> </dl></td>
<td style="text-align: left;">Требуется для настройки часового пояса, связанного с внутренним часами компьютера.<br/> Право пользователя: изменение часового пояса.<br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="SE_TRUSTED_CREDMAN_ACCESS_NAME"></span><span id="se_trusted_credman_access_name"></span><dl> <dt><strong></strong></dt> <dt>Текст SE_TRUSTED_CREDMAN_ACCESS_NAME ( &quot; сетрустедкредманакцесспривилеже &quot; )</dt> </dl></td>
<td style="text-align: left;">Требуется для доступа к диспетчеру учетных данных в качестве доверенного вызывающего объекта.<br/> Право пользователя: доступ к диспетчеру учетных данных как к доверенному вызывающему объекту.<br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="SE_UNDOCK_NAME"></span><span id="se_undock_name"></span><dl> <dt><strong></strong></dt> <dt>Текст SE_UNDOCK_NAME ( &quot; сеундоккпривилеже &quot; )</dt> </dl></td>
<td style="text-align: left;">Требуется для открепления ноутбука.<br/> Право пользователя: Удаление компьютера из стыковочного узла.<br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="SE_UNSOLICITED_INPUT_NAME"></span><span id="se_unsolicited_input_name"></span><dl> <dt><strong></strong></dt> <dt>Текст SE_UNSOLICITED_INPUT_NAME ( &quot; сеунсолиЦитединпутпривилеже &quot; )</dt> </dl></td>
<td style="text-align: left;">Требуется для чтения незапрошенных входных данных с устройства <a href="/windows/desktop/SecGloss/t-gly"><em>терминала</em></a> .<br/> Право пользователя: неприменимо.<br/></td>
</tr>
</tbody>
</table>



## <a name="remarks"></a>Комментарии

Константы прав определены как строки в Winnt. h. Например, \_ \_ константа имени аудита SE определяется как "SeAuditPrivilege".

## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------------------------|------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Только для \[ классических приложений Windows XP\]<br/>                                        |
| Минимальная версия сервера<br/> | \[Только для настольных приложений Windows Server 2003\]<br/>                               |
| Header<br/>                   | <dl> <dt>Файл Winnt. h</dt> </dl> |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[Права](privileges.md)
</dt> </dl>

