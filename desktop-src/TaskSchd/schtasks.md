---
title: Schtasks.exe
description: Позволяет администратору создавать, удалять, запрашивать, изменять, запускать и завершать запланированные задачи на локальном или удаленном компьютере.
ms.assetid: 3cf973de-14c4-4ca9-86a7-7f97181bd9e0
keywords:
- Schtasks.exe планировщик задач
topic_type:
- apiref
api_name:
- Schtasks.exe
api_type:
- NA
ms.topic: reference
ms.custom: snippet-project
ms.date: 05/31/2018
ms.openlocfilehash: 2a57ee4edae1cd1604f10a88f3fc8cf2ea0971fb
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105675219"
---
# <a name="schtasksexe"></a><span data-ttu-id="6bfb7-104">Schtasks.exe</span><span class="sxs-lookup"><span data-stu-id="6bfb7-104">Schtasks.exe</span></span>

<span data-ttu-id="6bfb7-105">Позволяет администратору создавать, удалять, запрашивать, изменять, запускать и завершать запланированные задачи на локальном или удаленном компьютере.</span><span class="sxs-lookup"><span data-stu-id="6bfb7-105">Enables an administrator to create, delete, query, change, run, and end scheduled tasks on a local or remote computer.</span></span> <span data-ttu-id="6bfb7-106">При выполнении Schtasks.exe без аргументов отображается состояние и время следующего выполнения для каждой зарегистрированной задачи.</span><span class="sxs-lookup"><span data-stu-id="6bfb7-106">Running Schtasks.exe without arguments displays the status and next run time for each registered task.</span></span> 

<span data-ttu-id="6bfb7-107">Дополнительные сведения о планировщик задач см. в статье Введение: [планировщик задач для разработчиков](task-scheduler-start-page.md).</span><span class="sxs-lookup"><span data-stu-id="6bfb7-107">For more information on Task Scheduler, see this introduction: [Task Scheduler for developers](task-scheduler-start-page.md).</span></span>

## <a name="creating-a-task"></a><span data-ttu-id="6bfb7-108">Создание задачи</span><span class="sxs-lookup"><span data-stu-id="6bfb7-108">Creating a Task</span></span>

<span data-ttu-id="6bfb7-109">Для создания задачи на локальном или удаленном компьютере используется следующий синтаксис.</span><span class="sxs-lookup"><span data-stu-id="6bfb7-109">The following syntax is used to create a task on the local or remote computer.</span></span>

``` syntax
schtasks /Create 
[/S system [/U username [/P [password]]]]
[/RU username [/RP [password]] /SC schedule [/MO modifier] [/D day]
[/M months] [/I idletime] /TN taskname /TR taskrun [/ST starttime]
[/RI interval] [ {/ET endtime | /DU duration} [/K] 
[/XML xmlfile] [/V1]] [/SD startdate] [/ED enddate] [/IT] [/Z] [/F]
```

## <a name="parameters"></a><span data-ttu-id="6bfb7-110">Параметры</span><span class="sxs-lookup"><span data-stu-id="6bfb7-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="6bfb7-111"><span id="_S_system"></span><span id="_s_system"></span><span id="_S_SYSTEM"></span>**/S** , **система**</span><span class="sxs-lookup"><span data-stu-id="6bfb7-111"><span id="_S_system"></span><span id="_s_system"></span><span id="_S_SYSTEM"></span>**/S** **system**</span></span>
</dt> <dd>

<span data-ttu-id="6bfb7-112">Значение типа, указывающее удаленный компьютер для подключения.</span><span class="sxs-lookup"><span data-stu-id="6bfb7-112">A value that specifies the remote computer to connect to.</span></span> <span data-ttu-id="6bfb7-113">Если этот параметр опущен, по умолчанию используется локальный компьютер.</span><span class="sxs-lookup"><span data-stu-id="6bfb7-113">If omitted, the system parameter defaults to the local computer.</span></span>

</dd> <dt>

<span data-ttu-id="6bfb7-114"><span id="_U_username"></span><span id="_u_username"></span><span id="_U_USERNAME"></span>**/U** **имя_пользователя**</span><span class="sxs-lookup"><span data-stu-id="6bfb7-114"><span id="_U_username"></span><span id="_u_username"></span><span id="_U_USERNAME"></span>**/U** **username**</span></span>
</dt> <dd>

<span data-ttu-id="6bfb7-115">Значение типа, указывающее контекст пользователя, в котором будет выполняться Schtasks.exe.</span><span class="sxs-lookup"><span data-stu-id="6bfb7-115">A value that specifies the user context under which Schtasks.exe should run.</span></span>

</dd> <dt>

<span data-ttu-id="6bfb7-116"><span id="_P__password_"></span><span id="_p__password_"></span><span id="_P__PASSWORD_"></span>**/P** **\[ пароль \]**</span><span class="sxs-lookup"><span data-stu-id="6bfb7-116"><span id="_P__password_"></span><span id="_p__password_"></span><span id="_P__PASSWORD_"></span>**/P** **\[password\]**</span></span>
</dt> <dd>

<span data-ttu-id="6bfb7-117">Значение типа, указывающее пароль для данного пользовательского контекста.</span><span class="sxs-lookup"><span data-stu-id="6bfb7-117">A value that specifies the password for a given user context.</span></span> <span data-ttu-id="6bfb7-118">Если этот параметр опущен, Schtasks.exe запрашивает у пользователя входные данные.</span><span class="sxs-lookup"><span data-stu-id="6bfb7-118">If omitted, Schtasks.exe prompts the user for input.</span></span>

</dd> <dt>

<span data-ttu-id="6bfb7-119"><span id="_RU_username"></span><span id="_ru_username"></span><span id="_RU_USERNAME"></span> **Имя пользователя** /ru</span><span class="sxs-lookup"><span data-stu-id="6bfb7-119"><span id="_RU_username"></span><span id="_ru_username"></span><span id="_RU_USERNAME"></span>**/RU** **username**</span></span>
</dt> <dd>

<span data-ttu-id="6bfb7-120">Значение типа, указывающее контекст пользователя, в котором выполняется задача.</span><span class="sxs-lookup"><span data-stu-id="6bfb7-120">A value that specifies the user context under which the task runs.</span></span> <span data-ttu-id="6bfb7-121">Для системной учетной записи допустимыми значениями являются "", "система NT AUTHORITY \\ System" или "System".</span><span class="sxs-lookup"><span data-stu-id="6bfb7-121">For the system account, valid values are "", "NT AUTHORITY\\SYSTEM", or "SYSTEM".</span></span> <span data-ttu-id="6bfb7-122">Для планировщик задач 2,0 задач, "служба NT AUTHORITY \\ LocalService" и "NT Authority \\ NetworkService" также являются допустимыми значениями.</span><span class="sxs-lookup"><span data-stu-id="6bfb7-122">For Task Scheduler 2.0 tasks, "NT AUTHORITY\\LOCALSERVICE", and "NT AUTHORITY\\NETWORKSERVICE" are also valid values.</span></span>

</dd> <dt>

<span data-ttu-id="6bfb7-123"><span id="_RP__password_"></span><span id="_rp__password_"></span><span id="_RP__PASSWORD_"></span>**/RP** **\[ пароль \]**</span><span class="sxs-lookup"><span data-stu-id="6bfb7-123"><span id="_RP__password_"></span><span id="_rp__password_"></span><span id="_RP__PASSWORD_"></span>**/RP** **\[password\]**</span></span>
</dt> <dd>

<span data-ttu-id="6bfb7-124">Значение типа, указывающее пароль для пользователя, указанного с помощью параметра/RU.</span><span class="sxs-lookup"><span data-stu-id="6bfb7-124">A value that specifies the password for the user specified with the /RU parameter.</span></span> <span data-ttu-id="6bfb7-125">Для запроса пароля значение должно быть либо " \* ", либо без значения.</span><span class="sxs-lookup"><span data-stu-id="6bfb7-125">To prompt for the password, the value must be either "\*" or no value.</span></span> <span data-ttu-id="6bfb7-126">Этот пароль не учитывается для системной учетной записи.</span><span class="sxs-lookup"><span data-stu-id="6bfb7-126">This password is ignored for the system account.</span></span> <span data-ttu-id="6bfb7-127">Этот параметр необходимо сочетать с параметром/RU или/XML.</span><span class="sxs-lookup"><span data-stu-id="6bfb7-127">This parameter must be combined with either /RU or the /XML switch.</span></span>

</dd> <dt>

<span data-ttu-id="6bfb7-128"><span id="_SC_schedule"></span><span id="_sc_schedule"></span><span id="_SC_SCHEDULE"></span>**/SC** **Schedule**</span><span class="sxs-lookup"><span data-stu-id="6bfb7-128"><span id="_SC_schedule"></span><span id="_sc_schedule"></span><span id="_SC_SCHEDULE"></span>**/SC** **schedule**</span></span>
</dt> <dd>

<span data-ttu-id="6bfb7-129">Значение, указывающее периодичность расписания.</span><span class="sxs-lookup"><span data-stu-id="6bfb7-129">A value that specifies the schedule frequency.</span></span> <span data-ttu-id="6bfb7-130">Допустимые значения: минуты, ЕЖЕЧАСно, ежедневно, ЕЖЕНЕДЕЛЬно, ЕЖЕМЕСЯЧно, один раз, OnLogon, OnLogon и OnLogon.</span><span class="sxs-lookup"><span data-stu-id="6bfb7-130">Valid values are: MINUTE, HOURLY, DAILY, WEEKLY, MONTHLY, ONCE, ONLOGON, ONIDLE, and ONEVENT.</span></span>

</dd> <dt>

<span data-ttu-id="6bfb7-131"><span id="_MO_modifier"></span><span id="_mo_modifier"></span><span id="_MO_MODIFIER"></span>**/Mo** **Модификатор**</span><span class="sxs-lookup"><span data-stu-id="6bfb7-131"><span id="_MO_modifier"></span><span id="_mo_modifier"></span><span id="_MO_MODIFIER"></span>**/MO** **modifier**</span></span>
</dt> <dd>

<span data-ttu-id="6bfb7-132">Значение, которое позволяет уточнить тип расписания, чтобы обеспечить более точный контроль над повторением расписания.</span><span class="sxs-lookup"><span data-stu-id="6bfb7-132">A value that refines the schedule type to allow for finer control over the schedule recurrence.</span></span> <span data-ttu-id="6bfb7-133">Допустимые значения:</span><span class="sxs-lookup"><span data-stu-id="6bfb7-133">Valid values are:</span></span>

