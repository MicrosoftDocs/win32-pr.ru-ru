---
description: Управляет репликацией для виртуальной машины.
ms.assetid: 0335fb94-5f2b-43be-bfb4-bc6811c5b507
title: Класс Msvm_ReplicationService
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_ReplicationService
- Msvm_ReplicationService.InstanceID
- Msvm_ReplicationService.Caption
- Msvm_ReplicationService.Description
- Msvm_ReplicationService.ElementName
- Msvm_ReplicationService.InstallDate
- Msvm_ReplicationService.Name
- Msvm_ReplicationService.OperationalStatus
- Msvm_ReplicationService.StatusDescriptions
- Msvm_ReplicationService.Status
- Msvm_ReplicationService.HealthState
- Msvm_ReplicationService.CommunicationStatus
- Msvm_ReplicationService.DetailedStatus
- Msvm_ReplicationService.OperatingStatus
- Msvm_ReplicationService.PrimaryStatus
- Msvm_ReplicationService.EnabledState
- Msvm_ReplicationService.OtherEnabledState
- Msvm_ReplicationService.RequestedState
- Msvm_ReplicationService.EnabledDefault
- Msvm_ReplicationService.TimeOfLastStateChange
- Msvm_ReplicationService.AvailableRequestedStates
- Msvm_ReplicationService.TransitioningToState
- Msvm_ReplicationService.SystemCreationClassName
- Msvm_ReplicationService.SystemName
- Msvm_ReplicationService.CreationClassName
- Msvm_ReplicationService.PrimaryOwnerName
- Msvm_ReplicationService.PrimaryOwnerContact
- Msvm_ReplicationService.StartMode
- Msvm_ReplicationService.Started
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: 86e9140e2fe9b047c57c762be2e0fba048511993
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "104265056"
---
# <a name="msvm_replicationservice-class"></a><span data-ttu-id="c0d1e-103">\_Класс мсвм репликатионсервице</span><span class="sxs-lookup"><span data-stu-id="c0d1e-103">Msvm\_ReplicationService class</span></span>

<span data-ttu-id="c0d1e-104">Управляет репликацией для виртуальной машины.</span><span class="sxs-lookup"><span data-stu-id="c0d1e-104">Manages the replication for a virtual machine.</span></span>

<span data-ttu-id="c0d1e-105">Следующий синтаксис является упрощенным MOF-файлным (MOF) кодом и включает все наследуемые свойства.</span><span class="sxs-lookup"><span data-stu-id="c0d1e-105">The following syntax is simplified Managed Object Format (MOF) code, and it includes all of the inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="c0d1e-106">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="c0d1e-106">Syntax</span></span>

``` syntax
[Dynamic, Provider("VmmsWmiInstanceAndMethodProvider"), AMENDMENT]
class Msvm_ReplicationService : CIM_Service
{
  string   InstanceID;
  string   Caption = "Hyper-V Replica Service";
  string   Description = "Replication Service";
  string   ElementName;
  datetime InstallDate;
  string   Name = "replicasvc";
  uint16   OperationalStatus[];
  string   StatusDescriptions[];
  string   Status = "OK";
  uint16   HealthState = 5;
  uint16   CommunicationStatus;
  uint16   DetailedStatus;
  uint16   OperatingStatus;
  uint16   PrimaryStatus;
  uint16   EnabledState = 2;
  string   OtherEnabledState;
  uint16   RequestedState = 12;
  uint16   EnabledDefault = 2;
  datetime TimeOfLastStateChange;
  uint16   AvailableRequestedStates[];
  uint16   TransitioningToState;
  string   SystemCreationClassName = "Msvm_ComputerSystem";
  string   SystemName;
  string   CreationClassName = "Msvm_ReplicationService";
  string   PrimaryOwnerName;
  string   PrimaryOwnerContact;
  string   StartMode;
  boolean  Started = True;
};
```

## <a name="members"></a><span data-ttu-id="c0d1e-107">Члены</span><span class="sxs-lookup"><span data-stu-id="c0d1e-107">Members</span></span>

<span data-ttu-id="c0d1e-108">Класс **мсвм \_ репликатионсервице** имеет следующие типы членов:</span><span class="sxs-lookup"><span data-stu-id="c0d1e-108">The **Msvm\_ReplicationService** class has these types of members:</span></span>

