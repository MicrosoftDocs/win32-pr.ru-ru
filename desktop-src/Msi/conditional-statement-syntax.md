---
description: В этом разделе описывается синтаксис условных операторов, используемых функцией Мсиевалуатекондитион и таблицами последовательности действий. Дополнительные сведения см. в разделе Примеры синтаксиса условных инструкций.
ms.assetid: 6f1657f9-063b-4d57-ad76-95e3dbe25786
title: Синтаксис условных операторов
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f0548a71756faff654bfe2b49e14c0581a6248a5
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "103909027"
---
# <a name="conditional-statement-syntax"></a><span data-ttu-id="9b838-104">Синтаксис условных операторов</span><span class="sxs-lookup"><span data-stu-id="9b838-104">Conditional Statement Syntax</span></span>

<span data-ttu-id="9b838-105">В этом разделе описывается синтаксис условных операторов, используемых функцией [**мсиевалуатекондитион**](/windows/desktop/api/Msiquery/nf-msiquery-msievaluateconditiona) и [таблицами последовательности](using-a-sequence-table.md)действий.</span><span class="sxs-lookup"><span data-stu-id="9b838-105">This section describes the syntax of conditional statements used by the [**MsiEvaluateCondition**](/windows/desktop/api/Msiquery/nf-msiquery-msievaluateconditiona) function and the action [sequence tables](using-a-sequence-table.md).</span></span> <span data-ttu-id="9b838-106">Дополнительные сведения см. в разделе [Примеры синтаксиса условных инструкций](examples-of-conditional-statement-syntax.md).</span><span class="sxs-lookup"><span data-stu-id="9b838-106">For more information, see, [Examples of Conditional Statement Syntax](examples-of-conditional-statement-syntax.md).</span></span>

## <a name="summary-of-conditional-statement-syntax"></a><span data-ttu-id="9b838-107">Сводка синтаксиса условных инструкций</span><span class="sxs-lookup"><span data-stu-id="9b838-107">Summary of Conditional Statement Syntax</span></span>

<span data-ttu-id="9b838-108">В этой таблице и следующем списке приведено краткое описание синтаксиса, используемого в условных выражениях.</span><span class="sxs-lookup"><span data-stu-id="9b838-108">This table and the following list summarize the syntax to use in conditional expressions.</span></span>



| <span data-ttu-id="9b838-109">Элемент</span><span class="sxs-lookup"><span data-stu-id="9b838-109">Item</span></span>                | <span data-ttu-id="9b838-110">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="9b838-110">Syntax</span></span>                                                                                                          |
|---------------------|-----------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="9b838-111">значение</span><span class="sxs-lookup"><span data-stu-id="9b838-111">value</span></span>               | <span data-ttu-id="9b838-112">\|символьное \| целое число</span><span class="sxs-lookup"><span data-stu-id="9b838-112">symbol \| literal \| integer</span></span>                                                                                    |
| <span data-ttu-id="9b838-113">оператор сравнения</span><span class="sxs-lookup"><span data-stu-id="9b838-113">comparison-operator</span></span> | < \| > \| <= \| >= \| = \| <>                                                                 |
| <span data-ttu-id="9b838-114">Слово</span><span class="sxs-lookup"><span data-stu-id="9b838-114">term</span></span>                | <span data-ttu-id="9b838-115">\|Сравнение значений — значение оператора \| (выражение)\|</span><span class="sxs-lookup"><span data-stu-id="9b838-115">value \| value comparison-operator value \| ( expression )\|</span></span>                                                    |
| <span data-ttu-id="9b838-116">Логический фактор</span><span class="sxs-lookup"><span data-stu-id="9b838-116">Boolean-factor</span></span>      | <span data-ttu-id="9b838-117">термин \| **не** является термином</span><span class="sxs-lookup"><span data-stu-id="9b838-117">term \| **NOT** term</span></span>                                                                                            |
| <span data-ttu-id="9b838-118">Логическое выражение</span><span class="sxs-lookup"><span data-stu-id="9b838-118">Boolean-term</span></span>        | <span data-ttu-id="9b838-119">Логический фактор логического \| **и** термина</span><span class="sxs-lookup"><span data-stu-id="9b838-119">Boolean-factor \| Boolean-factor **AND** term</span></span>                                                                   |
| <span data-ttu-id="9b838-120">expression</span><span class="sxs-lookup"><span data-stu-id="9b838-120">expression</span></span>          | <span data-ttu-id="9b838-121">Логическое \| выражение Boolean-Term **или** Expression</span><span class="sxs-lookup"><span data-stu-id="9b838-121">Boolean-term \| Boolean-term **OR** expression</span></span>                                                                  |
| <span data-ttu-id="9b838-122">символ</span><span class="sxs-lookup"><span data-stu-id="9b838-122">symbol</span></span>              | <span data-ttu-id="9b838-123">Свойство \| % Environment: переменная \| $Component-Action \| ? компонент-State \| &компонент-действие \| ! состояние компонента</span><span class="sxs-lookup"><span data-stu-id="9b838-123">property \| %environment-variable \| $component-action \| ?component-state \| &feature-action \| !feature-state</span></span> |



 

