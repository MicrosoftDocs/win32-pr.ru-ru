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
ms.openlocfilehash: 8efdd996ddeb58c09d1c8250f174c21bb939f082
ms.sourcegitcommit: cb87082135319cbdc5df541e3071eebb83a58972
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/04/2021
ms.locfileid: "111386833"
---
# <a name="preprocessor-directives-hlsl"></a><span data-ttu-id="a5715-103">Директивы препроцессора (HLSL)</span><span class="sxs-lookup"><span data-stu-id="a5715-103">Preprocessor Directives (HLSL)</span></span>

<span data-ttu-id="a5715-104">Директивы препроцессора, такие как [ \# define](dx-graphics-hlsl-appendix-pre-define.md) и [ \# ifdef](dx-graphics-hlsl-appendix-pre-ifdef.md), обычно используются для упрощения изменения и компиляции исходных программ в разных средах выполнения.</span><span class="sxs-lookup"><span data-stu-id="a5715-104">Preprocessor directives, such as [\#define](dx-graphics-hlsl-appendix-pre-define.md) and [\#ifdef](dx-graphics-hlsl-appendix-pre-ifdef.md), are typically used to make source programs easy to change and easy to compile in different execution environments.</span></span> <span data-ttu-id="a5715-105">Директивы в файле исходного кода позволяют препроцессору выполнять определенные действия.</span><span class="sxs-lookup"><span data-stu-id="a5715-105">Directives in the source file tell the preprocessor to perform specific actions.</span></span> <span data-ttu-id="a5715-106">Например, препроцессор может заменять токены в тексте, вставлять содержимое других файлов в файл исходного кода или отключать компиляцию части файла путем удаления разделов текста.</span><span class="sxs-lookup"><span data-stu-id="a5715-106">For example, the preprocessor can replace tokens in the text, insert the contents of other files into the source file, or suppress compilation of part of the file by removing sections of text.</span></span> <span data-ttu-id="a5715-107">Строки препроцессора распознаются и выполняются до расширения макросов.</span><span class="sxs-lookup"><span data-stu-id="a5715-107">Preprocessor lines are recognized and carried out before macro expansion.</span></span> <span data-ttu-id="a5715-108">Поэтому если макрос разворачивается в нечто, похожее на команду препроцессора, эта команда не распознается препроцессором.</span><span class="sxs-lookup"><span data-stu-id="a5715-108">Therefore, if a macro expands into something that looks like a preprocessor command, that command is not recognized by the preprocessor.</span></span>

<span data-ttu-id="a5715-109">В операторах препроцессора используется тот же набор символов, что и в операторах файла исходного кода, но escape-последовательности не поддерживаются.</span><span class="sxs-lookup"><span data-stu-id="a5715-109">Preprocessor statements use the same character set as source file statements, with the exception that escape sequences are not supported.</span></span> <span data-ttu-id="a5715-110">Набор символов в операторах препроцессора совпадает с кодировкой выполнения.</span><span class="sxs-lookup"><span data-stu-id="a5715-110">The character set used in preprocessor statements is the same as the execution character set.</span></span> <span data-ttu-id="a5715-111">Препроцессор также распознает отрицательные значения символов.</span><span class="sxs-lookup"><span data-stu-id="a5715-111">The preprocessor also recognizes negative character values.</span></span>

<span data-ttu-id="a5715-112">Препроцессор HLSL распознает следующие директивы:</span><span class="sxs-lookup"><span data-stu-id="a5715-112">The HLSL preprocessor recognizes the following directives:</span></span>

-   [<span data-ttu-id="a5715-113">\#определенно</span><span class="sxs-lookup"><span data-stu-id="a5715-113">\#define</span></span>](dx-graphics-hlsl-appendix-pre-define.md)
-   [<span data-ttu-id="a5715-114">\##elif</span><span class="sxs-lookup"><span data-stu-id="a5715-114">\#elif</span></span>](dx-graphics-hlsl-appendix-pre-if.md)
-   [<span data-ttu-id="a5715-115">\#Кроме</span><span class="sxs-lookup"><span data-stu-id="a5715-115">\#else</span></span>](dx-graphics-hlsl-appendix-pre-if.md)
-   [<span data-ttu-id="a5715-116">\#endif</span><span class="sxs-lookup"><span data-stu-id="a5715-116">\#endif</span></span>](dx-graphics-hlsl-appendix-pre-if.md)
-   [<span data-ttu-id="a5715-117">\#план</span><span class="sxs-lookup"><span data-stu-id="a5715-117">\#error</span></span>](dx-graphics-hlsl-appendix-pre-error.md)
-   [<span data-ttu-id="a5715-118">\#if</span><span class="sxs-lookup"><span data-stu-id="a5715-118">\#if</span></span>](dx-graphics-hlsl-appendix-pre-if.md)
-   [<span data-ttu-id="a5715-119">\#ifdef</span><span class="sxs-lookup"><span data-stu-id="a5715-119">\#ifdef</span></span>](dx-graphics-hlsl-appendix-pre-ifdef.md)
-   [<span data-ttu-id="a5715-120">\#ifndef</span><span class="sxs-lookup"><span data-stu-id="a5715-120">\#ifndef</span></span>](dx-graphics-hlsl-appendix-pre-ifdef.md)
-   [<span data-ttu-id="a5715-121">\#относится</span><span class="sxs-lookup"><span data-stu-id="a5715-121">\#include</span></span>](dx-graphics-hlsl-appendix-pre-include.md)
-   [<span data-ttu-id="a5715-122">\#line</span><span class="sxs-lookup"><span data-stu-id="a5715-122">\#line</span></span>](dx-graphics-hlsl-appendix-pre-line.md)
-   [<span data-ttu-id="a5715-123">\#включают</span><span class="sxs-lookup"><span data-stu-id="a5715-123">\#pragma</span></span>](dx-graphics-hlsl-appendix-pre-pragma.md)
-   [<span data-ttu-id="a5715-124">\#undef</span><span class="sxs-lookup"><span data-stu-id="a5715-124">\#undef</span></span>](dx-graphics-hlsl-appendix-pre-undef.md)

<span data-ttu-id="a5715-125">Знак решетки ( \# ) должен быть первым символом, не пробелом, в строке, содержащей директиву; символы пробела могут находиться между знаком номера и первой буквой директивы.</span><span class="sxs-lookup"><span data-stu-id="a5715-125">The number sign (\#) must be the first nonwhite-space character on the line containing the directive; white-space characters can appear between the number sign and the first letter of the directive.</span></span> <span data-ttu-id="a5715-126">Некоторые директивы содержат аргументы или значения.</span><span class="sxs-lookup"><span data-stu-id="a5715-126">Some directives include arguments or values.</span></span> <span data-ttu-id="a5715-127">Любой текст, следующий за директивой (за исключением аргумента или значения, который является частью директивы), должен предшествовать разделителю однострочных комментариев (//) или заключены в разделители комментариев (/ \* \* /).</span><span class="sxs-lookup"><span data-stu-id="a5715-127">Any text that follows a directive (except an argument or value that is part of the directive) must be preceded by the single-line comment delimiter (//) or enclosed in comment delimiters (/\* \*/).</span></span> <span data-ttu-id="a5715-128">Строки, содержащие директивы препроцессора, могут быть продолжены непосредственно перед маркером конца строки с обратной косой чертой ( \\ ).</span><span class="sxs-lookup"><span data-stu-id="a5715-128">Lines containing preprocessor directives can be continued by immediately preceding the end-of-line marker with a backslash (\\).</span></span>

<span data-ttu-id="a5715-129">Директивы препроцессора могут находиться в любом месте файла исходного кода, но применяются только к оставшейся части файла.</span><span class="sxs-lookup"><span data-stu-id="a5715-129">Preprocessor directives can appear anywhere in a source file, but they apply only to the remainder of the source file.</span></span>

## <a name="related-topics"></a><span data-ttu-id="a5715-130">Связанные темы</span><span class="sxs-lookup"><span data-stu-id="a5715-130">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="a5715-131">Приложение (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="a5715-131">Appendix (DirectX HLSL)</span></span>](dx-graphics-hlsl-appendix.md)
</dt> </dl>

 

 




