---
description: Представляет коллекцию опорных точек виртуальной системы.
ms.assetid: dc293f94-a683-468f-af05-ba99824d773e
title: Класс Msvm_ReferencePointCollection
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_ReferencePointCollection
- Msvm_ReferencePointCollection.CollectionID
- Msvm_ReferencePointCollection.ElementName
- Msvm_ReferencePointCollection.ReferencePointType
- Msvm_ReferencePointCollection.ConsistencyLevel
- Msvm_ReferencePointCollection.VirtualSystemCollectionId
- Msvm_ReferencePointCollection.HasAssociatedLog
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: 570590221ee8568d78e150fec3c359365c8434cd
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "103910143"
---
# <a name="msvm_referencepointcollection-class"></a><span data-ttu-id="f8be9-103">\_Класс мсвм референцепоинтколлектион</span><span class="sxs-lookup"><span data-stu-id="f8be9-103">Msvm\_ReferencePointCollection class</span></span>

<span data-ttu-id="f8be9-104">Представляет коллекцию опорных точек виртуальной системы.</span><span class="sxs-lookup"><span data-stu-id="f8be9-104">Represents a collection of virtual system reference points.</span></span>

<span data-ttu-id="f8be9-105">Следующий пример синтаксиса — упрощенный MOF-код, который включает все наследуемые свойства.</span><span class="sxs-lookup"><span data-stu-id="f8be9-105">The following syntax is simplified from Managed Object Format (MOF) code and includes all of the inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="f8be9-106">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="f8be9-106">Syntax</span></span>

``` syntax
[Dynamic, Provider("VmmsWmiInstanceAndMethodProvider"), AMENDMENT]
class Msvm_ReferencePointCollection : CIM_Collection
{
  string  CollectionID;
  string  ElementName;
  uint16  ReferencePointType;
  uint16  ConsistencyLevel;
  string  VirtualSystemCollectionId;
  boolean HasAssociatedLog;
};
```

## <a name="members"></a><span data-ttu-id="f8be9-107">Члены</span><span class="sxs-lookup"><span data-stu-id="f8be9-107">Members</span></span>

<span data-ttu-id="f8be9-108">Класс **мсвм \_ референцепоинтколлектион** имеет следующие типы членов:</span><span class="sxs-lookup"><span data-stu-id="f8be9-108">The **Msvm\_ReferencePointCollection** class has these types of members:</span></span>

