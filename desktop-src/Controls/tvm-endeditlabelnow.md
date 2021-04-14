---
title: Сообщение TVM_ENDEDITLABELNOW (Коммктрл. h)
description: Завершает редактирование метки элемента древовидного представления. Это сообщение можно отправить явно или с помощью \_ макроса Ендедитлабелнов TreeView.
ms.assetid: 68de2020-9311-4958-859a-de55f5e41fcf
keywords:
- Элементы управления Windows для TVM_ENDEDITLABELNOW сообщений
topic_type:
- apiref
api_name:
- TVM_ENDEDITLABELNOW
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4f059be20560adeb8cbcb0c63a2555283f6b7051
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104533974"
---
# <a name="tvm_endeditlabelnow-message"></a>\_Сообщение TVM ендедитлабелнов

Завершает редактирование метки элемента древовидного представления. Это сообщение можно отправить явно или с помощью макроса [**\_ ендедитлабелнов TreeView**](/windows/desktop/api/Commctrl/nf-commctrl-treeview_endeditlabelnow) .

## <a name="parameters"></a>Параметры

<dl> <dt>

*wParam* 
</dt> <dd>

Переменная, которая указывает, отменяется ли редактирование без сохранения в метке. Если этот параметр имеет **значение true**, система отменяет редактирование без сохранения изменений. В противном случае система сохранит изменения в метке.

</dd> <dt>

*lParam* 
</dt> <dd>Должен равняться нулю.</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Возвращает **значение true** , если успешно, или **false** в противном случае.

## <a name="remarks"></a>Комментарии

Это сообщение вызывает отправку кода уведомления [ТВН \_ ендлабеледит](tvn-endlabeledit.md) в родительское окно элемента управления "дерево-представление".

## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Только для \[ классических приложений Windows Vista\]<br/>                                        |
| Минимальная версия сервера<br/> | \[Только для настольных приложений Windows Server 2003\]<br/>                                  |
| Header<br/>                   | <dl> <dt>Коммктрл. h</dt> </dl> |



 

 





