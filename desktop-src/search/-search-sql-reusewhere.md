---
description: Предложение WHERE в запросе указывает набор элементов для сопоставления с результатами.
ms.assetid: ed51edd5-6edc-4fcd-a69b-cb48c399ba7c
title: Функция Реусевхере
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 16bb5af4c3acd4637b27a2b3c9c7e14436eabb0b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "105701383"
---
# <a name="reusewhere-function"></a>Функция Реусевхере

Предложение [WHERE](-search-sql-where.md) в запросе указывает набор элементов для сопоставления с результатами. Последующие запросы могут совместно использовать работу, выполненную для предыдущего запроса, с помощью функции Реусевхере в новом предложении WHERE запроса. Запросы, использующие эту функцию, выполняются быстрее.

## <a name="examples"></a>Примеры

В следующем сценарии показано, как использовать функцию Реусевхере:

1.  Вы выполните следующий запрос:
    ```
    SELECT System.ItemName FROM SystemIndex 
    WHERE CONTAINS(*, 'pencil') AND System.ItemDate > '2007-3-5'
    ```

    

2.  В возвращенном наборе строк вы получаете [идентификатор WHERE](-search-sql-rowset-properties.md), *Query1WhereID*.

    Идентификатор WHERE является свойством набора строк с параметром PROPs {aa6ee6b0-e828-11D0-B2-3E-00-AA-00-47-FC-01}, PROPID 8 и типом UI4.

3.  Вы выдаете второй запрос с помощью функции Реусевхере, передавая *Query1WhereID* из шага 2:
    ```
    SELECT System.ItemUrl FROM SystemIndex 
    WHERE ReuseWhere(Query1WhereID) AND SCOPE='file:'
    ```

    

Второй запрос эквивалентен следующему:


```
SELECT System.ItemUrl, System.ItemName FROM SystemIndex 
WHERE CONTAINS(*, 'pencil') AND System.ItemDate > '2007-3-5' AND Scope='file:'
```



Функцию Реусевхере можно использовать анвхере в предложении [WHERE](-search-sql-where.md) .

## <a name="related-topics"></a>Связанные темы

<dl> <dt>

**Reference**
</dt> <dt>

[Предложения WHERE](-search-sql-where.md)
</dt> <dt>

[Свойства набора строк](-search-sql-rowset-properties.md)
</dt> </dl>

 

 



