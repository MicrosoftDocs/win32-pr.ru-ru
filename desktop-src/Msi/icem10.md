---
description: ICEM10 проверяет, что модуль слияния содержит только те свойства, которые разрешены в таблице свойств.
ms.assetid: 9ac7a724-ea0e-4caa-bb4f-846bfb802037
title: ICEM10
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1bb9634ecec212954031e665fa0ebdc3c19856a9bcd02d894eb6e579455d059b
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "120129414"
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
| Color                                      | Красный       |
| [**Производителя**](manufacturer.md)       | Microsoft |
| [**продуктлангуаже**](productlanguage.md) | 1033      |



 

В следующей процедуре показано, как исправить ошибки.

**Исправление ошибок**

1.  Удалите свойство [**Manufacturer**](manufacturer.md)из [таблицы свойств](property-table.md).
2.  Удалите свойство "[**продуктлангуаже**](productlanguage.md)" из [таблицы свойств](property-table.md).

## <a name="table-used-during-execution"></a>Таблица, используемая во время выполнения

[Таблица свойств](property-table.md) используется во время выполнения.

## <a name="related-topics"></a>Связанные темы

<dl> <dt>

[Ссылка на модуль слияния ICE](merge-module-ice-reference.md)
</dt> </dl>

 

 



