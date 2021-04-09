---
description: Представляет службу в компьютерной системе под Windows.
ms.assetid: 713402d3-ee73-4a6c-afb9-ad8033a4c580
ms.tgt_platform: multiple
title: Класс Win32_Service
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_Service
- Win32_Service.AcceptPause
- Win32_Service.AcceptStop
- Win32_Service.Caption
- Win32_Service.CheckPoint
- Win32_Service.CreationClassName
- Win32_Service.DelayedAutoStart
- Win32_Service.Description
- Win32_Service.DesktopInteract
- Win32_Service.DisplayName
- Win32_Service.ErrorControl
- Win32_Service.ExitCode
- Win32_Service.InstallDate
- Win32_Service.Name
- Win32_Service.PathName
- Win32_Service.ProcessId
- Win32_Service.ServiceSpecificExitCode
- Win32_Service.ServiceType
- Win32_Service.Started
- Win32_Service.StartMode
- Win32_Service.StartName
- Win32_Service.State
- Win32_Service.Status
- Win32_Service.SystemCreationClassName
- Win32_Service.SystemName
- Win32_Service.TagId
- Win32_Service.WaitHint
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: b342282bfa3b49fe72e62cf79377a0ead11276eb
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104072369"
---
# <a name="win32_service-class"></a><span data-ttu-id="1dac9-103">\_Класс службы Win32</span><span class="sxs-lookup"><span data-stu-id="1dac9-103">Win32\_Service class</span></span>

<span data-ttu-id="1dac9-104">[Класс WMI](../wmisdk/retrieving-a-class.md) **\_ службы Win32** представляет службу в компьютерной системе под Windows.</span><span class="sxs-lookup"><span data-stu-id="1dac9-104">The **Win32\_Service** [WMI class](../wmisdk/retrieving-a-class.md) represents a service on a computer system running Windows.</span></span>

<span data-ttu-id="1dac9-105">Следующий пример синтаксиса — упрощенный MOF-код, который включает все наследуемые свойства.</span><span class="sxs-lookup"><span data-stu-id="1dac9-105">The following syntax is simplified from Managed Object Format (MOF) code and includes all of the inherited properties.</span></span> <span data-ttu-id="1dac9-106">Свойства и методы имеют алфавитный порядок, а не порядок MOF.</span><span class="sxs-lookup"><span data-stu-id="1dac9-106">Properties and methods are in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="1dac9-107">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="1dac9-107">Syntax</span></span>

``` syntax
[Dynamic, Provider("CIMWin32"), SupportsUpdate, UUID("{8502C4D9-5FBB-11D2-AAC1-006008C78BC7}"), DisplayName("Services"), AMENDMENT]
class Win32_Service : Win32_BaseService
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
};
```

## <a name="members"></a><span data-ttu-id="1dac9-108">Члены</span><span class="sxs-lookup"><span data-stu-id="1dac9-108">Members</span></span>

<span data-ttu-id="1dac9-109">Класс **\_ службы Win32** имеет следующие типы членов:</span><span class="sxs-lookup"><span data-stu-id="1dac9-109">The **Win32\_Service** class has these types of members:</span></span>

-   [<span data-ttu-id="1dac9-110">Методы</span><span class="sxs-lookup"><span data-stu-id="1dac9-110">Methods</span></span>](#methods)
-   [<span data-ttu-id="1dac9-111">Свойства</span><span class="sxs-lookup"><span data-stu-id="1dac9-111">Properties</span></span>](#properties)

### <a name="methods"></a><span data-ttu-id="1dac9-112">Методы</span><span class="sxs-lookup"><span data-stu-id="1dac9-112">Methods</span></span>

<span data-ttu-id="1dac9-113">В **классе \_ службы Win32** имеются следующие методы.</span><span class="sxs-lookup"><span data-stu-id="1dac9-113">The **Win32\_Service** class has these methods.</span></span>



| <span data-ttu-id="1dac9-114">Метод</span><span class="sxs-lookup"><span data-stu-id="1dac9-114">Method</span></span>                                                                               | <span data-ttu-id="1dac9-115">Описание</span><span class="sxs-lookup"><span data-stu-id="1dac9-115">Description</span></span>                                                                                          |
|:-------------------------------------------------------------------------------------|:-----------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="1dac9-116">**Change**</span><span class="sxs-lookup"><span data-stu-id="1dac9-116">**Change**</span></span>](change-method-in-class-win32-service.md)                               | <span data-ttu-id="1dac9-117">Изменяет службу.</span><span class="sxs-lookup"><span data-stu-id="1dac9-117">Modifies a service.</span></span><br/>                                                                       |
| [<span data-ttu-id="1dac9-118">**чанжестартмоде**</span><span class="sxs-lookup"><span data-stu-id="1dac9-118">**ChangeStartMode**</span></span>](changestartmode-method-in-class-win32-service.md)             | <span data-ttu-id="1dac9-119">Изменяет режим запуска службы.</span><span class="sxs-lookup"><span data-stu-id="1dac9-119">Modifies the start mode of a service.</span></span><br/>                                                     |
| [<span data-ttu-id="1dac9-120">**Создать**</span><span class="sxs-lookup"><span data-stu-id="1dac9-120">**Create**</span></span>](create-method-in-class-win32-service.md)                               | <span data-ttu-id="1dac9-121">Создает новую службу.</span><span class="sxs-lookup"><span data-stu-id="1dac9-121">Creates a new service.</span></span><br/>                                                                    |
| [<span data-ttu-id="1dac9-122">**Удалить**</span><span class="sxs-lookup"><span data-stu-id="1dac9-122">**Delete**</span></span>](delete-method-in-class-win32-service.md)                               | <span data-ttu-id="1dac9-123">Удаляет существующую службу.</span><span class="sxs-lookup"><span data-stu-id="1dac9-123">Deletes an existing service.</span></span><br/>                                                              |
| [<span data-ttu-id="1dac9-124">**жетсекуритидескриптор**</span><span class="sxs-lookup"><span data-stu-id="1dac9-124">**GetSecurityDescriptor**</span></span>](getsecuritydescriptor-method-in-class-win32-service.md) | <span data-ttu-id="1dac9-125">Возвращает дескриптор безопасности, управляющий доступом к службе.</span><span class="sxs-lookup"><span data-stu-id="1dac9-125">Returns the security descriptor that controls access to the service.</span></span><br/>                      |
| [<span data-ttu-id="1dac9-126">**интеррогатесервице**</span><span class="sxs-lookup"><span data-stu-id="1dac9-126">**InterrogateService**</span></span>](interrogateservice-method-in-class-win32-service.md)       | <span data-ttu-id="1dac9-127">Запрашивает обновление состояния службы до Service Manager.</span><span class="sxs-lookup"><span data-stu-id="1dac9-127">Requests that a service update its state to the service manager.</span></span><br/>                          |
| [<span data-ttu-id="1dac9-128">**PauseService**</span><span class="sxs-lookup"><span data-stu-id="1dac9-128">**PauseService**</span></span>](pauseservice-method-in-class-win32-service.md)                   | <span data-ttu-id="1dac9-129">Пытается перевести службу в приостановленное состояние.</span><span class="sxs-lookup"><span data-stu-id="1dac9-129">Attempts to place a service in the paused state.</span></span><br/>                                          |
| [<span data-ttu-id="1dac9-130">**ResumeService**</span><span class="sxs-lookup"><span data-stu-id="1dac9-130">**ResumeService**</span></span>](resumeservice-method-in-class-win32-service.md)                 | <span data-ttu-id="1dac9-131">Пытается перевести службу в состояние возобновления.</span><span class="sxs-lookup"><span data-stu-id="1dac9-131">Attempts to place a service in the resumed state.</span></span><br/>                                         |
| [<span data-ttu-id="1dac9-132">**сетсекуритидескриптор**</span><span class="sxs-lookup"><span data-stu-id="1dac9-132">**SetSecurityDescriptor**</span></span>](setsecuritydescriptor-method-in-class-win32-service.md) | <span data-ttu-id="1dac9-133">Записывает обновленную версию дескриптора безопасности, которая управляет доступом к службе.</span><span class="sxs-lookup"><span data-stu-id="1dac9-133">Writes an updated version of the security descriptor that controls access to the service.</span></span><br/> |
| [<span data-ttu-id="1dac9-134">**StartService**</span><span class="sxs-lookup"><span data-stu-id="1dac9-134">**StartService**</span></span>](startservice-method-in-class-win32-service.md)                   | <span data-ttu-id="1dac9-135">Пытается перевести службу в состояние запуска.</span><span class="sxs-lookup"><span data-stu-id="1dac9-135">Attempts to place a service into the startup state.</span></span><br/>                                       |
| [<span data-ttu-id="1dac9-136">**StopService**</span><span class="sxs-lookup"><span data-stu-id="1dac9-136">**StopService**</span></span>](stopservice-method-in-class-win32-service.md)                     | <span data-ttu-id="1dac9-137">Помещает службу в остановленное состояние.</span><span class="sxs-lookup"><span data-stu-id="1dac9-137">Places a service in the stopped state.</span></span><br/>                                                    |
| [<span data-ttu-id="1dac9-138">**усерконтролсервице**</span><span class="sxs-lookup"><span data-stu-id="1dac9-138">**UserControlService**</span></span>](usercontrolservice-method-in-class-win32-service.md)       | <span data-ttu-id="1dac9-139">Пытается отправить в службу определенный пользователем управляющий код.</span><span class="sxs-lookup"><span data-stu-id="1dac9-139">Attempts to send a user-defined control code to a service.</span></span><br/>                                |



 

### <a name="properties"></a><span data-ttu-id="1dac9-140">Свойства</span><span class="sxs-lookup"><span data-stu-id="1dac9-140">Properties</span></span>

<span data-ttu-id="1dac9-141">Класс **\_ службы Win32** имеет следующие свойства.</span><span class="sxs-lookup"><span data-stu-id="1dac9-141">The **Win32\_Service** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="1dac9-142">**AcceptPause**</span><span class="sxs-lookup"><span data-stu-id="1dac9-142">**AcceptPause**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1dac9-143">Тип данных: **логический**</span><span class="sxs-lookup"><span data-stu-id="1dac9-143">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="1dac9-144">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="1dac9-144">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="1dac9-145">Квалификаторы: [**маппингстрингс**](../wmisdk/standard-qualifiers.md) ("Win32API \| Service Structures \| [**\_ Status**](/windows/win32/api/winsvc/ns-winsvc-service_status) \| двконтролсакцептед \| Service \_ Accept \_ Пауза \_ Continue"), [**DisplayName**](../wmisdk/standard-qualifiers.md) ("служба принимает паузу")</span><span class="sxs-lookup"><span data-stu-id="1dac9-145">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32API\|Service Structures\|[**SERVICE\_STATUS**](/windows/win32/api/winsvc/ns-winsvc-service_status)\|dwControlsAccepted\|SERVICE\_ACCEPT\_PAUSE\_CONTINUE"), [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Service Accepts Pause")</span></span>
</dt> </dl>

<span data-ttu-id="1dac9-146">Указывает, можно ли приостановить работу службы.</span><span class="sxs-lookup"><span data-stu-id="1dac9-146">Indicates whether the service can be paused.</span></span>

<span data-ttu-id="1dac9-147">Это свойство наследуется из [**Win32 \_ басесервице**](win32-baseservice.md).</span><span class="sxs-lookup"><span data-stu-id="1dac9-147">This property is inherited from [**Win32\_BaseService**](win32-baseservice.md).</span></span>

</dd> <dt>

<span data-ttu-id="1dac9-148">**AcceptStop**</span><span class="sxs-lookup"><span data-stu-id="1dac9-148">**AcceptStop**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1dac9-149">Тип данных: **логический**</span><span class="sxs-lookup"><span data-stu-id="1dac9-149">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="1dac9-150">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="1dac9-150">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="1dac9-151">Квалификаторы: [**маппингстрингс**](../wmisdk/standard-qualifiers.md) ("Win32API \| Service Structures \| [**\_ Status**](/windows/win32/api/winsvc/ns-winsvc-service_status) \| двконтролсакцептед \| Service \_ Accept \_ "), [**DisplayName**](../wmisdk/standard-qualifiers.md) ("служба принимает" останавливается ").</span><span class="sxs-lookup"><span data-stu-id="1dac9-151">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32API\|Service Structures\|[**SERVICE\_STATUS**](/windows/win32/api/winsvc/ns-winsvc-service_status)\|dwControlsAccepted\|SERVICE\_ACCEPT\_STOP"), [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Service Accepts Stop")</span></span>
</dt> </dl>

