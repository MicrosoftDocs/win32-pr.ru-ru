---
description: Происходит при формировании нового отчета широты/долготы.
ms.assetid: 2b1a25a1-ccd6-43f8-979b-c2d414d666a2
title: Событие Невлатлонгрепорт
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- NewLatLongReport
api_type:
- COM
api_location: ''
ms.openlocfilehash: ea305d17169b71d183a8d453e9885d8de878b026
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "105674507"
---
# <a name="newlatlongreport-event"></a>Событие Невлатлонгрепорт

\[Объектная модель API расположения доступна для использования в операционных системах, указанных в разделе требования. В последующих версиях он может быть изменен или недоступен. Вместо этого для доступа к расположению с веб-сайта используйте [API географического расположения W3C](/previous-versions/windows/internet-explorer/ie-developer/samples/gg589513(v=vs.85)). Чтобы получить доступ к расположению из классического приложения, используйте API [**Windows. Devices. Географическое расположение**](/uwp/api/Windows.Devices.Geolocation) .\]

Происходит при формировании нового отчета широты/долготы.

## <a name="syntax"></a>Синтаксис


```JScript
.NewLatLongReport(
  newReport
)
```



## <a name="parameters"></a>Параметры

<dl> <dt>

*неврепорт* 
</dt> <dd>

Новый объект [**локатиондисп. дисплатлонгрепорт**](locationdisp-displatlongreport.md) .

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Это событие не возвращает значение.

## <a name="examples"></a>Примеры

Пример использования этого события см. в разделе [Listening for LatLong Reports Events](/uwp/api/Windows.Devices.Geolocation).

## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------------------------|--------------------------------------------|
| Минимальная версия клиента<br/> | \[Только классические приложения Windows 7\]<br/> |
| Минимальная версия сервера<br/> | Ни одна версия не поддерживается<br/>                  |



 

