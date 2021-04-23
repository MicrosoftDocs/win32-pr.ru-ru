---
description: Рекомендуемым методом для создания пакета исправлений является использование средств создания исправлений, таких как Msimsp.exe и Patchwiz.dll. Средство Msimsp.exe доступно только в компонентах Windows SDK для разработчиков установщик Windows.
ms.assetid: fa8e9d68-3db1-4d17-aa99-2ca0ed421c7a
title: Msimsp.exe
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1810fd0c544695742273bbb0e63b22138529c129
ms.sourcegitcommit: de72a1294df274b0a71dc0fdc42d757e5f6df0f3
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/05/2021
ms.locfileid: "105674563"
---
# <a name="msimspexe"></a><span data-ttu-id="258bd-104">Msimsp.exe</span><span class="sxs-lookup"><span data-stu-id="258bd-104">Msimsp.exe</span></span>

<span data-ttu-id="258bd-105">Рекомендуемым методом для создания пакета исправлений является использование средств создания исправлений, таких как Msimsp.exe и [Patchwiz.dll](patchwiz-dll.md).</span><span class="sxs-lookup"><span data-stu-id="258bd-105">The recommended method for generating a patch package is to use patch creation tools such as Msimsp.exe and [Patchwiz.dll](patchwiz-dll.md).</span></span> <span data-ttu-id="258bd-106">Средство Msimsp.exe доступно только в [компонентах Windows SDK для разработчиков установщик Windows](platform-sdk-components-for-windows-installer-developers.md).</span><span class="sxs-lookup"><span data-stu-id="258bd-106">The Msimsp.exe tool is only available in the [Windows SDK Components for Windows Installer Developers](platform-sdk-components-for-windows-installer-developers.md).</span></span>

<span data-ttu-id="258bd-107">Msimsp.exe — это исполняемый файл, который вызывает [Patchwiz.dll](patchwiz-dll.md).</span><span class="sxs-lookup"><span data-stu-id="258bd-107">Msimsp.exe is a executable file that calls [Patchwiz.dll](patchwiz-dll.md).</span></span> <span data-ttu-id="258bd-108">Средство можно использовать для создания пакета исправлений путем передачи пути в файл свойств создания исправления (файл. PCP) и путь к создаваемому пакету исправлений.</span><span class="sxs-lookup"><span data-stu-id="258bd-108">The tool can be used to create a patch package by passing in the path to a patch creation properties file (.pcp file) and the path to the patch package that is being created.</span></span> <span data-ttu-id="258bd-109">Мсимсп. ex можно также использовать для создания файла журнала и указания временной папки, в которой сохраняются преобразования, ящики и файлы, используемые для создания пакета исправлений.</span><span class="sxs-lookup"><span data-stu-id="258bd-109">Msimsp.ex can also be used to create a log file and to specify a temporary folder in which the transforms, cabinets, and files that are used to create the patch package are saved.</span></span>

<span data-ttu-id="258bd-110">Синтаксис командной строки для Msimsp.exe:</span><span class="sxs-lookup"><span data-stu-id="258bd-110">The command-line syntax for Msimsp.exe is:</span></span>

<span data-ttu-id="258bd-111">**Msimsp.exe-s** *\[ путь \] к файлу. PCP* **-p** *\[ путь к файлу \] MSP* **{Options}**</span><span class="sxs-lookup"><span data-stu-id="258bd-111">**Msimsp.exe -s** *\[path to .pcp file\]* **-p** *\[path to .msp file\]* **{options}**</span></span>

<span data-ttu-id="258bd-112">В параметрах командной строки не учитывается регистр, а вместо тире можно использовать разделители косой черты.</span><span class="sxs-lookup"><span data-stu-id="258bd-112">The command-line options are not case-sensitive, and slash delimiters can be used instead of a dash.</span></span> <span data-ttu-id="258bd-113">Если параметры не указаны, Msimsp.exe отображает текущие значения свойств сводных данных.</span><span class="sxs-lookup"><span data-stu-id="258bd-113">If no options are specified, Msimsp.exe displays the current values of the summary Information properties.</span></span>