<span data-ttu-id="1dac9-152">Указывает, можно ли остановить службу.</span><span class="sxs-lookup"><span data-stu-id="1dac9-152">Indicates whether the service can be stopped.</span></span>

<span data-ttu-id="1dac9-153">Это свойство наследуется из [**Win32 \_ басесервице**](win32-baseservice.md).</span><span class="sxs-lookup"><span data-stu-id="1dac9-153">This property is inherited from [**Win32\_BaseService**](win32-baseservice.md).</span></span>

</dd> <dt>

<span data-ttu-id="1dac9-154">**Заголовок**</span><span class="sxs-lookup"><span data-stu-id="1dac9-154">**Caption**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1dac9-155">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="1dac9-155">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="1dac9-156">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="1dac9-156">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="1dac9-157">Квалификаторы: [**maxlen**](../wmisdk/standard-qualifiers.md) (64), [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Caption")</span><span class="sxs-lookup"><span data-stu-id="1dac9-157">Qualifiers: [**MaxLen**](../wmisdk/standard-qualifiers.md) (64), [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Caption")</span></span>
</dt> </dl>

<span data-ttu-id="1dac9-158">Краткое описание службы — однострочная строка.</span><span class="sxs-lookup"><span data-stu-id="1dac9-158">Short description of the service —a one-line string.</span></span>

<span data-ttu-id="1dac9-159">Это свойство наследуется от [**CIM \_ манажедсистемелемент**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="1dac9-159">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="1dac9-160">**Создание**</span><span class="sxs-lookup"><span data-stu-id="1dac9-160">**CheckPoint**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1dac9-161">Тип данных: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="1dac9-161">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="1dac9-162">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="1dac9-162">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="1dac9-163">Квалификаторы: [**маппингстрингс**](../wmisdk/standard-qualifiers.md) ("Win32API \| Service Structures \| [**\_ Status**](/windows/win32/api/winsvc/ns-winsvc-service_status) \| Двчеккпоинт"), [**DisplayName**](../wmisdk/standard-qualifiers.md) ("число контрольных точек")</span><span class="sxs-lookup"><span data-stu-id="1dac9-163">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32API\|Service Structures\|[**SERVICE\_STATUS**](/windows/win32/api/winsvc/ns-winsvc-service_status)\|dwCheckPoint"), [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Check Point Count")</span></span>
</dt> </dl>

<span data-ttu-id="1dac9-164">Значение, которое служба периодически увеличивает, чтобы сообщить о ходе выполнения во время длительной операции запуска, остановки, приостановки или продолжения работы.</span><span class="sxs-lookup"><span data-stu-id="1dac9-164">Value that the service increments periodically to report its progress during a long start, stop, pause, or continue operation.</span></span> <span data-ttu-id="1dac9-165">Например, служба увеличивает это значение по мере завершения каждого этапа инициализации при запуске.</span><span class="sxs-lookup"><span data-stu-id="1dac9-165">For example, the service increments this value as it completes each step of its initialization when it is starting up.</span></span> <span data-ttu-id="1dac9-166">Программа пользовательского интерфейса, вызывающая операцию в службе, использует это значение для отслеживания хода выполнения службы во время длительной операции.</span><span class="sxs-lookup"><span data-stu-id="1dac9-166">The user interface program that invokes the operation on the service uses this value to track the progress of the service during a lengthy operation.</span></span> <span data-ttu-id="1dac9-167">Это значение недопустимо и должно быть равно нулю, если у службы нет ожидающих операций запуска, остановки, приостановки или возобновления.</span><span class="sxs-lookup"><span data-stu-id="1dac9-167">This value is not valid and should be zero when the service does not have a start, stop, pause, or continue operation pending.</span></span>

</dd> <dt>

<span data-ttu-id="1dac9-168">**CreationClassName**</span><span class="sxs-lookup"><span data-stu-id="1dac9-168">**CreationClassName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1dac9-169">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="1dac9-169">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="1dac9-170">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="1dac9-170">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="1dac9-171">Квалификаторы: [**\_ ключ CIM**](../wmisdk/standard-wmi-qualifiers.md), [**DisplayName**](../wmisdk/standard-qualifiers.md) ("имя класса")</span><span class="sxs-lookup"><span data-stu-id="1dac9-171">Qualifiers: [**CIM\_Key**](../wmisdk/standard-wmi-qualifiers.md), [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Class Name")</span></span>
</dt> </dl>

<span data-ttu-id="1dac9-172">Имя первого конкретного класса, который будет отображаться в цепочке наследования, используемой при создании экземпляра.</span><span class="sxs-lookup"><span data-stu-id="1dac9-172">Name of the first concrete class to appear in the inheritance chain used in the creation of an instance.</span></span> <span data-ttu-id="1dac9-173">При использовании с другими ключевыми свойствами класса это свойство позволяет уникально идентифицировать все экземпляры этого класса и его подклассов.</span><span class="sxs-lookup"><span data-stu-id="1dac9-173">When used with the other key properties of the class, this property allows all instances of this class and its subclasses to be uniquely identified.</span></span>

<span data-ttu-id="1dac9-174">Это свойство наследуется [**от \_ службы CIM**](cim-service.md).</span><span class="sxs-lookup"><span data-stu-id="1dac9-174">This property is inherited from [**CIM\_Service**](cim-service.md).</span></span>

</dd> <dt>

<span data-ttu-id="1dac9-175">**DelayedAutoStart**</span><span class="sxs-lookup"><span data-stu-id="1dac9-175">**DelayedAutoStart**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1dac9-176">Тип данных: **логический**</span><span class="sxs-lookup"><span data-stu-id="1dac9-176">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="1dac9-177">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="1dac9-177">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="1dac9-178">Квалификаторы: [**маппингстрингс**](../wmisdk/standard-qualifiers.md) ("Win32API Service Structures" \| \| [**Service \_ delay \_ \_ Start \_ info**](/windows/win32/api/winsvc/ns-winsvc-service_delayed_auto_start_info) \| фделайедаутостарт "), [**DisplayName**](../wmisdk/standard-qualifiers.md) (" отложенный автоматический запуск ")</span><span class="sxs-lookup"><span data-stu-id="1dac9-178">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32API\|Service Structures\|[**SERVICE\_DELAYED\_AUTO\_START\_INFO**](/windows/win32/api/winsvc/ns-winsvc-service_delayed_auto_start_info)\|fDelayedAutostart"), [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Delayed Auto-Start")</span></span>
</dt> </dl>

<span data-ttu-id="1dac9-179">Если **значение — true**, служба запускается после запуска других служб, запускающих автозапуск, и короткой задержки.</span><span class="sxs-lookup"><span data-stu-id="1dac9-179">If **True**, the service is started after other auto-start services are started plus a short delay.</span></span>

<span data-ttu-id="1dac9-180">**Windows server 2012 R2, Windows 8.1, Windows server 2012, Windows 8, Windows server 2008 R2, Windows 7, Windows server 2008 и Windows Vista:** Это свойство не поддерживается до Windows Server 2016 и Windows 10.</span><span class="sxs-lookup"><span data-stu-id="1dac9-180">**Windows Server 2012 R2, Windows 8.1, Windows Server 2012, Windows 8, Windows Server 2008 R2, Windows 7, Windows Server 2008 and Windows Vista:** This property is not supported before Windows Server 2016 and Windows 10.</span></span>

</dd> <dt>

