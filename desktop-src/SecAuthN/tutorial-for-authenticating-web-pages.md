---
description: В этом учебнике рассматриваются различные аспекты, с которыми должны заботиться веб-разработчики при разработке страниц для потока веб-авторизации в Windows 8. В этом разделе в этом примере демонстрируется поток авторизации из двух страниц.
ms.assetid: A26E09EF-6C7A-4F75-89A7-76086F63F3B1
title: Руководство по проверке подлинности веб-страниц
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a1c6fc6482c5e6dfaf89a9fc9732783f5f088b4d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "105651019"
---
# <a name="tutorial-for-authenticating-web-pages"></a><span data-ttu-id="70d67-104">Руководство по проверке подлинности веб-страниц</span><span class="sxs-lookup"><span data-stu-id="70d67-104">Tutorial for authenticating web pages</span></span>

<span data-ttu-id="70d67-105">В этом учебнике рассматриваются различные аспекты, с которыми должны заботиться веб-разработчики при разработке страниц для потока веб-авторизации в Windows 8.</span><span class="sxs-lookup"><span data-stu-id="70d67-105">This tutorial highlights the different aspects that web developers should care about when designing pages for the web authorization flow for Windows 8.</span></span> <span data-ttu-id="70d67-106">В этом разделе в этом примере демонстрируется поток авторизации из двух страниц.</span><span class="sxs-lookup"><span data-stu-id="70d67-106">This section This sample demonstrates a two-page authorization flow.</span></span>

<span data-ttu-id="70d67-107">**Цель:** Целью примера не является предварительное описание макета или визуального дизайна о том, что у каждого поставщика наверняка есть уникальная точка зрения, но для вызова нескольких областей, на которые стоит инвестиции, в качестве первого класса для Windows 8.</span><span class="sxs-lookup"><span data-stu-id="70d67-107">**Objective:** The goal of the sample is not to be prescriptive about the layout or visual design that each provider will certainly have a unique point of view on, but to call out a few areas worth investing in to have a first-class Microsoft design style experience for Windows 8.</span></span>

## <a name="prerequisites"></a><span data-ttu-id="70d67-108">Предварительные условия</span><span class="sxs-lookup"><span data-stu-id="70d67-108">Prerequisites</span></span>

<span data-ttu-id="70d67-109">Чтобы использовать API брокера веб-проверки подлинности, вам потребуется:</span><span class="sxs-lookup"><span data-stu-id="70d67-109">In order to use web authentication broker APIs, you need:</span></span>

-   <span data-ttu-id="70d67-110">Windows 8 (только x86 или AMD64)</span><span class="sxs-lookup"><span data-stu-id="70d67-110">Windows 8 (x86 or amd64 only)</span></span>
-   <span data-ttu-id="70d67-111">Microsoft службы IIS (IIS) следует установить из панели управления в разделе "программы и компоненты" и с помощью параметра "Включение или отключение компонентов Windows".</span><span class="sxs-lookup"><span data-stu-id="70d67-111">Microsoft Internet Information Services (IIS) should be installed from the Control Panel under "Programs and Features" and using the "Turn Windows features on or off" option.</span></span>

<span data-ttu-id="70d67-112">**Общее время выполнения:** 2 минуты.</span><span class="sxs-lookup"><span data-stu-id="70d67-112">**Total time to complete:** 2 minutes.</span></span>

## <a name="where-to-go-from-here"></a><span data-ttu-id="70d67-113">Дальнейшие действия</span><span class="sxs-lookup"><span data-stu-id="70d67-113">Where to go from here</span></span>

<span data-ttu-id="70d67-114">Следующая [Проверка подлинности для веб-страниц](authentication-for-web-pages.md)</span><span class="sxs-lookup"><span data-stu-id="70d67-114">Next [Authentication for web pages](authentication-for-web-pages.md)</span></span>

## <a name="related-topics"></a><span data-ttu-id="70d67-115">См. также</span><span class="sxs-lookup"><span data-stu-id="70d67-115">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="70d67-116">Рекомендации по разработке веб-страниц</span><span class="sxs-lookup"><span data-stu-id="70d67-116">Considerations for the web page development</span></span>](considerations-for-the-web-page-development.md)
</dt> <dt>

[<span data-ttu-id="70d67-117">Пример приложения SDK брокера веб-проверки подлинности</span><span class="sxs-lookup"><span data-stu-id="70d67-117">Web Authentication Broker SDK sample app</span></span>](https://github.com/microsoft/Windows-universal-samples/tree/master/Samples/WebAuthenticationBroker)
</dt> <dt>

[<span data-ttu-id="70d67-118">**Windows.Security.Authentication.Web**</span><span class="sxs-lookup"><span data-stu-id="70d67-118">**Windows.Security.Authentication.Web**</span></span>](/uwp/api/Windows.Security.Authentication.Web?view=winrt-19041)
</dt> </dl>

 

 
