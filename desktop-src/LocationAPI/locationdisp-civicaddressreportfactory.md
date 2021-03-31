---
description: Управляет отчетами об административном адресе.
ms.assetid: 46c2d001-409a-4a0a-9006-1c2c9d327c13
title: Локатиондисп. Цивикаддрессрепортфактори, объект
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- LocationDisp.CivicAddressReportFactory
api_type:
- COM
api_location: ''
ms.openlocfilehash: 451bb21822d1b56e4c7a45f1587df04761b67690
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "103816064"
---
# <a name="locationdispcivicaddressreportfactory-object"></a>Локатиондисп. Цивикаддрессрепортфактори, объект

\[Объектная модель API расположения доступна для использования в операционных системах, указанных в разделе требования. В последующих версиях он может быть изменен или недоступен. Вместо этого для доступа к расположению с веб-сайта используйте [API географического расположения W3C](/previous-versions/windows/internet-explorer/ie-developer/samples/gg589513(v=vs.85)). Чтобы получить доступ к расположению из классического приложения, используйте API [**Windows. Devices. Географическое расположение**](/uwp/api/Windows.Devices.Geolocation) .\]

Управляет отчетами об административном адресе.

## <a name="members"></a>Элементы

Объект **локатиондисп. Цивикаддрессрепортфактори** имеет следующие типы членов:

-   [Методы](#methods)
-   [Свойства](#properties)

### <a name="methods"></a>Методы

Объект **локатиондисп. Цивикаддрессрепортфактори** содержит следующие методы.



| Метод                                                                                            | Описание                                                                                   |
|:--------------------------------------------------------------------------------------------------|:----------------------------------------------------------------------------------------------|
| [**листенфоррепортс**](locationdisp-civicaddressreportfactory-listenforreports.md)               | Запрашивает события об административном адресе.<br/>                                              |
| [**рекуестпермиссионс**](locationdisp-civicaddressreportfactory-requestpermissions.md)           | Открывает диалоговое окно системы, в котором запрашиваются разрешения пользователя для устройств с поддержкой расположения.<br/> |
| [**стоплистенингфоррепортс**](locationdisp-civicaddressreportfactory-stoplisteningforreports.md) | Отменяет запросы событий для отчетов об административном адресе.<br/>                                       |



 

### <a name="properties"></a>Свойства

Объект **локатиондисп. Цивикаддрессрепортфактори** имеет следующие свойства.



| Свойство                                                                                        | Тип доступа           | Описание                                                                                                |
|:------------------------------------------------------------------------------------------------|:----------------------|:-----------------------------------------------------------------------------------------------------------|
| [**Цивикаддрессрепорт**](locationdisp-dispcivicaddressreport-civicaddressreport.md)<br/> | Только для чтения<br/>  | Текущий [**локатиондисп. диспЦивикаддрессрепорт**](locationdisp-dispcivicaddressreport.md).<br/> |
| [**десиредаккураци**](locationdisp-civicaddressreportfactory-desiredaccuracy.md)<br/>    | Чтение/запись<br/> | Текущее значение требуемой точности.<br/>                                                           |
| [**репортинтервал**](locationdisp-civicaddressreportfactory-reportinterval.md)<br/>      | Чтение/запись<br/> | Текущий интервал событий для отчета об административном адресе в миллисекундах.<br/>                                |
| [**Состояние**](locationdisp-civicaddressreportfactory-status.md)<br/>                      | Только для чтения<br/>  | Текущее состояние отчета.<br/>                                                                      |



 

## <a name="examples"></a>Примеры

В следующем примере кода показано, как создать этот объект в HTML-коде.


```Text
<object id="civicfactory" 
    classid="clsid:2A11F42C-3E81-4ad4-9CBE-45579D89671A"
    type="application/x-oleobject">
</object>
```



В следующем примере кода показано, как создать этот объект в JScript с помощью сервера сценариев Windows.


```JScript
var civicfactory = WScript.CreateObject("LocationDisp.CivicAddressReportFactory");
```



В следующем примере кода показано, как создать этот объект в VBScript с помощью сервера сценариев Windows.


```VB
Dim civicfactory
Set civicfactory = WScript.CreateObject("LocationDisp.CivicAddressReportFactory")
```



## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------------------------|--------------------------------------------|
| Минимальная версия клиента<br/> | \[Только классические приложения Windows 7\]<br/> |
| Минимальная версия сервера<br/> | Ни одна версия не поддерживается<br/>                  |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[**Локатиондисп. Цивикаддрессрепорт**](locationdisp-dispcivicaddressreport.md)
</dt> </dl>

 

