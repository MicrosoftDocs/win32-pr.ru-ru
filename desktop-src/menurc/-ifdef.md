---
title: " ifdef"
description: Директива \ ifdef управляет условной компиляцией файла ресурсов путем проверки указанного имени.
ms.assetid: 877c6b58-d8a1-4e68-8b69-29fe106d6cbd
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 38170fb2140f8405a86529c0899c1e4d4e93c026
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/16/2019
ms.locfileid: "104410984"
---
# <a name="ifdef"></a><span data-ttu-id="f5009-103">\#ifdef</span><span class="sxs-lookup"><span data-stu-id="f5009-103">\#ifdef</span></span>

<span data-ttu-id="f5009-104">Директива **\# ifdef** управляет условной компиляцией файла ресурсов путем проверки указанного имени.</span><span class="sxs-lookup"><span data-stu-id="f5009-104">The **\#ifdef** directive controls conditional compilation of the resource file by checking the specified name.</span></span> <span data-ttu-id="f5009-105">Если имя было определено с помощью директивы **\# define** или с помощью параметра командной строки **/d** в компиляторе ресурсов, параметр **\# ifdef** направляет компилятору инструкцию сразу после директивы **\# ifdef** .</span><span class="sxs-lookup"><span data-stu-id="f5009-105">If the name has been defined by using a **\#define** directive or by using the **/d** command-line option with the resource compiler, **\#ifdef** directs the compiler to continue with the statement immediately after the **\#ifdef** directive.</span></span> <span data-ttu-id="f5009-106">Если имя не определено, то параметр **\# ifdef** направляет компилятору пропуск всех инструкций вплоть до следующей директивы **\# endif** .</span><span class="sxs-lookup"><span data-stu-id="f5009-106">If the name has not been defined, **\#ifdef** directs the compiler to skip all statements up to the next **\#endif** directive.</span></span>

``` syntax
#ifdef name
```

<dl> <dt>

<span data-ttu-id="f5009-107"><span id="name"></span><span id="NAME"></span>*безымян*</span><span class="sxs-lookup"><span data-stu-id="f5009-107"><span id="name"></span><span id="NAME"></span>*name*</span></span>
</dt> <dd>

<span data-ttu-id="f5009-108">Имя, проверяемое директивой.</span><span class="sxs-lookup"><span data-stu-id="f5009-108">Name to be checked by the directive.</span></span>

</dd> </dl>

## <a name="example"></a><span data-ttu-id="f5009-109">Пример</span><span class="sxs-lookup"><span data-stu-id="f5009-109">Example</span></span>

<span data-ttu-id="f5009-110">Этот пример компилирует оператор [**Bitmap**](bitmap-resource.md) , только если определен параметр debug:</span><span class="sxs-lookup"><span data-stu-id="f5009-110">This example compiles the [**BITMAP**](bitmap-resource.md) statement only if Debug is defined:</span></span>

``` syntax
#ifdef Debug
BITMAP 1 errbox.bmp
#endif
```

## <a name="related-topics"></a><span data-ttu-id="f5009-111">См. также</span><span class="sxs-lookup"><span data-stu-id="f5009-111">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="f5009-112">Директивы препроцессора</span><span class="sxs-lookup"><span data-stu-id="f5009-112">Preprocessor Directives</span></span>](preprocessor-directives.md)
</dt> </dl>

 

 




