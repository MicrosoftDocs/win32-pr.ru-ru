---
title: '\#Директива define (макрос)'
description: Директива препроцессора, которая создает макрос, подобный функции.
ms.assetid: 73c19cf8-fbc5-444b-a51f-dc9f881f397b
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- apiref
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: d0c54c0c433c91522c8a72c5955a419eb72f9eee
ms.sourcegitcommit: cb87082135319cbdc5df541e3071eebb83a58972
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/04/2021
ms.locfileid: "111387520"
---
# <a name="define-directive-macro"></a><span data-ttu-id="ac6d3-103">\#Директива define (макрос)</span><span class="sxs-lookup"><span data-stu-id="ac6d3-103">\#define directive (macro)</span></span>

<span data-ttu-id="ac6d3-104">Директива препроцессора, которая создает макрос, подобный функции.</span><span class="sxs-lookup"><span data-stu-id="ac6d3-104">Preprocessor directive that creates a function-like macro.</span></span>



| <span data-ttu-id="ac6d3-105">\#определение *идентификатора*( *argument0*,..., *аргументн-1* ) *Строка токена*</span><span class="sxs-lookup"><span data-stu-id="ac6d3-105">\#define *identifier*( *argument0*, ... , *argumentN-1* ) *token-string*</span></span> |
|--------------------------------------------------------------------------|



 

## <a name="parameters"></a><span data-ttu-id="ac6d3-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="ac6d3-106">Parameters</span></span>



