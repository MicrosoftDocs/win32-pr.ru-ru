---
title: Сообщение EM_SCROLLCARET (Winuser. h)
description: Прокручивает курсор на представление в элементе управления "поле ввода". Это сообщение можно отправить либо в элемент управления "поле ввода", либо в элемент управления Rich Edit.
ms.assetid: 7a33034d-9369-49f8-a881-0c1d2cedff6a
keywords:
- Элементы управления Windows для EM_SCROLLCARET сообщений
topic_type:
- apiref
api_name:
- EM_SCROLLCARET
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: faa9f4bd69605f5e8fad36a683c9be2894546cb0
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104137622"
---
# <a name="em_scrollcaret-message"></a>\_Сообщение СКРОЛЛКАРЕТ EM

Прокручивает курсор на представление в элементе управления "поле ввода". Это сообщение можно отправить либо в элемент управления "поле ввода", либо в элемент управления Rich Edit.

## <a name="parameters"></a>Параметры

<dl> <dt>

*wParam* 
</dt> <dd>

Этот параметр зарезервирован. Он должен иметь значение 0.

</dd> <dt>

*lParam* 
</dt> <dd>

Этот параметр зарезервирован. Он должен иметь значение 0.

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Возвращаемое значение не имеет смысла.

## <a name="remarks"></a>Комментарии

**Расширенное редактирование:** Поддерживается в Microsoft Rich Edit 1,0 и более поздних версиях. Дополнительные сведения о совместимости расширенных версий редактирования с различными версиями системы см. в разделе [Общие сведения об элементах управления редактированием](about-rich-edit-controls.md).

## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Только для \[ классических приложений Windows Vista\]<br/>                                                           |
| Минимальная версия сервера<br/> | \[Только для настольных приложений Windows Server 2003\]<br/>                                                     |
| Header<br/>                   | <dl> <dt>Winuser. h (включение Windows. h)</dt> </dl> |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

**Ссылки**
</dt> <dt>

[**EM \_ линескролл**](em-linescroll.md)
</dt> <dt>

[**\_прокрутка EM**](em-scroll.md)
</dt> <dt>

[**WM \_ VSCROLL**](wm-vscroll.md)
</dt> </dl>

 

 





