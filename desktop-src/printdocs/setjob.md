---
description: Функция Сетжоб приостанавливает, возобновляет, отменяет или перезапускает задание печати на указанном принтере. Можно также использовать функцию Сетжоб, чтобы задать параметры задания печати, такие как приоритет задания печати и имя документа.
ms.assetid: 21947c69-c517-4962-8eb7-b45ed4211d9a
title: Функция Сетжоб (Винспул. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SetJob
- SetJobA
- SetJobW
api_type:
- DllExport
api_location:
- WinSpool.drv
- Ext-MS-Win-Printer-WinSpool-l1-1-2.dll
- Ext-MS-Win-Printer-WinSpool-L1-1-3.dll
ms.openlocfilehash: 34dfc8c0239a10d7e7f036beed457d57329f4c67
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "105683872"
---
# <a name="setjob-function"></a><span data-ttu-id="80542-104">Функция Сетжоб</span><span class="sxs-lookup"><span data-stu-id="80542-104">SetJob function</span></span>

<span data-ttu-id="80542-105">Функция **сетжоб** приостанавливает, возобновляет, отменяет или перезапускает задание печати на указанном принтере.</span><span class="sxs-lookup"><span data-stu-id="80542-105">The **SetJob** function pauses, resumes, cancels, or restarts a print job on a specified printer.</span></span> <span data-ttu-id="80542-106">Можно также использовать функцию **сетжоб** , чтобы задать параметры задания печати, такие как приоритет задания печати и имя документа.</span><span class="sxs-lookup"><span data-stu-id="80542-106">You can also use the **SetJob** function to set print job parameters, such as the print job priority and the document name.</span></span>

<span data-ttu-id="80542-107">Функцию **сетжоб** можно использовать, чтобы передать команду заданию печати или задать параметры задания печати или выполнить оба действия в одном вызове.</span><span class="sxs-lookup"><span data-stu-id="80542-107">You can use the **SetJob** function to give a command to a print job, or to set print job parameters, or to do both in the same call.</span></span> <span data-ttu-id="80542-108">Значение параметра *команды* не влияет на то, как функция использует параметры *Level* и *пжоб* .</span><span class="sxs-lookup"><span data-stu-id="80542-108">The value of the *Command* parameter does not affect how the function uses the *Level* and *pJob* parameters.</span></span> <span data-ttu-id="80542-109">Кроме того, можно использовать **сетжоб** со [**\_ сведениями \_ о задании 3**](job-info-3.md) , чтобы связать набор заданий печати.</span><span class="sxs-lookup"><span data-stu-id="80542-109">Also, you can use **SetJob** with [**JOB\_INFO\_3**](job-info-3.md) to link together a set of print jobs.</span></span> <span data-ttu-id="80542-110">Дополнительные сведения см. в разделе "Примечания".</span><span class="sxs-lookup"><span data-stu-id="80542-110">See Remarks for more information.</span></span>

## <a name="syntax"></a><span data-ttu-id="80542-111">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="80542-111">Syntax</span></span>


```C++
BOOL SetJob(
  _In_ HANDLE hPrinter,
  _In_ DWORD  JobId,
  _In_ DWORD  Level,
  _In_ LPBYTE pJob,
  _In_ DWORD  Command
);
```



## <a name="parameters"></a><span data-ttu-id="80542-112">Параметры</span><span class="sxs-lookup"><span data-stu-id="80542-112">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="80542-113">*хпринтер* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="80542-113">*hPrinter* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="80542-114">Описатель объекта принтера, который нужно заинтересовать.</span><span class="sxs-lookup"><span data-stu-id="80542-114">A handle to the printer object of interest.</span></span> <span data-ttu-id="80542-115">Используйте функцию [**опенпринтер**](openprinter.md), [**OpenPrinter2**](openprinter2.md)или [**аддпринтер**](addprinter.md) для получения маркера принтера.</span><span class="sxs-lookup"><span data-stu-id="80542-115">Use the [**OpenPrinter**](openprinter.md), [**OpenPrinter2**](openprinter2.md), or [**AddPrinter**](addprinter.md) function to retrieve a printer handle.</span></span>

</dd> <dt>

<span data-ttu-id="80542-116">Идентификатор *задания* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="80542-116">*JobId* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="80542-117">Идентификатор, указывающий задание печати.</span><span class="sxs-lookup"><span data-stu-id="80542-117">Identifier that specifies the print job.</span></span> <span data-ttu-id="80542-118">Чтобы получить идентификатор задания печати, вызовите функцию [**AddJob**](addjob.md) или функцию [**стартдок**](/windows/desktop/api/Wingdi/nf-wingdi-startdoca) .</span><span class="sxs-lookup"><span data-stu-id="80542-118">You obtain a print job identifier by calling the [**AddJob**](addjob.md) function or the [**StartDoc**](/windows/desktop/api/Wingdi/nf-wingdi-startdoca) function.</span></span>

<span data-ttu-id="80542-119">Если параметр *Level* имеет значение 3, то параметр *JOBID* должен соответствовать элементу **JOBID** структуры [**задания \_ \_ 3**](job-info-3.md) , на которую указывает *пжоб*</span><span class="sxs-lookup"><span data-stu-id="80542-119">If the *Level* parameter is set to 3, the *JobId* parameter must match the **JobId** member of the [**JOB\_INFO\_3**](job-info-3.md) structure pointed to by *pJob*</span></span>

</dd> <dt>

<span data-ttu-id="80542-120">*Уровень* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="80542-120">*Level* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="80542-121">Тип структуры сведений о задании, на которую указывает параметр *пжоб* .</span><span class="sxs-lookup"><span data-stu-id="80542-121">The type of job information structure pointed to by the *pJob* parameter.</span></span>

<span data-ttu-id="80542-122">**Все версии Windows**: для параметра *уровня* можно задать значение 0, 1 или 2.</span><span class="sxs-lookup"><span data-stu-id="80542-122">**All versions of Windows**: You can set the *Level* parameter to 0, 1, or 2.</span></span> <span data-ttu-id="80542-123">Если для параметра *Level* задать значение 0, *Пжоб* должен иметь **значение NULL**.</span><span class="sxs-lookup"><span data-stu-id="80542-123">When you set *Level* to 0, *pJob* should be **NULL**.</span></span> <span data-ttu-id="80542-124">Используйте эти значения, если не заданы какие либо параметры задания печати.</span><span class="sxs-lookup"><span data-stu-id="80542-124">Use these values when you are not setting any print job parameters.</span></span>

<span data-ttu-id="80542-125">Можно также задать для параметра *уровня* значение 3.</span><span class="sxs-lookup"><span data-stu-id="80542-125">You can also set the *Level* parameter to 3.</span></span>

<span data-ttu-id="80542-126">Начиная с **Windows Vista**, можно также задать для параметра *уровня* значение 4.</span><span class="sxs-lookup"><span data-stu-id="80542-126">Starting with **Windows Vista**: You can also set the *Level* parameter to 4.</span></span>

</dd> <dt>

<span data-ttu-id="80542-127">*пжоб* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="80542-127">*pJob* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="80542-128">Указатель на структуру, которая задает параметры задания печати.</span><span class="sxs-lookup"><span data-stu-id="80542-128">A pointer to a structure that sets the print job parameters.</span></span>

<span data-ttu-id="80542-129">**Все версии Windows**: *пжоб* могут указывать на структуру [**\_ сведений о задании \_ 1**](job-info-1.md) или [**о задании \_ \_ 2**](job-info-2.md) .</span><span class="sxs-lookup"><span data-stu-id="80542-129">**All versions of Windows**: *pJob* can point to a [**JOB\_INFO\_1**](job-info-1.md) or [**JOB\_INFO\_2**](job-info-2.md) structure.</span></span>

<span data-ttu-id="80542-130">*пжоб* также может указывать на структуру [**\_ сведений о \_ задании 3**](job-info-3.md) .</span><span class="sxs-lookup"><span data-stu-id="80542-130">*pJob* can also point to a [**JOB\_INFO\_3**](job-info-3.md) structure.</span></span> <span data-ttu-id="80542-131">Необходимо иметь **\_ доступ к заданиям \_ Администрирование** разрешение на доступ для заданий, указанных в элементах **JOBID** и **некстжобид** структуры **\_ сведений о задании \_ 3** .</span><span class="sxs-lookup"><span data-stu-id="80542-131">You must have **JOB\_ACCESS\_ADMINISTER** access permission for the jobs specified by the **JobId** and **NextJobId** members of the **JOB\_INFO\_3** structure.</span></span>

<span data-ttu-id="80542-132">Начиная с **Windows Vista**: *пжоб* также может указывать на структуру [**\_ сведений о \_ задании 4**](job-info-4.md) .</span><span class="sxs-lookup"><span data-stu-id="80542-132">Starting with **Windows Vista**: *pJob* can also point to a [**JOB\_INFO\_4**](job-info-4.md) structure.</span></span>

<span data-ttu-id="80542-133">Если параметр *уровня* равен 0, *Пжоб* должен иметь **значение NULL**.</span><span class="sxs-lookup"><span data-stu-id="80542-133">If the *Level* parameter is 0, *pJob* should be **NULL**.</span></span>

</dd> <dt>

<span data-ttu-id="80542-134">*Команда* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="80542-134">*Command* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="80542-135">Выполняемая операция задания печати.</span><span class="sxs-lookup"><span data-stu-id="80542-135">The print job operation to perform.</span></span> <span data-ttu-id="80542-136">Этот параметр может принимать одно из указанных ниже значений.</span><span class="sxs-lookup"><span data-stu-id="80542-136">This parameter can be one of the following values.</span></span>



| <span data-ttu-id="80542-137">Значение</span><span class="sxs-lookup"><span data-stu-id="80542-137">Value</span></span>                                                                                                                                                                                                            | <span data-ttu-id="80542-138">Значение</span><span class="sxs-lookup"><span data-stu-id="80542-138">Meaning</span></span>                                                                            |
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------|
| <span id="JOB_CONTROL_CANCEL"></span><span id="job_control_cancel"></span><dl> <span data-ttu-id="80542-139"><dt>**\_Отмена управления заданиями \_**</dt></span><span class="sxs-lookup"><span data-stu-id="80542-139"><dt>**JOB\_CONTROL\_CANCEL**</dt></span></span> </dl>                                    | <span data-ttu-id="80542-140">Не используйте.</span><span class="sxs-lookup"><span data-stu-id="80542-140">Do not use.</span></span> <span data-ttu-id="80542-141">Чтобы удалить задание печати, используйте **\_ элемент управления заданием \_ Удалить**.</span><span class="sxs-lookup"><span data-stu-id="80542-141">To delete a print job, use **JOB\_CONTROL\_DELETE**.</span></span><br/>        |
| <span id="JOB_CONTROL_PAUSE"></span><span id="job_control_pause"></span><dl> <span data-ttu-id="80542-142"><dt>**Приостановка задания \_ управления \_**</dt></span><span class="sxs-lookup"><span data-stu-id="80542-142"><dt>**JOB\_CONTROL\_PAUSE**</dt></span></span> </dl>                                       | <span data-ttu-id="80542-143">Приостановка задания печати.</span><span class="sxs-lookup"><span data-stu-id="80542-143">Pause the print job.</span></span><br/>                                                    |
| <span id="JOB_CONTROL_RESTART"></span><span id="job_control_restart"></span><dl> <span data-ttu-id="80542-144"><dt>**Управление ЗАДАНИЕм \_ \_ перезапуска**</dt></span><span class="sxs-lookup"><span data-stu-id="80542-144"><dt>**JOB\_CONTROL\_RESTART**</dt></span></span> </dl>                                 | <span data-ttu-id="80542-145">Перезапустите задание печати.</span><span class="sxs-lookup"><span data-stu-id="80542-145">Restart the print job.</span></span> <span data-ttu-id="80542-146">Задание может быть перезапущено только при его печати.</span><span class="sxs-lookup"><span data-stu-id="80542-146">A job can only be restarted if it was printing.</span></span><br/>  |
| <span id="JOB_CONTROL_RESUME"></span><span id="job_control_resume"></span><dl> <span data-ttu-id="80542-147"><dt>**возобновление управления ЗАДАНИЯми \_ \_**</dt></span><span class="sxs-lookup"><span data-stu-id="80542-147"><dt>**JOB\_CONTROL\_RESUME**</dt></span></span> </dl>                                    | <span data-ttu-id="80542-148">Возобновление приостановленного задания печати.</span><span class="sxs-lookup"><span data-stu-id="80542-148">Resume a paused print job.</span></span><br/>                                              |
| <span id="JOB_CONTROL_DELETE"></span><span id="job_control_delete"></span><dl> <span data-ttu-id="80542-149"><dt>**\_Удаление элемента управления заданием \_**</dt></span><span class="sxs-lookup"><span data-stu-id="80542-149"><dt>**JOB\_CONTROL\_DELETE**</dt></span></span> </dl>                                    | <span data-ttu-id="80542-150">Удалите задание печати.</span><span class="sxs-lookup"><span data-stu-id="80542-150">Delete the print job.</span></span><br/>                                                   |
| <span id="JOB_CONTROL_SENT_TO_PRINTER"></span><span id="job_control_sent_to_printer"></span><dl> <span data-ttu-id="80542-151"><dt>**Управление ЗАДАНИЕм \_ \_ Отправлено \_ на \_ принтер**</dt></span><span class="sxs-lookup"><span data-stu-id="80542-151"><dt>**JOB\_CONTROL\_SENT\_TO\_PRINTER**</dt></span></span> </dl>       | <span data-ttu-id="80542-152">Используется мониторами портов для завершения задания печати.</span><span class="sxs-lookup"><span data-stu-id="80542-152">Used by port monitors to end the print job.</span></span><br/>                             |
| <span id="JOB_CONTROL_LAST_PAGE_EJECTED"></span><span id="job_control_last_page_ejected"></span><dl> <span data-ttu-id="80542-153"><dt>**Последняя страница "Управление ЗАДАНИЕм" \_ \_ \_ \_ извлечена**</dt></span><span class="sxs-lookup"><span data-stu-id="80542-153"><dt>**JOB\_CONTROL\_LAST\_PAGE\_EJECTED**</dt></span></span> </dl> | <span data-ttu-id="80542-154">Используется мониторами языка для завершения задания печати.</span><span class="sxs-lookup"><span data-stu-id="80542-154">Used by language monitors to end the print job.</span></span><br/>                         |
| <span id="JOB_CONTROL_RETAIN"></span><span id="job_control_retain"></span><dl> <span data-ttu-id="80542-155"><dt>**\_сохраняемый элемент управления задания \_**</dt></span><span class="sxs-lookup"><span data-stu-id="80542-155"><dt>**JOB\_CONTROL\_RETAIN**</dt></span></span> </dl>                                    | <span data-ttu-id="80542-156">**Windows Vista и более поздние версии**: задание должно находиться в очереди после печати.</span><span class="sxs-lookup"><span data-stu-id="80542-156">**Windows Vista and later**: Keep the job in the queue after it prints.</span></span><br/> |
| <span id="JOB_CONTROL_RELEASE"></span><span id="job_control_release"></span><dl> <span data-ttu-id="80542-157"><dt>**\_выпуск элемента управления задания \_**</dt></span><span class="sxs-lookup"><span data-stu-id="80542-157"><dt>**JOB\_CONTROL\_RELEASE**</dt></span></span> </dl>                                 | <span data-ttu-id="80542-158">**Windows Vista и более поздние версии**: отпустите задание печати.</span><span class="sxs-lookup"><span data-stu-id="80542-158">**Windows Vista and later**: Release the print job.</span></span><br/>                     |



 

<span data-ttu-id="80542-159">Вы можете использовать тот же вызов функции **сетжоб** , чтобы задать параметры задания печати и дать команду заданию печати.</span><span class="sxs-lookup"><span data-stu-id="80542-159">You can use the same call to the **SetJob** function to set print job parameters and to give a command to a print job.</span></span> <span data-ttu-id="80542-160">Поэтому *команда* не должна иметь значение 0, если заданы параметры задания печати, хотя это может быть.</span><span class="sxs-lookup"><span data-stu-id="80542-160">Thus, *Command* does not need to be 0 if you are setting print job parameters, although it can be.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="80542-161">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="80542-161">Return value</span></span>

<span data-ttu-id="80542-162">Если функция выполнена, возвращаемое значение будет ненулевым.</span><span class="sxs-lookup"><span data-stu-id="80542-162">If the function succeeds, the return value is a nonzero value.</span></span>

<span data-ttu-id="80542-163">Если функция выполняется неудачно, возвращается нулевое значение.</span><span class="sxs-lookup"><span data-stu-id="80542-163">If the function fails, the return value is zero.</span></span>

## <a name="remarks"></a><span data-ttu-id="80542-164">Комментарии</span><span class="sxs-lookup"><span data-stu-id="80542-164">Remarks</span></span>

> [!Note]  
> <span data-ttu-id="80542-165">Это блокирующая или синхронная функция, которая может не возвращать значение немедленно.</span><span class="sxs-lookup"><span data-stu-id="80542-165">This is a blocking or synchronous function and might not return immediately.</span></span> <span data-ttu-id="80542-166">Скорость возврата этой функцией зависит от факторов времени выполнения, таких как состояние сети, Конфигурация сервера печати и факторы реализации драйвера принтера, которые трудно предсказать при написании приложения.</span><span class="sxs-lookup"><span data-stu-id="80542-166">How quickly this function returns depends on run-time factors such as network status, print server configuration, and printer driver implementation factors that are difficult to predict when writing an application.</span></span> <span data-ttu-id="80542-167">Вызов этой функции из потока, который управляет взаимодействием с пользовательским интерфейсом, может привести к невозможности реагирования приложения.</span><span class="sxs-lookup"><span data-stu-id="80542-167">Calling this function from a thread that manages interaction with the user interface could make the application appear to be unresponsive.</span></span>

 

<span data-ttu-id="80542-168">Для задания различных параметров задания печати можно использовать функцию **сетжоб** , указав указатель на сведения о задании [**\_ \_ 1**](job-info-1.md), [**сведения о задании \_ \_ 2**](job-info-2.md), [**\_ сведения о задании \_ 3**](job-info-3.md)или [**\_ сведения о задании \_ 4**](job-info-4.md) , содержащие необходимые данные.</span><span class="sxs-lookup"><span data-stu-id="80542-168">You can use the **SetJob** function to set various print job parameters by supplying a pointer to a [**JOB\_INFO\_1**](job-info-1.md), [**JOB\_INFO\_2**](job-info-2.md), [**JOB\_INFO\_3**](job-info-3.md), or [**JOB\_INFO\_4**](job-info-4.md) structure that contains the necessary data.</span></span>

<span data-ttu-id="80542-169">Чтобы удалить или удалить все задания печати для конкретного принтера, вызовите функцию [**сетпринтер**](setprinter.md) с параметром *Command* , для которого задана **\_ \_ Очистка элемента управления принтера**.</span><span class="sxs-lookup"><span data-stu-id="80542-169">To remove or delete all of the print jobs for a particular printer, call the [**SetPrinter**](setprinter.md) function with its *Command* parameter set to **PRINTER\_CONTROL\_PURGE**.</span></span>

<span data-ttu-id="80542-170">Следующие члены структуры [**\_ сведений о задании \_ 1**](job-info-1.md), [**\_ сведения о \_ задании 2**](job-info-2.md)или [**\_ сведения о задании \_ 4**](job-info-4.md) игнорируются при вызове **сетжоб**: **JOBID**, **ппринтернаме**, **пмачиненаме**, **пусернаме**, **пдривернаме**, **size**, **отправлен**, **time** и **TotalPages**.</span><span class="sxs-lookup"><span data-stu-id="80542-170">The following members of a [**JOB\_INFO\_1**](job-info-1.md), [**JOB\_INFO\_2**](job-info-2.md), or [**JOB\_INFO\_4**](job-info-4.md) structure are ignored on a call to **SetJob**: **JobId**, **pPrinterName**, **pMachineName**, **pUserName**, **pDrivername**, **Size**, **Submitted**, **Time**, and **TotalPages**.</span></span>

<span data-ttu-id="80542-171">Чтобы изменить расположение задания печати в очереди печати, необходимо иметь разрешение на доступ к **принтеру \_ \_ Управление** доступом к принтеру.</span><span class="sxs-lookup"><span data-stu-id="80542-171">You must have **PRINTER\_ACCESS\_ADMINISTER** access permission for a printer in order to change a print job's position in the print queue.</span></span>

<span data-ttu-id="80542-172">Если вы не хотите задавать расположение задания печати в очереди печати, необходимо задать для элемента **должность** в структуре задания [**\_ \_ 1**](job-info-1.md), [**\_ сведения о задании \_ 2**](job-info-2.md)или [**\_ сведения о задании \_ 4**](job-info-4.md) значение **должность задания не \_ \_ указано**.</span><span class="sxs-lookup"><span data-stu-id="80542-172">If you do not want to set a print job's position in the print queue, you should set the **Position** member of the [**JOB\_INFO\_1**](job-info-1.md), [**JOB\_INFO\_2**](job-info-2.md), or [**JOB\_INFO\_4**](job-info-4.md) structure to **JOB\_POSITION\_UNSPECIFIED**.</span></span>

<span data-ttu-id="80542-173">Используйте функцию **сетжоб** с структурой [**\_ сведений о \_ задании 3**](job-info-3.md) , чтобы связать набор заданий печати (также называемых цепочкой).</span><span class="sxs-lookup"><span data-stu-id="80542-173">Use the **SetJob** function with the [**JOB\_INFO\_3**](job-info-3.md) structure to link together a set of print jobs (also known as a chain).</span></span> <span data-ttu-id="80542-174">Это полезно в ситуациях, когда один документ состоит из нескольких частей, которые нужно визуализировать отдельно.</span><span class="sxs-lookup"><span data-stu-id="80542-174">This is useful in situations where a single document consists of several parts that you want to render separately.</span></span> <span data-ttu-id="80542-175">Для печати заданий A, B, C и D по порядку вызовите **сетжоб** со [**\_ сведениями \_ о задании 4**](job-info-4.md) , чтобы связать A с b, b с c и c по D.</span><span class="sxs-lookup"><span data-stu-id="80542-175">To print jobs A, B, C, and D in order, call **SetJob** with [**JOB\_INFO\_4**](job-info-4.md) to link A to B, B to C, and C to D.</span></span>

<span data-ttu-id="80542-176">При связывании заданий печати обратите внимание на следующее.</span><span class="sxs-lookup"><span data-stu-id="80542-176">If you link print jobs, note the following:</span></span>

-   <span data-ttu-id="80542-177">Задания можно добавлять в начало или в конец цепочки.</span><span class="sxs-lookup"><span data-stu-id="80542-177">Jobs can be added to the beginning or end of a chain.</span></span>
-   <span data-ttu-id="80542-178">Все задания в цепочке должны иметь один и тот же тип данных.</span><span class="sxs-lookup"><span data-stu-id="80542-178">All jobs in the chain must have the same data type.</span></span>
-   <span data-ttu-id="80542-179">Цепочка должна быть полностью связана перед началом буферизации, в противном случае диспетчер очереди печати может печатать и удалять задания, помещенные в очередь, прежде чем связать их все.</span><span class="sxs-lookup"><span data-stu-id="80542-179">The chain must be completely linked before spooling begins, otherwise the spooler may print and delete spooled jobs before you link them all.</span></span> <span data-ttu-id="80542-180">Существует два способа сделать цепочку непреждевременной печати:</span><span class="sxs-lookup"><span data-stu-id="80542-180">There are two ways to keep the chain from printing prematurely:</span></span>

    -   <span data-ttu-id="80542-181">Приостановите первое задание в цепочке, пока цепочка не будет полностью связана.</span><span class="sxs-lookup"><span data-stu-id="80542-181">Pause the first job in the chain until the chain is completely linked.</span></span> <span data-ttu-id="80542-182">Приостановленное состояние первого задания управляет состоянием всех заданий в цепочке.</span><span class="sxs-lookup"><span data-stu-id="80542-182">The paused state of the first job governs the state of all jobs in the chain.</span></span>
    -   <span data-ttu-id="80542-183">Не заключайте первое задание в неполное, т. е. не вызывайте [**енддок**](/windows/desktop/api/Wingdi/nf-wingdi-enddoc) или [**ScheduleJob**](schedulejob.md) для первого задания.</span><span class="sxs-lookup"><span data-stu-id="80542-183">Keep the first job incomplete, that is, do not call [**EndDoc**](/windows/desktop/api/Wingdi/nf-wingdi-enddoc) or [**ScheduleJob**](schedulejob.md) for the first job.</span></span> <span data-ttu-id="80542-184">Тем не менее, если включен параметр "печатать при постановке в очередь" (по умолчанию), этот метод блокирует порт во время сборки цепочки, что также предотвращает печать несвязанных заданий.</span><span class="sxs-lookup"><span data-stu-id="80542-184">However, if 'print while spooling' is enabled (the default), this method blocks the port while the chain is built, which also prevents the printing of non-related jobs.</span></span>

-   <span data-ttu-id="80542-185">Приложение должно работать в случае, когда пользователь удаляет задание в цепочке до того, как цепочка завершает печать.</span><span class="sxs-lookup"><span data-stu-id="80542-185">The application must handle the case where the user deletes a job in the chain before the chain finishes printing.</span></span> <span data-ttu-id="80542-186">Аргумент [**GetLastError**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror) возвращает **Недопустимый \_ параметр** , если идентификатор задания не существует.</span><span class="sxs-lookup"><span data-stu-id="80542-186">[**GetLastError**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror) returns **INVALID\_PARAMETER** when a JobID does not exist.</span></span>

## <a name="requirements"></a><span data-ttu-id="80542-187">Требования</span><span class="sxs-lookup"><span data-stu-id="80542-187">Requirements</span></span>



| <span data-ttu-id="80542-188">Требование</span><span class="sxs-lookup"><span data-stu-id="80542-188">Requirement</span></span> | <span data-ttu-id="80542-189">Значение</span><span class="sxs-lookup"><span data-stu-id="80542-189">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="80542-190">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="80542-190">Minimum supported client</span></span><br/> | <span data-ttu-id="80542-191">Windows 2000 Professional \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="80542-191">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                                |
| <span data-ttu-id="80542-192">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="80542-192">Minimum supported server</span></span><br/> | <span data-ttu-id="80542-193">Windows 2000 Server \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="80542-193">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                      |
| <span data-ttu-id="80542-194">Заголовок</span><span class="sxs-lookup"><span data-stu-id="80542-194">Header</span></span><br/>                   | <dl> <span data-ttu-id="80542-195"><dt>Винспул. h (включение Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="80542-195"><dt>WinSpool.h (include Windows.h)</dt></span></span> </dl> |
| <span data-ttu-id="80542-196">Библиотека</span><span class="sxs-lookup"><span data-stu-id="80542-196">Library</span></span><br/>                  | <dl> <span data-ttu-id="80542-197"><dt>Винспул. lib</dt></span><span class="sxs-lookup"><span data-stu-id="80542-197"><dt>WinSpool.lib</dt></span></span> </dl>                   |
| <span data-ttu-id="80542-198">DLL</span><span class="sxs-lookup"><span data-stu-id="80542-198">DLL</span></span><br/>                      | <dl> <span data-ttu-id="80542-199"><dt>Винспул. drv</dt></span><span class="sxs-lookup"><span data-stu-id="80542-199"><dt>WinSpool.drv</dt></span></span> </dl>                   |
| <span data-ttu-id="80542-200">Имя в кодировке Юникод и ANSI</span><span class="sxs-lookup"><span data-stu-id="80542-200">Unicode and ANSI names</span></span><br/>   | <span data-ttu-id="80542-201">**Сетжобв** (Юникод) и **сетжоба** (ANSI)</span><span class="sxs-lookup"><span data-stu-id="80542-201">**SetJobW** (Unicode) and **SetJobA** (ANSI)</span></span><br/>                                                   |



## <a name="see-also"></a><span data-ttu-id="80542-202">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="80542-202">See also</span></span>

<dl> <dt>

[<span data-ttu-id="80542-203">Вывод на печать</span><span class="sxs-lookup"><span data-stu-id="80542-203">Printing</span></span>](printdocs-printing.md)
</dt> <dt>

[<span data-ttu-id="80542-204">Функции API очереди печати принтера</span><span class="sxs-lookup"><span data-stu-id="80542-204">Print Spooler API Functions</span></span>](printing-and-print-spooler-functions.md)
</dt> <dt>

[<span data-ttu-id="80542-205">**AddJob**</span><span class="sxs-lookup"><span data-stu-id="80542-205">**AddJob**</span></span>](addjob.md)
</dt> <dt>

[<span data-ttu-id="80542-206">**жетжоб**</span><span class="sxs-lookup"><span data-stu-id="80542-206">**GetJob**</span></span>](getjob.md)
</dt> <dt>

[<span data-ttu-id="80542-207">**опенпринтер**</span><span class="sxs-lookup"><span data-stu-id="80542-207">**OpenPrinter**</span></span>](openprinter.md)
</dt> <dt>

[<span data-ttu-id="80542-208">**сетпринтер**</span><span class="sxs-lookup"><span data-stu-id="80542-208">**SetPrinter**</span></span>](setprinter.md)
</dt> <dt>

[<span data-ttu-id="80542-209">**\_Сведения о задании \_ 1**</span><span class="sxs-lookup"><span data-stu-id="80542-209">**JOB\_INFO\_1**</span></span>](job-info-1.md)
</dt> <dt>

[<span data-ttu-id="80542-210">**\_Сведения о задании \_ 2**</span><span class="sxs-lookup"><span data-stu-id="80542-210">**JOB\_INFO\_2**</span></span>](job-info-2.md)
</dt> <dt>

[<span data-ttu-id="80542-211">**\_Сведения о задании \_ 3**</span><span class="sxs-lookup"><span data-stu-id="80542-211">**JOB\_INFO\_3**</span></span>](job-info-3.md)
</dt> <dt>

[<span data-ttu-id="80542-212">**\_Сведения о задании \_ 4**</span><span class="sxs-lookup"><span data-stu-id="80542-212">**JOB\_INFO\_4**</span></span>](job-info-4.md)
</dt> </dl>

 