<dl> <dt>

<span data-ttu-id="258bd-114"><span id="-s_path_to_.pcp_file_"></span><span id="-S_PATH_TO_.PCP_FILE_"></span>**-s**_\[ путь к файлу \] . PCP_</span><span class="sxs-lookup"><span data-stu-id="258bd-114"><span id="-s_path_to_.pcp_file_"></span><span id="-S_PATH_TO_.PCP_FILE_"></span>**-s**_\[path to .pcp file\]_</span></span>
</dt> <dd>

<span data-ttu-id="258bd-115">Это обязательный параметр, за которым должен следовать путь к файлу свойств создания исправления (расширение PCP).</span><span class="sxs-lookup"><span data-stu-id="258bd-115">This is required and must be followed by the path to the patch creation properties file (.pcp extension).</span></span> <span data-ttu-id="258bd-116">Дополнительные сведения см. в разделе [PatchWiz.dll](patchwiz-dll.md).</span><span class="sxs-lookup"><span data-stu-id="258bd-116">For more information, see [PatchWiz.dll](patchwiz-dll.md).</span></span>

</dd> <dt>

<span data-ttu-id="258bd-117"><span id="-ppath_to_.msp_file"></span><span id="-PPATH_TO_.MSP_FILE"></span>**-p**_путь к MSP-файлу_</span><span class="sxs-lookup"><span data-stu-id="258bd-117"><span id="-ppath_to_.msp_file"></span><span id="-PPATH_TO_.MSP_FILE"></span>**-p**_path to .msp file_</span></span>
</dt> <dd>

<span data-ttu-id="258bd-118">Это обязательный параметр, а затем путь к создаваемому пакету исправлений (расширение MSP).</span><span class="sxs-lookup"><span data-stu-id="258bd-118">This is required and followed by the path to patch package that is being created (.msp extension).</span></span>

</dd> <dt>

<span data-ttu-id="258bd-119"><span id="-fpath_to_temporary_folder"></span><span id="-FPATH_TO_TEMPORARY_FOLDER"></span>**-f**_путь к временной папке_</span><span class="sxs-lookup"><span data-stu-id="258bd-119"><span id="-fpath_to_temporary_folder"></span><span id="-FPATH_TO_TEMPORARY_FOLDER"></span>**-f**_path to temporary folder_</span></span>
</dt> <dd>

<span data-ttu-id="258bd-120">Необязательный элемент.</span><span class="sxs-lookup"><span data-stu-id="258bd-120">Optional.</span></span> <span data-ttu-id="258bd-121">, За которым следует путь к временной папке.</span><span class="sxs-lookup"><span data-stu-id="258bd-121">Followed by path to temporary folder.</span></span> <span data-ttu-id="258bd-122">Расположение по умолчанию:% TMP% \\ ~ PCW \_ tmp. tmp \\ .</span><span class="sxs-lookup"><span data-stu-id="258bd-122">The default location is %TMP%\\~pcw\_tmp.tmp\\.</span></span>

</dd> <dt>

<span data-ttu-id="258bd-123"><span id="-k"></span><span id="-K"></span>**-k**</span><span class="sxs-lookup"><span data-stu-id="258bd-123"><span id="-k"></span><span id="-K"></span>**-k**</span></span>
</dt> <dd>

<span data-ttu-id="258bd-124">Необязательный элемент.</span><span class="sxs-lookup"><span data-stu-id="258bd-124">Optional.</span></span> <span data-ttu-id="258bd-125">Сбой, если временная папка уже существует.</span><span class="sxs-lookup"><span data-stu-id="258bd-125">Fail if the temporary folder already exists.</span></span>

</dd> <dt>

<span data-ttu-id="258bd-126"><span id="-lpath_to_log_file"></span><span id="-LPATH_TO_LOG_FILE"></span>**-l**_путь к файлу журнала_</span><span class="sxs-lookup"><span data-stu-id="258bd-126"><span id="-lpath_to_log_file"></span><span id="-LPATH_TO_LOG_FILE"></span>**-l**_path to log file_</span></span>
</dt> <dd>

