---
description: Представляет службу миграции виртуальной системы. Он используется для миграции виртуальной системы или для переноса хранилища виртуальной системы с одной платформы виртуализации в другую.
ms.assetid: af25e405-4498-40a8-ba8e-4b3873c56097
title: Класс Msvm_VirtualSystemMigrationService
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_VirtualSystemMigrationService
- Msvm_VirtualSystemMigrationService.InstanceID
- Msvm_VirtualSystemMigrationService.Caption
- Msvm_VirtualSystemMigrationService.Description
- Msvm_VirtualSystemMigrationService.ElementName
- Msvm_VirtualSystemMigrationService.InstallDate
- Msvm_VirtualSystemMigrationService.OperationalStatus
- Msvm_VirtualSystemMigrationService.StatusDescriptions
- Msvm_VirtualSystemMigrationService.Status
- Msvm_VirtualSystemMigrationService.HealthState
- Msvm_VirtualSystemMigrationService.CommunicationStatus
- Msvm_VirtualSystemMigrationService.DetailedStatus
- Msvm_VirtualSystemMigrationService.OperatingStatus
- Msvm_VirtualSystemMigrationService.PrimaryStatus
- Msvm_VirtualSystemMigrationService.EnabledState
- Msvm_VirtualSystemMigrationService.OtherEnabledState
- Msvm_VirtualSystemMigrationService.RequestedState
- Msvm_VirtualSystemMigrationService.EnabledDefault
- Msvm_VirtualSystemMigrationService.TimeOfLastStateChange
- Msvm_VirtualSystemMigrationService.AvailableRequestedStates
- Msvm_VirtualSystemMigrationService.TransitioningToState
- Msvm_VirtualSystemMigrationService.SystemCreationClassName
- Msvm_VirtualSystemMigrationService.SystemName
- Msvm_VirtualSystemMigrationService.Name
- Msvm_VirtualSystemMigrationService.CreationClassName
- Msvm_VirtualSystemMigrationService.PrimaryOwnerName
- Msvm_VirtualSystemMigrationService.PrimaryOwnerContact
- Msvm_VirtualSystemMigrationService.StartMode
- Msvm_VirtualSystemMigrationService.Started
- Msvm_VirtualSystemMigrationService.ActiveVirtualSystemMigrationCount
- Msvm_VirtualSystemMigrationService.ActiveStorageMigrationCount
- Msvm_VirtualSystemMigrationService.MigrationServiceListenerIPAddressList
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: 1e80cb12e6e6767b49670a1aff68c9791f224068
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "103808765"
---
# <a name="msvm_virtualsystemmigrationservice-class"></a><span data-ttu-id="e5eae-104">\_Класс мсвм виртуалсистеммигратионсервице</span><span class="sxs-lookup"><span data-stu-id="e5eae-104">Msvm\_VirtualSystemMigrationService class</span></span>

<span data-ttu-id="e5eae-105">Представляет службу миграции виртуальной системы.</span><span class="sxs-lookup"><span data-stu-id="e5eae-105">Represents the virtual system migration service.</span></span> <span data-ttu-id="e5eae-106">Он используется для миграции виртуальной системы или для переноса хранилища виртуальной системы с одной платформы виртуализации в другую.</span><span class="sxs-lookup"><span data-stu-id="e5eae-106">It is used for migrating a virtual system or for migrating the storage of a virtual system from one virtualization platform to another.</span></span>

<span data-ttu-id="e5eae-107">Следующий синтаксис является упрощенным MOF-файлным (MOF) кодом и включает все наследуемые свойства.</span><span class="sxs-lookup"><span data-stu-id="e5eae-107">The following syntax is simplified Managed Object Format (MOF) code, and it includes all of the inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="e5eae-108">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="e5eae-108">Syntax</span></span>

``` syntax
[Dynamic, Provider("VmmsWmiInstanceAndMethodProvider"), AMENDMENT]
class Msvm_VirtualSystemMigrationService : CIM_VirtualSystemMigrationService
{
  string   InstanceID;
  string   Caption = "Hyper-V Migration Service";
  string   Description = "Hyper-V Migration Service";
  string   ElementName = "Hyper-V Migration Service";
  datetime InstallDate;
  uint16   OperationalStatus[] = 2;
  string   StatusDescriptions[] = "OK";
  string   Status = "OK";
  uint16   HealthState = 5;
  uint16   CommunicationStatus;
  uint16   DetailedStatus;
  uint16   OperatingStatus;
  uint16   PrimaryStatus;
  string   EnabledState = 2;
  string   OtherEnabledState;
  uint16   RequestedState = 12;
  uint16   EnabledDefault = 2;
  datetime TimeOfLastStateChange;
  uint16   AvailableRequestedStates[];
  uint16   TransitioningToState;
  string   SystemCreationClassName = "Msvm_ComputerSystem";
  string   SystemName;
  string   Name = "migrationwmi";
  string   CreationClassName = "Msvm_VirtualSystemMigrationService";
  string   PrimaryOwnerName;
  string   PrimaryOwnerContact;
  string   StartMode;
  boolean  Started;
  uint32   ActiveVirtualSystemMigrationCount;
  uint32   ActiveStorageMigrationCount;
  string   MigrationServiceListenerIPAddressList[];
};
```

## <a name="members"></a><span data-ttu-id="e5eae-109">Члены</span><span class="sxs-lookup"><span data-stu-id="e5eae-109">Members</span></span>

<span data-ttu-id="e5eae-110">Класс **мсвм \_ виртуалсистеммигратионсервице** имеет следующие типы членов:</span><span class="sxs-lookup"><span data-stu-id="e5eae-110">The **Msvm\_VirtualSystemMigrationService** class has these types of members:</span></span>