-   [<span data-ttu-id="f8be9-109">Свойства</span><span class="sxs-lookup"><span data-stu-id="f8be9-109">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="f8be9-110">Свойства</span><span class="sxs-lookup"><span data-stu-id="f8be9-110">Properties</span></span>

<span data-ttu-id="f8be9-111">Класс **мсвм \_ референцепоинтколлектион** имеет следующие свойства.</span><span class="sxs-lookup"><span data-stu-id="f8be9-111">The **Msvm\_ReferencePointCollection** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="f8be9-112">**CollectionID**</span><span class="sxs-lookup"><span data-stu-id="f8be9-112">**CollectionID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f8be9-113">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="f8be9-113">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="f8be9-114">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="f8be9-114">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="f8be9-115">Квалификаторы: [**ключ**](/windows/desktop/WmiSdk/key-qualifier), [**Переопределение**](/windows/desktop/WmiSdk/standard-qualifiers) ("CollectionID"), [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (256)</span><span class="sxs-lookup"><span data-stu-id="f8be9-115">Qualifiers: [**Key**](/windows/desktop/WmiSdk/key-qualifier), [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("CollectionID"), [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (256)</span></span>
</dt> </dl>

<span data-ttu-id="f8be9-116">Уникальная идентификация объекта коллекции.</span><span class="sxs-lookup"><span data-stu-id="f8be9-116">The unique identification of the collection object.</span></span>

</dd> <dt>

<span data-ttu-id="f8be9-117">**ConsistencyLevel**</span><span class="sxs-lookup"><span data-stu-id="f8be9-117">**ConsistencyLevel**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f8be9-118">Тип данных: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="f8be9-118">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="f8be9-119">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="f8be9-119">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="f8be9-120">Уровень согласованности контрольной точки.</span><span class="sxs-lookup"><span data-stu-id="f8be9-120">Consistency level of the reference point.</span></span>

<dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="f8be9-121"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Неизвестно** (0)</span><span class="sxs-lookup"><span data-stu-id="f8be9-121"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (0)</span></span>


</dt> <dd></dd> <dt>

<span id="Crash_Consistent"></span><span id="crash_consistent"></span><span id="CRASH_CONSISTENT"></span>

<span data-ttu-id="f8be9-122"><span id="Crash_Consistent"></span><span id="crash_consistent"></span><span id="CRASH_CONSISTENT"></span>**Отказоустойчивость (1** )</span><span class="sxs-lookup"><span data-stu-id="f8be9-122"><span id="Crash_Consistent"></span><span id="crash_consistent"></span><span id="CRASH_CONSISTENT"></span>**Crash Consistent** (1)</span></span>


</dt> <dd>

<span data-ttu-id="f8be9-123">Эталонная точка указывает на момент времени, когда виртуальная система находилась в состоянии сбоя.</span><span class="sxs-lookup"><span data-stu-id="f8be9-123">The reference point indicates a point in time when the virtual system was in crash consistent state.</span></span>

</dd> <dt>

<span id="Application_Consistent"></span><span id="application_consistent"></span><span id="APPLICATION_CONSISTENT"></span>

<span data-ttu-id="f8be9-124"><span id="Application_Consistent"></span><span id="application_consistent"></span><span id="APPLICATION_CONSISTENT"></span>С **совместимостью приложений** (2)</span><span class="sxs-lookup"><span data-stu-id="f8be9-124"><span id="Application_Consistent"></span><span id="application_consistent"></span><span id="APPLICATION_CONSISTENT"></span>**Application Consistent** (2)</span></span>


</dt> <dd>

<span data-ttu-id="f8be9-125">Эталонная точка указывает на момент времени, когда виртуальная система находилась в состоянии совместимости с приложениями.</span><span class="sxs-lookup"><span data-stu-id="f8be9-125">The reference point indicates a point in time when the virtual system was in application consistent state.</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="f8be9-126">**ElementName**</span><span class="sxs-lookup"><span data-stu-id="f8be9-126">**ElementName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f8be9-127">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="f8be9-127">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="f8be9-128">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="f8be9-128">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="f8be9-129">Квалификаторы: [**override**](/windows/desktop/WmiSdk/standard-qualifiers) ("ElementName")</span><span class="sxs-lookup"><span data-stu-id="f8be9-129">Qualifiers: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("ElementName")</span></span>
</dt> </dl>

<span data-ttu-id="f8be9-130">Определяемое пользователем имя коллекции.</span><span class="sxs-lookup"><span data-stu-id="f8be9-130">An user-defined name for the collection.</span></span> <span data-ttu-id="f8be9-131">Обратите внимание, что это не обязательно должно быть уникальным.</span><span class="sxs-lookup"><span data-stu-id="f8be9-131">Note this is not guaranteed to be unique.</span></span>

</dd> <dt>

<span data-ttu-id="f8be9-132">**хасассоЦиатедлог**</span><span class="sxs-lookup"><span data-stu-id="f8be9-132">**HasAssociatedLog**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f8be9-133">Тип данных: **логический**</span><span class="sxs-lookup"><span data-stu-id="f8be9-133">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="f8be9-134">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="f8be9-134">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="f8be9-135">**значение true** , если все точки ссылки на элементы имеют связанные журналы.</span><span class="sxs-lookup"><span data-stu-id="f8be9-135">**true** if all the member reference points have associated logs.</span></span> <span data-ttu-id="f8be9-136">Это допустимо только для опорных точек на основе журналов.</span><span class="sxs-lookup"><span data-stu-id="f8be9-136">This is valid only for log based reference points.</span></span> <span data-ttu-id="f8be9-137">Для опорных точек на основе RCT **хасассоЦиатедлог** имеет значение **false**.</span><span class="sxs-lookup"><span data-stu-id="f8be9-137">For RCT based reference points, **HasAssociatedLog** is set to **false**.</span></span> <span data-ttu-id="f8be9-138">Для контрольных точек на основе журналов после удаления журнала **хасассоЦиатедлог** становится **ложным**.</span><span class="sxs-lookup"><span data-stu-id="f8be9-138">For log based reference points, once the log is discarded **HasAssociatedLog** becomes **false**.</span></span>

</dd> <dt>

<span data-ttu-id="f8be9-139">**референцепоинттипе**</span><span class="sxs-lookup"><span data-stu-id="f8be9-139">**ReferencePointType**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f8be9-140">Тип данных: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="f8be9-140">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="f8be9-141">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="f8be9-141">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="f8be9-142">Квалификаторы: [ **в**](/windows/desktop/WmiSdk/standard-qualifiers)</span><span class="sxs-lookup"><span data-stu-id="f8be9-142">Qualifiers: [**In**](/windows/desktop/WmiSdk/standard-qualifiers)</span></span>
</dt> </dl>

<span data-ttu-id="f8be9-143">Указывает тип контрольной точки.</span><span class="sxs-lookup"><span data-stu-id="f8be9-143">Indicates the type of the reference point.</span></span>

<dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="f8be9-144"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Неизвестно** (0)</span><span class="sxs-lookup"><span data-stu-id="f8be9-144"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (0)</span></span>


</dt> <dd></dd> <dt>

<span id="Log_based"></span><span id="log_based"></span><span id="LOG_BASED"></span>

<span data-ttu-id="f8be9-145"><span id="Log_based"></span><span id="log_based"></span><span id="LOG_BASED"></span>**На основе журнала** (1)</span><span class="sxs-lookup"><span data-stu-id="f8be9-145"><span id="Log_based"></span><span id="log_based"></span><span id="LOG_BASED"></span>**Log based** (1)</span></span>


</dt> <dd>

<span data-ttu-id="f8be9-146">Отслеживание журнала реплики Hyper-V.</span><span class="sxs-lookup"><span data-stu-id="f8be9-146">Hyper-V replica log tracking.</span></span>

</dd> <dt>

<span id="RCT_based"></span><span id="rct_based"></span><span id="RCT_BASED"></span>

<span data-ttu-id="f8be9-147"><span id="RCT_based"></span><span id="rct_based"></span><span id="RCT_BASED"></span>**На основе RCT** (2)</span><span class="sxs-lookup"><span data-stu-id="f8be9-147"><span id="RCT_based"></span><span id="rct_based"></span><span id="RCT_BASED"></span>**RCT based** (2)</span></span>


</dt> <dd>

<span data-ttu-id="f8be9-148">На основе устойчивых Отслеживание изменений виртуальных дисков.</span><span class="sxs-lookup"><span data-stu-id="f8be9-148">Based on Resilient Change Tracking of virtual disks.</span></span>

</dd> <dt>

<span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>

<span data-ttu-id="f8be9-149"><span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**Зарезервировано DMTF** (..)</span><span class="sxs-lookup"><span data-stu-id="f8be9-149"><span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF Reserved** (..)</span></span>


</dt> <dd></dd> <dt>

<span id="Vendor_Specific"></span><span id="vendor_specific"></span><span id="VENDOR_SPECIFIC"></span>

<span data-ttu-id="f8be9-150"><span id="Vendor_Specific"></span><span id="vendor_specific"></span><span id="VENDOR_SPECIFIC"></span>**Зависит от поставщика** (32768.65 535)</span><span class="sxs-lookup"><span data-stu-id="f8be9-150"><span id="Vendor_Specific"></span><span id="vendor_specific"></span><span id="VENDOR_SPECIFIC"></span>**Vendor Specific** (32768..65535)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="f8be9-151">**виртуалсистемколлектионид**</span><span class="sxs-lookup"><span data-stu-id="f8be9-151">**VirtualSystemCollectionId**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f8be9-152">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="f8be9-152">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="f8be9-153">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="f8be9-153">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="f8be9-154">Квалификаторы: [**Key**](/windows/desktop/WmiSdk/key-qualifier), [**Моделкорреспонденце**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**мсвм \_ виртуалсистемколлектион**](msvm-virtualsystemcollection.md).**CollectionID**")</span><span class="sxs-lookup"><span data-stu-id="f8be9-154">Qualifiers: [**Key**](/windows/desktop/WmiSdk/key-qualifier), [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**Msvm\_VirtualSystemCollection**](msvm-virtualsystemcollection.md).**CollectionID**")</span></span>
</dt> </dl>

