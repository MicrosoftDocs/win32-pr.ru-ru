---
title: Сохранение выходных данных препроцессора
description: Просмотр выходных данных препроцессора может быть эффективным методом устранения неполадок, например при возникновении неверного синтаксиса IDL, C или C-или в результате поддельных значений в командной строке MIDL. в этом случае возникает ошибка MIDL Reporting сложной Errors.
ms.assetid: 79c53f0c-c179-4731-a2c3-a1022d378e7b
keywords:
- MIDL компилятора MIDL, сохранение выходных данных препроцессора
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 49ca1e07658fb2da525999e396b7c3da27add385
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/16/2019
ms.locfileid: "104411065"
---
# <a name="saving-preprocessor-output"></a><span data-ttu-id="52112-104">Сохранение выходных данных препроцессора</span><span class="sxs-lookup"><span data-stu-id="52112-104">Saving Preprocessor Output</span></span>

<span data-ttu-id="52112-105">Просмотр выходных данных препроцессора может быть эффективным методом устранения неполадок, например при возникновении неверного синтаксиса IDL, C или C-или в результате поддельных значений в командной строке MIDL. в этом случае возникает ошибка MIDL Reporting сложной Errors.</span><span class="sxs-lookup"><span data-stu-id="52112-105">Viewing preprocessor output can be an effective troubleshooting method, such as when invalid IDL, C, or C-preprocessor syntax occurs, or when bogus -D values on the MIDL command line result in MIDL reporting arcane errors.</span></span> <span data-ttu-id="52112-106">Разработчикам также может потребоваться изучить выходные данные препроцессора, чтобы определить, какие файлы и определения присутствовали во входном потоке компилятора, например в случае, если трудно разрешить конфликт переопределений типов.</span><span class="sxs-lookup"><span data-stu-id="52112-106">Developers may also want to examine preprocessor output to determine which files and definitions were present in the compiler input stream, such as when a difficult case of type redefinition conflict must be resolved.</span></span> <span data-ttu-id="52112-107">Или реже, некоторым разработчикам может потребоваться принудительно использовать закрытые коммутаторы на препроцессоре с помощью [**/КПП \_ OPT**](-cpp-opt.md)или, возможно, потребуется посмотреть, как работают эти параметры.</span><span class="sxs-lookup"><span data-stu-id="52112-107">Or less commonly, certain developers may want to force private switches on the preprocessor with [**/cpp\_opt**](-cpp-opt.md), or may want to see how the switches work.</span></span>

<span data-ttu-id="52112-108">Самый простой и самый ненавязчивый способ получить предварительно обработанные файлы из компиляции MIDL — использовать параметр [**-савепп**](-savepp.md) .</span><span class="sxs-lookup"><span data-stu-id="52112-108">The easiest and the least obtrusive way to obtain the preprocessed files from a MIDL compile run is to use the [**-savePP**](-savepp.md) switch.</span></span> <span data-ttu-id="52112-109">Параметр **-савепп** просто предотвращает удаление временных файлов, которые препроцессор передает в MIDL, с помощью MIDL.</span><span class="sxs-lookup"><span data-stu-id="52112-109">The **-savePP** switch simply prevents MIDL from deleting the temporary files that the preprocessor passes back to MIDL.</span></span> <span data-ttu-id="52112-110">Рассмотрим следующий пример.</span><span class="sxs-lookup"><span data-stu-id="52112-110">Consider the following:</span></span>

<span data-ttu-id="52112-111">**MIDL-Савепп-ID: \\ NT \\ Public \\ SDK \\ Inc-Днтенв = 1-оикф-env Win32 заглушек. idl**</span><span class="sxs-lookup"><span data-stu-id="52112-111">**midl -savePP -Id:\\nt\\public\\sdk\\inc -DNTENV=1 -Oicf -env win32 stub.idl**</span></span>

<span data-ttu-id="52112-112">Эта директива компилирует файл заглушек. idl, но сохраняет все файлы препроцессора.</span><span class="sxs-lookup"><span data-stu-id="52112-112">This directive compiles Stub.idl, yet preserves all preprocessor files.</span></span>

> [!Note]  
> <span data-ttu-id="52112-113">MIDL порождает отдельные запуски препроцессора для файлов IDL и ACF (если они есть), а также для каждого импортированного файла.</span><span class="sxs-lookup"><span data-stu-id="52112-113">MIDL spawns separate preprocessor runs for IDL and ACF file (if present) as well as for every imported file.</span></span>

 

