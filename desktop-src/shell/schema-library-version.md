---
description: <version>Элемент указывает версию содержимого этой библиотеки. Этот элемент не имеет атрибутов и не содержит дочерних элементов.
ms.assetid: 77FD5EF6-6B6F-48e1-973F-AC069F729613
title: Элемент Version (схема библиотеки)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e7b16a6078a16f4ebbe5e995503114996572f1b8
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104984584"
---
# <a name="version-element-library-schema"></a>Элемент Version (схема библиотеки)

<version>Элемент указывает версию содержимого этой библиотеки. Этот элемент не имеет атрибутов и не содержит дочерних элементов.

## <a name="syntax"></a>Синтаксис

``` syntax
<!-- version -->
<xs:element name="version" type="xs:int" minOccurs="0"/>
```

## <a name="element-information"></a>Сведения об элементе



| Родительский элемент                                                               | Дочерние элементы |
|------------------------------------------------------------------------------|----------------|
| [Элемент Либраридескриптион (схема библиотеки)](schema-librarydescription.md) | None           |



 

## <a name="remarks"></a>Remarks

Версия содержимого библиотеки отличается от версии в формате файла библиотеки ( \* . Library-MS). Версия формата файла библиотеки указывается в [пространстве имен](library-schema-entry.md).

## <a name="related-topics"></a>См. также

<dl> <dt>

[Схема описания библиотеки](library-schema-entry.md)
</dt> <dt>

[Схема описания соединителя поиска](../search/search-sconn-desc-schema-entry.md)
</dt> </dl>

 

 
