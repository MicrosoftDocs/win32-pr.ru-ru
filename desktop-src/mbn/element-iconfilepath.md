---
description: иконфилепас
MS-HAID: WWAN\_profile\_v4.element\_ICONFilePath
MSHAttr:
- PreferredSiteName:MSDN
- PreferredLib:/library/windows/desktop
title: иконфилепас
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: bdb21e822f5f2418ad7d08f7d8f8edfff4f93b6a
ms.sourcegitcommit: 4665ebce0c106bdb52eef36e544280b496b6f50b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/26/2021
ms.locfileid: "122988827"
---
# <a name="span-idwwan_profile_v4element_iconfilepathspaniconfilepath"></a><span id="WWAN_profile_v4.element_ICONFilePath"></span>иконфилепас

Путь к файлу значка для соединения. Пользовательский интерфейс подключения операционной системы отображает значок, когда подключение устанавливается с помощью этого профиля.

Дополнительные сведения об использовании этого элемента см. в документации по версии 1 для [**иконфилепас**](./schema-iconfilepath-mbnprofile-element.md).

## <a name="element-hierarchy"></a>Иерархия элементов

[&lt;MBNProfileExt&gt;](element-mbnprofileext.md)  
**&lt;иконфилепас&gt;**

## <a name="syntax"></a>Синтаксис

``` syntax
<ICONFilePath>

  iconFileType

</ICONFilePath>
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


 

## <a name="requirements"></a>Требования


| Требование | Применение |
|------------|----------|
| <p>Пространство имен</p> | <p>https://www.microsoft.com/networking/WWAN/profile/v4</p> | 


 

 
