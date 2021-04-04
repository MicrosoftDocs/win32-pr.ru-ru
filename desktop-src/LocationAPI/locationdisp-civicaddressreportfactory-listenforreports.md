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
ms.openlocfilehash: 02315f8b2f7fced76c3d0d1330df246af6bad4b4
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "103999599"
---
# <a name="locationdispcivicaddressreportfactorylistenforreports-method"></a>Локатиондисп. Цивикаддрессрепортфактори. Листенфоррепортс, метод

\[Объектная модель API расположения доступна для использования в операционных системах, указанных в разделе требования. В последующих версиях он может быть изменен или недоступен. Вместо этого для доступа к расположению с веб-сайта используйте [API географического расположения W3C](/previous-versions/windows/internet-explorer/ie-developer/samples/gg589513(v=vs.85)). Чтобы получить доступ к расположению из классического приложения, используйте API [**Windows. Devices. Географическое расположение**](/uwp/api/Windows.Devices.Geolocation) .\]

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

## <a name="remarks"></a>Комментарии

Поставщик расположения не требуется для предоставления точности, которую вы запрашиваете. Прочитайте значение свойства [**репортинтервал**](locationdisp-civicaddressreportfactory-reportinterval.md) , чтобы определить значение параметра интервала true Report.

## <a name="examples"></a>Примеры

Пример использования этого метода см. в разделе [прослушивание событий административного адреса](/uwp/api/Windows.Devices.Geolocation).

## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------------------------|------------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | \[Только классические приложения Windows 7\]<br/>                                               |
| Минимальная версия сервера<br/> | Ни одна версия не поддерживается<br/>                                                                |
| Header<br/>                   | <dl> <dt>Локатионапи. h</dt> </dl> |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[**Событие НевЦивикаддрессрепорт**](newcivicaddressreport.md)
</dt> </dl>

 

