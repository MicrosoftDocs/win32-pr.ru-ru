---
description: Сторонние лица могут создавать приложения, которые запрашивают в индексе данные программным способом и могут расширять возможности поиска Windows для индексирования данных из пользовательских форматов файлов и хранилищ данных.
ms.assetid: 70046df0-ce48-472d-b24b-8231ea3a43c0
title: Руководством разработчика Windows Search
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 61593f47e081059966936a99a7d2baea114df92a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104497085"
---
# <a name="windows-search-developers-guide"></a><span data-ttu-id="0b927-103">Руководством разработчика Windows Search</span><span class="sxs-lookup"><span data-stu-id="0b927-103">Windows Search Developer's Guide</span></span>

<span data-ttu-id="0b927-104">Сторонние лица могут создавать приложения, которые запрашивают в индексе данные программным способом и могут расширять возможности поиска Windows для индексирования данных из пользовательских форматов файлов и хранилищ данных.</span><span class="sxs-lookup"><span data-stu-id="0b927-104">Third parties can create applications that query the index for data programmatically and can extend Windows Search to index data from custom file formats and data stores.</span></span> <span data-ttu-id="0b927-105">Для создания приложений Windows Search сторонние разработчики должны сначала реализовать хранилище данных оболочки, чтобы добиться разумного взаимодействия с пользователем.</span><span class="sxs-lookup"><span data-stu-id="0b927-105">To create Windows Search applications, third-party developers must first implement a Shell data store to a achieve a reasonable user experience.</span></span> <span data-ttu-id="0b927-106">Дополнительные сведения см. [в разделе Реализация базовых интерфейсов объекта папки](/previous-versions/windows/desktop/legacy/cc144093(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="0b927-106">For more information, see [Implementing the Basic Folder Object Interfaces](/previous-versions/windows/desktop/legacy/cc144093(v=vs.85)).</span></span>

<span data-ttu-id="0b927-107">Кроме того, необходимо загрузить [Windows SDK](https://msdn.microsoft.com/windowsvista/bb980924.aspx) для библиотек поиска Windows.</span><span class="sxs-lookup"><span data-stu-id="0b927-107">You must also download the [Windows SDK](https://msdn.microsoft.com/windowsvista/bb980924.aspx) for the Windows Search libraries.</span></span> <span data-ttu-id="0b927-108">[Примеры пакета SDK для Windows Search](https://www.microsoft.com/downloads/details.aspx?FamilyID=645300AE-5E7A-4CE7-95F0-49793F8F76E8) содержат полезные примеры кода и сборку взаимодействия для разработки с управляемым кодом.</span><span class="sxs-lookup"><span data-stu-id="0b927-108">The [Windows Search SDK Samples](https://www.microsoft.com/downloads/details.aspx?FamilyID=645300AE-5E7A-4CE7-95F0-49793F8F76E8) contains useful code samples and an interopability assembly for developing with managed code.</span></span> <span data-ttu-id="0b927-109">Дополнительные сведения об использовании примеров кода см. в статье [примеры кода для поиска Windows](-search-3x-wds-sampleentry.md).</span><span class="sxs-lookup"><span data-stu-id="0b927-109">For more information on using the code samples, see [Windows Search Code Samples](-search-3x-wds-sampleentry.md).</span></span>

<span data-ttu-id="0b927-110">Этот раздел организован следующим образом:</span><span class="sxs-lookup"><span data-stu-id="0b927-110">This section is organized as follows:</span></span>

- [<span data-ttu-id="0b927-111">Управление индексом</span><span class="sxs-lookup"><span data-stu-id="0b927-111">Managing the Index</span></span>](-search-3x-wds-mngidx-overview.md)
- [<span data-ttu-id="0b927-112">Отправка программных запросов к индексу</span><span class="sxs-lookup"><span data-stu-id="0b927-112">Querying the Index Programmatically</span></span>](-search-3x-wds-qryidx-overview.md)
- [<span data-ttu-id="0b927-113">Расширение индекса</span><span class="sxs-lookup"><span data-stu-id="0b927-113">Extending the Index</span></span>](-search-3x-wds-extidx-overview.md)
- [<span data-ttu-id="0b927-114">Расширение языковых ресурсов</span><span class="sxs-lookup"><span data-stu-id="0b927-114">Extending Language Resources</span></span>](extending-language-resources-in-windows-search.md)

## <a name="additional-resources"></a><span data-ttu-id="0b927-115">Дополнительные ресурсы</span><span class="sxs-lookup"><span data-stu-id="0b927-115">Additional Resources</span></span>

- <span data-ttu-id="0b927-116">Сведения о поддерживаемых сообществом досках сообщений и обсуждениях по технологиям поиска см. на [форуме MSDN: Разработка Windows Desktop Search](https://social.msdn.microsoft.com/Forums/windowsdesktopsearchdevelopment/threads).</span><span class="sxs-lookup"><span data-stu-id="0b927-116">For community-supported question and discussion message boards on Search technologies, see [MSDN Forum: Windows Desktop Search Development](https://social.msdn.microsoft.com/Forums/windowsdesktopsearchdevelopment/threads).</span></span>
- <span data-ttu-id="0b927-117">Чтобы скачать примеры кода поиска, выполните следующие действия.</span><span class="sxs-lookup"><span data-stu-id="0b927-117">To download the Search Code Samples:</span></span>
  - [<span data-ttu-id="0b927-118">Примеры поиска Windows</span><span class="sxs-lookup"><span data-stu-id="0b927-118">Windows Search Samples</span></span>](-search-samples-ovw.md)
- <span data-ttu-id="0b927-119">Чтобы скачать Windows SDK, выполните следующие действия.</span><span class="sxs-lookup"><span data-stu-id="0b927-119">To download the Windows SDK:</span></span>
  - <span data-ttu-id="0b927-120">Для Windows 10: [пакет SDK для Windows 10](https://developer.microsoft.com/windows/downloads/windows-10-sdk)</span><span class="sxs-lookup"><span data-stu-id="0b927-120">For Windows 10: [Windows 10 SDK](https://developer.microsoft.com/windows/downloads/windows-10-sdk)</span></span>
  - <span data-ttu-id="0b927-121">Для Windows 7: [Windows SDK для Windows 7 и платформа .NET Framework](https://msdn.microsoft.com/windowsvista/bb980924.aspx)</span><span class="sxs-lookup"><span data-stu-id="0b927-121">For Windows 7: [Windows SDK for Windows 7 and .NET Framework](https://msdn.microsoft.com/windowsvista/bb980924.aspx)</span></span>

## <a name="related-topics"></a><span data-ttu-id="0b927-122">См. также</span><span class="sxs-lookup"><span data-stu-id="0b927-122">Related topics</span></span>

[<span data-ttu-id="0b927-123">Обзор Windows Search</span><span class="sxs-lookup"><span data-stu-id="0b927-123">Windows Search Overview</span></span>](-search-3x-wds-overview.md)

[<span data-ttu-id="0b927-124">Справочник по поиску Windows</span><span class="sxs-lookup"><span data-stu-id="0b927-124">Windows Search Reference</span></span>](-search-reference-entry-page.md)

[<span data-ttu-id="0b927-125">Примеры кода для поиска Windows</span><span class="sxs-lookup"><span data-stu-id="0b927-125">Windows Search Code Samples</span></span>](-search-samples-ovw.md)

[<span data-ttu-id="0b927-126">Федеративный поиск в Windows</span><span class="sxs-lookup"><span data-stu-id="0b927-126">Federated Search in Windows</span></span>](-search-federated-search-overview.md)

[<span data-ttu-id="0b927-127">Связанные технологии поиска</span><span class="sxs-lookup"><span data-stu-id="0b927-127">Related Search Technologies</span></span>](-search-3x-wds-sampleentry.md)

[<span data-ttu-id="0b927-128">Глоссарий поиска Windows</span><span class="sxs-lookup"><span data-stu-id="0b927-128">Windows Search Glossary</span></span>](search-glossary.md)