| <span data-ttu-id="ac6d3-107">Элемент</span><span class="sxs-lookup"><span data-stu-id="ac6d3-107">Item</span></span>                                                                                                                                                                                                                                                          | <span data-ttu-id="ac6d3-108">Описание</span><span class="sxs-lookup"><span data-stu-id="ac6d3-108">Description</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                             |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="ac6d3-109"><span id="identifier"></span><span id="IDENTIFIER"></span>*Идентификатор*</span><span class="sxs-lookup"><span data-stu-id="ac6d3-109"><span id="identifier"></span><span id="IDENTIFIER"></span>*identifier*</span></span><br/>                                                                                                                                                                             | <span data-ttu-id="ac6d3-110">Идентификатор макроса.</span><span class="sxs-lookup"><span data-stu-id="ac6d3-110">Identifier of the macro.</span></span> <br/> <span data-ttu-id="ac6d3-111">Второе [ \# Определение](dx-graphics-hlsl-appendix-pre-define.md) для макроса с идентификатором, который уже существует в текущем контексте, вызывает ошибку, если вторая последовательность токенов не совпадает с первой.</span><span class="sxs-lookup"><span data-stu-id="ac6d3-111">A second [\#define](dx-graphics-hlsl-appendix-pre-define.md) for a macro with an identifier that already exists in the current context generates an error unless the second token sequence is identical to the first.</span></span> <br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                 |
| <span data-ttu-id="ac6d3-112"><span id="___________argument0___...___argumentN-1_________"></span><span id="___________argument0___...___argumentn-1_________"></span><span id="___________ARGUMENT0___...___ARGUMENTN-1_________"></span> ( *argument0*,..., *аргументн-1* )</span><span class="sxs-lookup"><span data-stu-id="ac6d3-112"><span id="___________argument0___...___argumentN-1_________"></span><span id="___________argument0___...___argumentn-1_________"></span><span id="___________ARGUMENT0___...___ARGUMENTN-1_________"></span> ( *argument0*, ... , *argumentN-1* )</span></span> <br/> | <span data-ttu-id="ac6d3-113">Список аргументов макроса.</span><span class="sxs-lookup"><span data-stu-id="ac6d3-113">List of arguments to the macro.</span></span> <span data-ttu-id="ac6d3-114">Список аргументов с разделителями-запятыми, может иметь любую длину и должен быть заключен в круглые скобки.</span><span class="sxs-lookup"><span data-stu-id="ac6d3-114">The argument list is comma-delimited, can be of any length, and must be enclosed in parentheses.</span></span> <span data-ttu-id="ac6d3-115">Каждое имя аргумента в списке должно быть уникальным.</span><span class="sxs-lookup"><span data-stu-id="ac6d3-115">Each argument name in the list must be unique.</span></span> <span data-ttu-id="ac6d3-116">Ни один пробел не может разделять параметр *идентификатора* и открывающую круглую скобку.</span><span class="sxs-lookup"><span data-stu-id="ac6d3-116">No white space can separate the *identifier* parameter and the opening parenthesis.</span></span> <br/> <span data-ttu-id="ac6d3-117">Использовать объединение строк поместите обратную косую черту ( \\ ) непосредственно перед символом новой строки, чтобы разделить длинные директивы на несколько исходных строк.</span><span class="sxs-lookup"><span data-stu-id="ac6d3-117">Use line concatenation place a backslash (\\) immediately before the newline character to split long directives onto multiple source lines.</span></span> <br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                 |
| <span data-ttu-id="ac6d3-118"><span id="token-string__optional________"></span><span id="TOKEN-STRING__OPTIONAL________"></span>*строка* \[ токена используемых\]</span><span class="sxs-lookup"><span data-stu-id="ac6d3-118"><span id="token-string__optional________"></span><span id="TOKEN-STRING__OPTIONAL________"></span>*token-string* \[optional\]</span></span> <br/>                                                                                                                     | <span data-ttu-id="ac6d3-119">Значение макроса.</span><span class="sxs-lookup"><span data-stu-id="ac6d3-119">Value of the macro.</span></span> <span data-ttu-id="ac6d3-120">Этот параметр состоит из ряда токенов, таких как ключевые слова, константы или полные инструкции.</span><span class="sxs-lookup"><span data-stu-id="ac6d3-120">This parameter consists of a series of tokens, such as keywords, constants, or complete statements.</span></span> <span data-ttu-id="ac6d3-121">Один или несколько пробельных символов должны отделять этот параметр от параметра *идентификатора* . Этот пробел не считается частью подставляемого текста и не является пробелом после последнего маркера текста.</span><span class="sxs-lookup"><span data-stu-id="ac6d3-121">One or more white-space characters must separate this parameter from the *identifier* parameter; this white space is not considered part of the substituted text, nor is any white space following the last token of the text.</span></span> <span data-ttu-id="ac6d3-122">Используйте круглые скобки, чтобы убедиться, что сложные аргументы правильно интерпретированы.</span><span class="sxs-lookup"><span data-stu-id="ac6d3-122">Make liberal use of parentheses to ensure that complicated arguments are interpreted correctly.</span></span> <br/> <span data-ttu-id="ac6d3-123">Если значение параметра *идентификатора* встречается в параметре *строки токена* (даже в результате другого расширения макроса), оно не разворачивается.</span><span class="sxs-lookup"><span data-stu-id="ac6d3-123">If the value of the *identifier* parameter occurs within the *token-string* parameter (even as a result of another macro expansion), it is not expanded.</span></span> <br/> <span data-ttu-id="ac6d3-124">Если вы исключите этот параметр, все экземпляры параметра *идентификатора* удаляются из исходного файла.</span><span class="sxs-lookup"><span data-stu-id="ac6d3-124">If you exclude this parameter, all instances of the *identifier* parameter are removed from the source file.</span></span> <span data-ttu-id="ac6d3-125">Идентификатор остается определенным и может быть проверен с помощью директив [ \# If](dx-graphics-hlsl-appendix-pre-ifdef.md), \# ifdef и \# ifndef.</span><span class="sxs-lookup"><span data-stu-id="ac6d3-125">The identifier remains defined, and can be tested using the [\#if defined](dx-graphics-hlsl-appendix-pre-ifdef.md), \#ifdef, and \#ifndef directives.</span></span> <br/> |



 

## <a name="remarks"></a><span data-ttu-id="ac6d3-126">Remarks</span><span class="sxs-lookup"><span data-stu-id="ac6d3-126">Remarks</span></span>

<span data-ttu-id="ac6d3-127">Все экземпляры параметра *идентификатора* , происходящие после директивы [ \# define](dx-graphics-hlsl-appendix-pre-define.md) в исходном файле, составляют вызов макроса, а идентификатор будет заменен версией параметра *строки токена* , которая содержит фактические аргументы, заменяющие формальные параметры.</span><span class="sxs-lookup"><span data-stu-id="ac6d3-127">All instances of the *identifier* parameter that occur after the [\#define](dx-graphics-hlsl-appendix-pre-define.md) directive in the source file constitute a macro call, and the identifier will be replaced by a version of the *token-string* parameter that has actual arguments substituted for formal parameters.</span></span> <span data-ttu-id="ac6d3-128">Число параметров в вызове должно соответствовать числу параметров в определении макроса.</span><span class="sxs-lookup"><span data-stu-id="ac6d3-128">The number of parameters in the call must match the number of parameters in the macro definition.</span></span> <span data-ttu-id="ac6d3-129">Идентификатор заменяется только в том случае, если он формирует токен. Например, идентификатор не заменяется, если он присутствует в комментарии, в строке или в составе более длинного идентификатора.</span><span class="sxs-lookup"><span data-stu-id="ac6d3-129">The identifier is replaced only when it forms a token; for example, the identifier is not replaced if it appears in a comment, within a string, or as part of a longer identifier.</span></span>

<span data-ttu-id="ac6d3-130">Директива [ \# undef](dx-graphics-hlsl-appendix-pre-undef.md) указывает препроцессору на необходимость запоминать определение идентификатора; дополнительные сведения см. в разделе \# директива undef (DirectX HLSL).</span><span class="sxs-lookup"><span data-stu-id="ac6d3-130">The [\#undef](dx-graphics-hlsl-appendix-pre-undef.md) directive instructs the preprocessor to forget the definition of an identifier; for more information, see \#undef Directive (DirectX HLSL).</span></span>

<span data-ttu-id="ac6d3-131">Определение констант с помощью параметра компилятора/D действует так же, как и директива [ \# define](dx-graphics-hlsl-appendix-pre-define.md) в начале файла.</span><span class="sxs-lookup"><span data-stu-id="ac6d3-131">Defining constants with the /D compiler option has the same effect as using the [\#define](dx-graphics-hlsl-appendix-pre-define.md) directive at the beginning of your file.</span></span> <span data-ttu-id="ac6d3-132">С параметром/D можно определить до 30 макросов.</span><span class="sxs-lookup"><span data-stu-id="ac6d3-132">Up to 30 macros can be defined with the /D option.</span></span>

<span data-ttu-id="ac6d3-133">Фактические аргументы в вызове макроса сопоставляются с соответствующими формальными аргументами в определении макроса.</span><span class="sxs-lookup"><span data-stu-id="ac6d3-133">The actual arguments in the macro call are matched to the corresponding formal arguments in the macro definition.</span></span> <span data-ttu-id="ac6d3-134">Каждый формальный аргумент в строке токена заменяется соответствующим фактическим аргументом, если только аргумент не предшествует \# оператору строковый (), преобразования ( \# @) или Token-вставляя ( \# \# ), или за ним следует \# \# оператор.</span><span class="sxs-lookup"><span data-stu-id="ac6d3-134">Each formal argument in the token string is replaced by the corresponding actual argument, unless the argument is preceded by a stringizing (\#), charizing (\#@), or token-pasting (\#\#) operator, or is followed by a \#\# operator.</span></span> <span data-ttu-id="ac6d3-135">Перед заменой директивой формального параметра все макросы в фактическом аргументе разворачиваются.</span><span class="sxs-lookup"><span data-stu-id="ac6d3-135">Any macros in the actual argument are expanded before the directive replaces the formal parameter.</span></span>

<span data-ttu-id="ac6d3-136">Маркер, вставленный в компилятор HLSL, немного отличается от токена, вставленного в компиляторе C, в том, что вставленные маркеры должны быть действительными самими маркерами.</span><span class="sxs-lookup"><span data-stu-id="ac6d3-136">Token pasting in the HLSL compiler is slightly different from token pasting in the C compiler, in that the pasted tokens must be valid tokens on their own.</span></span> <span data-ttu-id="ac6d3-137">Например, рассмотрим следующее определение макроса:</span><span class="sxs-lookup"><span data-stu-id="ac6d3-137">For example, consider the following macro definition:</span></span>


```
#define MERGE(a, b) a##b
MERGE(float, 4x4) test;
```



<span data-ttu-id="ac6d3-138">В компиляторе C происходит следующее:</span><span class="sxs-lookup"><span data-stu-id="ac6d3-138">In the C compiler, this results in the following:</span></span>


```
float4x4 test
```



<span data-ttu-id="ac6d3-139">Однако в компиляторе HLSL это приводит к следующим результатам:</span><span class="sxs-lookup"><span data-stu-id="ac6d3-139">In the HLSL compiler however, this results in the following:</span></span>


```
float4 x4 test
```



<span data-ttu-id="ac6d3-140">Это поведение можно обойти, используя следующее определение макроса.</span><span class="sxs-lookup"><span data-stu-id="ac6d3-140">You can work around this behavior by using the following macro definition instead.</span></span>


```
MERGE(MERGE(float, 4), x4) test;
```



## <a name="examples"></a><span data-ttu-id="ac6d3-141">Примеры</span><span class="sxs-lookup"><span data-stu-id="ac6d3-141">Examples</span></span>

<span data-ttu-id="ac6d3-142">В следующем примере для определения линий курсора используется макрос.</span><span class="sxs-lookup"><span data-stu-id="ac6d3-142">The following example uses a macro to define cursor lines.</span></span>


```
#define CURSOR(top, bottom) (((top) << 8) | (bottom))
```



<span data-ttu-id="ac6d3-143">В следующем примере определяется макрос, который получает целое число псевдослучайное в указанном диапазоне.</span><span class="sxs-lookup"><span data-stu-id="ac6d3-143">The following example defines a macro that retrieves a pseudorandom integer in the specified range.</span></span>


```
#define getrandom(min, max) \
((rand()%(int)(((max) + 1)-(min)))+ (min))
```



## <a name="related-topics"></a><span data-ttu-id="ac6d3-144">Связанные темы</span><span class="sxs-lookup"><span data-stu-id="ac6d3-144">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="ac6d3-145">Директивы препроцессора (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="ac6d3-145">Preprocessor Directives (DirectX HLSL)</span></span>](dx-graphics-hlsl-appendix-preprocessor.md)
</dt> <dt>

[<span data-ttu-id="ac6d3-146">\#определить перегрузки</span><span class="sxs-lookup"><span data-stu-id="ac6d3-146">\#define Overloads</span></span>](dx-graphics-hlsl-appendix-pre-define.md)
</dt> <dt>

[<span data-ttu-id="ac6d3-147">\#Директива undef (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="ac6d3-147">\#undef Directive (DirectX HLSL)</span></span>](dx-graphics-hlsl-appendix-pre-undef.md)
</dt> </dl>

 

 





