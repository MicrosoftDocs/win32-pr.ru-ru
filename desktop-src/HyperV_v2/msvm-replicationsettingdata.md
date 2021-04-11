---
description: Представляет параметры репликации для виртуальной машины.
ms.assetid: f6f6a413-a949-4aca-930b-37e39bdc1fdb
title: Класс Msvm_ReplicationSettingData
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_ReplicationSettingData
- Msvm_ReplicationSettingData.InstanceID
- Msvm_ReplicationSettingData.Caption
- Msvm_ReplicationSettingData.Description
- Msvm_ReplicationSettingData.ElementName
- Msvm_ReplicationSettingData.VirtualSystemIdentifier
- Msvm_ReplicationSettingData.VirtualSystemType
- Msvm_ReplicationSettingData.Notes
- Msvm_ReplicationSettingData.CreationTime
- Msvm_ReplicationSettingData.ConfigurationID
- Msvm_ReplicationSettingData.ConfigurationDataRoot
- Msvm_ReplicationSettingData.ConfigurationFile
- Msvm_ReplicationSettingData.SnapshotDataRoot
- Msvm_ReplicationSettingData.SuspendDataRoot
- Msvm_ReplicationSettingData.SwapFileDataRoot
- Msvm_ReplicationSettingData.LogDataRoot
- Msvm_ReplicationSettingData.AutomaticStartupAction
- Msvm_ReplicationSettingData.AutomaticStartupActionDelay
- Msvm_ReplicationSettingData.AutomaticStartupActionSequenceNumber
- Msvm_ReplicationSettingData.AutomaticShutdownAction
- Msvm_ReplicationSettingData.AutomaticRecoveryAction
- Msvm_ReplicationSettingData.RecoveryFile
- Msvm_ReplicationSettingData.AuthenticationType
- Msvm_ReplicationSettingData.CertificateThumbPrint
- Msvm_ReplicationSettingData.RootCertificateThumbPrint
- Msvm_ReplicationSettingData.CompressionEnabled
- Msvm_ReplicationSettingData.BypassProxyServer
- Msvm_ReplicationSettingData.RecoveryConnectionPoint
- Msvm_ReplicationSettingData.RecoveryHostSystem
- Msvm_ReplicationSettingData.PrimaryConnectionPoint
- Msvm_ReplicationSettingData.PrimaryHostSystem
- Msvm_ReplicationSettingData.RecoveryServerPortNumber
- Msvm_ReplicationSettingData.ReplicateHostKvpItems
- Msvm_ReplicationSettingData.ApplicationConsistentSnapshotInterval
- Msvm_ReplicationSettingData.RecoveryHistory
- Msvm_ReplicationSettingData.IncludedDisks
- Msvm_ReplicationSettingData.AutoResynchronizeEnabled
- Msvm_ReplicationSettingData.AutoResynchronizeIntervalStart
- Msvm_ReplicationSettingData.AutoResynchronizeIntervalEnd
- Msvm_ReplicationSettingData.EnableWriteOrderPreservationAcrossDisks
- Msvm_ReplicationSettingData.ReplicationProvider
- Msvm_ReplicationSettingData.AdditionalSettings
- Msvm_ReplicationSettingData.ReplicationInterval
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: 35bb97e531f8aca5f74801d55a71e5b3f2850c08
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "104265055"
---
# <a name="msvm_replicationsettingdata-class"></a><span data-ttu-id="2370d-103">\_Класс мсвм репликатионсеттингдата</span><span class="sxs-lookup"><span data-stu-id="2370d-103">Msvm\_ReplicationSettingData class</span></span>

<span data-ttu-id="2370d-104">Представляет параметры репликации для виртуальной машины.</span><span class="sxs-lookup"><span data-stu-id="2370d-104">Represents the replication-specific settings for a virtual machine.</span></span> <span data-ttu-id="2370d-105">Клиент передает экземпляр этого класса в [**мсвм \_ Репликатионсервице. CreateReplicationRelationship**](createreplicationrelationship-msvm-replicationservice.md) для создания отношения репликации.</span><span class="sxs-lookup"><span data-stu-id="2370d-105">The client passes an instance of this class to [**Msvm\_ReplicationService.CreateReplicationRelationship**](createreplicationrelationship-msvm-replicationservice.md) to create a replication relationship.</span></span> <span data-ttu-id="2370d-106">Клиент не может напрямую изменять значения любого из свойств этого класса. для изменения значений необходимо вызвать метод [**мсвм \_ Репликатионсервице. модифирепликатионсеттингс.**](modifyreplicationsettings-msvm-replicationservice.md)</span><span class="sxs-lookup"><span data-stu-id="2370d-106">The client can't directly change the values of any of the properties for this class; it must call the [**Msvm\_ReplicationService.ModifyReplicationSettings**](modifyreplicationsettings-msvm-replicationservice.md) method to change the values.</span></span> <span data-ttu-id="2370d-107">Каждое отношение репликации имеет единственный экземпляр параметров.</span><span class="sxs-lookup"><span data-stu-id="2370d-107">Each replication relationship has a single instance of settings.</span></span>

<span data-ttu-id="2370d-108">Следующий синтаксис является упрощенным MOF-файлным (MOF) кодом и включает все наследуемые свойства.</span><span class="sxs-lookup"><span data-stu-id="2370d-108">The following syntax is simplified Managed Object Format (MOF) code, and it includes all of the inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="2370d-109">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="2370d-109">Syntax</span></span>

``` syntax
[Dynamic, Provider("VmmsWmiInstanceAndMethodProvider"), AMENDMENT]
class Msvm_ReplicationSettingData : CIM_VirtualSystemSettingData
{
  string   InstanceID = "Microsoft:Virtual Machine GUID\HVR";
  string   Caption = "Replication Settings";
  string   Description = "Virtual Machine Replication Settings Data";
  string   ElementName;
  string   VirtualSystemIdentifier;
  string   VirtualSystemType = "Microsoft:Hyper-V:Replica";
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
  uint16   AuthenticationType;
  string   CertificateThumbPrint;
  string   RootCertificateThumbPrint;
  boolean  CompressionEnabled;
  boolean  BypassProxyServer;
  string   RecoveryConnectionPoint;
  string   RecoveryHostSystem;
  string   PrimaryConnectionPoint;
  string   PrimaryHostSystem;
  uint16   RecoveryServerPortNumber = 0;
  boolean  ReplicateHostKvpItems = True;
  uint16   ApplicationConsistentSnapshotInterval;
  uint16   RecoveryHistory = 0;
  string   IncludedDisks[];
  boolean  AutoResynchronizeEnabled = False;
  datetime AutoResynchronizeIntervalStart = 00000000183000.000000:000;
  datetime AutoResynchronizeIntervalEnd = 00000000060000.000000:000;
  boolean  EnableWriteOrderPreservationAcrossDisks;
  string   ReplicationProvider;
  string   AdditionalSettings;
  uint16   ReplicationInterval = 300;
};
```

