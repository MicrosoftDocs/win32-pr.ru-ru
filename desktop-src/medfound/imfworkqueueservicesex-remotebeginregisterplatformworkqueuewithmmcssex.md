---
description: 'Версия Имфворккуеуесервицесекс:: Бегинрегистерплатформворккуеуевисммкссекс, поддерживающая удаленное взаимодействие.'
ms.assetid: 75af7ce6-9b74-4d61-b7f2-5d07538f91cf
title: ремотебегинрегистерплатформворккуеуевисммкссекс
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ee1174e4edb8271aa9240857d8082ade87d1a8e6551ac788f98f217c41eb1d9d
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "120114294"
---
# <a name="remotebeginregisterplatformworkqueuewithmmcssex"></a>ремотебегинрегистерплатформворккуеуевисммкссекс

Версия [**имфворккуеуесервицесекс:: бегинрегистерплатформворккуеуевисммкссекс**](/windows/desktop/api/mfidl/nf-mfidl-imfworkqueueservicesex-beginregisterplatformworkqueuewithmmcssex), поддерживающая удаленное взаимодействие.

``` syntax
[call_as(BeginRegisterPlatformWorkQueueWithMMCSSEx)]
HRESULT RemoteBeginRegisterPlatformWorkQueueWithMMCSSEx(
    DWORD dwPlatformWorkQueue,
    LPCWSTR wszClass,
    DWORD dwTaskId, 
    LONG lPriority,
    IMFRemoteAsyncCallback *pCallback
);
```

## <a name="remarks"></a>Remarks

Приложения не могут вызывать этот метод напрямую, и объекты не реализуют этот метод. Метод не отображается в таблице vtable для интерфейса. Если [**бегинрегистерплатформворккуеуевисммкссекс**](/windows/desktop/api/mfidl/nf-mfidl-imfworkqueueservicesex-beginregisterplatformworkqueuewithmmcssex) вызывается через границы процесса, то библиотека DLL прокси или заглушки Media Foundation преобразует вызов в вызов удаленного метода и затем преобразует его обратно.

## <a name="requirements"></a>Requirements (Требования)



| Требование | Значение |
|-------------------------------------|--------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Windows 8 \[ только классические приложения\]<br/>                                           |
| Минимальная версия сервера<br/> | Windows Server 2012 \[ только классические приложения\]<br/>                                 |
| Заголовок<br/>                   | <dl> <dt>Мфидл. idl</dt> </dl> |



## <a name="see-also"></a>См. также

<dl> <dt>

[**имфворккуеуесервицесекс**](/windows/desktop/api/mfidl/nn-mfidl-imfworkqueueservicesex)
</dt> </dl>

 

 




