---
title: Компиляция разметки ленты
description: Чтобы платформа Windows Ribbon использовала файл разметки ленты, файл разметки должен быть скомпилирован в файл ресурсов в двоичном формате.
ms.assetid: ef9fea92-8c67-461d-9d74-2e259e407fb0
keywords:
- Лента Windows, компиляция разметки
- Лента, компиляция разметки
- Лента Windows, Рабочий процесс компилятора
- Лента, Рабочий процесс компилятора
- Лента Windows, компилятор команд пользовательского интерфейса (UICC.exe)
- Ribbon, компилятор команд пользовательского интерфейса (UICC.exe)
- Компилятор команд пользовательского интерфейса (UICC.exe)
- UICC.exe (компилятор команд пользовательского интерфейса)
- Компиляция разметки ленты Windows
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f671e03d7d3a941f1c97891d87c170e65e326d70
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/16/2019
ms.locfileid: "104532333"
---
# <a name="compiling-ribbon-markup"></a><span data-ttu-id="79af3-112">Компиляция разметки ленты</span><span class="sxs-lookup"><span data-stu-id="79af3-112">Compiling Ribbon Markup</span></span>

<span data-ttu-id="79af3-113">Чтобы платформа Windows Ribbon использовала файл [разметки ленты](windowsribbon-schema.md) , файл разметки должен быть скомпилирован в файл ресурсов в двоичном формате.</span><span class="sxs-lookup"><span data-stu-id="79af3-113">For the Windows Ribbon framework to consume the [Ribbon markup](windowsribbon-schema.md) file, the markup file must be compiled into a binary format resource file.</span></span> <span data-ttu-id="79af3-114">Для этой цели в составе пакета средств разработки программного обеспечения (SDK) для Windows входит выделенный компилятор разметки, компилятор команд пользовательского интерфейса (УИКК) (7,0 или более поздней версии).</span><span class="sxs-lookup"><span data-stu-id="79af3-114">A dedicated markup compiler, the UI Command Compiler (UICC), is included with the Windows Software Development Kit (SDK) (7.0 or later) for this purpose.</span></span> <span data-ttu-id="79af3-115">Помимо компиляции двоичной версии разметки, УИКК создает файл заголовка определения идентификатора (. h), который предоставляет все элементы разметки для хост-приложения ленты и файл ресурсов (. RC), который используется для связывания ресурсов Image и String с ведущим приложением во время сборки.</span><span class="sxs-lookup"><span data-stu-id="79af3-115">In addition to compiling the binary version of the markup, the UICC generates an ID definition header (.h) file that exposes all markup elements to the Ribbon host application and a resource (.rc) file that is used to link image and string resources to the host application at build time.</span></span>

