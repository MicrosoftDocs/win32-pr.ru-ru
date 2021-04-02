---
description: Управляет отчетами широты и долготы.
ms.assetid: 66025874-32dd-4494-a9ad-12fe3afa60f9
title: Локатиондисп. Латлонгрепортфактори, объект
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- LocationDisp.LatLongReportFactory
api_type:
- COM
api_location: ''
ms.openlocfilehash: 9fad1ca0f4605f1167f9b86b0df5bc8f20e46285
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "103913511"
---
# <a name="locationdisplatlongreportfactory-object"></a>Локатиондисп. Латлонгрепортфактори, объект

\[Объектная модель API расположения доступна для использования в операционных системах, указанных в разделе требования. В последующих версиях он может быть изменен или недоступен. Вместо этого для доступа к расположению с веб-сайта используйте [API географического расположения W3C](/previous-versions/windows/internet-explorer/ie-developer/samples/gg589513(v=vs.85)). Чтобы получить доступ к расположению из классического приложения, используйте API [**Windows. Devices. Географическое расположение**](/uwp/api/Windows.Devices.Geolocation) .\]

Управляет отчетами широты и долготы.

## <a name="members"></a>Элементы

Объект **локатиондисп. латлонгрепортфактори** имеет следующие типы членов:

-   [Методы](#methods)
-   [Свойства](#properties)

### <a name="methods"></a>Методы

Объект **локатиондисп. латлонгрепортфактори** содержит следующие методы.



| Метод                                                                                       | Описание                                                                                   |
|:---------------------------------------------------------------------------------------------|:----------------------------------------------------------------------------------------------|
| [**листенфоррепортс**](locationdisp-latlongreportfactory-listenforreports.md)               | Запрашивает события отчета широты и долготы.<br/>                                         |
| [**рекуестпермиссионс**](locationdisp-latlongreportfactory-requestpermissions.md)           | Открывает диалоговое окно системы, в котором запрашиваются разрешения пользователя для устройств с поддержкой расположения.<br/> |
| [**стоплистенингфоррепортс**](/previous-versions/windows/desktop/legacy/dd317718(v=vs.85)) | Отменяет запросы на события отчета широты и долготы.<br/>                             |



 

### <a name="properties"></a>Свойства

Объект **локатиондисп. латлонгрепортфактори** имеет следующие свойства.



| Свойство                                                                                | Тип доступа           | Описание                                                                                      |
|:----------------------------------------------------------------------------------------|:----------------------|:-------------------------------------------------------------------------------------------------|
| [**десиредаккураци**](locationdisp-latlongreportfactory-desiredaccuracy.md)<br/> | Чтение/запись<br/> | Текущее значение требуемой точности.<br/>                                                   |
| [**латлонгрепорт**](locationdisp-latlongreportfactory-latlongreport.md)<br/>     | Только для чтения<br/>  | Текущий [**локатиондисп. дисплатлонгрепорт**](locationdisp-displatlongreport.md).<br/> |
| [**репортинтервал**](locationdisp-latlongreportfactory-reportinterval.md)<br/>   | Чтение/запись<br/> | Текущий интервал событий для отчета широты и долготы в миллисекундах.<br/>                 |
| [**Состояние**](locationdisp-latlongreportfactory-status.md)<br/>                   | Только для чтения<br/>  | Текущее состояние отчета.<br/>                                                            |



 

## <a name="examples"></a>Примеры

В следующем примере кода показано, как создать этот объект в HTML-коде.


```
<object id="latlongfactory" 
    classid="clsid:9DCC3CC8-8609-4863-BAD4-03601F4C65E8"
    type="application/x-oleobject">
</object>
```



В следующем примере кода показано, как создать этот объект в JScript с помощью сервера сценариев Windows.


```JScript
var latlongfactory = WScript.CreateObject("LocationDisp.LatLongReportFactory");
```



В следующем примере кода показано, как создать этот объект в VBScript с помощью сервера сценариев Windows.


```VB
Dim latlongfactory
Set latlongfactory = WScript.CreateObject("LocationDisp.LatLongReportFactory")
```



## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------------------------|--------------------------------------------|
| Минимальная версия клиента<br/> | \[Только классические приложения Windows 7\]<br/> |
| Минимальная версия сервера<br/> | Ни одна версия не поддерживается<br/>                  |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[**Локатиондисп. Дисплатлонгрепорт**](locationdisp-displatlongreport.md)
</dt> </dl>

 

