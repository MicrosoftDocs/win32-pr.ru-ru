---
title: Сообщение HKM_GETHOTKEY (Коммктрл. h)
description: Получает виртуальный код ключа и флаги модификатора для горячего ключа из элемента управления горячего ключа.
ms.assetid: 8b061411-604d-46ea-a082-3eca2d47d992
keywords:
- Элементы управления Windows для HKM_GETHOTKEY сообщений
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
ms.openlocfilehash: 16e23e02f32a4dd6f82f61fd735688353f48ec19
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104490212"
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



 

## <a name="remarks"></a>Комментарии

16-разрядное значение, возвращаемое этим сообщением, можно использовать как параметр *wParam* в сообщении [**WM \_ сесоткэй**](/windows/desktop/inputdev/wm-sethotkey) .

## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Только для \[ классических приложений Windows Vista\]<br/>                                        |
| Минимальная версия сервера<br/> | \[Только для настольных приложений Windows Server 2003\]<br/>                                  |
| Header<br/>                   | <dl> <dt>Коммктрл. h</dt> </dl> |



 