<span data-ttu-id="258bd-127">Необязательный элемент.</span><span class="sxs-lookup"><span data-stu-id="258bd-127">Optional.</span></span> <span data-ttu-id="258bd-128">, За которым следует путь к файлу журнала, описывающий процесс создания исправления и ошибки.</span><span class="sxs-lookup"><span data-stu-id="258bd-128">Followed by the path to the log file that describes the patch creation process and errors.</span></span> <span data-ttu-id="258bd-129">Дополнительные сведения см. в разделе [возвращаемые значения для уикреатепатчпаккаже](return-values-for-uicreatepatchpackage.md).</span><span class="sxs-lookup"><span data-stu-id="258bd-129">For more information, see [Return Values for UiCreatePatchPackage](return-values-for-uicreatepatchpackage.md).</span></span>

</dd> <dt>

<span data-ttu-id="258bd-130"><span id="-lppath_to_log_file_with_performance_data"></span><span id="-LPPATH_TO_LOG_FILE_WITH_PERFORMANCE_DATA"></span>**-LP**_путь к файлу журнала с данными о производительности_</span><span class="sxs-lookup"><span data-stu-id="258bd-130"><span id="-lppath_to_log_file_with_performance_data"></span><span id="-LPPATH_TO_LOG_FILE_WITH_PERFORMANCE_DATA"></span>**-lp**_path to log file with performance data_</span></span>
</dt> <dd>

<span data-ttu-id="258bd-131">Необязательный элемент.</span><span class="sxs-lookup"><span data-stu-id="258bd-131">Optional.</span></span> <span data-ttu-id="258bd-132">, За которым следует путь к файлу журнала, описывающий процесс создания исправления и ошибки.</span><span class="sxs-lookup"><span data-stu-id="258bd-132">Followed by the path to the log file that describes the patch creation process and errors.</span></span> <span data-ttu-id="258bd-133">Этот параметр записывает данные о производительности в файл журнала.</span><span class="sxs-lookup"><span data-stu-id="258bd-133">This option writes performance data to log file.</span></span> <span data-ttu-id="258bd-134">Для этого параметра требуется версия 4,0 Patchwiz.dll.</span><span class="sxs-lookup"><span data-stu-id="258bd-134">This option requires version 4.0 of Patchwiz.dll.</span></span>

</dd> <dt>

<span data-ttu-id="258bd-135"><span id="-d"></span><span id="-D"></span>**-d**</span><span class="sxs-lookup"><span data-stu-id="258bd-135"><span id="-d"></span><span id="-D"></span>**-d**</span></span>
</dt> <dd>

<span data-ttu-id="258bd-136">Необязательный элемент.</span><span class="sxs-lookup"><span data-stu-id="258bd-136">Optional.</span></span> <span data-ttu-id="258bd-137">Отображает диалоговое окно при успешном завершении создания исправления.</span><span class="sxs-lookup"><span data-stu-id="258bd-137">Displays a dialog if the patch creation completes successfully.</span></span>

</dd> <dt>

<span data-ttu-id="258bd-138"><span id="-_"></span>**-?**</span><span class="sxs-lookup"><span data-stu-id="258bd-138"><span id="-_"></span>**-?**</span></span>
</dt> <dd>

<span data-ttu-id="258bd-139">Отображает справку по командной строке.</span><span class="sxs-lookup"><span data-stu-id="258bd-139">Displays command-line help.</span></span>

</dd> </dl>

