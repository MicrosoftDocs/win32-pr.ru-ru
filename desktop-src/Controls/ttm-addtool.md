---
title: Сообщение TTM_ADDTOOL (Коммктрл. h)
description: Регистрирует инструмент с помощью элемента управления ToolTip.
ms.assetid: c974866b-20e7-45bc-914e-9dcf9af161e0
keywords:
- элементы управления Windows сообщений TTM_ADDTOOL
topic_type:
- apiref
api_name:
- TTM_ADDTOOL
- TTM_ADDTOOLA
- TTM_ADDTOOLW
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: bb66c43033e54ce51b396ff5bb11efe3b2a99e8eb2578a2e9fe4d4bc4487ccf0
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119769544"
---
# <a name="ttm_addtool-message"></a>\_Сообщение ТТМ аддтул

Регистрирует инструмент с помощью элемента управления ToolTip.

## <a name="parameters"></a>Параметры

<dl> <dt>

*wParam* 
</dt> <dd>Должен равняться нулю.</dd> <dt>

*lParam* 
</dt> <dd>

Указатель на структуру [**тулинфо**](/windows/win32/api/commctrl/ns-commctrl-tttoolinfoa) , содержащую сведения, необходимые элементу управления ToolTip для показа текста для инструмента. Перед отправкой этого сообщения необходимо заполнить элемент **кбсизе** этой структуры.

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Возвращает **значение true** , если успешно, или **false** в противном случае.

## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Windows \[Только классические приложения Vista\]<br/>                                        |
| Минимальная версия сервера<br/> | Windows Только для \[ настольных приложений сервера 2003\]<br/>                                  |
| Заголовок<br/>                   | <dl> <dt>Коммктрл. h</dt> </dl> |
| Имя в кодировке Юникод и ANSI<br/>   | **ТТМ \_ АДДТУЛВ** (Юникод) и **ТТМ \_ аддтула** (ANSI)<br/>                   |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

**Ссылки**
</dt> <dt>

[**ТТМ \_ делтул**](ttm-deltool.md)
</dt> <dt>

**Зрения**
</dt> <dt>

[Сведения об элементах управления ToolTip](tooltip-controls.md)
</dt> </dl>

 

 





