---
title: Сообщение RB_INSERTBAND (Коммктрл. h)
description: Вставляет новый полосу в элемент управления главной панели.
ms.assetid: ac621f65-b8ab-41d6-928d-a48fbea572e7
keywords:
- элементы управления Windows сообщений RB_INSERTBAND
topic_type:
- apiref
api_name:
- RB_INSERTBAND
- RB_INSERTBANDA
- RB_INSERTBANDW
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e0e21020302e4dcbfeb75f4a57d37be4b5c5703668231e8ec8e9dd9bd9577cbb
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119770164"
---
# <a name="rb_insertband-message"></a>\_Сообщение ИНСЕРТБАНД RB

Вставляет новый полосу в элемент управления главной панели.

## <a name="parameters"></a>Параметры

<dl> <dt>

*wParam* 
</dt> <dd>

Отсчитываемый от нуля индекс расположения, в которое будет вставлен полоса. Если задать для этого параметра значение-1, элемент управления добавит новую полосу в последнее расположение.

</dd> <dt>

*lParam* 
</dt> <dd>

Указатель на структуру [**ребарбандинфо**](/windows/win32/api/commctrl/ns-commctrl-rebarbandinfoa) , определяющую полосу для вставки. Перед отправкой этого сообщения необходимо задать для элемента **кбсизе** этой структуры значение **sizeof**(ребарбандинфо).

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Возвращает ненулевое значение в случае успеха или ноль в противном случае.

## <a name="requirements"></a>Requirements (Требования)



| Требование | Значение |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Windows \[Только классические приложения Vista\]<br/>                                        |
| Минимальная версия сервера<br/> | Windows Только для \[ настольных приложений сервера 2003\]<br/>                                  |
| Заголовок<br/>                   | <dl> <dt>Коммктрл. h</dt> </dl> |
| Имя в кодировке Юникод и ANSI<br/>   | **RB \_ ИНСЕРТБАНДВ** (Юникод) и **RB \_ инсертбанда** (ANSI)<br/>               |



 

 





