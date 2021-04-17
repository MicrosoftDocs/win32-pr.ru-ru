---
description: Каждый файл, который доставляется в целевой пакет установки модулем слияния, должен храниться внутри CAB-файла, внедренного в виде потока в файл. msm. Имя этого ящика всегда MergeModule.CABinet.
ms.assetid: 884df249-977e-4e8e-8978-15331a7c1d8a
title: Создание CAB-файлов MergeModule.CABinet
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2a26eb9bb3daf92d81e21267b2f56706b74d9179
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "105663692"
---
# <a name="generating-mergemodulecabinet-cabinet-files"></a><span data-ttu-id="c0234-104">Создание CAB-файлов MergeModule.CABinet</span><span class="sxs-lookup"><span data-stu-id="c0234-104">Generating MergeModule.CABinet Cabinet Files</span></span>

<span data-ttu-id="c0234-105">Каждый файл, который доставляется в целевой пакет установки модулем слияния, должен храниться внутри CAB-файла, внедренного в виде потока в файл. msm.</span><span class="sxs-lookup"><span data-stu-id="c0234-105">Every file that is delivered to the target installation package by the merge module must be stored inside of a cabinet file embedded as a stream inside the .msm file.</span></span> <span data-ttu-id="c0234-106">Имя этого ящика всегда MergeModule.CABinet.</span><span class="sxs-lookup"><span data-stu-id="c0234-106">The name of this cabinet is always MergeModule.CABinet.</span></span>

<span data-ttu-id="c0234-107">Имена файлов в MergeModule.CABinet должны совпадать с первичными ключами, используемыми в [таблице файлов](file-table.md) модуля слияния, и должны соответствовать правилам, описанным в разделе [именование первичных ключей в базах данных модулей слияния](naming-primary-keys-in-merge-module-databases.md).</span><span class="sxs-lookup"><span data-stu-id="c0234-107">The names of files in MergeModule.CABinet must match the primary keys used in the merge module's [File table](file-table.md) and must adhere to the convention described in [Naming Primary Keys in Merge Module Databases](naming-primary-keys-in-merge-module-databases.md).</span></span>

<span data-ttu-id="c0234-108">Установщик пропускает дополнительные файлы, включенные в MergeModule.CABINET, которые не перечислены в [таблице файлов](file-table.md)модуля слияния.</span><span class="sxs-lookup"><span data-stu-id="c0234-108">The installer skips extra files included in MergeModule.CABinet that are not listed in the merge module's [File table](file-table.md).</span></span> <span data-ttu-id="c0234-109">Порядковые номера файлов, указанных в таблице файлов, не должны быть последовательными, но они должны следовать той же последовательности, что и файлы, хранящиеся в MergeModule.CABinet.</span><span class="sxs-lookup"><span data-stu-id="c0234-109">The sequence numbers of files specified in the File table do not need to be consecutive, but they must follow the same sequence as the files stored inside MergeModule.CABinet.</span></span> <span data-ttu-id="c0234-110">Дополнительные сведения см. в разделе [Создание таблиц файлов модулей слияния](authoring-merge-module-file-tables.md).</span><span class="sxs-lookup"><span data-stu-id="c0234-110">For more information, see [Authoring Merge Module File Tables](authoring-merge-module-file-tables.md).</span></span>

<span data-ttu-id="c0234-111">Это означает, что один CAB-файл может содержать все файлы, необходимые модулю слияния для поддержки нескольких языков.</span><span class="sxs-lookup"><span data-stu-id="c0234-111">This means that a single cabinet file can contain all the files needed for a merge module to support multiple languages.</span></span> <span data-ttu-id="c0234-112">Всем языковым файлам могут быть присвоены уникальные порядковые номера в CAB-файле, а затем можно использовать преобразование языка для добавления или удаления файлов из таблицы File, чтобы получить модуль слияния для определенного языка.</span><span class="sxs-lookup"><span data-stu-id="c0234-112">All the language files can be given unique sequence numbers in the cabinet and then a language transform can be used to add or remove files from the File table to obtain a merge module for a particular language.</span></span> <span data-ttu-id="c0234-113">Дополнительные сведения см. в разделе [Создание модулей слияния для нескольких языков](authoring-multiple-language-merge-modules.md).</span><span class="sxs-lookup"><span data-stu-id="c0234-113">For details, see [Authoring Multiple Language Merge Modules](authoring-multiple-language-merge-modules.md).</span></span>

<span data-ttu-id="c0234-114">MergeModule.CABinet можно добавить в модуль слияния, открыв временную [ \_ таблицу потоков](-streams-table.md).</span><span class="sxs-lookup"><span data-stu-id="c0234-114">MergeModule.CABinet can be added to the merge module by opening a temporary [\_Streams Table](-streams-table.md).</span></span> <span data-ttu-id="c0234-115">Например, средство Msidb.exe, предоставляемое с помощью пакета SDK для установщик Windows, можно использовать для добавления MergeModule.CABINET в модуль слияния.</span><span class="sxs-lookup"><span data-stu-id="c0234-115">For example, the tool Msidb.exe provided with the Windows Installer SDK can be used to add the MergeModule.CABinet to the merge module.</span></span> <span data-ttu-id="c0234-116">Дополнительные сведения см. [в разделе Включение CAB-файла в установку](including-a-cabinet-file-in-an-installation.md).</span><span class="sxs-lookup"><span data-stu-id="c0234-116">For more information, see [Including a Cabinet File in an Installation](including-a-cabinet-file-in-an-installation.md).</span></span>

 

 



