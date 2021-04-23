---
description: Функция Жетжоб извлекает сведения об указанном задании печати.
ms.assetid: 57e59f84-d2a0-4722-b0fc-6673f7bb5c57
title: Функция Жетжоб (Винспул. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- GetJob
- GetJobA
- GetJobW
api_type:
- DllExport
api_location:
- Winspool.drv
- Ext-MS-Win-Printer-WinSpool-l1-1-2.dll
- Ext-MS-Win-Printer-WinSpool-L1-1-3.dll
ms.openlocfilehash: 73ae36ebab4530bf21eb86918fdbbbe941ed0741
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104264452"
---
# <a name="getjob-function"></a><span data-ttu-id="7c943-103">Функция Жетжоб</span><span class="sxs-lookup"><span data-stu-id="7c943-103">GetJob function</span></span>

<span data-ttu-id="7c943-104">Функция **жетжоб** извлекает сведения об указанном задании печати.</span><span class="sxs-lookup"><span data-stu-id="7c943-104">The **GetJob** function retrieves information about a specified print job.</span></span>

## <a name="syntax"></a><span data-ttu-id="7c943-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="7c943-105">Syntax</span></span>


```C++
BOOL GetJob(
  _In_  HANDLE  hPrinter,
  _In_  DWORD   JobId,
  _In_  DWORD   Level,
  _Out_ LPBYTE  pJob,
  _In_  DWORD   cbBuf,
  _Out_ LPDWORD pcbNeeded
);
```



## <a name="parameters"></a><span data-ttu-id="7c943-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="7c943-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="7c943-107">*хпринтер* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="7c943-107">*hPrinter* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="7c943-108">Маркер принтера, для которого извлекаются данные задания печати.</span><span class="sxs-lookup"><span data-stu-id="7c943-108">A handle to the printer for which the print-job data is retrieved.</span></span> <span data-ttu-id="7c943-109">Используйте функцию [**опенпринтер**](openprinter.md) или [**аддпринтер**](addprinter.md) для получения маркера принтера.</span><span class="sxs-lookup"><span data-stu-id="7c943-109">Use the [**OpenPrinter**](openprinter.md) or [**AddPrinter**](addprinter.md) function to retrieve a printer handle.</span></span>

</dd> <dt>

<span data-ttu-id="7c943-110">Идентификатор *задания* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="7c943-110">*JobId* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="7c943-111">Определяет задание печати, для которого извлекаются данные.</span><span class="sxs-lookup"><span data-stu-id="7c943-111">Identifies the print job for which to retrieve data.</span></span> <span data-ttu-id="7c943-112">Чтобы получить идентификатор задания печати, используйте функцию [**AddJob**](addjob.md) или функцию [**стартдок**](/windows/desktop/api/Wingdi/nf-wingdi-startdoca) .</span><span class="sxs-lookup"><span data-stu-id="7c943-112">Use the [**AddJob**](addjob.md) function or [**StartDoc**](/windows/desktop/api/Wingdi/nf-wingdi-startdoca) function to get a print job identifier.</span></span>

</dd> <dt>

<span data-ttu-id="7c943-113">*Уровень* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="7c943-113">*Level* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="7c943-114">Тип сведений, возвращаемых в буфер *пжоб* .</span><span class="sxs-lookup"><span data-stu-id="7c943-114">The type of information returned in the *pJob* buffer.</span></span> <span data-ttu-id="7c943-115">Если *уровень* равен 1, *пжоб* Получает структуру [**\_ сведений о \_ задании 1**](job-info-1.md) .</span><span class="sxs-lookup"><span data-stu-id="7c943-115">If *Level* is 1, *pJob* receives a [**JOB\_INFO\_1**](job-info-1.md) structure.</span></span> <span data-ttu-id="7c943-116">Если *уровень* равен 2, *пжоб* Получает структуру [**\_ сведений о \_ задании 2**](job-info-2.md) .</span><span class="sxs-lookup"><span data-stu-id="7c943-116">If *Level* is 2, *pJob* receives a [**JOB\_INFO\_2**](job-info-2.md) structure.</span></span>

</dd> <dt>

<span data-ttu-id="7c943-117">*пжоб* \[ заполняет\]</span><span class="sxs-lookup"><span data-stu-id="7c943-117">*pJob* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="7c943-118">Указатель на буфер, получающий сведения о задании [**\_ \_ 1**](job-info-1.md) или сведения о задании [**\_ \_ 2**](job-info-2.md) , содержащие сведения о задании.</span><span class="sxs-lookup"><span data-stu-id="7c943-118">A pointer to a buffer that receives a [**JOB\_INFO\_1**](job-info-1.md) or a [**JOB\_INFO\_2**](job-info-2.md) structure containing information about the job.</span></span> <span data-ttu-id="7c943-119">Буфер должен быть достаточно большим, чтобы хранить строки, на которые указывает члены структуры.</span><span class="sxs-lookup"><span data-stu-id="7c943-119">The buffer must be large enough to store the strings pointed to by the structure members.</span></span>

<span data-ttu-id="7c943-120">Чтобы определить требуемый размер буфера, вызовите **жетжоб** с параметром *кббуф* , присвойте ему значение 0.</span><span class="sxs-lookup"><span data-stu-id="7c943-120">To determine the required buffer size, call **GetJob** with *cbBuf* set to zero.</span></span> <span data-ttu-id="7c943-121">**Жетжоб** завершается ошибкой, [**GetLastError**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror) возвращает ошибку, \_ недостаточную \_ для буфера, а параметр *пкбнидед* возвращает размер (в байтах) буфера, необходимого для хранения массива структур и их данных.</span><span class="sxs-lookup"><span data-stu-id="7c943-121">**GetJob** fails, [**GetLastError**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror) returns ERROR\_INSUFFICIENT\_BUFFER, and the *pcbNeeded* parameter returns the size, in bytes, of the buffer required to hold the array of structures and their data.</span></span>

</dd> <dt>

<span data-ttu-id="7c943-122">*кббуф* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="7c943-122">*cbBuf* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="7c943-123">Размер массива в байтах.</span><span class="sxs-lookup"><span data-stu-id="7c943-123">The size, in bytes, of the array.</span></span>

</dd> <dt>

<span data-ttu-id="7c943-124">*пкбнидед* \[ заполняет\]</span><span class="sxs-lookup"><span data-stu-id="7c943-124">*pcbNeeded* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="7c943-125">Указатель на значение, указывающее число байтов, скопированных при выполнении функции, или число байтов, необходимых, если *кббуф* слишком мал.</span><span class="sxs-lookup"><span data-stu-id="7c943-125">A pointer to a value that specifies the number of bytes copied if the function succeeds or the number of bytes required if *cbBuf* is too small.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="7c943-126">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="7c943-126">Return value</span></span>

<span data-ttu-id="7c943-127">Если функция выполнена, возвращаемое значение будет ненулевым.</span><span class="sxs-lookup"><span data-stu-id="7c943-127">If the function succeeds, the return value is a nonzero value.</span></span>

<span data-ttu-id="7c943-128">Если функция выполняется неудачно, возвращается нулевое значение.</span><span class="sxs-lookup"><span data-stu-id="7c943-128">If the function fails, the return value is zero.</span></span>

## <a name="remarks"></a><span data-ttu-id="7c943-129">Комментарии</span><span class="sxs-lookup"><span data-stu-id="7c943-129">Remarks</span></span>

> [!Note]  
> <span data-ttu-id="7c943-130">Это блокирующая или синхронная функция, которая может не возвращать значение немедленно.</span><span class="sxs-lookup"><span data-stu-id="7c943-130">This is a blocking or synchronous function and might not return immediately.</span></span> <span data-ttu-id="7c943-131">Скорость возврата этой функцией зависит от факторов времени выполнения, таких как состояние сети, Конфигурация сервера печати и факторы реализации драйвера принтера, которые трудно предсказать при написании приложения.</span><span class="sxs-lookup"><span data-stu-id="7c943-131">How quickly this function returns depends on run-time factors such as network status, print server configuration, and printer driver implementation factors that are difficult to predict when writing an application.</span></span> <span data-ttu-id="7c943-132">Вызов этой функции из потока, который управляет взаимодействием с пользовательским интерфейсом, может привести к невозможности реагирования приложения.</span><span class="sxs-lookup"><span data-stu-id="7c943-132">Calling this function from a thread that manages interaction with the user interface could make the application appear to be unresponsive.</span></span>

 

## <a name="requirements"></a><span data-ttu-id="7c943-133">Требования</span><span class="sxs-lookup"><span data-stu-id="7c943-133">Requirements</span></span>



| <span data-ttu-id="7c943-134">Требование</span><span class="sxs-lookup"><span data-stu-id="7c943-134">Requirement</span></span> | <span data-ttu-id="7c943-135">Значение</span><span class="sxs-lookup"><span data-stu-id="7c943-135">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="7c943-136">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="7c943-136">Minimum supported client</span></span><br/> | <span data-ttu-id="7c943-137">Windows 2000 Professional \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="7c943-137">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                                |
| <span data-ttu-id="7c943-138">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="7c943-138">Minimum supported server</span></span><br/> | <span data-ttu-id="7c943-139">Windows 2000 Server \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="7c943-139">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                      |
| <span data-ttu-id="7c943-140">Заголовок</span><span class="sxs-lookup"><span data-stu-id="7c943-140">Header</span></span><br/>                   | <dl> <span data-ttu-id="7c943-141"><dt>Винспул. h (включение Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="7c943-141"><dt>Winspool.h (include Windows.h)</dt></span></span> </dl> |
| <span data-ttu-id="7c943-142">Библиотека</span><span class="sxs-lookup"><span data-stu-id="7c943-142">Library</span></span><br/>                  | <dl> <span data-ttu-id="7c943-143"><dt>Винспул. lib</dt></span><span class="sxs-lookup"><span data-stu-id="7c943-143"><dt>Winspool.lib</dt></span></span> </dl>                   |
| <span data-ttu-id="7c943-144">DLL</span><span class="sxs-lookup"><span data-stu-id="7c943-144">DLL</span></span><br/>                      | <dl> <span data-ttu-id="7c943-145"><dt>Винспул. drv</dt></span><span class="sxs-lookup"><span data-stu-id="7c943-145"><dt>Winspool.drv</dt></span></span> </dl>                   |
| <span data-ttu-id="7c943-146">Имя в кодировке Юникод и ANSI</span><span class="sxs-lookup"><span data-stu-id="7c943-146">Unicode and ANSI names</span></span><br/>   | <span data-ttu-id="7c943-147">**Жетжобв** (Юникод) и **жетжоба** (ANSI)</span><span class="sxs-lookup"><span data-stu-id="7c943-147">**GetJobW** (Unicode) and **GetJobA** (ANSI)</span></span><br/>                                                   |



## <a name="see-also"></a><span data-ttu-id="7c943-148">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="7c943-148">See also</span></span>

<dl> <dt>

[<span data-ttu-id="7c943-149">Вывод на печать</span><span class="sxs-lookup"><span data-stu-id="7c943-149">Printing</span></span>](printdocs-printing.md)
</dt> <dt>

[<span data-ttu-id="7c943-150">Функции API очереди печати принтера</span><span class="sxs-lookup"><span data-stu-id="7c943-150">Print Spooler API Functions</span></span>](printing-and-print-spooler-functions.md)
</dt> <dt>

[<span data-ttu-id="7c943-151">**AddJob**</span><span class="sxs-lookup"><span data-stu-id="7c943-151">**AddJob**</span></span>](addjob.md)
</dt> <dt>

[<span data-ttu-id="7c943-152">**\_Сведения о задании \_ 1**</span><span class="sxs-lookup"><span data-stu-id="7c943-152">**JOB\_INFO\_1**</span></span>](job-info-1.md)
</dt> <dt>

[<span data-ttu-id="7c943-153">**\_Сведения о задании \_ 2**</span><span class="sxs-lookup"><span data-stu-id="7c943-153">**JOB\_INFO\_2**</span></span>](job-info-2.md)
</dt> <dt>

[<span data-ttu-id="7c943-154">**ScheduleJob**</span><span class="sxs-lookup"><span data-stu-id="7c943-154">**ScheduleJob**</span></span>](schedulejob.md)
</dt> <dt>

[<span data-ttu-id="7c943-155">**сетжоб**</span><span class="sxs-lookup"><span data-stu-id="7c943-155">**SetJob**</span></span>](setjob.md)
</dt> </dl>

 

