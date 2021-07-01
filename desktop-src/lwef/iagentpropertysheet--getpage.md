---
title: Иажентпропертишитная страница
description: Иажентпропертишитная страница
ms.assetid: 40d00e9b-dd81-4e23-907a-6ca24a28fa95
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a7c08e564b5170d62cf5757536b9e11baec4883c
ms.sourcegitcommit: b32433cc0394159c7263809ae67615ab5792d40d
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/30/2021
ms.locfileid: "113119869"
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



|                 | Описание            |
|-----------------|------------------------|
| **Речи**    | Страница речевого ввода. |
| **Проверки**    | Страница выходных данных.       |
| **Информация** | Страница авторских прав.    |



 

</dd> </dl>

## <a name="see-also"></a>См. также

[**Иажентпропертишит:: Сетпаже**](iagentpropertysheet--setpage.md)


 

 




