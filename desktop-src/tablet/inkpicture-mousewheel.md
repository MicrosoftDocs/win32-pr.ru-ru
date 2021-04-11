---
description: Происходит при движении колесика мыши, когда элемент управления InkPicture имеет фокус.
ms.assetid: f56a8af9-7618-4fa3-8dd5-aa81a7f817e4
title: Событие InkPicture. Маусевхил (Мсинкаут. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6cab870f3a00b2aa0cea3c003993e2b35cd2abbf
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "104346112"
---
# <a name="inkpicturemousewheel-event"></a>Событие InkPicture. Маусевхил

Происходит при движении колесика мыши, когда элемент управления [InkPicture](inkpicture-control-reference.md) имеет фокус.

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

Нажатая кнопка.

</dd> <dt>

*SHIFT* \[ окне\]
</dt> <dd>

Состояние клавиши SHIFT.

</dd> <dt>

*Дельта* \[ окне\]
</dt> <dd>

Расстояние, которое было включено колесиком мыши.

</dd> <dt>

*x* \[ в\]
</dt> <dd>

Координата x (в пикселях) объекта [**иинккурсор**](/windows/desktop/api/msinkaut/nn-msinkaut-iinkcursor) .

</dd> <dt>

*y* \[ в\]
</dt> <dd>

Координата по оси y (в пикселях) объекта [**иинккурсор**](/windows/desktop/api/msinkaut/nn-msinkaut-iinkcursor) .

</dd> <dt>

*Отмена* \[ в, out\]
</dt> <dd>

ВАРИАНТ \_ true, чтобы отменить событие **маусевхил** для родительского элемента управления; в противном случае — значение Variant \_ false.

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Это событие не возвращает значение.

## <a name="remarks"></a>Комментарии

> [!Note]  
> Параметры *x* и *y* задаются в пикселях, а не в HIMETRIC единицах, связанных с системой координат рукописного пространства. Это связано с тем, что это событие заменяет связанное событие мыши приложения, которое не поддерживает перо, и этот тип приложения относится только к пикселям.

 

Этот метод события определен в интерфейсе **\_ иинкпиктуривентс** . Интерфейс **\_ иинкпиктуривентс** реализует интерфейс [**IDISPATCH**](/windows/win32/api/oaidl/nn-oaidl-idispatch) с идентификатором DISPID \_ ипемаусевхил.

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
</dt> </dl>

 

