---
description: Параметр Стрпривилеже метода Свбемпривилежесет. Аддасстринг и параметр Ипривилеже для Свбемпривилежесет. Add требуются строки прав доступа из Вбемпривилежеенум.
ms.assetid: f9400597-81bb-44a8-80dc-aba0160aea26
ms.tgt_platform: multiple
title: Константы прав доступа (Wbemdisp. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- wbemPrivilegeCreateToken
- wbemPrivilegePrimaryToken
- wbemPrivilegeLockMemory
- wbemPrivilegeIncreaseQuota
- wbemPrivilegeMachineAccount
- wbemPrivilegeTcb
- wbemPrivilegeSecurity
- wbemPrivilegeTakeOwnership
- wbemPrivilegeLoadDriver
- wbemPrivilegeSystemProfile
- wbemPrivilegeSystemtime
- wbemPrivilegeProfileSingleProcess
- wbemPrivilegeIncreaseBasePriority
- wbemPrivilegeCreatePagefile
- wbemPrivilegeCreatePermanent
- wbemPrivilegeBackup
- wbemPrivilegeRestore
- wbemPrivilegeShutdown
- wbemPrivilegeDebug
- wbemPrivilegeAudit
- wbemPrivilegeSystemEnvironment
- wbemPrivilegeChangeNotify
- wbemPrivilegeRemoteShutdown
- wbemPrivilegeUndock
- wbemPrivilegeSyncAgent
- wbemPrivilegeEnableDelegation
- wbemPrivilegeManageVolume
api_type:
- HeaderDef
api_location:
- Wbemdisp.h
ms.openlocfilehash: 38d104c99885d4328ce8b12413e91607655ab1e260a61b511e3ea4a600b80b4d
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119131026"
---
# <a name="privilege-constants"></a>Константы прав доступа

Параметр *стрпривилеже* метода [**свбемпривилежесет. Аддасстринг**](swbemprivilegeset-addasstring.md) и параметр *ипривилеже* для [**свбемпривилежесет. Add**](swbemprivilegeset-add.md) требуются строки прав доступа из [вбемпривилежеенум](/windows/desktop/api/Wbemdisp/ne-wbemdisp-wbemprivilegeenum). Дополнительные сведения об использовании констант прав доступа см. в разделе [выполнение привилегированных операций](executing-privileged-operations.md).

В [**вбемпривилежеенум**](/windows/desktop/api/Wbemdisp/ne-wbemdisp-wbemprivilegeenum)определены следующие константы. В следующем списке приводятся эквивалентные константы для C++ и строки для создания скриптов. Для формирования краткого имени скрипта удалите слова "SE" и "Privilege" из имени константы C++.

В следующем примере кода VBScript показано, как включить привилегию Ремотешутдовн в скрипте.


```VB
Set Service = GetObject("winmgmts:{impersonationLevel=impersonate, (RemoteShutdown)}")
```



Для многих методов WMI необходимо включить одно или несколько разрешений. Если учетной записи не предоставлено право, ее нельзя включить для вызова метода.

<dl> <dt>

<span id="wbemPrivilegeCreateToken"></span><span id="wbemprivilegecreatetoken"></span><span id="WBEMPRIVILEGECREATETOKEN"></span>**вбемпривилежекреатетокен**
</dt> <dd> <dl> <dt>

1 (0x1)
</dt> <dt>



константа C++ **: \_ SE \_ создание \_ имени токена** — строка: **секреатетокенпривилеже**

Короткое имя сценария: **креатетокен**

Требуется для создания объекта первичного токена.


</dt> </dl> </dd> <dt>

<span id="wbemPrivilegePrimaryToken"></span><span id="wbemprivilegeprimarytoken"></span><span id="WBEMPRIVILEGEPRIMARYTOKEN"></span>**вбемпривилежепримаритокен**
</dt> <dd> <dl> <dt>

2 (0x2)
</dt> <dt>



Константа C++: строка **SeAssignPrimaryTokenPrivilege** : **SeAssignPrimaryTokenPrivilege**

Короткое имя сценария: **ассигнпримаритокен**

Требуется для замены маркера уровня процесса.


</dt> </dl> </dd> <dt>

<span id="wbemPrivilegeLockMemory"></span><span id="wbemprivilegelockmemory"></span><span id="WBEMPRIVILEGELOCKMEMORY"></span>**вбемпривилежелоккмемори**
</dt> <dd> <dl> <dt>

3 (0x3)
</dt> <dt>



константа C++: **SE строка \_ \_ \_ имени блокировки памяти** : **SeLockMemoryPrivilege**

Короткое имя сценария: **локкмемори**

Требуется для блокировки страниц в памяти.


</dt> </dl> </dd> <dt>

<span id="wbemPrivilegeIncreaseQuota"></span><span id="wbemprivilegeincreasequota"></span><span id="WBEMPRIVILEGEINCREASEQUOTA"></span>**вбемпривилежеинкреасекуота**
</dt> <dd> <dl> <dt>

4 (0x4)
</dt> <dt>



константа C++ **: \_ SE \_ увеличить \_ имя квоты** : **SeIncreaseQuotaPrivilege**

Короткое имя сценария: **инкреасекуотапривилеже**

Требуется для настройки квот памяти для процесса.


</dt> </dl> </dd> <dt>

<span id="wbemPrivilegeMachineAccount"></span><span id="wbemprivilegemachineaccount"></span><span id="WBEMPRIVILEGEMACHINEACCOUNT"></span>**вбемпривилежемачинеаккаунт**
</dt> <dd> <dl> <dt>

5 (0x5)
</dt> <dt>



константа C++: **SE строка \_ \_ \_ имени учетной записи машина** : **семачинеаккаунтпривилеже**

Короткое имя сценария: **мачинеаккаунт**

Требуется для добавления рабочих станций в домен.


</dt> </dl> </dd> <dt>

<span id="wbemPrivilegeTcb"></span><span id="wbemprivilegetcb"></span><span id="WBEMPRIVILEGETCB"></span>**вбемпривилежеткб**
</dt> <dd> <dl> <dt>

6 (0x6)
</dt> <dt>



константа C++: **SE строка \_ \_ имени TCB** : **SeTcbPrivilege**

Короткое имя сценария: **TCB**

Требуется для работы в составе операционной системы. Владелец является частью базы доверенного компьютера.


</dt> </dl> </dd> <dt>

<span id="wbemPrivilegeSecurity"></span><span id="wbemprivilegesecurity"></span><span id="WBEMPRIVILEGESECURITY"></span>**вбемпривилежесекурити**
</dt> <dd> <dl> <dt>

7 (0x7)
</dt> <dt>



константа C++: **SE строка \_ \_ имени безопасности** : **SeSecurityPrivilege**

Короткое имя сценария: **Безопасность**

Требуется для управления аудитом и журналом безопасности NT.


</dt> </dl> </dd> <dt>

<span id="wbemPrivilegeTakeOwnership"></span><span id="wbemprivilegetakeownership"></span><span id="WBEMPRIVILEGETAKEOWNERSHIP"></span>**вбемпривилежетакеовнершип**
</dt> <dd> <dl> <dt>

8 (0x8)
</dt> <dt>



константа C++ **: \_ SE \_ получение \_ имени владельца** строка: **сетакеовнершиппривилеже**

Короткое имя сценария: **такеовнершип**

Требуется для того, чтобы стать владельцем файлов или других объектов без [*записи контроля доступа*](/windows/desktop/SecGloss/a-gly) (ACE) в *списке управления доступом на уровне пользователей* (DACL).


</dt> </dl> </dd> <dt>

<span id="wbemPrivilegeLoadDriver"></span><span id="wbemprivilegeloaddriver"></span><span id="WBEMPRIVILEGELOADDRIVER"></span>**вбемпривилежелоаддривер**
</dt> <dd> <dl> <dt>

9 (0x9)
</dt> <dt>



константа C++: **SE \_ загрузка строки \_ драйвера** : **селоаддриверпривилеже**

Короткое имя сценария: **лоаддривер**

Требуется для загрузки или выгрузки драйвера устройства.


</dt> </dl> </dd> <dt>

<span id="wbemPrivilegeSystemProfile"></span><span id="wbemprivilegesystemprofile"></span><span id="WBEMPRIVILEGESYSTEMPROFILE"></span>**вбемпривилежесистемпрофиле**
</dt> <dd> <dl> <dt>

10 (0xA)
</dt> <dt>



константа C++: **SE строка \_ \_ \_ имени системного профиля** : **сесистемпрофилепривилеже**

Короткое имя сценария: **SystemProfile**

Требуется для сбора сведений о профиле производительности системы.


</dt> </dl> </dd> <dt>

<span id="wbemPrivilegeSystemtime"></span><span id="wbemprivilegesystemtime"></span><span id="WBEMPRIVILEGESYSTEMTIME"></span>**вбемпривилежесистемтиме**
</dt> <dd> <dl> <dt>

11 (0xB)
</dt> <dt>



константа C++: **SE имя \_ SYSTEMTIME** \_ строка: **сесистемтимепривилеже**

Короткое имя сценария: **SYSTEMTIME**

Требуется для изменения системного времени.


</dt> </dl> </dd> <dt>

<span id="wbemPrivilegeProfileSingleProcess"></span><span id="wbemprivilegeprofilesingleprocess"></span><span id="WBEMPRIVILEGEPROFILESINGLEPROCESS"></span>**вбемпривилежепрофилесинглепроцесс**
</dt> <dd> <dl> <dt>

12 (0xC)
</dt> <dt>



константа C++ **: \_ SE \_ PROF \_ \_ имя отдельного процесса** : **сепрофилесинглепроцесспривилеже**

Короткое имя сценария: **профилесинглепроцесс**

Требуется для сбора сведений о профиле для одного процесса.


</dt> </dl> </dd> <dt>

<span id="wbemPrivilegeIncreaseBasePriority"></span><span id="wbemprivilegeincreasebasepriority"></span><span id="WBEMPRIVILEGEINCREASEBASEPRIORITY"></span>**вбемпривилежеинкреасебасеприорити**
</dt> <dd> <dl> <dt>

13 (0xD)
</dt> <dt>



константа C++: строка **\_ \_ \_ \_ имени базового приоритета SE INC** : **SeIncreaseBasePriorityPrivilege**

Короткое имя сценария: **инкреасебасеприорити**

Требуется для увеличения приоритета планирования.


</dt> </dl> </dd> <dt>

<span id="wbemPrivilegeCreatePagefile"></span><span id="wbemprivilegecreatepagefile"></span><span id="WBEMPRIVILEGECREATEPAGEFILE"></span>**вбемпривилежекреатепажефиле**
</dt> <dd> <dl> <dt>

14 (0xE)
</dt> <dt>



константа C++ **: \_ SE \_ создать \_ имя файла подкачки** : **секреатепажефилепривилеже**

Короткое имя сценария: **креатепажефиле**

Требуется для создания файла подкачки.


</dt> </dl> </dd> <dt>

<span id="wbemPrivilegeCreatePermanent"></span><span id="wbemprivilegecreatepermanent"></span><span id="WBEMPRIVILEGECREATEPERMANENT"></span>**вбемпривилежекреатеперманент**
</dt> <dd> <dl> <dt>

15 (0xF)
</dt> <dt>



константа C++: **SE \_ создать строку \_ постоянного \_ имени** : **секреатеперманентпривилеже**

Короткое имя сценария: **креатеперманент**

Требуется для создания постоянных общих объектов.


</dt> </dl> </dd> <dt>

<span id="wbemPrivilegeBackup"></span><span id="wbemprivilegebackup"></span><span id="WBEMPRIVILEGEBACKUP"></span>**вбемпривилежебаккуп**
</dt> <dd> <dl> <dt>

16 (0x10)
</dt> <dt>



константа C++: **SE строка \_ \_ имени резервной копии** : **себаккуппривилеже**

Короткое имя сценария: **резервное копирование**

Требуется для резервного копирования файлов и каталогов, независимо от списка ACL, указанного для файла.


</dt> </dl> </dd> <dt>

<span id="wbemPrivilegeRestore"></span><span id="wbemprivilegerestore"></span><span id="WBEMPRIVILEGERESTORE"></span>**вбемпривилежересторе**
</dt> <dd> <dl> <dt>

17 (0x11)
</dt> <dt>



константа C++: **SE строка \_ \_ имени для восстановления** : **сересторепривилеже**

Короткое имя сценария: **RESTORE**

Требуется для восстановления файлов и каталогов независимо от списка ACL, указанного для файла.


</dt> </dl> </dd> <dt>

<span id="wbemPrivilegeShutdown"></span><span id="wbemprivilegeshutdown"></span><span id="WBEMPRIVILEGESHUTDOWN"></span>**вбемпривилежешутдовн**
</dt> <dd> <dl> <dt>

18 (0x12)
</dt> <dt>



константа C++: **SE строка \_ \_ имени завершения** : **сешутдовнпривилеже**

Короткое имя сценария: **Завершение работы**

Требуется для завершения работы локальной системы.


</dt> </dl> </dd> <dt>

<span id="wbemPrivilegeDebug"></span><span id="wbemprivilegedebug"></span><span id="WBEMPRIVILEGEDEBUG"></span>**вбемпривилежедебуг**
</dt> <dd> <dl> <dt>

19 (0x13)
</dt> <dt>



константа C++: **SE строка \_ \_ имени отладки** : **SeDebugPrivilege**

Короткое имя сценария: **Отладка**

Требуется для отладки и корректировки памяти процесса, принадлежащего другой учетной записи.


</dt> </dl> </dd> <dt>

<span id="wbemPrivilegeAudit"></span><span id="wbemprivilegeaudit"></span><span id="WBEMPRIVILEGEAUDIT"></span>**вбемпривилежеаудит**
</dt> <dd> <dl> <dt>

20 (0x14)
</dt> <dt>



константа C++: **SE строка \_ \_ имени аудита** : **SeAuditPrivilege**

Короткое имя сценария: **Аудит**

Требуется для создания записей аудита в журнале безопасности NT. Эта привилегия должна иметь только защищенные серверы.


</dt> </dl> </dd> <dt>

<span id="wbemPrivilegeSystemEnvironment"></span><span id="wbemprivilegesystemenvironment"></span><span id="WBEMPRIVILEGESYSTEMENVIRONMENT"></span>**вбемпривилежесистеменвиронмент**
</dt> <dd> <dl> <dt>

21 (0x15)
</dt> <dt>



константа C++: **SE строка \_ \_ \_ имени системной среды** : **сесистеменвиронментпривилеже**

Короткое имя сценария: **системенвиронмент**

Требуется для изменения энергонезависимого ОЗУ систем, использующих этот тип памяти для хранения данных конфигурации.


</dt> </dl> </dd> <dt>

<span id="wbemPrivilegeChangeNotify"></span><span id="wbemprivilegechangenotify"></span><span id="WBEMPRIVILEGECHANGENOTIFY"></span>**вбемпривилежечанженотифи**
</dt> <dd> <dl> <dt>

22 (0x16)
</dt> <dt>



константа C++ **: \_ SE \_ изменение \_ имени уведомления** строка: **SeChangeNotifyPrivilege**

Короткое имя сценария: **чанженотифи**

Требуется для получения уведомлений об изменениях в файлах или каталогах и обхода проверок доступа для обхода. Эта привилегия включена по умолчанию для всех пользователей.


</dt> </dl> </dd> <dt>

<span id="wbemPrivilegeRemoteShutdown"></span><span id="wbemprivilegeremoteshutdown"></span><span id="WBEMPRIVILEGEREMOTESHUTDOWN"></span>**вбемпривилежеремотешутдовн**
</dt> <dd> <dl> <dt>

23 (0x17)
</dt> <dt>



константа C++: **SE строка \_ \_ \_ имени удаленного завершения работы** : **серемотешутдовнпривилеже**

Короткое имя сценария: **ремотешутдовн**

Требуется для завершения работы удаленного компьютера.


</dt> </dl> </dd> <dt>

<span id="wbemPrivilegeUndock"></span><span id="wbemprivilegeundock"></span><span id="WBEMPRIVILEGEUNDOCK"></span>**вбемпривилежеундокк**
</dt> <dd> <dl> <dt>

24 (0x18)
</dt> <dt>



константа C++: **SE строка \_ \_ имени отстыковки** : **сеундоккпривилеже**

Короткое имя сценария: отмена **закрепления**

Требуется для удаления ноутбука с стыковочного узла.


</dt> </dl> </dd> <dt>

<span id="wbemPrivilegeSyncAgent"></span><span id="wbemprivilegesyncagent"></span><span id="WBEMPRIVILEGESYNCAGENT"></span>**вбемпривилежесинкажент**
</dt> <dd> <dl> <dt>

25 (0x19)
</dt> <dt>



константа C++: **SE строка \_ \_ \_ имени агента синхронизации** : **сесинкажентпривилеже**

Короткое имя сценария: **синкажент**

Требуется для синхронизации данных службы каталогов.


</dt> </dl> </dd> <dt>

<span id="wbemPrivilegeEnableDelegation"></span><span id="wbemprivilegeenabledelegation"></span><span id="WBEMPRIVILEGEENABLEDELEGATION"></span>**вбемпривилежеенабледелегатион**
</dt> <dd> <dl> <dt>

26 (0x1A)
</dt> <dt>



константа C++: **SE \_ включить строку \_ \_ имени делегирования** : **SeEnableDelegationPrivilege**

Короткое имя сценария: **енабледелегатион**

Требуется для включения доверия учетных записей компьютеров и пользователей для делегирования.


</dt> </dl> </dd> <dt>

<span id="wbemPrivilegeManageVolume"></span><span id="wbemprivilegemanagevolume"></span><span id="WBEMPRIVILEGEMANAGEVOLUME"></span>**вбемпривилежеманажеволуме**
</dt> <dd> <dl> <dt>

27 (0x1B)
</dt> <dt>



константа C++: **SE управление строкой \_ \_ \_ имени тома** : **семанажеволумепривилеже**

Короткое имя сценария: **манажеволуме**

Требуется для выполнения задач по обслуживанию томов.


</dt> </dl> </dd> </dl>

## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Windows Vista<br/>                                                                |
| Минимальная версия сервера<br/> | Windows Server 2008<br/>                                                          |
| Заголовок<br/>                   | <dl> <dt>Wbemdisp. h</dt> </dl>   |
| IDL<br/>                      | <dl> <dt>Wbemdisp. idl</dt> </dl> |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[Константы API скриптов](scripting-api-constants.md)
</dt> <dt>

[**свбемсекурити**](swbemsecurity.md)
</dt> <dt>

[**вбемпривилежеенум**](/windows/desktop/api/Wbemdisp/ne-wbemdisp-wbemprivilegeenum)
</dt> <dt>

[Выполнение привилегированных операций](executing-privileged-operations.md)
</dt> <dt>

[Выполнение привилегированных операций с помощью VBScript](executing-privileged-operations-using-vbscript.md)
</dt> </dl>

 

