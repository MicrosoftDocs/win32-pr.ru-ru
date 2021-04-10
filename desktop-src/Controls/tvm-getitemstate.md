---
title: Сообщение TVM_GETITEMSTATE (Коммктрл. h)
description: Извлекает некоторые или все атрибуты состояния элемента представления дерева. Это сообщение можно отправить явно или с помощью \_ макроса Жетитемстате TreeView.
ms.assetid: 89aaaa82-2809-4e4e-a325-5666a57c5cbb
keywords:
- Элементы управления Windows для TVM_GETITEMSTATE сообщений
topic_type:
- apiref
api_name:
- TVM_GETITEMSTATE
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b851ff3845743c802a2a914a0f40d5d9eb65c6a8
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104071804"
---
# <a name="tvm_getitemstate-message"></a>\_Сообщение TVM жетитемстате

Извлекает некоторые или все атрибуты состояния элемента представления дерева. Это сообщение можно отправить явно или с помощью макроса [**\_ жетитемстате TreeView**](/windows/desktop/api/Commctrl/nf-commctrl-treeview_getitemstate) .

## <a name="parameters"></a>Параметры

<dl> <dt>

*wParam* 
</dt> <dd>

Маркер для элемента.

</dd> <dt>

*lParam* 
</dt> <dd>

Маска, используемая для указания состояний для запроса. Он эквивалентен элементу **статемаск** элемента [**твитемекс**](/windows/win32/api/commctrl/ns-commctrl-tvitemexa).

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Возвращает значение **uint** с соответствующими битами состояния, установленным в **значение true**. Будут установлены только те биты, которые указаны в параметре *lParam* и имеют **значение true** . Это значение эквивалентно значению элемента **State** объекта [**твитемекс**](/windows/win32/api/commctrl/ns-commctrl-tvitemexa).

## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Только для \[ классических приложений Windows Vista\]<br/>                                        |
| Минимальная версия сервера<br/> | \[Только для настольных приложений Windows Server 2003\]<br/>                                  |
| Header<br/>                   | <dl> <dt>Коммктрл. h</dt> </dl> |



 

 





