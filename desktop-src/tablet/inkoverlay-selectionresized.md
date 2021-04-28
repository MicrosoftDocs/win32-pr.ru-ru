---
description: Событие InkOverlay. Селектионресизед — происходит при изменении размера текущего выделения, например посредством изменений пользовательского интерфейса, процедур копирования и вставки или свойства Selection.
ms.assetid: 606d4bdf-b02e-459f-a4cf-050daac6c309
title: Событие InkOverlay. Селектионресизед (Мсинкаут. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2f3dd3cf1bdda004733dde99bb66150710044310
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2021
ms.locfileid: "108116882"
---
# <a name="inkoverlayselectionresized-event"></a>Событие InkOverlay. Селектионресизед

Происходит при изменении размера текущего выделения, например с помощью изменений пользовательского интерфейса, процедур копирования и вставки или свойства [**Selection**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkoverlay-get_selection) .

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

Этот метод события определен в \_ \_ интерфейсах диспетчеризации иинковерлайевентс и иинкпиктуривентс (DISP) с идентификатором DISPID \_ иоеселектионресизед.

## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Только классические приложения Windows XP Tablet PC Edition \[\]<br/>                                                       |
| Минимальная версия сервера<br/> | Ни одна версия не поддерживается<br/>                                                                                           |
| Header<br/>                   | <dl> <dt>Мсинкаут. h (также требуется Мсинкаут \_ i. c)</dt> </dl> |
| Библиотека<br/>                  | <dl> <dt>InkObj.dll</dt> </dl>                               |



## <a name="see-also"></a>См. также

<dl> <dt>

[**Класс InkOverlay**](inkoverlay-class.md)
</dt> <dt>

[**Свойство Selection**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkoverlay-get_selection)
</dt> <dt>

[**Класс Инкректангле**](inkrectangle-class.md)
</dt> </dl>

 