<span data-ttu-id="1dac9-181">**Описание**</span><span class="sxs-lookup"><span data-stu-id="1dac9-181">**Description**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1dac9-182">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="1dac9-182">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="1dac9-183">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="1dac9-183">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="1dac9-184">Квалификаторы: [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Описание")</span><span class="sxs-lookup"><span data-stu-id="1dac9-184">Qualifiers: [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Description")</span></span>
</dt> </dl>

<span data-ttu-id="1dac9-185">Описание объекта.</span><span class="sxs-lookup"><span data-stu-id="1dac9-185">Description of the object.</span></span>

<span data-ttu-id="1dac9-186">Это свойство наследуется от [**CIM \_ манажедсистемелемент**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="1dac9-186">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="1dac9-187">**DesktopInteract**</span><span class="sxs-lookup"><span data-stu-id="1dac9-187">**DesktopInteract**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1dac9-188">Тип данных: **логический**</span><span class="sxs-lookup"><span data-stu-id="1dac9-188">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="1dac9-189">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="1dac9-189">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="1dac9-190">Квалификаторы: [**маппингстрингс**](../wmisdk/standard-qualifiers.md) (" \| структуры служб Win32API \| [**запрос \_ \_ конфигурации**](/windows/win32/api/winsvc/ns-winsvc-query_service_configa)службы \| двсервицетипе \| \_ Интерактивный \_ процесс"), [**DisplayName**](../wmisdk/standard-qualifiers.md) ("взаимодействует с Desktop")</span><span class="sxs-lookup"><span data-stu-id="1dac9-190">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32API\|Service Structures\|[**QUERY\_SERVICE\_CONFIG**](/windows/win32/api/winsvc/ns-winsvc-query_service_configa)\|dwServiceType\|SERVICE\_INTERACTIVE\_PROCESS"), [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Interacts With Desktop")</span></span>
</dt> </dl>

<span data-ttu-id="1dac9-191">Указывает, может ли служба создавать и взаимодействовать с Windows на настольном компьютере и, таким образом, взаимодействовать с пользователем.</span><span class="sxs-lookup"><span data-stu-id="1dac9-191">Indicates whether the service can create or communicate with windows on the desktop, and thus interact in some way with a user.</span></span> <span data-ttu-id="1dac9-192">Интерактивные службы должны запускаться под локальной системной учетной записью.</span><span class="sxs-lookup"><span data-stu-id="1dac9-192">Interactive services must run under the Local System account.</span></span> <span data-ttu-id="1dac9-193">Большинство служб не являются интерактивными; то есть они не взаимодействуют с пользователем каким-либо образом.</span><span class="sxs-lookup"><span data-stu-id="1dac9-193">Most services are not interactive; that is, they do not communicate with the user in any way.</span></span>

<span data-ttu-id="1dac9-194">Это свойство наследуется из [**Win32 \_ басесервице**](win32-baseservice.md).</span><span class="sxs-lookup"><span data-stu-id="1dac9-194">This property is inherited from [**Win32\_BaseService**](win32-baseservice.md).</span></span>

</dd> <dt>

<span data-ttu-id="1dac9-195">**Отображаемое имя**</span><span class="sxs-lookup"><span data-stu-id="1dac9-195">**DisplayName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1dac9-196">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="1dac9-196">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="1dac9-197">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="1dac9-197">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="1dac9-198">Квалификаторы: [**маппингстрингс**](../wmisdk/standard-qualifiers.md) (" \| структуры служб Win32API \| [**запрос \_ \_ конфигурации службы**](/windows/win32/api/winsvc/ns-winsvc-query_service_configa) \| Лпдисплайнаме"), [**DisplayName**](../wmisdk/standard-qualifiers.md) ("отображаемое имя")</span><span class="sxs-lookup"><span data-stu-id="1dac9-198">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32API\|Service Structures\|[**QUERY\_SERVICE\_CONFIG**](/windows/win32/api/winsvc/ns-winsvc-query_service_configa)\|lpDisplayName"), [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Display Name")</span></span>
</dt> </dl>

<span data-ttu-id="1dac9-199">Имя службы, отображаемое в оснастке "службы".</span><span class="sxs-lookup"><span data-stu-id="1dac9-199">Name of the service as viewed in the Services snap-in.</span></span> <span data-ttu-id="1dac9-200">Максимальная длина этой строки равна 256 символам.</span><span class="sxs-lookup"><span data-stu-id="1dac9-200">This string has a maximum length of 256 characters.</span></span> <span data-ttu-id="1dac9-201">Обратите внимание, что отображаемое имя и имя службы (которые хранятся в реестре) не всегда одинаковы.</span><span class="sxs-lookup"><span data-stu-id="1dac9-201">Note that the display name and the service name (which is stored in the registry) are not always the same.</span></span> <span data-ttu-id="1dac9-202">Например, служба DHCP-клиента имеет имя службы DHCP, а не отображаемое имя DHCP-клиента.</span><span class="sxs-lookup"><span data-stu-id="1dac9-202">For example, the DHCP Client service has the service name Dhcp but the display name DHCP Client.</span></span> <span data-ttu-id="1dac9-203">В диспетчере управления службами имя сохраняется с учетом регистра.</span><span class="sxs-lookup"><span data-stu-id="1dac9-203">The name is case-preserved in the Service Control Manager.</span></span> <span data-ttu-id="1dac9-204">Однако в сравнениях **DisplayName** всегда учитывается регистр.</span><span class="sxs-lookup"><span data-stu-id="1dac9-204">However, **DisplayName** comparisons are always case-insensitive.</span></span>

<span data-ttu-id="1dac9-205">Ограничение: принимает то же значение, что и свойство **Name** .</span><span class="sxs-lookup"><span data-stu-id="1dac9-205">Constraint: Accepts the same value as the **Name** property.</span></span>

<span data-ttu-id="1dac9-206">Пример: "Атдиск"</span><span class="sxs-lookup"><span data-stu-id="1dac9-206">Example: "Atdisk"</span></span>

<span data-ttu-id="1dac9-207">Это свойство наследуется из [**Win32 \_ басесервице**](win32-baseservice.md).</span><span class="sxs-lookup"><span data-stu-id="1dac9-207">This property is inherited from [**Win32\_BaseService**](win32-baseservice.md).</span></span>

</dd> <dt>

<span data-ttu-id="1dac9-208">**ErrorControl**</span><span class="sxs-lookup"><span data-stu-id="1dac9-208">**ErrorControl**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1dac9-209">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="1dac9-209">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="1dac9-210">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="1dac9-210">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="1dac9-211">Квалификаторы: [**маппингстрингс**](../wmisdk/standard-qualifiers.md) (" \| структуры служб Win32API \| [**запрос \_ \_ конфигурации службы**](/windows/win32/api/winsvc/ns-winsvc-query_service_configa) \| Дверрорконтрол"), [**DisplayName**](../wmisdk/standard-qualifiers.md) ("серьезность сбоя при запуске")</span><span class="sxs-lookup"><span data-stu-id="1dac9-211">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32API\|Service Structures\|[**QUERY\_SERVICE\_CONFIG**](/windows/win32/api/winsvc/ns-winsvc-query_service_configa)\|dwErrorControl"), [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Severity Of Startup Failure")</span></span>
</dt> </dl>

<span data-ttu-id="1dac9-212">Серьезность ошибки, если не удается запустить службу во время запуска.</span><span class="sxs-lookup"><span data-stu-id="1dac9-212">Severity of the error if this service fails to start during startup.</span></span> <span data-ttu-id="1dac9-213">Значение указывает действие, предпринимаемое программой запуска, если происходит сбой.</span><span class="sxs-lookup"><span data-stu-id="1dac9-213">The value indicates the action taken by the startup program if failure occurs.</span></span> <span data-ttu-id="1dac9-214">Все ошибки записываются в журнал системой компьютера.</span><span class="sxs-lookup"><span data-stu-id="1dac9-214">All errors are logged by the computer system.</span></span>

<dt>

<span id="Ignore"></span><span id="ignore"></span><span id="IGNORE"></span>

<span data-ttu-id="1dac9-215"><span id="Ignore"></span><span id="ignore"></span><span id="IGNORE"></span>**Игнорировать** ("ignore")</span><span class="sxs-lookup"><span data-stu-id="1dac9-215"><span id="Ignore"></span><span id="ignore"></span><span id="IGNORE"></span>**Ignore** ("Ignore")</span></span>


</dt> <dd>

<span data-ttu-id="1dac9-216">Пользователь не получает уведомление.</span><span class="sxs-lookup"><span data-stu-id="1dac9-216">User is not notified.</span></span>

</dd> <dt>

<span id="Normal"></span><span id="normal"></span><span id="NORMAL"></span>

<span data-ttu-id="1dac9-217"><span id="Normal"></span><span id="normal"></span><span id="NORMAL"></span>**Обычная** ("Обычная")</span><span class="sxs-lookup"><span data-stu-id="1dac9-217"><span id="Normal"></span><span id="normal"></span><span id="NORMAL"></span>**Normal** ("Normal")</span></span>


</dt> <dd>

<span data-ttu-id="1dac9-218">Пользователь получает уведомление.</span><span class="sxs-lookup"><span data-stu-id="1dac9-218">User is notified.</span></span> <span data-ttu-id="1dac9-219">Обычно это будет окно сообщения с уведомлением пользователя о проблеме.</span><span class="sxs-lookup"><span data-stu-id="1dac9-219">Usually this will be a message box display notifying the user of the problem.</span></span>

</dd> <dt>

<span id="Severe"></span><span id="severe"></span><span id="SEVERE"></span>

<span data-ttu-id="1dac9-220"><span id="Severe"></span><span id="severe"></span><span id="SEVERE"></span>**Серьезная** ("серьезная")</span><span class="sxs-lookup"><span data-stu-id="1dac9-220"><span id="Severe"></span><span id="severe"></span><span id="SEVERE"></span>**Severe** ("Severe")</span></span>


</dt> <dd>

<span data-ttu-id="1dac9-221">Система перезапускается в последней известной рабочей конфигурации.</span><span class="sxs-lookup"><span data-stu-id="1dac9-221">System is restarted with the last-known-good configuration.</span></span>

</dd> <dt>

<span id="Critical"></span><span id="critical"></span><span id="CRITICAL"></span>

<span data-ttu-id="1dac9-222"><span id="Critical"></span><span id="critical"></span><span id="CRITICAL"></span>**Критическая** ("критическая")</span><span class="sxs-lookup"><span data-stu-id="1dac9-222"><span id="Critical"></span><span id="critical"></span><span id="CRITICAL"></span>**Critical** ("Critical")</span></span>


</dt> <dd>

<span data-ttu-id="1dac9-223">Попытка перезапустить систему в рабочей конфигурации.</span><span class="sxs-lookup"><span data-stu-id="1dac9-223">System attempts to restart with a good configuration.</span></span> <span data-ttu-id="1dac9-224">Если служба не запускается второй раз, происходит сбой запуска.</span><span class="sxs-lookup"><span data-stu-id="1dac9-224">If the service fails to start a second time, startup fails.</span></span>

</dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="1dac9-225"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Неизвестно** ("неизвестно")</span><span class="sxs-lookup"><span data-stu-id="1dac9-225"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** ("Unknown")</span></span>


</dt> <dd>

<span data-ttu-id="1dac9-226">Серьезность ошибки неизвестна.</span><span class="sxs-lookup"><span data-stu-id="1dac9-226">Severity of the error is unknown.</span></span>

</dd> </dl>

<span data-ttu-id="1dac9-227">Это свойство наследуется из [**Win32 \_ басесервице**](win32-baseservice.md).</span><span class="sxs-lookup"><span data-stu-id="1dac9-227">This property is inherited from [**Win32\_BaseService**](win32-baseservice.md).</span></span>

</dd> <dt>

<span data-ttu-id="1dac9-228">**ExitCode**</span><span class="sxs-lookup"><span data-stu-id="1dac9-228">**ExitCode**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1dac9-229">Тип данных: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="1dac9-229">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="1dac9-230">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="1dac9-230">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="1dac9-231">Квалификаторы: [**маппингстрингс**](../wmisdk/standard-qualifiers.md) ("Win32API \| Service Structures \| [**\_ Status**](/windows/win32/api/winsvc/ns-winsvc-service_status) \| DwWin32ExitCode"), [**DisplayName**](../wmisdk/standard-qualifiers.md) ("код выхода")</span><span class="sxs-lookup"><span data-stu-id="1dac9-231">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32API\|Service Structures\|[**SERVICE\_STATUS**](/windows/win32/api/winsvc/ns-winsvc-service_status)\|dwWin32ExitCode"), [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Exit Code")</span></span>
</dt> </dl>

<span data-ttu-id="1dac9-232">Код ошибки Windows, определяющий ошибки, возникающие при запуске или остановке службы.</span><span class="sxs-lookup"><span data-stu-id="1dac9-232">Windows error code that defines errors encountered in starting or stopping the service.</span></span> <span data-ttu-id="1dac9-233">Это свойство имеет значение ошибка, связанное со **\_ службой \_ \_ ошибок** (1066), если ошибка является уникальной для службы, представленной этим классом, а сведения об ошибке доступны в свойстве **сервицеспеЦифицекситкоде** .</span><span class="sxs-lookup"><span data-stu-id="1dac9-233">This property is set to **ERROR\_SERVICE\_SPECIFIC\_ERROR** (1066) when the error is unique to the service represented by this class, and information about the error is available in the **ServiceSpecificExitCode** property.</span></span> <span data-ttu-id="1dac9-234">Служба задает это значение **без \_ ошибок** при выполнении и снова после нормального завершения.</span><span class="sxs-lookup"><span data-stu-id="1dac9-234">The service sets this value to **NO\_ERROR** when running, and again upon normal termination.</span></span>

<span data-ttu-id="1dac9-235">Это свойство наследуется из [**Win32 \_ басесервице**](win32-baseservice.md).</span><span class="sxs-lookup"><span data-stu-id="1dac9-235">This property is inherited from [**Win32\_BaseService**](win32-baseservice.md).</span></span>

</dd> <dt>

<span data-ttu-id="1dac9-236">**InstallDate**</span><span class="sxs-lookup"><span data-stu-id="1dac9-236">**InstallDate**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1dac9-237">Тип данных: **DateTime**</span><span class="sxs-lookup"><span data-stu-id="1dac9-237">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="1dac9-238">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="1dac9-238">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="1dac9-239">Квалификаторы: [**маппингстрингс**](../wmisdk/standard-qualifiers.md) (MIF. DMTF \| ComponentID \| 001,5 "), [**DisplayName**](../wmisdk/standard-qualifiers.md) (" Дата установки ")</span><span class="sxs-lookup"><span data-stu-id="1dac9-239">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("MIF.DMTF\|ComponentID\|001.5"), [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Install Date")</span></span>
</dt> </dl>

<span data-ttu-id="1dac9-240">Объект Date установлен.</span><span class="sxs-lookup"><span data-stu-id="1dac9-240">Date object is installed.</span></span> <span data-ttu-id="1dac9-241">Для этого свойства не требуется указывать значение, указывающее, что объект установлен.</span><span class="sxs-lookup"><span data-stu-id="1dac9-241">This property does not require a value to indicate that the object is installed.</span></span>

<span data-ttu-id="1dac9-242">Это свойство наследуется от [**CIM \_ манажедсистемелемент**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="1dac9-242">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="1dac9-243">**Name**</span><span class="sxs-lookup"><span data-stu-id="1dac9-243">**Name**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1dac9-244">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="1dac9-244">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="1dac9-245">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="1dac9-245">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="1dac9-246">Квалификаторы: [ **ключ**](../wmisdk/key-qualifier.md)</span><span class="sxs-lookup"><span data-stu-id="1dac9-246">Qualifiers: [**Key**](../wmisdk/key-qualifier.md)</span></span>
</dt> </dl>

<span data-ttu-id="1dac9-247">Уникальный идентификатор службы, который предоставляет сведения об управляемых функциях.</span><span class="sxs-lookup"><span data-stu-id="1dac9-247">Unique identifier of the service that provides an indication of the functionality that is managed.</span></span> <span data-ttu-id="1dac9-248">Эти функциональные возможности описаны в свойстве **Description** объекта.</span><span class="sxs-lookup"><span data-stu-id="1dac9-248">This functionality is described in the **Description** property of the object.</span></span>

<span data-ttu-id="1dac9-249">Это свойство наследуется от [**CIM \_ манажедсистемелемент**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="1dac9-249">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="1dac9-250">**PathName**</span><span class="sxs-lookup"><span data-stu-id="1dac9-250">**PathName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1dac9-251">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="1dac9-251">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="1dac9-252">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="1dac9-252">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="1dac9-253">Квалификаторы: [**маппингстрингс**](../wmisdk/standard-qualifiers.md) (" \| структуры служб Win32API \| [**запрос \_ \_ конфигурации**](/windows/win32/api/winsvc/ns-winsvc-query_service_configa) \| Лпбинарипаснаме"), [**DisplayName**](../wmisdk/standard-qualifiers.md) ("имя пути к файлу")</span><span class="sxs-lookup"><span data-stu-id="1dac9-253">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32API\|Service Structures\|[**QUERY\_SERVICE\_CONFIG**](/windows/win32/api/winsvc/ns-winsvc-query_service_configa)\|lpBinaryPathName"), [**DisplayName**](../wmisdk/standard-qualifiers.md) ("File Path Name")</span></span>
</dt> </dl>

<span data-ttu-id="1dac9-254">Полный путь к двоичному файлу службы, реализующему службу.</span><span class="sxs-lookup"><span data-stu-id="1dac9-254">Fully qualified path to the service binary file that implements the service.</span></span>

<span data-ttu-id="1dac9-255">Пример: " \\ СистемныйКорневойКаталог \\ system32 \\ Drivers \\afd.sys"</span><span class="sxs-lookup"><span data-stu-id="1dac9-255">Example: "\\SystemRoot\\System32\\drivers\\afd.sys"</span></span>

<span data-ttu-id="1dac9-256">Это свойство наследуется из [**Win32 \_ басесервице**](win32-baseservice.md).</span><span class="sxs-lookup"><span data-stu-id="1dac9-256">This property is inherited from [**Win32\_BaseService**](win32-baseservice.md).</span></span>

</dd> <dt>

<span data-ttu-id="1dac9-257">**Идентификатор**</span><span class="sxs-lookup"><span data-stu-id="1dac9-257">**ProcessId**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1dac9-258">Тип данных: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="1dac9-258">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="1dac9-259">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="1dac9-259">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="1dac9-260">Квалификаторы: [**маппингстрингс**](../wmisdk/standard-qualifiers.md) ("Win32API \| Service Structures \| [**\_ Status \_ Process**](/windows/win32/api/winsvc/ns-winsvc-service_status_process) \| двпроцессид"), [**DisplayName**](../wmisdk/standard-qualifiers.md) ("идентификатор процесса")</span><span class="sxs-lookup"><span data-stu-id="1dac9-260">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32API\|Service Structures\|[**SERVICE\_STATUS\_PROCESS**](/windows/win32/api/winsvc/ns-winsvc-service_status_process)\|dwProcessId"), [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Process Id")</span></span>
</dt> </dl>

<span data-ttu-id="1dac9-261">Идентификатор процесса службы.</span><span class="sxs-lookup"><span data-stu-id="1dac9-261">Process identifier of the service.</span></span>

<span data-ttu-id="1dac9-262">Пример: 324</span><span class="sxs-lookup"><span data-stu-id="1dac9-262">Example: 324</span></span>

</dd> <dt>

<span data-ttu-id="1dac9-263">**сервицеспеЦифицекситкоде**</span><span class="sxs-lookup"><span data-stu-id="1dac9-263">**ServiceSpecificExitCode**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1dac9-264">Тип данных: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="1dac9-264">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="1dac9-265">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="1dac9-265">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="1dac9-266">Квалификаторы: [**маппингстрингс**](../wmisdk/standard-qualifiers.md) ("Win32API \| Service Structures \| [**\_ Status**](/windows/win32/api/winsvc/ns-winsvc-service_status) \| двсервицеспеЦифицекситкоде"), [**DisplayName**](../wmisdk/standard-qualifiers.md) ("специфический для сервера код выхода")</span><span class="sxs-lookup"><span data-stu-id="1dac9-266">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32API\|Service Structures\|[**SERVICE\_STATUS**](/windows/win32/api/winsvc/ns-winsvc-service_status)\|dwServiceSpecificExitCode"), [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Server Specific Exit Code")</span></span>
</dt> </dl>

<span data-ttu-id="1dac9-267">Код ошибки, зависящей от службы, для ошибок, возникающих во время запуска или остановки службы.</span><span class="sxs-lookup"><span data-stu-id="1dac9-267">Service-specific error code for errors that occur while the service is either starting or stopping.</span></span> <span data-ttu-id="1dac9-268">Коды выхода определяются службой, представленной этим классом.</span><span class="sxs-lookup"><span data-stu-id="1dac9-268">The exit codes are defined by the service represented by this class.</span></span> <span data-ttu-id="1dac9-269">Это значение задается только в том случае, если значение свойства **ExitCode** — ошибка, связанная со **\_ службой ошибок \_ \_** (1066).</span><span class="sxs-lookup"><span data-stu-id="1dac9-269">This value is only set when the **ExitCode** property value is **ERROR\_SERVICE\_SPECIFIC\_ERROR** (1066).</span></span>

<span data-ttu-id="1dac9-270">Это свойство наследуется из [**Win32 \_ басесервице**](win32-baseservice.md).</span><span class="sxs-lookup"><span data-stu-id="1dac9-270">This property is inherited from [**Win32\_BaseService**](win32-baseservice.md).</span></span>

</dd> <dt>

<span data-ttu-id="1dac9-271">**ServiceType**</span><span class="sxs-lookup"><span data-stu-id="1dac9-271">**ServiceType**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1dac9-272">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="1dac9-272">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="1dac9-273">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="1dac9-273">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="1dac9-274">Квалификаторы: [**маппингстрингс**](../wmisdk/standard-qualifiers.md) (" \| структуры служб Win32API \| [**запрос \_ \_ конфигурации службы**](/windows/win32/api/winsvc/ns-winsvc-query_service_configa) \| двсервицетипе"), [**DisplayName**](../wmisdk/standard-qualifiers.md) ("тип службы")</span><span class="sxs-lookup"><span data-stu-id="1dac9-274">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32API\|Service Structures\|[**QUERY\_SERVICE\_CONFIG**](/windows/win32/api/winsvc/ns-winsvc-query_service_configa)\|dwServiceType"), [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Service Type")</span></span>
</dt> </dl>

<span data-ttu-id="1dac9-275">Тип службы, предоставленной для вызывающих процессов.</span><span class="sxs-lookup"><span data-stu-id="1dac9-275">Type of service provided to calling processes.</span></span>

<span data-ttu-id="1dac9-276">Значения качества производительности:</span><span class="sxs-lookup"><span data-stu-id="1dac9-276">The values are:</span></span>

<dt>

<span id="Kernel_Driver"></span><span id="kernel_driver"></span><span id="KERNEL_DRIVER"></span>

<span data-ttu-id="1dac9-277">**Драйвер ядра** ("драйвер ядра")</span><span class="sxs-lookup"><span data-stu-id="1dac9-277">**Kernel Driver** ("Kernel Driver")</span></span>


</dt> <dd></dd> <dt>

<span id="File_System_Driver"></span><span id="file_system_driver"></span><span id="FILE_SYSTEM_DRIVER"></span>

<span data-ttu-id="1dac9-278">**Драйвер файловой системы** ("драйвер файловой системы")</span><span class="sxs-lookup"><span data-stu-id="1dac9-278">**File System Driver** ("File System Driver")</span></span>


</dt> <dd></dd> <dt>

<span id="Adapter"></span><span id="adapter"></span><span id="ADAPTER"></span>

<span data-ttu-id="1dac9-279">**Адаптер** ("адаптер")</span><span class="sxs-lookup"><span data-stu-id="1dac9-279">**Adapter** ("Adapter")</span></span>


</dt> <dd></dd> <dt>

<span id="Recognizer_Driver"></span><span id="recognizer_driver"></span><span id="RECOGNIZER_DRIVER"></span>

<span data-ttu-id="1dac9-280">**Драйвер распознавателя** ("драйвер распознавателя")</span><span class="sxs-lookup"><span data-stu-id="1dac9-280">**Recognizer Driver** ("Recognizer Driver")</span></span>


</dt> <dd></dd> <dt>

<span id="Own_Process"></span><span id="own_process"></span><span id="OWN_PROCESS"></span>

<span data-ttu-id="1dac9-281">**Собственный процесс** ("собственный процесс")</span><span class="sxs-lookup"><span data-stu-id="1dac9-281">**Own Process** ("Own Process")</span></span>


</dt> <dd></dd> <dt>

<span id="Share_Process"></span><span id="share_process"></span><span id="SHARE_PROCESS"></span>

<span data-ttu-id="1dac9-282">**Общий процесс** ("общий процесс")</span><span class="sxs-lookup"><span data-stu-id="1dac9-282">**Share Process** ("Share Process")</span></span>


</dt> <dd></dd> <dt>

<span id="Interactive_Process"></span><span id="interactive_process"></span><span id="INTERACTIVE_PROCESS"></span>

<span data-ttu-id="1dac9-283">**Интерактивный процесс** (интерактивный процесс)</span><span class="sxs-lookup"><span data-stu-id="1dac9-283">**Interactive Process** ("Interactive Process")</span></span>


<span data-ttu-id="1dac9-284"></dt> <dd></dd> </dl></span><span class="sxs-lookup"><span data-stu-id="1dac9-284"></dt> <dd></dd> </dl></span></span>

<span data-ttu-id="1dac9-285">Это свойство наследуется из [**Win32 \_ басесервице**](win32-baseservice.md).</span><span class="sxs-lookup"><span data-stu-id="1dac9-285">This property is inherited from [**Win32\_BaseService**](win32-baseservice.md).</span></span>

</dd> <dt>

<span data-ttu-id="1dac9-286">**Запуск**</span><span class="sxs-lookup"><span data-stu-id="1dac9-286">**Started**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1dac9-287">Тип данных: **логический**</span><span class="sxs-lookup"><span data-stu-id="1dac9-287">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="1dac9-288">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="1dac9-288">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="1dac9-289">Квалификаторы: [**DisplayName**](../wmisdk/standard-qualifiers.md) ("запущено")</span><span class="sxs-lookup"><span data-stu-id="1dac9-289">Qualifiers: [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Started")</span></span>
</dt> </dl>

<span data-ttu-id="1dac9-290">Указывает, запущена ли служба.</span><span class="sxs-lookup"><span data-stu-id="1dac9-290">Indicates whether or not the service is started.</span></span>

<span data-ttu-id="1dac9-291">Это свойство наследуется [**от \_ службы CIM**](cim-service.md).</span><span class="sxs-lookup"><span data-stu-id="1dac9-291">This property is inherited from [**CIM\_Service**](cim-service.md).</span></span>

</dd> <dt>

<span data-ttu-id="1dac9-292">**StartMode**</span><span class="sxs-lookup"><span data-stu-id="1dac9-292">**StartMode**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1dac9-293">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="1dac9-293">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="1dac9-294">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="1dac9-294">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="1dac9-295">Квалификаторы: [**DisplayName**](../wmisdk/standard-qualifiers.md) ("режим запуска")</span><span class="sxs-lookup"><span data-stu-id="1dac9-295">Qualifiers: [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Start Mode")</span></span>
</dt> </dl>

<span data-ttu-id="1dac9-296">Режим запуска базовой службы Windows.</span><span class="sxs-lookup"><span data-stu-id="1dac9-296">Start mode of the Windows base service.</span></span>

<dt>

<span id="Boot"></span><span id="boot"></span><span id="BOOT"></span>

<span data-ttu-id="1dac9-297"><span id="Boot"></span><span id="boot"></span><span id="BOOT"></span>**Boot** (Загрузка)</span><span class="sxs-lookup"><span data-stu-id="1dac9-297"><span id="Boot"></span><span id="boot"></span><span id="BOOT"></span>**Boot** ("Boot")</span></span>


</dt> <dd>

<span data-ttu-id="1dac9-298">Драйвер устройства запущен загрузчиком операционной системы (действует только для служб драйверов).</span><span class="sxs-lookup"><span data-stu-id="1dac9-298">Device driver started by the operating system loader (valid only for driver services).</span></span>

</dd> <dt>

<span id="System"></span><span id="system"></span><span id="SYSTEM"></span>

<span data-ttu-id="1dac9-299"><span id="System"></span><span id="system"></span><span id="SYSTEM"></span>**Система** ("System")</span><span class="sxs-lookup"><span data-stu-id="1dac9-299"><span id="System"></span><span id="system"></span><span id="SYSTEM"></span>**System** ("System")</span></span>


</dt> <dd>

<span data-ttu-id="1dac9-300">Драйвер устройства запущен процессом инициализации операционной системы.</span><span class="sxs-lookup"><span data-stu-id="1dac9-300">Device driver started by the operating system initialization process.</span></span> <span data-ttu-id="1dac9-301">Это значение допустимо только для служб драйверов.</span><span class="sxs-lookup"><span data-stu-id="1dac9-301">This value is valid only for driver services.</span></span>

</dd> <dt>

<span id="Auto"></span><span id="auto"></span><span id="AUTO"></span>

<span data-ttu-id="1dac9-302"><span id="Auto"></span><span id="auto"></span><span id="AUTO"></span>**Авто** ("Auto")</span><span class="sxs-lookup"><span data-stu-id="1dac9-302"><span id="Auto"></span><span id="auto"></span><span id="AUTO"></span>**Auto** ("Auto")</span></span>


</dt> <dd>

<span data-ttu-id="1dac9-303">Служба запускается автоматически диспетчером управления службами во время запуска системы.</span><span class="sxs-lookup"><span data-stu-id="1dac9-303">Service to be started automatically by the service control manager during system startup.</span></span> <span data-ttu-id="1dac9-304">Автоматические службы запускаются, даже если пользователь не входит в систему.</span><span class="sxs-lookup"><span data-stu-id="1dac9-304">Auto services are started even if a user does not log on.</span></span>

</dd> <dt>

<span id="Manual"></span><span id="manual"></span><span id="MANUAL"></span>

<span data-ttu-id="1dac9-305"><span id="Manual"></span><span id="manual"></span><span id="MANUAL"></span>**Вручную** ("вручную")</span><span class="sxs-lookup"><span data-stu-id="1dac9-305"><span id="Manual"></span><span id="manual"></span><span id="MANUAL"></span>**Manual** ("Manual")</span></span>


</dt> <dd>

<span data-ttu-id="1dac9-306">Служба, запускаемая диспетчером управления службами, когда процесс вызывает метод [**StartService**](startservice-method-in-class-win32-service.md) .</span><span class="sxs-lookup"><span data-stu-id="1dac9-306">Service to be started by the Service Control Manager when a process calls the [**StartService**](startservice-method-in-class-win32-service.md) method.</span></span> <span data-ttu-id="1dac9-307">Эти службы не запускаются, пока пользователь не войдет в систему и не запустит их.</span><span class="sxs-lookup"><span data-stu-id="1dac9-307">These services do not start unless a user logs on and starts them.</span></span>

</dd> <dt>

<span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>

<span data-ttu-id="1dac9-308"><span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>**Отключено** ("отключено")</span><span class="sxs-lookup"><span data-stu-id="1dac9-308"><span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>**Disabled** ("Disabled")</span></span>


</dt> <dd>

<span data-ttu-id="1dac9-309">Служба, которая не может быть запущена до тех пор, пока ее значение StartMode не изменится на Auto или Manual.</span><span class="sxs-lookup"><span data-stu-id="1dac9-309">Service that cannot be started until its StartMode is changed to either Auto or Manual.</span></span>

</dd> </dl>

<span data-ttu-id="1dac9-310">Это свойство наследуется [**от \_ службы CIM**](cim-service.md).</span><span class="sxs-lookup"><span data-stu-id="1dac9-310">This property is inherited from [**CIM\_Service**](cim-service.md).</span></span>

</dd> <dt>

<span data-ttu-id="1dac9-311">**StartName**</span><span class="sxs-lookup"><span data-stu-id="1dac9-311">**StartName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1dac9-312">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="1dac9-312">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="1dac9-313">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="1dac9-313">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="1dac9-314">Квалификаторы: [**маппингстрингс**](../wmisdk/standard-qualifiers.md) (" \| структуры служб Win32API \| [**запрос \_ \_ конфигурации службы**](/windows/win32/api/winsvc/ns-winsvc-query_service_configa) \| Лпсервицестартнаме"), [**DisplayName**](../wmisdk/standard-qualifiers.md) ("начальное имя учетной записи")</span><span class="sxs-lookup"><span data-stu-id="1dac9-314">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32API\|Service Structures\|[**QUERY\_SERVICE\_CONFIG**](/windows/win32/api/winsvc/ns-winsvc-query_service_configa)\|lpServiceStartName"), [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Starting Account Name")</span></span>
</dt> </dl>

<span data-ttu-id="1dac9-315">Имя учетной записи, под которой выполняется служба.</span><span class="sxs-lookup"><span data-stu-id="1dac9-315">Account name under which a service runs.</span></span> <span data-ttu-id="1dac9-316">В зависимости от типа службы имя учетной записи может быть указано в \\ формате имя_домена имя пользователя или имя участника-пользователя (" *Username@DomainName* ").</span><span class="sxs-lookup"><span data-stu-id="1dac9-316">Depending on the service type, the account name may be in the form of "DomainName\\Username" or UPN format ("*Username@DomainName*").</span></span> <span data-ttu-id="1dac9-317">Процесс службы заносится в журнал с использованием одной из этих двух форм при запуске.</span><span class="sxs-lookup"><span data-stu-id="1dac9-317">The service process is logged by using one of these two forms when it runs.</span></span> <span data-ttu-id="1dac9-318">Если учетная запись принадлежит к встроенному домену, то ". \\ Можно указать имя пользователя.</span><span class="sxs-lookup"><span data-stu-id="1dac9-318">If the account belongs to the built-in domain, then ".\\Username" can be specified.</span></span> <span data-ttu-id="1dac9-319">Для драйверов ядра или системного уровня **StartName** содержит имя объекта драйвера (то есть " \\ FileSystem \\ RDR" или " \\ Driver \\ КСНС"), которое система ввода-вывода использует для загрузки драйвера устройства.</span><span class="sxs-lookup"><span data-stu-id="1dac9-319">For kernel or system-level drivers, **StartName** contains the driver object name (that is, "\\FileSystem\\Rdr" or "\\Driver\\Xns") which the I/O system uses to load the device driver.</span></span> <span data-ttu-id="1dac9-320">Кроме того, если указано **значение NULL** , драйвер запускается с именем объекта по умолчанию, созданным системой ввода-вывода на основе имени службы.</span><span class="sxs-lookup"><span data-stu-id="1dac9-320">Additionally, if **NULL** is specified, the driver runs with a default object name created by the I/O system based on the service name.</span></span>

<span data-ttu-id="1dac9-321">Пример: "ДВДОМ \\ Admin"</span><span class="sxs-lookup"><span data-stu-id="1dac9-321">Example: "DWDOM\\Admin"</span></span>

<span data-ttu-id="1dac9-322">Это свойство наследуется из [**Win32 \_ басесервице**](win32-baseservice.md).</span><span class="sxs-lookup"><span data-stu-id="1dac9-322">This property is inherited from [**Win32\_BaseService**](win32-baseservice.md).</span></span>

</dd> <dt>

<span data-ttu-id="1dac9-323">**Состояние**</span><span class="sxs-lookup"><span data-stu-id="1dac9-323">**State**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1dac9-324">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="1dac9-324">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="1dac9-325">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="1dac9-325">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="1dac9-326">Квалификаторы: [**маппингстрингс**](../wmisdk/standard-qualifiers.md) ("Win32API \| Service Structures \| [**\_ Status**](/windows/win32/api/winsvc/ns-winsvc-service_status) \| двкуррентстате"), [**DisplayName**](../wmisdk/standard-qualifiers.md) ("State")</span><span class="sxs-lookup"><span data-stu-id="1dac9-326">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32API\|Service Structures\|[**SERVICE\_STATUS**](/windows/win32/api/winsvc/ns-winsvc-service_status)\|dwCurrentState "), [**DisplayName**](../wmisdk/standard-qualifiers.md) ("State")</span></span>
</dt> </dl>

