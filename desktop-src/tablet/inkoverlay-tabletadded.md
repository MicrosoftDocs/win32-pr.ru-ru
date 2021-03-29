---
description: Происходит при добавлении Иинктаблет в систему.
ms.assetid: 2076a520-bd37-43b5-b57f-030828b096cb
title: Событие InkOverlay. Таблетаддед (Мсинкаут. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 79c2faadcbf87e0772afb8f417c97a4be546e08b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "105647665"
---
# <a name="inkoverlaytabletadded-event"></a>Событие InkOverlay. Таблетаддед

Происходит при добавлении [**иинктаблет**](/windows/desktop/api/msinkaut/nn-msinkaut-iinktablet) в систему.

## <a name="syntax"></a>Синтаксис


```C++
void TabletAdded(
  [in] IInkTablet *Tablet
);
```



## <a name="parameters"></a>Параметры

<dl> <dt>

*Планшетный ПК* \[ окне\]
</dt> <dd>

Объект [**иинктаблет**](/windows/desktop/api/msinkaut/nn-msinkaut-iinktablet) , который был добавлен в систему.

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Это событие не возвращает значение.

## <a name="remarks"></a>Комментарии

Этот метод события определен в \_ \_ \_ интерфейсах диспетчеризации (DISP) иинкколлекторевентс, иинковерлайевентс и иинкпиктуривентс с идентификатором DISPID \_ ицетаблетаддед.

## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Только классические приложения Windows XP Tablet PC Edition \[\]<br/>                                                       |
| Минимальная версия сервера<br/> | Ни одна версия не поддерживается<br/>                                                                                           |
| Header<br/>                   | <dl> <dt>Мсинкаут. h (также требуется Мсинкаут \_ i. c)</dt> </dl> |
| Библиотека<br/>                  | <dl> <dt>InkObj.dll</dt> </dl>                               |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[**Класс InkOverlay**](inkoverlay-class.md)
</dt> <dt>

[**Интерфейс Иинктаблет**](/windows/desktop/api/msinkaut/nn-msinkaut-iinktablet)
</dt> </dl>

 

 




