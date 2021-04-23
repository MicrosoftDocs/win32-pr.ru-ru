---
description: Проверка подлинности подтверждает, кто вы.
ms.assetid: 5B058197-67B3-40DD-80D8-7BD8EE084CC9
title: Проверка подлинности для веб-страниц
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2e7c7bd37334f345ae16074c050b6b06c5fd644f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "103999150"
---
# <a name="authentication-for-web-pages"></a><span data-ttu-id="628ae-103">Проверка подлинности для веб-страниц</span><span class="sxs-lookup"><span data-stu-id="628ae-103">Authentication for web pages</span></span>

<span data-ttu-id="628ae-104">Проверка подлинности подтверждает, кто вы.</span><span class="sxs-lookup"><span data-stu-id="628ae-104">Authentication is proving who you are.</span></span>

<span data-ttu-id="628ae-105">**Цель:** Чтобы брокер веб-проверки подлинности отображался как часть приложения.</span><span class="sxs-lookup"><span data-stu-id="628ae-105">**Objective:** To have the web authentication broker appear as part of your app.</span></span>

## <a name="prerequisites"></a><span data-ttu-id="628ae-106">Предварительные требования</span><span class="sxs-lookup"><span data-stu-id="628ae-106">Prerequisites</span></span>

<span data-ttu-id="628ae-107">Нет</span><span class="sxs-lookup"><span data-stu-id="628ae-107">None</span></span>

<span data-ttu-id="628ae-108">**Время на выполнение:** 15 минут.</span><span class="sxs-lookup"><span data-stu-id="628ae-108">**Time to complete:** 15 minutes.</span></span>

## <a name="instructions"></a><span data-ttu-id="628ae-109">Инструкции</span><span class="sxs-lookup"><span data-stu-id="628ae-109">Instructions</span></span>

### <a name="1-getting-started"></a><span data-ttu-id="628ae-110">1. Начало работы</span><span class="sxs-lookup"><span data-stu-id="628ae-110">1. Getting started</span></span>

<span data-ttu-id="628ae-111">Запустите файл установки, чтобы установить веб-сайт Contoso в службы IIS 8 на локальном компьютере для размещения примеров файлов HTML и CSS.</span><span class="sxs-lookup"><span data-stu-id="628ae-111">Launch the setup file to install a Contoso website in Internet Information Services 8 on the local machine to host the sample HTML and CSS files.</span></span>

1.  <span data-ttu-id="628ae-112">Образцы файлов HTML и CSS будут установлены в каталог Program Files в Microsoft \\ contoso.</span><span class="sxs-lookup"><span data-stu-id="628ae-112">Sample HTML and CSS files will be installed to the program files directory under Microsoft\\Contoso.</span></span>
2.  <span data-ttu-id="628ae-113">Кроме того, приложение Магазина Windows "Fabrikam Social" будет распаковаться на рабочем столе.</span><span class="sxs-lookup"><span data-stu-id="628ae-113">In addition a "Fabrikam Social"Windows Store app will be unpackaged to the desktop.</span></span>

### <a name="2-getting-familiar"></a><span data-ttu-id="628ae-114">2. Знакомство</span><span class="sxs-lookup"><span data-stu-id="628ae-114">2. Getting familiar</span></span>

<span data-ttu-id="628ae-115">Чтобы получить представление о том, как выглядят образцы страниц в брокере веб-проверки подлинности, откройте файл решения Fabrikam социальных версий Visual Studio 11 в папке Fabrikam Social на рабочем столе.</span><span class="sxs-lookup"><span data-stu-id="628ae-115">To get a feel for what the sample pages look like in the Web Authentication Broker, open the Fabrikam Social Visual Studio 11 solution file in the "Fabrikam Social" folder on the desktop.</span></span>

1.  <span data-ttu-id="628ae-116">Запустите приложение и нажмите кнопку "запустить", чтобы открыть образцы страниц в брокере веб-проверки подлинности.</span><span class="sxs-lookup"><span data-stu-id="628ae-116">Run the application and hit "Launch" to bring up the sample pages in the Web Authentication Broker.</span></span>
2.  <span data-ttu-id="628ae-117">Размер приложения можно изменить на одну сторону или активировать, открыв некоторые данные в приложении.</span><span class="sxs-lookup"><span data-stu-id="628ae-117">The app can be resized to one side or activated by sharing some data to the application.</span></span>

### <a name="3-authentication"></a><span data-ttu-id="628ae-118">3. Проверка подлинности</span><span class="sxs-lookup"><span data-stu-id="628ae-118">3. Authentication</span></span>

<span data-ttu-id="628ae-119">Когда интерфейс API веб-проверки подлинности вызывается базовым приложением для подключения к поставщику "Contoso Social", отображается страница входа.</span><span class="sxs-lookup"><span data-stu-id="628ae-119">When the Web Auth API is invoked by the underlying app to connect to the provider, "Contoso Social", the login page is shown.</span></span> <span data-ttu-id="628ae-120">Эта страница предназначена для лучшего использования при быстром и гибком входе в систему.</span><span class="sxs-lookup"><span data-stu-id="628ae-120">This page is designed to be best at a fast and fluid login experience.</span></span> <span data-ttu-id="628ae-121">Он также предоставляет точки входа для некоторых других распространенных действий пользователя, таких как получение сведений о пароле, регистрация учетной записи и чтение инструкций по конфиденциальности и условиям, выполненным в браузере.</span><span class="sxs-lookup"><span data-stu-id="628ae-121">It also provides entry points to some other common user actions such as retrieving password details, signing up for an account, and reading statements on privacy and terms and conditions that are completed in the browser.</span></span> ![страница входа contoso](images/wab-figure8.png)

## <a name="summary-and-next-steps"></a><span data-ttu-id="628ae-123">Сводка и дальнейшие действия</span><span class="sxs-lookup"><span data-stu-id="628ae-123">Summary and next steps</span></span>

<span data-ttu-id="628ae-124">Сводный [учебник по проверке подлинности веб-страниц](tutorial-for-authenticating-web-pages.md)</span><span class="sxs-lookup"><span data-stu-id="628ae-124">Summary [Tutorial for authenticating web pages](tutorial-for-authenticating-web-pages.md)</span></span>

<span data-ttu-id="628ae-125">Следующая [авторизация для веб-страниц](authorization-for-web-pages.md)</span><span class="sxs-lookup"><span data-stu-id="628ae-125">Next [Authorization for web pages](authorization-for-web-pages.md)</span></span>

## <a name="related-topics"></a><span data-ttu-id="628ae-126">См. также</span><span class="sxs-lookup"><span data-stu-id="628ae-126">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="628ae-127">Рекомендации по разработке веб-страниц</span><span class="sxs-lookup"><span data-stu-id="628ae-127">Considerations for the web page development</span></span>](considerations-for-the-web-page-development.md)
</dt> <dt>

[<span data-ttu-id="628ae-128">Пример приложения SDK брокера веб-проверки подлинности</span><span class="sxs-lookup"><span data-stu-id="628ae-128">Web Authentication Broker SDK sample app</span></span>](https://github.com/microsoft/Windows-universal-samples/tree/master/Samples/WebAuthenticationBroker)
</dt> <dt>

[<span data-ttu-id="628ae-129">**Windows.Security.Authentication.Web**</span><span class="sxs-lookup"><span data-stu-id="628ae-129">**Windows.Security.Authentication.Web**</span></span>](/uwp/api/Windows.Security.Authentication.Web)
</dt> </dl>

 

 
