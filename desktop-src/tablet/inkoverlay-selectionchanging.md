---
description: Происходит при изменении выделения рукописных данных в элементе управления, например при выполнении изменений в пользовательском интерфейсе, процедурах вырезания и вставки или при выборе свойства Selection.
ms.assetid: dffdb183-d363-40d3-81a2-d496433f7075
title: Событие InkOverlay. Селектиончангинг (Мсинкаут. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e830a9ea97f6722dd8ab9bdb782e4ae4ac5f44fb
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "105693466"
---
# <a name="inkoverlayselectionchanging-event"></a>Событие InkOverlay. Селектиончангинг

Происходит при изменении выделения рукописных данных в элементе управления, например при выполнении изменений в пользовательском интерфейсе, процедурах вырезания и вставки или при [**выборе свойства Selection**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkoverlay-get_selection) .

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

Этот метод события определен в \_ \_ интерфейсах диспетчеризации иинковерлайевентс и иинкпиктуривентс (DISP) с идентификатором DISPID \_ иоеселектиончангинг.

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

[**Свойство Selection**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkoverlay-get_selection)
</dt> </dl>

 

