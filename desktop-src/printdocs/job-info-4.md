---
description: Описывает полный набор значений, связанных с заданием, и поддерживает большие файлы очереди с размерами, которые выражаются с 64 битами.
ms.assetid: 90932ae2-ea9e-43bc-9a1d-c68223f6d0ee
title: Структура JOB_INFO_4 (Винспул. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- JOB_INFO_4
- _JOB_INFO_4A
- _JOB_INFO_4W
api_type:
- HeaderDef
api_location:
- Winspool.h
ms.openlocfilehash: 5a6ccd7bf589ed341c9aceab86205cd9852c0896
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "105647687"
---
# <a name="job_info_4-structure"></a><span data-ttu-id="6c28c-103">\_Структура сведений о задании \_ 4</span><span class="sxs-lookup"><span data-stu-id="6c28c-103">JOB\_INFO\_4 structure</span></span>

<span data-ttu-id="6c28c-104">Описывает полный набор значений, связанных с заданием, и поддерживает большие файлы очереди с размерами, которые выражаются с 64 битами.</span><span class="sxs-lookup"><span data-stu-id="6c28c-104">Describes a full set of values associated with a job and supports large spool files with sizes expressed with 64 bits.</span></span>

## <a name="syntax"></a><span data-ttu-id="6c28c-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="6c28c-105">Syntax</span></span>


```C++
typedef struct _JOB_INFO_4 {
  DWORD                JobId;
  LPTSTR               pPrinterName;
  LPTSTR               pMachineName;
  LPTSTR               pUserName;
  LPTSTR               pDocument;
  LPTSTR               pNotifyName;
  LPTSTR               pDatatype;
  LPTSTR               pPrintProcessor;
  LPTSTR               pParameters;
  LPTSTR               pDriverName;
  LPDEVMODE            pDevMode;
  LPTSTR               pStatus;
  PSECURITY_DESCRIPTOR pSecurityDescriptor;
  DWORD                Status;
  DWORD                Priority;
  DWORD                Position;
  DWORD                StartTime;
  DWORD                UntilTime;
  DWORD                TotalPages;
  DWORD                Size;
  SYSTEMTIME           Submitted;
  DWORD                Time;
  DWORD                PagesPrinted;
  LONG                 SizeHigh;
} JOB_INFO_4, *PJOB_INFO_4;
```



## <a name="members"></a><span data-ttu-id="6c28c-106">Члены</span><span class="sxs-lookup"><span data-stu-id="6c28c-106">Members</span></span>

<dl> <dt>

<span data-ttu-id="6c28c-107">**JobId**</span><span class="sxs-lookup"><span data-stu-id="6c28c-107">**JobId**</span></span>
</dt> <dd>

<span data-ttu-id="6c28c-108">Значение идентификатора задания.</span><span class="sxs-lookup"><span data-stu-id="6c28c-108">A job identifier value.</span></span>

</dd> <dt>

<span data-ttu-id="6c28c-109">**ппринтернаме**</span><span class="sxs-lookup"><span data-stu-id="6c28c-109">**pPrinterName**</span></span>
</dt> <dd>

<span data-ttu-id="6c28c-110">Указатель на строку, завершающуюся нулем, которая указывает имя принтера, для которого задано постановка в очередь.</span><span class="sxs-lookup"><span data-stu-id="6c28c-110">A pointer to a null-terminated string that specifies the name of the printer for which the job is spooled.</span></span>

</dd> <dt>

<span data-ttu-id="6c28c-111">**пмачиненаме**</span><span class="sxs-lookup"><span data-stu-id="6c28c-111">**pMachineName**</span></span>
</dt> <dd>

<span data-ttu-id="6c28c-112">Указатель на строку, завершающуюся нулем, которая указывает имя компьютера, создавшего задание печати.</span><span class="sxs-lookup"><span data-stu-id="6c28c-112">A pointer to a null-terminated string that specifies the name of the machine that created the print job.</span></span>

</dd> <dt>

<span data-ttu-id="6c28c-113">**пусернаме**</span><span class="sxs-lookup"><span data-stu-id="6c28c-113">**pUserName**</span></span>
</dt> <dd>

<span data-ttu-id="6c28c-114">Указатель на строку, завершающуюся нулем, которая указывает имя пользователя, владеющего заданием печати.</span><span class="sxs-lookup"><span data-stu-id="6c28c-114">A pointer to a null-terminated string that specifies the name of the user who owns the print job.</span></span>

</dd> <dt>

<span data-ttu-id="6c28c-115">**пдокумент**</span><span class="sxs-lookup"><span data-stu-id="6c28c-115">**pDocument**</span></span>
</dt> <dd>

<span data-ttu-id="6c28c-116">Указатель на строку, завершающуюся нулем, которая указывает имя задания печати (например, MS-WORD: Review.doc).</span><span class="sxs-lookup"><span data-stu-id="6c28c-116">A pointer to a null-terminated string that specifies the name of the print job (for example, "MS-WORD: Review.doc").</span></span>

</dd> <dt>

<span data-ttu-id="6c28c-117">**пнотифинаме**</span><span class="sxs-lookup"><span data-stu-id="6c28c-117">**pNotifyName**</span></span>
</dt> <dd>

<span data-ttu-id="6c28c-118">Указатель на строку, завершающуюся нулем, которая указывает имя пользователя, который должен получать уведомления при печати задания или при возникновении ошибки во время печати задания.</span><span class="sxs-lookup"><span data-stu-id="6c28c-118">A pointer to a null-terminated string that specifies the name of the user who should be notified when the job has been printed, or when an error occurs while printing the job.</span></span>

</dd> <dt>

<span data-ttu-id="6c28c-119">**пдататипе**</span><span class="sxs-lookup"><span data-stu-id="6c28c-119">**pDatatype**</span></span>
</dt> <dd>

<span data-ttu-id="6c28c-120">Указатель на строку, завершающуюся нулем, которая указывает тип данных, используемых для записи задания печати.</span><span class="sxs-lookup"><span data-stu-id="6c28c-120">A pointer to a null-terminated string that specifies the type of data used to record the print job.</span></span>

</dd> <dt>

<span data-ttu-id="6c28c-121">**ппринтпроцессор**</span><span class="sxs-lookup"><span data-stu-id="6c28c-121">**pPrintProcessor**</span></span>
</dt> <dd>

<span data-ttu-id="6c28c-122">Указатель на строку, завершающуюся нулем, которая указывает имя обработчика печати, который должен использоваться для печати задания.</span><span class="sxs-lookup"><span data-stu-id="6c28c-122">A pointer to a null-terminated string that specifies the name of the print processor that should be used to print the job.</span></span>

</dd> <dt>

<span data-ttu-id="6c28c-123">**ппараметерс**</span><span class="sxs-lookup"><span data-stu-id="6c28c-123">**pParameters**</span></span>
</dt> <dd>

<span data-ttu-id="6c28c-124">Указатель на строку, завершающуюся нулем, указывающую параметры процессора печати.</span><span class="sxs-lookup"><span data-stu-id="6c28c-124">A pointer to a null-terminated string that specifies print-processor parameters.</span></span>

</dd> <dt>

<span data-ttu-id="6c28c-125">**пдривернаме**</span><span class="sxs-lookup"><span data-stu-id="6c28c-125">**pDriverName**</span></span>
</dt> <dd>

<span data-ttu-id="6c28c-126">Указатель на строку, завершающуюся нулем, которая указывает имя драйвера принтера, который должен использоваться для обработки задания печати.</span><span class="sxs-lookup"><span data-stu-id="6c28c-126">A pointer to a null-terminated string that specifies the name of the printer driver that should be used to process the print job.</span></span>

</dd> <dt>

<span data-ttu-id="6c28c-127">**пдевмоде**</span><span class="sxs-lookup"><span data-stu-id="6c28c-127">**pDevMode**</span></span>
</dt> <dd>

<span data-ttu-id="6c28c-128">Указатель на структуру [**DEVMODE**](/windows/win32/api/wingdi/ns-wingdi-devmodea) , которая содержит данные об инициализации устройства и среде для драйвера принтера.</span><span class="sxs-lookup"><span data-stu-id="6c28c-128">A pointer to a [**DEVMODE**](/windows/win32/api/wingdi/ns-wingdi-devmodea) structure that contains device-initialization and environment data for the printer driver.</span></span>

</dd> <dt>

<span data-ttu-id="6c28c-129">**пстатус**</span><span class="sxs-lookup"><span data-stu-id="6c28c-129">**pStatus**</span></span>
</dt> <dd>

<span data-ttu-id="6c28c-130">Указатель на строку, завершающуюся нулем, которая указывает состояние задания печати.</span><span class="sxs-lookup"><span data-stu-id="6c28c-130">A pointer to a null-terminated string that specifies the status of the print job.</span></span> <span data-ttu-id="6c28c-131">Этот элемент должен быть проверен до **состояния** , и, если **Пстатус** имеет **значение NULL**, состояние определяется содержимым элемента Status.</span><span class="sxs-lookup"><span data-stu-id="6c28c-131">This member should be checked prior to **Status** and, if **pStatus** is **NULL**, the status is defined by the contents of the Status member.</span></span>

</dd> <dt>

<span data-ttu-id="6c28c-132">**псекуритидескриптор**</span><span class="sxs-lookup"><span data-stu-id="6c28c-132">**pSecurityDescriptor**</span></span>
</dt> <dd>

<span data-ttu-id="6c28c-133">Значение этого элемента равно **null**.</span><span class="sxs-lookup"><span data-stu-id="6c28c-133">The value of this member is **NULL**.</span></span> <span data-ttu-id="6c28c-134">Извлечение и настройка дескрипторов безопасности документов в этом выпуске не поддерживается.</span><span class="sxs-lookup"><span data-stu-id="6c28c-134">Retrieval and setting of document security descriptors is not supported in this release.</span></span>

</dd> <dt>

<span data-ttu-id="6c28c-135">**Состояние**</span><span class="sxs-lookup"><span data-stu-id="6c28c-135">**Status**</span></span>
</dt> <dd>

<span data-ttu-id="6c28c-136">Состояние задания.</span><span class="sxs-lookup"><span data-stu-id="6c28c-136">The job status.</span></span> <span data-ttu-id="6c28c-137">Этот элемент может иметь одно или несколько следующих значений:</span><span class="sxs-lookup"><span data-stu-id="6c28c-137">This member can be one or more of the following values:</span></span>

| <span data-ttu-id="6c28c-138">Значение</span><span class="sxs-lookup"><span data-stu-id="6c28c-138">Value</span></span>                           | <span data-ttu-id="6c28c-139">Значение</span><span class="sxs-lookup"><span data-stu-id="6c28c-139">Meaning</span></span>                                                      |
|---------------------------------|--------------------------------------------------------------|
| <span data-ttu-id="6c28c-140">\_состояние задания \_ заблокировано \_ девк</span><span class="sxs-lookup"><span data-stu-id="6c28c-140">JOB\_STATUS\_BLOCKED\_DEVQ</span></span>      | <span data-ttu-id="6c28c-141">Драйвер не может напечатать задание.</span><span class="sxs-lookup"><span data-stu-id="6c28c-141">The driver cannot print the job.</span></span>                             |
| <span data-ttu-id="6c28c-142">\_состояние задания \_ удалено</span><span class="sxs-lookup"><span data-stu-id="6c28c-142">JOB\_STATUS\_DELETED</span></span>            | <span data-ttu-id="6c28c-143">Задание удалено.</span><span class="sxs-lookup"><span data-stu-id="6c28c-143">Job has been deleted.</span></span>                                        |
| <span data-ttu-id="6c28c-144">\_удаление состояния \_ задания</span><span class="sxs-lookup"><span data-stu-id="6c28c-144">JOB\_STATUS\_DELETING</span></span>           | <span data-ttu-id="6c28c-145">Идет удаление задания.</span><span class="sxs-lookup"><span data-stu-id="6c28c-145">Job is being deleted.</span></span>                                        |
| <span data-ttu-id="6c28c-146">\_Ошибка состояния \_ задания</span><span class="sxs-lookup"><span data-stu-id="6c28c-146">JOB\_STATUS\_ERROR</span></span>              | <span data-ttu-id="6c28c-147">С заданием связана ошибка.</span><span class="sxs-lookup"><span data-stu-id="6c28c-147">An error is associated with the job.</span></span>                         |
| <span data-ttu-id="6c28c-148">состояние задания в \_ \_ автономном режиме</span><span class="sxs-lookup"><span data-stu-id="6c28c-148">JOB\_STATUS\_OFFLINE</span></span>            | <span data-ttu-id="6c28c-149">Принтер находится в автономном режиме.</span><span class="sxs-lookup"><span data-stu-id="6c28c-149">Printer is offline.</span></span>                                          |
| <span data-ttu-id="6c28c-150">\_Бумага состояния \_ задания</span><span class="sxs-lookup"><span data-stu-id="6c28c-150">JOB\_STATUS\_PAPEROUT</span></span>           | <span data-ttu-id="6c28c-151">В принтере нет бумаги.</span><span class="sxs-lookup"><span data-stu-id="6c28c-151">Printer is out of paper.</span></span>                                     |
| <span data-ttu-id="6c28c-152">\_состояние задания \_ приостановлено</span><span class="sxs-lookup"><span data-stu-id="6c28c-152">JOB\_STATUS\_PAUSED</span></span>             | <span data-ttu-id="6c28c-153">Задание приостановлено.</span><span class="sxs-lookup"><span data-stu-id="6c28c-153">Job is paused.</span></span>                                               |
| <span data-ttu-id="6c28c-154">\_состояние задания \_ напечатано</span><span class="sxs-lookup"><span data-stu-id="6c28c-154">JOB\_STATUS\_PRINTED</span></span>            | <span data-ttu-id="6c28c-155">Задание напечатано.</span><span class="sxs-lookup"><span data-stu-id="6c28c-155">Job has printed.</span></span>                                             |
| <span data-ttu-id="6c28c-156">\_Печать состояния \_ задания</span><span class="sxs-lookup"><span data-stu-id="6c28c-156">JOB\_STATUS\_PRINTING</span></span>           | <span data-ttu-id="6c28c-157">Идет печать задания.</span><span class="sxs-lookup"><span data-stu-id="6c28c-157">Job is printing.</span></span>                                             |
| <span data-ttu-id="6c28c-158">\_перезапуск состояния \_ задания</span><span class="sxs-lookup"><span data-stu-id="6c28c-158">JOB\_STATUS\_RESTART</span></span>            | <span data-ttu-id="6c28c-159">Задание перезапущено.</span><span class="sxs-lookup"><span data-stu-id="6c28c-159">Job has been restarted.</span></span>                                      |
| <span data-ttu-id="6c28c-160">\_очередь состояний \_ заданий</span><span class="sxs-lookup"><span data-stu-id="6c28c-160">JOB\_STATUS\_SPOOLING</span></span>           | <span data-ttu-id="6c28c-161">Задание находится в очереди.</span><span class="sxs-lookup"><span data-stu-id="6c28c-161">Job is spooling.</span></span>                                             |
| <span data-ttu-id="6c28c-162">\_состояние задания \_ — \_ вмешательство пользователя</span><span class="sxs-lookup"><span data-stu-id="6c28c-162">JOB\_STATUS\_USER\_INTERVENTION</span></span> | <span data-ttu-id="6c28c-163">В принтере есть ошибка, которая требует от пользователя выполнить какие-либо действия.</span><span class="sxs-lookup"><span data-stu-id="6c28c-163">Printer has an error that requires the user to do something.</span></span> |



 

<span data-ttu-id="6c28c-164">В Windows XP и более поздних версиях Windows также можно использовать следующие значения:</span><span class="sxs-lookup"><span data-stu-id="6c28c-164">In Windows XP and later versions of Windows, the following values can also be used:</span></span>

| <span data-ttu-id="6c28c-165">Значение</span><span class="sxs-lookup"><span data-stu-id="6c28c-165">Value</span></span>                 | <span data-ttu-id="6c28c-166">Значение</span><span class="sxs-lookup"><span data-stu-id="6c28c-166">Meaning</span></span>                                                                                       |
|-----------------------|-----------------------------------------------------------------------------------------------|
| <span data-ttu-id="6c28c-167">\_состояние задания \_ завершено</span><span class="sxs-lookup"><span data-stu-id="6c28c-167">JOB\_STATUS\_COMPLETE</span></span> | <span data-ttu-id="6c28c-168">Задание отправляется на принтер, но может быть еще не напечатано.</span><span class="sxs-lookup"><span data-stu-id="6c28c-168">The job is sent to the printer, but may not be printed yet.</span></span> <span data-ttu-id="6c28c-169">Дополнительные сведения см. в разделе "Примечания".</span><span class="sxs-lookup"><span data-stu-id="6c28c-169">See Remarks for more information.</span></span> |
| <span data-ttu-id="6c28c-170">состояние задания — " \_ \_ сохранены"</span><span class="sxs-lookup"><span data-stu-id="6c28c-170">JOB\_STATUS\_RETAINED</span></span> | <span data-ttu-id="6c28c-171">Задание было сохранено в очереди печати после печати.</span><span class="sxs-lookup"><span data-stu-id="6c28c-171">The job has been retained in the print queue following printing.</span></span>                              |



 

</dd> <dt>

<span data-ttu-id="6c28c-172">**Приоритет**</span><span class="sxs-lookup"><span data-stu-id="6c28c-172">**Priority**</span></span>
</dt> <dd>

<span data-ttu-id="6c28c-173">Приоритет задания.</span><span class="sxs-lookup"><span data-stu-id="6c28c-173">The job priority.</span></span> <span data-ttu-id="6c28c-174">Этот элемент может принимать одно из следующих значений или находиться в диапазоне от 1 до 99 (от МИНИМАЛЬного \_ приоритета до максимального \_ приоритета).</span><span class="sxs-lookup"><span data-stu-id="6c28c-174">This member can be one of the following values, or in the range between 1 through 99 (MIN\_PRIORITY through MAX\_PRIORITY).</span></span>



| <span data-ttu-id="6c28c-175">Значение</span><span class="sxs-lookup"><span data-stu-id="6c28c-175">Value</span></span>         | <span data-ttu-id="6c28c-176">Значение</span><span class="sxs-lookup"><span data-stu-id="6c28c-176">Meaning</span></span>           |
|---------------|-------------------|
| <span data-ttu-id="6c28c-177">Минимальный \_ приоритет</span><span class="sxs-lookup"><span data-stu-id="6c28c-177">MIN\_PRIORITY</span></span> | <span data-ttu-id="6c28c-178">Минимальный приоритет.</span><span class="sxs-lookup"><span data-stu-id="6c28c-178">Minimum priority.</span></span> |
| <span data-ttu-id="6c28c-179">МАКСИМАЛЬНЫЙ \_ приоритет</span><span class="sxs-lookup"><span data-stu-id="6c28c-179">MAX\_PRIORITY</span></span> | <span data-ttu-id="6c28c-180">Максимальный приоритет.</span><span class="sxs-lookup"><span data-stu-id="6c28c-180">Maximum priority.</span></span> |
| <span data-ttu-id="6c28c-181">\_приоритет DEF</span><span class="sxs-lookup"><span data-stu-id="6c28c-181">DEF\_PRIORITY</span></span> | <span data-ttu-id="6c28c-182">Приоритет по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="6c28c-182">Default priority.</span></span> |



 

</dd> <dt>

<span data-ttu-id="6c28c-183">**Позиция**</span><span class="sxs-lookup"><span data-stu-id="6c28c-183">**Position**</span></span>
</dt> <dd>

<span data-ttu-id="6c28c-184">Расположение задания в очереди печати.</span><span class="sxs-lookup"><span data-stu-id="6c28c-184">The job's position in the print queue.</span></span>

</dd> <dt>

<span data-ttu-id="6c28c-185">**StartTime**</span><span class="sxs-lookup"><span data-stu-id="6c28c-185">**StartTime**</span></span>
</dt> <dd>

<span data-ttu-id="6c28c-186">Самое раннее время, когда может быть распечатано задание.</span><span class="sxs-lookup"><span data-stu-id="6c28c-186">The earliest time that the job can be printed.</span></span>

</dd> <dt>

<span data-ttu-id="6c28c-187">**унтилтиме**</span><span class="sxs-lookup"><span data-stu-id="6c28c-187">**UntilTime**</span></span>
</dt> <dd>

<span data-ttu-id="6c28c-188">Последнее время, когда задание может быть напечатано.</span><span class="sxs-lookup"><span data-stu-id="6c28c-188">The latest time that the job can be printed.</span></span>

</dd> <dt>

<span data-ttu-id="6c28c-189">**TotalPages**</span><span class="sxs-lookup"><span data-stu-id="6c28c-189">**TotalPages**</span></span>
</dt> <dd>

<span data-ttu-id="6c28c-190">Количество страниц, необходимых для задания.</span><span class="sxs-lookup"><span data-stu-id="6c28c-190">The number of pages required for the job.</span></span> <span data-ttu-id="6c28c-191">Это значение может быть равно нулю, если задание печати не содержит сведений об разделителе страниц.</span><span class="sxs-lookup"><span data-stu-id="6c28c-191">This value may be zero if the print job does not contain page delimiting information.</span></span>

</dd> <dt>

<span data-ttu-id="6c28c-192">**Размер**</span><span class="sxs-lookup"><span data-stu-id="6c28c-192">**Size**</span></span>
</dt> <dd>

<span data-ttu-id="6c28c-193">Младшие четыре байта задания (в байтах).</span><span class="sxs-lookup"><span data-stu-id="6c28c-193">The lower four bytes of the size, in bytes, of the job.</span></span> <span data-ttu-id="6c28c-194">См. также элемент **сизехигх** ниже.</span><span class="sxs-lookup"><span data-stu-id="6c28c-194">See also the **SizeHigh** member below.</span></span>

</dd> <dt>

<span data-ttu-id="6c28c-195">**Отправлено**</span><span class="sxs-lookup"><span data-stu-id="6c28c-195">**Submitted**</span></span>
</dt> <dd>

<span data-ttu-id="6c28c-196">Структура [**SYSTEMTIME**](/windows/desktop/api/minwinbase/ns-minwinbase-systemtime) , указывающая время отправки задания.</span><span class="sxs-lookup"><span data-stu-id="6c28c-196">A [**SYSTEMTIME**](/windows/desktop/api/minwinbase/ns-minwinbase-systemtime) structure that specifies the time when the job was submitted.</span></span>

<span data-ttu-id="6c28c-197">Это значение времени указано в формате универсальной координаты времени (UTC).</span><span class="sxs-lookup"><span data-stu-id="6c28c-197">This time value is in Universal Time Coordinate (UTC) format.</span></span> <span data-ttu-id="6c28c-198">Перед отображением его необходимо преобразовать в местное значение времени.</span><span class="sxs-lookup"><span data-stu-id="6c28c-198">You should convert it to a local time value before displaying it.</span></span> <span data-ttu-id="6c28c-199">Для выполнения преобразования можно использовать функцию [**филетиметолокалфилетиме**](/windows/desktop/api/fileapi/nf-fileapi-filetimetolocalfiletime) .</span><span class="sxs-lookup"><span data-stu-id="6c28c-199">You can use the [**FileTimeToLocalFileTime**](/windows/desktop/api/fileapi/nf-fileapi-filetimetolocalfiletime) function to perform the conversion.</span></span>

</dd> <dt>

<span data-ttu-id="6c28c-200">**Time**</span><span class="sxs-lookup"><span data-stu-id="6c28c-200">**Time**</span></span>
</dt> <dd>

<span data-ttu-id="6c28c-201">Общее время (в миллисекундах), прошедшее с момента начала печати задания.</span><span class="sxs-lookup"><span data-stu-id="6c28c-201">The total time, in milliseconds, that has elapsed since the job began printing.</span></span>

</dd> <dt>

<span data-ttu-id="6c28c-202">**пажеспринтед**</span><span class="sxs-lookup"><span data-stu-id="6c28c-202">**PagesPrinted**</span></span>
</dt> <dd>

<span data-ttu-id="6c28c-203">Число напечатанных страниц.</span><span class="sxs-lookup"><span data-stu-id="6c28c-203">The number of pages that have printed.</span></span> <span data-ttu-id="6c28c-204">Это значение может быть равно нулю, если задание печати не содержит сведений об разделителе страниц.</span><span class="sxs-lookup"><span data-stu-id="6c28c-204">This value may be zero if the print job does not contain page delimiting information.</span></span>

</dd> <dt>

<span data-ttu-id="6c28c-205">**сизехигх**</span><span class="sxs-lookup"><span data-stu-id="6c28c-205">**SizeHigh**</span></span>
</dt> <dd>

<span data-ttu-id="6c28c-206">Старшие четыре байта для задания (в байтах).</span><span class="sxs-lookup"><span data-stu-id="6c28c-206">The higher four bytes of the size, in bytes, of the job.</span></span> <span data-ttu-id="6c28c-207">См. также элемент **size** выше.</span><span class="sxs-lookup"><span data-stu-id="6c28c-207">See also the **Size** member above.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="6c28c-208">Комментарии</span><span class="sxs-lookup"><span data-stu-id="6c28c-208">Remarks</span></span>

<span data-ttu-id="6c28c-209">Мониторы портов, не поддерживающие Труиндофжоб, задают задание как \_ состояние задания, \_ выводимое сразу после отправки задания на принтер.</span><span class="sxs-lookup"><span data-stu-id="6c28c-209">Port monitors that do not support TrueEndOfJob will set the job as JOB\_STATUS\_PRINTED immediately after the job is submitted to the printer.</span></span>

## <a name="requirements"></a><span data-ttu-id="6c28c-210">Требования</span><span class="sxs-lookup"><span data-stu-id="6c28c-210">Requirements</span></span>



| <span data-ttu-id="6c28c-211">Требование</span><span class="sxs-lookup"><span data-stu-id="6c28c-211">Requirement</span></span> | <span data-ttu-id="6c28c-212">Значение</span><span class="sxs-lookup"><span data-stu-id="6c28c-212">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="6c28c-213">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="6c28c-213">Minimum supported client</span></span><br/> | <span data-ttu-id="6c28c-214">Windows 2000 Professional \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="6c28c-214">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                            |
| <span data-ttu-id="6c28c-215">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="6c28c-215">Minimum supported server</span></span><br/> | <span data-ttu-id="6c28c-216">Windows 2000 Server \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="6c28c-216">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="6c28c-217">Заголовок</span><span class="sxs-lookup"><span data-stu-id="6c28c-217">Header</span></span><br/>                   | <dl> <span data-ttu-id="6c28c-218"><dt>Винспул. h</dt></span><span class="sxs-lookup"><span data-stu-id="6c28c-218"><dt>Winspool.h</dt></span></span> </dl> |
| <span data-ttu-id="6c28c-219">Имя в кодировке Юникод и ANSI</span><span class="sxs-lookup"><span data-stu-id="6c28c-219">Unicode and ANSI names</span></span><br/>   | <span data-ttu-id="6c28c-220">**\_ \_ Сведения о \_ задании 4W** (Юникод) и **\_ \_ сведения о задании \_ 4A** (ANSI)</span><span class="sxs-lookup"><span data-stu-id="6c28c-220">**\_JOB\_INFO\_4W** (Unicode) and **\_JOB\_INFO\_4A** (ANSI)</span></span><br/>               |



## <a name="see-also"></a><span data-ttu-id="6c28c-221">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="6c28c-221">See also</span></span>

<dl> <dt>

[<span data-ttu-id="6c28c-222">Вывод на печать</span><span class="sxs-lookup"><span data-stu-id="6c28c-222">Printing</span></span>](printdocs-printing.md)
</dt> <dt>

[<span data-ttu-id="6c28c-223">Структуры API диспетчера очереди печати</span><span class="sxs-lookup"><span data-stu-id="6c28c-223">Print Spooler API Structures</span></span>](printing-and-print-spooler-structures.md)
</dt> <dt>

[<span data-ttu-id="6c28c-224">**DEVMODE**</span><span class="sxs-lookup"><span data-stu-id="6c28c-224">**DEVMODE**</span></span>](/windows/win32/api/wingdi/ns-wingdi-devmodea)
</dt> <dt>

[<span data-ttu-id="6c28c-225">**енумжобс**</span><span class="sxs-lookup"><span data-stu-id="6c28c-225">**EnumJobs**</span></span>](enumjobs.md)
</dt> <dt>

[<span data-ttu-id="6c28c-226">**жетжоб**</span><span class="sxs-lookup"><span data-stu-id="6c28c-226">**GetJob**</span></span>](getjob.md)
</dt> <dt>

[<span data-ttu-id="6c28c-227">**сетжоб**</span><span class="sxs-lookup"><span data-stu-id="6c28c-227">**SetJob**</span></span>](setjob.md)
</dt> </dl>

 

