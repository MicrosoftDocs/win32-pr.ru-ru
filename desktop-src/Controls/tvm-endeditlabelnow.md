---
title: Сообщение TVM_ENDEDITLABELNOW (Коммктрл. h)
description: Завершает редактирование метки элемента древовидного представления. Это сообщение можно отправить явно или с помощью \_ макроса Ендедитлабелнов TreeView.
ms.assetid: 68de2020-9311-4958-859a-de55f5e41fcf
keywords:
- элементы управления Windows сообщений TVM_ENDEDITLABELNOW
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
ms.openlocfilehash: 18355edc8efb18ea56a39e60c68361a7ef8d72e39af644707d6d102738fd60c6
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119387264"
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

## <a name="remarks"></a>Remarks

Это сообщение вызывает отправку кода уведомления [ТВН \_ ендлабеледит](tvn-endlabeledit.md) в родительское окно элемента управления "дерево-представление".

## <a name="requirements"></a>Requirements (Требования)



| Требование | Значение |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Windows \[Только классические приложения Vista\]<br/>                                        |
| Минимальная версия сервера<br/> | Windows Только для \[ настольных приложений сервера 2003\]<br/>                                  |
| Header<br/>                   | <dl> <dt>Коммктрл. h</dt> </dl> |



 

 





