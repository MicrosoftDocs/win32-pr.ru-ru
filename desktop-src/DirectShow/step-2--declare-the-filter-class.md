---
description: Объявите класс C++, наследующий базовый класс, который выбран в качестве части записи фильтра преобразования.
ms.assetid: 74fbfc16-541f-4f80-a72f-26b67dc09a93
title: Шаг 2. Объявление класса фильтра
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ec3e814802a67185f320345dea2f397188999ecafb9596b9b368a4b6eff8e240
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "118652200"
---
# <a name="step-2-declare-the-filter-class"></a>Шаг 2. Объявление класса фильтра

Это шаг 2 учебника [Создание фильтров преобразования](writing-transform-filters.md).

Начните с объявления класса C++, который наследует базовый класс:


```C++
class CRleFilter : public CTransformFilter
{
    /* Declarations will go here. */
};
```



Каждый из классов фильтров имеет связанные классы закрепления. В зависимости от конкретных потребностей фильтра может потребоваться переопределить классы закрепления. В случае с **ктрансформфилтер** ПИН-коды делегируют большую часть своей работы в фильтр, поэтому вам, скорее всего, не придется переопределять эти ПИН-коды.

Необходимо создать уникальный идентификатор CLSID для фильтра. Можно использовать служебную программу guidgen или uuidgen. никогда не копируйте существующий GUID. Существует несколько способов объявления идентификатора CLSID. В следующем примере используется макрос **define \_ GUID** :


```C++
[RleFilt.h]
// {1915C5C7-02AA-415f-890F-76D94C85AAF1}
DEFINE_GUID(CLSID_RLEFilter, 
0x1915c5c7, 0x2aa, 0x415f, 0x89, 0xf, 0x76, 0xd9, 0x4c, 0x85, 0xaa, 0xf1);

[RleFilt.cpp]
#include <initguid.h>
#include "RleFilt.h"
```



Затем напишите метод-конструктор для фильтра:


```C++
CRleFilter::CRleFilter()
  : CTransformFilter(NAME("My RLE Encoder"), 0, CLSID_RLEFilter)
{ 
   /* Initialize any private variables here. */
}
```



Обратите внимание, что один из параметров конструктора [**ктрансформфилтер**](ctransformfilter-ctransformfilter.md) — это CLSID, определенный ранее.

Далее. [Шаг 3. Поддерживает согласование типов мультимедиа](step-3--support-media-type-negotiation.md).

## <a name="related-topics"></a>Связанные темы

<dl> <dt>

[написание фильтров DirectShow](writing-directshow-filters.md)
</dt> </dl>

 

 



