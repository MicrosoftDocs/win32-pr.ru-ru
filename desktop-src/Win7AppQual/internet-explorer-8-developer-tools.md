---
description: .
ms.assetid: D721167E-B04B-4B06-A9EE-56711A7A1942
title: Средства для разработчиков Internet Explorer 8
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a184b513717655ee0a738be6318b4c8f2515ca3f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "104156674"
---
# <a name="internet-explorer-8-developer-tools"></a><span data-ttu-id="21ebb-103">Средства для разработчиков Internet Explorer 8</span><span class="sxs-lookup"><span data-stu-id="21ebb-103">Internet Explorer 8 Developer Tools</span></span>

<span data-ttu-id="21ebb-104">Windows Internet Explorer 8 включает функцию Средства для разработчиков.</span><span class="sxs-lookup"><span data-stu-id="21ebb-104">Windows Internet Explorer 8 includes the Developer Tools feature.</span></span> <span data-ttu-id="21ebb-105">Эта функция позволяет быстро выполнять отладку Microsoft JScript, исследовать поведение Windows Internet Explorer или быстро выполнить итерацию по созданию прототипа или тестированию нового решения.</span><span class="sxs-lookup"><span data-stu-id="21ebb-105">This feature enables you to debug Microsoft JScript quickly, investigate a Windows Internet Explorer-specific behavior, or iterate rapidly to prototype or test a new design solution.</span></span>

<span data-ttu-id="21ebb-106">В следующих разделах описываются важные характеристики Средства для разработчиков в Internet Explorer 8.</span><span class="sxs-lookup"><span data-stu-id="21ebb-106">The following sections describe the important characteristics of the Developer Tools in Internet Explorer 8.</span></span>

## <a name="integrated-and-simple-to-use"></a><span data-ttu-id="21ebb-107">Интеграция и простота использования</span><span class="sxs-lookup"><span data-stu-id="21ebb-107">Integrated and Simple to Use</span></span>

<span data-ttu-id="21ebb-108">Средства для разработчиков включены в каждую установку Internet Explorer 8, поэтому можно выполнять отладку проблем на любом компьютере, где работает Internet Explorer 8.</span><span class="sxs-lookup"><span data-stu-id="21ebb-108">The Developer Tools are included with every installation of Internet Explorer 8, so you can debug issues on any computer that is running Internet Explorer 8.</span></span> <span data-ttu-id="21ebb-109">Кроме того, средства загружаются только при необходимости, чтобы ограничить их влияние на производительность браузера.</span><span class="sxs-lookup"><span data-stu-id="21ebb-109">In addition, the tools load only when you need them to limit how they impact the browser's performance.</span></span> <span data-ttu-id="21ebb-110">С помощью Средства для разработчиков можно быстро отлаживать только текущий процесс Internet Explorer, а не отладку для всего обозревателя Internet Explorer.</span><span class="sxs-lookup"><span data-stu-id="21ebb-110">By using the Developer Tools, you can rapidly debug only the current Internet Explorer process, instead of debugging for all of Internet Explorer.</span></span>

## <a name="provide-a-visual-interface-to-the-platform"></a><span data-ttu-id="21ebb-111">Предоставление визуального интерфейса для платформы</span><span class="sxs-lookup"><span data-stu-id="21ebb-111">Provide a Visual Interface to the Platform</span></span>

<span data-ttu-id="21ebb-112">Вместо реконструирования работы веб-сайта или изменения сайта для вывода отладочной информации Средства для разработчиков разрешите обозревателю Internet Explorer просмотреть его представление сайта.</span><span class="sxs-lookup"><span data-stu-id="21ebb-112">Instead of reverse engineering how your website works or modifying your site to output debug information, the Developer Tools let you look into Internet Explorer to view its representation of your site.</span></span> <span data-ttu-id="21ebb-113">Это представление сокращает время, затрачиваемое на отладку динамических сайтов, когда проверка исходного кода не полезна или изучает поведение, характерное для обозревателя Internet Explorer, в котором не может помочь универсальный инструмент разработки.</span><span class="sxs-lookup"><span data-stu-id="21ebb-113">This view reduces the time that you spend debugging dynamic sites, where source inspection is not useful, or investigating an Internet Explorer-specific behavior, where a generic authoring tool cannot help.</span></span>

## <a name="enable-fast-experimentation"></a><span data-ttu-id="21ebb-114">Включить быстрое экспериментирование</span><span class="sxs-lookup"><span data-stu-id="21ebb-114">Enable Fast Experimentation</span></span>

<span data-ttu-id="21ebb-115">При создании прототипа нового проекта или исправления в предыдущих версиях Internet Explorer, скорее всего, вы изменяете источник, сохраняете его, обновляете страницу в браузере и повторяйте.</span><span class="sxs-lookup"><span data-stu-id="21ebb-115">When you are prototyping a new design or testing fixes in previous versions of Internet Explorer, you likely edit your source, save it, refresh your page in the browser, and repeat.</span></span> <span data-ttu-id="21ebb-116">Средства для разработчиков упростить этот сценарий, позволяя редактировать сайт в браузере и немедленно просматривать изменения.</span><span class="sxs-lookup"><span data-stu-id="21ebb-116">The Developer Tools streamline this scenario by enabling you to edit your site within the browser and see changes immediately.</span></span>

## <a name="optimize-application-performance"></a><span data-ttu-id="21ebb-117">Оптимизация производительности приложения</span><span class="sxs-lookup"><span data-stu-id="21ebb-117">Optimize Application Performance</span></span>

<span data-ttu-id="21ebb-118">Чтобы выявление и устранение проблем с производительностью, вы, скорее всего, перебираетесь по одному сценарию за раз.</span><span class="sxs-lookup"><span data-stu-id="21ebb-118">To identify and fix performance issues, you likely iterate by focusing on one scenario at a time.</span></span> <span data-ttu-id="21ebb-119">С помощью профилировщика скриптов в Средства для разработчиков можно выполнять сбор статистики, включая время выполнения и число вызовов функции JavaScript.</span><span class="sxs-lookup"><span data-stu-id="21ebb-119">By using the script profiler in the Developer Tools, you can collect statistics, including execution time and the number of times that a JavaScript function is called.</span></span> <span data-ttu-id="21ebb-120">Эти сведения можно использовать при тестировании приложения и использовании отчета профиля для быстрого выявления и устранения узких мест производительности.</span><span class="sxs-lookup"><span data-stu-id="21ebb-120">You can use this information as you test your application and use the profile report to quickly identify and fix performance bottlenecks.</span></span>

<span data-ttu-id="21ebb-121">Чтобы получить доступ к Средства для разработчиков, нажмите клавишу F12 во время просмотра веб-страницы или выберите **средства для разработчиков** в меню **Сервис** .</span><span class="sxs-lookup"><span data-stu-id="21ebb-121">To access the Developer Tools, press F12 while you are viewing a webpage or click **Developer Tools** on the **Tools** menu.</span></span>

## <a name="related-topics"></a><span data-ttu-id="21ebb-122">См. также</span><span class="sxs-lookup"><span data-stu-id="21ebb-122">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="21ebb-123">Средства для отладки веб-приложений и дополнительных компонентов</span><span class="sxs-lookup"><span data-stu-id="21ebb-123">Tools for Debugging Web Applications and Add-Ons</span></span>](tools-for-debugging-web-applications-and-add-ons.md)
</dt> </dl>

 

 



