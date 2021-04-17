---
description: Происходит при изменении выделения рукописных данных в элементе управления, например при внесении изменений в пользовательский интерфейс, процедурах вырезания и вставки или при выборе свойства Selection.
ms.assetid: 6b4cd9fe-b09f-4a70-9aa5-92ef9409ff1b
title: Событие InkOverlay. SelectionChanged (Мсинкаут. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 997e0c8e9620b0a269ff8cd97ff04aa3abfb1df0
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "105703057"
---
# <a name="inkoverlayselectionchanged-event"></a>Событие InkOverlay. SelectionChanged

Происходит при изменении выделения рукописных данных в элементе управления, например при внесении изменений в пользовательский интерфейс, процедурах вырезания и вставки или при [**выборе свойства Selection**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkoverlay-get_selection) .

## <a name="syntax"></a>Синтаксис


```C++
void SelectionChanged();
```



## <a name="parameters"></a>Параметры

У этого события нет параметров.

## <a name="return-value"></a>Возвращаемое значение

Это событие не возвращает значение.

## <a name="remarks"></a>Комментарии

Данные событий отсутствуют.

Этот метод события определен в \_ \_ интерфейсах диспетчеризации иинковерлайевентс и иинкпиктуривентс (DISP) с идентификатором DISPID \_ иоеселектиончанжед.

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

 

 




