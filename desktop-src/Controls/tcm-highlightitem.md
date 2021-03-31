---
title: Сообщение TCM_HIGHLIGHTITEM (Коммктрл. h)
description: Задает состояние выделения элемента вкладки. Это сообщение можно отправить явным образом или с помощью \_ макроса табктрл хигхлигхтитем.
ms.assetid: b0d0850a-62d9-46a1-8846-81f67a886ea8
keywords:
- Элементы управления Windows для TCM_HIGHLIGHTITEM сообщений
topic_type:
- apiref
api_name:
- TCM_HIGHLIGHTITEM
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 55664aeeeefadfcb5205b9a5bde4fee1aafdfef3
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "103892525"
---
# <a name="tcm_highlightitem-message"></a>\_Сообщение ХИГХЛИГХТИТЕМ TCM

Задает состояние выделения элемента вкладки. Это сообщение можно отправить явным образом или с помощью макроса [**табктрл \_ хигхлигхтитем**](/windows/desktop/api/Commctrl/nf-commctrl-tabctrl_highlightitem) .

## <a name="parameters"></a>Параметры

<dl> <dt>

*wParam* 
</dt> <dd>

Значение **типа int** , указывающее Отсчитываемый от нуля индекс элемента управления вкладки.

</dd> <dt>

*lParam* 
</dt> <dd>

[**Ловорд**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85)) — это **логическое** значение, определяющее выделенное состояние выделения. Если это значение равно **true**, вкладка выделена; Если **значение равно false**, то для вкладки задано состояние по умолчанию. [**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85)) должен быть равен нулю.

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Возвращает ненулевое значение в случае успеха или ноль в противном случае.

## <a name="remarks"></a>Комментарии

В Comctl32.dll версии 6,0 это сообщение не отображается, если тема активна.

## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Только для \[ классических приложений Windows Vista\]<br/>                                        |
| Минимальная версия сервера<br/> | \[Только для настольных приложений Windows Server 2003\]<br/>                                  |
| Header<br/>                   | <dl> <dt>Коммктрл. h</dt> </dl> |



 