-   [<span data-ttu-id="e5eae-111">Методы</span><span class="sxs-lookup"><span data-stu-id="e5eae-111">Methods</span></span>](#methods)
-   [<span data-ttu-id="e5eae-112">Свойства</span><span class="sxs-lookup"><span data-stu-id="e5eae-112">Properties</span></span>](#properties)

### <a name="methods"></a><span data-ttu-id="e5eae-113">Методы</span><span class="sxs-lookup"><span data-stu-id="e5eae-113">Methods</span></span>

<span data-ttu-id="e5eae-114">Класс **мсвм \_ виртуалсистеммигратионсервице** содержит следующие методы.</span><span class="sxs-lookup"><span data-stu-id="e5eae-114">The **Msvm\_VirtualSystemMigrationService** class has these methods.</span></span>



| <span data-ttu-id="e5eae-115">Метод</span><span class="sxs-lookup"><span data-stu-id="e5eae-115">Method</span></span>                                                                                                                  | <span data-ttu-id="e5eae-116">Описание</span><span class="sxs-lookup"><span data-stu-id="e5eae-116">Description</span></span>                                                                                                                                                                  |
|:------------------------------------------------------------------------------------------------------------------------|:-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="e5eae-117">**адднетворксеттингс**</span><span class="sxs-lookup"><span data-stu-id="e5eae-117">**AddNetworkSettings**</span></span>](addnetworksettings-msvm-virtualsystemmigrationservice.md)                                     | <span data-ttu-id="e5eae-118">Добавляет подсети миграции сети для службы миграции виртуальной системы.</span><span class="sxs-lookup"><span data-stu-id="e5eae-118">Adds migration network subnets for the virtual system migration service.</span></span><br/>                                                                                          |
| [<span data-ttu-id="e5eae-119">**чекксистемкомпатибилитинфо**</span><span class="sxs-lookup"><span data-stu-id="e5eae-119">**CheckSystemCompatibilityInfo**</span></span>](checksystemcompatibilityinfo-msvm-virtualsystemmigrationservice.md)                 | <span data-ttu-id="e5eae-120">Проверяет сведения о совместимости для обеспечения совместимости с системой размещающего компьютера.</span><span class="sxs-lookup"><span data-stu-id="e5eae-120">Checks the compatibility information for compatibility with the hosting computer system.</span></span><br/>                                                                          |
| [<span data-ttu-id="e5eae-121">**чекквиртуалсистемисмигратабле**</span><span class="sxs-lookup"><span data-stu-id="e5eae-121">**CheckVirtualSystemIsMigratable**</span></span>](checkvirtualsystemismigratable-msvm-virtualsystemmigrationservice.md)             | <span data-ttu-id="e5eae-122">Метод миграции виртуальной системы или хранилища виртуальной системы на целевой узел, заданный именем узла.</span><span class="sxs-lookup"><span data-stu-id="e5eae-122">Method to migrate a virtual system or the storage of a virtual system to a destination host specified by a hostname.</span></span><br/>                                              |
| [<span data-ttu-id="e5eae-123">**чекквиртуалсистемисмигратаблетохост**</span><span class="sxs-lookup"><span data-stu-id="e5eae-123">**CheckVirtualSystemIsMigratableToHost**</span></span>](checkvirtualsystemismigratabletohost-msvm-virtualsystemmigrationservice.md) | <span data-ttu-id="e5eae-124">Определяет, можно ли перенести указанную виртуальную систему на целевой узел, заданный сетевым именем или IP-адресом.</span><span class="sxs-lookup"><span data-stu-id="e5eae-124">Determines whether the specified virtual system can be migrated to a target host specified by a network name or IP address.</span></span><br/>                                       |
| [<span data-ttu-id="e5eae-125">**жетсистемкомпатибилитинфо**</span><span class="sxs-lookup"><span data-stu-id="e5eae-125">**GetSystemCompatibilityInfo**</span></span>](getsystemcompatibilityinfo-msvm-virtualsystemmigrationservice.md)                     | <span data-ttu-id="e5eae-126">Создает непрозрачный большой двоичный объект данных, содержащий сведения о совместимости для указанной системы.</span><span class="sxs-lookup"><span data-stu-id="e5eae-126">Generates an opaque blob of data that contains compatibility information for the specified system.</span></span><br/>                                                                |
| [<span data-ttu-id="e5eae-127">**жетсистемкомпатибилитивекторс**</span><span class="sxs-lookup"><span data-stu-id="e5eae-127">**GetSystemCompatibilityVectors**</span></span>](getsystemcompatibilityvectors-msvm-virtualsystemmigrationservice.md)               | <span data-ttu-id="e5eae-128">Возвращает векторы совместимости для виртуальной машины или узла.</span><span class="sxs-lookup"><span data-stu-id="e5eae-128">Gets compatibility vectors for a virtual machine or a host.</span></span><br/> <span data-ttu-id="e5eae-129">**Windows 8.1:** Это значение не поддерживается до Windows 8.1 и Windows Server 2012 R2.</span><span class="sxs-lookup"><span data-stu-id="e5eae-129">**Windows 8.1:** This value is not supported until Windows 8.1 and Windows Server 2012 R2.</span></span><br/> |
| [<span data-ttu-id="e5eae-130">**мигратевиртуалсистемтохост**</span><span class="sxs-lookup"><span data-stu-id="e5eae-130">**MigrateVirtualSystemToHost**</span></span>](migratevirtualsystemtohost-msvm-virtualsystemmigrationservice.md)                     | <span data-ttu-id="e5eae-131">Переносит виртуальную систему или хранилище виртуальной системы на целевой узел, указанный именем узла.</span><span class="sxs-lookup"><span data-stu-id="e5eae-131">Migrates a virtual system or the storage of a virtual system to a destination host specified by a hostname.</span></span><br/>                                                       |
| [<span data-ttu-id="e5eae-132">**мигратевиртуалсистемтосистем**</span><span class="sxs-lookup"><span data-stu-id="e5eae-132">**MigrateVirtualSystemToSystem**</span></span>](migratevirtualsystemtosystem-msvm-virtualsystemmigrationservice.md)                 | <span data-ttu-id="e5eae-133">Перемещает или переносит виртуальную систему в целевую систему.</span><span class="sxs-lookup"><span data-stu-id="e5eae-133">Moves, migrates, or relocates a virtual system to a target system.</span></span><br/>                                                                                                |
| [<span data-ttu-id="e5eae-134">**модифинетворксеттингс**</span><span class="sxs-lookup"><span data-stu-id="e5eae-134">**ModifyNetworkSettings**</span></span>](modifynetworksettings-msvm-virtualsystemmigrationservice.md)                               | <span data-ttu-id="e5eae-135">Изменяет сетевые подсети миграции для службы миграции виртуальной системы.</span><span class="sxs-lookup"><span data-stu-id="e5eae-135">Modifies migration network subnets of the virtual system migration service.</span></span><br/>                                                                                       |
| [<span data-ttu-id="e5eae-136">**модифисервицесеттингс**</span><span class="sxs-lookup"><span data-stu-id="e5eae-136">**ModifyServiceSettings**</span></span>](modifyservicesettings-msvm-virtualsystemmigrationservice.md)                               | <span data-ttu-id="e5eae-137">Изменяет данные настройки для службы миграции.</span><span class="sxs-lookup"><span data-stu-id="e5eae-137">Modifies the setting data for the migration service.</span></span><br/>                                                                                                              |
| [<span data-ttu-id="e5eae-138">**ремовенетворксеттингс**</span><span class="sxs-lookup"><span data-stu-id="e5eae-138">**RemoveNetworkSettings**</span></span>](removenetworksettings-msvm-virtualsystemmigrationservice.md)                               | <span data-ttu-id="e5eae-139">Удаляет подсети миграции из службы миграции виртуальной системы.</span><span class="sxs-lookup"><span data-stu-id="e5eae-139">Removes migration network subnets from the virtual system migration service.</span></span><br/>                                                                                      |
| [<span data-ttu-id="e5eae-140">**Равен**</span><span class="sxs-lookup"><span data-stu-id="e5eae-140">**RequestStateChange**</span></span>](msvm-virtualsystemmigrationservice-requeststatechange.md)                                     | <span data-ttu-id="e5eae-141">Запрашивает изменение состояния</span><span class="sxs-lookup"><span data-stu-id="e5eae-141">Requests a state change</span></span><br/>                                                                                                                                           |
| [<span data-ttu-id="e5eae-142">**StartService**</span><span class="sxs-lookup"><span data-stu-id="e5eae-142">**StartService**</span></span>](msvm-virtualsystemmigrationservice-startservice.md)                                                 | <span data-ttu-id="e5eae-143">запускает службу.</span><span class="sxs-lookup"><span data-stu-id="e5eae-143">Starts the service.</span></span><br/>                                                                                                                                               |
| [<span data-ttu-id="e5eae-144">**StopService**</span><span class="sxs-lookup"><span data-stu-id="e5eae-144">**StopService**</span></span>](msvm-virtualsystemmigrationservice-stopservice.md)                                                   | <span data-ttu-id="e5eae-145">останавливает службу.</span><span class="sxs-lookup"><span data-stu-id="e5eae-145">Stops the service.</span></span><br/>                                                                                                                                                |



 

### <a name="properties"></a><span data-ttu-id="e5eae-146">Свойства</span><span class="sxs-lookup"><span data-stu-id="e5eae-146">Properties</span></span>

<span data-ttu-id="e5eae-147">Класс **мсвм \_ виртуалсистеммигратионсервице** имеет следующие свойства.</span><span class="sxs-lookup"><span data-stu-id="e5eae-147">The **Msvm\_VirtualSystemMigrationService** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="e5eae-148">**активесторажемигратионкаунт**</span><span class="sxs-lookup"><span data-stu-id="e5eae-148">**ActiveStorageMigrationCount**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e5eae-149">Тип данных: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="e5eae-149">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="e5eae-150">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="e5eae-150">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="e5eae-151">Текущее количество выполняющихся миграций хранилища.</span><span class="sxs-lookup"><span data-stu-id="e5eae-151">The number of current storage migrations in progress.</span></span>

</dd> <dt>

<span data-ttu-id="e5eae-152">**активевиртуалсистеммигратионкаунт**</span><span class="sxs-lookup"><span data-stu-id="e5eae-152">**ActiveVirtualSystemMigrationCount**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e5eae-153">Тип данных: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="e5eae-153">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="e5eae-154">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="e5eae-154">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="e5eae-155">Число текущих миграций виртуальной системы.</span><span class="sxs-lookup"><span data-stu-id="e5eae-155">The number of current virtual system migrations in progress.</span></span>

</dd> <dt>

<span data-ttu-id="e5eae-156">**аваилаблерекуестедстатес**</span><span class="sxs-lookup"><span data-stu-id="e5eae-156">**AvailableRequestedStates**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e5eae-157">Тип данных: **UInt16** , массив</span><span class="sxs-lookup"><span data-stu-id="e5eae-157">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="e5eae-158">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="e5eae-158">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="e5eae-159">Указывает возможные значения для параметра *RequestedState* метода **RequestStateChange** .</span><span class="sxs-lookup"><span data-stu-id="e5eae-159">Indicates the possible values for the *RequestedState* parameter of the **RequestStateChange** method.</span></span> <span data-ttu-id="e5eae-160">Это свойство наследуется от [**CIM \_ енабледлогикалелемент**](/previous-versions//cc136818(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="e5eae-160">This property is inherited from [**CIM\_EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)).</span></span>

</dd> <dt>

<span data-ttu-id="e5eae-161">**Заголовок**</span><span class="sxs-lookup"><span data-stu-id="e5eae-161">**Caption**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e5eae-162">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="e5eae-162">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="e5eae-163">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="e5eae-163">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="e5eae-164">Краткое описание объекта.</span><span class="sxs-lookup"><span data-stu-id="e5eae-164">A short description of the object.</span></span> <span data-ttu-id="e5eae-165">Это свойство наследуется от [**CIM \_ манажеделемент**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement)и всегда имеет значение "Служба миграции Hyper-V".</span><span class="sxs-lookup"><span data-stu-id="e5eae-165">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement), and it is always set to "Hyper-V Migration Service".</span></span>

</dd> <dt>

<span data-ttu-id="e5eae-166">**коммуникатионстатус**</span><span class="sxs-lookup"><span data-stu-id="e5eae-166">**CommunicationStatus**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e5eae-167">Тип данных: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="e5eae-167">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="e5eae-168">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="e5eae-168">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="e5eae-169">Указывает способность инструментирования взаимодействовать с базовым управляемым элементом.</span><span class="sxs-lookup"><span data-stu-id="e5eae-169">Indicates the ability of the instrumentation to communicate with the underlying managed element.</span></span> <span data-ttu-id="e5eae-170">Значение **null** указывает, что это свойство не реализовано.</span><span class="sxs-lookup"><span data-stu-id="e5eae-170">A **Null** value indicates that this property is not implemented.</span></span> <span data-ttu-id="e5eae-171">Это свойство наследуется от [**CIM \_ манажедсистемелемент**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span><span class="sxs-lookup"><span data-stu-id="e5eae-171">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

</dd> <dt>

<span data-ttu-id="e5eae-172">**CreationClassName**</span><span class="sxs-lookup"><span data-stu-id="e5eae-172">**CreationClassName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e5eae-173">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="e5eae-173">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="e5eae-174">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="e5eae-174">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="e5eae-175">Имя класса или подкласса, используемого при создании экземпляра.</span><span class="sxs-lookup"><span data-stu-id="e5eae-175">The name of the class or subclass used in the creation of an instance.</span></span> <span data-ttu-id="e5eae-176">Это свойство наследуется [**от \_ службы CIM**](/windows/desktop/CIMWin32Prov/cim-service)и всегда имеет значение "мсвм \_ виртуалсистеммигратионсервице".</span><span class="sxs-lookup"><span data-stu-id="e5eae-176">This property is inherited from [**CIM\_Service**](/windows/desktop/CIMWin32Prov/cim-service), and it is always set to "Msvm\_VirtualSystemMigrationService".</span></span>

</dd> <dt>

<span data-ttu-id="e5eae-177">**Описание**</span><span class="sxs-lookup"><span data-stu-id="e5eae-177">**Description**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e5eae-178">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="e5eae-178">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="e5eae-179">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="e5eae-179">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="e5eae-180">Описание объекта.</span><span class="sxs-lookup"><span data-stu-id="e5eae-180">A description of the object.</span></span> <span data-ttu-id="e5eae-181">Это свойство наследуется от [**CIM \_ манажеделемент**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement)и всегда имеет значение "Служба миграции Hyper-V".</span><span class="sxs-lookup"><span data-stu-id="e5eae-181">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement), and it is always set to "Hyper-V Migration Service".</span></span>

</dd> <dt>

<span data-ttu-id="e5eae-182">**DetailedStatus**</span><span class="sxs-lookup"><span data-stu-id="e5eae-182">**DetailedStatus**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e5eae-183">Тип данных: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="e5eae-183">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="e5eae-184">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="e5eae-184">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="e5eae-185">Дополняет свойство **примаристатус** дополнительными сведениями о состоянии.</span><span class="sxs-lookup"><span data-stu-id="e5eae-185">Compliments the **PrimaryStatus** property with additional status detail.</span></span> <span data-ttu-id="e5eae-186">Значение **null** указывает, что это свойство не реализовано.</span><span class="sxs-lookup"><span data-stu-id="e5eae-186">A **Null** value indicates that this property is not implemented.</span></span> <span data-ttu-id="e5eae-187">Это свойство наследуется от [**CIM \_ манажедсистемелемент**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span><span class="sxs-lookup"><span data-stu-id="e5eae-187">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

</dd> <dt>

<span data-ttu-id="e5eae-188">**ElementName**</span><span class="sxs-lookup"><span data-stu-id="e5eae-188">**ElementName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e5eae-189">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="e5eae-189">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="e5eae-190">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="e5eae-190">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="e5eae-191">Отображаемое имя объекта.</span><span class="sxs-lookup"><span data-stu-id="e5eae-191">A display name for the object.</span></span> <span data-ttu-id="e5eae-192">Это свойство наследуется от [**CIM \_ манажеделемент**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement)и всегда имеет значение "Служба миграции Hyper-V".</span><span class="sxs-lookup"><span data-stu-id="e5eae-192">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement), and it is always set to "Hyper-V Migration Service".</span></span>

</dd> <dt>

<span data-ttu-id="e5eae-193">**енабледдефаулт**</span><span class="sxs-lookup"><span data-stu-id="e5eae-193">**EnabledDefault**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e5eae-194">Тип данных: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="e5eae-194">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="e5eae-195">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="e5eae-195">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="e5eae-196">Конфигурация по умолчанию или запуска администратора для включенного состояния элемента.</span><span class="sxs-lookup"><span data-stu-id="e5eae-196">An administrator's default or startup configuration for the enabled state of an element.</span></span> <span data-ttu-id="e5eae-197">Это свойство наследуется от [**CIM \_ енабледлогикалелемент**](/previous-versions//cc136818(v=vs.85))и всегда имеет значение 2 (включено).</span><span class="sxs-lookup"><span data-stu-id="e5eae-197">This property is inherited from [**CIM\_EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)), and it is always set to 2 (Enabled).</span></span>

</dd> <dt>

<span data-ttu-id="e5eae-198">**EnabledState**</span><span class="sxs-lookup"><span data-stu-id="e5eae-198">**EnabledState**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e5eae-199">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="e5eae-199">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="e5eae-200">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="e5eae-200">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="e5eae-201">Включенные и отключенные состояния элемента.</span><span class="sxs-lookup"><span data-stu-id="e5eae-201">The enabled and disabled states of an element.</span></span> <span data-ttu-id="e5eae-202">Это свойство также может указывать переходы между этими запрошенными состояниями.</span><span class="sxs-lookup"><span data-stu-id="e5eae-202">This property can also indicate the transitions between these requested states.</span></span> <span data-ttu-id="e5eae-203">Это свойство наследуется от [**CIM \_ енабледлогикалелемент**](/previous-versions//cc136818(v=vs.85))и всегда имеет значение 2 (включено).</span><span class="sxs-lookup"><span data-stu-id="e5eae-203">This property is inherited from [**CIM\_EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)), and it is always set to 2 (Enabled).</span></span>

</dd> <dt>

<span data-ttu-id="e5eae-204">**HealthState**</span><span class="sxs-lookup"><span data-stu-id="e5eae-204">**HealthState**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e5eae-205">Тип данных: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="e5eae-205">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="e5eae-206">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="e5eae-206">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="e5eae-207">Текущая работоспособность элемента.</span><span class="sxs-lookup"><span data-stu-id="e5eae-207">The current health of the element.</span></span> <span data-ttu-id="e5eae-208">Этот атрибут выражает работоспособность этого элемента, но не обязательно для его подкомпонентов.</span><span class="sxs-lookup"><span data-stu-id="e5eae-208">This attribute expresses the health of this element but not necessarily that of its subcomponents.</span></span> <span data-ttu-id="e5eae-209">Возможные значения: от 0 до 30, где 5 означает, что элемент полностью работоспособен, а 30 означает, что элемент полностью нефункциональный.</span><span class="sxs-lookup"><span data-stu-id="e5eae-209">The possible values are 0 to 30, where 5 means the element is entirely healthy and 30 means the element is completely nonfunctional.</span></span> <span data-ttu-id="e5eae-210">Это свойство наследуется от [**CIM \_ манажедсистемелемент**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement)и всегда имеет значение 5 (ОК).</span><span class="sxs-lookup"><span data-stu-id="e5eae-210">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement), and it is always set to 5 (OK).</span></span>

</dd> <dt>

<span data-ttu-id="e5eae-211">**InstallDate**</span><span class="sxs-lookup"><span data-stu-id="e5eae-211">**InstallDate**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e5eae-212">Тип данных: **DateTime**</span><span class="sxs-lookup"><span data-stu-id="e5eae-212">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="e5eae-213">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="e5eae-213">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="e5eae-214">Дата и время создания конфигурации виртуальной машины.</span><span class="sxs-lookup"><span data-stu-id="e5eae-214">The date and time the virtual machine configuration was created.</span></span> <span data-ttu-id="e5eae-215">Это свойство наследуется от [**CIM \_ манажедсистемелемент**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span><span class="sxs-lookup"><span data-stu-id="e5eae-215">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

</dd> <dt>

<span data-ttu-id="e5eae-216">**InstanceID**</span><span class="sxs-lookup"><span data-stu-id="e5eae-216">**InstanceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e5eae-217">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="e5eae-217">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="e5eae-218">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="e5eae-218">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="e5eae-219">Квалификаторы: **ключ**</span><span class="sxs-lookup"><span data-stu-id="e5eae-219">Qualifiers: **Key**</span></span>
</dt> </dl>

<span data-ttu-id="e5eae-220">Уникально идентифицирует экземпляр этого класса.</span><span class="sxs-lookup"><span data-stu-id="e5eae-220">Uniquely identifies an instance of this class.</span></span> <span data-ttu-id="e5eae-221">Это свойство наследуется от [**CIM \_ манажеделемент**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement)и всегда имеет значение **null**.</span><span class="sxs-lookup"><span data-stu-id="e5eae-221">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement), and it is always set to **Null**.</span></span>

