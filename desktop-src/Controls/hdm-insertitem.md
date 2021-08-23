---
title: Сообщение HDM_INSERTITEM (Коммктрл. h)
description: Вставляет новый элемент в элемент управления "заголовок". Это сообщение можно отправить явным образом или воспользоваться заголовком \_ макроса InsertItem.
ms.assetid: aececf32-090d-4cd4-a239-4435a322f72e
keywords:
- элементы управления Windows сообщений HDM_INSERTITEM
topic_type:
- apiref
api_name:
- HDM_INSERTITEM
- HDM_INSERTITEMA
- HDM_INSERTITEMW
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e30a07637afae1a3efcf71b3b556c32bebf96775bb2a5cbdf6e92513d33ec5c6
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119544744"
---
# <a name="hdm_insertitem-message"></a>\_Сообщение INSERTITEM HDM

Вставляет новый элемент в элемент управления "заголовок". Это сообщение можно отправить явным образом или воспользоваться [**заголовком макроса \_ InsertItem**](/windows/desktop/api/Commctrl/nf-commctrl-header_insertitem) .

## <a name="parameters"></a>Параметры

<dl> <dt>

*wParam* 
</dt> <dd>

Индекс элемента, после которого вставляется новый элемент. Новый элемент вставляется в конец элемента управления заголовка, если параметр *wParam* больше или равен числу элементов в элементе управления. Если параметр *wParam* равен нулю, новый элемент вставляется в начало элемента управления заголовка.

</dd> <dt>

*lParam* 
</dt> <dd>

Указатель на структуру [**хдитем**](/windows/win32/api/commctrl/ns-commctrl-hditema) , содержащую сведения о новом элементе.

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Возвращает индекс нового элемента, если он выполнен успешно, или значение-1 в противном случае.

## <a name="requirements"></a>Requirements (Требования)



| Требование | Значение |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Windows \[Только классические приложения Vista\]<br/>                                        |
| Минимальная версия сервера<br/> | Windows Только для \[ настольных приложений сервера 2003\]<br/>                                  |
| Заголовок<br/>                   | <dl> <dt>Коммктрл. h</dt> </dl> |
| Имя в кодировке Юникод и ANSI<br/>   | **Разъем HDM \_ ИНСЕРТИТЕМВ** (Юникод) и **HDM \_ инсертитема** (ANSI)<br/>             |



 

 





