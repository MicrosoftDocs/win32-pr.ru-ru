---
description: 'Дополнительные сведения: JET_LS'
title: JET_LS
TOCTitle: JET_LS
ms:assetid: 8e4e7902-84b1-404b-8654-bb430a0952aa
ms:mtpsurl: https://msdn.microsoft.com/library/Gg269336(v=EXCHG.10)
ms:contentKeyID: 32765625
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
ms.openlocfilehash: 546ace6b93328c3420a33c131250510d8421491b
ms.sourcegitcommit: 9b5faa61c38b2d0c432b7f2dbee8c127b0e28a7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/19/2021
ms.locfileid: "122470840"
---
# <a name="jet_ls"></a>JET_LS


_**Применимо к:** Windows | Windows Сервером_

## <a name="jet_ls"></a>JET_LS

**JET_LS** тип данных содержит контекстный обработчик для локального хранилища (Ls). Этот маркер может быть связан с курсором или таблицей и может ссылаться на динамически выделенные ресурсы.

**Windows xp: JET_LS** введены в Windows xp.

```cpp
    typedef JET_API_PTR JET_LS;
```

### <a name="data-types"></a>Типы данных

JET_LS

Значение JET_LSNil указывает на недопустимый обработчик контекста.

### <a name="remarks"></a>Комментарии

Обработчик контекста изначально связан с типом данных **JET_LS** с помощью [жетсетлс](./jetsetls-function.md). Маркер контекста можно извлечь из типа данных **JET_LS** с помощью [жетжетлс](./jetgetls-function.md).

Обработчик контекста может быть явно связан с типом данных **JET_LS** с помощью [жетжетлс](./jetgetls-function.md) с JET_bitLSReset. Кроме того, маркер контекста может быть неявно связан с типом данных **JET_LS** , когда базовый объект освобождается ядром СУБД в результате прямого или непрямого действия приложения. В неявном случае для приложения выдается обратный вызов времени выполнения, чтобы он мог очистить контекстный маркер. Дополнительные сведения о неявном разрыве связи с типом данных **JET_LS** см. в разделе [жетсетлс](./jetsetls-function.md).

С типом данных JET_LS связаны следующие флаги.


| <p>Термин</p> | <p>Описание</p> | 
|-------------|--------------------|
| <p>JET_bitLSReset</p> | <p>Маркер контекста не связан с объектом.</p> | 
| <p>JET_bitLSCursor</p> | <p>Задает или получает локальное хранилище, связанное с курсором таблицы.</p> | 
| <p>JET_bitLSTable</p> | <p>Задайте или получите локальное хранилище, связанное с таблицей.</p> | 
| <p>JET_LSNil</p> | <p>Недопустимый маркер контекста.</p> | 



### <a name="requirements"></a>Требования


| | | <p><strong>Клиент</strong></p> | <p>требуется Windows Vista или Windows XP.</p> | | <p><strong>Сервер</strong></p> | <p>требуется Windows server 2008 или Windows server 2003.</p> | | <p><strong>Header</strong></p> | <p>Объявлено в ESENT. h.</p> | 



### <a name="see-also"></a>См. также:

[жетсетлс](./jetsetls-function.md)  
[жетжетлс](./jetgetls-function.md)
