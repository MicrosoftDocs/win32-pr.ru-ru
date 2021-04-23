---
title: Соглашения о стиле написания кода
description: В этой серии примеров используются соглашения о стиле написания кода для облегчения ясности и согласованности.
ms.assetid: d5e81a52-79f6-4561-891c-05fee125a1b0
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e28e65e19d69f060a5f85d86976c4bd3694f7611
ms.sourcegitcommit: a716ca2a6a22a400f02c6b31699cf4da83ee3619
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/04/2020
ms.locfileid: "103797371"
---
# <a name="coding-style-conventions"></a><span data-ttu-id="01264-103">Соглашения о стиле написания кода</span><span class="sxs-lookup"><span data-stu-id="01264-103">Coding Style Conventions</span></span>

<span data-ttu-id="01264-104">В этой серии примеров используются соглашения о стиле написания кода для облегчения ясности и согласованности.</span><span class="sxs-lookup"><span data-stu-id="01264-104">Coding style conventions are used in this sample series to aid clarity and consistency.</span></span> <span data-ttu-id="01264-105">Используются соглашения об нотации "Венгерский".</span><span class="sxs-lookup"><span data-stu-id="01264-105">The "Hungarian" notation conventions are used.</span></span> <span data-ttu-id="01264-106">Они стали распространенной практикой программирования в программировании Win32.</span><span class="sxs-lookup"><span data-stu-id="01264-106">These have become a common coding practice in Win32 programming.</span></span> <span data-ttu-id="01264-107">Они включают в себя обозначения префикса переменной, которые придают именам переменных предложение типа переменной.</span><span class="sxs-lookup"><span data-stu-id="01264-107">They include variable prefix notations that give to variable names a suggestion of the type of the variable.</span></span>

<span data-ttu-id="01264-108">В следующей таблице перечислены стандартные префиксы.</span><span class="sxs-lookup"><span data-stu-id="01264-108">The following table lists common prefixes.</span></span>



