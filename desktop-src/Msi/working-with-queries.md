---
description: поскольку установщик использует реляционную базу данных, существуют функции для выполнения язык SQL (SQL) запросов к базе данных. следующая процедура описывает использование SQL для запроса к базе данных.
ms.assetid: 1b8fd935-4964-4875-801b-cc6765b16924
title: Работа с запросами
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 17b6ea5a2f0b962b195fde531216f4b57fd5834162e31c1e34fc9ff1dd3695df
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "118942129"
---
# <a name="working-with-queries"></a>Работа с запросами

поскольку установщик использует реляционную базу данных, существуют функции для выполнения язык SQL (SQL) запросов к базе данных. следующая процедура описывает использование SQL для запроса к базе данных.

**Запрос базы данных с помощью SQL**

1.  откройте объект [**представления**](view-object.md) с соответствующей инструкцией SQL, вызвав функцию [**мсидатабасеопенвиев**](/windows/desktop/api/Msiquery/nf-msiquery-msidatabaseopenviewa) .

    Объект [**представления**](view-object.md) — это логическая таблица, созданная путем применения запроса к набору таблиц. SQL запросы должны соответствовать [синтаксису SQL](sql-syntax.md) , предоставленному установщиком. эта инструкция SQL может содержать маркеры параметров, которые не указаны, пока не будет запущен объект **представления** .

2.  Запустите объект [**представления**](view-object.md) , вызвав функцию [**мсивиевексекуте**](/windows/desktop/api/Msiquery/nf-msiquery-msiviewexecute) .
3.  Получите следующую запись из объекта [**представления**](view-object.md) , вызвав функцию [**мсивиевфетч**](/windows/desktop/api/Msiquery/nf-msiquery-msiviewfetch) .
4.  Измените объект [**представления**](view-object.md) , вызвав функцию [**мсивиевмодифи**](/windows/desktop/api/Msiquery/nf-msiquery-msiviewmodify) .

    Можно также проверить данные с помощью [**мсивиевмодифи**](/windows/desktop/api/Msiquery/nf-msiquery-msiviewmodify) , передав соответствующие флаги. Если **мсивиевмодифи** возвращает ошибку \_ недопустимых \_ данных из запроса на проверку, базовые данные повреждены.

5.  Получите подробные сведения об ошибке для объекта [**представления**](view-object.md) , вызвав функцию [**мсивиевжетеррор**](/windows/desktop/api/Msiquery/nf-msiquery-msiviewgeterrora) .
6.  Закройте объект [**представления**](view-object.md) , вызвав функцию [**мсивиевклосе**](/windows/desktop/api/Msiquery/nf-msiquery-msiviewclose) .

дополнительные сведения см. в разделе [примеры запросов к базам данных с помощью SQL и сценария](examples-of-database-queries-using-sql-and-script.md).

 

 



