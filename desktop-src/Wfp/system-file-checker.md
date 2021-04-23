---
description: Программа проверки системных файлов, Sfc.exe, позволяет администраторам сканировать все защищенные ресурсы, чтобы проверить их версии.
ms.assetid: 72f69ad2-15d9-4191-a8aa-4c23a2392006
title: " средство проверки системных файлов"
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: da4e0d67f6de6aba62fe262969d7f30db0c45335
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "105664553"
---
# <a name="system-file-checker"></a><span data-ttu-id="523b7-103"> средство проверки системных файлов</span><span class="sxs-lookup"><span data-stu-id="523b7-103">System File Checker</span></span>

<span data-ttu-id="523b7-104">Программа проверки системных файлов, Sfc.exe, позволяет администраторам сканировать все защищенные ресурсы, чтобы проверить их версии.</span><span class="sxs-lookup"><span data-stu-id="523b7-104">The system file checker utility, Sfc.exe, allows administrators to scan all protected resources to verify their versions.</span></span>

<span data-ttu-id="523b7-105">Файлы, критические для перезапуска Windows, которые не соответствуют ожидаемым версиям Windows, могут быть заменены на правильные версии.</span><span class="sxs-lookup"><span data-stu-id="523b7-105">Files critical to restart Windows that do not match the expected Windows version may be replaced with the correct versions.</span></span> <span data-ttu-id="523b7-106">При восстановлении файла также восстанавливаются соответствующие данные реестра.</span><span class="sxs-lookup"><span data-stu-id="523b7-106">If a file is repaired, the corresponding registry data is also repaired.</span></span> <span data-ttu-id="523b7-107">Защищенные файлы, не критические для перезапуска Windows, не восстанавливаются.</span><span class="sxs-lookup"><span data-stu-id="523b7-107">Protected files not critical to restart Windows are not repaired.</span></span>

## <a name="syntax"></a><span data-ttu-id="523b7-108">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="523b7-108">Syntax</span></span>

<span data-ttu-id="523b7-109">Ниже приведен синтаксис командной строки для SFC.</span><span class="sxs-lookup"><span data-stu-id="523b7-109">The following is the command-line syntax for Sfc.</span></span>

<span data-ttu-id="523b7-110">**Параметры SFC \[ = полный путь к файлу\]**</span><span class="sxs-lookup"><span data-stu-id="523b7-110">**SFC options \[=full file path\]**</span></span>

## <a name="options"></a><span data-ttu-id="523b7-111">Параметры</span><span class="sxs-lookup"><span data-stu-id="523b7-111">Options</span></span>

<dl> <dt>

<span data-ttu-id="523b7-112"><span id="_CACHESIZE_x"></span><span id="_cachesize_x"></span><span id="_CACHESIZE_X"></span>/КАЧЕСИЗЕ =*x*</span><span class="sxs-lookup"><span data-stu-id="523b7-112"><span id="_CACHESIZE_x"></span><span id="_cachesize_x"></span><span id="_CACHESIZE_X"></span>/CACHESIZE=*x*</span></span>
</dt> <dd>

<span data-ttu-id="523b7-113">Это значение не поддерживается.</span><span class="sxs-lookup"><span data-stu-id="523b7-113">This value is not supported.</span></span>

<span data-ttu-id="523b7-114">**Windows Server 2003 и Windows XP:** Задает размер файлового кэша.</span><span class="sxs-lookup"><span data-stu-id="523b7-114">**Windows Server 2003 and Windows XP:** Sets the file cache size.</span></span> <span data-ttu-id="523b7-115">Размер кэша по умолчанию — 0x32 (50 МБ).</span><span class="sxs-lookup"><span data-stu-id="523b7-115">The default size of the cache is 0x32 (50 MB).</span></span>

</dd> <dt>

<span data-ttu-id="523b7-116"><span id="_CANCEL"></span><span id="_cancel"></span>/канцел</span><span class="sxs-lookup"><span data-stu-id="523b7-116"><span id="_CANCEL"></span><span id="_cancel"></span>/CANCEL</span></span>
</dt> <dd>

<span data-ttu-id="523b7-117">Это значение не поддерживается.</span><span class="sxs-lookup"><span data-stu-id="523b7-117">This value is not supported.</span></span>

</dd> <dt>

