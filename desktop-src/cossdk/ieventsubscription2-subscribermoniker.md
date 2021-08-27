---
description: Моникер подписчиков.
ms.assetid: d33d8c80-3251-4ec7-9cf3-d0b60d91ed5a
title: IEventSubscription2SubscriberMoniker, свойство
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IEventSubscription2.SubscriberMoniker
- IEventSubscription2.get_SubscriberMoniker
- IEventSubscription2.put_SubscriberMoniker
api_type:
- COM
api_location: ''
ms.openlocfilehash: cdd783a4e3f8d29d3ffc4ae279602db71c3ee16247ad58c6f23aa10bb3ba5350
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "120070674"
---
# <a name="ieventsubscription2subscribermoniker-property"></a>Свойство IEventSubscription2:: Субскрибермоникер

Моникер подписчика.

Это свойство доступно для чтения и записи.

## <a name="syntax"></a>Синтаксис


```C++
HRESULT put_SubscriberMoniker(
  [in]          BSTR bstrMoniker
);

HRESULT get_SubscriberMoniker(
  [out, retval] BSTR *pbstrMoniker
);
```



## <a name="property-value"></a>Значение свойства

Строка моникера, указывающая подписчика.

## <a name="error-codes"></a>Коды ошибок

Этот метод может возвращать стандартные возвращаемые значения E \_ INVALIDARG, e \_ OUTOFMEMORY, e \_ непредвиденные, e \_ Fail и S \_ ОК.

## <a name="requirements"></a>Requirements (Требования)



| Требование | Значение |
|-------------------------------------|------------------------------------------------------------|
| Минимальная версия клиента<br/> | Windows 2000 Professional \[только классические приложения\]<br/> |
| Минимальная версия сервера<br/> | Windows 2000 Server \[только классические приложения\]<br/>       |



## <a name="see-also"></a>См. также

<dl> <dt>

[**IEventSubscription2**](ieventsubscription2.md)
</dt> </dl>

 

 




