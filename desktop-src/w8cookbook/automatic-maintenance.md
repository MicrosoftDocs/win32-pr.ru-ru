---
title: Автоматическое обслуживание (Cookbook совместимости для Windows)
description: Автоматическое обслуживание
ms.assetid: D3B61105-D118-42A4-8F3D-ED92EFAF597F
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 320625fa0ac8e56368396a7f1be88def0ac3c526
ms.sourcegitcommit: ea4baf9953a78d2d6bd530b680601e39f3884541
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/01/2020
ms.locfileid: "104488413"
---
# <a name="automatic-maintenance"></a><span data-ttu-id="0cb3d-103">Автоматическое обслуживание</span><span class="sxs-lookup"><span data-stu-id="0cb3d-103">Automatic Maintenance</span></span>

## <a name="platforms"></a><span data-ttu-id="0cb3d-104">Платформы</span><span class="sxs-lookup"><span data-stu-id="0cb3d-104">Platforms</span></span>

<span data-ttu-id="0cb3d-105">**Клиенты** — Windows 8</span><span class="sxs-lookup"><span data-stu-id="0cb3d-105">**Clients** – Windows 8</span></span>  
<span data-ttu-id="0cb3d-106">**Серверы** — Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="0cb3d-106">**Servers** – Windows Server 2012</span></span>  


## <a name="description"></a><span data-ttu-id="0cb3d-107">Описание</span><span class="sxs-lookup"><span data-stu-id="0cb3d-107">Description</span></span>

<span data-ttu-id="0cb3d-108">Windows зависит от выполнения действий "Входящие" и "обслуживание третьими лицами" для большей части его значений, включая Центр обновления Windows и автоматическое дефрагментацию диска, а также антивирусные обновления и проверки.</span><span class="sxs-lookup"><span data-stu-id="0cb3d-108">Windows depends on execution of inbox and third party maintenance activity for much of its value-add, including Windows Update, and automatic disk defragmentation, as well as antivirus updates and scans.</span></span> <span data-ttu-id="0cb3d-109">Кроме того, предприятия часто используют действия по обслуживанию, такие как сканирование защиты доступа к сети (NAP), для обеспечения стандартов безопасности на всех рабочих станциях предприятия.</span><span class="sxs-lookup"><span data-stu-id="0cb3d-109">Additionally, enterprises frequently use maintenance activity such as Network Access Protection (NAP) scanning to help enforce security standards on all enterprise workstations.</span></span>

<span data-ttu-id="0cb3d-110">Деятельность по обслуживанию в Windows предназначена для работы в фоновом режиме с ограниченным участием пользователя и минимальным влиянием на производительность и энергопотребление.</span><span class="sxs-lookup"><span data-stu-id="0cb3d-110">Maintenance activity in Windows is designed to run in the background with limited user interaction and minimal impact to performance and energy efficiency.</span></span> <span data-ttu-id="0cb3d-111">Однако в Windows 7 и более ранних версиях производительность и энергопотребление по-прежнему затронуты из-за недетерминированного и широкого разнообразия расписания нескольких действий по обслуживанию в Windows.</span><span class="sxs-lookup"><span data-stu-id="0cb3d-111">However, in Windows 7 and earlier versions, performance and energy efficiency are still impacted due to the non-deterministic and widely varied schedule of the multiple maintenance activities in Windows.</span></span> <span data-ttu-id="0cb3d-112">Скорость реагирования на пользователей уменьшается при выполнении действия обслуживания, когда пользователи активно используют компьютер.</span><span class="sxs-lookup"><span data-stu-id="0cb3d-112">Responsiveness to users is reduced when maintenance activity runs while users are actively using the computer.</span></span> <span data-ttu-id="0cb3d-113">Кроме того, приложения часто запрашивают у пользователя обновление программного обеспечения и запускают фоновое обслуживание, а также направляют пользователей в несколько функций, включая центр поддержки, панель управления, Центр обновления Windows, планировщик задач оснастку MMC и сторонние элементы управления.</span><span class="sxs-lookup"><span data-stu-id="0cb3d-113">Apps also frequently ask the user to update their software and run background maintenance, and direct users to multiple experiences, including Action Center, Control Panel, Windows Update, Task Scheduler MMC snap-in, and third-party controls.</span></span>

