---
description: Авторизация задает, к каким ресурсам у вас есть доступ.
ms.assetid: DD6836EE-DF73-4A07-9DF1-0F5A959DDE8F
title: Авторизация для веб-страниц
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 88c26e9bc8333d74d18989c5c581cc54054a29ab
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "103898302"
---
# <a name="authorization-for-web-pages"></a><span data-ttu-id="f7d30-103">Авторизация для веб-страниц</span><span class="sxs-lookup"><span data-stu-id="f7d30-103">Authorization for web pages</span></span>

<span data-ttu-id="f7d30-104">Авторизация задает, к каким ресурсам у вас есть доступ.</span><span class="sxs-lookup"><span data-stu-id="f7d30-104">Authorization sets what resources you have access to.</span></span>

<span data-ttu-id="f7d30-105">**Цель:** Чтобы разрешить пользователям доступ к приложению.</span><span class="sxs-lookup"><span data-stu-id="f7d30-105">**Objective:** To allow users access to your app.</span></span>

## <a name="prerequisites"></a><span data-ttu-id="f7d30-106">Предварительные требования</span><span class="sxs-lookup"><span data-stu-id="f7d30-106">Prerequisites</span></span>

<span data-ttu-id="f7d30-107">Нет</span><span class="sxs-lookup"><span data-stu-id="f7d30-107">None</span></span>

<span data-ttu-id="f7d30-108">**Время на выполнение:** 2 минуты.</span><span class="sxs-lookup"><span data-stu-id="f7d30-108">**Time to complete:** 2 minutes.</span></span>

## <a name="instructions"></a><span data-ttu-id="f7d30-109">Инструкции</span><span class="sxs-lookup"><span data-stu-id="f7d30-109">Instructions</span></span>

### <a name="1-authorization"></a><span data-ttu-id="f7d30-110">1. Авторизация</span><span class="sxs-lookup"><span data-stu-id="f7d30-110">1. Authorization</span></span>

<span data-ttu-id="f7d30-111">Когда пользователь вводит свои учетные данные и нажимает кнопку "вход", отображается страница разрешений.</span><span class="sxs-lookup"><span data-stu-id="f7d30-111">When the user enters their credentials and clicks the Login button, the permissions page is shown.</span></span> <span data-ttu-id="f7d30-112">Эта страница лучше позволяет пользователям управлять детализированными разрешениями, предоставляя приложению доступ к данным contoso.</span><span class="sxs-lookup"><span data-stu-id="f7d30-112">This page is best at allowing users to control granular permissions in granting the app to access to Contoso’s data.</span></span> ![Страница разрешений Contoso](images/wab-figure9.png)

### <a name="2-how-to-use-the-sample"></a><span data-ttu-id="f7d30-114">2. Использование примера</span><span class="sxs-lookup"><span data-stu-id="f7d30-114">2. How to use the sample</span></span>

<span data-ttu-id="f7d30-115">Необходимо знать следующие файлы HTML и CSS.</span><span class="sxs-lookup"><span data-stu-id="f7d30-115">You need to know about the following HTML and CSS files.</span></span>

1.  <span data-ttu-id="f7d30-116">Следующие HTML-файлы соответствуют двум страницам в потоке веб-авторизации.</span><span class="sxs-lookup"><span data-stu-id="f7d30-116">The following HTML files correspond to the two pages in the web authorization flow</span></span>
    -   <span data-ttu-id="f7d30-117">WebAuthLogin.html — пример HTML-кода для страницы входа</span><span class="sxs-lookup"><span data-stu-id="f7d30-117">WebAuthLogin.html – sample HTML for the login page</span></span>
    -   <span data-ttu-id="f7d30-118">WebAuthPermissions.html — пример HTML-кода для страницы разрешений</span><span class="sxs-lookup"><span data-stu-id="f7d30-118">WebAuthPermissions.html – sample HTML for the permissions page</span></span>
2.  <span data-ttu-id="f7d30-119">Файлы CSS содержат стили Windows 8, помогающие создать веб-страницу приложения для Магазина Windows.</span><span class="sxs-lookup"><span data-stu-id="f7d30-119">The CSS files contain Windows 8 styles to help create a Windows Store app web page.</span></span>
    -   <span data-ttu-id="f7d30-120">Уи-Лигхт. CSS — она была получена из базовой таблицы стилей для элементов управления Windows 8.</span><span class="sxs-lookup"><span data-stu-id="f7d30-120">ui-light.css – this has been derived from the base style sheet for Windows 8 controls.</span></span>
    -   <span data-ttu-id="f7d30-121">Уи-вебаус. CSS — обеспечивает добавочное Оформление для оптимизации макета страниц веб-аутентификации.</span><span class="sxs-lookup"><span data-stu-id="f7d30-121">ui-webauth.css – this provides incremental styling for optimizing layout for web auth pages.</span></span>
    -   <span data-ttu-id="f7d30-122">семе-Колорс. CSS — обеспечивает добавочный стиль для переопределения контрастных цветов по умолчанию для элементов управления с цветом торговой марки поставщика.</span><span class="sxs-lookup"><span data-stu-id="f7d30-122">theme-colors.css – this provides the incremental styling to override default accent colors of controls with the provider’s brand color.</span></span>

## <a name="summary-and-next-steps"></a><span data-ttu-id="f7d30-123">Сводка и дальнейшие действия</span><span class="sxs-lookup"><span data-stu-id="f7d30-123">Summary and next steps</span></span>

<span data-ttu-id="f7d30-124">Сводный [учебник по проверке подлинности веб-страниц](tutorial-for-authenticating-web-pages.md)</span><span class="sxs-lookup"><span data-stu-id="f7d30-124">Summary [Tutorial for authenticating web pages](tutorial-for-authenticating-web-pages.md)</span></span>

<span data-ttu-id="f7d30-125">Следующие рекомендации [по проектированию веб-страниц проверки подлинности](best-practices-for-designing-authentication-web-pages.md)</span><span class="sxs-lookup"><span data-stu-id="f7d30-125">Next [Best practices for designing authentication web pages](best-practices-for-designing-authentication-web-pages.md)</span></span>

## <a name="related-topics"></a><span data-ttu-id="f7d30-126">См. также</span><span class="sxs-lookup"><span data-stu-id="f7d30-126">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="f7d30-127">Рекомендации по разработке веб-страниц</span><span class="sxs-lookup"><span data-stu-id="f7d30-127">Considerations for the web page development</span></span>](considerations-for-the-web-page-development.md)
</dt> <dt>

[<span data-ttu-id="f7d30-128">Пример приложения SDK брокера веб-проверки подлинности</span><span class="sxs-lookup"><span data-stu-id="f7d30-128">Web Authentication Broker SDK sample app</span></span>](https://github.com/microsoft/Windows-universal-samples/tree/master/Samples/WebAuthenticationBroker)
</dt> <dt>

[<span data-ttu-id="f7d30-129">**Windows.Security.Authentication.Web**</span><span class="sxs-lookup"><span data-stu-id="f7d30-129">**Windows.Security.Authentication.Web**</span></span>](/uwp/api/Windows.Security.Authentication.Web)
</dt> </dl>

 

 