| <span data-ttu-id="01264-109">Prefix</span><span class="sxs-lookup"><span data-stu-id="01264-109">Prefix</span></span> | <span data-ttu-id="01264-110">Описание</span><span class="sxs-lookup"><span data-stu-id="01264-110">Description</span></span>                         |
|--------|-------------------------------------|
| <span data-ttu-id="01264-111">а</span><span class="sxs-lookup"><span data-stu-id="01264-111">a</span></span>      | <span data-ttu-id="01264-112">Array</span><span class="sxs-lookup"><span data-stu-id="01264-112">Array</span></span>                               |
| <span data-ttu-id="01264-113">b</span><span class="sxs-lookup"><span data-stu-id="01264-113">b</span></span>      | <span data-ttu-id="01264-114">BOOL (int)</span><span class="sxs-lookup"><span data-stu-id="01264-114">BOOL (int)</span></span>                          |
| <span data-ttu-id="01264-115">c</span><span class="sxs-lookup"><span data-stu-id="01264-115">c</span></span>      | <span data-ttu-id="01264-116">Char</span><span class="sxs-lookup"><span data-stu-id="01264-116">Char</span></span>                                |
| <span data-ttu-id="01264-117">CB</span><span class="sxs-lookup"><span data-stu-id="01264-117">cb</span></span>     | <span data-ttu-id="01264-118">Число байтов</span><span class="sxs-lookup"><span data-stu-id="01264-118">Count of bytes</span></span>                      |
| <span data-ttu-id="01264-119">Кредит</span><span class="sxs-lookup"><span data-stu-id="01264-119">cr</span></span>     | <span data-ttu-id="01264-120">Значение ссылки цвета</span><span class="sxs-lookup"><span data-stu-id="01264-120">Color reference value</span></span>               |
| <span data-ttu-id="01264-121">/CX</span><span class="sxs-lookup"><span data-stu-id="01264-121">cx</span></span>     | <span data-ttu-id="01264-122">Число x (коротких)</span><span class="sxs-lookup"><span data-stu-id="01264-122">Count of x (short)</span></span>                  |
| <span data-ttu-id="01264-123">dw</span><span class="sxs-lookup"><span data-stu-id="01264-123">dw</span></span>     | <span data-ttu-id="01264-124">DWORD (без знака)</span><span class="sxs-lookup"><span data-stu-id="01264-124">DWORD (unsigned long)</span></span>               |
| <span data-ttu-id="01264-125">f</span><span class="sxs-lookup"><span data-stu-id="01264-125">f</span></span>      | <span data-ttu-id="01264-126">Флаги (обычно несколько битовых значений)</span><span class="sxs-lookup"><span data-stu-id="01264-126">Flags (usually multiple bit values)</span></span> |
| <span data-ttu-id="01264-127">fn</span><span class="sxs-lookup"><span data-stu-id="01264-127">fn</span></span>     | <span data-ttu-id="01264-128">Функция</span><span class="sxs-lookup"><span data-stu-id="01264-128">Function</span></span>                            |
| <span data-ttu-id="01264-129">модуле\_</span><span class="sxs-lookup"><span data-stu-id="01264-129">g\_</span></span>    | <span data-ttu-id="01264-130">Глобальный</span><span class="sxs-lookup"><span data-stu-id="01264-130">Global</span></span>                              |
| <span data-ttu-id="01264-131">h</span><span class="sxs-lookup"><span data-stu-id="01264-131">h</span></span>      | <span data-ttu-id="01264-132">Дескриптор</span><span class="sxs-lookup"><span data-stu-id="01264-132">Handle</span></span>                              |
| <span data-ttu-id="01264-133">i</span><span class="sxs-lookup"><span data-stu-id="01264-133">i</span></span>      | <span data-ttu-id="01264-134">Целочисленный тип</span><span class="sxs-lookup"><span data-stu-id="01264-134">Integer</span></span>                             |
| <span data-ttu-id="01264-135">l</span><span class="sxs-lookup"><span data-stu-id="01264-135">l</span></span>      | <span data-ttu-id="01264-136">Long</span><span class="sxs-lookup"><span data-stu-id="01264-136">Long</span></span>                                |
| <span data-ttu-id="01264-137">lp</span><span class="sxs-lookup"><span data-stu-id="01264-137">lp</span></span>     | <span data-ttu-id="01264-138">Длинный указатель</span><span class="sxs-lookup"><span data-stu-id="01264-138">Long pointer</span></span>                        |
| <span data-ttu-id="01264-139">Пн\_</span><span class="sxs-lookup"><span data-stu-id="01264-139">m\_</span></span>    | <span data-ttu-id="01264-140">Элемент данных класса</span><span class="sxs-lookup"><span data-stu-id="01264-140">Data member of a class</span></span>              |
| <span data-ttu-id="01264-141">n</span><span class="sxs-lookup"><span data-stu-id="01264-141">n</span></span>      | <span data-ttu-id="01264-142">Короткое целое</span><span class="sxs-lookup"><span data-stu-id="01264-142">Short int</span></span>                           |
| <span data-ttu-id="01264-143">p</span><span class="sxs-lookup"><span data-stu-id="01264-143">p</span></span>      | <span data-ttu-id="01264-144">Указатель</span><span class="sxs-lookup"><span data-stu-id="01264-144">Pointer</span></span>                             |
| <span data-ttu-id="01264-145">s</span><span class="sxs-lookup"><span data-stu-id="01264-145">s</span></span>      | <span data-ttu-id="01264-146">Строка</span><span class="sxs-lookup"><span data-stu-id="01264-146">String</span></span>                              |
| <span data-ttu-id="01264-147">SZ</span><span class="sxs-lookup"><span data-stu-id="01264-147">sz</span></span>     | <span data-ttu-id="01264-148">Строка, завершающаяся нулем</span><span class="sxs-lookup"><span data-stu-id="01264-148">Zero terminated String</span></span>              |
| <span data-ttu-id="01264-149">tm</span><span class="sxs-lookup"><span data-stu-id="01264-149">tm</span></span>     | <span data-ttu-id="01264-150">Метрика текста</span><span class="sxs-lookup"><span data-stu-id="01264-150">Text metric</span></span>                         |
| <span data-ttu-id="01264-151">u</span><span class="sxs-lookup"><span data-stu-id="01264-151">u</span></span>      | <span data-ttu-id="01264-152">Целое число без знака</span><span class="sxs-lookup"><span data-stu-id="01264-152">Unsigned int</span></span>                        |
| <span data-ttu-id="01264-153">признан</span><span class="sxs-lookup"><span data-stu-id="01264-153">ul</span></span>     | <span data-ttu-id="01264-154">Long без знака (ULONG)</span><span class="sxs-lookup"><span data-stu-id="01264-154">Unsigned long (ULONG)</span></span>               |
| <span data-ttu-id="01264-155">w</span><span class="sxs-lookup"><span data-stu-id="01264-155">w</span></span>      | <span data-ttu-id="01264-156">WORD (без знака)</span><span class="sxs-lookup"><span data-stu-id="01264-156">WORD (unsigned short)</span></span>               |
| <span data-ttu-id="01264-157">x, y</span><span class="sxs-lookup"><span data-stu-id="01264-157">x,y</span></span>    | <span data-ttu-id="01264-158">координаты x, y (краткое)</span><span class="sxs-lookup"><span data-stu-id="01264-158">x, y coordinates (short)</span></span>            |



 