> [!Note]
> <span data-ttu-id="258bd-140">Msimsp.exe может завершиться ошибкой при вызове Makecab.exe, если в столбце file [таблицы File](file-table.md) пакета установки различаются только регистр.</span><span class="sxs-lookup"><span data-stu-id="258bd-140">Msimsp.exe can fail when it calls Makecab.exe if there are values in the File column of the [File table](file-table.md) of the installation package that differ only by case.</span></span> <span data-ttu-id="258bd-141">Установщик Windows учитывает регистр и разрешает пакет установки, например в таблице ниже, только если comp1 и Comp2 установлены в разные каталоги.</span><span class="sxs-lookup"><span data-stu-id="258bd-141">Windows Installer is case-sensitive and allows an installation package such as in the table below only when Comp1 and Comp2 are installed into different directories.</span></span> <span data-ttu-id="258bd-142">Однако в этом сценарии нельзя использовать Msimsp.exe или [Patchwiz.dll](patchwiz-dll.md) для создания исправления пакета, так как Msimsp.exe и Patchwiz.dll вызывают Makecab.exe, который не учитывает регистр.</span><span class="sxs-lookup"><span data-stu-id="258bd-142">However, in this scenario you cannot use Msimsp.exe or [Patchwiz.dll](patchwiz-dll.md) to generate a patch for the package, because Msimsp.exe and Patchwiz.dll call Makecab.exe, which is case-insensitive.</span></span>
> 
> <span data-ttu-id="258bd-143">Избегайте создания пакета установки, такого как Следующая частичная [таблица файлов](file-table.md).</span><span class="sxs-lookup"><span data-stu-id="258bd-143">Avoid authoring an installation package such as the following partial [File table](file-table.md).</span></span>
> 
> | <span data-ttu-id="258bd-144">Файл</span><span class="sxs-lookup"><span data-stu-id="258bd-144">File</span></span>       | <span data-ttu-id="258bd-145">Компонент\_</span><span class="sxs-lookup"><span data-stu-id="258bd-145">Component\_</span></span> | <span data-ttu-id="258bd-146">FileName</span><span class="sxs-lookup"><span data-stu-id="258bd-146">FileName</span></span>   |
> |------------|-------------|------------|
> | <span data-ttu-id="258bd-147">readMe.txt</span><span class="sxs-lookup"><span data-stu-id="258bd-147">readme.txt</span></span> | <span data-ttu-id="258bd-148">Comp1</span><span class="sxs-lookup"><span data-stu-id="258bd-148">Comp1</span></span>       | <span data-ttu-id="258bd-149">readMe.txt</span><span class="sxs-lookup"><span data-stu-id="258bd-149">readme.txt</span></span> |
> | <span data-ttu-id="258bd-150">ReadMe.txt</span><span class="sxs-lookup"><span data-stu-id="258bd-150">ReadMe.txt</span></span> | <span data-ttu-id="258bd-151">Comp2</span><span class="sxs-lookup"><span data-stu-id="258bd-151">Comp2</span></span>       | <span data-ttu-id="258bd-152">readMe.txt</span><span class="sxs-lookup"><span data-stu-id="258bd-152">readme.txt</span></span> |


## <a name="related-topics"></a><span data-ttu-id="258bd-153">См. также</span><span class="sxs-lookup"><span data-stu-id="258bd-153">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="258bd-154">Создание пакета исправлений</span><span class="sxs-lookup"><span data-stu-id="258bd-154">Creating a Patch Package</span></span>](creating-a-patch-package.md)
</dt> <dt>

[<span data-ttu-id="258bd-155">Пример небольшого обновления исправлений</span><span class="sxs-lookup"><span data-stu-id="258bd-155">A Small Update Patching Example</span></span>](a-small-update-patching-example.md)
</dt> <dt>

[<span data-ttu-id="258bd-156">Средства разработки установщик Windows</span><span class="sxs-lookup"><span data-stu-id="258bd-156">Windows Installer Development Tools</span></span>](windows-installer-development-tools.md)
</dt> <dt>

[<span data-ttu-id="258bd-157">Выпущенные версии, средства и распространяемые пакеты</span><span class="sxs-lookup"><span data-stu-id="258bd-157">Released Versions, Tools, and Redistributables</span></span>](released-versions-tools-and-redistributables.md)
</dt> </dl>

 

 



