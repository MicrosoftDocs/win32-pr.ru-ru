---
description: Функция Стартдокпринтер уведомляет Диспетчер очереди печати, что документ должен быть помещен в очередь для печати.
ms.assetid: caa2bd80-4af3-4968-a5b9-d12f16cac6fc
title: Функция Стартдокпринтер (Винспул. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- StartDocPrinter
- StartDocPrinterA
- StartDocPrinterW
api_type:
- DllExport
api_location:
- Winspool.drv
- Ext-MS-Win-Printer-WinSpool-l1-1-2.dll
- Ext-MS-Win-Printer-WinSpool-L1-1-3.dll
ms.openlocfilehash: f8bdb0ae08c88e553dad3a91f0f1a578bed4ad39
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "103912643"
---
# <a name="startdocprinter-function"></a><span data-ttu-id="e9117-103">Функция Стартдокпринтер</span><span class="sxs-lookup"><span data-stu-id="e9117-103">StartDocPrinter function</span></span>

<span data-ttu-id="e9117-104">Функция **стартдокпринтер** уведомляет Диспетчер очереди печати, что документ должен быть помещен в очередь для печати.</span><span class="sxs-lookup"><span data-stu-id="e9117-104">The **StartDocPrinter** function notifies the print spooler that a document is to be spooled for printing.</span></span>

## <a name="syntax"></a><span data-ttu-id="e9117-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="e9117-105">Syntax</span></span>


```C++
DWORD StartDocPrinter(
  _In_ HANDLE hPrinter,
  _In_ DWORD  Level,
  _In_ LPBYTE pDocInfo
);
```



## <a name="parameters"></a><span data-ttu-id="e9117-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="e9117-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="e9117-107">*хпринтер* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="e9117-107">*hPrinter* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="e9117-108">Маркер принтера.</span><span class="sxs-lookup"><span data-stu-id="e9117-108">A handle to the printer.</span></span> <span data-ttu-id="e9117-109">Используйте функцию [**опенпринтер**](openprinter.md) или [**аддпринтер**](addprinter.md) для получения маркера принтера.</span><span class="sxs-lookup"><span data-stu-id="e9117-109">Use the [**OpenPrinter**](openprinter.md) or [**AddPrinter**](addprinter.md) function to retrieve a printer handle.</span></span>

</dd> <dt>

<span data-ttu-id="e9117-110">*Уровень* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="e9117-110">*Level* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="e9117-111">Версия структуры, на которую указывает *пдоЦинфо* .</span><span class="sxs-lookup"><span data-stu-id="e9117-111">The version of the structure to which *pDocInfo* points.</span></span> <span data-ttu-id="e9117-112">Это значение должно быть равно 1.</span><span class="sxs-lookup"><span data-stu-id="e9117-112">This value must be 1.</span></span>

</dd> <dt>

<span data-ttu-id="e9117-113">*пдоЦинфо* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="e9117-113">*pDocInfo* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="e9117-114">Указатель на структуру документа [**с \_ информацией \_ 1**](doc-info-1.md) , описывающую документ для печати.</span><span class="sxs-lookup"><span data-stu-id="e9117-114">A pointer to a [**DOC\_INFO\_1**](doc-info-1.md) structure that describes the document to print.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="e9117-115">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="e9117-115">Return value</span></span>

<span data-ttu-id="e9117-116">Если функция выполнена, возвращаемое значение идентифицирует задание печати.</span><span class="sxs-lookup"><span data-stu-id="e9117-116">If the function succeeds, the return value identifies the print job.</span></span>

<span data-ttu-id="e9117-117">Если функция выполняется неудачно, возвращается нулевое значение.</span><span class="sxs-lookup"><span data-stu-id="e9117-117">If the function fails, the return value is zero.</span></span>

## <a name="remarks"></a><span data-ttu-id="e9117-118">Комментарии</span><span class="sxs-lookup"><span data-stu-id="e9117-118">Remarks</span></span>

> [!Note]  
> <span data-ttu-id="e9117-119">Это блокирующая или синхронная функция, которая может не возвращать значение немедленно.</span><span class="sxs-lookup"><span data-stu-id="e9117-119">This is a blocking or synchronous function and might not return immediately.</span></span> <span data-ttu-id="e9117-120">Скорость возврата этой функцией зависит от факторов времени выполнения, таких как состояние сети, Конфигурация сервера печати и факторы реализации драйвера принтера, которые трудно предсказать при написании приложения.</span><span class="sxs-lookup"><span data-stu-id="e9117-120">How quickly this function returns depends on run-time factors such as network status, print server configuration, and printer driver implementation factors that are difficult to predict when writing an application.</span></span> <span data-ttu-id="e9117-121">Вызов этой функции из потока, который управляет взаимодействием с пользовательским интерфейсом, может привести к невозможности реагирования приложения.</span><span class="sxs-lookup"><span data-stu-id="e9117-121">Calling this function from a thread that manages interaction with the user interface could make the application appear to be unresponsive.</span></span>

 

<span data-ttu-id="e9117-122">Типичная последовательность задания печати выглядит следующим образом:</span><span class="sxs-lookup"><span data-stu-id="e9117-122">The typical sequence for a print job is as follows:</span></span>

1.  <span data-ttu-id="e9117-123">Чтобы начать задание печати, вызовите **стартдокпринтер**.</span><span class="sxs-lookup"><span data-stu-id="e9117-123">To begin a print job, call **StartDocPrinter**.</span></span>
2.  <span data-ttu-id="e9117-124">Чтобы начать каждую страницу, вызовите [**стартпажепринтер**](startpageprinter.md).</span><span class="sxs-lookup"><span data-stu-id="e9117-124">To begin each page, call [**StartPagePrinter**](startpageprinter.md).</span></span>
3.  <span data-ttu-id="e9117-125">Чтобы записать данные на страницу, вызовите [**вритепринтер**](writeprinter.md).</span><span class="sxs-lookup"><span data-stu-id="e9117-125">To write data to a page, call [**WritePrinter**](writeprinter.md).</span></span>
4.  <span data-ttu-id="e9117-126">Чтобы завершить каждую страницу, вызовите [**ендпажепринтер**](endpageprinter.md).</span><span class="sxs-lookup"><span data-stu-id="e9117-126">To end each page, call [**EndPagePrinter**](endpageprinter.md).</span></span>
5.  <span data-ttu-id="e9117-127">Повторите 2, 3 и 4 для требуемого количества страниц.</span><span class="sxs-lookup"><span data-stu-id="e9117-127">Repeat 2, 3, and 4 for as many pages as necessary.</span></span>
6.  <span data-ttu-id="e9117-128">Чтобы завершить задание печати, вызовите [**енддокпринтер**](enddocprinter.md).</span><span class="sxs-lookup"><span data-stu-id="e9117-128">To end the print job, call [**EndDocPrinter**](enddocprinter.md).</span></span>

<span data-ttu-id="e9117-129">Обратите внимание, что вызов [**стартпажепринтер**](startpageprinter.md) и [**ендпажепринтер**](endpageprinter.md) может быть необязательным, например, если тип данных печати включает сведения о странице.</span><span class="sxs-lookup"><span data-stu-id="e9117-129">Note that calling [**StartPagePrinter**](startpageprinter.md) and [**EndPagePrinter**](endpageprinter.md) may not be necessary, such as if the print data type includes the page information.</span></span>

<span data-ttu-id="e9117-130">Если страница в буферизованном файле превышает приблизительно 350 МБ, она может не печататься и не отправить сообщение об ошибке.</span><span class="sxs-lookup"><span data-stu-id="e9117-130">When a page in a spooled file exceeds approximately 350 MB, it can fail to print and not send an error message.</span></span> <span data-ttu-id="e9117-131">Например, это может произойти при печати больших EMF файлов.</span><span class="sxs-lookup"><span data-stu-id="e9117-131">For example, this can occur when printing large EMF files.</span></span> <span data-ttu-id="e9117-132">Ограничение размера страницы зависит от многих факторов, включая объем доступной виртуальной памяти, объем памяти, выделенной вызывающими процессами, и объем фрагментации в куче процесса.</span><span class="sxs-lookup"><span data-stu-id="e9117-132">The page size limit depends on many factors including the amount of virtual memory available, the amount of memory allocated by calling processes, and the amount of fragmentation in the process heap.</span></span>

## <a name="examples"></a><span data-ttu-id="e9117-133">Примеры</span><span class="sxs-lookup"><span data-stu-id="e9117-133">Examples</span></span>

<span data-ttu-id="e9117-134">Пример программы, использующей эту функцию, см. в разделе [инструкции. печать с помощью API печати GDI](how-to--print-using-the-gdi-print-api.md).</span><span class="sxs-lookup"><span data-stu-id="e9117-134">For a sample program that uses this function, see [How To: Print Using the GDI Print API](how-to--print-using-the-gdi-print-api.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="e9117-135">Требования</span><span class="sxs-lookup"><span data-stu-id="e9117-135">Requirements</span></span>



| <span data-ttu-id="e9117-136">Требование</span><span class="sxs-lookup"><span data-stu-id="e9117-136">Requirement</span></span> | <span data-ttu-id="e9117-137">Значение</span><span class="sxs-lookup"><span data-stu-id="e9117-137">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="e9117-138">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="e9117-138">Minimum supported client</span></span><br/> | <span data-ttu-id="e9117-139">Windows 2000 Professional \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="e9117-139">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                                |
| <span data-ttu-id="e9117-140">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="e9117-140">Minimum supported server</span></span><br/> | <span data-ttu-id="e9117-141">Windows 2000 Server \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="e9117-141">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                      |
| <span data-ttu-id="e9117-142">Заголовок</span><span class="sxs-lookup"><span data-stu-id="e9117-142">Header</span></span><br/>                   | <dl> <span data-ttu-id="e9117-143"><dt>Винспул. h (включение Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="e9117-143"><dt>Winspool.h (include Windows.h)</dt></span></span> </dl> |
| <span data-ttu-id="e9117-144">Библиотека</span><span class="sxs-lookup"><span data-stu-id="e9117-144">Library</span></span><br/>                  | <dl> <span data-ttu-id="e9117-145"><dt>Винспул. lib</dt></span><span class="sxs-lookup"><span data-stu-id="e9117-145"><dt>Winspool.lib</dt></span></span> </dl>                   |
| <span data-ttu-id="e9117-146">DLL</span><span class="sxs-lookup"><span data-stu-id="e9117-146">DLL</span></span><br/>                      | <dl> <span data-ttu-id="e9117-147"><dt>Винспул. drv</dt></span><span class="sxs-lookup"><span data-stu-id="e9117-147"><dt>Winspool.drv</dt></span></span> </dl>                   |
| <span data-ttu-id="e9117-148">Имя в кодировке Юникод и ANSI</span><span class="sxs-lookup"><span data-stu-id="e9117-148">Unicode and ANSI names</span></span><br/>   | <span data-ttu-id="e9117-149">**Стартдокпринтерв** (Юникод) и **стартдокпринтера** (ANSI)</span><span class="sxs-lookup"><span data-stu-id="e9117-149">**StartDocPrinterW** (Unicode) and **StartDocPrinterA** (ANSI)</span></span><br/>                                 |



## <a name="see-also"></a><span data-ttu-id="e9117-150">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="e9117-150">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e9117-151">**AddJob**</span><span class="sxs-lookup"><span data-stu-id="e9117-151">**AddJob**</span></span>](addjob.md)
</dt> <dt>

[<span data-ttu-id="e9117-152">**\_Сведения о документе \_ 1**</span><span class="sxs-lookup"><span data-stu-id="e9117-152">**DOC\_INFO\_1**</span></span>](doc-info-1.md)
</dt> <dt>

[<span data-ttu-id="e9117-153">**\_Сведения о документе \_ 2**</span><span class="sxs-lookup"><span data-stu-id="e9117-153">**DOC\_INFO\_2**</span></span>](doc-info-2.md)
</dt> <dt>

[<span data-ttu-id="e9117-154">**енддокпринтер**</span><span class="sxs-lookup"><span data-stu-id="e9117-154">**EndDocPrinter**</span></span>](enddocprinter.md)
</dt> <dt>

[<span data-ttu-id="e9117-155">**ендпажепринтер**</span><span class="sxs-lookup"><span data-stu-id="e9117-155">**EndPagePrinter**</span></span>](endpageprinter.md)
</dt> <dt>

[<span data-ttu-id="e9117-156">**опенпринтер**</span><span class="sxs-lookup"><span data-stu-id="e9117-156">**OpenPrinter**</span></span>](openprinter.md)
</dt> <dt>

[<span data-ttu-id="e9117-157">Вывод на печать</span><span class="sxs-lookup"><span data-stu-id="e9117-157">Printing</span></span>](printdocs-printing.md)
</dt> <dt>

[<span data-ttu-id="e9117-158">Функции API очереди печати принтера</span><span class="sxs-lookup"><span data-stu-id="e9117-158">Print Spooler API Functions</span></span>](printing-and-print-spooler-functions.md)
</dt> <dt>

[<span data-ttu-id="e9117-159">**стартдокпринтер**</span><span class="sxs-lookup"><span data-stu-id="e9117-159">**StartDocPrinter**</span></span>](startdocprinter.md)
</dt> <dt>

[<span data-ttu-id="e9117-160">**стартпажепринтер**</span><span class="sxs-lookup"><span data-stu-id="e9117-160">**StartPagePrinter**</span></span>](startpageprinter.md)
</dt> <dt>

[<span data-ttu-id="e9117-161">**вритепринтер**</span><span class="sxs-lookup"><span data-stu-id="e9117-161">**WritePrinter**</span></span>](writeprinter.md)
</dt> </dl>

 

 




