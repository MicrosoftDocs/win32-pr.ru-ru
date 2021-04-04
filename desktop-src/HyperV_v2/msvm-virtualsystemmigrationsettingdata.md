---
description: Представляет параметры миграции для миграции виртуальной системы и хранилища, подключенного к виртуальной системе.
ms.assetid: 2d632fe2-31ee-4e4d-b2a6-c1d1f3b4d624
title: Класс Msvm_VirtualSystemMigrationSettingData
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_VirtualSystemMigrationSettingData
- Msvm_VirtualSystemMigrationSettingData.InstanceID
- Msvm_VirtualSystemMigrationSettingData.Caption
- Msvm_VirtualSystemMigrationSettingData.Description
- Msvm_VirtualSystemMigrationSettingData.ElementName
- Msvm_VirtualSystemMigrationSettingData.MigrationType
- Msvm_VirtualSystemMigrationSettingData.Priority
- Msvm_VirtualSystemMigrationSettingData.Bandwidth
- Msvm_VirtualSystemMigrationSettingData.BandwidthUnit
- Msvm_VirtualSystemMigrationSettingData.OtherTransportType
- Msvm_VirtualSystemMigrationSettingData.TransportType
- Msvm_VirtualSystemMigrationSettingData.RemoveSourceUnmanagedVhds
- Msvm_VirtualSystemMigrationSettingData.AvoidRemovingVHDs
- Msvm_VirtualSystemMigrationSettingData.CPUCappingMagnitude
- Msvm_VirtualSystemMigrationSettingData.CancelIfBlackoutThresholdExceeded
- Msvm_VirtualSystemMigrationSettingData.AllowOverwriteExistingFile
- Msvm_VirtualSystemMigrationSettingData.UnmanagedVhds
- Msvm_VirtualSystemMigrationSettingData.DestinationPlannedVirtualSystemId
- Msvm_VirtualSystemMigrationSettingData.DestinationIPAddressList
- Msvm_VirtualSystemMigrationSettingData.RetainVhdCopiesOnSource
- Msvm_VirtualSystemMigrationSettingData.EnableCompression
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: 254884153b3f733691b1103a6eb57f204b5d1764
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "103896822"
---
# <a name="msvm_virtualsystemmigrationsettingdata-class"></a><span data-ttu-id="e9dea-103">\_Класс мсвм виртуалсистеммигратионсеттингдата</span><span class="sxs-lookup"><span data-stu-id="e9dea-103">Msvm\_VirtualSystemMigrationSettingData class</span></span>

<span data-ttu-id="e9dea-104">Представляет параметры миграции для миграции виртуальной системы и хранилища, подключенного к виртуальной системе.</span><span class="sxs-lookup"><span data-stu-id="e9dea-104">Represents the migration settings for migrating a virtual system and the storage attached to a virtual system.</span></span>

<span data-ttu-id="e9dea-105">Следующий синтаксис является упрощенным MOF-файлным (MOF) кодом и включает все наследуемые свойства.</span><span class="sxs-lookup"><span data-stu-id="e9dea-105">The following syntax is simplified Managed Object Format (MOF) code, and it includes all of the inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="e9dea-106">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="e9dea-106">Syntax</span></span>

``` syntax
[Dynamic, Provider("VmmsWmiInstanceAndMethodProvider"), AMENDMENT]
class Msvm_VirtualSystemMigrationSettingData : CIM_VirtualSystemMigrationSettingData
{
  string  InstanceID;
  string  Caption = "Migration Setting Data";
  string  Description = "Virtual System Migration Setting Data";
  string  ElementName;
  uint16  MigrationType;
  uint16  Priority;
  uint16  Bandwidth;
  string  BandwidthUnit;
  string  OtherTransportType;
  uint16  TransportType;
  boolean RemoveSourceUnmanagedVhds;
  boolean AvoidRemovingVHDs;
  uint16  CPUCappingMagnitude;
  boolean CancelIfBlackoutThresholdExceeded;
  boolean AllowOverwriteExistingFile;
  string  UnmanagedVhds[];
  string  DestinationPlannedVirtualSystemId;
  string  DestinationIPAddressList[];
  boolean RetainVhdCopiesOnSource;
  boolean EnableCompression;
};
```

## <a name="members"></a><span data-ttu-id="e9dea-107">Члены</span><span class="sxs-lookup"><span data-stu-id="e9dea-107">Members</span></span>

<span data-ttu-id="e9dea-108">Класс **мсвм \_ виртуалсистеммигратионсеттингдата** имеет следующие типы членов:</span><span class="sxs-lookup"><span data-stu-id="e9dea-108">The **Msvm\_VirtualSystemMigrationSettingData** class has these types of members:</span></span>

