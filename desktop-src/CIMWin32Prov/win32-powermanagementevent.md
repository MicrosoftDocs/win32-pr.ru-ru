---
description: '&Win32 \_ поверманажементевент \# 32; Класс WMI представляет события управления питанием, возникающие при изменении состояния электропитания.'
ms.assetid: b5781805-87c7-4eaf-afbb-a1770fcff41c
ms.tgt_platform: multiple
title: Класс Win32_PowerManagementEvent
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_PowerManagementEvent
- Win32_PowerManagementEvent.SECURITY_DESCRIPTOR
- Win32_PowerManagementEvent.TIME_CREATED
- Win32_PowerManagementEvent.EventType
- Win32_PowerManagementEvent.OEMEventCode
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: e0e7dfa68646dbefb6d6b70218fe99830b44a0c1
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104141546"
---
# <a name="win32_powermanagementevent-class"></a><span data-ttu-id="87ffc-103">\_Класс Win32 поверманажементевент</span><span class="sxs-lookup"><span data-stu-id="87ffc-103">Win32\_PowerManagementEvent class</span></span>

<span data-ttu-id="87ffc-104">Класс **WMI \_ поверманажементевент** [инструментария](../wmisdk/retrieving-a-class.md) Win32 представляет события управления питанием, полученные при изменении состояния электропитания.</span><span class="sxs-lookup"><span data-stu-id="87ffc-104">The **Win32\_PowerManagementEvent** [WMI class](../wmisdk/retrieving-a-class.md) represents power management events resulting from power state changes.</span></span> <span data-ttu-id="87ffc-105">Эти изменения состояния связаны с протоколами управления системой расширенного управления питанием (APM) или интерфейсом ACPI.</span><span class="sxs-lookup"><span data-stu-id="87ffc-105">These state changes are associated with either the Advanced Power Management (APM) or the Advanced Configuration and Power Interface (ACPI) system management protocols.</span></span>

<span data-ttu-id="87ffc-106">Следующий пример синтаксиса — упрощенный MOF-код, который включает все наследуемые свойства.</span><span class="sxs-lookup"><span data-stu-id="87ffc-106">The following syntax is simplified from Managed Object Format (MOF) code and includes all of the inherited properties.</span></span> <span data-ttu-id="87ffc-107">Свойства перечислены в алфавитном порядке, а не в MOF.</span><span class="sxs-lookup"><span data-stu-id="87ffc-107">Properties are listed in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="87ffc-108">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="87ffc-108">Syntax</span></span>

``` syntax
[UUID("{86460B6B-E709-11d2-B139-00105A1F77A1}"), AMENDMENT]
class Win32_PowerManagementEvent : __ExtrinsicEvent
{
  uint8  SECURITY_DESCRIPTOR[];
  uint64 TIME_CREATED;
  uint16 EventType;
  uint16 OEMEventCode;
};
```

## <a name="members"></a><span data-ttu-id="87ffc-109">Члены</span><span class="sxs-lookup"><span data-stu-id="87ffc-109">Members</span></span>

<span data-ttu-id="87ffc-110">Класс **Win32 \_ поверманажементевент** имеет следующие типы членов:</span><span class="sxs-lookup"><span data-stu-id="87ffc-110">The **Win32\_PowerManagementEvent** class has these types of members:</span></span>

