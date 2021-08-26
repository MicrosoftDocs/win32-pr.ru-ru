---
title: Сообщение BCM_SETTEXTMARGIN (Коммктрл. h)
description: '\_Сообщение СЕТТЕКСТМАРГИН BCM задает поля для рисования текста в элементе управления "Кнопка".'
ms.assetid: 0798b1c5-7db4-46c6-8881-4c847abc7460
keywords:
- элементы управления Windows сообщений BCM_SETTEXTMARGIN
topic_type:
- apiref
api_name:
- BCM_SETTEXTMARGIN
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 724c3e16c19aa2fb146bc0b47dec563db8b871536cb8f7e58fc86cbb739c225c
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119921364"
---
# <a name="bcm_settextmargin-message"></a>\_Сообщение СЕТТЕКСТМАРГИН BCM

Сообщение **\_ сеттекстмаргин BCM** задает поля для рисования текста в элементе управления "Кнопка".

## <a name="parameters"></a>Параметры

<dl> <dt>

*wParam* 
</dt> <dd>

Не используется; должно быть равно нулю.

</dd> <dt>

*lParam* 
</dt> <dd>

Указатель на структуру [**Rect**](/previous-versions//dd162897(v=vs.85)) , указывающую поля, используемые для рисования текста.

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



## <a name="see-also"></a>См. также

<dl> <dt>

**Ссылки**
</dt> <dt>

[**Кнопка " \_ сеттекстмаргин"**](/windows/desktop/api/Commctrl/nf-commctrl-button_settextmargin)
</dt> <dt>

**Зрения**
</dt> <dt>

[Кнопки](buttons.md)
</dt> </dl>

 