## <a name="members"></a><span data-ttu-id="2370d-110">Члены</span><span class="sxs-lookup"><span data-stu-id="2370d-110">Members</span></span>

<span data-ttu-id="2370d-111">Класс **мсвм \_ репликатионсеттингдата** имеет следующие типы членов:</span><span class="sxs-lookup"><span data-stu-id="2370d-111">The **Msvm\_ReplicationSettingData** class has these types of members:</span></span>

-   [<span data-ttu-id="2370d-112">Свойства</span><span class="sxs-lookup"><span data-stu-id="2370d-112">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="2370d-113">Свойства</span><span class="sxs-lookup"><span data-stu-id="2370d-113">Properties</span></span>

<span data-ttu-id="2370d-114">Класс **мсвм \_ репликатионсеттингдата** имеет следующие свойства.</span><span class="sxs-lookup"><span data-stu-id="2370d-114">The **Msvm\_ReplicationSettingData** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="2370d-115">**аддитионалсеттингс**</span><span class="sxs-lookup"><span data-stu-id="2370d-115">**AdditionalSettings**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2370d-116">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="2370d-116">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="2370d-117">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="2370d-117">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="2370d-118">Дополнительные параметры репликации, которые может использовать поставщик конечной точки.</span><span class="sxs-lookup"><span data-stu-id="2370d-118">Additional replication settings that the endpoint provider can use.</span></span>

<span data-ttu-id="2370d-119">**Windows 8.1:** Это значение не поддерживается до Windows 8.1 и Windows Server 2012 R2.</span><span class="sxs-lookup"><span data-stu-id="2370d-119">**Windows 8.1:** This value is not supported until Windows 8.1 and Windows Server 2012 R2.</span></span>

</dd> <dt>

<span data-ttu-id="2370d-120">**аппликатионконсистентснапшотинтервал**</span><span class="sxs-lookup"><span data-stu-id="2370d-120">**ApplicationConsistentSnapshotInterval**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2370d-121">Тип данных: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="2370d-121">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="2370d-122">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="2370d-122">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="2370d-123">Интервал времени между моментальными снимками, согласованными с приложениями, заданными в часах.</span><span class="sxs-lookup"><span data-stu-id="2370d-123">The time interval between application consistent snapshots, specified in hours.</span></span> <span data-ttu-id="2370d-124">Допустимые значения: от 1 до 12 часов.</span><span class="sxs-lookup"><span data-stu-id="2370d-124">Valid values are from 1 hour to 12 hours.</span></span>

</dd> <dt>

<span data-ttu-id="2370d-125">**AuthenticationType**</span><span class="sxs-lookup"><span data-stu-id="2370d-125">**AuthenticationType**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2370d-126">Тип данных: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="2370d-126">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="2370d-127">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="2370d-127">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="2370d-128">Определите режим проверки подлинности, используемый для подключения к серверу восстановления.</span><span class="sxs-lookup"><span data-stu-id="2370d-128">Define authentication mode used to connect to recover server.</span></span>

<dt>

<span id="Kerberos_authentication"></span><span id="kerberos_authentication"></span><span id="KERBEROS_AUTHENTICATION"></span>

<span data-ttu-id="2370d-129"><span id="Kerberos_authentication"></span><span id="kerberos_authentication"></span><span id="KERBEROS_AUTHENTICATION"></span>**Проверка подлинности Kerberos** (1)</span><span class="sxs-lookup"><span data-stu-id="2370d-129"><span id="Kerberos_authentication"></span><span id="kerberos_authentication"></span><span id="KERBEROS_AUTHENTICATION"></span>**Kerberos authentication** (1)</span></span>


</dt> <dd>

<span data-ttu-id="2370d-130">Аутентификация Kerberos.</span><span class="sxs-lookup"><span data-stu-id="2370d-130">Kerberos authentication.</span></span>

</dd> <dt>

<span id="Certificate_based_authentication"></span><span id="certificate_based_authentication"></span><span id="CERTIFICATE_BASED_AUTHENTICATION"></span>

<span data-ttu-id="2370d-131"><span id="Certificate_based_authentication"></span><span id="certificate_based_authentication"></span><span id="CERTIFICATE_BASED_AUTHENTICATION"></span>**Проверка подлинности на основе сертификата** (2)</span><span class="sxs-lookup"><span data-stu-id="2370d-131"><span id="Certificate_based_authentication"></span><span id="certificate_based_authentication"></span><span id="CERTIFICATE_BASED_AUTHENTICATION"></span>**Certificate based authentication** (2)</span></span>


</dt> <dd>

<span data-ttu-id="2370d-132">Проверка подлинности на основе сертификата.</span><span class="sxs-lookup"><span data-stu-id="2370d-132">Certificate based authentication.</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="2370d-133">**аутоматикрековеряктион**</span><span class="sxs-lookup"><span data-stu-id="2370d-133">**AutomaticRecoveryAction**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2370d-134">Тип данных: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="2370d-134">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="2370d-135">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="2370d-135">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="2370d-136">Не используется.</span><span class="sxs-lookup"><span data-stu-id="2370d-136">Not used.</span></span>

<span data-ttu-id="2370d-137">Это свойство наследуется от [**CIM \_ виртуалсистемсеттингдата**](/previous-versions//cc136954(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="2370d-137">This property is inherited from [**CIM\_VirtualSystemSettingData**](/previous-versions//cc136954(v=vs.85)).</span></span>

</dd> <dt>

<span data-ttu-id="2370d-138">**аутоматикшутдовнактион**</span><span class="sxs-lookup"><span data-stu-id="2370d-138">**AutomaticShutdownAction**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2370d-139">Тип данных: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="2370d-139">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="2370d-140">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="2370d-140">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="2370d-141">Не используется.</span><span class="sxs-lookup"><span data-stu-id="2370d-141">Not used.</span></span>

<span data-ttu-id="2370d-142">Это свойство наследуется от [**CIM \_ виртуалсистемсеттингдата**](/previous-versions//cc136954(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="2370d-142">This property is inherited from [**CIM\_VirtualSystemSettingData**](/previous-versions//cc136954(v=vs.85)).</span></span>

</dd> <dt>

<span data-ttu-id="2370d-143">**аутоматикстартупактион**</span><span class="sxs-lookup"><span data-stu-id="2370d-143">**AutomaticStartupAction**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2370d-144">Тип данных: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="2370d-144">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="2370d-145">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="2370d-145">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="2370d-146">Не используется.</span><span class="sxs-lookup"><span data-stu-id="2370d-146">Not used.</span></span>

<span data-ttu-id="2370d-147">Это свойство наследуется от [**CIM \_ виртуалсистемсеттингдата**](/previous-versions//cc136954(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="2370d-147">This property is inherited from [**CIM\_VirtualSystemSettingData**](/previous-versions//cc136954(v=vs.85)).</span></span>

</dd> <dt>

<span data-ttu-id="2370d-148">**аутоматикстартупактионделай**</span><span class="sxs-lookup"><span data-stu-id="2370d-148">**AutomaticStartupActionDelay**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2370d-149">Тип данных: **DateTime**</span><span class="sxs-lookup"><span data-stu-id="2370d-149">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="2370d-150">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="2370d-150">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="2370d-151">Время задержки перед автоматическим запуском виртуальной машины.</span><span class="sxs-lookup"><span data-stu-id="2370d-151">The delay time before the virtual machine is automatically started up.</span></span> <span data-ttu-id="2370d-152">Это свойство наследуется от [**CIM \_ виртуалсистемсеттингдата**](/previous-versions//cc136954(v=vs.85)), но не используется.</span><span class="sxs-lookup"><span data-stu-id="2370d-152">This property is inherited from [**CIM\_VirtualSystemSettingData**](/previous-versions//cc136954(v=vs.85)), but it is not used.</span></span>

</dd> <dt>

<span data-ttu-id="2370d-153">**аутоматикстартупактионсекуенценумбер**</span><span class="sxs-lookup"><span data-stu-id="2370d-153">**AutomaticStartupActionSequenceNumber**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2370d-154">Тип данных: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="2370d-154">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="2370d-155">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="2370d-155">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="2370d-156">Число, указывающее относительную последовательность активации виртуальной машины при запуске главной системы.</span><span class="sxs-lookup"><span data-stu-id="2370d-156">A number that indicates the relative sequence of virtual machine activation when the host system is started.</span></span> <span data-ttu-id="2370d-157">Это свойство наследуется от [**CIM \_ виртуалсистемсеттингдата**](/previous-versions//cc136954(v=vs.85)), но не используется.</span><span class="sxs-lookup"><span data-stu-id="2370d-157">This property is inherited from [**CIM\_VirtualSystemSettingData**](/previous-versions//cc136954(v=vs.85)), but it is not used.</span></span>

</dd> <dt>

<span data-ttu-id="2370d-158">**ауторесинчронизинаблед**</span><span class="sxs-lookup"><span data-stu-id="2370d-158">**AutoResynchronizeEnabled**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2370d-159">Тип данных: **логический**</span><span class="sxs-lookup"><span data-stu-id="2370d-159">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="2370d-160">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="2370d-160">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="2370d-161">Указывает, будут ли автоматически запускаться операции повторной синхронизации при возникновении ошибки репликации из-за сбоев питания и оборудования.</span><span class="sxs-lookup"><span data-stu-id="2370d-161">Specifies whether resynchronization operations are automatically triggered when a replication error occurs due to power and hardware failures.</span></span> <span data-ttu-id="2370d-162">Операции повторной синхронизации активируются, только когда происходит сбой между временем, заданным в свойствах **ауторесинчронизеинтервалстарт** и **ауторесинчронизеинтерваленд** .</span><span class="sxs-lookup"><span data-stu-id="2370d-162">Resynchronization operations are only triggered when the failure occurs between the times specified by the **AutoResynchronizeIntervalStart** and **AutoResynchronizeIntervalEnd** properties.</span></span>

<span data-ttu-id="2370d-163">Значение по умолчанию равно **False**.</span><span class="sxs-lookup"><span data-stu-id="2370d-163">The default value is **False**.</span></span>

</dd> <dt>

<span data-ttu-id="2370d-164">**ауторесинчронизеинтерваленд**</span><span class="sxs-lookup"><span data-stu-id="2370d-164">**AutoResynchronizeIntervalEnd**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2370d-165">Тип данных: **DateTime**</span><span class="sxs-lookup"><span data-stu-id="2370d-165">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="2370d-166">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="2370d-166">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="2370d-167">Указывает время окончания для запуска автоматических операций повторной синхронизации.</span><span class="sxs-lookup"><span data-stu-id="2370d-167">Specifies the end time for automatic resynchronization operations to be triggered.</span></span> <span data-ttu-id="2370d-168">Это значение указано в местном времени.</span><span class="sxs-lookup"><span data-stu-id="2370d-168">This value is in local time.</span></span> <span data-ttu-id="2370d-169">Значение по умолчанию — 06:00 (6:00 утра).</span><span class="sxs-lookup"><span data-stu-id="2370d-169">The default value is 06:00 (6:00 A.M.).</span></span>

<span data-ttu-id="2370d-170">Операции повторной синхронизации активируются, только когда происходит сбой между временем, заданным в свойствах **ауторесинчронизеинтервалстарт** и **ауторесинчронизеинтерваленд** .</span><span class="sxs-lookup"><span data-stu-id="2370d-170">Resynchronization operations are only triggered when the failure occurs between the times specified by the **AutoResynchronizeIntervalStart** and **AutoResynchronizeIntervalEnd** properties.</span></span>

<span data-ttu-id="2370d-171">Операции повторной синхронизации также можно запланировать, чтобы они запускались в течение следующего интервала.</span><span class="sxs-lookup"><span data-stu-id="2370d-171">Resynchronization operations can also be scheduled so that they are triggered during the next interval.</span></span>

</dd> <dt>

<span data-ttu-id="2370d-172">**ауторесинчронизеинтервалстарт**</span><span class="sxs-lookup"><span data-stu-id="2370d-172">**AutoResynchronizeIntervalStart**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2370d-173">Тип данных: **DateTime**</span><span class="sxs-lookup"><span data-stu-id="2370d-173">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="2370d-174">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="2370d-174">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="2370d-175">Указывает время начала для запуска автоматических операций повторной синхронизации.</span><span class="sxs-lookup"><span data-stu-id="2370d-175">Specifies the start time for automatic resynchronization operations to be triggered.</span></span> <span data-ttu-id="2370d-176">Это значение указано в местном времени.</span><span class="sxs-lookup"><span data-stu-id="2370d-176">This value is in local time.</span></span> <span data-ttu-id="2370d-177">Значение по умолчанию — 18:30 (6:30 вечера).</span><span class="sxs-lookup"><span data-stu-id="2370d-177">The default value is 18:30 (6:30 P.M.).</span></span>

<span data-ttu-id="2370d-178">Операции повторной синхронизации активируются, только когда происходит сбой между временем, заданным в свойствах **ауторесинчронизеинтервалстарт** и **ауторесинчронизеинтерваленд** .</span><span class="sxs-lookup"><span data-stu-id="2370d-178">Resynchronization operations are only triggered when the failure occurs between the times specified by the **AutoResynchronizeIntervalStart** and **AutoResynchronizeIntervalEnd** properties.</span></span>

<span data-ttu-id="2370d-179">Операции повторной синхронизации также можно запланировать, чтобы они запускались в течение следующего интервала.</span><span class="sxs-lookup"><span data-stu-id="2370d-179">Resynchronization operations can also be scheduled so that they are triggered during the next interval.</span></span>

</dd> <dt>

<span data-ttu-id="2370d-180">**бипасспроксисервер**</span><span class="sxs-lookup"><span data-stu-id="2370d-180">**BypassProxyServer**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2370d-181">Тип данных: **логический**</span><span class="sxs-lookup"><span data-stu-id="2370d-181">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="2370d-182">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="2370d-182">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="2370d-183">Указывает, следует ли обходить прокси-сервер при соединении с сервером восстановления.</span><span class="sxs-lookup"><span data-stu-id="2370d-183">Specifies whether the proxy server should be bypassed when connecting to a recovery server.</span></span>

</dd> <dt>

<span data-ttu-id="2370d-184">**Заголовок**</span><span class="sxs-lookup"><span data-stu-id="2370d-184">**Caption**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2370d-185">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="2370d-185">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="2370d-186">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="2370d-186">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="2370d-187">Краткое описание объекта.</span><span class="sxs-lookup"><span data-stu-id="2370d-187">A short description of the object.</span></span> <span data-ttu-id="2370d-188">Это свойство наследуется от [**CIM \_ манажеделемент**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement)и всегда имеет значение "Параметры репликации".</span><span class="sxs-lookup"><span data-stu-id="2370d-188">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement), and it is always set to "Replication Settings".</span></span>

</dd> <dt>

<span data-ttu-id="2370d-189">**CertificateThumbPrint**</span><span class="sxs-lookup"><span data-stu-id="2370d-189">**CertificateThumbPrint**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2370d-190">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="2370d-190">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="2370d-191">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="2370d-191">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="2370d-192">Квалификаторы: [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (128)</span><span class="sxs-lookup"><span data-stu-id="2370d-192">Qualifiers: [**Maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (128)</span></span>
</dt> </dl>

<span data-ttu-id="2370d-193">Отпечаток сертификата, используемый, если свойство **AuthenticationType** использует проверку подлинности на основе сертификата.</span><span class="sxs-lookup"><span data-stu-id="2370d-193">Certificate thumbprint to use when the **AuthenticationType** property is certificate based authentication.</span></span>

</dd> <dt>

<span data-ttu-id="2370d-194">**компрессионенаблед**</span><span class="sxs-lookup"><span data-stu-id="2370d-194">**CompressionEnabled**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2370d-195">Тип данных: **логический**</span><span class="sxs-lookup"><span data-stu-id="2370d-195">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="2370d-196">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="2370d-196">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="2370d-197">Указывает, будут ли сжаты данные репликации во время отправки на сервер восстановления.</span><span class="sxs-lookup"><span data-stu-id="2370d-197">Specifies whether replication data will be compressed while sending it to the recovery server.</span></span>

</dd> <dt>

<span data-ttu-id="2370d-198">**конфигуратиондатарут**</span><span class="sxs-lookup"><span data-stu-id="2370d-198">**ConfigurationDataRoot**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2370d-199">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="2370d-199">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="2370d-200">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="2370d-200">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="2370d-201">Не используется.</span><span class="sxs-lookup"><span data-stu-id="2370d-201">Not used.</span></span>

<span data-ttu-id="2370d-202">Это свойство наследуется от [**CIM \_ виртуалсистемсеттингдата**](/previous-versions//cc136954(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="2370d-202">This property is inherited from [**CIM\_VirtualSystemSettingData**](/previous-versions//cc136954(v=vs.85)).</span></span>

</dd> <dt>

<span data-ttu-id="2370d-203">**Файл ConfigurationFile**</span><span class="sxs-lookup"><span data-stu-id="2370d-203">**ConfigurationFile**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2370d-204">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="2370d-204">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="2370d-205">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="2370d-205">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="2370d-206">Относительный путь и имя файла, в котором хранятся сведения о конфигурации виртуальной машины.</span><span class="sxs-lookup"><span data-stu-id="2370d-206">The relative path and file name of a file where information about the virtual machine configuration is stored.</span></span> <span data-ttu-id="2370d-207">Этот путь задается относительно свойства **конфигуратиондатарут** .</span><span class="sxs-lookup"><span data-stu-id="2370d-207">This path is relative to the **ConfigurationDataRoot** property.</span></span> <span data-ttu-id="2370d-208">Это свойство наследуется от [**CIM \_ виртуалсистемсеттингдата**](/previous-versions//cc136954(v=vs.85)), но не используется.</span><span class="sxs-lookup"><span data-stu-id="2370d-208">This property is inherited from [**CIM\_VirtualSystemSettingData**](/previous-versions//cc136954(v=vs.85)), but it is not used.</span></span>

</dd> <dt>

<span data-ttu-id="2370d-209">**ConfigurationID**</span><span class="sxs-lookup"><span data-stu-id="2370d-209">**ConfigurationID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2370d-210">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="2370d-210">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="2370d-211">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="2370d-211">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="2370d-212">Уникальный идентификатор конфигурации виртуальной машины.</span><span class="sxs-lookup"><span data-stu-id="2370d-212">The unique identifier of the virtual machine configuration.</span></span> <span data-ttu-id="2370d-213">Это свойство наследуется от [**CIM \_ виртуалсистемсеттингдата**](/previous-versions//cc136954(v=vs.85)), но не используется.</span><span class="sxs-lookup"><span data-stu-id="2370d-213">This property is inherited from [**CIM\_VirtualSystemSettingData**](/previous-versions//cc136954(v=vs.85)), but it is not used.</span></span>

</dd> <dt>

<span data-ttu-id="2370d-214">**CreationTime**</span><span class="sxs-lookup"><span data-stu-id="2370d-214">**CreationTime**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2370d-215">Тип данных: **DateTime**</span><span class="sxs-lookup"><span data-stu-id="2370d-215">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="2370d-216">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="2370d-216">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="2370d-217">Дата и время создания параметров виртуальной машины.</span><span class="sxs-lookup"><span data-stu-id="2370d-217">The date and time at which the settings for the virtual machine were created.</span></span> <span data-ttu-id="2370d-218">Если этот объект представляет текущие параметры виртуальной машины, это значение будет соответствовать времени создания системы.</span><span class="sxs-lookup"><span data-stu-id="2370d-218">If this object represents the current settings for the virtual machine, this value would be the time at which the system was created.</span></span> <span data-ttu-id="2370d-219">Если этот объект представляет параметры моментального снимка для виртуальной машины, это значение будет соответствовать времени создания моментального снимка.</span><span class="sxs-lookup"><span data-stu-id="2370d-219">If this object represents the snapshot settings for the virtual machine, this value would be the time at which the snapshot was taken.</span></span> <span data-ttu-id="2370d-220">Это свойство наследуется от [**CIM \_ виртуалсистемсеттингдата**](/previous-versions//cc136954(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="2370d-220">This property is inherited from [**CIM\_VirtualSystemSettingData**](/previous-versions//cc136954(v=vs.85)).</span></span>

<span data-ttu-id="2370d-221">Это свойство доступно только для чтения, но его можно изменить с помощью метода [**модифисистемсеттингс**](modifysystemsettings-msvm-virtualsystemmanagementservice.md) класса [**\_ виртуалсистемманажементсервице мсвм**](msvm-virtualsystemmanagementservice.md) .</span><span class="sxs-lookup"><span data-stu-id="2370d-221">This is a read-only property, but it can be changed by using the [**ModifySystemSettings**](modifysystemsettings-msvm-virtualsystemmanagementservice.md) method of the [**Msvm\_VirtualSystemManagementService**](msvm-virtualsystemmanagementservice.md) class.</span></span>

<span data-ttu-id="2370d-222">Это свойство наследуется от [**CIM \_ виртуалсистемсеттингдата**](/previous-versions//cc136954(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="2370d-222">This property is inherited from [**CIM\_VirtualSystemSettingData**](/previous-versions//cc136954(v=vs.85)).</span></span>

</dd> <dt>

<span data-ttu-id="2370d-223">**Описание**</span><span class="sxs-lookup"><span data-stu-id="2370d-223">**Description**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2370d-224">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="2370d-224">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="2370d-225">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="2370d-225">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="2370d-226">Описание объекта.</span><span class="sxs-lookup"><span data-stu-id="2370d-226">A description of the object.</span></span> <span data-ttu-id="2370d-227">Это свойство наследуется от [**CIM \_ манажеделемент**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement)и всегда имеет значение "данные параметров репликации виртуальной машины".</span><span class="sxs-lookup"><span data-stu-id="2370d-227">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement), and it is always set to "Virtual Machine Replication Settings Data".</span></span>

</dd> <dt>

<span data-ttu-id="2370d-228">**ElementName**</span><span class="sxs-lookup"><span data-stu-id="2370d-228">**ElementName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2370d-229">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="2370d-229">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="2370d-230">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="2370d-230">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="2370d-231">Отображаемое имя объекта.</span><span class="sxs-lookup"><span data-stu-id="2370d-231">A display name for the object.</span></span> <span data-ttu-id="2370d-232">Это свойство наследуется от [**CIM \_ виртуалсистемсеттингдата**](/previous-versions//cc136954(v=vs.85))и для него задается отображаемое имя виртуальной машины.</span><span class="sxs-lookup"><span data-stu-id="2370d-232">This property is inherited from [**CIM\_VirtualSystemSettingData**](/previous-versions//cc136954(v=vs.85)), and it is set to the display name for the virtual machine.</span></span>

</dd> <dt>

<span data-ttu-id="2370d-233">**енаблевритеордерпресерватионакроссдискс**</span><span class="sxs-lookup"><span data-stu-id="2370d-233">**EnableWriteOrderPreservationAcrossDisks**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2370d-234">Тип данных: **логический**</span><span class="sxs-lookup"><span data-stu-id="2370d-234">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="2370d-235">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="2370d-235">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="2370d-236">Квалификаторы: не [**рекомендуется**](/windows/desktop/WmiSdk/standard-wmi-qualifiers) ("нет значения")</span><span class="sxs-lookup"><span data-stu-id="2370d-236">Qualifiers: [**Deprecated**](/windows/desktop/WmiSdk/standard-wmi-qualifiers) ("No value")</span></span>
</dt> </dl>

<span data-ttu-id="2370d-237">Указывает, реплицируются ли все реплицируемые виртуальные жесткие диски виртуальной машины на тот же момент времени.</span><span class="sxs-lookup"><span data-stu-id="2370d-237">Specifies whether all replicating virtual hard disks for the virtual machine are replicated to the same point in time.</span></span> <span data-ttu-id="2370d-238">Это гарантирует, что репликация будет учитывать порядок записи приложений на виртуальной машине.</span><span class="sxs-lookup"><span data-stu-id="2370d-238">This ensures replication honors the write-order of the applications in the virtual machine.</span></span>

<span data-ttu-id="2370d-239">**Windows 8.1:** Начиная с Windows 8.1 и Windows Server 2012 R2 это свойство является устаревшим и всегда имеет значение **true**.</span><span class="sxs-lookup"><span data-stu-id="2370d-239">**Windows 8.1:** Beginning with Windows 8.1 and Windows Server 2012 R2, this property is deprecated and always set to **TRUE**.</span></span>

</dd> <dt>

<span data-ttu-id="2370d-240">**инклудеддискс**</span><span class="sxs-lookup"><span data-stu-id="2370d-240">**IncludedDisks**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2370d-241">Тип данных: массив **строк**</span><span class="sxs-lookup"><span data-stu-id="2370d-241">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="2370d-242">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="2370d-242">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="2370d-243">Квалификаторы: **хипервембеддединстанце** ("CIM \_ сторажеаллокатионсеттингдата"), [**arrayType**](/windows/desktop/WmiSdk/standard-qualifiers) ("индексированный")</span><span class="sxs-lookup"><span data-stu-id="2370d-243">Qualifiers: **HyperVEmbeddedInstance** ("CIM\_StorageAllocationSettingData"), [**ArrayType**](/windows/desktop/WmiSdk/standard-qualifiers) ("Indexed")</span></span>
</dt> </dl>

<span data-ttu-id="2370d-244">Список виртуальных жестких дисков (VHD), подключенных к системе, которые будут реплицироваться подсистемой репликации.</span><span class="sxs-lookup"><span data-stu-id="2370d-244">The list of virtual hard disks (VHDs) attached to the system that will be replicated by the replication engine.</span></span> <span data-ttu-id="2370d-245">Это массив строк, каждый из которых содержит **InstanceId** [**мсвм \_ сторажеаллокатионсеттингдата**](msvm-storageallocationsettingdata.md) , представляющего виртуальный жесткий диск.</span><span class="sxs-lookup"><span data-stu-id="2370d-245">This is an array of strings, each containing the **InstanceID** of the [**Msvm\_StorageAllocationSettingData**](msvm-storageallocationsettingdata.md) that represents the VHD.</span></span>

</dd> <dt>

<span data-ttu-id="2370d-246">**InstanceID**</span><span class="sxs-lookup"><span data-stu-id="2370d-246">**InstanceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2370d-247">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="2370d-247">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="2370d-248">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="2370d-248">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="2370d-249">Квалификаторы: **ключ**</span><span class="sxs-lookup"><span data-stu-id="2370d-249">Qualifiers: **Key**</span></span>
</dt> </dl>

<span data-ttu-id="2370d-250">Уникально идентифицирует экземпляр этого класса.</span><span class="sxs-lookup"><span data-stu-id="2370d-250">Uniquely identifies an instance of this class.</span></span> <span data-ttu-id="2370d-251">Это свойство наследуется [**от \_ SettingData в CIM**](/previous-versions//cc136911(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="2370d-251">This property is inherited from [**CIM\_SettingData**](/previous-versions//cc136911(v=vs.85)).</span></span> <span data-ttu-id="2370d-252">Для Windows 8 всегда устанавливается значение «Microsoft:*GUID* \\ HVR».</span><span class="sxs-lookup"><span data-stu-id="2370d-252">For Windows 8, it is always set to "Microsoft:*Virtual Machine GUID*\\HVR".</span></span> <span data-ttu-id="2370d-253">Для Windows 8.1 задано значение "Microsoft:*GUID виртуальной машины* \\ HVR \\<0/1>".</span><span class="sxs-lookup"><span data-stu-id="2370d-253">For Windows 8.1, it is set to "Microsoft:*Virtual Machine GUID*\\HVR\\<0/1>".</span></span> <span data-ttu-id="2370d-254">В Windows 8.1 значение 0 указывает на первичный, а 1 — на расширенную репликацию.</span><span class="sxs-lookup"><span data-stu-id="2370d-254">In the Windows 8.1 value, 0 indicates primary and 1 indicates extended replication.</span></span> <span data-ttu-id="2370d-255">Дополнительные сведения о расширенной репликации см. в разделе [**мсвм \_ репликатионрелатионшип**](msvm-replicationrelationship.md).</span><span class="sxs-lookup"><span data-stu-id="2370d-255">For more info about extended replication, see [**Msvm\_ReplicationRelationship**](msvm-replicationrelationship.md).</span></span>

</dd> <dt>

<span data-ttu-id="2370d-256">**логдатарут**</span><span class="sxs-lookup"><span data-stu-id="2370d-256">**LogDataRoot**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2370d-257">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="2370d-257">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="2370d-258">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="2370d-258">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="2370d-259">Путь к каталогу, в котором хранится информация журнала для виртуальной машины.</span><span class="sxs-lookup"><span data-stu-id="2370d-259">The path of a directory where log information for the virtual machine is stored.</span></span> <span data-ttu-id="2370d-260">Это свойство наследуется от [**CIM \_ виртуалсистемсеттингдата**](/previous-versions//cc136954(v=vs.85)), но не используется.</span><span class="sxs-lookup"><span data-stu-id="2370d-260">This property is inherited from [**CIM\_VirtualSystemSettingData**](/previous-versions//cc136954(v=vs.85)), but it is not used.</span></span>

</dd> <dt>

<span data-ttu-id="2370d-261">**Примечания**</span><span class="sxs-lookup"><span data-stu-id="2370d-261">**Notes**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2370d-262">Тип данных: массив **строк**</span><span class="sxs-lookup"><span data-stu-id="2370d-262">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="2370d-263">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="2370d-263">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="2370d-264">Не используется и не может быть задано.</span><span class="sxs-lookup"><span data-stu-id="2370d-264">Not used and can't be set.</span></span>

<span data-ttu-id="2370d-265">Это свойство наследуется от [**CIM \_ виртуалсистемсеттингдата**](/previous-versions//cc136954(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="2370d-265">This property is inherited from [**CIM\_VirtualSystemSettingData**](/previous-versions//cc136954(v=vs.85)).</span></span>

</dd> <dt>

<span data-ttu-id="2370d-266">**примариконнектионпоинт**</span><span class="sxs-lookup"><span data-stu-id="2370d-266">**PrimaryConnectionPoint**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2370d-267">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="2370d-267">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="2370d-268">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="2370d-268">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="2370d-269">Квалификаторы: [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (256)</span><span class="sxs-lookup"><span data-stu-id="2370d-269">Qualifiers: [**Maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (256)</span></span>
</dt> </dl>

<span data-ttu-id="2370d-270">Имя основной точки подключения.</span><span class="sxs-lookup"><span data-stu-id="2370d-270">The name of the primary connection point.</span></span> <span data-ttu-id="2370d-271">В случае с основным кластером это имя прикрепления брокера.</span><span class="sxs-lookup"><span data-stu-id="2370d-271">In the case of a primary cluster, this is the broker CAP name.</span></span> <span data-ttu-id="2370d-272">В случае автономного сервера-источника это имя системы узла.</span><span class="sxs-lookup"><span data-stu-id="2370d-272">In the case of a standalone primary server, this is the host system name.</span></span>

</dd> <dt>

<span data-ttu-id="2370d-273">**примарихостсистем**</span><span class="sxs-lookup"><span data-stu-id="2370d-273">**PrimaryHostSystem**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2370d-274">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="2370d-274">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="2370d-275">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="2370d-275">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="2370d-276">Квалификаторы: [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (256)</span><span class="sxs-lookup"><span data-stu-id="2370d-276">Qualifiers: [**Maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (256)</span></span>
</dt> </dl>

<span data-ttu-id="2370d-277">Полное доменное имя основной хост-системы, в которой размещается виртуальная машина.</span><span class="sxs-lookup"><span data-stu-id="2370d-277">The fully qualified domain name of the primary host system that is hosting the virtual machine.</span></span>

</dd> <dt>

<span data-ttu-id="2370d-278">**рековериконнектионпоинт**</span><span class="sxs-lookup"><span data-stu-id="2370d-278">**RecoveryConnectionPoint**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2370d-279">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="2370d-279">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="2370d-280">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="2370d-280">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="2370d-281">Квалификаторы: [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (256)</span><span class="sxs-lookup"><span data-stu-id="2370d-281">Qualifiers: [**Maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (256)</span></span>
</dt> </dl>

<span data-ttu-id="2370d-282">Имя точки подключения для восстановления.</span><span class="sxs-lookup"><span data-stu-id="2370d-282">The name of the recovery connection point.</span></span> <span data-ttu-id="2370d-283">В случае кластера восстановления это имя ограничения брокера.</span><span class="sxs-lookup"><span data-stu-id="2370d-283">In the case of a recovery cluster, this is the broker CAP name.</span></span> <span data-ttu-id="2370d-284">В случае с автономным сервером восстановления это имя системы узла.</span><span class="sxs-lookup"><span data-stu-id="2370d-284">In the case of a standalone recovery server, this is the host system name.</span></span>

</dd> <dt>

<span data-ttu-id="2370d-285">**рековерифиле**</span><span class="sxs-lookup"><span data-stu-id="2370d-285">**RecoveryFile**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2370d-286">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="2370d-286">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="2370d-287">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="2370d-287">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="2370d-288">Полный путь к файлу, в котором хранится информация, связанная с восстановлением для виртуальной машины.</span><span class="sxs-lookup"><span data-stu-id="2370d-288">The full path of a file where recovery related information for the virtual machine is stored.</span></span> <span data-ttu-id="2370d-289">Это свойство наследуется от [**CIM \_ виртуалсистемсеттингдата**](/previous-versions//cc136954(v=vs.85)), но не используется.</span><span class="sxs-lookup"><span data-stu-id="2370d-289">This property is inherited from [**CIM\_VirtualSystemSettingData**](/previous-versions//cc136954(v=vs.85)), but it is not used.</span></span>

</dd> <dt>

<span data-ttu-id="2370d-290">**рековерихистори**</span><span class="sxs-lookup"><span data-stu-id="2370d-290">**RecoveryHistory**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2370d-291">Тип данных: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="2370d-291">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="2370d-292">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="2370d-292">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="2370d-293">Максимальное число моментальных снимков восстановления, которые будут храниться на сервере восстановления.</span><span class="sxs-lookup"><span data-stu-id="2370d-293">The maximum number of recovery snapshots that will be stored on the recovery server.</span></span> <span data-ttu-id="2370d-294">Допустимые значения: от 0 до 24.</span><span class="sxs-lookup"><span data-stu-id="2370d-294">Valid values are from 0 to 24.</span></span>

</dd> <dt>

<span data-ttu-id="2370d-295">**рековерихостсистем**</span><span class="sxs-lookup"><span data-stu-id="2370d-295">**RecoveryHostSystem**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2370d-296">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="2370d-296">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="2370d-297">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="2370d-297">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="2370d-298">Квалификаторы: [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (256)</span><span class="sxs-lookup"><span data-stu-id="2370d-298">Qualifiers: [**Maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (256)</span></span>
</dt> </dl>

<span data-ttu-id="2370d-299">Полное доменное имя системы узла восстановления, в которой размещается виртуальная машина.</span><span class="sxs-lookup"><span data-stu-id="2370d-299">The fully qualified domain name of the recovery host system which is hosting the virtual machine.</span></span>

</dd> <dt>

<span data-ttu-id="2370d-300">**рековерисерверпортнумбер**</span><span class="sxs-lookup"><span data-stu-id="2370d-300">**RecoveryServerPortNumber**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2370d-301">Тип данных: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="2370d-301">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="2370d-302">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="2370d-302">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="2370d-303">Номер порта сервера восстановления, используемый при обеспечении безопасного подключения для репликации.</span><span class="sxs-lookup"><span data-stu-id="2370d-303">The recovery server port number to use when making a secure connection for replication.</span></span>

</dd> <dt>

<span data-ttu-id="2370d-304">**репликатехостквпитемс**</span><span class="sxs-lookup"><span data-stu-id="2370d-304">**ReplicateHostKvpItems**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2370d-305">Тип данных: **логический**</span><span class="sxs-lookup"><span data-stu-id="2370d-305">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="2370d-306">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="2370d-306">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="2370d-307">Указывает, следует ли реплицировать [**мсвм \_ квпексчанжедатаитем**](msvm-kvpexchangedataitem.md)(только для узла) с основной виртуальной машины на виртуальную машину восстановления.</span><span class="sxs-lookup"><span data-stu-id="2370d-307">Specifies whether host-only [**Msvm\_KvpExchangeDataItem**](msvm-kvpexchangedataitem.md)s should be replicated from the primary virtual machine to the recovery virtual machine.</span></span>

</dd> <dt>

<span data-ttu-id="2370d-308">**ReplicationInterval**</span><span class="sxs-lookup"><span data-stu-id="2370d-308">**ReplicationInterval**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2370d-309">Тип данных: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="2370d-309">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="2370d-310">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="2370d-310">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="2370d-311">Интервал репликации отношения репликации в секундах.</span><span class="sxs-lookup"><span data-stu-id="2370d-311">Replication interval of a replication relationship in seconds.</span></span> <span data-ttu-id="2370d-312">Допустимые значения:</span><span class="sxs-lookup"><span data-stu-id="2370d-312">Valid values are:</span></span>

<span data-ttu-id="2370d-313">30</span><span class="sxs-lookup"><span data-stu-id="2370d-313">30</span></span>

<span data-ttu-id="2370d-314">300</span><span class="sxs-lookup"><span data-stu-id="2370d-314">300</span></span>

<span data-ttu-id="2370d-315">900</span><span class="sxs-lookup"><span data-stu-id="2370d-315">900</span></span>

<span data-ttu-id="2370d-316">Значение по умолчанию — 300 секунд.</span><span class="sxs-lookup"><span data-stu-id="2370d-316">Default value is 300 seconds.</span></span>

<span data-ttu-id="2370d-317">**Windows 8.1:** Это значение не поддерживается до Windows 8.1 и Windows Server 2012 R2.</span><span class="sxs-lookup"><span data-stu-id="2370d-317">**Windows 8.1:** This value is not supported until Windows 8.1 and Windows Server 2012 R2.</span></span>

</dd> <dt>

<span data-ttu-id="2370d-318">**репликатионпровидер**</span><span class="sxs-lookup"><span data-stu-id="2370d-318">**ReplicationProvider**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2370d-319">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="2370d-319">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="2370d-320">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="2370d-320">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="2370d-321">Путь к экземпляру класса [**мсвм \_ репликатионпровидер**](msvm-replicationprovider.md) , который идентифицирует конечную точку поставщика репликации.</span><span class="sxs-lookup"><span data-stu-id="2370d-321">The path to the instance of the [**Msvm\_ReplicationProvider**](msvm-replicationprovider.md) class that identifies the replication provider endpoint.</span></span>

<span data-ttu-id="2370d-322">**Windows 8.1:** Это значение не поддерживается до Windows 8.1 и Windows Server 2012 R2.</span><span class="sxs-lookup"><span data-stu-id="2370d-322">**Windows 8.1:** This value is not supported until Windows 8.1 and Windows Server 2012 R2.</span></span>

</dd> <dt>

<span data-ttu-id="2370d-323">**рутцертификатесумбпринт**</span><span class="sxs-lookup"><span data-stu-id="2370d-323">**RootCertificateThumbPrint**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2370d-324">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="2370d-324">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="2370d-325">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="2370d-325">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="2370d-326">Квалификаторы: [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (128)</span><span class="sxs-lookup"><span data-stu-id="2370d-326">Qualifiers: [**Maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (128)</span></span>
</dt> </dl>

<span data-ttu-id="2370d-327">Отпечаток корневого сертификата в используемом сертификате, если **AuthenticationType** имеет значение 2 (авторизация на основе сертификата).</span><span class="sxs-lookup"><span data-stu-id="2370d-327">Root certificate thumbprint of the certificate in use when **AuthenticationType** is 2 (certificate based authorization).</span></span>

</dd> <dt>

<span data-ttu-id="2370d-328">**снапшотдатарут**</span><span class="sxs-lookup"><span data-stu-id="2370d-328">**SnapshotDataRoot**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2370d-329">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="2370d-329">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="2370d-330">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="2370d-330">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="2370d-331">Путь к каталогу, в котором хранятся сведения о моментальных снимках виртуальной машины.</span><span class="sxs-lookup"><span data-stu-id="2370d-331">The path of a directory where information about the virtual machine snapshots is stored.</span></span> <span data-ttu-id="2370d-332">Это свойство наследуется от [**CIM \_ виртуалсистемсеттингдата**](/previous-versions//cc136954(v=vs.85)), но не используется.</span><span class="sxs-lookup"><span data-stu-id="2370d-332">This property is inherited from [**CIM\_VirtualSystemSettingData**](/previous-versions//cc136954(v=vs.85)), but it is not used.</span></span>

</dd> <dt>

<span data-ttu-id="2370d-333">**суспенддатарут**</span><span class="sxs-lookup"><span data-stu-id="2370d-333">**SuspendDataRoot**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2370d-334">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="2370d-334">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="2370d-335">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="2370d-335">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="2370d-336">Путь к каталогу, в котором хранятся сведения о приостановке виртуальной машины.</span><span class="sxs-lookup"><span data-stu-id="2370d-336">The path of a directory where information about the virtual machine suspend-related information is stored.</span></span> <span data-ttu-id="2370d-337">Это свойство наследуется от [**CIM \_ виртуалсистемсеттингдата**](/previous-versions//cc136954(v=vs.85)), но не используется.</span><span class="sxs-lookup"><span data-stu-id="2370d-337">This property is inherited from [**CIM\_VirtualSystemSettingData**](/previous-versions//cc136954(v=vs.85)), but it is not used.</span></span>

</dd> <dt>

<span data-ttu-id="2370d-338">**свапфиледатарут**</span><span class="sxs-lookup"><span data-stu-id="2370d-338">**SwapFileDataRoot**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2370d-339">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="2370d-339">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="2370d-340">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="2370d-340">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="2370d-341">Путь к каталогу, в котором хранятся файлы подкачки для виртуальной машины.</span><span class="sxs-lookup"><span data-stu-id="2370d-341">The path of a directory where swap files for the virtual machine are stored.</span></span> <span data-ttu-id="2370d-342">Это свойство наследуется от [**CIM \_ виртуалсистемсеттингдата**](/previous-versions//cc136954(v=vs.85)), но не используется.</span><span class="sxs-lookup"><span data-stu-id="2370d-342">This property is inherited from [**CIM\_VirtualSystemSettingData**](/previous-versions//cc136954(v=vs.85)), but it is not used.</span></span>

</dd> <dt>

<span data-ttu-id="2370d-343">**виртуалсистемидентифиер**</span><span class="sxs-lookup"><span data-stu-id="2370d-343">**VirtualSystemIdentifier**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2370d-344">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="2370d-344">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="2370d-345">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="2370d-345">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="2370d-346">Имя объекта [**CIM \_ ComputerSystem**](/windows/desktop/CIMWin32Prov/cim-computersystem) , которому принадлежат данные этого параметра.</span><span class="sxs-lookup"><span data-stu-id="2370d-346">The name of the [**CIM\_ComputerSystem**](/windows/desktop/CIMWin32Prov/cim-computersystem) object to which this setting data belongs.</span></span> <span data-ttu-id="2370d-347">Это свойство является переопределением из [**CIM \_ виртуалсистемсеттингдата**](/previous-versions//cc136954(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="2370d-347">This property is an override from [**CIM\_VirtualSystemSettingData**](/previous-versions//cc136954(v=vs.85)).</span></span>

</dd> <dt>

<span data-ttu-id="2370d-348">**виртуалсистемтипе**</span><span class="sxs-lookup"><span data-stu-id="2370d-348">**VirtualSystemType**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2370d-349">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="2370d-349">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="2370d-350">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="2370d-350">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="2370d-351">Указывает тип виртуальной машины, которую представляют данные параметров.</span><span class="sxs-lookup"><span data-stu-id="2370d-351">Specifies the type of virtual machine the setting data represents.</span></span> <span data-ttu-id="2370d-352">Это свойство наследуется от [**CIM \_ виртуалсистемсеттингдата**](/previous-versions//cc136954(v=vs.85))и всегда имеет значение "Microsoft: Hyper-V: Реплика".</span><span class="sxs-lookup"><span data-stu-id="2370d-352">This property is inherited from [**CIM\_VirtualSystemSettingData**](/previous-versions//cc136954(v=vs.85)), and it is always set to "Microsoft:Hyper-V:Replica".</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="2370d-353">Требования</span><span class="sxs-lookup"><span data-stu-id="2370d-353">Requirements</span></span>



| <span data-ttu-id="2370d-354">Требование</span><span class="sxs-lookup"><span data-stu-id="2370d-354">Requirement</span></span> | <span data-ttu-id="2370d-355">Значение</span><span class="sxs-lookup"><span data-stu-id="2370d-355">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="2370d-356">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="2370d-356">Minimum supported client</span></span><br/> | <span data-ttu-id="2370d-357">\[Только классические приложения Windows 8\]</span><span class="sxs-lookup"><span data-stu-id="2370d-357">Windows 8 \[desktop apps only\]</span></span><br/>                                                              |
| <span data-ttu-id="2370d-358">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="2370d-358">Minimum supported server</span></span><br/> | <span data-ttu-id="2370d-359">\[Только для настольных приложений Windows Server 2012\]</span><span class="sxs-lookup"><span data-stu-id="2370d-359">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="2370d-360">Пространство имен</span><span class="sxs-lookup"><span data-stu-id="2370d-360">Namespace</span></span><br/>                | <span data-ttu-id="2370d-361">Корневая \\ виртуализация \\ версии 2</span><span class="sxs-lookup"><span data-stu-id="2370d-361">Root\\Virtualization\\V2</span></span><br/>                                                                     |
| <span data-ttu-id="2370d-362">MOF</span><span class="sxs-lookup"><span data-stu-id="2370d-362">MOF</span></span><br/>                      | <dl> <span data-ttu-id="2370d-363"><dt>Виндовсвиртуализатион. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="2370d-363"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="2370d-364">DLL</span><span class="sxs-lookup"><span data-stu-id="2370d-364">DLL</span></span><br/>                      | <dl> <span data-ttu-id="2370d-365"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="2370d-365"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="2370d-366">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="2370d-366">See also</span></span>

<dl> <dt>

[<span data-ttu-id="2370d-367">**\_ВИРТУАЛСИСТЕМСЕТТИНГДАТА CIM**</span><span class="sxs-lookup"><span data-stu-id="2370d-367">**CIM\_VirtualSystemSettingData**</span></span>](cim-virtualsystemsettingdata.md)
</dt> <dt>

[<span data-ttu-id="2370d-368">**модифирепликатионсеттингс**</span><span class="sxs-lookup"><span data-stu-id="2370d-368">**ModifyReplicationSettings**</span></span>](modifyreplicationsettings-msvm-replicationservice.md)
</dt> </dl>

 

