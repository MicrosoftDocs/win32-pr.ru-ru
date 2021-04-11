---
description: Предикаты глубины папок контролируют область поиска, указывая путь и необходимость выполнения глубокого или неполного обхода.
ms.assetid: 8eadbd42-3538-412e-9bf8-b2355d23437e
title: Предикаты областей и каталогов
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2418b2149a5bf05bd000460c787b7f967856c5c3
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104144098"
---
# <a name="scope-and-directory-predicates"></a>Предикаты областей и каталогов

Предикаты глубины папок контролируют область поиска, указывая путь и необходимость выполнения глубокого или неполного обхода. Ниже показан синтаксис предикатов глубины папок.


```
... WHERE [{SCOPE | DIRECTORY}='<protocol>:[{SID}]<path>']
```



За предикатом следует знак равенства. Путь ексклосед в одинарных кавычках и должен начинаться с протокола и двоеточия (например,, `file:` `mapi:` или `csc:` ). Предикат SCOPE выполняет глубокий обход пути, включая все вложенные папки, в то время как предикат DIRECTORY выполняет неполный обход только указанной папки. Как и другие ограничения язык SQL (SQL), в одном запросе можно указать более одного ограничения на глубину папки.

Чтобы запросить локальный каталог удаленного компьютера, включите имя компьютера перед каталогом и UNC-путь на удаленном компьютере в предложении SCOPE или DIRECTORY.

## <a name="examples"></a>Примеры


```
SELECT System.ItemName FROM SystemIndex WHERE SCOPE='file:C:/Files/Reports'

SELECT System.ItemName FROM SystemIndex WHERE DIRECTORY='file:C:/Files/Reports' 

SELECT System.ItemName FROM SystemIndex WHERE SCOPE='file:C:/Files/Published' OR SCOPE='file:C:/Files/Reports' AND NOT SCOPE='file:C:/Files/Reports/Confidential'

SELECT System.ItemName FROM zarasmachine.SystemIndex WHERE SCOPE='file://zarasmachine/C:/Files/Reports'

SELECT System.ItemURL FROM SystemIndex WHERE SCOPE='mapi://{S-1-5-21-2117521111-1604012920-1887927527-2285604}/Mailbox user/' AND CONTAINS('Microsoft')
```



В первом примере области выполняется поиск в папке C: \\ Files \\ Reports и во всех ее вложенных папках. Пример каталога выполняет поиск только в корневой папке C: \\ Files \\ Reports.

> [!Note]  
> Обратная косая черта файловой системы ( \\ ) преобразуется в символы косой черты в стиле URL-адреса (иногда называемые косой чертой) (/).

 

## <a name="related-topics"></a>Связанные темы

<dl> <dt>

**Reference**
</dt> <dt>

[Предложение FROM](-search-sql-from.md)
</dt> <dt>

[Предложения WHERE](-search-sql-where.md)
</dt> </dl>

 

 



