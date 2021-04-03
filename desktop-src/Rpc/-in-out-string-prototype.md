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
# <a name="in-out-string-prototype"></a>\[в, out, строковый \] прототип

В приведенном ниже прототипе функции используется одиночный \[ [**строковый**](/windows/desktop/Midl/string) параметр [**in**](/windows/desktop/Midl/in) [**и**](/windows/desktop/Midl/out-idl) \] входных и выходных строк. Строка сначала содержит входные данные пациента, а затем переписывается с ответом Doctor, как показано ниже:

``` syntax
void Analyze([in, out, string, size_is(STRSIZE)] char  achInOut[]);
```

Этот пример похож на тот, который использовал строку с одной подсчетностью для ввода и вывода. Как и в этом примере, \[ [**атрибут \_ size**](/windows/desktop/Midl/size-is) \] определяет количество элементов, выделенных на сервере. Атрибут \[ [**String**](/windows/desktop/Midl/string) \] направляет заглушку вызывать **strlen** для определения числа переданных элементов.

Клиент выделяет всю память перед вызовом:

``` syntax
/* client */
char achInOut[STRSIZE];
...
gets_s(achInOut, STRSIZE);            // get patient input
Analyze(achInOut);
printf("%s\n", achInOut);  // display doctor response
```

Обратите внимание, что функция Analyze больше не должна вычислять длину возвращаемой строки, как в примере подсчета строки, где атрибут **\[ String \]** не использовался. Теперь суррогаты рассчитывают длину, как показано ниже:

``` syntax
/* server */
void Analyze(char *pchInOut)
{
   ...
   Respond(response, pchInOut); // don't need to call strlen
   return;                      // stubs handle size
}
```

 

 