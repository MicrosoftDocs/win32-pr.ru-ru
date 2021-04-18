---
title: " if"
description: Директива \ if управляет условной компиляцией файла ресурсов путем проверки указанного константного выражения.
ms.assetid: 4d0f26a0-1a2d-4fad-b5ce-b9441397d2c3
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 364d6f5eb818813f61f6428446effb4793b96b2d
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/16/2019
ms.locfileid: "105700559"
---
# <a name="if"></a><span data-ttu-id="644e7-103">\#if</span><span class="sxs-lookup"><span data-stu-id="644e7-103">\#if</span></span>

<span data-ttu-id="644e7-104">Директива **\# If** управляет условной компиляцией файла ресурсов путем проверки указанного константного выражения.</span><span class="sxs-lookup"><span data-stu-id="644e7-104">The **\#if** directive controls conditional compilation of the resource file by checking the specified constant expression.</span></span> <span data-ttu-id="644e7-105">Значение, если константное выражение не равно нулю, **\# Если** указывает компилятору продолжить обработку операторов до следующей директивы **\# endif**, **\# else** или **\# elif** , а затем перейти к оператору после директивы **\# endif** .</span><span class="sxs-lookup"><span data-stu-id="644e7-105">If the constant expression is nonzero, **\#if** directs the compiler to continue processing statements up to the next **\#endif**, **\#else**, or **\#elif** directive and then skip to the statement after the **\#endif** directive.</span></span> <span data-ttu-id="644e7-106">Значение, если константное выражение равно нулю, **\# Если** указывает компилятору перейти к следующей директиве **\# endif**, **\# else** или **\# elif** .</span><span class="sxs-lookup"><span data-stu-id="644e7-106">If the constant expression is zero, **\#if** directs the compiler to skip to the next **\#endif**, **\#else**, or **\#elif** directive.</span></span>

``` syntax
#if constant-expression
```

<dl> <dt>

<span data-ttu-id="644e7-107"><span id="constant-expression"></span><span id="CONSTANT-EXPRESSION"></span>*константное выражение*</span><span class="sxs-lookup"><span data-stu-id="644e7-107"><span id="constant-expression"></span><span id="CONSTANT-EXPRESSION"></span>*constant-expression*</span></span>
</dt> <dd>

<span data-ttu-id="644e7-108">Выражение, которое должно быть проверено.</span><span class="sxs-lookup"><span data-stu-id="644e7-108">Expression to be checked.</span></span> <span data-ttu-id="644e7-109">Это значение представляет собой определенное имя, целочисленную константу или выражение, состоящее из имен, целых чисел, арифметических и реляционных операторов.</span><span class="sxs-lookup"><span data-stu-id="644e7-109">This value is a defined name, an integer constant, or an expression consisting of names, integers, and arithmetic and relational operators.</span></span>

</dd> </dl>

## <a name="example"></a><span data-ttu-id="644e7-110">Пример</span><span class="sxs-lookup"><span data-stu-id="644e7-110">Example</span></span>

<span data-ttu-id="644e7-111">В этом примере оператор [**Bitmap**](bitmap-resource.md) компилируется только в том случае, если значение назначенной версии меньше 3:</span><span class="sxs-lookup"><span data-stu-id="644e7-111">This example compiles the [**BITMAP**](bitmap-resource.md) statement only if the value assigned Version is less than 3:</span></span>

``` syntax
#if Version < 3
BITMAP 1 errbox.bmp
#endif
```

## <a name="related-topics"></a><span data-ttu-id="644e7-112">См. также</span><span class="sxs-lookup"><span data-stu-id="644e7-112">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="644e7-113">Директивы препроцессора</span><span class="sxs-lookup"><span data-stu-id="644e7-113">Preprocessor Directives</span></span>](preprocessor-directives.md)
</dt> </dl>

 

 




