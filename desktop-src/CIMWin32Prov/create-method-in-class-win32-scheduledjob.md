---
description: Отправляет задание в операционную систему для выполнения в указанное время и дату в будущем.
ms.assetid: 9d582fbb-24cb-401d-8b77-af7671a24e6d
ms.tgt_platform: multiple
title: Метод Create класса Win32_ScheduledJob
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_ScheduledJob.Create
api_type:
- COM
api_location:
- CIMWin32.dll
ms.openlocfilehash: 9f1acae94ea29d2d57b2952c0b0adc267ad3066c
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104342352"
---
# <a name="create-method-of-the-win32_scheduledjob-class"></a><span data-ttu-id="b629e-103">Метод Create \_ класса Win32 ScheduledJob</span><span class="sxs-lookup"><span data-stu-id="b629e-103">Create method of the Win32\_ScheduledJob class</span></span>

<span data-ttu-id="b629e-104">Метод **создания** [класса WMI](/windows/desktop/WmiSdk/retrieving-a-class) отправляет задание в операционную систему для выполнения в указанное время и дату в будущем.</span><span class="sxs-lookup"><span data-stu-id="b629e-104">The **Create** [WMI class](/windows/desktop/WmiSdk/retrieving-a-class) method submits a job to an operating system for execution at a specified time and date in the future.</span></span> <span data-ttu-id="b629e-105">Для этого метода требуется, чтобы служба расписаний была запущена на компьютере, на который отправляется задание.</span><span class="sxs-lookup"><span data-stu-id="b629e-105">This method requires that the schedule service be started on the computer to which the job is submitted.</span></span>

<span data-ttu-id="b629e-106">В этом разделе используется синтаксис MOF-файл (MOF).</span><span class="sxs-lookup"><span data-stu-id="b629e-106">This topic uses Managed Object Format (MOF) syntax.</span></span> <span data-ttu-id="b629e-107">Дополнительные сведения об использовании этого метода см. [в разделе вызов метода](/windows/desktop/WmiSdk/calling-a-method).</span><span class="sxs-lookup"><span data-stu-id="b629e-107">For more information about using this method, see [Calling a Method](/windows/desktop/WmiSdk/calling-a-method).</span></span>

## <a name="syntax"></a><span data-ttu-id="b629e-108">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="b629e-108">Syntax</span></span>


```mof
uint32 Create(
  [in]           string   Command,
  [in]           datetime StartTime,
  [in, optional] boolean  RunRepeatedly,
  [in, optional] uint32   DaysOfWeek,
  [in, optional] uint32   DaysOfMonth,
  [in, optional] boolean  InteractWithDesktop,
  [out]          uint32   JobId
);
```



## <a name="parameters"></a><span data-ttu-id="b629e-109">Параметры</span><span class="sxs-lookup"><span data-stu-id="b629e-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="b629e-110">*Команда* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="b629e-110">*Command* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="b629e-111">Имя команды, пакетной программы или двоичного файла и параметры командной строки, которые служба расписания использует для вызова задания.</span><span class="sxs-lookup"><span data-stu-id="b629e-111">Name of the command, batch program, or binary file and command-line parameters that the schedule service uses to invoke the job.</span></span>

<span data-ttu-id="b629e-112">Пример: "Defrag/q/f".</span><span class="sxs-lookup"><span data-stu-id="b629e-112">Example: "defrag /q /f".</span></span>

</dd> <dt>

<span data-ttu-id="b629e-113">Время *начала* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="b629e-113">*StartTime* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="b629e-114">Время в формате UTC для выполнения задания.</span><span class="sxs-lookup"><span data-stu-id="b629e-114">Coordinated Universal Time (UTC) time to run a job.</span></span> <span data-ttu-id="b629e-115">Форма должна иметь вид "YYYYMMDDHHMMSS. ММММММ (+-) OOO ", где" ГГГГММДД "должен быть заменен на" \* \* \* \* \* \* \* \* ".</span><span class="sxs-lookup"><span data-stu-id="b629e-115">The form must be: "YYYYMMDDHHMMSS.MMMMMM(+-)OOO", where "YYYYMMDD" must be replaced by "\*\*\*\*\*\*\*\*".</span></span> <span data-ttu-id="b629e-116">Например: " \* \* \* \* \* \* \* \* 143000.000000-420" указывает 14,30 (2:30 вечера) PST, в котором действует летнее время.</span><span class="sxs-lookup"><span data-stu-id="b629e-116">For example: "\*\*\*\*\*\*\*\*143000.000000-420" specifies 14.30 (2:30 P.M.) PST with daylight savings time in effect.</span></span>