<span data-ttu-id="01264-159">Они часто объединяются, как показано ниже.</span><span class="sxs-lookup"><span data-stu-id="01264-159">These are often combined, as in the following.</span></span>



| <span data-ttu-id="01264-160">Сочетание префикса</span><span class="sxs-lookup"><span data-stu-id="01264-160">Prefix combination</span></span> | <span data-ttu-id="01264-161">Описание</span><span class="sxs-lookup"><span data-stu-id="01264-161">Description</span></span>                                             |
|--------------------|---------------------------------------------------------|
| <span data-ttu-id="01264-162">псзмистринг</span><span class="sxs-lookup"><span data-stu-id="01264-162">pszMyString</span></span>        | <span data-ttu-id="01264-163">Указатель на строку.</span><span class="sxs-lookup"><span data-stu-id="01264-163">A pointer to a string.</span></span>                                  |
| <span data-ttu-id="01264-164">m \_ псзмистринг</span><span class="sxs-lookup"><span data-stu-id="01264-164">m\_pszMyString</span></span>     | <span data-ttu-id="01264-165">Указатель на строку, которая является элементом данных класса.</span><span class="sxs-lookup"><span data-stu-id="01264-165">A pointer to a string that is a data member of a class.</span></span> |



 

<span data-ttu-id="01264-166">Другие соглашения перечислены в следующей таблице.</span><span class="sxs-lookup"><span data-stu-id="01264-166">Other conventions are listed in the following table.</span></span>



| <span data-ttu-id="01264-167">Обозначение</span><span class="sxs-lookup"><span data-stu-id="01264-167">Convention</span></span>       | <span data-ttu-id="01264-168">Описание</span><span class="sxs-lookup"><span data-stu-id="01264-168">Description</span></span>                                              |
|------------------|----------------------------------------------------------|
| <span data-ttu-id="01264-169">кмикласс</span><span class="sxs-lookup"><span data-stu-id="01264-169">CMyClass</span></span>         | <span data-ttu-id="01264-170">Префикс "C" для имен классов C++.</span><span class="sxs-lookup"><span data-stu-id="01264-170">Prefix 'C' for C++ class names.</span></span>                          |
| <span data-ttu-id="01264-171">комйобжекткласс</span><span class="sxs-lookup"><span data-stu-id="01264-171">COMyObjectClass</span></span>  | <span data-ttu-id="01264-172">Добавьте префикс "CO" для имен классов COM-объектов.</span><span class="sxs-lookup"><span data-stu-id="01264-172">Prefix 'CO' for COM object class names.</span></span>                  |
| <span data-ttu-id="01264-173">кфмиклассфактори</span><span class="sxs-lookup"><span data-stu-id="01264-173">CFMyClassFactory</span></span> | <span data-ttu-id="01264-174">Добавьте в префикс "CF" имена фабрик класса COM.</span><span class="sxs-lookup"><span data-stu-id="01264-174">Prefix 'CF' for COM class factory names.</span></span>                 |
| <span data-ttu-id="01264-175">IMyInterface</span><span class="sxs-lookup"><span data-stu-id="01264-175">IMyInterface</span></span>     | <span data-ttu-id="01264-176">Префикс "I" для имен классов интерфейса COM.</span><span class="sxs-lookup"><span data-stu-id="01264-176">Prefix 'I' for COM interface class names.</span></span>                |
| <span data-ttu-id="01264-177">Цимпиминтерфаце</span><span class="sxs-lookup"><span data-stu-id="01264-177">CImpIMyInterface</span></span> | <span data-ttu-id="01264-178">Для классов реализации COM-интерфейса следует добавить префикс "Цимпи".</span><span class="sxs-lookup"><span data-stu-id="01264-178">Prefix 'CImpI' for COM interface implementation classes.</span></span> |



 