-   [<span data-ttu-id="c0d1e-109">Методы</span><span class="sxs-lookup"><span data-stu-id="c0d1e-109">Methods</span></span>](#methods)
-   [<span data-ttu-id="c0d1e-110">Свойства</span><span class="sxs-lookup"><span data-stu-id="c0d1e-110">Properties</span></span>](#properties)

### <a name="methods"></a><span data-ttu-id="c0d1e-111">Методы</span><span class="sxs-lookup"><span data-stu-id="c0d1e-111">Methods</span></span>

<span data-ttu-id="c0d1e-112">Класс **мсвм \_ репликатионсервице** содержит следующие методы.</span><span class="sxs-lookup"><span data-stu-id="c0d1e-112">The **Msvm\_ReplicationService** class has these methods.</span></span>



| <span data-ttu-id="c0d1e-113">Метод</span><span class="sxs-lookup"><span data-stu-id="c0d1e-113">Method</span></span>                                                                                                 | <span data-ttu-id="c0d1e-114">Описание</span><span class="sxs-lookup"><span data-stu-id="c0d1e-114">Description</span></span>                                                                                                                                                                                                                                                                                   |
|:-------------------------------------------------------------------------------------------------------|:----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="c0d1e-115">**аддаусоризатионентри**</span><span class="sxs-lookup"><span data-stu-id="c0d1e-115">**AddAuthorizationEntry**</span></span>](addauthorizationentry-msvm-replicationservice.md)                         | <span data-ttu-id="c0d1e-116">Добавляет запись авторизации на сервер.</span><span class="sxs-lookup"><span data-stu-id="c0d1e-116">Adds an authorization entry to a server.</span></span><br/>                                                                                                                                                                                                                                           |
| [<span data-ttu-id="c0d1e-117">**чанжерепликатионмодетопримари**</span><span class="sxs-lookup"><span data-stu-id="c0d1e-117">**ChangeReplicationModeToPrimary**</span></span>](changereplicationmodetoprimary-msvm-replicationservice.md)       | <span data-ttu-id="c0d1e-118">Изменяет отношение расширенной репликации на основное отношение для реплики виртуальной машины.</span><span class="sxs-lookup"><span data-stu-id="c0d1e-118">Changes the extended replication relationship to the primary relationship for a replica virtual machine.</span></span> <span data-ttu-id="c0d1e-119">Виртуальная машина реплики должна находиться в состоянии фиксации отработки отказа.</span><span class="sxs-lookup"><span data-stu-id="c0d1e-119">The replica virtual machine must be in a failover committed state.</span></span><br/> <span data-ttu-id="c0d1e-120">**Windows 8.1:** Этот метод не поддерживается до Windows 8.1 и Windows Server 2012 R2.</span><span class="sxs-lookup"><span data-stu-id="c0d1e-120">**Windows 8.1:** This method is not supported until Windows 8.1 and Windows Server 2012 R2.</span></span><br/> |
| [<span data-ttu-id="c0d1e-121">**коммитфаиловер**</span><span class="sxs-lookup"><span data-stu-id="c0d1e-121">**CommitFailover**</span></span>](commitfailover-msvm-replicationservice.md)                                       | <span data-ttu-id="c0d1e-122">Фиксирует моментальный снимок восстановления, который метод [**инитиатефаиловер**](initiatefailover-msvm-replicationservice.md) использовал для отработки отказа.</span><span class="sxs-lookup"><span data-stu-id="c0d1e-122">Commits the recovery snapshot that the [**InitiateFailover**](initiatefailover-msvm-replicationservice.md) method has used for a failover.</span></span><br/>                                                                                                                                        |
| [<span data-ttu-id="c0d1e-123">**CreateReplicationRelationship**</span><span class="sxs-lookup"><span data-stu-id="c0d1e-123">**CreateReplicationRelationship**</span></span>](createreplicationrelationship-msvm-replicationservice.md)         | <span data-ttu-id="c0d1e-124">Создает новое отношение репликации для виртуальной машины.</span><span class="sxs-lookup"><span data-stu-id="c0d1e-124">Creates a new replication relationship for a virtual machine.</span></span><br/>                                                                                                                                                                                                                      |
| [<span data-ttu-id="c0d1e-125">**жетрепликатионстатистикс**</span><span class="sxs-lookup"><span data-stu-id="c0d1e-125">**GetReplicationStatistics**</span></span>](getreplicationstatistics-msvm-replicationservice.md)                   | <span data-ttu-id="c0d1e-126">Извлекает статистику репликации для виртуальной машины.</span><span class="sxs-lookup"><span data-stu-id="c0d1e-126">Retrieves replication statistics for a virtual machine.</span></span><br/>                                                                                                                                                                                                                            |
| [<span data-ttu-id="c0d1e-127">**жетрепликатионстатистиксекс**</span><span class="sxs-lookup"><span data-stu-id="c0d1e-127">**GetReplicationStatisticsEx**</span></span>](getreplicationstatisticsex-msvm-replicationservice.md)               | <span data-ttu-id="c0d1e-128">Извлекает статистику репликации, связанную с указанным отношением репликации виртуальной машины.</span><span class="sxs-lookup"><span data-stu-id="c0d1e-128">Retrieves the replication statistics that are associated with specified replication relationship of the virtual machine.</span></span><br/> <span data-ttu-id="c0d1e-129">**Windows 8.1:** Этот метод не поддерживается до Windows 8.1 и Windows Server 2012 R2.</span><span class="sxs-lookup"><span data-stu-id="c0d1e-129">**Windows 8.1:** This method is not supported until Windows 8.1 and Windows Server 2012 R2.</span></span><br/>                                                    |
| [<span data-ttu-id="c0d1e-130">**жетсистемцертификатес**</span><span class="sxs-lookup"><span data-stu-id="c0d1e-130">**GetSystemCertificates**</span></span>](getsystemcertificates-msvm-replicationservice.md)                         | <span data-ttu-id="c0d1e-131">Получает системные сертификаты в системе узла.</span><span class="sxs-lookup"><span data-stu-id="c0d1e-131">Retrieves the system certificates on a host system.</span></span><br/>                                                                                                                                                                                                                                |
| [<span data-ttu-id="c0d1e-132">**импортинитиалреплика**</span><span class="sxs-lookup"><span data-stu-id="c0d1e-132">**ImportInitialReplica**</span></span>](importinitialreplica-msvm-replicationservice.md)                           | <span data-ttu-id="c0d1e-133">Импортирует начальную репликацию для виртуальной машины.</span><span class="sxs-lookup"><span data-stu-id="c0d1e-133">Imports the initial replication for a virtual machine.</span></span><br/>                                                                                                                                                                                                                             |
| [<span data-ttu-id="c0d1e-134">**инитиатефаилбакк**</span><span class="sxs-lookup"><span data-stu-id="c0d1e-134">**InitiateFailback**</span></span>](initiatefailback-msvm-replicationservice.md)                                   | <span data-ttu-id="c0d1e-135">Инициирует восстановление размещения для виртуальной машины восстановления.</span><span class="sxs-lookup"><span data-stu-id="c0d1e-135">Initiates the failback for a recovery virtual machine.</span></span> <span data-ttu-id="c0d1e-136">Это значит, что задает для виртуальной машины отработку отказа с помощью образа приложения или сбоя.</span><span class="sxs-lookup"><span data-stu-id="c0d1e-136">That is, sets the failover for the virtual machine to an app or crash consistent image.</span></span><br/> <span data-ttu-id="c0d1e-137">**Windows 8.1:** Этот метод не поддерживается до Windows 8.1 и Windows Server 2012 R2.</span><span class="sxs-lookup"><span data-stu-id="c0d1e-137">**Windows 8.1:** This method is not supported until Windows 8.1 and Windows Server 2012 R2.</span></span><br/>                              |
| [<span data-ttu-id="c0d1e-138">**инитиатефаиловер**</span><span class="sxs-lookup"><span data-stu-id="c0d1e-138">**InitiateFailover**</span></span>](initiatefailover-msvm-replicationservice.md)                                   | <span data-ttu-id="c0d1e-139">Инициирует отработку отказа для виртуальной машины в приложение или образ точки репликации уровня "Стандартный".</span><span class="sxs-lookup"><span data-stu-id="c0d1e-139">Initiates a failover for a virtual machine to an application or standard replication point image.</span></span><br/>                                                                                                                                                                                  |
| [<span data-ttu-id="c0d1e-140">**модифяусоризатионентри**</span><span class="sxs-lookup"><span data-stu-id="c0d1e-140">**ModifyAuthorizationEntry**</span></span>](modifyauthorizationentry-msvm-replicationservice.md)                   | <span data-ttu-id="c0d1e-141">Изменяет запись авторизации на сервере.</span><span class="sxs-lookup"><span data-stu-id="c0d1e-141">Modifies an authorization entry on a server.</span></span><br/>                                                                                                                                                                                                                                       |
| [<span data-ttu-id="c0d1e-142">**модифирепликатионсеттингс**</span><span class="sxs-lookup"><span data-stu-id="c0d1e-142">**ModifyReplicationSettings**</span></span>](modifyreplicationsettings-msvm-replicationservice.md)                 | <span data-ttu-id="c0d1e-143">Изменяет параметры репликации для виртуальной машины.</span><span class="sxs-lookup"><span data-stu-id="c0d1e-143">Modifies the replication settings for a virtual machine.</span></span><br/>                                                                                                                                                                                                                           |
| [<span data-ttu-id="c0d1e-144">**модифисервицесеттингс**</span><span class="sxs-lookup"><span data-stu-id="c0d1e-144">**ModifyServiceSettings**</span></span>](modifyservicesettings-msvm-replicationservice.md)                         | <span data-ttu-id="c0d1e-145">Изменяет параметры службы реплики Hyper-V.</span><span class="sxs-lookup"><span data-stu-id="c0d1e-145">Modifies the settings for the Hyper-V Replica service.</span></span><br/>                                                                                                                                                                                                                             |
| [<span data-ttu-id="c0d1e-146">**ремовеаусоризатионентри**</span><span class="sxs-lookup"><span data-stu-id="c0d1e-146">**RemoveAuthorizationEntry**</span></span>](removeauthorizationentry-msvm-replicationservice.md)                   | <span data-ttu-id="c0d1e-147">Удаляет запись авторизации с сервера.</span><span class="sxs-lookup"><span data-stu-id="c0d1e-147">Removes the authorization entry from a server.</span></span><br/>                                                                                                                                                                                                                                     |
| [<span data-ttu-id="c0d1e-148">**ремоверепликатионрелатионшип**</span><span class="sxs-lookup"><span data-stu-id="c0d1e-148">**RemoveReplicationRelationship**</span></span>](removereplicationrelationship-msvm-replicationservice.md)         | <span data-ttu-id="c0d1e-149">Удаляет отношение репликации виртуальной машины.</span><span class="sxs-lookup"><span data-stu-id="c0d1e-149">Removes a virtual machine replication relationship.</span></span><br/>                                                                                                                                                                                                                                |
| [<span data-ttu-id="c0d1e-150">**ремоверепликатионрелатионшипекс**</span><span class="sxs-lookup"><span data-stu-id="c0d1e-150">**RemoveReplicationRelationshipEx**</span></span>](removereplicationrelationshipex-msvm-replicationservice.md)     | <span data-ttu-id="c0d1e-151">Удаляет указанное отношение репликации виртуальной машины.</span><span class="sxs-lookup"><span data-stu-id="c0d1e-151">Removes the specified virtual machine replication relationship.</span></span> <span data-ttu-id="c0d1e-152">Для виртуальной машины реплики невозможно удалить первичную репликацию, если включена расширенная репликация.</span><span class="sxs-lookup"><span data-stu-id="c0d1e-152">For a replica virtual machine, primary replication can't be removed if extended replication is enabled.</span></span><br/> <span data-ttu-id="c0d1e-153">**Windows 8.1:** Этот метод не поддерживается до Windows 8.1 и Windows Server 2012 R2.</span><span class="sxs-lookup"><span data-stu-id="c0d1e-153">**Windows 8.1:** This method is not supported until Windows 8.1 and Windows Server 2012 R2.</span></span><br/>     |
| [<span data-ttu-id="c0d1e-154">**Равен**</span><span class="sxs-lookup"><span data-stu-id="c0d1e-154">**RequestStateChange**</span></span>](msvm-replicationservice-requeststatechange.md)                               | <span data-ttu-id="c0d1e-155">Запрашивает изменение состояния.</span><span class="sxs-lookup"><span data-stu-id="c0d1e-155">Requests a state change.</span></span><br/>                                                                                                                                                                                                                                                           |
| [<span data-ttu-id="c0d1e-156">**ресетрепликатионстатистикс**</span><span class="sxs-lookup"><span data-stu-id="c0d1e-156">**ResetReplicationStatistics**</span></span>](resetreplicationstatistics-msvm-replicationservice.md)               | <span data-ttu-id="c0d1e-157">Сбрасывает статистику репликации для виртуальной машины.</span><span class="sxs-lookup"><span data-stu-id="c0d1e-157">Resets the replication statistics for a virtual machine.</span></span><br/>                                                                                                                                                                                                                           |
| [<span data-ttu-id="c0d1e-158">**ресетрепликатионстатистиксекс**</span><span class="sxs-lookup"><span data-stu-id="c0d1e-158">**ResetReplicationStatisticsEx**</span></span>](resetreplicationstatisticsex-msvm-replicationservice.md)           | <span data-ttu-id="c0d1e-159">Сбрасывает статистику репликации, связанную с указанным отношением репликации виртуальной машины.</span><span class="sxs-lookup"><span data-stu-id="c0d1e-159">Resets replication statistics that are associated with the specified replication relationship of a virtual machine.</span></span><br/> <span data-ttu-id="c0d1e-160">**Windows 8.1:** Этот метод не поддерживается до Windows 8.1 и Windows Server 2012 R2.</span><span class="sxs-lookup"><span data-stu-id="c0d1e-160">**Windows 8.1:** This method is not supported until Windows 8.1 and Windows Server 2012 R2.</span></span><br/>                                                         |
| [<span data-ttu-id="c0d1e-161">**Повторная синхронизация**</span><span class="sxs-lookup"><span data-stu-id="c0d1e-161">**Resynchronize**</span></span>](resynchronize-msvm-replicationservice.md)                                         | <span data-ttu-id="c0d1e-162">Выполняет операцию повторной синхронизации на указанной виртуальной машине.</span><span class="sxs-lookup"><span data-stu-id="c0d1e-162">Performs a resynchronization operation on the specified virtual machine.</span></span><br/>                                                                                                                                                                                                           |
| [<span data-ttu-id="c0d1e-163">**реверсерепликатионрелатионшип**</span><span class="sxs-lookup"><span data-stu-id="c0d1e-163">**ReverseReplicationRelationship**</span></span>](reversereplicationrelationship-msvm-replicationservice.md)       | <span data-ttu-id="c0d1e-164">Реплицирует отработку отказа виртуальной машины обратно на сервер-источник.</span><span class="sxs-lookup"><span data-stu-id="c0d1e-164">Replicates a failed-over virtual machine back to the primary server.</span></span><br/>                                                                                                                                                                                                               |
| [<span data-ttu-id="c0d1e-165">**ревертфаиловер**</span><span class="sxs-lookup"><span data-stu-id="c0d1e-165">**RevertFailover**</span></span>](revertfailover-msvm-replicationservice.md)                                       | <span data-ttu-id="c0d1e-166">Отменяет текущую отработку отказа для виртуальной машины, удаляя текущий диск отработки отказа.</span><span class="sxs-lookup"><span data-stu-id="c0d1e-166">Reverts the current failover for a virtual machine by discarding the current failover disk.</span></span><br/>                                                                                                                                                                                        |
| [<span data-ttu-id="c0d1e-167">**сетаусоризатионентри**</span><span class="sxs-lookup"><span data-stu-id="c0d1e-167">**SetAuthorizationEntry**</span></span>](setauthorizationentry-msvm-replicationservice.md)                         | <span data-ttu-id="c0d1e-168">Задает запись авторизации репликации для виртуальной машины.</span><span class="sxs-lookup"><span data-stu-id="c0d1e-168">Sets the replication authorization entry for a virtual machine.</span></span><br/>                                                                                                                                                                                                                    |
| [<span data-ttu-id="c0d1e-169">**сетфаиловернетворкадаптерсеттингс**</span><span class="sxs-lookup"><span data-stu-id="c0d1e-169">**SetFailoverNetworkAdapterSettings**</span></span>](setfailovernetworkadaptersettings-msvm-replicationservice.md) | <span data-ttu-id="c0d1e-170">Настройка IP-параметров сетевого адаптера для применения к виртуальной машине после отработки отказа.</span><span class="sxs-lookup"><span data-stu-id="c0d1e-170">Configures the network adapter's IP settings to be applied to a virtual machine after a failover.</span></span><br/>                                                                                                                                                                                  |
| [<span data-ttu-id="c0d1e-171">**StartReplication**</span><span class="sxs-lookup"><span data-stu-id="c0d1e-171">**StartReplication**</span></span>](startreplication-msvm-replicationservice.md)                                   | <span data-ttu-id="c0d1e-172">Запускает репликацию виртуальной машины.</span><span class="sxs-lookup"><span data-stu-id="c0d1e-172">Starts the replication of a virtual machine.</span></span><br/>                                                                                                                                                                                                                                       |
| [<span data-ttu-id="c0d1e-173">**StartService**</span><span class="sxs-lookup"><span data-stu-id="c0d1e-173">**StartService**</span></span>](msvm-replicationservice-startservice.md)                                           | <span data-ttu-id="c0d1e-174">запускает службу.</span><span class="sxs-lookup"><span data-stu-id="c0d1e-174">Starts the service.</span></span><br/>                                                                                                                                                                                                                                                                |
| [<span data-ttu-id="c0d1e-175">**StopService**</span><span class="sxs-lookup"><span data-stu-id="c0d1e-175">**StopService**</span></span>](msvm-replicationservice-stopservice.md)                                             | <span data-ttu-id="c0d1e-176">останавливает службу.</span><span class="sxs-lookup"><span data-stu-id="c0d1e-176">Stops the service.</span></span><br/>                                                                                                                                                                                                                                                                 |
| [<span data-ttu-id="c0d1e-177">**тестрепликасистем**</span><span class="sxs-lookup"><span data-stu-id="c0d1e-177">**TestReplicaSystem**</span></span>](testreplicasystem-msvm-replicationservice.md)                                 | <span data-ttu-id="c0d1e-178">Создает новую реплику виртуальной машины с указанным моментальным снимком для целей тестирования.</span><span class="sxs-lookup"><span data-stu-id="c0d1e-178">Creates a new replica of a virtual machine with the specified snapshot for testing purposes.</span></span><br/>                                                                                                                                                                                       |
| [<span data-ttu-id="c0d1e-179">**тестрепликатионконнектион**</span><span class="sxs-lookup"><span data-stu-id="c0d1e-179">**TestReplicationConnection**</span></span>](testreplicationconnection-msvm-replicationservice.md)                 | <span data-ttu-id="c0d1e-180">Проверяет, можно ли включить репликацию из текущей системы узла в указанную систему восстановления.</span><span class="sxs-lookup"><span data-stu-id="c0d1e-180">Verifies if the replication can be enabled from the current host system to the specified recovery system.</span></span><br/>                                                                                                                                                                          |



 

### <a name="properties"></a><span data-ttu-id="c0d1e-181">Свойства</span><span class="sxs-lookup"><span data-stu-id="c0d1e-181">Properties</span></span>

<span data-ttu-id="c0d1e-182">Класс **мсвм \_ репликатионсервице** имеет следующие свойства.</span><span class="sxs-lookup"><span data-stu-id="c0d1e-182">The **Msvm\_ReplicationService** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="c0d1e-183">**аваилаблерекуестедстатес**</span><span class="sxs-lookup"><span data-stu-id="c0d1e-183">**AvailableRequestedStates**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c0d1e-184">Тип данных: **UInt16** , массив</span><span class="sxs-lookup"><span data-stu-id="c0d1e-184">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="c0d1e-185">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="c0d1e-185">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="c0d1e-186">Указывает возможные значения для параметра *RequestedState* .</span><span class="sxs-lookup"><span data-stu-id="c0d1e-186">Indicates the possible values for the *RequestedState* parameter.</span></span> <span data-ttu-id="c0d1e-187">Это свойство наследуется от [**CIM \_ енабледлогикалелемент**](/previous-versions//cc136818(v=vs.85))и всегда имеет значение **null**.</span><span class="sxs-lookup"><span data-stu-id="c0d1e-187">This property is inherited from [**CIM\_EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)), and it is always set to **Null**.</span></span>

</dd> <dt>

<span data-ttu-id="c0d1e-188">**Заголовок**</span><span class="sxs-lookup"><span data-stu-id="c0d1e-188">**Caption**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c0d1e-189">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="c0d1e-189">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="c0d1e-190">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="c0d1e-190">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="c0d1e-191">Краткое описание объекта.</span><span class="sxs-lookup"><span data-stu-id="c0d1e-191">A short description of the object.</span></span> <span data-ttu-id="c0d1e-192">Это свойство наследуется от [**CIM \_ манажеделемент**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement)и всегда имеет значение "служба реплики Hyper-V".</span><span class="sxs-lookup"><span data-stu-id="c0d1e-192">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement), and it is always set to "Hyper-V Replica Service".</span></span>

</dd> <dt>

<span data-ttu-id="c0d1e-193">**коммуникатионстатус**</span><span class="sxs-lookup"><span data-stu-id="c0d1e-193">**CommunicationStatus**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c0d1e-194">Тип данных: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="c0d1e-194">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="c0d1e-195">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="c0d1e-195">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="c0d1e-196">Указывает способность инструментирования взаимодействовать с базовым управляемым элементом.</span><span class="sxs-lookup"><span data-stu-id="c0d1e-196">Indicates the ability of the instrumentation to communicate with the underlying managed element.</span></span> <span data-ttu-id="c0d1e-197">Значение **null** указывает, что это свойство не реализовано.</span><span class="sxs-lookup"><span data-stu-id="c0d1e-197">A **Null** value indicates that this property is not implemented.</span></span> <span data-ttu-id="c0d1e-198">Это свойство наследуется от [**CIM \_ манажедсистемелемент**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span><span class="sxs-lookup"><span data-stu-id="c0d1e-198">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

<dl> <dt>

<span data-ttu-id="c0d1e-199"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Неизвестно** (0)</span><span class="sxs-lookup"><span data-stu-id="c0d1e-199"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (0)</span></span>
</dt> <dt>

<span data-ttu-id="c0d1e-200"><span id="Not_Available"></span><span id="not_available"></span><span id="NOT_AVAILABLE"></span>**Недоступно** (1)</span><span class="sxs-lookup"><span data-stu-id="c0d1e-200"><span id="Not_Available"></span><span id="not_available"></span><span id="NOT_AVAILABLE"></span>**Not Available** (1)</span></span>
</dt> <dt>

<span data-ttu-id="c0d1e-201"><span id="Communication_OK"></span><span id="communication_ok"></span><span id="COMMUNICATION_OK"></span>**Связь хорошо** (2)</span><span class="sxs-lookup"><span data-stu-id="c0d1e-201"><span id="Communication_OK"></span><span id="communication_ok"></span><span id="COMMUNICATION_OK"></span>**Communication OK** (2)</span></span>
</dt> <dt>

<span data-ttu-id="c0d1e-202"><span id="Lost_Communication"></span><span id="lost_communication"></span><span id="LOST_COMMUNICATION"></span>**Потеря связи** (3)</span><span class="sxs-lookup"><span data-stu-id="c0d1e-202"><span id="Lost_Communication"></span><span id="lost_communication"></span><span id="LOST_COMMUNICATION"></span>**Lost Communication** (3)</span></span>
</dt> <dt>

<span data-ttu-id="c0d1e-203"><span id="No_Contact"></span><span id="no_contact"></span><span id="NO_CONTACT"></span>**Нет контакта** (4)</span><span class="sxs-lookup"><span data-stu-id="c0d1e-203"><span id="No_Contact"></span><span id="no_contact"></span><span id="NO_CONTACT"></span>**No Contact** (4)</span></span>
</dt> <dt>

<span data-ttu-id="c0d1e-204"><span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**Зарезервировано DMTF** (..)</span><span class="sxs-lookup"><span data-stu-id="c0d1e-204"><span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF Reserved** (..)</span></span>
</dt> <dt>

<span data-ttu-id="c0d1e-205"><span id="Vendor_Reserved_"></span><span id="vendor_reserved_"></span><span id="VENDOR_RESERVED_"></span>**Поставщик зарезервирован** (0x8000..</span><span class="sxs-lookup"><span data-stu-id="c0d1e-205"><span id="Vendor_Reserved_"></span><span id="vendor_reserved_"></span><span id="VENDOR_RESERVED_"></span>**Vendor Reserved** (0x8000..</span></span> <span data-ttu-id="c0d1e-206">)</span><span class="sxs-lookup"><span data-stu-id="c0d1e-206">)</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="c0d1e-207">**CreationClassName**</span><span class="sxs-lookup"><span data-stu-id="c0d1e-207">**CreationClassName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c0d1e-208">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="c0d1e-208">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="c0d1e-209">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="c0d1e-209">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="c0d1e-210">Квалификаторы: **Key**, **maxlen** (256)</span><span class="sxs-lookup"><span data-stu-id="c0d1e-210">Qualifiers: **Key**, **MaxLen** ( 256 )</span></span>
</dt> </dl>

<span data-ttu-id="c0d1e-211">Имя класса или подкласса, используемого при создании экземпляра.</span><span class="sxs-lookup"><span data-stu-id="c0d1e-211">The name of the class or subclass used in the creation of an instance.</span></span> <span data-ttu-id="c0d1e-212">Это свойство наследуется [**от \_ службы CIM**](/windows/desktop/CIMWin32Prov/cim-service)и всегда имеет значение "мсвм \_ репликатионсервице".</span><span class="sxs-lookup"><span data-stu-id="c0d1e-212">This property is inherited from [**CIM\_Service**](/windows/desktop/CIMWin32Prov/cim-service), and it is always set to "Msvm\_ReplicationService".</span></span>

</dd> <dt>

<span data-ttu-id="c0d1e-213">**Описание**</span><span class="sxs-lookup"><span data-stu-id="c0d1e-213">**Description**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c0d1e-214">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="c0d1e-214">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="c0d1e-215">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="c0d1e-215">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="c0d1e-216">Описание объекта.</span><span class="sxs-lookup"><span data-stu-id="c0d1e-216">A description of the object.</span></span> <span data-ttu-id="c0d1e-217">Это свойство наследуется от [**CIM \_ манажеделемент**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement)и всегда имеет значение "Служба репликации".</span><span class="sxs-lookup"><span data-stu-id="c0d1e-217">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement), and it is always set to "Replication Service".</span></span>

</dd> <dt>

<span data-ttu-id="c0d1e-218">**DetailedStatus**</span><span class="sxs-lookup"><span data-stu-id="c0d1e-218">**DetailedStatus**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c0d1e-219">Тип данных: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="c0d1e-219">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="c0d1e-220">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="c0d1e-220">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="c0d1e-221">Дополняет свойство **примаристатус** дополнительными сведениями о состоянии.</span><span class="sxs-lookup"><span data-stu-id="c0d1e-221">Compliments the **PrimaryStatus** property with additional status detail.</span></span> <span data-ttu-id="c0d1e-222">Значение **null** указывает, что это свойство не реализовано.</span><span class="sxs-lookup"><span data-stu-id="c0d1e-222">A **Null** value indicates that this property is not implemented.</span></span> <span data-ttu-id="c0d1e-223">Это свойство наследуется от [**CIM \_ манажедсистемелемент**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span><span class="sxs-lookup"><span data-stu-id="c0d1e-223">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

<dl> <dt>

<span data-ttu-id="c0d1e-224"><span id="Not_Available"></span><span id="not_available"></span><span id="NOT_AVAILABLE"></span>**Недоступно** (0)</span><span class="sxs-lookup"><span data-stu-id="c0d1e-224"><span id="Not_Available"></span><span id="not_available"></span><span id="NOT_AVAILABLE"></span>**Not Available** (0)</span></span>
</dt> <dt>

<span data-ttu-id="c0d1e-225"><span id="No_Additional_Information"></span><span id="no_additional_information"></span><span id="NO_ADDITIONAL_INFORMATION"></span>**Нет дополнительных сведений** (1)</span><span class="sxs-lookup"><span data-stu-id="c0d1e-225"><span id="No_Additional_Information"></span><span id="no_additional_information"></span><span id="NO_ADDITIONAL_INFORMATION"></span>**No Additional Information** (1)</span></span>
</dt> <dt>

<span data-ttu-id="c0d1e-226"><span id="Stressed"></span><span id="stressed"></span><span id="STRESSED"></span>**Пренапряжении** (2)</span><span class="sxs-lookup"><span data-stu-id="c0d1e-226"><span id="Stressed"></span><span id="stressed"></span><span id="STRESSED"></span>**Stressed** (2)</span></span>
</dt> <dt>

<span data-ttu-id="c0d1e-227"><span id="Predictive_Failure"></span><span id="predictive_failure"></span><span id="PREDICTIVE_FAILURE"></span>**Прогнозируемый сбой** (3)</span><span class="sxs-lookup"><span data-stu-id="c0d1e-227"><span id="Predictive_Failure"></span><span id="predictive_failure"></span><span id="PREDICTIVE_FAILURE"></span>**Predictive Failure** (3)</span></span>
</dt> <dt>

<span data-ttu-id="c0d1e-228"><span id="Non-Recoverable_Error"></span><span id="non-recoverable_error"></span><span id="NON-RECOVERABLE_ERROR"></span>**Неустранимая ошибка** (4)</span><span class="sxs-lookup"><span data-stu-id="c0d1e-228"><span id="Non-Recoverable_Error"></span><span id="non-recoverable_error"></span><span id="NON-RECOVERABLE_ERROR"></span>**Non-Recoverable Error** (4)</span></span>
</dt> <dt>

<span data-ttu-id="c0d1e-229"><span id="Supporting_Entity_in_Error"></span><span id="supporting_entity_in_error"></span><span id="SUPPORTING_ENTITY_IN_ERROR"></span>**Ошибка вспомогательной сущности** (5)</span><span class="sxs-lookup"><span data-stu-id="c0d1e-229"><span id="Supporting_Entity_in_Error"></span><span id="supporting_entity_in_error"></span><span id="SUPPORTING_ENTITY_IN_ERROR"></span>**Supporting Entity in Error** (5)</span></span>
</dt> <dt>

<span data-ttu-id="c0d1e-230"><span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**Зарезервировано DMTF** (..)</span><span class="sxs-lookup"><span data-stu-id="c0d1e-230"><span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF Reserved** (..)</span></span>
</dt> <dt>

<span data-ttu-id="c0d1e-231"><span id="Vendor_Reserved_"></span><span id="vendor_reserved_"></span><span id="VENDOR_RESERVED_"></span>**Поставщик зарезервирован** (0x8000..</span><span class="sxs-lookup"><span data-stu-id="c0d1e-231"><span id="Vendor_Reserved_"></span><span id="vendor_reserved_"></span><span id="VENDOR_RESERVED_"></span>**Vendor Reserved** (0x8000..</span></span> <span data-ttu-id="c0d1e-232">)</span><span class="sxs-lookup"><span data-stu-id="c0d1e-232">)</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="c0d1e-233">**ElementName**</span><span class="sxs-lookup"><span data-stu-id="c0d1e-233">**ElementName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c0d1e-234">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="c0d1e-234">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="c0d1e-235">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="c0d1e-235">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="c0d1e-236">Отображаемое имя объекта.</span><span class="sxs-lookup"><span data-stu-id="c0d1e-236">A display name for the object.</span></span> <span data-ttu-id="c0d1e-237">Это свойство наследуется от [**CIM \_ манажеделемент**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span><span class="sxs-lookup"><span data-stu-id="c0d1e-237">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span></span>

</dd> <dt>

<span data-ttu-id="c0d1e-238">**енабледдефаулт**</span><span class="sxs-lookup"><span data-stu-id="c0d1e-238">**EnabledDefault**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c0d1e-239">Тип данных: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="c0d1e-239">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="c0d1e-240">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="c0d1e-240">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="c0d1e-241">Конфигурация по умолчанию или запуска администратора для включенного состояния элемента.</span><span class="sxs-lookup"><span data-stu-id="c0d1e-241">An administrator's default or startup configuration for the enabled state of an element.</span></span> <span data-ttu-id="c0d1e-242">Это свойство наследуется от [**CIM \_ енабледлогикалелемент**](/previous-versions//cc136818(v=vs.85))и всегда имеет значение 2 (включено).</span><span class="sxs-lookup"><span data-stu-id="c0d1e-242">This property is inherited from [**CIM\_EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)), and it is always set to 2 (Enabled).</span></span>



| <span data-ttu-id="c0d1e-243">Значение</span><span class="sxs-lookup"><span data-stu-id="c0d1e-243">Value</span></span>                                                                        | <span data-ttu-id="c0d1e-244">Значение</span><span class="sxs-lookup"><span data-stu-id="c0d1e-244">Meaning</span></span>            |
|------------------------------------------------------------------------------|--------------------|
| <dl> <span data-ttu-id="c0d1e-245"><dt>2</dt></span><span class="sxs-lookup"><span data-stu-id="c0d1e-245"><dt>2</dt></span></span> </dl> | <span data-ttu-id="c0d1e-246">Активировано</span><span class="sxs-lookup"><span data-stu-id="c0d1e-246">Enabled</span></span><br/> |



 

</dd> <dt>

<span data-ttu-id="c0d1e-247">**EnabledState**</span><span class="sxs-lookup"><span data-stu-id="c0d1e-247">**EnabledState**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c0d1e-248">Тип данных: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="c0d1e-248">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="c0d1e-249">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="c0d1e-249">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="c0d1e-250">Включенные и отключенные состояния элемента.</span><span class="sxs-lookup"><span data-stu-id="c0d1e-250">The enabled and disabled states of an element.</span></span> <span data-ttu-id="c0d1e-251">Он также может указывать на переходы между этими запрошенными состояниями.</span><span class="sxs-lookup"><span data-stu-id="c0d1e-251">It can also indicate the transitions between these requested states.</span></span> <span data-ttu-id="c0d1e-252">Это свойство наследуется от [**CIM \_ енабледлогикалелемент**](/previous-versions//cc136818(v=vs.85))и всегда имеет значение 2 (включено).</span><span class="sxs-lookup"><span data-stu-id="c0d1e-252">This property is inherited from [**CIM\_EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)), and it is always set to 2 (Enabled).</span></span>



| <span data-ttu-id="c0d1e-253">Значение</span><span class="sxs-lookup"><span data-stu-id="c0d1e-253">Value</span></span>                                                                        | <span data-ttu-id="c0d1e-254">Значение</span><span class="sxs-lookup"><span data-stu-id="c0d1e-254">Meaning</span></span>            |
|------------------------------------------------------------------------------|--------------------|
| <dl> <span data-ttu-id="c0d1e-255"><dt>2</dt></span><span class="sxs-lookup"><span data-stu-id="c0d1e-255"><dt>2</dt></span></span> </dl> | <span data-ttu-id="c0d1e-256">Активировано</span><span class="sxs-lookup"><span data-stu-id="c0d1e-256">Enabled</span></span><br/> |



 

</dd> <dt>

<span data-ttu-id="c0d1e-257">**HealthState**</span><span class="sxs-lookup"><span data-stu-id="c0d1e-257">**HealthState**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c0d1e-258">Тип данных: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="c0d1e-258">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="c0d1e-259">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="c0d1e-259">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="c0d1e-260">Текущая работоспособность элемента.</span><span class="sxs-lookup"><span data-stu-id="c0d1e-260">The current health of the element.</span></span> <span data-ttu-id="c0d1e-261">Этот атрибут выражает работоспособность этого элемента, но не обязательно для его подкомпонентов.</span><span class="sxs-lookup"><span data-stu-id="c0d1e-261">This attribute expresses the health of this element but not necessarily that of its subcomponents.</span></span> <span data-ttu-id="c0d1e-262">Возможные значения: от 0 до 30, где 5 означает, что элемент полностью работоспособен, а 30 означает, что элемент полностью нефункциональный.</span><span class="sxs-lookup"><span data-stu-id="c0d1e-262">The possible values are 0 to 30, where 5 means the element is entirely healthy and 30 means the element is completely nonfunctional.</span></span> <span data-ttu-id="c0d1e-263">Это свойство наследуется от [**CIM \_ манажедсистемелемент**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement)и всегда имеет значение 5 (ОК).</span><span class="sxs-lookup"><span data-stu-id="c0d1e-263">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement), and it is always set to 5 (OK).</span></span>



| <span data-ttu-id="c0d1e-264">Значение</span><span class="sxs-lookup"><span data-stu-id="c0d1e-264">Value</span></span>                                                                        | <span data-ttu-id="c0d1e-265">Значение</span><span class="sxs-lookup"><span data-stu-id="c0d1e-265">Meaning</span></span>                                 |
|------------------------------------------------------------------------------|-----------------------------------------|
| <dl> <span data-ttu-id="c0d1e-266"><dt>5</dt></span><span class="sxs-lookup"><span data-stu-id="c0d1e-266"><dt>5</dt></span></span> </dl> | <span data-ttu-id="c0d1e-267">Состояние работоспособности — нормальное.</span><span class="sxs-lookup"><span data-stu-id="c0d1e-267">The health status is normal.</span></span><br/> |



 

</dd> <dt>

<span data-ttu-id="c0d1e-268">**InstallDate**</span><span class="sxs-lookup"><span data-stu-id="c0d1e-268">**InstallDate**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c0d1e-269">Тип данных: **DateTime**</span><span class="sxs-lookup"><span data-stu-id="c0d1e-269">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="c0d1e-270">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="c0d1e-270">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="c0d1e-271">Дата и время создания конфигурации виртуальной машины.</span><span class="sxs-lookup"><span data-stu-id="c0d1e-271">The date and time the virtual machine configuration was created.</span></span> <span data-ttu-id="c0d1e-272">Это свойство наследуется от [**CIM \_ манажедсистемелемент**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span><span class="sxs-lookup"><span data-stu-id="c0d1e-272">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

</dd> <dt>

<span data-ttu-id="c0d1e-273">**InstanceID**</span><span class="sxs-lookup"><span data-stu-id="c0d1e-273">**InstanceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c0d1e-274">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="c0d1e-274">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="c0d1e-275">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="c0d1e-275">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="c0d1e-276">Квалификаторы: **ключ**</span><span class="sxs-lookup"><span data-stu-id="c0d1e-276">Qualifiers: **Key**</span></span>
</dt> </dl>

<span data-ttu-id="c0d1e-277">Уникально идентифицирует экземпляр этого класса.</span><span class="sxs-lookup"><span data-stu-id="c0d1e-277">Uniquely identifies an instance of this class.</span></span> <span data-ttu-id="c0d1e-278">Это свойство наследуется от [**CIM \_ манажеделемент**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement)и всегда имеет значение **null**.</span><span class="sxs-lookup"><span data-stu-id="c0d1e-278">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement), and it is always set to **Null**.</span></span>

