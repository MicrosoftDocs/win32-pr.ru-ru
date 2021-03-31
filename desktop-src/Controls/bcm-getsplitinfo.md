---
title: Сообщение BCM_GETSPLITINFO (Коммктрл. h)
description: Возвращает сведения для элемента управления "кнопка разворачивающейся кнопки". Отправляйте это сообщение явным образом или с помощью \_ макроса кнопки жетсплитинфо.
ms.assetid: d608440d-b8d8-4e32-9128-08b7566b185c
keywords:
- Элементы управления Windows для BCM_GETSPLITINFO сообщений
topic_type:
- apiref
api_name:
- BCM_GETSPLITINFO
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 162c5522fcb432e3d512f688ae24aa12d4d0d8e1
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "103988731"
---
# <a name="bcm_getsplitinfo-message"></a>\_Сообщение ЖЕТСПЛИТИНФО BCM

Возвращает сведения для элемента управления "кнопка разворачивающейся кнопки". Отправляйте это сообщение явным образом или с помощью макроса [**кнопки \_ жетсплитинфо**](/windows/desktop/api/Commctrl/nf-commctrl-button_getsplitinfo) .

## <a name="parameters"></a>Параметры

<dl> <dt>

*wParam* 
</dt> <dd>

Должен равняться нулю.

</dd> <dt>

*lParam* \[ в, out\]
</dt> <dd>

Указатель на структуру [**кнопки \_ сплитинфо**](/windows/win32/api/commctrl/ns-commctrl-button_splitinfo) для получения сведений о кнопке. Вызывающий объект отвечает за выделение памяти для структуры. Установите элемент **маски** этой структуры, чтобы определить, какие сведения следует получить.

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Возвращает **значение true** , если успешно, или **false** в противном случае.

## <a name="remarks"></a>Комментарии

Это сообщение используется только с стилями кнопки " [**BS \_**](button-styles.md) " и " [**BS \_ дефсплитбуттон**](button-styles.md) ".

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

 

 





