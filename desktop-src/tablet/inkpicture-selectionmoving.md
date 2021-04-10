---
description: Происходит, когда расположение текущего выделения собирается измениться, например, посредством изменений пользовательского интерфейса, процедур копирования и вставки или свойства Selection.
ms.assetid: 310003a1-f282-4efa-9a75-c575a9193a77
title: Событие InkPicture. Селектионмовинг (Мсинкаут. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ad2dbc0064e22f21faf80d67f51ca1eeb58b6433
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "104081453"
---
# <a name="inkpictureselectionmoving-event"></a>Событие InkPicture. Селектионмовинг

Происходит, когда расположение текущего выделения собирается измениться, например, посредством изменений пользовательского интерфейса, процедур копирования и вставки или свойства [**Selection**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkpicture-get_selection) .

## <a name="syntax"></a>Синтаксис


```C++
void SelectionMoving(
  [in] IInkRectangle *CurSelectionRect
);
```



## <a name="parameters"></a>Параметры

<dl> <dt>

*Курселектионрект* \[ окне\]
</dt> <dd>

Прямоугольник, в который перемещается выделение после события **селектионмовинг** .

> [!Note]  
> Этот прямоугольник задается в координатах окна клиента, что позволяет выполнять такие сценарии, как сохранение пропорций при изменении размера.

 

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Это событие не возвращает значение.

## <a name="remarks"></a>Комментарии

Этот метод события определен в интерфейсах диспетчеризации **\_ иинковерлайевентс** и **\_ ИИНКПИКТУРИВЕНТС** (DISP) с идентификатором DISPID \_ иоеселектионмовинг.

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
</dt> <dt>

[**\[Элемент управления InkPicture свойства Selection\]**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkpicture-get_selection)
</dt> <dt>

[**Класс Инкректангле**](inkrectangle-class.md)
</dt> </dl>

 

 