</dd> <dt>

<span data-ttu-id="c0d1e-279">**Name**</span><span class="sxs-lookup"><span data-stu-id="c0d1e-279">**Name**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c0d1e-280">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="c0d1e-280">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="c0d1e-281">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="c0d1e-281">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="c0d1e-282">Квалификаторы: **Key**, **maxlen** (256)</span><span class="sxs-lookup"><span data-stu-id="c0d1e-282">Qualifiers: **Key**, **MaxLen** ( 256 )</span></span>
</dt> </dl>

<span data-ttu-id="c0d1e-283">Метка, по которой известен объект.</span><span class="sxs-lookup"><span data-stu-id="c0d1e-283">The label by which the object is known.</span></span> <span data-ttu-id="c0d1e-284">Это свойство наследуется от [**CIM \_ манажедсистемелемент**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement)и всегда имеет значение "репликасвк".</span><span class="sxs-lookup"><span data-stu-id="c0d1e-284">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement), and it is always set to "replicasvc".</span></span>

</dd> <dt>

<span data-ttu-id="c0d1e-285">**оператингстатус**</span><span class="sxs-lookup"><span data-stu-id="c0d1e-285">**OperatingStatus**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c0d1e-286">Тип данных: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="c0d1e-286">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="c0d1e-287">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="c0d1e-287">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="c0d1e-288">Предоставляет сведения о текущем состоянии для рабочего условия элемента и может использоваться для предоставления более подробных сведений относительно значения свойства **EnabledState** .</span><span class="sxs-lookup"><span data-stu-id="c0d1e-288">Provides current status information for the operational condition of the element and can be used for providing more detail with respect to the value of the **EnabledState** property.</span></span> <span data-ttu-id="c0d1e-289">Значение **null** указывает, что это свойство не реализовано.</span><span class="sxs-lookup"><span data-stu-id="c0d1e-289">A **Null** value indicates that this property is not implemented.</span></span> <span data-ttu-id="c0d1e-290">Это свойство наследуется от [**CIM \_ манажедсистемелемент**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span><span class="sxs-lookup"><span data-stu-id="c0d1e-290">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

