---
title: Сообщение LVM_REDRAWITEMS (Коммктрл. h)
description: Заставляет элемент управления "представление списка" перерисовывать диапазон элементов. Это сообщение можно отправить явно или с помощью \_ макроса Редравитемс ListView.
ms.assetid: a717b17f-6e0a-4804-96f9-da93392a19ec
keywords:
- Элементы управления Windows для LVM_REDRAWITEMS сообщений
topic_type:
- apiref
api_name:
- LVM_REDRAWITEMS
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 42568a9ab78361a28a99eee372674287a24d03cf
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104071605"
---
# <a name="lvm_redrawitems-message"></a>\_Сообщение LVM редравитемс

Заставляет элемент управления "представление списка" перерисовывать диапазон элементов. Это сообщение можно отправить явно или с помощью макроса [**\_ редравитемс ListView**](/windows/desktop/api/Commctrl/nf-commctrl-listview_redrawitems) .

## <a name="parameters"></a>Параметры

<dl> <dt>

*wParam* 
</dt> <dd>

Индекс первого элемента для перерисовки.

</dd> <dt>

*lParam* 
</dt> <dd>

Индекс последнего элемента для перерисовки.

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Возвращает **значение true** , если успешно, или **false** в противном случае.

## <a name="remarks"></a>Комментарии

Указанные элементы на самом деле не перерисовывается до тех пор, пока окно списка представлений не получит сообщение [**WM \_ Paint**](/windows/desktop/gdi/wm-paint) для перерисовки. Для немедленного перерисовки вызовите функцию [**упдатевиндов**](/windows/desktop/api/winuser/nf-winuser-updatewindow) после использования этого макроса.

## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Только для \[ классических приложений Windows Vista\]<br/>                                        |
| Минимальная версия сервера<br/> | \[Только для настольных приложений Windows Server 2003\]<br/>                                  |
| Header<br/>                   | <dl> <dt>Коммктрл. h</dt> </dl> |



 