-   [<span data-ttu-id="e9dea-109">Свойства</span><span class="sxs-lookup"><span data-stu-id="e9dea-109">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="e9dea-110">Свойства</span><span class="sxs-lookup"><span data-stu-id="e9dea-110">Properties</span></span>

<span data-ttu-id="e9dea-111">Класс **мсвм \_ виртуалсистеммигратионсеттингдата** имеет следующие свойства.</span><span class="sxs-lookup"><span data-stu-id="e9dea-111">The **Msvm\_VirtualSystemMigrationSettingData** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="e9dea-112">**аллововервритиксистингфиле**</span><span class="sxs-lookup"><span data-stu-id="e9dea-112">**AllowOverwriteExistingFile**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e9dea-113">Тип данных: **логический**</span><span class="sxs-lookup"><span data-stu-id="e9dea-113">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="e9dea-114">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="e9dea-114">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="e9dea-115">Разрешить операции миграции хранилища перезаписывать существующие VHDX-файлы.</span><span class="sxs-lookup"><span data-stu-id="e9dea-115">Allow the storage migration operation to overwrite existing .vhdx files.</span></span>

> [!Note]  
> <span data-ttu-id="e9dea-116">Это свойство было добавлено в Windows 10 версии 1703.</span><span class="sxs-lookup"><span data-stu-id="e9dea-116">This property was added in Windows 10, version 1703.</span></span>

 

</dd> <dt>

<span data-ttu-id="e9dea-117">**авоидремовингвхдс**</span><span class="sxs-lookup"><span data-stu-id="e9dea-117">**AvoidRemovingVHDs**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e9dea-118">Тип данных: **логический**</span><span class="sxs-lookup"><span data-stu-id="e9dea-118">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="e9dea-119">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="e9dea-119">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="e9dea-120">Не удаляйте виртуальные жесткие диски во время миграции, т. е. виртуальные жесткие диски в источнике на сукцессанд виртуальных жестких дисках в случае сбоя.</span><span class="sxs-lookup"><span data-stu-id="e9dea-120">Do not remove any VHDs during the migration, i.e. VHDs on the source in successand VHDs on the destination in failure.</span></span>

> [!Note]  
> <span data-ttu-id="e9dea-121">Добавлено в Windows 10, версии 1703 и Windows Server 2016.</span><span class="sxs-lookup"><span data-stu-id="e9dea-121">Added in Windows 10, version 1703 and Windows Server 2016.</span></span>

 

</dd> <dt>

<span data-ttu-id="e9dea-122">**Пропускная способность**</span><span class="sxs-lookup"><span data-stu-id="e9dea-122">**Bandwidth**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e9dea-123">Тип данных: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="e9dea-123">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="e9dea-124">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="e9dea-124">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="e9dea-125">Указывает пропускную способность, назначенную или запрошенную для операции миграции виртуальной системы.</span><span class="sxs-lookup"><span data-stu-id="e9dea-125">Specifies the bandwidth assigned to or requested for a virtual system migration operation.</span></span> <span data-ttu-id="e9dea-126">Единицы пропускной способности задаются свойством **бандвидсунит** .</span><span class="sxs-lookup"><span data-stu-id="e9dea-126">The bandwidth units are specified by the **BandwidthUnit** property.</span></span> <span data-ttu-id="e9dea-127">В рамках миграции значение 0 указывает пропускную способность по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="e9dea-127">Within a migration, a value of 0 indicates the default bandwidth.</span></span> <span data-ttu-id="e9dea-128">В противном случае значение 0 указывает, что пропускная способность не поддерживается.</span><span class="sxs-lookup"><span data-stu-id="e9dea-128">Otherwise, a value of 0 indicates that bandwidths are not supported.</span></span>

<span data-ttu-id="e9dea-129">**Пропускную способность** и **приоритет** можно использовать в сочетании.</span><span class="sxs-lookup"><span data-stu-id="e9dea-129">**Bandwidth** and **Priority** can be used in conjunction.</span></span> <span data-ttu-id="e9dea-130">Процессы миграции, имеющие наивысшее значение приоритета, совместно используют доступную пропускную способность в зависимости от запрошенной пропускной способности.</span><span class="sxs-lookup"><span data-stu-id="e9dea-130">Migration processes that have the highest equal priority value share the available bandwidth based on their requested bandwidth.</span></span> <span data-ttu-id="e9dea-131">Если этот набор процессов потребляет не всю пропускную способность, процессы миграции со следующим меньшим приоритетом совместно используют оставшуюся пропускную способность.</span><span class="sxs-lookup"><span data-stu-id="e9dea-131">If not all bandwidth is consumed by this set of processes, migration processes with the next lower equal priority share the remaining bandwidth.</span></span> <span data-ttu-id="e9dea-132">Если по-прежнему пропускная способность остается, рассматриваются процессы миграции со следующим меньшим приоритетом и т. д.</span><span class="sxs-lookup"><span data-stu-id="e9dea-132">If still more bandwidth remains, migration processes with the next lower equal priority are considered, and so forth.</span></span>

<span data-ttu-id="e9dea-133">Это свойство наследуется от **CIM \_ виртуалсистеммигратионсеттингдата**.</span><span class="sxs-lookup"><span data-stu-id="e9dea-133">This property is inherited from **CIM\_VirtualSystemMigrationSettingData**.</span></span>

</dd> <dt>

<span data-ttu-id="e9dea-134">**бандвидсунит**</span><span class="sxs-lookup"><span data-stu-id="e9dea-134">**BandwidthUnit**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e9dea-135">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="e9dea-135">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="e9dea-136">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="e9dea-136">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="e9dea-137">Указывает единицы, используемые свойством **пропускной способности** .</span><span class="sxs-lookup"><span data-stu-id="e9dea-137">Specifies the units used by the **Bandwidth** property.</span></span> <span data-ttu-id="e9dea-138">Значение этого свойства должно быть допустимым значением квалификатора программных единиц, как определено в приложении C. 1 DSP0004 V 2.4 или более поздней версии.</span><span class="sxs-lookup"><span data-stu-id="e9dea-138">The value of this property must be a legal value of the Programmatic Units qualifier as defined in Appendix C.1 of DSP0004 V2.4 or later.</span></span>

<span data-ttu-id="e9dea-139">Если значение этого свойства равно "Percent", значение свойства **пропускной способности** должно находиться в диапазоне от 0 до 100 с более высокими значениями, указывающими на более высокую пропускную способность.</span><span class="sxs-lookup"><span data-stu-id="e9dea-139">If the value of this property is "percent", the value of the **Bandwidth** property must be between 0 and 100, with higher values indicating a higher bandwidth.</span></span> <span data-ttu-id="e9dea-140">Значение 100 указывает общую доступную пропускную способность для выполнения операций миграции виртуальной системы.</span><span class="sxs-lookup"><span data-stu-id="e9dea-140">A value of 100 indicates the total available bandwidth for performing virtual system migration operations.</span></span> <span data-ttu-id="e9dea-141">Значения от 1 до 100 должны линейно сопоставляться с доступным диапазоном пропускной способности.</span><span class="sxs-lookup"><span data-stu-id="e9dea-141">Values between 1 and 100 should linearly correlate with the available bandwidth range.</span></span> <span data-ttu-id="e9dea-142">Например, значение 50 должно запрашивать половину доступной пропускной способности.</span><span class="sxs-lookup"><span data-stu-id="e9dea-142">For example, a value of 50 should request half of the available bandwidth.</span></span>

<span data-ttu-id="e9dea-143">Это свойство наследуется от **CIM \_ виртуалсистеммигратионсеттингдата**.</span><span class="sxs-lookup"><span data-stu-id="e9dea-143">This property is inherited from **CIM\_VirtualSystemMigrationSettingData**.</span></span>

</dd> <dt>

<span data-ttu-id="e9dea-144">**канцелифблаккаутсрешолдексцеедед**</span><span class="sxs-lookup"><span data-stu-id="e9dea-144">**CancelIfBlackoutThresholdExceeded**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e9dea-145">Тип данных: **логический**</span><span class="sxs-lookup"><span data-stu-id="e9dea-145">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="e9dea-146">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="e9dea-146">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="e9dea-147">Отменяет миграцию, если превышено пороговое значение времени ожидания.</span><span class="sxs-lookup"><span data-stu-id="e9dea-147">Cancels migration if the blackout threshold time is exceeded.</span></span>

> [!Note]  
> <span data-ttu-id="e9dea-148">Добавлено в Windows 10 версии 1709.</span><span class="sxs-lookup"><span data-stu-id="e9dea-148">Added in Windows 10, version 1709.</span></span>

 

</dd> <dt>

<span data-ttu-id="e9dea-149">**Заголовок**</span><span class="sxs-lookup"><span data-stu-id="e9dea-149">**Caption**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e9dea-150">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="e9dea-150">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="e9dea-151">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="e9dea-151">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="e9dea-152">Краткое описание объекта.</span><span class="sxs-lookup"><span data-stu-id="e9dea-152">A short description of the object.</span></span> <span data-ttu-id="e9dea-153">Это свойство наследуется от [**CIM \_ манажеделемент**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span><span class="sxs-lookup"><span data-stu-id="e9dea-153">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span></span>

</dd> <dt>

<span data-ttu-id="e9dea-154">**кпукаппингмагнитуде**</span><span class="sxs-lookup"><span data-stu-id="e9dea-154">**CPUCappingMagnitude**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e9dea-155">Тип данных: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="e9dea-155">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="e9dea-156">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="e9dea-156">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="e9dea-157">Квалификаторы: [**override**](/windows/desktop/WmiSdk/standard-qualifiers) ("кпукаппингмагнитуде")</span><span class="sxs-lookup"><span data-stu-id="e9dea-157">Qualifiers: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("CPUCappingMagnitude")</span></span>
</dt> </dl>

<span data-ttu-id="e9dea-158">Степень выделения ЦП во время миграции.</span><span class="sxs-lookup"><span data-stu-id="e9dea-158">Degree of CPU capping during migration.</span></span>

> [!Note]  
> <span data-ttu-id="e9dea-159">Добавлено в Windows 10 версии 1709.</span><span class="sxs-lookup"><span data-stu-id="e9dea-159">Added in Windows 10, version 1709.</span></span>

 

<dt>

<span id="Normal"></span><span id="normal"></span><span id="NORMAL"></span>

<span data-ttu-id="e9dea-160">**Обычная** (0)</span><span class="sxs-lookup"><span data-stu-id="e9dea-160">**Normal** (0)</span></span>


</dt> <dd></dd> <dt>

<span id="Low"></span><span id="low"></span><span id="LOW"></span>

<span data-ttu-id="e9dea-161">**Низкая** (1)</span><span class="sxs-lookup"><span data-stu-id="e9dea-161">**Low** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="High"></span><span id="high"></span><span id="HIGH"></span>

<span data-ttu-id="e9dea-162">**Высокий** (2)</span><span class="sxs-lookup"><span data-stu-id="e9dea-162">**High** (2)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="e9dea-163">**Описание**</span><span class="sxs-lookup"><span data-stu-id="e9dea-163">**Description**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e9dea-164">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="e9dea-164">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="e9dea-165">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="e9dea-165">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="e9dea-166">Описание объекта.</span><span class="sxs-lookup"><span data-stu-id="e9dea-166">A description of the object.</span></span> <span data-ttu-id="e9dea-167">Это свойство наследуется от [**CIM \_ манажеделемент**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span><span class="sxs-lookup"><span data-stu-id="e9dea-167">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span></span>

</dd> <dt>

<span data-ttu-id="e9dea-168">**дестинатионипаддресслист**</span><span class="sxs-lookup"><span data-stu-id="e9dea-168">**DestinationIPAddressList**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e9dea-169">Тип данных: массив **строк**</span><span class="sxs-lookup"><span data-stu-id="e9dea-169">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="e9dea-170">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="e9dea-170">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="e9dea-171">Это значение будет **равно NULL** для миграции хранилища.</span><span class="sxs-lookup"><span data-stu-id="e9dea-171">This will be **Null** for storage migration.</span></span> <span data-ttu-id="e9dea-172">Для миграции виртуальной системы это может содержать список IP-адресов узла назначения.</span><span class="sxs-lookup"><span data-stu-id="e9dea-172">For virtual system migration, this can contain a list of IP addresses of the destination host.</span></span>

</dd> <dt>

<span data-ttu-id="e9dea-173">**дестинатионпланнедвиртуалсистемид**</span><span class="sxs-lookup"><span data-stu-id="e9dea-173">**DestinationPlannedVirtualSystemId**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e9dea-174">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="e9dea-174">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="e9dea-175">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="e9dea-175">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="e9dea-176">Если запланированная виртуальная машина существует в месте назначения миграции, для этого свойства будет задан идентификатор GUID целевой виртуальной машины, на которой требуется выполнить миграцию виртуальной машины.</span><span class="sxs-lookup"><span data-stu-id="e9dea-176">If a planned virtual machine exists at the migration destination, this property will be set to the GUID of the destination planned virtual machine where the virtual machine needs to migrate.</span></span> <span data-ttu-id="e9dea-177">Это полезно в случаях, когда пользователь создал запланированную виртуальную машину в месте назначения, а также настройку ресурсов и хочет, чтобы виртуальная машина из источника была перенесена на эту запланированную виртуальную машину.</span><span class="sxs-lookup"><span data-stu-id="e9dea-177">This is useful for cases where a user has created a planned virtual machine at the destination, along with resource setup, and wants a virtual machine from the source to migrate into this planned virtual machine.</span></span>

</dd> <dt>

<span data-ttu-id="e9dea-178">**ElementName**</span><span class="sxs-lookup"><span data-stu-id="e9dea-178">**ElementName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e9dea-179">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="e9dea-179">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="e9dea-180">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="e9dea-180">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="e9dea-181">Отображаемое имя объекта.</span><span class="sxs-lookup"><span data-stu-id="e9dea-181">A display name for the object.</span></span> <span data-ttu-id="e9dea-182">Это свойство наследуется [**от \_ SettingData в CIM**](/previous-versions//cc136911(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="e9dea-182">This property is inherited from [**CIM\_SettingData**](/previous-versions//cc136911(v=vs.85)).</span></span>

</dd> <dt>

<span data-ttu-id="e9dea-183">**EnableCompression**</span><span class="sxs-lookup"><span data-stu-id="e9dea-183">**EnableCompression**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e9dea-184">Тип данных: **логический**</span><span class="sxs-lookup"><span data-stu-id="e9dea-184">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="e9dea-185">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="e9dea-185">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="e9dea-186">Указывает, следует ли сжимать трафик динамической миграции.</span><span class="sxs-lookup"><span data-stu-id="e9dea-186">Indicates whether to compress the live migration traffic.</span></span> <span data-ttu-id="e9dea-187">**Значение true** указывает, что необходимо сжать; в противном случае — **false**.</span><span class="sxs-lookup"><span data-stu-id="e9dea-187">**True** indicates to compress; otherwise **False**.</span></span>

<span data-ttu-id="e9dea-188">**Windows 8.1:** Это значение не поддерживается до Windows 8.1 и Windows Server 2012 R2.</span><span class="sxs-lookup"><span data-stu-id="e9dea-188">**Windows 8.1:** This value is not supported until Windows 8.1 and Windows Server 2012 R2.</span></span>

</dd> <dt>

<span data-ttu-id="e9dea-189">**InstanceID**</span><span class="sxs-lookup"><span data-stu-id="e9dea-189">**InstanceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e9dea-190">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="e9dea-190">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="e9dea-191">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="e9dea-191">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="e9dea-192">Квалификаторы: **ключ**</span><span class="sxs-lookup"><span data-stu-id="e9dea-192">Qualifiers: **Key**</span></span>
</dt> </dl>

<span data-ttu-id="e9dea-193">Уникально идентифицирует экземпляр этого класса.</span><span class="sxs-lookup"><span data-stu-id="e9dea-193">Uniquely identifies an instance of this class.</span></span> <span data-ttu-id="e9dea-194">Это свойство наследуется от [**CIM \_ манажеделемент**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span><span class="sxs-lookup"><span data-stu-id="e9dea-194">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span></span>

</dd> <dt>

<span data-ttu-id="e9dea-195">**MigrationType**</span><span class="sxs-lookup"><span data-stu-id="e9dea-195">**MigrationType**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e9dea-196">Тип данных: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="e9dea-196">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="e9dea-197">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="e9dea-197">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="e9dea-198">Квалификаторы: [**override**](/windows/desktop/WmiSdk/standard-qualifiers) ("мигратионтипе")</span><span class="sxs-lookup"><span data-stu-id="e9dea-198">Qualifiers: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("MigrationType")</span></span>
</dt> </dl>

<span data-ttu-id="e9dea-199">Указывает тип выполняемой операции миграции.</span><span class="sxs-lookup"><span data-stu-id="e9dea-199">Specifies the type of migration operation to be performed.</span></span> <span data-ttu-id="e9dea-200">Это свойство наследуется от **CIM \_ виртуалсистеммигратионсеттингдата**.</span><span class="sxs-lookup"><span data-stu-id="e9dea-200">This property is inherited from **CIM\_VirtualSystemMigrationSettingData**.</span></span>

<dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="e9dea-201"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Неизвестно** (0)</span><span class="sxs-lookup"><span data-stu-id="e9dea-201"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (0)</span></span>


</dt> <dd></dd> <dt>

<span id="VirtualSystem"></span><span id="virtualsystem"></span><span id="VIRTUALSYSTEM"></span>

<span data-ttu-id="e9dea-202"><span id="VirtualSystem"></span><span id="virtualsystem"></span><span id="VIRTUALSYSTEM"></span>**Виртуалсистем** (32768)</span><span class="sxs-lookup"><span data-stu-id="e9dea-202"><span id="VirtualSystem"></span><span id="virtualsystem"></span><span id="VIRTUALSYSTEM"></span>**VirtualSystem** (32768)</span></span>


</dt> <dd>

<span data-ttu-id="e9dea-203">Переносит виртуальную систему на целевой узел.</span><span class="sxs-lookup"><span data-stu-id="e9dea-203">Migrates the virtual system to the destination host.</span></span>

</dd> <dt>

<span id="Storage"></span><span id="storage"></span><span id="STORAGE"></span>

<span data-ttu-id="e9dea-204"><span id="Storage"></span><span id="storage"></span><span id="STORAGE"></span>**Хранилище** (32769)</span><span class="sxs-lookup"><span data-stu-id="e9dea-204"><span id="Storage"></span><span id="storage"></span><span id="STORAGE"></span>**Storage** (32769)</span></span>


</dt> <dd>

<span data-ttu-id="e9dea-205">Переносит только ресурсы хранилища виртуальной системы.</span><span class="sxs-lookup"><span data-stu-id="e9dea-205">Migrates only the storage resources of the virtual system.</span></span>

</dd> <dt>

<span id="Staged"></span><span id="staged"></span><span id="STAGED"></span>

<span data-ttu-id="e9dea-206"><span id="Staged"></span><span id="staged"></span><span id="STAGED"></span>**Промежуточный** (32770)</span><span class="sxs-lookup"><span data-stu-id="e9dea-206"><span id="Staged"></span><span id="staged"></span><span id="STAGED"></span>**Staged** (32770)</span></span>


</dt> <dd>

<span data-ttu-id="e9dea-207">С помощью конфигурации виртуальной системы создает запланированную виртуальную систему на целевом узле.</span><span class="sxs-lookup"><span data-stu-id="e9dea-207">Using the virtual system configuration, creates a planned virtual system at the destination host.</span></span>

</dd> <dt>

<span id="VirtualSystemAndStorage"></span><span id="virtualsystemandstorage"></span><span id="VIRTUALSYSTEMANDSTORAGE"></span>

<span data-ttu-id="e9dea-208"><span id="VirtualSystemAndStorage"></span><span id="virtualsystemandstorage"></span><span id="VIRTUALSYSTEMANDSTORAGE"></span>**Виртуалсистемандстораже** (32771)</span><span class="sxs-lookup"><span data-stu-id="e9dea-208"><span id="VirtualSystemAndStorage"></span><span id="virtualsystemandstorage"></span><span id="VIRTUALSYSTEMANDSTORAGE"></span>**VirtualSystemAndStorage** (32771)</span></span>


</dt> <dd>

<span data-ttu-id="e9dea-209">Переносит виртуальную систему и ее хранилище на целевой узел.</span><span class="sxs-lookup"><span data-stu-id="e9dea-209">Migrates the virtual system and its storage to the destination host.</span></span>

</dd> <dt>

<span id="StorageDeepCheck"></span><span id="storagedeepcheck"></span><span id="STORAGEDEEPCHECK"></span>

<span data-ttu-id="e9dea-210"><span id="StorageDeepCheck"></span><span id="storagedeepcheck"></span><span id="STORAGEDEEPCHECK"></span>**Сторажедипчекк** (32772)</span><span class="sxs-lookup"><span data-stu-id="e9dea-210"><span id="StorageDeepCheck"></span><span id="storagedeepcheck"></span><span id="STORAGEDEEPCHECK"></span>**StorageDeepCheck** (32772)</span></span>


</dt> <dd>

<span data-ttu-id="e9dea-211">Выполняет проверку возможности миграции ресурсов хранилища виртуальной системы на целевом узле.</span><span class="sxs-lookup"><span data-stu-id="e9dea-211">Performs a virtual system storage resource migration ability check at the destination host.</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="e9dea-212">**осертранспорттипе**</span><span class="sxs-lookup"><span data-stu-id="e9dea-212">**OtherTransportType**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e9dea-213">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="e9dea-213">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="e9dea-214">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="e9dea-214">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="e9dea-215">Указывает тип транспорта, применяемого, если значение **TransportType** равно 1 (другое).</span><span class="sxs-lookup"><span data-stu-id="e9dea-215">Specifies the type of transport to be applied if the value of **TransportType** is 1 (Other).</span></span> <span data-ttu-id="e9dea-216">Это свойство наследуется от **CIM \_ виртуалсистеммигратионсеттингдата**.</span><span class="sxs-lookup"><span data-stu-id="e9dea-216">This property is inherited from **CIM\_VirtualSystemMigrationSettingData**.</span></span>

</dd> <dt>

<span data-ttu-id="e9dea-217">**Приоритет**</span><span class="sxs-lookup"><span data-stu-id="e9dea-217">**Priority**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e9dea-218">Тип данных: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="e9dea-218">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="e9dea-219">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="e9dea-219">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="e9dea-220">Указывает важность относительной миграции, которую система миграции может использовать для упорядочения или иным образом предоставлять предпочтение для нескольких ожидающих запросов на миграцию.</span><span class="sxs-lookup"><span data-stu-id="e9dea-220">Specifies a relative migration importance, which the migration system may use to order or otherwise give preference among multiple pending migration requests.</span></span> <span data-ttu-id="e9dea-221">Чем ниже значение, тем выше приоритет.</span><span class="sxs-lookup"><span data-stu-id="e9dea-221">The lower the value, the higher the priority.</span></span> <span data-ttu-id="e9dea-222">В рамках миграции значение 0 указывает приоритет по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="e9dea-222">Within a migration, a value of 0 indicates the default priority.</span></span> <span data-ttu-id="e9dea-223">В противном случае значение 0 указывает, что приоритеты не поддерживаются.</span><span class="sxs-lookup"><span data-stu-id="e9dea-223">Otherwise, a value of 0 indicates that priorities are not supported.</span></span>

<span data-ttu-id="e9dea-224">Это свойство наследуется от **CIM \_ виртуалсистеммигратионсеттингдата**.</span><span class="sxs-lookup"><span data-stu-id="e9dea-224">This property is inherited from **CIM\_VirtualSystemMigrationSettingData**.</span></span>

</dd> <dt>

<span data-ttu-id="e9dea-225">**ремовесаурцеунманажедвхдс**</span><span class="sxs-lookup"><span data-stu-id="e9dea-225">**RemoveSourceUnmanagedVhds**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e9dea-226">Тип данных: **логический**</span><span class="sxs-lookup"><span data-stu-id="e9dea-226">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="e9dea-227">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="e9dea-227">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="e9dea-228">Удалите исходные неуправляемые виртуальные жесткие диски.</span><span class="sxs-lookup"><span data-stu-id="e9dea-228">Remove source unmanaged VHDs.</span></span>

> [!Note]  
> <span data-ttu-id="e9dea-229">Добавлено в Windows 10 и Windows Server 2016.</span><span class="sxs-lookup"><span data-stu-id="e9dea-229">Added in Windows 10 and Windows Server 2016.</span></span>

 

</dd> <dt>

<span data-ttu-id="e9dea-230">**ретаинвхдкопиесонсаурце**</span><span class="sxs-lookup"><span data-stu-id="e9dea-230">**RetainVhdCopiesOnSource**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e9dea-231">Тип данных: **логический**</span><span class="sxs-lookup"><span data-stu-id="e9dea-231">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="e9dea-232">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="e9dea-232">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="e9dea-233">Для миграции хранилища указывает, следует ли удалять виртуальные жесткие диски только для чтения на исходном узле после завершения миграции.</span><span class="sxs-lookup"><span data-stu-id="e9dea-233">For a storage migration, this specifies whether the read-only VHDs on the source host should be removed after the migration is completed.</span></span>

</dd> <dt>

<span data-ttu-id="e9dea-234">**TransportType**</span><span class="sxs-lookup"><span data-stu-id="e9dea-234">**TransportType**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e9dea-235">Тип данных: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="e9dea-235">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="e9dea-236">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="e9dea-236">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="e9dea-237">Квалификаторы: [**override**](/windows/desktop/WmiSdk/standard-qualifiers) ("TransportType")</span><span class="sxs-lookup"><span data-stu-id="e9dea-237">Qualifiers: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("TransportType")</span></span>
</dt> </dl>

<span data-ttu-id="e9dea-238">Указывает тип транспорта, применяемого для операции миграции виртуальной системы.</span><span class="sxs-lookup"><span data-stu-id="e9dea-238">Specifies the type of transport to be applied for a virtual system migration operation.</span></span> <span data-ttu-id="e9dea-239">Это свойство наследуется от **CIM \_ виртуалсистеммигратионсеттингдата**.</span><span class="sxs-lookup"><span data-stu-id="e9dea-239">This property is inherited from **CIM\_VirtualSystemMigrationSettingData**.</span></span>

<dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="e9dea-240">**Неизвестно** (0)</span><span class="sxs-lookup"><span data-stu-id="e9dea-240">**Unknown** (0)</span></span>


</dt> <dd></dd> <dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="e9dea-241">**Другое** (1)</span><span class="sxs-lookup"><span data-stu-id="e9dea-241">**Other** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="SSH"></span><span id="ssh"></span>

<span data-ttu-id="e9dea-242">**SSH** (2)</span><span class="sxs-lookup"><span data-stu-id="e9dea-242">**SSH** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="TLS"></span><span id="tls"></span>

<span data-ttu-id="e9dea-243">**TLS** (3)</span><span class="sxs-lookup"><span data-stu-id="e9dea-243">**TLS** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="TLS_Strict"></span><span id="tls_strict"></span><span id="TLS_STRICT"></span>

<span data-ttu-id="e9dea-244">**TLS-точность** (4)</span><span class="sxs-lookup"><span data-stu-id="e9dea-244">**TLS Strict** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="TCP"></span><span id="tcp"></span>

<span data-ttu-id="e9dea-245">**TCP** (5)</span><span class="sxs-lookup"><span data-stu-id="e9dea-245">**TCP** (5)</span></span>


</dt> <dd></dd> <dt>

<span id="IPC"></span><span id="ipc"></span>

<span data-ttu-id="e9dea-246">**IPC** (6)</span><span class="sxs-lookup"><span data-stu-id="e9dea-246">**IPC** (6)</span></span>


</dt> <dd></dd> <dt>

<span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>

<span data-ttu-id="e9dea-247">**Зарезервировано DMTF** (..)</span><span class="sxs-lookup"><span data-stu-id="e9dea-247">**DMTF Reserved** (..)</span></span>


</dt> <dd></dd> <dt>

<span id="Vendor_Reserved"></span><span id="vendor_reserved"></span><span id="VENDOR_RESERVED"></span>

<span data-ttu-id="e9dea-248">**Поставщик зарезервирован** (32768...)</span><span class="sxs-lookup"><span data-stu-id="e9dea-248">**Vendor Reserved** (32768..)</span></span>


<span data-ttu-id="e9dea-249"></dt> <dd></dd> </dl></span><span class="sxs-lookup"><span data-stu-id="e9dea-249"></dt> <dd></dd> </dl></span></span>

<span data-ttu-id="e9dea-250">Для динамической миграции это свойство указывает тип транспорта, используемый для передачи состояния виртуальной системы на целевой узел.</span><span class="sxs-lookup"><span data-stu-id="e9dea-250">For live migration, this property specifies the transport type to be used for transferring virtual system state to the destination host.</span></span> <span data-ttu-id="e9dea-251">Поддерживаются такие значения:</span><span class="sxs-lookup"><span data-stu-id="e9dea-251">The supported values are:</span></span>

<dt>

<span id="TCP"></span><span id="tcp"></span>

<span data-ttu-id="e9dea-252"><span id="TCP"></span><span id="tcp"></span>**TCP** (5)</span><span class="sxs-lookup"><span data-stu-id="e9dea-252"><span id="TCP"></span><span id="tcp"></span>**TCP** (5)</span></span>


</dt> <dd>

<span data-ttu-id="e9dea-253">Указывает тип транспорта TCP.</span><span class="sxs-lookup"><span data-stu-id="e9dea-253">Indicates the TCP transport type.</span></span>

</dd> <dt>

<span id="SMB"></span><span id="smb"></span>

<span data-ttu-id="e9dea-254"><span id="SMB"></span><span id="smb"></span>**SMB** (32768)</span><span class="sxs-lookup"><span data-stu-id="e9dea-254"><span id="SMB"></span><span id="smb"></span>**SMB** (32768)</span></span>


</dt> <dd>

<span data-ttu-id="e9dea-255">Указывает тип транспорта для передачи состояния виртуальной машины — SMB.</span><span class="sxs-lookup"><span data-stu-id="e9dea-255">Indicates the transport type for transferring the virtual machine state is SMB.</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="e9dea-256">**унманажедвхдс**</span><span class="sxs-lookup"><span data-stu-id="e9dea-256">**UnmanagedVhds**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e9dea-257">Тип данных: массив **строк**</span><span class="sxs-lookup"><span data-stu-id="e9dea-257">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="e9dea-258">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="e9dea-258">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="e9dea-259">Квалификаторы: [**arrayType**](/windows/desktop/WmiSdk/standard-qualifiers) ("индексированный"), **Хипервембеддединстанце** ("мсвм \_ мовеунманажедвхд")</span><span class="sxs-lookup"><span data-stu-id="e9dea-259">Qualifiers: [**ArrayType**](/windows/desktop/WmiSdk/standard-qualifiers) ("Indexed"), **HyperVEmbeddedInstance** ("Msvm\_MoveUnmanagedVhd")</span></span>
</dt> </dl>

<span data-ttu-id="e9dea-260">Массив внедренных экземпляров [**мсвм \_ мовеунманажедвхд**](msvm-moveunmanagedvhd.md) , которые содержат неуправляемые сведения о виртуальных жестких дисках.</span><span class="sxs-lookup"><span data-stu-id="e9dea-260">An array of embedded [**Msvm\_MoveUnmanagedVhd**](msvm-moveunmanagedvhd.md) instances which contain unmanaged VHDs information.</span></span>

> [!Note]  
> <span data-ttu-id="e9dea-261">Добавлено в Windows 10 и Windows Server 2016.</span><span class="sxs-lookup"><span data-stu-id="e9dea-261">Added in Windows 10 and Windows Server 2016.</span></span>

 

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="e9dea-262">Требования</span><span class="sxs-lookup"><span data-stu-id="e9dea-262">Requirements</span></span>



| <span data-ttu-id="e9dea-263">Требование</span><span class="sxs-lookup"><span data-stu-id="e9dea-263">Requirement</span></span> | <span data-ttu-id="e9dea-264">Значение</span><span class="sxs-lookup"><span data-stu-id="e9dea-264">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="e9dea-265">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="e9dea-265">Minimum supported client</span></span><br/> | <span data-ttu-id="e9dea-266">\[Только классические приложения Windows 8\]</span><span class="sxs-lookup"><span data-stu-id="e9dea-266">Windows 8 \[desktop apps only\]</span></span><br/>                                                              |
| <span data-ttu-id="e9dea-267">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="e9dea-267">Minimum supported server</span></span><br/> | <span data-ttu-id="e9dea-268">\[Только для настольных приложений Windows Server 2012\]</span><span class="sxs-lookup"><span data-stu-id="e9dea-268">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="e9dea-269">Пространство имен</span><span class="sxs-lookup"><span data-stu-id="e9dea-269">Namespace</span></span><br/>                | <span data-ttu-id="e9dea-270">Корневая \\ виртуализация \\ версии 2</span><span class="sxs-lookup"><span data-stu-id="e9dea-270">Root\\Virtualization\\V2</span></span><br/>                                                                     |
| <span data-ttu-id="e9dea-271">MOF</span><span class="sxs-lookup"><span data-stu-id="e9dea-271">MOF</span></span><br/>                      | <dl> <span data-ttu-id="e9dea-272"><dt>Виндовсвиртуализатион. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="e9dea-272"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="e9dea-273">DLL</span><span class="sxs-lookup"><span data-stu-id="e9dea-273">DLL</span></span><br/>                      | <dl> <span data-ttu-id="e9dea-274"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="e9dea-274"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="e9dea-275">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="e9dea-275">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e9dea-276">**\_ВИРТУАЛСИСТЕММИГРАТИОНСЕТТИНГДАТА CIM**</span><span class="sxs-lookup"><span data-stu-id="e9dea-276">**CIM\_VirtualSystemMigrationSettingData**</span></span>](cim-virtualsystemmigrationsettingdata.md)
</dt> <dt>

[<span data-ttu-id="e9dea-277">**мигратевиртуалсистемтохост**</span><span class="sxs-lookup"><span data-stu-id="e9dea-277">**MigrateVirtualSystemToHost**</span></span>](migratevirtualsystemtohost-msvm-virtualsystemmigrationservice.md)
</dt> </dl>

 