<dl> <dt>

<span data-ttu-id="c0d1e-291"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Неизвестно** (0)</span><span class="sxs-lookup"><span data-stu-id="c0d1e-291"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (0)</span></span>
</dt> <dt>

<span data-ttu-id="c0d1e-292"><span id="Not_Available"></span><span id="not_available"></span><span id="NOT_AVAILABLE"></span>**Недоступно** (1)</span><span class="sxs-lookup"><span data-stu-id="c0d1e-292"><span id="Not_Available"></span><span id="not_available"></span><span id="NOT_AVAILABLE"></span>**Not Available** (1)</span></span>
</dt> <dt>

<span data-ttu-id="c0d1e-293"><span id="Servicing"></span><span id="servicing"></span><span id="SERVICING"></span>**Обслуживание** (2)</span><span class="sxs-lookup"><span data-stu-id="c0d1e-293"><span id="Servicing"></span><span id="servicing"></span><span id="SERVICING"></span>**Servicing** (2)</span></span>
</dt> <dt>

<span data-ttu-id="c0d1e-294"><span id="Starting"></span><span id="starting"></span><span id="STARTING"></span>**Запуск** (3)</span><span class="sxs-lookup"><span data-stu-id="c0d1e-294"><span id="Starting"></span><span id="starting"></span><span id="STARTING"></span>**Starting** (3)</span></span>
</dt> <dt>

