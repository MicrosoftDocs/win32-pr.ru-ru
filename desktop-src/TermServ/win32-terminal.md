---
title: Класс Win32_Terminal
description: Представляет терминал.
ms.assetid: d56cc605-6c5a-46ae-96fd-d0a4f5b6074a
ms.tgt_platform: multiple
keywords:
- Класс Win32_Terminal службы удаленных рабочих столов
- Службы удаленных рабочих столов класса Win32_Terminal, описание
topic_type:
- apiref
api_name:
- Win32_Terminal
- Win32_Terminal.Caption
- Win32_Terminal.Description
- Win32_Terminal.InstallDate
- Win32_Terminal.Name
- Win32_Terminal.Status
- Win32_Terminal.fEnableTerminal
- Win32_Terminal.LoggedOnUsers
- Win32_Terminal.TerminalName
api_location:
- TSCfgWmi.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f7ae74003f798049fbdb34c955db3f64112bfcd2
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104135382"
---
# <a name="win32_terminal-class"></a><span data-ttu-id="f864d-105">\_Класс терминала Win32</span><span class="sxs-lookup"><span data-stu-id="f864d-105">Win32\_Terminal class</span></span>

<span data-ttu-id="f864d-106">Класс **WMI \_ терминала Win32** представляет терминал.</span><span class="sxs-lookup"><span data-stu-id="f864d-106">The **Win32\_Terminal** WMI class represents a terminal.</span></span>

<span data-ttu-id="f864d-107">Следующий синтаксис упрощен из MOF-кода и включает все определенные и унаследованные свойства в алфавитном порядке.</span><span class="sxs-lookup"><span data-stu-id="f864d-107">The following syntax is simplified from MOF code and includes all defined and inherited properties, in alphabetical order.</span></span> <span data-ttu-id="f864d-108">Справочные сведения о методах см. в таблице методов далее в этом разделе.</span><span class="sxs-lookup"><span data-stu-id="f864d-108">For reference information on methods, see the table of methods later in this topic.</span></span>

## <a name="syntax"></a><span data-ttu-id="f864d-109">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="f864d-109">Syntax</span></span>

``` syntax
[dynamic, overwrite, provider("Win32_WIN32_TERMINAL_Prov"), ClassContext("local|hkey_local_machine\\SYSTEM\\CurrentControlSet\\Control\\TerminalServer\\WinStations"), AMENDMENT]
class Win32_Terminal : CIM_LogicalElement
{
  string   Caption;
  string   Description;
  datetime InstallDate;
  string   Name;
  string   Status;
  uint32   fEnableTerminal;
  uint32   LoggedOnUsers;
  string   TerminalName;
};
```

## <a name="members"></a><span data-ttu-id="f864d-110">Члены</span><span class="sxs-lookup"><span data-stu-id="f864d-110">Members</span></span>

<span data-ttu-id="f864d-111">Класс **\_ терминала Win32** имеет следующие типы членов:</span><span class="sxs-lookup"><span data-stu-id="f864d-111">The **Win32\_Terminal** class has these types of members:</span></span>

