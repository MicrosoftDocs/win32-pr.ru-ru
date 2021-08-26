---
description: Предикат NULL указывает, имеет ли документ значение для указанного столбца.
ms.assetid: 078ffd99-2020-4da2-8968-301dba8cc436
title: Предикат NULL
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0bd80ea6cba2009b398c8cdd0a2926240e3ce78309ca3f8511fb6ba286f44a64
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "120058124"
---
# <a name="null-predicate"></a>Предикат NULL

Предикат **null** указывает, имеет ли документ значение для указанного столбца.

Предикат **null** имеет следующий синтаксис:


```
...WHERE <column> IS [NOT] NULL
```



Необязательное ключевое слово NOT инвертирует результат. Столбец может быть обычным или [идентификатором](-search-sql-identifiers.md)с разделителями.

> [!IMPORTANT]
> Чтобы проверить, имеет ли столбец значение **null** , необходимо использовать предикат **null** . Недопустимо использовать значение **null** в предикате сравнения. "Где column имеет **значение NULL**" является правильным. Недопустимое значение "WHERE Column = **null**".

 

## <a name="example"></a>Пример

В следующем примере возвращаются документы, не имеющие значения System. Video. режиссер.


```
...WHERE System.Video.Director IS NULL
```



## <a name="related-topics"></a>Связанные темы

<dl> <dt>

**Reference**
</dt> <dt>

[Предикат LIKE](-search-sql-like.md)
</dt> <dt>

[Сравнение литеральных значений](-search-sql-literalvaluecomparison.md)
</dt> <dt>

[Сравнения с несколькими значениями (МАССИВы)](-search-sql-multivaluedcomparisons.md)
</dt> <dt>

**Зрения**
</dt> <dt>

[Полнотекстовые предикаты](-search-sql-fulltextpredicates.md)
</dt> <dt>

[Неполнотекстовые предикаты](-search-sql-nonfulltextpredicates.md)
</dt> </dl>

 

 



