---
description: Функция Жетпринтердатаекс получает данные конфигурации для указанного принтера или сервера печати.
ms.assetid: 5d9183a7-97cc-46de-848e-e37ce51396eb
title: Функция Жетпринтердатаекс (Винспул. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- GetPrinterDataEx
- GetPrinterDataExA
- GetPrinterDataExW
api_type:
- DllExport
api_location:
- Winspool.drv
- Ext-MS-Win-printer-Winspool-l1-1-1.dll
- Ext-MS-Win-Printer-WinSpool-l1-1-2.dll
- Ext-MS-Win-Printer-WinSpool-L1-1-3.dll
ms.openlocfilehash: bdadf2e1259445ca5285e5b12bc906140a137cf9
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "103817905"
---
# <a name="getprinterdataex-function"></a><span data-ttu-id="cdd79-103">Функция Жетпринтердатаекс</span><span class="sxs-lookup"><span data-stu-id="cdd79-103">GetPrinterDataEx function</span></span>

<span data-ttu-id="cdd79-104">Функция **жетпринтердатаекс** получает данные конфигурации для указанного принтера или сервера печати.</span><span class="sxs-lookup"><span data-stu-id="cdd79-104">The **GetPrinterDataEx** function retrieves configuration data for the specified printer or print server.</span></span> <span data-ttu-id="cdd79-105">**Жетпринтердатаекс** может извлекать значения, хранимые в функции [**сетпринтердата**](setprinterdata.md) .</span><span class="sxs-lookup"><span data-stu-id="cdd79-105">**GetPrinterDataEx** can retrieve values that the [**SetPrinterData**](setprinterdata.md) function stored.</span></span> <span data-ttu-id="cdd79-106">Кроме того, **жетпринтердатаекс** может извлекать значения, хранимые в функции [**сетпринтердатаекс**](setprinterdataex.md) в указанном ключе.</span><span class="sxs-lookup"><span data-stu-id="cdd79-106">In addition, **GetPrinterDataEx** can retrieve values that the [**SetPrinterDataEx**](setprinterdataex.md) function stored under a specified key.</span></span>

## <a name="syntax"></a><span data-ttu-id="cdd79-107">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="cdd79-107">Syntax</span></span>


```C++
DWORD GetPrinterDataEx(
  _In_  HANDLE  hPrinter,
  _In_  LPCTSTR pKeyName,
  _In_  LPCTSTR pValueName,
  _Out_ LPDWORD pType,
  _Out_ LPBYTE  pData,
  _In_  DWORD   nSize,
  _Out_ LPDWORD pcbNeeded
);
```



## <a name="parameters"></a><span data-ttu-id="cdd79-108">Параметры</span><span class="sxs-lookup"><span data-stu-id="cdd79-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="cdd79-109">*хпринтер* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="cdd79-109">*hPrinter* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="cdd79-110">Маркер принтера или сервера печати, для которого функция получает данные конфигурации.</span><span class="sxs-lookup"><span data-stu-id="cdd79-110">A handle to the printer or print server for which the function retrieves configuration data.</span></span> <span data-ttu-id="cdd79-111">Используйте функцию [**опенпринтер**](openprinter.md), [**OpenPrinter2**](openprinter2.md)или [**аддпринтер**](addprinter.md) для получения маркера принтера.</span><span class="sxs-lookup"><span data-stu-id="cdd79-111">Use the [**OpenPrinter**](openprinter.md), [**OpenPrinter2**](openprinter2.md), or [**AddPrinter**](addprinter.md) function to retrieve a printer handle.</span></span>

</dd> <dt>

<span data-ttu-id="cdd79-112">*пкэйнаме* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="cdd79-112">*pKeyName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="cdd79-113">Указатель на строку, завершающуюся нулем, которая указывает ключ, содержащий извлекаемое значение.</span><span class="sxs-lookup"><span data-stu-id="cdd79-113">A pointer to a null-terminated string that specifies the key containing the value to be retrieved.</span></span> <span data-ttu-id="cdd79-114">Используйте символ обратной косой черты ( \\ ) в качестве разделителя, чтобы указать путь с одним или несколькими подразделами.</span><span class="sxs-lookup"><span data-stu-id="cdd79-114">Use the backslash ( \\ ) character as a delimiter to specify a path that has one or more subkeys.</span></span>

<span data-ttu-id="cdd79-115">Если *хпринтер* является обработчиком для принтера, *Пкэйнаме* имеет **значение NULL** или является пустой строкой, **жетпринтердатаекс** возвращает **ошибку \_ Недопустимый \_ параметр**.</span><span class="sxs-lookup"><span data-stu-id="cdd79-115">If *hPrinter* is a handle to a printer and *pKeyName* is **NULL** or an empty string, **GetPrinterDataEx** returns **ERROR\_INVALID\_PARAMETER**.</span></span>

<span data-ttu-id="cdd79-116">Если *хпринтер* является обработчиком для сервера печати, *пкэйнаме* игнорируется.</span><span class="sxs-lookup"><span data-stu-id="cdd79-116">If *hPrinter* is a handle to a print server, *pKeyName* is ignored.</span></span>

</dd> <dt>

<span data-ttu-id="cdd79-117">*пвалуенаме* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="cdd79-117">*pValueName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="cdd79-118">Указатель на строку, завершающуюся нулем, которая определяет извлекаемые данные.</span><span class="sxs-lookup"><span data-stu-id="cdd79-118">A pointer to a null-terminated string that identifies the data to retrieve.</span></span>

<span data-ttu-id="cdd79-119">Для принтеров эта строка указывает имя значения под ключом *пкэйнаме* .</span><span class="sxs-lookup"><span data-stu-id="cdd79-119">For printers, this string specifies the name of a value under the *pKeyName* key.</span></span>

<span data-ttu-id="cdd79-120">Для серверов печати эта строка является одной из предопределенных строк, перечисленных в следующем разделе "Примечания".</span><span class="sxs-lookup"><span data-stu-id="cdd79-120">For print servers, this string is one of the predefined strings listed in the following Remarks section.</span></span>

</dd> <dt>

<span data-ttu-id="cdd79-121">*птипе* \[ заполняет\]</span><span class="sxs-lookup"><span data-stu-id="cdd79-121">*pType* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="cdd79-122">Указатель на переменную, которая получает тип данных, хранящихся в значении.</span><span class="sxs-lookup"><span data-stu-id="cdd79-122">A pointer to a variable that receives the type of data stored in the value.</span></span> <span data-ttu-id="cdd79-123">Функция возвращает тип, указанный в вызове [**сетпринтердатаекс**](setprinterdataex.md) при сохранении данных.</span><span class="sxs-lookup"><span data-stu-id="cdd79-123">The function returns the type specified in the [**SetPrinterDataEx**](setprinterdataex.md) call when the data was stored.</span></span> <span data-ttu-id="cdd79-124">Если сведения не нужны, этот параметр может иметь **значение NULL** .</span><span class="sxs-lookup"><span data-stu-id="cdd79-124">This parameter can be **NULL** if you don't need the information.</span></span> <span data-ttu-id="cdd79-125">**Жетпринтердатаекс** передает *птипе* в качестве параметра *лпдвтипе* вызова функции [**процедура RegQueryValueEx**](/windows/desktop/api/winreg/nf-winreg-regqueryvalueexa) .</span><span class="sxs-lookup"><span data-stu-id="cdd79-125">**GetPrinterDataEx** passes *pType* on as the *lpdwType* parameter of a [**RegQueryValueEx**](/windows/desktop/api/winreg/nf-winreg-regqueryvalueexa) function call.</span></span>

</dd> <dt>

<span data-ttu-id="cdd79-126">*pData* \[ заполняет\]</span><span class="sxs-lookup"><span data-stu-id="cdd79-126">*pData* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="cdd79-127">Указатель на буфер, который получает данные конфигурации.</span><span class="sxs-lookup"><span data-stu-id="cdd79-127">A pointer to a buffer that receives the configuration data.</span></span>

</dd> <dt>

<span data-ttu-id="cdd79-128">*нсизе* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="cdd79-128">*nSize* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="cdd79-129">Размер (в байтах) буфера, на который указывает *pData*.</span><span class="sxs-lookup"><span data-stu-id="cdd79-129">The size, in bytes, of the buffer pointed to by *pData*.</span></span>

</dd> <dt>

<span data-ttu-id="cdd79-130">*пкбнидед* \[ заполняет\]</span><span class="sxs-lookup"><span data-stu-id="cdd79-130">*pcbNeeded* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="cdd79-131">Указатель на переменную, которая получает размер данных конфигурации в байтах.</span><span class="sxs-lookup"><span data-stu-id="cdd79-131">A pointer to a variable that receives the size, in bytes, of the configuration data.</span></span> <span data-ttu-id="cdd79-132">Если размер буфера, указанный параметром *нсизе* , слишком мал, функция возвращает **ошибку \_ больше \_ данных**, а *пкбнидед* указывает требуемый размер буфера.</span><span class="sxs-lookup"><span data-stu-id="cdd79-132">If the buffer size specified by *nSize* is too small, the function returns **ERROR\_MORE\_DATA**, and *pcbNeeded* indicates the required buffer size.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="cdd79-133">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="cdd79-133">Return value</span></span>

<span data-ttu-id="cdd79-134">Если функция завершается успешно, возвращается значение **ошибки \_ Success**.</span><span class="sxs-lookup"><span data-stu-id="cdd79-134">If the function succeeds, the return value is **ERROR\_SUCCESS**.</span></span>

<span data-ttu-id="cdd79-135">Если функция завершается ошибкой, возвращается значение ошибки.</span><span class="sxs-lookup"><span data-stu-id="cdd79-135">If the function fails, the return value is an error value.</span></span>

## <a name="remarks"></a><span data-ttu-id="cdd79-136">Комментарии</span><span class="sxs-lookup"><span data-stu-id="cdd79-136">Remarks</span></span>

> [!Note]  
> <span data-ttu-id="cdd79-137">Это блокирующая или синхронная функция, которая может не возвращать значение немедленно.</span><span class="sxs-lookup"><span data-stu-id="cdd79-137">This is a blocking or synchronous function and might not return immediately.</span></span> <span data-ttu-id="cdd79-138">Скорость возврата этой функцией зависит от факторов времени выполнения, таких как состояние сети, Конфигурация сервера печати и факторы реализации драйвера принтера, которые трудно предсказать при написании приложения.</span><span class="sxs-lookup"><span data-stu-id="cdd79-138">How quickly this function returns depends on run-time factors such as network status, print server configuration, and printer driver implementation factors that are difficult to predict when writing an application.</span></span> <span data-ttu-id="cdd79-139">Вызов этой функции из потока, который управляет взаимодействием с пользовательским интерфейсом, может привести к невозможности реагирования приложения.</span><span class="sxs-lookup"><span data-stu-id="cdd79-139">Calling this function from a thread that manages interaction with the user interface could make the application appear to be unresponsive.</span></span>

 

<span data-ttu-id="cdd79-140">**Жетпринтердатаекс** получает данные конфигурации принтера, которые были заданы функциями [**сетпринтердатаекс**](setprinterdataex.md) и [**сетпринтердата**](setprinterdata.md) .</span><span class="sxs-lookup"><span data-stu-id="cdd79-140">**GetPrinterDataEx** retrieves printer-configuration data that was set by the [**SetPrinterDataEx**](setprinterdataex.md) and [**SetPrinterData**](setprinterdata.md) functions.</span></span>

<span data-ttu-id="cdd79-141">Вызов **жетпринтердатаекс** с параметром *пкэйнаме* , для которого задано значение "принтердривердата", эквивалентен вызову функции [**жетпринтердата**](getprinterdata.md) .</span><span class="sxs-lookup"><span data-stu-id="cdd79-141">Calling **GetPrinterDataEx** with the *pKeyName* parameter set to "PrinterDriverData" is equivalent to calling the [**GetPrinterData**](getprinterdata.md) function.</span></span>

<span data-ttu-id="cdd79-142">Если *хпринтер* является обработчиком для сервера печати, *пвалуенаме* может указать одно из следующих предопределенных значений.</span><span class="sxs-lookup"><span data-stu-id="cdd79-142">If *hPrinter* is a handle to a print server, *pValueName* can specify one of the following predefined values.</span></span>



| <span data-ttu-id="cdd79-143">Значение</span><span class="sxs-lookup"><span data-stu-id="cdd79-143">Value</span></span>                                                               | <span data-ttu-id="cdd79-144">Комментарии</span><span class="sxs-lookup"><span data-stu-id="cdd79-144">Comments</span></span>                                                                                                                                                                                                                        |
|---------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="cdd79-145">**СПЛРЕГ \_ Разрешить \_ \_ манажеформс пользователя**</span><span class="sxs-lookup"><span data-stu-id="cdd79-145">**SPLREG\_ALLOW\_USER\_MANAGEFORMS**</span></span>                                | <span data-ttu-id="cdd79-146">Windows XP с пакетом обновления 2 (SP2) и более поздние версии</span><span class="sxs-lookup"><span data-stu-id="cdd79-146">Windows XP with Service Pack 2 (SP2) and later</span></span><br/> <span data-ttu-id="cdd79-147">Windows Server 2003 с пакетом обновления 1 (SP1) и более поздние версии</span><span class="sxs-lookup"><span data-stu-id="cdd79-147">Windows Server 2003 with Service Pack 1 (SP1) and later</span></span><br/>                                                                                                    |
| <span data-ttu-id="cdd79-148">**\_архитектура сплрег**</span><span class="sxs-lookup"><span data-stu-id="cdd79-148">**SPLREG\_ARCHITECTURE**</span></span>                                            |                                                                                                                                                                                                                                 |
| <span data-ttu-id="cdd79-149">**\_включен звуковой сигнал сплрег \_**</span><span class="sxs-lookup"><span data-stu-id="cdd79-149">**SPLREG\_BEEP\_ENABLED**</span></span>                                           |                                                                                                                                                                                                                                 |
| <span data-ttu-id="cdd79-150">**СПЛРЕГ \_ \_ Каталог очереди печати по умолчанию \_**</span><span class="sxs-lookup"><span data-stu-id="cdd79-150">**SPLREG\_DEFAULT\_SPOOL\_DIRECTORY**</span></span>                               |                                                                                                                                                                                                                                 |
| <span data-ttu-id="cdd79-151">**СПЛРЕГ \_ DNS \_ - \_ имя компьютера**</span><span class="sxs-lookup"><span data-stu-id="cdd79-151">**SPLREG\_DNS\_MACHINE\_NAME**</span></span>                                      |                                                                                                                                                                                                                                 |
| <span data-ttu-id="cdd79-152">**СПЛРЕГ \_ DS \_**</span><span class="sxs-lookup"><span data-stu-id="cdd79-152">**SPLREG\_DS\_PRESENT**</span></span>                                             | <span data-ttu-id="cdd79-153">При успешном возвращении *pData* содержит 0x0001, если компьютер находится в домене DS, в противном случае — 0.</span><span class="sxs-lookup"><span data-stu-id="cdd79-153">On successful return, *pData* contains 0x0001 if the machine is on a DS domain, 0 otherwise.</span></span><br/>                                                                                                                         |
| <span data-ttu-id="cdd79-154">**СПЛРЕГ \_ DS \_ \_ для \_ пользователя**</span><span class="sxs-lookup"><span data-stu-id="cdd79-154">**SPLREG\_DS\_PRESENT\_FOR\_USER**</span></span>                                  | <span data-ttu-id="cdd79-155">При успешном возвращении *pData* содержит 0x0001, если пользователь вошел в домен DS, в противном случае — 0.</span><span class="sxs-lookup"><span data-stu-id="cdd79-155">On successful return, *pData* contains 0x0001 if the user is logged onto a DS domain, 0 otherwise.</span></span><br/>                                                                                                                   |
| <span data-ttu-id="cdd79-156">**\_журнал событий \_ сплрег**</span><span class="sxs-lookup"><span data-stu-id="cdd79-156">**SPLREG\_EVENT\_LOG**</span></span>                                              |                                                                                                                                                                                                                                 |
| <span data-ttu-id="cdd79-157">**\_Основная \_ версия сплрег**</span><span class="sxs-lookup"><span data-stu-id="cdd79-157">**SPLREG\_MAJOR\_VERSION**</span></span>                                          |                                                                                                                                                                                                                                 |
| <span data-ttu-id="cdd79-158">**\_дополнительный номер \_ версии сплрег**</span><span class="sxs-lookup"><span data-stu-id="cdd79-158">**SPLREG\_MINOR\_VERSION**</span></span>                                          |                                                                                                                                                                                                                                 |
| <span data-ttu-id="cdd79-159">**\_ \_ всплывающее меню сплрег NET**</span><span class="sxs-lookup"><span data-stu-id="cdd79-159">**SPLREG\_NET\_POPUP**</span></span>                                              | <span data-ttu-id="cdd79-160">Не поддерживается в Windows Server 2003 и более поздних версиях</span><span class="sxs-lookup"><span data-stu-id="cdd79-160">Not supported in Windows Server 2003 and later</span></span><br/>                                                                                                                                                                       |
| <span data-ttu-id="cdd79-161">**СПЛРЕГ \_ net \_ Popup \_ to \_ Computer**</span><span class="sxs-lookup"><span data-stu-id="cdd79-161">**SPLREG\_NET\_POPUP\_TO\_COMPUTER**</span></span>                                | <span data-ttu-id="cdd79-162">При успешном возвращении *pData* содержит 1, если уведомления о задании должны отправляться на клиентский компьютер, или 0, если уведомления о задании будут отправляться пользователю.</span><span class="sxs-lookup"><span data-stu-id="cdd79-162">On successful return, *pData* contains 1 if job notifications should be sent to the client computer, or 0 if job notifications are to be sent to the user.</span></span><br/> <span data-ttu-id="cdd79-163">Не поддерживается в Windows Server 2003 и более поздних версиях</span><span class="sxs-lookup"><span data-stu-id="cdd79-163">Not supported in Windows Server 2003 and later</span></span><br/> |
| <span data-ttu-id="cdd79-164">**\_версия ОС \_ сплрег**</span><span class="sxs-lookup"><span data-stu-id="cdd79-164">**SPLREG\_OS\_VERSION**</span></span>                                             | <span data-ttu-id="cdd79-165">Windows XP и более поздних версий.</span><span class="sxs-lookup"><span data-stu-id="cdd79-165">Windows XP and later</span></span><br/>                                                                                                                                                                                                 |
| <span data-ttu-id="cdd79-166">**СПЛРЕГ \_ OS \_ версионекс**</span><span class="sxs-lookup"><span data-stu-id="cdd79-166">**SPLREG\_OS\_VERSIONEX**</span></span>                                           |                                                                                                                                                                                                                                 |
| <span data-ttu-id="cdd79-167">**\_ \_ приоритет потока портов \_ сплрег \_ по умолчанию**</span><span class="sxs-lookup"><span data-stu-id="cdd79-167">**SPLREG\_PORT\_THREAD\_PRIORITY\_DEFAULT**</span></span>                         |                                                                                                                                                                                                                                 |
| <span data-ttu-id="cdd79-168">**\_ \_ приоритет потока портов \_ сплрег**</span><span class="sxs-lookup"><span data-stu-id="cdd79-168">**SPLREG\_PORT\_THREAD\_PRIORITY**</span></span>                                  |                                                                                                                                                                                                                                 |
| <span data-ttu-id="cdd79-169">**\_ \_ \_ группы изоляции драйвера печати \_ сплрег**</span><span class="sxs-lookup"><span data-stu-id="cdd79-169">**SPLREG\_PRINT\_DRIVER\_ISOLATION\_GROUPS**</span></span>                        | <span data-ttu-id="cdd79-170">Windows 7 и более поздние версии</span><span class="sxs-lookup"><span data-stu-id="cdd79-170">Windows 7 and later</span></span><br/>                                                                                                                                                                                                  |
| <span data-ttu-id="cdd79-171">**СПЛРЕГ \_ \_ \_ время изоляции драйвера \_ печати \_ перед \_ повторным запуском**</span><span class="sxs-lookup"><span data-stu-id="cdd79-171">**SPLREG\_PRINT\_DRIVER\_ISOLATION\_TIME\_BEFORE\_RECYCLE**</span></span>         | <span data-ttu-id="cdd79-172">Windows 7 и более поздние версии</span><span class="sxs-lookup"><span data-stu-id="cdd79-172">Windows 7 and later</span></span><br/>                                                                                                                                                                                                  |
| <span data-ttu-id="cdd79-173">**СПЛРЕГ \_ \_ \_ \_ Максимальное число объектов изоляции драйвера печати \_ \_ перед \_ повторным запуском**</span><span class="sxs-lookup"><span data-stu-id="cdd79-173">**SPLREG\_PRINT\_DRIVER\_ISOLATION\_MAX\_OBJECTS\_BEFORE\_RECYCLE**</span></span> | <span data-ttu-id="cdd79-174">Windows 7 и более поздние версии</span><span class="sxs-lookup"><span data-stu-id="cdd79-174">Windows 7 and later</span></span><br/>                                                                                                                                                                                                  |
| <span data-ttu-id="cdd79-175">**СПЛРЕГ \_ \_ \_ \_ время ожидания простоя для изоляции драйвера печати \_**</span><span class="sxs-lookup"><span data-stu-id="cdd79-175">**SPLREG\_PRINT\_DRIVER\_ISOLATION\_IDLE\_TIMEOUT**</span></span>                 | <span data-ttu-id="cdd79-176">Windows 7 и более поздние версии</span><span class="sxs-lookup"><span data-stu-id="cdd79-176">Windows 7 and later</span></span><br/>                                                                                                                                                                                                  |
| <span data-ttu-id="cdd79-177">**\_ \_ \_ \_ Политика выполнения изоляции драйвера печати \_ сплрег**</span><span class="sxs-lookup"><span data-stu-id="cdd79-177">**SPLREG\_PRINT\_DRIVER\_ISOLATION\_EXECUTION\_POLICY**</span></span>             | <span data-ttu-id="cdd79-178">Windows 7 и более поздние версии</span><span class="sxs-lookup"><span data-stu-id="cdd79-178">Windows 7 and later</span></span><br/>                                                                                                                                                                                                  |
| <span data-ttu-id="cdd79-179">**\_ \_ \_ Политика переопределения режима изоляции \_ драйвера \_ печати сплрег**</span><span class="sxs-lookup"><span data-stu-id="cdd79-179">**SPLREG\_PRINT\_DRIVER\_ISOLATION\_OVERRIDE\_POLICY**</span></span>              | <span data-ttu-id="cdd79-180">Windows 7 и более поздние версии</span><span class="sxs-lookup"><span data-stu-id="cdd79-180">Windows 7 and later</span></span><br/>                                                                                                                                                                                                  |
| <span data-ttu-id="cdd79-181">**\_Удаленный \_ Факс сплрег**</span><span class="sxs-lookup"><span data-stu-id="cdd79-181">**SPLREG\_REMOTE\_FAX**</span></span>                                             | <span data-ttu-id="cdd79-182">При успешном возвращении *pData* содержит 0x0001, если служба факсов поддерживает удаленные клиенты. в противном случае — 0.</span><span class="sxs-lookup"><span data-stu-id="cdd79-182">On successful return, *pData* contains 0x0001 if the FAX service supports remote clients, 0 otherwise.</span></span><br/>                                                                                                               |
| <span data-ttu-id="cdd79-183">**\_всплывающее окно повторной попытки сплрег \_**</span><span class="sxs-lookup"><span data-stu-id="cdd79-183">**SPLREG\_RETRY\_POPUP**</span></span>                                            | <span data-ttu-id="cdd79-184">При успешном возвращении *pData* содержит 1, если на сервере настроено повторное открытие всплывающих окон для всех заданий, или значение 0, если сервер не пытается повторно открывать всплывающие окна для всех заданий.</span><span class="sxs-lookup"><span data-stu-id="cdd79-184">On successful return, *pData* contains 1 if server is set to retry pop-up windows for all jobs, or 0 if server does not retry pop-up windows for all jobs.</span></span><br/> <span data-ttu-id="cdd79-185">Не поддерживается в Windows Server 2003 и более поздних версиях</span><span class="sxs-lookup"><span data-stu-id="cdd79-185">Not supported in Windows Server 2003 and later</span></span><br/> |
| <span data-ttu-id="cdd79-186">**\_приоритет потока планировщика сплрег \_ \_**</span><span class="sxs-lookup"><span data-stu-id="cdd79-186">**SPLREG\_SCHEDULER\_THREAD\_PRIORITY**</span></span>                             |                                                                                                                                                                                                                                 |
| <span data-ttu-id="cdd79-187">**\_приоритет потока планировщика сплрег \_ \_ \_ по умолчанию**</span><span class="sxs-lookup"><span data-stu-id="cdd79-187">**SPLREG\_SCHEDULER\_THREAD\_PRIORITY\_DEFAULT**</span></span>                    |                                                                                                                                                                                                                                 |
| <span data-ttu-id="cdd79-188">**СПЛРЕГ \_ вебшаремгмт**</span><span class="sxs-lookup"><span data-stu-id="cdd79-188">**SPLREG\_WEBSHAREMGMT**</span></span>                                            | <span data-ttu-id="cdd79-189">Windows Server 2003 и более поздние версии</span><span class="sxs-lookup"><span data-stu-id="cdd79-189">Windows Server 2003 and later</span></span><br/>                                                                                                                                                                                        |



 

<span data-ttu-id="cdd79-190">Следующие значения *пвалуенаме* указывают на поведение печати пула при возникновении ошибки.</span><span class="sxs-lookup"><span data-stu-id="cdd79-190">The following values of *pValueName* indicate the pool printing behavior when an error occurs.</span></span>



| <span data-ttu-id="cdd79-191">Значение</span><span class="sxs-lookup"><span data-stu-id="cdd79-191">Value</span></span>                                       | <span data-ttu-id="cdd79-192">Комментарии</span><span class="sxs-lookup"><span data-stu-id="cdd79-192">Comments</span></span>                                                                                                                                                                                              |
|---------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="cdd79-193">**\_сбой задания перезапуска сплрег \_ \_ при \_ \_ ошибке пула**</span><span class="sxs-lookup"><span data-stu-id="cdd79-193">**SPLREG\_RESTART\_JOB\_ON\_POOL\_ERROR**</span></span>   | <span data-ttu-id="cdd79-194">Значение *pData* указывает время в секундах, когда задание перезапускается на другом порте после возникновения ошибки.</span><span class="sxs-lookup"><span data-stu-id="cdd79-194">The value of *pData* indicates the time, in seconds, when a job is restarted on another port after an error occurs.</span></span> <span data-ttu-id="cdd79-195">Этот параметр используется при **\_ \_ \_ \_ \_ включении задания перезапуска сплрег в пуле**.</span><span class="sxs-lookup"><span data-stu-id="cdd79-195">This setting is used with **SPLREG\_RESTART\_JOB\_ON\_POOL\_ENABLED**.</span></span><br/> |
| <span data-ttu-id="cdd79-196">**\_Задание перезапуска сплрег \_ \_ в \_ пуле \_ включено**</span><span class="sxs-lookup"><span data-stu-id="cdd79-196">**SPLREG\_RESTART\_JOB\_ON\_POOL\_ENABLED**</span></span> | <span data-ttu-id="cdd79-197">Ненулевое значение в *pData* указывает, что включено **\_ Задание перезапуска сплрег \_ \_ при \_ \_ ошибке пула** .</span><span class="sxs-lookup"><span data-stu-id="cdd79-197">A nonzero value in *pData* indicates that **SPLREG\_RESTART\_JOB\_ON\_POOL\_ERROR** is enabled.</span></span><br/>                                                                                            |



 

<span data-ttu-id="cdd79-198">Время, указанное в **\_ задании перезапуска сплрег \_ \_ в случае \_ \_ ошибки пула** , является минимальным временем.</span><span class="sxs-lookup"><span data-stu-id="cdd79-198">The time specified in **SPLREG\_RESTART\_JOB\_ON\_POOL\_ERROR** is a minimum time.</span></span> <span data-ttu-id="cdd79-199">Фактическое время может быть больше, в зависимости от следующих параметров монитора портов, которые являются значениями реестра в этом разделе реестра:</span><span class="sxs-lookup"><span data-stu-id="cdd79-199">The actual time can be longer, depending on the following port monitor settings, which are registry values under this registry key:</span></span>

<span data-ttu-id="cdd79-200">**HKLM \\ System CurrentControlSet Control Monitoring MONITORS \\ \\ \\ \\ \\ < *мониторнаме* > \\ ports**</span><span class="sxs-lookup"><span data-stu-id="cdd79-200">**HKLM\\SYSTEM\\CurrentControlSet\\Control\\Print\\Monitors\\<*MonitorName*>\\Ports**</span></span>

<span data-ttu-id="cdd79-201">Чтобы запросить эти значения, вызовите функцию [**процедура RegQueryValueEx**](/windows/win32/api/winreg/nf-winreg-regqueryvalueexa) .</span><span class="sxs-lookup"><span data-stu-id="cdd79-201">Call the [**RegQueryValueEx**](/windows/win32/api/winreg/nf-winreg-regqueryvalueexa) function to query these values.</span></span>



| <span data-ttu-id="cdd79-202">Параметр монитора порта</span><span class="sxs-lookup"><span data-stu-id="cdd79-202">Port monitor setting</span></span>     | <span data-ttu-id="cdd79-203">Тип данных</span><span class="sxs-lookup"><span data-stu-id="cdd79-203">Data type</span></span>      | <span data-ttu-id="cdd79-204">Значение</span><span class="sxs-lookup"><span data-stu-id="cdd79-204">Meaning</span></span>                                                                                                        |
|--------------------------|----------------|----------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="cdd79-205">**статусупдатинаблед**</span><span class="sxs-lookup"><span data-stu-id="cdd79-205">**StatusUpdateEnabled**</span></span>  | <span data-ttu-id="cdd79-206">**REG \_ DWORD**</span><span class="sxs-lookup"><span data-stu-id="cdd79-206">**REG\_DWORD**</span></span> | <span data-ttu-id="cdd79-207">При ненулевом значении разрешает монитору портов обновлять Диспетчер очереди с состоянием порта.</span><span class="sxs-lookup"><span data-stu-id="cdd79-207">If a nonzero value, enables the port monitor to update the spooler with the port status.</span></span><br/>            |
| <span data-ttu-id="cdd79-208">**статусупдатеинтервал**</span><span class="sxs-lookup"><span data-stu-id="cdd79-208">**StatusUpdateInterval**</span></span> | <span data-ttu-id="cdd79-209">**REG \_ DWORD**</span><span class="sxs-lookup"><span data-stu-id="cdd79-209">**REG\_DWORD**</span></span> | <span data-ttu-id="cdd79-210">Указывает интервал (в минутах), в течение которого монитор порта обновляет Диспетчер очереди с состоянием порта.</span><span class="sxs-lookup"><span data-stu-id="cdd79-210">Specifies the interval, in minutes, when the port monitor updates the spooler with the port status.</span></span><br/> |



 

<span data-ttu-id="cdd79-211">Если *пкэйнаме* является одним из стандартных ключей службы каталогов (см. [**сетпринтер**](setprinter.md)), а *пвалуенаме* содержит запятую (","), то часть *пвалуенаме* перед запятой является именем значения, а часть *пвалуенаме* — идентификатор OID свойства DS.</span><span class="sxs-lookup"><span data-stu-id="cdd79-211">If *pKeyName* is one of the predefined Directory Service (DS) keys (see [**SetPrinter**](setprinter.md)) and *pValueName* contains a comma (','), then the portion of *pValueName* before the comma is the value name and the portion of *pValueName* to the right of the comma is the DS Property OID.</span></span> <span data-ttu-id="cdd79-212">Создается подраздел с именем OID, а в ключе OID указывается новое значение, состоящее из имени значения и OID.</span><span class="sxs-lookup"><span data-stu-id="cdd79-212">A subkey called OID is created and a new value that consists of the value name and OID is entered under the OID key.</span></span> <span data-ttu-id="cdd79-213">[**Сетпринтердатаекс**](setprinterdataex.md) также добавляет имя значения и данные в ключе DS.</span><span class="sxs-lookup"><span data-stu-id="cdd79-213">[**SetPrinterDataEx**](setprinterdataex.md) also adds the value name and data under the DS key.</span></span>

<span data-ttu-id="cdd79-214">В Windows 7 и более поздних версиях Windows задания печати, отправленные на сервер печати, по умолчанию подготавливаются к просмотру на клиенте.</span><span class="sxs-lookup"><span data-stu-id="cdd79-214">In Windows 7 and later versions of Windows, print jobs that are sent to a print server are rendered on the client by default.</span></span> <span data-ttu-id="cdd79-215">Конфигурацию отрисовки на стороне клиента для принтера можно прочитать, задав для параметра *пкэйнаме* значение "принтердривердата" и *пвалуенаме* в качестве значения параметра в следующей таблице.</span><span class="sxs-lookup"><span data-stu-id="cdd79-215">The configuration of client-side rendering for a printer can be read by setting *pKeyName* to "PrinterDriverData" and *pValueName* to the setting value in the following table.</span></span>



| <span data-ttu-id="cdd79-216">Параметр</span><span class="sxs-lookup"><span data-stu-id="cdd79-216">Setting</span></span>                      | <span data-ttu-id="cdd79-217">Тип данных</span><span class="sxs-lookup"><span data-stu-id="cdd79-217">Data type</span></span>      | <span data-ttu-id="cdd79-218">Описание</span><span class="sxs-lookup"><span data-stu-id="cdd79-218">Description</span></span>                                                                                                                                                                                                                                                                                                                                                                                                       |
|------------------------------|----------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="cdd79-219">**емфдеспулингсеттинг**</span><span class="sxs-lookup"><span data-stu-id="cdd79-219">**EMFDespoolingSetting**</span></span>     | <span data-ttu-id="cdd79-220">**REG \_ DWORD**</span><span class="sxs-lookup"><span data-stu-id="cdd79-220">**REG\_DWORD**</span></span> | <span data-ttu-id="cdd79-221">Значение 0 или, если это значение отсутствует в реестре, включает отрисовку заданий печати на стороне клиента по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="cdd79-221">A value of 0, or if this value is not present in the registry, enables the default client-side rendering of print jobs.</span></span><br/> <span data-ttu-id="cdd79-222">Значение 1 отключает отрисовку заданий печати на стороне клиента.</span><span class="sxs-lookup"><span data-stu-id="cdd79-222">A value of 1 disables client-side rendering of print jobs.</span></span><br/>                                                                                                                                                                                                          |
| <span data-ttu-id="cdd79-223">**форцеклиентсидерендеринг**</span><span class="sxs-lookup"><span data-stu-id="cdd79-223">**ForceClientSideRendering**</span></span> | <span data-ttu-id="cdd79-224">**REG \_ DWORD**</span><span class="sxs-lookup"><span data-stu-id="cdd79-224">**REG\_DWORD**</span></span> | <span data-ttu-id="cdd79-225">Значение 0 или, если это значение отсутствует в реестре, приведет к отображению заданий печати на клиенте.</span><span class="sxs-lookup"><span data-stu-id="cdd79-225">A value of 0, or if this value is not present in the registry, will cause the print jobs to be rendered on the client.</span></span> <span data-ttu-id="cdd79-226">Если задание печати не может быть визуализировано на клиенте, оно будет подготовлено к просмотру на сервере.</span><span class="sxs-lookup"><span data-stu-id="cdd79-226">If a print job cannot be rendered on the client, it will be rendered on the server.</span></span> <span data-ttu-id="cdd79-227">Если задание печати не может быть подготовлено к просмотру на сервере, оно завершится ошибкой.</span><span class="sxs-lookup"><span data-stu-id="cdd79-227">If a print job cannot be rendered on the server, it will fail.</span></span><br/> <span data-ttu-id="cdd79-228">Значение 1 будет отображать задания печати на клиенте.</span><span class="sxs-lookup"><span data-stu-id="cdd79-228">A value of 1 will render print jobs on the client.</span></span> <span data-ttu-id="cdd79-229">Если задание печати не может быть визуализировано на клиенте, оно завершится ошибкой.</span><span class="sxs-lookup"><span data-stu-id="cdd79-229">If a print job cannot be rendered on the client, it will fail.</span></span><br/> |



 

## <a name="requirements"></a><span data-ttu-id="cdd79-230">Требования</span><span class="sxs-lookup"><span data-stu-id="cdd79-230">Requirements</span></span>



| <span data-ttu-id="cdd79-231">Требование</span><span class="sxs-lookup"><span data-stu-id="cdd79-231">Requirement</span></span> | <span data-ttu-id="cdd79-232">Значение</span><span class="sxs-lookup"><span data-stu-id="cdd79-232">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="cdd79-233">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="cdd79-233">Minimum supported client</span></span><br/> | <span data-ttu-id="cdd79-234">Windows 2000 Professional \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="cdd79-234">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                                |
| <span data-ttu-id="cdd79-235">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="cdd79-235">Minimum supported server</span></span><br/> | <span data-ttu-id="cdd79-236">Windows 2000 Server \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="cdd79-236">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                      |
| <span data-ttu-id="cdd79-237">Заголовок</span><span class="sxs-lookup"><span data-stu-id="cdd79-237">Header</span></span><br/>                   | <dl> <span data-ttu-id="cdd79-238"><dt>Винспул. h (включение Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="cdd79-238"><dt>Winspool.h (include Windows.h)</dt></span></span> </dl> |
| <span data-ttu-id="cdd79-239">Библиотека</span><span class="sxs-lookup"><span data-stu-id="cdd79-239">Library</span></span><br/>                  | <dl> <span data-ttu-id="cdd79-240"><dt>Винспул. lib</dt></span><span class="sxs-lookup"><span data-stu-id="cdd79-240"><dt>Winspool.lib</dt></span></span> </dl>                   |
| <span data-ttu-id="cdd79-241">DLL</span><span class="sxs-lookup"><span data-stu-id="cdd79-241">DLL</span></span><br/>                      | <dl> <span data-ttu-id="cdd79-242"><dt>Винспул. drv</dt></span><span class="sxs-lookup"><span data-stu-id="cdd79-242"><dt>Winspool.drv</dt></span></span> </dl>                   |
| <span data-ttu-id="cdd79-243">Имя в кодировке Юникод и ANSI</span><span class="sxs-lookup"><span data-stu-id="cdd79-243">Unicode and ANSI names</span></span><br/>   | <span data-ttu-id="cdd79-244">**Жетпринтердатаексв** (Юникод) и **жетпринтердатаекса** (ANSI)</span><span class="sxs-lookup"><span data-stu-id="cdd79-244">**GetPrinterDataExW** (Unicode) and **GetPrinterDataExA** (ANSI)</span></span><br/>                               |



## <a name="see-also"></a><span data-ttu-id="cdd79-245">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="cdd79-245">See also</span></span>

<dl> <dt>

[<span data-ttu-id="cdd79-246">Вывод на печать</span><span class="sxs-lookup"><span data-stu-id="cdd79-246">Printing</span></span>](printdocs-printing.md)
</dt> <dt>

[<span data-ttu-id="cdd79-247">Функции API очереди печати принтера</span><span class="sxs-lookup"><span data-stu-id="cdd79-247">Print Spooler API Functions</span></span>](printing-and-print-spooler-functions.md)
</dt> <dt>

[<span data-ttu-id="cdd79-248">**опенпринтер**</span><span class="sxs-lookup"><span data-stu-id="cdd79-248">**OpenPrinter**</span></span>](openprinter.md)
</dt> <dt>

[<span data-ttu-id="cdd79-249">**сетпринтердатаекс**</span><span class="sxs-lookup"><span data-stu-id="cdd79-249">**SetPrinterDataEx**</span></span>](setprinterdataex.md)
</dt> </dl>

 

