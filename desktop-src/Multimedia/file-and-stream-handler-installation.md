---
title: Установка обработчика файлов и потоков
description: Установка обработчика файлов и потоков
ms.assetid: 8d007ea4-b75a-4b3f-965f-8091fcd4cb2f
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: be94137df69ed35b57b1b8fbeb5c9640dd7636d6
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/16/2019
ms.locfileid: "103779133"
---
# <a name="file-and-stream-handler-installation"></a><span data-ttu-id="f8e68-103">Установка обработчика файлов и потоков</span><span class="sxs-lookup"><span data-stu-id="f8e68-103">File and Stream Handler Installation</span></span>

<span data-ttu-id="f8e68-104">Библиотека Авифиле использует установленные обработчики потоков и файлов для чтения и записи файлов AVI и потоков.</span><span class="sxs-lookup"><span data-stu-id="f8e68-104">The AVIFile library uses installed stream and file handlers for reading and writing AVI files and streams.</span></span> <span data-ttu-id="f8e68-105">Обработчик устанавливается, если он находится в СИСТЕМном каталоге Windows, а реестр содержит следующие сведения, необходимые для описания и обнаружения обработчика:</span><span class="sxs-lookup"><span data-stu-id="f8e68-105">A handler is installed when it resides in the Windows SYSTEM directory and the registry contains the following information needed to describe and identify a handler:</span></span>

-   <span data-ttu-id="f8e68-106">16-байтовый идентификатор класса для обработчика</span><span class="sxs-lookup"><span data-stu-id="f8e68-106">The 16-byte class identifier for the handler</span></span>
-   <span data-ttu-id="f8e68-107">Краткое описание обработчика</span><span class="sxs-lookup"><span data-stu-id="f8e68-107">A brief description of the handler</span></span>
-   <span data-ttu-id="f8e68-108">Имя файла, содержащего обработчик</span><span class="sxs-lookup"><span data-stu-id="f8e68-108">The name of the file containing the handler</span></span>
-   <span data-ttu-id="f8e68-109">Расширение файла, которое может обработать обработчик файлов</span><span class="sxs-lookup"><span data-stu-id="f8e68-109">The file extension that a file handler can process</span></span>
-   <span data-ttu-id="f8e68-110">Доступ к файлам и другие свойства, связанные с обработчиком файлов</span><span class="sxs-lookup"><span data-stu-id="f8e68-110">File-access and other properties associated with a file handler</span></span>
-   <span data-ttu-id="f8e68-111">4-символьные коды, идентифицирующие типы потоков, которые может обработать обработчик потока</span><span class="sxs-lookup"><span data-stu-id="f8e68-111">Four-character codes identifying stream types that a stream handler can process</span></span>

<span data-ttu-id="f8e68-112">Библиотека Авифиле запрашивает в реестре обработчики, которые являются внешними для приложения при открытии файлов и доступе к потокам.</span><span class="sxs-lookup"><span data-stu-id="f8e68-112">The AVIFile library queries the registry for handlers that are external to an application when opening files and accessing streams.</span></span> <span data-ttu-id="f8e68-113">Результатом успешного запроса будет возврат имени файла обработчика, который может обработать тип файла или потока, указанный в запросе.</span><span class="sxs-lookup"><span data-stu-id="f8e68-113">The result of a successful query returns the filename of a handler that can process the file or stream type specified in the query.</span></span> <span data-ttu-id="f8e68-114">Реестр перечисляет каждый обработчик, создавая три записи, которые имеют следующий вид:</span><span class="sxs-lookup"><span data-stu-id="f8e68-114">The registry lists each handler by creating three entries that have the following form:</span></span>


```C++
[HKEY_CLASSES_ROOT\Clsid\{00010023-0000-0000-C000-000000000046}] 
@="Wave File reader/writer" 
[HKEY_CLASSES_ROOT\Clsid\{00010023-0000-0000-C000- 
000000000046}\InprocServer32] 
@="wavefile.dll" 
"ThreadingModel"="Apartment" 
[HKEY_CLASSES_ROOT\Clsid\{00010023-0000-0000-C000- 
000000000046}\AVIFile] 
@="3" 
 
```



<span data-ttu-id="f8e68-115">Эти записи состоят из следующих частей.</span><span class="sxs-lookup"><span data-stu-id="f8e68-115">These entries consist of the following parts.</span></span>



