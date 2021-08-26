---
title: монсдайстате
description: Тип данных МОНСДАЙСТАТЕ — это битовое поле, которое содержит состояние каждого дня месяца.
ms.assetid: eb3dd6cb-738e-424b-945b-1485798a444c
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a4e21eed1293a53bce8f38f5bd4db09b8cbe3fbf649fb07348a5dca65e908727
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "120079864"
---
# <a name="monthdaystate"></a>монсдайстате

Тип данных МОНСДАЙСТАТЕ — это битовое поле, которое содержит состояние каждого дня месяца. Тип данных определяется в Коммктрл. h следующим образом:


```
typedef DWORD MONTHDAYSTATE, *LPMONTHDAYSTATE;
```



Каждый бит (от 0 до 30) представляет состояние дня в месяце. Если бит включен, соответствующий день будет отображаться полужирным шрифтом; в противном случае он будет отображаться без каких бы то ни было внимания.

Этот тип данных используется с сообщением [**MCM \_ сетдайстате**](mcm-setdaystate.md) и соответствующим макросом, [**монскал \_ сетдайстате**](/windows/desktop/api/Commctrl/nf-commctrl-monthcal_setdaystate). Если значения МОНСДАЙСТАТЕ используются в ссылке на месяцы короче 31 день, будут доступны только необходимые биты.

Этот тип данных был впервые определен в Comctl32.dll [версии 4,70](common-control-versions.md) .

 

 




