---
description: Происходит, когда подсказка курсора обращается к поверхности планшета в дигитайзере.
ms.assetid: 6d524400-1341-45da-86b2-098e34ed5a1c
title: Событие InkPicture. Курсордовн (Мсинкаут. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 15724f0a71e801393ca8e93100ba2105da9ff2b7
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "104546554"
---
# <a name="inkpicturecursordown-event"></a>Событие InkPicture. Курсордовн

Происходит, когда подсказка курсора обращается к поверхности планшета в дигитайзере.

## <a name="syntax"></a>Синтаксис


```C++
void CursorDown(
  [in] IInkCursor     *Cursor,
  [in] IInkStrokeDisp *Stroke
);
```



## <a name="parameters"></a>Параметры

<dl> <dt>

*Курсор* \[ окне\]
</dt> <dd>

Объект [**иинккурсор**](/windows/desktop/api/msinkaut/nn-msinkaut-iinkcursor) , создавший событие **курсордовн** .

</dd> <dt>

*Штриховая линия* \[ окне\]
</dt> <dd>

Объект [**иинкстрокедисп**](/windows/desktop/api/msinkaut/nn-msinkaut-iinkstrokedisp) , который был запущен, когда объект [**иинккурсор**](/windows/desktop/api/msinkaut/nn-msinkaut-iinkcursor) привел к срабатыванию события **курсордовн** .

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Это событие не возвращает значение.

## <a name="remarks"></a>Комментарии

Эти методы событий определены в интерфейсах **\_ иинкколлекторевентс**, **\_ иинковерлайевентс** и **\_ иинкпиктуривентс** . Интерфейсы **\_ иинкколлекторевентс**, **\_ иинковерлайевентс** и **\_ иинкпиктуривентс** реализуют интерфейс [**IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch) с идентификатором DISPID \_ ицекурсордовн.

Используйте это событие осторожно, так как оно может оказать негативное воздействие на производительность рукописного ввода, если в обработчиках событий выполняется слишком много кода. Чтобы улучшить производительность рукописного ввода в режиме реального времени, скройте или покажите курсор мыши в обработчиках событий [**MouseDown**](inkpicture-mousedown.md) и [**MouseUp**](inkpicture-mouseup.md) .

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

[**Событие Курсорбуттонуп**](inkpicture-cursorbuttonup.md)
</dt> <dt>

[**Событие Курсорбуттондовн**](inkpicture-cursorbuttondown.md)
</dt> <dt>

[**Интерфейс Иинккурсор**](/windows/desktop/api/msinkaut/nn-msinkaut-iinkcursor)
</dt> <dt>

[**Интерфейс Иинкстрокедисп**](/windows/desktop/api/msinkaut/nn-msinkaut-iinkstrokedisp)
</dt> </dl>

 

