---
description: '\_Абстрактный класс WMI Басесервице Win32 представляет исполняемые объекты, установленные в базе данных реестра, обслуживаемой диспетчером управления службами.'
ms.assetid: 63673df9-3e41-4668-98fe-dc0e048328c1
ms.tgt_platform: multiple
title: Класс Win32_BaseService
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_BaseService
- Win32_BaseService.AcceptPause
- Win32_BaseService.AcceptStop
- Win32_BaseService.Caption
- Win32_BaseService.CreationClassName
- Win32_BaseService.Description
- Win32_BaseService.DesktopInteract
- Win32_BaseService.DisplayName
- Win32_BaseService.ErrorControl
- Win32_BaseService.ExitCode
- Win32_BaseService.InstallDate
- Win32_BaseService.Name
- Win32_BaseService.PathName
- Win32_BaseService.ServiceSpecificExitCode
- Win32_BaseService.ServiceType
- Win32_BaseService.Started
- Win32_BaseService.StartMode
- Win32_BaseService.StartName
- Win32_BaseService.State
- Win32_BaseService.Status
- Win32_BaseService.SystemCreationClassName
- Win32_BaseService.SystemName
- Win32_BaseService.TagId
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: b46f3b4bd37770a5f3a7c1a2d2faa93d49bc079a
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104142508"
---
# <a name="win32_baseservice-class"></a><span data-ttu-id="3c71d-103">\_Класс Win32 басесервице</span><span class="sxs-lookup"><span data-stu-id="3c71d-103">Win32\_BaseService class</span></span>

<span data-ttu-id="3c71d-104">Абстрактный [класс WMI](/windows/desktop/WmiSdk/retrieving-a-class) **\_ басесервице Win32** представляет исполняемые объекты, установленные в базе данных реестра, обслуживаемой диспетчером управления службами.</span><span class="sxs-lookup"><span data-stu-id="3c71d-104">The **Win32\_BaseService** abstract [WMI class](/windows/desktop/WmiSdk/retrieving-a-class) represents executable objects that are installed in a registry database maintained by the Service Control Manager.</span></span> <span data-ttu-id="3c71d-105">Исполняемый файл, связанный со службой, может запускаться во время загрузки программой загрузки или системой.</span><span class="sxs-lookup"><span data-stu-id="3c71d-105">The executable file associated with a service can be started at boot time by a boot program or by the system.</span></span> <span data-ttu-id="3c71d-106">Он также может быть запущен по запросу диспетчером управления службами.</span><span class="sxs-lookup"><span data-stu-id="3c71d-106">It can also be started on-demand by the Service Control Manager.</span></span> <span data-ttu-id="3c71d-107">Любая служба или процесс, не принадлежащий определенному пользователю и предоставляющий интерфейс некоторой функциональности, поддерживаемой компьютерной системой, является потомком (или членом) этого класса.</span><span class="sxs-lookup"><span data-stu-id="3c71d-107">Any service or process that is not owned by a specific user, and that provides an interface to some functionality supported by the computer system, is a descendant (or member) of this class.</span></span>

<span data-ttu-id="3c71d-108">Пример. служба клиента DHCP на компьютере под управлением Windows Server.</span><span class="sxs-lookup"><span data-stu-id="3c71d-108">Example: The dynamic host configuration protocol (DHCP) client service on a computer system running Windows Server.</span></span>

<span data-ttu-id="3c71d-109">Следующий пример синтаксиса — упрощенный MOF-код, который включает все наследуемые свойства.</span><span class="sxs-lookup"><span data-stu-id="3c71d-109">The following syntax is simplified from Managed Object Format (MOF) code and includes all of the inherited properties.</span></span> <span data-ttu-id="3c71d-110">Свойства перечислены в алфавитном порядке, а не в MOF.</span><span class="sxs-lookup"><span data-stu-id="3c71d-110">Properties are listed in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="3c71d-111">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="3c71d-111">Syntax</span></span>

``` syntax
[SupportsCreate, CreateBy("Create"), SupportsDelete, DeleteBy("DeleteInstance"), Abstract, Provider("CIMWin32"), UUID("{8502C4C4-5FBB-11D2-AAC1-006008C78BC7}"), DisplayName("System Drivers and Services"), AMENDMENT]
class Win32_BaseService : CIM_Service
{
  boolean  AcceptPause;
  boolean  AcceptStop;
  string   Caption;
  string   CreationClassName;
  string   Description;
  boolean  DesktopInteract;
  string   DisplayName;
  string   ErrorControl;
  uint32   ExitCode;
  datetime InstallDate;
  string   Name;
  string   PathName;
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
};
```

## <a name="members"></a><span data-ttu-id="3c71d-112">Члены</span><span class="sxs-lookup"><span data-stu-id="3c71d-112">Members</span></span>

<span data-ttu-id="3c71d-113">Класс **Win32 \_ басесервице** имеет следующие типы членов:</span><span class="sxs-lookup"><span data-stu-id="3c71d-113">The **Win32\_BaseService** class has these types of members:</span></span>

