---
description: Функция Жетпринтердата получает данные конфигурации для указанного принтера или сервера печати.
ms.assetid: b5a44b27-a4aa-4e58-9a64-05be87d12ab5
title: Функция Жетпринтердата (Винспул. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- GetPrinterData
- GetPrinterDataA
- GetPrinterDataW
api_type:
- DllExport
api_location:
- Winspool.drv
- Ext-MS-Win-Printer-WinSpool-l1-1-2.dll
- Ext-MS-Win-Printer-WinSpool-L1-1-3.dll
ms.openlocfilehash: cb18936d6d3c1d82f4a52a874883cdcdfaae4815
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "105702611"
---
# <a name="getprinterdata-function"></a><span data-ttu-id="be17d-103">Функция Жетпринтердата</span><span class="sxs-lookup"><span data-stu-id="be17d-103">GetPrinterData function</span></span>

<span data-ttu-id="be17d-104">Функция **жетпринтердата** получает данные конфигурации для указанного принтера или сервера печати.</span><span class="sxs-lookup"><span data-stu-id="be17d-104">The **GetPrinterData** function retrieves configuration data for the specified printer or print server.</span></span>

<span data-ttu-id="be17d-105">В Windows 2000 и более поздних версиях Windows вызов **жетпринтердата** эквивалентен вызову [**жетпринтердатаекс**](/windows/desktop/printdocs/getprinterdataex) с параметром *Пкэйнаме* , имеющим значение "принтердривердата".</span><span class="sxs-lookup"><span data-stu-id="be17d-105">In Windows 2000 and later versions of Windows, calling **GetPrinterData** is equivalent to calling [**GetPrinterDataEx**](/windows/desktop/printdocs/getprinterdataex) with the *pKeyName* parameter set to "PrinterDriverData".</span></span>

## <a name="syntax"></a><span data-ttu-id="be17d-106">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="be17d-106">Syntax</span></span>


```C++
DWORD GetPrinterData(
  _In_  HANDLE  hPrinter,
  _In_  LPTSTR  pValueName,
  _Out_ LPDWORD pType,
  _Out_ LPBYTE  pData,
  _In_  DWORD   nSize,
  _Out_ LPDWORD pcbNeeded
);
```



## <a name="parameters"></a><span data-ttu-id="be17d-107">Параметры</span><span class="sxs-lookup"><span data-stu-id="be17d-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="be17d-108">*хпринтер* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="be17d-108">*hPrinter* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="be17d-109">Маркер принтера или сервера печати, для которого функция получает данные конфигурации.</span><span class="sxs-lookup"><span data-stu-id="be17d-109">A handle to the printer or print server for which the function retrieves configuration data.</span></span> <span data-ttu-id="be17d-110">Используйте функцию [**опенпринтер**](openprinter.md), [**OpenPrinter2**](openprinter2.md)или [**аддпринтер**](addprinter.md) для получения маркера принтера.</span><span class="sxs-lookup"><span data-stu-id="be17d-110">Use the [**OpenPrinter**](openprinter.md), [**OpenPrinter2**](openprinter2.md), or [**AddPrinter**](addprinter.md) function to retrieve a printer handle.</span></span>

</dd> <dt>

<span data-ttu-id="be17d-111">*пвалуенаме* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="be17d-111">*pValueName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="be17d-112">Указатель на строку, завершающуюся нулем, которая определяет извлекаемые данные.</span><span class="sxs-lookup"><span data-stu-id="be17d-112">A pointer to a null-terminated string that identifies the data to retrieve.</span></span>

<span data-ttu-id="be17d-113">Для принтеров эта строка представляет собой имя значения реестра в разделе "Принтердривердата" принтера в реестре.</span><span class="sxs-lookup"><span data-stu-id="be17d-113">For printers, this string is the name of a registry value under the printer's "PrinterDriverData" key in the registry.</span></span>

<span data-ttu-id="be17d-114">Для серверов печати эта строка является одной из предопределенных строк, перечисленных в следующем разделе "Примечания".</span><span class="sxs-lookup"><span data-stu-id="be17d-114">For print servers, this string is one of the predefined strings listed in the following Remarks section.</span></span>

</dd> <dt>

<span data-ttu-id="be17d-115">*птипе* \[ заполняет\]</span><span class="sxs-lookup"><span data-stu-id="be17d-115">*pType* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="be17d-116">Указатель на переменную, которая получает значение, указывающее тип данных, полученных в *pData*.</span><span class="sxs-lookup"><span data-stu-id="be17d-116">A pointer to a variable that receives a value that indicates the type of data retrieved in *pData*.</span></span> <span data-ttu-id="be17d-117">Функция возвращает тип, указанный в вызове [**сетпринтердата**](setprinterdata.md) или [**сетпринтердатаекс**](setprinterdataex.md) , который хранит данные.</span><span class="sxs-lookup"><span data-stu-id="be17d-117">The function returns the type specified in the [**SetPrinterData**](setprinterdata.md) or [**SetPrinterDataEx**](setprinterdataex.md) call that stored the data.</span></span> <span data-ttu-id="be17d-118">Если тип данных не требуется, присвойте этому параметру **значение NULL** .</span><span class="sxs-lookup"><span data-stu-id="be17d-118">Set this parameter to **NULL** if you don't need the data type.</span></span>

</dd> <dt>

<span data-ttu-id="be17d-119">*pData* \[ заполняет\]</span><span class="sxs-lookup"><span data-stu-id="be17d-119">*pData* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="be17d-120">Указатель на буфер, который получает данные конфигурации.</span><span class="sxs-lookup"><span data-stu-id="be17d-120">A pointer to a buffer that receives the configuration data.</span></span>

</dd> <dt>

<span data-ttu-id="be17d-121">*нсизе* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="be17d-121">*nSize* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="be17d-122">Размер (в байтах) буфера, на который указывает *pData* .</span><span class="sxs-lookup"><span data-stu-id="be17d-122">The size, in bytes, of the buffer that *pData* points to.</span></span>

</dd> <dt>

<span data-ttu-id="be17d-123">*пкбнидед* \[ заполняет\]</span><span class="sxs-lookup"><span data-stu-id="be17d-123">*pcbNeeded* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="be17d-124">Указатель на переменную, которая получает размер данных конфигурации в байтах.</span><span class="sxs-lookup"><span data-stu-id="be17d-124">A pointer to a variable that receives the size, in bytes, of the configuration data.</span></span> <span data-ttu-id="be17d-125">Если размер буфера, указанный параметром *нсизе* , слишком мал, функция возвращает **ошибку \_ больше \_ данных**, а *пкбнидед* указывает требуемый размер буфера.</span><span class="sxs-lookup"><span data-stu-id="be17d-125">If the buffer size specified by *nSize* is too small, the function returns **ERROR\_MORE\_DATA**, and *pcbNeeded* indicates the required buffer size.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="be17d-126">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="be17d-126">Return value</span></span>

<span data-ttu-id="be17d-127">Если функция завершается успешно, возвращается значение **ошибки \_ Success**.</span><span class="sxs-lookup"><span data-stu-id="be17d-127">If the function succeeds, the return value is **ERROR\_SUCCESS**.</span></span> <span data-ttu-id="be17d-128">Если функция завершается ошибкой, возвращается значение ошибки.</span><span class="sxs-lookup"><span data-stu-id="be17d-128">If the function fails, the return value is an error value.</span></span>

## <a name="remarks"></a><span data-ttu-id="be17d-129">Комментарии</span><span class="sxs-lookup"><span data-stu-id="be17d-129">Remarks</span></span>

> [!Note]  
> <span data-ttu-id="be17d-130">Это блокирующая или синхронная функция, которая может не возвращать значение немедленно.</span><span class="sxs-lookup"><span data-stu-id="be17d-130">This is a blocking or synchronous function and might not return immediately.</span></span> <span data-ttu-id="be17d-131">Скорость возврата этой функцией зависит от факторов времени выполнения, таких как состояние сети, Конфигурация сервера печати и факторы реализации драйвера принтера, которые трудно предсказать при написании приложения.</span><span class="sxs-lookup"><span data-stu-id="be17d-131">How quickly this function returns depends on run-time factors such as network status, print server configuration, and printer driver implementation factors that are difficult to predict when writing an application.</span></span> <span data-ttu-id="be17d-132">Вызов этой функции из потока, который управляет взаимодействием с пользовательским интерфейсом, может привести к невозможности реагирования приложения.</span><span class="sxs-lookup"><span data-stu-id="be17d-132">Calling this function from a thread that manages interaction with the user interface could make the application appear to be unresponsive.</span></span>

 

<span data-ttu-id="be17d-133">**Жетпринтердата** извлекает данные конфигурации принтера, которые были заданы функцией [**сетпринтердатаекс**](setprinterdataex.md) или [**сетпринтердата**](setprinterdata.md) .</span><span class="sxs-lookup"><span data-stu-id="be17d-133">**GetPrinterData** retrieves printer configuration data that was set by the [**SetPrinterDataEx**](setprinterdataex.md) or [**SetPrinterData**](setprinterdata.md) function.</span></span>

<span data-ttu-id="be17d-134">**Жетпринтердата** может вызывать вызов Windows в [**жетпринтердатафромпорт**](/previous-versions//ff550506(v=vs.85)), который может записывать в реестр.</span><span class="sxs-lookup"><span data-stu-id="be17d-134">**GetPrinterData** might trigger a Windows call to [**GetPrinterDataFromPort**](/previous-versions//ff550506(v=vs.85)), which might write to the registry.</span></span> <span data-ttu-id="be17d-135">В противном случае могут возникать побочные эффекты, такие как запуск обновления или обновления события принтера с ИДЕНТИФИКАТОРом 20 в клиенте, если принтер является общим в сети.</span><span class="sxs-lookup"><span data-stu-id="be17d-135">If it does, side effects can occur, such as triggering an update or upgrade printer event ID 20 in the client, if the printer is shared in a network.</span></span>

<span data-ttu-id="be17d-136">Если *хпринтер* является обработчиком для сервера печати, *пвалуенаме* может указать одно из следующих предопределенных значений.</span><span class="sxs-lookup"><span data-stu-id="be17d-136">If *hPrinter* is a handle to a print server, *pValueName* can specify one of the following predefined values.</span></span>



| <span data-ttu-id="be17d-137">Значение</span><span class="sxs-lookup"><span data-stu-id="be17d-137">Value</span></span>                                                               | <span data-ttu-id="be17d-138">Комментарии</span><span class="sxs-lookup"><span data-stu-id="be17d-138">Comments</span></span>                                                                                                                                                                                                                        |
|---------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="be17d-139">**СПЛРЕГ \_ Разрешить \_ \_ манажеформс пользователя**</span><span class="sxs-lookup"><span data-stu-id="be17d-139">**SPLREG\_ALLOW\_USER\_MANAGEFORMS**</span></span>                                | <span data-ttu-id="be17d-140">Windows XP с пакетом обновления 2 (SP2) и более поздние версии</span><span class="sxs-lookup"><span data-stu-id="be17d-140">Windows XP with Service Pack 2 (SP2) and later</span></span><br/> <span data-ttu-id="be17d-141">Windows Server 2003 с пакетом обновления 1 (SP1) и более поздние версии</span><span class="sxs-lookup"><span data-stu-id="be17d-141">Windows Server 2003 with Service Pack 1 (SP1) and later</span></span><br/>                                                                                                    |
| <span data-ttu-id="be17d-142">**\_архитектура сплрег**</span><span class="sxs-lookup"><span data-stu-id="be17d-142">**SPLREG\_ARCHITECTURE**</span></span>                                            |                                                                                                                                                                                                                                 |
| <span data-ttu-id="be17d-143">**\_включен звуковой сигнал сплрег \_**</span><span class="sxs-lookup"><span data-stu-id="be17d-143">**SPLREG\_BEEP\_ENABLED**</span></span>                                           |                                                                                                                                                                                                                                 |
| <span data-ttu-id="be17d-144">**СПЛРЕГ \_ \_ Каталог очереди печати по умолчанию \_**</span><span class="sxs-lookup"><span data-stu-id="be17d-144">**SPLREG\_DEFAULT\_SPOOL\_DIRECTORY**</span></span>                               |                                                                                                                                                                                                                                 |
| <span data-ttu-id="be17d-145">**СПЛРЕГ \_ DNS \_ - \_ имя компьютера**</span><span class="sxs-lookup"><span data-stu-id="be17d-145">**SPLREG\_DNS\_MACHINE\_NAME**</span></span>                                      |                                                                                                                                                                                                                                 |
| <span data-ttu-id="be17d-146">**СПЛРЕГ \_ DS \_**</span><span class="sxs-lookup"><span data-stu-id="be17d-146">**SPLREG\_DS\_PRESENT**</span></span>                                             | <span data-ttu-id="be17d-147">При успешном возвращении *pData* содержит 0x0001, если компьютер находится в домене DS, в противном случае — 0.</span><span class="sxs-lookup"><span data-stu-id="be17d-147">On successful return, *pData* contains 0x0001 if the machine is on a DS domain, 0 otherwise.</span></span><br/>                                                                                                                         |
| <span data-ttu-id="be17d-148">**СПЛРЕГ \_ DS \_ \_ для \_ пользователя**</span><span class="sxs-lookup"><span data-stu-id="be17d-148">**SPLREG\_DS\_PRESENT\_FOR\_USER**</span></span>                                  | <span data-ttu-id="be17d-149">При успешном возвращении *pData* содержит 0x0001, если пользователь вошел в домен DS, в противном случае — 0.</span><span class="sxs-lookup"><span data-stu-id="be17d-149">On successful return, *pData* contains 0x0001 if the user is logged onto a DS domain, 0 otherwise.</span></span><br/>                                                                                                                   |
| <span data-ttu-id="be17d-150">**\_журнал событий \_ сплрег**</span><span class="sxs-lookup"><span data-stu-id="be17d-150">**SPLREG\_EVENT\_LOG**</span></span>                                              |                                                                                                                                                                                                                                 |
| <span data-ttu-id="be17d-151">**\_Основная \_ версия сплрег**</span><span class="sxs-lookup"><span data-stu-id="be17d-151">**SPLREG\_MAJOR\_VERSION**</span></span>                                          |                                                                                                                                                                                                                                 |
| <span data-ttu-id="be17d-152">**\_дополнительный номер \_ версии сплрег**</span><span class="sxs-lookup"><span data-stu-id="be17d-152">**SPLREG\_MINOR\_VERSION**</span></span>                                          |                                                                                                                                                                                                                                 |
| <span data-ttu-id="be17d-153">**\_ \_ всплывающее меню сплрег NET**</span><span class="sxs-lookup"><span data-stu-id="be17d-153">**SPLREG\_NET\_POPUP**</span></span>                                              | <span data-ttu-id="be17d-154">Не поддерживается в Windows Server 2003 и более поздних версиях</span><span class="sxs-lookup"><span data-stu-id="be17d-154">Not supported in Windows Server 2003 and later</span></span><br/>                                                                                                                                                                       |
| <span data-ttu-id="be17d-155">**СПЛРЕГ \_ net \_ Popup \_ to \_ Computer**</span><span class="sxs-lookup"><span data-stu-id="be17d-155">**SPLREG\_NET\_POPUP\_TO\_COMPUTER**</span></span>                                | <span data-ttu-id="be17d-156">При успешном возвращении *pData* содержит 1, если уведомления о задании должны отправляться на клиентский компьютер, или 0, если уведомления о задании будут отправляться пользователю.</span><span class="sxs-lookup"><span data-stu-id="be17d-156">On successful return, *pData* contains 1 if job notifications should be sent to the client computer, or 0 if job notifications are to be sent to the user.</span></span><br/> <span data-ttu-id="be17d-157">Не поддерживается в Windows Server 2003 и более поздних версиях</span><span class="sxs-lookup"><span data-stu-id="be17d-157">Not supported in Windows Server 2003 and later</span></span><br/> |
| <span data-ttu-id="be17d-158">**\_версия ОС \_ сплрег**</span><span class="sxs-lookup"><span data-stu-id="be17d-158">**SPLREG\_OS\_VERSION**</span></span>                                             | <span data-ttu-id="be17d-159">Windows XP и более поздних версий.</span><span class="sxs-lookup"><span data-stu-id="be17d-159">Windows XP and later</span></span><br/>                                                                                                                                                                                                 |
| <span data-ttu-id="be17d-160">**СПЛРЕГ \_ OS \_ версионекс**</span><span class="sxs-lookup"><span data-stu-id="be17d-160">**SPLREG\_OS\_VERSIONEX**</span></span>                                           |                                                                                                                                                                                                                                 |
| <span data-ttu-id="be17d-161">**\_ \_ приоритет потока портов \_ сплрег \_ по умолчанию**</span><span class="sxs-lookup"><span data-stu-id="be17d-161">**SPLREG\_PORT\_THREAD\_PRIORITY\_DEFAULT**</span></span>                         |                                                                                                                                                                                                                                 |
| <span data-ttu-id="be17d-162">**\_ \_ приоритет потока портов \_ сплрег**</span><span class="sxs-lookup"><span data-stu-id="be17d-162">**SPLREG\_PORT\_THREAD\_PRIORITY**</span></span>                                  |                                                                                                                                                                                                                                 |
| <span data-ttu-id="be17d-163">**\_ \_ \_ группы изоляции драйвера печати \_ сплрег**</span><span class="sxs-lookup"><span data-stu-id="be17d-163">**SPLREG\_PRINT\_DRIVER\_ISOLATION\_GROUPS**</span></span>                        | <span data-ttu-id="be17d-164">Windows 7 и более поздние версии</span><span class="sxs-lookup"><span data-stu-id="be17d-164">Windows 7 and later</span></span><br/>                                                                                                                                                                                                  |
| <span data-ttu-id="be17d-165">**СПЛРЕГ \_ \_ \_ время изоляции драйвера \_ печати \_ перед \_ повторным запуском**</span><span class="sxs-lookup"><span data-stu-id="be17d-165">**SPLREG\_PRINT\_DRIVER\_ISOLATION\_TIME\_BEFORE\_RECYCLE**</span></span>         | <span data-ttu-id="be17d-166">Windows 7 и более поздние версии</span><span class="sxs-lookup"><span data-stu-id="be17d-166">Windows 7 and later</span></span><br/>                                                                                                                                                                                                  |
| <span data-ttu-id="be17d-167">**СПЛРЕГ \_ \_ \_ \_ Максимальное число объектов изоляции драйвера печати \_ \_ перед \_ повторным запуском**</span><span class="sxs-lookup"><span data-stu-id="be17d-167">**SPLREG\_PRINT\_DRIVER\_ISOLATION\_MAX\_OBJECTS\_BEFORE\_RECYCLE**</span></span> | <span data-ttu-id="be17d-168">Windows 7 и более поздние версии</span><span class="sxs-lookup"><span data-stu-id="be17d-168">Windows 7 and later</span></span><br/>                                                                                                                                                                                                  |
| <span data-ttu-id="be17d-169">**СПЛРЕГ \_ \_ \_ \_ время ожидания простоя для изоляции драйвера печати \_**</span><span class="sxs-lookup"><span data-stu-id="be17d-169">**SPLREG\_PRINT\_DRIVER\_ISOLATION\_IDLE\_TIMEOUT**</span></span>                 | <span data-ttu-id="be17d-170">Windows 7 и более поздние версии</span><span class="sxs-lookup"><span data-stu-id="be17d-170">Windows 7 and later</span></span><br/>                                                                                                                                                                                                  |
| <span data-ttu-id="be17d-171">**\_ \_ \_ \_ Политика выполнения изоляции драйвера печати \_ сплрег**</span><span class="sxs-lookup"><span data-stu-id="be17d-171">**SPLREG\_PRINT\_DRIVER\_ISOLATION\_EXECUTION\_POLICY**</span></span>             | <span data-ttu-id="be17d-172">Windows 7 и более поздние версии</span><span class="sxs-lookup"><span data-stu-id="be17d-172">Windows 7 and later</span></span><br/>                                                                                                                                                                                                  |
| <span data-ttu-id="be17d-173">**\_ \_ \_ Политика переопределения режима изоляции \_ драйвера \_ печати сплрег**</span><span class="sxs-lookup"><span data-stu-id="be17d-173">**SPLREG\_PRINT\_DRIVER\_ISOLATION\_OVERRIDE\_POLICY**</span></span>              | <span data-ttu-id="be17d-174">Windows 7 и более поздние версии</span><span class="sxs-lookup"><span data-stu-id="be17d-174">Windows 7 and later</span></span><br/>                                                                                                                                                                                                  |
| <span data-ttu-id="be17d-175">**\_Удаленный \_ Факс сплрег**</span><span class="sxs-lookup"><span data-stu-id="be17d-175">**SPLREG\_REMOTE\_FAX**</span></span>                                             | <span data-ttu-id="be17d-176">При успешном возвращении *pData* содержит 0x0001, если служба факсов поддерживает удаленные клиенты. в противном случае — 0.</span><span class="sxs-lookup"><span data-stu-id="be17d-176">On successful return, *pData* contains 0x0001 if the FAX service supports remote clients, 0 otherwise.</span></span><br/>                                                                                                               |
| <span data-ttu-id="be17d-177">**\_всплывающее окно повторной попытки сплрег \_**</span><span class="sxs-lookup"><span data-stu-id="be17d-177">**SPLREG\_RETRY\_POPUP**</span></span>                                            | <span data-ttu-id="be17d-178">При успешном возвращении *pData* содержит 1, если на сервере настроено повторное открытие всплывающих окон для всех заданий, или значение 0, если сервер не пытается повторно открывать всплывающие окна для всех заданий.</span><span class="sxs-lookup"><span data-stu-id="be17d-178">On successful return, *pData* contains 1 if server is set to retry pop-up windows for all jobs, or 0 if server does not retry pop-up windows for all jobs.</span></span><br/> <span data-ttu-id="be17d-179">Не поддерживается в Windows Server 2003 и более поздних версиях</span><span class="sxs-lookup"><span data-stu-id="be17d-179">Not supported in Windows Server 2003 and later</span></span><br/> |
| <span data-ttu-id="be17d-180">**\_приоритет потока планировщика сплрег \_ \_**</span><span class="sxs-lookup"><span data-stu-id="be17d-180">**SPLREG\_SCHEDULER\_THREAD\_PRIORITY**</span></span>                             |                                                                                                                                                                                                                                 |
| <span data-ttu-id="be17d-181">**\_приоритет потока планировщика сплрег \_ \_ \_ по умолчанию**</span><span class="sxs-lookup"><span data-stu-id="be17d-181">**SPLREG\_SCHEDULER\_THREAD\_PRIORITY\_DEFAULT**</span></span>                    |                                                                                                                                                                                                                                 |
| <span data-ttu-id="be17d-182">**СПЛРЕГ \_ вебшаремгмт**</span><span class="sxs-lookup"><span data-stu-id="be17d-182">**SPLREG\_WEBSHAREMGMT**</span></span>                                            | <span data-ttu-id="be17d-183">Windows Server 2003 и более поздние версии</span><span class="sxs-lookup"><span data-stu-id="be17d-183">Windows Server 2003 and later</span></span><br/>                                                                                                                                                                                        |



 

<span data-ttu-id="be17d-184">Следующие значения *пвалуенаме* указывают на поведение печати пула при возникновении ошибки.</span><span class="sxs-lookup"><span data-stu-id="be17d-184">The following values of *pValueName* indicate the pool printing behavior when an error occurs.</span></span>



| <span data-ttu-id="be17d-185">Значение</span><span class="sxs-lookup"><span data-stu-id="be17d-185">Value</span></span>                                       | <span data-ttu-id="be17d-186">Комментарии</span><span class="sxs-lookup"><span data-stu-id="be17d-186">Comments</span></span>                                                                                                                                                                                              |
|---------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="be17d-187">**\_сбой задания перезапуска сплрег \_ \_ при \_ \_ ошибке пула**</span><span class="sxs-lookup"><span data-stu-id="be17d-187">**SPLREG\_RESTART\_JOB\_ON\_POOL\_ERROR**</span></span>   | <span data-ttu-id="be17d-188">Значение *pData* указывает время в секундах, когда задание перезапускается на другом порте после возникновения ошибки.</span><span class="sxs-lookup"><span data-stu-id="be17d-188">The value of *pData* indicates the time, in seconds, when a job is restarted on another port after an error occurs.</span></span> <span data-ttu-id="be17d-189">Этот параметр используется при **\_ \_ \_ \_ \_ включении задания перезапуска сплрег в пуле**.</span><span class="sxs-lookup"><span data-stu-id="be17d-189">This setting is used with **SPLREG\_RESTART\_JOB\_ON\_POOL\_ENABLED**.</span></span><br/> |
| <span data-ttu-id="be17d-190">**\_Задание перезапуска сплрег \_ \_ в \_ пуле \_ включено**</span><span class="sxs-lookup"><span data-stu-id="be17d-190">**SPLREG\_RESTART\_JOB\_ON\_POOL\_ENABLED**</span></span> | <span data-ttu-id="be17d-191">Ненулевое значение в *pData* указывает, что включено **\_ Задание перезапуска сплрег \_ \_ при \_ \_ ошибке пула** .</span><span class="sxs-lookup"><span data-stu-id="be17d-191">A nonzero value in *pData* indicates that **SPLREG\_RESTART\_JOB\_ON\_POOL\_ERROR** is enabled.</span></span><br/>                                                                                            |



 

<span data-ttu-id="be17d-192">Время, указанное в **\_ задании перезапуска сплрег \_ \_ в случае \_ \_ ошибки пула** , является минимальным временем.</span><span class="sxs-lookup"><span data-stu-id="be17d-192">The time specified in **SPLREG\_RESTART\_JOB\_ON\_POOL\_ERROR** is a minimum time.</span></span> <span data-ttu-id="be17d-193">Фактическое время может быть больше, в зависимости от следующих параметров монитора портов, которые являются значениями реестра в этом разделе реестра:</span><span class="sxs-lookup"><span data-stu-id="be17d-193">The actual time can be longer, depending on the following port monitor settings, which are registry values under this registry key:</span></span>

<span data-ttu-id="be17d-194">**HKLM \\ System CurrentControlSet Control Monitoring MONITORS \\ \\ \\ \\ \\ < *мониторнаме* > \\ ports**</span><span class="sxs-lookup"><span data-stu-id="be17d-194">**HKLM\\SYSTEM\\CurrentControlSet\\Control\\Print\\Monitors\\<*MonitorName*>\\Ports**</span></span>

<span data-ttu-id="be17d-195">Чтобы запросить эти значения, вызовите функцию [**процедура RegQueryValueEx**](/windows/win32/api/winreg/nf-winreg-regqueryvalueexa) .</span><span class="sxs-lookup"><span data-stu-id="be17d-195">Call the [**RegQueryValueEx**](/windows/win32/api/winreg/nf-winreg-regqueryvalueexa) function to query these values.</span></span>



| <span data-ttu-id="be17d-196">Параметр монитора порта</span><span class="sxs-lookup"><span data-stu-id="be17d-196">Port monitor setting</span></span>     | <span data-ttu-id="be17d-197">Тип данных</span><span class="sxs-lookup"><span data-stu-id="be17d-197">Data type</span></span>      | <span data-ttu-id="be17d-198">Значение</span><span class="sxs-lookup"><span data-stu-id="be17d-198">Meaning</span></span>                                                                                                        |
|--------------------------|----------------|----------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="be17d-199">**статусупдатинаблед**</span><span class="sxs-lookup"><span data-stu-id="be17d-199">**StatusUpdateEnabled**</span></span>  | <span data-ttu-id="be17d-200">**REG \_ DWORD**</span><span class="sxs-lookup"><span data-stu-id="be17d-200">**REG\_DWORD**</span></span> | <span data-ttu-id="be17d-201">При ненулевом значении разрешает монитору портов обновлять Диспетчер очереди с состоянием порта.</span><span class="sxs-lookup"><span data-stu-id="be17d-201">If a nonzero value, enables the port monitor to update the spooler with the port status.</span></span><br/>            |
| <span data-ttu-id="be17d-202">**статусупдатеинтервал**</span><span class="sxs-lookup"><span data-stu-id="be17d-202">**StatusUpdateInterval**</span></span> | <span data-ttu-id="be17d-203">**REG \_ DWORD**</span><span class="sxs-lookup"><span data-stu-id="be17d-203">**REG\_DWORD**</span></span> | <span data-ttu-id="be17d-204">Указывает интервал (в минутах), в течение которого монитор порта обновляет Диспетчер очереди с состоянием порта.</span><span class="sxs-lookup"><span data-stu-id="be17d-204">Specifies the interval, in minutes, when the port monitor updates the spooler with the port status.</span></span><br/> |



 

<span data-ttu-id="be17d-205">В Windows 7 и более поздних версиях Windows задания печати, отправленные на сервер печати, по умолчанию подготавливаются к просмотру на клиенте.</span><span class="sxs-lookup"><span data-stu-id="be17d-205">In Windows 7 and later versions of Windows, print jobs that are sent to a print server are rendered on the client by default.</span></span> <span data-ttu-id="be17d-206">Следующие значения настраивают отрисовку заданий печати на стороне клиента и могут быть считаны, если в *пвалуенаме* заданы следующие значения.</span><span class="sxs-lookup"><span data-stu-id="be17d-206">The following values configure client-side rendering of a print jobs and can be read if you set the following values in *pValueName*.</span></span>



| <span data-ttu-id="be17d-207">Параметр</span><span class="sxs-lookup"><span data-stu-id="be17d-207">Setting</span></span>                      | <span data-ttu-id="be17d-208">Тип данных</span><span class="sxs-lookup"><span data-stu-id="be17d-208">Data type</span></span>      | <span data-ttu-id="be17d-209">Описание</span><span class="sxs-lookup"><span data-stu-id="be17d-209">Description</span></span>                                                                                                                                                                                                                                                                                                                                                                                                       |
|------------------------------|----------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="be17d-210">**емфдеспулингсеттинг**</span><span class="sxs-lookup"><span data-stu-id="be17d-210">**EMFDespoolingSetting**</span></span>     | <span data-ttu-id="be17d-211">**REG \_ DWORD**</span><span class="sxs-lookup"><span data-stu-id="be17d-211">**REG\_DWORD**</span></span> | <span data-ttu-id="be17d-212">Значение 0 или, если это значение отсутствует в реестре, включает отрисовку заданий печати на стороне клиента по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="be17d-212">A value of 0, or if this value is not present in the registry, enables the default client-side rendering of print jobs.</span></span><br/> <span data-ttu-id="be17d-213">Значение 1 отключает отрисовку заданий печати на стороне клиента.</span><span class="sxs-lookup"><span data-stu-id="be17d-213">A value of 1 disables client-side rendering of print jobs.</span></span><br/>                                                                                                                                                                                                          |
| <span data-ttu-id="be17d-214">**форцеклиентсидерендеринг**</span><span class="sxs-lookup"><span data-stu-id="be17d-214">**ForceClientSideRendering**</span></span> | <span data-ttu-id="be17d-215">**REG \_ DWORD**</span><span class="sxs-lookup"><span data-stu-id="be17d-215">**REG\_DWORD**</span></span> | <span data-ttu-id="be17d-216">Значение 0 или, если это значение отсутствует в реестре, приведет к отображению заданий печати на клиенте.</span><span class="sxs-lookup"><span data-stu-id="be17d-216">A value of 0, or if this value is not present in the registry, will cause the print jobs to be rendered on the client.</span></span> <span data-ttu-id="be17d-217">Если задание печати не может быть визуализировано на клиенте, оно будет подготовлено к просмотру на сервере.</span><span class="sxs-lookup"><span data-stu-id="be17d-217">If a print job cannot be rendered on the client, it will be rendered on the server.</span></span> <span data-ttu-id="be17d-218">Если задание печати не может быть подготовлено к просмотру на сервере, оно завершится ошибкой.</span><span class="sxs-lookup"><span data-stu-id="be17d-218">If a print job cannot be rendered on the server, it will fail.</span></span><br/> <span data-ttu-id="be17d-219">Значение 1 будет отображать задания печати на клиенте.</span><span class="sxs-lookup"><span data-stu-id="be17d-219">A value of 1 will render print jobs on the client.</span></span> <span data-ttu-id="be17d-220">Если задание печати не может быть визуализировано на клиенте, оно завершится ошибкой.</span><span class="sxs-lookup"><span data-stu-id="be17d-220">If a print job cannot be rendered on the client, it will fail.</span></span><br/> |



 

## <a name="requirements"></a><span data-ttu-id="be17d-221">Требования</span><span class="sxs-lookup"><span data-stu-id="be17d-221">Requirements</span></span>



| <span data-ttu-id="be17d-222">Требование</span><span class="sxs-lookup"><span data-stu-id="be17d-222">Requirement</span></span> | <span data-ttu-id="be17d-223">Значение</span><span class="sxs-lookup"><span data-stu-id="be17d-223">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="be17d-224">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="be17d-224">Minimum supported client</span></span><br/> | <span data-ttu-id="be17d-225">Windows 2000 Professional \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="be17d-225">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                                |
| <span data-ttu-id="be17d-226">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="be17d-226">Minimum supported server</span></span><br/> | <span data-ttu-id="be17d-227">Windows 2000 Server \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="be17d-227">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                      |
| <span data-ttu-id="be17d-228">Заголовок</span><span class="sxs-lookup"><span data-stu-id="be17d-228">Header</span></span><br/>                   | <dl> <span data-ttu-id="be17d-229"><dt>Винспул. h (включение Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="be17d-229"><dt>Winspool.h (include Windows.h)</dt></span></span> </dl> |
| <span data-ttu-id="be17d-230">Библиотека</span><span class="sxs-lookup"><span data-stu-id="be17d-230">Library</span></span><br/>                  | <dl> <span data-ttu-id="be17d-231"><dt>Винспул. lib</dt></span><span class="sxs-lookup"><span data-stu-id="be17d-231"><dt>Winspool.lib</dt></span></span> </dl>                   |
| <span data-ttu-id="be17d-232">DLL</span><span class="sxs-lookup"><span data-stu-id="be17d-232">DLL</span></span><br/>                      | <dl> <span data-ttu-id="be17d-233"><dt>Винспул. drv</dt></span><span class="sxs-lookup"><span data-stu-id="be17d-233"><dt>Winspool.drv</dt></span></span> </dl>                   |
| <span data-ttu-id="be17d-234">Имя в кодировке Юникод и ANSI</span><span class="sxs-lookup"><span data-stu-id="be17d-234">Unicode and ANSI names</span></span><br/>   | <span data-ttu-id="be17d-235">**Жетпринтердатав** (Юникод) и **жетпринтердатаа** (ANSI)</span><span class="sxs-lookup"><span data-stu-id="be17d-235">**GetPrinterDataW** (Unicode) and **GetPrinterDataA** (ANSI)</span></span><br/>                                   |



## <a name="see-also"></a><span data-ttu-id="be17d-236">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="be17d-236">See also</span></span>

<dl> <dt>

[<span data-ttu-id="be17d-237">Вывод на печать</span><span class="sxs-lookup"><span data-stu-id="be17d-237">Printing</span></span>](printdocs-printing.md)
</dt> <dt>

[<span data-ttu-id="be17d-238">Функции API очереди печати принтера</span><span class="sxs-lookup"><span data-stu-id="be17d-238">Print Spooler API Functions</span></span>](printing-and-print-spooler-functions.md)
</dt> <dt>

[<span data-ttu-id="be17d-239">**жетпринтердатаекс**</span><span class="sxs-lookup"><span data-stu-id="be17d-239">**GetPrinterDataEx**</span></span>](getprinterdataex.md)
</dt> <dt>

[<span data-ttu-id="be17d-240">**опенпринтер**</span><span class="sxs-lookup"><span data-stu-id="be17d-240">**OpenPrinter**</span></span>](openprinter.md)
</dt> <dt>

[<span data-ttu-id="be17d-241">**сетпринтер**</span><span class="sxs-lookup"><span data-stu-id="be17d-241">**SetPrinter**</span></span>](setprinter.md)
</dt> <dt>

[<span data-ttu-id="be17d-242">**сетпринтердата**</span><span class="sxs-lookup"><span data-stu-id="be17d-242">**SetPrinterData**</span></span>](setprinterdata.md)
</dt> <dt>

[<span data-ttu-id="be17d-243">**сетпринтердатаекс**</span><span class="sxs-lookup"><span data-stu-id="be17d-243">**SetPrinterDataEx**</span></span>](setprinterdataex.md)
</dt> <dt>

[<span data-ttu-id="be17d-244">**ПРИНТПРОЦЕССОР \_ Cap \_ 1**</span><span class="sxs-lookup"><span data-stu-id="be17d-244">**PRINTPROCESSOR\_CAPS\_1**</span></span>](printprocessor-caps-1.md)
</dt> </dl>

 

