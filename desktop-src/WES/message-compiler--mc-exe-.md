---
title: Компилятор сообщений (MC.exe)
description: Используется для компиляции манифестов инструментирования и текстовых файлов сообщений.
ms.assetid: f9de35f1-6d31-4f4b-b2c4-8474d6fce9e0
keywords:
- Журнал компилятора сообщений (MC.exe)
topic_type:
- apiref
api_name:
- Message Compiler (MC.exe)
api_type:
- NA
ms.topic: reference
ms.date: 06/03/2020
ms.openlocfilehash: 5eb852dcbb13800705db0a0f19d912de899f9b0f
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104539332"
---
# <a name="message-compiler-mcexe"></a><span data-ttu-id="a4fae-104">Компилятор сообщений (MC.exe)</span><span class="sxs-lookup"><span data-stu-id="a4fae-104">Message Compiler (MC.exe)</span></span>

<span data-ttu-id="a4fae-105">Используется для компиляции манифестов инструментирования и текстовых файлов сообщений.</span><span class="sxs-lookup"><span data-stu-id="a4fae-105">Used to compile instrumentation manifests and message text files.</span></span> <span data-ttu-id="a4fae-106">Компилятор создает файлы ресурсов сообщений, на которые ссылается приложение.</span><span class="sxs-lookup"><span data-stu-id="a4fae-106">The compiler generates the message resource files to which your application links.</span></span>

``` syntax
MC [-?aAbcdnouUv] [-m <length>] [-h <path>] [-e <extension>] [-r <path>]
   [-x <path>] [-w <file>] [-W <file>] [-z <basename> ] [-cp <encoding>]
   [-km | -um | -generateProjections | -cs <namespace>]
   [-mof] [-p <prefix>] [-P <prefix>]
   [<filename.man>] [<filename.mc>]
```

