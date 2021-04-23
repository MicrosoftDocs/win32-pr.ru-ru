---
description: Инфраструктура совместимости использует базу данных для обнаружения проблем совместимости приложений и их решений.
ms.assetid: 3b35b758-18ca-40dd-8882-35d9b458264c
title: База данных совместимости приложений
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4ba33ab3a8de702f2e620b7607f4d2b6904e6165
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "103807126"
---
# <a name="application-compatibility-database"></a><span data-ttu-id="1363c-103">База данных совместимости приложений</span><span class="sxs-lookup"><span data-stu-id="1363c-103">Application Compatibility Database</span></span>

<span data-ttu-id="1363c-104">Инфраструктура совместимости использует базу данных для обнаружения проблем совместимости приложений и их решений.</span><span class="sxs-lookup"><span data-stu-id="1363c-104">The compatibility infrastructure uses a database to identify application compatibility issues and their solutions.</span></span> <span data-ttu-id="1363c-105">Эта база данных является индексированным двоичным файлом с расширением SDB.</span><span class="sxs-lookup"><span data-stu-id="1363c-105">This database is an indexed binary file with an .sdb extension.</span></span> <span data-ttu-id="1363c-106">Инфраструктура совместимости предоставляет программный интерфейс для доступа к базе данных.</span><span class="sxs-lookup"><span data-stu-id="1363c-106">The compatibility infrastructure provides a programming interface to access the database.</span></span>

<span data-ttu-id="1363c-107">Проблемы совместимости могут быть устранены в зависимости от приложения во время выполнения.</span><span class="sxs-lookup"><span data-stu-id="1363c-107">Compatibility issues can be addressed on an application-by-application basis at run time.</span></span> <span data-ttu-id="1363c-108">Каждое приложение, указанное в базе данных, содержит один или несколько компонентов, которым требуется решение.</span><span class="sxs-lookup"><span data-stu-id="1363c-108">Each application specified in the database contains one or more components that need a solution.</span></span> <span data-ttu-id="1363c-109">Компоненты — это исполняемые файлы, которые обычно описываются с помощью атрибутов файлов (например, CHECKSUM).</span><span class="sxs-lookup"><span data-stu-id="1363c-109">Components are executable files that are generally described using their file attributes (for example, checksum).</span></span>

<span data-ttu-id="1363c-110">Процесс поиска по базе данных и определения решений для каждого приложения называется *сопоставлением*.</span><span class="sxs-lookup"><span data-stu-id="1363c-110">The process of database lookup and determining the solutions for each application is called *matching*.</span></span> <span data-ttu-id="1363c-111">Для создания уникального совпадения можно использовать атрибуты файла и наличие связанных файлов в папке или подпапке, содержащей EXE-файл.</span><span class="sxs-lookup"><span data-stu-id="1363c-111">The file attributes and the presence of associated files in the folder or subfolder containing the .exe file can be used to create a unique match.</span></span> <span data-ttu-id="1363c-112">Связанные файлы называются *соответствующими файлами*.</span><span class="sxs-lookup"><span data-stu-id="1363c-112">The associated files are called *matching files*.</span></span>

<span data-ttu-id="1363c-113">*Тег* — это уникальный идентификатор для записей и атрибутов в базе данных.</span><span class="sxs-lookup"><span data-stu-id="1363c-113">A *TAG* is a unique identifier for the entries and attributes in the database.</span></span> <span data-ttu-id="1363c-114">*Тип тега* указывает формат данных, связанных с [**тегом**](tag.md).</span><span class="sxs-lookup"><span data-stu-id="1363c-114">The *TAG type* indicates the format of the data associated with the [**TAG**](tag.md).</span></span> <span data-ttu-id="1363c-115">Например, **\_ имя тега** имеет тип **Tag \_ тип \_ стрингреф**; данные для **\_ имени тега** являются строкой имени.</span><span class="sxs-lookup"><span data-stu-id="1363c-115">For example, **TAG\_NAME** is of type **TAG\_TYPE\_STRINGREF**; the data for **TAG\_NAME** is a name string.</span></span> <span data-ttu-id="1363c-116">*TAGID* — это указатель на запись в определенной базе данных.</span><span class="sxs-lookup"><span data-stu-id="1363c-116">A *TAGID* is a pointer to an entry in a particular database.</span></span> <span data-ttu-id="1363c-117">*Тагреф* — это указатель на запись, которую можно использовать в нескольких базах данных.</span><span class="sxs-lookup"><span data-stu-id="1363c-117">A *TAGREF* is a pointer to an entry that can be used across multiple databases.</span></span>

