---
description: Происходит при изменении выделения рукописных данных в элементе управления InkPicture, например при внесении изменений в пользовательский интерфейс, процедурах вырезания и вставки или при выборе свойства Selection.
ms.assetid: e300ec91-e8f3-473f-b526-efeafafaa32a
title: Событие InkPicture. SelectionChanged (Мсинкаут. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1a1fce27d9aa0dd043c5e474d790c1bd9737a9c10bffbed3eff6a287be67030f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119939004"
---
# <a name="inkpictureselectionchanged-event"></a>Событие InkPicture. SelectionChanged

Происходит при изменении выделения рукописных данных в элементе управления [InkPicture](inkpicture-control-reference.md) , например при внесении изменений в пользовательский интерфейс, процедурах вырезания и вставки или при [**выборе свойства Selection**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkpicture-get_selection) .

## <a name="syntax"></a>Синтаксис


```C++
void SelectionChanged();
```



## <a name="parameters"></a>Параметры

У этого события нет параметров.

## <a name="return-value"></a>Возвращаемое значение

Это событие не возвращает значение.

## <a name="remarks"></a>Remarks

Дополнительные сведения об этом событии см. в описании события [**SelectionChanged**](inkoverlay-selectionchanged.md) объекта [**InkOverlay**](inkoverlay-class.md) , имеющего те же функциональные возможности.

## <a name="requirements"></a>Requirements (Требования)



| Требование | Значение |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Windows XP Tablet PC Edition \[ только классические приложения\]<br/>                                                       |
| Минимальная версия сервера<br/> | Ни одна версия не поддерживается<br/>                                                                                           |
| Заголовок<br/>                   | <dl> <dt>Мсинкаут. h (также требуется Мсинкаут \_ i. c)</dt> </dl> |
| Библиотека<br/>                  | <dl> <dt>InkObj.dll</dt> </dl>                               |



## <a name="see-also"></a>См. также

<dl> <dt>

[InkPicture](inkpicture-control-reference.md)
</dt> <dt>

[**\[Элемент управления InkPicture свойства Selection\]**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkpicture-get_selection)
</dt> </dl>

 

 