<span data-ttu-id="1dac9-327">Текущее состояние базовой службы.</span><span class="sxs-lookup"><span data-stu-id="1dac9-327">Current state of the base service.</span></span>

<span data-ttu-id="1dac9-328">Значения качества производительности:</span><span class="sxs-lookup"><span data-stu-id="1dac9-328">The values are:</span></span>

<dt>

<span id="Stopped"></span><span id="stopped"></span><span id="STOPPED"></span>

<span data-ttu-id="1dac9-329">**Остановлено** ("остановлено")</span><span class="sxs-lookup"><span data-stu-id="1dac9-329">**Stopped** ("Stopped")</span></span>


</dt> <dd></dd> <dt>

<span id="Start_Pending"></span><span id="start_pending"></span><span id="START_PENDING"></span>

<span data-ttu-id="1dac9-330">**Ожидание запуска** ("Ожидание запуска")</span><span class="sxs-lookup"><span data-stu-id="1dac9-330">**Start Pending** ("Start Pending")</span></span>


</dt> <dd></dd> <dt>

<span id="Stop_Pending"></span><span id="stop_pending"></span><span id="STOP_PENDING"></span>

<span data-ttu-id="1dac9-331">**Ожидание ожидания** ("ожидание завершения")</span><span class="sxs-lookup"><span data-stu-id="1dac9-331">**Stop Pending** ("Stop Pending")</span></span>