-   [<span data-ttu-id="3c71d-114">Методы</span><span class="sxs-lookup"><span data-stu-id="3c71d-114">Methods</span></span>](#methods)
-   [<span data-ttu-id="3c71d-115">Свойства</span><span class="sxs-lookup"><span data-stu-id="3c71d-115">Properties</span></span>](#properties)

### <a name="methods"></a><span data-ttu-id="3c71d-116">Методы</span><span class="sxs-lookup"><span data-stu-id="3c71d-116">Methods</span></span>

<span data-ttu-id="3c71d-117">Класс **Win32 \_ басесервице** содержит следующие методы.</span><span class="sxs-lookup"><span data-stu-id="3c71d-117">The **Win32\_BaseService** class has these methods.</span></span>



| <span data-ttu-id="3c71d-118">Метод</span><span class="sxs-lookup"><span data-stu-id="3c71d-118">Method</span></span>                                                                             | <span data-ttu-id="3c71d-119">Описание</span><span class="sxs-lookup"><span data-stu-id="3c71d-119">Description</span></span>                                                                   |
|:-----------------------------------------------------------------------------------|:------------------------------------------------------------------------------|
| [<span data-ttu-id="3c71d-120">**Change**</span><span class="sxs-lookup"><span data-stu-id="3c71d-120">**Change**</span></span>](change-method-in-class-win32-baseservice.md)                         | <span data-ttu-id="3c71d-121">Изменяет службу.</span><span class="sxs-lookup"><span data-stu-id="3c71d-121">Modifies a service.</span></span><br/>                                                |
| [<span data-ttu-id="3c71d-122">**чанжестартмоде**</span><span class="sxs-lookup"><span data-stu-id="3c71d-122">**ChangeStartMode**</span></span>](changestartmode-method-in-class-win32-baseservice.md)       | <span data-ttu-id="3c71d-123">Изменяет режим запуска службы.</span><span class="sxs-lookup"><span data-stu-id="3c71d-123">Modifies the start mode of a service.</span></span><br/>                              |
| [<span data-ttu-id="3c71d-124">**Создать**</span><span class="sxs-lookup"><span data-stu-id="3c71d-124">**Create**</span></span>](create-method-in-class-win32-baseservice.md)                         | <span data-ttu-id="3c71d-125">Создает новую службу.</span><span class="sxs-lookup"><span data-stu-id="3c71d-125">Creates a new service.</span></span><br/>                                             |
| [<span data-ttu-id="3c71d-126">**Удалить**</span><span class="sxs-lookup"><span data-stu-id="3c71d-126">**Delete**</span></span>](delete-method-in-class-win32-baseservice.md)                         | <span data-ttu-id="3c71d-127">Удаляет существующую службу.</span><span class="sxs-lookup"><span data-stu-id="3c71d-127">Deletes an existing service.</span></span><br/>                                       |
| [<span data-ttu-id="3c71d-128">**интеррогатесервице**</span><span class="sxs-lookup"><span data-stu-id="3c71d-128">**InterrogateService**</span></span>](interrogateservice-method-in-class-win32-baseservice.md) | <span data-ttu-id="3c71d-129">Запрашивает обновление состояния службы до Service Manager.</span><span class="sxs-lookup"><span data-stu-id="3c71d-129">Requests that the service update its state to the service manager.</span></span><br/> |
| [<span data-ttu-id="3c71d-130">**PauseService**</span><span class="sxs-lookup"><span data-stu-id="3c71d-130">**PauseService**</span></span>](pauseservice-method-in-class-win32-baseservice.md)             | <span data-ttu-id="3c71d-131">Пытается перевести службу в состояние приостановки.</span><span class="sxs-lookup"><span data-stu-id="3c71d-131">Attempts to place the service in the paused state.</span></span><br/>                 |
| [<span data-ttu-id="3c71d-132">**ResumeService**</span><span class="sxs-lookup"><span data-stu-id="3c71d-132">**ResumeService**</span></span>](resumeservice-method-in-class-win32-baseservice.md)           | <span data-ttu-id="3c71d-133">Пытается перевести службу в состояние возобновления.</span><span class="sxs-lookup"><span data-stu-id="3c71d-133">Attempts to place the service in the resumed state.</span></span><br/>                |
| [<span data-ttu-id="3c71d-134">**StartService**</span><span class="sxs-lookup"><span data-stu-id="3c71d-134">**StartService**</span></span>](startservice-method-in-class-win32-baseservice.md)             | <span data-ttu-id="3c71d-135">Пытается перевести службу в состояние запуска.</span><span class="sxs-lookup"><span data-stu-id="3c71d-135">Attempts to place the service into its startup state.</span></span><br/>              |
| [<span data-ttu-id="3c71d-136">**StopService**</span><span class="sxs-lookup"><span data-stu-id="3c71d-136">**StopService**</span></span>](stopservice-method-in-class-win32-baseservice.md)               | <span data-ttu-id="3c71d-137">Метод класса, который помещает службу в остановленное состояние.</span><span class="sxs-lookup"><span data-stu-id="3c71d-137">Class method that places the service in the stopped state.</span></span><br/>         |
| [<span data-ttu-id="3c71d-138">**усерконтролсервице**</span><span class="sxs-lookup"><span data-stu-id="3c71d-138">**UserControlService**</span></span>](usercontrolservice-method-in-class-win32-baseservice.md) | <span data-ttu-id="3c71d-139">Пытается отправить в службу определенный пользователем управляющий код.</span><span class="sxs-lookup"><span data-stu-id="3c71d-139">Attempts to send a user-defined control code to a service.</span></span><br/>         |



 

### <a name="properties"></a><span data-ttu-id="3c71d-140">Свойства</span><span class="sxs-lookup"><span data-stu-id="3c71d-140">Properties</span></span>

<span data-ttu-id="3c71d-141">Класс **Win32 \_ басесервице** имеет следующие свойства.</span><span class="sxs-lookup"><span data-stu-id="3c71d-141">The **Win32\_BaseService** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="3c71d-142">**AcceptPause**</span><span class="sxs-lookup"><span data-stu-id="3c71d-142">**AcceptPause**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3c71d-143">Тип данных: **логический**</span><span class="sxs-lookup"><span data-stu-id="3c71d-143">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="3c71d-144">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="3c71d-144">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="3c71d-145">Квалификаторы: [**маппингстрингс**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32API \| Service Structures \| [**\_ Status**](/windows/desktop/api/winsvc/ns-winsvc-service_status) \| двконтролсакцептед \| Service \_ Accept \_ Пауза \_ Continue"), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("служба принимает паузу")</span><span class="sxs-lookup"><span data-stu-id="3c71d-145">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32API\|Service Structures\|[**SERVICE\_STATUS**](/windows/desktop/api/winsvc/ns-winsvc-service_status)\|dwControlsAccepted\|SERVICE\_ACCEPT\_PAUSE\_CONTINUE"), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Service Accepts Pause")</span></span>
</dt> </dl>

<span data-ttu-id="3c71d-146">Служба может быть приостановлена.</span><span class="sxs-lookup"><span data-stu-id="3c71d-146">Service can be paused.</span></span>

</dd> <dt>

<span data-ttu-id="3c71d-147">**AcceptStop**</span><span class="sxs-lookup"><span data-stu-id="3c71d-147">**AcceptStop**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3c71d-148">Тип данных: **логический**</span><span class="sxs-lookup"><span data-stu-id="3c71d-148">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="3c71d-149">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="3c71d-149">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="3c71d-150">Квалификаторы: [**маппингстрингс**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32API \| Service Structures \| [**\_ Status**](/windows/desktop/api/winsvc/ns-winsvc-service_status) \| двконтролсакцептед \| Service \_ Accept \_ "), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("служба принимает" останавливается ").</span><span class="sxs-lookup"><span data-stu-id="3c71d-150">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32API\|Service Structures\|[**SERVICE\_STATUS**](/windows/desktop/api/winsvc/ns-winsvc-service_status)\|dwControlsAccepted\|SERVICE\_ACCEPT\_STOP"), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Service Accepts Stop")</span></span>
</dt> </dl>

<span data-ttu-id="3c71d-151">Служба может быть остановлена.</span><span class="sxs-lookup"><span data-stu-id="3c71d-151">Service can be stopped.</span></span>

</dd> <dt>

<span data-ttu-id="3c71d-152">**Заголовок**</span><span class="sxs-lookup"><span data-stu-id="3c71d-152">**Caption**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3c71d-153">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="3c71d-153">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="3c71d-154">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="3c71d-154">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="3c71d-155">Квалификаторы: [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (64), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Caption")</span><span class="sxs-lookup"><span data-stu-id="3c71d-155">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Caption")</span></span>
</dt> </dl>

<span data-ttu-id="3c71d-156">Краткое описание объекта.</span><span class="sxs-lookup"><span data-stu-id="3c71d-156">Short description of the object.</span></span>

<span data-ttu-id="3c71d-157">Это свойство наследуется от [**CIM \_ манажедсистемелемент**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="3c71d-157">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="3c71d-158">**CreationClassName**</span><span class="sxs-lookup"><span data-stu-id="3c71d-158">**CreationClassName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3c71d-159">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="3c71d-159">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="3c71d-160">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="3c71d-160">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="3c71d-161">Квалификаторы: [**\_ ключ CIM**](/windows/desktop/WmiSdk/standard-wmi-qualifiers), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("имя класса")</span><span class="sxs-lookup"><span data-stu-id="3c71d-161">Qualifiers: [**CIM\_Key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Class Name")</span></span>
</dt> </dl>

<span data-ttu-id="3c71d-162">Имя первого конкретного класса, который будет отображаться в цепочке наследования, используемой при создании экземпляра.</span><span class="sxs-lookup"><span data-stu-id="3c71d-162">Name of the first concrete class to appear in the inheritance chain used in the creation of an instance.</span></span> <span data-ttu-id="3c71d-163">При использовании с другими ключевыми свойствами класса свойство позволяет однозначно идентифицировать все экземпляры этого класса и его подклассов.</span><span class="sxs-lookup"><span data-stu-id="3c71d-163">When used with the other key properties of the class, the property allows all instances of this class and its subclasses to be uniquely identified.</span></span>

<span data-ttu-id="3c71d-164">Это свойство наследуется [**от \_ службы CIM**](cim-service.md).</span><span class="sxs-lookup"><span data-stu-id="3c71d-164">This property is inherited from [**CIM\_Service**](cim-service.md).</span></span>

</dd> <dt>

