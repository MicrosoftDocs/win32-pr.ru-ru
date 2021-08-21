---
title: Сообщение TB_PRESSBUTTON (Коммктрл. h)
description: Нажимает или освобождает указанную кнопку на панели инструментов.
ms.assetid: 03f6c3c2-d679-4e3a-a07b-c7e46c97972a
keywords:
- элементы управления Windows сообщений TB_PRESSBUTTON
topic_type:
- apiref
api_name:
- TB_PRESSBUTTON
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8c72bd3e58b06510463fcfb872060d7fcbb529ce3e5a96376ae8cb25e142d9e0
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "118168014"
---
# <a name="tb_pressbutton-message"></a>\_Сообщение ПРЕССБУТТОН ТБ

Нажимает или освобождает указанную кнопку на панели инструментов.

## <a name="parameters"></a>Параметры

<dl> <dt>

*wParam* 
</dt> <dd>

Идентификатор команды для нажатия или выпуска.

</dd> <dt>

*lParam* 
</dt> <dd>

[**Ловорд**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85)) — это **логическое** значение, указывающее, следует ли нажать или отпустить указанную кнопку. Если **значение равно true**, кнопка нажата. Если **значение равно false**, кнопка отпущена.

[**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85)) должен быть равен нулю.

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Возвращает **значение true** , если успешно, или **false** в противном случае.

## <a name="requirements"></a>Requirements (Требования)



| Требование | Значение |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Windows \[Только классические приложения Vista\]<br/>                                        |
| Минимальная версия сервера<br/> | Windows Только для \[ настольных приложений сервера 2003\]<br/>                                  |
| Заголовок<br/>                   | <dl> <dt>Коммктрл. h</dt> </dl> |



 

