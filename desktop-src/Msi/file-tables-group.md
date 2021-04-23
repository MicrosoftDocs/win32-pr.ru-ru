---
description: Файловая группа таблиц содержит все установщик Windows таблицы, связанные с файлами.
ms.assetid: 8f56328e-ed58-41a1-94b6-266e9c117246
title: Группа таблиц файлов
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2667a1b9fe2bd9d2f8260523e2386bf7751dce8e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "105683091"
---
# <a name="file-tables-group"></a><span data-ttu-id="da2c6-103">Группа таблиц файлов</span><span class="sxs-lookup"><span data-stu-id="da2c6-103">File Tables Group</span></span>

![Группа таблиц файлов](images/filegrp.png)

<span data-ttu-id="da2c6-105">Дополнительные сведения об этой схеме см. в разделе [Условные обозначения диаграммы отношений сущностей](entity-relationship-diagram-legend.md).</span><span class="sxs-lookup"><span data-stu-id="da2c6-105">For more information about this diagram, see the [entity relationship diagram legend](entity-relationship-diagram-legend.md).</span></span>

<span data-ttu-id="da2c6-106">Разработчик пакета установщика должен рассмотреть возможность заполнения группы таблиц файлов после того, как приложение будет разбито на [компоненты и функции](components-and-features.md) и после заполнения группы " [основные таблицы](core-tables-group.md)".</span><span class="sxs-lookup"><span data-stu-id="da2c6-106">An installer package developer should consider populating the file table group of tables after breaking the application into [components and features](components-and-features.md) and after populating the [core tables group](core-tables-group.md).</span></span> <span data-ttu-id="da2c6-107">Группа таблица файлов содержит все файлы, относящиеся к установке, и большинство этих файлов перечислены в [таблице File](file-table.md).</span><span class="sxs-lookup"><span data-stu-id="da2c6-107">The file table group contains all of the files belonging to the installation and most of these files are listed in the [File table](file-table.md).</span></span> <span data-ttu-id="da2c6-108">[Таблица Directory](directory-table.md) не показана на рисунке, но тесно связана с группой файловых таблиц.</span><span class="sxs-lookup"><span data-stu-id="da2c6-108">The [Directory table](directory-table.md) is not shown in the figure but is closely related to the file table group.</span></span> <span data-ttu-id="da2c6-109">Таблица Directory предоставляет структуру каталогов установки.</span><span class="sxs-lookup"><span data-stu-id="da2c6-109">The Directory table gives the directory structure of the installation.</span></span>

<span data-ttu-id="da2c6-110">Файловая группа таблиц содержит все таблицы, связанные с файлами.</span><span class="sxs-lookup"><span data-stu-id="da2c6-110">The file group of tables contains all of the tables that are related to files.</span></span>

