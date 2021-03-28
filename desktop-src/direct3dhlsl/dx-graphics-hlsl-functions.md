---
title: Функции (Справочник по HLSL)
description: Функции инкапсулируют инструкции HLSL.
ms.assetid: b6f934e5-eac7-4859-b1d0-698632011e1d
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 59b0bfcb2079329d4d7ad7c02e7e5a326d22c236
ms.sourcegitcommit: cba7f424a292fd7f3a8518947b9466439b455419
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/23/2019
ms.locfileid: "104335659"
---
# <a name="functions-hlsl-reference"></a><span data-ttu-id="c035c-103">Функции (Справочник по HLSL)</span><span class="sxs-lookup"><span data-stu-id="c035c-103">Functions (HLSL reference)</span></span>

<span data-ttu-id="c035c-104">Функции инкапсулируют инструкции HLSL.</span><span class="sxs-lookup"><span data-stu-id="c035c-104">Functions encapsulate HLSL statements.</span></span> <span data-ttu-id="c035c-105">Это позволяет отлаживать набор функций, а затем повторно использовать их в шейдерах или эффектах.</span><span class="sxs-lookup"><span data-stu-id="c035c-105">This enables you to debug a set of functions and then reuse them across shaders or effects.</span></span> <span data-ttu-id="c035c-106">Может потребоваться создать функцию, которая инкапсулирует функциональные возможности шейдера вершин, шейдера пикселей или шейдера текстуры.</span><span class="sxs-lookup"><span data-stu-id="c035c-106">You may want to create a function that encapsulates the functionality of a vertex shader, pixel shader or texture shader.</span></span> <span data-ttu-id="c035c-107">В других случаях может потребоваться написать вспомогательную функцию, которая выполняет некоторую часто используемую задачу, а затем вызывать эту вспомогательную функцию из функции шейдера.</span><span class="sxs-lookup"><span data-stu-id="c035c-107">Other times, you may want to write a helper function that performs some commonly used task, and then call that helper function from your shader function.</span></span> <span data-ttu-id="c035c-108">Правила написания функций шейдера для HLSL очень похожи на написание функций C.</span><span class="sxs-lookup"><span data-stu-id="c035c-108">The rules for writing shader functions for HLSL are very similar to writing C functions.</span></span>

-   [<span data-ttu-id="c035c-109">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="c035c-109">Syntax</span></span>](dx-graphics-hlsl-function-syntax.md)
-   [<span data-ttu-id="c035c-110">Параметры</span><span class="sxs-lookup"><span data-stu-id="c035c-110">Parameters</span></span>](dx-graphics-hlsl-function-parameters.md)
-   [<span data-ttu-id="c035c-111">Оператор Return</span><span class="sxs-lookup"><span data-stu-id="c035c-111">Return Statement</span></span>](dx-graphics-hlsl-return.md)
-   [<span data-ttu-id="c035c-112">Сигнатуры</span><span class="sxs-lookup"><span data-stu-id="c035c-112">Signatures</span></span>](dx-graphics-hlsl-signatures.md)

<span data-ttu-id="c035c-113">HLSL также имеет ряд встроенных встроенных [**функций (DirectX HLSL)**](dx-graphics-hlsl-intrinsic-functions.md).</span><span class="sxs-lookup"><span data-stu-id="c035c-113">HLSL also has a number of built-in [**Intrinsic Functions (DirectX HLSL)**](dx-graphics-hlsl-intrinsic-functions.md).</span></span> <span data-ttu-id="c035c-114">Так как все встроенные функции протестированы и оптимизированы для производительности, рекомендуется использовать встроенную функцию, где это возможно, вместо создания собственной функции.</span><span class="sxs-lookup"><span data-stu-id="c035c-114">Because all intrinsic functions are tested and performance optimized, it is good practice to use an intrinsic function where possible instead of creating your own function.</span></span>

## <a name="related-topics"></a><span data-ttu-id="c035c-115">См. также</span><span class="sxs-lookup"><span data-stu-id="c035c-115">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="c035c-116">Синтаксис языка (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="c035c-116">Language Syntax (DirectX HLSL)</span></span>](dx-graphics-hlsl-language-syntax.md)
</dt> </dl>

 

 




