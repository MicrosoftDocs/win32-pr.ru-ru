---
description: Событие InkCollector. Курсорбуттондовн — возникает, когда класс InkCollector обнаруживает недоступную кнопку курсора.
ms.assetid: 65e7f68b-f911-4634-b850-178eb6eaf86e
title: Событие InkCollector. Курсорбуттондовн (Мсинкаут. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e2c8a2c1a2e832d4fd18c7c84f9905d0aa1694b425f5f5e7ece91e96afc1684f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "118451297"
---
# <a name="inkcollectorcursorbuttondown-event"></a>Событие InkCollector. Курсорбуттондовн

Происходит, когда [**класс InkCollector**](inkcollector-class.md) обнаруживает недоступную кнопку курсора.

## <a name="syntax"></a>Синтаксис


```C++
void CursorButtonDown(
  [in] IInkCursor       *Cursor,
  [in] IInkCursorButton *Button
);
```



## <a name="parameters"></a>Параметры

<dl> <dt>

*Курсор* \[ окне\]
</dt> <dd>

Объект [**иинккурсор**](/windows/desktop/api/msinkaut/nn-msinkaut-iinkcursor) , создавший событие **курсорбуттондовн** .

</dd> <dt>

*Кнопка "* \[ окне\]
</dt> <dd>

Нажатая кнопка.

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Это событие не возвращает значение.

## <a name="remarks"></a>Remarks

Кнопка в подсказке пера не работает, когда пользователь перемещает перо на дигитайзер и начинает трассировку штриха. Кнопка на элементе с назначением не работает при нажатии кнопки.

При нажатии правой кнопки мыши фактически появляется два события **курсорбуттондовн** : одна для нажатой правой кнопки, а другая для нажатой левой кнопки.

Этот метод события определен в \_ \_ \_ интерфейсах диспетчеризации (DISP) иинкколлекторевентс, иинковерлайевентс и иинкпиктуривентс с идентификатором DISPID \_ ицекурсорбуттондовн.

## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Windows XP Tablet PC Edition \[ только классические приложения\]<br/>                                                       |
| Минимальная версия сервера<br/> | Ни одна версия не поддерживается<br/>                                                                                           |
| Header<br/>                   | <dl> <dt>Мсинкаут. h (также требуется Мсинкаут \_ i. c)</dt> </dl> |
| Библиотека<br/>                  | <dl> <dt>InkObj.dll</dt> </dl>                               |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[**Класс InkCollector**](inkcollector-class.md)
</dt> <dt>

[**Событие Курсордовн**](inkcollector-cursordown.md)
</dt> <dt>

[**Событие Курсорбуттонуп**](inkcollector-cursorbuttonup.md)
</dt> <dt>

[**Интерфейс Иинккурсор**](/windows/desktop/api/msinkaut/nn-msinkaut-iinkcursor)
</dt> <dt>

[**Интерфейс Иинккурсорбуттон**](/windows/desktop/api/msinkaut/nn-msinkaut-iinkcursorbutton)
</dt> </dl>

 

 