</dd> <dt>

<span data-ttu-id="e5eae-222">**мигратионсервицелистенерипаддресслист**</span><span class="sxs-lookup"><span data-stu-id="e5eae-222">**MigrationServiceListenerIPAddressList**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e5eae-223">Тип данных: массив **строк**</span><span class="sxs-lookup"><span data-stu-id="e5eae-223">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="e5eae-224">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="e5eae-224">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="e5eae-225">Список IP-адресов узлов, которые можно использовать для миграции виртуальной системы.</span><span class="sxs-lookup"><span data-stu-id="e5eae-225">The list of host IP addresses that can be used for virtual system migration.</span></span>

</dd> <dt>

<span data-ttu-id="e5eae-226">**Name**</span><span class="sxs-lookup"><span data-stu-id="e5eae-226">**Name**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e5eae-227">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="e5eae-227">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="e5eae-228">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="e5eae-228">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="e5eae-229">Метка, по которой известен объект.</span><span class="sxs-lookup"><span data-stu-id="e5eae-229">The label by which the object is known.</span></span> <span data-ttu-id="e5eae-230">Это свойство наследуется [**от \_ службы CIM**](/windows/desktop/CIMWin32Prov/cim-service)и всегда имеет значение "мигратионвми".</span><span class="sxs-lookup"><span data-stu-id="e5eae-230">This property is inherited from [**CIM\_Service**](/windows/desktop/CIMWin32Prov/cim-service), and it is always set to "migrationwmi".</span></span>

