---
title: Импорт файлов и библиотек типов
description: Ключевые слова MIDL включают, импортирует и importlib позволяют повторно использовать код, ссылаясь на существующие файлы заголовка, IDL и файлов ODL, а также на скомпилированные библиотеки типов.
ms.assetid: b4571c1d-4bd7-4ab1-9ef6-14356a6c4bb4
keywords:
- Язык MIDL MIDL, задачи, импорт файлов и библиотек типов
- Импорт MIDL
- библиотеки типов MIDL, импорт
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d84b740f29726c1ce4d401fc69b2ea07e811eac0
ms.sourcegitcommit: 6515eef99ca0d1bbe3e27d4575e9986f5255f277
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/10/2021
ms.locfileid: "104353992"
---
# <a name="importing-files-and-type-libraries"></a><span data-ttu-id="b7703-106">Импорт файлов и библиотек типов</span><span class="sxs-lookup"><span data-stu-id="b7703-106">Importing Files and Type Libraries</span></span>

<span data-ttu-id="b7703-107">Ключевые слова MIDL [**включают**](include.md), [**импортирует**](import.md)и [**importlib**](importlib.md) позволяют повторно использовать код, ссылаясь на существующие файлы заголовка, IDL и файлов ODL, а также на скомпилированные библиотеки типов.</span><span class="sxs-lookup"><span data-stu-id="b7703-107">The MIDL keywords [**include**](include.md), [**import**](import.md), and [**importlib**](importlib.md) let you reuse code by referencing existing header, IDL, and object definition language (ODL) files, and compiled type libraries.</span></span>

<span data-ttu-id="b7703-108">Директива [**include**](include.md) ACF позволяет указать в файле ACF один или несколько файлов заголовков C-Language, которые будут включены в создаваемый MIDL код заглушки.</span><span class="sxs-lookup"><span data-stu-id="b7703-108">The ACF [**include**](include.md) directive lets you specify in an ACF file one or more C-language header files to be included in the MIDL-generated stub code.</span></span> <span data-ttu-id="b7703-109">В созданном файле будет **\# содержаться** строка с директивой C-препроцессора с указанным файлом заголовка.</span><span class="sxs-lookup"><span data-stu-id="b7703-109">The generated file will have a line with a **\#include** C-preprocessor directive with the indicated header file.</span></span> <span data-ttu-id="b7703-110">Используйте директиву **include** для переноса файлов заголовков, характерных для конкретной операционной среды, и не содержащих сведений, необходимых для интерфейса между клиентом и сервером.</span><span class="sxs-lookup"><span data-stu-id="b7703-110">Use this **include** directive to bring in header files that are specific to a particular operating environment and that do not contain information necessary for the interface between client and server.</span></span> <span data-ttu-id="b7703-111">Не используйте параметр **включить** для файлов заголовков, содержащих типы данных, которые должны быть доступны для IDL-файла. Вместо этого используйте директиву [**Import**](import.md) .</span><span class="sxs-lookup"><span data-stu-id="b7703-111">Do not use **include** for header files containing data types that you want available to the IDL file; instead, use the [**import**](import.md) directive.</span></span>

## <a name="example-1"></a><span data-ttu-id="b7703-112">Пример 1</span><span class="sxs-lookup"><span data-stu-id="b7703-112">Example 1</span></span>

``` syntax
[
  auto_handle
] 
interface X86PC
{ 
  include "gendefs.h", "protos.h", "myfile.h"; 
  //interface typdefs and function declarations here
}
```

<span data-ttu-id="b7703-113">Директива [**импорта**](import.md) IDL является стандартным методом для объединения определений типов и интерфейсов из других файлов IDL (или ODL) и файлов заголовков в IDL-файл.</span><span class="sxs-lookup"><span data-stu-id="b7703-113">The IDL [**import**](import.md) directive is the standard method for bringing type and interface definitions from other IDL (or ODL) files and header files into your IDL file.</span></span> <span data-ttu-id="b7703-114">Все инструкции IDL в импортируемом файле, такие как typedef, объявления [**const**](const.md) и определения интерфейса, становятся доступными для ИМПОРТИРОВАНного IDL-файла.</span><span class="sxs-lookup"><span data-stu-id="b7703-114">All IDL statements in the imported file, such as typedefs, [**const**](const.md) declarations, and interface definitions become available to the importing IDL file.</span></span>

