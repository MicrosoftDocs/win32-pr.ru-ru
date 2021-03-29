---
description: Рекомендации для веб-разработчиков и поставщиков в Интернете для создания веб-страниц, предназначенных для интерфейсов API брокера веб-проверки подлинности Windows 8 для возможностей единого входа (SSO).
ms.assetid: E2AECE26-9649-41CB-9808-4F8171C707C3
title: Руководство по началу работы для поставщиков услуг Интернета, интегрированных с API брокера веб-проверки подлинности
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 842f3c562d2ad288efaecec82f8da8ca771886a5
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "103911883"
---
# <a name="getting-started-guidance-for-online-providers-integrating-with-the-web-authentication-broker-apis"></a><span data-ttu-id="2aa0e-103">Руководство по началу работы для поставщиков услуг Интернета, интегрированных с API брокера веб-проверки подлинности</span><span class="sxs-lookup"><span data-stu-id="2aa0e-103">Getting started guidance for online providers integrating with the Web Authentication Broker APIs</span></span>

<span data-ttu-id="2aa0e-104">В этом разделе рассказывается о веб-разработчиках и сетевых поставщиках для создания веб-страниц, предназначенных для API брокера веб-проверки подлинности Windows 8.</span><span class="sxs-lookup"><span data-stu-id="2aa0e-104">This section guides web developers and online providers for creating web pages tailored for the Windows 8 Web Authentication Broker APIs.</span></span> <span data-ttu-id="2aa0e-105">Он предоставляет визуальные и интерактивные рекомендации для полноценного взаимодействия с пользователем на веб-странице, а также включает возможности единого входа (SSO).</span><span class="sxs-lookup"><span data-stu-id="2aa0e-105">It provides the visual and interactive recommendations for an end-to-end user experience of the web page as well as how to enable single sign-on (SSO) capabilities.</span></span>

## <a name="in-this-section"></a><span data-ttu-id="2aa0e-106">В этом разделе</span><span class="sxs-lookup"><span data-stu-id="2aa0e-106">In this section</span></span>



| <span data-ttu-id="2aa0e-107">Раздел</span><span class="sxs-lookup"><span data-stu-id="2aa0e-107">Topic</span></span>                                                                                                     | <span data-ttu-id="2aa0e-108">Описание</span><span class="sxs-lookup"><span data-stu-id="2aa0e-108">Description</span></span>                                                                                                                                                                                                                                                                    |
|-----------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="2aa0e-109">Рекомендации по разработке веб-страниц</span><span class="sxs-lookup"><span data-stu-id="2aa0e-109">Considerations for the web page development</span></span>](considerations-for-the-web-page-development.md)<br/> | <span data-ttu-id="2aa0e-110">Посредник веб-аутентификации основан на тех же технологиях, что и Power Internet Explorer в Windows.</span><span class="sxs-lookup"><span data-stu-id="2aa0e-110">Web Authentication Broker is built on the top of the same technologies that power Internet Explorer in Windows.</span></span> <span data-ttu-id="2aa0e-111">Однако из-за специального назначения этого компонента некоторые функции Internet Explorer были отключены или заблокированы для конкретной конфигурации.</span><span class="sxs-lookup"><span data-stu-id="2aa0e-111">However, due to a very special purpose of this component some features of the Internet Explorer were disabled or locked to specific configuration.</span></span> <br/> |
| [<span data-ttu-id="2aa0e-112">Настройка элементов пользовательского интерфейса</span><span class="sxs-lookup"><span data-stu-id="2aa0e-112">How to customize the UI elements</span></span>](how-to-customize-the-ui-elements.md)<br/>                       | <span data-ttu-id="2aa0e-113">Веб-страница настраивает пользовательский интерфейс с заголовком, значком и цветом заголовка с помощью тегов метаданных, определенных на веб-странице.</span><span class="sxs-lookup"><span data-stu-id="2aa0e-113">A web page customizes the user interface (UI) with the title, icon, and header color by using metadata tags defined on the web page.</span></span><br/>                                                                                                                                |
| [<span data-ttu-id="2aa0e-114">Руководство по проверке подлинности веб-страниц</span><span class="sxs-lookup"><span data-stu-id="2aa0e-114">Tutorial for authenticating web pages</span></span>](tutorial-for-authenticating-web-pages.md)<br/>             |                                                                                                                                                                                                                                                                                |
| [<span data-ttu-id="2aa0e-115">Неполадки при веб-аутентификации</span><span class="sxs-lookup"><span data-stu-id="2aa0e-115">Web authentication problems</span></span>](web-authentication-problems.md)<br/>                                 | <span data-ttu-id="2aa0e-116">В этом разделе описаны рекомендации по устранению неполадок при использовании API посредника веб-проверки подлинности для веб-страниц.</span><span class="sxs-lookup"><span data-stu-id="2aa0e-116">This topic describes troubleshooting tips for using the Web Authentication Broker APIs for your web pages.</span></span><br/>                                                                                                                                                          |
| [<span data-ttu-id="2aa0e-117">Вопросы и ответы по брокеру веб-проверки подлинности</span><span class="sxs-lookup"><span data-stu-id="2aa0e-117">FAQ for Web Authentication Broker</span></span>](faq-for-web-authentication-broker.md)<br/>                     | <span data-ttu-id="2aa0e-118">Часто задаваемые вопросы о брокере веб-проверки подлинности.</span><span class="sxs-lookup"><span data-stu-id="2aa0e-118">Frequently asked questions for Web Authentication Broker.</span></span><br/>                                                                                                                                                                                                           |



 

## <a name="related-topics"></a><span data-ttu-id="2aa0e-119">См. также</span><span class="sxs-lookup"><span data-stu-id="2aa0e-119">Related topics</span></span>

<dl> <dt>

<span data-ttu-id="2aa0e-120">[Обзор брокера веб-проверки подлинности](/previous-versions/windows/apps/hh750287(v=win.10))</span><span class="sxs-lookup"><span data-stu-id="2aa0e-120">[Web authentication broker overview](/previous-versions/windows/apps/hh750287(v=win.10))</span></span>
</dt> <dt>

[<span data-ttu-id="2aa0e-121">Пример приложения SDK брокера веб-проверки подлинности</span><span class="sxs-lookup"><span data-stu-id="2aa0e-121">Web Authentication Broker SDK sample app</span></span>](https://github.com/microsoft/Windows-universal-samples/tree/master/Samples/WebAuthenticationBroker)
</dt> <dt>

[<span data-ttu-id="2aa0e-122">**Windows.Security.Authentication.Web**</span><span class="sxs-lookup"><span data-stu-id="2aa0e-122">**Windows.Security.Authentication.Web**</span></span>](/uwp/api/Windows.Security.Authentication.Web)
</dt> </dl>

 