<span data-ttu-id="0cb3d-114">Цель автоматического обслуживания состоит в том, чтобы объединить все операции фонового обслуживания в Windows и помочь сторонним разработчикам добавить свои действия по обслуживанию в Windows без негативного влияния на производительность и эффективность энергопотребления.</span><span class="sxs-lookup"><span data-stu-id="0cb3d-114">The goal of Automatic Maintenance is to combine all background maintenance activity in Windows and help third-party developers add their maintenance activity to Windows without negatively impacting performance and energy efficiency.</span></span> <span data-ttu-id="0cb3d-115">Кроме того, автоматическое обслуживание позволяет пользователям и предприятиям управлять планированием и настройкой действий по обслуживанию.</span><span class="sxs-lookup"><span data-stu-id="0cb3d-115">Additionally, Automatic Maintenance enables users as well as enterprises to be in control of maintenance activity scheduling and configuration.</span></span>

<span data-ttu-id="0cb3d-116">**Основные проблемы**</span><span class="sxs-lookup"><span data-stu-id="0cb3d-116">**Key problems**</span></span>

<span data-ttu-id="0cb3d-117">Автоматическое обслуживание предназначено для решения этих проблем с действиями обслуживания в Windows:</span><span class="sxs-lookup"><span data-stu-id="0cb3d-117">Automatic Maintenance is designed to address these problems with maintenance activity in Windows:</span></span>

-   <span data-ttu-id="0cb3d-118">Расписание крайнего срока</span><span class="sxs-lookup"><span data-stu-id="0cb3d-118">Deadline scheduling</span></span>
-   <span data-ttu-id="0cb3d-119">Конфликты использования ресурсов</span><span class="sxs-lookup"><span data-stu-id="0cb3d-119">Resource utilization conflicts</span></span>
-   <span data-ttu-id="0cb3d-120">Эффективность энергопотребления</span><span class="sxs-lookup"><span data-stu-id="0cb3d-120">Energy efficiency</span></span>
-   <span data-ttu-id="0cb3d-121">Прозрачность для пользователя</span><span class="sxs-lookup"><span data-stu-id="0cb3d-121">Transparency to the user</span></span>

## <a name="functionality"></a><span data-ttu-id="0cb3d-122">Функциональность</span><span class="sxs-lookup"><span data-stu-id="0cb3d-122">Functionality</span></span>

<span data-ttu-id="0cb3d-123">Автоматическое обслуживание способствует повышению эффективности простоя и позволяет выполнять все действия своевременно и по расстановке приоритетов.</span><span class="sxs-lookup"><span data-stu-id="0cb3d-123">Automatic Maintenance facilitates idle efficiency and permits all activity to run in a timely and prioritized fashion.</span></span> <span data-ttu-id="0cb3d-124">Кроме того, он обеспечивает унифицированную видимость и контроль над деятельностью по обслуживанию, а также позволяет сторонним разработчикам добавлять свои действия по обслуживанию в Windows без негативного влияния на производительность и энергопотребление.</span><span class="sxs-lookup"><span data-stu-id="0cb3d-124">It also helps enable unified visibility and control over maintenance activity, and allows third-party developers to add their maintenance activity to Windows without negatively impacting performance and energy efficiency.</span></span> <span data-ttu-id="0cb3d-125">Для этого он предоставляет полностью автоматический режим, автоматический режим, автоматическую приостанавливаться, крайние сроки и уведомления, а также корпоративный контроль.</span><span class="sxs-lookup"><span data-stu-id="0cb3d-125">To do this, it provides a fully automatic mode, user-initiated mode, automatic stop, deadlines and notification, and enterprise control.</span></span> <span data-ttu-id="0cb3d-126">Они описаны ниже.</span><span class="sxs-lookup"><span data-stu-id="0cb3d-126">These are each described below.</span></span>

<span data-ttu-id="0cb3d-127">**Полностью автоматический режим**</span><span class="sxs-lookup"><span data-stu-id="0cb3d-127">**Fully automatic mode**</span></span>

