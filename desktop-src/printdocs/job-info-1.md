---
description: В \_ структуре сведений о задании \_ 1 указаны сведения о задании печати, такие как значение идентификатора задания, имя принтера, для которого задано Постановка задания, имя компьютера, создавшего задание печати, имя пользователя, владеющего заданием печати, и т. д.
ms.assetid: d42ada89-6bc7-4006-81d9-dbcc0347edd3
title: Структура JOB_INFO_1 (Винспул. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- JOB_INFO_1
- _JOB_INFO_1A
- _JOB_INFO_1W
api_type:
- HeaderDef
api_location:
- Winspool.h
ms.openlocfilehash: d56d4d6bce15a661ce141d8e22d27a15837a9f6f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "104349082"
---
# <a name="job_info_1-structure"></a><span data-ttu-id="e4b68-103">\_Структура сведений о задании \_ 1</span><span class="sxs-lookup"><span data-stu-id="e4b68-103">JOB\_INFO\_1 structure</span></span>

<span data-ttu-id="e4b68-104">В **структуре \_ сведений \_ о** задании 1 указаны сведения о задании печати, такие как значение идентификатора задания, имя принтера, для которого задано Постановка задания, имя компьютера, создавшего задание печати, имя пользователя, владеющего заданием печати, и т. д.</span><span class="sxs-lookup"><span data-stu-id="e4b68-104">The **JOB\_INFO\_1** structure specifies print-job information such as the job-identifier value, the name of the printer for which the job is spooled, the name of the machine that created the print job, the name of the user that owns the print job, and so on.</span></span>

## <a name="syntax"></a><span data-ttu-id="e4b68-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="e4b68-105">Syntax</span></span>


```C++
typedef struct _JOB_INFO_1 {
  DWORD      JobId;
  LPTSTR     pPrinterName;
  LPTSTR     pMachineName;
  LPTSTR     pUserName;
  LPTSTR     pDocument;
  LPTSTR     pDatatype;
  LPTSTR     pStatus;
  DWORD      Status;
  DWORD      Priority;
  DWORD      Position;
  DWORD      TotalPages;
  DWORD      PagesPrinted;
  SYSTEMTIME Submitted;
} JOB_INFO_1, *PJOB_INFO_1;
```



## <a name="members"></a><span data-ttu-id="e4b68-106">Члены</span><span class="sxs-lookup"><span data-stu-id="e4b68-106">Members</span></span>

<dl> <dt>

<span data-ttu-id="e4b68-107">**JobId**</span><span class="sxs-lookup"><span data-stu-id="e4b68-107">**JobId**</span></span>
</dt> <dd>

<span data-ttu-id="e4b68-108">Идентификатор задания.</span><span class="sxs-lookup"><span data-stu-id="e4b68-108">A job identifier.</span></span>

</dd> <dt>

<span data-ttu-id="e4b68-109">**ппринтернаме**</span><span class="sxs-lookup"><span data-stu-id="e4b68-109">**pPrinterName**</span></span>
</dt> <dd>

<span data-ttu-id="e4b68-110">Указатель на строку, завершающуюся нулем, которая указывает имя принтера, для которого задано постановка в очередь.</span><span class="sxs-lookup"><span data-stu-id="e4b68-110">A pointer to a null-terminated string that specifies the name of the printer for which the job is spooled.</span></span>

</dd> <dt>

<span data-ttu-id="e4b68-111">**пмачиненаме**</span><span class="sxs-lookup"><span data-stu-id="e4b68-111">**pMachineName**</span></span>
</dt> <dd>

<span data-ttu-id="e4b68-112">Указатель на строку, завершающуюся нулем, которая указывает имя компьютера, создавшего задание печати.</span><span class="sxs-lookup"><span data-stu-id="e4b68-112">A pointer to a null-terminated string that specifies the name of the machine that created the print job.</span></span>

</dd> <dt>

<span data-ttu-id="e4b68-113">**пусернаме**</span><span class="sxs-lookup"><span data-stu-id="e4b68-113">**pUserName**</span></span>
</dt> <dd>

<span data-ttu-id="e4b68-114">Указатель на строку, завершающуюся нулем, которая указывает имя пользователя, владеющего заданием печати.</span><span class="sxs-lookup"><span data-stu-id="e4b68-114">A pointer to a null-terminated string that specifies the name of the user that owns the print job.</span></span>

</dd> <dt>

<span data-ttu-id="e4b68-115">**пдокумент**</span><span class="sxs-lookup"><span data-stu-id="e4b68-115">**pDocument**</span></span>
</dt> <dd>

<span data-ttu-id="e4b68-116">Указатель на строку, завершающуюся нулем, которая указывает имя задания печати (например, MS-WORD: Review.doc).</span><span class="sxs-lookup"><span data-stu-id="e4b68-116">A pointer to a null-terminated string that specifies the name of the print job (for example, "MS-WORD: Review.doc").</span></span>

</dd> <dt>

<span data-ttu-id="e4b68-117">**пдататипе**</span><span class="sxs-lookup"><span data-stu-id="e4b68-117">**pDatatype**</span></span>
</dt> <dd>

<span data-ttu-id="e4b68-118">Указатель на строку, завершающуюся нулем, которая указывает тип данных, используемых для записи задания печати.</span><span class="sxs-lookup"><span data-stu-id="e4b68-118">A pointer to a null-terminated string that specifies the type of data used to record the print job.</span></span>

</dd> <dt>

<span data-ttu-id="e4b68-119">**пстатус**</span><span class="sxs-lookup"><span data-stu-id="e4b68-119">**pStatus**</span></span>
</dt> <dd>

<span data-ttu-id="e4b68-120">Указатель на строку, завершающуюся нулем, которая указывает состояние задания печати.</span><span class="sxs-lookup"><span data-stu-id="e4b68-120">A pointer to a null-terminated string that specifies the status of the print job.</span></span> <span data-ttu-id="e4b68-121">Этот элемент должен быть проверен до *состояния* , и, если *Пстатус* имеет **значение NULL**, состояние определяется содержимым элемента Status.</span><span class="sxs-lookup"><span data-stu-id="e4b68-121">This member should be checked prior to *Status* and, if *pStatus* is **NULL**, the status is defined by the contents of the Status member.</span></span>

</dd> <dt>

<span data-ttu-id="e4b68-122">**Состояние**</span><span class="sxs-lookup"><span data-stu-id="e4b68-122">**Status**</span></span>
</dt> <dd>

<span data-ttu-id="e4b68-123">Состояние задания.</span><span class="sxs-lookup"><span data-stu-id="e4b68-123">The job status.</span></span> <span data-ttu-id="e4b68-124">Значением этого элемента может быть ноль или сочетание одного или нескольких из следующих значений.</span><span class="sxs-lookup"><span data-stu-id="e4b68-124">The value of this member can be zero or a combination of one or more of the following values.</span></span> <span data-ttu-id="e4b68-125">Нулевое значение указывает, что очередь печати была приостановлена после завершения печати документа.</span><span class="sxs-lookup"><span data-stu-id="e4b68-125">A value of zero indicates that the print queue was paused after the document finished spooling.</span></span>



| <span data-ttu-id="e4b68-126">Значение</span><span class="sxs-lookup"><span data-stu-id="e4b68-126">Value</span></span>                           | <span data-ttu-id="e4b68-127">Значение</span><span class="sxs-lookup"><span data-stu-id="e4b68-127">Meaning</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                                                                     |
|---------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="e4b68-128">\_состояние задания \_ заблокировано \_ девк</span><span class="sxs-lookup"><span data-stu-id="e4b68-128">JOB\_STATUS\_BLOCKED\_DEVQ</span></span>      | <span data-ttu-id="e4b68-129">Драйвер не может напечатать задание.</span><span class="sxs-lookup"><span data-stu-id="e4b68-129">The driver cannot print the job.</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                                            |
| <span data-ttu-id="e4b68-130">\_состояние задания \_ завершено</span><span class="sxs-lookup"><span data-stu-id="e4b68-130">JOB\_STATUS\_COMPLETE</span></span>           | <span data-ttu-id="e4b68-131">**Windows XP и более поздние версии:** Задание отправляется на принтер, но задание может быть еще не напечатано.</span><span class="sxs-lookup"><span data-stu-id="e4b68-131">**Windows XP and later:** Job is sent to the printer, but the job may not be printed yet.</span></span><br/> <span data-ttu-id="e4b68-132">Дополнительные сведения см. в разделе "Примечания".</span><span class="sxs-lookup"><span data-stu-id="e4b68-132">See Remarks for more information.</span></span><br/>                                                                                                                                                                                                                                                                                                                           |
| <span data-ttu-id="e4b68-133">\_состояние задания \_ удалено</span><span class="sxs-lookup"><span data-stu-id="e4b68-133">JOB\_STATUS\_DELETED</span></span>            | <span data-ttu-id="e4b68-134">Задание удалено.</span><span class="sxs-lookup"><span data-stu-id="e4b68-134">Job has been deleted.</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                                                       |
| <span data-ttu-id="e4b68-135">\_удаление состояния \_ задания</span><span class="sxs-lookup"><span data-stu-id="e4b68-135">JOB\_STATUS\_DELETING</span></span>           | <span data-ttu-id="e4b68-136">Идет удаление задания.</span><span class="sxs-lookup"><span data-stu-id="e4b68-136">Job is being deleted.</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                                                       |
| <span data-ttu-id="e4b68-137">\_Ошибка состояния \_ задания</span><span class="sxs-lookup"><span data-stu-id="e4b68-137">JOB\_STATUS\_ERROR</span></span>              | <span data-ttu-id="e4b68-138">С заданием связана ошибка.</span><span class="sxs-lookup"><span data-stu-id="e4b68-138">An error is associated with the job.</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                                        |
| <span data-ttu-id="e4b68-139">состояние задания в \_ \_ автономном режиме</span><span class="sxs-lookup"><span data-stu-id="e4b68-139">JOB\_STATUS\_OFFLINE</span></span>            | <span data-ttu-id="e4b68-140">Принтер находится в автономном режиме.</span><span class="sxs-lookup"><span data-stu-id="e4b68-140">Printer is offline.</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                                                         |
| <span data-ttu-id="e4b68-141">\_Бумага состояния \_ задания</span><span class="sxs-lookup"><span data-stu-id="e4b68-141">JOB\_STATUS\_PAPEROUT</span></span>           | <span data-ttu-id="e4b68-142">В принтере нет бумаги.</span><span class="sxs-lookup"><span data-stu-id="e4b68-142">Printer is out of paper.</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                                                    |
| <span data-ttu-id="e4b68-143">\_состояние задания \_ приостановлено</span><span class="sxs-lookup"><span data-stu-id="e4b68-143">JOB\_STATUS\_PAUSED</span></span>             | <span data-ttu-id="e4b68-144">Задание приостановлено.</span><span class="sxs-lookup"><span data-stu-id="e4b68-144">Job is paused.</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                                                              |
| <span data-ttu-id="e4b68-145">\_состояние задания \_ напечатано</span><span class="sxs-lookup"><span data-stu-id="e4b68-145">JOB\_STATUS\_PRINTED</span></span>            | <span data-ttu-id="e4b68-146">Задание напечатано.</span><span class="sxs-lookup"><span data-stu-id="e4b68-146">Job has printed.</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                                                            |
| <span data-ttu-id="e4b68-147">\_Печать состояния \_ задания</span><span class="sxs-lookup"><span data-stu-id="e4b68-147">JOB\_STATUS\_PRINTING</span></span>           | <span data-ttu-id="e4b68-148">Идет печать задания.</span><span class="sxs-lookup"><span data-stu-id="e4b68-148">Job is printing.</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                                                            |
| <span data-ttu-id="e4b68-149">\_перезапуск состояния \_ задания</span><span class="sxs-lookup"><span data-stu-id="e4b68-149">JOB\_STATUS\_RESTART</span></span>            | <span data-ttu-id="e4b68-150">Задание перезапущено.</span><span class="sxs-lookup"><span data-stu-id="e4b68-150">Job has been restarted.</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                                                     |
| <span data-ttu-id="e4b68-151">состояние задания — " \_ \_ сохранены"</span><span class="sxs-lookup"><span data-stu-id="e4b68-151">JOB\_STATUS\_RETAINED</span></span>           | <span data-ttu-id="e4b68-152">**Windows Vista и более поздние версии:** Задание было сохранено в очереди печати и не может быть удалено.</span><span class="sxs-lookup"><span data-stu-id="e4b68-152">**Windows Vista and later:** Job has been retained in the print queue and cannot be deleted.</span></span> <span data-ttu-id="e4b68-153">Это может быть вызвано следующими проблемами:</span><span class="sxs-lookup"><span data-stu-id="e4b68-153">This can be caused by the following:</span></span><br/> <span data-ttu-id="e4b68-154">1) задание было вручную сохранено вызовом Сетжоб, а диспетчер очереди печати ожидает освобождения задания.</span><span class="sxs-lookup"><span data-stu-id="e4b68-154">1) The job was manually retained by a call to SetJob and the spooler is waiting for the job to be released.</span></span><br/> <span data-ttu-id="e4b68-155">2) задание не завершило печать и должно завершить печать, прежде чем его можно будет удалить автоматически.</span><span class="sxs-lookup"><span data-stu-id="e4b68-155">2) The job has not finished printing and must finish printing before it can be automatically deleted.</span></span><br/> <span data-ttu-id="e4b68-156">Дополнительные сведения о командах задания печати см. в разделе [**сетжоб**](setjob.md) .</span><span class="sxs-lookup"><span data-stu-id="e4b68-156">See [**SetJob**](setjob.md) for more information about print job commands.</span></span><br/> |
| <span data-ttu-id="e4b68-157">\_очередь состояний \_ заданий</span><span class="sxs-lookup"><span data-stu-id="e4b68-157">JOB\_STATUS\_SPOOLING</span></span>           | <span data-ttu-id="e4b68-158">Задание находится в очереди.</span><span class="sxs-lookup"><span data-stu-id="e4b68-158">Job is spooling.</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                                                            |
| <span data-ttu-id="e4b68-159">\_состояние задания \_ — \_ вмешательство пользователя</span><span class="sxs-lookup"><span data-stu-id="e4b68-159">JOB\_STATUS\_USER\_INTERVENTION</span></span> | <span data-ttu-id="e4b68-160">В принтере есть ошибка, которая требует от пользователя выполнить какие-либо действия.</span><span class="sxs-lookup"><span data-stu-id="e4b68-160">Printer has an error that requires the user to do something.</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                |



 

