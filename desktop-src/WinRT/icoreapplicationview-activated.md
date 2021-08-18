---
description: происходит при активации приложения Windows Store.
ms.assetid: CA0DB2D4-3417-48F5-8455-D87D0F323A1E
title: 'Событие Икореаппликатионвиев:: Activated (Windows. ApplicationModel. Core. h)'
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 93e736d0fb5403fe76d6d402c261e6b7e5336dfc096d8c39d7b3300b93ab1332
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "118560998"
---
# <a name="icoreapplicationviewactivated-event"></a>Событие Икореаппликатионвиев:: Activated

происходит при активации приложения Windows Store.

## <a name="syntax"></a>Синтаксис


```C++
void Activated(
  [in] ITypedEventHandler<ICoreApplicationView*, IActivatedEventArgs*> handler
);
```



## <a name="parameters"></a>Параметры

<dl> <dt>

*обработчик событий* \[ окне\]
</dt> <dd></dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Это событие не возвращает значение.

## <a name="remarks"></a>Remarks

Не вызывайте метод [**Exit**](/previous-versions//hh438368(v=vs.85)) из *обработчика*.

## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------------------------|--------------------------------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Windows 8<br/>                                                                                         |
| Минимальная версия сервера<br/> | Windows Server 2012<br/>                                                                               |
| Header<br/>                   | <dl> <dt>Windows. ApplicationModel. Core. h</dt> </dl>   |
| IDL<br/>                      | <dl> <dt>Windows. ApplicationModel. Core. idl</dt> </dl> |



 

 
