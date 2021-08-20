---
description: 'Версия метода Имфтопологиноде:: Жетаутпутпрефтипе, поддерживающая удаленное взаимодействие.'
ms.assetid: 56fbbf14-0c55-4f98-bcda-7f434cff803c
title: Ремотежетаутпутпрефтипе (Мфобжектс. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: aa443f909a5154ab8f695872033e64b49dc8e72a8a846c690f242271281af9a6
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "118062794"
---
# <a name="remotegetoutputpreftype"></a>ремотежетаутпутпрефтипе

Версия метода [**имфтопологиноде:: жетаутпутпрефтипе**](/windows/desktop/api/mfidl/nf-mfidl-imftopologynode-getoutputpreftype) , поддерживающая удаленное взаимодействие.

``` syntax
[call_as(GetOutputPrefType)] 
HRESULT RemoteGetOutputPrefType(
    DWORD dwOutputIndex,
    DWORD *pcbData,
    BYTE **ppbData
);
```

## <a name="remarks"></a>Remarks

Приложения не могут вызывать этот метод напрямую, и объекты не реализуют этот метод. Метод не отображается в таблице vtable для интерфейса. Если **жетаутпутпрефтипе** вызывается через границы процесса, то библиотека DLL прокси или заглушки Media Foundation преобразует вызов в вызов удаленного метода и затем преобразует его обратно.

## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Windows \[Только классические приложения Vista\]<br/>                                                           |
| Минимальная версия сервера<br/> | Windows Только для \[ настольных приложений сервера 2008\]<br/>                                                     |
| Заголовок<br/>                   | <dl> <dt>Мфобжектс. h (включение Мфидл. h)</dt> </dl> |
| Библиотека<br/>                  | <dl> <dt>Мфууид. lib</dt> </dl>                    |



## <a name="see-also"></a>См. также

<dl> <dt>

[**имфтопологиноде**](/windows/desktop/api/mfidl/nn-mfidl-imftopologynode)
</dt> </dl>

 

 




