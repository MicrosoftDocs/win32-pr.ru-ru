---
description: Идентификатор GUID приложения для объекта класса событий.
ms.assetid: 0d19183a-429c-4564-b6a5-f06481d27e00
title: 'Свойство IEventSubscription3:: Евентклассаппликатионид'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IEventSubscription3.EventClassApplicationID
- IEventSubscription3.get_EventClassApplicationID
- IEventSubscription3.put_EventClassApplicationID
api_type:
- COM
api_location: ''
ms.openlocfilehash: 3e80a8d8f557c80a1b2605328728260eb8ae7bd7
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104141821"
---
# <a name="ieventsubscription3eventclassapplicationid-property"></a>Свойство IEventSubscription3:: Евентклассаппликатионид

Идентификатор GUID приложения для объекта класса событий.

Это свойство доступно для чтения и записи.

## <a name="syntax"></a>Синтаксис


```C++
HRESULT put_EventClassApplicationID(
  [in]          BSTR bstrEventClassApplicationID
);

HRESULT get_EventClassApplicationID(
  [out, retval] BSTR *pbstrEventClassApplicationID
);
```



## <a name="property-value"></a>Значение свойства

Строка, содержащая идентификатор GUID приложения класса событий.

## <a name="error-codes"></a>Коды ошибок

Этот метод может возвращать стандартные возвращаемые значения E \_ INVALIDARG, e \_ OUTOFMEMORY, e \_ непредвиденные, e \_ Fail и S \_ ОК.

## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------------------------|------------------------------------------------------------|
| Минимальная версия клиента<br/> | Windows 2000 Professional \[только классические приложения\]<br/> |
| Минимальная версия сервера<br/> | Windows 2000 Server \[только классические приложения\]<br/>       |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[**IEventSubscription3**](ieventsubscription3.md)
</dt> </dl>

 

 