-   <span data-ttu-id="6bfb7-134">МИНУТа: 1-1439 минут.</span><span class="sxs-lookup"><span data-stu-id="6bfb7-134">MINUTE: 1 - 1439 minutes.</span></span>
-   <span data-ttu-id="6bfb7-135">ЕЖЕЧАСно: 1-23 ч.</span><span class="sxs-lookup"><span data-stu-id="6bfb7-135">HOURLY: 1 - 23 hours.</span></span>
-   <span data-ttu-id="6bfb7-136">ЕЖЕДНЕВНО: 1-365 дней.</span><span class="sxs-lookup"><span data-stu-id="6bfb7-136">DAILY: 1 - 365 days.</span></span>
-   <span data-ttu-id="6bfb7-137">ЕЖЕНЕДЕЛЬно: недели 1-52.</span><span class="sxs-lookup"><span data-stu-id="6bfb7-137">WEEKLY: weeks 1 - 52.</span></span>
-   <span data-ttu-id="6bfb7-138">ОДНОКРАТНО: нет модификаторов.</span><span class="sxs-lookup"><span data-stu-id="6bfb7-138">ONCE: No modifiers.</span></span>
-   <span data-ttu-id="6bfb7-139">OnStart: нет модификаторов.</span><span class="sxs-lookup"><span data-stu-id="6bfb7-139">ONSTART: No modifiers.</span></span>
-   <span data-ttu-id="6bfb7-140">OnLogon: без модификаторов.</span><span class="sxs-lookup"><span data-stu-id="6bfb7-140">ONLOGON: No modifiers.</span></span>
-   <span data-ttu-id="6bfb7-141">OnIdle: нет модификаторов.</span><span class="sxs-lookup"><span data-stu-id="6bfb7-141">ONIDLE: No modifiers.</span></span>
-   <span data-ttu-id="6bfb7-142">ЕЖЕМЕСЯЧно: 1-12, первый, второй, третий, четвертый, последний и ЛАСТДАЙ.</span><span class="sxs-lookup"><span data-stu-id="6bfb7-142">MONTHLY: 1 - 12, or FIRST, SECOND, THIRD, FOURTH, LAST, and LASTDAY.</span></span>
-   <span data-ttu-id="6bfb7-143">Oneven: строка запроса события XPath.</span><span class="sxs-lookup"><span data-stu-id="6bfb7-143">ONEVENT: XPath event query string.</span></span>

</dd> <dt>

<span data-ttu-id="6bfb7-144"><span id="_D_days"></span><span id="_d_days"></span><span id="_D_DAYS"></span>**/D** **дн** .</span><span class="sxs-lookup"><span data-stu-id="6bfb7-144"><span id="_D_days"></span><span id="_d_days"></span><span id="_D_DAYS"></span>**/D** **days**</span></span>
</dt> <dd>

<span data-ttu-id="6bfb7-145">Значение типа, указывающее день недели для выполнения задачи.</span><span class="sxs-lookup"><span data-stu-id="6bfb7-145">A value that specifies the day of the week to run the task.</span></span> <span data-ttu-id="6bfb7-146">Допустимые значения: Пн, вторник, среда, четверг, пятница, Кот, SUN и ЕЖЕМЕСЯЧное расписание 1-31 (дни месяца).</span><span class="sxs-lookup"><span data-stu-id="6bfb7-146">Valid values are: MON, TUE, WED, THU, FRI, SAT, SUN and for MONTHLY schedules 1 - 31 (days of the month).</span></span> <span data-ttu-id="6bfb7-147">Символ-шаблон ( \* ) указывает все дни.</span><span class="sxs-lookup"><span data-stu-id="6bfb7-147">The wildcard character (\*) specifies all days.</span></span>

</dd> <dt>

<span data-ttu-id="6bfb7-148"><span id="_M_months"></span><span id="_m_months"></span><span id="_M_MONTHS"></span>**/M** **мес** .</span><span class="sxs-lookup"><span data-stu-id="6bfb7-148"><span id="_M_months"></span><span id="_m_months"></span><span id="_M_MONTHS"></span>**/M** **months**</span></span>
</dt> <dd>

<span data-ttu-id="6bfb7-149">Значение, указывающее месяцы года.</span><span class="sxs-lookup"><span data-stu-id="6bfb7-149">A value that specifies months of the year.</span></span> <span data-ttu-id="6bfb7-150">По умолчанию используется первый день месяца.</span><span class="sxs-lookup"><span data-stu-id="6bfb7-150">Defaults to the first day of the month.</span></span> <span data-ttu-id="6bfb7-151">Допустимые значения: JAN, фев, MAR, Апр, Май, июн, Июл, Авг, SEP, OCT, Ноя и DEC.</span><span class="sxs-lookup"><span data-stu-id="6bfb7-151">Valid values are: JAN, FEB, MAR, APR, MAY, JUN, JUL, AUG, SEP, OCT, NOV, and DEC.</span></span> <span data-ttu-id="6bfb7-152">Символ-шаблон ( \* ) указывает все месяцы.</span><span class="sxs-lookup"><span data-stu-id="6bfb7-152">The wildcard character (\*) specifies all months.</span></span>

</dd> <dt>

<span data-ttu-id="6bfb7-153"><span id="_I_idletime"></span><span id="_i_idletime"></span><span id="_I_IDLETIME"></span>**/I** **идлетиме**</span><span class="sxs-lookup"><span data-stu-id="6bfb7-153"><span id="_I_idletime"></span><span id="_i_idletime"></span><span id="_I_IDLETIME"></span>**/I** **idletime**</span></span>
</dt> <dd>

<span data-ttu-id="6bfb7-154">Значение, указывающее время бездействия, которое необходимо ожидать перед выполнением запланированной задачи OnIdle.</span><span class="sxs-lookup"><span data-stu-id="6bfb7-154">A value that specifies the amount of idle time to wait before running a scheduled ONIDLE task.</span></span> <span data-ttu-id="6bfb7-155">Допустимый диапазон — 1-999 минут.</span><span class="sxs-lookup"><span data-stu-id="6bfb7-155">The valid range is 1 - 999 minutes.</span></span>

</dd> <dt>

<span data-ttu-id="6bfb7-156"><span id="_TN_taskname"></span><span id="_tn_taskname"></span><span id="_TN_TASKNAME"></span>**/TN** **имя_задания**</span><span class="sxs-lookup"><span data-stu-id="6bfb7-156"><span id="_TN_taskname"></span><span id="_tn_taskname"></span><span id="_TN_TASKNAME"></span>**/TN** **taskname**</span></span>
</dt> <dd>

<span data-ttu-id="6bfb7-157">Значение типа, указывающее имя, которое однозначно определяет запланированную задачу.</span><span class="sxs-lookup"><span data-stu-id="6bfb7-157">A value that specifies a name which uniquely identifies the scheduled task.</span></span>

</dd> <dt>

<span data-ttu-id="6bfb7-158"><span id="_TR_taskrun"></span><span id="_tr_taskrun"></span><span id="_TR_TASKRUN"></span>**/Tr** </span><span class="sxs-lookup"><span data-stu-id="6bfb7-158"><span id="_TR_taskrun"></span><span id="_tr_taskrun"></span><span id="_TR_TASKRUN"></span>**/TR** **taskrun**</span></span>
</dt> <dd>

<span data-ttu-id="6bfb7-159">Значение, указывающее путь и имя файла задачи, выполняемой в запланированное время.</span><span class="sxs-lookup"><span data-stu-id="6bfb7-159">A value that specifies the path and file name of the task to be run at the scheduled time.</span></span> <span data-ttu-id="6bfb7-160">Например: C: \\ Windows \\ system32 \\calc.exe.</span><span class="sxs-lookup"><span data-stu-id="6bfb7-160">For example: C:\\Windows\\System32\\calc.exe.</span></span>

</dd> <dt>

<span data-ttu-id="6bfb7-161"><span id="_ST_starttime"></span><span id="_st_starttime"></span><span id="_ST_STARTTIME"></span>**/St** **StartTime**</span><span class="sxs-lookup"><span data-stu-id="6bfb7-161"><span id="_ST_starttime"></span><span id="_st_starttime"></span><span id="_ST_STARTTIME"></span>**/ST** **starttime**</span></span>
</dt> <dd>

<span data-ttu-id="6bfb7-162">Значение, указывающее время начала выполнения задачи.</span><span class="sxs-lookup"><span data-stu-id="6bfb7-162">A value that specifies the start time to run the task.</span></span> <span data-ttu-id="6bfb7-163">Формат времени — ЧЧ: мм (24-часовое время).</span><span class="sxs-lookup"><span data-stu-id="6bfb7-163">The time format is HH:mm (24-hour time).</span></span> <span data-ttu-id="6bfb7-164">Например, 14:30 указывает 2:30.</span><span class="sxs-lookup"><span data-stu-id="6bfb7-164">For example, 14:30 specifies 2:30PM.</span></span> <span data-ttu-id="6bfb7-165">Значение по умолчанию — текущее время — не указано значение/ST.</span><span class="sxs-lookup"><span data-stu-id="6bfb7-165">The default is the current time is /ST is not specified.</span></span> <span data-ttu-id="6bfb7-166">Этот параметр является обязательным и аргументом/SC ONCE.</span><span class="sxs-lookup"><span data-stu-id="6bfb7-166">This option is required wit the /SC ONCE argument.</span></span>

</dd> <dt>

<span data-ttu-id="6bfb7-167"><span id="_RI_interval"></span><span id="_ri_interval"></span><span id="_RI_INTERVAL"></span>**/RI** **интервал**</span><span class="sxs-lookup"><span data-stu-id="6bfb7-167"><span id="_RI_interval"></span><span id="_ri_interval"></span><span id="_RI_INTERVAL"></span>**/RI** **interval**</span></span>
</dt> <dd>

<span data-ttu-id="6bfb7-168">Значение, указывающее интервал повторения в минутах.</span><span class="sxs-lookup"><span data-stu-id="6bfb7-168">A value that specifies the repetition interval in minutes.</span></span> <span data-ttu-id="6bfb7-169">Это неприменимо для следующих типов расписания: минуты, ЕЖЕЧАСно, OnStart, OnStart, OnStart и OnStart.</span><span class="sxs-lookup"><span data-stu-id="6bfb7-169">This is not applicable for the following schedule types: MINUTE, HOURLY, ONSTART, ONLOGON, ONIDLE, and ONEVENT.</span></span> <span data-ttu-id="6bfb7-170">Допустимый диапазон — 1-599940 минут.</span><span class="sxs-lookup"><span data-stu-id="6bfb7-170">The valid range is 1 - 599940 minutes.</span></span> <span data-ttu-id="6bfb7-171">Если указаны параметры/ET или/DU, значение по умолчанию — 10 минут.</span><span class="sxs-lookup"><span data-stu-id="6bfb7-171">If either the /ET or /DU parameters are specified, the default is 10 minutes.</span></span>

<span data-ttu-id="6bfb7-172">**Windows XP и Windows Server 2003:** Этот параметр недоступен.</span><span class="sxs-lookup"><span data-stu-id="6bfb7-172">**Windows XP and Windows Server 2003:** This option is not available.</span></span>

</dd> <dt>

<span data-ttu-id="6bfb7-173"><span id="_ET_endtime"></span><span id="_et_endtime"></span><span id="_ET_ENDTIME"></span>Время **окончания** **/et**</span><span class="sxs-lookup"><span data-stu-id="6bfb7-173"><span id="_ET_endtime"></span><span id="_et_endtime"></span><span id="_ET_ENDTIME"></span>**/ET** **endtime**</span></span>
</dt> <dd>

