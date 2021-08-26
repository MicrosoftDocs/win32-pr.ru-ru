---
description: 'Дополнительные сведения: JET_ERR'
title: JET_ERR
TOCTitle: JET_ERR
ms:assetid: cd9cb876-251c-458d-a015-8e9045e77fc9
ms:mtpsurl: https://msdn.microsoft.com/library/Gg294092(v=EXCHG.10)
ms:contentKeyID: 32765707
ms.date: 04/11/2016
ms.topic: reference
api_name: ''
topic_type:
- kbArticle
- apiref
api_type:
- COM
api_location: ''
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: f341f88a192fee6de55e0077778abde83493e35e
ms.sourcegitcommit: 9b5faa61c38b2d0c432b7f2dbee8c127b0e28a7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/19/2021
ms.locfileid: "122482280"
---
# <a name="jet_err"></a>JET_ERR


_**Применимо к:** Windows | Windows Сервером_

## <a name="jet_err"></a>JET_ERR

**JET_ERR** тип данных содержит [код ошибки расширяемого механизма служба хранилища](./extensible-storage-engine-error-codes.md).

```cpp
typedef long JET_ERR;
```

### <a name="data-types"></a>Типы данных

JET_ERR

Нулевое значение (соответствующее JET_errSuccess) указывает на Успешный вызов. Положительное значение предупреждает о некритическом условии, произошедшем при успешном вызове по ошибке. Отрицательное значение указывает на сбой вызова.

### <a name="remarks"></a>Комментарии

сведения об возврате ошибок в виде значений hresult см. в разделе [ошибки расширенных служба хранилища Engine](./extensible-storage-engine-errors.md). Дополнительные сведения о флагах настройки базы данных для обработки ошибок см. в разделе [Параметры обработки ошибок](./error-handling-parameters.md).

### <a name="requirements"></a>Требования


| | | <p><strong>Клиент</strong></p> | <p>требуется Windows Vista, Windows XP или Windows 2000 Professional.</p> | | <p><strong>Сервер</strong></p> | <p>требуется Windows server 2008, Windows server 2003 или сервер Windows 2000.</p> | | <p><strong>Header</strong></p> | <p>Объявлено в ESENT. h.</p> | 



### <a name="see-also"></a>См. также:

[ошибки расширенного обработчика служба хранилища](./extensible-storage-engine-errors.md)  
[коды ошибок расширенного механизма служба хранилища](./extensible-storage-engine-error-codes.md)  
[Параметры обработки ошибок](./error-handling-parameters.md)