-   <span data-ttu-id="9b838-124">В именах символов и значениях учитывается регистр.</span><span class="sxs-lookup"><span data-stu-id="9b838-124">Symbol names and values are case sensitive.</span></span>
-   <span data-ttu-id="9b838-125">В именах переменных среды регистр не учитывается.</span><span class="sxs-lookup"><span data-stu-id="9b838-125">Environment variable names are not case sensitive.</span></span>
-   <span data-ttu-id="9b838-126">Текст литерала должен быть заключен в кавычки ("Text").</span><span class="sxs-lookup"><span data-stu-id="9b838-126">Literal text must be enclosed between quotation marks ("text").</span></span>
    > [!Note]  
    > <span data-ttu-id="9b838-127">Литеральный текст, содержащий кавычки, нельзя использовать в условных инструкциях, так как в литеральном тексте нет escape-символа для кавычек.</span><span class="sxs-lookup"><span data-stu-id="9b838-127">Literal text containing quotation marks cannot be used in conditional statements because there is no escape character for quotation marks inside literal text.</span></span> <span data-ttu-id="9b838-128">Для сравнения с текстовым литералом, содержащим кавычки, текст литерала должен быть размещен в свойстве.</span><span class="sxs-lookup"><span data-stu-id="9b838-128">To do a comparison against literal text containing quotation marks, the literal text should be put in a property.</span></span> <span data-ttu-id="9b838-129">Например, чтобы убедиться, что свойство SERVERNAME не содержит кавычек, определите свойство с именем QUOTEs в [таблице свойств](property-table.md) со значением "и измените условие на" not ServerName><Quotes ".</span><span class="sxs-lookup"><span data-stu-id="9b838-129">For example, to verify that the SERVERNAME property does not contain any quotation marks, define a property called QUOTES in the [Property table](property-table.md) with a value of " and change the condition to NOT SERVERNAME><QUOTES.</span></span>

     

-   <span data-ttu-id="9b838-130">Несуществующие значения свойств рассматриваются как пустые строки.</span><span class="sxs-lookup"><span data-stu-id="9b838-130">Nonexistent property values are treated as empty strings.</span></span>
-   <span data-ttu-id="9b838-131">Числовые значения с плавающей запятой не поддерживаются.</span><span class="sxs-lookup"><span data-stu-id="9b838-131">Floating point numeric values are not supported.</span></span>
-   <span data-ttu-id="9b838-132">Операторы и приоритеты аналогичны тем, что основаны на языках BASIC и SQL.</span><span class="sxs-lookup"><span data-stu-id="9b838-132">Operators and precedence are the same as in the BASIC and SQL languages.</span></span>
-   <span data-ttu-id="9b838-133">Арифметические операторы не поддерживаются.</span><span class="sxs-lookup"><span data-stu-id="9b838-133">Arithmetic operators are not supported.</span></span>
-   <span data-ttu-id="9b838-134">Для переопределения приоритета операторов можно использовать круглые скобки.</span><span class="sxs-lookup"><span data-stu-id="9b838-134">Parentheses can be used to override operator precedence.</span></span>
-   <span data-ttu-id="9b838-135">В операторах регистр не учитывается.</span><span class="sxs-lookup"><span data-stu-id="9b838-135">Operators are not case sensitive.</span></span>
-   <span data-ttu-id="9b838-136">Для сравнения строк символ тильды "~", предваряющий оператор, выполняет сравнение без учета регистра.</span><span class="sxs-lookup"><span data-stu-id="9b838-136">For string comparisons, a tilde "~" prefixed to the operator performs a comparison that is not case sensitive.</span></span>
-   <span data-ttu-id="9b838-137">Сравнение целого числа со значением строки или свойства, которое не может быть преобразовано в целое число, всегда равно **мсиевалуатекондитионфалсе**, за исключением оператора сравнения "<>", который возвращает **мсиевалуатекондитионтруе**.</span><span class="sxs-lookup"><span data-stu-id="9b838-137">Comparison of an integer with a string or property value that cannot be converted to an integer is always **msiEvaluateConditionFalse**, except for the comparison operator "<>", which returns **msiEvaluateConditionTrue**.</span></span>

