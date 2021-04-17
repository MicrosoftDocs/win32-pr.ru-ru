---
description: Функция Уикреатепатчпаккажеекс принимает файл создания пакета (PCP-файл) и создает пакет исправлений установщик Windows (MSP-пакет). Вызов Msimsp.exe является рекомендуемым методом для использования Patchwiz.dll.
ms.assetid: 76d9a21d-73bc-41fc-8ed0-7d7d7deff815
title: Уикреатепатчпаккажеекс (Patchwiz.dll)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ac61371d1e7bf1809880c8f10a403d1730adc8e1
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "105673165"
---
# <a name="uicreatepatchpackageex-patchwizdll"></a><span data-ttu-id="ef7c4-104">Уикреатепатчпаккажеекс (Patchwiz.dll)</span><span class="sxs-lookup"><span data-stu-id="ef7c4-104">UiCreatePatchPackageEx (Patchwiz.dll)</span></span>

<span data-ttu-id="ef7c4-105">Функция Уикреатепатчпаккажеекс принимает файл создания пакета (PCP-файл) и создает пакет исправлений установщик Windows (MSP-пакет).</span><span class="sxs-lookup"><span data-stu-id="ef7c4-105">The UiCreatePatchPackageEx function takes a package creation file (.pcp file) and generates a Windows Installer patch package (.msp package).</span></span> <span data-ttu-id="ef7c4-106">Вызов [Msimsp.exe](msimsp-exe.md) является рекомендуемым методом для использования [Patchwiz.dll](patchwiz-dll.md).</span><span class="sxs-lookup"><span data-stu-id="ef7c4-106">Calling [Msimsp.exe](msimsp-exe.md) is the recommended method for using [Patchwiz.dll](patchwiz-dll.md).</span></span>

<span data-ttu-id="ef7c4-107">Функция Уикреатепатчпаккажеекс доступна начиная с версии Patchwiz.dll 4,0 и расширяет функциональные возможности функции [уикреатепатчпаккаже](uicreatepatchpackage-patchwiz-dll-.md) .</span><span class="sxs-lookup"><span data-stu-id="ef7c4-107">The UiCreatePatchPackageEx function is available beginning with Patchwiz.dll version 4.0 and extends the functionality of the [UiCreatePatchPackage](uicreatepatchpackage-patchwiz-dll-.md) function.</span></span>

``` syntax
UINT UiCreatePatchPackageEx(
  LPCTSTR szPcpPath,              
  LPCTSTR szPatchPath,            
  LPCTSTR szLogPath,             
  HWND hwndStatus,                
  LPCTSTR szTempFolder,           
  BOOL fRemoveTempFolderContents,
  DWORD dwFlags,
  DWORD dwReserved    
);
```

## <a name="parameters"></a><span data-ttu-id="ef7c4-108">Параметры</span><span class="sxs-lookup"><span data-stu-id="ef7c4-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="ef7c4-109"><span id="szPcpPath"></span><span id="szpcppath"></span><span id="SZPCPPATH"></span>*сзпкппас*</span><span class="sxs-lookup"><span data-stu-id="ef7c4-109"><span id="szPcpPath"></span><span id="szpcppath"></span><span id="SZPCPPATH"></span>*szPcpPath*</span></span>
</dt> <dd>

<span data-ttu-id="ef7c4-110">Полный путь к файлу свойств создания исправления (файл. PCP) для этого исправления.</span><span class="sxs-lookup"><span data-stu-id="ef7c4-110">Full path to the patch creation properties file (.pcp file) for this patch.</span></span>

</dd> <dt>

<span data-ttu-id="ef7c4-111"><span id="szPatchPath"></span><span id="szpatchpath"></span><span id="SZPATCHPATH"></span>*сзпатчпас*</span><span class="sxs-lookup"><span data-stu-id="ef7c4-111"><span id="szPatchPath"></span><span id="szpatchpath"></span><span id="SZPATCHPATH"></span>*szPatchPath*</span></span>
</dt> <dd>

