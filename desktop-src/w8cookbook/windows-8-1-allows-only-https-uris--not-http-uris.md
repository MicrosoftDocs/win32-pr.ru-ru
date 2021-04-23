---
title: URI в Windows 8.1
description: Windows 8.1 допускает только URI HTTPS, а не URI HTTP
ms.assetid: 06BDD3A3-67B7-4085-83DA-F322F718C876
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 994780798bfe7ada0d7dc49794deb284e30f1605
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "104413502"
---
# <a name="windows-81-allows-only-https-uris-not-http-uris"></a><span data-ttu-id="9a75c-103">Windows 8.1 допускает только URI HTTPS, а не URI HTTP</span><span class="sxs-lookup"><span data-stu-id="9a75c-103">Windows 8.1 allows only https URIs, not http URIs</span></span>

## <a name="platforms"></a><span data-ttu-id="9a75c-104">Платформы</span><span class="sxs-lookup"><span data-stu-id="9a75c-104">Platforms</span></span>

<dl> <span data-ttu-id="9a75c-105">Клиенты — Windows 8.1</span><span class="sxs-lookup"><span data-stu-id="9a75c-105">Clients - Windows 8.1</span></span>  
<span data-ttu-id="9a75c-106">Серверы — Windows Server 2012 R2</span><span class="sxs-lookup"><span data-stu-id="9a75c-106">Servers - Windows Server 2012 R2</span></span>  
</dl>

## <a name="description"></a><span data-ttu-id="9a75c-107">Описание</span><span class="sxs-lookup"><span data-stu-id="9a75c-107">Description</span></span>

<span data-ttu-id="9a75c-108">Хотя приложения, созданные для Windows 8, могут включать URI HTTP и HTTPS в URI содержимого приложения, приложения, созданные для Windows 8.1, могут содержать только URI-адреса HTTPS.</span><span class="sxs-lookup"><span data-stu-id="9a75c-108">While apps built for Windows 8 can include http and https URIs in their application content URIs, apps built for Windows 8.1 may include only https URIs.</span></span>

<span data-ttu-id="9a75c-109">Единственным исключением является динамическое Контентурирулес, указанное в файле AppxManifest.xml приложения.</span><span class="sxs-lookup"><span data-stu-id="9a75c-109">The only exception is for dynamic ContentUriRules that are specified in the app’s AppxManifest.xml file.</span></span> <span data-ttu-id="9a75c-110">Благодаря динамическому Контентурирулес приложения могут обращаться к дополнительным доменам или сетевым ресурсам, предоставляемым администратором, например групповая политика URI.</span><span class="sxs-lookup"><span data-stu-id="9a75c-110">With dynamic ContentUriRules, apps can access additional domains or network resources that are provided by the admin, such as Group Policy URIs.</span></span> <span data-ttu-id="9a75c-111">Однако динамические Контентурирулес доступны только для приложений Магазина Windows, если они отвечают следующим условиям:</span><span class="sxs-lookup"><span data-stu-id="9a75c-111">However, dynamic ContentUriRules are only available to Windows Store apps if they meet these conditions:</span></span>

-   <span data-ttu-id="9a75c-112">групповая политика включен</span><span class="sxs-lookup"><span data-stu-id="9a75c-112">The Group Policy is enabled</span></span>
-   <span data-ttu-id="9a75c-113">Пакет указал возможность Ентерприсеаусентикатион</span><span class="sxs-lookup"><span data-stu-id="9a75c-113">The package has specified the enterpriseAuthentication capability</span></span>
-   <span data-ttu-id="9a75c-114">OSMaxVersionTested пакета Windows 8.1 или больше</span><span class="sxs-lookup"><span data-stu-id="9a75c-114">The package’s OSMaxVersionTested is Windows 8.1 or greater</span></span>

<span data-ttu-id="9a75c-115">Новые ограничения в Windows 8.1 являются частью улучшенных ограничений безопасности для дальнейшей защиты платформы.</span><span class="sxs-lookup"><span data-stu-id="9a75c-115">The new restrictions in Windows 8.1 are part of enhanced security restrictions to further protect the platform.</span></span>

## <a name="manifestations"></a><span data-ttu-id="9a75c-116">Проявлениями</span><span class="sxs-lookup"><span data-stu-id="9a75c-116">Manifestations</span></span>

<span data-ttu-id="9a75c-117">При запуске приложения, созданного для Windows 8 на Windows 8.1, разрешено использование URI HTTP в [аппликатионконтентурирулес](/uwp/schemas/appxpackage/appxmanifestschema/element-applicationcontenturirules) .</span><span class="sxs-lookup"><span data-stu-id="9a75c-117">When running an app built for Windows 8 on Windows 8.1, the use of http URIs in the [ApplicationContentUriRules](/uwp/schemas/appxpackage/appxmanifestschema/element-applicationcontenturirules) is allowed.</span></span>