</dt> <dd></dd> <dt>

<span id="Running"></span><span id="running"></span><span id="RUNNING"></span>

<span data-ttu-id="1dac9-332">**Работает** ("работает")</span><span class="sxs-lookup"><span data-stu-id="1dac9-332">**Running** ("Running")</span></span>


</dt> <dd></dd> <dt>

<span id="Continue_Pending"></span><span id="continue_pending"></span><span id="CONTINUE_PENDING"></span>

<span data-ttu-id="1dac9-333">**Ожидание продолжения** ("Ожидание продолжения")</span><span class="sxs-lookup"><span data-stu-id="1dac9-333">**Continue Pending** ("Continue Pending")</span></span>


</dt> <dd></dd> <dt>

<span id="Pause_Pending"></span><span id="pause_pending"></span><span id="PAUSE_PENDING"></span>

<span data-ttu-id="1dac9-334">**Ожидание приостановки** ("ожидание приостановки")</span><span class="sxs-lookup"><span data-stu-id="1dac9-334">**Pause Pending** ("Pause Pending")</span></span>


</dt> <dd></dd> <dt>

<span id="Paused"></span><span id="paused"></span><span id="PAUSED"></span>

<span data-ttu-id="1dac9-335">**Приостановлено** ("приостановлено")</span><span class="sxs-lookup"><span data-stu-id="1dac9-335">**Paused** ("Paused")</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="1dac9-336">**Неизвестно** ("неизвестно")</span><span class="sxs-lookup"><span data-stu-id="1dac9-336">**Unknown** ("Unknown")</span></span>


