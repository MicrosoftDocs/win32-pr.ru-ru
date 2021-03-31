---
title: Сообщение STM_SETICON (Winuser. h)
description: Приложение отправляет \_ сообщение STM сетикон, чтобы связать значок с элементом управления "значок".
ms.assetid: 105b0667-8e23-47ed-9fb1-0792a22d7100
keywords:
- Элементы управления Windows для STM_SETICON сообщений
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
ms.openlocfilehash: cb9c7e2a007c1f866a1c73b3a1c1a55b157add47
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104071176"
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
| Минимальная версия клиента<br/> | Только для \[ классических приложений Windows Vista\]<br/>                                                           |
| Минимальная версия сервера<br/> | \[Только для настольных приложений Windows Server 2003\]<br/>                                                     |
| Header<br/>                   | <dl> <dt>Winuser. h (включение Windows. h)</dt> </dl> |



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

 