<span data-ttu-id="f8be9-155">Идентификатор [**\_ виртуалсистемколлектион мсвм**](msvm-virtualsystemcollection.md) , которому принадлежит данная точка ссылки.</span><span class="sxs-lookup"><span data-stu-id="f8be9-155">The identifier of the [**Msvm\_VirtualSystemCollection**](msvm-virtualsystemcollection.md) to which this reference point belongs.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="f8be9-156">Требования</span><span class="sxs-lookup"><span data-stu-id="f8be9-156">Requirements</span></span>



| <span data-ttu-id="f8be9-157">Требование</span><span class="sxs-lookup"><span data-stu-id="f8be9-157">Requirement</span></span> | <span data-ttu-id="f8be9-158">Значение</span><span class="sxs-lookup"><span data-stu-id="f8be9-158">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="f8be9-159">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="f8be9-159">Minimum supported client</span></span><br/> | <span data-ttu-id="f8be9-160">Только для \[ настольных приложений Windows 10\]</span><span class="sxs-lookup"><span data-stu-id="f8be9-160">Windows 10 \[desktop apps only\]</span></span><br/>                                                             |
| <span data-ttu-id="f8be9-161">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="f8be9-161">Minimum supported server</span></span><br/> | <span data-ttu-id="f8be9-162">Windows Server 2016</span><span class="sxs-lookup"><span data-stu-id="f8be9-162">Windows Server 2016</span></span><br/>                                                                          |
| <span data-ttu-id="f8be9-163">Пространство имен</span><span class="sxs-lookup"><span data-stu-id="f8be9-163">Namespace</span></span><br/>                | <span data-ttu-id="f8be9-164">Корневая \\ виртуализация \\ версии 2</span><span class="sxs-lookup"><span data-stu-id="f8be9-164">Root\\virtualization\\v2</span></span><br/>                                                                     |
| <span data-ttu-id="f8be9-165">MOF</span><span class="sxs-lookup"><span data-stu-id="f8be9-165">MOF</span></span><br/>                      | <dl> <span data-ttu-id="f8be9-166"><dt>Виндовсвиртуализатион. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="f8be9-166"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="f8be9-167">DLL</span><span class="sxs-lookup"><span data-stu-id="f8be9-167">DLL</span></span><br/>                      | <dl> <span data-ttu-id="f8be9-168"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="f8be9-168"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="f8be9-169">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="f8be9-169">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f8be9-170">**\_Коллекция CIM**</span><span class="sxs-lookup"><span data-stu-id="f8be9-170">**CIM\_Collection**</span></span>](cim-collection.md)
</dt> </dl>

 

