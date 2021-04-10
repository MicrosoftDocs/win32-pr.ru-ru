---
description: Происходит, когда класс InkCollector обнаруживает недоступную кнопку курсора.
ms.assetid: 9ee2c19e-8a44-428b-a4c1-3c7250dcdeda
title: Событие InkPicture. Курсорбуттондовн (Мсинкаут. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4531f41ce597d9cbb1fa0b8665a1821a8a32dd3e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "104266153"
---
# <a name="inkpicturecursorbuttondown-event"></a>Событие InkPicture. Курсорбуттондовн

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

## <a name="remarks"></a>Комментарии

Кнопка в подсказке пера не работает, когда пользователь перемещает перо на дигитайзер и начинает трассировку штриха. Кнопка на элементе с назначением не работает при нажатии кнопки.

При нажатии правой кнопки мыши фактически появляется два события **курсорбуттондовн** : одна для нажатой правой кнопки, а другая для нажатой левой кнопки.

Этот метод события определен в интерфейсе диспетчеризации **\_ иинкколлекторевентс**, **\_ иинковерлайевентс** и **\_ иинкпиктуривентс** с идентификатором DISPID \_ ицекурсорбуттондовн.

## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Только классические приложения Windows XP Tablet PC Edition \[\]<br/>                                                       |
| Минимальная версия сервера<br/> | Ни одна версия не поддерживается<br/>                                                                                           |
| Header<br/>                   | <dl> <dt>Мсинкаут. h (также требуется Мсинкаут \_ i. c)</dt> </dl> |
| Библиотека<br/>                  | <dl> <dt>InkObj.dll</dt> </dl>                               |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[InkPicture](inkpicture-control-reference.md)
</dt> <dt>

[**Событие Курсордовн**](inkpicture-cursordown.md)
</dt> <dt>

[**Событие Курсорбуттонуп**](inkpicture-cursorbuttonup.md)
</dt> <dt>

[**Интерфейс Иинккурсор**](/windows/desktop/api/msinkaut/nn-msinkaut-iinkcursor)
</dt> <dt>

[**Интерфейс Иинккурсорбуттон**](/windows/desktop/api/msinkaut/nn-msinkaut-iinkcursorbutton)
</dt> </dl>

 

 




