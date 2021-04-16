---
description: Используется в методе Жетсуммаринформатион \_ класса мсвм виртуалсистемманажементсервице для быстрого получения общих сведений, связанных с виртуальной системой или моментальным снимком.
ms.assetid: f8daa387-d812-4f44-bf5f-e0a0c18c6db8
title: Класс Msvm_SummaryInformationBase
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_SummaryInformationBase
- Msvm_SummaryInformationBase.InstanceID
- Msvm_SummaryInformationBase.CreationTime
- Msvm_SummaryInformationBase.ElementName
- Msvm_SummaryInformationBase.EnabledState
- Msvm_SummaryInformationBase.OtherEnabledState
- Msvm_SummaryInformationBase.HealthState
- Msvm_SummaryInformationBase.Name
- Msvm_SummaryInformationBase.Notes
- Msvm_SummaryInformationBase.Version
- Msvm_SummaryInformationBase.NumberOfProcessors
- Msvm_SummaryInformationBase.OperationalStatus
- Msvm_SummaryInformationBase.StatusDescriptions
- Msvm_SummaryInformationBase.UpTime
- Msvm_SummaryInformationBase.EnhancedSessionModeState
- Msvm_SummaryInformationBase.VirtualSwitchNames
- Msvm_SummaryInformationBase.VirtualSystemSubType
- Msvm_SummaryInformationBase.HostComputerSystemName
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: 65c20239673f279babba2581c4300f373f1392bb
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "105650626"
---
# <a name="msvm_summaryinformationbase-class"></a><span data-ttu-id="ad6e3-103">\_Класс мсвм суммаринформатионбасе</span><span class="sxs-lookup"><span data-stu-id="ad6e3-103">Msvm\_SummaryInformationBase class</span></span>

<span data-ttu-id="ad6e3-104">Используется в методе [**жетсуммаринформатион**](getsummaryinformation-msvm-virtualsystemmanagementservice.md) класса [**мсвм \_ виртуалсистемманажементсервице**](msvm-virtualsystemmanagementservice.md) для быстрого получения общих сведений, связанных с виртуальной системой или моментальным снимком.</span><span class="sxs-lookup"><span data-stu-id="ad6e3-104">Used in the [**GetSummaryInformation**](getsummaryinformation-msvm-virtualsystemmanagementservice.md) method in the [**Msvm\_VirtualSystemManagementService**](msvm-virtualsystemmanagementservice.md) class to quickly retrieve common information related to a virtual system or snapshot.</span></span>

<span data-ttu-id="ad6e3-105">Следующий пример синтаксиса — упрощенный MOF-код, который включает все наследуемые свойства.</span><span class="sxs-lookup"><span data-stu-id="ad6e3-105">The following syntax is simplified from Managed Object Format (MOF) code and includes all of the inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="ad6e3-106">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="ad6e3-106">Syntax</span></span>

``` syntax
[Abstract, Provider("VmmsWmiInstanceAndMethodProvider"), AMENDMENT]
class Msvm_SummaryInformationBase : CIM_View
{
  string   InstanceID;
  DateTime CreationTime;
  string   ElementName;
  uint16   EnabledState;
  string   OtherEnabledState;
  uint16   HealthState;
  string   Name;
  string   Notes;
  string   Version;
  uint16   NumberOfProcessors;
  uint16   OperationalStatus[];
  string   StatusDescriptions[];
  uint64   UpTime;
  uint16   EnhancedSessionModeState;
  string   VirtualSwitchNames[];
  string   VirtualSystemSubType;
  string   HostComputerSystemName;
};
```

## <a name="members"></a><span data-ttu-id="ad6e3-107">Члены</span><span class="sxs-lookup"><span data-stu-id="ad6e3-107">Members</span></span>

<span data-ttu-id="ad6e3-108">Класс **мсвм \_ суммаринформатионбасе** имеет следующие типы членов:</span><span class="sxs-lookup"><span data-stu-id="ad6e3-108">The **Msvm\_SummaryInformationBase** class has these types of members:</span></span>

