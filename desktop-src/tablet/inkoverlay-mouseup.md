---
description: Событие InkOverlay. MouseUp — происходит, когда указатель мыши находится над объектом InkCollector или InkOverlay и отпущена кнопка мыши.
ms.assetid: 049e1560-d4b2-4d34-9d54-2b45217001b2
title: Событие InkOverlay. MouseUp (Мсинкаут. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 402083aa677b134ea469980227a482ac5546da2b
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2021
ms.locfileid: "108086812"
---
# <a name="inkoverlaymouseup-event"></a>Событие InkOverlay. MouseUp

Происходит при отпускании кнопки мыши, когда указатель мыши находится над объектом [**InkCollector**](inkcollector-class.md) или [**InkOverlay**](inkoverlay-class.md) .

## <a name="syntax"></a>Синтаксис


```C++
void MouseUp(
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

Отжатая кнопка мыши.

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

Чтобы улучшить производительность рукописного ввода в режиме реального времени, скройте или покажите курсор мыши в обработчиках событий [**MouseDown**](inkcollector-mousedown.md) и [**MouseUp**](inkcollector-mouseup.md) .

> [!Note]  
> Свойства *px* и *корректировки* находятся в пикселях, а не в HIMETRIC единицах, связанных с пространством рукописного ввода. Это связано с тем, что это событие заменяет связанное событие мыши приложения, не поддерживающего перо, и такого типа приложения распознает только пикселы.

 

> [!Note]  
> Некоторые элементы управления используют определенную связь между событиями [**MouseDown**](inkcollector-mousedown.md), [**MouseMove**](inkcollector-mousemove.md)и [**MouseUp**](inkcollector-mouseup.md) . Отмена некоторых из этих событий может привести к непредвиденным результатам.

 

Этот метод события определен в \_ \_ \_ интерфейсах диспетчеризации (DISP) иинкколлекторевентс, иинковерлайевентс и иинкпиктуривентс с идентификатором DISPID \_ ипемаусеуп.

## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Только классические приложения Windows XP Tablet PC Edition \[\]<br/>                                                       |
| Минимальная версия сервера<br/> | Ни одна версия не поддерживается<br/>                                                                                           |
| Header<br/>                   | <dl> <dt>Мсинкаут. h (также требуется Мсинкаут \_ i. c)</dt> </dl> |
| Библиотека<br/>                  | <dl> <dt>InkObj.dll</dt> </dl>                               |



## <a name="see-also"></a>См. также

<dl> <dt>

[**Класс InkOverlay**](inkoverlay-class.md)
</dt> <dt>

[**Перечисление Инкмаусебуттон**](/windows/desktop/api/msinkaut/ne-msinkaut-inkmousebutton)
</dt> <dt>

[**Перечисление Инкшифткэймодифиерфлагс**](/windows/desktop/api/msinkaut/ne-msinkaut-inkshiftkeymodifierflags)
</dt> </dl>

 

 




