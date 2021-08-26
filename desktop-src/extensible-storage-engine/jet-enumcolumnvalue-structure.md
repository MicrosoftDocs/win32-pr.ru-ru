---
description: 'Дополнительные сведения: структура JET_ENUMCOLUMNVALUE'
title: Структура JET_ENUMCOLUMNVALUE
TOCTitle: JET_ENUMCOLUMNVALUE Structure
ms:assetid: a9882d7b-0c53-4a5d-bc98-0979e6e68c88
ms:mtpsurl: https://msdn.microsoft.com/library/Gg294052(v=EXCHG.10)
ms:contentKeyID: 32765652
ms.date: 04/11/2016
ms.topic: reference
api_name: ''
topic_type:
- apiref
- kbArticle
api_type:
- COM
api_location: ''
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 86905d49bb798d37bad48087c48e77349ec10f57
ms.sourcegitcommit: 9b5faa61c38b2d0c432b7f2dbee8c127b0e28a7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/19/2021
ms.locfileid: "122482290"
---
# <a name="jet_enumcolumnvalue-structure"></a>Структура JET_ENUMCOLUMNVALUE


_**Применимо к:** Windows | Windows Сервером_

## <a name="jet_enumcolumnvalue-structure"></a>Структура JET_ENUMCOLUMNVALUE

Структура **JET_ENUMCOLUMNVALUE** перечисляет значения столбцов записи с помощью функции [жетенумератеколумнс](./jetenumeratecolumns-function.md) . [Жетенумератеколумнс](./jetenumeratecolumns-function.md) возвращает массив структур **JET_ENUMCOLUMNVALUE** . Массив возвращается в памяти, выделенной с помощью обратного вызова, [перераспределения](/cpp/c-runtime-library/reference/realloc?view=vs-2019) которого было предоставлено этой функции.

```cpp
    typedef struct {
      unsigned long itagSequence;
      JET_ERR err;
      unsigned long cbData;
      void* pvData;
    } JET_ENUMCOLUMNVALUE;
```

### <a name="members"></a>Элементы

**итагсекуенце**

Значение столбца (по основанному на единицу индексу), которое было перечислено.

**Err**

Код состояния столбца, полученный в результате перечисления значения столбца.


| <p>Значение</p> | <p>Значение</p> | 
|--------------|----------------|
| <p>JET_wrnColumnNull</p> | <p>Запрошенное значение столбца равно NULL.</p> | 
| <p>JET_wrnColumnSkipped</p> | <p><em>Итагсекуенце</em> , указанный в элементе массива <em>ргтагсекуенце</em> в структуре <a href="gg294138(v=exchg.10).md">JET_ENUMCOLUMN</a> , соответствующей этой <strong>JET_ENUMCOLUMNVALUE</strong> структуре, была нулевой.</p> | 
| <p>JET_wrnColumnTruncated</p> | <p>Значение запрошенного столбца было усечено до указанного размера перед возвратом.</p><p>Это усечение происходит только для длинных текстовых и длинных двоичных столбцов, содержащих большие объемы данных.</p> | 



**cbData**

Значение столбца, перечисленное для столбца.

Выходной буфер возвращается в память, которая была выделена с помощью обратного вызова, [перераспределения](/cpp/c-runtime-library/reference/realloc?view=vs-2019) которого было предоставлено в [жетенумератеколумнс](./jetenumeratecolumns-function.md).

**пвдата**

Значение столбца, перечисленное для столбца.

Выходной буфер возвращается в память, которая была выделена с помощью обратного вызова, [перераспределения](/cpp/c-runtime-library/reference/realloc?view=vs-2019) которого было предоставлено в [жетенумератеколумнс](./jetenumeratecolumns-function.md).

### <a name="requirements"></a>Требования


| | | <p><strong>Клиент</strong></p> | <p>требуется Windows Vista, Windows XP или Windows 2000 Professional.</p> | | <p><strong>Сервер</strong></p> | <p>требуется Windows server 2008, Windows server 2003 или сервер Windows 2000.</p> | | <p><strong>Header</strong></p> | <p>Объявлено в ESENT. h.</p> | 



### <a name="see-also"></a>См. также:

[JET_ENUMCOLUMN](./jet-enumcolumn-structure.md)  
[JET_ENUMCOLUMNVALUE]()  
[JET_ERR](./jet-err.md)  
[жетенумератеколумнс](./jetenumeratecolumns-function.md)  
[realloc](/cpp/c-runtime-library/reference/realloc?view=vs-2019)
