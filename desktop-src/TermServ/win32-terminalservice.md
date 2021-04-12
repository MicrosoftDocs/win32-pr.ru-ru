---
title: Класс Win32_TerminalService
description: Подкласс \_ класса службы Win32. Win32 \_ терминалсервице представляет свойство element \_ ассоциации Win32 терминалсервицетосеттинг.
ms.assetid: 06c69d71-4e6f-48af-b13d-e593b8fcf376
ms.tgt_platform: multiple
keywords:
- Класс Win32_TerminalService службы удаленных рабочих столов
- Службы удаленных рабочих столов класса Win32_TerminalService, описание
topic_type:
- apiref
api_name:
- Win32_TerminalService
- Win32_TerminalService.AcceptPause
- Win32_TerminalService.AcceptStop
- Win32_TerminalService.Caption
- Win32_TerminalService.CheckPoint
- Win32_TerminalService.CreationClassName
- Win32_TerminalService.DelayedAutoStart
- Win32_TerminalService.Description
- Win32_TerminalService.DesktopInteract
- Win32_TerminalService.DisplayName
- Win32_TerminalService.ErrorControl
- Win32_TerminalService.ExitCode
- Win32_TerminalService.InstallDate
- Win32_TerminalService.Name
- Win32_TerminalService.PathName
- Win32_TerminalService.ProcessId
- Win32_TerminalService.ServiceSpecificExitCode
- Win32_TerminalService.ServiceType
- Win32_TerminalService.Started
- Win32_TerminalService.StartMode
- Win32_TerminalService.StartName
- Win32_TerminalService.State
- Win32_TerminalService.Status
- Win32_TerminalService.SystemCreationClassName
- Win32_TerminalService.SystemName
- Win32_TerminalService.TagId
- Win32_TerminalService.WaitHint
- Win32_TerminalService.DisconnectedSessions
- Win32_TerminalService.TotalSessions
api_location:
- TSCfgWmi.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ba5646c6ac9abf41fddc023ad39884e611681a71
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104492735"
---
# <a name="win32_terminalservice-class"></a><span data-ttu-id="03025-106">\_Класс Win32 терминалсервице</span><span class="sxs-lookup"><span data-stu-id="03025-106">Win32\_TerminalService class</span></span>

<span data-ttu-id="03025-107">Класс **WMI \_ Терминалсервице для Win32** является подклассом класса [**\_ службы Win32**](/windows/desktop/CIMWin32Prov/win32-service) .</span><span class="sxs-lookup"><span data-stu-id="03025-107">The **Win32\_TerminalService** WMI class is a subclass of the [**Win32\_Service**](/windows/desktop/CIMWin32Prov/win32-service) class.</span></span> <span data-ttu-id="03025-108">**Win32 \_ Терминалсервице** представляет свойство **element** ассоциации [**Win32 \_ терминалсервицетосеттинг**](win32-terminalservicetosetting.md) .</span><span class="sxs-lookup"><span data-stu-id="03025-108">**Win32\_TerminalService** represents the **Element** property of the [**Win32\_TerminalServiceToSetting**](win32-terminalservicetosetting.md) association.</span></span>

<span data-ttu-id="03025-109">Следующий синтаксис упрощен из MOF-кода и включает все определенные и унаследованные свойства в алфавитном порядке.</span><span class="sxs-lookup"><span data-stu-id="03025-109">The following syntax is simplified from MOF code and includes all defined and inherited properties, in alphabetical order.</span></span>

## <a name="syntax"></a><span data-ttu-id="03025-110">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="03025-110">Syntax</span></span>

``` syntax
[dynamic, provider("Win32_WIN32_TERMINALSERVICE_Prov"), ClassContext("local|hkey_local_machine\\SYSTEM\\CurrentControlSet\\Control\\TerminalServer"), AMENDMENT]
class Win32_TerminalService : Win32_Service
{
  boolean  AcceptPause;
  boolean  AcceptStop;
  string   Caption;
  uint32   CheckPoint;
  string   CreationClassName;
  boolean  DelayedAutoStart;
  string   Description;
  boolean  DesktopInteract;
  string   DisplayName;
  string   ErrorControl;
  uint32   ExitCode;
  datetime InstallDate;
  string   Name;
  string   PathName;
  uint32   ProcessId;
  uint32   ServiceSpecificExitCode;
  string   ServiceType;
  boolean  Started;
  string   StartMode;
  string   StartName;
  string   State;
  string   Status;
  string   SystemCreationClassName;
  string   SystemName;
  uint32   TagId;
  uint32   WaitHint;
  uint32   DisconnectedSessions;
  uint32   TotalSessions;
};
```

## <a name="members"></a><span data-ttu-id="03025-111">Члены</span><span class="sxs-lookup"><span data-stu-id="03025-111">Members</span></span>

<span data-ttu-id="03025-112">Класс **Win32 \_ терминалсервице** имеет следующие типы членов:</span><span class="sxs-lookup"><span data-stu-id="03025-112">The **Win32\_TerminalService** class has these types of members:</span></span>

-   [<span data-ttu-id="03025-113">Методы</span><span class="sxs-lookup"><span data-stu-id="03025-113">Methods</span></span>](#methods)
-   [<span data-ttu-id="03025-114">Свойства</span><span class="sxs-lookup"><span data-stu-id="03025-114">Properties</span></span>](#properties)

### <a name="methods"></a><span data-ttu-id="03025-115">Методы</span><span class="sxs-lookup"><span data-stu-id="03025-115">Methods</span></span>

<span data-ttu-id="03025-116">Класс **Win32 \_ терминалсервице** содержит следующие методы.</span><span class="sxs-lookup"><span data-stu-id="03025-116">The **Win32\_TerminalService** class has these methods.</span></span>



| <span data-ttu-id="03025-117">Метод</span><span class="sxs-lookup"><span data-stu-id="03025-117">Method</span></span>                                                                       | <span data-ttu-id="03025-118">Описание</span><span class="sxs-lookup"><span data-stu-id="03025-118">Description</span></span>                                                                                          |
|:-----------------------------------------------------------------------------|:-----------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="03025-119">**Change**</span><span class="sxs-lookup"><span data-stu-id="03025-119">**Change**</span></span>](win32-terminalservice-change.md)                               | <span data-ttu-id="03025-120">Изменяет службу.</span><span class="sxs-lookup"><span data-stu-id="03025-120">Modifies a service.</span></span><br/>                                                                       |
| [<span data-ttu-id="03025-121">**чанжестартмоде**</span><span class="sxs-lookup"><span data-stu-id="03025-121">**ChangeStartMode**</span></span>](win32-terminalservice-changestartmode.md)             | <span data-ttu-id="03025-122">Изменяет режим запуска службы.</span><span class="sxs-lookup"><span data-stu-id="03025-122">Modifies the start mode of a service.</span></span><br/>                                                     |
| [<span data-ttu-id="03025-123">**Создать**</span><span class="sxs-lookup"><span data-stu-id="03025-123">**Create**</span></span>](win32-terminalservice-create.md)                               | <span data-ttu-id="03025-124">Создает новую службу.</span><span class="sxs-lookup"><span data-stu-id="03025-124">Creates a new service.</span></span><br/>                                                                    |
| [<span data-ttu-id="03025-125">**Удалить**</span><span class="sxs-lookup"><span data-stu-id="03025-125">**Delete**</span></span>](win32-terminalservice-delete.md)                               | <span data-ttu-id="03025-126">Удаляет существующую службу.</span><span class="sxs-lookup"><span data-stu-id="03025-126">Deletes an existing service.</span></span><br/>                                                              |
| [<span data-ttu-id="03025-127">**жетсекуритидескриптор**</span><span class="sxs-lookup"><span data-stu-id="03025-127">**GetSecurityDescriptor**</span></span>](win32-terminalservice-getsecuritydescriptor.md) | <span data-ttu-id="03025-128">Возвращает дескриптор безопасности, управляющий доступом к службе.</span><span class="sxs-lookup"><span data-stu-id="03025-128">Returns the security descriptor that controls access to the service.</span></span><br/>                      |
| [<span data-ttu-id="03025-129">**интеррогатесервице**</span><span class="sxs-lookup"><span data-stu-id="03025-129">**InterrogateService**</span></span>](win32-terminalservice-interrogateservice.md)       | <span data-ttu-id="03025-130">Запрашивает обновление состояния службы до Service Manager.</span><span class="sxs-lookup"><span data-stu-id="03025-130">Requests that a service update its state to the service manager.</span></span><br/>                          |
| [<span data-ttu-id="03025-131">**PauseService**</span><span class="sxs-lookup"><span data-stu-id="03025-131">**PauseService**</span></span>](win32-terminalservice-pauseservice.md)                   | <span data-ttu-id="03025-132">Пытается перевести службу в приостановленное состояние.</span><span class="sxs-lookup"><span data-stu-id="03025-132">Attempts to place a service in the paused state.</span></span><br/>                                          |
| [<span data-ttu-id="03025-133">**ResumeService**</span><span class="sxs-lookup"><span data-stu-id="03025-133">**ResumeService**</span></span>](win32-terminalservice-resumeservice.md)                 | <span data-ttu-id="03025-134">Пытается перевести службу в состояние возобновления.</span><span class="sxs-lookup"><span data-stu-id="03025-134">Attempts to place a service in the resumed state.</span></span><br/>                                         |
| [<span data-ttu-id="03025-135">**сетсекуритидескриптор**</span><span class="sxs-lookup"><span data-stu-id="03025-135">**SetSecurityDescriptor**</span></span>](win32-terminalservice-setsecuritydescriptor.md) | <span data-ttu-id="03025-136">Записывает обновленную версию дескриптора безопасности, которая управляет доступом к службе.</span><span class="sxs-lookup"><span data-stu-id="03025-136">Writes an updated version of the security descriptor that controls access to the service.</span></span><br/> |
| [<span data-ttu-id="03025-137">**StartService**</span><span class="sxs-lookup"><span data-stu-id="03025-137">**StartService**</span></span>](win32-terminalservice-startservice.md)                   | <span data-ttu-id="03025-138">Пытается перевести службу в состояние запуска.</span><span class="sxs-lookup"><span data-stu-id="03025-138">Attempts to place a service into the startup state.</span></span><br/>                                       |
| [<span data-ttu-id="03025-139">**StopService**</span><span class="sxs-lookup"><span data-stu-id="03025-139">**StopService**</span></span>](win32-terminalservice-stopservice.md)                     | <span data-ttu-id="03025-140">Помещает службу в остановленное состояние.</span><span class="sxs-lookup"><span data-stu-id="03025-140">Places a service in the stopped state.</span></span><br/>                                                    |
| [<span data-ttu-id="03025-141">**усерконтролсервице**</span><span class="sxs-lookup"><span data-stu-id="03025-141">**UserControlService**</span></span>](win32-terminalservice-usercontrolservice.md)       | <span data-ttu-id="03025-142">Пытается отправить в службу определенный пользователем управляющий код.</span><span class="sxs-lookup"><span data-stu-id="03025-142">Attempts to send a user-defined control code to a service.</span></span><br/>                                |



 

### <a name="properties"></a><span data-ttu-id="03025-143">Свойства</span><span class="sxs-lookup"><span data-stu-id="03025-143">Properties</span></span>

<span data-ttu-id="03025-144">Класс **Win32 \_ терминалсервице** имеет следующие свойства.</span><span class="sxs-lookup"><span data-stu-id="03025-144">The **Win32\_TerminalService** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="03025-145">**AcceptPause**</span><span class="sxs-lookup"><span data-stu-id="03025-145">**AcceptPause**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="03025-146">Тип данных: **логический**</span><span class="sxs-lookup"><span data-stu-id="03025-146">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="03025-147">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="03025-147">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="03025-148">Квалификаторы: [**маппингстрингс**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32API \| Service Structures \| [**\_ Status**](/windows/desktop/api/winsvc/ns-winsvc-service_status) \| двконтролсакцептед \| Service \_ Accept \_ Пауза \_ Continue"), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("служба принимает паузу")</span><span class="sxs-lookup"><span data-stu-id="03025-148">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32API\|Service Structures\|[**SERVICE\_STATUS**](/windows/desktop/api/winsvc/ns-winsvc-service_status)\|dwControlsAccepted\|SERVICE\_ACCEPT\_PAUSE\_CONTINUE"), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Service Accepts Pause")</span></span>
</dt> </dl>

<span data-ttu-id="03025-149">Указывает, можно ли приостановить работу службы.</span><span class="sxs-lookup"><span data-stu-id="03025-149">Indicates whether the service can be paused.</span></span>

<span data-ttu-id="03025-150">Это свойство наследуется из [**Win32 \_ басесервице**](/windows/desktop/CIMWin32Prov/win32-baseservice).</span><span class="sxs-lookup"><span data-stu-id="03025-150">This property is inherited from [**Win32\_BaseService**](/windows/desktop/CIMWin32Prov/win32-baseservice).</span></span>

</dd> <dt>

<span data-ttu-id="03025-151">**AcceptStop**</span><span class="sxs-lookup"><span data-stu-id="03025-151">**AcceptStop**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="03025-152">Тип данных: **логический**</span><span class="sxs-lookup"><span data-stu-id="03025-152">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="03025-153">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="03025-153">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="03025-154">Квалификаторы: [**маппингстрингс**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32API \| Service Structures \| [**\_ Status**](/windows/desktop/api/winsvc/ns-winsvc-service_status) \| двконтролсакцептед \| Service \_ Accept \_ "), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("служба принимает" останавливается ").</span><span class="sxs-lookup"><span data-stu-id="03025-154">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32API\|Service Structures\|[**SERVICE\_STATUS**](/windows/desktop/api/winsvc/ns-winsvc-service_status)\|dwControlsAccepted\|SERVICE\_ACCEPT\_STOP"), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Service Accepts Stop")</span></span>
</dt> </dl>

