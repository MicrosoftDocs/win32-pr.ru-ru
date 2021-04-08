---
title: " #elif"
description: Директива \ elif помечает необязательное предложение блока условной компиляции, определенного директивой \ ifdef, \ ifndef или \ if.
ms.assetid: 432b8543-7e1a-411a-8191-cc0f0e4a2e86
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2a548cff74151dadf4a83a1e7d91ceedeafe07e2
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/16/2019
ms.locfileid: "104068109"
---
# <a name="elif"></a><span data-ttu-id="96605-103">\##elif</span><span class="sxs-lookup"><span data-stu-id="96605-103">\#elif</span></span>

<span data-ttu-id="96605-104">Директива **\# elif** помечает необязательное предложение блока условной компиляции, определенного директивой **\# ifdef**, **\# ifndef** или **\# If** .</span><span class="sxs-lookup"><span data-stu-id="96605-104">The **\#elif** directive marks an optional clause of a conditional-compilation block defined by a **\#ifdef**, **\#ifndef**, or **\#if** directive.</span></span> <span data-ttu-id="96605-105">Директива управляет условной компиляцией файла ресурсов путем проверки указанного константного выражения.</span><span class="sxs-lookup"><span data-stu-id="96605-105">The directive controls conditional compilation of the resource file by checking the specified constant expression.</span></span> <span data-ttu-id="96605-106">Если константное выражение не равно нулю, то параметр **\# elif** указывает компилятору продолжить обработку операторов вплоть до следующей директивы **\# endif**, **\# else** или **\# elif** , а затем перейти к инструкции после **\# endif**.</span><span class="sxs-lookup"><span data-stu-id="96605-106">If the constant expression is nonzero, **\#elif** directs the compiler to continue processing statements up to the next **\#endif**, **\#else**, or **\#elif** directive and then skip to the statement after **\#endif**.</span></span> <span data-ttu-id="96605-107">Если константное выражение равно нулю, то параметр **\# elif** указывает компилятору перейти к следующей директиве **\# endif**, **\# else** или **\# elif** .</span><span class="sxs-lookup"><span data-stu-id="96605-107">If the constant expression is zero, **\#elif** directs the compiler to skip to the next **\#endif**, **\#else**, or **\#elif** directive.</span></span> <span data-ttu-id="96605-108">В условном блоке можно использовать любое количество директив **\# elif** .</span><span class="sxs-lookup"><span data-stu-id="96605-108">You can use any number of **\#elif** directives in a conditional block.</span></span>

``` syntax
#elif constant-expression
```

<dl> <dt>

<span data-ttu-id="96605-109"><span id="constant-expression"></span><span id="CONSTANT-EXPRESSION"></span>*константное выражение*</span><span class="sxs-lookup"><span data-stu-id="96605-109"><span id="constant-expression"></span><span id="CONSTANT-EXPRESSION"></span>*constant-expression*</span></span>
</dt> <dd>

<span data-ttu-id="96605-110">Выражение, которое должно быть проверено.</span><span class="sxs-lookup"><span data-stu-id="96605-110">Expression to be checked.</span></span> <span data-ttu-id="96605-111">Это значение представляет собой определенное имя, целочисленную константу или выражение, состоящее из имен, целых чисел, арифметических и реляционных операторов.</span><span class="sxs-lookup"><span data-stu-id="96605-111">This value is a defined name, an integer constant, or an expression consisting of names, integers, and arithmetic and relational operators.</span></span>

</dd> </dl>

## <a name="example"></a><span data-ttu-id="96605-112">Пример</span><span class="sxs-lookup"><span data-stu-id="96605-112">Example</span></span>

<span data-ttu-id="96605-113">В этом примере с помощью параметра **\# elif** компилятор должен обрабатывать второй оператор [**Bitmap**](bitmap-resource.md) только в том случае, если значение, присвоенное имени версии, меньше 7.</span><span class="sxs-lookup"><span data-stu-id="96605-113">In this example, **\#elif** directs the compiler to process the second [**BITMAP**](bitmap-resource.md) statement only if the value assigned to the name Version is less than 7.</span></span> <span data-ttu-id="96605-114">Сама директива **\# elif** обрабатывается только в том случае, если версия больше или равна 3.</span><span class="sxs-lookup"><span data-stu-id="96605-114">The **\#elif** directive itself is processed only if Version is greater than or equal to 3.</span></span>

``` syntax
#if Version < 3
BITMAP 1 errbox.bmp
#elif Version < 7
BITMAP 1 userbox.bmp
#endif
```

## <a name="related-topics"></a><span data-ttu-id="96605-115">См. также</span><span class="sxs-lookup"><span data-stu-id="96605-115">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="96605-116">Директивы препроцессора</span><span class="sxs-lookup"><span data-stu-id="96605-116">Preprocessor Directives</span></span>](preprocessor-directives.md)
</dt> </dl>

 

 