<span data-ttu-id="1363c-118">*Атрибуты файлов* — это метаданные, связанные с файлом на диске.</span><span class="sxs-lookup"><span data-stu-id="1363c-118">*File attributes* are metadata associated with a file on disk.</span></span> <span data-ttu-id="1363c-119">Эти атрибуты включают имя файла, размер файла, контрольную сумму, версию и дату.</span><span class="sxs-lookup"><span data-stu-id="1363c-119">These attributes include the file name, file size, checksum, version, and date.</span></span> <span data-ttu-id="1363c-120">Эти атрибуты используются для определения того, совпадает ли файл, загружаемый системой, с записью базы данных.</span><span class="sxs-lookup"><span data-stu-id="1363c-120">These attributes are used to determine whether a file being loaded by the system matches a database entry.</span></span> <span data-ttu-id="1363c-121">Таким образом, эти атрибуты файлов также называются *соответствующими атрибутами*.</span><span class="sxs-lookup"><span data-stu-id="1363c-121">Therefore, these file attributes are also called *matching attributes*.</span></span>

## <a name="solutions"></a><span data-ttu-id="1363c-122">Решения</span><span class="sxs-lookup"><span data-stu-id="1363c-122">Solutions</span></span>

<span data-ttu-id="1363c-123">Наиболее распространенными решениями, применяемыми к компонентам приложения, являются AppHelp и Аппфикс.</span><span class="sxs-lookup"><span data-stu-id="1363c-123">The most common solutions applied to the components of an application are Apphelp and Appfix.</span></span>

<span data-ttu-id="1363c-124">При использовании AppHelp отображается настраиваемое уведомление о локализованном сообщении, обычно при установке или запуске приложения.</span><span class="sxs-lookup"><span data-stu-id="1363c-124">With Apphelp, a custom localized message notification is displayed, typically when the application is installed or started.</span></span> <span data-ttu-id="1363c-125">Он содержит краткий текст, объясняющий проблемы совместимости и позволяющий продолжить выполнение приложения.</span><span class="sxs-lookup"><span data-stu-id="1363c-125">It contains brief text that explains the compatibility issue and provides the option to continue running the application.</span></span> <span data-ttu-id="1363c-126">Однако выполнение некоторых приложений может завершиться неудачно. AppHelp не предоставит пользователю возможность продолжить выполнение этих приложений.</span><span class="sxs-lookup"><span data-stu-id="1363c-126">However, some applications will fail dramatically is allowed to run; Apphelp will not give the user the option to continue running these applications.</span></span>

<span data-ttu-id="1363c-127">При использовании Аппфикс для API-интерфейсов, вызванных компонентами приложения, устанавливаются обработчики.</span><span class="sxs-lookup"><span data-stu-id="1363c-127">With Appfix, hooks are installed for APIs called by the components of the application.</span></span> <span data-ttu-id="1363c-128">Эти обработчики указывают на функции-заглушки, которые могут вызываться вместо системных функций (также известных как *оболочек совместимости небольшого*).</span><span class="sxs-lookup"><span data-stu-id="1363c-128">These hooks point to stub functions that can be called instead of the system functions (also known as *shimming*).</span></span> <span data-ttu-id="1363c-129">Функции-заглушки выполняют операции, необходимые, чтобы приложение было запущено в установленной версии Windows.</span><span class="sxs-lookup"><span data-stu-id="1363c-129">The stub functions perform operations needed to enable the application to run on the installed version of Windows.</span></span> <span data-ttu-id="1363c-130">Каждая функция-заглушка может при необходимости вызвать системную функцию после завершения ее работы.</span><span class="sxs-lookup"><span data-stu-id="1363c-130">Each stub function may optionally call the system function after completing its work.</span></span> <span data-ttu-id="1363c-131">*Уровень совместимости* или *режим* содержит один или несколько оболочек совместимости и флагов.</span><span class="sxs-lookup"><span data-stu-id="1363c-131">A *compatibility layer* or *mode* contains one or more shims and flags.</span></span>

## <a name="in-this-section"></a><span data-ttu-id="1363c-132">Содержание раздела</span><span class="sxs-lookup"><span data-stu-id="1363c-132">In this section</span></span>

