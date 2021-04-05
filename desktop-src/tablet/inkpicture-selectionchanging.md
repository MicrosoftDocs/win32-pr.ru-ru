---
description: Происходит при изменении выделения рукописного ввода внутри элемента управления InkPicture, например посредством изменений пользовательского интерфейса, процедур копирования и вставки или свойства Selection.
ms.assetid: a8ae30ff-fb0d-44cc-a5d3-295117addafd
title: Событие InkPicture. Селектиончангинг (Мсинкаут. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 37b8a35d57aeb9367bb9d30647cb074a7e0e6fbd
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "103912907"
---
# <a name="inkpictureselectionchanging-event"></a>Событие InkPicture. Селектиончангинг

Происходит при изменении выделения рукописного ввода внутри элемента управления [InkPicture](inkpicture-control-reference.md) , например посредством изменений пользовательского интерфейса, процедур копирования и вставки или свойства [**Selection**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkpicture-get_selection) .

## <a name="syntax"></a>Синтаксис


```C++
void SelectionChanging(
  [in] IInkStrokes *NewSelection
);
```



## <a name="parameters"></a>Параметры

<dl> <dt>

*Невселектион* \[ окне\]
</dt> <dd>

Новая коллекция [инкстрокес](/previous-versions/windows/desktop/legacy/ms703293(v=vs.85)) , которая выбрана.

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Это событие не возвращает значение.

## <a name="remarks"></a>Комментарии

Этот метод события определен в интерфейсах диспетчеризации **\_ иинковерлайевентс** и **\_ ИИНКПИКТУРИВЕНТС** (DISP) с идентификатором DISPID \_ иоеселектиончангинг.

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
</dt> </dl>

 

