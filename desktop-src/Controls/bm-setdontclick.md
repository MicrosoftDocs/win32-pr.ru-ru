---
title: Сообщение BM_SETDONTCLICK (Winuser. h)
description: Устанавливает флаг на переключателе, который управляет созданием млрд ДОЛЛных \_ сообщений, когда кнопка получает фокус.
ms.assetid: 91d98bce-abea-4afc-a995-0f426ba7a518
keywords:
- Элементы управления Windows для BM_SETDONTCLICK сообщений
topic_type:
- apiref
api_name:
- BM_SETDONTCLICK
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c8596ec679ff07b87b3433d5b5a7805698f56f84
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "105654448"
---
# <a name="bm_setdontclick-message"></a>\_Сообщение BM сетдонткликк

Устанавливает флаг на переключателе, который управляет созданием [млрд доллных сообщений \_ ](bn-clicked.md) , когда кнопка получает фокус.

## <a name="parameters"></a>Параметры

<dl> <dt>

*wParam* \[ окне\]
</dt> <dd>

**Логическое** значение, указывающее состояние. **Значение true** , чтобы установить флаг; в противном случае — **значение false**.

</dd> <dt>

*lParam* 
</dt> <dd>

Не используется. Должен равняться нулю.

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Нет возвращаемого значения.

## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Только для \[ классических приложений Windows Vista\]<br/>                                                           |
| Минимальная версия сервера<br/> | \[Только для настольных приложений Windows Server 2008\]<br/>                                                     |
| Header<br/>                   | <dl> <dt>Winuser. h (включение Windows. h)</dt> </dl> |



 

 