<span data-ttu-id="6bfb7-174">Значение типа, указывающее время окончания выполнения задачи.</span><span class="sxs-lookup"><span data-stu-id="6bfb7-174">A value that specifies the end time to run the task.</span></span> <span data-ttu-id="6bfb7-175">Формат времени — ЧЧ: мм (24-часовое время).</span><span class="sxs-lookup"><span data-stu-id="6bfb7-175">The time format is HH:mm (24-hour time).</span></span> <span data-ttu-id="6bfb7-176">Например, 14:50 указывает 2:50PM.</span><span class="sxs-lookup"><span data-stu-id="6bfb7-176">For example, 14:50 specifies 2:50PM.</span></span> <span data-ttu-id="6bfb7-177">Это неприменимо для следующих типов расписания: OnStart, OnStart, OnStart и OnStart.</span><span class="sxs-lookup"><span data-stu-id="6bfb7-177">This is not applicable for the following schedule types: ONSTART, ONLOGON, ONIDLE, and ONEVENT.</span></span>

<span data-ttu-id="6bfb7-178">**Windows XP и Windows Server 2003:** Этот параметр недоступен.</span><span class="sxs-lookup"><span data-stu-id="6bfb7-178">**Windows XP and Windows Server 2003:** This option is not available.</span></span>

</dd> <dt>

<span data-ttu-id="6bfb7-179"><span id="_DU_duration"></span><span id="_du_duration"></span><span id="_DU_DURATION"></span>**/Du** **Длительность**</span><span class="sxs-lookup"><span data-stu-id="6bfb7-179"><span id="_DU_duration"></span><span id="_du_duration"></span><span id="_DU_DURATION"></span>**/DU** **duration**</span></span>
</dt> <dd>

<span data-ttu-id="6bfb7-180">Значение типа, указывающее длительность выполнения задачи.</span><span class="sxs-lookup"><span data-stu-id="6bfb7-180">A value that specifies the duration to run the task.</span></span> <span data-ttu-id="6bfb7-181">Формат времени — ЧЧ: мм (24-часовое время).</span><span class="sxs-lookup"><span data-stu-id="6bfb7-181">The time format is HH:mm (24-hour time).</span></span> <span data-ttu-id="6bfb7-182">Например, 14:50 указывает 2:50PM.</span><span class="sxs-lookup"><span data-stu-id="6bfb7-182">For example, 14:50 specifies 2:50PM.</span></span> <span data-ttu-id="6bfb7-183">Это неприменимо к параметрам/ET и для следующих типов расписания: OnStart, OnStart, OnStart и OnStart.</span><span class="sxs-lookup"><span data-stu-id="6bfb7-183">This is not applicable with /ET and for the following schedule types: ONSTART, ONLOGON, ONIDLE, and ONEVENT.</span></span> <span data-ttu-id="6bfb7-184">Для задач/v1 (планировщик задач 1,0 задач), если указан параметр/RI, то длительность по умолчанию составляет один час.</span><span class="sxs-lookup"><span data-stu-id="6bfb7-184">For /V1 tasks (Task Scheduler 1.0 tasks), if /RI is specified, then the duration default is one hour.</span></span>

<span data-ttu-id="6bfb7-185">**Windows XP:** Этот параметр недоступен.</span><span class="sxs-lookup"><span data-stu-id="6bfb7-185">**Windows XP:** This option is not available.</span></span>

</dd> <dt>

<span data-ttu-id="6bfb7-186"><span id="_K_"></span><span id="_k_"></span>**/K**</span><span class="sxs-lookup"><span data-stu-id="6bfb7-186"><span id="_K_"></span><span id="_k_"></span>**/K**</span></span> 
</dt> <dd>

<span data-ttu-id="6bfb7-187">Значение, которое прерывает задачу по времени окончания или длительности.</span><span class="sxs-lookup"><span data-stu-id="6bfb7-187">A value that terminates the task at the end time or duration time.</span></span> <span data-ttu-id="6bfb7-188">Это неприменимо для следующих типов расписания: OnStart, OnStart, OnStart и OnStart.</span><span class="sxs-lookup"><span data-stu-id="6bfb7-188">This is not applicable for the following schedule types: ONSTART, ONLOGON, ONIDLE, and ONEVENT.</span></span> <span data-ttu-id="6bfb7-189">Необходимо указать/ET или/DU.</span><span class="sxs-lookup"><span data-stu-id="6bfb7-189">Either /ET or /DU must be specified.</span></span>

<span data-ttu-id="6bfb7-190">**Windows XP и Windows Server 2003:** Этот параметр недоступен.</span><span class="sxs-lookup"><span data-stu-id="6bfb7-190">**Windows XP and Windows Server 2003:** This option is not available.</span></span>

</dd> <dt>

<span data-ttu-id="6bfb7-191"><span id="_SD_startdate"></span><span id="_sd_startdate"></span><span id="_SD_STARTDATE"></span>**/SD** **Дата** начала</span><span class="sxs-lookup"><span data-stu-id="6bfb7-191"><span id="_SD_startdate"></span><span id="_sd_startdate"></span><span id="_SD_STARTDATE"></span>**/SD** **startdate**</span></span>
</dt> <dd>

<span data-ttu-id="6bfb7-192">Значение, указывающее первую дату выполнения задачи.</span><span class="sxs-lookup"><span data-stu-id="6bfb7-192">A value that specifies the first date on which to run the task.</span></span> <span data-ttu-id="6bfb7-193">Формат: мм/дд/гггг.</span><span class="sxs-lookup"><span data-stu-id="6bfb7-193">The format is mm/dd/yyyy.</span></span> <span data-ttu-id="6bfb7-194">По умолчанию это значение равно текущей дате.</span><span class="sxs-lookup"><span data-stu-id="6bfb7-194">This value defaults to the current date.</span></span> <span data-ttu-id="6bfb7-195">Это неприменимо для следующих типов расписания: "OnStart", "OnStart", "Idle" и "OnStart".</span><span class="sxs-lookup"><span data-stu-id="6bfb7-195">This is not applicable for the following schedule types: ONCE, ONSTART, ONLOGON, ONIDLE, and ONEVENT.</span></span>

</dd> <dt>

<span data-ttu-id="6bfb7-196"><span id="_ED_enddate"></span><span id="_ed_enddate"></span><span id="_ED_ENDDATE"></span>**/ED** **Дата окончания**</span><span class="sxs-lookup"><span data-stu-id="6bfb7-196"><span id="_ED_enddate"></span><span id="_ed_enddate"></span><span id="_ED_ENDDATE"></span>**/ED** **enddate**</span></span>
</dt> <dd>

<span data-ttu-id="6bfb7-197">Значение, указывающее последнюю дату запуска задачи.</span><span class="sxs-lookup"><span data-stu-id="6bfb7-197">A value that specifies the last date that the task will run.</span></span> <span data-ttu-id="6bfb7-198">Формат: мм/дд/гггг.</span><span class="sxs-lookup"><span data-stu-id="6bfb7-198">The format is mm/dd/yyyy.</span></span> <span data-ttu-id="6bfb7-199">Это неприменимо для следующих типов расписания: "OnStart", "OnStart", "Idle" и "OnStart".</span><span class="sxs-lookup"><span data-stu-id="6bfb7-199">This is not applicable for the following schedule types: ONCE, ONSTART, ONLOGON, ONIDLE, and ONEVENT.</span></span>

</dd> <dt>

<span data-ttu-id="6bfb7-200"><span id="_EC_ChannelName"></span><span id="_ec_channelname"></span><span id="_EC_CHANNELNAME"></span>**/ЕК** **ChannelName**</span><span class="sxs-lookup"><span data-stu-id="6bfb7-200"><span id="_EC_ChannelName"></span><span id="_ec_channelname"></span><span id="_EC_CHANNELNAME"></span>**/EC** **ChannelName**</span></span>
</dt> <dd>

<span data-ttu-id="6bfb7-201">Значение, указывающее канал событий для триггеров oneven.</span><span class="sxs-lookup"><span data-stu-id="6bfb7-201">A value that specifies the event channel for ONEVENT triggers.</span></span>

<span data-ttu-id="6bfb7-202">**Windows XP и Windows Server 2003:** Этот параметр недоступен.</span><span class="sxs-lookup"><span data-stu-id="6bfb7-202">**Windows XP and Windows Server 2003:** This option is not available.</span></span>

</dd> <dt>

<span data-ttu-id="6bfb7-203"><span id="_IT_"></span><span id="_it_"></span>**Разрешает**</span><span class="sxs-lookup"><span data-stu-id="6bfb7-203"><span id="_IT_"></span><span id="_it_"></span>**/IT**</span></span> 
</dt> <dd>

<span data-ttu-id="6bfb7-204">Значение, которое позволяет выполнять задачу в интерактивном режиме только в том случае, если пользователь/RU вошел в систему в момент запуска задачи.</span><span class="sxs-lookup"><span data-stu-id="6bfb7-204">A value that enables the task to run interactively only if the /RU user is currently logged on at the time the task runs.</span></span> <span data-ttu-id="6bfb7-205">Задача выполняется только в том случае, если пользователь вошел в систему.</span><span class="sxs-lookup"><span data-stu-id="6bfb7-205">The task runs only if the user is logged on.</span></span>

<span data-ttu-id="6bfb7-206">**Windows XP и Windows Server 2003:** Этот параметр недоступен.</span><span class="sxs-lookup"><span data-stu-id="6bfb7-206">**Windows XP and Windows Server 2003:** This option is not available.</span></span>

</dd> <dt>

<span data-ttu-id="6bfb7-207"><span id="_NP_"></span><span id="_np_"></span>**/нп**</span><span class="sxs-lookup"><span data-stu-id="6bfb7-207"><span id="_NP_"></span><span id="_np_"></span>**/NP**</span></span> 
</dt> <dd>

<span data-ttu-id="6bfb7-208">Значение, указывающее, что пароль не хранится.</span><span class="sxs-lookup"><span data-stu-id="6bfb7-208">A value that indicates that no password is stored.</span></span> <span data-ttu-id="6bfb7-209">Задача не выполняется в интерактивном режиме от имени данного пользователя.</span><span class="sxs-lookup"><span data-stu-id="6bfb7-209">The task does not run interactively as the given user.</span></span> <span data-ttu-id="6bfb7-210">Доступны только локальные ресурсы.</span><span class="sxs-lookup"><span data-stu-id="6bfb7-210">Only local resources are available.</span></span>

<span data-ttu-id="6bfb7-211">**Windows XP и Windows Server 2003:** Этот параметр недоступен.</span><span class="sxs-lookup"><span data-stu-id="6bfb7-211">**Windows XP and Windows Server 2003:** This option is not available.</span></span>

</dd> <dt>

<span data-ttu-id="6bfb7-212"><span id="_Z_"></span><span id="_z_"></span>**/Z**</span><span class="sxs-lookup"><span data-stu-id="6bfb7-212"><span id="_Z_"></span><span id="_z_"></span>**/Z**</span></span> 
</dt> <dd>

<span data-ttu-id="6bfb7-213">Значение, которое помечает задачу, которая должна быть удалена после ее последнего запуска.</span><span class="sxs-lookup"><span data-stu-id="6bfb7-213">A value that marks the task to be deleted after its final run.</span></span>

