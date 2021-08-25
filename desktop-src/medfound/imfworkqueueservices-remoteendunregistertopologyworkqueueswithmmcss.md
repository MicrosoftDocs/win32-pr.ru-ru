---
description: 'Версия метода Имфворккуеуесервицес:: Ендунрегистертопологиворккуеуесвисммксс, поддерживающая удаленное взаимодействие.'
ms.assetid: 8767a145-07b9-4427-9446-cee25e9074fa
title: Ремотиндунрегистертопологиворккуеуесвисммксс (Мфобжектс. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f083b4c0d7ae5610b041c14b3e6e54b917fdf7570300a5d7973a096b803bc447
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119941904"
---
# <a name="remoteendunregistertopologyworkqueueswithmmcss"></a>ремотиндунрегистертопологиворккуеуесвисммксс

Версия метода [**имфворккуеуесервицес:: ендунрегистертопологиворккуеуесвисммксс**](/windows/desktop/api/mfidl/nf-mfidl-imfworkqueueservices-endunregistertopologyworkqueueswithmmcss) , поддерживающая удаленное взаимодействие.

``` syntax
[call_as(EndUnregisterTopologyWorkQueuesWithMMCSS)]
HRESULT RemoteEndUnregisterTopologyWorkQueuesWithMMCSS(
    IUnknown *pResult
);
```

## <a name="remarks"></a>Remarks

Приложения не могут вызывать этот метод напрямую, и объекты не реализуют этот метод. Метод не отображается в таблице vtable для интерфейса. Если [**ендунрегистертопологиворккуеуесвисммксс**](/windows/desktop/api/mfidl/nf-mfidl-imfworkqueueservices-endunregistertopologyworkqueueswithmmcss) вызывается через границы процесса, то библиотека DLL прокси или заглушки Media Foundation преобразует вызов в вызов удаленного метода и затем преобразует его обратно.

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

 

 




