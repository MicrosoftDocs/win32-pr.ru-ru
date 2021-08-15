---
description: Событие InkPicture. Селектионресизинг — происходит, когда размер текущего выделения собирается измениться, например посредством изменений пользовательского интерфейса, процедур копирования и вставки или свойства Selection.
ms.assetid: da708712-2773-45f5-9d9b-49fabe7fdb5a
title: Событие InkPicture. Селектионресизинг (Мсинкаут. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: caeae852802599a401c1cdff97436672e0cbfe252f8f1e96d6f4c98367c828ef
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "118966963"
---
# <a name="inkpictureselectionresizing-event"></a>Событие InkPicture. Селектионресизинг

Происходит, когда размер текущего выделения собирается измениться, например посредством изменений пользовательского интерфейса, процедур копирования и вставки или свойства [**Selection**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkpicture-get_selection) .

## <a name="syntax"></a>Синтаксис


```C++
void SelectionResizing(
  [in] IInkRectangle *CurSelectionRect
);
```



## <a name="parameters"></a>Параметры

<dl> <dt>

*Курселектионрект* \[ окне\]
</dt> <dd>

Ограничивающий прямоугольник выделения после события **селектионресизинг** .

> [!Note]  
> Этот прямоугольник задается в координатах окна клиента, что позволяет выполнять такие сценарии, как сохранение пропорций при изменении размера.

 

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Это событие не возвращает значение.

## <a name="remarks"></a>Remarks

Этот метод события определен в интерфейсах диспетчеризации **\_ иинковерлайевентс** и **\_ ИИНКПИКТУРИВЕНТС** (DISP) с идентификатором DISPID \_ иоеселектионресизинг.

## <a name="requirements"></a>Requirements (Требования)



| Требование | Значение |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Windows XP Tablet PC Edition \[ только классические приложения\]<br/>                                                       |
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

 

 




