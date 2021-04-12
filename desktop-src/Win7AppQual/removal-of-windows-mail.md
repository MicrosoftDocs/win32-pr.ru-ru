---
description: .
ms.assetid: 356f0d79-12dd-49f0-b756-a46f20177efa
title: Удаление почты Windows
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 836b2f447735c8e3595955ca7e99f1ae818c3d5c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "104272245"
---
# <a name="removal-of-windows-mail"></a><span data-ttu-id="8989c-103">Удаление почты Windows</span><span class="sxs-lookup"><span data-stu-id="8989c-103">Removal of Windows Mail</span></span>

## <a name="affected-platforms"></a><span data-ttu-id="8989c-104">Затронутые платформы</span><span class="sxs-lookup"><span data-stu-id="8989c-104">Affected Platforms</span></span>

<span data-ttu-id="8989c-105">**Клиенты** — Windows 7</span><span class="sxs-lookup"><span data-stu-id="8989c-105">**Clients** - Windows 7</span></span>  
<span data-ttu-id="8989c-106">**Серверы** — Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="8989c-106">**Servers** - Windows Server 2008 R2</span></span>  









## <a name="feature-impact"></a><span data-ttu-id="8989c-107">Воздействие на функции</span><span class="sxs-lookup"><span data-stu-id="8989c-107">Feature Impact</span></span>

<span data-ttu-id="8989c-108">**Серьезность** — высокая</span><span class="sxs-lookup"><span data-stu-id="8989c-108">**Severity** - High</span></span>  
<span data-ttu-id="8989c-109">**Частота** — высокая</span><span class="sxs-lookup"><span data-stu-id="8989c-109">**Frequency** - High</span></span>  









## <a name="description"></a><span data-ttu-id="8989c-110">Описание</span><span class="sxs-lookup"><span data-stu-id="8989c-110">Description</span></span>

<span data-ttu-id="8989c-111">Корпорация Майкрософт не является рекомендуемой служебной программой Windows Mail и отключением API Костартаутлукекспресс.</span><span class="sxs-lookup"><span data-stu-id="8989c-111">Microsoft is deprecating the Windows Mail utility and disabling the API CoStartOutlookExpress.</span></span> <span data-ttu-id="8989c-112">Другие почтовые API были помечены как устаревшие и будут удалены в более поздней версии Windows.</span><span class="sxs-lookup"><span data-stu-id="8989c-112">The other mail APIs have been marked as deprecated and are slated for removal in a later Windows version.</span></span> <span data-ttu-id="8989c-113">Однако общедоступные API, которые не помечены как устаревшие или устаревшие, будут продолжать работать в Windows 7.</span><span class="sxs-lookup"><span data-stu-id="8989c-113">However, the publicly documented APIs that are not marked as deprecated or obsolete will continue to function in Windows 7.</span></span> <span data-ttu-id="8989c-114">Двоичные файлы останутся в системах пользователей и будут по-прежнему доступны через API-интерфейсы, особенно в случаях, описанных выше.</span><span class="sxs-lookup"><span data-stu-id="8989c-114">Binaries will remain on the users' systems and will continue to be accessible via the APIs, specifically in the cases mentioned above.</span></span> <span data-ttu-id="8989c-115">Кроме того, файлы электронной почты пользователей (. EML) и новости (. NWS) останутся в системе.</span><span class="sxs-lookup"><span data-stu-id="8989c-115">In addition, the users' email (.eml) and news (.nws) files will remain on the system.</span></span>

## <a name="manifestation-of-impact"></a><span data-ttu-id="8989c-116">Влияние на манифесты</span><span class="sxs-lookup"><span data-stu-id="8989c-116">Manifestation of Impact</span></span>

<span data-ttu-id="8989c-117">Удаление почты Windows приводит к следующим результатам:</span><span class="sxs-lookup"><span data-stu-id="8989c-117">Removal of Windows Mail results in the following:</span></span>

