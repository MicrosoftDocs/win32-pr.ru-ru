---
title: Директивы препроцессора (HLSL)
description: Директивы препроцессора, такие как \ define и \ ifdef, обычно используются для упрощения изменения и компиляции исходных программ в разных средах выполнения.
ms.assetid: b5164c0e-62ab-4da5-9c22-efb5e6319bd6
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- apiref
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 0f2d9e51926d2a1b7bf374653becec4fe3de3daa
ms.sourcegitcommit: 8fa6614b715bddf14648cce36d2df22e5232801a
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/10/2020
ms.locfileid: "103800574"
---
# <a name="preprocessor-directives-hlsl"></a><span data-ttu-id="aa015-103">Директивы препроцессора (HLSL)</span><span class="sxs-lookup"><span data-stu-id="aa015-103">Preprocessor Directives (HLSL)</span></span>

<span data-ttu-id="aa015-104">Директивы препроцессора, такие как [ \# define](dx-graphics-hlsl-appendix-pre-define.md) и [ \# ifdef](dx-graphics-hlsl-appendix-pre-ifdef.md), обычно используются для упрощения изменения и компиляции исходных программ в разных средах выполнения.</span><span class="sxs-lookup"><span data-stu-id="aa015-104">Preprocessor directives, such as [\#define](dx-graphics-hlsl-appendix-pre-define.md) and [\#ifdef](dx-graphics-hlsl-appendix-pre-ifdef.md), are typically used to make source programs easy to change and easy to compile in different execution environments.</span></span> <span data-ttu-id="aa015-105">Директивы в файле исходного кода позволяют препроцессору выполнять определенные действия.</span><span class="sxs-lookup"><span data-stu-id="aa015-105">Directives in the source file tell the preprocessor to perform specific actions.</span></span> <span data-ttu-id="aa015-106">Например, препроцессор может заменять токены в тексте, вставлять содержимое других файлов в файл исходного кода или отключать компиляцию части файла путем удаления разделов текста.</span><span class="sxs-lookup"><span data-stu-id="aa015-106">For example, the preprocessor can replace tokens in the text, insert the contents of other files into the source file, or suppress compilation of part of the file by removing sections of text.</span></span> <span data-ttu-id="aa015-107">Строки препроцессора распознаются и выполняются до расширения макросов.</span><span class="sxs-lookup"><span data-stu-id="aa015-107">Preprocessor lines are recognized and carried out before macro expansion.</span></span> <span data-ttu-id="aa015-108">Поэтому если макрос разворачивается в нечто, похожее на команду препроцессора, эта команда не распознается препроцессором.</span><span class="sxs-lookup"><span data-stu-id="aa015-108">Therefore, if a macro expands into something that looks like a preprocessor command, that command is not recognized by the preprocessor.</span></span>

<span data-ttu-id="aa015-109">В операторах препроцессора используется тот же набор символов, что и в операторах файла исходного кода, но escape-последовательности не поддерживаются.</span><span class="sxs-lookup"><span data-stu-id="aa015-109">Preprocessor statements use the same character set as source file statements, with the exception that escape sequences are not supported.</span></span> <span data-ttu-id="aa015-110">Набор символов в операторах препроцессора совпадает с кодировкой выполнения.</span><span class="sxs-lookup"><span data-stu-id="aa015-110">The character set used in preprocessor statements is the same as the execution character set.</span></span> <span data-ttu-id="aa015-111">Препроцессор также распознает отрицательные значения символов.</span><span class="sxs-lookup"><span data-stu-id="aa015-111">The preprocessor also recognizes negative character values.</span></span>

<span data-ttu-id="aa015-112">Препроцессор HLSL распознает следующие директивы:</span><span class="sxs-lookup"><span data-stu-id="aa015-112">The HLSL preprocessor recognizes the following directives:</span></span>

-   [<span data-ttu-id="aa015-113">\#define</span><span class="sxs-lookup"><span data-stu-id="aa015-113">\#define</span></span>](dx-graphics-hlsl-appendix-pre-define.md)
-   [<span data-ttu-id="aa015-114">\##elif</span><span class="sxs-lookup"><span data-stu-id="aa015-114">\#elif</span></span>](dx-graphics-hlsl-appendix-pre-if.md)
-   [<span data-ttu-id="aa015-115">\#else</span><span class="sxs-lookup"><span data-stu-id="aa015-115">\#else</span></span>](dx-graphics-hlsl-appendix-pre-if.md)
-   [<span data-ttu-id="aa015-116">\#endif</span><span class="sxs-lookup"><span data-stu-id="aa015-116">\#endif</span></span>](dx-graphics-hlsl-appendix-pre-if.md)
-   [<span data-ttu-id="aa015-117">\#план</span><span class="sxs-lookup"><span data-stu-id="aa015-117">\#error</span></span>](dx-graphics-hlsl-appendix-pre-error.md)
-   [<span data-ttu-id="aa015-118">\#наличии</span><span class="sxs-lookup"><span data-stu-id="aa015-118">\#if</span></span>](dx-graphics-hlsl-appendix-pre-if.md)
-   [<span data-ttu-id="aa015-119">\#ifdef</span><span class="sxs-lookup"><span data-stu-id="aa015-119">\#ifdef</span></span>](dx-graphics-hlsl-appendix-pre-ifdef.md)
-   [<span data-ttu-id="aa015-120">\#ifndef</span><span class="sxs-lookup"><span data-stu-id="aa015-120">\#ifndef</span></span>](dx-graphics-hlsl-appendix-pre-ifdef.md)
-   [<span data-ttu-id="aa015-121">\#относится</span><span class="sxs-lookup"><span data-stu-id="aa015-121">\#include</span></span>](dx-graphics-hlsl-appendix-pre-include.md)
-   [<span data-ttu-id="aa015-122">\#штрих</span><span class="sxs-lookup"><span data-stu-id="aa015-122">\#line</span></span>](dx-graphics-hlsl-appendix-pre-line.md)
-   [<span data-ttu-id="aa015-123">\#pragma</span><span class="sxs-lookup"><span data-stu-id="aa015-123">\#pragma</span></span>](dx-graphics-hlsl-appendix-pre-pragma.md)
-   [<span data-ttu-id="aa015-124">\#undef</span><span class="sxs-lookup"><span data-stu-id="aa015-124">\#undef</span></span>](dx-graphics-hlsl-appendix-pre-undef.md)

<span data-ttu-id="aa015-125">Знак решетки ( \# ) должен быть первым символом, не пробелом, в строке, содержащей директиву; символы пробела могут находиться между знаком номера и первой буквой директивы.</span><span class="sxs-lookup"><span data-stu-id="aa015-125">The number sign (\#) must be the first nonwhite-space character on the line containing the directive; white-space characters can appear between the number sign and the first letter of the directive.</span></span> <span data-ttu-id="aa015-126">Некоторые директивы содержат аргументы или значения.</span><span class="sxs-lookup"><span data-stu-id="aa015-126">Some directives include arguments or values.</span></span> <span data-ttu-id="aa015-127">Любой текст, следующий за директивой (за исключением аргумента или значения, который является частью директивы), должен предшествовать разделителю однострочных комментариев (//) или заключены в разделители комментариев (/ \* \* /).</span><span class="sxs-lookup"><span data-stu-id="aa015-127">Any text that follows a directive (except an argument or value that is part of the directive) must be preceded by the single-line comment delimiter (//) or enclosed in comment delimiters (/\* \*/).</span></span> <span data-ttu-id="aa015-128">Строки, содержащие директивы препроцессора, могут быть продолжены непосредственно перед маркером конца строки с обратной косой чертой ( \) .</span><span class="sxs-lookup"><span data-stu-id="aa015-128">Lines containing preprocessor directives can be continued by immediately preceding the end-of-line marker with a backslash (\).</span></span>

<span data-ttu-id="aa015-129">Директивы препроцессора могут находиться в любом месте файла исходного кода, но применяются только к оставшейся части файла.</span><span class="sxs-lookup"><span data-stu-id="aa015-129">Preprocessor directives can appear anywhere in a source file, but they apply only to the remainder of the source file.</span></span>

## <a name="related-topics"></a><span data-ttu-id="aa015-130">См. также</span><span class="sxs-lookup"><span data-stu-id="aa015-130">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="aa015-131">Приложение (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="aa015-131">Appendix (DirectX HLSL)</span></span>](dx-graphics-hlsl-appendix.md)
</dt> </dl>

 

 




