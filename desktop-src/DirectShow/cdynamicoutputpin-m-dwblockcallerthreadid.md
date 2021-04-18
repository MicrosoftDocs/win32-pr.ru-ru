---
description: 'Идентификатор потока, который последним вызвал метод Ипинфловконтрол:: Block для этого ПИН-кода. Эта переменная-член допустима только в том случае, если ПИН-код заблокирован.'
ms.assetid: 7f8429c5-7e58-49a1-9f36-01088379a193
title: 'Элемент Кдинамикаутпутпин:: m_dwBlockCallerThreadID (Амфилтер. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- m_dwBlockCallerThreadID
api_type:
- LibDef
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 9aa2de66f1afe690715ab658483c01cdfeb3f451
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105658076"
---
# <a name="cdynamicoutputpinm_dwblockcallerthreadid-member"></a>Элемент Кдинамикаутпутпин:: m \_ двблокккаллерсреадид

Идентификатор потока, который последним вызвал метод [**ипинфловконтрол:: Block**](/windows/desktop/api/Strmif/nf-strmif-ipinflowcontrol-block) для этого ПИН-кода. Эта переменная-член допустима только в том случае, если ПИН-код заблокирован.

## <a name="syntax"></a>Синтаксис


```C++
DWORD m_dwBlockCallerThreadID;
```



## <a name="remarks"></a>Примечания

Прежде чем обращаться к этой переменной, удерживайте критический раздел [**кдинамикаутпутпин:: m \_ блоккстателокк**](cdynamicoutputpin-m-blockstatelock.md) .

## <a name="requirements"></a>Требования



| Требование | Значение |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>Амфилтер. h (включение Streams. h)</dt> </dl>                                                                                  |
| Библиотека<br/> | <dl> <dt>Стрмбасе. lib (розничные сборки); </dt> <dt>Стрмбасд. lib (отладочные сборки)</dt> </dl> |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[**Класс Кдинамикаутпутпин**](cdynamicoutputpin.md)
</dt> </dl>

 

 




