---
description: Происходит при создании отчета об использовании нового административного адреса.
ms.assetid: a8df870e-6744-4e8a-a103-56b446da135f
title: Событие НевЦивикаддрессрепорт
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- NewCivicAddressReport
api_type:
- COM
api_location: ''
ms.openlocfilehash: 61b5c6c05d8aa551148d278fa0cbafa8791bbc4c1a1f6b1142ef7f2ef80af318
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "118386744"
---
# <a name="newcivicaddressreport-event"></a>Событие НевЦивикаддрессрепорт

\[Объектная модель API расположения доступна для использования в операционных системах, указанных в разделе требования. В последующих версиях он может быть изменен или недоступен. Вместо этого для доступа к расположению с веб-сайта используйте [API географического расположения W3C](/previous-versions/windows/internet-explorer/ie-developer/samples/gg589513(v=vs.85)). Чтобы получить доступ к расположению из классического приложения, используйте [**Windows. API Devices. Географическое расположение**](/uwp/api/Windows.Devices.Geolocation) .\]

Происходит при создании отчета об использовании нового административного адреса.

## <a name="syntax"></a>Синтаксис


```JScript
.NewCivicAddressReport(
  newReport
)
```



## <a name="parameters"></a>Параметры

<dl> <dt>

*неврепорт* 
</dt> <dd>

Новый объект [**локатиондисп. диспЦивикаддрессрепорт**](locationdisp-dispcivicaddressreport.md) .

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Это событие не возвращает значение.

## <a name="examples"></a>Примеры

Пример использования этого события см. в разделе [прослушивание событий административного адреса](/uwp/api/Windows.Devices.Geolocation).

## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------------------------|--------------------------------------------|
| Минимальная версия клиента<br/> | только Windows 7 \[ настольных приложений\]<br/> |
| Минимальная версия сервера<br/> | Ни одна версия не поддерживается<br/>                  |



 

