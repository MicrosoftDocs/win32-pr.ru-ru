---
title: Сообщение CB_GETMINVISIBLE (Коммктрл. h)
description: Возвращает минимальное число видимых элементов в раскрывающемся списке поля со списком.
ms.assetid: 9861358a-1ef9-4d78-8ec8-561b97f3f18e
keywords:
- Элементы управления Windows для CB_GETMINVISIBLE сообщений
topic_type:
- apiref
api_name:
- CB_GETMINVISIBLE
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3dcf4fe5088d9c994e232a64ba16bbddf11b0d48
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "103891918"
---
# <a name="cb_getminvisible-message"></a>\_Сообщение ЖЕТМИНВИСИБЛЕ CB

Возвращает минимальное число видимых элементов в раскрывающемся списке поля со списком.

## <a name="parameters"></a>Параметры

<dl> <dt>

*wParam* 
</dt> <dd>

Не используется; должно быть равно нулю.

</dd> <dt>

*lParam* 
</dt> <dd>

Не используется; должно быть равно нулю.

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Возвращаемое значение — это минимальное число видимых элементов.

## <a name="remarks"></a>Комментарии

Если число элементов в раскрывающемся списке больше минимального, в поле со списком используется полоса прокрутки.

Это сообщение пропускается, если элемент управления "поле со списком" имеет стиль [**CBS \_ ноинтегралхеигхт**](combo-box-styles.md).

Чтобы использовать **CB \_ жетминвисибле**, приложение должно указать comctl32.dll версии 6 в манифесте. Дополнительные сведения см. в разделе [Включение визуальных стилей](cookbook-overview.md).

## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Только для \[ классических приложений Windows Vista\]<br/>                                        |
| Минимальная версия сервера<br/> | \[Только для настольных приложений Windows Server 2003\]<br/>                                  |
| Header<br/>                   | <dl> <dt>Коммктрл. h</dt> </dl> |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

**Ссылки**
</dt> <dt>

[**\_СЕТМИНВИСИБЛЕ CB**](cb-setminvisible.md)
</dt> <dt>

[**Поле со списком \_ жетминвисибле**](/windows/desktop/api/Commctrl/nf-commctrl-combobox_getminvisible)
</dt> </dl>

 

 





