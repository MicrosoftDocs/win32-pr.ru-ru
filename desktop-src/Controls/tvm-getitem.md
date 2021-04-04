---
title: Сообщение TVM_GETITEM (Коммктрл. h)
description: Извлекает некоторые или все атрибуты элемента представления дерева. Это сообщение можно отправить явно или с помощью \_ макроса элемента TreeView.
ms.assetid: e26ec000-967d-46de-8f71-6ebc36fefe5e
keywords:
- Элементы управления Windows для TVM_GETITEM сообщений
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
ms.openlocfilehash: dff96f4721a3c50eda54792b2b1c003cd808bf11
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104137827"
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

## <a name="remarks"></a>Комментарии

Когда сообщение отправляется, элемент **хитем** структуры [**твитем**](/windows/win32/api/commctrl/ns-commctrl-tvitema) или [**твитемекс**](/windows/win32/api/commctrl/ns-commctrl-tvitemexa) определяет элемент для получения сведений, а элемент **Mask** задает атрибуты для извлечения.

Если для \_ элемента **Mask** в структуре [**твитем**](/windows/win32/api/commctrl/ns-commctrl-tvitema) или [**твитемекс**](/windows/win32/api/commctrl/ns-commctrl-tvitemexa) задан флаг текста твиф, то элемент **псзтекст** должен указывать на допустимый буфер, а элемент **кчтекстмакс** должен быть установлен в число символов в этом буфере.

## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Только для \[ классических приложений Windows Vista\]<br/>                                        |
| Минимальная версия сервера<br/> | \[Только для настольных приложений Windows Server 2003\]<br/>                                  |
| Header<br/>                   | <dl> <dt>Коммктрл. h</dt> </dl> |
| Имя в кодировке Юникод и ANSI<br/>   | **TVM \_ ЖЕТИТЕМВ** (Юникод) и **TVM- \_ элемент** a (ANSI)<br/>                   |



 

 