</dd> <dt>

<span data-ttu-id="e4b68-161">**Приоритет**</span><span class="sxs-lookup"><span data-stu-id="e4b68-161">**Priority**</span></span>
</dt> <dd>

<span data-ttu-id="e4b68-162">Приоритет задания.</span><span class="sxs-lookup"><span data-stu-id="e4b68-162">The job priority.</span></span> <span data-ttu-id="e4b68-163">Этот элемент может принимать одно из следующих значений или находиться в диапазоне от 1 до 99 (от МИНИМАЛЬного \_ приоритета до максимального \_ приоритета).</span><span class="sxs-lookup"><span data-stu-id="e4b68-163">This member can be one of the following values or in the range between 1 through 99 (MIN\_PRIORITY through MAX\_PRIORITY).</span></span>



| <span data-ttu-id="e4b68-164">Значение</span><span class="sxs-lookup"><span data-stu-id="e4b68-164">Value</span></span>         | <span data-ttu-id="e4b68-165">Значение</span><span class="sxs-lookup"><span data-stu-id="e4b68-165">Meaning</span></span>           |
|---------------|-------------------|
| <span data-ttu-id="e4b68-166">Минимальный \_ приоритет</span><span class="sxs-lookup"><span data-stu-id="e4b68-166">MIN\_PRIORITY</span></span> | <span data-ttu-id="e4b68-167">Минимальный приоритет.</span><span class="sxs-lookup"><span data-stu-id="e4b68-167">Minimum priority.</span></span> |
| <span data-ttu-id="e4b68-168">МАКСИМАЛЬНЫЙ \_ приоритет</span><span class="sxs-lookup"><span data-stu-id="e4b68-168">MAX\_PRIORITY</span></span> | <span data-ttu-id="e4b68-169">Максимальный приоритет.</span><span class="sxs-lookup"><span data-stu-id="e4b68-169">Maximum priority.</span></span> |
| <span data-ttu-id="e4b68-170">\_приоритет DEF</span><span class="sxs-lookup"><span data-stu-id="e4b68-170">DEF\_PRIORITY</span></span> | <span data-ttu-id="e4b68-171">Приоритет по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="e4b68-171">Default priority.</span></span> |



 