<span data-ttu-id="c0d1e-295"><span id="Stopping"></span><span id="stopping"></span><span id="STOPPING"></span>**Остановка** (4)</span><span class="sxs-lookup"><span data-stu-id="c0d1e-295"><span id="Stopping"></span><span id="stopping"></span><span id="STOPPING"></span>**Stopping** (4)</span></span>
</dt> <dt>

<span data-ttu-id="c0d1e-296"><span id="Stopped"></span><span id="stopped"></span><span id="STOPPED"></span>**Остановлено** (5)</span><span class="sxs-lookup"><span data-stu-id="c0d1e-296"><span id="Stopped"></span><span id="stopped"></span><span id="STOPPED"></span>**Stopped** (5)</span></span>
</dt> <dt>

<span data-ttu-id="c0d1e-297"><span id="Aborted"></span><span id="aborted"></span><span id="ABORTED"></span>**Прервано** (6)</span><span class="sxs-lookup"><span data-stu-id="c0d1e-297"><span id="Aborted"></span><span id="aborted"></span><span id="ABORTED"></span>**Aborted** (6)</span></span>
</dt> <dt>

<span data-ttu-id="c0d1e-298"><span id="Dormant"></span><span id="dormant"></span><span id="DORMANT"></span>**Неактивный** (7)</span><span class="sxs-lookup"><span data-stu-id="c0d1e-298"><span id="Dormant"></span><span id="dormant"></span><span id="DORMANT"></span>**Dormant** (7)</span></span>
</dt> <dt>