<span data-ttu-id="b629e-117">Раздел "(+-) OOO" в значении свойства StartTime является текущим смещением для локального преобразования времени.</span><span class="sxs-lookup"><span data-stu-id="b629e-117">The "(+-)OOO" section of the StartTime property value is the current bias for local time translation.</span></span> <span data-ttu-id="b629e-118">Смещение — это разница между временем в формате UTC и местным временем.</span><span class="sxs-lookup"><span data-stu-id="b629e-118">The bias is the difference between the UTC time and the local time.</span></span> <span data-ttu-id="b629e-119">Чтобы вычислить смещение для часового пояса, умножьте число часов, в течение которых часовой пояс составляет вперед или выше среднего времени по Гринвичу (GMT) на 60 (Используйте положительное число в часах, если часовой пояс находится впереди GMT и отрицательное число, если часовой пояс находится за GMT).</span><span class="sxs-lookup"><span data-stu-id="b629e-119">To calculate the bias for your time zone, multiply the number of hours that your time zone is ahead or behind Greenwich Mean Time (GMT) by 60 (use a positive number for the number of hours if your time zone is ahead of GMT and a negative number if your time zone is behind GMT).</span></span> <span data-ttu-id="b629e-120">Добавьте дополнительные 60 к вычислению, если часовой пояс использует летнее время.</span><span class="sxs-lookup"><span data-stu-id="b629e-120">Add an additional 60 to your calculation if your time zone is using daylight savings time.</span></span> <span data-ttu-id="b629e-121">Например, тихоокеанское стандартное часовое пояса составляет восемь часов после GMT, поэтому он равен-420 (-8 \* 60 + 60) при использовании летнего времени и-480 (-8 \* 60), если летнее время не используется.</span><span class="sxs-lookup"><span data-stu-id="b629e-121">For example, the Pacific Standard Time zone is eight hours behind GMT, therefore the bias is equals to -420 (-8 \* 60 + 60) when daylight savings time is in use and -480 (-8 \* 60) when daylight savings time is not in use.</span></span> <span data-ttu-id="b629e-122">Можно также определить значение смещения, запросив свойство смещения класса [**\_ часового пояса Win32**](win32-timezone.md) .</span><span class="sxs-lookup"><span data-stu-id="b629e-122">You can also determine the value of the bias by querying the bias property of the [**Win32\_TimeZone**](win32-timezone.md) class.</span></span>

</dd> <dt>

<span data-ttu-id="b629e-123">*Рунрепеатедли* \[ в необязательное\]</span><span class="sxs-lookup"><span data-stu-id="b629e-123">*RunRepeatedly* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="b629e-124">Если задано **значение true**, запланированное задание выполняется многократно в определенные дни.</span><span class="sxs-lookup"><span data-stu-id="b629e-124">If **True**, a scheduled job runs repeatedly on specific days.</span></span> <span data-ttu-id="b629e-125">По умолчанию **False**.</span><span class="sxs-lookup"><span data-stu-id="b629e-125">The default is **False**.</span></span>

</dd> <dt>

<span data-ttu-id="b629e-126">*DaysOfWeek* \[ в необязательное\]</span><span class="sxs-lookup"><span data-stu-id="b629e-126">*DaysOfWeek* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="b629e-127">Дни недели, в которые запланировано выполнение задания; используется только в том случае, если параметр *рунрепеатедли* имеет **значение true**.</span><span class="sxs-lookup"><span data-stu-id="b629e-127">Days of the week when a job is scheduled to run; used only when the *RunRepeatedly* parameter is **True**.</span></span> <span data-ttu-id="b629e-128">Чтобы запланировать задание более чем на один день недели, присоедините соответствующие значения в логическом или.</span><span class="sxs-lookup"><span data-stu-id="b629e-128">To schedule a job for more than one day of the week, join the appropriate values in a logical OR.</span></span> <span data-ttu-id="b629e-129">Например, чтобы запланировать задание для вторники и пятницу, значение *DaysOfWeek* равно 2 или 16.</span><span class="sxs-lookup"><span data-stu-id="b629e-129">For example, to schedule a job for Tuesdays and Fridays, the value of *DaysOfWeek* are 2 OR 16.</span></span>