<span data-ttu-id="3c71d-165">**Описание**</span><span class="sxs-lookup"><span data-stu-id="3c71d-165">**Description**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3c71d-166">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="3c71d-166">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="3c71d-167">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="3c71d-167">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="3c71d-168">Квалификаторы: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Описание")</span><span class="sxs-lookup"><span data-stu-id="3c71d-168">Qualifiers: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Description")</span></span>
</dt> </dl>

<span data-ttu-id="3c71d-169">Описание объекта.</span><span class="sxs-lookup"><span data-stu-id="3c71d-169">Description of the object.</span></span>

<span data-ttu-id="3c71d-170">Это свойство наследуется от [**CIM \_ манажедсистемелемент**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="3c71d-170">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="3c71d-171">**DesktopInteract**</span><span class="sxs-lookup"><span data-stu-id="3c71d-171">**DesktopInteract**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3c71d-172">Тип данных: **логический**</span><span class="sxs-lookup"><span data-stu-id="3c71d-172">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="3c71d-173">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="3c71d-173">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="3c71d-174">Квалификаторы: [**маппингстрингс**](/windows/desktop/WmiSdk/standard-qualifiers) (" \| структуры служб Win32API \| [**запрос \_ \_ конфигурации**](/windows/desktop/api/winsvc/ns-winsvc-query_service_configa)службы \| двсервицетипе \| \_ Интерактивный \_ процесс"), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("взаимодействует с Desktop")</span><span class="sxs-lookup"><span data-stu-id="3c71d-174">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32API\|Service Structures\|[**QUERY\_SERVICE\_CONFIG**](/windows/desktop/api/winsvc/ns-winsvc-query_service_configa)\|dwServiceType\|SERVICE\_INTERACTIVE\_PROCESS"), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Interacts With Desktop")</span></span>
</dt> </dl>

<span data-ttu-id="3c71d-175">Служба может создавать Windows на рабочем столе и взаимодействовать с ними.</span><span class="sxs-lookup"><span data-stu-id="3c71d-175">Service can create or communicate with windows on the desktop.</span></span>

</dd> <dt>

<span data-ttu-id="3c71d-176">**Отображаемое имя**</span><span class="sxs-lookup"><span data-stu-id="3c71d-176">**DisplayName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3c71d-177">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="3c71d-177">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="3c71d-178">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="3c71d-178">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="3c71d-179">Квалификаторы: [**маппингстрингс**](/windows/desktop/WmiSdk/standard-qualifiers) (" \| структуры служб Win32API \| [**запрос \_ \_ конфигурации службы**](/windows/desktop/api/winsvc/ns-winsvc-query_service_configa) \| Лпдисплайнаме"), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("отображаемое имя")</span><span class="sxs-lookup"><span data-stu-id="3c71d-179">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32API\|Service Structures\|[**QUERY\_SERVICE\_CONFIG**](/windows/desktop/api/winsvc/ns-winsvc-query_service_configa)\|lpDisplayName"), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Display Name")</span></span>
</dt> </dl>

<span data-ttu-id="3c71d-180">Отображаемое имя службы.</span><span class="sxs-lookup"><span data-stu-id="3c71d-180">Display name of the service.</span></span> <span data-ttu-id="3c71d-181">Максимальная длина этой строки равна 256 символам.</span><span class="sxs-lookup"><span data-stu-id="3c71d-181">This string has a maximum length of 256 characters.</span></span> <span data-ttu-id="3c71d-182">В диспетчере управления службами имя сохраняется с учетом регистра.</span><span class="sxs-lookup"><span data-stu-id="3c71d-182">The name is case-preserved in the Service Control Manager.</span></span> <span data-ttu-id="3c71d-183">При сравнении **DisplayName** всегда учитывается регистр.</span><span class="sxs-lookup"><span data-stu-id="3c71d-183">Comparisons of **DisplayName** are always case-insensitive.</span></span>

<span data-ttu-id="3c71d-184">Ограничения: принимает то же значение, что и свойство **Name** .</span><span class="sxs-lookup"><span data-stu-id="3c71d-184">Constraints: Accepts the same value as the **Name** property.</span></span>

<span data-ttu-id="3c71d-185">Пример: "Атдиск"</span><span class="sxs-lookup"><span data-stu-id="3c71d-185">Example: "Atdisk"</span></span>

</dd> <dt>

<span data-ttu-id="3c71d-186">**ErrorControl**</span><span class="sxs-lookup"><span data-stu-id="3c71d-186">**ErrorControl**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3c71d-187">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="3c71d-187">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="3c71d-188">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="3c71d-188">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="3c71d-189">Квалификаторы: [**маппингстрингс**](/windows/desktop/WmiSdk/standard-qualifiers) (" \| структуры служб Win32API \| [**запрос \_ \_ конфигурации службы**](/windows/desktop/api/winsvc/ns-winsvc-query_service_configa) \| Дверрорконтрол"), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("серьезность сбоя при запуске")</span><span class="sxs-lookup"><span data-stu-id="3c71d-189">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32API\|Service Structures\|[**QUERY\_SERVICE\_CONFIG**](/windows/desktop/api/winsvc/ns-winsvc-query_service_configa)\|dwErrorControl"), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Severity Of Startup Failure")</span></span>
</dt> </dl>

<span data-ttu-id="3c71d-190">Серьезность ошибки.</span><span class="sxs-lookup"><span data-stu-id="3c71d-190">Severity of the error.</span></span> <span data-ttu-id="3c71d-191">Не удается запустить службу.</span><span class="sxs-lookup"><span data-stu-id="3c71d-191">Service fails to start.</span></span> <span data-ttu-id="3c71d-192">Значение указывает действие, предпринимаемое программой запуска, если происходит сбой.</span><span class="sxs-lookup"><span data-stu-id="3c71d-192">The value indicates the action taken by the startup program if failure occurs.</span></span> <span data-ttu-id="3c71d-193">Все ошибки записываются в журнал системой компьютера.</span><span class="sxs-lookup"><span data-stu-id="3c71d-193">All errors are logged by the computer system.</span></span>

<dt>

<span id="Ignore"></span><span id="ignore"></span><span id="IGNORE"></span>

<span data-ttu-id="3c71d-194"><span id="Ignore"></span><span id="ignore"></span><span id="IGNORE"></span>**Игнорировать** ("ignore")</span><span class="sxs-lookup"><span data-stu-id="3c71d-194"><span id="Ignore"></span><span id="ignore"></span><span id="IGNORE"></span>**Ignore** ("Ignore")</span></span>


</dt> <dd>

<span data-ttu-id="3c71d-195">Пользователь не получает уведомление.</span><span class="sxs-lookup"><span data-stu-id="3c71d-195">User is not notified.</span></span>

</dd> <dt>

<span id="Normal"></span><span id="normal"></span><span id="NORMAL"></span>

<span data-ttu-id="3c71d-196"><span id="Normal"></span><span id="normal"></span><span id="NORMAL"></span>**Обычная** ("Обычная")</span><span class="sxs-lookup"><span data-stu-id="3c71d-196"><span id="Normal"></span><span id="normal"></span><span id="NORMAL"></span>**Normal** ("Normal")</span></span>


</dt> <dd>

<span data-ttu-id="3c71d-197">Пользователь получает уведомление.</span><span class="sxs-lookup"><span data-stu-id="3c71d-197">User is notified.</span></span>

</dd> <dt>

<span id="Severe"></span><span id="severe"></span><span id="SEVERE"></span>

<span data-ttu-id="3c71d-198"><span id="Severe"></span><span id="severe"></span><span id="SEVERE"></span>**Серьезная** ("серьезная")</span><span class="sxs-lookup"><span data-stu-id="3c71d-198"><span id="Severe"></span><span id="severe"></span><span id="SEVERE"></span>**Severe** ("Severe")</span></span>


