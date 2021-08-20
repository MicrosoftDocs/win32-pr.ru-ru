---
description: 'Версия метода Имфворккуеуесервицес:: Ендрегистерплатформворккуеуевисммксс, поддерживающая удаленное взаимодействие.'
ms.assetid: cb15129e-a3ad-4351-a7d6-dd4b883437bd
title: Ремотиндрегистерплатформворккуеуевисммксс (Мфобжектс. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a14414d9fe6d093ee797d8c9e4879bd54cf89b3dbfc60b526ae8556f78ecc34e
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "117878301"
---
# <a name="remoteendregisterplatformworkqueuewithmmcss"></a>ремотиндрегистерплатформворккуеуевисммксс

Версия метода [**имфворккуеуесервицес:: ендрегистерплатформворккуеуевисммксс**](/windows/desktop/api/mfidl/nf-mfidl-imfworkqueueservices-endregisterplatformworkqueuewithmmcss) , поддерживающая удаленное взаимодействие.

``` syntax
[call_as(EndRegisterPlatformWorkQueueWithMMCSS)]
HRESULT RemoteEndRegisterPlatformWorkQueueWithMMCSS(
    IUnknown *pResult,
    DWORD *pdwTaskId
);
```

## <a name="remarks"></a>Remarks

Приложения не могут вызывать этот метод напрямую, и объекты не реализуют этот метод. Метод не отображается в таблице vtable для интерфейса. Если [**ендрегистерплатформворккуеуевисммксс**](/windows/desktop/api/mfidl/nf-mfidl-imfworkqueueservices-endregisterplatformworkqueuewithmmcss) вызывается через границы процесса, то библиотека DLL прокси или заглушки Media Foundation преобразует вызов в вызов удаленного метода и затем преобразует его обратно.

## <a name="requirements"></a>Requirements (Требования)



| Требование | Значение |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Windows \[Только классические приложения Vista\]<br/>                                                           |
| Минимальная версия сервера<br/> | Windows Только для \[ настольных приложений сервера 2008\]<br/>                                                     |
| Заголовок<br/>                   | <dl> <dt>Мфобжектс. h (включение Мфидл. h)</dt> </dl> |
| Библиотека<br/>                  | <dl> <dt>Мфууид. lib</dt> </dl>                    |



## <a name="see-also"></a>См. также

<dl> <dt>

[**имфворккуеуесервицес**](/windows/desktop/api/mfidl/nn-mfidl-imfworkqueueservices)
</dt> </dl>

 

 




