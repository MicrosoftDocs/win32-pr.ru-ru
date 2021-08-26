---
title: Сообщение TVM_GETITEM (Коммктрл. h)
description: Извлекает некоторые или все атрибуты элемента представления дерева. Это сообщение можно отправить явно или с помощью \_ макроса элемента TreeView.
ms.assetid: e26ec000-967d-46de-8f71-6ebc36fefe5e
keywords:
- элементы управления Windows сообщений TVM_GETITEM
topic_type:
- apiref
api_name:
- TVM_GETITEM
- TVM_GETITEMA
- TVM_GETITEMW
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 425b0200df62b1cfcbc18556ad12513e43cebadf6e5742b36880464fad195fb8
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119984894"
---
# <a name="tvm_getitem-message"></a>\_Сообщение TVM

Извлекает некоторые или все атрибуты элемента представления дерева. Это сообщение можно отправить явно или с помощью макроса [**\_ элемента TreeView**](/windows/desktop/api/Commctrl/nf-commctrl-treeview_getitem) .

## <a name="parameters"></a>Параметры

<dl> <dt>

*wParam* 
</dt> <dd>Должен равняться нулю.</dd> <dt>

*lParam* 
</dt> <dd>

Указатель на структуру [**твитем**](/windows/win32/api/commctrl/ns-commctrl-tvitema) , указывающую сведения для извлечения и получения сведений об элементе. В [версии 4,71](common-control-versions.md) и более поздних вместо нее можно использовать структуру [**твитемекс**](/windows/win32/api/commctrl/ns-commctrl-tvitemexa) .

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Возвращает **значение true** , если успешно, или **false** в противном случае.

## <a name="remarks"></a>Remarks

Когда сообщение отправляется, элемент **хитем** структуры [**твитем**](/windows/win32/api/commctrl/ns-commctrl-tvitema) или [**твитемекс**](/windows/win32/api/commctrl/ns-commctrl-tvitemexa) определяет элемент для получения сведений, а элемент **Mask** задает атрибуты для извлечения.

Если для \_ элемента **Mask** в структуре [**твитем**](/windows/win32/api/commctrl/ns-commctrl-tvitema) или [**твитемекс**](/windows/win32/api/commctrl/ns-commctrl-tvitemexa) задан флаг текста твиф, то элемент **псзтекст** должен указывать на допустимый буфер, а элемент **кчтекстмакс** должен быть установлен в число символов в этом буфере.

## <a name="requirements"></a>Requirements (Требования)



| Требование | Значение |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Windows \[Только классические приложения Vista\]<br/>                                        |
| Минимальная версия сервера<br/> | Windows Только для \[ настольных приложений сервера 2003\]<br/>                                  |
| Заголовок<br/>                   | <dl> <dt>Коммктрл. h</dt> </dl> |
| Имя в кодировке Юникод и ANSI<br/>   | **TVM \_ ЖЕТИТЕМВ** (Юникод) и **TVM- \_ элемент** a (ANSI)<br/>                   |



 

 





