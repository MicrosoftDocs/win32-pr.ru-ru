---
description: Поставщик
MS-HAID: WWAN\_profile\_v4.element\_Provider
MSHAttr:
- PreferredSiteName:MSDN
- PreferredLib:/library/windows/desktop
title: Поставщик
ms.topic: reference
ms.date: 05/31/2018
ms.assetid: a701c4dd-967f-4f03-ada4-d34059f5a1e4
api_name:
- Provider
api_type:
- Schema
api_location: ''
topic_type:
- APIRef
- kbSyntax
ms.openlocfilehash: 73d9018797770f206dbb518685c7b5dac5a6f9af
ms.sourcegitcommit: 4665ebce0c106bdb52eef36e544280b496b6f50b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/26/2021
ms.locfileid: "122982727"
---
# <a name="span-idwwan_profile_v4element_providerspanprovider"></a><span id="WWAN_profile_v4.element_Provider"></span>Поставщик

Указывает одного предпочитаемого поставщика сети в списке поставщиков, которые будут использоваться при роуминге.

Значение этого элемента является экземпляром сложного типа [**ProviderType**](./schema-providertype-complextype.md) на v1.

## <a name="element-hierarchy"></a>Иерархия элементов

[&lt;MBNProfileExt&gt;](element-mbnprofileext.md)  
[&lt;DataRoamingPartners&gt;](element-dataroamingpartners.md)  
**&lt;Поставщик&gt;**

## <a name="syntax"></a>Синтаксис

``` syntax
<Provider>

  providerType

</Provider>
```

## <a name="span-idattributes_and_elementsspanspan-idattributes_and_elementsspanspan-idattributes_and_elementsspanattributes-and-elements"></a><span id="Attributes_and_Elements"></span><span id="attributes_and_elements"></span><span id="ATTRIBUTES_AND_ELEMENTS"></span>Атрибуты и элементы

### <a name="span-idattributesspanspan-idattributesspanattributes"></a><span id="attributes"></span><span id="ATTRIBUTES"></span>Атрибуты

Отсутствует.

### <a name="span-idchild_elementsspanspan-idchild_elementsspanspan-idchild_elementsspanchild-elements"></a><span id="Child_Elements"></span><span id="child_elements"></span><span id="CHILD_ELEMENTS"></span>Дочерние элементы

Отсутствует.

### <a name="span-idparent_elementsspanspan-idparent_elementsspanparent-elements"></a><span id="parent_elements"></span><span id="PARENT_ELEMENTS"></span>Родительские элементы


| Родительский элемент | Описание | 
|----------------|-------------|
| <a href="element-dataroamingpartners.md">DataRoamingPartners</a> | <p>Указывает список предпочтительных поставщиков сети при роуминге.</p><p>Дополнительные сведения см. в документации по элементу <a href="../mbn/schema-dataroamingpartners-mbnprofile-element.md"><strong>датароамингпартнерс</strong></a> v1.</p> | 


 

## <a name="requirements"></a>Требования


| Требование | Применение |
|------------|----------|
| <p>Пространство имен</p> | <p>https://www.microsoft.com/networking/WWAN/profile/v4</p> | 


 

 
