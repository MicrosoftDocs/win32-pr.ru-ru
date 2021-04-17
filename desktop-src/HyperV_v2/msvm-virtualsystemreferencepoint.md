---
description: Представляет точку ссылки для виртуальной системы.
ms.assetid: b3ba4fa7-3b77-4a1d-ab8f-d38af12ab5dd
title: Класс Msvm_VirtualSystemReferencePoint
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_VirtualSystemReferencePoint
- Msvm_VirtualSystemReferencePoint.InstanceID
- Msvm_VirtualSystemReferencePoint.ReferencePointType
- Msvm_VirtualSystemReferencePoint.ConsistencyLevel
- Msvm_VirtualSystemReferencePoint.VirtualSystemIdentifier
- Msvm_VirtualSystemReferencePoint.HasAssociatedData
- Msvm_VirtualSystemReferencePoint.VirtualDiskIdentifiers
- Msvm_VirtualSystemReferencePoint.ResilientChangeTrackingIdentifiers
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: add160cf44a592462634704ddf783cd8f4084068
ms.sourcegitcommit: c16214e53680dc71d1c07111b51f72b82a4512d8
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/03/2021
ms.locfileid: "105664821"
---
# <a name="msvm_virtualsystemreferencepoint-class"></a><span data-ttu-id="1b871-103">\_Класс мсвм виртуалсистемреференцепоинт</span><span class="sxs-lookup"><span data-stu-id="1b871-103">Msvm\_VirtualSystemReferencePoint class</span></span>

<span data-ttu-id="1b871-104">Представляет точку ссылки для виртуальной системы.</span><span class="sxs-lookup"><span data-stu-id="1b871-104">Represents a reference point for a virtual system.</span></span>

<span data-ttu-id="1b871-105">Следующий пример синтаксиса — упрощенный MOF-код, который включает все наследуемые свойства.</span><span class="sxs-lookup"><span data-stu-id="1b871-105">The following syntax is simplified from Managed Object Format (MOF) code and includes all of the inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="1b871-106">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="1b871-106">Syntax</span></span>

``` syntax
[Dynamic, Provider("VmmsWmiInstanceAndMethodProvider"), AMENDMENT]
class Msvm_VirtualSystemReferencePoint : CIM_ManagedElement
{
  string  InstanceID;
  uint16  ReferencePointType;
  uint16  ConsistencyLevel;
  string  VirtualSystemIdentifier;
  boolean HasAssociatedData;
  string  VirtualDiskIdentifiers[];
  string  ResilientChangeTrackingIdentifiers[];
};
```

## <a name="members"></a><span data-ttu-id="1b871-107">Члены</span><span class="sxs-lookup"><span data-stu-id="1b871-107">Members</span></span>

<span data-ttu-id="1b871-108">Класс **мсвм \_ виртуалсистемреференцепоинт** имеет следующие типы членов:</span><span class="sxs-lookup"><span data-stu-id="1b871-108">The **Msvm\_VirtualSystemReferencePoint** class has these types of members:</span></span>