<span data-ttu-id="1dac9-337"></dt> <dd></dd> </dl></span><span class="sxs-lookup"><span data-stu-id="1dac9-337"></dt> <dd></dd> </dl></span></span>

<span data-ttu-id="1dac9-338">**Windows Server 2008 и Windows Vista:** Это свойство доступно только для чтения до Windows 7 и Windows Server 2008 R2.</span><span class="sxs-lookup"><span data-stu-id="1dac9-338">**Windows Server 2008 and Windows Vista:** This property is read-only before Windows 7 and Windows Server 2008 R2.</span></span>

<span data-ttu-id="1dac9-339">Это свойство наследуется из [**Win32 \_ басесервице**](win32-baseservice.md).</span><span class="sxs-lookup"><span data-stu-id="1dac9-339">This property is inherited from [**Win32\_BaseService**](win32-baseservice.md).</span></span>

</dd> <dt>

<span data-ttu-id="1dac9-340">**Состояние**</span><span class="sxs-lookup"><span data-stu-id="1dac9-340">**Status**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1dac9-341">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="1dac9-341">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="1dac9-342">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="1dac9-342">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="1dac9-343">Квалификаторы: [**maxlen**](../wmisdk/standard-qualifiers.md) (10), [**DisplayName**](../wmisdk/standard-qualifiers.md) ("состояние")</span><span class="sxs-lookup"><span data-stu-id="1dac9-343">Qualifiers: [**MaxLen**](../wmisdk/standard-qualifiers.md) (10), [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Status")</span></span>
</dt> </dl>

<span data-ttu-id="1dac9-344">Текущее состояние объекта.</span><span class="sxs-lookup"><span data-stu-id="1dac9-344">Current status of the object.</span></span> <span data-ttu-id="1dac9-345">Можно определить различные операционные и неоперационные состояния.</span><span class="sxs-lookup"><span data-stu-id="1dac9-345">Various operational and nonoperational statuses can be defined.</span></span> <span data-ttu-id="1dac9-346">Рабочие состояния включают: "ОК", "деградация" и "пред-ошибка" (элемент, например жесткий диск с поддержкой SMART, может работать правильно, но прогнозировать сбой в ближайшем будущем).</span><span class="sxs-lookup"><span data-stu-id="1dac9-346">Operational statuses include: "OK", "Degraded", and "Pred Fail" (an element, such as a SMART-enabled hard disk drive, may be functioning properly but predicting a failure in the near future).</span></span> <span data-ttu-id="1dac9-347">Неработающие состояния включают: "ошибка", "Запуск", "остановка" и "служба".</span><span class="sxs-lookup"><span data-stu-id="1dac9-347">Nonoperational statuses include: "Error", "Starting", "Stopping", and "Service".</span></span> <span data-ttu-id="1dac9-348">Последняя, «служба», может применяться во время зеркального копирования диска, перезагрузки списка разрешений пользователя или другой административной работы.</span><span class="sxs-lookup"><span data-stu-id="1dac9-348">The latter, "Service", could apply during mirror-resilvering of a disk, reload of a user permissions list, or other administrative work.</span></span> <span data-ttu-id="1dac9-349">Не вся такая работа находится в оперативном режиме, но управляемый элемент не является ни "ОК", ни одним из других состояний.</span><span class="sxs-lookup"><span data-stu-id="1dac9-349">Not all such work is online, yet the managed element is neither "OK" nor in one of the other states.</span></span>

