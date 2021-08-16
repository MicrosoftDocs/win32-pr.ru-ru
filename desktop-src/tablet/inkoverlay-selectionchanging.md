---
description: Происходит при изменении выделения рукописных данных в элементе управления, например при выполнении изменений в пользовательском интерфейсе, процедурах вырезания и вставки или при выборе свойства Selection.
ms.assetid: dffdb183-d363-40d3-81a2-d496433f7075
title: Событие InkOverlay. Селектиончангинг (Мсинкаут. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: fb9b7fa52c4897c7e1152deff7636259e07e2768929223327243c2da0b59e362
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "118218957"
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

## <a name="remarks"></a>Remarks

Этот метод события определен в \_ \_ интерфейсах диспетчеризации иинковерлайевентс и иинкпиктуривентс (DISP) с идентификатором DISPID \_ иоеселектиончангинг.

## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Windows XP Tablet PC Edition \[ только классические приложения\]<br/>                                                       |
| Минимальная версия сервера<br/> | Ни одна версия не поддерживается<br/>                                                                                           |
| Header<br/>                   | <dl> <dt>Мсинкаут. h (также требуется Мсинкаут \_ i. c)</dt> </dl> |
| Библиотека<br/>                  | <dl> <dt>InkObj.dll</dt> </dl>                               |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[**Класс InkOverlay**](inkoverlay-class.md)
</dt> <dt>

[**Свойство Selection**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkoverlay-get_selection)
</dt> </dl>

 

