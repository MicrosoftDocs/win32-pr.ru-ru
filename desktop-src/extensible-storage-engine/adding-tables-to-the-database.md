---
description: 'Дополнительные сведения: Добавление таблиц в базу данных'
title: Добавление таблиц в базу данных
TOCTitle: Adding Tables to the Database
ms:assetid: 176d4fea-c856-441b-bd58-165b37c35095
ms:mtpsurl: https://msdn.microsoft.com/library/Gg269195(v=EXCHG.10)
ms:contentKeyID: 32765498
ms.date: 04/11/2016
ms.topic: article
ms.openlocfilehash: 67569f8efc164cc7156f346b6754f13b296d3b08
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "103990852"
---
# <a name="adding-tables-to-the-database"></a>Добавление таблиц в базу данных


_**Применимо к:** Windows | Windows Server_

## <a name="adding-tables-to-the-database"></a>Добавление таблиц в базу данных

Таблицы представляют собой разнородную коллекцию записей, которые физически и логически группируют данные в базе данных. Таблицы уникально идентифицируются по имени. Идентификатор таблицы ([JET_TABLEID](./jet-tableid.md)) — это указатель на курсор, который используется для обновления таблиц и перехода по ним. Вы можете открыть несколько [JET_TABLEID](./jet-tableid.md) в одной таблице.

Существующая таблица открывается в вызове [жетопентабле](./jetopentable-function.md), а новая таблица создается без строк или столбцов с [жеткреатетабле](./jetcreatetable-function.md). Чтобы атомарным образом создать таблицу с начальным набором столбцов и индексов, вызовите [жеткреатетаблеколумниндекс](./jetcreatetablecolumnindex-function.md) или [JetCreateTableColumnIndex2](./jetcreatetablecolumnindex2-function.md). Исходный размер таблицы указывается в параметре *лпажес* в [жеткреатетабле](./jetcreatetable-function.md) или в элементе **улпажес** структуры [JET_TABLECREATE](./jet-tablecreate-structure.md) в вызове [жеткреатетаблеколумниндекс](./jetcreatetablecolumnindex-function.md). Таблицы автоматически увеличиваются при добавлении данных в таблицу. Рост пропорционально начальному размеру таблицы. Столбцы могут быть добавлены в таблицу в любое время с помощью [жетаддколумн](./jetaddcolumn-function.md). Если приложению больше не требуется доступ к таблице, курсор можно закрыть с помощью [жетклосетабле](./jetclosetable-function.md). Таблицу можно удалить с помощью вызова [жетделететабле](./jetdeletetable-function.md).

Операции с таблицами должны выполняться в контексте транзакции.

## <a name="see-also"></a>См. также:

[Транзакции](./transactions.md)