<span data-ttu-id="01264-179">Некоторые последовательные соглашения для блоков заголовков комментариев используются в этой серии примеров, как показано ниже.</span><span class="sxs-lookup"><span data-stu-id="01264-179">Some consistent conventions for comment header blocks are used in this sample series as follows.</span></span>

## <a name="file-header"></a><span data-ttu-id="01264-180">Заголовок файла</span><span class="sxs-lookup"><span data-stu-id="01264-180">File Header</span></span>

``` syntax
/*+===================================================================
  File:      MYFILE.EXT

  Summary:   Brief summary of the file contents and purpose.

  Classes:   Classes declared or used (in source files).

  Functions: Functions exported (in source files).

  Origin:    Indications of where content may have come from. This
             is not a change history but rather a reference to the
             editor-inheritance behind the content or other
             indications about the origin of the source.

  Copyright and Legal notices.
  Copyright and Legal notices.
===================================================================+*/
```

## <a name="plain-comment-block"></a><span data-ttu-id="01264-181">Блок простых комментариев</span><span class="sxs-lookup"><span data-stu-id="01264-181">Plain Comment Block</span></span>

``` syntax
/*--------------------------------------------------------------------
  Plain block of comment text that usually takes several lines.
  Plain block of comment text that usually takes several lines.
--------------------------------------------------------------------*/
```

## <a name="class-declaration-header"></a><span data-ttu-id="01264-182">Заголовок объявления класса</span><span class="sxs-lookup"><span data-stu-id="01264-182">Class Declaration Header</span></span>

``` syntax
/*C+C+++C+++C+++C+++C+++C+++C+++C+++C+++C+++C+++C+++C+++C+++C+++C+++C
  Class:    CMyClass

  Summary:  Short summary of purpose and content of CMyClass.
            Short summary of purpose and content of CMyClass.

  Methods:  MyMethodOne
              Short description of MyMethodOne.
            MyMethodTwo
              Short description of MyMethodTwo.
            CMyClass
              Constructor.
            ~CMyClass
              Destructor.
C---C---C---C---C---C---C---C---C---C---C---C---C---C---C---C---C-C*/
```

## <a name="class-method-definition-header"></a><span data-ttu-id="01264-183">Заголовок определения метода класса</span><span class="sxs-lookup"><span data-stu-id="01264-183">Class Method Definition Header</span></span>

``` syntax
/*M+M+++M+++M+++M+++M+++M+++M+++M+++M+++M+++M+++M+++M+++M+++M+++M+++M
  Method:   CMyClass::MyMethodOne

  Summary:  Short summary of purpose and content of MyMethodOne.
            Short summary of purpose and content of MyMethodOne.

  Args:     MYTYPE MyArgOne
              Short description of argument MyArgOne.
            MYTYPE MyArgTwo
              Short description of argument MyArgTwo.

  Modifies: [list of member data variables modified by this method].

  Returns:  MYRETURNTYPE
              Short description of meaning of the return type values.
M---M---M---M---M---M---M---M---M---M---M---M---M---M---M---M---M-M*/
```

## <a name="unexported-or-local-function"></a><span data-ttu-id="01264-184">Неэкспортированная или локальная функция</span><span class="sxs-lookup"><span data-stu-id="01264-184">Unexported or Local Function</span></span>

``` syntax
/*F+F+++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++
  Function: MyLocalFunction

  Summary:  What MyLocalFunction is for and what it does.

  Args:     MYTYPE MyFunctionArgument1
              Description.
            MYTYPE MyFunctionArgument1
              Description.

  Returns:  MyReturnType
              Description.
-----------------------------------------------------------------F-F*/
```

## <a name="exported-function-definition-header"></a><span data-ttu-id="01264-185">Заголовок определения экспортированной функции</span><span class="sxs-lookup"><span data-stu-id="01264-185">Exported Function Definition Header</span></span>

``` syntax
/*F+F+++F+++F+++F+++F+++F+++F+++F+++F+++F+++F+++F+++F+++F+++F+++F+++F
  Function: MyFunction

  Summary:  What MyFunction is for and what it does.

  Args:     MYTYPE MyFunctionArgument1
              Description.
            MYTYPE MyFunctionArgument1
              Description.

  Returns:  MyReturnType
              Description.
F---F---F---F---F---F---F---F---F---F---F---F---F---F---F---F---F-F*/
```

