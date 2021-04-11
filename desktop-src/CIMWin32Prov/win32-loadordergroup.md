---
description: '\_Класс WMI лоадордерграуп инструментария Win32 представляет группу системных служб, определяющих зависимости выполнения.'
ms.assetid: 0aa3151e-6622-46b4-9050-4e1c4c720902
ms.tgt_platform: multiple
title: Класс Win32_LoadOrderGroup
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_LoadOrderGroup
- Win32_LoadOrderGroup.Caption
- Win32_LoadOrderGroup.Description
- Win32_LoadOrderGroup.InstallDate
- Win32_LoadOrderGroup.Status
- Win32_LoadOrderGroup.DriverEnabled
- Win32_LoadOrderGroup.GroupOrder
- Win32_LoadOrderGroup.Name
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: b81a6cb282018692fb72c8dbfe5ef0c5c74fe815
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104142502"
---
# <a name="win32_loadordergroup-class"></a><span data-ttu-id="742d6-103">\_Класс Win32 лоадордерграуп</span><span class="sxs-lookup"><span data-stu-id="742d6-103">Win32\_LoadOrderGroup class</span></span>

<span data-ttu-id="742d6-104">Класс **WMI \_ лоадордерграуп** [инструментария](/windows/desktop/WmiSdk/retrieving-a-class) Win32 представляет группу системных служб, определяющих зависимости выполнения.</span><span class="sxs-lookup"><span data-stu-id="742d6-104">The **Win32\_LoadOrderGroup** [WMI class](/windows/desktop/WmiSdk/retrieving-a-class) represents a group of system services that define execution dependencies.</span></span> <span data-ttu-id="742d6-105">Службы должны запускаться в порядке, указанном в группе порядок загрузки, так как службы зависят друг от друга.</span><span class="sxs-lookup"><span data-stu-id="742d6-105">The services must be initiated in the order specified by the Load Order Group, as the services are dependent on each other.</span></span> <span data-ttu-id="742d6-106">Для правильной работы этих зависимых служб требуется наличие предшествующих служб.</span><span class="sxs-lookup"><span data-stu-id="742d6-106">These dependent services require the presence of the antecedent services to function correctly.</span></span> <span data-ttu-id="742d6-107">Данные в этом классе порождены от поставщика из раздела реестра: **hKey \_ локальный \_ компьютер** \\ **System** \\ **CurrentControlSet** \\ **Control** \\ **ServiceGroupOrder**.</span><span class="sxs-lookup"><span data-stu-id="742d6-107">The data in this class is derived by the provider from the registry key: **HKEY\_LOCAL\_MACHINE**\\**System**\\**CurrentControlSet**\\**Control**\\**ServiceGroupOrder**.</span></span>

<span data-ttu-id="742d6-108">Следующий пример синтаксиса — упрощенный MOF-код, который включает все наследуемые свойства.</span><span class="sxs-lookup"><span data-stu-id="742d6-108">The following syntax is simplified from Managed Object Format (MOF) code and includes all of the inherited properties.</span></span> <span data-ttu-id="742d6-109">Свойства перечислены в алфавитном порядке, а не в MOF.</span><span class="sxs-lookup"><span data-stu-id="742d6-109">Properties are listed in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="742d6-110">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="742d6-110">Syntax</span></span>

``` syntax
[Dynamic, Provider("CIMWin32"), UUID("{8502C4D4-5FBB-11D2-AAC1-006008C78BC7}"), AMENDMENT]
class Win32_LoadOrderGroup : CIM_LogicalElement
{
  string   Caption;
  string   Description;
  datetime InstallDate;
  string   Status;
  boolean  DriverEnabled;
  uint32   GroupOrder;
  string   Name;
};
```

## <a name="members"></a><span data-ttu-id="742d6-111">Члены</span><span class="sxs-lookup"><span data-stu-id="742d6-111">Members</span></span>

