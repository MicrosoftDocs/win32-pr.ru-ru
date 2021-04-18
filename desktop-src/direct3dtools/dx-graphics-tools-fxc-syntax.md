---
title: Синтаксис
description: Ниже приведен синтаксис вызова FXC.exe, средства-компилятора Effect. Пример см. в разделе автономная компиляция.
ms.assetid: 3aee89bd-02e1-4de1-8552-ba36814f8464
keywords:
- fxc, синтаксис
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6241a728b4835b11d10ea6e39d67fd73a8576cd7
ms.sourcegitcommit: ae73f4dd3cf5a3c6a1ea7d191ca32a5b01f6686b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/08/2020
ms.locfileid: "105691692"
---
# <a name="syntax"></a><span data-ttu-id="9e5e0-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="9e5e0-105">Syntax</span></span>

<span data-ttu-id="9e5e0-106">Ниже приведен синтаксис вызова FXC.exe, средства-компилятора Effect.</span><span class="sxs-lookup"><span data-stu-id="9e5e0-106">Here is the syntax for calling FXC.exe, the effect-compiler tool.</span></span> <span data-ttu-id="9e5e0-107">Пример см. в разделе [Автономная компиляция](dx-graphics-tools-fxc-using.md).</span><span class="sxs-lookup"><span data-stu-id="9e5e0-107">For an example, see [Offline Compiling](dx-graphics-tools-fxc-using.md).</span></span>

