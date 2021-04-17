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
ms.openlocfilehash: e2eae9590d0151bcdb2dc5621ae6df9e41e068a4
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "105693354"
---
# <a name="jet_tableid"></a>JET_TABLEID


_**Применимо к:** Windows | Windows Server_

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

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><strong>Клиент</strong></p></td>
<td><p>Требуется Windows Vista, Windows XP или Windows 2000 Professional.</p></td>
</tr>
<tr class="even">
<td><p><strong>Server</strong></p></td>
<td><p>Требуется Windows Server 2008, Windows Server 2003 или Windows 2000 Server.</p></td>
</tr>
<tr class="odd">
<td><p><strong>Header</strong></p></td>
<td><p>Объявлено в ESENT. h.</p></td>
</tr>
</tbody>
</table>


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
