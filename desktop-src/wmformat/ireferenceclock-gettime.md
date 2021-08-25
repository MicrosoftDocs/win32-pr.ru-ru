---
title: Иреференцеклокк метода времени
description: Метод Time извлекает текущее время ссылки.
ms.assetid: 9bf5050a-ae09-4a72-a3f2-3df8339d99b9
keywords:
- Метод Time формат Windows Media
- Метод Time формат Windows Media, интерфейс Иреференцеклокк
- Интерфейс Иреференцеклокк интерфейса Windows Media Format, метод
topic_type:
- apiref
api_name:
- IReferenceClock.GetTime
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: f7756240e8987199e1f1b5d79e3f0b676d4808520781fbac18dfa18dd75e88d4
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "120055444"
---
# <a name="ireferenceclockgettime-method"></a>Метод Иреференцеклокк:: OnTime

Метод **time** извлекает текущее время ссылки.

## <a name="syntax"></a>Синтаксис


```C++
HRESULT GetTime(
  [out] REFERENCE_TIME *pTime
);
```



## <a name="parameters"></a>Параметры

<dl> <dt>

*птиме* \[ заполняет\]
</dt> <dd>

Указатель на переменную, которая получает текущее время в единицах измерения 100-наносекундных.

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Метод возвращает **значение HRESULT**. Допустимые значения включают, но не ограничиваются, значения, приведенные в следующей таблице.



| Код возврата                                                                               | Описание                                   |
|-------------------------------------------------------------------------------------------|-----------------------------------------------|
| <dl> <dt>**\_ОК**</dt> </dl>      | Метод выполнен успешно.<br/>              |
| <dl> <dt>**\_указатель E**</dt> </dl> | Параметр *птиме* имеет **значение NULL**.<br/> |



 

## <a name="see-also"></a>См. также

<dl> <dt>

[**Интерфейс Иреференцеклокк**](ireferenceclock.md)
</dt> </dl>

 

 





