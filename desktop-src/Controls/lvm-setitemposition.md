---
title: Сообщение LVM_SETITEMPOSITION (Коммктрл. h)
description: Перемещает элемент в указанную позицию в элементе управления "представление списка" (должен быть в виде значка или маленького значка). Это сообщение можно отправить явно или с помощью \_ макроса Сетитемпоситион ListView.
ms.assetid: dfb35af4-e6c3-40fc-9d7c-cf0d68a3ea01
keywords:
- Элементы управления Windows для LVM_SETITEMPOSITION сообщений
topic_type:
- apiref
api_name:
- LVM_SETITEMPOSITION
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b95fcf2949f1e19677bd445c0f6c5f762db078d1
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "103892018"
---
# <a name="lvm_setitemposition-message"></a>\_Сообщение LVM сетитемпоситион

Перемещает элемент в указанную позицию в элементе управления "представление списка" (должен быть в виде значка или маленького значка). Это сообщение можно отправить явно или с помощью макроса [**\_ сетитемпоситион ListView**](/windows/desktop/api/Commctrl/nf-commctrl-listview_setitemposition) .

## <a name="parameters"></a>Параметры

<dl> <dt>

*wParam* 
</dt> <dd>

Индекс элемента представления списка.

</dd> <dt>

*lParam* 
</dt> <dd>

[**Ловорд**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85)) указывает новую позицию по оси x верхнего левого угла элемента в координатах представления. [**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85)) указывает новую позицию y верхнего левого угла элемента в координатах представления.

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Возвращает **значение true** , если успешно, или **false** в противном случае.

## <a name="remarks"></a>Комментарии

Если элемент управления "список" имеет стиль [**\_ автоупорядочивания LVS**](list-view-window-styles.md) , элементы в элементе управления "список" упорядочиваются после установки позиции элемента.

В Windows Vista отправка этого сообщения в элемент управления "представление списка" с помощью [**стиля \_ авторазмещения LVS**](list-view-window-styles.md) ничего не делает, а возвращаемое значение равно **false**.

## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Только для \[ классических приложений Windows Vista\]<br/>                                        |
| Минимальная версия сервера<br/> | \[Только для настольных приложений Windows Server 2003\]<br/>                                  |
| Header<br/>                   | <dl> <dt>Коммктрл. h</dt> </dl> |



 