<span data-ttu-id="6bfb7-214">**Windows XP и Windows Server 2003:** Этот параметр недоступен.</span><span class="sxs-lookup"><span data-stu-id="6bfb7-214">**Windows XP and Windows Server 2003:** This option is not available.</span></span>

</dd> <dt>

<span data-ttu-id="6bfb7-215"><span id="_XML_xmlfile"></span><span id="_xml_xmlfile"></span><span id="_XML_XMLFILE"></span>**/XML** **XmlFile**</span><span class="sxs-lookup"><span data-stu-id="6bfb7-215"><span id="_XML_xmlfile"></span><span id="_xml_xmlfile"></span><span id="_XML_XMLFILE"></span>**/XML** **xmlfile**</span></span>
</dt> <dd>

<span data-ttu-id="6bfb7-216">Значение, которое создает задачу из XML-файла.</span><span class="sxs-lookup"><span data-stu-id="6bfb7-216">A value that creates a task from an XML file.</span></span> <span data-ttu-id="6bfb7-217">Этот параметр можно сочетать с переключателями/RU и/RP или только с параметром/RP, если XML-файл задачи уже содержит участника.</span><span class="sxs-lookup"><span data-stu-id="6bfb7-217">This parameter can be combined with /RU and /RP switches, or with the /RP switch alone when the task XML already contains the principal.</span></span>

<span data-ttu-id="6bfb7-218">**Windows XP и Windows Server 2003:** Этот параметр недоступен.</span><span class="sxs-lookup"><span data-stu-id="6bfb7-218">**Windows XP and Windows Server 2003:** This option is not available.</span></span>

</dd> <dt>

<span data-ttu-id="6bfb7-219"><span id="_V1_"></span><span id="_v1_"></span>**/V1**</span><span class="sxs-lookup"><span data-stu-id="6bfb7-219"><span id="_V1_"></span><span id="_v1_"></span>**/V1**</span></span> 
</dt> <dd>

<span data-ttu-id="6bfb7-220">Значение, которое создает задачу, видимую для платформ Windows 2000, Windows Server 2003 и Windows XP.</span><span class="sxs-lookup"><span data-stu-id="6bfb7-220">A value that creates a task visible to Windows 2000, Windows Server 2003, and Windows XP platforms.</span></span>

<span data-ttu-id="6bfb7-221">**Windows XP и Windows Server 2003:** Этот параметр недоступен.</span><span class="sxs-lookup"><span data-stu-id="6bfb7-221">**Windows XP and Windows Server 2003:** This option is not available.</span></span>

</dd> <dt>

<span data-ttu-id="6bfb7-222"><span id="_F_"></span><span id="_f_"></span>**Ключа**</span><span class="sxs-lookup"><span data-stu-id="6bfb7-222"><span id="_F_"></span><span id="_f_"></span>**/F**</span></span> 
</dt> <dd>

<span data-ttu-id="6bfb7-223">Значение, которое принудительно создает задачу и подавляет предупреждения, если указанная задача уже существует.</span><span class="sxs-lookup"><span data-stu-id="6bfb7-223">A value that forcefully creates the task and suppresses warnings if the specified task already exists.</span></span>

<span data-ttu-id="6bfb7-224">**Windows XP и Windows Server 2003:** Этот параметр недоступен.</span><span class="sxs-lookup"><span data-stu-id="6bfb7-224">**Windows XP and Windows Server 2003:** This option is not available.</span></span>

</dd> <dt>

<span data-ttu-id="6bfb7-225"><span id="_RL_level"></span><span id="_rl_level"></span><span id="_RL_LEVEL"></span> **Уровень** /РЛ</span><span class="sxs-lookup"><span data-stu-id="6bfb7-225"><span id="_RL_level"></span><span id="_rl_level"></span><span id="_RL_LEVEL"></span>**/RL** **level**</span></span>
</dt> <dd>

<span data-ttu-id="6bfb7-226">Значение, устанавливающее уровень выполнения для задачи.</span><span class="sxs-lookup"><span data-stu-id="6bfb7-226">A value that sets the run level for the task.</span></span> <span data-ttu-id="6bfb7-227">Допустимые значения: LIMITED и максимальная.</span><span class="sxs-lookup"><span data-stu-id="6bfb7-227">Valid values are LIMITED and HIGHEST.</span></span> <span data-ttu-id="6bfb7-228">Значение по умолчанию — LIMITED.</span><span class="sxs-lookup"><span data-stu-id="6bfb7-228">The default is LIMITED.</span></span>

<span data-ttu-id="6bfb7-229">**Windows XP и Windows Server 2003:** Этот параметр недоступен.</span><span class="sxs-lookup"><span data-stu-id="6bfb7-229">**Windows XP and Windows Server 2003:** This option is not available.</span></span>

</dd> <dt>

<span data-ttu-id="6bfb7-230"><span id="_DELAY_delaytime"></span><span id="_delay_delaytime"></span><span id="_DELAY_DELAYTIME"></span>**/Delay** **DelayTime**</span><span class="sxs-lookup"><span data-stu-id="6bfb7-230"><span id="_DELAY_delaytime"></span><span id="_delay_delaytime"></span><span id="_DELAY_DELAYTIME"></span>**/DELAY** **delaytime**</span></span>
</dt> <dd>

<span data-ttu-id="6bfb7-231">Значение, указывающее время ожидания задержки задачи после срабатывания триггера.</span><span class="sxs-lookup"><span data-stu-id="6bfb7-231">A value that specifies the wait time to delay the task after the trigger is fired.</span></span> <span data-ttu-id="6bfb7-232">Формат времени — мммм: СС.</span><span class="sxs-lookup"><span data-stu-id="6bfb7-232">The time format is mmmm:ss.</span></span> <span data-ttu-id="6bfb7-233">Этот параметр допустим только для типов расписания OnStart, OnStart и OnStart.</span><span class="sxs-lookup"><span data-stu-id="6bfb7-233">This option is only valid for schedule types ONSTART, ONLOGON, and ONEVENT.</span></span>

<span data-ttu-id="6bfb7-234">**Windows XP и Windows Server 2003:** Этот параметр недоступен.</span><span class="sxs-lookup"><span data-stu-id="6bfb7-234">**Windows XP and Windows Server 2003:** This option is not available.</span></span>

</dd> <dt>

<span data-ttu-id="6bfb7-235"><span id="___"></span>**/?**</span><span class="sxs-lookup"><span data-stu-id="6bfb7-235"><span id="___"></span>**/?**</span></span> 
</dt> <dd>

<span data-ttu-id="6bfb7-236">Значение, которое отображает справочное сообщение для Schtasks.exe.</span><span class="sxs-lookup"><span data-stu-id="6bfb7-236">A value that displays the help message for Schtasks.exe.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="6bfb7-237">Комментарии</span><span class="sxs-lookup"><span data-stu-id="6bfb7-237">Remarks</span></span>

<span data-ttu-id="6bfb7-238">При создании задачи на удаленном компьютере, работающем под управлением операционной системы Windows XP, Windows Server 2003 или Windows 2000, используйте параметр/v1.</span><span class="sxs-lookup"><span data-stu-id="6bfb7-238">When creating a task on a remote computer running on the Windows XP, Windows Server 2003, or Windows 2000 operating system, use the /V1 switch.</span></span>

<span data-ttu-id="6bfb7-239">Невозможно создать неинтерактивную удаленную задачу планировщик задач 1,0 (создайте задачу, не используя параметр/IT, и параметр/V1), если на удаленном компьютере включено исключение брандмауэра для общего доступа к файлам и принтерам, а исключение брандмауэра для удаленного управления назначенными задачами отключено.</span><span class="sxs-lookup"><span data-stu-id="6bfb7-239">You cannot create a non-interactive remote Task Scheduler 1.0 task (create a task by not using the /IT switch and using the /V1 switch) if the remote computer has the File and Printer Sharing firewall exception enabled and the Remote Scheduled Tasks Management firewall exception disabled.</span></span>

## <a name="deleting-a-task"></a><span data-ttu-id="6bfb7-240">Удаление задачи</span><span class="sxs-lookup"><span data-stu-id="6bfb7-240">Deleting a Task</span></span>

<span data-ttu-id="6bfb7-241">Для удаления одной или нескольких запланированных задач используется следующий синтаксис.</span><span class="sxs-lookup"><span data-stu-id="6bfb7-241">The following syntax is used to delete one or more scheduled tasks.</span></span>

``` syntax
schtasks /Delete 
[/S system [/U username [/P [password]]]]
[/TN taskname] [/F]
```

## <a name="parameters"></a><span data-ttu-id="6bfb7-242">Параметры</span><span class="sxs-lookup"><span data-stu-id="6bfb7-242">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="6bfb7-243"><span id="_S_system"></span><span id="_s_system"></span><span id="_S_SYSTEM"></span>**/S** , **система**</span><span class="sxs-lookup"><span data-stu-id="6bfb7-243"><span id="_S_system"></span><span id="_s_system"></span><span id="_S_SYSTEM"></span>**/S** **system**</span></span>
</dt> <dd>

<span data-ttu-id="6bfb7-244">Значение типа, указывающее удаленный компьютер для подключения.</span><span class="sxs-lookup"><span data-stu-id="6bfb7-244">A value that specifies the remote computer to connect to.</span></span> <span data-ttu-id="6bfb7-245">Если этот параметр опущен, по умолчанию используется локальный компьютер.</span><span class="sxs-lookup"><span data-stu-id="6bfb7-245">If omitted, the system parameter defaults to the local computer.</span></span>

</dd> <dt>

<span data-ttu-id="6bfb7-246"><span id="_U_username"></span><span id="_u_username"></span><span id="_U_USERNAME"></span>**/U** **имя_пользователя**</span><span class="sxs-lookup"><span data-stu-id="6bfb7-246"><span id="_U_username"></span><span id="_u_username"></span><span id="_U_USERNAME"></span>**/U** **username**</span></span>
</dt> <dd>

<span data-ttu-id="6bfb7-247">Значение типа, указывающее контекст пользователя, в котором будет выполняться Schtasks.exe.</span><span class="sxs-lookup"><span data-stu-id="6bfb7-247">A value that specifies the user context under which Schtasks.exe should run.</span></span>

</dd> <dt>

<span data-ttu-id="6bfb7-248"><span id="_P__password_"></span><span id="_p__password_"></span><span id="_P__PASSWORD_"></span>**/P** **\[ пароль \]**</span><span class="sxs-lookup"><span data-stu-id="6bfb7-248"><span id="_P__password_"></span><span id="_p__password_"></span><span id="_P__PASSWORD_"></span>**/P** **\[password\]**</span></span>
</dt> <dd>

<span data-ttu-id="6bfb7-249">Значение типа, указывающее пароль для данного пользовательского контекста.</span><span class="sxs-lookup"><span data-stu-id="6bfb7-249">A value that specifies the password for the given user context.</span></span> <span data-ttu-id="6bfb7-250">Если этот параметр опущен, Schtasks.exe запрашивает у пользователя входные данные.</span><span class="sxs-lookup"><span data-stu-id="6bfb7-250">If omitted, Schtasks.exe prompts the user for input.</span></span>

</dd> <dt>