| <span data-ttu-id="f8e68-116">Отделение</span><span class="sxs-lookup"><span data-stu-id="f8e68-116">Part</span></span>                                   | <span data-ttu-id="f8e68-117">Описание</span><span class="sxs-lookup"><span data-stu-id="f8e68-117">Description</span></span>                                                                                                                                                                              |
|----------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="f8e68-118">\_корневой узел классов hKey \_</span><span class="sxs-lookup"><span data-stu-id="f8e68-118">HKEY\_CLASSES\_ROOT</span></span>                    | <span data-ttu-id="f8e68-119">Определяет корневую запись реестра.</span><span class="sxs-lookup"><span data-stu-id="f8e68-119">Identifies the root entry of the registry.</span></span>                                                                                                                                               |
| <span data-ttu-id="f8e68-120">Clsid</span><span class="sxs-lookup"><span data-stu-id="f8e68-120">Clsid</span></span>                                  | <span data-ttu-id="f8e68-121">Определяет эту запись как идентификатор класса.</span><span class="sxs-lookup"><span data-stu-id="f8e68-121">Identifies this entry as a class identifier.</span></span>                                                                                                                                             |
| <span data-ttu-id="f8e68-122">{00010023-0000-0000-C000-000000000046}</span><span class="sxs-lookup"><span data-stu-id="f8e68-122">{00010023-0000-0000-C000-000000000046}</span></span> | <span data-ttu-id="f8e68-123">Указывает идентификатор интерфейса (IID) или идентификатор класса.</span><span class="sxs-lookup"><span data-stu-id="f8e68-123">Specifies an interface identifier (IID) or class identifier.</span></span> <span data-ttu-id="f8e68-124">Это значение является уникальным 16-байтовым идентификатором.</span><span class="sxs-lookup"><span data-stu-id="f8e68-124">This value is a unique 16-byte identifier.</span></span> <span data-ttu-id="f8e68-125">(Идентификатор также может называться идентификатором GUID или UUID в других руководствах.)</span><span class="sxs-lookup"><span data-stu-id="f8e68-125">(The identifier might also be referred to as a GUID or a UUID in other manuals.)</span></span> |
| <span data-ttu-id="f8e68-126">Модуль чтения и записи WAV-файлов</span><span class="sxs-lookup"><span data-stu-id="f8e68-126">Wave File reader/writer</span></span>                | <span data-ttu-id="f8e68-127">Задает строку для описания обработчика.</span><span class="sxs-lookup"><span data-stu-id="f8e68-127">Specifies a string to describe the handler.</span></span> <span data-ttu-id="f8e68-128">Эта строка может отображаться в диалоговых окнах для выбора обработчиков потоков и файлов.</span><span class="sxs-lookup"><span data-stu-id="f8e68-128">This string can be displayed in dialog boxes for selecting stream and file handlers.</span></span>                                                         |
| <span data-ttu-id="f8e68-129">InProcServer32</span><span class="sxs-lookup"><span data-stu-id="f8e68-129">InProcServer32</span></span>                         | <span data-ttu-id="f8e68-130">Указывает файл (в данном примере это WAVEFILE.DLL), который можно загрузить для работы с этим классом.</span><span class="sxs-lookup"><span data-stu-id="f8e68-130">Specifies the file (in this example, WAVEFILE.DLL) that can be loaded to handle this class.</span></span>                                                                                              |
| <span data-ttu-id="f8e68-131">авифиле</span><span class="sxs-lookup"><span data-stu-id="f8e68-131">AVIFile</span></span>                                | <span data-ttu-id="f8e68-132">Задает свойства обработчика файлов.</span><span class="sxs-lookup"><span data-stu-id="f8e68-132">Specifies the properties of a file handler.</span></span> <span data-ttu-id="f8e68-133">В этом примере обработчик может считывать файл AVI и записывать его в него.</span><span class="sxs-lookup"><span data-stu-id="f8e68-133">In this example, the handler can read and write to an AVI file.</span></span>                                                                              |



 

<span data-ttu-id="f8e68-134">Обработчик файлов может иметь одно или несколько свойств, хранящихся в реестре.</span><span class="sxs-lookup"><span data-stu-id="f8e68-134">A file handler can have one or more of its properties stored in the registry.</span></span> <span data-ttu-id="f8e68-135">Следующие константы обозначают свойства, которые в настоящее время связаны с файлом.</span><span class="sxs-lookup"><span data-stu-id="f8e68-135">The following constants identify the properties currently associated with a file.</span></span>



