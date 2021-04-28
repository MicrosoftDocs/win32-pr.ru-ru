---
description: Событие InkPicture. Таблетаддед — происходит при добавлении Иинктаблет в систему.
ms.assetid: 5df10efd-7055-43fa-881f-67eb5fd6adcf
title: Событие InkPicture. Таблетаддед (Мсинкаут. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 81c5121b668f27034a04230311ee88ebb7564802
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2021
ms.locfileid: "108113662"
---
# <a name="inkpicturetabletadded-event"></a>Событие InkPicture. Таблетаддед

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

## <a name="remarks"></a>Remarks

Этот метод события определен в интерфейсах диспетчеризации (DISP) **\_ иинкколлекторевентс**, **\_ иинковерлайевентс** и **\_ иинкпиктуривентс** с идентификатором DISPID \_ ицетаблетаддед.

## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Только классические приложения Windows XP Tablet PC Edition \[\]<br/>                                                       |
| Минимальная версия сервера<br/> | Ни одна версия не поддерживается<br/>                                                                                           |
| Header<br/>                   | <dl> <dt>Мсинкаут. h (также требуется Мсинкаут \_ i. c)</dt> </dl> |
| Библиотека<br/>                  | <dl> <dt>InkObj.dll</dt> </dl>                               |



## <a name="see-also"></a>См. также

<dl> <dt>

[InkPicture](inkpicture-control-reference.md)
</dt> <dt>

[**Интерфейс Иинктаблет**](/windows/desktop/api/msinkaut/nn-msinkaut-iinktablet)
</dt> </dl>

 

 