<span data-ttu-id="ef7c4-112">Полный путь к создаваемому пакету исправлений установщик Windows (MSP-файл).</span><span class="sxs-lookup"><span data-stu-id="ef7c4-112">Full path to the Windows Installer patch package (.msp file) that is to be created.</span></span> <span data-ttu-id="ef7c4-113">Этот параметр может иметь **значение NULL** или быть пустой строкой, но не может быть пропущен.</span><span class="sxs-lookup"><span data-stu-id="ef7c4-113">This parameter may be **NULL** or an empty string but may not be omitted.</span></span> <span data-ttu-id="ef7c4-114">Если он имеет **значение NULL** или является пустой строкой, функция использует значение Патчаутпутпас в [таблице свойств (Patchwiz.dll)](properties-table-patchwiz-dll-.md).</span><span class="sxs-lookup"><span data-stu-id="ef7c4-114">If it is **NULL** or an empty string, the function uses the value of PatchOutputPath in the [Properties Table (Patchwiz.dll)](properties-table-patchwiz-dll-.md).</span></span>

</dd> <dt>

<span data-ttu-id="ef7c4-115"><span id="szLogPath"></span><span id="szlogpath"></span><span id="SZLOGPATH"></span>*сзлогпас*</span><span class="sxs-lookup"><span data-stu-id="ef7c4-115"><span id="szLogPath"></span><span id="szlogpath"></span><span id="SZLOGPATH"></span>*szLogPath*</span></span>
</dt> <dd>

<span data-ttu-id="ef7c4-116">Полный путь к текстовому файлу журнала, который будет добавлен.</span><span class="sxs-lookup"><span data-stu-id="ef7c4-116">Full path to a text log file that will be appended.</span></span> <span data-ttu-id="ef7c4-117">Этот параметр может иметь **значение NULL** или быть пустой строкой, но не может быть пропущен.</span><span class="sxs-lookup"><span data-stu-id="ef7c4-117">This parameter may be **NULL** or an empty string but may not be omitted.</span></span>

</dd> <dt>

<span data-ttu-id="ef7c4-118"><span id="hwndStatus"></span><span id="hwndstatus"></span><span id="HWNDSTATUS"></span>*хвндстатус*</span><span class="sxs-lookup"><span data-stu-id="ef7c4-118"><span id="hwndStatus"></span><span id="hwndstatus"></span><span id="HWNDSTATUS"></span>*hwndStatus*</span></span>
</dt> <dd>

<span data-ttu-id="ef7c4-119">Обработчик для окна, отображающего текст состояния.</span><span class="sxs-lookup"><span data-stu-id="ef7c4-119">Handle to a window that displays the status text.</span></span> <span data-ttu-id="ef7c4-120">Этот параметр может иметь **значение NULL** или быть пустой строкой, но не может быть пропущен.</span><span class="sxs-lookup"><span data-stu-id="ef7c4-120">This parameter may be **NULL** or an empty string but may not be omitted.</span></span>

</dd> <dt>

<span data-ttu-id="ef7c4-121"><span id="szTempFolder"></span><span id="sztempfolder"></span><span id="SZTEMPFOLDER"></span>*сзтемпфолдер*</span><span class="sxs-lookup"><span data-stu-id="ef7c4-121"><span id="szTempFolder"></span><span id="sztempfolder"></span><span id="SZTEMPFOLDER"></span>*szTempFolder*</span></span>
</dt> <dd>

<span data-ttu-id="ef7c4-122">Расположение временных файлов.</span><span class="sxs-lookup"><span data-stu-id="ef7c4-122">Location for temporary files.</span></span> <span data-ttu-id="ef7c4-123">Этот параметр может иметь **значение NULL** или быть пустой строкой, но не может быть пропущен.</span><span class="sxs-lookup"><span data-stu-id="ef7c4-123">This parameter may be **NULL** or an empty string but may not be omitted.</span></span> <span data-ttu-id="ef7c4-124">Пользователь должен иметь достаточные привилегии для чтения и записи в эту папку.</span><span class="sxs-lookup"><span data-stu-id="ef7c4-124">The user must have sufficient privileges to read and write to this folder.</span></span> <span data-ttu-id="ef7c4-125">Расположение по умолчанию:% TMP% \\ ~ PCW \_ tmp. tmp \\ .</span><span class="sxs-lookup"><span data-stu-id="ef7c4-125">The default location is %TMP%\\~pcw\_tmp.tmp\\.</span></span>

</dd> <dt>

<span data-ttu-id="ef7c4-126"><span id="fRemoveTempFolderContents"></span><span id="fremovetempfoldercontents"></span><span id="FREMOVETEMPFOLDERCONTENTS"></span>*фремоветемпфолдерконтентс*</span><span class="sxs-lookup"><span data-stu-id="ef7c4-126"><span id="fRemoveTempFolderContents"></span><span id="fremovetempfoldercontents"></span><span id="FREMOVETEMPFOLDERCONTENTS"></span>*fRemoveTempFolderContents*</span></span>
</dt> <dd>

