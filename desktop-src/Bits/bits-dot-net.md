---
title: Использование BITS из .NET с помощью ссылок на библиотеки DLL
description: В следующих примерах показано, как вызывать интерфейс COM BITS из программы .NET.
ms.assetid: 1058970C-CE81-47D6-950E-3B6289E956B6
ms.topic: article
ms.date: 11/13/2018
ms.openlocfilehash: c359bafe4f1937d49a6ec21896af32606a2ae894
ms.sourcegitcommit: 00e0a8e56d28c4c720b97f0cf424c29f547460d7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/26/2019
ms.locfileid: "103785118"
---
# <a name="calling-into-bits-from-net-and-c-using-reference-dlls"></a><span data-ttu-id="a2c3d-103">Вызов битов из .NET и C# с помощью справочника DLL</span><span class="sxs-lookup"><span data-stu-id="a2c3d-103">Calling into BITS from .NET and C# using Reference DLLs</span></span>

<span data-ttu-id="a2c3d-104">Одним из способов вызова классов COM BITS из программы .NET является создание ссылочного файла DLL, начиная с файлов [IDL](/windows/desktop/Midl/midl-start-page) (язык определения интерфейса) в Windows SDK с помощью средств [MIDL](/windows/desktop/Midl/using-the-midl-compiler-2) и [Tlbimp](/dotnet/framework/tools/tlbimp-exe-type-library-importer) .</span><span class="sxs-lookup"><span data-stu-id="a2c3d-104">One way to call into the BITS COM classes from a .NET program is to create a reference DLL file starting with the BITS [IDL](/windows/desktop/Midl/midl-start-page) (Interface Definition Language) files in the Windows SDK, using the [MIDL](/windows/desktop/Midl/using-the-midl-compiler-2) and [TLBIMP](/dotnet/framework/tools/tlbimp-exe-type-library-importer) tools.</span></span> <span data-ttu-id="a2c3d-105">Библиотека ссылок — это набор оболочек классов для классов COM BITS. Затем можно использовать классы-оболочки непосредственно из .NET.</span><span class="sxs-lookup"><span data-stu-id="a2c3d-105">The reference DLL is a set of class wrappers for the BITS COM classes; you can then use the wrapper classes directly from .NET.</span></span>

