---
title: Код уведомления LBN_SELCHANGE (Winuser. h)
description: Уведомляет приложение о том, что выбор в списке изменился в результате ввода данных пользователем. Родительское окно списка получает этот код уведомления через \_ командное сообщение WM.
ms.assetid: 126d2c47-816e-4179-a870-f5c5a34c5513
keywords:
- LBN_SELCHANGE кода уведомления элементы управления Windows
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
ms.openlocfilehash: e029d1753a0fa74f39a59a459d6ede45811a40fd
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "103802327"
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

## <a name="remarks"></a>Комментарии

Этот код уведомления отправляется только в список, в котором имеется стиль [**\_ уведомления фунта**](list-box-styles.md) .

Этот код уведомления не отправляется, если выбрано сообщение [**\_ сетсел балансировки**](lb-setsel.md)нагрузки, балансировка нагрузки [**\_ сеткурсел**](lb-setcursel.md), [**Балансировка нагрузки \_ селектстринг**](lb-selectstring.md), [**Балансировка нагрузки \_ селитемранже**](lb-selitemrange.md) или [**фунтов \_ селитемранжеекс**](lb-selitemrangeex.md) .

Для списка с множественным выбором \_ код уведомления ЛБН селчанже отправляется каждый раз, когда пользователь нажимает клавишу со стрелкой, даже если выделение не изменяется.

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

 

