---
description: Свойство Локатиондисп. Цивикаддрессрепортфактори. status — текущее состояние отчета.
ms.assetid: 3aae0b61-cdaa-4131-b6e1-406813bb1848
title: Локатиондисп. Цивикаддрессрепортфактори. status, свойство
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- LocationDisp.CivicAddressReportFactory.Status
api_type:
- COM
api_location: ''
ms.openlocfilehash: 8ba7d9e26a9741f80caed84d2a4ee4198eae05736aa8dee91019452cc3345ddf
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119693124"
---
# <a name="locationdispcivicaddressreportfactorystatus-property"></a>Локатиондисп. Цивикаддрессрепортфактори. status, свойство

\[Объектная модель API расположения доступна для использования в операционных системах, указанных в разделе требования. В последующих версиях он может быть изменен или недоступен. Вместо этого для доступа к расположению с веб-сайта используйте [API географического расположения W3C](/previous-versions/windows/internet-explorer/ie-developer/samples/gg589513(v=vs.85)). Чтобы получить доступ к расположению из классического приложения, используйте [**Windows. API Devices. Географическое расположение**](/uwp/api/Windows.Devices.Geolocation) .\]

Текущее состояние отчета.

Это свойство доступно только для чтения.

## <a name="syntax"></a>Синтаксис


```JScript
Status = LocationDisp.CivicAddressReportFactory.Status
```



## <a name="property-value"></a>Значение свойства

Это свойство является **числом** только для чтения (длинное целое).



| Состояние                                                                                               | Значение                          |
|------------------------------------------------------------------------------------------------------|----------------------------------|
| <span id="0"></span><dl> <dt>**0**</dt> </dl> | Отчет не поддерживается.<br/> |
| <span id="1"></span><dl> <dt>**1**</dt> </dl> | Ошибка.<br/>                |
| <span id="2"></span><dl> <dt>**2**</dt> </dl> | Доступ запрещен.<br/>        |
| <span id="3"></span><dl> <dt>**3**</dt> </dl> | Инициализация.<br/>         |
| <span id="4"></span><dl> <dt>**4**</dt> </dl> | Выполняется.<br/>              |



 

## <a name="examples"></a>Примеры

Пример использования этого свойства см. в разделе [прослушивание событий административного адреса](/uwp/api/Windows.Devices.Geolocation).

## <a name="requirements"></a>Requirements (Требования)



| Требование | Значение |
|-------------------------------------|--------------------------------------------|
| Минимальная версия клиента<br/> | только Windows 7 \[ настольных приложений\]<br/> |
| Минимальная версия сервера<br/> | Ни одна версия не поддерживается<br/>                  |



 