</dd> <dt>

<span data-ttu-id="e5eae-231">**оператингстатус**</span><span class="sxs-lookup"><span data-stu-id="e5eae-231">**OperatingStatus**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e5eae-232">Тип данных: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="e5eae-232">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="e5eae-233">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="e5eae-233">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="e5eae-234">Предоставляет сведения о текущем состоянии для рабочего условия элемента и может использоваться для предоставления более подробных сведений относительно значения свойства **EnabledState** .</span><span class="sxs-lookup"><span data-stu-id="e5eae-234">Provides current status information for the operational condition of the element and can be used for providing more detail with respect to the value of the **EnabledState** property.</span></span> <span data-ttu-id="e5eae-235">Значение **null** указывает, что это свойство не реализовано.</span><span class="sxs-lookup"><span data-stu-id="e5eae-235">A **Null** value indicates that this property is not implemented.</span></span> <span data-ttu-id="e5eae-236">Это свойство наследуется от [**CIM \_ манажедсистемелемент**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span><span class="sxs-lookup"><span data-stu-id="e5eae-236">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

</dd> <dt>

<span data-ttu-id="e5eae-237">**OperationalStatus**</span><span class="sxs-lookup"><span data-stu-id="e5eae-237">**OperationalStatus**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e5eae-238">Тип данных: **UInt16** , массив</span><span class="sxs-lookup"><span data-stu-id="e5eae-238">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="e5eae-239">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="e5eae-239">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="e5eae-240">Текущее состояние объекта.</span><span class="sxs-lookup"><span data-stu-id="e5eae-240">The current statuses of the object.</span></span> <span data-ttu-id="e5eae-241">Это свойство наследуется от [**CIM \_ манажедсистемелемент**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement), и каждый элемент массива всегда имеет значение 2 (ОК).</span><span class="sxs-lookup"><span data-stu-id="e5eae-241">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement), and each array element is always set to 2 (OK).</span></span>

