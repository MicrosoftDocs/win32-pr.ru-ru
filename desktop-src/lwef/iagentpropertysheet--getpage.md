---
title: Иажентпропертишитная страница
description: Иажентпропертишитная страница
ms.assetid: 40d00e9b-dd81-4e23-907a-6ca24a28fa95
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4fb1fe6cdf6f667011eb048625349f6905913a16
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/16/2019
ms.locfileid: "104411021"
---
# <a name="iagentpropertysheetgetpage"></a>Иажентпропертишит:: @ Page

\[Microsoft Agent является устаревшим в Windows 7 и может быть недоступен в последующих версиях Windows.\]

``` syntax
HRESULT GetPage(
BSTR * pbszPage  // address of variable for current property page
);
```

Извлекает текущую страницу страницы свойств Microsoft Agent.

-   Возвращает значение S \_ , чтобы указать, что операция выполнена успешно.

<dl> <dt>

<span id="pbszPage"></span><span id="pbszpage"></span><span id="PBSZPAGE"></span>*пбсзпаже*
</dt> <dd>

Адрес переменной, которая получает текущую страницу страницы свойств (последняя просмотренная страница, если окно не открыто). Параметр может быть одним из следующих:



|                 |                        |
|-----------------|------------------------|
| **Речи**    | Страница речевого ввода. |
| **Проверки**    | Страница выходных данных.       |
| **Информация** | Страница авторских прав.    |



 

</dd> </dl>

## <a name="see-also"></a>См. также:

[**Иажентпропертишит:: Сетпаже**](iagentpropertysheet--setpage.md)


 

 




