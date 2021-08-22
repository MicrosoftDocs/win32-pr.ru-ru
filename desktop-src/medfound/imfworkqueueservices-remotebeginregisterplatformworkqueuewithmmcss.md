---
description: 'Версия метода Имфворккуеуесервицес:: Бегинрегистерплатформворккуеуевисммксс, поддерживающая удаленное взаимодействие.'
ms.assetid: 158497a9-9d66-4e58-919d-e35765fd29e4
title: Ремотебегинрегистерплатформворккуеуевисммксс (Мфобжектс. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0b19d163e8f3e34a9d4b0eca70f70c15442f683450319243e80f3842548f78d6
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "118974283"
---
# <a name="remotebeginregisterplatformworkqueuewithmmcss"></a>ремотебегинрегистерплатформворккуеуевисммксс

Версия метода [**имфворккуеуесервицес:: бегинрегистерплатформворккуеуевисммксс**](/windows/desktop/api/mfidl/nf-mfidl-imfworkqueueservices-beginregisterplatformworkqueuewithmmcss) , поддерживающая удаленное взаимодействие.

``` syntax
[call_as(BeginRegisterPlatformWorkQueueWithMMCSS)]
HRESULT RemoteBeginRegisterPlatformWorkQueueWithMMCSS(
    DWORD dwPlatformWorkQueue,
    LPCWSTR wszClass,
    DWORD dwTaskId,
    IMFRemoteAsyncCallback *pCallback
);
```

## <a name="remarks"></a>Remarks

Приложения не могут вызывать этот метод напрямую, и объекты не реализуют этот метод. Метод не отображается в таблице vtable для интерфейса. Если [**бегинрегистерплатформворккуеуевисммксс**](/windows/desktop/api/mfidl/nf-mfidl-imfworkqueueservices-beginregisterplatformworkqueuewithmmcss) вызывается через границы процесса, то библиотека DLL прокси или заглушки Media Foundation преобразует вызов в вызов удаленного метода и затем преобразует его обратно.

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

 

 




