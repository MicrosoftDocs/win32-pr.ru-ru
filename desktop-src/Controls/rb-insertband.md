---
title: Сообщение RB_INSERTBAND (Коммктрл. h)
description: Вставляет новый полосу в элемент управления главной панели.
ms.assetid: ac621f65-b8ab-41d6-928d-a48fbea572e7
keywords:
- Элементы управления Windows для RB_INSERTBAND сообщений
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
ms.openlocfilehash: c39b45eb662fb4c2058b87837352339c84762188
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "103892809"
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

## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Только для \[ классических приложений Windows Vista\]<br/>                                        |
| Минимальная версия сервера<br/> | \[Только для настольных приложений Windows Server 2003\]<br/>                                  |
| Header<br/>                   | <dl> <dt>Коммктрл. h</dt> </dl> |
| Имя в кодировке Юникод и ANSI<br/>   | **RB \_ ИНСЕРТБАНДВ** (Юникод) и **RB \_ инсертбанда** (ANSI)<br/>               |



 

 





