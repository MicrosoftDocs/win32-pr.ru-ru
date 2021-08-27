---
description: Свойство Локатиондисп. Дисплатлонгрепорт. timestamp — Дата и время создания отчета.
ms.assetid: 3b8036aa-499c-4baf-bcc4-5b6c3f54eb7b
title: Локатиондисп. Дисплатлонгрепорт. timestamp, свойство
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- LocationDisp.DispLatLongReport.Timestamp
api_type:
- COM
api_location: ''
ms.openlocfilehash: 02b1d2bc344ec954f8c309e2370755464857fd754b16f6664760f9df4e0e5f54
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "120129914"
---
# <a name="locationdispdisplatlongreporttimestamp-property"></a>Локатиондисп. Дисплатлонгрепорт. timestamp, свойство

\[Объектная модель API расположения доступна для использования в операционных системах, указанных в разделе требования. В последующих версиях он может быть изменен или недоступен. Вместо этого для доступа к расположению с веб-сайта используйте [API географического расположения W3C](/previous-versions/windows/internet-explorer/ie-developer/samples/gg589513(v=vs.85)). Чтобы получить доступ к расположению из классического приложения, используйте [**Windows. API Devices. Географическое расположение**](/uwp/api/Windows.Devices.Geolocation) .\]

Дата и время создания отчета.

Это свойство доступно только для чтения.

## <a name="syntax"></a>Синтаксис


```JScript
Timestamp = LocationDisp.DispLatLongReport.Timestamp
```



## <a name="property-value"></a>Значение свойства

Это свойство является **датой** только для чтения. Временные метки задаются в формате UTC.

## <a name="remarks"></a>Remarks

обратите внимание, что для языков сценариев, таких как Microsoft JScript, может потребоваться выполнить преобразование в другие форматы времени при отображении меток времени в виде строк.

## <a name="examples"></a>Примеры

Пример использования этого свойства см. [в примере простого отчета LatLong](/uwp/api/Windows.Devices.Geolocation).

## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------------------------|--------------------------------------------|
| Минимальная версия клиента<br/> | только Windows 7 \[ настольных приложений\]<br/> |
| Минимальная версия сервера<br/> | Ни одна версия не поддерживается<br/>                  |



 

