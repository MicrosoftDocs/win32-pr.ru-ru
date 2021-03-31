---
description: Функция AddJob добавляет задание печати в список заданий печати, которые могут быть запланированы диспетчером очереди печати. Функция возвращает имя файла, который можно использовать для хранения задания.
ms.assetid: cfafa874-6022-4bf4-bf3d-096213eb0c98
title: Функция AddJob (Винспул. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- AddJob
- AddJobA
- AddJobW
api_type:
- DllExport
api_location:
- Winspool.drv
ms.openlocfilehash: ab21b98036975934c00e28d0be1d5670d4c0742c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "103813569"
---
# <a name="addjob-function"></a><span data-ttu-id="6b6bc-104">Функция AddJob</span><span class="sxs-lookup"><span data-stu-id="6b6bc-104">AddJob function</span></span>

<span data-ttu-id="6b6bc-105">Функция **AddJob** добавляет задание печати в список заданий печати, которые могут быть запланированы диспетчером очереди печати.</span><span class="sxs-lookup"><span data-stu-id="6b6bc-105">The **AddJob** function adds a print job to the list of print jobs that can be scheduled by the print spooler.</span></span> <span data-ttu-id="6b6bc-106">Функция возвращает имя файла, который можно использовать для хранения задания.</span><span class="sxs-lookup"><span data-stu-id="6b6bc-106">The function retrieves the name of the file you can use to store the job.</span></span>

> [!NOTE]
> <span data-ttu-id="6b6bc-107">В операционных системах Windows 8 и более поздних версий не рекомендуется использовать **AddJob** напрямую, так как существуют случаи (например, печать в очередь с помощью файла: или портпромпт:). где **AddJob** завершится ошибкой.</span><span class="sxs-lookup"><span data-stu-id="6b6bc-107">In Windows 8 and later operating systems, we do not recommended using **AddJob** directly because there are cases (such as printing to a queue using File: or PORTPROMPT:) where **AddJob** will fail.</span></span> <span data-ttu-id="6b6bc-108">Вместо этого рекомендуется использовать [API печати GDI](gdi-printing.md), [API печати XPS](xps-printing.md), [**стартдокпринтер**](startdocprinter.md)или соответствующий метод из пространства имен [**Windows. Graphics. Printing**](/uwp/api/Windows.Graphics.Printing) в зависимости от сценария печати.</span><span class="sxs-lookup"><span data-stu-id="6b6bc-108">Instead, you are advised to use [GDI Print API](gdi-printing.md), [XPS Print API](xps-printing.md), [**StartDocPrinter**](startdocprinter.md), or the appropriate method from the [**Windows.Graphics.Printing**](/uwp/api/Windows.Graphics.Printing) namespace, depending on the print scenario.</span></span>
>
> <span data-ttu-id="6b6bc-109">Если попытаться выполнить печать в очередь с помощью **файла:** или **портпромпт:**, **AddJob** вернет ошибку Not \_ Supported.</span><span class="sxs-lookup"><span data-stu-id="6b6bc-109">If you try to print to a queue using **File:** or **PORTPROMPT:**, **AddJob** will Return the NOT\_SUPPORTED error.</span></span>

## <a name="syntax"></a><span data-ttu-id="6b6bc-110">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="6b6bc-110">Syntax</span></span>

```C++
BOOL AddJob(
  _In_  HANDLE  hPrinter,
  _In_  DWORD   Level,
  _Out_ LPBYTE  pData,
  _In_  DWORD   cbBuf,
  _Out_ LPDWORD pcbNeeded
);
```

## <a name="parameters"></a><span data-ttu-id="6b6bc-111">Параметры</span><span class="sxs-lookup"><span data-stu-id="6b6bc-111">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="6b6bc-112">*хпринтер* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="6b6bc-112">*hPrinter* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="6b6bc-113">Маркер, указывающий принтер для задания печати.</span><span class="sxs-lookup"><span data-stu-id="6b6bc-113">A handle that specifies the printer for the print job.</span></span> <span data-ttu-id="6b6bc-114">Это должен быть локальный принтер, настроенный в качестве принтера с буферизацией.</span><span class="sxs-lookup"><span data-stu-id="6b6bc-114">This must be a local printer that is configured as a spooled printer.</span></span> <span data-ttu-id="6b6bc-115">Если *хпринтер* является маркером подключения к удаленному принтеру или если принтер настроен для прямой печати, функция **AddJob** завершается ошибкой.</span><span class="sxs-lookup"><span data-stu-id="6b6bc-115">If *hPrinter* is a handle to a remote printer connection, or if the printer is configured for direct printing, the **AddJob** function fails.</span></span> <span data-ttu-id="6b6bc-116">Используйте функцию [**опенпринтер**](openprinter.md) или [**аддпринтер**](addprinter.md) для получения маркера принтера.</span><span class="sxs-lookup"><span data-stu-id="6b6bc-116">Use the [**OpenPrinter**](openprinter.md) or [**AddPrinter**](addprinter.md) function to retrieve a printer handle.</span></span>

</dd> <dt>

<span data-ttu-id="6b6bc-117">*Уровень* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="6b6bc-117">*Level* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="6b6bc-118">Версия структуры данных о задании печати, которую функция сохраняет в буфер, на который указывает *pData*.</span><span class="sxs-lookup"><span data-stu-id="6b6bc-118">The version of the print job information data structure that the function stores into the buffer pointed to by *pData*.</span></span> <span data-ttu-id="6b6bc-119">Присвойте этому параметру значение One.</span><span class="sxs-lookup"><span data-stu-id="6b6bc-119">Set this parameter to one.</span></span>

</dd> <dt>

<span data-ttu-id="6b6bc-120">*pData* \[ заполняет\]</span><span class="sxs-lookup"><span data-stu-id="6b6bc-120">*pData* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="6b6bc-121">Указатель на буфер, который получает структуру данных [**ADDJOB \_ info \_ 1**](addjob-info-1.md) и строку пути.</span><span class="sxs-lookup"><span data-stu-id="6b6bc-121">A pointer to a buffer that receives an [**ADDJOB\_INFO\_1**](addjob-info-1.md) data structure and a path string.</span></span>

</dd> <dt>

<span data-ttu-id="6b6bc-122">*кббуф* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="6b6bc-122">*cbBuf* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="6b6bc-123">Размер (в байтах) буфера, на который указывает *pData*.</span><span class="sxs-lookup"><span data-stu-id="6b6bc-123">The size, in bytes, of the buffer pointed to by *pData*.</span></span> <span data-ttu-id="6b6bc-124">Буфер должен быть достаточно большим, чтобы содержать структуру [**ADDJOB \_ info \_ 1**](addjob-info-1.md) и строку пути.</span><span class="sxs-lookup"><span data-stu-id="6b6bc-124">The buffer needs to be large enough to contain an [**ADDJOB\_INFO\_1**](addjob-info-1.md) structure and a path string.</span></span>

</dd> <dt>

<span data-ttu-id="6b6bc-125">*пкбнидед* \[ заполняет\]</span><span class="sxs-lookup"><span data-stu-id="6b6bc-125">*pcbNeeded* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="6b6bc-126">Указатель на переменную, которая получает общий размер (в байтах) структуры данных [**ADDJOB \_ info \_ 1**](addjob-info-1.md) плюс строку пути.</span><span class="sxs-lookup"><span data-stu-id="6b6bc-126">A pointer to a variable that receives the total size, in bytes, of the [**ADDJOB\_INFO\_1**](addjob-info-1.md) data structure plus the path string.</span></span> <span data-ttu-id="6b6bc-127">Если это значение меньше или равно *кббуф* и функция выполнена, это фактическое число байтов, записанных в буфер, на который указывает *pData*.</span><span class="sxs-lookup"><span data-stu-id="6b6bc-127">If this value is less than or equal to *cbBuf* and the function succeeds, this is the actual number of bytes written to the buffer pointed to by *pData*.</span></span> <span data-ttu-id="6b6bc-128">Если это число больше *кббуф*, буфер слишком мал, и необходимо повторно вызвать функцию с размером буфера по крайней мере до размера \* *пкбнидед*.</span><span class="sxs-lookup"><span data-stu-id="6b6bc-128">If this number is greater than *cbBuf*, the buffer is too small, and you must call the function again with a buffer size at least as large as \**pcbNeeded*.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="6b6bc-129">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="6b6bc-129">Return value</span></span>

<span data-ttu-id="6b6bc-130">Если функция выполнена, возвращаемое значение будет ненулевым.</span><span class="sxs-lookup"><span data-stu-id="6b6bc-130">If the function succeeds, the return value is a nonzero value.</span></span>

<span data-ttu-id="6b6bc-131">Если функция выполняется неудачно, возвращается нулевое значение.</span><span class="sxs-lookup"><span data-stu-id="6b6bc-131">If the function fails, the return value is zero.</span></span>

## <a name="remarks"></a><span data-ttu-id="6b6bc-132">Комментарии</span><span class="sxs-lookup"><span data-stu-id="6b6bc-132">Remarks</span></span>

> [!Note]  
> <span data-ttu-id="6b6bc-133">Это блокирующая или синхронная функция, которая может не возвращать значение немедленно.</span><span class="sxs-lookup"><span data-stu-id="6b6bc-133">This is a blocking or synchronous function and might not return immediately.</span></span> <span data-ttu-id="6b6bc-134">Скорость возврата этой функцией зависит от факторов времени выполнения, таких как состояние сети, Конфигурация сервера печати и факторы реализации драйвера принтера, которые трудно предсказать при написании приложения.</span><span class="sxs-lookup"><span data-stu-id="6b6bc-134">How quickly this function returns depends on run-time factors such as network status, print server configuration, and printer driver implementation factors that are difficult to predict when writing an application.</span></span> <span data-ttu-id="6b6bc-135">Вызов этой функции из потока, который управляет взаимодействием с пользовательским интерфейсом, может привести к невозможности реагирования приложения.</span><span class="sxs-lookup"><span data-stu-id="6b6bc-135">Calling this function from a thread that manages interaction with the user interface could make the application appear to be unresponsive.</span></span>

 

<span data-ttu-id="6b6bc-136">Можно вызвать функцию [**CreateFile**](/windows/desktop/api/fileapi/nf-fileapi-createfilea) , чтобы открыть файл очереди, заданный элементом **path** структуры [**ADDJOB \_ info \_ 1**](addjob-info-1.md) , а затем вызвать функцию [**WriteFile**](/windows/desktop/api/fileapi/nf-fileapi-writefile) для записи в него данных задания печати.</span><span class="sxs-lookup"><span data-stu-id="6b6bc-136">You can call the [**CreateFile**](/windows/desktop/api/fileapi/nf-fileapi-createfilea) function to open the spool file specified by the **Path** member of the [**ADDJOB\_INFO\_1**](addjob-info-1.md) structure, and then call the [**WriteFile**](/windows/desktop/api/fileapi/nf-fileapi-writefile) function to write print job data to it.</span></span> <span data-ttu-id="6b6bc-137">После этого вызовите функцию [**ScheduleJob**](schedulejob.md) , чтобы уведомить Диспетчер очереди печати о том, что задание печати может быть запланировано с помощью диспетчера очереди печати.</span><span class="sxs-lookup"><span data-stu-id="6b6bc-137">After that is done, call the [**ScheduleJob**](schedulejob.md) function to notify the print spooler that the print job can now be scheduled by the spooler for printing.</span></span>

## <a name="requirements"></a><span data-ttu-id="6b6bc-138">Требования</span><span class="sxs-lookup"><span data-stu-id="6b6bc-138">Requirements</span></span>



| <span data-ttu-id="6b6bc-139">Требование</span><span class="sxs-lookup"><span data-stu-id="6b6bc-139">Requirement</span></span> | <span data-ttu-id="6b6bc-140">Значение</span><span class="sxs-lookup"><span data-stu-id="6b6bc-140">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="6b6bc-141">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="6b6bc-141">Minimum supported client</span></span><br/> | <span data-ttu-id="6b6bc-142">Windows 2000 Professional \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="6b6bc-142">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                                |
| <span data-ttu-id="6b6bc-143">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="6b6bc-143">Minimum supported server</span></span><br/> | <span data-ttu-id="6b6bc-144">Windows 2000 Server \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="6b6bc-144">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                      |
| <span data-ttu-id="6b6bc-145">Заголовок</span><span class="sxs-lookup"><span data-stu-id="6b6bc-145">Header</span></span><br/>                   | <dl> <span data-ttu-id="6b6bc-146"><dt>Винспул. h (включение Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="6b6bc-146"><dt>Winspool.h (include Windows.h)</dt></span></span> </dl> |
| <span data-ttu-id="6b6bc-147">Библиотека</span><span class="sxs-lookup"><span data-stu-id="6b6bc-147">Library</span></span><br/>                  | <dl> <span data-ttu-id="6b6bc-148"><dt>Винспул. lib</dt></span><span class="sxs-lookup"><span data-stu-id="6b6bc-148"><dt>Winspool.lib</dt></span></span> </dl>                   |
| <span data-ttu-id="6b6bc-149">DLL</span><span class="sxs-lookup"><span data-stu-id="6b6bc-149">DLL</span></span><br/>                      | <dl> <span data-ttu-id="6b6bc-150"><dt>Винспул. drv</dt></span><span class="sxs-lookup"><span data-stu-id="6b6bc-150"><dt>Winspool.drv</dt></span></span> </dl>                   |
| <span data-ttu-id="6b6bc-151">Имя в кодировке Юникод и ANSI</span><span class="sxs-lookup"><span data-stu-id="6b6bc-151">Unicode and ANSI names</span></span><br/>   | <span data-ttu-id="6b6bc-152">**Адджобв** (Юникод) и **адджоба** (ANSI)</span><span class="sxs-lookup"><span data-stu-id="6b6bc-152">**AddJobW** (Unicode) and **AddJobA** (ANSI)</span></span><br/>                                                   |



## <a name="see-also"></a><span data-ttu-id="6b6bc-153">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="6b6bc-153">See also</span></span>

<dl> <dt>

[<span data-ttu-id="6b6bc-154">**\_Сведения о ADDJOB \_ 1**</span><span class="sxs-lookup"><span data-stu-id="6b6bc-154">**ADDJOB\_INFO\_1**</span></span>](addjob-info-1.md)
</dt> <dt>

[<span data-ttu-id="6b6bc-155">**CreateFile**</span><span class="sxs-lookup"><span data-stu-id="6b6bc-155">**CreateFile**</span></span>](/windows/desktop/api/fileapi/nf-fileapi-createfilea)
</dt> <dt>

[<span data-ttu-id="6b6bc-156">API печати GDI</span><span class="sxs-lookup"><span data-stu-id="6b6bc-156">GDI Print API</span></span>](gdi-printing.md)
</dt> <dt>

[<span data-ttu-id="6b6bc-157">Вывод на печать</span><span class="sxs-lookup"><span data-stu-id="6b6bc-157">Printing</span></span>](printdocs-printing.md)
</dt> <dt>

[<span data-ttu-id="6b6bc-158">Функции API очереди печати принтера</span><span class="sxs-lookup"><span data-stu-id="6b6bc-158">Print Spooler API Functions</span></span>](printing-and-print-spooler-functions.md)
</dt> <dt>

[<span data-ttu-id="6b6bc-159">**опенпринтер**</span><span class="sxs-lookup"><span data-stu-id="6b6bc-159">**OpenPrinter**</span></span>](openprinter.md)
</dt> <dt>

[<span data-ttu-id="6b6bc-160">**ScheduleJob**</span><span class="sxs-lookup"><span data-stu-id="6b6bc-160">**ScheduleJob**</span></span>](schedulejob.md)
</dt> <dt>

[<span data-ttu-id="6b6bc-161">**стартдокпринтер**</span><span class="sxs-lookup"><span data-stu-id="6b6bc-161">**StartDocPrinter**</span></span>](startdocprinter.md)
</dt> <dt>

[<span data-ttu-id="6b6bc-162">**Windows. Graphics. Printing**</span><span class="sxs-lookup"><span data-stu-id="6b6bc-162">**Windows.Graphics.Printing**</span></span>](/uwp/api/Windows.Graphics.Printing)
</dt> <dt>

[<span data-ttu-id="6b6bc-163">**WriteFile**</span><span class="sxs-lookup"><span data-stu-id="6b6bc-163">**WriteFile**</span></span>](/windows/desktop/api/fileapi/nf-fileapi-writefile)
</dt> <dt>

[<span data-ttu-id="6b6bc-164">API печати XPS</span><span class="sxs-lookup"><span data-stu-id="6b6bc-164">XPS Print API</span></span>](xps-printing.md)
</dt> </dl>

 

