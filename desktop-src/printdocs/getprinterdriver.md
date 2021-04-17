---
description: Функция Жетпринтердривер извлекает данные драйвера для указанного принтера. Если драйвер не установлен на локальном компьютере, Жетпринтердривер устанавливает его.
ms.assetid: 93f859b4-1005-4359-8029-9536d6eeb7e7
title: Функция Жетпринтердривер (Винспул. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- GetPrinterDriver
- GetPrinterDriverA
- GetPrinterDriverW
api_type:
- DllExport
api_location:
- Winspool.drv
- Ext-MS-Win-Printer-WinSpool-l1-1-2.dll
- Ext-MS-Win-Printer-WinSpool-L1-1-3.dll
ms.openlocfilehash: a67a77a8167bf207231d2f3f6f063ed7636e201f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "105703137"
---
# <a name="getprinterdriver-function"></a><span data-ttu-id="8f193-104">Функция Жетпринтердривер</span><span class="sxs-lookup"><span data-stu-id="8f193-104">GetPrinterDriver function</span></span>

<span data-ttu-id="8f193-105">Функция **жетпринтердривер** извлекает данные драйвера для указанного принтера.</span><span class="sxs-lookup"><span data-stu-id="8f193-105">The **GetPrinterDriver** function retrieves driver data for the specified printer.</span></span> <span data-ttu-id="8f193-106">Если драйвер не установлен на локальном компьютере, **жетпринтердривер** устанавливает его.</span><span class="sxs-lookup"><span data-stu-id="8f193-106">If the driver is not installed on the local computer, **GetPrinterDriver** installs it.</span></span>

## <a name="syntax"></a><span data-ttu-id="8f193-107">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="8f193-107">Syntax</span></span>


```C++
BOOL GetPrinterDriver(
  _In_  HANDLE  hPrinter,
  _In_  LPTSTR  pEnvironment,
  _In_  DWORD   Level,
  _Out_ LPBYTE  pDriverInfo,
  _In_  DWORD   cbBuf,
  _Out_ LPDWORD pcbNeeded
);
```



## <a name="parameters"></a><span data-ttu-id="8f193-108">Параметры</span><span class="sxs-lookup"><span data-stu-id="8f193-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="8f193-109">*хпринтер* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="8f193-109">*hPrinter* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="8f193-110">Описатель принтера, для которого должны быть получены данные драйвера.</span><span class="sxs-lookup"><span data-stu-id="8f193-110">A handle to the printer for which the driver data should be retrieved.</span></span> <span data-ttu-id="8f193-111">Используйте функцию [**опенпринтер**](openprinter.md) или [**аддпринтер**](addprinter.md) для получения маркера принтера.</span><span class="sxs-lookup"><span data-stu-id="8f193-111">Use the [**OpenPrinter**](openprinter.md) or [**AddPrinter**](addprinter.md) function to retrieve a printer handle.</span></span>

</dd> <dt>

<span data-ttu-id="8f193-112">*пенвиронмент* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="8f193-112">*pEnvironment* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="8f193-113">Указатель на строку, завершающуюся нулем, которая указывает среду (например, Windows x86, Windows IA64 или Windows x64).</span><span class="sxs-lookup"><span data-stu-id="8f193-113">A pointer to a null-terminated string that specifies the environment (for example, Windows x86, Windows IA64, or Windows x64).</span></span> <span data-ttu-id="8f193-114">Если этот параметр имеет **значение NULL**, используется текущая среда вызывающего приложения и клиентского компьютера (не целевого приложения и сервера печати).</span><span class="sxs-lookup"><span data-stu-id="8f193-114">If this parameter is **NULL**, the current environment of the calling application and client machine (not of the destination application and print server) is used.</span></span>

</dd> <dt>

<span data-ttu-id="8f193-115">*Уровень* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="8f193-115">*Level* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="8f193-116">Структура драйвера принтера, возвращаемая в буфере *пдриверинфо* .</span><span class="sxs-lookup"><span data-stu-id="8f193-116">The printer driver structure returned in the *pDriverInfo* buffer.</span></span> <span data-ttu-id="8f193-117">Этот параметр может принимать одно из указанных ниже значений.</span><span class="sxs-lookup"><span data-stu-id="8f193-117">This parameter can be one of the following values.</span></span>



| <span data-ttu-id="8f193-118">Значение</span><span class="sxs-lookup"><span data-stu-id="8f193-118">Value</span></span>                                                                                                | <span data-ttu-id="8f193-119">Значение</span><span class="sxs-lookup"><span data-stu-id="8f193-119">Meaning</span></span>                                             |
|------------------------------------------------------------------------------------------------------|-----------------------------------------------------|
| <span id="1"></span><dl> <span data-ttu-id="8f193-120"><dt>**1**</dt></span><span class="sxs-lookup"><span data-stu-id="8f193-120"><dt>**1**</dt></span></span> </dl> | [<span data-ttu-id="8f193-121">**\_Сведения о драйвере \_ 1**</span><span class="sxs-lookup"><span data-stu-id="8f193-121">**DRIVER\_INFO\_1**</span></span>](driver-info-1.md)<br/> |
| <span id="2"></span><dl> <span data-ttu-id="8f193-122"><dt>**2**</dt></span><span class="sxs-lookup"><span data-stu-id="8f193-122"><dt>**2**</dt></span></span> </dl> | [<span data-ttu-id="8f193-123">**\_Сведения о драйвере \_ 2**</span><span class="sxs-lookup"><span data-stu-id="8f193-123">**DRIVER\_INFO\_2**</span></span>](driver-info-2.md)<br/> |
| <span id="3"></span><dl> <span data-ttu-id="8f193-124"><dt>**3-5**</dt></span><span class="sxs-lookup"><span data-stu-id="8f193-124"><dt>**3**</dt></span></span> </dl> | [<span data-ttu-id="8f193-125">**\_Сведения о драйвере \_ 3**</span><span class="sxs-lookup"><span data-stu-id="8f193-125">**DRIVER\_INFO\_3**</span></span>](driver-info-3.md)<br/> |
| <span id="4"></span><dl> <span data-ttu-id="8f193-126"><dt>**четырех**</dt></span><span class="sxs-lookup"><span data-stu-id="8f193-126"><dt>**4**</dt></span></span> </dl> | [<span data-ttu-id="8f193-127">**\_Сведения о драйвере \_ 4**</span><span class="sxs-lookup"><span data-stu-id="8f193-127">**DRIVER\_INFO\_4**</span></span>](driver-info-4.md)<br/> |
| <span id="5"></span><dl> <span data-ttu-id="8f193-128"><dt>**5.0**</dt></span><span class="sxs-lookup"><span data-stu-id="8f193-128"><dt>**5**</dt></span></span> </dl> | [<span data-ttu-id="8f193-129">**\_Сведения о драйвере \_ 5**</span><span class="sxs-lookup"><span data-stu-id="8f193-129">**DRIVER\_INFO\_5**</span></span>](driver-info-5.md)<br/> |
| <span id="6"></span><dl> <span data-ttu-id="8f193-130"><dt>**6**</dt></span><span class="sxs-lookup"><span data-stu-id="8f193-130"><dt>**6**</dt></span></span> </dl> | [<span data-ttu-id="8f193-131">**\_Сведения о драйвере \_ 6**</span><span class="sxs-lookup"><span data-stu-id="8f193-131">**DRIVER\_INFO\_6**</span></span>](driver-info-6.md)<br/> |
| <span id="8"></span><dl> <span data-ttu-id="8f193-132"><dt>**8**</dt></span><span class="sxs-lookup"><span data-stu-id="8f193-132"><dt>**8**</dt></span></span> </dl> | [<span data-ttu-id="8f193-133">**\_Сведения о драйвере \_ 8**</span><span class="sxs-lookup"><span data-stu-id="8f193-133">**DRIVER\_INFO\_8**</span></span>](driver-info-8.md)<br/> |



 

</dd> <dt>

<span data-ttu-id="8f193-134">*пдриверинфо* \[ заполняет\]</span><span class="sxs-lookup"><span data-stu-id="8f193-134">*pDriverInfo* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="8f193-135">Указатель на буфер, который получает структуру, содержащую сведения о драйвере, как указано в параметре Level.</span><span class="sxs-lookup"><span data-stu-id="8f193-135">A pointer to a buffer that receives a structure containing information about the driver, as specified by Level.</span></span> <span data-ttu-id="8f193-136">Буфер должен быть достаточно большим, чтобы хранить строки, на которые указывает члены структуры.</span><span class="sxs-lookup"><span data-stu-id="8f193-136">The buffer must be large enough to store the strings pointed to by the structure members.</span></span>

<span data-ttu-id="8f193-137">Чтобы определить требуемый размер буфера, вызовите **жетпринтердривер** с параметром *кббуф* , присвойте ему значение 0.</span><span class="sxs-lookup"><span data-stu-id="8f193-137">To determine the required buffer size, call **GetPrinterDriver** with *cbBuf* set to zero.</span></span> <span data-ttu-id="8f193-138">**Жетпринтердривер** завершается ошибкой, [**GetLastError**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror) возвращает ошибку, \_ недостаточную \_ для буфера, а параметр *пкбнидед* возвращает размер (в байтах) буфера, необходимого для хранения массива структур и их данных.</span><span class="sxs-lookup"><span data-stu-id="8f193-138">**GetPrinterDriver** fails, [**GetLastError**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror) returns ERROR\_INSUFFICIENT\_BUFFER, and the *pcbNeeded* parameter returns the size, in bytes, of the buffer required to hold the array of structures and their data.</span></span>

</dd> <dt>

<span data-ttu-id="8f193-139">*кббуф* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="8f193-139">*cbBuf* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="8f193-140">Размер (в байтах) массива, на который указывает *пдриверинфо* .</span><span class="sxs-lookup"><span data-stu-id="8f193-140">The size, in bytes, of the array at which *pDriverInfo* points.</span></span>

</dd> <dt>

<span data-ttu-id="8f193-141">*пкбнидед* \[ заполняет\]</span><span class="sxs-lookup"><span data-stu-id="8f193-141">*pcbNeeded* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="8f193-142">Указатель на значение, которое получает число байтов, скопированных, если функция выполнена, или число байтов, необходимое, если *кббуф* слишком мал.</span><span class="sxs-lookup"><span data-stu-id="8f193-142">A pointer to a value that receives the number of bytes copied if the function succeeds or the number of bytes required if *cbBuf* is too small.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="8f193-143">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="8f193-143">Return value</span></span>

<span data-ttu-id="8f193-144">Если функция выполнена, возвращаемое значение будет ненулевым.</span><span class="sxs-lookup"><span data-stu-id="8f193-144">If the function succeeds, the return value is a nonzero value.</span></span>

<span data-ttu-id="8f193-145">Если функция выполняется неудачно, возвращается нулевое значение.</span><span class="sxs-lookup"><span data-stu-id="8f193-145">If the function fails, the return value is zero.</span></span>

<span data-ttu-id="8f193-146">Для несуществующего драйвера функция возвращает ошибку \_ неизвестный \_ \_ драйвер принтера.</span><span class="sxs-lookup"><span data-stu-id="8f193-146">For a non-existent driver, the function returns ERROR\_UNKNOWN\_PRINTER\_DRIVER.</span></span>

## <a name="remarks"></a><span data-ttu-id="8f193-147">Комментарии</span><span class="sxs-lookup"><span data-stu-id="8f193-147">Remarks</span></span>

> [!Note]  
> <span data-ttu-id="8f193-148">Это блокирующая или синхронная функция, которая может не возвращать значение немедленно.</span><span class="sxs-lookup"><span data-stu-id="8f193-148">This is a blocking or synchronous function and might not return immediately.</span></span> <span data-ttu-id="8f193-149">Скорость возврата этой функцией зависит от факторов времени выполнения, таких как состояние сети, Конфигурация сервера печати и факторы реализации драйвера принтера, которые трудно предсказать при написании приложения.</span><span class="sxs-lookup"><span data-stu-id="8f193-149">How quickly this function returns depends on run-time factors such as network status, print server configuration, and printer driver implementation factors that are difficult to predict when writing an application.</span></span> <span data-ttu-id="8f193-150">Вызов этой функции из потока, который управляет взаимодействием с пользовательским интерфейсом, может привести к невозможности реагирования приложения.</span><span class="sxs-lookup"><span data-stu-id="8f193-150">Calling this function from a thread that manages interaction with the user interface could make the application appear to be unresponsive.</span></span>

 

<span data-ttu-id="8f193-151">Структуры [**драйвера \_ \_ 2**](driver-info-2.md), [**\_ сведения о \_**](driver-info-3.md)драйвере 3, [**\_ сведения о драйвере \_ 4**](driver-info-4.md), [**\_ сведения о драйвере \_ 5**](driver-info-5.md)и сведения о драйвере [**\_ \_ 6**](driver-info-6.md) содержат имя файла или полный путь и имя файла драйвера принтера в элементе **пдриверпас** .</span><span class="sxs-lookup"><span data-stu-id="8f193-151">The [**DRIVER\_INFO\_2**](driver-info-2.md), [**DRIVER\_INFO\_3**](driver-info-3.md), [**DRIVER\_INFO\_4**](driver-info-4.md), [**DRIVER\_INFO\_5**](driver-info-5.md), and [**DRIVER\_INFO\_6**](driver-info-6.md) structures contain the file name or the full path and file name of the printer driver in the **pDriverPath** member.</span></span> <span data-ttu-id="8f193-152">Приложение может использовать путь и имя файла для загрузки драйвера принтера, вызвав функцию [**LoadLibrary**](/windows/desktop/api/libloaderapi/nf-libloaderapi-loadlibrarya) и указав путь и имя файла в качестве одного аргумента.</span><span class="sxs-lookup"><span data-stu-id="8f193-152">An application can use the path and file name to load a printer driver by calling the [**LoadLibrary**](/windows/desktop/api/libloaderapi/nf-libloaderapi-loadlibrarya) function and supplying the path and file name as the single argument.</span></span>

## <a name="requirements"></a><span data-ttu-id="8f193-153">Требования</span><span class="sxs-lookup"><span data-stu-id="8f193-153">Requirements</span></span>



| <span data-ttu-id="8f193-154">Требование</span><span class="sxs-lookup"><span data-stu-id="8f193-154">Requirement</span></span> | <span data-ttu-id="8f193-155">Значение</span><span class="sxs-lookup"><span data-stu-id="8f193-155">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="8f193-156">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="8f193-156">Minimum supported client</span></span><br/> | <span data-ttu-id="8f193-157">Windows 2000 Professional \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="8f193-157">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                                |
| <span data-ttu-id="8f193-158">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="8f193-158">Minimum supported server</span></span><br/> | <span data-ttu-id="8f193-159">Windows 2000 Server \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="8f193-159">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                      |
| <span data-ttu-id="8f193-160">Заголовок</span><span class="sxs-lookup"><span data-stu-id="8f193-160">Header</span></span><br/>                   | <dl> <span data-ttu-id="8f193-161"><dt>Винспул. h (включение Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="8f193-161"><dt>Winspool.h (include Windows.h)</dt></span></span> </dl> |
| <span data-ttu-id="8f193-162">Библиотека</span><span class="sxs-lookup"><span data-stu-id="8f193-162">Library</span></span><br/>                  | <dl> <span data-ttu-id="8f193-163"><dt>Винспул. lib</dt></span><span class="sxs-lookup"><span data-stu-id="8f193-163"><dt>Winspool.lib</dt></span></span> </dl>                   |
| <span data-ttu-id="8f193-164">DLL</span><span class="sxs-lookup"><span data-stu-id="8f193-164">DLL</span></span><br/>                      | <dl> <span data-ttu-id="8f193-165"><dt>Винспул. drv</dt></span><span class="sxs-lookup"><span data-stu-id="8f193-165"><dt>Winspool.drv</dt></span></span> </dl>                   |
| <span data-ttu-id="8f193-166">Имя в кодировке Юникод и ANSI</span><span class="sxs-lookup"><span data-stu-id="8f193-166">Unicode and ANSI names</span></span><br/>   | <span data-ttu-id="8f193-167">**Жетпринтердриверв** (Юникод) и **жетпринтердривера** (ANSI)</span><span class="sxs-lookup"><span data-stu-id="8f193-167">**GetPrinterDriverW** (Unicode) and **GetPrinterDriverA** (ANSI)</span></span><br/>                               |



## <a name="see-also"></a><span data-ttu-id="8f193-168">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="8f193-168">See also</span></span>

<dl> <dt>

[<span data-ttu-id="8f193-169">Вывод на печать</span><span class="sxs-lookup"><span data-stu-id="8f193-169">Printing</span></span>](printdocs-printing.md)
</dt> <dt>

[<span data-ttu-id="8f193-170">Функции API очереди печати принтера</span><span class="sxs-lookup"><span data-stu-id="8f193-170">Print Spooler API Functions</span></span>](printing-and-print-spooler-functions.md)
</dt> <dt>

[<span data-ttu-id="8f193-171">**аддпринтердривер**</span><span class="sxs-lookup"><span data-stu-id="8f193-171">**AddPrinterDriver**</span></span>](addprinterdriver.md)
</dt> <dt>

[<span data-ttu-id="8f193-172">**\_Сведения о драйвере \_ 1**</span><span class="sxs-lookup"><span data-stu-id="8f193-172">**DRIVER\_INFO\_1**</span></span>](driver-info-1.md)
</dt> <dt>

[<span data-ttu-id="8f193-173">**\_Сведения о драйвере \_ 2**</span><span class="sxs-lookup"><span data-stu-id="8f193-173">**DRIVER\_INFO\_2**</span></span>](driver-info-2.md)
</dt> <dt>

[<span data-ttu-id="8f193-174">**\_Сведения о драйвере \_ 3**</span><span class="sxs-lookup"><span data-stu-id="8f193-174">**DRIVER\_INFO\_3**</span></span>](driver-info-3.md)
</dt> <dt>

[<span data-ttu-id="8f193-175">**\_Сведения о драйвере \_ 4**</span><span class="sxs-lookup"><span data-stu-id="8f193-175">**DRIVER\_INFO\_4**</span></span>](driver-info-4.md)
</dt> <dt>

[<span data-ttu-id="8f193-176">**\_Сведения о драйвере \_ 5**</span><span class="sxs-lookup"><span data-stu-id="8f193-176">**DRIVER\_INFO\_5**</span></span>](driver-info-5.md)
</dt> <dt>

[<span data-ttu-id="8f193-177">**\_Сведения о драйвере \_ 6**</span><span class="sxs-lookup"><span data-stu-id="8f193-177">**DRIVER\_INFO\_6**</span></span>](driver-info-6.md)
</dt> <dt>

[<span data-ttu-id="8f193-178">**енумпринтердриверс**</span><span class="sxs-lookup"><span data-stu-id="8f193-178">**EnumPrinterDrivers**</span></span>](enumprinterdrivers.md)
</dt> <dt>

[<span data-ttu-id="8f193-179">**опенпринтер**</span><span class="sxs-lookup"><span data-stu-id="8f193-179">**OpenPrinter**</span></span>](openprinter.md)
</dt> </dl>

 