## <a name="access-prefixes"></a><span data-ttu-id="9b838-138">Префиксы доступа</span><span class="sxs-lookup"><span data-stu-id="9b838-138">Access Prefixes</span></span>

<span data-ttu-id="9b838-139">В следующей таблице приведены префиксы, используемые для доступа к различным сведениям об установщике системы и установщика для использования в условных выражениях.</span><span class="sxs-lookup"><span data-stu-id="9b838-139">The following table shows the prefixes to use to access various system and installer information for use in conditional expressions.</span></span>



| <span data-ttu-id="9b838-140">Тип символа</span><span class="sxs-lookup"><span data-stu-id="9b838-140">Symbol type</span></span>          | <span data-ttu-id="9b838-141">Prefix</span><span class="sxs-lookup"><span data-stu-id="9b838-141">Prefix</span></span> | <span data-ttu-id="9b838-142">Значение</span><span class="sxs-lookup"><span data-stu-id="9b838-142">Value</span></span>                                                     |
|----------------------|--------|-----------------------------------------------------------|
| <span data-ttu-id="9b838-143">Свойство установщика</span><span class="sxs-lookup"><span data-stu-id="9b838-143">Installer property</span></span>   | <span data-ttu-id="9b838-144">(нет)</span><span class="sxs-lookup"><span data-stu-id="9b838-144">(none)</span></span> | <span data-ttu-id="9b838-145">Значение таблицы свойств ([Property](property-table.md)).</span><span class="sxs-lookup"><span data-stu-id="9b838-145">Value of property ([Property](property-table.md)) table.</span></span> |
| <span data-ttu-id="9b838-146">Переменная среды</span><span class="sxs-lookup"><span data-stu-id="9b838-146">Environment variable</span></span> | %      | <span data-ttu-id="9b838-147">Значение переменной среды.</span><span class="sxs-lookup"><span data-stu-id="9b838-147">Value of environment variable.</span></span>                            |
| <span data-ttu-id="9b838-148">Ключ таблицы компонента</span><span class="sxs-lookup"><span data-stu-id="9b838-148">Component table key</span></span>  | $      | <span data-ttu-id="9b838-149">Состояние действия компонента.</span><span class="sxs-lookup"><span data-stu-id="9b838-149">Action state of the component.</span></span>                            |
| <span data-ttu-id="9b838-150">Ключ таблицы компонента</span><span class="sxs-lookup"><span data-stu-id="9b838-150">Component table key</span></span>  | <span data-ttu-id="9b838-151">?</span><span class="sxs-lookup"><span data-stu-id="9b838-151">?</span></span>      | <span data-ttu-id="9b838-152">Установленное состояние компонента.</span><span class="sxs-lookup"><span data-stu-id="9b838-152">Installed state of the component.</span></span>                         |
| <span data-ttu-id="9b838-153">Ключ таблицы функций</span><span class="sxs-lookup"><span data-stu-id="9b838-153">Feature table key</span></span>    | &      | <span data-ttu-id="9b838-154">Состояние действия компонента.</span><span class="sxs-lookup"><span data-stu-id="9b838-154">Action state of the feature.</span></span>                              |
| <span data-ttu-id="9b838-155">Ключ таблицы функций</span><span class="sxs-lookup"><span data-stu-id="9b838-155">Feature table key</span></span>    | <span data-ttu-id="9b838-156">!</span><span class="sxs-lookup"><span data-stu-id="9b838-156">!</span></span>      | <span data-ttu-id="9b838-157">Состояние установки компонента.</span><span class="sxs-lookup"><span data-stu-id="9b838-157">Installed state of the feature.</span></span>                           |



 

