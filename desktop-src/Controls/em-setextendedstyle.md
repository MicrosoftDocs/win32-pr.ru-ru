---
title: Сообщение EM_SETEXTENDEDSTYLE (Коммктрл. h)
description: Информирует элемент управления "поле ввода" о необходимости установки расширенных стилей. Отправьте это сообщение или используйте макрос Edit \_ сетекстендедстиле.
ms.assetid: 4ca010c3-2c70-41e5-ade4-11e1895fda26
keywords:
- Элементы управления Windows для EM_SETEXTENDEDSTYLE сообщений
topic_type:
- apiref
api_name:
- EM_SETEXTENDEDSTYLE
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 10/19/2018
ms.openlocfilehash: 560b675927b4497810b8d492fd89b5765aa5a2c2
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104137159"
---
# <a name="em_setextendedstyle-message"></a>\_Сообщение СЕТЕКСТЕНДЕДСТИЛЕ EM

Информирует элемент управления "поле ввода" о необходимости установки расширенных стилей. Отправьте это сообщение или используйте макрос [**Edit \_ сетекстендедстиле**](/windows/desktop/api/Commctrl/nf-commctrl-edit_setextendedstyle).

## <a name="parameters"></a>Параметры

<dl> <dt>

*wParam* 
</dt> <dd>

Маска, используемая для выбора устанавливаемых стилей.

</dd> <dt>

*lParam* 
</dt> <dd>

Значение, указывающее расширенный стиль. Дополнительные сведения о стилях см. в разделе [Правка Управление расширенными стилями](edit-control-window-extended-styles.md).

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Если это сообщение завершается успешно, возвращается значение **S \_ ОК**. В противном случае возвращается код ошибки **HRESULT** .

## <a name="remarks"></a>Комментарии

Расширенные стили для элемента управления "поле ввода" не имеют никаких действий с расширенными стилями, используемыми с функцией [**CreateWindowEx**](/windows/desktop/api/winuser/nf-winuser-createwindowexa) или функцией [**SetWindowLong**](/windows/desktop/api/winuser/nf-winuser-setwindowlonga).

## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | \[Только для настольных приложений Windows 10 версии 1809\]<br/>                             |
| Минимальная версия сервера<br/> | \[Только для настольных приложений Windows Server 2019\]<br/>                                  |
| Header<br/>                   | <dl> <dt>Коммктрл. h</dt> </dl> |



 

