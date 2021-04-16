---
description: ICEM10 проверяет, что модуль слияния содержит только те свойства, которые разрешены в таблице свойств.
ms.assetid: 9ac7a724-ea0e-4caa-bb4f-846bfb802037
title: ICEM10
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 80263e5033ec14bd669c5d046c7f3842d58e332f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "105650973"
---
# <a name="icem10"></a>ICEM10

ICEM10 проверяет, что модуль слияния содержит только те свойства, которые разрешены в [таблице свойств](property-table.md). Следующие свойства продукта не допускаются в таблице свойств:

-   [**Продуктлангуаже, свойство**](productlanguage.md)
-   [**ProductCode, свойство**](productcode.md)
-   [**ProductVersion, свойство**](productversion.md)
-   [**Свойство ProductName**](productname.md)
-   [**Свойство Manufacturer**](manufacturer.md)

## <a name="result"></a>Результат

ICEM10 отправляет сообщение об ошибке, если модуль слияния содержит свойство, недопустимое в [таблице свойств](property-table.md).

## <a name="example"></a>Пример

ICEM10 отправляет следующие сообщения об ошибках для модуля, содержащего отображаемые записи базы данных.

``` syntax
The property 'ProductLanguage' is not allowed in a merge module.

The property 'Manufacturer' is not allowed in a merge module.
```

В следующей таблице показана таблица с частичным [свойством](property-table.md).



| Свойство                                   | Значения    |
|--------------------------------------------|-----------|
| Цвет                                      | Красный       |
| [**Производителя**](manufacturer.md)       | Microsoft |
| [**продуктлангуаже**](productlanguage.md) | 1033      |



 

В следующей процедуре показано, как исправить ошибки.

**Исправление ошибок**

1.  Удалите свойство [**Manufacturer**](manufacturer.md)из [таблицы свойств](property-table.md).
2.  Удалите свойство "[**продуктлангуаже**](productlanguage.md)" из [таблицы свойств](property-table.md).

## <a name="table-used-during-execution"></a>Таблица, используемая во время выполнения

[Таблица свойств](property-table.md) используется во время выполнения.

## <a name="related-topics"></a>См. также

<dl> <dt>

[Ссылка на модуль слияния ICE](merge-module-ice-reference.md)
</dt> </dl>

 

 