</dd> <dt>

<span data-ttu-id="e4b68-172">**Позиция**</span><span class="sxs-lookup"><span data-stu-id="e4b68-172">**Position**</span></span>
</dt> <dd>

<span data-ttu-id="e4b68-173">Расположение задания в очереди печати.</span><span class="sxs-lookup"><span data-stu-id="e4b68-173">The job's position in the print queue.</span></span>

</dd> <dt>

<span data-ttu-id="e4b68-174">**TotalPages**</span><span class="sxs-lookup"><span data-stu-id="e4b68-174">**TotalPages**</span></span>
</dt> <dd>

<span data-ttu-id="e4b68-175">Общее число страниц, содержащихся в документе.</span><span class="sxs-lookup"><span data-stu-id="e4b68-175">The total number of pages that the document contains.</span></span> <span data-ttu-id="e4b68-176">Это значение может быть равно нулю, если задание печати не содержит сведений об разделителе страниц.</span><span class="sxs-lookup"><span data-stu-id="e4b68-176">This value may be zero if the print job does not contain page delimiting information.</span></span>

</dd> <dt>

<span data-ttu-id="e4b68-177">**пажеспринтед**</span><span class="sxs-lookup"><span data-stu-id="e4b68-177">**PagesPrinted**</span></span>
</dt> <dd>

