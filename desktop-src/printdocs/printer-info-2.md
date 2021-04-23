---
description: В структуре "сведения о ПРИНТЕРе \_ \_ 2" указаны подробные сведения о принтере.
ms.assetid: 944cbfcd-9edf-4b60-a45c-9bb1839f8141
title: Структура PRINTER_INFO_2 (Винспул. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- PRINTER_INFO_2
- _PRINTER_INFO_2A
- _PRINTER_INFO_2W
api_type:
- HeaderDef
api_location:
- Winspool.h
ms.openlocfilehash: b299cb1bbdd3ac2475b7a9f2b600bcd9652246d7
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "104546367"
---
# <a name="printer_info_2-structure"></a><span data-ttu-id="53564-103">\_Сведения о принтере \_ 2 Структура</span><span class="sxs-lookup"><span data-stu-id="53564-103">PRINTER\_INFO\_2 structure</span></span>

<span data-ttu-id="53564-104">В структуре " **сведения о принтере \_ \_ 2** " указаны подробные сведения о принтере.</span><span class="sxs-lookup"><span data-stu-id="53564-104">The **PRINTER\_INFO\_2** structure specifies detailed printer information.</span></span>

## <a name="syntax"></a><span data-ttu-id="53564-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="53564-105">Syntax</span></span>


```C++
typedef struct _PRINTER_INFO_2 {
  LPTSTR               pServerName;
  LPTSTR               pPrinterName;
  LPTSTR               pShareName;
  LPTSTR               pPortName;
  LPTSTR               pDriverName;
  LPTSTR               pComment;
  LPTSTR               pLocation;
  LPDEVMODE            pDevMode;
  LPTSTR               pSepFile;
  LPTSTR               pPrintProcessor;
  LPTSTR               pDatatype;
  LPTSTR               pParameters;
  PSECURITY_DESCRIPTOR pSecurityDescriptor;
  DWORD                Attributes;
  DWORD                Priority;
  DWORD                DefaultPriority;
  DWORD                StartTime;
  DWORD                UntilTime;
  DWORD                Status;
  DWORD                cJobs;
  DWORD                AveragePPM;
} PRINTER_INFO_2, *PPRINTER_INFO_2;
```



## <a name="members"></a><span data-ttu-id="53564-106">Члены</span><span class="sxs-lookup"><span data-stu-id="53564-106">Members</span></span>

<dl> <dt>

<span data-ttu-id="53564-107">**псервернаме**</span><span class="sxs-lookup"><span data-stu-id="53564-107">**pServerName**</span></span>
</dt> <dd>

<span data-ttu-id="53564-108">Указатель на строку, завершающуюся нулем, определяющую сервер, управляющий принтером.</span><span class="sxs-lookup"><span data-stu-id="53564-108">A pointer to a null-terminated string identifying the server that controls the printer.</span></span> <span data-ttu-id="53564-109">Если эта строка имеет **значение NULL**, управление принтером осуществляется локально.</span><span class="sxs-lookup"><span data-stu-id="53564-109">If this string is **NULL**, the printer is controlled locally.</span></span>

</dd> <dt>

<span data-ttu-id="53564-110">**ппринтернаме**</span><span class="sxs-lookup"><span data-stu-id="53564-110">**pPrinterName**</span></span>
</dt> <dd>

<span data-ttu-id="53564-111">Указатель на строку, завершающуюся нулем, которая указывает имя принтера.</span><span class="sxs-lookup"><span data-stu-id="53564-111">A pointer to a null-terminated string that specifies the name of the printer.</span></span>

</dd> <dt>

<span data-ttu-id="53564-112">**пшаренаме**</span><span class="sxs-lookup"><span data-stu-id="53564-112">**pShareName**</span></span>
</dt> <dd>

<span data-ttu-id="53564-113">Указатель на строку, завершающуюся нулем, которая обозначает общую точку для принтера.</span><span class="sxs-lookup"><span data-stu-id="53564-113">A pointer to a null-terminated string that identifies the share point for the printer.</span></span> <span data-ttu-id="53564-114">(Эта строка используется только в том случае, если принтер \_ \_Для элемента **Attributes** задана общая константа атрибута.)</span><span class="sxs-lookup"><span data-stu-id="53564-114">(This string is used only if the PRINTER\_ATTRIBUTE\_SHARED constant was set for the **Attributes** member.)</span></span>

</dd> <dt>

<span data-ttu-id="53564-115">**ппортнаме**</span><span class="sxs-lookup"><span data-stu-id="53564-115">**pPortName**</span></span>
</dt> <dd>

<span data-ttu-id="53564-116">Указатель на строку, завершающуюся нулем, которая определяет порты, используемые для передачи данных на принтер.</span><span class="sxs-lookup"><span data-stu-id="53564-116">A pointer to a null-terminated string that identifies the port(s) used to transmit data to the printer.</span></span> <span data-ttu-id="53564-117">Если принтер подключен к нескольким портам, имена каждого порта должны быть разделены запятыми (например, "LPT1:, LPT2:, LPT3:").</span><span class="sxs-lookup"><span data-stu-id="53564-117">If a printer is connected to more than one port, the names of each port must be separated by commas (for example, "LPT1:,LPT2:,LPT3:").</span></span>

</dd> <dt>

<span data-ttu-id="53564-118">**пдривернаме**</span><span class="sxs-lookup"><span data-stu-id="53564-118">**pDriverName**</span></span>
</dt> <dd>

<span data-ttu-id="53564-119">Указатель на строку, завершающуюся нулем, которая указывает имя драйвера принтера.</span><span class="sxs-lookup"><span data-stu-id="53564-119">A pointer to a null-terminated string that specifies the name of the printer driver.</span></span>

</dd> <dt>

<span data-ttu-id="53564-120">**пкоммент**</span><span class="sxs-lookup"><span data-stu-id="53564-120">**pComment**</span></span>
</dt> <dd>

<span data-ttu-id="53564-121">Указатель на строку, завершающуюся нулем, которая предоставляет краткое описание принтера.</span><span class="sxs-lookup"><span data-stu-id="53564-121">A pointer to a null-terminated string that provides a brief description of the printer.</span></span>

</dd> <dt>

<span data-ttu-id="53564-122">**плокатион**</span><span class="sxs-lookup"><span data-stu-id="53564-122">**pLocation**</span></span>
</dt> <dd>

<span data-ttu-id="53564-123">Указатель на строку, завершающуюся нулем, которая указывает физическое расположение принтера (например, "Блдг.</span><span class="sxs-lookup"><span data-stu-id="53564-123">A pointer to a null-terminated string that specifies the physical location of the printer (for example, "Bldg.</span></span> <span data-ttu-id="53564-124">38, комната 1164 ").</span><span class="sxs-lookup"><span data-stu-id="53564-124">38, Room 1164").</span></span>

</dd> <dt>

<span data-ttu-id="53564-125">**пдевмоде**</span><span class="sxs-lookup"><span data-stu-id="53564-125">**pDevMode**</span></span>
</dt> <dd>

<span data-ttu-id="53564-126">Указатель на структуру [**DEVMODE**](/windows/win32/api/wingdi/ns-wingdi-devmodea) , которая определяет данные принтера по умолчанию, такие как ориентация бумаги и разрешение.</span><span class="sxs-lookup"><span data-stu-id="53564-126">A pointer to a [**DEVMODE**](/windows/win32/api/wingdi/ns-wingdi-devmodea) structure that defines default printer data such as the paper orientation and the resolution.</span></span>

</dd> <dt>

<span data-ttu-id="53564-127">**псепфиле**</span><span class="sxs-lookup"><span data-stu-id="53564-127">**pSepFile**</span></span>
</dt> <dd>

<span data-ttu-id="53564-128">Указатель на строку, завершающуюся нулем, которая указывает имя файла, используемого для создания страницы-разделителя.</span><span class="sxs-lookup"><span data-stu-id="53564-128">A pointer to a null-terminated string that specifies the name of the file used to create the separator page.</span></span> <span data-ttu-id="53564-129">Эта страница используется для разделения заданий печати, отправленных на принтер.</span><span class="sxs-lookup"><span data-stu-id="53564-129">This page is used to separate print jobs sent to the printer.</span></span>

</dd> <dt>

<span data-ttu-id="53564-130">**ппринтпроцессор**</span><span class="sxs-lookup"><span data-stu-id="53564-130">**pPrintProcessor**</span></span>
</dt> <dd>

<span data-ttu-id="53564-131">Указатель на строку, завершающуюся нулем, которая указывает имя обработчика печати, используемого принтером.</span><span class="sxs-lookup"><span data-stu-id="53564-131">A pointer to a null-terminated string that specifies the name of the print processor used by the printer.</span></span> <span data-ttu-id="53564-132">Для получения списка обработчиков печати, установленных на сервере, можно использовать функцию [**енумпринтпроцессорс**](enumprintprocessors.md) .</span><span class="sxs-lookup"><span data-stu-id="53564-132">You can use the [**EnumPrintProcessors**](enumprintprocessors.md) function to obtain a list of print processors installed on a server.</span></span>

</dd> <dt>

<span data-ttu-id="53564-133">**пдататипе**</span><span class="sxs-lookup"><span data-stu-id="53564-133">**pDatatype**</span></span>
</dt> <dd>

<span data-ttu-id="53564-134">Указатель на строку, завершающуюся нулем, которая указывает тип данных, используемый для записи задания печати.</span><span class="sxs-lookup"><span data-stu-id="53564-134">A pointer to a null-terminated string that specifies the data type used to record the print job.</span></span> <span data-ttu-id="53564-135">Для получения списка типов данных, поддерживаемых конкретным обработчиком печати, можно использовать функцию [**енумпринтпроцессордататипес**](enumprintprocessordatatypes.md) .</span><span class="sxs-lookup"><span data-stu-id="53564-135">You can use the [**EnumPrintProcessorDatatypes**](enumprintprocessordatatypes.md) function to obtain a list of data types supported by a specific print processor.</span></span>

</dd> <dt>

<span data-ttu-id="53564-136">**ппараметерс**</span><span class="sxs-lookup"><span data-stu-id="53564-136">**pParameters**</span></span>
</dt> <dd>

<span data-ttu-id="53564-137">Указатель на строку, завершающуюся нулем, которая указывает параметры обработчика печати по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="53564-137">A pointer to a null-terminated string that specifies the default print-processor parameters.</span></span>

</dd> <dt>

<span data-ttu-id="53564-138">**псекуритидескриптор**</span><span class="sxs-lookup"><span data-stu-id="53564-138">**pSecurityDescriptor**</span></span>
</dt> <dd>

<span data-ttu-id="53564-139">Указатель на структуру [**\_ дескриптора безопасности**](/windows/desktop/api/winnt/ns-winnt-security_descriptor) для принтера.</span><span class="sxs-lookup"><span data-stu-id="53564-139">A pointer to a [**SECURITY\_DESCRIPTOR**](/windows/desktop/api/winnt/ns-winnt-security_descriptor) structure for the printer.</span></span> <span data-ttu-id="53564-140">Этот элемент может иметь **значение NULL**.</span><span class="sxs-lookup"><span data-stu-id="53564-140">This member may be **NULL**.</span></span>

</dd> <dt>

<span data-ttu-id="53564-141">**Атрибуты**</span><span class="sxs-lookup"><span data-stu-id="53564-141">**Attributes**</span></span>
</dt> <dd>

<span data-ttu-id="53564-142">Атрибуты принтера.</span><span class="sxs-lookup"><span data-stu-id="53564-142">The printer attributes.</span></span> <span data-ttu-id="53564-143">Этот элемент может быть любым разумным сочетанием следующих значений.</span><span class="sxs-lookup"><span data-stu-id="53564-143">This member can be any reasonable combination of the following values.</span></span>

| <span data-ttu-id="53564-144">Значение</span><span class="sxs-lookup"><span data-stu-id="53564-144">Value</span></span>                                   | <span data-ttu-id="53564-145">Значение</span><span class="sxs-lookup"><span data-stu-id="53564-145">Meaning</span></span>                                                                                                                                                                                 |
|-----------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="53564-146">атрибут «принтер» \_ \_ Direct</span><span class="sxs-lookup"><span data-stu-id="53564-146">PRINTER\_ATTRIBUTE\_DIRECT</span></span>              | <span data-ttu-id="53564-147">Задание отправляется непосредственно на принтер (он не помещается в очередь).</span><span class="sxs-lookup"><span data-stu-id="53564-147">Job is sent directly to the printer (it is not spooled).</span></span>                                                                                                                                |
| <span data-ttu-id="53564-148">\_ \_ \_ сначала необходимо выполнить атрибут \_ Printer</span><span class="sxs-lookup"><span data-stu-id="53564-148">PRINTER\_ATTRIBUTE\_DO\_COMPLETE\_FIRST</span></span> | <span data-ttu-id="53564-149">Если для параметра задать и принтер задано значение печать во время очереди печати, то все задания, для которых была завершена буферизация, будут распечатываться перед заданиями, которые не завершают работу с очередью.</span><span class="sxs-lookup"><span data-stu-id="53564-149">If set and printer is set for print-while-spooling, any jobs that have completed spooling are scheduled to print before jobs that have not completed spooling.</span></span>                          |
| <span data-ttu-id="53564-150">\_атрибут принтера \_ Enable \_ девк</span><span class="sxs-lookup"><span data-stu-id="53564-150">PRINTER\_ATTRIBUTE\_ENABLE\_DEVQ</span></span>        | <span data-ttu-id="53564-151">Если задано значение, вызывается **девкуерипринт** .</span><span class="sxs-lookup"><span data-stu-id="53564-151">If set, **DevQueryPrint** is called.</span></span> <span data-ttu-id="53564-152">**Девкуерипринт** может завершиться ошибкой, если настройки документа и принтера не совпадают.</span><span class="sxs-lookup"><span data-stu-id="53564-152">**DevQueryPrint** may fail if the document and printer setups do not match.</span></span> <span data-ttu-id="53564-153">Установка этого флага приводит к тому, что документы не будут храниться в очереди.</span><span class="sxs-lookup"><span data-stu-id="53564-153">Setting this flag causes mismatched documents to be held in the queue.</span></span> |
| <span data-ttu-id="53564-154">\_атрибут принтера \_ скрыт</span><span class="sxs-lookup"><span data-stu-id="53564-154">PRINTER\_ATTRIBUTE\_HIDDEN</span></span>              | <span data-ttu-id="53564-155">Зарезервировано.</span><span class="sxs-lookup"><span data-stu-id="53564-155">Reserved.</span></span>                                                                                                                                                                               |
| <span data-ttu-id="53564-156">\_киппринтеджобс атрибута \_ принтера</span><span class="sxs-lookup"><span data-stu-id="53564-156">PRINTER\_ATTRIBUTE\_KEEPPRINTEDJOBS</span></span>     | <span data-ttu-id="53564-157">Если задано, задания сохраняются после печати.</span><span class="sxs-lookup"><span data-stu-id="53564-157">If set, jobs are kept after they are printed.</span></span> <span data-ttu-id="53564-158">Если не задано, задания удаляются.</span><span class="sxs-lookup"><span data-stu-id="53564-158">If unset, jobs are deleted.</span></span>                                                                                                               |
| <span data-ttu-id="53564-159">\_локальный атрибут \_ принтера</span><span class="sxs-lookup"><span data-stu-id="53564-159">PRINTER\_ATTRIBUTE\_LOCAL</span></span>               | <span data-ttu-id="53564-160">Принтер является локальным принтером.</span><span class="sxs-lookup"><span data-stu-id="53564-160">Printer is a local printer.</span></span>                                                                                                                                                             |
| <span data-ttu-id="53564-161">\_сеть АТРИБУТОВ \_ принтера</span><span class="sxs-lookup"><span data-stu-id="53564-161">PRINTER\_ATTRIBUTE\_NETWORK</span></span>             | <span data-ttu-id="53564-162">Принтер является подключением к сетевому принтеру.</span><span class="sxs-lookup"><span data-stu-id="53564-162">Printer is a network printer connection.</span></span>                                                                                                                                                |
| <span data-ttu-id="53564-163">\_атрибут принтера \_ опубликован</span><span class="sxs-lookup"><span data-stu-id="53564-163">PRINTER\_ATTRIBUTE\_PUBLISHED</span></span>           | <span data-ttu-id="53564-164">Указывает, опубликован ли принтер в службе каталогов.</span><span class="sxs-lookup"><span data-stu-id="53564-164">Indicates whether the printer is published in the directory service.</span></span>                                                                                                                    |
| <span data-ttu-id="53564-165">\_атрибут принтера \_ поставлен в очередь</span><span class="sxs-lookup"><span data-stu-id="53564-165">PRINTER\_ATTRIBUTE\_QUEUED</span></span>              | <span data-ttu-id="53564-166">Если задано, принтер помещается в очередь и начинает печать после постановки в очередь последней страницы.</span><span class="sxs-lookup"><span data-stu-id="53564-166">If set, the printer spools and starts printing after the last page is spooled.</span></span> <span data-ttu-id="53564-167">Если параметр не установлен и \_ атрибут принтера \_ Direct не задан, принтер помещается в очередь и печатается при постановке в очередь.</span><span class="sxs-lookup"><span data-stu-id="53564-167">If not set and PRINTER\_ATTRIBUTE\_DIRECT is not set, the printer spools and prints while spooling.</span></span>      |
| <span data-ttu-id="53564-168">\_только атрибут принтера \_ RAW \_</span><span class="sxs-lookup"><span data-stu-id="53564-168">PRINTER\_ATTRIBUTE\_RAW\_ONLY</span></span>           | <span data-ttu-id="53564-169">Указывает, что только задания печати необработанного типа данных могут быть поставлены в очередь.</span><span class="sxs-lookup"><span data-stu-id="53564-169">Indicates that only raw data type print jobs can be spooled.</span></span>                                                                                                                            |
| <span data-ttu-id="53564-170">\_общий атрибут \_ принтера</span><span class="sxs-lookup"><span data-stu-id="53564-170">PRINTER\_ATTRIBUTE\_SHARED</span></span>              | <span data-ttu-id="53564-171">Принтер является общим.</span><span class="sxs-lookup"><span data-stu-id="53564-171">Printer is shared.</span></span>                                                                                                                                                                      |



 

<span data-ttu-id="53564-172">В Windows XP и более поздних версиях Windows также можно использовать следующее значение.</span><span class="sxs-lookup"><span data-stu-id="53564-172">In Windows XP and later versions of Windows, the following value can also be used.</span></span>

| <span data-ttu-id="53564-173">Значение</span><span class="sxs-lookup"><span data-stu-id="53564-173">Value</span></span>                   | <span data-ttu-id="53564-174">Значение</span><span class="sxs-lookup"><span data-stu-id="53564-174">Meaning</span></span>                                                                                                                                                                                           |
|-------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="53564-175">\_Факс атрибута \_ принтера</span><span class="sxs-lookup"><span data-stu-id="53564-175">PRINTER\_ATTRIBUTE\_FAX</span></span> | <span data-ttu-id="53564-176">Если задано, то принтер является принтером факсов.</span><span class="sxs-lookup"><span data-stu-id="53564-176">If set, printer is a fax printer.</span></span> <span data-ttu-id="53564-177">Это значение может быть задано только параметром [**аддпринтер**](addprinter.md), но его можно получить с помощью [**енумпринтерс**](enumprinters.md) [**и**](getprinter.md).</span><span class="sxs-lookup"><span data-stu-id="53564-177">This can only be set by [**AddPrinter**](addprinter.md), but it can be retrieved by [**EnumPrinters**](enumprinters.md) and [**GetPrinter**](getprinter.md).</span></span> |



 

<span data-ttu-id="53564-178">В Windows Vista и более поздних версиях Windows также можно использовать следующие значения.</span><span class="sxs-lookup"><span data-stu-id="53564-178">In Windows Vista and later versions of Windows, the following values can also be used.</span></span>

| <span data-ttu-id="53564-179">Значение</span><span class="sxs-lookup"><span data-stu-id="53564-179">Value</span></span>                               | <span data-ttu-id="53564-180">Значение</span><span class="sxs-lookup"><span data-stu-id="53564-180">Meaning</span></span>                                                                          |
|-------------------------------------|----------------------------------------------------------------------------------|
| <span data-ttu-id="53564-181">\_ \_ понятное имя атрибута принтера \_</span><span class="sxs-lookup"><span data-stu-id="53564-181">PRINTER\_ATTRIBUTE\_FRIENDLY\_NAME</span></span>  | <span data-ttu-id="53564-182">Компьютер подключился к принтеру и получил понятное имя.</span><span class="sxs-lookup"><span data-stu-id="53564-182">A computer has connected to this printer and given it a friendly name.</span></span>           |
| <span data-ttu-id="53564-183">\_компьютер с атрибутом принтера \_</span><span class="sxs-lookup"><span data-stu-id="53564-183">PRINTER\_ATTRIBUTE\_MACHINE</span></span>         | <span data-ttu-id="53564-184">Принтер является подключением для каждого компьютера.</span><span class="sxs-lookup"><span data-stu-id="53564-184">Printer is a per-machine connection.</span></span>                                             |
| <span data-ttu-id="53564-185">атрибут принтера, \_ \_ отправленный \_ пользователем</span><span class="sxs-lookup"><span data-stu-id="53564-185">PRINTER\_ATTRIBUTE\_PUSHED\_USER</span></span>    | <span data-ttu-id="53564-186">Принтер был установлен с помощью политики пользователя "принудительное подключение к принтеру".</span><span class="sxs-lookup"><span data-stu-id="53564-186">The printer was installed by using the Push Printer Connections user policy.</span></span>     |
| <span data-ttu-id="53564-187">атрибут принтера, \_ \_ отправленный на \_ компьютер</span><span class="sxs-lookup"><span data-stu-id="53564-187">PRINTER\_ATTRIBUTE\_PUSHED\_MACHINE</span></span> | <span data-ttu-id="53564-188">Принтер был установлен с помощью политики компьютера Push-подключения принтера.</span><span class="sxs-lookup"><span data-stu-id="53564-188">The printer was installed by using the Push Printer Connections computer policy.</span></span> |



 

<span data-ttu-id="53564-189">В Windows Server 2003 также можно использовать следующее значение.</span><span class="sxs-lookup"><span data-stu-id="53564-189">In Windows Server 2003, the following value can also be used.</span></span>

| <span data-ttu-id="53564-190">Значение</span><span class="sxs-lookup"><span data-stu-id="53564-190">Value</span></span>                  | <span data-ttu-id="53564-191">Значение</span><span class="sxs-lookup"><span data-stu-id="53564-191">Meaning</span></span>                                                                 |
|------------------------|-------------------------------------------------------------------------|
| <span data-ttu-id="53564-192">\_атрибут принтера \_ TS</span><span class="sxs-lookup"><span data-stu-id="53564-192">PRINTER\_ATTRIBUTE\_TS</span></span> | <span data-ttu-id="53564-193">Указывает, что принтер в настоящее время подключен через сервер терминалов.</span><span class="sxs-lookup"><span data-stu-id="53564-193">Indicates the printer is currently connected through a terminal server.</span></span> |



 

</dd> <dt>

<span data-ttu-id="53564-194">**Приоритет**</span><span class="sxs-lookup"><span data-stu-id="53564-194">**Priority**</span></span>
</dt> <dd>

<span data-ttu-id="53564-195">Значение приоритета, используемое диспетчером очереди для маршрутизации заданий печати.</span><span class="sxs-lookup"><span data-stu-id="53564-195">A priority value that the spooler uses to route print jobs.</span></span>

</dd> <dt>

<span data-ttu-id="53564-196">**дефаултприорити**</span><span class="sxs-lookup"><span data-stu-id="53564-196">**DefaultPriority**</span></span>
</dt> <dd>

<span data-ttu-id="53564-197">Значение приоритета по умолчанию, назначенное каждому заданию печати.</span><span class="sxs-lookup"><span data-stu-id="53564-197">The default priority value assigned to each print job.</span></span>

</dd> <dt>

<span data-ttu-id="53564-198">**StartTime**</span><span class="sxs-lookup"><span data-stu-id="53564-198">**StartTime**</span></span>
</dt> <dd>

<span data-ttu-id="53564-199">Самое раннее время, когда принтер будет печатать задание.</span><span class="sxs-lookup"><span data-stu-id="53564-199">The earliest time at which the printer will print a job.</span></span> <span data-ttu-id="53564-200">Это значение выражается в минутах, истекшем с 12:00 AM GMT (время по Гринвичу).</span><span class="sxs-lookup"><span data-stu-id="53564-200">This value is expressed as minutes elapsed since 12:00 AM GMT (Greenwich Mean Time).</span></span>

</dd> <dt>

<span data-ttu-id="53564-201">**унтилтиме**</span><span class="sxs-lookup"><span data-stu-id="53564-201">**UntilTime**</span></span>
</dt> <dd>

<span data-ttu-id="53564-202">Последнее время, когда принтер будет печатать задание.</span><span class="sxs-lookup"><span data-stu-id="53564-202">The latest time at which the printer will print a job.</span></span> <span data-ttu-id="53564-203">Это значение выражается в минутах, истекшем с 12:00 AM GMT (время по Гринвичу).</span><span class="sxs-lookup"><span data-stu-id="53564-203">This value is expressed as minutes elapsed since 12:00 AM GMT (Greenwich Mean Time).</span></span>

</dd> <dt>

<span data-ttu-id="53564-204">**Состояние**</span><span class="sxs-lookup"><span data-stu-id="53564-204">**Status**</span></span>
</dt> <dd>

<span data-ttu-id="53564-205">Состояние принтера.</span><span class="sxs-lookup"><span data-stu-id="53564-205">The printer status.</span></span> <span data-ttu-id="53564-206">Этот элемент может быть любым разумным сочетанием следующих значений.</span><span class="sxs-lookup"><span data-stu-id="53564-206">This member can be any reasonable combination of the following values.</span></span>



| <span data-ttu-id="53564-207">Значение</span><span class="sxs-lookup"><span data-stu-id="53564-207">Value</span></span>                               | <span data-ttu-id="53564-208">Значение</span><span class="sxs-lookup"><span data-stu-id="53564-208">Meaning</span></span>                                                          |
|-------------------------------------|------------------------------------------------------------------|
| <span data-ttu-id="53564-209">\_состояние принтера \_ занято</span><span class="sxs-lookup"><span data-stu-id="53564-209">PRINTER\_STATUS\_BUSY</span></span>               | <span data-ttu-id="53564-210">Принтер занят.</span><span class="sxs-lookup"><span data-stu-id="53564-210">The printer is busy.</span></span>                                             |
| <span data-ttu-id="53564-211">\_ \_ открыта дверца состояния принтера \_</span><span class="sxs-lookup"><span data-stu-id="53564-211">PRINTER\_STATUS\_DOOR\_OPEN</span></span>         | <span data-ttu-id="53564-212">Открыта дверца принтера.</span><span class="sxs-lookup"><span data-stu-id="53564-212">The printer door is open.</span></span>                                        |
| <span data-ttu-id="53564-213">\_Ошибка состояния \_ принтера</span><span class="sxs-lookup"><span data-stu-id="53564-213">PRINTER\_STATUS\_ERROR</span></span>              | <span data-ttu-id="53564-214">Принтер находится в состоянии ошибки.</span><span class="sxs-lookup"><span data-stu-id="53564-214">The printer is in an error state.</span></span>                                |
| <span data-ttu-id="53564-215">\_ \_ Инициализация состояния принтера</span><span class="sxs-lookup"><span data-stu-id="53564-215">PRINTER\_STATUS\_INITIALIZING</span></span>       | <span data-ttu-id="53564-216">Идет инициализация принтера.</span><span class="sxs-lookup"><span data-stu-id="53564-216">The printer is initializing.</span></span>                                     |
| <span data-ttu-id="53564-217">\_Активный статус \_ ввода-вывода принтера \_</span><span class="sxs-lookup"><span data-stu-id="53564-217">PRINTER\_STATUS\_IO\_ACTIVE</span></span>         | <span data-ttu-id="53564-218">Принтер находится в активном состоянии ввода-вывода</span><span class="sxs-lookup"><span data-stu-id="53564-218">The printer is in an active input/output state</span></span>                   |
| <span data-ttu-id="53564-219">\_ \_ канал ручного состояния принтера \_</span><span class="sxs-lookup"><span data-stu-id="53564-219">PRINTER\_STATUS\_MANUAL\_FEED</span></span>       | <span data-ttu-id="53564-220">Принтер находится в состоянии ручного перевода.</span><span class="sxs-lookup"><span data-stu-id="53564-220">The printer is in a manual feed state.</span></span>                           |
| <span data-ttu-id="53564-221">\_состояние принтера \_ без \_ тонера</span><span class="sxs-lookup"><span data-stu-id="53564-221">PRINTER\_STATUS\_NO\_TONER</span></span>          | <span data-ttu-id="53564-222">В принтере закончился тонер.</span><span class="sxs-lookup"><span data-stu-id="53564-222">The printer is out of toner.</span></span>                                     |
| <span data-ttu-id="53564-223">\_состояние принтера \_ \_ недоступно</span><span class="sxs-lookup"><span data-stu-id="53564-223">PRINTER\_STATUS\_NOT\_AVAILABLE</span></span>     | <span data-ttu-id="53564-224">Принтер недоступен для печати.</span><span class="sxs-lookup"><span data-stu-id="53564-224">The printer is not available for printing.</span></span>                       |
| <span data-ttu-id="53564-225">состояние принтера " \_ \_ вне сети"</span><span class="sxs-lookup"><span data-stu-id="53564-225">PRINTER\_STATUS\_OFFLINE</span></span>            | <span data-ttu-id="53564-226">Принтер отключен.</span><span class="sxs-lookup"><span data-stu-id="53564-226">The printer is offline.</span></span>                                          |
| <span data-ttu-id="53564-227">состояние принтера " \_ \_ недостаточно \_ \_ памяти"</span><span class="sxs-lookup"><span data-stu-id="53564-227">PRINTER\_STATUS\_OUT\_OF\_MEMORY</span></span>    | <span data-ttu-id="53564-228">В принтере закончилось память.</span><span class="sxs-lookup"><span data-stu-id="53564-228">The printer has run out of memory.</span></span>                               |
| <span data-ttu-id="53564-229">\_ \_ выходной лоток состояния \_ принтера \_ полон</span><span class="sxs-lookup"><span data-stu-id="53564-229">PRINTER\_STATUS\_OUTPUT\_BIN\_FULL</span></span>  | <span data-ttu-id="53564-230">Выходной лоток принтера полностью заполнен.</span><span class="sxs-lookup"><span data-stu-id="53564-230">The printer's output bin is full.</span></span>                                |
| <span data-ttu-id="53564-231">\_страница состояния принтера с \_ \_ непечатанием</span><span class="sxs-lookup"><span data-stu-id="53564-231">PRINTER\_STATUS\_PAGE\_PUNT</span></span>         | <span data-ttu-id="53564-232">Принтеру не удается напечатать текущую страницу.</span><span class="sxs-lookup"><span data-stu-id="53564-232">The printer cannot print the current page.</span></span>                       |
| <span data-ttu-id="53564-233">\_ \_ Застревание бумаги по СОСТОЯНИю принтера \_</span><span class="sxs-lookup"><span data-stu-id="53564-233">PRINTER\_STATUS\_PAPER\_JAM</span></span>         | <span data-ttu-id="53564-234">Бумага застряла на принтере</span><span class="sxs-lookup"><span data-stu-id="53564-234">Paper is jammed in the printer</span></span>                                   |
| <span data-ttu-id="53564-235">\_Бумага состояния \_ принтера \_</span><span class="sxs-lookup"><span data-stu-id="53564-235">PRINTER\_STATUS\_PAPER\_OUT</span></span>         | <span data-ttu-id="53564-236">В принтере нет бумаги.</span><span class="sxs-lookup"><span data-stu-id="53564-236">The printer is out of paper.</span></span>                                     |
| <span data-ttu-id="53564-237">\_проблема с \_ бумагой по СОСТОЯНИю принтера \_</span><span class="sxs-lookup"><span data-stu-id="53564-237">PRINTER\_STATUS\_PAPER\_PROBLEM</span></span>     | <span data-ttu-id="53564-238">В принтере есть проблема с бумагой.</span><span class="sxs-lookup"><span data-stu-id="53564-238">The printer has a paper problem.</span></span>                                 |
| <span data-ttu-id="53564-239">\_состояние принтера \_ приостановлено</span><span class="sxs-lookup"><span data-stu-id="53564-239">PRINTER\_STATUS\_PAUSED</span></span>             | <span data-ttu-id="53564-240">Работа принтера приостановлена.</span><span class="sxs-lookup"><span data-stu-id="53564-240">The printer is paused.</span></span>                                           |
| <span data-ttu-id="53564-241">\_состояние принтера \_ ожидает \_ удаления</span><span class="sxs-lookup"><span data-stu-id="53564-241">PRINTER\_STATUS\_PENDING\_DELETION</span></span>  | <span data-ttu-id="53564-242">Идет удаление принтера.</span><span class="sxs-lookup"><span data-stu-id="53564-242">The printer is being deleted.</span></span>                                    |
| <span data-ttu-id="53564-243">состояние принтера "Энергосбережение" \_ \_ \_</span><span class="sxs-lookup"><span data-stu-id="53564-243">PRINTER\_STATUS\_POWER\_SAVE</span></span>        | <span data-ttu-id="53564-244">Принтер находится в режиме экономии энергии.</span><span class="sxs-lookup"><span data-stu-id="53564-244">The printer is in power save mode.</span></span>                               |
| <span data-ttu-id="53564-245">\_Печать состояния \_ принтера</span><span class="sxs-lookup"><span data-stu-id="53564-245">PRINTER\_STATUS\_PRINTING</span></span>           | <span data-ttu-id="53564-246">Принтер печатает.</span><span class="sxs-lookup"><span data-stu-id="53564-246">The printer is printing.</span></span>                                         |
| <span data-ttu-id="53564-247">\_Обработка состояния \_ принтера</span><span class="sxs-lookup"><span data-stu-id="53564-247">PRINTER\_STATUS\_PROCESSING</span></span>         | <span data-ttu-id="53564-248">Принтер обрабатывает задание печати.</span><span class="sxs-lookup"><span data-stu-id="53564-248">The printer is processing a print job.</span></span>                           |
| <span data-ttu-id="53564-249">\_сервер состояния \_ принтера \_ неизвестен</span><span class="sxs-lookup"><span data-stu-id="53564-249">PRINTER\_STATUS\_SERVER\_UNKNOWN</span></span>    | <span data-ttu-id="53564-250">Состояние принтера неизвестно.</span><span class="sxs-lookup"><span data-stu-id="53564-250">The printer status is unknown.</span></span>                                   |
| <span data-ttu-id="53564-251">\_ \_ низкое тонер на состояние принтера \_</span><span class="sxs-lookup"><span data-stu-id="53564-251">PRINTER\_STATUS\_TONER\_LOW</span></span>         | <span data-ttu-id="53564-252">На принтере недостаточно тонера.</span><span class="sxs-lookup"><span data-stu-id="53564-252">The printer is low on toner.</span></span>                                     |
| <span data-ttu-id="53564-253">\_состояние принтера \_ — \_ вмешательство пользователя</span><span class="sxs-lookup"><span data-stu-id="53564-253">PRINTER\_STATUS\_USER\_INTERVENTION</span></span> | <span data-ttu-id="53564-254">В принтере есть ошибка, которая требует от пользователя выполнить какие-либо действия.</span><span class="sxs-lookup"><span data-stu-id="53564-254">The printer has an error that requires the user to do something.</span></span> |
| <span data-ttu-id="53564-255">\_ \_ Ожидание состояния принтера</span><span class="sxs-lookup"><span data-stu-id="53564-255">PRINTER\_STATUS\_WAITING</span></span>            | <span data-ttu-id="53564-256">Принтер находится в состоянии ожидания.</span><span class="sxs-lookup"><span data-stu-id="53564-256">The printer is waiting.</span></span>                                          |
| <span data-ttu-id="53564-257">\_прогрев состояния \_ принтера \_</span><span class="sxs-lookup"><span data-stu-id="53564-257">PRINTER\_STATUS\_WARMING\_UP</span></span>        | <span data-ttu-id="53564-258">Идет прогрев принтера.</span><span class="sxs-lookup"><span data-stu-id="53564-258">The printer is warming up.</span></span>                                       |



 

</dd> <dt>

<span data-ttu-id="53564-259">**кжобс**</span><span class="sxs-lookup"><span data-stu-id="53564-259">**cJobs**</span></span>
</dt> <dd>

<span data-ttu-id="53564-260">Число заданий печати, поставленных в очередь для принтера.</span><span class="sxs-lookup"><span data-stu-id="53564-260">The number of print jobs that have been queued for the printer.</span></span>

</dd> <dt>

<span data-ttu-id="53564-261">**аверажеппм**</span><span class="sxs-lookup"><span data-stu-id="53564-261">**AveragePPM**</span></span>
</dt> <dd>

<span data-ttu-id="53564-262">Среднее число страниц в минуту, напечатанных на принтере.</span><span class="sxs-lookup"><span data-stu-id="53564-262">The average number of pages per minute that have been printed on the printer.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="53564-263">Требования</span><span class="sxs-lookup"><span data-stu-id="53564-263">Requirements</span></span>



| <span data-ttu-id="53564-264">Требование</span><span class="sxs-lookup"><span data-stu-id="53564-264">Requirement</span></span> | <span data-ttu-id="53564-265">Значение</span><span class="sxs-lookup"><span data-stu-id="53564-265">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="53564-266">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="53564-266">Minimum supported client</span></span><br/> | <span data-ttu-id="53564-267">Windows 2000 Professional \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="53564-267">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                                |
| <span data-ttu-id="53564-268">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="53564-268">Minimum supported server</span></span><br/> | <span data-ttu-id="53564-269">Windows 2000 Server \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="53564-269">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                      |
| <span data-ttu-id="53564-270">Заголовок</span><span class="sxs-lookup"><span data-stu-id="53564-270">Header</span></span><br/>                   | <dl> <span data-ttu-id="53564-271"><dt>Винспул. h (включение Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="53564-271"><dt>Winspool.h (include Windows.h)</dt></span></span> </dl> |
| <span data-ttu-id="53564-272">Имя в кодировке Юникод и ANSI</span><span class="sxs-lookup"><span data-stu-id="53564-272">Unicode and ANSI names</span></span><br/>   | <span data-ttu-id="53564-273">**\_ \_ Сведения о \_ принтере 2W** (Юникод) и **\_ \_ сведения о принтере \_ 2A** (ANSI)</span><span class="sxs-lookup"><span data-stu-id="53564-273">**\_PRINTER\_INFO\_2W** (Unicode) and **\_PRINTER\_INFO\_2A** (ANSI)</span></span><br/>                           |



## <a name="see-also"></a><span data-ttu-id="53564-274">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="53564-274">See also</span></span>

<dl> <dt>

[<span data-ttu-id="53564-275">Вывод на печать</span><span class="sxs-lookup"><span data-stu-id="53564-275">Printing</span></span>](printdocs-printing.md)
</dt> <dt>

[<span data-ttu-id="53564-276">Структуры API диспетчера очереди печати</span><span class="sxs-lookup"><span data-stu-id="53564-276">Print Spooler API Structures</span></span>](printing-and-print-spooler-structures.md)
</dt> <dt>

[<span data-ttu-id="53564-277">**DEVMODE**</span><span class="sxs-lookup"><span data-stu-id="53564-277">**DEVMODE**</span></span>](/windows/win32/api/wingdi/ns-wingdi-devmodea)
</dt> <dt>

[<span data-ttu-id="53564-278">**енумпринтерс**</span><span class="sxs-lookup"><span data-stu-id="53564-278">**EnumPrinters**</span></span>](enumprinters.md)
</dt> <dt>

[<span data-ttu-id="53564-279">**\_Сведения о принтере \_ 1**</span><span class="sxs-lookup"><span data-stu-id="53564-279">**PRINTER\_INFO\_1**</span></span>](printer-info-1.md)
</dt> <dt>

[<span data-ttu-id="53564-280">**\_Сведения о принтере \_ 3**</span><span class="sxs-lookup"><span data-stu-id="53564-280">**PRINTER\_INFO\_3**</span></span>](printer-info-3.md)
</dt> <dt>

[<span data-ttu-id="53564-281">**\_Сведения о принтере \_ 4**</span><span class="sxs-lookup"><span data-stu-id="53564-281">**PRINTER\_INFO\_4**</span></span>](printer-info-4.md)
</dt> <dt>

[<span data-ttu-id="53564-282">**\_дескриптор безопасности**</span><span class="sxs-lookup"><span data-stu-id="53564-282">**SECURITY\_DESCRIPTOR**</span></span>](/windows/desktop/api/winnt/ns-winnt-security_descriptor)
</dt> </dl>

 