## <a name="mitigations"></a><span data-ttu-id="9a75c-118">Устранение проблем</span><span class="sxs-lookup"><span data-stu-id="9a75c-118">Mitigations</span></span>

<span data-ttu-id="9a75c-119">Рекомендуется, чтобы ВВА разработчики переключились с [<iframe>](https://msdn.microsoft.com/library/windows/apps/hh465955.aspx) элемента управления [WebView](/uwp/api/Windows.UI.Xaml.Controls.WebView?view=winrt-19041) (<x-ms-WebView>).</span><span class="sxs-lookup"><span data-stu-id="9a75c-119">We recommend that WWA developers switch from [<iframe>](https://msdn.microsoft.com/library/windows/apps/hh465955.aspx) to the [WebView](/uwp/api/Windows.UI.Xaml.Controls.WebView?view=winrt-19041) control (<x-ms-webview>).</span></span> <span data-ttu-id="9a75c-120">Тем не менее, если требуется поддержка Аппкаче, Индекседдб, географического расположения или программного доступа к буферу обмена, необходимо продолжить использовать</span><span class="sxs-lookup"><span data-stu-id="9a75c-120">However, if you need support for AppCache, IndexedDB, geolocation, or programmatic clipboard access, you will need to continue using</span></span> <iframe> <span data-ttu-id="9a75c-121">для Windows 8.1.</span><span class="sxs-lookup"><span data-stu-id="9a75c-121">for Windows 8.1.</span></span>

<span data-ttu-id="9a75c-122">Продолжение использования</span><span class="sxs-lookup"><span data-stu-id="9a75c-122">Continued usage of</span></span> <iframe> <span data-ttu-id="9a75c-123">для удаленного содержимого потребуется новая запись в Аппликатионконтентурирулес для приложения.</span><span class="sxs-lookup"><span data-stu-id="9a75c-123">for remote content will require a new entry in the ApplicationContentUriRules for the app.</span></span> <span data-ttu-id="9a75c-124">Приложениям с WebView требуются новые записи в Аппликатионконтентурирулес, если веб-содержимому необходимо вызвать метод Window. external. notify для создания события [скриптнотифи](/uwp/api/Windows.UI.Xaml.Controls.WebView?view=winrt-19041) .</span><span class="sxs-lookup"><span data-stu-id="9a75c-124">Apps with WebView require new entries in the ApplicationContentUriRules if the web content needs to invoke window.external.notify for generating a [ScriptNotify](/uwp/api/Windows.UI.Xaml.Controls.WebView?view=winrt-19041) event.</span></span> <span data-ttu-id="9a75c-125">Если у вас нет Visual Studio, вы можете обновить манифест приложения, добавив следующий код XML, включая подстановочные знаки для поддоменов (например, https:// \* . Microsoft.com):</span><span class="sxs-lookup"><span data-stu-id="9a75c-125">If you do not have Visual Studio, you can update the app manifest by adding the following XML, including wildcards for subdomains (e.g. https://\*.microsoft.com):</span></span>


```
<Package>
    …
    <Applications>
        <Application>
            …
            <ApplicationContentUriRules>
                <Rule Match="https://www.example.com" Type="include"/>
            </ApplicationContentUriRules>
        </Application>
    </Applications>
</Package>
```



## <a name="resources"></a><span data-ttu-id="9a75c-126">Ресурсы</span><span class="sxs-lookup"><span data-stu-id="9a75c-126">Resources</span></span>

-   [<span data-ttu-id="9a75c-127">ApplicationContentUriRules</span><span class="sxs-lookup"><span data-stu-id="9a75c-127">ApplicationContentUriRules</span></span>](/uwp/schemas/appxpackage/appxmanifestschema/element-applicationcontenturirules)
-   [<span data-ttu-id="9a75c-128"><iframe>\| <iframe> объект element</span><span class="sxs-lookup"><span data-stu-id="9a75c-128"><iframe> element \| <iframe> object</span></span>](https://msdn.microsoft.com/library/windows/apps/hh465955.aspx)
-   [<span data-ttu-id="9a75c-129">Класс WebView</span><span class="sxs-lookup"><span data-stu-id="9a75c-129">Webview class</span></span>](/uwp/api/Windows.UI.Xaml.Controls.WebView?view=winrt-19041)
-   [<span data-ttu-id="9a75c-130">WebView. Скриптнотифи, событие</span><span class="sxs-lookup"><span data-stu-id="9a75c-130">WebView.ScriptNotify event</span></span>](/uwp/api/Windows.UI.Xaml.Controls.WebView?view=winrt-19041)

 

 