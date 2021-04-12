---
title: Сообщение WM_POINTERROUTEDTO
description: Отправляется при текущем вводе указателя для существующего идентификатора указателя, переходит от одного процесса к другому через содержимое, настроенное для межпроцессных цепочек (Аддконтентвискросспроцессчаининг).
ms.assetid: 163E2C31-4E29-4CBA-B079-1963D4762D7B
keywords:
- WM_POINTERROUTEDTO сообщения и уведомления о входе
topic_type:
- apiref
api_name:
- WM_POINTERROUTEDTO
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: article
ms.date: 02/03/2020
ms.openlocfilehash: 7658aeef77a0f7e19f2449213e9332b4e60c9450
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104415285"
---
# <a name="wm_pointerroutedto-message"></a>Сообщение WM_POINTERROUTEDTO

Отправляется при текущем вводе указателя для существующего идентификатора указателя, переходит от одного процесса к другому через содержимое, настроенное для межпроцессных цепочек ([**аддконтентвискросспроцессчаининг**](/windows/win32/api/directmanipulation/nf-directmanipulation-idirectmanipulationcompositor2-addcontentwithcrossprocesschaining)).

Это сообщение отправляется в процесс, не принимающий входные данные указателя.


```C++
#define WM_POINTERROUTEDTO       0x0251
```



## <a name="parameters"></a>Параметры

<dl> <dt>

*wParam* 
</dt> <dd>

Не используется.

</dd> <dt>

*lParam* 
</dt> <dd>

Не используется.

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

NULL

## <a name="remarks"></a>Комментарии

Это сообщение не отправляется при публикации [**WM_POINTERDOWN**](wm-pointerdown.md) сообщения для нового идентификатора указателя в другом процессе.

[**WM_POINTERDOWN**](wm-pointerdown.md) сообщение не отправляется, если сначала будет отправлено **WM_POINTERROUTEDTO** сообщение.

## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Только для \[ настольных приложений Windows 10\]<br/>                                                              |
| Минимальная версия сервера<br/> | \[Только для настольных приложений Windows Server 2016\]<br/>                                                     |
| Header<br/>                   | <dl> <dt>Winuser. h (включение Windows. h)</dt> </dl> |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[Сообщения](messages.md)
</dt> <dt>

[**WM_POINTERROUTEDAWAY**](wm-pointerroutedaway.md)
</dt> </dl>

 

