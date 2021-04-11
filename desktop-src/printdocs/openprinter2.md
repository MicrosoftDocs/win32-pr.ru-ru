---
description: Извлекает дескриптор указанного принтера, сервера печати или других типов дескрипторов в подсистеме печати при настройке некоторых параметров принтера.
ms.assetid: e2370ae4-4475-4ccc-a6f9-3d33d1370054
title: Функция OpenPrinter2 (Винспул. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- OpenPrinter2
- OpenPrinter2A
- OpenPrinter2W
api_type:
- DllExport
api_location:
- Spoolss.dll
ms.openlocfilehash: 46788d7ad810ef623cd77793a72ab6c046b73590
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "103910487"
---
# <a name="openprinter2-function"></a><span data-ttu-id="2059c-103">Функция OpenPrinter2</span><span class="sxs-lookup"><span data-stu-id="2059c-103">OpenPrinter2 function</span></span>

<span data-ttu-id="2059c-104">Извлекает дескриптор указанного принтера, сервера печати или других типов дескрипторов в подсистеме печати при настройке некоторых параметров принтера.</span><span class="sxs-lookup"><span data-stu-id="2059c-104">Retrieves a handle to the specified printer, print server, or other types of handles in the print subsystem, while setting some of the printer options.</span></span>

## <a name="syntax"></a><span data-ttu-id="2059c-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="2059c-105">Syntax</span></span>


```C++
BOOL OpenPrinter2(
  _In_  LPCTSTR            pPrinterName,
  _Out_ LPHANDLE           phPrinter,
  _In_  LPPRINTER_DEFAULTS pDefault,
  _In_  PPRINTER_OPTIONS   pOptions
);
```



## <a name="parameters"></a><span data-ttu-id="2059c-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="2059c-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="2059c-107">*ппринтернаме* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="2059c-107">*pPrinterName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="2059c-108">Указатель на константную строку, завершающуюся нулем, которая указывает имя принтера или сервера печати, объект принтера, Ксквмонитор или Ксквпорт.</span><span class="sxs-lookup"><span data-stu-id="2059c-108">A pointer to a constant null-terminated string that specifies the name of the printer or print server, the printer object, the XcvMonitor, or the XcvPort.</span></span>

<span data-ttu-id="2059c-109">Для объекта принтера используйте: Принтернаме, задание XXXX.</span><span class="sxs-lookup"><span data-stu-id="2059c-109">For a printer object, use: PrinterName,Job xxxx.</span></span> <span data-ttu-id="2059c-110">Для Ксквмонитор используйте: ServerName, Ксквмонитор Мониторнаме.</span><span class="sxs-lookup"><span data-stu-id="2059c-110">For an XcvMonitor, use: ServerName,XcvMonitor MonitorName.</span></span> <span data-ttu-id="2059c-111">Для Ксквпорт используйте: ServerName, Ксквпорт Портнаме.</span><span class="sxs-lookup"><span data-stu-id="2059c-111">For an XcvPort, use: ServerName,XcvPort PortName.</span></span>

<span data-ttu-id="2059c-112">**Windows Vista:** **Значение NULL** указывает на локальный сервер печати.</span><span class="sxs-lookup"><span data-stu-id="2059c-112">**Windows Vista:** If **NULL**, it indicates the local print server.</span></span>

</dd> <dt>

<span data-ttu-id="2059c-113">*фпринтер* \[ заполняет\]</span><span class="sxs-lookup"><span data-stu-id="2059c-113">*phPrinter* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="2059c-114">Указатель на переменную, которая получает маркер для открытого принтера или объекта сервера печати.</span><span class="sxs-lookup"><span data-stu-id="2059c-114">A pointer to a variable that receives a handle to the open printer or print server object.</span></span>

</dd> <dt>

<span data-ttu-id="2059c-115">*пдефаулт* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="2059c-115">*pDefault* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="2059c-116">Указатель на структуру [**\_ по умолчанию принтера**](printer-defaults.md) .</span><span class="sxs-lookup"><span data-stu-id="2059c-116">A pointer to a [**PRINTER\_DEFAULTS**](printer-defaults.md) structure.</span></span> <span data-ttu-id="2059c-117">Это значение может быть **равно NULL**.</span><span class="sxs-lookup"><span data-stu-id="2059c-117">This value can be **NULL**.</span></span>

</dd> <dt>

<span data-ttu-id="2059c-118">*поптионс* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="2059c-118">*pOptions* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="2059c-119">Указатель на структуру [**\_ параметров принтера**](printer-options.md) .</span><span class="sxs-lookup"><span data-stu-id="2059c-119">A pointer to a [**PRINTER\_OPTIONS**](printer-options.md) structure.</span></span> <span data-ttu-id="2059c-120">Это значение может быть **равно NULL**.</span><span class="sxs-lookup"><span data-stu-id="2059c-120">This value can be **NULL**.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="2059c-121">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="2059c-121">Return value</span></span>

<span data-ttu-id="2059c-122">Если функция выполнена, возвращаемое значение будет ненулевым.</span><span class="sxs-lookup"><span data-stu-id="2059c-122">If the function succeeds, the return value is a nonzero value.</span></span>

<span data-ttu-id="2059c-123">Если функция выполняется неудачно, возвращается нулевое значение.</span><span class="sxs-lookup"><span data-stu-id="2059c-123">If the function fails, the return value is zero.</span></span> <span data-ttu-id="2059c-124">Для получения расширенных сведений об ошибках вызовите [**GetLastError**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror).</span><span class="sxs-lookup"><span data-stu-id="2059c-124">For extended error information, call [**GetLastError**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror).</span></span>

## <a name="remarks"></a><span data-ttu-id="2059c-125">Комментарии</span><span class="sxs-lookup"><span data-stu-id="2059c-125">Remarks</span></span>

<span data-ttu-id="2059c-126">Не вызывайте этот метод в [**DllMain**](/windows/desktop/Dlls/dllmain).</span><span class="sxs-lookup"><span data-stu-id="2059c-126">Do not call this method in [**DllMain**](/windows/desktop/Dlls/dllmain).</span></span>

> [!Note]  
> <span data-ttu-id="2059c-127">Это блокирующая или синхронная функция, которая может не возвращать значение немедленно.</span><span class="sxs-lookup"><span data-stu-id="2059c-127">This is a blocking or synchronous function and might not return immediately.</span></span> <span data-ttu-id="2059c-128">Скорость возврата этой функцией зависит от факторов времени выполнения, таких как состояние сети, Конфигурация сервера печати и факторы реализации драйвера принтера, которые трудно предсказать при написании приложения.</span><span class="sxs-lookup"><span data-stu-id="2059c-128">How quickly this function returns depends on run-time factors such as network status, print server configuration, and printer driver implementation factors that are difficult to predict when writing an application.</span></span> <span data-ttu-id="2059c-129">Вызов этой функции из потока, который управляет взаимодействием с пользовательским интерфейсом, может привести к невозможности реагирования приложения.</span><span class="sxs-lookup"><span data-stu-id="2059c-129">Calling this function from a thread that manages interaction with the user interface could make the application appear to be unresponsive.</span></span>

 

<span data-ttu-id="2059c-130">Версия ANSI этой функции не реализована и возвращает ошибку \_ не \_ поддерживается.</span><span class="sxs-lookup"><span data-stu-id="2059c-130">The ANSI version of this function is not implemented and returns ERROR\_NOT\_SUPPORTED.</span></span>

<span data-ttu-id="2059c-131">Параметр *пдефаулт* позволяет указать тип данных и значения режима устройства, используемые для печати документов, отправляемых функцией [**стартдокпринтер**](startdocprinter.md) .</span><span class="sxs-lookup"><span data-stu-id="2059c-131">The *pDefault* parameter enables you to specify the data type and device mode values that are used for printing documents submitted by the [**StartDocPrinter**](startdocprinter.md) function.</span></span> <span data-ttu-id="2059c-132">Однако эти значения можно переопределить с помощью функции [**сетжоб**](setjob.md) после запуска документа.</span><span class="sxs-lookup"><span data-stu-id="2059c-132">However, you can override these values by using the [**SetJob**](setjob.md) function after a document has been started.</span></span>

<span data-ttu-id="2059c-133">Можно вызвать функцию **OpenPrinter2** , чтобы открыть обработчик для сервера печати или определить права доступа клиента к серверу печати.</span><span class="sxs-lookup"><span data-stu-id="2059c-133">You can call the **OpenPrinter2** function to open a handle to a print server or to determine client access rights to a print server.</span></span> <span data-ttu-id="2059c-134">Для этого укажите имя сервера печати в параметре *ппринтернаме* , установите для элементов **пдататипе** и **пдевмоде** структуры [**принтеров \_ по умолчанию**](printer-defaults.md) **значение NULL**, а для элемента **десиредакцесс** задайте значение маски доступа сервера, например сервер \_ все \_ доступ.</span><span class="sxs-lookup"><span data-stu-id="2059c-134">To do this, specify the name of the print server in the *pPrinterName* parameter, set the **pDatatype** and **pDevMode** members of the [**PRINTER\_DEFAULTS**](printer-defaults.md) structure to **NULL**, and set the **DesiredAccess** member to specify a server access mask value such as SERVER\_ALL\_ACCESS.</span></span> <span data-ttu-id="2059c-135">По завершении работы с маркером передайте его в функцию [**клосепринтер**](closeprinter.md) , чтобы закрыть его.</span><span class="sxs-lookup"><span data-stu-id="2059c-135">When you are finished with the handle, pass it to the [**ClosePrinter**](closeprinter.md) function to close it.</span></span>

<span data-ttu-id="2059c-136">Используйте элемент **десиредакцесс** в структуре [**\_ параметров принтера**](printer-defaults.md) , чтобы указать необходимые права доступа.</span><span class="sxs-lookup"><span data-stu-id="2059c-136">Use the **DesiredAccess** member of the [**PRINTER\_DEFAULTS**](printer-defaults.md) structure to specify the necessary access rights.</span></span> <span data-ttu-id="2059c-137">Права доступа могут быть одним из следующих.</span><span class="sxs-lookup"><span data-stu-id="2059c-137">The access rights can be one of the following.</span></span>



| <span data-ttu-id="2059c-138">Требуемое значение доступа</span><span class="sxs-lookup"><span data-stu-id="2059c-138">Desired Access value</span></span>                        | <span data-ttu-id="2059c-139">Значение</span><span class="sxs-lookup"><span data-stu-id="2059c-139">Meaning</span></span>                                                                                                                                                                                      |
|---------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="2059c-140">доступ к ПРИНТЕРу — \_ \_ Администрирование</span><span class="sxs-lookup"><span data-stu-id="2059c-140">PRINTER\_ACCESS\_ADMINISTER</span></span>                 | <span data-ttu-id="2059c-141">Для выполнения административных задач, например, предоставляемых [**сетпринтер**](setprinter.md).</span><span class="sxs-lookup"><span data-stu-id="2059c-141">To perform administrative tasks, such as those provided by [**SetPrinter**](setprinter.md).</span></span>                                                                                                 |
| <span data-ttu-id="2059c-142">\_Использование доступа к принтерам \_</span><span class="sxs-lookup"><span data-stu-id="2059c-142">PRINTER\_ACCESS\_USE</span></span>                        | <span data-ttu-id="2059c-143">Для выполнения основных операций печати.</span><span class="sxs-lookup"><span data-stu-id="2059c-143">To perform basic printing operations.</span></span>                                                                                                                                                        |
| <span data-ttu-id="2059c-144">\_доступ ко всем принтерам \_</span><span class="sxs-lookup"><span data-stu-id="2059c-144">PRINTER\_ALL\_ACCESS</span></span>                        | <span data-ttu-id="2059c-145">Для выполнения всех административных задач и базовых операций печати, кроме синхронизации.</span><span class="sxs-lookup"><span data-stu-id="2059c-145">To perform all administrative tasks and basic printing operations except SYNCHRONIZE.</span></span> <span data-ttu-id="2059c-146">См. раздел [стандартные права доступа](/windows/desktop/SecAuthZ/standard-access-rights).</span><span class="sxs-lookup"><span data-stu-id="2059c-146">See [Standard Access Rights](/windows/desktop/SecAuthZ/standard-access-rights).</span></span>                                         |
| <span data-ttu-id="2059c-147">доступ к ПРИНТЕРу — \_ \_ Управление \_ ограниченным доступом</span><span class="sxs-lookup"><span data-stu-id="2059c-147">PRINTER\_ACCESS\_MANAGE\_LIMITED</span></span>            | <span data-ttu-id="2059c-148">Для выполнения административных задач, например, предоставляемых [**сетпринтер**](setprinter.md) и [**сетпринтердата**](setprinterdata.md).</span><span class="sxs-lookup"><span data-stu-id="2059c-148">To perform administrative tasks, such as those provided by [**SetPrinter**](setprinter.md) and [**SetPrinterData**](setprinterdata.md).</span></span> <span data-ttu-id="2059c-149">Это значение доступно начиная с Windows 8.1.</span><span class="sxs-lookup"><span data-stu-id="2059c-149">This value is available starting from Windows 8.1.</span></span> |
| <span data-ttu-id="2059c-150">универсальные значения безопасности, такие как запись \_ DAC</span><span class="sxs-lookup"><span data-stu-id="2059c-150">generic security values, such as WRITE\_DAC</span></span> | <span data-ttu-id="2059c-151">Для разрешения конкретных прав доступа.</span><span class="sxs-lookup"><span data-stu-id="2059c-151">To allow specific control access rights.</span></span> <span data-ttu-id="2059c-152">См. раздел [стандартные права доступа](/windows/desktop/SecAuthZ/standard-access-rights).</span><span class="sxs-lookup"><span data-stu-id="2059c-152">See [Standard Access Rights](/windows/desktop/SecAuthZ/standard-access-rights).</span></span>                                                                                      |



 

<span data-ttu-id="2059c-153">Если у пользователя нет разрешения на открытие указанного принтера или сервера печати с требуемым доступом, вызов **OpenPrinter2** завершится ошибкой, а [**GetLastError**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror) вернет значение "ошибка \_ отказа в доступе" \_ .</span><span class="sxs-lookup"><span data-stu-id="2059c-153">If a user does not have permission to open a specified printer or print server with the desired access, the **OpenPrinter2** call will fail, and [**GetLastError**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror) will return the value ERROR\_ACCESS\_DENIED.</span></span>

<span data-ttu-id="2059c-154">Если *ппринтернаме* является локальным принтером, **OpenPrinter2** игнорирует все значения **dwFlags** , что на структуру [**\_ параметров принтера**](printer-options.md) указывает на использование *поптионс*, за исключением \_ изменения клиента для параметра принтера \_ \_ .</span><span class="sxs-lookup"><span data-stu-id="2059c-154">When *pPrinterName* is a local printer, then **OpenPrinter2** ignores all values of the **dwFlags** that the [**PRINTER\_OPTIONS**](printer-options.md) structure pointed to using *pOptions*, except PRINTER\_OPTION\_CLIENT\_CHANGE.</span></span> <span data-ttu-id="2059c-155">Если последний передается, **OpenPrinter2** будет возвращать ошибку \_ отказа в доступе \_ .</span><span class="sxs-lookup"><span data-stu-id="2059c-155">If the latter is passed, then **OpenPrinter2** will return ERROR\_ACCESS\_DENIED.</span></span> <span data-ttu-id="2059c-156">Соответственно, при открытии локального принтера **OpenPrinter2** не предоставляет преимуществ по сравнению с [**опенпринтер**](openprinter.md).</span><span class="sxs-lookup"><span data-stu-id="2059c-156">Accordingly, when opening a local printer, **OpenPrinter2** provides no advantage over [**OpenPrinter**](openprinter.md).</span></span>

<span data-ttu-id="2059c-157">**Windows Vista:** Данные принтера, возвращаемые **OpenPrinter2** , извлекаются из локального кэша, если в поле **DwFlags** структуры [**\_ параметров принтера**](printer-options.md) , на которую ссылается *поптионс*, не установлен флаг " **\_ параметр принтера \_ без \_ кэша** ".</span><span class="sxs-lookup"><span data-stu-id="2059c-157">**Windows Vista:** The printer data returned by **OpenPrinter2** is retrieved from a local cache unless the **PRINTER\_OPTION\_NO\_CACHE** flag is set in the **dwFlags** field of the [**PRINTER\_OPTIONS**](printer-options.md) structure referenced by *pOptions*.</span></span>

## <a name="examples"></a><span data-ttu-id="2059c-158">Примеры</span><span class="sxs-lookup"><span data-stu-id="2059c-158">Examples</span></span>

<span data-ttu-id="2059c-159">В этом примере **OpenPrinter2** завершается с ошибкой, когда \_ доступ к принтеру \_ управляется в \_ структуре [**\_ по умолчанию**](printer-defaults.md) , а пользователь не имеет соответствующего разрешения.</span><span class="sxs-lookup"><span data-stu-id="2059c-159">In this example, **OpenPrinter2** fails when PRINTER\_ACCESS\_MANAGE\_LIMITED is passed to the [**PRINTER\_DEFAULTS**](printer-defaults.md) structure, and the user does not have the appropriate permission.</span></span>


```C++
// Specify the limited management permission.
PRINTER_DEFAULTS defaults = {};
defaults.DesiredAccess = PRINTER_ACCESS_MANAGE_LIMITED;

// Open a printer to which the user has no administrative rights.
HANDLE printer = nullptr;
assert(!OpenPrinter2(L QueueWithNoAdminRights , // Queue name
                     &printer,                  // Printer handle
                     &defaults,                 // Printer defaults
                     nullptr));                 // Printer options

assert(GetLastError() == ERROR_ACCESS_DENIED);

if (printer)
{
    ClosePrinter(printer);
}
```



<span data-ttu-id="2059c-160">Пример программы, демонстрирующий использование этой функции, см. в разделе [инструкции. печать с помощью API печати GDI](how-to--print-using-the-gdi-print-api.md).</span><span class="sxs-lookup"><span data-stu-id="2059c-160">For a sample program that shows how to use this function, see [How To: Print Using the GDI Print API](how-to--print-using-the-gdi-print-api.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="2059c-161">Требования</span><span class="sxs-lookup"><span data-stu-id="2059c-161">Requirements</span></span>



| <span data-ttu-id="2059c-162">Требование</span><span class="sxs-lookup"><span data-stu-id="2059c-162">Requirement</span></span> | <span data-ttu-id="2059c-163">Значение</span><span class="sxs-lookup"><span data-stu-id="2059c-163">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="2059c-164">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="2059c-164">Minimum supported client</span></span><br/> | <span data-ttu-id="2059c-165">Только для \[ классических приложений Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="2059c-165">Windows Vista \[desktop apps only\]</span></span><br/>                                                            |
| <span data-ttu-id="2059c-166">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="2059c-166">Minimum supported server</span></span><br/> | <span data-ttu-id="2059c-167">\[Только для настольных приложений Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="2059c-167">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                                      |
| <span data-ttu-id="2059c-168">Header</span><span class="sxs-lookup"><span data-stu-id="2059c-168">Header</span></span><br/>                   | <dl> <span data-ttu-id="2059c-169"><dt>Винспул. h (включение Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="2059c-169"><dt>Winspool.h (include Windows.h)</dt></span></span> </dl> |
| <span data-ttu-id="2059c-170">Библиотека</span><span class="sxs-lookup"><span data-stu-id="2059c-170">Library</span></span><br/>                  | <dl> <span data-ttu-id="2059c-171"><dt>Винспул. lib</dt></span><span class="sxs-lookup"><span data-stu-id="2059c-171"><dt>Winspool.lib</dt></span></span> </dl>                   |
| <span data-ttu-id="2059c-172">DLL</span><span class="sxs-lookup"><span data-stu-id="2059c-172">DLL</span></span><br/>                      | <dl> <span data-ttu-id="2059c-173"><dt>Spoolss.dll</dt></span><span class="sxs-lookup"><span data-stu-id="2059c-173"><dt>Spoolss.dll</dt></span></span> </dl>                    |
| <span data-ttu-id="2059c-174">Имя в кодировке Юникод и ANSI</span><span class="sxs-lookup"><span data-stu-id="2059c-174">Unicode and ANSI names</span></span><br/>   | <span data-ttu-id="2059c-175">**OpenPrinter2W** (Юникод) и **OpenPrinter2A** (ANSI)</span><span class="sxs-lookup"><span data-stu-id="2059c-175">**OpenPrinter2W** (Unicode) and **OpenPrinter2A** (ANSI)</span></span><br/>                                       |



## <a name="see-also"></a><span data-ttu-id="2059c-176">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="2059c-176">See also</span></span>

<dl> <dt>

[<span data-ttu-id="2059c-177">Вывод на печать</span><span class="sxs-lookup"><span data-stu-id="2059c-177">Printing</span></span>](printdocs-printing.md)
</dt> <dt>

[<span data-ttu-id="2059c-178">Функции API очереди печати принтера</span><span class="sxs-lookup"><span data-stu-id="2059c-178">Print Spooler API Functions</span></span>](printing-and-print-spooler-functions.md)
</dt> <dt>

[<span data-ttu-id="2059c-179">**клосепринтер**</span><span class="sxs-lookup"><span data-stu-id="2059c-179">**ClosePrinter**</span></span>](closeprinter.md)
</dt> <dt>

[<span data-ttu-id="2059c-180">**\_значения по умолчанию для принтера**</span><span class="sxs-lookup"><span data-stu-id="2059c-180">**PRINTER\_DEFAULTS**</span></span>](printer-defaults.md)
</dt> <dt>

[<span data-ttu-id="2059c-181">**\_Параметры принтера**</span><span class="sxs-lookup"><span data-stu-id="2059c-181">**PRINTER\_OPTIONS**</span></span>](printer-options.md)
</dt> <dt>

[<span data-ttu-id="2059c-182">**сетжоб**</span><span class="sxs-lookup"><span data-stu-id="2059c-182">**SetJob**</span></span>](setjob.md)
</dt> <dt>

[<span data-ttu-id="2059c-183">**сетпринтер**</span><span class="sxs-lookup"><span data-stu-id="2059c-183">**SetPrinter**</span></span>](setprinter.md)
</dt> <dt>

[<span data-ttu-id="2059c-184">**стартдокпринтер**</span><span class="sxs-lookup"><span data-stu-id="2059c-184">**StartDocPrinter**</span></span>](startdocprinter.md)
</dt> <dt>

[<span data-ttu-id="2059c-185">**опенпринтер**</span><span class="sxs-lookup"><span data-stu-id="2059c-185">**OpenPrinter**</span></span>](openprinter.md)
</dt> </dl>

 

