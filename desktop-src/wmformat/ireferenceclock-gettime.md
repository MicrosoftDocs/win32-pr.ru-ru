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
ms.openlocfilehash: c679ce0adbbc6cc7ddc014c12f1b0ace4be6b4b0
ms.sourcegitcommit: 57758ecb246c84d65e6e0e4bd5570d9176fa39cd
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/25/2019
ms.locfileid: "104411985"
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



 

## <a name="see-also"></a>См. также раздел

<dl> <dt>

[**Интерфейс Иреференцеклокк**](ireferenceclock.md)
</dt> </dl>

 

 





