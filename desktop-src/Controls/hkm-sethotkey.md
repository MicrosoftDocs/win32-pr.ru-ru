---
title: Сообщение HKM_SETHOTKEY (Коммктрл. h)
description: Задает сочетание горячих клавиш для элемента управления "горячий ключ".
ms.assetid: 372a7b2f-d9d5-43a8-9c06-730f2f5dc56e
keywords:
- Элементы управления Windows для HKM_SETHOTKEY сообщений
topic_type:
- apiref
api_name:
- HKM_SETHOTKEY
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a3672136c44c0268e218e7f87cbbeb3373b76b39
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104534037"
---
# <a name="hkm_sethotkey-message"></a>\_Сообщение ХКМ сесоткэй

Задает сочетание горячих клавиш для элемента управления "горячий ключ".

## <a name="parameters"></a>Параметры

<dl> <dt>

*wParam* 
</dt> <dd>

[**Лобите**](/previous-versions/windows/desktop/legacy/ms632658(v=vs.85)) [**ловорд**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85)) — это виртуальный код клавиши для сочетания клавиш. [**Хибите**](/previous-versions/windows/desktop/legacy/ms632656(v=vs.85)) **ловорд** — это модификатор ключа, который указывает ключи, определяющие сочетание клавиш. Список значений флагов модификаторов см. в описании сообщения ХКМ- [**\_ горячих клавиш**](hkm-gethotkey.md) .

</dd> <dt>

*lParam* 
</dt> <dd>

Не используется; должно быть равно нулю.

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Всегда возвращает значение 0.

## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Только для \[ классических приложений Windows Vista\]<br/>                                        |
| Минимальная версия сервера<br/> | \[Только для настольных приложений Windows Server 2003\]<br/>                                  |
| Header<br/>                   | <dl> <dt>Коммктрл. h</dt> </dl> |



 

