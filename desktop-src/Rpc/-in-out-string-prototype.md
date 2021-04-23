---
title: " в, out, строковый прототип"
description: В следующем прототипе функции для входных и выходных строк используется одиночный параметр "in", "out", "String \".
ms.assetid: 5a652b79-11ca-4780-aac1-60a22f96b4af
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2ed8ed47c02ea3e08672d529bf7ce9f627925518
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "103987615"
---
# <a name="in-out-string-prototype"></a><span data-ttu-id="d5e41-103">\[в, out, строковый \] прототип</span><span class="sxs-lookup"><span data-stu-id="d5e41-103">\[in, out, string\] Prototype</span></span>

<span data-ttu-id="d5e41-104">В приведенном ниже прототипе функции используется одиночный \[ [**строковый**](/windows/desktop/Midl/string) параметр [**in**](/windows/desktop/Midl/in) [**и**](/windows/desktop/Midl/out-idl) \] входных и выходных строк.</span><span class="sxs-lookup"><span data-stu-id="d5e41-104">The following function prototype uses a single \[[**in**](/windows/desktop/Midl/in), [**out**](/windows/desktop/Midl/out-idl), [**string**](/windows/desktop/Midl/string)\] parameter for both the input and output strings.</span></span> <span data-ttu-id="d5e41-105">Строка сначала содержит входные данные пациента, а затем переписывается с ответом Doctor, как показано ниже:</span><span class="sxs-lookup"><span data-stu-id="d5e41-105">The string first contains patient input and is then overwritten with the doctor response as shown:</span></span>

``` syntax
void Analyze([in, out, string, size_is(STRSIZE)] char  achInOut[]);
```

<span data-ttu-id="d5e41-106">Этот пример похож на тот, который использовал строку с одной подсчетностью для ввода и вывода.</span><span class="sxs-lookup"><span data-stu-id="d5e41-106">This example is similar to the one that employed a single-counted string for both input and output.</span></span> <span data-ttu-id="d5e41-107">Как и в этом примере, \[ [**атрибут \_ size**](/windows/desktop/Midl/size-is) \] определяет количество элементов, выделенных на сервере.</span><span class="sxs-lookup"><span data-stu-id="d5e41-107">As with that example, the \[[**size\_is**](/windows/desktop/Midl/size-is)\] attribute determines the number of elements allocated on the server.</span></span> <span data-ttu-id="d5e41-108">Атрибут \[ [**String**](/windows/desktop/Midl/string) \] направляет заглушку вызывать **strlen** для определения числа переданных элементов.</span><span class="sxs-lookup"><span data-stu-id="d5e41-108">The \[[**string**](/windows/desktop/Midl/string)\] attribute directs the stub to call **strlen** to determine the number of transmitted elements.</span></span>

<span data-ttu-id="d5e41-109">Клиент выделяет всю память перед вызовом:</span><span class="sxs-lookup"><span data-stu-id="d5e41-109">The client allocates all memory before the call as:</span></span>

``` syntax
/* client */
char achInOut[STRSIZE];
...
gets_s(achInOut, STRSIZE);            // get patient input
Analyze(achInOut);
printf("%s\n", achInOut);  // display doctor response
```

<span data-ttu-id="d5e41-110">Обратите внимание, что функция Analyze больше не должна вычислять длину возвращаемой строки, как в примере подсчета строки, где атрибут **\[ String \]** не использовался.</span><span class="sxs-lookup"><span data-stu-id="d5e41-110">Note that the Analyze function no longer must calculate the length of the return string as it did in the counted-string example where the **\[string\]** attribute was not used.</span></span> <span data-ttu-id="d5e41-111">Теперь суррогаты рассчитывают длину, как показано ниже:</span><span class="sxs-lookup"><span data-stu-id="d5e41-111">Now the stubs calculate the length as shown:</span></span>

``` syntax
/* server */
void Analyze(char *pchInOut)
{
   ...
   Respond(response, pchInOut); // don't need to call strlen
   return;                      // stubs handle size
}
```

 

 