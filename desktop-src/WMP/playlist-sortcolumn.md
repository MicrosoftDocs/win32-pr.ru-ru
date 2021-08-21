---
title: Список воспроизведения. sortColumn
description: Метод sortColumn сортирует данные в указанном столбце.
ms.assetid: 1563fee8-044a-4cb4-a9c2-11d4533536da
keywords:
- проигрыватель Windows Media списка воспроизведения. sortColumn
topic_type:
- apiref
api_name:
- PLAYLIST.sortColumn
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 34dfce7306ceb39d64665538a21dbaef965ea799141a2756c2fea5bbe23ea9cd
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "118335665"
---
# <a name="playlistsortcolumn"></a>Список воспроизведения. sortColumn

Метод **sortColumn** сортирует данные в указанном столбце.

``` syntax
        elementID.sortColumn(column)
```

## <a name="parameters"></a>Параметры

<dl> <dt>

<span id="column"></span><span id="COLUMN"></span>*рубрик*
</dt> <dd>

**Число** (**Long**), указывающее индекс столбца для сортировки.

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Этот метод не возвращает значение.

## <a name="remarks"></a>Remarks

Этот метод сортирует указанный столбец так же, как кнопки заголовка столбца в элементе **списка воспроизведения** . Если столбец еще не отсортирован, он сортируется в алфавитно-цифровом порядке. Если сортировка выполнена, ее порядок изменяется на обратный.

Чтобы этот метод работал, атрибуту **алловколумнсортинг** должно быть присвоено значение true.

## <a name="requirements"></a>Requirements (Требования)



| Требование | Значение |
|--------------------|------------------------------------------------------|
| Версия<br/> | проигрыватель Windows Media версии 7,0 или более поздней<br/> |



## <a name="see-also"></a>См. также

<dl> <dt>

[**Элемент списка воспроизведения**](playlist-element.md)
</dt> <dt>

[**Список воспроизведения. Алловколумнсортинг**](playlist-allowcolumnsorting.md)
</dt> </dl>

 

 





