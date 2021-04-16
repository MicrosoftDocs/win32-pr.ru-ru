---
description: Как символьные ссылки влияют на стандартные функции файлов, использующие имена путей для указания одного или нескольких файлов.
ms.assetid: afda53eb-d0db-4844-9dd0-8a7d93ca341f
title: Символьные эффекты ссылок в функциях файловых систем
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6d4a2fe1696bf5260a0c55ba8b6e4f107270d6da
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "105664276"
---
# <a name="symbolic-link-effects-on-file-systems-functions"></a><span data-ttu-id="aa9b7-103">Символьные эффекты ссылок в функциях файловых систем</span><span class="sxs-lookup"><span data-stu-id="aa9b7-103">Symbolic Link Effects on File Systems Functions</span></span>

<span data-ttu-id="aa9b7-104">Несколько стандартных файловых функций, использующих имена путей для указания одного или нескольких файлов, зависят от использования символических ссылок.</span><span class="sxs-lookup"><span data-stu-id="aa9b7-104">Several standard file functions that use path names to specify one or more files are affected by the use of symbolic links.</span></span> <span data-ttu-id="aa9b7-105">В этом разделе перечислены эти функции и описаны изменения в поведении.</span><span class="sxs-lookup"><span data-stu-id="aa9b7-105">This topic lists those functions and describes the changes in behavior:</span></span>