-   [<span data-ttu-id="1b871-109">Свойства</span><span class="sxs-lookup"><span data-stu-id="1b871-109">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="1b871-110">Свойства</span><span class="sxs-lookup"><span data-stu-id="1b871-110">Properties</span></span>

<span data-ttu-id="1b871-111">Класс **мсвм \_ виртуалсистемреференцепоинт** имеет следующие свойства.</span><span class="sxs-lookup"><span data-stu-id="1b871-111">The **Msvm\_VirtualSystemReferencePoint** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="1b871-112">**ConsistencyLevel**</span><span class="sxs-lookup"><span data-stu-id="1b871-112">**ConsistencyLevel**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1b871-113">Тип данных: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="1b871-113">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="1b871-114">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="1b871-114">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="1b871-115">Уровень согласованности контрольной точки.</span><span class="sxs-lookup"><span data-stu-id="1b871-115">The consistency level of the reference point.</span></span>

<dt>

<span id="Application_Consistent"></span><span id="application_consistent"></span><span id="APPLICATION_CONSISTENT"></span>

<span data-ttu-id="1b871-116"><span id="Application_Consistent"></span><span id="application_consistent"></span><span id="APPLICATION_CONSISTENT"></span>С **совместимостью приложений** (1)</span><span class="sxs-lookup"><span data-stu-id="1b871-116"><span id="Application_Consistent"></span><span id="application_consistent"></span><span id="APPLICATION_CONSISTENT"></span>**Application Consistent** (1)</span></span>


</dt> <dd>

<span data-ttu-id="1b871-117">Эталонная точка указывает на момент времени, когда виртуальная система находилась в состоянии совместимости с приложениями.</span><span class="sxs-lookup"><span data-stu-id="1b871-117">The reference point indicates a point in time when the virtual system was in application consistent state.</span></span>

</dd> <dt>

<span id="Crash_Consistent"></span><span id="crash_consistent"></span><span id="CRASH_CONSISTENT"></span>

<span data-ttu-id="1b871-118"><span id="Crash_Consistent"></span><span id="crash_consistent"></span><span id="CRASH_CONSISTENT"></span>**Отказоустойчивость (2** )</span><span class="sxs-lookup"><span data-stu-id="1b871-118"><span id="Crash_Consistent"></span><span id="crash_consistent"></span><span id="CRASH_CONSISTENT"></span>**Crash Consistent** (2)</span></span>


</dt> <dd>

<span data-ttu-id="1b871-119">Эталонная точка указывает на момент времени, когда виртуальная система находилась в состоянии сбоя.</span><span class="sxs-lookup"><span data-stu-id="1b871-119">The reference point indicates a point in time when the virtual system was in crash consistent state.</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="1b871-120">**хасассоЦиатеддата**</span><span class="sxs-lookup"><span data-stu-id="1b871-120">**HasAssociatedData**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1b871-121">Тип данных: **логический**</span><span class="sxs-lookup"><span data-stu-id="1b871-121">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="1b871-122">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="1b871-122">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="1b871-123">Задайте значение **true** , если эталонная точка имеет связанные данные.</span><span class="sxs-lookup"><span data-stu-id="1b871-123">Set to **true** if the reference point has associated data.</span></span> <span data-ttu-id="1b871-124">Это допустимо только для опорных точек на основе журналов.</span><span class="sxs-lookup"><span data-stu-id="1b871-124">This is valid only for log based reference points.</span></span> <span data-ttu-id="1b871-125">Для опорных точек, основанных на RCT, **хасассоЦиатеддата** имеет значение **false**.</span><span class="sxs-lookup"><span data-stu-id="1b871-125">For RCT-based reference points, **HasAssociatedData** is set to **false**.</span></span> <span data-ttu-id="1b871-126">Для контрольных точек на основе журналов после удаления журнала **хасассоЦиатеддата** становится **ложным**.</span><span class="sxs-lookup"><span data-stu-id="1b871-126">For log based reference points, once the log is discarded **HasAssociatedData** becomes **false**.</span></span>

</dd> <dt>

<span data-ttu-id="1b871-127">**InstanceID**</span><span class="sxs-lookup"><span data-stu-id="1b871-127">**InstanceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1b871-128">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="1b871-128">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="1b871-129">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="1b871-129">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="1b871-130">Квалификаторы: [**ключ**](/windows/desktop/WmiSdk/key-qualifier), [**Переопределение**](/windows/desktop/WmiSdk/standard-qualifiers) ("InstanceId"), [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (256)</span><span class="sxs-lookup"><span data-stu-id="1b871-130">Qualifiers: [**Key**](/windows/desktop/WmiSdk/key-qualifier), [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("InstanceID"), [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (256)</span></span>
</dt> </dl>

<span data-ttu-id="1b871-131">Уникальная идентификация объекта опорной точки.</span><span class="sxs-lookup"><span data-stu-id="1b871-131">Unique identification of a reference point object.</span></span>

</dd> <dt>

<span data-ttu-id="1b871-132">**референцепоинттипе**</span><span class="sxs-lookup"><span data-stu-id="1b871-132">**ReferencePointType**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1b871-133">Тип данных: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="1b871-133">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="1b871-134">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="1b871-134">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="1b871-135">Указывает тип контрольной точки.</span><span class="sxs-lookup"><span data-stu-id="1b871-135">Indicates the type of the reference point.</span></span>

<dt>

<span id="Log_based"></span><span id="log_based"></span><span id="LOG_BASED"></span>

<span data-ttu-id="1b871-136"><span id="Log_based"></span><span id="log_based"></span><span id="LOG_BASED"></span>**На основе журнала** (1)</span><span class="sxs-lookup"><span data-stu-id="1b871-136"><span id="Log_based"></span><span id="log_based"></span><span id="LOG_BASED"></span>**Log based** (1)</span></span>


</dt> <dd>

<span data-ttu-id="1b871-137">Отслеживание журнала реплики Hyper-V.</span><span class="sxs-lookup"><span data-stu-id="1b871-137">Hyper-V replica log tracking.</span></span>

</dd> <dt>

<span id="RCT_based"></span><span id="rct_based"></span><span id="RCT_BASED"></span>

<span data-ttu-id="1b871-138"><span id="RCT_based"></span><span id="rct_based"></span><span id="RCT_BASED"></span>**На основе RCT** (2)</span><span class="sxs-lookup"><span data-stu-id="1b871-138"><span id="RCT_based"></span><span id="rct_based"></span><span id="RCT_BASED"></span>**RCT based** (2)</span></span>


</dt> <dd>

<span data-ttu-id="1b871-139">На основе устойчивых Отслеживание изменений виртуальных дисков.</span><span class="sxs-lookup"><span data-stu-id="1b871-139">Based on Resilient Change Tracking of virtual disks.</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="1b871-140">**ресилиентчанжетраккингидентифиерс**</span><span class="sxs-lookup"><span data-stu-id="1b871-140">**ResilientChangeTrackingIdentifiers**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1b871-141">Тип данных: массив **строк**</span><span class="sxs-lookup"><span data-stu-id="1b871-141">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="1b871-142">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="1b871-142">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="1b871-143">Массив идентификаторов RCT, соответствующих виртуальным дискам виртуальной машины на момент создания этой контрольной точки.</span><span class="sxs-lookup"><span data-stu-id="1b871-143">An array of RCT IDs corresponding to the virtual disks of the VM at the time this reference point was created.</span></span> <span data-ttu-id="1b871-144">Это поле допустимо только для опорных точек на основе RCT.</span><span class="sxs-lookup"><span data-stu-id="1b871-144">This field is valid only for RCT-based reference points.</span></span>

</dd> <dt>

<span data-ttu-id="1b871-145">**виртуалдискидентифиерс**</span><span class="sxs-lookup"><span data-stu-id="1b871-145">**VirtualDiskIdentifiers**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1b871-146">Тип данных: массив **строк**</span><span class="sxs-lookup"><span data-stu-id="1b871-146">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="1b871-147">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="1b871-147">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="1b871-148">Массив идентификаторов экземпляров WMI, соответствующий виртуальным дискам виртуальной машины на момент создания этой контрольной точки.</span><span class="sxs-lookup"><span data-stu-id="1b871-148">An array of WMI instance IDs corresponding to the virtual disks of the VM at the time this reference point was created.</span></span> <span data-ttu-id="1b871-149">С этими виртуальными дисками связаны идентификаторы RCT.</span><span class="sxs-lookup"><span data-stu-id="1b871-149">These virtual disks have RCT IDs associated with them.</span></span>

</dd> <dt>

<span data-ttu-id="1b871-150">**виртуалсистемидентифиер**</span><span class="sxs-lookup"><span data-stu-id="1b871-150">**VirtualSystemIdentifier**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1b871-151">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="1b871-151">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="1b871-152">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="1b871-152">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="1b871-153">Квалификаторы: [**Key**](/windows/desktop/WmiSdk/key-qualifier), [**Моделкорреспонденце**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM \_ ComputerSystem**](cim-computersystem.md).**Name**")</span><span class="sxs-lookup"><span data-stu-id="1b871-153">Qualifiers: [**Key**](/windows/desktop/WmiSdk/key-qualifier), [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM\_ComputerSystem**](cim-computersystem.md).**Name**")</span></span>
</dt> </dl>

