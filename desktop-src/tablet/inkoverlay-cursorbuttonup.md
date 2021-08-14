---
description: Событие InkOverlay. Курсорбуттонуп — происходит, когда InkCollector обнаруживает, что кнопка курсора находится в установленном положении.
ms.assetid: ce7205f7-727c-4acf-a727-4dbb3cc42441
title: Событие InkOverlay. Курсорбуттонуп (Мсинкаут. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 60e94fb9c1727e0c8fce13f3696397462fdf590c076627df869dcafd177190c9
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "118220853"
---
# <a name="inkoverlaycursorbuttonup-event"></a>Событие InkOverlay. Курсорбуттонуп

Происходит, когда [**InkCollector**](inkcollector-class.md) обнаруживает кнопку курсора, которая находится в up.

## <a name="syntax"></a>Синтаксис


```C++
void CursorButtonUp(
  [in] IInkCursor       *Cursor,
  [in] IInkCursorButton *Button
);
```



## <a name="parameters"></a>Параметры

<dl> <dt>

*Курсор* \[ окне\]
</dt> <dd>

Объект [**интерфейса иинккурсор**](/windows/desktop/api/msinkaut/nn-msinkaut-iinkcursor) , создавший событие [**курсорбуттонуп**](inkcollector-cursorbuttonup.md) .

</dd> <dt>

*Кнопка "* \[ окне\]
</dt> <dd>

Кнопка, которая была выпущена.

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Это событие не возвращает значение.

## <a name="remarks"></a>Remarks

Кнопка в подсказке пера работает, когда пользователь завершает штрих и отрывает перо от дигитайзера. Кнопка на элементе с назначением находится вверх, когда кнопка не нажата.

Когда вы отпустите правую кнопку мыши, вы получаете два события [**курсорбуттонуп**](inkcollector-cursorbuttonup.md) : одно для правой кнопки вверх, а другое — для кнопки слева.

Этот метод события определен в \_ \_ \_ интерфейсах диспетчеризации (DISP) иинкколлекторевентс, иинковерлайевентс и иинкпиктуривентс с идентификатором DISPID \_ ицекурсорбуттонуп.

## <a name="requirements"></a>Requirements (Требования)



| Требование | Значение |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Windows XP Tablet PC Edition \[ только классические приложения\]<br/>                                                       |
| Минимальная версия сервера<br/> | Ни одна версия не поддерживается<br/>                                                                                           |
| Header<br/>                   | <dl> <dt>Мсинкаут. h (также требуется Мсинкаут \_ i. c)</dt> </dl> |
| Библиотека<br/>                  | <dl> <dt>InkObj.dll</dt> </dl>                               |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[**Класс InkOverlay**](inkoverlay-class.md)
</dt> <dt>

[**Событие Курсорбуттондовн**](inkcollector-cursorbuttondown.md)
</dt> <dt>

[**Событие Курсордовн**](inkcollector-cursordown.md)
</dt> <dt>

[**Интерфейс Иинккурсор**](/windows/desktop/api/msinkaut/nn-msinkaut-iinkcursor)
</dt> <dt>

[**Интерфейс Иинккурсорбуттон**](/windows/desktop/api/msinkaut/nn-msinkaut-iinkcursorbutton)
</dt> </dl>

 

 




