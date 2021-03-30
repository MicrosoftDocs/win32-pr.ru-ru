---
title: Иажентпропертишит Сетпаже
description: Иажентпропертишит Сетпаже
ms.assetid: 52451a45-4f05-4209-ac3a-b4f2d90b3e74
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4d86bbacfed445c5266a299495df5c07fd6166d9
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/16/2019
ms.locfileid: "103776889"
---
# <a name="iagentpropertysheetsetpage"></a>Иажентпропертишит:: Сетпаже

\[Microsoft Agent является устаревшим в Windows 7 и может быть недоступен в последующих версиях Windows.\]

``` syntax
HRESULT SetPage(
   BSTR bszPage  // current property page
);
```

Задает текущую страницу страницы свойств Microsoft Agent.

-   Возвращает значение S \_ , чтобы указать, что операция выполнена успешно.

<dl> <dt>

<span id="bszPage"></span><span id="bszpage"></span><span id="BSZPAGE"></span>*бсзпаже*
</dt> <dd>

Объект BSTR, задающий текущую страницу Свойства. Параметр может принимать одно из следующих действий.



|                 |                        |
|-----------------|------------------------|
| **Речи**    | Страница речевого ввода. |
| **Проверки**    | Страница выходных данных.       |
| **Информация** | Страница авторских прав.    |



 

</dd> </dl>

## <a name="see-also"></a>См. также:

[**Иажентпропертишит:: @ Page**](iagentpropertysheet--getpage.md)


 

 