<span data-ttu-id="e4b68-178">Число напечатанных страниц.</span><span class="sxs-lookup"><span data-stu-id="e4b68-178">The number of pages that have printed.</span></span> <span data-ttu-id="e4b68-179">Это значение может быть равно нулю, если задание печати не содержит сведений об разделителе страниц.</span><span class="sxs-lookup"><span data-stu-id="e4b68-179">This value may be zero if the print job does not contain page delimiting information.</span></span>

</dd> <dt>

<span data-ttu-id="e4b68-180">**Отправлено**</span><span class="sxs-lookup"><span data-stu-id="e4b68-180">**Submitted**</span></span>
</dt> <dd>

<span data-ttu-id="e4b68-181">Структура [**SYSTEMTIME**](/windows/desktop/api/minwinbase/ns-minwinbase-systemtime) , указывающая время, когда документ был помещен в очередь.</span><span class="sxs-lookup"><span data-stu-id="e4b68-181">A [**SYSTEMTIME**](/windows/desktop/api/minwinbase/ns-minwinbase-systemtime) structure that specifies the time that this document was spooled.</span></span>

<span data-ttu-id="e4b68-182">Это значение времени указано в формате универсальной координаты времени (UTC).</span><span class="sxs-lookup"><span data-stu-id="e4b68-182">This time value is in Universal Time Coordinate (UTC) format.</span></span> <span data-ttu-id="e4b68-183">Перед отображением его необходимо преобразовать в местное значение времени.</span><span class="sxs-lookup"><span data-stu-id="e4b68-183">You should convert it to a local time value before displaying it.</span></span> <span data-ttu-id="e4b68-184">Для выполнения преобразования можно использовать функцию [**филетиметолокалфилетиме**](/windows/desktop/api/fileapi/nf-fileapi-filetimetolocalfiletime) .</span><span class="sxs-lookup"><span data-stu-id="e4b68-184">You can use the [**FileTimeToLocalFileTime**](/windows/desktop/api/fileapi/nf-fileapi-filetimetolocalfiletime) function to perform the conversion.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="e4b68-185">Комментарии</span><span class="sxs-lookup"><span data-stu-id="e4b68-185">Remarks</span></span>

