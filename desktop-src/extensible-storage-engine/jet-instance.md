---
description: 'Дополнительные сведения: JET_INSTANCE'
title: JET_INSTANCE
TOCTitle: JET_INSTANCE
ms:assetid: a4136bec-95b3-42d7-b21b-1df09197bb11
ms:mtpsurl: https://msdn.microsoft.com/library/Gg294048(v=EXCHG.10)
ms:contentKeyID: 32765647
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
ms.openlocfilehash: 1fc288c17c90070d48669c7ad6f1554d52c83278
ms.sourcegitcommit: 9b5faa61c38b2d0c432b7f2dbee8c127b0e28a7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/19/2021
ms.locfileid: "122481770"
---
# <a name="jet_instance"></a>JET_INSTANCE


_**Применимо к:** Windows | Windows Сервером_

## <a name="jet_instance"></a>JET_INSTANCE

Тип данных **JET_INSTANCE** содержит обработчик для экземпляра базы данных, который используется для вызова API Jet.

```cpp
    typedef JET_API_PTR JET_INSTANCE;
```

### <a name="data-types"></a>Типы данных

JET_INSTANCE

Для указания недопустимого обработчика экземпляра можно использовать **значение NULL** или [JET_instanceNil](./invalid-handle-constants.md) .

### <a name="remarks"></a>Комментарии

Этот маркер получается при создании экземпляра базы данных путем вызова функций [жеткреатеинстанце](./jetcreateinstance-function.md), [JetCreateInstance2](./jetcreateinstance2-function.md), [жетинит](./jetinit-function.md)или [JetInit2](./jetinit2-function.md) .

**Windows XP:**  явное использование экземпляров поддерживается только в Windows XP и более поздних выпусках.

**Windows 2000:**  Для каждого процесса поддерживается только один глобальный экземпляр.

### <a name="requirements"></a>Требования


| | | <p><strong>Клиент</strong></p> | <p>требуется Windows Vista, Windows XP или Windows 2000 Professional.</p> | | <p><strong>Сервер</strong></p> | <p>требуется Windows server 2008, Windows server 2003 или сервер Windows 2000.</p> | | <p><strong>Header</strong></p> | <p>Объявлено в ESENT. h.</p> | 



### <a name="see-also"></a>См. также:

[жеткреатеинстанце](./jetcreateinstance-function.md)  
[JetCreateInstance2](./jetcreateinstance2-function.md)  
[жетинит](./jetinit-function.md)  
[JetInit2](./jetinit2-function.md)