<span data-ttu-id="1b871-154">Имя [**\_ компьютерной платформы CIM**](cim-computersystem.md) , которой принадлежит эта точка ссылки</span><span class="sxs-lookup"><span data-stu-id="1b871-154">The name of the [**CIM\_ComputerSystem**](cim-computersystem.md) to which this reference point belongs</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="1b871-155">Требования</span><span class="sxs-lookup"><span data-stu-id="1b871-155">Requirements</span></span>



| <span data-ttu-id="1b871-156">Требование</span><span class="sxs-lookup"><span data-stu-id="1b871-156">Requirement</span></span> | <span data-ttu-id="1b871-157">Значение</span><span class="sxs-lookup"><span data-stu-id="1b871-157">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="1b871-158">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="1b871-158">Minimum supported client</span></span><br/> | <span data-ttu-id="1b871-159">Только для \[ настольных приложений Windows 10\]</span><span class="sxs-lookup"><span data-stu-id="1b871-159">Windows 10 \[desktop apps only\]</span></span><br/>                                                             |
| <span data-ttu-id="1b871-160">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="1b871-160">Minimum supported server</span></span><br/> | <span data-ttu-id="1b871-161">Windows Server 2016</span><span class="sxs-lookup"><span data-stu-id="1b871-161">Windows Server 2016</span></span><br/>                                                                          |
| <span data-ttu-id="1b871-162">Пространство имен</span><span class="sxs-lookup"><span data-stu-id="1b871-162">Namespace</span></span><br/>                | <span data-ttu-id="1b871-163">Корневая \\ виртуализация \\ версии 2</span><span class="sxs-lookup"><span data-stu-id="1b871-163">Root\\virtualization\\v2</span></span><br/>                                                                     |
| <span data-ttu-id="1b871-164">MOF</span><span class="sxs-lookup"><span data-stu-id="1b871-164">MOF</span></span><br/>                      | <dl> <span data-ttu-id="1b871-165"><dt>Виндовсвиртуализатион. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="1b871-165"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="1b871-166">DLL</span><span class="sxs-lookup"><span data-stu-id="1b871-166">DLL</span></span><br/>                      | <dl> <span data-ttu-id="1b871-167"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="1b871-167"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="1b871-168">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="1b871-168">See also</span></span>

<dl> <dt>

[<span data-ttu-id="1b871-169">**\_МАНАЖЕДЕЛЕМЕНТ CIM**</span><span class="sxs-lookup"><span data-stu-id="1b871-169">**CIM\_ManagedElement**</span></span>](cim-managedelement.md)
</dt> </dl>

 

