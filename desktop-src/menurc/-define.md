---
title: " define"
description: Директива \ define Присваивает заданному значению указанное имя. Все последующие вхождения имени заменяются значением.
ms.assetid: 2699d2dc-caf8-47d6-8b2e-526357962532
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 557c6b486d9c2bd07b0b012c17e806f5d9eaae91
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/16/2019
ms.locfileid: "103777486"
---
# <a name="define"></a><span data-ttu-id="effb9-104">\#определенно</span><span class="sxs-lookup"><span data-stu-id="effb9-104">\#define</span></span>

<span data-ttu-id="effb9-105">Директива **\# define** Присваивает заданному значению указанное имя.</span><span class="sxs-lookup"><span data-stu-id="effb9-105">The **\#define** directive assigns the given value to the specified name.</span></span> <span data-ttu-id="effb9-106">Все последующие вхождения имени заменяются значением.</span><span class="sxs-lookup"><span data-stu-id="effb9-106">All subsequent occurrences of the name are replaced by the value.</span></span>

``` syntax
#define name value
```

<dl> <dt>

<span data-ttu-id="effb9-107"><span id="name"></span><span id="NAME"></span>*безымян*</span><span class="sxs-lookup"><span data-stu-id="effb9-107"><span id="name"></span><span id="NAME"></span>*name*</span></span>
</dt> <dd>

<span data-ttu-id="effb9-108">Имя, которое необходимо определить.</span><span class="sxs-lookup"><span data-stu-id="effb9-108">Name to be defined.</span></span> <span data-ttu-id="effb9-109">Это значение представляет собой любое сочетание букв, цифр и знаков препинания, допустимое для препроцессора C/C++.</span><span class="sxs-lookup"><span data-stu-id="effb9-109">This value is any combination of letters, digits, and punctuation that is valid for the C/C++ preprocessor.</span></span>

</dd> <dt>

<span data-ttu-id="effb9-110"><span id="value"></span><span id="VALUE"></span>*значений*</span><span class="sxs-lookup"><span data-stu-id="effb9-110"><span id="value"></span><span id="VALUE"></span>*value*</span></span>
</dt> <dd>

<span data-ttu-id="effb9-111">Целое число, символьная строка или строка текста.</span><span class="sxs-lookup"><span data-stu-id="effb9-111">Integer, character string, or line of text.</span></span>

</dd> </dl>

## <a name="example"></a><span data-ttu-id="effb9-112">Пример</span><span class="sxs-lookup"><span data-stu-id="effb9-112">Example</span></span>

<span data-ttu-id="effb9-113">В этом примере значения присваиваются именам ненулевые и USERCLASS:</span><span class="sxs-lookup"><span data-stu-id="effb9-113">This example assigns values to the names NONZERO and USERCLASS:</span></span>

``` syntax
#define     NONZERO     1
#define     USERCLASS   "MyControlClass"
```

## <a name="related-topics"></a><span data-ttu-id="effb9-114">См. также</span><span class="sxs-lookup"><span data-stu-id="effb9-114">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="effb9-115">Директивы препроцессора</span><span class="sxs-lookup"><span data-stu-id="effb9-115">Preprocessor Directives</span></span>](preprocessor-directives.md)
</dt> </dl>

 

 




