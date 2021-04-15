---
title: Сообщение CB_SETLOCALE (Winuser. h)
description: Приложение отправляет \_ сообщение CB SETLOCALE для установки текущего языкового стандарта поля со списком. Если поле со списком имеет \_ стиль сортировки CBS и строки добавляются с помощью CB \_ ADDSTRING, языковой стандарт поля со списком влияет на порядок сортировки элементов списка.
ms.assetid: 06f9c69d-1220-490f-bc67-6e125f696e87
keywords:
- Элементы управления Windows для CB_SETLOCALE сообщений
topic_type:
- apiref
api_name:
- CB_SETLOCALE
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 025f33dc8ba236965a98ca984446b04846ecd2ba
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104491541"
---
# <a name="cb_setlocale-message"></a>\_Сообщение CB SETLOCALE

Приложение отправляет сообщение **CB \_ SETLOCALE** для установки текущего языкового стандарта поля со списком. Если поле со списком имеет стиль [**\_ сортировки CBS**](combo-box-styles.md) и строки добавляются с помощью [**CB \_ ADDSTRING**](cb-addstring.md), языковой стандарт поля со списком влияет на порядок сортировки элементов списка.

## <a name="parameters"></a>Параметры

<dl> <dt>

*wParam* 
</dt> <dd>

Задает код локали для поля со списком, используемого для сортировки при добавлении текста.

</dd> <dt>

*lParam* 
</dt> <dd>

Этот параметр не используется.

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Возвращаемое значение — это предыдущий идентификатор локали. Если параметр *wParam* задает языковой стандарт, не установленный в системе, возвращается значение CB \_ Err, а текущий языковой стандарт поля со списком не изменяется.

## <a name="remarks"></a>Комментарии

Используйте макрос [**макелЦид**](/windows/desktop/api/winnt/nf-winnt-makelcid) для создания идентификатора языкового стандарта и макроса [**макелангид**](/windows/desktop/api/winnt/nf-winnt-makelangid) для создания идентификатора языка. Идентификатор языка состоит из основного идентификатора языка и идентификатора языка.

## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Только для \[ классических приложений Windows Vista\]<br/>                                                           |
| Минимальная версия сервера<br/> | \[Только для настольных приложений Windows Server 2003\]<br/>                                                     |
| Header<br/>                   | <dl> <dt>Winuser. h (включение Windows. h)</dt> </dl> |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

**Ссылки**
</dt> <dt>

[**\_ADDSTRING CB**](cb-addstring.md)
</dt> <dt>

[**CB \_ ЦБ**](cb-getlocale.md)
</dt> <dt>

**Другие ресурсы**
</dt> <dt>

[**макелангид**](/windows/desktop/api/winnt/nf-winnt-makelangid)
</dt> <dt>

[**макелЦид**](/windows/desktop/api/winnt/nf-winnt-makelcid)
</dt> </dl>

 

