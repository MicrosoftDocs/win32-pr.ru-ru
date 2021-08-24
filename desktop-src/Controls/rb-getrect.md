---
title: Сообщение RB_GETRECT (Коммктрл. h)
description: Извлекает ограничивающий прямоугольник для заданной полосы в элементе управления "Главная панель".
ms.assetid: e272b090-1e4d-4cff-87f0-557ad8116e7e
keywords:
- элементы управления Windows сообщений RB_GETRECT
topic_type:
- apiref
api_name:
- RB_GETRECT
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 43d2f085fa7c6f413700156999f1325879f91affc2c8984fb33d08cb6cc90b66
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "118169300"
---
# <a name="rb_getrect-message"></a>\_Сообщение RB

Извлекает ограничивающий прямоугольник для заданной полосы в элементе управления "Главная панель".

## <a name="parameters"></a>Параметры

<dl> <dt>

*wParam* 
</dt> <dd>

Отсчитываемый от нуля индекс полосы в элементе управления главной панели.

</dd> <dt>

*lParam* 
</dt> <dd>

Указатель на структуру [**Rect**](/previous-versions//dd162897(v=vs.85)) , которая будет принимать границы полосы-панели.

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Возвращает ненулевое значение в случае успеха или ноль в противном случае.

## <a name="requirements"></a>Requirements (Требования)



| Требование | Значение |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Windows \[Только классические приложения Vista\]<br/>                                        |
| Минимальная версия сервера<br/> | Windows Только для \[ настольных приложений сервера 2003\]<br/>                                  |
| Заголовок<br/>                   | <dl> <dt>Коммктрл. h</dt> </dl> |



 

