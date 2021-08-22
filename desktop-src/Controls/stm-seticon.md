---
title: Сообщение STM_SETICON (Winuser. h)
description: Приложение отправляет \_ сообщение STM сетикон, чтобы связать значок с элементом управления "значок".
ms.assetid: 105b0667-8e23-47ed-9fb1-0792a22d7100
keywords:
- элементы управления Windows сообщений STM_SETICON
topic_type:
- apiref
api_name:
- STM_SETICON
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 55ff1cbaa6a1083751b3619392fbb0d3b60695e829907c2dfe27fdb41170e167
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119281424"
---
# <a name="stm_seticon-message"></a>\_Сообщение СЕТИКОН STM

Приложение отправляет сообщение **STM \_ сетикон** , чтобы связать значок с элементом управления "значок".

## <a name="parameters"></a>Параметры

<dl> <dt>

*wParam* 
</dt> <dd>

Обработчик значка, связываемый с элементом управления "значок".

</dd> <dt>

*lParam* 
</dt> <dd>

Этот параметр не используется.

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Возвращаемое значение является обработчиком значка, ранее связанного с элементом управления "значок", или нулем в случае возникновения ошибки.

## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Windows \[Только классические приложения Vista\]<br/>                                                           |
| Минимальная версия сервера<br/> | Windows Только для \[ настольных приложений сервера 2003\]<br/>                                                     |
| Заголовок<br/>                   | <dl> <dt>Winuser. h (включает Windows. h)</dt> </dl> |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

**Ссылки**
</dt> <dt>

[**\_значок STM**](stm-geticon.md)
</dt> <dt>

**Другие ресурсы**
</dt> <dt>

[**лоадикон**](/windows/desktop/api/winuser/nf-winuser-loadicona)
</dt> </dl>

 

