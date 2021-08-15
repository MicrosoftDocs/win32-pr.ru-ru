---
title: Сообщение LVM_SETCOLUMN (Коммктрл. h)
description: Задает атрибуты столбца представления списка. Это сообщение можно отправить явно или с помощью \_ макроса Сетколумн ListView.
ms.assetid: 8ca1c269-fd86-4561-940d-b75f8ca2b731
keywords:
- элементы управления Windows сообщений LVM_SETCOLUMN
topic_type:
- apiref
api_name:
- LVM_SETCOLUMN
- LVM_SETCOLUMNW
- LVM_SETCOLUMNW
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: cca00e62d941a753c70e0dd31c1af4003fe639d49503be7009fe5a010febf0c8
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119019222"
---
# <a name="lvm_setcolumn-message"></a>\_Сообщение LVM сетколумн

Задает атрибуты столбца представления списка. Это сообщение можно отправить явно или с помощью макроса [**\_ сетколумн ListView**](/windows/desktop/api/Commctrl/nf-commctrl-listview_setcolumn) .

## <a name="parameters"></a>Параметры

<dl> <dt>

*wParam* 
</dt> <dd>

Индекс столбца.

</dd> <dt>

*lParam* 
</dt> <dd>

Указатель на структуру [**LVCOLUMN**](/windows/win32/api/commctrl/ns-commctrl-lvcolumna) , содержащую атрибуты нового столбца. Элемент **маски** указывает, какие атрибуты столбца задаются. Если элемент **Mask** задает \_ текстовое значение лвкф, то элемент **псзтекст** является адресом строки, завершающейся нулем, а элемент **кчтекстмакс** игнорируется.

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Возвращает **значение true** , если успешно, или **false** в противном случае.

## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Windows \[Только классические приложения Vista\]<br/>                                        |
| Минимальная версия сервера<br/> | Windows Только для \[ настольных приложений сервера 2003\]<br/>                                  |
| Header<br/>                   | <dl> <dt>Коммктрл. h</dt> </dl> |
| Имя в кодировке Юникод и ANSI<br/>   | **LVM \_ СЕТКОЛУМНВ** (Юникод) и **LVM \_ сетколумнв** (ANSI)<br/>               |



 

 