<dt>

<span id="Monday"></span><span id="monday"></span><span id="MONDAY"></span>

<span data-ttu-id="b629e-130">**Понедельник** (1)</span><span class="sxs-lookup"><span data-stu-id="b629e-130">**Monday** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Tuesday"></span><span id="tuesday"></span><span id="TUESDAY"></span>

<span data-ttu-id="b629e-131">**Вторник** (2)</span><span class="sxs-lookup"><span data-stu-id="b629e-131">**Tuesday** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Wednesday"></span><span id="wednesday"></span><span id="WEDNESDAY"></span>

<span data-ttu-id="b629e-132">**Среда** (4)</span><span class="sxs-lookup"><span data-stu-id="b629e-132">**Wednesday** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="Thursday"></span><span id="thursday"></span><span id="THURSDAY"></span>

<span data-ttu-id="b629e-133">**Четверг** (8)</span><span class="sxs-lookup"><span data-stu-id="b629e-133">**Thursday** (8)</span></span>


</dt> <dd></dd> <dt>

<span id="Friday"></span><span id="friday"></span><span id="FRIDAY"></span>

<span data-ttu-id="b629e-134">**Пятница** (16)</span><span class="sxs-lookup"><span data-stu-id="b629e-134">**Friday** (16)</span></span>


</dt> <dd></dd> <dt>

<span id="Saturday"></span><span id="saturday"></span><span id="SATURDAY"></span>

<span data-ttu-id="b629e-135">**Суббота** (32)</span><span class="sxs-lookup"><span data-stu-id="b629e-135">**Saturday** (32)</span></span>


</dt> <dd></dd> <dt>

<span id="Sunday"></span><span id="sunday"></span><span id="SUNDAY"></span>

<span data-ttu-id="b629e-136">**Воскресенье** (64)</span><span class="sxs-lookup"><span data-stu-id="b629e-136">**Sunday** (64)</span></span>


</dt> <dd></dd> </dl> </dd> <dt>

<span data-ttu-id="b629e-137">*DaysOfMonth* \[ в необязательное\]</span><span class="sxs-lookup"><span data-stu-id="b629e-137">*DaysOfMonth* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="b629e-138">Дни месяца, когда запланировано выполнение задания; используется только в том случае, если параметр *рунрепеатедли* имеет **значение true**.</span><span class="sxs-lookup"><span data-stu-id="b629e-138">Days of the month when a job is scheduled to run; used only when the *RunRepeatedly* parameter is **True**.</span></span>

<dt>

<span id="1"></span>

<span data-ttu-id="b629e-139"><span id="1"></span>**1** (1)</span><span class="sxs-lookup"><span data-stu-id="b629e-139"><span id="1"></span>**1** (1)</span></span>


</dt> <dd>

<span data-ttu-id="b629e-140">День 1 месяца</span><span class="sxs-lookup"><span data-stu-id="b629e-140">Day 1 of a month</span></span>

</dd> <dt>

<span id="2"></span>

<span data-ttu-id="b629e-141"><span id="2"></span>**2** (2)</span><span class="sxs-lookup"><span data-stu-id="b629e-141"><span id="2"></span>**2** (2)</span></span>


</dt> <dd>

<span data-ttu-id="b629e-142">День 2 месяца</span><span class="sxs-lookup"><span data-stu-id="b629e-142">Day 2 of a month</span></span>

</dd> <dt>

<span id="3"></span>

<span data-ttu-id="b629e-143"><span id="3"></span>**3** (4)</span><span class="sxs-lookup"><span data-stu-id="b629e-143"><span id="3"></span>**3** (4)</span></span>


</dt> <dd>

<span data-ttu-id="b629e-144">День 3 месяца</span><span class="sxs-lookup"><span data-stu-id="b629e-144">Day 3 of a month</span></span>

</dd> <dt>

<span id="4"></span>

<span data-ttu-id="b629e-145"><span id="4"></span>**4** (8)</span><span class="sxs-lookup"><span data-stu-id="b629e-145"><span id="4"></span>**4** (8)</span></span>


</dt> <dd>

<span data-ttu-id="b629e-146">День 4 месяца</span><span class="sxs-lookup"><span data-stu-id="b629e-146">Day 4 of a month</span></span>