## <a name="logical-operators"></a><span data-ttu-id="9b838-158">Логические операторы</span><span class="sxs-lookup"><span data-stu-id="9b838-158">Logical Operators</span></span>

<span data-ttu-id="9b838-159">В следующей таблице показаны логические операторы в условных выражениях в порядке убывания приоритета.</span><span class="sxs-lookup"><span data-stu-id="9b838-159">The following table shows the logical operators in conditional expressions, in order of high-to-low precedence.</span></span>



| <span data-ttu-id="9b838-160">Оператор</span><span class="sxs-lookup"><span data-stu-id="9b838-160">Operator</span></span> | <span data-ttu-id="9b838-161">Значение</span><span class="sxs-lookup"><span data-stu-id="9b838-161">Meaning</span></span>                                                 |
|----------|---------------------------------------------------------|
| <span data-ttu-id="9b838-162">Not</span><span class="sxs-lookup"><span data-stu-id="9b838-162">Not</span></span>      | <span data-ttu-id="9b838-163">Префикс унарного оператора; Инвертирует состояние следующего термина.</span><span class="sxs-lookup"><span data-stu-id="9b838-163">Prefix unary operator; inverts state of following term.</span></span> |
| <span data-ttu-id="9b838-164">И</span><span class="sxs-lookup"><span data-stu-id="9b838-164">And</span></span>      | <span data-ttu-id="9b838-165">Значение TRUE, если оба условия имеют значение TRUE.</span><span class="sxs-lookup"><span data-stu-id="9b838-165">TRUE if both terms are TRUE.</span></span>                            |
| <span data-ttu-id="9b838-166">либо</span><span class="sxs-lookup"><span data-stu-id="9b838-166">Or</span></span>       | <span data-ttu-id="9b838-167">Значение TRUE, если одно или оба условия имеют значение TRUE.</span><span class="sxs-lookup"><span data-stu-id="9b838-167">TRUE if either or both terms are TRUE.</span></span>                  |
| <span data-ttu-id="9b838-168">Xor</span><span class="sxs-lookup"><span data-stu-id="9b838-168">Xor</span></span>      | <span data-ttu-id="9b838-169">Значение TRUE, если оба условия имеют значение TRUE.</span><span class="sxs-lookup"><span data-stu-id="9b838-169">TRUE if either but not both terms are TRUE.</span></span>             |
| <span data-ttu-id="9b838-170">Eqv</span><span class="sxs-lookup"><span data-stu-id="9b838-170">Eqv</span></span>      | <span data-ttu-id="9b838-171">TRUE, если оба условия имеют значение TRUE или оба условия имеют значение FALSE.</span><span class="sxs-lookup"><span data-stu-id="9b838-171">TRUE if both terms are TRUE or both terms are FALSE.</span></span>    |
| <span data-ttu-id="9b838-172">Imp</span><span class="sxs-lookup"><span data-stu-id="9b838-172">Imp</span></span>      | <span data-ttu-id="9b838-173">Значение TRUE, если левый термин имеет значение FALSE или правое выражение имеет значение TRUE.</span><span class="sxs-lookup"><span data-stu-id="9b838-173">TRUE if left term is FALSE or right term is TRUE.</span></span>       |



 

## <a name="comparative-operators"></a><span data-ttu-id="9b838-174">Сравнительные операторы</span><span class="sxs-lookup"><span data-stu-id="9b838-174">Comparative Operators</span></span>

