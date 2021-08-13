---
title: Сообщение HKM_SETHOTKEY (Коммктрл. h)
description: Задает сочетание горячих клавиш для элемента управления "горячий ключ".
ms.assetid: 372a7b2f-d9d5-43a8-9c06-730f2f5dc56e
keywords:
- элементы управления Windows сообщений HKM_SETHOTKEY
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
ms.openlocfilehash: 0ae397e3034e917eec85a6b56397cbac8b14a59af03aca6ebee08fec89cf6b53
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "118672262"
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
| Минимальная версия клиента<br/> | Windows \[Только классические приложения Vista\]<br/>                                        |
| Минимальная версия сервера<br/> | Windows Только для \[ настольных приложений сервера 2003\]<br/>                                  |
| Header<br/>                   | <dl> <dt>Коммктрл. h</dt> </dl> |



 