</dd> <dt>

<span id="5"></span>

<span data-ttu-id="b629e-147"><span id="5"></span>**5** (16)</span><span class="sxs-lookup"><span data-stu-id="b629e-147"><span id="5"></span>**5** (16)</span></span>


</dt> <dd>

<span data-ttu-id="b629e-148">День 5 в месяце</span><span class="sxs-lookup"><span data-stu-id="b629e-148">Day 5 of a month</span></span>

</dd> <dt>

<span id="6"></span>

<span data-ttu-id="b629e-149"><span id="6"></span>**6** (32)</span><span class="sxs-lookup"><span data-stu-id="b629e-149"><span id="6"></span>**6** (32)</span></span>


</dt> <dd>

<span data-ttu-id="b629e-150">День 6 месяца</span><span class="sxs-lookup"><span data-stu-id="b629e-150">Day 6 of a month</span></span>

</dd> <dt>

<span id="7"></span>

<span data-ttu-id="b629e-151"><span id="7"></span>**7** (64)</span><span class="sxs-lookup"><span data-stu-id="b629e-151"><span id="7"></span>**7** (64)</span></span>


</dt> <dd>

<span data-ttu-id="b629e-152">День 7 месяца</span><span class="sxs-lookup"><span data-stu-id="b629e-152">Day 7 of a month</span></span>

</dd> <dt>

<span id="8"></span>

<span data-ttu-id="b629e-153"><span id="8"></span>**8** (128)</span><span class="sxs-lookup"><span data-stu-id="b629e-153"><span id="8"></span>**8** (128)</span></span>


</dt> <dd>

<span data-ttu-id="b629e-154">День 8 месяца</span><span class="sxs-lookup"><span data-stu-id="b629e-154">Day 8 of a month</span></span>

</dd> <dt>

<span id="9"></span>

<span data-ttu-id="b629e-155"><span id="9"></span>**9** (256)</span><span class="sxs-lookup"><span data-stu-id="b629e-155"><span id="9"></span>**9** (256)</span></span>


</dt> <dd>

<span data-ttu-id="b629e-156">9-й день месяца</span><span class="sxs-lookup"><span data-stu-id="b629e-156">Day 9 of a month</span></span>

</dd> <dt>

<span id="10"></span>

<span data-ttu-id="b629e-157"><span id="10"></span>**10** (512)</span><span class="sxs-lookup"><span data-stu-id="b629e-157"><span id="10"></span>**10** (512)</span></span>


</dt> <dd>

<span data-ttu-id="b629e-158">День 10 месяца</span><span class="sxs-lookup"><span data-stu-id="b629e-158">Day 10 of a month</span></span>

</dd> <dt>

<span id="11"></span>

<span data-ttu-id="b629e-159"><span id="11"></span>**11** (1024)</span><span class="sxs-lookup"><span data-stu-id="b629e-159"><span id="11"></span>**11** (1024)</span></span>


</dt> <dd>

<span data-ttu-id="b629e-160">День 11 в месяце</span><span class="sxs-lookup"><span data-stu-id="b629e-160">Day 11 of a month</span></span>

</dd> <dt>

<span id="12"></span>

<span data-ttu-id="b629e-161"><span id="12"></span>**12** (2048)</span><span class="sxs-lookup"><span data-stu-id="b629e-161"><span id="12"></span>**12** (2048)</span></span>


</dt> <dd>

<span data-ttu-id="b629e-162">12-й день месяца</span><span class="sxs-lookup"><span data-stu-id="b629e-162">Day 12 of a month</span></span>

</dd> <dt>

<span id="13"></span>

<span data-ttu-id="b629e-163"><span id="13"></span>**13** (4096)</span><span class="sxs-lookup"><span data-stu-id="b629e-163"><span id="13"></span>**13** (4096)</span></span>


</dt> <dd>

<span data-ttu-id="b629e-164">13-й день месяца</span><span class="sxs-lookup"><span data-stu-id="b629e-164">Day 13 of a month</span></span>

</dd> <dt>

<span id="14"></span>

<span data-ttu-id="b629e-165"><span id="14"></span>**14** (8192)</span><span class="sxs-lookup"><span data-stu-id="b629e-165"><span id="14"></span>**14** (8192)</span></span>


</dt> <dd>

