---
title: Сообщение RB_SETPALETTE (Коммктрл. h)
description: Задает текущую палитру элемента управления главной панели.
ms.assetid: 85f0726a-21fd-41b3-aa52-6a0a0c1947fa
keywords:
- Элементы управления Windows для RB_SETPALETTE сообщений
topic_type:
- apiref
api_name:
- RB_SETPALETTE
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e7ee47985c05bcd8a857620e7fe501bddf53bdec
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "103988984"
---
# <a name="rb_setpalette-message"></a>\_Сообщение СЕТПАЛЕТТЕ RB

Задает текущую палитру элемента управления главной панели.

## <a name="parameters"></a>Параметры

<dl> <dt>

*wParam* 
</dt> <dd>Должен равняться нулю.</dd> <dt>

*lParam* 
</dt> <dd>

Объект **хпалетте** , указывающий новую палитру, которую будет использовать элемент управления "Главная панель".

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Возвращает объект **хпалетте** , указывающий предыдущую палитру элемента управления главной панели.

## <a name="remarks"></a>Комментарии

Приложение, отправляющее это сообщение, отвечает за удаление **хпалетте** , переданных в этом сообщении (см. [**DeleteObject**](/windows/desktop/api/wingdi/nf-wingdi-deleteobject)). Элемент управления "Главная панель" не удалит набор **хпалетте** с этим сообщением.

## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Только для \[ классических приложений Windows Vista\]<br/>                                        |
| Минимальная версия сервера<br/> | \[Только для настольных приложений Windows Server 2003\]<br/>                                  |
| Header<br/>                   | <dl> <dt>Коммктрл. h</dt> </dl> |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[**панель \_ RB**](rb-getpalette.md)
</dt> </dl>

 