<span data-ttu-id="0cb3d-128">Этот режим по умолчанию обеспечивает интеллектуальное планирование во время простоя ПК и в запланированное время — выполнение и автоматическую приостановку действий по обслуживанию без вмешательства пользователя.</span><span class="sxs-lookup"><span data-stu-id="0cb3d-128">This default mode enables intelligent scheduling during PC idle-time and at scheduled times—the execution and automatic pausing of maintenance activity without any user intervention.</span></span> <span data-ttu-id="0cb3d-129">Пользователь может задать расписание по неделям или по дням.</span><span class="sxs-lookup"><span data-stu-id="0cb3d-129">The user can set a weekly or daily schedule.</span></span> <span data-ttu-id="0cb3d-130">Все действия по обслуживанию являются неинтерактивными и выполняются автоматически.</span><span class="sxs-lookup"><span data-stu-id="0cb3d-130">All maintenance activity is non-interactive and executes silently.</span></span>

<span data-ttu-id="0cb3d-131">Компьютер автоматически возобновляет работу из спящего режима, когда система, скорее всего, не используется, при соблюдении политики управления питанием, которая в случае ноутбуков, по умолчанию разрешает пробуждение только в том случае, если включено питание от сети.</span><span class="sxs-lookup"><span data-stu-id="0cb3d-131">The computer automatically is resumed from sleep when the system is not likely to be in use, respecting the Power Management policy, which in the case of laptops, defaults to allow wake-up only if it is on AC power.</span></span> <span data-ttu-id="0cb3d-132">Все системные ресурсы с высокой степенью энергопотребления используются для выполнения действий по обслуживанию как можно быстрее.</span><span class="sxs-lookup"><span data-stu-id="0cb3d-132">Full system resources at high power are used to complete the maintenance activity as quickly as possible.</span></span> <span data-ttu-id="0cb3d-133">Если система была восстановлена из спящего режима для автоматического обслуживания, она запрашивает возврат в спящий режим.</span><span class="sxs-lookup"><span data-stu-id="0cb3d-133">If the system was resumed from sleep for Automatic Maintenance, it is requested to return to sleep.</span></span>

<span data-ttu-id="0cb3d-134">Все необходимые взаимодействия с пользователем, связанные с действиями, такими как Настройка, выполняются за пределами автоматического обслуживания.</span><span class="sxs-lookup"><span data-stu-id="0cb3d-134">Any required user interactions related to activities such as configuration are performed outside of Automatic Maintenance execution.</span></span>

<span data-ttu-id="0cb3d-135">**Режим, инициированный пользователем**</span><span class="sxs-lookup"><span data-stu-id="0cb3d-135">**User-initiated mode**</span></span>

<span data-ttu-id="0cb3d-136">Если пользователям необходимо подготовиться к командировке, предполагается, что в течение длительного времени заряжается заряд батареи или вы хотите оптимизировать производительность и скорость реагирования, у них есть возможность запуска автоматического обслуживания по требованию.</span><span class="sxs-lookup"><span data-stu-id="0cb3d-136">If users need to prepare for travel, expect to be on battery power for a prolonged time, or wish to optimize for performance and responsiveness, they have the option of initiating Automatic Maintenance on demand.</span></span> <span data-ttu-id="0cb3d-137">Пользователи могут настраивать атрибуты автоматического обслуживания, включая автоматическое расписание выполнения.</span><span class="sxs-lookup"><span data-stu-id="0cb3d-137">Users can configure Automatic Maintenance attributes, including the automatic run schedule.</span></span> <span data-ttu-id="0cb3d-138">Они могут просматривать текущее состояние автоматического выполнения обслуживания, а также могут прекращать автоматическое обслуживание при необходимости.</span><span class="sxs-lookup"><span data-stu-id="0cb3d-138">They can view the current status of Automatic Maintenance execution, and they can stop Automatic Maintenance if needed.</span></span>

<span data-ttu-id="0cb3d-139">**Автоматическая отмена**</span><span class="sxs-lookup"><span data-stu-id="0cb3d-139">**Automatic stop**</span></span>

<span data-ttu-id="0cb3d-140">Автоматическое обслуживание автоматически прекращает выполнение действий по обслуживанию, если пользователь начинает взаимодействовать с компьютером.</span><span class="sxs-lookup"><span data-stu-id="0cb3d-140">Automatic Maintenance automatically stops currently running maintenance activities if the user starts interacting with the computer.</span></span> <span data-ttu-id="0cb3d-141">Действие обслуживания возобновится, когда система вернется в состояние простоя.</span><span class="sxs-lookup"><span data-stu-id="0cb3d-141">Maintenance activity will resume when the system returns to idle status.</span></span>

