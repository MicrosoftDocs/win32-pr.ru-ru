---
description: Часто задаваемые вопросы о брокере веб-проверки подлинности.
ms.assetid: 49ACB2E3-CF57-4D8E-9670-E7C18A06F76A
title: Вопросы и ответы по брокеру веб-проверки подлинности
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 95942a32bba86f7b2ccb12264cc1a50419b248a5
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "104545890"
---
# <a name="faq-for-web-authentication-broker"></a><span data-ttu-id="59173-103">Вопросы и ответы по брокеру веб-проверки подлинности</span><span class="sxs-lookup"><span data-stu-id="59173-103">FAQ for Web Authentication Broker</span></span>

<span data-ttu-id="59173-104">Часто задаваемые вопросы о брокере веб-проверки подлинности.</span><span class="sxs-lookup"><span data-stu-id="59173-104">Frequently asked questions for Web Authentication Broker.</span></span>



| <span data-ttu-id="59173-105">Вопрос</span><span class="sxs-lookup"><span data-stu-id="59173-105">Question</span></span>                                                                                                    | <span data-ttu-id="59173-106">Ответ</span><span class="sxs-lookup"><span data-stu-id="59173-106">Answer</span></span>                                                                                                                                                                                                            |
|-------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="59173-107">Как убедиться, что страница https://работает с брокером веб-проверки подлинности?</span><span class="sxs-lookup"><span data-stu-id="59173-107">How can I make sure that my https:// page works with the Web Authentication Broker?</span></span>                         | <span data-ttu-id="59173-108">Попробуйте загрузить страницу в Windows Internet Explorer, прежде чем пытаться выполнить ее с помощью брокера веб-проверки подлинности.</span><span class="sxs-lookup"><span data-stu-id="59173-108">Try loading the page in Windows Internet Explorer before trying it with Web Authentication Broker.</span></span> <span data-ttu-id="59173-109">Если веб-страница загружается без ошибок, она также будет правильно отображена брокером веб-аутентификации.</span><span class="sxs-lookup"><span data-stu-id="59173-109">If your web page loads with no errors, it will be rendered correctly by the Web Authentication Broker as well.</span></span> |
| <span data-ttu-id="59173-110">В случае ошибки будет ли отображаться код ошибки для пользователя?</span><span class="sxs-lookup"><span data-stu-id="59173-110">In case of an error, will the error codes be displayed to the user?</span></span>                                         | <span data-ttu-id="59173-111">Хотя пользователю будет выводиться страница ошибки, код ошибки не отображается.</span><span class="sxs-lookup"><span data-stu-id="59173-111">While an error page will be displayed to the user, the underlying error code is not shown.</span></span> <span data-ttu-id="59173-112">Он возвращается только приложению.</span><span class="sxs-lookup"><span data-stu-id="59173-112">It is only returned to the app.</span></span> <span data-ttu-id="59173-113">Кроме того, можно также использовать операционные журналы.</span><span class="sxs-lookup"><span data-stu-id="59173-113">Alternately, you can also use the operational logs.</span></span>                                    |
| <span data-ttu-id="59173-114">Как найти дополнительные сведения об обнаруженной ошибке?</span><span class="sxs-lookup"><span data-stu-id="59173-114">How can I find more details on the error encountered?</span></span>                                                       | <span data-ttu-id="59173-115">Для получения дополнительных сведений используйте Операционные журналы.</span><span class="sxs-lookup"><span data-stu-id="59173-115">Use the operational logs for details.</span></span>                                                                                                                                                                             |
| <span data-ttu-id="59173-116">Использует ли контейнер приложения единого входа (SSO) свои файлы cookie в Internet Explorer или других браузерах?</span><span class="sxs-lookup"><span data-stu-id="59173-116">Does the single sign-on (SSO) app container share its cookies with the Internet Explorer or other browsers?</span></span> | <span data-ttu-id="59173-117">Нет.</span><span class="sxs-lookup"><span data-stu-id="59173-117">No.</span></span>                                                                                                                                                                                                               |



 

## <a name="related-topics"></a><span data-ttu-id="59173-118">См. также</span><span class="sxs-lookup"><span data-stu-id="59173-118">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="59173-119">Рекомендации по разработке веб-страниц</span><span class="sxs-lookup"><span data-stu-id="59173-119">Considerations for the web page development</span></span>](considerations-for-the-web-page-development.md)
</dt> <dt>

[<span data-ttu-id="59173-120">Пример приложения SDK брокера веб-проверки подлинности</span><span class="sxs-lookup"><span data-stu-id="59173-120">Web Authentication Broker SDK sample app</span></span>](https://github.com/microsoft/Windows-universal-samples/tree/master/Samples/WebAuthenticationBroker)
</dt> <dt>

[<span data-ttu-id="59173-121">**Windows.Security.Authentication.Web**</span><span class="sxs-lookup"><span data-stu-id="59173-121">**Windows.Security.Authentication.Web**</span></span>](/uwp/api/Windows.Security.Authentication.Web)
</dt> </dl>

 

 
