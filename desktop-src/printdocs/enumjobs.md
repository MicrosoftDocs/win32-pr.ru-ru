---
description: Функция Енумжобс извлекает сведения об указанном наборе заданий печати для указанного принтера.
ms.assetid: 1cf429ea-b40e-4063-b6de-c43b7b87f3d3
title: Функция Енумжобс (Винспул. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- EnumJobs
- EnumJobsA
- EnumJobsW
api_type:
- DllExport
api_location:
- Winspool.drv
ms.openlocfilehash: 174f58ba3fb1012e6ff46612fe312579969e6945
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "104265498"
---
# <a name="enumjobs-function"></a><span data-ttu-id="010b8-103">Функция Енумжобс</span><span class="sxs-lookup"><span data-stu-id="010b8-103">EnumJobs function</span></span>

<span data-ttu-id="010b8-104">Функция **енумжобс** извлекает сведения об указанном наборе заданий печати для указанного принтера.</span><span class="sxs-lookup"><span data-stu-id="010b8-104">The **EnumJobs** function retrieves information about a specified set of print jobs for a specified printer.</span></span>

## <a name="syntax"></a><span data-ttu-id="010b8-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="010b8-105">Syntax</span></span>


```C++
BOOL EnumJobs(
  _In_  HANDLE  hPrinter,
  _In_  DWORD   FirstJob,
  _In_  DWORD   NoJobs,
  _In_  DWORD   Level,
  _Out_ LPBYTE  pJob,
  _In_  DWORD   cbBuf,
  _Out_ LPDWORD pcbNeeded,
  _Out_ LPDWORD pcReturned
);
```



## <a name="parameters"></a><span data-ttu-id="010b8-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="010b8-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="010b8-107">*хпринтер* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="010b8-107">*hPrinter* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="010b8-108">Описатель объекта принтера, задания печати которого перечисляются функцией.</span><span class="sxs-lookup"><span data-stu-id="010b8-108">A handle to the printer object whose print jobs the function enumerates.</span></span> <span data-ttu-id="010b8-109">Используйте функцию [**опенпринтер**](openprinter.md) или [**аддпринтер**](addprinter.md) для получения маркера принтера.</span><span class="sxs-lookup"><span data-stu-id="010b8-109">Use the [**OpenPrinter**](openprinter.md) or [**AddPrinter**](addprinter.md) function to retrieve a printer handle.</span></span>

</dd> <dt>

<span data-ttu-id="010b8-110">*Фирстжоб* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="010b8-110">*FirstJob* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="010b8-111">Отсчитываемое от нуля расположение в очереди печати первого задания печати для перечисления.</span><span class="sxs-lookup"><span data-stu-id="010b8-111">The zero-based position within the print queue of the first print job to enumerate.</span></span> <span data-ttu-id="010b8-112">Например, значение 0 указывает, что перечисление должно начинаться с первого задания печати в очереди печати. значение 9 указывает, что перечисление должно начинаться со десятого задания печати в очереди печати.</span><span class="sxs-lookup"><span data-stu-id="010b8-112">For example, a value of 0 specifies that enumeration should begin at the first print job in the print queue; a value of 9 specifies that enumeration should begin at the tenth print job in the print queue.</span></span>

</dd> <dt>

<span data-ttu-id="010b8-113">*Задания* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="010b8-113">*NoJobs* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="010b8-114">Общее число заданий печати для перечисления.</span><span class="sxs-lookup"><span data-stu-id="010b8-114">The total number of print jobs to enumerate.</span></span>

</dd> <dt>

<span data-ttu-id="010b8-115">*Уровень* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="010b8-115">*Level* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="010b8-116">Тип сведений, возвращаемых в буфер *пжоб* .</span><span class="sxs-lookup"><span data-stu-id="010b8-116">The type of information returned in the *pJob* buffer.</span></span>



| <span data-ttu-id="010b8-117">Значение</span><span class="sxs-lookup"><span data-stu-id="010b8-117">Value</span></span>                                                                                                | <span data-ttu-id="010b8-118">Значение</span><span class="sxs-lookup"><span data-stu-id="010b8-118">Meaning</span></span>                                                                              |
|------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------|
| <span id="1"></span><dl> <span data-ttu-id="010b8-119"><dt>**1**</dt></span><span class="sxs-lookup"><span data-stu-id="010b8-119"><dt>**1**</dt></span></span> </dl> | <span data-ttu-id="010b8-120">*пжоб* получает массив [**\_ сведений о задании \_ 1**](job-info-1.md)</span><span class="sxs-lookup"><span data-stu-id="010b8-120">*pJob* receives an array of [**JOB\_INFO\_1**](job-info-1.md) structures</span></span><br/> |
| <span id="2"></span><dl> <span data-ttu-id="010b8-121"><dt>**2**</dt></span><span class="sxs-lookup"><span data-stu-id="010b8-121"><dt>**2**</dt></span></span> </dl> | <span data-ttu-id="010b8-122">*пжоб* получает массив [**\_ сведений о задании \_ 2**](job-info-2.md) структуры</span><span class="sxs-lookup"><span data-stu-id="010b8-122">*pJob* receives an array of [**JOB\_INFO\_2**](job-info-2.md) structures</span></span><br/> |
| <span id="3"></span><dl> <span data-ttu-id="010b8-123"><dt>**3-5**</dt></span><span class="sxs-lookup"><span data-stu-id="010b8-123"><dt>**3**</dt></span></span> </dl> | <span data-ttu-id="010b8-124">*пжоб* получает массив [**\_ сведений о задании \_ 3**](job-info-3.md) структуры</span><span class="sxs-lookup"><span data-stu-id="010b8-124">*pJob* receives an array of [**JOB\_INFO\_3**](job-info-3.md) structures</span></span><br/> |



 

</dd> <dt>

<span data-ttu-id="010b8-125">*пжоб* \[ заполняет\]</span><span class="sxs-lookup"><span data-stu-id="010b8-125">*pJob* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="010b8-126">Указатель на буфер, который получает массив [**сведений о задании \_ \_ 1**](job-info-1.md), [**\_ сведения о задании \_ 2**](job-info-2.md)или [**\_ сведения о задании \_ 3**](job-info-3.md) .</span><span class="sxs-lookup"><span data-stu-id="010b8-126">A pointer to a buffer that receives an array of [**JOB\_INFO\_1**](job-info-1.md), [**JOB\_INFO\_2**](job-info-2.md), or [**JOB\_INFO\_3**](job-info-3.md) structures.</span></span> <span data-ttu-id="010b8-127">Буфер должен быть достаточно большим, чтобы получать массив структур и любые строки или другие данные, к которым она указывает.</span><span class="sxs-lookup"><span data-stu-id="010b8-127">The buffer must be large enough to receive the array of structures and any strings or other data to which the structure members point.</span></span>

<span data-ttu-id="010b8-128">Чтобы определить требуемый размер буфера, вызовите **енумжобс** с параметром *кббуф* , присвойте ему значение 0.</span><span class="sxs-lookup"><span data-stu-id="010b8-128">To determine the required buffer size, call **EnumJobs** with *cbBuf* set to zero.</span></span> <span data-ttu-id="010b8-129">**Енумжобс** завершается ошибкой, [**GetLastError**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror) возвращает ошибку, \_ недостаточную \_ для буфера, а параметр *пкбнидед* возвращает размер (в байтах) буфера, необходимого для хранения массива структур и их данных.</span><span class="sxs-lookup"><span data-stu-id="010b8-129">**EnumJobs** fails, [**GetLastError**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror) returns ERROR\_INSUFFICIENT\_BUFFER, and the *pcbNeeded* parameter returns the size, in bytes, of the buffer required to hold the array of structures and their data.</span></span>

</dd> <dt>

<span data-ttu-id="010b8-130">*кббуф* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="010b8-130">*cbBuf* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="010b8-131">Размер (в байтах) буфера *пжоб* .</span><span class="sxs-lookup"><span data-stu-id="010b8-131">The size, in bytes, of the *pJob* buffer.</span></span>

</dd> <dt>

<span data-ttu-id="010b8-132">*пкбнидед* \[ заполняет\]</span><span class="sxs-lookup"><span data-stu-id="010b8-132">*pcbNeeded* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="010b8-133">Указатель на переменную, которая получает число байтов, скопированных в случае, если функция выполнена.</span><span class="sxs-lookup"><span data-stu-id="010b8-133">A pointer to a variable that receives the number of bytes copied if the function succeeds.</span></span> <span data-ttu-id="010b8-134">Если функция завершается с ошибкой, переменная получает необходимое количество байтов.</span><span class="sxs-lookup"><span data-stu-id="010b8-134">If the function fails, the variable receives the number of bytes required.</span></span>

</dd> <dt>

<span data-ttu-id="010b8-135">*пкретурнед* \[ заполняет\]</span><span class="sxs-lookup"><span data-stu-id="010b8-135">*pcReturned* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="010b8-136">Указатель на переменную, которая получает число структур [**\_ сведений \_ о**](job-info-1.md)задании 1, [**\_ сведения о задании \_ 2**](job-info-2.md)или [**\_ сведения о задании \_ 3**](job-info-3.md) , возвращаемых в буфер *пжоб* .</span><span class="sxs-lookup"><span data-stu-id="010b8-136">A pointer to a variable that receives the number of [**JOB\_INFO\_1**](job-info-1.md), [**JOB\_INFO\_2**](job-info-2.md), or [**JOB\_INFO\_3**](job-info-3.md) structures returned in the *pJob* buffer.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="010b8-137">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="010b8-137">Return value</span></span>

<span data-ttu-id="010b8-138">Если функция выполнена, возвращаемое значение будет ненулевым.</span><span class="sxs-lookup"><span data-stu-id="010b8-138">If the function succeeds, the return value is a nonzero value.</span></span>

<span data-ttu-id="010b8-139">Если функция выполняется неудачно, возвращается нулевое значение.</span><span class="sxs-lookup"><span data-stu-id="010b8-139">If the function fails, the return value is zero.</span></span>

## <a name="remarks"></a><span data-ttu-id="010b8-140">Комментарии</span><span class="sxs-lookup"><span data-stu-id="010b8-140">Remarks</span></span>

> [!Note]  
> <span data-ttu-id="010b8-141">Это блокирующая или синхронная функция, которая может не возвращать значение немедленно.</span><span class="sxs-lookup"><span data-stu-id="010b8-141">This is a blocking or synchronous function and might not return immediately.</span></span> <span data-ttu-id="010b8-142">Скорость возврата этой функцией зависит от факторов времени выполнения, таких как состояние сети, Конфигурация сервера печати и факторы реализации драйвера принтера, которые трудно предсказать при написании приложения.</span><span class="sxs-lookup"><span data-stu-id="010b8-142">How quickly this function returns depends on run-time factors such as network status, print server configuration, and printer driver implementation factors that are difficult to predict when writing an application.</span></span> <span data-ttu-id="010b8-143">Вызов этой функции из потока, который управляет взаимодействием с пользовательским интерфейсом, может привести к невозможности реагирования приложения.</span><span class="sxs-lookup"><span data-stu-id="010b8-143">Calling this function from a thread that manages interaction with the user interface could make the application appear to be unresponsive.</span></span>

 

<span data-ttu-id="010b8-144">Структура [**\_ сведений о \_ задании 1**](job-info-1.md) содержит общие сведения о задании печати; в структуре [**\_ сведений о \_ задании**](job-info-2.md) содержится гораздо более подробные сведения.</span><span class="sxs-lookup"><span data-stu-id="010b8-144">The [**JOB\_INFO\_1**](job-info-1.md) structure contains general print-job information; the [**JOB\_INFO\_2**](job-info-2.md) structure has much more detailed information.</span></span> <span data-ttu-id="010b8-145">Структура [**сведений о задании \_ \_ 3**](job-info-3.md) содержит сведения о том, как связаны задания.</span><span class="sxs-lookup"><span data-stu-id="010b8-145">The [**JOB\_INFO\_3**](job-info-3.md) structure contains information about how jobs are linked.</span></span>

<span data-ttu-id="010b8-146">Чтобы определить число заданий печати в очереди принтера, вызовите функцию [**PrintOut**](getprinter.md) с параметром *Level* , равным 2.</span><span class="sxs-lookup"><span data-stu-id="010b8-146">To determine the number of print jobs in the printer queue, call the [**GetPrinter**](getprinter.md) function with the *Level* parameter set to 2.</span></span>

## <a name="requirements"></a><span data-ttu-id="010b8-147">Требования</span><span class="sxs-lookup"><span data-stu-id="010b8-147">Requirements</span></span>



| <span data-ttu-id="010b8-148">Требование</span><span class="sxs-lookup"><span data-stu-id="010b8-148">Requirement</span></span> | <span data-ttu-id="010b8-149">Значение</span><span class="sxs-lookup"><span data-stu-id="010b8-149">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="010b8-150">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="010b8-150">Minimum supported client</span></span><br/> | <span data-ttu-id="010b8-151">Windows 2000 Professional \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="010b8-151">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                                |
| <span data-ttu-id="010b8-152">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="010b8-152">Minimum supported server</span></span><br/> | <span data-ttu-id="010b8-153">Windows 2000 Server \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="010b8-153">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                      |
| <span data-ttu-id="010b8-154">Заголовок</span><span class="sxs-lookup"><span data-stu-id="010b8-154">Header</span></span><br/>                   | <dl> <span data-ttu-id="010b8-155"><dt>Винспул. h (включение Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="010b8-155"><dt>Winspool.h (include Windows.h)</dt></span></span> </dl> |
| <span data-ttu-id="010b8-156">Библиотека</span><span class="sxs-lookup"><span data-stu-id="010b8-156">Library</span></span><br/>                  | <dl> <span data-ttu-id="010b8-157"><dt>Винспул. lib</dt></span><span class="sxs-lookup"><span data-stu-id="010b8-157"><dt>Winspool.lib</dt></span></span> </dl>                   |
| <span data-ttu-id="010b8-158">DLL</span><span class="sxs-lookup"><span data-stu-id="010b8-158">DLL</span></span><br/>                      | <dl> <span data-ttu-id="010b8-159"><dt>Винспул. drv</dt></span><span class="sxs-lookup"><span data-stu-id="010b8-159"><dt>Winspool.drv</dt></span></span> </dl>                   |
| <span data-ttu-id="010b8-160">Имя в кодировке Юникод и ANSI</span><span class="sxs-lookup"><span data-stu-id="010b8-160">Unicode and ANSI names</span></span><br/>   | <span data-ttu-id="010b8-161">**Енумжобсв** (Юникод) и **енумжобса** (ANSI)</span><span class="sxs-lookup"><span data-stu-id="010b8-161">**EnumJobsW** (Unicode) and **EnumJobsA** (ANSI)</span></span><br/>                                               |



## <a name="see-also"></a><span data-ttu-id="010b8-162">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="010b8-162">See also</span></span>

<dl> <dt>

[<span data-ttu-id="010b8-163">Вывод на печать</span><span class="sxs-lookup"><span data-stu-id="010b8-163">Printing</span></span>](printdocs-printing.md)
</dt> <dt>

[<span data-ttu-id="010b8-164">Функции API очереди печати принтера</span><span class="sxs-lookup"><span data-stu-id="010b8-164">Print Spooler API Functions</span></span>](printing-and-print-spooler-functions.md)
</dt> <dt>

[<span data-ttu-id="010b8-165">**жетжоб**</span><span class="sxs-lookup"><span data-stu-id="010b8-165">**GetJob**</span></span>](getjob.md)
</dt> <dt>

[<span data-ttu-id="010b8-166">**Наложение**</span><span class="sxs-lookup"><span data-stu-id="010b8-166">**GetPrinter**</span></span>](getprinter.md)
</dt> <dt>

[<span data-ttu-id="010b8-167">**\_Сведения о задании \_ 1**</span><span class="sxs-lookup"><span data-stu-id="010b8-167">**JOB\_INFO\_1**</span></span>](job-info-1.md)
</dt> <dt>

[<span data-ttu-id="010b8-168">**\_Сведения о задании \_ 2**</span><span class="sxs-lookup"><span data-stu-id="010b8-168">**JOB\_INFO\_2**</span></span>](job-info-2.md)
</dt> <dt>

[<span data-ttu-id="010b8-169">**\_Сведения о задании \_ 3**</span><span class="sxs-lookup"><span data-stu-id="010b8-169">**JOB\_INFO\_3**</span></span>](job-info-3.md)
</dt> <dt>

[<span data-ttu-id="010b8-170">**опенпринтер**</span><span class="sxs-lookup"><span data-stu-id="010b8-170">**OpenPrinter**</span></span>](openprinter.md)
</dt> <dt>

[<span data-ttu-id="010b8-171">**сетжоб**</span><span class="sxs-lookup"><span data-stu-id="010b8-171">**SetJob**</span></span>](setjob.md)
</dt> </dl>

 

