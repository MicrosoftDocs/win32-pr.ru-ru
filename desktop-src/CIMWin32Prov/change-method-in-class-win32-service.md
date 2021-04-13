---
description: Изменяет \_ службу Win32.
ms.assetid: b32753c5-8fcf-44ee-a95f-e4f6076e0f28
ms.tgt_platform: multiple
title: Метод Change класса Win32_Service (Мбнапи. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_Service.Change
api_type:
- COM
api_location:
- CIMWin32.dll
ms.openlocfilehash: 321b27239114fc86861c0360d507db6c8c520a9c
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104539095"
---
# <a name="change-method-of-the-win32_service-class-mbnapih"></a><span data-ttu-id="083f2-103">Метод Change класса Win32_Service (Мбнапи. h)</span><span class="sxs-lookup"><span data-stu-id="083f2-103">Change method of the Win32_Service class (Mbnapi.h)</span></span>

<span data-ttu-id="083f2-104">Метод класса **Change** [WMI](/windows/desktop/WmiSdk/retrieving-a-class) изменяет [**\_ службу Win32**](win32-service.md).</span><span class="sxs-lookup"><span data-stu-id="083f2-104">The **Change** [WMI class](/windows/desktop/WmiSdk/retrieving-a-class) method modifies a [**Win32\_Service**](win32-service.md).</span></span>

<span data-ttu-id="083f2-105">В этом разделе используется синтаксис MOF-файл (MOF).</span><span class="sxs-lookup"><span data-stu-id="083f2-105">This topic uses Managed Object Format (MOF) syntax.</span></span> <span data-ttu-id="083f2-106">Дополнительные сведения об использовании этого метода см. [в разделе вызов метода](/windows/desktop/WmiSdk/calling-a-method).</span><span class="sxs-lookup"><span data-stu-id="083f2-106">For more information about using this method, see [Calling a Method](/windows/desktop/WmiSdk/calling-a-method).</span></span>

## <a name="syntax"></a><span data-ttu-id="083f2-107">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="083f2-107">Syntax</span></span>


```mof
uint32 Change(
  [in] string  DisplayName,
  [in] string  PathName,
  [in] uint32  ServiceType,
  [in] uint32  ErrorControl,
  [in] string  StartMode,
  [in] boolean DesktopInteract,
  [in] string  StartName,
  [in] string  StartPassword,
  [in] string  LoadOrderGroup,
  [in] string  LoadOrderGroupDependencies[],
  [in] string  ServiceDependencies[]
);
```



## <a name="parameters"></a><span data-ttu-id="083f2-108">Параметры</span><span class="sxs-lookup"><span data-stu-id="083f2-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="083f2-109">*DisplayName* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="083f2-109">*DisplayName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="083f2-110">Отображаемое имя для службы.</span><span class="sxs-lookup"><span data-stu-id="083f2-110">The display name of the service.</span></span> <span data-ttu-id="083f2-111">Максимальная длина этой строки равна 256 символам.</span><span class="sxs-lookup"><span data-stu-id="083f2-111">This string has a maximum length of 256 characters.</span></span> <span data-ttu-id="083f2-112">В диспетчере управления службами имя сохраняется с учетом регистра.</span><span class="sxs-lookup"><span data-stu-id="083f2-112">The name is case- preserved in the service control manager.</span></span> <span data-ttu-id="083f2-113">В сравнениях *DisplayName* всегда учитывается регистр.</span><span class="sxs-lookup"><span data-stu-id="083f2-113">*DisplayName* comparisons are always case-insensitive.</span></span>

<span data-ttu-id="083f2-114">Ограничения: принимает то же значение, что и свойство **Name** .</span><span class="sxs-lookup"><span data-stu-id="083f2-114">Constraints: Accepts the same value as the **Name** property.</span></span>

<span data-ttu-id="083f2-115">Например, "Атдиск".</span><span class="sxs-lookup"><span data-stu-id="083f2-115">Example, "Atdisk".</span></span>

</dd> <dt>

<span data-ttu-id="083f2-116">*Путь к файлу* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="083f2-116">*PathName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="083f2-117">Полный путь к исполняемому файлу, реализующему службу, например " \\ СистемныйКорневойКаталог \\ system32 \\ Drivers \\afd.sys".</span><span class="sxs-lookup"><span data-stu-id="083f2-117">The fully qualified path to the executable file that implements the service, for example, "\\SystemRoot\\System32\\drivers\\afd.sys".</span></span>

</dd> <dt>

<span data-ttu-id="083f2-118">*ServiceType* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="083f2-118">*ServiceType* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="083f2-119">Тип служб, предоставляемых процессам, которые их вызывают.</span><span class="sxs-lookup"><span data-stu-id="083f2-119">The type of services provided to processes that call them.</span></span>

<dt>

<span data-ttu-id="083f2-120">1 (0x1)</span><span class="sxs-lookup"><span data-stu-id="083f2-120">1 (0x1)</span></span>
</dt> <dd>

<span data-ttu-id="083f2-121">Драйвер ядра</span><span class="sxs-lookup"><span data-stu-id="083f2-121">Kernel Driver</span></span>

</dd> <dt>

<span data-ttu-id="083f2-122">2 (0x2)</span><span class="sxs-lookup"><span data-stu-id="083f2-122">2 (0x2)</span></span>
</dt> <dd>

<span data-ttu-id="083f2-123">Драйвер файловой системы</span><span class="sxs-lookup"><span data-stu-id="083f2-123">File System Driver</span></span>

</dd> <dt>

<span data-ttu-id="083f2-124">4 (0x4)</span><span class="sxs-lookup"><span data-stu-id="083f2-124">4 (0x4)</span></span>
</dt> <dd>

<span data-ttu-id="083f2-125">Адаптер</span><span class="sxs-lookup"><span data-stu-id="083f2-125">Adapter</span></span>

</dd> <dt>

<span data-ttu-id="083f2-126">8 (0x8)</span><span class="sxs-lookup"><span data-stu-id="083f2-126">8 (0x8)</span></span>
</dt> <dd>

<span data-ttu-id="083f2-127">Драйвер распознавателя</span><span class="sxs-lookup"><span data-stu-id="083f2-127">Recognizer Driver</span></span>

</dd> <dt>

<span data-ttu-id="083f2-128">16 (0x10)</span><span class="sxs-lookup"><span data-stu-id="083f2-128">16 (0x10)</span></span>
</dt> <dd>

<span data-ttu-id="083f2-129">Собственный процесс</span><span class="sxs-lookup"><span data-stu-id="083f2-129">Own Process</span></span>

</dd> <dt>

<span data-ttu-id="083f2-130">32 (0x20)</span><span class="sxs-lookup"><span data-stu-id="083f2-130">32 (0x20)</span></span>
</dt> <dd>

<span data-ttu-id="083f2-131">Общий процесс</span><span class="sxs-lookup"><span data-stu-id="083f2-131">Share Process</span></span>

</dd> <dt>

<span data-ttu-id="083f2-132">256 (0x100)</span><span class="sxs-lookup"><span data-stu-id="083f2-132">256 (0x100)</span></span>
</dt> <dd>

<span data-ttu-id="083f2-133">Интерактивный процесс</span><span class="sxs-lookup"><span data-stu-id="083f2-133">Interactive Process</span></span>

</dd> </dl> </dd> <dt>

<span data-ttu-id="083f2-134">*ErrorControl* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="083f2-134">*ErrorControl* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="083f2-135">Серьезность ошибки, если не удается запустить службу во время запуска.</span><span class="sxs-lookup"><span data-stu-id="083f2-135">Severity of the error if this service fails to start during startup.</span></span> <span data-ttu-id="083f2-136">Значение указывает действие, предпринимаемое программой запуска, если происходит сбой.</span><span class="sxs-lookup"><span data-stu-id="083f2-136">The value indicates the action taken by the startup program if failure occurs.</span></span> <span data-ttu-id="083f2-137">Все ошибки регистрируются системой.</span><span class="sxs-lookup"><span data-stu-id="083f2-137">All errors are logged by the system.</span></span>

<dt>

<span id="Ignore"></span><span id="ignore"></span><span id="IGNORE"></span>

<span data-ttu-id="083f2-138"><span id="Ignore"></span><span id="ignore"></span><span id="IGNORE"></span>**Игнорировать** (0)</span><span class="sxs-lookup"><span data-stu-id="083f2-138"><span id="Ignore"></span><span id="ignore"></span><span id="IGNORE"></span>**Ignore** (0)</span></span>


</dt> <dd>

<span data-ttu-id="083f2-139">Пользователь не получает уведомление.</span><span class="sxs-lookup"><span data-stu-id="083f2-139">User is not notified.</span></span>

</dd> <dt>

<span id="Normal"></span><span id="normal"></span><span id="NORMAL"></span>

<span data-ttu-id="083f2-140"><span id="Normal"></span><span id="normal"></span><span id="NORMAL"></span>**Обычная** (1)</span><span class="sxs-lookup"><span data-stu-id="083f2-140"><span id="Normal"></span><span id="normal"></span><span id="NORMAL"></span>**Normal** (1)</span></span>


</dt> <dd>

<span data-ttu-id="083f2-141">Нормальный.</span><span class="sxs-lookup"><span data-stu-id="083f2-141">Normal.</span></span> <span data-ttu-id="083f2-142">Пользователь получает уведомление.</span><span class="sxs-lookup"><span data-stu-id="083f2-142">User is notified.</span></span>

</dd> <dt>

<span id="Severe"></span><span id="severe"></span><span id="SEVERE"></span>

<span data-ttu-id="083f2-143"><span id="Severe"></span><span id="severe"></span><span id="SEVERE"></span>**Серьезная** (2)</span><span class="sxs-lookup"><span data-stu-id="083f2-143"><span id="Severe"></span><span id="severe"></span><span id="SEVERE"></span>**Severe** (2)</span></span>


</dt> <dd>

<span data-ttu-id="083f2-144">Система перезапускается с последней удачной конфигурацией.</span><span class="sxs-lookup"><span data-stu-id="083f2-144">System is restarted with the last good configuration.</span></span>

</dd> <dt>

<span id="Critical"></span><span id="critical"></span><span id="CRITICAL"></span>

<span data-ttu-id="083f2-145"><span id="Critical"></span><span id="critical"></span><span id="CRITICAL"></span>**Критическая** (3)</span><span class="sxs-lookup"><span data-stu-id="083f2-145"><span id="Critical"></span><span id="critical"></span><span id="CRITICAL"></span>**Critical** (3)</span></span>


</dt> <dd>

<span data-ttu-id="083f2-146">Попытка перезапустить систему в рабочей конфигурации.</span><span class="sxs-lookup"><span data-stu-id="083f2-146">System attempts to restart with a good configuration.</span></span>

</dd> </dl> </dd> <dt>

<span data-ttu-id="083f2-147">*StartMode* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="083f2-147">*StartMode* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="083f2-148">Режим запуска базовой службы Windows.</span><span class="sxs-lookup"><span data-stu-id="083f2-148">Start mode of the Windows base service.</span></span> <span data-ttu-id="083f2-149">Дополнительные сведения см. в разделе "Замечания".</span><span class="sxs-lookup"><span data-stu-id="083f2-149">For more information, see the Remarks section.</span></span>

<dt>

<span data-ttu-id="083f2-150">Загрузка</span><span class="sxs-lookup"><span data-stu-id="083f2-150">Boot</span></span>
</dt> <dd>

<span data-ttu-id="083f2-151">Драйвер устройства запущен загрузчиком операционной системы.</span><span class="sxs-lookup"><span data-stu-id="083f2-151">Device driver started by the operating system loader.</span></span> <span data-ttu-id="083f2-152">Это значение допустимо только для служб драйверов.</span><span class="sxs-lookup"><span data-stu-id="083f2-152">This value is valid only for driver services.</span></span>

</dd> <dt>

<span data-ttu-id="083f2-153">Система</span><span class="sxs-lookup"><span data-stu-id="083f2-153">System</span></span>
</dt> <dd>

<span data-ttu-id="083f2-154">Драйвер устройства запущен процессом инициализации операционной системы.</span><span class="sxs-lookup"><span data-stu-id="083f2-154">Device driver started by the operating system initialization process.</span></span> <span data-ttu-id="083f2-155">Это значение допустимо только для служб драйверов.</span><span class="sxs-lookup"><span data-stu-id="083f2-155">This value is valid only for driver services.</span></span>

</dd> <dt>

<span data-ttu-id="083f2-156">Автоматически</span><span class="sxs-lookup"><span data-stu-id="083f2-156">Automatic</span></span>
</dt> <dd>

<span data-ttu-id="083f2-157">Служба запускается автоматически диспетчером управления службами во время запуска системы.</span><span class="sxs-lookup"><span data-stu-id="083f2-157">Service to be started automatically by the Service Control Manager during system startup.</span></span>

</dd> <dt>

<span data-ttu-id="083f2-158">Вручную</span><span class="sxs-lookup"><span data-stu-id="083f2-158">Manual</span></span>
</dt> <dd>

<span data-ttu-id="083f2-159">Служба, запускаемая диспетчером управления службами, когда процесс вызывает метод [**StartService**](startservice-method-in-class-win32-service.md) .</span><span class="sxs-lookup"><span data-stu-id="083f2-159">Service to be started by the Service Control Manager when a process calls the [**StartService**](startservice-method-in-class-win32-service.md) method.</span></span>

</dd> <dt>

<span data-ttu-id="083f2-160">Выключено</span><span class="sxs-lookup"><span data-stu-id="083f2-160">Disabled</span></span>
</dt> <dd>

<span data-ttu-id="083f2-161">Служба, которая больше не может быть запущена.</span><span class="sxs-lookup"><span data-stu-id="083f2-161">Service that can no longer be started.</span></span>

</dd> </dl> </dd> <dt>

<span data-ttu-id="083f2-162">*Десктопинтеракт* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="083f2-162">*DesktopInteract* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="083f2-163">Если **значение — true**, служба может создавать окно на рабочем столе или взаимодействовать с ним.</span><span class="sxs-lookup"><span data-stu-id="083f2-163">If **True**, the service can create or communicate with a window on the desktop.</span></span>

</dd> <dt>

<span data-ttu-id="083f2-164">*StartName* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="083f2-164">*StartName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="083f2-165">Имя учетной записи, в которой выполняется служба.</span><span class="sxs-lookup"><span data-stu-id="083f2-165">Account name the service runs under.</span></span> <span data-ttu-id="083f2-166">В зависимости от типа службы имя учетной записи может быть в формате имя_домена \\ имя пользователя или. \\ Имен.</span><span class="sxs-lookup"><span data-stu-id="083f2-166">Depending on the service type, the account name may be in the form of DomainName\\Username or .\\Username.</span></span> <span data-ttu-id="083f2-167">Процесс службы будет заноситься в журнал с использованием одной из этих двух форм при запуске.</span><span class="sxs-lookup"><span data-stu-id="083f2-167">The service process will be logged using one of these two forms when it runs.</span></span> <span data-ttu-id="083f2-168">Если учетная запись принадлежит к встроенному домену,. \\ Можно указать имя пользователя.</span><span class="sxs-lookup"><span data-stu-id="083f2-168">If the account belongs to the built-in domain, .\\Username can be specified.</span></span> <span data-ttu-id="083f2-169">Если указано **значение NULL** , служба будет входить в систему как учетная запись LocalSystem.</span><span class="sxs-lookup"><span data-stu-id="083f2-169">If **NULL** is specified, the service will be logged on as the LocalSystem account.</span></span> <span data-ttu-id="083f2-170">Для драйверов ядра или системного уровня *StartName* содержит имя объекта драйвера (то есть \\ FileSystem \\ RDR или \\ Driver \\ КСНС), которое используется системой ввода и вывода для загрузки драйвера устройства.</span><span class="sxs-lookup"><span data-stu-id="083f2-170">For kernel or system-level drivers, *StartName* contains the driver object name (that is, \\FileSystem\\Rdr or \\Driver\\Xns) that the input and output (I/O) system uses to load the device driver.</span></span> <span data-ttu-id="083f2-171">Если указано **значение NULL** , драйвер запускается с именем объекта по умолчанию, созданным системой ввода-вывода на основе имени службы, например "двдом \\ Admin".</span><span class="sxs-lookup"><span data-stu-id="083f2-171">If **NULL** is specified, the driver runs with a default object name created by the I/O system based on the service name, for example, "DWDOM\\Admin".</span></span>

<span data-ttu-id="083f2-172">Можно также использовать формат имени участника-пользователя (UPN) для указания **StartName**, например *Username@DomainName* .</span><span class="sxs-lookup"><span data-stu-id="083f2-172">You also can use the User Principal Name (UPN) format to specify the **StartName**, for example, *Username@DomainName*.</span></span>

</dd> <dt>

<span data-ttu-id="083f2-173">*Стартпассворд* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="083f2-173">*StartPassword* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="083f2-174">Пароль к имени учетной записи, заданному параметром *StartName* .</span><span class="sxs-lookup"><span data-stu-id="083f2-174">Password to the account name specified by the *StartName* parameter.</span></span> <span data-ttu-id="083f2-175">Если пароль не изменяется, укажите **значение NULL** .</span><span class="sxs-lookup"><span data-stu-id="083f2-175">Specify **NULL** if you are not changing the password.</span></span> <span data-ttu-id="083f2-176">Если служба не имеет пароля, указывается пустая строка.</span><span class="sxs-lookup"><span data-stu-id="083f2-176">Specify an empty string if the service has no password.</span></span>

> [!Note]  
> <span data-ttu-id="083f2-177">При изменении службы с локальной системы на сеть или из сети в локальную систему *стартпассворд* должен быть пустой строкой (""), а не **null**.</span><span class="sxs-lookup"><span data-stu-id="083f2-177">When changing a service from a local system to a network, or from a network to a local system, *StartPassword* must be an empty string ("") and not **NULL**.</span></span>

 

</dd> <dt>

<span data-ttu-id="083f2-178">*Лоадордерграуп* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="083f2-178">*LoadOrderGroup* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="083f2-179">Имя группы, с которой она связана.</span><span class="sxs-lookup"><span data-stu-id="083f2-179">Group name that it is associated with.</span></span> <span data-ttu-id="083f2-180">Группы порядка загрузки содержатся в системном реестре и определяют последовательность, в которой службы загружаются в операционную систему.</span><span class="sxs-lookup"><span data-stu-id="083f2-180">Load order groups are contained in the system registry, and determine the sequence in which services are loaded into the operating system.</span></span> <span data-ttu-id="083f2-181">Если указатель равен **null** или указывает на пустую строку, служба не принадлежит группе.</span><span class="sxs-lookup"><span data-stu-id="083f2-181">If the pointer is **NULL**, or if it points to an empty string, the service does not belong to a group.</span></span> <span data-ttu-id="083f2-182">Дополнительные сведения см. в разделе "Замечания".</span><span class="sxs-lookup"><span data-stu-id="083f2-182">For more information, see the Remarks section.</span></span>

<span data-ttu-id="083f2-183">Зависимости между группами должны быть перечислены в параметре *лоадордерграупдепенденЦиес* .</span><span class="sxs-lookup"><span data-stu-id="083f2-183">Dependencies between groups should be listed in the *LoadOrderGroupDependencies* parameter.</span></span> <span data-ttu-id="083f2-184">Сначала запускаются службы в списке группы упорядочения нагрузки, а затем — службы в группах, которые не входят в список групп порядка загрузки, за которыми следуют службы, не входящие в группу.</span><span class="sxs-lookup"><span data-stu-id="083f2-184">Services in the load-ordering group list are started first, followed by services in groups not in the load-ordering group list, followed by services that do not belong to a group.</span></span> <span data-ttu-id="083f2-185">Системный реестр содержит список групп упорядочения нагрузки, расположенных по адресу:</span><span class="sxs-lookup"><span data-stu-id="083f2-185">The system registry has a list of load ordering groups located at:</span></span>

<span data-ttu-id="083f2-186">**HKey \_ \_** \\  \\  \\  \\ **ServiceGroupOrder** управления CurrentControlSet системы локального компьютера</span><span class="sxs-lookup"><span data-stu-id="083f2-186">**HKEY\_LOCAL\_MACHINE**\\**System**\\**CurrentControlSet**\\**Control**\\**ServiceGroupOrder**</span></span>

</dd> <dt>

<span data-ttu-id="083f2-187">*ЛоадордерграупдепенденЦиес* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="083f2-187">*LoadOrderGroupDependencies* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="083f2-188">Список групп упорядочивания нагрузки, которые должны быть запущены перед запуском этой службы.</span><span class="sxs-lookup"><span data-stu-id="083f2-188">List of load-ordering groups that must start before this service starts.</span></span> <span data-ttu-id="083f2-189">Массив завершается двойным **нулем.**</span><span class="sxs-lookup"><span data-stu-id="083f2-189">The array is doubly **null**-terminated.</span></span> <span data-ttu-id="083f2-190">Если указатель имеет **значение NULL** или указывает на пустую строку, служба не имеет зависимостей.</span><span class="sxs-lookup"><span data-stu-id="083f2-190">If the pointer is **NULL**, or if it points to an empty string, the service has no dependencies.</span></span> <span data-ttu-id="083f2-191">Имена групп должны быть префиксом **\_ \_ идентификатора группы SC** (определенного в файле винсвк. h), чтобы отличать их от имен служб, так как службы и группы служб используют одно и то же пространство имен.</span><span class="sxs-lookup"><span data-stu-id="083f2-191">Group names must be prefixed by the **SC\_GROUP\_IDENTIFIER** (defined in the Winsvc.h file) character to differentiate them from service names because services and service groups share the same namespace.</span></span> <span data-ttu-id="083f2-192">Зависимость от группы означает, что эту службу можно запустить, если хотя бы один член группы запущен после попытки запуска всех членов группы.</span><span class="sxs-lookup"><span data-stu-id="083f2-192">Dependency on a group means that this service can run if at least one member of the group is running after an attempt to start all of the members of the group.</span></span>

</dd> <dt>

<span data-ttu-id="083f2-193">*СервицедепенденЦиес* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="083f2-193">*ServiceDependencies* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="083f2-194">Список, содержащий имена служб, которые должны быть запущены перед запуском этой службы.</span><span class="sxs-lookup"><span data-stu-id="083f2-194">List that contains the names of services that must start before this service starts.</span></span> <span data-ttu-id="083f2-195">Массив завершается двойным **нулем.**</span><span class="sxs-lookup"><span data-stu-id="083f2-195">The array is doubly **NULL**-terminated.</span></span> <span data-ttu-id="083f2-196">Если указатель имеет **значение NULL** или указывает на пустую строку, служба не имеет зависимостей.</span><span class="sxs-lookup"><span data-stu-id="083f2-196">If the pointer is **NULL**, or if it points to an empty string, the service has no dependencies.</span></span> <span data-ttu-id="083f2-197">Зависимость от службы указывает, что эта служба может выполняться, только если запущена служба, от которой она зависит.</span><span class="sxs-lookup"><span data-stu-id="083f2-197">Dependency on a service indicates that this service can run only if the service it depends on is running.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="083f2-198">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="083f2-198">Return value</span></span>

<span data-ttu-id="083f2-199">Возвращает одно из значений, перечисленных в следующем списке, или любое другое значение, указывающее на ошибку.</span><span class="sxs-lookup"><span data-stu-id="083f2-199">Returns one of the values listed in the following list, or any other value to indicate an error.</span></span> <span data-ttu-id="083f2-200">Дополнительные коды ошибок см. в разделе [**константы WMI Error**](/windows/desktop/WmiSdk/wmi-error-constants) или [**вбемерроренум**](/windows/desktop/api/wbemdisp/ne-wbemdisp-wbemerrorenum).</span><span class="sxs-lookup"><span data-stu-id="083f2-200">For additional error codes, see [**WMI Error Constants**](/windows/desktop/WmiSdk/wmi-error-constants) or [**WbemErrorEnum**](/windows/desktop/api/wbemdisp/ne-wbemdisp-wbemerrorenum).</span></span> <span data-ttu-id="083f2-201">Общие значения **HRESULT** см. в разделе [коды системных ошибок](/windows/desktop/Debug/system-error-codes).</span><span class="sxs-lookup"><span data-stu-id="083f2-201">For general **HRESULT** values, see [System Error Codes](/windows/desktop/Debug/system-error-codes).</span></span>

<dl> <dt>

<span data-ttu-id="083f2-202">**Успешно**</span><span class="sxs-lookup"><span data-stu-id="083f2-202">**Success**</span></span>
</dt> <dd>

<span data-ttu-id="083f2-203">0</span><span class="sxs-lookup"><span data-stu-id="083f2-203">0</span></span>

<span data-ttu-id="083f2-204">Запрос принят.</span><span class="sxs-lookup"><span data-stu-id="083f2-204">The request was accepted.</span></span>

</dd> <dt>

<span data-ttu-id="083f2-205">**Не поддерживается**</span><span class="sxs-lookup"><span data-stu-id="083f2-205">**Not Supported**</span></span>
</dt> <dd>

<span data-ttu-id="083f2-206">1</span><span class="sxs-lookup"><span data-stu-id="083f2-206">1</span></span>

<span data-ttu-id="083f2-207">Запрос не поддерживается.</span><span class="sxs-lookup"><span data-stu-id="083f2-207">The request is not supported.</span></span>

</dd> <dt>

<span data-ttu-id="083f2-208">**Доступ запрещен**</span><span class="sxs-lookup"><span data-stu-id="083f2-208">**Access Denied**</span></span>
</dt> <dd>

<span data-ttu-id="083f2-209">2</span><span class="sxs-lookup"><span data-stu-id="083f2-209">2</span></span>

<span data-ttu-id="083f2-210">У пользователя нет необходимых прав доступа.</span><span class="sxs-lookup"><span data-stu-id="083f2-210">The user did not have the necessary access.</span></span>

</dd> <dt>

<span data-ttu-id="083f2-211">**Работающие зависимые службы**</span><span class="sxs-lookup"><span data-stu-id="083f2-211">**Dependent Services Running**</span></span>
</dt> <dd>

<span data-ttu-id="083f2-212">3</span><span class="sxs-lookup"><span data-stu-id="083f2-212">3</span></span>

<span data-ttu-id="083f2-213">Службу нельзя остановить, так как от нее зависят другие работающие службы.</span><span class="sxs-lookup"><span data-stu-id="083f2-213">The service cannot be stopped because other services that are running are dependent on it.</span></span>

</dd> <dt>

<span data-ttu-id="083f2-214">**Недопустимый элемент управления службой**</span><span class="sxs-lookup"><span data-stu-id="083f2-214">**Invalid Service Control**</span></span>
</dt> <dd>

<span data-ttu-id="083f2-215">4</span><span class="sxs-lookup"><span data-stu-id="083f2-215">4</span></span>

<span data-ttu-id="083f2-216">Запрошенный управляющий код недопустим или неприемлем для данной службы.</span><span class="sxs-lookup"><span data-stu-id="083f2-216">The requested control code is not valid, or it is unacceptable to the service.</span></span>

</dd> <dt>

<span data-ttu-id="083f2-217">**Служба не может принять контроль**</span><span class="sxs-lookup"><span data-stu-id="083f2-217">**Service Cannot Accept Control**</span></span>
</dt> <dd>

<span data-ttu-id="083f2-218">5</span><span class="sxs-lookup"><span data-stu-id="083f2-218">5</span></span>

<span data-ttu-id="083f2-219">Запрошенный управляющий код не может быть отправлен в службу, так как это состояние службы ([**Win32 \_ басесервице**](win32-baseservice.md).**Свойство State** ) равно 0, 1 или 2.</span><span class="sxs-lookup"><span data-stu-id="083f2-219">The requested control code cannot be sent to the service because the state of the service ([**Win32\_BaseService**](win32-baseservice.md).**State** property) is equal to 0, 1, or 2.</span></span>

</dd> <dt>

<span data-ttu-id="083f2-220">**Служба неактивна**</span><span class="sxs-lookup"><span data-stu-id="083f2-220">**Service Not Active**</span></span>
</dt> <dd>

<span data-ttu-id="083f2-221">6</span><span class="sxs-lookup"><span data-stu-id="083f2-221">6</span></span>

<span data-ttu-id="083f2-222">Служба не запущена.</span><span class="sxs-lookup"><span data-stu-id="083f2-222">The service has not been started.</span></span>

</dd> <dt>

<span data-ttu-id="083f2-223">**Время ожидания запроса на обслуживание**</span><span class="sxs-lookup"><span data-stu-id="083f2-223">**Service Request Timeout**</span></span>
</dt> <dd>

<span data-ttu-id="083f2-224">7</span><span class="sxs-lookup"><span data-stu-id="083f2-224">7</span></span>

<span data-ttu-id="083f2-225">Служба не ответила на запрос запуска за отведенное время.</span><span class="sxs-lookup"><span data-stu-id="083f2-225">The service did not respond to the start request in a timely fashion.</span></span>

</dd> <dt>

<span data-ttu-id="083f2-226">**Неизвестный сбой**</span><span class="sxs-lookup"><span data-stu-id="083f2-226">**Unknown Failure**</span></span>
</dt> <dd>

<span data-ttu-id="083f2-227">8</span><span class="sxs-lookup"><span data-stu-id="083f2-227">8</span></span>

<span data-ttu-id="083f2-228">Неизвестный сбой при запуске службы.</span><span class="sxs-lookup"><span data-stu-id="083f2-228">Unknown failure when starting the service.</span></span>

</dd> <dt>

<span data-ttu-id="083f2-229">**Путь не найден**</span><span class="sxs-lookup"><span data-stu-id="083f2-229">**Path Not Found**</span></span>
</dt> <dd>

<span data-ttu-id="083f2-230">9</span><span class="sxs-lookup"><span data-stu-id="083f2-230">9</span></span>

<span data-ttu-id="083f2-231">Не найден путь к каталогу исполняемого файла службы.</span><span class="sxs-lookup"><span data-stu-id="083f2-231">The directory path to the service executable file was not found.</span></span>

</dd> <dt>

<span data-ttu-id="083f2-232">**Служба уже запущена**</span><span class="sxs-lookup"><span data-stu-id="083f2-232">**Service Already Running**</span></span>
</dt> <dd>

<span data-ttu-id="083f2-233">10</span><span class="sxs-lookup"><span data-stu-id="083f2-233">10</span></span>

<span data-ttu-id="083f2-234">Служба уже запущена.</span><span class="sxs-lookup"><span data-stu-id="083f2-234">The service is already running.</span></span>

</dd> <dt>

<span data-ttu-id="083f2-235">**База данных службы заблокирована**</span><span class="sxs-lookup"><span data-stu-id="083f2-235">**Service Database Locked**</span></span>
</dt> <dd>

<span data-ttu-id="083f2-236">11</span><span class="sxs-lookup"><span data-stu-id="083f2-236">11</span></span>

<span data-ttu-id="083f2-237">База данных для добавления новой службы заблокирована.</span><span class="sxs-lookup"><span data-stu-id="083f2-237">The database to add a new service is locked.</span></span>

</dd> <dt>

<span data-ttu-id="083f2-238">**Зависимость службы удалена**</span><span class="sxs-lookup"><span data-stu-id="083f2-238">**Service Dependency Deleted**</span></span>
</dt> <dd>

<span data-ttu-id="083f2-239">12</span><span class="sxs-lookup"><span data-stu-id="083f2-239">12</span></span>

<span data-ttu-id="083f2-240">Зависимость, от которой зависит эта служба, удалена из системы.</span><span class="sxs-lookup"><span data-stu-id="083f2-240">A dependency this service relies on has been removed from the system.</span></span>

</dd> <dt>

<span data-ttu-id="083f2-241">**Сбой зависимости службы**</span><span class="sxs-lookup"><span data-stu-id="083f2-241">**Service Dependency Failure**</span></span>
</dt> <dd>

<span data-ttu-id="083f2-242">13</span><span class="sxs-lookup"><span data-stu-id="083f2-242">13</span></span>

<span data-ttu-id="083f2-243">Этой службе не удалось найти службу, которая необходима зависимой службе.</span><span class="sxs-lookup"><span data-stu-id="083f2-243">The service failed to find the service needed from a dependent service.</span></span>

</dd> <dt>

<span data-ttu-id="083f2-244">**Служба отключена**</span><span class="sxs-lookup"><span data-stu-id="083f2-244">**Service Disabled**</span></span>
</dt> <dd>

<span data-ttu-id="083f2-245">14</span><span class="sxs-lookup"><span data-stu-id="083f2-245">14</span></span>

<span data-ttu-id="083f2-246">Эта служба была отключена в системе.</span><span class="sxs-lookup"><span data-stu-id="083f2-246">The service has been disabled from the system.</span></span>

</dd> <dt>

<span data-ttu-id="083f2-247">**Сбой при входе в службу**</span><span class="sxs-lookup"><span data-stu-id="083f2-247">**Service Logon Failed**</span></span>
</dt> <dd>

<span data-ttu-id="083f2-248">15</span><span class="sxs-lookup"><span data-stu-id="083f2-248">15</span></span>

<span data-ttu-id="083f2-249">Эта служба не поддерживает проверку подлинности, необходимую для работы в системе.</span><span class="sxs-lookup"><span data-stu-id="083f2-249">The service does not have the correct authentication to run on the system.</span></span>

</dd> <dt>

<span data-ttu-id="083f2-250">**Служба помечена для удаления**</span><span class="sxs-lookup"><span data-stu-id="083f2-250">**Service Marked For Deletion**</span></span>
</dt> <dd>

<span data-ttu-id="083f2-251">16</span><span class="sxs-lookup"><span data-stu-id="083f2-251">16</span></span>

<span data-ttu-id="083f2-252">Эта служба удаляется из системы.</span><span class="sxs-lookup"><span data-stu-id="083f2-252">This service is being removed from the system.</span></span>

</dd> <dt>

<span data-ttu-id="083f2-253">**Служба без потока**</span><span class="sxs-lookup"><span data-stu-id="083f2-253">**Service No Thread**</span></span>
</dt> <dd>

<span data-ttu-id="083f2-254">17</span><span class="sxs-lookup"><span data-stu-id="083f2-254">17</span></span>

<span data-ttu-id="083f2-255">Служба не имеет потока выполнения.</span><span class="sxs-lookup"><span data-stu-id="083f2-255">The service has no execution thread.</span></span>

</dd> <dt>

<span data-ttu-id="083f2-256">**Состояние "циклическая зависимость"**</span><span class="sxs-lookup"><span data-stu-id="083f2-256">**Status Circular Dependency**</span></span>
</dt> <dd>

<span data-ttu-id="083f2-257">18</span><span class="sxs-lookup"><span data-stu-id="083f2-257">18</span></span>

<span data-ttu-id="083f2-258">Служба имеет циклические зависимости при запуске.</span><span class="sxs-lookup"><span data-stu-id="083f2-258">The service has circular dependencies when it starts.</span></span>

</dd> <dt>

<span data-ttu-id="083f2-259">**Состояние "повторяющееся имя"**</span><span class="sxs-lookup"><span data-stu-id="083f2-259">**Status Duplicate Name**</span></span>
</dt> <dd>

<span data-ttu-id="083f2-260">19</span><span class="sxs-lookup"><span data-stu-id="083f2-260">19</span></span>

<span data-ttu-id="083f2-261">Служба выполняется с тем же именем.</span><span class="sxs-lookup"><span data-stu-id="083f2-261">A service is running under the same name.</span></span>

</dd> <dt>

<span data-ttu-id="083f2-262">**Состояние "Недопустимое имя"**</span><span class="sxs-lookup"><span data-stu-id="083f2-262">**Status Invalid Name**</span></span>
</dt> <dd>

<span data-ttu-id="083f2-263">20</span><span class="sxs-lookup"><span data-stu-id="083f2-263">20</span></span>

<span data-ttu-id="083f2-264">Имя службы содержит недопустимые символы.</span><span class="sxs-lookup"><span data-stu-id="083f2-264">The service name has invalid characters.</span></span>

</dd> <dt>

<span data-ttu-id="083f2-265">**Недопустимый параметр Status**</span><span class="sxs-lookup"><span data-stu-id="083f2-265">**Status Invalid Parameter**</span></span>
</dt> <dd>

<span data-ttu-id="083f2-266">21</span><span class="sxs-lookup"><span data-stu-id="083f2-266">21</span></span>

<span data-ttu-id="083f2-267">Службе переданы недопустимые параметры.</span><span class="sxs-lookup"><span data-stu-id="083f2-267">Invalid parameters have been passed to the service.</span></span>

</dd> <dt>

<span data-ttu-id="083f2-268">**Недопустимое состояние учетной записи службы**</span><span class="sxs-lookup"><span data-stu-id="083f2-268">**Status Invalid Service Account**</span></span>
</dt> <dd>

<span data-ttu-id="083f2-269">22</span><span class="sxs-lookup"><span data-stu-id="083f2-269">22</span></span>

<span data-ttu-id="083f2-270">Учетная запись, под которой работает эта служба, либо недопустима, либо не имеет разрешений на запуск службы.</span><span class="sxs-lookup"><span data-stu-id="083f2-270">The account under which this service runs is either invalid or lacks the permissions to run the service.</span></span>

</dd> <dt>

<span data-ttu-id="083f2-271">**Служба состояний существует**</span><span class="sxs-lookup"><span data-stu-id="083f2-271">**Status Service Exists**</span></span>
</dt> <dd>

<span data-ttu-id="083f2-272">23</span><span class="sxs-lookup"><span data-stu-id="083f2-272">23</span></span>

<span data-ttu-id="083f2-273">Служба существует в базе данных доступных в системе служб.</span><span class="sxs-lookup"><span data-stu-id="083f2-273">The service exists in the database of services available from the system.</span></span>

</dd> <dt>

<span data-ttu-id="083f2-274">**Служба уже приостановлена**</span><span class="sxs-lookup"><span data-stu-id="083f2-274">**Service Already Paused**</span></span>
</dt> <dd>

<span data-ttu-id="083f2-275">24</span><span class="sxs-lookup"><span data-stu-id="083f2-275">24</span></span>

<span data-ttu-id="083f2-276">Служба в данный момент приостановлена в системе.</span><span class="sxs-lookup"><span data-stu-id="083f2-276">The service is currently paused in the system.</span></span>

</dd> <dt>

<span data-ttu-id="083f2-277">**Другое**</span><span class="sxs-lookup"><span data-stu-id="083f2-277">**Other**</span></span>
</dt> <dd>

<span data-ttu-id="083f2-278">25 4294967295</span><span class="sxs-lookup"><span data-stu-id="083f2-278">25 4294967295</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="083f2-279">Комментарии</span><span class="sxs-lookup"><span data-stu-id="083f2-279">Remarks</span></span>

<span data-ttu-id="083f2-280">При запуске компьютера также запускаются все службы автозапуска.</span><span class="sxs-lookup"><span data-stu-id="083f2-280">When a computer starts, all the autostart services also start.</span></span> <span data-ttu-id="083f2-281">Иногда одна из этих служб может не запускаться вместе с компьютером.</span><span class="sxs-lookup"><span data-stu-id="083f2-281">On occasion, one of these services might fail to start along with the computer.</span></span> <span data-ttu-id="083f2-282">При сбое службы во время запуска системы компьютер принимает действия в соответствии со значением управляющего кода ошибки службы.</span><span class="sxs-lookup"><span data-stu-id="083f2-282">When a service fails during system startup, the computer takes action based on the value of the service error control code.</span></span>

<span data-ttu-id="083f2-283">Большинство служб устанавливаются с помощью обычного управляющего кода ошибок.</span><span class="sxs-lookup"><span data-stu-id="083f2-283">most services are installed using the Normal error control code.</span></span> <span data-ttu-id="083f2-284">Некоторые исключения, которые устанавливаются с помощью команды игнорировать код ошибки, включают:</span><span class="sxs-lookup"><span data-stu-id="083f2-284">A few of the exceptions, which are installed using the Ignore error code, include:</span></span>

-   <span data-ttu-id="083f2-285">Служба репликации файлов</span><span class="sxs-lookup"><span data-stu-id="083f2-285">File Replication Service</span></span>
-   <span data-ttu-id="083f2-286">Смарт-карта</span><span class="sxs-lookup"><span data-stu-id="083f2-286">Smart Card</span></span>
-   <span data-ttu-id="083f2-287">Вторичный вход в систему</span><span class="sxs-lookup"><span data-stu-id="083f2-287">Secondary Logon</span></span>
-   <span data-ttu-id="083f2-288">WMI</span><span class="sxs-lookup"><span data-stu-id="083f2-288">WMI</span></span>

<span data-ttu-id="083f2-289">Для служб, установленных с помощью команды игнорировать код ошибки, пользователю не выдается уведомление о том, что служба завершилась ошибкой.</span><span class="sxs-lookup"><span data-stu-id="083f2-289">For the services installed using the Ignore error code, no notification is given to the user that the service has failed.</span></span> <span data-ttu-id="083f2-290">Если вы предпочитаете на экране уведомление о том, что не удалось запустить службу, можно использовать инструментарий WMI для изменения управляющего кода ошибки.</span><span class="sxs-lookup"><span data-stu-id="083f2-290">If you prefer on-screen notification that a service could not start, you can use WMI to change the error control code.</span></span> <span data-ttu-id="083f2-291">Коды управления ошибками применяются только к загрузке компьютера; управляющие коды ошибок не используются, если вы останавливаете и попытаетесь перезапустить службу после запуска компьютера.</span><span class="sxs-lookup"><span data-stu-id="083f2-291">Error control codes apply only to computer startup; error control codes are not used if you stop and then attempt to restart a service after the computer is running.</span></span>

<span data-ttu-id="083f2-292">Иногда может потребоваться изменить учетную запись, под которой работает данная служба.</span><span class="sxs-lookup"><span data-stu-id="083f2-292">On occasion, you might need to change the account under which a given service runs.</span></span> <span data-ttu-id="083f2-293">Например, служба может запускаться под административной учетной записью.</span><span class="sxs-lookup"><span data-stu-id="083f2-293">For example, you might run a service under an administrative account.</span></span> <span data-ttu-id="083f2-294">Поскольку это может привести к уязвимости системы безопасности, можно переключить службу на учетную запись с меньшим числом привилегий.</span><span class="sxs-lookup"><span data-stu-id="083f2-294">Because this can create a security vulnerability, you might switch the service to an account with fewer privileges.</span></span> <span data-ttu-id="083f2-295">Кроме того, могут быть запущены службы с учетной записью, которая будет удалена, или необходимо убедиться, что на всех серверах некоторые службы выполняются под определенными учетными записями.</span><span class="sxs-lookup"><span data-stu-id="083f2-295">Alternatively, you might have services running under an account that is about to be deleted, or you might want to ensure that, on all your servers, certain services run under certain accounts.</span></span> <span data-ttu-id="083f2-296">Можно использовать метод **Change** класса [**\_ службы Win32**](win32-service.md) , чтобы настроить службы для работы с указанной учетной записью пользователя.</span><span class="sxs-lookup"><span data-stu-id="083f2-296">You can use the **Change** method of the [**Win32\_Service**](win32-service.md) class to configure services to run under a specified user account.</span></span> <span data-ttu-id="083f2-297">При выборе учетной записи учитывайте следующее.</span><span class="sxs-lookup"><span data-stu-id="083f2-297">When selecting an account, keep in mind the following:</span></span>

-   <span data-ttu-id="083f2-298">Учетная запись, используемая в качестве учетной записи службы, должна иметь право на вход в качестве службы.</span><span class="sxs-lookup"><span data-stu-id="083f2-298">The account being used as a service account must have the right to log on as a service.</span></span> <span data-ttu-id="083f2-299">Это право можно предоставить с помощью групповая политика.</span><span class="sxs-lookup"><span data-stu-id="083f2-299">This right can be granted by using Group Policy.</span></span>
-   <span data-ttu-id="083f2-300">Учетная запись, используемая как учетная запись службы, не должна быть членом локальной группы администраторов, домена или администратора предприятия.</span><span class="sxs-lookup"><span data-stu-id="083f2-300">The account being used as a service account should not be a member of a local, domain, or enterprise Administrators group.</span></span>
-   <span data-ttu-id="083f2-301">Каждый экземпляр службы должен работать под уникальной учетной записью пользователя.</span><span class="sxs-lookup"><span data-stu-id="083f2-301">Each instance of a service should run under a unique user account.</span></span> <span data-ttu-id="083f2-302">Это обеспечивает дополнительную безопасность и включает аудит отдельных экземпляров службы.</span><span class="sxs-lookup"><span data-stu-id="083f2-302">This provides additional security, and enables the auditing of individual service instances.</span></span>
-   <span data-ttu-id="083f2-303">Если служба является интерактивной, она должна работать под учетной записью LocalSystem.</span><span class="sxs-lookup"><span data-stu-id="083f2-303">If the service is interactive, then the service must run under the LocalSystem account.</span></span>

    <span data-ttu-id="083f2-304">LocalSystem является обязательным, так как только одна Windows-станция (WinSta0) может быть видимой и интерактивной в каждый момент времени.</span><span class="sxs-lookup"><span data-stu-id="083f2-304">LocalSystem is required because only one window station (WinSta0) can be visible and interactive at a time.</span></span> <span data-ttu-id="083f2-305">Если служба выполняется под учетной записью, отличной от LocalSystem, она выполняется в окне Service-0x03e7 $ \\ Default Windows Station, которое является невидимым окном.</span><span class="sxs-lookup"><span data-stu-id="083f2-305">If a service runs under an account other than LocalSystem, it runs in the Service-0x03e7$\\Default window station, which is an invisible window.</span></span> <span data-ttu-id="083f2-306">Службы, работающие на этой экранной станции, не могут принимать входные данные и отображать выходные данные.</span><span class="sxs-lookup"><span data-stu-id="083f2-306">Services running in this window station cannot receive input or display output.</span></span>

<span data-ttu-id="083f2-307">При назначении учетной записи службе SCM требует для этой учетной записи правильный пароль, прежде чем приступать к назначению.</span><span class="sxs-lookup"><span data-stu-id="083f2-307">When you assign an account to a service, the SCM requires the correct password for that account before it makes the assignment.</span></span> <span data-ttu-id="083f2-308">При указании неверного пароля SCM отклоняет учетную запись.</span><span class="sxs-lookup"><span data-stu-id="083f2-308">If you supply an incorrect password, the SCM rejects the account.</span></span> <span data-ttu-id="083f2-309">Если вы настраиваете учетную запись службы с помощью учетной записи LocalSystem, LocalService или NetworkService, вам не нужно указывать пароль учетной записи, так как у этих учетных записей нет паролей.</span><span class="sxs-lookup"><span data-stu-id="083f2-309">If you configure a service account using the LocalSystem, LocalService, or NetworkService account, you do not need to supply an account password because these accounts do not have passwords.</span></span>

<span data-ttu-id="083f2-310">SCM хранит пароль учетной записи в базе данных служб.</span><span class="sxs-lookup"><span data-stu-id="083f2-310">The SCM stores the account password in the services database.</span></span> <span data-ttu-id="083f2-311">Однако после назначения пароля SCM не гарантирует, что пароль, хранящийся в базе данных служб, и пароль, назначенный учетной записи пользователя в Active Directory, будут по-прежнему совпадать.</span><span class="sxs-lookup"><span data-stu-id="083f2-311">After the password is assigned, however, the SCM does not ensure that the password stored in the services database and the password assigned to the user account in Active Directory continue to match.</span></span> <span data-ttu-id="083f2-312">Следовательно, может произойти ситуация, подобная следующей:</span><span class="sxs-lookup"><span data-stu-id="083f2-312">Consequently, a situation similar to the following could occur:</span></span>

-   <span data-ttu-id="083f2-313">Служба настраивается для запуска от имени определенной учетной записи пользователя.</span><span class="sxs-lookup"><span data-stu-id="083f2-313">You configure a service to run under a particular user account.</span></span>
-   <span data-ttu-id="083f2-314">Служба запускается под этой учетной записью с использованием пароля текущей учетной записи.</span><span class="sxs-lookup"><span data-stu-id="083f2-314">The service starts up under that account by using the current account password.</span></span>
-   <span data-ttu-id="083f2-315">Вы изменяете пароль для учетной записи пользователя.</span><span class="sxs-lookup"><span data-stu-id="083f2-315">You change the password for the user account.</span></span>
-   <span data-ttu-id="083f2-316">Служба продолжит работу.</span><span class="sxs-lookup"><span data-stu-id="083f2-316">The service continues to run.</span></span> <span data-ttu-id="083f2-317">Однако если служба остановлена, ее нельзя перезапустить, так как SCM продолжит использовать старый, недопустимый пароль.</span><span class="sxs-lookup"><span data-stu-id="083f2-317">However, if the service stops, you cannot restart it because the SCM continues to use the old, invalid password.</span></span> <span data-ttu-id="083f2-318">Изменение пароля в Active Directory не приводит к изменению пароля, хранящегося в базе данных служб.</span><span class="sxs-lookup"><span data-stu-id="083f2-318">Changing the password in Active Directory does not change the password stored in the services database.</span></span>

<span data-ttu-id="083f2-319">При запуске служб с обычными учетными записями пользователей необходимо обновлять эти пароли служб при каждом изменении пароля учетной записи пользователя.</span><span class="sxs-lookup"><span data-stu-id="083f2-319">If you run services under regular user accounts, you need to update those service passwords each time the user account password changes.</span></span> <span data-ttu-id="083f2-320">Это может быть особенно трудоемким, если вы не уверены, какие службы выполняются под этой учетной записью или на каких компьютерах выполняются службы с этой учетной записью.</span><span class="sxs-lookup"><span data-stu-id="083f2-320">This can be particularly time-consuming if you are not sure which services are running under that account or which computers have services running under that account.</span></span> <span data-ttu-id="083f2-321">К счастью, вы можете использовать инструментарий WMI для проверки учетных записей служб на всех компьютерах и при необходимости изменить пароль учетной записи службы.</span><span class="sxs-lookup"><span data-stu-id="083f2-321">Fortunately, you can use WMI to check the service accounts on all your computers and, if necessary, change the service account password.</span></span>

<span data-ttu-id="083f2-322">Параметр [**Win32 \_ лоадордерграуп**](win32-loadordergroup.md) представляет группу системных служб, определяющих зависимости выполнения.</span><span class="sxs-lookup"><span data-stu-id="083f2-322">The [**Win32\_LoadOrderGroup**](win32-loadordergroup.md) parameter represents a group of system services that define execution dependencies.</span></span> <span data-ttu-id="083f2-323">Службы должны запускаться в порядке, указанном в группе порядок загрузки, так как службы зависят друг от друга.</span><span class="sxs-lookup"><span data-stu-id="083f2-323">The services must be initiated in the order specified by the Load Order Group because the services depend on each other.</span></span> <span data-ttu-id="083f2-324">Для правильной работы этих зависимых служб требуется наличие предшествующих служб.</span><span class="sxs-lookup"><span data-stu-id="083f2-324">These dependent services require the presence of the antecedent services to function correctly.</span></span>

<span data-ttu-id="083f2-325">Чтобы изменить службу с сетевой службы на локальную систему, параметры *StartName* и *стартпассворд* должны иметь следующие значения:</span><span class="sxs-lookup"><span data-stu-id="083f2-325">To change a service from a network service to a local system the *StartName* and *StartPassword* parameters should have the following values:</span></span>


```C++
StartName = "LocalSystem"
StartPassword = "" // - empty string, not NULL
```



<span data-ttu-id="083f2-326">Чтобы изменить службу с локальной системной службы на сеть, параметры *StartName* и *стартпассворд* должны иметь следующие значения:</span><span class="sxs-lookup"><span data-stu-id="083f2-326">To change a service from a local system service to a network the *StartName* and *StartPassword* parameters should have the following values:</span></span>


```C++
StartName = "NT AUTHORITY\NetworkService"
StartPassword = "" // - empty string, not NULL
```



## <a name="examples"></a><span data-ttu-id="083f2-327">Примеры</span><span class="sxs-lookup"><span data-stu-id="083f2-327">Examples</span></span>

<span data-ttu-id="083f2-328">Следующая команда VBScript изменяет учетную запись службы для служб, выполняемых от имени указанной учетной записи пользователя, на LocalSystem.</span><span class="sxs-lookup"><span data-stu-id="083f2-328">The following VBScript changes the service account for services from running under a specified user account to LocalSystem.</span></span>


```VB
strComputer = "."
Set objWMIService = GetObject("winmgmts:{impersonationLevel=impersonate}!\\" & strComputer & "\Root\CIMv2")
Set colServiceList = objWMIService.ExecQuery("SELECT * FROM Win32_Service WHERE StartName = '.\\NetSvc'")
For Each objService in colServices
 errServiceChange = objService.Change( , , , , , , ".\LocalSystem" , "")
Next
```



<span data-ttu-id="083f2-329">Следующая команда VBScript изменяет пароль учетной записи службы для всех сценариев, выполняемых в Нетсвк</span><span class="sxs-lookup"><span data-stu-id="083f2-329">The following VBScript changes the service account password for all scripts running under Netsvc</span></span>


```VB
strComputer = "."
Set objWMIService = GetObject("winmgmts:{impersonationLevel=impersonate}!\\" & strComputer & "\Root\CIMv2")
Set colServiceList = objWMIService.ExecQuery("SELECT * FROM Win32_Service WHERE StartName = '.\\NetSvc'")
For Each objservice in colServiceList
 errReturn = objService.Change( , , , , , , , "password")
Next
```



## <a name="requirements"></a><span data-ttu-id="083f2-330">Требования</span><span class="sxs-lookup"><span data-stu-id="083f2-330">Requirements</span></span>



| <span data-ttu-id="083f2-331">Требование</span><span class="sxs-lookup"><span data-stu-id="083f2-331">Requirement</span></span> | <span data-ttu-id="083f2-332">Значение</span><span class="sxs-lookup"><span data-stu-id="083f2-332">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="083f2-333">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="083f2-333">Minimum supported client</span></span><br/> | <span data-ttu-id="083f2-334">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="083f2-334">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="083f2-335">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="083f2-335">Minimum supported server</span></span><br/> | <span data-ttu-id="083f2-336">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="083f2-336">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="083f2-337">Пространство имен</span><span class="sxs-lookup"><span data-stu-id="083f2-337">Namespace</span></span><br/>                | <span data-ttu-id="083f2-338">Корневой \\ CIMV2</span><span class="sxs-lookup"><span data-stu-id="083f2-338">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="083f2-339">Header</span><span class="sxs-lookup"><span data-stu-id="083f2-339">Header</span></span><br/>                   | <dl> <span data-ttu-id="083f2-340"><dt>Мбнапи. h</dt></span><span class="sxs-lookup"><span data-stu-id="083f2-340"><dt>Mbnapi.h</dt></span></span> </dl>     |
| <span data-ttu-id="083f2-341">MOF</span><span class="sxs-lookup"><span data-stu-id="083f2-341">MOF</span></span><br/>                      | <dl> <span data-ttu-id="083f2-342"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="083f2-342"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="083f2-343">DLL</span><span class="sxs-lookup"><span data-stu-id="083f2-343">DLL</span></span><br/>                      | <dl> <span data-ttu-id="083f2-344"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="083f2-344"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="083f2-345">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="083f2-345">See also</span></span>

<dl> <dt>

<span data-ttu-id="083f2-346">[Классы операционной системы](/previous-versions//aa392727(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="083f2-346">[Operating System Classes](/previous-versions//aa392727(v=vs.85))</span></span>
</dt> <dt>

[<span data-ttu-id="083f2-347">**\_Служба Win32**</span><span class="sxs-lookup"><span data-stu-id="083f2-347">**Win32\_Service**</span></span>](win32-service.md)
</dt> <dt>

[<span data-ttu-id="083f2-348">Задачи WMI: службы</span><span class="sxs-lookup"><span data-stu-id="083f2-348">WMI Tasks: Services</span></span>](/windows/desktop/WmiSdk/wmi-tasks--services)
</dt> </dl>

 

