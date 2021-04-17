---
title: Метод Change класса Win32_Service (Мбнапи. h)
description: Изменяет \_ Терминалсервице Win32.
ms.assetid: 19E43A80-47C9-4C5A-8E73-723F206AA7C0
ms.tgt_platform: multiple
keywords:
- службы удаленных рабочих столов метода изменения
- Службы удаленных рабочих столов метода изменения, класс Win32_Service
- Класс Win32_Service службы удаленных рабочих столов, метод Change
topic_type:
- apiref
api_name:
- Win32_Service.Change
api_location:
- TSCfgWmi.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f4514d89e47ded60550a28303d0f04e227211e3a
ms.sourcegitcommit: 168d11879cb9fd89d26f826482725c0a626be00f
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/16/2021
ms.locfileid: "105685014"
---
# <a name="change-method-of-the-win32_service-class-mbnapih---terminalservice"></a><span data-ttu-id="4c457-106">Метод Change класса Win32_Service (Мбнапи. h) — Терминалсервице</span><span class="sxs-lookup"><span data-stu-id="4c457-106">Change method of the Win32_Service class (Mbnapi.h) - TerminalService</span></span>

<span data-ttu-id="4c457-107">Метод  [класса WMI](/windows/desktop/WmiSdk/retrieving-a-class) Change изменяет [**\_ терминалсервице Win32**](win32-terminalservice.md).</span><span class="sxs-lookup"><span data-stu-id="4c457-107">The **Change** [WMI class](/windows/desktop/WmiSdk/retrieving-a-class) method modifies a [**Win32\_TerminalService**](win32-terminalservice.md).</span></span>

<span data-ttu-id="4c457-108">В этом разделе используется синтаксис MOF-файл (MOF).</span><span class="sxs-lookup"><span data-stu-id="4c457-108">This topic uses Managed Object Format (MOF) syntax.</span></span> <span data-ttu-id="4c457-109">Дополнительные сведения об использовании этого метода см. [в разделе вызов метода](/windows/desktop/WmiSdk/calling-a-method).</span><span class="sxs-lookup"><span data-stu-id="4c457-109">For more information about using this method, see [Calling a Method](/windows/desktop/WmiSdk/calling-a-method).</span></span>

