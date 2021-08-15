---
title: Иажентпропертишит Сетпаже
description: Иажентпропертишит Сетпаже
ms.assetid: 52451a45-4f05-4209-ac3a-b4f2d90b3e74
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bf67c3ecb10ec5a8372a00e11d356e4b050b50be4a0563d9c4ebeefcd8040f1c
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "118476794"
---
# <a name="iagentpropertysheetsetpage"></a>Иажентпропертишит:: Сетпаже

\[Microsoft Agent является устаревшим по отношению к Windows 7 и может быть недоступен в последующих версиях Windows.\]

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



|                 | Описание            |
|-----------------|------------------------|
| **Речи**    | Страница речевого ввода. |
| **Проверки**    | Страница выходных данных.       |
| **Информация** | Страница авторских прав.    |



 

</dd> </dl>

## <a name="see-also"></a>См. также

[**Иажентпропертишит:: @ Page**](iagentpropertysheet--getpage.md)


 

 




