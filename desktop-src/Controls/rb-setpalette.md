---
title: Сообщение RB_SETPALETTE (Коммктрл. h)
description: Задает текущую палитру элемента управления главной панели.
ms.assetid: 85f0726a-21fd-41b3-aa52-6a0a0c1947fa
keywords:
- элементы управления Windows сообщений RB_SETPALETTE
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
ms.openlocfilehash: 85cd2968fa5fa74915e37f40f30dd47751e2316e8d91d0f51f9d3c7145b893fc
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119434944"
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

## <a name="remarks"></a>Remarks

Приложение, отправляющее это сообщение, отвечает за удаление **хпалетте** , переданных в этом сообщении (см. [**DeleteObject**](/windows/desktop/api/wingdi/nf-wingdi-deleteobject)). Элемент управления "Главная панель" не удалит набор **хпалетте** с этим сообщением.

## <a name="requirements"></a>Requirements (Требования)



| Требование | Значение |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Windows \[Только классические приложения Vista\]<br/>                                        |
| Минимальная версия сервера<br/> | Windows Только для \[ настольных приложений сервера 2003\]<br/>                                  |
| Header<br/>                   | <dl> <dt>Коммктрл. h</dt> </dl> |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[**панель \_ RB**](rb-getpalette.md)
</dt> </dl>

 

