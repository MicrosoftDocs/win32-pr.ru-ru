---
description: Сведения об управлении индексом Windows Search с помощью диспетчера поиска, диспетчера каталогов и диспетчера области обхода содержимого.
ms.assetid: 345d1159-aa51-4a01-9831-216075a8fb78
title: Управление индексом
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7cd59fc804b4a7c3802a921462e0579c0640bbca
ms.sourcegitcommit: b32433cc0394159c7263809ae67615ab5792d40d
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/30/2021
ms.locfileid: "113120169"
---
# <a name="managing-the-index"></a><span data-ttu-id="33cb5-103">Управление индексом</span><span class="sxs-lookup"><span data-stu-id="33cb5-103">Managing the Index</span></span>

<span data-ttu-id="33cb5-104">Поиск Windows позволяет управлять индексом Windows Search с помощью трех основных компонентов: Диспетчер поиска, диспетчер каталогов и Диспетчер области обхода содержимого.</span><span class="sxs-lookup"><span data-stu-id="33cb5-104">Windows Search enables you to manage the Windows Search index with three main components: Search Manager, Catalog Manager, and Crawl Scope Manager.</span></span>

<span data-ttu-id="33cb5-105">Этот раздел организован следующим образом:</span><span class="sxs-lookup"><span data-stu-id="33cb5-105">This section is organized as follows:</span></span>

- [<span data-ttu-id="33cb5-106">Интерфейсы для управления индексом</span><span class="sxs-lookup"><span data-stu-id="33cb5-106">Interfaces for Managing the Index</span></span>](interfaces-for-managing-the-index.md)
- [<span data-ttu-id="33cb5-107">Использование диспетчера поиска</span><span class="sxs-lookup"><span data-stu-id="33cb5-107">Using the Search Manager</span></span>](-search-3x-wds-mngidx-searchmanager.md)
- [<span data-ttu-id="33cb5-108">Использование диспетчера каталогов</span><span class="sxs-lookup"><span data-stu-id="33cb5-108">Using the Catalog Manager</span></span>](-search-3x-wds-mngidx-catalog-manager.md)
- [<span data-ttu-id="33cb5-109">Использование диспетчера области сканирования</span><span class="sxs-lookup"><span data-stu-id="33cb5-109">Using the Crawl Scope Manager</span></span>](-search-3x-wds-extidx-csm.md)

## <a name="additional-resources"></a><span data-ttu-id="33cb5-110">Дополнительные ресурсы</span><span class="sxs-lookup"><span data-stu-id="33cb5-110">Additional Resources</span></span>

- <span data-ttu-id="33cb5-111">Сведения о поддерживаемых сообществом досках сообщений и обсуждениях по технологиям поиска см. на [форуме MSDN: Разработка Windows Desktop Search](https://social.msdn.microsoft.com/Forums/windowsdesktopsearchdevelopment/threads).</span><span class="sxs-lookup"><span data-stu-id="33cb5-111">For community-supported question and discussion message boards on Search technologies, see [MSDN Forum: Windows Desktop Search Development](https://social.msdn.microsoft.com/Forums/windowsdesktopsearchdevelopment/threads).</span></span>
- <span data-ttu-id="33cb5-112">Чтобы скачать примеры кода пакета SDK для поиска, выполните следующие действия.</span><span class="sxs-lookup"><span data-stu-id="33cb5-112">To download the Search SDK Code Samples:</span></span>
  - [<span data-ttu-id="33cb5-113">Примеры для поиска Windows в коллекции кода</span><span class="sxs-lookup"><span data-stu-id="33cb5-113">Windows Search Samples on Code Gallery</span></span>](./-search-samples-ovw.md)
- <span data-ttu-id="33cb5-114">Чтобы скачать Windows SDK, выполните следующие действия.</span><span class="sxs-lookup"><span data-stu-id="33cb5-114">To download the Windows SDK:</span></span>
  - <span data-ttu-id="33cb5-115">Для Windows 10: [пакет SDK для Windows 10](https://developer.microsoft.com/windows/downloads/windows-10-sdk)</span><span class="sxs-lookup"><span data-stu-id="33cb5-115">For Windows 10: [Windows 10 SDK](https://developer.microsoft.com/windows/downloads/windows-10-sdk)</span></span>
  - <span data-ttu-id="33cb5-116">Для Windows 7: [Windows SDK для Windows 7 и платформа .NET Framework](https://msdn.microsoft.com/windowsvista/bb980924.aspx)</span><span class="sxs-lookup"><span data-stu-id="33cb5-116">For Windows 7: [Windows SDK for Windows 7 and .NET Framework](https://msdn.microsoft.com/windowsvista/bb980924.aspx)</span></span>
  - <span data-ttu-id="33cb5-117">Для Windows Vista: [Windows SDK для Windows Vista и платформа .NET Framework](https://www.microsoft.com/download/details.aspx?id=31950)</span><span class="sxs-lookup"><span data-stu-id="33cb5-117">For Windows Vista: [Windows SDK for Windows Vista and .NET Framework](https://www.microsoft.com/download/details.aspx?id=31950)</span></span>

## <a name="related-topics"></a><span data-ttu-id="33cb5-118">Связанные темы</span><span class="sxs-lookup"><span data-stu-id="33cb5-118">Related topics</span></span>

[<span data-ttu-id="33cb5-119">Руководством по разработке для поиска Windows</span><span class="sxs-lookup"><span data-stu-id="33cb5-119">Windows Search Development Guide</span></span>](-search-developers-guide-entry-page.md)

[<span data-ttu-id="33cb5-120">Отправка программных запросов к индексу</span><span class="sxs-lookup"><span data-stu-id="33cb5-120">Querying the Index Programmatically</span></span>](-search-3x-wds-qryidx-overview.md)

[<span data-ttu-id="33cb5-121">Расширение индекса</span><span class="sxs-lookup"><span data-stu-id="33cb5-121">Extending the Index</span></span>](-search-3x-wds-extidx-overview.md)

[<span data-ttu-id="33cb5-122">Расширение языковых ресурсов</span><span class="sxs-lookup"><span data-stu-id="33cb5-122">Extending Language Resources</span></span>](extending-language-resources-in-windows-search.md)
