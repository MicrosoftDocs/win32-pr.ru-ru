---
description: Извлекает различные сведения о батарее.
ms.assetid: 4cc89b89-ab33-47c2-8327-9627cbd1595e
title: Код элемента управления IOCTL_BATTERY_QUERY_INFORMATION (Покласс. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IOCTL_BATTERY_QUERY_INFORMATION
api_type:
- HeaderDef
api_location:
- Poclass.h
- BatClass.h
ms.openlocfilehash: ee4010e055686c0df2987c34b48b133975b434ce
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "103998503"
---
# <a name="ioctl_battery_query_information-control-code"></a><span data-ttu-id="550f0-103">\_ \_ \_ Код управления сведениями о запросе к батарее ioctl</span><span class="sxs-lookup"><span data-stu-id="550f0-103">IOCTL\_BATTERY\_QUERY\_INFORMATION control code</span></span>

<span data-ttu-id="550f0-104">Извлекает различные сведения о батарее.</span><span class="sxs-lookup"><span data-stu-id="550f0-104">Retrieves a variety of information for the battery.</span></span>

<span data-ttu-id="550f0-105">Чтобы выполнить эту операцию, вызовите функцию [**DeviceIoControl**](/windows/desktop/api/ioapiset/nf-ioapiset-deviceiocontrol) со следующими параметрами.</span><span class="sxs-lookup"><span data-stu-id="550f0-105">To perform this operation, call the [**DeviceIoControl**](/windows/desktop/api/ioapiset/nf-ioapiset-deviceiocontrol) function with the following parameters.</span></span>


```C++
BOOL DeviceIoControl(
  (HANDLE) hDevice,                // handle to battery
  IOCTL_BATTERY_QUERY_INFORMATION, // dwIoControlCode
  (LPVOID) lpInBuffer,             // input buffer
  (DWORD) nInBufferSize,           // size of input buffer
  (LPVOID) lpOutBuffer,            // output buffer
  (DWORD) nOutBufferSize,          // size of output buffer
  (LPDWORD) lpBytesReturned,       // number of bytes returned
  (LPOVERLAPPED) lpOverlapped      // OVERLAPPED structure
);
```



## <a name="parameters"></a><span data-ttu-id="550f0-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="550f0-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="550f0-107">*хдевице*</span><span class="sxs-lookup"><span data-stu-id="550f0-107">*hDevice*</span></span> 
</dt> <dd>

<span data-ttu-id="550f0-108">Маркер батареи, сведения о котором должны быть возвращены.</span><span class="sxs-lookup"><span data-stu-id="550f0-108">A handle to the battery on which information is to be returned.</span></span> <span data-ttu-id="550f0-109">Чтобы получить маркер устройства, вызовите функцию [**CreateFile**](/windows/desktop/api/fileapi/nf-fileapi-createfilea) .</span><span class="sxs-lookup"><span data-stu-id="550f0-109">To retrieve a device handle, call the [**CreateFile**](/windows/desktop/api/fileapi/nf-fileapi-createfilea) function.</span></span>

</dd> <dt>

<span data-ttu-id="550f0-110">*двиоконтролкоде*</span><span class="sxs-lookup"><span data-stu-id="550f0-110">*dwIoControlCode*</span></span> 
</dt> <dd>

<span data-ttu-id="550f0-111">Управляющий код для операции.</span><span class="sxs-lookup"><span data-stu-id="550f0-111">The control code for the operation.</span></span> <span data-ttu-id="550f0-112">Это значение определяет конкретную выполняемую операцию и тип устройства, на котором она выполняется.</span><span class="sxs-lookup"><span data-stu-id="550f0-112">This value identifies the specific operation to be performed and the type of device on which to perform it.</span></span> <span data-ttu-id="550f0-113">Для выполнения этой операции используйте **\_ \_ \_ сведения о запросе аккумулятора** с помощью ioctl.</span><span class="sxs-lookup"><span data-stu-id="550f0-113">Use **IOCTL\_BATTERY\_QUERY\_INFORMATION** for this operation.</span></span>

</dd> <dt>

<span data-ttu-id="550f0-114">*лпинбуффер*</span><span class="sxs-lookup"><span data-stu-id="550f0-114">*lpInBuffer*</span></span> 
</dt> <dd>

<span data-ttu-id="550f0-115">Указатель на [**\_ \_ информационную структуру запроса батареи**](battery-query-information-str.md) .</span><span class="sxs-lookup"><span data-stu-id="550f0-115">A pointer to a [**BATTERY\_QUERY\_INFORMATION**](battery-query-information-str.md) structure.</span></span>

</dd> <dt>

<span data-ttu-id="550f0-116">*нинбуфферсизе*</span><span class="sxs-lookup"><span data-stu-id="550f0-116">*nInBufferSize*</span></span> 
</dt> <dd>

<span data-ttu-id="550f0-117">Размер входного буфера в байтах.</span><span class="sxs-lookup"><span data-stu-id="550f0-117">The size of the input buffer, in bytes.</span></span>

</dd> <dt>

<span data-ttu-id="550f0-118">*лпаутбуффер*</span><span class="sxs-lookup"><span data-stu-id="550f0-118">*lpOutBuffer*</span></span> 
</dt> <dd>

<span data-ttu-id="550f0-119">Указатель на буфер возврата.</span><span class="sxs-lookup"><span data-stu-id="550f0-119">A pointer to the return buffer.</span></span> <span data-ttu-id="550f0-120">Тип данных (и, следовательно, размер) буфера возврата зависит от информации, запрашиваемой элементом **\_ \_ \_ уровень информации о заряде аккумулятора** в структуре входных [**\_ \_ данных запроса**](battery-query-information-str.md) .</span><span class="sxs-lookup"><span data-stu-id="550f0-120">The data type (and, therefore, size) of the return buffer depends on the information requested in the **BATTERY\_QUERY\_INFORMATION\_LEVEL** member of the input [**BATTERY\_QUERY\_INFORMATION**](battery-query-information-str.md) structure.</span></span>

<span data-ttu-id="550f0-121">В следующей таблице показаны данные, возвращаемые данным уровнем данных.</span><span class="sxs-lookup"><span data-stu-id="550f0-121">The following table shows the data returned by a given information level.</span></span>



| <span data-ttu-id="550f0-122">Уровень информации</span><span class="sxs-lookup"><span data-stu-id="550f0-122">Information level</span></span>                 | <span data-ttu-id="550f0-123">Возвращенные данные</span><span class="sxs-lookup"><span data-stu-id="550f0-123">Data returned</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                     |
|-----------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="550f0-124">**баттеридевиценаме**</span><span class="sxs-lookup"><span data-stu-id="550f0-124">**BatteryDeviceName**</span></span>             | <span data-ttu-id="550f0-125">Строка Юникода, заканчивающаяся **нулем,** которая указывает имя батареи.</span><span class="sxs-lookup"><span data-stu-id="550f0-125">**Null**-terminated Unicode string that specifies the battery's name.</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                             |
| <span data-ttu-id="550f0-126">**баттерестиматедтиме**</span><span class="sxs-lookup"><span data-stu-id="550f0-126">**BatteryEstimatedTime**</span></span>          | <span data-ttu-id="550f0-127">**Ulong** , указывающая предполагаемое время выполнения аккумулятора в секундах.</span><span class="sxs-lookup"><span data-stu-id="550f0-127">A **ULONG** that specifies estimated battery run time, in seconds.</span></span> <span data-ttu-id="550f0-128">Если скорость очистки, указанная в элементе **атрате** в структуре [**\_ \_ данных запроса аккумулятора**](battery-query-information-str.md) , равна нулю, это вычисление основывается на текущей скорости очистки.</span><span class="sxs-lookup"><span data-stu-id="550f0-128">If the rate of drain provided in the **AtRate** member of the [**BATTERY\_QUERY\_INFORMATION**](battery-query-information-str.md) structure is zero, this calculation is based on the present rate of drain.</span></span> <span data-ttu-id="550f0-129">Если **атрате** не равно нулю, то возвращаемое время является ожидаемым временем выполнения для заданной ставки.</span><span class="sxs-lookup"><span data-stu-id="550f0-129">If **AtRate** is nonzero, the time returned is the expected run time for the given rate.</span></span> <span data-ttu-id="550f0-130">Если расчетное время неизвестно (например, батарея не расряжается, а **атрате** — нуль), возвращается **\_ неизвестное \_ время работы аккумулятора** .</span><span class="sxs-lookup"><span data-stu-id="550f0-130">If the estimated time is unknown (for example, the battery is not discharging and **AtRate** is zero), **BATTERY\_UNKNOWN\_TIME** is returned.</span></span> <span data-ttu-id="550f0-131">Обратите внимание, что это значение не очень точное в некоторых системах с батареей.</span><span class="sxs-lookup"><span data-stu-id="550f0-131">Note that this value is not very accurate on some battery systems.</span></span> <span data-ttu-id="550f0-132">Это значение может сильно различаться в зависимости от текущего энергопотребления, которое может зависеть от активности диска и других факторов.</span><span class="sxs-lookup"><span data-stu-id="550f0-132">The value may vary widely depending on present power usage, which could be affected by disk activity and other factors.</span></span> <span data-ttu-id="550f0-133">В этом значении нет механизма уведомления об изменениях.</span><span class="sxs-lookup"><span data-stu-id="550f0-133">There is no notification mechanism for changes in this value.</span></span> |
| <span data-ttu-id="550f0-134">**баттеригрануларитинформатион**</span><span class="sxs-lookup"><span data-stu-id="550f0-134">**BatteryGranularityInformation**</span></span> | <span data-ttu-id="550f0-135">Массив переменной длины, содержащий [**\_ \_ коэффициенты масштабирования аккумулятора**](/windows/desktop/api/WinNT/ns-winnt-battery_reporting_scale) , который содержит сведения о степени детализации аккумулятора, возвращаемой из [**\_ \_ \_ состояния запроса IOCTL от аккумулятора**](ioctl-battery-query-status.md).</span><span class="sxs-lookup"><span data-stu-id="550f0-135">A variable-length array of [**BATTERY\_REPORTING\_SCALE**](/windows/desktop/api/WinNT/ns-winnt-battery_reporting_scale) structures that contains the reporting granularity for the battery capacity that is returned from [**IOCTL\_BATTERY\_QUERY\_STATUS**](ioctl-battery-query-status.md).</span></span> <span data-ttu-id="550f0-136">Если гранулярность зависит от текущей емкости батареи, возвращаются несколько записей.</span><span class="sxs-lookup"><span data-stu-id="550f0-136">Multiple entries are returned when the granularity depends on the present capacity of the battery.</span></span> <span data-ttu-id="550f0-137">Интерпретация массива записей см. в разделе **\_ \_ масштабирование отчетов батареи** .</span><span class="sxs-lookup"><span data-stu-id="550f0-137">See **BATTERY\_REPORTING\_SCALE** for the interpretation of the array of entries.</span></span> <span data-ttu-id="550f0-138">Количество записей определяется размером возвращенного буфера и может быть вычислено (*лпбитесретурнед* /sizeof (**\_ \_ Масштаб отчета батареи**)).</span><span class="sxs-lookup"><span data-stu-id="550f0-138">The number of entries is indicated by the size of the buffer returned, and can be calculated as (*lpBytesReturned* / sizeof (**BATTERY\_REPORTING\_SCALE**)).</span></span> <span data-ttu-id="550f0-139">Максимальное число возвращаемых записей равно четырем.</span><span class="sxs-lookup"><span data-stu-id="550f0-139">The maximum number of entries that will be returned is four.</span></span>                                                                                                |
| <span data-ttu-id="550f0-140">**баттеринформатион**</span><span class="sxs-lookup"><span data-stu-id="550f0-140">**BatteryInformation**</span></span>            | <span data-ttu-id="550f0-141">Структура [**\_ сведений о батарее**](battery-information-str.md) .</span><span class="sxs-lookup"><span data-stu-id="550f0-141">A [**BATTERY\_INFORMATION**](battery-information-str.md) structure.</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                              |
| <span data-ttu-id="550f0-142">**баттеримануфактуредате**</span><span class="sxs-lookup"><span data-stu-id="550f0-142">**BatteryManufactureDate**</span></span>        | <span data-ttu-id="550f0-143">Структура [**\_ \_ даты изготовления аккумулятора**](battery-manufacture-date-str.md) .</span><span class="sxs-lookup"><span data-stu-id="550f0-143">A [**BATTERY\_MANUFACTURE\_DATE**](battery-manufacture-date-str.md) structure.</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                   |
| <span data-ttu-id="550f0-144">**баттеримануфактуренаме**</span><span class="sxs-lookup"><span data-stu-id="550f0-144">**BatteryManufactureName**</span></span>        | <span data-ttu-id="550f0-145">Строка Юникода, заканчивающаяся **нулем**, которая содержит имя производителя батареи.</span><span class="sxs-lookup"><span data-stu-id="550f0-145">**Null**-terminated Unicode string that contains the name of the manufacturer of the battery.</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                     |
| <span data-ttu-id="550f0-146">**баттерисериалнумбер**</span><span class="sxs-lookup"><span data-stu-id="550f0-146">**BatterySerialNumber**</span></span>           | <span data-ttu-id="550f0-147">Строка Юникода, заканчивающаяся **нулем**, которая содержит серийный номер аккумулятора.</span><span class="sxs-lookup"><span data-stu-id="550f0-147">**Null**-terminated Unicode string that contains the battery's serial number.</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                     |
| <span data-ttu-id="550f0-148">**баттеритемпературе**</span><span class="sxs-lookup"><span data-stu-id="550f0-148">**BatteryTemperature**</span></span>            | <span data-ttu-id="550f0-149">**Ulong** , которая содержит текущую температуру батареи (в десятых градусах градуса Кельвина).</span><span class="sxs-lookup"><span data-stu-id="550f0-149">A **ULONG** that contains the battery's current temperature, in 10ths of a degree Kelvin.</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                         |
| <span data-ttu-id="550f0-150">**баттерюникуеид**</span><span class="sxs-lookup"><span data-stu-id="550f0-150">**BatteryUniqueID**</span></span>               | <span data-ttu-id="550f0-151">Строка Юникода, заканчивающаяся **нулем**, которая однозначно определяет батарею.</span><span class="sxs-lookup"><span data-stu-id="550f0-151">**Null**-terminated Unicode string that uniquely identifies the battery.</span></span> <span data-ttu-id="550f0-152">Это значение можно использовать для контроля определенного аккумулятора.</span><span class="sxs-lookup"><span data-stu-id="550f0-152">This value can be used to track a specific battery.</span></span> <span data-ttu-id="550f0-153">В случае Smart-батарей этот идентификатор будет использоваться для объединения имени производителя, имени устройства, даты изготовления и печатного представления серийного номера.</span><span class="sxs-lookup"><span data-stu-id="550f0-153">In the case of smart batteries, this ID will be the concatenation of the manufacturer's name, device name, date of manufacture, and a printable representation of the serial number.</span></span> <span data-ttu-id="550f0-154">Это значение не должно отображаться для пользователя.</span><span class="sxs-lookup"><span data-stu-id="550f0-154">This value is not intended to be displayed to the user.</span></span><br/>                                                                                                                                                                                                                                                                                                                                                                                              |



 

</dd> <dt>

<span data-ttu-id="550f0-155">*наутбуфферсизе*</span><span class="sxs-lookup"><span data-stu-id="550f0-155">*nOutBufferSize*</span></span> 
</dt> <dd>

<span data-ttu-id="550f0-156">Размер выходного буфера в байтах.</span><span class="sxs-lookup"><span data-stu-id="550f0-156">The size of the output buffer, in bytes.</span></span> <span data-ttu-id="550f0-157">В зависимости от уровня информации запрошенных данных это может быть буфер размера вариабли.</span><span class="sxs-lookup"><span data-stu-id="550f0-157">Depending on the information level of data requested, this may be a variably sized buffer.</span></span>

</dd> <dt>

<span data-ttu-id="550f0-158">*лпбитесретурнед*</span><span class="sxs-lookup"><span data-stu-id="550f0-158">*lpBytesReturned*</span></span> 
</dt> <dd>

<span data-ttu-id="550f0-159">Указатель на переменную, которая получает размер данных, возвращаемых в буфере *лпаутбуффер* , в байтах.</span><span class="sxs-lookup"><span data-stu-id="550f0-159">A pointer to a variable that receives the size of the data returned in the *lpOutBuffer* buffer, in bytes.</span></span>

<span data-ttu-id="550f0-160">Если выходной буфер слишком мал для возвращения каких-либо данных, то вызов завершается неудачно, [**GetLastError**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror) возвращает код ошибки **\_ недостаточный \_ Размер буфера**, а возвращенное число байтов равно нулю.</span><span class="sxs-lookup"><span data-stu-id="550f0-160">If the output buffer is too small to return any data then the call fails, [**GetLastError**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror) returns the error code **ERROR\_INSUFFICIENT\_BUFFER**, and the returned byte count is zero.</span></span>

<span data-ttu-id="550f0-161">Если *лповерлаппед* имеет **значение NULL** (ноноверлаппед I/O), *Лпбитесретурнед* не может иметь **значение NULL**.</span><span class="sxs-lookup"><span data-stu-id="550f0-161">If *lpOverlapped* is **NULL** (nonoverlapped I/O), *lpBytesReturned* cannot be **NULL**.</span></span>

<span data-ttu-id="550f0-162">Если *лповерлаппед* не **равно NULL** (перекрывающиеся операции ввода-вывода), *лпбитесретурнед* может иметь **значение NULL**.</span><span class="sxs-lookup"><span data-stu-id="550f0-162">If *lpOverlapped* is not **NULL** (overlapped I/O), *lpBytesReturned* can be **NULL**.</span></span> <span data-ttu-id="550f0-163">Если это операция с перекрытием, можно получить число байтов, возвращенных путем вызова функции [**GetOverlappedResult**](/windows/desktop/api/ioapiset/nf-ioapiset-getoverlappedresult) .</span><span class="sxs-lookup"><span data-stu-id="550f0-163">If this is an overlapped operation, you can retrieve the number of bytes returned by calling the [**GetOverlappedResult**](/windows/desktop/api/ioapiset/nf-ioapiset-getoverlappedresult) function.</span></span> <span data-ttu-id="550f0-164">Если *хдевице* связан с портом завершения ввода-вывода, можно получить число возвращаемых байтов, вызвав функцию [**жеткуеуедкомплетионстатус**](/windows/desktop/api/ioapiset/nf-ioapiset-getqueuedcompletionstatus) .</span><span class="sxs-lookup"><span data-stu-id="550f0-164">If *hDevice* is associated with an I/O completion port, you can get the number of bytes returned by calling the [**GetQueuedCompletionStatus**](/windows/desktop/api/ioapiset/nf-ioapiset-getqueuedcompletionstatus) function.</span></span>

</dd> <dt>

<span data-ttu-id="550f0-165">*лповерлаппед*</span><span class="sxs-lookup"><span data-stu-id="550f0-165">*lpOverlapped*</span></span> 
</dt> <dd>

<span data-ttu-id="550f0-166">Указатель на структуру [**OVERLAPPED**](/windows/desktop/api/minwinbase/ns-minwinbase-overlapped) .</span><span class="sxs-lookup"><span data-stu-id="550f0-166">A pointer to an [**OVERLAPPED**](/windows/desktop/api/minwinbase/ns-minwinbase-overlapped) structure.</span></span>

<span data-ttu-id="550f0-167">Если *хдевице* был открыт с флагом **File \_ Flag \_ OVERLAPPED** , *ЛПОВЕРЛАППЕД* должен указывать на допустимую структуру [**OVERLAPPED**](/windows/desktop/api/minwinbase/ns-minwinbase-overlapped) .</span><span class="sxs-lookup"><span data-stu-id="550f0-167">If *hDevice* was opened with the **FILE\_FLAG\_OVERLAPPED** flag, *lpOverlapped* must point to a valid [**OVERLAPPED**](/windows/desktop/api/minwinbase/ns-minwinbase-overlapped) structure.</span></span> <span data-ttu-id="550f0-168">В этом случае [**DeviceIoControl**](/windows/desktop/api/ioapiset/nf-ioapiset-deviceiocontrol) выполняется как Перекрываемая (асинхронная) операция.</span><span class="sxs-lookup"><span data-stu-id="550f0-168">In this case, [**DeviceIoControl**](/windows/desktop/api/ioapiset/nf-ioapiset-deviceiocontrol) is performed as an overlapped (asynchronous) operation.</span></span> <span data-ttu-id="550f0-169">Если устройство было открыто с флагом **File \_ Flag \_ OVERLAPPED** и *лповерлаппед* имеет **значение NULL**, функция завершается ошибкой непредсказуемым образом.</span><span class="sxs-lookup"><span data-stu-id="550f0-169">If the device was opened with the **FILE\_FLAG\_OVERLAPPED** flag and *lpOverlapped* is **NULL**, the function fails in unpredictable ways.</span></span>

<span data-ttu-id="550f0-170">Если *хдевице* был открыт без указания флага **File \_ Flag \_ OVERLAPPED** , *лповерлаппед* игнорируется и функция [**DeviceIoControl**](/windows/desktop/api/ioapiset/nf-ioapiset-deviceiocontrol) не возвращает значение до тех пор, пока операция не будет завершена или пока не произойдет ошибка.</span><span class="sxs-lookup"><span data-stu-id="550f0-170">If *hDevice* was opened without specifying the **FILE\_FLAG\_OVERLAPPED** flag, *lpOverlapped* is ignored and the [**DeviceIoControl**](/windows/desktop/api/ioapiset/nf-ioapiset-deviceiocontrol) function does not return until the operation has been completed, or until an error occurs.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="550f0-171">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="550f0-171">Return value</span></span>

<span data-ttu-id="550f0-172">Если операция завершается успешно, [**DeviceIoControl**](/windows/desktop/api/ioapiset/nf-ioapiset-deviceiocontrol) возвращает ненулевое значение.</span><span class="sxs-lookup"><span data-stu-id="550f0-172">If the operation completes successfully, [**DeviceIoControl**](/windows/desktop/api/ioapiset/nf-ioapiset-deviceiocontrol) returns a nonzero value.</span></span>

<span data-ttu-id="550f0-173">Если операция завершается неудачно или ожидает выполнения, [**DeviceIoControl**](/windows/desktop/api/ioapiset/nf-ioapiset-deviceiocontrol) возвращает ноль.</span><span class="sxs-lookup"><span data-stu-id="550f0-173">If the operation fails or is pending, [**DeviceIoControl**](/windows/desktop/api/ioapiset/nf-ioapiset-deviceiocontrol) returns zero.</span></span> <span data-ttu-id="550f0-174">Дополнительные сведения об ошибке можно получить, вызвав [**GetLastError**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror).</span><span class="sxs-lookup"><span data-stu-id="550f0-174">To get extended error information, call [**GetLastError**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror).</span></span>

<span data-ttu-id="550f0-175">Некоторые сведения о батареях являются необязательными или могут быть бессмысленными для некоторых батарей.</span><span class="sxs-lookup"><span data-stu-id="550f0-175">Some information about batteries is optional or may be meaningless for some batteries.</span></span> <span data-ttu-id="550f0-176">Если запрошенный тип данных недоступен для текущего аккумулятора, то возвращается **Ошибка \_ Недопустимая \_ функция** .</span><span class="sxs-lookup"><span data-stu-id="550f0-176">If the particular type of data requested is not available for the current battery, then **ERROR\_INVALID\_FUNCTION** is returned.</span></span>

<span data-ttu-id="550f0-177">Все запросы сведений о батарее будут завершены с состоянием " **\_ файл ошибки \_ не \_ найден** ", если элемент **баттеритаг** запроса не соответствует значению текущего тега батареи.</span><span class="sxs-lookup"><span data-stu-id="550f0-177">All requests for battery information will complete with the status of **ERROR\_FILE\_NOT\_FOUND** whenever the **BatteryTag** element of the request does not match that of the current battery tag.</span></span> <span data-ttu-id="550f0-178">Это гарантирует, что возвращенные сведения о батарее соответствуют запрошенному аккумулятору.</span><span class="sxs-lookup"><span data-stu-id="550f0-178">This ensures that the returned battery information matches that of the requested battery.</span></span> <span data-ttu-id="550f0-179">(Дополнительные сведения см. в разделе " [теги батареи](battery-information.md) ".)</span><span class="sxs-lookup"><span data-stu-id="550f0-179">(See [Battery Tags](battery-information.md) for more information.)</span></span>

## <a name="remarks"></a><span data-ttu-id="550f0-180">Комментарии</span><span class="sxs-lookup"><span data-stu-id="550f0-180">Remarks</span></span>

<span data-ttu-id="550f0-181">Этот параметр аккумулятора IOCTL получает разнообразные сведения о батарее.</span><span class="sxs-lookup"><span data-stu-id="550f0-181">This battery IOCTL retrieves a variety of information for the battery.</span></span> <span data-ttu-id="550f0-182">Структура входного параметра, [**\_ \_ сведения о запросе аккумулятора**](battery-query-information-str.md), указывает тип возвращаемых данных и сведения о батарее.</span><span class="sxs-lookup"><span data-stu-id="550f0-182">The input parameter structure, [**BATTERY\_QUERY\_INFORMATION**](battery-query-information-str.md), indicates the type of information to be returned and when the battery information should be returned.</span></span> <span data-ttu-id="550f0-183">Тип данных и содержимое выходного буфера зависят от запрошенных данных.</span><span class="sxs-lookup"><span data-stu-id="550f0-183">The data type and contents of the output buffer vary based on the data requested.</span></span>

<span data-ttu-id="550f0-184">Влияние перекрывающегося ввода-вывода на эту операцию см. в разделе "Примечания" раздела [**DeviceIoControl**](/windows/desktop/api/ioapiset/nf-ioapiset-deviceiocontrol) .</span><span class="sxs-lookup"><span data-stu-id="550f0-184">For the implications of overlapped I/O on this operation, see the Remarks section of the [**DeviceIoControl**](/windows/desktop/api/ioapiset/nf-ioapiset-deviceiocontrol) topic.</span></span>

## <a name="examples"></a><span data-ttu-id="550f0-185">Примеры</span><span class="sxs-lookup"><span data-stu-id="550f0-185">Examples</span></span>

<span data-ttu-id="550f0-186">Пример см. в разделе [Перечисление устройств аккумулятора](enumerating-battery-devices.md).</span><span class="sxs-lookup"><span data-stu-id="550f0-186">For an example, see [Enumerating Battery Devices](enumerating-battery-devices.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="550f0-187">Требования</span><span class="sxs-lookup"><span data-stu-id="550f0-187">Requirements</span></span>



| <span data-ttu-id="550f0-188">Требование</span><span class="sxs-lookup"><span data-stu-id="550f0-188">Requirement</span></span> | <span data-ttu-id="550f0-189">Значение</span><span class="sxs-lookup"><span data-stu-id="550f0-189">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="550f0-190">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="550f0-190">Minimum supported client</span></span><br/> | <span data-ttu-id="550f0-191">Только для \[ классических приложений Windows XP\]</span><span class="sxs-lookup"><span data-stu-id="550f0-191">Windows XP \[desktop apps only\]</span></span><br/>                                                                                                                                                                                                                         |
| <span data-ttu-id="550f0-192">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="550f0-192">Minimum supported server</span></span><br/> | <span data-ttu-id="550f0-193">\[Только для настольных приложений Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="550f0-193">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                                                                                                                                                                                                |
| <span data-ttu-id="550f0-194">Header</span><span class="sxs-lookup"><span data-stu-id="550f0-194">Header</span></span><br/>                   | <dl> <span data-ttu-id="550f0-195"><dt>Покласс. h; </dt> <dt>Баткласс. h в Windows server 2008 R2, Windows 7, Windows server 2008, Windows Vista, Windows server 2003 и Windows XP</dt></span><span class="sxs-lookup"><span data-stu-id="550f0-195"><dt>Poclass.h; </dt> <dt>BatClass.h on Windows Server 2008 R2, Windows 7, Windows Server 2008, Windows Vista, Windows Server 2003 and Windows XP</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="550f0-196">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="550f0-196">See also</span></span>

<dl> <dt>

[<span data-ttu-id="550f0-197">Сведения о батарее</span><span class="sxs-lookup"><span data-stu-id="550f0-197">Battery Information</span></span>](battery-information.md)
</dt> <dt>

[<span data-ttu-id="550f0-198">Управляющие коды управления питанием</span><span class="sxs-lookup"><span data-stu-id="550f0-198">Power Management Control Codes</span></span>](power-management-control-codes.md)
</dt> <dt>

[<span data-ttu-id="550f0-199">**DeviceIoControl**</span><span class="sxs-lookup"><span data-stu-id="550f0-199">**DeviceIoControl**</span></span>](/windows/desktop/api/ioapiset/nf-ioapiset-deviceiocontrol)
</dt> <dt>

[<span data-ttu-id="550f0-200">**\_ \_ сведения о запросе аккумулятора**</span><span class="sxs-lookup"><span data-stu-id="550f0-200">**BATTERY\_QUERY\_INFORMATION**</span></span>](battery-query-information-str.md)
</dt> <dt>

[<span data-ttu-id="550f0-201">**\_ \_ масштабирование отчета батареи**</span><span class="sxs-lookup"><span data-stu-id="550f0-201">**BATTERY\_REPORTING\_SCALE**</span></span>](/windows/desktop/api/WinNT/ns-winnt-battery_reporting_scale)
</dt> <dt>

[<span data-ttu-id="550f0-202">**\_ \_ состояние запроса аккумулятора \_ ioctl**</span><span class="sxs-lookup"><span data-stu-id="550f0-202">**IOCTL\_BATTERY\_QUERY\_STATUS**</span></span>](ioctl-battery-query-status.md)
</dt> <dt>

[<span data-ttu-id="550f0-203">**\_тег запроса на батарею ioctl \_ \_**</span><span class="sxs-lookup"><span data-stu-id="550f0-203">**IOCTL\_BATTERY\_QUERY\_TAG**</span></span>](ioctl-battery-query-tag.md)
</dt> <dt>

[<span data-ttu-id="550f0-204">**\_ \_ сведения о настройке аккумулятора ioctl \_**</span><span class="sxs-lookup"><span data-stu-id="550f0-204">**IOCTL\_BATTERY\_SET\_INFORMATION**</span></span>](ioctl-battery-set-information.md)
</dt> </dl>

 

