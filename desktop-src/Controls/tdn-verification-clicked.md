---
title: Код уведомления TDN_VERIFICATION_CLICKED (Коммктрл. h)
description: Отправляется диалоговым окном задачи, когда пользователь нажимает флажок "Проверка диалогового окна задачи". Этот код уведомления получается только через функцию обратного вызова диалогового окна задачи, которую можно зарегистрировать с помощью метода Таскдиалогиндирект.
ms.assetid: cd7bc07a-9a70-4361-abfa-986a5a2e13e0
keywords:
- TDN_VERIFICATION_CLICKED кода уведомления элементы управления Windows
topic_type:
- apiref
api_name:
- TDN_VERIFICATION_CLICKED
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7887a4d696f5294ebffc6fc6cc7183ff2c0aed8d
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "103989364"
---
# <a name="tdn_verification_clicked-notification-code"></a>\_ \_ Код уведомления о нажатии ТДН проверки

Отправляется диалоговым окном задачи, когда пользователь нажимает флажок "Проверка диалогового окна задачи". Этот код уведомления получается только через функцию обратного вызова диалогового окна задачи, которую можно зарегистрировать с помощью метода [**таскдиалогиндирект**](/windows/desktop/api/Commctrl/nf-commctrl-taskdialogindirect) .


```C++
TDN_VERIFICATION_CLICKED

   WPARAM wParam;
   LPARAM lParam;
```



## <a name="parameters"></a>Параметры

<dl> <dt>

*wParam* 
</dt> <dd>

**Логическое** значение, указывающее состояние флажка проверки. **Значение true** , если флажок проверки установлен, или **значение false** , если флажок снят.

</dd> <dt>

*lParam* 
</dt> <dd>

Должен равняться нулю.

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Возвращаемое значение игнорируется.

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

[*таскдиалогкаллбаккпрок*](/windows/win32/api/commctrl/nc-commctrl-pftaskdialogcallback)
</dt> </dl>

 