-   <span data-ttu-id="8989c-118">Все точки входа в почту Windows и контакты (например, меню "Пуск", ярлыки, созданные пользователем, "Запуск >" и т. д.) удаляются или отключаются.</span><span class="sxs-lookup"><span data-stu-id="8989c-118">All entry points to Windows Mail and Contacts (for example, Start Menu, user-created Shortcuts, Start -> Run, and so on) are removed or disabled.</span></span> <span data-ttu-id="8989c-119">Некоторые из них полностью удалены, другие не будут работать при попытке запуска.</span><span class="sxs-lookup"><span data-stu-id="8989c-119">Some of these are completely removed, others will fail when trying to launch.</span></span>
-   <span data-ttu-id="8989c-120">Все библиотеки DLL поставляются в Box</span><span class="sxs-lookup"><span data-stu-id="8989c-120">All DLLs ship in the box</span></span>
-   <span data-ttu-id="8989c-121">Общедоступные API-интерфейсы продолжают работать, как в Windows Vista</span><span class="sxs-lookup"><span data-stu-id="8989c-121">Publicly documented APIs continue to work as they did in Windows Vista</span></span>
-   <span data-ttu-id="8989c-122">Все интерфейсы API, пытающиеся запустить основной пользовательский интерфейс браузера, были изменены для создания автоматического сбоя.</span><span class="sxs-lookup"><span data-stu-id="8989c-122">Any APIs that attempt to launch the main browser UI have been modified to create a silent failure.</span></span> <span data-ttu-id="8989c-123">Функция вернет значение Success, но не будет отображать пользовательский интерфейс для пользователя.</span><span class="sxs-lookup"><span data-stu-id="8989c-123">The function will return success, but will not show the UI to the user.</span></span> <span data-ttu-id="8989c-124">Интерфейсы API, вызывающие другие диалоговые окна (например, диспетчер очереди печати или диалоговое окно учетных записей), продолжают отображать этот пользовательский интерфейс</span><span class="sxs-lookup"><span data-stu-id="8989c-124">APIs that call other dialog boxes (for example, the Spooler or the Accounts dialog) continue to show that UI</span></span>
-   <span data-ttu-id="8989c-125">Протокол (mailto, LDAP, News, сневс, NNTP) не будет связан с компонентом "Почта Windows" или "Контакты".</span><span class="sxs-lookup"><span data-stu-id="8989c-125">Protocol (mailto, ldap, news, snews, nntp) handlers will not be associated with Windows Mail or Contacts.</span></span> <span data-ttu-id="8989c-126">При попытке запустить их клиенты увидят диалоговое окно с сообщением об ошибке, указывающее на расположение, где они могут установить эти связи для другой программы.</span><span class="sxs-lookup"><span data-stu-id="8989c-126">When attempting to launch these, customers will see an error dialog pointing them to the location where they can set these associations to another program</span></span>
-   <span data-ttu-id="8989c-127">Сопоставления файлов (. EML,. NWS,. Contact,. Group,. wab,. p7c,. VFC) будут разорваны или отключены.</span><span class="sxs-lookup"><span data-stu-id="8989c-127">File associations (.eml, .nws, .contact, .group, .wab, .p7c, .vfc) are broken or disabled.</span></span> <span data-ttu-id="8989c-128">При попытке открыть файл с этими расширениями клиенты получат диалоговое окно с предложением установить другие приложения, которые они могут использовать, и указать веб-странице, предлагающей решения</span><span class="sxs-lookup"><span data-stu-id="8989c-128">When attempting to open a file with these extensions, customers will get a dialog box offering them other apps that are installed that they can use and point them to a webpage that offers solutions</span></span>
-   <span data-ttu-id="8989c-129">Все файлы пользователей (например, файлы контактов или сообщения) остаются в системе в сценарии обновления.</span><span class="sxs-lookup"><span data-stu-id="8989c-129">Any user files (for example, contact files or messages) remain on the system in the upgrade scenario</span></span>
-   <span data-ttu-id="8989c-130">Папка Контакты скрыта по умолчанию, поэтому клиенты не увидят ее.</span><span class="sxs-lookup"><span data-stu-id="8989c-130">The Contacts folder is hidden by default so customers will not see it</span></span>
-   <span data-ttu-id="8989c-131">API-интерфейсы помечены как устаревшие в MSDN</span><span class="sxs-lookup"><span data-stu-id="8989c-131">APIs are marked as deprecated in MSDN</span></span>
-   <span data-ttu-id="8989c-132">Функция предварительного просмотра файла удалена</span><span class="sxs-lookup"><span data-stu-id="8989c-132">The file preview function is removed</span></span>
-   <span data-ttu-id="8989c-133">Перехватчики оболочки в контекстном меню удаляются</span><span class="sxs-lookup"><span data-stu-id="8989c-133">Shell hooks in the right-click menu are removed</span></span>
-   <span data-ttu-id="8989c-134">Функция поиска файлов удалена</span><span class="sxs-lookup"><span data-stu-id="8989c-134">The file search function is removed</span></span>

