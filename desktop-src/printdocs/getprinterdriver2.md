---
description: Функция GetPrinterDriver2 извлекает данные драйвера для указанного принтера. Если драйвер не установлен на локальном компьютере, GetPrinterDriver2 устанавливает его и отображает в указанном окне любой пользовательский интерфейс.
ms.assetid: 0d482d28-7668-4734-ba71-5b355c18ddec
title: Функция GetPrinterDriver2 (Винспул. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- GetPrinterDriver2
- GetPrinterDriver2W
api_type:
- DllExport
api_location:
- Winspool.drv
ms.openlocfilehash: b0a9d2bfe7827a2c0e3db9fff9e8249b73bf5102
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "104272490"
---
# <a name="getprinterdriver2-function"></a><span data-ttu-id="390d8-104">Функция GetPrinterDriver2</span><span class="sxs-lookup"><span data-stu-id="390d8-104">GetPrinterDriver2 function</span></span>

<span data-ttu-id="390d8-105">Функция **GetPrinterDriver2** извлекает данные драйвера для указанного принтера.</span><span class="sxs-lookup"><span data-stu-id="390d8-105">The **GetPrinterDriver2** function retrieves driver data for the specified printer.</span></span> <span data-ttu-id="390d8-106">Если драйвер не установлен на локальном компьютере, **GetPrinterDriver2** устанавливает его и отображает в указанном окне любой пользовательский интерфейс.</span><span class="sxs-lookup"><span data-stu-id="390d8-106">If the driver is not installed on the local computer, **GetPrinterDriver2** installs it and displays any user interface to the specified window.</span></span>

## <a name="syntax"></a><span data-ttu-id="390d8-107">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="390d8-107">Syntax</span></span>


```C++
BOOL GetPrinterDriver2(
  _In_opt_ HWND    hWnd,
  _In_     HANDLE  hPrinter,
  _In_opt_ LPTSTR  pEnvironment,
  _In_     DWORD   Level,
  _Out_    LPBYTE  pDriverInfo,
  _In_     DWORD   cbBuf,
  _Out_    LPDWORD pcbNeeded
);
```



## <a name="parameters"></a><span data-ttu-id="390d8-108">Параметры</span><span class="sxs-lookup"><span data-stu-id="390d8-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="390d8-109">*HWND* \[ в необязательное\]</span><span class="sxs-lookup"><span data-stu-id="390d8-109">*hWnd* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="390d8-110">Маркер окна, который будет использоваться в качестве родительского окна любого пользовательского интерфейса, такого как диалоговое окно, которое драйвер отображает во время установки.</span><span class="sxs-lookup"><span data-stu-id="390d8-110">A handle of the window that will be used as the parent window of any user interface, such as a dialog box, that the driver displays during installation.</span></span> <span data-ttu-id="390d8-111">Если значение этого параметра равно **null**, Пользовательский интерфейс драйвера по-прежнему будет отображаться для пользователя во время установки, но не будет иметь родительского окна.</span><span class="sxs-lookup"><span data-stu-id="390d8-111">If the value of this parameter is **NULL**, the driver's user interface will still be displayed to the user during installation, but it will not have a parent window.</span></span>

</dd> <dt>

<span data-ttu-id="390d8-112">*хпринтер* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="390d8-112">*hPrinter* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="390d8-113">Описатель принтера, для которого должны быть получены данные драйвера.</span><span class="sxs-lookup"><span data-stu-id="390d8-113">A handle to the printer for which the driver data should be retrieved.</span></span> <span data-ttu-id="390d8-114">Используйте функцию [**опенпринтер**](openprinter.md) или [**аддпринтер**](addprinter.md) для получения маркера принтера.</span><span class="sxs-lookup"><span data-stu-id="390d8-114">Use the [**OpenPrinter**](openprinter.md) or [**AddPrinter**](addprinter.md) function to retrieve a printer handle.</span></span>

</dd> <dt>

<span data-ttu-id="390d8-115">*пенвиронмент* \[ в необязательное\]</span><span class="sxs-lookup"><span data-stu-id="390d8-115">*pEnvironment* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="390d8-116">Указатель на строку, завершающуюся нулем, которая указывает среду (например, Windows x86, Windows IA64 или Windows x64).</span><span class="sxs-lookup"><span data-stu-id="390d8-116">A pointer to a null-terminated string that specifies the environment (for example, Windows x86, Windows IA64, or Windows x64).</span></span> <span data-ttu-id="390d8-117">Если этот параметр имеет **значение NULL**, используется текущая среда вызывающего приложения и клиентского компьютера (не целевого приложения и сервера печати).</span><span class="sxs-lookup"><span data-stu-id="390d8-117">If this parameter is **NULL**, the current environment of the calling application and client machine (not of the destination application and print server) is used.</span></span>

</dd> <dt>

<span data-ttu-id="390d8-118">*Уровень* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="390d8-118">*Level* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="390d8-119">Структура драйвера принтера, возвращаемая в буфере *пдриверинфо* .</span><span class="sxs-lookup"><span data-stu-id="390d8-119">The printer driver structure returned in the *pDriverInfo* buffer.</span></span> <span data-ttu-id="390d8-120">Этот параметр может принимать одно из указанных ниже значений.</span><span class="sxs-lookup"><span data-stu-id="390d8-120">This parameter can be one of the following values.</span></span>



| <span data-ttu-id="390d8-121">Значение</span><span class="sxs-lookup"><span data-stu-id="390d8-121">Value</span></span>                                                                                                | <span data-ttu-id="390d8-122">Значение</span><span class="sxs-lookup"><span data-stu-id="390d8-122">Meaning</span></span>                                             |
|------------------------------------------------------------------------------------------------------|-----------------------------------------------------|
| <span id="1"></span><dl> <span data-ttu-id="390d8-123"><dt>**1**</dt></span><span class="sxs-lookup"><span data-stu-id="390d8-123"><dt>**1**</dt></span></span> </dl> | [<span data-ttu-id="390d8-124">**\_Сведения о драйвере \_ 1**</span><span class="sxs-lookup"><span data-stu-id="390d8-124">**DRIVER\_INFO\_1**</span></span>](driver-info-1.md)<br/> |
| <span id="2"></span><dl> <span data-ttu-id="390d8-125"><dt>**2**</dt></span><span class="sxs-lookup"><span data-stu-id="390d8-125"><dt>**2**</dt></span></span> </dl> | [<span data-ttu-id="390d8-126">**\_Сведения о драйвере \_ 2**</span><span class="sxs-lookup"><span data-stu-id="390d8-126">**DRIVER\_INFO\_2**</span></span>](driver-info-2.md)<br/> |
| <span id="3"></span><dl> <span data-ttu-id="390d8-127"><dt>**3-5**</dt></span><span class="sxs-lookup"><span data-stu-id="390d8-127"><dt>**3**</dt></span></span> </dl> | [<span data-ttu-id="390d8-128">**\_Сведения о драйвере \_ 3**</span><span class="sxs-lookup"><span data-stu-id="390d8-128">**DRIVER\_INFO\_3**</span></span>](driver-info-3.md)<br/> |
| <span id="4"></span><dl> <span data-ttu-id="390d8-129"><dt>**четырех**</dt></span><span class="sxs-lookup"><span data-stu-id="390d8-129"><dt>**4**</dt></span></span> </dl> | [<span data-ttu-id="390d8-130">**\_Сведения о драйвере \_ 4**</span><span class="sxs-lookup"><span data-stu-id="390d8-130">**DRIVER\_INFO\_4**</span></span>](driver-info-4.md)<br/> |
| <span id="5"></span><dl> <span data-ttu-id="390d8-131"><dt>**5.0**</dt></span><span class="sxs-lookup"><span data-stu-id="390d8-131"><dt>**5**</dt></span></span> </dl> | [<span data-ttu-id="390d8-132">**\_Сведения о драйвере \_ 5**</span><span class="sxs-lookup"><span data-stu-id="390d8-132">**DRIVER\_INFO\_5**</span></span>](driver-info-5.md)<br/> |
| <span id="6"></span><dl> <span data-ttu-id="390d8-133"><dt>**6**</dt></span><span class="sxs-lookup"><span data-stu-id="390d8-133"><dt>**6**</dt></span></span> </dl> | [<span data-ttu-id="390d8-134">**\_Сведения о драйвере \_ 6**</span><span class="sxs-lookup"><span data-stu-id="390d8-134">**DRIVER\_INFO\_6**</span></span>](driver-info-6.md)<br/> |
| <span id="8"></span><dl> <span data-ttu-id="390d8-135"><dt>**8**</dt></span><span class="sxs-lookup"><span data-stu-id="390d8-135"><dt>**8**</dt></span></span> </dl> | [<span data-ttu-id="390d8-136">**\_Сведения о драйвере \_ 8**</span><span class="sxs-lookup"><span data-stu-id="390d8-136">**DRIVER\_INFO\_8**</span></span>](driver-info-8.md)<br/> |



 

</dd> <dt>

<span data-ttu-id="390d8-137">*пдриверинфо* \[ заполняет\]</span><span class="sxs-lookup"><span data-stu-id="390d8-137">*pDriverInfo* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="390d8-138">Указатель на буфер, который получает структуру, содержащую сведения о драйвере, как указано в параметре *Level*.</span><span class="sxs-lookup"><span data-stu-id="390d8-138">A pointer to a buffer that receives a structure containing information about the driver, as specified by *Level*.</span></span> <span data-ttu-id="390d8-139">Буфер должен быть достаточно большим, чтобы хранить строки, на которые указывает члены структуры.</span><span class="sxs-lookup"><span data-stu-id="390d8-139">The buffer must be large enough to store the strings pointed to by the structure members.</span></span>

<span data-ttu-id="390d8-140">Чтобы определить требуемый размер буфера, вызовите **GetPrinterDriver2** с параметром *кббуф* , присвойте ему значение 0.</span><span class="sxs-lookup"><span data-stu-id="390d8-140">To determine the required buffer size, call **GetPrinterDriver2** with *cbBuf* set to zero.</span></span> <span data-ttu-id="390d8-141">**GetPrinterDriver2** завершается ошибкой, [**GetLastError**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror) возвращает **ошибку, \_ недостаточную для \_ буфера**, а параметр *пкбнидед* возвращает размер (в байтах) буфера, необходимого для хранения массива структур и их данных.</span><span class="sxs-lookup"><span data-stu-id="390d8-141">**GetPrinterDriver2** fails, [**GetLastError**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror) returns **ERROR\_INSUFFICIENT\_BUFFER**, and the *pcbNeeded* parameter returns the size, in bytes, of the buffer required to hold the array of structures and their data.</span></span>

</dd> <dt>

<span data-ttu-id="390d8-142">*кббуф* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="390d8-142">*cbBuf* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="390d8-143">Размер (в байтах) массива, на который указывает *пдриверинфо* .</span><span class="sxs-lookup"><span data-stu-id="390d8-143">The size, in bytes, of the array at which *pDriverInfo* points.</span></span>

</dd> <dt>

<span data-ttu-id="390d8-144">*пкбнидед* \[ заполняет\]</span><span class="sxs-lookup"><span data-stu-id="390d8-144">*pcbNeeded* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="390d8-145">Указатель на значение, которое получает число байтов, скопированных, если функция выполнена, или число байтов, необходимое, если *кббуф* слишком мал.</span><span class="sxs-lookup"><span data-stu-id="390d8-145">A pointer to a value that receives the number of bytes copied if the function succeeds or the number of bytes required if *cbBuf* is too small.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="390d8-146">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="390d8-146">Return value</span></span>

<span data-ttu-id="390d8-147">Если функция выполнена, возвращаемое значение будет ненулевым.</span><span class="sxs-lookup"><span data-stu-id="390d8-147">If the function succeeds, the return value is a nonzero value.</span></span>

<span data-ttu-id="390d8-148">Если функция выполняется неудачно, возвращается нулевое значение.</span><span class="sxs-lookup"><span data-stu-id="390d8-148">If the function fails, the return value is zero.</span></span> <span data-ttu-id="390d8-149">Чтобы получить состояние возврата, вызовите [**GetLastError**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror).</span><span class="sxs-lookup"><span data-stu-id="390d8-149">To get the return status, call [**GetLastError**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror).</span></span>

## <a name="remarks"></a><span data-ttu-id="390d8-150">Комментарии</span><span class="sxs-lookup"><span data-stu-id="390d8-150">Remarks</span></span>

<span data-ttu-id="390d8-151">В [**\_ сведениях драйвера \_ 2**](driver-info-2.md), [**\_ сведения о драйвере \_ 3**](driver-info-3.md), [**\_ сведения о драйвере \_ 4**](driver-info-4.md), [**\_ сведения о драйвере \_ 5**](driver-info-5.md), сведения о драйвере [**\_ \_ 6**](driver-info-6.md)и сведения о драйвере [**\_ \_ 8**](driver-info-8.md) содержатся имя файла или полный путь и имя файла драйвера принтера в элементе **пдриверпас** .</span><span class="sxs-lookup"><span data-stu-id="390d8-151">The [**DRIVER\_INFO\_2**](driver-info-2.md), [**DRIVER\_INFO\_3**](driver-info-3.md), [**DRIVER\_INFO\_4**](driver-info-4.md), [**DRIVER\_INFO\_5**](driver-info-5.md), [**DRIVER\_INFO\_6**](driver-info-6.md), and [**DRIVER\_INFO\_8**](driver-info-8.md) structures contain the file name or the full path and file name of the printer driver in the **pDriverPath** member.</span></span> <span data-ttu-id="390d8-152">Приложение может использовать путь и имя файла для загрузки драйвера принтера, вызвав функцию [**LoadLibrary**](/windows/desktop/api/libloaderapi/nf-libloaderapi-loadlibrarya) и указав путь и имя файла в качестве одного аргумента.</span><span class="sxs-lookup"><span data-stu-id="390d8-152">An application can use the path and file name to load a printer driver by calling the [**LoadLibrary**](/windows/desktop/api/libloaderapi/nf-libloaderapi-loadlibrarya) function and supplying the path and file name as the single argument.</span></span>

<span data-ttu-id="390d8-153">Версия ANSI этой функции, **GetPrinterDriver2A** , не поддерживается и возвращает **ошибку \_ не \_ поддерживается**.</span><span class="sxs-lookup"><span data-stu-id="390d8-153">The ANSI version of this function, **GetPrinterDriver2A** is not supported and returns **ERROR\_NOT\_SUPPORTED**.</span></span>

## <a name="requirements"></a><span data-ttu-id="390d8-154">Требования</span><span class="sxs-lookup"><span data-stu-id="390d8-154">Requirements</span></span>



| <span data-ttu-id="390d8-155">Требование</span><span class="sxs-lookup"><span data-stu-id="390d8-155">Requirement</span></span> | <span data-ttu-id="390d8-156">Значение</span><span class="sxs-lookup"><span data-stu-id="390d8-156">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="390d8-157">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="390d8-157">Minimum supported client</span></span><br/> | <span data-ttu-id="390d8-158">Только для \[ классических приложений Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="390d8-158">Windows Vista \[desktop apps only\]</span></span><br/>                                                            |
| <span data-ttu-id="390d8-159">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="390d8-159">Minimum supported server</span></span><br/> | <span data-ttu-id="390d8-160">\[Только для настольных приложений Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="390d8-160">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                                      |
| <span data-ttu-id="390d8-161">Header</span><span class="sxs-lookup"><span data-stu-id="390d8-161">Header</span></span><br/>                   | <dl> <span data-ttu-id="390d8-162"><dt>Винспул. h (включение Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="390d8-162"><dt>Winspool.h (include Windows.h)</dt></span></span> </dl> |
| <span data-ttu-id="390d8-163">Библиотека</span><span class="sxs-lookup"><span data-stu-id="390d8-163">Library</span></span><br/>                  | <dl> <span data-ttu-id="390d8-164"><dt>Винспул. lib</dt></span><span class="sxs-lookup"><span data-stu-id="390d8-164"><dt>Winspool.lib</dt></span></span> </dl>                   |
| <span data-ttu-id="390d8-165">DLL</span><span class="sxs-lookup"><span data-stu-id="390d8-165">DLL</span></span><br/>                      | <dl> <span data-ttu-id="390d8-166"><dt>Винспул. drv</dt></span><span class="sxs-lookup"><span data-stu-id="390d8-166"><dt>Winspool.drv</dt></span></span> </dl>                   |
| <span data-ttu-id="390d8-167">Имя в кодировке Юникод и ANSI</span><span class="sxs-lookup"><span data-stu-id="390d8-167">Unicode and ANSI names</span></span><br/>   | <span data-ttu-id="390d8-168">**GetPrinterDriver2W** (Юникод)</span><span class="sxs-lookup"><span data-stu-id="390d8-168">**GetPrinterDriver2W** (Unicode)</span></span><br/>                                                               |



## <a name="see-also"></a><span data-ttu-id="390d8-169">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="390d8-169">See also</span></span>

<dl> <dt>

[<span data-ttu-id="390d8-170">Вывод на печать</span><span class="sxs-lookup"><span data-stu-id="390d8-170">Printing</span></span>](printdocs-printing.md)
</dt> <dt>

[<span data-ttu-id="390d8-171">Функции API очереди печати принтера</span><span class="sxs-lookup"><span data-stu-id="390d8-171">Print Spooler API Functions</span></span>](printing-and-print-spooler-functions.md)
</dt> <dt>

[<span data-ttu-id="390d8-172">**аддпринтердривер**</span><span class="sxs-lookup"><span data-stu-id="390d8-172">**AddPrinterDriver**</span></span>](addprinterdriver.md)
</dt> <dt>

[<span data-ttu-id="390d8-173">**\_Сведения о драйвере \_ 1**</span><span class="sxs-lookup"><span data-stu-id="390d8-173">**DRIVER\_INFO\_1**</span></span>](driver-info-1.md)
</dt> <dt>

[<span data-ttu-id="390d8-174">**\_Сведения о драйвере \_ 2**</span><span class="sxs-lookup"><span data-stu-id="390d8-174">**DRIVER\_INFO\_2**</span></span>](driver-info-2.md)
</dt> <dt>

[<span data-ttu-id="390d8-175">**\_Сведения о драйвере \_ 3**</span><span class="sxs-lookup"><span data-stu-id="390d8-175">**DRIVER\_INFO\_3**</span></span>](driver-info-3.md)
</dt> <dt>

[<span data-ttu-id="390d8-176">**\_Сведения о драйвере \_ 4**</span><span class="sxs-lookup"><span data-stu-id="390d8-176">**DRIVER\_INFO\_4**</span></span>](driver-info-4.md)
</dt> <dt>

[<span data-ttu-id="390d8-177">**\_Сведения о драйвере \_ 5**</span><span class="sxs-lookup"><span data-stu-id="390d8-177">**DRIVER\_INFO\_5**</span></span>](driver-info-5.md)
</dt> <dt>

[<span data-ttu-id="390d8-178">**\_Сведения о драйвере \_ 6**</span><span class="sxs-lookup"><span data-stu-id="390d8-178">**DRIVER\_INFO\_6**</span></span>](driver-info-6.md)
</dt> <dt>

[<span data-ttu-id="390d8-179">**енумпринтердриверс**</span><span class="sxs-lookup"><span data-stu-id="390d8-179">**EnumPrinterDrivers**</span></span>](enumprinterdrivers.md)
</dt> <dt>

[<span data-ttu-id="390d8-180">**жетпринтердривер**</span><span class="sxs-lookup"><span data-stu-id="390d8-180">**GetPrinterDriver**</span></span>](getprinterdriver.md)
</dt> <dt>

[<span data-ttu-id="390d8-181">**опенпринтер**</span><span class="sxs-lookup"><span data-stu-id="390d8-181">**OpenPrinter**</span></span>](openprinter.md)
</dt> </dl>

 

