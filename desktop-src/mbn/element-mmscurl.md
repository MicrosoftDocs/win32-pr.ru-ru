---
description: MmscUrl
MS-HAID: WWAN\_profile\_v4.element\_MmscUrl
MSHAttr:
- PreferredSiteName:MSDN
- PreferredLib:/library/windows/desktop
title: MmscUrl
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: eab913845a12f8a54c9cbc4f65de5208f7661555
ms.sourcegitcommit: 4665ebce0c106bdb52eef36e544280b496b6f50b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/26/2021
ms.locfileid: "122986277"
---
# <a name="span-idwwan_profile_v4element_mmscurlspanmmscurl"></a><span id="WWAN_profile_v4.element_MmscUrl"></span>ммскурл

Указывает URL-адрес сервера ММСК для устройства. Необязательный элемент.

## <a name="element-hierarchy"></a>Иерархия элементов

[&lt;MBNProfileExt&gt;](element-mbnprofileext.md)  
[&lt;ммсконфигуратион&gt;](element-mmsconfiguration.md)  
**&lt;MmscUrl&gt;**

## <a name="syntax"></a>Синтаксис

``` syntax
<MmscUrl>

  anyURI

</MmscUrl>
```

## <a name="span-idattributes_and_elementsspanspan-idattributes_and_elementsspanspan-idattributes_and_elementsspanattributes-and-elements"></a><span id="Attributes_and_Elements"></span><span id="attributes_and_elements"></span><span id="ATTRIBUTES_AND_ELEMENTS"></span>Атрибуты и элементы

### <a name="span-idattributesspanspan-idattributesspanattributes"></a><span id="attributes"></span><span id="ATTRIBUTES"></span>Атрибуты

Отсутствует.

### <a name="span-idchild_elementsspanspan-idchild_elementsspanspan-idchild_elementsspanchild-elements"></a><span id="Child_Elements"></span><span id="child_elements"></span><span id="CHILD_ELEMENTS"></span>Дочерние элементы

Отсутствует.

### <a name="span-idparent_elementsspanspan-idparent_elementsspanparent-elements"></a><span id="parent_elements"></span><span id="PARENT_ELEMENTS"></span>Родительские элементы


| Родительский элемент | Описание | 
|----------------|-------------|
| <a href="element-mmsconfiguration.md">ммсконфигуратион</a> | <p>Сведения о конфигурации для службы обмена сообщениями мультимедиа (MMS).</p><p>Помимо настройки элементов конфигурации в этом элементе, профиль MMS должен иметь следующие параметры.</p><ul><li>Его элемент <a href="element-name.md"><strong>Name</strong></a> должен содержать уникальное для всей системы имя.</li><li>Его <a href="../mbn/schema-profilecreationtype-mbnprofile-element.md"><strong>профилекреатионтипе</strong></a> должен быть установлен в значение <strong>усерпровисионед</strong>.</li><li>Его <a href="/windows/desktop/api/mbnapi/nf-mbnapi-imbnsubscriberinformation-get_simiccid"><strong>симикЦид</strong></a> должен содержать ICCID SIM-карты, для которой предназначен этот профиль.</li><li>Его <a href="../mbn/schema-connectionmode-mbnprofile-element.md"><strong>ConnectionMode</strong></a> должен быть установлен в значение " <strong>вручную</strong>".</li><li>Его <a href="element-purposegroupguid.md"><strong>пурпосеграупгуид</strong></a> должен содержать GUID для группы целей MMS.</li><li>Его <a href="/previous-versions/windows/desktop/legacy/mt156987(v=vs.85)"><strong>исаддитионалпдпконтекстпрофиле</strong></a> должен быть установлен в <strong>значение true</strong>.</li></ul> | 


 

## <a name="requirements"></a>Требования


| Требование | Применение |
|------------|----------|
| <p>Пространство имен</p> | <p>https://www.microsoft.com/networking/WWAN/profile/v4</p> | 


 

 
