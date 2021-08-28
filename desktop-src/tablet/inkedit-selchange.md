---
description: Происходит при изменении текущего выделения текста в элементе управления InkEdit или при перемещении точки вставки.
ms.assetid: 14ddffe7-bdfe-4a35-82c7-b3401b5b720c
title: Событие InkEdit. Селчанже (with. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9677aafa254de3d834e9b947ad1b858b893d6a42e53336dd11ad5c54157c13dc
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119712654"
---
# <a name="inkeditselchange-event"></a>Событие InkEdit. Селчанже

Происходит при изменении текущего выделения текста в элементе управления [InkEdit](inkedit-control-reference.md) или при перемещении точки вставки.

## <a name="syntax"></a>Синтаксис


```C++
void SelChange();
```



## <a name="parameters"></a>Параметры

У этого события нет параметров.

## <a name="return-value"></a>Возвращаемое значение

Это событие не возвращает значение.

## <a name="remarks"></a>Remarks

Событие **селчанже** можно использовать для проверки различных свойств, которые предоставляют сведения о текущем выделении (например, [**селболд**](/windows/desktop/api/inked/nf-inked-iinkedit-get_selbold)), что позволяет обновлять кнопки на панели инструментов, например.

## <a name="requirements"></a>Requirements (Требования)



| Требование | Значение |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Windows XP Tablet PC Edition \[ только классические приложения\]<br/>                                                 |
| Минимальная версия сервера<br/> | Ни одна версия не поддерживается<br/>                                                                                     |
| Заголовок<br/>                   | <dl> <dt>«С». h (также требует \_ ввода i. c)</dt> </dl> |
| Библиотека<br/>                  | <dl> <dt>InkEd.dll</dt> </dl>                          |



## <a name="see-also"></a>См. также

<dl> <dt>

[InkEdit](inkedit-control-reference.md)
</dt> </dl>

 

 




