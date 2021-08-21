---
description: Событие InkCollector. Курсордовн — происходит, когда подсказка курсора обращается к планшету с дигитайзером.
ms.assetid: bf914849-ef33-4746-b2e1-c768cd1d87aa
title: Событие InkCollector. Курсордовн (Мсинкаут. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 65a98a58ce3c6576b45b4c60d47781f8de6ae9f8d5ab0cfea3222ef36890290f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119032122"
---
# <a name="inkcollectorcursordown-event"></a>Событие InkCollector. Курсордовн

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

## <a name="remarks"></a>Remarks

Этот метод события определен в \_ иинкколлекторевентс, \_ иинковерлайевентс и \_ иинкпиктуривентс. \_интерфейсы иинкколлекторевентс, \_ иинковерлайевентс и \_ иинкпиктуривентс реализуют интерфейс [**IDISPATCH**](/windows/win32/api/oaidl/nn-oaidl-idispatch) с идентификатором DISPID \_ ицекурсордовн.

Используйте это событие осторожно, так как оно может оказать негативное воздействие на производительность рукописного ввода, если в обработчиках событий выполняется слишком много кода. Чтобы улучшить производительность рукописного ввода в режиме реального времени, скройте или покажите курсор мыши в обработчиках событий [**MouseDown**](inkcollector-mousedown.md) и [**MouseUp**](inkcollector-mouseup.md) .

## <a name="requirements"></a>Requirements (Требования)



| Требование | Значение |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Windows XP Tablet PC Edition \[ только классические приложения\]<br/>                                                       |
| Минимальная версия сервера<br/> | Ни одна версия не поддерживается<br/>                                                                                           |
| Заголовок<br/>                   | <dl> <dt>Мсинкаут. h (также требуется Мсинкаут \_ i. c)</dt> </dl> |
| Библиотека<br/>                  | <dl> <dt>InkObj.dll</dt> </dl>                               |



## <a name="see-also"></a>См. также

<dl> <dt>

[**Класс InkCollector**](inkcollector-class.md)
</dt> <dt>

[**Событие Курсорбуттондовн**](inkcollector-cursorbuttondown.md)
</dt> <dt>

[**Событие Курсорбуттонуп**](inkcollector-cursorbuttonup.md)
</dt> <dt>

[**Интерфейс Иинккурсор**](/windows/desktop/api/msinkaut/nn-msinkaut-iinkcursor)
</dt> <dt>

[**Интерфейс Иинкстрокедисп**](/windows/desktop/api/msinkaut/nn-msinkaut-iinkstrokedisp)
</dt> </dl>

 