-   [<span data-ttu-id="ad6e3-109">Свойства</span><span class="sxs-lookup"><span data-stu-id="ad6e3-109">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="ad6e3-110">Свойства</span><span class="sxs-lookup"><span data-stu-id="ad6e3-110">Properties</span></span>

<span data-ttu-id="ad6e3-111">Класс **мсвм \_ суммаринформатионбасе** имеет следующие свойства.</span><span class="sxs-lookup"><span data-stu-id="ad6e3-111">The **Msvm\_SummaryInformationBase** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="ad6e3-112">**CreationTime**</span><span class="sxs-lookup"><span data-stu-id="ad6e3-112">**CreationTime**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ad6e3-113">Тип данных: **DateTime**</span><span class="sxs-lookup"><span data-stu-id="ad6e3-113">Data type: **DateTime**</span></span>
</dt> <dt>

<span data-ttu-id="ad6e3-114">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="ad6e3-114">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="ad6e3-115">Время создания виртуальной системы или моментального снимка.</span><span class="sxs-lookup"><span data-stu-id="ad6e3-115">The time at which the virtual system or snapshot was created.</span></span>

</dd> <dt>

<span data-ttu-id="ad6e3-116">**ElementName**</span><span class="sxs-lookup"><span data-stu-id="ad6e3-116">**ElementName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ad6e3-117">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="ad6e3-117">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="ad6e3-118">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="ad6e3-118">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="ad6e3-119">Квалификаторы: [**override**](/windows/desktop/WmiSdk/standard-qualifiers) ("CIM \_ манажеделемент. ElementName")</span><span class="sxs-lookup"><span data-stu-id="ad6e3-119">Qualifiers: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("CIM\_ManagedElement.ElementName")</span></span>
</dt> </dl>

<span data-ttu-id="ad6e3-120">Понятное имя виртуальной системы или моментального снимка.</span><span class="sxs-lookup"><span data-stu-id="ad6e3-120">The friendly name for the virtual system or snapshot.</span></span>

</dd> <dt>

<span data-ttu-id="ad6e3-121">**EnabledState**</span><span class="sxs-lookup"><span data-stu-id="ad6e3-121">**EnabledState**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ad6e3-122">Тип данных: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="ad6e3-122">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="ad6e3-123">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="ad6e3-123">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="ad6e3-124">Текущее состояние виртуальной системы или моментального снимка.</span><span class="sxs-lookup"><span data-stu-id="ad6e3-124">The current state of the virtual system or snapshot.</span></span>

</dd> <dt>

<span data-ttu-id="ad6e3-125">**енханцедсессионмодестате**</span><span class="sxs-lookup"><span data-stu-id="ad6e3-125">**EnhancedSessionModeState**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ad6e3-126">Тип данных: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="ad6e3-126">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="ad6e3-127">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="ad6e3-127">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="ad6e3-128">Указывает, разрешены ли для узла подключения в расширенном режиме, а также если они разрешены, независимо от того, доступны ли они для виртуальной машины.</span><span class="sxs-lookup"><span data-stu-id="ad6e3-128">Indicates whether or not enhanced mode connections are allowed by the host and if allowed, whether or not they are available to the virtual machine.</span></span>

<dt>

<span id="Allowed_and_available"></span><span id="allowed_and_available"></span><span id="ALLOWED_AND_AVAILABLE"></span>

<span data-ttu-id="ad6e3-129">**Разрешено и доступно** (2)</span><span class="sxs-lookup"><span data-stu-id="ad6e3-129">**Allowed and available** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Not_allowed"></span><span id="not_allowed"></span><span id="NOT_ALLOWED"></span>

<span data-ttu-id="ad6e3-130">**Не разрешено** (3)</span><span class="sxs-lookup"><span data-stu-id="ad6e3-130">**Not allowed** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="Allowed_but_not_available"></span><span id="allowed_but_not_available"></span><span id="ALLOWED_BUT_NOT_AVAILABLE"></span>

<span data-ttu-id="ad6e3-131">**Разрешено, но недоступно** (6)</span><span class="sxs-lookup"><span data-stu-id="ad6e3-131">**Allowed but not available** (6)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="ad6e3-132">**HealthState**</span><span class="sxs-lookup"><span data-stu-id="ad6e3-132">**HealthState**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ad6e3-133">Тип данных: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="ad6e3-133">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="ad6e3-134">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="ad6e3-134">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="ad6e3-135">Текущее состояние работоспособности виртуальной системы.</span><span class="sxs-lookup"><span data-stu-id="ad6e3-135">The current health state for the virtual system.</span></span> <span data-ttu-id="ad6e3-136">Это свойство является недопустимым для экземпляров [**мсвм \_ SummaryInformation**](msvm-summaryinformation.md) , представляющих моментальный снимок виртуальной системы.</span><span class="sxs-lookup"><span data-stu-id="ad6e3-136">This property is not valid for instances of [**Msvm\_SummaryInformation**](msvm-summaryinformation.md) representing a virtual system snapshot.</span></span>

</dd> <dt>

<span data-ttu-id="ad6e3-137">**хосткомпутерсистемнаме**</span><span class="sxs-lookup"><span data-stu-id="ad6e3-137">**HostComputerSystemName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ad6e3-138">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="ad6e3-138">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="ad6e3-139">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="ad6e3-139">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="ad6e3-140">Имя компьютера, на котором размещена эта виртуальная машина.</span><span class="sxs-lookup"><span data-stu-id="ad6e3-140">The name of the computer hosting this virtual machine.</span></span>

</dd> <dt>

<span data-ttu-id="ad6e3-141">**InstanceID**</span><span class="sxs-lookup"><span data-stu-id="ad6e3-141">**InstanceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ad6e3-142">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="ad6e3-142">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="ad6e3-143">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="ad6e3-143">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="ad6e3-144">Квалификаторы: [**override**](/windows/desktop/WmiSdk/standard-qualifiers) ("CIM \_ манажеделемент. InstanceId"), [**ключ**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="ad6e3-144">Qualifiers: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("CIM\_ManagedElement.InstanceID"), [**Key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

<span data-ttu-id="ad6e3-145">InstanceID — это необязательное свойство, которое можно использовать для непрозрачного и уникального определения экземпляра этого класса в области действия экземпляра пространства имен.</span><span class="sxs-lookup"><span data-stu-id="ad6e3-145">InstanceID is an optional property that may be used to opaquely and uniquely identify an instance of this class within the scope of the instantiating Namespace.</span></span> <span data-ttu-id="ad6e3-146">Различные подклассы этого класса могут переопределять это свойство, чтобы сделать его обязательным, или ключ.</span><span class="sxs-lookup"><span data-stu-id="ad6e3-146">Various subclasses of this class may override this property to make it required, or a key.</span></span> <span data-ttu-id="ad6e3-147">Такие подклассы также могут изменять предпочтительные алгоритмы, чтобы обеспечить уникальность, определенную ниже.</span><span class="sxs-lookup"><span data-stu-id="ad6e3-147">Such subclasses may also modify the preferred algorithms for ensuring uniqueness that are defined below.</span></span>

<span data-ttu-id="ad6e3-148">Чтобы обеспечить уникальность в пространстве имен, значение InstanceID должно быть создано с использованием следующего "предпочтительного" алгоритма:</span><span class="sxs-lookup"><span data-stu-id="ad6e3-148">To ensure uniqueness within the NameSpace, the value of InstanceID should be constructed using the following "preferred" algorithm:</span></span>

<span data-ttu-id="ad6e3-149"><OrgID>:<LocalID></span><span class="sxs-lookup"><span data-stu-id="ad6e3-149"><OrgID>:<LocalID></span></span>

<span data-ttu-id="ad6e3-150">Где <OrgID> и <LocalID> разделяются двоеточием (:), а <OrgID> в месте должно быть указано уникальное имя, которое принадлежит бизнес-сущности, создающему или определяющему InstanceId или зарегистрированный идентификатор, назначенный бизнес-сущностю распознанным глобальным центром сертификации.</span><span class="sxs-lookup"><span data-stu-id="ad6e3-150">Where <OrgID> and <LocalID> are separated by a colon (:), and where <OrgID> must include a copyrighted, trademarked, or otherwise unique name that is owned by the business entity that is creating or defining the InstanceID or that is a registered ID assigned to the business entity by a recognized global authority.</span></span> <span data-ttu-id="ad6e3-151">(Это требование аналогично <Schema Name> \_ <Class Name> Структура имен классов схемы.) Кроме того, чтобы обеспечить уникальность, <OrgID> не следует включать двоеточие (:).</span><span class="sxs-lookup"><span data-stu-id="ad6e3-151">(This requirement is similar to the <Schema Name>\_<Class Name> structure of Schema class names.) In addition, to ensure uniqueness, <OrgID> must not contain a colon (:).</span></span> <span data-ttu-id="ad6e3-152">При использовании этого алгоритма первым двоеточием, которое должно находиться в InstanceID, должен находиться в диапазоне от <OrgID> до <LocalID> .</span><span class="sxs-lookup"><span data-stu-id="ad6e3-152">When using this algorithm, the first colon to appear in InstanceID must appear between <OrgID> and <LocalID>.</span></span>

<span data-ttu-id="ad6e3-153"><LocalID> выбирается бизнес-сущностью и не должна использоваться повторно для обнаружения различных базовых (реальных) элементов.</span><span class="sxs-lookup"><span data-stu-id="ad6e3-153"><LocalID> is chosen by the business entity and should not be reused to identify different underlying (real-world) elements.</span></span> <span data-ttu-id="ad6e3-154">Если не равно NULL и указанный выше алгоритм не используется, определяющая сущность должна гарантировать, что результирующий InstanceID не будет повторно использоваться в любых InstanceId, созданных этим или другими поставщиками для пространства имен данного экземпляра.</span><span class="sxs-lookup"><span data-stu-id="ad6e3-154">If not null and the above "preferred" algorithm is not used, the defining entity must assure that the resulting InstanceID is not reused across any InstanceIDs produced by this or other providers for the NameSpace of this instance.</span></span>

<span data-ttu-id="ad6e3-155">Если для экземпляров, определяемых DMTF, не задано значение null, то для набора, для которого задано значение CIM, необходимо использовать "предпочтительный" алгоритм <OrgID> .</span><span class="sxs-lookup"><span data-stu-id="ad6e3-155">If not set to null for DMTF-defined instances, the "preferred" algorithm must be used with the <OrgID> set to CIM.</span></span>

</dd> <dt>

<span data-ttu-id="ad6e3-156">**Name**</span><span class="sxs-lookup"><span data-stu-id="ad6e3-156">**Name**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ad6e3-157">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="ad6e3-157">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="ad6e3-158">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="ad6e3-158">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="ad6e3-159">Уникальное имя виртуальной системы или моментального снимка.</span><span class="sxs-lookup"><span data-stu-id="ad6e3-159">The unique name for the virtual system or snapshot.</span></span>

</dd> <dt>

<span data-ttu-id="ad6e3-160">**Примечания**</span><span class="sxs-lookup"><span data-stu-id="ad6e3-160">**Notes**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ad6e3-161">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="ad6e3-161">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="ad6e3-162">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="ad6e3-162">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="ad6e3-163">Примечания, связанные с виртуальной системой или моментальным снимком.</span><span class="sxs-lookup"><span data-stu-id="ad6e3-163">The notes associated with the virtual system or snapshot.</span></span>

</dd> <dt>

<span data-ttu-id="ad6e3-164">**NumberOfProcessors**</span><span class="sxs-lookup"><span data-stu-id="ad6e3-164">**NumberOfProcessors**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ad6e3-165">Тип данных: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="ad6e3-165">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="ad6e3-166">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="ad6e3-166">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="ad6e3-167">Общее число виртуальных процессоров, выделенных для виртуальной системы или моментального снимка.</span><span class="sxs-lookup"><span data-stu-id="ad6e3-167">The total number of virtual processors allocated to the virtual system or snapshot.</span></span>

</dd> <dt>

<span data-ttu-id="ad6e3-168">**OperationalStatus**</span><span class="sxs-lookup"><span data-stu-id="ad6e3-168">**OperationalStatus**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ad6e3-169">Тип данных: **UInt16** , массив</span><span class="sxs-lookup"><span data-stu-id="ad6e3-169">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="ad6e3-170">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="ad6e3-170">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="ad6e3-171">Квалификаторы: [**arrayType**](/windows/desktop/WmiSdk/standard-qualifiers) ("индексированный")</span><span class="sxs-lookup"><span data-stu-id="ad6e3-171">Qualifiers: [**ArrayType**](/windows/desktop/WmiSdk/standard-qualifiers) ("Indexed")</span></span>
</dt> </dl>

<span data-ttu-id="ad6e3-172">Текущее состояние элемента.</span><span class="sxs-lookup"><span data-stu-id="ad6e3-172">The current status of the element.</span></span>

</dd> <dt>

<span data-ttu-id="ad6e3-173">**осеренабледстате**</span><span class="sxs-lookup"><span data-stu-id="ad6e3-173">**OtherEnabledState**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ad6e3-174">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="ad6e3-174">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="ad6e3-175">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="ad6e3-175">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="ad6e3-176">Строка, описывающая включенное или отключенное состояние элемента, если свойство **EnabledState** имеет значение 1 ("другое").</span><span class="sxs-lookup"><span data-stu-id="ad6e3-176">A string that describes the enabled or disabled state of the element when the **EnabledState** property is set to 1 ("Other").</span></span> <span data-ttu-id="ad6e3-177">Для этого свойства необходимо задать значение null, если параметр **EnabledState** имеет любое значение, отличное от 1.</span><span class="sxs-lookup"><span data-stu-id="ad6e3-177">This property must be set to null when **EnabledState** is any value other than 1.</span></span>

</dd> <dt>

<span data-ttu-id="ad6e3-178">**статусдескриптионс**</span><span class="sxs-lookup"><span data-stu-id="ad6e3-178">**StatusDescriptions**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ad6e3-179">Тип данных: массив **строк**</span><span class="sxs-lookup"><span data-stu-id="ad6e3-179">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="ad6e3-180">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="ad6e3-180">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="ad6e3-181">Квалификаторы: [**arrayType**](/windows/desktop/WmiSdk/standard-qualifiers) ("индексированный")</span><span class="sxs-lookup"><span data-stu-id="ad6e3-181">Qualifiers: [**ArrayType**](/windows/desktop/WmiSdk/standard-qualifiers) ("Indexed")</span></span>
</dt> </dl>

<span data-ttu-id="ad6e3-182">Строки, описывающие различные значения массива **OperationalStatus** .</span><span class="sxs-lookup"><span data-stu-id="ad6e3-182">Strings that describe the various **OperationalStatus** array values.</span></span>

</dd> <dt>

<span data-ttu-id="ad6e3-183">**Просто**</span><span class="sxs-lookup"><span data-stu-id="ad6e3-183">**UpTime**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ad6e3-184">Тип данных: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="ad6e3-184">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="ad6e3-185">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="ad6e3-185">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="ad6e3-186">Количество времени, прошедшее с момента последней загрузки виртуальной системы.</span><span class="sxs-lookup"><span data-stu-id="ad6e3-186">The amount of time since the virtual system was last booted.</span></span> <span data-ttu-id="ad6e3-187">Это свойство является недопустимым для экземпляров [**мсвм \_ SummaryInformation**](msvm-summaryinformation.md) , представляющих моментальный снимок виртуальной системы.</span><span class="sxs-lookup"><span data-stu-id="ad6e3-187">This property is not valid for instances of [**Msvm\_SummaryInformation**](msvm-summaryinformation.md) representing a virtual system snapshot.</span></span>

</dd> <dt>

<span data-ttu-id="ad6e3-188">**Version**</span><span class="sxs-lookup"><span data-stu-id="ad6e3-188">**Version**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ad6e3-189">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="ad6e3-189">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="ad6e3-190">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="ad6e3-190">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="ad6e3-191">Версия виртуальной системы в формате "основная. Дополнительная"; Например, "2,0".</span><span class="sxs-lookup"><span data-stu-id="ad6e3-191">The version of the virtual system in a format of "major.minor"; for example, "2.0".</span></span>

</dd> <dt>

<span data-ttu-id="ad6e3-192">**виртуалсвитчнамес**</span><span class="sxs-lookup"><span data-stu-id="ad6e3-192">**VirtualSwitchNames**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ad6e3-193">Тип данных: массив **строк**</span><span class="sxs-lookup"><span data-stu-id="ad6e3-193">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="ad6e3-194">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="ad6e3-194">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="ad6e3-195">Квалификаторы: [**arrayType**](/windows/desktop/WmiSdk/standard-qualifiers) ("индексированный")</span><span class="sxs-lookup"><span data-stu-id="ad6e3-195">Qualifiers: [**ArrayType**](/windows/desktop/WmiSdk/standard-qualifiers) ("Indexed")</span></span>
</dt> </dl>

<span data-ttu-id="ad6e3-196">Строки, в которых перечислены понятные имена виртуальных коммутаторов, к которым подключена виртуальная машина.</span><span class="sxs-lookup"><span data-stu-id="ad6e3-196">Strings that list the friendly names of the virtual switches the VM is connected to.</span></span>

</dd> <dt>

<span data-ttu-id="ad6e3-197">**VirtualSystemSubType**</span><span class="sxs-lookup"><span data-stu-id="ad6e3-197">**VirtualSystemSubType**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ad6e3-198">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="ad6e3-198">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="ad6e3-199">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="ad6e3-199">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="ad6e3-200">Подтип виртуальной системы.</span><span class="sxs-lookup"><span data-stu-id="ad6e3-200">The subtype of the virtual system.</span></span>

<dt>

<span id="Microsoft_Hyper-V_SubType_1"></span><span id="microsoft_hyper-v_subtype_1"></span><span id="MICROSOFT_HYPER-V_SUBTYPE_1"></span>

<span data-ttu-id="ad6e3-201">**Microsoft: Hyper-v: подтип: 1** ("Microsoft: Hyper-V: подтип: 1")</span><span class="sxs-lookup"><span data-stu-id="ad6e3-201">**Microsoft:Hyper-V:SubType:1** ("Microsoft:Hyper-V:SubType:1")</span></span>


</dt> <dd></dd> <dt>

<span id="Microsoft_Hyper-V_SubType_2"></span><span id="microsoft_hyper-v_subtype_2"></span><span id="MICROSOFT_HYPER-V_SUBTYPE_2"></span>

<span data-ttu-id="ad6e3-202">**Microsoft: Hyper-v: подтип: 2** ("Microsoft: Hyper-V: подтип: 2")</span><span class="sxs-lookup"><span data-stu-id="ad6e3-202">**Microsoft:Hyper-V:SubType:2** ("Microsoft:Hyper-V:SubType:2")</span></span>


<span data-ttu-id="ad6e3-203"></dt> <dd></dd> </dl>

</dd> </dl></span><span class="sxs-lookup"><span data-stu-id="ad6e3-203"></dt> <dd></dd> </dl>

</dd> </dl></span></span>

## <a name="requirements"></a><span data-ttu-id="ad6e3-204">Требования</span><span class="sxs-lookup"><span data-stu-id="ad6e3-204">Requirements</span></span>



| <span data-ttu-id="ad6e3-205">Требование</span><span class="sxs-lookup"><span data-stu-id="ad6e3-205">Requirement</span></span> | <span data-ttu-id="ad6e3-206">Значение</span><span class="sxs-lookup"><span data-stu-id="ad6e3-206">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="ad6e3-207">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="ad6e3-207">Minimum supported client</span></span><br/> | <span data-ttu-id="ad6e3-208">\[Только для настольных приложений Windows 10 версии 1703\]</span><span class="sxs-lookup"><span data-stu-id="ad6e3-208">Windows 10, version 1703 \[desktop apps only\]</span></span><br/>                                               |
| <span data-ttu-id="ad6e3-209">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="ad6e3-209">Minimum supported server</span></span><br/> | <span data-ttu-id="ad6e3-210">Windows Server 2016</span><span class="sxs-lookup"><span data-stu-id="ad6e3-210">Windows Server 2016</span></span><br/>                                                                          |
| <span data-ttu-id="ad6e3-211">Пространство имен</span><span class="sxs-lookup"><span data-stu-id="ad6e3-211">Namespace</span></span><br/>                | <span data-ttu-id="ad6e3-212">Корневая \\ виртуализация \\ версии 2</span><span class="sxs-lookup"><span data-stu-id="ad6e3-212">Root\\virtualization\\v2</span></span><br/>                                                                     |
| <span data-ttu-id="ad6e3-213">MOF</span><span class="sxs-lookup"><span data-stu-id="ad6e3-213">MOF</span></span><br/>                      | <dl> <span data-ttu-id="ad6e3-214"><dt>Виндовсвиртуализатион. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="ad6e3-214"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="ad6e3-215">DLL</span><span class="sxs-lookup"><span data-stu-id="ad6e3-215">DLL</span></span><br/>                      | <dl> <span data-ttu-id="ad6e3-216"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="ad6e3-216"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="ad6e3-217">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="ad6e3-217">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ad6e3-218">**\_Представление CIM**</span><span class="sxs-lookup"><span data-stu-id="ad6e3-218">**CIM\_View**</span></span>](cim-view.md)
</dt> </dl>

 

