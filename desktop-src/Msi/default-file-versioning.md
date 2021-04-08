---
description: На схемах потоков в следующих разделах показаны правила управления версиями файлов по умолчанию, используемые при наличии того же имени файла ключа, который уже установлен в целевом расположении.
ms.assetid: a09e091c-ee82-4951-b129-d1d4c8948883
title: Управление версиями файлов по умолчанию
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fad33a7af49c28b560d9d558abbc86b220c4cb42
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "103910979"
---
# <a name="default-file-versioning"></a><span data-ttu-id="985ac-103">Управление версиями файлов по умолчанию</span><span class="sxs-lookup"><span data-stu-id="985ac-103">Default File Versioning</span></span>

<span data-ttu-id="985ac-104">На схемах потоков в следующих разделах показаны правила управления версиями файлов по умолчанию, используемые при наличии того же имени файла ключа, который уже установлен в целевом расположении.</span><span class="sxs-lookup"><span data-stu-id="985ac-104">The flow diagrams in the following sections illustrate the default file versioning rules used when the key file of a component being installed has the same name as a file already installed in the target location.</span></span> <span data-ttu-id="985ac-105">Управление версиями файлов по умолчанию также демонстрируется при [замене существующих файлов](replacing-existing-files.md).</span><span class="sxs-lookup"><span data-stu-id="985ac-105">Default file versioning is also illustrated in [Replacing Existing Files](replacing-existing-files.md).</span></span>

<span data-ttu-id="985ac-106">Обратите внимание, что при использовании установщик Windows для оптимизации копирования файлов доступно хэширование файлов.</span><span class="sxs-lookup"><span data-stu-id="985ac-106">Note that with Windows Installer, file hashing is available to optimize the copying of files.</span></span> <span data-ttu-id="985ac-107">Дополнительные сведения см. в разделе [**мсижетфилехаш**](/windows/desktop/api/Msi/nf-msi-msigetfilehasha) и [Таблица мсифилехаш](msifilehash-table.md).</span><span class="sxs-lookup"><span data-stu-id="985ac-107">For details, see [**MsiGetFileHash**](/windows/desktop/api/Msi/nf-msi-msigetfilehasha) and the [MsiFileHash table](msifilehash-table.md).</span></span> <span data-ttu-id="985ac-108">Таблицу Мсифилехаш можно использовать только с файлами без версий.</span><span class="sxs-lookup"><span data-stu-id="985ac-108">The MsiFileHash table can only be used with unversioned files.</span></span>

-   [<span data-ttu-id="985ac-109">Оба файла имеют версию</span><span class="sxs-lookup"><span data-stu-id="985ac-109">Both Files Have a Version</span></span>](both-files-have-a-version.md)
-   [<span data-ttu-id="985ac-110">Ни один из файлов не имеет версии</span><span class="sxs-lookup"><span data-stu-id="985ac-110">Neither File Has a Version</span></span>](neither-file-has-a-version.md)
-   [<span data-ttu-id="985ac-111">Ни один из файлов не имеет версии с проверками хэша файла</span><span class="sxs-lookup"><span data-stu-id="985ac-111">Neither File Has a Version with File Hash Check</span></span>](neither-file-has-a-version-with-file-hash-check.md)
-   [<span data-ttu-id="985ac-112">Один файл имеет версию</span><span class="sxs-lookup"><span data-stu-id="985ac-112">One File Has a Version</span></span>](one-file-has-a-version.md)

 

 