</dt> <dd>

<span data-ttu-id="3c71d-199">Система перезапущена с последней удачной конфигурацией.</span><span class="sxs-lookup"><span data-stu-id="3c71d-199">System restarted with the last-known-good configuration.</span></span>

</dd> <dt>

<span id="Critical"></span><span id="critical"></span><span id="CRITICAL"></span>

<span data-ttu-id="3c71d-200"><span id="Critical"></span><span id="critical"></span><span id="CRITICAL"></span>**Критическая** ("критическая")</span><span class="sxs-lookup"><span data-stu-id="3c71d-200"><span id="Critical"></span><span id="critical"></span><span id="CRITICAL"></span>**Critical** ("Critical")</span></span>


</dt> <dd>

<span data-ttu-id="3c71d-201">Попытка перезапустить систему в рабочей конфигурации.</span><span class="sxs-lookup"><span data-stu-id="3c71d-201">System attempts to restart with a good configuration.</span></span>

</dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="3c71d-202"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Неизвестно** ("неизвестно")</span><span class="sxs-lookup"><span data-stu-id="3c71d-202"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** ("Unknown")</span></span>


</dt> <dd>

<span data-ttu-id="3c71d-203">Не указано действие, которое было принято.</span><span class="sxs-lookup"><span data-stu-id="3c71d-203">Action taken is unspecified.</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="3c71d-204">**ExitCode**</span><span class="sxs-lookup"><span data-stu-id="3c71d-204">**ExitCode**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3c71d-205">Тип данных: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="3c71d-205">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="3c71d-206">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="3c71d-206">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="3c71d-207">Квалификаторы: [**маппингстрингс**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32API \| Service Structures \| [**\_ Status**](/windows/desktop/api/winsvc/ns-winsvc-service_status) \| DwWin32ExitCode"), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("код выхода")</span><span class="sxs-lookup"><span data-stu-id="3c71d-207">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32API\|Service Structures\|[**SERVICE\_STATUS**](/windows/desktop/api/winsvc/ns-winsvc-service_status)\|dwWin32ExitCode"), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Exit Code")</span></span>
</dt> </dl>

<span data-ttu-id="3c71d-208">Определение любых проблем, возникших при запуске или остановке службы.</span><span class="sxs-lookup"><span data-stu-id="3c71d-208">Defining any problems encountered in starting or stopping the service.</span></span> <span data-ttu-id="3c71d-209">Это свойство имеет значение ошибка, связанное со **\_ службой \_ \_ ошибок** (1066), если ошибка является уникальной для службы, представленной этим классом, а сведения об ошибке доступны в свойстве **сервицеспеЦифицекситкоде** .</span><span class="sxs-lookup"><span data-stu-id="3c71d-209">This property is set to **ERROR\_SERVICE\_SPECIFIC\_ERROR** (1066) when the error is unique to the service represented by this class, and information about the error is available in the **ServiceSpecificExitCode** property.</span></span> <span data-ttu-id="3c71d-210">Служба задает это значение **без \_ ошибок** при выполнении и снова после нормального завершения.</span><span class="sxs-lookup"><span data-stu-id="3c71d-210">The service sets this value to **NO\_ERROR** when running, and again upon normal termination.</span></span>

</dd> <dt>

<span data-ttu-id="3c71d-211">**InstallDate**</span><span class="sxs-lookup"><span data-stu-id="3c71d-211">**InstallDate**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3c71d-212">Тип данных: **DateTime**</span><span class="sxs-lookup"><span data-stu-id="3c71d-212">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="3c71d-213">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="3c71d-213">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="3c71d-214">Квалификаторы: [**маппингстрингс**](/windows/desktop/WmiSdk/standard-qualifiers) (MIF. DMTF \| ComponentID \| 001,5 "), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) (" Дата установки ")</span><span class="sxs-lookup"><span data-stu-id="3c71d-214">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|ComponentID\|001.5"), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Install Date")</span></span>
</dt> </dl>

<span data-ttu-id="3c71d-215">Объект был установлен.</span><span class="sxs-lookup"><span data-stu-id="3c71d-215">Object was installed.</span></span> <span data-ttu-id="3c71d-216">Для этого свойства не требуется значение, указывающее, что объект установлен.</span><span class="sxs-lookup"><span data-stu-id="3c71d-216">This property does not need a value to indicate that the object is installed.</span></span>

<span data-ttu-id="3c71d-217">Это свойство наследуется от [**CIM \_ манажедсистемелемент**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="3c71d-217">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="3c71d-218">**Name**</span><span class="sxs-lookup"><span data-stu-id="3c71d-218">**Name**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3c71d-219">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="3c71d-219">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="3c71d-220">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="3c71d-220">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="3c71d-221">Квалификаторы: [ **ключ**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="3c71d-221">Qualifiers: [**Key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

<span data-ttu-id="3c71d-222">Уникальный идентификатор службы, который предоставляет сведения об управляемых функциях.</span><span class="sxs-lookup"><span data-stu-id="3c71d-222">Unique identifier of the service, which provides an indication of the functionality that is managed.</span></span> <span data-ttu-id="3c71d-223">Эти функциональные возможности более подробно описаны в свойстве « **Описание** » объекта.</span><span class="sxs-lookup"><span data-stu-id="3c71d-223">This functionality is described in more detail in the object's **Description** property.</span></span>

<span data-ttu-id="3c71d-224">Это свойство наследуется от [**CIM \_ манажедсистемелемент**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="3c71d-224">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="3c71d-225">**PathName**</span><span class="sxs-lookup"><span data-stu-id="3c71d-225">**PathName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3c71d-226">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="3c71d-226">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="3c71d-227">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="3c71d-227">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="3c71d-228">Квалификаторы: [**маппингстрингс**](/windows/desktop/WmiSdk/standard-qualifiers) (" \| структуры служб Win32API \| [**запрос \_ \_ конфигурации**](/windows/desktop/api/winsvc/ns-winsvc-query_service_configa) \| Лпбинарипаснаме"), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("имя пути к файлу")</span><span class="sxs-lookup"><span data-stu-id="3c71d-228">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32API\|Service Structures\|[**QUERY\_SERVICE\_CONFIG**](/windows/desktop/api/winsvc/ns-winsvc-query_service_configa)\|lpBinaryPathName"), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("File Path Name")</span></span>
</dt> </dl>

<span data-ttu-id="3c71d-229">Полный путь к двоичному файлу службы, реализующему службу.</span><span class="sxs-lookup"><span data-stu-id="3c71d-229">Fully qualified path to the service binary file that implements the service.</span></span>

<span data-ttu-id="3c71d-230">Пример: " \\ СистемныйКорневойКаталог \\ system32 \\ Drivers \\afd.sys"</span><span class="sxs-lookup"><span data-stu-id="3c71d-230">Example: "\\SystemRoot\\System32\\drivers\\afd.sys"</span></span>

</dd> <dt>

<span data-ttu-id="3c71d-231">**сервицеспеЦифицекситкоде**</span><span class="sxs-lookup"><span data-stu-id="3c71d-231">**ServiceSpecificExitCode**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3c71d-232">Тип данных: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="3c71d-232">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="3c71d-233">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="3c71d-233">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="3c71d-234">Квалификаторы: [**маппингстрингс**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32API \| Service Structures \| [**\_ Status**](/windows/desktop/api/winsvc/ns-winsvc-service_status) \| двсервицеспеЦифицекситкоде"), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("специфический для сервера код выхода")</span><span class="sxs-lookup"><span data-stu-id="3c71d-234">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32API\|Service Structures\|[**SERVICE\_STATUS**](/windows/desktop/api/winsvc/ns-winsvc-service_status)\|dwServiceSpecificExitCode"), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Server Specific Exit Code")</span></span>
</dt> </dl>