<span data-ttu-id="523b7-118"><span id="_ENABLE"></span><span id="_enable"></span>Разрешение</span><span class="sxs-lookup"><span data-stu-id="523b7-118"><span id="_ENABLE"></span><span id="_enable"></span>/ENABLE</span></span>
</dt> <dd>

<span data-ttu-id="523b7-119">Это значение не поддерживается.</span><span class="sxs-lookup"><span data-stu-id="523b7-119">This value is not supported.</span></span>

</dd> <dt>

<span data-ttu-id="523b7-120"><span id="_FILESONLY"></span><span id="_filesonly"></span>/филесонли</span><span class="sxs-lookup"><span data-stu-id="523b7-120"><span id="_FILESONLY"></span><span id="_filesonly"></span>/FILESONLY</span></span>
</dt> <dd>

<span data-ttu-id="523b7-121">Проверьте или исправьте только файлы.</span><span class="sxs-lookup"><span data-stu-id="523b7-121">Verify or repair only files.</span></span> <span data-ttu-id="523b7-122">Не проверять и не восстанавливать разделы реестра.</span><span class="sxs-lookup"><span data-stu-id="523b7-122">Do not verify or repair registry keys.</span></span>

<span data-ttu-id="523b7-123">**Windows XP:** Не поддерживается.</span><span class="sxs-lookup"><span data-stu-id="523b7-123">**Windows XP:** Not supported.</span></span>

</dd> <dt>

<span data-ttu-id="523b7-124"><span id="_OFFBOOTDIR"></span><span id="_offbootdir"></span>/оффбутдир</span><span class="sxs-lookup"><span data-stu-id="523b7-124"><span id="_OFFBOOTDIR"></span><span id="_offbootdir"></span>/OFFBOOTDIR</span></span>
</dt> <dd>

<span data-ttu-id="523b7-125">Используйте этот параметр для автономного восстановления.</span><span class="sxs-lookup"><span data-stu-id="523b7-125">Use this option for offline repairs.</span></span> <span data-ttu-id="523b7-126">Укажите расположение каталога автономной загрузки.</span><span class="sxs-lookup"><span data-stu-id="523b7-126">Specify the location of the offline boot directory.</span></span>

<span data-ttu-id="523b7-127">**Windows XP:** Не поддерживается.</span><span class="sxs-lookup"><span data-stu-id="523b7-127">**Windows XP:** Not supported.</span></span>

</dd> <dt>

<span data-ttu-id="523b7-128"><span id="_OFFWINDIR"></span><span id="_offwindir"></span>/оффвиндир</span><span class="sxs-lookup"><span data-stu-id="523b7-128"><span id="_OFFWINDIR"></span><span id="_offwindir"></span>/OFFWINDIR</span></span>
</dt> <dd>

<span data-ttu-id="523b7-129">Используйте этот параметр для автономного восстановления.</span><span class="sxs-lookup"><span data-stu-id="523b7-129">Use this option for offline repairs.</span></span> <span data-ttu-id="523b7-130">Укажите расположение автономного каталога Windows.</span><span class="sxs-lookup"><span data-stu-id="523b7-130">Specify the location of the offline Windows directory.</span></span>

<span data-ttu-id="523b7-131">**Windows XP:** Не поддерживается.</span><span class="sxs-lookup"><span data-stu-id="523b7-131">**Windows XP:** Not supported.</span></span>

</dd> <dt>

<span data-ttu-id="523b7-132"><span id="_PURGECACHE"></span><span id="_purgecache"></span>/пуржекаче</span><span class="sxs-lookup"><span data-stu-id="523b7-132"><span id="_PURGECACHE"></span><span id="_purgecache"></span>/PURGECACHE</span></span>
</dt> <dd>

<span data-ttu-id="523b7-133">Это значение не поддерживается.</span><span class="sxs-lookup"><span data-stu-id="523b7-133">This value is not supported.</span></span>

<span data-ttu-id="523b7-134">**Windows Server 2003 и Windows XP:** Очищает файловый кэш и сканирует все защищенные системные файлы.</span><span class="sxs-lookup"><span data-stu-id="523b7-134">**Windows Server 2003 and Windows XP:** Empties the file cache and scans all protected system files.</span></span>

</dd> <dt>

<span data-ttu-id="523b7-135"><span id="_QUIET"></span><span id="_quiet"></span>/QUIET</span><span class="sxs-lookup"><span data-stu-id="523b7-135"><span id="_QUIET"></span><span id="_quiet"></span>/QUIET</span></span>
</dt> <dd>

