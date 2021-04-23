---
description: Представляет параметры виртуализации для виртуальной машины.
ms.assetid: BE81405E-E773-41CE-9441-33D60B63550E
title: Класс Msvm_VirtualSystemSettingData
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_VirtualSystemSettingData
- Msvm_VirtualSystemSettingData.InstanceID
- Msvm_VirtualSystemSettingData.Caption
- Msvm_VirtualSystemSettingData.Description
- Msvm_VirtualSystemSettingData.ElementName
- Msvm_VirtualSystemSettingData.VirtualSystemIdentifier
- Msvm_VirtualSystemSettingData.VirtualSystemType
- Msvm_VirtualSystemSettingData.Notes
- Msvm_VirtualSystemSettingData.CreationTime
- Msvm_VirtualSystemSettingData.ConfigurationID
- Msvm_VirtualSystemSettingData.ConfigurationDataRoot
- Msvm_VirtualSystemSettingData.ConfigurationFile
- Msvm_VirtualSystemSettingData.SnapshotDataRoot
- Msvm_VirtualSystemSettingData.SuspendDataRoot
- Msvm_VirtualSystemSettingData.SwapFileDataRoot
- Msvm_VirtualSystemSettingData.LogDataRoot
- Msvm_VirtualSystemSettingData.AutomaticStartupAction
- Msvm_VirtualSystemSettingData.AutomaticStartupActionDelay
- Msvm_VirtualSystemSettingData.AutomaticStartupActionSequenceNumber
- Msvm_VirtualSystemSettingData.AutomaticShutdownAction
- Msvm_VirtualSystemSettingData.AutomaticRecoveryAction
- Msvm_VirtualSystemSettingData.RecoveryFile
- Msvm_VirtualSystemSettingData.BIOSGUID
- Msvm_VirtualSystemSettingData.BIOSSerialNumber
- Msvm_VirtualSystemSettingData.BaseBoardSerialNumber
- Msvm_VirtualSystemSettingData.ChassisSerialNumber
- Msvm_VirtualSystemSettingData.Architecture
- Msvm_VirtualSystemSettingData.ChassisAssetTag
- Msvm_VirtualSystemSettingData.BIOSNumLock
- Msvm_VirtualSystemSettingData.BootOrder
- Msvm_VirtualSystemSettingData.Parent
- Msvm_VirtualSystemSettingData.UserSnapshotType
- Msvm_VirtualSystemSettingData.IsSaved
- Msvm_VirtualSystemSettingData.AdditionalRecoveryInformation
- Msvm_VirtualSystemSettingData.AllowFullSCSICommandSet
- Msvm_VirtualSystemSettingData.DebugChannelId
- Msvm_VirtualSystemSettingData.DebugPortEnabled
- Msvm_VirtualSystemSettingData.DebugPort
- Msvm_VirtualSystemSettingData.Version
- Msvm_VirtualSystemSettingData.IncrementalBackupEnabled
- Msvm_VirtualSystemSettingData.VirtualNumaEnabled
- Msvm_VirtualSystemSettingData.AllowReducedFcRedundancy
- Msvm_VirtualSystemSettingData.VirtualSystemSubType
- Msvm_VirtualSystemSettingData.BootSourceOrder
- Msvm_VirtualSystemSettingData.PauseAfterBootFailure
- Msvm_VirtualSystemSettingData.NetworkBootPreferredProtocol
- Msvm_VirtualSystemSettingData.GuestControlledCacheTypes
- Msvm_VirtualSystemSettingData.AutomaticSnapshotsEnabled
- Msvm_VirtualSystemSettingData.IsAutomaticSnapshot
- Msvm_VirtualSystemSettingData.GuestStateFile
- Msvm_VirtualSystemSettingData.GuestStateDataRoot
- Msvm_VirtualSystemSettingData.LockOnDisconnect
- Msvm_VirtualSystemSettingData.ParentPackage
- Msvm_VirtualSystemSettingData.AutomaticCriticalErrorActionTimeout
- Msvm_VirtualSystemSettingData.AutomaticCriticalErrorAction
- Msvm_VirtualSystemSettingData.ConsoleMode
- Msvm_VirtualSystemSettingData.SecureBootEnabled
- Msvm_VirtualSystemSettingData.SecureBootTemplateId
- Msvm_VirtualSystemSettingData.LowMmioGapSize
- Msvm_VirtualSystemSettingData.HighMmioGapSize
- Msvm_VirtualSystemSettingData.EnhancedSessionTransportType
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: 2787abbacfe4220b135544eecd3aeb7e86596c81
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "103990928"
---
# <a name="msvm_virtualsystemsettingdata-class"></a><span data-ttu-id="be8cd-103">\_Класс мсвм виртуалсистемсеттингдата</span><span class="sxs-lookup"><span data-stu-id="be8cd-103">Msvm\_VirtualSystemSettingData class</span></span>

<span data-ttu-id="be8cd-104">Представляет параметры виртуализации для виртуальной машины.</span><span class="sxs-lookup"><span data-stu-id="be8cd-104">Represents the virtualization-specific settings for a virtual machine.</span></span>

<span data-ttu-id="be8cd-105">Следующий синтаксис является упрощенным MOF-файлным (MOF) кодом и включает все наследуемые свойства.</span><span class="sxs-lookup"><span data-stu-id="be8cd-105">The following syntax is simplified Managed Object Format (MOF) code, and it includes all of the inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="be8cd-106">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="be8cd-106">Syntax</span></span>

``` syntax
[Dynamic, Provider("VmmsWmiInstanceAndMethodProvider"), AMENDMENT]
class Msvm_VirtualSystemSettingData : CIM_VirtualSystemSettingData
{
  string   InstanceID;
  string   Caption = "Virtual Machine Settings";
  string   Description;
  string   ElementName;
  string   VirtualSystemIdentifier;
  string   VirtualSystemType;
  string   Notes[];
  datetime CreationTime;
  string   ConfigurationID;
  string   ConfigurationDataRoot;
  string   ConfigurationFile;
  string   SnapshotDataRoot;
  string   SuspendDataRoot;
  string   SwapFileDataRoot;
  string   LogDataRoot;
  uint16   AutomaticStartupAction;
  datetime AutomaticStartupActionDelay;
  uint16   AutomaticStartupActionSequenceNumber;
  uint16   AutomaticShutdownAction;
  uint16   AutomaticRecoveryAction;
  string   RecoveryFile;
  string   BIOSGUID;
  string   BIOSSerialNumber;
  string   BaseBoardSerialNumber;
  string   ChassisSerialNumber;
  string   Architecture;
  string   ChassisAssetTag;
  boolean  BIOSNumLock;
  uint16   BootOrder[];
  string   Parent;
  uint16   UserSnapshotType;
  boolean  IsSaved;
  string   AdditionalRecoveryInformation;
  boolean  AllowFullSCSICommandSet;
  uint32   DebugChannelId;
  uint16   DebugPortEnabled;
  uint32   DebugPort;
  string   Version;
  boolean  IncrementalBackupEnabled;
  boolean  VirtualNumaEnabled;
  boolean  AllowReducedFcRedundancy = False;
  string   VirtualSystemSubType;
  string   BootSourceOrder[];
  boolean  PauseAfterBootFailure;
  uint16   NetworkBootPreferredProtocol;
  boolean  GuestControlledCacheTypes;
  boolean  AutomaticSnapshotsEnabled;
  boolean  IsAutomaticSnapshot;
  string   GuestStateFile;
  string   GuestStateDataRoot;
  boolean  LockOnDisconnect;
  string   ParentPackage;
  datetime AutomaticCriticalErrorActionTimeout;
  uint16   AutomaticCriticalErrorAction;
  uint16   ConsoleMode;
  boolean  SecureBootEnabled;
  string   SecureBootTemplateId;
  uint64   LowMmioGapSize;
  uint64   HighMmioGapSize;
  uint16   EnhancedSessionTransportType;
};
```

## <a name="members"></a><span data-ttu-id="be8cd-107">Члены</span><span class="sxs-lookup"><span data-stu-id="be8cd-107">Members</span></span>

<span data-ttu-id="be8cd-108">Класс **мсвм \_ виртуалсистемсеттингдата** имеет следующие типы членов:</span><span class="sxs-lookup"><span data-stu-id="be8cd-108">The **Msvm\_VirtualSystemSettingData** class has these types of members:</span></span>

