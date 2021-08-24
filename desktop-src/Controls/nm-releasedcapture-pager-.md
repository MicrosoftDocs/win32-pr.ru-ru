---
title: Код уведомления NM_RELEASEDCAPTURE (пейджер) (Коммктрл. h)
description: Сообщает родительскому окну элемента управления страничного навигатора, что элемент управления отпускает захват мыши. Этот код уведомления отправляется в виде \_ сообщения WM notify.
ms.assetid: 5ce9c38a-5d37-4ac7-8510-30bc59d85cca
keywords:
- элементы управления Windows кода уведомления NM_RELEASEDCAPTURE (пейджер)
topic_type:
- apiref
api_name:
- NM_RELEASEDCAPTURE
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f857f64b6964d9258aca6cb923553a85e11e8b0fd9931c3fe2ceb4050038a7ce
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119826064"
---
# <a name="nm_releasedcapture-pager-notification-code"></a>\_Код уведомления NM релеаседкаптуре (пейджер)

Сообщает родительскому окну элемента управления страничного навигатора, что элемент управления отпускает захват мыши. Этот код уведомления отправляется в виде сообщения [**WM \_ Notify**](wm-notify.md) .


```C++
NM_RELEASEDCAPTURE

    lpnmh = (LPNMHDR) lParam; 
```



## <a name="parameters"></a>Параметры

<dl> <dt>

*lParam* 
</dt> <dd>

Указатель на структуру [**NMHDR**](/windows/desktop/api/richedit/ns-richedit-nmhdr) , содержащую дополнительные сведения об этом уведомлении.

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Возвращаемое значение игнорируется элементом управления страничного навигатора.

## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Windows \[Только классические приложения Vista\]<br/>                                        |
| Минимальная версия сервера<br/> | Windows Только для \[ настольных приложений сервера 2003\]<br/>                                  |
| Заголовок<br/>                   | <dl> <dt>Коммктрл. h</dt> </dl> |



 

 





