---
title: Сообщение TB_SETWINDOWTHEME (Коммктрл. h)
description: Задает визуальный стиль элемента управления ToolBar.
ms.assetid: 8b05c561-af66-47e7-8ef3-7f9f81da4840
keywords:
- элементы управления Windows сообщений TB_SETWINDOWTHEME
topic_type:
- apiref
api_name:
- TB_SETWINDOWTHEME
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d1f3f4ae5f6e7a3a05670a8ba9bfe533156e1ef3e6043ff2a039744da705da39
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119078128"
---
# <a name="tb_setwindowtheme-message"></a>\_Сообщение SETWINDOWTHEME ТБ

Задает визуальный стиль элемента управления ToolBar.

## <a name="parameters"></a>Параметры

<dl> <dt>

*wParam* 
</dt> <dd>Должен равняться нулю.</dd> <dt>

*lParam* 
</dt> <dd>

Указатель на строку в Юникоде, содержащую стиль отображения панели инструментов, который необходимо задать.

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Возвращаемое значение не используется.

## <a name="remarks"></a>Remarks

> [!Note]  
> Чтобы использовать это сообщение, необходимо указать манифест, указывающий Comclt32.dll версии 6,0. Дополнительные сведения о манифестах см. в разделе [Включение визуальных стилей](cookbook-overview.md).

 

Отправка этого сообщения эквивалентна вызову [**SetWindowTheme**](/windows/desktop/api/Uxtheme/nf-uxtheme-setwindowtheme) на панели инструментов и ее элементе управления ToolTip, если таковой имеется.

## <a name="requirements"></a>Requirements (Требования)



| Требование | Значение |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Windows \[Только классические приложения Vista\]<br/>                                        |
| Минимальная версия сервера<br/> | Windows Только для \[ настольных приложений сервера 2003\]<br/>                                  |
| Заголовок<br/>                   | <dl> <dt>Коммктрл. h</dt> </dl> |



 

 





