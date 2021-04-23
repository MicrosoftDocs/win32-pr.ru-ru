---
description: Представляет системный драйвер для базовой службы.
ms.assetid: 67dc6e14-c8c1-4168-8f99-b04c6ecd4ad2
ms.tgt_platform: multiple
title: Класс Win32_SystemDriver
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_SystemDriver
- Win32_SystemDriver.AcceptPause
- Win32_SystemDriver.AcceptStop
- Win32_SystemDriver.Caption
- Win32_SystemDriver.CreationClassName
- Win32_SystemDriver.Description
- Win32_SystemDriver.DesktopInteract
- Win32_SystemDriver.DisplayName
- Win32_SystemDriver.ErrorControl
- Win32_SystemDriver.ExitCode
- Win32_SystemDriver.InstallDate
- Win32_SystemDriver.Name
- Win32_SystemDriver.PathName
- Win32_SystemDriver.ServiceSpecificExitCode
- Win32_SystemDriver.ServiceType
- Win32_SystemDriver.Started
- Win32_SystemDriver.StartMode
- Win32_SystemDriver.StartName
- Win32_SystemDriver.State
- Win32_SystemDriver.Status
- Win32_SystemDriver.SystemCreationClassName
- Win32_SystemDriver.SystemName
- Win32_SystemDriver.TagId
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: 15be9b176680e8abb259d3d011da9d6cec0c2fa8
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "103807451"
---
# <a name="win32_systemdriver-class"></a><span data-ttu-id="3d458-103">\_Класс Win32 SystemDriver</span><span class="sxs-lookup"><span data-stu-id="3d458-103">Win32\_SystemDriver class</span></span>

<span data-ttu-id="3d458-104"> [Класс WMI](../wmisdk/retrieving-a-class.md) *\*\_ SystemDriver для Win32** представляет системный драйвер для базовой службы.</span><span class="sxs-lookup"><span data-stu-id="3d458-104">The **Win32\_SystemDriver** [WMI class](../wmisdk/retrieving-a-class.md) represents the system driver for a base service.</span></span>

<span data-ttu-id="3d458-105">Следующий пример синтаксиса — упрощенный MOF-код, который включает все наследуемые свойства.</span><span class="sxs-lookup"><span data-stu-id="3d458-105">The following syntax is simplified from Managed Object Format (MOF) code and includes all of the inherited properties.</span></span> <span data-ttu-id="3d458-106">Свойства и методы имеют алфавитный порядок, а не порядок MOF.</span><span class="sxs-lookup"><span data-stu-id="3d458-106">Properties and methods are in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="3d458-107">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="3d458-107">Syntax</span></span>

