---
title: " Директивы if, elif, else и endif"
description: Директивы препроцессора, управляющие компиляцией частей исходного файла.
ms.assetid: f29e5a9b-cc0c-4fca-aac7-809a226eda58
keywords:
- Директивы if, elif, else и endif HLSL
topic_type:
- apiref
api_name:
- if, elif, else, and endif Directives
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: a32206232c726f19febf77c3f3270882894a6747
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "104133894"
---
# <a name="if-elif-else-and-endif-directives"></a><span data-ttu-id="e9991-104">\#\#директивы if, elif, \# else и \# endif</span><span class="sxs-lookup"><span data-stu-id="e9991-104">\#if, \#elif, \#else, and \#endif Directives</span></span>

<span data-ttu-id="e9991-105">Директивы препроцессора, управляющие компиляцией частей исходного файла.</span><span class="sxs-lookup"><span data-stu-id="e9991-105">Preprocessor directives that control compilation of portions of a source file.</span></span>



| <span data-ttu-id="e9991-106">\#Если *ифкондитион* ...</span><span class="sxs-lookup"><span data-stu-id="e9991-106">\#if *ifCondition* ...</span></span>         |
|--------------------------------|
| <span data-ttu-id="e9991-107">\[\#*елифкондитион* elif...\]</span><span class="sxs-lookup"><span data-stu-id="e9991-107">\[\#elif *elifCondition* ...\]</span></span> |
| <span data-ttu-id="e9991-108">\[\#else...\]</span><span class="sxs-lookup"><span data-stu-id="e9991-108">\[\#else ...\]</span></span>                 |
| <span data-ttu-id="e9991-109">\#endif</span><span class="sxs-lookup"><span data-stu-id="e9991-109">\#endif</span></span>                        |



 

## <a name="parameters"></a><span data-ttu-id="e9991-110">Параметры</span><span class="sxs-lookup"><span data-stu-id="e9991-110">Parameters</span></span>



| <span data-ttu-id="e9991-111">Элемент</span><span class="sxs-lookup"><span data-stu-id="e9991-111">Item</span></span>                                                                                                                                                                                                 | <span data-ttu-id="e9991-112">Описание</span><span class="sxs-lookup"><span data-stu-id="e9991-112">Description</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                    |
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="e9991-113"><span id="ifCondition"></span><span id="ifcondition"></span><span id="IFCONDITION"></span>*ифкондитион*</span><span class="sxs-lookup"><span data-stu-id="e9991-113"><span id="ifCondition"></span><span id="ifcondition"></span><span id="IFCONDITION"></span>*ifCondition*</span></span><br/>                                                                                   | <span data-ttu-id="e9991-114">Основное условие для вычисления.</span><span class="sxs-lookup"><span data-stu-id="e9991-114">Primary condition to evaluate.</span></span> <span data-ttu-id="e9991-115">Если этот параметр принимает ненулевое значение, весь текст между этой \# директивой If и следующим экземпляром \# директивы elif, \# Else или \# endif сохраняется в записи преобразования; в противном случае следующий исходный код не сохраняется.</span><span class="sxs-lookup"><span data-stu-id="e9991-115">If this parameter evaluates to a nonzero value, all text between this \#if directive and the next instance of the \#elif, \#else, or \#endif directive is retained in the translation unit; otherwise, the subsequent source code is not retained.</span></span> <br/> <span data-ttu-id="e9991-116">Условие может использовать оператор препроцессора, определенный для определения, определена ли конкретная константа препроцессора или макрос. Это использование эквивалентно использованию директивы [ \# ifdef](dx-graphics-hlsl-appendix-pre-ifdef.md) .</span><span class="sxs-lookup"><span data-stu-id="e9991-116">The condition can use the preprocessor operator defined to determine whether a specific preprocessor constant or macro is defined; this usage is equivalent to the use of the [\#ifdef](dx-graphics-hlsl-appendix-pre-ifdef.md) directive.</span></span> <br/> <span data-ttu-id="e9991-117">Ограничения на значение параметра *ифкондитион* см. в разделе "Примечания".</span><span class="sxs-lookup"><span data-stu-id="e9991-117">See the Remarks section for restrictions on the value of the *ifCondition* parameter.</span></span> <br/>                                                                                        |
| <span data-ttu-id="e9991-118"><span id="elifCondition__optional__________"></span><span id="elifcondition__optional__________"></span><span id="ELIFCONDITION__OPTIONAL__________"></span>*елифкондитион* \[ используемых\]</span><span class="sxs-lookup"><span data-stu-id="e9991-118"><span id="elifCondition__optional__________"></span><span id="elifcondition__optional__________"></span><span id="ELIFCONDITION__OPTIONAL__________"></span>*elifCondition* \[optional\]</span></span> <br/> | <span data-ttu-id="e9991-119">Другое условие для вычисления.</span><span class="sxs-lookup"><span data-stu-id="e9991-119">Other condition to evaluate.</span></span> <span data-ttu-id="e9991-120">Если параметр *ифкондитион* и все предыдущие \# директивы elif равны нулю, и этот параметр принимает ненулевое значение, весь текст между этой \# директивой elif и следующим экземпляром \# \# директивы elif, else или \# endif сохраняется в записи преобразования; в противном случае последующий исходный код не сохраняется.</span><span class="sxs-lookup"><span data-stu-id="e9991-120">If the *ifCondition* parameter and all previous \#elif directives evaluate to zero, and this parameter evaluates to a nonzero value, all text between this \#elif directive and the next instance of the \#elif, \#else, or \#endif directive is retained in the translation unit; otherwise, the subsequent source code is not retained.</span></span> <br/> <span data-ttu-id="e9991-121">Условие может использовать оператор препроцессора, определенный для определения, определена ли конкретная константа препроцессора или макрос. Это использование эквивалентно использованию директивы [ \# ifdef](dx-graphics-hlsl-appendix-pre-ifdef.md) .</span><span class="sxs-lookup"><span data-stu-id="e9991-121">The condition can use the preprocessor operator defined to determine whether a specific preprocessor constant or macro is defined; this usage is equivalent to the use of the [\#ifdef](dx-graphics-hlsl-appendix-pre-ifdef.md) directive.</span></span> <br/> <span data-ttu-id="e9991-122">Ограничения на значение параметра *елифкондитион* см. в разделе "Примечания".</span><span class="sxs-lookup"><span data-stu-id="e9991-122">See the Remarks section for restrictions on the value of the *elifCondition* parameter.</span></span> <br/> |



 

## <a name="remarks"></a><span data-ttu-id="e9991-123">Примечания</span><span class="sxs-lookup"><span data-stu-id="e9991-123">Remarks</span></span>

<span data-ttu-id="e9991-124">Каждая \# директива if в исходном файле должна соответствовать закрываемой \# директиве endif.</span><span class="sxs-lookup"><span data-stu-id="e9991-124">Each \#if directive in a source file must be matched by a closing \#endif directive.</span></span> <span data-ttu-id="e9991-125">\#Между директивами if и endif может использоваться любое число директивов elif \# \# , но \# допускается не более одной директивы else.</span><span class="sxs-lookup"><span data-stu-id="e9991-125">Any number of \#elif directives can appear between the \#if and \#endif directives, but at most one \#else directive is allowed.</span></span> <span data-ttu-id="e9991-126">\#Директива Else, если она есть, должна быть последней директивой перед \# endif.</span><span class="sxs-lookup"><span data-stu-id="e9991-126">The \#else directive, if present, must be the last directive before \#endif.</span></span> <span data-ttu-id="e9991-127">Директивы условной компиляции, содержащиеся в включаемых файлах, должны соответствовать тем же условиям.</span><span class="sxs-lookup"><span data-stu-id="e9991-127">Conditional-compilation directives contained in include files must satisfy the same conditions.</span></span>

<span data-ttu-id="e9991-128">\# \# Директивы if, elif, \# else и \# endif могут быть вложены в текстовые части других \# директив if.</span><span class="sxs-lookup"><span data-stu-id="e9991-128">The \#if, \#elif, \#else, and \#endif directives can nest in the text portions of other \#if directives.</span></span> <span data-ttu-id="e9991-129">Каждая вложенная \# \# директива Else, elif или \# endif принадлежит ближайшей предшествующей \# директиве if.</span><span class="sxs-lookup"><span data-stu-id="e9991-129">Each nested \#else, \#elif, or \#endif directive belongs to the closest preceding \#if directive.</span></span>

<span data-ttu-id="e9991-130">Если ни одно из условий не имеет ненулевого значения, препроцессор выбирает текстовый блок после \# директивы else.</span><span class="sxs-lookup"><span data-stu-id="e9991-130">If no conditions evaluate to a nonzero value, the preprocessor selects the text block after the \#else directive.</span></span> <span data-ttu-id="e9991-131">Если \# предложение else пропущено и ни одно из условий не имеет ненулевого значения, то текстовый блок не выбран.</span><span class="sxs-lookup"><span data-stu-id="e9991-131">If the \#else clause is omitted and no conditions evaluate to a nonzero value, no text block is selected.</span></span>

<span data-ttu-id="e9991-132">Параметры *ифкондитион* и *елифкондитион* в значительной степени соответствуют следующим требованиям.</span><span class="sxs-lookup"><span data-stu-id="e9991-132">The *ifCondition* and *elifCondition* parameters much meet the following requirements:</span></span>

-   <span data-ttu-id="e9991-133">Выражения условной компиляции обрабатываются как [**длинные значения со знаком**](https://msdn.microsoft.com/library/cc953fe1(v=VS.71).aspx) , и эти выражения оцениваются с использованием тех же правил, что и выражения в C++.</span><span class="sxs-lookup"><span data-stu-id="e9991-133">Conditional compilation expressions are treated as [**signed long**](https://msdn.microsoft.com/library/cc953fe1(v=VS.71).aspx) values, and these expressions are evaluated using the same rules as expressions in C++.</span></span>
-   <span data-ttu-id="e9991-134">Выражения должны иметь целочисленный тип и могут содержать только целочисленные константы, символьные константы и оператор defined.</span><span class="sxs-lookup"><span data-stu-id="e9991-134">Expressions must have integral type and can include only integer constants, character constants, and the defined operator.</span></span>
-   <span data-ttu-id="e9991-135">Выражения не могут использовать **sizeof** или оператор приведения типа.</span><span class="sxs-lookup"><span data-stu-id="e9991-135">Expressions cannot use **sizeof** or a type-cast operator.</span></span>
-   <span data-ttu-id="e9991-136">Целевая среда может быть не в состоянии представлять все диапазоны целых чисел.</span><span class="sxs-lookup"><span data-stu-id="e9991-136">The target environment may not be able to represent all ranges of integers.</span></span>
-   <span data-ttu-id="e9991-137">Преобразование представляет тип [**int**](/windows/desktop/WinProg/windows-data-types) , то же, что и тип **Long**, и [**Неподписанное целое**](https://msdn.microsoft.com/library/cc953fe1(v=VS.71).aspx) число без **знака Long**.</span><span class="sxs-lookup"><span data-stu-id="e9991-137">The translation represents type [**int**](/windows/desktop/WinProg/windows-data-types) the same as type **long**, and [**unsigned int**](https://msdn.microsoft.com/library/cc953fe1(v=VS.71).aspx) the same as **unsigned long**.</span></span>
-   <span data-ttu-id="e9991-138">Транслятор может преобразовывать символьные константы в набор кодовых значений, отличающийся от набора для целевой среды.</span><span class="sxs-lookup"><span data-stu-id="e9991-138">The translator can translate character constants to a set of code values different from the set for the target environment.</span></span> <span data-ttu-id="e9991-139">Для определения свойств целевой среды проверьте значения макросов из файла LIMITS.H в приложении, собранном для целевой среды.</span><span class="sxs-lookup"><span data-stu-id="e9991-139">To determine the properties of the target environment, check values of macros from LIMITS.H in an application built for the target environment.</span></span>
-   <span data-ttu-id="e9991-140">Выражение не должно выполнять никаких запросов среды и не должно зависеть от конкретной реализации на целевом компьютере.</span><span class="sxs-lookup"><span data-stu-id="e9991-140">The expression must not perform any environmental inquiries and must remain insulated from implementation details on the target computer.</span></span>

## <a name="examples"></a><span data-ttu-id="e9991-141">Примеры</span><span class="sxs-lookup"><span data-stu-id="e9991-141">Examples</span></span>

<span data-ttu-id="e9991-142">В этом разделе содержатся примеры, демонстрирующие использование директив препроцессора условной компиляции.</span><span class="sxs-lookup"><span data-stu-id="e9991-142">This section contains examples that demonstrate how to use conditional compilation preprocessor directives.</span></span>

### <a name="use-of-the-defined-operator"></a><span data-ttu-id="e9991-143">Использование определенного оператора</span><span class="sxs-lookup"><span data-stu-id="e9991-143">Use of the defined operator</span></span>

<span data-ttu-id="e9991-144">В следующем примере показано использование определенного оператора.</span><span class="sxs-lookup"><span data-stu-id="e9991-144">The following example shows the use of the defined operator.</span></span> <span data-ttu-id="e9991-145">Если определен кредит идентификатора, вызывается вызов функции **кредита** .</span><span class="sxs-lookup"><span data-stu-id="e9991-145">If the identifier CREDIT is defined, the call to the **credit** function is compiled.</span></span> <span data-ttu-id="e9991-146">Если определен ДЕБЕТ идентификатора, вызывается вызов функции **Debit** .</span><span class="sxs-lookup"><span data-stu-id="e9991-146">If the identifier DEBIT is defined, the call to the **debit** function is compiled.</span></span> <span data-ttu-id="e9991-147">Если ни один из идентификаторов не определен, вызывается вызов функции **принтеррор** .</span><span class="sxs-lookup"><span data-stu-id="e9991-147">If neither identifier is defined, the call to the **printerror** function is compiled.</span></span> <span data-ttu-id="e9991-148">Обратите внимание, что "Кредит" и "Кредит" — это уникальные идентификаторы в C и C++, так как их варианты различны.</span><span class="sxs-lookup"><span data-stu-id="e9991-148">Note that "CREDIT" and "credit" are distinct identifiers in C and C++ because their cases are different.</span></span>


```
#if defined(CREDIT)
    credit();
#elif defined(DEBIT)
    debit();
#else
    printerror();
#endif
```



### <a name="use-of-nested-if-directives"></a><span data-ttu-id="e9991-149">Использование вложенных \# директив if</span><span class="sxs-lookup"><span data-stu-id="e9991-149">Use of nested \#if directives</span></span>

<span data-ttu-id="e9991-150">В следующем примере показано, как вкладывать \# директивы if.</span><span class="sxs-lookup"><span data-stu-id="e9991-150">The following example shows how to nest \#if directives.</span></span> <span data-ttu-id="e9991-151">В этом примере предполагается, что символьная константа с именем ДЛЕВЕЛ была ранее определена.</span><span class="sxs-lookup"><span data-stu-id="e9991-151">This example assumes that a symbolic constant named DLEVEL has been previously defined.</span></span> <span data-ttu-id="e9991-152">\# \# Директивы elif и Else используются для выбора одного из четырех вариантов в зависимости от значения длевел.</span><span class="sxs-lookup"><span data-stu-id="e9991-152">The \#elif and \#else directives are used to make one of four choices, based on the value of DLEVEL.</span></span> <span data-ttu-id="e9991-153">В зависимости от определения ДЛЕВЕЛ в СТЕКе констант устанавливается значение 0, 100 или 200.</span><span class="sxs-lookup"><span data-stu-id="e9991-153">The constant STACK is set to 0, 100, or 200, depending on the definition of DLEVEL.</span></span> <span data-ttu-id="e9991-154">Если ДЛЕВЕЛ больше 5, то стек не определен.</span><span class="sxs-lookup"><span data-stu-id="e9991-154">If DLEVEL is greater than 5, then STACK is not defined.</span></span>


```
#if DLEVEL > 5
    #define SIGNAL  1
    #if STACKUSE == 1
        #define STACK   200
    #else
        #define STACK   100
    #endif
#else
    #define SIGNAL  0
    #if STACKUSE == 1
        #define STACK   100
    #else
        #define STACK   50
    #endif
#endif
#if DLEVEL == 0
    #define STACK 0
#elif DLEVEL == 1
    #define STACK 100
#elif DLEVEL > 5
    display( debugptr );
#else
    #define STACK 200
#endif
```



### <a name="use-for-including-header-files"></a><span data-ttu-id="e9991-155">Использовать для включения файлов заголовков</span><span class="sxs-lookup"><span data-stu-id="e9991-155">Use for including header files</span></span>

<span data-ttu-id="e9991-156">Условная компиляция обычно используется для предотвращения нескольких включений одного и того же файла заголовка.</span><span class="sxs-lookup"><span data-stu-id="e9991-156">A common use for conditional compilation is to prevent multiple inclusions of the same header file.</span></span> <span data-ttu-id="e9991-157">В C++, где классы часто определяются в файлах заголовков, конструкции условной компиляции можно использовать для предотвращения нескольких определений.</span><span class="sxs-lookup"><span data-stu-id="e9991-157">In C++, where classes are often defined in header files, conditional compilation constructs can be used to prevent multiple definitions.</span></span> <span data-ttu-id="e9991-158">В следующем примере определяется, определена ли символьная константа в примере \_ H.</span><span class="sxs-lookup"><span data-stu-id="e9991-158">The following example determines whether the symbolic constant EXAMPLE\_H is defined.</span></span> <span data-ttu-id="e9991-159">Если да, то файл уже включен и не нуждается в повторной обработке. в противном случае \_ для указания этого примера определяется константа H. H уже обработан.</span><span class="sxs-lookup"><span data-stu-id="e9991-159">If so, the file has already been included and does not need to be reprocessed; if not, the constant EXAMPLE\_H is defined to indicate that EXAMPLE.H has already been processed.</span></span>


```
#if !defined( EXAMPLE_H )
#define EXAMPLE_H

class Example
{
...
};

#endif // !defined( EXAMPLE_H )
```



## <a name="see-also"></a><span data-ttu-id="e9991-160">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="e9991-160">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e9991-161">Директивы препроцессора (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="e9991-161">Preprocessor Directives (DirectX HLSL)</span></span>](dx-graphics-hlsl-appendix-preprocessor.md)
</dt> </dl>

 

