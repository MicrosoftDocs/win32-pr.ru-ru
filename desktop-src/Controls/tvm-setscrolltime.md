---
title: Сообщение TVM_SETSCROLLTIME (Коммктрл. h)
description: Задает максимальное время прокрутки для элемента управления "дерево-представление". Это сообщение можно отправить явно или с помощью \_ макроса Сетскроллтиме TreeView.
ms.assetid: b0ad81ba-0621-42b7-8fe1-f3bd5bc16d6a
keywords:
- элементы управления Windows сообщений TVM_SETSCROLLTIME
topic_type:
- apiref
api_name:
- TVM_SETSCROLLTIME
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4c9ca3392de81a712aa6be7dc2addb87eedf65af4aa77958e5b7f5fbb2eafc87
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "118408491"
---
# <a name="tvm_setscrolltime-message"></a>\_Сообщение TVM сетскроллтиме

Задает максимальное время прокрутки для элемента управления "дерево-представление". Это сообщение можно отправить явно или с помощью макроса [**\_ сетскроллтиме TreeView**](/windows/desktop/api/Commctrl/nf-commctrl-treeview_setscrolltime) .

## <a name="parameters"></a>Параметры

<dl> <dt>

*wParam* 
</dt> <dd>

Новое максимальное время прокрутки в миллисекундах.

</dd> <dt>

*lParam* 
</dt> <dd>Должен равняться нулю.</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Возвращает предыдущее максимальное время прокрутки в миллисекундах.

## <a name="remarks"></a>Remarks

Максимальное время прокрутки — это наибольшее количество времени, которое может занять операция прокрутки. Прокрутка будет скорректирована таким образом, что прокрутка будет выполняться в пределах максимального времени прокрутки. Операция прокрутки может занять меньше времени, чем максимальное значение.

## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Windows \[Только классические приложения Vista\]<br/>                                        |
| Минимальная версия сервера<br/> | Windows Только для \[ настольных приложений сервера 2003\]<br/>                                  |
| Header<br/>                   | <dl> <dt>Коммктрл. h</dt> </dl> |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[**TVM \_ жетскроллтиме**](tvm-getscrolltime.md)
</dt> </dl>

 

 





