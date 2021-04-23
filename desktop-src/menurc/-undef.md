---
title: " undef"
description: Директива \ undef удаляет текущее определение указанного имени. Все последующие вхождения имени обрабатываются без замены.
ms.assetid: c9a0b538-3030-4d39-bfc2-d158061967b6
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a04b14eeea18a05795cd8ebbb94d81d0aead6a9d
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/16/2019
ms.locfileid: "105710083"
---
# <a name="undef"></a><span data-ttu-id="6700c-104">\#undef</span><span class="sxs-lookup"><span data-stu-id="6700c-104">\#undef</span></span>

<span data-ttu-id="6700c-105">Директива **\# undef** удаляет текущее определение указанного имени.</span><span class="sxs-lookup"><span data-stu-id="6700c-105">The **\#undef** directive removes the current definition of the specified name.</span></span> <span data-ttu-id="6700c-106">Все последующие вхождения имени обрабатываются без замены.</span><span class="sxs-lookup"><span data-stu-id="6700c-106">All subsequent occurrences of the name are processed without replacement.</span></span>

``` syntax
#undef name
```

<dl> <dt>

<span data-ttu-id="6700c-107"><span id="name"></span><span id="NAME"></span>*безымян*</span><span class="sxs-lookup"><span data-stu-id="6700c-107"><span id="name"></span><span id="NAME"></span>*name*</span></span>
</dt> <dd>

<span data-ttu-id="6700c-108">Удаляемое имя.</span><span class="sxs-lookup"><span data-stu-id="6700c-108">Name to be removed.</span></span> <span data-ttu-id="6700c-109">Это значение представляет собой любое сочетание букв, цифр и знаков препинания, допустимое для препроцессора C/C++.</span><span class="sxs-lookup"><span data-stu-id="6700c-109">This value is any combination of letters, digits, and punctuation that is valid for the C/C++ preprocessor.</span></span>

</dd> </dl>

## <a name="example"></a><span data-ttu-id="6700c-110">Пример</span><span class="sxs-lookup"><span data-stu-id="6700c-110">Example</span></span>

<span data-ttu-id="6700c-111">В этом примере удаляются определения имен ненулевых и USERCLASS:</span><span class="sxs-lookup"><span data-stu-id="6700c-111">This example removes the definitions for the names nonzero and USERCLASS:</span></span>

``` syntax
#undef     nonzero
#undef     USERCLASS
```

## <a name="related-topics"></a><span data-ttu-id="6700c-112">См. также</span><span class="sxs-lookup"><span data-stu-id="6700c-112">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="6700c-113">Директивы препроцессора</span><span class="sxs-lookup"><span data-stu-id="6700c-113">Preprocessor Directives</span></span>](preprocessor-directives.md)
</dt> </dl>

 

 




