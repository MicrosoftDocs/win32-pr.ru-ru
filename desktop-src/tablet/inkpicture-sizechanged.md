---
description: Происходит после изменения размера элемента управления InkPicture, в частности после того, как изменяется значение свойства Width или Height.
ms.assetid: a5fc6c82-f9c8-4104-8abe-082c47c56be9
title: Событие InkPicture. SizeChanged (Мсинкаут. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a4473bf580e1683c8d410cd1f2cdbaf271302485f51556b68c4fae7a5d6b99ef
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119032042"
---
# <a name="inkpicturesizechanged-event"></a>Событие InkPicture. SizeChanged

Происходит после изменения размера элемента управления [InkPicture](inkpicture-control-reference.md) , в частности после того, как изменяется значение свойства [**Width**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkdrawingattributes-get_width) или [**Height**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkdrawingattributes-get_height) .

## <a name="syntax"></a>Синтаксис


```C++
void SizeChanged(
  [in] long Left,
  [in] long Top,
  [in] long Right,
  [in] long Bottom
);
```



## <a name="parameters"></a>Параметры

<dl> <dt>

По *левому краю* \[ окне\]
</dt> <dd>

Координата по оси x левой стороны элемента управления [InkPicture](inkpicture-control-reference.md) .

</dd> <dt>

В *Начало* \[ окне\]
</dt> <dd>

Координата по оси y верхнего края элемента управления [InkPicture](inkpicture-control-reference.md) .

</dd> <dt>

По *правому краю* \[ окне\]
</dt> <dd>

Координата по оси x правой стороны элемента управления [InkPicture](inkpicture-control-reference.md) .

</dd> <dt>

По *нижнему краю* \[ окне\]
</dt> <dd>

Координата по оси y нижней части элемента управления [InkPicture](inkpicture-control-reference.md) .

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Это событие не возвращает значение.

## <a name="remarks"></a>Remarks

Этот метод события определен в интерфейсе **\_ иинкпиктуривентс** . Интерфейс **\_ иинкпиктуривентс** реализует интерфейс [**IDISPATCH**](/windows/win32/api/oaidl/nn-oaidl-idispatch) с идентификатором DISPID \_ ипесизечанжед.

## <a name="requirements"></a>Requirements (Требования)



| Требование | Значение |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Windows XP Tablet PC Edition \[ только классические приложения\]<br/>                                                       |
| Минимальная версия сервера<br/> | Ни одна версия не поддерживается<br/>                                                                                           |
| Заголовок<br/>                   | <dl> <dt>Мсинкаут. h (также требуется Мсинкаут \_ i. c)</dt> </dl> |
| Библиотека<br/>                  | <dl> <dt>InkObj.dll</dt> </dl>                               |



## <a name="see-also"></a>См. также

<dl> <dt>

[InkPicture](inkpicture-control-reference.md)
</dt> </dl>

 

