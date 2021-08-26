---
description: 'Версия метода Имфворккуеуесервицес:: Ендунрегистерплатформворккуеуевисммксс, поддерживающая удаленное взаимодействие.'
ms.assetid: 92eef511-0af0-4146-ac81-7dfa4a649016
title: Ремотиндунрегистерплатформворккуеуевисммксс (Мфобжектс. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a93a5d969dda1323d8ddb5f313fabbf482651ccd4bb966a922e0c4f0f734ebde
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "120013914"
---
# <a name="remoteendunregisterplatformworkqueuewithmmcss"></a>ремотиндунрегистерплатформворккуеуевисммксс

Версия метода [**имфворккуеуесервицес:: ендунрегистерплатформворккуеуевисммксс**](/windows/desktop/api/mfidl/nf-mfidl-imfworkqueueservices-endunregisterplatformworkqueuewithmmcss) , поддерживающая удаленное взаимодействие.

``` syntax
[call_as(EndUnregisterPlatformWorkQueueWithMMCSS)]
HRESULT RemoteEndUnregisterPlatformWorkQueueWithMMCSS(
    IUnknown *pResult
);
```

## <a name="remarks"></a>Remarks

Приложения не могут вызывать этот метод напрямую, и объекты не реализуют этот метод. Метод не отображается в таблице vtable для интерфейса. Если [**ендунрегистерплатформворккуеуевисммксс**](/windows/desktop/api/mfidl/nf-mfidl-imfworkqueueservices-endunregisterplatformworkqueuewithmmcss) вызывается через границы процесса, то библиотека DLL прокси или заглушки Media Foundation преобразует вызов в вызов удаленного метода и затем преобразует его обратно.

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

 

 