<span data-ttu-id="b7703-115">Как и директива препроцессора языка C **\# , директива** [**Import**](import.md) указывает компилятору включать типы данных, определенные в импортированных IDL-файлах.</span><span class="sxs-lookup"><span data-stu-id="b7703-115">Like the C-language preprocessor directive **\#include**, the [**import**](import.md) directive tells the compiler to include data types that were defined in the imported IDL files.</span></span> <span data-ttu-id="b7703-116">В отличие от директивы **\# include** , Директива **Import** игнорирует прототипы процедур, так как для импортированного файла не создаются заглушки.</span><span class="sxs-lookup"><span data-stu-id="b7703-116">Unlike the **\#include** directive, the **import** directive ignores procedure prototypes, since no stubs are generated for anything in the imported file.</span></span> <span data-ttu-id="b7703-117">Поскольку препроцессор вызывается отдельно для импортированного файла, директивы препроцессора (например, \* \*) не переносятся в импортируемый IDL-файл.</span><span class="sxs-lookup"><span data-stu-id="b7703-117">Because the preprocessor is invoked separately for the imported file, preprocessor directives (such as \*\*) do not carry over to the importing IDL file.</span></span>

<span data-ttu-id="b7703-118">Дополнительные сведения об использовании [**импорта**](import.md) для включения системных файлов заголовков в IDL-файл см. в разделе [Импорт системных файлов заголовков](importing-system-header-files.md).</span><span class="sxs-lookup"><span data-stu-id="b7703-118">For additional information on using [**import**](import.md) to include system header files in an IDL file, see [Importing System Header Files](importing-system-header-files.md).</span></span>

## <a name="example-2"></a><span data-ttu-id="b7703-119">Пример 2</span><span class="sxs-lookup"><span data-stu-id="b7703-119">Example 2</span></span>

``` syntax
[
  uuid(. . .), object
] 
interface IKnown : IUnknown
{
  import "base.idl", "unknwn.idl", "helper.idl";
  //remainder of interface definition
}
```

<span data-ttu-id="b7703-120">Директива ODL [**importlib**](importlib.md) позволяет ссылаться на скомпилированную библиотеку типов в файле IDL или ODL.</span><span class="sxs-lookup"><span data-stu-id="b7703-120">The ODL [**importlib**](importlib.md) directive lets you reference a compiled type library in your IDL or ODL file.</span></span> <span data-ttu-id="b7703-121">Директива **importlib** должна находиться внутри оператора [**Library**](library.md) и должна предшествовать другим описаниям типов в библиотеке.</span><span class="sxs-lookup"><span data-stu-id="b7703-121">The **importlib** directive must be inside a [**library**](library.md) statement, and must precede other type descriptions in the library.</span></span> <span data-ttu-id="b7703-122">Импортированная библиотека, а также созданная библиотека должна быть доступна приложению во время выполнения.</span><span class="sxs-lookup"><span data-stu-id="b7703-122">The imported library, as well as the generated library, must be available to the application at runtime.</span></span>

## <a name="example-3"></a><span data-ttu-id="b7703-123">Пример 3</span><span class="sxs-lookup"><span data-stu-id="b7703-123">Example 3</span></span>

``` syntax
library NewBrowser
{
  importlib("stdole32.tlb");
  importlib("legacy.tlb");
  //remainder of library definition
};
```

<span data-ttu-id="b7703-124">Также можно использовать директиву C-препроцессор **\# include** для включения заголовков и других файлов в IDL-или ODL-файл.</span><span class="sxs-lookup"><span data-stu-id="b7703-124">You can also use the C-preprocessor **\#include** directive to include headers and other files in your IDL or ODL file.</span></span> <span data-ttu-id="b7703-125">Однако имейте в виду, что эта директива будет включать все содержимое указанного файла в буквальном смысле.</span><span class="sxs-lookup"><span data-stu-id="b7703-125">Be aware, however, that this directive will literally include the entire contents of the specified file.</span></span> <span data-ttu-id="b7703-126">Если файл заголовка содержит прототипы, которые не нужны или не нужны в файлах заглушки, созданных MIDL, или если они содержат определения типов, не поддерживающие удаленное взаимодействие, следует использовать директиву MIDL [**Import**](import.md) вместо директивы **\# include** .</span><span class="sxs-lookup"><span data-stu-id="b7703-126">If a header file contains prototypes that you do not need or want in the MIDL-generated stub files, or if it contains nonremotable type definitions, you should use the MIDL [**import**](import.md) directive instead of the **\#include** directive.</span></span>

## <a name="related-topics"></a><span data-ttu-id="b7703-127">См. также</span><span class="sxs-lookup"><span data-stu-id="b7703-127">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="b7703-128">**импортиру**</span><span class="sxs-lookup"><span data-stu-id="b7703-128">**import**</span></span>](import.md)
</dt> <dt>

[<span data-ttu-id="b7703-129">**importlib**</span><span class="sxs-lookup"><span data-stu-id="b7703-129">**importlib**</span></span>](importlib.md)
</dt> <dt>

[<span data-ttu-id="b7703-130">**относится**</span><span class="sxs-lookup"><span data-stu-id="b7703-130">**include**</span></span>](include.md)
</dt> <dt>

[<span data-ttu-id="b7703-131">Импорт системных файлов заголовков</span><span class="sxs-lookup"><span data-stu-id="b7703-131">Importing System Header Files</span></span>](importing-system-header-files.md)
</dt> </dl>

 

 