</dd> <dt>

<span data-ttu-id="e5eae-242">**осеренабледстате**</span><span class="sxs-lookup"><span data-stu-id="e5eae-242">**OtherEnabledState**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e5eae-243">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="e5eae-243">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="e5eae-244">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="e5eae-244">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="e5eae-245">Строка, описывающая включенное или отключенное состояние элемента, если свойство **EnabledState** имеет значение 1 (другое).</span><span class="sxs-lookup"><span data-stu-id="e5eae-245">A string that describes the enabled or disabled state of the element when the **EnabledState** property is set to 1 (Other).</span></span> <span data-ttu-id="e5eae-246">Для этого свойства необходимо задать значение **null** , если параметр **EnabledState** имеет любое значение, отличное от 1.</span><span class="sxs-lookup"><span data-stu-id="e5eae-246">This property must be set to **Null** when **EnabledState** is any value other than 1.</span></span> <span data-ttu-id="e5eae-247">Это свойство наследуется от [**CIM \_ енабледлогикалелемент**](/previous-versions//cc136818(v=vs.85))и всегда имеет значение **null**.</span><span class="sxs-lookup"><span data-stu-id="e5eae-247">This property is inherited from [**CIM\_EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)), and it is always set to **Null**.</span></span>

</dd> <dt>

