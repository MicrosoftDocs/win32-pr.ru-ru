---
description: Изменяет объект службы, производный от Win32 \_ басесервице.
ms.assetid: d5f4f472-e7d9-4664-9430-9c77034a5978
ms.tgt_platform: multiple
title: Метод Change класса Win32_BaseService (Мбнапи. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_BaseService.Change
api_type:
- COM
api_location:
- CIMWin32.dll
ms.openlocfilehash: a70ee83229a830e22fba4241a6c50eb8d971c5ad
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104142118"
---
# <a name="change-method-of-the-win32_baseservice-class"></a><span data-ttu-id="55df6-103">Метод Change \_ класса Win32 басесервице</span><span class="sxs-lookup"><span data-stu-id="55df6-103">Change method of the Win32\_BaseService class</span></span>

<span data-ttu-id="55df6-104">Метод  [класса WMI](/windows/desktop/WmiSdk/retrieving-a-class) Change изменяет объект службы, производный от [**Win32 \_ басесервице**](win32-baseservice.md).</span><span class="sxs-lookup"><span data-stu-id="55df6-104">The **Change** [WMI class](/windows/desktop/WmiSdk/retrieving-a-class) method modifies a service object derived from [**Win32\_BaseService**](win32-baseservice.md).</span></span> <span data-ttu-id="55df6-105">Параметр [**Win32 \_ лоадордерграуп**](win32-loadordergroup.md) представляет группу системных служб, определяющих зависимости выполнения.</span><span class="sxs-lookup"><span data-stu-id="55df6-105">The [**Win32\_LoadOrderGroup**](win32-loadordergroup.md) parameter represents a group of system services that define execution dependencies.</span></span> <span data-ttu-id="55df6-106">Службы должны запускаться в порядке, указанном в группе порядок загрузки, так как службы зависят друг от друга.</span><span class="sxs-lookup"><span data-stu-id="55df6-106">The services must be initiated in the order specified by the Load Order Group, because the services depend on each other.</span></span> <span data-ttu-id="55df6-107">Для правильной работы этих зависимых служб требуются предшествующие службы.</span><span class="sxs-lookup"><span data-stu-id="55df6-107">These dependent services require antecedent services to function correctly.</span></span>

<span data-ttu-id="55df6-108">В этом разделе используется синтаксис MOF-файл (MOF).</span><span class="sxs-lookup"><span data-stu-id="55df6-108">This topic uses Managed Object Format (MOF) syntax.</span></span> <span data-ttu-id="55df6-109">Дополнительные сведения об использовании этого метода см. [в разделе вызов метода](/windows/desktop/WmiSdk/calling-a-method).</span><span class="sxs-lookup"><span data-stu-id="55df6-109">For more information about using this method, see [Calling a Method](/windows/desktop/WmiSdk/calling-a-method).</span></span>

## <a name="syntax"></a><span data-ttu-id="55df6-110">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="55df6-110">Syntax</span></span>


```mof
uint32 Change(
  [in] string  DisplayName,
  [in] string  PathName,
  [in] uint8   ServiceType,
  [in] uint8   ErrorControl,
  [in] string  StartMode,
  [in] boolean DesktopInteract,
  [in] string  StartName,
  [in] string  StartPassword,
  [in] string  LoadOrderGroup,
  [in] string  LoadOrderGroupDependencies[],
  [in] string  ServiceDependencies[]
);
```



## <a name="parameters"></a><span data-ttu-id="55df6-111">Параметры</span><span class="sxs-lookup"><span data-stu-id="55df6-111">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="55df6-112">*DisplayName* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="55df6-112">*DisplayName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="55df6-113">Отображаемое имя службы.</span><span class="sxs-lookup"><span data-stu-id="55df6-113">The display name for a service.</span></span> <span data-ttu-id="55df6-114">Максимальная длина этой строки равна 256 символам.</span><span class="sxs-lookup"><span data-stu-id="55df6-114">This string has a maximum length of 256 characters.</span></span> <span data-ttu-id="55df6-115">Имя регистра сохраняется в диспетчере управления службами.</span><span class="sxs-lookup"><span data-stu-id="55df6-115">The name is case preserved in the service control manager.</span></span> <span data-ttu-id="55df6-116">В сравнениях *DisplayName* регистр всегда не учитывается.</span><span class="sxs-lookup"><span data-stu-id="55df6-116">*DisplayName* comparisons are always case insensitive.</span></span>

<span data-ttu-id="55df6-117">Ограничения: принимает то же значение, что и параметр *Name* .</span><span class="sxs-lookup"><span data-stu-id="55df6-117">Constraints: Accepts the same value as the *Name* parameter.</span></span>

<span data-ttu-id="55df6-118">Пример: "Атдиск".</span><span class="sxs-lookup"><span data-stu-id="55df6-118">Example: "Atdisk".</span></span>

</dd> <dt>

<span data-ttu-id="55df6-119">*Путь к файлу* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="55df6-119">*PathName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="55df6-120">Полный путь к исполняемому файлу, реализующему службу.</span><span class="sxs-lookup"><span data-stu-id="55df6-120">The fully qualified path to the executable file that implements a service.</span></span>

<span data-ttu-id="55df6-121">Пример: " \\ СистемныйКорневойКаталог \\ system32 \\ Drivers \\afd.sys".</span><span class="sxs-lookup"><span data-stu-id="55df6-121">Example: "\\SystemRoot\\System32\\drivers\\afd.sys".</span></span>

</dd> <dt>

<span data-ttu-id="55df6-122">*ServiceType* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="55df6-122">*ServiceType* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="55df6-123">Тип служб, предоставляемых процессам, которые их вызывают.</span><span class="sxs-lookup"><span data-stu-id="55df6-123">Type of services provided to processes that call them.</span></span>

<dt>

<span id="Kernel_Driver"></span><span id="kernel_driver"></span><span id="KERNEL_DRIVER"></span>

<span data-ttu-id="55df6-124"><span id="Kernel_Driver"></span><span id="kernel_driver"></span><span id="KERNEL_DRIVER"></span>**Драйвер ядра** (1)</span><span class="sxs-lookup"><span data-stu-id="55df6-124"><span id="Kernel_Driver"></span><span id="kernel_driver"></span><span id="KERNEL_DRIVER"></span>**Kernel Driver** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="File_System_Driver"></span><span id="file_system_driver"></span><span id="FILE_SYSTEM_DRIVER"></span>

<span data-ttu-id="55df6-125"><span id="File_System_Driver"></span><span id="file_system_driver"></span><span id="FILE_SYSTEM_DRIVER"></span>**Драйвер файловой системы** (2)</span><span class="sxs-lookup"><span data-stu-id="55df6-125"><span id="File_System_Driver"></span><span id="file_system_driver"></span><span id="FILE_SYSTEM_DRIVER"></span>**File System Driver** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Adapter"></span><span id="adapter"></span><span id="ADAPTER"></span>

<span data-ttu-id="55df6-126"><span id="Adapter"></span><span id="adapter"></span><span id="ADAPTER"></span>**Адаптер** (4)</span><span class="sxs-lookup"><span data-stu-id="55df6-126"><span id="Adapter"></span><span id="adapter"></span><span id="ADAPTER"></span>**Adapter** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="Recognizer_Driver"></span><span id="recognizer_driver"></span><span id="RECOGNIZER_DRIVER"></span>

<span data-ttu-id="55df6-127"><span id="Recognizer_Driver"></span><span id="recognizer_driver"></span><span id="RECOGNIZER_DRIVER"></span>**Драйвер распознавателя** (8)</span><span class="sxs-lookup"><span data-stu-id="55df6-127"><span id="Recognizer_Driver"></span><span id="recognizer_driver"></span><span id="RECOGNIZER_DRIVER"></span>**Recognizer Driver** (8)</span></span>


</dt> <dd></dd> <dt>

<span id="Own_Process"></span><span id="own_process"></span><span id="OWN_PROCESS"></span>

<span data-ttu-id="55df6-128"><span id="Own_Process"></span><span id="own_process"></span><span id="OWN_PROCESS"></span>**Собственный процесс** (16)</span><span class="sxs-lookup"><span data-stu-id="55df6-128"><span id="Own_Process"></span><span id="own_process"></span><span id="OWN_PROCESS"></span>**Own Process** (16)</span></span>


</dt> <dd></dd> <dt>

<span id="Share_Process"></span><span id="share_process"></span><span id="SHARE_PROCESS"></span>

<span data-ttu-id="55df6-129"><span id="Share_Process"></span><span id="share_process"></span><span id="SHARE_PROCESS"></span>**Общий процесс** (32)</span><span class="sxs-lookup"><span data-stu-id="55df6-129"><span id="Share_Process"></span><span id="share_process"></span><span id="SHARE_PROCESS"></span>**Share Process** (32)</span></span>


</dt> <dd></dd> <dt>



 <span data-ttu-id="55df6-130">(256)</span><span class="sxs-lookup"><span data-stu-id="55df6-130">(256)</span></span>


</dt> <dd>

<span data-ttu-id="55df6-131">Интерактивный процесс</span><span class="sxs-lookup"><span data-stu-id="55df6-131">Interactive Process</span></span>

</dd> </dl> </dd> <dt>

<span data-ttu-id="55df6-132">*ErrorControl* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="55df6-132">*ErrorControl* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="55df6-133">Серьезность ошибки, если эта служба не запускается во время запуска.</span><span class="sxs-lookup"><span data-stu-id="55df6-133">Severity of an error if this service does not start during startup.</span></span> <span data-ttu-id="55df6-134">Значение указывает действие, которое принимает программа запуска, если происходит сбой.</span><span class="sxs-lookup"><span data-stu-id="55df6-134">The value indicates the action that the startup program takes if failure occurs.</span></span> <span data-ttu-id="55df6-135">Система регистрирует все ошибки.</span><span class="sxs-lookup"><span data-stu-id="55df6-135">The system logs all errors.</span></span>

<dt>

<span id="Ignore"></span><span id="ignore"></span><span id="IGNORE"></span>

<span data-ttu-id="55df6-136"><span id="Ignore"></span><span id="ignore"></span><span id="IGNORE"></span>**Игнорировать** (0)</span><span class="sxs-lookup"><span data-stu-id="55df6-136"><span id="Ignore"></span><span id="ignore"></span><span id="IGNORE"></span>**Ignore** (0)</span></span>


</dt> <dd>

<span data-ttu-id="55df6-137">Пользователь не получает уведомление.</span><span class="sxs-lookup"><span data-stu-id="55df6-137">User is not notified.</span></span>

</dd> <dt>

<span id="Normal"></span><span id="normal"></span><span id="NORMAL"></span>

<span data-ttu-id="55df6-138"><span id="Normal"></span><span id="normal"></span><span id="NORMAL"></span>**Обычная** (1)</span><span class="sxs-lookup"><span data-stu-id="55df6-138"><span id="Normal"></span><span id="normal"></span><span id="NORMAL"></span>**Normal** (1)</span></span>


</dt> <dd>

<span data-ttu-id="55df6-139">Нормальный.</span><span class="sxs-lookup"><span data-stu-id="55df6-139">Normal.</span></span> <span data-ttu-id="55df6-140">Пользователь получает уведомление.</span><span class="sxs-lookup"><span data-stu-id="55df6-140">User is notified.</span></span>

</dd> <dt>

<span id="Severe"></span><span id="severe"></span><span id="SEVERE"></span>

<span data-ttu-id="55df6-141"><span id="Severe"></span><span id="severe"></span><span id="SEVERE"></span>**Серьезная** (2)</span><span class="sxs-lookup"><span data-stu-id="55df6-141"><span id="Severe"></span><span id="severe"></span><span id="SEVERE"></span>**Severe** (2)</span></span>


</dt> <dd>

<span data-ttu-id="55df6-142">Система перезапускается с последней удачной конфигурацией.</span><span class="sxs-lookup"><span data-stu-id="55df6-142">System is restarted with the last good configuration.</span></span>

</dd> <dt>

<span id="Critical"></span><span id="critical"></span><span id="CRITICAL"></span>

<span data-ttu-id="55df6-143"><span id="Critical"></span><span id="critical"></span><span id="CRITICAL"></span>**Критическая** (3)</span><span class="sxs-lookup"><span data-stu-id="55df6-143"><span id="Critical"></span><span id="critical"></span><span id="CRITICAL"></span>**Critical** (3)</span></span>


</dt> <dd>

<span data-ttu-id="55df6-144">Попытка перезапустить систему в рабочей конфигурации.</span><span class="sxs-lookup"><span data-stu-id="55df6-144">System attempts to restart with a good configuration.</span></span>

</dd> </dl> </dd> <dt>

<span data-ttu-id="55df6-145">*StartMode* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="55df6-145">*StartMode* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="55df6-146">Режим запуска базовой службы Windows.</span><span class="sxs-lookup"><span data-stu-id="55df6-146">Start mode of the Windows base service.</span></span>

<dt>

<span id="Boot_Start"></span><span id="boot_start"></span><span id="BOOT_START"></span>

<span data-ttu-id="55df6-147"><span id="Boot_Start"></span><span id="boot_start"></span><span id="BOOT_START"></span>**Запуск загрузки** ("Boot")</span><span class="sxs-lookup"><span data-stu-id="55df6-147"><span id="Boot_Start"></span><span id="boot_start"></span><span id="BOOT_START"></span>**Boot Start** ("Boot")</span></span>


</dt> <dd>

<span data-ttu-id="55df6-148">Драйвер устройства, с которого запускается загрузчик операционной системы.</span><span class="sxs-lookup"><span data-stu-id="55df6-148">Device driver that the operating system loader starts.</span></span>

</dd> <dt>

<span id="System_Start"></span><span id="system_start"></span><span id="SYSTEM_START"></span>

<span data-ttu-id="55df6-149"><span id="System_Start"></span><span id="system_start"></span><span id="SYSTEM_START"></span>**Системный запуск** ("System")</span><span class="sxs-lookup"><span data-stu-id="55df6-149"><span id="System_Start"></span><span id="system_start"></span><span id="SYSTEM_START"></span>**System Start** ("System")</span></span>


</dt> <dd>

<span data-ttu-id="55df6-150">Драйвер устройства запущен процессом инициализации операционной системы.</span><span class="sxs-lookup"><span data-stu-id="55df6-150">Device driver started by the operating system initialization process.</span></span> <span data-ttu-id="55df6-151">Это значение допустимо только для служб драйверов.</span><span class="sxs-lookup"><span data-stu-id="55df6-151">This value is valid only for driver services.</span></span>

</dd> <dt>

<span id="Auto_Start"></span><span id="auto_start"></span><span id="AUTO_START"></span>

<span data-ttu-id="55df6-152"><span id="Auto_Start"></span><span id="auto_start"></span><span id="AUTO_START"></span>**Автоматический запуск** (автоматический)</span><span class="sxs-lookup"><span data-stu-id="55df6-152"><span id="Auto_Start"></span><span id="auto_start"></span><span id="AUTO_START"></span>**Auto Start** ("Automatic")</span></span>


</dt> <dd>

<span data-ttu-id="55df6-153">Служба запускается автоматически диспетчером управления службами во время запуска системы.</span><span class="sxs-lookup"><span data-stu-id="55df6-153">Service to start automatically by the service control manager during system startup.</span></span>

</dd> <dt>

<span id="Demand_Start"></span><span id="demand_start"></span><span id="DEMAND_START"></span>

<span data-ttu-id="55df6-154"><span id="Demand_Start"></span><span id="demand_start"></span><span id="DEMAND_START"></span>**Запуск по требованию** (вручную)</span><span class="sxs-lookup"><span data-stu-id="55df6-154"><span id="Demand_Start"></span><span id="demand_start"></span><span id="DEMAND_START"></span>**Demand Start** ("Manual")</span></span>


</dt> <dd>

<span data-ttu-id="55df6-155">Служба, запускаемая диспетчером управления службами, когда процесс вызывает метод [**StartService**](startservice-method-in-class-win32-baseservice.md) .</span><span class="sxs-lookup"><span data-stu-id="55df6-155">Service to start by the service control manager when a process calls the [**StartService**](startservice-method-in-class-win32-baseservice.md) method.</span></span>

</dd> <dt>

<span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>

<span data-ttu-id="55df6-156"><span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>**Отключено** ("отключено")</span><span class="sxs-lookup"><span data-stu-id="55df6-156"><span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>**Disabled** ("Disabled")</span></span>


</dt> <dd>

<span data-ttu-id="55df6-157">Служба, которая не может быть запущена.</span><span class="sxs-lookup"><span data-stu-id="55df6-157">Service that cannot be started.</span></span>

</dd> </dl> </dd> <dt>

<span data-ttu-id="55df6-158">*Десктопинтеракт* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="55df6-158">*DesktopInteract* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="55df6-159">Если **значение — true**, служба может создавать окно на рабочем столе или взаимодействовать с ним.</span><span class="sxs-lookup"><span data-stu-id="55df6-159">If **True**, the service can create or communicate with a window on the desktop.</span></span>

</dd> <dt>

<span data-ttu-id="55df6-160">*StartName* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="55df6-160">*StartName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="55df6-161">Имя учетной записи, под которой выполняется служба, которая зависит от типа службы.</span><span class="sxs-lookup"><span data-stu-id="55df6-161">Account name that the service runs under, which depends on the service type.</span></span> <span data-ttu-id="55df6-162">Имя учетной записи может иметь формат имя_домена \\ имя пользователя или. \\ Имен.</span><span class="sxs-lookup"><span data-stu-id="55df6-162">The account name may be in the form of DomainName\\Username or .\\Username.</span></span> <span data-ttu-id="55df6-163">При запуске процесс службы заносится в журнал с использованием одной из двух предыдущих форм.</span><span class="sxs-lookup"><span data-stu-id="55df6-163">When it runs, the service process is logged by using one of the previous two forms.</span></span> <span data-ttu-id="55df6-164">Если учетная запись принадлежит к встроенному домену,. \\ Можно указать имя пользователя.</span><span class="sxs-lookup"><span data-stu-id="55df6-164">If the account belongs to the built-in domain, .\\Username can be specified.</span></span> <span data-ttu-id="55df6-165">Если указана пустая строка, служба входит в систему как учетную запись LocalSystem.</span><span class="sxs-lookup"><span data-stu-id="55df6-165">If an empty string is specified, the service is logged on as the LocalSystem account.</span></span> <span data-ttu-id="55df6-166">Для драйверов ядра или системного уровня *StartName* содержит имя объекта драйвера, например \\ FileSystem \\ RDR или \\ Driver \\ КСНС, которое используется системой ввода и вывода для загрузки драйвера устройства.</span><span class="sxs-lookup"><span data-stu-id="55df6-166">For kernel or system-level drivers, *StartName* contains the driver object name, for example, \\FileSystem\\Rdr or \\Driver\\Xns, which the input and output (I/O) system uses to load the device driver.</span></span> <span data-ttu-id="55df6-167">Если указано **значение NULL** , драйвер запускается с именем объекта по умолчанию, созданным системой ввода-вывода на основе имени службы, например \\ администратора двдом.</span><span class="sxs-lookup"><span data-stu-id="55df6-167">If **NULL** is specified, the driver runs with a default object name that the I/O system creates based on the service name, for example, DWDOM\\Admin.</span></span>

<span data-ttu-id="55df6-168">Можно также использовать формат имени участника-пользователя (UPN) для указания **StartName**, например *Username@DomainName* .</span><span class="sxs-lookup"><span data-stu-id="55df6-168">You also can use the User Principal Name (UPN) format to specify the **StartName**, for example, *Username@DomainName*.</span></span>

</dd> <dt>

<span data-ttu-id="55df6-169">*Стартпассворд* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="55df6-169">*StartPassword* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="55df6-170">Пароль к имени учетной записи, указанному параметром *StartName* .</span><span class="sxs-lookup"><span data-stu-id="55df6-170">Password to the account name that the *StartName* parameter specifies.</span></span> <span data-ttu-id="55df6-171">Если пароль не изменен, укажите **значение NULL** .</span><span class="sxs-lookup"><span data-stu-id="55df6-171">Specify **NULL** when you do not change the password.</span></span> <span data-ttu-id="55df6-172">Если служба не имеет пароля, укажите пустую строку.</span><span class="sxs-lookup"><span data-stu-id="55df6-172">Specify an empty string if the service does not have a password.</span></span>

> [!Note]  
> <span data-ttu-id="55df6-173">При изменении службы с локальной системы на сеть или из сети в локальную систему *стартпассворд* должен быть пустой строкой (""), а не **null**.</span><span class="sxs-lookup"><span data-stu-id="55df6-173">When you change a service from local system to network or from network to local system, *StartPassword* must be an empty string ("") and not **NULL**.</span></span>

 

</dd> <dt>

<span data-ttu-id="55df6-174">*Лоадордерграуп* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="55df6-174">*LoadOrderGroup* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="55df6-175">Имя группы, с которой она связана.</span><span class="sxs-lookup"><span data-stu-id="55df6-175">Group name that it is associated with.</span></span> <span data-ttu-id="55df6-176">Группы порядка загрузки содержатся в системном реестре и определяют последовательность загрузки служб в операционную систему.</span><span class="sxs-lookup"><span data-stu-id="55df6-176">Load order groups are contained in the system registry, and determine the sequence that services are loaded into an operating system.</span></span> <span data-ttu-id="55df6-177">Если указатель равен **null** или указывает на пустую строку, служба не принадлежит группе.</span><span class="sxs-lookup"><span data-stu-id="55df6-177">If the pointer is **NULL**, or points to an empty string, the service does not belong to a group.</span></span> <span data-ttu-id="55df6-178">Зависимости между группами должны быть перечислены в параметре *лоадордерграупдепенденЦиес* .</span><span class="sxs-lookup"><span data-stu-id="55df6-178">Dependencies between groups should be listed in the *LoadOrderGroupDependencies* parameter.</span></span> <span data-ttu-id="55df6-179">Сначала запускаются службы в списке группы упорядочения нагрузки, а затем — службы в группах, которые не входят в список групп порядка загрузки, за которыми следуют службы, не входящие в группу.</span><span class="sxs-lookup"><span data-stu-id="55df6-179">Services in the load-ordering group list are started first, followed by services in groups not in the load-ordering group list, followed by services that do not belong to a group.</span></span> <span data-ttu-id="55df6-180">Системный реестр содержит список групп упорядочения нагрузки, расположенных в папке **hKey \_ Local \_ Machine** \\ **System** \\ **CurrentControlSet** \\ **Control** \\ **ServiceGroupOrder**.</span><span class="sxs-lookup"><span data-stu-id="55df6-180">The system registry has a list of load ordering groups located at **HKEY\_LOCAL\_MACHINE**\\**System**\\**CurrentControlSet**\\**Control**\\**ServiceGroupOrder**.</span></span>

</dd> <dt>

<span data-ttu-id="55df6-181">*ЛоадордерграупдепенденЦиес* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="55df6-181">*LoadOrderGroupDependencies* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="55df6-182">Список групп упорядочивания нагрузки, которые должны быть запущены перед запуском этой службы.</span><span class="sxs-lookup"><span data-stu-id="55df6-182">List of load-ordering groups that must start before this service starts.</span></span> <span data-ttu-id="55df6-183">Массив завершается двойным **нулем.**</span><span class="sxs-lookup"><span data-stu-id="55df6-183">The array is doubly **null**-terminated.</span></span> <span data-ttu-id="55df6-184">Если указатель имеет **значение NULL** или указывает на пустую строку, служба не имеет зависимостей.</span><span class="sxs-lookup"><span data-stu-id="55df6-184">If the pointer is **NULL**, or if it points to an empty string, the service does not have dependencies.</span></span> <span data-ttu-id="55df6-185">Имена групп должны иметь префикс в виде **\_ \_ идентификатора группы SC** (определенного в файле винсвк. h), чтобы отличать их от имен служб, так как службы и группы служб используют одно и то же пространство имен.</span><span class="sxs-lookup"><span data-stu-id="55df6-185">Group names must be prefixed by the **SC\_GROUP\_IDENTIFIER** (defined in the Winsvc.h file) character to differentiate them from service names, because services and service groups share the same namespace.</span></span> <span data-ttu-id="55df6-186">Зависимость от группы означает, что эту службу можно запустить, если хотя бы один член группы запущен после попытки запуска всех членов группы.</span><span class="sxs-lookup"><span data-stu-id="55df6-186">Dependency on a group means that this service can run if at least one member of the group is running after an attempt to start all of the members of the group.</span></span>

</dd> <dt>

<span data-ttu-id="55df6-187">*СервицедепенденЦиес* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="55df6-187">*ServiceDependencies* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="55df6-188">Список, содержащий имена служб, которые должны быть запущены перед запуском этой службы.</span><span class="sxs-lookup"><span data-stu-id="55df6-188">List that contains the names of services that must start before this service starts.</span></span> <span data-ttu-id="55df6-189">Массив завершается двойным **нулем.**</span><span class="sxs-lookup"><span data-stu-id="55df6-189">The array is doubly **null**-terminated.</span></span> <span data-ttu-id="55df6-190">Если указатель равен **null** или указывает на пустую строку, служба не имеет зависимостей.</span><span class="sxs-lookup"><span data-stu-id="55df6-190">If the pointer is **NULL**, or points to an empty string, the service does not have dependencies.</span></span> <span data-ttu-id="55df6-191">Зависимость от службы означает, что эта служба может выполняться, только если запущена служба, от которой она зависит.</span><span class="sxs-lookup"><span data-stu-id="55df6-191">Dependency on a service means that this service can run only if the service it depends on is running.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="55df6-192">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="55df6-192">Return value</span></span>

<span data-ttu-id="55df6-193">Возвращает одно из значений, перечисленных в следующем списке, или другое значение, указывающее на ошибку.</span><span class="sxs-lookup"><span data-stu-id="55df6-193">Returns one of the values listed in the following list, or a different value to indicate an error.</span></span>

<dl> <dt>

<span data-ttu-id="55df6-194">**Успешно**</span><span class="sxs-lookup"><span data-stu-id="55df6-194">**Success**</span></span>
</dt> <dd>

<span data-ttu-id="55df6-195">0</span><span class="sxs-lookup"><span data-stu-id="55df6-195">0</span></span>

<span data-ttu-id="55df6-196">Запрос принят.</span><span class="sxs-lookup"><span data-stu-id="55df6-196">The request is accepted.</span></span>

</dd> <dt>

<span data-ttu-id="55df6-197">**Не поддерживается**</span><span class="sxs-lookup"><span data-stu-id="55df6-197">**Not Supported**</span></span>
</dt> <dd>

<span data-ttu-id="55df6-198">1</span><span class="sxs-lookup"><span data-stu-id="55df6-198">1</span></span>

<span data-ttu-id="55df6-199">Запрос не поддерживается.</span><span class="sxs-lookup"><span data-stu-id="55df6-199">The request is not supported.</span></span>

</dd> <dt>

<span data-ttu-id="55df6-200">**Доступ запрещен**</span><span class="sxs-lookup"><span data-stu-id="55df6-200">**Access Denied**</span></span>
</dt> <dd>

<span data-ttu-id="55df6-201">2</span><span class="sxs-lookup"><span data-stu-id="55df6-201">2</span></span>

<span data-ttu-id="55df6-202">У пользователя нет необходимых прав доступа.</span><span class="sxs-lookup"><span data-stu-id="55df6-202">The user does not have the necessary access privileges.</span></span>

</dd> <dt>

<span data-ttu-id="55df6-203">**Работающие зависимые службы**</span><span class="sxs-lookup"><span data-stu-id="55df6-203">**Dependent Services Running**</span></span>
</dt> <dd>

<span data-ttu-id="55df6-204">3</span><span class="sxs-lookup"><span data-stu-id="55df6-204">3</span></span>

<span data-ttu-id="55df6-205">Службу нельзя остановить, так как от нее зависят другие работающие службы.</span><span class="sxs-lookup"><span data-stu-id="55df6-205">The service cannot be stopped because other services that are running are dependent on it.</span></span>

</dd> <dt>

<span data-ttu-id="55df6-206">**Недопустимый элемент управления службой**</span><span class="sxs-lookup"><span data-stu-id="55df6-206">**Invalid Service Control**</span></span>
</dt> <dd>

<span data-ttu-id="55df6-207">4</span><span class="sxs-lookup"><span data-stu-id="55df6-207">4</span></span>

<span data-ttu-id="55df6-208">Запрошенный управляющий код недопустим или неприемлем для службы.</span><span class="sxs-lookup"><span data-stu-id="55df6-208">The requested control code is not valid, or is unacceptable to the service.</span></span>

</dd> <dt>

<span data-ttu-id="55df6-209">**Служба не может принять контроль**</span><span class="sxs-lookup"><span data-stu-id="55df6-209">**Service Cannot Accept Control**</span></span>
</dt> <dd>

<span data-ttu-id="55df6-210">5</span><span class="sxs-lookup"><span data-stu-id="55df6-210">5</span></span>

<span data-ttu-id="55df6-211">Запрошенный управляющий код не может быть отправлен в службу, так как свойство [**State**](win32-baseservice.md) в объекте [**Win32 \_ басесервице**](win32-baseservice.md) равно 0, 1 или 2.</span><span class="sxs-lookup"><span data-stu-id="55df6-211">The requested control code cannot be sent to the service because the [**State**](win32-baseservice.md) property in the [**Win32\_BaseService**](win32-baseservice.md) object is equal to 0, 1, or 2.</span></span>

</dd> <dt>

<span data-ttu-id="55df6-212">**Служба неактивна**</span><span class="sxs-lookup"><span data-stu-id="55df6-212">**Service Not Active**</span></span>
</dt> <dd>

<span data-ttu-id="55df6-213">6</span><span class="sxs-lookup"><span data-stu-id="55df6-213">6</span></span>

<span data-ttu-id="55df6-214">Служба не запущена.</span><span class="sxs-lookup"><span data-stu-id="55df6-214">The service has not been started.</span></span>

</dd> <dt>

<span data-ttu-id="55df6-215">**Время ожидания запроса на обслуживание**</span><span class="sxs-lookup"><span data-stu-id="55df6-215">**Service Request Timeout**</span></span>
</dt> <dd>

<span data-ttu-id="55df6-216">7</span><span class="sxs-lookup"><span data-stu-id="55df6-216">7</span></span>

<span data-ttu-id="55df6-217">Служба не реагирует на запрос на запуск быстро.</span><span class="sxs-lookup"><span data-stu-id="55df6-217">The service does not respond to the start request quickly.</span></span>

</dd> <dt>

<span data-ttu-id="55df6-218">**Неизвестный сбой**</span><span class="sxs-lookup"><span data-stu-id="55df6-218">**Unknown Failure**</span></span>
</dt> <dd>

<span data-ttu-id="55df6-219">8</span><span class="sxs-lookup"><span data-stu-id="55df6-219">8</span></span>

<span data-ttu-id="55df6-220">Интерактивный процесс.</span><span class="sxs-lookup"><span data-stu-id="55df6-220">Interactive process.</span></span>

</dd> <dt>

<span data-ttu-id="55df6-221">**Путь не найден**</span><span class="sxs-lookup"><span data-stu-id="55df6-221">**Path Not Found**</span></span>
</dt> <dd>

<span data-ttu-id="55df6-222">9</span><span class="sxs-lookup"><span data-stu-id="55df6-222">9</span></span>

<span data-ttu-id="55df6-223">Не найден путь к каталогу исполняемого файла службы.</span><span class="sxs-lookup"><span data-stu-id="55df6-223">The directory path to the service executable file is not found.</span></span>

</dd> <dt>

<span data-ttu-id="55df6-224">**Служба уже запущена**</span><span class="sxs-lookup"><span data-stu-id="55df6-224">**Service Already Running**</span></span>
</dt> <dd>

<span data-ttu-id="55df6-225">10</span><span class="sxs-lookup"><span data-stu-id="55df6-225">10</span></span>

<span data-ttu-id="55df6-226">Служба уже запущена.</span><span class="sxs-lookup"><span data-stu-id="55df6-226">The service is already running.</span></span>

</dd> <dt>

<span data-ttu-id="55df6-227">**База данных службы заблокирована**</span><span class="sxs-lookup"><span data-stu-id="55df6-227">**Service Database Locked**</span></span>
</dt> <dd>

<span data-ttu-id="55df6-228">11</span><span class="sxs-lookup"><span data-stu-id="55df6-228">11</span></span>

<span data-ttu-id="55df6-229">База данных для добавления новой службы заблокирована.</span><span class="sxs-lookup"><span data-stu-id="55df6-229">The database to add a new service is locked.</span></span>

</dd> <dt>

<span data-ttu-id="55df6-230">**Зависимость службы удалена**</span><span class="sxs-lookup"><span data-stu-id="55df6-230">**Service Dependency Deleted**</span></span>
</dt> <dd>

<span data-ttu-id="55df6-231">12</span><span class="sxs-lookup"><span data-stu-id="55df6-231">12</span></span>

<span data-ttu-id="55df6-232">Зависимость, от которой зависит эта служба, удаляется из системы.</span><span class="sxs-lookup"><span data-stu-id="55df6-232">A dependency for which this service relies on is removed from the system.</span></span>

</dd> <dt>

<span data-ttu-id="55df6-233">**Сбой зависимости службы**</span><span class="sxs-lookup"><span data-stu-id="55df6-233">**Service Dependency Failure**</span></span>
</dt> <dd>

<span data-ttu-id="55df6-234">13</span><span class="sxs-lookup"><span data-stu-id="55df6-234">13</span></span>

<span data-ttu-id="55df6-235">Служба не находит службу, необходимую зависимой службе.</span><span class="sxs-lookup"><span data-stu-id="55df6-235">The service does not find the service needed from a dependent service.</span></span>

</dd> <dt>

<span data-ttu-id="55df6-236">**Служба отключена**</span><span class="sxs-lookup"><span data-stu-id="55df6-236">**Service Disabled**</span></span>
</dt> <dd>

<span data-ttu-id="55df6-237">14</span><span class="sxs-lookup"><span data-stu-id="55df6-237">14</span></span>

<span data-ttu-id="55df6-238">Служба отключена от системы.</span><span class="sxs-lookup"><span data-stu-id="55df6-238">The service is disabled from the system.</span></span>

</dd> <dt>

<span data-ttu-id="55df6-239">**Сбой при входе в службу**</span><span class="sxs-lookup"><span data-stu-id="55df6-239">**Service Logon Failed**</span></span>
</dt> <dd>

<span data-ttu-id="55df6-240">15</span><span class="sxs-lookup"><span data-stu-id="55df6-240">15</span></span>

<span data-ttu-id="55df6-241">Эта служба не поддерживает проверку подлинности, необходимую для работы в системе.</span><span class="sxs-lookup"><span data-stu-id="55df6-241">The service does not have the correct authentication to run on the system.</span></span>

</dd> <dt>

<span data-ttu-id="55df6-242">**Служба помечена для удаления**</span><span class="sxs-lookup"><span data-stu-id="55df6-242">**Service Marked For Deletion**</span></span>
</dt> <dd>

<span data-ttu-id="55df6-243">16</span><span class="sxs-lookup"><span data-stu-id="55df6-243">16</span></span>

<span data-ttu-id="55df6-244">Эта служба удаляется из системы.</span><span class="sxs-lookup"><span data-stu-id="55df6-244">This service is being removed from the system.</span></span>

</dd> <dt>

<span data-ttu-id="55df6-245">**Служба без потока**</span><span class="sxs-lookup"><span data-stu-id="55df6-245">**Service No Thread**</span></span>
</dt> <dd>

<span data-ttu-id="55df6-246">17</span><span class="sxs-lookup"><span data-stu-id="55df6-246">17</span></span>

<span data-ttu-id="55df6-247">Отсутствует поток исполнения для этой службы.</span><span class="sxs-lookup"><span data-stu-id="55df6-247">There is no execution thread for the service.</span></span>

</dd> <dt>

<span data-ttu-id="55df6-248">**Состояние "циклическая зависимость"**</span><span class="sxs-lookup"><span data-stu-id="55df6-248">**Status Circular Dependency**</span></span>
</dt> <dd>

<span data-ttu-id="55df6-249">18</span><span class="sxs-lookup"><span data-stu-id="55df6-249">18</span></span>

<span data-ttu-id="55df6-250">При запуске службы обнаружены циклические зависимости.</span><span class="sxs-lookup"><span data-stu-id="55df6-250">There are circular dependencies when starting the service.</span></span>

</dd> <dt>

<span data-ttu-id="55df6-251">**Состояние "повторяющееся имя"**</span><span class="sxs-lookup"><span data-stu-id="55df6-251">**Status Duplicate Name**</span></span>
</dt> <dd>

<span data-ttu-id="55df6-252">19</span><span class="sxs-lookup"><span data-stu-id="55df6-252">19</span></span>

<span data-ttu-id="55df6-253">Служба с таким именем уже запущена.</span><span class="sxs-lookup"><span data-stu-id="55df6-253">There is a service running under the same name.</span></span>

</dd> <dt>

<span data-ttu-id="55df6-254">**Состояние "Недопустимое имя"**</span><span class="sxs-lookup"><span data-stu-id="55df6-254">**Status Invalid Name**</span></span>
</dt> <dd>

<span data-ttu-id="55df6-255">20</span><span class="sxs-lookup"><span data-stu-id="55df6-255">20</span></span>

<span data-ttu-id="55df6-256">В имени службы присутствуют недопустимые символы.</span><span class="sxs-lookup"><span data-stu-id="55df6-256">There are invalid characters in the name of the service.</span></span>

</dd> <dt>

<span data-ttu-id="55df6-257">**Недопустимый параметр Status**</span><span class="sxs-lookup"><span data-stu-id="55df6-257">**Status Invalid Parameter**</span></span>
</dt> <dd>

<span data-ttu-id="55df6-258">21</span><span class="sxs-lookup"><span data-stu-id="55df6-258">21</span></span>

<span data-ttu-id="55df6-259">Службе переданы недопустимые параметры.</span><span class="sxs-lookup"><span data-stu-id="55df6-259">Invalid parameters have been passed to the service.</span></span>

</dd> <dt>

<span data-ttu-id="55df6-260">**Недопустимое состояние учетной записи службы**</span><span class="sxs-lookup"><span data-stu-id="55df6-260">**Status Invalid Service Account**</span></span>
</dt> <dd>

<span data-ttu-id="55df6-261">22</span><span class="sxs-lookup"><span data-stu-id="55df6-261">22</span></span>

<span data-ttu-id="55df6-262">Учетная запись для запуска службы не является допустимой или не имеет разрешений на запуск службы.</span><span class="sxs-lookup"><span data-stu-id="55df6-262">The account for this service to run under is not valid or does not have the permissions to run the service.</span></span>

</dd> <dt>

<span data-ttu-id="55df6-263">**Служба состояний существует**</span><span class="sxs-lookup"><span data-stu-id="55df6-263">**Status Service Exists**</span></span>
</dt> <dd>

<span data-ttu-id="55df6-264">23</span><span class="sxs-lookup"><span data-stu-id="55df6-264">23</span></span>

<span data-ttu-id="55df6-265">Служба существует в базе данных доступных в системе служб.</span><span class="sxs-lookup"><span data-stu-id="55df6-265">The service exists in the database of services available from the system.</span></span>

</dd> <dt>

<span data-ttu-id="55df6-266">**Служба уже приостановлена**</span><span class="sxs-lookup"><span data-stu-id="55df6-266">**Service Already Paused**</span></span>
</dt> <dd>

<span data-ttu-id="55df6-267">24</span><span class="sxs-lookup"><span data-stu-id="55df6-267">24</span></span>

<span data-ttu-id="55df6-268">Служба в данный момент приостановлена в системе.</span><span class="sxs-lookup"><span data-stu-id="55df6-268">The service is currently paused in the system.</span></span>

</dd> <dt>

<span data-ttu-id="55df6-269">**Другое**</span><span class="sxs-lookup"><span data-stu-id="55df6-269">**Other**</span></span>
</dt> <dd>

<span data-ttu-id="55df6-270">25 4294967295</span><span class="sxs-lookup"><span data-stu-id="55df6-270">25 4294967295</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="55df6-271">Комментарии</span><span class="sxs-lookup"><span data-stu-id="55df6-271">Remarks</span></span>

<span data-ttu-id="55df6-272">Чтобы изменить службу из сети в локальную систему, используйте следующие значения параметров *StartName* и *стартпассворд* :</span><span class="sxs-lookup"><span data-stu-id="55df6-272">To change a service from a network to a local system, use the following values for the *StartName* and *StartPassword* parameters:</span></span>


```C++
StartName = "LocalSystem"
StartPassword = "" // - empty string, not NULL
```



<span data-ttu-id="55df6-273">Чтобы изменить службу с локальной системы на сеть, используйте следующие значения параметров *StartName* и *стартпассворд* :</span><span class="sxs-lookup"><span data-stu-id="55df6-273">To change a service from a local system to a network, use the following values for the *StartName* and *StartPassword* parameters:</span></span>


```C++
StartName = "NT AUTHORITY\NetworkService"
StartPassword = "" // - empty string, not NULL
```



## <a name="requirements"></a><span data-ttu-id="55df6-274">Требования</span><span class="sxs-lookup"><span data-stu-id="55df6-274">Requirements</span></span>



| <span data-ttu-id="55df6-275">Требование</span><span class="sxs-lookup"><span data-stu-id="55df6-275">Requirement</span></span> | <span data-ttu-id="55df6-276">Значение</span><span class="sxs-lookup"><span data-stu-id="55df6-276">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="55df6-277">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="55df6-277">Minimum supported client</span></span><br/> | <span data-ttu-id="55df6-278">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="55df6-278">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="55df6-279">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="55df6-279">Minimum supported server</span></span><br/> | <span data-ttu-id="55df6-280">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="55df6-280">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="55df6-281">Пространство имен</span><span class="sxs-lookup"><span data-stu-id="55df6-281">Namespace</span></span><br/>                | <span data-ttu-id="55df6-282">Корневой \\ CIMV2</span><span class="sxs-lookup"><span data-stu-id="55df6-282">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="55df6-283">Header</span><span class="sxs-lookup"><span data-stu-id="55df6-283">Header</span></span><br/>                   | <dl> <span data-ttu-id="55df6-284"><dt>Мбнапи. h</dt></span><span class="sxs-lookup"><span data-stu-id="55df6-284"><dt>Mbnapi.h</dt></span></span> </dl>     |
| <span data-ttu-id="55df6-285">MOF</span><span class="sxs-lookup"><span data-stu-id="55df6-285">MOF</span></span><br/>                      | <dl> <span data-ttu-id="55df6-286"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="55df6-286"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="55df6-287">DLL</span><span class="sxs-lookup"><span data-stu-id="55df6-287">DLL</span></span><br/>                      | <dl> <span data-ttu-id="55df6-288"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="55df6-288"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="55df6-289">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="55df6-289">See also</span></span>

<dl> <dt>

<span data-ttu-id="55df6-290">[Классы операционной системы](/previous-versions//aa392727(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="55df6-290">[Operating System Classes](/previous-versions//aa392727(v=vs.85))</span></span>
</dt> <dt>

[<span data-ttu-id="55df6-291">**\_Басесервице Win32**</span><span class="sxs-lookup"><span data-stu-id="55df6-291">**Win32\_BaseService**</span></span>](win32-baseservice.md)
</dt> </dl>

 

