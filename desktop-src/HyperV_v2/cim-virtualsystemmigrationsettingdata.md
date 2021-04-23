---
description: Определяет параметры миграции виртуальной системы, управляемой экземпляром \_ класса CIM виртуалсистеммигратионсервице.
ms.assetid: c28ed48b-bacc-49c8-9131-2543c0edb3fd
title: Класс CIM_VirtualSystemMigrationSettingData
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_VirtualSystemMigrationSettingData
- CIM_VirtualSystemMigrationSettingData.MigrationType
- CIM_VirtualSystemMigrationSettingData.Priority
- CIM_VirtualSystemMigrationSettingData.Bandwidth
- CIM_VirtualSystemMigrationSettingData.BandwidthUnit
- CIM_VirtualSystemMigrationSettingData.OtherTransportType
- CIM_VirtualSystemMigrationSettingData.TransportType
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: 0d33479d0148bc4004fbbbda216e508c276c7ee9
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "103813385"
---
# <a name="cim_virtualsystemmigrationsettingdata-class"></a><span data-ttu-id="71140-103">\_Класс CIM виртуалсистеммигратионсеттингдата</span><span class="sxs-lookup"><span data-stu-id="71140-103">CIM\_VirtualSystemMigrationSettingData class</span></span>

<span data-ttu-id="71140-104">Определяет параметры миграции виртуальной системы, управляемой экземпляром класса [**CIM \_ виртуалсистеммигратионсервице**](cim-virtualsystemmigrationservice.md) .</span><span class="sxs-lookup"><span data-stu-id="71140-104">Defines the settings for virtual system migration that is managed by an instance of the [**CIM\_VirtualSystemMigrationService**](cim-virtualsystemmigrationservice.md) class.</span></span>

## <a name="syntax"></a><span data-ttu-id="71140-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="71140-105">Syntax</span></span>

``` syntax
[Experimental, Abstract, Version("2.20.0"), UMLPackagePath("CIM::System::Virtualization"), AMENDMENT]
class CIM_VirtualSystemMigrationSettingData : CIM_SettingData
{
  uint16 MigrationType;
  uint16 Priority;
  uint16 Bandwidth;
  string BandwidthUnit;
  string OtherTransportType;
  uint16 TransportType;
};
```

## <a name="members"></a><span data-ttu-id="71140-106">Члены</span><span class="sxs-lookup"><span data-stu-id="71140-106">Members</span></span>

<span data-ttu-id="71140-107">Класс **CIM \_ виртуалсистеммигратионсеттингдата** имеет следующие типы членов:</span><span class="sxs-lookup"><span data-stu-id="71140-107">The **CIM\_VirtualSystemMigrationSettingData** class has these types of members:</span></span>

