---
description: Расширенный синтаксис запросов (АКС) — это синтаксис запроса по умолчанию, используемый службой поиска Windows для запроса индекса и уточнения и сужения параметров поиска.
ms.assetid: 76e33903-d063-48c0-9afe-912c3daa8237
title: Использование расширенного синтаксиса запросов программными средствами
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bc8fa69a5a5ccaa37b84a10abd367e5a29656455
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "105719320"
---
# <a name="using-advanced-query-syntax-programmatically"></a><span data-ttu-id="ae187-103">Использование расширенного синтаксиса запросов программными средствами</span><span class="sxs-lookup"><span data-stu-id="ae187-103">Using Advanced Query Syntax Programmatically</span></span>

<span data-ttu-id="ae187-104">Расширенный синтаксис запросов (АКС) — это синтаксис запроса по умолчанию, используемый службой поиска Windows для запроса индекса и уточнения и сужения параметров поиска.</span><span class="sxs-lookup"><span data-stu-id="ae187-104">Advanced Query Syntax (AQS) is the default query syntax used by Windows Search to query the index and to refine and narrow search parameters.</span></span> <span data-ttu-id="ae187-105">АКС используется разработчиками для создания запросов программным способом (и пользователями для ограничения параметров поиска).</span><span class="sxs-lookup"><span data-stu-id="ae187-105">AQS is employed by developers to build queries programmatically (and by users to narrow their search parameters).</span></span> <span data-ttu-id="ae187-106">Канонический АКС появился в Windows 7 и должен использоваться в Windows 7 и более поздних версиях для программного создания запросов АКС.</span><span class="sxs-lookup"><span data-stu-id="ae187-106">Canonical AQS was introduced in Windows 7 and must be used in Windows 7 and later to programmatically generate AQS queries.</span></span>

<span data-ttu-id="ae187-107">Этот раздел организован следующим образом:</span><span class="sxs-lookup"><span data-stu-id="ae187-107">This topic is organized as follows:</span></span>

