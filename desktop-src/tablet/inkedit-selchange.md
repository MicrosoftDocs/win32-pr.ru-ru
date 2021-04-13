---
description: Происходит при изменении текущего выделения текста в элементе управления InkEdit или при перемещении точки вставки.
ms.assetid: 14ddffe7-bdfe-4a35-82c7-b3401b5b720c
title: Событие InkEdit. Селчанже (with. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 66b51ef4edbf7d7fb02be17dc416c0a777a9519a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "105647449"
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

## <a name="remarks"></a>Комментарии

Событие **селчанже** можно использовать для проверки различных свойств, которые предоставляют сведения о текущем выделении (например, [**селболд**](/windows/desktop/api/inked/nf-inked-iinkedit-get_selbold)), что позволяет обновлять кнопки на панели инструментов, например.

## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Только классические приложения Windows XP Tablet PC Edition \[\]<br/>                                                 |
| Минимальная версия сервера<br/> | Ни одна версия не поддерживается<br/>                                                                                     |
| Header<br/>                   | <dl> <dt>«С». h (также требует \_ ввода i. c)</dt> </dl> |
| Библиотека<br/>                  | <dl> <dt>InkEd.dll</dt> </dl>                          |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[InkEdit](inkedit-control-reference.md)
</dt> </dl>

 

 




