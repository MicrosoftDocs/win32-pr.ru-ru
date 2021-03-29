---
description: 'Версия метода Имфтопологиноде:: Жетинпутпрефтипе, поддерживающая удаленное взаимодействие.'
ms.assetid: b02cf739-97a9-4bb0-abb1-0da491857c50
title: Ремотежетинпутпрефтипе (Мфобжектс. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6461e804d6066b467378742ff02c8e708f5f6714
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "103810816"
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

## <a name="remarks"></a>Комментарии

Приложения не могут вызывать этот метод напрямую, и объекты не реализуют этот метод. Метод не отображается в таблице vtable для интерфейса. Если [**жетинпутпрефтипе**](/windows/desktop/api/mfidl/nf-mfidl-imftopologynode-getinputpreftype) вызывается через границы процесса, то библиотека DLL прокси или заглушки Media Foundation преобразует вызов в вызов удаленного метода и затем преобразует его обратно.

## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Только для \[ классических приложений Windows Vista\]<br/>                                                           |
| Минимальная версия сервера<br/> | \[Только для настольных приложений Windows Server 2008\]<br/>                                                     |
| Header<br/>                   | <dl> <dt>Мфобжектс. h (включение Мфидл. h)</dt> </dl> |
| Библиотека<br/>                  | <dl> <dt>Мфууид. lib</dt> </dl>                    |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[**имфтопологиноде**](/windows/desktop/api/mfidl/nn-mfidl-imftopologynode)
</dt> </dl>

 

 




