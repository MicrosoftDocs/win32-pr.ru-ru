---
description: Функция Опенпринтер извлекает дескриптор указанного принтера или сервера печати или других типов дескрипторов в подсистеме печати.
ms.assetid: 96763220-d851-46f0-8be8-403f3356edb9
title: Функция Опенпринтер (Винспул. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- OpenPrinter
- OpenPrinterA
- OpenPrinterW
api_type:
- DllExport
api_location:
- Winspool.drv
- Ext-MS-Win-printer-Winspool-l1-1-0.dll
- Ext-MS-Win-printer-Winspool-l1-1-1.dll
- Ext-MS-Win-Printer-WinSpool-l1-1-2.dll
- Ext-MS-Win-Printer-WinSpool-L1-1-3.dll
ms.openlocfilehash: 02cd6f6b5d56eec525bd00e2feef50f4d5f07734
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "105647393"
---
# <a name="openprinter-function"></a><span data-ttu-id="959bd-103">Функция Опенпринтер</span><span class="sxs-lookup"><span data-stu-id="959bd-103">OpenPrinter function</span></span>

<span data-ttu-id="959bd-104">Функция **опенпринтер** извлекает дескриптор указанного принтера или сервера печати или других типов дескрипторов в подсистеме печати.</span><span class="sxs-lookup"><span data-stu-id="959bd-104">The **OpenPrinter** function retrieves a handle to the specified printer or print server or other types of handles in the print subsystem.</span></span>

## <a name="syntax"></a><span data-ttu-id="959bd-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="959bd-105">Syntax</span></span>


```C++
BOOL OpenPrinter(
  _In_  LPTSTR             pPrinterName,
  _Out_ LPHANDLE           phPrinter,
  _In_  LPPRINTER_DEFAULTS pDefault
);
```



## <a name="parameters"></a><span data-ttu-id="959bd-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="959bd-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="959bd-107">*ппринтернаме* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="959bd-107">*pPrinterName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="959bd-108">Указатель на строку, завершающуюся нулем, которая указывает имя принтера или сервера печати, объект принтера, Ксквмонитор или Ксквпорт.</span><span class="sxs-lookup"><span data-stu-id="959bd-108">A pointer to a null-terminated string that specifies the name of the printer or print server, the printer object, the XcvMonitor, or the XcvPort.</span></span>

<span data-ttu-id="959bd-109">Для объекта принтера используйте: Принтернаме, задание XXXX.</span><span class="sxs-lookup"><span data-stu-id="959bd-109">For a printer object use: PrinterName, Job xxxx.</span></span> <span data-ttu-id="959bd-110">Для Ксквмонитор используйте: ServerName, Ксквмонитор Мониторнаме.</span><span class="sxs-lookup"><span data-stu-id="959bd-110">For an XcvMonitor, use: ServerName, XcvMonitor MonitorName.</span></span> <span data-ttu-id="959bd-111">Для Ксквпорт используйте: ServerName, Ксквпорт Портнаме.</span><span class="sxs-lookup"><span data-stu-id="959bd-111">For an XcvPort, use: ServerName, XcvPort PortName.</span></span>

<span data-ttu-id="959bd-112">**Значение NULL** указывает на локальный сервер печати.</span><span class="sxs-lookup"><span data-stu-id="959bd-112">If **NULL**, it indicates the local printer server.</span></span>

</dd> <dt>

<span data-ttu-id="959bd-113">*фпринтер* \[ заполняет\]</span><span class="sxs-lookup"><span data-stu-id="959bd-113">*phPrinter* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="959bd-114">Указатель на переменную, которая получает маркер (не является потокобезопасным) на открытый принтер или объект сервера печати.</span><span class="sxs-lookup"><span data-stu-id="959bd-114">A pointer to a variable that receives a handle (not thread safe) to the open printer or print server object.</span></span>

<span data-ttu-id="959bd-115">Параметр *фпринтер* может возвращать маркер кскв для использования с функцией ксквдата.</span><span class="sxs-lookup"><span data-stu-id="959bd-115">The *phPrinter* parameter can return an Xcv handle for use with the XcvData function.</span></span> <span data-ttu-id="959bd-116">Дополнительные сведения о Ксквдата см. в пакете DDK.</span><span class="sxs-lookup"><span data-stu-id="959bd-116">For more information about XcvData, see the DDK.</span></span>

</dd> <dt>

<span data-ttu-id="959bd-117">*пдефаулт* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="959bd-117">*pDefault* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="959bd-118">Указатель на структуру [**\_ по умолчанию принтера**](printer-defaults.md) .</span><span class="sxs-lookup"><span data-stu-id="959bd-118">A pointer to a [**PRINTER\_DEFAULTS**](printer-defaults.md) structure.</span></span> <span data-ttu-id="959bd-119">Это значение может быть **равно NULL**.</span><span class="sxs-lookup"><span data-stu-id="959bd-119">This value can be **NULL**.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="959bd-120">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="959bd-120">Return value</span></span>

<span data-ttu-id="959bd-121">Если функция выполнена, возвращаемое значение будет ненулевым.</span><span class="sxs-lookup"><span data-stu-id="959bd-121">If the function succeeds, the return value is a nonzero value.</span></span>

<span data-ttu-id="959bd-122">Если функция выполняется неудачно, возвращается нулевое значение.</span><span class="sxs-lookup"><span data-stu-id="959bd-122">If the function fails, the return value is zero.</span></span>

## <a name="remarks"></a><span data-ttu-id="959bd-123">Комментарии</span><span class="sxs-lookup"><span data-stu-id="959bd-123">Remarks</span></span>

<span data-ttu-id="959bd-124">Не вызывайте этот метод в [**DllMain**](/windows/desktop/Dlls/dllmain).</span><span class="sxs-lookup"><span data-stu-id="959bd-124">Do not call this method in [**DllMain**](/windows/desktop/Dlls/dllmain).</span></span>

> [!Note]  
> <span data-ttu-id="959bd-125">Маркер, полученный для удаленного принтера путем вызова **опенпринтер** для удаленного принтера, обращается к принтеру через локальный кэш в службе диспетчера очереди печати.</span><span class="sxs-lookup"><span data-stu-id="959bd-125">A handle obtained for a remote printer by a call to **OpenPrinter** for a remote printer accesses the printer through a local cache in the print spooler service.</span></span> <span data-ttu-id="959bd-126">Этот кэш не является точным в режиме реального времени.</span><span class="sxs-lookup"><span data-stu-id="959bd-126">This cache isn't real-time accurate.</span></span> <span data-ttu-id="959bd-127">Чтобы получить точные данные, замените вызов Опенпринтер на [**OpenPrinter2**](openprinter2.md) с Поптионс. dwFlags установленным в \_ параметре Printer ( \_ нет \_ кэша).</span><span class="sxs-lookup"><span data-stu-id="959bd-127">To obtain accurate data, replace the OpenPrinter call with [**OpenPrinter2**](openprinter2.md) with pOptions.dwFlags set to PRINTER\_OPTION\_NO\_CACHE.</span></span> <span data-ttu-id="959bd-128">Обратите внимание, что работает только OpenPrinter2W.</span><span class="sxs-lookup"><span data-stu-id="959bd-128">Note that only OpenPrinter2W is functional.</span></span> <span data-ttu-id="959bd-129">Функция возвращает маркер принтера, который использует другие вызовы API печати и обходит локальный кэш.</span><span class="sxs-lookup"><span data-stu-id="959bd-129">The function returns a printer handle that uses other Printing API calls and bypasses the local cache.</span></span> <span data-ttu-id="959bd-130">Этот метод блокируется при ожидании сетевого подключения к удаленному принтеру, поэтому он может не возвращаться немедленно.</span><span class="sxs-lookup"><span data-stu-id="959bd-130">This method blocks while waiting for network communication with the remote printer, so it might not return immediately.</span></span> <span data-ttu-id="959bd-131">Скорость возврата этой функцией зависит от факторов времени выполнения, таких как состояние сети, Конфигурация сервера печати и факторы реализации драйвера принтера, которые трудно предсказать при написании приложения.</span><span class="sxs-lookup"><span data-stu-id="959bd-131">How quickly this function returns depends on run-time factors such as network status, print server configuration, and printer driver implementation factors that are difficult to predict when writing an application.</span></span> <span data-ttu-id="959bd-132">Вызов этой функции из потока, который управляет взаимодействием с пользовательским интерфейсом, может привести к невозможности реагирования приложения.</span><span class="sxs-lookup"><span data-stu-id="959bd-132">Calling this function from a thread that manages user interface interaction might make the application appear unresponsive.</span></span>

 

> [!Note]  
> <span data-ttu-id="959bd-133">Маркер, полученный при вызове **опенпринтер** для удаленного принтера, будет обращаться к принтеру через локальный кэш в службе диспетчера очереди печати.</span><span class="sxs-lookup"><span data-stu-id="959bd-133">A handle obtained by a call to **OpenPrinter** for a remote printer will access the printer through a local cache in the print spooler service.</span></span> <span data-ttu-id="959bd-134">Этот кэш, по своей структуре, не является точным в реальном времени.</span><span class="sxs-lookup"><span data-stu-id="959bd-134">This cache is, by design, not real time accurate.</span></span> <span data-ttu-id="959bd-135">Если необходимо получить точные данные, замените вызов **опенпринтер** параметром [**OpenPrinter2**](openprinter2.md) с *поптионс. dwFlags* , установленным в [**режим принтера, \_ \_ нет \_ кэша**](printer-options.md).</span><span class="sxs-lookup"><span data-stu-id="959bd-135">If you need to obtain accurate data, replace the **OpenPrinter** call with [**OpenPrinter2**](openprinter2.md) with *pOptions.dwFlags* set to [**PRINTER\_OPTION\_NO\_CACHE**](printer-options.md).</span></span> <span data-ttu-id="959bd-136">Обратите внимание, что работает только **OpenPrinter2W** .</span><span class="sxs-lookup"><span data-stu-id="959bd-136">Note that only **OpenPrinter2W** is functional.</span></span> <span data-ttu-id="959bd-137">Таким образом, функция возвращает маркер принтера, который делает другие вызовы API печати для обхода локального кэша.</span><span class="sxs-lookup"><span data-stu-id="959bd-137">Doing so the function returns a printer handle that makes other Printing API calls to bypass the local cache.</span></span> <span data-ttu-id="959bd-138">Обратите внимание, что этот подход будет заблокирован при ожидании сетевого подключения к удаленному принтеру, поэтому он может не возвращаться немедленно.</span><span class="sxs-lookup"><span data-stu-id="959bd-138">Note that this approach will block while waiting for the round-trip network communication to the remote printer, so it may not return immediately.</span></span> <span data-ttu-id="959bd-139">Скорость возврата этой функцией зависит от факторов времени выполнения, таких как состояние сети, Конфигурация сервера печати и факторы реализации драйвера принтера, которые трудно спрогнозировать при написании приложения.</span><span class="sxs-lookup"><span data-stu-id="959bd-139">How quickly this function returns depends on run-time factors such as network status, print server configuration, and printer driver implementation - factors that are difficult to predict when writing an application.</span></span> <span data-ttu-id="959bd-140">Поэтому вызов этой функции из потока, который управляет взаимодействием с пользовательским интерфейсом, может привести к невозможности реагирования приложения.</span><span class="sxs-lookup"><span data-stu-id="959bd-140">Therefore calling this function from a thread that manages interaction with the user interface could make the application appear to be unresponsive.</span></span>

 

<span data-ttu-id="959bd-141">Маркер, на который указывает *фпринтер* , не является потокобезопасным.</span><span class="sxs-lookup"><span data-stu-id="959bd-141">The handle pointed to by *phPrinter* is not thread safe.</span></span> <span data-ttu-id="959bd-142">Если вызывающие объекты должны одновременно использовать его в нескольких потоках, они должны предоставить настраиваемый доступ к обработке принтера с помощью [функций синхронизации](/windows/desktop/Sync/synchronization-functions).</span><span class="sxs-lookup"><span data-stu-id="959bd-142">If callers need to use it concurrently on multiple threads, they must provide custom synchronization access to the printer handle using the [Synchronization Functions](/windows/desktop/Sync/synchronization-functions).</span></span> <span data-ttu-id="959bd-143">Чтобы избежать написания пользовательского кода, приложение может по мере необходимости открывать маркеры принтера в каждом потоке.</span><span class="sxs-lookup"><span data-stu-id="959bd-143">To avoid writing custom code the application can open a printer handle on each thread, as needed.</span></span>

<span data-ttu-id="959bd-144">Параметр *пдефаулт* позволяет указать тип данных и значения режима устройства, используемые для печати документов, отправляемых функцией [**стартдокпринтер**](startdocprinter.md) .</span><span class="sxs-lookup"><span data-stu-id="959bd-144">The *pDefault* parameter enables you to specify the data type and device mode values that are used for printing documents submitted by the [**StartDocPrinter**](startdocprinter.md) function.</span></span> <span data-ttu-id="959bd-145">Однако эти значения можно переопределить с помощью функции [**сетжоб**](setjob.md) после запуска документа.</span><span class="sxs-lookup"><span data-stu-id="959bd-145">However, you can override these values by using the [**SetJob**](setjob.md) function after a document has been started.</span></span>

<span data-ttu-id="959bd-146">Параметры [**DEVMODE**](/windows/win32/api/wingdi/ns-wingdi-devmodea) , определенные в структуре [**\_ по умолчанию**](printer-defaults.md) параметра *пдефаулт* , не используются, если значение элемента *пдататипе* структуры [**документа \_ info \_ 1**](doc-info-1.md) , переданной в параметре *пдоЦинфо* вызова [**стартдокпринтер**](startdocprinter.md) , — "RAW".</span><span class="sxs-lookup"><span data-stu-id="959bd-146">The [**DEVMODE**](/windows/win32/api/wingdi/ns-wingdi-devmodea) settings defined in the [**PRINTER\_DEFAULTS**](printer-defaults.md) structure of the *pDefault* parameter are not used when the value of the *pDatatype* member of the [**DOC\_INFO\_1**](doc-info-1.md) structure that was passed in the *pDocInfo* parameter of the [**StartDocPrinter**](startdocprinter.md) call is "RAW".</span></span> <span data-ttu-id="959bd-147">Если документ высокого уровня (например, файл Adobe PDF или Microsoft Word) или другие данные принтера (например, PCL, PS или ХПГЛ) отправляются непосредственно на принтер с *пдататипе* , для которого задано значение "RAW", документ должен полностью описывать параметры задания печати в стиле **DEVMODE** на языке, понятном оборудовании.</span><span class="sxs-lookup"><span data-stu-id="959bd-147">When a high-level document (such as an Adobe PDF or Microsoft Word file) or other printer data (such PCL, PS, or HPGL) is sent directly to a printer with *pDatatype* set to "RAW", the document must fully describe the **DEVMODE**-style print job settings in the language understood by the hardware.</span></span>

<span data-ttu-id="959bd-148">Можно вызвать функцию **опенпринтер** , чтобы открыть обработчик для сервера печати или определить права доступа клиента к серверу печати.</span><span class="sxs-lookup"><span data-stu-id="959bd-148">You can call the **OpenPrinter** function to open a handle to a print server or to determine the access rights that a client has to a print server.</span></span> <span data-ttu-id="959bd-149">Для этого укажите имя сервера печати в параметре *ппринтернаме* , установите для элементов **пдататипе** и **пдевмоде** структуры [**принтеров \_ по умолчанию**](printer-defaults.md) **значение NULL**, а для элемента **десиредакцесс** задайте значение маски доступа сервера, например сервер \_ все \_ доступ.</span><span class="sxs-lookup"><span data-stu-id="959bd-149">To do so, specify the name of the print server in the *pPrinterName* parameter, set the **pDatatype** and **pDevMode** members of the [**PRINTER\_DEFAULTS**](printer-defaults.md) structure to **NULL**, and set the **DesiredAccess** member to specify a server access mask value such as SERVER\_ALL\_ACCESS.</span></span> <span data-ttu-id="959bd-150">После завершения работы с маркером передайте его в функцию [**клосепринтер**](closeprinter.md) , чтобы закрыть его.</span><span class="sxs-lookup"><span data-stu-id="959bd-150">When you finish with the handle, pass it to the [**ClosePrinter**](closeprinter.md) function to close it.</span></span>

<span data-ttu-id="959bd-151">Используйте элемент **десиредакцесс** в структуре [**\_ по умолчанию принтера**](printer-defaults.md) , чтобы указать права доступа, необходимые для принтера.</span><span class="sxs-lookup"><span data-stu-id="959bd-151">Use the **DesiredAccess** member of the [**PRINTER\_DEFAULTS**](printer-defaults.md) structure to specify the access rights that you need to the printer.</span></span> <span data-ttu-id="959bd-152">Права доступа могут быть одним из следующих.</span><span class="sxs-lookup"><span data-stu-id="959bd-152">The access rights can be one of the following.</span></span> <span data-ttu-id="959bd-153">(Если *пдефаулт* имеет **значение NULL**, то права доступа являются принтером \_ ДОСТУП к \_ использованию.)</span><span class="sxs-lookup"><span data-stu-id="959bd-153">(If *pDefault* is **NULL**, then the access rights are PRINTER\_ACCESS\_USE.)</span></span>



| <span data-ttu-id="959bd-154">Требуемое значение доступа</span><span class="sxs-lookup"><span data-stu-id="959bd-154">Desired Access value</span></span>                        | <span data-ttu-id="959bd-155">Значение</span><span class="sxs-lookup"><span data-stu-id="959bd-155">Meaning</span></span>                                                                                                                                                                                      |
|---------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="959bd-156">доступ к ПРИНТЕРу — \_ \_ Администрирование</span><span class="sxs-lookup"><span data-stu-id="959bd-156">PRINTER\_ACCESS\_ADMINISTER</span></span>                 | <span data-ttu-id="959bd-157">Для выполнения административных задач, например, предоставляемых [**сетпринтер**](setprinter.md).</span><span class="sxs-lookup"><span data-stu-id="959bd-157">To perform administrative tasks, such as those provided by [**SetPrinter**](setprinter.md).</span></span>                                                                                                 |
| <span data-ttu-id="959bd-158">\_Использование доступа к принтерам \_</span><span class="sxs-lookup"><span data-stu-id="959bd-158">PRINTER\_ACCESS\_USE</span></span>                        | <span data-ttu-id="959bd-159">Для выполнения основных операций печати.</span><span class="sxs-lookup"><span data-stu-id="959bd-159">To perform basic printing operations.</span></span>                                                                                                                                                        |
| <span data-ttu-id="959bd-160">\_доступ ко всем принтерам \_</span><span class="sxs-lookup"><span data-stu-id="959bd-160">PRINTER\_ALL\_ACCESS</span></span>                        | <span data-ttu-id="959bd-161">Для выполнения всех административных задач и базовых операций печати, за исключением синхронизации (см. раздел [стандартные права доступа](/windows/desktop/SecAuthZ/standard-access-rights)).</span><span class="sxs-lookup"><span data-stu-id="959bd-161">To perform all administrative tasks and basic printing operations except for SYNCHRONIZE (see [Standard Access Rights](/windows/desktop/SecAuthZ/standard-access-rights).</span></span>                                     |
| <span data-ttu-id="959bd-162">доступ к ПРИНТЕРу — \_ \_ Управление \_ ограниченным доступом</span><span class="sxs-lookup"><span data-stu-id="959bd-162">PRINTER\_ACCESS\_MANAGE\_LIMITED</span></span>            | <span data-ttu-id="959bd-163">Для выполнения административных задач, например, предоставляемых [**сетпринтер**](setprinter.md) и [**сетпринтердата**](setprinterdata.md).</span><span class="sxs-lookup"><span data-stu-id="959bd-163">To perform administrative tasks, such as those provided by [**SetPrinter**](setprinter.md) and [**SetPrinterData**](setprinterdata.md).</span></span> <span data-ttu-id="959bd-164">Это значение доступно начиная с Windows 8.1.</span><span class="sxs-lookup"><span data-stu-id="959bd-164">This value is available starting from Windows 8.1.</span></span> |
| <span data-ttu-id="959bd-165">универсальные значения безопасности, такие как запись \_ DAC</span><span class="sxs-lookup"><span data-stu-id="959bd-165">generic security values, such as WRITE\_DAC</span></span> | <span data-ttu-id="959bd-166">Для разрешения конкретных прав доступа.</span><span class="sxs-lookup"><span data-stu-id="959bd-166">To allow specific control access rights.</span></span> <span data-ttu-id="959bd-167">См. раздел [стандартные права доступа](/windows/desktop/SecAuthZ/standard-access-rights).</span><span class="sxs-lookup"><span data-stu-id="959bd-167">See [Standard Access Rights](/windows/desktop/SecAuthZ/standard-access-rights).</span></span>                                                                                      |



 

<span data-ttu-id="959bd-168">Если у пользователя нет разрешения на открытие указанного принтера или сервера печати с требуемым доступом, вызов **опенпринтер** завершится ошибкой с возвращаемым нулевым значением, а [**GETLASTERROR**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror) вернет значение Ошибка \_ отказа в доступе \_ .</span><span class="sxs-lookup"><span data-stu-id="959bd-168">If a user does not have permission to open a specified printer or print server with the desired access, the **OpenPrinter** call will fail with a return value of zero and [**GetLastError**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror) will return the value ERROR\_ACCESS\_DENIED.</span></span>

## <a name="examples"></a><span data-ttu-id="959bd-169">Примеры</span><span class="sxs-lookup"><span data-stu-id="959bd-169">Examples</span></span>

<span data-ttu-id="959bd-170">Пример программы, использующей эту функцию, см. в разделе [инструкции. печать с помощью API печати GDI](how-to--print-using-the-gdi-print-api.md).</span><span class="sxs-lookup"><span data-stu-id="959bd-170">For a sample program that uses this function, see [How To: Print Using the GDI Print API](how-to--print-using-the-gdi-print-api.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="959bd-171">Требования</span><span class="sxs-lookup"><span data-stu-id="959bd-171">Requirements</span></span>



| <span data-ttu-id="959bd-172">Требование</span><span class="sxs-lookup"><span data-stu-id="959bd-172">Requirement</span></span> | <span data-ttu-id="959bd-173">Значение</span><span class="sxs-lookup"><span data-stu-id="959bd-173">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="959bd-174">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="959bd-174">Minimum supported client</span></span><br/> | <span data-ttu-id="959bd-175">Windows 2000 Professional \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="959bd-175">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                                |
| <span data-ttu-id="959bd-176">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="959bd-176">Minimum supported server</span></span><br/> | <span data-ttu-id="959bd-177">Windows 2000 Server \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="959bd-177">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                      |
| <span data-ttu-id="959bd-178">Заголовок</span><span class="sxs-lookup"><span data-stu-id="959bd-178">Header</span></span><br/>                   | <dl> <span data-ttu-id="959bd-179"><dt>Винспул. h (включение Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="959bd-179"><dt>Winspool.h (include Windows.h)</dt></span></span> </dl> |
| <span data-ttu-id="959bd-180">Библиотека</span><span class="sxs-lookup"><span data-stu-id="959bd-180">Library</span></span><br/>                  | <dl> <span data-ttu-id="959bd-181"><dt>Винспул. lib</dt></span><span class="sxs-lookup"><span data-stu-id="959bd-181"><dt>Winspool.lib</dt></span></span> </dl>                   |
| <span data-ttu-id="959bd-182">DLL</span><span class="sxs-lookup"><span data-stu-id="959bd-182">DLL</span></span><br/>                      | <dl> <span data-ttu-id="959bd-183"><dt>Винспул. drv</dt></span><span class="sxs-lookup"><span data-stu-id="959bd-183"><dt>Winspool.drv</dt></span></span> </dl>                   |
| <span data-ttu-id="959bd-184">Имя в кодировке Юникод и ANSI</span><span class="sxs-lookup"><span data-stu-id="959bd-184">Unicode and ANSI names</span></span><br/>   | <span data-ttu-id="959bd-185">**Опенпринтерв** (Юникод) и **опенпринтера** (ANSI)</span><span class="sxs-lookup"><span data-stu-id="959bd-185">**OpenPrinterW** (Unicode) and **OpenPrinterA** (ANSI)</span></span><br/>                                         |



## <a name="see-also"></a><span data-ttu-id="959bd-186">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="959bd-186">See also</span></span>

<dl> <dt>

[<span data-ttu-id="959bd-187">Вывод на печать</span><span class="sxs-lookup"><span data-stu-id="959bd-187">Printing</span></span>](printdocs-printing.md)
</dt> <dt>

[<span data-ttu-id="959bd-188">Функции API очереди печати принтера</span><span class="sxs-lookup"><span data-stu-id="959bd-188">Print Spooler API Functions</span></span>](printing-and-print-spooler-functions.md)
</dt> <dt>

[<span data-ttu-id="959bd-189">**вритепринтер**</span><span class="sxs-lookup"><span data-stu-id="959bd-189">**WritePrinter**</span></span>](writeprinter.md)
</dt> <dt>

[<span data-ttu-id="959bd-190">**клосепринтер**</span><span class="sxs-lookup"><span data-stu-id="959bd-190">**ClosePrinter**</span></span>](closeprinter.md)
</dt> <dt>

[<span data-ttu-id="959bd-191">**\_значения по умолчанию для принтера**</span><span class="sxs-lookup"><span data-stu-id="959bd-191">**PRINTER\_DEFAULTS**</span></span>](printer-defaults.md)
</dt> <dt>

[<span data-ttu-id="959bd-192">**сетжоб**</span><span class="sxs-lookup"><span data-stu-id="959bd-192">**SetJob**</span></span>](setjob.md)
</dt> <dt>

[<span data-ttu-id="959bd-193">**сетпринтер**</span><span class="sxs-lookup"><span data-stu-id="959bd-193">**SetPrinter**</span></span>](setprinter.md)
</dt> <dt>

[<span data-ttu-id="959bd-194">**стартдокпринтер**</span><span class="sxs-lookup"><span data-stu-id="959bd-194">**StartDocPrinter**</span></span>](startdocprinter.md)
</dt> </dl>

 

