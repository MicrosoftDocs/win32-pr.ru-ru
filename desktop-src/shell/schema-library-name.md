---
description: <name>Элемент указывает имя этой библиотеки. Этот элемент является обязательным и не имеет атрибутов или дочерних элементов.
ms.assetid: 1F433405-5943-4579-BDAD-423C4E1A6E76
title: Элемент Name (схема библиотеки)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 179d8b4a1f4358ccb441cc38c6c0765a6dc4d9ade8b3c32a1504be2151cfedaa
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119883944"
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



 

## <a name="remarks"></a>Remarks

имя — это понятное имя библиотеки, отображаемое в Windows Explorer. Имя можно указать в <dllname> формате, как показано <index> в следующем примере.


```
<?xml version="1.0" encoding="UTF-8"?>
<libraryDescription xmlns="http://schemas.microsoft.com/windows/2009/library">
  <name>@shell32.dll,-34575</name>
...
</libraryDescription>
```



## <a name="related-topics"></a>Связанные темы

<dl> <dt>

[Элемент Либраридескриптион (схема библиотеки)](schema-librarydescription.md)
</dt> <dt>

[Схема описания соединителя поиска](../search/search-sconn-desc-schema-entry.md)
</dt> </dl>

 

 