<span data-ttu-id="9b838-175">В следующей таблице показаны операторы сравнения, используемые в условных выражениях.</span><span class="sxs-lookup"><span data-stu-id="9b838-175">The following table shows the comparison operators used in conditional expressions.</span></span> <span data-ttu-id="9b838-176">Эти операторы сравнения могут находиться только между двумя значениями.</span><span class="sxs-lookup"><span data-stu-id="9b838-176">These comparison operators can only occur between two values.</span></span>



| <span data-ttu-id="9b838-177">Оператор</span><span class="sxs-lookup"><span data-stu-id="9b838-177">Operator</span></span> | <span data-ttu-id="9b838-178">Значение</span><span class="sxs-lookup"><span data-stu-id="9b838-178">Meaning</span></span>                                                     |
|----------|-------------------------------------------------------------|
| =        | <span data-ttu-id="9b838-179">Значение TRUE, если значение left равно значению right.</span><span class="sxs-lookup"><span data-stu-id="9b838-179">TRUE if left value is equal to right value.</span></span>                 |
| <> | <span data-ttu-id="9b838-180">TRUE, если левое значение не равно значению right.</span><span class="sxs-lookup"><span data-stu-id="9b838-180">TRUE if left value is not equal to right value.</span></span>             |
| >     | <span data-ttu-id="9b838-181">Значение TRUE, если значение left больше значения right.</span><span class="sxs-lookup"><span data-stu-id="9b838-181">TRUE if left value is greater than right value.</span></span>             |
| >=    | <span data-ttu-id="9b838-182">Значение TRUE, если значение left больше или равно значению right.</span><span class="sxs-lookup"><span data-stu-id="9b838-182">TRUE if left value is greater than or equal to right value.</span></span> |
| <     | <span data-ttu-id="9b838-183">Значение TRUE, если значение Left меньше значения right.</span><span class="sxs-lookup"><span data-stu-id="9b838-183">TRUE if left value is less than right value.</span></span>                |
| <=    | <span data-ttu-id="9b838-184">Значение TRUE, если значение Left меньше или равно значению right.</span><span class="sxs-lookup"><span data-stu-id="9b838-184">TRUE if left value is less than or equal to right value.</span></span>    |



 

## <a name="substring-operators"></a><span data-ttu-id="9b838-185">Операторы substring</span><span class="sxs-lookup"><span data-stu-id="9b838-185">Substring Operators</span></span>

<span data-ttu-id="9b838-186">В следующей таблице показаны операторы подстроки, используемые в условных выражениях.</span><span class="sxs-lookup"><span data-stu-id="9b838-186">The following table shows the substring operators used in conditional expressions.</span></span> <span data-ttu-id="9b838-187">Операторы подстроки могут находиться между двумя строковыми значениями.</span><span class="sxs-lookup"><span data-stu-id="9b838-187">Substring operators can occur between two string values.</span></span>



| <span data-ttu-id="9b838-188">Оператор</span><span class="sxs-lookup"><span data-stu-id="9b838-188">Operator</span></span> | <span data-ttu-id="9b838-189">Значение</span><span class="sxs-lookup"><span data-stu-id="9b838-189">Meaning</span></span>                                           |
|----------|---------------------------------------------------|
| >< | <span data-ttu-id="9b838-190">Значение TRUE, если левая строка содержит правую строку.</span><span class="sxs-lookup"><span data-stu-id="9b838-190">TRUE if left string contains the right string.</span></span>    |
| << | <span data-ttu-id="9b838-191">Значение TRUE, если левая строка начинается с правой строки.</span><span class="sxs-lookup"><span data-stu-id="9b838-191">TRUE if left string starts with the right string.</span></span> |
| >> | <span data-ttu-id="9b838-192">Значение TRUE, если левая строка заканчивается на правую строку.</span><span class="sxs-lookup"><span data-stu-id="9b838-192">TRUE if left string ends with the right string.</span></span>   |



 

## <a name="bitwise-numeric-operators"></a><span data-ttu-id="9b838-193">Битовые числовые операторы</span><span class="sxs-lookup"><span data-stu-id="9b838-193">Bitwise Numeric Operators</span></span>

