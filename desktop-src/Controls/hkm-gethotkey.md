---
title: Сообщение HKM_GETHOTKEY (Коммктрл. h)
description: Получает виртуальный код ключа и флаги модификатора для горячего ключа из элемента управления горячего ключа.
ms.assetid: 8b061411-604d-46ea-a082-3eca2d47d992
keywords:
- элементы управления Windows сообщений HKM_GETHOTKEY
topic_type:
- apiref
api_name:
- HKM_GETHOTKEY
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 79bfbad1eb5e9a6679a1b3e419a0877e61cd90247ef0cf91b0a30c655f755a57
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "118672272"
---
# <a name="hkm_gethotkey-message"></a>\_Сообщение ХКМ

Получает виртуальный код ключа и флаги модификатора для горячего ключа из элемента управления горячего ключа.

## <a name="parameters"></a>Параметры

<dl> <dt>

*wParam* 
</dt> <dd>Должен равняться нулю.</dd> <dt>

*lParam* 
</dt> <dd>Должен равняться нулю.</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Возвращает код виртуального ключа и флаги модификатора. [**Лобите**](/previous-versions/windows/desktop/legacy/ms632658(v=vs.85)) [**ловорд**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85)) — это виртуальный код клавиши для сочетания клавиш. [**Хибите**](/previous-versions/windows/desktop/legacy/ms632656(v=vs.85)) **ловорд** — это модификатор ключа, который задает ключи, определяющие сочетание клавиш. Флаги модификатора могут быть сочетанием следующих значений.



| Значение            | Значение      |
|------------------|--------------|
| ХОТКЭЙФ \_ ALT     | ALT - клавиша      |
| \_элемент управления хоткэйф | Ключ управления  |
| ХОТКЭЙФ \_ ext     | Расширенный ключ |
| ХОТКЭЙФ \_ SHIFT   | Клавиша SHIFT    |



 

## <a name="remarks"></a>Remarks

16-разрядное значение, возвращаемое этим сообщением, можно использовать как параметр *wParam* в сообщении [**WM \_ сесоткэй**](/windows/desktop/inputdev/wm-sethotkey) .

## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Windows \[Только классические приложения Vista\]<br/>                                        |
| Минимальная версия сервера<br/> | Windows Только для \[ настольных приложений сервера 2003\]<br/>                                  |
| Header<br/>                   | <dl> <dt>Коммктрл. h</dt> </dl> |



 

