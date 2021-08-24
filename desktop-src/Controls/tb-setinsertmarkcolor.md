---
title: Сообщение TB_SETINSERTMARKCOLOR (Коммктрл. h)
description: Задает цвет, используемый для отображения метки вставки для панели инструментов.
ms.assetid: 09a04449-9a1f-4f9a-b09f-9f22f930d735
keywords:
- элементы управления Windows сообщений TB_SETINSERTMARKCOLOR
topic_type:
- apiref
api_name:
- TB_SETINSERTMARKCOLOR
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 466c9bfe27462b11cc0c6cf3a183328ddedb1b422b4d0c07b4496c7a90f83890
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119540044"
---
# <a name="tb_setinsertmarkcolor-message"></a>\_Сообщение СЕТИНСЕРТМАРККОЛОР ТБ

Задает цвет, используемый для отображения метки вставки для панели инструментов.

## <a name="parameters"></a>Параметры

<dl> <dt>

*wParam* 
</dt> <dd>Должен равняться нулю.</dd> <dt>

*lParam* 
</dt> <dd>

Значение **COLORREF** , содержащее новый цвет метки вставки.

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Возвращает значение **COLORREF** , содержащее предыдущий цвет отметки вставки.

## <a name="requirements"></a>Requirements (Требования)



| Требование | Значение |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Windows \[Только классические приложения Vista\]<br/>                                        |
| Минимальная версия сервера<br/> | Windows Только для \[ настольных приложений сервера 2003\]<br/>                                  |
| Заголовок<br/>                   | <dl> <dt>Коммктрл. h</dt> </dl> |



## <a name="see-also"></a>См. также

<dl> <dt>

[**\_ЖЕТИНСЕРТМАРККОЛОР ТБ**](tb-getinsertmarkcolor.md)
</dt> </dl>

 

 





