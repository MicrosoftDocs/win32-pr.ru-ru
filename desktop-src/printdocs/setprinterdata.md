---
description: Функция Сетпринтердата задает данные конфигурации для принтера или сервера печати.
ms.assetid: 16072de9-98fb-4ada-8216-180b64cf44c8
title: Функция Сетпринтердата (Винспул. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SetPrinterData
- SetPrinterDataA
- SetPrinterDataW
api_type:
- DllExport
api_location:
- Winspool.drv
- Ext-MS-Win-Printer-WinSpool-l1-1-2.dll
- Ext-MS-Win-Printer-WinSpool-L1-1-3.dll
ms.openlocfilehash: 36af84fe665d68fd7996a0b81fbbf291314cc69e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "103909368"
---
# <a name="setprinterdata-function"></a><span data-ttu-id="3dba5-103">Функция Сетпринтердата</span><span class="sxs-lookup"><span data-stu-id="3dba5-103">SetPrinterData function</span></span>

<span data-ttu-id="3dba5-104">Функция **сетпринтердата** задает данные конфигурации для принтера или сервера печати.</span><span class="sxs-lookup"><span data-stu-id="3dba5-104">The **SetPrinterData** function sets the configuration data for a printer or print server.</span></span>

<span data-ttu-id="3dba5-105">Чтобы указать раздел реестра, в котором должны храниться данные, вызовите функцию [**сетпринтердатаекс**](setprinterdataex.md) .</span><span class="sxs-lookup"><span data-stu-id="3dba5-105">To specify the registry key under which to store the data, call the [**SetPrinterDataEx**](setprinterdataex.md) function.</span></span> <span data-ttu-id="3dba5-106">Вызов **сетпринтердата** эквивалентен вызову функции **сетпринтердатаекс** с параметром *Пкэйнаме* , имеющим значение "принтердривердата".</span><span class="sxs-lookup"><span data-stu-id="3dba5-106">Calling **SetPrinterData** is equivalent to calling the **SetPrinterDataEx** function with the *pKeyName* parameter set to "PrinterDriverData".</span></span>

## <a name="syntax"></a><span data-ttu-id="3dba5-107">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="3dba5-107">Syntax</span></span>


```C++
DWORD SetPrinterData(
  _In_ HANDLE hPrinter,
  _In_ LPTSTR pValueName,
  _In_ DWORD  Type,
  _In_ LPBYTE pData,
  _In_ DWORD  cbData
);
```



## <a name="parameters"></a><span data-ttu-id="3dba5-108">Параметры</span><span class="sxs-lookup"><span data-stu-id="3dba5-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="3dba5-109">*хпринтер* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="3dba5-109">*hPrinter* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="3dba5-110">Маркер принтера или сервера печати, для которого функция задает данные конфигурации.</span><span class="sxs-lookup"><span data-stu-id="3dba5-110">A handle to the printer or print server for which the function sets configuration data.</span></span> <span data-ttu-id="3dba5-111">Используйте функцию [**опенпринтер**](openprinter.md), [**OpenPrinter2**](openprinter2.md)или [**аддпринтер**](addprinter.md) для получения маркера принтера.</span><span class="sxs-lookup"><span data-stu-id="3dba5-111">Use the [**OpenPrinter**](openprinter.md), [**OpenPrinter2**](openprinter2.md), or [**AddPrinter**](addprinter.md) function to retrieve a printer handle.</span></span>

</dd> <dt>

<span data-ttu-id="3dba5-112">*пвалуенаме* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="3dba5-112">*pValueName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="3dba5-113">Указатель на строку, завершающуюся нулем, которая определяет данные для задания.</span><span class="sxs-lookup"><span data-stu-id="3dba5-113">A pointer to a null-terminated string that identifies the data to set.</span></span>

<span data-ttu-id="3dba5-114">Для принтеров эта строка представляет собой имя значения реестра в разделе "Принтердривердата" принтера в реестре.</span><span class="sxs-lookup"><span data-stu-id="3dba5-114">For printers, this string is the name of a registry value under the printer's "PrinterDriverData" key in the registry.</span></span>

<span data-ttu-id="3dba5-115">Для серверов печати эта строка является одной из предопределенных строк, перечисленных в следующем разделе "Примечания".</span><span class="sxs-lookup"><span data-stu-id="3dba5-115">For print servers, this string is one of the predefined strings listed in the following Remarks section.</span></span>

</dd> <dt>

<span data-ttu-id="3dba5-116">*Тип* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="3dba5-116">*Type* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="3dba5-117">Код, указывающий тип данных, на которые указывает параметр *pData* .</span><span class="sxs-lookup"><span data-stu-id="3dba5-117">A code that indicates the type of data that the *pData* parameter points to.</span></span> <span data-ttu-id="3dba5-118">Список возможных кодов типов см. в разделе [типы значений реестра](/windows/desktop/SysInfo/registry-value-types).</span><span class="sxs-lookup"><span data-stu-id="3dba5-118">For a list of the possible type codes, see [Registry Value Types](/windows/desktop/SysInfo/registry-value-types).</span></span>

</dd> <dt>

<span data-ttu-id="3dba5-119">*pData* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="3dba5-119">*pData* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="3dba5-120">Указатель на массив байтов, содержащий данные конфигурации принтера.</span><span class="sxs-lookup"><span data-stu-id="3dba5-120">A pointer to an array of bytes that contains the printer configuration data.</span></span>

</dd> <dt>

<span data-ttu-id="3dba5-121">*cbData* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="3dba5-121">*cbData* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="3dba5-122">Размер массива в байтах.</span><span class="sxs-lookup"><span data-stu-id="3dba5-122">The size, in bytes, of the array.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="3dba5-123">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="3dba5-123">Return value</span></span>

<span data-ttu-id="3dba5-124">Если функция завершается успешно, возвращается значение **ошибки \_ Success**.</span><span class="sxs-lookup"><span data-stu-id="3dba5-124">If the function succeeds, the return value is **ERROR\_SUCCESS**.</span></span>

<span data-ttu-id="3dba5-125">Если функция завершается ошибкой, возвращается значение ошибки.</span><span class="sxs-lookup"><span data-stu-id="3dba5-125">If the function fails, the return value is an error value.</span></span>

## <a name="remarks"></a><span data-ttu-id="3dba5-126">Комментарии</span><span class="sxs-lookup"><span data-stu-id="3dba5-126">Remarks</span></span>

> [!Note]  
> <span data-ttu-id="3dba5-127">Это блокирующая или синхронная функция, которая может не возвращать значение немедленно.</span><span class="sxs-lookup"><span data-stu-id="3dba5-127">This is a blocking or synchronous function and might not return immediately.</span></span> <span data-ttu-id="3dba5-128">Скорость возврата этой функцией зависит от факторов времени выполнения, таких как состояние сети, Конфигурация сервера печати и факторы реализации драйвера принтера, которые трудно предсказать при написании приложения.</span><span class="sxs-lookup"><span data-stu-id="3dba5-128">How quickly this function returns depends on run-time factors such as network status, print server configuration, and printer driver implementation factors that are difficult to predict when writing an application.</span></span> <span data-ttu-id="3dba5-129">Вызов этой функции из потока, который управляет взаимодействием с пользовательским интерфейсом, может привести к невозможности реагирования приложения.</span><span class="sxs-lookup"><span data-stu-id="3dba5-129">Calling this function from a thread that manages interaction with the user interface could make the application appear to be unresponsive.</span></span>

 

<span data-ttu-id="3dba5-130">Чтобы получить существующие данные конфигурации для принтера, вызовите функцию [**жетпринтердатаекс**](getprinterdataex.md) или [**жетпринтердата**](getprinterdata.md) .</span><span class="sxs-lookup"><span data-stu-id="3dba5-130">To retrieve existing configuration data for a printer, call the [**GetPrinterDataEx**](getprinterdataex.md) or [**GetPrinterData**](getprinterdata.md) function.</span></span>

<span data-ttu-id="3dba5-131">Если *хпринтер* является обработчиком для сервера печати, *пвалуенаме* может указать одно из следующих предопределенных значений.</span><span class="sxs-lookup"><span data-stu-id="3dba5-131">If *hPrinter* is a handle to a print server, *pValueName* can specify one of the following predefined values.</span></span>



| <span data-ttu-id="3dba5-132">Значение</span><span class="sxs-lookup"><span data-stu-id="3dba5-132">Value</span></span>                                                               | <span data-ttu-id="3dba5-133">Комментарии</span><span class="sxs-lookup"><span data-stu-id="3dba5-133">Comments</span></span>                                                                                                                                                                                                                        |
|---------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="3dba5-134">**СПЛРЕГ \_ Разрешить \_ \_ манажеформс пользователя**</span><span class="sxs-lookup"><span data-stu-id="3dba5-134">**SPLREG\_ALLOW\_USER\_MANAGEFORMS**</span></span>                                | <span data-ttu-id="3dba5-135">Windows XP с пакетом обновления 2 (SP2) и более поздние версии</span><span class="sxs-lookup"><span data-stu-id="3dba5-135">Windows XP with Service Pack 2 (SP2) and later</span></span><br/> <span data-ttu-id="3dba5-136">Windows Server 2003 с пакетом обновления 1 (SP1) и более поздние версии</span><span class="sxs-lookup"><span data-stu-id="3dba5-136">Windows Server 2003 with Service Pack 1 (SP1) and later</span></span><br/>                                                                                                    |
| <span data-ttu-id="3dba5-137">**\_включен звуковой сигнал сплрег \_**</span><span class="sxs-lookup"><span data-stu-id="3dba5-137">**SPLREG\_BEEP\_ENABLED**</span></span>                                           |                                                                                                                                                                                                                                 |
| <span data-ttu-id="3dba5-138">**СПЛРЕГ \_ \_ Каталог очереди печати по умолчанию \_**</span><span class="sxs-lookup"><span data-stu-id="3dba5-138">**SPLREG\_DEFAULT\_SPOOL\_DIRECTORY**</span></span>                               |                                                                                                                                                                                                                                 |
| <span data-ttu-id="3dba5-139">**\_журнал событий \_ сплрег**</span><span class="sxs-lookup"><span data-stu-id="3dba5-139">**SPLREG\_EVENT\_LOG**</span></span>                                              |                                                                                                                                                                                                                                 |
| <span data-ttu-id="3dba5-140">**\_ \_ всплывающее меню сплрег NET**</span><span class="sxs-lookup"><span data-stu-id="3dba5-140">**SPLREG\_NET\_POPUP**</span></span>                                              | <span data-ttu-id="3dba5-141">Не поддерживается в Windows Server 2003 и более поздних версиях</span><span class="sxs-lookup"><span data-stu-id="3dba5-141">Not supported in Windows Server 2003 and later</span></span><br/>                                                                                                                                                                       |
| <span data-ttu-id="3dba5-142">**\_ \_ приоритет потока портов \_ сплрег \_ по умолчанию**</span><span class="sxs-lookup"><span data-stu-id="3dba5-142">**SPLREG\_PORT\_THREAD\_PRIORITY\_DEFAULT**</span></span>                         |                                                                                                                                                                                                                                 |
| <span data-ttu-id="3dba5-143">**\_ \_ приоритет потока портов \_ сплрег**</span><span class="sxs-lookup"><span data-stu-id="3dba5-143">**SPLREG\_PORT\_THREAD\_PRIORITY**</span></span>                                  |                                                                                                                                                                                                                                 |
| <span data-ttu-id="3dba5-144">**\_ \_ \_ группы изоляции драйвера печати \_ сплрег**</span><span class="sxs-lookup"><span data-stu-id="3dba5-144">**SPLREG\_PRINT\_DRIVER\_ISOLATION\_GROUPS**</span></span>                        | <span data-ttu-id="3dba5-145">Windows 7 и более поздние версии</span><span class="sxs-lookup"><span data-stu-id="3dba5-145">Windows 7 and later</span></span><br/>                                                                                                                                                                                                  |
| <span data-ttu-id="3dba5-146">**СПЛРЕГ \_ \_ \_ время изоляции драйвера \_ печати \_ перед \_ повторным запуском**</span><span class="sxs-lookup"><span data-stu-id="3dba5-146">**SPLREG\_PRINT\_DRIVER\_ISOLATION\_TIME\_BEFORE\_RECYCLE**</span></span>         | <span data-ttu-id="3dba5-147">Windows 7 и более поздние версии</span><span class="sxs-lookup"><span data-stu-id="3dba5-147">Windows 7 and later</span></span><br/>                                                                                                                                                                                                  |
| <span data-ttu-id="3dba5-148">**СПЛРЕГ \_ \_ \_ \_ Максимальное число объектов изоляции драйвера печати \_ \_ перед \_ повторным запуском**</span><span class="sxs-lookup"><span data-stu-id="3dba5-148">**SPLREG\_PRINT\_DRIVER\_ISOLATION\_MAX\_OBJECTS\_BEFORE\_RECYCLE**</span></span> | <span data-ttu-id="3dba5-149">Windows 7 и более поздние версии</span><span class="sxs-lookup"><span data-stu-id="3dba5-149">Windows 7 and later</span></span><br/>                                                                                                                                                                                                  |
| <span data-ttu-id="3dba5-150">**СПЛРЕГ \_ \_ \_ \_ время ожидания простоя для изоляции драйвера печати \_**</span><span class="sxs-lookup"><span data-stu-id="3dba5-150">**SPLREG\_PRINT\_DRIVER\_ISOLATION\_IDLE\_TIMEOUT**</span></span>                 | <span data-ttu-id="3dba5-151">Windows 7 и более поздние версии</span><span class="sxs-lookup"><span data-stu-id="3dba5-151">Windows 7 and later</span></span><br/>                                                                                                                                                                                                  |
| <span data-ttu-id="3dba5-152">**\_ \_ \_ \_ Политика выполнения изоляции драйвера печати \_ сплрег**</span><span class="sxs-lookup"><span data-stu-id="3dba5-152">**SPLREG\_PRINT\_DRIVER\_ISOLATION\_EXECUTION\_POLICY**</span></span>             | <span data-ttu-id="3dba5-153">Windows 7 и более поздние версии</span><span class="sxs-lookup"><span data-stu-id="3dba5-153">Windows 7 and later</span></span><br/>                                                                                                                                                                                                  |
| <span data-ttu-id="3dba5-154">**\_ \_ \_ Политика переопределения режима изоляции \_ драйвера \_ печати сплрег**</span><span class="sxs-lookup"><span data-stu-id="3dba5-154">**SPLREG\_PRINT\_DRIVER\_ISOLATION\_OVERRIDE\_POLICY**</span></span>              | <span data-ttu-id="3dba5-155">Windows 7 и более поздние версии</span><span class="sxs-lookup"><span data-stu-id="3dba5-155">Windows 7 and later</span></span><br/>                                                                                                                                                                                                  |
| <span data-ttu-id="3dba5-156">**\_всплывающее окно повторной попытки сплрег \_**</span><span class="sxs-lookup"><span data-stu-id="3dba5-156">**SPLREG\_RETRY\_POPUP**</span></span>                                            | <span data-ttu-id="3dba5-157">При успешном возвращении *pData* содержит 1, если на сервере настроено повторное открытие всплывающих окон для всех заданий, или значение 0, если сервер не пытается повторно открывать всплывающие окна для всех заданий.</span><span class="sxs-lookup"><span data-stu-id="3dba5-157">On successful return, *pData* contains 1 if server is set to retry pop-up windows for all jobs, or 0 if server does not retry pop-up windows for all jobs.</span></span><br/> <span data-ttu-id="3dba5-158">Не поддерживается в Windows Server 2003 и более поздних версиях</span><span class="sxs-lookup"><span data-stu-id="3dba5-158">Not supported in Windows Server 2003 and later</span></span><br/> |
| <span data-ttu-id="3dba5-159">**\_приоритет потока планировщика сплрег \_ \_**</span><span class="sxs-lookup"><span data-stu-id="3dba5-159">**SPLREG\_SCHEDULER\_THREAD\_PRIORITY**</span></span>                             |                                                                                                                                                                                                                                 |
| <span data-ttu-id="3dba5-160">**\_приоритет потока планировщика сплрег \_ \_ \_ по умолчанию**</span><span class="sxs-lookup"><span data-stu-id="3dba5-160">**SPLREG\_SCHEDULER\_THREAD\_PRIORITY\_DEFAULT**</span></span>                    |                                                                                                                                                                                                                                 |
| <span data-ttu-id="3dba5-161">**СПЛРЕГ \_ вебшаремгмт**</span><span class="sxs-lookup"><span data-stu-id="3dba5-161">**SPLREG\_WEBSHAREMGMT**</span></span>                                            | <span data-ttu-id="3dba5-162">Windows Server 2003 и более поздние версии</span><span class="sxs-lookup"><span data-stu-id="3dba5-162">Windows Server 2003 and later</span></span><br/>                                                                                                                                                                                        |



 

<span data-ttu-id="3dba5-163">Следующие значения *пвалуенаме* определяют режим печати пула при возникновении ошибки.</span><span class="sxs-lookup"><span data-stu-id="3dba5-163">The following values of *pValueName* determine the pool printing behavior when an error occurs.</span></span>



| <span data-ttu-id="3dba5-164">Значение</span><span class="sxs-lookup"><span data-stu-id="3dba5-164">Value</span></span>                                       | <span data-ttu-id="3dba5-165">Комментарии</span><span class="sxs-lookup"><span data-stu-id="3dba5-165">Comments</span></span>                                                                                                                                                                                              |
|---------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="3dba5-166">**\_сбой задания перезапуска сплрег \_ \_ при \_ \_ ошибке пула**</span><span class="sxs-lookup"><span data-stu-id="3dba5-166">**SPLREG\_RESTART\_JOB\_ON\_POOL\_ERROR**</span></span>   | <span data-ttu-id="3dba5-167">Значение *pData* указывает время в секундах, когда задание перезапускается на другом порте после возникновения ошибки.</span><span class="sxs-lookup"><span data-stu-id="3dba5-167">The value of *pData* indicates the time, in seconds, when a job is restarted on another port after an error occurs.</span></span> <span data-ttu-id="3dba5-168">Этот параметр используется при **\_ \_ \_ \_ \_ включении задания перезапуска сплрег в пуле**.</span><span class="sxs-lookup"><span data-stu-id="3dba5-168">This setting is used with **SPLREG\_RESTART\_JOB\_ON\_POOL\_ENABLED**.</span></span><br/> |
| <span data-ttu-id="3dba5-169">**\_Задание перезапуска сплрег \_ \_ в \_ пуле \_ включено**</span><span class="sxs-lookup"><span data-stu-id="3dba5-169">**SPLREG\_RESTART\_JOB\_ON\_POOL\_ENABLED**</span></span> | <span data-ttu-id="3dba5-170">Ненулевое значение в *pData* указывает, что включено **\_ Задание перезапуска сплрег \_ \_ при \_ \_ ошибке пула** .</span><span class="sxs-lookup"><span data-stu-id="3dba5-170">A nonzero value in *pData* indicates that **SPLREG\_RESTART\_JOB\_ON\_POOL\_ERROR** is enabled.</span></span><br/>                                                                                            |



 

<span data-ttu-id="3dba5-171">Время, указанное в **\_ задании перезапуска сплрег \_ \_ в случае \_ \_ ошибки пула** , является минимальным временем.</span><span class="sxs-lookup"><span data-stu-id="3dba5-171">The time specified in **SPLREG\_RESTART\_JOB\_ON\_POOL\_ERROR** is a minimum time.</span></span> <span data-ttu-id="3dba5-172">Фактическое время может быть больше, в зависимости от следующих параметров монитора портов, которые являются значениями реестра в этом разделе реестра:</span><span class="sxs-lookup"><span data-stu-id="3dba5-172">The actual time can be longer, depending on the following port monitor settings, which are registry values under this registry key:</span></span>

<span data-ttu-id="3dba5-173">**HKLM \\ System CurrentControlSet Control Monitoring MONITORS \\ \\ \\ \\ \\ < *мониторнаме* > \\ ports**</span><span class="sxs-lookup"><span data-stu-id="3dba5-173">**HKLM\\SYSTEM\\CurrentControlSet\\Control\\Print\\Monitors\\<*MonitorName*>\\Ports**</span></span>

<span data-ttu-id="3dba5-174">Чтобы задать эти значения, вызовите функцию [**RegSetValueEx**](/windows/win32/api/winreg/nf-winreg-regsetvaluea) .</span><span class="sxs-lookup"><span data-stu-id="3dba5-174">Call the [**RegSetValueEx**](/windows/win32/api/winreg/nf-winreg-regsetvaluea) function to set these values.</span></span>



| <span data-ttu-id="3dba5-175">Параметр монитора порта</span><span class="sxs-lookup"><span data-stu-id="3dba5-175">Port monitor setting</span></span>     | <span data-ttu-id="3dba5-176">Тип данных</span><span class="sxs-lookup"><span data-stu-id="3dba5-176">Data type</span></span>      | <span data-ttu-id="3dba5-177">Значение</span><span class="sxs-lookup"><span data-stu-id="3dba5-177">Meaning</span></span>                                                                                                        |
|--------------------------|----------------|----------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="3dba5-178">**статусупдатинаблед**</span><span class="sxs-lookup"><span data-stu-id="3dba5-178">**StatusUpdateEnabled**</span></span>  | <span data-ttu-id="3dba5-179">**REG \_ DWORD**</span><span class="sxs-lookup"><span data-stu-id="3dba5-179">**REG\_DWORD**</span></span> | <span data-ttu-id="3dba5-180">При ненулевом значении разрешает монитору портов обновлять Диспетчер очереди с состоянием порта.</span><span class="sxs-lookup"><span data-stu-id="3dba5-180">If a nonzero value, enables the port monitor to update the spooler with the port status.</span></span><br/>            |
| <span data-ttu-id="3dba5-181">**статусупдатеинтервал**</span><span class="sxs-lookup"><span data-stu-id="3dba5-181">**StatusUpdateInterval**</span></span> | <span data-ttu-id="3dba5-182">**REG \_ DWORD**</span><span class="sxs-lookup"><span data-stu-id="3dba5-182">**REG\_DWORD**</span></span> | <span data-ttu-id="3dba5-183">Указывает интервал (в минутах), в течение которого монитор порта обновляет Диспетчер очереди с состоянием порта.</span><span class="sxs-lookup"><span data-stu-id="3dba5-183">Specifies the interval, in minutes, when the port monitor updates the spooler with the port status.</span></span><br/> |



 

<span data-ttu-id="3dba5-184">В Windows 7 и более поздних версиях Windows задания печати, отправленные на сервер печати, по умолчанию подготавливаются к просмотру на клиенте.</span><span class="sxs-lookup"><span data-stu-id="3dba5-184">In Windows 7 and later versions of Windows, print jobs that are sent to a print server are rendered on the client by default.</span></span> <span data-ttu-id="3dba5-185">Отрисовку заданий печати на стороне клиента можно настроить для каждого принтера, задав следующие значения в *пвалуенаме*.</span><span class="sxs-lookup"><span data-stu-id="3dba5-185">Client-side rendering of a print jobs can be configured for each printer by setting the following values in *pValueName*.</span></span>



| <span data-ttu-id="3dba5-186">Параметр</span><span class="sxs-lookup"><span data-stu-id="3dba5-186">Setting</span></span>                      | <span data-ttu-id="3dba5-187">Тип данных</span><span class="sxs-lookup"><span data-stu-id="3dba5-187">Data type</span></span>      | <span data-ttu-id="3dba5-188">Описание</span><span class="sxs-lookup"><span data-stu-id="3dba5-188">Description</span></span>                                                                                                                                                                                                                                                                                                                                                                                                   |
|------------------------------|----------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="3dba5-189">**емфдеспулингсеттинг**</span><span class="sxs-lookup"><span data-stu-id="3dba5-189">**EMFDespoolingSetting**</span></span>     | <span data-ttu-id="3dba5-190">**REG \_ DWORD**</span><span class="sxs-lookup"><span data-stu-id="3dba5-190">**REG\_DWORD**</span></span> | <span data-ttu-id="3dba5-191">Значение 0 или, если это значение отсутствует в реестре, включает отрисовку заданий печати на стороне клиента по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="3dba5-191">A value of 0, or if this value is not present in the registry, enables the default client-side rendering of print jobs.</span></span><br/> <span data-ttu-id="3dba5-192">Значение 1 отключает отрисовку заданий печати на стороне клиента.</span><span class="sxs-lookup"><span data-stu-id="3dba5-192">A value of 1 disables client-side rendering of print jobs.</span></span><br/>                                                                                                                                                                                                      |
| <span data-ttu-id="3dba5-193">**форцеклиентсидерендеринг**</span><span class="sxs-lookup"><span data-stu-id="3dba5-193">**ForceClientSideRendering**</span></span> | <span data-ttu-id="3dba5-194">**REG \_ DWORD**</span><span class="sxs-lookup"><span data-stu-id="3dba5-194">**REG\_DWORD**</span></span> | <span data-ttu-id="3dba5-195">Значение 0 или, если это значение отсутствует в реестре, приводит к отображению заданий печати на клиенте.</span><span class="sxs-lookup"><span data-stu-id="3dba5-195">A value of 0, or if this value is not present in the registry, causes the print jobs to be rendered on the client.</span></span> <span data-ttu-id="3dba5-196">Если задание печати не может быть визуализировано на клиенте, оно будет подготовлено к просмотру на сервере.</span><span class="sxs-lookup"><span data-stu-id="3dba5-196">If a print job cannot be rendered on the client, it will be rendered on the server.</span></span> <span data-ttu-id="3dba5-197">Если задание печати не может быть подготовлено к просмотру на сервере, оно завершится ошибкой.</span><span class="sxs-lookup"><span data-stu-id="3dba5-197">If a print job cannot be rendered on the server, it will fail.</span></span><br/> <span data-ttu-id="3dba5-198">Значение 1 будет отображать задания печати на клиенте.</span><span class="sxs-lookup"><span data-stu-id="3dba5-198">A value of 1 will render print jobs on the client.</span></span> <span data-ttu-id="3dba5-199">Если задание печати не может быть визуализировано на клиенте, оно завершится ошибкой.</span><span class="sxs-lookup"><span data-stu-id="3dba5-199">If a print job cannot be rendered on the client, it will fail.</span></span><br/> |



 

## <a name="requirements"></a><span data-ttu-id="3dba5-200">Требования</span><span class="sxs-lookup"><span data-stu-id="3dba5-200">Requirements</span></span>



| <span data-ttu-id="3dba5-201">Требование</span><span class="sxs-lookup"><span data-stu-id="3dba5-201">Requirement</span></span> | <span data-ttu-id="3dba5-202">Значение</span><span class="sxs-lookup"><span data-stu-id="3dba5-202">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="3dba5-203">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="3dba5-203">Minimum supported client</span></span><br/> | <span data-ttu-id="3dba5-204">Windows 2000 Professional \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="3dba5-204">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                                |
| <span data-ttu-id="3dba5-205">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="3dba5-205">Minimum supported server</span></span><br/> | <span data-ttu-id="3dba5-206">Windows 2000 Server \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="3dba5-206">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                      |
| <span data-ttu-id="3dba5-207">Заголовок</span><span class="sxs-lookup"><span data-stu-id="3dba5-207">Header</span></span><br/>                   | <dl> <span data-ttu-id="3dba5-208"><dt>Винспул. h (включение Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="3dba5-208"><dt>Winspool.h (include Windows.h)</dt></span></span> </dl> |
| <span data-ttu-id="3dba5-209">Библиотека</span><span class="sxs-lookup"><span data-stu-id="3dba5-209">Library</span></span><br/>                  | <dl> <span data-ttu-id="3dba5-210"><dt>Винспул. lib</dt></span><span class="sxs-lookup"><span data-stu-id="3dba5-210"><dt>Winspool.lib</dt></span></span> </dl>                   |
| <span data-ttu-id="3dba5-211">DLL</span><span class="sxs-lookup"><span data-stu-id="3dba5-211">DLL</span></span><br/>                      | <dl> <span data-ttu-id="3dba5-212"><dt>Винспул. drv</dt></span><span class="sxs-lookup"><span data-stu-id="3dba5-212"><dt>Winspool.drv</dt></span></span> </dl>                   |
| <span data-ttu-id="3dba5-213">Имя в кодировке Юникод и ANSI</span><span class="sxs-lookup"><span data-stu-id="3dba5-213">Unicode and ANSI names</span></span><br/>   | <span data-ttu-id="3dba5-214">**Сетпринтердатав** (Юникод) и **сетпринтердатаа** (ANSI)</span><span class="sxs-lookup"><span data-stu-id="3dba5-214">**SetPrinterDataW** (Unicode) and **SetPrinterDataA** (ANSI)</span></span><br/>                                   |



## <a name="see-also"></a><span data-ttu-id="3dba5-215">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="3dba5-215">See also</span></span>

<dl> <dt>

[<span data-ttu-id="3dba5-216">Вывод на печать</span><span class="sxs-lookup"><span data-stu-id="3dba5-216">Printing</span></span>](printdocs-printing.md)
</dt> <dt>

[<span data-ttu-id="3dba5-217">Функции API очереди печати принтера</span><span class="sxs-lookup"><span data-stu-id="3dba5-217">Print Spooler API Functions</span></span>](printing-and-print-spooler-functions.md)
</dt> <dt>

[<span data-ttu-id="3dba5-218">**Наложение**</span><span class="sxs-lookup"><span data-stu-id="3dba5-218">**GetPrinter**</span></span>](getprinter.md)
</dt> <dt>

[<span data-ttu-id="3dba5-219">**жетпринтердата**</span><span class="sxs-lookup"><span data-stu-id="3dba5-219">**GetPrinterData**</span></span>](getprinterdata.md)
</dt> <dt>

[<span data-ttu-id="3dba5-220">**жетпринтердатаекс**</span><span class="sxs-lookup"><span data-stu-id="3dba5-220">**GetPrinterDataEx**</span></span>](getprinterdataex.md)
</dt> <dt>

[<span data-ttu-id="3dba5-221">**опенпринтер**</span><span class="sxs-lookup"><span data-stu-id="3dba5-221">**OpenPrinter**</span></span>](openprinter.md)
</dt> <dt>

[<span data-ttu-id="3dba5-222">**сетпринтердатаекс**</span><span class="sxs-lookup"><span data-stu-id="3dba5-222">**SetPrinterDataEx**</span></span>](setprinterdataex.md)
</dt> </dl>

 

