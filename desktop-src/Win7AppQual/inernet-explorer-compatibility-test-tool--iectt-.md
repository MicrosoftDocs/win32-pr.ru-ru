---
description: Средство проверки совместимости с Internet Explorer (IECTT)
ms.assetid: 11169540-555A-48A9-A4CD-535D5765C005
title: Средство проверки совместимости с Internet Explorer (IECTT)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a3a35b3120e95c668f2808c9c525d0c1d4f89f8f
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2021
ms.locfileid: "108088288"
---
# <a name="internet-explorer-compatibility-test-tool-iectt"></a><span data-ttu-id="10477-103">Средство проверки совместимости с Internet Explorer (IECTT)</span><span class="sxs-lookup"><span data-stu-id="10477-103">Internet Explorer Compatibility Test Tool (IECTT)</span></span>

<span data-ttu-id="10477-104">Средство тестирования совместимости Internet Explorer (ИЕКТТ) является компонентом [набора средств для обеспечения совместимости приложений (Майкрософт](/windows-hardware/get-started/adk-install)).</span><span class="sxs-lookup"><span data-stu-id="10477-104">The Internet Explorer Compatibility Test Tool (IECTT) is a component of the [Microsoft Application Compatibility Toolkit](/windows-hardware/get-started/adk-install).</span></span> <span data-ttu-id="10477-105">Это средство помогает диагностировать проблемы в веб-приложениях за счет отображения проблем в режиме реального времени и при необходимости отправки результатов в базу данных служб.</span><span class="sxs-lookup"><span data-stu-id="10477-105">This tool can help you diagnose issues in your web applications by displaying issues in real time and optionally uploading the results to an ACT database.</span></span> <span data-ttu-id="10477-106">В результаты входят сведения о возможных проблемах совместимости и ссылки на дополнительные сведения о каждой из проблем совместимости.</span><span class="sxs-lookup"><span data-stu-id="10477-106">The results include details about possible compatibility issues and links for more information about each compatibility issue.</span></span> <span data-ttu-id="10477-107">ИЕКТТ также позволяет исключать проблемы и изменять доступные атрибуты.</span><span class="sxs-lookup"><span data-stu-id="10477-107">IECTT also enables you to exclude issues and modify available attributes.</span></span>

## <a name="to-open-iectt"></a><span data-ttu-id="10477-108">Открытие ИЕКТТ</span><span class="sxs-lookup"><span data-stu-id="10477-108">To open IECTT</span></span>

1.  <span data-ttu-id="10477-109">Установите [набор средств для обеспечения совместимости приложений Microsoft](/windows-hardware/get-started/adk-install).</span><span class="sxs-lookup"><span data-stu-id="10477-109">Install the [Microsoft Application Compatibility Toolkit](/windows-hardware/get-started/adk-install).</span></span>
2.  <span data-ttu-id="10477-110">Нажмите кнопку **Пуск**, последовательно выберите пункты **программы**, набор средств для **обеспечения совместимости приложений Microsoft 5,6**, **Инструменты разработчика и тестера**, а затем щелкните **средство проверки совместимости Internet Explorer**.</span><span class="sxs-lookup"><span data-stu-id="10477-110">Click **Start**, point to **Programs**, point to **Microsoft Application Compatibility Toolkit 5.6**, point to **Developer and Tester Tools**, and then click **Internet Explorer Compatibility Test Tool**.</span></span>

<span data-ttu-id="10477-111">В следующих разделах описаны распространенные сценарии ИЕКТТ.</span><span class="sxs-lookup"><span data-stu-id="10477-111">The following sections describe common IECTT scenarios.</span></span>

## <a name="view-issues-in-real-time"></a><span data-ttu-id="10477-112">Просмотр проблем в режиме реального времени</span><span class="sxs-lookup"><span data-stu-id="10477-112">View Issues in Real Time</span></span>

<span data-ttu-id="10477-113">Вы можете размещать и просматривать веб-проблемы в режиме реального времени, во время тестирования веб-сайтов и приложений на основе Windows Internet Explorer 7 и Windows Internet Explorer 8.</span><span class="sxs-lookup"><span data-stu-id="10477-113">You can locate and view your web-based issues in real time, while you are testing your websites and web applications against Windows Internet Explorer 7 and Windows Internet Explorer 8.</span></span> <span data-ttu-id="10477-114">После завершения тестирования можно просмотреть результаты на экране " **Интерактивные данные** " иектт.</span><span class="sxs-lookup"><span data-stu-id="10477-114">After you complete your testing, you can view your results in the **Live Data** screen of the IECTT.</span></span>

## <a name="upload-issues-to-your-act-database"></a><span data-ttu-id="10477-115">Отправка проблем в базу данных функций</span><span class="sxs-lookup"><span data-stu-id="10477-115">Upload Issues to Your ACT Database</span></span>

<span data-ttu-id="10477-116">Вы можете отправить веб-проблемы в базу данных, которая обрабатывает эту информацию и позволяет просматривать результаты на экране **анализ** диспетчера совместимости приложений.</span><span class="sxs-lookup"><span data-stu-id="10477-116">You can upload your web-based issues to the ACT database, which processes the information and enables you to view your results on the **Analyze** screen of the Application Compatibility Manager.</span></span>

## <a name="collect-your-compatibility-data"></a><span data-ttu-id="10477-117">Собирайте данные о совместимости</span><span class="sxs-lookup"><span data-stu-id="10477-117">Collect Your Compatibility Data</span></span>