## <a name="com-interface-declaration-header"></a><span data-ttu-id="01264-186">Заголовок объявления COM-интерфейса</span><span class="sxs-lookup"><span data-stu-id="01264-186">COM Interface Declaration Header</span></span>

``` syntax
/*I+I+++I+++I+++I+++I+++I+++I+++I+++I+++I+++I+++I+++I+++I+++I+++I+++I
  Interface: IMyInterface

  Summary:   Short summary of what features the interface can bring to
             a COM Component.

  Methods:   MYTYPE MyMethodOne
               Description.
             MYTYPE MyMethodTwo
               Description.
I---I---I---I---I---I---I---I---I---I---I---I---I---I---I---I---I-I*/
```

## <a name="com-object-class-declaration-header"></a><span data-ttu-id="01264-187">Заголовок объявления класса COM-объекта</span><span class="sxs-lookup"><span data-stu-id="01264-187">COM Object Class Declaration Header</span></span>

``` syntax
/*O+O+++O+++O+++O+++O+++O+++O+++O+++O+++O+++O+++O+++O+++O+++O+++O+++O
  ObjectClass: COMyCOMObject

  Summary:     Short summary of purpose and content of this object.

  Interfaces:  IUnknown
                 Standard interface providing COM object features.
               IMyInterfaceOne
                 Description.
               IMyInterfaceTwo
                 Description.

  Aggregation: [whether this COM Object is aggregatable or not]
O---O---O---O---O---O---O---O---O---O---O---O---O---O---O---O---O-O*/
```

<span data-ttu-id="01264-188">Все эти соглашения блока комментариев имеют одинаковые начальные и конечные строки токена.</span><span class="sxs-lookup"><span data-stu-id="01264-188">All of these comment block conventions have consistent beginning and ending token strings.</span></span> <span data-ttu-id="01264-189">Такая согласованность поддерживает автоматическую обработку заголовков каким бы то ни было образом.</span><span class="sxs-lookup"><span data-stu-id="01264-189">This consistency supports automatic processing of the headers in some fashion.</span></span> <span data-ttu-id="01264-190">Например, скрипты AWK могут быть написаны для фильтрации заголовков функций в отдельный текстовый файл, который затем может служить основанием для документа спецификации.</span><span class="sxs-lookup"><span data-stu-id="01264-190">For example, AWK scripts can be written to filter the function headers into a separate text file that can then serve as the basis for a specification document.</span></span> <span data-ttu-id="01264-191">Аналогичным образом, такие средства, как неподдерживаемая служебная программа АУТОДУКК (в настоящее время доступная на компакт-диске библиотеки разработки Майкрософт для разработчиков сети), можно использовать для обработки блоков комментариев в этих заголовках.</span><span class="sxs-lookup"><span data-stu-id="01264-191">Similarly, tools like the unsupported AUTODUCK utility (currently available on the Microsoft Developer Network Development Library CD-ROM) can be used to process the comment blocks in these headers.</span></span>

<span data-ttu-id="01264-192">В следующей таблице перечислены начальные и конечные строки токенов, используемые в примерах учебников.</span><span class="sxs-lookup"><span data-stu-id="01264-192">The following table lists beginning and ending token strings used in sample tutorials.</span></span>



