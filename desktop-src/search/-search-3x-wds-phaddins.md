---
description: В этом разделе приводятся общие сведения, необходимые для реализации, расширения и тестирования обработчиков протоколов.
ms.assetid: c76d5c82-d62b-4dd4-9743-9572be61e2be
title: Разработка обработчиков протоколов для поиска Windows
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6e56c237dd4876ae05bcd7b983c4da2708f299a4
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "103808969"
---
# <a name="developing-protocol-handlers-for-windows-search"></a><span data-ttu-id="f2eaf-103">Разработка обработчиков протоколов для поиска Windows</span><span class="sxs-lookup"><span data-stu-id="f2eaf-103">Developing Protocol Handlers for Windows Search</span></span>

<span data-ttu-id="f2eaf-104">В этом разделе приводятся общие сведения, необходимые для реализации, расширения и тестирования обработчиков протоколов.</span><span class="sxs-lookup"><span data-stu-id="f2eaf-104">This section provides conceptual information necessary for the implementation, extension and testing of protocol handlers.</span></span>

-   [<span data-ttu-id="f2eaf-105">Основные сведения о обработчиках протоколов</span><span class="sxs-lookup"><span data-stu-id="f2eaf-105">Understanding Protocol Handlers</span></span>](-search-3x-wds-extidx-prot-implementing.md)
-   [<span data-ttu-id="f2eaf-106">Уведомление индекса изменений</span><span class="sxs-lookup"><span data-stu-id="f2eaf-106">Notifying the Index of Changes</span></span>](-search-3x-wds-notifyingofchanges.md)
-   [<span data-ttu-id="f2eaf-107">Добавление значков и контекстных меню</span><span class="sxs-lookup"><span data-stu-id="f2eaf-107">Adding Icons and Context Menus</span></span>](-search-3x-wds-ph-ui-extensions.md)
-   [<span data-ttu-id="f2eaf-108">Пример кода: расширения оболочки для обработчиков протоколов</span><span class="sxs-lookup"><span data-stu-id="f2eaf-108">Code Sample: Shell Extensions for Protocol Handlers</span></span>](-search-3x-wds-ph-ui-samplecode.md)
-   [<span data-ttu-id="f2eaf-109">Установка и регистрация обработчиков протоколов</span><span class="sxs-lookup"><span data-stu-id="f2eaf-109">Installing and Registering Protocol Handlers</span></span>](-search-3x-wds-ph-install-registration.md)
-   [<span data-ttu-id="f2eaf-110">Создание соединителя поиска для обработчика протокола</span><span class="sxs-lookup"><span data-stu-id="f2eaf-110">Creating a Search Connector for a Protocol Handler</span></span>](-search-3x-wds-ph-search-connector.md)
-   [<span data-ttu-id="f2eaf-111">Обработчики протокола отладки</span><span class="sxs-lookup"><span data-stu-id="f2eaf-111">Debugging Protocol Handlers</span></span>](-search-ws-protocolhandlertesting.md)

## <a name="additional-resources"></a><span data-ttu-id="f2eaf-112">Дополнительные ресурсы</span><span class="sxs-lookup"><span data-stu-id="f2eaf-112">Additional Resources</span></span>

<span data-ttu-id="f2eaf-113">Общие сведения об индексировании см. в следующих разделах:</span><span class="sxs-lookup"><span data-stu-id="f2eaf-113">For conceptual background on indexing, see the following topics:</span></span>

-   <span data-ttu-id="f2eaf-114">Общие сведения о процессе индексирования см. [в разделе процесс индексирования](-search-indexing-process-overview.md).</span><span class="sxs-lookup"><span data-stu-id="f2eaf-114">For an overview of the indexing process, see [The Indexing Process](-search-indexing-process-overview.md).</span></span>
-   <span data-ttu-id="f2eaf-115">Сведения о расширении поиска Windows для индексирования содержимого и свойств новых форматов файлов и хранилищ данных см. в разделе [расширение индекса](-search-3x-wds-extidx-overview.md).</span><span class="sxs-lookup"><span data-stu-id="f2eaf-115">To extend Windows Search to index the contents and properties of new file formats and data stores, see [Extending the Index](-search-3x-wds-extidx-overview.md).</span></span>
-   <span data-ttu-id="f2eaf-116">Обзоры диспетчера каталога и диспетчера поиска в каталоге (CSM) см. в разделе [Использование диспетчера каталогов](-search-3x-wds-mngidx-catalog-manager.md) и [диспетчера области сканирования](-search-3x-wds-extidx-csm.md).</span><span class="sxs-lookup"><span data-stu-id="f2eaf-116">For overviews of the Catalog Manager and Catalog Search Manager (CSM), see [Using the Catalog Manager](-search-3x-wds-mngidx-catalog-manager.md) and [Using the Crawl Scope Manager](-search-3x-wds-extidx-csm.md).</span></span>

<span data-ttu-id="f2eaf-117">Основные сведения о типах файлов и обработчиках см. в следующих разделах:</span><span class="sxs-lookup"><span data-stu-id="f2eaf-117">For conceptual background on file types and handlers, see the following topics:</span></span>