<span data-ttu-id="10477-118">Вы можете собираются данные о совместимости веб-сайта и приложения с помощью средства ИЕКТТ с Internet Explorer 7 или Internet Explorer 7.</span><span class="sxs-lookup"><span data-stu-id="10477-118">You can collect your website and web application-related compatibility data by using the IECTT tool with either Internet Explorer 7 or Internet Explorer 7.</span></span>

<span data-ttu-id="10477-119">**Получение данных о совместимости**</span><span class="sxs-lookup"><span data-stu-id="10477-119">**To collect your compatibility data**</span></span>

1.  <span data-ttu-id="10477-120">Закройте все активные окна Windows Internet Explorer.</span><span class="sxs-lookup"><span data-stu-id="10477-120">Close all of your active Windows Internet Explorer windows.</span></span>
2.  <span data-ttu-id="10477-121">В ИЕКТТ на панели инструментов **средства тестирования совместимости Internet Explorer** щелкните **включить**.</span><span class="sxs-lookup"><span data-stu-id="10477-121">In IECTT, on the **Internet Explorer Compatibility Test Tool** toolbar, click **Enable**.</span></span>
3.  <span data-ttu-id="10477-122">Откройте окно Internet Explorer 7 или Internet Explorer 8.</span><span class="sxs-lookup"><span data-stu-id="10477-122">Open an Internet Explorer 7 or Internet Explorer 8 window.</span></span>

    <span data-ttu-id="10477-123">Появится сообщение, в котором будет указано, что включено ведение журнала оценки совместимости.</span><span class="sxs-lookup"><span data-stu-id="10477-123">A message appears and states that compatibility evaluation logging is turned on.</span></span>

4.  <span data-ttu-id="10477-124">Посетите веб-сайты или веб-приложения, необходимые для использования в Организации.</span><span class="sxs-lookup"><span data-stu-id="10477-124">Visit the websites or web applications that are required for use by your organization.</span></span> <span data-ttu-id="10477-125">По мере посещения каждого сайта средство ИЕКТТ отображает в реальном времени потенциальные проблемы совместимости.</span><span class="sxs-lookup"><span data-stu-id="10477-125">As you visit each site, the IECTT tool displays, in real-time, your potential compatibility issues.</span></span>
5.  <span data-ttu-id="10477-126">На панели инструментов **средства тестирования совместимости Internet Explorer** нажмите кнопку **Отключить** по завершении.</span><span class="sxs-lookup"><span data-stu-id="10477-126">On the **Internet Explorer Compatibility Test Tool** toolbar, click **Disable** when you are done.</span></span>

    <span data-ttu-id="10477-127">Процесс ведения журнала совместимости завершается и останавливается.</span><span class="sxs-lookup"><span data-stu-id="10477-127">The compatibility logging process finishes and stops.</span></span>

## <a name="filter-your-issue-results"></a><span data-ttu-id="10477-128">Фильтрация результатов проблем</span><span class="sxs-lookup"><span data-stu-id="10477-128">Filter Your Issue Results</span></span>

<span data-ttu-id="10477-129">Можно отфильтровать любые результаты ИЕКТТ по имени объекта, по типу проблемы или обоим.</span><span class="sxs-lookup"><span data-stu-id="10477-129">You can filter any of your IECTT results by object name, by issue type, or by both.</span></span>

<span data-ttu-id="10477-130">**Фильтрация результатов проблемы**</span><span class="sxs-lookup"><span data-stu-id="10477-130">**To filter your issue results**</span></span>

1.  <span data-ttu-id="10477-131">На экране **средства проверки совместимости Internet Explorer** нажмите кнопку **Фильтр**.</span><span class="sxs-lookup"><span data-stu-id="10477-131">On the **Internet Explorer Compatibility Test Tool** screen, click **Filter**.</span></span>

    <span data-ttu-id="10477-132">Откроется диалоговое окно **фильтр проблем** .</span><span class="sxs-lookup"><span data-stu-id="10477-132">The **Issues Filter** dialog box appears.</span></span>

2.  <span data-ttu-id="10477-133">Введите имя объекта, который вы хотите просмотреть, в поле **введите имя объекта для просмотра проблем** .</span><span class="sxs-lookup"><span data-stu-id="10477-133">Enter the name of the object that you intend to view in the **Enter the name of the object to view issues for** box.</span></span>

<span data-ttu-id="10477-134">Дополнительные сведения об этом средстве и других средствах для разработчиков см. в статье [что такое средство тестирования совместимости Internet Explorer?](/previous-versions/windows/it-pro/windows-7/cc721989(v=ws.10)) в библиотеке MSDN и в записи блога о [совместимости приложений в приложении IE8](/archive/blogs/ie/application-compatibility-logging-in-ie8) .</span><span class="sxs-lookup"><span data-stu-id="10477-134">For more information about this tool and other developers tools, see [What is the Internet Explorer Compatibility Test Tool?](/previous-versions/windows/it-pro/windows-7/cc721989(v=ws.10)) in the MSDN Library and the [Application Compatibility Logging in IE8](/archive/blogs/ie/application-compatibility-logging-in-ie8) blog post.</span></span>

## <a name="related-topics"></a><span data-ttu-id="10477-135">Связанные разделы</span><span class="sxs-lookup"><span data-stu-id="10477-135">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="10477-136">Средства для отладки веб-приложений и дополнительных компонентов</span><span class="sxs-lookup"><span data-stu-id="10477-136">Tools for Debugging Web Applications and Add-Ons</span></span>](tools-for-debugging-web-applications-and-add-ons.md)
</dt> </dl>

 

 
