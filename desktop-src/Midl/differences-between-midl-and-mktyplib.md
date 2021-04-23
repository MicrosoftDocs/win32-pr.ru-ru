---
title: Различия между MIDL и MkTypLib
description: Различия между MIDL и MkTypLib
ms.assetid: 86abd70b-7238-49a6-a996-2c8906a14449
keywords:
- MIDL и ODL MIDL, различия между MIDL и MkTypLib
- MkTypLib MIDL
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6a54b6103cc230e1c5e6700b0ddc93312c767f9b
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/16/2019
ms.locfileid: "104068615"
---
# <a name="differences-between-midl-and-mktyplib"></a><span data-ttu-id="bdee0-105">Различия между MIDL и MkTypLib</span><span class="sxs-lookup"><span data-stu-id="bdee0-105">Differences Between MIDL and MkTypLib</span></span>

> [!Note]  
> <span data-ttu-id="bdee0-106">Средство Mktyplib.exe устарело.</span><span class="sxs-lookup"><span data-stu-id="bdee0-106">The Mktyplib.exe tool is obsolete.</span></span> <span data-ttu-id="bdee0-107">Вместо этого используйте компилятор MIDL.</span><span class="sxs-lookup"><span data-stu-id="bdee0-107">Use the MIDL compiler instead.</span></span>

 

<span data-ttu-id="bdee0-108">Существует несколько ключевых областей, в которых компилятор MIDL отличается от MkTypLib.</span><span class="sxs-lookup"><span data-stu-id="bdee0-108">There are a few key areas in which the MIDL compiler differs from MkTypLib.</span></span> <span data-ttu-id="bdee0-109">Большая часть этих различий возникает, поскольку MIDL ориентирован более в сторону C-синтаксиса, чем MkTypLib.</span><span class="sxs-lookup"><span data-stu-id="bdee0-109">Most of these differences arise because MIDL is oriented more toward C-syntax than MkTypLib.</span></span>

<span data-ttu-id="bdee0-110">В общем случае вам потребуется использовать синтаксис MIDL в IDL-файлах.</span><span class="sxs-lookup"><span data-stu-id="bdee0-110">In general, you will want to use the MIDL syntax in your IDL files.</span></span> <span data-ttu-id="bdee0-111">Однако если необходимо скомпилировать существующий файл ODL или иным образом поддерживать совместимость с MkTypLib, используйте параметр компилятора [**/Mktyplib203**](-mktyplib203.md) MIDL, чтобы заставить MIDL вести себя так же, как Mkktyplib.exe, версия 2,03.</span><span class="sxs-lookup"><span data-stu-id="bdee0-111">However, if you need to compile an existing ODL file, or otherwise maintain compatibility with MkTypLib, use the [**/mktyplib203**](-mktyplib203.md) MIDL compiler option to force MIDL to behave like Mkktyplib.exe, version 2.03.</span></span> <span data-ttu-id="bdee0-112">(Это последний выпуск средства MkTypLib.) В частности, параметр **/mktyplib203** разрешает следующие различия:</span><span class="sxs-lookup"><span data-stu-id="bdee0-112">(This is the last release of the MkTypLib tool.) Specifically, the **/mktyplib203** option resolves these differences:</span></span>

