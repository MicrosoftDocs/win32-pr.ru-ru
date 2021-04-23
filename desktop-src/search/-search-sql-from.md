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
# <a name="from-clause"></a><span data-ttu-id="b99f0-103">Предложение FROM</span><span class="sxs-lookup"><span data-stu-id="b99f0-103">FROM Clause</span></span>

<span data-ttu-id="b99f0-104">После инструкции SELECT используйте предложение FROM, чтобы указать, где искать совпадающие документы.</span><span class="sxs-lookup"><span data-stu-id="b99f0-104">Following the SELECT statement, you use the FROM clause to specify where to search for matching documents.</span></span> <span data-ttu-id="b99f0-105">Ниже приведен синтаксис предложения FROM для локального запроса.</span><span class="sxs-lookup"><span data-stu-id="b99f0-105">The following is the syntax of the FROM clause for a local query:</span></span>


```
FROM [<ComputerName>.]SystemIndex
```



<span data-ttu-id="b99f0-106">В настоящее время Поиск Windows поддерживает только один каталог — Системиндекс.</span><span class="sxs-lookup"><span data-stu-id="b99f0-106">Currently, Windows Search supports only one catalog, SystemIndex.</span></span> <span data-ttu-id="b99f0-107">Чтобы запросить локальный каталог удаленного компьютера, включите имя компьютера перед каталогом и UNC-путь на удаленном компьютере в предложении SCOPE или DIRECTORY.</span><span class="sxs-lookup"><span data-stu-id="b99f0-107">To query the local catalog of a remote computer, include the computer name before the catalog and a Universal Naming Convention (UNC) path on the remote computer in the SCOPE or DIRECTORY clause.</span></span>

<span data-ttu-id="b99f0-108">Область указывается в предложении WHERE как ограничение, как описано в разделе [предикаты Scope и Directory](-search-sql-folderdepth.md) .</span><span class="sxs-lookup"><span data-stu-id="b99f0-108">You specify a scope as a restriction in the WHERE clause, as described in the [SCOPE and DIRECTORY Predicates](-search-sql-folderdepth.md) topic.</span></span>

## <a name="examples"></a><span data-ttu-id="b99f0-109">Примеры</span><span class="sxs-lookup"><span data-stu-id="b99f0-109">Examples</span></span>


```
SELECT System.ItemName,System.ItemUrl
FROM SystemIndex WHERE CONTAINS('Microsoft')

SELECT System.Author,System.ItemName,System.ItemUrl
FROM zarascomputer.SystemIndex WHERE SCOPE='file://zarascomputer/SomeFolder' AND CONTAINS('Microsoft')

SELECT System.Author,System.ItemName,System.ItemUrl
FROM server.SystemIndex WHERE SCOPE='file://server/users' AND CONTAINS('Microsoft')
```



<span data-ttu-id="b99f0-110">Во втором из приведенных выше примеров запрос предназначен для удаленного компьютера с именем «зараскомпутер».</span><span class="sxs-lookup"><span data-stu-id="b99f0-110">In the second of the preceding examples, the query targets a remote computer called "zarascomputer".</span></span> <span data-ttu-id="b99f0-111">Обратите внимание, что это имя компьютера отображается в предложениях FROM и SCOPE.</span><span class="sxs-lookup"><span data-stu-id="b99f0-111">Notice that this computer name appears in both the FROM and SCOPE clauses.</span></span> <span data-ttu-id="b99f0-112">В третьем примере запрос обращается к имени общей папки "Users" на сервере с именем "Server" (где UNC-путь будет являться \\ \\ \\ пользователями сервера).</span><span class="sxs-lookup"><span data-stu-id="b99f0-112">In the third example, the query targets a share name "users" on a server named "server" (where the UNC path would be \\\\server\\users).</span></span>

## <a name="related-topics"></a><span data-ttu-id="b99f0-113">Связанные темы</span><span class="sxs-lookup"><span data-stu-id="b99f0-113">Related topics</span></span>

<dl> <dt>

<span data-ttu-id="b99f0-114">**Reference**</span><span class="sxs-lookup"><span data-stu-id="b99f0-114">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="b99f0-115">Общие сведения о синтаксисе SQL Search</span><span class="sxs-lookup"><span data-stu-id="b99f0-115">Overview of the Search SQL Syntax</span></span>](-search-sql-ovwofsearchquery.md)
</dt> <dt>

[<span data-ttu-id="b99f0-116">Инструкция SELECT</span><span class="sxs-lookup"><span data-stu-id="b99f0-116">SELECT Statement</span></span>](-search-sql-select.md)
</dt> <dt>

[<span data-ttu-id="b99f0-117">Предложения WHERE</span><span class="sxs-lookup"><span data-stu-id="b99f0-117">WHERE Clause</span></span>](-search-sql-where.md)
</dt> <dt>

[<span data-ttu-id="b99f0-118">Предикаты областей и каталогов</span><span class="sxs-lookup"><span data-stu-id="b99f0-118">SCOPE and DIRECTORY Predicates</span></span>](-search-sql-folderdepth.md)
</dt> </dl>

 

 



