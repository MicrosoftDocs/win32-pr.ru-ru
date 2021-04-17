---
description: Дата и время создания отчета.
ms.assetid: b9435384-72e0-42c4-a948-df52621a5ec2
title: Локатиондисп. ДиспЦивикаддрессрепорт. timestamp, свойство
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- LocationDisp.DispCivicAddressReport.Timestamp
api_type:
- COM
api_location: ''
ms.openlocfilehash: 7b805454a6c2d62a58ba5a2a3de8f5b5095e1db8
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "105684452"
---
# <a name="locationdispdispcivicaddressreporttimestamp-property"></a>Локатиондисп. ДиспЦивикаддрессрепорт. timestamp, свойство

\[Объектная модель API расположения доступна для использования в операционных системах, указанных в разделе требования. В последующих версиях он может быть изменен или недоступен. Вместо этого для доступа к расположению с веб-сайта используйте [API географического расположения W3C](/previous-versions/windows/internet-explorer/ie-developer/samples/gg589513(v=vs.85)). Чтобы получить доступ к расположению из классического приложения, используйте API [**Windows. Devices. Географическое расположение**](/uwp/api/Windows.Devices.Geolocation) .\]

Дата и время создания отчета.

Это свойство доступно только для чтения.

## <a name="syntax"></a>Синтаксис


```JScript
Timestamp = LocationDisp.DispCivicAddressReport.Timestamp
```



## <a name="property-value"></a>Значение свойства

Это свойство является **датой** только для чтения. Временные метки задаются в формате UTC.

## <a name="remarks"></a>Комментарии

Обратите внимание, что для языков сценариев, таких как Microsoft JScript, может потребоваться выполнить преобразование в другие форматы времени при отображении меток времени в виде строк.

## <a name="examples"></a>Примеры

Пример использования этого свойства см. [в примере простого отчета об использовании административного адреса](/uwp/api/Windows.Devices.Geolocation).

## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------------------------|--------------------------------------------|
| Минимальная версия клиента<br/> | \[Только классические приложения Windows 7\]<br/> |
| Минимальная версия сервера<br/> | Ни одна версия не поддерживается<br/>                  |



 

