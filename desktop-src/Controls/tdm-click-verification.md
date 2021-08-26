---
title: Сообщение TDM_CLICK_VERIFICATION (Коммктрл. h)
description: Имитирует нажатие флажка проверки диалогового окна задачи, если оно существует.
ms.assetid: 1c6c135e-4e39-4f1a-88f4-5e9f7181a2dd
keywords:
- элементы управления Windows сообщений TDM_CLICK_VERIFICATION
topic_type:
- apiref
api_name:
- TDM_CLICK_VERIFICATION
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b3cda5e85b138225d69e159792cbe641122e91bf9602b3e0f5edafa419edc3c3
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119876094"
---
# <a name="tdm_click_verification-message"></a>TDM \_ щелкните \_ сообщение о проверке

Имитирует нажатие флажка проверки диалогового окна задачи, если оно существует.

## <a name="parameters"></a>Параметры

<dl> <dt>

*wParam* \[ окне\]
</dt> <dd>

**Значение true** , чтобы установить флажок проверять состояние флажка; **Значение false** , чтобы снять флажок для этого параметра.

</dd> <dt>

*lParam* \[ окне\]
</dt> <dd>

**Значение true** , чтобы установить флажок в фокусе клавиатуры; В противном случае — **значение false** .

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Возвращаемое значение игнорируется.

## <a name="requirements"></a>Requirements (Требования)



| Требование | Значение |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Windows \[Только классические приложения Vista\]<br/>                                        |
| Минимальная версия сервера<br/> | Windows Только для \[ настольных приложений сервера 2008\]<br/>                                  |
| Заголовок<br/>                   | <dl> <dt>Коммктрл. h</dt> </dl> |



 

 





