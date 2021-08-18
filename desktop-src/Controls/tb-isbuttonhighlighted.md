---
title: Сообщение TB_ISBUTTONHIGHLIGHTED (Коммктрл. h)
description: Проверяет состояние выделения кнопки на панели инструментов.
ms.assetid: d5aab670-a989-46f2-b4f8-d8a8968cbe07
keywords:
- элементы управления Windows сообщений TB_ISBUTTONHIGHLIGHTED
topic_type:
- apiref
api_name:
- TB_ISBUTTONHIGHLIGHTED
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 903932fddb7bf356a89adda0513a045d099a22c459add6401818eec54a3f0657
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119918374"
---
# <a name="tb_isbuttonhighlighted-message"></a>\_Сообщение ИСБУТТОНХИГХЛИГХТЕД ТБ

Проверяет состояние выделения кнопки на панели инструментов.

## <a name="parameters"></a>Параметры

<dl> <dt>

*wParam* 
</dt> <dd>

Идентификатор команды для кнопки панели инструментов.

</dd> <dt>

*lParam* 
</dt> <dd>Должен равняться нулю.</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Возвращает ненулевое значение, если кнопка выделяется, или ноль в противном случае.

## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Windows \[Только классические приложения Vista\]<br/>                                        |
| Минимальная версия сервера<br/> | Windows Только для \[ настольных приложений сервера 2003\]<br/>                                  |
| Заголовок<br/>                   | <dl> <dt>Коммктрл. h</dt> </dl> |



 

 





