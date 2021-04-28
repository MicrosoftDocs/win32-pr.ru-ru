---
description: Событие InkPicture. Селектионресизед — происходит при изменении размера текущего выделения, например посредством изменений пользовательского интерфейса, процедур копирования и вставки или свойства Selection.
ms.assetid: 4e7f461f-2909-40ab-98d8-b763d489eb62
title: Событие InkPicture. Селектионресизед (Мсинкаут. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1dcad4b84cd21ee9b4d385f24033c56913765810
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2021
ms.locfileid: "108086472"
---
# <a name="inkpictureselectionresized-event"></a>Событие InkPicture. Селектионресизед

Происходит при изменении размера текущего выделения, например с помощью изменений пользовательского интерфейса, процедур копирования и вставки или свойства [**Selection**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkpicture-get_selection) .

## <a name="syntax"></a>Синтаксис


```C++
void SelectionResized(
  [in] IInkRectangle *OldSelectionRect
);
```



## <a name="parameters"></a>Параметры

<dl> <dt>

*Олдселектионрект* \[ окне\]
</dt> <dd>

Ограничивающий прямоугольник выбранной коллекции [инкстрокес](/previous-versions/windows/desktop/legacy/ms703293(v=vs.85)) , который существовал до запуска события **селектионресизед** .

> [!Note]  
> Этот прямоугольник задается в координатах области рукописного ввода, что позволяет выполнять сценарии отмены.

 

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Это событие не возвращает значение.

## <a name="remarks"></a>Remarks

Этот метод события определен в интерфейсах диспетчеризации **\_ иинковерлайевентс** и **\_ ИИНКПИКТУРИВЕНТС** (DISP) с идентификатором DISPID \_ иоеселектионресизед.

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

[**\[Элемент управления InkPicture свойства Selection\]**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkpicture-get_selection)
</dt> <dt>

[**Класс Инкректангле**](inkrectangle-class.md)
</dt> </dl>

 