<span data-ttu-id="3c71d-235">Код ошибки, зависящей от службы, для ошибок, возникающих во время запуска или остановки службы.</span><span class="sxs-lookup"><span data-stu-id="3c71d-235">Service-specific error code for errors that occur while the service is either starting or stopping.</span></span> <span data-ttu-id="3c71d-236">Коды выхода определяются службой, представленной этим классом.</span><span class="sxs-lookup"><span data-stu-id="3c71d-236">The exit codes are defined by the service represented by this class.</span></span> <span data-ttu-id="3c71d-237">Это значение задается только в том случае, если значение **екситкодепроперти** является **\_ \_ \_ ошибкой службы, характерной для ошибки** (1066).</span><span class="sxs-lookup"><span data-stu-id="3c71d-237">This value is only set when the **ExitCodeproperty** value is **ERROR\_SERVICE\_SPECIFIC\_ERROR** (1066).</span></span>

</dd> <dt>

<span data-ttu-id="3c71d-238">**ServiceType**</span><span class="sxs-lookup"><span data-stu-id="3c71d-238">**ServiceType**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3c71d-239">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="3c71d-239">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="3c71d-240">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="3c71d-240">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="3c71d-241">Квалификаторы: [**маппингстрингс**](/windows/desktop/WmiSdk/standard-qualifiers) (" \| структуры служб Win32API \| [**запрос \_ \_ конфигурации службы**](/windows/desktop/api/winsvc/ns-winsvc-query_service_configa) \| двсервицетипе"), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("тип службы")</span><span class="sxs-lookup"><span data-stu-id="3c71d-241">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32API\|Service Structures\|[**QUERY\_SERVICE\_CONFIG**](/windows/desktop/api/winsvc/ns-winsvc-query_service_configa)\|dwServiceType"), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Service Type")</span></span>
</dt> </dl>

<span data-ttu-id="3c71d-242">Служба, предоставляемая для вызова процессов.</span><span class="sxs-lookup"><span data-stu-id="3c71d-242">Service provided to calling processes.</span></span>

<dt>

<span id="Kernel_Driver"></span><span id="kernel_driver"></span><span id="KERNEL_DRIVER"></span>

<span data-ttu-id="3c71d-243">**Драйвер ядра** ("драйвер ядра")</span><span class="sxs-lookup"><span data-stu-id="3c71d-243">**Kernel Driver** ("Kernel Driver")</span></span>


</dt> <dd></dd> <dt>

<span id="File_System_Driver"></span><span id="file_system_driver"></span><span id="FILE_SYSTEM_DRIVER"></span>

<span data-ttu-id="3c71d-244">**Драйвер файловой системы** ("драйвер файловой системы")</span><span class="sxs-lookup"><span data-stu-id="3c71d-244">**File System Driver** ("File System Driver")</span></span>


</dt> <dd></dd> <dt>

<span id="Adapter"></span><span id="adapter"></span><span id="ADAPTER"></span>

<span data-ttu-id="3c71d-245">**Адаптер** ("адаптер")</span><span class="sxs-lookup"><span data-stu-id="3c71d-245">**Adapter** ("Adapter")</span></span>


</dt> <dd></dd> <dt>

<span id="Recognizer_Driver"></span><span id="recognizer_driver"></span><span id="RECOGNIZER_DRIVER"></span>

<span data-ttu-id="3c71d-246">**Драйвер распознавателя** ("драйвер распознавателя")</span><span class="sxs-lookup"><span data-stu-id="3c71d-246">**Recognizer Driver** ("Recognizer Driver")</span></span>


</dt> <dd></dd> <dt>

<span id="Own_Process"></span><span id="own_process"></span><span id="OWN_PROCESS"></span>

<span data-ttu-id="3c71d-247">**Собственный процесс** ("собственный процесс")</span><span class="sxs-lookup"><span data-stu-id="3c71d-247">**Own Process** ("Own Process")</span></span>


</dt> <dd></dd> <dt>

<span id="Share_Process"></span><span id="share_process"></span><span id="SHARE_PROCESS"></span>

<span data-ttu-id="3c71d-248">**Общий процесс** ("общий процесс")</span><span class="sxs-lookup"><span data-stu-id="3c71d-248">**Share Process** ("Share Process")</span></span>


</dt> <dd></dd> <dt>

<span id="Interactive_Process"></span><span id="interactive_process"></span><span id="INTERACTIVE_PROCESS"></span>

<span data-ttu-id="3c71d-249">**Интерактивный процесс** (интерактивный процесс)</span><span class="sxs-lookup"><span data-stu-id="3c71d-249">**Interactive Process** ("Interactive Process")</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="3c71d-250">**Запуск**</span><span class="sxs-lookup"><span data-stu-id="3c71d-250">**Started**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3c71d-251">Тип данных: **логический**</span><span class="sxs-lookup"><span data-stu-id="3c71d-251">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="3c71d-252">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="3c71d-252">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="3c71d-253">Квалификаторы: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("запущено")</span><span class="sxs-lookup"><span data-stu-id="3c71d-253">Qualifiers: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Started")</span></span>
</dt> </dl>

<span data-ttu-id="3c71d-254">Служба запущена.</span><span class="sxs-lookup"><span data-stu-id="3c71d-254">Service has been started.</span></span>

<span data-ttu-id="3c71d-255">Это свойство наследуется [**от \_ службы CIM**](cim-service.md).</span><span class="sxs-lookup"><span data-stu-id="3c71d-255">This property is inherited from [**CIM\_Service**](cim-service.md).</span></span>

</dd> <dt>

<span data-ttu-id="3c71d-256">**StartMode**</span><span class="sxs-lookup"><span data-stu-id="3c71d-256">**StartMode**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3c71d-257">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="3c71d-257">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="3c71d-258">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="3c71d-258">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="3c71d-259">Квалификаторы: [**override**](/windows/desktop/WmiSdk/standard-qualifiers) ("StartMode"), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("режим запуска")</span><span class="sxs-lookup"><span data-stu-id="3c71d-259">Qualifiers: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("StartMode"), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Start Mode")</span></span>
</dt> </dl>

<span data-ttu-id="3c71d-260">Режим запуска базовой службы Windows.</span><span class="sxs-lookup"><span data-stu-id="3c71d-260">Start mode of the Windows base service.</span></span>

<span data-ttu-id="3c71d-261">Это свойство наследуется [**от \_ службы CIM**](cim-service.md).</span><span class="sxs-lookup"><span data-stu-id="3c71d-261">This property is inherited from [**CIM\_Service**](cim-service.md).</span></span>

<dt>

<span id="Boot"></span><span id="boot"></span><span id="BOOT"></span>

<span data-ttu-id="3c71d-262"><span id="Boot"></span><span id="boot"></span><span id="BOOT"></span>**Boot** (Загрузка)</span><span class="sxs-lookup"><span data-stu-id="3c71d-262"><span id="Boot"></span><span id="boot"></span><span id="BOOT"></span>**Boot** ("Boot")</span></span>


</dt> <dd>

<span data-ttu-id="3c71d-263">Драйвер устройства запущен загрузчиком операционной системы (действует только для служб драйверов).</span><span class="sxs-lookup"><span data-stu-id="3c71d-263">Device driver started by the operating system loader (valid only for driver services).</span></span>

</dd> <dt>

<span id="System"></span><span id="system"></span><span id="SYSTEM"></span>

<span data-ttu-id="3c71d-264"><span id="System"></span><span id="system"></span><span id="SYSTEM"></span>**Система** ("System")</span><span class="sxs-lookup"><span data-stu-id="3c71d-264"><span id="System"></span><span id="system"></span><span id="SYSTEM"></span>**System** ("System")</span></span>