| <span data-ttu-id="f8e68-136">Константа</span><span class="sxs-lookup"><span data-stu-id="f8e68-136">Constant</span></span>                        | <span data-ttu-id="f8e68-137">Описание</span><span class="sxs-lookup"><span data-stu-id="f8e68-137">Description</span></span>                                                          |
|---------------------------------|----------------------------------------------------------------------|
| <span data-ttu-id="f8e68-138">АВИФИЛЕХАНДЛЕР \_ канакцептнонргб</span><span class="sxs-lookup"><span data-stu-id="f8e68-138">AVIFILEHANDLER\_CANACCEPTNONRGB</span></span> | <span data-ttu-id="f8e68-139">Указывает, что обработчик файлов может обрабатывать данные изображения, отличные от RGB.</span><span class="sxs-lookup"><span data-stu-id="f8e68-139">Indicates that a file handler can process image data other than RGB.</span></span> |
| <span data-ttu-id="f8e68-140">АВИФИЛЕХАНДЛЕР \_ CANREAD</span><span class="sxs-lookup"><span data-stu-id="f8e68-140">AVIFILEHANDLER\_CANREAD</span></span>         | <span data-ttu-id="f8e68-141">Указывает, что обработчик файлов может открыть файл с доступом для чтения.</span><span class="sxs-lookup"><span data-stu-id="f8e68-141">Indicates that a file handler can open a file with read access.</span></span>      |
| <span data-ttu-id="f8e68-142">АВИФИЛЕХАНДЛЕР \_ CANWRITE</span><span class="sxs-lookup"><span data-stu-id="f8e68-142">AVIFILEHANDLER\_CANWRITE</span></span>        | <span data-ttu-id="f8e68-143">Указывает, что обработчик файлов может открыть файл с доступом для записи.</span><span class="sxs-lookup"><span data-stu-id="f8e68-143">Indicates that a file handler can open a file with write access.</span></span>     |



 

<span data-ttu-id="f8e68-144">При создании обработчика файлов или потоков можно получить новый идентификатор, выполнив UUIDGEN.EXE.</span><span class="sxs-lookup"><span data-stu-id="f8e68-144">When creating a file or stream handler, you can obtain a new identifier by running UUIDGEN.EXE.</span></span> <span data-ttu-id="f8e68-145">Для создания нового идентификатора всегда используйте UUIDGEN.EXE.</span><span class="sxs-lookup"><span data-stu-id="f8e68-145">Always use UUIDGEN.EXE to create a new identifier.</span></span> <span data-ttu-id="f8e68-146">16-байтовое шестнадцатеричное число, созданное этим исполняемым файлом, уникально идентифицирует обработчик.</span><span class="sxs-lookup"><span data-stu-id="f8e68-146">The 16-byte hexadecimal number created by this executable will uniquely identify your handler.</span></span>

<span data-ttu-id="f8e68-147">Библиотека Авифиле использует дополнительные записи в реестре для идентификации идентификатора класса на основе расширения файла, обрабатываемого обработчиком файлов, или кода из четырех символов, которые могут обрабатываться обработчиком файла или потока.</span><span class="sxs-lookup"><span data-stu-id="f8e68-147">The AVIFile library uses additional entries in the registry to identify a class identifier based on the file extension that a file handler can process or a four-character code that a file or stream handler can process.</span></span> <span data-ttu-id="f8e68-148">Например, следующие записи связывают идентификатор класса с расширением файла. WAV и 4-значный код "WAVE":</span><span class="sxs-lookup"><span data-stu-id="f8e68-148">For example, the following entries associate a class identifier with the file extension .WAV and the four-character code "WAVE":</span></span>


```C++
[HKEY_CLASSES_ROOT\AVIFile\Extensions\WAV] 
@="{00010023-0000-0000-C000-000000000046}" 
[HKEY_CLASSES_ROOT\AVIFile\RIFFHandlers\WAVE] 
@="{00010023-0000-0000-C000-000000000046}" 
 
```



<span data-ttu-id="f8e68-149">Эти записи состоят из следующих частей.</span><span class="sxs-lookup"><span data-stu-id="f8e68-149">These entries consist of the following parts.</span></span>



