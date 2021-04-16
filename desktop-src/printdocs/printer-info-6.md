---
description: В \_ сведениях о принтере \_ 6 указывается значение состояния принтера.
ms.assetid: f26fe75b-7c97-47ad-892f-d9e40331fa5d
title: Структура PRINTER_INFO_6 (Винспул. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- PRINTER_INFO_6
- _PRINTER_INFO_6A
- _PRINTER_INFO_6W
api_type:
- HeaderDef
api_location:
- Winspool.h
ms.openlocfilehash: 0ee4e86590483ec1751fa088fd56770c5891df0a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "105712851"
---
# <a name="printer_info_6-structure"></a><span data-ttu-id="f80f1-103">\_Структура сведений о принтере \_ 6</span><span class="sxs-lookup"><span data-stu-id="f80f1-103">PRINTER\_INFO\_6 structure</span></span>

<span data-ttu-id="f80f1-104">В **\_ сведениях \_ о принтере 6** указывается значение состояния принтера.</span><span class="sxs-lookup"><span data-stu-id="f80f1-104">The **PRINTER\_INFO\_6** specifies the status value of a printer.</span></span>

## <a name="syntax"></a><span data-ttu-id="f80f1-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="f80f1-105">Syntax</span></span>


```C++
typedef struct _PRINTER_INFO_6 {
  DWORD dwStatus;
} PRINTER_INFO_6, *PPRINTER_INFO_6;
```



## <a name="members"></a><span data-ttu-id="f80f1-106">Члены</span><span class="sxs-lookup"><span data-stu-id="f80f1-106">Members</span></span>

<dl> <dt>

<span data-ttu-id="f80f1-107">**Dwstatus устанавливается**</span><span class="sxs-lookup"><span data-stu-id="f80f1-107">**dwStatus**</span></span>
</dt> <dd>

<span data-ttu-id="f80f1-108">Состояние принтера.</span><span class="sxs-lookup"><span data-stu-id="f80f1-108">The printer status.</span></span> <span data-ttu-id="f80f1-109">Этот элемент может быть любым разумным сочетанием следующих значений.</span><span class="sxs-lookup"><span data-stu-id="f80f1-109">This member can be any reasonable combination of the following values.</span></span>



| <span data-ttu-id="f80f1-110">Значение</span><span class="sxs-lookup"><span data-stu-id="f80f1-110">Value</span></span>                               | <span data-ttu-id="f80f1-111">Значение</span><span class="sxs-lookup"><span data-stu-id="f80f1-111">Meaning</span></span>                                                                                                       |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="f80f1-112">\_состояние принтера \_ занято</span><span class="sxs-lookup"><span data-stu-id="f80f1-112">PRINTER\_STATUS\_BUSY</span></span>               | <span data-ttu-id="f80f1-113">Принтер занят.</span><span class="sxs-lookup"><span data-stu-id="f80f1-113">The printer is busy.</span></span>                                                                                          |
| <span data-ttu-id="f80f1-114">\_ \_ открыта дверца состояния принтера \_</span><span class="sxs-lookup"><span data-stu-id="f80f1-114">PRINTER\_STATUS\_DOOR\_OPEN</span></span>         | <span data-ttu-id="f80f1-115">Открыта дверца принтера.</span><span class="sxs-lookup"><span data-stu-id="f80f1-115">The printer door is open.</span></span>                                                                                     |
| <span data-ttu-id="f80f1-116">\_Ошибка состояния \_ принтера</span><span class="sxs-lookup"><span data-stu-id="f80f1-116">PRINTER\_STATUS\_ERROR</span></span>              | <span data-ttu-id="f80f1-117">Не используется.</span><span class="sxs-lookup"><span data-stu-id="f80f1-117">Not used.</span></span>                                                                                                     |
| <span data-ttu-id="f80f1-118">\_ \_ Инициализация состояния принтера</span><span class="sxs-lookup"><span data-stu-id="f80f1-118">PRINTER\_STATUS\_INITIALIZING</span></span>       | <span data-ttu-id="f80f1-119">Идет инициализация принтера.</span><span class="sxs-lookup"><span data-stu-id="f80f1-119">The printer is initializing.</span></span>                                                                                  |
| <span data-ttu-id="f80f1-120">\_Активный статус \_ ввода-вывода принтера \_</span><span class="sxs-lookup"><span data-stu-id="f80f1-120">PRINTER\_STATUS\_IO\_ACTIVE</span></span>         | <span data-ttu-id="f80f1-121">Принтер находится в активном состоянии ввода-вывода</span><span class="sxs-lookup"><span data-stu-id="f80f1-121">The printer is in an active input/output state</span></span>                                                                |
| <span data-ttu-id="f80f1-122">\_ \_ канал ручного состояния принтера \_</span><span class="sxs-lookup"><span data-stu-id="f80f1-122">PRINTER\_STATUS\_MANUAL\_FEED</span></span>       | <span data-ttu-id="f80f1-123">Принтер находится в состоянии ручного перевода.</span><span class="sxs-lookup"><span data-stu-id="f80f1-123">The printer is in a manual feed state.</span></span>                                                                        |
| <span data-ttu-id="f80f1-124">\_состояние принтера \_ без \_ тонера</span><span class="sxs-lookup"><span data-stu-id="f80f1-124">PRINTER\_STATUS\_NO\_TONER</span></span>          | <span data-ttu-id="f80f1-125">В принтере закончился тонер.</span><span class="sxs-lookup"><span data-stu-id="f80f1-125">The printer is out of toner.</span></span>                                                                                  |
| <span data-ttu-id="f80f1-126">\_состояние принтера \_ \_ недоступно</span><span class="sxs-lookup"><span data-stu-id="f80f1-126">PRINTER\_STATUS\_NOT\_AVAILABLE</span></span>     | <span data-ttu-id="f80f1-127">Принтер недоступен для печати.</span><span class="sxs-lookup"><span data-stu-id="f80f1-127">The printer is not available for printing.</span></span>                                                                    |
| <span data-ttu-id="f80f1-128">состояние принтера " \_ \_ вне сети"</span><span class="sxs-lookup"><span data-stu-id="f80f1-128">PRINTER\_STATUS\_OFFLINE</span></span>            | <span data-ttu-id="f80f1-129">Принтер отключен.</span><span class="sxs-lookup"><span data-stu-id="f80f1-129">The printer is offline.</span></span>                                                                                       |
| <span data-ttu-id="f80f1-130">состояние принтера " \_ \_ недостаточно \_ \_ памяти"</span><span class="sxs-lookup"><span data-stu-id="f80f1-130">PRINTER\_STATUS\_OUT\_OF\_MEMORY</span></span>    | <span data-ttu-id="f80f1-131">В принтере закончилось память.</span><span class="sxs-lookup"><span data-stu-id="f80f1-131">The printer has run out of memory.</span></span>                                                                            |
| <span data-ttu-id="f80f1-132">\_ \_ выходной лоток состояния \_ принтера \_ полон</span><span class="sxs-lookup"><span data-stu-id="f80f1-132">PRINTER\_STATUS\_OUTPUT\_BIN\_FULL</span></span>  | <span data-ttu-id="f80f1-133">Выходной лоток принтера полностью заполнен.</span><span class="sxs-lookup"><span data-stu-id="f80f1-133">The printer's output bin is full.</span></span>                                                                             |
| <span data-ttu-id="f80f1-134">\_страница состояния принтера с \_ \_ непечатанием</span><span class="sxs-lookup"><span data-stu-id="f80f1-134">PRINTER\_STATUS\_PAGE\_PUNT</span></span>         | <span data-ttu-id="f80f1-135">Принтеру не удается напечатать текущую страницу.</span><span class="sxs-lookup"><span data-stu-id="f80f1-135">The printer cannot print the current page.</span></span>                                                                    |
| <span data-ttu-id="f80f1-136">\_ \_ Застревание бумаги по СОСТОЯНИю принтера \_</span><span class="sxs-lookup"><span data-stu-id="f80f1-136">PRINTER\_STATUS\_PAPER\_JAM</span></span>         | <span data-ttu-id="f80f1-137">Бумага застряла на принтере</span><span class="sxs-lookup"><span data-stu-id="f80f1-137">Paper is jammed in the printer</span></span>                                                                                |
| <span data-ttu-id="f80f1-138">\_Бумага состояния \_ принтера \_</span><span class="sxs-lookup"><span data-stu-id="f80f1-138">PRINTER\_STATUS\_PAPER\_OUT</span></span>         | <span data-ttu-id="f80f1-139">В принтере нет бумаги.</span><span class="sxs-lookup"><span data-stu-id="f80f1-139">The printer is out of paper.</span></span>                                                                                  |
| <span data-ttu-id="f80f1-140">\_проблема с \_ бумагой по СОСТОЯНИю принтера \_</span><span class="sxs-lookup"><span data-stu-id="f80f1-140">PRINTER\_STATUS\_PAPER\_PROBLEM</span></span>     | <span data-ttu-id="f80f1-141">В принтере есть проблема с бумагой.</span><span class="sxs-lookup"><span data-stu-id="f80f1-141">The printer has a paper problem.</span></span>                                                                              |
| <span data-ttu-id="f80f1-142">\_состояние принтера \_ приостановлено</span><span class="sxs-lookup"><span data-stu-id="f80f1-142">PRINTER\_STATUS\_PAUSED</span></span>             | <span data-ttu-id="f80f1-143">Работа принтера приостановлена.</span><span class="sxs-lookup"><span data-stu-id="f80f1-143">The printer is paused.</span></span>                                                                                        |
| <span data-ttu-id="f80f1-144">\_состояние принтера \_ ожидает \_ удаления</span><span class="sxs-lookup"><span data-stu-id="f80f1-144">PRINTER\_STATUS\_PENDING\_DELETION</span></span>  | <span data-ttu-id="f80f1-145">Принтер ожидает удаления в результате вызова функции [**делетепринтер**](deleteprinter.md) .</span><span class="sxs-lookup"><span data-stu-id="f80f1-145">The printer is pending deletion as a result of a call to the [**DeletePrinter**](deleteprinter.md) function.</span></span> |
| <span data-ttu-id="f80f1-146">состояние принтера "Энергосбережение" \_ \_ \_</span><span class="sxs-lookup"><span data-stu-id="f80f1-146">PRINTER\_STATUS\_POWER\_SAVE</span></span>        | <span data-ttu-id="f80f1-147">Принтер находится в режиме экономии энергии.</span><span class="sxs-lookup"><span data-stu-id="f80f1-147">The printer is in power save mode.</span></span>                                                                            |
| <span data-ttu-id="f80f1-148">\_Печать состояния \_ принтера</span><span class="sxs-lookup"><span data-stu-id="f80f1-148">PRINTER\_STATUS\_PRINTING</span></span>           | <span data-ttu-id="f80f1-149">Принтер печатает.</span><span class="sxs-lookup"><span data-stu-id="f80f1-149">The printer is printing.</span></span>                                                                                      |
| <span data-ttu-id="f80f1-150">\_Обработка состояния \_ принтера</span><span class="sxs-lookup"><span data-stu-id="f80f1-150">PRINTER\_STATUS\_PROCESSING</span></span>         | <span data-ttu-id="f80f1-151">Принтер обрабатывает команду из функции [**сетпринтер**](setprinter.md) .</span><span class="sxs-lookup"><span data-stu-id="f80f1-151">The printer is processing a command from the [**SetPrinter**](setprinter.md) function.</span></span>                       |
| <span data-ttu-id="f80f1-152">\_сервер состояния \_ принтера \_ неизвестен</span><span class="sxs-lookup"><span data-stu-id="f80f1-152">PRINTER\_STATUS\_SERVER\_UNKNOWN</span></span>    | <span data-ttu-id="f80f1-153">Состояние принтера неизвестно.</span><span class="sxs-lookup"><span data-stu-id="f80f1-153">The printer status is unknown.</span></span>                                                                                |
| <span data-ttu-id="f80f1-154">\_ \_ низкое тонер на состояние принтера \_</span><span class="sxs-lookup"><span data-stu-id="f80f1-154">PRINTER\_STATUS\_TONER\_LOW</span></span>         | <span data-ttu-id="f80f1-155">На принтере недостаточно тонера.</span><span class="sxs-lookup"><span data-stu-id="f80f1-155">The printer is low on toner.</span></span>                                                                                  |
| <span data-ttu-id="f80f1-156">\_состояние принтера \_ — \_ вмешательство пользователя</span><span class="sxs-lookup"><span data-stu-id="f80f1-156">PRINTER\_STATUS\_USER\_INTERVENTION</span></span> | <span data-ttu-id="f80f1-157">В принтере есть ошибка, которая требует от пользователя выполнить какие-либо действия.</span><span class="sxs-lookup"><span data-stu-id="f80f1-157">The printer has an error that requires the user to do something.</span></span>                                              |
| <span data-ttu-id="f80f1-158">\_ \_ Ожидание состояния принтера</span><span class="sxs-lookup"><span data-stu-id="f80f1-158">PRINTER\_STATUS\_WAITING</span></span>            | <span data-ttu-id="f80f1-159">Принтер находится в состоянии ожидания.</span><span class="sxs-lookup"><span data-stu-id="f80f1-159">The printer is waiting.</span></span>                                                                                       |
| <span data-ttu-id="f80f1-160">\_прогрев состояния \_ принтера \_</span><span class="sxs-lookup"><span data-stu-id="f80f1-160">PRINTER\_STATUS\_WARMING\_UP</span></span>        | <span data-ttu-id="f80f1-161">Идет прогрев принтера.</span><span class="sxs-lookup"><span data-stu-id="f80f1-161">The printer is warming up.</span></span>                                                                                    |



 

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="f80f1-162">Требования</span><span class="sxs-lookup"><span data-stu-id="f80f1-162">Requirements</span></span>



| <span data-ttu-id="f80f1-163">Требование</span><span class="sxs-lookup"><span data-stu-id="f80f1-163">Requirement</span></span> | <span data-ttu-id="f80f1-164">Значение</span><span class="sxs-lookup"><span data-stu-id="f80f1-164">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="f80f1-165">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="f80f1-165">Minimum supported client</span></span><br/> | <span data-ttu-id="f80f1-166">Windows 2000 Professional \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="f80f1-166">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                                |
| <span data-ttu-id="f80f1-167">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="f80f1-167">Minimum supported server</span></span><br/> | <span data-ttu-id="f80f1-168">Windows 2000 Server \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="f80f1-168">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                      |
| <span data-ttu-id="f80f1-169">Заголовок</span><span class="sxs-lookup"><span data-stu-id="f80f1-169">Header</span></span><br/>                   | <dl> <span data-ttu-id="f80f1-170"><dt>Винспул. h (включение Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="f80f1-170"><dt>Winspool.h (include Windows.h)</dt></span></span> </dl> |
| <span data-ttu-id="f80f1-171">Имя в кодировке Юникод и ANSI</span><span class="sxs-lookup"><span data-stu-id="f80f1-171">Unicode and ANSI names</span></span><br/>   | <span data-ttu-id="f80f1-172">**\_ \_ Сведения о \_ принтере 6W** (Юникод) и **\_ \_ сведения о принтере \_ 6a** (ANSI)</span><span class="sxs-lookup"><span data-stu-id="f80f1-172">**\_PRINTER\_INFO\_6W** (Unicode) and **\_PRINTER\_INFO\_6A** (ANSI)</span></span><br/>                           |



## <a name="see-also"></a><span data-ttu-id="f80f1-173">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="f80f1-173">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f80f1-174">Вывод на печать</span><span class="sxs-lookup"><span data-stu-id="f80f1-174">Printing</span></span>](printdocs-printing.md)
</dt> <dt>

[<span data-ttu-id="f80f1-175">Структуры API диспетчера очереди печати</span><span class="sxs-lookup"><span data-stu-id="f80f1-175">Print Spooler API Structures</span></span>](printing-and-print-spooler-structures.md)
</dt> <dt>

[<span data-ttu-id="f80f1-176">**сетпринтер**</span><span class="sxs-lookup"><span data-stu-id="f80f1-176">**SetPrinter**</span></span>](setprinter.md)
</dt> <dt>

[<span data-ttu-id="f80f1-177">**\_Сведения о принтере \_ 1**</span><span class="sxs-lookup"><span data-stu-id="f80f1-177">**PRINTER\_INFO\_1**</span></span>](printer-info-1.md)
</dt> <dt>

[<span data-ttu-id="f80f1-178">**\_Сведения о принтере \_ 2**</span><span class="sxs-lookup"><span data-stu-id="f80f1-178">**PRINTER\_INFO\_2**</span></span>](printer-info-2.md)
</dt> <dt>

[<span data-ttu-id="f80f1-179">**\_Сведения о принтере \_ 3**</span><span class="sxs-lookup"><span data-stu-id="f80f1-179">**PRINTER\_INFO\_3**</span></span>](printer-info-3.md)
</dt> <dt>

[<span data-ttu-id="f80f1-180">**\_Сведения о принтере \_ 4**</span><span class="sxs-lookup"><span data-stu-id="f80f1-180">**PRINTER\_INFO\_4**</span></span>](printer-info-4.md)
</dt> <dt>

[<span data-ttu-id="f80f1-181">**\_Сведения о принтере \_ 5**</span><span class="sxs-lookup"><span data-stu-id="f80f1-181">**PRINTER\_INFO\_5**</span></span>](printer-info-5.md)
</dt> </dl>

 

 




