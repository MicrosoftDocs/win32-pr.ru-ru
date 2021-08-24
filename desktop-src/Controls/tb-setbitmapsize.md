---
title: Сообщение TB_SETBITMAPSIZE (Коммктрл. h)
description: Задает размер растровых изображений, добавляемых на панель инструментов.
ms.assetid: 20b99cd8-6ef1-4037-92d2-c64a1003b5fe
keywords:
- элементы управления Windows сообщений TB_SETBITMAPSIZE
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
ms.openlocfilehash: db2a26dacd63c00d1dd793163facce0ab4a45302e85dde11522f8844977eb0ff
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "118167977"
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

## <a name="remarks"></a>Remarks

Размер можно задать только перед добавлением точечных рисунков на панель инструментов. Если в приложении явно не задан размер точечного рисунка, размер по умолчанию равен 16 x 15 пикселей.

## <a name="requirements"></a>Requirements (Требования)



| Требование | Значение |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Windows \[Только классические приложения Vista\]<br/>                                        |
| Минимальная версия сервера<br/> | Windows Только для \[ настольных приложений сервера 2003\]<br/>                                  |
| Заголовок<br/>                   | <dl> <dt>Коммктрл. h</dt> </dl> |



 

