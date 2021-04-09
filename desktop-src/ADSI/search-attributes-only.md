---
title: Только атрибуты поиска
description: Иногда можно выполнить поиск для определения типа данных, доступных для объекта.
ms.assetid: 97eccea6-6a2b-4785-afd8-4af3dc7bd657
ms.tgt_platform: multiple
keywords:
- Поиск по атрибутам только ADSI
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f5c2a97873dfb52f56b123919c3eedd277a63a74
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/16/2019
ms.locfileid: "103986091"
---
# <a name="search-attributes-only"></a>Только атрибуты поиска

Иногда можно выполнить поиск для определения типа данных, доступных для объекта. В этом случае вы заинтересованы только в атрибутах, а не на значениях объекта. Для этого необходимо установить параметр "только атрибуты поиска". При указании этого параметра возвращаются имена атрибутов без их значений. Однако результирующий набор включает только те атрибуты, которые имеют присвоенные значения. Например, рассмотрим объект со следующими атрибутами:

``` syntax
First Name = Jeff
Last Name = Smith
Department = <Empty>
Phone Number = (425) 432-3442
```

Если задан параметр только атрибуты поиска, результирующий набор включает:

``` syntax
First Name
Last Name
Phone Number
```

Дополнительные сведения об использовании параметра поиска только атрибуты с конкретным интерфейсом поиска см. в следующих статьях:

-   [Возвращение только имен атрибутов с помощью IDirectorySearch](returning-only-attribute-names-with-idirectorysearch.md)
-   [Поиск с помощью объекты данных ActiveX](searching-with-activex-data-objects-ado.md)
-   [Поиск с помощью OLE DB](searching-with-ole-db.md)

 

 