<span data-ttu-id="e5eae-248">**примарйовнерконтакт**</span><span class="sxs-lookup"><span data-stu-id="e5eae-248">**PrimaryOwnerContact**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e5eae-249">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="e5eae-249">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="e5eae-250">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="e5eae-250">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="e5eae-251">Значение, которое предоставляет сведения о том, как можно достичь основного владельца службы (например, номер телефона, адрес электронной почты и т. д.).</span><span class="sxs-lookup"><span data-stu-id="e5eae-251">A value that provides information about how the primary owner of the service can be reached (for example, phone number, email address, and so on).</span></span> <span data-ttu-id="e5eae-252">Это свойство наследуется [**от \_ службы CIM**](/windows/desktop/CIMWin32Prov/cim-service)и всегда имеет значение **null**.</span><span class="sxs-lookup"><span data-stu-id="e5eae-252">This property is inherited from [**CIM\_Service**](/windows/desktop/CIMWin32Prov/cim-service), and it is always set to **Null**.</span></span>

</dd> <dt>

<span data-ttu-id="e5eae-253">**примарйовнернаме**</span><span class="sxs-lookup"><span data-stu-id="e5eae-253">**PrimaryOwnerName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e5eae-254">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="e5eae-254">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="e5eae-255">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="e5eae-255">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="e5eae-256">Имя основного владельца службы, если она определена.</span><span class="sxs-lookup"><span data-stu-id="e5eae-256">The name of the primary owner for the service, if one is defined.</span></span> <span data-ttu-id="e5eae-257">Первичный владелец — это первоначальный контактный контакт для службы поддержки.</span><span class="sxs-lookup"><span data-stu-id="e5eae-257">The primary owner is the initial support contact for the service.</span></span> <span data-ttu-id="e5eae-258">Это свойство наследуется [**от \_ службы CIM**](/windows/desktop/CIMWin32Prov/cim-service)и всегда имеет значение **null**.</span><span class="sxs-lookup"><span data-stu-id="e5eae-258">This property is inherited from [**CIM\_Service**](/windows/desktop/CIMWin32Prov/cim-service), and it is always set to **Null**.</span></span>

</dd> <dt>

