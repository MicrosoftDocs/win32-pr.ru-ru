---
description: Рекомендации по программированию для работы с символической ссылкой.
ms.assetid: 8966ac3e-a92b-4d68-b40b-e32a4173f869
title: Рекомендации по программированию (локальные файловые системы)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1a5d63c231c88da95efc0e5078506bf9fc0d6d9a
ms.sourcegitcommit: 3d9dce1bd6c84e2b51759e940aa95aa9b459cd20
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/04/2021
ms.locfileid: "105684798"
---
# <a name="programming-considerations-local-file-systems"></a><span data-ttu-id="89c73-103">Рекомендации по программированию (локальные файловые системы)</span><span class="sxs-lookup"><span data-stu-id="89c73-103">Programming Considerations (Local File Systems)</span></span>

<span data-ttu-id="89c73-104">При работе с символическими ссылками учитывайте следующие моменты программирования:</span><span class="sxs-lookup"><span data-stu-id="89c73-104">Keep the following programming considerations in mind when working with symbolic links:</span></span>

-   <span data-ttu-id="89c73-105">Символьные ссылки могут указывать на несуществующий целевой объект.</span><span class="sxs-lookup"><span data-stu-id="89c73-105">Symbolic links can point to a non-existent target.</span></span>
-   <span data-ttu-id="89c73-106">При создании символьной ссылки операционная система не проверяет, существует ли целевой объект.</span><span class="sxs-lookup"><span data-stu-id="89c73-106">When creating a symbolic link, the operating system does not check to see if the target exists.</span></span>
-   <span data-ttu-id="89c73-107">Если приложение пытается открыть несуществующий целевой объект, возвращается **\_ файл ошибки \_ не \_ найден** .</span><span class="sxs-lookup"><span data-stu-id="89c73-107">If an application tries to open a non-existent target, **ERROR\_FILE\_NOT\_FOUND** is returned.</span></span>
-   <span data-ttu-id="89c73-108">Символьные ссылки — это точки повторного анализа.</span><span class="sxs-lookup"><span data-stu-id="89c73-108">Symbolic links are reparse points.</span></span> <span data-ttu-id="89c73-109">Дополнительные сведения см. [в разделе Определение того, является ли каталог подключенной папкой](determining-whether-a-directory-is-a-volume-mount-point.md).</span><span class="sxs-lookup"><span data-stu-id="89c73-109">For more information, see [Determining Whether a Directory Is a Mounted Folder](determining-whether-a-directory-is-a-volume-mount-point.md).</span></span>
-   <span data-ttu-id="89c73-110">В определенном пути допускается не более 63 точек повторного анализа (и, следовательно, символьных ссылок).</span><span class="sxs-lookup"><span data-stu-id="89c73-110">There is a maximum of 63 reparse points (and therefore symbolic links) allowed in a particular path.</span></span>

    <span data-ttu-id="89c73-111">**Windows Server 2003 и Windows XP:** Существует ограничение в 31 точки повторного анализа по любому указанному пути.</span><span class="sxs-lookup"><span data-stu-id="89c73-111">**Windows Server 2003 and Windows XP:** There is a limit of 31 reparse points on any given path.</span></span>

## <a name="related-topics"></a><span data-ttu-id="89c73-112">См. также</span><span class="sxs-lookup"><span data-stu-id="89c73-112">Related topics</span></span>

<dl> <span data-ttu-id="89c73-113"><dt>


</dt> <dt></span><span class="sxs-lookup"><span data-stu-id="89c73-113"><dt>


</dt> <dt></span></span>

[<span data-ttu-id="89c73-114">Жесткие связи и соединения</span><span class="sxs-lookup"><span data-stu-id="89c73-114">Hard Links and Junctions</span></span>](hard-links-and-junctions.md)
</dt> </dl>

 

 