-   [<span data-ttu-id="1363c-133">**\_данные APPHELP**</span><span class="sxs-lookup"><span data-stu-id="1363c-133">**APPHELP\_DATA**</span></span>](apphelp-data.md)
-   [<span data-ttu-id="1363c-134">**аттринфо**</span><span class="sxs-lookup"><span data-stu-id="1363c-134">**ATTRINFO**</span></span>](attrinfo.md)
-   [<span data-ttu-id="1363c-135">**басефлушаппкомпаткаче**</span><span class="sxs-lookup"><span data-stu-id="1363c-135">**BaseFlushAppcompatCache**</span></span>](baseflushappcompatcache.md)
-   [<span data-ttu-id="1363c-136">**НАЙТИ \_ сведения**</span><span class="sxs-lookup"><span data-stu-id="1363c-136">**FIND\_INFO**</span></span>](find-info.md)
-   [<span data-ttu-id="1363c-137">**индексид**</span><span class="sxs-lookup"><span data-stu-id="1363c-137">**INDEXID**</span></span>](indexid.md)
-   [<span data-ttu-id="1363c-138">**\_тип пути**</span><span class="sxs-lookup"><span data-stu-id="1363c-138">**PATH\_TYPE**</span></span>](path-type.md)
-   [<span data-ttu-id="1363c-139">**сдббегинврителисттаг**</span><span class="sxs-lookup"><span data-stu-id="1363c-139">**SdbBeginWriteListTag**</span></span>](sdbbeginwritelisttag.md)
-   [<span data-ttu-id="1363c-140">**сдбклоседатабасе**</span><span class="sxs-lookup"><span data-stu-id="1363c-140">**SdbCloseDatabase**</span></span>](sdbclosedatabase.md)
-   [<span data-ttu-id="1363c-141">**сдбклоседатабасеврите**</span><span class="sxs-lookup"><span data-stu-id="1363c-141">**SdbCloseDatabaseWrite**</span></span>](sdbclosedatabasewrite.md)
-   [<span data-ttu-id="1363c-142">**сдбкоммитиндексес**</span><span class="sxs-lookup"><span data-stu-id="1363c-142">**SdbCommitIndexes**</span></span>](sdbcommitindexes.md)
-   [<span data-ttu-id="1363c-143">**сдбкреатедатабасе**</span><span class="sxs-lookup"><span data-stu-id="1363c-143">**SdbCreateDatabase**</span></span>](sdbcreatedatabase.md)
-   [<span data-ttu-id="1363c-144">**сдбдеклареиндекс**</span><span class="sxs-lookup"><span data-stu-id="1363c-144">**SdbDeclareIndex**</span></span>](sdbdeclareindex.md)
-   [<span data-ttu-id="1363c-145">**сдбендврителисттаг**</span><span class="sxs-lookup"><span data-stu-id="1363c-145">**SdbEndWriteListTag**</span></span>](sdbendwritelisttag.md)
-   [<span data-ttu-id="1363c-146">**сдбфиндфирстдвординдекседтаг**</span><span class="sxs-lookup"><span data-stu-id="1363c-146">**SdbFindFirstDWORDIndexedTag**</span></span>](sdbfindfirstdwordindexedtag.md)
-   [<span data-ttu-id="1363c-147">**сдбфиндфирсттаг**</span><span class="sxs-lookup"><span data-stu-id="1363c-147">**SdbFindFirstTag**</span></span>](sdbfindfirsttag.md)
-   [<span data-ttu-id="1363c-148">**сдбфинднексттаг**</span><span class="sxs-lookup"><span data-stu-id="1363c-148">**SdbFindNextTag**</span></span>](sdbfindnexttag.md)
-   [<span data-ttu-id="1363c-149">**сдбформататтрибуте**</span><span class="sxs-lookup"><span data-stu-id="1363c-149">**SdbFormatAttribute**</span></span>](sdbformatattribute.md)
-   [<span data-ttu-id="1363c-150">**сдбфрифилеаттрибутес**</span><span class="sxs-lookup"><span data-stu-id="1363c-150">**SdbFreeFileAttributes**</span></span>](sdbfreefileattributes.md)
-   [<span data-ttu-id="1363c-151">**сдбжетапппатчдир**</span><span class="sxs-lookup"><span data-stu-id="1363c-151">**SdbGetAppPatchDir**</span></span>](sdbgetapppatchdir.md)
-   [<span data-ttu-id="1363c-152">**сдбжетбинаритагдата**</span><span class="sxs-lookup"><span data-stu-id="1363c-152">**SdbGetBinaryTagData**</span></span>](sdbgetbinarytagdata.md)
-   [<span data-ttu-id="1363c-153">**сдбжетфилеаттрибутес**</span><span class="sxs-lookup"><span data-stu-id="1363c-153">**SdbGetFileAttributes**</span></span>](sdbgetfileattributes.md)
-   [<span data-ttu-id="1363c-154">**сдбжетфирстчилд**</span><span class="sxs-lookup"><span data-stu-id="1363c-154">**SdbGetFirstChild**</span></span>](sdbgetfirstchild.md)
-   [<span data-ttu-id="1363c-155">**сдбжетиндекс**</span><span class="sxs-lookup"><span data-stu-id="1363c-155">**SdbGetIndex**</span></span>](sdbgetindex.md)
-   [<span data-ttu-id="1363c-156">**сдбжетматчинжексе**</span><span class="sxs-lookup"><span data-stu-id="1363c-156">**SdbGetMatchingExe**</span></span>](sdbgetmatchingexe.md)
-   [<span data-ttu-id="1363c-157">**сдбжетнекстчилд**</span><span class="sxs-lookup"><span data-stu-id="1363c-157">**SdbGetNextChild**</span></span>](sdbgetnextchild.md)
-   [<span data-ttu-id="1363c-158">**сдбжетстрингтагптр**</span><span class="sxs-lookup"><span data-stu-id="1363c-158">**SdbGetStringTagPtr**</span></span>](sdbgetstringtagptr.md)
-   [<span data-ttu-id="1363c-159">**сдбжеттагфромтагид**</span><span class="sxs-lookup"><span data-stu-id="1363c-159">**SdbGetTagFromTagID**</span></span>](sdbgettagfromtagid.md)
-   [<span data-ttu-id="1363c-160">**сдбинитдатабасе**</span><span class="sxs-lookup"><span data-stu-id="1363c-160">**SdbInitDatabase**</span></span>](sdbinitdatabase.md)
-   [<span data-ttu-id="1363c-161">**сдбисстандарддатабасе**</span><span class="sxs-lookup"><span data-stu-id="1363c-161">**SdbIsStandardDatabase**</span></span>](sdbisstandarddatabase.md)
-   [<span data-ttu-id="1363c-162">**сдбмакеиндекскэйфромстринг**</span><span class="sxs-lookup"><span data-stu-id="1363c-162">**SdbMakeIndexKeyFromString**</span></span>](sdbmakeindexkeyfromstring.md)
-   [<span data-ttu-id="1363c-163">**сдбопенапфелпдетаилсдатабасе**</span><span class="sxs-lookup"><span data-stu-id="1363c-163">**SdbOpenApphelpDetailsDatabase**</span></span>](sdbopenapphelpdetailsdatabase.md)
-   [<span data-ttu-id="1363c-164">**сдбопенапфелпресаурцефиле**</span><span class="sxs-lookup"><span data-stu-id="1363c-164">**SdbOpenApphelpResourceFile**</span></span>](sdbopenapphelpresourcefile.md)
-   [<span data-ttu-id="1363c-165">**сдбопендатабасе**</span><span class="sxs-lookup"><span data-stu-id="1363c-165">**SdbOpenDatabase**</span></span>](sdbopendatabase.md)
-   [<span data-ttu-id="1363c-166">**сдбкуеридатаекстагид**</span><span class="sxs-lookup"><span data-stu-id="1363c-166">**SdbQueryDataExTagID**</span></span>](sdbquerydataextagid.md)
-   [<span data-ttu-id="1363c-167">**сдбкуериресулт**</span><span class="sxs-lookup"><span data-stu-id="1363c-167">**SDBQUERYRESULT**</span></span>](sdbqueryresult.md)
-   [<span data-ttu-id="1363c-168">**сдбреадапфелпдетаилсдата**</span><span class="sxs-lookup"><span data-stu-id="1363c-168">**SdbReadApphelpDetailsData**</span></span>](sdbreadapphelpdetailsdata.md)
-   [<span data-ttu-id="1363c-169">**сдбреадбинаритаг**</span><span class="sxs-lookup"><span data-stu-id="1363c-169">**SdbReadBinaryTag**</span></span>](sdbreadbinarytag.md)
-   [<span data-ttu-id="1363c-170">**сдбреаддвордтаг**</span><span class="sxs-lookup"><span data-stu-id="1363c-170">**SdbReadDWORDTag**</span></span>](sdbreaddwordtag.md)
-   [<span data-ttu-id="1363c-171">**сдбреадквордтаг**</span><span class="sxs-lookup"><span data-stu-id="1363c-171">**SdbReadQWORDTag**</span></span>](sdbreadqwordtag.md)
-   [<span data-ttu-id="1363c-172">**сдбреадстрингтаг**</span><span class="sxs-lookup"><span data-stu-id="1363c-172">**SdbReadStringTag**</span></span>](sdbreadstringtag.md)
-   [<span data-ttu-id="1363c-173">**сдбрегистердатабасикс**</span><span class="sxs-lookup"><span data-stu-id="1363c-173">**SdbRegisterDatabaseEx**</span></span>](sdbregisterdatabaseex.md)
-   [<span data-ttu-id="1363c-174">**сдбрелеаседатабасе**</span><span class="sxs-lookup"><span data-stu-id="1363c-174">**SdbReleaseDatabase**</span></span>](sdbreleasedatabase.md)
-   [<span data-ttu-id="1363c-175">**сдбрелеасематчинжексе**</span><span class="sxs-lookup"><span data-stu-id="1363c-175">**SdbReleaseMatchingExe**</span></span>](sdbreleasematchingexe.md)
-   [<span data-ttu-id="1363c-176">**сдбстартиндексинг**</span><span class="sxs-lookup"><span data-stu-id="1363c-176">**SdbStartIndexing**</span></span>](sdbstartindexing.md)
-   [<span data-ttu-id="1363c-177">**сдбстопиндексинг**</span><span class="sxs-lookup"><span data-stu-id="1363c-177">**SdbStopIndexing**</span></span>](sdbstopindexing.md)
-   [<span data-ttu-id="1363c-178">**сдбтагрефтотагид**</span><span class="sxs-lookup"><span data-stu-id="1363c-178">**SdbTagRefToTagID**</span></span>](sdbtagreftotagid.md)
-   [<span data-ttu-id="1363c-179">**сдбтагтостринг**</span><span class="sxs-lookup"><span data-stu-id="1363c-179">**SdbTagToString**</span></span>](sdbtagtostring.md)
-   [<span data-ttu-id="1363c-180">**сдбунрегистердатабасе**</span><span class="sxs-lookup"><span data-stu-id="1363c-180">**SdbUnregisterDatabase**</span></span>](sdbunregisterdatabase.md)
-   [<span data-ttu-id="1363c-181">**сдбвритебинаритаг**</span><span class="sxs-lookup"><span data-stu-id="1363c-181">**SdbWriteBinaryTag**</span></span>](sdbwritebinarytag.md)
-   [<span data-ttu-id="1363c-182">**сдбвритебинаритагфромфиле**</span><span class="sxs-lookup"><span data-stu-id="1363c-182">**SdbWriteBinaryTagFromFile**</span></span>](sdbwritebinarytagfromfile.md)
-   [<span data-ttu-id="1363c-183">**сдбвритедвордтаг**</span><span class="sxs-lookup"><span data-stu-id="1363c-183">**SdbWriteDWORDTag**</span></span>](sdbwritedwordtag.md)
-   [<span data-ttu-id="1363c-184">**сдбвритенуллтаг**</span><span class="sxs-lookup"><span data-stu-id="1363c-184">**SdbWriteNULLTag**</span></span>](sdbwritenulltag.md)
-   [<span data-ttu-id="1363c-185">**сдбвритеквордтаг**</span><span class="sxs-lookup"><span data-stu-id="1363c-185">**SdbWriteQWORDTag**</span></span>](sdbwriteqwordtag.md)
-   [<span data-ttu-id="1363c-186">**сдбвритестрингтаг**</span><span class="sxs-lookup"><span data-stu-id="1363c-186">**SdbWriteStringTag**</span></span>](sdbwritestringtag.md)
-   [<span data-ttu-id="1363c-187">**сдбвритевордтаг**</span><span class="sxs-lookup"><span data-stu-id="1363c-187">**SdbWriteWORDTag**</span></span>](sdbwritewordtag.md)
-   [<span data-ttu-id="1363c-188">**Типы баз данных оболочек совместимости**</span><span class="sxs-lookup"><span data-stu-id="1363c-188">**Shim Database Types**</span></span>](shim-database-types.md)
-   [<span data-ttu-id="1363c-189">**шимфлушкаче**</span><span class="sxs-lookup"><span data-stu-id="1363c-189">**ShimFlushCache**</span></span>](shimflushcache.md)
-   [<span data-ttu-id="1363c-190">**ТЕГАМИ**</span><span class="sxs-lookup"><span data-stu-id="1363c-190">**TAG**</span></span>](tag.md)
-   [<span data-ttu-id="1363c-191">**Типы тегов**</span><span class="sxs-lookup"><span data-stu-id="1363c-191">**TAG Types**</span></span>](tag-types.md)
-   [<span data-ttu-id="1363c-192">**TAGID**</span><span class="sxs-lookup"><span data-stu-id="1363c-192">**TAGID**</span></span>](tagid.md)
-   [<span data-ttu-id="1363c-193">**тагреф**</span><span class="sxs-lookup"><span data-stu-id="1363c-193">**TAGREF**</span></span>](tagref.md)

 

 