<span data-ttu-id="e5eae-259">**примаристатус**</span><span class="sxs-lookup"><span data-stu-id="e5eae-259">**PrimaryStatus**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e5eae-260">Тип данных: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="e5eae-260">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="e5eae-261">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="e5eae-261">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="e5eae-262">Предоставляет сведения о состоянии высокого уровня.</span><span class="sxs-lookup"><span data-stu-id="e5eae-262">Provides high level status information.</span></span> <span data-ttu-id="e5eae-263">Это свойство следует использовать вместе со свойством **детаиледстатус** , чтобы обеспечить высокий уровень и подробные сведения о состоянии работоспособности элемента и его подкомпонентов.</span><span class="sxs-lookup"><span data-stu-id="e5eae-263">This property should be used in conjunction with the **DetailedStatus** property to provide high level and detailed health status of the element and its subcomponents.</span></span> <span data-ttu-id="e5eae-264">Значение **null** указывает, что это свойство не реализовано.</span><span class="sxs-lookup"><span data-stu-id="e5eae-264">A **Null** value indicates that this property is not implemented.</span></span> <span data-ttu-id="e5eae-265">Это свойство наследуется от [**CIM \_ манажедсистемелемент**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span><span class="sxs-lookup"><span data-stu-id="e5eae-265">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

</dd> <dt>

<span data-ttu-id="e5eae-266">**RequestedState**</span><span class="sxs-lookup"><span data-stu-id="e5eae-266">**RequestedState**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e5eae-267">Тип данных: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="e5eae-267">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="e5eae-268">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="e5eae-268">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="e5eae-269">Последнее запрошенное или требуемое состояние элемента.</span><span class="sxs-lookup"><span data-stu-id="e5eae-269">The last requested or desired state for the element.</span></span> <span data-ttu-id="e5eae-270">Фактическое состояние элемента представлено параметром **EnabledState**.</span><span class="sxs-lookup"><span data-stu-id="e5eae-270">The actual state of the element is represented by **EnabledState**.</span></span> <span data-ttu-id="e5eae-271">Это свойство предназначено для сравнения последнего запрошенного и текущего включенного или отключенного состояния.</span><span class="sxs-lookup"><span data-stu-id="e5eae-271">This property is provided to compare the last requested and current enabled or disabled states.</span></span> <span data-ttu-id="e5eae-272">Конкретный экземпляр [**CIM \_ енабледлогикалелемент**](/previous-versions//cc136818(v=vs.85)) может не поддерживать метод **RequestStateChange** .</span><span class="sxs-lookup"><span data-stu-id="e5eae-272">A particular instance of [**CIM\_EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)) might not support the **RequestStateChange** method.</span></span> <span data-ttu-id="e5eae-273">В этом случае используется значение 12 (неприменимо).</span><span class="sxs-lookup"><span data-stu-id="e5eae-273">If this occurs, the value 12 (Not Applicable) is used.</span></span> <span data-ttu-id="e5eae-274">Это свойство наследуется от **CIM \_ енабледлогикалелемент** и всегда имеет значение 12 (неприменимо).</span><span class="sxs-lookup"><span data-stu-id="e5eae-274">This property is inherited from **CIM\_EnabledLogicalElement**, and it is always set to 12 (Not Applicable).</span></span>

</dd> <dt>

<span data-ttu-id="e5eae-275">**Запуск**</span><span class="sxs-lookup"><span data-stu-id="e5eae-275">**Started**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e5eae-276">Тип данных: **логический**</span><span class="sxs-lookup"><span data-stu-id="e5eae-276">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="e5eae-277">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="e5eae-277">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="e5eae-278">Указывает, запущена ли служба в данный момент.</span><span class="sxs-lookup"><span data-stu-id="e5eae-278">Indicates whether the service is currently running.</span></span> <span data-ttu-id="e5eae-279">Это свойство наследуется [**от \_ службы CIM**](/windows/desktop/CIMWin32Prov/cim-service).</span><span class="sxs-lookup"><span data-stu-id="e5eae-279">This property is inherited from [**CIM\_Service**](/windows/desktop/CIMWin32Prov/cim-service).</span></span>

</dd> <dt>

<span data-ttu-id="e5eae-280">**StartMode**</span><span class="sxs-lookup"><span data-stu-id="e5eae-280">**StartMode**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e5eae-281">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="e5eae-281">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="e5eae-282">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="e5eae-282">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="e5eae-283">Строковое значение, указывающее, запускается ли служба автоматически системой, операционной системой или запускается только по запросу.</span><span class="sxs-lookup"><span data-stu-id="e5eae-283">A string value that indicates whether the service is automatically started by a system, an operating system, or is started only upon request.</span></span> <span data-ttu-id="e5eae-284">Это свойство наследуется [**от \_ службы CIM**](/windows/desktop/CIMWin32Prov/cim-service)и всегда имеет значение **null**.</span><span class="sxs-lookup"><span data-stu-id="e5eae-284">This property is inherited from [**CIM\_Service**](/windows/desktop/CIMWin32Prov/cim-service), and it is always set to **Null**.</span></span>

</dd> <dt>

<span data-ttu-id="e5eae-285">**Состояние**</span><span class="sxs-lookup"><span data-stu-id="e5eae-285">**Status**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e5eae-286">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="e5eae-286">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="e5eae-287">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="e5eae-287">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="e5eae-288">Это свойство наследуется от [**CIM \_ манажедсистемелемент**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement)и всегда имеет значение "ОК".</span><span class="sxs-lookup"><span data-stu-id="e5eae-288">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement), and it is always set to "OK".</span></span>

</dd> <dt>

