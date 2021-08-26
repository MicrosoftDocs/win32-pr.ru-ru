---
title: Сообщение TB_GETEXTENDEDSTYLE (Коммктрл. h)
description: Извлекает расширенные стили для элемента управления ToolBar.
ms.assetid: d9e31a8e-5e5a-4d2d-bc3b-65ac40e8592f
keywords:
- элементы управления Windows сообщений TB_GETEXTENDEDSTYLE
topic_type:
- apiref
api_name:
- TB_GETEXTENDEDSTYLE
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4ab059933c2019009ebc746cc59df6affb840f09c40a201a4ee4048dc2498a17
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119918864"
---
# <a name="tb_getextendedstyle-message"></a>\_Сообщение ЖЕТЕКСТЕНДЕДСТИЛЕ ТБ

Извлекает расширенные стили для элемента управления ToolBar.

## <a name="parameters"></a>Параметры

<dl> <dt>

*wParam* 
</dt> <dd>Должен равняться нулю.</dd> <dt>

*lParam* 
</dt> <dd>Должен равняться нулю.</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Возвращает **DWORD** , представляющий стили, используемые в данный момент для элемента управления ToolBar. Это значение может быть сочетанием [расширенных стилей](toolbar-extended-styles.md).

## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Windows \[Только классические приложения Vista\]<br/>                                        |
| Минимальная версия сервера<br/> | Windows Только для \[ настольных приложений сервера 2003\]<br/>                                  |
| Заголовок<br/>                   | <dl> <dt>Коммктрл. h</dt> </dl> |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[**\_СЕТЕКСТЕНДЕДСТИЛЕ ТБ**](tb-setextendedstyle.md)
</dt> </dl>

 

 