-   [<span data-ttu-id="a4fae-107">Аргументы, общие для текстовых файлов сообщений и файлов манифеста</span><span class="sxs-lookup"><span data-stu-id="a4fae-107">Arguments common to both message text files and manifest files</span></span>](#arguments-common-to-both-message-text-files-and-manifest-files)
-   [<span data-ttu-id="a4fae-108">Аргументы, относящиеся к файлам манифеста</span><span class="sxs-lookup"><span data-stu-id="a4fae-108">Arguments specific to manifest files</span></span>](#arguments-specific-to-manifest-files)
-   [<span data-ttu-id="a4fae-109">Аргументы, относящиеся к генерированию кода, который поставщик будет использовать для регистрации событий</span><span class="sxs-lookup"><span data-stu-id="a4fae-109">Arguments specific to generating code that your provider would use to log events</span></span>](#arguments-specific-to-generating-code-that-your-provider-would-use-to-log-events)
-   [<span data-ttu-id="a4fae-110">Аргументы, относящиеся к текстовым файлам сообщений</span><span class="sxs-lookup"><span data-stu-id="a4fae-110">Arguments specific to message text files</span></span>](#arguments-specific-to-message-text-files)

## <a name="arguments-common-to-both-message-text-files-and-manifest-files"></a><span data-ttu-id="a4fae-111">Аргументы, общие для текстовых файлов сообщений и файлов манифеста</span><span class="sxs-lookup"><span data-stu-id="a4fae-111">Arguments common to both message text files and manifest files</span></span>

<dl> <dt>

<span data-ttu-id="a4fae-112"><span id="-_"></span>**-?**</span><span class="sxs-lookup"><span data-stu-id="a4fae-112"><span id="-_"></span>**-?**</span></span>
</dt> <dd>

<span data-ttu-id="a4fae-113">Отображает сведения об использовании компилятора сообщений.</span><span class="sxs-lookup"><span data-stu-id="a4fae-113">Displays the usage information for the Message Compiler.</span></span>

</dd> <dt>

<span data-ttu-id="a4fae-114"><span id="-c"></span><span id="-C"></span>**-c**</span><span class="sxs-lookup"><span data-stu-id="a4fae-114"><span id="-c"></span><span id="-C"></span>**-c**</span></span>
</dt> <dd>

<span data-ttu-id="a4fae-115">Используйте этот аргумент, чтобы задать для компилятора бит клиента (бит 28) во всех идентификаторах сообщений.</span><span class="sxs-lookup"><span data-stu-id="a4fae-115">Use this argument to have the compiler set the customer bit (bit 28) in all message IDs.</span></span> <span data-ttu-id="a4fae-116">Сведения о разряде клиента см. в файле Winerror. h.</span><span class="sxs-lookup"><span data-stu-id="a4fae-116">For information on the customer bit, see winerror.h.</span></span>

</dd> <dt>

<span data-ttu-id="a4fae-117"><span id="-cp"></span><span id="-CP"></span>**-CP** *кодирование*</span><span class="sxs-lookup"><span data-stu-id="a4fae-117"><span id="-cp"></span><span id="-CP"></span>**-cp** *encoding*</span></span>
</dt> <dd>

<span data-ttu-id="a4fae-118">Используйте этот аргумент, чтобы указать кодировку символов, используемую для всех созданных текстовых файлов.</span><span class="sxs-lookup"><span data-stu-id="a4fae-118">Use this argument to specify the character encoding used for all generated text files.</span></span> <span data-ttu-id="a4fae-119">Допустимые имена: "ANSI" (по умолчанию), "UTF-8" и "UTF-16".</span><span class="sxs-lookup"><span data-stu-id="a4fae-119">Valid names include "ansi" (default), "utf-8", and "utf-16".</span></span> <span data-ttu-id="a4fae-120">В кодировках Юникода будет добавлена метка порядка байтов.</span><span class="sxs-lookup"><span data-stu-id="a4fae-120">The Unicode encodings will add a byte order mark.</span></span>

</dd> <dt>

<span data-ttu-id="a4fae-121"><span id="-e_extension"></span><span id="-E_EXTENSION"></span>**-e** , *расширение*</span><span class="sxs-lookup"><span data-stu-id="a4fae-121"><span id="-e_extension"></span><span id="-E_EXTENSION"></span>**-e** *extension*</span></span>
</dt> <dd>

<span data-ttu-id="a4fae-122">Используйте этот аргумент, чтобы указать расширение, используемое для файла заголовка.</span><span class="sxs-lookup"><span data-stu-id="a4fae-122">Use this argument to specify the extension to use for the header file.</span></span> <span data-ttu-id="a4fae-123">Можно указать до трех символов, не включая точку.</span><span class="sxs-lookup"><span data-stu-id="a4fae-123">You can specify up to a three characters extension, not including the period.</span></span> <span data-ttu-id="a4fae-124">Значение по умолчанию —. h.</span><span class="sxs-lookup"><span data-stu-id="a4fae-124">The default is .h.</span></span>

</dd> <dt>

<span data-ttu-id="a4fae-125"><span id="-h_path"></span><span id="-H_PATH"></span>**-h** *путь*</span><span class="sxs-lookup"><span data-stu-id="a4fae-125"><span id="-h_path"></span><span id="-H_PATH"></span>**-h** *path*</span></span>
</dt> <dd>

<span data-ttu-id="a4fae-126">Используйте этот аргумент, чтобы указать папку, в которую компилятор должен поместить созданный файл заголовка.</span><span class="sxs-lookup"><span data-stu-id="a4fae-126">Use this argument to specify the folder into which you want the compiler to place the generated header file.</span></span> <span data-ttu-id="a4fae-127">Значением по умолчанию является текущий каталог.</span><span class="sxs-lookup"><span data-stu-id="a4fae-127">The default is the current directory.</span></span>

</dd> <dt>

<span data-ttu-id="a4fae-128"><span id="-m_length"></span><span id="-M_LENGTH"></span>**-m** *Длина*</span><span class="sxs-lookup"><span data-stu-id="a4fae-128"><span id="-m_length"></span><span id="-M_LENGTH"></span>**-m** *length*</span></span>
</dt> <dd>

<span data-ttu-id="a4fae-129">Используйте этот аргумент, чтобы компилятор создавал предупреждение, если длина любого сообщения превышает *длину* символов.</span><span class="sxs-lookup"><span data-stu-id="a4fae-129">Use this argument to have the compiler generate a warning if the any message exceeds *length* characters.</span></span>

</dd> <dt>

<span data-ttu-id="a4fae-130"><span id="-r_path"></span><span id="-R_PATH"></span>**-r** *путь*</span><span class="sxs-lookup"><span data-stu-id="a4fae-130"><span id="-r_path"></span><span id="-R_PATH"></span>**-r** *path*</span></span>
</dt> <dd>

<span data-ttu-id="a4fae-131">Используйте этот аргумент, чтобы указать папку, в которую компилятор должен поместить созданный скрипт компилятора ресурсов (RC-файл) и созданные файлы bin (двоичные ресурсы), включаемые в скрипт компилятора ресурсов.</span><span class="sxs-lookup"><span data-stu-id="a4fae-131">Use this argument to specify the folder into which you want the compiler to place the generated resource compiler script (.rc file) and the generated .bin files (binary resources) that the resource compiler script includes.</span></span> <span data-ttu-id="a4fae-132">Значением по умолчанию является текущий каталог.</span><span class="sxs-lookup"><span data-stu-id="a4fae-132">The default is the current directory.</span></span>

</dd> <dt>

<span data-ttu-id="a4fae-133"><span id="-z_name"></span><span id="-Z_NAME"></span>**-z** *имя*</span><span class="sxs-lookup"><span data-stu-id="a4fae-133"><span id="-z_name"></span><span id="-Z_NAME"></span>**-z** *name*</span></span>
</dt> <dd>

<span data-ttu-id="a4fae-134">Используйте этот аргумент, чтобы переопределить базовое имя по умолчанию, используемое компилятором для создаваемых им файлов.</span><span class="sxs-lookup"><span data-stu-id="a4fae-134">Use this argument to override the default base name that the compiler uses for the files that it generates.</span></span> <span data-ttu-id="a4fae-135">По умолчанию используется базовое имя входного файла *имени* файла.</span><span class="sxs-lookup"><span data-stu-id="a4fae-135">The default is to use the base name of the *filename* input file.</span></span>

</dd> <dt>

<span data-ttu-id="a4fae-136"><span id="filename"></span><span id="FILENAME"></span>*файлов*</span><span class="sxs-lookup"><span data-stu-id="a4fae-136"><span id="filename"></span><span id="FILENAME"></span>*filename*</span></span>
</dt> <dd>

<span data-ttu-id="a4fae-137">Файл манифеста инструментирования или текстовый файл сообщения.</span><span class="sxs-lookup"><span data-stu-id="a4fae-137">The instrumentation manifest file or message text file.</span></span> <span data-ttu-id="a4fae-138">Файл должен находиться в текущем каталоге.</span><span class="sxs-lookup"><span data-stu-id="a4fae-138">The file must exist in the current directory.</span></span> <span data-ttu-id="a4fae-139">Можно указать файл манифеста, текстовый файл сообщения или и то, и другое.</span><span class="sxs-lookup"><span data-stu-id="a4fae-139">You can specify a manifest file, message text file, or both.</span></span> <span data-ttu-id="a4fae-140">Имя файла должно включать расширение.</span><span class="sxs-lookup"><span data-stu-id="a4fae-140">The file name must include the extension.</span></span> <span data-ttu-id="a4fae-141">Соглашение заключается в использовании расширения. Man для файлов манифеста и расширения MC для текстовых файлов сообщений.</span><span class="sxs-lookup"><span data-stu-id="a4fae-141">The convention is to use a .man extension for manifest files and a .mc extension for message text files.</span></span>

</dd> </dl>

### <a name="arguments-specific-to-manifest-files"></a><span data-ttu-id="a4fae-142">Аргументы, относящиеся к файлам манифеста</span><span class="sxs-lookup"><span data-stu-id="a4fae-142">Arguments specific to manifest files</span></span>

<dl> <dt>

<span data-ttu-id="a4fae-143"><span id="-s_path"></span><span id="-S_PATH"></span>**-s** *путь*</span><span class="sxs-lookup"><span data-stu-id="a4fae-143"><span id="-s_path"></span><span id="-S_PATH"></span>**-s** *path*</span></span>
</dt> <dd>

<span data-ttu-id="a4fae-144">Используйте этот аргумент для создания базового плана инструментирования.</span><span class="sxs-lookup"><span data-stu-id="a4fae-144">Use this argument to create a baseline of your instrumentation.</span></span> <span data-ttu-id="a4fae-145">Укажите путь к папке, содержащей файлы базового манифеста.</span><span class="sxs-lookup"><span data-stu-id="a4fae-145">Specify the path to the folder that contains your baseline manifest files.</span></span> <span data-ttu-id="a4fae-146">Для последующих выпусков следует использовать аргумент **-t** для проверки нового манифеста в соответствии с базовыми показателями проблем совместимости.</span><span class="sxs-lookup"><span data-stu-id="a4fae-146">For subsequent releases, you would then use the **-t** argument to check the new manifest against the baseline for compatibility issues.</span></span>

<span data-ttu-id="a4fae-147">**До версии MC 1.12.7051:** Недоступно</span><span class="sxs-lookup"><span data-stu-id="a4fae-147">**Prior to MC version 1.12.7051:** Not available</span></span>

</dd> <dt>

<span data-ttu-id="a4fae-148"><span id="-t_path"></span><span id="-T_PATH"></span>**-t** *путь*</span><span class="sxs-lookup"><span data-stu-id="a4fae-148"><span id="-t_path"></span><span id="-T_PATH"></span>**-t** *path*</span></span>
</dt> <dd>

<span data-ttu-id="a4fae-149">Используйте этот аргумент при создании новой версии манифеста и необходимости его проверки на совместимость приложений с базовыми показателями, созданными с помощью аргумента **-s** .</span><span class="sxs-lookup"><span data-stu-id="a4fae-149">Use this argument when you create a new version of your manifest and want to check it for application compatibility against the baseline that you created using the **-s** argument.</span></span> <span data-ttu-id="a4fae-150">Путь должен указывать на папку, содержащую. Файлы BIN, созданные базовой операцией (см. параметр **-s** ).</span><span class="sxs-lookup"><span data-stu-id="a4fae-150">The path must point to the folder that contains the .BIN files that the baseline operation created (see the **-s** switch).</span></span>

<span data-ttu-id="a4fae-151">**До версии MC 1.12.7051:** Недоступно</span><span class="sxs-lookup"><span data-stu-id="a4fae-151">**Prior to MC version 1.12.7051:** Not available</span></span>

</dd> <dt>

<span data-ttu-id="a4fae-152"><span id="-w_path"></span><span id="-W_PATH"></span>**-w** *путь*</span><span class="sxs-lookup"><span data-stu-id="a4fae-152"><span id="-w_path"></span><span id="-W_PATH"></span>**-w** *path*</span></span>
</dt> <dd>

<span data-ttu-id="a4fae-153">Компилятор игнорирует этот аргумент и автоматически проверяет манифест.</span><span class="sxs-lookup"><span data-stu-id="a4fae-153">The compiler ignores this argument and automatically validates the manifest.</span></span>

<span data-ttu-id="a4fae-154">**До версии MC 1.12.7051:** Используйте этот аргумент, чтобы указать папку, содержащую файл схемы Events. xsd, который компилятор использует для проверки манифеста.</span><span class="sxs-lookup"><span data-stu-id="a4fae-154">**Prior to MC version 1.12.7051:** Use this argument to specify the folder that contains the Eventman.xsd schema file, which the compiler uses to validate your manifest.</span></span> <span data-ttu-id="a4fae-155">Windows SDK включает файл схемы Events. xsd в \\ папку include.</span><span class="sxs-lookup"><span data-stu-id="a4fae-155">The Windows SDK includes the Eventman.xsd schema file in the \\Include folder.</span></span> <span data-ttu-id="a4fae-156">Если этот аргумент не указан, компилятор не проверяет манифест.</span><span class="sxs-lookup"><span data-stu-id="a4fae-156">If you do not specify this argument, the compiler does not validate your manifest.</span></span>

</dd> <dt>

<span data-ttu-id="a4fae-157"><span id="-W_path"></span><span id="-w_path"></span><span id="-W_PATH"></span>**-W** *путь*</span><span class="sxs-lookup"><span data-stu-id="a4fae-157"><span id="-W_path"></span><span id="-w_path"></span><span id="-W_PATH"></span>**-W** *path*</span></span>
</dt> <dd>

<span data-ttu-id="a4fae-158">Компилятор игнорирует этот аргумент.</span><span class="sxs-lookup"><span data-stu-id="a4fae-158">The compiler ignores this argument.</span></span>

<span data-ttu-id="a4fae-159">**До версии MC 1.12.7051:** Используйте этот аргумент, чтобы указать папку, содержащую файл Winmeta.xml.</span><span class="sxs-lookup"><span data-stu-id="a4fae-159">**Prior to MC version 1.12.7051:** Use this argument to specify the folder that contains the Winmeta.xml file.</span></span> <span data-ttu-id="a4fae-160">Файл Winmeta.xml содержит распознаваемые типы входных и выходных данных, а также стандартные каналы, уровни и коды операций.</span><span class="sxs-lookup"><span data-stu-id="a4fae-160">The Winmeta.xml file contains the recognized input and output types as well as the predefined channels, levels, and opcodes.</span></span> <span data-ttu-id="a4fae-161">Windows SDK включает файл Winmeta.xml в \\ папку include.</span><span class="sxs-lookup"><span data-stu-id="a4fae-161">The Windows SDK includes the Winmeta.xml file in the \\Include folder.</span></span>

</dd> </dl>

### <a name="arguments-specific-to-generating-code-that-your-provider-would-use-to-log-events"></a><span data-ttu-id="a4fae-162">Аргументы, относящиеся к генерированию кода, который поставщик будет использовать для регистрации событий</span><span class="sxs-lookup"><span data-stu-id="a4fae-162">Arguments specific to generating code that your provider would use to log events</span></span>

<span data-ttu-id="a4fae-163">Следующие аргументы компилятора можно использовать для создания кода режима ядра или пользовательского режима, который можно использовать для записи событий в журнал.</span><span class="sxs-lookup"><span data-stu-id="a4fae-163">You can use the following compiler arguments to generate kernel-mode or user-mode code that you can use to log events.</span></span> <span data-ttu-id="a4fae-164">Кроме того, можно запросить создание кода компилятором для поддержки записи событий на компьютерах до Windows Vista.</span><span class="sxs-lookup"><span data-stu-id="a4fae-164">You can also request that the compiler generate code to support writing events on computers prior to Windows Vista.</span></span> <span data-ttu-id="a4fae-165">Если приложение написано на C#, компилятор может создать класс C#, который можно использовать для регистрации событий.</span><span class="sxs-lookup"><span data-stu-id="a4fae-165">If your application is written C#, the compiler can generate a C# class that you can use to log events.</span></span> <span data-ttu-id="a4fae-166">Эти аргументы доступны начиная с версии MC 1.12.7051, поставляемой с Windows 7 пакета SDK для окна.</span><span class="sxs-lookup"><span data-stu-id="a4fae-166">These arguments are available beginning with MC version 1.12.7051 that ships with the Windows 7 version of the Window SDK.</span></span>

<dl> <dt>

<span data-ttu-id="a4fae-167"><span id="-co"></span><span id="-CO"></span>**-Co**</span><span class="sxs-lookup"><span data-stu-id="a4fae-167"><span id="-co"></span><span id="-CO"></span>**-co**</span></span>
</dt> <dd>

<span data-ttu-id="a4fae-168">Используйте этот аргумент, чтобы служба ведения журнала вызывала определяемую пользователем функцию для каждого события, которое вы регистрируете (функция вызывается после регистрации события).</span><span class="sxs-lookup"><span data-stu-id="a4fae-168">Use this argument to have the logging service call your user-defined function for each event that you log (the function is called after the event has been logged).</span></span> <span data-ttu-id="a4fae-169">Определяемая пользователем функция должна иметь следующую сигнатуру.</span><span class="sxs-lookup"><span data-stu-id="a4fae-169">Your user-defined function must have the following signature.</span></span>


```C++
VOID
pFnUserFunction(
    __in REGHANDLE RegHandle,
    __in PCEVENT_DESCRIPTOR Descriptor,
    __in ULONG EventDataCount,
    __in_ecount(EventDataCount) PEVENT_DATA_DESCRIPTOR EventData
    );
```



<span data-ttu-id="a4fae-170">В код необходимо также включить следующую директиву.</span><span class="sxs-lookup"><span data-stu-id="a4fae-170">You must also include the following directive in your code.</span></span>

`#define MCGEN_CALLOUT pFnUserFunction`

<span data-ttu-id="a4fae-171">Чтобы избежать проблем с ведением журнала, следует использовать максимально короткий способ реализации. служба больше не будет регистрировать события до тех пор, пока функция не вернет значение.</span><span class="sxs-lookup"><span data-stu-id="a4fae-171">You should keep your implementation as short as possible to prevent logging issues; the service will not log anymore of your events until the function returns.</span></span>

<span data-ttu-id="a4fae-172">Этот аргумент можно использовать с аргументом **-км** или **-UM** .</span><span class="sxs-lookup"><span data-stu-id="a4fae-172">You can use this argument with the **-km** or **-um** argument.</span></span>

</dd> <dt>

<span data-ttu-id="a4fae-173"><span id="-cs_namespace"></span><span id="-CS_NAMESPACE"></span>**—** *пространство имен* CS</span><span class="sxs-lookup"><span data-stu-id="a4fae-173"><span id="-cs_namespace"></span><span id="-CS_NAMESPACE"></span>**-cs** *namespace*</span></span>
</dt> <dd>

<span data-ttu-id="a4fae-174">Используйте этот аргумент, чтобы компилятор создавал класс C# на основе класса .NET 3,5 [EventProvider](/dotnet/api/system.diagnostics.eventing.eventprovider?view=netframework-3.5&preserve-view=true) .</span><span class="sxs-lookup"><span data-stu-id="a4fae-174">Use this argument to have the compiler generate a C# class based on the .NET 3.5 [EventProvider](/dotnet/api/system.diagnostics.eventing.eventprovider?view=netframework-3.5&preserve-view=true) class.</span></span>

</dd> <dt>

<span data-ttu-id="a4fae-175"><span id="-css_namespace"></span><span id="-CSS_NAMESPACE"></span>**-** *пространство имен* CSS</span><span class="sxs-lookup"><span data-stu-id="a4fae-175"><span id="-css_namespace"></span><span id="-CSS_NAMESPACE"></span>**-css** *namespace*</span></span>
</dt> <dd>

<span data-ttu-id="a4fae-176">Используйте этот аргумент, чтобы компилятор создавал статический класс C# на основе класса .NET 3,5 [EventProvider](/dotnet/api/system.diagnostics.eventing.eventprovider?view=netframework-3.5&preserve-view=true) .</span><span class="sxs-lookup"><span data-stu-id="a4fae-176">Use this argument to have the compiler generate a static C# class based on the .NET 3.5 [EventProvider](/dotnet/api/system.diagnostics.eventing.eventprovider?view=netframework-3.5&preserve-view=true) class.</span></span>

</dd> <dt>

<span data-ttu-id="a4fae-177"><span id="-km"></span><span id="-KM"></span>**-км**</span><span class="sxs-lookup"><span data-stu-id="a4fae-177"><span id="-km"></span><span id="-KM"></span>**-km**</span></span>
</dt> <dd>

<span data-ttu-id="a4fae-178">Используйте этот аргумент, чтобы компилятор создавал код режима ядра, который будет использоваться для записи в журнал событий, определенных в манифесте.</span><span class="sxs-lookup"><span data-stu-id="a4fae-178">Use this argument to have the compiler generate the kernel-mode code that you would use to log the events defined in your manifest.</span></span>

</dd> <dt>

<span data-ttu-id="a4fae-179"><span id="-mof"></span><span id="-MOF"></span>**-MOF**</span><span class="sxs-lookup"><span data-stu-id="a4fae-179"><span id="-mof"></span><span id="-MOF"></span>**-mof**</span></span>
</dt> <dd>

<span data-ttu-id="a4fae-180">Не рекомендуется.</span><span class="sxs-lookup"><span data-stu-id="a4fae-180">DEPRECATED.</span></span> <span data-ttu-id="a4fae-181">Используйте этот аргумент, чтобы компилятор создавал код, который можно использовать для регистрации событий на компьютерах до Windows Vista.</span><span class="sxs-lookup"><span data-stu-id="a4fae-181">Use this argument to have the compiler generate code that you can use to log events on computers prior to Windows Vista.</span></span> <span data-ttu-id="a4fae-182">Этот параметр также создает MOF-файл, содержащий классы MOF для каждого события, определенного в манифесте.</span><span class="sxs-lookup"><span data-stu-id="a4fae-182">This option also creates a MOF file that contains the MOF classes for each event defined in the manifest.</span></span> <span data-ttu-id="a4fae-183">Чтобы зарегистрировать классы в MOF-файле, чтобы потребители могли декодировать события, используйте компилятор MOF (Mofcomp.exe).</span><span class="sxs-lookup"><span data-stu-id="a4fae-183">To register the classes in the MOF file so that consumers can decode the events, use the MOF compiler (Mofcomp.exe).</span></span> <span data-ttu-id="a4fae-184">Дополнительные сведения об использовании компилятора MOF см. в разделе [MOF-файл](/windows/desktop/WmiSdk/managed-object-format--mof-).</span><span class="sxs-lookup"><span data-stu-id="a4fae-184">For details on using the MOF compiler, see [Managed Object Format](/windows/desktop/WmiSdk/managed-object-format--mof-).</span></span>

<span data-ttu-id="a4fae-185">Чтобы использовать этот параметр, необходимо соблюдать следующие ограничения.</span><span class="sxs-lookup"><span data-stu-id="a4fae-185">To use this switch, you must adhere to the following restrictions:</span></span>

-   <span data-ttu-id="a4fae-186">Каждое определение события должно включать атрибуты Task и opcode.</span><span class="sxs-lookup"><span data-stu-id="a4fae-186">Every event definition must include the task and opcode attributes</span></span>
-   <span data-ttu-id="a4fae-187">Каждая задача должна включать атрибут Евентгуид</span><span class="sxs-lookup"><span data-stu-id="a4fae-187">Every task must include the eventGuid attribute</span></span>
-   <span data-ttu-id="a4fae-188">Данные шаблона, на которые ссылается событие, не могут содержать:</span><span class="sxs-lookup"><span data-stu-id="a4fae-188">The template data that the event references cannot contain:</span></span>
    -   <span data-ttu-id="a4fae-189">Элементы данных, указывающие типы ввода Win: binary или Win: SYSTEMTIME</span><span class="sxs-lookup"><span data-stu-id="a4fae-189">Data items that specify the win:Binary or win:SYSTEMTIME input types</span></span>
    -   <span data-ttu-id="a4fae-190">Структуры</span><span class="sxs-lookup"><span data-stu-id="a4fae-190">Structures</span></span>
    -   <span data-ttu-id="a4fae-191">Массивы переменного размера; Однако можно указать массивы фиксированной длины.</span><span class="sxs-lookup"><span data-stu-id="a4fae-191">Variable sized arrays; however, you can specify fixed length arrays</span></span>
    -   <span data-ttu-id="a4fae-192">Строковые типы данных не могут задавать атрибут длины</span><span class="sxs-lookup"><span data-stu-id="a4fae-192">String data types cannot specify the length attribute</span></span>

<span data-ttu-id="a4fae-193">Этот аргумент необходимо использовать с аргументом **-UM**, **-CS**, **-CSS** или **-км** .</span><span class="sxs-lookup"><span data-stu-id="a4fae-193">You must use this argument with the **-um**, **-cs**, **-css**, or **-km** argument</span></span>

</dd> <dt>

<span data-ttu-id="a4fae-194"><span id="-p_prefix"></span><span id="-P_PREFIX"></span>**-p** , *префикс*</span><span class="sxs-lookup"><span data-stu-id="a4fae-194"><span id="-p_prefix"></span><span id="-P_PREFIX"></span>**-p** *prefix*</span></span>
</dt> <dd>

<span data-ttu-id="a4fae-195">Используйте этот аргумент, чтобы переопределить префикс по умолчанию, используемый компилятором для имен макросов и имен методов в журнале.</span><span class="sxs-lookup"><span data-stu-id="a4fae-195">Use this argument to override the default prefix that the compiler uses for the logging macro names and method names.</span></span> <span data-ttu-id="a4fae-196">Префикс по умолчанию — "EventWrite".</span><span class="sxs-lookup"><span data-stu-id="a4fae-196">The default prefix is "EventWrite".</span></span> <span data-ttu-id="a4fae-197">Строка обрабатывается с учетом регистра.</span><span class="sxs-lookup"><span data-stu-id="a4fae-197">The string is case-sensitive.</span></span>

<span data-ttu-id="a4fae-198">Этот аргумент можно использовать с аргументом **-UM**, **-CS**, **-CSS** или **-км** .</span><span class="sxs-lookup"><span data-stu-id="a4fae-198">You can use this argument with the **-um**, **-cs**, **-css**, or **-km** argument.</span></span>

</dd> <dt>

<span data-ttu-id="a4fae-199"><span id="-P_prefix"></span><span id="-p_prefix"></span><span id="-P_PREFIX"></span>**-P** , *префикс*</span><span class="sxs-lookup"><span data-stu-id="a4fae-199"><span id="-P_prefix"></span><span id="-p_prefix"></span><span id="-P_PREFIX"></span>**-P** *prefix*</span></span>
</dt> <dd>

<span data-ttu-id="a4fae-200">Используйте этот аргумент, чтобы удалить символы из начала символического имени, указанного для события.</span><span class="sxs-lookup"><span data-stu-id="a4fae-200">Use this argument to remove characters from the beginning of the symbolic name that you specified for the event.</span></span> <span data-ttu-id="a4fae-201">При сравнении регистр не учитывается.</span><span class="sxs-lookup"><span data-stu-id="a4fae-201">The comparison is case-insensitive.</span></span> <span data-ttu-id="a4fae-202">Компилятор использует символьное имя для формирования имен макросов и имен методов.</span><span class="sxs-lookup"><span data-stu-id="a4fae-202">The compiler uses the symbolic name to form the logging macro names and method names.</span></span>

<span data-ttu-id="a4fae-203">По умолчанию для макроса ведения журнала используется имя EventWrite *симболнаме*, где *симболнаме* — это символьное имя, указанное для события.</span><span class="sxs-lookup"><span data-stu-id="a4fae-203">The default name for a logging macro is EventWrite *SymbolName*, where *SymbolName* is the symbolic name that you specified for the event.</span></span> <span data-ttu-id="a4fae-204">Например, если задать для атрибута Symbol события значение Принтерконнектион, то имя макроса будет Евентвритепринтерконнектион.</span><span class="sxs-lookup"><span data-stu-id="a4fae-204">For example, if you set the symbol attribute of the event to PrinterConnection, the macro name would be EventWritePrinterConnection.</span></span> <span data-ttu-id="a4fae-205">Чтобы удалить принтер из имени, используйте параметр **-P** **Printer**, который приводит к евентвритеконнектион.</span><span class="sxs-lookup"><span data-stu-id="a4fae-205">To remove Printer from the name, use **-P** **Printer**, which results in EventWriteConnection.</span></span>

<span data-ttu-id="a4fae-206">Этот аргумент можно использовать с аргументом **-UM**, **-CS**, **-CSS** или **-км** .</span><span class="sxs-lookup"><span data-stu-id="a4fae-206">You can use this argument with the **-um**, **-cs**, **-css**, or **-km** argument.</span></span>

</dd> <dt>

<span data-ttu-id="a4fae-207"><span id="-um"></span><span id="-UM"></span>**-UM**</span><span class="sxs-lookup"><span data-stu-id="a4fae-207"><span id="-um"></span><span id="-UM"></span>**-um**</span></span>
</dt> <dd>

<span data-ttu-id="a4fae-208">Используйте этот аргумент, чтобы компилятор создавал код пользовательского режима, который будет использоваться для записи в журнал событий, определенных в манифесте.</span><span class="sxs-lookup"><span data-stu-id="a4fae-208">Use this argument to have the compiler generate the user-mode code that you would use to log the events defined in your manifest.</span></span>

</dd> </dl>

<span data-ttu-id="a4fae-209">Чтобы компилятор создавал код ведения журнала, необходимо указать аргумент **-UM**, **-CS**, **-CSS** или **-км** . Эти аргументы являются взаимоисключающими.</span><span class="sxs-lookup"><span data-stu-id="a4fae-209">To have the compiler generate logging code, you must specify the **-um**, **-cs**, **-css**, or **-km** argument; these arguments are mutually exclusive.</span></span>

<span data-ttu-id="a4fae-210">Чтобы указать место размещения файлов. h,. cs и. mof, создаваемых компилятором, используйте аргумент **-h** .</span><span class="sxs-lookup"><span data-stu-id="a4fae-210">To specify where to place the .h, .cs, and .mof files that the compiler generates, use the **-h** argument.</span></span> <span data-ttu-id="a4fae-211">Если не указать аргумент **-h** , файлы помещаются в текущую папку.</span><span class="sxs-lookup"><span data-stu-id="a4fae-211">If you do not specify the **-h** argument, the files are placed in the current folder.</span></span>

<span data-ttu-id="a4fae-212">Чтобы указать место размещения RC-файла и двоичных файлов (которые содержат ресурсы метаданных), создаваемых компилятором, используйте аргумент **-r** .</span><span class="sxs-lookup"><span data-stu-id="a4fae-212">To specify where to place the .rc file and binary files (that contain the metadata resources) that the compiler generates, use the **-r** argument.</span></span> <span data-ttu-id="a4fae-213">Если не указать аргумент **-r** , файлы будут помещены в текущую папку.</span><span class="sxs-lookup"><span data-stu-id="a4fae-213">If you do not specify the **-r** argument, the files are placed in the current folder.</span></span>

<span data-ttu-id="a4fae-214">Компилятор использует базовое имя входного файла в качестве базового имени создаваемых им файлов.</span><span class="sxs-lookup"><span data-stu-id="a4fae-214">The compiler uses the base name of the input file as the base name of the files that it generates.</span></span> <span data-ttu-id="a4fae-215">Чтобы указать базовое имя, используйте аргумент **-z** .</span><span class="sxs-lookup"><span data-stu-id="a4fae-215">To specify a base name, use the **-z** argument.</span></span>

### <a name="arguments-specific-to-message-text-files"></a><span data-ttu-id="a4fae-216">Аргументы, относящиеся к текстовым файлам сообщений</span><span class="sxs-lookup"><span data-stu-id="a4fae-216">Arguments specific to message text files</span></span>

<dl> <dt>

<span data-ttu-id="a4fae-217"><span id="-a"></span><span id="-A"></span>**-a**</span><span class="sxs-lookup"><span data-stu-id="a4fae-217"><span id="-a"></span><span id="-A"></span>**-a**</span></span>
</dt> <dd>

<span data-ttu-id="a4fae-218">Используйте этот аргумент, чтобы указать, что входной файл *filename* содержит содержимое в системной кодовой странице Windows ANSI по умолчанию (CP_ACP).</span><span class="sxs-lookup"><span data-stu-id="a4fae-218">Use this argument to specify that the *filename* input file contains content in the system-default Windows ANSI code page (CP_ACP).</span></span> <span data-ttu-id="a4fae-219">Это значение по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="a4fae-219">This is the default.</span></span> <span data-ttu-id="a4fae-220">Используйте параметр **-u** для Юникода.</span><span class="sxs-lookup"><span data-stu-id="a4fae-220">Use **-u** for Unicode.</span></span> <span data-ttu-id="a4fae-221">Если входной файл содержит BOM, этот аргумент будет проигнорирован.</span><span class="sxs-lookup"><span data-stu-id="a4fae-221">If the input file contains a BOM this argument will be ignored.</span></span>

</dd> <dt>

<span data-ttu-id="a4fae-222"><span id="-A"></span><span id="-a"></span>**-A**</span><span class="sxs-lookup"><span data-stu-id="a4fae-222"><span id="-A"></span><span id="-a"></span>**-A**</span></span>
</dt> <dd>

<span data-ttu-id="a4fae-223">Не рекомендуется.</span><span class="sxs-lookup"><span data-stu-id="a4fae-223">DEPRECATED.</span></span> <span data-ttu-id="a4fae-224">Используйте этот аргумент, чтобы указать, что сообщения в файле Output. bin должны быть ANSI.</span><span class="sxs-lookup"><span data-stu-id="a4fae-224">Use this argument to specify that the messages in the output .bin file should be ANSI.</span></span>

</dd> <dt>

<span data-ttu-id="a4fae-225"><span id="-b"></span><span id="-B"></span>**-б**</span><span class="sxs-lookup"><span data-stu-id="a4fae-225"><span id="-b"></span><span id="-B"></span>**-b**</span></span>
</dt> <dd>

<span data-ttu-id="a4fae-226">Используйте этот аргумент, чтобы компилятор использовал базовое имя входного файла *filename* для имен файлов. bin.</span><span class="sxs-lookup"><span data-stu-id="a4fae-226">Use this argument to have the compiler use the base name of the *filename* input file for the .bin file names.</span></span> <span data-ttu-id="a4fae-227">По умолчанию используется сообщение.</span><span class="sxs-lookup"><span data-stu-id="a4fae-227">The default is to use "MSG".</span></span>

</dd> <dt>

<span data-ttu-id="a4fae-228"><span id="-d"></span><span id="-D"></span>**-d**</span><span class="sxs-lookup"><span data-stu-id="a4fae-228"><span id="-d"></span><span id="-D"></span>**-d**</span></span>
</dt> <dd>

<span data-ttu-id="a4fae-229">Используйте этот аргумент, чтобы использовать десятичные значения для констант и средств серьезности в файле заголовка вместо шестнадцатеричных значений.</span><span class="sxs-lookup"><span data-stu-id="a4fae-229">Use this argument to use decimal values for the Severity and Facility constants in the header file instead of hexadecimal values.</span></span>

</dd> <dt>

<span data-ttu-id="a4fae-230"><span id="-n"></span><span id="-N"></span>**-n**</span><span class="sxs-lookup"><span data-stu-id="a4fae-230"><span id="-n"></span><span id="-N"></span>**-n**</span></span>
</dt> <dd>

<span data-ttu-id="a4fae-231">Используйте этот аргумент, чтобы указать, что сообщения завершаются сразу после текста сообщения.</span><span class="sxs-lookup"><span data-stu-id="a4fae-231">Use this argument to specify that messages terminate immediately after the message body.</span></span> <span data-ttu-id="a4fae-232">По умолчанию тело сообщения прерывается с помощью CR/LF.</span><span class="sxs-lookup"><span data-stu-id="a4fae-232">The default is to terminate the message body with a CR/LF.</span></span>

</dd> <dt>

<span data-ttu-id="a4fae-233"><span id="-o"></span><span id="-O"></span>**-o**</span><span class="sxs-lookup"><span data-stu-id="a4fae-233"><span id="-o"></span><span id="-O"></span>**-o**</span></span>
</dt> <dd>

<span data-ttu-id="a4fae-234">Используйте этот аргумент, чтобы компилятор создавал файл заголовка OLE2, используя определения **HRESULT** вместо кодов состояния.</span><span class="sxs-lookup"><span data-stu-id="a4fae-234">Use this argument to have the compiler generate an OLE2 header file using **HRESULT** definitions instead of status codes.</span></span> <span data-ttu-id="a4fae-235">По умолчанию используются коды состояния.</span><span class="sxs-lookup"><span data-stu-id="a4fae-235">Using status codes is the default.</span></span>

</dd> <dt>

<span data-ttu-id="a4fae-236"><span id="-u"></span><span id="-U"></span>**-u**</span><span class="sxs-lookup"><span data-stu-id="a4fae-236"><span id="-u"></span><span id="-U"></span>**-u**</span></span>
</dt> <dd>

<span data-ttu-id="a4fae-237">Используйте этот аргумент, чтобы указать, что входной файл *filename* содержит содержимое UTF-16LE.</span><span class="sxs-lookup"><span data-stu-id="a4fae-237">Use this argument to specify that the *filename* input file contains UTF-16LE content.</span></span> <span data-ttu-id="a4fae-238">По умолчанию используется содержимое ANSI.</span><span class="sxs-lookup"><span data-stu-id="a4fae-238">The default is ANSI content.</span></span> <span data-ttu-id="a4fae-239">Если входной файл содержит BOM, этот аргумент будет проигнорирован.</span><span class="sxs-lookup"><span data-stu-id="a4fae-239">If the input file contains a BOM this argument will be ignored.</span></span>

</dd> <dt>

<span data-ttu-id="a4fae-240"><span id="-U"></span><span id="-u"></span>**-U**</span><span class="sxs-lookup"><span data-stu-id="a4fae-240"><span id="-U"></span><span id="-u"></span>**-U**</span></span>
</dt> <dd>

<span data-ttu-id="a4fae-241">Используйте этот аргумент, чтобы указать, что сообщения в файле Output. bin должны быть в Юникоде.</span><span class="sxs-lookup"><span data-stu-id="a4fae-241">Use this argument to specify that the messages in the output .bin file should be Unicode.</span></span> <span data-ttu-id="a4fae-242">Это значение по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="a4fae-242">This is the default.</span></span>

</dd> <dt>

<span data-ttu-id="a4fae-243"><span id="-v"></span><span id="-V"></span>**-v**</span><span class="sxs-lookup"><span data-stu-id="a4fae-243"><span id="-v"></span><span id="-V"></span>**-v**</span></span>
</dt> <dd>

<span data-ttu-id="a4fae-244">Используйте этот аргумент для создания подробных выходных данных.</span><span class="sxs-lookup"><span data-stu-id="a4fae-244">Use this argument to generate verbose output.</span></span>

</dd> <dt>

<span data-ttu-id="a4fae-245"><span id="-x_path"></span><span id="-X_PATH"></span>**-x** *путь*</span><span class="sxs-lookup"><span data-stu-id="a4fae-245"><span id="-x_path"></span><span id="-X_PATH"></span>**-x** *path*</span></span>
</dt> <dd>

<span data-ttu-id="a4fae-246">Используйте этот аргумент, чтобы указать папку, в которую компилятор должен поместить файл. dbg C.</span><span class="sxs-lookup"><span data-stu-id="a4fae-246">Use this argument to specify the folder into which you want the compiler to place the .dbg C include file.</span></span> <span data-ttu-id="a4fae-247">Файл. dbg сопоставляет идентификаторы сообщений с их символическими именами.</span><span class="sxs-lookup"><span data-stu-id="a4fae-247">The .dbg file maps message IDs to their symbolic names.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="a4fae-248">Комментарии</span><span class="sxs-lookup"><span data-stu-id="a4fae-248">Remarks</span></span>

<span data-ttu-id="a4fae-249">Аргументы **-A** и **-MOF** являются устаревшими и будут удалены в будущем.</span><span class="sxs-lookup"><span data-stu-id="a4fae-249">The **-A** and **-mof** arguments are deprecated and will be removed in the future.</span></span>

<span data-ttu-id="a4fae-250">Компилятор принимает в качестве входных данных файл манифеста (. Man) или текст сообщения (. MC) и создает следующие файлы:</span><span class="sxs-lookup"><span data-stu-id="a4fae-250">The compiler accepts as input a manifest (.man) file or a message text (.mc) file and generates the following files:</span></span>

-   <span data-ttu-id="a4fae-251">*filename*. h</span><span class="sxs-lookup"><span data-stu-id="a4fae-251">*filename*.h</span></span>

    <span data-ttu-id="a4fae-252">Заголовочный файл C/C++, который содержит дескрипторы событий, GUID поставщика и имена символов, на которые вы ссылаетесь в приложении.</span><span class="sxs-lookup"><span data-stu-id="a4fae-252">A C/C++ header file that contains the event descriptors, provider GUID, and symbol names that you reference in your application.</span></span>

-   <span data-ttu-id="a4fae-253">*имя файла* TEMP. bin</span><span class="sxs-lookup"><span data-stu-id="a4fae-253">*filename* TEMP.bin</span></span>

    <span data-ttu-id="a4fae-254">Двоичный файл ресурсов, содержащий метаданные поставщика и события.</span><span class="sxs-lookup"><span data-stu-id="a4fae-254">A binary resource file that contains the provider and event metadata.</span></span> <span data-ttu-id="a4fae-255">Это ресурс шаблона, который обозначается ВРЕМЕНным суффиксом базового имени файла.</span><span class="sxs-lookup"><span data-stu-id="a4fae-255">This is the template resource, which is signified by the TEMP suffix of the base name of the file.</span></span>

-   <span data-ttu-id="a4fae-256">Msg00001. bin</span><span class="sxs-lookup"><span data-stu-id="a4fae-256">Msg00001.bin</span></span>

    <span data-ttu-id="a4fae-257">Двоичный файл ресурсов для каждого указанного языка (например, если манифест содержит строки сообщений в EN-US и fr-FR, компилятор создаст Msg00001. bin и Msg00002. bin).</span><span class="sxs-lookup"><span data-stu-id="a4fae-257">A binary resource file for each language that you specify (for example, if your manifest contains message strings in en-US and fr-FR, the compiler would generate Msg00001.bin and Msg00002.bin).</span></span>

-   <span data-ttu-id="a4fae-258">*имя файла*. RC</span><span class="sxs-lookup"><span data-stu-id="a4fae-258">*filename*.rc</span></span>

    <span data-ttu-id="a4fae-259">Скрипт компилятора ресурсов, содержащий инструкции для включения каждого файла. bin в качестве ресурса.</span><span class="sxs-lookup"><span data-stu-id="a4fae-259">A resource compiler script that contains the statements to include each .bin file as a resource.</span></span>

<span data-ttu-id="a4fae-260">Для аргументов, которые принимают путь, путь может быть абсолютным, относительным или UNC-путем и содержать переменные среды.</span><span class="sxs-lookup"><span data-stu-id="a4fae-260">For arguments that take a path, the path can be an absolute, relative, or UNC path and it can contain environment variables.</span></span>

<span data-ttu-id="a4fae-261">**До версии MC 1.12.7051:** Компилятор не разрешает относительные пути или переменные среды.</span><span class="sxs-lookup"><span data-stu-id="a4fae-261">**Prior to MC version 1.12.7051:** The compiler does not allow relative paths or environment variables.</span></span>

<span data-ttu-id="a4fae-262">Windows SDK включает компилятор (mc.exe) в \\ папку bin.</span><span class="sxs-lookup"><span data-stu-id="a4fae-262">The Windows SDK includes the compiler (mc.exe) in the \\Bin folder.</span></span>

## <a name="examples"></a><span data-ttu-id="a4fae-263">Примеры</span><span class="sxs-lookup"><span data-stu-id="a4fae-263">Examples</span></span>

<span data-ttu-id="a4fae-264">В следующем примере манифест компилируется с использованием параметров компилятора по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="a4fae-264">The following example compiles a manifest using the compiler defaults.</span></span>

``` syntax
mc spooler.man
```

<span data-ttu-id="a4fae-265">В следующем примере компилируется манифест и размещаются файлы заголовков и ресурсов в указанных папках.</span><span class="sxs-lookup"><span data-stu-id="a4fae-265">The following example compiles the manifest and places the header and resource files in the specified folders.</span></span>

``` syntax
mc -h <pathgoeshere> -r <pathgoeshere> spooler.man
```

## <a name="requirements"></a><span data-ttu-id="a4fae-266">Требования</span><span class="sxs-lookup"><span data-stu-id="a4fae-266">Requirements</span></span>

| <span data-ttu-id="a4fae-267">Требование</span><span class="sxs-lookup"><span data-stu-id="a4fae-267">Requirement</span></span> | <span data-ttu-id="a4fae-268">Значение</span><span class="sxs-lookup"><span data-stu-id="a4fae-268">Value</span></span> |
|--------------------------|-------------------------------------------------|
| <span data-ttu-id="a4fae-269">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="a4fae-269">Minimum supported client</span></span> | <span data-ttu-id="a4fae-270">Windows 2000 Professional \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="a4fae-270">Windows 2000 Professional \[desktop apps only\]</span></span> |
| <span data-ttu-id="a4fae-271">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="a4fae-271">Minimum supported server</span></span> | <span data-ttu-id="a4fae-272">Windows 2000 Server \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="a4fae-272">Windows 2000 Server \[desktop apps only\]</span></span>       |
