---
title: Определения типов, объявления конструкций и импорты
description: Определения типов, объявления конструкций и импорты могут происходить за пределами тела интерфейса.
ms.assetid: 5d9011ab-bfc4-41f6-bd69-953660191652
keywords:
- интерфейсы MIDL, определения типов
- интерфейсы MIDL, объявления конструкций
- интерфейсы MIDL, импорты
- определения типов MIDL
- создать объявления с MIDL
- Импорт MIDL
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 645781f033566ba43dc6e355935ed112d0e8f5f6
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/16/2019
ms.locfileid: "105661521"
---
# <a name="type-definitions-construct-declarations-and-imports"></a><span data-ttu-id="9036f-109">Определения типов, объявления конструкций и импорты</span><span class="sxs-lookup"><span data-stu-id="9036f-109">Type Definitions, Construct Declarations, and Imports</span></span>

<span data-ttu-id="9036f-110">Определения типов, объявления конструкций и импорты могут происходить за пределами тела интерфейса.</span><span class="sxs-lookup"><span data-stu-id="9036f-110">Type definitions, construct declarations, and imports can occur outside of the interface body.</span></span> <span data-ttu-id="9036f-111">Все определения из основного IDL-файла будут отображаться в созданном файле заголовка, а все процедуры из всех интерфейсов в основном IDL-файле будут создавать подпрограммы-заглушки.</span><span class="sxs-lookup"><span data-stu-id="9036f-111">All definitions from the main IDL file will appear in the generated header file, and all the procedures from all the interfaces in the main IDL file will generate stub routines.</span></span> <span data-ttu-id="9036f-112">Это позволяет приложениям, поддерживающим несколько интерфейсов, объединять файлы IDL в один объединенный IDL-файл.</span><span class="sxs-lookup"><span data-stu-id="9036f-112">This enables applications that support multiple interfaces to merge IDL files into a single, combined IDL file.</span></span>

<span data-ttu-id="9036f-113">Поэтому компиляция файлов требует меньше времени, а также позволяет MIDL сократить избыточность в созданных заглушках.</span><span class="sxs-lookup"><span data-stu-id="9036f-113">As a result, it requires less time to compile the files and also allows MIDL to reduce redundancies in the generated stubs.</span></span> <span data-ttu-id="9036f-114">Это может значительно улучшить интерфейсы [**объектов**](object.md) посредством возможности совместного использования общего кода для базовых интерфейсов и производных интерфейсов.</span><span class="sxs-lookup"><span data-stu-id="9036f-114">This can significantly improve [**object**](object.md) interfaces through the ability to share common code for base interfaces and derived interfaces.</span></span> <span data-ttu-id="9036f-115">Для интерфейсов, не являющихся **объектами** , имена процедур должны быть уникальными во всех интерфейсах.</span><span class="sxs-lookup"><span data-stu-id="9036f-115">For non- **object** interfaces, the procedure names must be unique across all the interfaces.</span></span> <span data-ttu-id="9036f-116">В интерфейсах **объектов** имена процедур должны быть уникальными только в пределах интерфейса.</span><span class="sxs-lookup"><span data-stu-id="9036f-116">For **object** interfaces, the procedure names need to be unique only within an interface.</span></span> <span data-ttu-id="9036f-117">Обратите внимание, что при использовании параметра [**/ОСФ**](-osf.md) не разрешается использовать несколько интерфейсов.</span><span class="sxs-lookup"><span data-stu-id="9036f-117">Note that multiple interfaces are not permitted when you use the [**/osf**](-osf.md) switch.</span></span>

## <a name="declarative-constructs"></a><span data-ttu-id="9036f-118">Декларативные конструкции</span><span class="sxs-lookup"><span data-stu-id="9036f-118">Declarative Constructs</span></span>

<span data-ttu-id="9036f-119">Синтаксис для декларативных конструкций в IDL-файле подобен тому, что для C. MIDL поддерживает все декларативные конструкции Microsoft C/C++, за исключением следующих:</span><span class="sxs-lookup"><span data-stu-id="9036f-119">The syntax for declarative constructs in the IDL file is similar to that for C. MIDL supports all Microsoft C/C++ declarative constructs except the following:</span></span>

