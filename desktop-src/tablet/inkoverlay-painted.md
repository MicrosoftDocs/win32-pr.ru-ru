---
description: Происходит при завершении перерисовки объекта InkOverlay или элемента управления InkPicture.
ms.assetid: de3c69de-4a33-46e4-96e5-462805681bda
title: Событие InkOverlay. окрашено (Мсинкаут. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3de0628679aa034b16a3562aa08cdbd1928653ad
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "104498075"
---
# <a name="inkoverlaypainted-event"></a>Событие InkOverlay. окрашено

Происходит при завершении перерисовки объекта [**InkOverlay**](inkoverlay-class.md) или элемента управления [InkPicture](inkpicture-control-reference.md) .

## <a name="syntax"></a>Синтаксис


```C++
void Painted(
  [in] long         hDC,
  [in] InkRectangle *Rect
);
```



## <a name="parameters"></a>Параметры

<dl> <dt>

*HDC* \[ окне\]
</dt> <dd>

Контекст устройства, в котором произошло событие.

</dd> <dt>

*Rect* \[ окне\]
</dt> <dd>

Перерисовка [**инкректангле**](inkrectangle-class.md) .

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Это событие не возвращает значение.

## <a name="remarks"></a>Комментарии

Этот метод события определен в \_ \_ интерфейсах диспетчеризации иинковерлайевентс и иинкпиктуривентс (DISP) с идентификатором DISPID \_ иоепаинтед.

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
</dt> </dl>

 

 




