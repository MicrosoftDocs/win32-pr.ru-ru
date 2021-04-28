---
title: Выделение памяти в COM
description: Выделение памяти в COM
ms.assetid: b3c318d2-1273-430e-8aca-5bd5c95c138e
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 82cb9913da55fab82f699ac05dae3998f7582224
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2021
ms.locfileid: "108103892"
---
# <a name="memory-allocation-in-com"></a>Выделение памяти в COM

Иногда метод выделяет буфер памяти в куче и возвращает адрес буфера вызывающему объекту. COM определяет пару функций для выделения и освобождения памяти в куче.

-   Функция [**CoTaskMemAlloc**](/windows/desktop/api/combaseapi/nf-combaseapi-cotaskmemalloc) выделяет блок памяти.
-   Функция [**CoTaskMemFree**](/windows/desktop/api/combaseapi/nf-combaseapi-cotaskmemfree) освобождает блок памяти, выделенный с помощью функции [**CoTaskMemAlloc**](/windows/desktop/api/combaseapi/nf-combaseapi-cotaskmemalloc).

Мы видели пример этого шаблона в [примере открытия диалогового окна](example--the-open-dialog-box.md):


```C++
PWSTR pszFilePath;
hr = pItem->GetDisplayName(SIGDN_FILESYSPATH, &pszFilePath);
if (SUCCEEDED(hr))
{
    // ...
    CoTaskMemFree(pszFilePath);
}
```



Метод " [**DisplayName**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishellitem-getdisplayname) " выделяет память для строки. На внутреннем уровне метод вызывает функцию [**CoTaskMemAlloc**](/windows/desktop/api/combaseapi/nf-combaseapi-cotaskmemalloc) для выделения строки. Когда метод возвращает значение, *псзфилепас* указывает на расположение памяти нового буфера. Вызывающий объект отвечает за вызов [**CoTaskMemFree**](/windows/desktop/api/combaseapi/nf-combaseapi-cotaskmemfree) для освобождения памяти.

Почему COM определяет собственные функции выделения памяти? Одна из причин — предоставить уровень абстракции для распределителя кучи. В противном случае некоторые методы могут вызывать функцию **malloc** , а другие — как **New**. В некоторых случаях программе потребуется вызвать **бесплатную** функцию, а затем **Удалить** ее в других, а также быстро стать невозможной. Функции выделения COM создают единообразный подход.

Еще один вопрос заключается в том, что COM является *двоичным* стандартом, поэтому он не привязан к конкретному языку программирования. Таким образом, COM не может полагаться на любые специфические для конкретного языка формы выделения памяти.

## <a name="next"></a>Следующая

[Методики программирования COM](com-coding-practices.md)

 

 
