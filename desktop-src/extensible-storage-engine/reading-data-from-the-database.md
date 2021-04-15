---
description: 'Дополнительные сведения: чтение данных из базы данных'
title: Чтение данных из базы данных
TOCTitle: Reading Data from the Database
ms:assetid: c3c48918-ccd6-4c34-849c-93bd7533ce92
ms:mtpsurl: https://msdn.microsoft.com/library/Gg294080(v=EXCHG.10)
ms:contentKeyID: 32765695
ms.date: 04/11/2016
ms.topic: article
ms.openlocfilehash: 176cd3189dd1c2701331eff0ef5387827da19b94
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "105683584"
---
# <a name="reading-data-from-the-database"></a>Чтение данных из базы данных


_**Применимо к:** Windows | Windows Server_

## <a name="reading-data-from-the-database"></a>Чтение данных из базы данных

Чтение данных из базы данных должно выполняться в рамках транзакции.

В следующей процедуре показано, как выполнить простую операцию чтения в базе данных.

### <a name="to-read-data-from-a-database"></a>Чтение данных из базы данных

1.  Вызовите [жетбегинтрансактион](./jetbegintransaction-function.md) или [JetBeginTransaction2](./jetbegintransaction2-function.md) с идентификатором сеанса, чтобы начать транзакцию.

2.  Переместите курсор к нужной записи, вызвав [жетмове](./jetmove-function.md) с JET_MoveFirst в параметре *CRowset* . Дополнительные сведения о том, как переместить курсор, см. в статье [индексирование в разделе таблицы](./indexing-in-the-table.md) .

3.  Вызовите [жетжеттаблеколумнинфо](./jetgettablecolumninfo-function.md) для текущей записи с JET_ColInfo, указанным в параметре *инфолевел* , чтобы получить идентификатор столбца для столбца. Идентификатор столбца возвращается в структуре [JET_COLUMNDEF](./jet-columndef-structure.md) .

4.  Прочтите данные из столбца, вызвав [жетретриевеколумн](./jetretrievecolumn-function.md) с идентификатором столбца, полученным на шаге 3 в параметре columnid. Параметр *пвдата* содержит тип данных, указанных в структуре [JET_COLUMNDEF](./jet-columndef-structure.md) , полученной на шаге 3.

5.  Вызовите [жеткоммиттрансактион](./jetcommittransaction-function.md) , чтобы зафиксировать транзакцию в базе данных.