> [!Note]  
> <span data-ttu-id="0cb3d-142">Все действия в автоматическом обслуживании должны поддерживать остановку в течение 2 секунд или меньше.</span><span class="sxs-lookup"><span data-stu-id="0cb3d-142">All activities in Automatic Maintenance must support stopping in 2 seconds or less.</span></span> <span data-ttu-id="0cb3d-143">Пользователь должен получать уведомления о том, что действие было остановлено.</span><span class="sxs-lookup"><span data-stu-id="0cb3d-143">The user should be notified that the activity has been stopped.</span></span>

 

<span data-ttu-id="0cb3d-144">**Крайние сроки и уведомление**</span><span class="sxs-lookup"><span data-stu-id="0cb3d-144">**Deadlines and notification**</span></span>

<span data-ttu-id="0cb3d-145">Критическое действие обслуживания должно выполняться в заранее определенном временном окне.</span><span class="sxs-lookup"><span data-stu-id="0cb3d-145">Critical maintenance activity must execute within a pre-defined time window.</span></span> <span data-ttu-id="0cb3d-146">Если критические задачи не удалось запустить в течение заданного времени, автоматическое обслуживание начнется автоматически при следующей доступной возможности простоя системы.</span><span class="sxs-lookup"><span data-stu-id="0cb3d-146">If critical tasks have not been able to run within their designated time, Automatic Maintenance will automatically start executing at the next available system idle opportunity.</span></span> <span data-ttu-id="0cb3d-147">Однако если состояние задачи остается за крайний срок, автоматическое обслуживание сообщит пользователю об этом действии и предоставит возможность ручного выполнения автоматического обслуживания.</span><span class="sxs-lookup"><span data-stu-id="0cb3d-147">However, if the task state remains behind deadline, Automatic Maintenance will notify the user about the activity and provide an option for a manual run of Automatic Maintenance.</span></span> <span data-ttu-id="0cb3d-148">Будут выполнены все задачи, запланированные на обслуживание, хотя наиболее несущественное выполнение задач имеет приоритет.</span><span class="sxs-lookup"><span data-stu-id="0cb3d-148">All tasks scheduled for maintenance will run, although the most starved tasks take precedence.</span></span> <span data-ttu-id="0cb3d-149">Это действие может повлиять на скорость реагирования и производительность системы. Таким образом, автоматическое обслуживание будет уведомлять пользователя о том, что выполняется критическое действие обслуживания.</span><span class="sxs-lookup"><span data-stu-id="0cb3d-149">This activity may impact system responsiveness and performance; therefore, Automatic Maintenance will notify the user that critical maintenance activity is executing.</span></span>

<span data-ttu-id="0cb3d-150">**Корпоративный контроль**</span><span class="sxs-lookup"><span data-stu-id="0cb3d-150">**Enterprise control**</span></span>

<span data-ttu-id="0cb3d-151">Специалисты по ИТ должны иметь возможность определить, когда автоматическое обслуживание выполняется в своих системах Windows, применять это расписание через стандартизированные интерфейсы управления и получать данные событий о состоянии попыток автоматического обслуживания.</span><span class="sxs-lookup"><span data-stu-id="0cb3d-151">Enterprise IT professionals should be able to determine when Automatic Maintenance executes on their Windows systems, enforce that schedule via standardized management interfaces, and retrieve event data about the status of Automatic Maintenance execution attempts.</span></span> <span data-ttu-id="0cb3d-152">Кроме того, ИТ-специалисты должны иметь возможность удаленного вызова определенной операции автоматического обслуживания через стандартные интерфейсы управления.</span><span class="sxs-lookup"><span data-stu-id="0cb3d-152">Additionally, IT professionals should be able to invoke specific Automatic Maintenance activity remotely via standard management interfaces.</span></span> <span data-ttu-id="0cb3d-153">При каждом выполнении автоматического обслуживания, отчетов о состоянии, включая уведомления, если автоматическое обслуживание не удалось выполнить, так как пользователь вручную приостановил действие, выполняется.</span><span class="sxs-lookup"><span data-stu-id="0cb3d-153">Each time Automatic Maintenance executes, status reporting, including notifications when Automatic Maintenance could not be executed because the user has manually paused the activity, runs.</span></span> <span data-ttu-id="0cb3d-154">ИТ-специалистам следует рассмотреть возможность перемещения сценариев входа в автоматическое обслуживание, чтобы ускорить процесс входа пользователя.</span><span class="sxs-lookup"><span data-stu-id="0cb3d-154">IT professionals should consider moving logon scripts to Automatic Maintenance to help make the user’s logon experience quicker.</span></span>

