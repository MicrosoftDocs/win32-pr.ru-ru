---
description: DataRoamingPartners
MS-HAID: WWAN\_profile\_v4.element\_DataRoamingPartners
MSHAttr:
- PreferredSiteName:MSDN
- PreferredLib:/library/windows/desktop
title: DataRoamingPartners
ms.topic: reference
ms.date: 05/31/2018
ms.assetid: c29edf9c-4e70-4b8f-8c71-0ec8a9fad60d
api_name:
- DataRoamingPartners
api_type:
- Schema
api_location: ''
topic_type:
- APIRef
- kbSyntax
ms.openlocfilehash: f43f2cba06d75aa08a6419c0b39fa08bf898c111
ms.sourcegitcommit: 4665ebce0c106bdb52eef36e544280b496b6f50b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/26/2021
ms.locfileid: "122987097"
---
# <a name="span-idwwan_profile_v4element_dataroamingpartnersspandataroamingpartners"></a><span id="WWAN_profile_v4.element_DataRoamingPartners"></span>DataRoamingPartners

Указывает список предпочтительных поставщиков сети при роуминге.

Дополнительные сведения см. в документации по элементу [**датароамингпартнерс**](./schema-dataroamingpartners-mbnprofile-element.md) v1.

## <a name="element-hierarchy"></a>Иерархия элементов

[&lt;MBNProfileExt&gt;](element-mbnprofileext.md)  
**&lt;DataRoamingPartners&gt;**

## <a name="syntax"></a>Синтаксис

``` syntax
<DataRoamingPartners>

  <!-- Child elements -->
  Provider+

</DataRoamingPartners>
```

### <a name="key"></a>Ключ

`+`   обязательный (один или несколько)

## <a name="span-idattributes_and_elementsspanspan-idattributes_and_elementsspanspan-idattributes_and_elementsspanattributes-and-elements"></a><span id="Attributes_and_Elements"></span><span id="attributes_and_elements"></span><span id="ATTRIBUTES_AND_ELEMENTS"></span>Атрибуты и элементы

### <a name="span-idattributesspanspan-idattributesspanattributes"></a><span id="attributes"></span><span id="ATTRIBUTES"></span>Атрибуты

Отсутствует.

### <a name="span-idchild_elementsspanspan-idchild_elementsspanspan-idchild_elementsspanchild-elements"></a><span id="Child_Elements"></span><span id="child_elements"></span><span id="CHILD_ELEMENTS"></span>Дочерние элементы


| Дочерний элемент | Описание | 
|---------------|-------------|
| <a href="element-provider.md">Поставщик</a> | <p>Указывает одного предпочитаемого поставщика сети в списке поставщиков, которые будут использоваться при роуминге.</p><p>Значение этого элемента является экземпляром сложного типа <a href="../mbn/schema-providertype-complextype.md"><strong>ProviderType</strong></a> на v1.</p> | 


 

### <a name="span-idparent_elementsspanspan-idparent_elementsspanparent-elements"></a><span id="parent_elements"></span><span id="PARENT_ELEMENTS"></span>Родительские элементы


| Родительский элемент | Описание | 
|----------------|-------------|
| <a href="element-mbnprofileext.md">MBNProfileExt</a> | <p>Элемент <strong>мбнпрофиликст</strong> является расширением более раннего элемента мбнпрофиле. Он определяет профиль мобильного широкополосного подключения с более широким набором параметров, чем элемент Мбнпрофиле.</p><p>В профиле может быть несколько элементов Мбнпрофиликст, описывающих параметры профиля для определенного набора условий. Используйте дочерний элемент <a href="element-profileconditionedon.md"><strong>профилекондитионедон</strong></a> из <strong>мбнпрофиликст</strong> , чтобы указать, какие операционные условия делают определенный профиль активным.</p> | 


 

## <a name="requirements"></a>Требования


| Требование | Применение |
|------------|----------|
| <p>Пространство имен</p> | <p>https://www.microsoft.com/networking/WWAN/profile/v4</p> | 


 

 