<span data-ttu-id="b629e-166">14-й день месяца</span><span class="sxs-lookup"><span data-stu-id="b629e-166">Day 14 of a month</span></span>

</dd> <dt>

<span id="15"></span>

<span data-ttu-id="b629e-167"><span id="15"></span>**15** (16384)</span><span class="sxs-lookup"><span data-stu-id="b629e-167"><span id="15"></span>**15** (16384)</span></span>


</dt> <dd>

<span data-ttu-id="b629e-168">День 15 месяца</span><span class="sxs-lookup"><span data-stu-id="b629e-168">Day 15 of a month</span></span>

</dd> <dt>

<span id="16"></span>

<span data-ttu-id="b629e-169"><span id="16"></span>**16** (32768)</span><span class="sxs-lookup"><span data-stu-id="b629e-169"><span id="16"></span>**16** (32768)</span></span>


</dt> <dd>

<span data-ttu-id="b629e-170">16-й день месяца</span><span class="sxs-lookup"><span data-stu-id="b629e-170">Day 16 of a month</span></span>

</dd> <dt>

<span id="17"></span>

<span data-ttu-id="b629e-171"><span id="17"></span>**17** (65536)</span><span class="sxs-lookup"><span data-stu-id="b629e-171"><span id="17"></span>**17** (65536)</span></span>


</dt> <dd>

<span data-ttu-id="b629e-172">День 17 месяца</span><span class="sxs-lookup"><span data-stu-id="b629e-172">Day 17 of a month</span></span>

</dd> <dt>

<span id="18"></span>

<span data-ttu-id="b629e-173"><span id="18"></span>**18** (131072)</span><span class="sxs-lookup"><span data-stu-id="b629e-173"><span id="18"></span>**18** (131072)</span></span>


</dt> <dd>

<span data-ttu-id="b629e-174">18 дней месяца</span><span class="sxs-lookup"><span data-stu-id="b629e-174">Day 18 of a month</span></span>

</dd> <dt>

<span id="19"></span>

<span data-ttu-id="b629e-175"><span id="19"></span>**19** (262144)</span><span class="sxs-lookup"><span data-stu-id="b629e-175"><span id="19"></span>**19** (262144)</span></span>


</dt> <dd>

<span data-ttu-id="b629e-176">День 19 месяца</span><span class="sxs-lookup"><span data-stu-id="b629e-176">Day 19 of a month</span></span>

</dd> <dt>

<span id="20"></span>

<span data-ttu-id="b629e-177"><span id="20"></span>**20** (524288)</span><span class="sxs-lookup"><span data-stu-id="b629e-177"><span id="20"></span>**20** (524288)</span></span>


</dt> <dd>

<span data-ttu-id="b629e-178">День 20 месяца</span><span class="sxs-lookup"><span data-stu-id="b629e-178">Day 20 of a month</span></span>

</dd> <dt>

<span id="21"></span>

<span data-ttu-id="b629e-179"><span id="21"></span>**21** (1048576)</span><span class="sxs-lookup"><span data-stu-id="b629e-179"><span id="21"></span>**21** (1048576)</span></span>


</dt> <dd>

<span data-ttu-id="b629e-180">День 21 месяца</span><span class="sxs-lookup"><span data-stu-id="b629e-180">Day 21 of a month</span></span>

</dd> <dt>

<span id="22"></span>

<span data-ttu-id="b629e-181"><span id="22"></span>**22** (2097152)</span><span class="sxs-lookup"><span data-stu-id="b629e-181"><span id="22"></span>**22** (2097152)</span></span>


</dt> <dd>

<span data-ttu-id="b629e-182">День 22 месяца</span><span class="sxs-lookup"><span data-stu-id="b629e-182">Day 22 of a month</span></span>

</dd> <dt>

<span id="23"></span>

<span data-ttu-id="b629e-183"><span id="23"></span>**23** (4194304)</span><span class="sxs-lookup"><span data-stu-id="b629e-183"><span id="23"></span>**23** (4194304)</span></span>


</dt> <dd>

<span data-ttu-id="b629e-184">23-й день месяца</span><span class="sxs-lookup"><span data-stu-id="b629e-184">Day 23 of a month</span></span>

</dd> <dt>

<span id="24"></span>

<span data-ttu-id="b629e-185"><span id="24"></span>**24** (8388608)</span><span class="sxs-lookup"><span data-stu-id="b629e-185"><span id="24"></span>**24** (8388608)</span></span>