<span data-ttu-id="9b838-194">В следующей таблице показаны побитовые операторы сравнения в условных выражениях.</span><span class="sxs-lookup"><span data-stu-id="9b838-194">The following table shows the bitwise numeric operators in conditional expressions.</span></span> <span data-ttu-id="9b838-195">Эти операторы могут находиться между двумя целочисленными значениями.</span><span class="sxs-lookup"><span data-stu-id="9b838-195">These operators can occur between two integer values.</span></span>



| <span data-ttu-id="9b838-196">Оператор</span><span class="sxs-lookup"><span data-stu-id="9b838-196">Operator</span></span> | <span data-ttu-id="9b838-197">Значение</span><span class="sxs-lookup"><span data-stu-id="9b838-197">Meaning</span></span>                                                                      |
|----------|------------------------------------------------------------------------------|
| >< | <span data-ttu-id="9b838-198">Побитовое и, TRUE, если левое и правое целые числа имеют общие биты.</span><span class="sxs-lookup"><span data-stu-id="9b838-198">Bitwise AND, TRUE if the left and right integers have any bits in common.</span></span>    |
| << | <span data-ttu-id="9b838-199">Значение true, если старшие 16-разряды левого целого числа равны значению правого целого числа.</span><span class="sxs-lookup"><span data-stu-id="9b838-199">True if the high 16-bits of the left integer are equal to the right integer.</span></span> |
| >> | <span data-ttu-id="9b838-200">Значение true, если младшие 16 разрядов левого целого числа равны значению правого целого числа.</span><span class="sxs-lookup"><span data-stu-id="9b838-200">True if the low 16-bits of the left integer are equal to the right integer.</span></span>  |



 

## <a name="feature-and-component-state-values"></a><span data-ttu-id="9b838-201">Значения состояния компонентов и компонентов</span><span class="sxs-lookup"><span data-stu-id="9b838-201">Feature and Component State Values</span></span>

<span data-ttu-id="9b838-202">В следующей таблице показано, где можно использовать символы операторов и компонентов.</span><span class="sxs-lookup"><span data-stu-id="9b838-202">The following table shows where it is valid to use the feature and component operator symbols.</span></span>



| <span data-ttu-id="9b838-203">Станции <state></span><span class="sxs-lookup"><span data-stu-id="9b838-203">Operator <state></span></span> | <span data-ttu-id="9b838-204">Допустимый синтаксис</span><span class="sxs-lookup"><span data-stu-id="9b838-204">Where this syntax is valid</span></span>                                                                                                                                         |
|------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="9b838-205">$component действие</span><span class="sxs-lookup"><span data-stu-id="9b838-205">$component-action</span></span>      | <span data-ttu-id="9b838-206">В таблице [условие](condition-table.md) и в таблицах [последовательности](using-a-sequence-table.md) после действия [костфинализе](costfinalize-action.md) .</span><span class="sxs-lookup"><span data-stu-id="9b838-206">In the [Condition](condition-table.md) table, and in the [sequence](using-a-sequence-table.md) tables, after the [CostFinalize](costfinalize-action.md) action.</span></span> |
| <span data-ttu-id="9b838-207">Действие &компонента</span><span class="sxs-lookup"><span data-stu-id="9b838-207">&feature-action</span></span>        | <span data-ttu-id="9b838-208">В таблице [условие](condition-table.md) и в таблицах [последовательности](using-a-sequence-table.md) после действия [костфинализе](costfinalize-action.md) .</span><span class="sxs-lookup"><span data-stu-id="9b838-208">In the [Condition](condition-table.md) table, and in the [sequence](using-a-sequence-table.md) tables, after the [CostFinalize](costfinalize-action.md) action.</span></span> |
| <span data-ttu-id="9b838-209">! состояние компонента</span><span class="sxs-lookup"><span data-stu-id="9b838-209">!feature-state</span></span>         | <span data-ttu-id="9b838-210">В таблице [условие](condition-table.md) и в таблицах [последовательности](using-a-sequence-table.md) после действия [костфинализе](costfinalize-action.md) .</span><span class="sxs-lookup"><span data-stu-id="9b838-210">In the [Condition](condition-table.md) table, and in the [sequence](using-a-sequence-table.md) tables, after the [CostFinalize](costfinalize-action.md) action.</span></span> |
| <span data-ttu-id="9b838-211">? состояние компонента</span><span class="sxs-lookup"><span data-stu-id="9b838-211">?component-state</span></span>       | <span data-ttu-id="9b838-212">В таблице [условие](condition-table.md) и в таблицах [последовательности](using-a-sequence-table.md) после действия [костфинализе](costfinalize-action.md) .</span><span class="sxs-lookup"><span data-stu-id="9b838-212">In the [Condition](condition-table.md) table, and in the [sequence](using-a-sequence-table.md) tables, after the [CostFinalize](costfinalize-action.md) action.</span></span> |



 

