---
description: Происходит при освобождении ключа, когда элемент управления InkPicture имеет фокус.
ms.assetid: e22633b5-40fe-4b94-a660-684c4f5c96f3
title: Событие InkPicture. KeyUp (Мсинкаут. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7c2390b6cbb7b91ab8e447df912e591ea37248e9
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "105712363"
---
# <a name="inkpicturekeyup-event"></a>Событие InkPicture. KeyUp

Происходит при освобождении ключа, когда элемент управления [InkPicture](inkpicture-control-reference.md) имеет фокус.

## <a name="syntax"></a>Синтаксис


```C++
void KeyUp(
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

Этот метод события определен в интерфейсе **\_ иинкпиктуривентс** . Интерфейс **\_ иинкпиктуривентс** реализует интерфейс [**IDISPATCH**](/windows/win32/api/oaidl/nn-oaidl-idispatch) с идентификатором DISPID \_ ипекэйуп.

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

 

