---
description: Функция Сетпринтердатаекс задает данные конфигурации для принтера или сервера печати. Функция сохраняет данные конфигурации в разделе реестра Printers.
ms.assetid: b7faadfc-1c81-4ddf-8fe5-68f4cc0376f1
title: Функция Сетпринтердатаекс (Винспул. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SetPrinterDataEx
- SetPrinterDataExA
- SetPrinterDataExW
api_type:
- DllExport
api_location:
- Winspool.drv
- Ext-MS-Win-printer-Winspool-l1-1-1.dll
- Ext-MS-Win-Printer-WinSpool-l1-1-2.dll
- Ext-MS-Win-Printer-WinSpool-L1-1-3.dll
ms.openlocfilehash: 9f384c9c9d6f0d956264b45ec8b52043ad20e897
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "104272103"
---
# <a name="setprinterdataex-function"></a><span data-ttu-id="42957-104">Функция Сетпринтердатаекс</span><span class="sxs-lookup"><span data-stu-id="42957-104">SetPrinterDataEx function</span></span>

<span data-ttu-id="42957-105">Функция **сетпринтердатаекс** задает данные конфигурации для принтера или сервера печати.</span><span class="sxs-lookup"><span data-stu-id="42957-105">The **SetPrinterDataEx** function sets the configuration data for a printer or print server.</span></span> <span data-ttu-id="42957-106">Функция сохраняет данные конфигурации в разделе реестра принтера.</span><span class="sxs-lookup"><span data-stu-id="42957-106">The function stores the configuration data under the printer's registry key.</span></span>

## <a name="syntax"></a><span data-ttu-id="42957-107">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="42957-107">Syntax</span></span>


```C++
DWORD SetPrinterDataEx(
  _In_ HANDLE  hPrinter,
  _In_ LPCTSTR pKeyName,
  _In_ LPCTSTR pValueName,
  _In_ DWORD   Type,
  _In_ LPBYTE  pData,
  _In_ DWORD   cbData
);
```



## <a name="parameters"></a><span data-ttu-id="42957-108">Параметры</span><span class="sxs-lookup"><span data-stu-id="42957-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="42957-109">*хпринтер* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="42957-109">*hPrinter* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="42957-110">Маркер принтера или сервера печати, для которого функция задает данные конфигурации.</span><span class="sxs-lookup"><span data-stu-id="42957-110">A handle to the printer or print server for which the function sets configuration data.</span></span> <span data-ttu-id="42957-111">Используйте функцию [**опенпринтер**](openprinter.md), [**OpenPrinter2**](openprinter2.md)или [**аддпринтер**](addprinter.md) для получения маркера принтера.</span><span class="sxs-lookup"><span data-stu-id="42957-111">Use the [**OpenPrinter**](openprinter.md), [**OpenPrinter2**](openprinter2.md), or [**AddPrinter**](addprinter.md) function to retrieve a printer handle.</span></span>

</dd> <dt>

<span data-ttu-id="42957-112">*пкэйнаме* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="42957-112">*pKeyName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="42957-113">Указатель на строку, завершающуюся нулем, которая указывает ключ, содержащий заданное значение.</span><span class="sxs-lookup"><span data-stu-id="42957-113">A pointer to a null-terminated string that specifies the key containing the value to set.</span></span> <span data-ttu-id="42957-114">Если указанный ключ или подразделы не существуют, функция создает их.</span><span class="sxs-lookup"><span data-stu-id="42957-114">If the specified key or subkeys do not exist, the function creates them.</span></span>

<span data-ttu-id="42957-115">Чтобы сохранить данные конфигурации, которые могут быть опубликованы в службе каталогов (DS), укажите один из следующих предопределенных разделов реестра.</span><span class="sxs-lookup"><span data-stu-id="42957-115">To store configuration data that can be published in the directory service (DS), specify one of the following predefined registry keys.</span></span>



| <span data-ttu-id="42957-116">Значение</span><span class="sxs-lookup"><span data-stu-id="42957-116">Value</span></span>                                                                                                                                                                      | <span data-ttu-id="42957-117">Значение</span><span class="sxs-lookup"><span data-stu-id="42957-117">Meaning</span></span>                                                                                         |
|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------|
| <span id="SPLDS_DRIVER_KEY"></span><span id="splds_driver_key"></span><dl> <span data-ttu-id="42957-118"><dt>**SPLDS_DRIVER_KEY**</dt></span><span class="sxs-lookup"><span data-stu-id="42957-118"><dt>**SPLDS_DRIVER_KEY**</dt></span></span> </dl>    | <span data-ttu-id="42957-119">Драйверы принтера этот ключ используется для хранения свойств драйвера.</span><span class="sxs-lookup"><span data-stu-id="42957-119">Printer drivers use this key to store driver properties.</span></span><br/>                             |
| <span id="SPLDS_SPOOLER_KEY"></span><span id="splds_spooler_key"></span><dl> <span data-ttu-id="42957-120"><dt>**SPLDS_SPOOLER_KEY**</dt></span><span class="sxs-lookup"><span data-stu-id="42957-120"><dt>**SPLDS_SPOOLER_KEY**</dt></span></span> </dl> | <span data-ttu-id="42957-121">Зарезервировано.</span><span class="sxs-lookup"><span data-stu-id="42957-121">Reserved.</span></span> <span data-ttu-id="42957-122">Используется только диспетчером очереди печати для хранения свойств внутреннего диспетчера очереди сообщений.</span><span class="sxs-lookup"><span data-stu-id="42957-122">Used only by the print spooler to store internal spooler properties.</span></span><br/>       |
| <span id="SPLDS_USER_KEY"></span><span id="splds_user_key"></span><dl> <span data-ttu-id="42957-123"><dt>**SPLDS_USER_KEY**</dt></span><span class="sxs-lookup"><span data-stu-id="42957-123"><dt>**SPLDS_USER_KEY**</dt></span></span> </dl>          | <span data-ttu-id="42957-124">Приложения используют этот ключ для хранения свойств принтера, например номеров ресурсов принтера.</span><span class="sxs-lookup"><span data-stu-id="42957-124">Applications use this key to store printer properties such as printer asset numbers.</span></span><br/> |



 

<span data-ttu-id="42957-125">Значения, хранящиеся в ключе SPLDS_USER_KEY, публикуются в службе каталогов только при наличии соответствующего свойства в схеме.</span><span class="sxs-lookup"><span data-stu-id="42957-125">Values that are stored under the SPLDS_USER_KEY key are published in the directory service only if there is a corresponding property in the schema.</span></span> <span data-ttu-id="42957-126">Администратор домена должен создать свойство, если оно еще не существует.</span><span class="sxs-lookup"><span data-stu-id="42957-126">A domain administrator must create the property if it doesn't already exist.</span></span> <span data-ttu-id="42957-127">Чтобы опубликовать определяемое пользователем свойство после использования **сетпринтердатаекс** для добавления или изменения значения, вызовите [**сетпринтер**](setprinter.md) с *Level* = 7 и установите для элемента **двактион** [**PRINTER_INFO_7**](printer-info-7.md) значение **DSPRINT_UPDATE**.</span><span class="sxs-lookup"><span data-stu-id="42957-127">To publish a user-defined property after you use **SetPrinterDataEx** to add or change a value, call [**SetPrinter**](setprinter.md) with *Level* = 7 and with the **dwAction** member of [**PRINTER_INFO_7**](printer-info-7.md) set to **DSPRINT_UPDATE**.</span></span>

<span data-ttu-id="42957-128">Можно указать другие ключи для хранения данных конфигурации, не являющихся службами DS.</span><span class="sxs-lookup"><span data-stu-id="42957-128">You can specify other keys to store non-DS configuration data.</span></span> <span data-ttu-id="42957-129">Используйте символ обратной косой черты ( \\ ) в качестве разделителя, чтобы указать путь с одним или несколькими подразделами.</span><span class="sxs-lookup"><span data-stu-id="42957-129">Use the backslash ( \\ ) character as a delimiter to specify a path that has one or more subkeys.</span></span>

<span data-ttu-id="42957-130">Если *хпринтер* является обработчиком для принтера, *Пкэйнаме* имеет **значение NULL** или является пустой строкой, **сетпринтердатаекс** возвращает **ERROR_INVALID_PARAMETER**.</span><span class="sxs-lookup"><span data-stu-id="42957-130">If *hPrinter* is a handle to a printer and *pKeyName* is **NULL** or an empty string, **SetPrinterDataEx** returns **ERROR_INVALID_PARAMETER**.</span></span>

<span data-ttu-id="42957-131">Если *хпринтер* является обработчиком для сервера печати, *пкэйнаме* игнорируется.</span><span class="sxs-lookup"><span data-stu-id="42957-131">If *hPrinter* is a handle to a print server, *pKeyName* is ignored.</span></span>

<span data-ttu-id="42957-132">Не используйте **SPLDS_SPOOLER_KEY**.</span><span class="sxs-lookup"><span data-stu-id="42957-132">Do not use **SPLDS_SPOOLER_KEY**.</span></span> <span data-ttu-id="42957-133">Чтобы изменить свойства принтера диспетчера очереди печати, используйте [**сетпринтер**](setprinter.md) с *Level* = 2.</span><span class="sxs-lookup"><span data-stu-id="42957-133">To change the spooler printer properties, use [**SetPrinter**](setprinter.md) with *Level* = 2.</span></span>

</dd> <dt>

<span data-ttu-id="42957-134">*пвалуенаме* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="42957-134">*pValueName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="42957-135">Указатель на строку, завершающуюся нулем, которая определяет данные для задания.</span><span class="sxs-lookup"><span data-stu-id="42957-135">A pointer to a null-terminated string that identifies the data to set.</span></span>

<span data-ttu-id="42957-136">Для принтеров эта строка указывает имя значения под ключом *пкэйнаме* .</span><span class="sxs-lookup"><span data-stu-id="42957-136">For printers, this string specifies the name of a value under the *pKeyName* key.</span></span>

<span data-ttu-id="42957-137">Для серверов печати эта строка является одной из предопределенных строк, перечисленных в следующем разделе "Примечания".</span><span class="sxs-lookup"><span data-stu-id="42957-137">For print servers, this string is one of the predefined strings listed in the following Remarks section.</span></span>

</dd> <dt>

<span data-ttu-id="42957-138">*Тип* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="42957-138">*Type* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="42957-139">Код, указывающий тип данных, на который указывает параметр *pData* .</span><span class="sxs-lookup"><span data-stu-id="42957-139">A code indicating the type of data pointed to by the *pData* parameter.</span></span> <span data-ttu-id="42957-140">Список возможных кодов типов см. в разделе [типы значений реестра](/windows/desktop/SysInfo/registry-value-types).</span><span class="sxs-lookup"><span data-stu-id="42957-140">For a list of the possible type codes, see [Registry Value Types](/windows/desktop/SysInfo/registry-value-types).</span></span>

<span data-ttu-id="42957-141">Если *пкэйнаме* указывает один из стандартных ключей службы каталогов, *тип* должен быть **REG_SZ**, **REG_MULTI_SZ**, **REG_DWORD** или **REG_BINARY**.</span><span class="sxs-lookup"><span data-stu-id="42957-141">If *pKeyName* specifies one of the predefined directory service keys, *Type* must be **REG_SZ**, **REG_MULTI_SZ**, **REG_DWORD**, or **REG_BINARY**.</span></span> <span data-ttu-id="42957-142">Если используется **REG_BINARY** , *cbData* должен быть равен 1, а служба каталогов обрабатывает их как логическое значение.</span><span class="sxs-lookup"><span data-stu-id="42957-142">If **REG_BINARY** is used, *cbData* must be equal to 1, and the directory service treats the data as a Boolean value.</span></span>

</dd> <dt>

<span data-ttu-id="42957-143">*pData* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="42957-143">*pData* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="42957-144">Указатель на буфер, содержащий данные конфигурации принтера.</span><span class="sxs-lookup"><span data-stu-id="42957-144">A pointer to a buffer that contains the printer configuration data.</span></span>

</dd> <dt>

<span data-ttu-id="42957-145">*cbData* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="42957-145">*cbData* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="42957-146">Размер массива в байтах.</span><span class="sxs-lookup"><span data-stu-id="42957-146">The size, in bytes, of the array.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="42957-147">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="42957-147">Return value</span></span>

<span data-ttu-id="42957-148">Если функция выполнена, возвращаемое значение будет **ERROR_SUCCESS**.</span><span class="sxs-lookup"><span data-stu-id="42957-148">If the function succeeds, the return value is **ERROR_SUCCESS**.</span></span>

<span data-ttu-id="42957-149">Если функция завершается ошибкой, возвращается значение ошибки.</span><span class="sxs-lookup"><span data-stu-id="42957-149">If the function fails, the return value is an error value.</span></span>

## <a name="remarks"></a><span data-ttu-id="42957-150">Комментарии</span><span class="sxs-lookup"><span data-stu-id="42957-150">Remarks</span></span>

> [!Note]  
> <span data-ttu-id="42957-151">Это блокирующая или синхронная функция, которая может не возвращать значение немедленно.</span><span class="sxs-lookup"><span data-stu-id="42957-151">This is a blocking or synchronous function and might not return immediately.</span></span> <span data-ttu-id="42957-152">Скорость возврата этой функцией зависит от факторов времени выполнения, таких как состояние сети, Конфигурация сервера печати и факторы реализации драйвера принтера, которые трудно предсказать при написании приложения.</span><span class="sxs-lookup"><span data-stu-id="42957-152">How quickly this function returns depends on run-time factors such as network status, print server configuration, and printer driver implementation factors that are difficult to predict when writing an application.</span></span> <span data-ttu-id="42957-153">Вызов этой функции из потока, который управляет взаимодействием с пользовательским интерфейсом, может привести к невозможности реагирования приложения.</span><span class="sxs-lookup"><span data-stu-id="42957-153">Calling this function from a thread that manages interaction with the user interface could make the application appear to be unresponsive.</span></span>

 

<span data-ttu-id="42957-154">Чтобы получить существующие данные конфигурации для принтера или диспетчера очереди печати, вызовите функцию [**жетпринтердатаекс**](getprinterdataex.md) .</span><span class="sxs-lookup"><span data-stu-id="42957-154">To retrieve existing configuration data for a printer or print spooler, call the [**GetPrinterDataEx**](getprinterdataex.md) function.</span></span>

<span data-ttu-id="42957-155">Вызов **сетпринтердатаекс** с параметром *пкэйнаме* , для которого задано значение "принтердривердата", эквивалентен вызову функции [**сетпринтердата**](setprinterdata.md) .</span><span class="sxs-lookup"><span data-stu-id="42957-155">Calling **SetPrinterDataEx** with the *pKeyName* parameter set to "PrinterDriverData" is equivalent to calling the [**SetPrinterData**](setprinterdata.md) function.</span></span>

<span data-ttu-id="42957-156">Если *хпринтер* является обработчиком для сервера печати, *пвалуенаме* может указать одно из следующих предопределенных значений.</span><span class="sxs-lookup"><span data-stu-id="42957-156">If *hPrinter* is a handle to a print server, *pValueName* can specify one of the following predefined values.</span></span>



| <span data-ttu-id="42957-157">Значение</span><span class="sxs-lookup"><span data-stu-id="42957-157">Value</span></span>                                                               | <span data-ttu-id="42957-158">Комментарии</span><span class="sxs-lookup"><span data-stu-id="42957-158">Comments</span></span>                                                                                                                                                                                                                        |
|---------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="42957-159">**SPLREG_ALLOW_USER_MANAGEFORMS**</span><span class="sxs-lookup"><span data-stu-id="42957-159">**SPLREG_ALLOW_USER_MANAGEFORMS**</span></span>                                | <span data-ttu-id="42957-160">Windows XP с пакетом обновления 2 (SP2) и более поздние версии</span><span class="sxs-lookup"><span data-stu-id="42957-160">Windows XP with Service Pack 2 (SP2) and later</span></span><br/> <span data-ttu-id="42957-161">Windows Server 2003 с пакетом обновления 1 (SP1) и более поздние версии</span><span class="sxs-lookup"><span data-stu-id="42957-161">Windows Server 2003 with Service Pack 1 (SP1) and later</span></span><br/>                                                                                                    |
| <span data-ttu-id="42957-162">**SPLREG_BEEP_ENABLED**</span><span class="sxs-lookup"><span data-stu-id="42957-162">**SPLREG_BEEP_ENABLED**</span></span>                                           |                                                                                                                                                                                                                                 |
| <span data-ttu-id="42957-163">**SPLREG_DEFAULT_SPOOL_DIRECTORY**</span><span class="sxs-lookup"><span data-stu-id="42957-163">**SPLREG_DEFAULT_SPOOL_DIRECTORY**</span></span>                               |                                                                                                                                                                                                                                 |
| <span data-ttu-id="42957-164">**SPLREG_EVENT_LOG**</span><span class="sxs-lookup"><span data-stu-id="42957-164">**SPLREG_EVENT_LOG**</span></span>                                              |                                                                                                                                                                                                                                 |
| <span data-ttu-id="42957-165">**SPLREG_NET_POPUP**</span><span class="sxs-lookup"><span data-stu-id="42957-165">**SPLREG_NET_POPUP**</span></span>                                              | <span data-ttu-id="42957-166">Не поддерживается в Windows Server 2003 и более поздних версиях</span><span class="sxs-lookup"><span data-stu-id="42957-166">Not supported in Windows Server 2003 and later</span></span><br/>                                                                                                                                                                       |
| <span data-ttu-id="42957-167">**SPLREG_PORT_THREAD_PRIORITY_DEFAULT**</span><span class="sxs-lookup"><span data-stu-id="42957-167">**SPLREG_PORT_THREAD_PRIORITY_DEFAULT**</span></span>                         |                                                                                                                                                                                                                                 |
| <span data-ttu-id="42957-168">**SPLREG_PORT_THREAD_PRIORITY**</span><span class="sxs-lookup"><span data-stu-id="42957-168">**SPLREG_PORT_THREAD_PRIORITY**</span></span>                                  |                                                                                                                                                                                                                                 |
| <span data-ttu-id="42957-169">**SPLREG_PRINT_DRIVER_ISOLATION_GROUPS**</span><span class="sxs-lookup"><span data-stu-id="42957-169">**SPLREG_PRINT_DRIVER_ISOLATION_GROUPS**</span></span>                        | <span data-ttu-id="42957-170">Windows 7 и более поздние версии</span><span class="sxs-lookup"><span data-stu-id="42957-170">Windows 7 and later</span></span><br/>                                                                                                                                                                                                  |
| <span data-ttu-id="42957-171">**SPLREG_PRINT_DRIVER_ISOLATION_TIME_BEFORE_RECYCLE**</span><span class="sxs-lookup"><span data-stu-id="42957-171">**SPLREG_PRINT_DRIVER_ISOLATION_TIME_BEFORE_RECYCLE**</span></span>         | <span data-ttu-id="42957-172">Windows 7 и более поздние версии</span><span class="sxs-lookup"><span data-stu-id="42957-172">Windows 7 and later</span></span><br/>                                                                                                                                                                                                  |
| <span data-ttu-id="42957-173">**SPLREG_PRINT_DRIVER_ISOLATION_MAX_OBJECTS_BEFORE_RECYCLE**</span><span class="sxs-lookup"><span data-stu-id="42957-173">**SPLREG_PRINT_DRIVER_ISOLATION_MAX_OBJECTS_BEFORE_RECYCLE**</span></span> | <span data-ttu-id="42957-174">Windows 7 и более поздние версии</span><span class="sxs-lookup"><span data-stu-id="42957-174">Windows 7 and later</span></span><br/>                                                                                                                                                                                                  |
| <span data-ttu-id="42957-175">**SPLREG_PRINT_DRIVER_ISOLATION_IDLE_TIMEOUT**</span><span class="sxs-lookup"><span data-stu-id="42957-175">**SPLREG_PRINT_DRIVER_ISOLATION_IDLE_TIMEOUT**</span></span>                 | <span data-ttu-id="42957-176">Windows 7 и более поздние версии</span><span class="sxs-lookup"><span data-stu-id="42957-176">Windows 7 and later</span></span><br/>                                                                                                                                                                                                  |
| <span data-ttu-id="42957-177">**SPLREG_PRINT_DRIVER_ISOLATION_EXECUTION_POLICY**</span><span class="sxs-lookup"><span data-stu-id="42957-177">**SPLREG_PRINT_DRIVER_ISOLATION_EXECUTION_POLICY**</span></span>             | <span data-ttu-id="42957-178">Windows 7 и более поздние версии</span><span class="sxs-lookup"><span data-stu-id="42957-178">Windows 7 and later</span></span><br/>                                                                                                                                                                                                  |
| <span data-ttu-id="42957-179">**SPLREG_PRINT_DRIVER_ISOLATION_OVERRIDE_POLICY**</span><span class="sxs-lookup"><span data-stu-id="42957-179">**SPLREG_PRINT_DRIVER_ISOLATION_OVERRIDE_POLICY**</span></span>              | <span data-ttu-id="42957-180">Windows 7 и более поздние версии</span><span class="sxs-lookup"><span data-stu-id="42957-180">Windows 7 and later</span></span><br/>                                                                                                                                                                                                  |
| <span data-ttu-id="42957-181">**SPLREG_RETRY_POPUP**</span><span class="sxs-lookup"><span data-stu-id="42957-181">**SPLREG_RETRY_POPUP**</span></span>                                            | <span data-ttu-id="42957-182">При успешном возвращении *pData* содержит 1, если на сервере настроено повторное открытие всплывающих окон для всех заданий, или значение 0, если сервер не пытается повторно открывать всплывающие окна для всех заданий.</span><span class="sxs-lookup"><span data-stu-id="42957-182">On successful return, *pData* contains 1 if server is set to retry pop-up windows for all jobs, or 0 if server does not retry pop-up windows for all jobs.</span></span><br/> <span data-ttu-id="42957-183">Не поддерживается в Windows Server 2003 и более поздних версиях</span><span class="sxs-lookup"><span data-stu-id="42957-183">Not supported in Windows Server 2003 and later</span></span><br/> |
| <span data-ttu-id="42957-184">**SPLREG_SCHEDULER_THREAD_PRIORITY**</span><span class="sxs-lookup"><span data-stu-id="42957-184">**SPLREG_SCHEDULER_THREAD_PRIORITY**</span></span>                             |                                                                                                                                                                                                                                 |
| <span data-ttu-id="42957-185">**SPLREG_SCHEDULER_THREAD_PRIORITY_DEFAULT**</span><span class="sxs-lookup"><span data-stu-id="42957-185">**SPLREG_SCHEDULER_THREAD_PRIORITY_DEFAULT**</span></span>                    |                                                                                                                                                                                                                                 |
| <span data-ttu-id="42957-186">**SPLREG_WEBSHAREMGMT**</span><span class="sxs-lookup"><span data-stu-id="42957-186">**SPLREG_WEBSHAREMGMT**</span></span>                                            | <span data-ttu-id="42957-187">Windows Server 2003 и более поздние версии</span><span class="sxs-lookup"><span data-stu-id="42957-187">Windows Server 2003 and later</span></span><br/>                                                                                                                                                                                        |



 

<span data-ttu-id="42957-188">Передача одного из следующих стандартных значений в качестве *пвалуенаме* задает режим печати пула при возникновении ошибки.</span><span class="sxs-lookup"><span data-stu-id="42957-188">Passing one of the following predefined values as *pValueName* sets the pool printing behavior when an error occurs.</span></span>



| <span data-ttu-id="42957-189">Значение</span><span class="sxs-lookup"><span data-stu-id="42957-189">Value</span></span>                                       | <span data-ttu-id="42957-190">Комментарии</span><span class="sxs-lookup"><span data-stu-id="42957-190">Comments</span></span>                                                                                                                                                                                              |
|---------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="42957-191">**SPLREG_RESTART_JOB_ON_POOL_ERROR**</span><span class="sxs-lookup"><span data-stu-id="42957-191">**SPLREG_RESTART_JOB_ON_POOL_ERROR**</span></span>   | <span data-ttu-id="42957-192">Значение *pData* указывает время в секундах, когда задание перезапускается на другом порте после возникновения ошибки.</span><span class="sxs-lookup"><span data-stu-id="42957-192">The value of *pData* indicates the time, in seconds, when a job is restarted on another port after an error occurs.</span></span> <span data-ttu-id="42957-193">Этот параметр используется с **SPLREG_RESTART_JOB_ON_POOL_ENABLED**.</span><span class="sxs-lookup"><span data-stu-id="42957-193">This setting is used with **SPLREG_RESTART_JOB_ON_POOL_ENABLED**.</span></span><br/> |
| <span data-ttu-id="42957-194">**SPLREG_RESTART_JOB_ON_POOL_ENABLED**</span><span class="sxs-lookup"><span data-stu-id="42957-194">**SPLREG_RESTART_JOB_ON_POOL_ENABLED**</span></span> | <span data-ttu-id="42957-195">Ненулевое значение в *pData* указывает, что **SPLREG_RESTART_JOB_ON_POOL_ERROR** включен.</span><span class="sxs-lookup"><span data-stu-id="42957-195">A nonzero value in *pData* indicates that **SPLREG_RESTART_JOB_ON_POOL_ERROR** is enabled.</span></span><br/>                                                                                            |



 

<span data-ttu-id="42957-196">Время, указанное в **SPLREG_RESTART_JOB_ON_POOL_ERROR** , является минимальным временем.</span><span class="sxs-lookup"><span data-stu-id="42957-196">The time specified in **SPLREG_RESTART_JOB_ON_POOL_ERROR** is a minimum time.</span></span> <span data-ttu-id="42957-197">Фактическое время может быть больше, в зависимости от следующих параметров монитора портов, которые являются значениями реестра в этом разделе реестра:</span><span class="sxs-lookup"><span data-stu-id="42957-197">The actual time can be longer, depending on the following port monitor settings, which are registry values under this registry key:</span></span>

<span data-ttu-id="42957-198">**HKLM \\ System CurrentControlSet Control Monitoring MONITORS \\ \\ \\ \\ \\ < *мониторнаме* > \\ ports**</span><span class="sxs-lookup"><span data-stu-id="42957-198">**HKLM\\SYSTEM\\CurrentControlSet\\Control\\Print\\Monitors\\<*MonitorName*>\\Ports**</span></span>

<span data-ttu-id="42957-199">Чтобы задать эти значения, вызовите функцию [**RegSetValueEx**](/windows/win32/api/winreg/nf-winreg-regsetvaluea) .</span><span class="sxs-lookup"><span data-stu-id="42957-199">Call the [**RegSetValueEx**](/windows/win32/api/winreg/nf-winreg-regsetvaluea) function to set these values.</span></span>



| <span data-ttu-id="42957-200">Параметр монитора порта</span><span class="sxs-lookup"><span data-stu-id="42957-200">Port monitor setting</span></span>     | <span data-ttu-id="42957-201">Тип данных</span><span class="sxs-lookup"><span data-stu-id="42957-201">Data type</span></span>      | <span data-ttu-id="42957-202">Значение</span><span class="sxs-lookup"><span data-stu-id="42957-202">Meaning</span></span>                                                                                                        |
|--------------------------|----------------|----------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="42957-203">**статусупдатинаблед**</span><span class="sxs-lookup"><span data-stu-id="42957-203">**StatusUpdateEnabled**</span></span>  | <span data-ttu-id="42957-204">**REG_DWORD**</span><span class="sxs-lookup"><span data-stu-id="42957-204">**REG_DWORD**</span></span> | <span data-ttu-id="42957-205">При ненулевом значении разрешает монитору портов обновлять Диспетчер очереди с состоянием порта.</span><span class="sxs-lookup"><span data-stu-id="42957-205">If a nonzero value, enables the port monitor to update the spooler with the port status.</span></span><br/>            |
| <span data-ttu-id="42957-206">**статусупдатеинтервал**</span><span class="sxs-lookup"><span data-stu-id="42957-206">**StatusUpdateInterval**</span></span> | <span data-ttu-id="42957-207">**REG_DWORD**</span><span class="sxs-lookup"><span data-stu-id="42957-207">**REG_DWORD**</span></span> | <span data-ttu-id="42957-208">Указывает интервал (в минутах), в течение которого монитор порта обновляет Диспетчер очереди с состоянием порта.</span><span class="sxs-lookup"><span data-stu-id="42957-208">Specifies the interval, in minutes, when the port monitor updates the spooler with the port status.</span></span><br/> |



 

<span data-ttu-id="42957-209">Чтобы диспетчер очереди перенаправлял задания на следующий доступный принтер в пуле (если задание печати не печатается в течение заданного времени), монитор порта должен поддерживать протокол SNMP, а сетевые порты в пуле должны быть настроены как "SNMP Status Enabled".</span><span class="sxs-lookup"><span data-stu-id="42957-209">To ensure that the spooler redirects jobs to the next available printer in the pool (when the print job is not printed within the set time), the port monitor must support SNMP and the network ports in the pool must be configured as "SNMP status enabled."</span></span> <span data-ttu-id="42957-210">Монитор порта, поддерживающий SNMP, является стандартным монитором порта TCP/IP.</span><span class="sxs-lookup"><span data-stu-id="42957-210">The port monitor that supports SNMP is Standard TCP/IP port monitor.</span></span>

<span data-ttu-id="42957-211">В Windows 7 и более поздних версиях Windows задания печати, отправленные на сервер печати, по умолчанию подготавливаются к просмотру на клиенте.</span><span class="sxs-lookup"><span data-stu-id="42957-211">In Windows 7 and later versions of Windows, print jobs that are sent to a print server are rendered on the client by default.</span></span> <span data-ttu-id="42957-212">Отрисовку заданий печати на стороне клиента можно настроить, задав для параметра *пкэйнаме* значение "принтердривердата" и *пвалуенаме* в качестве значения параметра в следующей таблице.</span><span class="sxs-lookup"><span data-stu-id="42957-212">Client-side rendering of print jobs can be configured by setting *pKeyName* to "PrinterDriverData" and *pValueName* to the setting value in the following table.</span></span>



| <span data-ttu-id="42957-213">Параметр</span><span class="sxs-lookup"><span data-stu-id="42957-213">Setting</span></span>                      | <span data-ttu-id="42957-214">Тип данных</span><span class="sxs-lookup"><span data-stu-id="42957-214">Data type</span></span>      | <span data-ttu-id="42957-215">Описание</span><span class="sxs-lookup"><span data-stu-id="42957-215">Description</span></span>                                                                                                                                                                                                                                                                                                                                                                                                       |
|------------------------------|----------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="42957-216">**емфдеспулингсеттинг**</span><span class="sxs-lookup"><span data-stu-id="42957-216">**EMFDespoolingSetting**</span></span>     | <span data-ttu-id="42957-217">**REG_DWORD**</span><span class="sxs-lookup"><span data-stu-id="42957-217">**REG_DWORD**</span></span> | <span data-ttu-id="42957-218">Значение 0 или, если это значение отсутствует в реестре, включает отрисовку заданий печати на стороне клиента по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="42957-218">A value of 0, or if this value is not present in the registry, enables the default client-side rendering of print jobs.</span></span><br/> <span data-ttu-id="42957-219">Значение 1 отключает отрисовку заданий печати на стороне клиента.</span><span class="sxs-lookup"><span data-stu-id="42957-219">A value of 1 disables client-side rendering of print jobs.</span></span><br/>                                                                                                                                                                                                          |
| <span data-ttu-id="42957-220">**форцеклиентсидерендеринг**</span><span class="sxs-lookup"><span data-stu-id="42957-220">**ForceClientSideRendering**</span></span> | <span data-ttu-id="42957-221">**REG_DWORD**</span><span class="sxs-lookup"><span data-stu-id="42957-221">**REG_DWORD**</span></span> | <span data-ttu-id="42957-222">Значение 0 или, если это значение отсутствует в реестре, приведет к отображению заданий печати на клиенте.</span><span class="sxs-lookup"><span data-stu-id="42957-222">A value of 0, or if this value is not present in the registry, will cause the print jobs to be rendered on the client.</span></span> <span data-ttu-id="42957-223">Если задание печати не может быть визуализировано на клиенте, оно будет подготовлено к просмотру на сервере.</span><span class="sxs-lookup"><span data-stu-id="42957-223">If a print job cannot be rendered on the client, it will be rendered on the server.</span></span> <span data-ttu-id="42957-224">Если задание печати не может быть подготовлено к просмотру на сервере, оно завершится ошибкой.</span><span class="sxs-lookup"><span data-stu-id="42957-224">If a print job cannot be rendered on the server, it will fail.</span></span><br/> <span data-ttu-id="42957-225">Значение 1 будет отображать задания печати на клиенте.</span><span class="sxs-lookup"><span data-stu-id="42957-225">A value of 1 will render print jobs on the client.</span></span> <span data-ttu-id="42957-226">Если задание печати не может быть визуализировано на клиенте, оно завершится ошибкой.</span><span class="sxs-lookup"><span data-stu-id="42957-226">If a print job cannot be rendered on the client, it will fail.</span></span><br/> |



 

## <a name="requirements"></a><span data-ttu-id="42957-227">Требования</span><span class="sxs-lookup"><span data-stu-id="42957-227">Requirements</span></span>



| <span data-ttu-id="42957-228">Требование</span><span class="sxs-lookup"><span data-stu-id="42957-228">Requirement</span></span> | <span data-ttu-id="42957-229">Значение</span><span class="sxs-lookup"><span data-stu-id="42957-229">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="42957-230">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="42957-230">Minimum supported client</span></span><br/> | <span data-ttu-id="42957-231">Windows 2000 Professional \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="42957-231">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                                |
| <span data-ttu-id="42957-232">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="42957-232">Minimum supported server</span></span><br/> | <span data-ttu-id="42957-233">Windows 2000 Server \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="42957-233">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                      |
| <span data-ttu-id="42957-234">Заголовок</span><span class="sxs-lookup"><span data-stu-id="42957-234">Header</span></span><br/>                   | <dl> <span data-ttu-id="42957-235"><dt>Винспул. h (включение Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="42957-235"><dt>Winspool.h (include Windows.h)</dt></span></span> </dl> |
| <span data-ttu-id="42957-236">Библиотека</span><span class="sxs-lookup"><span data-stu-id="42957-236">Library</span></span><br/>                  | <dl> <span data-ttu-id="42957-237"><dt>Винспул. lib</dt></span><span class="sxs-lookup"><span data-stu-id="42957-237"><dt>Winspool.lib</dt></span></span> </dl>                   |
| <span data-ttu-id="42957-238">DLL</span><span class="sxs-lookup"><span data-stu-id="42957-238">DLL</span></span><br/>                      | <dl> <span data-ttu-id="42957-239"><dt>Винспул. drv</dt></span><span class="sxs-lookup"><span data-stu-id="42957-239"><dt>Winspool.drv</dt></span></span> </dl>                   |
| <span data-ttu-id="42957-240">Имя в кодировке Юникод и ANSI</span><span class="sxs-lookup"><span data-stu-id="42957-240">Unicode and ANSI names</span></span><br/>   | <span data-ttu-id="42957-241">**Сетпринтердатаексв** (Юникод) и **сетпринтердатаекса** (ANSI)</span><span class="sxs-lookup"><span data-stu-id="42957-241">**SetPrinterDataExW** (Unicode) and **SetPrinterDataExA** (ANSI)</span></span><br/>                               |



## <a name="see-also"></a><span data-ttu-id="42957-242">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="42957-242">See also</span></span>

<dl> <dt>

[<span data-ttu-id="42957-243">Вывод на печать</span><span class="sxs-lookup"><span data-stu-id="42957-243">Printing</span></span>](printdocs-printing.md)
</dt> <dt>

[<span data-ttu-id="42957-244">Функции API очереди печати принтера</span><span class="sxs-lookup"><span data-stu-id="42957-244">Print Spooler API Functions</span></span>](printing-and-print-spooler-functions.md)
</dt> <dt>

[<span data-ttu-id="42957-245">**жетпринтердатаекс**</span><span class="sxs-lookup"><span data-stu-id="42957-245">**GetPrinterDataEx**</span></span>](getprinterdataex.md)
</dt> <dt>

[<span data-ttu-id="42957-246">**опенпринтер**</span><span class="sxs-lookup"><span data-stu-id="42957-246">**OpenPrinter**</span></span>](openprinter.md)
</dt> <dt>

[<span data-ttu-id="42957-247">**сетпринтер**</span><span class="sxs-lookup"><span data-stu-id="42957-247">**SetPrinter**</span></span>](setprinter.md)
</dt> <dt>

[<span data-ttu-id="42957-248">**PRINTER_INFO_7**</span><span class="sxs-lookup"><span data-stu-id="42957-248">**PRINTER_INFO_7**</span></span>](printer-info-7.md)
</dt> </dl>

 