<span data-ttu-id="03025-155">Указывает, можно ли остановить службу.</span><span class="sxs-lookup"><span data-stu-id="03025-155">Indicates whether the service can be stopped.</span></span>

<span data-ttu-id="03025-156">Это свойство наследуется из [**Win32 \_ басесервице**](/windows/desktop/CIMWin32Prov/win32-baseservice).</span><span class="sxs-lookup"><span data-stu-id="03025-156">This property is inherited from [**Win32\_BaseService**](/windows/desktop/CIMWin32Prov/win32-baseservice).</span></span>

</dd> <dt>

<span data-ttu-id="03025-157">**Заголовок**</span><span class="sxs-lookup"><span data-stu-id="03025-157">**Caption**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="03025-158">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="03025-158">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="03025-159">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="03025-159">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="03025-160">Квалификаторы: [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (64), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Caption")</span><span class="sxs-lookup"><span data-stu-id="03025-160">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Caption")</span></span>
</dt> </dl>

<span data-ttu-id="03025-161">Краткое описание службы — однострочная строка.</span><span class="sxs-lookup"><span data-stu-id="03025-161">Short description of the service  a one-line string.</span></span>

<span data-ttu-id="03025-162">Это свойство наследуется от [**CIM \_ манажедсистемелемент**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span><span class="sxs-lookup"><span data-stu-id="03025-162">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

</dd> <dt>

<span data-ttu-id="03025-163">**Создание**</span><span class="sxs-lookup"><span data-stu-id="03025-163">**CheckPoint**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="03025-164">Тип данных: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="03025-164">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="03025-165">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="03025-165">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="03025-166">Квалификаторы: [**маппингстрингс**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32API \| Service Structures \| [**\_ Status**](/windows/desktop/api/winsvc/ns-winsvc-service_status) \| Двчеккпоинт"), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("число контрольных точек")</span><span class="sxs-lookup"><span data-stu-id="03025-166">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32API\|Service Structures\|[**SERVICE\_STATUS**](/windows/desktop/api/winsvc/ns-winsvc-service_status)\|dwCheckPoint"), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Check Point Count")</span></span>
</dt> </dl>

<span data-ttu-id="03025-167">Значение, которое служба периодически увеличивает, чтобы сообщить о ходе выполнения во время длительной операции запуска, остановки, приостановки или продолжения работы.</span><span class="sxs-lookup"><span data-stu-id="03025-167">Value that the service increments periodically to report its progress during a long start, stop, pause, or continue operation.</span></span> <span data-ttu-id="03025-168">Например, служба увеличивает это значение по мере завершения каждого этапа инициализации при запуске.</span><span class="sxs-lookup"><span data-stu-id="03025-168">For example, the service increments this value as it completes each step of its initialization when it is starting up.</span></span> <span data-ttu-id="03025-169">Программа пользовательского интерфейса, вызывающая операцию в службе, использует это значение для отслеживания хода выполнения службы во время длительной операции.</span><span class="sxs-lookup"><span data-stu-id="03025-169">The user interface program that invokes the operation on the service uses this value to track the progress of the service during a lengthy operation.</span></span> <span data-ttu-id="03025-170">Это значение недопустимо и должно быть равно нулю, если у службы нет ожидающих операций запуска, остановки, приостановки или возобновления.</span><span class="sxs-lookup"><span data-stu-id="03025-170">This value is not valid and should be zero when the service does not have a start, stop, pause, or continue operation pending.</span></span>

<span data-ttu-id="03025-171">Это свойство наследуется [**от \_ службы Win32**](/windows/desktop/CIMWin32Prov/win32-service).</span><span class="sxs-lookup"><span data-stu-id="03025-171">This property is inherited from [**Win32\_Service**](/windows/desktop/CIMWin32Prov/win32-service).</span></span>

</dd> <dt>

<span data-ttu-id="03025-172">**CreationClassName**</span><span class="sxs-lookup"><span data-stu-id="03025-172">**CreationClassName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="03025-173">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="03025-173">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="03025-174">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="03025-174">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="03025-175">Квалификаторы: [**\_ ключ CIM**](/windows/desktop/WmiSdk/standard-wmi-qualifiers), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("имя класса")</span><span class="sxs-lookup"><span data-stu-id="03025-175">Qualifiers: [**CIM\_Key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Class Name")</span></span>
</dt> </dl>

<span data-ttu-id="03025-176">Имя первого конкретного класса, который будет отображаться в цепочке наследования, используемой при создании экземпляра.</span><span class="sxs-lookup"><span data-stu-id="03025-176">Name of the first concrete class to appear in the inheritance chain used in the creation of an instance.</span></span> <span data-ttu-id="03025-177">При использовании с другими ключевыми свойствами класса это свойство позволяет уникально идентифицировать все экземпляры этого класса и его подклассов.</span><span class="sxs-lookup"><span data-stu-id="03025-177">When used with the other key properties of the class, this property allows all instances of this class and its subclasses to be uniquely identified.</span></span>

<span data-ttu-id="03025-178">Это свойство наследуется [**от \_ службы CIM**](/windows/desktop/CIMWin32Prov/cim-service).</span><span class="sxs-lookup"><span data-stu-id="03025-178">This property is inherited from [**CIM\_Service**](/windows/desktop/CIMWin32Prov/cim-service).</span></span>

</dd> <dt>

<span data-ttu-id="03025-179">**DelayedAutoStart**</span><span class="sxs-lookup"><span data-stu-id="03025-179">**DelayedAutoStart**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="03025-180">Тип данных: **логический**</span><span class="sxs-lookup"><span data-stu-id="03025-180">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="03025-181">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="03025-181">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="03025-182">Квалификаторы: [**маппингстрингс**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32API Service Structures" \| \| [**Service \_ delay \_ \_ Start \_ info**](/windows/desktop/api/winsvc/ns-winsvc-service_delayed_auto_start_info) \| фделайедаутостарт "), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) (" отложенный автоматический запуск ")</span><span class="sxs-lookup"><span data-stu-id="03025-182">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32API\|Service Structures\|[**SERVICE\_DELAYED\_AUTO\_START\_INFO**](/windows/desktop/api/winsvc/ns-winsvc-service_delayed_auto_start_info)\|fDelayedAutostart"), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Delayed Auto-Start")</span></span>
</dt> </dl>

<span data-ttu-id="03025-183">Если **значение — true**, служба запускается после запуска других служб, запускающих автозапуск, и короткой задержки.</span><span class="sxs-lookup"><span data-stu-id="03025-183">If **True**, the service is started after other auto-start services are started plus a short delay.</span></span>

<span data-ttu-id="03025-184">**Windows server 2012 R2, Windows 8.1, Windows server 2012, Windows 8, Windows server 2008 R2, Windows 7, Windows server 2008 и Windows Vista:** Это свойство не поддерживается до Windows Server 2016 и Windows 10.</span><span class="sxs-lookup"><span data-stu-id="03025-184">**Windows Server 2012 R2, Windows 8.1, Windows Server 2012, Windows 8, Windows Server 2008 R2, Windows 7, Windows Server 2008 and Windows Vista:** This property is not supported before Windows Server 2016 and Windows 10.</span></span>

