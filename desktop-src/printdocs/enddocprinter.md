---
description: Функция Енддокпринтер завершает задание печати для указанного принтера.
ms.assetid: 13c713e8-cc24-4191-8b1e-967b9e20e541
title: Функция Енддокпринтер (Винспул. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- EndDocPrinter
api_type:
- DllExport
api_location:
- Spoolss.dll
- Ext-MS-Win-Printer-WinSpool-l1-1-2.dll
- WinSpool.Drv
- Ext-MS-Win-Printer-WinSpool-L1-1-3.dll
ms.openlocfilehash: 8d3e2bc110e5ee9412bb1edb89779f896edb015a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "105693142"
---
# <a name="enddocprinter-function"></a><span data-ttu-id="b5230-103">Функция Енддокпринтер</span><span class="sxs-lookup"><span data-stu-id="b5230-103">EndDocPrinter function</span></span>

<span data-ttu-id="b5230-104">Функция **енддокпринтер** завершает задание печати для указанного принтера.</span><span class="sxs-lookup"><span data-stu-id="b5230-104">The **EndDocPrinter** function ends a print job for the specified printer.</span></span>

## <a name="syntax"></a><span data-ttu-id="b5230-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="b5230-105">Syntax</span></span>


```C++
BOOL EndDocPrinter(
  _In_ HANDLE hPrinter
);
```



## <a name="parameters"></a><span data-ttu-id="b5230-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="b5230-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="b5230-107">*хпринтер* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="b5230-107">*hPrinter* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="b5230-108">Обработчик принтера, для которого должно быть завершено задание печати.</span><span class="sxs-lookup"><span data-stu-id="b5230-108">Handle to a printer for which the print job should be ended.</span></span> <span data-ttu-id="b5230-109">Используйте функцию [**опенпринтер**](openprinter.md) или [**аддпринтер**](addprinter.md) для получения маркера принтера.</span><span class="sxs-lookup"><span data-stu-id="b5230-109">Use the [**OpenPrinter**](openprinter.md) or [**AddPrinter**](addprinter.md) function to retrieve a printer handle.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="b5230-110">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="b5230-110">Return value</span></span>

<span data-ttu-id="b5230-111">Если функция выполнена, возвращаемое значение будет ненулевым.</span><span class="sxs-lookup"><span data-stu-id="b5230-111">If the function succeeds, the return value is a nonzero value.</span></span>

<span data-ttu-id="b5230-112">Если функция выполняется неудачно, возвращается нулевое значение.</span><span class="sxs-lookup"><span data-stu-id="b5230-112">If the function fails, the return value is zero.</span></span>

## <a name="remarks"></a><span data-ttu-id="b5230-113">Комментарии</span><span class="sxs-lookup"><span data-stu-id="b5230-113">Remarks</span></span>

> [!Note]  
> <span data-ttu-id="b5230-114">Это блокирующая или синхронная функция, которая может не возвращать значение немедленно.</span><span class="sxs-lookup"><span data-stu-id="b5230-114">This is a blocking or synchronous function and might not return immediately.</span></span> <span data-ttu-id="b5230-115">Скорость возврата этой функцией зависит от факторов времени выполнения, таких как состояние сети, Конфигурация сервера печати и факторы реализации драйвера принтера, которые трудно предсказать при написании приложения.</span><span class="sxs-lookup"><span data-stu-id="b5230-115">How quickly this function returns depends on run-time factors such as network status, print server configuration, and printer driver implementation factors that are difficult to predict when writing an application.</span></span> <span data-ttu-id="b5230-116">Вызов этой функции из потока, который управляет взаимодействием с пользовательским интерфейсом, может привести к невозможности реагирования приложения.</span><span class="sxs-lookup"><span data-stu-id="b5230-116">Calling this function from a thread that manages interaction with the user interface could make the application appear to be unresponsive.</span></span>

 

<span data-ttu-id="b5230-117">Функция **енддокпринтер** возвращает ошибку, если задание печати не было запущено вызовом функции [**стартдокпринтер**](startdocprinter.md) .</span><span class="sxs-lookup"><span data-stu-id="b5230-117">The **EndDocPrinter** function returns an error if the print job was not started by calling the [**StartDocPrinter**](startdocprinter.md) function.</span></span>

<span data-ttu-id="b5230-118">Последовательность для задания печати выглядит следующим образом:</span><span class="sxs-lookup"><span data-stu-id="b5230-118">The sequence for a print job is as follows:</span></span>

1.  <span data-ttu-id="b5230-119">Чтобы начать задание печати, вызовите [**стартдокпринтер**](startdocprinter.md).</span><span class="sxs-lookup"><span data-stu-id="b5230-119">To begin a print job, call [**StartDocPrinter**](startdocprinter.md).</span></span>
2.  <span data-ttu-id="b5230-120">Чтобы начать каждую страницу, вызовите [**стартпажепринтер**](startpageprinter.md).</span><span class="sxs-lookup"><span data-stu-id="b5230-120">To begin each page, call [**StartPagePrinter**](startpageprinter.md).</span></span>
3.  <span data-ttu-id="b5230-121">Чтобы записать данные на страницу, вызовите [**вритепринтер**](writeprinter.md).</span><span class="sxs-lookup"><span data-stu-id="b5230-121">To write data to a page, call [**WritePrinter**](writeprinter.md).</span></span>
4.  <span data-ttu-id="b5230-122">Чтобы завершить каждую страницу, вызовите [**ендпажепринтер**](endpageprinter.md).</span><span class="sxs-lookup"><span data-stu-id="b5230-122">To end each page, call [**EndPagePrinter**](endpageprinter.md).</span></span>
5.  <span data-ttu-id="b5230-123">Повторите 2, 3 и 4 для требуемого количества страниц.</span><span class="sxs-lookup"><span data-stu-id="b5230-123">Repeat 2, 3, and 4 for as many pages as necessary.</span></span>
6.  <span data-ttu-id="b5230-124">Чтобы завершить задание печати, вызовите **енддокпринтер**.</span><span class="sxs-lookup"><span data-stu-id="b5230-124">To end the print job, call **EndDocPrinter**.</span></span>

<span data-ttu-id="b5230-125">Если страница в выгруженном в очередь файле превышает приблизительно 350 МБ, может произойти сбой печати и сообщение об ошибке не отправляется.</span><span class="sxs-lookup"><span data-stu-id="b5230-125">When a page in a spooled file exceeds approximately 350 MB, it may fail to print and not send an error message.</span></span> <span data-ttu-id="b5230-126">Например, это может произойти при печати больших EMF файлов.</span><span class="sxs-lookup"><span data-stu-id="b5230-126">For example, this can occur when printing large EMF files.</span></span> <span data-ttu-id="b5230-127">Ограничение размера страницы зависит от многих факторов, включая объем доступной виртуальной памяти, объем памяти, выделенной вызывающими процессами, и объем фрагментации в куче процесса.</span><span class="sxs-lookup"><span data-stu-id="b5230-127">The page size limit depends on many factors including the amount of virtual memory available, the amount of memory allocated by calling processes, and the amount of fragmentation in the process heap.</span></span>

## <a name="requirements"></a><span data-ttu-id="b5230-128">Требования</span><span class="sxs-lookup"><span data-stu-id="b5230-128">Requirements</span></span>



| <span data-ttu-id="b5230-129">Требование</span><span class="sxs-lookup"><span data-stu-id="b5230-129">Requirement</span></span> | <span data-ttu-id="b5230-130">Значение</span><span class="sxs-lookup"><span data-stu-id="b5230-130">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="b5230-131">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="b5230-131">Minimum supported client</span></span><br/> | <span data-ttu-id="b5230-132">Windows 2000 Professional \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="b5230-132">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                                |
| <span data-ttu-id="b5230-133">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="b5230-133">Minimum supported server</span></span><br/> | <span data-ttu-id="b5230-134">Windows 2000 Server \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="b5230-134">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                      |
| <span data-ttu-id="b5230-135">Заголовок</span><span class="sxs-lookup"><span data-stu-id="b5230-135">Header</span></span><br/>                   | <dl> <span data-ttu-id="b5230-136"><dt>Винспул. h (включение Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="b5230-136"><dt>Winspool.h (include Windows.h)</dt></span></span> </dl> |
| <span data-ttu-id="b5230-137">Библиотека</span><span class="sxs-lookup"><span data-stu-id="b5230-137">Library</span></span><br/>                  | <dl> <span data-ttu-id="b5230-138"><dt>Винспул. lib</dt></span><span class="sxs-lookup"><span data-stu-id="b5230-138"><dt>Winspool.lib</dt></span></span> </dl>                   |
| <span data-ttu-id="b5230-139">DLL</span><span class="sxs-lookup"><span data-stu-id="b5230-139">DLL</span></span><br/>                      | <dl> <span data-ttu-id="b5230-140"><dt>Spoolss.dll</dt></span><span class="sxs-lookup"><span data-stu-id="b5230-140"><dt>Spoolss.dll</dt></span></span> </dl>                    |



## <a name="see-also"></a><span data-ttu-id="b5230-141">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="b5230-141">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b5230-142">Вывод на печать</span><span class="sxs-lookup"><span data-stu-id="b5230-142">Printing</span></span>](printdocs-printing.md)
</dt> <dt>

[<span data-ttu-id="b5230-143">Функции API очереди печати принтера</span><span class="sxs-lookup"><span data-stu-id="b5230-143">Print Spooler API Functions</span></span>](printing-and-print-spooler-functions.md)
</dt> <dt>

[<span data-ttu-id="b5230-144">**енддокпринтер**</span><span class="sxs-lookup"><span data-stu-id="b5230-144">**EndDocPrinter**</span></span>](enddocprinter.md)
</dt> <dt>

[<span data-ttu-id="b5230-145">**ендпажепринтер**</span><span class="sxs-lookup"><span data-stu-id="b5230-145">**EndPagePrinter**</span></span>](endpageprinter.md)
</dt> <dt>

[<span data-ttu-id="b5230-146">**стартдокпринтер**</span><span class="sxs-lookup"><span data-stu-id="b5230-146">**StartDocPrinter**</span></span>](startdocprinter.md)
</dt> <dt>

[<span data-ttu-id="b5230-147">**стартпажепринтер**</span><span class="sxs-lookup"><span data-stu-id="b5230-147">**StartPagePrinter**</span></span>](startpageprinter.md)
</dt> <dt>

[<span data-ttu-id="b5230-148">**вритепринтер**</span><span class="sxs-lookup"><span data-stu-id="b5230-148">**WritePrinter**</span></span>](writeprinter.md)
</dt> </dl>

 

 




