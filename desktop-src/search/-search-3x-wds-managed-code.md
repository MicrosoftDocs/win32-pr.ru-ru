---
description: Пакет SDK для Windows Search предоставляет сборку взаимодействия для работы с COM-объектами, предоставляемыми средствами поиска Windows и другими программами с интерфейсами и классами с помощью управляемого кода.
ms.assetid: 9ade6f55-de65-4f73-9d22-1be819549704
title: Использование управляемого кода с данными оболочки и Windows Search
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4e0a4c0f4182739fe553c21b45bcfc3a3af7a68f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104144188"
---
# <a name="using-managed-code-with-shell-data-and-windows-search"></a><span data-ttu-id="da5c7-103">Использование управляемого кода с данными оболочки и Windows Search</span><span class="sxs-lookup"><span data-stu-id="da5c7-103">Using Managed Code with Shell Data and Windows Search</span></span>

<span data-ttu-id="da5c7-104">Пакет SDK для Windows Search предоставляет сборку взаимодействия для работы с COM-объектами, предоставляемыми средствами поиска Windows и другими программами с интерфейсами и классами с помощью управляемого кода.</span><span class="sxs-lookup"><span data-stu-id="da5c7-104">The Windows Search SDK provides an interopability assembly for you to work with Component Object Model (COM) objects that are exposed by Windows Search and other programs against the interfaces and classes using managed code.</span></span> <span data-ttu-id="da5c7-105">Сборка взаимодействия подписана цифровой подписью корпорацией Майкрософт и может быть найдена с помощью [примеров поиска Windows](-search-samples-ovw.md).</span><span class="sxs-lookup"><span data-stu-id="da5c7-105">The interopability assembly is digitally signed by Microsoft and can be found with the [Windows Search samples](-search-samples-ovw.md).</span></span>

<span data-ttu-id="da5c7-106">Этот раздел организован следующим образом:</span><span class="sxs-lookup"><span data-stu-id="da5c7-106">This topic is organized as follows:</span></span>

