---
description: Текущее состояние отчета.
ms.assetid: bcdf76b5-88c4-481a-89ac-2b9558cecfc0
title: Локатиондисп. Латлонгрепортфактори. status, свойство
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- LocationDisp.LatLongReportFactory.Status
api_type:
- COM
api_location: ''
ms.openlocfilehash: c32f1e58c5c519bdbdf797f81f11a449bfb3dc1d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "104346032"
---
# <a name="locationdisplatlongreportfactorystatus-property"></a>Локатиондисп. Латлонгрепортфактори. status, свойство

\[Объектная модель API расположения доступна для использования в операционных системах, указанных в разделе требования. В последующих версиях он может быть изменен или недоступен. Вместо этого для доступа к расположению с веб-сайта используйте [API географического расположения W3C](/previous-versions/windows/internet-explorer/ie-developer/samples/gg589513(v=vs.85)). Чтобы получить доступ к расположению из классического приложения, используйте API [**Windows. Devices. Географическое расположение**](/uwp/api/Windows.Devices.Geolocation) .\]

Текущее состояние отчета.

Это свойство доступно только для чтения.

## <a name="syntax"></a>Синтаксис


```JScript
Status = LocationDisp.LatLongReportFactory.Status
```



## <a name="property-value"></a>Значение свойства

Это свойство является **числом** только для чтения (длинное целое).



| Состояние                                                                                               | Значение                          |
|------------------------------------------------------------------------------------------------------|----------------------------------|
| <span id="0"></span><dl> <dt>**0**</dt> </dl> | Отчет не поддерживается.<br/> |
| <span id="1"></span><dl> <dt>**1**</dt> </dl> | Ошибка.<br/>                |
| <span id="2"></span><dl> <dt>**2**</dt> </dl> | Доступ запрещен.<br/>        |
| <span id="3"></span><dl> <dt>**3-5**</dt> </dl> | Инициализация.<br/>         |
| <span id="4"></span><dl> <dt>**четырех**</dt> </dl> | Выполняется.<br/>              |



 

## <a name="examples"></a>Примеры

Пример использования этого свойства см. в разделе [Listening for LatLong Report Events](/uwp/api/Windows.Devices.Geolocation).

## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------------------------|--------------------------------------------|
| Минимальная версия клиента<br/> | \[Только классические приложения Windows 7\]<br/> |
| Минимальная версия сервера<br/> | Ни одна версия не поддерживается<br/>                  |



 

