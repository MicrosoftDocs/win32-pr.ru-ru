---
description: Происходит после изменения размера элемента управления InkPicture, в частности после того, как изменяется значение свойства Width или Height.
ms.assetid: a5fc6c82-f9c8-4104-8abe-082c47c56be9
title: Событие InkPicture. SizeChanged (Мсинкаут. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c5675d2a581d9e8973b88fa9fb6e213f54c0e283
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "103999428"
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

## <a name="remarks"></a>Комментарии

Этот метод события определен в интерфейсе **\_ иинкпиктуривентс** . Интерфейс **\_ иинкпиктуривентс** реализует интерфейс [**IDISPATCH**](/windows/win32/api/oaidl/nn-oaidl-idispatch) с идентификатором DISPID \_ ипесизечанжед.

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

 