<span data-ttu-id="c0d1e-299"><span id="Completed"></span><span id="completed"></span><span id="COMPLETED"></span>**Завершено** (8)</span><span class="sxs-lookup"><span data-stu-id="c0d1e-299"><span id="Completed"></span><span id="completed"></span><span id="COMPLETED"></span>**Completed** (8)</span></span>
</dt> <dt>

<span data-ttu-id="c0d1e-300"><span id="Migrating"></span><span id="migrating"></span><span id="MIGRATING"></span>**Миграция** (9)</span><span class="sxs-lookup"><span data-stu-id="c0d1e-300"><span id="Migrating"></span><span id="migrating"></span><span id="MIGRATING"></span>**Migrating** (9)</span></span>
</dt> <dt>

<span data-ttu-id="c0d1e-301"><span id="Emigrating"></span><span id="emigrating"></span><span id="EMIGRATING"></span>**Емигратинг** (10)</span><span class="sxs-lookup"><span data-stu-id="c0d1e-301"><span id="Emigrating"></span><span id="emigrating"></span><span id="EMIGRATING"></span>**Emigrating** (10)</span></span>
</dt> <dt>

<span data-ttu-id="c0d1e-302"><span id="Immigrating"></span><span id="immigrating"></span><span id="IMMIGRATING"></span>**Перемиграция** (11)</span><span class="sxs-lookup"><span data-stu-id="c0d1e-302"><span id="Immigrating"></span><span id="immigrating"></span><span id="IMMIGRATING"></span>**Immigrating** (11)</span></span>
</dt> <dt>

<span data-ttu-id="c0d1e-303"><span id="Snapshotting"></span><span id="snapshotting"></span><span id="SNAPSHOTTING"></span>**Значит** (12)</span><span class="sxs-lookup"><span data-stu-id="c0d1e-303"><span id="Snapshotting"></span><span id="snapshotting"></span><span id="SNAPSHOTTING"></span>**Snapshotting** (12)</span></span>
</dt> <dt>

<span data-ttu-id="c0d1e-304"><span id="Shutting_Down"></span><span id="shutting_down"></span><span id="SHUTTING_DOWN"></span>**Завершение работы** (13)</span><span class="sxs-lookup"><span data-stu-id="c0d1e-304"><span id="Shutting_Down"></span><span id="shutting_down"></span><span id="SHUTTING_DOWN"></span>**Shutting Down** (13)</span></span>
</dt> <dt>

<span data-ttu-id="c0d1e-305"><span id="In_Test"></span><span id="in_test"></span><span id="IN_TEST"></span>**В тесте** (14)</span><span class="sxs-lookup"><span data-stu-id="c0d1e-305"><span id="In_Test"></span><span id="in_test"></span><span id="IN_TEST"></span>**In Test** (14)</span></span>
</dt> <dt>

<span data-ttu-id="c0d1e-306"><span id="Transitioning"></span><span id="transitioning"></span><span id="TRANSITIONING"></span>**Переход** (15)</span><span class="sxs-lookup"><span data-stu-id="c0d1e-306"><span id="Transitioning"></span><span id="transitioning"></span><span id="TRANSITIONING"></span>**Transitioning** (15)</span></span>
</dt> <dt>

<span data-ttu-id="c0d1e-307"><span id="In_Service"></span><span id="in_service"></span><span id="IN_SERVICE"></span>**В службе** (16)</span><span class="sxs-lookup"><span data-stu-id="c0d1e-307"><span id="In_Service"></span><span id="in_service"></span><span id="IN_SERVICE"></span>**In Service** (16)</span></span>
</dt> <dt>

<span data-ttu-id="c0d1e-308"><span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**Зарезервировано DMTF** (..)</span><span class="sxs-lookup"><span data-stu-id="c0d1e-308"><span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF Reserved** (..)</span></span>
</dt> <dt>

<span data-ttu-id="c0d1e-309"><span id="Vendor_Reserved_"></span><span id="vendor_reserved_"></span><span id="VENDOR_RESERVED_"></span>**Поставщик зарезервирован** (0x8000..</span><span class="sxs-lookup"><span data-stu-id="c0d1e-309"><span id="Vendor_Reserved_"></span><span id="vendor_reserved_"></span><span id="VENDOR_RESERVED_"></span>**Vendor Reserved** (0x8000..</span></span> <span data-ttu-id="c0d1e-310">)</span><span class="sxs-lookup"><span data-stu-id="c0d1e-310">)</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="c0d1e-311">**OperationalStatus**</span><span class="sxs-lookup"><span data-stu-id="c0d1e-311">**OperationalStatus**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c0d1e-312">Тип данных: **UInt16** , массив</span><span class="sxs-lookup"><span data-stu-id="c0d1e-312">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="c0d1e-313">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="c0d1e-313">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="c0d1e-314">Массив, содержащий текущие состояния объекта.</span><span class="sxs-lookup"><span data-stu-id="c0d1e-314">An array that contains the current statuses of the object.</span></span> <span data-ttu-id="c0d1e-315">Это свойство наследуется от [**CIM \_ манажедсистемелемент**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span><span class="sxs-lookup"><span data-stu-id="c0d1e-315">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span> <span data-ttu-id="c0d1e-316">Значением с нулевым индексом будет одно из следующих значений.</span><span class="sxs-lookup"><span data-stu-id="c0d1e-316">The value at index zero will be one of the following values.</span></span>



| <span data-ttu-id="c0d1e-317">Значение</span><span class="sxs-lookup"><span data-stu-id="c0d1e-317">Value</span></span>                                                                                                                                                                                                               | <span data-ttu-id="c0d1e-318">Значение</span><span class="sxs-lookup"><span data-stu-id="c0d1e-318">Meaning</span></span>                                                                                                                       |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------|
| <span id="OK"></span><span id="ok"></span><dl> <span data-ttu-id="c0d1e-319"><dt>**ОК**</dt> <dt>2</dt></span><span class="sxs-lookup"><span data-stu-id="c0d1e-319"><dt>**OK**</dt> <dt>2</dt></span></span> </dl>                                  | <span data-ttu-id="c0d1e-320">Служба репликации работает нормально.</span><span class="sxs-lookup"><span data-stu-id="c0d1e-320">The replication service is operating normally.</span></span><br/>                                                                     |
| <span id="Error"></span><span id="error"></span><span id="ERROR"></span><dl> <span data-ttu-id="c0d1e-321"><dt>**Ошибка**</dt> <dt>6</dt></span><span class="sxs-lookup"><span data-stu-id="c0d1e-321"><dt>**Error**</dt> <dt>6</dt></span></span> </dl> | <span data-ttu-id="c0d1e-322">Один или несколько прослушивателей сети репликации не работают.</span><span class="sxs-lookup"><span data-stu-id="c0d1e-322">One or more replication network listeners are not running.</span></span> <span data-ttu-id="c0d1e-323">Убедитесь, что параметры службы репликации являются допустимыми.</span><span class="sxs-lookup"><span data-stu-id="c0d1e-323">Verify that the replication service settings are valid.</span></span><br/> |



 

</dd> <dt>

