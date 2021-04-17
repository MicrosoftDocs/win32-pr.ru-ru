---
description: 'Дополнительные сведения о: использование столбцов в таблице'
title: Использование столбцов в таблице
TOCTitle: Using Columns in a Table
ms:assetid: 064ac59e-d306-4335-a623-754a003f5ebc
ms:mtpsurl: https://msdn.microsoft.com/library/Gg269178(v=EXCHG.10)
ms:contentKeyID: 32765481
ms.date: 04/11/2016
ms.topic: article
ms.openlocfilehash: cd715b171162f63aaf0772ff6ec2e4a6d057a0d6
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "105711194"
---
# <a name="using-columns-in-a-table"></a>Использование столбцов в таблице


_**Применимо к:** Windows | Windows Server_

## <a name="using-columns-in-a-table"></a>Использование столбцов в таблице

Таблицу можно создать с начальным набором столбцов, вызвав [жеткреатетаблеколумниндекс](./jetcreatetablecolumnindex-function.md) или без столбцов путем вызова [жеткреатетабле](./jetcreatetable-function.md). Если таблица создается с начальным набором столбцов в вызове [жеткреатетаблеколумниндекс](./jetcreatetablecolumnindex-function.md) или [JetCreateTableColumnIndex2](./jetcreatetablecolumnindex2-function.md), она содержит структуру [JET_TABLECREATE](./jet-tablecreate-structure.md) (или [JET_TABLECREATE2](./jet-tablecreate2-structure.md)). Эти структуры содержат массив [JET_COLUMNCREATEных](./jet-columncreate-structure.md) структур, определяющих набор столбцов в таблице. Элемент **грбит** задает параметры для столбца, а элемент **колтип** задает тип данных, которые могут быть заданы в столбце.

Если таблица создается без столбцов, ее необходимо добавить, вызвав [жетаддколумн](./jetaddcolumn-function.md) со структурой [JET_COLUMNDEF](./jet-columndef-structure.md) . Элемент **грбит** структуры [JET_COLUMNDEF](./jet-columndef-structure.md) задает параметры в столбце, а элемент **колтип** задает тип данных, которые могут быть заданы в столбце. Значения столбцов по умолчанию задаются в вызове [жетаддколумн](./jetaddcolumn-function.md) путем указания значения в параметре *пвдефаулт* и размера в параметре *кбдефаулт* . Столбец без значения по умолчанию фактически имеет значение по умолчанию NULL.

Значения в таблице могут быть заданы только в контексте транзакции. Транзакция начинается в вызове [жетбегинтрансактион](./jetbegintransaction-function.md) и заканчивается в вызове [жеткоммиттрансактион](./jetcommittransaction-function.md). Внутри транзакции значение одного столбца может быть установлено путем вызова [жетсетколумн](./jetsetcolumn-function.md), или значения нескольких столбцов могут быть заданы путем вызова [жетсетколумнс](./jetsetcolumns-function.md). [Жетсетколумнс](./jetsetcolumns-function.md) использует массив структур [JET_SETCOLUMN](./jet-setcolumn-structure.md) для задания нескольких столбцов в таблице. Данные содержатся в параметре *пвдата* объекта [жетсетколумн](./jetsetcolumn-function.md)или в элементе **пвдата** в структуре [JET_SETCOLUMN](./jet-setcolumn-structure.md) .

Структуры [JET_COLUMNBASE](./jet-columnbase-structure.md), [JET_COLUMNLIST](./jet-columnlist-structure.md)и [JET_COLUMNDEF](./jet-columndef-structure.md) возвращаются в вызовах [жетжеттаблеколумнинфо](./jetgettablecolumninfo-function.md)и [жетжетколумнинфо](./jetgetcolumninfo-function.md) в зависимости от типа извлекаемого столбца. Структура [JET_COLUMNBASE](./jet-columnbase-structure.md) описывает параметры базового столбца, а [JET_COLUMNLIST](./jet-columnlist-structure.md) содержит сведения, необходимые для прохода по временной таблице, созданной функциями [жетжетколумнинфо](./jetgetcolumninfo-function.md) и [жетжеттаблеколумнинфо](./jetgettablecolumninfo-function.md) .
