---
description: Модель безопасности Windows позволяет управлять доступом к диспетчеру управления службами (SCM) и объектам служб.
ms.assetid: 23d1c382-6ba4-49e2-8039-c2a91471076c
title: Права доступа и безопасности службы
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e7677b8a9f7a5e1fadf8231999d266a9474fb731
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "105664372"
---
# <a name="service-security-and-access-rights"></a>Права доступа и безопасности службы

Модель безопасности Windows позволяет управлять доступом к диспетчеру управления службами (SCM) и объектам служб. Подробные сведения приведены в следующих разделах:

-   [Права доступа для диспетчера управления службами](#access-rights-for-the-service-control-manager)
-   [Права доступа для службы](#access-rights-for-a-service)

## <a name="access-rights-for-the-service-control-manager"></a>Права доступа для диспетчера управления службами

Ниже перечислены особые права доступа к SCM.



| Право доступа                                   | Описание                                                                                                                                                                                                                                                                                                                                                              |
|------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **SC \_ Управление \_ всем \_ доступом** (0xF003F)         | В дополнение ко всем правам доступа в этой таблице включает **стандартные \_ права \_**.                                                                                                                                                                                                                                                                                 |
| **SC \_ \_ \_ Служба создания диспетчера** (0x0002)      | Требуется для вызова функции [**CreateService**](/windows/desktop/api/Winsvc/nf-winsvc-createservicea) для создания объекта службы и его добавления в базу данных.                                                                                                                                                                                                                                              |
| **SC \_ Диспетчер \_ подключений** (0x0001)              | Требуется для подключения к диспетчеру управления службами.                                                                                                                                                                                                                                                                                                                      |
| **SC \_ \_ \_ Служба Enumerate Manager** (0x0004)   | Требуется для вызова функции [**енумсервицесстатус**](/windows/desktop/api/Winsvc/nf-winsvc-enumservicesstatusa) или [**енумсервицесстатусекс**](/windows/desktop/api/Winsvc/nf-winsvc-enumservicesstatusexa) для перечисления служб в базе данных.<br/> Требуется для вызова функции [**NotifyServiceStatusChange**](/windows/desktop/api/Winsvc/nf-winsvc-notifyservicestatuschangea) для получения уведомлений при создании или удалении какой-либо службы.<br/> |
| **SC \_ \_Блокировка руководителя** (0x0008)                 | Требуется для вызова функции [**локксервицедатабасе**](/windows/desktop/api/Winsvc/nf-winsvc-lockservicedatabase) для получения блокировки базы данных.                                                                                                                                                                                                                                                      |
| **SC \_ \_Изменение \_ \_ конфигурации загрузки Configuration Manager** (0x0020) | Требуется для вызова функции [**нотифибутконфигстатус**](/windows/desktop/api/Winsvc/nf-winsvc-notifybootconfigstatus) .                                                                                                                                                                                                                                                                                  |
| **SC \_ \_ \_ \_ Состояние блокировки запроса диспетчера** (0x0010)  | Требуется для вызова функции [**куерисервицелоккстатус**](/windows/desktop/api/Winsvc/nf-winsvc-queryservicelockstatusa) для получения сведений о состоянии блокировки базы данных.                                                                                                                                                                                                                         |



 

Ниже перечислены [универсальные права доступа](/windows/desktop/SecAuthZ/generic-access-rights) для SCM.



<table>
<thead>
<tr class="header">
<th>Право доступа</th>
<th>Описание</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><strong>GENERIC_READ</strong></td>
<td><dl> <strong>STANDARD_RIGHTS_READ</strong><br />
<strong>SC_MANAGER_ENUMERATE_SERVICE</strong><br />
<strong>SC_MANAGER_QUERY_LOCK_STATUS</strong><br />
</dl></td>
</tr>
<tr class="even">
<td><strong>GENERIC_WRITE</strong></td>
<td><dl> <strong>STANDARD_RIGHTS_WRITE</strong><br />
<strong>SC_MANAGER_CREATE_SERVICE</strong><br />
<strong>SC_MANAGER_MODIFY_BOOT_CONFIG</strong><br />
</dl></td>
</tr>
<tr class="odd">
<td><strong>GENERIC_EXECUTE</strong></td>
<td><dl> <strong>STANDARD_RIGHTS_EXECUTE</strong><br />
<strong>SC_MANAGER_CONNECT</strong><br />
<strong>SC_MANAGER_LOCK</strong><br />
</dl></td>
</tr>
<tr class="even">
<td><strong>GENERIC_ALL</strong></td>
<td><dl> <strong>SC_MANAGER_ALL_ACCESS</strong><br />
</dl></td>
</tr>
</tbody>
</table>



 

Процесс с правильными правами доступа может открыть обработчик SCM, который можно использовать в функциях [**OpenService**](/windows/desktop/api/Winsvc/nf-winsvc-openservicea), [**енумсервицесстатусекс**](/windows/desktop/api/Winsvc/nf-winsvc-enumservicesstatusexa)и [**куерисервицелоккстатус**](/windows/desktop/api/Winsvc/nf-winsvc-queryservicelockstatusa) . Только процессы с правами администратора могут открывать дескрипторы SCM, которые могут использоваться функциями [**CreateService**](/windows/desktop/api/Winsvc/nf-winsvc-createservicea) и [**локксервицедатабасе**](/windows/desktop/api/Winsvc/nf-winsvc-lockservicedatabase) .

Система создает дескриптор безопасности для SCM. Чтобы получить или задать дескриптор безопасности для SCM, используйте функции [**куерисервицеобжектсекурити**](/windows/desktop/api/winsvc/nf-winsvc-queryserviceobjectsecurity) и [**сетсервицеобжектсекурити**](/windows/desktop/api/winsvc/nf-winsvc-setserviceobjectsecurity) с дескриптором объекта SCManager.

**Windows Server 2003 и Windows XP:** В отличие от большинства других защищаемых объектов, дескриптор безопасности для SCM не может быть изменен. Это поведение изменилось по сравнению с Windows Server 2003 с пакетом обновления 1 (SP1).

Предоставляются следующие права доступа.



<table>
<thead>
<tr class="header">
<th>Учетная запись</th>
<th>Права доступа</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>Удаленные пользователи, прошедшие проверку подлинности</td>
<td><dl> <strong>SC_MANAGER_CONNECT</strong><br />
</dl></td>
</tr>
<tr class="even">
<td>Локальные пользователи, прошедшие проверку подлинности (включая LocalService и NetworkService);</td>
<td><dl> <strong>SC_MANAGER_CONNECT</strong><br />
<strong>SC_MANAGER_ENUMERATE_SERVICE</strong><br />
<strong>SC_MANAGER_QUERY_LOCK_STATUS</strong><br />
<strong>STANDARD_RIGHTS_READ</strong><br />
</dl></td>
</tr>
<tr class="odd">
<td>локальная система;</td>
<td><dl> <strong>SC_MANAGER_CONNECT</strong><br />
<strong>SC_MANAGER_ENUMERATE_SERVICE</strong><br />
<strong>SC_MANAGER_MODIFY_BOOT_CONFIG</strong><br />
<strong>SC_MANAGER_QUERY_LOCK_STATUS</strong><br />
<strong>STANDARD_RIGHTS_READ</strong><br />
</dl></td>
</tr>
<tr class="even">
<td>Администраторы</td>
<td><dl> <strong>SC_MANAGER_ALL_ACCESS</strong><br />
</dl></td>
</tr>
</tbody>
</table>



 

Обратите внимание, что удаленные пользователи, прошедшие проверку подлинности по сети, но не зарегистрированные в интерактивном режиме, могут подключаться к SCM, но не выполнять операции, для которых требуются другие права доступа. Для выполнения этих операций пользователь должен войти в систему в интерактивном режиме, или служба должна использовать одну из учетных записей служб.

**Windows Server 2003 и Windows XP:** Удаленным пользователям, прошедшим проверку подлинности, предоставляются службы **SC \_ Manager \_ Connect**, **SC \_ Manager \_ Enumerate \_ Service**, **SC \_ Manager \_ \_ Блокировка \_ запросов** и стандартные права доступа на **\_ \_ Чтение** . Эти права доступа ограничены, как описано в предыдущей таблице в Windows Server 2003 с пакетом обновления 1 (SP1)

Когда процесс использует функцию [**OpenSCManager**](/windows/desktop/api/Winsvc/nf-winsvc-openscmanagera) для открытия обработчика базы данных установленных служб, он может запросить права доступа. Перед предоставлением запрошенных прав доступа система проверяет безопасность дескриптора безопасности SCM.

## <a name="access-rights-for-a-service"></a>Права доступа для службы

Ниже перечислены определенные права доступа к службе.



| Право доступа                                | Описание                                                                                                                                                                                                                                                                                                                                                                          |
|---------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **Служба \_ ВСЕ \_ доступ** (0xF01FF)          | Включает **стандартные \_ права, \_ необходимые** в дополнение ко всем правам доступа в этой таблице.                                                                                                                                                                                                                                                                                              |
| **Служба \_ ИЗМЕНИТЬ \_ конфигурацию** (0x0002)        | Требуется для вызова функции [**чанжесервицеконфиг**](/windows/desktop/api/Winsvc/nf-winsvc-changeserviceconfiga) или [**ChangeServiceConfig2**](/windows/desktop/api/Winsvc/nf-winsvc-changeserviceconfig2a) для изменения конфигурации службы. Так как это дает участнику право изменять исполняемый файл, который система запускает, он должен быть предоставлен только администраторам.                                                              |
| **Служба \_ Перечисление \_ зависимых** объектов (0x0008) | Требуется для вызова функции [**енумдепендентсервицес**](/windows/desktop/api/Winsvc/nf-winsvc-enumdependentservicesa) для перечисления всех служб, зависящих от службы.                                                                                                                                                                                                                                         |
| **Служба \_ Опрос** (0x0080)           | Требуется для вызова функции [**ControlService**](/windows/desktop/api/Winsvc/nf-winsvc-controlservice) , чтобы попросить службу немедленно сообщить о своем состоянии.                                                                                                                                                                                                                                                          |
| **Служба \_ Приостановить \_ продолжение** (0x0040)       | Требуется для вызова функции [**ControlService**](/windows/desktop/api/Winsvc/nf-winsvc-controlservice) для приостановки или продолжения работы службы.                                                                                                                                                                                                                                                                             |
| **Служба \_ \_Конфигурация запроса** (0x0001)         | Требуется для вызова функций [**куерисервицеконфиг**](/windows/desktop/api/Winsvc/nf-winsvc-queryserviceconfiga) и [**QueryServiceConfig2**](/windows/desktop/api/Winsvc/nf-winsvc-queryserviceconfig2a) для запроса конфигурации службы.                                                                                                                                                                                                           |
| **Служба \_ \_Состояние запроса** (0x0004)         | Требуется для вызова функции [**куерисервицестатус**](/windows/desktop/api/Winsvc/nf-winsvc-queryservicestatus) или [**куерисервицестатусекс**](/windows/desktop/api/Winsvc/nf-winsvc-queryservicestatusex) , чтобы диспетчер управления службами запросил состояние службы.<br/> Требуется для вызова функции [**NotifyServiceStatusChange**](/windows/desktop/api/Winsvc/nf-winsvc-notifyservicestatuschangea) , чтобы получить уведомление при изменении состояния службы.<br/> |
| **Служба \_ Запуск** (0x0010)                 | Требуется для вызова функции [**StartService**](/windows/desktop/api/Winsvc/nf-winsvc-startservicea) для запуска службы.                                                                                                                                                                                                                                                                                             |
| **Служба \_ Прерывать** (0x0020)                  | Требуется для вызова функции [**ControlService**](/windows/desktop/api/Winsvc/nf-winsvc-controlservice) для завершения работы службы.                                                                                                                                                                                                                                                                                          |
| **Служба \_ \_Определяемый пользователем \_ элемент управления**(0x0100) | Требуется для вызова функции [**ControlService**](/windows/desktop/api/Winsvc/nf-winsvc-controlservice) , чтобы указать определяемый пользователем код элемента управления.                                                                                                                                                                                                                                                                       |



 

Ниже перечислены [стандартные права доступа](/windows/desktop/SecAuthZ/standard-access-rights) для службы.



| Право доступа                 | Описание                                                                                                                                                                                                                                                                                                                                                                                                                                  |
|------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **ДОСТУП \_ к \_ безопасности системы** | Требуется для вызова функции [**куерисервицеобжектсекурити**](/windows/desktop/api/winsvc/nf-winsvc-queryserviceobjectsecurity) или [**сетсервицеобжектсекурити**](/windows/desktop/api/winsvc/nf-winsvc-setserviceobjectsecurity) для доступа к SACL. Правильный способ получить такой доступ — включить [**привилегию**](/windows/desktop/SecAuthZ/privileges) **\_ \_ имени безопасности SE** в текущем маркере доступа вызывающего объекта, открыть маркер для доступа к **\_ системе \_ безопасности системы** , а затем отключить эту привилегию. |
| **Delete**   (0x10000)       | Требуется для вызова функции [**DeleteService**](/windows/desktop/api/Winsvc/nf-winsvc-deleteservice) для удаления службы.                                                                                                                                                                                                                                                                                                                                                  |
| **Чтение \_ Элемент управления**  (0x20000)    | Требуется для вызова функции [**куерисервицеобжектсекурити**](/windows/desktop/api/winsvc/nf-winsvc-queryserviceobjectsecurity) для запроса дескриптора безопасности объекта службы.                                                                                                                                                                                                                                                                                  |
| **Запись \_ DAC**  (0x40000)    | Требуется для вызова функции [**сетсервицеобжектсекурити**](/windows/desktop/api/winsvc/nf-winsvc-setserviceobjectsecurity) , чтобы изменить элемент **DACL** дескриптора безопасности объекта службы.                                                                                                                                                                                                                                                                   |
| **Запись \_ Владелец** (0x80000)   | Требуется для вызова функции [**сетсервицеобжектсекурити**](/windows/desktop/api/winsvc/nf-winsvc-setserviceobjectsecurity) для изменения **владельца** и членов **группы** дескриптора безопасности объекта службы.                                                                                                                                                                                                                                                   |



 

Ниже перечислены [универсальные права доступа](/windows/desktop/SecAuthZ/generic-access-rights) для службы.



<table>
<thead>
<tr class="header">
<th>Право доступа</th>
<th>Описание</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><strong>GENERIC_READ</strong></td>
<td><dl> <strong>STANDARD_RIGHTS_READ</strong><br />
<strong>SERVICE_QUERY_CONFIG</strong><br />
<strong>SERVICE_QUERY_STATUS</strong><br />
<strong>SERVICE_INTERROGATE</strong><br />
<strong>SERVICE_ENUMERATE_DEPENDENTS</strong><br />
</dl></td>
</tr>
<tr class="even">
<td><strong>GENERIC_WRITE</strong></td>
<td><dl> <strong>STANDARD_RIGHTS_WRITE</strong><br />
<strong>SERVICE_CHANGE_CONFIG</strong><br />
</dl></td>
</tr>
<tr class="odd">
<td><strong>GENERIC_EXECUTE</strong></td>
<td><dl> <strong>STANDARD_RIGHTS_EXECUTE</strong><br />
<strong>SERVICE_START</strong><br />
<strong>SERVICE_STOP</strong><br />
<strong>SERVICE_PAUSE_CONTINUE</strong><br />
<strong>SERVICE_USER_DEFINED_CONTROL</strong><br />
</dl></td>
</tr>
</tbody>
</table>



 

SCM создает дескриптор безопасности объекта службы, когда служба устанавливается с помощью функции [**CreateService**](/windows/desktop/api/Winsvc/nf-winsvc-createservicea) . Дескриптор безопасности по умолчанию объекта службы предоставляет следующий доступ.



<table>
<thead>
<tr class="header">
<th>Учетная запись</th>
<th>Права доступа</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>Удаленные пользователи, прошедшие проверку подлинности</td>
<td>По умолчанию не предоставлено. <strong>Windows Server 2003 с пакетом обновления 1 (SP1): SERVICE_USER_DEFINED_CONTROL</strong><br/> <strong>Windows Server 2003 и Windows XP:</strong> Права доступа для удаленных пользователей, прошедших проверку подлинности, совпадают с правами локальных пользователей, прошедших проверку подлинности.<br/></td>
</tr>
<tr class="even">
<td>Локальные пользователи, прошедшие проверку подлинности (включая LocalService и NetworkService);</td>
<td><dl> <strong>READ_CONTROL</strong><br />
<strong>SERVICE_ENUMERATE_DEPENDENTS</strong><br />
<strong>SERVICE_INTERROGATE</strong><br />
<strong>SERVICE_QUERY_CONFIG</strong><br />
<strong>SERVICE_QUERY_STATUS</strong><br />
<strong>SERVICE_USER_DEFINED_CONTROL</strong><br />
</dl></td>
</tr>
<tr class="odd">
<td>локальная система;</td>
<td><dl> <strong>READ_CONTROL</strong><br />
<strong>SERVICE_ENUMERATE_DEPENDENTS</strong><br />
<strong>SERVICE_INTERROGATE</strong><br />
<strong>SERVICE_PAUSE_CONTINUE</strong><br />
<strong>SERVICE_QUERY_CONFIG</strong><br />
<strong>SERVICE_QUERY_STATUS</strong><br />
<strong>SERVICE_START</strong><br />
<strong>SERVICE_STOP</strong><br />
<strong>SERVICE_USER_DEFINED_CONTROL</strong><br />
</dl></td>
</tr>
<tr class="even">
<td>Администраторы</td>
<td><dl> <strong>DELETE</strong><br />
<strong>READ_CONTROL</strong><br />
<strong>SERVICE_ALL_ACCESS</strong><br />
<strong>WRITE_DAC</strong><br />
<strong>WRITE_OWNER</strong><br />
</dl></td>
</tr>
</tbody>
</table>



 

Для выполнения любых операций пользователь должен войти в систему в интерактивном режиме, или служба должна использовать одну из учетных записей служб.

Чтобы получить или задать дескриптор безопасности для объекта службы, используйте функции [**куерисервицеобжектсекурити**](/windows/desktop/api/winsvc/nf-winsvc-queryserviceobjectsecurity) и [**сетсервицеобжектсекурити**](/windows/desktop/api/winsvc/nf-winsvc-setserviceobjectsecurity) . Дополнительные сведения см. [в разделе изменение списка DACL для службы](modifying-the-dacl-for-a-service.md).

Когда процесс использует функцию [**OpenService**](/windows/desktop/api/Winsvc/nf-winsvc-openservicea) , система проверяет запрошенные права доступа в отношении дескриптора безопасности для объекта службы.

Предоставление определенных прав доступа недоверенным пользователям (например, настройке **\_ изменения службы \_** или **ее \_ остановкой**) может привести к конфликту с выполнением службы и, возможно, позволит им запускать приложения под учетной записью LocalSystem.

Когда вызывается [**функция енумсервицесстатусекс**](/windows/desktop/api/Winsvc/nf-winsvc-enumservicesstatusexa) , если у вызывающего объекта нет права доступа к **\_ \_ состоянию запроса** на обслуживание службы, служба автоматически опускается из списка служб, возвращаемых клиенту.

 