-   <span data-ttu-id="bdee0-113">синтаксис typedef для сложных типов данных</span><span class="sxs-lookup"><span data-stu-id="bdee0-113">typedef syntax for complex data types</span></span>

    <span data-ttu-id="bdee0-114">В MkTypLib оба следующих определения создают \_ запись ткинд для "этой \_ структуры" в библиотеке типов.</span><span class="sxs-lookup"><span data-stu-id="bdee0-114">In MkTypLib, both of the following definitions generate a TKIND\_RECORD for "this\_struct" in the type library.</span></span> <span data-ttu-id="bdee0-115">Тег "тег структуры \_ " является необязательным и, если он используется, не будет отображаться в библиотеке типов.</span><span class="sxs-lookup"><span data-stu-id="bdee0-115">The tag "struct\_tag" is optional and, if used, will not show up in the type library.</span></span>

    ``` syntax
    typedef struct struct_tag { ... } this_struct;
    typedef struct { ... } that_struct;
    ```

    <span data-ttu-id="bdee0-116">Если отсутствует дополнительный тег, MIDL создаст его, фактически добавив тег к определению, предоставленному пользователем.</span><span class="sxs-lookup"><span data-stu-id="bdee0-116">If an optional tag is missing, MIDL will generate it, effectively adding a tag to the definition supplied by the user.</span></span> <span data-ttu-id="bdee0-117">Поскольку первое определение содержит тег, MIDL создает \_ запись ткинд для "этой \_ структуры" и \_ псевдоним ткинд для "этой \_ структуры" (определяя "эту \_ структуру" в качестве псевдонима для "тега структуры" \_ ).</span><span class="sxs-lookup"><span data-stu-id="bdee0-117">Since the first definition has a tag, MIDL will generate a TKIND\_RECORD for "this\_struct" and a TKIND\_ALIAS for "this\_struct" (defining "this\_struct" as an alias for "struct\_tag").</span></span> <span data-ttu-id="bdee0-118">Так как тег отсутствует во втором определении, MIDL создает \_ запись ткинд для искаженного имени, internal для MIDL, которая не имеет смысла для пользователя и \_ псевдонима ткинд для "этой \_ структуры".</span><span class="sxs-lookup"><span data-stu-id="bdee0-118">Because the tag is missing in the second definition, MIDL will generate a TKIND\_RECORD for a mangled name, internal to MIDL, that is not meaningful to the user and a TKIND\_ALIAS for "that\_struct".</span></span>

    <span data-ttu-id="bdee0-119">Это имеет потенциальные последствия для браузеров библиотек типов, которые просто отображают имя записи в пользовательском интерфейсе.</span><span class="sxs-lookup"><span data-stu-id="bdee0-119">This has potential implications for type library browsers that simply show the name of a record in their user interface.</span></span> <span data-ttu-id="bdee0-120">Если предполагается, что \_ запись ткинд имеет реальное имя, нераспознаваемые имена могут появиться в пользовательском интерфейсе.</span><span class="sxs-lookup"><span data-stu-id="bdee0-120">If you expect a TKIND\_RECORD to have a real name, unrecognizable names could appear in the user interface.</span></span> <span data-ttu-id="bdee0-121">Это поведение также применяется к определениям [**Union**](union.md) и [**enum**](enum.md) , при этом компилятор MIDL создает ткинд \_ объединения и \_ перечисления ткинд соответственно.</span><span class="sxs-lookup"><span data-stu-id="bdee0-121">This behavior also applies to [**union**](union.md) and [**enum**](enum.md) definitions, with the MIDL compiler generating TKIND\_UNIONs and TKIND\_ENUMs, respectively.</span></span>

    <span data-ttu-id="bdee0-122">MIDL также допускает определения [**структуры**](struct.md), [**объединения**](union.md)и [**перечисления**](enum.md) в стиле C.</span><span class="sxs-lookup"><span data-stu-id="bdee0-122">MIDL also allows C-style [**struct**](struct.md), [**union**](union.md), and [**enum**](enum.md) definitions.</span></span> <span data-ttu-id="bdee0-123">Например, следующее определение является допустимым в MIDL:</span><span class="sxs-lookup"><span data-stu-id="bdee0-123">For example, the following definition is legal in MIDL:</span></span>

    ``` syntax
    struct my_struct { ... };
    typedef struct my_struct your_struct;
    ```

-   <span data-ttu-id="bdee0-124">Логические типы данных</span><span class="sxs-lookup"><span data-stu-id="bdee0-124">Boolean data types</span></span>

    <span data-ttu-id="bdee0-125">В MkTypLib логический тип [**Boolean**](boolean.md) и тип данных MkTypLib bool эквивалентны логическому типу VT \_ , который СОПОСТАВЛЯЕТСЯ с типом Variant \_ bool, который определен как [**короткий**](short.md).</span><span class="sxs-lookup"><span data-stu-id="bdee0-125">In MkTypLib, the [**Boolean**](boolean.md) base type and the MkTypLib data type BOOL equate to VT\_BOOL, which maps to VARIANT\_BOOL, and which is defined as a [**short**](short.md).</span></span> <span data-ttu-id="bdee0-126">В MIDL базовый тип **Boolean** эквивалентен VT \_ UI1, который определен как [**символ без знака**](unsigned.md), а тип данных bool определен как [**Long**](long.md).</span><span class="sxs-lookup"><span data-stu-id="bdee0-126">In MIDL, the **Boolean** base type is equivalent to VT\_UI1, which is defined as an [**unsigned char**](unsigned.md), and the BOOL data type is defined as a [**long**](long.md).</span></span> <span data-ttu-id="bdee0-127">Это приводит к проблемам при использовании синтаксиса IDL и синтаксиса ODL в одном и том же файле и при этом пытаются обеспечить совместимость с MkTypLib.</span><span class="sxs-lookup"><span data-stu-id="bdee0-127">This leads to difficulties if you mix IDL syntax and ODL syntax in the same file while still trying to maintain compatibility with MkTypLib.</span></span> <span data-ttu-id="bdee0-128">Поскольку типы данных имеют разные размеры, код маршалирования не будет соответствовать описанию в сведениях о типе.</span><span class="sxs-lookup"><span data-stu-id="bdee0-128">Because the data types are different sizes, the marshaling code will not match what is described in the type information.</span></span> <span data-ttu-id="bdee0-129">Если требуется логическое значение VT \_ в библиотеке типов, следует использовать \_ тип данных Variant bool.</span><span class="sxs-lookup"><span data-stu-id="bdee0-129">If you want a VT\_BOOL in your type library, you should use the VARIANT\_BOOL data type.</span></span>

