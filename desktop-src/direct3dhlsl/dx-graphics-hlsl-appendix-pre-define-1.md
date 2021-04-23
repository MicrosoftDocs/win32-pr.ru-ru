---
title: '\#определение директивы (константа)'
description: Директива препроцессора, которая назначает понятное имя константе в приложении.
ms.assetid: cc9b34a3-4c83-4999-99ec-e6261ecb2785
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- apiref
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: deae1ca92c2280cd31cbec2bf3482c61fcf2b88a
ms.sourcegitcommit: cba7f424a292fd7f3a8518947b9466439b455419
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/23/2019
ms.locfileid: "104069392"
---
# <a name="define-directive-constant"></a><span data-ttu-id="7beac-103">\#определение директивы (константа)</span><span class="sxs-lookup"><span data-stu-id="7beac-103">\#define directive (constant)</span></span>

<span data-ttu-id="7beac-104">Директива препроцессора, которая назначает понятное имя константе в приложении.</span><span class="sxs-lookup"><span data-stu-id="7beac-104">Preprocessor directive that assigns a meaningful name to a constant in your application.</span></span>



| <span data-ttu-id="7beac-105">\#определение *идентифиертокен-String*</span><span class="sxs-lookup"><span data-stu-id="7beac-105">\#define *identifiertoken-string*</span></span> |
|-----------------------------------|



 

## <a name="parameters"></a><span data-ttu-id="7beac-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="7beac-106">Parameters</span></span>