</dt> <dd>

<span data-ttu-id="b629e-186">24-й день месяца</span><span class="sxs-lookup"><span data-stu-id="b629e-186">Day 24 of a month</span></span>

</dd> <dt>

<span id="25"></span>

<span data-ttu-id="b629e-187"><span id="25"></span>**25** (16777216)</span><span class="sxs-lookup"><span data-stu-id="b629e-187"><span id="25"></span>**25** (16777216)</span></span>


</dt> <dd>

<span data-ttu-id="b629e-188">25-й день месяца</span><span class="sxs-lookup"><span data-stu-id="b629e-188">Day 25 of a month</span></span>

</dd> <dt>

<span id="26"></span>

<span data-ttu-id="b629e-189"><span id="26"></span>**26** (33554432)</span><span class="sxs-lookup"><span data-stu-id="b629e-189"><span id="26"></span>**26** (33554432)</span></span>


</dt> <dd>

<span data-ttu-id="b629e-190">День 26 месяца</span><span class="sxs-lookup"><span data-stu-id="b629e-190">Day 26 of a month</span></span>

</dd> <dt>

<span id="27"></span>

<span data-ttu-id="b629e-191"><span id="27"></span>**27** (67108864)</span><span class="sxs-lookup"><span data-stu-id="b629e-191"><span id="27"></span>**27** (67108864)</span></span>


</dt> <dd>

<span data-ttu-id="b629e-192">День 27 месяца</span><span class="sxs-lookup"><span data-stu-id="b629e-192">Day 27 of a month</span></span>

</dd> <dt>

<span id="28"></span>

<span data-ttu-id="b629e-193"><span id="28"></span>**28** (134217728)</span><span class="sxs-lookup"><span data-stu-id="b629e-193"><span id="28"></span>**28** (134217728)</span></span>


</dt> <dd>

<span data-ttu-id="b629e-194">28-й день месяца</span><span class="sxs-lookup"><span data-stu-id="b629e-194">Day 28 of a month</span></span>

</dd> <dt>

<span id="29"></span>

<span data-ttu-id="b629e-195"><span id="29"></span>**29** (268435456)</span><span class="sxs-lookup"><span data-stu-id="b629e-195"><span id="29"></span>**29** (268435456)</span></span>


</dt> <dd>

<span data-ttu-id="b629e-196">День 29 месяца</span><span class="sxs-lookup"><span data-stu-id="b629e-196">Day 29 of a month</span></span>

</dd> <dt>

<span id="30"></span>

<span data-ttu-id="b629e-197"><span id="30"></span>**30** (536870912)</span><span class="sxs-lookup"><span data-stu-id="b629e-197"><span id="30"></span>**30** (536870912)</span></span>


</dt> <dd>

<span data-ttu-id="b629e-198">День 30 месяца</span><span class="sxs-lookup"><span data-stu-id="b629e-198">Day 30 of a month</span></span>

</dd> <dt>

<span id="31"></span>

<span data-ttu-id="b629e-199"><span id="31"></span>**31** (1073741824)</span><span class="sxs-lookup"><span data-stu-id="b629e-199"><span id="31"></span>**31** (1073741824)</span></span>


</dt> <dd>

<span data-ttu-id="b629e-200">День 31 месяца</span><span class="sxs-lookup"><span data-stu-id="b629e-200">Day 31 of a month</span></span>

</dd> </dl> </dd> <dt>

<span data-ttu-id="b629e-201">*Интерактвисдесктоп* \[ в необязательное\]</span><span class="sxs-lookup"><span data-stu-id="b629e-201">*InteractWithDesktop* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="b629e-202">Если задано **значение true**, указанное задание должно быть интерактивным, а это означает, что пользователь может предоставить входные данные для запланированного задания во время выполнения задания.</span><span class="sxs-lookup"><span data-stu-id="b629e-202">If **True**, the specified job should be interactive, which means that a user can give input to a scheduled job while the job is executing.</span></span> <span data-ttu-id="b629e-203">По умолчанию **False**.</span><span class="sxs-lookup"><span data-stu-id="b629e-203">The default is **False**.</span></span>

</dd> <dt>