<span data-ttu-id="c0d1e-324">**осеренабледстате**</span><span class="sxs-lookup"><span data-stu-id="c0d1e-324">**OtherEnabledState**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c0d1e-325">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="c0d1e-325">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="c0d1e-326">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="c0d1e-326">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="c0d1e-327">Строка, описывающая включенное или отключенное состояние элемента, если свойство **EnabledState** имеет значение 1 ("другое").</span><span class="sxs-lookup"><span data-stu-id="c0d1e-327">A string that describes the enabled or disabled state of the element when the **EnabledState** property is set to 1 ("Other").</span></span> <span data-ttu-id="c0d1e-328">Для этого свойства необходимо задать значение **null** , если параметр **EnabledState** имеет любое значение, отличное от 1.</span><span class="sxs-lookup"><span data-stu-id="c0d1e-328">This property must be set to **Null** when **EnabledState** is any value other than 1.</span></span> <span data-ttu-id="c0d1e-329">Это свойство наследуется от [**CIM \_ енабледлогикалелемент**](/previous-versions//cc136818(v=vs.85))и всегда имеет значение **null**.</span><span class="sxs-lookup"><span data-stu-id="c0d1e-329">This property is inherited from [**CIM\_EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)), and it is always set to **Null**.</span></span>

</dd> <dt>

<span data-ttu-id="c0d1e-330">**примарйовнерконтакт**</span><span class="sxs-lookup"><span data-stu-id="c0d1e-330">**PrimaryOwnerContact**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c0d1e-331">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="c0d1e-331">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="c0d1e-332">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="c0d1e-332">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="c0d1e-333">Квалификаторы: **maxlen** (256)</span><span class="sxs-lookup"><span data-stu-id="c0d1e-333">Qualifiers: **MaxLen** ( 256 )</span></span>
</dt> </dl>

<span data-ttu-id="c0d1e-334">Любые сведения о том, как можно достичь основного владельца службы (например, номер телефона, адрес электронной почты и т. д.).</span><span class="sxs-lookup"><span data-stu-id="c0d1e-334">Any information about how the primary owner of the service can be reached (for example, phone number, email address, and so on).</span></span> <span data-ttu-id="c0d1e-335">Это свойство наследуется [**от \_ службы CIM**](/windows/desktop/CIMWin32Prov/cim-service)и всегда имеет значение **null**.</span><span class="sxs-lookup"><span data-stu-id="c0d1e-335">This property is inherited from [**CIM\_Service**](/windows/desktop/CIMWin32Prov/cim-service), and it is always set to **Null**.</span></span>

</dd> <dt>

<span data-ttu-id="c0d1e-336">**примарйовнернаме**</span><span class="sxs-lookup"><span data-stu-id="c0d1e-336">**PrimaryOwnerName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c0d1e-337">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="c0d1e-337">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="c0d1e-338">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="c0d1e-338">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="c0d1e-339">Квалификаторы: **maxlen** (64)</span><span class="sxs-lookup"><span data-stu-id="c0d1e-339">Qualifiers: **MaxLen** ( 64 )</span></span>
</dt> </dl>

<span data-ttu-id="c0d1e-340">Имя основного владельца службы, если она определена.</span><span class="sxs-lookup"><span data-stu-id="c0d1e-340">The name of the primary owner for the service, if one is defined.</span></span> <span data-ttu-id="c0d1e-341">Первичный владелец — это первоначальный контактный контакт для службы поддержки.</span><span class="sxs-lookup"><span data-stu-id="c0d1e-341">The primary owner is the initial support contact for the service.</span></span> <span data-ttu-id="c0d1e-342">Это свойство наследуется [**от \_ службы CIM**](/windows/desktop/CIMWin32Prov/cim-service)и всегда имеет значение **null**.</span><span class="sxs-lookup"><span data-stu-id="c0d1e-342">This property is inherited from [**CIM\_Service**](/windows/desktop/CIMWin32Prov/cim-service), and it is always set to **Null**.</span></span>

</dd> <dt>

<span data-ttu-id="c0d1e-343">**примаристатус**</span><span class="sxs-lookup"><span data-stu-id="c0d1e-343">**PrimaryStatus**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c0d1e-344">Тип данных: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="c0d1e-344">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="c0d1e-345">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="c0d1e-345">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="c0d1e-346">Предоставляет сведения о состоянии высокого уровня.</span><span class="sxs-lookup"><span data-stu-id="c0d1e-346">Provides high level status information.</span></span> <span data-ttu-id="c0d1e-347">Это свойство следует использовать вместе со свойством **детаиледстатус** , чтобы обеспечить высокий уровень и подробные сведения о состоянии работоспособности элемента и его подкомпонентов.</span><span class="sxs-lookup"><span data-stu-id="c0d1e-347">This property should be used in conjunction with the **DetailedStatus** property to provide high level and detailed health status of the element and its subcomponents.</span></span> <span data-ttu-id="c0d1e-348">Значение **null** указывает, что это свойство не реализовано.</span><span class="sxs-lookup"><span data-stu-id="c0d1e-348">A **Null** value indicates that this property is not implemented.</span></span> <span data-ttu-id="c0d1e-349">Это свойство наследуется от [**CIM \_ манажедсистемелемент**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span><span class="sxs-lookup"><span data-stu-id="c0d1e-349">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

<dl> <dt>

<span data-ttu-id="c0d1e-350"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Неизвестно** (0)</span><span class="sxs-lookup"><span data-stu-id="c0d1e-350"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (0)</span></span>
</dt> <dt>

<span data-ttu-id="c0d1e-351"><span id="OK"></span><span id="ok"></span>**ОК** (1)</span><span class="sxs-lookup"><span data-stu-id="c0d1e-351"><span id="OK"></span><span id="ok"></span>**OK** (1)</span></span>
</dt> <dt>

<span data-ttu-id="c0d1e-352"><span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>С **пониженной производительностью** (2)</span><span class="sxs-lookup"><span data-stu-id="c0d1e-352"><span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>**Degraded** (2)</span></span>
</dt> <dt>

<span data-ttu-id="c0d1e-353"><span id="Error"></span><span id="error"></span><span id="ERROR"></span>**Ошибка** (3)</span><span class="sxs-lookup"><span data-stu-id="c0d1e-353"><span id="Error"></span><span id="error"></span><span id="ERROR"></span>**Error** (3)</span></span>
</dt> <dt>

<span data-ttu-id="c0d1e-354"><span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**Зарезервировано DMTF** (..)</span><span class="sxs-lookup"><span data-stu-id="c0d1e-354"><span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF Reserved** (..)</span></span>
</dt> <dt>

<span data-ttu-id="c0d1e-355"><span id="Vendor_Reserved_"></span><span id="vendor_reserved_"></span><span id="VENDOR_RESERVED_"></span>**Поставщик зарезервирован** (0x8000..</span><span class="sxs-lookup"><span data-stu-id="c0d1e-355"><span id="Vendor_Reserved_"></span><span id="vendor_reserved_"></span><span id="VENDOR_RESERVED_"></span>**Vendor Reserved** (0x8000..</span></span> <span data-ttu-id="c0d1e-356">)</span><span class="sxs-lookup"><span data-stu-id="c0d1e-356">)</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="c0d1e-357">**RequestedState**</span><span class="sxs-lookup"><span data-stu-id="c0d1e-357">**RequestedState**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c0d1e-358">Тип данных: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="c0d1e-358">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="c0d1e-359">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="c0d1e-359">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="c0d1e-360">Последнее запрошенное или требуемое состояние элемента.</span><span class="sxs-lookup"><span data-stu-id="c0d1e-360">The last requested or desired state for the element.</span></span> <span data-ttu-id="c0d1e-361">Фактическое состояние элемента представлено параметром **EnabledState**.</span><span class="sxs-lookup"><span data-stu-id="c0d1e-361">The actual state of the element is represented by **EnabledState**.</span></span> <span data-ttu-id="c0d1e-362">Это свойство предназначено для сравнения последнего запрошенного и текущего состояний элемента.</span><span class="sxs-lookup"><span data-stu-id="c0d1e-362">This property is provided to compare the last requested and current states for an element.</span></span> <span data-ttu-id="c0d1e-363">Конкретный экземпляр класса [**CIM \_ енабледлогикалелемент**](/previous-versions//cc136818(v=vs.85)) может не поддерживать свойство **RequestedState** .</span><span class="sxs-lookup"><span data-stu-id="c0d1e-363">A particular instance of the [**CIM\_EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)) class might not support the **RequestedState** property.</span></span> <span data-ttu-id="c0d1e-364">В этом случае используется значение 12 ("неприменимо").</span><span class="sxs-lookup"><span data-stu-id="c0d1e-364">If this occurs, the value 12 ("Not Applicable") is used.</span></span> <span data-ttu-id="c0d1e-365">Это свойство наследуется от **CIM \_ енабледлогикалелемент** и всегда имеет значение 12 (неприменимо).</span><span class="sxs-lookup"><span data-stu-id="c0d1e-365">This property is inherited from **CIM\_EnabledLogicalElement**, and it is always set to 12 (Not Applicable).</span></span>



| <span data-ttu-id="c0d1e-366">Значение</span><span class="sxs-lookup"><span data-stu-id="c0d1e-366">Value</span></span>                                                                         | <span data-ttu-id="c0d1e-367">Значение</span><span class="sxs-lookup"><span data-stu-id="c0d1e-367">Meaning</span></span>                    |
|-------------------------------------------------------------------------------|----------------------------|
| <dl> <span data-ttu-id="c0d1e-368"><dt>12</dt></span><span class="sxs-lookup"><span data-stu-id="c0d1e-368"><dt>12</dt></span></span> </dl> | <span data-ttu-id="c0d1e-369">Не применяется</span><span class="sxs-lookup"><span data-stu-id="c0d1e-369">Not applicable.</span></span><br/> |



 

</dd> <dt>

