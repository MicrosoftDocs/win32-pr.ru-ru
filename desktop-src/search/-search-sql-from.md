---
description: После инструкции SELECT используйте предложение FROM, чтобы указать, где искать совпадающие документы.
ms.assetid: 437d36d1-dd6d-4405-8f35-c37fd04fa0f6
title: Предложение FROM
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 37100a614ca7cc08cdf510f27e42b045acc1ec23
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "105682528"
---
# <a name="from-clause"></a>Предложение FROM

После инструкции SELECT используйте предложение FROM, чтобы указать, где искать совпадающие документы. Ниже приведен синтаксис предложения FROM для локального запроса.


```
FROM [<ComputerName>.]SystemIndex
```



В настоящее время Поиск Windows поддерживает только один каталог — Системиндекс. Чтобы запросить локальный каталог удаленного компьютера, включите имя компьютера перед каталогом и UNC-путь на удаленном компьютере в предложении SCOPE или DIRECTORY.

Область указывается в предложении WHERE как ограничение, как описано в разделе [предикаты Scope и Directory](-search-sql-folderdepth.md) .

## <a name="examples"></a>Примеры


```
SELECT System.ItemName,System.ItemUrl
FROM SystemIndex WHERE CONTAINS('Microsoft')

SELECT System.Author,System.ItemName,System.ItemUrl
FROM zarascomputer.SystemIndex WHERE SCOPE='file://zarascomputer/SomeFolder' AND CONTAINS('Microsoft')

SELECT System.Author,System.ItemName,System.ItemUrl
FROM server.SystemIndex WHERE SCOPE='file://server/users' AND CONTAINS('Microsoft')
```



Во втором из приведенных выше примеров запрос предназначен для удаленного компьютера с именем «зараскомпутер». Обратите внимание, что это имя компьютера отображается в предложениях FROM и SCOPE. В третьем примере запрос обращается к имени общей папки "Users" на сервере с именем "Server" (где UNC-путь будет являться \\ \\ \\ пользователями сервера).

## <a name="related-topics"></a>Связанные темы

<dl> <dt>

**Reference**
</dt> <dt>

[Общие сведения о синтаксисе SQL Search](-search-sql-ovwofsearchquery.md)
</dt> <dt>

[Инструкция SELECT](-search-sql-select.md)
</dt> <dt>

[Предложения WHERE](-search-sql-where.md)
</dt> <dt>

[Предикаты областей и каталогов](-search-sql-folderdepth.md)
</dt> </dl>

 

 



