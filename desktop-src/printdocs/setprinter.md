---
description: Функция Сетпринтер задает данные для указанного принтера или задает состояние указанного принтера путем приостановки печати, возобновления печати или очистки всех заданий печати.
ms.assetid: ade367c5-20d6-4da9-bb52-ce6768cf7537
title: Функция Сетпринтер (Винспул. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SetPrinter
- SetPrinterA
- SetPrinterW
api_type:
- DllExport
api_location:
- WinSpool.drv
- Ext-MS-Win-printer-WinSpool-l1-1-0.dll
- Ext-MS-Win-printer-WinSpool-l1-1-1.dll
- Ext-MS-Win-Printer-WinSpool-l1-1-2.dll
- Ext-MS-Win-Printer-WinSpool-L1-1-3.dll
ms.openlocfilehash: 5f2c58d97315ff108c8f12bd029849993a307025
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "105712387"
---
# <a name="setprinter-function"></a><span data-ttu-id="8838a-103">Функция Сетпринтер</span><span class="sxs-lookup"><span data-stu-id="8838a-103">SetPrinter function</span></span>

<span data-ttu-id="8838a-104">Функция **сетпринтер** задает данные для указанного принтера или задает состояние указанного принтера путем приостановки печати, возобновления печати или очистки всех заданий печати.</span><span class="sxs-lookup"><span data-stu-id="8838a-104">The **SetPrinter** function sets the data for a specified printer or sets the state of the specified printer by pausing printing, resuming printing, or clearing all print jobs.</span></span>

## <a name="syntax"></a><span data-ttu-id="8838a-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="8838a-105">Syntax</span></span>


```C++
BOOL SetPrinter(
  _In_ HANDLE hPrinter,
  _In_ DWORD  Level,
  _In_ LPBYTE pPrinter,
  _In_ DWORD  Command
);
```



## <a name="parameters"></a><span data-ttu-id="8838a-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="8838a-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="8838a-107">*хпринтер* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="8838a-107">*hPrinter* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="8838a-108">Маркер принтера.</span><span class="sxs-lookup"><span data-stu-id="8838a-108">A handle to the printer.</span></span> <span data-ttu-id="8838a-109">Используйте функцию [**опенпринтер**](openprinter.md), [**OpenPrinter2**](openprinter2.md)или [**аддпринтер**](addprinter.md) для получения маркера принтера.</span><span class="sxs-lookup"><span data-stu-id="8838a-109">Use the [**OpenPrinter**](openprinter.md), [**OpenPrinter2**](openprinter2.md), or [**AddPrinter**](addprinter.md) function to retrieve a printer handle.</span></span>

</dd> <dt>

<span data-ttu-id="8838a-110">*Уровень* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="8838a-110">*Level* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="8838a-111">Тип данных, которые функция хранит в буфере, на который указывает *ппринтер*.</span><span class="sxs-lookup"><span data-stu-id="8838a-111">The type of data that the function stores into the buffer pointed to by *pPrinter*.</span></span> <span data-ttu-id="8838a-112">Если параметр *команды* не равен нулю, параметр *уровня* должен равняться нулю.</span><span class="sxs-lookup"><span data-stu-id="8838a-112">If the *Command* parameter is not equal to zero, the *Level* parameter must be zero.</span></span>

<span data-ttu-id="8838a-113">Это значение может быть равно 0, 2, 3, 4, 5, 6, 7, 8 или 9.</span><span class="sxs-lookup"><span data-stu-id="8838a-113">This value can be 0, 2, 3, 4, 5, 6, 7, 8, or 9.</span></span>

</dd> <dt>

<span data-ttu-id="8838a-114">*ппринтер* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="8838a-114">*pPrinter* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="8838a-115">Указатель на буфер, содержащий данные, задаваемые для принтера, или содержит сведения о команде, указанной параметром *команды* .</span><span class="sxs-lookup"><span data-stu-id="8838a-115">A pointer to a buffer containing data to set for the printer, or containing information for the command specified by the *Command* parameter.</span></span> <span data-ttu-id="8838a-116">Тип данных в буфере определяется значением *Level*.</span><span class="sxs-lookup"><span data-stu-id="8838a-116">The type of data in the buffer is determined by the value of *Level*.</span></span>



| <span data-ttu-id="8838a-117">Level</span><span class="sxs-lookup"><span data-stu-id="8838a-117">Level</span></span>                                                                                                | <span data-ttu-id="8838a-118">Структура</span><span class="sxs-lookup"><span data-stu-id="8838a-118">Structure</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                |
|------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="0"></span><dl> <span data-ttu-id="8838a-119"><dt>**0**</dt></span><span class="sxs-lookup"><span data-stu-id="8838a-119"><dt>**0**</dt></span></span> </dl> | <span data-ttu-id="8838a-120">Если параметр *Command* имеет значение **\_ \_ \_ Status элемента управления принтера**, *ппринтер* должен содержать значение **DWORD** , указывающее новое состояние принтера для установки.</span><span class="sxs-lookup"><span data-stu-id="8838a-120">If the *Command* parameter is **PRINTER\_CONTROL\_SET\_STATUS**, *pPrinter* must contain a **DWORD** value that specifies the new printer status to set.</span></span> <span data-ttu-id="8838a-121">Список возможных значений состояния см. в описании элемента **Status** в структуре [**Printer \_ info \_ 2**](printer-info-2.md) .</span><span class="sxs-lookup"><span data-stu-id="8838a-121">For a list of the possible status values, see the **Status** member of the [**PRINTER\_INFO\_2**](printer-info-2.md) structure.</span></span> <span data-ttu-id="8838a-122">Обратите внимание, что **\_ состояние принтера \_ приостановлено** , а **\_ состояние принтера \_ ожидает \_ удаления** — недопустимые значения состояния для задания.</span><span class="sxs-lookup"><span data-stu-id="8838a-122">Note that **PRINTER\_STATUS\_PAUSED** and **PRINTER\_STATUS\_PENDING\_DELETION** are not valid status values to set.</span></span><br/> <span data-ttu-id="8838a-123">Если *Level* имеет значение 0, но *параметр команды* не имеет **\_ \_ \_ состояние управления принтерами**, *ппринтер* должен иметь **значение NULL**.</span><span class="sxs-lookup"><span data-stu-id="8838a-123">If *Level* is 0, but the *Command* parameter is not **PRINTER\_CONTROL\_SET\_STATUS**, *pPrinter* must be **NULL**.</span></span><br/> |
| <span id="2"></span><dl> <span data-ttu-id="8838a-124"><dt>**2**</dt></span><span class="sxs-lookup"><span data-stu-id="8838a-124"><dt>**2**</dt></span></span> </dl> | <span data-ttu-id="8838a-125">Структура [**сведений о принтере \_ \_ 2**](printer-info-2.md) , содержащая подробные сведения о принтере.</span><span class="sxs-lookup"><span data-stu-id="8838a-125">A [**PRINTER\_INFO\_2**](printer-info-2.md) structure containing detailed information about the printer.</span></span><br/>                                                                                                                                                                                                                                                                                                                                                                                                                                     |
| <span id="3"></span><dl> <span data-ttu-id="8838a-126"><dt>**3-5**</dt></span><span class="sxs-lookup"><span data-stu-id="8838a-126"><dt>**3**</dt></span></span> </dl> | <span data-ttu-id="8838a-127">Структура [**принтера \_ info \_ 3**](printer-info-3.md) , содержащая сведения о безопасности принтера.</span><span class="sxs-lookup"><span data-stu-id="8838a-127">A [**PRINTER\_INFO\_3**](printer-info-3.md) structure containing the printer's security information.</span></span><br/>                                                                                                                                                                                                                                                                                                                                                                                                                                         |
| <span id="4"></span><dl> <span data-ttu-id="8838a-128"><dt>**четырех**</dt></span><span class="sxs-lookup"><span data-stu-id="8838a-128"><dt>**4**</dt></span></span> </dl> | <span data-ttu-id="8838a-129">Структура [**принтера с информацией \_ \_ 4**](printer-info-4.md) , содержащая минимальные сведения о принтерах, включая имя принтера, имя сервера, а также то, является ли принтер удаленным или локальным.</span><span class="sxs-lookup"><span data-stu-id="8838a-129">A [**PRINTER\_INFO\_4**](printer-info-4.md) structure containing minimal printer information, including the name of the printer, the name of the server, and whether the printer is remote or local.</span></span><br/>                                                                                                                                                                                                                                                                                                                                         |
| <span id="5"></span><dl> <span data-ttu-id="8838a-130"><dt>**5.0**</dt></span><span class="sxs-lookup"><span data-stu-id="8838a-130"><dt>**5**</dt></span></span> </dl> | <span data-ttu-id="8838a-131">Структура сведений о принтере [**\_ \_ 5**](printer-info-5.md) , содержащая сведения о принтерах, такие как атрибуты принтера и параметры времени ожидания.</span><span class="sxs-lookup"><span data-stu-id="8838a-131">A [**PRINTER\_INFO\_5**](printer-info-5.md) structure containing printer information such as printer attributes and time-out settings.</span></span><br/>                                                                                                                                                                                                                                                                                                                                                                                                       |
| <span id="6"></span><dl> <span data-ttu-id="8838a-132"><dt>**6**</dt></span><span class="sxs-lookup"><span data-stu-id="8838a-132"><dt>**6**</dt></span></span> </dl> | <span data-ttu-id="8838a-133">Структура [**принтера с \_ информацией \_ 6**](printer-info-6.md) , указывающая значение состояния принтера.</span><span class="sxs-lookup"><span data-stu-id="8838a-133">A [**PRINTER\_INFO\_6**](printer-info-6.md) structure specifying the status value of a printer.</span></span><br/>                                                                                                                                                                                                                                                                                                                                                                                                                                              |
| <span id="7"></span><dl> <span data-ttu-id="8838a-134"><dt>**7**</dt></span><span class="sxs-lookup"><span data-stu-id="8838a-134"><dt>**7**</dt></span></span> </dl> | <span data-ttu-id="8838a-135">Структура [**принтера с \_ информацией \_ 7**](printer-info-7.md) .</span><span class="sxs-lookup"><span data-stu-id="8838a-135">A [**PRINTER\_INFO\_7**](printer-info-7.md) structure.</span></span> <span data-ttu-id="8838a-136">Член *двактион* этой структуры указывает, должна ли **сетпринтер** публиковать, отменять публикацию, повторно публиковать или обновлять данные принтера в службе каталогов.</span><span class="sxs-lookup"><span data-stu-id="8838a-136">The *dwAction* member of this structure indicates whether **SetPrinter** should publish, unpublish, re-publish, or update the printer's data in the directory service.</span></span><br/>                                                                                                                                                                                                                                                                                                                |
| <span id="8"></span><dl> <span data-ttu-id="8838a-137"><dt>**8**</dt></span><span class="sxs-lookup"><span data-stu-id="8838a-137"><dt>**8**</dt></span></span> </dl> | <span data-ttu-id="8838a-138">Структура [**принтера \_ info \_ 8**](printer-info-8.md) , указывающая глобальные параметры принтера по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="8838a-138">A [**PRINTER\_INFO\_8**](printer-info-8.md) structure specifying the global default printer settings.</span></span><br/>                                                                                                                                                                                                                                                                                                                                                                                                                                        |
| <span id="9"></span><dl> <span data-ttu-id="8838a-139"><dt>**9**</dt></span><span class="sxs-lookup"><span data-stu-id="8838a-139"><dt>**9**</dt></span></span> </dl> | <span data-ttu-id="8838a-140">Структура [**принтера с \_ информацией \_ 9**](printer-info-9.md) , указывающая параметры принтера по умолчанию для каждого пользователя.</span><span class="sxs-lookup"><span data-stu-id="8838a-140">A [**PRINTER\_INFO\_9**](printer-info-9.md) structure specifying the per-user default printer settings.</span></span><br/>                                                                                                                                                                                                                                                                                                                                                                                                                                      |



 

</dd> <dt>

<span data-ttu-id="8838a-141">*Команда* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="8838a-141">*Command* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="8838a-142">действие для выполнения.</span><span class="sxs-lookup"><span data-stu-id="8838a-142">The action to perform.</span></span>

<span data-ttu-id="8838a-143">Если параметр *Level* имеет ненулевое значение, присвойте этому параметру нулевые значения.</span><span class="sxs-lookup"><span data-stu-id="8838a-143">If the *Level* parameter is nonzero, set the value of this parameter to zero.</span></span> <span data-ttu-id="8838a-144">В этом случае принтер оставляет свое текущее состояние, а функция перенастраивает данные принтера в соответствии с параметрами *Level* и *ппринтер* .</span><span class="sxs-lookup"><span data-stu-id="8838a-144">In this case, the printer retains its current state and the function reconfigures the printer data as specified by the *Level* and *pPrinter* parameters.</span></span>

<span data-ttu-id="8838a-145">Если значение параметра *Level* равно нулю, присвойте этому параметру одно из следующих значений.</span><span class="sxs-lookup"><span data-stu-id="8838a-145">If the *Level* parameter is zero, set the value of this parameter to one of the following values.</span></span>



| <span data-ttu-id="8838a-146">Значение</span><span class="sxs-lookup"><span data-stu-id="8838a-146">Value</span></span>                                                                                                                                                                                                  | <span data-ttu-id="8838a-147">Значение</span><span class="sxs-lookup"><span data-stu-id="8838a-147">Meaning</span></span>                                                                                                                                             |
|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="PRINTER_CONTROL_PAUSE"></span><span id="printer_control_pause"></span><dl> <span data-ttu-id="8838a-148"><dt>**приостановка управления ПРИНТЕРом \_ \_**</dt></span><span class="sxs-lookup"><span data-stu-id="8838a-148"><dt>**PRINTER\_CONTROL\_PAUSE**</dt></span></span> </dl>                 | <span data-ttu-id="8838a-149">Приостановка принтера.</span><span class="sxs-lookup"><span data-stu-id="8838a-149">Pause the printer.</span></span><br/>                                                                                                                       |
| <span id="PRINTER_CONTROL_PURGE"></span><span id="printer_control_purge"></span><dl> <span data-ttu-id="8838a-150"><dt>**\_Очистка элемента управления принтера \_**</dt></span><span class="sxs-lookup"><span data-stu-id="8838a-150"><dt>**PRINTER\_CONTROL\_PURGE**</dt></span></span> </dl>                 | <span data-ttu-id="8838a-151">Удаление всех заданий печати на принтере.</span><span class="sxs-lookup"><span data-stu-id="8838a-151">Delete all print jobs in the printer.</span></span><br/>                                                                                                    |
| <span id="PRINTER_CONTROL_RESUME"></span><span id="printer_control_resume"></span><dl> <span data-ttu-id="8838a-152"><dt>**\_возобновление элемента управления принтера \_**</dt></span><span class="sxs-lookup"><span data-stu-id="8838a-152"><dt>**PRINTER\_CONTROL\_RESUME**</dt></span></span> </dl>              | <span data-ttu-id="8838a-153">Возобновление работы приостановленного принтера.</span><span class="sxs-lookup"><span data-stu-id="8838a-153">Resume a paused printer.</span></span><br/>                                                                                                                 |
| <span id="PRINTER_CONTROL_SET_STATUS"></span><span id="printer_control_set_status"></span><dl> <span data-ttu-id="8838a-154"><dt>**\_состояние набора элементов управления принтера \_ \_**</dt></span><span class="sxs-lookup"><span data-stu-id="8838a-154"><dt>**PRINTER\_CONTROL\_SET\_STATUS**</dt></span></span> </dl> | <span data-ttu-id="8838a-155">Задайте состояние принтера.</span><span class="sxs-lookup"><span data-stu-id="8838a-155">Set the printer status.</span></span><br/> <span data-ttu-id="8838a-156">Задайте для параметра *ппринтер* указатель на значение **типа DWORD** , указывающее новое состояние принтера.</span><span class="sxs-lookup"><span data-stu-id="8838a-156">Set the *pPrinter* parameter to a pointer to a **DWORD** value that specifies the new printer status.</span></span><br/> |



 

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="8838a-157">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="8838a-157">Return value</span></span>

<span data-ttu-id="8838a-158">Если функция выполнена, возвращаемое значение будет ненулевым.</span><span class="sxs-lookup"><span data-stu-id="8838a-158">If the function succeeds, the return value is a nonzero value.</span></span>

<span data-ttu-id="8838a-159">Если функция выполняется неудачно, возвращается нулевое значение.</span><span class="sxs-lookup"><span data-stu-id="8838a-159">If the function fails, the return value is zero.</span></span>

<span data-ttu-id="8838a-160">Если *уровень* равен 7, а действие публикации завершилось неудачей, **сетпринтер** возвращает **ошибку ввода-вывода об ошибке \_ \_** и пытается выполнить действие в фоновом режиме.</span><span class="sxs-lookup"><span data-stu-id="8838a-160">If *Level* is 7 and the publish action failed, **SetPrinter** returns **ERROR\_IO\_PENDING** and attempts to complete the action in the background.</span></span> <span data-ttu-id="8838a-161">Если *уровень* равен 7, а действие обновления завершилось с ошибкой, **Сетпринтер** возвращает **\_ файл ошибки \_ не \_ найден**.</span><span class="sxs-lookup"><span data-stu-id="8838a-161">If *Level* is 7 and the update action failed, **SetPrinter** returns **ERROR\_FILE\_NOT\_FOUND**.</span></span>

## <a name="remarks"></a><span data-ttu-id="8838a-162">Комментарии</span><span class="sxs-lookup"><span data-stu-id="8838a-162">Remarks</span></span>

> [!Note]  
> <span data-ttu-id="8838a-163">Это блокирующая или синхронная функция, которая может не возвращать значение немедленно.</span><span class="sxs-lookup"><span data-stu-id="8838a-163">This is a blocking or synchronous function and might not return immediately.</span></span> <span data-ttu-id="8838a-164">Скорость возврата этой функцией зависит от факторов времени выполнения, таких как состояние сети, Конфигурация сервера печати и факторы реализации драйвера принтера, которые трудно предсказать при написании приложения.</span><span class="sxs-lookup"><span data-stu-id="8838a-164">How quickly this function returns depends on run-time factors such as network status, print server configuration, and printer driver implementation factors that are difficult to predict when writing an application.</span></span> <span data-ttu-id="8838a-165">Вызов этой функции из потока, который управляет взаимодействием с пользовательским интерфейсом, может привести к невозможности реагирования приложения.</span><span class="sxs-lookup"><span data-stu-id="8838a-165">Calling this function from a thread that manages interaction with the user interface could make the application appear to be unresponsive.</span></span>

 

<span data-ttu-id="8838a-166">Нельзя использовать **сетпринтер** для изменения принтера по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="8838a-166">You cannot use **SetPrinter** to change the default printer.</span></span>

<span data-ttu-id="8838a-167">Чтобы изменить текущие параметры принтера, вызовите функцию [**PrintOut**](getprinter.md) , чтобы получить текущие параметры в структуре [**принтера с \_ информацией \_ 2**](printer-info-2.md) , при необходимости измените элементы этой структуры, а затем вызовите **сетпринтер**.</span><span class="sxs-lookup"><span data-stu-id="8838a-167">To modify the current printer settings, call the [**GetPrinter**](getprinter.md) function to retrieve the current settings into a [**PRINTER\_INFO\_2**](printer-info-2.md) structure, modify the members of that structure as necessary, and then call **SetPrinter**.</span></span>

<span data-ttu-id="8838a-168">Функция **сетпринтер** игнорирует элементы **псервернаме**, **аверажеппм**, **Status** и **кжобс** структуры « [**\_ сведения о принтере \_ 2**](printer-info-2.md) ».</span><span class="sxs-lookup"><span data-stu-id="8838a-168">The **SetPrinter** function ignores the **pServerName**, **AveragePPM**, **Status**, and **cJobs** members of a [**PRINTER\_INFO\_2**](printer-info-2.md) structure.</span></span>

<span data-ttu-id="8838a-169">Приостановка принтера приостанавливает планирование всех заданий печати для этого принтера, за исключением одного задания печати, которое может быть напечатано в данный момент.</span><span class="sxs-lookup"><span data-stu-id="8838a-169">Pausing a printer suspends scheduling of all print jobs for that printer, except for the one print job that may be currently printing.</span></span> <span data-ttu-id="8838a-170">Задания печати могут быть отправлены на приостановленный принтер, но никакие задания не будут запланированы для печати на этом принтере до тех пор, пока печать не будет возобновлена.</span><span class="sxs-lookup"><span data-stu-id="8838a-170">Print jobs can be submitted to a paused printer, but no jobs will be scheduled to print on that printer until printing is resumed.</span></span> <span data-ttu-id="8838a-171">Если принтер сброшен, все задания печати для этого принтера удаляются, за исключением текущего задания печати.</span><span class="sxs-lookup"><span data-stu-id="8838a-171">If a printer is cleared, all print jobs for that printer are deleted, except for the current print job.</span></span>

<span data-ttu-id="8838a-172">При использовании **сетпринтер** для изменения структуры [**DEVMODE**](/windows/win32/api/wingdi/ns-wingdi-devmodea) по умолчанию для принтера (глобально настроив значения по умолчанию для принтера) необходимо сначала вызвать функцию [**DocumentProperties**](documentproperties.md) для проверки структуры **DEVMODE** .</span><span class="sxs-lookup"><span data-stu-id="8838a-172">If you use **SetPrinter** to modify the default [**DEVMODE**](/windows/win32/api/wingdi/ns-wingdi-devmodea) structure for a printer (globally setting the printer defaults), you must first call the [**DocumentProperties**](documentproperties.md) function to validate the **DEVMODE** structure.</span></span>

<span data-ttu-id="8838a-173">Для структур [**" \_ сведения \_ о принтере 2**](printer-info-2.md) " и " [**\_ сведения о принтере \_ 3**](printer-info-3.md) ", которые содержат указатель на дескриптор безопасности, функция может задавать только те компоненты дескриптора безопасности, которые у вызывающего объекта есть разрешение на изменение.</span><span class="sxs-lookup"><span data-stu-id="8838a-173">For the [**PRINTER\_INFO\_2**](printer-info-2.md) and [**PRINTER\_INFO\_3**](printer-info-3.md) structures that contain a pointer to a security descriptor, the function can set only those components of the security descriptor that the caller has permission to modify.</span></span> <span data-ttu-id="8838a-174">Чтобы задать определенные компоненты дескриптора безопасности, необходимо указать необходимые права доступа при вызове функции [**опенпринтер**](openprinter.md) или [**OpenPrinter2**](openprinter2.md) для получения дескриптора принтера.</span><span class="sxs-lookup"><span data-stu-id="8838a-174">To set particular security descriptor components, you must specify the necessary access rights when you call the [**OpenPrinter**](openprinter.md) or [**OpenPrinter2**](openprinter2.md) function to retrieve a handle to the printer.</span></span> <span data-ttu-id="8838a-175">В следующей таблице показаны права доступа, необходимые для изменения различных компонентов дескриптора безопасности.</span><span class="sxs-lookup"><span data-stu-id="8838a-175">The following table shows the access rights required to modify the various security descriptor components.</span></span>



| <span data-ttu-id="8838a-176">Разрешение на доступ</span><span class="sxs-lookup"><span data-stu-id="8838a-176">Access permission</span></span>            | <span data-ttu-id="8838a-177">Компонент дескриптора безопасности</span><span class="sxs-lookup"><span data-stu-id="8838a-177">Security descriptor component</span></span>             |
|------------------------------|-------------------------------------------|
| <span data-ttu-id="8838a-178">**\_владелец записи**</span><span class="sxs-lookup"><span data-stu-id="8838a-178">**WRITE\_OWNER**</span></span>             | <span data-ttu-id="8838a-179">Владелец</span><span class="sxs-lookup"><span data-stu-id="8838a-179">Owner</span></span><br/> <span data-ttu-id="8838a-180">Основная группа</span><span class="sxs-lookup"><span data-stu-id="8838a-180">Primary group</span></span><br/> |
| <span data-ttu-id="8838a-181">**ЗАПИСЬ \_ DAC**</span><span class="sxs-lookup"><span data-stu-id="8838a-181">**WRITE\_DAC**</span></span>               | <span data-ttu-id="8838a-182">Список управления доступом на уровне пользователей (DACL)</span><span class="sxs-lookup"><span data-stu-id="8838a-182">Discretionary access-control list (DACL)</span></span>  |
| <span data-ttu-id="8838a-183">**ДОСТУП \_ к \_ безопасности системы**</span><span class="sxs-lookup"><span data-stu-id="8838a-183">**ACCESS\_SYSTEM\_SECURITY**</span></span> | <span data-ttu-id="8838a-184">Системный доступ — список управления (SACL)</span><span class="sxs-lookup"><span data-stu-id="8838a-184">System access-control list (SACL)</span></span>         |



 

<span data-ttu-id="8838a-185">Если дескриптор безопасности содержит компонент, для которого вызывающий объект не имеет права доступа для изменения, **сетпринтер** завершается с ошибкой.</span><span class="sxs-lookup"><span data-stu-id="8838a-185">If the security descriptor contains a component that the caller does not have the access right to modify, **SetPrinter** fails.</span></span> <span data-ttu-id="8838a-186">Эти компоненты дескриптора безопасности, которые не нужно изменять, должны иметь **значение NULL** или отсутствовать, если это уместно.</span><span class="sxs-lookup"><span data-stu-id="8838a-186">Those components of a security descriptor that you don't want to modify should be **NULL** or not be present, as appropriate.</span></span> <span data-ttu-id="8838a-187">Если вы не хотите изменять дескриптор безопасности и вызываете **сетпринтер** со структурой [**сведений о принтере \_ \_ 2**](printer-info-2.md) , установите для элемента **псекуритидескриптор** этой структуры **значение NULL**.</span><span class="sxs-lookup"><span data-stu-id="8838a-187">If you do not want to modify the security descriptor, and are calling **SetPrinter** with a [**PRINTER\_INFO\_2**](printer-info-2.md) structure, set the **pSecurityDescriptor** member of that structure to **NULL**.</span></span>

<span data-ttu-id="8838a-188">Брандмауэр подключения к Интернету (ICF) блокирует порты принтера по умолчанию, но можно включить исключение для общего доступа к файлам и принтерам.</span><span class="sxs-lookup"><span data-stu-id="8838a-188">The Internet Connection Firewall (ICF) blocks printer ports by default, but an exception for File and Print Sharing can be enabled.</span></span> <span data-ttu-id="8838a-189">Если **сетпринтер** вызывается администратором машины, он включает исключение.</span><span class="sxs-lookup"><span data-stu-id="8838a-189">If **SetPrinter** is called by a machine admin, it enables the exception.</span></span> <span data-ttu-id="8838a-190">Если он вызывается не администратором, а исключение еще не включено, вызов завершается ошибкой.</span><span class="sxs-lookup"><span data-stu-id="8838a-190">If it is called by a non-admin and the exception has not already been enabled, the call fails.</span></span>

<span data-ttu-id="8838a-191">Чтобы опубликовать, отменить публикацию или обновить данные службы каталогов для принтера, можно использовать уровень 7 с структурой " [**\_ сведения о принтере \_ 7**](printer-info-7.md) ".</span><span class="sxs-lookup"><span data-stu-id="8838a-191">You can use level 7 with the [**PRINTER\_INFO\_7**](printer-info-7.md) structure to publish, unpublish, or update directory service data for the printer.</span></span> <span data-ttu-id="8838a-192">Данные службы каталогов для принтера включают все данные, хранящиеся в \_ \* ключах сплдс, путем вызова функции [**сетпринтердатаекс**](setprinterdataex.md) для принтера.</span><span class="sxs-lookup"><span data-stu-id="8838a-192">The directory service data for a printer includes all the data stored under the SPLDS\_\* keys by calls to the [**SetPrinterDataEx**](setprinterdataex.md) function for the printer.</span></span> <span data-ttu-id="8838a-193">Перед вызовом **сетпринтер** установите для элемента **псзобжектгуид** в **\_ сведениях \_ о принтере 7** **значение NULL** и задайте для элемента *двактион* одно из следующих значений.</span><span class="sxs-lookup"><span data-stu-id="8838a-193">Before calling **SetPrinter**, set the **pszObjectGUID** member of **PRINTER\_INFO\_7** to **NULL** and set the *dwAction* member to one of the following values.</span></span>



| <span data-ttu-id="8838a-194">Значение</span><span class="sxs-lookup"><span data-stu-id="8838a-194">Value</span></span>                             | <span data-ttu-id="8838a-195">Описание</span><span class="sxs-lookup"><span data-stu-id="8838a-195">Description</span></span>                                                                                                                                                                                                                                                                                                                                                                             |
|-----------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="8838a-196">**\_Публикация дспринт**</span><span class="sxs-lookup"><span data-stu-id="8838a-196">**DSPRINT\_PUBLISH**</span></span><br/>   | <span data-ttu-id="8838a-197">Публикует данные службы каталогов.</span><span class="sxs-lookup"><span data-stu-id="8838a-197">Publishes the directory service data.</span></span><br/>                                                                                                                                                                                                                                                                                                                                        |
| <span data-ttu-id="8838a-198">**ДСПРИНТ \_ Повторная публикация**</span><span class="sxs-lookup"><span data-stu-id="8838a-198">**DSPRINT\_REPUBLISH**</span></span><br/> | <span data-ttu-id="8838a-199">Данные службы каталогов для принтера не публикуются, а затем публикуются снова, обновляются все свойства на опубликованном принтере.</span><span class="sxs-lookup"><span data-stu-id="8838a-199">The directory service data for the printer is unpublished and then published again, refreshing all properties in the published printer.</span></span> <span data-ttu-id="8838a-200">Повторная публикация также изменяет идентификатор GUID опубликованного принтера.</span><span class="sxs-lookup"><span data-stu-id="8838a-200">Re-publishing also changes the GUID of the published printer.</span></span> <span data-ttu-id="8838a-201">Используйте это значение, если вы подозреваете, что опубликованные данные принтера повреждены.</span><span class="sxs-lookup"><span data-stu-id="8838a-201">Use this value if you suspect the printer's published data has been corrupted.</span></span><br/>                                                                                         |
| <span data-ttu-id="8838a-202">**ДСПРИНТ \_ отменить публикацию**</span><span class="sxs-lookup"><span data-stu-id="8838a-202">**DSPRINT\_UNPUBLISH**</span></span><br/> | <span data-ttu-id="8838a-203">Отменяет публикацию данных службы каталогов.</span><span class="sxs-lookup"><span data-stu-id="8838a-203">Unpublishes the directory service data.</span></span><br/>                                                                                                                                                                                                                                                                                                                                      |
| <span data-ttu-id="8838a-204">**\_Обновление дспринт**</span><span class="sxs-lookup"><span data-stu-id="8838a-204">**DSPRINT\_UPDATE**</span></span><br/>    | <span data-ttu-id="8838a-205">Обновляет данные службы каталогов.</span><span class="sxs-lookup"><span data-stu-id="8838a-205">Updates the directory service data.</span></span> <span data-ttu-id="8838a-206">Это то же самое, что и **дспринт \_ Publish**, за исключением того, что **сетпринтер** завершается сбоем, но **\_ файл ошибок \_ не \_ найден** , если принтер еще не опубликован.</span><span class="sxs-lookup"><span data-stu-id="8838a-206">This is the same as **DSPRINT\_PUBLISH**, except that **SetPrinter** fails with **ERROR\_FILE\_NOT\_FOUND** if the printer is not already published.</span></span><br/> <span data-ttu-id="8838a-207">Используйте **\_ Обновление дспринт** для обновления опубликованных свойств, но не для принудительной публикации.</span><span class="sxs-lookup"><span data-stu-id="8838a-207">Use **DSPRINT\_UPDATE** to update published properties but not force publishing.</span></span> <span data-ttu-id="8838a-208">Драйверы принтеров всегда должны **использовать \_ Обновление дспринт** , а не **дспринт \_ Publish**.</span><span class="sxs-lookup"><span data-stu-id="8838a-208">Printer drivers should always use **DSPRINT\_UPDATE** rather than **DSPRINT\_PUBLISH**.</span></span><br/> |



 

<span data-ttu-id="8838a-209">**Дспринт \_ PENDING** не является допустимым значением *Двактион* для **сетпринтер**.</span><span class="sxs-lookup"><span data-stu-id="8838a-209">**DSPRINT\_PENDING** is not a valid *dwAction* value for **SetPrinter**.</span></span>

## <a name="requirements"></a><span data-ttu-id="8838a-210">Требования</span><span class="sxs-lookup"><span data-stu-id="8838a-210">Requirements</span></span>



| <span data-ttu-id="8838a-211">Требование</span><span class="sxs-lookup"><span data-stu-id="8838a-211">Requirement</span></span> | <span data-ttu-id="8838a-212">Значение</span><span class="sxs-lookup"><span data-stu-id="8838a-212">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="8838a-213">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="8838a-213">Minimum supported client</span></span><br/> | <span data-ttu-id="8838a-214">Windows 2000 Professional \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="8838a-214">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                                |
| <span data-ttu-id="8838a-215">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="8838a-215">Minimum supported server</span></span><br/> | <span data-ttu-id="8838a-216">Windows 2000 Server \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="8838a-216">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                      |
| <span data-ttu-id="8838a-217">Заголовок</span><span class="sxs-lookup"><span data-stu-id="8838a-217">Header</span></span><br/>                   | <dl> <span data-ttu-id="8838a-218"><dt>Винспул. h (включение Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="8838a-218"><dt>WinSpool.h (include Windows.h)</dt></span></span> </dl> |
| <span data-ttu-id="8838a-219">Библиотека</span><span class="sxs-lookup"><span data-stu-id="8838a-219">Library</span></span><br/>                  | <dl> <span data-ttu-id="8838a-220"><dt>Винспул. lib</dt></span><span class="sxs-lookup"><span data-stu-id="8838a-220"><dt>WinSpool.lib</dt></span></span> </dl>                   |
| <span data-ttu-id="8838a-221">DLL</span><span class="sxs-lookup"><span data-stu-id="8838a-221">DLL</span></span><br/>                      | <dl> <span data-ttu-id="8838a-222"><dt>Винспул. drv</dt></span><span class="sxs-lookup"><span data-stu-id="8838a-222"><dt>WinSpool.drv</dt></span></span> </dl>                   |
| <span data-ttu-id="8838a-223">Имя в кодировке Юникод и ANSI</span><span class="sxs-lookup"><span data-stu-id="8838a-223">Unicode and ANSI names</span></span><br/>   | <span data-ttu-id="8838a-224">**Сетпринтерв** (Юникод) и **сетпринтера** (ANSI)</span><span class="sxs-lookup"><span data-stu-id="8838a-224">**SetPrinterW** (Unicode) and **SetPrinterA** (ANSI)</span></span><br/>                                           |



## <a name="see-also"></a><span data-ttu-id="8838a-225">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="8838a-225">See also</span></span>

<dl> <dt>

[<span data-ttu-id="8838a-226">Вывод на печать</span><span class="sxs-lookup"><span data-stu-id="8838a-226">Printing</span></span>](printdocs-printing.md)
</dt> <dt>

[<span data-ttu-id="8838a-227">Функции API очереди печати принтера</span><span class="sxs-lookup"><span data-stu-id="8838a-227">Print Spooler API Functions</span></span>](printing-and-print-spooler-functions.md)
</dt> <dt>

[<span data-ttu-id="8838a-228">**аддпринтер**</span><span class="sxs-lookup"><span data-stu-id="8838a-228">**AddPrinter**</span></span>](addprinter.md)
</dt> <dt>

[<span data-ttu-id="8838a-229">**Наложение**</span><span class="sxs-lookup"><span data-stu-id="8838a-229">**GetPrinter**</span></span>](getprinter.md)
</dt> <dt>

[<span data-ttu-id="8838a-230">**опенпринтер**</span><span class="sxs-lookup"><span data-stu-id="8838a-230">**OpenPrinter**</span></span>](openprinter.md)
</dt> <dt>

[<span data-ttu-id="8838a-231">**OpenPrinter2**</span><span class="sxs-lookup"><span data-stu-id="8838a-231">**OpenPrinter2**</span></span>](openprinter2.md)
</dt> <dt>

[<span data-ttu-id="8838a-232">**\_Сведения о принтере \_ 2**</span><span class="sxs-lookup"><span data-stu-id="8838a-232">**PRINTER\_INFO\_2**</span></span>](printer-info-2.md)
</dt> <dt>

[<span data-ttu-id="8838a-233">**\_Сведения о принтере \_ 3**</span><span class="sxs-lookup"><span data-stu-id="8838a-233">**PRINTER\_INFO\_3**</span></span>](printer-info-3.md)
</dt> <dt>

[<span data-ttu-id="8838a-234">**\_Сведения о принтере \_ 4**</span><span class="sxs-lookup"><span data-stu-id="8838a-234">**PRINTER\_INFO\_4**</span></span>](printer-info-4.md)
</dt> <dt>

[<span data-ttu-id="8838a-235">**\_Сведения о принтере \_ 5**</span><span class="sxs-lookup"><span data-stu-id="8838a-235">**PRINTER\_INFO\_5**</span></span>](printer-info-5.md)
</dt> <dt>

[<span data-ttu-id="8838a-236">**\_Сведения о принтере \_ 6**</span><span class="sxs-lookup"><span data-stu-id="8838a-236">**PRINTER\_INFO\_6**</span></span>](printer-info-6.md)
</dt> <dt>

[<span data-ttu-id="8838a-237">**\_Сведения о принтере \_ 7**</span><span class="sxs-lookup"><span data-stu-id="8838a-237">**PRINTER\_INFO\_7**</span></span>](printer-info-7.md)
</dt> <dt>

[<span data-ttu-id="8838a-238">**\_Сведения о принтере \_ 8**</span><span class="sxs-lookup"><span data-stu-id="8838a-238">**PRINTER\_INFO\_8**</span></span>](printer-info-8.md)
</dt> <dt>

[<span data-ttu-id="8838a-239">**\_Сведения о принтере \_ 9**</span><span class="sxs-lookup"><span data-stu-id="8838a-239">**PRINTER\_INFO\_9**</span></span>](printer-info-9.md)
</dt> <dt>

[<span data-ttu-id="8838a-240">**сетпринтердатаекс**</span><span class="sxs-lookup"><span data-stu-id="8838a-240">**SetPrinterDataEx**</span></span>](setprinterdataex.md)
</dt> </dl>

 

 




