---
description: Запрашивает события отчета широты и долготы.
ms.assetid: c26a388b-e042-43da-a220-e3ecfcbd03a8
title: Метод Локатиондисп. Латлонгрепортфактори. Листенфоррепортс (Локатионапи. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- LocationDisp.LatLongReportFactory.ListenForReports
api_type:
- COM
api_location:
- locationapi.h
ms.openlocfilehash: 7e822595339fa499aaf469336ca3580acb2815bc
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "103814808"
---
# <a name="locationdisplatlongreportfactorylistenforreports-method"></a>Локатиондисп. Латлонгрепортфактори. Листенфоррепортс, метод

\[Объектная модель API расположения доступна для использования в операционных системах, указанных в разделе требования. В последующих версиях он может быть изменен или недоступен. Вместо этого для доступа к расположению с веб-сайта используйте [API географического расположения W3C](/previous-versions/windows/internet-explorer/ie-developer/samples/gg589513(v=vs.85)). Чтобы получить доступ к расположению из классического приложения, используйте API [**Windows. Devices. Географическое расположение**](/uwp/api/Windows.Devices.Geolocation) .\]

Запрашивает события отчета широты и долготы.

## <a name="syntax"></a>Синтаксис


```JScript
LocationDisp.LatLongReportFactory.ListenForReports(
  requestedReportInterval
)
```



## <a name="parameters"></a>Параметры

<dl> <dt>

*рекуестедрепортинтервал* 
</dt> <dd> Число (**двойное слово**), представляющее запрошенное время между событиями отчета широты и долготы в миллисекундах. См. заметки.</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Этот метод не возвращает значение.

## <a name="remarks"></a>Комментарии

Поставщик расположения не требуется для предоставления отчетов на запрошенный интервал. Прочитайте значение свойства [**репортинтервал**](locationdisp-latlongreportfactory-reportinterval.md) , чтобы определить значение параметра интервала true Report.

## <a name="examples"></a>Примеры

Пример использования этого метода см. в разделе [Listening for LatLong Report Events](/uwp/api/Windows.Devices.Geolocation).

## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------------------------|------------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | \[Только классические приложения Windows 7\]<br/>                                               |
| Минимальная версия сервера<br/> | Ни одна версия не поддерживается<br/>                                                                |
| Header<br/>                   | <dl> <dt>Локатионапи. h</dt> </dl> |



 