## <a name="creating-an-automatic-maintenance-task"></a><span data-ttu-id="0cb3d-155">Создание задачи автоматического обслуживания</span><span class="sxs-lookup"><span data-stu-id="0cb3d-155">Creating an Automatic Maintenance task</span></span>

<span data-ttu-id="0cb3d-156">В этом разделе подробно описано, как разработчики могут создавать задачи с помощью определения задачи в языке XML или C.</span><span class="sxs-lookup"><span data-stu-id="0cb3d-156">This section details how developers can create a task using a task definition in XML or C language.</span></span> <span data-ttu-id="0cb3d-157">Помните, что действие обслуживания не должно запускать пользовательский интерфейс, требующий взаимодействия с пользователем, так как автоматическое обслуживание выполняется полностью без вмешательства пользователя и выполняется, когда пользователь отсутствует.</span><span class="sxs-lookup"><span data-stu-id="0cb3d-157">Keep in mind that maintenance activity should not launch any user interface that requires user interaction, as Automatic Maintenance is completely silent and runs when the user is not present.</span></span> <span data-ttu-id="0cb3d-158">В действительности, если пользователь взаимодействует с компьютером во время автоматического обслуживания, все задачи в процессе будут завершаться до следующего периода простоя.</span><span class="sxs-lookup"><span data-stu-id="0cb3d-158">Indeed, if the user interacts with the computer during Automatic Maintenance, any tasks in process will be ended until the next idle period.</span></span>

<span data-ttu-id="0cb3d-159">**Использование XML**</span><span class="sxs-lookup"><span data-stu-id="0cb3d-159">**Using XML**</span></span>

<span data-ttu-id="0cb3d-160">Планировщик задач включает встроенное средство командной строки schtasks.exe, которое может импортировать определение задачи в формате XML.</span><span class="sxs-lookup"><span data-stu-id="0cb3d-160">Task Scheduler includes a built-in command-line tool, schtasks.exe, that can import a task definition in XML format.</span></span> <span data-ttu-id="0cb3d-161">Схема для определения задачи описана в статье https://msdn.microsoft.com/library/aa383609(v=VS.85).aspx .</span><span class="sxs-lookup"><span data-stu-id="0cb3d-161">The schema for task definition is documented at https://msdn.microsoft.com/library/aa383609(v=VS.85).aspx.</span></span> <span data-ttu-id="0cb3d-162">Ниже приведен пример задачи автоматического обслуживания, определенной в XML.</span><span class="sxs-lookup"><span data-stu-id="0cb3d-162">Below is an example of an Automatic Maintenance task defined in XML.</span></span>


```
<?xml version="1.0" encoding="UTF-16"?>
<Task version="1.4" xmlns="http://schemas.microsoft.com/windows/2004/02/mit/task">
  <RegistrationInfo>
    <Date>2011-07-01T11:34:31</Date>
    <Author>IT Deptartment</Author>
  </RegistrationInfo>
  <Principals>
    <Principal id="Author">
      <RunLevel>LeastPrivilege</RunLevel>
      <GroupId>NT AUTHORITY\SYSTEM</GroupId>
    </Principal>
  </Principals>
  <Settings>
    <MultipleInstancesPolicy>IgnoreNew</MultipleInstancesPolicy>
    <DisallowStartIfOnBatteries>true</DisallowStartIfOnBatteries>
    <StopIfGoingOnBatteries>true</StopIfGoingOnBatteries>
    <AllowHardTerminate>true</AllowHardTerminate>
    <StartWhenAvailable>false</StartWhenAvailable>
    <RunOnlyIfNetworkAvailable>false</RunOnlyIfNetworkAvailable>
    <MaintenanceSettings>
      <Period>P2D</Period>
      <Deadline>P14D</Deadline>
    </MaintenanceSettings>
    <AllowStartOnDemand>true</AllowStartOnDemand>
    <Enabled>true</Enabled>
    <Hidden>false</Hidden>
    <RunOnlyIfIdle>false</RunOnlyIfIdle>
    <DisallowStartOnRemoteAppSession>false</DisallowStartOnRemoteAppSession>
    <UseUnifiedSchedulingEngine>true</UseUnifiedSchedulingEngine>
    <WakeToRun>false</WakeToRun>
    <ExecutionTimeLimit>P3D</ExecutionTimeLimit>
    <Priority>7</Priority>
  </Settings>
  <Actions Context="Author">
    <Exec>
      <Command>cmd</Command>
      <Arguments>/c timeout -t 60</Arguments>
    </Exec>
  </Actions>
</Task> 
```