-   [<span data-ttu-id="ae187-108">О расширенном синтаксисе запросов</span><span class="sxs-lookup"><span data-stu-id="ae187-108">About Advanced Query Syntax</span></span>](#about-advanced-query-syntax)
    -   [<span data-ttu-id="ae187-109">Примеры</span><span class="sxs-lookup"><span data-stu-id="ae187-109">Examples</span></span>](#examples)
    -   [<span data-ttu-id="ae187-110">Свойства</span><span class="sxs-lookup"><span data-stu-id="ae187-110">Properties</span></span>](#properties)
-   [<span data-ttu-id="ae187-111">Использование ключевых слов в локальных языках</span><span class="sxs-lookup"><span data-stu-id="ae187-111">Keyword Use in Local Languages</span></span>](#keyword-use-in-local-languages)
-   [<span data-ttu-id="ae187-112">Канонический синтаксис расширенных запросов в Windows 7</span><span class="sxs-lookup"><span data-stu-id="ae187-112">Canonical Advanced Query Syntax in Windows 7</span></span>](#canonical-advanced-query-syntax-in-windows-7)
    -   [<span data-ttu-id="ae187-113">Примеры</span><span class="sxs-lookup"><span data-stu-id="ae187-113">Examples</span></span>](#examples)
    -   [<span data-ttu-id="ae187-114">Операторы запросов</span><span class="sxs-lookup"><span data-stu-id="ae187-114">Query Operators</span></span>](#query-operators)
    -   [<span data-ttu-id="ae187-115">Значения запроса</span><span class="sxs-lookup"><span data-stu-id="ae187-115">Query Values</span></span>](#query-values)
-   [<span data-ttu-id="ae187-116">Ограничения области</span><span class="sxs-lookup"><span data-stu-id="ae187-116">Scope Restrictions</span></span>](#scope-restrictions)
-   [<span data-ttu-id="ae187-117">Дополнительные ресурсы</span><span class="sxs-lookup"><span data-stu-id="ae187-117">Additional Resources</span></span>](#additional-resources)
-   [<span data-ttu-id="ae187-118">См. также</span><span class="sxs-lookup"><span data-stu-id="ae187-118">Related topics</span></span>](#related-topics)

## <a name="about-advanced-query-syntax"></a><span data-ttu-id="ae187-119">О расширенном синтаксисе запросов</span><span class="sxs-lookup"><span data-stu-id="ae187-119">About Advanced Query Syntax</span></span>

<span data-ttu-id="ae187-120">Запрос состоит из базовых запросов, связанных с AND, OR и NOT, как показано в следующем примере синтаксиса:</span><span class="sxs-lookup"><span data-stu-id="ae187-120">A query consists of basic queries connected with AND, OR, and NOT, as shown in the following example syntax:</span></span>

``` syntax
<query> ::=
     <basic query>
| ( <query> )
| <query> AND <query>  
| <query> <query>    // Same as <query> AND <query>
| <query> OR <query> 
| NOT <query>
```

> [!Note]  
> <span data-ttu-id="ae187-121">АКС не учитывает регистр, за исключением AND, OR и NOT, которые должны располагаться в верхнем регистре.</span><span class="sxs-lookup"><span data-stu-id="ae187-121">AQS is not case sensitive, with the exception of AND, OR, and NOT, which must be in all uppercase.</span></span>

 

<span data-ttu-id="ae187-122">Если запрос имеет два или более использования и или или, то они будут привязаны слева направо, независимо от того, является он и или или.</span><span class="sxs-lookup"><span data-stu-id="ae187-122">If a query has two or more uses of AND or OR, they will bind from left to right, regardless of whether it is AND or OR.</span></span> <span data-ttu-id="ae187-123">Таким образом, запрос "Apple AND груш или Плам" будет интерпретирован так, как если бы он был написан как "(Apple AND груш) или Плам", а запрос "Apple или груш и Плам" будет интерпретироваться как "(Apple или груша) и Плам".</span><span class="sxs-lookup"><span data-stu-id="ae187-123">That is, the query, "apple AND pear OR plum" will be interpreted as if it were written as "(apple AND pear) OR plum", and the query, "apple OR pear AND plum", will be interpreted as if it were written as "(apple OR pear) AND plum".</span></span> <span data-ttu-id="ae187-124">Таким образом, если документ содержит слово Плам, но ни Apple, ни груши, первый запрос возвратит его, но второй запрос не будет.</span><span class="sxs-lookup"><span data-stu-id="ae187-124">So if a document contains the word plum but neither apple, nor pear, the first query will return it but the second query will not.</span></span> <span data-ttu-id="ae187-125">Поэтому рекомендуется использовать явные круглые скобки для любого запроса, который смешивается с, и или, чтобы избежать ошибок или неправильных интерпретаций.</span><span class="sxs-lookup"><span data-stu-id="ae187-125">Hence, we recommend that you use explicit parentheses for any query that mixes AND and OR to avoid mistakes or misinterpretations.</span></span>

<span data-ttu-id="ae187-126">Базовый запрос выполняет поиск элементов, которые соответствуют ограничению для свойства.</span><span class="sxs-lookup"><span data-stu-id="ae187-126">A basic query searches for items that satisfy a restriction over a property.</span></span> <span data-ttu-id="ae187-127">Единственной обязательной частью базового запроса является значение ограничения или поиска.</span><span class="sxs-lookup"><span data-stu-id="ae187-127">The only required portion of a basic query is the restriction or search value.</span></span> <span data-ttu-id="ae187-128">Если не указать свойство, Поиск Windows будет выполнять поиск по всем свойствам.</span><span class="sxs-lookup"><span data-stu-id="ae187-128">If you do not specify a property, Windows Search searches all properties.</span></span> <span data-ttu-id="ae187-129"><restr> представляет ограничение поиска.</span><span class="sxs-lookup"><span data-stu-id="ae187-129"><restr> represents the search restriction.</span></span>

<span data-ttu-id="ae187-130">Следующие формы для базового запроса являются допустимыми:</span><span class="sxs-lookup"><span data-stu-id="ae187-130">The following forms for a basic query are valid:</span></span>

``` syntax
<basic query> ::=
     <prop>:<basic restr>
| <restr>
```

<span data-ttu-id="ae187-131">Свойство обозначается ключевым словом, таким как Author или size, или каноническим именем свойства, например [System. DateModified](../properties/props-system-datemodified.md).</span><span class="sxs-lookup"><span data-stu-id="ae187-131">A property is designated by a keyword such as author or size, or by a canonical property name such as [System.DateModified](../properties/props-system-datemodified.md).</span></span> <span data-ttu-id="ae187-132">Для свойства допустимы следующие формы:</span><span class="sxs-lookup"><span data-stu-id="ae187-132">Valid forms for a property are as follows:</span></span>

``` syntax
<prop> ::= 
     <canonical property name>
| <property label in UI language>
```

<span data-ttu-id="ae187-133">Оператор указывает операцию, например < или =.</span><span class="sxs-lookup"><span data-stu-id="ae187-133">An operator indicates an operation such as < or =.</span></span> <span data-ttu-id="ae187-134">Список допустимых операторов см. в подразделе «операторы запроса» далее в этом разделе.</span><span class="sxs-lookup"><span data-stu-id="ae187-134">For a list of valid operators, see the Query Operators section later in this topic.</span></span>

<span data-ttu-id="ae187-135">Базовое ограничение — это простое ограничение для свойства, которое можно записать без скобок:</span><span class="sxs-lookup"><span data-stu-id="ae187-135">A basic restriction is a simple restriction on a property that can be written without parentheses:</span></span>

``` syntax
<basic restr> ::=
     <value>
| <op><value>
| NOT <basic restr>
| ( <restr> )
```

<span data-ttu-id="ae187-136">Ограничение — это искомое значение, например числовое значение или строковое значение, при необходимости оператор.</span><span class="sxs-lookup"><span data-stu-id="ae187-136">A restriction is a search value such as a number value or string value, optionally with an operator.</span></span> <span data-ttu-id="ae187-137">Допустимые формы для ограничения приведены ниже.</span><span class="sxs-lookup"><span data-stu-id="ae187-137">Valid forms for a restriction are as follows:</span></span>

``` syntax
<restr> ::=
    <basic restr>
| <restr> AND <restr>
| <restr> <restr>      // Same as <restr> AND <restr>
| <restr> OR <restr>
```

<span data-ttu-id="ae187-138">Если оператор не указан, Windows Search выбирает наиболее подходящий оператор для запроса:</span><span class="sxs-lookup"><span data-stu-id="ae187-138">If you do not specify an operator, Windows Search chooses the most appropriate operator for your query:</span></span>

-   <span data-ttu-id="ae187-139">Для свойства String \_ \_ предполагается использование оператора COP Word STARTSWITH $<.</span><span class="sxs-lookup"><span data-stu-id="ae187-139">For a string property, the COP\_WORD\_STARTSWITH $< operator is assumed.</span></span>
-   <span data-ttu-id="ae187-140">Для всех остальных свойств \_ предполагается, что используется оператор COP EQUAL =.</span><span class="sxs-lookup"><span data-stu-id="ae187-140">For all other properties, the COP\_EQUAL = operator is assumed.</span></span>

<span data-ttu-id="ae187-141">Для программного использования АКС рекомендуется всегда иметь явный оператор.</span><span class="sxs-lookup"><span data-stu-id="ae187-141">For the programmatic use of AQS, we recommend that you always have an explicit operator.</span></span> <span data-ttu-id="ae187-142">Допустимая форма для поиска простого значения или диапазона значений выглядит следующим образом:</span><span class="sxs-lookup"><span data-stu-id="ae187-142">The valid form for searching a simple value or value range is as follows:</span></span>

``` syntax
<value> ::=
    <simplevalue>
| <simplevalue> .. <simplevalue>
```

<span data-ttu-id="ae187-143">Простое значение может состоять из любого из следующих типов:</span><span class="sxs-lookup"><span data-stu-id="ae187-143">A simple value can consist of any of the following types:</span></span>

``` syntax
<simplevalue> ::=
  []         // No value, or a null value
| <word>     // A sequence of characters without whitespace
| <number>   // An integer or a floating point number
| <datetime> // A relative date, or an absolute date and/or time
| <Boolean>
| "..."      // A phrase
| <enumeration range>
```

### <a name="examples"></a><span data-ttu-id="ae187-144">Примеры</span><span class="sxs-lookup"><span data-stu-id="ae187-144">Examples</span></span>

<span data-ttu-id="ae187-145">Запрос, выполняющий поиск документа, содержащего этап «прошлый квартал», созданный с помощью Сереса или Иванов и сохраненный в папке MyDocs, объединяет три основных запроса следующим образом:</span><span class="sxs-lookup"><span data-stu-id="ae187-145">A query that searches for a document containing the phase "last quarter," authored by Theresa or Lee, and that was saved to the folder MyDocs, combines three basic queries as follows:</span></span>

``` syntax
"last quarter" author:(theresa OR lee) folder:MyDocs
```

<span data-ttu-id="ae187-146">Вот три основных запроса:</span><span class="sxs-lookup"><span data-stu-id="ae187-146">The three basic queries are:</span></span>

-   <span data-ttu-id="ae187-147">"прошлый квартал"</span><span class="sxs-lookup"><span data-stu-id="ae187-147">"last quarter"</span></span>
-   <span data-ttu-id="ae187-148">Автор: (Сереса или Иванов)</span><span class="sxs-lookup"><span data-stu-id="ae187-148">author:(theresa OR lee)</span></span>
-   <span data-ttu-id="ae187-149">Папка: MyDocs</span><span class="sxs-lookup"><span data-stu-id="ae187-149">folder:MyDocs</span></span>

<span data-ttu-id="ae187-150">Базовый запрос, в котором используется канонический синтаксис:</span><span class="sxs-lookup"><span data-stu-id="ae187-150">A basic query that uses canonical syntax is:</span></span>

``` syntax
System.Size:>1kb
```

### <a name="properties"></a><span data-ttu-id="ae187-151">Свойства</span><span class="sxs-lookup"><span data-stu-id="ae187-151">Properties</span></span>

<span data-ttu-id="ae187-152">На свойства ссылается ключевое слово, которое может быть именем канонического свойства в Windows 7 и более поздних версиях.</span><span class="sxs-lookup"><span data-stu-id="ae187-152">Properties are referred to by a keyword, which can be a canonical property name in Windows 7 and later.</span></span> <span data-ttu-id="ae187-153">АКС в пользовательском интерфейсе Windows может использовать метку вместо канонического имени свойства, например author, а не [System. Author](../properties/props-system-author.md).</span><span class="sxs-lookup"><span data-stu-id="ae187-153">AQS in the Windows UI can use the label instead of the canonical property name, such as author instead of [System.Author](../properties/props-system-author.md).</span></span> <span data-ttu-id="ae187-154">В Windows Vista и более ранних версиях можно было использовать метки на английском языке независимо от языка пользовательского интерфейса.</span><span class="sxs-lookup"><span data-stu-id="ae187-154">In Windows Vista and earlier it was possible to use English labels regardless of the UI language.</span></span> <span data-ttu-id="ae187-155">В Windows 7 и более поздних версиях Поиск Windows распознает ключевые слова в текущем языке пользовательского интерфейса по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="ae187-155">In Windows 7 and later, Windows Search recognizes keywords in the current default UI language only.</span></span>

### <a name="support-for-custom-properties"></a><span data-ttu-id="ae187-156">Поддержка пользовательских свойств</span><span class="sxs-lookup"><span data-stu-id="ae187-156">Support for Custom Properties</span></span>

<span data-ttu-id="ae187-157">В Windows Vista и более ранних версиях пользовательские свойства недоступны в АКС.</span><span class="sxs-lookup"><span data-stu-id="ae187-157">In Windows Vista and earlier, custom properties were not available in AQS.</span></span> <span data-ttu-id="ae187-158">В Windows 7 и более поздних версиях АКС работает с пользовательскими свойствами, зарегистрированными в системе свойств.</span><span class="sxs-lookup"><span data-stu-id="ae187-158">In Windows 7 and later, AQS works with custom properties that are registered with the property system.</span></span> <span data-ttu-id="ae187-159">Дополнительные сведения о создании пользовательских свойств см. в разделе [система свойств](../properties/building-property-handlers.md).</span><span class="sxs-lookup"><span data-stu-id="ae187-159">For more information on creating custom properties, see [Property System](../properties/building-property-handlers.md).</span></span>

### <a name="datetime-properties-in-windows-8"></a><span data-ttu-id="ae187-160">Свойства даты и времени в Windows 8</span><span class="sxs-lookup"><span data-stu-id="ae187-160">DateTime properties in Windows 8</span></span>

<span data-ttu-id="ae187-161">Начиная с Windows 8, свойства DateTime (например, [System. DateModified](../properties/props-system-datemodified.md)) поддерживают канонический формат даты и времени, заданный [ISO-8601](https://www.w3.org/TR/NOTE-datetime), при необходимости включая часовой пояс UTC.</span><span class="sxs-lookup"><span data-stu-id="ae187-161">As of Windows 8, DateTime properties (like [System.DateModified](../properties/props-system-datemodified.md)) support the canonical date and time format specified by [ISO-8601](https://www.w3.org/TR/NOTE-datetime), optionally including the UTC time zone.</span></span>

-   <span data-ttu-id="ae187-162">**Windows 8 и более ранние версии, Дата и время без часового пояса UTC:** *гггг* - *мм* - *DDThh*:*мм*:*СС*</span><span class="sxs-lookup"><span data-stu-id="ae187-162">**Windows 8 and earlier, date-time without UTC time zone:** *YYYY*-*MM*-*DDThh*:*mm*:*ss*</span></span>

    <span data-ttu-id="ae187-163">Этот формат задает местное время независимо от национальной настройки пользователя или системы.</span><span class="sxs-lookup"><span data-stu-id="ae187-163">This format specifies a local time, regardless of the user or system locale.</span></span>

-   <span data-ttu-id="ae187-164">**Windows 8, Дата-время с часовым поясом UTC:** *гггг* - *мм* - *DDThh*:*мм*:*сстзд*</span><span class="sxs-lookup"><span data-stu-id="ae187-164">**Windows 8, date-time with UTC time zone:** *YYYY*-*MM*-*DDThh*:*mm*:*ssTZD*</span></span>

    <span data-ttu-id="ae187-165">Этот формат задает время в указанном часовом поясе в формате UTC.</span><span class="sxs-lookup"><span data-stu-id="ae187-165">This format specifies a time at the specified UTC time zone.</span></span>

## <a name="keyword-use-in-local-languages"></a><span data-ttu-id="ae187-166">Использование ключевых слов в локальных языках</span><span class="sxs-lookup"><span data-stu-id="ae187-166">Keyword Use in Local Languages</span></span>

<span data-ttu-id="ae187-167">В Windows 7 и более поздних версиях назначенные ключевые слова работают только в системном языке, такие как ключевые слова немецкого языка только в немецкой операционной системе, а ключевые слова на английском языке — только в английской версии операционной системы.</span><span class="sxs-lookup"><span data-stu-id="ae187-167">In Windows 7 and later, mnemonic keywords work in the system language only, such as German keywords only on a German operating system, and English keywords only on an English operating system.</span></span> <span data-ttu-id="ae187-168">[System. Author](../properties/props-system-author.md) — это каноническое ключевое слово, а для свойства System. Author — Author, например,.</span><span class="sxs-lookup"><span data-stu-id="ae187-168">[System.Author](../properties/props-system-author.md) is a canonical keyword, and the mnemonic value for the System.Author property is Author, for example.</span></span> <span data-ttu-id="ae187-169">Введение канонических ключевых слов компенсирует тот факт, что ключевые слова, назначенные английским языком, больше не распознаются во всех операционных системах независимо от языка, как в Windows Vista и более ранних версиях.</span><span class="sxs-lookup"><span data-stu-id="ae187-169">The introduction of canonical keywords compensates for the fact that English mnemonic keywords are no longer universally recognized on all operating systems regardless of language, as was the case in Windows Vista and earlier.</span></span>

> [!Note]  
> <span data-ttu-id="ae187-170">В Windows 7 и более поздних версиях Поиск Windows распознает ключевые слова только в текущем языке по умолчанию, а не на английском языке, если только английская версия не является текущей по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="ae187-170">In Windows 7 and later, Windows Search recognizes keywords in the current default language only, and not in English unless English is the current default.</span></span> <span data-ttu-id="ae187-171">Рекомендуется, чтобы разработчики всегда использовали канонический синтаксис, чтобы их приложения не имели проблем языка с ключевыми словами.</span><span class="sxs-lookup"><span data-stu-id="ae187-171">We recommend that developers always use canonical syntax so that their application won't have language problems with keywords.</span></span>

 

## <a name="canonical-advanced-query-syntax-in-windows-7"></a><span data-ttu-id="ae187-172">Канонический синтаксис расширенных запросов в Windows 7</span><span class="sxs-lookup"><span data-stu-id="ae187-172">Canonical Advanced Query Syntax in Windows 7</span></span>

<span data-ttu-id="ae187-173">Канонический синтаксис был введен для ключевых слов в Windows 7.</span><span class="sxs-lookup"><span data-stu-id="ae187-173">Canonical syntax was introduced for keywords in Windows 7.</span></span> <span data-ttu-id="ae187-174">Примером запроса с каноническим свойством является `System.Message.FromAddress:=me@microsoft.com` .</span><span class="sxs-lookup"><span data-stu-id="ae187-174">An example of a query with a canonical property is `System.Message.FromAddress:=me@microsoft.com`.</span></span> <span data-ttu-id="ae187-175">При кодировании запросов в приложениях, работающих в Windows 7 и более поздних версиях, необходимо использовать канонический синтаксис для программного создания запросов АКС.</span><span class="sxs-lookup"><span data-stu-id="ae187-175">When coding queries in applications running on Windows 7 and later, you must use canonical syntax to programmatically generate AQS queries.</span></span> <span data-ttu-id="ae187-176">Если не использовать канонический синтаксис и приложение развертывается в языковом стандарте или на языке пользовательского интерфейса, отличном от языка в коде приложения, запросы будут интерпретироваться неправильно.</span><span class="sxs-lookup"><span data-stu-id="ae187-176">If you do not use canonical syntax and your application is deployed in a locale or UI language different from the language in the application code, your queries will not be interpreted correctly.</span></span>

<span data-ttu-id="ae187-177">Ниже приведены соглашения для канонического синтаксиса ключевого слова.</span><span class="sxs-lookup"><span data-stu-id="ae187-177">The conventions for canonical keyword syntax are as follows:</span></span>

-   <span data-ttu-id="ae187-178">Каноническим синтаксисом для свойства является его каноническое имя, например `System.Photo.LightSource` .</span><span class="sxs-lookup"><span data-stu-id="ae187-178">The canonical syntax for a property is its canonical name, such as `System.Photo.LightSource`.</span></span> <span data-ttu-id="ae187-179">Канонические имена не учитывают регистр.</span><span class="sxs-lookup"><span data-stu-id="ae187-179">Canonical names are not case sensitive.</span></span>
-   <span data-ttu-id="ae187-180">Канонический синтаксис логических операторов состоит из ключевых слов, или, и не в верхнем регистре.</span><span class="sxs-lookup"><span data-stu-id="ae187-180">The canonical syntax for the Boolean operators consists of the keywords AND, OR, and NOT, in all uppercase.</span></span>
-   <span data-ttu-id="ae187-181">Операторы <, >, = и т. д. не локализуются и поэтому также являются частью канонического синтаксиса.</span><span class="sxs-lookup"><span data-stu-id="ae187-181">The operators <, >, =, and so forth, are not localized and are thus also part of the canonical syntax.</span></span>
-   <span data-ttu-id="ae187-182">Если свойство `P` содержит перечислимые значения или диапазоны с именами N ₁ по NK, то канонический синтаксис для *I*-го значения или диапазона является каноническим именем для P, за которым следует символ \# , а затем N <sub>I</sub>, как показано в следующем примере:</span><span class="sxs-lookup"><span data-stu-id="ae187-182">If a property `P` has enumerated values or ranges named N₁ through Nₖ, the canonical syntax for the *I* th value or range is the canonical name for P, followed by the character \#, followed by N<sub>I</sub>, as illustrated in the following example:</span></span>
    -   <span data-ttu-id="ae187-183">`System.Photo.LightSource#Daylight`, `System.Photo.LightSource#StandardA` и т. д.</span><span class="sxs-lookup"><span data-stu-id="ae187-183">`System.Photo.LightSource#Daylight`, `System.Photo.LightSource#StandardA`, and so forth.</span></span>
-   <span data-ttu-id="ae187-184">Для определенного семантического типа T со значениями или диапазонами с именами N ₁ по NK, каноническим синтаксисом *I*-го значения или диапазона является каноническое имя для T, за которым следует символ \# , а затем — N <sub>I</sub>, как показано в следующем примере:</span><span class="sxs-lookup"><span data-stu-id="ae187-184">For a defined semantic type T with values or ranges named N₁ through Nₖ, the canonical syntax for the *I* th value or range is the canonical name for T, followed by the character \#, followed by N<sub>I</sub>, as illustrated in the following example:</span></span>
    -   `System.Devices.LaunchDeviceStageFromExplorer:=System.StructuredQueryType.Boolean#True`
-   <span data-ttu-id="ae187-185">Для литеральных значений, таких как слова или фразы, канонический синтаксис совпадает с обычным синтаксисом.</span><span class="sxs-lookup"><span data-stu-id="ae187-185">For literal values such as words or phrases, the canonical syntax is the same as the regular syntax.</span></span> <span data-ttu-id="ae187-186">Примеры запросов с литеральными значениями в каноническом синтаксисе:</span><span class="sxs-lookup"><span data-stu-id="ae187-186">Examples of queries with literal values in canonical syntax are:</span></span>
    -   `System.Author:sanjay`
    -   `System.Keywords:"Animal"`
    -   `System.FileCount:>100`

> [!Note]  
> <span data-ttu-id="ae187-187">Не существует канонического синтаксиса для чисел в Windows 7 и более поздних версиях.</span><span class="sxs-lookup"><span data-stu-id="ae187-187">There is no canonical syntax for numbers in Windows 7 and later.</span></span> <span data-ttu-id="ae187-188">Поскольку форматы с плавающей запятой различаются в разных языковых стандартах, использование канонического запроса, включающего константу с плавающей запятой, не поддерживается.</span><span class="sxs-lookup"><span data-stu-id="ae187-188">Because floating point formats vary among locales, the use of a canonical query that involves a floating point constant is not supported.</span></span> <span data-ttu-id="ae187-189">Целочисленные константы, напротив, могут быть написаны только с помощью цифр (без разделителей для тысяч) и могут безопасно использоваться в канонических запросах в Windows 7 и более поздних версиях.</span><span class="sxs-lookup"><span data-stu-id="ae187-189">Integer constants, in contrast, can be written using only digits (no separators for thousands) and can be safely used in canonical queries in Windows 7 and later.</span></span>

 

### <a name="examples"></a><span data-ttu-id="ae187-190">Примеры</span><span class="sxs-lookup"><span data-stu-id="ae187-190">Examples</span></span>

<span data-ttu-id="ae187-191">В следующей таблице приведены некоторые примеры канонических свойств и синтаксис для их использования.</span><span class="sxs-lookup"><span data-stu-id="ae187-191">The following table shows some examples of canonical properties and the syntax for using them.</span></span>



| <span data-ttu-id="ae187-192">Тип канонического свойства</span><span class="sxs-lookup"><span data-stu-id="ae187-192">Type of canonical property</span></span> | <span data-ttu-id="ae187-193">Пример</span><span class="sxs-lookup"><span data-stu-id="ae187-193">Example</span></span>                                                                                     | <span data-ttu-id="ae187-194">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="ae187-194">Syntax</span></span>                                                                                                                                                                                                                                                  |
|----------------------------|---------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="ae187-195">Строковое значение</span><span class="sxs-lookup"><span data-stu-id="ae187-195">String value</span></span>               | [<span data-ttu-id="ae187-196">System.Author</span><span class="sxs-lookup"><span data-stu-id="ae187-196">System.Author</span></span>](../properties/props-system-author.md)<br/>    | <span data-ttu-id="ae187-197">Строковое значение ищется в свойстве Author:</span><span class="sxs-lookup"><span data-stu-id="ae187-197">The string value is searched for in the author property:</span></span> <br/>`System.Author:Jacobs`                                                                                                                                                              |
| <span data-ttu-id="ae187-198">Диапазон перечисления</span><span class="sxs-lookup"><span data-stu-id="ae187-198">Enumeration range</span></span>          | [<span data-ttu-id="ae187-199">System. Priority</span><span class="sxs-lookup"><span data-stu-id="ae187-199">System.Priority</span></span>](../properties/props-system-priority.md)             | <span data-ttu-id="ae187-200">Свойство Priority может иметь числовой диапазон значений:</span><span class="sxs-lookup"><span data-stu-id="ae187-200">The priority property can have a numerical value range:</span></span><br/>`System.Priority:System.Priority#High`                                                                                                                                                |
| <span data-ttu-id="ae187-201">Логическое</span><span class="sxs-lookup"><span data-stu-id="ae187-201">Boolean</span></span>                    | [<span data-ttu-id="ae187-202">System. isDeleted</span><span class="sxs-lookup"><span data-stu-id="ae187-202">System.IsDeleted</span></span>](../properties/props-system-isdeleted.md)<br/> | <span data-ttu-id="ae187-203">Логические значения можно использовать с любым логическим свойством:</span><span class="sxs-lookup"><span data-stu-id="ae187-203">Boolean values can be used with any Boolean property:</span></span><br/><span data-ttu-id="ae187-204">`System.IsDeleted:System.StructuredQueryType.Boolean#True`, и `System.IsDeleted:System.StructuredQueryType.Boolean#False`.</span><span class="sxs-lookup"><span data-stu-id="ae187-204">`System.IsDeleted:System.StructuredQueryType.Boolean#True`, and `System.IsDeleted:System.StructuredQueryType.Boolean#False`</span></span>                                                             |
| <span data-ttu-id="ae187-205">числовые;</span><span class="sxs-lookup"><span data-stu-id="ae187-205">Numerical</span></span>                  | [<span data-ttu-id="ae187-206">System. size</span><span class="sxs-lookup"><span data-stu-id="ae187-206">System.Size</span></span>](../properties/props-system-size.md)<br/>      | <span data-ttu-id="ae187-207">Невозможно безопасно писать канонический запрос, включающий константу с плавающей запятой, так как форматы с плавающей запятой могут различаться в разных языковых стандартах.</span><span class="sxs-lookup"><span data-stu-id="ae187-207">It is not possible to write safely a canonical query that involves a floating point constant, because floating point formats vary among locales.</span></span> <span data-ttu-id="ae187-208">Целые числа должны быть записаны без разделителей для тысяч.</span><span class="sxs-lookup"><span data-stu-id="ae187-208">Integers must be written with no separators for thousands.</span></span> <span data-ttu-id="ae187-209">Пример:</span><span class="sxs-lookup"><span data-stu-id="ae187-209">For example:</span></span><br/>`System.Size:<12345` |



 

<span data-ttu-id="ae187-210">Дополнительные сведения о канонических свойствах и системе свойств обычно см. в разделе [Свойства системы](../properties/props.md).</span><span class="sxs-lookup"><span data-stu-id="ae187-210">For more information about canonical properties and the property system generally, see [System Properties](../properties/props.md).</span></span> <span data-ttu-id="ae187-211">Кроме того, можно обратиться к файлам общедоступного заголовка.</span><span class="sxs-lookup"><span data-stu-id="ae187-211">Alternatively, refer to the public header files.</span></span>

### <a name="query-operators"></a><span data-ttu-id="ae187-212">Операторы запроса</span><span class="sxs-lookup"><span data-stu-id="ae187-212">Query Operators</span></span>

<span data-ttu-id="ae187-213">Если свойство p имеет несколько значений для некоторого элемента, запрос АКС для p: <restr> возвращает элемент, если <restr> имеет **значение true** по крайней мере для одного из значений.</span><span class="sxs-lookup"><span data-stu-id="ae187-213">If a property, p, has multiple values for some item, an AQS query for p:<restr> returns the item if <restr> is **true** for at least one of the values.</span></span> <span data-ttu-id="ae187-214">( <restr> представляет ограничение.)</span><span class="sxs-lookup"><span data-stu-id="ae187-214">(<restr> represents a restriction.)</span></span>

<span data-ttu-id="ae187-215">Синтаксис, приведенный в следующей таблице, состоит из оператора, символа оператора, примера и описания примера.</span><span class="sxs-lookup"><span data-stu-id="ae187-215">The syntax listed in the following table consists of an operator, operator symbol, example and example description.</span></span> <span data-ttu-id="ae187-216">Оператор и символ могут использоваться на любом языке и включаться в любой запрос.</span><span class="sxs-lookup"><span data-stu-id="ae187-216">The operator and symbol can be used in any language and included in any query.</span></span> <span data-ttu-id="ae187-217">Не используйте \_ Операторы неявных или COP \_ приложений COP \_ .</span><span class="sxs-lookup"><span data-stu-id="ae187-217">Do not use the COP\_IMPLICIT or COP\_APPLICATION\_SPECIFIC operators.</span></span> <span data-ttu-id="ae187-218">Некоторые операторы имеют взаимозаменяемые символы.</span><span class="sxs-lookup"><span data-stu-id="ae187-218">Some of the operators have interchangeable symbols.</span></span>



<table>
<colgroup>
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="ae187-219">Оператор</span><span class="sxs-lookup"><span data-stu-id="ae187-219">Operator</span></span></th>
<th><span data-ttu-id="ae187-220">Символ</span><span class="sxs-lookup"><span data-stu-id="ae187-220">Symbol</span></span></th>
<th><span data-ttu-id="ae187-221">Пример</span><span class="sxs-lookup"><span data-stu-id="ae187-221">Example</span></span></th>
<th><span data-ttu-id="ae187-222">Описание</span><span class="sxs-lookup"><span data-stu-id="ae187-222">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="ae187-223">COP_EQUAL</span><span class="sxs-lookup"><span data-stu-id="ae187-223">COP_EQUAL</span></span></td>
<td>=<br/></td>
<td><span data-ttu-id="ae187-224">System. FileExtension: = &quot; . txt&quot;</span><span class="sxs-lookup"><span data-stu-id="ae187-224">System.FileExtension:=&quot;.txt&quot;</span></span><br/></td>
<td><span data-ttu-id="ae187-225">Значение — String &quot; <em>. txt</em> &quot; .</span><span class="sxs-lookup"><span data-stu-id="ae187-225">The value is the string &quot;<em>.txt</em>&quot;.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="ae187-226">COP_NOTEQUAL</span><span class="sxs-lookup"><span data-stu-id="ae187-226">COP_NOTEQUAL</span></span></td>
<td><span data-ttu-id="ae187-227">≠</span><span class="sxs-lookup"><span data-stu-id="ae187-227">≠</span></span><br/> -<br/> &lt;&gt;<br/> <span data-ttu-id="ae187-228">NOT</span><span class="sxs-lookup"><span data-stu-id="ae187-228">NOT</span></span><br/> - -<br/></td>
<td><span data-ttu-id="ae187-229">System. Kind: ≠ рисунок</span><span class="sxs-lookup"><span data-stu-id="ae187-229">System.Kind:≠picture</span></span><br/> <span data-ttu-id="ae187-230">System. photo. Датетакен:-[] ¹</span><span class="sxs-lookup"><span data-stu-id="ae187-230">System.Photo.DateTaken:-[]¹</span></span><br/> <span data-ttu-id="ae187-231">System. Тип: &lt; &gt; Рисунок</span><span class="sxs-lookup"><span data-stu-id="ae187-231">System.Kind:&lt;&gt;picture</span></span><br/> <span data-ttu-id="ae187-232">System. Тип: не рисунок</span><span class="sxs-lookup"><span data-stu-id="ae187-232">System.Kind:NOT picture</span></span><br/> <span data-ttu-id="ae187-233">System. Kind:--рисунок</span><span class="sxs-lookup"><span data-stu-id="ae187-233">System.Kind:- -picture</span></span><br/></td>
<td><span data-ttu-id="ae187-234">Свойство <a href="/windows/desktop/properties/props-system-kind">System. Kind</a> не является изображением.</span><span class="sxs-lookup"><span data-stu-id="ae187-234">The <a href="/windows/desktop/properties/props-system-kind">System.Kind</a> property is not a picture.</span></span><br/> <span data-ttu-id="ae187-235">Свойство <a href="/windows/desktop/properties/props-system-photo-datetaken">System. photo. датетакен</a> имеет значение.</span><span class="sxs-lookup"><span data-stu-id="ae187-235">The <a href="/windows/desktop/properties/props-system-photo-datetaken">System.Photo.DateTaken</a> property has a value.</span></span><br/> <span data-ttu-id="ae187-236">Свойство <a href="/windows/desktop/properties/props-system-kind">System. Kind</a> не является изображением.</span><span class="sxs-lookup"><span data-stu-id="ae187-236">The <a href="/windows/desktop/properties/props-system-kind">System.Kind</a> property is not a picture.</span></span> <br/> <span data-ttu-id="ae187-237">Свойство <a href="/windows/desktop/properties/props-system-kind">System. Kind</a> не является изображением.</span><span class="sxs-lookup"><span data-stu-id="ae187-237">The <a href="/windows/desktop/properties/props-system-kind">System.Kind</a> property is not a picture.</span></span> <br/> <span data-ttu-id="ae187-238">Двойные операторы, применяемые к одному и тому же свойству, не отменяют. Таким образом, System. Kind:--Picture эквивалентен System. Kind:-Picture и System. Kind: NOT Picture.</span><span class="sxs-lookup"><span data-stu-id="ae187-238">Double NOT operators applied to the same property do not cancel out. Hence, System.Kind:- -picture is equivalent to System.Kind:-picture and System.Kind:NOT picture.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="ae187-239">COP_LESSTHAN</span><span class="sxs-lookup"><span data-stu-id="ae187-239">COP_LESSTHAN</span></span></td>
<td>&lt;<br/></td>
<td><span data-ttu-id="ae187-240">System. Size: &lt; 1 КБ</span><span class="sxs-lookup"><span data-stu-id="ae187-240">System.Size:&lt;1kb</span></span><br/></td>
<td><span data-ttu-id="ae187-241">Это значение меньше <em>1 КБ</em>.</span><span class="sxs-lookup"><span data-stu-id="ae187-241">This value is less than <em>1kb</em>.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="ae187-242">COP_GREATERTHAN</span><span class="sxs-lookup"><span data-stu-id="ae187-242">COP_GREATERTHAN</span></span></td>
<td>&gt;<br/></td>
<td><span data-ttu-id="ae187-243">System. Итемдате: &gt; System. структуредкуеритипе. DateTime # сегодня</span><span class="sxs-lookup"><span data-stu-id="ae187-243">System.ItemDate:&gt;System.StructuredQueryType.DateTime#Today</span></span><br/></td>
<td><span data-ttu-id="ae187-244">Это значение больше <em>сегодняшнего</em>.</span><span class="sxs-lookup"><span data-stu-id="ae187-244">This value is greater than <em>today</em>.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="ae187-245">COP_LESSTHANOREQUAL</span><span class="sxs-lookup"><span data-stu-id="ae187-245">COP_LESSTHANOREQUAL</span></span></td>
<td>&lt;=<br/> <span data-ttu-id="ae187-246">≤</span><span class="sxs-lookup"><span data-stu-id="ae187-246">≤</span></span><br/></td>
<td><span data-ttu-id="ae187-247">System. Size: &lt; = 1 КБ</span><span class="sxs-lookup"><span data-stu-id="ae187-247">System.Size:&lt;=1kb</span></span><br/></td>
<td><span data-ttu-id="ae187-248">Это значение меньше или равно <em>1 КБ</em>.</span><span class="sxs-lookup"><span data-stu-id="ae187-248">This value is less than or equal to <em>1kb</em>.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="ae187-249">COP_GREATERTHANOREQUAL</span><span class="sxs-lookup"><span data-stu-id="ae187-249">COP_GREATERTHANOREQUAL</span></span></td>
<td>&gt;=<br/> <span data-ttu-id="ae187-250">≥</span><span class="sxs-lookup"><span data-stu-id="ae187-250">≥</span></span><br/></td>
<td><span data-ttu-id="ae187-251">System. Size: &gt; = 1 КБ</span><span class="sxs-lookup"><span data-stu-id="ae187-251">System.Size:&gt;=1kb</span></span><br/></td>
<td><span data-ttu-id="ae187-252">Это значение равно или больше <em>1 КБ</em>.</span><span class="sxs-lookup"><span data-stu-id="ae187-252">This value is equal to or greater than <em>1kb</em>.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="ae187-253">COP_VALUE_STARTSWITH</span><span class="sxs-lookup"><span data-stu-id="ae187-253">COP_VALUE_STARTSWITH</span></span></td>
<td>~&lt;<br/></td>
<td><span data-ttu-id="ae187-254">System. имя_файла: ~ &lt; &quot; руководство по C++&quot;</span><span class="sxs-lookup"><span data-stu-id="ae187-254">System.FileName:~&lt;&quot;C++ Primer&quot;</span></span><br/></td>
<td><span data-ttu-id="ae187-255">Находит элементы, где имя файла начинается с символов " &quot; <em>учебник по C++</em>" &quot; .</span><span class="sxs-lookup"><span data-stu-id="ae187-255">Finds items where the file name begins with the characters &quot;<em>C++ Primer</em>&quot;.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="ae187-256">COP_VALUE_ENDSWITH</span><span class="sxs-lookup"><span data-stu-id="ae187-256">COP_VALUE_ENDSWITH</span></span></td>
<td>~&gt;<br/></td>
<td><span data-ttu-id="ae187-257">System. photo. Камерамодел: ~ &gt; не</span><span class="sxs-lookup"><span data-stu-id="ae187-257">System.Photo.CameraModel:~&gt;non</span></span><br/></td>
<td><span data-ttu-id="ae187-258">Находит элементы, в которых значение свойства заканчивается символами, <em>не являющимися</em>.</span><span class="sxs-lookup"><span data-stu-id="ae187-258">Finds items where the property value ends with the characters <em>non</em>.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="ae187-259">COP_VALUE_CONTAINS</span><span class="sxs-lookup"><span data-stu-id="ae187-259">COP_VALUE_CONTAINS</span></span></td>
<td>~=<br/> ~~<br/></td>
<td><span data-ttu-id="ae187-260">System. Subject. ~ = округлить</span><span class="sxs-lookup"><span data-stu-id="ae187-260">System.Subject.~=round</span></span> <br/> <span data-ttu-id="ae187-261">System. Search. автосводка: ~ ~ Round</span><span class="sxs-lookup"><span data-stu-id="ae187-261">System.Search.Autosummary:~~round</span></span><br/></td>
<td><span data-ttu-id="ae187-262">Находит сообщение, имеющее эту строку в теме, и соответствует &quot; правилам g<em>Round</em> , &quot; например.</span><span class="sxs-lookup"><span data-stu-id="ae187-262">Finds a message that has this string in the subject, and will match &quot;g<em>round</em> rules&quot; for example.</span></span><br/> <span data-ttu-id="ae187-263">Находит все элементы с автосводками, содержащими символы <em>Round</em>.</span><span class="sxs-lookup"><span data-stu-id="ae187-263">Finds all items with an Autosummary that contains the characters <em>round</em>.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="ae187-264">COP_VALUE_NOTCONTAINS</span><span class="sxs-lookup"><span data-stu-id="ae187-264">COP_VALUE_NOTCONTAINS</span></span></td>
<td><span data-ttu-id="ae187-265">~!</span><span class="sxs-lookup"><span data-stu-id="ae187-265">~!</span></span><br/></td>
<td><span data-ttu-id="ae187-266">System. author: ~! &quot; Санджей&quot;</span><span class="sxs-lookup"><span data-stu-id="ae187-266">System.Author:~!&quot;sanjay&quot;</span></span><br/></td>
<td><span data-ttu-id="ae187-267">Находит авторов, у которых нет последовательности символов, &quot; <em>Санджей</em> &quot; в них.</span><span class="sxs-lookup"><span data-stu-id="ae187-267">Finds authors that do not have the character sequence&quot;<em>sanjay</em>&quot; in them.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="ae187-268">COP_DOSWILDCARDS</span><span class="sxs-lookup"><span data-stu-id="ae187-268">COP_DOSWILDCARDS</span></span></td>
<td>~ <br/></td>
<td><span data-ttu-id="ae187-269">System. имя_файла: ~ &quot; MIC? Ософт W \* d&quot;</span><span class="sxs-lookup"><span data-stu-id="ae187-269">System.FileName:~&quot;Mic?osoft W\*d&quot;</span></span><br/></td>
<td><span data-ttu-id="ae187-270">Поиск файлов, имя файла которых начинается с <em>MIC</em>, за которым следует некоторый символ, затем <em>ософт w</em>, за которым следуют все символы, заканчивающиеся на <em>d</em>.</span><span class="sxs-lookup"><span data-stu-id="ae187-270">Finds files where the file name starts with <em>Mic</em>, followed by some character, followed by <em>osoft w</em>, followed by any characters ending with <em>d</em>.</span></span> <br/> <span data-ttu-id="ae187-271">Знак вопроса</span><span class="sxs-lookup"><span data-stu-id="ae187-271">The ?</span></span> <span data-ttu-id="ae187-272">и \* символы не обрабатываются буквально и работают, как символы-шаблоны в стиле DOS:</span><span class="sxs-lookup"><span data-stu-id="ae187-272">and \* characters are not interpreted literally, and work like DOS-style wildcard characters:</span></span><br/>
<ul>
<li><span data-ttu-id="ae187-273">?</span><span class="sxs-lookup"><span data-stu-id="ae187-273">?</span></span> <span data-ttu-id="ae187-274">соответствует одному произвольному символу.</span><span class="sxs-lookup"><span data-stu-id="ae187-274">matches one arbitrary character.</span></span></li>
<li><span data-ttu-id="ae187-275">\* соответствует нулю или более произвольным символам.</span><span class="sxs-lookup"><span data-stu-id="ae187-275">\* matches zero or more arbitrary characters.</span></span></li>
</ul></td>
</tr>
<tr class="even">
<td><span data-ttu-id="ae187-276">COP_WORD_EQUAL</span><span class="sxs-lookup"><span data-stu-id="ae187-276">COP_WORD_EQUAL</span></span></td>
<td>$=<br/> $$<br/></td>
<td><span data-ttu-id="ae187-277">System. Структуредкуери. виртуальный. from: $ = &quot; Санджей Jacobs&quot;</span><span class="sxs-lookup"><span data-stu-id="ae187-277">System.StructuredQuery.Virtual.From:$=&quot;Sanjay Jacobs&quot;</span></span><br/></td>
<td><span data-ttu-id="ae187-278">Для Windows 7 и более поздних версий.</span><span class="sxs-lookup"><span data-stu-id="ae187-278">For Windows 7 and later.</span></span> <span data-ttu-id="ae187-279">Находит фразу &quot; <em>Санджей Jacobs</em> &quot; во всех свойствах.</span><span class="sxs-lookup"><span data-stu-id="ae187-279">Finds the phrase &quot;<em>Sanjay Jacobs</em>&quot; in all From properties.</span></span> <span data-ttu-id="ae187-280">После слова <em>Санджей</em> должно следовать слово <em>Jacobs</em>.</span><span class="sxs-lookup"><span data-stu-id="ae187-280">The word <em>Sanjay</em> must be followed by the word <em>Jacobs</em>.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="ae187-281">COP_WORD_STARTSWITH</span><span class="sxs-lookup"><span data-stu-id="ae187-281">COP_WORD_STARTSWITH</span></span></td>
<td>$<<br/></td>
<td><span data-ttu-id="ae187-282">System. author: $</span><span class="sxs-lookup"><span data-stu-id="ae187-282">System.Author:$</span></span><&quot;San&quot; System.Filename:$<&quot;Micro Exe&quot;<br/></td>
<td><span data-ttu-id="ae187-283">Для Windows 7 и более поздних версий.</span><span class="sxs-lookup"><span data-stu-id="ae187-283">For Windows 7 and later.</span></span> <span data-ttu-id="ae187-284">Находит любой элемент, где автор содержит слово, начинающееся с символов &quot; <em>San</em> &quot; .</span><span class="sxs-lookup"><span data-stu-id="ae187-284">Finds any item where Author contains a word starting with the characters &quot;<em>San</em>&quot;.</span></span><br/> <span data-ttu-id="ae187-285">Находит любой файл, в котором имя файла содержит слово, начинающееся с <em>Micro</em>, за которым следует слово, начинающееся с <em>exe</em>.</span><span class="sxs-lookup"><span data-stu-id="ae187-285">Finds any file in which the file name contains a word starting with <em>micro</em>, followed by a word starting with <em>exe</em>.</span></span><br/></td>
</tr>
</tbody>
</table>



 

<span data-ttu-id="ae187-286">¹ пустые квадратные скобки ( \[ \] ) обозначают отсутствие значения.</span><span class="sxs-lookup"><span data-stu-id="ae187-286">¹ Empty square brackets (\[\]) denote "no value".</span></span>

<span data-ttu-id="ae187-287">Для строковых свойств операция по умолчанию — COP \_ слово, \_ начинающееся \_ с или COP \_ слово, \_ равно.</span><span class="sxs-lookup"><span data-stu-id="ae187-287">For string properties the default operation is either COP\_WORD\_STARTS\_WITH or COP\_WORD\_EQUAL.</span></span>

### <a name="query-values"></a><span data-ttu-id="ae187-288">Значения запроса</span><span class="sxs-lookup"><span data-stu-id="ae187-288">Query Values</span></span>

<span data-ttu-id="ae187-289">Полезные примеры ограничения значений запросов перечислены в следующей таблице.</span><span class="sxs-lookup"><span data-stu-id="ae187-289">Useful examples of how query values can be restricted are listed in the following table.</span></span>



<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="ae187-290">Значение или символ</span><span class="sxs-lookup"><span data-stu-id="ae187-290">Value/symbol</span></span></th>
<th><span data-ttu-id="ae187-291">Примеры</span><span class="sxs-lookup"><span data-stu-id="ae187-291">Examples</span></span></th>
<th><span data-ttu-id="ae187-292">Описание</span><span class="sxs-lookup"><span data-stu-id="ae187-292">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="ae187-293">Строка</span><span class="sxs-lookup"><span data-stu-id="ae187-293">String</span></span></td>
<td><span data-ttu-id="ae187-294">auto</span><span class="sxs-lookup"><span data-stu-id="ae187-294">auto</span></span><br/></td>
<td><span data-ttu-id="ae187-295">Любая последовательность символов, которую можно искать.</span><span class="sxs-lookup"><span data-stu-id="ae187-295">Any sequence of characters that can be searched for.</span></span> <span data-ttu-id="ae187-296">Строка не должна содержать пробелы или сочетания символов, которые являются частью синтаксиса.</span><span class="sxs-lookup"><span data-stu-id="ae187-296">The string must not contain whitespace or character combinations that are part of the syntax.</span></span> <span data-ttu-id="ae187-297">В этом примере выполняется поиск слова, начинающегося с <em>Auto</em>.</span><span class="sxs-lookup"><span data-stu-id="ae187-297">This example searches for a word beginning with <em>auto</em>.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="ae187-298">Строка в кавычках &quot;&quot;</span><span class="sxs-lookup"><span data-stu-id="ae187-298">Quoted string &quot;&quot;</span></span></td>
<td><span data-ttu-id="ae187-299">&quot;Выводы: действительная &quot; &quot; &quot; &quot; Группа "синий &quot; &quot; "&quot;</span><span class="sxs-lookup"><span data-stu-id="ae187-299">&quot;Conclusions: valid&quot; &quot;The &quot;&quot;blue&quot;&quot; team&quot;</span></span><br/></td>
<td><span data-ttu-id="ae187-300">Любая последовательность символов.</span><span class="sxs-lookup"><span data-stu-id="ae187-300">Any sequence of characters.</span></span> <span data-ttu-id="ae187-301">Строка не интерпретируется как часть синтаксиса.</span><span class="sxs-lookup"><span data-stu-id="ae187-301">The string is not interpreted as part of the syntax.</span></span><br/> <span data-ttu-id="ae187-302">Кавычки могут включаться в запрос, если они являются двойными.</span><span class="sxs-lookup"><span data-stu-id="ae187-302">Quotation marks can be included in a query if they are doubled.</span></span> <span data-ttu-id="ae187-303">В этом примере выполняется <em>Поиск &quot; синей &quot; команды</em>.</span><span class="sxs-lookup"><span data-stu-id="ae187-303">This example searches for <em>The &quot;blue&quot; team</em>.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="ae187-304">Целочисленный тип</span><span class="sxs-lookup"><span data-stu-id="ae187-304">Integer</span></span></td>
<td><span data-ttu-id="ae187-305">5678</span><span class="sxs-lookup"><span data-stu-id="ae187-305">5678</span></span><br/></td>
<td><span data-ttu-id="ae187-306">Для целых чисел следует использовать только цифры.</span><span class="sxs-lookup"><span data-stu-id="ae187-306">Use only digits for integers.</span></span> <span data-ttu-id="ae187-307">Не используйте разделители для тысяч.</span><span class="sxs-lookup"><span data-stu-id="ae187-307">Do not use any separators for thousands.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="ae187-308">Число с плавающей запятой</span><span class="sxs-lookup"><span data-stu-id="ae187-308">Floating point number</span></span></td>
<td><span data-ttu-id="ae187-309">5678,1234</span><span class="sxs-lookup"><span data-stu-id="ae187-309">5678.1234</span></span><br/></td>
<td><span data-ttu-id="ae187-310">Поскольку форматы с плавающей запятой различаются в разных языковых стандартах, канонические запросы не могут использовать константу с плавающей запятой.</span><span class="sxs-lookup"><span data-stu-id="ae187-310">Because floating point formats vary among locales, a canonical query cannot use a floating point constant.</span></span> <span data-ttu-id="ae187-311">Использование канонического синтаксиса с числами с плавающей запятой не является типобезопасным.</span><span class="sxs-lookup"><span data-stu-id="ae187-311">The use of canonical syntax with floating point numbers is not localization safe.</span></span> <br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="ae187-312">Логическое <strong>значение true</strong> / <strong>false</strong></span><span class="sxs-lookup"><span data-stu-id="ae187-312">Boolean <strong>true</strong>/<strong>false</strong></span></span></td>
<td><span data-ttu-id="ae187-313">System. читал: = System. Структуредкуеритипе. Boolean # true</span><span class="sxs-lookup"><span data-stu-id="ae187-313">System.IsRead:=System.StructuredQueryType.Boolean#True</span></span><br/> <span data-ttu-id="ae187-314">System. encrypted:-System. Структуредкуеритипе. Boolean # false</span><span class="sxs-lookup"><span data-stu-id="ae187-314">System.IsEncrypted:-System.StructuredQueryType.Boolean#False</span></span><br/></td>
<td><span data-ttu-id="ae187-315"><strong>Истинное</strong> логическое значение.</span><span class="sxs-lookup"><span data-stu-id="ae187-315">The <strong>TRUE</strong> Boolean value.</span></span><br/> <span data-ttu-id="ae187-316">Логическое значение <strong>false</strong> .</span><span class="sxs-lookup"><span data-stu-id="ae187-316">The <strong>FALSE</strong> Boolean value.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="ae187-317">[]</span><span class="sxs-lookup"><span data-stu-id="ae187-317">[]</span></span></td>
<td><span data-ttu-id="ae187-318">System. Keywords: = []</span><span class="sxs-lookup"><span data-stu-id="ae187-318">System.Keywords:=[]</span></span><br/></td>
<td><span data-ttu-id="ae187-319">Пустые квадратные скобки обозначают отсутствие значения.</span><span class="sxs-lookup"><span data-stu-id="ae187-319">Empty square brackets denote that there is no value.</span></span> <span data-ttu-id="ae187-320">В этом примере выполняется поиск всех элементов, которые не были помечены тегом.</span><span class="sxs-lookup"><span data-stu-id="ae187-320">This example finds all items that have not been tagged.</span></span> <br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="ae187-321">Абсолютные даты</span><span class="sxs-lookup"><span data-stu-id="ae187-321">Absolute dates</span></span></td>
<td><span data-ttu-id="ae187-322">System. Итемдате: 1/26/2010</span><span class="sxs-lookup"><span data-stu-id="ae187-322">System.ItemDate:1/26/2010</span></span><br/> <span data-ttu-id="ae187-323">Системдатемодифиед 10/15/2002 19:00</span><span class="sxs-lookup"><span data-stu-id="ae187-323">SystemDateModified 10/15/2002 19:00</span></span><br/></td>
<td><span data-ttu-id="ae187-324">Находит элементы с датой 26 января 2010.</span><span class="sxs-lookup"><span data-stu-id="ae187-324">Finds items with a date of 26 January 2010.</span></span><br/> <span data-ttu-id="ae187-325">Находит элементы, которые были изменены 15 октября 2002 в течение 19:00:00 и 19:00:59.</span><span class="sxs-lookup"><span data-stu-id="ae187-325">Finds items that were modified on 15 October 2002 between the hours 19:00:00 and 19:00:59.</span></span> <br/>
<blockquote>
[!Note]<br />
<span data-ttu-id="ae187-326">Так как форматы даты (например, форматы с плавающей запятой) различаются в разных языковых стандартах, использование канонического синтаксиса с абсолютными датами не поддерживается и не является типобезопасным.</span><span class="sxs-lookup"><span data-stu-id="ae187-326">Because date formats (like floating point formats) vary among locales, the use of canonical syntax with absolute dates is not supported and is not localization safe.</span></span>
</blockquote>
<br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="ae187-327">Относительные даты</span><span class="sxs-lookup"><span data-stu-id="ae187-327">Relative dates</span></span></td>
<td><span data-ttu-id="ae187-328">System. Итемдате: System. Структуредкуеритипе. DateTime # сегодня</span><span class="sxs-lookup"><span data-stu-id="ae187-328">System.ItemDate:System.StructuredQueryType.DateTime#Today</span></span><br/> <span data-ttu-id="ae187-329">System. Датеаккуиред: System. Структуредкуеритипе. DateTime # NextMonth</span><span class="sxs-lookup"><span data-stu-id="ae187-329">System.DateAcquired:System.StructuredQueryType.DateTime#NextMonth</span></span><br/> <span data-ttu-id="ae187-330">System. Message. Датерецеивед: System. Структуредкуеритипе. DateTime # Ластеар</span><span class="sxs-lookup"><span data-stu-id="ae187-330">System.Message.DateReceived:System.StructuredQueryType.DateTime#LastYear</span></span><br/></td>
<td><span data-ttu-id="ae187-331">Поиск элементов с сегодняшней датой.</span><span class="sxs-lookup"><span data-stu-id="ae187-331">Finds items with today's date.</span></span><br/> <span data-ttu-id="ae187-332">Находит элементы с датой в следующем месяце.</span><span class="sxs-lookup"><span data-stu-id="ae187-332">Finds items with a date in the next month.</span></span><br/> <span data-ttu-id="ae187-333">Находит элементы с датой за прошлый год.</span><span class="sxs-lookup"><span data-stu-id="ae187-333">Finds items with a date in the last year.</span></span><br/>
<blockquote>
[!Note]<br />
<span data-ttu-id="ae187-334">Помимо поиска по конкретным датам и диапазонам дат, АКС распознает относительные значения даты (например, <em>сегодня</em>, <em>завтра</em>, <em>некствик</em>, <em>Nextmonth</em>) и Day (например, <em>вторник</em> или понедельник). <em> Среда</em>) и месяц (<em>Февраль</em>).</span><span class="sxs-lookup"><span data-stu-id="ae187-334">In addition to searching on specific dates and date ranges, AQS recognizes relative date values (like <em>today</em>, <em>tomorrow</em>, <em>nextweek</em>, <em>nextmonth</em>), and day (like <em>Tuesday</em> or <em>Monday..Wednesday</em>), and month (<em>February</em>).</span></span>
</blockquote>
<br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="ae187-335">..</span><span class="sxs-lookup"><span data-stu-id="ae187-335">..</span></span></td>
<td><span data-ttu-id="ae187-336">System. Итемдате: 11/05/04.. 11/10/04 System. Size: 5Kb.. 10 КБ</span><span class="sxs-lookup"><span data-stu-id="ae187-336">System.ItemDate:11/05/04..11/10/04 System.Size:5kb..10kb</span></span><br/></td>
<td><span data-ttu-id="ae187-337">Диапазон значений указывается в двойных периодах.</span><span class="sxs-lookup"><span data-stu-id="ae187-337">Double periods indicate a value range.</span></span> <span data-ttu-id="ae187-338">Находит элементы с датой в диапазоне от 11/05/04 до 11/10/04 включительно.</span><span class="sxs-lookup"><span data-stu-id="ae187-338">Finds items with a date between 11/05/04 and 11/10/04, inclusive.</span></span><br/> <span data-ttu-id="ae187-339">Находит элементы от 5 до 10 КБ в размере.</span><span class="sxs-lookup"><span data-stu-id="ae187-339">Finds items between 5 and 10kb in size.</span></span><br/></td>
</tr>
</tbody>
</table>



 

## <a name="scope-restrictions"></a><span data-ttu-id="ae187-340">Ограничения области</span><span class="sxs-lookup"><span data-stu-id="ae187-340">Scope Restrictions</span></span>

<span data-ttu-id="ae187-341">Пользователи могут ограничить область поиска для конкретных расположений папок или хранилищ данных.</span><span class="sxs-lookup"><span data-stu-id="ae187-341">Users can limit the scope of their searches to specific folder locations or data stores.</span></span> <span data-ttu-id="ae187-342">Например, если вы используете несколько учетных записей электронной почты и хотите ограничить запрос либо с Microsoft Outlook, либо с помощью Microsoft Outlook Express, можно использовать `System.Search.Store:mapi` или `System.Search.Store:oe` соответственно.</span><span class="sxs-lookup"><span data-stu-id="ae187-342">For example, if you use several email accounts and you want to limit a query to either Microsoft Outlook or Microsoft Outlook Express, you can use `System.Search.Store:mapi` or `System.Search.Store:oe` respectively.</span></span> <span data-ttu-id="ae187-343">В следующей таблице приведены некоторые примеры ограничения поиска по хранилищу данных.</span><span class="sxs-lookup"><span data-stu-id="ae187-343">The following table shows some examples of how to restrict a search by data store.</span></span>



| <span data-ttu-id="ae187-344">Ограничить поиск по хранилищу данных</span><span class="sxs-lookup"><span data-stu-id="ae187-344">Restrict search by data store</span></span>  | <span data-ttu-id="ae187-345">Ключевое слово</span><span class="sxs-lookup"><span data-stu-id="ae187-345">Keyword</span></span> | <span data-ttu-id="ae187-346">Пример</span><span class="sxs-lookup"><span data-stu-id="ae187-346">Example</span></span>                                     |
|--------------------------------|---------|---------------------------------------------|
| <span data-ttu-id="ae187-347">Файлы</span><span class="sxs-lookup"><span data-stu-id="ae187-347">Files</span></span>                          | <span data-ttu-id="ae187-348">файл</span><span class="sxs-lookup"><span data-stu-id="ae187-348">file</span></span>    | <span data-ttu-id="ae187-349">System. Search. Store: файл</span><span class="sxs-lookup"><span data-stu-id="ae187-349">System.Search.Store:file</span></span>                    |
| <span data-ttu-id="ae187-350">Outlook</span><span class="sxs-lookup"><span data-stu-id="ae187-350">Outlook</span></span>                        | <span data-ttu-id="ae187-351">действует</span><span class="sxs-lookup"><span data-stu-id="ae187-351">mapi</span></span>    | <span data-ttu-id="ae187-352">System. Search. Store: MAPI</span><span class="sxs-lookup"><span data-stu-id="ae187-352">System.Search.Store:mapi</span></span>                    |
| <span data-ttu-id="ae187-353">Outlook Express</span><span class="sxs-lookup"><span data-stu-id="ae187-353">Outlook Express</span></span>                | <span data-ttu-id="ae187-354">OE</span><span class="sxs-lookup"><span data-stu-id="ae187-354">oe</span></span>      | <span data-ttu-id="ae187-355">System. Search. Store: OE</span><span class="sxs-lookup"><span data-stu-id="ae187-355">System.Search.Store:oe</span></span>                      |
| <span data-ttu-id="ae187-356">автономные файлы;</span><span class="sxs-lookup"><span data-stu-id="ae187-356">Offline files</span></span>                  | <span data-ttu-id="ae187-357">CSC</span><span class="sxs-lookup"><span data-stu-id="ae187-357">csc</span></span>     | <span data-ttu-id="ae187-358">System. Search. Store: CSC</span><span class="sxs-lookup"><span data-stu-id="ae187-358">System.Search.Store:csc</span></span>                     |
| <span data-ttu-id="ae187-359">Определенная папка на локальном диске</span><span class="sxs-lookup"><span data-stu-id="ae187-359">Specific folder on local drive</span></span> | <span data-ttu-id="ae187-360">folder</span><span class="sxs-lookup"><span data-stu-id="ae187-360">folder</span></span>  | <span data-ttu-id="ae187-361">System. Итемфолдернамедисплай: C: " \\ MyFolder"</span><span class="sxs-lookup"><span data-stu-id="ae187-361">System.ItemFolderNameDisplay:C:"\\MyFolder"</span></span> |



 

## <a name="additional-resources"></a><span data-ttu-id="ae187-362">Дополнительные ресурсы</span><span class="sxs-lookup"><span data-stu-id="ae187-362">Additional Resources</span></span>

-   <span data-ttu-id="ae187-363">В Windows 7 и более поздних версиях параметр контекстного меню может быть доступен в зависимости от того, выполнено ли условие АКС.</span><span class="sxs-lookup"><span data-stu-id="ae187-363">In Windows 7 and later, a shortcut menu option can be available based on whether an AQS condition is met.</span></span> <span data-ttu-id="ae187-364">Дополнительные сведения см. в разделе «получение динамического поведения для статических команд с помощью расширенного синтаксиса запросов» раздела [Создание обработчиков контекстного меню](../shell/context-menu-handlers.md).</span><span class="sxs-lookup"><span data-stu-id="ae187-364">For more information, see "Getting Dynamic Behavior for Static Verbs by Using Advanced Query Syntax" in [Creating Context Menu Handlers](../shell/context-menu-handlers.md).</span></span>
-   <span data-ttu-id="ae187-365">Запросы АКС могут быть ограничены определенными типами файлов, которые называются типами файлов.</span><span class="sxs-lookup"><span data-stu-id="ae187-365">AQS queries can be limited to specific types of files, which are known as file kinds.</span></span> <span data-ttu-id="ae187-366">Дополнительные сведения см. в разделе [типы файлов и ассоциации](../shell/fa-intro.md).</span><span class="sxs-lookup"><span data-stu-id="ae187-366">For more information, see [File Types and Associations](../shell/fa-intro.md).</span></span> <span data-ttu-id="ae187-367">Справочную документацию по свойствам см. в разделе [System. Kind](../properties/props-system-kind.md)и [System. киндтекст](../properties/props-system-kindtext.md).</span><span class="sxs-lookup"><span data-stu-id="ae187-367">For property reference documentation, see [System.Kind](../properties/props-system-kind.md), and [System.KindText](../properties/props-system-kindtext.md).</span></span>

## <a name="related-topics"></a><span data-ttu-id="ae187-368">См. также</span><span class="sxs-lookup"><span data-stu-id="ae187-368">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="ae187-369">Отправка программных запросов к индексу</span><span class="sxs-lookup"><span data-stu-id="ae187-369">Querying the Index Programmatically</span></span>](-search-3x-wds-qryidx-overview.md)
</dt> <dt>

[<span data-ttu-id="ae187-370">Использование методов SQL и АКС для запроса индекса</span><span class="sxs-lookup"><span data-stu-id="ae187-370">Using SQL and AQS Approaches to Query the Index</span></span>](-search-3x-wds-qryidx-overview.md)
</dt> <dt>

[<span data-ttu-id="ae187-371">Запрос индекса с помощью Исеарчкуерихелпер</span><span class="sxs-lookup"><span data-stu-id="ae187-371">Querying the Index with ISearchQueryHelper</span></span>](-search-3x-wds-qryidx-searchqueryhelper.md)
</dt> <dt>

[<span data-ttu-id="ae187-372">Запрос индекса с помощью протокола Search-MS</span><span class="sxs-lookup"><span data-stu-id="ae187-372">Querying the Index with the search-ms Protocol</span></span>](-search-3x-wds-qryidx-searchms.md)
</dt> <dt>

[<span data-ttu-id="ae187-373">Запрос к индексу с помощью синтаксиса SQL для поиска Windows</span><span class="sxs-lookup"><span data-stu-id="ae187-373">Querying the Index with Windows Search SQL Syntax</span></span>](-search-sql-windowssearch-entry.md)
</dt> </dl>

 

 