<span data-ttu-id="1dac9-350">Это свойство наследуется от [**CIM \_ манажедсистемелемент**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="1dac9-350">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

<span data-ttu-id="1dac9-351">Значения качества производительности:</span><span class="sxs-lookup"><span data-stu-id="1dac9-351">The values are:</span></span>

<dt>

<span id="OK"></span><span id="ok"></span>

<span data-ttu-id="1dac9-352">**ОК** ("ОК")</span><span class="sxs-lookup"><span data-stu-id="1dac9-352">**OK** ("OK")</span></span>


</dt> <dd></dd> <dt>

<span id="Error"></span><span id="error"></span><span id="ERROR"></span>

<span data-ttu-id="1dac9-353">**Ошибка** ("ошибка")</span><span class="sxs-lookup"><span data-stu-id="1dac9-353">**Error** ("Error")</span></span>


</dt> <dd></dd> <dt>

<span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>

<span data-ttu-id="1dac9-354">**Пониженная работоспособность** (пониженная работоспособность)</span><span class="sxs-lookup"><span data-stu-id="1dac9-354">**Degraded** ("Degraded")</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="1dac9-355">**Неизвестно** ("неизвестно")</span><span class="sxs-lookup"><span data-stu-id="1dac9-355">**Unknown** ("Unknown")</span></span>


</dt> <dd></dd> <dt>

<span id="Pred_Fail"></span><span id="pred_fail"></span><span id="PRED_FAIL"></span>

<span data-ttu-id="1dac9-356">**Пред-ошибка** ("пред Fail")</span><span class="sxs-lookup"><span data-stu-id="1dac9-356">**Pred Fail** ("Pred Fail")</span></span>


</dt> <dd></dd> <dt>

<span id="Starting"></span><span id="starting"></span><span id="STARTING"></span>

<span data-ttu-id="1dac9-357">**Запуск** ("Запуск")</span><span class="sxs-lookup"><span data-stu-id="1dac9-357">**Starting** ("Starting")</span></span>


</dt> <dd></dd> <dt>

<span id="Stopping"></span><span id="stopping"></span><span id="STOPPING"></span>

<span data-ttu-id="1dac9-358">**Остановка** ("остановка")</span><span class="sxs-lookup"><span data-stu-id="1dac9-358">**Stopping** ("Stopping")</span></span>


</dt> <dd></dd> <dt>

<span id="Service"></span><span id="service"></span><span id="SERVICE"></span>

<span data-ttu-id="1dac9-359">**Служба** ("служба")</span><span class="sxs-lookup"><span data-stu-id="1dac9-359">**Service** ("Service")</span></span>


</dt> <dd></dd> <dt>

<span id="Stressed"></span><span id="stressed"></span><span id="STRESSED"></span>

<span data-ttu-id="1dac9-360">**Пренапряжению** ("напряжению")</span><span class="sxs-lookup"><span data-stu-id="1dac9-360">**Stressed** ("Stressed")</span></span>


</dt> <dd></dd> <dt>

<span id="NonRecover"></span><span id="nonrecover"></span><span id="NONRECOVER"></span>

<span data-ttu-id="1dac9-361">**Невосстановление** ("невосстановление")</span><span class="sxs-lookup"><span data-stu-id="1dac9-361">**NonRecover** ("NonRecover")</span></span>


</dt> <dd></dd> <dt>

<span id="No_Contact"></span><span id="no_contact"></span><span id="NO_CONTACT"></span>

<span data-ttu-id="1dac9-362">**Нет контакта** ("нет контакта")</span><span class="sxs-lookup"><span data-stu-id="1dac9-362">**No Contact** ("No Contact")</span></span>


</dt> <dd></dd> <dt>

<span id="Lost_Comm"></span><span id="lost_comm"></span><span id="LOST_COMM"></span>

<span data-ttu-id="1dac9-363">**Потеря** связи ("потеря связи")</span><span class="sxs-lookup"><span data-stu-id="1dac9-363">**Lost Comm** ("Lost Comm")</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="1dac9-364">**системкреатионкласснаме**</span><span class="sxs-lookup"><span data-stu-id="1dac9-364">**SystemCreationClassName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1dac9-365">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="1dac9-365">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="1dac9-366">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="1dac9-366">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="1dac9-367">Квалификаторы: [**распространено**](../wmisdk/standard-qualifiers.md) ("[**\_ система CIM**](cim-system.md).**CreationClassName**"), [**\_ ключ CIM**](../wmisdk/standard-wmi-qualifiers.md), [**DisplayName**](../wmisdk/standard-qualifiers.md) (" имя класса системы ")</span><span class="sxs-lookup"><span data-stu-id="1dac9-367">Qualifiers: [**Propagated**](../wmisdk/standard-qualifiers.md) ("[**CIM\_System**](cim-system.md).**CreationClassName**"), [**CIM\_Key**](../wmisdk/standard-wmi-qualifiers.md), [**DisplayName**](../wmisdk/standard-qualifiers.md) ("System Class Name")</span></span>
</dt> </dl>

<span data-ttu-id="1dac9-368">Имя типа системы, в которой размещена эта служба.</span><span class="sxs-lookup"><span data-stu-id="1dac9-368">Type name of the system that hosts this service.</span></span>

<span data-ttu-id="1dac9-369">Это свойство наследуется [**от \_ службы CIM**](cim-service.md).</span><span class="sxs-lookup"><span data-stu-id="1dac9-369">This property is inherited from [**CIM\_Service**](cim-service.md).</span></span>

</dd> <dt>

<span data-ttu-id="1dac9-370">**SystemName**</span><span class="sxs-lookup"><span data-stu-id="1dac9-370">**SystemName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1dac9-371">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="1dac9-371">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="1dac9-372">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="1dac9-372">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="1dac9-373">Квалификаторы: [**распространено**](../wmisdk/standard-qualifiers.md) ("[**\_ система CIM**](cim-system.md).**Name**"), [**\_ ключ CIM**](../wmisdk/standard-wmi-qualifiers.md), [**DisplayName**](../wmisdk/standard-qualifiers.md) (" System Name ")</span><span class="sxs-lookup"><span data-stu-id="1dac9-373">Qualifiers: [**Propagated**](../wmisdk/standard-qualifiers.md) ("[**CIM\_System**](cim-system.md).**Name**"), [**CIM\_Key**](../wmisdk/standard-wmi-qualifiers.md), [**DisplayName**](../wmisdk/standard-qualifiers.md) ("System Name")</span></span>
</dt> </dl>

<span data-ttu-id="1dac9-374">Имя системы, в которой размещена эта служба.</span><span class="sxs-lookup"><span data-stu-id="1dac9-374">Name of the system that hosts this service.</span></span>

<span data-ttu-id="1dac9-375">Это свойство наследуется [**от \_ службы CIM**](cim-service.md).</span><span class="sxs-lookup"><span data-stu-id="1dac9-375">This property is inherited from [**CIM\_Service**](cim-service.md).</span></span>

</dd> <dt>

<span data-ttu-id="1dac9-376">**TagId**</span><span class="sxs-lookup"><span data-stu-id="1dac9-376">**TagId**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1dac9-377">Тип данных: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="1dac9-377">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="1dac9-378">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="1dac9-378">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="1dac9-379">Квалификаторы: [**маппингстрингс**](../wmisdk/standard-qualifiers.md) (" \| структуры служб Win32API \| [**запрос \_ \_ конфигурации**](/windows/win32/api/winsvc/ns-winsvc-query_service_configa) \| двтагид"), [**DisplayName**](../wmisdk/standard-qualifiers.md) ("идентификатор тега")</span><span class="sxs-lookup"><span data-stu-id="1dac9-379">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32API\|Service Structures\|[**QUERY\_SERVICE\_CONFIG**](/windows/win32/api/winsvc/ns-winsvc-query_service_configa)\|dwTagId"), [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Tag Id")</span></span>
</dt> </dl>

<span data-ttu-id="1dac9-380">Уникальное значение тега для этой службы в группе.</span><span class="sxs-lookup"><span data-stu-id="1dac9-380">Unique tag value for this service in the group.</span></span> <span data-ttu-id="1dac9-381">Значение 0 (ноль) указывает, что у службы нет тега.</span><span class="sxs-lookup"><span data-stu-id="1dac9-381">A value of 0 (zero) indicates that the service does not have a tag.</span></span> <span data-ttu-id="1dac9-382">Тег можно использовать для упорядочивания запуска службы в группе порядка загрузки, указывая в реестре вектор порядка тегов в папке:</span><span class="sxs-lookup"><span data-stu-id="1dac9-382">A tag can be used to order service startup within a load order group by specifying a tag order vector in the registry located at:</span></span>

<span data-ttu-id="1dac9-383">**HKey \_ \_** \\  \\  \\  \\ **Граупордерлист** управления CurrentControlSet системы локального компьютера    </span><span class="sxs-lookup"><span data-stu-id="1dac9-383">**HKEY\_LOCAL\_MACHINE**\\**System**\\**CurrentControlSet**\\**Control**\\    **GroupOrderList**</span></span>

<span data-ttu-id="1dac9-384">Теги оцениваются только для служб типа "драйвер ядра" и "драйвер файловой системы", которые имеют режимы загрузки или запуска системы.</span><span class="sxs-lookup"><span data-stu-id="1dac9-384">Tags are only evaluated for Kernel Driver and File System Driver start type services that have Boot or System start modes.</span></span>

<span data-ttu-id="1dac9-385">Это свойство наследуется из [**Win32 \_ басесервице**](win32-baseservice.md).</span><span class="sxs-lookup"><span data-stu-id="1dac9-385">This property is inherited from [**Win32\_BaseService**](win32-baseservice.md).</span></span>

</dd> <dt>

<span data-ttu-id="1dac9-386">**ваисинт**</span><span class="sxs-lookup"><span data-stu-id="1dac9-386">**WaitHint**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1dac9-387">Тип данных: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="1dac9-387">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="1dac9-388">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="1dac9-388">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="1dac9-389">Квалификаторы: [**маппингстрингс**](../wmisdk/standard-qualifiers.md) ("Win32API \| Service Structures \| [**\_ Status**](/windows/win32/api/winsvc/ns-winsvc-service_status) \| двваисинт"), [**DisplayName**](../wmisdk/standard-qualifiers.md) ("предполагаемое время ожидания")</span><span class="sxs-lookup"><span data-stu-id="1dac9-389">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32API\|Service Structures\|[**SERVICE\_STATUS**](/windows/win32/api/winsvc/ns-winsvc-service_status)\|dwWaitHint"), [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Estimated Wait Time")</span></span>
</dt> </dl>

<span data-ttu-id="1dac9-390">Предполагаемое время в миллисекундах для ожидающей операции запуска, остановки, приостановки или продолжения работы.</span><span class="sxs-lookup"><span data-stu-id="1dac9-390">Estimated time required, in milliseconds, for a pending start, stop, pause, or continue operation.</span></span> <span data-ttu-id="1dac9-391">По истечении указанного времени служба выполняет следующий вызов метода **сбой SetServiceStatus** с увеличенным значением **контрольной точки** или изменением в **CurrentState**.</span><span class="sxs-lookup"><span data-stu-id="1dac9-391">After the specified time has elapsed, the service makes its next call to the **SetServiceStatus** method with either an incremented **CheckPoint** value or a change in **CurrentState**.</span></span> <span data-ttu-id="1dac9-392">Если время, указанное в **ваисинт** , прошло, а **контрольная точка** не была увеличена или **CurrentState** не изменилась, диспетчер управления службами или программа управления службами предполагает, что произошла ошибка.</span><span class="sxs-lookup"><span data-stu-id="1dac9-392">If the amount of time specified by **WaitHint** passes, and **CheckPoint** has not been incremented, or **CurrentState** has not changed, the service control manager or service control program assumes that an error has occurred.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="1dac9-393">Комментарии</span><span class="sxs-lookup"><span data-stu-id="1dac9-393">Remarks</span></span>

<span data-ttu-id="1dac9-394">Класс **\_ службы Win32** является производным от [**Win32 \_ басесервице**](win32-baseservice.md).</span><span class="sxs-lookup"><span data-stu-id="1dac9-394">The **Win32\_Service** class is derived from [**Win32\_BaseService**](win32-baseservice.md).</span></span>

<span data-ttu-id="1dac9-395">Способ управления конкретным компьютером сильно зависит от роли, которую играет компьютер.</span><span class="sxs-lookup"><span data-stu-id="1dac9-395">The way in which you manage a specific computer depends greatly on the role that computer plays.</span></span> <span data-ttu-id="1dac9-396">Например, вы обычно отслеживаете различные аспекты DNS-сервера, чем DHCP-сервер.</span><span class="sxs-lookup"><span data-stu-id="1dac9-396">For example, you generally monitor different aspects of a DNS server than a DHCP server.</span></span> <span data-ttu-id="1dac9-397">Хотя ни одно свойство не может сообщить вам, является ли конкретный компьютер сервером базы данных, сервером электронной почты или сервером мультимедиа, часто можно определить роль, которую компьютер воспроизводит, определив установленные на нем службы.</span><span class="sxs-lookup"><span data-stu-id="1dac9-397">Although no single property can tell you whether a particular computer is a database server, an e-mail server, or a multimedia server, you can often identify the role a computer plays by identifying the services installed on it.</span></span>

<span data-ttu-id="1dac9-398">В больших организациях только одна из основных служб (например, электронная почта), скорее всего, будет установлена на одном компьютере.</span><span class="sxs-lookup"><span data-stu-id="1dac9-398">In large organizations, only one of the major services (such as e-mail) is likely to be installed on a single computer.</span></span> <span data-ttu-id="1dac9-399">Почтовый сервер также будет работать как сервер для Microsoft® файлы проигрывателя® технологии Windows Media.</span><span class="sxs-lookup"><span data-stu-id="1dac9-399">It would be unusual for a mail server to also perform as a server for Microsoft® Windows Media® technologies player files.</span></span> <span data-ttu-id="1dac9-400">По этой причине определение службы, установленной на компьютере, может помочь определить роль компьютера в сети.</span><span class="sxs-lookup"><span data-stu-id="1dac9-400">Because of this, identifying a service installed on a computer can help identify the computer's role in the network.</span></span> <span data-ttu-id="1dac9-401">Если служба Microsoft® Exchange Server установлена и запущена на компьютере, как правило, предполагается, что этот компьютер работает как почтовый сервер.</span><span class="sxs-lookup"><span data-stu-id="1dac9-401">If the Microsoft® Exchange Server service is installed and running on a computer, it is generally safe to assume that this computer functions as a mail server.</span></span>

<span data-ttu-id="1dac9-402">Для перечисления служб, установленных на компьютере, можно использовать класс **\_ службы Win32** инструментария WMI.</span><span class="sxs-lookup"><span data-stu-id="1dac9-402">You can use the WMI **Win32\_Service** class to enumerate the services installed on a computer.</span></span> <span data-ttu-id="1dac9-403">Кроме того, этот класс можно использовать для определения того, работают ли эти службы в данный момент, а также какие другие необходимые сведения об этой службе и как они были настроены.</span><span class="sxs-lookup"><span data-stu-id="1dac9-403">In addition, you can use this class to determine whether those services are currently running and to return any other required information about that service and how it has been configured.</span></span>

<span data-ttu-id="1dac9-404">Приложение службы соответствует правилам интерфейса диспетчера управления службами (SCM) и может запускаться пользователем автоматически при запуске системы с помощью служебной программы панели управления "службы" или приложения, использующего функции службы, входящие в API Windows.</span><span class="sxs-lookup"><span data-stu-id="1dac9-404">A service application conforms to the interface rules of the Service Control Manager (SCM), and can be started by a user automatically at system start through the Services control panel utility, or by an application that uses the service functions included in the Windows API.</span></span> <span data-ttu-id="1dac9-405">Службы могут запускаться при отсутствии пользователей, выполнивших вход в систему.</span><span class="sxs-lookup"><span data-stu-id="1dac9-405">Services can start when there are no users logged on to the computer.</span></span>

<span data-ttu-id="1dac9-406">Пользователь, подключающийся с удаленного компьютера, должен иметь разрешение **SC \_ Manager \_ Connect** , чтобы иметь возможность перечислить этот класс.</span><span class="sxs-lookup"><span data-stu-id="1dac9-406">A user connecting from a remote computer must have the **SC\_MANAGER\_CONNECT** privilege enabled to be able to enumerate this class.</span></span> <span data-ttu-id="1dac9-407">Дополнительные сведения см. в разделе [Безопасность службы и права доступа](../services/service-security-and-access-rights.md).</span><span class="sxs-lookup"><span data-stu-id="1dac9-407">For more information, see [Service Security and Access Rights](../services/service-security-and-access-rights.md).</span></span>

## <a name="examples"></a><span data-ttu-id="1dac9-408">Примеры</span><span class="sxs-lookup"><span data-stu-id="1dac9-408">Examples</span></span>

<span data-ttu-id="1dac9-409">[Запрос PS-WMI, который возвращает службу "состояние" в](https://Gallery.TechNet.Microsoft.Com/0f1ab629-d463-4406-be54-ec2c4c23bc1f) примере PowerShell для группы устройств в коллекции TechNet, использует **\_ службу Win32** для создания списка устройств на основе Active Directory, а затем запрашивает каждое устройство, отвечающее на пингфор определенной службы.</span><span class="sxs-lookup"><span data-stu-id="1dac9-409">The [PS- WMI Query that returns Service 'State' on a group of devices](https://Gallery.TechNet.Microsoft.Com/0f1ab629-d463-4406-be54-ec2c4c23bc1f) PowerShell sample on TechNet Gallery uses **Win32\_Service** to create a list of devices from Active Directory, and then query each device that responds with pingfor a specific service running.</span></span>

<span data-ttu-id="1dac9-410">Пример [серверного отчета](https://Gallery.TechNet.Microsoft.Com/Server-Report-7b4ac2fb) PowerShell в коллекции TechNet использует **\_ службу Win32** для сбора сведений о сервере и публикации в документе Word.</span><span class="sxs-lookup"><span data-stu-id="1dac9-410">The [Server Report](https://Gallery.TechNet.Microsoft.Com/Server-Report-7b4ac2fb) PowerShell sample on TechNet Gallery uses **Win32\_Service** to gather server information and publish in Word document.</span></span>

<span data-ttu-id="1dac9-411">В следующем образце кода VBScript отображаются все установленные в данный момент службы.</span><span class="sxs-lookup"><span data-stu-id="1dac9-411">The following VBScript code sample displays all currently installed services.</span></span>


```VB
for each Service in _ 
    GetObject("winmgmts:").InstancesOf ("Win32_Service")
 WScript.Echo ""
 WScript.Echo Service.Name

 description = Service.Description 
 if IsNull(description) then description = "<No description>"

 pathName = Service.PathName
 if IsNull(pathName) then pathName = "<No path>"

 startName = Service.StartName
 if IsNull(startName) then startName = "<None>"

 WScript.Echo "  Description:  ", description
 WScript.Echo "  Executable:   ", pathName
 WScript.Echo "  Status:       ", Service.Status
 WScript.Echo "  State:        ", Service.State
 WScript.Echo "  Start Mode:   ", Service.StartMode
 Wscript.Echo "  Start Name:   ", startName
next
```



<span data-ttu-id="1dac9-412">Следующий пример кода VBScript описывает приостановленные, запущенные и остановленные службы на указанном компьютере.</span><span class="sxs-lookup"><span data-stu-id="1dac9-412">The following VBScript code sample describes the paused, running, and stopped services on the specified computer.</span></span>


```VB
On Error Resume Next
 StateString = "Paused,Running,Stopped"
 StateArray = Split(StateString, ",", -1, 1) 
 ComputerName = InputBox("Enter the computer name", "List Service", "localhost")

 For x = 0 to Ubound (StateArray)
 Set Services = GetObject("winmgmts:\\" & ComputerName & "\Root\CIMv2").ExecQuery("SELECT * FROM Win32_Service where State='" & StateArray(x) & "'")
 
 For Each Service in Services
  SList = SList & Service.Name & VBlf 
 Next

 WScript.Echo StateArray(x) & " Services: " & VBlf & SList
 SList = ""

Next
```



<span data-ttu-id="1dac9-413">В следующем скрипте Perl показано, как получить список выполняющихся служб из экземпляров **\_ службы Win32**.</span><span class="sxs-lookup"><span data-stu-id="1dac9-413">The following Perl script demonstrates how to retrieve a list of running services from instances of **Win32\_Service**.</span></span>


```
use strict;
use Win32::OLE;

my ( $ServiceSet, $Service );

eval { $ServiceSet = Win32::OLE->GetObject("winmgmts:{impersonationLevel=impersonate}!\\\\.\\Root\\CIMv2")->
 ExecQuery("SELECT * FROM Win32_Service WHERE State=\"Running\""); };
unless ($@)
{
 print "\n";
 foreach $Service (in $ServiceSet) 
 {
  print $Service->{Name}, "\n";
  if( $Service->{Description} ) 
   {
    print "  $Service->{Description}\n";
   }
  else
   {
    print "  <No description>\n";
   }
  print "  Process ID: ", $Service->{ProcessId}, "\n";
  print "  Start Mode: ", $Service->{StartMode}, "\n";
  print "\n";
 }
}
else
{
 print STDERR Win32::OLE->LastError, "\n";
}
```



<span data-ttu-id="1dac9-414">В следующем \# образце c используется [Microsoft. Management. Infrastructure](/previous-versions/windows/desktop/wmi_v2/mi-managed-api/hh832958(v=vs.85)) для получения всех выполняющихся служб на локальном компьютере.</span><span class="sxs-lookup"><span data-stu-id="1dac9-414">The following c\# sample uses [Microsoft.Management.Infrastructure](/previous-versions/windows/desktop/wmi_v2/mi-managed-api/hh832958(v=vs.85)) to retrieve all the running services on the local machine.</span></span>


```CSharp
static void QueryInstanceFunc()
        {
 
            CimSession session = CimSession.Create("localHost");
            IEnumerable<CimInstance> queryInstance = session.QueryInstances(@"root\cimv2", "WQL", "SELECT * FROM Win32_Service");

            foreach (CimInstance cimObj in queryInstance)
            {
                Console.WriteLine(cimObj.CimInstanceProperties["Name"].ToString());
                Console.WriteLine(cimObj.CimInstanceProperties["State"].ToString());
                Console.WriteLine(cimObj.CimInstanceProperties["Status"].ToString());
                
                //Console.WriteLine(cimObj.CimInstanceProperties["NetworkAddress"].ToString());
                Console.WriteLine();

            }

            Console.ReadLine();
        }
    
```



<span data-ttu-id="1dac9-415">Следующий пример кода на языке C \# использует пространство имен [System. Management](/dotnet/api/system.management) для получения всех работающих служб на локальном компьютере.</span><span class="sxs-lookup"><span data-stu-id="1dac9-415">The following C\# code sample uses [System.Management](/dotnet/api/system.management) namespace to retrieve all running services on the local machine.</span></span>

> [!Note]  
> <span data-ttu-id="1dac9-416">[System. Management](/dotnet/api/system.management) содержит исходные классы, используемые для доступа к WMI; Однако они считаются более медленными и обычно не масштабируются, а также их аналоги [Microsoft. Management. Infrastructure](/previous-versions/windows/desktop/wmi_v2/mi-managed-api/hh832958(v=vs.85)) .</span><span class="sxs-lookup"><span data-stu-id="1dac9-416">[System.Management](/dotnet/api/system.management) contains the original classes used to access WMI; however, they are considered slower and generally do not scale as well as their [Microsoft.Management.Infrastructure](/previous-versions/windows/desktop/wmi_v2/mi-managed-api/hh832958(v=vs.85)) counterparts.</span></span>

 


```CSharp
using System.Management;
...
        static void oldSchoolQueryInstanceFunc()
        {

            ObjectQuery query = new ObjectQuery("SELECT * FROM Win32_Service");
            ManagementObjectSearcher searcher = new ManagementObjectSearcher(query);


            ManagementObjectCollection queryCollection = searcher.Get();
            foreach (ManagementObject m in queryCollection)
            {
                Console.WriteLine("ServiceName : {0}", m["Name"]);
                Console.WriteLine("State : {0}", m["State"]);
                Console.WriteLine("Status : {0}", m["Status"]);
                Console.WriteLine();
            }

            Console.ReadLine();


        }
```



## <a name="requirements"></a><span data-ttu-id="1dac9-417">Требования</span><span class="sxs-lookup"><span data-stu-id="1dac9-417">Requirements</span></span>



| <span data-ttu-id="1dac9-418">Требование</span><span class="sxs-lookup"><span data-stu-id="1dac9-418">Requirement</span></span> | <span data-ttu-id="1dac9-419">Значение</span><span class="sxs-lookup"><span data-stu-id="1dac9-419">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="1dac9-420">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="1dac9-420">Minimum supported client</span></span><br/> | <span data-ttu-id="1dac9-421">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="1dac9-421">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="1dac9-422">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="1dac9-422">Minimum supported server</span></span><br/> | <span data-ttu-id="1dac9-423">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="1dac9-423">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="1dac9-424">Пространство имен</span><span class="sxs-lookup"><span data-stu-id="1dac9-424">Namespace</span></span><br/>                | <span data-ttu-id="1dac9-425">Корневой \\ CIMV2</span><span class="sxs-lookup"><span data-stu-id="1dac9-425">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="1dac9-426">MOF</span><span class="sxs-lookup"><span data-stu-id="1dac9-426">MOF</span></span><br/>                      | <dl> <span data-ttu-id="1dac9-427"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="1dac9-427"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="1dac9-428">DLL</span><span class="sxs-lookup"><span data-stu-id="1dac9-428">DLL</span></span><br/>                      | <dl> <span data-ttu-id="1dac9-429"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="1dac9-429"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="1dac9-430">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="1dac9-430">See also</span></span>

<dl> <dt>

[<span data-ttu-id="1dac9-431">**\_Басесервице Win32**</span><span class="sxs-lookup"><span data-stu-id="1dac9-431">**Win32\_BaseService**</span></span>](win32-baseservice.md)
</dt> <dt>

[<span data-ttu-id="1dac9-432">Классы операционной системы</span><span class="sxs-lookup"><span data-stu-id="1dac9-432">Operating System Classes</span></span>](./operating-system-classes.md)
</dt> <dt>

[<span data-ttu-id="1dac9-433">Задачи WMI: службы</span><span class="sxs-lookup"><span data-stu-id="1dac9-433">WMI Tasks: Services</span></span>](../wmisdk/wmi-tasks--services.md)
</dt> </dl>

 

 