| <span data-ttu-id="01264-193">Токен</span><span class="sxs-lookup"><span data-stu-id="01264-193">Token</span></span> | <span data-ttu-id="01264-194">Описание</span><span class="sxs-lookup"><span data-stu-id="01264-194">Description</span></span>                      |
|-------|----------------------------------|
| /\*+  | <span data-ttu-id="01264-195">Начало заголовка файла</span><span class="sxs-lookup"><span data-stu-id="01264-195">File Header Begin</span></span>                |
| +\*/  | <span data-ttu-id="01264-196">Конец заголовка файла</span><span class="sxs-lookup"><span data-stu-id="01264-196">File Header End</span></span>                  |
| /\*-  | <span data-ttu-id="01264-197">Начало заголовка блока с обычными комментариями</span><span class="sxs-lookup"><span data-stu-id="01264-197">Plain comment block Header Begin</span></span> |
| -\*/  | <span data-ttu-id="01264-198">Конец заголовка блока обычного комментария</span><span class="sxs-lookup"><span data-stu-id="01264-198">Plain comment block Header End</span></span>   |
| <span data-ttu-id="01264-199">/\*Ц</span><span class="sxs-lookup"><span data-stu-id="01264-199">/\*C</span></span>  | <span data-ttu-id="01264-200">Начало заголовка класса</span><span class="sxs-lookup"><span data-stu-id="01264-200">Class Header Begin</span></span>               |
| <span data-ttu-id="01264-201">Ц\*/</span><span class="sxs-lookup"><span data-stu-id="01264-201">C\*/</span></span>  | <span data-ttu-id="01264-202">Конец заголовка класса</span><span class="sxs-lookup"><span data-stu-id="01264-202">Class Header End</span></span>                 |
| <span data-ttu-id="01264-203">/\*Пн</span><span class="sxs-lookup"><span data-stu-id="01264-203">/\*M</span></span>  | <span data-ttu-id="01264-204">Начало заголовка метода</span><span class="sxs-lookup"><span data-stu-id="01264-204">Method Header Begin</span></span>              |
| <span data-ttu-id="01264-205">Пн\*/</span><span class="sxs-lookup"><span data-stu-id="01264-205">M\*/</span></span>  | <span data-ttu-id="01264-206">Конец заголовка метода</span><span class="sxs-lookup"><span data-stu-id="01264-206">Method Header End</span></span>                |
| <span data-ttu-id="01264-207">/\*Ж</span><span class="sxs-lookup"><span data-stu-id="01264-207">/\*F</span></span>  | <span data-ttu-id="01264-208">Начало заголовка функции</span><span class="sxs-lookup"><span data-stu-id="01264-208">Function Header Begin</span></span>            |
| <span data-ttu-id="01264-209">Ж\*/</span><span class="sxs-lookup"><span data-stu-id="01264-209">F\*/</span></span>  | <span data-ttu-id="01264-210">Конец заголовка функции</span><span class="sxs-lookup"><span data-stu-id="01264-210">Function Header End</span></span>              |
| <span data-ttu-id="01264-211">/\*Сохранении</span><span class="sxs-lookup"><span data-stu-id="01264-211">/\*I</span></span>  | <span data-ttu-id="01264-212">Начало заголовка интерфейса</span><span class="sxs-lookup"><span data-stu-id="01264-212">Interface Header Begin</span></span>           |
| <span data-ttu-id="01264-213">Сохранении\*/</span><span class="sxs-lookup"><span data-stu-id="01264-213">I\*/</span></span>  | <span data-ttu-id="01264-214">Конец заголовка интерфейса</span><span class="sxs-lookup"><span data-stu-id="01264-214">Interface Header End</span></span>             |
| <span data-ttu-id="01264-215">/\*Вывода</span><span class="sxs-lookup"><span data-stu-id="01264-215">/\*O</span></span>  | <span data-ttu-id="01264-216">Начало заголовка класса COM-объекта</span><span class="sxs-lookup"><span data-stu-id="01264-216">COM Object Class Header Begin</span></span>    |
| <span data-ttu-id="01264-217">Вывода\*/</span><span class="sxs-lookup"><span data-stu-id="01264-217">O\*/</span></span>  | <span data-ttu-id="01264-218">Конец заголовка класса COM-объекта</span><span class="sxs-lookup"><span data-stu-id="01264-218">COM Object Class Header End</span></span>      |



 

<span data-ttu-id="01264-219">Эти заголовки также можно использовать в качестве визуальных подсказок для быстрого сканирования исходных файлов.</span><span class="sxs-lookup"><span data-stu-id="01264-219">These headers can also be used as visual cues for rapid scanning of source files.</span></span> <span data-ttu-id="01264-220">Они также позволяют быстро получить доступ к определенному исходному расположению, если вы настроили строки поиска в редакторе, а затем "Повторить последний Поиск", чтобы быстро найти эти заголовки.</span><span class="sxs-lookup"><span data-stu-id="01264-220">They also provide convenience for rapidly getting to some source location if you set up search strings in your editor and then 'repeat last search' to quickly locate these headers.</span></span>

<span data-ttu-id="01264-221">Например, строка поиска "M + M" найдет начало заголовков метода, а "M-M" найдет начало фактического определения метода или кода реализации.</span><span class="sxs-lookup"><span data-stu-id="01264-221">For example, the search string "M+M" will locate the start of method headers, and "M-M" will locate the beginning of the actual method definition/implementation code.</span></span>

 

 




