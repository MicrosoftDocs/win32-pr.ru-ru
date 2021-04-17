---
description: Извлекает Поддерживаемые уровни подсветки.
ms.assetid: b4c1ee3f-af75-477e-b7ed-53be905374d7
title: Код элемента управления IOCTL_VIDEO_QUERY_SUPPORTED_BRIGHTNESS (Нтддвдео. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IOCTL_VIDEO_QUERY_SUPPORTED_BRIGHTNESS
api_type:
- HeaderDef
api_location:
- Ntddvdeo.h
ms.openlocfilehash: a5618ec29fd47ba690106b5f826e6fb145eac208
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "105663118"
---
# <a name="ioctl_video_query_supported_brightness-control-code"></a><span data-ttu-id="a0364-103">Видеозапрос IOCTL, \_ \_ \_ поддерживаемый \_ код управления яркостью</span><span class="sxs-lookup"><span data-stu-id="a0364-103">IOCTL\_VIDEO\_QUERY\_SUPPORTED\_BRIGHTNESS control code</span></span>

<span data-ttu-id="a0364-104">Извлекает Поддерживаемые уровни подсветки.</span><span class="sxs-lookup"><span data-stu-id="a0364-104">Retrieves the supported backlight levels.</span></span>

<span data-ttu-id="a0364-105">Чтобы выполнить эту операцию, вызовите функцию [**DeviceIoControl**](/windows/desktop/api/ioapiset/nf-ioapiset-deviceiocontrol) со следующими параметрами.</span><span class="sxs-lookup"><span data-stu-id="a0364-105">To perform this operation, call the [**DeviceIoControl**](/windows/desktop/api/ioapiset/nf-ioapiset-deviceiocontrol) function with the following parameters.</span></span>


```C++
BOOL DeviceIoControl(
  (HANDLE) hDevice,                // handle to device
  IOCTL_VIDEO_QUERY_SUPPORTED_BRIGHTNESS,  // dwIoControlCode
  NULL,                            // lpInBuffer
  0,                               // nInBufferSize
  (LPVOID) lpOutBuffer,            // output buffer
  (DWORD) nOutBufferSize,          // size of output buffer
  (LPDWORD) lpBytesReturned,       // number of bytes returned
  (LPOVERLAPPED) lpOverlapped      // OVERLAPPED structure
);
```



## <a name="parameters"></a><span data-ttu-id="a0364-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="a0364-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="a0364-107">*хдевице*</span><span class="sxs-lookup"><span data-stu-id="a0364-107">*hDevice*</span></span> 
</dt> <dd>

<span data-ttu-id="a0364-108">Маркер для \\ \\ . \\ ЖК-устройство.</span><span class="sxs-lookup"><span data-stu-id="a0364-108">A handle to the \\\\.\\LCD device.</span></span> <span data-ttu-id="a0364-109">Чтобы получить маркер устройства, вызовите функцию [**CreateFile**](/windows/desktop/api/fileapi/nf-fileapi-createfilea) .</span><span class="sxs-lookup"><span data-stu-id="a0364-109">To retrieve a device handle, call the [**CreateFile**](/windows/desktop/api/fileapi/nf-fileapi-createfilea) function.</span></span>

</dd> <dt>

<span data-ttu-id="a0364-110">*двиоконтролкоде*</span><span class="sxs-lookup"><span data-stu-id="a0364-110">*dwIoControlCode*</span></span> 
</dt> <dd>

<span data-ttu-id="a0364-111">Управляющий код для операции.</span><span class="sxs-lookup"><span data-stu-id="a0364-111">The control code for the operation.</span></span> <span data-ttu-id="a0364-112">Это значение определяет конкретную выполняемую операцию и тип устройства, на котором она выполняется.</span><span class="sxs-lookup"><span data-stu-id="a0364-112">This value identifies the specific operation to be performed and the type of device on which to perform it.</span></span> <span data-ttu-id="a0364-113">Использование **\_ запроса видео \_ \_ \_ ioctl** для этой операции.</span><span class="sxs-lookup"><span data-stu-id="a0364-113">Use **IOCTL\_VIDEO\_QUERY\_SUPPORTED\_BRIGHTNESS** for this operation.</span></span>

</dd> <dt>

<span data-ttu-id="a0364-114">*лпинбуффер*</span><span class="sxs-lookup"><span data-stu-id="a0364-114">*lpInBuffer*</span></span> 
</dt> <dd>

<span data-ttu-id="a0364-115">Не используется в этой операции; Задайте **значение NULL**.</span><span class="sxs-lookup"><span data-stu-id="a0364-115">Not used with this operation; set to **NULL**.</span></span>

</dd> <dt>

<span data-ttu-id="a0364-116">*нинбуфферсизе*</span><span class="sxs-lookup"><span data-stu-id="a0364-116">*nInBufferSize*</span></span> 
</dt> <dd>

<span data-ttu-id="a0364-117">Не используется в этой операции; присвойте ему значение 0.</span><span class="sxs-lookup"><span data-stu-id="a0364-117">Not used with this operation; set to zero.</span></span>

</dd> <dt>

<span data-ttu-id="a0364-118">*лпаутбуффер*</span><span class="sxs-lookup"><span data-stu-id="a0364-118">*lpOutBuffer*</span></span> 
</dt> <dd>

<span data-ttu-id="a0364-119">Указатель на буфер, который получает массив доступных уровней питания.</span><span class="sxs-lookup"><span data-stu-id="a0364-119">A pointer to a buffer that receives an array of the available power levels.</span></span> <span data-ttu-id="a0364-120">Размер этого буфера должен составлять 256 байт.</span><span class="sxs-lookup"><span data-stu-id="a0364-120">This buffer should be 256 bytes long.</span></span>

</dd> <dt>

<span data-ttu-id="a0364-121">*наутбуфферсизе*</span><span class="sxs-lookup"><span data-stu-id="a0364-121">*nOutBufferSize*</span></span> 
</dt> <dd>

<span data-ttu-id="a0364-122">Размер выходного буфера в байтах.</span><span class="sxs-lookup"><span data-stu-id="a0364-122">The size of the output buffer, in bytes.</span></span>

</dd> <dt>

<span data-ttu-id="a0364-123">*лпбитесретурнед*</span><span class="sxs-lookup"><span data-stu-id="a0364-123">*lpBytesReturned*</span></span> 
</dt> <dd>

<span data-ttu-id="a0364-124">Указатель на переменную, которая получает размер возвращаемых выходных данных в байтах.</span><span class="sxs-lookup"><span data-stu-id="a0364-124">A pointer to a variable that receives the size, in bytes, of output data returned.</span></span>

<span data-ttu-id="a0364-125">Если выходной буфер слишком мал для возвращения каких-либо данных, вызов завершается ошибкой, [**GetLastError**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror) возвращает код ошибки \_ недостаточный \_ Размер буфера, а возвращенное число байтов равно нулю.</span><span class="sxs-lookup"><span data-stu-id="a0364-125">If the output buffer is too small to return any data, then the call fails, [**GetLastError**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror) returns the error code ERROR\_INSUFFICIENT\_BUFFER, and the returned byte count is zero.</span></span>

<span data-ttu-id="a0364-126">Если выходной буфер слишком мал для хранения всех данных, но может содержать некоторые записи, то операционная система возвращает столько, сколько подходит, вызов завершается неудачно, [**GetLastError**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror) возвращает код ошибки \_ Дополнительные \_ данные, а *лпбитесретурнед* указывает объем возвращаемых данных.</span><span class="sxs-lookup"><span data-stu-id="a0364-126">If the output buffer is too small to hold all of the data but can hold some entries, then the operating system returns as much as fits, the call fails, [**GetLastError**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror) returns the error code ERROR\_MORE\_DATA, and *lpBytesReturned* indicates the amount of data returned.</span></span> <span data-ttu-id="a0364-127">Приложение должно повторно вызвать [**DeviceIoControl**](/windows/desktop/api/ioapiset/nf-ioapiset-deviceiocontrol) с той же операцией, указав новую отправную точку.</span><span class="sxs-lookup"><span data-stu-id="a0364-127">Your application should call [**DeviceIoControl**](/windows/desktop/api/ioapiset/nf-ioapiset-deviceiocontrol) again with the same operation, specifying a new starting point.</span></span>

<span data-ttu-id="a0364-128">Если *лповерлаппед* имеет **значение NULL** (ноноверлаппед I/O), *Лпбитесретурнед* не может иметь **значение NULL**.</span><span class="sxs-lookup"><span data-stu-id="a0364-128">If *lpOverlapped* is **NULL** (nonoverlapped I/O), *lpBytesReturned* cannot be **NULL**.</span></span>

<span data-ttu-id="a0364-129">Если *лповерлаппед* не **равно NULL** (перекрывающиеся операции ввода-вывода), *лпбитесретурнед* может иметь **значение NULL**.</span><span class="sxs-lookup"><span data-stu-id="a0364-129">If *lpOverlapped* is not **NULL** (overlapped I/O), *lpBytesReturned* can be **NULL**.</span></span> <span data-ttu-id="a0364-130">Если это операция с перекрытием, можно получить число байтов, возвращенных путем вызова функции [**GetOverlappedResult**](/windows/desktop/api/ioapiset/nf-ioapiset-getoverlappedresult) .</span><span class="sxs-lookup"><span data-stu-id="a0364-130">If this is an overlapped operation, you can retrieve the number of bytes returned by calling the [**GetOverlappedResult**](/windows/desktop/api/ioapiset/nf-ioapiset-getoverlappedresult) function.</span></span> <span data-ttu-id="a0364-131">Если *хдевице* связан с портом завершения ввода-вывода, можно получить число возвращаемых байтов, вызвав функцию [**жеткуеуедкомплетионстатус**](/windows/desktop/api/ioapiset/nf-ioapiset-getqueuedcompletionstatus) .</span><span class="sxs-lookup"><span data-stu-id="a0364-131">If *hDevice* is associated with an I/O completion port, you can get the number of bytes returned by calling the [**GetQueuedCompletionStatus**](/windows/desktop/api/ioapiset/nf-ioapiset-getqueuedcompletionstatus) function.</span></span>

</dd> <dt>

<span data-ttu-id="a0364-132">*лповерлаппед*</span><span class="sxs-lookup"><span data-stu-id="a0364-132">*lpOverlapped*</span></span> 
</dt> <dd>

<span data-ttu-id="a0364-133">Указатель на структуру [**OVERLAPPED**](/windows/desktop/api/minwinbase/ns-minwinbase-overlapped) .</span><span class="sxs-lookup"><span data-stu-id="a0364-133">A pointer to an [**OVERLAPPED**](/windows/desktop/api/minwinbase/ns-minwinbase-overlapped) structure.</span></span>

<span data-ttu-id="a0364-134">Если *хдевице* был открыт с \_ \_ флагом File Flag OVERLAPPED, *лповерлаппед* должен указывать на допустимую структуру [**OVERLAPPED**](/windows/desktop/api/minwinbase/ns-minwinbase-overlapped) .</span><span class="sxs-lookup"><span data-stu-id="a0364-134">If *hDevice* was opened with the FILE\_FLAG\_OVERLAPPED flag, *lpOverlapped* must point to a valid [**OVERLAPPED**](/windows/desktop/api/minwinbase/ns-minwinbase-overlapped) structure.</span></span> <span data-ttu-id="a0364-135">В этом случае операция выполняется как Перекрываемая (асинхронная) операция.</span><span class="sxs-lookup"><span data-stu-id="a0364-135">In this case, the operation is performed as an overlapped (asynchronous) operation.</span></span> <span data-ttu-id="a0364-136">Если устройство было открыто с \_ флагом File Flag \_ OVERLAPPED и *Лповерлаппед* имеет **значение NULL**, функция завершается ошибкой непредсказуемым образом.</span><span class="sxs-lookup"><span data-stu-id="a0364-136">If the device was opened with the FILE\_FLAG\_OVERLAPPED flag and *lpOverlapped* is **NULL**, the function fails in unpredictable ways.</span></span>

<span data-ttu-id="a0364-137">Если *хдевице* был открыт без указания \_ \_ флага File Flag OVERLAPPED, *Лповерлаппед* игнорируется, а [**DeviceIoControl**](/windows/desktop/api/ioapiset/nf-ioapiset-deviceiocontrol) не возвращает значение до тех пор, пока операция не будет завершена или пока не произойдет ошибка.</span><span class="sxs-lookup"><span data-stu-id="a0364-137">If *hDevice* was opened without specifying the FILE\_FLAG\_OVERLAPPED flag, *lpOverlapped* is ignored and [**DeviceIoControl**](/windows/desktop/api/ioapiset/nf-ioapiset-deviceiocontrol) does not return until the operation has been completed, or until an error occurs.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="a0364-138">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="a0364-138">Return value</span></span>

<span data-ttu-id="a0364-139">Если операция завершается успешно, [**DeviceIoControl**](/windows/desktop/api/ioapiset/nf-ioapiset-deviceiocontrol) возвращает ненулевое значение.</span><span class="sxs-lookup"><span data-stu-id="a0364-139">If the operation completes successfully, [**DeviceIoControl**](/windows/desktop/api/ioapiset/nf-ioapiset-deviceiocontrol) returns a nonzero value.</span></span>

<span data-ttu-id="a0364-140">Если операция завершается неудачно или ожидает выполнения, [**DeviceIoControl**](/windows/desktop/api/ioapiset/nf-ioapiset-deviceiocontrol) возвращает ноль.</span><span class="sxs-lookup"><span data-stu-id="a0364-140">If the operation fails or is pending, [**DeviceIoControl**](/windows/desktop/api/ioapiset/nf-ioapiset-deviceiocontrol) returns zero.</span></span> <span data-ttu-id="a0364-141">Дополнительные сведения об ошибке можно получить, вызвав [**GetLastError**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror).</span><span class="sxs-lookup"><span data-stu-id="a0364-141">To get extended error information, call [**GetLastError**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror).</span></span>

## <a name="remarks"></a><span data-ttu-id="a0364-142">Комментарии</span><span class="sxs-lookup"><span data-stu-id="a0364-142">Remarks</span></span>

<span data-ttu-id="a0364-143">Каждый элемент в массиве *лпаутбуффер* имеет длину один байт.</span><span class="sxs-lookup"><span data-stu-id="a0364-143">Each element in the *lpOutBuffer* array is one byte in length.</span></span> <span data-ttu-id="a0364-144">Поэтому после возврата параметр *лпбитесретурнед* указывает количество поддерживаемых уровней.</span><span class="sxs-lookup"><span data-stu-id="a0364-144">Therefore, upon return, the *lpBytesReturned* parameter indicates the number of supported levels.</span></span> <span data-ttu-id="a0364-145">Каждый уровень имеет значение от 0 до 100.</span><span class="sxs-lookup"><span data-stu-id="a0364-145">Each level is a value from 0 to 100.</span></span> <span data-ttu-id="a0364-146">Чем больше значение, тем ярче подсветка.</span><span class="sxs-lookup"><span data-stu-id="a0364-146">The larger the value, the brighter the backlight.</span></span> <span data-ttu-id="a0364-147">Все уровни поддерживаются независимо от того, подключен ли источник питания к сети AC или DC.</span><span class="sxs-lookup"><span data-stu-id="a0364-147">All levels are supported whether the power source is AC or DC.</span></span>

<span data-ttu-id="a0364-148">Файл заголовка, используемый для создания приложений, включающих эту функцию, Нтддвдео. h, входит в состав пакета средств разработки драйверов Microsoft Windows (DDK).</span><span class="sxs-lookup"><span data-stu-id="a0364-148">The header file used to build applications that include this functionality, Ntddvdeo.h, is included in the Microsoft Windows Driver Development Kit (DDK).</span></span> <span data-ttu-id="a0364-149">Сведения о получении DDK см. в разделе [https://www.microsoft.com/whdc/devtools/ddk/default.mspx](https://msdn.microsoft.com/windows/hardware/gg454513) .</span><span class="sxs-lookup"><span data-stu-id="a0364-149">For information on obtaining the DDK, see [https://www.microsoft.com/whdc/devtools/ddk/default.mspx](https://msdn.microsoft.com/windows/hardware/gg454513).</span></span>

<span data-ttu-id="a0364-150">Кроме того, этот код элемента управления можно определить следующим образом:</span><span class="sxs-lookup"><span data-stu-id="a0364-150">Alternatively, you can define this control code as follows:</span></span>

``` syntax
#define IOCTL_VIDEO_QUERY_SUPPORTED_BRIGHTNESS \
  CTL_CODE(FILE_DEVICE_VIDEO, 0x125, METHOD_BUFFERED, FILE_ANY_ACCESS)
```

## <a name="requirements"></a><span data-ttu-id="a0364-151">Требования</span><span class="sxs-lookup"><span data-stu-id="a0364-151">Requirements</span></span>



| <span data-ttu-id="a0364-152">Требование</span><span class="sxs-lookup"><span data-stu-id="a0364-152">Requirement</span></span> | <span data-ttu-id="a0364-153">Значение</span><span class="sxs-lookup"><span data-stu-id="a0364-153">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="a0364-154">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="a0364-154">Minimum supported client</span></span><br/> | <span data-ttu-id="a0364-155">Windows Vista, Windows XP с пакетом обновления 1 (SP1), \[ только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="a0364-155">Windows Vista, Windows XP with SP1 \[desktop apps only\]</span></span><br/>                   |
| <span data-ttu-id="a0364-156">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="a0364-156">Minimum supported server</span></span><br/> | <span data-ttu-id="a0364-157">\[Только для настольных приложений Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="a0364-157">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="a0364-158">Header</span><span class="sxs-lookup"><span data-stu-id="a0364-158">Header</span></span><br/>                   | <dl> <span data-ttu-id="a0364-159"><dt>Нтддвдео. h</dt></span><span class="sxs-lookup"><span data-stu-id="a0364-159"><dt>Ntddvdeo.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="a0364-160">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="a0364-160">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a0364-161">Интерфейс управления подсветкой</span><span class="sxs-lookup"><span data-stu-id="a0364-161">Backlight Control Interface</span></span>](backlight-control-interface.md)
</dt> <dt>

[<span data-ttu-id="a0364-162">**DeviceIoControl**</span><span class="sxs-lookup"><span data-stu-id="a0364-162">**DeviceIoControl**</span></span>](/windows/desktop/api/ioapiset/nf-ioapiset-deviceiocontrol)
</dt> </dl>

 