-   [<span data-ttu-id="79af3-116">Рабочий процесс компилятора</span><span class="sxs-lookup"><span data-stu-id="79af3-116">Compiler Workflow</span></span>](#compiler-workflow)
-   [<span data-ttu-id="79af3-117">Синтаксис командной строки</span><span class="sxs-lookup"><span data-stu-id="79af3-117">Command-Line Syntax</span></span>](#command-line-syntax)
    -   [<span data-ttu-id="79af3-118">Аргументы и параметры</span><span class="sxs-lookup"><span data-stu-id="79af3-118">Arguments and Options</span></span>](#arguments-and-options)
    -   [<span data-ttu-id="79af3-119">Пример</span><span class="sxs-lookup"><span data-stu-id="79af3-119">Example</span></span>](#example)
-   [<span data-ttu-id="79af3-120">См. также</span><span class="sxs-lookup"><span data-stu-id="79af3-120">Related topics</span></span>](#related-topics)

## <a name="compiler-workflow"></a><span data-ttu-id="79af3-121">Рабочий процесс компилятора</span><span class="sxs-lookup"><span data-stu-id="79af3-121">Compiler Workflow</span></span>

<span data-ttu-id="79af3-122">Рабочий процесс компилятора разметки ленты показан на следующей схеме.</span><span class="sxs-lookup"><span data-stu-id="79af3-122">The workflow of the Ribbon markup compiler is illustrated in the following diagram.</span></span>

![Схема, показывающая рабочий процесс компилятора разметки ленты.](images/overviews/overviews-intentcl.png)

## <a name="command-line-syntax"></a><span data-ttu-id="79af3-124">Синтаксис командной строки</span><span class="sxs-lookup"><span data-stu-id="79af3-124">Command-Line Syntax</span></span>

<span data-ttu-id="79af3-125">Синтаксис командной строки для компилятора разметки ленты показан в следующем примере.</span><span class="sxs-lookup"><span data-stu-id="79af3-125">The command-line syntax for the Ribbon markup compiler is shown in the following example.</span></span>


```
UICC <ribbonFile> <binaryFile> [options]
```



### <a name="arguments-and-options"></a><span data-ttu-id="79af3-126">Аргументы и параметры</span><span class="sxs-lookup"><span data-stu-id="79af3-126">Arguments and Options</span></span>

<span data-ttu-id="79af3-127">Аргументы и параметры для этого средства описаны в следующей таблице.</span><span class="sxs-lookup"><span data-stu-id="79af3-127">The arguments and options for this tool are described in the following table.</span></span>

> [!Note]  
> <span data-ttu-id="79af3-128">Указанные параметры командной строки должны быть указаны в указанном порядке.</span><span class="sxs-lookup"><span data-stu-id="79af3-128">The command-line options listed must be specified in the order given.</span></span>

 



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="79af3-129">Параметр</span><span class="sxs-lookup"><span data-stu-id="79af3-129">Option</span></span></th>
<th><span data-ttu-id="79af3-130">Описание</span><span class="sxs-lookup"><span data-stu-id="79af3-130">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="79af3-131">/Header<headerFile></span><span class="sxs-lookup"><span data-stu-id="79af3-131">/header:<headerFile></span></span></td>
<td><span data-ttu-id="79af3-132">Создайте заголовочный файл <headerFile> с именем, содержащий символы ресурса идентификатора команды разметки.</span><span class="sxs-lookup"><span data-stu-id="79af3-132">Generate a header file called <headerFile> that contains the markup Command ID resource symbols.</span></span> <span data-ttu-id="79af3-133">Если этот параметр опущен, файл заголовка не создается.</span><span class="sxs-lookup"><span data-stu-id="79af3-133">If omitted, a header file is not generated.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="79af3-134">/RES<resourceFile></span><span class="sxs-lookup"><span data-stu-id="79af3-134">/res:<resourceFile></span></span></td>
<td><span data-ttu-id="79af3-135">Создайте файл ресурсов с именем <resourceFile> , который связывает все ресурсы изображения и строки, двоичный файл разметки и заголовочный файл с ведущим приложением во время сборки.</span><span class="sxs-lookup"><span data-stu-id="79af3-135">Generate a resource file called <resourceFile> that links all image and string resources, the binary markup file, and the header file to the host application at build time.</span></span> <span data-ttu-id="79af3-136">Если этот параметр опущен, файл ресурсов не создается.</span><span class="sxs-lookup"><span data-stu-id="79af3-136">If omitted, a resource file is not generated.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="79af3-137">/Name<ribbonName></span><span class="sxs-lookup"><span data-stu-id="79af3-137">/name:<ribbonName></span></span></td>
<td><span data-ttu-id="79af3-138">Имя ресурса для двоичного файла разметки, который заносится в журнал <resourceFile> .</span><span class="sxs-lookup"><span data-stu-id="79af3-138">The resource name for the binary markup file that is logged in the <resourceFile>.</span></span> <span data-ttu-id="79af3-139">Значение по умолчанию — APPLICATION_RIBBON.</span><span class="sxs-lookup"><span data-stu-id="79af3-139">The default is APPLICATION_RIBBON.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="79af3-140">/W{0\1\2}</span><span class="sxs-lookup"><span data-stu-id="79af3-140">/W{0\1\2}</span></span></td>
<td><span data-ttu-id="79af3-141">Фильтрация сообщений о событиях на основе серьезности.</span><span class="sxs-lookup"><span data-stu-id="79af3-141">Filter the event messages based on severity.</span></span> 
<table>
<tbody>
<tr class="odd">
<td><span data-ttu-id="79af3-142">0</span><span class="sxs-lookup"><span data-stu-id="79af3-142">0</span></span><br/></td>
<td><span data-ttu-id="79af3-143">Только сообщения об ошибках.</span><span class="sxs-lookup"><span data-stu-id="79af3-143">Error messages only.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="79af3-144">1</span><span class="sxs-lookup"><span data-stu-id="79af3-144">1</span></span><br/></td>
<td><span data-ttu-id="79af3-145">Только сообщения об ошибках и предупреждения.</span><span class="sxs-lookup"><span data-stu-id="79af3-145">Error and Warning messages only.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="79af3-146"><strong>2</strong></span><span class="sxs-lookup"><span data-stu-id="79af3-146"><strong>2</strong></span></span><br/></td>
<td><span data-ttu-id="79af3-147">По умолчанию.</span><span class="sxs-lookup"><span data-stu-id="79af3-147">Default.</span></span> <br/> <span data-ttu-id="79af3-148">Ошибки, предупреждения и информационные сообщения.</span><span class="sxs-lookup"><span data-stu-id="79af3-148">Error, Warning, and Informational messages.</span></span><br/></td>
</tr>
</tbody>
</table>

<p> </p></td>
</tr>
</tbody>
</table>



 

### <a name="example"></a><span data-ttu-id="79af3-149">Пример</span><span class="sxs-lookup"><span data-stu-id="79af3-149">Example</span></span>

<span data-ttu-id="79af3-150">В следующем примере показано, как использовать компилятор разметки ленты для создания типичного набора файлов ресурсов для приложения на ленте.</span><span class="sxs-lookup"><span data-stu-id="79af3-150">The following example demonstrates how to use the Ribbon markup compiler to generate a typical set of resource files for a Ribbon application.</span></span>

`UICC.exe RibbonMarkup.xml RibbonMarkup.bml /header:RibbonIds.h /res:RibbonUI.rc`

## <a name="related-topics"></a><span data-ttu-id="79af3-151">См. также</span><span class="sxs-lookup"><span data-stu-id="79af3-151">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="79af3-152">Объявление команд и элементов управления с разметкой ленты</span><span class="sxs-lookup"><span data-stu-id="79af3-152">Declaring Commands and Controls with Ribbon Markup</span></span>](windowsribbon-schema.md)
</dt> <dt>

[<span data-ttu-id="79af3-153">Создание приложения для ленты</span><span class="sxs-lookup"><span data-stu-id="79af3-153">Creating a Ribbon Application</span></span>](windowsribbon-stepbystep.md)
</dt> </dl>

 

 





