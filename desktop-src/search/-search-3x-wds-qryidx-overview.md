---
description: Существует несколько способов использования службы поиска Windows для запроса индекса.
ms.assetid: 2c161b7f-4e28-4e8a-add6-3c1cda00a622
title: Отправка программных запросов к индексу
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6390b31f4a1cc01ca723978a5107d5d9a502c4ff
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "105656105"
---
# <a name="querying-the-index-programmatically"></a><span data-ttu-id="77360-103">Отправка программных запросов к индексу</span><span class="sxs-lookup"><span data-stu-id="77360-103">Querying the Index Programmatically</span></span>

<span data-ttu-id="77360-104">Существует несколько способов использования службы поиска Windows для запроса индекса.</span><span class="sxs-lookup"><span data-stu-id="77360-104">There are several ways to use Windows Search to query the index.</span></span>

<span data-ttu-id="77360-105">В этом разделе представлена концептуальная платформа для выполнения запросов к индексу программным способом.</span><span class="sxs-lookup"><span data-stu-id="77360-105">This section provides the conceptual framework for querying the index programmatically:</span></span>

-   [<span data-ttu-id="77360-106">Использование методов SQL и АКС для запроса индекса</span><span class="sxs-lookup"><span data-stu-id="77360-106">Using SQL and AQS Approaches to Query the Index</span></span>](using-sql-and-aqs-to-query-the-index.md)
-   [<span data-ttu-id="77360-107">Запрос индекса с помощью Исеарчкуерихелпер</span><span class="sxs-lookup"><span data-stu-id="77360-107">Querying the Index with ISearchQueryHelper</span></span>](-search-3x-wds-qryidx-searchqueryhelper.md)
-   [<span data-ttu-id="77360-108">Запрос индекса с помощью протокола Search-MS</span><span class="sxs-lookup"><span data-stu-id="77360-108">Querying the Index with the search-ms Protocol</span></span>](-search-3x-wds-qryidx-searchms.md)
-   [<span data-ttu-id="77360-109">Запрос к индексу с помощью синтаксиса SQL для поиска Windows</span><span class="sxs-lookup"><span data-stu-id="77360-109">Querying the Index with Windows Search SQL Syntax</span></span>](-search-sql-windowssearch-entry.md)
-   [<span data-ttu-id="77360-110">Использование расширенного синтаксиса запросов программными средствами</span><span class="sxs-lookup"><span data-stu-id="77360-110">Using Advanced Query Syntax Programmatically</span></span>](-search-3x-advancedquerysyntax.md)

