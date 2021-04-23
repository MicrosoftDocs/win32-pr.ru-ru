---
description: Действие Инсталлфилес копирует файлы, указанные в таблице файлов из исходного каталога, в целевой каталог.
ms.assetid: 187ad82f-13f5-4ea3-913c-2ae7561a6ee6
title: Действие Инсталлфилес
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5c2a0206ec5a64974f27375e175f25ce1888b430
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "105662638"
---
# <a name="installfiles-action"></a><span data-ttu-id="21409-103">Действие Инсталлфилес</span><span class="sxs-lookup"><span data-stu-id="21409-103">InstallFiles Action</span></span>

<span data-ttu-id="21409-104">Действие Инсталлфилес копирует файлы, указанные в таблице файлов из исходного каталога, в целевой каталог.</span><span class="sxs-lookup"><span data-stu-id="21409-104">The InstallFiles action copies files specified in the File table from the source directory to the destination directory.</span></span>

## <a name="sequence-restrictions"></a><span data-ttu-id="21409-105">Ограничения последовательности</span><span class="sxs-lookup"><span data-stu-id="21409-105">Sequence Restrictions</span></span>

<span data-ttu-id="21409-106">Действие Инсталлфилес должно следовать после действия [инсталлвалидате](installvalidate-action.md) и перед всеми зависимыми от файла действиями.</span><span class="sxs-lookup"><span data-stu-id="21409-106">The InstallFiles action must come after the [InstallValidate](installvalidate-action.md) action and before any file-dependent actions.</span></span>

## <a name="actiondata-messages"></a><span data-ttu-id="21409-107">Сообщения Актиондата</span><span class="sxs-lookup"><span data-stu-id="21409-107">ActionData Messages</span></span>



| <span data-ttu-id="21409-108">Поле</span><span class="sxs-lookup"><span data-stu-id="21409-108">Field</span></span> | <span data-ttu-id="21409-109">Описание данных действия</span><span class="sxs-lookup"><span data-stu-id="21409-109">Description of action data</span></span>                      |
|-------|-------------------------------------------------|
| <span data-ttu-id="21409-110">\[1\]</span><span class="sxs-lookup"><span data-stu-id="21409-110">\[1\]</span></span> | <span data-ttu-id="21409-111">Идентификатор установленного файла.</span><span class="sxs-lookup"><span data-stu-id="21409-111">Identifier of installed file.</span></span>                   |
| <span data-ttu-id="21409-112">\[6\]</span><span class="sxs-lookup"><span data-stu-id="21409-112">\[6\]</span></span> | <span data-ttu-id="21409-113">Размер установленного файла в байтах.</span><span class="sxs-lookup"><span data-stu-id="21409-113">Size of installed file in bytes.</span></span>                |
| <span data-ttu-id="21409-114">\[9\]</span><span class="sxs-lookup"><span data-stu-id="21409-114">\[9\]</span></span> | <span data-ttu-id="21409-115">Идентификатор каталога, в котором установлен файл.</span><span class="sxs-lookup"><span data-stu-id="21409-115">Identifier of directory holding installed file.</span></span> |



 

## <a name="remarks"></a><span data-ttu-id="21409-116">Комментарии</span><span class="sxs-lookup"><span data-stu-id="21409-116">Remarks</span></span>

<span data-ttu-id="21409-117">Действие Инсталлфилес работает с файлами, указанными в [таблице File](file-table.md).</span><span class="sxs-lookup"><span data-stu-id="21409-117">The InstallFiles action operates on files specified in the [File table](file-table.md).</span></span> <span data-ttu-id="21409-118">Каждый файл устанавливается на основе состояния установки компонента, связанного с файлом, в [таблице Component](component-table.md).</span><span class="sxs-lookup"><span data-stu-id="21409-118">Each file is installed based on the installation state of the file's associated component in the [Component table](component-table.md).</span></span> <span data-ttu-id="21409-119">Только те файлы, компоненты которых разрешаются в состояние **мсиинсталлстателокал** , могут быть скопированы.</span><span class="sxs-lookup"><span data-stu-id="21409-119">Only those files whose components are resolved to the **msiInstallStatelocal** state are eligible for copying.</span></span>

<span data-ttu-id="21409-120">Действие Инсталлфилес реализует следующие столбцы таблицы File.</span><span class="sxs-lookup"><span data-stu-id="21409-120">The InstallFiles action implements the following columns of the File table.</span></span>

-   <span data-ttu-id="21409-121">В столбце FileName указывается имя целевого файла.</span><span class="sxs-lookup"><span data-stu-id="21409-121">The FileName column specifies the target file name.</span></span>
-   <span data-ttu-id="21409-122">В столбце версия указывается версия файла.</span><span class="sxs-lookup"><span data-stu-id="21409-122">The Version column specifies the file version.</span></span>
-   <span data-ttu-id="21409-123">В столбце атрибуты указываются биты флага файла и атрибута установки.</span><span class="sxs-lookup"><span data-stu-id="21409-123">The Attributes column specifies the file and installation attribute flag bits.</span></span>
-   <span data-ttu-id="21409-124">В столбце File указывается уникальный маркер файла.</span><span class="sxs-lookup"><span data-stu-id="21409-124">The File column specifies the unique file token.</span></span>
-   <span data-ttu-id="21409-125">В столбце Размер файла указан размер несжатого файла в байтах.</span><span class="sxs-lookup"><span data-stu-id="21409-125">The FileSize column specifies the uncompressed file size in bytes.</span></span>
-   <span data-ttu-id="21409-126">В столбце Language указывается идентификатор языка файла.</span><span class="sxs-lookup"><span data-stu-id="21409-126">The Language column specifies the file language identifier.</span></span>
-   <span data-ttu-id="21409-127">В столбце Sequence указывается порядковый номер носителя.</span><span class="sxs-lookup"><span data-stu-id="21409-127">The Sequence column specifies the sequence number on media.</span></span>