<span data-ttu-id="03025-185">Это свойство наследуется [**от \_ службы Win32**](/windows/desktop/CIMWin32Prov/win32-service).</span><span class="sxs-lookup"><span data-stu-id="03025-185">This property is inherited from [**Win32\_Service**](/windows/desktop/CIMWin32Prov/win32-service).</span></span>

</dd> <dt>

<span data-ttu-id="03025-186">**Описание**</span><span class="sxs-lookup"><span data-stu-id="03025-186">**Description**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="03025-187">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="03025-187">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="03025-188">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="03025-188">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="03025-189">Квалификаторы: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Описание")</span><span class="sxs-lookup"><span data-stu-id="03025-189">Qualifiers: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Description")</span></span>
</dt> </dl>

<span data-ttu-id="03025-190">Описание объекта.</span><span class="sxs-lookup"><span data-stu-id="03025-190">Description of the object.</span></span>

<span data-ttu-id="03025-191">Это свойство наследуется от [**CIM \_ манажедсистемелемент**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span><span class="sxs-lookup"><span data-stu-id="03025-191">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

</dd> <dt>

<span data-ttu-id="03025-192">**DesktopInteract**</span><span class="sxs-lookup"><span data-stu-id="03025-192">**DesktopInteract**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="03025-193">Тип данных: **логический**</span><span class="sxs-lookup"><span data-stu-id="03025-193">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="03025-194">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="03025-194">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="03025-195">Квалификаторы: [**маппингстрингс**](/windows/desktop/WmiSdk/standard-qualifiers) (" \| структуры служб Win32API \| [**запрос \_ \_ конфигурации**](/windows/desktop/api/winsvc/ns-winsvc-query_service_configa)службы \| двсервицетипе \| \_ Интерактивный \_ процесс"), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("взаимодействует с Desktop")</span><span class="sxs-lookup"><span data-stu-id="03025-195">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32API\|Service Structures\|[**QUERY\_SERVICE\_CONFIG**](/windows/desktop/api/winsvc/ns-winsvc-query_service_configa)\|dwServiceType\|SERVICE\_INTERACTIVE\_PROCESS"), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Interacts With Desktop")</span></span>
</dt> </dl>

<span data-ttu-id="03025-196">Указывает, может ли служба создавать и взаимодействовать с Windows на настольном компьютере и, таким образом, взаимодействовать с пользователем.</span><span class="sxs-lookup"><span data-stu-id="03025-196">Indicates whether the service can create or communicate with windows on the desktop, and thus interact in some way with a user.</span></span> <span data-ttu-id="03025-197">Интерактивные службы должны запускаться под локальной системной учетной записью.</span><span class="sxs-lookup"><span data-stu-id="03025-197">Interactive services must run under the Local System account.</span></span> <span data-ttu-id="03025-198">Большинство служб не являются интерактивными; то есть они не взаимодействуют с пользователем каким-либо образом.</span><span class="sxs-lookup"><span data-stu-id="03025-198">Most services are not interactive; that is, they do not communicate with the user in any way.</span></span>

<span data-ttu-id="03025-199">Это свойство наследуется из [**Win32 \_ басесервице**](/windows/desktop/CIMWin32Prov/win32-baseservice).</span><span class="sxs-lookup"><span data-stu-id="03025-199">This property is inherited from [**Win32\_BaseService**](/windows/desktop/CIMWin32Prov/win32-baseservice).</span></span>

</dd> <dt>

<span data-ttu-id="03025-200">**дисконнектедсессионс**</span><span class="sxs-lookup"><span data-stu-id="03025-200">**DisconnectedSessions**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="03025-201">Тип данных: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="03025-201">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="03025-202">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="03025-202">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="03025-203">Число отключенных сеансов на текущем сервере.</span><span class="sxs-lookup"><span data-stu-id="03025-203">The number of disconnected sessions on the current server.</span></span> <span data-ttu-id="03025-204">Эти сеансы по-прежнему могут активно потреблять ресурсы сервера, но в настоящее время они не имеют сетевого подключения к клиенту.</span><span class="sxs-lookup"><span data-stu-id="03025-204">These sessions may still be actively consuming server resources, however they currently have no network connection with a client.</span></span>

</dd> <dt>

<span data-ttu-id="03025-205">**Отображаемое имя**</span><span class="sxs-lookup"><span data-stu-id="03025-205">**DisplayName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="03025-206">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="03025-206">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="03025-207">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="03025-207">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="03025-208">Квалификаторы: [**маппингстрингс**](/windows/desktop/WmiSdk/standard-qualifiers) (" \| структуры служб Win32API \| [**запрос \_ \_ конфигурации службы**](/windows/desktop/api/winsvc/ns-winsvc-query_service_configa) \| Лпдисплайнаме"), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("отображаемое имя")</span><span class="sxs-lookup"><span data-stu-id="03025-208">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32API\|Service Structures\|[**QUERY\_SERVICE\_CONFIG**](/windows/desktop/api/winsvc/ns-winsvc-query_service_configa)\|lpDisplayName"), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Display Name")</span></span>
</dt> </dl>

<span data-ttu-id="03025-209">Имя службы, отображаемое в оснастке "службы".</span><span class="sxs-lookup"><span data-stu-id="03025-209">Name of the service as viewed in the Services snap-in.</span></span> <span data-ttu-id="03025-210">Максимальная длина этой строки равна 256 символам.</span><span class="sxs-lookup"><span data-stu-id="03025-210">This string has a maximum length of 256 characters.</span></span> <span data-ttu-id="03025-211">Обратите внимание, что отображаемое имя и имя службы (которые хранятся в реестре) не всегда одинаковы.</span><span class="sxs-lookup"><span data-stu-id="03025-211">Note that the display name and the service name (which is stored in the registry) are not always the same.</span></span> <span data-ttu-id="03025-212">Например, служба DHCP-клиента имеет имя службы DHCP, а не отображаемое имя DHCP-клиента.</span><span class="sxs-lookup"><span data-stu-id="03025-212">For example, the DHCP Client service has the service name Dhcp but the display name DHCP Client.</span></span> <span data-ttu-id="03025-213">В диспетчере управления службами имя сохраняется с учетом регистра.</span><span class="sxs-lookup"><span data-stu-id="03025-213">The name is case-preserved in the Service Control Manager.</span></span> <span data-ttu-id="03025-214">Однако в сравнениях [**DisplayName**](/windows/desktop/CIMWin32Prov/win32-service) всегда учитывается регистр.</span><span class="sxs-lookup"><span data-stu-id="03025-214">However, [**DisplayName**](/windows/desktop/CIMWin32Prov/win32-service) comparisons are always case-insensitive.</span></span>

<span data-ttu-id="03025-215">Ограничение: принимает то же значение, что и свойство [**Name**](/windows/desktop/CIMWin32Prov/win32-service) .</span><span class="sxs-lookup"><span data-stu-id="03025-215">Constraint: Accepts the same value as the [**Name**](/windows/desktop/CIMWin32Prov/win32-service) property.</span></span>

<span data-ttu-id="03025-216">Пример: "Атдиск"</span><span class="sxs-lookup"><span data-stu-id="03025-216">Example: "Atdisk"</span></span>

<span data-ttu-id="03025-217">Это свойство наследуется из [**Win32 \_ басесервице**](/windows/desktop/CIMWin32Prov/win32-baseservice).</span><span class="sxs-lookup"><span data-stu-id="03025-217">This property is inherited from [**Win32\_BaseService**](/windows/desktop/CIMWin32Prov/win32-baseservice).</span></span>

</dd> <dt>

<span data-ttu-id="03025-218">**ErrorControl**</span><span class="sxs-lookup"><span data-stu-id="03025-218">**ErrorControl**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="03025-219">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="03025-219">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="03025-220">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="03025-220">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="03025-221">Квалификаторы: [**маппингстрингс**](/windows/desktop/WmiSdk/standard-qualifiers) (" \| структуры служб Win32API \| [**запрос \_ \_ конфигурации службы**](/windows/desktop/api/winsvc/ns-winsvc-query_service_configa) \| Дверрорконтрол"), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("серьезность сбоя при запуске")</span><span class="sxs-lookup"><span data-stu-id="03025-221">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32API\|Service Structures\|[**QUERY\_SERVICE\_CONFIG**](/windows/desktop/api/winsvc/ns-winsvc-query_service_configa)\|dwErrorControl"), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Severity Of Startup Failure")</span></span>
</dt> </dl>

<span data-ttu-id="03025-222">Серьезность ошибки, если не удается запустить службу во время запуска.</span><span class="sxs-lookup"><span data-stu-id="03025-222">Severity of the error if this service fails to start during startup.</span></span> <span data-ttu-id="03025-223">Значение указывает действие, предпринимаемое программой запуска, если происходит сбой.</span><span class="sxs-lookup"><span data-stu-id="03025-223">The value indicates the action taken by the startup program if failure occurs.</span></span> <span data-ttu-id="03025-224">Все ошибки записываются в журнал системой компьютера.</span><span class="sxs-lookup"><span data-stu-id="03025-224">All errors are logged by the computer system.</span></span>

<dt>

<span id="Ignore"></span><span id="ignore"></span><span id="IGNORE"></span>

<span data-ttu-id="03025-225"><span id="Ignore"></span><span id="ignore"></span><span id="IGNORE"></span>**Игнорировать** ("ignore")</span><span class="sxs-lookup"><span data-stu-id="03025-225"><span id="Ignore"></span><span id="ignore"></span><span id="IGNORE"></span>**Ignore** ("Ignore")</span></span>


</dt> <dd>

<span data-ttu-id="03025-226">Пользователь не получает уведомление.</span><span class="sxs-lookup"><span data-stu-id="03025-226">User is not notified.</span></span>

</dd> <dt>

<span id="Normal"></span><span id="normal"></span><span id="NORMAL"></span>

<span data-ttu-id="03025-227"><span id="Normal"></span><span id="normal"></span><span id="NORMAL"></span>**Обычная** ("Обычная")</span><span class="sxs-lookup"><span data-stu-id="03025-227"><span id="Normal"></span><span id="normal"></span><span id="NORMAL"></span>**Normal** ("Normal")</span></span>


</dt> <dd>

