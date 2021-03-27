---
description: В следующем примере гипотетическая компания разработки программного обеспечения под названием Litware, Inc.
ms.assetid: e4392907-a84f-40ea-aa88-2ad0510bca3c
title: Пример сопоставления файлов
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7f4104c9bc241fed4bc698bd150b03d32a70e054
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104143078"
---
# <a name="file-association-example"></a><span data-ttu-id="04c5e-103">Пример сопоставления файлов</span><span class="sxs-lookup"><span data-stu-id="04c5e-103">File Association Example</span></span>

<span data-ttu-id="04c5e-104">В следующем примере гипотетическая компания разработки программного обеспечения под названием Litware, Inc. создает новый звуковой проигрыватель с именем Литвареплайер.</span><span class="sxs-lookup"><span data-stu-id="04c5e-104">In the following example, a hypothetical software development company called Litware, Inc. creates a new audio player called LitwarePlayer.</span></span> <span data-ttu-id="04c5e-105">Litware хочет разработать сопоставление файлов между Литвареплайер и его первичным типом файлов, который использует недавно разработанный звуковой формат, позволяющий хранить весь аудио компакт-диск менее чем на 10 килобайтах памяти без потери качества.</span><span class="sxs-lookup"><span data-stu-id="04c5e-105">Litware wants to design a file association between LitwarePlayer and its primary file type, which uses a newly developed audio format that enables an entire audio CD to be stored in less than 10 kilobytes of memory with no loss of quality.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="04c5e-106">Этот раздел не относится к Windows 10.</span><span class="sxs-lookup"><span data-stu-id="04c5e-106">This topic does not apply for Windows 10.</span></span> <span data-ttu-id="04c5e-107">Способ изменения связей файлов по умолчанию в Windows 10.</span><span class="sxs-lookup"><span data-stu-id="04c5e-107">The way that default file associations work changed in Windows 10.</span></span> <span data-ttu-id="04c5e-108">Дополнительные сведения см. в разделе об **изменениях в статье обработка приложений по умолчанию** в [этой записи](https://blogs.windows.com/bloggingwindows/2015/05/20/announcing-windows-10-insider-preview-build-10122-for-pcs/)в Windows 10.</span><span class="sxs-lookup"><span data-stu-id="04c5e-108">For more information, see the section on **Changes to how Windows 10 handles default apps** in [this post](https://blogs.windows.com/bloggingwindows/2015/05/20/announcing-windows-10-insider-preview-build-10122-for-pcs/).</span></span>

 

## <a name="designing-a-new-file-association"></a><span data-ttu-id="04c5e-109">Проектирование нового сопоставления файлов</span><span class="sxs-lookup"><span data-stu-id="04c5e-109">Designing a New File Association</span></span>

<span data-ttu-id="04c5e-110">Компания должна выполнить следующие действия.</span><span class="sxs-lookup"><span data-stu-id="04c5e-110">The company should take the following steps.</span></span>

1.  <span data-ttu-id="04c5e-111">**Определите, следует ли обрабатывать новый тип файлов как открытый или частный.**</span><span class="sxs-lookup"><span data-stu-id="04c5e-111">**Decide if the new file type should be treated as public or private.**</span></span> <span data-ttu-id="04c5e-112">Этот новый тип файла является типом носителя.</span><span class="sxs-lookup"><span data-stu-id="04c5e-112">This new file type is a media type.</span></span> <span data-ttu-id="04c5e-113">Так как пользователи обмениваются файлами мультимедиа на различных платформах и могут иметь другие приложения, которым необходимо считывать формат Литвареплайер, наиболее подходящим является [общедоступный](fa-file-types.md) тип файлов.</span><span class="sxs-lookup"><span data-stu-id="04c5e-113">Because users exchange media files across various platforms and there might be other applications that need to read the LitwarePlayer format, a [public](fa-file-types.md) file type is the most appropriate.</span></span>
2.  <span data-ttu-id="04c5e-114">**Определите, был ли уже определен этот тип файла.**</span><span class="sxs-lookup"><span data-stu-id="04c5e-114">**Determine whether this file type is already defined.**</span></span> <span data-ttu-id="04c5e-115">Проверьте базу данных MIME (IANA), а также другие общедоступные базы данных типа файлов в Интернете, чтобы определить, что сравниваемый тип файлов не определен.</span><span class="sxs-lookup"><span data-stu-id="04c5e-115">Check the Internet Assigned Numbers Authority (IANA) MIME database, and other public file type databases on the Internet to determine that no comparable file type has been defined.</span></span> <span data-ttu-id="04c5e-116">Так как это новый формат файла, необходимо определить новый тип файлов.</span><span class="sxs-lookup"><span data-stu-id="04c5e-116">Because this is a new file format, you need to define a new file type.</span></span>
3.  <span data-ttu-id="04c5e-117">**Определите расширение имени файла для нового типа файлов.**</span><span class="sxs-lookup"><span data-stu-id="04c5e-117">**Define a file name extension for the new file type.**</span></span> <span data-ttu-id="04c5e-118">Разработчики выбирают объект `.opa-ltw-audio` , который включает в себя аббревиатуру поставщика, и подсказку о том, что содержит файл.</span><span class="sxs-lookup"><span data-stu-id="04c5e-118">The developers choose the `.opa-ltw-audio`, which incorporates their vendor abbreviation and a hint about the what the file contains.</span></span> <span data-ttu-id="04c5e-119">Исследование определяет, что расширение не используется другими пользователями.</span><span class="sxs-lookup"><span data-stu-id="04c5e-119">Research determines that the extension is not being used by anyone else.</span></span> <span data-ttu-id="04c5e-120">В соответствии с текущими рекомендациями короткое расширение не определено.</span><span class="sxs-lookup"><span data-stu-id="04c5e-120">Following current recommendations, no short extension is defined.</span></span>
4.  <span data-ttu-id="04c5e-121">**Определите тип MIME для типа файла и зарегистрируйте его с помощью IANA.**</span><span class="sxs-lookup"><span data-stu-id="04c5e-121">**Define a MIME type for the file type and register it with the IANA.**</span></span> <span data-ttu-id="04c5e-122">Litware определяет новый тип MIME как *Audio/литвареплайер. 1* и подготавливает приложение типа MIME, следуя рекомендациям, изложенным в документе RFC (запросы на комментарии) 2045, 2046, 2047 и 2048.</span><span class="sxs-lookup"><span data-stu-id="04c5e-122">Litware defines the new MIME type as *audio/LitwarePlayer.1* and prepares a MIME type application, following the guidelines laid out in Request for Comments (RFC) numbers 2045, 2046, 2047, and 2048.</span></span> <span data-ttu-id="04c5e-123">Затем они отправляют приложение в IANA, который добавляет новый тип файлов в базу данных зарегистрированных типов MIME.</span><span class="sxs-lookup"><span data-stu-id="04c5e-123">They then submit the application to the IANA, which adds the new file type to the database of registered MIME types.</span></span>
5.  <span data-ttu-id="04c5e-124">**Определите, существует ли идентификатор ProgID для типа файла.**</span><span class="sxs-lookup"><span data-stu-id="04c5e-124">**Determine whether a ProgID exists for the file type.**</span></span> <span data-ttu-id="04c5e-125">Так как это новый тип файла, для него не существует [ProgID](fa-progids.md) .</span><span class="sxs-lookup"><span data-stu-id="04c5e-125">Because this is a new file type, no [ProgID](fa-progids.md) exists for it.</span></span> <span data-ttu-id="04c5e-126">Litware задает создание нового идентификатора ProgID для Литвареплайер.</span><span class="sxs-lookup"><span data-stu-id="04c5e-126">Litware sets about designing a new ProgID for LitwarePlayer.</span></span> <span data-ttu-id="04c5e-127">Они решают использовать понятное имя "Литвареплайер Audio Player" (которое хранится в виде ресурса в файле LitwarePlayer.exe) и разрабатывает значок по умолчанию для файлов, связанных с Литвареплайер (также хранимых в LitwarePlayer.exe).</span><span class="sxs-lookup"><span data-stu-id="04c5e-127">They decide on the friendly name "LitwarePlayer Audio Player" (which is stored as a resource in the LitwarePlayer.exe file), and they design a default icon to use for files associated with LitwarePlayer (also stored in LitwarePlayer.exe).</span></span> <span data-ttu-id="04c5e-128">Так как Литвареплайер — это новое приложение, это идентификатор ProgID версии 1.</span><span class="sxs-lookup"><span data-stu-id="04c5e-128">Because LitwarePlayer is a new application, this is a version 1 ProgID.</span></span>
6.  <span data-ttu-id="04c5e-129">**Зарегистрируйте идентификатор ProgID.**</span><span class="sxs-lookup"><span data-stu-id="04c5e-129">**Register the ProgID.**</span></span> <span data-ttu-id="04c5e-130">При установке Литвареплайер программа установки создает в реестре следующую запись [ProgID](fa-progids.md) .</span><span class="sxs-lookup"><span data-stu-id="04c5e-130">When LitwarePlayer is installed, the installation program creates the following [ProgID](fa-progids.md) entry in the registry.</span></span>

    ```
    HKEY_CLASSES_ROOT
       Litware.LitwarePlayer.1
          (Default) = LitwarePlayer Audio Player
          FriendlyTypeName = @LitwarePlayer, -120
          CurVer
             (Default) = Litware.LitwarePlayer.1
          DefaultIcon
             (Default) = LitwarePlayer, -142
          shell
             play
                command
                   (Default) = "%ProgramFiles%\LitwarePlayer\LitwarePlayer.exe" "%1"
    ```

    <span data-ttu-id="04c5e-131">В командном ключе %1 передается в качестве пути к файлу для воспроизведения.</span><span class="sxs-lookup"><span data-stu-id="04c5e-131">In the command key, %1 is passed as the path to the file to play.</span></span>

7.  <span data-ttu-id="04c5e-132">**Зарегистрируйте расширение имени файла для типа файла.**</span><span class="sxs-lookup"><span data-stu-id="04c5e-132">**Register the file name extension for the file type.**</span></span> <span data-ttu-id="04c5e-133">При установке Литвареплайер программа установки создает в реестре следующие записи для пользовательского расширения типа файла.</span><span class="sxs-lookup"><span data-stu-id="04c5e-133">When LitwarePlayer is installed, the installation program creates the following entries in the registry for its custom file type extension.</span></span>

    ```
    HKEY_CLASSES_ROOT
       .opa-vwi-audio
          (Default) = Litware.LitwarePlayer.1
          PerceivedType = Audio
          Content Type = audio/LitwarePlayer
    ```

> [!Note]  
> <span data-ttu-id="04c5e-134">При каждом создании или изменении сопоставления файлов уведомите систему о том, что изменение было выполнено путем вызова [**шчанженотифи**](/windows/desktop/api/shlobj_core/nf-shlobj_core-shchangenotify), указав \_ событие ассокчанжед шкне.</span><span class="sxs-lookup"><span data-stu-id="04c5e-134">Whenever a file association is created or changed, notify the system that a change has been made by calling [**SHChangeNotify**](/windows/desktop/api/shlobj_core/nf-shlobj_core-shchangenotify), specifying the SHCNE\_ASSOCCHANGED event.</span></span> <span data-ttu-id="04c5e-135">Если это не сделано, оболочка может не распознать изменения, внесенные до перезагрузки системы.</span><span class="sxs-lookup"><span data-stu-id="04c5e-135">If this is not done, the Shell might not recognize any changes made until the system restarts.</span></span>

 

## <a name="additional-resources"></a><span data-ttu-id="04c5e-136">Дополнительные ресурсы</span><span class="sxs-lookup"><span data-stu-id="04c5e-136">Additional Resources</span></span>

-   [<span data-ttu-id="04c5e-137">Общие сведения о сопоставлении файлов</span><span class="sxs-lookup"><span data-stu-id="04c5e-137">Introduction to File Associations</span></span>](fa-intro.md)
-   [<span data-ttu-id="04c5e-138">Как зарегистрировать Интернет браузер или почтовый клиент в меню "Пуск" Windows</span><span class="sxs-lookup"><span data-stu-id="04c5e-138">How to Register an Internet Browser or Email Client With the Windows Start Menu</span></span>](start-menu-reg.md)
-   <span data-ttu-id="04c5e-139">[Регистрация приложения в схеме URI](/previous-versions/windows/internet-explorer/ie-developer/platform-apis/aa767914(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="04c5e-139">[Registering an Application to a URI Scheme](/previous-versions/windows/internet-explorer/ie-developer/platform-apis/aa767914(v=vs.85))</span></span>

## <a name="related-topics"></a><span data-ttu-id="04c5e-140">См. также</span><span class="sxs-lookup"><span data-stu-id="04c5e-140">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="04c5e-141">Рекомендации по сопоставлению файлов</span><span class="sxs-lookup"><span data-stu-id="04c5e-141">Best Practices for File Associations</span></span>](fa-best-practices.md)
</dt> <dt>

[<span data-ttu-id="04c5e-142">Рекомендации по управлению приложениями по умолчанию в Windows Vista и более поздних версиях</span><span class="sxs-lookup"><span data-stu-id="04c5e-142">Guidelines for Managing Default Applications in Windows Vista and Later</span></span>](vista-managing-defaults.md)
</dt> <dt>

[<span data-ttu-id="04c5e-143">Программы по умолчанию</span><span class="sxs-lookup"><span data-stu-id="04c5e-143">Default Programs</span></span>](default-programs.md)
</dt> <dt>

[<span data-ttu-id="04c5e-144">Настройка доступа к программе и параметров по умолчанию для компьютера (SPAD)</span><span class="sxs-lookup"><span data-stu-id="04c5e-144">Set Program Access and Computer Defaults (SPAD)</span></span>](cpl-setprogramaccess.md)
</dt> </dl>

 

 