-   <span data-ttu-id="bdee0-130">Определения GUID в файлах заголовков</span><span class="sxs-lookup"><span data-stu-id="bdee0-130">GUID definitions in header files</span></span>

    <span data-ttu-id="bdee0-131">В MkTypLib идентификаторы GUID определяются в файле заголовка с помощью макроса, который может быть условно скомпилирован для создания либо предварительного определения GUID, либо экземпляра GUID.</span><span class="sxs-lookup"><span data-stu-id="bdee0-131">In MkTypLib, GUIDs are defined in the header file with a macro that can be conditionally compiled to generate either a GUID predefinition or an instantiated GUID.</span></span> <span data-ttu-id="bdee0-132">MIDL обычно помещает в создаваемые файлы заголовков определения GUID и создает экземпляры GUID только в файле, созданном с помощью параметра [**/IID**](-iid.md) .</span><span class="sxs-lookup"><span data-stu-id="bdee0-132">MIDL normally puts GUID predefinitions in its generated header files and GUID instantiations only in the file generated by the [**/iid**](-iid.md) switch.</span></span>

<span data-ttu-id="bdee0-133">Следующие различия в поведении не могут быть разрешены с помощью параметра [**/mktyplib203**](-mktyplib203.md) :</span><span class="sxs-lookup"><span data-stu-id="bdee0-133">The following differences in behavior cannot be resolved by using the [**/mktyplib203**](-mktyplib203.md) switch:</span></span>

-   <span data-ttu-id="bdee0-134">Чувствительность к регистру</span><span class="sxs-lookup"><span data-stu-id="bdee0-134">Case sensitivity</span></span>

    <span data-ttu-id="bdee0-135">MIDL учитывает регистр, а OLE Automation — нет.</span><span class="sxs-lookup"><span data-stu-id="bdee0-135">MIDL is case sensitive, OLE Automation is not.</span></span>

-   <span data-ttu-id="bdee0-136">Область символов в объявлении перечисления</span><span class="sxs-lookup"><span data-stu-id="bdee0-136">Scope of symbols in an enum declaration</span></span>

    <span data-ttu-id="bdee0-137">В MkTypLib область действия символов в перечислении является локальной.</span><span class="sxs-lookup"><span data-stu-id="bdee0-137">In MkTypLib the scope of symbols in an enum is local.</span></span> <span data-ttu-id="bdee0-138">В MIDL область символов в перечислении является глобальной, как и в C. Например, следующий код будет компилироваться в MkTypLib, но создаст ошибку повторяющегося имени в MIDL:</span><span class="sxs-lookup"><span data-stu-id="bdee0-138">In MIDL, the scope of symbols in an enum is global, as it is in C. For example, the following code will compile in MkTypLib, but will generate a duplicate name error in MIDL:</span></span>

    ``` syntax
    typedef struct { ... } a;
    enum {a=1, b=2, c=3};
    ```

-   <span data-ttu-id="bdee0-139">Область видимости открытого атрибута</span><span class="sxs-lookup"><span data-stu-id="bdee0-139">Scope of public attribute</span></span>

    <span data-ttu-id="bdee0-140">При применении атрибута [**Public**](public.md) к блоку интерфейса MkTypLib обрабатывает каждое определение типа в этом блоке интерфейса как общедоступное.</span><span class="sxs-lookup"><span data-stu-id="bdee0-140">If you apply the [**public**](public.md) attribute to an interface block, MkTypLib treats every typedef inside that interface block as public.</span></span> <span data-ttu-id="bdee0-141">Для языка MIDL необходимо явно применить атрибут **Public** к этим определениям типов, которые должны быть общедоступными.</span><span class="sxs-lookup"><span data-stu-id="bdee0-141">MIDL requires that you explicitly apply the **public** attribute to those typedefs that you want public.</span></span>