<span data-ttu-id="03025-228">Пользователь получает уведомление.</span><span class="sxs-lookup"><span data-stu-id="03025-228">User is notified.</span></span> <span data-ttu-id="03025-229">Обычно это будет окно сообщения с уведомлением пользователя о проблеме.</span><span class="sxs-lookup"><span data-stu-id="03025-229">Usually this will be a message box display notifying the user of the problem.</span></span>

</dd> <dt>

<span id="Severe"></span><span id="severe"></span><span id="SEVERE"></span>

<span data-ttu-id="03025-230"><span id="Severe"></span><span id="severe"></span><span id="SEVERE"></span>**Серьезная** ("серьезная")</span><span class="sxs-lookup"><span data-stu-id="03025-230"><span id="Severe"></span><span id="severe"></span><span id="SEVERE"></span>**Severe** ("Severe")</span></span>


</dt> <dd>

<span data-ttu-id="03025-231">Система перезапускается в последней известной рабочей конфигурации.</span><span class="sxs-lookup"><span data-stu-id="03025-231">System is restarted with the last-known-good configuration.</span></span>

</dd> <dt>

<span id="Critical"></span><span id="critical"></span><span id="CRITICAL"></span>

<span data-ttu-id="03025-232"><span id="Critical"></span><span id="critical"></span><span id="CRITICAL"></span>**Критическая** ("критическая")</span><span class="sxs-lookup"><span data-stu-id="03025-232"><span id="Critical"></span><span id="critical"></span><span id="CRITICAL"></span>**Critical** ("Critical")</span></span>


</dt> <dd>

<span data-ttu-id="03025-233">Попытка перезапустить систему в рабочей конфигурации.</span><span class="sxs-lookup"><span data-stu-id="03025-233">System attempts to restart with a good configuration.</span></span> <span data-ttu-id="03025-234">Если служба не запускается второй раз, происходит сбой запуска.</span><span class="sxs-lookup"><span data-stu-id="03025-234">If the service fails to start a second time, startup fails.</span></span>

</dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="03025-235"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Неизвестно** ("неизвестно")</span><span class="sxs-lookup"><span data-stu-id="03025-235"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** ("Unknown")</span></span>


</dt> <dd>

<span data-ttu-id="03025-236">Серьезность ошибки неизвестна.</span><span class="sxs-lookup"><span data-stu-id="03025-236">Severity of the error is unknown.</span></span>

</dd> </dl>

<span data-ttu-id="03025-237">Это свойство наследуется из [**Win32 \_ басесервице**](/windows/desktop/CIMWin32Prov/win32-baseservice).</span><span class="sxs-lookup"><span data-stu-id="03025-237">This property is inherited from [**Win32\_BaseService**](/windows/desktop/CIMWin32Prov/win32-baseservice).</span></span>

</dd> <dt>

<span data-ttu-id="03025-238">**ExitCode**</span><span class="sxs-lookup"><span data-stu-id="03025-238">**ExitCode**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="03025-239">Тип данных: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="03025-239">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="03025-240">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="03025-240">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="03025-241">Квалификаторы: [**маппингстрингс**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32API \| Service Structures \| [**\_ Status**](/windows/desktop/api/winsvc/ns-winsvc-service_status) \| DwWin32ExitCode"), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("код выхода")</span><span class="sxs-lookup"><span data-stu-id="03025-241">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32API\|Service Structures\|[**SERVICE\_STATUS**](/windows/desktop/api/winsvc/ns-winsvc-service_status)\|dwWin32ExitCode"), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Exit Code")</span></span>
</dt> </dl>

<span data-ttu-id="03025-242">Код ошибки Windows, определяющий ошибки, возникающие при запуске или остановке службы.</span><span class="sxs-lookup"><span data-stu-id="03025-242">Windows error code that defines errors encountered in starting or stopping the service.</span></span> <span data-ttu-id="03025-243">Это свойство имеет значение ошибка, связанное со **\_ службой \_ \_ ошибок** (1066), если ошибка является уникальной для службы, представленной этим классом, а сведения об ошибке доступны в свойстве [**сервицеспеЦифицекситкоде**](/windows/desktop/CIMWin32Prov/win32-service) .</span><span class="sxs-lookup"><span data-stu-id="03025-243">This property is set to **ERROR\_SERVICE\_SPECIFIC\_ERROR** (1066) when the error is unique to the service represented by this class, and information about the error is available in the [**ServiceSpecificExitCode**](/windows/desktop/CIMWin32Prov/win32-service) property.</span></span> <span data-ttu-id="03025-244">Служба задает это значение **без \_ ошибок** при выполнении и снова после нормального завершения.</span><span class="sxs-lookup"><span data-stu-id="03025-244">The service sets this value to **NO\_ERROR** when running, and again upon normal termination.</span></span>

<span data-ttu-id="03025-245">Это свойство наследуется из [**Win32 \_ басесервице**](/windows/desktop/CIMWin32Prov/win32-baseservice).</span><span class="sxs-lookup"><span data-stu-id="03025-245">This property is inherited from [**Win32\_BaseService**](/windows/desktop/CIMWin32Prov/win32-baseservice).</span></span>

</dd> <dt>

<span data-ttu-id="03025-246">**InstallDate**</span><span class="sxs-lookup"><span data-stu-id="03025-246">**InstallDate**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="03025-247">Тип данных: **DateTime**</span><span class="sxs-lookup"><span data-stu-id="03025-247">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="03025-248">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="03025-248">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="03025-249">Квалификаторы: [**маппингстрингс**](/windows/desktop/WmiSdk/standard-qualifiers) (MIF. DMTF \| ComponentID \| 001,5 "), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) (" Дата установки ")</span><span class="sxs-lookup"><span data-stu-id="03025-249">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|ComponentID\|001.5"), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Install Date")</span></span>
</dt> </dl>

<span data-ttu-id="03025-250">Объект Date установлен.</span><span class="sxs-lookup"><span data-stu-id="03025-250">Date object is installed.</span></span> <span data-ttu-id="03025-251">Для этого свойства не требуется указывать значение, указывающее, что объект установлен.</span><span class="sxs-lookup"><span data-stu-id="03025-251">This property does not require a value to indicate that the object is installed.</span></span>

