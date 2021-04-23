---
title: " ifndef"
description: Директива \ ifndef управляет условной компиляцией файла ресурсов путем проверки указанного имени.
ms.assetid: b83d7b0e-1a37-47a8-b495-0eab05ed3a9a
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 984a969123ea68fd68b14c1b98354b8bc5205aba
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/16/2019
ms.locfileid: "105691230"
---
# <a name="ifndef"></a><span data-ttu-id="8585c-103">\#ifndef</span><span class="sxs-lookup"><span data-stu-id="8585c-103">\#ifndef</span></span>

<span data-ttu-id="8585c-104">Директива **\# ifndef** управляет условной компиляцией файла ресурсов путем проверки указанного имени.</span><span class="sxs-lookup"><span data-stu-id="8585c-104">The **\#ifndef** directive controls conditional compilation of the resource file by checking the specified name.</span></span> <span data-ttu-id="8585c-105">Если имя не было определено или его определение было удалено с помощью директивы **\# undef** , то параметр **\# ifndef** указывает компилятору продолжить обработку операторов вплоть до следующей директивы **\# endif**, **\# else** или **\# elif** , а затем перейти к оператору после директивы **\# endif** .</span><span class="sxs-lookup"><span data-stu-id="8585c-105">If the name has not been defined or if its definition has been removed by using the **\#undef** directive, **\#ifndef** directs the compiler to continue processing statements up to the next **\#endif**, **\#else**, or **\#elif** directive and then skip to the statement after the **\#endif** directive.</span></span> <span data-ttu-id="8585c-106">Если имя определено, то параметр **\# ifndef** направляет компилятор в следующую директиву **\# endif**, **\# else** или **\# elif** .</span><span class="sxs-lookup"><span data-stu-id="8585c-106">If the name is defined, **\#ifndef** directs the compiler to skip to the next **\#endif**, **\#else**, or **\#elif** directive.</span></span>

``` syntax
#ifndef name
```

<dl> <dt>

<span data-ttu-id="8585c-107"><span id="name"></span><span id="NAME"></span>*безымян*</span><span class="sxs-lookup"><span data-stu-id="8585c-107"><span id="name"></span><span id="NAME"></span>*name*</span></span>
</dt> <dd>

<span data-ttu-id="8585c-108">Имя, проверяемое директивой.</span><span class="sxs-lookup"><span data-stu-id="8585c-108">Name to be checked by the directive.</span></span>

</dd> </dl>

## <a name="example"></a><span data-ttu-id="8585c-109">Пример</span><span class="sxs-lookup"><span data-stu-id="8585c-109">Example</span></span>

<span data-ttu-id="8585c-110">Этот пример компилирует оператор [**Bitmap**](bitmap-resource.md) , только если не определен параметр optimize:</span><span class="sxs-lookup"><span data-stu-id="8585c-110">This example compiles the [**BITMAP**](bitmap-resource.md) statement only if Optimize is not defined:</span></span>

``` syntax
#ifndef Optimize
BITMAP 1 errbox.bmp
#endif
```

## <a name="related-topics"></a><span data-ttu-id="8585c-111">См. также</span><span class="sxs-lookup"><span data-stu-id="8585c-111">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="8585c-112">Директивы препроцессора</span><span class="sxs-lookup"><span data-stu-id="8585c-112">Preprocessor Directives</span></span>](preprocessor-directives.md)
</dt> </dl>

 

 




