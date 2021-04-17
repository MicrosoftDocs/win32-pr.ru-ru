---
description: Функция Делетепринтердриверекс удаляет указанное имя драйвера принтера из списка имен поддерживаемых драйверов на сервере и удаляет файлы, связанные с драйвером. Эта функция также может удалять определенные версии драйвера.
ms.assetid: 1a3d7c7f-1d45-4877-a8f7-a77f40e3c319
title: Функция Делетепринтердриверекс (Винспул. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- DeletePrinterDriverEx
- DeletePrinterDriverExA
- DeletePrinterDriverExW
api_type:
- DllExport
api_location:
- Winspool.drv
ms.openlocfilehash: b88ef38236961286875a1885dad9dde936887d13
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "105702334"
---
# <a name="deleteprinterdriverex-function"></a><span data-ttu-id="0752e-104">Функция Делетепринтердриверекс</span><span class="sxs-lookup"><span data-stu-id="0752e-104">DeletePrinterDriverEx function</span></span>

<span data-ttu-id="0752e-105">Функция **делетепринтердриверекс** удаляет указанное имя драйвера принтера из списка имен поддерживаемых драйверов на сервере и удаляет файлы, связанные с драйвером.</span><span class="sxs-lookup"><span data-stu-id="0752e-105">The **DeletePrinterDriverEx** function removes the specified printer-driver name from the list of names of supported drivers on a server and deletes the files associated with the driver.</span></span> <span data-ttu-id="0752e-106">Эта функция также может удалять определенные версии драйвера.</span><span class="sxs-lookup"><span data-stu-id="0752e-106">This function can also delete specific versions of the driver.</span></span>

## <a name="syntax"></a><span data-ttu-id="0752e-107">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="0752e-107">Syntax</span></span>


```C++
BOOL DeletePrinterDriverEx(
  _In_ LPTSTR pName,
  _In_ LPTSTR pEnvironment,
  _In_ LPTSTR pDriverName,
  _In_ DWORD  dwDeleteFlag,
  _In_ DWORD  dwVersionFlag
);
```



## <a name="parameters"></a><span data-ttu-id="0752e-108">Параметры</span><span class="sxs-lookup"><span data-stu-id="0752e-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="0752e-109">*pName* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="0752e-109">*pName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="0752e-110">Указатель на строку, завершающуюся нулем, которая указывает имя сервера, с которого должен быть удален драйвер.</span><span class="sxs-lookup"><span data-stu-id="0752e-110">A pointer to a null-terminated string that specifies the name of the server from which the driver is to be deleted.</span></span> <span data-ttu-id="0752e-111">Если этот параметр имеет **значение NULL**, функция удаляет драйвер принтера с локального компьютера.</span><span class="sxs-lookup"><span data-stu-id="0752e-111">If this parameter is **NULL**, the function deletes the printer-driver from the local computer.</span></span>

</dd> <dt>

<span data-ttu-id="0752e-112">*пенвиронмент* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="0752e-112">*pEnvironment* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="0752e-113">Указатель на строку, завершающуюся нулем, которая указывает среду, из которой должен быть удален драйвер (например, Windows NT x86, Windows IA64 или Windows x64).</span><span class="sxs-lookup"><span data-stu-id="0752e-113">A pointer to a null-terminated string that specifies the environment from which the driver is to be deleted (for example, Windows NT x86, Windows IA64, or Windows x64).</span></span> <span data-ttu-id="0752e-114">Если этот параметр имеет **значение NULL**, имя драйвера удаляется из текущей среды вызывающего приложения и клиентского компьютера (не из целевого приложения и сервера печати).</span><span class="sxs-lookup"><span data-stu-id="0752e-114">If this parameter is **NULL**, the driver name is deleted from the current environment of the calling application and client computer (not of the destination application and print server).</span></span>

</dd> <dt>

<span data-ttu-id="0752e-115">*пдривернаме* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="0752e-115">*pDriverName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="0752e-116">Указатель на строку с завершающим нулем, указывающую имя драйвера для удаления.</span><span class="sxs-lookup"><span data-stu-id="0752e-116">A pointer to a null-terminated string specifying the name of the driver to delete.</span></span>

</dd> <dt>

<span data-ttu-id="0752e-117">*двделетефлаг* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="0752e-117">*dwDeleteFlag* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="0752e-118">Параметры удаления файлов и версий драйвера.</span><span class="sxs-lookup"><span data-stu-id="0752e-118">The options for deleting files and versions of the driver.</span></span> <span data-ttu-id="0752e-119">Этот параметр может принимать одно или несколько следующих значений.</span><span class="sxs-lookup"><span data-stu-id="0752e-119">This parameter can be one or more of the following values.</span></span>



| <span data-ttu-id="0752e-120">Значение</span><span class="sxs-lookup"><span data-stu-id="0752e-120">Value</span></span>                                                                                                                                                                                                     | <span data-ttu-id="0752e-121">Значение</span><span class="sxs-lookup"><span data-stu-id="0752e-121">Meaning</span></span>                                                                                                                                                                               |
|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="DPD_DELETE_SPECIFIC_VERSION"></span><span id="dpd_delete_specific_version"></span><dl> <span data-ttu-id="0752e-122"><dt>**DPD \_ удалить \_ определенную \_ версию**</dt></span><span class="sxs-lookup"><span data-stu-id="0752e-122"><dt>**DPD\_DELETE\_SPECIFIC\_VERSION**</dt></span></span> </dl> | <span data-ttu-id="0752e-123">Удаляет версию, указанную в *двверсионфлаг*.</span><span class="sxs-lookup"><span data-stu-id="0752e-123">Deletes the version specified in *dwVersionFlag*.</span></span> <span data-ttu-id="0752e-124">Это не гарантирует, что драйвер будет удален из списка поддерживаемых драйверов для сервера.</span><span class="sxs-lookup"><span data-stu-id="0752e-124">This does not ensure that the driver will be removed from the list of supported drivers for the server.</span></span><br/>                  |
| <span id="DPD_DELETE_UNUSED_FILES"></span><span id="dpd_delete_unused_files"></span><dl> <span data-ttu-id="0752e-125"><dt>**DPD \_ удалить \_ неиспользуемые \_ файлы**</dt></span><span class="sxs-lookup"><span data-stu-id="0752e-125"><dt>**DPD\_DELETE\_UNUSED\_FILES**</dt></span></span> </dl>             | <span data-ttu-id="0752e-126">Удаляет все неиспользуемые файлы драйверов.</span><span class="sxs-lookup"><span data-stu-id="0752e-126">Removes any unused driver files.</span></span><br/>                                                                                                                                           |
| <span id="DPD_DELETE_ALL_FILES"></span><span id="dpd_delete_all_files"></span><dl> <span data-ttu-id="0752e-127"><dt>**DPD \_ удалить \_ все \_ файлы**</dt></span><span class="sxs-lookup"><span data-stu-id="0752e-127"><dt>**DPD\_DELETE\_ALL\_FILES**</dt></span></span> </dl>                      | <span data-ttu-id="0752e-128">Удаляет драйвер только в том случае, если все связанные с ним файлы могут быть удалены.</span><span class="sxs-lookup"><span data-stu-id="0752e-128">Deletes the driver only if all its associated files can be removed.</span></span> <span data-ttu-id="0752e-129">Операция удаления завершается ошибкой, если какие либо файлы драйвера используются другим установленным драйвером.</span><span class="sxs-lookup"><span data-stu-id="0752e-129">The delete operation fails if any of the driver's files are being used by some other installed driver.</span></span><br/> |



 

<span data-ttu-id="0752e-130">Если \_ \_ не указана DPD удалить определенную \_ версию, функция удаляет все версии драйвера, если ни одна из них не используется.</span><span class="sxs-lookup"><span data-stu-id="0752e-130">If DPD\_DELETE\_SPECIFIC\_VERSION is not specified, the function deletes all versions of the driver if none of them is in use.</span></span> <span data-ttu-id="0752e-131">Если ни один из DPD \_ \_ не удаляет неиспользуемые \_ файлы или DPD не \_ \_ \_ указан, функция не удаляет файлы драйверов.</span><span class="sxs-lookup"><span data-stu-id="0752e-131">If neither DPD\_DELETE\_UNUSED\_FILES nor DPD\_DELETE\_ALL\_FILES is specified, the function does not delete driver files.</span></span>

</dd> <dt>

<span data-ttu-id="0752e-132">*двверсионфлаг* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="0752e-132">*dwVersionFlag* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="0752e-133">Версия удаляемого драйвера.</span><span class="sxs-lookup"><span data-stu-id="0752e-133">The version of the driver to be deleted.</span></span> <span data-ttu-id="0752e-134">Этот параметр может иметь значение 0, 1, 2 или 3.</span><span class="sxs-lookup"><span data-stu-id="0752e-134">This parameter can be 0, 1, 2 or 3.</span></span> <span data-ttu-id="0752e-135">Этот параметр используется только в том случае, если *двделетефлаг* включает \_ флаг DPD удаления \_ определенной \_ версии.</span><span class="sxs-lookup"><span data-stu-id="0752e-135">This parameter is used only if *dwDeleteFlag* includes the DPD\_DELETE\_SPECIFIC\_VERSION flag.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="0752e-136">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="0752e-136">Return value</span></span>

<span data-ttu-id="0752e-137">Если функция выполнена, возвращаемое значение будет ненулевым.</span><span class="sxs-lookup"><span data-stu-id="0752e-137">If the function succeeds, the return value is a nonzero value.</span></span>

<span data-ttu-id="0752e-138">Если функция выполняется неудачно, возвращается нулевое значение.</span><span class="sxs-lookup"><span data-stu-id="0752e-138">If the function fails, the return value is zero.</span></span>

## <a name="remarks"></a><span data-ttu-id="0752e-139">Комментарии</span><span class="sxs-lookup"><span data-stu-id="0752e-139">Remarks</span></span>

> [!Note]  
> <span data-ttu-id="0752e-140">Это блокирующая или синхронная функция, которая может не возвращать значение немедленно.</span><span class="sxs-lookup"><span data-stu-id="0752e-140">This is a blocking or synchronous function and might not return immediately.</span></span> <span data-ttu-id="0752e-141">Скорость возврата этой функцией зависит от факторов времени выполнения, таких как состояние сети, Конфигурация сервера печати и факторы реализации драйвера принтера, которые трудно предсказать при написании приложения.</span><span class="sxs-lookup"><span data-stu-id="0752e-141">How quickly this function returns depends on run-time factors such as network status, print server configuration, and printer driver implementation factors that are difficult to predict when writing an application.</span></span> <span data-ttu-id="0752e-142">Вызов этой функции из потока, который управляет взаимодействием с пользовательским интерфейсом, может привести к невозможности реагирования приложения.</span><span class="sxs-lookup"><span data-stu-id="0752e-142">Calling this function from a thread that manages interaction with the user interface could make the application appear to be unresponsive.</span></span>

 

<span data-ttu-id="0752e-143">Прежде чем функция удалит файлы драйверов, она вызывает функцию **дрвдриверевент** драйвера, позволяя драйверу удалить все закрытые файлы, которые не используются.</span><span class="sxs-lookup"><span data-stu-id="0752e-143">Before the function deletes the driver files, it calls the driver's **DrvDriverEvent** function, allowing the driver to remove any private files that are not used.</span></span> <span data-ttu-id="0752e-144">Дополнительные сведения о **дрвдриверевент** см. в пакете средств разработки драйверов Microsoft Windows (DDK).</span><span class="sxs-lookup"><span data-stu-id="0752e-144">For more information about **DrvDriverEvent**, see the Microsoft Windows Driver Development Kit (DDK).</span></span>

<span data-ttu-id="0752e-145">Если файлы драйверов загружены в данный момент, функция переместит их в каталог TEMP и помечает их для удаления при перезапуске.</span><span class="sxs-lookup"><span data-stu-id="0752e-145">If the driver files are currently loaded, the function moves them to a temp directory and marks them for deletion on restart.</span></span>

<span data-ttu-id="0752e-146">Перед вызовом **делетепринтердриверекс** необходимо удалить все объекты принтера, использующие драйвер принтера.</span><span class="sxs-lookup"><span data-stu-id="0752e-146">Before calling **DeletePrinterDriverEx**, you must delete all printer objects that use the printer driver.</span></span>

## <a name="requirements"></a><span data-ttu-id="0752e-147">Требования</span><span class="sxs-lookup"><span data-stu-id="0752e-147">Requirements</span></span>



| <span data-ttu-id="0752e-148">Требование</span><span class="sxs-lookup"><span data-stu-id="0752e-148">Requirement</span></span> | <span data-ttu-id="0752e-149">Значение</span><span class="sxs-lookup"><span data-stu-id="0752e-149">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="0752e-150">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="0752e-150">Minimum supported client</span></span><br/> | <span data-ttu-id="0752e-151">Windows 2000 Professional \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="0752e-151">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                                |
| <span data-ttu-id="0752e-152">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="0752e-152">Minimum supported server</span></span><br/> | <span data-ttu-id="0752e-153">Windows 2000 Server \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="0752e-153">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                      |
| <span data-ttu-id="0752e-154">Заголовок</span><span class="sxs-lookup"><span data-stu-id="0752e-154">Header</span></span><br/>                   | <dl> <span data-ttu-id="0752e-155"><dt>Винспул. h (включение Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="0752e-155"><dt>Winspool.h (include Windows.h)</dt></span></span> </dl> |
| <span data-ttu-id="0752e-156">Библиотека</span><span class="sxs-lookup"><span data-stu-id="0752e-156">Library</span></span><br/>                  | <dl> <span data-ttu-id="0752e-157"><dt>Винспул. lib</dt></span><span class="sxs-lookup"><span data-stu-id="0752e-157"><dt>Winspool.lib</dt></span></span> </dl>                   |
| <span data-ttu-id="0752e-158">DLL</span><span class="sxs-lookup"><span data-stu-id="0752e-158">DLL</span></span><br/>                      | <dl> <span data-ttu-id="0752e-159"><dt>Винспул. drv</dt></span><span class="sxs-lookup"><span data-stu-id="0752e-159"><dt>Winspool.drv</dt></span></span> </dl>                   |
| <span data-ttu-id="0752e-160">Имя в кодировке Юникод и ANSI</span><span class="sxs-lookup"><span data-stu-id="0752e-160">Unicode and ANSI names</span></span><br/>   | <span data-ttu-id="0752e-161">**Делетепринтердриверексв** (Юникод) и **делетепринтердриверекса** (ANSI)</span><span class="sxs-lookup"><span data-stu-id="0752e-161">**DeletePrinterDriverExW** (Unicode) and **DeletePrinterDriverExA** (ANSI)</span></span><br/>                     |



## <a name="see-also"></a><span data-ttu-id="0752e-162">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="0752e-162">See also</span></span>

<dl> <dt>

[<span data-ttu-id="0752e-163">Вывод на печать</span><span class="sxs-lookup"><span data-stu-id="0752e-163">Printing</span></span>](printdocs-printing.md)
</dt> <dt>

[<span data-ttu-id="0752e-164">Функции API очереди печати принтера</span><span class="sxs-lookup"><span data-stu-id="0752e-164">Print Spooler API Functions</span></span>](printing-and-print-spooler-functions.md)
</dt> <dt>

[<span data-ttu-id="0752e-165">**аддпринтердриверекс**</span><span class="sxs-lookup"><span data-stu-id="0752e-165">**AddPrinterDriverEx**</span></span>](addprinterdriverex.md)
</dt> </dl>

 

 




