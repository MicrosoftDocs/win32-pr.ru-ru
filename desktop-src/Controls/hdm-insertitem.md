---
title: Сообщение HDM_INSERTITEM (Коммктрл. h)
description: Вставляет новый элемент в элемент управления "заголовок". Это сообщение можно отправить явным образом или воспользоваться заголовком \_ макроса InsertItem.
ms.assetid: aececf32-090d-4cd4-a239-4435a322f72e
keywords:
- Элементы управления Windows для HDM_INSERTITEM сообщений
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
ms.openlocfilehash: c9cabf86fea79fd437b3e9fb7e32890b3ba1a780
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104490710"
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

## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Только для \[ классических приложений Windows Vista\]<br/>                                        |
| Минимальная версия сервера<br/> | \[Только для настольных приложений Windows Server 2003\]<br/>                                  |
| Header<br/>                   | <dl> <dt>Коммктрл. h</dt> </dl> |
| Имя в кодировке Юникод и ANSI<br/>   | **Разъем HDM \_ ИНСЕРТИТЕМВ** (Юникод) и **HDM \_ инсертитема** (ANSI)<br/>             |



 

 





