---
description: EC_DVD_VOBU_Timestamp — отправляется, когда Навигатор DVD выполняет синтаксический анализ пакета PCI.
ms.assetid: 25548c23-22f0-47cb-9062-273ad39d3007
title: EC_DVD_VOBU_Timestamp (Двдевкоде. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- EC_DVD_VOBU_Timestamp
api_type:
- HeaderDef
api_location:
- dvdevcode.h
ms.openlocfilehash: 6bd06eb99cae60960db64a6f32df5e4c932b362f
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2021
ms.locfileid: "108094622"
---
# <a name="ec_dvd_vobu_timestamp"></a>\_Отметка \_ времени вобу DVD-диска EC \_

Отправляется, когда [Навигатор DVD](dvd-navigator-filter.md) АНАЛИЗИРУЕТ пакет PCI.

Данные события — это метка времени последней единицы видеообъекта (ВОБУ).

## <a name="parameters"></a>Параметры

<dl> <dt>

<span id="lParam1"></span><span id="lparam1"></span><span id="LPARAM1"></span>*lParam1*
</dt> <dd>

Содержит **параметр DWORD** нижнего порядка метки времени.

</dd> <dt>

<span id="lParam2"></span><span id="lparam2"></span><span id="LPARAM2"></span>*lParam2*
</dt> <dd>

Содержит **параметр DWORD** с высоким порядковым обозначением метки времени.

</dd> </dl>

## <a name="remarks"></a>Remarks

По умолчанию это событие отключено. Чтобы включить это событие, вызовите [**IDvdControl2:: SetOption**](/windows/desktop/api/Strmif/nf-strmif-idvdcontrol2-setoption) и установите для параметра **\_ енаблелоггинжевентс DVD** значение **true**.

Воссоздайте отметку времени следующим образом:


```C++
LARGE_INTEGER li;
li.LowPart = DWORD( lParam1 );
li.HighPart = DWORD( lParam2 );
```



## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------|----------------------------------------------------------------------------------------------------------|
| Header<br/> | <dl> <dt>Двдевкоде. h (включение DShow. h)</dt> </dl> |



## <a name="see-also"></a>См. также

<dl> <dt>

[DVD-приложения](dvd-applications.md)
</dt> <dt>

[Коды уведомлений о событиях DVD](dvd-notification-codes.md)
</dt> <dt>

[Уведомление о событии в DirectShow](event-notification-in-directshow.md)
</dt> </dl>

 

 




