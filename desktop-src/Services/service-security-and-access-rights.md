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
# <a name="service-security-and-access-rights"></a><span data-ttu-id="926e9-103">Права доступа и безопасности службы</span><span class="sxs-lookup"><span data-stu-id="926e9-103">Service Security and Access Rights</span></span>

<span data-ttu-id="926e9-104">Модель безопасности Windows позволяет управлять доступом к диспетчеру управления службами (SCM) и объектам служб.</span><span class="sxs-lookup"><span data-stu-id="926e9-104">The Windows security model enables you to control access to the service control manager (SCM) and service objects.</span></span> <span data-ttu-id="926e9-105">Подробные сведения приведены в следующих разделах:</span><span class="sxs-lookup"><span data-stu-id="926e9-105">The following sections provide detailed information:</span></span>

-   [<span data-ttu-id="926e9-106">Права доступа для диспетчера управления службами</span><span class="sxs-lookup"><span data-stu-id="926e9-106">Access Rights for the Service Control Manager</span></span>](#access-rights-for-the-service-control-manager)
-   [<span data-ttu-id="926e9-107">Права доступа для службы</span><span class="sxs-lookup"><span data-stu-id="926e9-107">Access Rights for a Service</span></span>](#access-rights-for-a-service)

## <a name="access-rights-for-the-service-control-manager"></a><span data-ttu-id="926e9-108">Права доступа для диспетчера управления службами</span><span class="sxs-lookup"><span data-stu-id="926e9-108">Access Rights for the Service Control Manager</span></span>

<span data-ttu-id="926e9-109">Ниже перечислены особые права доступа к SCM.</span><span class="sxs-lookup"><span data-stu-id="926e9-109">The following are the specific access rights for the SCM.</span></span>



| <span data-ttu-id="926e9-110">Право доступа</span><span class="sxs-lookup"><span data-stu-id="926e9-110">Access right</span></span>                                   | <span data-ttu-id="926e9-111">Описание</span><span class="sxs-lookup"><span data-stu-id="926e9-111">Description</span></span>                                                                                                                                                                                                                                                                                                                                                              |
|------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="926e9-112">**SC \_ Управление \_ всем \_ доступом** (0xF003F)</span><span class="sxs-lookup"><span data-stu-id="926e9-112">**SC\_MANAGER\_ALL\_ACCESS** (0xF003F)</span></span>         | <span data-ttu-id="926e9-113">В дополнение ко всем правам доступа в этой таблице включает **стандартные \_ права \_**.</span><span class="sxs-lookup"><span data-stu-id="926e9-113">Includes **STANDARD\_RIGHTS\_REQUIRED**, in addition to all access rights in this table.</span></span>                                                                                                                                                                                                                                                                                 |
| <span data-ttu-id="926e9-114">**SC \_ \_ \_ Служба создания диспетчера** (0x0002)</span><span class="sxs-lookup"><span data-stu-id="926e9-114">**SC\_MANAGER\_CREATE\_SERVICE** (0x0002)</span></span>      | <span data-ttu-id="926e9-115">Требуется для вызова функции [**CreateService**](/windows/desktop/api/Winsvc/nf-winsvc-createservicea) для создания объекта службы и его добавления в базу данных.</span><span class="sxs-lookup"><span data-stu-id="926e9-115">Required to call the [**CreateService**](/windows/desktop/api/Winsvc/nf-winsvc-createservicea) function to create a service object and add it to the database.</span></span>                                                                                                                                                                                                                                              |
| <span data-ttu-id="926e9-116">**SC \_ Диспетчер \_ подключений** (0x0001)</span><span class="sxs-lookup"><span data-stu-id="926e9-116">**SC\_MANAGER\_CONNECT** (0x0001)</span></span>              | <span data-ttu-id="926e9-117">Требуется для подключения к диспетчеру управления службами.</span><span class="sxs-lookup"><span data-stu-id="926e9-117">Required to connect to the service control manager.</span></span>                                                                                                                                                                                                                                                                                                                      |
| <span data-ttu-id="926e9-118">**SC \_ \_ \_ Служба Enumerate Manager** (0x0004)</span><span class="sxs-lookup"><span data-stu-id="926e9-118">**SC\_MANAGER\_ENUMERATE\_SERVICE** (0x0004)</span></span>   | <span data-ttu-id="926e9-119">Требуется для вызова функции [**енумсервицесстатус**](/windows/desktop/api/Winsvc/nf-winsvc-enumservicesstatusa) или [**енумсервицесстатусекс**](/windows/desktop/api/Winsvc/nf-winsvc-enumservicesstatusexa) для перечисления служб в базе данных.</span><span class="sxs-lookup"><span data-stu-id="926e9-119">Required to call the [**EnumServicesStatus**](/windows/desktop/api/Winsvc/nf-winsvc-enumservicesstatusa) or [**EnumServicesStatusEx**](/windows/desktop/api/Winsvc/nf-winsvc-enumservicesstatusexa) function to list the services that are in the database.</span></span><br/> <span data-ttu-id="926e9-120">Требуется для вызова функции [**NotifyServiceStatusChange**](/windows/desktop/api/Winsvc/nf-winsvc-notifyservicestatuschangea) для получения уведомлений при создании или удалении какой-либо службы.</span><span class="sxs-lookup"><span data-stu-id="926e9-120">Required to call the [**NotifyServiceStatusChange**](/windows/desktop/api/Winsvc/nf-winsvc-notifyservicestatuschangea) function to receive notification when any service is created or deleted.</span></span><br/> |
| <span data-ttu-id="926e9-121">**SC \_ \_Блокировка руководителя** (0x0008)</span><span class="sxs-lookup"><span data-stu-id="926e9-121">**SC\_MANAGER\_LOCK** (0x0008)</span></span>                 | <span data-ttu-id="926e9-122">Требуется для вызова функции [**локксервицедатабасе**](/windows/desktop/api/Winsvc/nf-winsvc-lockservicedatabase) для получения блокировки базы данных.</span><span class="sxs-lookup"><span data-stu-id="926e9-122">Required to call the [**LockServiceDatabase**](/windows/desktop/api/Winsvc/nf-winsvc-lockservicedatabase) function to acquire a lock on the database.</span></span>                                                                                                                                                                                                                                                      |
| <span data-ttu-id="926e9-123">**SC \_ \_Изменение \_ \_ конфигурации загрузки Configuration Manager** (0x0020)</span><span class="sxs-lookup"><span data-stu-id="926e9-123">**SC\_MANAGER\_MODIFY\_BOOT\_CONFIG** (0x0020)</span></span> | <span data-ttu-id="926e9-124">Требуется для вызова функции [**нотифибутконфигстатус**](/windows/desktop/api/Winsvc/nf-winsvc-notifybootconfigstatus) .</span><span class="sxs-lookup"><span data-stu-id="926e9-124">Required to call the [**NotifyBootConfigStatus**](/windows/desktop/api/Winsvc/nf-winsvc-notifybootconfigstatus) function.</span></span>                                                                                                                                                                                                                                                                                  |
| <span data-ttu-id="926e9-125">**SC \_ \_ \_ \_ Состояние блокировки запроса диспетчера** (0x0010)</span><span class="sxs-lookup"><span data-stu-id="926e9-125">**SC\_MANAGER\_QUERY\_LOCK\_STATUS** (0x0010)</span></span>  | <span data-ttu-id="926e9-126">Требуется для вызова функции [**куерисервицелоккстатус**](/windows/desktop/api/Winsvc/nf-winsvc-queryservicelockstatusa) для получения сведений о состоянии блокировки базы данных.</span><span class="sxs-lookup"><span data-stu-id="926e9-126">Required to call the [**QueryServiceLockStatus**](/windows/desktop/api/Winsvc/nf-winsvc-queryservicelockstatusa) function to retrieve the lock status information for the database.</span></span>                                                                                                                                                                                                                         |



 

<span data-ttu-id="926e9-127">Ниже перечислены [универсальные права доступа](/windows/desktop/SecAuthZ/generic-access-rights) для SCM.</span><span class="sxs-lookup"><span data-stu-id="926e9-127">The following are the [generic access rights](/windows/desktop/SecAuthZ/generic-access-rights) for the SCM.</span></span>



<table>
<thead>
<tr class="header">
<th><span data-ttu-id="926e9-128">Право доступа</span><span class="sxs-lookup"><span data-stu-id="926e9-128">Access right</span></span></th>
<th><span data-ttu-id="926e9-129">Описание</span><span class="sxs-lookup"><span data-stu-id="926e9-129">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="926e9-130"><strong>GENERIC_READ</strong></span><span class="sxs-lookup"><span data-stu-id="926e9-130"><strong>GENERIC_READ</strong></span></span></td>
<td><dl> <span data-ttu-id="926e9-131"><strong>STANDARD_RIGHTS_READ</strong></span><span class="sxs-lookup"><span data-stu-id="926e9-131"><strong>STANDARD_RIGHTS_READ</strong></span></span><br /><span data-ttu-id="926e9-132">
<strong>SC_MANAGER_ENUMERATE_SERVICE</strong></span><span class="sxs-lookup"><span data-stu-id="926e9-132">
<strong>SC_MANAGER_ENUMERATE_SERVICE</strong></span></span><br /><span data-ttu-id="926e9-133">
<strong>SC_MANAGER_QUERY_LOCK_STATUS</strong></span><span class="sxs-lookup"><span data-stu-id="926e9-133">
<strong>SC_MANAGER_QUERY_LOCK_STATUS</strong></span></span><br />
</dl></td>
</tr>
<tr class="even">
<td><span data-ttu-id="926e9-134"><strong>GENERIC_WRITE</strong></span><span class="sxs-lookup"><span data-stu-id="926e9-134"><strong>GENERIC_WRITE</strong></span></span></td>
<td><dl> <span data-ttu-id="926e9-135"><strong>STANDARD_RIGHTS_WRITE</strong></span><span class="sxs-lookup"><span data-stu-id="926e9-135"><strong>STANDARD_RIGHTS_WRITE</strong></span></span><br /><span data-ttu-id="926e9-136">
<strong>SC_MANAGER_CREATE_SERVICE</strong></span><span class="sxs-lookup"><span data-stu-id="926e9-136">
<strong>SC_MANAGER_CREATE_SERVICE</strong></span></span><br /><span data-ttu-id="926e9-137">
<strong>SC_MANAGER_MODIFY_BOOT_CONFIG</strong></span><span class="sxs-lookup"><span data-stu-id="926e9-137">
<strong>SC_MANAGER_MODIFY_BOOT_CONFIG</strong></span></span><br />
</dl></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="926e9-138"><strong>GENERIC_EXECUTE</strong></span><span class="sxs-lookup"><span data-stu-id="926e9-138"><strong>GENERIC_EXECUTE</strong></span></span></td>
<td><dl> <span data-ttu-id="926e9-139"><strong>STANDARD_RIGHTS_EXECUTE</strong></span><span class="sxs-lookup"><span data-stu-id="926e9-139"><strong>STANDARD_RIGHTS_EXECUTE</strong></span></span><br /><span data-ttu-id="926e9-140">
<strong>SC_MANAGER_CONNECT</strong></span><span class="sxs-lookup"><span data-stu-id="926e9-140">
<strong>SC_MANAGER_CONNECT</strong></span></span><br /><span data-ttu-id="926e9-141">
<strong>SC_MANAGER_LOCK</strong></span><span class="sxs-lookup"><span data-stu-id="926e9-141">
<strong>SC_MANAGER_LOCK</strong></span></span><br />
</dl></td>
</tr>
<tr class="even">
<td><span data-ttu-id="926e9-142"><strong>GENERIC_ALL</strong></span><span class="sxs-lookup"><span data-stu-id="926e9-142"><strong>GENERIC_ALL</strong></span></span></td>
<td><dl> <span data-ttu-id="926e9-143"><strong>SC_MANAGER_ALL_ACCESS</strong></span><span class="sxs-lookup"><span data-stu-id="926e9-143"><strong>SC_MANAGER_ALL_ACCESS</strong></span></span><br />
</dl></td>
</tr>
</tbody>
</table>



 

<span data-ttu-id="926e9-144">Процесс с правильными правами доступа может открыть обработчик SCM, который можно использовать в функциях [**OpenService**](/windows/desktop/api/Winsvc/nf-winsvc-openservicea), [**енумсервицесстатусекс**](/windows/desktop/api/Winsvc/nf-winsvc-enumservicesstatusexa)и [**куерисервицелоккстатус**](/windows/desktop/api/Winsvc/nf-winsvc-queryservicelockstatusa) .</span><span class="sxs-lookup"><span data-stu-id="926e9-144">A process with the correct access rights can open a handle to the SCM that can be used in the [**OpenService**](/windows/desktop/api/Winsvc/nf-winsvc-openservicea), [**EnumServicesStatusEx**](/windows/desktop/api/Winsvc/nf-winsvc-enumservicesstatusexa), and [**QueryServiceLockStatus**](/windows/desktop/api/Winsvc/nf-winsvc-queryservicelockstatusa) functions.</span></span> <span data-ttu-id="926e9-145">Только процессы с правами администратора могут открывать дескрипторы SCM, которые могут использоваться функциями [**CreateService**](/windows/desktop/api/Winsvc/nf-winsvc-createservicea) и [**локксервицедатабасе**](/windows/desktop/api/Winsvc/nf-winsvc-lockservicedatabase) .</span><span class="sxs-lookup"><span data-stu-id="926e9-145">Only processes with Administrator privileges are able to open handles to the SCM that can be used by the [**CreateService**](/windows/desktop/api/Winsvc/nf-winsvc-createservicea) and [**LockServiceDatabase**](/windows/desktop/api/Winsvc/nf-winsvc-lockservicedatabase) functions.</span></span>

<span data-ttu-id="926e9-146">Система создает дескриптор безопасности для SCM.</span><span class="sxs-lookup"><span data-stu-id="926e9-146">The system creates the security descriptor for the SCM.</span></span> <span data-ttu-id="926e9-147">Чтобы получить или задать дескриптор безопасности для SCM, используйте функции [**куерисервицеобжектсекурити**](/windows/desktop/api/winsvc/nf-winsvc-queryserviceobjectsecurity) и [**сетсервицеобжектсекурити**](/windows/desktop/api/winsvc/nf-winsvc-setserviceobjectsecurity) с дескриптором объекта SCManager.</span><span class="sxs-lookup"><span data-stu-id="926e9-147">To get or set the security descriptor for the SCM, use the [**QueryServiceObjectSecurity**](/windows/desktop/api/winsvc/nf-winsvc-queryserviceobjectsecurity) and [**SetServiceObjectSecurity**](/windows/desktop/api/winsvc/nf-winsvc-setserviceobjectsecurity) functions with a handle to the SCManager object.</span></span>

<span data-ttu-id="926e9-148">**Windows Server 2003 и Windows XP:** В отличие от большинства других защищаемых объектов, дескриптор безопасности для SCM не может быть изменен.</span><span class="sxs-lookup"><span data-stu-id="926e9-148">**Windows Server 2003 and Windows XP:** Unlike most other securable objects, the security descriptor for the SCM cannot be modified.</span></span> <span data-ttu-id="926e9-149">Это поведение изменилось по сравнению с Windows Server 2003 с пакетом обновления 1 (SP1).</span><span class="sxs-lookup"><span data-stu-id="926e9-149">This behavior has changed as of Windows Server 2003 with Service Pack 1 (SP1).</span></span>

<span data-ttu-id="926e9-150">Предоставляются следующие права доступа.</span><span class="sxs-lookup"><span data-stu-id="926e9-150">The following access rights are granted.</span></span>



<table>
<thead>
<tr class="header">
<th><span data-ttu-id="926e9-151">Учетная запись</span><span class="sxs-lookup"><span data-stu-id="926e9-151">Account</span></span></th>
<th><span data-ttu-id="926e9-152">Права доступа</span><span class="sxs-lookup"><span data-stu-id="926e9-152">Access rights</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="926e9-153">Удаленные пользователи, прошедшие проверку подлинности</span><span class="sxs-lookup"><span data-stu-id="926e9-153">Remote authenticated users</span></span></td>
<td><dl> <span data-ttu-id="926e9-154"><strong>SC_MANAGER_CONNECT</strong></span><span class="sxs-lookup"><span data-stu-id="926e9-154"><strong>SC_MANAGER_CONNECT</strong></span></span><br />
</dl></td>
</tr>
<tr class="even">
<td><span data-ttu-id="926e9-155">Локальные пользователи, прошедшие проверку подлинности (включая LocalService и NetworkService);</span><span class="sxs-lookup"><span data-stu-id="926e9-155">Local authenticated users (including LocalService and NetworkService)</span></span></td>
<td><dl> <span data-ttu-id="926e9-156"><strong>SC_MANAGER_CONNECT</strong></span><span class="sxs-lookup"><span data-stu-id="926e9-156"><strong>SC_MANAGER_CONNECT</strong></span></span><br /><span data-ttu-id="926e9-157">
<strong>SC_MANAGER_ENUMERATE_SERVICE</strong></span><span class="sxs-lookup"><span data-stu-id="926e9-157">
<strong>SC_MANAGER_ENUMERATE_SERVICE</strong></span></span><br /><span data-ttu-id="926e9-158">
<strong>SC_MANAGER_QUERY_LOCK_STATUS</strong></span><span class="sxs-lookup"><span data-stu-id="926e9-158">
<strong>SC_MANAGER_QUERY_LOCK_STATUS</strong></span></span><br /><span data-ttu-id="926e9-159">
<strong>STANDARD_RIGHTS_READ</strong></span><span class="sxs-lookup"><span data-stu-id="926e9-159">
<strong>STANDARD_RIGHTS_READ</strong></span></span><br />
</dl></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="926e9-160">локальная система;</span><span class="sxs-lookup"><span data-stu-id="926e9-160">LocalSystem</span></span></td>
<td><dl> <span data-ttu-id="926e9-161"><strong>SC_MANAGER_CONNECT</strong></span><span class="sxs-lookup"><span data-stu-id="926e9-161"><strong>SC_MANAGER_CONNECT</strong></span></span><br /><span data-ttu-id="926e9-162">
<strong>SC_MANAGER_ENUMERATE_SERVICE</strong></span><span class="sxs-lookup"><span data-stu-id="926e9-162">
<strong>SC_MANAGER_ENUMERATE_SERVICE</strong></span></span><br /><span data-ttu-id="926e9-163">
<strong>SC_MANAGER_MODIFY_BOOT_CONFIG</strong></span><span class="sxs-lookup"><span data-stu-id="926e9-163">
<strong>SC_MANAGER_MODIFY_BOOT_CONFIG</strong></span></span><br /><span data-ttu-id="926e9-164">
<strong>SC_MANAGER_QUERY_LOCK_STATUS</strong></span><span class="sxs-lookup"><span data-stu-id="926e9-164">
<strong>SC_MANAGER_QUERY_LOCK_STATUS</strong></span></span><br /><span data-ttu-id="926e9-165">
<strong>STANDARD_RIGHTS_READ</strong></span><span class="sxs-lookup"><span data-stu-id="926e9-165">
<strong>STANDARD_RIGHTS_READ</strong></span></span><br />
</dl></td>
</tr>
<tr class="even">
<td><span data-ttu-id="926e9-166">Администраторы</span><span class="sxs-lookup"><span data-stu-id="926e9-166">Administrators</span></span></td>
<td><dl> <span data-ttu-id="926e9-167"><strong>SC_MANAGER_ALL_ACCESS</strong></span><span class="sxs-lookup"><span data-stu-id="926e9-167"><strong>SC_MANAGER_ALL_ACCESS</strong></span></span><br />
</dl></td>
</tr>
</tbody>
</table>



 

<span data-ttu-id="926e9-168">Обратите внимание, что удаленные пользователи, прошедшие проверку подлинности по сети, но не зарегистрированные в интерактивном режиме, могут подключаться к SCM, но не выполнять операции, для которых требуются другие права доступа.</span><span class="sxs-lookup"><span data-stu-id="926e9-168">Notice that remote users authenticated over the network but not interactively logged on can connect to the SCM but not perform operations that require other access rights.</span></span> <span data-ttu-id="926e9-169">Для выполнения этих операций пользователь должен войти в систему в интерактивном режиме, или служба должна использовать одну из учетных записей служб.</span><span class="sxs-lookup"><span data-stu-id="926e9-169">To perform these operations, the user must be logged on interactively or the service must use one of the service accounts.</span></span>

<span data-ttu-id="926e9-170">**Windows Server 2003 и Windows XP:** Удаленным пользователям, прошедшим проверку подлинности, предоставляются службы **SC \_ Manager \_ Connect**, **SC \_ Manager \_ Enumerate \_ Service**, **SC \_ Manager \_ \_ Блокировка \_ запросов** и стандартные права доступа на **\_ \_ Чтение** .</span><span class="sxs-lookup"><span data-stu-id="926e9-170">**Windows Server 2003 and Windows XP:** Remote authenticated users are granted the **SC\_MANAGER\_CONNECT**, **SC\_MANAGER\_ENUMERATE\_SERVICE**, **SC\_MANAGER\_QUERY\_LOCK\_STATUS**, and **STANDARD\_RIGHTS\_READ** access rights.</span></span> <span data-ttu-id="926e9-171">Эти права доступа ограничены, как описано в предыдущей таблице в Windows Server 2003 с пакетом обновления 1 (SP1)</span><span class="sxs-lookup"><span data-stu-id="926e9-171">These access rights are restricted as described in the previous table as of Windows Server 2003 with SP1</span></span>

<span data-ttu-id="926e9-172">Когда процесс использует функцию [**OpenSCManager**](/windows/desktop/api/Winsvc/nf-winsvc-openscmanagera) для открытия обработчика базы данных установленных служб, он может запросить права доступа.</span><span class="sxs-lookup"><span data-stu-id="926e9-172">When a process uses the [**OpenSCManager**](/windows/desktop/api/Winsvc/nf-winsvc-openscmanagera) function to open a handle to a database of installed services, it can request access rights.</span></span> <span data-ttu-id="926e9-173">Перед предоставлением запрошенных прав доступа система проверяет безопасность дескриптора безопасности SCM.</span><span class="sxs-lookup"><span data-stu-id="926e9-173">The system performs a security check against the security descriptor for the SCM before granting the requested access rights.</span></span>

## <a name="access-rights-for-a-service"></a><span data-ttu-id="926e9-174">Права доступа для службы</span><span class="sxs-lookup"><span data-stu-id="926e9-174">Access Rights for a Service</span></span>

<span data-ttu-id="926e9-175">Ниже перечислены определенные права доступа к службе.</span><span class="sxs-lookup"><span data-stu-id="926e9-175">The following are the specific access rights for a service.</span></span>



| <span data-ttu-id="926e9-176">Право доступа</span><span class="sxs-lookup"><span data-stu-id="926e9-176">Access right</span></span>                                | <span data-ttu-id="926e9-177">Описание</span><span class="sxs-lookup"><span data-stu-id="926e9-177">Description</span></span>                                                                                                                                                                                                                                                                                                                                                                          |
|---------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="926e9-178">**Служба \_ ВСЕ \_ доступ** (0xF01FF)</span><span class="sxs-lookup"><span data-stu-id="926e9-178">**SERVICE\_ALL\_ACCESS** (0xF01FF)</span></span>          | <span data-ttu-id="926e9-179">Включает **стандартные \_ права, \_ необходимые** в дополнение ко всем правам доступа в этой таблице.</span><span class="sxs-lookup"><span data-stu-id="926e9-179">Includes **STANDARD\_RIGHTS\_REQUIRED** in addition to all access rights in this table.</span></span>                                                                                                                                                                                                                                                                                              |
| <span data-ttu-id="926e9-180">**Служба \_ ИЗМЕНИТЬ \_ конфигурацию** (0x0002)</span><span class="sxs-lookup"><span data-stu-id="926e9-180">**SERVICE\_CHANGE\_CONFIG** (0x0002)</span></span>        | <span data-ttu-id="926e9-181">Требуется для вызова функции [**чанжесервицеконфиг**](/windows/desktop/api/Winsvc/nf-winsvc-changeserviceconfiga) или [**ChangeServiceConfig2**](/windows/desktop/api/Winsvc/nf-winsvc-changeserviceconfig2a) для изменения конфигурации службы.</span><span class="sxs-lookup"><span data-stu-id="926e9-181">Required to call the [**ChangeServiceConfig**](/windows/desktop/api/Winsvc/nf-winsvc-changeserviceconfiga) or [**ChangeServiceConfig2**](/windows/desktop/api/Winsvc/nf-winsvc-changeserviceconfig2a) function to change the service configuration.</span></span> <span data-ttu-id="926e9-182">Так как это дает участнику право изменять исполняемый файл, который система запускает, он должен быть предоставлен только администраторам.</span><span class="sxs-lookup"><span data-stu-id="926e9-182">Because this grants the caller the right to change the executable file that the system runs, it should be granted only to administrators.</span></span>                                                              |
| <span data-ttu-id="926e9-183">**Служба \_ Перечисление \_ зависимых** объектов (0x0008)</span><span class="sxs-lookup"><span data-stu-id="926e9-183">**SERVICE\_ENUMERATE\_DEPENDENTS** (0x0008)</span></span> | <span data-ttu-id="926e9-184">Требуется для вызова функции [**енумдепендентсервицес**](/windows/desktop/api/Winsvc/nf-winsvc-enumdependentservicesa) для перечисления всех служб, зависящих от службы.</span><span class="sxs-lookup"><span data-stu-id="926e9-184">Required to call the [**EnumDependentServices**](/windows/desktop/api/Winsvc/nf-winsvc-enumdependentservicesa) function to enumerate all the services dependent on the service.</span></span>                                                                                                                                                                                                                                         |
| <span data-ttu-id="926e9-185">**Служба \_ Опрос** (0x0080)</span><span class="sxs-lookup"><span data-stu-id="926e9-185">**SERVICE\_INTERROGATE** (0x0080)</span></span>           | <span data-ttu-id="926e9-186">Требуется для вызова функции [**ControlService**](/windows/desktop/api/Winsvc/nf-winsvc-controlservice) , чтобы попросить службу немедленно сообщить о своем состоянии.</span><span class="sxs-lookup"><span data-stu-id="926e9-186">Required to call the [**ControlService**](/windows/desktop/api/Winsvc/nf-winsvc-controlservice) function to ask the service to report its status immediately.</span></span>                                                                                                                                                                                                                                                          |
| <span data-ttu-id="926e9-187">**Служба \_ Приостановить \_ продолжение** (0x0040)</span><span class="sxs-lookup"><span data-stu-id="926e9-187">**SERVICE\_PAUSE\_CONTINUE** (0x0040)</span></span>       | <span data-ttu-id="926e9-188">Требуется для вызова функции [**ControlService**](/windows/desktop/api/Winsvc/nf-winsvc-controlservice) для приостановки или продолжения работы службы.</span><span class="sxs-lookup"><span data-stu-id="926e9-188">Required to call the [**ControlService**](/windows/desktop/api/Winsvc/nf-winsvc-controlservice) function to pause or continue the service.</span></span>                                                                                                                                                                                                                                                                             |
| <span data-ttu-id="926e9-189">**Служба \_ \_Конфигурация запроса** (0x0001)</span><span class="sxs-lookup"><span data-stu-id="926e9-189">**SERVICE\_QUERY\_CONFIG** (0x0001)</span></span>         | <span data-ttu-id="926e9-190">Требуется для вызова функций [**куерисервицеконфиг**](/windows/desktop/api/Winsvc/nf-winsvc-queryserviceconfiga) и [**QueryServiceConfig2**](/windows/desktop/api/Winsvc/nf-winsvc-queryserviceconfig2a) для запроса конфигурации службы.</span><span class="sxs-lookup"><span data-stu-id="926e9-190">Required to call the [**QueryServiceConfig**](/windows/desktop/api/Winsvc/nf-winsvc-queryserviceconfiga) and [**QueryServiceConfig2**](/windows/desktop/api/Winsvc/nf-winsvc-queryserviceconfig2a) functions to query the service configuration.</span></span>                                                                                                                                                                                                           |
| <span data-ttu-id="926e9-191">**Служба \_ \_Состояние запроса** (0x0004)</span><span class="sxs-lookup"><span data-stu-id="926e9-191">**SERVICE\_QUERY\_STATUS** (0x0004)</span></span>         | <span data-ttu-id="926e9-192">Требуется для вызова функции [**куерисервицестатус**](/windows/desktop/api/Winsvc/nf-winsvc-queryservicestatus) или [**куерисервицестатусекс**](/windows/desktop/api/Winsvc/nf-winsvc-queryservicestatusex) , чтобы диспетчер управления службами запросил состояние службы.</span><span class="sxs-lookup"><span data-stu-id="926e9-192">Required to call the [**QueryServiceStatus**](/windows/desktop/api/Winsvc/nf-winsvc-queryservicestatus) or [**QueryServiceStatusEx**](/windows/desktop/api/Winsvc/nf-winsvc-queryservicestatusex) function to ask the service control manager about the status of the service.</span></span><br/> <span data-ttu-id="926e9-193">Требуется для вызова функции [**NotifyServiceStatusChange**](/windows/desktop/api/Winsvc/nf-winsvc-notifyservicestatuschangea) , чтобы получить уведомление при изменении состояния службы.</span><span class="sxs-lookup"><span data-stu-id="926e9-193">Required to call the [**NotifyServiceStatusChange**](/windows/desktop/api/Winsvc/nf-winsvc-notifyservicestatuschangea) function to receive notification when a service changes status.</span></span><br/> |
| <span data-ttu-id="926e9-194">**Служба \_ Запуск** (0x0010)</span><span class="sxs-lookup"><span data-stu-id="926e9-194">**SERVICE\_START** (0x0010)</span></span>                 | <span data-ttu-id="926e9-195">Требуется для вызова функции [**StartService**](/windows/desktop/api/Winsvc/nf-winsvc-startservicea) для запуска службы.</span><span class="sxs-lookup"><span data-stu-id="926e9-195">Required to call the [**StartService**](/windows/desktop/api/Winsvc/nf-winsvc-startservicea) function to start the service.</span></span>                                                                                                                                                                                                                                                                                             |
| <span data-ttu-id="926e9-196">**Служба \_ Прерывать** (0x0020)</span><span class="sxs-lookup"><span data-stu-id="926e9-196">**SERVICE\_STOP** (0x0020)</span></span>                  | <span data-ttu-id="926e9-197">Требуется для вызова функции [**ControlService**](/windows/desktop/api/Winsvc/nf-winsvc-controlservice) для завершения работы службы.</span><span class="sxs-lookup"><span data-stu-id="926e9-197">Required to call the [**ControlService**](/windows/desktop/api/Winsvc/nf-winsvc-controlservice) function to stop the service.</span></span>                                                                                                                                                                                                                                                                                          |
| <span data-ttu-id="926e9-198">**Служба \_ \_Определяемый пользователем \_ элемент управления**(0x0100)</span><span class="sxs-lookup"><span data-stu-id="926e9-198">**SERVICE\_USER\_DEFINED\_CONTROL**(0x0100)</span></span> | <span data-ttu-id="926e9-199">Требуется для вызова функции [**ControlService**](/windows/desktop/api/Winsvc/nf-winsvc-controlservice) , чтобы указать определяемый пользователем код элемента управления.</span><span class="sxs-lookup"><span data-stu-id="926e9-199">Required to call the [**ControlService**](/windows/desktop/api/Winsvc/nf-winsvc-controlservice) function to specify a user-defined control code.</span></span>                                                                                                                                                                                                                                                                       |



 

<span data-ttu-id="926e9-200">Ниже перечислены [стандартные права доступа](/windows/desktop/SecAuthZ/standard-access-rights) для службы.</span><span class="sxs-lookup"><span data-stu-id="926e9-200">The following are the [standard access rights](/windows/desktop/SecAuthZ/standard-access-rights) for a service.</span></span>



| <span data-ttu-id="926e9-201">Право доступа</span><span class="sxs-lookup"><span data-stu-id="926e9-201">Access right</span></span>                 | <span data-ttu-id="926e9-202">Описание</span><span class="sxs-lookup"><span data-stu-id="926e9-202">Description</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                                  |
|------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="926e9-203">**ДОСТУП \_ к \_ безопасности системы**</span><span class="sxs-lookup"><span data-stu-id="926e9-203">**ACCESS\_SYSTEM\_SECURITY**</span></span> | <span data-ttu-id="926e9-204">Требуется для вызова функции [**куерисервицеобжектсекурити**](/windows/desktop/api/winsvc/nf-winsvc-queryserviceobjectsecurity) или [**сетсервицеобжектсекурити**](/windows/desktop/api/winsvc/nf-winsvc-setserviceobjectsecurity) для доступа к SACL.</span><span class="sxs-lookup"><span data-stu-id="926e9-204">Required to call the [**QueryServiceObjectSecurity**](/windows/desktop/api/winsvc/nf-winsvc-queryserviceobjectsecurity) or [**SetServiceObjectSecurity**](/windows/desktop/api/winsvc/nf-winsvc-setserviceobjectsecurity) function to access the SACL.</span></span> <span data-ttu-id="926e9-205">Правильный способ получить такой доступ — включить [**привилегию**](/windows/desktop/SecAuthZ/privileges) **\_ \_ имени безопасности SE** в текущем маркере доступа вызывающего объекта, открыть маркер для доступа к **\_ системе \_ безопасности системы** , а затем отключить эту привилегию.</span><span class="sxs-lookup"><span data-stu-id="926e9-205">The proper way to obtain this access is to enable the **SE\_SECURITY\_NAME**[**privilege**](/windows/desktop/SecAuthZ/privileges) in the caller's current access token, open the handle for **ACCESS\_SYSTEM\_SECURITY** access, and then disable the privilege.</span></span> |
| <span data-ttu-id="926e9-206">**Delete**   (0x10000)</span><span class="sxs-lookup"><span data-stu-id="926e9-206">**DELETE**   (0x10000)</span></span>       | <span data-ttu-id="926e9-207">Требуется для вызова функции [**DeleteService**](/windows/desktop/api/Winsvc/nf-winsvc-deleteservice) для удаления службы.</span><span class="sxs-lookup"><span data-stu-id="926e9-207">Required to call the [**DeleteService**](/windows/desktop/api/Winsvc/nf-winsvc-deleteservice) function to delete the service.</span></span>                                                                                                                                                                                                                                                                                                                                                  |
| <span data-ttu-id="926e9-208">**Чтение \_ Элемент управления**  (0x20000)</span><span class="sxs-lookup"><span data-stu-id="926e9-208">**READ\_CONTROL**  (0x20000)</span></span>    | <span data-ttu-id="926e9-209">Требуется для вызова функции [**куерисервицеобжектсекурити**](/windows/desktop/api/winsvc/nf-winsvc-queryserviceobjectsecurity) для запроса дескриптора безопасности объекта службы.</span><span class="sxs-lookup"><span data-stu-id="926e9-209">Required to call the [**QueryServiceObjectSecurity**](/windows/desktop/api/winsvc/nf-winsvc-queryserviceobjectsecurity) function to query the security descriptor of the service object.</span></span>                                                                                                                                                                                                                                                                                  |
| <span data-ttu-id="926e9-210">**Запись \_ DAC**  (0x40000)</span><span class="sxs-lookup"><span data-stu-id="926e9-210">**WRITE\_DAC**  (0x40000)</span></span>    | <span data-ttu-id="926e9-211">Требуется для вызова функции [**сетсервицеобжектсекурити**](/windows/desktop/api/winsvc/nf-winsvc-setserviceobjectsecurity) , чтобы изменить элемент **DACL** дескриптора безопасности объекта службы.</span><span class="sxs-lookup"><span data-stu-id="926e9-211">Required to call the [**SetServiceObjectSecurity**](/windows/desktop/api/winsvc/nf-winsvc-setserviceobjectsecurity) function to modify the **Dacl** member of the service object's security descriptor.</span></span>                                                                                                                                                                                                                                                                   |
| <span data-ttu-id="926e9-212">**Запись \_ Владелец** (0x80000)</span><span class="sxs-lookup"><span data-stu-id="926e9-212">**WRITE\_OWNER** (0x80000)</span></span>   | <span data-ttu-id="926e9-213">Требуется для вызова функции [**сетсервицеобжектсекурити**](/windows/desktop/api/winsvc/nf-winsvc-setserviceobjectsecurity) для изменения **владельца** и членов **группы** дескриптора безопасности объекта службы.</span><span class="sxs-lookup"><span data-stu-id="926e9-213">Required to call the [**SetServiceObjectSecurity**](/windows/desktop/api/winsvc/nf-winsvc-setserviceobjectsecurity) function to modify the **Owner** and **Group** members of the service object's security descriptor.</span></span>                                                                                                                                                                                                                                                   |



 

<span data-ttu-id="926e9-214">Ниже перечислены [универсальные права доступа](/windows/desktop/SecAuthZ/generic-access-rights) для службы.</span><span class="sxs-lookup"><span data-stu-id="926e9-214">The following are the [generic access rights](/windows/desktop/SecAuthZ/generic-access-rights) for a service.</span></span>



<table>
<thead>
<tr class="header">
<th><span data-ttu-id="926e9-215">Право доступа</span><span class="sxs-lookup"><span data-stu-id="926e9-215">Access right</span></span></th>
<th><span data-ttu-id="926e9-216">Описание</span><span class="sxs-lookup"><span data-stu-id="926e9-216">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="926e9-217"><strong>GENERIC_READ</strong></span><span class="sxs-lookup"><span data-stu-id="926e9-217"><strong>GENERIC_READ</strong></span></span></td>
<td><dl> <span data-ttu-id="926e9-218"><strong>STANDARD_RIGHTS_READ</strong></span><span class="sxs-lookup"><span data-stu-id="926e9-218"><strong>STANDARD_RIGHTS_READ</strong></span></span><br /><span data-ttu-id="926e9-219">
<strong>SERVICE_QUERY_CONFIG</strong></span><span class="sxs-lookup"><span data-stu-id="926e9-219">
<strong>SERVICE_QUERY_CONFIG</strong></span></span><br /><span data-ttu-id="926e9-220">
<strong>SERVICE_QUERY_STATUS</strong></span><span class="sxs-lookup"><span data-stu-id="926e9-220">
<strong>SERVICE_QUERY_STATUS</strong></span></span><br /><span data-ttu-id="926e9-221">
<strong>SERVICE_INTERROGATE</strong></span><span class="sxs-lookup"><span data-stu-id="926e9-221">
<strong>SERVICE_INTERROGATE</strong></span></span><br /><span data-ttu-id="926e9-222">
<strong>SERVICE_ENUMERATE_DEPENDENTS</strong></span><span class="sxs-lookup"><span data-stu-id="926e9-222">
<strong>SERVICE_ENUMERATE_DEPENDENTS</strong></span></span><br />
</dl></td>
</tr>
<tr class="even">
<td><span data-ttu-id="926e9-223"><strong>GENERIC_WRITE</strong></span><span class="sxs-lookup"><span data-stu-id="926e9-223"><strong>GENERIC_WRITE</strong></span></span></td>
<td><dl> <span data-ttu-id="926e9-224"><strong>STANDARD_RIGHTS_WRITE</strong></span><span class="sxs-lookup"><span data-stu-id="926e9-224"><strong>STANDARD_RIGHTS_WRITE</strong></span></span><br /><span data-ttu-id="926e9-225">
<strong>SERVICE_CHANGE_CONFIG</strong></span><span class="sxs-lookup"><span data-stu-id="926e9-225">
<strong>SERVICE_CHANGE_CONFIG</strong></span></span><br />
</dl></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="926e9-226"><strong>GENERIC_EXECUTE</strong></span><span class="sxs-lookup"><span data-stu-id="926e9-226"><strong>GENERIC_EXECUTE</strong></span></span></td>
<td><dl> <span data-ttu-id="926e9-227"><strong>STANDARD_RIGHTS_EXECUTE</strong></span><span class="sxs-lookup"><span data-stu-id="926e9-227"><strong>STANDARD_RIGHTS_EXECUTE</strong></span></span><br /><span data-ttu-id="926e9-228">
<strong>SERVICE_START</strong></span><span class="sxs-lookup"><span data-stu-id="926e9-228">
<strong>SERVICE_START</strong></span></span><br /><span data-ttu-id="926e9-229">
<strong>SERVICE_STOP</strong></span><span class="sxs-lookup"><span data-stu-id="926e9-229">
<strong>SERVICE_STOP</strong></span></span><br /><span data-ttu-id="926e9-230">
<strong>SERVICE_PAUSE_CONTINUE</strong></span><span class="sxs-lookup"><span data-stu-id="926e9-230">
<strong>SERVICE_PAUSE_CONTINUE</strong></span></span><br /><span data-ttu-id="926e9-231">
<strong>SERVICE_USER_DEFINED_CONTROL</strong></span><span class="sxs-lookup"><span data-stu-id="926e9-231">
<strong>SERVICE_USER_DEFINED_CONTROL</strong></span></span><br />
</dl></td>
</tr>
</tbody>
</table>



 

<span data-ttu-id="926e9-232">SCM создает дескриптор безопасности объекта службы, когда служба устанавливается с помощью функции [**CreateService**](/windows/desktop/api/Winsvc/nf-winsvc-createservicea) .</span><span class="sxs-lookup"><span data-stu-id="926e9-232">The SCM creates a service object's security descriptor when the service is installed by the [**CreateService**](/windows/desktop/api/Winsvc/nf-winsvc-createservicea) function.</span></span> <span data-ttu-id="926e9-233">Дескриптор безопасности по умолчанию объекта службы предоставляет следующий доступ.</span><span class="sxs-lookup"><span data-stu-id="926e9-233">The default security descriptor of a service object grants the following access.</span></span>



<table>
<thead>
<tr class="header">
<th><span data-ttu-id="926e9-234">Учетная запись</span><span class="sxs-lookup"><span data-stu-id="926e9-234">Account</span></span></th>
<th><span data-ttu-id="926e9-235">Права доступа</span><span class="sxs-lookup"><span data-stu-id="926e9-235">Access rights</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="926e9-236">Удаленные пользователи, прошедшие проверку подлинности</span><span class="sxs-lookup"><span data-stu-id="926e9-236">Remote authenticated users</span></span></td>
<td><span data-ttu-id="926e9-237">По умолчанию не предоставлено. <strong>Windows Server 2003 с пакетом обновления 1 (SP1): SERVICE_USER_DEFINED_CONTROL</strong></span><span class="sxs-lookup"><span data-stu-id="926e9-237">Not granted by default.<strong>Windows Server 2003 with SP1:  SERVICE_USER_DEFINED_CONTROL</strong></span></span><br/> <span data-ttu-id="926e9-238"><strong>Windows Server 2003 и Windows XP:</strong> Права доступа для удаленных пользователей, прошедших проверку подлинности, совпадают с правами локальных пользователей, прошедших проверку подлинности.</span><span class="sxs-lookup"><span data-stu-id="926e9-238"><strong>Windows Server 2003 and Windows XP:</strong> The access rights for remote authenticated users are the same as for local authenticated users.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="926e9-239">Локальные пользователи, прошедшие проверку подлинности (включая LocalService и NetworkService);</span><span class="sxs-lookup"><span data-stu-id="926e9-239">Local authenticated users (including LocalService and NetworkService)</span></span></td>
<td><dl> <span data-ttu-id="926e9-240"><strong>READ_CONTROL</strong></span><span class="sxs-lookup"><span data-stu-id="926e9-240"><strong>READ_CONTROL</strong></span></span><br /><span data-ttu-id="926e9-241">
<strong>SERVICE_ENUMERATE_DEPENDENTS</strong></span><span class="sxs-lookup"><span data-stu-id="926e9-241">
<strong>SERVICE_ENUMERATE_DEPENDENTS</strong></span></span><br /><span data-ttu-id="926e9-242">
<strong>SERVICE_INTERROGATE</strong></span><span class="sxs-lookup"><span data-stu-id="926e9-242">
<strong>SERVICE_INTERROGATE</strong></span></span><br /><span data-ttu-id="926e9-243">
<strong>SERVICE_QUERY_CONFIG</strong></span><span class="sxs-lookup"><span data-stu-id="926e9-243">
<strong>SERVICE_QUERY_CONFIG</strong></span></span><br /><span data-ttu-id="926e9-244">
<strong>SERVICE_QUERY_STATUS</strong></span><span class="sxs-lookup"><span data-stu-id="926e9-244">
<strong>SERVICE_QUERY_STATUS</strong></span></span><br /><span data-ttu-id="926e9-245">
<strong>SERVICE_USER_DEFINED_CONTROL</strong></span><span class="sxs-lookup"><span data-stu-id="926e9-245">
<strong>SERVICE_USER_DEFINED_CONTROL</strong></span></span><br />
</dl></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="926e9-246">локальная система;</span><span class="sxs-lookup"><span data-stu-id="926e9-246">LocalSystem</span></span></td>
<td><dl> <span data-ttu-id="926e9-247"><strong>READ_CONTROL</strong></span><span class="sxs-lookup"><span data-stu-id="926e9-247"><strong>READ_CONTROL</strong></span></span><br /><span data-ttu-id="926e9-248">
<strong>SERVICE_ENUMERATE_DEPENDENTS</strong></span><span class="sxs-lookup"><span data-stu-id="926e9-248">
<strong>SERVICE_ENUMERATE_DEPENDENTS</strong></span></span><br /><span data-ttu-id="926e9-249">
<strong>SERVICE_INTERROGATE</strong></span><span class="sxs-lookup"><span data-stu-id="926e9-249">
<strong>SERVICE_INTERROGATE</strong></span></span><br /><span data-ttu-id="926e9-250">
<strong>SERVICE_PAUSE_CONTINUE</strong></span><span class="sxs-lookup"><span data-stu-id="926e9-250">
<strong>SERVICE_PAUSE_CONTINUE</strong></span></span><br /><span data-ttu-id="926e9-251">
<strong>SERVICE_QUERY_CONFIG</strong></span><span class="sxs-lookup"><span data-stu-id="926e9-251">
<strong>SERVICE_QUERY_CONFIG</strong></span></span><br /><span data-ttu-id="926e9-252">
<strong>SERVICE_QUERY_STATUS</strong></span><span class="sxs-lookup"><span data-stu-id="926e9-252">
<strong>SERVICE_QUERY_STATUS</strong></span></span><br /><span data-ttu-id="926e9-253">
<strong>SERVICE_START</strong></span><span class="sxs-lookup"><span data-stu-id="926e9-253">
<strong>SERVICE_START</strong></span></span><br /><span data-ttu-id="926e9-254">
<strong>SERVICE_STOP</strong></span><span class="sxs-lookup"><span data-stu-id="926e9-254">
<strong>SERVICE_STOP</strong></span></span><br /><span data-ttu-id="926e9-255">
<strong>SERVICE_USER_DEFINED_CONTROL</strong></span><span class="sxs-lookup"><span data-stu-id="926e9-255">
<strong>SERVICE_USER_DEFINED_CONTROL</strong></span></span><br />
</dl></td>
</tr>
<tr class="even">
<td><span data-ttu-id="926e9-256">Администраторы</span><span class="sxs-lookup"><span data-stu-id="926e9-256">Administrators</span></span></td>
<td><dl> <span data-ttu-id="926e9-257"><strong>DELETE</strong></span><span class="sxs-lookup"><span data-stu-id="926e9-257"><strong>DELETE</strong></span></span><br /><span data-ttu-id="926e9-258">
<strong>READ_CONTROL</strong></span><span class="sxs-lookup"><span data-stu-id="926e9-258">
<strong>READ_CONTROL</strong></span></span><br /><span data-ttu-id="926e9-259">
<strong>SERVICE_ALL_ACCESS</strong></span><span class="sxs-lookup"><span data-stu-id="926e9-259">
<strong>SERVICE_ALL_ACCESS</strong></span></span><br /><span data-ttu-id="926e9-260">
<strong>WRITE_DAC</strong></span><span class="sxs-lookup"><span data-stu-id="926e9-260">
<strong>WRITE_DAC</strong></span></span><br /><span data-ttu-id="926e9-261">
<strong>WRITE_OWNER</strong></span><span class="sxs-lookup"><span data-stu-id="926e9-261">
<strong>WRITE_OWNER</strong></span></span><br />
</dl></td>
</tr>
</tbody>
</table>



 

<span data-ttu-id="926e9-262">Для выполнения любых операций пользователь должен войти в систему в интерактивном режиме, или служба должна использовать одну из учетных записей служб.</span><span class="sxs-lookup"><span data-stu-id="926e9-262">To perform any operations, the user must be logged on interactively or the service must use one of the service accounts.</span></span>

<span data-ttu-id="926e9-263">Чтобы получить или задать дескриптор безопасности для объекта службы, используйте функции [**куерисервицеобжектсекурити**](/windows/desktop/api/winsvc/nf-winsvc-queryserviceobjectsecurity) и [**сетсервицеобжектсекурити**](/windows/desktop/api/winsvc/nf-winsvc-setserviceobjectsecurity) .</span><span class="sxs-lookup"><span data-stu-id="926e9-263">To get or set the security descriptor for a service object, use the [**QueryServiceObjectSecurity**](/windows/desktop/api/winsvc/nf-winsvc-queryserviceobjectsecurity) and [**SetServiceObjectSecurity**](/windows/desktop/api/winsvc/nf-winsvc-setserviceobjectsecurity) functions.</span></span> <span data-ttu-id="926e9-264">Дополнительные сведения см. [в разделе изменение списка DACL для службы](modifying-the-dacl-for-a-service.md).</span><span class="sxs-lookup"><span data-stu-id="926e9-264">For more information, see [Modifying the DACL for a Service](modifying-the-dacl-for-a-service.md).</span></span>

<span data-ttu-id="926e9-265">Когда процесс использует функцию [**OpenService**](/windows/desktop/api/Winsvc/nf-winsvc-openservicea) , система проверяет запрошенные права доступа в отношении дескриптора безопасности для объекта службы.</span><span class="sxs-lookup"><span data-stu-id="926e9-265">When a process uses the [**OpenService**](/windows/desktop/api/Winsvc/nf-winsvc-openservicea) function, the system checks the requested access rights against the security descriptor for the service object.</span></span>

<span data-ttu-id="926e9-266">Предоставление определенных прав доступа недоверенным пользователям (например, настройке **\_ изменения службы \_** или **ее \_ остановкой**) может привести к конфликту с выполнением службы и, возможно, позволит им запускать приложения под учетной записью LocalSystem.</span><span class="sxs-lookup"><span data-stu-id="926e9-266">Granting certain access rights to untrusted users (such as **SERVICE\_CHANGE\_CONFIG** or **SERVICE\_STOP**) can allow them to interfere with the execution of your service, and possibly allow them to run applications under the LocalSystem account.</span></span>

<span data-ttu-id="926e9-267">Когда вызывается [**функция енумсервицесстатусекс**](/windows/desktop/api/Winsvc/nf-winsvc-enumservicesstatusexa) , если у вызывающего объекта нет права доступа к **\_ \_ состоянию запроса** на обслуживание службы, служба автоматически опускается из списка служб, возвращаемых клиенту.</span><span class="sxs-lookup"><span data-stu-id="926e9-267">When [**EnumServicesStatusEx function**](/windows/desktop/api/Winsvc/nf-winsvc-enumservicesstatusexa) is called, if the caller does not have the **SERVICE\_QUERY\_STATUS** access right to a service, the service is silently omitted from the list of services returned to the client.</span></span>

 

