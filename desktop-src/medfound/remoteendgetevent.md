---
description: 'Версия метода Имфмедиаевентженератор:: Енджетевент, поддерживающая удаленное взаимодействие.'
ms.assetid: 5b793760-546c-43d4-8251-d89d8d7152ad
title: Ремотинджетевент (Мфобжектс. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 709cb65280e32c1aa662c5dfbec851b24d353370853db1742814a4ba5daf61de
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119034902"
---
# <a name="remoteendgetevent"></a>ремотинджетевент

Версия метода [**имфмедиаевентженератор:: енджетевент**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediaeventgenerator-endgetevent) , поддерживающая удаленное взаимодействие.

``` syntax
[call_as(EndGetEvent)]
HRESULT RemoteEndGetEvent(
    IUnknown *pResult,
    DWORD *pcbEvent,
    BYTE **ppbEvent
);
```

## <a name="remarks"></a>Remarks

Приложения не могут вызывать этот метод напрямую, и объекты не реализуют этот метод. Метод не отображается в таблице vtable для интерфейса. Если [**енджетевент**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediaeventgenerator-endgetevent) вызывается через границы процесса, то библиотека DLL прокси или заглушки Media Foundation преобразует вызов в вызов удаленного метода и затем преобразует его обратно.

## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Windows \[Приложения UWP для классических приложений Vista \|\]<br/>                                                    |
| Минимальная версия сервера<br/> | Windows \[Приложения UWP для классических приложений сервера 2008 \|\]<br/>                                              |
| Заголовок<br/>                   | <dl> <dt>Мфобжектс. h (включение Мфидл. h)</dt> </dl> |
| Библиотека<br/>                  | <dl> <dt>Мфууид. lib</dt> </dl>                    |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[**имфмедиаевентженератор**](/windows/desktop/api/mfobjects/nn-mfobjects-imfmediaeventgenerator)
</dt> </dl>

 

 




