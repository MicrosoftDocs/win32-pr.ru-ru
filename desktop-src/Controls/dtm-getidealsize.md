---
title: Сообщение DTM_GETIDEALSIZE (Коммктрл. h)
description: Возвращает размер, необходимый для вывода элемента управления без усечения. Отправляйте это сообщение явным образом или с помощью \_ макроса DateTime жетидеалсизе.
ms.assetid: 15ec26a1-645b-4a96-af66-1031e1a46c6c
keywords:
- элементы управления Windows сообщений DTM_GETIDEALSIZE
topic_type:
- apiref
api_name:
- DTM_GETIDEALSIZE
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 639fbbb25fbf61695f83b54f106f45ff3dd421f528807120be52edd7031e4f66
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119878234"
---
# <a name="dtm_getidealsize-message"></a>\_Сообщение DTM жетидеалсизе

Возвращает размер, необходимый для вывода элемента управления без усечения. Отправляйте это сообщение явным образом или с помощью макроса [**DateTime \_ жетидеалсизе**](/windows/desktop/api/Commctrl/nf-commctrl-datetime_getidealsize) .

## <a name="parameters"></a>Параметры

<dl> <dt>

*wParam* 
</dt> <dd>

Не используется. Должен равняться нулю.

</dd> <dt>

*lParam* 
</dt> <dd>

Указатель на структуру [**размера**](/previous-versions//dd145106(v=vs.85)) для получения идеального размера. Вызывающее приложение отвечает за выделение этой структуры.

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Возвращает **значение true**.

## <a name="requirements"></a>Requirements (Требования)



| Требование | Значение |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Windows \[Только классические приложения Vista\]<br/>                                        |
| Минимальная версия сервера<br/> | Windows Только для \[ настольных приложений сервера 2008\]<br/>                                  |
| Заголовок<br/>                   | <dl> <dt>Коммктрл. h</dt> </dl> |



 

