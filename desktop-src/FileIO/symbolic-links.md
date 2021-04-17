---
description: Символьная ссылка — это объект файловой системы, указывающий на другой объект файловой системы. Объект, на который указывает указатель, называется целевым объектом.
ms.assetid: d6bf5df7-bc12-4dec-b116-95d9109f5eb4
title: Символические связи
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f051beb7de0280ba42df782264cef385f8d01a20
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "105684191"
---
# <a name="symbolic-links"></a><span data-ttu-id="bc71b-104">Символические связи</span><span class="sxs-lookup"><span data-stu-id="bc71b-104">Symbolic Links</span></span>

<span data-ttu-id="bc71b-105">Символьная ссылка — это объект файловой системы, указывающий на другой объект файловой системы.</span><span class="sxs-lookup"><span data-stu-id="bc71b-105">A symbolic link is a file-system object that points to another file system object.</span></span> <span data-ttu-id="bc71b-106">Объект, на который указывает указатель, называется целевым объектом.</span><span class="sxs-lookup"><span data-stu-id="bc71b-106">The object being pointed to is called the target.</span></span>

<span data-ttu-id="bc71b-107">Символьные ссылки прозрачны для пользователей; ссылки отображаются как обычные файлы или каталоги и могут быть обработаны пользователем или приложением точно таким же образом.</span><span class="sxs-lookup"><span data-stu-id="bc71b-107">Symbolic links are transparent to users; the links appear as normal files or directories, and can be acted upon by the user or application in exactly the same manner.</span></span>

<span data-ttu-id="bc71b-108">Символьные ссылки предназначены для упрощения миграции и совместимости приложений с операционными системами UNIX.</span><span class="sxs-lookup"><span data-stu-id="bc71b-108">Symbolic links are designed to aid in migration and application compatibility with UNIX operating systems.</span></span> <span data-ttu-id="bc71b-109">Корпорация Майкрософт реализовала символические ссылки для работы так же, как связи UNIX.</span><span class="sxs-lookup"><span data-stu-id="bc71b-109">Microsoft has implemented its symbolic links to function just like UNIX links.</span></span>

<span data-ttu-id="bc71b-110">Дополнительные сведения см. в следующих разделах:</span><span class="sxs-lookup"><span data-stu-id="bc71b-110">For more information, see the following topics.</span></span>

## <a name="in-this-section"></a><span data-ttu-id="bc71b-111">В этом разделе</span><span class="sxs-lookup"><span data-stu-id="bc71b-111">In this section</span></span>



| <span data-ttu-id="bc71b-112">Раздел</span><span class="sxs-lookup"><span data-stu-id="bc71b-112">Topic</span></span>                                                                                                             | <span data-ttu-id="bc71b-113">Описание</span><span class="sxs-lookup"><span data-stu-id="bc71b-113">Description</span></span>                                                                                                                                           |
|-------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="bc71b-114">Символьные эффекты ссылок в функциях файловых систем</span><span class="sxs-lookup"><span data-stu-id="bc71b-114">Symbolic Link Effects on File Systems Functions</span></span>](symbolic-link-effects-on-file-systems-functions.md)<br/> | <span data-ttu-id="bc71b-115">Как символьные ссылки влияют на стандартные функции файлов, использующие имена путей для указания одного или нескольких файлов.</span><span class="sxs-lookup"><span data-stu-id="bc71b-115">How symbolic links affect standard file functions that use path names to specify one or more files.</span></span><br/>                                        |
| [<span data-ttu-id="bc71b-116">Вопросы программирования</span><span class="sxs-lookup"><span data-stu-id="bc71b-116">Programming Considerations</span></span>](symbolic-link-programming-considerations.md)<br/>                             | <span data-ttu-id="bc71b-117">Рекомендации по программированию для работы с символической ссылкой.</span><span class="sxs-lookup"><span data-stu-id="bc71b-117">Programming considerations for working with symbolic links.</span></span><br/>                                                                                |
| [<span data-ttu-id="bc71b-118">Создание символьных ссылок</span><span class="sxs-lookup"><span data-stu-id="bc71b-118">Creating Symbolic Links</span></span>](creating-symbolic-links.md)<br/>                                                 | <span data-ttu-id="bc71b-119">Создайте символические ссылки, использующие абсолютный или относительный путь с помощью функции [**креатесимболиклинк**](/windows/desktop/api/WinBase/nf-winbase-createsymboliclinka) .</span><span class="sxs-lookup"><span data-stu-id="bc71b-119">Create symbolic links that use either an absolute or relative path by using the [**CreateSymbolicLink**](/windows/desktop/api/WinBase/nf-winbase-createsymboliclinka) function.</span></span><br/> |



 

## <a name="supported-operating-systems"></a><span data-ttu-id="bc71b-120">Поддерживаемые операционные системы</span><span class="sxs-lookup"><span data-stu-id="bc71b-120">Supported Operating Systems</span></span>

<span data-ttu-id="bc71b-121">Символьные ссылки доступны в файловой системе NTFS, начиная с Windows Vista.</span><span class="sxs-lookup"><span data-stu-id="bc71b-121">Symbolic links are available in NTFS starting with Windows Vista.</span></span>

 

 




