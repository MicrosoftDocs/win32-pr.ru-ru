---
description: <name>Элемент указывает имя этой библиотеки. Этот элемент является обязательным и не имеет атрибутов или дочерних элементов.
ms.assetid: 1F433405-5943-4579-BDAD-423C4E1A6E76
title: Элемент Name (схема библиотеки)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 54d38baa32587ee04c62c8c3086d5353e8eed9e1
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "104997955"
---
# <a name="name-element-library-schema"></a>Элемент Name (схема библиотеки)

<name>Элемент указывает имя этой библиотеки. Этот элемент является обязательным и не имеет атрибутов или дочерних элементов.

## <a name="syntax"></a>Синтаксис

``` syntax
<!-- name -->
<xs:element name="libraryDescription">
    <xs:complexType>
        <xs:all>
            <xs:element name="name" type="xs:string"/>
...
</libraryDescription>
```

## <a name="element-information"></a>Сведения об элементе



| Родительский элемент                                                               | Дочерние элементы |
|------------------------------------------------------------------------------|----------------|
| [Элемент Либраридескриптион (схема библиотеки)](schema-librarydescription.md) |                |



 

## <a name="remarks"></a>Примечания

Имя — это понятное имя библиотеки, отображаемое в проводнике Windows. Имя можно указать в <dllname> формате, как показано <index> в следующем примере.


```
<?xml version="1.0" encoding="UTF-8"?>
<libraryDescription xmlns="http://schemas.microsoft.com/windows/2009/library">
  <name>@shell32.dll,-34575</name>
...
</libraryDescription>
```



## <a name="related-topics"></a>См. также

<dl> <dt>

[Элемент Либраридескриптион (схема библиотеки)](schema-librarydescription.md)
</dt> <dt>

[Схема описания соединителя поиска](../search/search-sconn-desc-schema-entry.md)
</dt> </dl>

 

 