<span data-ttu-id="6bfb7-251"><span id="_TN_taskname"></span><span id="_tn_taskname"></span><span id="_TN_TASKNAME"></span>**/TN** **имя_задания**</span><span class="sxs-lookup"><span data-stu-id="6bfb7-251"><span id="_TN_taskname"></span><span id="_tn_taskname"></span><span id="_TN_TASKNAME"></span>**/TN** **taskname**</span></span>
</dt> <dd>

<span data-ttu-id="6bfb7-252">Значение типа, указывающее имя удаляемой запланированной задачи.</span><span class="sxs-lookup"><span data-stu-id="6bfb7-252">A value that specifies the name of the scheduled task to delete.</span></span> <span data-ttu-id="6bfb7-253">\*Для удаления всех задач можно использовать подстановочный знак ().</span><span class="sxs-lookup"><span data-stu-id="6bfb7-253">The wildcard character (\*) can be used to delete all tasks.</span></span>

</dd> <dt>

<span data-ttu-id="6bfb7-254"><span id="_F_"></span><span id="_f_"></span>**Ключа**</span><span class="sxs-lookup"><span data-stu-id="6bfb7-254"><span id="_F_"></span><span id="_f_"></span>**/F**</span></span> 
</dt> <dd>

<span data-ttu-id="6bfb7-255">Значение, которое принудительно удаляет задачу и подавляет предупреждения, если указанная задача запущена.</span><span class="sxs-lookup"><span data-stu-id="6bfb7-255">A value that forcefully deletes the task and suppresses warnings if the specified task is running.</span></span>

</dd> <dt>

<span data-ttu-id="6bfb7-256"><span id="__"></span>**/?**</span><span class="sxs-lookup"><span data-stu-id="6bfb7-256"><span id="__"></span>**/?**</span></span>
</dt> <dd>

<span data-ttu-id="6bfb7-257">Значение, которое отображает справку для Schtasks.exe.</span><span class="sxs-lookup"><span data-stu-id="6bfb7-257">A value that displays Help for Schtasks.exe.</span></span>

</dd> </dl>

## <a name="running-a-task"></a><span data-ttu-id="6bfb7-258">Выполнение задачи</span><span class="sxs-lookup"><span data-stu-id="6bfb7-258">Running a Task</span></span>

<span data-ttu-id="6bfb7-259">Для немедленного выполнения запланированной задачи используется следующий синтаксис.</span><span class="sxs-lookup"><span data-stu-id="6bfb7-259">The following syntax is used to immediately run a scheduled task.</span></span>

``` syntax
schtasks /Run 
[/S system [/U username [/P [password]]]]
/TN taskname
```

## <a name="parameters"></a><span data-ttu-id="6bfb7-260">Параметры</span><span class="sxs-lookup"><span data-stu-id="6bfb7-260">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="6bfb7-261"><span id="_S_system"></span><span id="_s_system"></span><span id="_S_SYSTEM"></span>**/S** , **система**</span><span class="sxs-lookup"><span data-stu-id="6bfb7-261"><span id="_S_system"></span><span id="_s_system"></span><span id="_S_SYSTEM"></span>**/S** **system**</span></span>
</dt> <dd>

<span data-ttu-id="6bfb7-262">Значение типа, указывающее удаленный компьютер для подключения.</span><span class="sxs-lookup"><span data-stu-id="6bfb7-262">A value that specifies the remote computer to connect to.</span></span> <span data-ttu-id="6bfb7-263">Если этот параметр опущен, по умолчанию используется локальный компьютер.</span><span class="sxs-lookup"><span data-stu-id="6bfb7-263">If omitted, the system parameter defaults to the local computer.</span></span>

</dd> <dt>

<span data-ttu-id="6bfb7-264"><span id="_U_username"></span><span id="_u_username"></span><span id="_U_USERNAME"></span>**/U** **имя_пользователя**</span><span class="sxs-lookup"><span data-stu-id="6bfb7-264"><span id="_U_username"></span><span id="_u_username"></span><span id="_U_USERNAME"></span>**/U** **username**</span></span>
</dt> <dd>

<span data-ttu-id="6bfb7-265">Значение типа, указывающее контекст пользователя, в котором будет выполняться Schtasks.exe.</span><span class="sxs-lookup"><span data-stu-id="6bfb7-265">A value that specifies the user context under which Schtasks.exe should run.</span></span>

</dd> <dt>

<span data-ttu-id="6bfb7-266"><span id="_P__password_"></span><span id="_p__password_"></span><span id="_P__PASSWORD_"></span>**/P** **\[ пароль \]**</span><span class="sxs-lookup"><span data-stu-id="6bfb7-266"><span id="_P__password_"></span><span id="_p__password_"></span><span id="_P__PASSWORD_"></span>**/P** **\[password\]**</span></span>
</dt> <dd>

<span data-ttu-id="6bfb7-267">Значение типа, указывающее пароль для данного пользовательского контекста.</span><span class="sxs-lookup"><span data-stu-id="6bfb7-267">A value that specifies the password for the given user context.</span></span> <span data-ttu-id="6bfb7-268">Если этот параметр опущен, Schtasks.exe запрашивает у пользователя входные данные.</span><span class="sxs-lookup"><span data-stu-id="6bfb7-268">If omitted, Schtasks.exe prompts the user for input.</span></span>

</dd> <dt>

<span data-ttu-id="6bfb7-269"><span id="_TN_taskname"></span><span id="_tn_taskname"></span><span id="_TN_TASKNAME"></span>**/TN** **имя_задания**</span><span class="sxs-lookup"><span data-stu-id="6bfb7-269"><span id="_TN_taskname"></span><span id="_tn_taskname"></span><span id="_TN_TASKNAME"></span>**/TN** **taskname**</span></span>
</dt> <dd>

<span data-ttu-id="6bfb7-270">Значение типа, указывающее имя выполняемой запланированной задачи.</span><span class="sxs-lookup"><span data-stu-id="6bfb7-270">A value that specifies the name of the scheduled task to run.</span></span>

</dd> <dt>

<span data-ttu-id="6bfb7-271"><span id="__"></span>**/?**</span><span class="sxs-lookup"><span data-stu-id="6bfb7-271"><span id="__"></span>**/?**</span></span>
</dt> <dd>

<span data-ttu-id="6bfb7-272">Значение, которое отображает справку для Schtasks.exe.</span><span class="sxs-lookup"><span data-stu-id="6bfb7-272">A value that displays Help for Schtasks.exe.</span></span>

</dd> </dl>

## <a name="ending-a-running-task"></a><span data-ttu-id="6bfb7-273">Завершение выполняющейся задачи</span><span class="sxs-lookup"><span data-stu-id="6bfb7-273">Ending a Running Task</span></span>

<span data-ttu-id="6bfb7-274">Для завершения выполнения запланированной задачи используется следующий синтаксис.</span><span class="sxs-lookup"><span data-stu-id="6bfb7-274">The following syntax is used to stop a running scheduled task.</span></span>

> [!Note]  
> <span data-ttu-id="6bfb7-275">Чтобы предотвратить выполнение удаленной задачи, убедитесь, что на удаленном компьютере включены исключения брандмауэра для управления файлами и принтерами и удаленное управление назначенными задачами.</span><span class="sxs-lookup"><span data-stu-id="6bfb7-275">To stop a remote task from running, ensure that the remote computer has the File and Printer Sharing and Remote Scheduled Tasks Management firewall exceptions enabled.</span></span>

 

``` syntax
schtasks /End 
[/S system [/U username [/P [password]]]]
/TN taskname
```

## <a name="parameters"></a><span data-ttu-id="6bfb7-276">Параметры</span><span class="sxs-lookup"><span data-stu-id="6bfb7-276">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="6bfb7-277"><span id="_S_system"></span><span id="_s_system"></span><span id="_S_SYSTEM"></span>**/S** , **система**</span><span class="sxs-lookup"><span data-stu-id="6bfb7-277"><span id="_S_system"></span><span id="_s_system"></span><span id="_S_SYSTEM"></span>**/S** **system**</span></span>
</dt> <dd>

<span data-ttu-id="6bfb7-278">Значение типа, указывающее удаленный компьютер для подключения.</span><span class="sxs-lookup"><span data-stu-id="6bfb7-278">A value that specifies the remote computer to connect to.</span></span> <span data-ttu-id="6bfb7-279">Если этот параметр опущен, по умолчанию используется локальный компьютер.</span><span class="sxs-lookup"><span data-stu-id="6bfb7-279">If omitted, the system parameter defaults to the local computer.</span></span>

</dd> <dt>

<span data-ttu-id="6bfb7-280"><span id="_U_username"></span><span id="_u_username"></span><span id="_U_USERNAME"></span>**/U** **имя_пользователя**</span><span class="sxs-lookup"><span data-stu-id="6bfb7-280"><span id="_U_username"></span><span id="_u_username"></span><span id="_U_USERNAME"></span>**/U** **username**</span></span>
</dt> <dd>

<span data-ttu-id="6bfb7-281">Значение типа, указывающее контекст пользователя, в котором будет выполняться Schtasks.exe.</span><span class="sxs-lookup"><span data-stu-id="6bfb7-281">A value that specifies the user context under which Schtasks.exe should run.</span></span>

</dd> <dt>

<span data-ttu-id="6bfb7-282"><span id="_P__password_"></span><span id="_p__password_"></span><span id="_P__PASSWORD_"></span>**/P** **\[ пароль \]**</span><span class="sxs-lookup"><span data-stu-id="6bfb7-282"><span id="_P__password_"></span><span id="_p__password_"></span><span id="_P__PASSWORD_"></span>**/P** **\[password\]**</span></span>
</dt> <dd>

<span data-ttu-id="6bfb7-283">Значение типа, указывающее пароль для данного пользовательского контекста.</span><span class="sxs-lookup"><span data-stu-id="6bfb7-283">A value that specifies the password for the given user context.</span></span> <span data-ttu-id="6bfb7-284">Если этот параметр опущен, Schtasks.exe запрашивает у пользователя входные данные.</span><span class="sxs-lookup"><span data-stu-id="6bfb7-284">If omitted, Schtasks.exe prompts the user for input.</span></span>

</dd> <dt>

<span data-ttu-id="6bfb7-285"><span id="_TN_taskname"></span><span id="_tn_taskname"></span><span id="_TN_TASKNAME"></span>**/TN** **имя_задания**</span><span class="sxs-lookup"><span data-stu-id="6bfb7-285"><span id="_TN_taskname"></span><span id="_tn_taskname"></span><span id="_TN_TASKNAME"></span>**/TN** **taskname**</span></span>
</dt> <dd>

<span data-ttu-id="6bfb7-286">Значение типа, указывающее имя запланированной задачи, которую необходимо завершить.</span><span class="sxs-lookup"><span data-stu-id="6bfb7-286">A value that specifies the name of the scheduled task to stop.</span></span>

</dd> <dt>

<span data-ttu-id="6bfb7-287"><span id="__"></span>**/?**</span><span class="sxs-lookup"><span data-stu-id="6bfb7-287"><span id="__"></span>**/?**</span></span>
</dt> <dd>

<span data-ttu-id="6bfb7-288">Значение, которое отображает справку для Schtasks.exe.</span><span class="sxs-lookup"><span data-stu-id="6bfb7-288">A value that displays Help for Schtasks.exe.</span></span>

