---
title: Сообщение CB_SETITEMDATA (Winuser. h)
description: Приложение отправляет \_ сообщение СЕТИТЕМДАТА CB, чтобы задать значение, связанное с указанным элементом в поле со списком.
ms.assetid: 8be9eb57-a635-4c52-9838-556368813c74
keywords:
- элементы управления Windows сообщений CB_SETITEMDATA
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
ms.openlocfilehash: 7abd50db9050178bc5d8d3b8ff556bce90f340fdb8d6692a514b0348aceeeab3
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "120089014"
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

## <a name="remarks"></a>Remarks

Если указанный элемент находится в поле со списком, рисуемом владельцем, созданным без стиля [**\_ хасстрингс CBS**](combo-box-styles.md) , это сообщение заменяет значение параметра *lParam* сообщения [**CB \_ ADDSTRING**](cb-addstring.md) или [**CB \_ инсертстринг**](cb-insertstring.md) , которое добавляет элемент в поле со списком.

## <a name="requirements"></a>Requirements (Требования)



| Требование | Значение |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Windows \[Только классические приложения Vista\]<br/>                                                           |
| Минимальная версия сервера<br/> | Windows Только для \[ настольных приложений сервера 2003\]<br/>                                                     |
| Заголовок<br/>                   | <dl> <dt>Winuser. h (включает Windows. h)</dt> </dl> |



## <a name="see-also"></a>См. также

<dl> <dt>

**Ссылки**
</dt> <dt>

[**\_ADDSTRING CB**](cb-addstring.md)
</dt> <dt>

[**\_ЖЕТИТЕМДАТА CB**](cb-getitemdata.md)
</dt> <dt>

[**\_ИНСЕРТСТРИНГ CB**](cb-insertstring.md)
</dt> </dl>

 

 