<span data-ttu-id="9b838-213">В следующей таблице показаны значения компонентов и состояния компонентов, используемые в условных выражениях.</span><span class="sxs-lookup"><span data-stu-id="9b838-213">The following table shows the feature and component state values used in conditional expressions.</span></span> <span data-ttu-id="9b838-214">Эти состояния не задаются, пока не будет вызван [**мсисетинсталллевел**](/windows/desktop/api/Msiquery/nf-msiquery-msisetinstalllevel) , напрямую или с помощью действия [костфинализе](costfinalize-action.md) .</span><span class="sxs-lookup"><span data-stu-id="9b838-214">These states are not set until [**MsiSetInstallLevel**](/windows/desktop/api/Msiquery/nf-msiquery-msisetinstalllevel) is called, either directly or by the [CostFinalize](costfinalize-action.md) action.</span></span>



| <span data-ttu-id="9b838-215">Состояние</span><span class="sxs-lookup"><span data-stu-id="9b838-215">State</span></span>                    | <span data-ttu-id="9b838-216">Значение</span><span class="sxs-lookup"><span data-stu-id="9b838-216">Value</span></span> | <span data-ttu-id="9b838-217">Значение</span><span class="sxs-lookup"><span data-stu-id="9b838-217">Meaning</span></span>                                                         |
|--------------------------|-------|-----------------------------------------------------------------|
| <span data-ttu-id="9b838-218">INSTALLSTATE \_ неизвестный</span><span class="sxs-lookup"><span data-stu-id="9b838-218">INSTALLSTATE\_UNKNOWN</span></span>    | <span data-ttu-id="9b838-219">-1</span><span class="sxs-lookup"><span data-stu-id="9b838-219">-1</span></span>    | <span data-ttu-id="9b838-220">Не предпринимать никаких действий с функцией или компонентом.</span><span class="sxs-lookup"><span data-stu-id="9b838-220">No action to be taken on the feature or component.</span></span>              |
| <span data-ttu-id="9b838-221">INSTALLSTATE \_ объявлено</span><span class="sxs-lookup"><span data-stu-id="9b838-221">INSTALLSTATE\_ADVERTISED</span></span> | <span data-ttu-id="9b838-222">1</span><span class="sxs-lookup"><span data-stu-id="9b838-222">1</span></span>     | <span data-ttu-id="9b838-223">Объявленный компонент.</span><span class="sxs-lookup"><span data-stu-id="9b838-223">Advertised feature.</span></span> <span data-ttu-id="9b838-224">Это состояние недоступно для компонентов.</span><span class="sxs-lookup"><span data-stu-id="9b838-224">This state is not available for components.</span></span> |
| <span data-ttu-id="9b838-225">\_отсутствует InstallState</span><span class="sxs-lookup"><span data-stu-id="9b838-225">INSTALLSTATE\_ABSENT</span></span>     | <span data-ttu-id="9b838-226">2</span><span class="sxs-lookup"><span data-stu-id="9b838-226">2</span></span>     | <span data-ttu-id="9b838-227">Отсутствует компонент или компонент.</span><span class="sxs-lookup"><span data-stu-id="9b838-227">Feature or component is not present.</span></span>                            |
| <span data-ttu-id="9b838-228">INSTALLSTATE \_ локальный</span><span class="sxs-lookup"><span data-stu-id="9b838-228">INSTALLSTATE\_LOCAL</span></span>      | <span data-ttu-id="9b838-229">3</span><span class="sxs-lookup"><span data-stu-id="9b838-229">3</span></span>     | <span data-ttu-id="9b838-230">Компонент или компонент на локальном компьютере.</span><span class="sxs-lookup"><span data-stu-id="9b838-230">Feature or component on the local computer.</span></span>                     |
| <span data-ttu-id="9b838-231">\_источник InstallState</span><span class="sxs-lookup"><span data-stu-id="9b838-231">INSTALLSTATE\_SOURCE</span></span>     | <span data-ttu-id="9b838-232">4</span><span class="sxs-lookup"><span data-stu-id="9b838-232">4</span></span>     | <span data-ttu-id="9b838-233">Компонент или компонент запускается из источника.</span><span class="sxs-lookup"><span data-stu-id="9b838-233">Feature or component run from the source.</span></span>                       |



 