<span data-ttu-id="ef7c4-127">Если **значение — true**, удалите временную папку и все ее содержимое, если оно есть.</span><span class="sxs-lookup"><span data-stu-id="ef7c4-127">If **TRUE**, remove the temporary folder and all of its contents if present.</span></span> <span data-ttu-id="ef7c4-128">Если задано **значение false** и имеется папка, функция завершается ошибкой.</span><span class="sxs-lookup"><span data-stu-id="ef7c4-128">If **FALSE**, and folder is present, the function fails.</span></span>

</dd> <dt>

<span data-ttu-id="ef7c4-129"><span id="dwFlags"></span><span id="dwflags"></span><span id="DWFLAGS"></span>*dwFlags*</span><span class="sxs-lookup"><span data-stu-id="ef7c4-129"><span id="dwFlags"></span><span id="dwflags"></span><span id="DWFLAGS"></span>*dwFlags*</span></span>
</dt> <dd>

<span data-ttu-id="ef7c4-130">Этому параметру можно присвоить одно или несколько следующих значений, чтобы указать параметры ведения журнала или пользовательского интерфейса.</span><span class="sxs-lookup"><span data-stu-id="ef7c4-130">This parameter can be set to one or a combination of the following values to specify logging or user interface options.</span></span>



| <span data-ttu-id="ef7c4-131">Флаг</span><span class="sxs-lookup"><span data-stu-id="ef7c4-131">Flag</span></span>            | <span data-ttu-id="ef7c4-132">Значение</span><span class="sxs-lookup"><span data-stu-id="ef7c4-132">Value</span></span>       | <span data-ttu-id="ef7c4-133">Значение</span><span class="sxs-lookup"><span data-stu-id="ef7c4-133">Meaning</span></span>                                  |
|-----------------|-------------|------------------------------------------|
| <span data-ttu-id="ef7c4-134">логноне</span><span class="sxs-lookup"><span data-stu-id="ef7c4-134">LOGNONE</span></span>         | <span data-ttu-id="ef7c4-135">0x00000000</span><span class="sxs-lookup"><span data-stu-id="ef7c4-135">0x00000000</span></span>  | <span data-ttu-id="ef7c4-136">В журнал не записываются сообщения.</span><span class="sxs-lookup"><span data-stu-id="ef7c4-136">Write no messages to the log.</span></span>            |
| <span data-ttu-id="ef7c4-137">LOGINFO</span><span class="sxs-lookup"><span data-stu-id="ef7c4-137">LOGINFO</span></span>         | <span data-ttu-id="ef7c4-138">0x00000001</span><span class="sxs-lookup"><span data-stu-id="ef7c4-138">0x00000001</span></span>  | <span data-ttu-id="ef7c4-139">Запись информационных сообщений в журнал.</span><span class="sxs-lookup"><span data-stu-id="ef7c4-139">Write informational messages to the log.</span></span> |
| <span data-ttu-id="ef7c4-140">логварн</span><span class="sxs-lookup"><span data-stu-id="ef7c4-140">LOGWARN</span></span>         | <span data-ttu-id="ef7c4-141">0x00000002</span><span class="sxs-lookup"><span data-stu-id="ef7c4-141">0x00000002</span></span>  | <span data-ttu-id="ef7c4-142">Запись предупреждений в журнал.</span><span class="sxs-lookup"><span data-stu-id="ef7c4-142">Write warnings to the log.</span></span>               |
| <span data-ttu-id="ef7c4-143">ложерр</span><span class="sxs-lookup"><span data-stu-id="ef7c4-143">LOGERR</span></span>          | <span data-ttu-id="ef7c4-144">0x00000004</span><span class="sxs-lookup"><span data-stu-id="ef7c4-144">0x00000004</span></span>  | <span data-ttu-id="ef7c4-145">Запись сообщений об ошибках в журнал.</span><span class="sxs-lookup"><span data-stu-id="ef7c4-145">Write error messages to the log.</span></span>         |
| <span data-ttu-id="ef7c4-146">логперфмессажес</span><span class="sxs-lookup"><span data-stu-id="ef7c4-146">LOGPERFMESSAGES</span></span> | <span data-ttu-id="ef7c4-147">0x00000008</span><span class="sxs-lookup"><span data-stu-id="ef7c4-147">0x00000008</span></span>  | <span data-ttu-id="ef7c4-148">Запись сообщений о производительности в журнал.</span><span class="sxs-lookup"><span data-stu-id="ef7c4-148">Write performance messages to the log.</span></span>   |
| <span data-ttu-id="ef7c4-149">уиноне</span><span class="sxs-lookup"><span data-stu-id="ef7c4-149">UINONE</span></span>          | <span data-ttu-id="ef7c4-150">0x00000000f</span><span class="sxs-lookup"><span data-stu-id="ef7c4-150">0x00000000f</span></span> | <span data-ttu-id="ef7c4-151">Не отображать пользовательский интерфейс.</span><span class="sxs-lookup"><span data-stu-id="ef7c4-151">Do not display the user interface.</span></span>       |
| <span data-ttu-id="ef7c4-152">уиалл</span><span class="sxs-lookup"><span data-stu-id="ef7c4-152">UIALL</span></span>           | <span data-ttu-id="ef7c4-153">0x00000010</span><span class="sxs-lookup"><span data-stu-id="ef7c4-153">0x00000010</span></span>  | <span data-ttu-id="ef7c4-154">Отображение пользовательского интерфейса.</span><span class="sxs-lookup"><span data-stu-id="ef7c4-154">Display the user interface.</span></span>              |



 

