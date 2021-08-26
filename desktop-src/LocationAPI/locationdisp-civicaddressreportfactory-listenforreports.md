---
description: Запрашивает события об административном адресе.
ms.assetid: cb02f611-7cda-405f-aeee-833b7385a4be
title: Метод Локатиондисп. Цивикаддрессрепортфактори. Листенфоррепортс (Локатионапи. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- LocationDisp.CivicAddressReportFactory.ListenForReports
api_type:
- COM
api_location:
- locationapi.h
ms.openlocfilehash: 218684dcdb1c79b3b1a37517a4369ad492031cae1badfb9f0b16bbb6933289d8
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119979774"
---
# <a name="locationdispcivicaddressreportfactorylistenforreports-method"></a>Локатиондисп. Цивикаддрессрепортфактори. Листенфоррепортс, метод

\[Объектная модель API расположения доступна для использования в операционных системах, указанных в разделе требования. В последующих версиях он может быть изменен или недоступен. Вместо этого для доступа к расположению с веб-сайта используйте [API географического расположения W3C](/previous-versions/windows/internet-explorer/ie-developer/samples/gg589513(v=vs.85)). Чтобы получить доступ к расположению из классического приложения, используйте [**Windows. API Devices. Географическое расположение**](/uwp/api/Windows.Devices.Geolocation) .\]

Запрашивает события об административном адресе.

## <a name="syntax"></a>Синтаксис


```JScript
LocationDisp.CivicAddressReportFactory.ListenForReports(
  requestedReportInterval
)
```



## <a name="parameters"></a>Параметры

<dl> <dt>

*рекуестедрепортинтервал* 
</dt> <dd> Число (**двойное слово**), представляющее запрошенное время между событиями отчета об административном адресе (в миллисекундах). См. заметки.</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Этот метод не возвращает значение.

## <a name="remarks"></a>Remarks

Поставщик расположения не требуется для предоставления точности, которую вы запрашиваете. Прочитайте значение свойства [**репортинтервал**](locationdisp-civicaddressreportfactory-reportinterval.md) , чтобы определить значение параметра интервала true Report.

## <a name="examples"></a>Примеры

Пример использования этого метода см. в разделе [прослушивание событий административного адреса](/uwp/api/Windows.Devices.Geolocation).

## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------------------------|------------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | только Windows 7 \[ настольных приложений\]<br/>                                               |
| Минимальная версия сервера<br/> | Ни одна версия не поддерживается<br/>                                                                |
| Заголовок<br/>                   | <dl> <dt>Локатионапи. h</dt> </dl> |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[**Событие НевЦивикаддрессрепорт**](newcivicaddressreport.md)
</dt> </dl>

 

