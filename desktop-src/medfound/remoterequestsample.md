---
description: 'Версия метода Имфмедиастреам:: Рекуестсампле, поддерживающая удаленное взаимодействие.'
ms.assetid: 05ed4de0-fe5c-4183-8f1d-55d5a27e436a
title: Ремотерекуестсампле (Мфобжектс. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b0b572a9de9a74a744b9a9fc2c31dd816900301da623869cecdb03820ccbcf1d
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119034912"
---
# <a name="remoterequestsample"></a>ремотерекуестсампле

Версия метода [**имфмедиастреам:: рекуестсампле**](/windows/desktop/api/mfidl/nf-mfidl-imfmediastream-requestsample) , поддерживающая удаленное взаимодействие.

``` syntax
[call_as(RequestSample)]
HRESULT RemoteRequestSample();
```

## <a name="remarks"></a>Remarks

Приложения не могут вызывать этот метод напрямую, и объекты не реализуют этот метод. Метод не отображается в таблице vtable для интерфейса. Если [**рекуестсампле**](/windows/desktop/api/mfidl/nf-mfidl-imfmediastream-requestsample) вызывается через границы процесса, то библиотека DLL прокси или заглушки Media Foundation преобразует вызов в вызов удаленного метода и затем преобразует его обратно.

## <a name="requirements"></a>Requirements (Требования)



| Требование | Значение |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Windows \[Приложения UWP для классических приложений Vista \|\]<br/>                                                    |
| Минимальная версия сервера<br/> | Windows \[Приложения UWP для классических приложений сервера 2008 \|\]<br/>                                              |
| Заголовок<br/>                   | <dl> <dt>Мфобжектс. h (включение Мфидл. h)</dt> </dl> |
| Библиотека<br/>                  | <dl> <dt>Мфууид. lib</dt> </dl>                    |



## <a name="see-also"></a>См. также

<dl> <dt>

[**имфмедиастреам**](/windows/desktop/api/mfidl/nn-mfidl-imfmediastream)
</dt> </dl>

 

 




