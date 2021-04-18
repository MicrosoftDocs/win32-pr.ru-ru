---
description: Запись управления условным доступом (ACE) позволяет оценивать условие доступа при выполнении проверки доступа. Язык определения дескрипторов безопасности (SDDL) предоставляет синтаксис для определения условных элементов ACE в строковом формате.
ms.assetid: cdc3629d-c4d8-4910-8838-3bdb601f7064
title: Язык определения дескрипторов безопасности для условных элементов ACE
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f65cb6ae0588ae197c84d3b13362721cc3e98b43
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104542711"
---
# <a name="security-descriptor-definition-language-for-conditional-aces"></a><span data-ttu-id="ab0ef-104">Язык определения дескрипторов безопасности для условных элементов ACE</span><span class="sxs-lookup"><span data-stu-id="ab0ef-104">Security Descriptor Definition Language for Conditional ACEs</span></span>

<span data-ttu-id="ab0ef-105">[*Запись управления*](/windows/desktop/SecGloss/a-gly) условным доступом (ACE) позволяет оценивать условие доступа при выполнении проверки доступа.</span><span class="sxs-lookup"><span data-stu-id="ab0ef-105">A conditional [*access control entry*](/windows/desktop/SecGloss/a-gly) (ACE) allows an access condition to be evaluated when an access check is performed.</span></span> <span data-ttu-id="ab0ef-106">Язык определения дескрипторов безопасности (SDDL) предоставляет синтаксис для определения условных элементов ACE в строковом формате.</span><span class="sxs-lookup"><span data-stu-id="ab0ef-106">The security descriptor definition language (SDDL) provides syntax for defining conditional ACEs in a string format.</span></span>

<span data-ttu-id="ab0ef-107">SDDL для условной записи ACE такой же, как и для любого элемента ACE, с синтаксисом для условной инструкции, добавленной в конец строки ACE.</span><span class="sxs-lookup"><span data-stu-id="ab0ef-107">The SDDL for a conditional ACE is the same as for any ACE, with the syntax for the conditional statement appended to the end of the ACE string.</span></span> <span data-ttu-id="ab0ef-108">Дополнительные сведения о SDDL см. в разделе [язык определения дескрипторов безопасности](security-descriptor-definition-language.md).</span><span class="sxs-lookup"><span data-stu-id="ab0ef-108">For information about SDDL, see [Security Descriptor Definition Language](security-descriptor-definition-language.md).</span></span>

