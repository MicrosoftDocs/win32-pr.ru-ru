---
title: Сообщение BCM_GETTEXTMARGIN (Коммктрл. h)
description: Возвращает поля, используемые для рисования текста в элементе управления "Кнопка". Это сообщение можно отправить явным образом или воспользоваться \_ макросом кнопки жеттекстмаргин.
ms.assetid: 6c141752-e636-41c4-9d05-df8b320ff59f
keywords:
- элементы управления Windows сообщений BCM_GETTEXTMARGIN
topic_type:
- apiref
api_name:
- BCM_GETTEXTMARGIN
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2ea871d0054558e1522011d4fdb00fdd3c82a0dd1562fe3420d3295bbab89a01
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "120064414"
---
# <a name="bcm_gettextmargin-message"></a>\_Сообщение ЖЕТТЕКСТМАРГИН BCM

Возвращает поля, используемые для рисования текста в элементе управления "Кнопка". Это сообщение можно отправить явным образом или воспользоваться макросом [**кнопки \_ жеттекстмаргин**](/windows/desktop/api/Commctrl/nf-commctrl-button_gettextmargin) .

## <a name="parameters"></a>Параметры

<dl> <dt>

*wParam* 
</dt> <dd>

Не используется; должно быть равно нулю.

</dd> <dt>

*lParam* 
</dt> <dd>

Указатель на структуру [**Rect**](/previous-versions//dd162897(v=vs.85)) , содержащую поля, используемые для рисования текста.

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Если сообщение завершается с ошибкой, возвращается **значение true**. В противном случае возвращается **значение false**.

## <a name="remarks"></a>Remarks

> [!Note]  
> Чтобы использовать это сообщение, необходимо указать манифест, указывающий Comclt32.dll версии 6,0. Дополнительные сведения о манифестах см. в разделе [Включение визуальных стилей](cookbook-overview.md).

 

## <a name="requirements"></a>Requirements (Требования)



| Требование | Значение |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Windows \[Только классические приложения Vista\]<br/>                                        |
| Минимальная версия сервера<br/> | Windows Только для \[ настольных приложений сервера 2003\]<br/>                                  |
| Заголовок<br/>                   | <dl> <dt>Коммктрл. h</dt> </dl> |



 

