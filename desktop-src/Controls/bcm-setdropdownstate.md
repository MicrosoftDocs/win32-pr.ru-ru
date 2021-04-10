---
title: Сообщение BCM_SETDROPDOWNSTATE (Коммктрл. h)
description: Задает раскрывающееся состояние для кнопки с \_ раскрывающимся списком Style тбстиле. Отправляйте это сообщение явным образом или с помощью \_ макроса кнопки сетдропдовнстате.
ms.assetid: 725deff4-0bcb-497d-a6cf-e9c98b05f16e
keywords:
- Элементы управления Windows для BCM_SETDROPDOWNSTATE сообщений
topic_type:
- apiref
api_name:
- BCM_SETDROPDOWNSTATE
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: fc44ec58d40e047708591121f81c84f327ca47c1
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104135867"
---
# <a name="bcm_setdropdownstate-message"></a>\_Сообщение СЕТДРОПДОВНСТАТЕ BCM

Задает раскрывающееся состояние для кнопки с [**\_ раскрывающимся списком Style тбстиле**](toolbar-control-and-button-styles.md). Отправляйте это сообщение явным образом или с помощью макроса [**кнопки \_ сетдропдовнстате**](/windows/desktop/api/Commctrl/nf-commctrl-button_setdropdownstate) .

## <a name="parameters"></a>Параметры

<dl> <dt>

*wParam* \[ окне\]
</dt> <dd>

**Логическое** **значение, истинное** для состояния BST \_ дропдовнпушед, или **false** в противном случае.

</dd> <dt>

*lParam* 
</dt> <dd>

Должен равняться нулю.

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Возвращает **значение true** , если успешно, или **false** в противном случае.

## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Только для \[ классических приложений Windows Vista\]<br/>                                        |
| Минимальная версия сервера<br/> | \[Только для настольных приложений Windows Server 2008\]<br/>                                  |
| Header<br/>                   | <dl> <dt>Коммктрл. h</dt> </dl> |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

**Ссылки**
</dt> <dt>

[Стили кнопок](button-styles.md)
</dt> <dt>

**Зрения**
</dt> <dt>

[Типы кнопок](button-types-and-styles.md)
</dt> </dl>

 

 