<span data-ttu-id="0cb3d-163">Чтобы сохранить задачу на компьютере Windows, сохраните приведенный выше XML как текстовый файл и используйте следующую командную строку:</span><span class="sxs-lookup"><span data-stu-id="0cb3d-163">To save the task on a Windows computer, save the above XML as a text file and use this command line:</span></span>

`Schtasks.exe /create /tn <task name> /xml <text file name>`

<span data-ttu-id="0cb3d-164">**Использование C**</span><span class="sxs-lookup"><span data-stu-id="0cb3d-164">**Using C**</span></span>

<span data-ttu-id="0cb3d-165">Задачу автоматического обслуживания также можно создать с помощью кода на языке C.</span><span class="sxs-lookup"><span data-stu-id="0cb3d-165">An Automatic Maintenance task also can be created using C code.</span></span> <span data-ttu-id="0cb3d-166">Ниже приведен пример кода, который можно использовать для настройки параметров автоматического обслуживания задачи.</span><span class="sxs-lookup"><span data-stu-id="0cb3d-166">Below is a code sample that can be used to configure a task’s Automatic Maintenance settings:</span></span>


```
/********************************************************************
This sample creates a maintenance task to start cmd window during maintenance opportunities with periodicity of 2 days and deadline 0f 14 days.
********************************************************************/

#define _WIN32_DCOM

#include <windows.h>
#include <iostream>
#include <stdio.h>
#include <comdef.h>
#include <wincred.h>
//  Include the task header file.
#include <taskschd.h>
//#pragma comment(lib, "taskschd.lib")
//#pragma comment(lib, "comsupp.lib")

int __cdecl 
MainteanceTask( )
{
    //  ------------------------------------------------------
    //  Initialize COM.
    HRESULT hr;

    //  ------------------------------------------------------
    //  Create a name for the task.
    LPCWSTR wszTaskName = L"MaintenanceTask";

    ITaskService *pService = NULL;
    ITaskFolder *pRootFolder = NULL;
    ITaskDefinition *pTask = NULL;
    ITaskSettings *pSettings = NULL;
    IRegistrationInfo *pRegInfo= NULL;
    IPrincipal *pPrincipal = NULL;
    ITaskSettings3 *pSettings3 = NULL;
    IMaintenanceSettings* pMaintenanceSettings = NULL;
    IActionCollection *pActionCollection = NULL;
    IAction *pAction = NULL;
    IExecAction *pExecAction = NULL;
    IRegisteredTask *pRegisteredTask = NULL;

    wprintf(L"\nCreate Maintenance Task %ws", wszTaskName );

    hr = CoInitializeEx( NULL, COINIT_MULTITHREADED);
    if( FAILED(hr) )
    {
        wprintf(L"\nCoInitializeEx failed: %x", hr );
        return 1;
    }

    //  Set general COM security levels.
    hr = CoInitializeSecurity( NULL,
        -1,
        NULL,
        NULL,
        RPC_C_AUTHN_LEVEL_PKT_PRIVACY,
        RPC_C_IMP_LEVEL_IMPERSONATE,
        NULL,
        0,
        NULL);

    if( FAILED(hr) )
    {
        wprintf(L"\nCoInitializeSecurity failed: %x", hr );
        goto CleanUp;
    }

    //  ------------------------------------------------------
    //  Create an instance of the Task Service. 
    hr = CoCreateInstance( CLSID_TaskScheduler,
                           NULL,
                           CLSCTX_INPROC_SERVER,
                           IID_ITaskService,
                           (void**)&pService );  
    if (FAILED(hr))
    {
        wprintf(L"\nFailed to create an instance of ITaskService: %x", hr);
        goto CleanUp;
    }
        
    //  Connect to the task service.
    hr = pService->Connect(_variant_t(), _variant_t(), _variant_t(), _variant_t());
    if( FAILED(hr) )
    {
        wprintf(L"\nITaskService::Connect failed: %x", hr );
        goto CleanUp;
    }

    //  ------------------------------------------------------
    //  Get the pointer to the root task folder.  This folder will hold the
    //  new task that is registered.
    hr = pService->GetFolder( _bstr_t( L"\\") , &pRootFolder );
    if( FAILED(hr) )
    {
        wprintf(L"\nCannot get Root folder pointer: %x", hr );
        goto CleanUp;
    }
    
    //  If the same task exists, remove it.
    ( void ) pRootFolder->DeleteTask( _bstr_t(wszTaskName), 0  );
    
    //  Create the task definition object to create the task.
    hr = pService->NewTask( 0, &pTask );
    if (FAILED(hr))
    {
        wprintf(L"\nFailed to CoCreate an instance of the TaskService class: %x", hr);
        goto CleanUp;
    }
        
    //  ------------------------------------------------------
    //  Get the registration info for setting the identification.
    hr = pTask->get_RegistrationInfo( &pRegInfo );
    if( FAILED(hr) )
    {
        wprintf(L"\nCannot get identification pointer: %x", hr );
        goto CleanUp;
    }
    
    hr = pRegInfo->put_Author( _bstr_t(L"Author Name") );    
    if( FAILED(hr) )
    {
        wprintf(L"\nCannot put identification info: %x", hr );
        goto CleanUp;
    }

    // The task needs to grant explicit FRFX to LOCAL SERVICE (A;;FRFX;;;LS)
    hr = pRegInfo->put_SecurityDescriptor( _variant_t(L"D:P(A;;FA;;;BA)(A;;FA;;;SY)(A;;FRFX;;;LS)") );
    if( FAILED(hr) )
    {
        wprintf(L"\nCannot put security descriptor: %x", hr );
        goto CleanUp;
    }

    //  ------------------------------------------------------
    //  Create the principal for the task - these credentials
    //  are overwritten with the credentials passed to RegisterTaskDefinition
    hr = pTask->get_Principal( &pPrincipal );
    if( FAILED(hr) )
    {
        wprintf(L"\nCannot get principal pointer: %x", hr );
        goto CleanUp;
    }
    
    //  Set up principal logon type to interactive logon
    hr = pPrincipal->put_LogonType( TASK_LOGON_INTERACTIVE_TOKEN );
    if( FAILED(hr) )
    {
        wprintf(L"\nCannot put principal info: %x", hr );
        goto CleanUp;
    }  

    //  ------------------------------------------------------
    //  Create the settings for the task
    hr = pTask->get_Settings( &pSettings );
    if( FAILED(hr) )
    {
        wprintf(L"\nCannot get settings pointer: %x", hr );
        goto CleanUp;
    }

    hr = pSettings->QueryInterface( __uuidof(ITaskSettings3), (void**) &pSettings3 );
    if( FAILED(hr) )
    {
        wprintf(L"\nCannot query ITaskSettings3 interface: %x", hr );
        goto CleanUp;
    }

    hr = pSettings3->put_UseUnifiedSchedulingEngine( VARIANT_TRUE );
    if( FAILED(hr) )
    {
        wprintf(L"\nCannot put_UseUnifiedSchedulingEngine: %x", hr );
        goto CleanUp;
    }

    hr = pSettings3->CreateMaintenanceSettings( &pMaintenanceSettings );
    if( FAILED(hr) )
    {
        wprintf(L"\nCannot CreateMaintenanceSettings: %x", hr );
        goto CleanUp;
    }

    hr = pMaintenanceSettings->put_Period ( _bstr_t(L"P2D") );
    if( FAILED(hr) )
    {
        wprintf(L"\nCannot put_Period: %x", hr );
        goto CleanUp;
    }

    hr = pMaintenanceSettings->put_Deadline ( _bstr_t(L"P14D") );
    if( FAILED(hr) )
    {
        wprintf(L"\nCannot put_Period: %x", hr );
        goto CleanUp;
    }

    //  ------------------------------------------------------
    //  Add an action to the task. This task will execute notepad.exe.     
    //  Get the task action collection pointer.
    hr = pTask->get_Actions( &pActionCollection );
    if( FAILED(hr) )
    {
        wprintf(L"\nCannot get Task collection pointer: %x", hr );
        goto CleanUp;
    }
    
    //  Create the action, specifying that it is an executable action.
    hr = pActionCollection->Create( TASK_ACTION_EXEC, &pAction );
    if( FAILED(hr) )
    {
        wprintf(L"\nCannot create the action: %x", hr );
        goto CleanUp;
    }

    //  QI for the executable task pointer.
    hr = pAction->QueryInterface( IID_IExecAction, (void**) &pExecAction );
    if( FAILED(hr) )
    {
        wprintf(L"\nQueryInterface call failed for IExecAction: %x", hr );
        goto CleanUp;
    }

    //  Set the path of the executable to notepad.exe.
    hr = pExecAction->put_Path( _bstr_t(L"cmd") );
    if( FAILED(hr) )
    {
        wprintf(L"\nCannot put action path: %x", hr );
        goto CleanUp;
    }  
    
    //  ------------------------------------------------------
    //  Save the task in the root folder.
    hr = pRootFolder->RegisterTaskDefinition(
            _bstr_t(wszTaskName),
            pTask,
            TASK_CREATE_OR_UPDATE, 
            _variant_t(), 
            _variant_t(), 
            TASK_LOGON_INTERACTIVE_TOKEN,
            _variant_t(L""),
            &pRegisteredTask);
    if( FAILED(hr) )
    {
        wprintf(L"\nError saving the Task : %x", hr );
        goto CleanUp;
    }
    
    wprintf(L"\nSuccess!\n----------------------------------" );

CleanUp:

    if ( pService != NULL ) pService->Release();
    if ( pRootFolder != NULL ) pRootFolder->Release();
    if ( pTask != NULL ) pTask->Release();
    if ( pSettings != NULL ) pSettings->Release();
    if ( pRegInfo != NULL ) pRegInfo->Release();
    if ( pPrincipal != NULL ) pPrincipal->Release();
    if ( pSettings3 != NULL ) pSettings3->Release();
    if ( pMaintenanceSettings != NULL ) pMaintenanceSettings->Release();
    if ( pActionCollection != NULL ) pActionCollection->Release();
    if ( pAction != NULL ) pAction->Release();
    if ( pExecAction != NULL ) pExecAction->Release();
    if ( pRegisteredTask != NULL ) pRegisteredTask->Release();

    CoUninitialize();
    return SUCCEEDED ( hr ) ? 0 : 1;
}
```