</dd> </dl>

## <a name="querying-for-task-information"></a><span data-ttu-id="6bfb7-289">Запрос сведений о задачах</span><span class="sxs-lookup"><span data-stu-id="6bfb7-289">Querying for Task Information</span></span>

<span data-ttu-id="6bfb7-290">Для вывода запланированных задач с локального или удаленного компьютера используется следующий синтаксис.</span><span class="sxs-lookup"><span data-stu-id="6bfb7-290">The following syntax is used to display the scheduled tasks from the local or remote computer.</span></span>

``` syntax
schtasks /Query 
[/S system [/U username [/P [password]]]]
[/FO format | /XML] [/NH] [/V] [/TN taskname] [/?]
```

## <a name="parameters"></a><span data-ttu-id="6bfb7-291">Параметры</span><span class="sxs-lookup"><span data-stu-id="6bfb7-291">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="6bfb7-292"><span id="_S_system"></span><span id="_s_system"></span><span id="_S_SYSTEM"></span>**/S** , **система**</span><span class="sxs-lookup"><span data-stu-id="6bfb7-292"><span id="_S_system"></span><span id="_s_system"></span><span id="_S_SYSTEM"></span>**/S** **system**</span></span>
</dt> <dd>

<span data-ttu-id="6bfb7-293">Значение типа, указывающее удаленный компьютер для подключения.</span><span class="sxs-lookup"><span data-stu-id="6bfb7-293">A value that specifies the remote computer to connect to.</span></span> <span data-ttu-id="6bfb7-294">Если этот параметр опущен, по умолчанию используется локальный компьютер.</span><span class="sxs-lookup"><span data-stu-id="6bfb7-294">If omitted, the system parameter defaults to the local computer.</span></span>

</dd> <dt>

<span data-ttu-id="6bfb7-295"><span id="_U_username"></span><span id="_u_username"></span><span id="_U_USERNAME"></span>**/U** **имя_пользователя**</span><span class="sxs-lookup"><span data-stu-id="6bfb7-295"><span id="_U_username"></span><span id="_u_username"></span><span id="_U_USERNAME"></span>**/U** **username**</span></span>
</dt> <dd>

<span data-ttu-id="6bfb7-296">Значение типа, указывающее контекст пользователя, в котором будет выполняться Schtasks.exe.</span><span class="sxs-lookup"><span data-stu-id="6bfb7-296">A value that specifies the user context under which Schtasks.exe should run.</span></span>

</dd> <dt>

<span data-ttu-id="6bfb7-297"><span id="_P__password_"></span><span id="_p__password_"></span><span id="_P__PASSWORD_"></span>**/P** **\[ пароль \]**</span><span class="sxs-lookup"><span data-stu-id="6bfb7-297"><span id="_P__password_"></span><span id="_p__password_"></span><span id="_P__PASSWORD_"></span>**/P** **\[password\]**</span></span>
</dt> <dd>

<span data-ttu-id="6bfb7-298">Значение типа, указывающее пароль для данного пользовательского контекста.</span><span class="sxs-lookup"><span data-stu-id="6bfb7-298">A value that specifies the password for the given user context.</span></span> <span data-ttu-id="6bfb7-299">Если этот параметр опущен, Schtasks.exe запрашивает у пользователя входные данные.</span><span class="sxs-lookup"><span data-stu-id="6bfb7-299">If omitted, Schtasks.exe prompts the user for input.</span></span>

</dd> <dt>

<span data-ttu-id="6bfb7-300"><span id="_FO_format"></span><span id="_fo_format"></span><span id="_FO_FORMAT"></span>**/FO** , **Формат**</span><span class="sxs-lookup"><span data-stu-id="6bfb7-300"><span id="_FO_format"></span><span id="_fo_format"></span><span id="_FO_FORMAT"></span>**/FO** **format**</span></span>
</dt> <dd>

<span data-ttu-id="6bfb7-301">Значение типа, указывающее формат выходных данных.</span><span class="sxs-lookup"><span data-stu-id="6bfb7-301">A value that specifies the output format.</span></span> <span data-ttu-id="6bfb7-302">Допустимые значения: TABLE, LIST и CSV.</span><span class="sxs-lookup"><span data-stu-id="6bfb7-302">The valid values are TABLE, LIST, and CSV.</span></span>

</dd> <dt>

<span data-ttu-id="6bfb7-303"><span id="_NH_"></span><span id="_nh_"></span>**Использован**</span><span class="sxs-lookup"><span data-stu-id="6bfb7-303"><span id="_NH_"></span><span id="_nh_"></span>**/NH**</span></span> 
</dt> <dd>

<span data-ttu-id="6bfb7-304">Значение, указывающее, что заголовок столбца не должен отображаться в выходных данных.</span><span class="sxs-lookup"><span data-stu-id="6bfb7-304">A value that specifies that the column header should not be displayed in the output.</span></span> <span data-ttu-id="6bfb7-305">Это допустимо только для форматов TABLE и CSV.</span><span class="sxs-lookup"><span data-stu-id="6bfb7-305">This is valid only for TABLE and CSV formats.</span></span>

</dd> <dt>

<span data-ttu-id="6bfb7-306"><span id="_V_"></span><span id="_v_"></span>**/V**</span><span class="sxs-lookup"><span data-stu-id="6bfb7-306"><span id="_V_"></span><span id="_v_"></span>**/V**</span></span> 
</dt> <dd>

<span data-ttu-id="6bfb7-307">Значение, отображающее подробные выходные данные задачи.</span><span class="sxs-lookup"><span data-stu-id="6bfb7-307">A value that displays verbose task output.</span></span>

> [!Note]  
> <span data-ttu-id="6bfb7-308">Если задача запланирована на выполнение только один раз, отображаемые сведения о расписании — "данные планирования недоступны в этом формате".</span><span class="sxs-lookup"><span data-stu-id="6bfb7-308">If a task was scheduled to run only one time, then the displayed schedule information is "Scheduling data is not available in this format."</span></span>

 

</dd> <dt>

<span data-ttu-id="6bfb7-309"><span id="_TN_taskname"></span><span id="_tn_taskname"></span><span id="_TN_TASKNAME"></span>**/TN** **имя_задания**</span><span class="sxs-lookup"><span data-stu-id="6bfb7-309"><span id="_TN_taskname"></span><span id="_tn_taskname"></span><span id="_TN_TASKNAME"></span>**/TN** **taskname**</span></span>
</dt> <dd>

<span data-ttu-id="6bfb7-310">Значение типа, указывающее имя задачи, для которой необходимо получить сведения.</span><span class="sxs-lookup"><span data-stu-id="6bfb7-310">A value that specifies the task name for which to retrieve the information.</span></span> <span data-ttu-id="6bfb7-311">Если имя задачи не указано, будут отображены сведения для всех задач.</span><span class="sxs-lookup"><span data-stu-id="6bfb7-311">If no task name is specified, then information for all the tasks will be displayed.</span></span>

<span data-ttu-id="6bfb7-312">**Windows XP и Windows Server 2003:** Этот параметр недоступен.</span><span class="sxs-lookup"><span data-stu-id="6bfb7-312">**Windows XP and Windows Server 2003:** This option is not available.</span></span>

</dd> <dt>

<span data-ttu-id="6bfb7-313"><span id="_XML_"></span><span id="_xml_"></span>**/XML**</span><span class="sxs-lookup"><span data-stu-id="6bfb7-313"><span id="_XML_"></span><span id="_xml_"></span>**/XML**</span></span> 
</dt> <dd>

<span data-ttu-id="6bfb7-314">Значение, используемое для вывода определений задач в формате XML.</span><span class="sxs-lookup"><span data-stu-id="6bfb7-314">A value that is used to display the task definitions in XML format.</span></span>

<span data-ttu-id="6bfb7-315">**Windows XP и Windows Server 2003:** Этот параметр недоступен.</span><span class="sxs-lookup"><span data-stu-id="6bfb7-315">**Windows XP and Windows Server 2003:** This option is not available.</span></span>

</dd> <dt>

<span data-ttu-id="6bfb7-316"><span id="__"></span>**/?**</span><span class="sxs-lookup"><span data-stu-id="6bfb7-316"><span id="__"></span>**/?**</span></span>
</dt> <dd>

<span data-ttu-id="6bfb7-317">Значение, используемое для вывода справки по Schtasks.exe.</span><span class="sxs-lookup"><span data-stu-id="6bfb7-317">A value that is used to display the Help for Schtasks.exe.</span></span>

</dd> </dl>

## <a name="changing-a-task"></a><span data-ttu-id="6bfb7-318">Изменение задачи</span><span class="sxs-lookup"><span data-stu-id="6bfb7-318">Changing a Task</span></span>

<span data-ttu-id="6bfb7-319">Следующий синтаксис используется для изменения способа выполнения программы, а также для изменения учетной записи пользователя и пароля, используемых запланированной задачей.</span><span class="sxs-lookup"><span data-stu-id="6bfb7-319">The following syntax is used to change how the program runs, or change the user account and password used by a scheduled task.</span></span>

``` syntax
schtasks /Change 
[/S system [/U username [/P [password]]]] /TN taskname
{ [/RU runasuser] [/RP runaspassword] [/TR taskrun] [/ST starttime] 
[/RI interval] [ {/ET endtime | /DU duration} [/K] ]
[/SD startdate] [/ED enddate] [/ENABLE | /DISABLE] [/IT] [/Z] }
```

## <a name="parameters"></a><span data-ttu-id="6bfb7-320">Параметры</span><span class="sxs-lookup"><span data-stu-id="6bfb7-320">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="6bfb7-321"><span id="_S_system"></span><span id="_s_system"></span><span id="_S_SYSTEM"></span>**/S** , **система**</span><span class="sxs-lookup"><span data-stu-id="6bfb7-321"><span id="_S_system"></span><span id="_s_system"></span><span id="_S_SYSTEM"></span>**/S** **system**</span></span>
</dt> <dd>

<span data-ttu-id="6bfb7-322">Значение типа, указывающее удаленный компьютер для подключения.</span><span class="sxs-lookup"><span data-stu-id="6bfb7-322">A value that specifies the remote computer to connect to.</span></span> <span data-ttu-id="6bfb7-323">Если этот параметр опущен, по умолчанию используется локальный компьютер.</span><span class="sxs-lookup"><span data-stu-id="6bfb7-323">If omitted, the system parameter defaults to the local computer.</span></span>

</dd> <dt>

<span data-ttu-id="6bfb7-324"><span id="_U_username"></span><span id="_u_username"></span><span id="_U_USERNAME"></span>**/U** **имя_пользователя**</span><span class="sxs-lookup"><span data-stu-id="6bfb7-324"><span id="_U_username"></span><span id="_u_username"></span><span id="_U_USERNAME"></span>**/U** **username**</span></span>
</dt> <dd>

<span data-ttu-id="6bfb7-325">Значение типа, указывающее контекст пользователя, в котором будет выполняться Schtasks.exe.</span><span class="sxs-lookup"><span data-stu-id="6bfb7-325">A value that specifies the user context under which Schtasks.exe should run.</span></span>

