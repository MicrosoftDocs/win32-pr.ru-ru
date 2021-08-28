---
title: Код уведомления LBN_SELCHANGE (Winuser. h)
description: Уведомляет приложение о том, что выбор в списке изменился в результате ввода данных пользователем. Родительское окно списка получает этот код уведомления через \_ командное сообщение WM.
ms.assetid: 126d2c47-816e-4179-a870-f5c5a34c5513
keywords:
- LBN_SELCHANGE кода уведомления Windows элементы управления
topic_type:
- apiref
api_name:
- LBN_SELCHANGE
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3ef87aebcf2ce804a10b4682bfaf2cba900bd227a06671959d11babce5f46774
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "120085184"
---
# <a name="lbn_selchange-notification-code"></a>\_Код уведомления ЛБН селчанже

Уведомляет приложение о том, что выбор в списке изменился в результате ввода данных пользователем. Родительское окно списка получает этот код уведомления через [**\_ командное сообщение WM**](/windows/desktop/menurc/wm-command) .


```C++
LBN_SELCHANGE

    WPARAM wParam;
    LPARAM lParam; 
```



## <a name="parameters"></a>Параметры

<dl> <dt>

*wParam* 
</dt> <dd>

[**Ловорд**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85)) содержит идентификатор поля списка. [**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85)) указывает код уведомления.

</dd> <dt>

*lParam* 
</dt> <dd>

Обработайте с списком.

</dd> </dl>

## <a name="remarks"></a>Remarks

Этот код уведомления отправляется только в список, в котором имеется стиль [**\_ уведомления фунта**](list-box-styles.md) .

Этот код уведомления не отправляется, если выбрано сообщение [**\_ сетсел балансировки**](lb-setsel.md)нагрузки, балансировка нагрузки [**\_ сеткурсел**](lb-setcursel.md), [**Балансировка нагрузки \_ селектстринг**](lb-selectstring.md), [**Балансировка нагрузки \_ селитемранже**](lb-selitemrange.md) или [**фунтов \_ селитемранжеекс**](lb-selitemrangeex.md) .

Для списка с множественным выбором \_ код уведомления ЛБН селчанже отправляется каждый раз, когда пользователь нажимает клавишу со стрелкой, даже если выделение не изменяется.

## <a name="requirements"></a>Requirements (Требования)



| Требование | Значение |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Windows \[Только классические приложения Vista\]<br/>                                                           |
| Минимальная версия сервера<br/> | Windows Только для \[ настольных приложений сервера 2003\]<br/>                                                     |
| Заголовок<br/>                   | <dl> <dt>Winuser. h (включает Windows. h)</dt> </dl> |



## <a name="see-also"></a>См. также

<dl> <dt>

**Ссылки**
</dt> <dt>

[**сеткурсел балансировки нагрузки \_**](lb-setcursel.md)
</dt> <dt>

[ЛБН \_ дблклк](lbn-dblclk.md)
</dt> <dt>

[ЛБН \_ селканцел](lbn-selcancel.md)
</dt> <dt>

**Другие ресурсы**
</dt> <dt>

[**\_команда WM**](/windows/desktop/menurc/wm-command)
</dt> </dl>

 

