---
title: Требования к препроцессору C-препроцессор для MIDL
description: Эта страница относится только к разработчикам, имеющим определенные причины для замены препроцессора Microsoft C/C++ в качестве препроцессора, используемого MIDL, или для разработчиков, которые должны указывать настраиваемые параметры препроцессора.
ms.assetid: 1dd5eef4-5ea4-4958-8f53-9a95c0ccbf3e
keywords:
- MIDL компилятора MIDL, C-препроцессор, требования
- C-препроцессор MIDL, требования
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b49c4e0c086a52eda2705d72cf2a2ff22c759290
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/16/2019
ms.locfileid: "103986703"
---
# <a name="c-preprocessor-requirements-for-midl"></a><span data-ttu-id="8416b-105">Требования к препроцессору C-препроцессор для MIDL</span><span class="sxs-lookup"><span data-stu-id="8416b-105">C-Preprocessor Requirements for MIDL</span></span>

<span data-ttu-id="8416b-106">Эта страница относится только к разработчикам, имеющим определенные причины для замены препроцессора Microsoft C/C++ в качестве препроцессора, используемого MIDL, или для разработчиков, которые должны указывать настраиваемые параметры препроцессора.</span><span class="sxs-lookup"><span data-stu-id="8416b-106">This page applies only to developers who have specific reasons to replace the Microsoft C/C++ preprocessor as the preprocessor used by MIDL, or to developers who must specify customized preprocessor switches.</span></span> <span data-ttu-id="8416b-107">Для переопределения поведения компилятора по умолчанию используются параметры MIDL, [**/КПП \_ cmd**](-cpp-cmd.md), [**/КПП \_ OPT**](-cpp-opt.md)и [**/но \_ cpp**](-no-cpp-nocpp.md) .</span><span class="sxs-lookup"><span data-stu-id="8416b-107">The MIDL switches [**/cpp\_cmd**](-cpp-cmd.md), [**/cpp\_opt**](-cpp-opt.md), and [**/no\_cpp**](-no-cpp-nocpp.md) are used to override the default behavior of the compiler.</span></span> <span data-ttu-id="8416b-108">Обычно нет причин для замены препроцессора Microsoft C/C++, а также для указания настраиваемых параметров препроцессора.</span><span class="sxs-lookup"><span data-stu-id="8416b-108">There is typically no reason to replace the Microsoft C/C++ preprocessor, nor to specify customized preprocessor switches.</span></span>

<span data-ttu-id="8416b-109">Компилятор MIDL использует препроцессор C во время первоначальной обработки IDL-файла.</span><span class="sxs-lookup"><span data-stu-id="8416b-109">The MIDL compiler uses a C preprocessor during initial processing of the IDL file.</span></span> <span data-ttu-id="8416b-110">Среда сборки, используемая при компиляции IDL-файлов, связана с препроцессором C/C++ по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="8416b-110">The build environment used when compiling the IDL files is associated with a default C/C++ preprocessor.</span></span> <span data-ttu-id="8416b-111">При использовании другого препроцессора параметр компилятора MIDL [**/КПП \_ cmd**](-cpp-cmd.md) позволяет переопределить имя препроцессора по умолчанию C/C++:</span><span class="sxs-lookup"><span data-stu-id="8416b-111">If a different preprocessor is to be used, the MIDL compiler switch [**/cpp\_cmd**](-cpp-cmd.md) enables an override of the default C/C++-preprocessor name:</span></span>

``` syntax
midl /cpp_cmd preprocessor_name filename
```

<dl> <dt>

<span data-ttu-id="8416b-112"><span id="preprocessor_name"></span><span id="PREPROCESSOR_NAME"></span>*имя препроцессора \_*</span><span class="sxs-lookup"><span data-stu-id="8416b-112"><span id="preprocessor_name"></span><span id="PREPROCESSOR_NAME"></span>*preprocessor\_name*</span></span>
</dt> <dd>

<span data-ttu-id="8416b-113">Указывает имя препроцессора, используемого MIDL.</span><span class="sxs-lookup"><span data-stu-id="8416b-113">Specifies the name of the preprocessor to be used by MIDL.</span></span> <span data-ttu-id="8416b-114">Может быть указан с путем к двоичному файлу.</span><span class="sxs-lookup"><span data-stu-id="8416b-114">May be specified with a path to the binary.</span></span> <span data-ttu-id="8416b-115">Расширение EXE является необязательным.</span><span class="sxs-lookup"><span data-stu-id="8416b-115">The .exe extension is optional.</span></span>

</dd> <dt>

<span data-ttu-id="8416b-116"><span id="filename"></span><span id="FILENAME"></span>*файлов*</span><span class="sxs-lookup"><span data-stu-id="8416b-116"><span id="filename"></span><span id="FILENAME"></span>*filename*</span></span>
</dt> <dd>