</dd> <dt>

<span data-ttu-id="6bfb7-326"><span id="_P__password_"></span><span id="_p__password_"></span><span id="_P__PASSWORD_"></span>**/P** **\[ пароль \]**</span><span class="sxs-lookup"><span data-stu-id="6bfb7-326"><span id="_P__password_"></span><span id="_p__password_"></span><span id="_P__PASSWORD_"></span>**/P** **\[password\]**</span></span>
</dt> <dd>

<span data-ttu-id="6bfb7-327">Значение типа, указывающее пароль для данного пользовательского контекста.</span><span class="sxs-lookup"><span data-stu-id="6bfb7-327">A value that specifies the password for the given user context.</span></span> <span data-ttu-id="6bfb7-328">Если этот параметр опущен, Schtasks.exe запрашивает у пользователя входные данные.</span><span class="sxs-lookup"><span data-stu-id="6bfb7-328">If omitted, Schtasks.exe prompts the user for input.</span></span>

</dd> <dt>

<span data-ttu-id="6bfb7-329"><span id="_TN_taskname"></span><span id="_tn_taskname"></span><span id="_TN_TASKNAME"></span>**/TN** **имя_задания**</span><span class="sxs-lookup"><span data-stu-id="6bfb7-329"><span id="_TN_taskname"></span><span id="_tn_taskname"></span><span id="_TN_TASKNAME"></span>**/TN** **taskname**</span></span>
</dt> <dd>

<span data-ttu-id="6bfb7-330">Значение, указывающее, какую запланированную задачу следует изменить.</span><span class="sxs-lookup"><span data-stu-id="6bfb7-330">A value that specifies which scheduled task to change.</span></span>

</dd> <dt>

<span data-ttu-id="6bfb7-331"><span id="_RU_runasuser"></span><span id="_ru_runasuser"></span><span id="_RU_RUNASUSER"></span>**/Ru**  выполняющий</span><span class="sxs-lookup"><span data-stu-id="6bfb7-331"><span id="_RU_runasuser"></span><span id="_ru_runasuser"></span><span id="_RU_RUNASUSER"></span>**/RU** **runasuser**</span></span>
</dt> <dd>

<span data-ttu-id="6bfb7-332">Значение, которое изменяет имя пользователя (пользовательский контекст), в котором будет выполняться запланированная задача.</span><span class="sxs-lookup"><span data-stu-id="6bfb7-332">A value that changes the user name (user context) under which the scheduled task will run.</span></span> <span data-ttu-id="6bfb7-333">Для системной учетной записи допустимыми значениями являются "", "система NT AUTHORITY \\ System" или "System".</span><span class="sxs-lookup"><span data-stu-id="6bfb7-333">For the system account, valid values are "", "NT AUTHORITY\\SYSTEM", or "SYSTEM".</span></span> <span data-ttu-id="6bfb7-334">Для задач планировщик задач 2,0 \\ \\ доступны также допустимые значения "NT Authority LocalService" и "NT Authority NetworkService".</span><span class="sxs-lookup"><span data-stu-id="6bfb7-334">For Task Scheduler 2.0 tasks, "NT AUTHORITY\\LOCALSERVICE" and "NT AUTHORITY\\NETWORKSERVICE" are also valid values.</span></span>

</dd> <dt>

<span data-ttu-id="6bfb7-335"><span id="_RP_runaspassword"></span><span id="_rp_runaspassword"></span><span id="_RP_RUNASPASSWORD"></span>**/RP** **runaspassword**</span><span class="sxs-lookup"><span data-stu-id="6bfb7-335"><span id="_RP_runaspassword"></span><span id="_rp_runaspassword"></span><span id="_RP_RUNASPASSWORD"></span>**/RP** **runaspassword**</span></span>
</dt> <dd>

<span data-ttu-id="6bfb7-336">Значение типа, указывающее новый пароль для существующего контекста пользователя или пароль для новой учетной записи пользователя.</span><span class="sxs-lookup"><span data-stu-id="6bfb7-336">A value that specifies a new password for the existing user context or the password for a new user account.</span></span> <span data-ttu-id="6bfb7-337">Этот пароль не учитывается для системной учетной записи.</span><span class="sxs-lookup"><span data-stu-id="6bfb7-337">This password is ignored for the system account.</span></span>

</dd> <dt>

<span data-ttu-id="6bfb7-338"><span id="_TR_taskrun"></span><span id="_tr_taskrun"></span><span id="_TR_TASKRUN"></span>**/Tr** </span><span class="sxs-lookup"><span data-stu-id="6bfb7-338"><span id="_TR_taskrun"></span><span id="_tr_taskrun"></span><span id="_TR_TASKRUN"></span>**/TR** **taskrun**</span></span>
</dt> <dd>

<span data-ttu-id="6bfb7-339">Значение типа, указывающее новую программу, которая будет запускаться задачей.</span><span class="sxs-lookup"><span data-stu-id="6bfb7-339">A value that specifies a new program that the task will run.</span></span>

</dd> <dt>

<span data-ttu-id="6bfb7-340"><span id="_ST_starttime"></span><span id="_st_starttime"></span><span id="_ST_STARTTIME"></span>**/St** **StartTime**</span><span class="sxs-lookup"><span data-stu-id="6bfb7-340"><span id="_ST_starttime"></span><span id="_st_starttime"></span><span id="_ST_STARTTIME"></span>**/ST** **starttime**</span></span>
</dt> <dd>

<span data-ttu-id="6bfb7-341">Значение, указывающее время начала выполнения задачи.</span><span class="sxs-lookup"><span data-stu-id="6bfb7-341">A value that specifies the start time to run the task.</span></span> <span data-ttu-id="6bfb7-342">Формат времени — ЧЧ: мм (24-часовое время).</span><span class="sxs-lookup"><span data-stu-id="6bfb7-342">The time format is HH:mm (24-hour time).</span></span> <span data-ttu-id="6bfb7-343">Например, 14:30 указывает 2:30.</span><span class="sxs-lookup"><span data-stu-id="6bfb7-343">For example, 14:30 specifies 2:30PM.</span></span>

<span data-ttu-id="6bfb7-344">**Windows XP и Windows Server 2003:** Этот параметр недоступен.</span><span class="sxs-lookup"><span data-stu-id="6bfb7-344">**Windows XP and Windows Server 2003:** This option is not available.</span></span>

</dd> <dt>

<span data-ttu-id="6bfb7-345"><span id="_RI_interval"></span><span id="_ri_interval"></span><span id="_RI_INTERVAL"></span>**/RI** **интервал**</span><span class="sxs-lookup"><span data-stu-id="6bfb7-345"><span id="_RI_interval"></span><span id="_ri_interval"></span><span id="_RI_INTERVAL"></span>**/RI** **interval**</span></span>
</dt> <dd>

<span data-ttu-id="6bfb7-346">Значение, указывающее интервал повторения в минутах.</span><span class="sxs-lookup"><span data-stu-id="6bfb7-346">A value that specifies the repetition interval, in minutes.</span></span> <span data-ttu-id="6bfb7-347">Допустимый диапазон — 1-599940 минут.</span><span class="sxs-lookup"><span data-stu-id="6bfb7-347">The valid range is 1 - 599940 minutes.</span></span>

<span data-ttu-id="6bfb7-348">**Windows XP и Windows Server 2003:** Этот параметр недоступен.</span><span class="sxs-lookup"><span data-stu-id="6bfb7-348">**Windows XP and Windows Server 2003:** This option is not available.</span></span>

</dd> <dt>

<span data-ttu-id="6bfb7-349"><span id="_ET_endtime"></span><span id="_et_endtime"></span><span id="_ET_ENDTIME"></span>Время **окончания** **/et**</span><span class="sxs-lookup"><span data-stu-id="6bfb7-349"><span id="_ET_endtime"></span><span id="_et_endtime"></span><span id="_ET_ENDTIME"></span>**/ET** **endtime**</span></span>
</dt> <dd>

<span data-ttu-id="6bfb7-350">Значение типа, указывающее время окончания задачи.</span><span class="sxs-lookup"><span data-stu-id="6bfb7-350">A value that specifies the end time for the task.</span></span> <span data-ttu-id="6bfb7-351">Формат времени — ЧЧ: мм (24-часовое время).</span><span class="sxs-lookup"><span data-stu-id="6bfb7-351">The time format is HH:mm (24-hour time).</span></span> <span data-ttu-id="6bfb7-352">Например, 14:50 указывает 2:50PM.</span><span class="sxs-lookup"><span data-stu-id="6bfb7-352">For example, 14:50 specifies 2:50PM.</span></span>

<span data-ttu-id="6bfb7-353">**Windows XP и Windows Server 2003:** Этот параметр недоступен.</span><span class="sxs-lookup"><span data-stu-id="6bfb7-353">**Windows XP and Windows Server 2003:** This option is not available.</span></span>

</dd> <dt>

<span data-ttu-id="6bfb7-354"><span id="_DU_duration"></span><span id="_du_duration"></span><span id="_DU_DURATION"></span>**/Du** **Длительность**</span><span class="sxs-lookup"><span data-stu-id="6bfb7-354"><span id="_DU_duration"></span><span id="_du_duration"></span><span id="_DU_DURATION"></span>**/DU** **duration**</span></span>
</dt> <dd>

<span data-ttu-id="6bfb7-355">Значение типа, указывающее длительность выполнения задачи.</span><span class="sxs-lookup"><span data-stu-id="6bfb7-355">A value that specifies the duration to run the task.</span></span> <span data-ttu-id="6bfb7-356">Формат времени — ЧЧ: мм (24-часовое время).</span><span class="sxs-lookup"><span data-stu-id="6bfb7-356">The time format is HH:mm (24-hour time).</span></span> <span data-ttu-id="6bfb7-357">Например, 14:50 указывает 2:50PM.</span><span class="sxs-lookup"><span data-stu-id="6bfb7-357">For example, 14:50 specifies 2:50PM.</span></span> <span data-ttu-id="6bfb7-358">Это неприменимо к параметру/ET.</span><span class="sxs-lookup"><span data-stu-id="6bfb7-358">This is not applicable with the /ET parameter.</span></span>

<span data-ttu-id="6bfb7-359">**Windows XP и Windows Server 2003:** Этот параметр недоступен.</span><span class="sxs-lookup"><span data-stu-id="6bfb7-359">**Windows XP and Windows Server 2003:** This option is not available.</span></span>

</dd> <dt>

<span data-ttu-id="6bfb7-360"><span id="_K_"></span><span id="_k_"></span>**/K**</span><span class="sxs-lookup"><span data-stu-id="6bfb7-360"><span id="_K_"></span><span id="_k_"></span>**/K**</span></span> 
</dt> <dd>

<span data-ttu-id="6bfb7-361">Значение, которое прерывает задачу по времени окончания или длительности.</span><span class="sxs-lookup"><span data-stu-id="6bfb7-361">A value that terminates the task at the end time or duration time.</span></span>

<span data-ttu-id="6bfb7-362">**Windows XP и Windows Server 2003:** Этот параметр недоступен.</span><span class="sxs-lookup"><span data-stu-id="6bfb7-362">**Windows XP and Windows Server 2003:** This option is not available.</span></span>

