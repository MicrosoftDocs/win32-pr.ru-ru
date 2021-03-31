---
title: Сообщение LVM_SETCOLUMN (Коммктрл. h)
description: Задает атрибуты столбца представления списка. Это сообщение можно отправить явно или с помощью \_ макроса Сетколумн ListView.
ms.assetid: 8ca1c269-fd86-4561-940d-b75f8ca2b731
keywords:
- Элементы управления Windows для LVM_SETCOLUMN сообщений
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
ms.openlocfilehash: 7251da70c7ac1e2cb7bbcf7b3e220a2f6cdf055f
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "103988691"
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
| Минимальная версия клиента<br/> | Только для \[ классических приложений Windows Vista\]<br/>                                        |
| Минимальная версия сервера<br/> | \[Только для настольных приложений Windows Server 2003\]<br/>                                  |
| Header<br/>                   | <dl> <dt>Коммктрл. h</dt> </dl> |
| Имя в кодировке Юникод и ANSI<br/>   | **LVM \_ СЕТКОЛУМНВ** (Юникод) и **LVM \_ сетколумнв** (ANSI)<br/>               |



 

 





