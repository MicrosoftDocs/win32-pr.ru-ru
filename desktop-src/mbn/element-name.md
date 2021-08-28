---
description: '\/Имя мбнпрофиликст (v4)'
MS-HAID: WWAN\_profile\_v4.element\_Name
MSHAttr:
- PreferredSiteName:MSDN
- PreferredLib:/library/windows/desktop
title: Название
ms.topic: reference
ms.date: 05/31/2018
ms.assetid: 260ae6ea-2386-4473-9376-74c53addd8f3
api_name:
- Name
api_type:
- Schema
api_location: ''
topic_type:
- APIRef
- kbSyntax
ms.openlocfilehash: 728b819b267e17b4624135298554ebaabc9efc65
ms.sourcegitcommit: 4665ebce0c106bdb52eef36e544280b496b6f50b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/26/2021
ms.locfileid: "122988707"
---
# <a name="span-idwwan_profile_v4element_namespanmbnprofileextname-v4"></a><span id="WWAN_profile_v4.element_Name"></span>\/Имя мбнпрофиликст (v4)

Имя профиля. Дополнительные сведения см. в документации по элементу [**имени**](./schema-name-mbnprofile-element.md) v1.

## <a name="element-hierarchy"></a>Иерархия элементов

[\<MBNProfileExt\>](element-mbnprofileext.md)  
&nbsp;&nbsp;**\<Name\>**

[\<ModemDMConfigProfile\>](element-modemdmconfigprofile.md)  
&nbsp;&nbsp;**\<Name\>**

## <a name="syntax"></a>Синтаксис

``` syntax
<Name>

  nameType

</Name>
```

## <a name="span-idattributes_and_elementsspanspan-idattributes_and_elementsspanspan-idattributes_and_elementsspanattributes-and-elements"></a><span id="Attributes_and_Elements"></span><span id="attributes_and_elements"></span><span id="ATTRIBUTES_AND_ELEMENTS"></span>Атрибуты и элементы

### <a name="span-idattributesspanspan-idattributesspanattributes"></a><span id="attributes"></span><span id="ATTRIBUTES"></span>Атрибуты

Отсутствует.

### <a name="span-idchild_elementsspanspan-idchild_elementsspanspan-idchild_elementsspanchild-elements"></a><span id="Child_Elements"></span><span id="child_elements"></span><span id="CHILD_ELEMENTS"></span>Дочерние элементы

Отсутствует.

### <a name="span-idparent_elementsspanspan-idparent_elementsspanparent-elements"></a><span id="parent_elements"></span><span id="PARENT_ELEMENTS"></span>Родительские элементы


| Родительский элемент | Описание | 
|----------------|-------------|
| <a href="element-mbnprofileext.md">MBNProfileExt</a> | <p>Элемент <strong>мбнпрофиликст</strong> является расширением более раннего элемента мбнпрофиле. Он определяет профиль мобильного широкополосного подключения с более широким набором параметров, чем элемент Мбнпрофиле.</p><p>В профиле может быть несколько элементов Мбнпрофиликст, описывающих параметры профиля для определенного набора условий. Используйте дочерний элемент <a href="element-profileconditionedon.md"><strong>профилекондитионедон</strong></a> из <strong>мбнпрофиликст</strong> , чтобы указать, какие операционные условия делают определенный профиль активным.</p> | 
| <a href="element-modemdmconfigprofile.md">ModemDMConfigProfile</a> | <p>Профиль конфигурации DM для модема.</p> | 


 

## <a name="requirements"></a>Требования


| Требование | Применение |
|------------|----------|
| <p>Пространство имен</p> | <p>https://www.microsoft.com/networking/WWAN/profile/v4</p> | 


 

 
