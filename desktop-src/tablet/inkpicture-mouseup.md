---
description: Происходит при отпускании кнопки мыши при перемещении указателя мыши над элементом управления InkPicture.
ms.assetid: 5e49acc8-1ce1-45ff-b87c-04bdc653156a
title: Событие InkPicture. MouseUp (Мсинкаут. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: bf652e1ad4110afb4819e5326a5a19a894a310a2
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "105712215"
---
# <a name="inkpicturemouseup-event"></a>Событие InkPicture. MouseUp

Происходит при отпускании кнопки мыши при перемещении указателя мыши над элементом управления [InkPicture](inkpicture-control-reference.md) .

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

Нажатая кнопка.

</dd> <dt>

*SHIFT* \[ окне\]
</dt> <dd>

Состояние клавиши SHIFT.

</dd> <dt>

*ПКС* \[ окне\]
</dt> <dd>

Координата x (в пикселях) объекта [**иинккурсор**](/windows/desktop/api/msinkaut/nn-msinkaut-iinkcursor) .

</dd> <dt>

*Копировать* \[ в окне\]
</dt> <dd>

Координата по оси y (в пикселях) объекта [**иинккурсор**](/windows/desktop/api/msinkaut/nn-msinkaut-iinkcursor) .

</dd> <dt>

*Отмена* \[ в, out\]
</dt> <dd>

**Вариант \_ Значение TRUE** , чтобы отменить событие MouseUp для родительского элемента управления; в противном случае — **\_ значение false**.

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Это событие не возвращает значение.

## <a name="remarks"></a>Комментарии

> [!Note]  
> Параметры *px* и *корректировки* находятся в пикселях, а не в HIMETRIC единицах, связанных с системой координат рукописного пространства. Это связано с тем, что это событие заменяет связанное событие мыши приложения, которое не поддерживает перо, и этот тип приложения относится только к пикселям.

 

> [!Caution]  
> Некоторые элементы управления используют определенную связь между событиями [**MouseDown**](inkpicture-mousedown.md), [**MouseMove**](inkpicture-mousemove.md)и **MouseUp** . Отмена некоторых из этих событий может привести к непредвиденным результатам.

 

Этот метод события определен в интерфейсе **\_ иинкпиктуривентс** . Интерфейс **\_ иинкпиктуривентс** реализует интерфейс [**IDISPATCH**](/windows/win32/api/oaidl/nn-oaidl-idispatch) с идентификатором DISPID \_ ипемауседовн.

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

 

