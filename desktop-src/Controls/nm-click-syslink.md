---
title: Код уведомления NM_CLICK (Syslink) (Коммктрл. h)
description: Сообщает родительскому окну элемента управления, что пользователь щелкнул гиперссылку с левой кнопкой мыши внутри элемента управления. Этот код уведомления отправляется в виде \_ сообщения WM notify.
ms.assetid: e92d7c92-f2c6-44aa-bce5-3bb07c184e7d
keywords:
- Элементы управления Windows для кода уведомления NM_CLICK (Syslink)
topic_type:
- apiref
api_name:
- NM_CLICK
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2ea34682b0cfdfdf1206a133abe4fdb22b8af5cd
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104137874"
---
# <a name="nm_click-syslink-notification-code"></a>\_Код уведомления Click (Syslink) NM

Сообщает родительскому окну элемента управления, что пользователь щелкнул гиперссылку с левой кнопкой мыши внутри элемента управления. Этот код уведомления отправляется в виде сообщения [**WM \_ Notify**](wm-notify.md) .


```C++
NM_CLICK

    pnmLink = (PNMLINK) lParam; 
```



## <a name="parameters"></a>Параметры

<dl> <dt>

*lParam* 
</dt> <dd>

Указатель на структуру [**нмлинк**](/windows/win32/api/commctrl/ns-commctrl-nmlink) , содержащую дополнительные сведения об этом уведомлении.

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Возвращаемое значение игнорируется элементом управления.

## <a name="remarks"></a>Комментарии

> [!Note]  
> Чтобы использовать этот код уведомления, необходимо указать манифест, указывающий Comclt32.dll версии 6,0. Дополнительные сведения о манифестах см. в разделе [Включение визуальных стилей](cookbook-overview.md).

 

## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Только для \[ классических приложений Windows Vista\]<br/>                                        |
| Минимальная версия сервера<br/> | \[Только для настольных приложений Windows Server 2003\]<br/>                                  |
| Header<br/>                   | <dl> <dt>Коммктрл. h</dt> </dl> |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

**Ссылки**
</dt> <dt>

[**нмлинк**](/windows/win32/api/commctrl/ns-commctrl-nmlink)
</dt> <dt>

[**\_уведомление WM**](wm-notify.md)
</dt> </dl>

 

 





