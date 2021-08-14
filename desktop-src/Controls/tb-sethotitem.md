---
title: Сообщение TB_SETHOTITEM (Коммктрл. h)
description: TB_SETHOTITEM сообщение — задает горячий элемент на панели инструментов.
ms.assetid: 15005741-29d2-48c6-b5f0-15178a49b917
keywords:
- элементы управления Windows сообщений TB_SETHOTITEM
topic_type:
- apiref
api_name:
- TB_SETHOTITEM
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a48de58e07d877d999c2d0388bf32845fce349511da563c3a6b1fa9f9c7b3d20
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119318844"
---
# <a name="tb_sethotitem-message"></a>\_Сообщение СЕСОТИТЕМ ТБ

Задает горячий элемент на панели инструментов.

## <a name="parameters"></a>Параметры

<dl> <dt>

*wParam* 
</dt> <dd>

Индекс элемента, который будет активным. Если это значение равно-1, ни один из элементов не будет активным.

</dd> <dt>

*lParam* 
</dt> <dd>Должен равняться нулю.</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Возвращает индекс предыдущего горячего элемента или значение-1, если элемент не был активным.

## <a name="remarks"></a>Remarks

Поведение этого сообщения не определено для панелей инструментов, не имеющих [**\_ неструктурированного стиля тбстиле**](toolbar-control-and-button-styles.md) .

## <a name="requirements"></a>Requirements (Требования)



| Требование | Значение |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Windows \[Только классические приложения Vista\]<br/>                                        |
| Минимальная версия сервера<br/> | Windows Только для \[ настольных приложений сервера 2003\]<br/>                                  |
| Header<br/>                   | <dl> <dt>Коммктрл. h</dt> </dl> |



 

 