<span data-ttu-id="ab0ef-109">Знак " \# " является синонимом "0" в атрибутах ресурса.</span><span class="sxs-lookup"><span data-stu-id="ab0ef-109">The "\#" sign is synonymous with "0" in resource attributes.</span></span> <span data-ttu-id="ab0ef-110">Например, Д:АИ (XA; ОИЦИ; FA;;; WD; (Октетстрингтипе = = \# 1 \# 2 \# 3 \# \# )) эквивалентен и интерпретируется как д:АИ (XA; оиЦи; FA;;; WD; (Октетстрингтипе = = \# 01020300)).</span><span class="sxs-lookup"><span data-stu-id="ab0ef-110">For example, D:AI(XA;OICI;FA;;;WD;(OctetStringType==\#1\#2\#3\#\#)) is equivalent to and interpreted as D:AI(XA;OICI;FA;;;WD;(OctetStringType==\#01020300)).</span></span>

-   [<span data-ttu-id="ab0ef-111">Формат строки условной записи ACE</span><span class="sxs-lookup"><span data-stu-id="ab0ef-111">Conditional ACE String Format</span></span>](#conditional-ace-string-format)
-   [<span data-ttu-id="ab0ef-112">Условные выражения</span><span class="sxs-lookup"><span data-stu-id="ab0ef-112">Conditional Expressions</span></span>](#conditional-expressions)
-   [<span data-ttu-id="ab0ef-113">Атрибуты</span><span class="sxs-lookup"><span data-stu-id="ab0ef-113">Attributes</span></span>](#attributes)
-   [<span data-ttu-id="ab0ef-114">Операторы</span><span class="sxs-lookup"><span data-stu-id="ab0ef-114">Operators</span></span>](#operators)
-   [<span data-ttu-id="ab0ef-115">Приоритет операторов</span><span class="sxs-lookup"><span data-stu-id="ab0ef-115">Operator Precedence</span></span>](#operator-precedence)
-   [<span data-ttu-id="ab0ef-116">Неизвестные значения</span><span class="sxs-lookup"><span data-stu-id="ab0ef-116">Unknown Values</span></span>](#unknown-values)
-   [<span data-ttu-id="ab0ef-117">Условная оценка ACE</span><span class="sxs-lookup"><span data-stu-id="ab0ef-117">Conditional ACE Evaluation</span></span>](#conditional-ace-evaluation)
-   [<span data-ttu-id="ab0ef-118">Примеры</span><span class="sxs-lookup"><span data-stu-id="ab0ef-118">Examples</span></span>](#examples)
-   [<span data-ttu-id="ab0ef-119">См. также</span><span class="sxs-lookup"><span data-stu-id="ab0ef-119">Related topics</span></span>](#related-topics)

## <a name="conditional-ace-string-format"></a><span data-ttu-id="ab0ef-120">Формат строки условной записи ACE</span><span class="sxs-lookup"><span data-stu-id="ab0ef-120">Conditional ACE String Format</span></span>

<span data-ttu-id="ab0ef-121">Каждый элемент ACE в строке [*дескриптора безопасности*](/windows/desktop/SecGloss/s-gly) заключен в круглые скобки.</span><span class="sxs-lookup"><span data-stu-id="ab0ef-121">Each ACE in a [*security descriptor*](/windows/desktop/SecGloss/s-gly) string is enclosed in parentheses.</span></span> <span data-ttu-id="ab0ef-122">Поля ACE находятся в следующем порядке и разделены точкой с запятой (;).</span><span class="sxs-lookup"><span data-stu-id="ab0ef-122">The fields of the ACE are in the following order and are separated by semicolons (;).</span></span>

<span data-ttu-id="ab0ef-123">*AceType ***;** _AceFlags_* _;_ *_Права_*_;_ *_ObjectGUID_*_;_ *_Инхеритобжектгуид_*_;_ *_AccountSid_*_;(_*_кондитионалекспрессион_*_)_*</span><span class="sxs-lookup"><span data-stu-id="ab0ef-123">*AceType\***;**_AceFlags_*_;_*_Rights_*_;_*_ObjectGuid_*_;_*_InheritObjectGuid_*_;_*_AccountSid_*_;(_*_ConditionalExpression_*_)_\*</span></span>

<span data-ttu-id="ab0ef-124">Эти поля описаны в [строках ACE](ace-strings.md), за исключением следующих.</span><span class="sxs-lookup"><span data-stu-id="ab0ef-124">The fields are as described in [ACE Strings](ace-strings.md), with the following exceptions.</span></span>

-   <span data-ttu-id="ab0ef-125">Поле *AceType* может быть одной из следующих строк.</span><span class="sxs-lookup"><span data-stu-id="ab0ef-125">The *AceType* field can be one of the following strings.</span></span>

    | <span data-ttu-id="ab0ef-126">Строка типа ACE</span><span class="sxs-lookup"><span data-stu-id="ab0ef-126">ACE type string</span></span> | <span data-ttu-id="ab0ef-127">Константа в SDDL. h</span><span class="sxs-lookup"><span data-stu-id="ab0ef-127">Constant in Sddl.h</span></span>                         | <span data-ttu-id="ab0ef-128">Значение AceType</span><span class="sxs-lookup"><span data-stu-id="ab0ef-128">AceType value</span></span>                                   |
    |-----------------|--------------------------------------------|-------------------------------------------------|
    | <span data-ttu-id="ab0ef-129">СООБЩЕН</span><span class="sxs-lookup"><span data-stu-id="ab0ef-129">"XA"</span></span><br/> | <span data-ttu-id="ab0ef-130">\_ \_ разрешен доступ к обратному ВЫЗОВу SDDL \_</span><span class="sxs-lookup"><span data-stu-id="ab0ef-130">SDDL\_CALLBACK\_ACCESS\_ALLOWED</span></span><br/> | <span data-ttu-id="ab0ef-131">ДОСТУП \_ к \_ \_ типу ACE разрешенного обратного вызова \_</span><span class="sxs-lookup"><span data-stu-id="ab0ef-131">ACCESS\_ALLOWED\_CALLBACK\_ACE\_TYPE</span></span><br/> |
    | <span data-ttu-id="ab0ef-132">XD</span><span class="sxs-lookup"><span data-stu-id="ab0ef-132">"XD"</span></span><br/> | <span data-ttu-id="ab0ef-133">\_доступ к обратному вызову SDDL \_ \_ запрещен</span><span class="sxs-lookup"><span data-stu-id="ab0ef-133">SDDL\_CALLBACK\_ACCESS\_DENIED</span></span><br/>  | <span data-ttu-id="ab0ef-134">\_ \_ Тип ACE обратного вызова с ЗАПРЕТом доступа \_ \_</span><span class="sxs-lookup"><span data-stu-id="ab0ef-134">ACCESS\_DENIED\_CALLBACK\_ACE\_TYPE</span></span><br/>  |

    

     

-   <span data-ttu-id="ab0ef-135">Строка ACE содержит одно или несколько условных выражений, заключенных в круглые скобки в конце строки.</span><span class="sxs-lookup"><span data-stu-id="ab0ef-135">The ACE string includes one or more conditional expressions, enclosed in parentheses at the end of the string.</span></span>

## <a name="conditional-expressions"></a><span data-ttu-id="ab0ef-136">Условные выражения</span><span class="sxs-lookup"><span data-stu-id="ab0ef-136">Conditional Expressions</span></span>

<span data-ttu-id="ab0ef-137">Условное выражение может включать любой из следующих элементов.</span><span class="sxs-lookup"><span data-stu-id="ab0ef-137">A conditional expression can include any of the following elements.</span></span>



| <span data-ttu-id="ab0ef-138">Элемент выражения</span><span class="sxs-lookup"><span data-stu-id="ab0ef-138">Expression element</span></span>                                                | <span data-ttu-id="ab0ef-139">Описание</span><span class="sxs-lookup"><span data-stu-id="ab0ef-139">Description</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                       |
|-------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="ab0ef-140">*AttributeName*</span><span class="sxs-lookup"><span data-stu-id="ab0ef-140">*AttributeName*</span></span><br/>                                        | <span data-ttu-id="ab0ef-141">Проверяет, имеет ли указанный атрибут ненулевое значение.</span><span class="sxs-lookup"><span data-stu-id="ab0ef-141">Tests whether the specified attribute has a nonzero value.</span></span><br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                             |
| <span data-ttu-id="ab0ef-142">**существует** *attributeName*</span><span class="sxs-lookup"><span data-stu-id="ab0ef-142">**exists** *AttributeName*</span></span><br/>                             | <span data-ttu-id="ab0ef-143">Проверяет, существует ли указанный атрибут в контексте клиента.</span><span class="sxs-lookup"><span data-stu-id="ab0ef-143">Tests whether the specified attribute exists in the client context.</span></span><br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                    |
| <span data-ttu-id="ab0ef-144">*AttributeName* , *значение* *оператора*</span><span class="sxs-lookup"><span data-stu-id="ab0ef-144">*AttributeName* *Operator* *Value*</span></span><br/>                     | <span data-ttu-id="ab0ef-145">Возвращает результат указанной операции.</span><span class="sxs-lookup"><span data-stu-id="ab0ef-145">Returns the result of the specified operation.</span></span><br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                         |
| <span data-ttu-id="ab0ef-146">\* Кондитионалекспрессион \* **\|\|** _кондитионалекспрессион_</span><span class="sxs-lookup"><span data-stu-id="ab0ef-146">\*ConditionalExpression\***\|\|**_ConditionalExpression_</span></span><br/> | <span data-ttu-id="ab0ef-147">Проверяет, имеет ли любое из указанных условных выражений значение true.</span><span class="sxs-lookup"><span data-stu-id="ab0ef-147">Tests whether either of the specified conditional expressions is true.</span></span><br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                 |
| <span data-ttu-id="ab0ef-148">*Кондитионалекспрессион* **&&** *Кондитионалекспрессион*</span><span class="sxs-lookup"><span data-stu-id="ab0ef-148">*ConditionalExpression* **&&** *ConditionalExpression*</span></span><br/> | <span data-ttu-id="ab0ef-149">Проверяет, имеет ли оба указанных условных выражений значение true.</span><span class="sxs-lookup"><span data-stu-id="ab0ef-149">Tests whether both of the specified conditional expressions are true.</span></span><br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                  |
| <span data-ttu-id="ab0ef-150">**! (**_Кондитионалекспрессион_*_)_*</span><span class="sxs-lookup"><span data-stu-id="ab0ef-150">**!(**_ConditionalExpression_*_)_*</span></span><br/>                     | <span data-ttu-id="ab0ef-151">Обратная часть условного выражения.</span><span class="sxs-lookup"><span data-stu-id="ab0ef-151">The inverse of a conditional expression.</span></span><br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                               |
| <span data-ttu-id="ab0ef-152">**Член \_ {**_сидаррай_*_}_*</span><span class="sxs-lookup"><span data-stu-id="ab0ef-152">**Member\_of{**_SidArray_*_}_*</span></span><br/>                         | <span data-ttu-id="ab0ef-153">Проверяет, содержит ли массив [**SID \_ и \_ атрибуты**](/windows/desktop/api/Winnt/ns-winnt-sid_and_attributes) контекста клиента все [идентификаторы безопасности](security-identifiers.md) (SID) в списке с разделителями-запятыми, заданном параметром *сидаррай*.</span><span class="sxs-lookup"><span data-stu-id="ab0ef-153">Tests whether the [**SID\_AND\_ATTRIBUTES**](/windows/desktop/api/Winnt/ns-winnt-sid_and_attributes) array of the client context contains all of the [Security Identifiers](security-identifiers.md) (SIDs) in the comma-separated list specified by *SidArray*.</span></span><br/> <span data-ttu-id="ab0ef-154">Для параметра Разрешить ACE для контекста клиента необходимо, чтобы атрибут **SE \_ Group \_ Enabled** был установлен как совпадающий.</span><span class="sxs-lookup"><span data-stu-id="ab0ef-154">For Allow ACEs, a client context SID must have the **SE\_GROUP\_ENABLED** attribute set to be considered a match.</span></span><br/> <span data-ttu-id="ab0ef-155">Для запрета доступа ACE для контекста клиента необходимо **\_ \_ включить группу SE** или параметр **\_ использовать группу SE \_ \_ \_ \_ только для атрибута запретить** , чтобы считаться совпадением.</span><span class="sxs-lookup"><span data-stu-id="ab0ef-155">For Deny ACEs, a client context SID must have either the **SE\_GROUP\_ENABLED** or the **SE\_GROUP\_USE\_FOR\_DENY\_ONLY** attribute set to be considered a match.</span></span><br/> <span data-ttu-id="ab0ef-156">Массив *сидаррай* может содержать строки SID (например, "S-1-5-6") или псевдонимы SID (например, "BA"</span><span class="sxs-lookup"><span data-stu-id="ab0ef-156">The *SidArray* array can contain either SID strings (for example, "S-1-5-6") or SID aliases (for example, "BA"</span></span><br/> |



 

## <a name="attributes"></a><span data-ttu-id="ab0ef-157">Атрибуты</span><span class="sxs-lookup"><span data-stu-id="ab0ef-157">Attributes</span></span>

<span data-ttu-id="ab0ef-158">Атрибут представляет элемент в массиве [**\_ \_ \_ сведений об атрибутах безопасности AUTHZ**](/windows/desktop/api/Authz/ns-authz-authz_security_attributes_information) в контексте клиента.</span><span class="sxs-lookup"><span data-stu-id="ab0ef-158">An attribute represents an element in the [**AUTHZ\_SECURITY\_ATTRIBUTES\_INFORMATION**](/windows/desktop/api/Authz/ns-authz-authz_security_attributes_information) array in the client context.</span></span> <span data-ttu-id="ab0ef-159">Имя атрибута может содержать любые буквенно-цифровые символы и любые символы ":", "/", "." и " \_ ".</span><span class="sxs-lookup"><span data-stu-id="ab0ef-159">An attribute name can contain any alphanumeric characters and any of the characters ":", "/", ".", and "\_".</span></span>

<span data-ttu-id="ab0ef-160">Значением атрибута может быть любой из следующих типов.</span><span class="sxs-lookup"><span data-stu-id="ab0ef-160">An attribute value can be any of the following types.</span></span>



| <span data-ttu-id="ab0ef-161">Тип значения</span><span class="sxs-lookup"><span data-stu-id="ab0ef-161">Value type</span></span>         | <span data-ttu-id="ab0ef-162">Описание</span><span class="sxs-lookup"><span data-stu-id="ab0ef-162">Description</span></span>                                                                                                                                                                                         |
|--------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="ab0ef-163">Целочисленный тип</span><span class="sxs-lookup"><span data-stu-id="ab0ef-163">Integer</span></span><br/> | <span data-ttu-id="ab0ef-164">64-разрядное целое число в десятичной или шестнадцатеричной нотации.</span><span class="sxs-lookup"><span data-stu-id="ab0ef-164">A 64-bit integer in either decimal or hexadecimal notation.</span></span><br/>                                                                                                                              |
| <span data-ttu-id="ab0ef-165">Строка</span><span class="sxs-lookup"><span data-stu-id="ab0ef-165">String</span></span><br/>  | <span data-ttu-id="ab0ef-166">Строковое значение, разделенное кавычками.</span><span class="sxs-lookup"><span data-stu-id="ab0ef-166">A string value delimited by quotes.</span></span><br/>                                                                                                                                                      |
| <span data-ttu-id="ab0ef-167">SID</span><span class="sxs-lookup"><span data-stu-id="ab0ef-167">SID</span></span><br/>     | <span data-ttu-id="ab0ef-168">SID (S-1-1-0) или SID (BA).</span><span class="sxs-lookup"><span data-stu-id="ab0ef-168">SID(S-1-1-0) or SID(BA).</span></span> <span data-ttu-id="ab0ef-169">Должен находиться в RHS участника \_ или устройства \_ \_ .</span><span class="sxs-lookup"><span data-stu-id="ab0ef-169">Has to be on RHS of Member\_of or Device\_Member\_of.</span></span><br/>                                                                                                           |
| <span data-ttu-id="ab0ef-170">BLOB</span><span class="sxs-lookup"><span data-stu-id="ab0ef-170">BLOB</span></span><br/>    | <span data-ttu-id="ab0ef-171">\# с последующими шестнадцатеричными числами.</span><span class="sxs-lookup"><span data-stu-id="ab0ef-171">\# followed by hexadecimal numbers.</span></span> <span data-ttu-id="ab0ef-172">Если длина чисел нечетна, то \# преобразуется в 0, чтобы сделать его четным.</span><span class="sxs-lookup"><span data-stu-id="ab0ef-172">If length of the numbers is odd, then the \# is translated to a 0 to make it even.</span></span> <span data-ttu-id="ab0ef-173">Кроме того, при \# появления в любом другое место в значении преобразуется в 0.</span><span class="sxs-lookup"><span data-stu-id="ab0ef-173">Also an \# appearing elsewhere in the value is translated to a 0.</span></span><br/> |



 

## <a name="operators"></a><span data-ttu-id="ab0ef-174">Операторы</span><span class="sxs-lookup"><span data-stu-id="ab0ef-174">Operators</span></span>

<span data-ttu-id="ab0ef-175">Следующие операторы определяются для использования в условных выражениях для проверки значений атрибутов.</span><span class="sxs-lookup"><span data-stu-id="ab0ef-175">The following operators are defined for use in conditional expressions to test the values of attributes.</span></span> <span data-ttu-id="ab0ef-176">Все они являются бинарными операторами и используются в виде   *значения* оператора AttributeName.</span><span class="sxs-lookup"><span data-stu-id="ab0ef-176">All of these are binary operators and used in the form *AttributeName* *Operator* *Value*.</span></span>



| <span data-ttu-id="ab0ef-177">Оператор</span><span class="sxs-lookup"><span data-stu-id="ab0ef-177">Operator</span></span>            | <span data-ttu-id="ab0ef-178">Описание</span><span class="sxs-lookup"><span data-stu-id="ab0ef-178">Description</span></span>                                                                                                              |
|---------------------|--------------------------------------------------------------------------------------------------------------------------|
| ==<br/>       | <span data-ttu-id="ab0ef-179">Стандартное определение.</span><span class="sxs-lookup"><span data-stu-id="ab0ef-179">Conventional definition.</span></span><br/>                                                                                      |
| <span data-ttu-id="ab0ef-180">!=</span><span class="sxs-lookup"><span data-stu-id="ab0ef-180">!=</span></span><br/>       | <span data-ttu-id="ab0ef-181">Стандартное определение.</span><span class="sxs-lookup"><span data-stu-id="ab0ef-181">Conventional definition.</span></span><br/>                                                                                      |
| <<br/>     | <span data-ttu-id="ab0ef-182">Стандартное определение.</span><span class="sxs-lookup"><span data-stu-id="ab0ef-182">Conventional definition.</span></span><br/>                                                                                      |
| <=<br/>    | <span data-ttu-id="ab0ef-183">Стандартное определение.</span><span class="sxs-lookup"><span data-stu-id="ab0ef-183">Conventional definition.</span></span><br/>                                                                                      |
| ><br/>     | <span data-ttu-id="ab0ef-184">Стандартное определение.</span><span class="sxs-lookup"><span data-stu-id="ab0ef-184">Conventional definition.</span></span><br/>                                                                                      |
| >=<br/>    | <span data-ttu-id="ab0ef-185">Стандартное определение.</span><span class="sxs-lookup"><span data-stu-id="ab0ef-185">Conventional definition.</span></span><br/>                                                                                      |
| <span data-ttu-id="ab0ef-186">Содержит</span><span class="sxs-lookup"><span data-stu-id="ab0ef-186">Contains</span></span><br/> | <span data-ttu-id="ab0ef-187">Значение **true** , если значение указанного атрибута является надмножеством указанного значения; в противном случае — **значение false**.</span><span class="sxs-lookup"><span data-stu-id="ab0ef-187">**TRUE** if the value of the specified attribute is a superset of the specified value; otherwise, **FALSE**.</span></span><br/>  |
| <span data-ttu-id="ab0ef-188">Любой \_ из</span><span class="sxs-lookup"><span data-stu-id="ab0ef-188">Any\_of</span></span><br/>  | <span data-ttu-id="ab0ef-189">Значение **true** , если указанное значение является надмножеством значения указанного атрибута; в противном случае — **значение false**.</span><span class="sxs-lookup"><span data-stu-id="ab0ef-189">**TRUE** if the specified value is a superset of the value of the specified attribute; otherwise, **FALSE**.</span></span> <br/> |



 

<span data-ttu-id="ab0ef-190">Кроме того, унарные операторы EXISTS, Member \_ и отрицание (!) определяются, как описано в таблице условные выражения.</span><span class="sxs-lookup"><span data-stu-id="ab0ef-190">In addition, the unary operators Exists, Member\_of, and negation (!) are defined as described in the Conditional Expressions table.</span></span>

<span data-ttu-id="ab0ef-191">Оператору "Contains" перед ним должен предшествовать пробел, а \_ оператору "any of" должен предшествовать пробел.</span><span class="sxs-lookup"><span data-stu-id="ab0ef-191">The "Contains" operator must be preceded and followed by white space, and the "Any\_of" operator must be preceded by white space.</span></span>

## <a name="operator-precedence"></a><span data-ttu-id="ab0ef-192">Приоритет операторов</span><span class="sxs-lookup"><span data-stu-id="ab0ef-192">Operator Precedence</span></span>

<span data-ttu-id="ab0ef-193">Операторы оцениваются в следующем порядке приоритета, при этом операции с одинаковым приоритетом оцениваются слева направо.</span><span class="sxs-lookup"><span data-stu-id="ab0ef-193">The operators are evaluated in the following order of precedence, with operations of equal precedence being evaluated from left to right.</span></span>

1.  <span data-ttu-id="ab0ef-194">Существует \_ , член</span><span class="sxs-lookup"><span data-stu-id="ab0ef-194">Exists, Member\_of</span></span>
2.  <span data-ttu-id="ab0ef-195">Содержит, любой \_ из</span><span class="sxs-lookup"><span data-stu-id="ab0ef-195">Contains, Any\_of</span></span>
3.  <span data-ttu-id="ab0ef-196">= =,! =, <, <=, >, >=</span><span class="sxs-lookup"><span data-stu-id="ab0ef-196">==, !=, <, <=, >, >=</span></span>
4.  <span data-ttu-id="ab0ef-197">!</span><span class="sxs-lookup"><span data-stu-id="ab0ef-197">!</span></span>
5.  &&
6.  \|\|

<span data-ttu-id="ab0ef-198">Кроме того, любая часть условного выражения может быть заключена в круглые скобки.</span><span class="sxs-lookup"><span data-stu-id="ab0ef-198">In addition, any portion of a conditional expression can be enclosed in parenthesis.</span></span> <span data-ttu-id="ab0ef-199">Выражения в круглых скобках оцениваются первыми.</span><span class="sxs-lookup"><span data-stu-id="ab0ef-199">Expressions within parentheses are evaluated first.</span></span>

## <a name="unknown-values"></a><span data-ttu-id="ab0ef-200">Неизвестные значения</span><span class="sxs-lookup"><span data-stu-id="ab0ef-200">Unknown Values</span></span>

<span data-ttu-id="ab0ef-201">Результаты условных выражений иногда возвращают значение **Unknown**.</span><span class="sxs-lookup"><span data-stu-id="ab0ef-201">The results of conditional expressions sometimes return a value of **Unknown**.</span></span> <span data-ttu-id="ab0ef-202">Например, любая из реляционных операций возвращает значение **Unknown** , если указанный атрибут не существует.</span><span class="sxs-lookup"><span data-stu-id="ab0ef-202">For example, any of the relational operations return **Unknown** when the specified attribute does not exist.</span></span>

<span data-ttu-id="ab0ef-203">В следующей таблице описаны результаты логической операции **and** между двумя условными выражениями, *ConditionalExpression1* и *ConditionalExpression2*.</span><span class="sxs-lookup"><span data-stu-id="ab0ef-203">The following table describes the results for a logical **AND** operation between two conditional expressions, *ConditionalExpression1* and *ConditionalExpression2*.</span></span>



| <span data-ttu-id="ab0ef-204">*ConditionalExpression1*</span><span class="sxs-lookup"><span data-stu-id="ab0ef-204">*ConditionalExpression1*</span></span> | <span data-ttu-id="ab0ef-205">*ConditionalExpression2*</span><span class="sxs-lookup"><span data-stu-id="ab0ef-205">*ConditionalExpression2*</span></span> | <span data-ttu-id="ab0ef-206">*ConditionalExpression1* **&&** *ConditionalExpression2*</span><span class="sxs-lookup"><span data-stu-id="ab0ef-206">*ConditionalExpression1* **&&** *ConditionalExpression2*</span></span> |
|--------------------------|--------------------------|----------------------------------------------------------|
| <span data-ttu-id="ab0ef-207">**TRUE**</span><span class="sxs-lookup"><span data-stu-id="ab0ef-207">**TRUE**</span></span><br/>      | <span data-ttu-id="ab0ef-208">**TRUE**</span><span class="sxs-lookup"><span data-stu-id="ab0ef-208">**TRUE**</span></span><br/>      | <span data-ttu-id="ab0ef-209">**TRUE**</span><span class="sxs-lookup"><span data-stu-id="ab0ef-209">**TRUE**</span></span><br/>                                      |
| <span data-ttu-id="ab0ef-210">**TRUE**</span><span class="sxs-lookup"><span data-stu-id="ab0ef-210">**TRUE**</span></span><br/>      | <span data-ttu-id="ab0ef-211">**FALSE**</span><span class="sxs-lookup"><span data-stu-id="ab0ef-211">**FALSE**</span></span><br/>     | <span data-ttu-id="ab0ef-212">**FALSE**</span><span class="sxs-lookup"><span data-stu-id="ab0ef-212">**FALSE**</span></span><br/>                                     |
| <span data-ttu-id="ab0ef-213">**TRUE**</span><span class="sxs-lookup"><span data-stu-id="ab0ef-213">**TRUE**</span></span><br/>      | <span data-ttu-id="ab0ef-214">**UNKNOWN**</span><span class="sxs-lookup"><span data-stu-id="ab0ef-214">**UNKNOWN**</span></span><br/>   | <span data-ttu-id="ab0ef-215">**UNKNOWN**</span><span class="sxs-lookup"><span data-stu-id="ab0ef-215">**UNKNOWN**</span></span><br/>                                   |
| <span data-ttu-id="ab0ef-216">**FALSE**</span><span class="sxs-lookup"><span data-stu-id="ab0ef-216">**FALSE**</span></span><br/>     | <span data-ttu-id="ab0ef-217">**TRUE**</span><span class="sxs-lookup"><span data-stu-id="ab0ef-217">**TRUE**</span></span><br/>      | <span data-ttu-id="ab0ef-218">**FALSE**</span><span class="sxs-lookup"><span data-stu-id="ab0ef-218">**FALSE**</span></span><br/>                                     |
| <span data-ttu-id="ab0ef-219">**FALSE**</span><span class="sxs-lookup"><span data-stu-id="ab0ef-219">**FALSE**</span></span><br/>     | <span data-ttu-id="ab0ef-220">**FALSE**</span><span class="sxs-lookup"><span data-stu-id="ab0ef-220">**FALSE**</span></span><br/>     | <span data-ttu-id="ab0ef-221">**FALSE**</span><span class="sxs-lookup"><span data-stu-id="ab0ef-221">**FALSE**</span></span><br/>                                     |
| <span data-ttu-id="ab0ef-222">**FALSE**</span><span class="sxs-lookup"><span data-stu-id="ab0ef-222">**FALSE**</span></span><br/>     | <span data-ttu-id="ab0ef-223">**UNKNOWN**</span><span class="sxs-lookup"><span data-stu-id="ab0ef-223">**UNKNOWN**</span></span><br/>   | <span data-ttu-id="ab0ef-224">**FALSE**</span><span class="sxs-lookup"><span data-stu-id="ab0ef-224">**FALSE**</span></span><br/>                                     |
| <span data-ttu-id="ab0ef-225">**UNKNOWN**</span><span class="sxs-lookup"><span data-stu-id="ab0ef-225">**UNKNOWN**</span></span><br/>   | <span data-ttu-id="ab0ef-226">**TRUE**</span><span class="sxs-lookup"><span data-stu-id="ab0ef-226">**TRUE**</span></span><br/>      | <span data-ttu-id="ab0ef-227">**UNKNOWN**</span><span class="sxs-lookup"><span data-stu-id="ab0ef-227">**UNKNOWN**</span></span><br/>                                   |
| <span data-ttu-id="ab0ef-228">**UNKNOWN**</span><span class="sxs-lookup"><span data-stu-id="ab0ef-228">**UNKNOWN**</span></span><br/>   | <span data-ttu-id="ab0ef-229">**FALSE**</span><span class="sxs-lookup"><span data-stu-id="ab0ef-229">**FALSE**</span></span><br/>     | <span data-ttu-id="ab0ef-230">**FALSE**</span><span class="sxs-lookup"><span data-stu-id="ab0ef-230">**FALSE**</span></span><br/>                                     |
| <span data-ttu-id="ab0ef-231">**UNKNOWN**</span><span class="sxs-lookup"><span data-stu-id="ab0ef-231">**UNKNOWN**</span></span><br/>   | <span data-ttu-id="ab0ef-232">**UNKNOWN**</span><span class="sxs-lookup"><span data-stu-id="ab0ef-232">**UNKNOWN**</span></span><br/>   | <span data-ttu-id="ab0ef-233">**UNKNOWN**</span><span class="sxs-lookup"><span data-stu-id="ab0ef-233">**UNKNOWN**</span></span><br/>                                   |



 

<span data-ttu-id="ab0ef-234">В следующей таблице описаны результаты логической операции **or** между двумя условными выражениями, *ConditionalExpression1* и *ConditionalExpression2*.</span><span class="sxs-lookup"><span data-stu-id="ab0ef-234">The following table describes the results for a logical **OR** operation between two conditional expressions, *ConditionalExpression1* and *ConditionalExpression2*.</span></span>



| <span data-ttu-id="ab0ef-235">*ConditionalExpression1*</span><span class="sxs-lookup"><span data-stu-id="ab0ef-235">*ConditionalExpression1*</span></span> | <span data-ttu-id="ab0ef-236">*ConditionalExpression2*</span><span class="sxs-lookup"><span data-stu-id="ab0ef-236">*ConditionalExpression2*</span></span> | <span data-ttu-id="ab0ef-237">*ConditionalExpression1* \*\*</span><span class="sxs-lookup"><span data-stu-id="ab0ef-237">*ConditionalExpression1* \*\*</span></span>\|\|<span data-ttu-id="ab0ef-238">\*\* *ConditionalExpression2*</span><span class="sxs-lookup"><span data-stu-id="ab0ef-238">\*\* *ConditionalExpression2*</span></span> |
|--------------------------|--------------------------|------------------------------------------------------------|
| <span data-ttu-id="ab0ef-239">**TRUE**</span><span class="sxs-lookup"><span data-stu-id="ab0ef-239">**TRUE**</span></span><br/>      | <span data-ttu-id="ab0ef-240">**TRUE**</span><span class="sxs-lookup"><span data-stu-id="ab0ef-240">**TRUE**</span></span><br/>      | <span data-ttu-id="ab0ef-241">**TRUE**</span><span class="sxs-lookup"><span data-stu-id="ab0ef-241">**TRUE**</span></span><br/>                                        |
| <span data-ttu-id="ab0ef-242">**TRUE**</span><span class="sxs-lookup"><span data-stu-id="ab0ef-242">**TRUE**</span></span><br/>      | <span data-ttu-id="ab0ef-243">**FALSE**</span><span class="sxs-lookup"><span data-stu-id="ab0ef-243">**FALSE**</span></span><br/>     | <span data-ttu-id="ab0ef-244">**TRUE**</span><span class="sxs-lookup"><span data-stu-id="ab0ef-244">**TRUE**</span></span><br/>                                        |
| <span data-ttu-id="ab0ef-245">**TRUE**</span><span class="sxs-lookup"><span data-stu-id="ab0ef-245">**TRUE**</span></span><br/>      | <span data-ttu-id="ab0ef-246">**UNKNOWN**</span><span class="sxs-lookup"><span data-stu-id="ab0ef-246">**UNKNOWN**</span></span><br/>   | <span data-ttu-id="ab0ef-247">**TRUE**</span><span class="sxs-lookup"><span data-stu-id="ab0ef-247">**TRUE**</span></span><br/>                                        |
| <span data-ttu-id="ab0ef-248">**FALSE**</span><span class="sxs-lookup"><span data-stu-id="ab0ef-248">**FALSE**</span></span><br/>     | <span data-ttu-id="ab0ef-249">**TRUE**</span><span class="sxs-lookup"><span data-stu-id="ab0ef-249">**TRUE**</span></span><br/>      | <span data-ttu-id="ab0ef-250">**TRUE**</span><span class="sxs-lookup"><span data-stu-id="ab0ef-250">**TRUE**</span></span><br/>                                        |
| <span data-ttu-id="ab0ef-251">**FALSE**</span><span class="sxs-lookup"><span data-stu-id="ab0ef-251">**FALSE**</span></span><br/>     | <span data-ttu-id="ab0ef-252">**FALSE**</span><span class="sxs-lookup"><span data-stu-id="ab0ef-252">**FALSE**</span></span><br/>     | <span data-ttu-id="ab0ef-253">**FALSE**</span><span class="sxs-lookup"><span data-stu-id="ab0ef-253">**FALSE**</span></span><br/>                                       |
| <span data-ttu-id="ab0ef-254">**FALSE**</span><span class="sxs-lookup"><span data-stu-id="ab0ef-254">**FALSE**</span></span><br/>     | <span data-ttu-id="ab0ef-255">**UNKNOWN**</span><span class="sxs-lookup"><span data-stu-id="ab0ef-255">**UNKNOWN**</span></span><br/>   | <span data-ttu-id="ab0ef-256">**UNKNOWN**</span><span class="sxs-lookup"><span data-stu-id="ab0ef-256">**UNKNOWN**</span></span><br/>                                     |
| <span data-ttu-id="ab0ef-257">**UNKNOWN**</span><span class="sxs-lookup"><span data-stu-id="ab0ef-257">**UNKNOWN**</span></span><br/>   | <span data-ttu-id="ab0ef-258">**TRUE**</span><span class="sxs-lookup"><span data-stu-id="ab0ef-258">**TRUE**</span></span><br/>      | <span data-ttu-id="ab0ef-259">**TRUE**</span><span class="sxs-lookup"><span data-stu-id="ab0ef-259">**TRUE**</span></span><br/>                                        |
| <span data-ttu-id="ab0ef-260">**UNKNOWN**</span><span class="sxs-lookup"><span data-stu-id="ab0ef-260">**UNKNOWN**</span></span><br/>   | <span data-ttu-id="ab0ef-261">**FALSE**</span><span class="sxs-lookup"><span data-stu-id="ab0ef-261">**FALSE**</span></span><br/>     | <span data-ttu-id="ab0ef-262">**UNKNOWN**</span><span class="sxs-lookup"><span data-stu-id="ab0ef-262">**UNKNOWN**</span></span><br/>                                     |
| <span data-ttu-id="ab0ef-263">**UNKNOWN**</span><span class="sxs-lookup"><span data-stu-id="ab0ef-263">**UNKNOWN**</span></span><br/>   | <span data-ttu-id="ab0ef-264">**UNKNOWN**</span><span class="sxs-lookup"><span data-stu-id="ab0ef-264">**UNKNOWN**</span></span><br/>   | <span data-ttu-id="ab0ef-265">**UNKNOWN**</span><span class="sxs-lookup"><span data-stu-id="ab0ef-265">**UNKNOWN**</span></span><br/>                                     |



 

<span data-ttu-id="ab0ef-266">Отрицание условного выражения со значением **Unknown** также **неизвестно**.</span><span class="sxs-lookup"><span data-stu-id="ab0ef-266">The negation of a conditional expression with a value of **UNKNOWN** is also **UNKNOWN**.</span></span>

## <a name="conditional-ace-evaluation"></a><span data-ttu-id="ab0ef-267">Условная оценка ACE</span><span class="sxs-lookup"><span data-stu-id="ab0ef-267">Conditional ACE Evaluation</span></span>

<span data-ttu-id="ab0ef-268">В следующей таблице описывается результат проверки доступа условного элемента управления доступом в зависимости от окончательной оценки условного выражения.</span><span class="sxs-lookup"><span data-stu-id="ab0ef-268">The following table describes the access check result of a conditional ACE depending on the final evaluation of the conditional expression.</span></span>

| <span data-ttu-id="ab0ef-269">Тип ACE</span><span class="sxs-lookup"><span data-stu-id="ab0ef-269">ACE type</span></span>         | <span data-ttu-id="ab0ef-270">TRUE</span><span class="sxs-lookup"><span data-stu-id="ab0ef-270">TRUE</span></span>             | <span data-ttu-id="ab0ef-271">FALSE</span><span class="sxs-lookup"><span data-stu-id="ab0ef-271">FALSE</span></span>                 | <span data-ttu-id="ab0ef-272">UNKNOWN</span><span class="sxs-lookup"><span data-stu-id="ab0ef-272">UNKNOWN</span></span>               |
|------------------|------------------|-----------------------|-----------------------|
| <span data-ttu-id="ab0ef-273">Allow</span><span class="sxs-lookup"><span data-stu-id="ab0ef-273">Allow</span></span><br/> | <span data-ttu-id="ab0ef-274">Allow</span><span class="sxs-lookup"><span data-stu-id="ab0ef-274">Allow</span></span><br/> | <span data-ttu-id="ab0ef-275">Игнорировать ACE</span><span class="sxs-lookup"><span data-stu-id="ab0ef-275">Ignore ACE</span></span><br/> | <span data-ttu-id="ab0ef-276">Игнорировать ACE</span><span class="sxs-lookup"><span data-stu-id="ab0ef-276">Ignore ACE</span></span><br/> |
| <span data-ttu-id="ab0ef-277">Запрет</span><span class="sxs-lookup"><span data-stu-id="ab0ef-277">Deny</span></span><br/>  | <span data-ttu-id="ab0ef-278">Запрет</span><span class="sxs-lookup"><span data-stu-id="ab0ef-278">Deny</span></span><br/>  | <span data-ttu-id="ab0ef-279">Игнорировать ACE</span><span class="sxs-lookup"><span data-stu-id="ab0ef-279">Ignore ACE</span></span><br/> | <span data-ttu-id="ab0ef-280">Запрет</span><span class="sxs-lookup"><span data-stu-id="ab0ef-280">Deny</span></span><br/>       |



 

## <a name="examples"></a><span data-ttu-id="ab0ef-281">Примеры</span><span class="sxs-lookup"><span data-stu-id="ab0ef-281">Examples</span></span>

<span data-ttu-id="ab0ef-282">В следующих примерах показано, как указанные политики доступа представлены условным элементом ACE, определенным с помощью SDDL.</span><span class="sxs-lookup"><span data-stu-id="ab0ef-282">The following examples show how the specified access policies are represented by a conditional ACE defined by using SDDL.</span></span>

<dl> <dt>

<span data-ttu-id="ab0ef-283"><span id="Policy"></span><span id="policy"></span><span id="POLICY"></span>Политик</span><span class="sxs-lookup"><span data-stu-id="ab0ef-283"><span id="Policy"></span><span id="policy"></span><span id="POLICY"></span>Policy</span></span>
</dt> <dd>

<span data-ttu-id="ab0ef-284">Разрешить выполнение всем, если выполняются оба следующих условия.</span><span class="sxs-lookup"><span data-stu-id="ab0ef-284">Allow Execute to Everyone if both of the following conditions are met:</span></span>

-   <span data-ttu-id="ab0ef-285">Title = PM</span><span class="sxs-lookup"><span data-stu-id="ab0ef-285">Title = PM</span></span>
-   <span data-ttu-id="ab0ef-286">Деление = финансы или деление = продажи</span><span class="sxs-lookup"><span data-stu-id="ab0ef-286">Division = Finance or Division = Sales</span></span>

</dd> <dt>

<span data-ttu-id="ab0ef-287"><span id="SDDL"></span><span id="sddl"></span>АВТОРИЗАЦИИ</span><span class="sxs-lookup"><span data-stu-id="ab0ef-287"><span id="SDDL"></span><span id="sddl"></span>SDDL</span></span>
</dt> <dd>

<span data-ttu-id="ab0ef-288">D: (XA;; FX;;; S-1-1-0; ( @User.Title = = "PM"  &&  ( @User.Division = = "Финансы" \| \| @User.Division = = "Sales")))</span><span class="sxs-lookup"><span data-stu-id="ab0ef-288">D:(XA; ;FX;;;S-1-1-0; (@User.Title=="PM" && (@User.Division=="Finance" \|\| @User.Division ==" Sales")))</span></span>

</dd> <dt>

 
</dt> <dd>

 

</dd> <dt>

<span data-ttu-id="ab0ef-289"><span id="Policy"></span><span id="policy"></span><span id="POLICY"></span>Политик</span><span class="sxs-lookup"><span data-stu-id="ab0ef-289"><span id="Policy"></span><span id="policy"></span><span id="POLICY"></span>Policy</span></span>
</dt> <dd>

<span data-ttu-id="ab0ef-290">Разрешить Execute, если любой из пользовательских проектов пересекается с проектами файлов.</span><span class="sxs-lookup"><span data-stu-id="ab0ef-290">Allow execute if any of the user s projects intersect with the file s projects.</span></span>

</dd> <dt>

<span data-ttu-id="ab0ef-291"><span id="SDDL"></span><span id="sddl"></span>АВТОРИЗАЦИИ</span><span class="sxs-lookup"><span data-stu-id="ab0ef-291"><span id="SDDL"></span><span id="sddl"></span>SDDL</span></span>
</dt> <dd>

<span data-ttu-id="ab0ef-292">D: (XA;; FX;;; S-1-1-0; ( @User.Project Любой \_ из @Resource.Project )</span><span class="sxs-lookup"><span data-stu-id="ab0ef-292">D:(XA; ;FX;;;S-1-1-0; (@User.Project Any\_of @Resource.Project))</span></span>

</dd> <dt>

 
</dt> <dd>

 

</dd> <dt>

<span data-ttu-id="ab0ef-293"><span id="Policy"></span><span id="policy"></span><span id="POLICY"></span>Политик</span><span class="sxs-lookup"><span data-stu-id="ab0ef-293"><span id="Policy"></span><span id="policy"></span><span id="POLICY"></span>Policy</span></span>
</dt> <dd>

<span data-ttu-id="ab0ef-294">Разрешить доступ на чтение, если пользователь выполнил вход с помощью смарт-карты, является оператором резервного копирования и подключается к компьютеру с включенным BitLocker.</span><span class="sxs-lookup"><span data-stu-id="ab0ef-294">Allow read access if the user has logged in with a smart card, is a backup operator, and is connecting from a machine with Bitlocker enabled.</span></span>

</dd> <dt>

<span data-ttu-id="ab0ef-295"><span id="SDDL"></span><span id="sddl"></span>АВТОРИЗАЦИИ</span><span class="sxs-lookup"><span data-stu-id="ab0ef-295"><span id="SDDL"></span><span id="sddl"></span>SDDL</span></span>
</dt> <dd>

<span data-ttu-id="ab0ef-296">D: (XA;; FR;;; S-1-1-0; (Член \_ {sid (ИД безопасности смарт-карты \_ ), SID (т. е.)}  && @Device.Bitlocker ))</span><span class="sxs-lookup"><span data-stu-id="ab0ef-296">D:(XA; ;FR;;;S-1-1-0; (Member\_of {SID(Smartcard\_SID), SID(BO)} && @Device.Bitlocker))</span></span>

</dd> <dt>

 
</dt> <dd>

 

</dd> </dl>

## <a name="related-topics"></a><span data-ttu-id="ab0ef-297">См. также</span><span class="sxs-lookup"><span data-stu-id="ab0ef-297">Related topics</span></span>

<dl> <dt>

<span data-ttu-id="ab0ef-298">[\[MS-ДТИП \] : язык описания дескрипторов безопасности](/openspecs/windows_protocols/ms-dtyp/4f4251cc-23b6-44b6-93ba-69688422cb06)</span><span class="sxs-lookup"><span data-stu-id="ab0ef-298">[\[MS-DTYP\]: Security Descriptor Description Language](/openspecs/windows_protocols/ms-dtyp/4f4251cc-23b6-44b6-93ba-69688422cb06)</span></span>
</dt> </dl>

