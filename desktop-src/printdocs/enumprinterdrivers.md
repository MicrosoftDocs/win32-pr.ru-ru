---
description: Функция Енумпринтердриверс перечисляет драйверы принтера, установленные на указанном сервере принтера.
ms.assetid: fa3d8cf4-70bc-4362-833e-e4217ed5d43b
title: Функция Енумпринтердриверс (Винспул. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- EnumPrinterDrivers
- EnumPrinterDriversA
- EnumPrinterDriversW
api_type:
- DllExport
api_location:
- Winspool.drv
- Ext-MS-Win-Printer-WinSpool-L1-1-3.dll
ms.openlocfilehash: c5175daf0a59ac4231baa1a32772863a0017c45d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "103813552"
---
# <a name="enumprinterdrivers-function"></a><span data-ttu-id="873cb-103">Функция Енумпринтердриверс</span><span class="sxs-lookup"><span data-stu-id="873cb-103">EnumPrinterDrivers function</span></span>

<span data-ttu-id="873cb-104">Функция **енумпринтердриверс** перечисляет драйверы принтера, установленные на указанном сервере принтера.</span><span class="sxs-lookup"><span data-stu-id="873cb-104">The **EnumPrinterDrivers** function enumerates the printer drivers installed on a specified printer server.</span></span>

## <a name="syntax"></a><span data-ttu-id="873cb-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="873cb-105">Syntax</span></span>


```C++
BOOL EnumPrinterDrivers(
  _In_  LPTSTR  pName,
  _In_  LPTSTR  pEnvironment,
  _In_  DWORD   Level,
  _Out_ LPBYTE  pDriverInfo,
  _In_  DWORD   cbBuf,
  _Out_ LPDWORD pcbNeeded,
  _Out_ LPDWORD pcReturned
);
```



## <a name="parameters"></a><span data-ttu-id="873cb-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="873cb-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="873cb-107">*pName* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="873cb-107">*pName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="873cb-108">Указатель на строку, завершающуюся нулем, которая указывает имя сервера, на котором перечислены драйверы принтеров.</span><span class="sxs-lookup"><span data-stu-id="873cb-108">A pointer to a null-terminated string that specifies the name of the server on which the printer drivers are enumerated.</span></span>

<span data-ttu-id="873cb-109">Если *pName* имеет **значение NULL**, функция перечисляет драйверы локального принтера.</span><span class="sxs-lookup"><span data-stu-id="873cb-109">If *pName* is **NULL**, the function enumerates the local printer drivers.</span></span>

</dd> <dt>

<span data-ttu-id="873cb-110">*пенвиронмент* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="873cb-110">*pEnvironment* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="873cb-111">Указатель на строку, завершающуюся нулем, которая указывает среду (например, Windows x86, Windows IA64, Windows x64 или Windows NT R4000).</span><span class="sxs-lookup"><span data-stu-id="873cb-111">A pointer to a null-terminated string that specifies the environment (for example, Windows x86, Windows IA64, Windows x64, or Windows NT R4000).</span></span> <span data-ttu-id="873cb-112">Если этот параметр имеет **значение NULL**, функция использует текущую среду вызывающего или клиентского объекта (не целевого или сервера).</span><span class="sxs-lookup"><span data-stu-id="873cb-112">If this parameter is **NULL**, the function uses the current environment of the caller/client (not of the destination/server).</span></span>

<span data-ttu-id="873cb-113">Если в строке *пенвиронмент* указано значение ALL, **енумпринтердриверс** перечисляет драйверы принтеров для всех платформ, установленных на указанном сервере.</span><span class="sxs-lookup"><span data-stu-id="873cb-113">If the *pEnvironment* string specifies "all", **EnumPrinterDrivers** enumerates printer drivers for all platforms installed on the specified server.</span></span>

</dd> <dt>

<span data-ttu-id="873cb-114">*Уровень* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="873cb-114">*Level* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="873cb-115">Тип информационной структуры, возвращаемой в буфере *пдриверинфо* .</span><span class="sxs-lookup"><span data-stu-id="873cb-115">The type of information structure returned in the *pDriverInfo* buffer.</span></span> <span data-ttu-id="873cb-116">Может быть одним из следующих.</span><span class="sxs-lookup"><span data-stu-id="873cb-116">It can be one of the following.</span></span>



| <span data-ttu-id="873cb-117">Значение</span><span class="sxs-lookup"><span data-stu-id="873cb-117">Value</span></span>                                                                                                | <span data-ttu-id="873cb-118">Значение</span><span class="sxs-lookup"><span data-stu-id="873cb-118">Meaning</span></span>                                             |
|------------------------------------------------------------------------------------------------------|-----------------------------------------------------|
| <span id="1"></span><dl> <span data-ttu-id="873cb-119"><dt>**1**</dt></span><span class="sxs-lookup"><span data-stu-id="873cb-119"><dt>**1**</dt></span></span> </dl> | [<span data-ttu-id="873cb-120">**\_Сведения о драйвере \_ 1**</span><span class="sxs-lookup"><span data-stu-id="873cb-120">**DRIVER\_INFO\_1**</span></span>](driver-info-1.md)<br/> |
| <span id="2"></span><dl> <span data-ttu-id="873cb-121"><dt>**2**</dt></span><span class="sxs-lookup"><span data-stu-id="873cb-121"><dt>**2**</dt></span></span> </dl> | [<span data-ttu-id="873cb-122">**\_Сведения о драйвере \_ 2**</span><span class="sxs-lookup"><span data-stu-id="873cb-122">**DRIVER\_INFO\_2**</span></span>](driver-info-2.md)<br/> |
| <span id="3"></span><dl> <span data-ttu-id="873cb-123"><dt>**3-5**</dt></span><span class="sxs-lookup"><span data-stu-id="873cb-123"><dt>**3**</dt></span></span> </dl> | [<span data-ttu-id="873cb-124">**\_Сведения о драйвере \_ 3**</span><span class="sxs-lookup"><span data-stu-id="873cb-124">**DRIVER\_INFO\_3**</span></span>](driver-info-3.md)<br/> |
| <span id="4"></span><dl> <span data-ttu-id="873cb-125"><dt>**четырех**</dt></span><span class="sxs-lookup"><span data-stu-id="873cb-125"><dt>**4**</dt></span></span> </dl> | [<span data-ttu-id="873cb-126">**\_Сведения о драйвере \_ 4**</span><span class="sxs-lookup"><span data-stu-id="873cb-126">**DRIVER\_INFO\_4**</span></span>](driver-info-4.md)<br/> |
| <span id="5"></span><dl> <span data-ttu-id="873cb-127"><dt>**5.0**</dt></span><span class="sxs-lookup"><span data-stu-id="873cb-127"><dt>**5**</dt></span></span> </dl> | [<span data-ttu-id="873cb-128">**\_Сведения о драйвере \_ 5**</span><span class="sxs-lookup"><span data-stu-id="873cb-128">**DRIVER\_INFO\_5**</span></span>](driver-info-5.md)<br/> |
| <span id="6"></span><dl> <span data-ttu-id="873cb-129"><dt>**6**</dt></span><span class="sxs-lookup"><span data-stu-id="873cb-129"><dt>**6**</dt></span></span> </dl> | [<span data-ttu-id="873cb-130">**\_Сведения о драйвере \_ 6**</span><span class="sxs-lookup"><span data-stu-id="873cb-130">**DRIVER\_INFO\_6**</span></span>](driver-info-6.md)<br/> |
| <span id="8"></span><dl> <span data-ttu-id="873cb-131"><dt>**8**</dt></span><span class="sxs-lookup"><span data-stu-id="873cb-131"><dt>**8**</dt></span></span> </dl> | [<span data-ttu-id="873cb-132">**\_Сведения о драйвере \_ 8**</span><span class="sxs-lookup"><span data-stu-id="873cb-132">**DRIVER\_INFO\_8**</span></span>](driver-info-8.md)<br/> |



 

</dd> <dt>

<span data-ttu-id="873cb-133">*пдриверинфо* \[ заполняет\]</span><span class="sxs-lookup"><span data-stu-id="873cb-133">*pDriverInfo* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="873cb-134">Указатель на буфер, который получает массив \_ структур сведений драйвера \_ \* , как указано в *уровне*.</span><span class="sxs-lookup"><span data-stu-id="873cb-134">A pointer to a buffer that receives an array of DRIVER\_INFO\_\* structures, as specified by *Level*.</span></span> <span data-ttu-id="873cb-135">Каждая структура содержит данные, описывающие доступный драйвер принтера.</span><span class="sxs-lookup"><span data-stu-id="873cb-135">Each structure contains data that describes an available printer driver.</span></span> <span data-ttu-id="873cb-136">Буфер должен быть достаточно большим, чтобы получать массив структур и любые строки или другие данные, к которым она указывает.</span><span class="sxs-lookup"><span data-stu-id="873cb-136">The buffer must be large enough to receive the array of structures and any strings or other data to which the structure members point.</span></span>

<span data-ttu-id="873cb-137">Чтобы определить требуемый размер буфера, вызовите **енумпринтердриверс** с параметром *кббуф* , присвойте ему значение 0.</span><span class="sxs-lookup"><span data-stu-id="873cb-137">To determine the required buffer size, call **EnumPrinterDrivers** with *cbBuf* set to zero.</span></span> <span data-ttu-id="873cb-138">**Енумпринтердриверс** завершается ошибкой, [**GetLastError**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror) возвращает ошибку, \_ недостаточную \_ для буфера, а параметр *пкбнидед* возвращает размер (в байтах) буфера, необходимого для хранения массива структур и их данных.</span><span class="sxs-lookup"><span data-stu-id="873cb-138">**EnumPrinterDrivers** fails, [**GetLastError**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror) returns ERROR\_INSUFFICIENT\_BUFFER, and the *pcbNeeded* parameter returns the size, in bytes, of the buffer required to hold the array of structures and their data.</span></span>

</dd> <dt>

<span data-ttu-id="873cb-139">*кббуф* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="873cb-139">*cbBuf* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="873cb-140">Размер (в байтах) буфера, на который указывает *пдриверинфо*</span><span class="sxs-lookup"><span data-stu-id="873cb-140">The size, in bytes, of the buffer pointed to by *pDriverInfo*</span></span>

</dd> <dt>

<span data-ttu-id="873cb-141">*пкбнидед* \[ заполняет\]</span><span class="sxs-lookup"><span data-stu-id="873cb-141">*pcbNeeded* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="873cb-142">Указатель на переменную, которая получает число байтов, скопированных в буфер *пдриверинфо* , если функция выполнена.</span><span class="sxs-lookup"><span data-stu-id="873cb-142">A pointer to a variable that receives the number of bytes copied to the *pDriverInfo* buffer if the function succeeds.</span></span> <span data-ttu-id="873cb-143">Если буфер слишком мал, функция завершается ошибкой и переменная получает необходимое количество байтов.</span><span class="sxs-lookup"><span data-stu-id="873cb-143">If the buffer is too small, the function fails and the variable receives the number of bytes required.</span></span>

</dd> <dt>

<span data-ttu-id="873cb-144">*пкретурнед* \[ заполняет\]</span><span class="sxs-lookup"><span data-stu-id="873cb-144">*pcReturned* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="873cb-145">Указатель на переменную, которая получает количество структур, возвращенных в буфере *пдриверинфо* .</span><span class="sxs-lookup"><span data-stu-id="873cb-145">A pointer to a variable that receives the number of structures returned in the *pDriverInfo* buffer.</span></span> <span data-ttu-id="873cb-146">Число драйверов принтера, установленных на указанном сервере печати.</span><span class="sxs-lookup"><span data-stu-id="873cb-146">This is the number of printer drivers installed on the specified print server.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="873cb-147">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="873cb-147">Return value</span></span>

<span data-ttu-id="873cb-148">Если функция выполнена, возвращаемое значение будет ненулевым.</span><span class="sxs-lookup"><span data-stu-id="873cb-148">If the function succeeds, the return value is a nonzero value.</span></span>

<span data-ttu-id="873cb-149">Если функция выполняется неудачно, возвращается нулевое значение.</span><span class="sxs-lookup"><span data-stu-id="873cb-149">If the function fails, the return value is zero.</span></span>

## <a name="remarks"></a><span data-ttu-id="873cb-150">Комментарии</span><span class="sxs-lookup"><span data-stu-id="873cb-150">Remarks</span></span>

> [!Note]  
> <span data-ttu-id="873cb-151">Это блокирующая или синхронная функция, которая может не возвращать значение немедленно.</span><span class="sxs-lookup"><span data-stu-id="873cb-151">This is a blocking or synchronous function and might not return immediately.</span></span> <span data-ttu-id="873cb-152">Скорость возврата этой функцией зависит от факторов времени выполнения, таких как состояние сети, Конфигурация сервера печати и факторы реализации драйвера принтера, которые трудно предсказать при написании приложения.</span><span class="sxs-lookup"><span data-stu-id="873cb-152">How quickly this function returns depends on run-time factors such as network status, print server configuration, and printer driver implementation factors that are difficult to predict when writing an application.</span></span> <span data-ttu-id="873cb-153">Вызов этой функции из потока, который управляет взаимодействием с пользовательским интерфейсом, может привести к невозможности реагирования приложения.</span><span class="sxs-lookup"><span data-stu-id="873cb-153">Calling this function from a thread that manages interaction with the user interface could make the application appear to be unresponsive.</span></span>

 

## <a name="requirements"></a><span data-ttu-id="873cb-154">Требования</span><span class="sxs-lookup"><span data-stu-id="873cb-154">Requirements</span></span>



| <span data-ttu-id="873cb-155">Требование</span><span class="sxs-lookup"><span data-stu-id="873cb-155">Requirement</span></span> | <span data-ttu-id="873cb-156">Значение</span><span class="sxs-lookup"><span data-stu-id="873cb-156">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="873cb-157">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="873cb-157">Minimum supported client</span></span><br/> | <span data-ttu-id="873cb-158">Windows 2000 Professional \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="873cb-158">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                                |
| <span data-ttu-id="873cb-159">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="873cb-159">Minimum supported server</span></span><br/> | <span data-ttu-id="873cb-160">Windows 2000 Server \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="873cb-160">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                      |
| <span data-ttu-id="873cb-161">Заголовок</span><span class="sxs-lookup"><span data-stu-id="873cb-161">Header</span></span><br/>                   | <dl> <span data-ttu-id="873cb-162"><dt>Винспул. h (включение Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="873cb-162"><dt>Winspool.h (include Windows.h)</dt></span></span> </dl> |
| <span data-ttu-id="873cb-163">Библиотека</span><span class="sxs-lookup"><span data-stu-id="873cb-163">Library</span></span><br/>                  | <dl> <span data-ttu-id="873cb-164"><dt>Винспул. lib</dt></span><span class="sxs-lookup"><span data-stu-id="873cb-164"><dt>Winspool.lib</dt></span></span> </dl>                   |
| <span data-ttu-id="873cb-165">DLL</span><span class="sxs-lookup"><span data-stu-id="873cb-165">DLL</span></span><br/>                      | <dl> <span data-ttu-id="873cb-166"><dt>Винспул. drv</dt></span><span class="sxs-lookup"><span data-stu-id="873cb-166"><dt>Winspool.drv</dt></span></span> </dl>                   |
| <span data-ttu-id="873cb-167">Имя в кодировке Юникод и ANSI</span><span class="sxs-lookup"><span data-stu-id="873cb-167">Unicode and ANSI names</span></span><br/>   | <span data-ttu-id="873cb-168">**Енумпринтердриверсв** (Юникод) и **енумпринтердриверса** (ANSI)</span><span class="sxs-lookup"><span data-stu-id="873cb-168">**EnumPrinterDriversW** (Unicode) and **EnumPrinterDriversA** (ANSI)</span></span><br/>                           |



## <a name="see-also"></a><span data-ttu-id="873cb-169">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="873cb-169">See also</span></span>

<dl> <dt>

[<span data-ttu-id="873cb-170">Вывод на печать</span><span class="sxs-lookup"><span data-stu-id="873cb-170">Printing</span></span>](printdocs-printing.md)
</dt> <dt>

[<span data-ttu-id="873cb-171">Функции API очереди печати принтера</span><span class="sxs-lookup"><span data-stu-id="873cb-171">Print Spooler API Functions</span></span>](printing-and-print-spooler-functions.md)
</dt> <dt>

[<span data-ttu-id="873cb-172">**аддпринтердривер**</span><span class="sxs-lookup"><span data-stu-id="873cb-172">**AddPrinterDriver**</span></span>](addprinterdriver.md)
</dt> <dt>

[<span data-ttu-id="873cb-173">**\_Сведения о драйвере \_ 1**</span><span class="sxs-lookup"><span data-stu-id="873cb-173">**DRIVER\_INFO\_1**</span></span>](driver-info-1.md)
</dt> <dt>

[<span data-ttu-id="873cb-174">**\_Сведения о драйвере \_ 2**</span><span class="sxs-lookup"><span data-stu-id="873cb-174">**DRIVER\_INFO\_2**</span></span>](driver-info-2.md)
</dt> <dt>

[<span data-ttu-id="873cb-175">**\_Сведения о драйвере \_ 3**</span><span class="sxs-lookup"><span data-stu-id="873cb-175">**DRIVER\_INFO\_3**</span></span>](driver-info-3.md)
</dt> <dt>

[<span data-ttu-id="873cb-176">**\_Сведения о драйвере \_ 4**</span><span class="sxs-lookup"><span data-stu-id="873cb-176">**DRIVER\_INFO\_4**</span></span>](driver-info-4.md)
</dt> <dt>

[<span data-ttu-id="873cb-177">**\_Сведения о драйвере \_ 5**</span><span class="sxs-lookup"><span data-stu-id="873cb-177">**DRIVER\_INFO\_5**</span></span>](driver-info-5.md)
</dt> <dt>

[<span data-ttu-id="873cb-178">**\_Сведения о драйвере \_ 6**</span><span class="sxs-lookup"><span data-stu-id="873cb-178">**DRIVER\_INFO\_6**</span></span>](driver-info-6.md)
</dt> <dt>

[<span data-ttu-id="873cb-179">**жетпринтердривер**</span><span class="sxs-lookup"><span data-stu-id="873cb-179">**GetPrinterDriver**</span></span>](getprinterdriver.md)
</dt> </dl>

 

