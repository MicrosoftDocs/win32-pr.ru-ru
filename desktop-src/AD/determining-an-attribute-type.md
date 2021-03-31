---
title: Определение типа атрибута
description: Атрибут systemFlags объекта attributeSchema содержит набор флагов, которые указывают различные значения качества объекта атрибута, например, создается или не реплицируется атрибут.
ms.assetid: 58f44ea4-ecbd-4650-b366-37b05a975c68
ms.tgt_platform: multiple
keywords:
- Определение типа атрибута Active Directory
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b64b4d8b0ae5d6cbac38c9c44ed8e4a7aa5d5f57
ms.sourcegitcommit: 803f3ccd65bdefe36bd851b9c6e7280be9489016
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/17/2020
ms.locfileid: "104069782"
---
# <a name="determining-an-attribute-type"></a>Определение типа атрибута

Атрибут [**systemFlags**](/windows/desktop/ADSchema/a-systemflags) объекта [**attributeSchema**](/windows/desktop/ADSchema/c-attributeschema) содержит набор флагов, которые указывают различные значения качества объекта атрибута, например, создается или не реплицируется атрибут. В следующей таблице перечислены флаги атрибута **systemFlags** , влияющие на тип хранения атрибута. 

| Значение флага | Описание                                                                                                          |
|------------|----------------------------------------------------------------------------------------------------------------------|
| 0x00000001 | Если этот флаг имеется в атрибуте [**systemFlags**](/windows/desktop/ADSchema/a-systemflags) , то этот атрибут не реплицируется. |
| 0x00000004 | Если этот флаг имеется в атрибуте [**systemFlags**](/windows/desktop/ADSchema/a-systemflags) , то создается атрибут.    |



 

Можно создать строку запроса, которая может использоваться для запроса созданных или нереплицируемых атрибутов. Например, следующая строка запроса находит все нереплицированные объекты [**attributeSchema**](/windows/desktop/ADSchema/c-attributeschema) . Имейте в виду, что строка запроса требует десятичного эквивалента значения, а не шестнадцатеричного эквивалента значения. Дополнительные сведения о идентификаторе OID правила сопоставления, используемом этой строкой запроса, см. [в разделе как указать значения для сравнения](how-to-specify-comparison-values.md).


```C++
(&(objectCategory=attributeSchema)(systemFlags:1.2.840.113556.1.4.804:=1))
```



Атрибут [**searchFlags**](/windows/desktop/ADSchema/a-searchflags) объекта [**attributeSchema**](/windows/desktop/ADSchema/c-attributeschema) каждого атрибута определяет, индексируется ли атрибут. индексированный атрибут имеет значение 1, неиндексированный атрибут имеет значение 0. Например, следующая строка запроса находит объекты **attributeSchema** , представляющие индексированные атрибуты.


```C++
(&(objectCategory=attributeSchema)(searchFlags=1))
```



Атрибут [**исмемберофпартиалаттрибутесет**](/windows/desktop/ADSchema/a-ismemberofpartialattributeset) объекта [**attributeSchema**](/windows/desktop/ADSchema/c-attributeschema) каждого атрибута определяет, реплицируется ли атрибут в глобальный каталог. Этот атрибут имеет значение **true** , если атрибут является членом глобального каталога, или **значение false** , если атрибуты не находятся в глобальном каталоге. Например, следующая строка запроса выполняет поиск объектов **attributeSchema** , которые реплицируются в глобальный каталог.


```C++
(&(objectCategory=attributeSchema)(isMemberOfPartialAttributeSet=TRUE))
```



 

 