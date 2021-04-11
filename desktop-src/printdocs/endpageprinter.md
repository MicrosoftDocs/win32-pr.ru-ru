---
description: Функция Ендпажепринтер уведомляет Диспетчер очереди печати о том, что приложение находится в конце страницы в задании печати.
ms.assetid: aceb88b9-375b-4cd2-996a-c369f590154e
title: Функция Ендпажепринтер (Винспул. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- EndPagePrinter
api_type:
- DllExport
api_location:
- Spoolss.dll
ms.openlocfilehash: 45e8ce005953e07f10ec621660ed38e68d50c62b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104156443"
---
# <a name="endpageprinter-function"></a><span data-ttu-id="9bd8a-103">Функция Ендпажепринтер</span><span class="sxs-lookup"><span data-stu-id="9bd8a-103">EndPagePrinter function</span></span>

<span data-ttu-id="9bd8a-104">Функция **ендпажепринтер** уведомляет Диспетчер очереди печати о том, что приложение находится в конце страницы в задании печати.</span><span class="sxs-lookup"><span data-stu-id="9bd8a-104">The **EndPagePrinter** function notifies the print spooler that the application is at the end of a page in a print job.</span></span>

## <a name="syntax"></a><span data-ttu-id="9bd8a-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="9bd8a-105">Syntax</span></span>


```C++
BOOL EndPagePrinter(
  _In_ HANDLE hPrinter
);
```



## <a name="parameters"></a><span data-ttu-id="9bd8a-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="9bd8a-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="9bd8a-107">*хпринтер* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="9bd8a-107">*hPrinter* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="9bd8a-108">Обработайте с принтером, для которого страница будет закончена.</span><span class="sxs-lookup"><span data-stu-id="9bd8a-108">Handle to the printer for which the page will be concluded.</span></span> <span data-ttu-id="9bd8a-109">Используйте функцию [**опенпринтер**](openprinter.md) или [**аддпринтер**](addprinter.md) для получения маркера принтера.</span><span class="sxs-lookup"><span data-stu-id="9bd8a-109">Use the [**OpenPrinter**](openprinter.md) or [**AddPrinter**](addprinter.md) function to retrieve a printer handle.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="9bd8a-110">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="9bd8a-110">Return value</span></span>

<span data-ttu-id="9bd8a-111">Если функция выполнена, возвращаемое значение будет ненулевым.</span><span class="sxs-lookup"><span data-stu-id="9bd8a-111">If the function succeeds, the return value is a nonzero value.</span></span>

<span data-ttu-id="9bd8a-112">Если функция выполняется неудачно, возвращается нулевое значение.</span><span class="sxs-lookup"><span data-stu-id="9bd8a-112">If the function fails, the return value is zero.</span></span>

## <a name="remarks"></a><span data-ttu-id="9bd8a-113">Комментарии</span><span class="sxs-lookup"><span data-stu-id="9bd8a-113">Remarks</span></span>

> [!Note]  
> <span data-ttu-id="9bd8a-114">Это блокирующая или синхронная функция, которая может не возвращать значение немедленно.</span><span class="sxs-lookup"><span data-stu-id="9bd8a-114">This is a blocking or synchronous function and might not return immediately.</span></span> <span data-ttu-id="9bd8a-115">Скорость возврата этой функцией зависит от факторов времени выполнения, таких как состояние сети, Конфигурация сервера печати и факторы реализации драйвера принтера, которые трудно предсказать при написании приложения.</span><span class="sxs-lookup"><span data-stu-id="9bd8a-115">How quickly this function returns depends on run-time factors such as network status, print server configuration, and printer driver implementation factors that are difficult to predict when writing an application.</span></span> <span data-ttu-id="9bd8a-116">Вызов этой функции из потока, который управляет взаимодействием с пользовательским интерфейсом, может привести к невозможности реагирования приложения.</span><span class="sxs-lookup"><span data-stu-id="9bd8a-116">Calling this function from a thread that manages interaction with the user interface could make the application appear to be unresponsive.</span></span>

 

<span data-ttu-id="9bd8a-117">Последовательность для задания печати выглядит следующим образом:</span><span class="sxs-lookup"><span data-stu-id="9bd8a-117">The sequence for a print job is as follows:</span></span>

1.  <span data-ttu-id="9bd8a-118">Чтобы начать задание печати, вызовите [**стартдокпринтер**](startdocprinter.md).</span><span class="sxs-lookup"><span data-stu-id="9bd8a-118">To begin a print job, call [**StartDocPrinter**](startdocprinter.md).</span></span>
2.  <span data-ttu-id="9bd8a-119">Чтобы начать каждую страницу, вызовите [**стартпажепринтер**](startpageprinter.md).</span><span class="sxs-lookup"><span data-stu-id="9bd8a-119">To begin each page, call [**StartPagePrinter**](startpageprinter.md).</span></span>
3.  <span data-ttu-id="9bd8a-120">Чтобы записать данные на страницу, вызовите [**вритепринтер**](writeprinter.md).</span><span class="sxs-lookup"><span data-stu-id="9bd8a-120">To write data to a page, call [**WritePrinter**](writeprinter.md).</span></span>
4.  <span data-ttu-id="9bd8a-121">Чтобы завершить каждую страницу, вызовите **ендпажепринтер**.</span><span class="sxs-lookup"><span data-stu-id="9bd8a-121">To end each page, call **EndPagePrinter**.</span></span>
5.  <span data-ttu-id="9bd8a-122">Повторите 2, 3 и 4 для требуемого количества страниц.</span><span class="sxs-lookup"><span data-stu-id="9bd8a-122">Repeat 2, 3, and 4 for as many pages as necessary.</span></span>
6.  <span data-ttu-id="9bd8a-123">Чтобы завершить задание печати, вызовите [**енддокпринтер**](enddocprinter.md).</span><span class="sxs-lookup"><span data-stu-id="9bd8a-123">To end the print job, call [**EndDocPrinter**](enddocprinter.md).</span></span>

<span data-ttu-id="9bd8a-124">Если страница в буферизованном файле превышает приблизительно 350 МБ, она может не печататься и не отправить сообщение об ошибке.</span><span class="sxs-lookup"><span data-stu-id="9bd8a-124">When a page in a spooled file exceeds approximately 350 MB, it can fail to print and not send an error message.</span></span> <span data-ttu-id="9bd8a-125">Например, это может произойти при печати больших EMF файлов.</span><span class="sxs-lookup"><span data-stu-id="9bd8a-125">For example, this can occur when printing large EMF files.</span></span> <span data-ttu-id="9bd8a-126">Ограничение размера страницы зависит от многих факторов, включая объем доступной виртуальной памяти, объем памяти, выделенной вызывающими процессами, и объем фрагментации в куче процесса.</span><span class="sxs-lookup"><span data-stu-id="9bd8a-126">The page size limit depends on many factors including the amount of virtual memory available, the amount of memory allocated by calling processes, and the amount of fragmentation in the process heap.</span></span>

## <a name="requirements"></a><span data-ttu-id="9bd8a-127">Требования</span><span class="sxs-lookup"><span data-stu-id="9bd8a-127">Requirements</span></span>



| <span data-ttu-id="9bd8a-128">Требование</span><span class="sxs-lookup"><span data-stu-id="9bd8a-128">Requirement</span></span> | <span data-ttu-id="9bd8a-129">Значение</span><span class="sxs-lookup"><span data-stu-id="9bd8a-129">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="9bd8a-130">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="9bd8a-130">Minimum supported client</span></span><br/> | <span data-ttu-id="9bd8a-131">Windows 2000 Professional \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="9bd8a-131">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                                |
| <span data-ttu-id="9bd8a-132">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="9bd8a-132">Minimum supported server</span></span><br/> | <span data-ttu-id="9bd8a-133">Windows 2000 Server \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="9bd8a-133">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                      |
| <span data-ttu-id="9bd8a-134">Заголовок</span><span class="sxs-lookup"><span data-stu-id="9bd8a-134">Header</span></span><br/>                   | <dl> <span data-ttu-id="9bd8a-135"><dt>Винспул. h (включение Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="9bd8a-135"><dt>Winspool.h (include Windows.h)</dt></span></span> </dl> |
| <span data-ttu-id="9bd8a-136">Библиотека</span><span class="sxs-lookup"><span data-stu-id="9bd8a-136">Library</span></span><br/>                  | <dl> <span data-ttu-id="9bd8a-137"><dt>Винспул. lib</dt></span><span class="sxs-lookup"><span data-stu-id="9bd8a-137"><dt>Winspool.lib</dt></span></span> </dl>                   |
| <span data-ttu-id="9bd8a-138">DLL</span><span class="sxs-lookup"><span data-stu-id="9bd8a-138">DLL</span></span><br/>                      | <dl> <span data-ttu-id="9bd8a-139"><dt>Spoolss.dll</dt></span><span class="sxs-lookup"><span data-stu-id="9bd8a-139"><dt>Spoolss.dll</dt></span></span> </dl>                    |



## <a name="see-also"></a><span data-ttu-id="9bd8a-140">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="9bd8a-140">See also</span></span>

<dl> <dt>

[<span data-ttu-id="9bd8a-141">Вывод на печать</span><span class="sxs-lookup"><span data-stu-id="9bd8a-141">Printing</span></span>](printdocs-printing.md)
</dt> <dt>

[<span data-ttu-id="9bd8a-142">Функции API очереди печати принтера</span><span class="sxs-lookup"><span data-stu-id="9bd8a-142">Print Spooler API Functions</span></span>](printing-and-print-spooler-functions.md)
</dt> <dt>

[<span data-ttu-id="9bd8a-143">**енддокпринтер**</span><span class="sxs-lookup"><span data-stu-id="9bd8a-143">**EndDocPrinter**</span></span>](enddocprinter.md)
</dt> <dt>

[<span data-ttu-id="9bd8a-144">**ендпажепринтер**</span><span class="sxs-lookup"><span data-stu-id="9bd8a-144">**EndPagePrinter**</span></span>](endpageprinter.md)
</dt> <dt>

[<span data-ttu-id="9bd8a-145">**опенпринтер**</span><span class="sxs-lookup"><span data-stu-id="9bd8a-145">**OpenPrinter**</span></span>](openprinter.md)
</dt> <dt>

[<span data-ttu-id="9bd8a-146">**стартдокпринтер**</span><span class="sxs-lookup"><span data-stu-id="9bd8a-146">**StartDocPrinter**</span></span>](startdocprinter.md)
</dt> <dt>

[<span data-ttu-id="9bd8a-147">**стартпажепринтер**</span><span class="sxs-lookup"><span data-stu-id="9bd8a-147">**StartPagePrinter**</span></span>](startpageprinter.md)
</dt> <dt>

[<span data-ttu-id="9bd8a-148">**вритепринтер**</span><span class="sxs-lookup"><span data-stu-id="9bd8a-148">**WritePrinter**</span></span>](writeprinter.md)
</dt> </dl>

 

 