<span data-ttu-id="c0d1e-370">**Запуск**</span><span class="sxs-lookup"><span data-stu-id="c0d1e-370">**Started**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c0d1e-371">Тип данных: **логический**</span><span class="sxs-lookup"><span data-stu-id="c0d1e-371">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="c0d1e-372">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="c0d1e-372">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="c0d1e-373">Указывает, запущена ли служба в данный момент.</span><span class="sxs-lookup"><span data-stu-id="c0d1e-373">Indicates whether the service is currently running.</span></span> <span data-ttu-id="c0d1e-374">Это свойство наследуется [**от \_ службы CIM**](/windows/desktop/CIMWin32Prov/cim-service)и всегда имеет значение **true**.</span><span class="sxs-lookup"><span data-stu-id="c0d1e-374">This property is inherited from [**CIM\_Service**](/windows/desktop/CIMWin32Prov/cim-service), and it is always set to **True**.</span></span>

</dd> <dt>

<span data-ttu-id="c0d1e-375">**StartMode**</span><span class="sxs-lookup"><span data-stu-id="c0d1e-375">**StartMode**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c0d1e-376">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="c0d1e-376">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="c0d1e-377">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="c0d1e-377">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="c0d1e-378">Квалификаторы: **maxlen** (10)</span><span class="sxs-lookup"><span data-stu-id="c0d1e-378">Qualifiers: **MaxLen** ( 10 )</span></span>
</dt> </dl>

<span data-ttu-id="c0d1e-379">Строковое значение, указывающее, запускается ли служба автоматически системой, операционной системой или запускается только по запросу.</span><span class="sxs-lookup"><span data-stu-id="c0d1e-379">A string value that indicates whether the service is automatically started by a system, an operating system, or is started only upon request.</span></span> <span data-ttu-id="c0d1e-380">Это свойство наследуется [**от \_ службы CIM**](/windows/desktop/CIMWin32Prov/cim-service)и всегда имеет значение **null**.</span><span class="sxs-lookup"><span data-stu-id="c0d1e-380">This property is inherited from [**CIM\_Service**](/windows/desktop/CIMWin32Prov/cim-service), and it is always set to **Null**.</span></span>

</dd> <dt>

<span data-ttu-id="c0d1e-381">**Состояние**</span><span class="sxs-lookup"><span data-stu-id="c0d1e-381">**Status**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c0d1e-382">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="c0d1e-382">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="c0d1e-383">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="c0d1e-383">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="c0d1e-384">Указывает состояние элемента.</span><span class="sxs-lookup"><span data-stu-id="c0d1e-384">Indicates the status of the element.</span></span> <span data-ttu-id="c0d1e-385">Это свойство наследуется от [**CIM \_ манажедсистемелемент**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement)и всегда имеет значение "ОК".</span><span class="sxs-lookup"><span data-stu-id="c0d1e-385">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement), and it is always set to "OK".</span></span>

</dd> <dt>

<span data-ttu-id="c0d1e-386">**статусдескриптионс**</span><span class="sxs-lookup"><span data-stu-id="c0d1e-386">**StatusDescriptions**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c0d1e-387">Тип данных: массив **строк**</span><span class="sxs-lookup"><span data-stu-id="c0d1e-387">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="c0d1e-388">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="c0d1e-388">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="c0d1e-389">Строки, описывающие различные значения массива **OperationalStatus** .</span><span class="sxs-lookup"><span data-stu-id="c0d1e-389">Strings that describe the various **OperationalStatus** array values.</span></span> <span data-ttu-id="c0d1e-390">Это свойство наследуется от [**CIM \_ манажедсистемелемент**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span><span class="sxs-lookup"><span data-stu-id="c0d1e-390">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

</dd> <dt>

<span data-ttu-id="c0d1e-391">**системкреатионкласснаме**</span><span class="sxs-lookup"><span data-stu-id="c0d1e-391">**SystemCreationClassName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c0d1e-392">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="c0d1e-392">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="c0d1e-393">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="c0d1e-393">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="c0d1e-394">Квалификаторы: **Key**, **maxlen** (256)</span><span class="sxs-lookup"><span data-stu-id="c0d1e-394">Qualifiers: **Key**, **MaxLen** ( 256 )</span></span>
</dt> </dl>

<span data-ttu-id="c0d1e-395">Имя класса создания системы области.</span><span class="sxs-lookup"><span data-stu-id="c0d1e-395">The scoping system's creation class name.</span></span> <span data-ttu-id="c0d1e-396">Это свойство наследуется [**от \_ службы CIM**](/windows/desktop/CIMWin32Prov/cim-service)и всегда имеет значение "мсвм \_ ComputerSystem".</span><span class="sxs-lookup"><span data-stu-id="c0d1e-396">This property is inherited from [**CIM\_Service**](/windows/desktop/CIMWin32Prov/cim-service), and it is always set to "Msvm\_ComputerSystem".</span></span>

</dd> <dt>

<span data-ttu-id="c0d1e-397">**SystemName**</span><span class="sxs-lookup"><span data-stu-id="c0d1e-397">**SystemName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c0d1e-398">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="c0d1e-398">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="c0d1e-399">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="c0d1e-399">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="c0d1e-400">Квалификаторы: **Key**, **maxlen** (256)</span><span class="sxs-lookup"><span data-stu-id="c0d1e-400">Qualifiers: **Key**, **MaxLen** ( 256 )</span></span>
</dt> </dl>

<span data-ttu-id="c0d1e-401">NetBIOS-имя системы размещающего компьютера.</span><span class="sxs-lookup"><span data-stu-id="c0d1e-401">The NetBIOS name of the hosting computer system.</span></span> <span data-ttu-id="c0d1e-402">Это свойство наследуется [**от \_ службы CIM**](/windows/desktop/CIMWin32Prov/cim-service).</span><span class="sxs-lookup"><span data-stu-id="c0d1e-402">This property is inherited from [**CIM\_Service**](/windows/desktop/CIMWin32Prov/cim-service).</span></span>

</dd> <dt>

<span data-ttu-id="c0d1e-403">**тимеофластстатечанже**</span><span class="sxs-lookup"><span data-stu-id="c0d1e-403">**TimeOfLastStateChange**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c0d1e-404">Тип данных: **DateTime**</span><span class="sxs-lookup"><span data-stu-id="c0d1e-404">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="c0d1e-405">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="c0d1e-405">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="c0d1e-406">Дата или время последнего изменения включенного состояния элемента.</span><span class="sxs-lookup"><span data-stu-id="c0d1e-406">The date or time when the enabled state of the element last changed.</span></span> <span data-ttu-id="c0d1e-407">Это свойство наследуется от [**CIM \_ енабледлогикалелемент**](/previous-versions//cc136818(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="c0d1e-407">This property is inherited from [**CIM\_EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)).</span></span>

</dd> <dt>

<span data-ttu-id="c0d1e-408">**транситионингтостате**</span><span class="sxs-lookup"><span data-stu-id="c0d1e-408">**TransitioningToState**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c0d1e-409">Тип данных: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="c0d1e-409">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="c0d1e-410">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="c0d1e-410">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="c0d1e-411">Указывает целевое состояние, в которое переходит экземпляр.</span><span class="sxs-lookup"><span data-stu-id="c0d1e-411">Indicates the target state to which the instance is transitioning.</span></span> <span data-ttu-id="c0d1e-412">Это свойство наследуется от [**CIM \_ енабледлогикалелемент**](/previous-versions//cc136818(v=vs.85))и всегда имеет значение **null**.</span><span class="sxs-lookup"><span data-stu-id="c0d1e-412">This property is inherited from [**CIM\_EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)), and it is always set to **Null**.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="c0d1e-413">Требования</span><span class="sxs-lookup"><span data-stu-id="c0d1e-413">Requirements</span></span>



| <span data-ttu-id="c0d1e-414">Требование</span><span class="sxs-lookup"><span data-stu-id="c0d1e-414">Requirement</span></span> | <span data-ttu-id="c0d1e-415">Значение</span><span class="sxs-lookup"><span data-stu-id="c0d1e-415">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="c0d1e-416">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="c0d1e-416">Minimum supported client</span></span><br/> | <span data-ttu-id="c0d1e-417">\[Только классические приложения Windows 8\]</span><span class="sxs-lookup"><span data-stu-id="c0d1e-417">Windows 8 \[desktop apps only\]</span></span><br/>                                                              |
| <span data-ttu-id="c0d1e-418">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="c0d1e-418">Minimum supported server</span></span><br/> | <span data-ttu-id="c0d1e-419">\[Только для настольных приложений Windows Server 2012\]</span><span class="sxs-lookup"><span data-stu-id="c0d1e-419">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="c0d1e-420">Пространство имен</span><span class="sxs-lookup"><span data-stu-id="c0d1e-420">Namespace</span></span><br/>                | <span data-ttu-id="c0d1e-421">Корневая \\ виртуализация \\ версии 2</span><span class="sxs-lookup"><span data-stu-id="c0d1e-421">Root\\Virtualization\\V2</span></span><br/>                                                                     |
| <span data-ttu-id="c0d1e-422">MOF</span><span class="sxs-lookup"><span data-stu-id="c0d1e-422">MOF</span></span><br/>                      | <dl> <span data-ttu-id="c0d1e-423"><dt>Виндовсвиртуализатион. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="c0d1e-423"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="c0d1e-424">DLL</span><span class="sxs-lookup"><span data-stu-id="c0d1e-424">DLL</span></span><br/>                      | <dl> <span data-ttu-id="c0d1e-425"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="c0d1e-425"><dt>Vmms.exe</dt></span></span> </dl>                     |



 

