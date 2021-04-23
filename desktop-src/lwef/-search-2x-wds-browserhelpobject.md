---
title: Вызов WDS из веб-страниц
description: Можно вызвать Microsoft Windows Desktop Search (WDS) с любой веб-страницы, созданной или обслуживаемой с помощью объекта модуля поддержки браузера (BHO) и Windows Internet Explorer.
ms.assetid: 8d9fa541-530e-4917-a6d9-4e04549ce32e
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 782e7ca8b529c8f69b1f36d44decfae44895e4ec
ms.sourcegitcommit: b9a94cea8f83153214af4c09509e1cc61a1bb616
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 05/19/2020
ms.locfileid: "104069676"
---
# <a name="calling-wds-from-web-pages"></a><span data-ttu-id="e9a22-103">Вызов WDS из веб-страниц</span><span class="sxs-lookup"><span data-stu-id="e9a22-103">Calling WDS from Web Pages</span></span>

> [!NOTE]
> <span data-ttu-id="e9a22-104">Windows Desktop Search 2. x — это устаревшая технология, которая изначально была доступна в качестве надстройки для Windows XP и Windows Server 2003.</span><span class="sxs-lookup"><span data-stu-id="e9a22-104">Windows Desktop Search 2.x is an obsolete technology that was originally available as an add-in for Windows XP and Windows Server 2003.</span></span> <span data-ttu-id="e9a22-105">В более поздних выпусках используйте вместо этого [Поиск Windows](../search/-search-3x-wds-overview.md) .</span><span class="sxs-lookup"><span data-stu-id="e9a22-105">On later releases, use [Windows Search](../search/-search-3x-wds-overview.md) instead.</span></span>

<span data-ttu-id="e9a22-106">Можно вызвать Microsoft Windows Desktop Search (WDS) с любой веб-страницы, созданной или обслуживаемой с помощью объекта модуля поддержки браузера (BHO) и Windows Internet Explorer.</span><span class="sxs-lookup"><span data-stu-id="e9a22-106">You can call Microsoft Windows Desktop Search (WDS) from any webpage you create or maintain using the Browser Helper Object (BHO) and Windows Internet Explorer.</span></span> <span data-ttu-id="e9a22-107">Вы можете увидеть, как это работает на веб-странице MSN.</span><span class="sxs-lookup"><span data-stu-id="e9a22-107">You can see how this works on the MSN webpage.</span></span> <span data-ttu-id="e9a22-108">Над полем поиска https://www.msn.com находится несколько типов поиска: Web, News, Images, Desktop, Encarta и local.</span><span class="sxs-lookup"><span data-stu-id="e9a22-108">Above the search box on https://www.msn.com are several search types: Web, News, Images, Desktop, Encarta, and Local.</span></span> <span data-ttu-id="e9a22-109">При нажатии кнопки Desktop параметры поиска передаются в Windows Desktop Search, который выполняет поиск в каталоге и отображает результаты в пользовательском интерфейсе WDS.</span><span class="sxs-lookup"><span data-stu-id="e9a22-109">If you click Desktop, the search parameters are passed to Windows Desktop Search, which searches the catalog and displays results in the WDS user interface.</span></span> <span data-ttu-id="e9a22-110">Чтобы пользователи могли запускать поиск на рабочем столе с веб-страниц, ВДСБХО должен быть установлен и включен в своих системах, веб-страницы должны быть зарегистрированы в WDS в качестве разрешенного URL-адреса, и необходимо создать ссылку для передачи запроса User-енетеред в WDS.</span><span class="sxs-lookup"><span data-stu-id="e9a22-110">For users to start a desktop search from your webpage(s), the WDSBHO must be installed and enabled on their systems, your webpage(s) must be registered with WDS as an allowed URL, and you must create a link to pass the user-enetered query to WDS.</span></span>

## <a name="enabling-the-wds-browser-help-object"></a><span data-ttu-id="e9a22-111">Включение объекта справки в браузере WDS</span><span class="sxs-lookup"><span data-stu-id="e9a22-111">Enabling the WDS Browser Help Object</span></span>

