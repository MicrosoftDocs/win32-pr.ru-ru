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
# <a name="scope-and-directory-predicates"></a><span data-ttu-id="79d62-103">Предикаты областей и каталогов</span><span class="sxs-lookup"><span data-stu-id="79d62-103">SCOPE and DIRECTORY Predicates</span></span>

<span data-ttu-id="79d62-104">Предикаты глубины папок контролируют область поиска, указывая путь и необходимость выполнения глубокого или неполного обхода.</span><span class="sxs-lookup"><span data-stu-id="79d62-104">Folder depth predicates control the scope of a search by specifying a path and whether to perform a deep or shallow traversal.</span></span> <span data-ttu-id="79d62-105">Ниже показан синтаксис предикатов глубины папок.</span><span class="sxs-lookup"><span data-stu-id="79d62-105">The following shows the syntax of the folder depth predicates:</span></span>


```
... WHERE [{SCOPE | DIRECTORY}='<protocol>:[{SID}]<path>']
```



<span data-ttu-id="79d62-106">За предикатом следует знак равенства.</span><span class="sxs-lookup"><span data-stu-id="79d62-106">The predicate is followed by an equal sign.</span></span> <span data-ttu-id="79d62-107">Путь ексклосед в одинарных кавычках и должен начинаться с протокола и двоеточия (например,, `file:` `mapi:` или `csc:` ).</span><span class="sxs-lookup"><span data-stu-id="79d62-107">The path is exclosed in single quotes and must begin with a protocol and a colon (for example, `file:`, `mapi:`, or `csc:`).</span></span> <span data-ttu-id="79d62-108">Предикат SCOPE выполняет глубокий обход пути, включая все вложенные папки, в то время как предикат DIRECTORY выполняет неполный обход только указанной папки.</span><span class="sxs-lookup"><span data-stu-id="79d62-108">The SCOPE predicate performs a deep traversal of the path, including all subfolders, while the DIRECTORY predicate does a shallow traversal of only the folder specified.</span></span> <span data-ttu-id="79d62-109">Как и другие ограничения язык SQL (SQL), в одном запросе можно указать более одного ограничения на глубину папки.</span><span class="sxs-lookup"><span data-stu-id="79d62-109">Like other Structured Query Language (SQL) restrictions, you can specify more than one folder depth restriction in a single query.</span></span>

<span data-ttu-id="79d62-110">Чтобы запросить локальный каталог удаленного компьютера, включите имя компьютера перед каталогом и UNC-путь на удаленном компьютере в предложении SCOPE или DIRECTORY.</span><span class="sxs-lookup"><span data-stu-id="79d62-110">To query the local catalog of a remote computer, include the computer name before the catalog and a Universal Naming Convention (UNC) path on the remote computer in the SCOPE or DIRECTORY clause.</span></span>

## <a name="examples"></a><span data-ttu-id="79d62-111">Примеры</span><span class="sxs-lookup"><span data-stu-id="79d62-111">Examples</span></span>


```
SELECT System.ItemName FROM SystemIndex WHERE SCOPE='file:C:/Files/Reports'

SELECT System.ItemName FROM SystemIndex WHERE DIRECTORY='file:C:/Files/Reports' 

SELECT System.ItemName FROM SystemIndex WHERE SCOPE='file:C:/Files/Published' OR SCOPE='file:C:/Files/Reports' AND NOT SCOPE='file:C:/Files/Reports/Confidential'

SELECT System.ItemName FROM zarasmachine.SystemIndex WHERE SCOPE='file://zarasmachine/C:/Files/Reports'

SELECT System.ItemURL FROM SystemIndex WHERE SCOPE='mapi://{S-1-5-21-2117521111-1604012920-1887927527-2285604}/Mailbox user/' AND CONTAINS('Microsoft')
```



<span data-ttu-id="79d62-112">В первом примере области выполняется поиск в папке C: \\ Files \\ Reports и во всех ее вложенных папках.</span><span class="sxs-lookup"><span data-stu-id="79d62-112">The first SCOPE example searches the C:\\Files\\Reports folder and all its subfolders.</span></span> <span data-ttu-id="79d62-113">Пример каталога выполняет поиск только в корневой папке C: \\ Files \\ Reports.</span><span class="sxs-lookup"><span data-stu-id="79d62-113">The DIRECTORY example searches only the root folder C:\\Files\\Reports.</span></span>

> [!Note]  
> <span data-ttu-id="79d62-114">Обратная косая черта файловой системы ( \\ ) преобразуется в символы косой черты в стиле URL-адреса (иногда называемые косой чертой) (/).</span><span class="sxs-lookup"><span data-stu-id="79d62-114">The file system backslashes (\\) become a URL-style slash marks (sometimes called forward slashes) (/).</span></span>

 

## <a name="related-topics"></a><span data-ttu-id="79d62-115">Связанные темы</span><span class="sxs-lookup"><span data-stu-id="79d62-115">Related topics</span></span>

<dl> <dt>

<span data-ttu-id="79d62-116">**Reference**</span><span class="sxs-lookup"><span data-stu-id="79d62-116">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="79d62-117">Предложение FROM</span><span class="sxs-lookup"><span data-stu-id="79d62-117">FROM Clause</span></span>](-search-sql-from.md)
</dt> <dt>

[<span data-ttu-id="79d62-118">Предложения WHERE</span><span class="sxs-lookup"><span data-stu-id="79d62-118">WHERE Clause</span></span>](-search-sql-where.md)
</dt> </dl>

 

 