-   [<span data-ttu-id="aa9b7-106">CopyFile и Копифилетрансактед</span><span class="sxs-lookup"><span data-stu-id="aa9b7-106">CopyFile and CopyFileTransacted</span></span>](#copyfile-and-copyfiletransacted)
-   [<span data-ttu-id="aa9b7-107">копифиликс</span><span class="sxs-lookup"><span data-stu-id="aa9b7-107">CopyFileEx</span></span>](#copyfileex)
-   [<span data-ttu-id="aa9b7-108">CreateFile и Креатефилетрансактед</span><span class="sxs-lookup"><span data-stu-id="aa9b7-108">CreateFile and CreateFileTransacted</span></span>](#createfile-and-createfiletransacted)
-   [<span data-ttu-id="aa9b7-109">Креатехардлинк и Креатехардлинктрансактед</span><span class="sxs-lookup"><span data-stu-id="aa9b7-109">CreateHardLink and CreateHardLinkTransacted</span></span>](#createhardlink-and-createhardlinktransacted)
-   [<span data-ttu-id="aa9b7-110">DeleteFile и Делетефилетрансактед</span><span class="sxs-lookup"><span data-stu-id="aa9b7-110">DeleteFile and DeleteFileTransacted</span></span>](#deletefile-and-deletefiletransacted)
-   [<span data-ttu-id="aa9b7-111">финдфирстчанженотификатион</span><span class="sxs-lookup"><span data-stu-id="aa9b7-111">FindFirstChangeNotification</span></span>](#findfirstchangenotification)
-   [<span data-ttu-id="aa9b7-112">FindFirstFile и Финдфирстфилетрансактед</span><span class="sxs-lookup"><span data-stu-id="aa9b7-112">FindFirstFile and FindFirstFileTransacted</span></span>](#findfirstfile-and-findfirstfiletransacted)
-   [<span data-ttu-id="aa9b7-113">финдфирстфиликс</span><span class="sxs-lookup"><span data-stu-id="aa9b7-113">FindFirstFileEx</span></span>](#findfirstfileex)
-   [<span data-ttu-id="aa9b7-114">FindNextFile</span><span class="sxs-lookup"><span data-stu-id="aa9b7-114">FindNextFile</span></span>](#findnextfile)
-   [<span data-ttu-id="aa9b7-115">жетбинаритипе</span><span class="sxs-lookup"><span data-stu-id="aa9b7-115">GetBinaryType</span></span>](#getbinarytype)
-   [<span data-ttu-id="aa9b7-116">Жеткомпресседфилесизе и Жеткомпресседфилесизетрансактед</span><span class="sxs-lookup"><span data-stu-id="aa9b7-116">GetCompressedFileSize and GetCompressedFileSizeTransacted</span></span>](#getcompressedfilesize-and-getcompressedfilesizetransacted)
-   [<span data-ttu-id="aa9b7-117">жетдискфриспаце</span><span class="sxs-lookup"><span data-stu-id="aa9b7-117">GetDiskFreeSpace</span></span>](#getdiskfreespaceex)
-   [<span data-ttu-id="aa9b7-118">жетдискфриспацеекс</span><span class="sxs-lookup"><span data-stu-id="aa9b7-118">GetDiskFreeSpaceEx</span></span>](#getdiskfreespaceex)
-   [<span data-ttu-id="aa9b7-119">GetFileAttributes</span><span class="sxs-lookup"><span data-stu-id="aa9b7-119">GetFileAttributes</span></span>](#getfileattributesex)
-   [<span data-ttu-id="aa9b7-120">Сбой getfileattributesex</span><span class="sxs-lookup"><span data-stu-id="aa9b7-120">GetFileAttributesEx</span></span>](#getfileattributesex)
-   [<span data-ttu-id="aa9b7-121">жетфилесекурити</span><span class="sxs-lookup"><span data-stu-id="aa9b7-121">GetFileSecurity</span></span>](#getfilesecurity)
-   [<span data-ttu-id="aa9b7-122">жеттемппас</span><span class="sxs-lookup"><span data-stu-id="aa9b7-122">GetTempPath</span></span>](#gettemppath)
-   [<span data-ttu-id="aa9b7-123">жетволумеинформатион</span><span class="sxs-lookup"><span data-stu-id="aa9b7-123">GetVolumeInformation</span></span>](#getvolumeinformation)
-   [<span data-ttu-id="aa9b7-124">сетфилеаттрибутес</span><span class="sxs-lookup"><span data-stu-id="aa9b7-124">SetFileAttributes</span></span>](#setfileattributes)
-   [<span data-ttu-id="aa9b7-125">сетфилесекурити</span><span class="sxs-lookup"><span data-stu-id="aa9b7-125">SetFileSecurity</span></span>](#setfilesecurity)
-   [<span data-ttu-id="aa9b7-126">См. также</span><span class="sxs-lookup"><span data-stu-id="aa9b7-126">Related topics</span></span>](#related-topics)

<span data-ttu-id="aa9b7-127">В приведенных ниже описаниях используются следующие термины.</span><span class="sxs-lookup"><span data-stu-id="aa9b7-127">In the descriptions below, the following terms are used:</span></span>

-   <span data-ttu-id="aa9b7-128">Исходный файл — исходный копируемый файл.</span><span class="sxs-lookup"><span data-stu-id="aa9b7-128">Source file—The original file that is to be copied.</span></span>
-   <span data-ttu-id="aa9b7-129">Целевой файл — созданная копия файла.</span><span class="sxs-lookup"><span data-stu-id="aa9b7-129">Destination file—The newly created copy of the file.</span></span>
-   <span data-ttu-id="aa9b7-130">Target — сущность, на которую указывает символьная ссылка.</span><span class="sxs-lookup"><span data-stu-id="aa9b7-130">Target—The entity that a symbolic link points to.</span></span>

> [!Note]  
> <span data-ttu-id="aa9b7-131">Поведение функций, которые принимают маркер, созданный с помощью функции [**CreateFile**](/windows/desktop/api/FileAPI/nf-fileapi-createfilea) , например функции [**функции getFileTime**](/windows/desktop/api/fileapi/nf-fileapi-getfiletime) , будет различаться в зависимости от того, была ли вызвана функция **CreateFile** с помощью флага **файла \_ флаг \_ открытия \_ \_ точки** повторной обработки.</span><span class="sxs-lookup"><span data-stu-id="aa9b7-131">The behavior of functions that accept a handle created using the [**CreateFile**](/windows/desktop/api/FileAPI/nf-fileapi-createfilea) function, such as the [**GetFileTime**](/windows/desktop/api/fileapi/nf-fileapi-getfiletime) function, will differ based on whether or not the **CreateFile** function was called using the **FILE\_FLAG\_OPEN\_REPARSE\_POINT** flag.</span></span> <span data-ttu-id="aa9b7-132">Дополнительные сведения см. в разделах [**CreateFile**](/windows/desktop/api/FileAPI/nf-fileapi-createfilea) и следующие разделы [CreateFile и креатефилетрансактед](#createfile-and-createfiletransacted) .</span><span class="sxs-lookup"><span data-stu-id="aa9b7-132">For more information, see [**CreateFile**](/windows/desktop/api/FileAPI/nf-fileapi-createfilea) and the following [CreateFile and CreateFileTransacted](#createfile-and-createfiletransacted) section.</span></span>

 

## <a name="copyfile-and-copyfiletransacted"></a><span data-ttu-id="aa9b7-133">CopyFile и Копифилетрансактед</span><span class="sxs-lookup"><span data-stu-id="aa9b7-133">CopyFile and CopyFileTransacted</span></span>

<span data-ttu-id="aa9b7-134">Если исходный файл является символьной ссылкой, то фактически скопированный файл является целевым объектом символьной ссылки.</span><span class="sxs-lookup"><span data-stu-id="aa9b7-134">If the source file is a symbolic link, the actual file copied is the target of the symbolic link.</span></span>

<span data-ttu-id="aa9b7-135">Если конечный файл уже существует и является символьной ссылкой, то символьная ссылка перезаписывается исходным файлом.</span><span class="sxs-lookup"><span data-stu-id="aa9b7-135">If the destination file already exists and is a symbolic link, the symbolic link is overwritten by the source file.</span></span>

## <a name="copyfileex"></a><span data-ttu-id="aa9b7-136">копифиликс</span><span class="sxs-lookup"><span data-stu-id="aa9b7-136">CopyFileEx</span></span>

<span data-ttu-id="aa9b7-137">Если задано копирование **\_ файла Copy \_ \_ символьную ссылку** и:</span><span class="sxs-lookup"><span data-stu-id="aa9b7-137">If **COPY\_FILE\_COPY\_SYMLINK** is specified and:</span></span>

-   <span data-ttu-id="aa9b7-138">Если исходный файл является символьной ссылкой, копируется символьная ссылка, а не целевой файл.</span><span class="sxs-lookup"><span data-stu-id="aa9b7-138">If the source file is a symbolic link, the symbolic link is copied, not the target file.</span></span>
-   <span data-ttu-id="aa9b7-139">Если исходный файл не является символьной ссылкой, поведение не изменяется.</span><span class="sxs-lookup"><span data-stu-id="aa9b7-139">If the source file is not a symbolic link, there is no change in behavior.</span></span>
-   <span data-ttu-id="aa9b7-140">Если целевой файл является существующей символьной ссылкой, то символьная ссылка перезаписывается, а не на целевой файл.</span><span class="sxs-lookup"><span data-stu-id="aa9b7-140">If the destination file is an existing symbolic link, the symbolic link is overwritten, not the target file.</span></span>
-   <span data-ttu-id="aa9b7-141">Если также указан параметр exist (если **\_ \_ \_ \_ существует** ) и файл назначения является существующей символьной ссылкой, то операция завершается ошибкой во всех случаях.</span><span class="sxs-lookup"><span data-stu-id="aa9b7-141">If **COPY\_FILE\_FAIL\_IF\_EXISTS** is also specified, and the destination file is an existing symbolic link, the operation fails in all cases.</span></span>

<span data-ttu-id="aa9b7-142">Если **копия \_ файла \_ Copy \_ символьную ссылку** не указана и:</span><span class="sxs-lookup"><span data-stu-id="aa9b7-142">If **COPY\_FILE\_COPY\_SYMLINK** is not specified and:</span></span>

-   <span data-ttu-id="aa9b7-143">Если также задан параметр **\_ \_ \_ \_ Exists** if, а файл назначения является существующей символьной ссылкой, операция завершается ошибкой, только если существует целевой объект символьной ссылки.</span><span class="sxs-lookup"><span data-stu-id="aa9b7-143">If **COPY\_FILE\_FAIL\_IF\_EXISTS** is also specified, and the destination file is an existing symbolic link, the operation fails only if the target of the symbolic link exists.</span></span>
-   <span data-ttu-id="aa9b7-144">Если не задано значение **\_ \_ \_ \_ Exists** , то поведение при копировании файла не изменяется.</span><span class="sxs-lookup"><span data-stu-id="aa9b7-144">If **COPY\_FILE\_FAIL\_IF\_EXISTS** is not specified, there is no change in behavior.</span></span>

<span data-ttu-id="aa9b7-145">**Windows Server 2003 и Windows XP:** Флаг **\_ копирования файла \_ Copy \_ символьную ссылку** не поддерживается.</span><span class="sxs-lookup"><span data-stu-id="aa9b7-145">**Windows Server 2003 and Windows XP:** The **COPY\_FILE\_COPY\_SYMLINK** flag is not supported.</span></span> <span data-ttu-id="aa9b7-146">Если исходный файл является символьной ссылкой, то фактически скопированный файл является целевым объектом символьной ссылки.</span><span class="sxs-lookup"><span data-stu-id="aa9b7-146">If the source file is a symbolic link, the actual file copied is the target of the symbolic link.</span></span>

## <a name="createfile-and-createfiletransacted"></a><span data-ttu-id="aa9b7-147">CreateFile и Креатефилетрансактед</span><span class="sxs-lookup"><span data-stu-id="aa9b7-147">CreateFile and CreateFileTransacted</span></span>

<span data-ttu-id="aa9b7-148">Если вызов этой функции создает новый файл, поведение не изменяется.</span><span class="sxs-lookup"><span data-stu-id="aa9b7-148">If the call to this function creates a new file, there is no change in behavior.</span></span>

<span data-ttu-id="aa9b7-149">Если указан параметр **\_ \_ открыть \_ \_ точку** повторного анализа, используется значение, и:</span><span class="sxs-lookup"><span data-stu-id="aa9b7-149">If **FILE\_FLAG\_OPEN\_REPARSE\_POINT** is specified and:</span></span>

-   <span data-ttu-id="aa9b7-150">Если существующий файл открыт и является символьной ссылкой, возвращаемый маркер является маркером для символьной ссылки.</span><span class="sxs-lookup"><span data-stu-id="aa9b7-150">If an existing file is opened and it is a symbolic link, the handle returned is a handle to the symbolic link.</span></span>
-   <span data-ttu-id="aa9b7-151">Если задан параметр **создать \_ всегда**, **усекать \_ существующий** или **\_ удалить флаг \_ файла \_ при \_ закрытии** , то затронутый файл является символьной ссылкой.</span><span class="sxs-lookup"><span data-stu-id="aa9b7-151">If **CREATE\_ALWAYS**, **TRUNCATE\_EXISTING**, or **FILE\_FLAG\_DELETE\_ON\_CLOSE** are specified, the file affected is a symbolic link.</span></span>

<span data-ttu-id="aa9b7-152">Если не задана **\_ \_ открытая \_ \_ точка** повторного анализа, если не указан флаг файла и:</span><span class="sxs-lookup"><span data-stu-id="aa9b7-152">If **FILE\_FLAG\_OPEN\_REPARSE\_POINT** is not specified and:</span></span>

-   <span data-ttu-id="aa9b7-153">Если существующий файл открыт и является символьной ссылкой, возвращаемый маркер является обработкой целевого объекта.</span><span class="sxs-lookup"><span data-stu-id="aa9b7-153">If an existing file is opened and it is a symbolic link, the handle returned is a handle to the target.</span></span>
-   <span data-ttu-id="aa9b7-154">Если задан параметр **создать \_ всегда**, **усекать \_ существующий** или **\_ удалить флаг \_ файла \_ при \_ закрытии** , то затронутый файл является целевым объектом.</span><span class="sxs-lookup"><span data-stu-id="aa9b7-154">If **CREATE\_ALWAYS**, **TRUNCATE\_EXISTING**, or **FILE\_FLAG\_DELETE\_ON\_CLOSE** are specified, the file affected is the target.</span></span>

## <a name="createhardlink-and-createhardlinktransacted"></a><span data-ttu-id="aa9b7-155">Креатехардлинк и Креатехардлинктрансактед</span><span class="sxs-lookup"><span data-stu-id="aa9b7-155">CreateHardLink and CreateHardLinkTransacted</span></span>

<span data-ttu-id="aa9b7-156">Если путь указывает на символьную ссылку, функция создает жесткую связь с целевым объектом.</span><span class="sxs-lookup"><span data-stu-id="aa9b7-156">If the path points to a symbolic link, the function creates a hard link to the target.</span></span>

## <a name="deletefile-and-deletefiletransacted"></a><span data-ttu-id="aa9b7-157">DeleteFile и Делетефилетрансактед</span><span class="sxs-lookup"><span data-stu-id="aa9b7-157">DeleteFile and DeleteFileTransacted</span></span>

<span data-ttu-id="aa9b7-158">Если путь указывает на символьную ссылку, то символьная ссылка удаляется, а не на целевой объект.</span><span class="sxs-lookup"><span data-stu-id="aa9b7-158">If the path points to a symbolic link, the symbolic link is deleted, not the target.</span></span> <span data-ttu-id="aa9b7-159">Чтобы удалить целевой объект, необходимо вызвать [**CreateFile**](/windows/desktop/api/FileAPI/nf-fileapi-createfilea) и указать параметр **\_ удалить флаг \_ файла \_ при \_ закрытии**.</span><span class="sxs-lookup"><span data-stu-id="aa9b7-159">To delete a target, you must call [**CreateFile**](/windows/desktop/api/FileAPI/nf-fileapi-createfilea) and specify **FILE\_FLAG\_DELETE\_ON\_CLOSE**.</span></span>

## <a name="findfirstchangenotification"></a><span data-ttu-id="aa9b7-160">финдфирстчанженотификатион</span><span class="sxs-lookup"><span data-stu-id="aa9b7-160">FindFirstChangeNotification</span></span>

<span data-ttu-id="aa9b7-161">Если путь указывает на символьную ссылку, для целевого объекта создается маркер уведомления.</span><span class="sxs-lookup"><span data-stu-id="aa9b7-161">If the path points to a symbolic link, the notification handle is created for the target.</span></span> <span data-ttu-id="aa9b7-162">Если приложение зарегистрировано для получения уведомлений об изменениях каталога, содержащего символьные ссылки, приложение уведомляется только при изменении символьных ссылок, а не на целевых файлах.</span><span class="sxs-lookup"><span data-stu-id="aa9b7-162">If an application has registered to receive change notifications for a directory that contains symbolic links, the application is only notified when the symbolic links have been changed, not the target files.</span></span>

## <a name="findfirstfile-and-findfirstfiletransacted"></a><span data-ttu-id="aa9b7-163">FindFirstFile и Финдфирстфилетрансактед</span><span class="sxs-lookup"><span data-stu-id="aa9b7-163">FindFirstFile and FindFirstFileTransacted</span></span>

<span data-ttu-id="aa9b7-164">Если путь указывает на символьную ссылку, буфер [**Win32 \_ Find \_**](/windows/desktop/api/MinWinBase/ns-minwinbase-win32_find_dataa) содержит сведения о символьной ссылке, а не целевом объекте.</span><span class="sxs-lookup"><span data-stu-id="aa9b7-164">If the path points to a symbolic link, the [**WIN32\_FIND\_DATA**](/windows/desktop/api/MinWinBase/ns-minwinbase-win32_find_dataa) buffer contains information about the symbolic link, not the target.</span></span>

## <a name="findfirstfileex"></a><span data-ttu-id="aa9b7-165">финдфирстфиликс</span><span class="sxs-lookup"><span data-stu-id="aa9b7-165">FindFirstFileEx</span></span>

<span data-ttu-id="aa9b7-166">Если путь указывает на символьную ссылку, буфер [**Win32 \_ Find \_**](/windows/desktop/api/MinWinBase/ns-minwinbase-win32_find_dataa) содержит сведения о символьной ссылке, а не целевом объекте.</span><span class="sxs-lookup"><span data-stu-id="aa9b7-166">If the path points to a symbolic link, the [**WIN32\_FIND\_DATA**](/windows/desktop/api/MinWinBase/ns-minwinbase-win32_find_dataa) buffer contains information about the symbolic link, not the target.</span></span>

## <a name="findnextfile"></a><span data-ttu-id="aa9b7-167">FindNextFile</span><span class="sxs-lookup"><span data-stu-id="aa9b7-167">FindNextFile</span></span>

<span data-ttu-id="aa9b7-168">Если путь указывает на символьную ссылку, буфер [**Win32 \_ Find \_**](/windows/desktop/api/MinWinBase/ns-minwinbase-win32_find_dataa) содержит сведения о символьной ссылке, а не целевом объекте.</span><span class="sxs-lookup"><span data-stu-id="aa9b7-168">If the path points to a symbolic link, the [**WIN32\_FIND\_DATA**](/windows/desktop/api/MinWinBase/ns-minwinbase-win32_find_dataa) buffer contains information about the symbolic link, not the target.</span></span>

## <a name="getbinarytype"></a><span data-ttu-id="aa9b7-169">жетбинаритипе</span><span class="sxs-lookup"><span data-stu-id="aa9b7-169">GetBinaryType</span></span>

<span data-ttu-id="aa9b7-170">Если путь указывает на символьную ссылку, используется целевой файл.</span><span class="sxs-lookup"><span data-stu-id="aa9b7-170">If the path points to a symbolic link, the target file is used.</span></span>

## <a name="getcompressedfilesize-and-getcompressedfilesizetransacted"></a><span data-ttu-id="aa9b7-171">Жеткомпресседфилесизе и Жеткомпресседфилесизетрансактед</span><span class="sxs-lookup"><span data-stu-id="aa9b7-171">GetCompressedFileSize and GetCompressedFileSizeTransacted</span></span>

<span data-ttu-id="aa9b7-172">Если путь указывает на символьную ссылку, функция возвращает размер файла целевого объекта.</span><span class="sxs-lookup"><span data-stu-id="aa9b7-172">If the path points to a symbolic link, the function returns the file size of the target.</span></span>

## <a name="getdiskfreespace"></a><span data-ttu-id="aa9b7-173">жетдискфриспаце</span><span class="sxs-lookup"><span data-stu-id="aa9b7-173">GetDiskFreeSpace</span></span>

<span data-ttu-id="aa9b7-174">Если путь указывает на символьную ссылку, операция выполняется на целевом объекте.</span><span class="sxs-lookup"><span data-stu-id="aa9b7-174">If the path points to a symbolic link, the operation is performed on the target.</span></span>

## <a name="getdiskfreespaceex"></a><span data-ttu-id="aa9b7-175">жетдискфриспацеекс</span><span class="sxs-lookup"><span data-stu-id="aa9b7-175">GetDiskFreeSpaceEx</span></span>

<span data-ttu-id="aa9b7-176">Если путь указывает на символьную ссылку, операция выполняется на целевом объекте.</span><span class="sxs-lookup"><span data-stu-id="aa9b7-176">If the path points to a symbolic link, the operation is performed on the target.</span></span>

## <a name="getfileattributes"></a><span data-ttu-id="aa9b7-177">GetFileAttributes</span><span class="sxs-lookup"><span data-stu-id="aa9b7-177">GetFileAttributes</span></span>

<span data-ttu-id="aa9b7-178">Если путь указывает на символьную ссылку, функция возвращает атрибуты для символьной ссылки.</span><span class="sxs-lookup"><span data-stu-id="aa9b7-178">If the path points to a symbolic link, the function returns attributes for the symbolic link.</span></span>

## <a name="getfileattributesex"></a><span data-ttu-id="aa9b7-179">Сбой getfileattributesex</span><span class="sxs-lookup"><span data-stu-id="aa9b7-179">GetFileAttributesEx</span></span>

<span data-ttu-id="aa9b7-180">Если путь указывает на символьную ссылку, функция возвращает атрибуты для символьной ссылки.</span><span class="sxs-lookup"><span data-stu-id="aa9b7-180">If the path points to a symbolic link, the function returns attributes for the symbolic link.</span></span>

## <a name="getfilesecurity"></a><span data-ttu-id="aa9b7-181">жетфилесекурити</span><span class="sxs-lookup"><span data-stu-id="aa9b7-181">GetFileSecurity</span></span>

<span data-ttu-id="aa9b7-182">Если путь указывает на символьную ссылку, функция возвращает атрибуты для символьной ссылки.</span><span class="sxs-lookup"><span data-stu-id="aa9b7-182">If the path points to a symbolic link, the function returns attributes for the symbolic link.</span></span>

## <a name="gettemppath"></a><span data-ttu-id="aa9b7-183">жеттемппас</span><span class="sxs-lookup"><span data-stu-id="aa9b7-183">GetTempPath</span></span>

<span data-ttu-id="aa9b7-184">Если путь указывает на символьную ссылку, то имя временного пути поддерживает все символьные ссылки.</span><span class="sxs-lookup"><span data-stu-id="aa9b7-184">If the path points to a symbolic link, the temp path name maintains any symbolic links.</span></span>

## <a name="getvolumeinformation"></a><span data-ttu-id="aa9b7-185">жетволумеинформатион</span><span class="sxs-lookup"><span data-stu-id="aa9b7-185">GetVolumeInformation</span></span>

<span data-ttu-id="aa9b7-186">Если путь указывает на символьную ссылку, функция возвращает сведения о томе для целевого объекта.</span><span class="sxs-lookup"><span data-stu-id="aa9b7-186">If the path points to a symbolic link, the function returns volume information for the target.</span></span>

## <a name="setfileattributes"></a><span data-ttu-id="aa9b7-187">сетфилеаттрибутес</span><span class="sxs-lookup"><span data-stu-id="aa9b7-187">SetFileAttributes</span></span>

<span data-ttu-id="aa9b7-188">Если путь указывает на символьную ссылку, функция получает атрибуты для символьной ссылки.</span><span class="sxs-lookup"><span data-stu-id="aa9b7-188">If the path points to a symbolic link, the function retrieves attributes for the symbolic link.</span></span>

## <a name="setfilesecurity"></a><span data-ttu-id="aa9b7-189">сетфилесекурити</span><span class="sxs-lookup"><span data-stu-id="aa9b7-189">SetFileSecurity</span></span>

<span data-ttu-id="aa9b7-190">Если путь указывает на символьную ссылку, функция возвращает атрибуты для символьной ссылки.</span><span class="sxs-lookup"><span data-stu-id="aa9b7-190">If the path points to a symbolic link, the function returns attributes for the symbolic link.</span></span>

## <a name="related-topics"></a><span data-ttu-id="aa9b7-191">См. также</span><span class="sxs-lookup"><span data-stu-id="aa9b7-191">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="aa9b7-192">**CopyFile**</span><span class="sxs-lookup"><span data-stu-id="aa9b7-192">**CopyFile**</span></span>](/windows/desktop/api/WinBase/nf-winbase-copyfile)
</dt> <dt>

[<span data-ttu-id="aa9b7-193">**копифилетрансактед**</span><span class="sxs-lookup"><span data-stu-id="aa9b7-193">**CopyFileTransacted**</span></span>](/windows/desktop/api/WinBase/nf-winbase-copyfiletransacteda)
</dt> <dt>

[<span data-ttu-id="aa9b7-194">**копифиликс**</span><span class="sxs-lookup"><span data-stu-id="aa9b7-194">**CopyFileEx**</span></span>](/windows/desktop/api/WinBase/nf-winbase-copyfileexa)
</dt> <dt>

[<span data-ttu-id="aa9b7-195">**CreateFile**</span><span class="sxs-lookup"><span data-stu-id="aa9b7-195">**CreateFile**</span></span>](/windows/desktop/api/FileAPI/nf-fileapi-createfilea)
</dt> <dt>

[<span data-ttu-id="aa9b7-196">**креатефилетрансактед**</span><span class="sxs-lookup"><span data-stu-id="aa9b7-196">**CreateFileTransacted**</span></span>](/windows/desktop/api/WinBase/nf-winbase-createfiletransacteda)
</dt> <dt>

[<span data-ttu-id="aa9b7-197">**креатехардлинк**</span><span class="sxs-lookup"><span data-stu-id="aa9b7-197">**CreateHardLink**</span></span>](/windows/desktop/api/WinBase/nf-winbase-createhardlinka)
</dt> <dt>

[<span data-ttu-id="aa9b7-198">**креатехардлинктрансактед**</span><span class="sxs-lookup"><span data-stu-id="aa9b7-198">**CreateHardLinkTransacted**</span></span>](/windows/desktop/api/WinBase/nf-winbase-createhardlinktransacteda)
</dt> <dt>

[<span data-ttu-id="aa9b7-199">**DeleteFile**</span><span class="sxs-lookup"><span data-stu-id="aa9b7-199">**DeleteFile**</span></span>](/windows/desktop/api/FileAPI/nf-fileapi-deletefilea)
</dt> <dt>

[<span data-ttu-id="aa9b7-200">**делетефилетрансактед**</span><span class="sxs-lookup"><span data-stu-id="aa9b7-200">**DeleteFileTransacted**</span></span>](/windows/desktop/api/WinBase/nf-winbase-deletefiletransacteda)
</dt> <dt>

[<span data-ttu-id="aa9b7-201">**финдфирстчанженотификатион**</span><span class="sxs-lookup"><span data-stu-id="aa9b7-201">**FindFirstChangeNotification**</span></span>](/windows/desktop/api/FileAPI/nf-fileapi-findfirstchangenotificationa)
</dt> <dt>

[<span data-ttu-id="aa9b7-202">**FindFirstFile**</span><span class="sxs-lookup"><span data-stu-id="aa9b7-202">**FindFirstFile**</span></span>](/windows/desktop/api/FileAPI/nf-fileapi-findfirstfilea)
</dt> <dt>

[<span data-ttu-id="aa9b7-203">**финдфирстфиликс**</span><span class="sxs-lookup"><span data-stu-id="aa9b7-203">**FindFirstFileEx**</span></span>](/windows/desktop/api/FileAPI/nf-fileapi-findfirstfileexa)
</dt> <dt>

[<span data-ttu-id="aa9b7-204">**финдфирстфилетрансактед**</span><span class="sxs-lookup"><span data-stu-id="aa9b7-204">**FindFirstFileTransacted**</span></span>](/windows/desktop/api/WinBase/nf-winbase-findfirstfiletransacteda)
</dt> <dt>

[<span data-ttu-id="aa9b7-205">**FindNextFile**</span><span class="sxs-lookup"><span data-stu-id="aa9b7-205">**FindNextFile**</span></span>](/windows/desktop/api/FileAPI/nf-fileapi-findnextfilea)
</dt> <dt>

[<span data-ttu-id="aa9b7-206">**жетбинаритипе**</span><span class="sxs-lookup"><span data-stu-id="aa9b7-206">**GetBinaryType**</span></span>](/windows/desktop/api/WinBase/nf-winbase-getbinarytypea)
</dt> <dt>

[<span data-ttu-id="aa9b7-207">**жеткомпресседфилесизе**</span><span class="sxs-lookup"><span data-stu-id="aa9b7-207">**GetCompressedFileSize**</span></span>](/windows/desktop/api/fileapi/nf-fileapi-getcompressedfilesizea)
</dt> <dt>

[<span data-ttu-id="aa9b7-208">**жеткомпресседфилесизетрансактед**</span><span class="sxs-lookup"><span data-stu-id="aa9b7-208">**GetCompressedFileSizeTransacted**</span></span>](/windows/desktop/api/WinBase/nf-winbase-getcompressedfilesizetransacteda)
</dt> <dt>

[<span data-ttu-id="aa9b7-209">**жетдискфриспаце**</span><span class="sxs-lookup"><span data-stu-id="aa9b7-209">**GetDiskFreeSpace**</span></span>](/windows/desktop/api/FileAPI/nf-fileapi-getdiskfreespacea)
</dt> <dt>

[<span data-ttu-id="aa9b7-210">**жетдискфриспацеекс**</span><span class="sxs-lookup"><span data-stu-id="aa9b7-210">**GetDiskFreeSpaceEx**</span></span>](/windows/desktop/api/FileAPI/nf-fileapi-getdiskfreespaceexa)
</dt> <dt>

[<span data-ttu-id="aa9b7-211">**GetFileAttributes**</span><span class="sxs-lookup"><span data-stu-id="aa9b7-211">**GetFileAttributes**</span></span>](/windows/desktop/api/FileAPI/nf-fileapi-getfileattributesa)
</dt> <dt>

[<span data-ttu-id="aa9b7-212">**Сбой getfileattributesex**</span><span class="sxs-lookup"><span data-stu-id="aa9b7-212">**GetFileAttributesEx**</span></span>](/windows/desktop/api/FileAPI/nf-fileapi-getfileattributesexa)
</dt> <dt>

[<span data-ttu-id="aa9b7-213">**жетфилесекурити**</span><span class="sxs-lookup"><span data-stu-id="aa9b7-213">**GetFileSecurity**</span></span>](/windows/desktop/api/winbase/nf-winbase-getfilesecuritya)
</dt> <dt>

[<span data-ttu-id="aa9b7-214">**жеттемппас**</span><span class="sxs-lookup"><span data-stu-id="aa9b7-214">**GetTempPath**</span></span>](/windows/desktop/api/FileAPI/nf-fileapi-gettemppatha)
</dt> <dt>

[<span data-ttu-id="aa9b7-215">**жетволумеинформатион**</span><span class="sxs-lookup"><span data-stu-id="aa9b7-215">**GetVolumeInformation**</span></span>](/windows/desktop/api/FileAPI/nf-fileapi-getvolumeinformationa)
</dt> <dt>

[<span data-ttu-id="aa9b7-216">**сетфилеаттрибутес**</span><span class="sxs-lookup"><span data-stu-id="aa9b7-216">**SetFileAttributes**</span></span>](/windows/desktop/api/FileAPI/nf-fileapi-setfileattributesa)
</dt> <dt>

[<span data-ttu-id="aa9b7-217">**сетфилесекурити**</span><span class="sxs-lookup"><span data-stu-id="aa9b7-217">**SetFileSecurity**</span></span>](/windows/desktop/api/winbase/nf-winbase-setfilesecuritya)
</dt> </dl>

 

 