-   <span data-ttu-id="9036f-120">Более старые деклараторы стиля, позволяющие указывать декларатор без спецификатора типа, например:</span><span class="sxs-lookup"><span data-stu-id="9036f-120">Older style declarators that allow a declarator to be specified without a type specifier, such as:</span></span>

    ``` syntax
    x (y) 
    short x (y)
    ```

-   <span data-ttu-id="9036f-121">Объявления с инициализаторами (MIDL принимает только объявления, которые соответствуют синтаксису MIDL [**const**](const.md) ).</span><span class="sxs-lookup"><span data-stu-id="9036f-121">Declarations with initializers (MIDL only accepts declarations that conform to the MIDL [**const**](const.md) syntax).</span></span>

<span data-ttu-id="9036f-122">Ключевое слово [**Import**](import.md) указывает имена одного или нескольких IDL-файлов для импорта.</span><span class="sxs-lookup"><span data-stu-id="9036f-122">The [**import**](import.md) keyword specifies the names of one or more IDL files to import.</span></span> <span data-ttu-id="9036f-123">Директива import аналогична директиве [**include**](include.md) в C, за исключением того, что в импортируемый IDL-файл ассимилатед только типы данных.</span><span class="sxs-lookup"><span data-stu-id="9036f-123">The import directive is similar to the C [**include**](include.md) directive, except that only data types are assimilated into the importing IDL file.</span></span>

## <a name="constant-declaration"></a><span data-ttu-id="9036f-124">Объявление константы</span><span class="sxs-lookup"><span data-stu-id="9036f-124">Constant Declaration</span></span>

<span data-ttu-id="9036f-125">В объявлении константы указываются [**логические**](boolean.md)константы, целые числа, символы, знаки в расширенных символах, строки и **void \*** .</span><span class="sxs-lookup"><span data-stu-id="9036f-125">The constant declaration specifies [**Boolean**](boolean.md), integer, character, wide-character, string, and **void \*** constants.</span></span> <span data-ttu-id="9036f-126">Дополнительные сведения см. в разделе [**const**](const.md).</span><span class="sxs-lookup"><span data-stu-id="9036f-126">For more information, see [**const**](const.md).</span></span>

## <a name="general-declaration"></a><span data-ttu-id="9036f-127">Общее объявление</span><span class="sxs-lookup"><span data-stu-id="9036f-127">General Declaration</span></span>

<span data-ttu-id="9036f-128">Общее объявление похоже на инструкцию C [**typedef**](typedef.md) с добавлением АТРИБУТОВ типа IDL.</span><span class="sxs-lookup"><span data-stu-id="9036f-128">A general declaration is similar to the C [**typedef**](typedef.md) statement with the addition of IDL type attributes.</span></span> <span data-ttu-id="9036f-129">Компилятор MIDL также разрешает неявное объявление в форме определения переменной, за исключением режима [**/ОСФ**](-osf.md) .</span><span class="sxs-lookup"><span data-stu-id="9036f-129">Except in [**/osf**](-osf.md) mode, the MIDL compiler also allows an implicit declaration in the form of a variable definition.</span></span>

## <a name="function-declaration"></a><span data-ttu-id="9036f-130">Объявление функции</span><span class="sxs-lookup"><span data-stu-id="9036f-130">Function Declaration</span></span>

<span data-ttu-id="9036f-131">Декларатор функции является особым случаем общего объявления.</span><span class="sxs-lookup"><span data-stu-id="9036f-131">The function declarator is a special case of the general declaration.</span></span> <span data-ttu-id="9036f-132">Атрибуты IDL можно использовать для указания поведения возвращаемого типа функции и каждого из параметров.</span><span class="sxs-lookup"><span data-stu-id="9036f-132">You can use IDL attributes to specify the behavior of the function return type and each of the parameters.</span></span>

## <a name="examples"></a><span data-ttu-id="9036f-133">Примеры</span><span class="sxs-lookup"><span data-stu-id="9036f-133">Examples</span></span>

``` syntax
[ 
    uuid(12345678-1234-1234-1234-123456789ABC), 
    version(3.1), 
    pointer_default(unique) 
] 
interface IdlGrammarExample 
{ 
    import "windows.idl", "other.idl"; 
    const wchar_t * NAME = L"Example Program"; 
    typedef char * PCHAR; 
 
    HRESULT DictCheckSpelling( 
        [in, string] PCHAR   word,     // word to look up 
        [out]        short * isPresent // 0 if not present 
    ); 
}
```

 

 




