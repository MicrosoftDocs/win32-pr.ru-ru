---
title: Справочник по HLSL
description: В справочной документации HLSL указаны языковые характеристики. Он разбивается на несколько разделов.
ms.assetid: 1d0e12ff-8559-4e5c-9914-6ed313ea5464
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: ce0bb59dd26bd8bb9723bcdff23bbc79ee810253
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/16/2019
ms.locfileid: "104068361"
---
# <a name="reference-for-hlsl"></a><span data-ttu-id="bfe17-104">Справочник по HLSL</span><span class="sxs-lookup"><span data-stu-id="bfe17-104">Reference for HLSL</span></span>

<span data-ttu-id="bfe17-105">В справочной документации HLSL указаны языковые характеристики.</span><span class="sxs-lookup"><span data-stu-id="bfe17-105">The HLSL reference documentation specifies the language characteristics.</span></span> <span data-ttu-id="bfe17-106">Он разбивается на несколько разделов.</span><span class="sxs-lookup"><span data-stu-id="bfe17-106">It is broken into several sections.</span></span>

-   <span data-ttu-id="bfe17-107">[Синтаксис языка (DirectX HLSL)](dx-graphics-hlsl-language-syntax.md) . шейдеры программирования в HLSL требуют понимания синтаксиса языка, т. е. НАПИСАНИЯ кода HLSL.</span><span class="sxs-lookup"><span data-stu-id="bfe17-107">[Language Syntax (DirectX HLSL)](dx-graphics-hlsl-language-syntax.md) - Programming shaders in HLSL requires that you understand the language syntax, that is, how you write HLSL code.</span></span> <span data-ttu-id="bfe17-108">Сюда входит код для объявления и инициализации переменных, написания определяемых пользователем функций шейдеров и добавления операторов управления потоком, чтобы сделать функции более мощными.</span><span class="sxs-lookup"><span data-stu-id="bfe17-108">This includes code to declare and initialize variables, write user-defined shader functions, and add flow control statements to make your functions more powerful.</span></span>
-   <span data-ttu-id="bfe17-109">[Модели шейдеров и профили шейдеров](dx-graphics-hlsl-models.md) . компилятор HLSL реализует правила и ограничения на основе моделей шейдеров.</span><span class="sxs-lookup"><span data-stu-id="bfe17-109">[Shader Models vs Shader Profiles](dx-graphics-hlsl-models.md) - The HLSL compiler implements rules and restrictions based on shader models.</span></span> <span data-ttu-id="bfe17-110">Код в каждом шейдере вершин, шейдер геометрии (при использовании Direct3D 10) и построитель текстуры проверяются по модели шейдера, которую вы предоставляете во время компиляции.</span><span class="sxs-lookup"><span data-stu-id="bfe17-110">The code in each vertex shader, geometry shader (if you are using Direct3D 10) and pixel shader are validated against a shader model, which you supply at compile time.</span></span>
-   <span data-ttu-id="bfe17-111">[**Встроенные функции (DirectX HLSL)**](dx-graphics-hlsl-intrinsic-functions.md) — HLSL имеет множество встроенных функций.</span><span class="sxs-lookup"><span data-stu-id="bfe17-111">[**Intrinsic Functions (DirectX HLSL)**](dx-graphics-hlsl-intrinsic-functions.md) - HLSL has many intrinsic functions.</span></span> <span data-ttu-id="bfe17-112">Они реализуются и тестируются, чтобы вы могли использовать их, зная, что они уже отлажены и работают хорошо.</span><span class="sxs-lookup"><span data-stu-id="bfe17-112">These are implemented and tested so that you can use them knowing that they are already debugged and they perform well.</span></span> <span data-ttu-id="bfe17-113">Если вы решили написать собственные функции, см. раздел Синтаксис языка для написания определяемых пользователем функций.</span><span class="sxs-lookup"><span data-stu-id="bfe17-113">If you choose to write your own functions, see the language syntax section for writing user-defined functions.</span></span>
-   <span data-ttu-id="bfe17-114">[Справочник по шейдеру ASM](dx9-graphics-reference-asm.md) . инструкции по сборке, которые можно использовать для программирования и отладки шейдеров.</span><span class="sxs-lookup"><span data-stu-id="bfe17-114">[Asm Shader Reference](dx9-graphics-reference-asm.md) - Assembly instructions that you can use to program and debug shaders.</span></span>
-   <span data-ttu-id="bfe17-115">[D3DCompiler Reference](dx-graphics-d3dcompiler-reference.md) — компилирует необработанный источник HLSL.</span><span class="sxs-lookup"><span data-stu-id="bfe17-115">[D3DCompiler Reference](dx-graphics-d3dcompiler-reference.md) - Compiles raw HLSL source.</span></span>
-   <span data-ttu-id="bfe17-116">[Ссылка на преобразование встроенного формата](inline-format-conversion-reference.md) \_ . файл D3DX дксгиформатконверт. inl содержит функции преобразования встроенного формата, которые можно использовать в шейдере вычислений или шейдере пикселей на оборудовании Direct3D 11.</span><span class="sxs-lookup"><span data-stu-id="bfe17-116">[Inline Format Conversion Reference](inline-format-conversion-reference.md) - The D3DX\_DXGIFormatConvert.inl file contains inline format conversion functions that you can use in the compute shader or pixel shader on Direct3D 11 hardware.</span></span> <span data-ttu-id="bfe17-117">Эти функции можно использовать в приложении для одновременного чтения и записи текстуры.</span><span class="sxs-lookup"><span data-stu-id="bfe17-117">You can use these functions in your application to simultaneously both read from and write to a texture.</span></span> <span data-ttu-id="bfe17-118">Это значит, что можно выполнять редактирование изображений на месте.</span><span class="sxs-lookup"><span data-stu-id="bfe17-118">That is, you can perform in-place image editing.</span></span> <span data-ttu-id="bfe17-119">Чтобы использовать эти функции преобразования встроенного формата, включите в \_ приложение файл D3DX дксгиформатконверт. inl.</span><span class="sxs-lookup"><span data-stu-id="bfe17-119">To use these inline format conversion functions, include the D3DX\_DXGIFormatConvert.inl file in your application.</span></span>
-   <span data-ttu-id="bfe17-120">[Приложение (DirectX HLSL)](dx-graphics-hlsl-appendix.md) — приложение включено для полноты.</span><span class="sxs-lookup"><span data-stu-id="bfe17-120">[Appendix (DirectX HLSL)](dx-graphics-hlsl-appendix.md) - The appendix is included for completeness.</span></span> <span data-ttu-id="bfe17-121">Он включает список ключевых слов и зарезервированных слов; Эти слова нельзя использовать в качестве идентификаторов в программах.</span><span class="sxs-lookup"><span data-stu-id="bfe17-121">It includes a listing of the keywords and reserved words; these words cannot be used as identifiers in your programs.</span></span> <span data-ttu-id="bfe17-122">Он также содержит список грамматики языка для справки.</span><span class="sxs-lookup"><span data-stu-id="bfe17-122">It also includes a listing of the language grammar for reference.</span></span>
-   <span data-ttu-id="bfe17-123">[**HLSL Errors and**](hlsl-errors-and-warnings.md) Warnings — содержит коды ошибок и предупреждений, которые может возвращать шейдер.</span><span class="sxs-lookup"><span data-stu-id="bfe17-123">[**HLSL errors and warnings**](hlsl-errors-and-warnings.md) - Provides error and warning codes that a shader can return.</span></span>

## <a name="related-topics"></a><span data-ttu-id="bfe17-124">См. также</span><span class="sxs-lookup"><span data-stu-id="bfe17-124">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="bfe17-125">HLSL</span><span class="sxs-lookup"><span data-stu-id="bfe17-125">HLSL</span></span>](dx-graphics-hlsl.md)
</dt> <dt>

[<span data-ttu-id="bfe17-126">Руководство по программированию для HLSL</span><span class="sxs-lookup"><span data-stu-id="bfe17-126">Programming Guide for HLSL</span></span>](dx-graphics-hlsl-pguide.md)
</dt> </dl>

 

 