-   [<span data-ttu-id="9e5e0-108">Использование</span><span class="sxs-lookup"><span data-stu-id="9e5e0-108">Usage</span></span>](#usage)
-   [<span data-ttu-id="9e5e0-109">Аргументы</span><span class="sxs-lookup"><span data-stu-id="9e5e0-109">Arguments</span></span>](#arguments)
-   [<span data-ttu-id="9e5e0-110">Замечания</span><span class="sxs-lookup"><span data-stu-id="9e5e0-110">Remarks</span></span>](#remarks)
-   [<span data-ttu-id="9e5e0-111">Профили</span><span class="sxs-lookup"><span data-stu-id="9e5e0-111">Profiles</span></span>](#profiles)
-   [<span data-ttu-id="9e5e0-112">Заметки о версии</span><span class="sxs-lookup"><span data-stu-id="9e5e0-112">Version notes</span></span>](#version-notes)
-   [<span data-ttu-id="9e5e0-113">См. также</span><span class="sxs-lookup"><span data-stu-id="9e5e0-113">Related topics</span></span>](#related-topics)

## <a name="usage"></a><span data-ttu-id="9e5e0-114">Использование</span><span class="sxs-lookup"><span data-stu-id="9e5e0-114">Usage</span></span>

<span data-ttu-id="9e5e0-115">**fxc** *свитчоптионс* *имена файлов*</span><span class="sxs-lookup"><span data-stu-id="9e5e0-115">**fxc** *SwitchOptions* *Filenames*</span></span>

## <a name="arguments"></a><span data-ttu-id="9e5e0-116">Аргументы</span><span class="sxs-lookup"><span data-stu-id="9e5e0-116">Arguments</span></span>
<span data-ttu-id="9e5e0-117">Разделите каждый параметр Switch с пробелом или двоеточием.</span><span class="sxs-lookup"><span data-stu-id="9e5e0-117">Separate each switch option with a space or a colon.</span></span>

### <a name="switchoptions"></a><span data-ttu-id="9e5e0-118">*свитчоптионс*</span><span class="sxs-lookup"><span data-stu-id="9e5e0-118">*SwitchOptions*</span></span>
<span data-ttu-id="9e5e0-119">\[в \] параметрах компиляции.</span><span class="sxs-lookup"><span data-stu-id="9e5e0-119">\[in\] Compile options.</span></span> <span data-ttu-id="9e5e0-120">Существует только один обязательный параметр, и многие другие являются необязательными.</span><span class="sxs-lookup"><span data-stu-id="9e5e0-120">There is just one required option, and many more that are optional.</span></span> <span data-ttu-id="9e5e0-121">Разделяйте их пробелами или двоеточиями.</span><span class="sxs-lookup"><span data-stu-id="9e5e0-121">Separate each with a space or colon.</span></span>

#### <a name="required-option"></a><span data-ttu-id="9e5e0-122">Обязательный параметр</span><span class="sxs-lookup"><span data-stu-id="9e5e0-122">Required option</span></span>
##### <a name="t-profile"></a><span data-ttu-id="9e5e0-123">/T <*профиль*></span><span class="sxs-lookup"><span data-stu-id="9e5e0-123">/T <*profile*></span></span>
<span data-ttu-id="9e5e0-124">Модель шейдера (см. [Профили](#profiles)).</span><span class="sxs-lookup"><span data-stu-id="9e5e0-124">Shader model (see [Profiles](#profiles)).</span></span>

#### <a name="optional-options"></a><span data-ttu-id="9e5e0-125">Необязательные параметры</span><span class="sxs-lookup"><span data-stu-id="9e5e0-125">Optional options</span></span>
##### <a name="-help"></a><span data-ttu-id="9e5e0-126">/?, /help</span><span class="sxs-lookup"><span data-stu-id="9e5e0-126">/?, /help</span></span>
<span data-ttu-id="9e5e0-127">Печать справки для `FXC.exe` .</span><span class="sxs-lookup"><span data-stu-id="9e5e0-127">Print help for `FXC.exe`.</span></span>

##### <a name="commandoptionfile"></a><span data-ttu-id="9e5e0-128">@<*Command. параметр. File*></span><span class="sxs-lookup"><span data-stu-id="9e5e0-128">@<*command.option.file*></span></span>
<span data-ttu-id="9e5e0-129">Файл, содержащий дополнительные параметры компиляции.</span><span class="sxs-lookup"><span data-stu-id="9e5e0-129">File that contains additional compile options.</span></span> <span data-ttu-id="9e5e0-130">Этот параметр можно использовать совместно с другими параметрами компиляции командной строки.</span><span class="sxs-lookup"><span data-stu-id="9e5e0-130">This option can be mixed with other command line compile options.</span></span> <span data-ttu-id="9e5e0-131">*Команда. параметр. File* должна содержать только один параметр в строке.</span><span class="sxs-lookup"><span data-stu-id="9e5e0-131">The *command.option.file* must contain only one option per line.</span></span> <span data-ttu-id="9e5e0-132">*Команда. параметр. File* не может содержать пустые строки.</span><span class="sxs-lookup"><span data-stu-id="9e5e0-132">The *command.option.file* cannot contain any blank lines.</span></span> <span data-ttu-id="9e5e0-133">Параметры, указанные в файле, не должны содержать начальных и конечных пробелов.</span><span class="sxs-lookup"><span data-stu-id="9e5e0-133">Options specified in the file must not contain any leading or trailing spaces.</span></span>

##### <a name="all_resources_bound"></a><span data-ttu-id="9e5e0-134">/all_resources_bound</span><span class="sxs-lookup"><span data-stu-id="9e5e0-134">/all_resources_bound</span></span>
<span data-ttu-id="9e5e0-135">Включить агрессивное сведение в SM 5.1 +.</span><span class="sxs-lookup"><span data-stu-id="9e5e0-135">Enable aggressive flattening in SM5.1+.</span></span> <span data-ttu-id="9e5e0-136">Новое для Direct3D 12.</span><span class="sxs-lookup"><span data-stu-id="9e5e0-136">New for Direct3D 12.</span></span>

##### <a name="cc"></a><span data-ttu-id="9e5e0-137">/CC</span><span class="sxs-lookup"><span data-stu-id="9e5e0-137">/Cc</span></span>
<span data-ttu-id="9e5e0-138">Выходная цветовая кодировка сборки.</span><span class="sxs-lookup"><span data-stu-id="9e5e0-138">Output color-coded assembly.</span></span>

##### <a name="compress"></a><span data-ttu-id="9e5e0-139">/compress</span><span class="sxs-lookup"><span data-stu-id="9e5e0-139">/compress</span></span>
<span data-ttu-id="9e5e0-140">Сжимать байты СОДЕРЖИМЫМ DX10 шейдера из файлов.</span><span class="sxs-lookup"><span data-stu-id="9e5e0-140">Compress DX10 shader bytecode from files.</span></span>

##### <a name="d-idtext"></a><span data-ttu-id="9e5e0-141">/D < >=< *текст* идентификатора></span><span class="sxs-lookup"><span data-stu-id="9e5e0-141">/D <*id*>=<*text*></span></span>
<span data-ttu-id="9e5e0-142">Определить макрос.</span><span class="sxs-lookup"><span data-stu-id="9e5e0-142">Define macro.</span></span>

##### <a name="decompress"></a><span data-ttu-id="9e5e0-143">/декомпресс</span><span class="sxs-lookup"><span data-stu-id="9e5e0-143">/decompress</span></span>
<span data-ttu-id="9e5e0-144">Распаковать байтовый код шейдера СОДЕРЖИМЫМ DX10 из первого файла.</span><span class="sxs-lookup"><span data-stu-id="9e5e0-144">Decompress DX10 shader bytecode from first file.</span></span> <span data-ttu-id="9e5e0-145">Выходные файлы должны быть перечислены в том порядке, в котором они были в процессе сжатия.</span><span class="sxs-lookup"><span data-stu-id="9e5e0-145">Output files should be listed in the order they were in during compression.</span></span>

##### <a name="dumpbin"></a><span data-ttu-id="9e5e0-146">/думпбин</span><span class="sxs-lookup"><span data-stu-id="9e5e0-146">/dumpbin</span></span>
<span data-ttu-id="9e5e0-147">Загружает двоичный файл, а не компилирует шейдер.</span><span class="sxs-lookup"><span data-stu-id="9e5e0-147">Loads a binary file rather than compiling a shader.</span></span>

##### <a name="e-name"></a><span data-ttu-id="9e5e0-148">/E <name></span><span class="sxs-lookup"><span data-stu-id="9e5e0-148">/E <name></span></span>
<span data-ttu-id="9e5e0-149">Точка входа шейдера.</span><span class="sxs-lookup"><span data-stu-id="9e5e0-149">Shader entry point.</span></span> <span data-ttu-id="9e5e0-150">Если точка входа не указана, **основным** считается именем записи шейдера.</span><span class="sxs-lookup"><span data-stu-id="9e5e0-150">If no entry point is given, **main** is considered to be the shader entry name.</span></span>

##### <a name="enable_unbounded_descriptor_tables"></a><span data-ttu-id="9e5e0-151">/enable_unbounded_descriptor_tables</span><span class="sxs-lookup"><span data-stu-id="9e5e0-151">/enable_unbounded_descriptor_tables</span></span>
<span data-ttu-id="9e5e0-152">Включает неограниченные таблицы дескрипторов.</span><span class="sxs-lookup"><span data-stu-id="9e5e0-152">Enables unbounded descriptor tables.</span></span> <span data-ttu-id="9e5e0-153">Новое для Direct3D 12.</span><span class="sxs-lookup"><span data-stu-id="9e5e0-153">New for Direct3D 12.</span></span>

##### <a name="extractrootsignature-file"></a><span data-ttu-id="9e5e0-154">*файл* </екстрактрутсигнатуре></span><span class="sxs-lookup"><span data-stu-id="9e5e0-154">/extractrootsignature <*file*></span></span>
<span data-ttu-id="9e5e0-155">Извлечение корневой сигнатуры из байтового кода шейдера.</span><span class="sxs-lookup"><span data-stu-id="9e5e0-155">Extract root signature from shader bytecode.</span></span> <span data-ttu-id="9e5e0-156">Новое для Direct3D 12.</span><span class="sxs-lookup"><span data-stu-id="9e5e0-156">New for Direct3D 12.</span></span>

##### <a name="fc-file"></a><span data-ttu-id="9e5e0-157">*Файл* </FC></span><span class="sxs-lookup"><span data-stu-id="9e5e0-157">/Fc <*file*></span></span>
<span data-ttu-id="9e5e0-158">Выходной файл листинга кода сборки.</span><span class="sxs-lookup"><span data-stu-id="9e5e0-158">Output assembly code listing file.</span></span>

##### <a name="fd-file"></a><span data-ttu-id="9e5e0-159">/FD <*файл*></span><span class="sxs-lookup"><span data-stu-id="9e5e0-159">/Fd <*file*></span></span>
<span data-ttu-id="9e5e0-160">Извлечение сведений о базе данных программы шейдера (PDB) и запись в заданный файл. При компиляции шейдера используйте параметр/FD для создания PDB-файла с отладочными сведениями шейдера.</span><span class="sxs-lookup"><span data-stu-id="9e5e0-160">Extract shader program database (PDB) info and write to the given file.When you compile the shader, use /Fd to generate a PDB file with shader debugging info.</span></span>

##### <a name="fe-file"></a><span data-ttu-id="9e5e0-161">*Файл* </Fe></span><span class="sxs-lookup"><span data-stu-id="9e5e0-161">/Fe <*file*></span></span>
<span data-ttu-id="9e5e0-162">Выводить предупреждения и ошибки в заданный файл.</span><span class="sxs-lookup"><span data-stu-id="9e5e0-162">Output warnings and errors to the given file.</span></span>

##### <a name="fh-file"></a><span data-ttu-id="9e5e0-163">*Файл* </ФХ></span><span class="sxs-lookup"><span data-stu-id="9e5e0-163">/Fh <*file*></span></span>
<span data-ttu-id="9e5e0-164">Выходной файл заголовка, содержащий объектный код.</span><span class="sxs-lookup"><span data-stu-id="9e5e0-164">Output header file containing object code.</span></span>

##### <a name="fl-file"></a><span data-ttu-id="9e5e0-165">*Файл* </ФЛ</span><span class="sxs-lookup"><span data-stu-id="9e5e0-165">/Fl <*file*</span></span>
<span data-ttu-id="9e5e0-166">Вывод библиотеки.</span><span class="sxs-lookup"><span data-stu-id="9e5e0-166">Output a library.</span></span> <span data-ttu-id="9e5e0-167">Требуется D3dcompiler \_47.dll или более поздней версии библиотеки DLL.</span><span class="sxs-lookup"><span data-stu-id="9e5e0-167">Requires the D3dcompiler\_47.dll or a later version of the DLL.</span></span>

##### <a name="fo-file"></a><span data-ttu-id="9e5e0-168">/FO <*файл*></span><span class="sxs-lookup"><span data-stu-id="9e5e0-168">/Fo <*file*></span></span>
<span data-ttu-id="9e5e0-169">Выходной файл объекта.</span><span class="sxs-lookup"><span data-stu-id="9e5e0-169">Output object file.</span></span> <span data-ttu-id="9e5e0-170">Часто получается расширение &quot; . fxc &quot; , хотя используются другие расширения, такие как &quot; . o &quot; , &quot; . obj &quot; или &quot; . dxbc &quot; .</span><span class="sxs-lookup"><span data-stu-id="9e5e0-170">Often given the extension &quot;.fxc&quot;, though other extensions are used, such as &quot;.o&quot;, &quot;.obj&quot; or &quot;.dxbc&quot;.</span></span>

##### <a name="fx-file"></a><span data-ttu-id="9e5e0-171">*Файл* </FX></span><span class="sxs-lookup"><span data-stu-id="9e5e0-171">/Fx <*file*></span></span>
<span data-ttu-id="9e5e0-172">Выходной код сборки и шестнадцатеричный файл листинга.</span><span class="sxs-lookup"><span data-stu-id="9e5e0-172">Output assembly code and hex listing file.</span></span>

##### <a name="gch"></a><span data-ttu-id="9e5e0-173">/гч</span><span class="sxs-lookup"><span data-stu-id="9e5e0-173">/Gch</span></span>
<span data-ttu-id="9e5e0-174">Компилировать как дочерний результат для профилей fx_4_x.</span><span class="sxs-lookup"><span data-stu-id="9e5e0-174">Compile as a child effect for fx_4_x profiles.</span></span>

> [!NOTE]
> <span data-ttu-id="9e5e0-175">Поддержка профилей устаревших эффектов устарела.</span><span class="sxs-lookup"><span data-stu-id="9e5e0-175">Support for legacy Effects profiles is deprecated.</span></span>

##### <a name="gdp"></a><span data-ttu-id="9e5e0-176">/гдп</span><span class="sxs-lookup"><span data-stu-id="9e5e0-176">/Gdp</span></span>
<span data-ttu-id="9e5e0-177">Отключить режим производительности влияния.</span><span class="sxs-lookup"><span data-stu-id="9e5e0-177">Disable effect performance mode.</span></span>

##### <a name="gec"></a><span data-ttu-id="9e5e0-178">/жек</span><span class="sxs-lookup"><span data-stu-id="9e5e0-178">/Gec</span></span>
<span data-ttu-id="9e5e0-179">Включить режим обратной совместимости.</span><span class="sxs-lookup"><span data-stu-id="9e5e0-179">Enable backward compatibility mode.</span></span>

##### <a name="ges"></a><span data-ttu-id="9e5e0-180">/жес</span><span class="sxs-lookup"><span data-stu-id="9e5e0-180">/Ges</span></span>
<span data-ttu-id="9e5e0-181">Включить режим "в режиме".</span><span class="sxs-lookup"><span data-stu-id="9e5e0-181">Enable strict mode.</span></span>

##### <a name="getprivate-file"></a><span data-ttu-id="9e5e0-182">*файл* </жетпривате></span><span class="sxs-lookup"><span data-stu-id="9e5e0-182">/getprivate <*file*></span></span>
<span data-ttu-id="9e5e0-183">Сохранение закрытых данных из большого двоичного объекта шейдера (скомпилированного двоичного шейдера) в заданный файл.</span><span class="sxs-lookup"><span data-stu-id="9e5e0-183">Save private data from the shader blob (compiled shader binary) to the given file.</span></span> <span data-ttu-id="9e5e0-184">Извлекает из большого двоичного объекта шейдера закрытые данные, ранее внедренные с помощью/сетпривате.</span><span class="sxs-lookup"><span data-stu-id="9e5e0-184">Extracts private data, previously embedded by /setprivate, from the shader blob.</span></span>

<span data-ttu-id="9e5e0-185">Необходимо указать параметр/думпбин с/жетпривате.</span><span class="sxs-lookup"><span data-stu-id="9e5e0-185">You must specify the /dumpbin option with /getprivate.</span></span> <span data-ttu-id="9e5e0-186">Пример:</span><span class="sxs-lookup"><span data-stu-id="9e5e0-186">For example:</span></span>

```console
fxc /getprivate ps01.private.data 
    /dumpbin ps01.with.private.obj
```
    
##### <a name="gfa"></a><span data-ttu-id="9e5e0-187">/гфа</span><span class="sxs-lookup"><span data-stu-id="9e5e0-187">/Gfa</span></span>
<span data-ttu-id="9e5e0-188">Избегайте конструкций управления потоком.</span><span class="sxs-lookup"><span data-stu-id="9e5e0-188">Avoid flow control constructs.</span></span>

##### <a name="gfp"></a><span data-ttu-id="9e5e0-189">/GFP</span><span class="sxs-lookup"><span data-stu-id="9e5e0-189">/Gfp</span></span>
<span data-ttu-id="9e5e0-190">Предпочитать конструкции управления потоком.</span><span class="sxs-lookup"><span data-stu-id="9e5e0-190">Prefer flow control constructs.</span></span>

##### <a name="gis"></a><span data-ttu-id="9e5e0-191">/гис</span><span class="sxs-lookup"><span data-stu-id="9e5e0-191">/Gis</span></span>
<span data-ttu-id="9e5e0-192">Принудительно использовать IEEE.</span><span class="sxs-lookup"><span data-stu-id="9e5e0-192">Force IEEE strictness.</span></span>

##### <a name="gpp"></a><span data-ttu-id="9e5e0-193">/гпп</span><span class="sxs-lookup"><span data-stu-id="9e5e0-193">/Gpp</span></span>
<span data-ttu-id="9e5e0-194">Принудительная частичная точность.</span><span class="sxs-lookup"><span data-stu-id="9e5e0-194">Force partial precision.</span></span>
    
##### <a name="i-include"></a><span data-ttu-id="9e5e0-195">/I <*включить*></span><span class="sxs-lookup"><span data-stu-id="9e5e0-195">/I <*include*></span></span>
<span data-ttu-id="9e5e0-196">Дополнительный путь включения.</span><span class="sxs-lookup"><span data-stu-id="9e5e0-196">Additional include path.</span></span>

##### <a name="lx"></a><span data-ttu-id="9e5e0-197">/лкс</span><span class="sxs-lookup"><span data-stu-id="9e5e0-197">/Lx</span></span>
<span data-ttu-id="9e5e0-198">Выходные шестнадцатеричные литералы.</span><span class="sxs-lookup"><span data-stu-id="9e5e0-198">Output hexadecimal literals.</span></span> <span data-ttu-id="9e5e0-199">Требуется D3dcompiler \_47.dll или более поздней версии библиотеки DLL.</span><span class="sxs-lookup"><span data-stu-id="9e5e0-199">Requires the D3dcompiler\_47.dll or a later version of the DLL.</span></span>

##### <a name="matchuavs"></a><span data-ttu-id="9e5e0-200">/матчуавс</span><span class="sxs-lookup"><span data-stu-id="9e5e0-200">/matchUAVs</span></span>
<span data-ttu-id="9e5e0-201">Соответствие выделениям слотов UAVа шаблона в текущем шейдере.</span><span class="sxs-lookup"><span data-stu-id="9e5e0-201">Match template shader UAV slot allocations in the current shader.</span></span> <span data-ttu-id="9e5e0-202">Дополнительные сведения см. в разделе <a href="#remarks">Примечания</a>.</span><span class="sxs-lookup"><span data-stu-id="9e5e0-202">For more info, see <a href="#remarks">Remarks</a>.</span></span>

##### <a name="mergeuavs"></a><span data-ttu-id="9e5e0-203">/мержеуавс</span><span class="sxs-lookup"><span data-stu-id="9e5e0-203">/mergeUAVs</span></span>
<span data-ttu-id="9e5e0-204">Слияние выделения слота UAV для шаблона шейдера и текущего шейдера.</span><span class="sxs-lookup"><span data-stu-id="9e5e0-204">Merge UAV slot allocations of template shader and the current shader.</span></span> <span data-ttu-id="9e5e0-205">Дополнительные сведения см. в разделе <a href=""></a> <a href="#remarks">Примечания</a>.</span><span class="sxs-lookup"><span data-stu-id="9e5e0-205">For more info, see <a href=""></a><a href="#remarks">Remarks</a>.</span></span>

##### <a name="ni"></a><span data-ttu-id="9e5e0-206">/ни</span><span class="sxs-lookup"><span data-stu-id="9e5e0-206">/Ni</span></span>
<span data-ttu-id="9e5e0-207">Выходные номера инструкций в листингах сборок.</span><span class="sxs-lookup"><span data-stu-id="9e5e0-207">Output instruction numbers in assembly listings.</span></span>

##### <a name="no"></a><span data-ttu-id="9e5e0-208">/но</span><span class="sxs-lookup"><span data-stu-id="9e5e0-208">/No</span></span>
<span data-ttu-id="9e5e0-209">Смещение в байтах для инструкций вывода в листингах сборок.</span><span class="sxs-lookup"><span data-stu-id="9e5e0-209">Output instruction byte offset in assembly listings.</span></span> <span data-ttu-id="9e5e0-210">При создании сборки используйте/но, чтобы добавить к ней смещение в байтах для каждой инструкции.</span><span class="sxs-lookup"><span data-stu-id="9e5e0-210">When you produce assembly, use /No to annotate it with the byte offset for each instruction.</span></span>

##### <a name="nologo"></a><span data-ttu-id="9e5e0-211">/nologo</span><span class="sxs-lookup"><span data-stu-id="9e5e0-211">/nologo</span></span>
<span data-ttu-id="9e5e0-212">Позволяет запретить вывод сообщения об авторских правах.</span><span class="sxs-lookup"><span data-stu-id="9e5e0-212">Suppress copyright message.</span></span>

##### <a name="od"></a><span data-ttu-id="9e5e0-213">/Od</span><span class="sxs-lookup"><span data-stu-id="9e5e0-213">/Od</span></span>
<span data-ttu-id="9e5e0-214">Отключает оптимизацию.</span><span class="sxs-lookup"><span data-stu-id="9e5e0-214">Disable optimizations.</span></span> <span data-ttu-id="9e5e0-215">/OD подразумевает/GFP, хотя вывод может не совпадать с/OD/ГФП.</span><span class="sxs-lookup"><span data-stu-id="9e5e0-215">/Od implies /Gfp, though output may not be identical to /Od /Gfp.</span></span>

##### <a name="op"></a><span data-ttu-id="9e5e0-216">/Op</span><span class="sxs-lookup"><span data-stu-id="9e5e0-216">/Op</span></span>
<span data-ttu-id="9e5e0-217">Отключить предшейдеры (не рекомендуется).</span><span class="sxs-lookup"><span data-stu-id="9e5e0-217">Disable preshaders (deprecated).</span></span>

##### <a name="o0-o1-o2-o3"></a><span data-ttu-id="9e5e0-218">/O0/O1,/O2,/O3</span><span class="sxs-lookup"><span data-stu-id="9e5e0-218">/O0 /O1, /O2, /O3</span></span>
<span data-ttu-id="9e5e0-219">Уровни оптимизации.</span><span class="sxs-lookup"><span data-stu-id="9e5e0-219">Optimization levels.</span></span> <span data-ttu-id="9e5e0-220">Параметр o1 используется по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="9e5e0-220">O1 is the default setting.</span></span>
- <span data-ttu-id="9e5e0-221">O0 — отключает изменение порядка команд.</span><span class="sxs-lookup"><span data-stu-id="9e5e0-221">O0 - Disables instruction reordering.</span></span> <span data-ttu-id="9e5e0-222">Это помогает сократить нагрузку при регистрации и обеспечивает более быстрое моделирование цикла.</span><span class="sxs-lookup"><span data-stu-id="9e5e0-222">This helps reduce register load and enables faster loop simulation.</span></span>
- <span data-ttu-id="9e5e0-223">O1 — отключает изменение порядка команд для ps_3_0 и выше.</span><span class="sxs-lookup"><span data-stu-id="9e5e0-223">O1 - Disables instruction reordering for ps_3_0 and up.</span></span>
- <span data-ttu-id="9e5e0-224">O2 — то же, что и O1.</span><span class="sxs-lookup"><span data-stu-id="9e5e0-224">O2 - Same as O1.</span></span> <span data-ttu-id="9e5e0-225">Зарезервировано для последующего использования.</span><span class="sxs-lookup"><span data-stu-id="9e5e0-225">Reserved for future use.</span></span>
- <span data-ttu-id="9e5e0-226">O3 — то же, что и O1.</span><span class="sxs-lookup"><span data-stu-id="9e5e0-226">O3 - Same as O1.</span></span> <span data-ttu-id="9e5e0-227">Зарезервировано для последующего использования.</span><span class="sxs-lookup"><span data-stu-id="9e5e0-227">Reserved for future use.</span></span>

##### <a name="p-file"></a><span data-ttu-id="9e5e0-228">/P <*файл*></span><span class="sxs-lookup"><span data-stu-id="9e5e0-228">/P <*file*></span></span>
<span data-ttu-id="9e5e0-229">Предварительная обработка в файле (должна использоваться отдельно).</span><span class="sxs-lookup"><span data-stu-id="9e5e0-229">Preprocess to file (must be used alone).</span></span>

##### <a name="qstrip_debug"></a><span data-ttu-id="9e5e0-230">/Qstrip_debug</span><span class="sxs-lookup"><span data-stu-id="9e5e0-230">/Qstrip_debug</span></span>
<span data-ttu-id="9e5e0-231">Удалить отладочные данные из байтового кода шейдера для профилей 4_0 и.</span><span class="sxs-lookup"><span data-stu-id="9e5e0-231">Strip debug data from shader bytecode for 4_0+ profiles.</span></span>

##### <a name="qstrip_priv"></a><span data-ttu-id="9e5e0-232">/Qstrip_priv</span><span class="sxs-lookup"><span data-stu-id="9e5e0-232">/Qstrip_priv</span></span>
<span data-ttu-id="9e5e0-233">Удалите закрытые данные из байтового кода шейдера 4_0 +.</span><span class="sxs-lookup"><span data-stu-id="9e5e0-233">Strip the private data from 4_0+ shader bytecode.</span></span> <span data-ttu-id="9e5e0-234">Удаляет закрытые данные (произвольную последовательность байтов) из большого двоичного объекта шейдера (скомпилированного двоичного шейдера), внедренного ранее с `/setprivate <file>` параметром.</span><span class="sxs-lookup"><span data-stu-id="9e5e0-234">Removes private data (arbitrary sequence of bytes) from the shader blob (compiled shader binary) that you previously embedded with the `/setprivate <file>` option.</span></span>

<span data-ttu-id="9e5e0-235">Необходимо указать параметр/думпбин с/Qstrip_priv.</span><span class="sxs-lookup"><span data-stu-id="9e5e0-235">You must specify the /dumpbin option with /Qstrip_priv.</span></span> <span data-ttu-id="9e5e0-236">Пример:</span><span class="sxs-lookup"><span data-stu-id="9e5e0-236">For example:</span></span>

```console
fxc /Qstrip_priv /dumpbin /Fo ps01.no.private.obj 
    ps01.with.private.obj
```

##### <a name="qstrip_reflect"></a><span data-ttu-id="9e5e0-237">/Qstrip_reflect</span><span class="sxs-lookup"><span data-stu-id="9e5e0-237">/Qstrip_reflect</span></span>
<span data-ttu-id="9e5e0-238">Чередование данных отражения из байтового кода шейдера для профилей 4_0 и.</span><span class="sxs-lookup"><span data-stu-id="9e5e0-238">Strip reflection data from shader bytecode for 4_0+ profiles.</span></span>

##### <a name="qstrip_rootsignature"></a><span data-ttu-id="9e5e0-239">/Qstrip_rootsignature</span><span class="sxs-lookup"><span data-stu-id="9e5e0-239">/Qstrip_rootsignature</span></span>
<span data-ttu-id="9e5e0-240">Удалить корневую подпись из байтового кода шейдера.</span><span class="sxs-lookup"><span data-stu-id="9e5e0-240">Strip root signature from shader bytecode.</span></span> <span data-ttu-id="9e5e0-241">Новое для Direct3D 12.</span><span class="sxs-lookup"><span data-stu-id="9e5e0-241">New for Direct3D 12.</span></span>

##### <a name="res_may_alias"></a><span data-ttu-id="9e5e0-242">/res_may_alias</span><span class="sxs-lookup"><span data-stu-id="9e5e0-242">/res_may_alias</span></span>
<span data-ttu-id="9e5e0-243">Предположим, что Уавс/СРВС может быть псевдонимом для cs_5_0 +.</span><span class="sxs-lookup"><span data-stu-id="9e5e0-243">Assume that UAVs/SRVs may alias for cs_5_0+.</span></span> <span data-ttu-id="9e5e0-244">Требуется D3dcompiler \_47.dll или более поздней версии библиотеки DLL.</span><span class="sxs-lookup"><span data-stu-id="9e5e0-244">Requires the D3dcompiler\_47.dll or a later version of the DLL.</span></span>

##### <a name="setprivate-file"></a><span data-ttu-id="9e5e0-245">*файл* </сетпривате></span><span class="sxs-lookup"><span data-stu-id="9e5e0-245">/setprivate <*file*></span></span>
<span data-ttu-id="9e5e0-246">Добавление закрытых данных в заданном файле в скомпилированный BLOB-объект шейдера.</span><span class="sxs-lookup"><span data-stu-id="9e5e0-246">Add private data in the given file to the compiled shader blob.</span></span> <span data-ttu-id="9e5e0-247">Внедряет заданный файл, который рассматривается как необработанный буфер, в большой двоичный объект шейдера.</span><span class="sxs-lookup"><span data-stu-id="9e5e0-247">Embeds the given file, which is treated as a raw buffer, to the shader blob.</span></span> <span data-ttu-id="9e5e0-248">Используйте/сетпривате для добавления частных данных при компиляции шейдера.</span><span class="sxs-lookup"><span data-stu-id="9e5e0-248">Use /setprivate to add private data when you compile a shader.</span></span> <span data-ttu-id="9e5e0-249">Либо используйте параметр/думпбин с/сетпривате для загрузки существующего объекта шейдера, а затем после того, как объект находится в памяти, чтобы добавить закрытый BLOB-объект данных.</span><span class="sxs-lookup"><span data-stu-id="9e5e0-249">Or, use the /dumpbin option with /setprivate to load an existing shader object, and then after the object is in memory, to add the private data blob.</span></span> <span data-ttu-id="9e5e0-250">Например, можно использовать одну команду с/сетпривате, чтобы добавить закрытые данные в скомпилированный BLOB-объект шейдера:</span><span class="sxs-lookup"><span data-stu-id="9e5e0-250">For example, use either a single command with /setprivate to add private data to a compiled shader blob:</span></span>

```console
fxc /T ps_4_0 /Fo ps01.with.private.obj ps01.fx 
    /setprivate ps01.private.data
```
    
<span data-ttu-id="9e5e0-251">Или используйте две команды, где вторая команда загружает объект шейдера, а затем добавляет закрытые данные:</span><span class="sxs-lookup"><span data-stu-id="9e5e0-251">Or, use two commands where the second command loads a shader object and then adds private data:</span></span>

```console
fxc /T ps_4_0 /Fo ps01.no.private.obj ps01.fx
fxc /dumpbin /Fo ps01.with.private.obj ps01.no.private.obj 
    /setprivate ps01.private.data
```
    
##### <a name="setrootsignature-file"></a><span data-ttu-id="9e5e0-252">*файл* </setrootsignature></span><span class="sxs-lookup"><span data-stu-id="9e5e0-252">/setrootsignature <*file*></span></span>
<span data-ttu-id="9e5e0-253">Добавляет корневую подпись к байт-коду шейдера.</span><span class="sxs-lookup"><span data-stu-id="9e5e0-253">Attach root signature to shader bytecode.</span></span> <span data-ttu-id="9e5e0-254">Новое для Direct3D 12.</span><span class="sxs-lookup"><span data-stu-id="9e5e0-254">New for Direct3D 12.</span></span>

##### <a name="shtemplate-file"></a><span data-ttu-id="9e5e0-255">*файл* </штемплате></span><span class="sxs-lookup"><span data-stu-id="9e5e0-255">/shtemplate <*file*></span></span>
<span data-ttu-id="9e5e0-256">Используйте заданный файл шейдера шаблона для слияния (/Мержеуавс) и сопоставления (/Матчуавс) ресурсов.</span><span class="sxs-lookup"><span data-stu-id="9e5e0-256">Use given template shader file for merging (/mergeUAVs) and matching (/matchUAVs) resources.</span></span> <span data-ttu-id="9e5e0-257">Дополнительные сведения см. в разделе <a href="#remarks">Примечания</a>.</span><span class="sxs-lookup"><span data-stu-id="9e5e0-257">For more info, see <a href="#remarks">Remarks</a>.</span></span>

##### <a name="vd"></a><span data-ttu-id="9e5e0-258">/вд</span><span class="sxs-lookup"><span data-stu-id="9e5e0-258">/Vd</span></span>
<span data-ttu-id="9e5e0-259">Отключить проверку.</span><span class="sxs-lookup"><span data-stu-id="9e5e0-259">Disable validation.</span></span>

##### <a name="verifyrootsignature-file"></a><span data-ttu-id="9e5e0-260">*файл* </верифирутсигнатуре></span><span class="sxs-lookup"><span data-stu-id="9e5e0-260">/verifyrootsignature <*file*></span></span>
<span data-ttu-id="9e5e0-261">Проверьте байты шейдера на соответствие корневой подписи.</span><span class="sxs-lookup"><span data-stu-id="9e5e0-261">Verify shader bytecode against root signature.</span></span> <span data-ttu-id="9e5e0-262">Новое для Direct3D 12.</span><span class="sxs-lookup"><span data-stu-id="9e5e0-262">New for Direct3D 12.</span></span>

##### <a name="vi"></a><span data-ttu-id="9e5e0-263">/ви</span><span class="sxs-lookup"><span data-stu-id="9e5e0-263">/Vi</span></span>
<span data-ttu-id="9e5e0-264">Отображение сведений о процессе включения.</span><span class="sxs-lookup"><span data-stu-id="9e5e0-264">Display details about the include process.</span></span>

##### <a name="vn-name"></a><span data-ttu-id="9e5e0-265">*Имя* </VN></span><span class="sxs-lookup"><span data-stu-id="9e5e0-265">/Vn <*name*></span></span>
<span data-ttu-id="9e5e0-266">Используйте имя в качестве имени переменной в файле заголовка.</span><span class="sxs-lookup"><span data-stu-id="9e5e0-266">Use name as variable name in header file.</span></span>

##### <a name="wx"></a><span data-ttu-id="9e5e0-267">/WX</span><span class="sxs-lookup"><span data-stu-id="9e5e0-267">/WX</span></span>
<span data-ttu-id="9e5e0-268">Обрабатывать предупреждения как ошибки.</span><span class="sxs-lookup"><span data-stu-id="9e5e0-268">Treat warnings as errors.</span></span>

##### <a name="zi"></a><span data-ttu-id="9e5e0-269">/ZI</span><span class="sxs-lookup"><span data-stu-id="9e5e0-269">/Zi</span></span>
<span data-ttu-id="9e5e0-270">Включает сведения об отладке.</span><span class="sxs-lookup"><span data-stu-id="9e5e0-270">Enable debugging information.</span></span>

##### <a name="zpc"></a><span data-ttu-id="9e5e0-271">/зпк</span><span class="sxs-lookup"><span data-stu-id="9e5e0-271">/Zpc</span></span>
<span data-ttu-id="9e5e0-272">Матрицы упаковки в столбце — основной порядок.</span><span class="sxs-lookup"><span data-stu-id="9e5e0-272">Pack matrices in column-major order.</span></span>

##### <a name="zpr"></a><span data-ttu-id="9e5e0-273">/зпр</span><span class="sxs-lookup"><span data-stu-id="9e5e0-273">/Zpr</span></span>
<span data-ttu-id="9e5e0-274">Матрицы упаковки в основном порядке строк.</span><span class="sxs-lookup"><span data-stu-id="9e5e0-274">Pack matrices in row-major order.</span></span>

### <a name="filenames"></a><span data-ttu-id="9e5e0-275">*Имена файлов*</span><span class="sxs-lookup"><span data-stu-id="9e5e0-275">*Filenames*</span></span>

<span data-ttu-id="9e5e0-276">\[в \] файлах, содержащих шейдеры и (или) эффекты.</span><span class="sxs-lookup"><span data-stu-id="9e5e0-276">\[in\] The files that contains the shader(s) and/or the effect(s).</span></span>

## <a name="remarks"></a><span data-ttu-id="9e5e0-277">Комментарии</span><span class="sxs-lookup"><span data-stu-id="9e5e0-277">Remarks</span></span>

<span data-ttu-id="9e5e0-278">Используйте `/mergeUAVs` Параметры, `/matchUAVs` и `/shtemplate` для согласования слотов привязки UAV для цепочки шейдеров.</span><span class="sxs-lookup"><span data-stu-id="9e5e0-278">Use the `/mergeUAVs`, `/matchUAVs`, and `/shtemplate` options to align the UAV binding slots for a chain of shaders.</span></span>

<span data-ttu-id="9e5e0-279">Предположим, у вас есть шейдеры A. FX, B. FX и C. FX.</span><span class="sxs-lookup"><span data-stu-id="9e5e0-279">Suppose you have shaders A.fx, B.fx, and C.fx.</span></span> <span data-ttu-id="9e5e0-280">Чтобы вычислить области привязки UAV для этой цепочки шейдеров, необходимы два прохода компиляции:</span><span class="sxs-lookup"><span data-stu-id="9e5e0-280">To align the UAV binding slots for this chain of shaders, you need two passes of compilation:</span></span>

<span data-ttu-id="9e5e0-281">**Выровняйте слоты привязки UAV для цепочки шейдеров**</span><span class="sxs-lookup"><span data-stu-id="9e5e0-281">**To align the UAV binding slots for a chain of shaders**</span></span>

1.  <span data-ttu-id="9e5e0-282">Используйте/Мержеуавс для компиляции шейдеров и укажите ранее скомпилированный большой двоичный объект шейдера с помощью/штемплате.</span><span class="sxs-lookup"><span data-stu-id="9e5e0-282">Use /mergeUAVs to compile shaders, and specify a previously-compiled shader blob with /shtemplate.</span></span> <span data-ttu-id="9e5e0-283">Пример:</span><span class="sxs-lookup"><span data-stu-id="9e5e0-283">For example:</span></span>
    ```
    fxc.exe /T cs_5_0 C.fx /Fo C.o /mergeUAVs /shtemplate Btmp.o
    ```
2.  <span data-ttu-id="9e5e0-284">Используйте/Матчуавс для компиляции шейдеров и укажите последний большой двоичный объект шейдера из первого прохода с помощью/штемплате.</span><span class="sxs-lookup"><span data-stu-id="9e5e0-284">Use /matchUAVs to compile shaders, and specify the last shader blob from the first pass with /shtemplate.</span></span> <span data-ttu-id="9e5e0-285">Можно компилировать в любом порядке.</span><span class="sxs-lookup"><span data-stu-id="9e5e0-285">You can compile in any order.</span></span> <span data-ttu-id="9e5e0-286">Пример:</span><span class="sxs-lookup"><span data-stu-id="9e5e0-286">For example:</span></span>
    ```
    fxc.exe /T cs_5_0 A.fx /Fo A.o /matchUAVs /shtemplate C.o
    ```
<span data-ttu-id="9e5e0-287">При втором прохождении повторной компиляции C. FX не требуется.</span><span class="sxs-lookup"><span data-stu-id="9e5e0-287">You don't have to recompile C.fx in the second pass.</span></span>

<span data-ttu-id="9e5e0-288">После выполнения предыдущих двух проходов компиляции можно использовать A. o, B. o и C. o в качестве итоговых больших двоичных объектов шейдера с согласованными UAV слотами.</span><span class="sxs-lookup"><span data-stu-id="9e5e0-288">After you perform the preceding two compilation passes, you can use A.o, B.o, and C.o as final shader blobs with aligned UAV slots.</span></span>

## <a name="profiles"></a><span data-ttu-id="9e5e0-289">Профили</span><span class="sxs-lookup"><span data-stu-id="9e5e0-289">Profiles</span></span>

<span data-ttu-id="9e5e0-290">Каждая модель шейдеров помечена профилем HLSL.</span><span class="sxs-lookup"><span data-stu-id="9e5e0-290">Each shader model is labeled with an HLSL profile.</span></span> <span data-ttu-id="9e5e0-291">Чтобы скомпилировать шейдер на основе определенной модели шейдера, выберите соответствующий профиль шейдера из следующей таблицы.</span><span class="sxs-lookup"><span data-stu-id="9e5e0-291">To compile a shader against a particular shader model, choose the appropriate shader profile from the following table.</span></span>

<table><thead><tr class="header"><th><span data-ttu-id="9e5e0-292">Тип шейдера</span><span class="sxs-lookup"><span data-stu-id="9e5e0-292">Shader Type</span></span></th><th><span data-ttu-id="9e5e0-293">Профили</span><span class="sxs-lookup"><span data-stu-id="9e5e0-293">Profiles</span></span></th></tr></thead><tbody><tr class="odd"><td><span data-ttu-id="9e5e0-294">Вычисление шейдера</span><span class="sxs-lookup"><span data-stu-id="9e5e0-294">Compute Shader</span></span></td><td><dl> <span data-ttu-id="9e5e0-295">cs_4_0</span><span class="sxs-lookup"><span data-stu-id="9e5e0-295">cs_4_0</span></span><br />
<span data-ttu-id="9e5e0-296">cs_4_1</span><span class="sxs-lookup"><span data-stu-id="9e5e0-296">cs_4_1</span></span><br />
<span data-ttu-id="9e5e0-297">cs_5_0</span><span class="sxs-lookup"><span data-stu-id="9e5e0-297">cs_5_0</span></span><br />
<span data-ttu-id="9e5e0-298">cs_5_1</span><span class="sxs-lookup"><span data-stu-id="9e5e0-298">cs_5_1</span></span><br />
</dl></td></tr><tr class="even"><td><span data-ttu-id="9e5e0-299">Шейдер доменов</span><span class="sxs-lookup"><span data-stu-id="9e5e0-299">Domain Shader</span></span></td><td><dl> <span data-ttu-id="9e5e0-300">ds_5_0</span><span class="sxs-lookup"><span data-stu-id="9e5e0-300">ds_5_0</span></span><br />
<span data-ttu-id="9e5e0-301">ds_5_1</span><span class="sxs-lookup"><span data-stu-id="9e5e0-301">ds_5_1</span></span><br />
</dl></td></tr><tr class="odd"><td><span data-ttu-id="9e5e0-302">Шейдер геометрии</span><span class="sxs-lookup"><span data-stu-id="9e5e0-302">Geometry Shader</span></span></td><td><dl> <span data-ttu-id="9e5e0-303">gs_4_0</span><span class="sxs-lookup"><span data-stu-id="9e5e0-303">gs_4_0</span></span><br />
<span data-ttu-id="9e5e0-304">gs_4_1</span><span class="sxs-lookup"><span data-stu-id="9e5e0-304">gs_4_1</span></span><br />
<span data-ttu-id="9e5e0-305">gs_5_0</span><span class="sxs-lookup"><span data-stu-id="9e5e0-305">gs_5_0</span></span><br />
<span data-ttu-id="9e5e0-306">gs_5_1</span><span class="sxs-lookup"><span data-stu-id="9e5e0-306">gs_5_1</span></span><br />
</dl></td></tr><tr class="even"><td><span data-ttu-id="9e5e0-307">Связывание шейдера HLSL</span><span class="sxs-lookup"><span data-stu-id="9e5e0-307">HLSL shader linking</span></span> </td><td><dl> <span data-ttu-id="9e5e0-308">lib_4_0</span><span class="sxs-lookup"><span data-stu-id="9e5e0-308">lib_4_0</span></span><br />
<span data-ttu-id="9e5e0-309">lib_4_1</span><span class="sxs-lookup"><span data-stu-id="9e5e0-309">lib_4_1</span></span><br />
<span data-ttu-id="9e5e0-310">lib_4_0_level_9_1</span><span class="sxs-lookup"><span data-stu-id="9e5e0-310">lib_4_0_level_9_1</span></span><br />
<span data-ttu-id="9e5e0-311">lib_4_0_level_9_1_vs_only</span><span class="sxs-lookup"><span data-stu-id="9e5e0-311">lib_4_0_level_9_1_vs_only</span></span><br />
<span data-ttu-id="9e5e0-312">lib_4_0_level_9_1_ps_only</span><span class="sxs-lookup"><span data-stu-id="9e5e0-312">lib_4_0_level_9_1_ps_only</span></span><br />
<span data-ttu-id="9e5e0-313">lib_4_0_level_9_3</span><span class="sxs-lookup"><span data-stu-id="9e5e0-313">lib_4_0_level_9_3</span></span><br />
<span data-ttu-id="9e5e0-314">lib_4_0_level_9_3_vs_only</span><span class="sxs-lookup"><span data-stu-id="9e5e0-314">lib_4_0_level_9_3_vs_only</span></span><br />
<span data-ttu-id="9e5e0-315">lib_4_0_level_9_3_ps_only</span><span class="sxs-lookup"><span data-stu-id="9e5e0-315">lib_4_0_level_9_3_ps_only</span></span><br />
<span data-ttu-id="9e5e0-316">lib_5_0</span><span class="sxs-lookup"><span data-stu-id="9e5e0-316">lib_5_0</span></span><br />
</dl> <span data-ttu-id="9e5e0-317">Дополнительные сведения о связывании шейдеров см. в разделе <a href="/windows/desktop/api/d3d11shader/nn-d3d11shader-id3d11linker"><strong>ID3D11Linker</strong></a> и <a href="/windows/desktop/api/d3d11shader/nn-d3d11shader-id3d11functionlinkinggraph"><strong>ID3D11FunctionLinkingGraph</strong></a>.</span><span class="sxs-lookup"><span data-stu-id="9e5e0-317">For more info about shader linking, see <a href="/windows/desktop/api/d3d11shader/nn-d3d11shader-id3d11linker"><strong>ID3D11Linker</strong></a> and <a href="/windows/desktop/api/d3d11shader/nn-d3d11shader-id3d11functionlinkinggraph"><strong>ID3D11FunctionLinkingGraph</strong></a>.</span></span> <br/></td></tr><tr class="odd"><td><span data-ttu-id="9e5e0-318">Шейдер поверхности</span><span class="sxs-lookup"><span data-stu-id="9e5e0-318">Hull Shader</span></span></td><td><dl> <span data-ttu-id="9e5e0-319">hs_5_0</span><span class="sxs-lookup"><span data-stu-id="9e5e0-319">hs_5_0</span></span><br />
<span data-ttu-id="9e5e0-320">hs_5_1</span><span class="sxs-lookup"><span data-stu-id="9e5e0-320">hs_5_1</span></span><br />
</dl></td></tr><tr class="even"><td><span data-ttu-id="9e5e0-321">Построитель текстуры</span><span class="sxs-lookup"><span data-stu-id="9e5e0-321">Pixel Shader</span></span></td><td><dl> <span data-ttu-id="9e5e0-322">ps_2_0</span><span class="sxs-lookup"><span data-stu-id="9e5e0-322">ps_2_0</span></span><br />
<span data-ttu-id="9e5e0-323">ps_2_a</span><span class="sxs-lookup"><span data-stu-id="9e5e0-323">ps_2_a</span></span><br />
<span data-ttu-id="9e5e0-324">ps_2_b</span><span class="sxs-lookup"><span data-stu-id="9e5e0-324">ps_2_b</span></span><br />
<span data-ttu-id="9e5e0-325">ps_2_sw</span><span class="sxs-lookup"><span data-stu-id="9e5e0-325">ps_2_sw</span></span><br />
<span data-ttu-id="9e5e0-326">ps_3_0</span><span class="sxs-lookup"><span data-stu-id="9e5e0-326">ps_3_0</span></span><br />
<span data-ttu-id="9e5e0-327">ps_3_sw</span><span class="sxs-lookup"><span data-stu-id="9e5e0-327">ps_3_sw</span></span><br />
<span data-ttu-id="9e5e0-328">ps_4_0</span><span class="sxs-lookup"><span data-stu-id="9e5e0-328">ps_4_0</span></span><br />
<span data-ttu-id="9e5e0-329">ps_4_0_level_9_0</span><span class="sxs-lookup"><span data-stu-id="9e5e0-329">ps_4_0_level_9_0</span></span><br />
<span data-ttu-id="9e5e0-330">ps_4_0_level_9_1</span><span class="sxs-lookup"><span data-stu-id="9e5e0-330">ps_4_0_level_9_1</span></span><br />
<span data-ttu-id="9e5e0-331">ps_4_0_level_9_3</span><span class="sxs-lookup"><span data-stu-id="9e5e0-331">ps_4_0_level_9_3</span></span><br />
<span data-ttu-id="9e5e0-332">ps_4_1</span><span class="sxs-lookup"><span data-stu-id="9e5e0-332">ps_4_1</span></span><br />
<span data-ttu-id="9e5e0-333">ps_5_0</span><span class="sxs-lookup"><span data-stu-id="9e5e0-333">ps_5_0</span></span><br />
<span data-ttu-id="9e5e0-334">ps_5_1</span><span class="sxs-lookup"><span data-stu-id="9e5e0-334">ps_5_1</span></span><br />
</dl></td></tr><tr class="odd"><td><span data-ttu-id="9e5e0-335">Корневая подпись</span><span class="sxs-lookup"><span data-stu-id="9e5e0-335">Root Signature</span></span></td><td><dl> <span data-ttu-id="9e5e0-336">rootsig_1_0</span><span class="sxs-lookup"><span data-stu-id="9e5e0-336">rootsig_1_0</span></span><br />
</dl></td></tr><tr class="even"><td><span data-ttu-id="9e5e0-337">Шейдер текстуры</span><span class="sxs-lookup"><span data-stu-id="9e5e0-337">Texture Shader</span></span></td><td><dl> <span data-ttu-id="9e5e0-338">tx_1_0</span><span class="sxs-lookup"><span data-stu-id="9e5e0-338">tx_1_0</span></span><br />
</dl></td></tr><tr class="odd"><td><span data-ttu-id="9e5e0-339">Вершинный построитель текстуры</span><span class="sxs-lookup"><span data-stu-id="9e5e0-339">Vertex Shader</span></span></td><td><dl> <span data-ttu-id="9e5e0-340">vs_1_1</span><span class="sxs-lookup"><span data-stu-id="9e5e0-340">vs_1_1</span></span><br />
<span data-ttu-id="9e5e0-341">vs_2_0</span><span class="sxs-lookup"><span data-stu-id="9e5e0-341">vs_2_0</span></span><br />
<span data-ttu-id="9e5e0-342">vs_2_a</span><span class="sxs-lookup"><span data-stu-id="9e5e0-342">vs_2_a</span></span><br />
<span data-ttu-id="9e5e0-343">vs_2_sw</span><span class="sxs-lookup"><span data-stu-id="9e5e0-343">vs_2_sw</span></span><br />
<span data-ttu-id="9e5e0-344">vs_3_0</span><span class="sxs-lookup"><span data-stu-id="9e5e0-344">vs_3_0</span></span><br />
<span data-ttu-id="9e5e0-345">vs_3_sw</span><span class="sxs-lookup"><span data-stu-id="9e5e0-345">vs_3_sw</span></span><br />
<span data-ttu-id="9e5e0-346">vs_4_0</span><span class="sxs-lookup"><span data-stu-id="9e5e0-346">vs_4_0</span></span><br />
<span data-ttu-id="9e5e0-347">vs_4_0_level_9_0</span><span class="sxs-lookup"><span data-stu-id="9e5e0-347">vs_4_0_level_9_0</span></span><br />
<span data-ttu-id="9e5e0-348">vs_4_0_level_9_1</span><span class="sxs-lookup"><span data-stu-id="9e5e0-348">vs_4_0_level_9_1</span></span><br />
<span data-ttu-id="9e5e0-349">vs_4_0_level_9_3</span><span class="sxs-lookup"><span data-stu-id="9e5e0-349">vs_4_0_level_9_3</span></span><br />
<span data-ttu-id="9e5e0-350">vs_4_1</span><span class="sxs-lookup"><span data-stu-id="9e5e0-350">vs_4_1</span></span><br />
<span data-ttu-id="9e5e0-351">vs_5_0</span><span class="sxs-lookup"><span data-stu-id="9e5e0-351">vs_5_0</span></span><br />
<span data-ttu-id="9e5e0-352">vs_5_1</span><span class="sxs-lookup"><span data-stu-id="9e5e0-352">vs_5_1</span></span><br />
</dl></td></tr></tbody></table>

## <a name="version-notes"></a><span data-ttu-id="9e5e0-353">Заметки о версии</span><span class="sxs-lookup"><span data-stu-id="9e5e0-353">Version notes</span></span>

<span data-ttu-id="9e5e0-354">В Direct3D 12 см. [Указание корневых подписей в HLSL](/windows/desktop/direct3d12/specifying-root-signatures-in-hlsl), [Привязка ресурсов в HLSL](/windows/desktop/direct3d12/resource-binding-in-hlsl) и [динамическое индексирование с помощью HLSL 5,1](/windows/desktop/direct3d12/dynamic-indexing-using-hlsl-5-1).</span><span class="sxs-lookup"><span data-stu-id="9e5e0-354">For Direct3D 12 refer to [Specifying Root Signatures in HLSL](/windows/desktop/direct3d12/specifying-root-signatures-in-hlsl), [Resource Binding in HLSL](/windows/desktop/direct3d12/resource-binding-in-hlsl) and [Dynamic Indexing using HLSL 5.1](/windows/desktop/direct3d12/dynamic-indexing-using-hlsl-5-1).</span></span>

<span data-ttu-id="9e5e0-355">В Direct3D 10 используйте API, чтобы получить вершину, геометрию и профиль пиксельного шейдера, которые лучше всего подходят для данного устройства, вызвав следующие функции: [**D3D10GetVertexShaderProfile**](/windows/desktop/api/d3d10shader/nf-d3d10shader-d3d10getvertexshaderprofile), [**D3D10GetPixelShaderProfile**](/windows/desktop/api/d3d10shader/nf-d3d10shader-d3d10getpixelshaderprofile)и [**D3D10GetGeometryShaderProfile**](/windows/desktop/api/d3d10shader/nf-d3d10shader-d3d10getgeometryshaderprofile).</span><span class="sxs-lookup"><span data-stu-id="9e5e0-355">In Direct3D 10 use the API to get the vertex, geometry, and pixel-shader profile best suited to a given device by calling these functions: [**D3D10GetVertexShaderProfile**](/windows/desktop/api/d3d10shader/nf-d3d10shader-d3d10getvertexshaderprofile), [**D3D10GetPixelShaderProfile**](/windows/desktop/api/d3d10shader/nf-d3d10shader-d3d10getpixelshaderprofile), and [**D3D10GetGeometryShaderProfile**](/windows/desktop/api/d3d10shader/nf-d3d10shader-d3d10getgeometryshaderprofile).</span></span>

<span data-ttu-id="9e5e0-356">В Direct3D 9 используйте методы [**жетдевицекапс**](/windows/desktop/api/d3d9/nf-d3d9-idirect3d9-getdevicecaps) или [**жетдевицекапс**](/windows/desktop/api/d3d9/nf-d3d9-idirect3ddevice9-getdevicecaps) для получения профилей вершин и пиксельных шейдеров, поддерживаемых устройством.</span><span class="sxs-lookup"><span data-stu-id="9e5e0-356">In Direct3D 9 use the [**GetDeviceCaps**](/windows/desktop/api/d3d9/nf-d3d9-idirect3d9-getdevicecaps) or [**GetDeviceCaps**](/windows/desktop/api/d3d9/nf-d3d9-idirect3ddevice9-getdevicecaps) methods to retrieve the vertex and pixel-shader profiles supported by a device.</span></span> <span data-ttu-id="9e5e0-357">Структура [**D3DCAPS9**](/windows/desktop/api/d3d9caps/ns-d3d9caps-d3dcaps9) , возвращаемая этими методами, указывает профили вершин и растрового шейдера, поддерживаемые устройством в его членах **вертексшадерверсион** и **пикселшадерверсион** .</span><span class="sxs-lookup"><span data-stu-id="9e5e0-357">The [**D3DCAPS9**](/windows/desktop/api/d3d9caps/ns-d3d9caps-d3dcaps9) structure returned by those methods indicates the vertex and pixel-shader profiles supported by a device in its **VertexShaderVersion** and **PixelShaderVersion** members.</span></span>

<span data-ttu-id="9e5e0-358">Примеры см. [в разделе Компиляция с текущим компилятором](dx-graphics-tools-fxc-using.md).</span><span class="sxs-lookup"><span data-stu-id="9e5e0-358">For examples, see [Compiling with the Current Compiler](dx-graphics-tools-fxc-using.md).</span></span>

## <a name="related-topics"></a><span data-ttu-id="9e5e0-359">См. также</span><span class="sxs-lookup"><span data-stu-id="9e5e0-359">Related topics</span></span>

* [<span data-ttu-id="9e5e0-360">Effect — средство компилятора</span><span class="sxs-lookup"><span data-stu-id="9e5e0-360">Effect-Compiler Tool</span></span>](fxc.md)