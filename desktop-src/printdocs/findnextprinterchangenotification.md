---
description: Функция Финднекстпринтерчанженотификатион извлекает сведения о последнем уведомлении об изменении для объекта уведомления о изменении, связанного с принтером или сервером печати.
ms.assetid: ea7774ae-361f-41e4-bbc6-3f100028b22a
title: Функция Финднекстпринтерчанженотификатион (Винспул. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- FindNextPrinterChangeNotification
api_type:
- DllExport
api_location:
- Spoolss.dll
ms.openlocfilehash: ef3ece0d4831409d79e2152cf7b6a37d6bbdc8b3
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "103910799"
---
# <a name="findnextprinterchangenotification-function"></a><span data-ttu-id="76145-103">Функция Финднекстпринтерчанженотификатион</span><span class="sxs-lookup"><span data-stu-id="76145-103">FindNextPrinterChangeNotification function</span></span>

<span data-ttu-id="76145-104">Функция **финднекстпринтерчанженотификатион** извлекает сведения о последнем уведомлении об изменении для объекта уведомления о изменении, связанного с принтером или сервером печати.</span><span class="sxs-lookup"><span data-stu-id="76145-104">The **FindNextPrinterChangeNotification** function retrieves information about the most recent change notification for a change notification object associated with a printer or print server.</span></span> <span data-ttu-id="76145-105">Вызывайте эту функцию, если выполняется операция ожидания объекта уведомления об изменении.</span><span class="sxs-lookup"><span data-stu-id="76145-105">Call this function when a wait operation on the change notification object is satisfied.</span></span>

<span data-ttu-id="76145-106">Функция также сбрасывает объект уведомления об изменении на несигнальное состояние.</span><span class="sxs-lookup"><span data-stu-id="76145-106">The function also resets the change notification object to the not-signaled state.</span></span> <span data-ttu-id="76145-107">Затем можно использовать объект в другой операции ожидания, чтобы продолжить наблюдение за принтером или сервером печати.</span><span class="sxs-lookup"><span data-stu-id="76145-107">You can then use the object in another wait operation to continue monitoring the printer or print server.</span></span> <span data-ttu-id="76145-108">Операционная система задаст объекту сигнальное состояние при следующем выполнении одного из указанных изменений на принтере или на сервере печати.</span><span class="sxs-lookup"><span data-stu-id="76145-108">The operating system will set the object to the signaled state the next time one of a specified set of changes occurs to the printer or print server.</span></span> <span data-ttu-id="76145-109">Функция [**финдфирстпринтерчанженотификатион**](findfirstprinterchangenotification.md) создает объект уведомления об изменении и задает набор отслеживаемых изменений.</span><span class="sxs-lookup"><span data-stu-id="76145-109">The [**FindFirstPrinterChangeNotification**](findfirstprinterchangenotification.md) function creates the change notification object and specifies the set of changes to be monitored.</span></span>

## <a name="syntax"></a><span data-ttu-id="76145-110">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="76145-110">Syntax</span></span>


```C++
BOOL FindNextPrinterChangeNotification(
  _In_      HANDLE hChange,
  _Out_opt_ PDWORD pdwChange,
  _In_opt_  LPVOID pPrinterNotifyOptions,
  _Out_opt_ LPVOID *ppPrinterNotifyInfo
);
```



## <a name="parameters"></a><span data-ttu-id="76145-111">Параметры</span><span class="sxs-lookup"><span data-stu-id="76145-111">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="76145-112">*хчанже* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="76145-112">*hChange* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="76145-113">Маркер объекта уведомления об изменении, связанного с принтером или сервером печати.</span><span class="sxs-lookup"><span data-stu-id="76145-113">A handle to a change notification object associated with a printer or print server.</span></span> <span data-ttu-id="76145-114">Такой обработчик можно получить, вызвав функцию [**финдфирстпринтерчанженотификатион**](findfirstprinterchangenotification.md) .</span><span class="sxs-lookup"><span data-stu-id="76145-114">You obtain such a handle by calling the [**FindFirstPrinterChangeNotification**](findfirstprinterchangenotification.md) function.</span></span> <span data-ttu-id="76145-115">Операционная система устанавливает этот объект уведомления об изменении в сигнальное состояние при обнаружении одного из изменений, указанных в фильтре уведомлений об изменении объекта.</span><span class="sxs-lookup"><span data-stu-id="76145-115">The operating system sets this change notification object to the signaled state when it detects one of the changes specified in the object's change notification filter.</span></span>

</dd> <dt>

<span data-ttu-id="76145-116">*пдвчанже* \[ out, необязательно\]</span><span class="sxs-lookup"><span data-stu-id="76145-116">*pdwChange* \[out, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="76145-117">Указатель на переменную, биты которой заданы, чтобы указать, какие изменения вызвали самое последнее уведомление.</span><span class="sxs-lookup"><span data-stu-id="76145-117">A pointer to a variable whose bits are set to indicate the changes that occurred to cause the most recent notification.</span></span> <span data-ttu-id="76145-118">Битовые флаги, которые могут быть заданы, соответствуют указанным в параметре *фдвфилтер* вызова [**финдфирстпринтерчанженотификатион**](findfirstprinterchangenotification.md) .</span><span class="sxs-lookup"><span data-stu-id="76145-118">The bit flags that might be set correspond to those specified in the *fdwFilter* parameter of the [**FindFirstPrinterChangeNotification**](findfirstprinterchangenotification.md) call.</span></span> <span data-ttu-id="76145-119">Система устанавливает один или несколько следующих битовых флагов.</span><span class="sxs-lookup"><span data-stu-id="76145-119">The system sets one or more of the following bit flags.</span></span>



| <span data-ttu-id="76145-120">Значение</span><span class="sxs-lookup"><span data-stu-id="76145-120">Value</span></span>                                                                                                                                                                                                                                             | <span data-ttu-id="76145-121">Значение</span><span class="sxs-lookup"><span data-stu-id="76145-121">Meaning</span></span>                                                   |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------|
| <span id="PRINTER_CHANGE_ADD_FORM"></span><span id="printer_change_add_form"></span><dl> <span data-ttu-id="76145-122"><dt>**\_ \_ Добавление формы изменения \_ принтера**</dt></span><span class="sxs-lookup"><span data-stu-id="76145-122"><dt>**PRINTER\_CHANGE\_ADD\_FORM**</dt></span></span> </dl>                                                     | <span data-ttu-id="76145-123">На сервер была добавлена форма.</span><span class="sxs-lookup"><span data-stu-id="76145-123">A form was added to the server.</span></span><br/>                |
| <span id="PRINTER_CHANGE_ADD_JOB"></span><span id="printer_change_add_job"></span><dl> <span data-ttu-id="76145-124"><dt>**\_ \_ Добавление задания изменения \_ принтера**</dt></span><span class="sxs-lookup"><span data-stu-id="76145-124"><dt>**PRINTER\_CHANGE\_ADD\_JOB**</dt></span></span> </dl>                                                        | <span data-ttu-id="76145-125">Задание печати было отправлено на принтер.</span><span class="sxs-lookup"><span data-stu-id="76145-125">A print job was sent to the printer.</span></span><br/>           |
| <span id="PRINTER_CHANGE_ADD_PORT"></span><span id="printer_change_add_port"></span><dl> <span data-ttu-id="76145-126"><dt>**\_ \_ Добавление порта для изменения принтера \_**</dt></span><span class="sxs-lookup"><span data-stu-id="76145-126"><dt>**PRINTER\_CHANGE\_ADD\_PORT**</dt></span></span> </dl>                                                     | <span data-ttu-id="76145-127">На сервер был добавлен порт или монитор.</span><span class="sxs-lookup"><span data-stu-id="76145-127">A port or monitor was added to the server.</span></span><br/>     |
| <span id="PRINTER_CHANGE_ADD_PRINT_PROCESSOR"></span><span id="printer_change_add_print_processor"></span><dl> <span data-ttu-id="76145-128"><dt>**\_Изменение принтера \_ Добавление \_ \_ обработчика печати**</dt></span><span class="sxs-lookup"><span data-stu-id="76145-128"><dt>**PRINTER\_CHANGE\_ADD\_PRINT\_PROCESSOR**</dt></span></span> </dl>                   | <span data-ttu-id="76145-129">Обработчик заданий печати был добавлен на сервер.</span><span class="sxs-lookup"><span data-stu-id="76145-129">A print processor was added to the server.</span></span><br/>     |
| <span id="PRINTER_CHANGE_ADD_PRINTER"></span><span id="printer_change_add_printer"></span><dl> <span data-ttu-id="76145-130"><dt>**\_Изменение принтера \_ Добавление \_ принтера**</dt></span><span class="sxs-lookup"><span data-stu-id="76145-130"><dt>**PRINTER\_CHANGE\_ADD\_PRINTER**</dt></span></span> </dl>                                            | <span data-ttu-id="76145-131">На сервер был добавлен принтер.</span><span class="sxs-lookup"><span data-stu-id="76145-131">A printer was added to the server.</span></span><br/>             |
| <span id="PRINTER_CHANGE_ADD_PRINTER_DRIVER"></span><span id="printer_change_add_printer_driver"></span><dl> <span data-ttu-id="76145-132"><dt>**\_Изменение принтера \_ Добавление \_ \_ драйвера принтера**</dt></span><span class="sxs-lookup"><span data-stu-id="76145-132"><dt>**PRINTER\_CHANGE\_ADD\_PRINTER\_DRIVER**</dt></span></span> </dl>                      | <span data-ttu-id="76145-133">На сервер был добавлен драйвер принтера.</span><span class="sxs-lookup"><span data-stu-id="76145-133">A printer driver was added to the server.</span></span><br/>      |
| <span id="PRINTER_CHANGE_CONFIGURE_PORT"></span><span id="printer_change_configure_port"></span><dl> <span data-ttu-id="76145-134"><dt>**\_Изменение принтера \_ Настройка \_ порта**</dt></span><span class="sxs-lookup"><span data-stu-id="76145-134"><dt>**PRINTER\_CHANGE\_CONFIGURE\_PORT**</dt></span></span> </dl>                                   | <span data-ttu-id="76145-135">Порт был настроен на сервере.</span><span class="sxs-lookup"><span data-stu-id="76145-135">A port was configured on the server.</span></span><br/>           |
| <span id="PRINTER_CHANGE_DELETE_FORM"></span><span id="printer_change_delete_form"></span><dl> <span data-ttu-id="76145-136"><dt>**\_ \_ форма удаления изменения \_ принтера**</dt></span><span class="sxs-lookup"><span data-stu-id="76145-136"><dt>**PRINTER\_CHANGE\_DELETE\_FORM**</dt></span></span> </dl>                                            | <span data-ttu-id="76145-137">Форма была удалена с сервера.</span><span class="sxs-lookup"><span data-stu-id="76145-137">A form was deleted from the server.</span></span><br/>            |
| <span id="PRINTER_CHANGE_DELETE_JOB"></span><span id="printer_change_delete_job"></span><dl> <span data-ttu-id="76145-138"><dt>**\_ \_ Задание удаления изменений \_ принтера**</dt></span><span class="sxs-lookup"><span data-stu-id="76145-138"><dt>**PRINTER\_CHANGE\_DELETE\_JOB**</dt></span></span> </dl>                                               | <span data-ttu-id="76145-139">Задание удалено.</span><span class="sxs-lookup"><span data-stu-id="76145-139">A job was deleted.</span></span><br/>                             |
| <span id="PRINTER_CHANGE_DELETE_PORT"></span><span id="printer_change_delete_port"></span><dl> <span data-ttu-id="76145-140"><dt>**\_ \_ порт удаления для изменения принтера \_**</dt></span><span class="sxs-lookup"><span data-stu-id="76145-140"><dt>**PRINTER\_CHANGE\_DELETE\_PORT**</dt></span></span> </dl>                                            | <span data-ttu-id="76145-141">Порт или монитор был удален с сервера.</span><span class="sxs-lookup"><span data-stu-id="76145-141">A port or monitor was deleted from the server.</span></span><br/> |
| <span id="PRINTER_CHANGE_DELETE_PRINT_PROCESSOR"></span><span id="printer_change_delete_print_processor"></span><dl> <span data-ttu-id="76145-142"><dt>**\_ \_ \_ обработчик печати изменения принтера \_**</dt></span><span class="sxs-lookup"><span data-stu-id="76145-142"><dt>**PRINTER\_CHANGE\_DELETE\_PRINT\_PROCESSOR**</dt></span></span> </dl>          | <span data-ttu-id="76145-143">Обработчик заданий печати был удален с сервера.</span><span class="sxs-lookup"><span data-stu-id="76145-143">A print processor was deleted from the server.</span></span><br/> |
| <span id="PRINTER_CHANGE_DELETE_PRINTER"></span><span id="printer_change_delete_printer"></span><dl> <span data-ttu-id="76145-144"><dt>**\_Изменение принтера \_ Удаление \_ принтера**</dt></span><span class="sxs-lookup"><span data-stu-id="76145-144"><dt>**PRINTER\_CHANGE\_DELETE\_PRINTER**</dt></span></span> </dl>                                   | <span data-ttu-id="76145-145">Принтер удален.</span><span class="sxs-lookup"><span data-stu-id="76145-145">A printer was deleted.</span></span><br/>                         |
| <span id="PRINTER_CHANGE_DELETE_PRINTER_DRIVER"></span><span id="printer_change_delete_printer_driver"></span><dl> <span data-ttu-id="76145-146"><dt>**\_Изменение принтера \_ Удаление \_ \_ драйвера принтера**</dt></span><span class="sxs-lookup"><span data-stu-id="76145-146"><dt>**PRINTER\_CHANGE\_DELETE\_PRINTER\_DRIVER**</dt></span></span> </dl>             | <span data-ttu-id="76145-147">С сервера удален драйвер принтера.</span><span class="sxs-lookup"><span data-stu-id="76145-147">A printer driver was deleted from the server.</span></span><br/>  |
| <span id="PRINTER_CHANGE_FAILED_CONNECTION_PRINTER"></span><span id="printer_change_failed_connection_printer"></span><dl> <span data-ttu-id="76145-148"><dt>**принтер \_ \_ не смог изменить \_ подключение \_**</dt></span><span class="sxs-lookup"><span data-stu-id="76145-148"><dt>**PRINTER\_CHANGE\_FAILED\_CONNECTION\_PRINTER**</dt></span></span> </dl> | <span data-ttu-id="76145-149">Сбой подключения принтера.</span><span class="sxs-lookup"><span data-stu-id="76145-149">A printer connection has failed.</span></span><br/>               |
| <span id="PRINTER_CHANGE_SET_FORM"></span><span id="printer_change_set_form"></span><dl> <span data-ttu-id="76145-150"><dt>**\_ \_ форма набора изменений \_ принтера**</dt></span><span class="sxs-lookup"><span data-stu-id="76145-150"><dt>**PRINTER\_CHANGE\_SET\_FORM**</dt></span></span> </dl>                                                     | <span data-ttu-id="76145-151">Форма была установлена на сервере.</span><span class="sxs-lookup"><span data-stu-id="76145-151">A form was set on the server.</span></span><br/>                  |
| <span id="PRINTER_CHANGE_SET_JOB"></span><span id="printer_change_set_job"></span><dl> <span data-ttu-id="76145-152"><dt>**\_Задание по изменению \_ набора принтеров \_**</dt></span><span class="sxs-lookup"><span data-stu-id="76145-152"><dt>**PRINTER\_CHANGE\_SET\_JOB**</dt></span></span> </dl>                                                        | <span data-ttu-id="76145-153">Задание задано.</span><span class="sxs-lookup"><span data-stu-id="76145-153">A job was set.</span></span><br/>                                 |
| <span id="PRINTER_CHANGE_SET_PRINTER"></span><span id="printer_change_set_printer"></span><dl> <span data-ttu-id="76145-154"><dt>**\_Настройка принтера \_ изменить \_ принтер**</dt></span><span class="sxs-lookup"><span data-stu-id="76145-154"><dt>**PRINTER\_CHANGE\_SET\_PRINTER**</dt></span></span> </dl>                                            | <span data-ttu-id="76145-155">Установлен принтер.</span><span class="sxs-lookup"><span data-stu-id="76145-155">A printer was set.</span></span><br/>                             |
| <span id="PRINTER_CHANGE_SET_PRINTER_DRIVER"></span><span id="printer_change_set_printer_driver"></span><dl> <span data-ttu-id="76145-156"><dt>**изменение принтера " \_ \_ задать \_ \_ драйвер принтера"**</dt></span><span class="sxs-lookup"><span data-stu-id="76145-156"><dt>**PRINTER\_CHANGE\_SET\_PRINTER\_DRIVER**</dt></span></span> </dl>                      | <span data-ttu-id="76145-157">Установлен драйвер принтера.</span><span class="sxs-lookup"><span data-stu-id="76145-157">A printer driver was set.</span></span><br/>                      |
| <span id="PRINTER_CHANGE_WRITE_JOB"></span><span id="printer_change_write_job"></span><dl> <span data-ttu-id="76145-158"><dt>**\_ \_ Задание записи изменения \_ принтера**</dt></span><span class="sxs-lookup"><span data-stu-id="76145-158"><dt>**PRINTER\_CHANGE\_WRITE\_JOB**</dt></span></span> </dl>                                                  | <span data-ttu-id="76145-159">Данные задания были записаны.</span><span class="sxs-lookup"><span data-stu-id="76145-159">Job data was written.</span></span><br/>                          |
| <span id="PRINTER_CHANGE_TIMEOUT"></span><span id="printer_change_timeout"></span><dl> <span data-ttu-id="76145-160"><dt>**\_ \_ время ожидания изменения принтера**</dt></span><span class="sxs-lookup"><span data-stu-id="76145-160"><dt>**PRINTER\_CHANGE\_TIMEOUT**</dt></span></span> </dl>                                                         | <span data-ttu-id="76145-161">Время ожидания задания истекло.</span><span class="sxs-lookup"><span data-stu-id="76145-161">The job timed out.</span></span><br/>                             |
| <span id="PRINTER_CHANGE_SERVER"></span><span id="printer_change_server"></span><dl> <span data-ttu-id="76145-162"><dt>**\_сервер изменения \_ принтера**</dt></span><span class="sxs-lookup"><span data-stu-id="76145-162"><dt>**PRINTER\_CHANGE\_SERVER**</dt></span></span> </dl>                                                            | <span data-ttu-id="76145-163">Windows 7: произошло изменение на сервере.</span><span class="sxs-lookup"><span data-stu-id="76145-163">Windows 7: A change occurred on the server.</span></span><br/>    |



 

</dd> <dt>

<span data-ttu-id="76145-164">*ппринтернотифйоптионс* \[ в необязательное\]</span><span class="sxs-lookup"><span data-stu-id="76145-164">*pPrinterNotifyOptions* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="76145-165">Указатель на структуру [**\_ \_ параметров уведомления принтера**](printer-notify-options.md) .</span><span class="sxs-lookup"><span data-stu-id="76145-165">A pointer to a [**PRINTER\_NOTIFY\_OPTIONS**](printer-notify-options.md) structure.</span></span> <span data-ttu-id="76145-166">Установите для элемента **flags** этой структуры значение **принтер \_ \_ Параметры уведомления \_ Обновить**, чтобы функция возвращала текущие данные для всех отслеживаемых полей сведений о принтерах.</span><span class="sxs-lookup"><span data-stu-id="76145-166">Set the **Flags** member of this structure to **PRINTER\_NOTIFY\_OPTIONS\_REFRESH**, to cause the function to return the current data for all monitored printer information fields.</span></span> <span data-ttu-id="76145-167">Функция игнорирует все остальные члены структуры.</span><span class="sxs-lookup"><span data-stu-id="76145-167">The function ignores all other members of the structure.</span></span> <span data-ttu-id="76145-168">Этот параметр может принимать значение **NULL**.</span><span class="sxs-lookup"><span data-stu-id="76145-168">This parameter can be **NULL**.</span></span>

</dd> <dt>

<span data-ttu-id="76145-169">*пппринтернотифинфо* \[ out, необязательно\]</span><span class="sxs-lookup"><span data-stu-id="76145-169">*ppPrinterNotifyInfo* \[out, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="76145-170">Указатель на переменную указателя, которая получает указатель на выделенный системой буфер, доступный только для чтения.</span><span class="sxs-lookup"><span data-stu-id="76145-170">A pointer to a pointer variable that receives a pointer to a system-allocated, read-only buffer.</span></span> <span data-ttu-id="76145-171">Вызовите функцию [**фрипринтернотифинфо**](freeprinternotifyinfo.md) , чтобы освободить буфер по завершении работы с ним.</span><span class="sxs-lookup"><span data-stu-id="76145-171">Call the [**FreePrinterNotifyInfo**](freeprinternotifyinfo.md) function to free the buffer when you are finished with it.</span></span> <span data-ttu-id="76145-172">Если сведения не требуются, этот параметр может иметь **значение NULL** .</span><span class="sxs-lookup"><span data-stu-id="76145-172">This parameter can be **NULL** if no information is required.</span></span>

<span data-ttu-id="76145-173">Буфер содержит структуру [**\_ \_ сведений об уведомлении принтера**](printer-notify-info.md) , которая содержит массив информационных структур [**\_ \_ \_ данных принтера**](printer-notify-info-data.md) .</span><span class="sxs-lookup"><span data-stu-id="76145-173">The buffer contains a [**PRINTER\_NOTIFY\_INFO**](printer-notify-info.md) structure, which contains an array of [**PRINTER\_NOTIFY\_INFO\_DATA**](printer-notify-info-data.md) structures.</span></span> <span data-ttu-id="76145-174">Каждый элемент массива содержит сведения об одном из полей, указанных в параметре *ппринтернотифйоптионс* вызова [**финдфирстпринтерчанженотификатион**](findfirstprinterchangenotification.md) .</span><span class="sxs-lookup"><span data-stu-id="76145-174">Each element of the array contains information about one of the fields specified in the *pPrinterNotifyOptions* parameter of the [**FindFirstPrinterChangeNotification**](findfirstprinterchangenotification.md) call.</span></span> <span data-ttu-id="76145-175">Как правило, функция предоставляет данные только для тех полей, которые были изменены, чтобы вызвать самое последнее уведомление.</span><span class="sxs-lookup"><span data-stu-id="76145-175">Typically, the function provides data only for the fields that changed to cause the most recent notification.</span></span> <span data-ttu-id="76145-176">Однако если структура, на которую указывает параметр *ппринтернотифйоптионс* , указывает **\_ Параметры уведомления для \_ принтера \_ Обновить**, функция предоставляет данные для всех отслеживаемых полей.</span><span class="sxs-lookup"><span data-stu-id="76145-176">However, if the structure pointed to by the *pPrinterNotifyOptions* parameter specifies **PRINTER\_NOTIFY\_OPTIONS\_REFRESH**, the function provides data for all monitored fields.</span></span>

<span data-ttu-id="76145-177">Если бит **" \_ уведомление \_ \_ принтера** " установлен в элементе **flags** в структуре [**\_ \_ сведений о принтере**](printer-notify-info.md) , то произошло переполнение или ошибка, а уведомления могли быть потеряны.</span><span class="sxs-lookup"><span data-stu-id="76145-177">If the **PRINTER\_NOTIFY\_INFO\_DISCARDED** bit is set in the **Flags** member of the [**PRINTER\_NOTIFY\_INFO**](printer-notify-info.md) structure, an overflow or error occurred, and notifications may have been lost.</span></span> <span data-ttu-id="76145-178">В этом случае никакие дополнительные уведомления не будут отправляться, пока вы не выполните второй вызов **финднекстпринтерчанженотификатион** , указывающий **\_ Параметры уведомления принтера \_ \_ Обновить**.</span><span class="sxs-lookup"><span data-stu-id="76145-178">In this case, no additional notifications will be sent until you make a second **FindNextPrinterChangeNotification** call that specifies **PRINTER\_NOTIFY\_OPTIONS\_REFRESH**.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="76145-179">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="76145-179">Return value</span></span>

<span data-ttu-id="76145-180">Если функция выполнена, возвращаемое значение будет ненулевым.</span><span class="sxs-lookup"><span data-stu-id="76145-180">If the function succeeds, the return value is a nonzero value.</span></span>

<span data-ttu-id="76145-181">Если функция выполняется неудачно, возвращается нулевое значение.</span><span class="sxs-lookup"><span data-stu-id="76145-181">If the function fails, the return value is zero.</span></span>

## <a name="remarks"></a><span data-ttu-id="76145-182">Комментарии</span><span class="sxs-lookup"><span data-stu-id="76145-182">Remarks</span></span>

> [!Note]  
> <span data-ttu-id="76145-183">Это блокирующая или синхронная функция, которая может не возвращать значение немедленно.</span><span class="sxs-lookup"><span data-stu-id="76145-183">This is a blocking or synchronous function and might not return immediately.</span></span> <span data-ttu-id="76145-184">Скорость возврата этой функцией зависит от факторов времени выполнения, таких как состояние сети, Конфигурация сервера печати и факторы реализации драйвера принтера, которые трудно предсказать при написании приложения.</span><span class="sxs-lookup"><span data-stu-id="76145-184">How quickly this function returns depends on run-time factors such as network status, print server configuration, and printer driver implementation factors that are difficult to predict when writing an application.</span></span> <span data-ttu-id="76145-185">Вызов этой функции из потока, который управляет взаимодействием с пользовательским интерфейсом, может привести к невозможности реагирования приложения.</span><span class="sxs-lookup"><span data-stu-id="76145-185">Calling this function from a thread that manages interaction with the user interface could make the application appear to be unresponsive.</span></span>

 

<span data-ttu-id="76145-186">Вызов функции **финднекстпринтерчанженотификатион** после выполнения операции ожидания для объекта уведомления, созданного с помощью [**финдфирстпринтерчанженотификатион**](findfirstprinterchangenotification.md) , удовлетворен.</span><span class="sxs-lookup"><span data-stu-id="76145-186">Call the **FindNextPrinterChangeNotification** function after a wait operation on a notification object created by [**FindFirstPrinterChangeNotification**](findfirstprinterchangenotification.md) has been satisfied.</span></span> <span data-ttu-id="76145-187">Вызов **финднекстпринтерчанженотификатион** позволяет получить сведения об изменениях, удовлетворяющих операции ожидания, и сбрасывает объект уведомления, чтобы он мог получать сигналы при следующем изменении.</span><span class="sxs-lookup"><span data-stu-id="76145-187">Calling **FindNextPrinterChangeNotification** lets you obtain information about the change that satisfied the wait operation, and resets the notification object so it can be signaled when the next change occurs.</span></span>

<span data-ttu-id="76145-188">За одним исключением не следует вызывать функцию **финднекстпринтерчанженотификатион** , если объект уведомления об изменении не находится в сигнальном состоянии.</span><span class="sxs-lookup"><span data-stu-id="76145-188">With one exception, do not call the **FindNextPrinterChangeNotification** function if the change notification object is not in the signaled state.</span></span> <span data-ttu-id="76145-189">Если функция Wait возвращает значение **\_ времени ожидания ожидания**, объект изменения не находится в сигнальном состоянии.</span><span class="sxs-lookup"><span data-stu-id="76145-189">If a wait function returns the value **WAIT\_TIMEOUT**, the change object is not in the signaled state.</span></span> <span data-ttu-id="76145-190">Вызовите функцию **финднекстпринтерчанженотификатион** только в том случае, если функция Wait завершилась без времени ожидания. Исключением является то, что при вызове **финднекстпринтерчанженотификатион** с параметром " **\_ \_ \_ Обновить" параметры уведомления принтера** , заданные в аргументе *ппринтернотифйоптионс* .</span><span class="sxs-lookup"><span data-stu-id="76145-190">Call the **FindNextPrinterChangeNotification** function only if the wait function succeeds without timing out. The exception is when **FindNextPrinterChangeNotification** is called with the **PRINTER\_NOTIFY\_OPTIONS\_REFRESH** bit set in the *pPrinterNotifyOptions* parameter.</span></span> <span data-ttu-id="76145-191">Обратите внимание, что даже если этот флаг установлен, в параметре *пппринтернотифинфо* по-прежнему может быть задан флаг **\_ \_ \_ отклонения сведений о принтере** .</span><span class="sxs-lookup"><span data-stu-id="76145-191">Note that even when this flag is set, it is still possible for the **PRINTER\_NOTIFY\_INFO\_DISCARDED** flag to be set in the *ppPrinterNotifyInfo* parameter.</span></span>

<span data-ttu-id="76145-192">Чтобы продолжить наблюдение за изменениями принтера или сервера печати, повторите цикл вызова одной из [функций ожидания](/windows/desktop/Sync/wait-functions) , а затем вызовите функцию **финднекстпринтерчанженотификатион** , чтобы проверить изменение и сбросить объект уведомления.</span><span class="sxs-lookup"><span data-stu-id="76145-192">To continue monitoring the printer or print server for changes, repeat the cycle of calling one of the [wait functions](/windows/desktop/Sync/wait-functions) , and then calling the **FindNextPrinterChangeNotification** function to examine the change and reset the notification object.</span></span>

<span data-ttu-id="76145-193">**Финднекстпринтерчанженотификатион** может объединять несколько изменений одного и того же поля сведений о принтере в одно уведомление.</span><span class="sxs-lookup"><span data-stu-id="76145-193">**FindNextPrinterChangeNotification** may combine multiple changes to the same printer information field into a single notification.</span></span> <span data-ttu-id="76145-194">В этом случае функция, как правило, сворачивает все изменения для поля в одну запись в массиве структур [**\_ \_ \_ данных с уведомлением принтера**](printer-notify-info-data.md) в *пппринтернотифинфо*; одна запись содержит только самые актуальные сведения.</span><span class="sxs-lookup"><span data-stu-id="76145-194">When this occurs, the function typically collapses all changes for the field into a single entry in the array of [**PRINTER\_NOTIFY\_INFO\_DATA**](printer-notify-info-data.md) structures in *ppPrinterNotifyInfo*; the single entry reports only the most current information.</span></span> <span data-ttu-id="76145-195">Однако для некоторых полей сведений о заданиях и принтерах функция может возвращать несколько записей массива для одного поля.</span><span class="sxs-lookup"><span data-stu-id="76145-195">However, for some job and printer information fields, the function can return multiple array entries for the same field.</span></span> <span data-ttu-id="76145-196">В этом случае последняя запись массива для поля сообщает о текущих данных, а более ранние записи содержат данные для промежуточных этапов.</span><span class="sxs-lookup"><span data-stu-id="76145-196">In this case, the last array entry for the field reports the current data, and the earlier entries contain the data for the intermediate stages.</span></span>

<span data-ttu-id="76145-197">Если объект уведомления об изменениях больше не нужен, закройте его, вызвав функцию [**финдклосепринтерчанженотификатион**](findcloseprinterchangenotification.md) .</span><span class="sxs-lookup"><span data-stu-id="76145-197">When you no longer need the change notification object, close it by calling the [**FindClosePrinterChangeNotification**](findcloseprinterchangenotification.md) function.</span></span>

> [!Note]  
> <span data-ttu-id="76145-198">В Windows XP с пакетом обновления 2 (SP2) и более поздних версий брандмауэр подключения к Интернету (ICF) блокирует порты принтера по умолчанию, но можно включить исключение для общего доступа к файлам и принтерам.</span><span class="sxs-lookup"><span data-stu-id="76145-198">In Windows XP with Service Pack 2 (SP2) and later, the Internet Connection Firewall (ICF) blocks printer ports by default, but an exception for File and Print Sharing can be enabled.</span></span> <span data-ttu-id="76145-199">Если пользователь устанавливает подключение принтера к другому компьютеру и исключение не включено, пользователь не будет получать уведомления об изменении принтера с сервера.</span><span class="sxs-lookup"><span data-stu-id="76145-199">If a user makes a printer connection to another machine, and the exception is not enabled, then the user will not receive printer change notifications from the server.</span></span> <span data-ttu-id="76145-200">Администратор компьютера должен включить исключение.</span><span class="sxs-lookup"><span data-stu-id="76145-200">A machine admin will have to enable exception.</span></span>

 

## <a name="examples"></a><span data-ttu-id="76145-201">Примеры</span><span class="sxs-lookup"><span data-stu-id="76145-201">Examples</span></span>

<span data-ttu-id="76145-202">В следующем образце кода показано, как можно отслеживать состояние принтера с помощью этих функций.</span><span class="sxs-lookup"><span data-stu-id="76145-202">The following code sample illustrates how you might monitor printer status by using these functions.</span></span>


```C++
// Get change notification handle for the printer   
chgObject = FindFirstPrinterChangeNotification( 
                hPrinter, 
                PRINTER_CHANGE_JOB, 
                0, 
                NULL); 

if (chgObject != INVALID_HANDLE_VALUE) {
    while (bKeepMonitoring) {
        // Wait for the change notification 
        WaitForSingleObject(chgObject, INFINITE);

        fcnreturn = FindNextPrinterChangeNotification(
                        chgObject, 
                        pdwChange, 
                        NULL, 
                        NULL);

        if (fcnreturn) {
            // Check value of *pdwChange and 
            //  deal with the indicated change 
        }
        // Insert some mechanism to stop monitoring
        //  such as: 
        //
        // if (something happens) {
        //     bKeepMonitoring = false; 
        // }
        //
    }
    // Close Printer Change Notification handle when finished. 
    FindClosePrinterChangeNotification(chgObject);
} else {
    // Unable to open printer change notification handle 
    dwStatus = GetLastError();
}
```



## <a name="requirements"></a><span data-ttu-id="76145-203">Требования</span><span class="sxs-lookup"><span data-stu-id="76145-203">Requirements</span></span>



| <span data-ttu-id="76145-204">Требование</span><span class="sxs-lookup"><span data-stu-id="76145-204">Requirement</span></span> | <span data-ttu-id="76145-205">Значение</span><span class="sxs-lookup"><span data-stu-id="76145-205">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="76145-206">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="76145-206">Minimum supported client</span></span><br/> | <span data-ttu-id="76145-207">Windows 2000 Professional \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="76145-207">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                                |
| <span data-ttu-id="76145-208">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="76145-208">Minimum supported server</span></span><br/> | <span data-ttu-id="76145-209">Windows 2000 Server \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="76145-209">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                      |
| <span data-ttu-id="76145-210">Заголовок</span><span class="sxs-lookup"><span data-stu-id="76145-210">Header</span></span><br/>                   | <dl> <span data-ttu-id="76145-211"><dt>Винспул. h (включение Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="76145-211"><dt>Winspool.h (include Windows.h)</dt></span></span> </dl> |
| <span data-ttu-id="76145-212">Библиотека</span><span class="sxs-lookup"><span data-stu-id="76145-212">Library</span></span><br/>                  | <dl> <span data-ttu-id="76145-213"><dt>Винспул. lib</dt></span><span class="sxs-lookup"><span data-stu-id="76145-213"><dt>Winspool.lib</dt></span></span> </dl>                   |
| <span data-ttu-id="76145-214">DLL</span><span class="sxs-lookup"><span data-stu-id="76145-214">DLL</span></span><br/>                      | <dl> <span data-ttu-id="76145-215"><dt>Spoolss.dll</dt></span><span class="sxs-lookup"><span data-stu-id="76145-215"><dt>Spoolss.dll</dt></span></span> </dl>                    |



## <a name="see-also"></a><span data-ttu-id="76145-216">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="76145-216">See also</span></span>

<dl> <dt>

[<span data-ttu-id="76145-217">Вывод на печать</span><span class="sxs-lookup"><span data-stu-id="76145-217">Printing</span></span>](printdocs-printing.md)
</dt> <dt>

[<span data-ttu-id="76145-218">Функции API очереди печати принтера</span><span class="sxs-lookup"><span data-stu-id="76145-218">Print Spooler API Functions</span></span>](printing-and-print-spooler-functions.md)
</dt> <dt>

[<span data-ttu-id="76145-219">**финдклосепринтерчанженотификатион**</span><span class="sxs-lookup"><span data-stu-id="76145-219">**FindClosePrinterChangeNotification**</span></span>](findcloseprinterchangenotification.md)
</dt> <dt>

[<span data-ttu-id="76145-220">**финдфирстпринтерчанженотификатион**</span><span class="sxs-lookup"><span data-stu-id="76145-220">**FindFirstPrinterChangeNotification**</span></span>](findfirstprinterchangenotification.md)
</dt> <dt>

[<span data-ttu-id="76145-221">**\_сведения об уведомлении принтера \_**</span><span class="sxs-lookup"><span data-stu-id="76145-221">**PRINTER\_NOTIFY\_INFO**</span></span>](printer-notify-info.md)
</dt> <dt>

[<span data-ttu-id="76145-222">**\_данные уведомления \_ принтера \_**</span><span class="sxs-lookup"><span data-stu-id="76145-222">**PRINTER\_NOTIFY\_INFO\_DATA**</span></span>](printer-notify-info-data.md)
</dt> <dt>

[<span data-ttu-id="76145-223">**\_Параметры уведомления \_ принтера**</span><span class="sxs-lookup"><span data-stu-id="76145-223">**PRINTER\_NOTIFY\_OPTIONS**</span></span>](printer-notify-options.md)
</dt> </dl>

 

