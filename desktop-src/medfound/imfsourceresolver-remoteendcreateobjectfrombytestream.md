---
description: 'Версия метода Имфсаурцересолвер:: Ендкреатеобжектфромбитестреам, поддерживающая удаленное взаимодействие.'
ms.assetid: 6e4e9ace-e18a-45df-b20c-28e352fcdee7
title: Ремотиндкреатеобжектфромбитестреам (Мфобжектс. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8ce7e04368e099f00f0bd9d3f87141b5f8224f9c935f258ec9b4f7018cb7f364
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "118974303"
---
# <a name="remoteendcreateobjectfrombytestream"></a>ремотиндкреатеобжектфромбитестреам

Версия метода [**имфсаурцересолвер:: ендкреатеобжектфромбитестреам**](/windows/desktop/api/mfidl/nf-mfidl-imfsourceresolver-endcreateobjectfrombytestream) , поддерживающая удаленное взаимодействие.

``` syntax
[call_as(EndCreateObjectFromByteStream)]
HRESULT RemoteEndCreateObjectFromByteStream(
    IUnknown *pResult,
    MF_OBJECT_TYPE *pObjectType,
    IUnknown **ppObject
);
```

## <a name="remarks"></a>Remarks

Приложения не могут вызывать этот метод напрямую, и объекты не реализуют этот метод. Метод не отображается в таблице vtable для интерфейса. Если [**ендкреатеобжектфромбитестреам**](/windows/desktop/api/mfidl/nf-mfidl-imfsourceresolver-endcreateobjectfrombytestream) вызывается через границы процесса, то библиотека DLL прокси или заглушки Media Foundation преобразует вызов в вызов удаленного метода и затем преобразует его обратно.

## <a name="requirements"></a>Requirements (Требования)



| Требование | Значение |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Windows \[Приложения UWP для классических приложений Vista \|\]<br/>                                                    |
| Минимальная версия сервера<br/> | Windows \[Приложения UWP для классических приложений сервера 2008 \|\]<br/>                                              |
| Заголовок<br/>                   | <dl> <dt>Мфобжектс. h (включение Мфидл. h)</dt> </dl> |
| Библиотека<br/>                  | <dl> <dt>Мфууид. lib</dt> </dl>                    |



## <a name="see-also"></a>См. также

<dl> <dt>

[**имфсаурцересолвер**](/windows/desktop/api/mfidl/nn-mfidl-imfsourceresolver)
</dt> </dl>

 

 




