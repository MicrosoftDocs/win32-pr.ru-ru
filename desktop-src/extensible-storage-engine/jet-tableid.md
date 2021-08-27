---
description: 'Дополнительные сведения: JET_TABLEID'
title: JET_TABLEID
TOCTitle: JET_TABLEID
ms:assetid: 09705c32-97d8-460c-8b58-921497e29c13
ms:mtpsurl: https://msdn.microsoft.com/library/Gg269182(v=EXCHG.10)
ms:contentKeyID: 32765485
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
ms.openlocfilehash: 04e59ddada8715872978ccc21da11a349e1b7c43
ms.sourcegitcommit: 4665ebce0c106bdb52eef36e544280b496b6f50b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/26/2021
ms.locfileid: "122983577"
---
# <a name="jet_tableid"></a>JET_TABLEID


_**Применимо к:** Windows | Windows Сервером_

## <a name="jet_tableid"></a>JET_TABLEID

JET_TABLEID тип данных содержит указатель на курсор базы данных, используемый для вызова API JET. Курсор можно использовать только с сеансом, который использовался для открытия этого курсора.

```cpp
    typedef JET_API_PTR JET_TABLEID;
```

### <a name="data-types"></a>Типы данных

JET_TABLEID

Для указания недопустимого маркера курсора можно использовать **значение NULL** или [JET_tableidNil](./invalid-handle-constants.md) .

### <a name="remarks"></a>Комментарии

Курсор управляет использованием таблицы для ядра СУБД. Курсор может выполнять следующие задачи:

  - Просмотр записей

  - Поиск записей

  - Выберите эффективный порядок сортировки и видимость этих записей

  - Создание, обновление и удаление записей

  - Изменение схемы таблицы

Поддерживаемые функциональные возможности курсора могут изменяться по мере изменения состояния или типа базовой таблицы. Например, временная таблица может запретить поиск данных при открытии с определенными параметрами. Курсор всегда полностью подключен к базовой таблице и взаимодействует с данными напрямую без кэширования. Почти все основные функции ISAM, предоставляемые этим ядром СУБД, работают с курсором.

Курсор можно создать с помощью [жетопентабле](./jetopentable-function.md) или [жетопентемптабле](./jetopentemptable-function.md). Курсор можно дублировать с помощью [жетдупкурсор](./jetdupcursor-function.md). Курсор можно явно закрыть с помощью [жетклосетабле](./jetclosetable-function.md) или неявно закрыть с помощью [жетендсессион](./jetendsession-function.md) или [жеттерм](./jetterm-function.md). Курсор также может быть неявно закрыт [жетроллбакк](./jetrollback-function.md) , если он был открыт в транзакции, которая была прервана. Максимальное количество курсоров, которые могут быть созданы за один раз, управляется [JET_paramMaxCursors](./resource-parameters.md), которые можно настроить с помощью [жетсетсистемпараметер](./jetsetsystemparameter-function.md).

### <a name="requirements"></a>Требования


| Требование | Применение |
|------------|----------|
| <p><strong>Клиент</strong></p> | <p>требуется Windows Vista, Windows XP или Windows 2000 Professional.</p> | 
| <p><strong>Server</strong></p> | <p>требуется Windows server 2008, Windows server 2003 или сервер Windows 2000.</p> | 
| <p><strong>Header</strong></p> | <p>Объявлено в ESENT. h.</p> | 



### <a name="see-also"></a>См. также:

[JET_paramMaxSessions](./resource-parameters.md)  
[жетклосетабле](./jetclosetable-function.md)  
[жетдупкурсор](./jetdupcursor-function.md)  
[жетендсессион](./jetendsession-function.md)  
[жетопентабле](./jetopentable-function.md)  
[жетопентемптабле](./jetopentemptable-function.md)  
[жетроллбакк](./jetrollback-function.md)  
[жетсетсистемпараметер](./jetsetsystemparameter-function.md)  
[жеттерм](./jetterm-function.md)
