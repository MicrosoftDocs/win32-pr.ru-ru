---
title: " include, директива"
description: Директива препроцессора, которая вставляет содержимое указанного файла в исходную программу в точке, где отображается директива.
ms.assetid: 24796d89-5690-469b-950e-df56783aa05a
keywords:
- включить директиву HLSL
topic_type:
- apiref
api_name:
- include Directive
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: a844459234200ca99233eb3f64a2a1c30449cdcc
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "104997086"
---
# <a name="include-directive"></a><span data-ttu-id="77df2-104">\#include, директива</span><span class="sxs-lookup"><span data-stu-id="77df2-104">\#include Directive</span></span>

<span data-ttu-id="77df2-105">Директива препроцессора, которая вставляет содержимое указанного файла в исходную программу в точке, где отображается директива.</span><span class="sxs-lookup"><span data-stu-id="77df2-105">Preprocessor directive that inserts the contents of the specified file into the source program at the point where the directive appears.</span></span>


| <span data-ttu-id="77df2-106">\#включить "*ИмяФайла*"</span><span class="sxs-lookup"><span data-stu-id="77df2-106">\#include "*filename*"</span></span>       |
|------------------------------|
| <span data-ttu-id="77df2-107">\#включить *имя файла* <></span><span class="sxs-lookup"><span data-stu-id="77df2-107">\#include <*filename*></span></span> |

## <a name="parameters"></a><span data-ttu-id="77df2-108">Параметры</span><span class="sxs-lookup"><span data-stu-id="77df2-108">Parameters</span></span>

| <span data-ttu-id="77df2-109">Элемент</span><span class="sxs-lookup"><span data-stu-id="77df2-109">Item</span></span> | <span data-ttu-id="77df2-110">Описание</span><span class="sxs-lookup"><span data-stu-id="77df2-110">Description</span></span> |
|------|-------------|
| <span data-ttu-id="77df2-111">*filename*</span><span class="sxs-lookup"><span data-stu-id="77df2-111">*filename*</span></span> | <span data-ttu-id="77df2-112">Имя файла для включения, при необходимости предшествующее спецификации каталога.</span><span class="sxs-lookup"><span data-stu-id="77df2-112">Filename of the file to include, optionally preceded by a directory specification.</span></span> <span data-ttu-id="77df2-113">Имя файла должно содержать существующий файл.</span><span class="sxs-lookup"><span data-stu-id="77df2-113">The filename must specify an existing file.</span></span> |

## <a name="remarks"></a><span data-ttu-id="77df2-114">Примечания</span><span class="sxs-lookup"><span data-stu-id="77df2-114">Remarks</span></span>

<span data-ttu-id="77df2-115">\#Директива include приводит к замене директивы всем содержимым указанного файла.</span><span class="sxs-lookup"><span data-stu-id="77df2-115">The \#include directive causes replacement of the directive by the entire contents of the specified file.</span></span> <span data-ttu-id="77df2-116">Препроцессор прекращает поиск, как только находит файл с указанным именем; Если указать полную, однозначную спецификацию пути для файла, препроцессор будет искать только указанный путь.</span><span class="sxs-lookup"><span data-stu-id="77df2-116">The preprocessor stops searching as soon as it finds a file with the specified name; if you specify a complete, unambiguous path specification for the file, the preprocessor searches only the specified path.</span></span>

> [!NOTE]
> <span data-ttu-id="77df2-117">[Средство компилятора Effect](/windows/desktop/direct3dtools/fxc) имеет встроенный обработчик include с параметром/i.</span><span class="sxs-lookup"><span data-stu-id="77df2-117">The [Effect-Compiler Tool](/windows/desktop/direct3dtools/fxc) has a built-in include handler using the /I switch.</span></span> <span data-ttu-id="77df2-118">Однако при выполнении компилятора из API можно предоставить настраиваемый обработчик include, реализовав интерфейс ID3DXInclude.</span><span class="sxs-lookup"><span data-stu-id="77df2-118">However, when executing the compiler from the API, you can provide a customized include handler by implementing the ID3DXInclude interface.</span></span>