<span data-ttu-id="523b7-136">Это значение не поддерживается.</span><span class="sxs-lookup"><span data-stu-id="523b7-136">This value is not supported.</span></span>

</dd> <dt>

<span data-ttu-id="523b7-137"><span id="_REVERT"></span><span id="_revert"></span>/реверт</span><span class="sxs-lookup"><span data-stu-id="523b7-137"><span id="_REVERT"></span><span id="_revert"></span>/REVERT</span></span>
</dt> <dd>

<span data-ttu-id="523b7-138">Вернитесь к параметрам по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="523b7-138">Return to default settings.</span></span>

<span data-ttu-id="523b7-139">**Windows Server 2008 и Windows Vista:** Не поддерживается.</span><span class="sxs-lookup"><span data-stu-id="523b7-139">**Windows Server 2008 and Windows Vista:** Not supported.</span></span>

</dd> <dt>

<span data-ttu-id="523b7-140"><span id="_SCANBOOT"></span><span id="_scanboot"></span>/сканбут</span><span class="sxs-lookup"><span data-stu-id="523b7-140"><span id="_SCANBOOT"></span><span id="_scanboot"></span>/SCANBOOT</span></span>
</dt> <dd>

<span data-ttu-id="523b7-141">Это значение не поддерживается.</span><span class="sxs-lookup"><span data-stu-id="523b7-141">This value is not supported.</span></span>

<span data-ttu-id="523b7-142">**Windows Server 2003 и Windows XP:** Сканирует все защищенные системные файлы при каждой загрузке.</span><span class="sxs-lookup"><span data-stu-id="523b7-142">**Windows Server 2003 and Windows XP:** Scans all protected system files at every boot.</span></span>

</dd> <dt>

<span data-ttu-id="523b7-143"><span id="_SCANFILE"></span><span id="_scanfile"></span>/сканфиле</span><span class="sxs-lookup"><span data-stu-id="523b7-143"><span id="_SCANFILE"></span><span id="_scanfile"></span>/SCANFILE</span></span>
</dt> <dd>

<span data-ttu-id="523b7-144">Сканирует и восстанавливает файл, расположенный по указанному полному пути.</span><span class="sxs-lookup"><span data-stu-id="523b7-144">Scans and repairs the file located at the specified full path.</span></span>

<span data-ttu-id="523b7-145">**Windows XP:** Не поддерживается.</span><span class="sxs-lookup"><span data-stu-id="523b7-145">**Windows XP:** Not supported.</span></span>

</dd> <dt>

<span data-ttu-id="523b7-146"><span id="_SCANNOW"></span><span id="_scannow"></span>/SCANNOW</span><span class="sxs-lookup"><span data-stu-id="523b7-146"><span id="_SCANNOW"></span><span id="_scannow"></span>/SCANNOW</span></span>
</dt> <dd>

<span data-ttu-id="523b7-147">Немедленно сканирует все защищенные системные файлы.</span><span class="sxs-lookup"><span data-stu-id="523b7-147">Scans all protected system files immediately.</span></span>

</dd> <dt>

<span data-ttu-id="523b7-148"><span id="_SCANONCE"></span><span id="_scanonce"></span>/сканонце</span><span class="sxs-lookup"><span data-stu-id="523b7-148"><span id="_SCANONCE"></span><span id="_scanonce"></span>/SCANONCE</span></span>
</dt> <dd>

<span data-ttu-id="523b7-149">Это значение не поддерживается.</span><span class="sxs-lookup"><span data-stu-id="523b7-149">This value is not supported.</span></span>

<span data-ttu-id="523b7-150">**Windows Server 2003 и Windows XP:** Сканирует все защищенные системные файлы при следующей загрузке.</span><span class="sxs-lookup"><span data-stu-id="523b7-150">**Windows Server 2003 and Windows XP:** Scans all protected system files at the next boot.</span></span>

</dd> <dt>

<span data-ttu-id="523b7-151"><span id="_VERIFYFILE"></span><span id="_verifyfile"></span>/верифифиле</span><span class="sxs-lookup"><span data-stu-id="523b7-151"><span id="_VERIFYFILE"></span><span id="_verifyfile"></span>/VERIFYFILE</span></span>
</dt> <dd>