</dt> <dd>

<span data-ttu-id="3c71d-265">Драйвер устройства запущен процессом инициализации операционной системы.</span><span class="sxs-lookup"><span data-stu-id="3c71d-265">Device driver started by the operating system initialization process.</span></span> <span data-ttu-id="3c71d-266">Это значение допустимо только для служб драйверов.</span><span class="sxs-lookup"><span data-stu-id="3c71d-266">This value is valid only for driver services.</span></span>

</dd> <dt>

<span id="Auto"></span><span id="auto"></span><span id="AUTO"></span>

<span data-ttu-id="3c71d-267"><span id="Auto"></span><span id="auto"></span><span id="AUTO"></span>**Авто** ("Auto")</span><span class="sxs-lookup"><span data-stu-id="3c71d-267"><span id="Auto"></span><span id="auto"></span><span id="AUTO"></span>**Auto** ("Auto")</span></span>


</dt> <dd>

<span data-ttu-id="3c71d-268">Служба запускается автоматически диспетчером управления службами во время запуска системы.</span><span class="sxs-lookup"><span data-stu-id="3c71d-268">Service to be started automatically by the service control manager during system start up.</span></span>

</dd> <dt>

<span id="Manual"></span><span id="manual"></span><span id="MANUAL"></span>

<span data-ttu-id="3c71d-269"><span id="Manual"></span><span id="manual"></span><span id="MANUAL"></span>**Вручную** ("вручную")</span><span class="sxs-lookup"><span data-stu-id="3c71d-269"><span id="Manual"></span><span id="manual"></span><span id="MANUAL"></span>**Manual** ("Manual")</span></span>


</dt> <dd>

<span data-ttu-id="3c71d-270">Служба, запускаемая диспетчером управления службами, когда процесс вызывает метод [**StartService**](startservice-method-in-class-win32-baseservice.md) .</span><span class="sxs-lookup"><span data-stu-id="3c71d-270">Service to be started by the service control manager when a process calls the [**StartService**](startservice-method-in-class-win32-baseservice.md) method.</span></span>

</dd> <dt>

<span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>

<span data-ttu-id="3c71d-271"><span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>**Отключено** ("отключено")</span><span class="sxs-lookup"><span data-stu-id="3c71d-271"><span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>**Disabled** ("Disabled")</span></span>


</dt> <dd>

<span data-ttu-id="3c71d-272">Служба, которая больше не может быть запущена.</span><span class="sxs-lookup"><span data-stu-id="3c71d-272">Service that can no longer be started.</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="3c71d-273">**StartName**</span><span class="sxs-lookup"><span data-stu-id="3c71d-273">**StartName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3c71d-274">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="3c71d-274">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="3c71d-275">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="3c71d-275">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="3c71d-276">Квалификаторы: [**маппингстрингс**](/windows/desktop/WmiSdk/standard-qualifiers) (" \| структуры служб Win32API \| [**запрос \_ \_ конфигурации службы**](/windows/desktop/api/winsvc/ns-winsvc-query_service_configa) \| Лпсервицестартнаме"), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("начальное имя учетной записи")</span><span class="sxs-lookup"><span data-stu-id="3c71d-276">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32API\|Service Structures\|[**QUERY\_SERVICE\_CONFIG**](/windows/desktop/api/winsvc/ns-winsvc-query_service_configa)\|lpServiceStartName"), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Starting Account Name")</span></span>
</dt> </dl>

<span data-ttu-id="3c71d-277">Имя учетной записи, под которой выполняется служба.</span><span class="sxs-lookup"><span data-stu-id="3c71d-277">Account name under which the service runs.</span></span> <span data-ttu-id="3c71d-278">В зависимости от типа службы имя учетной записи может быть указано в \\ формате имя_домена имя пользователя или имя участника-пользователя ( Username@DomainName ).</span><span class="sxs-lookup"><span data-stu-id="3c71d-278">Depending on the service type, the account name may be in the form of "DomainName\\Username" or UPN format (Username@DomainName).</span></span> <span data-ttu-id="3c71d-279">Процесс службы будет заноситься в журнал с использованием одной из этих двух форм при запуске.</span><span class="sxs-lookup"><span data-stu-id="3c71d-279">The service process will be logged using one of these two forms when it runs.</span></span> <span data-ttu-id="3c71d-280">Если учетная запись принадлежит к встроенному домену, ". \\ Можно указать имя пользователя.</span><span class="sxs-lookup"><span data-stu-id="3c71d-280">If the account belongs to the built-in domain, ".\\Username" can be specified.</span></span> <span data-ttu-id="3c71d-281">Если указано **значение NULL** , служба будет входить в систему как учетная запись LocalSystem.</span><span class="sxs-lookup"><span data-stu-id="3c71d-281">If **NULL** is specified, the service will be logged on as the LocalSystem account.</span></span> <span data-ttu-id="3c71d-282">Для драйверов ядра или системного уровня **StartName** содержит имя объекта драйвера (то есть \\ FileSystem \\ RDR или \\ Driver \\ КСНС), которое используется системой ввода и вывода для загрузки драйвера устройства.</span><span class="sxs-lookup"><span data-stu-id="3c71d-282">For kernel or system-level drivers, **StartName** contains the driver object name (that is, \\FileSystem\\Rdr or \\Driver\\Xns) which the input and output (I/O) system uses to load the device driver.</span></span> <span data-ttu-id="3c71d-283">Кроме того, если указано **значение NULL** , драйвер запускается с именем объекта по умолчанию, созданным системой ввода-вывода на основе имени службы.</span><span class="sxs-lookup"><span data-stu-id="3c71d-283">Additionally, if **NULL** is specified, the driver runs with a default object name created by the I/O system based on the service name.</span></span> <span data-ttu-id="3c71d-284">Пример: "ДВДОМ \\ Admin".</span><span class="sxs-lookup"><span data-stu-id="3c71d-284">Example: "DWDOM\\Admin".</span></span>

</dd> <dt>

<span data-ttu-id="3c71d-285">**Состояние**</span><span class="sxs-lookup"><span data-stu-id="3c71d-285">**State**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3c71d-286">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="3c71d-286">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="3c71d-287">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="3c71d-287">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="3c71d-288">Квалификаторы: [**маппингстрингс**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32API \| Service Structures \| [**\_ Status**](/windows/desktop/api/winsvc/ns-winsvc-service_status) \| двкуррентстате"), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("State")</span><span class="sxs-lookup"><span data-stu-id="3c71d-288">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32API\|Service Structures\|[**SERVICE\_STATUS**](/windows/desktop/api/winsvc/ns-winsvc-service_status)\|dwCurrentState "), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("State")</span></span>
</dt> </dl>

<span data-ttu-id="3c71d-289">Текущее состояние базовой службы.</span><span class="sxs-lookup"><span data-stu-id="3c71d-289">Current state of the base service.</span></span>

<dt>

<span id="Stopped"></span><span id="stopped"></span><span id="STOPPED"></span>

<span data-ttu-id="3c71d-290">**Остановлено** ("остановлено")</span><span class="sxs-lookup"><span data-stu-id="3c71d-290">**Stopped** ("Stopped")</span></span>


</dt> <dd></dd> <dt>

<span id="Start_Pending"></span><span id="start_pending"></span><span id="START_PENDING"></span>

<span data-ttu-id="3c71d-291">**Ожидание запуска** ("Ожидание запуска")</span><span class="sxs-lookup"><span data-stu-id="3c71d-291">**Start Pending** ("Start Pending")</span></span>


</dt> <dd></dd> <dt>

<span id="Stop_Pending"></span><span id="stop_pending"></span><span id="STOP_PENDING"></span>

<span data-ttu-id="3c71d-292">**Ожидание ожидания** ("ожидание завершения")</span><span class="sxs-lookup"><span data-stu-id="3c71d-292">**Stop Pending** ("Stop Pending")</span></span>