-   <span data-ttu-id="da2c6-111">В [таблице File](file-table.md) перечислены файлы, принадлежащие установке.</span><span class="sxs-lookup"><span data-stu-id="da2c6-111">The [File table](file-table.md) lists files belonging to the installation.</span></span> <span data-ttu-id="da2c6-112">Файлы, не перечисленные в таблице File, включают файлы дисков, которые перечислены в таблице Media.</span><span class="sxs-lookup"><span data-stu-id="da2c6-112">Files that are not listed in the File table include disk files, which are listed in Media table.</span></span> <span data-ttu-id="da2c6-113">Поскольку каждый файл принадлежит к компоненту, таблица File имеет внешний ключ в таблице Component.</span><span class="sxs-lookup"><span data-stu-id="da2c6-113">Because every file belongs to a component, the File table has an external key into the Component table.</span></span>
-   <span data-ttu-id="da2c6-114">[Таблица ремовефиле](removefile-table.md) содержит список файлов, которые будут удалены [действием ремовефилес](removefiles-action.md).</span><span class="sxs-lookup"><span data-stu-id="da2c6-114">The [RemoveFile table](removefile-table.md) contains a list of files to be removed by the [RemoveFiles action](removefiles-action.md).</span></span>
-   <span data-ttu-id="da2c6-115">В [таблице Font](font-table.md) перечислены файлы шрифтов, которые должны быть зарегистрированы в системе.</span><span class="sxs-lookup"><span data-stu-id="da2c6-115">The [Font table](font-table.md) lists font files to be registered with the system.</span></span>
-   <span data-ttu-id="da2c6-116">В [таблице селфрег](selfreg-table.md) перечислены файлы модулей, которые были зарегистрированы самостоятельно.</span><span class="sxs-lookup"><span data-stu-id="da2c6-116">The [SelfReg table](selfreg-table.md) lists module files of the installation that are self-registered.</span></span>
-   <span data-ttu-id="da2c6-117">В [таблице Media](media-table.md) перечислены исходные носители и диски, принадлежащие установке.</span><span class="sxs-lookup"><span data-stu-id="da2c6-117">The [Media table](media-table.md) lists the source media and disks belonging to the installation.</span></span>
-   <span data-ttu-id="da2c6-118">В [таблице BindImage](bindimage-table.md) перечислены файлы, привязанные к библиотекам DLL, импортированным исполняемыми файлами.</span><span class="sxs-lookup"><span data-stu-id="da2c6-118">The [BindImage table](bindimage-table.md) lists files that are bound to DLLs imported by executables.</span></span>
-   <span data-ttu-id="da2c6-119">В [таблице MoveFile](movefile-table.md) указаны файлы, которые будут перемещены во время установки.</span><span class="sxs-lookup"><span data-stu-id="da2c6-119">The [MoveFile table](movefile-table.md) specifies which files are moved during the installation.</span></span>
-   <span data-ttu-id="da2c6-120">В [таблице дупликатефиле](duplicatefile-table.md) указано, какие файлы дублируются во время установки.</span><span class="sxs-lookup"><span data-stu-id="da2c6-120">The [DuplicateFile table](duplicatefile-table.md) specifies which files are duplicated during the installation.</span></span>
-   <span data-ttu-id="da2c6-121">В [таблице инифиле](inifile-table.md) перечислены ini-файлы и сведения, которые приложение должно задать в файле.</span><span class="sxs-lookup"><span data-stu-id="da2c6-121">The [IniFile table](inifile-table.md) lists the .ini files and the information that the application needs to set in the file.</span></span>
-   <span data-ttu-id="da2c6-122">[Таблица ремовеинифиле](removeinifile-table.md) содержит сведения, которые необходимо удалить из ini-файла приложения.</span><span class="sxs-lookup"><span data-stu-id="da2c6-122">The [RemoveIniFile table](removeinifile-table.md) contains the information an application needs to delete from a .ini file.</span></span>
-   <span data-ttu-id="da2c6-123">[Таблица среда](environment-table.md) используется для задания значений переменных среды.</span><span class="sxs-lookup"><span data-stu-id="da2c6-123">The [Environment table](environment-table.md) is used to set the values of environment variables.</span></span>
-   <span data-ttu-id="da2c6-124">В [таблице значков](icon-table.md) содержатся сведения о значках, которые копируются в файл как часть объявления продукта.</span><span class="sxs-lookup"><span data-stu-id="da2c6-124">The [Icon table](icon-table.md) provides icon information which is copied to a file as a part of product advertisement.</span></span>
-   <span data-ttu-id="da2c6-125">[Таблица филесфпкаталог](filesfpcatalog-table.md) связывает указанные файлы с файлами каталога защиты системных файлов.</span><span class="sxs-lookup"><span data-stu-id="da2c6-125">The [FileSFPCatalog table](filesfpcatalog-table.md) associates specified files with system file protection catalog files.</span></span>

    <span data-ttu-id="da2c6-126">Windows **Vista, Windows Server 2003 и Windows XP:** Не поддерживается.</span><span class="sxs-lookup"><span data-stu-id="da2c6-126">**Windows Vista, Windows Server 2003 and Windows XP:** Not supported.</span></span>

-   <span data-ttu-id="da2c6-127">[Таблица сфпкаталог](sfpcatalog-table.md) содержит каталоги защиты системных файлов.</span><span class="sxs-lookup"><span data-stu-id="da2c6-127">The [SFPCatalog table](sfpcatalog-table.md) contains system file protection catalogs.</span></span>

    <span data-ttu-id="da2c6-128">Windows **Vista, Windows Server 2003 и Windows XP:** Не поддерживается.</span><span class="sxs-lookup"><span data-stu-id="da2c6-128">**Windows Vista, Windows Server 2003 and Windows XP:** Not supported.</span></span>

-   <span data-ttu-id="da2c6-129">[Таблица мсифилехаш](msifilehash-table.md) используется для хранения 128-разрядного хэша исходного файла, предоставленного пакетом установщик Windows.</span><span class="sxs-lookup"><span data-stu-id="da2c6-129">The [MsiFileHash table](msifilehash-table.md) is used to store a 128-bit hash of a source file provided by the Windows Installer package.</span></span>

 

 



