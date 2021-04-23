---
description: Функция PrintOut получает сведения о указанном принтере.
ms.assetid: f162edbb-83ee-40c3-8710-9c867301d652
title: Функция PrintOut (Винспул. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- GetPrinter
- GetPrinterA
- GetPrinterW
api_type:
- DllExport
api_location:
- Winspool.drv
- Ext-MS-Win-printer-Winspool-l1-1-0.dll
- Ext-MS-Win-printer-Winspool-l1-1-1.dll
- Ext-MS-Win-Printer-WinSpool-l1-1-2.dll
- Ext-MS-Win-Printer-WinSpool-L1-1-3.dll
ms.openlocfilehash: e99b3574762b84b830845da8149b0406664b6da7
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "105703075"
---
# <a name="getprinter-function"></a><span data-ttu-id="a5132-103">Функция PrintOut</span><span class="sxs-lookup"><span data-stu-id="a5132-103">GetPrinter function</span></span>

<span data-ttu-id="a5132-104">Функция **PrintOut** получает сведения о указанном принтере.</span><span class="sxs-lookup"><span data-stu-id="a5132-104">The **GetPrinter** function retrieves information about a specified printer.</span></span>

## <a name="syntax"></a><span data-ttu-id="a5132-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="a5132-105">Syntax</span></span>


```C++
BOOL GetPrinter(
  _In_  HANDLE  hPrinter,
  _In_  DWORD   Level,
  _Out_ LPBYTE  pPrinter,
  _In_  DWORD   cbBuf,
  _Out_ LPDWORD pcbNeeded
);
```



## <a name="parameters"></a><span data-ttu-id="a5132-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="a5132-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="a5132-107">*хпринтер* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="a5132-107">*hPrinter* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="a5132-108">Описатель принтера, для которого функция получает сведения.</span><span class="sxs-lookup"><span data-stu-id="a5132-108">A handle to the printer for which the function retrieves information.</span></span> <span data-ttu-id="a5132-109">Используйте функцию [**опенпринтер**](openprinter.md) или [**аддпринтер**](addprinter.md) для получения маркера принтера.</span><span class="sxs-lookup"><span data-stu-id="a5132-109">Use the [**OpenPrinter**](openprinter.md) or [**AddPrinter**](addprinter.md) function to retrieve a printer handle.</span></span>

</dd> <dt>

<span data-ttu-id="a5132-110">*Уровень* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="a5132-110">*Level* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="a5132-111">Уровень или тип структуры, которую функция хранит в буфере, на который указывает *ппринтер*.</span><span class="sxs-lookup"><span data-stu-id="a5132-111">The level or type of structure that the function stores into the buffer pointed to by *pPrinter*.</span></span>

<span data-ttu-id="a5132-112">Это значение может быть равно 1, 2, 3, 4, 5, 6, 7, 8 или 9.</span><span class="sxs-lookup"><span data-stu-id="a5132-112">This value can be 1, 2, 3, 4, 5, 6, 7, 8 or 9.</span></span>

</dd> <dt>

<span data-ttu-id="a5132-113">*ппринтер* \[ заполняет\]</span><span class="sxs-lookup"><span data-stu-id="a5132-113">*pPrinter* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="a5132-114">Указатель на буфер, который получает структуру, содержащую сведения о указанном принтере.</span><span class="sxs-lookup"><span data-stu-id="a5132-114">A pointer to a buffer that receives a structure containing information about the specified printer.</span></span> <span data-ttu-id="a5132-115">Буфер должен быть достаточно большим, чтобы получить структуру и любые строки или другие данные, на которые указывает элемент структуры.</span><span class="sxs-lookup"><span data-stu-id="a5132-115">The buffer must be large enough to receive the structure and any strings or other data to which the structure members point.</span></span> <span data-ttu-id="a5132-116">Если буфер слишком мал, параметр *пкбнидед* возвращает требуемый размер буфера.</span><span class="sxs-lookup"><span data-stu-id="a5132-116">If the buffer is too small, the *pcbNeeded* parameter returns the required buffer size.</span></span>

<span data-ttu-id="a5132-117">Тип структуры определяется значением *Level*.</span><span class="sxs-lookup"><span data-stu-id="a5132-117">The type of structure is determined by the value of *Level*.</span></span>



| <span data-ttu-id="a5132-118">Level</span><span class="sxs-lookup"><span data-stu-id="a5132-118">Level</span></span>                                                                                                | <span data-ttu-id="a5132-119">Структура</span><span class="sxs-lookup"><span data-stu-id="a5132-119">Structure</span></span>                                                                                                                                                                                                        |
|------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="1"></span><dl> <span data-ttu-id="a5132-120"><dt>**1**</dt></span><span class="sxs-lookup"><span data-stu-id="a5132-120"><dt>**1**</dt></span></span> </dl> | <span data-ttu-id="a5132-121">Структура [**принтера с информацией \_ \_ 1**](printer-info-1.md) , содержащая общие сведения о принтере.</span><span class="sxs-lookup"><span data-stu-id="a5132-121">A [**PRINTER\_INFO\_1**](printer-info-1.md) structure containing general printer information.</span></span><br/>                                                                                                        |
| <span id="2"></span><dl> <span data-ttu-id="a5132-122"><dt>**2**</dt></span><span class="sxs-lookup"><span data-stu-id="a5132-122"><dt>**2**</dt></span></span> </dl> | <span data-ttu-id="a5132-123">Структура [**сведений о принтере \_ \_ 2**](printer-info-2.md) , содержащая подробные сведения о принтере.</span><span class="sxs-lookup"><span data-stu-id="a5132-123">A [**PRINTER\_INFO\_2**](printer-info-2.md) structure containing detailed information about the printer.</span></span><br/>                                                                                             |
| <span id="3"></span><dl> <span data-ttu-id="a5132-124"><dt>**3-5**</dt></span><span class="sxs-lookup"><span data-stu-id="a5132-124"><dt>**3**</dt></span></span> </dl> | <span data-ttu-id="a5132-125">Структура [**принтера \_ info \_ 3**](printer-info-3.md) , содержащая сведения о безопасности принтера.</span><span class="sxs-lookup"><span data-stu-id="a5132-125">A [**PRINTER\_INFO\_3**](printer-info-3.md) structure containing the printer's security information.</span></span><br/>                                                                                                 |
| <span id="4"></span><dl> <span data-ttu-id="a5132-126"><dt>**четырех**</dt></span><span class="sxs-lookup"><span data-stu-id="a5132-126"><dt>**4**</dt></span></span> </dl> | <span data-ttu-id="a5132-127">Структура [**принтера с информацией \_ \_ 4**](printer-info-4.md) , содержащая минимальные сведения о принтерах, включая имя принтера, имя сервера, а также то, является ли принтер удаленным или локальным.</span><span class="sxs-lookup"><span data-stu-id="a5132-127">A [**PRINTER\_INFO\_4**](printer-info-4.md) structure containing minimal printer information, including the name of the printer, the name of the server, and whether the printer is remote or local.</span></span><br/> |
| <span id="5"></span><dl> <span data-ttu-id="a5132-128"><dt>**5.0**</dt></span><span class="sxs-lookup"><span data-stu-id="a5132-128"><dt>**5**</dt></span></span> </dl> | <span data-ttu-id="a5132-129">Структура сведений о принтере [**\_ \_ 5**](printer-info-5.md) , содержащая сведения о принтерах, такие как атрибуты принтера и параметры времени ожидания.</span><span class="sxs-lookup"><span data-stu-id="a5132-129">A [**PRINTER\_INFO\_5**](printer-info-5.md) structure containing printer information such as printer attributes and time-out settings.</span></span><br/>                                                               |
| <span id="6"></span><dl> <span data-ttu-id="a5132-130"><dt>**6**</dt></span><span class="sxs-lookup"><span data-stu-id="a5132-130"><dt>**6**</dt></span></span> </dl> | <span data-ttu-id="a5132-131">Структура [**принтера с \_ информацией \_ 6**](printer-info-6.md) , указывающая значение состояния принтера.</span><span class="sxs-lookup"><span data-stu-id="a5132-131">A [**PRINTER\_INFO\_6**](printer-info-6.md) structure specifying the status value of a printer.</span></span><br/>                                                                                                      |
| <span id="7"></span><dl> <span data-ttu-id="a5132-132"><dt>**7**</dt></span><span class="sxs-lookup"><span data-stu-id="a5132-132"><dt>**7**</dt></span></span> </dl> | <span data-ttu-id="a5132-133">Структура [**принтера с \_ информацией \_ 7**](printer-info-7.md) , указывающая, опубликован ли принтер в службе каталогов.</span><span class="sxs-lookup"><span data-stu-id="a5132-133">A [**PRINTER\_INFO\_7**](printer-info-7.md) structure that indicates whether the printer is published in the directory service.</span></span><br/>                                                                      |
| <span id="8"></span><dl> <span data-ttu-id="a5132-134"><dt>**8**</dt></span><span class="sxs-lookup"><span data-stu-id="a5132-134"><dt>**8**</dt></span></span> </dl> | <span data-ttu-id="a5132-135">Структура [**принтера \_ info \_ 8**](printer-info-8.md) , указывающая глобальные параметры принтера по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="a5132-135">A [**PRINTER\_INFO\_8**](printer-info-8.md) structure specifying the global default printer settings.</span></span><br/>                                                                                                |
| <span id="9"></span><dl> <span data-ttu-id="a5132-136"><dt>**9**</dt></span><span class="sxs-lookup"><span data-stu-id="a5132-136"><dt>**9**</dt></span></span> </dl> | <span data-ttu-id="a5132-137">Структура [**принтера с \_ информацией \_ 9**](printer-info-9.md) , указывающая параметры принтера по умолчанию для каждого пользователя.</span><span class="sxs-lookup"><span data-stu-id="a5132-137">A [**PRINTER\_INFO\_9**](printer-info-9.md) structure specifying the per-user default printer settings.</span></span><br/>                                                                                              |



 

</dd> <dt>

<span data-ttu-id="a5132-138">*кббуф* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="a5132-138">*cbBuf* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="a5132-139">Размер (в байтах) буфера, на который указывает *ппринтер*.</span><span class="sxs-lookup"><span data-stu-id="a5132-139">The size, in bytes, of the buffer pointed to by *pPrinter*.</span></span>

</dd> <dt>

<span data-ttu-id="a5132-140">*пкбнидед* \[ заполняет\]</span><span class="sxs-lookup"><span data-stu-id="a5132-140">*pcbNeeded* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="a5132-141">Указатель на переменную, для которой в качестве функции задается размер (в байтах) сведений о принтере.</span><span class="sxs-lookup"><span data-stu-id="a5132-141">A pointer to a variable that the function sets to the size, in bytes, of the printer information.</span></span> <span data-ttu-id="a5132-142">Если значение *кббуф* меньше этого значения, то не удается выполнить **Печать** , а значение представляет требуемый размер буфера.</span><span class="sxs-lookup"><span data-stu-id="a5132-142">If *cbBuf* is smaller than this value, **GetPrinter** fails, and the value represents the required buffer size.</span></span> <span data-ttu-id="a5132-143">Если значение *кббуф* равно или больше этого значения, то будет выполнен **Повтор** , а значение представляет число байтов, хранящихся в буфере.</span><span class="sxs-lookup"><span data-stu-id="a5132-143">If *cbBuf* is equal to or greater than this value, **GetPrinter** succeeds, and the value represents the number of bytes stored in the buffer.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="a5132-144">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="a5132-144">Return value</span></span>

<span data-ttu-id="a5132-145">Если функция выполнена, возвращаемое значение будет ненулевым.</span><span class="sxs-lookup"><span data-stu-id="a5132-145">If the function succeeds, the return value is a nonzero value.</span></span>

<span data-ttu-id="a5132-146">Если функция выполняется неудачно, возвращается нулевое значение.</span><span class="sxs-lookup"><span data-stu-id="a5132-146">If the function fails, the return value is zero.</span></span>

## <a name="remarks"></a><span data-ttu-id="a5132-147">Комментарии</span><span class="sxs-lookup"><span data-stu-id="a5132-147">Remarks</span></span>

> [!Note]  
> <span data-ttu-id="a5132-148">Это блокирующая или синхронная функция, которая может не возвращать значение немедленно.</span><span class="sxs-lookup"><span data-stu-id="a5132-148">This is a blocking or synchronous function and might not return immediately.</span></span> <span data-ttu-id="a5132-149">Скорость возврата этой функцией зависит от факторов времени выполнения, таких как состояние сети, Конфигурация сервера печати и факторы реализации драйвера принтера, которые трудно предсказать при написании приложения.</span><span class="sxs-lookup"><span data-stu-id="a5132-149">How quickly this function returns depends on run-time factors such as network status, print server configuration, and printer driver implementation factors that are difficult to predict when writing an application.</span></span> <span data-ttu-id="a5132-150">Вызов этой функции из потока, который управляет взаимодействием с пользовательским интерфейсом, может привести к невозможности реагирования приложения.</span><span class="sxs-lookup"><span data-stu-id="a5132-150">Calling this function from a thread that manages interaction with the user interface could make the application appear to be unresponsive.</span></span>

 

<span data-ttu-id="a5132-151">Элемент **пдевмоде** в структурах [**принтера \_ \_ 2**](printer-info-2.md), [**\_ сведения о принтере \_ 8**](printer-info-8.md)и [**\_ сведения о принтере \_ 9**](printer-info-9.md) могут иметь **значение NULL**.</span><span class="sxs-lookup"><span data-stu-id="a5132-151">The **pDevMode** member in the [**PRINTER\_INFO\_2**](printer-info-2.md), [**PRINTER\_INFO\_8**](printer-info-8.md), and [**PRINTER\_INFO\_9**](printer-info-9.md) structures can be **NULL**.</span></span> <span data-ttu-id="a5132-152">В этом случае принтер непригоден для использования, пока драйвер не будет успешно переустановлен.</span><span class="sxs-lookup"><span data-stu-id="a5132-152">When this happens, the printer is unusable until the driver is reinstalled successfully.</span></span>

<span data-ttu-id="a5132-153">Для структур [**" \_ сведения \_ о принтере 2**](printer-info-2.md) " и " [**\_ сведения о принтере \_ 3**](printer-info-3.md) ", которые содержат указатель на дескриптор безопасности, эта функция извлекает только те компоненты дескриптора безопасности, которые у вызывающего объекта есть разрешение на чтение.</span><span class="sxs-lookup"><span data-stu-id="a5132-153">For the [**PRINTER\_INFO\_2**](printer-info-2.md) and [**PRINTER\_INFO\_3**](printer-info-3.md) structures that contain a pointer to a security descriptor, the function retrieves only those components of the security descriptor that the caller has permission to read.</span></span> <span data-ttu-id="a5132-154">Чтобы получить определенные компоненты дескриптора безопасности, необходимо указать необходимые права доступа при вызове функции [**опенпринтер**](openprinter.md) для получения дескриптора принтера.</span><span class="sxs-lookup"><span data-stu-id="a5132-154">To retrieve particular security descriptor components, you must specify the necessary access rights when you call the [**OpenPrinter**](openprinter.md) function to retrieve a handle to the printer.</span></span> <span data-ttu-id="a5132-155">В следующей таблице показаны права доступа, необходимые для чтения различных компонентов дескриптора безопасности.</span><span class="sxs-lookup"><span data-stu-id="a5132-155">The following table shows the access rights required to read the various security descriptor components.</span></span>



| <span data-ttu-id="a5132-156">Право доступа</span><span class="sxs-lookup"><span data-stu-id="a5132-156">Access Right</span></span>                        | <span data-ttu-id="a5132-157">Компонент дескриптора безопасности</span><span class="sxs-lookup"><span data-stu-id="a5132-157">Security Descriptor Component</span></span>                                                                 |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| <span data-ttu-id="a5132-158">\_Контроль чтения</span><span class="sxs-lookup"><span data-stu-id="a5132-158">READ\_CONTROL</span></span><br/>            | <span data-ttu-id="a5132-159">Владелец</span><span class="sxs-lookup"><span data-stu-id="a5132-159">Owner</span></span><br/> <span data-ttu-id="a5132-160">Основная группа</span><span class="sxs-lookup"><span data-stu-id="a5132-160">Primary group</span></span><br/> <span data-ttu-id="a5132-161">Список управления доступом на уровне пользователей (DACL)</span><span class="sxs-lookup"><span data-stu-id="a5132-161">Discretionary access-control list (DACL)</span></span><br/> |
| <span data-ttu-id="a5132-162">ДОСТУП \_ к \_ безопасности системы</span><span class="sxs-lookup"><span data-stu-id="a5132-162">ACCESS\_SYSTEM\_SECURITY</span></span><br/> | <span data-ttu-id="a5132-163">Системный доступ — список управления (SACL)</span><span class="sxs-lookup"><span data-stu-id="a5132-163">System access-control list (SACL)</span></span><br/>                                                  |



 

<span data-ttu-id="a5132-164">Если указан уровень 7, элемент **двактион** в [**\_ сведениях о принтере \_ 7**](printer-info-7.md) возвращает одно из следующих значений, чтобы указать, опубликован ли принтер в службе каталогов.</span><span class="sxs-lookup"><span data-stu-id="a5132-164">If you specify level 7, the **dwAction** member of [**PRINTER\_INFO\_7**](printer-info-7.md) returns one of the following values to indicate whether the printer is published in the directory service.</span></span>



| <span data-ttu-id="a5132-165">значение Двактион</span><span class="sxs-lookup"><span data-stu-id="a5132-165">dwAction value</span></span>     | <span data-ttu-id="a5132-166">Значение</span><span class="sxs-lookup"><span data-stu-id="a5132-166">Meaning</span></span>                                                                                                                                                                                                                                                  |
|--------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="a5132-167">\_Публикация дспринт</span><span class="sxs-lookup"><span data-stu-id="a5132-167">DSPRINT\_PUBLISH</span></span>   | <span data-ttu-id="a5132-168">Принтер опубликован.</span><span class="sxs-lookup"><span data-stu-id="a5132-168">The printer is published.</span></span> <span data-ttu-id="a5132-169">Член **псзобжектгуид** содержит идентификатор GUID объекта очереди печати служб каталогов, связанного с принтером.</span><span class="sxs-lookup"><span data-stu-id="a5132-169">The **pszObjectGUID** member contains the GUID of the directory services print queue object associated with the printer.</span></span>                                                                                                       |
| <span data-ttu-id="a5132-170">ДСПРИНТ \_ отменить публикацию</span><span class="sxs-lookup"><span data-stu-id="a5132-170">DSPRINT\_UNPUBLISH</span></span> | <span data-ttu-id="a5132-171">Принтер не опубликован.</span><span class="sxs-lookup"><span data-stu-id="a5132-171">The printer is not published.</span></span>                                                                                                                                                                                                                            |
| <span data-ttu-id="a5132-172">\_Ожидание дспринт</span><span class="sxs-lookup"><span data-stu-id="a5132-172">DSPRINT\_PENDING</span></span>   | <span data-ttu-id="a5132-173">Указывает, что система пытается завершить операцию публикации или отмены публикации.</span><span class="sxs-lookup"><span data-stu-id="a5132-173">Indicates that the system is attempting to complete a publish or unpublish operation.</span></span> <span data-ttu-id="a5132-174">Если при вызове [**сетпринтер**](setprinter.md) не удается опубликовать или отменить публикацию принтера, система выполняет дальнейшие попытки выполнить операцию в фоновом режиме.</span><span class="sxs-lookup"><span data-stu-id="a5132-174">If a [**SetPrinter**](setprinter.md) call fails to publish or unpublish a printer, the system makes further attempts to complete the operation in the background.</span></span> |



 

<span data-ttu-id="a5132-175">Начиная с Windows Vista, данные принтера, возвращаемые методом **PrintOut** , получаются из локального кэша, когда *хпринтер* ссылается на принтер, размещенный на сервере печати, и существует по крайней мере одно открытое соединение с сервером печати.</span><span class="sxs-lookup"><span data-stu-id="a5132-175">Starting with Windows Vista, the printer data returned by **GetPrinter** is retrieved from a local cache when *hPrinter* refers to a printer hosted by a print server and there is at least one open connection to the print server.</span></span> <span data-ttu-id="a5132-176">Во всех остальных конфигурациях данные принтера запрашиваются с сервера печати.</span><span class="sxs-lookup"><span data-stu-id="a5132-176">In all other configurations, the printer data is queried from the print server.</span></span>

## <a name="requirements"></a><span data-ttu-id="a5132-177">Требования</span><span class="sxs-lookup"><span data-stu-id="a5132-177">Requirements</span></span>



| <span data-ttu-id="a5132-178">Требование</span><span class="sxs-lookup"><span data-stu-id="a5132-178">Requirement</span></span> | <span data-ttu-id="a5132-179">Значение</span><span class="sxs-lookup"><span data-stu-id="a5132-179">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="a5132-180">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="a5132-180">Minimum supported client</span></span><br/> | <span data-ttu-id="a5132-181">Windows 2000 Professional \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="a5132-181">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                                |
| <span data-ttu-id="a5132-182">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="a5132-182">Minimum supported server</span></span><br/> | <span data-ttu-id="a5132-183">Windows 2000 Server \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="a5132-183">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                      |
| <span data-ttu-id="a5132-184">Заголовок</span><span class="sxs-lookup"><span data-stu-id="a5132-184">Header</span></span><br/>                   | <dl> <span data-ttu-id="a5132-185"><dt>Винспул. h (включение Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="a5132-185"><dt>Winspool.h (include Windows.h)</dt></span></span> </dl> |
| <span data-ttu-id="a5132-186">Библиотека</span><span class="sxs-lookup"><span data-stu-id="a5132-186">Library</span></span><br/>                  | <dl> <span data-ttu-id="a5132-187"><dt>Винспул. lib</dt></span><span class="sxs-lookup"><span data-stu-id="a5132-187"><dt>Winspool.lib</dt></span></span> </dl>                   |
| <span data-ttu-id="a5132-188">DLL</span><span class="sxs-lookup"><span data-stu-id="a5132-188">DLL</span></span><br/>                      | <dl> <span data-ttu-id="a5132-189"><dt>Винспул. drv</dt></span><span class="sxs-lookup"><span data-stu-id="a5132-189"><dt>Winspool.drv</dt></span></span> </dl>                   |
| <span data-ttu-id="a5132-190">Имя в кодировке Юникод и ANSI</span><span class="sxs-lookup"><span data-stu-id="a5132-190">Unicode and ANSI names</span></span><br/>   | <span data-ttu-id="a5132-191">**Жетпринтерв** (Юникод) и a- **Printer** (ANSI)</span><span class="sxs-lookup"><span data-stu-id="a5132-191">**GetPrinterW** (Unicode) and **GetPrinterA** (ANSI)</span></span><br/>                                           |



## <a name="see-also"></a><span data-ttu-id="a5132-192">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="a5132-192">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a5132-193">Вывод на печать</span><span class="sxs-lookup"><span data-stu-id="a5132-193">Printing</span></span>](printdocs-printing.md)
</dt> <dt>

[<span data-ttu-id="a5132-194">Функции API очереди печати принтера</span><span class="sxs-lookup"><span data-stu-id="a5132-194">Print Spooler API Functions</span></span>](printing-and-print-spooler-functions.md)
</dt> <dt>

[<span data-ttu-id="a5132-195">**абортпринтер**</span><span class="sxs-lookup"><span data-stu-id="a5132-195">**AbortPrinter**</span></span>](abortprinter.md)
</dt> <dt>

[<span data-ttu-id="a5132-196">**аддпринтер**</span><span class="sxs-lookup"><span data-stu-id="a5132-196">**AddPrinter**</span></span>](addprinter.md)
</dt> <dt>

[<span data-ttu-id="a5132-197">**клосепринтер**</span><span class="sxs-lookup"><span data-stu-id="a5132-197">**ClosePrinter**</span></span>](closeprinter.md)
</dt> <dt>

[<span data-ttu-id="a5132-198">**делетепринтер**</span><span class="sxs-lookup"><span data-stu-id="a5132-198">**DeletePrinter**</span></span>](deleteprinter.md)
</dt> <dt>

[<span data-ttu-id="a5132-199">**енумпринтерс**</span><span class="sxs-lookup"><span data-stu-id="a5132-199">**EnumPrinters**</span></span>](enumprinters.md)
</dt> <dt>

[<span data-ttu-id="a5132-200">**\_Сведения о принтере \_ 1**</span><span class="sxs-lookup"><span data-stu-id="a5132-200">**PRINTER\_INFO\_1**</span></span>](printer-info-1.md)
</dt> <dt>

[<span data-ttu-id="a5132-201">**\_Сведения о принтере \_ 2**</span><span class="sxs-lookup"><span data-stu-id="a5132-201">**PRINTER\_INFO\_2**</span></span>](printer-info-2.md)
</dt> <dt>

[<span data-ttu-id="a5132-202">**\_Сведения о принтере \_ 3**</span><span class="sxs-lookup"><span data-stu-id="a5132-202">**PRINTER\_INFO\_3**</span></span>](printer-info-3.md)
</dt> <dt>

[<span data-ttu-id="a5132-203">**\_Сведения о принтере \_ 4**</span><span class="sxs-lookup"><span data-stu-id="a5132-203">**PRINTER\_INFO\_4**</span></span>](printer-info-4.md)
</dt> <dt>

[<span data-ttu-id="a5132-204">**\_Сведения о принтере \_ 5**</span><span class="sxs-lookup"><span data-stu-id="a5132-204">**PRINTER\_INFO\_5**</span></span>](printer-info-5.md)
</dt> <dt>

[<span data-ttu-id="a5132-205">**\_Сведения о принтере \_ 7**</span><span class="sxs-lookup"><span data-stu-id="a5132-205">**PRINTER\_INFO\_7**</span></span>](printer-info-7.md)
</dt> <dt>

[<span data-ttu-id="a5132-206">**\_Сведения о принтере \_ 8**</span><span class="sxs-lookup"><span data-stu-id="a5132-206">**PRINTER\_INFO\_8**</span></span>](printer-info-8.md)
</dt> <dt>

[<span data-ttu-id="a5132-207">**\_Сведения о принтере \_ 9**</span><span class="sxs-lookup"><span data-stu-id="a5132-207">**PRINTER\_INFO\_9**</span></span>](printer-info-9.md)
</dt> <dt>

[<span data-ttu-id="a5132-208">**опенпринтер**</span><span class="sxs-lookup"><span data-stu-id="a5132-208">**OpenPrinter**</span></span>](openprinter.md)
</dt> <dt>

[<span data-ttu-id="a5132-209">**сетпринтер**</span><span class="sxs-lookup"><span data-stu-id="a5132-209">**SetPrinter**</span></span>](setprinter.md)
</dt> </dl>

 

 




