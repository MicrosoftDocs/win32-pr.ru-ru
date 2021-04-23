---
description: Задает текущие уровни подсветки AC и DC.
ms.assetid: baa77811-046d-4a07-b3df-2a31fba2d9a7
title: Код элемента управления IOCTL_VIDEO_SET_DISPLAY_BRIGHTNESS (Нтддвдео. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IOCTL_VIDEO_SET_DISPLAY_BRIGHTNESS
api_type:
- HeaderDef
api_location:
- Ntddvdeo.h
ms.openlocfilehash: a0c679f352012eea66b80335bc3ad1547501dd92
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "103998502"
---
# <a name="ioctl_video_set_display_brightness-control-code"></a><span data-ttu-id="7b85b-103">\_ \_ \_ \_ Код управления яркостью дисплея ioctl Video Set</span><span class="sxs-lookup"><span data-stu-id="7b85b-103">IOCTL\_VIDEO\_SET\_DISPLAY\_BRIGHTNESS control code</span></span>

<span data-ttu-id="7b85b-104">Задает текущие уровни подсветки AC и DC.</span><span class="sxs-lookup"><span data-stu-id="7b85b-104">Sets the current AC and DC backlight levels.</span></span>

<span data-ttu-id="7b85b-105">Чтобы выполнить эту операцию, вызовите функцию [**DeviceIoControl**](/windows/desktop/api/ioapiset/nf-ioapiset-deviceiocontrol) со следующими параметрами.</span><span class="sxs-lookup"><span data-stu-id="7b85b-105">To perform this operation, call the [**DeviceIoControl**](/windows/desktop/api/ioapiset/nf-ioapiset-deviceiocontrol) function with the following parameters.</span></span>


```C++
BOOL DeviceIoControl(
  (HANDLE) hDevice,            // handle to device
  IOCTL_VIDEO_SET_DISPLAY_BRIGHTNESS, // dwIoControlCode
  (LPVOID) lpInBuffer,         // input buffer
  (DWORD) nInBufferSize,       // size of the input buffer
  NULL,                        // lpOutBuffer
  0,                           // nOutBufferSize 
  (LPDWORD) lpBytesReturned,   // number of bytes returned
  (LPOVERLAPPED) lpOverlapped  // OVERLAPPED structure
);
```



## <a name="parameters"></a><span data-ttu-id="7b85b-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="7b85b-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="7b85b-107">*хдевице*</span><span class="sxs-lookup"><span data-stu-id="7b85b-107">*hDevice*</span></span> 
</dt> <dd>

<span data-ttu-id="7b85b-108">Маркер для \\ \\ . \\ ЖК-устройство.</span><span class="sxs-lookup"><span data-stu-id="7b85b-108">A handle to the \\\\.\\LCD device.</span></span> <span data-ttu-id="7b85b-109">Чтобы получить маркер устройства, вызовите функцию [**CreateFile**](/windows/desktop/api/fileapi/nf-fileapi-createfilea) .</span><span class="sxs-lookup"><span data-stu-id="7b85b-109">To retrieve a device handle, call the [**CreateFile**](/windows/desktop/api/fileapi/nf-fileapi-createfilea) function.</span></span>

</dd> <dt>

<span data-ttu-id="7b85b-110">*двиоконтролкоде*</span><span class="sxs-lookup"><span data-stu-id="7b85b-110">*dwIoControlCode*</span></span> 
</dt> <dd>

<span data-ttu-id="7b85b-111">Управляющий код для операции.</span><span class="sxs-lookup"><span data-stu-id="7b85b-111">The control code for the operation.</span></span> <span data-ttu-id="7b85b-112">Это значение определяет конкретную выполняемую операцию и тип устройства, на котором она выполняется.</span><span class="sxs-lookup"><span data-stu-id="7b85b-112">This value identifies the specific operation to be performed and the type of device on which to perform it.</span></span> <span data-ttu-id="7b85b-113">Использовать для этой операции **\_ \_ \_ \_ яркость экрана с помощью ioctl Video Set** .</span><span class="sxs-lookup"><span data-stu-id="7b85b-113">Use **IOCTL\_VIDEO\_SET\_DISPLAY\_BRIGHTNESS** for this operation.</span></span>

</dd> <dt>

<span data-ttu-id="7b85b-114">*лпинбуффер*</span><span class="sxs-lookup"><span data-stu-id="7b85b-114">*lpInBuffer*</span></span> 
</dt> <dd>

<span data-ttu-id="7b85b-115">Указатель на структуру [**\_ яркости экрана**](/previous-versions/windows/desktop/legacy/aa372686(v=vs.85)) .</span><span class="sxs-lookup"><span data-stu-id="7b85b-115">A pointer to a [**DISPLAY\_BRIGHTNESS**](/previous-versions/windows/desktop/legacy/aa372686(v=vs.85)) structure.</span></span>

</dd> <dt>

<span data-ttu-id="7b85b-116">*нинбуфферсизе*</span><span class="sxs-lookup"><span data-stu-id="7b85b-116">*nInBufferSize*</span></span> 
</dt> <dd>

<span data-ttu-id="7b85b-117">Размер буфера, на который указывает *лпаутбуффер*, в байтах.</span><span class="sxs-lookup"><span data-stu-id="7b85b-117">The size of the buffer pointed to by *lpOutBuffer*, in bytes.</span></span>

</dd> <dt>

<span data-ttu-id="7b85b-118">*лпаутбуффер*</span><span class="sxs-lookup"><span data-stu-id="7b85b-118">*lpOutBuffer*</span></span> 
</dt> <dd>

<span data-ttu-id="7b85b-119">Не используется в этой операции; Задайте **значение NULL**.</span><span class="sxs-lookup"><span data-stu-id="7b85b-119">Not used with this operation; set to **NULL**.</span></span>

</dd> <dt>

<span data-ttu-id="7b85b-120">*наутбуфферсизе*</span><span class="sxs-lookup"><span data-stu-id="7b85b-120">*nOutBufferSize*</span></span> 
</dt> <dd>

<span data-ttu-id="7b85b-121">Не используется в этой операции; присвойте ему значение 0.</span><span class="sxs-lookup"><span data-stu-id="7b85b-121">Not used with this operation; set to zero.</span></span>

</dd> <dt>

<span data-ttu-id="7b85b-122">*лпбитесретурнед*</span><span class="sxs-lookup"><span data-stu-id="7b85b-122">*lpBytesReturned*</span></span> 
</dt> <dd>

<span data-ttu-id="7b85b-123">Указатель на переменную, которая получает фактическое число байтов, возвращенных функцией в выходном буфере.</span><span class="sxs-lookup"><span data-stu-id="7b85b-123">A pointer to a variable that receives the actual count of bytes returned by the function in the output buffer.</span></span>

<span data-ttu-id="7b85b-124">Если *лповерлаппед* имеет **значение NULL** (ноноверлаппед I/O), *лпбитесретурнед* используется внутренне и не может иметь **значение NULL**.</span><span class="sxs-lookup"><span data-stu-id="7b85b-124">If *lpOverlapped* is **NULL** (nonoverlapped I/O), *lpBytesReturned* is used internally and cannot be **NULL**.</span></span>

<span data-ttu-id="7b85b-125">Если *лповерлаппед* не **равно NULL** (перекрывающиеся операции ввода-вывода), *лпбитесретурнед* может иметь **значение NULL**.</span><span class="sxs-lookup"><span data-stu-id="7b85b-125">If *lpOverlapped* is not **NULL** (overlapped I/O), *lpBytesReturned* can be **NULL**.</span></span>

</dd> <dt>

<span data-ttu-id="7b85b-126">*лповерлаппед*</span><span class="sxs-lookup"><span data-stu-id="7b85b-126">*lpOverlapped*</span></span> 
</dt> <dd>

<span data-ttu-id="7b85b-127">Указатель на структуру [**OVERLAPPED**](/windows/desktop/api/minwinbase/ns-minwinbase-overlapped) .</span><span class="sxs-lookup"><span data-stu-id="7b85b-127">A pointer to an [**OVERLAPPED**](/windows/desktop/api/minwinbase/ns-minwinbase-overlapped) structure.</span></span>

<span data-ttu-id="7b85b-128">Если *хдевице* был открыт с \_ \_ флагом File Flag OVERLAPPED, *лповерлаппед* должен указывать на допустимую структуру [**OVERLAPPED**](/windows/desktop/api/minwinbase/ns-minwinbase-overlapped) .</span><span class="sxs-lookup"><span data-stu-id="7b85b-128">If *hDevice* was opened with the FILE\_FLAG\_OVERLAPPED flag, *lpOverlapped* must point to a valid [**OVERLAPPED**](/windows/desktop/api/minwinbase/ns-minwinbase-overlapped) structure.</span></span> <span data-ttu-id="7b85b-129">В этом случае операция выполняется как Перекрываемая (асинхронная) операция.</span><span class="sxs-lookup"><span data-stu-id="7b85b-129">In this case, the operation is performed as an overlapped (asynchronous) operation.</span></span> <span data-ttu-id="7b85b-130">Если устройство было открыто с \_ флагом File Flag \_ OVERLAPPED и *Лповерлаппед* имеет **значение NULL**, функция завершается ошибкой непредсказуемым образом.</span><span class="sxs-lookup"><span data-stu-id="7b85b-130">If the device was opened with the FILE\_FLAG\_OVERLAPPED flag and *lpOverlapped* is **NULL**, the function fails in unpredictable ways.</span></span>

<span data-ttu-id="7b85b-131">Если *хдевице* был открыт без указания \_ \_ флага File Flag OVERLAPPED, *Лповерлаппед* игнорируется, а [**DeviceIoControl**](/windows/desktop/api/ioapiset/nf-ioapiset-deviceiocontrol) не возвращает значение до тех пор, пока операция не будет завершена или пока не произойдет ошибка.</span><span class="sxs-lookup"><span data-stu-id="7b85b-131">If *hDevice* was opened without specifying the FILE\_FLAG\_OVERLAPPED flag, *lpOverlapped* is ignored and [**DeviceIoControl**](/windows/desktop/api/ioapiset/nf-ioapiset-deviceiocontrol) does not return until the operation has been completed, or until an error occurs.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="7b85b-132">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="7b85b-132">Return value</span></span>

<span data-ttu-id="7b85b-133">Если операция завершается успешно, [**DeviceIoControl**](/windows/desktop/api/ioapiset/nf-ioapiset-deviceiocontrol) возвращает ненулевое значение.</span><span class="sxs-lookup"><span data-stu-id="7b85b-133">If the operation completes successfully, [**DeviceIoControl**](/windows/desktop/api/ioapiset/nf-ioapiset-deviceiocontrol) returns a nonzero value.</span></span>

<span data-ttu-id="7b85b-134">Если операция завершается неудачно или ожидает выполнения, [**DeviceIoControl**](/windows/desktop/api/ioapiset/nf-ioapiset-deviceiocontrol) возвращает ноль.</span><span class="sxs-lookup"><span data-stu-id="7b85b-134">If the operation fails or is pending, [**DeviceIoControl**](/windows/desktop/api/ioapiset/nf-ioapiset-deviceiocontrol) returns zero.</span></span> <span data-ttu-id="7b85b-135">Дополнительные сведения об ошибке можно получить, вызвав [**GetLastError**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror).</span><span class="sxs-lookup"><span data-stu-id="7b85b-135">To get extended error information, call [**GetLastError**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror).</span></span>

## <a name="remarks"></a><span data-ttu-id="7b85b-136">Комментарии</span><span class="sxs-lookup"><span data-stu-id="7b85b-136">Remarks</span></span>

<span data-ttu-id="7b85b-137">Значения, указанные в элементах **укакбригхтнесс** и **Укдкбригхтнесс** структуры [**\_ яркости экрана**](/previous-versions/windows/desktop/legacy/aa372686(v=vs.85)) , должны быть ранее возвращены с помощью [**\_ запроса видео \_ , \_ поддерживаемого \_ функцией ioctl**](ioctl-video-query-supported-brightness.md).</span><span class="sxs-lookup"><span data-stu-id="7b85b-137">The values specified in the **ucACBrightness** and **ucDCBrightness** members of the [**DISPLAY\_BRIGHTNESS**](/previous-versions/windows/desktop/legacy/aa372686(v=vs.85)) structure must have been previously returned by [**IOCTL\_VIDEO\_QUERY\_SUPPORTED\_BRIGHTNESS**](ioctl-video-query-supported-brightness.md).</span></span> <span data-ttu-id="7b85b-138">Например, если поддерживаются значения 10, 20, 30, 40, 50, 60, 70, 80, 90 и 100, то при использовании значения 33 будет выдаваться ошибка.</span><span class="sxs-lookup"><span data-stu-id="7b85b-138">For example, if the supported values are 10, 20, 30, 40, 50, 60, 70, 80, 90, and 100, then using a value of 33 would be an error.</span></span>

<span data-ttu-id="7b85b-139">Файл заголовка, используемый для создания приложений, включающих эту функцию, Нтддвдео. h, входит в состав пакета средств разработки драйверов Microsoft Windows (DDK).</span><span class="sxs-lookup"><span data-stu-id="7b85b-139">The header file used to build applications that include this functionality, Ntddvdeo.h, is included in the Microsoft Windows Driver Development Kit (DDK).</span></span> <span data-ttu-id="7b85b-140">Сведения о получении DDK см. в разделе [https://www.microsoft.com/whdc/devtools/ddk/default.mspx](https://msdn.microsoft.com/windows/hardware/gg454513) .</span><span class="sxs-lookup"><span data-stu-id="7b85b-140">For information on obtaining the DDK, see [https://www.microsoft.com/whdc/devtools/ddk/default.mspx](https://msdn.microsoft.com/windows/hardware/gg454513).</span></span>

<span data-ttu-id="7b85b-141">Кроме того, этот код элемента управления можно определить следующим образом:</span><span class="sxs-lookup"><span data-stu-id="7b85b-141">Alternatively, you can define this control code as follows:</span></span>

``` syntax
#define IOCTL_VIDEO_SET_DISPLAY_BRIGHTNESS \
  CTL_CODE(FILE_DEVICE_VIDEO, 0x127, METHOD_BUFFERED, FILE_ANY_ACCESS)
```

## <a name="requirements"></a><span data-ttu-id="7b85b-142">Требования</span><span class="sxs-lookup"><span data-stu-id="7b85b-142">Requirements</span></span>



| <span data-ttu-id="7b85b-143">Требование</span><span class="sxs-lookup"><span data-stu-id="7b85b-143">Requirement</span></span> | <span data-ttu-id="7b85b-144">Значение</span><span class="sxs-lookup"><span data-stu-id="7b85b-144">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="7b85b-145">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="7b85b-145">Minimum supported client</span></span><br/> | <span data-ttu-id="7b85b-146">Windows Vista, Windows XP с пакетом обновления 1 (SP1), \[ только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="7b85b-146">Windows Vista, Windows XP with SP1 \[desktop apps only\]</span></span><br/>                   |
| <span data-ttu-id="7b85b-147">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="7b85b-147">Minimum supported server</span></span><br/> | <span data-ttu-id="7b85b-148">\[Только для настольных приложений Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="7b85b-148">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="7b85b-149">Header</span><span class="sxs-lookup"><span data-stu-id="7b85b-149">Header</span></span><br/>                   | <dl> <span data-ttu-id="7b85b-150"><dt>Нтддвдео. h</dt></span><span class="sxs-lookup"><span data-stu-id="7b85b-150"><dt>Ntddvdeo.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="7b85b-151">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="7b85b-151">See also</span></span>

<dl> <dt>

[<span data-ttu-id="7b85b-152">Интерфейс управления подсветкой</span><span class="sxs-lookup"><span data-stu-id="7b85b-152">Backlight Control Interface</span></span>](backlight-control-interface.md)
</dt> <dt>

[<span data-ttu-id="7b85b-153">**DeviceIoControl**</span><span class="sxs-lookup"><span data-stu-id="7b85b-153">**DeviceIoControl**</span></span>](/windows/desktop/api/ioapiset/nf-ioapiset-deviceiocontrol)
</dt> <dt>

<span data-ttu-id="7b85b-154">[**\_яркость экрана**](/previous-versions/windows/desktop/legacy/aa372686(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="7b85b-154">[**DISPLAY\_BRIGHTNESS**](/previous-versions/windows/desktop/legacy/aa372686(v=vs.85))</span></span>
</dt> <dt>

[<span data-ttu-id="7b85b-155">**\_ \_ \_ яркость экрана запроса видео \_ ioctl**</span><span class="sxs-lookup"><span data-stu-id="7b85b-155">**IOCTL\_VIDEO\_QUERY\_DISPLAY\_BRIGHTNESS**</span></span>](ioctl-video-query-display-brightness.md)
</dt> <dt>

[<span data-ttu-id="7b85b-156">**видеозапрос IOCTL — \_ \_ \_ поддерживаемая \_ яркость**</span><span class="sxs-lookup"><span data-stu-id="7b85b-156">**IOCTL\_VIDEO\_QUERY\_SUPPORTED\_BRIGHTNESS**</span></span>](ioctl-video-query-supported-brightness.md)
</dt> </dl>

 

