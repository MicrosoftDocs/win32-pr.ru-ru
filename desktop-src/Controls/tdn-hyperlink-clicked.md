---
title: Код уведомления TDN_HYPERLINK_CLICKED (Коммктрл. h)
description: Отправляется диалоговым окном задачи, когда пользователь щелкает гиперссылку в содержимом диалогового окна задачи. Этот код уведомления получается только через функцию обратного вызова диалогового окна задачи, которую можно зарегистрировать с помощью метода Таскдиалогиндирект.
ms.assetid: b769af31-32d0-463e-be15-6abf5dcb425c
keywords:
- TDN_HYPERLINK_CLICKED кода уведомления Windows элементы управления
topic_type:
- apiref
api_name:
- TDN_HYPERLINK_CLICKED
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0adaf5ecf05b22e3ff33aa88e28cb3f8f8c8b78f0b06d2127792b7639942bf7f
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119875774"
---
# <a name="tdn_hyperlink_clicked-notification-code"></a>\_ \_ Код уведомления щелчка по ГИПЕРССЫЛКе ТДН

Отправляется диалоговым окном задачи, когда пользователь щелкает гиперссылку в содержимом диалогового окна задачи. Этот код уведомления получается только через функцию обратного вызова диалогового окна задачи, которую можно зарегистрировать с помощью метода [**таскдиалогиндирект**](/windows/desktop/api/Commctrl/nf-commctrl-taskdialogindirect) .


```C++
TDN_HYPERLINK_CLICKED

   WPARAM wParam;
   LPARAM lParam;
```



## <a name="parameters"></a>Параметры

<dl> <dt>

*wParam* 
</dt> <dd>

Должен равняться нулю.

</dd> <dt>

*lParam* 
</dt> <dd>

Указатель на строку расширенных символов, содержащую URL-адрес гиперссылки.

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Возвращаемое значение игнорируется.

## <a name="requirements"></a>Requirements (Требования)



| Требование | Значение |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Windows \[Только классические приложения Vista\]<br/>                                        |
| Минимальная версия сервера<br/> | Windows Только для \[ настольных приложений сервера 2008\]<br/>                                  |
| Заголовок<br/>                   | <dl> <dt>Коммктрл. h</dt> </dl> |



 

 