<span data-ttu-id="21409-128">Действие Инсталлфилес реализует следующие столбцы таблицы Component.</span><span class="sxs-lookup"><span data-stu-id="21409-128">The InstallFiles action implements the following columns of the Component table.</span></span>

-   <span data-ttu-id="21409-129">Столбец Directory \_ указывает ссылку на элемент [таблицы каталога](directory-table.md) .</span><span class="sxs-lookup"><span data-stu-id="21409-129">The Directory\_ column specifies a reference to a [Directory table](directory-table.md) item.</span></span>
-   <span data-ttu-id="21409-130">В столбце Component указывается уникальное имя элемента компонента.</span><span class="sxs-lookup"><span data-stu-id="21409-130">The Component column specifies a unique name for the component item.</span></span>

<span data-ttu-id="21409-131">Указанный файл копируется только в том случае, если выполняется одно из следующих условий.</span><span class="sxs-lookup"><span data-stu-id="21409-131">The specified file is copied only if one of the following is true:</span></span>

-   <span data-ttu-id="21409-132">Этот файл в данный момент не установлен на локальном компьютере.</span><span class="sxs-lookup"><span data-stu-id="21409-132">The file is not currently installed on the local computer.</span></span>
-   <span data-ttu-id="21409-133">Файл находится на локальном компьютере, но имеет номер версии ниже, чем файл в [таблице File](file-table.md).</span><span class="sxs-lookup"><span data-stu-id="21409-133">The file is on the local computer but has a lower version number than the file in the [File table](file-table.md).</span></span>
-   <span data-ttu-id="21409-134">Файл находится на локальном компьютере, но связанный номер версии отсутствует.</span><span class="sxs-lookup"><span data-stu-id="21409-134">The file is on the local computer, but there is no associated version number.</span></span>

<span data-ttu-id="21409-135">Исходный каталог для каждого копируемого файла определяется Саурцемоде, который, в свою очередь, зависит от значения в столбце "CAB-файл" таблицы Media.</span><span class="sxs-lookup"><span data-stu-id="21409-135">The source directory for each file to be copied is determined by the sourceMode, which in turn depends on the value in the Cabinet column of the Media table.</span></span> <span data-ttu-id="21409-136">Полное описание режима исходного кода см. в [таблице Media](media-table.md).</span><span class="sxs-lookup"><span data-stu-id="21409-136">For a full discussion of the source mode, see the [Media table](media-table.md).</span></span>

<span data-ttu-id="21409-137">Если исходный каталог копируемого файла находится на съемном носителе, например на дискете или компакт-диске, действие Инсталлфилес проверяет, вставлен ли правильный исходный носитель перед попыткой копирования файла.</span><span class="sxs-lookup"><span data-stu-id="21409-137">If the source directory for a file to be copied resides on removable media such as a floppy disk or CD-ROM, the InstallFiles action verifies that the proper source media is inserted before attempting to copy the file.</span></span> <span data-ttu-id="21409-138">Инсталлфилес выполняет поиск носителя того же съемного типа с меткой [*тома*](v-gly.md) , совпадающей со значением, заданным в столбце VolumeLabel таблицы Media.</span><span class="sxs-lookup"><span data-stu-id="21409-138">The InstallFiles searches for media of the same removable type with a [*volume*](v-gly.md) label that matches the value given in the VolumeLabel column of the Media table.</span></span> <span data-ttu-id="21409-139">Если найден соответствующий подключенный том, процесс копирования файла продолжается.</span><span class="sxs-lookup"><span data-stu-id="21409-139">If a matching mounted volume is found, the file copying process proceeds.</span></span> <span data-ttu-id="21409-140">Если совпадений не найдено, диалоговое окно предпросит пользователя вставить нужный носитель.</span><span class="sxs-lookup"><span data-stu-id="21409-140">If no match is found, a dialog box requests that the user to insert the proper media.</span></span> <span data-ttu-id="21409-141">В этом случае диалоговое окно использует имя носителя, найденное в столбце DiskPrompt таблицы Media в составе запроса.</span><span class="sxs-lookup"><span data-stu-id="21409-141">In this case, the dialog box uses the media name found in the DiskPrompt column of the Media table as part of the prompt.</span></span>

<span data-ttu-id="21409-142">Необходимо соблюдать осторожность, так как действие Инсталлфилес может удалить исходный файл и не заменить его.</span><span class="sxs-lookup"><span data-stu-id="21409-142">Caution must be exercised because the InstallFiles action can delete an original file and not replace it.</span></span> <span data-ttu-id="21409-143">Это происходит, когда в действии Инсталлфилес возникает ошибка при замене старого файла, и пользователь решил пропустить эту ошибку.</span><span class="sxs-lookup"><span data-stu-id="21409-143">This occurs when the InstallFiles action experiences an error while replacing an older file and the user chooses to ignore the error.</span></span> <span data-ttu-id="21409-144">Поведение установщика по умолчанию — удалить старый файл, прежде чем гарантировать правильную копию нового файла.</span><span class="sxs-lookup"><span data-stu-id="21409-144">The default behavior of installer is to delete an old file before ensuring the new file is copied correctly.</span></span>

<span data-ttu-id="21409-145">Правила управления версиями файлов, используемые установщиком, см. в разделе [правила управления версиями файлов](file-versioning-rules.md).</span><span class="sxs-lookup"><span data-stu-id="21409-145">For the file versioning rules used by the installer, see [File Versioning Rules](file-versioning-rules.md).</span></span>

 

 