<span data-ttu-id="b629e-204">Идентификатор *задания* \[ заполняет\]</span><span class="sxs-lookup"><span data-stu-id="b629e-204">*JobId* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="b629e-205">Идентификатор задания.</span><span class="sxs-lookup"><span data-stu-id="b629e-205">Identifier number of a job.</span></span> <span data-ttu-id="b629e-206">Этот параметр является обработчиком для задания, запланированного на компьютере.</span><span class="sxs-lookup"><span data-stu-id="b629e-206">This parameter is a handle to a job being scheduled on a computer.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="b629e-207">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="b629e-207">Return value</span></span>

<span data-ttu-id="b629e-208">Возвращает значение 0 (нуль) при успешном выполнении и другое число для указания ошибки.</span><span class="sxs-lookup"><span data-stu-id="b629e-208">Returns a value of 0 (zero) when successful, and a different number to indicate an error.</span></span> <span data-ttu-id="b629e-209">Дополнительные коды ошибок см. в разделе [**константы WMI Error**](/windows/desktop/WmiSdk/wmi-error-constants) или [**вбемерроренум**](/windows/desktop/api/wbemdisp/ne-wbemdisp-wbemerrorenum).</span><span class="sxs-lookup"><span data-stu-id="b629e-209">For additional error codes, see [**WMI Error Constants**](/windows/desktop/WmiSdk/wmi-error-constants) or [**WbemErrorEnum**](/windows/desktop/api/wbemdisp/ne-wbemdisp-wbemerrorenum).</span></span> <span data-ttu-id="b629e-210">Общие значения **HRESULT** см. в разделе [коды системных ошибок](/windows/desktop/Debug/system-error-codes).</span><span class="sxs-lookup"><span data-stu-id="b629e-210">For general **HRESULT** values, see [System Error Codes](/windows/desktop/Debug/system-error-codes).</span></span>

<dl> <dt>

<span data-ttu-id="b629e-211">**Успешное завершение**</span><span class="sxs-lookup"><span data-stu-id="b629e-211">**Successful completion**</span></span>
</dt> <dd>

<span data-ttu-id="b629e-212">0</span><span class="sxs-lookup"><span data-stu-id="b629e-212">0</span></span>

<span data-ttu-id="b629e-213">Запрос принят.</span><span class="sxs-lookup"><span data-stu-id="b629e-213">The request is accepted.</span></span>

</dd> <dt>

<span data-ttu-id="b629e-214">**Не поддерживается**</span><span class="sxs-lookup"><span data-stu-id="b629e-214">**Not supported**</span></span>
</dt> <dd>

<span data-ttu-id="b629e-215">1</span><span class="sxs-lookup"><span data-stu-id="b629e-215">1</span></span>

<span data-ttu-id="b629e-216">Запрос не поддерживается.</span><span class="sxs-lookup"><span data-stu-id="b629e-216">The request is not supported.</span></span>

</dd> <dt>

<span data-ttu-id="b629e-217">**Доступ запрещен**</span><span class="sxs-lookup"><span data-stu-id="b629e-217">**Access denied**</span></span>
</dt> <dd>

<span data-ttu-id="b629e-218">2</span><span class="sxs-lookup"><span data-stu-id="b629e-218">2</span></span>

<span data-ttu-id="b629e-219">У пользователя нет необходимых прав доступа.</span><span class="sxs-lookup"><span data-stu-id="b629e-219">The user does not have the necessary access.</span></span>

</dd> <dt>

<span data-ttu-id="b629e-220">**Неизвестный сбой**</span><span class="sxs-lookup"><span data-stu-id="b629e-220">**Unknown failure**</span></span>
</dt> <dd>

<span data-ttu-id="b629e-221">8</span><span class="sxs-lookup"><span data-stu-id="b629e-221">8</span></span>

<span data-ttu-id="b629e-222">Интерактивный процесс.</span><span class="sxs-lookup"><span data-stu-id="b629e-222">Interactive process.</span></span>

</dd> <dt>

<span data-ttu-id="b629e-223">**Путь не найден**</span><span class="sxs-lookup"><span data-stu-id="b629e-223">**Path not found**</span></span>
</dt> <dd>

<span data-ttu-id="b629e-224">9</span><span class="sxs-lookup"><span data-stu-id="b629e-224">9</span></span>

<span data-ttu-id="b629e-225">Не удается найти путь каталога к исполняемому файлу службы.</span><span class="sxs-lookup"><span data-stu-id="b629e-225">The directory path to the service executable file cannot be found.</span></span>

