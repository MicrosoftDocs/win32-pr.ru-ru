---
title: Сообщение DTM_GETIDEALSIZE (Коммктрл. h)
description: Возвращает размер, необходимый для вывода элемента управления без усечения. Отправляйте это сообщение явным образом или с помощью \_ макроса DateTime жетидеалсизе.
ms.assetid: 15ec26a1-645b-4a96-af66-1031e1a46c6c
keywords:
- Элементы управления Windows для DTM_GETIDEALSIZE сообщений
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
ms.openlocfilehash: a979883f431fea4627f52fe19c3716341e3f2328
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104262187"
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

## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Только для \[ классических приложений Windows Vista\]<br/>                                        |
| Минимальная версия сервера<br/> | \[Только для настольных приложений Windows Server 2008\]<br/>                                  |
| Header<br/>                   | <dl> <dt>Коммктрл. h</dt> </dl> |



 

