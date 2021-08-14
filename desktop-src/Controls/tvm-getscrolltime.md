---
title: Сообщение TVM_GETSCROLLTIME (Коммктрл. h)
description: Возвращает максимальное время прокрутки для элемента управления "дерево-представление". Это сообщение можно отправить явно или с помощью \_ макроса Жетскроллтиме TreeView.
ms.assetid: 992d1906-cda3-4ac7-ba90-c681c551ac2e
keywords:
- элементы управления Windows сообщений TVM_GETSCROLLTIME
topic_type:
- apiref
api_name:
- TVM_GETSCROLLTIME
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e026a463476d5625f7632d7b6679ce94ca2c8ab6d8c6a050d8938bd46d9858b6
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "118408501"
---
# <a name="tvm_getscrolltime-message"></a>\_Сообщение TVM жетскроллтиме

Возвращает максимальное время прокрутки для элемента управления "дерево-представление". Это сообщение можно отправить явно или с помощью макроса [**\_ жетскроллтиме TreeView**](/windows/desktop/api/Commctrl/nf-commctrl-treeview_getscrolltime) .

## <a name="parameters"></a>Параметры

<dl> <dt>

*wParam* 
</dt> <dd>Должен равняться нулю.</dd> <dt>

*lParam* 
</dt> <dd>Должен равняться нулю.</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Возвращает максимальное время прокрутки в миллисекундах.

## <a name="remarks"></a>Remarks

Максимальное время прокрутки — это наибольшее количество времени, которое может занять операция прокрутки. Прокрутка будет скорректирована таким образом, что прокрутка будет выполняться в пределах максимального времени прокрутки. Операция прокрутки может занять меньше времени, чем максимальное значение.

## <a name="requirements"></a>Requirements (Требования)



| Требование | Значение |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Windows \[Только классические приложения Vista\]<br/>                                        |
| Минимальная версия сервера<br/> | Windows Только для \[ настольных приложений сервера 2003\]<br/>                                  |
| Header<br/>                   | <dl> <dt>Коммктрл. h</dt> </dl> |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[**TVM \_ сетскроллтиме**](tvm-setscrolltime.md)
</dt> </dl>

 

 





