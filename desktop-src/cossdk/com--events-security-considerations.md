---
description: При использовании службы событий COM+ можно выполнить действия, чтобы убедиться, что все конфиденциальные сведения, содержащиеся в событии, не скомпрометированы.
ms.assetid: 1f8faea0-afc2-4999-a962-d6fd10307d6c
title: Вопросы безопасности событий COM+
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1e8f5c7dada980046627e9b778fd56e3e2727060
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "103990816"
---
# <a name="com-events-security-considerations"></a><span data-ttu-id="d6072-103">Вопросы безопасности событий COM+</span><span class="sxs-lookup"><span data-stu-id="d6072-103">COM+ Events Security Considerations</span></span>

<span data-ttu-id="d6072-104">При использовании службы событий COM+ можно выполнить действия, чтобы убедиться, что все конфиденциальные сведения, содержащиеся в событии, не скомпрометированы.</span><span class="sxs-lookup"><span data-stu-id="d6072-104">When using the COM+ events service, there are steps you can take to ensure that any sensitive information contained in an event is not compromised.</span></span>

<span data-ttu-id="d6072-105">Издатели событий должны иметь в виду, что любая сторона, которая может записывать в каталог COM+, может подписаться на ваши события.</span><span class="sxs-lookup"><span data-stu-id="d6072-105">Event publishers should keep in mind that any party that can write to your COM+ catalog can subscribe to your events.</span></span> <span data-ttu-id="d6072-106">Таким образом, если информация, содержащаяся в объекте класса событий, является конфиденциальной, следует использовать средство администрирования служб компонентов, чтобы убедиться, что связь с подписчиками шифруется для приложения, содержащего компоненты класса событий.</span><span class="sxs-lookup"><span data-stu-id="d6072-106">Therefore, if the information contained in an event class object is sensitive, you should use the Component Services administration tool to verify that communications with subscribers are encrypted for the application that contains the event class components.</span></span> <span data-ttu-id="d6072-107">(На вкладке **Безопасность** на странице свойств приложения COM+ выберите параметр **Конфиденциальность пакетов** в качестве **уровня проверки подлинности для вызовов** .) Кроме того, следует использовать [фильтры событий](filtering-events-in-com-.md) , чтобы гарантировать, что события доставляются только соответствующим подписчикам.</span><span class="sxs-lookup"><span data-stu-id="d6072-107">(On the **Security** tab of the COM+ application property sheet, select **Packet Privacy** as the **Authentication Level for Calls** setting.) Also, you should use [event filters](filtering-events-in-com-.md) to help ensure that events are delivered only to the appropriate subscribers.</span></span>

<span data-ttu-id="d6072-108">Подписчики на события должны иметь в виду, что вредоносная сторона с доступом к вашей сети и сведения об объекте класса событий могут создавать ложные события.</span><span class="sxs-lookup"><span data-stu-id="d6072-108">Event subscribers should keep in mind that a malicious party with access to your network and knowledge of your event class object could create false events.</span></span> <span data-ttu-id="d6072-109">Поэтому следует использовать [безопасность на основе ролей](role-based-security-administration.md) , чтобы убедиться, что вызывающие методы объекта класса событий имеют соответствующие учетные данные для выполнения действий, описанных в реализации.</span><span class="sxs-lookup"><span data-stu-id="d6072-109">You should therefore use [role-based security](role-based-security-administration.md) to help ensure that callers of your event class object's methods have appropriate credentials to perform the actions described by your implementation.</span></span>

<span data-ttu-id="d6072-110">Для защиты издателей и подписчиков используйте службу событий COM+ в частной сети доверенных узлов, изолированных от Интернета брандмауэром.</span><span class="sxs-lookup"><span data-stu-id="d6072-110">To help protect both publishers and subscribers, use the COM+ Events service on a private network of trusted hosts that is isolated from the Internet by a firewall.</span></span>

## <a name="related-topics"></a><span data-ttu-id="d6072-111">См. также</span><span class="sxs-lookup"><span data-stu-id="d6072-111">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="d6072-112">Безопасность COM+</span><span class="sxs-lookup"><span data-stu-id="d6072-112">COM+ Security</span></span>](com--security.md)
</dt> <dt>

[<span data-ttu-id="d6072-113">Фильтрация событий в COM+</span><span class="sxs-lookup"><span data-stu-id="d6072-113">Filtering Events in COM+</span></span>](filtering-events-in-com-.md)
</dt> <dt>

[<span data-ttu-id="d6072-114">Объект класса событий COM+</span><span class="sxs-lookup"><span data-stu-id="d6072-114">The COM+ Event Class Object</span></span>](the-com--event-class-object.md)
</dt> </dl>

 

 



