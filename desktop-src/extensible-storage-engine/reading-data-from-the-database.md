---
description: 'Дополнительные сведения: чтение данных из базы данных'
title: Чтение данных из базы данных
TOCTitle: Reading Data from the Database
ms:assetid: c3c48918-ccd6-4c34-849c-93bd7533ce92
ms:mtpsurl: https://msdn.microsoft.com/library/Gg294080(v=EXCHG.10)
ms:contentKeyID: 32765695
ms.date: 04/11/2016
ms.topic: article
ms.openlocfilehash: 7d33aa2640c07018186a5516d985fd4e46194d39cd4b12b7254f430f889e2484
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119780264"
---
# <a name="reading-data-from-the-database"></a>Чтение данных из базы данных


_**Применимо к:** Windows | Windows Сервером_

## <a name="reading-data-from-the-database"></a>Чтение данных из базы данных

Чтение данных из базы данных должно выполняться в рамках транзакции.

В следующей процедуре показано, как выполнить простую операцию чтения в базе данных.

### <a name="to-read-data-from-a-database"></a>Чтение данных из базы данных

1.  Вызовите [жетбегинтрансактион](./jetbegintransaction-function.md) или [JetBeginTransaction2](./jetbegintransaction2-function.md) с идентификатором сеанса, чтобы начать транзакцию.

2.  Переместите курсор к нужной записи, вызвав [жетмове](./jetmove-function.md) с JET_MoveFirst в параметре *CRowset* . Дополнительные сведения о том, как переместить курсор, см. в статье [индексирование в разделе таблицы](./indexing-in-the-table.md) .

3.  Вызовите [жетжеттаблеколумнинфо](./jetgettablecolumninfo-function.md) для текущей записи с JET_ColInfo, указанным в параметре *инфолевел* , чтобы получить идентификатор столбца для столбца. Идентификатор столбца возвращается в структуре [JET_COLUMNDEF](./jet-columndef-structure.md) .

4.  Прочтите данные из столбца, вызвав [жетретриевеколумн](./jetretrievecolumn-function.md) с идентификатором столбца, полученным на шаге 3 в параметре columnid. Параметр *пвдата* содержит тип данных, указанных в структуре [JET_COLUMNDEF](./jet-columndef-structure.md) , полученной на шаге 3.

5.  Вызовите [жеткоммиттрансактион](./jetcommittransaction-function.md) , чтобы зафиксировать транзакцию в базе данных.
