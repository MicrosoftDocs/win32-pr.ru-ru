---
description: 'Версия метода Имфсаурцересолвер:: Бегинкреатеобжектфромбитестреам, поддерживающая удаленное взаимодействие.'
ms.assetid: 960b5c51-b9b1-4956-a270-abfb7eedd482
title: Ремотебегинкреатеобжектфромбитестреам (Мфобжектс. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ac2cf089f0b80e83373c36731de4bd9a36d8835b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "105701710"
---
# <a name="remotebegincreateobjectfrombytestream"></a>ремотебегинкреатеобжектфромбитестреам

Версия метода [**имфсаурцересолвер:: бегинкреатеобжектфромбитестреам**](/windows/desktop/api/mfidl/nf-mfidl-imfsourceresolver-begincreateobjectfrombytestream) , поддерживающая удаленное взаимодействие.

``` syntax
[call_as(BeginCreateObjectFromByteStream)]
HRESULT RemoteBeginCreateObjectFromByteStream(
    IMFByteStream* pByteStream,
    LPCWSTR pwszURL,
    IPropertyStore *pProps,
    DWORD dwFlags,
    IMFRemoteAsyncCallback *pCallback
);
```

## <a name="remarks"></a>Комментарии

Приложения не могут вызывать этот метод напрямую, и объекты не реализуют этот метод. Метод не отображается в таблице vtable для интерфейса. Если [**бегинкреатеобжектфромбитестреам**](/windows/desktop/api/mfidl/nf-mfidl-imfsourceresolver-begincreateobjectfrombytestream) вызывается через границы процесса, то библиотека DLL прокси или заглушки Media Foundation преобразует вызов в вызов удаленного метода и затем преобразует его обратно.

## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | \[Приложения UWP для классических приложений Windows Vista \|\]<br/>                                                    |
| Минимальная версия сервера<br/> | \[Приложения UWP для классических приложений Windows Server 2008 \|\]<br/>                                              |
| Header<br/>                   | <dl> <dt>Мфобжектс. h (включение Мфидл. h)</dt> </dl> |
| Библиотека<br/>                  | <dl> <dt>Мфууид. lib</dt> </dl>                    |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[**имфсаурцересолвер**](/windows/desktop/api/mfidl/nn-mfidl-imfsourceresolver)
</dt> </dl>

 

 




