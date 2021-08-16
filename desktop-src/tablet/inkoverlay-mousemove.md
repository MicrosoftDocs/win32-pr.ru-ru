---
description: Событие InkOverlay. MouseMove — происходит при перемещении указателя мыши по объекту InkCollector или InkOverlay.
ms.assetid: b25aeead-9fb1-4221-82fa-ce2d81f5fed8
title: Событие InkOverlay. MouseMove (Мсинкаут. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e8b4bec85062f1cf07edefd3f5712c43b12bdbe98b5773a962372bb00a186fee
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "118219810"
---
# <a name="inkoverlaymousemove-event"></a>Событие InkOverlay. MouseMove

Происходит при перемещении указателя мыши над объектом [**InkCollector**](inkcollector-class.md) или [**InkOverlay**](inkoverlay-class.md) .

## <a name="syntax"></a>Синтаксис


```C++
void MouseMove(
  [in]      InkMouseButton           Button,
  [in]      InkShiftKeyModifierFlags Shift,
  [in]      long                     pX,
  [in]      long                     pY,
  [in, out] VARIANT_BOOL             *Cancel
);
```



## <a name="parameters"></a>Параметры

<dl> <dt>

*Кнопка "* \[ окне\]
</dt> <dd>

Нажатая кнопка мыши.

</dd> <dt>

*SHIFT* \[ окне\]
</dt> <dd>

Состояние клавиши SHIFT.

</dd> <dt>

*ПКС* \[ окне\]
</dt> <dd>

Координата по оси x (в пикселях) щелчка мыши.

</dd> <dt>

*Копировать* \[ в окне\]
</dt> <dd>

Координата по оси y (в пикселях) щелчка мыши.

</dd> <dt>

*Отмена* \[ в, out\]
</dt> <dd>

Следует ли отменять событие для родительского элемента управления. Значение по умолчанию — **false**, которое указывает, что событие не должно быть отменено.

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Это событие не возвращает значение.

## <a name="remarks"></a>Remarks

> [!Note]  
> Свойства *px* и *корректировки* находятся в пикселях, а не в HIMETRIC единицах, связанных с пространством рукописного ввода. Это связано с тем, что это событие заменяет связанное событие мыши приложения, не поддерживающего перо, и такого типа приложения распознает только пикселы.

 

> [!Note]  
> Некоторые элементы управления используют определенную связь между событиями [**MouseDown**](inkcollector-mousedown.md), [**MouseMove**](inkcollector-mousemove.md)и [**MouseUp**](inkcollector-mouseup.md) . Отмена некоторых из этих событий может привести к непредвиденным результатам.

 

Этот метод события определен в \_ \_ \_ интерфейсах диспетчеризации (DISP) иинкколлекторевентс, иинковерлайевентс и иинкпиктуривентс с идентификатором DISPID \_ ипемаусемове.

## <a name="requirements"></a>Требования



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

[**Перечисление Инкмаусебуттон**](/windows/desktop/api/msinkaut/ne-msinkaut-inkmousebutton)
</dt> <dt>

[**Перечисление Инкшифткэймодифиерфлагс**](/windows/desktop/api/msinkaut/ne-msinkaut-inkshiftkeymodifierflags)
</dt> </dl>

 

 




