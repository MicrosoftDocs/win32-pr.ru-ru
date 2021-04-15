---
title: Сообщение BCM_GETNOTE (Коммктрл. h)
description: Возвращает текст заметки, связанной с кнопкой ссылки на команду. Это сообщение можно отправить явным образом или воспользоваться макросом "Кнопка" \_ .
ms.assetid: ddaf4227-1316-49b5-abf0-00215472c46c
keywords:
- Элементы управления Windows для BCM_GETNOTE сообщений
topic_type:
- apiref
api_name:
- BCM_GETNOTE
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 758dac90ba4c0f3087a6df90d9acf2c1321b1d73
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "105654528"
---
# <a name="bcm_getnote-message"></a>\_Сообщение о НЕзамете BCM

Возвращает текст заметки, связанной с кнопкой ссылки на команду. Это сообщение можно отправить явным образом или воспользоваться макросом [**"Кнопка" \_**](/windows/desktop/api/Commctrl/nf-commctrl-button_getnote) .

## <a name="parameters"></a>Параметры

<dl> <dt>

*wParam* \[ в, out\]
</dt> <dd>

Значение **типа DWORD** , указывающее размер буфера, на который указывает *lParam*, в символах.

</dd> <dt>

*lParam* \[ заполняет\]
</dt> <dd>

Буфер строки для получения текста. Размер буфера должен быть достаточным для размещения завершающего нуль символа.

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Если сообщение завершается с ошибкой, возвращается **значение true**. В противном случае возвращается **значение false**.

## <a name="remarks"></a>Комментарии

Сообщение **BCM/ \_ Note** работает только с кнопками, у которых есть стиль кнопки [**BS \_ коммандлинк**](button-styles.md) или [**BS \_ дефкоммандлинк**](button-styles.md) .

[**GetLastError**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror) будет содержать:

-   Ошибка \_ не \_ поддерживается, если у кнопки нет стиля " [**BS \_ Дефкоммандлинк**](button-styles.md) " или " [**BS \_ коммандлинк**](button-styles.md) ".
-   Ошибка \_ \_ не хватает буфера, если буфер *lParam* слишком мал. Параметр *wParam* будет содержать требуемый размер буфера в символах.

## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Только для \[ классических приложений Windows Vista\]<br/>                                        |
| Минимальная версия сервера<br/> | \[Только для настольных приложений Windows Server 2008\]<br/>                                  |
| Header<br/>                   | <dl> <dt>Коммктрл. h</dt> </dl> |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

**Ссылки**
</dt> <dt>

[Стили кнопок](button-styles.md)
</dt> <dt>

**Зрения**
</dt> <dt>

[Типы кнопок](button-types-and-styles.md)
</dt> </dl>

 

