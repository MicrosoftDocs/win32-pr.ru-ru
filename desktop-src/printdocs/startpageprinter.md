---
description: Функция Стартпажепринтер уведомляет Диспетчер очереди печати, что страница будет напечатана на указанном принтере.
ms.assetid: 8ac7c47b-b3a7-4642-bfb7-54e014139fbf
title: Функция Стартпажепринтер (Винспул. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- StartPagePrinter
api_type:
- DllExport
api_location:
- Spoolss.dll
ms.openlocfilehash: f8d1c5cc296fae1b166b891fc881a6abcdb6b2af
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "103998383"
---
# <a name="startpageprinter-function"></a><span data-ttu-id="6948e-103">Функция Стартпажепринтер</span><span class="sxs-lookup"><span data-stu-id="6948e-103">StartPagePrinter function</span></span>

<span data-ttu-id="6948e-104">Функция **стартпажепринтер** уведомляет Диспетчер очереди печати, что страница будет напечатана на указанном принтере.</span><span class="sxs-lookup"><span data-stu-id="6948e-104">The **StartPagePrinter** function notifies the spooler that a page is about to be printed on the specified printer.</span></span>

## <a name="syntax"></a><span data-ttu-id="6948e-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="6948e-105">Syntax</span></span>


```C++
BOOL StartPagePrinter(
  _In_ HANDLE hPrinter
);
```



## <a name="parameters"></a><span data-ttu-id="6948e-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="6948e-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="6948e-107">*хпринтер* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="6948e-107">*hPrinter* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="6948e-108">Работа с принтером.</span><span class="sxs-lookup"><span data-stu-id="6948e-108">Handle to a printer.</span></span> <span data-ttu-id="6948e-109">Используйте функцию [**опенпринтер**](openprinter.md) или [**аддпринтер**](addprinter.md) для получения маркера принтера.</span><span class="sxs-lookup"><span data-stu-id="6948e-109">Use the [**OpenPrinter**](openprinter.md) or [**AddPrinter**](addprinter.md) function to retrieve a printer handle.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="6948e-110">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="6948e-110">Return value</span></span>

<span data-ttu-id="6948e-111">Если функция выполнена, возвращаемое значение будет ненулевым.</span><span class="sxs-lookup"><span data-stu-id="6948e-111">If the function succeeds, the return value is a nonzero value.</span></span>

<span data-ttu-id="6948e-112">Если функция выполняется неудачно, возвращается нулевое значение.</span><span class="sxs-lookup"><span data-stu-id="6948e-112">If the function fails, the return value is zero.</span></span>

## <a name="remarks"></a><span data-ttu-id="6948e-113">Комментарии</span><span class="sxs-lookup"><span data-stu-id="6948e-113">Remarks</span></span>

> [!Note]  
> <span data-ttu-id="6948e-114">Это блокирующая или синхронная функция, которая может не возвращать значение немедленно.</span><span class="sxs-lookup"><span data-stu-id="6948e-114">This is a blocking or synchronous function and might not return immediately.</span></span> <span data-ttu-id="6948e-115">Скорость возврата этой функцией зависит от факторов времени выполнения, таких как состояние сети, Конфигурация сервера печати и факторы реализации драйвера принтера, которые трудно предсказать при написании приложения.</span><span class="sxs-lookup"><span data-stu-id="6948e-115">How quickly this function returns depends on run-time factors such as network status, print server configuration, and printer driver implementation factors that are difficult to predict when writing an application.</span></span> <span data-ttu-id="6948e-116">Вызов этой функции из потока, который управляет взаимодействием с пользовательским интерфейсом, может привести к невозможности реагирования приложения.</span><span class="sxs-lookup"><span data-stu-id="6948e-116">Calling this function from a thread that manages interaction with the user interface could make the application appear to be unresponsive.</span></span>

 

<span data-ttu-id="6948e-117">Последовательность для задания печати выглядит следующим образом:</span><span class="sxs-lookup"><span data-stu-id="6948e-117">The sequence for a print job is as follows:</span></span>

1.  <span data-ttu-id="6948e-118">Чтобы начать задание печати, вызовите [**стартдокпринтер**](startdocprinter.md).</span><span class="sxs-lookup"><span data-stu-id="6948e-118">To begin a print job, call [**StartDocPrinter**](startdocprinter.md).</span></span>
2.  <span data-ttu-id="6948e-119">Чтобы начать каждую страницу, вызовите **стартпажепринтер**.</span><span class="sxs-lookup"><span data-stu-id="6948e-119">To begin each page, call **StartPagePrinter**.</span></span>
3.  <span data-ttu-id="6948e-120">Чтобы записать данные на страницу, вызовите [**вритепринтер**](writeprinter.md).</span><span class="sxs-lookup"><span data-stu-id="6948e-120">To write data to a page, call [**WritePrinter**](writeprinter.md).</span></span>
4.  <span data-ttu-id="6948e-121">Чтобы завершить каждую страницу, вызовите [**ендпажепринтер**](endpageprinter.md).</span><span class="sxs-lookup"><span data-stu-id="6948e-121">To end each page, call [**EndPagePrinter**](endpageprinter.md).</span></span>
5.  <span data-ttu-id="6948e-122">Повторите 2, 3 и 4 для требуемого количества страниц.</span><span class="sxs-lookup"><span data-stu-id="6948e-122">Repeat 2, 3, and 4 for as many pages as necessary.</span></span>
6.  <span data-ttu-id="6948e-123">Чтобы завершить задание печати, вызовите [**енддокпринтер**](enddocprinter.md).</span><span class="sxs-lookup"><span data-stu-id="6948e-123">To end the print job, call [**EndDocPrinter**](enddocprinter.md).</span></span>

<span data-ttu-id="6948e-124">Если страница в буферизованном файле превышает приблизительно 350 МБ, она может не печататься и не отправить сообщение об ошибке.</span><span class="sxs-lookup"><span data-stu-id="6948e-124">When a page in a spooled file exceeds approximately 350 MB, it can fail to print and not send an error message.</span></span> <span data-ttu-id="6948e-125">Например, это может произойти при печати больших EMF файлов.</span><span class="sxs-lookup"><span data-stu-id="6948e-125">For example, this can occur when printing large EMF files.</span></span> <span data-ttu-id="6948e-126">Ограничение размера страницы зависит от многих факторов, включая объем доступной виртуальной памяти, объем памяти, выделенной вызывающими процессами, и объем фрагментации в куче процесса.</span><span class="sxs-lookup"><span data-stu-id="6948e-126">The page size limit depends on many factors including the amount of virtual memory available, the amount of memory allocated by calling processes, and the amount of fragmentation in the process heap.</span></span>

## <a name="examples"></a><span data-ttu-id="6948e-127">Примеры</span><span class="sxs-lookup"><span data-stu-id="6948e-127">Examples</span></span>

<span data-ttu-id="6948e-128">Пример программы, использующей эту функцию, см. в разделе [инструкции. печать с помощью API печати GDI](how-to--print-using-the-gdi-print-api.md).</span><span class="sxs-lookup"><span data-stu-id="6948e-128">For a sample program that uses this function, see [How To: Print Using the GDI Print API](how-to--print-using-the-gdi-print-api.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="6948e-129">Требования</span><span class="sxs-lookup"><span data-stu-id="6948e-129">Requirements</span></span>



| <span data-ttu-id="6948e-130">Требование</span><span class="sxs-lookup"><span data-stu-id="6948e-130">Requirement</span></span> | <span data-ttu-id="6948e-131">Значение</span><span class="sxs-lookup"><span data-stu-id="6948e-131">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="6948e-132">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="6948e-132">Minimum supported client</span></span><br/> | <span data-ttu-id="6948e-133">Windows 2000 Professional \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="6948e-133">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                                |
| <span data-ttu-id="6948e-134">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="6948e-134">Minimum supported server</span></span><br/> | <span data-ttu-id="6948e-135">Windows 2000 Server \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="6948e-135">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                      |
| <span data-ttu-id="6948e-136">Заголовок</span><span class="sxs-lookup"><span data-stu-id="6948e-136">Header</span></span><br/>                   | <dl> <span data-ttu-id="6948e-137"><dt>Винспул. h (включение Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="6948e-137"><dt>Winspool.h (include Windows.h)</dt></span></span> </dl> |
| <span data-ttu-id="6948e-138">Библиотека</span><span class="sxs-lookup"><span data-stu-id="6948e-138">Library</span></span><br/>                  | <dl> <span data-ttu-id="6948e-139"><dt>Винспул. lib</dt></span><span class="sxs-lookup"><span data-stu-id="6948e-139"><dt>Winspool.lib</dt></span></span> </dl>                   |
| <span data-ttu-id="6948e-140">DLL</span><span class="sxs-lookup"><span data-stu-id="6948e-140">DLL</span></span><br/>                      | <dl> <span data-ttu-id="6948e-141"><dt>Spoolss.dll</dt></span><span class="sxs-lookup"><span data-stu-id="6948e-141"><dt>Spoolss.dll</dt></span></span> </dl>                    |



## <a name="see-also"></a><span data-ttu-id="6948e-142">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="6948e-142">See also</span></span>

<dl> <dt>

[<span data-ttu-id="6948e-143">Вывод на печать</span><span class="sxs-lookup"><span data-stu-id="6948e-143">Printing</span></span>](printdocs-printing.md)
</dt> <dt>

[<span data-ttu-id="6948e-144">Функции API очереди печати принтера</span><span class="sxs-lookup"><span data-stu-id="6948e-144">Print Spooler API Functions</span></span>](printing-and-print-spooler-functions.md)
</dt> <dt>

[<span data-ttu-id="6948e-145">**енддокпринтер**</span><span class="sxs-lookup"><span data-stu-id="6948e-145">**EndDocPrinter**</span></span>](enddocprinter.md)
</dt> <dt>

[<span data-ttu-id="6948e-146">**ендпажепринтер**</span><span class="sxs-lookup"><span data-stu-id="6948e-146">**EndPagePrinter**</span></span>](endpageprinter.md)
</dt> <dt>

[<span data-ttu-id="6948e-147">**опенпринтер**</span><span class="sxs-lookup"><span data-stu-id="6948e-147">**OpenPrinter**</span></span>](openprinter.md)
</dt> <dt>

[<span data-ttu-id="6948e-148">**стартдокпринтер**</span><span class="sxs-lookup"><span data-stu-id="6948e-148">**StartDocPrinter**</span></span>](startdocprinter.md)
</dt> <dt>

[<span data-ttu-id="6948e-149">**стартпажепринтер**</span><span class="sxs-lookup"><span data-stu-id="6948e-149">**StartPagePrinter**</span></span>](startpageprinter.md)
</dt> <dt>

[<span data-ttu-id="6948e-150">**вритепринтер**</span><span class="sxs-lookup"><span data-stu-id="6948e-150">**WritePrinter**</span></span>](writeprinter.md)
</dt> </dl>

 

 