</dd> <dt>

<span data-ttu-id="b629e-226">**недопустимый параметр.**</span><span class="sxs-lookup"><span data-stu-id="b629e-226">**Invalid parameter**</span></span>
</dt> <dd>

<span data-ttu-id="b629e-227">21</span><span class="sxs-lookup"><span data-stu-id="b629e-227">21</span></span>

<span data-ttu-id="b629e-228">Службе переданы недопустимые параметры.</span><span class="sxs-lookup"><span data-stu-id="b629e-228">Invalid parameters have been passed to the service.</span></span>

</dd> <dt>

<span data-ttu-id="b629e-229">**Служба не запущена**</span><span class="sxs-lookup"><span data-stu-id="b629e-229">**Service not started**</span></span>
</dt> <dd>

<span data-ttu-id="b629e-230">22</span><span class="sxs-lookup"><span data-stu-id="b629e-230">22</span></span>

<span data-ttu-id="b629e-231">Учетная запись, под которой выполняется эта служба, недопустима или не имеет разрешений на запуск службы.</span><span class="sxs-lookup"><span data-stu-id="b629e-231">The account that this service runs under is invalid or lacks the permissions to run the service.</span></span>

</dd> <dt>

<span data-ttu-id="b629e-232">**Другое**</span><span class="sxs-lookup"><span data-stu-id="b629e-232">**Other**</span></span>
</dt> <dd>

<span data-ttu-id="b629e-233">23 4294967295</span><span class="sxs-lookup"><span data-stu-id="b629e-233">23 4294967295</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="b629e-234">Комментарии</span><span class="sxs-lookup"><span data-stu-id="b629e-234">Remarks</span></span>

<span data-ttu-id="b629e-235">Если запланированное задание запускает интерактивную программу, например Блокнот, то свойство **интерактвисдескто** должно иметь значение **true** или экран программы не отображается.</span><span class="sxs-lookup"><span data-stu-id="b629e-235">If your scheduled job starts an interactive program such as Notepad, then the **InteractWithDeskto** property must be set to **True** or the program's screen is not visible.</span></span> <span data-ttu-id="b629e-236">Процесс по-прежнему отображается в **диспетчере задач** , даже если он не отображается на экране.</span><span class="sxs-lookup"><span data-stu-id="b629e-236">The process still appears in the **Task Manager** even if it does not appear on the screen.</span></span>

## <a name="requirements"></a><span data-ttu-id="b629e-237">Требования</span><span class="sxs-lookup"><span data-stu-id="b629e-237">Requirements</span></span>



| <span data-ttu-id="b629e-238">Требование</span><span class="sxs-lookup"><span data-stu-id="b629e-238">Requirement</span></span> | <span data-ttu-id="b629e-239">Значение</span><span class="sxs-lookup"><span data-stu-id="b629e-239">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="b629e-240">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="b629e-240">Minimum supported client</span></span><br/> | <span data-ttu-id="b629e-241">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="b629e-241">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="b629e-242">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="b629e-242">Minimum supported server</span></span><br/> | <span data-ttu-id="b629e-243">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="b629e-243">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="b629e-244">Пространство имен</span><span class="sxs-lookup"><span data-stu-id="b629e-244">Namespace</span></span><br/>                | <span data-ttu-id="b629e-245">Корневой \\ CIMV2</span><span class="sxs-lookup"><span data-stu-id="b629e-245">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="b629e-246">MOF</span><span class="sxs-lookup"><span data-stu-id="b629e-246">MOF</span></span><br/>                      | <dl> <span data-ttu-id="b629e-247"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="b629e-247"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="b629e-248">DLL</span><span class="sxs-lookup"><span data-stu-id="b629e-248">DLL</span></span><br/>                      | <dl> <span data-ttu-id="b629e-249"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="b629e-249"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="b629e-250">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="b629e-250">See also</span></span>

<dl> <dt>

<span data-ttu-id="b629e-251">[Классы операционной системы](/previous-versions//aa392727(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="b629e-251">[Operating System Classes](/previous-versions//aa392727(v=vs.85))</span></span>
</dt> <dt>

[<span data-ttu-id="b629e-252">**\_ScheduledJob Win32**</span><span class="sxs-lookup"><span data-stu-id="b629e-252">**Win32\_ScheduledJob**</span></span>](win32-scheduledjob.md)
</dt> </dl>

 

