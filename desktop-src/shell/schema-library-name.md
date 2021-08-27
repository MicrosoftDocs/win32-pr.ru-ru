---
description: '&lt;Элемент Name &gt; указывает имя этой библиотеки. Этот элемент является обязательным и не имеет атрибутов или дочерних элементов.'
ms.assetid: 1F433405-5943-4579-BDAD-423C4E1A6E76
title: Элемент Name (схема библиотеки)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6d32b6d929a58f19cc2b87a79af846d22fc0ebda
ms.sourcegitcommit: 61a4c522182aa1cacbf5669683d9570a3bf043b2
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/26/2021
ms.locfileid: "122880860"
---
# <a name="name-element-library-schema"></a>Элемент Name (схема библиотеки)

&lt;Элемент Name &gt; указывает имя этой библиотеки. Этот элемент является обязательным и не имеет атрибутов или дочерних элементов.

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



 

## <a name="remarks"></a>Комментарии

имя — это понятное имя библиотеки, отображаемое в Windows Explorer. Имя можно указать в &lt; &gt; формате dllname, &lt; индексе &gt; , как показано в следующем примере.


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

 

 
