---
title: Сообщение CB_SETITEMDATA (Winuser. h)
description: Приложение отправляет \_ сообщение СЕТИТЕМДАТА CB, чтобы задать значение, связанное с указанным элементом в поле со списком.
ms.assetid: 8be9eb57-a635-4c52-9838-556368813c74
keywords:
- Элементы управления Windows для CB_SETITEMDATA сообщений
topic_type:
- apiref
api_name:
- CB_SETITEMDATA
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: bbb1603f9906ebf30a391b57bd812dc2002136c4
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "103892253"
---
# <a name="cb_setitemdata-message"></a>\_Сообщение СЕТИТЕМДАТА CB

Приложение отправляет сообщение **\_ сетитемдата CB** , чтобы задать значение, связанное с указанным элементом в поле со списком.

## <a name="parameters"></a>Параметры

<dl> <dt>

*wParam* 
</dt> <dd>

Указывает индекс (Отсчитываемый от нуля) элемента.

</dd> <dt>

*lParam* 
</dt> <dd>

Указывает новое значение, которое должно быть связано с элементом.

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Если возникает ошибка, возвращается значение CB \_ Err.

## <a name="remarks"></a>Комментарии

Если указанный элемент находится в поле со списком, рисуемом владельцем, созданным без стиля [**\_ хасстрингс CBS**](combo-box-styles.md) , это сообщение заменяет значение параметра *lParam* сообщения [**CB \_ ADDSTRING**](cb-addstring.md) или [**CB \_ инсертстринг**](cb-insertstring.md) , которое добавляет элемент в поле со списком.

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

[**\_ЖЕТИТЕМДАТА CB**](cb-getitemdata.md)
</dt> <dt>

[**\_ИНСЕРТСТРИНГ CB**](cb-insertstring.md)
</dt> </dl>

 

 





