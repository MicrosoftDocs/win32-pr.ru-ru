---
description: В структуре сведения о ПРИНТЕРе \_ \_ 5 указаны подробные сведения о принтере.
ms.assetid: c8599f2e-3b7c-4fde-a340-ca7d3ddaa106
title: Структура PRINTER_INFO_5 (Винспул. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- PRINTER_INFO_5
- _PRINTER_INFO_5A
- _PRINTER_INFO_5W
api_type:
- HeaderDef
api_location:
- Winspool.h
ms.openlocfilehash: 2ec207b60eca8cc20f6f24e2bb08bb1e3b191fcc
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "105719594"
---
# <a name="printer_info_5-structure"></a><span data-ttu-id="99cc1-103">\_Структура сведения о принтере \_ 5</span><span class="sxs-lookup"><span data-stu-id="99cc1-103">PRINTER\_INFO\_5 structure</span></span>

<span data-ttu-id="99cc1-104">В структуре сведения о **принтере \_ \_ 5** указаны подробные сведения о принтере.</span><span class="sxs-lookup"><span data-stu-id="99cc1-104">The **PRINTER\_INFO\_5** structure specifies detailed printer information.</span></span>

## <a name="syntax"></a><span data-ttu-id="99cc1-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="99cc1-105">Syntax</span></span>


```C++
typedef struct _PRINTER_INFO_5 {
  LPTSTR pPrinterName;
  LPTSTR pPortName;
  DWORD  Attributes;
  DWORD  DeviceNotSelectedTimeout;
  DWORD  TransmissionRetryTimeout;
} PRINTER_INFO_5, *PPRINTER_INFO_5;
```



## <a name="members"></a><span data-ttu-id="99cc1-106">Члены</span><span class="sxs-lookup"><span data-stu-id="99cc1-106">Members</span></span>

<dl> <dt>

<span data-ttu-id="99cc1-107">**ппринтернаме**</span><span class="sxs-lookup"><span data-stu-id="99cc1-107">**pPrinterName**</span></span>
</dt> <dd>

<span data-ttu-id="99cc1-108">Указатель на строку, завершающуюся нулем, которая указывает имя принтера.</span><span class="sxs-lookup"><span data-stu-id="99cc1-108">A pointer to a null-terminated string that specifies the name of the printer.</span></span>

</dd> <dt>

<span data-ttu-id="99cc1-109">**ппортнаме**</span><span class="sxs-lookup"><span data-stu-id="99cc1-109">**pPortName**</span></span>
</dt> <dd>

<span data-ttu-id="99cc1-110">Указатель на строку, завершающуюся нулем, которая определяет порты, используемые для передачи данных на принтер.</span><span class="sxs-lookup"><span data-stu-id="99cc1-110">A pointer to a null-terminated string that identifies the port(s) used to transmit data to the printer.</span></span> <span data-ttu-id="99cc1-111">Если принтер подключен к нескольким портам, имена каждого порта должны быть разделены запятыми (например, "LPT1:, LPT2:, LPT3:").</span><span class="sxs-lookup"><span data-stu-id="99cc1-111">If a printer is connected to more than one port, the names of each port must be separated by commas (for example, "LPT1:,LPT2:,LPT3:").</span></span>

</dd> <dt>

<span data-ttu-id="99cc1-112">**Атрибуты**</span><span class="sxs-lookup"><span data-stu-id="99cc1-112">**Attributes**</span></span>
</dt> <dd>

<span data-ttu-id="99cc1-113">Атрибуты принтера.</span><span class="sxs-lookup"><span data-stu-id="99cc1-113">The printer attributes.</span></span> <span data-ttu-id="99cc1-114">Этот элемент может быть любым разумным сочетанием следующих значений.</span><span class="sxs-lookup"><span data-stu-id="99cc1-114">This member can be any reasonable combination of the following values.</span></span>

| <span data-ttu-id="99cc1-115">Значение</span><span class="sxs-lookup"><span data-stu-id="99cc1-115">Value</span></span>                                   | <span data-ttu-id="99cc1-116">Значение</span><span class="sxs-lookup"><span data-stu-id="99cc1-116">Meaning</span></span>                                                                                                                                                                                 |
|-----------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="99cc1-117">атрибут «принтер» \_ \_ Direct</span><span class="sxs-lookup"><span data-stu-id="99cc1-117">PRINTER\_ATTRIBUTE\_DIRECT</span></span>              | <span data-ttu-id="99cc1-118">Задание отправляется непосредственно на принтер (он не помещается в очередь).</span><span class="sxs-lookup"><span data-stu-id="99cc1-118">Job is sent directly to the printer (it is not spooled).</span></span>                                                                                                                                |
| <span data-ttu-id="99cc1-119">\_ \_ \_ сначала необходимо выполнить атрибут \_ Printer</span><span class="sxs-lookup"><span data-stu-id="99cc1-119">PRINTER\_ATTRIBUTE\_DO\_COMPLETE\_FIRST</span></span> | <span data-ttu-id="99cc1-120">Если для параметра задать и принтер задано значение печать во время очереди печати, то все задания, для которых была завершена буферизация, будут распечатываться перед заданиями, которые не завершают работу с очередью.</span><span class="sxs-lookup"><span data-stu-id="99cc1-120">If set and printer is set for print-while-spooling, any jobs that have completed spooling are scheduled to print before jobs that have not completed spooling.</span></span>                          |
| <span data-ttu-id="99cc1-121">\_атрибут принтера \_ Enable \_ девк</span><span class="sxs-lookup"><span data-stu-id="99cc1-121">PRINTER\_ATTRIBUTE\_ENABLE\_DEVQ</span></span>        | <span data-ttu-id="99cc1-122">Если задано значение, вызывается **девкуерипринт** .</span><span class="sxs-lookup"><span data-stu-id="99cc1-122">If set, **DevQueryPrint** is called.</span></span> <span data-ttu-id="99cc1-123">**Девкуерипринт** может завершиться ошибкой, если настройки документа и принтера не совпадают.</span><span class="sxs-lookup"><span data-stu-id="99cc1-123">**DevQueryPrint** may fail if the document and printer setups do not match.</span></span> <span data-ttu-id="99cc1-124">Установка этого флага приводит к тому, что документы не будут храниться в очереди.</span><span class="sxs-lookup"><span data-stu-id="99cc1-124">Setting this flag causes mismatched documents to be held in the queue.</span></span> |
| <span data-ttu-id="99cc1-125">\_атрибут принтера \_ скрыт</span><span class="sxs-lookup"><span data-stu-id="99cc1-125">PRINTER\_ATTRIBUTE\_HIDDEN</span></span>              | <span data-ttu-id="99cc1-126">Зарезервировано.</span><span class="sxs-lookup"><span data-stu-id="99cc1-126">Reserved.</span></span>                                                                                                                                                                               |
| <span data-ttu-id="99cc1-127">\_киппринтеджобс атрибута \_ принтера</span><span class="sxs-lookup"><span data-stu-id="99cc1-127">PRINTER\_ATTRIBUTE\_KEEPPRINTEDJOBS</span></span>     | <span data-ttu-id="99cc1-128">Если задано, задания сохраняются после печати.</span><span class="sxs-lookup"><span data-stu-id="99cc1-128">If set, jobs are kept after they are printed.</span></span> <span data-ttu-id="99cc1-129">Если не задано, задания удаляются.</span><span class="sxs-lookup"><span data-stu-id="99cc1-129">If unset, jobs are deleted.</span></span>                                                                                                               |
| <span data-ttu-id="99cc1-130">\_локальный атрибут \_ принтера</span><span class="sxs-lookup"><span data-stu-id="99cc1-130">PRINTER\_ATTRIBUTE\_LOCAL</span></span>               | <span data-ttu-id="99cc1-131">Принтер является локальным принтером.</span><span class="sxs-lookup"><span data-stu-id="99cc1-131">Printer is a local printer.</span></span>                                                                                                                                                             |
| <span data-ttu-id="99cc1-132">\_сеть АТРИБУТОВ \_ принтера</span><span class="sxs-lookup"><span data-stu-id="99cc1-132">PRINTER\_ATTRIBUTE\_NETWORK</span></span>             | <span data-ttu-id="99cc1-133">Принтер является подключением к сетевому принтеру.</span><span class="sxs-lookup"><span data-stu-id="99cc1-133">Printer is a network printer connection.</span></span>                                                                                                                                                |
| <span data-ttu-id="99cc1-134">\_атрибут принтера \_ опубликован</span><span class="sxs-lookup"><span data-stu-id="99cc1-134">PRINTER\_ATTRIBUTE\_PUBLISHED</span></span>           | <span data-ttu-id="99cc1-135">Указывает, опубликован ли принтер в службе каталогов.</span><span class="sxs-lookup"><span data-stu-id="99cc1-135">Indicates whether the printer is published in the directory service.</span></span>                                                                                                                    |
| <span data-ttu-id="99cc1-136">\_атрибут принтера \_ поставлен в очередь</span><span class="sxs-lookup"><span data-stu-id="99cc1-136">PRINTER\_ATTRIBUTE\_QUEUED</span></span>              | <span data-ttu-id="99cc1-137">Если задано, принтер помещается в очередь и начинает печать после постановки в очередь последней страницы.</span><span class="sxs-lookup"><span data-stu-id="99cc1-137">If set, the printer spools and starts printing after the last page is spooled.</span></span> <span data-ttu-id="99cc1-138">Если параметр не установлен и \_ атрибут принтера \_ Direct не задан, принтер помещается в очередь и печатается при постановке в очередь.</span><span class="sxs-lookup"><span data-stu-id="99cc1-138">If not set and PRINTER\_ATTRIBUTE\_DIRECT is not set, the printer spools and prints while spooling.</span></span>      |
| <span data-ttu-id="99cc1-139">\_только атрибут принтера \_ RAW \_</span><span class="sxs-lookup"><span data-stu-id="99cc1-139">PRINTER\_ATTRIBUTE\_RAW\_ONLY</span></span>           | <span data-ttu-id="99cc1-140">Указывает, что только задания печати необработанного типа данных могут быть поставлены в очередь.</span><span class="sxs-lookup"><span data-stu-id="99cc1-140">Indicates that only raw data type print jobs can be spooled.</span></span>                                                                                                                            |
| <span data-ttu-id="99cc1-141">\_общий атрибут \_ принтера</span><span class="sxs-lookup"><span data-stu-id="99cc1-141">PRINTER\_ATTRIBUTE\_SHARED</span></span>              | <span data-ttu-id="99cc1-142">Принтер является общим.</span><span class="sxs-lookup"><span data-stu-id="99cc1-142">Printer is shared.</span></span>                                                                                                                                                                      |



 

<span data-ttu-id="99cc1-143">В Windows XP и более поздних версиях Windows также можно использовать следующее значение.</span><span class="sxs-lookup"><span data-stu-id="99cc1-143">In Windows XP and later versions of Windows, the following value can also be used.</span></span>

| <span data-ttu-id="99cc1-144">Значение</span><span class="sxs-lookup"><span data-stu-id="99cc1-144">Value</span></span>                   | <span data-ttu-id="99cc1-145">Значение</span><span class="sxs-lookup"><span data-stu-id="99cc1-145">Meaning</span></span>                                                                                                                                                                                           |
|-------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="99cc1-146">\_Факс атрибута \_ принтера</span><span class="sxs-lookup"><span data-stu-id="99cc1-146">PRINTER\_ATTRIBUTE\_FAX</span></span> | <span data-ttu-id="99cc1-147">Если задано, то принтер является принтером факсов.</span><span class="sxs-lookup"><span data-stu-id="99cc1-147">If set, printer is a fax printer.</span></span> <span data-ttu-id="99cc1-148">Это значение может быть задано только параметром [**аддпринтер**](addprinter.md), но его можно получить с помощью [**енумпринтерс**](enumprinters.md) [**и**](getprinter.md).</span><span class="sxs-lookup"><span data-stu-id="99cc1-148">This can only be set by [**AddPrinter**](addprinter.md), but it can be retrieved by [**EnumPrinters**](enumprinters.md) and [**GetPrinter**](getprinter.md).</span></span> |



 

<span data-ttu-id="99cc1-149">В Windows Vista и более поздних версиях Windows также можно использовать следующие значения.</span><span class="sxs-lookup"><span data-stu-id="99cc1-149">In Windows Vista and later versions of Windows, the following values can also be used.</span></span>

| <span data-ttu-id="99cc1-150">Значение</span><span class="sxs-lookup"><span data-stu-id="99cc1-150">Value</span></span>                               | <span data-ttu-id="99cc1-151">Значение</span><span class="sxs-lookup"><span data-stu-id="99cc1-151">Meaning</span></span>                                                                          |
|-------------------------------------|----------------------------------------------------------------------------------|
| <span data-ttu-id="99cc1-152">\_ \_ понятное имя атрибута принтера \_</span><span class="sxs-lookup"><span data-stu-id="99cc1-152">PRINTER\_ATTRIBUTE\_FRIENDLY\_NAME</span></span>  | <span data-ttu-id="99cc1-153">Компьютер подключился к принтеру и получил понятное имя.</span><span class="sxs-lookup"><span data-stu-id="99cc1-153">A computer has connected to this printer and given it a friendly name.</span></span>           |
| <span data-ttu-id="99cc1-154">\_компьютер с атрибутом принтера \_</span><span class="sxs-lookup"><span data-stu-id="99cc1-154">PRINTER\_ATTRIBUTE\_MACHINE</span></span>         | <span data-ttu-id="99cc1-155">Принтер является подключением для каждого компьютера.</span><span class="sxs-lookup"><span data-stu-id="99cc1-155">Printer is a per-machine connection.</span></span>                                             |
| <span data-ttu-id="99cc1-156">атрибут принтера, \_ \_ отправленный \_ пользователем</span><span class="sxs-lookup"><span data-stu-id="99cc1-156">PRINTER\_ATTRIBUTE\_PUSHED\_USER</span></span>    | <span data-ttu-id="99cc1-157">Принтер был установлен с помощью политики пользователя "принудительное подключение к принтеру".</span><span class="sxs-lookup"><span data-stu-id="99cc1-157">The printer was installed by using the Push Printer Connections user policy.</span></span>     |
| <span data-ttu-id="99cc1-158">атрибут принтера, \_ \_ отправленный на \_ компьютер</span><span class="sxs-lookup"><span data-stu-id="99cc1-158">PRINTER\_ATTRIBUTE\_PUSHED\_MACHINE</span></span> | <span data-ttu-id="99cc1-159">Принтер был установлен с помощью политики компьютера Push-подключения принтера.</span><span class="sxs-lookup"><span data-stu-id="99cc1-159">The printer was installed by using the Push Printer Connections computer policy.</span></span> |



 

</dd> <dt>

<span data-ttu-id="99cc1-160">**девиценотселектедтимеаут**</span><span class="sxs-lookup"><span data-stu-id="99cc1-160">**DeviceNotSelectedTimeout**</span></span>
</dt> <dd>

<span data-ttu-id="99cc1-161">Это значение не используется.</span><span class="sxs-lookup"><span data-stu-id="99cc1-161">This value is not used.</span></span>

</dd> <dt>

<span data-ttu-id="99cc1-162">**трансмиссионретритимеаут**</span><span class="sxs-lookup"><span data-stu-id="99cc1-162">**TransmissionRetryTimeout**</span></span>
</dt> <dd>

<span data-ttu-id="99cc1-163">Это значение не используется.</span><span class="sxs-lookup"><span data-stu-id="99cc1-163">This value is not used.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="99cc1-164">Требования</span><span class="sxs-lookup"><span data-stu-id="99cc1-164">Requirements</span></span>



| <span data-ttu-id="99cc1-165">Требование</span><span class="sxs-lookup"><span data-stu-id="99cc1-165">Requirement</span></span> | <span data-ttu-id="99cc1-166">Значение</span><span class="sxs-lookup"><span data-stu-id="99cc1-166">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="99cc1-167">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="99cc1-167">Minimum supported client</span></span><br/> | <span data-ttu-id="99cc1-168">Windows 2000 Professional \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="99cc1-168">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                                |
| <span data-ttu-id="99cc1-169">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="99cc1-169">Minimum supported server</span></span><br/> | <span data-ttu-id="99cc1-170">Windows 2000 Server \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="99cc1-170">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                      |
| <span data-ttu-id="99cc1-171">Заголовок</span><span class="sxs-lookup"><span data-stu-id="99cc1-171">Header</span></span><br/>                   | <dl> <span data-ttu-id="99cc1-172"><dt>Винспул. h (включение Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="99cc1-172"><dt>Winspool.h (include Windows.h)</dt></span></span> </dl> |
| <span data-ttu-id="99cc1-173">Имя в кодировке Юникод и ANSI</span><span class="sxs-lookup"><span data-stu-id="99cc1-173">Unicode and ANSI names</span></span><br/>   | <span data-ttu-id="99cc1-174">**\_ \_ Сведения о \_ принтере 5W** (Юникод) и **\_ \_ сведения о принтере \_ 5A** (ANSI)</span><span class="sxs-lookup"><span data-stu-id="99cc1-174">**\_PRINTER\_INFO\_5W** (Unicode) and **\_PRINTER\_INFO\_5A** (ANSI)</span></span><br/>                           |



## <a name="see-also"></a><span data-ttu-id="99cc1-175">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="99cc1-175">See also</span></span>

<dl> <dt>

[<span data-ttu-id="99cc1-176">Вывод на печать</span><span class="sxs-lookup"><span data-stu-id="99cc1-176">Printing</span></span>](printdocs-printing.md)
</dt> <dt>

[<span data-ttu-id="99cc1-177">Структуры API диспетчера очереди печати</span><span class="sxs-lookup"><span data-stu-id="99cc1-177">Print Spooler API Structures</span></span>](printing-and-print-spooler-structures.md)
</dt> <dt>

[<span data-ttu-id="99cc1-178">**енумпринтерс**</span><span class="sxs-lookup"><span data-stu-id="99cc1-178">**EnumPrinters**</span></span>](enumprinters.md)
</dt> <dt>

[<span data-ttu-id="99cc1-179">**Наложение**</span><span class="sxs-lookup"><span data-stu-id="99cc1-179">**GetPrinter**</span></span>](getprinter.md)
</dt> <dt>

[<span data-ttu-id="99cc1-180">**сетпринтер**</span><span class="sxs-lookup"><span data-stu-id="99cc1-180">**SetPrinter**</span></span>](setprinter.md)
</dt> <dt>

[<span data-ttu-id="99cc1-181">**\_Сведения о принтере \_ 1**</span><span class="sxs-lookup"><span data-stu-id="99cc1-181">**PRINTER\_INFO\_1**</span></span>](printer-info-1.md)
</dt> <dt>

[<span data-ttu-id="99cc1-182">**\_Сведения о принтере \_ 2**</span><span class="sxs-lookup"><span data-stu-id="99cc1-182">**PRINTER\_INFO\_2**</span></span>](printer-info-2.md)
</dt> <dt>

[<span data-ttu-id="99cc1-183">**\_Сведения о принтере \_ 3**</span><span class="sxs-lookup"><span data-stu-id="99cc1-183">**PRINTER\_INFO\_3**</span></span>](printer-info-3.md)
</dt> <dt>

[<span data-ttu-id="99cc1-184">**\_Сведения о принтере \_ 4**</span><span class="sxs-lookup"><span data-stu-id="99cc1-184">**PRINTER\_INFO\_4**</span></span>](printer-info-4.md)
</dt> </dl>

 

 




