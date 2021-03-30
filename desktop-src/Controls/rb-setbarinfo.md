---
title: Сообщение RB_SETBARINFO (Коммктрл. h)
description: Задает характеристики элемента управления главной панели.
ms.assetid: e4413d46-574f-4ccd-b5fd-3ba6c1e3924b
keywords:
- Элементы управления Windows для RB_SETBARINFO сообщений
topic_type:
- apiref
api_name:
- RB_SETBARINFO
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b360bc0b4d14963619aad8f769634d7dd0ad17e5
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104071178"
---
# <a name="rb_setbarinfo-message"></a>\_Сообщение СЕТБАРИНФО RB

Задает характеристики элемента управления главной панели.

## <a name="parameters"></a>Параметры

<dl> <dt>

*wParam* 
</dt> <dd>Должен равняться нулю.</dd> <dt>

*lParam* 
</dt> <dd>

Указатель на структуру [**ребаринфо**](/windows/win32/api/commctrl/ns-commctrl-rebarinfo) , содержащую данные, которые необходимо задать. Перед отправкой этого сообщения необходимо задать для элемента **кбсизе** этой структуры значение **sizeof**(ребаринфо).

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Возвращает ненулевое значение в случае успеха или ноль в противном случае.

## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Только для \[ классических приложений Windows Vista\]<br/>                                        |
| Минимальная версия сервера<br/> | \[Только для настольных приложений Windows Server 2003\]<br/>                                  |
| Header<br/>                   | <dl> <dt>Коммктрл. h</dt> </dl> |



 

 