| <span data-ttu-id="7beac-107">Элемент</span><span class="sxs-lookup"><span data-stu-id="7beac-107">Item</span></span>                                                                                                                       | <span data-ttu-id="7beac-108">Описание</span><span class="sxs-lookup"><span data-stu-id="7beac-108">Description</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                           |
|----------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="7beac-109"><span id="identifier"></span><span id="IDENTIFIER"></span>*Идентификатор*</span><span class="sxs-lookup"><span data-stu-id="7beac-109"><span id="identifier"></span><span id="IDENTIFIER"></span>*identifier*</span></span><br/>                                          | <span data-ttu-id="7beac-110">Идентификатор константы.</span><span class="sxs-lookup"><span data-stu-id="7beac-110">Identifier of the constant.</span></span> <br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                               |
| <span data-ttu-id="7beac-111"><span id="token-string__optional_"></span><span id="TOKEN-STRING__OPTIONAL_"></span>*строка* \[ токена используемых\]</span><span class="sxs-lookup"><span data-stu-id="7beac-111"><span id="token-string__optional_"></span><span id="TOKEN-STRING__OPTIONAL_"></span>*token-string* \[optional\]</span></span><br/> | <span data-ttu-id="7beac-112">Значение константы.</span><span class="sxs-lookup"><span data-stu-id="7beac-112">Value of the constant.</span></span> <span data-ttu-id="7beac-113">Этот параметр состоит из ряда токенов, таких как ключевые слова, константы или полные инструкции.</span><span class="sxs-lookup"><span data-stu-id="7beac-113">This parameter consists of a series of tokens, such as keywords, constants, or complete statements.</span></span> <span data-ttu-id="7beac-114">Один или несколько пробельных символов должны отделять этот параметр от параметра *идентификатора* . Этот пробел не считается частью подставляемого текста и не является пробелом после последнего маркера текста.</span><span class="sxs-lookup"><span data-stu-id="7beac-114">One or more white-space characters must separate this parameter from the *identifier* parameter; this white space is not considered part of the substituted text, nor is any white space following the last token of the text.</span></span> <br/> <span data-ttu-id="7beac-115">Если вы исключите этот параметр, все экземпляры параметра *идентификатора* удаляются из исходного файла.</span><span class="sxs-lookup"><span data-stu-id="7beac-115">If you exclude this parameter, all instances of the *identifier* parameter are removed from the source file.</span></span> <span data-ttu-id="7beac-116">Идентификатор остается определенным и может быть проверен с помощью директив [ \# If](dx-graphics-hlsl-appendix-pre-ifdef.md), \# ifdef и \# ifndef.</span><span class="sxs-lookup"><span data-stu-id="7beac-116">The identifier remains defined, and can be tested using the [\#if defined](dx-graphics-hlsl-appendix-pre-ifdef.md), \#ifdef, and \#ifndef directives.</span></span> <br/> |



 

## <a name="remarks"></a><span data-ttu-id="7beac-117">Примечания</span><span class="sxs-lookup"><span data-stu-id="7beac-117">Remarks</span></span>

<span data-ttu-id="7beac-118">Все экземпляры параметра *идентификатора* , которые выполняются после директивы [ \# define](dx-graphics-hlsl-appendix-pre-define.md) в исходном файле, будут заменены значением параметра *строки токена* .</span><span class="sxs-lookup"><span data-stu-id="7beac-118">All instances of the *identifier* parameter that occur after the [\#define](dx-graphics-hlsl-appendix-pre-define.md) directive in the source file will be replaced by the value of the *token-string* parameter.</span></span> <span data-ttu-id="7beac-119">Идентификатор заменяется только в том случае, если он формирует токен. Например, идентификатор не заменяется, если он присутствует в комментарии, в строке или в составе более длинного идентификатора.</span><span class="sxs-lookup"><span data-stu-id="7beac-119">The identifier is replaced only when it forms a token; for example, the identifier is not replaced if it appears in a comment, within a string, or as part of a longer identifier.</span></span>

<span data-ttu-id="7beac-120">Директива [ \# undef](dx-graphics-hlsl-appendix-pre-undef.md) указывает препроцессору на необходимость запоминать определение идентификатора; дополнительные сведения см. в разделе \# директива undef (DirectX HLSL).</span><span class="sxs-lookup"><span data-stu-id="7beac-120">The [\#undef](dx-graphics-hlsl-appendix-pre-undef.md) directive instructs the preprocessor to forget the definition of an identifier; for more information, see \#undef Directive (DirectX HLSL).</span></span>

<span data-ttu-id="7beac-121">Определение констант с помощью параметра компилятора/D действует так же, как и директива [ \# define](dx-graphics-hlsl-appendix-pre-define.md) в начале файла.</span><span class="sxs-lookup"><span data-stu-id="7beac-121">Defining constants with the /D compiler option has the same effect as using the [\#define](dx-graphics-hlsl-appendix-pre-define.md) directive at the beginning of your file.</span></span> <span data-ttu-id="7beac-122">С параметром/D можно определить до 30 констант.</span><span class="sxs-lookup"><span data-stu-id="7beac-122">Up to 30 constants can be defined with the /D option.</span></span> <span data-ttu-id="7beac-123">Пример того, как это можно использовать, см. в подразделе "примеры" файла [ \# ifdef и)](dx-graphics-hlsl-appendix-pre-ifdef.md).</span><span class="sxs-lookup"><span data-stu-id="7beac-123">For an example of how this can be used, see the Examples section of [\#ifdef and )](dx-graphics-hlsl-appendix-pre-ifdef.md).</span></span>

## <a name="examples"></a><span data-ttu-id="7beac-124">Примеры</span><span class="sxs-lookup"><span data-stu-id="7beac-124">Examples</span></span>

<span data-ttu-id="7beac-125">В следующем примере определяется ширина идентификатора в виде целочисленной константы 80, а затем определяется длина с точки зрения ширины и целочисленной константы 10.</span><span class="sxs-lookup"><span data-stu-id="7beac-125">The following example defines the identifier WIDTH as the integer constant 80 and then defines LENGTH in terms of WIDTH and the integer constant 10.</span></span>


```
#define WIDTH       80
#define LENGTH      ( WIDTH + 10 )
```



<span data-ttu-id="7beac-126">Каждый последующий экземпляр LENGTH заменяется на (WIDTH + 10), а каждый последующий экземпляр WIDTH + 10 заменяется выражением (80 + 10).</span><span class="sxs-lookup"><span data-stu-id="7beac-126">Every subsequent instance of LENGTH is replaced by (WIDTH + 10), and every subsequent instance of WIDTH + 10 is replaced by the expression (80 + 10).</span></span> <span data-ttu-id="7beac-127">Круглые скобки вокруг WIDTH + 10 важны, так как они управляют интерпретацией в инструкциях, таких как следующие.</span><span class="sxs-lookup"><span data-stu-id="7beac-127">The parentheses around WIDTH + 10 are important because they control the interpretation in statements such as the following.</span></span>


```
var = LENGTH * 20;
```



<span data-ttu-id="7beac-128">После этапа предварительной обработки инструкция примет следующий вид, результатом которого является 1 800.</span><span class="sxs-lookup"><span data-stu-id="7beac-128">After the preprocessing stage the statement becomes the following, which evaluates to 1,800.</span></span>


```
var = ( 80 + 10 ) * 20;
```



<span data-ttu-id="7beac-129">Без скобок результат будет следующим: 280.</span><span class="sxs-lookup"><span data-stu-id="7beac-129">Without parentheses, the result would be the following, which evaluates to 280.</span></span>


```
var = 80 + 10 * 20;
```



## <a name="related-topics"></a><span data-ttu-id="7beac-130">См. также</span><span class="sxs-lookup"><span data-stu-id="7beac-130">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="7beac-131">Директивы препроцессора (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="7beac-131">Preprocessor Directives (DirectX HLSL)</span></span>](dx-graphics-hlsl-appendix-preprocessor.md)
</dt> <dt>

[<span data-ttu-id="7beac-132">\#определить перегрузки</span><span class="sxs-lookup"><span data-stu-id="7beac-132">\#define Overloads</span></span>](dx-graphics-hlsl-appendix-pre-define.md)
</dt> <dt>

[<span data-ttu-id="7beac-133">\#Директива undef (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="7beac-133">\#undef Directive (DirectX HLSL)</span></span>](dx-graphics-hlsl-appendix-pre-undef.md)
</dt> </dl>

 

 