## <a name="mitigation"></a><span data-ttu-id="8989c-135">Меры по снижению риска</span><span class="sxs-lookup"><span data-stu-id="8989c-135">Mitigation</span></span>

<span data-ttu-id="8989c-136">Пользователям следует установить Windows Live Mail или любой другой почтовый продукт, который может читать файлы. EML и. NWS.</span><span class="sxs-lookup"><span data-stu-id="8989c-136">Users should install Windows Live Mail or any other mail product that is able to read .eml and .nws files.</span></span>

## <a name="solution"></a><span data-ttu-id="8989c-137">Решение</span><span class="sxs-lookup"><span data-stu-id="8989c-137">Solution</span></span>

<span data-ttu-id="8989c-138">Определение наличия установленного обработчика почты по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="8989c-138">Detect if there is a default mail handler installed.</span></span> <span data-ttu-id="8989c-139">Если нет, посоветуйте пользователю установить Windows Live Mail или любой другой продукт, который может читать файлы EML и NWS.</span><span class="sxs-lookup"><span data-stu-id="8989c-139">If not, advise user to install Windows Live Mail or any other product that is able to read .eml and .nws files.</span></span>

<span data-ttu-id="8989c-140">Не разрабатывать код, вызывающий API пользовательского интерфейса почты Windows, так как он не будет работать.</span><span class="sxs-lookup"><span data-stu-id="8989c-140">Do not design code that calls the Windows Mail UI API, since it will not work.</span></span> <span data-ttu-id="8989c-141">Вы должны найти другие способы доступа к файлам. EML и. NWS.</span><span class="sxs-lookup"><span data-stu-id="8989c-141">You must find other ways to access the .eml and .nws files.</span></span> <span data-ttu-id="8989c-142">Кроме того, как только это станет возможным, следует прекратить зависимость от всех других API почты Windows.</span><span class="sxs-lookup"><span data-stu-id="8989c-142">In addition, as soon as is feasible, discontinue your reliance on all other Windows Mail APIs.</span></span>

## <a name="compatibility-performance-reliability-and-usability-testing"></a><span data-ttu-id="8989c-143">Совместимость, производительность, надежность и тестирование на удобство использования</span><span class="sxs-lookup"><span data-stu-id="8989c-143">Compatibility, Performance, Reliability, and Usability Testing</span></span>

-   <span data-ttu-id="8989c-144">Запустите приложение в среде Windows 7, чтобы убедиться, что приложение не пытается вызвать API пользовательского интерфейса.</span><span class="sxs-lookup"><span data-stu-id="8989c-144">Exercise your application in a Windows 7 environment to ensure that the application does not try to call the UI API.</span></span>
-   <span data-ttu-id="8989c-145">Кроме того, вы можете запустить набор средств для обеспечения совместимости приложений (ACT) с помощью средства оценки совместимости Windows (ВЦЕ), чтобы нахождение потенциальных проблем из-за нерекомендуемых функциональных возможностей.</span><span class="sxs-lookup"><span data-stu-id="8989c-145">Alternatively, you can run the Application Compatibility Toolkit (ACT) using the Windows Compatibility Evaluator (WCE) to locate any potential issues due to the deprecation of this functionality.</span></span>

## <a name="links-to-other-resources"></a><span data-ttu-id="8989c-146">Ссылки на другие ресурсы</span><span class="sxs-lookup"><span data-stu-id="8989c-146">Links to Other Resources</span></span>

<dl>

[<span data-ttu-id="8989c-147">Загрузка набора средств для обеспечения совместимости приложений</span><span class="sxs-lookup"><span data-stu-id="8989c-147">Application Compatibility Toolkit Download</span></span>](/windows-hardware/get-started/adk-install)  
</dl>

 

 