> [!Note]  
> <span data-ttu-id="77360-111">Традиционная совместимость Microsoft Windows Desktop Search (WDS) 2x: на компьютерах под управлением Windows XP и более поздних версий [**исеарчдесктоп**](/previous-versions//aa965729(v=vs.85)) не рекомендуется.</span><span class="sxs-lookup"><span data-stu-id="77360-111">Legacy Microsoft Windows Desktop Search (WDS) 2x compatibility: On computers running Windows XP and later, [**ISearchDesktop**](/previous-versions//aa965729(v=vs.85)) is deprecated.</span></span> <span data-ttu-id="77360-112">Вместо этого разработчики должны использовать [**исеарчкуерихелпер**](/windows/win32/api/Searchapi/nn-searchapi-isearchqueryhelper) для получения строки подключения и анализа запроса пользователя в язык SQL (SQL), а затем выполнять запросы через связывание объектов и внедрение базы данных (OLE DB).</span><span class="sxs-lookup"><span data-stu-id="77360-112">Instead, developers should use [**ISearchQueryHelper**](/windows/win32/api/Searchapi/nn-searchapi-isearchqueryhelper) to get a connection string and to parse the user's query into Structured Query Language (SQL), and then query through Object Linking and Embedding Database (OLE DB).</span></span>

 

## <a name="additional-resources"></a><span data-ttu-id="77360-113">Дополнительные ресурсы</span><span class="sxs-lookup"><span data-stu-id="77360-113">Additional Resources</span></span>

-   <span data-ttu-id="77360-114">Дополнительные сведения о OLE DB см. в разделе [Общие сведения о программировании OLE DB](https://msdn.microsoft.com/library/Cc522830(v=VS.71).aspx).</span><span class="sxs-lookup"><span data-stu-id="77360-114">For information on OLE DB, see [OLE DB Programming Overview](https://msdn.microsoft.com/library/Cc522830(v=VS.71).aspx).</span></span> <span data-ttu-id="77360-115">Сведения о поставщике данных платформа .NET Framework для OLE DB см. в разделе [пространство имен System. Data. OLEDB](/dotnet/api/system.data.oledb?view=dotnet-plat-ext-3.1).</span><span class="sxs-lookup"><span data-stu-id="77360-115">For information on the .NET Framework Data Provider for OLE DB, see the [System.Data.OleDb Namespace](/dotnet/api/system.data.oledb?view=dotnet-plat-ext-3.1).</span></span>
-   <span data-ttu-id="77360-116">Дополнительные сведения об использовании свойств в запросах см. в следующих разделах:</span><span class="sxs-lookup"><span data-stu-id="77360-116">For additional background on using properties in querying, see the following topics:</span></span>
    -   [<span data-ttu-id="77360-117">Система свойств</span><span class="sxs-lookup"><span data-stu-id="77360-117">Property System</span></span>](../properties/building-property-handlers.md)
    -   <span data-ttu-id="77360-118">[Свойства системы](https://msdn.microsoft.com/library/bb763010(VS.85).aspx)</span><span class="sxs-lookup"><span data-stu-id="77360-118">[System Properties](https://msdn.microsoft.com/library/bb763010(VS.85).aspx)</span></span>
-   <span data-ttu-id="77360-119">Сведения о создании и изменении папок поиска см. в разделе [**интерфейс исеарчфолдеритемфактори**](/windows/win32/api/shobjidl_core/nn-shobjidl_core-isearchfolderitemfactory).</span><span class="sxs-lookup"><span data-stu-id="77360-119">For information on how to create and modify search folders, see [**ISearchFolderItemFactory Interface**](/windows/win32/api/shobjidl_core/nn-shobjidl_core-isearchfolderitemfactory).</span></span>
-   <span data-ttu-id="77360-120">Сведения о поддерживаемых сообществом досках сообщений и обсуждениях по технологиям поиска см. на [форуме MSDN: Разработка Windows Desktop Search](https://social.msdn.microsoft.com/Forums/windowsdesktopsearchdevelopment/threads).</span><span class="sxs-lookup"><span data-stu-id="77360-120">For community-supported question and discussion message boards on Search technologies, see [MSDN Forum: Windows Desktop Search Development](https://social.msdn.microsoft.com/Forums/windowsdesktopsearchdevelopment/threads).</span></span>
-   <span data-ttu-id="77360-121">Чтобы скачать примеры кода пакета SDK для поиска, выполните следующие действия.</span><span class="sxs-lookup"><span data-stu-id="77360-121">To download the Search SDK Code Samples:</span></span>
    -   <span data-ttu-id="77360-122">Для Windows 7: [примеры поиска Windows на GitHub](https://github.com/Microsoft/Windows-classic-samples/tree/master/Samples/Win7Samples/winui/WindowsSearch)</span><span class="sxs-lookup"><span data-stu-id="77360-122">For Windows 7: [Windows Search Samples on GitHub](https://github.com/Microsoft/Windows-classic-samples/tree/master/Samples/Win7Samples/winui/WindowsSearch)</span></span>
    -   <span data-ttu-id="77360-123">Для Windows Vista: [примеры пакета SDK для Windows Search](https://www.microsoft.com/downloads/details.aspx?FamilyID=645300AE-5E7A-4CE7-95F0-49793F8F76E8)</span><span class="sxs-lookup"><span data-stu-id="77360-123">For Windows Vista: [Windows Search SDK Samples](https://www.microsoft.com/downloads/details.aspx?FamilyID=645300AE-5E7A-4CE7-95F0-49793F8F76E8)</span></span>
-   <span data-ttu-id="77360-124">Чтобы скачать Windows SDK, выполните следующие действия.</span><span class="sxs-lookup"><span data-stu-id="77360-124">To download the Windows SDK:</span></span>
    -   <span data-ttu-id="77360-125">Для Windows 7: [Windows SDK для Windows 7 и платформа .NET Framework](https://msdn.microsoft.com/windowsvista/bb980924.aspx)</span><span class="sxs-lookup"><span data-stu-id="77360-125">For Windows 7: [Windows SDK for Windows 7 and .NET Framework](https://msdn.microsoft.com/windowsvista/bb980924.aspx)</span></span>
    -   <span data-ttu-id="77360-126">Для Windows Vista: [Windows SDK для Windows Vista и платформа .NET Framework](https://www.microsoft.com/download/details.aspx?id=31950)</span><span class="sxs-lookup"><span data-stu-id="77360-126">For Windows Vista: [Windows SDK for Windows Vista and .NET Framework](https://www.microsoft.com/download/details.aspx?id=31950)</span></span>

## <a name="related-topics"></a><span data-ttu-id="77360-127">См. также</span><span class="sxs-lookup"><span data-stu-id="77360-127">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="77360-128">Руководством по разработке для поиска Windows</span><span class="sxs-lookup"><span data-stu-id="77360-128">Windows Search Development Guide</span></span>](-search-developers-guide-entry-page.md)
</dt> <dt>

[<span data-ttu-id="77360-129">Управление индексом</span><span class="sxs-lookup"><span data-stu-id="77360-129">Managing the Index</span></span>](-search-3x-wds-mngidx-overview.md)
</dt> <dt>

[<span data-ttu-id="77360-130">Расширение индекса поиска Windows</span><span class="sxs-lookup"><span data-stu-id="77360-130">Extending the Windows Search Index</span></span>](-search-3x-wds-extidx-overview.md)
</dt> <dt>

[<span data-ttu-id="77360-131">Расширение языковых ресурсов</span><span class="sxs-lookup"><span data-stu-id="77360-131">Extending Language Resources</span></span>](extending-language-resources-in-windows-search.md)
</dt> </dl>

 

 
