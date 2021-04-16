---
description: Происходит при завершении перерисовки элемента управления InkPicture.
ms.assetid: a8194cff-ed94-402e-8564-08d370f958b4
title: Событие InkPicture. окрашено (Мсинкаут. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 60188ef87d88ba7412a07300e708718bedc947fe
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "105712210"
---
# <a name="inkpicturepainted-event"></a>Событие InkPicture. окрашено

Происходит при завершении перерисовки элемента управления [InkPicture](inkpicture-control-reference.md) .

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

Этот метод события определен в DISP-интерфейсах **\_ иинковерлайевентс** и **\_ иинкпиктуривентс** с идентификатором DISPID \_ иоепаинтед.

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

 

 




