---
description: Группа "таблицы локаторов" используется для поиска файлов и приложений.
ms.assetid: 44ab770b-1a7f-4590-9681-8f6bd343bf86
title: Группа "таблицы указателей"
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 300a869a912c06b2112476f50bcda021833cfbe7
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "105683728"
---
# <a name="locator-tables-group"></a><span data-ttu-id="eb263-103">Группа "таблицы указателей"</span><span class="sxs-lookup"><span data-stu-id="eb263-103">Locator Tables Group</span></span>

<span data-ttu-id="eb263-104">Группа "таблицы локаторов" используется для поиска файлов и приложений.</span><span class="sxs-lookup"><span data-stu-id="eb263-104">The Locator Tables group is used to locate files and applications.</span></span> <span data-ttu-id="eb263-105">Чтобы найти файл, сначала определите подпись файла, а затем найдите файл.</span><span class="sxs-lookup"><span data-stu-id="eb263-105">To search for a file, first determine the file signature and then locate the file.</span></span> <span data-ttu-id="eb263-106">Таблицы локатора используются для поиска уникальной сигнатуры файла в реестре, данных конфигурации установщика, дереве каталогов или в ini-файлах.</span><span class="sxs-lookup"><span data-stu-id="eb263-106">The Locator tables are used to search the registry, installer configuration data, directory tree, or .ini files for the unique signature of a file.</span></span> <span data-ttu-id="eb263-107">Подпись файла можно затем проверить в [таблице сигнатур](signature-table.md) , чтобы убедиться, что конкретный файл фактически является искомым файлом, а не другим файлом с тем же именем.</span><span class="sxs-lookup"><span data-stu-id="eb263-107">The file signature can then be checked in the [Signature table](signature-table.md) to ascertain that a particular file is really the file being sought and not another file with the same name.</span></span> <span data-ttu-id="eb263-108">Если запись в таблице локатора не содержит ключ в таблицу сигнатур, то запись ссылается на каталог, а не на файл.</span><span class="sxs-lookup"><span data-stu-id="eb263-108">If a record in a locator table does not contain a key into the Signature table, then the record refers to a directory and not a file.</span></span>

<span data-ttu-id="eb263-109">Компонент, управляющий файлом, находится в [таблице File](file-table.md) через внешний ключ к [таблице Component](component-table.md).</span><span class="sxs-lookup"><span data-stu-id="eb263-109">The component controlling a file is found in the [File table](file-table.md) through the external key to the [Component table](component-table.md).</span></span> <span data-ttu-id="eb263-110">Установщик разрешает расположение файла с помощью таблицы Component, так как каждый файл принадлежит одному компоненту.</span><span class="sxs-lookup"><span data-stu-id="eb263-110">The installer resolves the location of a file through the Component table because every file belongs to one component.</span></span> <span data-ttu-id="eb263-111">Расположение компонента можно найти по внешнему ключу в таблице Component в [таблице Directory](directory-table.md).</span><span class="sxs-lookup"><span data-stu-id="eb263-111">The location of a component is found through an external key in the Component table to the [Directory table](directory-table.md).</span></span>

<span data-ttu-id="eb263-112">Расположение приложения можно найти, выполнив поиск файлов, составляющих приложение.</span><span class="sxs-lookup"><span data-stu-id="eb263-112">The location of an application is found by searching for files that make up the application.</span></span> <span data-ttu-id="eb263-113">Установщик также предоставляет две таблицы для поиска предыдущих версий приложения: [таблицу аппсеарч](appsearch-table.md) и [таблицу ккпсеарч](ccpsearch-table.md).</span><span class="sxs-lookup"><span data-stu-id="eb263-113">The installer also provides two tables for searching for previous versions of an application: the [AppSearch table](appsearch-table.md) and the [CCPSearch table](ccpsearch-table.md).</span></span>

<span data-ttu-id="eb263-114">Следующие таблицы составляют группу «таблицы локаторов» и используются для определения подписи файла.</span><span class="sxs-lookup"><span data-stu-id="eb263-114">The following tables make up the Locator tables group and are used to determine the file signature.</span></span>

-   <span data-ttu-id="eb263-115">[Таблица реглокатор](reglocator-table.md) содержит сведения, необходимые для поиска файла или каталога в реестре.</span><span class="sxs-lookup"><span data-stu-id="eb263-115">The [RegLocator table](reglocator-table.md) holds the information needed to search for a file or directory in the registry.</span></span>
-   <span data-ttu-id="eb263-116">[Таблица инилокатор](inilocator-table.md) содержит сведения, необходимые для поиска ini-файла.</span><span class="sxs-lookup"><span data-stu-id="eb263-116">The [IniLocator table](inilocator-table.md) holds the information needed to search for a .ini file.</span></span> <span data-ttu-id="eb263-117">INI-файл должен присутствовать в каталоге Microsoft Windows по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="eb263-117">The .ini file must be present in the default Microsoft Windows directory.</span></span>
-   <span data-ttu-id="eb263-118">[Таблица комплокатор](complocator-table.md) содержит сведения, необходимые для поиска файла или каталога с помощью данных конфигурации установщика.</span><span class="sxs-lookup"><span data-stu-id="eb263-118">The [CompLocator table](complocator-table.md) holds the information needed to search for a file or a directory using the installer's configuration data.</span></span>
-   <span data-ttu-id="eb263-119">[Таблица дрлокатор](drlocator-table.md) содержит сведения, необходимые для поиска файла или каталога в дереве каталогов.</span><span class="sxs-lookup"><span data-stu-id="eb263-119">The [DrLocator table](drlocator-table.md) holds the information needed to search for a file or directory in the directory tree.</span></span>
-   <span data-ttu-id="eb263-120">[Таблица аппсеарч](appsearch-table.md) содержит свойства, которые должны быть установлены в результате поиска соответствующей сигнатуры файла.</span><span class="sxs-lookup"><span data-stu-id="eb263-120">The [AppSearch table](appsearch-table.md) contains the properties that must be set to the search result of a corresponding file signature.</span></span>
-   <span data-ttu-id="eb263-121">[Таблица ккпсеарч](ccpsearch-table.md) содержит список подписей файлов, по крайней мере один из которых должен присутствовать на компьютере пользователя для программы проверки соответствия (CCP).</span><span class="sxs-lookup"><span data-stu-id="eb263-121">The [CCPSearch table](ccpsearch-table.md) contains the list of file signatures, at least one of which needs to be present on a user's computer for the Compliance Checking Program (CCP).</span></span>

 

 



