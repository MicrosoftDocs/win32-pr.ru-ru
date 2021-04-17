---
description: Представляет отчет об административном адресе.
ms.assetid: 7c6e790f-0150-4ea8-9583-df633ebf035d
title: Локатиондисп. ДиспЦивикаддрессрепорт, объект
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- LocationDisp.DispCivicAddressReport
api_type:
- COM
api_location: ''
ms.openlocfilehash: 2a2a96f3d0c2a1fe8e3ac78e5db67ded031a4aa8
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "105673942"
---
# <a name="locationdispdispcivicaddressreport-object"></a>Локатиондисп. ДиспЦивикаддрессрепорт, объект

\[Объектная модель API расположения доступна для использования в операционных системах, указанных в разделе требования. В последующих версиях он может быть изменен или недоступен. Вместо этого для доступа к расположению с веб-сайта используйте [API географического расположения W3C](/previous-versions/windows/internet-explorer/ie-developer/samples/gg589513(v=vs.85)). Чтобы получить доступ к расположению из классического приложения, используйте API [**Windows. Devices. Географическое расположение**](/uwp/api/Windows.Devices.Geolocation) .\]

Представляет отчет об административном адресе.

## <a name="members"></a>Элементы

Объект **локатиондисп. диспЦивикаддрессрепорт** имеет следующие типы членов:

-   [Свойства](#properties)

### <a name="properties"></a>Свойства

Объект **локатиондисп. диспЦивикаддрессрепорт** имеет следующие свойства.



| Свойство                                                                              | Тип доступа          | Описание                                                 |
|:--------------------------------------------------------------------------------------|:---------------------|:------------------------------------------------------------|
| [**AddressLine1**](locationdisp-dispcivicaddressreport-addressline1.md)<br/>   | Только для чтения<br/> | Первая строка почтового адреса.<br/>              |
| [**AddressLine2**](locationdisp-dispcivicaddressreport-addressline2.md)<br/>   | Только для чтения<br/> | Вторая строка почтового адреса.<br/>             |
| [**Город**](locationdisp-dispcivicaddressreport-city.md)<br/>                   | Только для чтения<br/> | Название города.<br/>                                   |
| [**Страна**](locationdisp-civicaddressreport-countryregion.md)<br/>     | Только для чтения<br/> | Название страны или региона.<br/>                      |
| [**детаиллевел**](locationdisp-dispcivicaddressreport-detaillevel.md)<br/>     | Только для чтения<br/> | Уровень детализации для отчета.<br/>                 |
| [**Почтовый**](locationdisp-dispcivicaddressreport-postalcode.md)<br/>       | Только для чтения<br/> | Почтовый индекс.<br/>                                 |
| [**StateProvince**](locationdisp-dispcivicaddressreport-stateprovince.md)<br/> | Только для чтения<br/> | Название штата или Республики.<br/>                      |
| [**Отметка времени**](locationdisp-dispcivicaddressreport-timestamp.md)<br/>         | Только для чтения<br/> | Дата и время создания отчета.<br/> |



 

## <a name="remarks"></a>Комментарии

Этот объект можно получить с помощью свойства [**Цивикаддрессрепорт**](locationdisp-dispcivicaddressreport-civicaddressreport.md) объекта [**Цивикаддрессрепортфактори**](locationdisp-civicaddressreportfactory.md) . Этот объект можно получить с помощью события [**невЦивикаддрессрепорт**](newcivicaddressreport.md) .

## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------------------------|--------------------------------------------|
| Минимальная версия клиента<br/> | \[Только классические приложения Windows 7\]<br/> |
| Минимальная версия сервера<br/> | Ни одна версия не поддерживается<br/>                  |



 

