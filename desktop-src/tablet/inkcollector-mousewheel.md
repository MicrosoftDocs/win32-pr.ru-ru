---
description: Событие InkCollector. Маусевхил — происходит при движении колесика мыши, когда объект InkCollector или InkOverlay имеет фокус.
ms.assetid: 418cf67c-0ec0-49e3-a17f-9eaeb40bb602
title: Событие InkCollector. Маусевхил (Мсинкаут. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 851a017af4bb71917c88e2194db86eec64218771
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2021
ms.locfileid: "108110142"
---
# <a name="inkcollectormousewheel-event"></a>Событие InkCollector. Маусевхил

Происходит при движении колесика мыши, когда объект [**InkCollector**](inkcollector-class.md) или [**InkOverlay**](inkoverlay-class.md) имеет фокус.

## <a name="syntax"></a>Синтаксис


```C++
void MouseWheel(
  [in]      InkMouseButton           Button,
  [in]      InkShiftKeyModifierFlags Shift,
  [in]      long                     Delta,
  [in]      long                     x,
  [in]      long                     y,
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

*Дельта* \[ окне\]
</dt> <dd>

Число со знаком для числа поворотов, повернутых колесиком мыши. Делением называется один зубец колесика мыши.

</dd> <dt>

*x* \[ в\]
</dt> <dd>

Координата по оси x (в пикселях) щелчка мыши.

</dd> <dt>

*y* \[ в\]
</dt> <dd>

Координата по оси y (в пикселях) щелчка мыши.

</dd> <dt>

*Отмена* \[ в, out\]
</dt> <dd>

**Вариант \_ Значение TRUE** , чтобы отменить событие для родительского элемента управления; в противном случае — **\_ значение false**. Значение по умолчанию — **Variant \_ false**.

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Это событие не возвращает значение.

## <a name="remarks"></a>Remarks

> [!Note]  
> Свойства *px* и *корректировки* находятся в пикселях, а не в HIMETRIC единицах, связанных с пространством рукописного ввода. Это связано с тем, что это событие заменяет связанное событие мыши приложения, не поддерживающего перо, и такого типа приложения распознает только пикселы.

 

Этот метод события определен в \_ \_ \_ интерфейсах диспетчеризации (DISP) иинкколлекторевентс, иинковерлайевентс и иинкпиктуривентс с идентификатором DISPID \_ ипемаусевхил.

## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Только классические приложения Windows XP Tablet PC Edition \[\]<br/>                                                       |
| Минимальная версия сервера<br/> | Ни одна версия не поддерживается<br/>                                                                                           |
| Header<br/>                   | <dl> <dt>Мсинкаут. h (также требуется Мсинкаут \_ i. c)</dt> </dl> |
| Библиотека<br/>                  | <dl> <dt>InkObj.dll</dt> </dl>                               |



## <a name="see-also"></a>См. также

<dl> <dt>

[**Класс InkCollector**](inkcollector-class.md)
</dt> <dt>

[**Перечисление Инкмаусебуттон**](/windows/desktop/api/msinkaut/ne-msinkaut-inkmousebutton)
</dt> <dt>

[**Перечисление Инкшифткэймодифиерфлагс**](/windows/desktop/api/msinkaut/ne-msinkaut-inkshiftkeymodifierflags)
</dt> </dl>

 

 