<span data-ttu-id="9b838-234">Например, условное выражение "&Мифеатуре = 3" принимает значение true, только если Мифеатуре меняется от текущего состояния к состоянию, установленному на локальном компьютере, INSTALLSTATE \_ Local.</span><span class="sxs-lookup"><span data-stu-id="9b838-234">For example, the conditional expression "&MyFeature=3" evaluates to True only if MyFeature is changing from its current state to the state of being installed on the local computer, INSTALLSTATE\_LOCAL.</span></span>

<span data-ttu-id="9b838-235">Обратите внимание, что не следует зависеть от условия $Component 1 = 3, чтобы проверить, установлена ли на компьютере Component1 локально.</span><span class="sxs-lookup"><span data-stu-id="9b838-235">Note that you should not depend upon the condition $Component1=3 to check whether Component1 is locally installed on the computer.</span></span> <span data-ttu-id="9b838-236">Это может привести к сбою, если Component1 установлен более чем одним продуктом.</span><span class="sxs-lookup"><span data-stu-id="9b838-236">This can fail if Component1 is installed by more than one product.</span></span> <span data-ttu-id="9b838-237">После того как Component1 установлен локально с помощью product1, установщик оценивает условие $Component 1 = 3 как false во время установки Product2.</span><span class="sxs-lookup"><span data-stu-id="9b838-237">After Component1 has been installed locally by Product1, the installer evaluates the condition $Component1=3 as False during the installation of Product2.</span></span> <span data-ttu-id="9b838-238">Это обусловлено тем, что установщик определяет версию компонента, используя путь к ключу компонента, и помечает компонент для установки, если его версия больше или равна установленному компоненту.</span><span class="sxs-lookup"><span data-stu-id="9b838-238">This is because the installer determines the version of the component using the component's key path and marks the component for installation if its version is greater than or equal to the installed component.</span></span>

<span data-ttu-id="9b838-239">Обратите внимание, что установщик не выполняет прямое сравнение типа данных [версии](version.md) в условных инструкциях.</span><span class="sxs-lookup"><span data-stu-id="9b838-239">Note that the installer will not do direct comparisons of the [Version](version.md) data type in conditional statements.</span></span> <span data-ttu-id="9b838-240">Например, нельзя использовать сравнительные операторы для сравнения версий, таких как "01,10" и "1,010", в условном операторе.</span><span class="sxs-lookup"><span data-stu-id="9b838-240">For example, you cannot use comparative operators to compare versions such as "01.10" and "1.010" in a conditional statement.</span></span> <span data-ttu-id="9b838-241">Вместо этого используйте допустимый метод для поиска версии, как описано в разделе [Поиск существующих приложений, файлов, записей реестра или INI-файлов](searching-for-existing-applications-files-registry-entries-or--ini-file-entries.md), а затем задайте свойство.</span><span class="sxs-lookup"><span data-stu-id="9b838-241">Instead use a valid method to search for a version, such as described in [Searching for Existing Applications, Files, Registry Entries or .ini File Entries](searching-for-existing-applications-files-registry-entries-or--ini-file-entries.md), and then set a property.</span></span>

## <a name="related-topics"></a><span data-ttu-id="9b838-242">См. также</span><span class="sxs-lookup"><span data-stu-id="9b838-242">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="9b838-243">Использование свойств в условных инструкциях</span><span class="sxs-lookup"><span data-stu-id="9b838-243">Using Properties in Conditional Statements</span></span>](using-properties-in-conditional-statements.md)
</dt> </dl>

 

 



