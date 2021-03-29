---
description: Отправляет пакет завершения ввода-вывода в порт завершения ввода-вывода.
ms.assetid: 69a9b1e5-2d40-42de-a14a-f7b6f29bf571
title: Функция PostQueuedCompletionStatus (Иоапи. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- PostQueuedCompletionStatus
api_type:
- DllExport
api_location:
- Kernel32.dll
- API-MS-Win-Core-io-l1-1-0.dll
- KernelBase.dll
- MinKernelBase.dll
- API-MS-Win-Core-io-l1-1-1.dll
- api-ms-win-downlevel-kernel32-l1-1-0.dll
ms.openlocfilehash: f12de10032df7fec32dd9a577353dd20c0f4eaa5
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "105664179"
---
# <a name="postqueuedcompletionstatus-function"></a><span data-ttu-id="99309-103">Функция PostQueuedCompletionStatus</span><span class="sxs-lookup"><span data-stu-id="99309-103">PostQueuedCompletionStatus function</span></span>

<span data-ttu-id="99309-104">Отправляет пакет завершения ввода-вывода в порт завершения ввода-вывода.</span><span class="sxs-lookup"><span data-stu-id="99309-104">Posts an I/O completion packet to an I/O completion port.</span></span>

## <a name="syntax"></a><span data-ttu-id="99309-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="99309-105">Syntax</span></span>


```C++
BOOL WINAPI PostQueuedCompletionStatus(
  _In_     HANDLE       CompletionPort,
  _In_     DWORD        dwNumberOfBytesTransferred,
  _In_     ULONG_PTR    dwCompletionKey,
  _In_opt_ LPOVERLAPPED lpOverlapped
);
```



## <a name="parameters"></a><span data-ttu-id="99309-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="99309-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="99309-107">*Комплетионпорт* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="99309-107">*CompletionPort* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="99309-108">Маркер порта завершения ввода-вывода, в который должен быть отправлен пакет завершения ввода-вывода.</span><span class="sxs-lookup"><span data-stu-id="99309-108">A handle to an I/O completion port to which the I/O completion packet is to be posted.</span></span>

</dd> <dt>

<span data-ttu-id="99309-109">*двнумберофбитестрансферред* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="99309-109">*dwNumberOfBytesTransferred* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="99309-110">Значение, возвращаемое с помощью параметра *лпнумберофбитестрансферред* функции [**жеткуеуедкомплетионстатус**](/windows/win32/api/ioapiset/nf-ioapiset-getqueuedcompletionstatus) .</span><span class="sxs-lookup"><span data-stu-id="99309-110">The value to be returned through the *lpNumberOfBytesTransferred* parameter of the [**GetQueuedCompletionStatus**](/windows/win32/api/ioapiset/nf-ioapiset-getqueuedcompletionstatus) function.</span></span>

</dd> <dt>

<span data-ttu-id="99309-111">*двкомплетионкэй* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="99309-111">*dwCompletionKey* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="99309-112">Значение, возвращаемое с помощью параметра *лпкомплетионкэй* функции [**жеткуеуедкомплетионстатус**](/windows/win32/api/ioapiset/nf-ioapiset-getqueuedcompletionstatus) .</span><span class="sxs-lookup"><span data-stu-id="99309-112">The value to be returned through the *lpCompletionKey* parameter of the [**GetQueuedCompletionStatus**](/windows/win32/api/ioapiset/nf-ioapiset-getqueuedcompletionstatus) function.</span></span>

</dd> <dt>

<span data-ttu-id="99309-113">*лповерлаппед* \[ в необязательное\]</span><span class="sxs-lookup"><span data-stu-id="99309-113">*lpOverlapped* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="99309-114">Значение, возвращаемое с помощью параметра *лповерлаппед* функции [**жеткуеуедкомплетионстатус**](/windows/win32/api/ioapiset/nf-ioapiset-getqueuedcompletionstatus) .</span><span class="sxs-lookup"><span data-stu-id="99309-114">The value to be returned through the *lpOverlapped* parameter of the [**GetQueuedCompletionStatus**](/windows/win32/api/ioapiset/nf-ioapiset-getqueuedcompletionstatus) function.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="99309-115">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="99309-115">Return value</span></span>

<span data-ttu-id="99309-116">Если функция выполняется успешно, возвращается ненулевое значение.</span><span class="sxs-lookup"><span data-stu-id="99309-116">If the function succeeds, the return value is nonzero.</span></span>

<span data-ttu-id="99309-117">Если функция выполняется неудачно, возвращается нулевое значение.</span><span class="sxs-lookup"><span data-stu-id="99309-117">If the function fails, the return value is zero.</span></span> <span data-ttu-id="99309-118">Чтобы получить расширенные сведения об ошибке, вызовите [**GetLastError**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror) .</span><span class="sxs-lookup"><span data-stu-id="99309-118">To get extended error information, call [**GetLastError**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror) .</span></span>

## <a name="remarks"></a><span data-ttu-id="99309-119">Комментарии</span><span class="sxs-lookup"><span data-stu-id="99309-119">Remarks</span></span>

<span data-ttu-id="99309-120">Пакет завершения ввода-вывода будет отвечать за необработанный вызов функции [**жеткуеуедкомплетионстатус**](/windows/win32/api/ioapiset/nf-ioapiset-getqueuedcompletionstatus) .</span><span class="sxs-lookup"><span data-stu-id="99309-120">The I/O completion packet will satisfy an outstanding call to the [**GetQueuedCompletionStatus**](/windows/win32/api/ioapiset/nf-ioapiset-getqueuedcompletionstatus) function.</span></span> <span data-ttu-id="99309-121">Эта функция возвращает с тремя значениями, передаваемыми в качестве второго, третьего и четвертого параметров вызова **PostQueuedCompletionStatus**.</span><span class="sxs-lookup"><span data-stu-id="99309-121">This function returns with the three values passed as the second, third, and fourth parameters of the call to **PostQueuedCompletionStatus**.</span></span> <span data-ttu-id="99309-122">Система не использует или не проверяет эти значения.</span><span class="sxs-lookup"><span data-stu-id="99309-122">The system does not use or validate these values.</span></span> <span data-ttu-id="99309-123">В частности, параметр *лповерлаппед* не должен указывать на структуру [**OVERLAPPED**](/windows/desktop/api/minwinbase/ns-minwinbase-overlapped) .</span><span class="sxs-lookup"><span data-stu-id="99309-123">In particular, the *lpOverlapped* parameter need not point to an [**OVERLAPPED**](/windows/desktop/api/minwinbase/ns-minwinbase-overlapped) structure.</span></span>

<span data-ttu-id="99309-124">В Windows 8 и Windows Server 2012 эта функция поддерживается следующими технологиями.</span><span class="sxs-lookup"><span data-stu-id="99309-124">In Windows 8 and Windows Server 2012, this function is supported by the following technologies.</span></span>



| <span data-ttu-id="99309-125">Технология</span><span class="sxs-lookup"><span data-stu-id="99309-125">Technology</span></span>                                           | <span data-ttu-id="99309-126">Поддерживается</span><span class="sxs-lookup"><span data-stu-id="99309-126">Supported</span></span>      |
|------------------------------------------------------|----------------|
| <span data-ttu-id="99309-127">Протокол SMB 3,0</span><span class="sxs-lookup"><span data-stu-id="99309-127">Server Message Block (SMB) 3.0 protocol</span></span><br/>   | <span data-ttu-id="99309-128">Да</span><span class="sxs-lookup"><span data-stu-id="99309-128">Yes</span></span><br/> |
| <span data-ttu-id="99309-129">Прозрачная отработка отказа SMB 3,0 (ОТРАБОТКА отказа)</span><span class="sxs-lookup"><span data-stu-id="99309-129">SMB 3.0 Transparent Failover (TFO)</span></span><br/>        | <span data-ttu-id="99309-130">Да</span><span class="sxs-lookup"><span data-stu-id="99309-130">Yes</span></span><br/> |
| <span data-ttu-id="99309-131">SMB 3,0 с масштабируемыми файловыми ресурсами (SO)</span><span class="sxs-lookup"><span data-stu-id="99309-131">SMB 3.0 with Scale-out File Shares (SO)</span></span><br/>   | <span data-ttu-id="99309-132">Да</span><span class="sxs-lookup"><span data-stu-id="99309-132">Yes</span></span><br/> |
| <span data-ttu-id="99309-133">Общий том кластераная файловая система (CsvFS)</span><span class="sxs-lookup"><span data-stu-id="99309-133">Cluster Shared Volume File System (CsvFS)</span></span><br/> | <span data-ttu-id="99309-134">Да</span><span class="sxs-lookup"><span data-stu-id="99309-134">Yes</span></span><br/> |
| <span data-ttu-id="99309-135">Восстанавливаемая файловая система (ReFS)</span><span class="sxs-lookup"><span data-stu-id="99309-135">Resilient File System (ReFS)</span></span><br/>              | <span data-ttu-id="99309-136">Да</span><span class="sxs-lookup"><span data-stu-id="99309-136">Yes</span></span><br/> |



 

<span data-ttu-id="99309-137">CsvFs выполнит перенаправление операций ввода-вывода для сжатых файлов.</span><span class="sxs-lookup"><span data-stu-id="99309-137">CsvFs will do redirected IO for compressed files.</span></span>

## <a name="requirements"></a><span data-ttu-id="99309-138">Требования</span><span class="sxs-lookup"><span data-stu-id="99309-138">Requirements</span></span>



| <span data-ttu-id="99309-139">Требование</span><span class="sxs-lookup"><span data-stu-id="99309-139">Requirement</span></span> | <span data-ttu-id="99309-140">Значение</span><span class="sxs-lookup"><span data-stu-id="99309-140">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="99309-141">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="99309-141">Minimum supported client</span></span><br/> | <span data-ttu-id="99309-142">\[Приложения UWP для классических приложений Windows XP \|\]</span><span class="sxs-lookup"><span data-stu-id="99309-142">Windows XP \[desktop apps \| UWP apps\]</span></span><br/>                                                                                                                                                                                                                                                       |
| <span data-ttu-id="99309-143">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="99309-143">Minimum supported server</span></span><br/> | <span data-ttu-id="99309-144">\[Приложения UWP для классических приложений Windows Server 2003 \|\]</span><span class="sxs-lookup"><span data-stu-id="99309-144">Windows Server 2003 \[desktop apps \| UWP apps\]</span></span><br/>                                                                                                                                                                                                                                              |
| <span data-ttu-id="99309-145">Header</span><span class="sxs-lookup"><span data-stu-id="99309-145">Header</span></span><br/>                   | <dl> <span data-ttu-id="99309-146"><dt>Иоапи. h (включение Windows. h); </dt> <dt>Винбасе. h в Windows server 2008 R2, Windows 7, Windows server 2008, Windows Vista, Windows server 2003 и Windows XP (включая Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="99309-146"><dt>IoAPI.h (include Windows.h); </dt> <dt>WinBase.h on Windows Server 2008 R2, Windows 7, Windows Server 2008, Windows Vista, Windows Server 2003 and Windows XP (include Windows.h)</dt></span></span> </dl> |
| <span data-ttu-id="99309-147">Библиотека</span><span class="sxs-lookup"><span data-stu-id="99309-147">Library</span></span><br/>                  | <dl> <span data-ttu-id="99309-148"><dt>Kernel32.lib</dt></span><span class="sxs-lookup"><span data-stu-id="99309-148"><dt>Kernel32.lib</dt></span></span> </dl>                                                                                                                                                                                                                  |
| <span data-ttu-id="99309-149">DLL</span><span class="sxs-lookup"><span data-stu-id="99309-149">DLL</span></span><br/>                      | <dl> <span data-ttu-id="99309-150"><dt>Kernel32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="99309-150"><dt>Kernel32.dll</dt></span></span> </dl>                                                                                                                                                                                                                  |



## <a name="see-also"></a><span data-ttu-id="99309-151">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="99309-151">See also</span></span>

<dl> <dt>

[<span data-ttu-id="99309-152">**CreateIoCompletionPort**</span><span class="sxs-lookup"><span data-stu-id="99309-152">**CreateIoCompletionPort**</span></span>](createiocompletionport.md)
</dt> <dt>

[<span data-ttu-id="99309-153">Функции управления файлами</span><span class="sxs-lookup"><span data-stu-id="99309-153">File Management Functions</span></span>](file-management-functions.md)
</dt> <dt>

[<span data-ttu-id="99309-154">**жеткуеуедкомплетионстатус**</span><span class="sxs-lookup"><span data-stu-id="99309-154">**GetQueuedCompletionStatus**</span></span>](/windows/win32/api/ioapiset/nf-ioapiset-getqueuedcompletionstatus)
</dt> <dt>

[<span data-ttu-id="99309-155">**OVERLAPPED**</span><span class="sxs-lookup"><span data-stu-id="99309-155">**OVERLAPPED**</span></span>](/windows/desktop/api/minwinbase/ns-minwinbase-overlapped)
</dt> </dl>

 