## <a name="syntax"></a><span data-ttu-id="4c457-110">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="4c457-110">Syntax</span></span>


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
  [in] string  LoadOrderGroupDependencies,
  [in] string  ServiceDependencies
);
```



## <a name="parameters"></a><span data-ttu-id="4c457-111">Параметры</span><span class="sxs-lookup"><span data-stu-id="4c457-111">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="4c457-112">*DisplayName* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="4c457-112">*DisplayName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="4c457-113">Отображаемое имя для службы.</span><span class="sxs-lookup"><span data-stu-id="4c457-113">The display name of the service.</span></span> <span data-ttu-id="4c457-114">Максимальная длина этой строки равна 256 символам.</span><span class="sxs-lookup"><span data-stu-id="4c457-114">This string has a maximum length of 256 characters.</span></span> <span data-ttu-id="4c457-115">В диспетчере управления службами имя сохраняется с учетом регистра.</span><span class="sxs-lookup"><span data-stu-id="4c457-115">The name is case-preserved in the service control manager.</span></span> <span data-ttu-id="4c457-116">В сравнениях *DisplayName* всегда учитывается регистр.</span><span class="sxs-lookup"><span data-stu-id="4c457-116">*DisplayName* comparisons are always case-insensitive.</span></span>

<span data-ttu-id="4c457-117">Ограничения: принимает то же значение, что и свойство **Name** .</span><span class="sxs-lookup"><span data-stu-id="4c457-117">Constraints: Accepts the same value as the **Name** property.</span></span>

<span data-ttu-id="4c457-118">Например, "Атдиск".</span><span class="sxs-lookup"><span data-stu-id="4c457-118">Example, "Atdisk".</span></span>

</dd> <dt>

<span data-ttu-id="4c457-119">*Путь к файлу* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="4c457-119">*PathName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="4c457-120">Полный путь к исполняемому файлу, реализующему службу, например " \\ СистемныйКорневойКаталог \\ system32 \\ Drivers \\afd.sys".</span><span class="sxs-lookup"><span data-stu-id="4c457-120">The fully qualified path to the executable file that implements the service, for example, "\\SystemRoot\\System32\\drivers\\afd.sys".</span></span>

</dd> <dt>

<span data-ttu-id="4c457-121">*ServiceType* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="4c457-121">*ServiceType* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="4c457-122">Тип служб, предоставляемых процессам, которые их вызывают.</span><span class="sxs-lookup"><span data-stu-id="4c457-122">The type of services provided to processes that call them.</span></span>

<dt>

<span data-ttu-id="4c457-123">1 (0x1)</span><span class="sxs-lookup"><span data-stu-id="4c457-123">1 (0x1)</span></span>
</dt> <dd>

<span data-ttu-id="4c457-124">Драйвер ядра</span><span class="sxs-lookup"><span data-stu-id="4c457-124">Kernel Driver</span></span>

</dd> <dt>

<span data-ttu-id="4c457-125">2 (0x2)</span><span class="sxs-lookup"><span data-stu-id="4c457-125">2 (0x2)</span></span>
</dt> <dd>

<span data-ttu-id="4c457-126">Драйвер файловой системы</span><span class="sxs-lookup"><span data-stu-id="4c457-126">File System Driver</span></span>

</dd> <dt>

<span data-ttu-id="4c457-127">4 (0x4)</span><span class="sxs-lookup"><span data-stu-id="4c457-127">4 (0x4)</span></span>
</dt> <dd>

<span data-ttu-id="4c457-128">Адаптер</span><span class="sxs-lookup"><span data-stu-id="4c457-128">Adapter</span></span>

</dd> <dt>

<span data-ttu-id="4c457-129">8 (0x8)</span><span class="sxs-lookup"><span data-stu-id="4c457-129">8 (0x8)</span></span>
</dt> <dd>

<span data-ttu-id="4c457-130">Драйвер распознавателя</span><span class="sxs-lookup"><span data-stu-id="4c457-130">Recognizer Driver</span></span>

</dd> <dt>

<span data-ttu-id="4c457-131">16 (0x10)</span><span class="sxs-lookup"><span data-stu-id="4c457-131">16 (0x10)</span></span>
</dt> <dd>

<span data-ttu-id="4c457-132">Собственный процесс</span><span class="sxs-lookup"><span data-stu-id="4c457-132">Own Process</span></span>

</dd> <dt>

<span data-ttu-id="4c457-133">32 (0x20)</span><span class="sxs-lookup"><span data-stu-id="4c457-133">32 (0x20)</span></span>
</dt> <dd>

<span data-ttu-id="4c457-134">Общий процесс</span><span class="sxs-lookup"><span data-stu-id="4c457-134">Share Process</span></span>

</dd> <dt>

<span data-ttu-id="4c457-135">256 (0x100)</span><span class="sxs-lookup"><span data-stu-id="4c457-135">256 (0x100)</span></span>
</dt> <dd>

<span data-ttu-id="4c457-136">Интерактивный процесс</span><span class="sxs-lookup"><span data-stu-id="4c457-136">Interactive Process</span></span>

</dd> </dl> </dd> <dt>

<span data-ttu-id="4c457-137">*ErrorControl* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="4c457-137">*ErrorControl* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="4c457-138">Серьезность ошибки, если не удается запустить службу во время запуска.</span><span class="sxs-lookup"><span data-stu-id="4c457-138">Severity of the error if this service fails to start during startup.</span></span> <span data-ttu-id="4c457-139">Значение указывает действие, предпринимаемое программой запуска, если происходит сбой.</span><span class="sxs-lookup"><span data-stu-id="4c457-139">The value indicates the action taken by the startup program if failure occurs.</span></span> <span data-ttu-id="4c457-140">Все ошибки регистрируются системой.</span><span class="sxs-lookup"><span data-stu-id="4c457-140">All errors are logged by the system.</span></span>

<dt>

<span data-ttu-id="4c457-141">0</span><span class="sxs-lookup"><span data-stu-id="4c457-141">0</span></span>
</dt> <dd>

<span data-ttu-id="4c457-142">**Пропуск**.</span><span class="sxs-lookup"><span data-stu-id="4c457-142">**Ignore**.</span></span> <span data-ttu-id="4c457-143">Запуск продолжится.</span><span class="sxs-lookup"><span data-stu-id="4c457-143">Startup continues.</span></span> <span data-ttu-id="4c457-144">Пользователю не удалось получить уведомление о сбое службы.</span><span class="sxs-lookup"><span data-stu-id="4c457-144">No notification is given to the user that the service failed.</span></span>

</dd> <dt>

<span data-ttu-id="4c457-145">1</span><span class="sxs-lookup"><span data-stu-id="4c457-145">1</span></span>
</dt> <dd>

<span data-ttu-id="4c457-146">**Обычно.**</span><span class="sxs-lookup"><span data-stu-id="4c457-146">**Normal.**</span></span> <span data-ttu-id="4c457-147">Запуск продолжится.</span><span class="sxs-lookup"><span data-stu-id="4c457-147">Startup continues.</span></span> <span data-ttu-id="4c457-148">Перед входом пользователя в систему пользователь получает уведомление "не удалось выполнить по крайней мере одну службу или устройство во время запуска".</span><span class="sxs-lookup"><span data-stu-id="4c457-148">Before the user logs on, the user receives the notification, "At least one service or device failed during startup."</span></span>

</dd> <dt>

<span data-ttu-id="4c457-149">2</span><span class="sxs-lookup"><span data-stu-id="4c457-149">2</span></span>
</dt> <dd>

<span data-ttu-id="4c457-150">**Серьезные.**</span><span class="sxs-lookup"><span data-stu-id="4c457-150">**Severe.**</span></span> <span data-ttu-id="4c457-151">Компьютер пытается перезапуститься с последней удачной конфигурацией.</span><span class="sxs-lookup"><span data-stu-id="4c457-151">Computer attempts to restart with last-known good configuration.</span></span> <span data-ttu-id="4c457-152">Если служба снова завершается со сбоем, запуск продолжится и пользователю будет предоставлено уведомление.</span><span class="sxs-lookup"><span data-stu-id="4c457-152">If the service fails again, startup continues and notification is given to the user.</span></span>

</dd> <dt>

<span data-ttu-id="4c457-153">3</span><span class="sxs-lookup"><span data-stu-id="4c457-153">3</span></span>
</dt> <dd>

<span data-ttu-id="4c457-154">**Критическое.**</span><span class="sxs-lookup"><span data-stu-id="4c457-154">**Critical.**</span></span> <span data-ttu-id="4c457-155">Компьютер пытается перезапуститься с последней удачной конфигурацией.</span><span class="sxs-lookup"><span data-stu-id="4c457-155">Computer attempts to restart with last-known good configuration.</span></span> <span data-ttu-id="4c457-156">Если служба снова завершается со сбоем, запуск останавливается.</span><span class="sxs-lookup"><span data-stu-id="4c457-156">If the service fails again, startup stops.</span></span>

</dd> </dl> </dd> <dt>

<span data-ttu-id="4c457-157">*StartMode* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="4c457-157">*StartMode* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="4c457-158">Режим запуска базовой службы Windows.</span><span class="sxs-lookup"><span data-stu-id="4c457-158">Start mode of the Windows base service.</span></span> <span data-ttu-id="4c457-159">Дополнительные сведения см. в разделе "Замечания".</span><span class="sxs-lookup"><span data-stu-id="4c457-159">For more information, see the Remarks section.</span></span>

<dt>

<span id="Boot"></span><span id="boot"></span><span id="BOOT"></span>

<span data-ttu-id="4c457-160"><span id="Boot"></span><span id="boot"></span><span id="BOOT"></span>**Файле**</span><span class="sxs-lookup"><span data-stu-id="4c457-160"><span id="Boot"></span><span id="boot"></span><span id="BOOT"></span>**Boot**</span></span>


</dt> <dd>

<span data-ttu-id="4c457-161">Драйвер устройства запущен загрузчиком операционной системы.</span><span class="sxs-lookup"><span data-stu-id="4c457-161">Device driver started by the operating system loader.</span></span>

</dd> <dt>

<span id="System"></span><span id="system"></span><span id="SYSTEM"></span>

<span data-ttu-id="4c457-162"><span id="System"></span><span id="system"></span><span id="SYSTEM"></span>**Системой**</span><span class="sxs-lookup"><span data-stu-id="4c457-162"><span id="System"></span><span id="system"></span><span id="SYSTEM"></span>**System**</span></span>


</dt> <dd>

<span data-ttu-id="4c457-163">Драйвер устройства запущен процессом инициализации операционной системы.</span><span class="sxs-lookup"><span data-stu-id="4c457-163">Device driver started by the operating system initialization process.</span></span> <span data-ttu-id="4c457-164">Это значение допустимо только для служб драйверов.</span><span class="sxs-lookup"><span data-stu-id="4c457-164">This value is valid only for driver services.</span></span>

</dd> <dt>

<span id="Automatic"></span><span id="automatic"></span><span id="AUTOMATIC"></span>

<span data-ttu-id="4c457-165"><span id="Automatic"></span><span id="automatic"></span><span id="AUTOMATIC"></span>**Автоматически**</span><span class="sxs-lookup"><span data-stu-id="4c457-165"><span id="Automatic"></span><span id="automatic"></span><span id="AUTOMATIC"></span>**Automatic**</span></span>


</dt> <dd>

<span data-ttu-id="4c457-166">Служба запускается автоматически диспетчером управления службами во время запуска системы.</span><span class="sxs-lookup"><span data-stu-id="4c457-166">Service is started automatically by the service control manager during system startup.</span></span> <span data-ttu-id="4c457-167">Службы автозапуска запускаются до входа пользователя в систему и запуска, даже если пользователь не входит в систему.</span><span class="sxs-lookup"><span data-stu-id="4c457-167">Autostart services start before a user logs on to the computer and run even if no user logs on to the computer.</span></span>

</dd> <dt>

<span id="Manual"></span><span id="manual"></span><span id="MANUAL"></span>

<span data-ttu-id="4c457-168"><span id="Manual"></span><span id="manual"></span><span id="MANUAL"></span>**Вручную**</span><span class="sxs-lookup"><span data-stu-id="4c457-168"><span id="Manual"></span><span id="manual"></span><span id="MANUAL"></span>**Manual**</span></span>


</dt> <dd>

<span data-ttu-id="4c457-169">Служба, запускаемая диспетчером управления службами, когда процесс вызывает метод [**StartService**](win32-terminalservice-startservice.md) .</span><span class="sxs-lookup"><span data-stu-id="4c457-169">Service to be started by the service control manager when a process calls the [**StartService**](win32-terminalservice-startservice.md) method.</span></span> <span data-ttu-id="4c457-170">Хотя ручные службы должны быть специально запущены пользователем (или сценарием), они продолжают работать, даже если пользователь выходит из системы.</span><span class="sxs-lookup"><span data-stu-id="4c457-170">Although manual services must be specifically started by a user (or by a script), they continue to run even if the user logs off.</span></span> <span data-ttu-id="4c457-171">Ручные службы часто называются службами по требованию.</span><span class="sxs-lookup"><span data-stu-id="4c457-171">Manual services are often referred to as on-demand services.</span></span>

</dd> <dt>

<span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>

<span data-ttu-id="4c457-172"><span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>**Доступ**</span><span class="sxs-lookup"><span data-stu-id="4c457-172"><span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>**Disabled**</span></span>


</dt> <dd>

<span data-ttu-id="4c457-173">Служба, которая больше не может быть запущена.</span><span class="sxs-lookup"><span data-stu-id="4c457-173">Service that can no longer be started.</span></span> <span data-ttu-id="4c457-174">Чтобы запустить отключенную службу, необходимо сначала изменить параметр запуска на Auto или Manual.</span><span class="sxs-lookup"><span data-stu-id="4c457-174">To start a disabled service, you must first change the startup option to either Auto or Manual.</span></span>

</dd> </dl> </dd> <dt>

<span data-ttu-id="4c457-175">*Десктопинтеракт* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="4c457-175">*DesktopInteract* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="4c457-176">Если **значение — true**, служба может создавать окно на рабочем столе или взаимодействовать с ним.</span><span class="sxs-lookup"><span data-stu-id="4c457-176">If **True**, the service can create or communicate with a window on the desktop.</span></span>

</dd> <dt>

<span data-ttu-id="4c457-177">*StartName* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="4c457-177">*StartName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="4c457-178">Имя учетной записи, в которой выполняется служба.</span><span class="sxs-lookup"><span data-stu-id="4c457-178">Account name the service runs under.</span></span> <span data-ttu-id="4c457-179">В зависимости от типа службы имя учетной записи может быть в формате имя_домена \\ имя пользователя или. \\ Имен.</span><span class="sxs-lookup"><span data-stu-id="4c457-179">Depending on the service type, the account name may be in the form of DomainName\\Username or .\\Username.</span></span> <span data-ttu-id="4c457-180">Процесс службы будет заноситься в журнал с использованием одной из этих двух форм при запуске.</span><span class="sxs-lookup"><span data-stu-id="4c457-180">The service process will be logged using one of these two forms when it runs.</span></span> <span data-ttu-id="4c457-181">Если учетная запись принадлежит к встроенному домену,. \\ Можно указать имя пользователя.</span><span class="sxs-lookup"><span data-stu-id="4c457-181">If the account belongs to the built-in domain, .\\Username can be specified.</span></span> <span data-ttu-id="4c457-182">Если указано **значение NULL** , служба будет входить в систему как учетная запись LocalSystem.</span><span class="sxs-lookup"><span data-stu-id="4c457-182">If **NULL** is specified, the service will be logged on as the LocalSystem account.</span></span> <span data-ttu-id="4c457-183">Для драйверов ядра или системного уровня *StartName* содержит имя объекта драйвера (то есть \\ FileSystem \\ RDR или \\ Driver \\ КСНС), которое используется системой ввода и вывода для загрузки драйвера устройства.</span><span class="sxs-lookup"><span data-stu-id="4c457-183">For kernel or system-level drivers, *StartName* contains the driver object name (that is, \\FileSystem\\Rdr or \\Driver\\Xns) that the input and output (I/O) system uses to load the device driver.</span></span> <span data-ttu-id="4c457-184">Если указано **значение NULL** , драйвер запускается с именем объекта по умолчанию, созданным системой ввода-вывода на основе имени службы, например "двдом \\ Admin".</span><span class="sxs-lookup"><span data-stu-id="4c457-184">If **NULL** is specified, the driver runs with a default object name created by the I/O system based on the service name, for example, "DWDOM\\Admin".</span></span>

<span data-ttu-id="4c457-185">Можно также использовать формат имени участника-пользователя (UPN) для указания **StartName**, например *Username@DomainName* .</span><span class="sxs-lookup"><span data-stu-id="4c457-185">You also can use the User Principal Name (UPN) format to specify the **StartName**, for example, *Username@DomainName*.</span></span>

</dd> <dt>

<span data-ttu-id="4c457-186">*Стартпассворд* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="4c457-186">*StartPassword* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="4c457-187">Пароль к имени учетной записи, заданному параметром *StartName* .</span><span class="sxs-lookup"><span data-stu-id="4c457-187">Password to the account name specified by the *StartName* parameter.</span></span> <span data-ttu-id="4c457-188">Если пароль не изменяется, укажите **значение NULL** .</span><span class="sxs-lookup"><span data-stu-id="4c457-188">Specify **NULL** if you are not changing the password.</span></span> <span data-ttu-id="4c457-189">Если служба не имеет пароля, указывается пустая строка.</span><span class="sxs-lookup"><span data-stu-id="4c457-189">Specify an empty string if the service has no password.</span></span>

> [!Note]  
> <span data-ttu-id="4c457-190">При изменении службы с локальной системы на сеть или из сети в локальную систему *стартпассворд* должен быть пустой строкой (""), а не **null**.</span><span class="sxs-lookup"><span data-stu-id="4c457-190">When changing a service from a local system to a network, or from a network to a local system, *StartPassword* must be an empty string ("") and not **NULL**.</span></span>

 

</dd> <dt>

<span data-ttu-id="4c457-191">*Лоадордерграуп* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="4c457-191">*LoadOrderGroup* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="4c457-192">Имя группы, с которой она связана.</span><span class="sxs-lookup"><span data-stu-id="4c457-192">Group name that it is associated with.</span></span> <span data-ttu-id="4c457-193">Группы порядка загрузки содержатся в системном реестре и определяют последовательность, в которой службы загружаются в операционную систему.</span><span class="sxs-lookup"><span data-stu-id="4c457-193">Load order groups are contained in the system registry, and determine the sequence in which services are loaded into the operating system.</span></span> <span data-ttu-id="4c457-194">Если указатель равен **null** или указывает на пустую строку, служба не принадлежит группе.</span><span class="sxs-lookup"><span data-stu-id="4c457-194">If the pointer is **NULL**, or if it points to an empty string, the service does not belong to a group.</span></span> <span data-ttu-id="4c457-195">Дополнительные сведения см. в разделе "Замечания".</span><span class="sxs-lookup"><span data-stu-id="4c457-195">For more information, see the Remarks section.</span></span>

<span data-ttu-id="4c457-196">Зависимости между группами должны быть перечислены в параметре *лоадордерграупдепенденЦиес* .</span><span class="sxs-lookup"><span data-stu-id="4c457-196">Dependencies between groups should be listed in the *LoadOrderGroupDependencies* parameter.</span></span> <span data-ttu-id="4c457-197">Сначала запускаются службы в списке группы упорядочения нагрузки, а затем — службы в группах, которые не входят в список групп порядка загрузки, за которыми следуют службы, не входящие в группу.</span><span class="sxs-lookup"><span data-stu-id="4c457-197">Services in the load-ordering group list are started first, followed by services in groups not in the load-ordering group list, followed by services that do not belong to a group.</span></span> <span data-ttu-id="4c457-198">Системный реестр содержит список групп упорядочения нагрузки, расположенных по адресу:</span><span class="sxs-lookup"><span data-stu-id="4c457-198">The system registry has a list of load ordering groups located at:</span></span>

<span data-ttu-id="4c457-199">**HKey \_ \_** \\  \\  \\  \\ **ServiceGroupOrder** управления CurrentControlSet системы локального компьютера</span><span class="sxs-lookup"><span data-stu-id="4c457-199">**HKEY\_LOCAL\_MACHINE**\\**System**\\**CurrentControlSet**\\**Control**\\**ServiceGroupOrder**</span></span>

</dd> <dt>

<span data-ttu-id="4c457-200">*ЛоадордерграупдепенденЦиес* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="4c457-200">*LoadOrderGroupDependencies* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="4c457-201">Список групп упорядочивания нагрузки, которые должны быть запущены перед запуском этой службы.</span><span class="sxs-lookup"><span data-stu-id="4c457-201">List of load-ordering groups that must start before this service starts.</span></span> <span data-ttu-id="4c457-202">Массив завершается двойным **нулем.**</span><span class="sxs-lookup"><span data-stu-id="4c457-202">The array is doubly **null**-terminated.</span></span> <span data-ttu-id="4c457-203">Если указатель имеет **значение NULL** или указывает на пустую строку, служба не имеет зависимостей.</span><span class="sxs-lookup"><span data-stu-id="4c457-203">If the pointer is **NULL**, or if it points to an empty string, the service has no dependencies.</span></span> <span data-ttu-id="4c457-204">Имена групп должны быть префиксом **\_ \_ идентификатора группы SC** (определенного в файле винсвк. h), чтобы отличать их от имен служб, так как службы и группы служб используют одно и то же пространство имен.</span><span class="sxs-lookup"><span data-stu-id="4c457-204">Group names must be prefixed by the **SC\_GROUP\_IDENTIFIER** (defined in the Winsvc.h file) character to differentiate them from service names because services and service groups share the same namespace.</span></span> <span data-ttu-id="4c457-205">Зависимость от группы означает, что эту службу можно запустить, если хотя бы один член группы запущен после попытки запуска всех членов группы.</span><span class="sxs-lookup"><span data-stu-id="4c457-205">Dependency on a group means that this service can run if at least one member of the group is running after an attempt to start all of the members of the group.</span></span>

</dd> <dt>

<span data-ttu-id="4c457-206">*СервицедепенденЦиес* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="4c457-206">*ServiceDependencies* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="4c457-207">Список, содержащий имена служб, которые должны быть запущены перед запуском этой службы.</span><span class="sxs-lookup"><span data-stu-id="4c457-207">List that contains the names of services that must start before this service starts.</span></span> <span data-ttu-id="4c457-208">Массив завершается двойным **нулем.**</span><span class="sxs-lookup"><span data-stu-id="4c457-208">The array is doubly **NULL**-terminated.</span></span> <span data-ttu-id="4c457-209">Если указатель имеет **значение NULL** или указывает на пустую строку, служба не имеет зависимостей.</span><span class="sxs-lookup"><span data-stu-id="4c457-209">If the pointer is **NULL**, or if it points to an empty string, the service has no dependencies.</span></span> <span data-ttu-id="4c457-210">Зависимость от службы указывает, что эта служба может выполняться, только если запущена служба, от которой она зависит.</span><span class="sxs-lookup"><span data-stu-id="4c457-210">Dependency on a service indicates that this service can run only if the service it depends on is running.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="4c457-211">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="4c457-211">Return value</span></span>

<span data-ttu-id="4c457-212">Возвращает одно из значений, перечисленных в следующем списке, или любое другое значение, указывающее на ошибку.</span><span class="sxs-lookup"><span data-stu-id="4c457-212">Returns one of the values listed in the following list, or any other value to indicate an error.</span></span> <span data-ttu-id="4c457-213">Дополнительные коды ошибок см. в разделе [**константы WMI Error**](/windows/desktop/WmiSdk/wmi-error-constants) или [**вбемерроренум**](/windows/desktop/api/wbemdisp/ne-wbemdisp-wbemerrorenum).</span><span class="sxs-lookup"><span data-stu-id="4c457-213">For additional error codes, see [**WMI Error Constants**](/windows/desktop/WmiSdk/wmi-error-constants) or [**WbemErrorEnum**](/windows/desktop/api/wbemdisp/ne-wbemdisp-wbemerrorenum).</span></span> <span data-ttu-id="4c457-214">Общие значения **HRESULT** см. в разделе [коды системных ошибок](/windows/desktop/Debug/system-error-codes).</span><span class="sxs-lookup"><span data-stu-id="4c457-214">For general **HRESULT** values, see [System Error Codes](/windows/desktop/Debug/system-error-codes).</span></span>

<dl> <dt>

<span data-ttu-id="4c457-215">**0**</span><span class="sxs-lookup"><span data-stu-id="4c457-215">**0**</span></span>
</dt> <dd>

<span data-ttu-id="4c457-216">Запрос принят.</span><span class="sxs-lookup"><span data-stu-id="4c457-216">The request was accepted.</span></span>

</dd> <dt>

<span data-ttu-id="4c457-217">**1**</span><span class="sxs-lookup"><span data-stu-id="4c457-217">**1**</span></span>
</dt> <dd>

<span data-ttu-id="4c457-218">Запрос не поддерживается.</span><span class="sxs-lookup"><span data-stu-id="4c457-218">The request is not supported.</span></span>

</dd> <dt>

<span data-ttu-id="4c457-219">**2**</span><span class="sxs-lookup"><span data-stu-id="4c457-219">**2**</span></span>
</dt> <dd>

<span data-ttu-id="4c457-220">У пользователя нет необходимых прав доступа.</span><span class="sxs-lookup"><span data-stu-id="4c457-220">The user did not have the necessary access.</span></span>

</dd> <dt>

<span data-ttu-id="4c457-221">**3**</span><span class="sxs-lookup"><span data-stu-id="4c457-221">**3**</span></span>
</dt> <dd>

<span data-ttu-id="4c457-222">Службу нельзя остановить, так как от нее зависят другие работающие службы.</span><span class="sxs-lookup"><span data-stu-id="4c457-222">The service cannot be stopped because other services that are running are dependent on it.</span></span>

</dd> <dt>

<span data-ttu-id="4c457-223">**4**</span><span class="sxs-lookup"><span data-stu-id="4c457-223">**4**</span></span>
</dt> <dd>

<span data-ttu-id="4c457-224">Запрошенный управляющий код недопустим или неприемлем для данной службы.</span><span class="sxs-lookup"><span data-stu-id="4c457-224">The requested control code is not valid, or it is unacceptable to the service.</span></span>

</dd> <dt>

<span data-ttu-id="4c457-225">**5**</span><span class="sxs-lookup"><span data-stu-id="4c457-225">**5**</span></span>
</dt> <dd>

<span data-ttu-id="4c457-226">Запрошенный управляющий код не может быть отправлен в службу, так как это состояние службы ([**Win32 \_ басесервице**](/windows/desktop/CIMWin32Prov/win32-baseservice).**Свойство State** ) равно 0, 1 или 2.</span><span class="sxs-lookup"><span data-stu-id="4c457-226">The requested control code cannot be sent to the service because the state of the service ([**Win32\_BaseService**](/windows/desktop/CIMWin32Prov/win32-baseservice).**State** property) is equal to 0, 1, or 2.</span></span>

</dd> <dt>

<span data-ttu-id="4c457-227">**6**</span><span class="sxs-lookup"><span data-stu-id="4c457-227">**6**</span></span>
</dt> <dd>

<span data-ttu-id="4c457-228">Служба не запущена.</span><span class="sxs-lookup"><span data-stu-id="4c457-228">The service has not been started.</span></span>

</dd> <dt>

<span data-ttu-id="4c457-229">**7**</span><span class="sxs-lookup"><span data-stu-id="4c457-229">**7**</span></span>
</dt> <dd>

<span data-ttu-id="4c457-230">Служба не ответила на запрос запуска за отведенное время.</span><span class="sxs-lookup"><span data-stu-id="4c457-230">The service did not respond to the start request in a timely fashion.</span></span>

</dd> <dt>

<span data-ttu-id="4c457-231">**8**</span><span class="sxs-lookup"><span data-stu-id="4c457-231">**8**</span></span>
</dt> <dd>

<span data-ttu-id="4c457-232">Неизвестный сбой при запуске службы.</span><span class="sxs-lookup"><span data-stu-id="4c457-232">Unknown failure when starting the service.</span></span>

</dd> <dt>

<span data-ttu-id="4c457-233">**9**</span><span class="sxs-lookup"><span data-stu-id="4c457-233">**9**</span></span>
</dt> <dd>

<span data-ttu-id="4c457-234">Не найден путь к каталогу исполняемого файла службы.</span><span class="sxs-lookup"><span data-stu-id="4c457-234">The directory path to the service executable file was not found.</span></span>

</dd> <dt>

<span data-ttu-id="4c457-235">**10**</span><span class="sxs-lookup"><span data-stu-id="4c457-235">**10**</span></span>
</dt> <dd>

<span data-ttu-id="4c457-236">Служба уже запущена.</span><span class="sxs-lookup"><span data-stu-id="4c457-236">The service is already running.</span></span>

</dd> <dt>

<span data-ttu-id="4c457-237">**11**</span><span class="sxs-lookup"><span data-stu-id="4c457-237">**11**</span></span>
</dt> <dd>

<span data-ttu-id="4c457-238">База данных для добавления новой службы заблокирована.</span><span class="sxs-lookup"><span data-stu-id="4c457-238">The database to add a new service is locked.</span></span>

</dd> <dt>

<span data-ttu-id="4c457-239">**12**</span><span class="sxs-lookup"><span data-stu-id="4c457-239">**12**</span></span>
</dt> <dd>

<span data-ttu-id="4c457-240">Зависимость, от которой зависит эта служба, удалена из системы.</span><span class="sxs-lookup"><span data-stu-id="4c457-240">A dependency this service relies on has been removed from the system.</span></span>

</dd> <dt>

<span data-ttu-id="4c457-241">**13**</span><span class="sxs-lookup"><span data-stu-id="4c457-241">**13**</span></span>
</dt> <dd>

<span data-ttu-id="4c457-242">Этой службе не удалось найти службу, которая необходима зависимой службе.</span><span class="sxs-lookup"><span data-stu-id="4c457-242">The service failed to find the service needed from a dependent service.</span></span>

</dd> <dt>

<span data-ttu-id="4c457-243">**14**</span><span class="sxs-lookup"><span data-stu-id="4c457-243">**14**</span></span>
</dt> <dd>

<span data-ttu-id="4c457-244">Эта служба была отключена в системе.</span><span class="sxs-lookup"><span data-stu-id="4c457-244">The service has been disabled from the system.</span></span>

</dd> <dt>

<span data-ttu-id="4c457-245">**15**</span><span class="sxs-lookup"><span data-stu-id="4c457-245">**15**</span></span>
</dt> <dd>

<span data-ttu-id="4c457-246">Эта служба не поддерживает проверку подлинности, необходимую для работы в системе.</span><span class="sxs-lookup"><span data-stu-id="4c457-246">The service does not have the correct authentication to run on the system.</span></span>

</dd> <dt>

<span data-ttu-id="4c457-247">**16**</span><span class="sxs-lookup"><span data-stu-id="4c457-247">**16**</span></span>
</dt> <dd>

<span data-ttu-id="4c457-248">Эта служба удаляется из системы.</span><span class="sxs-lookup"><span data-stu-id="4c457-248">This service is being removed from the system.</span></span>

</dd> <dt>

<span data-ttu-id="4c457-249">**17**</span><span class="sxs-lookup"><span data-stu-id="4c457-249">**17**</span></span>
</dt> <dd>

<span data-ttu-id="4c457-250">Служба не имеет потока выполнения.</span><span class="sxs-lookup"><span data-stu-id="4c457-250">The service has no execution thread.</span></span>

</dd> <dt>

<span data-ttu-id="4c457-251">**стр**</span><span class="sxs-lookup"><span data-stu-id="4c457-251">**18**</span></span>
</dt> <dd>

<span data-ttu-id="4c457-252">Служба имеет циклические зависимости при запуске.</span><span class="sxs-lookup"><span data-stu-id="4c457-252">The service has circular dependencies when it starts.</span></span>

</dd> <dt>

<span data-ttu-id="4c457-253">**стр**</span><span class="sxs-lookup"><span data-stu-id="4c457-253">**19**</span></span>
</dt> <dd>

<span data-ttu-id="4c457-254">Служба выполняется с тем же именем.</span><span class="sxs-lookup"><span data-stu-id="4c457-254">A service is running under the same name.</span></span>

</dd> <dt>

<span data-ttu-id="4c457-255">**20**</span><span class="sxs-lookup"><span data-stu-id="4c457-255">**20**</span></span>
</dt> <dd>

<span data-ttu-id="4c457-256">Имя службы содержит недопустимые символы.</span><span class="sxs-lookup"><span data-stu-id="4c457-256">The service name has invalid characters.</span></span>

</dd> <dt>

<span data-ttu-id="4c457-257">**открыт**</span><span class="sxs-lookup"><span data-stu-id="4c457-257">**21**</span></span>
</dt> <dd>

<span data-ttu-id="4c457-258">Службе переданы недопустимые параметры.</span><span class="sxs-lookup"><span data-stu-id="4c457-258">Invalid parameters have been passed to the service.</span></span>

</dd> <dt>

<span data-ttu-id="4c457-259">**22**</span><span class="sxs-lookup"><span data-stu-id="4c457-259">**22**</span></span>
</dt> <dd>

<span data-ttu-id="4c457-260">Учетная запись, под которой работает эта служба, либо недопустима, либо не имеет разрешений на запуск службы.</span><span class="sxs-lookup"><span data-stu-id="4c457-260">The account under which this service runs is either invalid or lacks the permissions to run the service.</span></span>

</dd> <dt>

<span data-ttu-id="4c457-261">**23**</span><span class="sxs-lookup"><span data-stu-id="4c457-261">**23**</span></span>
</dt> <dd>

<span data-ttu-id="4c457-262">Служба существует в базе данных доступных в системе служб.</span><span class="sxs-lookup"><span data-stu-id="4c457-262">The service exists in the database of services available from the system.</span></span>

</dd> <dt>

<span data-ttu-id="4c457-263">**24**</span><span class="sxs-lookup"><span data-stu-id="4c457-263">**24**</span></span>
</dt> <dd>

<span data-ttu-id="4c457-264">Служба в данный момент приостановлена в системе.</span><span class="sxs-lookup"><span data-stu-id="4c457-264">The service is currently paused in the system.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="4c457-265">Комментарии</span><span class="sxs-lookup"><span data-stu-id="4c457-265">Remarks</span></span>

<span data-ttu-id="4c457-266">При запуске компьютера также запускаются все службы автозапуска.</span><span class="sxs-lookup"><span data-stu-id="4c457-266">When a computer starts, all the autostart services also start.</span></span> <span data-ttu-id="4c457-267">Иногда одна из этих служб может не запускаться вместе с компьютером.</span><span class="sxs-lookup"><span data-stu-id="4c457-267">On occasion, one of these services might fail to start along with the computer.</span></span> <span data-ttu-id="4c457-268">При сбое службы во время запуска системы компьютер принимает действия в соответствии со значением управляющего кода ошибки службы.</span><span class="sxs-lookup"><span data-stu-id="4c457-268">When a service fails during system startup, the computer takes action based on the value of the service error control code.</span></span>

<span data-ttu-id="4c457-269">Большинство служб устанавливаются с помощью обычного управляющего кода ошибок.</span><span class="sxs-lookup"><span data-stu-id="4c457-269">most services are installed using the Normal error control code.</span></span> <span data-ttu-id="4c457-270">Некоторые исключения, которые устанавливаются с помощью команды игнорировать код ошибки, включают:</span><span class="sxs-lookup"><span data-stu-id="4c457-270">A few of the exceptions, which are installed using the Ignore error code, include:</span></span>

-   <span data-ttu-id="4c457-271">Служба репликации файлов</span><span class="sxs-lookup"><span data-stu-id="4c457-271">File Replication Service</span></span>
-   <span data-ttu-id="4c457-272">Смарт-карта</span><span class="sxs-lookup"><span data-stu-id="4c457-272">Smart Card</span></span>
-   <span data-ttu-id="4c457-273">Вторичный вход в систему</span><span class="sxs-lookup"><span data-stu-id="4c457-273">Secondary Logon</span></span>
-   <span data-ttu-id="4c457-274">WMI</span><span class="sxs-lookup"><span data-stu-id="4c457-274">WMI</span></span>

<span data-ttu-id="4c457-275">Для служб, установленных с помощью команды игнорировать код ошибки, пользователю не выдается уведомление о том, что служба завершилась ошибкой.</span><span class="sxs-lookup"><span data-stu-id="4c457-275">For the services installed using the Ignore error code, no notification is given to the user that the service has failed.</span></span> <span data-ttu-id="4c457-276">Если вы предпочитаете на экране уведомление о том, что не удалось запустить службу, можно использовать инструментарий WMI для изменения управляющего кода ошибки.</span><span class="sxs-lookup"><span data-stu-id="4c457-276">If you prefer on-screen notification that a service could not start, you can use WMI to change the error control code.</span></span> <span data-ttu-id="4c457-277">Коды управления ошибками применяются только к загрузке компьютера; управляющие коды ошибок не используются, если вы останавливаете и попытаетесь перезапустить службу после запуска компьютера.</span><span class="sxs-lookup"><span data-stu-id="4c457-277">Error control codes apply only to computer startup; error control codes are not used if you stop and then attempt to restart a service after the computer is running.</span></span>

<span data-ttu-id="4c457-278">Иногда может потребоваться изменить учетную запись, под которой работает данная служба.</span><span class="sxs-lookup"><span data-stu-id="4c457-278">On occasion, you might need to change the account under which a given service runs.</span></span> <span data-ttu-id="4c457-279">Например, служба может запускаться под административной учетной записью.</span><span class="sxs-lookup"><span data-stu-id="4c457-279">For example, you might run a service under an administrative account.</span></span> <span data-ttu-id="4c457-280">Поскольку это может привести к уязвимости системы безопасности, можно переключить службу на учетную запись с меньшим числом привилегий.</span><span class="sxs-lookup"><span data-stu-id="4c457-280">Because this can create a security vulnerability, you might switch the service to an account with fewer privileges.</span></span> <span data-ttu-id="4c457-281">Кроме того, могут быть запущены службы с учетной записью, которая будет удалена, или необходимо убедиться, что на всех серверах некоторые службы выполняются под определенными учетными записями.</span><span class="sxs-lookup"><span data-stu-id="4c457-281">Alternatively, you might have services running under an account that is about to be deleted, or you might want to ensure that, on all your servers, certain services run under certain accounts.</span></span> <span data-ttu-id="4c457-282">Можно использовать метод **Change** класса [**Win32 \_ терминалсервице**](win32-terminalservice.md) , чтобы настроить службы для работы с указанной учетной записью пользователя.</span><span class="sxs-lookup"><span data-stu-id="4c457-282">You can use the **Change** method of the [**Win32\_TerminalService**](win32-terminalservice.md) class to configure services to run under a specified user account.</span></span> <span data-ttu-id="4c457-283">При выборе учетной записи учитывайте следующее.</span><span class="sxs-lookup"><span data-stu-id="4c457-283">When selecting an account, keep in mind the following:</span></span>

-   <span data-ttu-id="4c457-284">Учетная запись, используемая в качестве учетной записи службы, должна иметь право на вход в качестве службы.</span><span class="sxs-lookup"><span data-stu-id="4c457-284">The account being used as a service account must have the right to log on as a service.</span></span> <span data-ttu-id="4c457-285">Это право можно предоставить с помощью групповая политика.</span><span class="sxs-lookup"><span data-stu-id="4c457-285">This right can be granted by using Group Policy.</span></span>
-   <span data-ttu-id="4c457-286">Учетная запись, используемая как учетная запись службы, не должна быть членом локальной группы администраторов, домена или администратора предприятия.</span><span class="sxs-lookup"><span data-stu-id="4c457-286">The account being used as a service account should not be a member of a local, domain, or enterprise Administrators group.</span></span>
-   <span data-ttu-id="4c457-287">Каждый экземпляр службы должен работать под уникальной учетной записью пользователя.</span><span class="sxs-lookup"><span data-stu-id="4c457-287">Each instance of a service should run under a unique user account.</span></span> <span data-ttu-id="4c457-288">Это обеспечивает дополнительную безопасность и включает аудит отдельных экземпляров службы.</span><span class="sxs-lookup"><span data-stu-id="4c457-288">This provides additional security, and enables the auditing of individual service instances.</span></span>
-   <span data-ttu-id="4c457-289">Если служба является интерактивной, она должна работать под учетной записью LocalSystem.</span><span class="sxs-lookup"><span data-stu-id="4c457-289">If the service is interactive, then the service must run under the LocalSystem account.</span></span>

    <span data-ttu-id="4c457-290">LocalSystem является обязательным, так как только одна Windows-станция (WinSta0) может быть видимой и интерактивной в каждый момент времени.</span><span class="sxs-lookup"><span data-stu-id="4c457-290">LocalSystem is required because only one window station (WinSta0) can be visible and interactive at a time.</span></span> <span data-ttu-id="4c457-291">Если служба выполняется под учетной записью, отличной от LocalSystem, она выполняется в окне Service-0x03e7 $ \\ Default Windows Station, которое является невидимым окном.</span><span class="sxs-lookup"><span data-stu-id="4c457-291">If a service runs under an account other than LocalSystem, it runs in the Service-0x03e7$\\Default window station, which is an invisible window.</span></span> <span data-ttu-id="4c457-292">Службы, работающие на этой экранной станции, не могут принимать входные данные и отображать выходные данные.</span><span class="sxs-lookup"><span data-stu-id="4c457-292">Services running in this window station cannot receive input or display output.</span></span>

<span data-ttu-id="4c457-293">При назначении учетной записи службе SCM требует для этой учетной записи правильный пароль, прежде чем приступать к назначению.</span><span class="sxs-lookup"><span data-stu-id="4c457-293">When you assign an account to a service, the SCM requires the correct password for that account before it makes the assignment.</span></span> <span data-ttu-id="4c457-294">При указании неверного пароля SCM отклоняет учетную запись.</span><span class="sxs-lookup"><span data-stu-id="4c457-294">If you supply an incorrect password, the SCM rejects the account.</span></span> <span data-ttu-id="4c457-295">Если вы настраиваете учетную запись службы с помощью учетной записи LocalSystem, LocalService или NetworkService, вам не нужно указывать пароль учетной записи, так как у этих учетных записей нет паролей.</span><span class="sxs-lookup"><span data-stu-id="4c457-295">If you configure a service account using the LocalSystem, LocalService, or NetworkService account, you do not need to supply an account password because these accounts do not have passwords.</span></span>

<span data-ttu-id="4c457-296">SCM хранит пароль учетной записи в базе данных служб.</span><span class="sxs-lookup"><span data-stu-id="4c457-296">The SCM stores the account password in the services database.</span></span> <span data-ttu-id="4c457-297">Однако после назначения пароля SCM не гарантирует, что пароль, хранящийся в базе данных служб, и пароль, назначенный учетной записи пользователя в Active Directory, будут по-прежнему совпадать.</span><span class="sxs-lookup"><span data-stu-id="4c457-297">After the password is assigned, however, the SCM does not ensure that the password stored in the services database and the password assigned to the user account in Active Directory continue to match.</span></span> <span data-ttu-id="4c457-298">Следовательно, может произойти ситуация, подобная следующей:</span><span class="sxs-lookup"><span data-stu-id="4c457-298">Consequently, a situation similar to the following could occur:</span></span>

-   <span data-ttu-id="4c457-299">. Служба настраивается для запуска от имени определенной учетной записи пользователя.</span><span class="sxs-lookup"><span data-stu-id="4c457-299">.You configure a service to run under a particular user account.</span></span>
-   <span data-ttu-id="4c457-300">Служба запускается под этой учетной записью с использованием пароля текущей учетной записи.</span><span class="sxs-lookup"><span data-stu-id="4c457-300">The service starts up under that account by using the current account password.</span></span>
-   <span data-ttu-id="4c457-301">Вы изменяете пароль для учетной записи пользователя.</span><span class="sxs-lookup"><span data-stu-id="4c457-301">You change the password for the user account.</span></span>
-   <span data-ttu-id="4c457-302">Служба продолжит работу.</span><span class="sxs-lookup"><span data-stu-id="4c457-302">The service continues to run.</span></span> <span data-ttu-id="4c457-303">Однако если служба остановлена, ее нельзя перезапустить, так как SCM продолжит использовать старый, недопустимый пароль.</span><span class="sxs-lookup"><span data-stu-id="4c457-303">However, if the service stops, you cannot restart it because the SCM continues to use the old, invalid password.</span></span> <span data-ttu-id="4c457-304">Изменение пароля в Active Directory не приводит к изменению пароля, хранящегося в базе данных служб.</span><span class="sxs-lookup"><span data-stu-id="4c457-304">Changing the password in Active Directory does not change the password stored in the services database.</span></span>

<span data-ttu-id="4c457-305">При запуске служб с обычными учетными записями пользователей необходимо обновлять эти пароли служб при каждом изменении пароля учетной записи пользователя.</span><span class="sxs-lookup"><span data-stu-id="4c457-305">If you run services under regular user accounts, you need to update those service passwords each time the user account password changes.</span></span> <span data-ttu-id="4c457-306">Это может быть особенно трудоемким, если вы не уверены, какие службы выполняются под этой учетной записью или на каких компьютерах выполняются службы с этой учетной записью.</span><span class="sxs-lookup"><span data-stu-id="4c457-306">This can be particularly time-consuming if you are not sure which services are running under that account or which computers have services running under that account.</span></span> <span data-ttu-id="4c457-307">К счастью, вы можете использовать инструментарий WMI для проверки учетных записей служб на всех компьютерах и при необходимости изменить пароль учетной записи службы.</span><span class="sxs-lookup"><span data-stu-id="4c457-307">Fortunately, you can use WMI to check the service accounts on all your computers and, if necessary, change the service account password.</span></span>

<span data-ttu-id="4c457-308">Параметр [**Win32 \_ лоадордерграуп**](/windows/desktop/CIMWin32Prov/win32-loadordergroup) представляет группу системных служб, определяющих зависимости выполнения.</span><span class="sxs-lookup"><span data-stu-id="4c457-308">The [**Win32\_LoadOrderGroup**](/windows/desktop/CIMWin32Prov/win32-loadordergroup) parameter represents a group of system services that define execution dependencies.</span></span> <span data-ttu-id="4c457-309">Службы должны запускаться в порядке, указанном в группе порядок загрузки, так как службы зависят друг от друга.</span><span class="sxs-lookup"><span data-stu-id="4c457-309">The services must be initiated in the order specified by the Load Order Group because the services depend on each other.</span></span> <span data-ttu-id="4c457-310">Для правильной работы этих зависимых служб требуется наличие предшествующих служб.</span><span class="sxs-lookup"><span data-stu-id="4c457-310">These dependent services require the presence of the antecedent services to function correctly.</span></span>

<span data-ttu-id="4c457-311">Чтобы изменить службу с сетевой службы на локальную систему, параметры *StartName* и *стартпассворд* должны иметь следующие значения:</span><span class="sxs-lookup"><span data-stu-id="4c457-311">To change a service from a network service to a local system the *StartName* and *StartPassword* parameters should have the following values:</span></span>


```C++
StartName = "LocalSystem"
StartPassword = "" // - empty string, not NULL
```



<span data-ttu-id="4c457-312">Чтобы изменить службу с локальной системной службы на сеть, параметры *StartName* и *стартпассворд* должны иметь следующие значения:</span><span class="sxs-lookup"><span data-stu-id="4c457-312">To change a service from a local system service to a network the *StartName* and *StartPassword* parameters should have the following values:</span></span>


```C++
StartName = "NT AUTHORITY\NetworkService"
StartPassword = "" // - empty string, not NULL
```



## <a name="examples"></a><span data-ttu-id="4c457-313">Примеры</span><span class="sxs-lookup"><span data-stu-id="4c457-313">Examples</span></span>

<span data-ttu-id="4c457-314">Следующая команда VBScript изменяет учетную запись службы для служб, выполняемых от имени указанной учетной записи пользователя, на LocalSystem.</span><span class="sxs-lookup"><span data-stu-id="4c457-314">The following VBScript changes the service account for services from running under a specified user account to LocalSystem.</span></span>


```VB
strComputer = "."
Set objWMIService = GetObject("winmgmts:" _
 & "{impersonationLevel=impersonate}!\\" & strComputer & "\root\cimv2")
