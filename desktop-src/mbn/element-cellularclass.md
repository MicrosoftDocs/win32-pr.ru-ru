---
description: целлуларкласс
MS-HAID: WWAN\_profile\_v4.element\_CellularClass
MSHAttr:
- PreferredSiteName:MSDN
- PreferredLib:/library/windows/desktop
title: целлуларкласс
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6d8f0fbbd2ab8548eec9550f83fc15d1461ed56a
ms.sourcegitcommit: 9b5faa61c38b2d0c432b7f2dbee8c127b0e28a7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/19/2021
ms.locfileid: "122474780"
---
# <a name="span-idwwan_profile_v4element_cellularclassspancellularclass"></a><span id="WWAN_profile_v4.element_CellularClass"></span>целлуларкласс

Указывает, что этот профиль активен, только если указан текущий класс сотовой связи. В противном случае профиль неприменим и не может использоваться для активации контекста протокола данных пакетов (PDP).

## <a name="element-hierarchy"></a>Иерархия элементов

[<MBNProfileExt>](element-mbnprofileext.md)  
[<ProfileConditionedOn>](element-profileconditionedon.md)  
**<CellularClass>**

## <a name="syntax"></a>Синтаксис

``` syntax
<CellularClass>

  "3GPP" | "3GPP2"

</CellularClass>
```

## <a name="span-idattributes_and_elementsspanspan-idattributes_and_elementsspanspan-idattributes_and_elementsspanattributes-and-elements"></a><span id="Attributes_and_Elements"></span><span id="attributes_and_elements"></span><span id="ATTRIBUTES_AND_ELEMENTS"></span>Атрибуты и элементы

### <a name="span-idattributesspanspan-idattributesspanattributes"></a><span id="attributes"></span><span id="ATTRIBUTES"></span>Атрибуты

Нет.

### <a name="span-idchild_elementsspanspan-idchild_elementsspanspan-idchild_elementsspanchild-elements"></a><span id="Child_Elements"></span><span id="child_elements"></span><span id="CHILD_ELEMENTS"></span>Дочерние элементы

Нет.

### <a name="span-idparent_elementsspanspan-idparent_elementsspanparent-elements"></a><span id="parent_elements"></span><span id="PARENT_ELEMENTS"></span>Родительские элементы


| Родительский элемент | Описание | 
|----------------|-------------|
| <a href="element-profileconditionedon.md">профилекондитионедон</a> | <p>Указывает условия, которые должны быть удовлетворены для применения профиля.</p><p>Этот элемент является новым для v4. Он позволяет указать несколько профилей, которые применяются в различных условиях, а также для автоматического использования соответствующего профиля. Этот элемент является необязательным. Если его не указать, профиль всегда будет применяться в соответствии с указанными условиями.</p> | 


 

## <a name="requirements"></a>Требования


| | | <p>Пространство имен</p> | <p>https://www.microsoft.com/networking/WWAN/profile/v4</p> | 


 

 