</dd> <dt>

<span data-ttu-id="ef7c4-155"><span id="dwReserved"></span><span id="dwreserved"></span><span id="DWRESERVED"></span>*двресервед*</span><span class="sxs-lookup"><span data-stu-id="ef7c4-155"><span id="dwReserved"></span><span id="dwreserved"></span><span id="DWRESERVED"></span>*dwReserved*</span></span>
</dt> <dd>

<span data-ttu-id="ef7c4-156">Зарезервировано.</span><span class="sxs-lookup"><span data-stu-id="ef7c4-156">Reserved.</span></span> <span data-ttu-id="ef7c4-157">Этот параметр должен иметь значение 0.</span><span class="sxs-lookup"><span data-stu-id="ef7c4-157">This parameter must be set to zero.</span></span>

</dd> </dl>

## <a name="return-values"></a><span data-ttu-id="ef7c4-158">Возвращаемые значения</span><span class="sxs-lookup"><span data-stu-id="ef7c4-158">Return Values</span></span>

<span data-ttu-id="ef7c4-159">См. таблицу в разделе [возвращаемые значения для уикреатепатчпаккаже](return-values-for-uicreatepatchpackage.md).</span><span class="sxs-lookup"><span data-stu-id="ef7c4-159">See the table in [Return Values for UiCreatePatchPackage](return-values-for-uicreatepatchpackage.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="ef7c4-160">Комментарии</span><span class="sxs-lookup"><span data-stu-id="ef7c4-160">Remarks</span></span>

<span data-ttu-id="ef7c4-161">Пример создания PCP-файла и использования [уикреатепатчпаккаже](uicreatepatchpackage-patchwiz-dll-.md) для создания пакета исправлений установщик Windows см. в разделе [Пример небольшого обновления исправлений](a-small-update-patching-example.md).</span><span class="sxs-lookup"><span data-stu-id="ef7c4-161">For an example of authoring a .pcp file and using [UiCreatePatchPackage](uicreatepatchpackage-patchwiz-dll-.md) to generate a Windows Installer patch package, see the section [A Small Update Patching Example](a-small-update-patching-example.md).</span></span>

<span data-ttu-id="ef7c4-162">Для создания исправления требуется несжатый образ установки, например административный образ или несжатый образ установки с компакт-диска.</span><span class="sxs-lookup"><span data-stu-id="ef7c4-162">Creating a patch requires an uncompressed setup image, such as an administrative image or an uncompressed setup image from a CD-ROM.</span></span> <span data-ttu-id="ef7c4-163">[Уикреатепатчпаккаже](uicreatepatchpackage-patchwiz-dll-.md) не создает двоичные исправления для файлов в ящиках.</span><span class="sxs-lookup"><span data-stu-id="ef7c4-163">[UiCreatePatchPackage](uicreatepatchpackage-patchwiz-dll-.md) does not generate binary patches for files in cabinets.</span></span>

 

 



