---
description: 'Версия метода Имфтопологиноде:: Жетинпутпрефтипе, поддерживающая удаленное взаимодействие.'
ms.assetid: b02cf739-97a9-4bb0-abb1-0da491857c50
title: Ремотежетинпутпрефтипе (Мфобжектс. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8cc11bbb28f15bad78955b59e556873d0500c92e45c126a9e710961ab83cf7e2
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "117878319"
---
# <a name="remotegetinputpreftype"></a>ремотежетинпутпрефтипе

Версия метода [**имфтопологиноде:: жетинпутпрефтипе**](/windows/desktop/api/mfidl/nf-mfidl-imftopologynode-getinputpreftype) , поддерживающая удаленное взаимодействие.

``` syntax
[call_as(GetInputPrefType)] 
HRESULT RemoteGetInputPrefType(
    DWORD dwInputIndex,
    DWORD *pcbData,
    BYTE **ppbData
);
```

## <a name="remarks"></a>Remarks

Приложения не могут вызывать этот метод напрямую, и объекты не реализуют этот метод. Метод не отображается в таблице vtable для интерфейса. Если [**жетинпутпрефтипе**](/windows/desktop/api/mfidl/nf-mfidl-imftopologynode-getinputpreftype) вызывается через границы процесса, то библиотека DLL прокси или заглушки Media Foundation преобразует вызов в вызов удаленного метода и затем преобразует его обратно.

## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Windows \[Только классические приложения Vista\]<br/>                                                           |
| Минимальная версия сервера<br/> | Windows Только для \[ настольных приложений сервера 2008\]<br/>                                                     |
| Заголовок<br/>                   | <dl> <dt>Мфобжектс. h (включение Мфидл. h)</dt> </dl> |
| Библиотека<br/>                  | <dl> <dt>Мфууид. lib</dt> </dl>                    |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[**имфтопологиноде**](/windows/desktop/api/mfidl/nn-mfidl-imftopologynode)
</dt> </dl>

 

 