<span data-ttu-id="742d6-112">Класс **Win32 \_ лоадордерграуп** имеет следующие типы членов:</span><span class="sxs-lookup"><span data-stu-id="742d6-112">The **Win32\_LoadOrderGroup** class has these types of members:</span></span>

-   [<span data-ttu-id="742d6-113">Свойства</span><span class="sxs-lookup"><span data-stu-id="742d6-113">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="742d6-114">Свойства</span><span class="sxs-lookup"><span data-stu-id="742d6-114">Properties</span></span>

<span data-ttu-id="742d6-115">Класс **Win32 \_ лоадордерграуп** имеет следующие свойства.</span><span class="sxs-lookup"><span data-stu-id="742d6-115">The **Win32\_LoadOrderGroup** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="742d6-116">**Заголовок**</span><span class="sxs-lookup"><span data-stu-id="742d6-116">**Caption**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="742d6-117">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="742d6-117">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="742d6-118">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="742d6-118">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="742d6-119">Квалификаторы: [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (64), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Caption")</span><span class="sxs-lookup"><span data-stu-id="742d6-119">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Caption")</span></span>
</dt> </dl>

<span data-ttu-id="742d6-120">Краткое текстовое описание объекта.</span><span class="sxs-lookup"><span data-stu-id="742d6-120">A short textual description of the object.</span></span>

<span data-ttu-id="742d6-121">Это свойство наследуется от [**CIM \_ манажедсистемелемент**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="742d6-121">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="742d6-122">**Описание**</span><span class="sxs-lookup"><span data-stu-id="742d6-122">**Description**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="742d6-123">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="742d6-123">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="742d6-124">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="742d6-124">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="742d6-125">Квалификаторы: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Описание")</span><span class="sxs-lookup"><span data-stu-id="742d6-125">Qualifiers: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Description")</span></span>
</dt> </dl>

<span data-ttu-id="742d6-126">Текстовое описание объекта.</span><span class="sxs-lookup"><span data-stu-id="742d6-126">A textual description of the object.</span></span>

<span data-ttu-id="742d6-127">Это свойство наследуется от [**CIM \_ манажедсистемелемент**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="742d6-127">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="742d6-128">**дриверенаблед**</span><span class="sxs-lookup"><span data-stu-id="742d6-128">**DriverEnabled**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="742d6-129">Тип данных: **логический**</span><span class="sxs-lookup"><span data-stu-id="742d6-129">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="742d6-130">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="742d6-130">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="742d6-131">Квалификаторы: [**маппингстрингс**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32Registry \| System \\ \\ CurrentControlSet \\ \\ Control \\ \\ граупордерлист")</span><span class="sxs-lookup"><span data-stu-id="742d6-131">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32Registry\|System\\\\CurrentControlSet\\\\Control\\\\GroupOrderList")</span></span>
</dt> </dl>

<span data-ttu-id="742d6-132">Указывает, может ли эта группа порядка загрузки включать драйверы вместе с системными службами.</span><span class="sxs-lookup"><span data-stu-id="742d6-132">Indicates whether this load order group can include drivers along with system services.</span></span>

</dd> <dt>

<span data-ttu-id="742d6-133">**граупордер**</span><span class="sxs-lookup"><span data-stu-id="742d6-133">**GroupOrder**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="742d6-134">Тип данных: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="742d6-134">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="742d6-135">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="742d6-135">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="742d6-136">Квалификаторы: [**маппингстрингс**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32Registry \| System \\ \\ CurrentControlSet \\ \\ Control \\ \\ граупордерлист")</span><span class="sxs-lookup"><span data-stu-id="742d6-136">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32Registry\|System\\\\CurrentControlSet\\\\Control\\\\GroupOrderList")</span></span>
</dt> </dl>

<span data-ttu-id="742d6-137">Последовательность, в которой эта группа служб загружается в операционную систему.</span><span class="sxs-lookup"><span data-stu-id="742d6-137">Sequence in which this group of services is loaded onto the operating system.</span></span>

<span data-ttu-id="742d6-138">Пример: 2</span><span class="sxs-lookup"><span data-stu-id="742d6-138">Example: 2</span></span>

</dd> <dt>

<span data-ttu-id="742d6-139">**InstallDate**</span><span class="sxs-lookup"><span data-stu-id="742d6-139">**InstallDate**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="742d6-140">Тип данных: **DateTime**</span><span class="sxs-lookup"><span data-stu-id="742d6-140">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="742d6-141">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="742d6-141">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="742d6-142">Квалификаторы: [**маппингстрингс**](/windows/desktop/WmiSdk/standard-qualifiers) (MIF. DMTF \| ComponentID \| 001,5 "), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) (" Дата установки ")</span><span class="sxs-lookup"><span data-stu-id="742d6-142">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|ComponentID\|001.5"), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Install Date")</span></span>
</dt> </dl>

<span data-ttu-id="742d6-143">Указывает, когда был установлен объект.</span><span class="sxs-lookup"><span data-stu-id="742d6-143">Indicates when the object was installed.</span></span> <span data-ttu-id="742d6-144">Отсутствие значения не означает, что объект не установлен.</span><span class="sxs-lookup"><span data-stu-id="742d6-144">Lack of a value does not indicate that the object is not installed.</span></span>

<span data-ttu-id="742d6-145">Это свойство наследуется от [**CIM \_ манажедсистемелемент**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="742d6-145">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="742d6-146">**Name**</span><span class="sxs-lookup"><span data-stu-id="742d6-146">**Name**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="742d6-147">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="742d6-147">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="742d6-148">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="742d6-148">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="742d6-149">Квалификаторы: [**ключ**](/windows/desktop/WmiSdk/key-qualifier), [**Переопределение**](/windows/desktop/WmiSdk/standard-qualifiers) ("имя"), [**маппингстрингс**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32Registry \| System \\ \\ CurrentControlSet \\ \\ Control \\ \\ граупордерлист")</span><span class="sxs-lookup"><span data-stu-id="742d6-149">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier), [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Name"), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32Registry\|System\\\\CurrentControlSet\\\\Control\\\\GroupOrderList")</span></span>
</dt> </dl>

<span data-ttu-id="742d6-150">Имя группы порядка загрузки.</span><span class="sxs-lookup"><span data-stu-id="742d6-150">Name of the load order group.</span></span>

<span data-ttu-id="742d6-151">Пример: "основной диск"</span><span class="sxs-lookup"><span data-stu-id="742d6-151">Example: "Primary disk"</span></span>

</dd> <dt>

<span data-ttu-id="742d6-152">**Состояние**</span><span class="sxs-lookup"><span data-stu-id="742d6-152">**Status**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="742d6-153">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="742d6-153">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="742d6-154">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="742d6-154">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="742d6-155">Квалификаторы: [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (10), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("состояние")</span><span class="sxs-lookup"><span data-stu-id="742d6-155">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (10), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Status")</span></span>
</dt> </dl>

<span data-ttu-id="742d6-156">Строка, указывающая текущее состояние объекта.</span><span class="sxs-lookup"><span data-stu-id="742d6-156">String that indicates the current status of the object.</span></span> <span data-ttu-id="742d6-157">Можно определить операционное и нерабочее состояние.</span><span class="sxs-lookup"><span data-stu-id="742d6-157">Operational and non-operational status can be defined.</span></span> <span data-ttu-id="742d6-158">Оперативное состояние может включать "ОК", "деградация" и "пред Fail".</span><span class="sxs-lookup"><span data-stu-id="742d6-158">Operational status can include "OK", "Degraded", and "Pred Fail".</span></span> <span data-ttu-id="742d6-159">"Пред-Fail" указывает, что элемент работает правильно, но прогнозирует сбой (например, жесткий диск с поддержкой SMART).</span><span class="sxs-lookup"><span data-stu-id="742d6-159">"Pred Fail" indicates that an element is functioning properly, but is predicting a failure (for example, a SMART-enabled hard disk drive).</span></span>

<span data-ttu-id="742d6-160">Нерабочее состояние может включать "Error", "starting", "остановка" и "обслуживание".</span><span class="sxs-lookup"><span data-stu-id="742d6-160">Non-operational status can include "Error", "Starting", "Stopping", and "Service".</span></span> <span data-ttu-id="742d6-161">"Служба" может применяться при зеркальном отображении дисков, перезагрузке списка разрешений пользователя или выполнении других административных задач.</span><span class="sxs-lookup"><span data-stu-id="742d6-161">"Service" can apply during disk mirror-resilvering, reloading a user permissions list, or other administrative work.</span></span> <span data-ttu-id="742d6-162">Не вся такая работа находится в оперативном режиме, но управляемый элемент не является ни "ОК", ни в одном из других состояний.</span><span class="sxs-lookup"><span data-stu-id="742d6-162">Not all such work is online, but the managed element is neither "OK" nor in one of the other states.</span></span>

<span data-ttu-id="742d6-163">Это свойство наследуется от [**CIM \_ манажедсистемелемент**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="742d6-163">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

<span data-ttu-id="742d6-164">В эти значения входят:</span><span class="sxs-lookup"><span data-stu-id="742d6-164">Values include the following:</span></span>

<dt>

<span id="OK"></span><span id="ok"></span>

<span data-ttu-id="742d6-165">**ОК** ("ОК")</span><span class="sxs-lookup"><span data-stu-id="742d6-165">**OK** ("OK")</span></span>


</dt> <dd></dd> <dt>

<span id="Error"></span><span id="error"></span><span id="ERROR"></span>

<span data-ttu-id="742d6-166">**Ошибка** ("ошибка")</span><span class="sxs-lookup"><span data-stu-id="742d6-166">**Error** ("Error")</span></span>


</dt> <dd></dd> <dt>

<span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>

<span data-ttu-id="742d6-167">**Пониженная работоспособность** (пониженная работоспособность)</span><span class="sxs-lookup"><span data-stu-id="742d6-167">**Degraded** ("Degraded")</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="742d6-168">**Неизвестно** ("неизвестно")</span><span class="sxs-lookup"><span data-stu-id="742d6-168">**Unknown** ("Unknown")</span></span>


</dt> <dd></dd> <dt>

<span id="Pred_Fail"></span><span id="pred_fail"></span><span id="PRED_FAIL"></span>

<span data-ttu-id="742d6-169">**Пред-ошибка** ("пред Fail")</span><span class="sxs-lookup"><span data-stu-id="742d6-169">**Pred Fail** ("Pred Fail")</span></span>


</dt> <dd></dd> <dt>

<span id="Starting"></span><span id="starting"></span><span id="STARTING"></span>

<span data-ttu-id="742d6-170">**Запуск** ("Запуск")</span><span class="sxs-lookup"><span data-stu-id="742d6-170">**Starting** ("Starting")</span></span>


</dt> <dd></dd> <dt>

<span id="Stopping"></span><span id="stopping"></span><span id="STOPPING"></span>

<span data-ttu-id="742d6-171">**Остановка** ("остановка")</span><span class="sxs-lookup"><span data-stu-id="742d6-171">**Stopping** ("Stopping")</span></span>


</dt> <dd></dd> <dt>

<span id="Service"></span><span id="service"></span><span id="SERVICE"></span>

<span data-ttu-id="742d6-172">**Служба** ("служба")</span><span class="sxs-lookup"><span data-stu-id="742d6-172">**Service** ("Service")</span></span>


</dt> <dd></dd> <dt>

<span id="Stressed"></span><span id="stressed"></span><span id="STRESSED"></span>

<span data-ttu-id="742d6-173">**Пренапряжению** ("напряжению")</span><span class="sxs-lookup"><span data-stu-id="742d6-173">**Stressed** ("Stressed")</span></span>


</dt> <dd></dd> <dt>

<span id="NonRecover"></span><span id="nonrecover"></span><span id="NONRECOVER"></span>

<span data-ttu-id="742d6-174">**Невосстановление** ("невосстановление")</span><span class="sxs-lookup"><span data-stu-id="742d6-174">**NonRecover** ("NonRecover")</span></span>


</dt> <dd></dd> <dt>

<span id="No_Contact"></span><span id="no_contact"></span><span id="NO_CONTACT"></span>

<span data-ttu-id="742d6-175">**Нет контакта** ("нет контакта")</span><span class="sxs-lookup"><span data-stu-id="742d6-175">**No Contact** ("No Contact")</span></span>


</dt> <dd></dd> <dt>

<span id="Lost_Comm"></span><span id="lost_comm"></span><span id="LOST_COMM"></span>

<span data-ttu-id="742d6-176">**Потеря** связи ("потеря связи")</span><span class="sxs-lookup"><span data-stu-id="742d6-176">**Lost Comm** ("Lost Comm")</span></span>


<span data-ttu-id="742d6-177"></dt> <dd></dd> </dl>

</dd> </dl></span><span class="sxs-lookup"><span data-stu-id="742d6-177"></dt> <dd></dd> </dl>

</dd> </dl></span></span>

## <a name="remarks"></a><span data-ttu-id="742d6-178">Комментарии</span><span class="sxs-lookup"><span data-stu-id="742d6-178">Remarks</span></span>

<span data-ttu-id="742d6-179">Класс **Win32 \_ лоадордерграуп** является производным от [**CIM \_ логикалелемент**](cim-logicalelement.md).</span><span class="sxs-lookup"><span data-stu-id="742d6-179">The **Win32\_LoadOrderGroup** class is derived from [**CIM\_LogicalElement**](cim-logicalelement.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="742d6-180">Требования</span><span class="sxs-lookup"><span data-stu-id="742d6-180">Requirements</span></span>



| <span data-ttu-id="742d6-181">Требование</span><span class="sxs-lookup"><span data-stu-id="742d6-181">Requirement</span></span> | <span data-ttu-id="742d6-182">Значение</span><span class="sxs-lookup"><span data-stu-id="742d6-182">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="742d6-183">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="742d6-183">Minimum supported client</span></span><br/> | <span data-ttu-id="742d6-184">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="742d6-184">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="742d6-185">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="742d6-185">Minimum supported server</span></span><br/> | <span data-ttu-id="742d6-186">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="742d6-186">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="742d6-187">Пространство имен</span><span class="sxs-lookup"><span data-stu-id="742d6-187">Namespace</span></span><br/>                | <span data-ttu-id="742d6-188">Корневой \\ CIMV2</span><span class="sxs-lookup"><span data-stu-id="742d6-188">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="742d6-189">MOF</span><span class="sxs-lookup"><span data-stu-id="742d6-189">MOF</span></span><br/>                      | <dl> <span data-ttu-id="742d6-190"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="742d6-190"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="742d6-191">DLL</span><span class="sxs-lookup"><span data-stu-id="742d6-191">DLL</span></span><br/>                      | <dl> <span data-ttu-id="742d6-192"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="742d6-192"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="742d6-193">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="742d6-193">See also</span></span>

<dl> <dt>

[<span data-ttu-id="742d6-194">**\_ЛОГИКАЛЕЛЕМЕНТ CIM**</span><span class="sxs-lookup"><span data-stu-id="742d6-194">**CIM\_LogicalElement**</span></span>](cim-logicalelement.md)
</dt> <dt>

<span data-ttu-id="742d6-195">[Классы операционной системы](/previous-versions//aa392727(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="742d6-195">[Operating System Classes](/previous-versions//aa392727(v=vs.85))</span></span>
</dt> </dl>

 