<span data-ttu-id="e4b68-186">Мониторы портов, не поддерживающие Труиндофжоб, задают задание как \_ состояние задания, \_ напечатанное сразу после отправки задания на принтер.</span><span class="sxs-lookup"><span data-stu-id="e4b68-186">Port monitors that do not support TrueEndOfJob will set the job as JOB\_STATUS\_PRINTED right after the job is submitted to the printer.</span></span>

## <a name="requirements"></a><span data-ttu-id="e4b68-187">Требования</span><span class="sxs-lookup"><span data-stu-id="e4b68-187">Requirements</span></span>



| <span data-ttu-id="e4b68-188">Требование</span><span class="sxs-lookup"><span data-stu-id="e4b68-188">Requirement</span></span> | <span data-ttu-id="e4b68-189">Значение</span><span class="sxs-lookup"><span data-stu-id="e4b68-189">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="e4b68-190">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="e4b68-190">Minimum supported client</span></span><br/> | <span data-ttu-id="e4b68-191">Windows 2000 Professional \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="e4b68-191">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                                |
| <span data-ttu-id="e4b68-192">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="e4b68-192">Minimum supported server</span></span><br/> | <span data-ttu-id="e4b68-193">Windows 2000 Server \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="e4b68-193">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                      |
| <span data-ttu-id="e4b68-194">Заголовок</span><span class="sxs-lookup"><span data-stu-id="e4b68-194">Header</span></span><br/>                   | <dl> <span data-ttu-id="e4b68-195"><dt>Винспул. h (включение Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="e4b68-195"><dt>Winspool.h (include Windows.h)</dt></span></span> </dl> |
| <span data-ttu-id="e4b68-196">Имя в кодировке Юникод и ANSI</span><span class="sxs-lookup"><span data-stu-id="e4b68-196">Unicode and ANSI names</span></span><br/>   | <span data-ttu-id="e4b68-197">**\_ \_ Сведения о \_ задании 1W** (Юникод) и **\_ \_ сведения о задании \_ 1A** (ANSI)</span><span class="sxs-lookup"><span data-stu-id="e4b68-197">**\_JOB\_INFO\_1W** (Unicode) and **\_JOB\_INFO\_1A** (ANSI)</span></span><br/>                                   |



## <a name="see-also"></a><span data-ttu-id="e4b68-198">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="e4b68-198">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e4b68-199">Вывод на печать</span><span class="sxs-lookup"><span data-stu-id="e4b68-199">Printing</span></span>](printdocs-printing.md)
</dt> <dt>

[<span data-ttu-id="e4b68-200">Структуры API диспетчера очереди печати</span><span class="sxs-lookup"><span data-stu-id="e4b68-200">Print Spooler API Structures</span></span>](printing-and-print-spooler-structures.md)
</dt> <dt>

[<span data-ttu-id="e4b68-201">**енумжобс**</span><span class="sxs-lookup"><span data-stu-id="e4b68-201">**EnumJobs**</span></span>](enumjobs.md)
</dt> <dt>

[<span data-ttu-id="e4b68-202">**жетжоб**</span><span class="sxs-lookup"><span data-stu-id="e4b68-202">**GetJob**</span></span>](getjob.md)
</dt> <dt>

[<span data-ttu-id="e4b68-203">**сетжоб**</span><span class="sxs-lookup"><span data-stu-id="e4b68-203">**SetJob**</span></span>](setjob.md)
</dt> </dl>

 