</dd> <dt>

<span data-ttu-id="6bfb7-363"><span id="_SD_startdate"></span><span id="_sd_startdate"></span><span id="_SD_STARTDATE"></span>**/SD** **Дата** начала</span><span class="sxs-lookup"><span data-stu-id="6bfb7-363"><span id="_SD_startdate"></span><span id="_sd_startdate"></span><span id="_SD_STARTDATE"></span>**/SD** **startdate**</span></span>
</dt> <dd>

<span data-ttu-id="6bfb7-364">Значение, указывающее первую дату выполнения задачи.</span><span class="sxs-lookup"><span data-stu-id="6bfb7-364">A value that specifies the first date on which to run the task.</span></span> <span data-ttu-id="6bfb7-365">Формат: мм/дд/гггг.</span><span class="sxs-lookup"><span data-stu-id="6bfb7-365">The format is mm/dd/yyyy.</span></span>

<span data-ttu-id="6bfb7-366">**Windows XP и Windows Server 2003:** Этот параметр недоступен.</span><span class="sxs-lookup"><span data-stu-id="6bfb7-366">**Windows XP and Windows Server 2003:** This option is not available.</span></span>

</dd> <dt>

<span data-ttu-id="6bfb7-367"><span id="_ED_enddate"></span><span id="_ed_enddate"></span><span id="_ED_ENDDATE"></span>**/ED** **Дата окончания**</span><span class="sxs-lookup"><span data-stu-id="6bfb7-367"><span id="_ED_enddate"></span><span id="_ed_enddate"></span><span id="_ED_ENDDATE"></span>**/ED** **enddate**</span></span>
</dt> <dd>

<span data-ttu-id="6bfb7-368">Значение, указывающее последнюю дату запуска задачи.</span><span class="sxs-lookup"><span data-stu-id="6bfb7-368">A value that specifies the last date that the task will run.</span></span> <span data-ttu-id="6bfb7-369">Формат: мм/дд/гггг.</span><span class="sxs-lookup"><span data-stu-id="6bfb7-369">The format is mm/dd/yyyy.</span></span>

<span data-ttu-id="6bfb7-370">**Windows XP и Windows Server 2003:** Этот параметр недоступен.</span><span class="sxs-lookup"><span data-stu-id="6bfb7-370">**Windows XP and Windows Server 2003:** This option is not available.</span></span>

</dd> <dt>

<span data-ttu-id="6bfb7-371"><span id="_IT_"></span><span id="_it_"></span>**Разрешает**</span><span class="sxs-lookup"><span data-stu-id="6bfb7-371"><span id="_IT_"></span><span id="_it_"></span>**/IT**</span></span> 
</dt> <dd>

<span data-ttu-id="6bfb7-372">Значение, которое позволяет выполнять задачу в интерактивном режиме только в том случае, если пользователь/RU вошел в систему в момент запуска задачи.</span><span class="sxs-lookup"><span data-stu-id="6bfb7-372">A value that enables the task to run interactively only if the /RU user is currently logged on at the time the task runs.</span></span> <span data-ttu-id="6bfb7-373">Задача выполняется только в том случае, если пользователь вошел в систему.</span><span class="sxs-lookup"><span data-stu-id="6bfb7-373">The task runs only if the user is logged on.</span></span>

<span data-ttu-id="6bfb7-374">**Windows XP и Windows Server 2003:** Этот параметр недоступен.</span><span class="sxs-lookup"><span data-stu-id="6bfb7-374">**Windows XP and Windows Server 2003:** This option is not available.</span></span>

</dd> <dt>

<span data-ttu-id="6bfb7-375"><span id="_RL_level"></span><span id="_rl_level"></span><span id="_RL_LEVEL"></span> **Уровень** /РЛ</span><span class="sxs-lookup"><span data-stu-id="6bfb7-375"><span id="_RL_level"></span><span id="_rl_level"></span><span id="_RL_LEVEL"></span>**/RL** **level**</span></span>
</dt> <dd>

<span data-ttu-id="6bfb7-376">Значение, устанавливающее уровень выполнения для задачи.</span><span class="sxs-lookup"><span data-stu-id="6bfb7-376">A value that sets the run level for the task.</span></span> <span data-ttu-id="6bfb7-377">Допустимые значения: LIMITED и максимальная.</span><span class="sxs-lookup"><span data-stu-id="6bfb7-377">Valid values are LIMITED and HIGHEST.</span></span>

<span data-ttu-id="6bfb7-378">**Windows XP и Windows Server 2003:** Этот параметр недоступен.</span><span class="sxs-lookup"><span data-stu-id="6bfb7-378">**Windows XP and Windows Server 2003:** This option is not available.</span></span>

</dd> <dt>

<span data-ttu-id="6bfb7-379"><span id="_ENABLE_"></span><span id="_enable_"></span>**Разрешение**</span><span class="sxs-lookup"><span data-stu-id="6bfb7-379"><span id="_ENABLE_"></span><span id="_enable_"></span>**/ENABLE**</span></span> 
</dt> <dd>

<span data-ttu-id="6bfb7-380">Значение, включающее запланированную задачу.</span><span class="sxs-lookup"><span data-stu-id="6bfb7-380">A value that enables the scheduled task.</span></span> <span data-ttu-id="6bfb7-381">Разрешенная задача может быть запущена, а отключенная задача не может быть запущена.</span><span class="sxs-lookup"><span data-stu-id="6bfb7-381">An enabled task can run, and a disabled task cannot run.</span></span>

<span data-ttu-id="6bfb7-382">**Windows XP и Windows Server 2003:** Этот параметр недоступен.</span><span class="sxs-lookup"><span data-stu-id="6bfb7-382">**Windows XP and Windows Server 2003:** This option is not available.</span></span>

</dd> <dt>

<span data-ttu-id="6bfb7-383"><span id="_DISABLE_"></span><span id="_disable_"></span>**/DISABLE**</span><span class="sxs-lookup"><span data-stu-id="6bfb7-383"><span id="_DISABLE_"></span><span id="_disable_"></span>**/DISABLE**</span></span> 
</dt> <dd>

<span data-ttu-id="6bfb7-384">Значение, которое отключает выполнение запланированной задачи.</span><span class="sxs-lookup"><span data-stu-id="6bfb7-384">A value that disables the scheduled task from running.</span></span>

> [!Note]  
> <span data-ttu-id="6bfb7-385">Если удаленная задача планировщик задач 1,0 отключена Schtasks.exe и на удаленном компьютере включено исключение брандмауэра для общего доступа к файлам и принтерам, а исключение брандмауэра управления удаленными задачами отключено, задача не будет отключена при чтении из API-интерфейса планировщик задач 2,0.</span><span class="sxs-lookup"><span data-stu-id="6bfb7-385">If a remote Task Scheduler 1.0 task is disabled by Schtasks.exe and the remote computer has the File and Printer Sharing firewall exception enabled and the Remote Scheduled Tasks Management firewall exception disabled, then the task will not be disabled when read from a Task Scheduler 2.0 API.</span></span>

 

<span data-ttu-id="6bfb7-386">**Windows XP и Windows Server 2003:** Этот параметр недоступен.</span><span class="sxs-lookup"><span data-stu-id="6bfb7-386">**Windows XP and Windows Server 2003:** This option is not available.</span></span>

</dd> <dt>

<span data-ttu-id="6bfb7-387"><span id="_Z_"></span><span id="_z_"></span>**/Z**</span><span class="sxs-lookup"><span data-stu-id="6bfb7-387"><span id="_Z_"></span><span id="_z_"></span>**/Z**</span></span> 
</dt> <dd>

<span data-ttu-id="6bfb7-388">Значение, которое помечает задачу, которая должна быть удалена после ее последнего запуска.</span><span class="sxs-lookup"><span data-stu-id="6bfb7-388">A value that marks the task to be deleted after its final run.</span></span>

<span data-ttu-id="6bfb7-389">**Windows XP и Windows Server 2003:** Этот параметр недоступен.</span><span class="sxs-lookup"><span data-stu-id="6bfb7-389">**Windows XP and Windows Server 2003:** This option is not available.</span></span>

</dd> <dt>

<span data-ttu-id="6bfb7-390"><span id="_DELAY_delaytime"></span><span id="_delay_delaytime"></span><span id="_DELAY_DELAYTIME"></span>**/Delay** **DelayTime**</span><span class="sxs-lookup"><span data-stu-id="6bfb7-390"><span id="_DELAY_delaytime"></span><span id="_delay_delaytime"></span><span id="_DELAY_DELAYTIME"></span>**/DELAY** **delaytime**</span></span>
</dt> <dd>

<span data-ttu-id="6bfb7-391">Значение, указывающее время ожидания выполнения задачи после срабатывания триггера.</span><span class="sxs-lookup"><span data-stu-id="6bfb7-391">A value that specifies the wait time to delay the running of the task after the trigger is fired.</span></span> <span data-ttu-id="6bfb7-392">Формат времени — мммм: СС.</span><span class="sxs-lookup"><span data-stu-id="6bfb7-392">The time format is mmmm:ss.</span></span> <span data-ttu-id="6bfb7-393">Этот параметр допустим только для задач с типами расписания OnStart, OnStart и OnStart.</span><span class="sxs-lookup"><span data-stu-id="6bfb7-393">This option is only valid for tasks with the schedule types ONSTART, ONLOGON, and ONEVENT.</span></span>

<span data-ttu-id="6bfb7-394">**Windows XP и Windows Server 2003:** Этот параметр недоступен.</span><span class="sxs-lookup"><span data-stu-id="6bfb7-394">**Windows XP and Windows Server 2003:** This option is not available.</span></span>

</dd> <dt>

<span data-ttu-id="6bfb7-395"><span id="___"></span>**/?**</span><span class="sxs-lookup"><span data-stu-id="6bfb7-395"><span id="___"></span>**/?**</span></span> 
</dt> <dd>

<span data-ttu-id="6bfb7-396">Значение, которое отображает справочное сообщение для Schtasks.exe.</span><span class="sxs-lookup"><span data-stu-id="6bfb7-396">A value that displays the Help message for Schtasks.exe.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="6bfb7-397">Требования</span><span class="sxs-lookup"><span data-stu-id="6bfb7-397">Requirements</span></span>



| <span data-ttu-id="6bfb7-398">Требование</span><span class="sxs-lookup"><span data-stu-id="6bfb7-398">Requirement</span></span> | <span data-ttu-id="6bfb7-399">Значение</span><span class="sxs-lookup"><span data-stu-id="6bfb7-399">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="6bfb7-400">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="6bfb7-400">Minimum supported client</span></span><br/> | <span data-ttu-id="6bfb7-401">Только для \[ классических приложений Windows XP\]</span><span class="sxs-lookup"><span data-stu-id="6bfb7-401">Windows XP \[desktop apps only\]</span></span><br/>          |
| <span data-ttu-id="6bfb7-402">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="6bfb7-402">Minimum supported server</span></span><br/> | <span data-ttu-id="6bfb7-403">\[Только для настольных приложений Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="6bfb7-403">Windows Server 2003 \[desktop apps only\]</span></span><br/> |



 

 





