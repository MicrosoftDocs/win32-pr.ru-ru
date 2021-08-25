---
title: Код уведомления TBN_SAVE (Коммктрл. h)
description: Сообщает родительскому окну панели инструментов, что панель инструментов находится в процессе сохранения. Этот код уведомления отправляется в виде \_ сообщения WM notify.
ms.assetid: 31622f5e-2e33-4a42-8c49-cc3028a6fa62
keywords:
- TBN_SAVE кода уведомления Windows элементы управления
topic_type:
- apiref
api_name:
- TBN_SAVE
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7f9d4fb40d0e5beafcd720b4de52a8cf09d17c3e4c6f7b4dcfa8da78e00e97ef
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119876594"
---
# <a name="tbn_save-notification-code"></a>ТБН \_ сохранить код уведомления

Сообщает родительскому окну панели инструментов, что панель инструментов находится в процессе сохранения. Этот код уведомления отправляется в виде сообщения [**WM \_ Notify**](wm-notify.md) .


```C++
TBN_SAVE 

    lpnmtb = (LPNMTBSAVE) lParam; 
```



## <a name="parameters"></a>Параметры

<dl> <dt>

*lParam* 
</dt> <dd>

Указатель на структуру [**нмтбсаве**](/windows/win32/api/commctrl/ns-commctrl-nmtbsave) .

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Нет возвращаемого значения.

## <a name="remarks"></a>Remarks

Приложение получит этот код уведомления один раз в начале процесса сохранения и один раз для каждой кнопки. Этот код уведомления позволяет добавлять в оболочку собственные сведения, сохраненные с помощью оболочки. Если вы не хотите добавлять сведения, пропустите код уведомления. Дополнительные сведения об обработке ТБН Save см. в статье [Настройка панелей инструментов](toolbar-controls-overview.md) \_ .

## <a name="requirements"></a>Requirements (Требования)



| Требование | Значение |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Windows \[Только классические приложения Vista\]<br/>                                        |
| Минимальная версия сервера<br/> | Windows Только для \[ настольных приложений сервера 2003\]<br/>                                  |
| Заголовок<br/>                   | <dl> <dt>Коммктрл. h</dt> </dl> |



## <a name="see-also"></a>См. также

<dl> <dt>

[\_Восстановление ТБН](tbn-restore.md)
</dt> </dl>

 

 





