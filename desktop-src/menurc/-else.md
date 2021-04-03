---
title: " else"
description: Директива \ else помечает необязательное предложение блока условной компиляции, определенного директивой \ ifdef, \ ifndef или \ if. Директива \ else должна быть последней директивой перед директивой \ endif.
ms.assetid: 982466d9-ae77-4e1c-89f3-511335165da7
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 086acd9e6323f7be11a65951a33b2b11b680ad46
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/16/2019
ms.locfileid: "103776448"
---
# <a name="else"></a><span data-ttu-id="0d036-104">\#else</span><span class="sxs-lookup"><span data-stu-id="0d036-104">\#else</span></span>

<span data-ttu-id="0d036-105">Директива **\# else** помечает необязательное предложение блока условной компиляции, определенного директивой **\# ifdef**, **\# ifndef** или **\# If** .</span><span class="sxs-lookup"><span data-stu-id="0d036-105">The **\#else** directive marks an optional clause of a conditional-compilation block defined by a **\#ifdef**, **\#ifndef**, or **\#if** directive.</span></span> <span data-ttu-id="0d036-106">Директива **\# else** должна быть последней директивой перед директивой **\# endif** .</span><span class="sxs-lookup"><span data-stu-id="0d036-106">The **\#else** directive must be the last directive before the **\#endif** directive.</span></span>

``` syntax
#else
```

<span data-ttu-id="0d036-107">Эта директива не имеет параметров.</span><span class="sxs-lookup"><span data-stu-id="0d036-107">This directive has no parameters.</span></span>

## <a name="example"></a><span data-ttu-id="0d036-108">Пример</span><span class="sxs-lookup"><span data-stu-id="0d036-108">Example</span></span>

<span data-ttu-id="0d036-109">Этот пример компилирует второй оператор [**Bitmap**](bitmap-resource.md) , только если не ОПРЕДЕЛЕН параметр debug:</span><span class="sxs-lookup"><span data-stu-id="0d036-109">This example compiles the second [**BITMAP**](bitmap-resource.md) statement only if DEBUG is not defined:</span></span>

``` syntax
#ifdef DEBUG
    BITMAP 1 errbox.bmp
#else
    BITMAP 1 userbox.bmp
#endif
```

## <a name="related-topics"></a><span data-ttu-id="0d036-110">См. также</span><span class="sxs-lookup"><span data-stu-id="0d036-110">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="0d036-111">Директивы препроцессора</span><span class="sxs-lookup"><span data-stu-id="0d036-111">Preprocessor Directives</span></span>](preprocessor-directives.md)
</dt> </dl>

 

 




