---
description: Происходит при нажатии клавиши и в расположении вниз, пока элемент управления InkPicture находится в фокусе.
ms.assetid: d83823ea-d863-4eb7-8f6b-fa7a3396e64b
title: Событие InkPicture. KeyDown (Мсинкаут. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4b5d6bd3555aeec98ac28555c1674dfef32ecc53
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "104081590"
---
# <a name="inkpicturekeydown-event"></a>Событие InkPicture. KeyDown

Происходит при нажатии клавиши и в расположении вниз, пока элемент управления [InkPicture](inkpicture-control-reference.md) находится в фокусе.

## <a name="syntax"></a>Синтаксис


```C++
void KeyDown(
  [in, out] short *KeyCode,
  [in, out] short *Shift
);
```



## <a name="parameters"></a>Параметры

<dl> <dt>

*KeyCode* \[ в, out\]
</dt> <dd>

Значение ASCII для нажатого клавиши.

</dd> <dt>

*SHIFT* \[ в, out\]
</dt> <dd>

Состояние клавиши SHIFT.

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Это событие не возвращает значение.

## <a name="remarks"></a>Комментарии

Этот метод события определен в интерфейсе **\_ иинкпиктуривентс** . Интерфейс **\_ иинкпиктуривентс** реализует интерфейс [**IDISPATCH**](/windows/win32/api/oaidl/nn-oaidl-idispatch) с идентификатором DISPID \_ ипекэйдовн.

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

 