<span data-ttu-id="03025-252">Это свойство наследуется от [**CIM \_ манажедсистемелемент**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span><span class="sxs-lookup"><span data-stu-id="03025-252">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

</dd> <dt>

<span data-ttu-id="03025-253">**Name**</span><span class="sxs-lookup"><span data-stu-id="03025-253">**Name**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="03025-254">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="03025-254">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="03025-255">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="03025-255">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="03025-256">Квалификаторы: [ **ключ**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="03025-256">Qualifiers: [**Key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

<span data-ttu-id="03025-257">Уникальный идентификатор службы, который предоставляет сведения об управляемых функциях.</span><span class="sxs-lookup"><span data-stu-id="03025-257">Unique identifier of the service that provides an indication of the functionality that is managed.</span></span> <span data-ttu-id="03025-258">Эти функциональные возможности описаны в свойстве [**Description**](/windows/desktop/CIMWin32Prov/win32-service) объекта.</span><span class="sxs-lookup"><span data-stu-id="03025-258">This functionality is described in the [**Description**](/windows/desktop/CIMWin32Prov/win32-service) property of the object.</span></span>

<span data-ttu-id="03025-259">Это свойство наследуется от [**CIM \_ манажедсистемелемент**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span><span class="sxs-lookup"><span data-stu-id="03025-259">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

</dd> <dt>

<span data-ttu-id="03025-260">**PathName**</span><span class="sxs-lookup"><span data-stu-id="03025-260">**PathName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="03025-261">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="03025-261">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="03025-262">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="03025-262">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="03025-263">Квалификаторы: [**маппингстрингс**](/windows/desktop/WmiSdk/standard-qualifiers) (" \| структуры служб Win32API \| [**запрос \_ \_ конфигурации**](/windows/desktop/api/winsvc/ns-winsvc-query_service_configa) \| Лпбинарипаснаме"), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("имя пути к файлу")</span><span class="sxs-lookup"><span data-stu-id="03025-263">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32API\|Service Structures\|[**QUERY\_SERVICE\_CONFIG**](/windows/desktop/api/winsvc/ns-winsvc-query_service_configa)\|lpBinaryPathName"), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("File Path Name")</span></span>
</dt> </dl>

<span data-ttu-id="03025-264">Полный путь к двоичному файлу службы, реализующему службу.</span><span class="sxs-lookup"><span data-stu-id="03025-264">Fully qualified path to the service binary file that implements the service.</span></span>

<span data-ttu-id="03025-265">Пример: " \\ СистемныйКорневойКаталог \\ system32 \\ Drivers \\afd.sys"</span><span class="sxs-lookup"><span data-stu-id="03025-265">Example: "\\SystemRoot\\System32\\drivers\\afd.sys"</span></span>

<span data-ttu-id="03025-266">Это свойство наследуется из [**Win32 \_ басесервице**](/windows/desktop/CIMWin32Prov/win32-baseservice).</span><span class="sxs-lookup"><span data-stu-id="03025-266">This property is inherited from [**Win32\_BaseService**](/windows/desktop/CIMWin32Prov/win32-baseservice).</span></span>

</dd> <dt>

<span data-ttu-id="03025-267">**Идентификатор**</span><span class="sxs-lookup"><span data-stu-id="03025-267">**ProcessId**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="03025-268">Тип данных: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="03025-268">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="03025-269">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="03025-269">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="03025-270">Квалификаторы: [**маппингстрингс**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32API \| Service Structures \| [**\_ Status \_ Process**](/windows/desktop/api/winsvc/ns-winsvc-service_status_process) \| двпроцессид"), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("идентификатор процесса")</span><span class="sxs-lookup"><span data-stu-id="03025-270">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32API\|Service Structures\|[**SERVICE\_STATUS\_PROCESS**](/windows/desktop/api/winsvc/ns-winsvc-service_status_process)\|dwProcessId"), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Process Id")</span></span>
</dt> </dl>

<span data-ttu-id="03025-271">Идентификатор процесса службы.</span><span class="sxs-lookup"><span data-stu-id="03025-271">Process identifier of the service.</span></span>

<span data-ttu-id="03025-272">Пример: 324</span><span class="sxs-lookup"><span data-stu-id="03025-272">Example: 324</span></span>

<span data-ttu-id="03025-273">Это свойство наследуется [**от \_ службы Win32**](/windows/desktop/CIMWin32Prov/win32-service).</span><span class="sxs-lookup"><span data-stu-id="03025-273">This property is inherited from [**Win32\_Service**](/windows/desktop/CIMWin32Prov/win32-service).</span></span>

</dd> <dt>

<span data-ttu-id="03025-274">**сервицеспеЦифицекситкоде**</span><span class="sxs-lookup"><span data-stu-id="03025-274">**ServiceSpecificExitCode**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="03025-275">Тип данных: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="03025-275">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="03025-276">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="03025-276">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="03025-277">Квалификаторы: [**маппингстрингс**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32API \| Service Structures \| [**\_ Status**](/windows/desktop/api/winsvc/ns-winsvc-service_status) \| двсервицеспеЦифицекситкоде"), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("специфический для сервера код выхода")</span><span class="sxs-lookup"><span data-stu-id="03025-277">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32API\|Service Structures\|[**SERVICE\_STATUS**](/windows/desktop/api/winsvc/ns-winsvc-service_status)\|dwServiceSpecificExitCode"), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Server Specific Exit Code")</span></span>
</dt> </dl>

<span data-ttu-id="03025-278">Код ошибки, зависящей от службы, для ошибок, возникающих во время запуска или остановки службы.</span><span class="sxs-lookup"><span data-stu-id="03025-278">Service-specific error code for errors that occur while the service is either starting or stopping.</span></span> <span data-ttu-id="03025-279">Коды выхода определяются службой, представленной этим классом.</span><span class="sxs-lookup"><span data-stu-id="03025-279">The exit codes are defined by the service represented by this class.</span></span> <span data-ttu-id="03025-280">Это значение задается только в том случае, если значение свойства [**ExitCode**](/windows/desktop/CIMWin32Prov/win32-service) — ошибка, связанная со **\_ службой ошибок \_ \_** (1066).</span><span class="sxs-lookup"><span data-stu-id="03025-280">This value is only set when the [**ExitCode**](/windows/desktop/CIMWin32Prov/win32-service) property value is **ERROR\_SERVICE\_SPECIFIC\_ERROR** (1066).</span></span>

<span data-ttu-id="03025-281">Это свойство наследуется из [**Win32 \_ басесервице**](/windows/desktop/CIMWin32Prov/win32-baseservice).</span><span class="sxs-lookup"><span data-stu-id="03025-281">This property is inherited from [**Win32\_BaseService**](/windows/desktop/CIMWin32Prov/win32-baseservice).</span></span>

</dd> <dt>

<span data-ttu-id="03025-282">**ServiceType**</span><span class="sxs-lookup"><span data-stu-id="03025-282">**ServiceType**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="03025-283">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="03025-283">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="03025-284">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="03025-284">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="03025-285">Квалификаторы: [**маппингстрингс**](/windows/desktop/WmiSdk/standard-qualifiers) (" \| структуры служб Win32API \| [**запрос \_ \_ конфигурации службы**](/windows/desktop/api/winsvc/ns-winsvc-query_service_configa) \| двсервицетипе"), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("тип службы")</span><span class="sxs-lookup"><span data-stu-id="03025-285">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32API\|Service Structures\|[**QUERY\_SERVICE\_CONFIG**](/windows/desktop/api/winsvc/ns-winsvc-query_service_configa)\|dwServiceType"), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Service Type")</span></span>
</dt> </dl>

<span data-ttu-id="03025-286">Тип службы, предоставленной для вызывающих процессов.</span><span class="sxs-lookup"><span data-stu-id="03025-286">Type of service provided to calling processes.</span></span>

<span data-ttu-id="03025-287">Значения качества производительности:</span><span class="sxs-lookup"><span data-stu-id="03025-287">The values are:</span></span>

<dt>

<span id="Kernel_Driver"></span><span id="kernel_driver"></span><span id="KERNEL_DRIVER"></span>

<span data-ttu-id="03025-288">**Драйвер ядра** ("драйвер ядра")</span><span class="sxs-lookup"><span data-stu-id="03025-288">**Kernel Driver** ("Kernel Driver")</span></span>


</dt> <dd></dd> <dt>

<span id="File_System_Driver"></span><span id="file_system_driver"></span><span id="FILE_SYSTEM_DRIVER"></span>

<span data-ttu-id="03025-289">**Драйвер файловой системы** ("драйвер файловой системы")</span><span class="sxs-lookup"><span data-stu-id="03025-289">**File System Driver** ("File System Driver")</span></span>


</dt> <dd></dd> <dt>

<span id="Adapter"></span><span id="adapter"></span><span id="ADAPTER"></span>

<span data-ttu-id="03025-290">**Адаптер** ("адаптер")</span><span class="sxs-lookup"><span data-stu-id="03025-290">**Adapter** ("Adapter")</span></span>


</dt> <dd></dd> <dt>

<span id="Recognizer_Driver"></span><span id="recognizer_driver"></span><span id="RECOGNIZER_DRIVER"></span>

<span data-ttu-id="03025-291">**Драйвер распознавателя** ("драйвер распознавателя")</span><span class="sxs-lookup"><span data-stu-id="03025-291">**Recognizer Driver** ("Recognizer Driver")</span></span>


</dt> <dd></dd> <dt>

<span id="Own_Process"></span><span id="own_process"></span><span id="OWN_PROCESS"></span>

<span data-ttu-id="03025-292">**Собственный процесс** ("собственный процесс")</span><span class="sxs-lookup"><span data-stu-id="03025-292">**Own Process** ("Own Process")</span></span>


</dt> <dd></dd> <dt>

<span id="Share_Process"></span><span id="share_process"></span><span id="SHARE_PROCESS"></span>

<span data-ttu-id="03025-293">**Общий процесс** ("общий процесс")</span><span class="sxs-lookup"><span data-stu-id="03025-293">**Share Process** ("Share Process")</span></span>


</dt> <dd></dd> <dt>

<span id="Interactive_Process"></span><span id="interactive_process"></span><span id="INTERACTIVE_PROCESS"></span>

<span data-ttu-id="03025-294">**Интерактивный процесс** (интерактивный процесс)</span><span class="sxs-lookup"><span data-stu-id="03025-294">**Interactive Process** ("Interactive Process")</span></span>


<span data-ttu-id="03025-295"></dt> <dd></dd> </dl></span><span class="sxs-lookup"><span data-stu-id="03025-295"></dt> <dd></dd> </dl></span></span>

<span data-ttu-id="03025-296">Это свойство наследуется из [**Win32 \_ басесервице**](/windows/desktop/CIMWin32Prov/win32-baseservice).</span><span class="sxs-lookup"><span data-stu-id="03025-296">This property is inherited from [**Win32\_BaseService**](/windows/desktop/CIMWin32Prov/win32-baseservice).</span></span>

</dd> <dt>

<span data-ttu-id="03025-297">**Запуск**</span><span class="sxs-lookup"><span data-stu-id="03025-297">**Started**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="03025-298">Тип данных: **логический**</span><span class="sxs-lookup"><span data-stu-id="03025-298">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="03025-299">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="03025-299">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="03025-300">Квалификаторы: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("запущено")</span><span class="sxs-lookup"><span data-stu-id="03025-300">Qualifiers: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Started")</span></span>
</dt> </dl>

<span data-ttu-id="03025-301">Указывает, запущена ли служба.</span><span class="sxs-lookup"><span data-stu-id="03025-301">Indicates whether or not the service is started.</span></span>

<span data-ttu-id="03025-302">Это свойство наследуется [**от \_ службы CIM**](/windows/desktop/CIMWin32Prov/cim-service).</span><span class="sxs-lookup"><span data-stu-id="03025-302">This property is inherited from [**CIM\_Service**](/windows/desktop/CIMWin32Prov/cim-service).</span></span>

</dd> <dt>

<span data-ttu-id="03025-303">**StartMode**</span><span class="sxs-lookup"><span data-stu-id="03025-303">**StartMode**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="03025-304">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="03025-304">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="03025-305">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="03025-305">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="03025-306">Квалификаторы: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("режим запуска")</span><span class="sxs-lookup"><span data-stu-id="03025-306">Qualifiers: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Start Mode")</span></span>
</dt> </dl>

<span data-ttu-id="03025-307">Режим запуска базовой службы Windows.</span><span class="sxs-lookup"><span data-stu-id="03025-307">Start mode of the Windows base service.</span></span>

<dt>

<span id="Boot"></span><span id="boot"></span><span id="BOOT"></span>

<span data-ttu-id="03025-308"><span id="Boot"></span><span id="boot"></span><span id="BOOT"></span>**Boot** (Загрузка)</span><span class="sxs-lookup"><span data-stu-id="03025-308"><span id="Boot"></span><span id="boot"></span><span id="BOOT"></span>**Boot** ("Boot")</span></span>


</dt> <dd>

<span data-ttu-id="03025-309">Драйвер устройства запущен загрузчиком операционной системы (действует только для служб драйверов).</span><span class="sxs-lookup"><span data-stu-id="03025-309">Device driver started by the operating system loader (valid only for driver services).</span></span>

</dd> <dt>

<span id="System"></span><span id="system"></span><span id="SYSTEM"></span>

<span data-ttu-id="03025-310"><span id="System"></span><span id="system"></span><span id="SYSTEM"></span>**Система** ("System")</span><span class="sxs-lookup"><span data-stu-id="03025-310"><span id="System"></span><span id="system"></span><span id="SYSTEM"></span>**System** ("System")</span></span>


</dt> <dd>

<span data-ttu-id="03025-311">Драйвер устройства запущен процессом инициализации операционной системы.</span><span class="sxs-lookup"><span data-stu-id="03025-311">Device driver started by the operating system initialization process.</span></span> <span data-ttu-id="03025-312">Это значение допустимо только для служб драйверов.</span><span class="sxs-lookup"><span data-stu-id="03025-312">This value is valid only for driver services.</span></span>

</dd> <dt>

<span id="Auto"></span><span id="auto"></span><span id="AUTO"></span>

<span data-ttu-id="03025-313"><span id="Auto"></span><span id="auto"></span><span id="AUTO"></span>**Авто** ("Auto")</span><span class="sxs-lookup"><span data-stu-id="03025-313"><span id="Auto"></span><span id="auto"></span><span id="AUTO"></span>**Auto** ("Auto")</span></span>


</dt> <dd>

<span data-ttu-id="03025-314">Служба запускается автоматически диспетчером управления службами во время запуска системы.</span><span class="sxs-lookup"><span data-stu-id="03025-314">Service to be started automatically by the service control manager during system startup.</span></span> <span data-ttu-id="03025-315">Автоматические службы запускаются, даже если пользователь не входит в систему.</span><span class="sxs-lookup"><span data-stu-id="03025-315">Auto services are started even if a user does not log on.</span></span>

</dd> <dt>

<span id="Manual"></span><span id="manual"></span><span id="MANUAL"></span>

<span data-ttu-id="03025-316"><span id="Manual"></span><span id="manual"></span><span id="MANUAL"></span>**Вручную** ("вручную")</span><span class="sxs-lookup"><span data-stu-id="03025-316"><span id="Manual"></span><span id="manual"></span><span id="MANUAL"></span>**Manual** ("Manual")</span></span>


</dt> <dd>

<span data-ttu-id="03025-317">Служба, запускаемая диспетчером управления службами, когда процесс вызывает метод [**StartService**](/windows/desktop/CIMWin32Prov/startservice-method-in-class-win32-service) .</span><span class="sxs-lookup"><span data-stu-id="03025-317">Service to be started by the Service Control Manager when a process calls the [**StartService**](/windows/desktop/CIMWin32Prov/startservice-method-in-class-win32-service) method.</span></span> <span data-ttu-id="03025-318">Эти службы не запускаются, пока пользователь не войдет в систему и не запустит их.</span><span class="sxs-lookup"><span data-stu-id="03025-318">These services do not start unless a user logs on and starts them.</span></span>

</dd> <dt>

<span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>

<span data-ttu-id="03025-319"><span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>**Отключено** ("отключено")</span><span class="sxs-lookup"><span data-stu-id="03025-319"><span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>**Disabled** ("Disabled")</span></span>


</dt> <dd>

<span data-ttu-id="03025-320">Служба, которая не может быть запущена до тех пор, пока ее значение StartMode не изменится на Auto или Manual.</span><span class="sxs-lookup"><span data-stu-id="03025-320">Service that cannot be started until its StartMode is changed to either Auto or Manual.</span></span>

</dd> </dl>

<span data-ttu-id="03025-321">Это свойство наследуется [**от \_ службы CIM**](/windows/desktop/CIMWin32Prov/cim-service).</span><span class="sxs-lookup"><span data-stu-id="03025-321">This property is inherited from [**CIM\_Service**](/windows/desktop/CIMWin32Prov/cim-service).</span></span>

</dd> <dt>

<span data-ttu-id="03025-322">**StartName**</span><span class="sxs-lookup"><span data-stu-id="03025-322">**StartName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="03025-323">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="03025-323">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="03025-324">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="03025-324">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="03025-325">Квалификаторы: [**маппингстрингс**](/windows/desktop/WmiSdk/standard-qualifiers) (" \| структуры служб Win32API \| [**запрос \_ \_ конфигурации службы**](/windows/desktop/api/winsvc/ns-winsvc-query_service_configa) \| Лпсервицестартнаме"), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("начальное имя учетной записи")</span><span class="sxs-lookup"><span data-stu-id="03025-325">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32API\|Service Structures\|[**QUERY\_SERVICE\_CONFIG**](/windows/desktop/api/winsvc/ns-winsvc-query_service_configa)\|lpServiceStartName"), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Starting Account Name")</span></span>
</dt> </dl>

<span data-ttu-id="03025-326">Имя учетной записи, под которой выполняется служба.</span><span class="sxs-lookup"><span data-stu-id="03025-326">Account name under which a service runs.</span></span> <span data-ttu-id="03025-327">В зависимости от типа службы имя учетной записи может быть указано в \\ формате имя_домена имя пользователя или имя участника-пользователя (" *Username@DomainName* ").</span><span class="sxs-lookup"><span data-stu-id="03025-327">Depending on the service type, the account name may be in the form of "DomainName\\Username" or UPN format ("*Username@DomainName*").</span></span> <span data-ttu-id="03025-328">Процесс службы заносится в журнал с использованием одной из этих двух форм при запуске.</span><span class="sxs-lookup"><span data-stu-id="03025-328">The service process is logged by using one of these two forms when it runs.</span></span> <span data-ttu-id="03025-329">Если учетная запись принадлежит к встроенному домену, то ". \\ Можно указать имя пользователя.</span><span class="sxs-lookup"><span data-stu-id="03025-329">If the account belongs to the built-in domain, then ".\\Username" can be specified.</span></span> <span data-ttu-id="03025-330">Для драйверов ядра или системного уровня [**StartName**](/windows/desktop/CIMWin32Prov/win32-service) содержит имя объекта драйвера (то есть " \\ FileSystem \\ RDR" или " \\ Driver \\ КСНС"), которое система ввода-вывода использует для загрузки драйвера устройства.</span><span class="sxs-lookup"><span data-stu-id="03025-330">For kernel or system-level drivers, [**StartName**](/windows/desktop/CIMWin32Prov/win32-service) contains the driver object name (that is, "\\FileSystem\\Rdr" or "\\Driver\\Xns") which the I/O system uses to load the device driver.</span></span> <span data-ttu-id="03025-331">Кроме того, если указано **значение NULL** , драйвер запускается с именем объекта по умолчанию, созданным системой ввода-вывода на основе имени службы.</span><span class="sxs-lookup"><span data-stu-id="03025-331">Additionally, if **NULL** is specified, the driver runs with a default object name created by the I/O system based on the service name.</span></span>

<span data-ttu-id="03025-332">Пример: "ДВДОМ \\ Admin"</span><span class="sxs-lookup"><span data-stu-id="03025-332">Example: "DWDOM\\Admin"</span></span>

<span data-ttu-id="03025-333">Это свойство наследуется из [**Win32 \_ басесервице**](/windows/desktop/CIMWin32Prov/win32-baseservice).</span><span class="sxs-lookup"><span data-stu-id="03025-333">This property is inherited from [**Win32\_BaseService**](/windows/desktop/CIMWin32Prov/win32-baseservice).</span></span>

</dd> <dt>

<span data-ttu-id="03025-334">**Состояние**</span><span class="sxs-lookup"><span data-stu-id="03025-334">**State**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="03025-335">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="03025-335">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="03025-336">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="03025-336">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="03025-337">Квалификаторы: [**маппингстрингс**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32API \| Service Structures \| [**\_ Status**](/windows/desktop/api/winsvc/ns-winsvc-service_status) \| двкуррентстате"), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("State")</span><span class="sxs-lookup"><span data-stu-id="03025-337">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32API\|Service Structures\|[**SERVICE\_STATUS**](/windows/desktop/api/winsvc/ns-winsvc-service_status)\|dwCurrentState "), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("State")</span></span>
</dt> </dl>

<span data-ttu-id="03025-338">Текущее состояние базовой службы.</span><span class="sxs-lookup"><span data-stu-id="03025-338">Current state of the base service.</span></span>

<span data-ttu-id="03025-339">Значения качества производительности:</span><span class="sxs-lookup"><span data-stu-id="03025-339">The values are:</span></span>

<dt>

<span id="Stopped"></span><span id="stopped"></span><span id="STOPPED"></span>

<span data-ttu-id="03025-340">**Остановлено** ("остановлено")</span><span class="sxs-lookup"><span data-stu-id="03025-340">**Stopped** ("Stopped")</span></span>


</dt> <dd></dd> <dt>

<span id="Start_Pending"></span><span id="start_pending"></span><span id="START_PENDING"></span>

<span data-ttu-id="03025-341">**Ожидание запуска** ("Ожидание запуска")</span><span class="sxs-lookup"><span data-stu-id="03025-341">**Start Pending** ("Start Pending")</span></span>


</dt> <dd></dd> <dt>

<span id="Stop_Pending"></span><span id="stop_pending"></span><span id="STOP_PENDING"></span>

<span data-ttu-id="03025-342">**Ожидание ожидания** ("ожидание завершения")</span><span class="sxs-lookup"><span data-stu-id="03025-342">**Stop Pending** ("Stop Pending")</span></span>


</dt> <dd></dd> <dt>

<span id="Running"></span><span id="running"></span><span id="RUNNING"></span>

<span data-ttu-id="03025-343">**Работает** ("работает")</span><span class="sxs-lookup"><span data-stu-id="03025-343">**Running** ("Running")</span></span>


</dt> <dd></dd> <dt>

<span id="Continue_Pending"></span><span id="continue_pending"></span><span id="CONTINUE_PENDING"></span>

<span data-ttu-id="03025-344">**Ожидание продолжения** ("Ожидание продолжения")</span><span class="sxs-lookup"><span data-stu-id="03025-344">**Continue Pending** ("Continue Pending")</span></span>


</dt> <dd></dd> <dt>

<span id="Pause_Pending"></span><span id="pause_pending"></span><span id="PAUSE_PENDING"></span>

<span data-ttu-id="03025-345">**Ожидание приостановки** ("ожидание приостановки")</span><span class="sxs-lookup"><span data-stu-id="03025-345">**Pause Pending** ("Pause Pending")</span></span>


</dt> <dd></dd> <dt>

<span id="Paused"></span><span id="paused"></span><span id="PAUSED"></span>

<span data-ttu-id="03025-346">**Приостановлено** ("приостановлено")</span><span class="sxs-lookup"><span data-stu-id="03025-346">**Paused** ("Paused")</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="03025-347">**Неизвестно** ("неизвестно")</span><span class="sxs-lookup"><span data-stu-id="03025-347">**Unknown** ("Unknown")</span></span>


<span data-ttu-id="03025-348"></dt> <dd></dd> </dl></span><span class="sxs-lookup"><span data-stu-id="03025-348"></dt> <dd></dd> </dl></span></span>

<span data-ttu-id="03025-349">**Windows Server 2008 и Windows Vista:** Это свойство доступно только для чтения до Windows 7 и Windows Server 2008 R2.</span><span class="sxs-lookup"><span data-stu-id="03025-349">**Windows Server 2008 and Windows Vista:** This property is read-only before Windows 7 and Windows Server 2008 R2.</span></span>

<span data-ttu-id="03025-350">Это свойство наследуется из [**Win32 \_ басесервице**](/windows/desktop/CIMWin32Prov/win32-baseservice).</span><span class="sxs-lookup"><span data-stu-id="03025-350">This property is inherited from [**Win32\_BaseService**](/windows/desktop/CIMWin32Prov/win32-baseservice).</span></span>

</dd> <dt>

<span data-ttu-id="03025-351">**Состояние**</span><span class="sxs-lookup"><span data-stu-id="03025-351">**Status**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="03025-352">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="03025-352">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="03025-353">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="03025-353">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="03025-354">Квалификаторы: [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (10), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("состояние")</span><span class="sxs-lookup"><span data-stu-id="03025-354">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (10), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Status")</span></span>
</dt> </dl>

<span data-ttu-id="03025-355">Текущее состояние объекта.</span><span class="sxs-lookup"><span data-stu-id="03025-355">Current status of the object.</span></span> <span data-ttu-id="03025-356">Можно определить различные операционные и неоперационные состояния.</span><span class="sxs-lookup"><span data-stu-id="03025-356">Various operational and nonoperational statuses can be defined.</span></span> <span data-ttu-id="03025-357">Рабочие состояния включают: "ОК", "деградация" и "пред-ошибка" (элемент, например жесткий диск с поддержкой SMART, может работать правильно, но прогнозировать сбой в ближайшем будущем).</span><span class="sxs-lookup"><span data-stu-id="03025-357">Operational statuses include: "OK", "Degraded", and "Pred Fail" (an element, such as a SMART-enabled hard disk drive, may be functioning properly but predicting a failure in the near future).</span></span> <span data-ttu-id="03025-358">Неработающие состояния включают: "ошибка", "Запуск", "остановка" и "служба".</span><span class="sxs-lookup"><span data-stu-id="03025-358">Nonoperational statuses include: "Error", "Starting", "Stopping", and "Service".</span></span> <span data-ttu-id="03025-359">Последняя, «служба», может применяться во время зеркального копирования диска, перезагрузки списка разрешений пользователя или другой административной работы.</span><span class="sxs-lookup"><span data-stu-id="03025-359">The latter, "Service", could apply during mirror-resilvering of a disk, reload of a user permissions list, or other administrative work.</span></span> <span data-ttu-id="03025-360">Не вся такая работа находится в оперативном режиме, но управляемый элемент не является ни "ОК", ни одним из других состояний.</span><span class="sxs-lookup"><span data-stu-id="03025-360">Not all such work is online, yet the managed element is neither "OK" nor in one of the other states.</span></span>

<span data-ttu-id="03025-361">Значения качества производительности:</span><span class="sxs-lookup"><span data-stu-id="03025-361">The values are:</span></span>

<dt>

<span id="OK"></span><span id="ok"></span>

<span data-ttu-id="03025-362">**ОК** ("ОК")</span><span class="sxs-lookup"><span data-stu-id="03025-362">**OK** ("OK")</span></span>


</dt> <dd></dd> <dt>

<span id="Error"></span><span id="error"></span><span id="ERROR"></span>

<span data-ttu-id="03025-363">**Ошибка** ("ошибка")</span><span class="sxs-lookup"><span data-stu-id="03025-363">**Error** ("Error")</span></span>


</dt> <dd></dd> <dt>

<span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>

<span data-ttu-id="03025-364">**Пониженная работоспособность** (пониженная работоспособность)</span><span class="sxs-lookup"><span data-stu-id="03025-364">**Degraded** ("Degraded")</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="03025-365">**Неизвестно** ("неизвестно")</span><span class="sxs-lookup"><span data-stu-id="03025-365">**Unknown** ("Unknown")</span></span>


</dt> <dd></dd> <dt>

<span id="Pred_Fail"></span><span id="pred_fail"></span><span id="PRED_FAIL"></span>

<span data-ttu-id="03025-366">**Пред-ошибка** ("пред Fail")</span><span class="sxs-lookup"><span data-stu-id="03025-366">**Pred Fail** ("Pred Fail")</span></span>


</dt> <dd></dd> <dt>

<span id="Starting"></span><span id="starting"></span><span id="STARTING"></span>

<span data-ttu-id="03025-367">**Запуск** ("Запуск")</span><span class="sxs-lookup"><span data-stu-id="03025-367">**Starting** ("Starting")</span></span>


</dt> <dd></dd> <dt>

<span id="Stopping"></span><span id="stopping"></span><span id="STOPPING"></span>

<span data-ttu-id="03025-368">**Остановка** ("остановка")</span><span class="sxs-lookup"><span data-stu-id="03025-368">**Stopping** ("Stopping")</span></span>


</dt> <dd></dd> <dt>

<span id="Service"></span><span id="service"></span><span id="SERVICE"></span>

<span data-ttu-id="03025-369">**Служба** ("служба")</span><span class="sxs-lookup"><span data-stu-id="03025-369">**Service** ("Service")</span></span>


</dt> <dd></dd> <dt>

<span id="Stressed"></span><span id="stressed"></span><span id="STRESSED"></span>

<span data-ttu-id="03025-370">**Пренапряжению** ("напряжению")</span><span class="sxs-lookup"><span data-stu-id="03025-370">**Stressed** ("Stressed")</span></span>


</dt> <dd></dd> <dt>

<span id="NonRecover"></span><span id="nonrecover"></span><span id="NONRECOVER"></span>

<span data-ttu-id="03025-371">**Невосстановление** ("невосстановление")</span><span class="sxs-lookup"><span data-stu-id="03025-371">**NonRecover** ("NonRecover")</span></span>


</dt> <dd></dd> <dt>

<span id="No_Contact"></span><span id="no_contact"></span><span id="NO_CONTACT"></span>

<span data-ttu-id="03025-372">**Нет контакта** ("нет контакта")</span><span class="sxs-lookup"><span data-stu-id="03025-372">**No Contact** ("No Contact")</span></span>


</dt> <dd></dd> <dt>

<span id="Lost_Comm"></span><span id="lost_comm"></span><span id="LOST_COMM"></span>

<span data-ttu-id="03025-373">**Потеря** связи ("потеря связи")</span><span class="sxs-lookup"><span data-stu-id="03025-373">**Lost Comm** ("Lost Comm")</span></span>


<span data-ttu-id="03025-374"></dt> <dd></dd> </dl></span><span class="sxs-lookup"><span data-stu-id="03025-374"></dt> <dd></dd> </dl></span></span>

<span data-ttu-id="03025-375">Это свойство наследуется от [**CIM \_ манажедсистемелемент**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span><span class="sxs-lookup"><span data-stu-id="03025-375">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

</dd> <dt>

<span data-ttu-id="03025-376">**системкреатионкласснаме**</span><span class="sxs-lookup"><span data-stu-id="03025-376">**SystemCreationClassName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="03025-377">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="03025-377">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="03025-378">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="03025-378">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="03025-379">Квалификаторы: [**распространено**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**\_ система CIM**](/windows/desktop/CIMWin32Prov/cim-system). CreationClassName "), [**\_ ключ CIM**](/windows/desktop/WmiSdk/standard-wmi-qualifiers), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) (" имя класса системы ")</span><span class="sxs-lookup"><span data-stu-id="03025-379">Qualifiers: [**Propagated**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM\_System**](/windows/desktop/CIMWin32Prov/cim-system).CreationClassName"), [**CIM\_Key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("System Class Name")</span></span>
</dt> </dl>

<span data-ttu-id="03025-380">Имя типа системы, в которой размещена эта служба.</span><span class="sxs-lookup"><span data-stu-id="03025-380">Type name of the system that hosts this service.</span></span>

<span data-ttu-id="03025-381">Это свойство наследуется [**от \_ службы CIM**](/windows/desktop/CIMWin32Prov/cim-service).</span><span class="sxs-lookup"><span data-stu-id="03025-381">This property is inherited from [**CIM\_Service**](/windows/desktop/CIMWin32Prov/cim-service).</span></span>

</dd> <dt>

<span data-ttu-id="03025-382">**SystemName**</span><span class="sxs-lookup"><span data-stu-id="03025-382">**SystemName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="03025-383">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="03025-383">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="03025-384">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="03025-384">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="03025-385">Квалификаторы: [**распространено**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**\_ система CIM**](/windows/desktop/CIMWin32Prov/cim-system). Name "), [**\_ ключ CIM**](/windows/desktop/WmiSdk/standard-wmi-qualifiers), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) (" System Name ")</span><span class="sxs-lookup"><span data-stu-id="03025-385">Qualifiers: [**Propagated**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM\_System**](/windows/desktop/CIMWin32Prov/cim-system).Name"), [**CIM\_Key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("System Name")</span></span>
</dt> </dl>

<span data-ttu-id="03025-386">Имя системы, в которой размещена эта служба.</span><span class="sxs-lookup"><span data-stu-id="03025-386">Name of the system that hosts this service.</span></span>

<span data-ttu-id="03025-387">Это свойство наследуется [**от \_ службы CIM**](/windows/desktop/CIMWin32Prov/cim-service).</span><span class="sxs-lookup"><span data-stu-id="03025-387">This property is inherited from [**CIM\_Service**](/windows/desktop/CIMWin32Prov/cim-service).</span></span>

</dd> <dt>

<span data-ttu-id="03025-388">**TagId**</span><span class="sxs-lookup"><span data-stu-id="03025-388">**TagId**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="03025-389">Тип данных: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="03025-389">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="03025-390">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="03025-390">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="03025-391">Квалификаторы: [**маппингстрингс**](/windows/desktop/WmiSdk/standard-qualifiers) (" \| структуры служб Win32API \| [**запрос \_ \_ конфигурации**](/windows/desktop/api/winsvc/ns-winsvc-query_service_configa) \| двтагид"), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("идентификатор тега")</span><span class="sxs-lookup"><span data-stu-id="03025-391">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32API\|Service Structures\|[**QUERY\_SERVICE\_CONFIG**](/windows/desktop/api/winsvc/ns-winsvc-query_service_configa)\|dwTagId"), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Tag Id")</span></span>
</dt> </dl>

<span data-ttu-id="03025-392">Уникальное значение тега для этой службы в группе.</span><span class="sxs-lookup"><span data-stu-id="03025-392">Unique tag value for this service in the group.</span></span> <span data-ttu-id="03025-393">Значение 0 (ноль) указывает, что у службы нет тега.</span><span class="sxs-lookup"><span data-stu-id="03025-393">A value of 0 (zero) indicates that the service does not have a tag.</span></span> <span data-ttu-id="03025-394">Тег можно использовать для упорядочивания запуска службы в группе порядка загрузки, указывая в реестре вектор порядка тегов в папке:</span><span class="sxs-lookup"><span data-stu-id="03025-394">A tag can be used to order service startup within a load order group by specifying a tag order vector in the registry located at:</span></span>

<span data-ttu-id="03025-395">**HKey \_ \_** \\  \\  \\  \\ **Граупордерлист** управления CurrentControlSet системы локального компьютера    </span><span class="sxs-lookup"><span data-stu-id="03025-395">**HKEY\_LOCAL\_MACHINE**\\**System**\\**CurrentControlSet**\\**Control**\\    **GroupOrderList**</span></span>

<span data-ttu-id="03025-396">Теги оцениваются только для служб типа "драйвер ядра" и "драйвер файловой системы", которые имеют режимы загрузки или запуска системы.</span><span class="sxs-lookup"><span data-stu-id="03025-396">Tags are only evaluated for Kernel Driver and File System Driver start type services that have Boot or System start modes.</span></span>

<span data-ttu-id="03025-397">Это свойство наследуется из [**Win32 \_ басесервице**](/windows/desktop/CIMWin32Prov/win32-baseservice).</span><span class="sxs-lookup"><span data-stu-id="03025-397">This property is inherited from [**Win32\_BaseService**](/windows/desktop/CIMWin32Prov/win32-baseservice).</span></span>

</dd> <dt>

<span data-ttu-id="03025-398">**тоталсессионс**</span><span class="sxs-lookup"><span data-stu-id="03025-398">**TotalSessions**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="03025-399">Тип данных: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="03025-399">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="03025-400">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="03025-400">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="03025-401">Общее число сеансов на текущем сервере.</span><span class="sxs-lookup"><span data-stu-id="03025-401">The total number of sessions on the current server.</span></span> <span data-ttu-id="03025-402">Сюда входят подключенные и отключенные сеансы.</span><span class="sxs-lookup"><span data-stu-id="03025-402">This includes both connected and disconnected sessions.</span></span>

</dd> <dt>

<span data-ttu-id="03025-403">**ваисинт**</span><span class="sxs-lookup"><span data-stu-id="03025-403">**WaitHint**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="03025-404">Тип данных: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="03025-404">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="03025-405">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="03025-405">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="03025-406">Квалификаторы: [**маппингстрингс**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32API \| Service Structures \| [**\_ Status**](/windows/desktop/api/winsvc/ns-winsvc-service_status) \| двваисинт"), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("предполагаемое время ожидания")</span><span class="sxs-lookup"><span data-stu-id="03025-406">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32API\|Service Structures\|[**SERVICE\_STATUS**](/windows/desktop/api/winsvc/ns-winsvc-service_status)\|dwWaitHint"), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Estimated Wait Time")</span></span>
</dt> </dl>

<span data-ttu-id="03025-407">Предполагаемое время в миллисекундах для ожидающей операции запуска, остановки, приостановки или продолжения работы.</span><span class="sxs-lookup"><span data-stu-id="03025-407">Estimated time required, in milliseconds, for a pending start, stop, pause, or continue operation.</span></span> <span data-ttu-id="03025-408">По истечении указанного времени служба выполняет следующий вызов метода **сбой SetServiceStatus** с увеличенным значением [**контрольной точки**](/windows/desktop/CIMWin32Prov/win32-service) или изменением в **CurrentState**.</span><span class="sxs-lookup"><span data-stu-id="03025-408">After the specified time has elapsed, the service makes its next call to the **SetServiceStatus** method with either an incremented [**CheckPoint**](/windows/desktop/CIMWin32Prov/win32-service) value or a change in **CurrentState**.</span></span> <span data-ttu-id="03025-409">Если время, указанное в **ваисинт** , прошло, а **контрольная точка** не была увеличена или **CurrentState** не изменилась, диспетчер управления службами или программа управления службами предполагает, что произошла ошибка.</span><span class="sxs-lookup"><span data-stu-id="03025-409">If the amount of time specified by **WaitHint** passes, and **CheckPoint** has not been incremented, or **CurrentState** has not changed, the service control manager or service control program assumes that an error has occurred.</span></span>

<span data-ttu-id="03025-410">Это свойство наследуется [**от \_ службы Win32**](/windows/desktop/CIMWin32Prov/win32-service).</span><span class="sxs-lookup"><span data-stu-id="03025-410">This property is inherited from [**Win32\_Service**](/windows/desktop/CIMWin32Prov/win32-service).</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="03025-411">Комментарии</span><span class="sxs-lookup"><span data-stu-id="03025-411">Remarks</span></span>

<span data-ttu-id="03025-412">Поскольку класс **Win32 \_ терминалсервице** является подклассом класса [**\_ службы Win32**](/windows/desktop/CIMWin32Prov/win32-service) , класс наследует все свойства и методы **\_ службы Win32**.</span><span class="sxs-lookup"><span data-stu-id="03025-412">Since the **Win32\_TerminalService** class is a subclass of the [**Win32\_Service**](/windows/desktop/CIMWin32Prov/win32-service) class, the class inherits all properties and methods of **Win32\_Service**.</span></span>

<span data-ttu-id="03025-413">[**Win32 \_ Терминалсервицесеттинг**](win32-terminalservicesetting.md) связан с **Win32 \_ терминалсервице** в качестве свойства **Setting** ассоциации [**Win32 \_ терминалсервицетосеттинг**](win32-terminalservicetosetting.md) .</span><span class="sxs-lookup"><span data-stu-id="03025-413">[**Win32\_TerminalServiceSetting**](win32-terminalservicesetting.md) is associated to **Win32\_TerminalService** as the **Setting** property of the [**Win32\_TerminalServiceToSetting**](win32-terminalservicetosetting.md) association.</span></span>

<span data-ttu-id="03025-414">[**Win32 \_ Тссессиондиректори**](win32-tssessiondirectory.md) связан с **Win32 \_ терминалсервице** в качестве свойства **Setting** ассоциации [**Win32 \_ тссессиондиректорисеттинг**](win32-tssessiondirectorysetting.md) .</span><span class="sxs-lookup"><span data-stu-id="03025-414">[**Win32\_TSSessionDirectory**](win32-tssessiondirectory.md) is associated to **Win32\_TerminalService** as the **Setting** property of the [**Win32\_TSSessionDirectorySetting**](win32-tssessiondirectorysetting.md) association.</span></span>

<span data-ttu-id="03025-415">Файлы MOF-файл (MOF) содержат определения для классов инструментарий управления Windows (WMI) (WMI).</span><span class="sxs-lookup"><span data-stu-id="03025-415">Managed Object Format (MOF) files contain the definitions for Windows Management Instrumentation (WMI) classes.</span></span> <span data-ttu-id="03025-416">MOF-файлы не устанавливаются в составе пакета средств разработки программного обеспечения Microsoft Windows (SDK).</span><span class="sxs-lookup"><span data-stu-id="03025-416">MOF files are not installed as part of the Microsoft Windows Software Development Kit (SDK).</span></span> <span data-ttu-id="03025-417">Они устанавливаются на сервере при добавлении связанной роли с помощью диспетчер сервера.</span><span class="sxs-lookup"><span data-stu-id="03025-417">They are installed on the server when you add the associated role by using the Server Manager.</span></span> <span data-ttu-id="03025-418">Дополнительные сведения о файлах MOF см. в разделе [MOF-файл (MOF)](/windows/desktop/WmiSdk/managed-object-format--mof-).</span><span class="sxs-lookup"><span data-stu-id="03025-418">For more information about MOF files, see [Managed Object Format (MOF)](/windows/desktop/WmiSdk/managed-object-format--mof-).</span></span>

## <a name="requirements"></a><span data-ttu-id="03025-419">Требования</span><span class="sxs-lookup"><span data-stu-id="03025-419">Requirements</span></span>



| <span data-ttu-id="03025-420">Требование</span><span class="sxs-lookup"><span data-stu-id="03025-420">Requirement</span></span> | <span data-ttu-id="03025-421">Значение</span><span class="sxs-lookup"><span data-stu-id="03025-421">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="03025-422">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="03025-422">Minimum supported client</span></span><br/> | <span data-ttu-id="03025-423">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="03025-423">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="03025-424">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="03025-424">Minimum supported server</span></span><br/> | <span data-ttu-id="03025-425">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="03025-425">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="03025-426">Пространство имен</span><span class="sxs-lookup"><span data-stu-id="03025-426">Namespace</span></span><br/>                | <span data-ttu-id="03025-427">Root\\CIMv2</span><span class="sxs-lookup"><span data-stu-id="03025-427">Root\\CIMv2</span></span><br/>                                                                  |
| <span data-ttu-id="03025-428">MOF</span><span class="sxs-lookup"><span data-stu-id="03025-428">MOF</span></span><br/>                      | <dl> <span data-ttu-id="03025-429"><dt>Тскфгвми. mof</dt></span><span class="sxs-lookup"><span data-stu-id="03025-429"><dt>TSCfgWmi.mof</dt></span></span> </dl> |
| <span data-ttu-id="03025-430">DLL</span><span class="sxs-lookup"><span data-stu-id="03025-430">DLL</span></span><br/>                      | <dl> <span data-ttu-id="03025-431"><dt>TSCfgWmi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="03025-431"><dt>TSCfgWmi.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="03025-432">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="03025-432">See also</span></span>

<dl> <dt>

[<span data-ttu-id="03025-433">**\_Служба Win32**</span><span class="sxs-lookup"><span data-stu-id="03025-433">**Win32\_Service**</span></span>](/windows/desktop/CIMWin32Prov/win32-service)
</dt> <dt>

[<span data-ttu-id="03025-434">**\_Терминалсервицетосеттинг Win32**</span><span class="sxs-lookup"><span data-stu-id="03025-434">**Win32\_TerminalServiceToSetting**</span></span>](win32-terminalservicetosetting.md)
</dt> <dt>

[<span data-ttu-id="03025-435">**\_Тссессиондиректори Win32**</span><span class="sxs-lookup"><span data-stu-id="03025-435">**Win32\_TSSessionDirectory**</span></span>](win32-tssessiondirectory.md)
</dt> <dt>

[<span data-ttu-id="03025-436">**\_Басесервице Win32**</span><span class="sxs-lookup"><span data-stu-id="03025-436">**Win32\_BaseService**</span></span>](/windows/desktop/CIMWin32Prov/win32-baseservice)
</dt> <dt>

[<span data-ttu-id="03025-437">**\_Служба CIM**</span><span class="sxs-lookup"><span data-stu-id="03025-437">**CIM\_Service**</span></span>](/windows/desktop/CIMWin32Prov/cim-service)
</dt> </dl>

 

