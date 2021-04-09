---
title: Сообщение TVM_INSERTITEM (Коммктрл. h)
description: Вставляет новый элемент в элемент управления представлением в виде дерева. Это сообщение можно отправить явно или с помощью \_ макроса InsertItem TreeView.
ms.assetid: c5e5f88f-6ec8-4b95-89ea-97f6f1fd735e
keywords:
- Элементы управления Windows для TVM_INSERTITEM сообщений
topic_type:
- apiref
api_name:
- TVM_INSERTITEM
- TVM_INSERTITEMA
- TVM_INSERTITEMW
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 719de4c2391ff924c9f6deb8cb4206cfdb56c3ba
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "103891641"
---
# <a name="tvm_insertitem-message"></a>\_Сообщение TVM INSERTITEM

Вставляет новый элемент в элемент управления представлением в виде дерева. Это сообщение можно отправить явно или с помощью макроса [**\_ InsertItem TreeView**](/windows/desktop/api/Commctrl/nf-commctrl-treeview_insertitem) .

## <a name="parameters"></a>Параметры

<dl> <dt>

*wParam* 
</dt> <dd>Должен равняться нулю.</dd> <dt>

*lParam* 
</dt> <dd>

Указатель на структуру [**твинсертструкт**](/windows/win32/api/commctrl/ns-commctrl-tvinsertstructa) , указывающую атрибуты элемента представления дерева.

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Возвращает маркер **хтриитем** для нового элемента, если он успешно, или **значение NULL** в противном случае.

## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Только для \[ классических приложений Windows Vista\]<br/>                                        |
| Минимальная версия сервера<br/> | \[Только для настольных приложений Windows Server 2003\]<br/>                                  |
| Header<br/>                   | <dl> <dt>Коммктрл. h</dt> </dl> |
| Имя в кодировке Юникод и ANSI<br/>   | **TVM \_ ИНСЕРТИТЕМВ** (Юникод) и **TVM \_ инсертитема** (ANSI)<br/>             |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[ТВН \_ ендлабеледит](tvn-endlabeledit.md)
</dt> </dl>

 

 





