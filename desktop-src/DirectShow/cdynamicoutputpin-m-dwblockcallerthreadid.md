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
ms.openlocfilehash: b52bd7f718798ea9dd2cf9d227f6d22e069d2c1a59bb8591f6126c20599af9f0
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119539754"
---
# <a name="cdynamicoutputpinm_dwblockcallerthreadid-member"></a>Элемент Кдинамикаутпутпин:: m \_ двблокккаллерсреадид

Идентификатор потока, который последним вызвал метод [**ипинфловконтрол:: Block**](/windows/desktop/api/Strmif/nf-strmif-ipinflowcontrol-block) для этого ПИН-кода. Эта переменная-член допустима только в том случае, если ПИН-код заблокирован.

## <a name="syntax"></a>Синтаксис


```C++
DWORD m_dwBlockCallerThreadID;
```



## <a name="remarks"></a>Remarks

Прежде чем обращаться к этой переменной, удерживайте критический раздел [**кдинамикаутпутпин:: m \_ блоккстателокк**](cdynamicoutputpin-m-blockstatelock.md) .

## <a name="requirements"></a>Requirements (Требования)



| Требование | Значение |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Заголовок<br/>  | <dl> <dt>амфилтер. h (включает Потоки. h)</dt> </dl>                                                                                  |
| Библиотека<br/> | <dl> <dt>Стрмбасе. lib (розничные сборки); </dt> <dt>Стрмбасд. lib (отладочные сборки)</dt> </dl> |



## <a name="see-also"></a>См. также

<dl> <dt>

[**Класс Кдинамикаутпутпин**](cdynamicoutputpin.md)
</dt> </dl>

 

 




