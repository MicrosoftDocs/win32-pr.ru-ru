---
title: Сообщение TB_SETBITMAPSIZE (Коммктрл. h)
description: Задает размер растровых изображений, добавляемых на панель инструментов.
ms.assetid: 20b99cd8-6ef1-4037-92d2-c64a1003b5fe
keywords:
- Элементы управления Windows для TB_SETBITMAPSIZE сообщений
topic_type:
- apiref
api_name:
- TB_SETBITMAPSIZE
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8d9c8a717151041fb83b7a0206acf570a6ad7f76
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104489030"
---
# <a name="tb_setbitmapsize-message"></a>\_Сообщение СЕТБИТМАПСИЗЕ ТБ

Задает размер растровых изображений, добавляемых на панель инструментов.

## <a name="parameters"></a>Параметры

<dl> <dt>

*wParam* 
</dt> <dd>

Должен равняться нулю.

</dd> <dt>

*lParam* 
</dt> <dd>

[**Ловорд**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85)) задает ширину (в пикселях) растровых изображений. [**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85)) задает высоту растровых изображений в пикселях.

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Возвращает **значение true** , если успешно, или **false** в противном случае.

## <a name="remarks"></a>Комментарии

Размер можно задать только перед добавлением точечных рисунков на панель инструментов. Если в приложении явно не задан размер точечного рисунка, размер по умолчанию равен 16 x 15 пикселей.

## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Только для \[ классических приложений Windows Vista\]<br/>                                        |
| Минимальная версия сервера<br/> | \[Только для настольных приложений Windows Server 2003\]<br/>                                  |
| Header<br/>                   | <dl> <dt>Коммктрл. h</dt> </dl> |



 