<span data-ttu-id="a2c3d-106">Альтернативой использованию автоматически создаваемых ссылок на библиотеки DLL является использование сторонней сторонней оболочки .NET РАЗРЯДов из [GitHub](https://github.com/) и [NuGet](https://www.nuget.org/).</span><span class="sxs-lookup"><span data-stu-id="a2c3d-106">An alternative to using automatically-created reference DLLs is to use a 3rd party .NET BITS wrapper from [GitHub](https://github.com/) and [NuGet](https://www.nuget.org/).</span></span> <span data-ttu-id="a2c3d-107">Эти оболочки часто имеют более естественный стиль программирования .NET, но могут отставать от изменений и обновлений в интерфейсах BITS.</span><span class="sxs-lookup"><span data-stu-id="a2c3d-107">These wrappers often have a more natural .NET programming style but they might lag behind the changes and updates in the BITS interfaces.</span></span>

## <a name="creating-the-reference-dlls"></a><span data-ttu-id="a2c3d-108">Создание ссылок на библиотеки DLL</span><span class="sxs-lookup"><span data-stu-id="a2c3d-108">Creating the reference DLLs</span></span>
### <a name="bits-idl-files"></a><span data-ttu-id="a2c3d-109">IDL-файлы BITS</span><span class="sxs-lookup"><span data-stu-id="a2c3d-109">BITS IDL files</span></span>

<span data-ttu-id="a2c3d-110">Вы начнете с набора IDL-файлов BITS.</span><span class="sxs-lookup"><span data-stu-id="a2c3d-110">You will start with the set of BITS IDL files.</span></span> <span data-ttu-id="a2c3d-111">Это файлы, полностью определяющие COM-интерфейс BITS.</span><span class="sxs-lookup"><span data-stu-id="a2c3d-111">These are files that fully define the BITS COM interface.</span></span> <span data-ttu-id="a2c3d-112">Файлы находятся в каталоге **Windows Kit** и называются BITS *версии*. idl (например, bits10_2. IDL), за исключением файла версии 1,0, который просто является файлом BITS. idl.</span><span class="sxs-lookup"><span data-stu-id="a2c3d-112">The files are located in the **Windows Kits** directory and are named bits *version*.idl (for example, bits10_2.idl) except for the version 1.0 file which is just Bits.idl.</span></span> <span data-ttu-id="a2c3d-113">По мере создания новых версий BITS также создаются новые файлы IDL для битов.</span><span class="sxs-lookup"><span data-stu-id="a2c3d-113">As new versions of BITS are created, new BITS IDL files are also created.</span></span>

<span data-ttu-id="a2c3d-114">Также может потребоваться изменить копию IDL-файлов пакета SDK, чтобы использовать функции BITS, которые не преобразуются автоматически в эквиваленты .NET.</span><span class="sxs-lookup"><span data-stu-id="a2c3d-114">You may also want to modify a copy of the SDK BITS IDL files to use BITS features that aren't automatically converted into .NET equivalents.</span></span> <span data-ttu-id="a2c3d-115">Возможные изменения IDL-файлов обсуждаются далее в.</span><span class="sxs-lookup"><span data-stu-id="a2c3d-115">Possible IDL file changes are discussed later on.</span></span>

<span data-ttu-id="a2c3d-116">Файлы IDL в БИТАХ содержат несколько других IDL-файлов по ссылке.</span><span class="sxs-lookup"><span data-stu-id="a2c3d-116">The BITS IDL files include several other IDL files by reference.</span></span> <span data-ttu-id="a2c3d-117">Они также вложены, поэтому при использовании одной версии она включает в себя все более ранние версии.</span><span class="sxs-lookup"><span data-stu-id="a2c3d-117">They also nest, so that if you use one version, it includes all the lower versions.</span></span>

<span data-ttu-id="a2c3d-118">Для каждой версии BITS, которую необходимо нацелить в программе, потребуется одна ссылка на библиотеку DLL для этой версии.</span><span class="sxs-lookup"><span data-stu-id="a2c3d-118">For each version of BITS that you want to target in your program you will need one reference DLL for that version.</span></span> <span data-ttu-id="a2c3d-119">Например, если вы хотите написать программу, которая работает в БИТАХ 1,5 и выше, но имеет дополнительные функции при наличии службы BITS 10,2, необходимо преобразовать файлы bits1_5. idl и bits10_2. idl.</span><span class="sxs-lookup"><span data-stu-id="a2c3d-119">For example, if you want to write a program that works on BITS 1.5 and up but has additional features when BITS 10.2 is present, you need to convert both the bits1_5.idl and bits10_2.idl files.</span></span>


### <a name="midl-and-tlbimp-utilities"></a><span data-ttu-id="a2c3d-120">MIDL и служебные программы TLBIMP</span><span class="sxs-lookup"><span data-stu-id="a2c3d-120">MIDL and TLBIMP utilities</span></span>

<span data-ttu-id="a2c3d-121">Программа [MIDL](/windows/desktop/Midl/using-the-midl-compiler-2) (язык MIDL) ПРЕОБРАЗУЕТ IDL-файлы, описывающие интерфейс COM BITS, в файл TLB (библиотеки типов).</span><span class="sxs-lookup"><span data-stu-id="a2c3d-121">The [MIDL](/windows/desktop/Midl/using-the-midl-compiler-2) (Microsoft Interface Definition Language) utility converts the IDL files that describe the BITS COM interface into a TLB (Type Library) file.</span></span> <span data-ttu-id="a2c3d-122">Средство MIDL зависит от программы CL (препроцессора C) для правильного чтения файла языка IDL.</span><span class="sxs-lookup"><span data-stu-id="a2c3d-122">The MIDL tool depends on the CL utility (C preprocessor) to correctly read the IDL language file.</span></span> <span data-ttu-id="a2c3d-123">Программа CL является частью Visual Studio и устанавливается при включении функций C/C++ в установку Visual Studio.</span><span class="sxs-lookup"><span data-stu-id="a2c3d-123">The CL utility is part of Visual Studio and is installed when you include C/C++ features in the Visual Studio installation.</span></span>

<span data-ttu-id="a2c3d-124">Программа MIDL, как правило, создает набор файлов C и H (код языка C и язык C).</span><span class="sxs-lookup"><span data-stu-id="a2c3d-124">The MIDL utility will normally create a set of C and H (C language code and C language header) files.</span></span> <span data-ttu-id="a2c3d-125">Эти дополнительные файлы можно отключить, отправив выходные данные на устройство NUL:.</span><span class="sxs-lookup"><span data-stu-id="a2c3d-125">You can suppress these extra files by sending the output to the NUL: device.</span></span> <span data-ttu-id="a2c3d-126">Например, при настройке параметра/dlldata NUL: будет отключено создание файла DLLDATA. c.</span><span class="sxs-lookup"><span data-stu-id="a2c3d-126">For example, setting the /dlldata NUL: switch will suppress creating a dlldata.c file.</span></span> <span data-ttu-id="a2c3d-127">В приведенных ниже примерах команд показано, какие параметры должны иметь значение NUL:.</span><span class="sxs-lookup"><span data-stu-id="a2c3d-127">The sample commands below shows which switches should be set to NUL:.</span></span>

<span data-ttu-id="a2c3d-128">Программа [Tlbimp](/dotnet/framework/tools/tlbimp-exe-type-library-importer) (средство импорта библиотек типов) СЧИТЫВАЕТ файл TLB и создает соответствующий справочный файл DLL.</span><span class="sxs-lookup"><span data-stu-id="a2c3d-128">The [TLBIMP](/dotnet/framework/tools/tlbimp-exe-type-library-importer) (Type Library Importer) utility reads in a TLB file and creates the corresponding reference DLL file.</span></span> 


### <a name="example-commands-for-midl-and-tlbimp"></a><span data-ttu-id="a2c3d-129">Примеры команд для MIDL и TLBIMP</span><span class="sxs-lookup"><span data-stu-id="a2c3d-129">Example commands for MIDL and TLBIMP</span></span>

<span data-ttu-id="a2c3d-130">Это пример полного набора команд для создания набора справочных файлов.</span><span class="sxs-lookup"><span data-stu-id="a2c3d-130">This is an example of the complete set of commands to generate a set of reference files.</span></span> <span data-ttu-id="a2c3d-131">Вам может потребоваться изменить команды на основе Visual Studio и Windows SDK установки и в зависимости от того, какие функции BITS и версии ОС вы используете.</span><span class="sxs-lookup"><span data-stu-id="a2c3d-131">You may need to modify the commands based on your Visual Studio and Windows SDK installation and based on the BITS features and OS versions you are targeting.</span></span> 

<span data-ttu-id="a2c3d-132">В примере создается каталог для размещения ссылок на DLL-файлы и создается переменная среды БИТСТЕМП, указывающая на этот каталог.</span><span class="sxs-lookup"><span data-stu-id="a2c3d-132">The example creates a directory to place the reference DLL files and creates an environment variable BITSTEMP to point to that directory.</span></span> 

<span data-ttu-id="a2c3d-133">Затем команды запускают файл vsdevcmd.bat, созданный установщиком Visual Studio.</span><span class="sxs-lookup"><span data-stu-id="a2c3d-133">The example commands then run the vsdevcmd.bat file that's created by the Visual Studio installer.</span></span> <span data-ttu-id="a2c3d-134">В этом файле BAT будут настроены пути и некоторые переменные среды, чтобы выполнялись команды MIDL и TLBIMP.</span><span class="sxs-lookup"><span data-stu-id="a2c3d-134">This BAT file will set up your paths and some environment variables so that the MIDL and TLBIMP commands will run.</span></span> <span data-ttu-id="a2c3d-135">Он также настраивает переменные Виндовссдкдир и Виндовссдклибверсион, чтобы они указывали на самые последние Windows SDK каталоги.</span><span class="sxs-lookup"><span data-stu-id="a2c3d-135">It also sets up the WindowsSdkDir and WindowsSDKLibVersion variables to point to the most recent Windows SDK directories.</span></span>

```console
REM Create a working directory
REM You can select a different directory based on your needs.
SET BITSTEMP=C:\BITSTEMPDIR
MKDIR "%BITSTEMP%"

REM Run the VsDevCmd.bat file to locate the Windows
REM SDK directory and the tools directories
REM This will be different for different versions of
REM Visual Studio

CALL "C:\Program Files (x86)\Microsoft Visual Studio\2017\Enterprise\Common7\Tools\vsdevcmd.bat"

REM Run the MIDL command on the desired BITS IDL file
REM This will generate a TLB file for the TLBIMP command
REM The IDL file will be different depending on which
REM set of BITS interfaces you need to use.
REM Run the MIDL command once per reference file
REM that you will need to explicitly use.
PUSHD .
CD /D "%WindowsSdkDir%Include\%WindowsSDKLibVersion%um"

MIDL  /I ..\shared /out "%BITSTEMP%" bits1_5.idl /dlldata NUL: /header NUL: /iid NUL: /proxy NUL:
MIDL  /I ..\shared /out "%BITSTEMP%" bits4_0.idl /dlldata NUL: /header NUL: /iid NUL: /proxy NUL:
MIDL  /I ..\shared /out "%BITSTEMP%" bits5_0.idl /dlldata NUL: /header NUL: /iid NUL: /proxy NUL:
MIDL  /I ..\shared /out "%BITSTEMP%" bits10_1.idl /dlldata NUL: /header NUL: /iid NUL: /proxy NUL:
MIDL  /I ..\shared /out "%BITSTEMP%" bits10_2.idl /dlldata NUL: /header NUL: /iid NUL: /proxy NUL:

REM Run the TLBIMP command on the resulting TLB file(s)
REM Try to keep a parallel set of names.
TLBIMP "%BITSTEMP%"\bits1_5.tlb /out: "%BITSTEMP%"\BITSReference1_5.dll
TLBIMP "%BITSTEMP%"\bits4_0.tlb /out: "%BITSTEMP%"\BITSReference4_0.dll
TLBIMP "%BITSTEMP%"\bits5_0.tlb /out: "%BITSTEMP%"\BITSReference5_0.dll
TLBIMP "%BITSTEMP%"\bits10_1.tlb /out: "%BITSTEMP%"\BITSReference10_1.dll
TLBIMP "%BITSTEMP%"\bits10_2.tlb /out: "%BITSTEMP%"\BITSReference10_2.dll
DEL "%BITSTEMP%"\bits*.tlb
POPD

```
<span data-ttu-id="a2c3d-136">После выполнения этих команд у вас будет набор справочных библиотек DLL в каталоге БИТСТЕМП.</span><span class="sxs-lookup"><span data-stu-id="a2c3d-136">Once these commands are run you will have a set of reference DLLs in the BITSTEMP directory.</span></span>

### <a name="adding-the-reference-dlls-to-your-project"></a><span data-ttu-id="a2c3d-137">Добавление ссылочных библиотек DLL в проект</span><span class="sxs-lookup"><span data-stu-id="a2c3d-137">Adding the reference DLLs to your project</span></span>

<span data-ttu-id="a2c3d-138">Чтобы использовать ссылочную библиотеку DLL в проекте C#, откройте проект C# в Visual Studio.</span><span class="sxs-lookup"><span data-stu-id="a2c3d-138">To use a reference DLL in a C# project, open your C# project in Visual Studio.</span></span> <span data-ttu-id="a2c3d-139">В обозреватель решений щелкните правой кнопкой мыши ссылки и выберите команду Добавить ссылку.</span><span class="sxs-lookup"><span data-stu-id="a2c3d-139">In the Solution Explorer, right-click the References and click Add Reference.</span></span> <span data-ttu-id="a2c3d-140">Затем нажмите кнопку обзора, а затем кнопку Добавить.</span><span class="sxs-lookup"><span data-stu-id="a2c3d-140">Then click the Browse button and then the Add button.</span></span> <span data-ttu-id="a2c3d-141">Перейдите в каталог со ссылками на библиотеки DLL, выберите их и нажмите кнопку Добавить.</span><span class="sxs-lookup"><span data-stu-id="a2c3d-141">Navigate to the directory with the reference DLLs, select them, and click Add.</span></span> <span data-ttu-id="a2c3d-142">В окне диспетчера ссылок будут проверены ссылочные библиотеки DLL.</span><span class="sxs-lookup"><span data-stu-id="a2c3d-142">In the Reference Manager window the reference DLLs will be checked.</span></span> <span data-ttu-id="a2c3d-143">Затем нажмите кнопку ОК.</span><span class="sxs-lookup"><span data-stu-id="a2c3d-143">Then click OK.</span></span>

<span data-ttu-id="a2c3d-144">Библиотеки DLL ссылок на BITS теперь добавляются в проект.</span><span class="sxs-lookup"><span data-stu-id="a2c3d-144">The BITS reference DLLs are now added to your project.</span></span>

<span data-ttu-id="a2c3d-145">Информация в файлах DLL ссылок будет внедрена в окончательную программу.</span><span class="sxs-lookup"><span data-stu-id="a2c3d-145">The information in the reference DLL files will be embedded into your final program.</span></span> <span data-ttu-id="a2c3d-146">Вам не нужно поставлять файлы DLL ссылок в вашу программу; Вам нужно просто поставлять. Программы.</span><span class="sxs-lookup"><span data-stu-id="a2c3d-146">You do not have to ship the reference DLL files with your program; you just need to ship the .EXE.</span></span> 

<span data-ttu-id="a2c3d-147">Можно изменить, внедряются ли ссылочные библиотеки DLL в окончательный исполняемый файл.</span><span class="sxs-lookup"><span data-stu-id="a2c3d-147">You can change whether the reference DLLs are embedded into the final EXE.</span></span> <span data-ttu-id="a2c3d-148">Используйте свойство [Внедрить типы взаимодействия](/dotnet/framework/interop/how-to-add-references-to-type-libraries) , чтобы задать, будут ли внедрены ссылочные библиотеки DLL.</span><span class="sxs-lookup"><span data-stu-id="a2c3d-148">Use the [Embed Interop Types](/dotnet/framework/interop/how-to-add-references-to-type-libraries) property to set whether or not the reference DLLs will be embedded.</span></span> <span data-ttu-id="a2c3d-149">Это можно сделать на основе каждой ссылки.</span><span class="sxs-lookup"><span data-stu-id="a2c3d-149">This can be done on a per-reference basis.</span></span> <span data-ttu-id="a2c3d-150">Значение по умолчанию — true для внедрения библиотек DLL.</span><span class="sxs-lookup"><span data-stu-id="a2c3d-150">The default is True to embed the DLLs.</span></span>

## <a name="modifying-idl-files-for-more-complete-net-code"></a><span data-ttu-id="a2c3d-151">Изменение IDL-файлов для более полного кода .NET</span><span class="sxs-lookup"><span data-stu-id="a2c3d-151">Modifying IDL files for more complete .NET code</span></span>

<span data-ttu-id="a2c3d-152">Файлы IDL (язык MIDL) BITS можно использовать без изменений, чтобы сделать DLL-файл Баккграундкопиманажер.</span><span class="sxs-lookup"><span data-stu-id="a2c3d-152">The BITS IDL (Microsoft Interface Definition Language) files can be used unchanged to make the BackgroundCopyManager DLL file.</span></span> <span data-ttu-id="a2c3d-153">Однако результирующая DLL-библиотека .NET не будет содержать некоторые непреобразованные объединения и имеет трудные имена для некоторых структур и перечислений.</span><span class="sxs-lookup"><span data-stu-id="a2c3d-153">However, the resulting .NET reference DLL will be missing some untranslatable unions and has hard-to-use names for some structures and enums.</span></span> <span data-ttu-id="a2c3d-154">В этом разделе описаны некоторые изменения, которые можно сделать, чтобы сделать библиотеку DLL .NET более полной и удобной для использования.</span><span class="sxs-lookup"><span data-stu-id="a2c3d-154">This section will describe some of the changes that you can make to make the .NET DLL more complete and easier to use.</span></span>

### <a name="simpler-enum-names"></a><span data-ttu-id="a2c3d-155">Более простые имена перечислений</span><span class="sxs-lookup"><span data-stu-id="a2c3d-155">Simpler ENUM names</span></span>

<span data-ttu-id="a2c3d-156">IDL-файлы BITS обычно определяют перечисляемые значения следующим образом:</span><span class="sxs-lookup"><span data-stu-id="a2c3d-156">The BITS IDL files typically define enum values like this:</span></span>
```
    typedef enum
    {
            BG_AUTH_TARGET_SERVER = 1,
            BG_AUTH_TARGET_PROXY
    } BG_AUTH_TARGET;
```
<span data-ttu-id="a2c3d-157">BG_AUTH_TARGET — имя определения типа; фактическое перечисление не называется.</span><span class="sxs-lookup"><span data-stu-id="a2c3d-157">The BG_AUTH_TARGET is the name of the typedef; the actual enum is not named.</span></span> <span data-ttu-id="a2c3d-158">Обычно это не вызывает проблем с кодом C, но не подходит для использования с программой .NET.</span><span class="sxs-lookup"><span data-stu-id="a2c3d-158">This doesn’t typically cause problems with C code but doesn’t translate well for use with a .NET program.</span></span> <span data-ttu-id="a2c3d-159">Новое имя будет создано автоматически, но оно может выглядеть так, как _MIDL___MIDL_itf_bits4_0_0005_0001_0001, а не как удобное для восприятия значение.</span><span class="sxs-lookup"><span data-stu-id="a2c3d-159">A new name will be automatically created, but it might look something like _MIDL___MIDL_itf_bits4_0_0005_0001_0001 instead of a human-readable value.</span></span> <span data-ttu-id="a2c3d-160">Эту проблему можно устранить, обновив файлы MIDL, включив в них имя перечисления.</span><span class="sxs-lookup"><span data-stu-id="a2c3d-160">You can fix this problem by updating the MIDL files to include an enum name.</span></span>

```
    typedef enum BG_AUTH_TARGET
    {
            BG_AUTH_TARGET_SERVER = 1,
            BG_AUTH_TARGET_PROXY
    } BG_AUTH_TARGET;
```

<span data-ttu-id="a2c3d-161">Имя перечисления может совпадать с именем typedef.</span><span class="sxs-lookup"><span data-stu-id="a2c3d-161">The enum name is allowed to be the same as the typedef name.</span></span> <span data-ttu-id="a2c3d-162">Некоторые программисты имеют соглашение об именовании, где они различаются (например, при вводе символа подчеркивания перед именем перечисления), но это будет путать только переводы .NET.</span><span class="sxs-lookup"><span data-stu-id="a2c3d-162">Some programmers have a naming convention where they are kept different (for example, by putting an underscore before the enum name), but this will only confuse the .NET translations.</span></span> 

### <a name="string-types-in-unions"></a><span data-ttu-id="a2c3d-163">Строковые типы в объединениях</span><span class="sxs-lookup"><span data-stu-id="a2c3d-163">String types in unions</span></span>

<span data-ttu-id="a2c3d-164">Файлы IDL-файлов BITS передают строки с помощью LPWSTR (длинный указатель на строку расширенных символов).</span><span class="sxs-lookup"><span data-stu-id="a2c3d-164">The BITS IDL files pass strings using the LPWSTR (long pointer to wide-character string) convention.</span></span> <span data-ttu-id="a2c3d-165">Хотя это работает при передаче параметров функции (например, метод Job. Pval ([out] LPWSTR \*)), он не работает, если строки являются частью объединения.</span><span class="sxs-lookup"><span data-stu-id="a2c3d-165">Although this works when passing function parameters (like the Job.GetDisplayName([out] LPWSTR \*pVal) method), it doesn’t work when the strings are part of unions.</span></span> <span data-ttu-id="a2c3d-166">Например, файл bits5_0. idl включает в себя BITS_FILE_PROPERTY_VALUEное объединение:</span><span class="sxs-lookup"><span data-stu-id="a2c3d-166">For example, the bits5_0.idl file includes the BITS_FILE_PROPERTY_VALUE union:</span></span>

```
typedef [switch_type(BITS_FILE_PROPERTY_ID)] union
{
    [case( BITS_FILE_PROPERTY_ID_HTTP_RESPONSE_HEADERS )]
        LPWSTR String;
}
BITS_FILE_PROPERTY_VALUE;
```

<span data-ttu-id="a2c3d-167">Поле LPWSTR не будет включаться в версию .NET объединения.</span><span class="sxs-lookup"><span data-stu-id="a2c3d-167">The LPWSTR field won’t be included in the .NET version of the union.</span></span> <span data-ttu-id="a2c3d-168">Чтобы устранить эту проблему, измените параметр LPWSTR на WCHAR \*.</span><span class="sxs-lookup"><span data-stu-id="a2c3d-168">To fix this, change the LPWSTR to a WCHAR\*.</span></span> <span data-ttu-id="a2c3d-169">Итоговое поле (называемое строкой) будет передано как IntPtr.</span><span class="sxs-lookup"><span data-stu-id="a2c3d-169">The resulting field (called String) will be passed as a IntPtr.</span></span> <span data-ttu-id="a2c3d-170">Преобразуйте его в строку, используя System. Runtime. InteropServices. Marshal. Птртострингауто (значение. Строка); Method.</span><span class="sxs-lookup"><span data-stu-id="a2c3d-170">Convert this into a string using the  System.Runtime.InteropServices.Marshal.PtrToStringAuto(value.String); method.</span></span>

### <a name="unions-in-structures"></a><span data-ttu-id="a2c3d-171">Объединения в структурах</span><span class="sxs-lookup"><span data-stu-id="a2c3d-171">Unions in structures</span></span>

<span data-ttu-id="a2c3d-172">Иногда объединения, внедренные в структуры, не будут включены в структуру.</span><span class="sxs-lookup"><span data-stu-id="a2c3d-172">Sometimes unions that are embedded in structures won't be included in the structure at all.</span></span> <span data-ttu-id="a2c3d-173">Например, в Bits1_5. idl BG_AUTH_CREDENTIALS определяется следующим образом:</span><span class="sxs-lookup"><span data-stu-id="a2c3d-173">For example, in the Bits1_5.idl the BG_AUTH_CREDENTIALS is defined as follows:</span></span>
```
    typedef struct
    {
        BG_AUTH_TARGET Target;
        BG_AUTH_SCHEME Scheme;
        [switch_is(Scheme)] BG_AUTH_CREDENTIALS_UNION Credentials;
    }
    BG_AUTH_CREDENTIALS;
```

<span data-ttu-id="a2c3d-174">BG_AUTH_CREDENTIALS_UNION определяется как объединение следующим образом:</span><span class="sxs-lookup"><span data-stu-id="a2c3d-174">The BG_AUTH_CREDENTIALS_UNION is defined to be a union as follows:</span></span>
```
    typedef [switch_type(BG_AUTH_SCHEME)] union
    {
            [case( BG_AUTH_SCHEME_BASIC, BG_AUTH_SCHEME_DIGEST, BG_AUTH_SCHEME_NTLM,
            BG_AUTH_SCHEME_NEGOTIATE, BG_AUTH_SCHEME_PASSPORT )] BG_BASIC_CREDENTIALS Basic;
            [default] ;
    } BG_AUTH_CREDENTIALS_UNION;
```
<span data-ttu-id="a2c3d-175">Поле учетные данные в BG_AUTH_CREDENTIALS не будет включаться в определение класса .NET.</span><span class="sxs-lookup"><span data-stu-id="a2c3d-175">The Credentials field in the BG_AUTH_CREDENTIALS will not be included in the .NET class definition.</span></span>

<span data-ttu-id="a2c3d-176">Обратите внимание, что UNION определяется так, чтобы всегда быть BG_BASIC_CREDENTIALS независимо от BG_AUTH_SCHEME.</span><span class="sxs-lookup"><span data-stu-id="a2c3d-176">Note that the union is defined to always be a BG_BASIC_CREDENTIALS regardless of the BG_AUTH_SCHEME.</span></span> <span data-ttu-id="a2c3d-177">Поскольку объединение не используется в качестве объединения, можно просто передать BG_BASIC_CREDENTIALS следующим образом:</span><span class="sxs-lookup"><span data-stu-id="a2c3d-177">Because the union isn’t used as a union, we can just pass a BG_BASIC_CREDENTIALS like this:</span></span>
```
    typedef struct
    {
        BG_AUTH_TARGET Target;
        BG_AUTH_SCHEME Scheme;
        BG_BASIC_CREDENTIALS Credentials;
    }
    BG_AUTH_CREDENTIALS;
```

## <a name="using-bits-from-c"></a><span data-ttu-id="a2c3d-178">Использование битов из C #</span><span class="sxs-lookup"><span data-stu-id="a2c3d-178">Using BITS from C#</span></span>

### <a name="recommended-using-statement"></a><span data-ttu-id="a2c3d-179">Рекомендуемая инструкция using</span><span class="sxs-lookup"><span data-stu-id="a2c3d-179">Recommended using statement</span></span>

<span data-ttu-id="a2c3d-180">Настройка некоторых инструкций using в C# сокращает количество символов, которые необходимо ввести для использования различных версий BITS.</span><span class="sxs-lookup"><span data-stu-id="a2c3d-180">Setting up some using statements in C# will reduce the number of characters you need to type to use the different BITS versions.</span></span> <span data-ttu-id="a2c3d-181">Имя "Битсреференце" берется из имени справочной библиотеки DLL.</span><span class="sxs-lookup"><span data-stu-id="a2c3d-181">The name "BITSReference" comes from the name of the reference DLL.</span></span>

```csharp
// Set up the BITS namespaces
using BITS = BITSReference1_5;
using BITS4 = BITSReference4_0;
using BITS5 = BITSReference5_0;
using BITS10_2 = BITSReference10_2;
```

### <a name="quick-sample-download-a-file"></a><span data-ttu-id="a2c3d-182">Краткий пример: скачивание файла</span><span class="sxs-lookup"><span data-stu-id="a2c3d-182">Quick Sample: download a file</span></span>

<span data-ttu-id="a2c3d-183">Ниже приведен короткий, но полный фрагмент кода C# для загрузки файла из URL-адреса.</span><span class="sxs-lookup"><span data-stu-id="a2c3d-183">A short but complete snippet of C# code to download a file from a URL is given below.</span></span> 

```csharp
    var mgr = new BITS.BackgroundCopyManager1_5();
    BITS.GUID jobGuid;
    BITS.IBackgroundCopyJob job;
    mgr.CreateJob("Quick download", BITS.BG_JOB_TYPE.BG_JOB_TYPE_DOWNLOAD, out jobGuid, out job);
    job.AddFile("https://aka.ms/WinServ16/StndPDF", @"C:\Server2016.pdf");
    job.Resume();
    bool jobIsFinal = false;
    while (!jobIsFinal)
    {
        BITS.BG_JOB_STATE state;
        job.GetState(out state);
        switch (state)
        {
            case BITS.BG_JOB_STATE.BG_JOB_STATE_ERROR:
            case BITS.BG_JOB_STATE.BG_JOB_STATE_TRANSFERRED:
                job.Complete();
                break;

            case BITS.BG_JOB_STATE.BG_JOB_STATE_CANCELLED:
            case BITS.BG_JOB_STATE.BG_JOB_STATE_ACKNOWLEDGED:
                jobIsFinal = true;
                break;
            default:
                Task.Delay(500); // delay a little bit
                break;
        }
    }
    // Job is complete
```

<span data-ttu-id="a2c3d-184">В этом примере кода создается диспетчер BITS с именем диспетчера.</span><span class="sxs-lookup"><span data-stu-id="a2c3d-184">In this sample code, a BITS manager named mgr is created.</span></span> <span data-ttu-id="a2c3d-185">Он непосредственно соответствует интерфейсу [ибаккграундкопиманажер](/windows/desktop/api/bits/nn-bits-ibackgroundcopymanager) .</span><span class="sxs-lookup"><span data-stu-id="a2c3d-185">It directly corresponds to the [IBackgroundCopyManager](/windows/desktop/api/bits/nn-bits-ibackgroundcopymanager) interface.</span></span> 

<span data-ttu-id="a2c3d-186">В диспетчере создается новое задание.</span><span class="sxs-lookup"><span data-stu-id="a2c3d-186">From the manager a new job is created.</span></span> <span data-ttu-id="a2c3d-187">Задание является выходным параметром метода CreateJob.</span><span class="sxs-lookup"><span data-stu-id="a2c3d-187">The job is an out parameter on the CreateJob method.</span></span> <span data-ttu-id="a2c3d-188">Кроме того, передано имя задания (которое не обязательно должно быть уникальным) и тип загрузки, который является заданием скачивания.</span><span class="sxs-lookup"><span data-stu-id="a2c3d-188">Also passed in is the job name (which doesn't have to be unique) and the download type, which is a download job.</span></span> <span data-ttu-id="a2c3d-189">Также заполняется идентификатор GUID BITS для идентификатора задания.</span><span class="sxs-lookup"><span data-stu-id="a2c3d-189">A BITS GUID for the job identifier is also filled in.</span></span>

<span data-ttu-id="a2c3d-190">После создания задания добавьте новый файл загрузки в задание с помощью метода AddFile.</span><span class="sxs-lookup"><span data-stu-id="a2c3d-190">Once the job is created you add a new download file to the job with the AddFile method.</span></span> <span data-ttu-id="a2c3d-191">Необходимо передать две строки: одну для удаленного файла (URL-адрес или общую папку), а другой — для локального файла.</span><span class="sxs-lookup"><span data-stu-id="a2c3d-191">You need to pass in two strings, one for the remote file (the URL or file share) and one for the local file.</span></span> 

<span data-ttu-id="a2c3d-192">После добавления файла вызовите для задания команду Resume, чтобы запустить его.</span><span class="sxs-lookup"><span data-stu-id="a2c3d-192">After adding the file, call Resume on the job to start it.</span></span> <span data-ttu-id="a2c3d-193">Затем код ждет, пока задание находится в конечном состоянии (ошибка или передано), а затем завершается.</span><span class="sxs-lookup"><span data-stu-id="a2c3d-193">Then the code waits until the job is in a final state (ERROR or TRANSFERRED) and is then completed.</span></span>

### <a name="bits-versions-casting-and-queryinterface"></a><span data-ttu-id="a2c3d-194">Версии BITS, приведение и QueryInterface</span><span class="sxs-lookup"><span data-stu-id="a2c3d-194">BITS Versions, Casting and QueryInterface</span></span>

<span data-ttu-id="a2c3d-195">Вы обнаружите, что часто приходится использовать как раннюю версию объекта BITS, так и более позднюю версию в программе.</span><span class="sxs-lookup"><span data-stu-id="a2c3d-195">You'll find that you often have to use both an early version of a BITS object and a more recent version in your program.</span></span>  

<span data-ttu-id="a2c3d-196">Например, при создании объекта задания вы получите использованием метода ibackgroundcopyjob (часть версии BITS 1,0), даже если вы делаете это с помощью более свежего объекта Manager и доступен более новый объект использованием метода ibackgroundcopyjob.</span><span class="sxs-lookup"><span data-stu-id="a2c3d-196">For example, when you make a job object, you will get an IBackgroundCopyJob (part of BITS version 1.0) even when you're making it using a more recent manager object and a more recent IBackgroundCopyJob object is available.</span></span> <span data-ttu-id="a2c3d-197">Поскольку метод CreateJob не принимает интерфейс для более новой версии, вы не можете напрямую сделать более свежую версию.</span><span class="sxs-lookup"><span data-stu-id="a2c3d-197">Because the CreateJob method doesn't accept an interface for the more recent version, you can't directly make the more recent version.</span></span>

<span data-ttu-id="a2c3d-198">Используйте приведение к .NET для преобразования старого объекта типа в более новый объект типа.</span><span class="sxs-lookup"><span data-stu-id="a2c3d-198">Use a .NET cast to convert from an older type object to a newer type object.</span></span> <span data-ttu-id="a2c3d-199">Приведение будет автоматически вызывать QueryInterface COM, как нужно.</span><span class="sxs-lookup"><span data-stu-id="a2c3d-199">The cast will automatically call a COM QueryInterface as appropriate.</span></span> 

<span data-ttu-id="a2c3d-200">В этом примере имеется объект BITS использованием метода ibackgroundcopyjob с именем Job, и мы хотим преобразовать его в объект IBackgroundCopyJob5 с именем «job5», чтобы мы могли вызвать метод-свойство BITS 5,0.</span><span class="sxs-lookup"><span data-stu-id="a2c3d-200">In this example, there's a BITS IBackgroundCopyJob object named "job", and we want to convert it to an IBackgroundCopyJob5 object named "job5" so that we can call the BITS 5.0 GetProperty method.</span></span> <span data-ttu-id="a2c3d-201">Мы просто приведен к типу IBackgroundCopyJob5 следующим образом:</span><span class="sxs-lookup"><span data-stu-id="a2c3d-201">We just cast to the IBackgroundCopyJob5 type like this:</span></span>

```csharp
var job5 = (BITS5.IBackgroundCopyJob5)job;
```

<span data-ttu-id="a2c3d-202">Переменная job5 будет инициализирована .NET с помощью правильного QueryInterface.</span><span class="sxs-lookup"><span data-stu-id="a2c3d-202">The job5 variable will be initialized by .NET by using the correct QueryInterface.</span></span> 

<span data-ttu-id="a2c3d-203">Если код может выполняться в системе, которая не поддерживает определенную версию BITS, можно попробовать выполнить приведение и перехватить System. InvalidCastException.</span><span class="sxs-lookup"><span data-stu-id="a2c3d-203">If your code might run on a system that doesn't support a particular version of BITS, you can try the cast and catch the System.InvalidCastException.</span></span> 

```csharp
BITS5.IBackgroundCopyJob5 job5 = null;
try
{
    job5 = (BITS5.IBackgroundCopyJob5)Job;
}
catch (System.InvalidCastException)
{
    ; // Must be running an earlier version of BITS
}
```

<span data-ttu-id="a2c3d-204">Распространенной проблемой является попытка привести к неправильному виду объекта.</span><span class="sxs-lookup"><span data-stu-id="a2c3d-204">A common problem is when you try to cast into the wrong kind of object.</span></span> <span data-ttu-id="a2c3d-205">Система .NET не знает о реальной связи между интерфейсами BITS.</span><span class="sxs-lookup"><span data-stu-id="a2c3d-205">The .NET system doesn't know about the real relationship between the BITS interfaces.</span></span> <span data-ttu-id="a2c3d-206">Если запрашивается неправильный тип интерфейса, .NET попытается сделать его для вас и завершится ошибкой InvalidCastException и HResult 0x80004002 (E_NOINTERFACE).</span><span class="sxs-lookup"><span data-stu-id="a2c3d-206">If you ask for the wrong kind of interface, .NET will try to make it for you and will fail with an InvalidCastException and HResult 0x80004002 (E_NOINTERFACE).</span></span>

### <a name="working-with-bits-versions-10_1-and-10_2"></a><span data-ttu-id="a2c3d-207">Работа с версиями BITS 10_1 и 10_2</span><span class="sxs-lookup"><span data-stu-id="a2c3d-207">Working with BITS Versions 10_1 and 10_2</span></span>

<span data-ttu-id="a2c3d-208">В некоторых версиях Windows 10 нельзя напрямую создать объект Ибаккграундкопиманажер BITS с помощью интерфейсов 10,1 или 10,2.</span><span class="sxs-lookup"><span data-stu-id="a2c3d-208">On some versions of Windows 10 you can't directly create a BITS IBackgroundCopyManager object using the 10.1 or 10.2 interfaces.</span></span> <span data-ttu-id="a2c3d-209">Вместо этого необходимо использовать несколько версий справочных файлов DLL Баккграундкопиманажер.</span><span class="sxs-lookup"><span data-stu-id="a2c3d-209">Instead, you'll have to use multiple versions of the BackgroundCopyManager DLL reference files.</span></span> <span data-ttu-id="a2c3d-210">Например, можно использовать версию 1,5 для создания объекта Ибаккграундкопиманажер, а затем привести результирующее задание или объекты файлов с помощью версий 10,1 или 10,2.</span><span class="sxs-lookup"><span data-stu-id="a2c3d-210">For example, you can use the 1.5 version to make an IBackgroundCopyManager object, and then cast the resulting job or file objects using the 10.1 or 10.2 versions.</span></span>