<span data-ttu-id="e5eae-289">**статусдескриптионс**</span><span class="sxs-lookup"><span data-stu-id="e5eae-289">**StatusDescriptions**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e5eae-290">Тип данных: массив **строк**</span><span class="sxs-lookup"><span data-stu-id="e5eae-290">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="e5eae-291">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="e5eae-291">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="e5eae-292">Строки, описывающие различные значения массива **OperationalStatus** .</span><span class="sxs-lookup"><span data-stu-id="e5eae-292">Strings that describe the various **OperationalStatus** array values.</span></span> <span data-ttu-id="e5eae-293">Это свойство наследуется от [**CIM \_ манажедсистемелемент**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement), а для строк всегда задано значение "ОК".</span><span class="sxs-lookup"><span data-stu-id="e5eae-293">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement), and the strings are always set to "OK".</span></span>

</dd> <dt>

<span data-ttu-id="e5eae-294">**системкреатионкласснаме**</span><span class="sxs-lookup"><span data-stu-id="e5eae-294">**SystemCreationClassName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e5eae-295">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="e5eae-295">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="e5eae-296">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="e5eae-296">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="e5eae-297">Имя класса создания системы области.</span><span class="sxs-lookup"><span data-stu-id="e5eae-297">The scoping system's creation class name.</span></span> <span data-ttu-id="e5eae-298">Это свойство наследуется [**от \_ службы CIM**](/windows/desktop/CIMWin32Prov/cim-service)и всегда имеет значение "мсвм \_ ComputerSystem".</span><span class="sxs-lookup"><span data-stu-id="e5eae-298">This property is inherited from [**CIM\_Service**](/windows/desktop/CIMWin32Prov/cim-service), and it is always set to "Msvm\_ComputerSystem".</span></span>

</dd> <dt>

<span data-ttu-id="e5eae-299">**SystemName**</span><span class="sxs-lookup"><span data-stu-id="e5eae-299">**SystemName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e5eae-300">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="e5eae-300">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="e5eae-301">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="e5eae-301">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="e5eae-302">Имя системы размещающего компьютера.</span><span class="sxs-lookup"><span data-stu-id="e5eae-302">The name of the hosting computer system.</span></span> <span data-ttu-id="e5eae-303">Это свойство наследуется [**от \_ службы CIM**](/windows/desktop/CIMWin32Prov/cim-service).</span><span class="sxs-lookup"><span data-stu-id="e5eae-303">This property is inherited from [**CIM\_Service**](/windows/desktop/CIMWin32Prov/cim-service).</span></span>

</dd> <dt>

<span data-ttu-id="e5eae-304">**тимеофластстатечанже**</span><span class="sxs-lookup"><span data-stu-id="e5eae-304">**TimeOfLastStateChange**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e5eae-305">Тип данных: **DateTime**</span><span class="sxs-lookup"><span data-stu-id="e5eae-305">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="e5eae-306">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="e5eae-306">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="e5eae-307">Дата или время последнего изменения включенного состояния элемента.</span><span class="sxs-lookup"><span data-stu-id="e5eae-307">The date or time when the enabled state of the element last changed.</span></span> <span data-ttu-id="e5eae-308">Это свойство наследуется от [**CIM \_ енабледлогикалелемент**](/previous-versions//cc136818(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="e5eae-308">This property is inherited from [**CIM\_EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)).</span></span>

</dd> <dt>

<span data-ttu-id="e5eae-309">**транситионингтостате**</span><span class="sxs-lookup"><span data-stu-id="e5eae-309">**TransitioningToState**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e5eae-310">Тип данных: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="e5eae-310">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="e5eae-311">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="e5eae-311">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="e5eae-312">Указывает целевое состояние, в которое переходит экземпляр.</span><span class="sxs-lookup"><span data-stu-id="e5eae-312">Indicates the target state to which the instance is transitioning.</span></span> <span data-ttu-id="e5eae-313">Это свойство наследуется от [**CIM \_ енабледлогикалелемент**](/previous-versions//cc136818(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="e5eae-313">This property is inherited from [**CIM\_EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)).</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="e5eae-314">Требования</span><span class="sxs-lookup"><span data-stu-id="e5eae-314">Requirements</span></span>



| <span data-ttu-id="e5eae-315">Требование</span><span class="sxs-lookup"><span data-stu-id="e5eae-315">Requirement</span></span> | <span data-ttu-id="e5eae-316">Значение</span><span class="sxs-lookup"><span data-stu-id="e5eae-316">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="e5eae-317">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="e5eae-317">Minimum supported client</span></span><br/> | <span data-ttu-id="e5eae-318">\[Только классические приложения Windows 8\]</span><span class="sxs-lookup"><span data-stu-id="e5eae-318">Windows 8 \[desktop apps only\]</span></span><br/>                                                              |
| <span data-ttu-id="e5eae-319">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="e5eae-319">Minimum supported server</span></span><br/> | <span data-ttu-id="e5eae-320">\[Только для настольных приложений Windows Server 2012\]</span><span class="sxs-lookup"><span data-stu-id="e5eae-320">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="e5eae-321">Пространство имен</span><span class="sxs-lookup"><span data-stu-id="e5eae-321">Namespace</span></span><br/>                | <span data-ttu-id="e5eae-322">Корневая \\ виртуализация \\ версии 2</span><span class="sxs-lookup"><span data-stu-id="e5eae-322">Root\\Virtualization\\V2</span></span><br/>                                                                     |
| <span data-ttu-id="e5eae-323">MOF</span><span class="sxs-lookup"><span data-stu-id="e5eae-323">MOF</span></span><br/>                      | <dl> <span data-ttu-id="e5eae-324"><dt>Виндовсвиртуализатион. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="e5eae-324"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="e5eae-325">DLL</span><span class="sxs-lookup"><span data-stu-id="e5eae-325">DLL</span></span><br/>                      | <dl> <span data-ttu-id="e5eae-326"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="e5eae-326"><dt>Vmms.exe</dt></span></span> </dl>                     |



 