-   [<span data-ttu-id="be8cd-109">Свойства</span><span class="sxs-lookup"><span data-stu-id="be8cd-109">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="be8cd-110">Свойства</span><span class="sxs-lookup"><span data-stu-id="be8cd-110">Properties</span></span>

<span data-ttu-id="be8cd-111">Класс **мсвм \_ виртуалсистемсеттингдата** имеет следующие свойства.</span><span class="sxs-lookup"><span data-stu-id="be8cd-111">The **Msvm\_VirtualSystemSettingData** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="be8cd-112">**аддитионалрековеринформатион**</span><span class="sxs-lookup"><span data-stu-id="be8cd-112">**AdditionalRecoveryInformation**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="be8cd-113">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="be8cd-113">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="be8cd-114">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="be8cd-114">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="be8cd-115">Дополнительные сведения, предоставленные действию восстановления.</span><span class="sxs-lookup"><span data-stu-id="be8cd-115">Any additional information provided to the recovery action.</span></span> <span data-ttu-id="be8cd-116">Значение этого свойства определяется действием в **аутоматикрековеряктион**.</span><span class="sxs-lookup"><span data-stu-id="be8cd-116">The meaning of this property is defined by the action in **AutomaticRecoveryAction**.</span></span> <span data-ttu-id="be8cd-117">Если **аутоматикрековеряктион** равен 0 ("None") или 1 ("Restart"), это значение равно **null**.</span><span class="sxs-lookup"><span data-stu-id="be8cd-117">If **AutomaticRecoveryAction** is 0 ("None") or 1 ("Restart"), this value is **Null**.</span></span> <span data-ttu-id="be8cd-118">Если **аутоматикрековеряктион** имеет значение 2 ("вернуться к снимку"), это путь к объекту моментального снимка, который должен быть применен при сбое рабочего процесса виртуальной машины.</span><span class="sxs-lookup"><span data-stu-id="be8cd-118">If **AutomaticRecoveryAction** is 2 ("Revert to Snapshot"), this is the object path to a snapshot that should be applied on failure of the virtual machine worker process.</span></span>

</dd> <dt>

<span data-ttu-id="be8cd-119">**алловфуллсксикоммандсет**</span><span class="sxs-lookup"><span data-stu-id="be8cd-119">**AllowFullSCSICommandSet**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="be8cd-120">Тип данных: **логический**</span><span class="sxs-lookup"><span data-stu-id="be8cd-120">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="be8cd-121">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="be8cd-121">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="be8cd-122">**Значение true** , если команды SCSI из операционной системы на виртуальной машине передаются транзитным дискам. в противном случае — **значение false**.</span><span class="sxs-lookup"><span data-stu-id="be8cd-122">**True** if SCSI commands from the guest operating system are passed to pass-through disks; otherwise, **False**.</span></span> <span data-ttu-id="be8cd-123">Если задано **значение true**, команды SCSI, выдаваемые гостевой операционной системой для транзитных дисков, не фильтруются.</span><span class="sxs-lookup"><span data-stu-id="be8cd-123">If **True**, SCSI commands emitted by the guest operating system to pass-through disks are not filtered.</span></span> <span data-ttu-id="be8cd-124">Рекомендуется, чтобы фильтрация SCSI оставалась включенной для рабочих развертываний.</span><span class="sxs-lookup"><span data-stu-id="be8cd-124">We recommend that SCSI filtering remain enabled for production deployments.</span></span>

</dd> <dt>

<span data-ttu-id="be8cd-125">**алловредуцедфкредунданци**</span><span class="sxs-lookup"><span data-stu-id="be8cd-125">**AllowReducedFcRedundancy**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="be8cd-126">Тип данных: **логический**</span><span class="sxs-lookup"><span data-stu-id="be8cd-126">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="be8cd-127">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="be8cd-127">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="be8cd-128">Указывает, разрешена ли динамическая миграция виртуальной машины, настроенной с виртуальным Fibre Channelным адаптером, на конечный компьютер, на котором могут отсутствовать или уменьшаться пути к целевым устройствам Fibre Channel.</span><span class="sxs-lookup"><span data-stu-id="be8cd-128">Specifies whether live migration of a virtual machine that is configured with a virtual Fibre Channel adapter is allowed to a destination computer that may have no or reduced paths to the target Fibre Channel devices.</span></span> <span data-ttu-id="be8cd-129">Это свойство должно быть сброшено после динамической миграции.</span><span class="sxs-lookup"><span data-stu-id="be8cd-129">This property should be cleared after a live migration.</span></span>



| <span data-ttu-id="be8cd-130">Значение</span><span class="sxs-lookup"><span data-stu-id="be8cd-130">Value</span></span>                                                                            | <span data-ttu-id="be8cd-131">Значение</span><span class="sxs-lookup"><span data-stu-id="be8cd-131">Meaning</span></span>                                                                                                                                                                                                                                                |
|----------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="be8cd-132"><dt>False</dt></span><span class="sxs-lookup"><span data-stu-id="be8cd-132"><dt>False</dt></span></span> </dl> | <span data-ttu-id="be8cd-133">Невозможно выполнить динамическую миграцию виртуальной машины на целевой компьютер, который может не иметь или не уменьшить пути к целевому Fibre Channel устройствам.</span><span class="sxs-lookup"><span data-stu-id="be8cd-133">The virtual machine cannot be live migrated to a target computer that may have no or reduced paths to the target Fibre Channel devices.</span></span><br/>                                                                                                     |
| <dl> <span data-ttu-id="be8cd-134"><dt>True</dt></span><span class="sxs-lookup"><span data-stu-id="be8cd-134"><dt>True</dt></span></span> </dl>  | <span data-ttu-id="be8cd-135">Виртуальную машину можно динамически перенести на целевой компьютер, который может не иметь или не уменьшить пути к целевому Fibre Channel устройств.</span><span class="sxs-lookup"><span data-stu-id="be8cd-135">The virtual machine can be live migrated to a target computer that may have no or reduced paths to the target Fibre Channel devices.</span></span> <span data-ttu-id="be8cd-136">Гостевая операционная система может потерять возможность подключения к хранилищу и может вести себя непредсказуемым образом.</span><span class="sxs-lookup"><span data-stu-id="be8cd-136">The guest operating system may lose connectivity to storage and may behave in an unpredictable manner.</span></span><br/> |



 

</dd> <dt>

<span data-ttu-id="be8cd-137">**Архитектура**</span><span class="sxs-lookup"><span data-stu-id="be8cd-137">**Architecture**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="be8cd-138">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="be8cd-138">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="be8cd-139">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="be8cd-139">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="be8cd-140">Архитектура этой системы.</span><span class="sxs-lookup"><span data-stu-id="be8cd-140">The architecture of this system.</span></span>

> [!Note]  
> <span data-ttu-id="be8cd-141">Добавлено в Windows 10 версии 1709.</span><span class="sxs-lookup"><span data-stu-id="be8cd-141">Added in Windows 10, version 1709.</span></span>

 

<dt>

<span id="x64"></span><span id="X64"></span>

<span data-ttu-id="be8cd-142">**x64** ()</span><span class="sxs-lookup"><span data-stu-id="be8cd-142">**x64** ()</span></span>


</dt> <dd></dd> <dt>

<span id="arm64"></span><span id="ARM64"></span>

<span data-ttu-id="be8cd-143">**arm64** ()</span><span class="sxs-lookup"><span data-stu-id="be8cd-143">**arm64** ()</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="be8cd-144">**аутоматиккритикалеррорактион**</span><span class="sxs-lookup"><span data-stu-id="be8cd-144">**AutomaticCriticalErrorAction**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="be8cd-145">Тип данных: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="be8cd-145">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="be8cd-146">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="be8cd-146">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="be8cd-147">Определяет действие, выполняемое на виртуальной машине, когда происходит критическая ошибка, например Отключение хранилища.</span><span class="sxs-lookup"><span data-stu-id="be8cd-147">Identifies the action to be taken on VM, when a critical error happens, like storage disconnect.</span></span>

> [!Note]  
> <span data-ttu-id="be8cd-148">Добавлено в Windows 10 и Windows Server 2016.</span><span class="sxs-lookup"><span data-stu-id="be8cd-148">Added in Windows 10 and Windows Server 2016.</span></span>

 

<dt>

<span id="None"></span><span id="none"></span><span id="NONE"></span>

<span data-ttu-id="be8cd-149"><span id="None"></span><span id="none"></span><span id="NONE"></span>**Нет** (0)</span><span class="sxs-lookup"><span data-stu-id="be8cd-149"><span id="None"></span><span id="none"></span><span id="NONE"></span>**None** (0)</span></span>


</dt> <dd>

<span data-ttu-id="be8cd-150">Для критических ошибок не будет выполняться никаких действий.</span><span class="sxs-lookup"><span data-stu-id="be8cd-150">No specific action will be taken for critical error conditions.</span></span>

</dd> <dt>

<span id="Pause_Resume"></span><span id="pause_resume"></span><span id="PAUSE_RESUME"></span>

<span data-ttu-id="be8cd-151"><span id="Pause_Resume"></span><span id="pause_resume"></span><span id="PAUSE_RESUME"></span>**Приостановить возобновление** (1)</span><span class="sxs-lookup"><span data-stu-id="be8cd-151"><span id="Pause_Resume"></span><span id="pause_resume"></span><span id="PAUSE_RESUME"></span>**Pause Resume** (1)</span></span>


</dt> <dd>

<span data-ttu-id="be8cd-152">Вызывает приостановку и автоматическое возобновление работы виртуальной машины после устранения критической ошибки.</span><span class="sxs-lookup"><span data-stu-id="be8cd-152">Causes the VM to be paused and automatically resumed when the critical error condition is resolved.</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="be8cd-153">**аутоматиккритикалеррорактионтимеаут**</span><span class="sxs-lookup"><span data-stu-id="be8cd-153">**AutomaticCriticalErrorActionTimeout**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="be8cd-154">Тип данных: **DateTime**</span><span class="sxs-lookup"><span data-stu-id="be8cd-154">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="be8cd-155">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="be8cd-155">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="be8cd-156">Квалификаторы: [**подтип**](/windows/desktop/WmiSdk/standard-wmi-qualifiers) ("интервал")</span><span class="sxs-lookup"><span data-stu-id="be8cd-156">Qualifiers: [**SubType**](/windows/desktop/WmiSdk/standard-wmi-qualifiers) ("interval")</span></span>
</dt> </dl>

<span data-ttu-id="be8cd-157">Определяет максимальное время, в течение которого **аутоматиккритикалеррорактион** будет выполняться для устранения критической ошибки.</span><span class="sxs-lookup"><span data-stu-id="be8cd-157">Identifies the maximum duration for which the **AutomaticCriticalErrorAction** will be performed to resolve the critical error.</span></span> <span data-ttu-id="be8cd-158">Это применимо только в том случае, если значение свойства **аутоматиккритикалеррорактион** не равно 0 (нет).</span><span class="sxs-lookup"><span data-stu-id="be8cd-158">This is applicable only when the value of the **AutomaticCriticalErrorAction** property is not 0 (None).</span></span> <span data-ttu-id="be8cd-159">По истечении времени ожидания виртуальная машина будет выключена.</span><span class="sxs-lookup"><span data-stu-id="be8cd-159">Once the timeout expires, the VM will be powered off.</span></span> <span data-ttu-id="be8cd-160">Значение будет округляться в большую сторону до ближайшей минуты.</span><span class="sxs-lookup"><span data-stu-id="be8cd-160">The value will be rounded up to the nearest minute.</span></span> <span data-ttu-id="be8cd-161">Значение 0 означает, что виртуальная машина должна быть выключена немедленно при возникновении критической ошибки.</span><span class="sxs-lookup"><span data-stu-id="be8cd-161">A value of 0 implies that the VM should be powered off immediately when it encounters a critical error condition.</span></span>

> [!Note]  
> <span data-ttu-id="be8cd-162">Добавлено в Windows 10 и Windows Server 2016.</span><span class="sxs-lookup"><span data-stu-id="be8cd-162">Added in Windows 10 and Windows Server 2016.</span></span>

 

</dd> <dt>

<span data-ttu-id="be8cd-163">**аутоматикрековеряктион**</span><span class="sxs-lookup"><span data-stu-id="be8cd-163">**AutomaticRecoveryAction**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="be8cd-164">Тип данных: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="be8cd-164">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="be8cd-165">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="be8cd-165">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="be8cd-166">Действие, выполняемое для виртуальной машины при сбое программного обеспечения, выполняемого виртуальной машиной.</span><span class="sxs-lookup"><span data-stu-id="be8cd-166">Action to take for the virtual machine when the software executed by the virtual machine fails.</span></span> <span data-ttu-id="be8cd-167">Сбои в этом случае означают сбой, который обнаруживается платформой размещения, например условие состояния взаимоблокировки.</span><span class="sxs-lookup"><span data-stu-id="be8cd-167">Failures in this case means a failure that is detectable by the host platform, such as a noninterruptible wait state condition.</span></span> <span data-ttu-id="be8cd-168">Это свойство наследуется от [**CIM \_ виртуалсистемсеттингдата**](/previous-versions//cc136954(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="be8cd-168">This property is inherited from [**CIM\_VirtualSystemSettingData**](/previous-versions//cc136954(v=vs.85)).</span></span>

<span data-ttu-id="be8cd-169">Это может быть одно из следующих значений.</span><span class="sxs-lookup"><span data-stu-id="be8cd-169">This can be one of the following values.</span></span>



| <span data-ttu-id="be8cd-170">Значение</span><span class="sxs-lookup"><span data-stu-id="be8cd-170">Value</span></span>                                                                               | <span data-ttu-id="be8cd-171">Значение</span><span class="sxs-lookup"><span data-stu-id="be8cd-171">Meaning</span></span>                        |
|-------------------------------------------------------------------------------------|--------------------------------|
| <dl> <span data-ttu-id="be8cd-172"><dt>2</dt></span><span class="sxs-lookup"><span data-stu-id="be8cd-172"><dt>2</dt></span></span> </dl>        | <span data-ttu-id="be8cd-173">Нет.</span><span class="sxs-lookup"><span data-stu-id="be8cd-173">None.</span></span><br/>               |
| <dl> <span data-ttu-id="be8cd-174"><dt>3</dt></span><span class="sxs-lookup"><span data-stu-id="be8cd-174"><dt>3</dt></span></span> </dl>        | <span data-ttu-id="be8cd-175">Перезапуск.</span><span class="sxs-lookup"><span data-stu-id="be8cd-175">Restart.</span></span><br/>            |
| <dl> <span data-ttu-id="be8cd-176"><dt>4</dt></span><span class="sxs-lookup"><span data-stu-id="be8cd-176"><dt>4</dt></span></span> </dl>        | <span data-ttu-id="be8cd-177">Вернуться к моментальному снимку.</span><span class="sxs-lookup"><span data-stu-id="be8cd-177">Revert to snapshot.</span></span><br/> |
| <dl> <span data-ttu-id="be8cd-178"><dt>5.. 32768</dt></span><span class="sxs-lookup"><span data-stu-id="be8cd-178"><dt>5..32768</dt></span></span> </dl> | <span data-ttu-id="be8cd-179">Зарезервировано.</span><span class="sxs-lookup"><span data-stu-id="be8cd-179">Reserved.</span></span><br/>           |



 

</dd> <dt>

<span data-ttu-id="be8cd-180">**аутоматикшутдовнактион**</span><span class="sxs-lookup"><span data-stu-id="be8cd-180">**AutomaticShutdownAction**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="be8cd-181">Тип данных: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="be8cd-181">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="be8cd-182">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="be8cd-182">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="be8cd-183">Действие, выполняемое для виртуальной машины при завершении работы узла.</span><span class="sxs-lookup"><span data-stu-id="be8cd-183">Action to take for the virtual machine when the host is shut down.</span></span> <span data-ttu-id="be8cd-184">Это свойство наследуется от [**CIM \_ виртуалсистемсеттингдата**](/previous-versions//cc136954(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="be8cd-184">This property is inherited from [**CIM\_VirtualSystemSettingData**](/previous-versions//cc136954(v=vs.85)).</span></span>

<span data-ttu-id="be8cd-185">Это может быть одно из следующих значений.</span><span class="sxs-lookup"><span data-stu-id="be8cd-185">This can be one of the following values.</span></span>



| <span data-ttu-id="be8cd-186">Значение</span><span class="sxs-lookup"><span data-stu-id="be8cd-186">Value</span></span>                                                                               | <span data-ttu-id="be8cd-187">Значение</span><span class="sxs-lookup"><span data-stu-id="be8cd-187">Meaning</span></span>                |
|-------------------------------------------------------------------------------------|------------------------|
| <dl> <span data-ttu-id="be8cd-188"><dt>2</dt></span><span class="sxs-lookup"><span data-stu-id="be8cd-188"><dt>2</dt></span></span> </dl>        | <span data-ttu-id="be8cd-189">Отключить.</span><span class="sxs-lookup"><span data-stu-id="be8cd-189">Turn off.</span></span><br/>   |
| <dl> <span data-ttu-id="be8cd-190"><dt>3</dt></span><span class="sxs-lookup"><span data-stu-id="be8cd-190"><dt>3</dt></span></span> </dl>        | <span data-ttu-id="be8cd-191">Сохранить состояние.</span><span class="sxs-lookup"><span data-stu-id="be8cd-191">Save state.</span></span><br/> |
| <dl> <span data-ttu-id="be8cd-192"><dt>4</dt></span><span class="sxs-lookup"><span data-stu-id="be8cd-192"><dt>4</dt></span></span> </dl>        | <span data-ttu-id="be8cd-193">Завершение работы.</span><span class="sxs-lookup"><span data-stu-id="be8cd-193">Shutdown.</span></span><br/>   |
| <dl> <span data-ttu-id="be8cd-194"><dt>5.. 32768</dt></span><span class="sxs-lookup"><span data-stu-id="be8cd-194"><dt>5..32768</dt></span></span> </dl> | <span data-ttu-id="be8cd-195">Зарезервировано.</span><span class="sxs-lookup"><span data-stu-id="be8cd-195">Reserved.</span></span><br/>   |



 

</dd> <dt>

<span data-ttu-id="be8cd-196">**аутоматикснапшотсенаблед**</span><span class="sxs-lookup"><span data-stu-id="be8cd-196">**AutomaticSnapshotsEnabled**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="be8cd-197">Тип данных: **логический**</span><span class="sxs-lookup"><span data-stu-id="be8cd-197">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="be8cd-198">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="be8cd-198">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="be8cd-199">Указывает, включены ли Автоматические моментальные снимки для этой виртуальной машины.</span><span class="sxs-lookup"><span data-stu-id="be8cd-199">Indicates whether this virtual machine should have automatic snapshots enabled.</span></span>

> [!Note]  
> <span data-ttu-id="be8cd-200">Добавлено в Windows 10 версии 1709.</span><span class="sxs-lookup"><span data-stu-id="be8cd-200">Added in Windows 10, version 1709.</span></span>

 

</dd> <dt>

<span data-ttu-id="be8cd-201">**аутоматикстартупактион**</span><span class="sxs-lookup"><span data-stu-id="be8cd-201">**AutomaticStartupAction**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="be8cd-202">Тип данных: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="be8cd-202">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="be8cd-203">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="be8cd-203">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="be8cd-204">Действие, выполняемое для виртуальной машины при запуске узла.</span><span class="sxs-lookup"><span data-stu-id="be8cd-204">Action to take for the virtual machine when the host is started.</span></span> <span data-ttu-id="be8cd-205">Это свойство наследуется от [**CIM \_ виртуалсистемсеттингдата**](/previous-versions//cc136954(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="be8cd-205">This property is inherited from [**CIM\_VirtualSystemSettingData**](/previous-versions//cc136954(v=vs.85)).</span></span>

<span data-ttu-id="be8cd-206">Это может быть одно из следующих значений.</span><span class="sxs-lookup"><span data-stu-id="be8cd-206">This can be one of the following values.</span></span>



| <span data-ttu-id="be8cd-207">Значение</span><span class="sxs-lookup"><span data-stu-id="be8cd-207">Value</span></span>                                                                               | <span data-ttu-id="be8cd-208">Значение</span><span class="sxs-lookup"><span data-stu-id="be8cd-208">Meaning</span></span>                                  |
|-------------------------------------------------------------------------------------|------------------------------------------|
| <dl> <span data-ttu-id="be8cd-209"><dt>2</dt></span><span class="sxs-lookup"><span data-stu-id="be8cd-209"><dt>2</dt></span></span> </dl>        | <span data-ttu-id="be8cd-210">Нет.</span><span class="sxs-lookup"><span data-stu-id="be8cd-210">None.</span></span><br/>                         |
| <dl> <span data-ttu-id="be8cd-211"><dt>3</dt></span><span class="sxs-lookup"><span data-stu-id="be8cd-211"><dt>3</dt></span></span> </dl>        | <span data-ttu-id="be8cd-212">Перезапустить, если ранее он был активен.</span><span class="sxs-lookup"><span data-stu-id="be8cd-212">Restart if previously active.</span></span><br/> |
| <dl> <span data-ttu-id="be8cd-213"><dt>4</dt></span><span class="sxs-lookup"><span data-stu-id="be8cd-213"><dt>4</dt></span></span> </dl>        | <span data-ttu-id="be8cd-214">Всегда запускать.</span><span class="sxs-lookup"><span data-stu-id="be8cd-214">Always start.</span></span><br/>                 |
| <dl> <span data-ttu-id="be8cd-215"><dt>5.. 32768</dt></span><span class="sxs-lookup"><span data-stu-id="be8cd-215"><dt>5..32768</dt></span></span> </dl> | <span data-ttu-id="be8cd-216">Зарезервировано.</span><span class="sxs-lookup"><span data-stu-id="be8cd-216">Reserved.</span></span><br/>                     |



 

</dd> <dt>

<span data-ttu-id="be8cd-217">**аутоматикстартупактионделай**</span><span class="sxs-lookup"><span data-stu-id="be8cd-217">**AutomaticStartupActionDelay**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="be8cd-218">Тип данных: **DateTime**</span><span class="sxs-lookup"><span data-stu-id="be8cd-218">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="be8cd-219">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="be8cd-219">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="be8cd-220">Время задержки перед автоматическим запуском виртуальной машины.</span><span class="sxs-lookup"><span data-stu-id="be8cd-220">The delay time before the virtual machine is automatically started up.</span></span> <span data-ttu-id="be8cd-221">Это свойство наследуется от [**CIM \_ виртуалсистемсеттингдата**](/previous-versions//cc136954(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="be8cd-221">This property is inherited from [**CIM\_VirtualSystemSettingData**](/previous-versions//cc136954(v=vs.85)).</span></span>

</dd> <dt>

<span data-ttu-id="be8cd-222">**аутоматикстартупактионсекуенценумбер**</span><span class="sxs-lookup"><span data-stu-id="be8cd-222">**AutomaticStartupActionSequenceNumber**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="be8cd-223">Тип данных: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="be8cd-223">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="be8cd-224">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="be8cd-224">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="be8cd-225">Число, указывающее относительную последовательность активации виртуальной машины при запуске главной системы.</span><span class="sxs-lookup"><span data-stu-id="be8cd-225">A number that indicates the relative sequence of virtual machine activation when the host system is started.</span></span> <span data-ttu-id="be8cd-226">Меньшее значение указывает на более раннюю активацию.</span><span class="sxs-lookup"><span data-stu-id="be8cd-226">A lower number indicates earlier activation.</span></span> <span data-ttu-id="be8cd-227">Если одна или несколько конфигураций отображают одно и то же значение, последовательность зависит от реализации.</span><span class="sxs-lookup"><span data-stu-id="be8cd-227">If one or more configurations show the same value, the sequence is implementation dependent.</span></span> <span data-ttu-id="be8cd-228">Значение 0 указывает, что последовательность зависит от реализации.</span><span class="sxs-lookup"><span data-stu-id="be8cd-228">A value of 0 indicates that the sequence is implementation dependent.</span></span> <span data-ttu-id="be8cd-229">Это свойство наследуется от [**CIM \_ виртуалсистемсеттингдата**](/previous-versions//cc136954(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="be8cd-229">This property is inherited from [**CIM\_VirtualSystemSettingData**](/previous-versions//cc136954(v=vs.85)).</span></span>

</dd> <dt>

<span data-ttu-id="be8cd-230">**басебоардсериалнумбер**</span><span class="sxs-lookup"><span data-stu-id="be8cd-230">**BaseBoardSerialNumber**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="be8cd-231">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="be8cd-231">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="be8cd-232">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="be8cd-232">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="be8cd-233">Серийный номер основной платы для виртуальной машины.</span><span class="sxs-lookup"><span data-stu-id="be8cd-233">The serial number of the base board for the virtual machine.</span></span>

</dd> <dt>

<span data-ttu-id="be8cd-234">**биосгуид**</span><span class="sxs-lookup"><span data-stu-id="be8cd-234">**BIOSGUID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="be8cd-235">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="be8cd-235">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="be8cd-236">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="be8cd-236">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="be8cd-237">Глобальный уникальный идентификатор BIOS виртуальной машины.</span><span class="sxs-lookup"><span data-stu-id="be8cd-237">The globally unique identifier for the BIOS of the virtual machine.</span></span>

</dd> <dt>

<span data-ttu-id="be8cd-238">**биоснумлокк**</span><span class="sxs-lookup"><span data-stu-id="be8cd-238">**BIOSNumLock**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="be8cd-239">Тип данных: **логический**</span><span class="sxs-lookup"><span data-stu-id="be8cd-239">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="be8cd-240">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="be8cd-240">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="be8cd-241">**Значение true** , если параметр Num Lock установлен в значение on BIOS; **Значение false** , если BIOS имеет значение OFF для параметра Num Lock.</span><span class="sxs-lookup"><span data-stu-id="be8cd-241">**True** if the num lock key is set to on by the BIOS; **False** if the num lock key is set to off by the BIOS.</span></span>

</dd> <dt>

<span data-ttu-id="be8cd-242">**BIOSSerialNumber**</span><span class="sxs-lookup"><span data-stu-id="be8cd-242">**BIOSSerialNumber**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="be8cd-243">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="be8cd-243">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="be8cd-244">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="be8cd-244">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="be8cd-245">Серийный номер BIOS для виртуальной машины.</span><span class="sxs-lookup"><span data-stu-id="be8cd-245">The serial number of the BIOS for the virtual machine.</span></span>

</dd> <dt>

<span data-ttu-id="be8cd-246">**BootOrder**</span><span class="sxs-lookup"><span data-stu-id="be8cd-246">**BootOrder**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="be8cd-247">Тип данных: **UInt16** , массив</span><span class="sxs-lookup"><span data-stu-id="be8cd-247">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="be8cd-248">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="be8cd-248">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="be8cd-249">Квалификаторы: [**arrayType**](/windows/desktop/WmiSdk/standard-qualifiers) ("индексированный"), [**максимум**](/windows/desktop/WmiSdk/standard-qualifiers) (4)</span><span class="sxs-lookup"><span data-stu-id="be8cd-249">Qualifiers: [**ArrayType**](/windows/desktop/WmiSdk/standard-qualifiers) ("Indexed"), [**MAX**](/windows/desktop/WmiSdk/standard-qualifiers) (4)</span></span>
</dt> </dl>

<span data-ttu-id="be8cd-250">Порядок загрузки, заданный в BIOS виртуальной машины.</span><span class="sxs-lookup"><span data-stu-id="be8cd-250">The boot order set within the BIOS of the virtual machine.</span></span> <span data-ttu-id="be8cd-251">Это свойство представляет собой массив значений **BootOrder** \[ \] от 0 до **BootOrder** \[ 3 \] включительно, где каждое значение обозначает устройство для загрузки.</span><span class="sxs-lookup"><span data-stu-id="be8cd-251">This property is an array of values, **BootOrder**\[0\] through **BootOrder**\[3\], inclusive, where each value indicates a device to boot from.</span></span> <span data-ttu-id="be8cd-252">Каждое из 4 значений в массиве должно быть задано и не должно совпадать с другим значением в массиве.</span><span class="sxs-lookup"><span data-stu-id="be8cd-252">Each of the 4 values in the array must be set and must not be the same as another value in the array.</span></span> <span data-ttu-id="be8cd-253">Виртуальная машина сначала попытается загрузиться с устройства, указанного первым значением в массиве.</span><span class="sxs-lookup"><span data-stu-id="be8cd-253">The virtual machine will first attempt to boot from the device indicated by the first value within the array.</span></span> <span data-ttu-id="be8cd-254">Если это устройство не содержит загрузочный сектор, виртуальная машина попытается загрузиться со следующего устройства, указанного свойством **BootOrder** , и т. д.</span><span class="sxs-lookup"><span data-stu-id="be8cd-254">If that device does not contain a boot sector, the virtual machine will attempt to boot from the next device specified by the **BootOrder** property and so on.</span></span> <span data-ttu-id="be8cd-255">Если устройство, указанное в **BootOrder** , не содержит загрузочный сектор, виртуальная машина не сможет загрузиться.</span><span class="sxs-lookup"><span data-stu-id="be8cd-255">If no device specified within the **BootOrder** contains a boot sector the virtual machine will fail to boot.</span></span> <span data-ttu-id="be8cd-256">Значение по умолчанию для виртуальной машины — \[ 0, 1, 2, 3 \] .</span><span class="sxs-lookup"><span data-stu-id="be8cd-256">The default value for a virtual machine is \[0, 1, 2, 3\].</span></span>

<dt>

<span id="Floppy"></span><span id="floppy"></span><span id="FLOPPY"></span>

<span data-ttu-id="be8cd-257"><span id="Floppy"></span><span id="floppy"></span><span id="FLOPPY"></span>**Дискета** (0)</span><span class="sxs-lookup"><span data-stu-id="be8cd-257"><span id="Floppy"></span><span id="floppy"></span><span id="FLOPPY"></span>**Floppy** (0)</span></span>


</dt> <dd>

<span data-ttu-id="be8cd-258">Виртуальная машина будет пытаться загрузиться с гибкого диска в дисководе.</span><span class="sxs-lookup"><span data-stu-id="be8cd-258">The virtual machine will attempt to boot from the floppy disk within the floppy drive.</span></span>

</dd> <dt>

<span id="CD-ROM"></span><span id="cd-rom"></span>

<span data-ttu-id="be8cd-259"><span id="CD-ROM"></span><span id="cd-rom"></span>**Компакт-** диск (1)</span><span class="sxs-lookup"><span data-stu-id="be8cd-259"><span id="CD-ROM"></span><span id="cd-rom"></span>**CD-ROM** (1)</span></span>


</dt> <dd>

<span data-ttu-id="be8cd-260">Виртуальная машина будет пытаться загрузиться с первого компакт-или DVD-диска, найденного в загрузочном секторе.</span><span class="sxs-lookup"><span data-stu-id="be8cd-260">The virtual machine will attempt to boot from the first CD or DVD disk found with a boot sector.</span></span>

</dd> <dt>

<span id="IDE_Hard_Drive"></span><span id="ide_hard_drive"></span><span id="IDE_HARD_DRIVE"></span>

<span data-ttu-id="be8cd-261"><span id="IDE_Hard_Drive"></span><span id="ide_hard_drive"></span><span id="IDE_HARD_DRIVE"></span>**Жесткий диск IDE** (2)</span><span class="sxs-lookup"><span data-stu-id="be8cd-261"><span id="IDE_Hard_Drive"></span><span id="ide_hard_drive"></span><span id="IDE_HARD_DRIVE"></span>**IDE Hard Drive** (2)</span></span>


</dt> <dd>

<span data-ttu-id="be8cd-262">Виртуальная машина попытается выполнить загрузку с первого жесткого диска, найденного в загрузочном секторе.</span><span class="sxs-lookup"><span data-stu-id="be8cd-262">The virtual machine will attempt to boot from the first hard disk drive found with a boot sector.</span></span>

</dd> <dt>

<span id="PXE_Boot"></span><span id="pxe_boot"></span><span id="PXE_BOOT"></span>

<span data-ttu-id="be8cd-263"><span id="PXE_Boot"></span><span id="pxe_boot"></span><span id="PXE_BOOT"></span>**Загрузка PXE** (3)</span><span class="sxs-lookup"><span data-stu-id="be8cd-263"><span id="PXE_Boot"></span><span id="pxe_boot"></span><span id="PXE_BOOT"></span>**PXE Boot** (3)</span></span>


</dt> <dd>

<span data-ttu-id="be8cd-264">Виртуальная машина будет пытаться загрузить PXE из сети.</span><span class="sxs-lookup"><span data-stu-id="be8cd-264">The virtual machine will attempt to PXE boot from the network.</span></span>

</dd> <dt>

<span id="SCSI_Hard_Drive"></span><span id="scsi_hard_drive"></span><span id="SCSI_HARD_DRIVE"></span>

<span data-ttu-id="be8cd-265"><span id="SCSI_Hard_Drive"></span><span id="scsi_hard_drive"></span><span id="SCSI_HARD_DRIVE"></span>**Жесткий диск SCSI** (4)</span><span class="sxs-lookup"><span data-stu-id="be8cd-265"><span id="SCSI_Hard_Drive"></span><span id="scsi_hard_drive"></span><span id="SCSI_HARD_DRIVE"></span>**SCSI Hard Drive** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="Reserved"></span><span id="reserved"></span><span id="RESERVED"></span>

<span data-ttu-id="be8cd-266"><span id="Reserved"></span><span id="reserved"></span><span id="RESERVED"></span>**Зарезервировано** (5.. 65535)</span><span class="sxs-lookup"><span data-stu-id="be8cd-266"><span id="Reserved"></span><span id="reserved"></span><span id="RESERVED"></span>**Reserved** (5..65535)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="be8cd-267">**бутсаурцеордер**</span><span class="sxs-lookup"><span data-stu-id="be8cd-267">**BootSourceOrder**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="be8cd-268">Тип данных: массив **строк**</span><span class="sxs-lookup"><span data-stu-id="be8cd-268">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="be8cd-269">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="be8cd-269">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="be8cd-270">Исходный порядок загрузки для виртуальной машины.</span><span class="sxs-lookup"><span data-stu-id="be8cd-270">The boot source order for the virtual machine.</span></span>

<span data-ttu-id="be8cd-271">**Windows 8.1:** Это значение не поддерживается до Windows 8.1 и Windows Server 2012 R2.</span><span class="sxs-lookup"><span data-stu-id="be8cd-271">**Windows 8.1:** This value is not supported until Windows 8.1 and Windows Server 2012 R2.</span></span>

</dd> <dt>

<span data-ttu-id="be8cd-272">**Заголовок**</span><span class="sxs-lookup"><span data-stu-id="be8cd-272">**Caption**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="be8cd-273">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="be8cd-273">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="be8cd-274">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="be8cd-274">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="be8cd-275">Краткое описание объекта.</span><span class="sxs-lookup"><span data-stu-id="be8cd-275">A short description of the object.</span></span> <span data-ttu-id="be8cd-276">Это свойство наследуется от [**CIM \_ манажеделемент**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span><span class="sxs-lookup"><span data-stu-id="be8cd-276">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span></span>

</dd> <dt>

<span data-ttu-id="be8cd-277">**чассисассеттаг**</span><span class="sxs-lookup"><span data-stu-id="be8cd-277">**ChassisAssetTag**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="be8cd-278">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="be8cd-278">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="be8cd-279">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="be8cd-279">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="be8cd-280">Тег ресурса для корпуса виртуальной машины.</span><span class="sxs-lookup"><span data-stu-id="be8cd-280">The asset tag of the chassis for the virtual machine.</span></span>

</dd> <dt>

<span data-ttu-id="be8cd-281">**чассиссериалнумбер**</span><span class="sxs-lookup"><span data-stu-id="be8cd-281">**ChassisSerialNumber**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="be8cd-282">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="be8cd-282">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="be8cd-283">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="be8cd-283">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="be8cd-284">Серийный номер корпуса для виртуальной машины.</span><span class="sxs-lookup"><span data-stu-id="be8cd-284">The serial number of the chassis for the virtual machine.</span></span>

</dd> <dt>

<span data-ttu-id="be8cd-285">**конфигуратиондатарут**</span><span class="sxs-lookup"><span data-stu-id="be8cd-285">**ConfigurationDataRoot**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="be8cd-286">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="be8cd-286">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="be8cd-287">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="be8cd-287">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="be8cd-288">Путь к каталогу, в котором хранится информация о конфигурации виртуальной машины.</span><span class="sxs-lookup"><span data-stu-id="be8cd-288">The path of a directory where information about the virtual machine configuration is stored.</span></span> <span data-ttu-id="be8cd-289">Это свойство наследуется от [**CIM \_ виртуалсистемсеттингдата**](/previous-versions//cc136954(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="be8cd-289">This property is inherited from [**CIM\_VirtualSystemSettingData**](/previous-versions//cc136954(v=vs.85)).</span></span>

</dd> <dt>

<span data-ttu-id="be8cd-290">**Файл ConfigurationFile**</span><span class="sxs-lookup"><span data-stu-id="be8cd-290">**ConfigurationFile**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="be8cd-291">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="be8cd-291">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="be8cd-292">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="be8cd-292">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="be8cd-293">Относительный путь и имя файла, в котором хранятся сведения о конфигурации виртуальной машины.</span><span class="sxs-lookup"><span data-stu-id="be8cd-293">The relative path and file name of a file where information about the virtual machine configuration is stored.</span></span> <span data-ttu-id="be8cd-294">Этот путь задается относительно свойства **конфигуратиондатарут** .</span><span class="sxs-lookup"><span data-stu-id="be8cd-294">This path is relative to the **ConfigurationDataRoot** property.</span></span> <span data-ttu-id="be8cd-295">Это свойство наследуется от [**CIM \_ виртуалсистемсеттингдата**](/previous-versions//cc136954(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="be8cd-295">This property is inherited from [**CIM\_VirtualSystemSettingData**](/previous-versions//cc136954(v=vs.85)).</span></span>

</dd> <dt>

<span data-ttu-id="be8cd-296">**ConfigurationID**</span><span class="sxs-lookup"><span data-stu-id="be8cd-296">**ConfigurationID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="be8cd-297">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="be8cd-297">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="be8cd-298">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="be8cd-298">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="be8cd-299">Уникальный идентификатор конфигурации виртуальной машины.</span><span class="sxs-lookup"><span data-stu-id="be8cd-299">The unique identifier of the virtual machine configuration.</span></span> <span data-ttu-id="be8cd-300">Это свойство наследуется от [**CIM \_ виртуалсистемсеттингдата**](/previous-versions//cc136954(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="be8cd-300">This property is inherited from [**CIM\_VirtualSystemSettingData**](/previous-versions//cc136954(v=vs.85)).</span></span>

</dd> <dt>

<span data-ttu-id="be8cd-301">**консолемоде**</span><span class="sxs-lookup"><span data-stu-id="be8cd-301">**ConsoleMode**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="be8cd-302">Тип данных: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="be8cd-302">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="be8cd-303">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="be8cd-303">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="be8cd-304">Определяет режим консоли для виртуальной машины.</span><span class="sxs-lookup"><span data-stu-id="be8cd-304">Identifies the Console Mode for the VM.</span></span>

> [!Note]  
> <span data-ttu-id="be8cd-305">Это свойство было добавлено в Windows 10 и Windows Server 2016.</span><span class="sxs-lookup"><span data-stu-id="be8cd-305">This property was added in Windows 10 and Windows Server 2016.</span></span>

 

<dt>

<span id="Default"></span><span id="default"></span><span id="DEFAULT"></span>

<span data-ttu-id="be8cd-306">**По умолчанию** (0)</span><span class="sxs-lookup"><span data-stu-id="be8cd-306">**Default** (0)</span></span>


</dt> <dd></dd> <dt>

<span id="COM1"></span><span id="com1"></span>

<span data-ttu-id="be8cd-307">**COM1** (1)</span><span class="sxs-lookup"><span data-stu-id="be8cd-307">**COM1** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="COM2"></span><span id="com2"></span>

<span data-ttu-id="be8cd-308">**COM2** (2)</span><span class="sxs-lookup"><span data-stu-id="be8cd-308">**COM2** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="None"></span><span id="none"></span><span id="NONE"></span>

<span data-ttu-id="be8cd-309">**Нет** (3)</span><span class="sxs-lookup"><span data-stu-id="be8cd-309">**None** (3)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="be8cd-310">**CreationTime**</span><span class="sxs-lookup"><span data-stu-id="be8cd-310">**CreationTime**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="be8cd-311">Тип данных: **DateTime**</span><span class="sxs-lookup"><span data-stu-id="be8cd-311">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="be8cd-312">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="be8cd-312">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="be8cd-313">Дата и время создания параметров виртуальной машины.</span><span class="sxs-lookup"><span data-stu-id="be8cd-313">The date and time at which the settings for the virtual machine were created.</span></span> <span data-ttu-id="be8cd-314">Если этот объект представляет текущие параметры виртуальной машины, это значение будет соответствовать времени создания системы.</span><span class="sxs-lookup"><span data-stu-id="be8cd-314">If this object represents the current settings for the virtual machine, this value would be the time at which the system was created.</span></span> <span data-ttu-id="be8cd-315">Если этот объект представляет параметры моментального снимка для виртуальной машины, это значение будет соответствовать времени создания моментального снимка.</span><span class="sxs-lookup"><span data-stu-id="be8cd-315">If this object represents the snapshot settings for the virtual machine, this value would be the time at which the snapshot was taken.</span></span> <span data-ttu-id="be8cd-316">Это свойство наследуется от [**CIM \_ виртуалсистемсеттингдата**](/previous-versions//cc136954(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="be8cd-316">This property is inherited from [**CIM\_VirtualSystemSettingData**](/previous-versions//cc136954(v=vs.85)).</span></span>

</dd> <dt>

<span data-ttu-id="be8cd-317">**дебугчаннелид**</span><span class="sxs-lookup"><span data-stu-id="be8cd-317">**DebugChannelId**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="be8cd-318">Тип данных: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="be8cd-318">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="be8cd-319">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="be8cd-319">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="be8cd-320">Идентификатор канала, используемый для отладки виртуальной машины с помощью унифицированного отладчика.</span><span class="sxs-lookup"><span data-stu-id="be8cd-320">The channel identifier used to debug the virtual machine using the unified debugger.</span></span>

</dd> <dt>

<span data-ttu-id="be8cd-321">**дебугпорт**</span><span class="sxs-lookup"><span data-stu-id="be8cd-321">**DebugPort**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="be8cd-322">Тип данных: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="be8cd-322">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="be8cd-323">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="be8cd-323">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="be8cd-324">Порт TCP/IP, используемый для отладки виртуальной машины с помощью искусственной отладки.</span><span class="sxs-lookup"><span data-stu-id="be8cd-324">The TCP/IP port used to debug the virtual machine using synthetic debugging.</span></span>

</dd> <dt>

<span data-ttu-id="be8cd-325">**дебугпортенаблед**</span><span class="sxs-lookup"><span data-stu-id="be8cd-325">**DebugPortEnabled**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="be8cd-326">Тип данных: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="be8cd-326">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="be8cd-327">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="be8cd-327">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="be8cd-328">Указывает, использует ли виртуальная машина искусственную отладку.</span><span class="sxs-lookup"><span data-stu-id="be8cd-328">Specifies whether the virtual machine is using synthetic debugging.</span></span> <span data-ttu-id="be8cd-329">Это может быть одно из следующих значений.</span><span class="sxs-lookup"><span data-stu-id="be8cd-329">This can be one of the following values.</span></span>

<dt>

<span id="Off"></span><span id="off"></span><span id="OFF"></span>

<span data-ttu-id="be8cd-330"><span id="Off"></span><span id="off"></span><span id="OFF"></span>**Выкл** . (0)</span><span class="sxs-lookup"><span data-stu-id="be8cd-330"><span id="Off"></span><span id="off"></span><span id="OFF"></span>**Off** (0)</span></span>


</dt> <dd></dd> <dt>

<span id="On"></span><span id="on"></span><span id="ON"></span>

<span data-ttu-id="be8cd-331"><span id="On"></span><span id="on"></span><span id="ON"></span>**В** (1)</span><span class="sxs-lookup"><span data-stu-id="be8cd-331"><span id="On"></span><span id="on"></span><span id="ON"></span>**On** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="OnAutoAssigned"></span><span id="onautoassigned"></span><span id="ONAUTOASSIGNED"></span>

<span data-ttu-id="be8cd-332"><span id="OnAutoAssigned"></span><span id="onautoassigned"></span><span id="ONAUTOASSIGNED"></span>**Онаутоассигнед** (2)</span><span class="sxs-lookup"><span data-stu-id="be8cd-332"><span id="OnAutoAssigned"></span><span id="onautoassigned"></span><span id="ONAUTOASSIGNED"></span>**OnAutoAssigned** (2)</span></span>


</dt> <dd>

<span data-ttu-id="be8cd-333">Назначено авто</span><span class="sxs-lookup"><span data-stu-id="be8cd-333">Auto-assigned</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="be8cd-334">**Описание**</span><span class="sxs-lookup"><span data-stu-id="be8cd-334">**Description**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="be8cd-335">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="be8cd-335">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="be8cd-336">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="be8cd-336">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="be8cd-337">Описание объекта.</span><span class="sxs-lookup"><span data-stu-id="be8cd-337">A description of the object.</span></span> <span data-ttu-id="be8cd-338">Это свойство наследуется от [**CIM \_ манажеделемент**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement)и всегда устанавливается в одно из следующих значений.</span><span class="sxs-lookup"><span data-stu-id="be8cd-338">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement), and it is always set to one of the following values.</span></span>



| <span data-ttu-id="be8cd-339">Значение</span><span class="sxs-lookup"><span data-stu-id="be8cd-339">Value</span></span>                                                                                                                  | <span data-ttu-id="be8cd-340">Значение</span><span class="sxs-lookup"><span data-stu-id="be8cd-340">Meaning</span></span>                                               |
|------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------|
| <dl> <span data-ttu-id="be8cd-341"><dt>"Активные параметры для виртуальной машины"</dt></span><span class="sxs-lookup"><span data-stu-id="be8cd-341"><dt>"Active settings for the virtual machine"</dt></span></span> </dl>   | <span data-ttu-id="be8cd-342">Этот экземпляр ссылается на виртуальную машину.</span><span class="sxs-lookup"><span data-stu-id="be8cd-342">This instance refers to a virtual machine.</span></span><br/> |
| <dl> <span data-ttu-id="be8cd-343"><dt>"Параметры моментальных снимков для виртуальной машины"</dt></span><span class="sxs-lookup"><span data-stu-id="be8cd-343"><dt>"Snapshot settings for the virtual machine"</dt></span></span> </dl> | <span data-ttu-id="be8cd-344">Этот экземпляр ссылается на моментальный снимок.</span><span class="sxs-lookup"><span data-stu-id="be8cd-344">This instance refers to a snapshot.</span></span><br/>        |



 

</dd> <dt>

<span data-ttu-id="be8cd-345">**ElementName**</span><span class="sxs-lookup"><span data-stu-id="be8cd-345">**ElementName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="be8cd-346">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="be8cd-346">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="be8cd-347">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="be8cd-347">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="be8cd-348">Отображаемое имя объекта.</span><span class="sxs-lookup"><span data-stu-id="be8cd-348">A display name for the object.</span></span> <span data-ttu-id="be8cd-349">Это свойство наследуется от [**CIM \_ виртуалсистемсеттингдата**](/previous-versions//cc136954(v=vs.85))и всегда устанавливается в качестве отображаемого имени для компьютера.</span><span class="sxs-lookup"><span data-stu-id="be8cd-349">This property is inherited from [**CIM\_VirtualSystemSettingData**](/previous-versions//cc136954(v=vs.85)), and it is always set to the display name for the machine.</span></span> <span data-ttu-id="be8cd-350">Длина имени не может превышать 100 символов.</span><span class="sxs-lookup"><span data-stu-id="be8cd-350">This name may not exceed 100 characters in length.</span></span>

</dd> <dt>

<span data-ttu-id="be8cd-351">**енханцедсессионтранспорттипе**</span><span class="sxs-lookup"><span data-stu-id="be8cd-351">**EnhancedSessionTransportType**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="be8cd-352">Тип данных: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="be8cd-352">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="be8cd-353">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="be8cd-353">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="be8cd-354">Указывает тип транспорта, используемый при подключении к расширенному сеансу.</span><span class="sxs-lookup"><span data-stu-id="be8cd-354">Indicates the transport type to use when connecting to an enhanced session.</span></span>

> [!Note]  
> <span data-ttu-id="be8cd-355">Это свойство было добавлено в Windows 10 версии 1803.</span><span class="sxs-lookup"><span data-stu-id="be8cd-355">This property was added in Windows 10, version 1803.</span></span>

 

<dt>

<span id="VMBus_Pipe"></span><span id="vmbus_pipe"></span><span id="VMBUS_PIPE"></span>

<span data-ttu-id="be8cd-356">**Канал VMBus** (0)</span><span class="sxs-lookup"><span data-stu-id="be8cd-356">**VMBus Pipe** (0)</span></span>


</dt> <dd></dd> <dt>

<span id="Hyper-V_Socket"></span><span id="hyper-v_socket"></span><span id="HYPER-V_SOCKET"></span>

<span data-ttu-id="be8cd-357">**Сокет Hyper-V** (1)</span><span class="sxs-lookup"><span data-stu-id="be8cd-357">**Hyper-V Socket** (1)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="be8cd-358">**гуестконтролледкачетипес**</span><span class="sxs-lookup"><span data-stu-id="be8cd-358">**GuestControlledCacheTypes**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="be8cd-359">Тип данных: **логический**</span><span class="sxs-lookup"><span data-stu-id="be8cd-359">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="be8cd-360">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="be8cd-360">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="be8cd-361">Указывает, может ли гостевой клиент управлять типами кэша.</span><span class="sxs-lookup"><span data-stu-id="be8cd-361">Indicates whether the guest can control cache types.</span></span>

> [!Note]  
> <span data-ttu-id="be8cd-362">Добавлено в Windows 10 и Windows Server 2016.</span><span class="sxs-lookup"><span data-stu-id="be8cd-362">Added in Windows 10 and Windows Server 2016.</span></span>

 

</dd> <dt>

<span data-ttu-id="be8cd-363">**гуестстатедатарут**</span><span class="sxs-lookup"><span data-stu-id="be8cd-363">**GuestStateDataRoot**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="be8cd-364">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="be8cd-364">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="be8cd-365">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="be8cd-365">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="be8cd-366">FilePath каталога, в котором хранятся сведения о состоянии гостевой среды выполнения.</span><span class="sxs-lookup"><span data-stu-id="be8cd-366">Filepath of a directory where information about the guest runtime state is stored.</span></span>

> [!Note]  
> <span data-ttu-id="be8cd-367">Добавлено в Windows 10 версии 1709.</span><span class="sxs-lookup"><span data-stu-id="be8cd-367">Added in Windows 10, version 1709.</span></span>

 

</dd> <dt>

<span data-ttu-id="be8cd-368">**гуестстатефиле**</span><span class="sxs-lookup"><span data-stu-id="be8cd-368">**GuestStateFile**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="be8cd-369">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="be8cd-369">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="be8cd-370">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="be8cd-370">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="be8cd-371">Путь к файлу, где хранятся сведения о состоянии гостевой среды выполнения.</span><span class="sxs-lookup"><span data-stu-id="be8cd-371">Filepath of a file where information about the guest runtime state is stored.</span></span> <span data-ttu-id="be8cd-372">Относительный путь добавляет к значению свойства **гуестстатедатарут** .</span><span class="sxs-lookup"><span data-stu-id="be8cd-372">A relative path appends to the value of the **GuestStateDataRoot** property.</span></span>

> [!Note]  
> <span data-ttu-id="be8cd-373">Добавлено в Windows 10 версии 1709.</span><span class="sxs-lookup"><span data-stu-id="be8cd-373">Added in Windows 10, version 1709.</span></span>

 

</dd> <dt>

<span data-ttu-id="be8cd-374">**хигхммиогапсизе**</span><span class="sxs-lookup"><span data-stu-id="be8cd-374">**HighMmioGapSize**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="be8cd-375">Тип данных: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="be8cd-375">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="be8cd-376">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="be8cd-376">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="be8cd-377">Размер верхнего (свыше 4 ГБ) Memory-Mapped зазора ввода-вывода в МБ</span><span class="sxs-lookup"><span data-stu-id="be8cd-377">The size of the High (above 4GB) Memory-Mapped IO Gap in MB</span></span>

> [!Note]  
> <span data-ttu-id="be8cd-378">Это свойство было добавлено в Windows 10 версии 1703.</span><span class="sxs-lookup"><span data-stu-id="be8cd-378">This property was added in Windows 10, version 1703.</span></span>

 

</dd> <dt>

<span data-ttu-id="be8cd-379">**инкременталбаккупенаблед**</span><span class="sxs-lookup"><span data-stu-id="be8cd-379">**IncrementalBackupEnabled**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="be8cd-380">Тип данных: **логический**</span><span class="sxs-lookup"><span data-stu-id="be8cd-380">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="be8cd-381">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="be8cd-381">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="be8cd-382">Указывает, поддерживает ли модуль записи VSS Hyper-V добавочное резервное копирование этой виртуальной машины.</span><span class="sxs-lookup"><span data-stu-id="be8cd-382">Indicates whether the Hyper-V VSS writer supports taking incremental backups of this virtual machine.</span></span>

</dd> <dt>

<span data-ttu-id="be8cd-383">**InstanceID**</span><span class="sxs-lookup"><span data-stu-id="be8cd-383">**InstanceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="be8cd-384">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="be8cd-384">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="be8cd-385">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="be8cd-385">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="be8cd-386">Квалификаторы: **ключ**</span><span class="sxs-lookup"><span data-stu-id="be8cd-386">Qualifiers: **Key**</span></span>
</dt> </dl>

<span data-ttu-id="be8cd-387">Уникально идентифицирует экземпляр этого класса.</span><span class="sxs-lookup"><span data-stu-id="be8cd-387">Uniquely identifies an instance of this class.</span></span> <span data-ttu-id="be8cd-388">Это свойство наследуется [**от \_ SettingData в CIM**](/previous-versions//cc136911(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="be8cd-388">This property is inherited from [**CIM\_SettingData**](/previous-versions//cc136911(v=vs.85)).</span></span>

</dd> <dt>

<span data-ttu-id="be8cd-389">**исаутоматикснапшот**</span><span class="sxs-lookup"><span data-stu-id="be8cd-389">**IsAutomaticSnapshot**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="be8cd-390">Тип данных: **логический**</span><span class="sxs-lookup"><span data-stu-id="be8cd-390">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="be8cd-391">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="be8cd-391">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="be8cd-392">Указывает, создается ли для пользователя моментальный снимок автоматически.</span><span class="sxs-lookup"><span data-stu-id="be8cd-392">Indicates whether this is a snapshot created automatically for the user.</span></span>

> [!Note]  
> <span data-ttu-id="be8cd-393">Добавлено в Windows 10 версии 1709.</span><span class="sxs-lookup"><span data-stu-id="be8cd-393">Added in Windows 10, version 1709.</span></span>

 

</dd> <dt>

<span data-ttu-id="be8cd-394">**IsSaved**</span><span class="sxs-lookup"><span data-stu-id="be8cd-394">**IsSaved**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="be8cd-395">Тип данных: **логический**</span><span class="sxs-lookup"><span data-stu-id="be8cd-395">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="be8cd-396">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="be8cd-396">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="be8cd-397">**Значение true** , если конфигурация содержит ссылку на файл сохраненного состояния; в противном случае — **значение false**.</span><span class="sxs-lookup"><span data-stu-id="be8cd-397">**True** if the configuration has a reference to a saved state file; otherwise, **False**.</span></span> <span data-ttu-id="be8cd-398">Это не указывает на наличие такого файла, и только в конфигурации его указывает.</span><span class="sxs-lookup"><span data-stu-id="be8cd-398">This does not indicate the presence of such a file, only that the configuration specifies one.</span></span>

</dd> <dt>

<span data-ttu-id="be8cd-399">**локкондисконнект**</span><span class="sxs-lookup"><span data-stu-id="be8cd-399">**LockOnDisconnect**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="be8cd-400">Тип данных: **логический**</span><span class="sxs-lookup"><span data-stu-id="be8cd-400">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="be8cd-401">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="be8cd-401">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="be8cd-402">Блокировка консоли при отключении от Vmconnect.</span><span class="sxs-lookup"><span data-stu-id="be8cd-402">Lock the console when disconnecting from vmconnect.</span></span>

> [!Note]  
> <span data-ttu-id="be8cd-403">Добавлено в Windows 10 и Windows Server 2016.</span><span class="sxs-lookup"><span data-stu-id="be8cd-403">Added in Windows 10 and Windows Server 2016.</span></span>

 

</dd> <dt>

<span data-ttu-id="be8cd-404">**логдатарут**</span><span class="sxs-lookup"><span data-stu-id="be8cd-404">**LogDataRoot**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="be8cd-405">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="be8cd-405">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="be8cd-406">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="be8cd-406">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="be8cd-407">Путь к каталогу, в котором хранится информация журнала для виртуальной машины.</span><span class="sxs-lookup"><span data-stu-id="be8cd-407">The path of a directory where log information for the virtual machine is stored.</span></span> <span data-ttu-id="be8cd-408">Это свойство наследуется от [**CIM \_ виртуалсистемсеттингдата**](/previous-versions//cc136954(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="be8cd-408">This property is inherited from [**CIM\_VirtualSystemSettingData**](/previous-versions//cc136954(v=vs.85)).</span></span>

</dd> <dt>

<span data-ttu-id="be8cd-409">**ловммиогапсизе**</span><span class="sxs-lookup"><span data-stu-id="be8cd-409">**LowMmioGapSize**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="be8cd-410">Тип данных: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="be8cd-410">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="be8cd-411">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="be8cd-411">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="be8cd-412">Настраивает размер первого зазора MMIO для виртуальной машины (в мегабайтах).</span><span class="sxs-lookup"><span data-stu-id="be8cd-412">Configures the size, in megabytes, of the first MMIO gap for a virtual machine (VM).</span></span>

<span data-ttu-id="be8cd-413">**Windows 8.1:** Это значение не поддерживается до Windows 8.1 и Windows Server 2012 R2.</span><span class="sxs-lookup"><span data-stu-id="be8cd-413">**Windows 8.1:** This value is not supported until Windows 8.1 and Windows Server 2012 R2.</span></span>

<span data-ttu-id="be8cd-414">Диапазон: 128 3584</span><span class="sxs-lookup"><span data-stu-id="be8cd-414">Range: 128 3584</span></span>

</dd> <dt>

<span data-ttu-id="be8cd-415">**нетворкбутпреферредпротокол**</span><span class="sxs-lookup"><span data-stu-id="be8cd-415">**NetworkBootPreferredProtocol**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="be8cd-416">Тип данных: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="be8cd-416">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="be8cd-417">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="be8cd-417">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="be8cd-418">Определяет, является ли предпочтительным протоколом для загрузки PXE IPv4 или IPv6.</span><span class="sxs-lookup"><span data-stu-id="be8cd-418">Determines if the preferred protocol for PXE boot is IPv4 or IPv6.</span></span>

<span data-ttu-id="be8cd-419">**Windows 8.1:** Это значение не поддерживается до Windows 8.1 и Windows Server 2012 R2.</span><span class="sxs-lookup"><span data-stu-id="be8cd-419">**Windows 8.1:** This value is not supported until Windows 8.1 and Windows Server 2012 R2.</span></span>

<dt>

<span id="IPv4"></span><span id="ipv4"></span><span id="IPV4"></span>

<span data-ttu-id="be8cd-420">**IPv4** (4096)</span><span class="sxs-lookup"><span data-stu-id="be8cd-420">**IPv4** (4096)</span></span>


</dt> <dd></dd> <dt>

<span id="IPv6"></span><span id="ipv6"></span><span id="IPV6"></span>

<span data-ttu-id="be8cd-421">**IPv6** (4097)</span><span class="sxs-lookup"><span data-stu-id="be8cd-421">**IPv6** (4097)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="be8cd-422">**Примечания**</span><span class="sxs-lookup"><span data-stu-id="be8cd-422">**Notes**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="be8cd-423">Тип данных: массив **строк**</span><span class="sxs-lookup"><span data-stu-id="be8cd-423">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="be8cd-424">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="be8cd-424">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="be8cd-425">Указанные пользователем примечания, связанные с виртуальной машиной.</span><span class="sxs-lookup"><span data-stu-id="be8cd-425">User supplied notes that are related to the virtual machine.</span></span> <span data-ttu-id="be8cd-426">Это свойство наследуется от [**CIM \_ виртуалсистемсеттингдата**](/previous-versions//cc136954(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="be8cd-426">This property is inherited from [**CIM\_VirtualSystemSettingData**](/previous-versions//cc136954(v=vs.85)).</span></span>

</dd> <dt>

<span data-ttu-id="be8cd-427">**Родительский объект**</span><span class="sxs-lookup"><span data-stu-id="be8cd-427">**Parent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="be8cd-428">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="be8cd-428">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="be8cd-429">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="be8cd-429">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="be8cd-430">Если этот экземпляр не представляет систему на основе моментального снимка виртуальной машины, это свойство имеет **значение NULL**.</span><span class="sxs-lookup"><span data-stu-id="be8cd-430">If this instance does not represent a system based on a snapshot of a virtual machine, this property is **Null**.</span></span> <span data-ttu-id="be8cd-431">В противном случае свойство содержит путь к объекту **мсвм \_ виртуалсистемсеттингдата** , на котором основан этот экземпляр.</span><span class="sxs-lookup"><span data-stu-id="be8cd-431">Otherwise, the property holds the object path of the **Msvm\_VirtualSystemSettingData** object on which this instance is based.</span></span> <span data-ttu-id="be8cd-432">При создании иерархии дерева моментальных снимков для виртуальной машины это свойство ссылается на объект, производный от которого является текущим экземпляром (текущий экземпляр является дочерним узлом, а объект, на который ссылается это свойство, является родительским узлом).</span><span class="sxs-lookup"><span data-stu-id="be8cd-432">When building a snapshot tree hierarchy for the virtual machine, this property references the object from which the current instance is derived (the current instance is the child node and the object referenced in this property is the parent node.)</span></span>

</dd> <dt>

<span data-ttu-id="be8cd-433">**парентпаккаже**</span><span class="sxs-lookup"><span data-stu-id="be8cd-433">**ParentPackage**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="be8cd-434">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="be8cd-434">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="be8cd-435">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="be8cd-435">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="be8cd-436">Если эта система является контейнером, то путь к Мсвм \_ контаинерпаккаже, на котором основана данная система.</span><span class="sxs-lookup"><span data-stu-id="be8cd-436">If this system is a container, the path to the Msvm\_ContainerPackage from which this system is based.</span></span>

> [!Note]  
> <span data-ttu-id="be8cd-437">Добавлено в Windows 10; удалено в Windows 10, версия 1703.</span><span class="sxs-lookup"><span data-stu-id="be8cd-437">Added in Windows 10; removed in Windows 10, version 1703.</span></span>

 

</dd> <dt>

<span data-ttu-id="be8cd-438">**паусеафтербутфаилуре**</span><span class="sxs-lookup"><span data-stu-id="be8cd-438">**PauseAfterBootFailure**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="be8cd-439">Тип данных: **логический**</span><span class="sxs-lookup"><span data-stu-id="be8cd-439">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="be8cd-440">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="be8cd-440">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="be8cd-441">Указывает, будет ли BIOS приостанавливать работу после каждой неудачной записи загрузки, ожидающей нажатия пользователем клавиши.</span><span class="sxs-lookup"><span data-stu-id="be8cd-441">Indicates whether the BIOS pauses after every boot entry failure waiting for the user to press a key.</span></span> <span data-ttu-id="be8cd-442">**Значение true** , если BIOS приостанавливает работу; в противном случае — **значение false**.</span><span class="sxs-lookup"><span data-stu-id="be8cd-442">**True** if the BIOS pauses; otherwise, **False**.</span></span>

<span data-ttu-id="be8cd-443">**Windows 8.1:** Это значение не поддерживается до Windows 8.1 и Windows Server 2012 R2.</span><span class="sxs-lookup"><span data-stu-id="be8cd-443">**Windows 8.1:** This value is not supported until Windows 8.1 and Windows Server 2012 R2.</span></span>

</dd> <dt>

<span data-ttu-id="be8cd-444">**рековерифиле**</span><span class="sxs-lookup"><span data-stu-id="be8cd-444">**RecoveryFile**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="be8cd-445">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="be8cd-445">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="be8cd-446">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="be8cd-446">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="be8cd-447">Полный путь к файлу, в котором хранится информация, связанная с восстановлением для виртуальной машины.</span><span class="sxs-lookup"><span data-stu-id="be8cd-447">The full path of a file where recovery related information for the virtual machine is stored.</span></span> <span data-ttu-id="be8cd-448">Это свойство наследуется от [**CIM \_ виртуалсистемсеттингдата**](/previous-versions//cc136954(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="be8cd-448">This property is inherited from [**CIM\_VirtualSystemSettingData**](/previous-versions//cc136954(v=vs.85)).</span></span>

</dd> <dt>

<span data-ttu-id="be8cd-449">**SecureBootEnabled**</span><span class="sxs-lookup"><span data-stu-id="be8cd-449">**SecureBootEnabled**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="be8cd-450">Тип данных: **логический**</span><span class="sxs-lookup"><span data-stu-id="be8cd-450">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="be8cd-451">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="be8cd-451">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="be8cd-452">Указывает, включена ли безопасная загрузка для виртуальной машины.</span><span class="sxs-lookup"><span data-stu-id="be8cd-452">Indicates whether secure boot is enabled for the virtual machine (VM).</span></span> <span data-ttu-id="be8cd-453">**Значение true** , если включено; в противном случае — **значение false**.</span><span class="sxs-lookup"><span data-stu-id="be8cd-453">**True** if enabled; otherwise, **False**.</span></span>

> [!Note]  
> <span data-ttu-id="be8cd-454">Безопасную загрузку можно включить только для виртуальных машин поколения 2.</span><span class="sxs-lookup"><span data-stu-id="be8cd-454">Secure boot can only be enabled for generation 2 VMs.</span></span>

 

<span data-ttu-id="be8cd-455">**Windows 8.1:** Это значение не поддерживается до Windows 8.1 и Windows Server 2012 R2.</span><span class="sxs-lookup"><span data-stu-id="be8cd-455">**Windows 8.1:** This value is not supported until Windows 8.1 and Windows Server 2012 R2.</span></span>

</dd> <dt>

<span data-ttu-id="be8cd-456">**секуребуттемплатеид**</span><span class="sxs-lookup"><span data-stu-id="be8cd-456">**SecureBootTemplateId**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="be8cd-457">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="be8cd-457">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="be8cd-458">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="be8cd-458">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="be8cd-459">Глобальный уникальный идентификатор шаблона начальное значений переменных, связанных с безопасной загрузкой UEFI.</span><span class="sxs-lookup"><span data-stu-id="be8cd-459">The globally-unique identifier of the template of intial values of UEFI Secure Boot related variables.</span></span>

<span data-ttu-id="be8cd-460">Это свойство доступно только для чтения, но его можно изменить с помощью метода [**модифивиртуалсистем**](https://www.bing.com/search?q=**ModifyVirtualSystem**) класса [**\_ виртуалсистемманажементсервице мсвм**](msvm-virtualsystemmanagementservice.md) .</span><span class="sxs-lookup"><span data-stu-id="be8cd-460">This is a read-only property, but it can be changed using the [**ModifyVirtualSystem**](https://www.bing.com/search?q=**ModifyVirtualSystem**) method of the [**Msvm\_VirtualSystemManagementService**](msvm-virtualsystemmanagementservice.md) class.</span></span>

> [!Note]  
> <span data-ttu-id="be8cd-461">Добавлено в Windows 10 и Windows Server 2016.</span><span class="sxs-lookup"><span data-stu-id="be8cd-461">Added in Windows 10 and Windows Server 2016.</span></span>

 

</dd> <dt>

<span data-ttu-id="be8cd-462">**снапшотдатарут**</span><span class="sxs-lookup"><span data-stu-id="be8cd-462">**SnapshotDataRoot**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="be8cd-463">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="be8cd-463">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="be8cd-464">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="be8cd-464">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="be8cd-465">Путь к каталогу, в котором хранятся сведения о моментальных снимках виртуальной машины.</span><span class="sxs-lookup"><span data-stu-id="be8cd-465">The path of a directory where information about the virtual machine snapshots is stored.</span></span> <span data-ttu-id="be8cd-466">Это свойство наследуется от [**CIM \_ виртуалсистемсеттингдата**](/previous-versions//cc136954(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="be8cd-466">This property is inherited from [**CIM\_VirtualSystemSettingData**](/previous-versions//cc136954(v=vs.85)).</span></span>

</dd> <dt>

<span data-ttu-id="be8cd-467">**суспенддатарут**</span><span class="sxs-lookup"><span data-stu-id="be8cd-467">**SuspendDataRoot**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="be8cd-468">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="be8cd-468">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="be8cd-469">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="be8cd-469">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="be8cd-470">Путь к каталогу, в котором хранятся сведения о приостановке виртуальной машины.</span><span class="sxs-lookup"><span data-stu-id="be8cd-470">The path of a directory where information about the virtual machine suspend-related information is stored.</span></span> <span data-ttu-id="be8cd-471">Это свойство наследуется от [**CIM \_ виртуалсистемсеттингдата**](/previous-versions//cc136954(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="be8cd-471">This property is inherited from [**CIM\_VirtualSystemSettingData**](/previous-versions//cc136954(v=vs.85)).</span></span>

</dd> <dt>

<span data-ttu-id="be8cd-472">**свапфиледатарут**</span><span class="sxs-lookup"><span data-stu-id="be8cd-472">**SwapFileDataRoot**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="be8cd-473">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="be8cd-473">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="be8cd-474">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="be8cd-474">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="be8cd-475">Путь к каталогу, в котором хранятся файлы подкачки для виртуальной машины.</span><span class="sxs-lookup"><span data-stu-id="be8cd-475">The path of a directory where swap files for the virtual machine are stored.</span></span> <span data-ttu-id="be8cd-476">Это свойство наследуется от [**CIM \_ виртуалсистемсеттингдата**](/previous-versions//cc136954(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="be8cd-476">This property is inherited from [**CIM\_VirtualSystemSettingData**](/previous-versions//cc136954(v=vs.85)).</span></span>

</dd> <dt>

<span data-ttu-id="be8cd-477">**усерснапшоттипе**</span><span class="sxs-lookup"><span data-stu-id="be8cd-477">**UserSnapshotType**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="be8cd-478">Тип данных: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="be8cd-478">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="be8cd-479">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="be8cd-479">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="be8cd-480">Указывает определяемый пользователем тип моментального снимка.</span><span class="sxs-lookup"><span data-stu-id="be8cd-480">Indicates the user-defined snapshot type.</span></span>

> [!Note]  
> <span data-ttu-id="be8cd-481">Добавлено в Windows 10 и Windows Server 2016.</span><span class="sxs-lookup"><span data-stu-id="be8cd-481">Added in Windows 10 and Windows Server 2016.</span></span>

 

<dt>

<span id="Disable"></span><span id="disable"></span><span id="DISABLE"></span>

<span data-ttu-id="be8cd-482"><span id="Disable"></span><span id="disable"></span><span id="DISABLE"></span>**Отключить** (2)</span><span class="sxs-lookup"><span data-stu-id="be8cd-482"><span id="Disable"></span><span id="disable"></span><span id="DISABLE"></span>**Disable** (2)</span></span>


</dt> <dd>

<span data-ttu-id="be8cd-483">Отключить создание моментального снимка.</span><span class="sxs-lookup"><span data-stu-id="be8cd-483">Disable the creation of any snapshot.</span></span>

</dd> <dt>

<span id="ProductionFallbackToTest"></span><span id="productionfallbacktotest"></span><span id="PRODUCTIONFALLBACKTOTEST"></span>

<span data-ttu-id="be8cd-484"><span id="ProductionFallbackToTest"></span><span id="productionfallbacktotest"></span><span id="PRODUCTIONFALLBACKTOTEST"></span>**Продуктионфаллбакктотест** (3)</span><span class="sxs-lookup"><span data-stu-id="be8cd-484"><span id="ProductionFallbackToTest"></span><span id="productionfallbacktotest"></span><span id="PRODUCTIONFALLBACKTOTEST"></span>**ProductionFallbackToTest** (3)</span></span>


</dt> <dd>

<span data-ttu-id="be8cd-485">Моментальный снимок, совместимый с данными, для использования в рабочей среде. Выполняет моментальный снимок с состоянием приложения, если возможность создания моментального снимка с одинаковыми данными недоступна.</span><span class="sxs-lookup"><span data-stu-id="be8cd-485">Data-consistent snapshot for use in the production environment.Performs a snapshot with application state when the ability to create data consistent snapshot is not available.</span></span>

</dd> <dt>

<span id="ProductionNoFallback"></span><span id="productionnofallback"></span><span id="PRODUCTIONNOFALLBACK"></span>

<span data-ttu-id="be8cd-486"><span id="ProductionNoFallback"></span><span id="productionnofallback"></span><span id="PRODUCTIONNOFALLBACK"></span>**Продуктионнофаллбакк** (4)</span><span class="sxs-lookup"><span data-stu-id="be8cd-486"><span id="ProductionNoFallback"></span><span id="productionnofallback"></span><span id="PRODUCTIONNOFALLBACK"></span>**ProductionNoFallback** (4)</span></span>


</dt> <dd>

<span data-ttu-id="be8cd-487">Моментальный снимок, совместимый с данными, для использования в рабочей среде. Не создает моментальный снимок с состоянием приложения, если невозможно создать моментальный снимок с одинаковыми данными.</span><span class="sxs-lookup"><span data-stu-id="be8cd-487">Data-consistent snapshot for use in the production environment.Does not create a snapshot with application state if it is not possible to create a data consistent snapshot.</span></span>

</dd> <dt>

<span id="Test"></span><span id="test"></span><span id="TEST"></span>

<span data-ttu-id="be8cd-488"><span id="Test"></span><span id="test"></span><span id="TEST"></span>**Тест** (5)</span><span class="sxs-lookup"><span data-stu-id="be8cd-488"><span id="Test"></span><span id="test"></span><span id="TEST"></span>**Test** (5)</span></span>


</dt> <dd>

<span data-ttu-id="be8cd-489">Моментальный снимок, который содержит сведения о памяти и устройстве для целей тестирования и разработки.</span><span class="sxs-lookup"><span data-stu-id="be8cd-489">Snapshot that contains memory and device information for test and development purpose.</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="be8cd-490">**Version**</span><span class="sxs-lookup"><span data-stu-id="be8cd-490">**Version**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="be8cd-491">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="be8cd-491">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="be8cd-492">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="be8cd-492">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="be8cd-493">Версия виртуальной машины в формате "основной. дополнительный", например "2,0".</span><span class="sxs-lookup"><span data-stu-id="be8cd-493">The version of the virtual machine in a format of "major.minor", for example "2.0".</span></span>

</dd> <dt>

<span data-ttu-id="be8cd-494">**виртуалнумаенаблед**</span><span class="sxs-lookup"><span data-stu-id="be8cd-494">**VirtualNumaEnabled**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="be8cd-495">Тип данных: **логический**</span><span class="sxs-lookup"><span data-stu-id="be8cd-495">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="be8cd-496">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="be8cd-496">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="be8cd-497">Квалификаторы: [**моделкорреспонденце**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**мсвм \_ процессорсеттингдата**](msvm-processorsettingdata.md).**Макспроцессорспернуманоде**","[**мсвм \_ меморисеттингдата**](msvm-memorysettingdata.md).**Максмемориблоккспернуманоде**")</span><span class="sxs-lookup"><span data-stu-id="be8cd-497">Qualifiers: [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**Msvm\_ProcessorSettingData**](msvm-processorsettingdata.md).**MaxProcessorsPerNumaNode**", "[**Msvm\_MemorySettingData**](msvm-memorysettingdata.md).**MaxMemoryBlocksPerNumaNode**")</span></span>
</dt> </dl>

<span data-ttu-id="be8cd-498">**Значение true** , если виртуальные узлы неоднородного доступа к памяти (NUMA) проецируются в виртуальную машину; **Значение false** , если виртуальная машина будет иметь один узел.</span><span class="sxs-lookup"><span data-stu-id="be8cd-498">**True** if virtual non-uniform memory access (NUMA) nodes are projected into the virtual machine; **False** if the virtual machine will have a single node.</span></span> <span data-ttu-id="be8cd-499">Если **значение — true**, количество ВИРТУАЛЬНЫХ узлов NUMA, проецируемых в виртуальную машину, определяется значениями свойств [**Мсвм \_ Процессорсеттингдата. макспроцессорспернуманоде**](msvm-processorsettingdata.md) и [**мсвм \_ меморисеттингдата. максмемориблоккспернуманоде**](msvm-memorysettingdata.md) .</span><span class="sxs-lookup"><span data-stu-id="be8cd-499">If **True**, the number of virtual NUMA nodes projected into the virtual machine is determined from the values of the [**Msvm\_ProcessorSettingData.MaxProcessorsPerNumaNode**](msvm-processorsettingdata.md) and [**Msvm\_MemorySettingData.MaxMemoryBlocksPerNumaNode**](msvm-memorysettingdata.md) properties.</span></span>

</dd> <dt>

<span data-ttu-id="be8cd-500">**виртуалсистемидентифиер**</span><span class="sxs-lookup"><span data-stu-id="be8cd-500">**VirtualSystemIdentifier**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="be8cd-501">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="be8cd-501">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="be8cd-502">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="be8cd-502">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="be8cd-503">Квалификаторы: [**override**](/windows/desktop/WmiSdk/standard-qualifiers) ("CIM \_ виртуалсистемсеттингдата. виртуалсистемидентифиер"), [**моделкорреспонденце**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM \_ ComputerSystem**](cim-computersystem.md).**Name**")</span><span class="sxs-lookup"><span data-stu-id="be8cd-503">Qualifiers: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("CIM\_VirtualSystemSettingData.VirtualSystemIdentifier"), [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM\_ComputerSystem**](cim-computersystem.md).**Name**")</span></span>
</dt> </dl>

<span data-ttu-id="be8cd-504">Имя объекта [**CIM \_ ComputerSystem**](/windows/desktop/CIMWin32Prov/cim-computersystem) , которому принадлежат данные этого параметра.</span><span class="sxs-lookup"><span data-stu-id="be8cd-504">The name of the [**CIM\_ComputerSystem**](/windows/desktop/CIMWin32Prov/cim-computersystem) object to which this setting data belongs.</span></span> <span data-ttu-id="be8cd-505">Это свойство является переопределением из [**CIM \_ виртуалсистемсеттингдата**](/previous-versions//cc136954(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="be8cd-505">This property is an override from [**CIM\_VirtualSystemSettingData**](/previous-versions//cc136954(v=vs.85)).</span></span>

</dd> <dt>

<span data-ttu-id="be8cd-506">**VirtualSystemSubType**</span><span class="sxs-lookup"><span data-stu-id="be8cd-506">**VirtualSystemSubType**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="be8cd-507">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="be8cd-507">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="be8cd-508">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="be8cd-508">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="be8cd-509">Допустимыми значениями для этого свойства являются Microsoft: Hyper-V: подтип: 1 и Microsoft: Hyper-V: подтип: 2.</span><span class="sxs-lookup"><span data-stu-id="be8cd-509">The valid values for this property are Microsoft:Hyper-V:SubType:1 and Microsoft:Hyper-V:SubType:2.</span></span> <span data-ttu-id="be8cd-510">Виртуальная машина поколения 1 имеет подтип 1.</span><span class="sxs-lookup"><span data-stu-id="be8cd-510">A  Generation 1  VM is subtype 1.</span></span> <span data-ttu-id="be8cd-511">Виртуальная машина поколения 2 имеет подтип 2.</span><span class="sxs-lookup"><span data-stu-id="be8cd-511">A  Generation 2  VM is subtype 2.</span></span>

<span data-ttu-id="be8cd-512">**Windows 8.1:** Это значение не поддерживается до Windows 8.1 и Windows Server 2012 R2.</span><span class="sxs-lookup"><span data-stu-id="be8cd-512">**Windows 8.1:** This value is not supported until Windows 8.1 and Windows Server 2012 R2.</span></span>

<dt>

<span id="Microsoft_Hyper-V_SubType_1"></span><span id="microsoft_hyper-v_subtype_1"></span><span id="MICROSOFT_HYPER-V_SUBTYPE_1"></span>

<span data-ttu-id="be8cd-513">**Microsoft: Hyper-v: подтип: 1** ("Microsoft: Hyper-V: подтип: 1")</span><span class="sxs-lookup"><span data-stu-id="be8cd-513">**Microsoft:Hyper-V:SubType:1** ("Microsoft:Hyper-V:SubType:1")</span></span>


</dt> <dd></dd> <dt>

<span id="Microsoft_Hyper-V_SubType_2"></span><span id="microsoft_hyper-v_subtype_2"></span><span id="MICROSOFT_HYPER-V_SUBTYPE_2"></span>

<span data-ttu-id="be8cd-514">**Microsoft: Hyper-v: подтип: 2** ("Microsoft: Hyper-V: подтип: 2")</span><span class="sxs-lookup"><span data-stu-id="be8cd-514">**Microsoft:Hyper-V:SubType:2** ("Microsoft:Hyper-V:SubType:2")</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="be8cd-515">**виртуалсистемтипе**</span><span class="sxs-lookup"><span data-stu-id="be8cd-515">**VirtualSystemType**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="be8cd-516">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="be8cd-516">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="be8cd-517">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="be8cd-517">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="be8cd-518">Указывает тип виртуальной машины, которую представляют данные параметров.</span><span class="sxs-lookup"><span data-stu-id="be8cd-518">Specifies the type of virtual machine the setting data represents.</span></span> <span data-ttu-id="be8cd-519">Это свойство наследуется от класса [**CIM \_ виртуалсистемсеттингдата**](/previous-versions//cc136954(v=vs.85)) .</span><span class="sxs-lookup"><span data-stu-id="be8cd-519">This property is inherited from the [**CIM\_VirtualSystemSettingData**](/previous-versions//cc136954(v=vs.85)) class.</span></span> <span data-ttu-id="be8cd-520">Это может быть одно из следующих значений.</span><span class="sxs-lookup"><span data-stu-id="be8cd-520">This will be one of the following values.</span></span>



| <span data-ttu-id="be8cd-521">Значение</span><span class="sxs-lookup"><span data-stu-id="be8cd-521">Value</span></span>                                                                                                                                 | <span data-ttu-id="be8cd-522">Значение</span><span class="sxs-lookup"><span data-stu-id="be8cd-522">Meaning</span></span>                                              |
|---------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------|
| <dl> <span data-ttu-id="be8cd-523"><dt>"Microsoft: Hyper-V: System: Реализовано"</dt></span><span class="sxs-lookup"><span data-stu-id="be8cd-523"><dt>"Microsoft:Hyper-V:System:Realized"</dt></span></span> </dl>                        | <span data-ttu-id="be8cd-524">Реализованная виртуальная машина.</span><span class="sxs-lookup"><span data-stu-id="be8cd-524">A realized virtual machine.</span></span><br/>               |
| <dl> <span data-ttu-id="be8cd-525"><dt>"Microsoft: Hyper-V: система: запланировано"</dt></span><span class="sxs-lookup"><span data-stu-id="be8cd-525"><dt>"Microsoft:Hyper-V:System:Planned"</dt></span></span> </dl>                         | <span data-ttu-id="be8cd-526">Запланированная виртуальная машина.</span><span class="sxs-lookup"><span data-stu-id="be8cd-526">A planned virtual machine.</span></span><br/>                |
| <dl> <span data-ttu-id="be8cd-527"><dt>"Microsoft: Hyper-V: моментальный снимок: реализован"</dt></span><span class="sxs-lookup"><span data-stu-id="be8cd-527"><dt>"Microsoft:Hyper-V:Snapshot:Realized"</dt></span></span> </dl>                      | <span data-ttu-id="be8cd-528">Моментальный снимок реализованной виртуальной машины.</span><span class="sxs-lookup"><span data-stu-id="be8cd-528">A snapshot of a realized virtual machine.</span></span><br/> |
| <dl> <span data-ttu-id="be8cd-529"><dt>"Microsoft: Hyper-V: моментальный снимок: восстановление"</dt></span><span class="sxs-lookup"><span data-stu-id="be8cd-529"><dt>"Microsoft:Hyper-V:Snapshot:Recovery"</dt></span></span> </dl>                      | <span data-ttu-id="be8cd-530">Моментальный снимок виртуальной машины восстановления.</span><span class="sxs-lookup"><span data-stu-id="be8cd-530">A snapshot of a recovery virtual machine.</span></span><br/> |
| <dl> <span data-ttu-id="be8cd-531"><dt>"Microsoft: Hyper-V: моментальный снимок: запланированный"</dt></span><span class="sxs-lookup"><span data-stu-id="be8cd-531"><dt>"Microsoft:Hyper-V:Snapshot:Planned"</dt></span></span> </dl>                       | <span data-ttu-id="be8cd-532">Моментальный снимок запланированной виртуальной машины.</span><span class="sxs-lookup"><span data-stu-id="be8cd-532">A snapshot of a planned virtual machine.</span></span><br/>  |
| <dl> <span data-ttu-id="be8cd-533"><dt>"Microsoft: Hyper-V: моментальный снимок: отсутствует"</dt></span><span class="sxs-lookup"><span data-stu-id="be8cd-533"><dt>"Microsoft:Hyper-V:Snapshot:Missing"</dt></span></span> </dl>                       | <span data-ttu-id="be8cd-534">Отсутствует моментальный снимок.</span><span class="sxs-lookup"><span data-stu-id="be8cd-534">A missing snapshot.</span></span><br/>                       |
| <dl> <span data-ttu-id="be8cd-535"><dt>"Microsoft: Hyper-V: моментальный снимок: Реплика: Стандартный"</dt></span><span class="sxs-lookup"><span data-stu-id="be8cd-535"><dt>"Microsoft:Hyper-V:Snapshot:Replica:Standard"</dt></span></span> </dl>              | <span data-ttu-id="be8cd-536">Моментальный снимок точки репликации на основе времени.</span><span class="sxs-lookup"><span data-stu-id="be8cd-536">A time-based replication point snapshot.</span></span><br/>  |
| <dl> <span data-ttu-id="be8cd-537"><dt>"Microsoft: Hyper-V: моментальный снимок: Реплика: Аппликатионконсистент"</dt></span><span class="sxs-lookup"><span data-stu-id="be8cd-537"><dt>"Microsoft:Hyper-V:Snapshot:Replica:ApplicationConsistent"</dt></span></span> </dl> | <span data-ttu-id="be8cd-538">Моментальный снимок точки репликации VSS.</span><span class="sxs-lookup"><span data-stu-id="be8cd-538">A VSS replication point snapshot.</span></span><br/>         |
| <dl> <span data-ttu-id="be8cd-539"><dt>"Microsoft: Hyper-V: моментальный снимок: Реплика: Планнедфаиловер"</dt></span><span class="sxs-lookup"><span data-stu-id="be8cd-539"><dt>"Microsoft:Hyper-V:Snapshot:Replica:PlannedFailover"</dt></span></span> </dl>       | <span data-ttu-id="be8cd-540">Плановый моментальный снимок репликации.</span><span class="sxs-lookup"><span data-stu-id="be8cd-540">A planned replication snapshot.</span></span><br/>           |



 

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="be8cd-541">Комментарии</span><span class="sxs-lookup"><span data-stu-id="be8cd-541">Remarks</span></span>

<span data-ttu-id="be8cd-542">Доступ к классу **\_ виртуалсистемсеттингдата мсвм** может быть ограничен фильтром контроля учетных записей.</span><span class="sxs-lookup"><span data-stu-id="be8cd-542">Access to the **Msvm\_VirtualSystemSettingData** class might be restricted by UAC Filtering.</span></span> <span data-ttu-id="be8cd-543">Дополнительные сведения см. в разделе [Управление учетными записями пользователей и инструментарий WMI](/windows/desktop/WmiSdk/user-account-control-and-wmi).</span><span class="sxs-lookup"><span data-stu-id="be8cd-543">For more information, see [User Account Control and WMI](/windows/desktop/WmiSdk/user-account-control-and-wmi).</span></span>

## <a name="requirements"></a><span data-ttu-id="be8cd-544">Требования</span><span class="sxs-lookup"><span data-stu-id="be8cd-544">Requirements</span></span>



| <span data-ttu-id="be8cd-545">Требование</span><span class="sxs-lookup"><span data-stu-id="be8cd-545">Requirement</span></span> | <span data-ttu-id="be8cd-546">Значение</span><span class="sxs-lookup"><span data-stu-id="be8cd-546">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="be8cd-547">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="be8cd-547">Minimum supported client</span></span><br/> | <span data-ttu-id="be8cd-548">\[Только классические приложения Windows 8\]</span><span class="sxs-lookup"><span data-stu-id="be8cd-548">Windows 8 \[desktop apps only\]</span></span><br/>                                                              |
| <span data-ttu-id="be8cd-549">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="be8cd-549">Minimum supported server</span></span><br/> | <span data-ttu-id="be8cd-550">\[Только для настольных приложений Windows Server 2012\]</span><span class="sxs-lookup"><span data-stu-id="be8cd-550">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="be8cd-551">Пространство имен</span><span class="sxs-lookup"><span data-stu-id="be8cd-551">Namespace</span></span><br/>                | <span data-ttu-id="be8cd-552">Корневая \\ виртуализация \\ версии 2</span><span class="sxs-lookup"><span data-stu-id="be8cd-552">Root\\Virtualization\\V2</span></span><br/>                                                                     |
| <span data-ttu-id="be8cd-553">MOF</span><span class="sxs-lookup"><span data-stu-id="be8cd-553">MOF</span></span><br/>                      | <dl> <span data-ttu-id="be8cd-554"><dt>Виндовсвиртуализатион. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="be8cd-554"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="be8cd-555">DLL</span><span class="sxs-lookup"><span data-stu-id="be8cd-555">DLL</span></span><br/>                      | <dl> <span data-ttu-id="be8cd-556"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="be8cd-556"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="be8cd-557">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="be8cd-557">See also</span></span>

<dl> <dt>

[<span data-ttu-id="be8cd-558">**\_ВИРТУАЛСИСТЕМСЕТТИНГДАТА CIM**</span><span class="sxs-lookup"><span data-stu-id="be8cd-558">**CIM\_VirtualSystemSettingData**</span></span>](cim-virtualsystemsettingdata.md)
</dt> <dt>

<span data-ttu-id="be8cd-559">[**\_ВИРТУАЛСИСТЕМСЕТТИНГДАТА CIM**](/previous-versions//cc136954(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="be8cd-559">[**CIM\_VirtualSystemSettingData**](/previous-versions//cc136954(v=vs.85))</span></span>
</dt> <dt>

[<span data-ttu-id="be8cd-560">Классы виртуальных систем</span><span class="sxs-lookup"><span data-stu-id="be8cd-560">Virtual System Classes</span></span>](virtual-system-classes.md)
</dt> </dl>

 

