---
description: Происходит при нажатии клавиши, когда элемент управления InkPicture имеет фокус.
ms.assetid: adb61eff-a92c-40b0-940c-02e14cd34e5f
title: Событие InkPicture. KeyPress (Мсинкаут. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7545b0de722ec9b48c66aa5d2236bf81eb576d87916c15e618508e537981a2cb
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119939014"
---
# <a name="inkpicturekeypress-event"></a>Событие InkPicture. KeyPress

Происходит при нажатии клавиши, когда элемент управления [InkPicture](inkpicture-control-reference.md) имеет фокус.

## <a name="syntax"></a>Синтаксис


```C++
void KeyPress(
  [in, out] short *KeyAscii
);
```



## <a name="parameters"></a>Параметры

<dl> <dt>

*КэйасЦии* \[ в, out\]
</dt> <dd>

Значение ASCII для нажатого клавиши.

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Это событие не возвращает значение.

## <a name="remarks"></a>Remarks

Этот метод события определен в интерфейсе **\_ иинкпиктуривентс** . Интерфейс **\_ иинкпиктуривентс** реализует интерфейс [**IDISPATCH**](/windows/win32/api/oaidl/nn-oaidl-idispatch) с идентификатором DISPID \_ ипекэйпресс.

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

 