<span data-ttu-id="523b7-152">Проверяет файл по указанному полному пути.</span><span class="sxs-lookup"><span data-stu-id="523b7-152">Verifies the file at the specified full path.</span></span> <span data-ttu-id="523b7-153">Этот параметр не восстанавливает файл.</span><span class="sxs-lookup"><span data-stu-id="523b7-153">This option does not repair the file.</span></span>

<span data-ttu-id="523b7-154">**Windows XP:** Не поддерживается.</span><span class="sxs-lookup"><span data-stu-id="523b7-154">**Windows XP:** Not supported.</span></span>

</dd> <dt>

<span data-ttu-id="523b7-155"><span id="_VERIFYONLY"></span><span id="_verifyonly"></span>/верифйонли</span><span class="sxs-lookup"><span data-stu-id="523b7-155"><span id="_VERIFYONLY"></span><span id="_verifyonly"></span>/VERIFYONLY</span></span>
</dt> <dd>

<span data-ttu-id="523b7-156">Сканирует все защищенные системные файлы, но не восстанавливает их.</span><span class="sxs-lookup"><span data-stu-id="523b7-156">Scans all protected system files but does not repair files.</span></span>

<span data-ttu-id="523b7-157">**Windows XP:** Не поддерживается.</span><span class="sxs-lookup"><span data-stu-id="523b7-157">**Windows XP:** Not supported.</span></span>

</dd> </dl>

<span data-ttu-id="523b7-158">SFC устанавливает следующее значение реестра:</span><span class="sxs-lookup"><span data-stu-id="523b7-158">Sfc sets the following registry value:</span></span>

 <span data-ttu-id="523b7-159">= HKEY \_ Локальное \_ компьютерное \\ программное обеспечение \\ Microsoft \\ Windows NT \\ CurrentVersion \\ Winlogon \\ сфкскан</span><span class="sxs-lookup"><span data-stu-id="523b7-159">= HKEY\_LOCAL\_MACHINE\\SOFTWARE\\Microsoft\\Windows NT\\CurrentVersion\\Winlogon\\SFCScan</span></span>

<span data-ttu-id="523b7-160">Дополнительные сведения см. в разделе [значения реестра WFP](wfp-registry-values.md).</span><span class="sxs-lookup"><span data-stu-id="523b7-160">For more information, see [WFP Registry Values](wfp-registry-values.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="523b7-161">Комментарии</span><span class="sxs-lookup"><span data-stu-id="523b7-161">Remarks</span></span>

<span data-ttu-id="523b7-162">Только в Windows Vista для переменной среды **\_ \_ журнала трассировки Windows** можно задать расположение допустимого каталога для получения файла журнала.</span><span class="sxs-lookup"><span data-stu-id="523b7-162">On Windows Vista only, you can set the **WINDOWS\_TRACING\_LOGFILE** environment variable to the location of a valid directory to receive a log file.</span></span>

## <a name="examples"></a><span data-ttu-id="523b7-163">Примеры</span><span class="sxs-lookup"><span data-stu-id="523b7-163">Examples</span></span>

<span data-ttu-id="523b7-164">В примерах командных строк приведены примеры синтаксиса sfc.exe.</span><span class="sxs-lookup"><span data-stu-id="523b7-164">The following sample command lines are examples of sfc.exe syntax.</span></span>

<span data-ttu-id="523b7-165">**sfc/SCANNOW**</span><span class="sxs-lookup"><span data-stu-id="523b7-165">**sfc /SCANNOW**</span></span>

<span data-ttu-id="523b7-166">**SFC/ВЕРИФИФИЛЕ = c: \\ Windows \\ system32 \\kernel32.dll**</span><span class="sxs-lookup"><span data-stu-id="523b7-166">**sfc /VERIFYFILE=c:\\windows\\system32\\kernel32.dll**</span></span>

<span data-ttu-id="523b7-167">**SFC/СКАНФИЛЕ = d: \\ Windows \\ system32 \\kernel32.dll/оффбутдир = d: \\ /оффвиндир = d: \\ Windows**</span><span class="sxs-lookup"><span data-stu-id="523b7-167">**sfc /SCANFILE=d:\\windows\\system32\\kernel32.dll /OFFBOOTDIR=d:\\ /OFFWINDIR=d:\\windows**</span></span>

<span data-ttu-id="523b7-168">**SFC/ВЕРИФЙОНЛИ/ФИЛЕСОНЛИ**</span><span class="sxs-lookup"><span data-stu-id="523b7-168">**sfc /VERIFYONLY /FILESONLY**</span></span>

 

 