-   [<span data-ttu-id="da5c7-107">Использование Windows API Кодепакк</span><span class="sxs-lookup"><span data-stu-id="da5c7-107">Using the Windows API CodePack</span></span>](#using-the-windows-api-codepack)
    -   [<span data-ttu-id="da5c7-108">Доступ к результатам индекса</span><span class="sxs-lookup"><span data-stu-id="da5c7-108">Accessing Index Results</span></span>](#accessing-index-results)
    -   [<span data-ttu-id="da5c7-109">Пример приложения, использующего API Windows Кодепакк</span><span class="sxs-lookup"><span data-stu-id="da5c7-109">Sample Application Using the Windows API Codepack</span></span>](#sample-application-using-the-windows-api-codepack)
-   [<span data-ttu-id="da5c7-110">См. также</span><span class="sxs-lookup"><span data-stu-id="da5c7-110">Related topics</span></span>](#related-topics)

## <a name="using-the-windows-api-codepack"></a><span data-ttu-id="da5c7-111">Использование Windows API Кодепакк</span><span class="sxs-lookup"><span data-stu-id="da5c7-111">Using the Windows API CodePack</span></span>

<span data-ttu-id="da5c7-112">Если вы работаете в среде Microsoft .NET, используйте [пакет кода Windows API для Microsoft .NET Framework](https://www.nuget.org/packages/Microsoft.Windows.Compatibility) , чтобы получить результаты поиска, или просто просмотрите пространство имен.</span><span class="sxs-lookup"><span data-stu-id="da5c7-112">If you are working in the Microsoft .NET environment, use the [Windows API Code Pack for Microsoft .NET Framework](https://www.nuget.org/packages/Microsoft.Windows.Compatibility) to obtain search results, or just browse the namespace.</span></span> <span data-ttu-id="da5c7-113">[Пакет кода Windows API для Microsoft .NET Framework](https://www.nuget.org/packages/Microsoft.Windows.Compatibility) предоставляет коллекцию элементов оболочки, которые, по сути, являются оболочками для собственного [интерфейса интерфейса IShellItem](/windows/win32/api/shobjidl_core/nn-shobjidl_core-ishellitem).</span><span class="sxs-lookup"><span data-stu-id="da5c7-113">The [Windows API Code Pack for Microsoft .NET Framework](https://www.nuget.org/packages/Microsoft.Windows.Compatibility) provides you with a collection of Shell items that are essentially wrappers around the native [IShellItem Interface](/windows/win32/api/shobjidl_core/nn-shobjidl_core-ishellitem).</span></span> <span data-ttu-id="da5c7-114">Можно выполнить итерацию по этой коллекции и получить различные значения свойств аналогично перечислению результатов в таблице из запроса связывания и внедрения базы данных (OLE DB).</span><span class="sxs-lookup"><span data-stu-id="da5c7-114">You can iterate over this collection and get the various property values in a fashion similar to how you would enumerate the results in a table from an Object Linking and Embedding Database (OLE DB) query.</span></span>

<span data-ttu-id="da5c7-115">В следующем фрагменте кода показано, как выполнять итерацию по элементам поиска и получать значения свойств для каждого из них.</span><span class="sxs-lookup"><span data-stu-id="da5c7-115">The following code snippet illustrates how to iterate over Search items and obtain the property values for each.</span></span>


```
foreach (ShellObject so in KnownFolders.SavedSearches)
{
    searchFolder = new ShellSearchFolder(finalSearchCondition, (ShellContainer)so);
    List<ShellObject> items = new List<ShellObject>();
    foreach (ShellObject so2 in searchFolder) items.Add(so2);   
}
```



### <a name="accessing-index-results"></a><span data-ttu-id="da5c7-116">Доступ к результатам индекса</span><span class="sxs-lookup"><span data-stu-id="da5c7-116">Accessing Index Results</span></span>

<span data-ttu-id="da5c7-117">Получить доступ к результатам индекса можно с помощью OLE DB или модели данных оболочки.</span><span class="sxs-lookup"><span data-stu-id="da5c7-117">You can access index results through either OLE DB or the Shell data model.</span></span> <span data-ttu-id="da5c7-118">Оба подхода имеют преимущества и недостатки.</span><span class="sxs-lookup"><span data-stu-id="da5c7-118">There are advantages and disadvantages with either approach.</span></span> <span data-ttu-id="da5c7-119">Одно из преимуществ заключается в том, что OLE DB и язык SQL (SQL) знакомы программистам баз данных.</span><span class="sxs-lookup"><span data-stu-id="da5c7-119">One advantage is that OLE DB and Structured Query Language (SQL) are familiar to database programmers.</span></span> <span data-ttu-id="da5c7-120">Другие преимущества — лучше контролировать производительность при запросе только индексатора и доступ к дополнительным функциям, таким как возможность поиска предыдущих результатов в новом наборе строк быстро.</span><span class="sxs-lookup"><span data-stu-id="da5c7-120">Other advantages are better control over performance when querying only the indexer, and access to additional functionality such as the ability to locate previous results in a new rowset quickly.</span></span>

<span data-ttu-id="da5c7-121">Преимущество модели данных оболочки заключается в том, что она абстрагирует по разным источникам информации, например OpenSearch, и предоставляет доступ к дополнительным функциям, таким как эскизы и обработчики свойств.</span><span class="sxs-lookup"><span data-stu-id="da5c7-121">Advantages of the Shell data model are that it abstracts across different sources of information such as OpenSearch, and provides access to additional functionality such as thumbnails and property handlers.</span></span> <span data-ttu-id="da5c7-122">Кроме того, объектная модель оболочки не требует особой поддержки для таких результатов, как элементы почты и результаты OneNote, а также для любого элемента, находящегося в индексе пользователя.</span><span class="sxs-lookup"><span data-stu-id="da5c7-122">Nor does the Shell object model require special case support for non-filename results such as mail items and OneNote results, nor for any item that resides in the user's index.</span></span> <span data-ttu-id="da5c7-123">Обратите внимание, что в Shell [кновнфолдерид](../shell/knownfolderid.md) — это область известных папок для локального индексированного содержимого.</span><span class="sxs-lookup"><span data-stu-id="da5c7-123">Note that in Shell [KNOWNFOLDERID](../shell/knownfolderid.md) is the known folder scope for local indexed content.</span></span> <span data-ttu-id="da5c7-124">Дополнительные сведения о создании источника данных оболочки см. в разделе [реализация базовых интерфейсов объекта папки](/previous-versions/windows/desktop/legacy/cc144093(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="da5c7-124">For more information on creating a Shell data source, see [Implementing the Basic Folder Object Interfaces](/previous-versions/windows/desktop/legacy/cc144093(v=vs.85)).</span></span>

<span data-ttu-id="da5c7-125">Источники данных OpenSearch не предоставляются через OLE DB для федеративного поиска в Windows 7 и более поздних версиях.</span><span class="sxs-lookup"><span data-stu-id="da5c7-125">OpenSearch data sources are not exposed through OLE DB for federated search in Windows 7 and later.</span></span> <span data-ttu-id="da5c7-126">По этой причине рекомендуется писать поставщик LINQ для пространства имен оболочки вместо того, чтобы использовать OLE DB для доступа к результатам индексатора.</span><span class="sxs-lookup"><span data-stu-id="da5c7-126">For this reason we recommend that you consider writing a LINQ provider for the Shell namespace instead of using OLE DB to access the indexer results.</span></span> <span data-ttu-id="da5c7-127">Дополнительные сведения см. в разделе [Пошаговое руководство. Создание поставщика LINQ](/previous-versions/bb546158(v=vs.140)), использующего IQueryable.</span><span class="sxs-lookup"><span data-stu-id="da5c7-127">For more information, see [Walkthrough: Creating an IQueryable LINQ Provider](/previous-versions/bb546158(v=vs.140)).</span></span>

### <a name="sample-application-using-the-windows-api-codepack"></a><span data-ttu-id="da5c7-128">Пример приложения, использующего API Windows Кодепакк</span><span class="sxs-lookup"><span data-stu-id="da5c7-128">Sample Application Using the Windows API Codepack</span></span>

<span data-ttu-id="da5c7-129">На следующем снимке экрана представлен макет примера приложения, созданного с помощью [пакета кода Windows API для Microsoft .NET Framework](https://www.nuget.org/packages/Microsoft.Windows.Compatibility).</span><span class="sxs-lookup"><span data-stu-id="da5c7-129">The following screenshot represents a mock up of a sample application created with the [Windows API Code Pack for Microsoft .NET Framework](https://www.nuget.org/packages/Microsoft.Windows.Compatibility).</span></span>

![снимок экрана приложения проигрывателя мультимедиа, отображающего сообщения электронной почты](images/folderid-searchhome.png)

## <a name="related-topics"></a><span data-ttu-id="da5c7-131">См. также</span><span class="sxs-lookup"><span data-stu-id="da5c7-131">Related topics</span></span>

<dl> <dt>

<span data-ttu-id="da5c7-132">**Зрения**</span><span class="sxs-lookup"><span data-stu-id="da5c7-132">**Conceptual**</span></span>
</dt> <dt>

[<span data-ttu-id="da5c7-133">Федеративный поиск в Windows</span><span class="sxs-lookup"><span data-stu-id="da5c7-133">Federated Search in Windows</span></span>](-search-federated-search-overview.md)
</dt> <dt>

<span data-ttu-id="da5c7-134">**Другие ресурсы**</span><span class="sxs-lookup"><span data-stu-id="da5c7-134">**Other Resources**</span></span>
</dt> <dt>

<span data-ttu-id="da5c7-135">[Взаимная совместимость кодов на разных языках](/previous-versions/dotnet/netframework-1.1/730f1wy3(v=vs.71))</span><span class="sxs-lookup"><span data-stu-id="da5c7-135">[Cross-Language Interoperability](/previous-versions/dotnet/netframework-1.1/730f1wy3(v=vs.71))</span></span>
</dt> </dl>

 

 