</dt> <dd></dd> <dt>

<span id="Running"></span><span id="running"></span><span id="RUNNING"></span>

<span data-ttu-id="3c71d-293">**Работает** ("работает")</span><span class="sxs-lookup"><span data-stu-id="3c71d-293">**Running** ("Running")</span></span>


</dt> <dd></dd> <dt>

<span id="Continue_Pending"></span><span id="continue_pending"></span><span id="CONTINUE_PENDING"></span>

<span data-ttu-id="3c71d-294">**Ожидание продолжения** ("Ожидание продолжения")</span><span class="sxs-lookup"><span data-stu-id="3c71d-294">**Continue Pending** ("Continue Pending")</span></span>


</dt> <dd></dd> <dt>

<span id="Pause_Pending"></span><span id="pause_pending"></span><span id="PAUSE_PENDING"></span>

<span data-ttu-id="3c71d-295">**Ожидание приостановки** ("ожидание приостановки")</span><span class="sxs-lookup"><span data-stu-id="3c71d-295">**Pause Pending** ("Pause Pending")</span></span>


</dt> <dd></dd> <dt>

<span id="Paused"></span><span id="paused"></span><span id="PAUSED"></span>

<span data-ttu-id="3c71d-296">**Приостановлено** ("приостановлено")</span><span class="sxs-lookup"><span data-stu-id="3c71d-296">**Paused** ("Paused")</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="3c71d-297">**Неизвестно** ("неизвестно")</span><span class="sxs-lookup"><span data-stu-id="3c71d-297">**Unknown** ("Unknown")</span></span>


<span data-ttu-id="3c71d-298"></dt> <dd></dd> </dl></span><span class="sxs-lookup"><span data-stu-id="3c71d-298"></dt> <dd></dd> </dl></span></span>

<span data-ttu-id="3c71d-299">**Windows Server 2008 и Windows Vista:** Это свойство доступно только для чтения.</span><span class="sxs-lookup"><span data-stu-id="3c71d-299">**Windows Server 2008 and Windows Vista:** This property is read-only.</span></span>

</dd> <dt>

<span data-ttu-id="3c71d-300">**Состояние**</span><span class="sxs-lookup"><span data-stu-id="3c71d-300">**Status**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3c71d-301">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="3c71d-301">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="3c71d-302">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="3c71d-302">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="3c71d-303">Квалификаторы: [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (10), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("состояние")</span><span class="sxs-lookup"><span data-stu-id="3c71d-303">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (10), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Status")</span></span>
</dt> </dl>

<span data-ttu-id="3c71d-304">Текущее состояние объекта.</span><span class="sxs-lookup"><span data-stu-id="3c71d-304">Current status of the object.</span></span> <span data-ttu-id="3c71d-305">Можно определить различные операционные и неоперационные состояния.</span><span class="sxs-lookup"><span data-stu-id="3c71d-305">Various operational and nonoperational statuses can be defined.</span></span> <span data-ttu-id="3c71d-306">Рабочие состояния включают: "ОК", "деградация" и "пред-ошибка" (элемент, например жесткий диск с поддержкой SMART, может работать правильно, но прогнозировать сбой в ближайшем будущем).</span><span class="sxs-lookup"><span data-stu-id="3c71d-306">Operational statuses include: "OK", "Degraded", and "Pred Fail" (an element, such as a SMART-enabled hard disk drive, may be functioning properly but predicting a failure in the near future).</span></span> <span data-ttu-id="3c71d-307">Неработающие состояния включают: "ошибка", "Запуск", "остановка" и "служба".</span><span class="sxs-lookup"><span data-stu-id="3c71d-307">Nonoperational statuses include: "Error", "Starting", "Stopping", and "Service".</span></span> <span data-ttu-id="3c71d-308">Последняя, «служба», может применяться во время зеркального копирования диска, перезагрузки списка разрешений пользователя или другой административной работы.</span><span class="sxs-lookup"><span data-stu-id="3c71d-308">The latter, "Service", could apply during mirror-resilvering of a disk, reload of a user permissions list, or other administrative work.</span></span> <span data-ttu-id="3c71d-309">Не вся такая работа находится в оперативном режиме, но управляемый элемент не является ни "ОК", ни одним из других состояний.</span><span class="sxs-lookup"><span data-stu-id="3c71d-309">Not all such work is online, yet the managed element is neither "OK" nor in one of the other states.</span></span>

<span data-ttu-id="3c71d-310">Это свойство наследуется от [**CIM \_ манажедсистемелемент**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="3c71d-310">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

<span data-ttu-id="3c71d-311">В эти значения входят:</span><span class="sxs-lookup"><span data-stu-id="3c71d-311">Values include the following:</span></span>

<dt>

<span id="OK"></span><span id="ok"></span>

<span data-ttu-id="3c71d-312">**ОК** ("ОК")</span><span class="sxs-lookup"><span data-stu-id="3c71d-312">**OK** ("OK")</span></span>


</dt> <dd></dd> <dt>

<span id="Error"></span><span id="error"></span><span id="ERROR"></span>

<span data-ttu-id="3c71d-313">**Ошибка** ("ошибка")</span><span class="sxs-lookup"><span data-stu-id="3c71d-313">**Error** ("Error")</span></span>


</dt> <dd></dd> <dt>

<span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>

<span data-ttu-id="3c71d-314">**Пониженная работоспособность** (пониженная работоспособность)</span><span class="sxs-lookup"><span data-stu-id="3c71d-314">**Degraded** ("Degraded")</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="3c71d-315">**Неизвестно** ("неизвестно")</span><span class="sxs-lookup"><span data-stu-id="3c71d-315">**Unknown** ("Unknown")</span></span>


</dt> <dd></dd> <dt>

<span id="Pred_Fail"></span><span id="pred_fail"></span><span id="PRED_FAIL"></span>

<span data-ttu-id="3c71d-316">**Пред-ошибка** ("пред Fail")</span><span class="sxs-lookup"><span data-stu-id="3c71d-316">**Pred Fail** ("Pred Fail")</span></span>


</dt> <dd></dd> <dt>

<span id="Starting"></span><span id="starting"></span><span id="STARTING"></span>

<span data-ttu-id="3c71d-317">**Запуск** ("Запуск")</span><span class="sxs-lookup"><span data-stu-id="3c71d-317">**Starting** ("Starting")</span></span>


</dt> <dd></dd> <dt>

<span id="Stopping"></span><span id="stopping"></span><span id="STOPPING"></span>

<span data-ttu-id="3c71d-318">**Остановка** ("остановка")</span><span class="sxs-lookup"><span data-stu-id="3c71d-318">**Stopping** ("Stopping")</span></span>


</dt> <dd></dd> <dt>

<span id="Service"></span><span id="service"></span><span id="SERVICE"></span>

<span data-ttu-id="3c71d-319">**Служба** ("служба")</span><span class="sxs-lookup"><span data-stu-id="3c71d-319">**Service** ("Service")</span></span>


</dt> <dd></dd> <dt>

<span id="Stressed"></span><span id="stressed"></span><span id="STRESSED"></span>

<span data-ttu-id="3c71d-320">**Пренапряжению** ("напряжению")</span><span class="sxs-lookup"><span data-stu-id="3c71d-320">**Stressed** ("Stressed")</span></span>


</dt> <dd></dd> <dt>

<span id="NonRecover"></span><span id="nonrecover"></span><span id="NONRECOVER"></span>

<span data-ttu-id="3c71d-321">**Невосстановление** ("невосстановление")</span><span class="sxs-lookup"><span data-stu-id="3c71d-321">**NonRecover** ("NonRecover")</span></span>


</dt> <dd></dd> <dt>

<span id="No_Contact"></span><span id="no_contact"></span><span id="NO_CONTACT"></span>

<span data-ttu-id="3c71d-322">**Нет контакта** ("нет контакта")</span><span class="sxs-lookup"><span data-stu-id="3c71d-322">**No Contact** ("No Contact")</span></span>


</dt> <dd></dd> <dt>

<span id="Lost_Comm"></span><span id="lost_comm"></span><span id="LOST_COMM"></span>

<span data-ttu-id="3c71d-323">**Потеря** связи ("потеря связи")</span><span class="sxs-lookup"><span data-stu-id="3c71d-323">**Lost Comm** ("Lost Comm")</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="3c71d-324">**системкреатионкласснаме**</span><span class="sxs-lookup"><span data-stu-id="3c71d-324">**SystemCreationClassName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3c71d-325">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="3c71d-325">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="3c71d-326">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="3c71d-326">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="3c71d-327">Квалификаторы: [**распространено**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**\_ система CIM**](cim-system.md).**CreationClassName**"), [**\_ ключ CIM**](/windows/desktop/WmiSdk/standard-wmi-qualifiers), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) (" имя класса системы ")</span><span class="sxs-lookup"><span data-stu-id="3c71d-327">Qualifiers: [**Propagated**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM\_System**](cim-system.md).**CreationClassName**"), [**CIM\_Key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("System Class Name")</span></span>
</dt> </dl>

