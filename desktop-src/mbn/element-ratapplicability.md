---
description: ратаппликабилити
MS-HAID: WWAN\_profile\_v4.element\_RATApplicability
MSHAttr:
- PreferredSiteName:MSDN
- PreferredLib:/library/windows/desktop
title: ратаппликабилити
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 328aa4978e951da1679582f41c087038869e008e
ms.sourcegitcommit: 61a4c522182aa1cacbf5669683d9570a3bf043b2
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/26/2021
ms.locfileid: "122880474"
---
# <a name="span-idwwan_profile_v4element_ratapplicabilityspanratapplicability"></a><span id="WWAN_profile_v4.element_RATApplicability"></span>ратаппликабилити

Указывает, что этот профиль активен, только если указан тип RAT. В противном случае профиль неприменим и не может использоваться для активации контекста протокола данных пакетов (PDP).

## <a name="element-hierarchy"></a>Иерархия элементов

[&lt;MBNProfileExt&gt;](element-mbnprofileext.md)  
[&lt;профилекондитионедон&gt;](element-profileconditionedon.md)  
**&lt;ратаппликабилити&gt;**

## <a name="syntax"></a>Синтаксис

``` syntax
<RATApplicability>

  "LTE_eHRPD" | "3GPP_LEGACY"

</RATApplicability>
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


 

 



