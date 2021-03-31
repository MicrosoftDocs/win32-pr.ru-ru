---
title: Сообщение HDM_GETITEMDROPDOWNRECT (Коммктрл. h)
description: Возвращает ограничивающий прямоугольник кнопки разворачивающегося элемента заголовка со стилем ХДФ \_ SPLITBUTTON. Отправляйте это сообщение явным образом или с помощью \_ макроса Жетитемдропдовнрект заголовка.
ms.assetid: d7188dfb-4ffa-4641-b210-2c2ec480ca13
keywords:
- Элементы управления Windows для HDM_GETITEMDROPDOWNRECT сообщений
topic_type:
- apiref
api_name:
- HDM_GETITEMDROPDOWNRECT
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b86f3df8de5224e79ca4e15ea18409e13972ca5d
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104071656"
---
# <a name="hdm_getitemdropdownrect-message"></a>\_Сообщение ЖЕТИТЕМДРОПДОВНРЕКТ HDM

Возвращает ограничивающий прямоугольник кнопки разворачивающегося элемента заголовка со стилем **ХДФ \_ SPLITBUTTON**. Отправляйте это сообщение явным образом или с помощью макроса [**\_ жетитемдропдовнрект заголовка**](/windows/desktop/api/Commctrl/nf-commctrl-header_getitemdropdownrect) .

## <a name="parameters"></a>Параметры

<dl> <dt>

*wParam* \[ окне\]
</dt> <dd>

Отсчитываемый от нуля индекс элемента управления заголовка, для которого требуется получить ограничивающий прямоугольник.

</dd> <dt>

*lParam* \[ в, out\]
</dt> <dd>

Указатель на структуру [**Rect**](/windows/win32/api/windef/ns-windef-rect) , которая получает сведения об ограничивающем прямоугольнике. Отправитель сообщения отвечает за выделение этой структуры. Координаты, возвращаемые в структуре RECT, выражаются относительно родительского элемента управления заголовка.

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Возвращает **значение true** , если успешно, или **false** в противном случае.

## <a name="remarks"></a>Комментарии

Элемент заголовка должен иметь Style **ХДФ \_ SPLITBUTTON**.

## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Только для \[ классических приложений Windows Vista\]<br/>                                        |
| Минимальная версия сервера<br/> | \[Только для настольных приложений Windows Server 2008\]<br/>                                  |
| Header<br/>                   | <dl> <dt>Коммктрл. h</dt> </dl> |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[Сведения об элементах управления "заголовок"](header-controls.md)
</dt> </dl>

 

 