-   [<span data-ttu-id="f864d-112">Методы</span><span class="sxs-lookup"><span data-stu-id="f864d-112">Methods</span></span>](#methods)
-   [<span data-ttu-id="f864d-113">Свойства</span><span class="sxs-lookup"><span data-stu-id="f864d-113">Properties</span></span>](#properties)

### <a name="methods"></a><span data-ttu-id="f864d-114">Методы</span><span class="sxs-lookup"><span data-stu-id="f864d-114">Methods</span></span>

<span data-ttu-id="f864d-115">Класс **\_ терминала Win32** содержит следующие методы.</span><span class="sxs-lookup"><span data-stu-id="f864d-115">The **Win32\_Terminal** class has these methods.</span></span>



| <span data-ttu-id="f864d-116">Метод</span><span class="sxs-lookup"><span data-stu-id="f864d-116">Method</span></span>                                  | <span data-ttu-id="f864d-117">Описание</span><span class="sxs-lookup"><span data-stu-id="f864d-117">Description</span></span>                                                                                                                                                                             |
|:----------------------------------------|:----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="f864d-118">**Создания**</span><span class="sxs-lookup"><span data-stu-id="f864d-118">**Create**</span></span>](create-win32-terminal.md) | <span data-ttu-id="f864d-119">Создает терминал с параметрами по умолчанию, которые можно настроить с помощью свойств и методов классов [**Win32 \_ терминалсеттинг**](win32-terminalsetting.md) .</span><span class="sxs-lookup"><span data-stu-id="f864d-119">Creates a terminal with default settings which can be customized by using the properties and methods of the [**Win32\_TerminalSetting**](win32-terminalsetting.md) classes.</span></span><br/> |
| [<span data-ttu-id="f864d-120">**Удалить**</span><span class="sxs-lookup"><span data-stu-id="f864d-120">**Delete**</span></span>](delete-win32-terminal.md) | <span data-ttu-id="f864d-121">Удаляет указанный терминал.</span><span class="sxs-lookup"><span data-stu-id="f864d-121">Deletes the specified terminal.</span></span><br/>                                                                                                                                              |
| [<span data-ttu-id="f864d-122">**Включить**</span><span class="sxs-lookup"><span data-stu-id="f864d-122">**Enable**</span></span>](win32-terminal-enable.md) | <span data-ttu-id="f864d-123">Отключает или включает терминал.</span><span class="sxs-lookup"><span data-stu-id="f864d-123">Disables or enables the terminal.</span></span><br/>                                                                                                                                            |
| [<span data-ttu-id="f864d-124">**Имени**</span><span class="sxs-lookup"><span data-stu-id="f864d-124">**Rename**</span></span>](win32-terminal-rename.md) | <span data-ttu-id="f864d-125">Переименовывает терминал.</span><span class="sxs-lookup"><span data-stu-id="f864d-125">Renames the terminal.</span></span><br/>                                                                                                                                                        |



 

### <a name="properties"></a><span data-ttu-id="f864d-126">Свойства</span><span class="sxs-lookup"><span data-stu-id="f864d-126">Properties</span></span>

<span data-ttu-id="f864d-127">Класс **\_ терминала Win32** имеет следующие свойства.</span><span class="sxs-lookup"><span data-stu-id="f864d-127">The **Win32\_Terminal** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="f864d-128">**Заголовок**</span><span class="sxs-lookup"><span data-stu-id="f864d-128">**Caption**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f864d-129">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="f864d-129">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="f864d-130">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="f864d-130">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="f864d-131">Квалификаторы: [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (64)</span><span class="sxs-lookup"><span data-stu-id="f864d-131">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64)</span></span>
</dt> </dl>

<span data-ttu-id="f864d-132">Краткое описание (однострочная строка) объекта.</span><span class="sxs-lookup"><span data-stu-id="f864d-132">Short description (one-line string) of the object.</span></span>

<span data-ttu-id="f864d-133">Это свойство наследуется от [**CIM \_ манажедсистемелемент**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="f864d-133">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="f864d-134">**Описание**</span><span class="sxs-lookup"><span data-stu-id="f864d-134">**Description**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f864d-135">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="f864d-135">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="f864d-136">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="f864d-136">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="f864d-137">Описание объекта.</span><span class="sxs-lookup"><span data-stu-id="f864d-137">Description of the object.</span></span>

<span data-ttu-id="f864d-138">Это свойство наследуется от [**CIM \_ манажедсистемелемент**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="f864d-138">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="f864d-139">**фенаблетерминал**</span><span class="sxs-lookup"><span data-stu-id="f864d-139">**fEnableTerminal**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f864d-140">Тип данных: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="f864d-140">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="f864d-141">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="f864d-141">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="f864d-142">Указывает, отключен ли или включен указанный терминал.</span><span class="sxs-lookup"><span data-stu-id="f864d-142">Specifies whether the specified terminal is disabled or enabled.</span></span>

<dt>

<span id="FALSE"></span><span id="false"></span>

<span data-ttu-id="f864d-143"><span id="FALSE"></span><span id="false"></span>**False** (0)</span><span class="sxs-lookup"><span data-stu-id="f864d-143"><span id="FALSE"></span><span id="false"></span>**FALSE** (0)</span></span>


</dt> <dd>

<span data-ttu-id="f864d-144">Терминал отключен.</span><span class="sxs-lookup"><span data-stu-id="f864d-144">The terminal is disabled.</span></span>

</dd> <dt>

<span id="TRUE"></span><span id="true"></span>

<span data-ttu-id="f864d-145"><span id="TRUE"></span><span id="true"></span>**True** (1)</span><span class="sxs-lookup"><span data-stu-id="f864d-145"><span id="TRUE"></span><span id="true"></span>**TRUE** (1)</span></span>


</dt> <dd>

<span data-ttu-id="f864d-146">Терминал включен.</span><span class="sxs-lookup"><span data-stu-id="f864d-146">The terminal is enabled.</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="f864d-147">**InstallDate**</span><span class="sxs-lookup"><span data-stu-id="f864d-147">**InstallDate**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f864d-148">Тип данных: **DateTime**</span><span class="sxs-lookup"><span data-stu-id="f864d-148">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="f864d-149">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="f864d-149">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="f864d-150">Квалификаторы: [**маппингстрингс**](/windows/desktop/WmiSdk/standard-qualifiers) (MIF. \|Значение ComponentID \| 001,5 в DMTF</span><span class="sxs-lookup"><span data-stu-id="f864d-150">Qualifiers: [**Mappingstrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|ComponentID\|001.5")</span></span>
</dt> </dl>

<span data-ttu-id="f864d-151">Дата установки объекта.</span><span class="sxs-lookup"><span data-stu-id="f864d-151">The date the object was installed.</span></span> <span data-ttu-id="f864d-152">Отсутствие значения не означает, что объект не установлен.</span><span class="sxs-lookup"><span data-stu-id="f864d-152">A lack of a value does not indicate that the object is not installed.</span></span>

<span data-ttu-id="f864d-153">Это свойство наследуется от [**CIM \_ манажедсистемелемент**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="f864d-153">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="f864d-154">**логжедонусерс**</span><span class="sxs-lookup"><span data-stu-id="f864d-154">**LoggedOnUsers**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f864d-155">Тип данных: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="f864d-155">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="f864d-156">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="f864d-156">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="f864d-157">Число сеансов, вошедших в систему терминала.</span><span class="sxs-lookup"><span data-stu-id="f864d-157">Number of logged-on sessions for the terminal.</span></span>

</dd> <dt>

<span data-ttu-id="f864d-158">**Name**</span><span class="sxs-lookup"><span data-stu-id="f864d-158">**Name**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f864d-159">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="f864d-159">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="f864d-160">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="f864d-160">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="f864d-161">Имя объекта.</span><span class="sxs-lookup"><span data-stu-id="f864d-161">The name of the object.</span></span>

<span data-ttu-id="f864d-162">Это свойство наследуется от [**CIM \_ манажедсистемелемент**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="f864d-162">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="f864d-163">**Состояние**</span><span class="sxs-lookup"><span data-stu-id="f864d-163">**Status**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f864d-164">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="f864d-164">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="f864d-165">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="f864d-165">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="f864d-166">Квалификаторы: [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (10)</span><span class="sxs-lookup"><span data-stu-id="f864d-166">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (10)</span></span>
</dt> </dl>

<span data-ttu-id="f864d-167">Текущее состояние объекта.</span><span class="sxs-lookup"><span data-stu-id="f864d-167">Current status of the object.</span></span> <span data-ttu-id="f864d-168">Можно определить различные операционные и неоперационные состояния.</span><span class="sxs-lookup"><span data-stu-id="f864d-168">Various operational and nonoperational statuses can be defined.</span></span> <span data-ttu-id="f864d-169">Рабочие состояния включают: "ОК", "деградация" и "пред-ошибка" (элемент, например жесткий диск с поддержкой SMART, может работать правильно, но прогнозировать сбой в ближайшем будущем).</span><span class="sxs-lookup"><span data-stu-id="f864d-169">Operational statuses include: "OK", "Degraded", and "Pred Fail" (an element, such as a SMART-enabled hard disk drive, may be functioning properly but predicting a failure in the near future).</span></span> <span data-ttu-id="f864d-170">Неработающие состояния включают: "ошибка", "Запуск", "остановка" и "служба".</span><span class="sxs-lookup"><span data-stu-id="f864d-170">Nonoperational statuses include: "Error", "Starting", "Stopping", and "Service".</span></span> <span data-ttu-id="f864d-171">Последняя, «служба», может применяться во время зеркального копирования диска, перезагрузки списка разрешений пользователя или другой административной работы.</span><span class="sxs-lookup"><span data-stu-id="f864d-171">The latter, "Service", could apply during mirror-resilvering of a disk, reload of a user permissions list, or other administrative work.</span></span> <span data-ttu-id="f864d-172">Не вся такая работа выполняется в интерактивном состоянии, но управляемый элемент не является ни "ОК", ни одним из других состояний.</span><span class="sxs-lookup"><span data-stu-id="f864d-172">Not all such work is on-line, yet the managed element is neither "OK" nor in one of the other states.</span></span>

<span data-ttu-id="f864d-173">Это свойство наследуется от [**CIM \_ манажедсистемелемент**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="f864d-173">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

<dt>



 <span data-ttu-id="f864d-174">("ОК")</span><span class="sxs-lookup"><span data-stu-id="f864d-174">("OK")</span></span>


</dt> <dd></dd> <dt>



 <span data-ttu-id="f864d-175">("Ошибка")</span><span class="sxs-lookup"><span data-stu-id="f864d-175">("Error")</span></span>


</dt> <dd></dd> <dt>



 <span data-ttu-id="f864d-176">("Пониженное состояние")</span><span class="sxs-lookup"><span data-stu-id="f864d-176">("Degraded")</span></span>


</dt> <dd></dd> <dt>



 <span data-ttu-id="f864d-177">("Неизвестно")</span><span class="sxs-lookup"><span data-stu-id="f864d-177">("Unknown")</span></span>


</dt> <dd></dd> <dt>



 <span data-ttu-id="f864d-178">("Пред Fail")</span><span class="sxs-lookup"><span data-stu-id="f864d-178">("Pred Fail")</span></span>


</dt> <dd></dd> <dt>



 <span data-ttu-id="f864d-179">("Запуск")</span><span class="sxs-lookup"><span data-stu-id="f864d-179">("Starting")</span></span>


</dt> <dd></dd> <dt>



 <span data-ttu-id="f864d-180">("Остановка")</span><span class="sxs-lookup"><span data-stu-id="f864d-180">("Stopping")</span></span>


</dt> <dd></dd> <dt>



 <span data-ttu-id="f864d-181">("Служба")</span><span class="sxs-lookup"><span data-stu-id="f864d-181">("Service")</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="f864d-182">**терминалнаме**</span><span class="sxs-lookup"><span data-stu-id="f864d-182">**TerminalName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f864d-183">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="f864d-183">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="f864d-184">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="f864d-184">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="f864d-185">Квалификаторы: [ **ключ**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="f864d-185">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

<span data-ttu-id="f864d-186">Уникальное имя, идентифицирующее экземпляр терминала.</span><span class="sxs-lookup"><span data-stu-id="f864d-186">The unique name that identifies the instance of the terminal.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="f864d-187">Комментарии</span><span class="sxs-lookup"><span data-stu-id="f864d-187">Remarks</span></span>

<span data-ttu-id="f864d-188">**Win32 \_ Терминал** связан с [**Win32 \_ терминалсеттинг**](win32-terminalsetting.md) в качестве свойства **element** ассоциации [**Win32 \_ терминалтерминалсеттинг**](win32-terminalterminalsetting.md) .</span><span class="sxs-lookup"><span data-stu-id="f864d-188">**Win32\_Terminal** is associated with [**Win32\_TerminalSetting**](win32-terminalsetting.md) as the **Element** property of the [**Win32\_TerminalTerminalSetting**](win32-terminalterminalsetting.md) association.</span></span>

<span data-ttu-id="f864d-189">Следующие классы являются подклассами класса **\_ терминала Win32** : [**Win32 \_ тсженералсеттинг**](win32-tsgeneralsetting.md), [**Win32 \_ тслогонсеттинг**](win32-tslogonsetting.md), [**Win32 \_ тссессионсеттинг**](win32-tssessionsetting.md), [**Win32 \_ тсенвиронментсеттинг**](win32-tsenvironmentsetting.md), [**Win32 \_ тсремотеконтролсеттинг**](win32-tsremotecontrolsetting.md), [**Win32 \_ TSClientSetting**](win32-tsclientsetting.md), [**Win32 \_ TSNetworkAdapterSetting**](win32-tsnetworkadaptersetting.md), [**Win32 \_ TSNetworkAdapterListSetting**](win32-tsnetworkadapterlistsetting.md), [**Win32 \_ TSPermissionsSetting**](win32-tspermissionssetting.md)и [**Win32 \_ TSAccount**](win32-tsaccount.md).</span><span class="sxs-lookup"><span data-stu-id="f864d-189">The following classes are subclasses of the **Win32\_Terminal** class: [**Win32\_TSGeneralSetting**](win32-tsgeneralsetting.md), [**Win32\_TSLogonSetting**](win32-tslogonsetting.md), [**Win32\_TSSessionSetting**](win32-tssessionsetting.md), [**Win32\_TSEnvironmentSetting**](win32-tsenvironmentsetting.md), [**Win32\_TSRemoteControlSetting**](win32-tsremotecontrolsetting.md), [**Win32\_TSClientSetting**](win32-tsclientsetting.md), [**Win32\_TSNetworkAdapterSetting**](win32-tsnetworkadaptersetting.md), [**Win32\_TSNetworkAdapterListSetting**](win32-tsnetworkadapterlistsetting.md), [**Win32\_TSPermissionsSetting**](win32-tspermissionssetting.md), and [**Win32\_TSAccount**](win32-tsaccount.md).</span></span>

<span data-ttu-id="f864d-190">Обратите внимание, что Винстатионс, связанный с сеансом консоли, не может получить доступ к методам и свойствам этого класса.</span><span class="sxs-lookup"><span data-stu-id="f864d-190">Note that Winstations associated with the console session cannot access the methods and properties of this class.</span></span> <span data-ttu-id="f864d-191">Если предпринимается попытка сделать это, указав "Console" в качестве значения свойства **терминалнаме** , методы этого объекта возвращают **WBEM \_ E \_ не \_ поддерживаются**.</span><span class="sxs-lookup"><span data-stu-id="f864d-191">If an attempt is made to do so by specifying "Console" as the value of the **TerminalName** property, methods of this object return **WBEM\_E\_NOT\_SUPPORTED**.</span></span> <span data-ttu-id="f864d-192">Этот код ошибки также возвращается, если станция окна пытается вызвать методы этого объекта для добавления или изменения свойств безопасности учетных записей LocalSystem, LocalService или NetworkService.</span><span class="sxs-lookup"><span data-stu-id="f864d-192">This error code is also returned if a window station attempts to call methods of this object to add or modify the security properties of the LocalSystem, LocalService, or NetworkService accounts.</span></span>

<span data-ttu-id="f864d-193">Чтобы подключиться к \\ корневому \\ \\ пространству имен CIMV2 терминалсервицес, уровень проверки подлинности должен включать в себя конфиденциальность пакетов.</span><span class="sxs-lookup"><span data-stu-id="f864d-193">To connect to the \\root\\CIMV2\\TerminalServices namespace, the authentication level must include packet privacy.</span></span> <span data-ttu-id="f864d-194">Для вызовов C/C++ это уровень проверки подлинности **AUTHN на \_ \_ \_ уровне \_ \_ безопасности RPC C уровня "PKT**".</span><span class="sxs-lookup"><span data-stu-id="f864d-194">For C/C++ calls, this is an authentication level of **RPC\_C\_AUTHN\_LEVEL\_PKT\_PRIVACY**.</span></span> <span data-ttu-id="f864d-195">Для Visual Basic и написания сценариев это уровень проверки подлинности **вбемаусентикатионлевелпктприваци** или "пктприваци" со значением 6.</span><span class="sxs-lookup"><span data-stu-id="f864d-195">For Visual Basic and scripting calls, this is an authentication level of **WbemAuthenticationLevelPktPrivacy** or "pktPrivacy", with a value of 6.</span></span> <span data-ttu-id="f864d-196">В следующем примере Visual Basic Scripting Edition (VBScript) показано, как подключиться к удаленному компьютеру с использованием конфиденциальности пакетов.</span><span class="sxs-lookup"><span data-stu-id="f864d-196">The following Visual Basic Scripting Edition (VBScript) example shows how to connect to a remote computer with packet privacy.</span></span>


```VB
strComputer = "RemoteServer1" 
Set objServices = GetObject( _
    "winmgmts:{authenticationLevel=pktPrivacy}!Root/CIMv2/TerminalServices")
```



<span data-ttu-id="f864d-197">Файлы MOF-файл (MOF) содержат определения для классов инструментарий управления Windows (WMI) (WMI).</span><span class="sxs-lookup"><span data-stu-id="f864d-197">Managed Object Format (MOF) files contain the definitions for Windows Management Instrumentation (WMI) classes.</span></span> <span data-ttu-id="f864d-198">MOF-файлы не устанавливаются в составе пакета средств разработки программного обеспечения Microsoft Windows (SDK).</span><span class="sxs-lookup"><span data-stu-id="f864d-198">MOF files are not installed as part of the Microsoft Windows Software Development Kit (SDK).</span></span> <span data-ttu-id="f864d-199">Они устанавливаются на сервере при добавлении связанной роли с помощью диспетчер сервера.</span><span class="sxs-lookup"><span data-stu-id="f864d-199">They are installed on the server when you add the associated role by using the Server Manager.</span></span> <span data-ttu-id="f864d-200">Дополнительные сведения о файлах MOF см. в разделе [MOF-файл (MOF)](/windows/desktop/WmiSdk/managed-object-format--mof-).</span><span class="sxs-lookup"><span data-stu-id="f864d-200">For more information about MOF files, see [Managed Object Format (MOF)](/windows/desktop/WmiSdk/managed-object-format--mof-).</span></span>

## <a name="requirements"></a><span data-ttu-id="f864d-201">Требования</span><span class="sxs-lookup"><span data-stu-id="f864d-201">Requirements</span></span>



| <span data-ttu-id="f864d-202">Требование</span><span class="sxs-lookup"><span data-stu-id="f864d-202">Requirement</span></span> | <span data-ttu-id="f864d-203">Значение</span><span class="sxs-lookup"><span data-stu-id="f864d-203">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="f864d-204">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="f864d-204">Minimum supported client</span></span><br/> | <span data-ttu-id="f864d-205">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="f864d-205">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="f864d-206">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="f864d-206">Minimum supported server</span></span><br/> | <span data-ttu-id="f864d-207">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="f864d-207">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="f864d-208">Пространство имен</span><span class="sxs-lookup"><span data-stu-id="f864d-208">Namespace</span></span><br/>                | <span data-ttu-id="f864d-209">Корневой \\ CIMv2 \\ терминалсервицес</span><span class="sxs-lookup"><span data-stu-id="f864d-209">Root\\CIMv2\\TerminalServices</span></span><br/>                                                |
| <span data-ttu-id="f864d-210">MOF</span><span class="sxs-lookup"><span data-stu-id="f864d-210">MOF</span></span><br/>                      | <dl> <span data-ttu-id="f864d-211"><dt>Тскфгвми. mof</dt></span><span class="sxs-lookup"><span data-stu-id="f864d-211"><dt>TSCfgWmi.mof</dt></span></span> </dl> |
| <span data-ttu-id="f864d-212">DLL</span><span class="sxs-lookup"><span data-stu-id="f864d-212">DLL</span></span><br/>                      | <dl> <span data-ttu-id="f864d-213"><dt>TSCfgWmi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="f864d-213"><dt>TSCfgWmi.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="f864d-214">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="f864d-214">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f864d-215">**\_ЛОГИКАЛЕЛЕМЕНТ CIM**</span><span class="sxs-lookup"><span data-stu-id="f864d-215">**CIM\_LogicalElement**</span></span>](cim-logicalelement.md)
</dt> <dt>

[<span data-ttu-id="f864d-216">**\_Терминалсервицесеттинг Win32**</span><span class="sxs-lookup"><span data-stu-id="f864d-216">**Win32\_TerminalServiceSetting**</span></span>](win32-terminalservicesetting.md)
</dt> <dt>

[<span data-ttu-id="f864d-217">**\_Терминалтерминалсеттинг Win32**</span><span class="sxs-lookup"><span data-stu-id="f864d-217">**Win32\_TerminalTerminalSetting**</span></span>](win32-terminalterminalsetting.md)
</dt> </dl>

 