<span data-ttu-id="77df2-119">Различие между двумя формами синтаксиса — это порядок, в котором препроцессор выполняет поиск файлов заголовков, если путь не указан, как показано в следующей таблице.</span><span class="sxs-lookup"><span data-stu-id="77df2-119">The difference between the two syntax forms is the order in which the preprocessor searches for header files when the path is incompletely specified, as shown in the following table.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="77df2-120">Форма синтаксиса</span><span class="sxs-lookup"><span data-stu-id="77df2-120">Syntax form</span></span></th>
<th><span data-ttu-id="77df2-121">Шаблон поиска препроцессора</span><span class="sxs-lookup"><span data-stu-id="77df2-121">Preprocessor search pattern</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="77df2-122">#включить <b>&quot;</b> <em>имя файла</em><b>&quot;</b></span><span class="sxs-lookup"><span data-stu-id="77df2-122">#include <b>&quot;</b><em>filename</em><b>&quot;</b></span></span></td>
<td><span data-ttu-id="77df2-123">Выполняет поиск включаемого файла:</span><span class="sxs-lookup"><span data-stu-id="77df2-123">Searches for the include file:</span></span>
<ol>
<li><span data-ttu-id="77df2-124">в том же каталоге, где находится файл, содержащий директиву #include.</span><span class="sxs-lookup"><span data-stu-id="77df2-124">in the same directory as the file that contains the #include directive.</span></span></li>
<li><span data-ttu-id="77df2-125">в каталогах любых файлов, содержащих директиву #include для файла, содержащего директиву #include.</span><span class="sxs-lookup"><span data-stu-id="77df2-125">in the directories of any files that contain a #include directive for the file that contains the #include directive.</span></span></li>
<li><span data-ttu-id="77df2-126">в путях, заданных параметром компилятора/I, в порядке их перечисления.</span><span class="sxs-lookup"><span data-stu-id="77df2-126">in paths specified by the /I compiler option, in the order in which they are listed.</span></span></li>
<li><p><span data-ttu-id="77df2-127">в путях, заданных переменной среды INCLUDE, в порядке их перечисления.</span><span class="sxs-lookup"><span data-stu-id="77df2-127">in paths specified by the INCLUDE environment variable, in the order in which they are listed.</span></span></p>
<blockquote>
[!NOTE]<br />
<span data-ttu-id="77df2-128">Переменная среды INCLUDE игнорируется в среде разработки.</span><span class="sxs-lookup"><span data-stu-id="77df2-128">The INCLUDE environment variable is ignored in an development environment.</span></span> <span data-ttu-id="77df2-129">Сведения о том, как задать пути включения для проекта, см. в документации по среде разработки.</span><span class="sxs-lookup"><span data-stu-id="77df2-129">Refer to your development environment's documentation for information about how to set the include paths for your project.</span></span>
</blockquote>
<p><br/></p></li>
</ol></td>
</tr>
<tr class="even">
<td><span data-ttu-id="77df2-130">#включить <b><</b> <em>имя файла</em><b>></b></span><span class="sxs-lookup"><span data-stu-id="77df2-130">#include <b><</b><em>filename</em><b>></b></span></span></td>
<td><span data-ttu-id="77df2-131">Выполняет поиск включаемого файла:</span><span class="sxs-lookup"><span data-stu-id="77df2-131">Searches for the include file:</span></span>
<ol>
<li><span data-ttu-id="77df2-132">в путях, заданных параметром компилятора/I, в порядке их перечисления.</span><span class="sxs-lookup"><span data-stu-id="77df2-132">in paths specified by the /I compiler option, in the order in which they are listed.</span></span></li>
<li><p><span data-ttu-id="77df2-133">в путях, заданных переменной среды INCLUDE, в порядке их перечисления.</span><span class="sxs-lookup"><span data-stu-id="77df2-133">in paths specified by the INCLUDE environment variable, in the order in which they are listed.</span></span></p>
<blockquote>
[!NOTE]<br />
<span data-ttu-id="77df2-134">Переменная среды INCLUDE игнорируется в среде разработки.</span><span class="sxs-lookup"><span data-stu-id="77df2-134">The INCLUDE environment variable is ignored in an development environment.</span></span> <span data-ttu-id="77df2-135">Сведения о том, как задать пути включения для проекта, см. в документации по среде разработки.</span><span class="sxs-lookup"><span data-stu-id="77df2-135">Refer to your development environment's documentation for information about how to set the include paths for your project.</span></span>
</blockquote>
<p><br/></p></li>
</ol></td>
</tr>
</tbody>
</table>

## <a name="examples"></a><span data-ttu-id="77df2-136">Примеры</span><span class="sxs-lookup"><span data-stu-id="77df2-136">Examples</span></span>

<span data-ttu-id="77df2-137">В следующем примере препроцессор заменяет \# директиву include содержимым файла stdio. h.</span><span class="sxs-lookup"><span data-stu-id="77df2-137">The following example causes the preprocessor to replace the \#include directive with the contents of stdio.h.</span></span> <span data-ttu-id="77df2-138">Поскольку в примере используется формат угловой скобки, препроцессор будет искать файл только в каталогах, указанных параметром компилятора/I и переменной среды INCLUDE.</span><span class="sxs-lookup"><span data-stu-id="77df2-138">Because the example uses the angle bracket format, the preprocessor will search for the file only in the directories listed by the /I compiler option and the INCLUDE environment variable.</span></span>

```cpp
#include <stdio.h>
```

## <a name="see-also"></a><span data-ttu-id="77df2-139">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="77df2-139">See also</span></span>

- [<span data-ttu-id="77df2-140">Директивы препроцессора (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="77df2-140">Preprocessor Directives (DirectX HLSL)</span></span>](dx-graphics-hlsl-appendix-preprocessor.md)

- <span data-ttu-id="77df2-141">[Интерфейс ID3D10Include](/previous-versions/windows/desktop/legacy/bb173775(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="77df2-141">[ID3D10Include Interface](/previous-versions/windows/desktop/legacy/bb173775(v=vs.85))</span></span>

- [<span data-ttu-id="77df2-142">Effect — средство компилятора</span><span class="sxs-lookup"><span data-stu-id="77df2-142">Effect-Compiler Tool</span></span>](/windows/desktop/direct3dtools/fxc)