| <span data-ttu-id="f8e68-150">Отделение</span><span class="sxs-lookup"><span data-stu-id="f8e68-150">Part</span></span>                                   | <span data-ttu-id="f8e68-151">Описание</span><span class="sxs-lookup"><span data-stu-id="f8e68-151">Description</span></span>                                                                                       |
|----------------------------------------|---------------------------------------------------------------------------------------------------|
| <span data-ttu-id="f8e68-152">\_корневой узел классов hKey \_</span><span class="sxs-lookup"><span data-stu-id="f8e68-152">HKEY\_CLASSES\_ROOT</span></span>                    | <span data-ttu-id="f8e68-153">Определяет корневую запись реестра.</span><span class="sxs-lookup"><span data-stu-id="f8e68-153">Identifies the root entry of the registry.</span></span>                                                        |
| <span data-ttu-id="f8e68-154">авифиле</span><span class="sxs-lookup"><span data-stu-id="f8e68-154">AVIFile</span></span>                                | <span data-ttu-id="f8e68-155">Определяет эту запись как запись, используемую Авифиле.</span><span class="sxs-lookup"><span data-stu-id="f8e68-155">Identifies this entry as an entry used by AVIFile.</span></span>                                                |
| <span data-ttu-id="f8e68-156">Модули</span><span class="sxs-lookup"><span data-stu-id="f8e68-156">Extensions</span></span>                             | <span data-ttu-id="f8e68-157">Указывает расширение файла (в этом примере —. WAV), которую обработчик файлов может обработать.</span><span class="sxs-lookup"><span data-stu-id="f8e68-157">Specifies the file extension (in this example, .WAV) that a file handler can process.</span></span>             |
| <span data-ttu-id="f8e68-158">риффхандлерс</span><span class="sxs-lookup"><span data-stu-id="f8e68-158">RIFFHandlers</span></span>                           | <span data-ttu-id="f8e68-159">Задает код из четырех символов (в этом примере это «WAVE»), который может обрабатываться обработчиком файла или потока.</span><span class="sxs-lookup"><span data-stu-id="f8e68-159">Specifies the four-character code (in this example, "WAVE") a file or stream handler can process.</span></span> |
| <span data-ttu-id="f8e68-160">{00010023-0000-0000-C000-000000000046}</span><span class="sxs-lookup"><span data-stu-id="f8e68-160">{00010023-0000-0000-C000-000000000046}</span></span> | <span data-ttu-id="f8e68-161">Указывает идентификатор интерфейса (IID) или идентификатор класса.</span><span class="sxs-lookup"><span data-stu-id="f8e68-161">Specifies an interface identifier (IID) or class identifier.</span></span>                                      |



 

<span data-ttu-id="f8e68-162">Если вы распространяете поток или обработчик файлов без приложения установки, чтобы установить его в системе пользователя, необходимо включить. REG File, чтобы пользователь мог установить обработчик.</span><span class="sxs-lookup"><span data-stu-id="f8e68-162">If you distribute your stream or file handler without a setup application to install it in the user's system, you must include a .REG file so the user can install the handler.</span></span> <span data-ttu-id="f8e68-163">Пользователь будет использовать редактор реестра для создания записей реестра для обработчика потока или файла.</span><span class="sxs-lookup"><span data-stu-id="f8e68-163">The user will use the registry editor to create registry entries for your stream or file handler.</span></span>

<span data-ttu-id="f8e68-164">В следующем примере показано содержимое типичного объекта. Файл REG.</span><span class="sxs-lookup"><span data-stu-id="f8e68-164">The following example shows the contents of a typical .REG file.</span></span> <span data-ttu-id="f8e68-165">Первая запись в следующем примере представляет собой описательную строку для обработчика.</span><span class="sxs-lookup"><span data-stu-id="f8e68-165">The first entry in the following example is the descriptive string for the handler.</span></span> <span data-ttu-id="f8e68-166">Вторая запись определяет файл, содержащий обработчик.</span><span class="sxs-lookup"><span data-stu-id="f8e68-166">The second entry identifies the file containing the handler.</span></span> <span data-ttu-id="f8e68-167">Третья запись определяет свойства обработчика файлов (в данном случае доступ к файлам только для чтения).</span><span class="sxs-lookup"><span data-stu-id="f8e68-167">The third entry identifies the properties of the file handler (in this case, read-only access to files).</span></span> <span data-ttu-id="f8e68-168">Четвертая запись связывает тип файла, обрабатываемого обработчиком (в данном случае файлы с. Расширение имени файла JPG) с идентификатором класса.</span><span class="sxs-lookup"><span data-stu-id="f8e68-168">The fourth entry associates the type of file the handler processes (in this case, files with a .JPG filename extension) with the class identifier.</span></span>


```C++
[HKEY_CLASSES_ROOT\Clsid\{5C2B8200-E2C8-1068-B1CA-6066188C6002}] 
@="JFIF (JPEG) Files" 
[HKEY_CLASSES_ROOT\Clsid\{5C2B8200-E2C8-1068-B1CA-6066188C6002}]\InprocServer32] 
@="jfiffile.dll" 
[HKEY_CLASSES_ROOT\AVIFile\Extensions\JPG] 
@="{5C2B8200-E2C8-1068-B1CA-6066188C6002}" 
 
```



<span data-ttu-id="f8e68-169">При создании этого файла сохраните его с помощью. Расширение REG для его обнаружения в качестве файла обновления для реестра.</span><span class="sxs-lookup"><span data-stu-id="f8e68-169">When creating this file, save it with a .REG extension to identify it as an update file for the registry.</span></span> <span data-ttu-id="f8e68-170">Кроме того, замените уникальный IID для 16-байтового кода, используемого в примере.</span><span class="sxs-lookup"><span data-stu-id="f8e68-170">Also, substitute a unique IID for the 16-byte code used in the example.</span></span>

 

 