-   [<span data-ttu-id="71140-108">Свойства</span><span class="sxs-lookup"><span data-stu-id="71140-108">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="71140-109">Свойства</span><span class="sxs-lookup"><span data-stu-id="71140-109">Properties</span></span>

<span data-ttu-id="71140-110">Класс **CIM \_ виртуалсистеммигратионсеттингдата** имеет следующие свойства.</span><span class="sxs-lookup"><span data-stu-id="71140-110">The **CIM\_VirtualSystemMigrationSettingData** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="71140-111">**Пропускная способность**</span><span class="sxs-lookup"><span data-stu-id="71140-111">**Bandwidth**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="71140-112">Тип данных: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="71140-112">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="71140-113">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="71140-113">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="71140-114">Квалификаторы: [**датчик**](/windows/desktop/WmiSdk/standard-qualifiers), [**Моделкорреспонденце**](/windows/desktop/WmiSdk/standard-qualifiers) ("**CIM \_ виртуалсистеммигратионсеттингдата**.**Бандвидсунит**")</span><span class="sxs-lookup"><span data-stu-id="71140-114">Qualifiers: [**Gauge**](/windows/desktop/WmiSdk/standard-qualifiers), [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("**CIM\_VirtualSystemMigrationSettingData**.**BandwidthUnit**")</span></span>
</dt> </dl>

<span data-ttu-id="71140-115">Пропускная способность, назначенная или запрошенная для операции миграции виртуальной системы.</span><span class="sxs-lookup"><span data-stu-id="71140-115">The bandwidth assigned to or requested for a virtual system migration operation.</span></span> <span data-ttu-id="71140-116">"0" — пропускная способность по умолчанию для запросов на миграцию.</span><span class="sxs-lookup"><span data-stu-id="71140-116">"0" is default bandwidth for migration requests.</span></span>

<span data-ttu-id="71140-117">Свойства **пропускной способности** и **приоритета** можно использовать в сочетании.</span><span class="sxs-lookup"><span data-stu-id="71140-117">The **Bandwidth** and **Priority** properties may be used in conjunction.</span></span> <span data-ttu-id="71140-118">Процессы миграции, имеющие наивысшие значения **приоритета** , совместно используют доступную пропускную способность в зависимости от запрошенной пропускной способности.</span><span class="sxs-lookup"><span data-stu-id="71140-118">Migration processes that have the highest equal **Priority** values share the available bandwidth based on their requested bandwidth.</span></span> <span data-ttu-id="71140-119">Если этот набор процессов потребляет не всю пропускную способность, процессы миграции со следующими более низкими значениями **приоритета** совместно используют оставшуюся пропускную способность.</span><span class="sxs-lookup"><span data-stu-id="71140-119">If not all bandwidth is consumed by this set of processes, migration processes with the next lower equal **Priority** values share the remaining bandwidth.</span></span> <span data-ttu-id="71140-120">Если пропускная способность осталась, рассматриваются процессы миграции со следующими более низкими значениями **приоритета** .</span><span class="sxs-lookup"><span data-stu-id="71140-120">If more bandwidth remains, migration processes with the next lower equal **Priority** values are considered.</span></span>

<span data-ttu-id="71140-121">Единица, используемая в свойстве **пропускной способности** , задается значением свойства **бандвидсунит** .</span><span class="sxs-lookup"><span data-stu-id="71140-121">The unit used in **Bandwidth** property is specified by the value of the **BandwidthUnit** property.</span></span>

<span data-ttu-id="71140-122">Если свойство **бандвидсунит** имеет значение «Percent», применяются следующие правила.</span><span class="sxs-lookup"><span data-stu-id="71140-122">If the value of the **BandwidthUnit** property is "percent", the following rules apply:</span></span>

-   <span data-ttu-id="71140-123">Значение свойства **пропускной способности** должно находиться в диапазоне от "0" до "100" с более высоким значением, указывающим на более высокую пропускную способность.</span><span class="sxs-lookup"><span data-stu-id="71140-123">The value of the **Bandwidth** property must be between "0" and "100", with higher values indicating a higher bandwidth.</span></span>
-   <span data-ttu-id="71140-124">Значение "100" указывает всю доступную пропускную способность для выполнения операций миграции виртуальной системы.</span><span class="sxs-lookup"><span data-stu-id="71140-124">A value of "100" indicates all available bandwidth for performing virtual system migration operations.</span></span>
-   <span data-ttu-id="71140-125">Значения между "1" и "100" линейно сопоставляются с доступным диапазоном пропускной способности.</span><span class="sxs-lookup"><span data-stu-id="71140-125">Values between "1" and "100" linearly correlate with the available bandwidth range.</span></span> <span data-ttu-id="71140-126">Например, значение 50 запрашивает половину доступной пропускной способности.</span><span class="sxs-lookup"><span data-stu-id="71140-126">For example, a value of 50 requests half of the available bandwidth.</span></span>

</dd> <dt>

<span data-ttu-id="71140-127">**бандвидсунит**</span><span class="sxs-lookup"><span data-stu-id="71140-127">**BandwidthUnit**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="71140-128">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="71140-128">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="71140-129">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="71140-129">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="71140-130">Квалификаторы: [**моделкорреспонденце**](/windows/desktop/WmiSdk/standard-qualifiers) ("**CIM \_ виртуалсистеммигратионсеттингдата**.**Пропускная способность**"), **испунит**</span><span class="sxs-lookup"><span data-stu-id="71140-130">Qualifiers: [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("**CIM\_VirtualSystemMigrationSettingData**.**Bandwidth**"), **IsPUnit**</span></span>
</dt> </dl>

<span data-ttu-id="71140-131">Единица, используемая свойством **пропускной способности** .</span><span class="sxs-lookup"><span data-stu-id="71140-131">The unit used by the **Bandwidth** property.</span></span> <span data-ttu-id="71140-132">Значением этого свойства должно быть допустимое значение квалификатора программных единиц, определенное в приложении C. 1 DSP0004 V 2.4 или более поздней версии.</span><span class="sxs-lookup"><span data-stu-id="71140-132">The value of this property should be a legal value of the Programmatic Units qualifier defined in Appendix C.1 of DSP0004 V2.4 or later.</span></span>

> [!Note]  
> <span data-ttu-id="71140-133">Такие профили, как DMTF DSP1081, определяют, как клиенты могут обнаруживать набор единиц, поддерживаемых реализацией, а также диапазоны и приращения значений свойства **пропускной способности** .</span><span class="sxs-lookup"><span data-stu-id="71140-133">Profiles such as DMTF DSP1081 define how clients can discover the set of units supported by an implementation, and ranges and increments for values of the **Bandwidth** property.</span></span>

 

</dd> <dt>

<span data-ttu-id="71140-134">**MigrationType**</span><span class="sxs-lookup"><span data-stu-id="71140-134">**MigrationType**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="71140-135">Тип данных: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="71140-135">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="71140-136">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="71140-136">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="71140-137">Тип выполняемой операции миграции.</span><span class="sxs-lookup"><span data-stu-id="71140-137">The type of migration operation to perform.</span></span>

<dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="71140-138">**Неизвестно** (0)</span><span class="sxs-lookup"><span data-stu-id="71140-138">**Unknown** (0)</span></span>


</dt> <dd></dd> <dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="71140-139">**Другое** (1)</span><span class="sxs-lookup"><span data-stu-id="71140-139">**Other** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Live"></span><span id="live"></span><span id="LIVE"></span>

<span data-ttu-id="71140-140">**Live** (2)</span><span class="sxs-lookup"><span data-stu-id="71140-140">**Live** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Resume"></span><span id="resume"></span><span id="RESUME"></span>

<span data-ttu-id="71140-141">**Возобновление** (3)</span><span class="sxs-lookup"><span data-stu-id="71140-141">**Resume** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="Restart"></span><span id="restart"></span><span id="RESTART"></span>

<span data-ttu-id="71140-142">**Перезапустить** (4)</span><span class="sxs-lookup"><span data-stu-id="71140-142">**Restart** (4)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="71140-143">**осертранспорттипе**</span><span class="sxs-lookup"><span data-stu-id="71140-143">**OtherTransportType**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="71140-144">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="71140-144">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="71140-145">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="71140-145">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="71140-146">Квалификаторы: [**моделкорреспонденце**](/windows/desktop/WmiSdk/standard-qualifiers) ("**CIM \_ виртуалсистеммигратионсеттингдата**.**TransportType**")</span><span class="sxs-lookup"><span data-stu-id="71140-146">Qualifiers: [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("**CIM\_VirtualSystemMigrationSettingData**.**TransportType**")</span></span>
</dt> </dl>

<span data-ttu-id="71140-147">Тип транспорта, который необходимо применить, если значение **TransportType** равно "1" (другое).</span><span class="sxs-lookup"><span data-stu-id="71140-147">The type of transport to apply if the value of **TransportType** is "1" (other).</span></span>

</dd> <dt>

<span data-ttu-id="71140-148">**Приоритет**</span><span class="sxs-lookup"><span data-stu-id="71140-148">**Priority**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="71140-149">Тип данных: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="71140-149">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="71140-150">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="71140-150">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="71140-151">Важность относительной миграции, которую реализация миграции виртуальной системы может использовать для упорядочивания или назначения предпочтений между несколькими ожидающими запросами на миграцию.</span><span class="sxs-lookup"><span data-stu-id="71140-151">The relative migration importance that the virtual system migration implementation may use to order or assign preference among multiple pending migration requests.</span></span> <span data-ttu-id="71140-152">Чем ниже значение, тем выше приоритет.</span><span class="sxs-lookup"><span data-stu-id="71140-152">The lower the value, the higher the priority.</span></span> <span data-ttu-id="71140-153">"0" — пропускная способность по умолчанию для запросов на миграцию.</span><span class="sxs-lookup"><span data-stu-id="71140-153">"0" is default bandwidth for migration requests.</span></span>

</dd> <dt>

<span data-ttu-id="71140-154">**TransportType**</span><span class="sxs-lookup"><span data-stu-id="71140-154">**TransportType**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="71140-155">Тип данных: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="71140-155">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="71140-156">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="71140-156">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="71140-157">Квалификаторы: [**моделкорреспонденце**](/windows/desktop/WmiSdk/standard-qualifiers) ("**CIM \_ виртуалсистеммигратионсеттингдата**.**Осертранспорттипе**")</span><span class="sxs-lookup"><span data-stu-id="71140-157">Qualifiers: [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("**CIM\_VirtualSystemMigrationSettingData**.**OtherTransportType**")</span></span>
</dt> </dl>

<span data-ttu-id="71140-158">Тип транспорта, применяемый к операции миграции виртуальной системы.</span><span class="sxs-lookup"><span data-stu-id="71140-158">The type of transport to apply to a virtual system migration operation.</span></span>

<dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="71140-159">**Неизвестно** (0)</span><span class="sxs-lookup"><span data-stu-id="71140-159">**Unknown** (0)</span></span>


</dt> <dd></dd> <dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="71140-160">**Другое** (1)</span><span class="sxs-lookup"><span data-stu-id="71140-160">**Other** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="SSH"></span><span id="ssh"></span>

<span data-ttu-id="71140-161">**SSH** (2)</span><span class="sxs-lookup"><span data-stu-id="71140-161">**SSH** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="TLS"></span><span id="tls"></span>

<span data-ttu-id="71140-162">**TLS** (3)</span><span class="sxs-lookup"><span data-stu-id="71140-162">**TLS** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="TLS_Strict"></span><span id="tls_strict"></span><span id="TLS_STRICT"></span>

<span data-ttu-id="71140-163">**TLS-точность** (4)</span><span class="sxs-lookup"><span data-stu-id="71140-163">**TLS Strict** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="TCP"></span><span id="tcp"></span>

<span data-ttu-id="71140-164">**TCP** (5)</span><span class="sxs-lookup"><span data-stu-id="71140-164">**TCP** (5)</span></span>


</dt> <dd></dd> <dt>

<span id="IPC"></span><span id="ipc"></span>

<span data-ttu-id="71140-165">**IPC** (6)</span><span class="sxs-lookup"><span data-stu-id="71140-165">**IPC** (6)</span></span>


</dt> <dd></dd> <dt>

<span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>

<span data-ttu-id="71140-166">**Зарезервировано DMTF** (..)</span><span class="sxs-lookup"><span data-stu-id="71140-166">**DMTF Reserved** (..)</span></span>


</dt> <dd></dd> <dt>

<span id="Vendor_Reserved"></span><span id="vendor_reserved"></span><span id="VENDOR_RESERVED"></span>

<span data-ttu-id="71140-167">**Поставщик зарезервирован** (32768...)</span><span class="sxs-lookup"><span data-stu-id="71140-167">**Vendor Reserved** (32768..)</span></span>


<span data-ttu-id="71140-168"></dt> <dd></dd> </dl>

</dd> </dl></span><span class="sxs-lookup"><span data-stu-id="71140-168"></dt> <dd></dd> </dl>

</dd> </dl></span></span>

## <a name="requirements"></a><span data-ttu-id="71140-169">Требования</span><span class="sxs-lookup"><span data-stu-id="71140-169">Requirements</span></span>



| <span data-ttu-id="71140-170">Требование</span><span class="sxs-lookup"><span data-stu-id="71140-170">Requirement</span></span> | <span data-ttu-id="71140-171">Значение</span><span class="sxs-lookup"><span data-stu-id="71140-171">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="71140-172">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="71140-172">Minimum supported client</span></span><br/> | <span data-ttu-id="71140-173">Windows 8</span><span class="sxs-lookup"><span data-stu-id="71140-173">Windows 8</span></span><br/>                                                                                    |
| <span data-ttu-id="71140-174">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="71140-174">Minimum supported server</span></span><br/> | <span data-ttu-id="71140-175">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="71140-175">Windows Server 2012</span></span><br/>                                                                          |
| <span data-ttu-id="71140-176">Пространство имен</span><span class="sxs-lookup"><span data-stu-id="71140-176">Namespace</span></span><br/>                | <span data-ttu-id="71140-177">Корневая \\ виртуализация \\ версии 2</span><span class="sxs-lookup"><span data-stu-id="71140-177">Root\\virtualization\\v2</span></span><br/>                                                                     |
| <span data-ttu-id="71140-178">MOF</span><span class="sxs-lookup"><span data-stu-id="71140-178">MOF</span></span><br/>                      | <dl> <span data-ttu-id="71140-179"><dt>Виндовсвиртуализатион. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="71140-179"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="71140-180">DLL</span><span class="sxs-lookup"><span data-stu-id="71140-180">DLL</span></span><br/>                      | <dl> <span data-ttu-id="71140-181"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="71140-181"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="71140-182">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="71140-182">See also</span></span>

<dl> <dt>

[<span data-ttu-id="71140-183">**\_SETTINGDATA CIM**</span><span class="sxs-lookup"><span data-stu-id="71140-183">**CIM\_SettingData**</span></span>](cim-settingdata.md)
</dt> </dl>

 

