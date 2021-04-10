---
title: Сообщение TDM_CLICK_VERIFICATION (Коммктрл. h)
description: Имитирует нажатие флажка проверки диалогового окна задачи, если оно существует.
ms.assetid: 1c6c135e-4e39-4f1a-88f4-5e9f7181a2dd
keywords:
- Элементы управления Windows для TDM_CLICK_VERIFICATION сообщений
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
ms.openlocfilehash: df61676104169e3084e7cde09439c218f2237e60
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104135086"
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

## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Только для \[ классических приложений Windows Vista\]<br/>                                        |
| Минимальная версия сервера<br/> | \[Только для настольных приложений Windows Server 2008\]<br/>                                  |
| Header<br/>                   | <dl> <dt>Коммктрл. h</dt> </dl> |



 

 