-   <span data-ttu-id="f2eaf-118">Сведения о расширении оболочки с помощью обработчиков типов файлов см. в разделе [Создание обработчиков расширений оболочки](../shell/handlers.md).</span><span class="sxs-lookup"><span data-stu-id="f2eaf-118">To extend the Shell with file type handlers, see [Creating Shell Extension Handlers](../shell/handlers.md).</span></span>
-   <span data-ttu-id="f2eaf-119">Основные сведения о обработчиках фильтров см. в разделе [Разработка обработчиков фильтров](-search-ifilter-conceptual.md).</span><span class="sxs-lookup"><span data-stu-id="f2eaf-119">For conceptual information on filter handlers, see [Developing Filter Handlers](-search-ifilter-conceptual.md).</span></span>
-   <span data-ttu-id="f2eaf-120">Сведения о создании обработчиков см. [в статьях введение в сопоставления файлов](../shell/fa-intro.md), [Регистрация расширений оболочки](../shell/reg-shell-exts.md), [Создание обработчиков расширений оболочки](../shell/handlers.md), [контекстное меню](/previous-versions/windows/desktop/legacy/cc144169(v=vs.85))и [обработчики просмотра](../shell/preview-handlers.md).</span><span class="sxs-lookup"><span data-stu-id="f2eaf-120">For information about creating handlers, see [Introduction to File Associations](../shell/fa-intro.md), [Registering Shell Extensions](../shell/reg-shell-exts.md), [Creating Shell Extension Handlers](../shell/handlers.md), [Context Menu](/previous-versions/windows/desktop/legacy/cc144169(v=vs.85)), and [Preview Handlers](../shell/preview-handlers.md).</span></span>

<span data-ttu-id="f2eaf-121">Дополнительные сведения о связанных технологиях и реализации хранилища данных см. в следующих разделах:</span><span class="sxs-lookup"><span data-stu-id="f2eaf-121">For background on related technologies and on implementing a data store, see the following topics:</span></span>

-   <span data-ttu-id="f2eaf-122">Обработчики протоколов поиска Windows используют спецификации проектирования, аналогичные SharePoint Server, и часто взаимозаменяемы.</span><span class="sxs-lookup"><span data-stu-id="f2eaf-122">Windows Search protocol handlers use design specifications similar to SharePoint Server, and they can often be used interchangeably.</span></span> <span data-ttu-id="f2eaf-123">Дополнительные сведения см. в разделе [Центр разработчиков SharePoint Server](https://developer.microsoft.com/office/docs).</span><span class="sxs-lookup"><span data-stu-id="f2eaf-123">For more information, see [SharePoint Server Developer Center](https://developer.microsoft.com/office/docs).</span></span>
-   <span data-ttu-id="f2eaf-124">В Windows 7 и более поздних версиях SharePoint Search Server 2008 и MOSS 2007 с пакетом обновления 2 (SP2) также поддерживают федеративный поиск.</span><span class="sxs-lookup"><span data-stu-id="f2eaf-124">In Windows 7 and later, SharePoint Search Server 2008 and MOSS 2007 SP2 also support federated search.</span></span> <span data-ttu-id="f2eaf-125">Дополнительные сведения об федеративного поиска и развертывании Search Server 2008 с помощью Office SharePoint Server 2007 см. в разделе [федеративный поисковый \[ сервер search Server 2008 \] ](/previous-versions/office/bb931109(v=office.14)).</span><span class="sxs-lookup"><span data-stu-id="f2eaf-125">For more information about federated search and Search Server 2008 deployment with Office SharePoint Server 2007, see [Federated Search \[Search Server 2008\]](/previous-versions/office/bb931109(v=office.14)).</span></span>
-   <span data-ttu-id="f2eaf-126">Сведения о создании хранилища данных оболочки см. в разделе [реализация базовых интерфейсов объекта папки](/previous-versions/windows/desktop/legacy/cc144093(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="f2eaf-126">To create a Shell data store, see [Implementing the Basic Folder Object Interfaces](/previous-versions/windows/desktop/legacy/cc144093(v=vs.85)).</span></span>

<span data-ttu-id="f2eaf-127">Примеры кода см. на следующих страницах портала:</span><span class="sxs-lookup"><span data-stu-id="f2eaf-127">For code samples, see the following portal pages:</span></span>

-   <span data-ttu-id="f2eaf-128">Примеры кода поиска см. в разделе [примеры пакета SDK для Windows Search](https://www.microsoft.com/downloads/details.aspx?FamilyID=645300AE-5E7A-4CE7-95F0-49793F8F76E8).</span><span class="sxs-lookup"><span data-stu-id="f2eaf-128">For Search code samples, see [Windows Search SDK Samples](https://www.microsoft.com/downloads/details.aspx?FamilyID=645300AE-5E7A-4CE7-95F0-49793F8F76E8).</span></span>
-   <span data-ttu-id="f2eaf-129">Примеры кода оболочки см. в разделе [примеры пакетов SDK](/previous-versions/windows/desktop/legacy/dd940376(v=vs.85))для оболочки.</span><span class="sxs-lookup"><span data-stu-id="f2eaf-129">For Shell code samples, see [Shell SDK Samples](/previous-versions/windows/desktop/legacy/dd940376(v=vs.85)).</span></span>

 

 