<span data-ttu-id="3c71d-328">Имя типа системы, в которой размещена эта служба.</span><span class="sxs-lookup"><span data-stu-id="3c71d-328">Type name of the system that hosts this service.</span></span>

<span data-ttu-id="3c71d-329">Это свойство наследуется [**от \_ службы CIM**](cim-service.md).</span><span class="sxs-lookup"><span data-stu-id="3c71d-329">This property is inherited from [**CIM\_Service**](cim-service.md).</span></span>

</dd> <dt>

<span data-ttu-id="3c71d-330">**SystemName**</span><span class="sxs-lookup"><span data-stu-id="3c71d-330">**SystemName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3c71d-331">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="3c71d-331">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="3c71d-332">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="3c71d-332">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="3c71d-333">Квалификаторы: [**распространено**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**\_ система CIM**](cim-system.md).**Name**"), [**\_ ключ CIM**](/windows/desktop/WmiSdk/standard-wmi-qualifiers), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) (" System Name ")</span><span class="sxs-lookup"><span data-stu-id="3c71d-333">Qualifiers: [**Propagated**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM\_System**](cim-system.md).**Name**"), [**CIM\_Key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("System Name")</span></span>
</dt> </dl>

<span data-ttu-id="3c71d-334">Имя системы, в которой размещена эта служба.</span><span class="sxs-lookup"><span data-stu-id="3c71d-334">Name of the system that hosts this service.</span></span>

<span data-ttu-id="3c71d-335">Это свойство наследуется [**от \_ службы CIM**](cim-service.md).</span><span class="sxs-lookup"><span data-stu-id="3c71d-335">This property is inherited from [**CIM\_Service**](cim-service.md).</span></span>

</dd> <dt>

<span data-ttu-id="3c71d-336">**TagId**</span><span class="sxs-lookup"><span data-stu-id="3c71d-336">**TagId**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3c71d-337">Тип данных: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="3c71d-337">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="3c71d-338">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="3c71d-338">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="3c71d-339">Квалификаторы: [**маппингстрингс**](/windows/desktop/WmiSdk/standard-qualifiers) (" \| структуры служб Win32API \| [**запрос \_ \_ конфигурации**](/windows/desktop/api/winsvc/ns-winsvc-query_service_configa) \| двтагид"), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("идентификатор тега")</span><span class="sxs-lookup"><span data-stu-id="3c71d-339">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32API\|Service Structures\|[**QUERY\_SERVICE\_CONFIG**](/windows/desktop/api/winsvc/ns-winsvc-query_service_configa)\|dwTagId"), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Tag Id")</span></span>
</dt> </dl>

<span data-ttu-id="3c71d-340">Уникальное значение тега для этой службы в группе.</span><span class="sxs-lookup"><span data-stu-id="3c71d-340">Unique tag value for this service in the group.</span></span> <span data-ttu-id="3c71d-341">Значение 0 (ноль) указывает, что службе не назначен тег.</span><span class="sxs-lookup"><span data-stu-id="3c71d-341">A value of 0 (zero) indicates that the service has not been assigned a tag.</span></span> <span data-ttu-id="3c71d-342">Тег можно использовать для упорядочивания службы Star тройки в группе порядка загрузки, указав в реестре вектор порядка тегов, расположенный в папке: HKEY \_ локальный \_ компьютер \\ System \\ CurrentControlSet \\ Control \\ граупордерлист.</span><span class="sxs-lookup"><span data-stu-id="3c71d-342">A tag can be used for ordering service star tup within a load order group by specifying a tag order vector in the registry located at: HKEY\_LOCAL\_MACHINE\\System\\CurrentControlSet\\Control\\GroupOrderList.</span></span> <span data-ttu-id="3c71d-343">Теги оцениваются только для драйверов ядра и драйверов файловой системы, которые имеют режимы загрузки или запуска системы.</span><span class="sxs-lookup"><span data-stu-id="3c71d-343">Tags are only evaluated for Kernel Driver and File System Driver start-type services that have Boot or System start modes.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="3c71d-344">Комментарии</span><span class="sxs-lookup"><span data-stu-id="3c71d-344">Remarks</span></span>

<span data-ttu-id="3c71d-345">Класс **Win32 \_ басесервице** является производным от [**\_ службы CIM**](cim-service.md).</span><span class="sxs-lookup"><span data-stu-id="3c71d-345">The **Win32\_BaseService** class is derived from [**CIM\_Service**](cim-service.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="3c71d-346">Требования</span><span class="sxs-lookup"><span data-stu-id="3c71d-346">Requirements</span></span>



| <span data-ttu-id="3c71d-347">Требование</span><span class="sxs-lookup"><span data-stu-id="3c71d-347">Requirement</span></span> | <span data-ttu-id="3c71d-348">Значение</span><span class="sxs-lookup"><span data-stu-id="3c71d-348">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="3c71d-349">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="3c71d-349">Minimum supported client</span></span><br/> | <span data-ttu-id="3c71d-350">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="3c71d-350">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="3c71d-351">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="3c71d-351">Minimum supported server</span></span><br/> | <span data-ttu-id="3c71d-352">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="3c71d-352">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="3c71d-353">Пространство имен</span><span class="sxs-lookup"><span data-stu-id="3c71d-353">Namespace</span></span><br/>                | <span data-ttu-id="3c71d-354">Корневой \\ CIMV2</span><span class="sxs-lookup"><span data-stu-id="3c71d-354">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="3c71d-355">MOF</span><span class="sxs-lookup"><span data-stu-id="3c71d-355">MOF</span></span><br/>                      | <dl> <span data-ttu-id="3c71d-356"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="3c71d-356"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="3c71d-357">DLL</span><span class="sxs-lookup"><span data-stu-id="3c71d-357">DLL</span></span><br/>                      | <dl> <span data-ttu-id="3c71d-358"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="3c71d-358"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="3c71d-359">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="3c71d-359">See also</span></span>

<dl> <dt>

[<span data-ttu-id="3c71d-360">**\_Служба CIM**</span><span class="sxs-lookup"><span data-stu-id="3c71d-360">**CIM\_Service**</span></span>](cim-service.md)
</dt> <dt>

<span data-ttu-id="3c71d-361">[Классы операционной системы](/previous-versions//aa392727(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="3c71d-361">[Operating System Classes](/previous-versions//aa392727(v=vs.85))</span></span>
</dt> </dl>

 

