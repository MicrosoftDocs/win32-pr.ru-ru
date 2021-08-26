---
description: 'Дополнительные сведения: структура JET_UNICODEINDEX'
title: Структура JET_UNICODEINDEX
TOCTitle: JET_UNICODEINDEX Structure
ms:assetid: d0b8ef74-850e-4e21-9f71-b56ec472aa0f
ms:mtpsurl: https://msdn.microsoft.com/library/Gg294097(v=EXCHG.10)
ms:contentKeyID: 32765712
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
ms.openlocfilehash: 544438541affba1121850d5ad5a7a60d54d398bd
ms.sourcegitcommit: 9b5faa61c38b2d0c432b7f2dbee8c127b0e28a7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/19/2021
ms.locfileid: "122471390"
---
# <a name="jet_unicodeindex-structure"></a>Структура JET_UNICODEINDEX


_**Применимо к:** Windows | Windows Сервером_

## <a name="jet_unicodeindex-structure"></a>Структура JET_UNICODEINDEX

Структура **JET_UNICODEINDEX** настроена для нормализации данных в Юникоде при создании индекса на основе столбца в Юникоде.

```cpp
typedef struct tagJET_UNICODEINDEX {
  unsigned long lcid;
  unsigned long dwMapFlags;
} JET_UNICODEINDEX;
```

### <a name="members"></a>Элементы

**lcid**

КОД локали, используемый при нормализации данных. Любой языковой стандарт может использоваться при условии, что на компьютере установлен соответствующий языковой пакет. Единственное исключение заключается в том, что независимый от языка языковой стандарт (LCID 0) является недопустимым.

**dwMapFlags**

Эти флаги передаются в [LCMapString завершилось ошибкой](/windows/win32/api/winnls/nf-winnls-lcmapstringa) , когда данные в Юникоде нормализуются к ключу, что позволяет определяемым пользователем флагам переопределять значение по умолчанию.

**Windows 2000**: для **dwFlags** доступны только два допустимых значения:

  - (LCMAP_SORTKEY | NORM_IGNORECASE | NORM_IGNOREKANATYPE | NORM_IGNOREWIDTH | NORM_IGNORENONSPACE)

<!-- end list -->

  - (LCMAP_SORTKEY | NORM_IGNORECASE | NORM_IGNOREKANATYPE | NORM_IGNOREWIDTH)

**двмапфлагс** имеет следующие ограничения.


| <p>Значение</p> | <p>Значение</p> | 
|--------------|----------------|
| <p>LCMAP_SORTKEY</p> | <p>Mandatory.</p> | 
| <p>LCMAP_BYTEREV</p> | <p>Необязательный элемент.</p> | 
| <p>NORM_IGNORECASE</p> | <p>Необязательный элемент.</p> | 
| <p>NORM_IGNORENONSPACE</p> | <p>Необязательный элемент.</p> | 
| <p>NORM_IGNORESYMBOLS</p> | <p>Необязательный элемент.</p> | 
| <p>NORM_IGNOREKANATYPE</p> | <p>Необязательный элемент.</p> | 
| <p>NORM_IGNOREWIDTH</p> | <p>Необязательный элемент.</p> | 
| <p>SORT_STRINGSORT</p> | <p>Необязательный элемент.</p> | 



### <a name="requirements"></a>Требования


| | | <p><strong>Клиент</strong></p> | <p>требуется Windows Vista, Windows XP или Windows 2000 Professional.</p> | | <p><strong>Сервер</strong></p> | <p>требуется Windows server 2008, Windows server 2003 или сервер Windows 2000.</p> | | <p><strong>Header</strong></p> | <p>Объявлено в ESENT. h.</p> | 



### <a name="see-also"></a>См. также:

[JET_COLTYP](./jet-coltyp.md)  
[JET_INDEXCREATE](./jet-indexcreate-structure.md)  
[JetOpenTempTable3](./jetopentemptable3-function.md)