<span data-ttu-id="8416b-117">Указывает имя IDL-файла.</span><span class="sxs-lookup"><span data-stu-id="8416b-117">Specifies the name of the IDL file.</span></span>

</dd> </dl>

-   <span data-ttu-id="8416b-118">Компилятор MIDL должен иметь любые препроцессоры для отслеживания следующих соглашений:</span><span class="sxs-lookup"><span data-stu-id="8416b-118">The MIDL compiler expects any preprocessor to observe the following conventions:</span></span>
-   <span data-ttu-id="8416b-119">Входной файл указывается в качестве последнего аргумента в командной строке.</span><span class="sxs-lookup"><span data-stu-id="8416b-119">The input file is specified as the last argument on the command line.</span></span>
-   <span data-ttu-id="8416b-120">Препроцессор должен перенаправить выходные данные на стандартное выходное устройство stdout.</span><span class="sxs-lookup"><span data-stu-id="8416b-120">The preprocessor must redirect output to the standard output device, stdout.</span></span>
-   <span data-ttu-id="8416b-121">В потоке вывода препроцессора имеются директивы **\# line** , позволяющие улучшить сообщения диагностики.</span><span class="sxs-lookup"><span data-stu-id="8416b-121">In the output stream of the preprocessor, the **\#line** directives are present to enable better diagnostic messages.</span></span>
-   <span data-ttu-id="8416b-122">Директивы line являются единственными директивами препроцессора в выходном потоке.</span><span class="sxs-lookup"><span data-stu-id="8416b-122">The line directives are the only preprocessor directives in the output stream.</span></span>

<span data-ttu-id="8416b-123">MIDL предполагает, что порожденный препроцессор удалил все директивы препроцессора из входного потока компилятора, за исключением вхождений директивы line, необходимых для определения местоположения источника в сообщениях компилятора.</span><span class="sxs-lookup"><span data-stu-id="8416b-123">MIDL assumes that the spawned preprocessor has removed all preprocessor directives from the input stream of the compiler, with the exception of the occurrences of the line directive necessary for pinpointing source location in compiler messages.</span></span> <span data-ttu-id="8416b-124">При указании препроцессора, отличного от препроцессора Microsoft C/C++, или при задании параметров препроцессора с помощью параметра [**/КПП \_ OPT**](-cpp-opt.md) , следует указать соответствующий параметр препроцессора, который помещает директивы line во входной поток компилятора.</span><span class="sxs-lookup"><span data-stu-id="8416b-124">When indicating a preprocessor different from the Microsoft C/C++ preprocessor, or when specifying preprocessor options with the [**/cpp\_opt**](-cpp-opt.md) switch, specifying an appropriate preprocessor option that puts the line directives in the input stream of the compiler is required.</span></span> <span data-ttu-id="8416b-125">Например, для препроцессора Microsoft C/C++ необходимо использовать параметр **/e** :</span><span class="sxs-lookup"><span data-stu-id="8416b-125">For example, for the Microsoft C/C++ preprocessor the **/E** option would have to be used:</span></span>

``` syntax
midl /cpp_cmd cl.exe /cpp_opt "/E" file.idl
```

<span data-ttu-id="8416b-126">Директива **\# line** принимается MIDL в одной из следующих форм:</span><span class="sxs-lookup"><span data-stu-id="8416b-126">The **\#line** directive is accepted by MIDL in one of the following forms:</span></span>

``` syntax
#line digit-sequence "filename" new-line
 
# digit-sequence "filename" new-line
```

<span data-ttu-id="8416b-127">Полное описание директивы line и других директив препроцессора см. в документации по используемому компилятору C.</span><span class="sxs-lookup"><span data-stu-id="8416b-127">For a complete description of the line directive and other preprocessor directives, see the documentation for the C-compiler being used.</span></span>

<span data-ttu-id="8416b-128">MIDL принимает только директиву препроцессора Line.</span><span class="sxs-lookup"><span data-stu-id="8416b-128">MIDL accepts only the line preprocessor directive.</span></span> <span data-ttu-id="8416b-129">Таким образом, если используется параметр [**/но \_ cpp**](-no-cpp-nocpp.md) , входной файл не должен содержать другие директивы препроцессора, или входной файл должен быть ОБРАБОТАН до вызова MIDL.</span><span class="sxs-lookup"><span data-stu-id="8416b-129">Therefore, if the [**/no\_cpp**](-no-cpp-nocpp.md) switch is used, the input file must not have other preprocessor directives, or the input file must have been processed prior to invoking MIDL.</span></span>

<span data-ttu-id="8416b-130">Дополнительные сведения см. [в разделе Работа с \# определениями в IDL-файлах](dealing-with-defines-in-idl-files-2.md).</span><span class="sxs-lookup"><span data-stu-id="8416b-130">For more information, see [Dealing with \#defines in IDL Files](dealing-with-defines-in-idl-files-2.md).</span></span>

 

 