## <a name="validating-tasks"></a><span data-ttu-id="0cb3d-167">Проверка задач</span><span class="sxs-lookup"><span data-stu-id="0cb3d-167">Validating tasks</span></span>

<span data-ttu-id="0cb3d-168">Убедитесь, что задача успешно создана и выполняется как часть обслуживания.</span><span class="sxs-lookup"><span data-stu-id="0cb3d-168">Validate that the task has been created successfully and runs as part of maintenance.</span></span>

<span data-ttu-id="0cb3d-169">**Проверка создания задачи**</span><span class="sxs-lookup"><span data-stu-id="0cb3d-169">**Validating task creation**</span></span>

<span data-ttu-id="0cb3d-170">Используйте эту командную строку, чтобы экспортировать определение задачи в файл и убедиться, что определение задачи должно быть ожидаемым:</span><span class="sxs-lookup"><span data-stu-id="0cb3d-170">Use this command line to export the task definition to a file and ensure that the task definition is as expected:</span></span>

`Schtasks.exe /Query /tn<task name> /xml <text file name>`

<span data-ttu-id="0cb3d-171">**Проверка выполнения задачи**</span><span class="sxs-lookup"><span data-stu-id="0cb3d-171">**Validating task execution**</span></span>

<span data-ttu-id="0cb3d-172">Запустите эту командную строку, чтобы запустить задачу и проверить, что планировщик задач пользовательский интерфейс (тасксчд. msc) показывает, что задача выполнена:</span><span class="sxs-lookup"><span data-stu-id="0cb3d-172">Run this command line to launch the task and validate that the Task Scheduler UI (taskschd.msc) shows the task has run:</span></span>

`Schtasks.exe /Run /tn<task name>`

## <a name="resources"></a><span data-ttu-id="0cb3d-173">Ресурсы</span><span class="sxs-lookup"><span data-stu-id="0cb3d-173">Resources</span></span>

-   <span data-ttu-id="0cb3d-174">[Расписание задач 2,0](/previous-versions/bb756979(v=msdn.10))</span><span class="sxs-lookup"><span data-stu-id="0cb3d-174">[Task Schedule 2.0](/previous-versions/bb756979(v=msdn.10))</span></span>

 

 