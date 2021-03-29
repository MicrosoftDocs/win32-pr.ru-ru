---
description: 'Версия метода Имфворккуеуесервицес:: Ендрегистерплатформворккуеуевисммксс, поддерживающая удаленное взаимодействие.'
ms.assetid: cb15129e-a3ad-4351-a7d6-dd4b883437bd
title: Ремотиндрегистерплатформворккуеуевисммксс (Мфобжектс. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 673281a8ed4e4c4174ecd2d874e7032776ea44c8
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "103808050"
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

## <a name="remarks"></a>Комментарии

Приложения не могут вызывать этот метод напрямую, и объекты не реализуют этот метод. Метод не отображается в таблице vtable для интерфейса. Если [**ендрегистерплатформворккуеуевисммксс**](/windows/desktop/api/mfidl/nf-mfidl-imfworkqueueservices-endregisterplatformworkqueuewithmmcss) вызывается через границы процесса, то библиотека DLL прокси или заглушки Media Foundation преобразует вызов в вызов удаленного метода и затем преобразует его обратно.

## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Только для \[ классических приложений Windows Vista\]<br/>                                                           |
| Минимальная версия сервера<br/> | \[Только для настольных приложений Windows Server 2008\]<br/>                                                     |
| Header<br/>                   | <dl> <dt>Мфобжектс. h (включение Мфидл. h)</dt> </dl> |
| Библиотека<br/>                  | <dl> <dt>Мфууид. lib</dt> </dl>                    |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[**имфворккуеуесервицес**](/windows/desktop/api/mfidl/nn-mfidl-imfworkqueueservices)
</dt> </dl>

 

 




