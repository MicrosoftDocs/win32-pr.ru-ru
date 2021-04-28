---
description: Событие InkPicture. Курсорбуттонуп — происходит, когда InkCollector обнаруживает, что кнопка курсора находится в up.
ms.assetid: bb10b032-a88d-4b52-9062-c0b63dfe98e9
title: Событие InkPicture. Курсорбуттонуп (Мсинкаут. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 639d0cbd89e2ca44d8855b6508c5284f59a7c654
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2021
ms.locfileid: "108086662"
---
# <a name="inkpicturecursorbuttonup-event"></a>Событие InkPicture. Курсорбуттонуп

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

Объект [**интерфейса иинккурсор**](/windows/desktop/api/msinkaut/nn-msinkaut-iinkcursor) , создавший событие **курсорбуттонуп** .

</dd> <dt>

*Кнопка "* \[ окне\]
</dt> <dd>

Кнопка, которая была выпущена.

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Это событие не возвращает значение.

## <a name="remarks"></a>Remarks

Кнопка в подсказке пера работает, когда пользователь завершает штрих и отрывает перо от дигитайзера. Кнопка на элементе с назначением находится вверх, когда кнопка не нажата.

Когда вы отпустите правую кнопку мыши, вы получаете два события **курсорбуттонуп** : одно для правой кнопки вверх, а другое — для кнопки слева.

Этот метод события определен в DISP-интерфейсах **\_ иинкколлекторевентс**, **\_ иинковерлайевентс** и **\_ иинкпиктуривентс** с идентификатором DISPID \_ ицекурсорбуттонуп.

## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Только классические приложения Windows XP Tablet PC Edition \[\]<br/>                                                       |
| Минимальная версия сервера<br/> | Ни одна версия не поддерживается<br/>                                                                                           |
| Header<br/>                   | <dl> <dt>Мсинкаут. h (также требуется Мсинкаут \_ i. c)</dt> </dl> |
| Библиотека<br/>                  | <dl> <dt>InkObj.dll</dt> </dl>                               |



## <a name="see-also"></a>См. также

<dl> <dt>

[InkPicture](inkpicture-control-reference.md)
</dt> <dt>

[**Событие Курсорбуттондовн**](inkpicture-cursorbuttondown.md)
</dt> <dt>

[**Событие Курсордовн**](inkpicture-cursordown.md)
</dt> <dt>

[**Интерфейс Иинккурсор**](/windows/desktop/api/msinkaut/nn-msinkaut-iinkcursor)
</dt> <dt>

[**Интерфейс Иинккурсорбуттон**](/windows/desktop/api/msinkaut/nn-msinkaut-iinkcursorbutton)
</dt> </dl>

 

 