<span data-ttu-id="e9a22-112">Объект BHO устанавливается и включается в Internet Explorer по умолчанию при установке WDS, но можно легко проверить, что он не был отключен или удален.</span><span class="sxs-lookup"><span data-stu-id="e9a22-112">The BHO is installed and enabled within Internet Explorer by default when you install WDS, but you can easily verify that it hasn't been disabled or uninstalled.</span></span> <span data-ttu-id="e9a22-113">В системе пользователя откройте Internet Explorer, в меню **Сервис** выберите пункт **Свойства обозревателя** , перейдите на вкладку **программы** и выберите пункт **Управление надстройками**.</span><span class="sxs-lookup"><span data-stu-id="e9a22-113">On a user's system, open Internet Explorer , select **Internet Options** from the **Tools** menu, click the **Programs** tab, and then click **Manage Add-Ons**.</span></span> <span data-ttu-id="e9a22-114">В списке надстроек Найдите класс Дсвебалловбхо и убедитесь, что он включен.</span><span class="sxs-lookup"><span data-stu-id="e9a22-114">In your list of add-ons, look for the dsWebAllowBHO Class and make sure it is enabled.</span></span> <span data-ttu-id="e9a22-115">Если объект BHO отключен, службы WDS продолжат работу в обычном режиме. Однако вы не сможете выполнять поиск на рабочем столе с веб-страницы.</span><span class="sxs-lookup"><span data-stu-id="e9a22-115">When the BHO is disabled, WDS will continue to work normally; however, you will not be able to search the desktop from a webpage.</span></span>

<span data-ttu-id="e9a22-116">Оба следующих варианта для разрешения поиска на рабочем столе будут выполнять поиск локально с зарегистрированным приложением поиска.</span><span class="sxs-lookup"><span data-stu-id="e9a22-116">Both of the following options for allowing a desktop search will execute the search locally with the registered search application.</span></span>

## <a name="registering-web-page-urls"></a><span data-ttu-id="e9a22-117">Регистрация URL веб-страниц</span><span class="sxs-lookup"><span data-stu-id="e9a22-117">Registering Web Page URLs</span></span>

<span data-ttu-id="e9a22-118">В реестре содержится список разрешенных URL-адресов доменов, из которых можно вызывать службы WDS.</span><span class="sxs-lookup"><span data-stu-id="e9a22-118">The Registry includes a list of "allowed" domain URLs from which WDS can be called.</span></span> <span data-ttu-id="e9a22-119">Чтобы включить веб-страницы, необходимо перечислить URL-адреса доменов в виде REG \_ SZ в реестре следующим образом:</span><span class="sxs-lookup"><span data-stu-id="e9a22-119">To include your webpage(s), you need to list your domain URL(s) as REG\_SZ in the Registry as follows:</span></span>

<span data-ttu-id="e9a22-120">**HKey \_ \_** \\ **Программное обеспечение** локального компьютера \\ **Microsoft** \\ **Windows Desktop Search** \\ **DSW** \\ **Allowed**\\*<number>* = <domainURL></span><span class="sxs-lookup"><span data-stu-id="e9a22-120">**HKEY\_LOCAL\_MACHINE**\\**Software**\\**Microsoft**\\**Windows Desktop Search**\\**DSW**\\**Allowed**\\*<number>* = <domainURL></span></span>

<span data-ttu-id="e9a22-121">Где **<number>** является последовательно пронумерованным, а **<domainURL>** — URL веб-страницы, из которой нужно разрешить поиск WDS.</span><span class="sxs-lookup"><span data-stu-id="e9a22-121">Where **<number>** is sequentially numbered, and **<domainURL>** is the URL of the Web Page you want to allow WDS searches from.</span></span> <span data-ttu-id="e9a22-122">Эта строка URL-адреса может включать символ звездочки \* в начале или в конце URL-адреса.</span><span class="sxs-lookup"><span data-stu-id="e9a22-122">This URL string can include the wildcard asterisk \* at the beginning or end of the URL.</span></span> <span data-ttu-id="e9a22-123">Например, если строка имеет значение " \* . mydomain.com", можно запустить поиск WDS из обеих https://www.mydomain.com и https://mydomain.com .</span><span class="sxs-lookup"><span data-stu-id="e9a22-123">For example, if the string is "\*.mydomain.com", then you can start a WDS search from both https://www.mydomain.com and https://mydomain.com.</span></span>

## <a name="enabling-desktop-search-by-url"></a><span data-ttu-id="e9a22-124">Включение поиска на рабочем столе по URL-адресу</span><span class="sxs-lookup"><span data-stu-id="e9a22-124">Enabling Desktop Search by URL</span></span>

<span data-ttu-id="e9a22-125">Другим вариантом, который не требует доступа к реестру, является использование следующего URL-адреса на веб-страницах:</span><span class="sxs-lookup"><span data-stu-id="e9a22-125">Another option that does not require access to the Registry is to use the following URL on your webpage(s):</span></span>

https://toolbar.msn.com/desktop/results.aspx?q=QUERY

<span data-ttu-id="e9a22-126">где **Query** — строка в кодировке URL, в которой выполняется поиск пользователя, включая все [Расширенные термины синтаксиса запроса](-search-2x-wds-aqsreference.md) .</span><span class="sxs-lookup"><span data-stu-id="e9a22-126">where **QUERY** is the URL-encoded string the user is searching on, including any [Advanced Query Syntax](-search-2x-wds-aqsreference.md) terms.</span></span>

 

 