``` syntax
[Dynamic, Provider("CIMWin32"), SupportsUpdate, UUID("{8502C4C5-5FBB-11D2-AAC1-006008C78BC7}"), AMENDMENT]
class Win32_SystemDriver : Win32_BaseService
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

## <a name="members"></a><span data-ttu-id="3d458-108">Члены</span><span class="sxs-lookup"><span data-stu-id="3d458-108">Members</span></span>

<span data-ttu-id="3d458-109">Класс **Win32 \_ SystemDriver** имеет следующие типы членов:</span><span class="sxs-lookup"><span data-stu-id="3d458-109">The **Win32\_SystemDriver** class has these types of members:</span></span>

-   [<span data-ttu-id="3d458-110">Методы</span><span class="sxs-lookup"><span data-stu-id="3d458-110">Methods</span></span>](#methods)
-   [<span data-ttu-id="3d458-111">Свойства</span><span class="sxs-lookup"><span data-stu-id="3d458-111">Properties</span></span>](#properties)

### <a name="methods"></a><span data-ttu-id="3d458-112">Методы</span><span class="sxs-lookup"><span data-stu-id="3d458-112">Methods</span></span>

<span data-ttu-id="3d458-113">Класс **Win32 \_ SystemDriver** содержит следующие методы.</span><span class="sxs-lookup"><span data-stu-id="3d458-113">The **Win32\_SystemDriver** class has these methods.</span></span>



| <span data-ttu-id="3d458-114">Метод</span><span class="sxs-lookup"><span data-stu-id="3d458-114">Method</span></span>                                                                              | <span data-ttu-id="3d458-115">Описание</span><span class="sxs-lookup"><span data-stu-id="3d458-115">Description</span></span>                                                                                     |
|:------------------------------------------------------------------------------------|:------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="3d458-116">**Change**</span><span class="sxs-lookup"><span data-stu-id="3d458-116">**Change**</span></span>](change-method-in-class-win32-systemdriver.md)                         | <span data-ttu-id="3d458-117">Метод класса, который изменяет службу.</span><span class="sxs-lookup"><span data-stu-id="3d458-117">Class method that modifies a service.</span></span><br/>                                                |
| [<span data-ttu-id="3d458-118">**чанжестартмоде**</span><span class="sxs-lookup"><span data-stu-id="3d458-118">**ChangeStartMode**</span></span>](changestartmode-method-in-class-win32-systemdriver.md)       | <span data-ttu-id="3d458-119">Метод класса, который изменяет режим запуска службы.</span><span class="sxs-lookup"><span data-stu-id="3d458-119">Class method that modifies the start mode of a service.</span></span><br/>                              |
| [<span data-ttu-id="3d458-120">**Создать**</span><span class="sxs-lookup"><span data-stu-id="3d458-120">**Create**</span></span>](create-method-in-class-win32-systemdriver.md)                         | <span data-ttu-id="3d458-121">Метод класса, который создает новую службу.</span><span class="sxs-lookup"><span data-stu-id="3d458-121">Class method that creates a new service.</span></span><br/>                                             |
| [<span data-ttu-id="3d458-122">**Удалить**</span><span class="sxs-lookup"><span data-stu-id="3d458-122">**Delete**</span></span>](delete-method-in-class-win32-systemdriver.md)                         | <span data-ttu-id="3d458-123">Метод класса, который удаляет существующую службу.</span><span class="sxs-lookup"><span data-stu-id="3d458-123">Class method that deletes an existing service.</span></span><br/>                                       |
| [<span data-ttu-id="3d458-124">**интеррогатесервице**</span><span class="sxs-lookup"><span data-stu-id="3d458-124">**InterrogateService**</span></span>](interrogateservice-method-in-class-win32-systemdriver.md) | <span data-ttu-id="3d458-125">Метод класса, запрашивающий обновление состояния службы до Service Manager.</span><span class="sxs-lookup"><span data-stu-id="3d458-125">Class method that requests that the service update its state to the service manager.</span></span><br/> |
| [<span data-ttu-id="3d458-126">**PauseService**</span><span class="sxs-lookup"><span data-stu-id="3d458-126">**PauseService**</span></span>](pauseservice-method-in-class-win32-systemdriver.md)             | <span data-ttu-id="3d458-127">Метод класса, который пытается перевести службу в приостановленное состояние.</span><span class="sxs-lookup"><span data-stu-id="3d458-127">Class method that attempts to place the service in the paused state.</span></span><br/>                 |
| [<span data-ttu-id="3d458-128">**ResumeService**</span><span class="sxs-lookup"><span data-stu-id="3d458-128">**ResumeService**</span></span>](resumeservice-method-in-class-win32-systemdriver.md)           | <span data-ttu-id="3d458-129">Метод класса, который пытается перевести службу в состояние возобновления.</span><span class="sxs-lookup"><span data-stu-id="3d458-129">Class method that attempts to place the service in the resumed state.</span></span><br/>                |
| [<span data-ttu-id="3d458-130">**StartService**</span><span class="sxs-lookup"><span data-stu-id="3d458-130">**StartService**</span></span>](startservice-method-in-class-win32-systemdriver.md)             | <span data-ttu-id="3d458-131">Метод класса, который пытается перевести службу в состояние запуска.</span><span class="sxs-lookup"><span data-stu-id="3d458-131">Class method that attempts to place the service into its startup state.</span></span><br/>              |
| [<span data-ttu-id="3d458-132">**StopService**</span><span class="sxs-lookup"><span data-stu-id="3d458-132">**StopService**</span></span>](stopservice-method-in-class-win32-systemdriver.md)               | <span data-ttu-id="3d458-133">Метод класса, который помещает службу в остановленное состояние.</span><span class="sxs-lookup"><span data-stu-id="3d458-133">Class method that places the service in the stopped state.</span></span><br/>                           |
| [<span data-ttu-id="3d458-134">**усерконтролсервице**</span><span class="sxs-lookup"><span data-stu-id="3d458-134">**UserControlService**</span></span>](usercontrolservice-method-in-class-win32-systemdriver.md) | <span data-ttu-id="3d458-135">Метод класса, который пытается отправить в службу определяемый пользователем код элемента управления.</span><span class="sxs-lookup"><span data-stu-id="3d458-135">Class method that attempts to send a user-defined control code to a service.</span></span><br/>         |



 

### <a name="properties"></a><span data-ttu-id="3d458-136">Свойства</span><span class="sxs-lookup"><span data-stu-id="3d458-136">Properties</span></span>

<span data-ttu-id="3d458-137">Класс **Win32 \_ SystemDriver** имеет следующие свойства.</span><span class="sxs-lookup"><span data-stu-id="3d458-137">The **Win32\_SystemDriver** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="3d458-138">**AcceptPause**</span><span class="sxs-lookup"><span data-stu-id="3d458-138">**AcceptPause**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3d458-139">Тип данных: **логический**</span><span class="sxs-lookup"><span data-stu-id="3d458-139">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="3d458-140">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="3d458-140">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="3d458-141">Квалификаторы: [**маппингстрингс**](../wmisdk/standard-qualifiers.md) ("Win32API \| Service Structures \| [**\_ Status**](/windows/win32/api/winsvc/ns-winsvc-service_status) \| двконтролсакцептед \| Service \_ Accept \_ Пауза \_ Continue"), [**DisplayName**](../wmisdk/standard-qualifiers.md) ("служба принимает паузу")</span><span class="sxs-lookup"><span data-stu-id="3d458-141">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32API\|Service Structures\|[**SERVICE\_STATUS**](/windows/win32/api/winsvc/ns-winsvc-service_status)\|dwControlsAccepted\|SERVICE\_ACCEPT\_PAUSE\_CONTINUE"), [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Service Accepts Pause")</span></span>
</dt> </dl>

<span data-ttu-id="3d458-142">Служба может быть приостановлена.</span><span class="sxs-lookup"><span data-stu-id="3d458-142">Service can be paused.</span></span>

<span data-ttu-id="3d458-143">Это свойство наследуется из [**Win32 \_ басесервице**](win32-baseservice.md).</span><span class="sxs-lookup"><span data-stu-id="3d458-143">This property is inherited from [**Win32\_BaseService**](win32-baseservice.md).</span></span>

</dd> <dt>

<span data-ttu-id="3d458-144">**AcceptStop**</span><span class="sxs-lookup"><span data-stu-id="3d458-144">**AcceptStop**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3d458-145">Тип данных: **логический**</span><span class="sxs-lookup"><span data-stu-id="3d458-145">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="3d458-146">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="3d458-146">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="3d458-147">Квалификаторы: [**маппингстрингс**](../wmisdk/standard-qualifiers.md) ("Win32API \| Service Structures \| [**\_ Status**](/windows/win32/api/winsvc/ns-winsvc-service_status) \| двконтролсакцептед \| Service \_ Accept \_ "), [**DisplayName**](../wmisdk/standard-qualifiers.md) ("служба принимает" останавливается ").</span><span class="sxs-lookup"><span data-stu-id="3d458-147">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32API\|Service Structures\|[**SERVICE\_STATUS**](/windows/win32/api/winsvc/ns-winsvc-service_status)\|dwControlsAccepted\|SERVICE\_ACCEPT\_STOP"), [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Service Accepts Stop")</span></span>
</dt> </dl>

<span data-ttu-id="3d458-148">Служба может быть остановлена.</span><span class="sxs-lookup"><span data-stu-id="3d458-148">Service can be stopped.</span></span>

<span data-ttu-id="3d458-149">Это свойство наследуется из [**Win32 \_ басесервице**](win32-baseservice.md).</span><span class="sxs-lookup"><span data-stu-id="3d458-149">This property is inherited from [**Win32\_BaseService**](win32-baseservice.md).</span></span>

</dd> <dt>

<span data-ttu-id="3d458-150">**Заголовок**</span><span class="sxs-lookup"><span data-stu-id="3d458-150">**Caption**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3d458-151">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="3d458-151">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="3d458-152">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="3d458-152">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="3d458-153">Квалификаторы: [**maxlen**](../wmisdk/standard-qualifiers.md) (64), [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Caption")</span><span class="sxs-lookup"><span data-stu-id="3d458-153">Qualifiers: [**MaxLen**](../wmisdk/standard-qualifiers.md) (64), [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Caption")</span></span>
</dt> </dl>

<span data-ttu-id="3d458-154">Краткое описание объекта.</span><span class="sxs-lookup"><span data-stu-id="3d458-154">Short description of the object.</span></span>

<span data-ttu-id="3d458-155">Это свойство наследуется от [**CIM \_ манажедсистемелемент**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="3d458-155">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="3d458-156">**CreationClassName**</span><span class="sxs-lookup"><span data-stu-id="3d458-156">**CreationClassName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3d458-157">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="3d458-157">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="3d458-158">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="3d458-158">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="3d458-159">Квалификаторы: [**\_ ключ CIM**](../wmisdk/standard-wmi-qualifiers.md), [**DisplayName**](../wmisdk/standard-qualifiers.md) ("имя класса")</span><span class="sxs-lookup"><span data-stu-id="3d458-159">Qualifiers: [**CIM\_Key**](../wmisdk/standard-wmi-qualifiers.md), [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Class Name")</span></span>
</dt> </dl>

<span data-ttu-id="3d458-160">Имя первого конкретного класса, который будет отображаться в цепочке наследования, используемой при создании экземпляра.</span><span class="sxs-lookup"><span data-stu-id="3d458-160">Name of the first concrete class to appear in the inheritance chain used in the creation of an instance.</span></span> <span data-ttu-id="3d458-161">При использовании с другими ключевыми свойствами класса это свойство позволяет уникально идентифицировать все экземпляры этого класса и его подклассов.</span><span class="sxs-lookup"><span data-stu-id="3d458-161">When used with the other key properties of the class, this property allows all instances of this class and its subclasses to be uniquely identified.</span></span>

<span data-ttu-id="3d458-162">Это свойство наследуется [**от \_ службы CIM**](cim-service.md).</span><span class="sxs-lookup"><span data-stu-id="3d458-162">This property is inherited from [**CIM\_Service**](cim-service.md).</span></span>

</dd> <dt>

<span data-ttu-id="3d458-163">**Описание**</span><span class="sxs-lookup"><span data-stu-id="3d458-163">**Description**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3d458-164">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="3d458-164">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="3d458-165">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="3d458-165">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="3d458-166">Квалификаторы: [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Описание")</span><span class="sxs-lookup"><span data-stu-id="3d458-166">Qualifiers: [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Description")</span></span>
</dt> </dl>

<span data-ttu-id="3d458-167">Описание объекта.</span><span class="sxs-lookup"><span data-stu-id="3d458-167">Description of the object.</span></span>

<span data-ttu-id="3d458-168">Это свойство наследуется от [**CIM \_ манажедсистемелемент**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="3d458-168">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="3d458-169">**DesktopInteract**</span><span class="sxs-lookup"><span data-stu-id="3d458-169">**DesktopInteract**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3d458-170">Тип данных: **логический**</span><span class="sxs-lookup"><span data-stu-id="3d458-170">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="3d458-171">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="3d458-171">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="3d458-172">Квалификаторы: [**маппингстрингс**](../wmisdk/standard-qualifiers.md) (" \| структуры служб Win32API \| [**запрос \_ \_ конфигурации**](/windows/win32/api/winsvc/ns-winsvc-query_service_configa)службы \| двсервицетипе \| \_ Интерактивный \_ процесс"), [**DisplayName**](../wmisdk/standard-qualifiers.md) ("взаимодействует с Desktop")</span><span class="sxs-lookup"><span data-stu-id="3d458-172">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32API\|Service Structures\|[**QUERY\_SERVICE\_CONFIG**](/windows/win32/api/winsvc/ns-winsvc-query_service_configa)\|dwServiceType\|SERVICE\_INTERACTIVE\_PROCESS"), [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Interacts With Desktop")</span></span>
</dt> </dl>

<span data-ttu-id="3d458-173">Эта служба может создавать Windows на рабочем столе и взаимодействовать с ними.</span><span class="sxs-lookup"><span data-stu-id="3d458-173">This service can create or communicate with windows on the desktop.</span></span>

<span data-ttu-id="3d458-174">Это свойство наследуется из [**Win32 \_ басесервице**](win32-baseservice.md).</span><span class="sxs-lookup"><span data-stu-id="3d458-174">This property is inherited from [**Win32\_BaseService**](win32-baseservice.md).</span></span>

</dd> <dt>

<span data-ttu-id="3d458-175">**Отображаемое имя**</span><span class="sxs-lookup"><span data-stu-id="3d458-175">**DisplayName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3d458-176">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="3d458-176">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="3d458-177">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="3d458-177">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="3d458-178">Квалификаторы: [**маппингстрингс**](../wmisdk/standard-qualifiers.md) (" \| структуры служб Win32API \| [**запрос \_ \_ конфигурации службы**](/windows/win32/api/winsvc/ns-winsvc-query_service_configa) \| Лпдисплайнаме"), [**DisplayName**](../wmisdk/standard-qualifiers.md) ("отображаемое имя")</span><span class="sxs-lookup"><span data-stu-id="3d458-178">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32API\|Service Structures\|[**QUERY\_SERVICE\_CONFIG**](/windows/win32/api/winsvc/ns-winsvc-query_service_configa)\|lpDisplayName"), [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Display Name")</span></span>
</dt> </dl>

<span data-ttu-id="3d458-179">Отображаемое имя службы.</span><span class="sxs-lookup"><span data-stu-id="3d458-179">Display name of the service.</span></span> <span data-ttu-id="3d458-180">Максимальная длина этой строки равна 256 символам.</span><span class="sxs-lookup"><span data-stu-id="3d458-180">This string has a maximum length of 256 characters.</span></span> <span data-ttu-id="3d458-181">В диспетчере управления службами имя сохраняется с учетом регистра.</span><span class="sxs-lookup"><span data-stu-id="3d458-181">The name is case-preserved in the Service Control Manager.</span></span> <span data-ttu-id="3d458-182">В сравнениях **DisplayName** всегда учитывается регистр.</span><span class="sxs-lookup"><span data-stu-id="3d458-182">**DisplayName** comparisons are always case-insensitive.</span></span>

<span data-ttu-id="3d458-183">Ограничения: принимает то же значение, что и свойство **Name** .</span><span class="sxs-lookup"><span data-stu-id="3d458-183">Constraints: Accepts the same value as the **Name** property.</span></span>

<span data-ttu-id="3d458-184">Пример: "Атдиск"</span><span class="sxs-lookup"><span data-stu-id="3d458-184">Example: "Atdisk"</span></span>

<span data-ttu-id="3d458-185">Это свойство наследуется из [**Win32 \_ басесервице**](win32-baseservice.md).</span><span class="sxs-lookup"><span data-stu-id="3d458-185">This property is inherited from [**Win32\_BaseService**](win32-baseservice.md).</span></span>

</dd> <dt>

<span data-ttu-id="3d458-186">**ErrorControl**</span><span class="sxs-lookup"><span data-stu-id="3d458-186">**ErrorControl**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3d458-187">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="3d458-187">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="3d458-188">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="3d458-188">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="3d458-189">Квалификаторы: [**маппингстрингс**](../wmisdk/standard-qualifiers.md) (" \| структуры служб Win32API \| [**запрос \_ \_ конфигурации службы**](/windows/win32/api/winsvc/ns-winsvc-query_service_configa) \| Дверрорконтрол"), [**DisplayName**](../wmisdk/standard-qualifiers.md) ("серьезность сбоя при запуске")</span><span class="sxs-lookup"><span data-stu-id="3d458-189">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32API\|Service Structures\|[**QUERY\_SERVICE\_CONFIG**](/windows/win32/api/winsvc/ns-winsvc-query_service_configa)\|dwErrorControl"), [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Severity Of Startup Failure")</span></span>
</dt> </dl>

<span data-ttu-id="3d458-190">Серьезность ошибки, если не удается запустить службу во время запуска.</span><span class="sxs-lookup"><span data-stu-id="3d458-190">Severity of the error if this service fails to start during startup.</span></span> <span data-ttu-id="3d458-191">Это значение указывает на действие, предпринимаемое программой запуска, если происходит сбой.</span><span class="sxs-lookup"><span data-stu-id="3d458-191">This value indicates the action taken by the startup program if failure occurs.</span></span> <span data-ttu-id="3d458-192">Все ошибки записываются в журнал системой компьютера.</span><span class="sxs-lookup"><span data-stu-id="3d458-192">All errors are logged by the computer system.</span></span>

<span data-ttu-id="3d458-193">Это свойство наследуется из [**Win32 \_ басесервице**](win32-baseservice.md).</span><span class="sxs-lookup"><span data-stu-id="3d458-193">This property is inherited from [**Win32\_BaseService**](win32-baseservice.md).</span></span>

<dt>

<span id="Ignore"></span><span id="ignore"></span><span id="IGNORE"></span>

<span data-ttu-id="3d458-194"><span id="Ignore"></span><span id="ignore"></span><span id="IGNORE"></span>**Игнорировать** ("ignore")</span><span class="sxs-lookup"><span data-stu-id="3d458-194"><span id="Ignore"></span><span id="ignore"></span><span id="IGNORE"></span>**Ignore** ("Ignore")</span></span>


</dt> <dd>

<span data-ttu-id="3d458-195">Пользователь не получает уведомление.</span><span class="sxs-lookup"><span data-stu-id="3d458-195">User is not notified.</span></span>

</dd> <dt>

<span id="Normal"></span><span id="normal"></span><span id="NORMAL"></span>

<span data-ttu-id="3d458-196"><span id="Normal"></span><span id="normal"></span><span id="NORMAL"></span>**Обычная** ("Обычная")</span><span class="sxs-lookup"><span data-stu-id="3d458-196"><span id="Normal"></span><span id="normal"></span><span id="NORMAL"></span>**Normal** ("Normal")</span></span>


</dt> <dd>

<span data-ttu-id="3d458-197">Пользователь получает уведомление.</span><span class="sxs-lookup"><span data-stu-id="3d458-197">User is notified.</span></span>

</dd> <dt>

<span id="Severe"></span><span id="severe"></span><span id="SEVERE"></span>

<span data-ttu-id="3d458-198"><span id="Severe"></span><span id="severe"></span><span id="SEVERE"></span>**Серьезная** ("серьезная")</span><span class="sxs-lookup"><span data-stu-id="3d458-198"><span id="Severe"></span><span id="severe"></span><span id="SEVERE"></span>**Severe** ("Severe")</span></span>


</dt> <dd>

<span data-ttu-id="3d458-199">Система перезапускается в последней известной рабочей конфигурации.</span><span class="sxs-lookup"><span data-stu-id="3d458-199">System is restarted with the last-known-good configuration.</span></span>

</dd> <dt>

<span id="Critical"></span><span id="critical"></span><span id="CRITICAL"></span>

<span data-ttu-id="3d458-200"><span id="Critical"></span><span id="critical"></span><span id="CRITICAL"></span>**Критическая** ("критическая")</span><span class="sxs-lookup"><span data-stu-id="3d458-200"><span id="Critical"></span><span id="critical"></span><span id="CRITICAL"></span>**Critical** ("Critical")</span></span>


</dt> <dd>

<span data-ttu-id="3d458-201">Попытка перезапустить систему в рабочей конфигурации.</span><span class="sxs-lookup"><span data-stu-id="3d458-201">System attempts to restart with a good configuration.</span></span>

</dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="3d458-202"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Неизвестно** ("неизвестно")</span><span class="sxs-lookup"><span data-stu-id="3d458-202"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** ("Unknown")</span></span>


</dt> <dd>

<span data-ttu-id="3d458-203">Причина сбоя неизвестна.</span><span class="sxs-lookup"><span data-stu-id="3d458-203">Cause of the failure is unknown.</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="3d458-204">**ExitCode**</span><span class="sxs-lookup"><span data-stu-id="3d458-204">**ExitCode**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3d458-205">Тип данных: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="3d458-205">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="3d458-206">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="3d458-206">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="3d458-207">Квалификаторы: [**маппингстрингс**](../wmisdk/standard-qualifiers.md) ("Win32API \| Service Structures \| [**\_ Status**](/windows/win32/api/winsvc/ns-winsvc-service_status) \| DwWin32ExitCode"), [**DisplayName**](../wmisdk/standard-qualifiers.md) ("код выхода")</span><span class="sxs-lookup"><span data-stu-id="3d458-207">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32API\|Service Structures\|[**SERVICE\_STATUS**](/windows/win32/api/winsvc/ns-winsvc-service_status)\|dwWin32ExitCode"), [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Exit Code")</span></span>
</dt> </dl>

<span data-ttu-id="3d458-208">Код ошибки Windows, определяющий любые проблемы, возникшие при запуске или остановке службы.</span><span class="sxs-lookup"><span data-stu-id="3d458-208">Windows error code defining any problems encountered in starting or stopping the service.</span></span> <span data-ttu-id="3d458-209">Это свойство имеет значение ошибка, связанное со **\_ службой \_ \_ ошибок** (1066), если ошибка является уникальной для службы, представленной этим классом, а сведения об ошибке доступны в свойстве **сервицеспеЦифицекситкоде** .</span><span class="sxs-lookup"><span data-stu-id="3d458-209">This property is set to **ERROR\_SERVICE\_SPECIFIC\_ERROR** (1066) when the error is unique to the service represented by this class, and information about the error is available in the **ServiceSpecificExitCode** property.</span></span> <span data-ttu-id="3d458-210">Служба задает это значение **без \_ ошибок** при выполнении и снова после нормального завершения.</span><span class="sxs-lookup"><span data-stu-id="3d458-210">The service sets this value to **NO\_ERROR** when running, and again upon normal termination.</span></span>

<span data-ttu-id="3d458-211">Это свойство наследуется из [**Win32 \_ басесервице**](win32-baseservice.md).</span><span class="sxs-lookup"><span data-stu-id="3d458-211">This property is inherited from [**Win32\_BaseService**](win32-baseservice.md).</span></span>

</dd> <dt>

<span data-ttu-id="3d458-212">**InstallDate**</span><span class="sxs-lookup"><span data-stu-id="3d458-212">**InstallDate**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3d458-213">Тип данных: **DateTime**</span><span class="sxs-lookup"><span data-stu-id="3d458-213">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="3d458-214">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="3d458-214">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="3d458-215">Квалификаторы: [**маппингстрингс**](../wmisdk/standard-qualifiers.md) (MIF. DMTF \| ComponentID \| 001,5 "), [**DisplayName**](../wmisdk/standard-qualifiers.md) (" Дата установки ")</span><span class="sxs-lookup"><span data-stu-id="3d458-215">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("MIF.DMTF\|ComponentID\|001.5"), [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Install Date")</span></span>
</dt> </dl>

<span data-ttu-id="3d458-216">Объект был установлен.</span><span class="sxs-lookup"><span data-stu-id="3d458-216">Object was installed.</span></span> <span data-ttu-id="3d458-217">Для этого свойства не требуется значение, указывающее, что объект установлен.</span><span class="sxs-lookup"><span data-stu-id="3d458-217">This property does not need a value to indicate that the object is installed.</span></span>

<span data-ttu-id="3d458-218">Это свойство наследуется от [**CIM \_ манажедсистемелемент**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="3d458-218">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="3d458-219">**Name**</span><span class="sxs-lookup"><span data-stu-id="3d458-219">**Name**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3d458-220">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="3d458-220">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="3d458-221">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="3d458-221">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="3d458-222">Квалификаторы: [ **ключ**](../wmisdk/key-qualifier.md)</span><span class="sxs-lookup"><span data-stu-id="3d458-222">Qualifiers: [**Key**](../wmisdk/key-qualifier.md)</span></span>
</dt> </dl>

<span data-ttu-id="3d458-223">Уникальный идентификатор службы, который предоставляет сведения об управляемых функциях.</span><span class="sxs-lookup"><span data-stu-id="3d458-223">Unique identifier for the service which provides an indication of the functionality that is managed.</span></span> <span data-ttu-id="3d458-224">Эти функциональные возможности более подробно описаны в свойстве **Описание** объекта.</span><span class="sxs-lookup"><span data-stu-id="3d458-224">This functionality is described in more detail in the object **Description** property.</span></span>

<span data-ttu-id="3d458-225">Это свойство наследуется [**от \_ службы CIM**](cim-service.md).</span><span class="sxs-lookup"><span data-stu-id="3d458-225">This property is inherited from [**CIM\_Service**](cim-service.md).</span></span>

</dd> <dt>

<span data-ttu-id="3d458-226">**PathName**</span><span class="sxs-lookup"><span data-stu-id="3d458-226">**PathName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3d458-227">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="3d458-227">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="3d458-228">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="3d458-228">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="3d458-229">Квалификаторы: [**маппингстрингс**](../wmisdk/standard-qualifiers.md) (" \| структуры служб Win32API \| [**запрос \_ \_ конфигурации**](/windows/win32/api/winsvc/ns-winsvc-query_service_configa) \| Лпбинарипаснаме"), [**DisplayName**](../wmisdk/standard-qualifiers.md) ("имя пути к файлу")</span><span class="sxs-lookup"><span data-stu-id="3d458-229">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32API\|Service Structures\|[**QUERY\_SERVICE\_CONFIG**](/windows/win32/api/winsvc/ns-winsvc-query_service_configa)\|lpBinaryPathName"), [**DisplayName**](../wmisdk/standard-qualifiers.md) ("File Path Name")</span></span>
</dt> </dl>

<span data-ttu-id="3d458-230">Полный путь к двоичному файлу службы, реализующему службу.</span><span class="sxs-lookup"><span data-stu-id="3d458-230">Fully qualified path to the service binary file that implements the service.</span></span>

<span data-ttu-id="3d458-231">Пример: " \\ СистемныйКорневойКаталог \\ system32 \\ Drivers \\afd.sys"</span><span class="sxs-lookup"><span data-stu-id="3d458-231">Example: "\\SystemRoot\\System32\\drivers\\afd.sys"</span></span>

<span data-ttu-id="3d458-232">Это свойство наследуется из [**Win32 \_ басесервице**](win32-baseservice.md).</span><span class="sxs-lookup"><span data-stu-id="3d458-232">This property is inherited from [**Win32\_BaseService**](win32-baseservice.md).</span></span>

</dd> <dt>

<span data-ttu-id="3d458-233">**сервицеспеЦифицекситкоде**</span><span class="sxs-lookup"><span data-stu-id="3d458-233">**ServiceSpecificExitCode**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3d458-234">Тип данных: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="3d458-234">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="3d458-235">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="3d458-235">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="3d458-236">Квалификаторы: [**маппингстрингс**](../wmisdk/standard-qualifiers.md) ("Win32API \| Service Structures \| [**\_ Status**](/windows/win32/api/winsvc/ns-winsvc-service_status) \| двсервицеспеЦифицекситкоде"), [**DisplayName**](../wmisdk/standard-qualifiers.md) ("специфический для сервера код выхода")</span><span class="sxs-lookup"><span data-stu-id="3d458-236">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32API\|Service Structures\|[**SERVICE\_STATUS**](/windows/win32/api/winsvc/ns-winsvc-service_status)\|dwServiceSpecificExitCode"), [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Server Specific Exit Code")</span></span>
</dt> </dl>

<span data-ttu-id="3d458-237">Код ошибки, зависящей от службы, для ошибок, возникающих во время запуска или остановки службы.</span><span class="sxs-lookup"><span data-stu-id="3d458-237">Service-specific error code for errors that occur while the service is either starting or stopping.</span></span> <span data-ttu-id="3d458-238">Коды выхода определяются службой, представленной этим классом.</span><span class="sxs-lookup"><span data-stu-id="3d458-238">The exit codes are defined by the service represented by this class.</span></span> <span data-ttu-id="3d458-239">Это значение задается только в том случае, если значение свойства **ExitCode** — ошибка, связанная со **\_ службой ошибок \_ \_** (1066).</span><span class="sxs-lookup"><span data-stu-id="3d458-239">This value is only set when the **ExitCode** property value is **ERROR\_SERVICE\_SPECIFIC\_ERROR** (1066).</span></span>

<span data-ttu-id="3d458-240">Это свойство наследуется из [**Win32 \_ басесервице**](win32-baseservice.md).</span><span class="sxs-lookup"><span data-stu-id="3d458-240">This property is inherited from [**Win32\_BaseService**](win32-baseservice.md).</span></span>

</dd> <dt>

<span data-ttu-id="3d458-241">**ServiceType**</span><span class="sxs-lookup"><span data-stu-id="3d458-241">**ServiceType**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3d458-242">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="3d458-242">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="3d458-243">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="3d458-243">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="3d458-244">Квалификаторы: [**маппингстрингс**](../wmisdk/standard-qualifiers.md) (" \| структуры служб Win32API \| [**запрос \_ \_ конфигурации службы**](/windows/win32/api/winsvc/ns-winsvc-query_service_configa) \| двсервицетипе"), [**DisplayName**](../wmisdk/standard-qualifiers.md) ("тип службы")</span><span class="sxs-lookup"><span data-stu-id="3d458-244">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32API\|Service Structures\|[**QUERY\_SERVICE\_CONFIG**](/windows/win32/api/winsvc/ns-winsvc-query_service_configa)\|dwServiceType"), [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Service Type")</span></span>
</dt> </dl>

<span data-ttu-id="3d458-245">Тип службы, предоставленной для вызывающих процессов.</span><span class="sxs-lookup"><span data-stu-id="3d458-245">Type of service provided to calling processes.</span></span>

<span data-ttu-id="3d458-246">Это свойство наследуется из [**Win32 \_ басесервице**](win32-baseservice.md).</span><span class="sxs-lookup"><span data-stu-id="3d458-246">This property is inherited from [**Win32\_BaseService**](win32-baseservice.md).</span></span>

<span data-ttu-id="3d458-247">Значения качества производительности:</span><span class="sxs-lookup"><span data-stu-id="3d458-247">The values are:</span></span>

<dt>

<span id="Kernel_Driver"></span><span id="kernel_driver"></span><span id="KERNEL_DRIVER"></span>

<span data-ttu-id="3d458-248">**Драйвер ядра** ("драйвер ядра")</span><span class="sxs-lookup"><span data-stu-id="3d458-248">**Kernel Driver** ("Kernel Driver")</span></span>


</dt> <dd></dd> <dt>

<span id="File_System_Driver"></span><span id="file_system_driver"></span><span id="FILE_SYSTEM_DRIVER"></span>

<span data-ttu-id="3d458-249">**Драйвер файловой системы** ("драйвер файловой системы")</span><span class="sxs-lookup"><span data-stu-id="3d458-249">**File System Driver** ("File System Driver")</span></span>


</dt> <dd></dd> <dt>

<span id="Adapter"></span><span id="adapter"></span><span id="ADAPTER"></span>

<span data-ttu-id="3d458-250">**Адаптер** ("адаптер")</span><span class="sxs-lookup"><span data-stu-id="3d458-250">**Adapter** ("Adapter")</span></span>


</dt> <dd></dd> <dt>

<span id="Recognizer_Driver"></span><span id="recognizer_driver"></span><span id="RECOGNIZER_DRIVER"></span>

<span data-ttu-id="3d458-251">**Драйвер распознавателя** ("драйвер распознавателя")</span><span class="sxs-lookup"><span data-stu-id="3d458-251">**Recognizer Driver** ("Recognizer Driver")</span></span>


</dt> <dd></dd> <dt>

<span id="Own_Process"></span><span id="own_process"></span><span id="OWN_PROCESS"></span>

<span data-ttu-id="3d458-252">**Собственный процесс** ("собственный процесс")</span><span class="sxs-lookup"><span data-stu-id="3d458-252">**Own Process** ("Own Process")</span></span>


</dt> <dd></dd> <dt>

<span id="Share_Process"></span><span id="share_process"></span><span id="SHARE_PROCESS"></span>

<span data-ttu-id="3d458-253">**Общий процесс** ("общий процесс")</span><span class="sxs-lookup"><span data-stu-id="3d458-253">**Share Process** ("Share Process")</span></span>


</dt> <dd></dd> <dt>

<span id="Interactive_Process"></span><span id="interactive_process"></span><span id="INTERACTIVE_PROCESS"></span>

<span data-ttu-id="3d458-254">**Интерактивный процесс** (интерактивный процесс)</span><span class="sxs-lookup"><span data-stu-id="3d458-254">**Interactive Process** ("Interactive Process")</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="3d458-255">**Запуск**</span><span class="sxs-lookup"><span data-stu-id="3d458-255">**Started**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3d458-256">Тип данных: **логический**</span><span class="sxs-lookup"><span data-stu-id="3d458-256">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="3d458-257">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="3d458-257">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="3d458-258">Квалификаторы: [**DisplayName**](../wmisdk/standard-qualifiers.md) ("запущено")</span><span class="sxs-lookup"><span data-stu-id="3d458-258">Qualifiers: [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Started")</span></span>
</dt> </dl>

<span data-ttu-id="3d458-259">Служба запущена.</span><span class="sxs-lookup"><span data-stu-id="3d458-259">Service has been started.</span></span>

<span data-ttu-id="3d458-260">Это свойство наследуется [**от \_ службы CIM**](cim-service.md).</span><span class="sxs-lookup"><span data-stu-id="3d458-260">This property is inherited from [**CIM\_Service**](cim-service.md).</span></span>

</dd> <dt>

<span data-ttu-id="3d458-261">**StartMode**</span><span class="sxs-lookup"><span data-stu-id="3d458-261">**StartMode**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3d458-262">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="3d458-262">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="3d458-263">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="3d458-263">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="3d458-264">Квалификаторы: [**DisplayName**](../wmisdk/standard-qualifiers.md) ("режим запуска")</span><span class="sxs-lookup"><span data-stu-id="3d458-264">Qualifiers: [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Start Mode")</span></span>
</dt> </dl>

<span data-ttu-id="3d458-265">Режим запуска драйвера системы.</span><span class="sxs-lookup"><span data-stu-id="3d458-265">Start mode of the system driver.</span></span>

<span data-ttu-id="3d458-266">Это свойство наследуется из [**Win32 \_ басесервице**](win32-baseservice.md).</span><span class="sxs-lookup"><span data-stu-id="3d458-266">This property is inherited from [**Win32\_BaseService**](win32-baseservice.md).</span></span>

<dt>

<span id="Boot"></span><span id="boot"></span><span id="BOOT"></span>

<span data-ttu-id="3d458-267"><span id="Boot"></span><span id="boot"></span><span id="BOOT"></span>**Boot** (Загрузка)</span><span class="sxs-lookup"><span data-stu-id="3d458-267"><span id="Boot"></span><span id="boot"></span><span id="BOOT"></span>**Boot** ("Boot")</span></span>


</dt> <dd>

<span data-ttu-id="3d458-268">Драйвер устройства запущен загрузчиком операционной системы (действует только для служб драйверов).</span><span class="sxs-lookup"><span data-stu-id="3d458-268">Device driver started by the operating system loader (valid only for driver services).</span></span>

</dd> <dt>

<span id="System"></span><span id="system"></span><span id="SYSTEM"></span>

<span data-ttu-id="3d458-269"><span id="System"></span><span id="system"></span><span id="SYSTEM"></span>**Система** ("System")</span><span class="sxs-lookup"><span data-stu-id="3d458-269"><span id="System"></span><span id="system"></span><span id="SYSTEM"></span>**System** ("System")</span></span>


</dt> <dd>

<span data-ttu-id="3d458-270">Драйвер устройства запущен процессом инициализации операционной системы.</span><span class="sxs-lookup"><span data-stu-id="3d458-270">Device driver started by the operating system initialization process.</span></span> <span data-ttu-id="3d458-271">Это значение допустимо только для служб драйверов.</span><span class="sxs-lookup"><span data-stu-id="3d458-271">This value is valid only for driver services.</span></span>

</dd> <dt>

<span id="Auto"></span><span id="auto"></span><span id="AUTO"></span>

<span data-ttu-id="3d458-272"><span id="Auto"></span><span id="auto"></span><span id="AUTO"></span>**Авто** ("Auto")</span><span class="sxs-lookup"><span data-stu-id="3d458-272"><span id="Auto"></span><span id="auto"></span><span id="AUTO"></span>**Auto** ("Auto")</span></span>


</dt> <dd>

<span data-ttu-id="3d458-273">Служба запускается автоматически диспетчером управления службами во время запуска системы.</span><span class="sxs-lookup"><span data-stu-id="3d458-273">Service to be started automatically by the service control manager during system start up.</span></span>

</dd> <dt>

<span id="Manual"></span><span id="manual"></span><span id="MANUAL"></span>

<span data-ttu-id="3d458-274"><span id="Manual"></span><span id="manual"></span><span id="MANUAL"></span>**Вручную** ("вручную")</span><span class="sxs-lookup"><span data-stu-id="3d458-274"><span id="Manual"></span><span id="manual"></span><span id="MANUAL"></span>**Manual** ("Manual")</span></span>


</dt> <dd>

<span data-ttu-id="3d458-275">Служба, запускаемая диспетчером управления службами, когда процесс вызывает метод [**StartService**](startservice-method-in-class-win32-systemdriver.md) .</span><span class="sxs-lookup"><span data-stu-id="3d458-275">Service to be started by the service control manager when a process calls the [**StartService**](startservice-method-in-class-win32-systemdriver.md) method.</span></span>

</dd> <dt>

<span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>

<span data-ttu-id="3d458-276"><span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>**Отключено** ("отключено")</span><span class="sxs-lookup"><span data-stu-id="3d458-276"><span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>**Disabled** ("Disabled")</span></span>


</dt> <dd>

<span data-ttu-id="3d458-277">Служба, которая больше не может быть запущена.</span><span class="sxs-lookup"><span data-stu-id="3d458-277">Service that can no longer be started.</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="3d458-278">**StartName**</span><span class="sxs-lookup"><span data-stu-id="3d458-278">**StartName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3d458-279">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="3d458-279">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="3d458-280">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="3d458-280">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="3d458-281">Квалификаторы: [**маппингстрингс**](../wmisdk/standard-qualifiers.md) (" \| структуры служб Win32API \| [**запрос \_ \_ конфигурации службы**](/windows/win32/api/winsvc/ns-winsvc-query_service_configa) \| Лпсервицестартнаме"), [**DisplayName**](../wmisdk/standard-qualifiers.md) ("начальное имя учетной записи")</span><span class="sxs-lookup"><span data-stu-id="3d458-281">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32API\|Service Structures\|[**QUERY\_SERVICE\_CONFIG**](/windows/win32/api/winsvc/ns-winsvc-query_service_configa)\|lpServiceStartName"), [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Starting Account Name")</span></span>
</dt> </dl>

<span data-ttu-id="3d458-282">Имя учетной записи, под которой выполняется служба.</span><span class="sxs-lookup"><span data-stu-id="3d458-282">Account name under which the service runs.</span></span> <span data-ttu-id="3d458-283">В зависимости от типа службы имя учетной записи может иметь формат имя_домена \\ имя пользователя.</span><span class="sxs-lookup"><span data-stu-id="3d458-283">Depending on the service type, the account name may be in the form of DomainName\\Username.</span></span> <span data-ttu-id="3d458-284">Процесс службы будет заноситься в журнал с использованием одной из этих двух форм при запуске.</span><span class="sxs-lookup"><span data-stu-id="3d458-284">The service process will be logged using one of these two forms when it runs.</span></span> <span data-ttu-id="3d458-285">Если учетная запись принадлежит к встроенному домену,. \\ Можно указать имя пользователя.</span><span class="sxs-lookup"><span data-stu-id="3d458-285">If the account belongs to the built-in domain, .\\Username can be specified.</span></span> <span data-ttu-id="3d458-286">Если указано **значение NULL** , служба будет входить в систему как учетная запись LocalSystem.</span><span class="sxs-lookup"><span data-stu-id="3d458-286">If **NULL** is specified, the service will be logged on as the LocalSystem account.</span></span> <span data-ttu-id="3d458-287">Для драйверов ядра или системного уровня **StartName** содержит имя объекта драйвера (то есть \\ FileSystem \\ RDR или \\ Driver \\ КСНС), которое используется системой ввода и вывода для загрузки драйвера устройства.</span><span class="sxs-lookup"><span data-stu-id="3d458-287">For kernel or system-level drivers, **StartName** contains the driver object name (that is, \\FileSystem\\Rdr or \\Driver\\Xns) which the input and output (I/O) system uses to load the device driver.</span></span> <span data-ttu-id="3d458-288">Кроме того, если указано **значение NULL** , драйвер запускается с именем объекта по умолчанию, созданным системой ввода-вывода на основе имени службы.</span><span class="sxs-lookup"><span data-stu-id="3d458-288">Additionally, if **NULL** is specified, the driver runs with a default object name created by the I/O system based on the service name.</span></span>

<span data-ttu-id="3d458-289">Пример: "ДВДОМ \\ Admin"</span><span class="sxs-lookup"><span data-stu-id="3d458-289">Example: "DWDOM\\Admin"</span></span>

<span data-ttu-id="3d458-290">Это свойство наследуется из [**Win32 \_ басесервице**](win32-baseservice.md).</span><span class="sxs-lookup"><span data-stu-id="3d458-290">This property is inherited from [**Win32\_BaseService**](win32-baseservice.md).</span></span>

</dd> <dt>

<span data-ttu-id="3d458-291">**Состояние**</span><span class="sxs-lookup"><span data-stu-id="3d458-291">**State**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3d458-292">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="3d458-292">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="3d458-293">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="3d458-293">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="3d458-294">Квалификаторы: [**маппингстрингс**](../wmisdk/standard-qualifiers.md) ("Win32API \| Service Structures \| [**\_ Status**](/windows/win32/api/winsvc/ns-winsvc-service_status) \| двкуррентстате"), [**DisplayName**](../wmisdk/standard-qualifiers.md) ("State")</span><span class="sxs-lookup"><span data-stu-id="3d458-294">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32API\|Service Structures\|[**SERVICE\_STATUS**](/windows/win32/api/winsvc/ns-winsvc-service_status)\|dwCurrentState "), [**DisplayName**](../wmisdk/standard-qualifiers.md) ("State")</span></span>
</dt> </dl>

<span data-ttu-id="3d458-295">Текущее состояние базовой службы.</span><span class="sxs-lookup"><span data-stu-id="3d458-295">Current state of the base service.</span></span>

<span data-ttu-id="3d458-296">Это свойство наследуется из [**Win32 \_ басесервице**](win32-baseservice.md).</span><span class="sxs-lookup"><span data-stu-id="3d458-296">This property is inherited from [**Win32\_BaseService**](win32-baseservice.md).</span></span>

<span data-ttu-id="3d458-297">Значения качества производительности:</span><span class="sxs-lookup"><span data-stu-id="3d458-297">The values are:</span></span>

<dt>

<span id="Stopped"></span><span id="stopped"></span><span id="STOPPED"></span>

<span data-ttu-id="3d458-298">**Остановлено** ("остановлено")</span><span class="sxs-lookup"><span data-stu-id="3d458-298">**Stopped** ("Stopped")</span></span>


</dt> <dd></dd> <dt>

<span id="Start_Pending"></span><span id="start_pending"></span><span id="START_PENDING"></span>

<span data-ttu-id="3d458-299">**Ожидание запуска** ("Ожидание запуска")</span><span class="sxs-lookup"><span data-stu-id="3d458-299">**Start Pending** ("Start Pending")</span></span>


</dt> <dd></dd> <dt>

<span id="Stop_Pending"></span><span id="stop_pending"></span><span id="STOP_PENDING"></span>

<span data-ttu-id="3d458-300">**Ожидание ожидания** ("ожидание завершения")</span><span class="sxs-lookup"><span data-stu-id="3d458-300">**Stop Pending** ("Stop Pending")</span></span>


</dt> <dd></dd> <dt>

<span id="Running"></span><span id="running"></span><span id="RUNNING"></span>

<span data-ttu-id="3d458-301">**Работает** ("работает")</span><span class="sxs-lookup"><span data-stu-id="3d458-301">**Running** ("Running")</span></span>


</dt> <dd></dd> <dt>

<span id="Continue_Pending"></span><span id="continue_pending"></span><span id="CONTINUE_PENDING"></span>

<span data-ttu-id="3d458-302">**Ожидание продолжения** ("Ожидание продолжения")</span><span class="sxs-lookup"><span data-stu-id="3d458-302">**Continue Pending** ("Continue Pending")</span></span>


</dt> <dd></dd> <dt>

<span id="Pause_Pending"></span><span id="pause_pending"></span><span id="PAUSE_PENDING"></span>

<span data-ttu-id="3d458-303">**Ожидание приостановки** ("ожидание приостановки")</span><span class="sxs-lookup"><span data-stu-id="3d458-303">**Pause Pending** ("Pause Pending")</span></span>


</dt> <dd></dd> <dt>

<span id="Paused"></span><span id="paused"></span><span id="PAUSED"></span>

<span data-ttu-id="3d458-304">**Приостановлено** ("приостановлено")</span><span class="sxs-lookup"><span data-stu-id="3d458-304">**Paused** ("Paused")</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="3d458-305">**Неизвестно** ("неизвестно")</span><span class="sxs-lookup"><span data-stu-id="3d458-305">**Unknown** ("Unknown")</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="3d458-306">**Состояние**</span><span class="sxs-lookup"><span data-stu-id="3d458-306">**Status**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3d458-307">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="3d458-307">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="3d458-308">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="3d458-308">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="3d458-309">Квалификаторы: [**maxlen**](../wmisdk/standard-qualifiers.md) (10), [**DisplayName**](../wmisdk/standard-qualifiers.md) ("состояние")</span><span class="sxs-lookup"><span data-stu-id="3d458-309">Qualifiers: [**MaxLen**](../wmisdk/standard-qualifiers.md) (10), [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Status")</span></span>
</dt> </dl>

<span data-ttu-id="3d458-310">Текущее состояние объекта.</span><span class="sxs-lookup"><span data-stu-id="3d458-310">Current status of the object.</span></span> <span data-ttu-id="3d458-311">Можно определить различные операционные и неоперационные состояния.</span><span class="sxs-lookup"><span data-stu-id="3d458-311">Various operational and nonoperational statuses can be defined.</span></span> <span data-ttu-id="3d458-312">Рабочие состояния включают: "ОК", "деградация" и "пред-ошибка" (элемент, например жесткий диск с поддержкой SMART, может работать правильно, но прогнозировать сбой в ближайшем будущем).</span><span class="sxs-lookup"><span data-stu-id="3d458-312">Operational statuses include: "OK", "Degraded", and "Pred Fail" (an element, such as a SMART-enabled hard disk drive, may be functioning properly but predicting a failure in the near future).</span></span> <span data-ttu-id="3d458-313">Неработающие состояния включают: "ошибка", "Запуск", "остановка" и "служба".</span><span class="sxs-lookup"><span data-stu-id="3d458-313">Nonoperational statuses include: "Error", "Starting", "Stopping", and "Service".</span></span> <span data-ttu-id="3d458-314">Последняя, «служба», может применяться во время зеркального копирования диска, перезагрузки списка разрешений пользователя или другой административной работы.</span><span class="sxs-lookup"><span data-stu-id="3d458-314">The latter, "Service", could apply during mirror-resilvering of a disk, reload of a user permissions list, or other administrative work.</span></span> <span data-ttu-id="3d458-315">Не вся такая работа находится в оперативном режиме, но управляемый элемент не является ни "ОК", ни одним из других состояний.</span><span class="sxs-lookup"><span data-stu-id="3d458-315">Not all such work is online, yet the managed element is neither "OK" nor in one of the other states.</span></span>

<span data-ttu-id="3d458-316">Это свойство наследуется от [**CIM \_ манажедсистемелемент**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="3d458-316">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

<span data-ttu-id="3d458-317">Значения качества производительности:</span><span class="sxs-lookup"><span data-stu-id="3d458-317">The values are:</span></span>

<dt>

<span id="OK"></span><span id="ok"></span>

<span data-ttu-id="3d458-318">**ОК** ("ОК")</span><span class="sxs-lookup"><span data-stu-id="3d458-318">**OK** ("OK")</span></span>


</dt> <dd></dd> <dt>

<span id="Error"></span><span id="error"></span><span id="ERROR"></span>

<span data-ttu-id="3d458-319">**Ошибка** ("ошибка")</span><span class="sxs-lookup"><span data-stu-id="3d458-319">**Error** ("Error")</span></span>


</dt> <dd></dd> <dt>

<span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>

<span data-ttu-id="3d458-320">**Пониженная работоспособность** (пониженная работоспособность)</span><span class="sxs-lookup"><span data-stu-id="3d458-320">**Degraded** ("Degraded")</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="3d458-321">**Неизвестно** ("неизвестно")</span><span class="sxs-lookup"><span data-stu-id="3d458-321">**Unknown** ("Unknown")</span></span>


</dt> <dd></dd> <dt>

<span id="Pred_Fail"></span><span id="pred_fail"></span><span id="PRED_FAIL"></span>

<span data-ttu-id="3d458-322">**Пред-ошибка** ("пред Fail")</span><span class="sxs-lookup"><span data-stu-id="3d458-322">**Pred Fail** ("Pred Fail")</span></span>


</dt> <dd></dd> <dt>

<span id="Starting"></span><span id="starting"></span><span id="STARTING"></span>

<span data-ttu-id="3d458-323">**Запуск** ("Запуск")</span><span class="sxs-lookup"><span data-stu-id="3d458-323">**Starting** ("Starting")</span></span>


</dt> <dd></dd> <dt>

<span id="Stopping"></span><span id="stopping"></span><span id="STOPPING"></span>

<span data-ttu-id="3d458-324">**Остановка** ("остановка")</span><span class="sxs-lookup"><span data-stu-id="3d458-324">**Stopping** ("Stopping")</span></span>


</dt> <dd></dd> <dt>

<span id="Service"></span><span id="service"></span><span id="SERVICE"></span>

<span data-ttu-id="3d458-325">**Служба** ("служба")</span><span class="sxs-lookup"><span data-stu-id="3d458-325">**Service** ("Service")</span></span>


</dt> <dd></dd> <dt>

<span id="Stressed"></span><span id="stressed"></span><span id="STRESSED"></span>

<span data-ttu-id="3d458-326">**Пренапряжению** ("напряжению")</span><span class="sxs-lookup"><span data-stu-id="3d458-326">**Stressed** ("Stressed")</span></span>


</dt> <dd></dd> <dt>

<span id="NonRecover"></span><span id="nonrecover"></span><span id="NONRECOVER"></span>

<span data-ttu-id="3d458-327">**Невосстановление** ("невосстановление")</span><span class="sxs-lookup"><span data-stu-id="3d458-327">**NonRecover** ("NonRecover")</span></span>


</dt> <dd></dd> <dt>

<span id="No_Contact"></span><span id="no_contact"></span><span id="NO_CONTACT"></span>

<span data-ttu-id="3d458-328">**Нет контакта** ("нет контакта")</span><span class="sxs-lookup"><span data-stu-id="3d458-328">**No Contact** ("No Contact")</span></span>


</dt> <dd></dd> <dt>

<span id="Lost_Comm"></span><span id="lost_comm"></span><span id="LOST_COMM"></span>

<span data-ttu-id="3d458-329">**Потеря** связи ("потеря связи")</span><span class="sxs-lookup"><span data-stu-id="3d458-329">**Lost Comm** ("Lost Comm")</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="3d458-330">**системкреатионкласснаме**</span><span class="sxs-lookup"><span data-stu-id="3d458-330">**SystemCreationClassName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3d458-331">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="3d458-331">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="3d458-332">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="3d458-332">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="3d458-333">Квалификаторы: [**распространено**](../wmisdk/standard-qualifiers.md) ("[**\_ система CIM**](cim-system.md).**CreationClassName**"), [**\_ ключ CIM**](../wmisdk/standard-wmi-qualifiers.md), [**DisplayName**](../wmisdk/standard-qualifiers.md) (" имя класса системы ")</span><span class="sxs-lookup"><span data-stu-id="3d458-333">Qualifiers: [**Propagated**](../wmisdk/standard-qualifiers.md) ("[**CIM\_System**](cim-system.md).**CreationClassName**"), [**CIM\_Key**](../wmisdk/standard-wmi-qualifiers.md), [**DisplayName**](../wmisdk/standard-qualifiers.md) ("System Class Name")</span></span>
</dt> </dl>

<span data-ttu-id="3d458-334">Имя типа системы, в которой размещена эта служба.</span><span class="sxs-lookup"><span data-stu-id="3d458-334">Type name of the system that hosts this service.</span></span>

<span data-ttu-id="3d458-335">Это свойство наследуется [**от \_ службы CIM**](cim-service.md).</span><span class="sxs-lookup"><span data-stu-id="3d458-335">This property is inherited from [**CIM\_Service**](cim-service.md).</span></span>

</dd> <dt>

<span data-ttu-id="3d458-336">**SystemName**</span><span class="sxs-lookup"><span data-stu-id="3d458-336">**SystemName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3d458-337">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="3d458-337">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="3d458-338">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="3d458-338">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="3d458-339">Квалификаторы: [**распространено**](../wmisdk/standard-qualifiers.md) ("[**\_ система CIM**](cim-system.md).**Name**"), [**\_ ключ CIM**](../wmisdk/standard-wmi-qualifiers.md), [**DisplayName**](../wmisdk/standard-qualifiers.md) (" System Name ")</span><span class="sxs-lookup"><span data-stu-id="3d458-339">Qualifiers: [**Propagated**](../wmisdk/standard-qualifiers.md) ("[**CIM\_System**](cim-system.md).**Name**"), [**CIM\_Key**](../wmisdk/standard-wmi-qualifiers.md), [**DisplayName**](../wmisdk/standard-qualifiers.md) ("System Name")</span></span>
</dt> </dl>

<span data-ttu-id="3d458-340">Имя системы, в которой размещена эта служба.</span><span class="sxs-lookup"><span data-stu-id="3d458-340">Name of the system that hosts this service.</span></span>

<span data-ttu-id="3d458-341">Это свойство наследуется [**от \_ службы CIM**](cim-service.md).</span><span class="sxs-lookup"><span data-stu-id="3d458-341">This property is inherited from [**CIM\_Service**](cim-service.md).</span></span>

</dd> <dt>

<span data-ttu-id="3d458-342">**TagId**</span><span class="sxs-lookup"><span data-stu-id="3d458-342">**TagId**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3d458-343">Тип данных: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="3d458-343">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="3d458-344">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="3d458-344">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="3d458-345">Квалификаторы: [**маппингстрингс**](../wmisdk/standard-qualifiers.md) (" \| структуры служб Win32API \| [**запрос \_ \_ конфигурации**](/windows/win32/api/winsvc/ns-winsvc-query_service_configa) \| двтагид"), [**DisplayName**](../wmisdk/standard-qualifiers.md) ("идентификатор тега")</span><span class="sxs-lookup"><span data-stu-id="3d458-345">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32API\|Service Structures\|[**QUERY\_SERVICE\_CONFIG**](/windows/win32/api/winsvc/ns-winsvc-query_service_configa)\|dwTagId"), [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Tag Id")</span></span>
</dt> </dl>

<span data-ttu-id="3d458-346">Уникальное значение тега для этой службы в группе.</span><span class="sxs-lookup"><span data-stu-id="3d458-346">Unique tag value for this service in the group.</span></span> <span data-ttu-id="3d458-347">Значение 0 (ноль) указывает, что службе не назначен тег.</span><span class="sxs-lookup"><span data-stu-id="3d458-347">A value of 0 (zero) indicates that the service has not been assigned a tag.</span></span> <span data-ttu-id="3d458-348">Тег можно использовать для упорядочения запуска службы в группе порядка загрузки, указывая в реестре вектор порядка тегов в папке:</span><span class="sxs-lookup"><span data-stu-id="3d458-348">A tag can be used for ordering service startup within a load order group by specifying a tag order vector in the registry located at:</span></span>

<span data-ttu-id="3d458-349">Это свойство наследуется из [**Win32 \_ басесервице**](win32-baseservice.md).</span><span class="sxs-lookup"><span data-stu-id="3d458-349">This property is inherited from [**Win32\_BaseService**](win32-baseservice.md).</span></span>

<span data-ttu-id="3d458-350">**HKey \_ \_ \\ \\ \\ \\ Граупордерлист управления CurrentControlSet системы локального компьютера**.</span><span class="sxs-lookup"><span data-stu-id="3d458-350">**HKEY\_LOCAL\_MACHINE\\System\\CurrentControlSet\\Control\\GroupOrderList**.</span></span>

<span data-ttu-id="3d458-351">Теги оцениваются только для драйверов ядра и драйверов файловой системы, которые имеют режимы загрузки или запуска системы.</span><span class="sxs-lookup"><span data-stu-id="3d458-351">Tags are only evaluated for Kernel Driver and File System Driver start-type services that have Boot or System start modes.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="3d458-352">Комментарии</span><span class="sxs-lookup"><span data-stu-id="3d458-352">Remarks</span></span>

<span data-ttu-id="3d458-353">Класс **Win32 \_ SystemDriver** является производным от [**Win32 \_ басесервице**](win32-baseservice.md).</span><span class="sxs-lookup"><span data-stu-id="3d458-353">The **Win32\_SystemDriver** class is derived from [**Win32\_BaseService**](win32-baseservice.md).</span></span>

## <a name="examples"></a><span data-ttu-id="3d458-354">Примеры</span><span class="sxs-lookup"><span data-stu-id="3d458-354">Examples</span></span>

<span data-ttu-id="3d458-355">В примере [List Drivers](https://Gallery.TechNet.Microsoft.Com/5629cc13-cefc-4e51-a24f-aac6db23d141) VBScript в файле HTML отображаются установленные системные драйверы.</span><span class="sxs-lookup"><span data-stu-id="3d458-355">The [List System Drivers](https://Gallery.TechNet.Microsoft.Com/5629cc13-cefc-4e51-a24f-aac6db23d141) VBScript sample Displays installed system drivers in an HTML file.</span></span>

<span data-ttu-id="3d458-356">В следующем примере PowerShell извлекается ряд свойств из выполняемых системных драйверов на компьютере.</span><span class="sxs-lookup"><span data-stu-id="3d458-356">The following PowerShell example retrieves a number of properties from the running system drivers on a computer.</span></span>


```PowerShell
Get-WmiObject -Class Win32_SystemDriver | Where-Object -FilterScript {$_.State -eq "Running"} | Where-Object -FilterScript {$_.StartMode -eq "Manual"} | Format-Table -Property Name,DisplayName
```



## <a name="requirements"></a><span data-ttu-id="3d458-357">Требования</span><span class="sxs-lookup"><span data-stu-id="3d458-357">Requirements</span></span>



| <span data-ttu-id="3d458-358">Требование</span><span class="sxs-lookup"><span data-stu-id="3d458-358">Requirement</span></span> | <span data-ttu-id="3d458-359">Значение</span><span class="sxs-lookup"><span data-stu-id="3d458-359">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="3d458-360">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="3d458-360">Minimum supported client</span></span><br/> | <span data-ttu-id="3d458-361">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="3d458-361">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="3d458-362">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="3d458-362">Minimum supported server</span></span><br/> | <span data-ttu-id="3d458-363">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="3d458-363">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="3d458-364">Пространство имен</span><span class="sxs-lookup"><span data-stu-id="3d458-364">Namespace</span></span><br/>                | <span data-ttu-id="3d458-365">Корневой \\ CIMV2</span><span class="sxs-lookup"><span data-stu-id="3d458-365">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="3d458-366">MOF</span><span class="sxs-lookup"><span data-stu-id="3d458-366">MOF</span></span><br/>                      | <dl> <span data-ttu-id="3d458-367"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="3d458-367"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="3d458-368">DLL</span><span class="sxs-lookup"><span data-stu-id="3d458-368">DLL</span></span><br/>                      | <dl> <span data-ttu-id="3d458-369"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="3d458-369"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="3d458-370">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="3d458-370">See also</span></span>

<dl> <dt>

[<span data-ttu-id="3d458-371">**\_Басесервице Win32**</span><span class="sxs-lookup"><span data-stu-id="3d458-371">**Win32\_BaseService**</span></span>](win32-baseservice.md)
</dt> <dt>

[<span data-ttu-id="3d458-372">Классы операционной системы</span><span class="sxs-lookup"><span data-stu-id="3d458-372">Operating System Classes</span></span>](./operating-system-classes.md)
</dt> </dl>

 

 