Set colServiceList = objWMIService.ExecQuery _
 ("SELECT * FROM Win32_Service WHERE StartName = '.\\NetSvc'")
For Each objService in colServices
 errServiceChange = objService.Change _
 ( , , , , , , ".\LocalSystem" , "")
Next
```



<span data-ttu-id="4c457-315">Следующая команда VBScript изменяет пароль учетной записи службы для всех сценариев, выполняемых в Нетсвк</span><span class="sxs-lookup"><span data-stu-id="4c457-315">The following VBScript changes the service account password for all scripts running under Netsvc</span></span>


```VB
strComputer = "."
Set objWMIService = GetObject("winmgmts:" _
 & "{impersonationLevel=impersonate}!\\" & strComputer & "\root\cimv2")
Set colServiceList = objWMIService.ExecQuery _
 ("SELECT * FROM Win32_Service WHERE StartName = '.\\NetSvc'")
For Each objservice in colServiceList
 errReturn = objService.Change( , , , , , , , "password")
Next
```



## <a name="requirements"></a><span data-ttu-id="4c457-316">Требования</span><span class="sxs-lookup"><span data-stu-id="4c457-316">Requirements</span></span>



| <span data-ttu-id="4c457-317">Требование</span><span class="sxs-lookup"><span data-stu-id="4c457-317">Requirement</span></span> | <span data-ttu-id="4c457-318">Значение</span><span class="sxs-lookup"><span data-stu-id="4c457-318">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="4c457-319">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="4c457-319">Minimum supported client</span></span><br/> | <span data-ttu-id="4c457-320">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="4c457-320">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="4c457-321">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="4c457-321">Minimum supported server</span></span><br/> | <span data-ttu-id="4c457-322">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="4c457-322">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="4c457-323">Пространство имен</span><span class="sxs-lookup"><span data-stu-id="4c457-323">Namespace</span></span><br/>                | <span data-ttu-id="4c457-324">Корневой \\ CIMv2 \\ терминалсервицес</span><span class="sxs-lookup"><span data-stu-id="4c457-324">Root\\CIMv2\\TerminalServices</span></span><br/>                                                |
| <span data-ttu-id="4c457-325">Header</span><span class="sxs-lookup"><span data-stu-id="4c457-325">Header</span></span><br/>                   | <dl> <span data-ttu-id="4c457-326"><dt>Мбнапи. h</dt></span><span class="sxs-lookup"><span data-stu-id="4c457-326"><dt>Mbnapi.h</dt></span></span> </dl>     |
| <span data-ttu-id="4c457-327">MOF</span><span class="sxs-lookup"><span data-stu-id="4c457-327">MOF</span></span><br/>                      | <dl> <span data-ttu-id="4c457-328"><dt>Тскфгвми. mof</dt></span><span class="sxs-lookup"><span data-stu-id="4c457-328"><dt>TSCfgWmi.mof</dt></span></span> </dl> |
| <span data-ttu-id="4c457-329">DLL</span><span class="sxs-lookup"><span data-stu-id="4c457-329">DLL</span></span><br/>                      | <dl> <span data-ttu-id="4c457-330"><dt>TSCfgWmi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="4c457-330"><dt>TSCfgWmi.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="4c457-331">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="4c457-331">See also</span></span>

<dl> <dt>

[<span data-ttu-id="4c457-332">**\_Служба Win32**</span><span class="sxs-lookup"><span data-stu-id="4c457-332">**Win32\_Service**</span></span>](/windows/desktop/CIMWin32Prov/win32-service)
</dt> <dt>

[<span data-ttu-id="4c457-333">Классы операционной системы</span><span class="sxs-lookup"><span data-stu-id="4c457-333">Operating System Classes</span></span>](/windows/desktop/CIMWin32Prov/operating-system-classes)
</dt> <dt>

[<span data-ttu-id="4c457-334">**\_Терминалсервице Win32**</span><span class="sxs-lookup"><span data-stu-id="4c457-334">**Win32\_TerminalService**</span></span>](win32-terminalservice.md)
</dt> <dt>

[<span data-ttu-id="4c457-335">Задачи WMI: службы</span><span class="sxs-lookup"><span data-stu-id="4c457-335">WMI Tasks: Services</span></span>](/windows/desktop/WmiSdk/wmi-tasks--services)
</dt> </dl>

 