<span data-ttu-id="52112-114">Для компиляции DCOM обычно создаются несколько файлов препроцессора, даже если они обрабатываются MIDL как виртуальный смежный входной поток.</span><span class="sxs-lookup"><span data-stu-id="52112-114">For a DCOM compile, several preprocessor files are typically produced, even though they are processed by MIDL as a virtual contiguous input stream.</span></span> <span data-ttu-id="52112-115">В типичной среде программирования Windows временные файлы можно найти во временном каталоге в виде имен файлов, таких как MID \* . tmp.</span><span class="sxs-lookup"><span data-stu-id="52112-115">In a typical Windows programming environment, the temporary files can be found in the Temp directory as file names such as MID\*.tmp.</span></span> <span data-ttu-id="52112-116">При сохранении выходных данных препроцессора рекомендуется следить за последними файлами в каталоге Temp, чтобы узнать, какие файлы связаны с выполняемым препроцессором.</span><span class="sxs-lookup"><span data-stu-id="52112-116">If preserving preprocessor output, it is good practice to watch for recent files in the Temp directory to identify which files are associated with which preprocessor run.</span></span>

<span data-ttu-id="52112-117">В простых случаях, например, когда скомпилированный IDL-файл не импортирует другие файлы напрямую или косвенно или при проверке файла верхнего уровня, препроцессор можно вызвать напрямую.</span><span class="sxs-lookup"><span data-stu-id="52112-117">In simple cases, such as when the compiled IDL file does not import other files directly or indirectly, or when examining the top-level file, the preprocessor can be invoked directly.</span></span> <span data-ttu-id="52112-118">Непосредственное исполнение препроцессора C/C++ позволяет выявить ошибки, маскированные или запутать MIDL.</span><span class="sxs-lookup"><span data-stu-id="52112-118">Executing C/C++ preprocessor directly can reveal errors masked or confused by MIDL.</span></span> <span data-ttu-id="52112-119">Например, для ранее заключенной в кавычки строки MIDL можно использовать следующие две команд препроцессора:</span><span class="sxs-lookup"><span data-stu-id="52112-119">For example, the following two preprocessor command lines can be used for the previously quoted MIDL line:</span></span>

<span data-ttu-id="52112-120">**CL/E/nologo-ID: \\ net \\ Public \\ SDK \\ Inc-днтенв = 1 заглушка. idl > заглушек. PP**</span><span class="sxs-lookup"><span data-stu-id="52112-120">**cl /E /nologo -Id:\\nt\\public\\sdk\\inc -DNTENV=1 stub.idl > stub.pp**</span></span>

<span data-ttu-id="52112-121">**CL/E/P-ID: \\ \\ пакет общедоступного \\ пакета SDK \\ Inc-днтенв = 1 заглушка. idl**</span><span class="sxs-lookup"><span data-stu-id="52112-121">**cl /E /P -Id:\\nt\\public\\sdk\\inc -DNTENV=1 stub.idl**</span></span>

<span data-ttu-id="52112-122">В первом из этих двух примеров параметр **/e** [**/nologo**](-nologo.md) — это ключи, которые добавляются MIDL при вызове препроцессора.</span><span class="sxs-lookup"><span data-stu-id="52112-122">In the first of these two examples, **/E** [**/nologo**](-nologo.md) are the switches that MIDL adds when invoking the preprocessor.</span></span> <span data-ttu-id="52112-123">Выходные данные препроцессора отправляются в stdout (экран) и поэтому требуют перенаправления в файл для проверки.</span><span class="sxs-lookup"><span data-stu-id="52112-123">The preprocessor output is sent to stdout (the screen), and therefore requires redirection to a file for examination.</span></span> <span data-ttu-id="52112-124">Во втором из этих примеров параметр **/p** направляет препроцессору перенаправление выходных данных в \* файл. i. в этом случае файл заглушки будет создан в текущем каталоге.</span><span class="sxs-lookup"><span data-stu-id="52112-124">In the second of these examples, **/P** directs the preprocessor to redirect the output to a \*.i file; in this case a Stub.i file would be created in the current directory.</span></span>

<span data-ttu-id="52112-125">Параметр [**/КПП \_ OPT**](-cpp-opt.md) также можно использовать для получения предварительно обработанного файла, но он является сложным и подключается к упомянутым выше методам.</span><span class="sxs-lookup"><span data-stu-id="52112-125">The [**/cpp\_opt**](-cpp-opt.md) switch can also be used to obtain a preprocessed file, but is difficult and inferior to the previously mentioned methods.</span></span> <span data-ttu-id="52112-126">В следующем примере также создается файл заглушки. i, как в предыдущем примере.</span><span class="sxs-lookup"><span data-stu-id="52112-126">The following example also produces a Stub.i file, as did the previous example.</span></span> <span data-ttu-id="52112-127">В следующем примере необходимы кавычки:</span><span class="sxs-lookup"><span data-stu-id="52112-127">The quotes in the following example are essential:</span></span>

<span data-ttu-id="52112-128">**MIDL-Оикф-Win32-cpp \_ OPT "/E/p-ID: \\ net \\ Public \\ SDK \\ Inc-днтенв = 1" заглушка. idl**</span><span class="sxs-lookup"><span data-stu-id="52112-128">**Midl -Oicf -win32 -cpp\_opt "/E /P -Id:\\nt\\public\\sdk\\inc -DNTENV=1" stub.idl**</span></span>

 

 