-   <span data-ttu-id="bdee0-142">Importlib порядок поиска</span><span class="sxs-lookup"><span data-stu-id="bdee0-142">Importlib search order</span></span>

    <span data-ttu-id="bdee0-143">Если импортируется более одной библиотеки типов, и если эти библиотеки содержат дублирующиеся ссылки, MkTypLib разрешает это с помощью первой найденной ссылки.</span><span class="sxs-lookup"><span data-stu-id="bdee0-143">If you import more than one type library, and if these libraries contain duplicate references, MkTypLib resolves this by using the first reference that it finds.</span></span> <span data-ttu-id="bdee0-144">MIDL будет использовать последнюю найденную ссылку.</span><span class="sxs-lookup"><span data-stu-id="bdee0-144">MIDL will use the last reference that it finds.</span></span> <span data-ttu-id="bdee0-145">Например, при использовании приведенного ниже синтаксиса ODL библиотека C будет использовать МУУУ typedef из библиотеки а, если компиляция выполняется с помощью MkTypLib, а МУУУ typedef из библиотеки B, если компиляция выполняется с помощью MIDL:</span><span class="sxs-lookup"><span data-stu-id="bdee0-145">For example, given the following ODL syntax, library C will use the MOO typedef from library A if you compile with MkTypLib, and the MOO typedef from library B if you compile with MIDL:</span></span>

    ``` syntax
    [...]library A
    {
        typedef struct tagMOO
        {...}MOO
    }

    [...]library B
    {
        typedef struct tagMOO
        {...} MOO
    }

    [...]library C
    {
        importlib (A.TLB)
        importlib (B.TLB)
        typedef struct tagBAA
        {MOO y;}BAA
    }
    ```

    <span data-ttu-id="bdee0-146">Чтобы устранить эту проблему, необходимо уточнить каждую из этих ссылок, указав правильное имя библиотеки импорта, например:</span><span class="sxs-lookup"><span data-stu-id="bdee0-146">The appropriate workaround for this is to qualify each such reference with the correct import library name, like this:</span></span>

    ``` syntax
    typedef struct tagBAA
        {A.MOO y;}BAA
    ```

-   <span data-ttu-id="bdee0-147">Тип данных VOID не распознан</span><span class="sxs-lookup"><span data-stu-id="bdee0-147">VOID data type not recognized</span></span>

    <span data-ttu-id="bdee0-148">MIDL распознает тип данных [**void**](void.md) C-Language и не распознает тип данных OLE Automation void.</span><span class="sxs-lookup"><span data-stu-id="bdee0-148">MIDL recognizes the C-language [**void**](void.md) data type and does not recognize the OLE Automation VOID data type.</span></span> <span data-ttu-id="bdee0-149">Если у вас есть ODL файл, использующий VOID, поместите это определение в начало файла:</span><span class="sxs-lookup"><span data-stu-id="bdee0-149">If you have an ODL file that uses VOID, place this definition at the top of the file:</span></span>

    ``` syntax
#define VOID void
    ```

-   <span data-ttu-id="bdee0-150">Экспоненциальная нотация</span><span class="sxs-lookup"><span data-stu-id="bdee0-150">Exponential notation</span></span>

    <span data-ttu-id="bdee0-151">MIDL требует, чтобы значения, выраженные в экспоненциальной нотации, содержались в кавычках.</span><span class="sxs-lookup"><span data-stu-id="bdee0-151">MIDL requires that values expressed in exponential notation be contained within quotation marks.</span></span> <span data-ttu-id="bdee0-152">Например, "-2.5 E + 3"</span><span class="sxs-lookup"><span data-stu-id="bdee0-152">For example, "-2.5E+3"</span></span>

-   <span data-ttu-id="bdee0-153">Значения и константы LCID</span><span class="sxs-lookup"><span data-stu-id="bdee0-153">LCID values and constants</span></span>

    <span data-ttu-id="bdee0-154">Обычно MIDL не учитывает код языка при синтаксическом анализе файлов.</span><span class="sxs-lookup"><span data-stu-id="bdee0-154">Normally MIDL does not consider the LCID when parsing files.</span></span> <span data-ttu-id="bdee0-155">Чтобы принудительно применить это поведение к значению или при определении константы необходимо использовать нотацию определенного языкового стандарта, заключите значение или константу в кавычки.</span><span class="sxs-lookup"><span data-stu-id="bdee0-155">To force this behavior for a value, or if you need to use locale-specific notation when defining a constant, enclose the value or constant in quotation marks.</span></span>

<span data-ttu-id="bdee0-156">Дополнительные сведения см. в разделе [**/mktyplib203**](-mktyplib203.md), [**/IID**](-iid.md)и [маршалирование типов данных OLE](marshaling-ole-data-types.md).</span><span class="sxs-lookup"><span data-stu-id="bdee0-156">For more information, see [**/mktyplib203**](-mktyplib203.md), [**/iid**](-iid.md), and [Marshaling OLE Data Types](marshaling-ole-data-types.md).</span></span>

 

 




