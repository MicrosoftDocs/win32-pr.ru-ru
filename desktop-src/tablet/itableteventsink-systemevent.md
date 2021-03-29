---
description: Происходит при наличии системного события.
ms.assetid: 3d9e98f0-b11e-4a65-a544-9e1998a80d5f
title: 'Метод Итаблетевентсинк:: Системевент'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ITabletEventSink.SystemEvent
api_type:
- COM
api_location:
- wisptis.exe
- wisptis.exe.dll
ms.openlocfilehash: 71b5882fd9e19df43581e00cce55c2af5faa432b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "105647487"
---
# <a name="itableteventsinksystemevent-method"></a>Метод Итаблетевентсинк:: Системевент

Происходит при наличии системного события.

## <a name="syntax"></a>Синтаксис


```C++
HRESULT SystemEvent(
  [in] TABLET_CONTEXT_ID tcid,
  [in] CURSOR_ID         cid,
  [in] SYSTEM_EVENT      event,
  [in] SYSTEM_EVENT_DATA eventdata
);
```



## <a name="parameters"></a>Параметры

<dl> <dt>

*тЦид* \[ окне\]
</dt> <dd>

Идентификатор планшета.

</dd> <dt>

*CID* \[ в\]
</dt> <dd>

Идентификатор пера.

</dd> <dt>

*событие* \[ окне\]
</dt> <dd>

Код системного события.

</dd> <dt>

*EVENTDATA* \[ окне\]
</dt> <dd>

Данные системных событий.

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Этот метод может возвращать одно из этих значений.



| Код возврата                                                                            | Описание                               |
|----------------------------------------------------------------------------------------|-------------------------------------------|
| <dl> <dt>**\_ОК**</dt> </dl>   | Успешно.<br/>                       |
| <dl> <dt>**\_Ошибка E**</dt> </dl> | Произошла неизвестная ошибка.<br/> |



 

## <a name="remarks"></a>Комментарии

Следующий список содержит допустимые значения для параметра события.

-   \_касание SE
-   SE \_ Двойное \_ касание
-   SE, \_ правое \_ касание
-   SE, \_ перетаскивание
-   SE \_ , \_ перетаскивание
-   SE, \_ удержание \_ Ввод
-   SE, \_ удержание \_ оставить
-   SE. \_ Ввод с наведением \_
-   SE \_ навести на \_ выход
-   \_средний щелчок по центру SE \_
-   \_ключ SE
-   \_ключ модификатора \_ SE
-   \_режим ЖЕСТОВ \_ SE
-   \_курсор SE

## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------------------------|----------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Только классические приложения Windows XP Tablet PC Edition \[\]<br/>                          |
| Минимальная версия сервера<br/> | Ни одна версия не поддерживается<br/>                                                              |
| Библиотека<br/>                  | <dl> <dt>Wisptis.exe</dt> </dl> |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[**Интерфейс Итаблетевентсинк**](itableteventsink.md)
</dt> </dl>

 

 




