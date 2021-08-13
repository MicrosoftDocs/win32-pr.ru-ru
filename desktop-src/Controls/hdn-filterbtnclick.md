---
title: Код уведомления HDN_FILTERBTNCLICK (Коммктрл. h)
description: Уведомляет родительское окно элемента управления заголовка при нажатии кнопки фильтра или в ответ на \_ сообщение СЕТИТЕМ HDM. Этот код уведомления отправляется в виде \_ сообщения WM notify.
ms.assetid: 36b85cdc-1022-4568-8891-0c919c850fd4
keywords:
- HDN_FILTERBTNCLICK кода уведомления Windows элементы управления
topic_type:
- apiref
api_name:
- HDN_FILTERBTNCLICK
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 01ba216c9946854ccfc6a651db90ab1dd5ed106dfca6ddf568d485c33dae70ab
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119435514"
---
# <a name="hdn_filterbtnclick-notification-code"></a>\_Код уведомления ХДН филтербтнкликк

Уведомляет родительское окно элемента управления заголовка при нажатии кнопки фильтра или в ответ на сообщение [**\_ сетитем HDM**](hdm-setitem.md) . Этот код уведомления отправляется в виде сообщения [**WM \_ Notify**](wm-notify.md) .


```C++
HDN_FILTERBTNCLICK

    pNMHDFilterBtnClk = (LPNMHDFILTERBTNCLICK) lParam;
```



## <a name="parameters"></a>Параметры

<dl> <dt>

*lParam* 
</dt> <dd>

Указатель на структуру [**нмхдфилтербтнкликк**](/windows/win32/api/commctrl/ns-commctrl-nmhdfilterbtnclick) , содержащую сведения о элементе управления "заголовок" и кнопку фильтра заголовка.

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Если вы возвращаете **значение true**, код уведомления [ХДН \_ филтерчанже](hdn-filterchange.md) будет отправлен в родительское окно элемента управления заголовка. Этот код уведомления дает родительскому окну возможность синхронизировать свои элементы пользовательского интерфейса. Возвращает **значение false** , если не нужно отправлять уведомление.

## <a name="requirements"></a>Requirements (Требования)



| Требование | Значение |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Windows \[Только классические приложения Vista\]<br/>                                        |
| Минимальная версия сервера<br/> | Windows Только для \[ настольных приложений сервера 2003\]<br/>                                  |
| Header<br/>                   | <dl> <dt>Коммктрл. h</dt> </dl> |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[**нмхдфилтербтнкликк**](/windows/win32/api/commctrl/ns-commctrl-nmhdfilterbtnclick)
</dt> </dl>

 

 





