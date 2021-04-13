---
description: Происходит при активации приложения для Магазина Windows.
ms.assetid: CA0DB2D4-3417-48F5-8455-D87D0F323A1E
title: 'Событие Икореаппликатионвиев:: Activated (Windows. ApplicationModel. Core. h)'
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 612f7110aa149396b18815afe664ee404c70fc52
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104263085"
---
# <a name="icoreapplicationviewactivated-event"></a>Событие Икореаппликатионвиев:: Activated

Происходит при активации приложения для Магазина Windows.

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

## <a name="remarks"></a>Комментарии

Не вызывайте метод [**Exit**](/previous-versions//hh438368(v=vs.85)) из *обработчика*.

## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------------------------|--------------------------------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Windows 8<br/>                                                                                         |
| Минимальная версия сервера<br/> | Windows Server 2012<br/>                                                                               |
| Header<br/>                   | <dl> <dt>Windows. ApplicationModel. Core. h</dt> </dl>   |
| IDL<br/>                      | <dl> <dt>Windows. ApplicationModel. Core. idl</dt> </dl> |



 

 