-   [<span data-ttu-id="87ffc-111">Свойства</span><span class="sxs-lookup"><span data-stu-id="87ffc-111">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="87ffc-112">Свойства</span><span class="sxs-lookup"><span data-stu-id="87ffc-112">Properties</span></span>

<span data-ttu-id="87ffc-113">Класс **Win32 \_ поверманажементевент** имеет следующие свойства.</span><span class="sxs-lookup"><span data-stu-id="87ffc-113">The **Win32\_PowerManagementEvent** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="87ffc-114">**EventType**</span><span class="sxs-lookup"><span data-stu-id="87ffc-114">**EventType**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="87ffc-115">Тип данных: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="87ffc-115">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="87ffc-116">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="87ffc-116">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="87ffc-117">Квалификаторы: [**маппингстрингс**](../wmisdk/standard-qualifiers.md) (" \| события управления питанием Win32API")</span><span class="sxs-lookup"><span data-stu-id="87ffc-117">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32API\|Power Management Events")</span></span>
</dt> </dl>

<span data-ttu-id="87ffc-118">Тип изменения состояния энергопотребления системы.</span><span class="sxs-lookup"><span data-stu-id="87ffc-118">Type of change in the system power state.</span></span>

<dt>

<span id="Entering_Suspend"></span><span id="entering_suspend"></span><span id="ENTERING_SUSPEND"></span>

<span data-ttu-id="87ffc-119"><span id="Entering_Suspend"></span><span id="entering_suspend"></span><span id="ENTERING_SUSPEND"></span>**Вход в приостановку** (4)</span><span class="sxs-lookup"><span data-stu-id="87ffc-119"><span id="Entering_Suspend"></span><span id="entering_suspend"></span><span id="ENTERING_SUSPEND"></span>**Entering Suspend** (4)</span></span>


</dt> <dd>

<span data-ttu-id="87ffc-120">В приостановленном состоянии компьютер находится в выключенном состоянии; Однако это может быть "пробуждено" в ответ на различные события, включая ввод пользователя (например, перемещение мыши или нажатие клавиши на клавиатуре).</span><span class="sxs-lookup"><span data-stu-id="87ffc-120">While suspended, the computer appears to be off; however, it can be "awakened" in response to various events, including user input (such as moving the mouse or pressing a key on the keyboard).</span></span> <span data-ttu-id="87ffc-121">В то время как компьютер приостановлен, энергопотребление уменьшается до одного из нескольких уровней в зависимости от того, как будет использоваться система.</span><span class="sxs-lookup"><span data-stu-id="87ffc-121">While the computer is suspended, power consumption is reduced to one of several levels depending on how the system is to be used.</span></span> <span data-ttu-id="87ffc-122">Чем меньше уровень энергопотребления, тем больше времени требуется системе для возврата в рабочее состояние.</span><span class="sxs-lookup"><span data-stu-id="87ffc-122">The lower the level of power consumption, the more time it takes the system to return to the working state.</span></span> <span data-ttu-id="87ffc-123">Когда компьютер переходит в состояние приостановки, Рабочий стол блокируется и необходимо нажать клавиши CTRL + ALT + DELETE и указать допустимое имя пользователя и пароль для возобновления операций.</span><span class="sxs-lookup"><span data-stu-id="87ffc-123">When the computer enters the suspend state, the desktop is locked, and you must press CTRL+ALT+DELETE and provide a valid user name and password to resume operations</span></span>

</dd> <dt>

<span id="Resume_from_Suspend"></span><span id="resume_from_suspend"></span><span id="RESUME_FROM_SUSPEND"></span>

<span data-ttu-id="87ffc-124"><span id="Resume_from_Suspend"></span><span id="resume_from_suspend"></span><span id="RESUME_FROM_SUSPEND"></span>**Возобновление с приостановки** (7)</span><span class="sxs-lookup"><span data-stu-id="87ffc-124"><span id="Resume_from_Suspend"></span><span id="resume_from_suspend"></span><span id="RESUME_FROM_SUSPEND"></span>**Resume from Suspend** (7)</span></span>


</dt> <dd>

<span data-ttu-id="87ffc-125">Указывает, что было отправлено сообщение о выходе из спящего режима, что позволяет компьютеру вернуться к обычному энергопотреблению.</span><span class="sxs-lookup"><span data-stu-id="87ffc-125">Indicates that a Resume from Suspend message has been sent, enabling the computer to return to its regular power state.</span></span>

</dd> <dt>

<span id="Power_Status_Change"></span><span id="power_status_change"></span><span id="POWER_STATUS_CHANGE"></span>

<span data-ttu-id="87ffc-126"><span id="Power_Status_Change"></span><span id="power_status_change"></span><span id="POWER_STATUS_CHANGE"></span>**Изменение состояния питания** (10)</span><span class="sxs-lookup"><span data-stu-id="87ffc-126"><span id="Power_Status_Change"></span><span id="power_status_change"></span><span id="POWER_STATUS_CHANGE"></span>**Power Status Change** (10)</span></span>


</dt> <dd>

<span data-ttu-id="87ffc-127">Указывает изменение состояния питания компьютера, например переключение от батареи питания в AC или от AC к источнику бесперебойного питания.</span><span class="sxs-lookup"><span data-stu-id="87ffc-127">Indicates a change in the power status of the computer, such as a switch from battery power to AC, or from AC to an uninterruptible power supply.</span></span> <span data-ttu-id="87ffc-128">Это событие возникает также, если уровень заряда батареи становится ниже заданного пользователем порога или изменяется на заданную величину в процентах.</span><span class="sxs-lookup"><span data-stu-id="87ffc-128">The system also broadcasts this event when remaining battery power slips below the threshold specified by the user or if the battery power changes by a specified percentage.</span></span>

</dd> <dt>

<span id="OEM_Event"></span><span id="oem_event"></span><span id="OEM_EVENT"></span>

<span data-ttu-id="87ffc-129"><span id="OEM_Event"></span><span id="oem_event"></span><span id="OEM_EVENT"></span>**Событие OEM** (11)</span><span class="sxs-lookup"><span data-stu-id="87ffc-129"><span id="OEM_Event"></span><span id="oem_event"></span><span id="OEM_EVENT"></span>**OEM Event** (11)</span></span>


</dt> <dd>

<span data-ttu-id="87ffc-130">Указывает, что система управления расширенным управлением питанием (APM) отправила OEM-событие.</span><span class="sxs-lookup"><span data-stu-id="87ffc-130">Indicates that an Advanced Power Management (APM) BIOS has sent an OEM event.</span></span> <span data-ttu-id="87ffc-131">Значение события будет захвачено в свойстве **оемевенткоде** .</span><span class="sxs-lookup"><span data-stu-id="87ffc-131">The value of the event will be captured in the **OEMEventCode** property.</span></span> <span data-ttu-id="87ffc-132">Поскольку некоторые реализации APM BIOS не предоставляют уведомления о событии OEM, это событие может никогда не транслироваться на некоторые компьютеры.</span><span class="sxs-lookup"><span data-stu-id="87ffc-132">Because some APM BIOS implementations do not provide OEM event notifications, this event might never be broadcast on some computers.</span></span> <span data-ttu-id="87ffc-133">APM — это устаревшая схема управления питанием.</span><span class="sxs-lookup"><span data-stu-id="87ffc-133">APM is a legacy power management scheme.</span></span> <span data-ttu-id="87ffc-134">Несмотря на то что поддержка APM в основном была заменена ACPI (Расширенная конфигурация и интерфейс питания).</span><span class="sxs-lookup"><span data-stu-id="87ffc-134">Although still supported, APM has been largely superseded by ACPI (Advanced Configuration and Power Interface).</span></span>

</dd> <dt>

<span id="Resume_Automatic"></span><span id="resume_automatic"></span><span id="RESUME_AUTOMATIC"></span>

<span data-ttu-id="87ffc-135"><span id="Resume_Automatic"></span><span id="resume_automatic"></span><span id="RESUME_AUTOMATIC"></span>**Автоматическое возобновление** (18)</span><span class="sxs-lookup"><span data-stu-id="87ffc-135"><span id="Resume_Automatic"></span><span id="resume_automatic"></span><span id="RESUME_AUTOMATIC"></span>**Resume Automatic** (18)</span></span>


</dt> <dd>

<span data-ttu-id="87ffc-136">Указывает, что компьютер был пробужден в ответ на событие.</span><span class="sxs-lookup"><span data-stu-id="87ffc-136">Indicates that the computer has awakened in response to an event.</span></span> <span data-ttu-id="87ffc-137">Если система обнаруживает активность пользователей (например, щелчок мышью), сообщение Ресумесуспенд будет транслироваться, позволяя приложениям узнавать о том, что они могут возобновить интерактивное взаимодействие с пользователем.</span><span class="sxs-lookup"><span data-stu-id="87ffc-137">If the system detects user activity (such as a mouse click), the ResumeSuspend message will be broadcast, letting applications know that they can resume full interactivity with the user.</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="87ffc-138">**оемевенткоде**</span><span class="sxs-lookup"><span data-stu-id="87ffc-138">**OEMEventCode**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="87ffc-139">Тип данных: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="87ffc-139">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="87ffc-140">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="87ffc-140">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="87ffc-141">Квалификаторы: [**маппингстрингс**](../wmisdk/standard-qualifiers.md) (" \| события управления питанием Win32API")</span><span class="sxs-lookup"><span data-stu-id="87ffc-141">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32API\|Power Management Events")</span></span>
</dt> </dl>

<span data-ttu-id="87ffc-142">Состояние питания системы, определенное изготовителем оборудования (OEM), если свойство **EventType** этого класса имеет значение 11 (событие OEM); в противном случае этому свойству присваивается **значение NULL**.</span><span class="sxs-lookup"><span data-stu-id="87ffc-142">System power state defined by the original equipment manufacturer (OEM) when the **EventType** property of this class is set to 11 (OEM Event); otherwise, this property is set to **NULL**.</span></span> <span data-ttu-id="87ffc-143">События OEM генерируются, когда BIOS APM сообщает о событии APM OEM.</span><span class="sxs-lookup"><span data-stu-id="87ffc-143">OEM events are generated when an APM BIOS signals an APM OEM event.</span></span> <span data-ttu-id="87ffc-144">Коды событий OEM находятся в диапазоне 0x0200h-0x02FFh.</span><span class="sxs-lookup"><span data-stu-id="87ffc-144">OEM event codes are in the range 0x0200h - 0x02FFh.</span></span>

</dd> <dt>

<span data-ttu-id="87ffc-145">**\_дескриптор безопасности**</span><span class="sxs-lookup"><span data-stu-id="87ffc-145">**SECURITY\_DESCRIPTOR**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="87ffc-146">Тип данных: массив **Uint8**</span><span class="sxs-lookup"><span data-stu-id="87ffc-146">Data type: **uint8** array</span></span>
</dt> <dt>

<span data-ttu-id="87ffc-147">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="87ffc-147">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="87ffc-148">Дескриптор, используемый поставщиком событий для определения того, какие пользователи могут получить событие.</span><span class="sxs-lookup"><span data-stu-id="87ffc-148">Descriptor used by the event provider to determine which users can receive the event.</span></span> <span data-ttu-id="87ffc-149">Это свойство наследуется от [**\_ \_ события**](../wmisdk/--event.md).</span><span class="sxs-lookup"><span data-stu-id="87ffc-149">This property is inherited from [**\_\_Event**](../wmisdk/--event.md).</span></span> <span data-ttu-id="87ffc-150">Дополнительные сведения о константах, используемых для задания этого дескриптора безопасности, см. в разделе [константы безопасности WMI](../wmisdk/wmi-security-constants.md).</span><span class="sxs-lookup"><span data-stu-id="87ffc-150">For more information about constants used to set this security descriptor, see [WMI Security Constants](../wmisdk/wmi-security-constants.md).</span></span>

</dd> <dt>

<span data-ttu-id="87ffc-151">**ВРЕМЯ \_ создания**</span><span class="sxs-lookup"><span data-stu-id="87ffc-151">**TIME\_CREATED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="87ffc-152">Тип данных: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="87ffc-152">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="87ffc-153">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="87ffc-153">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="87ffc-154">Уникальное значение, указывающее время создания события.</span><span class="sxs-lookup"><span data-stu-id="87ffc-154">Unique value that indicates the time at which the event was generated.</span></span> <span data-ttu-id="87ffc-155">Это 64-разрядное значение, представляющее число 100-наносекундных интервалов после 1 января 1601 г.</span><span class="sxs-lookup"><span data-stu-id="87ffc-155">This is a 64-bit value that represents the number of 100-nanosecond intervals after January 1, 1601.</span></span> <span data-ttu-id="87ffc-156">Эти сведения находятся в формате всеобщего скоординированного времени (UTC).</span><span class="sxs-lookup"><span data-stu-id="87ffc-156">The information is in the Coordinated Universal Times (UTC) format.</span></span>

<span data-ttu-id="87ffc-157">Это свойство наследуется от [**\_ \_ события**](../wmisdk/--event.md).</span><span class="sxs-lookup"><span data-stu-id="87ffc-157">This property is inherited from [**\_\_Event**](../wmisdk/--event.md).</span></span>

<span data-ttu-id="87ffc-158">Дополнительные сведения об использовании значений **UInt64** в скриптах см. [в разделе Создание сценариев в WMI](../wmisdk/creating-a-wmi-script.md).</span><span class="sxs-lookup"><span data-stu-id="87ffc-158">For more information about using **uint64** values in scripts, see [Scripting in WMI](../wmisdk/creating-a-wmi-script.md).</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="87ffc-159">Комментарии</span><span class="sxs-lookup"><span data-stu-id="87ffc-159">Remarks</span></span>

<span data-ttu-id="87ffc-160">Класс **Win32 \_ поверманажементевент** является производным от [**\_ \_ екстринсицевент**](../wmisdk/--extrinsicevent.md).</span><span class="sxs-lookup"><span data-stu-id="87ffc-160">The **Win32\_PowerManagementEvent** class is derived from [**\_\_ExtrinsicEvent**](../wmisdk/--extrinsicevent.md).</span></span>

<span data-ttu-id="87ffc-161">Изменения в состоянии электропитания часто указывают на наличие проблемы с компьютером или с другим управляемым устройством.</span><span class="sxs-lookup"><span data-stu-id="87ffc-161">Changes in power status often indicate that a problem has occurred with a computer or with another managed device.</span></span> <span data-ttu-id="87ffc-162">Если сервер неожиданно переключается от питания от сети к источнику бесперебойного питания, это изменение может указывать на то, что произошла электрическая проблема определенного рода, с компьютером или с электрической системой в комнате, в которой хранится компьютер.</span><span class="sxs-lookup"><span data-stu-id="87ffc-162">If a server suddenly switches from AC power to an uninterruptible power supply, this change can indicate that an electrical problem of some kind has occurred, either with the computer itself or with the electrical system in the room in which the computer is kept.</span></span>

<span data-ttu-id="87ffc-163">Администраторам необходимо отслеживать эти изменения в состоянии электропитания и немедленно получать уведомления об этих изменениях.</span><span class="sxs-lookup"><span data-stu-id="87ffc-163">Administrators need to monitor these changes in power status and be notified of such changes immediately.</span></span> <span data-ttu-id="87ffc-164">Это позволит им выполнять действия до того, как устройство полностью теряет питание.</span><span class="sxs-lookup"><span data-stu-id="87ffc-164">This enables them to take action before the device loses power entirely.</span></span> <span data-ttu-id="87ffc-165">(Например, системы источников бесперебойного питания могут работать только через 15 минут или до завершения работы.)</span><span class="sxs-lookup"><span data-stu-id="87ffc-165">(Uninterruptible power supply systems, for example, might run for only 15 minutes or so before shutting down.)</span></span>

<span data-ttu-id="87ffc-166">Класс **Win32 \_ поверманажементевент** можно использовать для отслеживания изменений состояния питания на компьютере.</span><span class="sxs-lookup"><span data-stu-id="87ffc-166">The **Win32\_PowerManagementEvent** class can be used to monitor changes in power status on a computer.</span></span> <span data-ttu-id="87ffc-167">Эти изменения могут включать в себя переключение с одного источника питания на другой, а также на изменение состояния электропитания компьютера (например, ввод или выход из режима приостановки).</span><span class="sxs-lookup"><span data-stu-id="87ffc-167">These changes can include a switch from one power source to another as well as a change in computer power state (for example, entering or exiting Suspend mode).</span></span>

<span data-ttu-id="87ffc-168">Класс **Win32 \_ поверманажементевент** имеет только два свойства: EventType, используемый для указания типа произошедшего события изменения питания, и оемевенттипе, который используется некоторыми производителями оборудования для определения дополнительных событий изменения питания.</span><span class="sxs-lookup"><span data-stu-id="87ffc-168">The **Win32\_PowerManagementEvent** class has only two properties: EventType, used to indicate the type of power change event that occurred, and OEMEventType, which is used by some original equipment manufacturers to define additional power change events.</span></span>

<span data-ttu-id="87ffc-169">Дополнительные сведения о реагировании на события питания Windows см. в статье [мониторинг и реагирование на события питания Windows с помощью PowerShell](https://blogs.technet.com/b/heyscriptingguy/archive/2011/08/16/monitor-and-respond-to-windows-power-events-with-powershell.aspx) в разделе "Эй!".</span><span class="sxs-lookup"><span data-stu-id="87ffc-169">For more information on responding to Windows power events, see the [Monitor and Respond to Windows Power Events with PowerShell](https://blogs.technet.com/b/heyscriptingguy/archive/2011/08/16/monitor-and-respond-to-windows-power-events-with-powershell.aspx) article on the Hey!</span></span> <span data-ttu-id="87ffc-170">Сценарист!</span><span class="sxs-lookup"><span data-stu-id="87ffc-170">Scripting Guy!</span></span> <span data-ttu-id="87ffc-171">.</span><span class="sxs-lookup"><span data-stu-id="87ffc-171">blog.</span></span>

## <a name="examples"></a><span data-ttu-id="87ffc-172">Примеры</span><span class="sxs-lookup"><span data-stu-id="87ffc-172">Examples</span></span>

<span data-ttu-id="87ffc-173">Следующий сценарий VBScript отслеживает изменения состояния питания на компьютере.</span><span class="sxs-lookup"><span data-stu-id="87ffc-173">The following VBScript monitors changes in power status on a computer.</span></span>


```VB
Set colMonitoredEvents = GetObject("winmgmts:")._
 ExecNotificationQuery("SELECT * FROM Win32_PowerManagementEvent")
Do
 Set strLatestEvent = colMonitoredEvents.NextEvent
 Wscript.Echo strLatestEvent.EventType
Loop
```



## <a name="requirements"></a><span data-ttu-id="87ffc-174">Требования</span><span class="sxs-lookup"><span data-stu-id="87ffc-174">Requirements</span></span>



| <span data-ttu-id="87ffc-175">Требование</span><span class="sxs-lookup"><span data-stu-id="87ffc-175">Requirement</span></span> | <span data-ttu-id="87ffc-176">Значение</span><span class="sxs-lookup"><span data-stu-id="87ffc-176">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="87ffc-177">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="87ffc-177">Minimum supported client</span></span><br/> | <span data-ttu-id="87ffc-178">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="87ffc-178">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="87ffc-179">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="87ffc-179">Minimum supported server</span></span><br/> | <span data-ttu-id="87ffc-180">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="87ffc-180">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="87ffc-181">Пространство имен</span><span class="sxs-lookup"><span data-stu-id="87ffc-181">Namespace</span></span><br/>                | <span data-ttu-id="87ffc-182">Корневой \\ CIMV2</span><span class="sxs-lookup"><span data-stu-id="87ffc-182">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="87ffc-183">MOF</span><span class="sxs-lookup"><span data-stu-id="87ffc-183">MOF</span></span><br/>                      | <dl> <span data-ttu-id="87ffc-184"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="87ffc-184"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="87ffc-185">DLL</span><span class="sxs-lookup"><span data-stu-id="87ffc-185">DLL</span></span><br/>                      | <dl> <span data-ttu-id="87ffc-186"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="87ffc-186"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="87ffc-187">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="87ffc-187">See also</span></span>

<dl> <dt>

[<span data-ttu-id="87ffc-188">**\_\_екстринсицевент**</span><span class="sxs-lookup"><span data-stu-id="87ffc-188">**\_\_ExtrinsicEvent**</span></span>](../wmisdk/--extrinsicevent.md)
</dt> <dt>

[<span data-ttu-id="87ffc-189">Аппаратные классы системы компьютера</span><span class="sxs-lookup"><span data-stu-id="87ffc-189">Computer System Hardware Classes</span></span>](computer-system-hardware-classes.md)
</dt> <dt>

<span data-ttu-id="87ffc-190">[Наблюдение за изменениями в состоянии электропитания компьютера](/previous-versions/tn-archive/ee176537(v=technet.10))</span><span class="sxs-lookup"><span data-stu-id="87ffc-190">[Monitoring Changes in Computer Power Status](/previous-versions/tn-archive/ee176537(v=technet.10))</span></span>
</dt> </dl>

 

 
