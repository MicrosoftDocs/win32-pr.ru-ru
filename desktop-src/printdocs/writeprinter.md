---
description: Функция Вритепринтер уведомляет Диспетчер очереди печати, что данные должны быть записаны на указанный принтер.
ms.assetid: 9411b71f-d686-44ed-9051-d410e5ab228e
title: Функция Вритепринтер (Винспул. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- WritePrinter
api_type:
- DllExport
api_location:
- Spoolss.dll
- Ext-MS-Win-Printer-WinSpool-l1-1-2.dll
- WinSpool.Drv
- Ext-MS-Win-Printer-WinSpool-L1-1-3.dll
ms.openlocfilehash: 490221b15ed1e3c7dad3a4cb523c15e9ec484b13
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "105711995"
---
# <a name="writeprinter-function"></a><span data-ttu-id="983d1-103">Функция Вритепринтер</span><span class="sxs-lookup"><span data-stu-id="983d1-103">WritePrinter function</span></span>

<span data-ttu-id="983d1-104">Функция **вритепринтер** уведомляет Диспетчер очереди печати, что данные должны быть записаны на указанный принтер.</span><span class="sxs-lookup"><span data-stu-id="983d1-104">The **WritePrinter** function notifies the print spooler that data should be written to the specified printer.</span></span>

> [!Note]  
> <span data-ttu-id="983d1-105">**Вритепринтер** поддерживает только печать GDI и не может использоваться для печати XPS.</span><span class="sxs-lookup"><span data-stu-id="983d1-105">**WritePrinter** only supports GDI printing and must not be used for XPS printing.</span></span> <span data-ttu-id="983d1-106">Если в задании печати используется XPS или Опенкспс печати, используйте [API печати XPS](/windows/desktop/printdocs/xps-printing).</span><span class="sxs-lookup"><span data-stu-id="983d1-106">If your print job uses the XPS or the OpenXPS print path, then use the [XPS Print API](/windows/desktop/printdocs/xps-printing).</span></span> <span data-ttu-id="983d1-107">Отправка заданий печати XPS или Опенкспс в Диспетчер очереди с помощью **вритепринтер** не поддерживается и может привести к неопределенному результату.</span><span class="sxs-lookup"><span data-stu-id="983d1-107">Sending XPS or OpenXPS print jobs to the spooler using **WritePrinter** is not supported and can result in undetermined results.</span></span>

 

## <a name="syntax"></a><span data-ttu-id="983d1-108">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="983d1-108">Syntax</span></span>


```C++
BOOL WritePrinter(
  _In_  HANDLE  hPrinter,
  _In_  LPVOID  pBuf,
  _In_  DWORD   cbBuf,
  _Out_ LPDWORD pcWritten
);
```



## <a name="parameters"></a><span data-ttu-id="983d1-109">Параметры</span><span class="sxs-lookup"><span data-stu-id="983d1-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="983d1-110">*хпринтер* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="983d1-110">*hPrinter* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="983d1-111">Маркер принтера.</span><span class="sxs-lookup"><span data-stu-id="983d1-111">A handle to the printer.</span></span> <span data-ttu-id="983d1-112">Используйте функцию [**опенпринтер**](openprinter.md) или [**аддпринтер**](addprinter.md) для получения маркера принтера.</span><span class="sxs-lookup"><span data-stu-id="983d1-112">Use the [**OpenPrinter**](openprinter.md) or [**AddPrinter**](addprinter.md) function to retrieve a printer handle.</span></span>

</dd> <dt>

<span data-ttu-id="983d1-113">*пбуф* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="983d1-113">*pBuf* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="983d1-114">Указатель на массив байтов, содержащий данные, которые должны быть записаны на принтер.</span><span class="sxs-lookup"><span data-stu-id="983d1-114">A pointer to an array of bytes that contains the data that should be written to the printer.</span></span>

</dd> <dt>

<span data-ttu-id="983d1-115">*кббуф* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="983d1-115">*cbBuf* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="983d1-116">Размер массива в байтах.</span><span class="sxs-lookup"><span data-stu-id="983d1-116">The size, in bytes, of the array.</span></span>

</dd> <dt>

<span data-ttu-id="983d1-117">*пквриттен* \[ заполняет\]</span><span class="sxs-lookup"><span data-stu-id="983d1-117">*pcWritten* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="983d1-118">Указатель на значение, которое получает число байтов данных, записанных на принтер.</span><span class="sxs-lookup"><span data-stu-id="983d1-118">A pointer to a value that receives the number of bytes of data that were written to the printer.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="983d1-119">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="983d1-119">Return value</span></span>

<span data-ttu-id="983d1-120">Если функция выполнена, возвращаемое значение будет ненулевым.</span><span class="sxs-lookup"><span data-stu-id="983d1-120">If the function succeeds, the return value is a nonzero value.</span></span>

<span data-ttu-id="983d1-121">Если функция выполняется неудачно, возвращается нулевое значение.</span><span class="sxs-lookup"><span data-stu-id="983d1-121">If the function fails, the return value is zero.</span></span>

## <a name="remarks"></a><span data-ttu-id="983d1-122">Комментарии</span><span class="sxs-lookup"><span data-stu-id="983d1-122">Remarks</span></span>

> [!Note]  
> <span data-ttu-id="983d1-123">Это блокирующая или синхронная функция, которая может не возвращать значение немедленно.</span><span class="sxs-lookup"><span data-stu-id="983d1-123">This is a blocking or synchronous function and might not return immediately.</span></span> <span data-ttu-id="983d1-124">Скорость возврата этой функцией зависит от факторов времени выполнения, таких как состояние сети, Конфигурация сервера печати и факторы реализации драйвера принтера, которые трудно предсказать при написании приложения.</span><span class="sxs-lookup"><span data-stu-id="983d1-124">How quickly this function returns depends on run-time factors such as network status, print server configuration, and printer driver implementation factors that are difficult to predict when writing an application.</span></span> <span data-ttu-id="983d1-125">Вызов этой функции из потока, который управляет взаимодействием с пользовательским интерфейсом, может привести к невозможности реагирования приложения.</span><span class="sxs-lookup"><span data-stu-id="983d1-125">Calling this function from a thread that manages interaction with the user interface could make the application appear to be unresponsive.</span></span>

 

<span data-ttu-id="983d1-126">Последовательность для задания печати выглядит следующим образом:</span><span class="sxs-lookup"><span data-stu-id="983d1-126">The sequence for a print job is as follows:</span></span>

1.  <span data-ttu-id="983d1-127">Чтобы начать задание печати, вызовите [**стартдокпринтер**](startdocprinter.md).</span><span class="sxs-lookup"><span data-stu-id="983d1-127">To begin a print job, call [**StartDocPrinter**](startdocprinter.md).</span></span>
2.  <span data-ttu-id="983d1-128">Чтобы начать каждую страницу, вызовите [**стартпажепринтер**](startpageprinter.md).</span><span class="sxs-lookup"><span data-stu-id="983d1-128">To begin each page, call [**StartPagePrinter**](startpageprinter.md).</span></span>
3.  <span data-ttu-id="983d1-129">Чтобы записать данные на страницу, вызовите **вритепринтер**.</span><span class="sxs-lookup"><span data-stu-id="983d1-129">To write data to a page, call **WritePrinter**.</span></span>
4.  <span data-ttu-id="983d1-130">Чтобы завершить каждую страницу, вызовите [**ендпажепринтер**](endpageprinter.md).</span><span class="sxs-lookup"><span data-stu-id="983d1-130">To end each page, call [**EndPagePrinter**](endpageprinter.md).</span></span>
5.  <span data-ttu-id="983d1-131">Повторите 2, 3 и 4 для требуемого количества страниц.</span><span class="sxs-lookup"><span data-stu-id="983d1-131">Repeat 2, 3, and 4 for as many pages as necessary.</span></span>
6.  <span data-ttu-id="983d1-132">Чтобы завершить задание печати, вызовите [**енддокпринтер**](enddocprinter.md).</span><span class="sxs-lookup"><span data-stu-id="983d1-132">To end the print job, call [**EndDocPrinter**](enddocprinter.md).</span></span>

<span data-ttu-id="983d1-133">Когда документ высокого уровня (например, файл Adobe PDF или Microsoft Word) или другие данные принтера (такие как PCL, PS или ХПГЛ) отправляются непосредственно на принтер, параметры печати, определенные в документе, вступают в силу по сравнению с параметрами печати Windows.</span><span class="sxs-lookup"><span data-stu-id="983d1-133">When a high-level document (such as an Adobe PDF or Microsoft Word file) or other printer data (such PCL, PS, or HPGL) is sent directly to a printer, the print settings defined in the document take precedent over Windows print settings.</span></span> <span data-ttu-id="983d1-134">Выходные данные документа, если значение элемента *пдататипе* структуры Document [**\_ info \_ 1**](doc-info-1.md) , переданное в параметре *пдоЦинфо* в вызове [**стартдокпринтер**](startdocprinter.md) , — "RAW", должно полностью описать параметры задания печати в стиле [**DEVMODE**](/windows/win32/api/wingdi/ns-wingdi-devmodea)на языке, понятном оборудованию.</span><span class="sxs-lookup"><span data-stu-id="983d1-134">Documents output when the value of the *pDatatype* member of the [**DOC\_INFO\_1**](doc-info-1.md) structure that was passed in the *pDocInfo* parameter of the [**StartDocPrinter**](startdocprinter.md) call is "RAW" must fully describe the [**DEVMODE**](/windows/win32/api/wingdi/ns-wingdi-devmodea)-style print job settings in the language understood by the hardware.</span></span>

<span data-ttu-id="983d1-135">В версиях Windows, предшествовавших Windows XP, если страница в буферизованном файле превышает приблизительно 350 МБ, она может не печататься и не отправить сообщение об ошибке.</span><span class="sxs-lookup"><span data-stu-id="983d1-135">In versions of Windows prior to Windows XP, when a page in a spooled file exceeds approximately 350 MB, it can fail to print and not send an error message.</span></span> <span data-ttu-id="983d1-136">Например, это может произойти при печати больших EMF файлов.</span><span class="sxs-lookup"><span data-stu-id="983d1-136">For example, this can occur when printing large EMF files.</span></span> <span data-ttu-id="983d1-137">Ограничение размера страницы в версиях Windows до Windows XP зависит от многих факторов, включая объем доступной виртуальной памяти, объем памяти, выделенной вызывающими процессами, и объем фрагментации в куче процесса.</span><span class="sxs-lookup"><span data-stu-id="983d1-137">The page size limit in versions of Windows prior to Windows XP depends on many factors including the amount of virtual memory available, the amount of memory allocated by calling processes, and the amount of fragmentation in the process heap.</span></span> <span data-ttu-id="983d1-138">В Windows XP и более поздних версиях Windows файлы EMF должны иметь размер не более 2 ГБ.</span><span class="sxs-lookup"><span data-stu-id="983d1-138">In Windows XP and later versions of Windows, EMF files must be 2GB or less in size.</span></span> <span data-ttu-id="983d1-139">Если **вритепринтер** используется для записи данных без EMF, таких как файл PDL, готовый для печати, размер файла ограничивается только доступным местом на диске.</span><span class="sxs-lookup"><span data-stu-id="983d1-139">If **WritePrinter** is used to write non EMF data, such as printer-ready PDL, the size of the file is limited only by the available disk space.</span></span>

## <a name="examples"></a><span data-ttu-id="983d1-140">Примеры</span><span class="sxs-lookup"><span data-stu-id="983d1-140">Examples</span></span>

<span data-ttu-id="983d1-141">Пример программы, использующей эту функцию, см. в разделе [инструкции. печать с помощью API печати GDI](how-to--print-using-the-gdi-print-api.md).</span><span class="sxs-lookup"><span data-stu-id="983d1-141">For a sample program that uses this function, see [How To: Print Using the GDI Print API](how-to--print-using-the-gdi-print-api.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="983d1-142">Требования</span><span class="sxs-lookup"><span data-stu-id="983d1-142">Requirements</span></span>



| <span data-ttu-id="983d1-143">Требование</span><span class="sxs-lookup"><span data-stu-id="983d1-143">Requirement</span></span> | <span data-ttu-id="983d1-144">Значение</span><span class="sxs-lookup"><span data-stu-id="983d1-144">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="983d1-145">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="983d1-145">Minimum supported client</span></span><br/> | <span data-ttu-id="983d1-146">Windows 2000 Professional \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="983d1-146">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                                |
| <span data-ttu-id="983d1-147">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="983d1-147">Minimum supported server</span></span><br/> | <span data-ttu-id="983d1-148">Windows 2000 Server \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="983d1-148">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                      |
| <span data-ttu-id="983d1-149">Заголовок</span><span class="sxs-lookup"><span data-stu-id="983d1-149">Header</span></span><br/>                   | <dl> <span data-ttu-id="983d1-150"><dt>Винспул. h (включение Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="983d1-150"><dt>Winspool.h (include Windows.h)</dt></span></span> </dl> |
| <span data-ttu-id="983d1-151">Библиотека</span><span class="sxs-lookup"><span data-stu-id="983d1-151">Library</span></span><br/>                  | <dl> <span data-ttu-id="983d1-152"><dt>Винспул. lib</dt></span><span class="sxs-lookup"><span data-stu-id="983d1-152"><dt>Winspool.lib</dt></span></span> </dl>                   |
| <span data-ttu-id="983d1-153">DLL</span><span class="sxs-lookup"><span data-stu-id="983d1-153">DLL</span></span><br/>                      | <dl> <span data-ttu-id="983d1-154"><dt>Spoolss.dll</dt></span><span class="sxs-lookup"><span data-stu-id="983d1-154"><dt>Spoolss.dll</dt></span></span> </dl>                    |



## <a name="see-also"></a><span data-ttu-id="983d1-155">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="983d1-155">See also</span></span>

<dl> <dt>

[<span data-ttu-id="983d1-156">Вывод на печать</span><span class="sxs-lookup"><span data-stu-id="983d1-156">Printing</span></span>](printdocs-printing.md)
</dt> <dt>

[<span data-ttu-id="983d1-157">Функции API очереди печати принтера</span><span class="sxs-lookup"><span data-stu-id="983d1-157">Print Spooler API Functions</span></span>](printing-and-print-spooler-functions.md)
</dt> <dt>

[<span data-ttu-id="983d1-158">**енддокпринтер**</span><span class="sxs-lookup"><span data-stu-id="983d1-158">**EndDocPrinter**</span></span>](enddocprinter.md)
</dt> <dt>

[<span data-ttu-id="983d1-159">**ендпажепринтер**</span><span class="sxs-lookup"><span data-stu-id="983d1-159">**EndPagePrinter**</span></span>](endpageprinter.md)
</dt> <dt>

[<span data-ttu-id="983d1-160">**опенпринтер**</span><span class="sxs-lookup"><span data-stu-id="983d1-160">**OpenPrinter**</span></span>](openprinter.md)
</dt> <dt>

[<span data-ttu-id="983d1-161">**стартдокпринтер**</span><span class="sxs-lookup"><span data-stu-id="983d1-161">**StartDocPrinter**</span></span>](startdocprinter.md)
</dt> <dt>

[<span data-ttu-id="983d1-162">**стартпажепринтер**</span><span class="sxs-lookup"><span data-stu-id="983d1-162">**StartPagePrinter**</span></span>](startpageprinter.md)
</dt> <dt>

[<span data-ttu-id="983d1-163">**вритепринтер**</span><span class="sxs-lookup"><span data-stu-id="983d1-163">**WritePrinter**</span></span>](writeprinter.md)
</dt> </dl>

 

