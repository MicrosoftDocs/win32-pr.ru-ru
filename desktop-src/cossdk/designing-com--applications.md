---
description: Независимо от того, разрабатываете ли вы приложение для выполнения интерактивной торговли, отслеживания информации, доступа к данным в устаревших системах, обмена ресурсами, планирования и управления знаниями, или важного бизнес-приложения, вы можете усовершенствовать и оптимизировать разработку среднего уровня, интегрируя службы COM+. Самый распространенный способ сделать это — сгруппировать компоненты в приложения COM+.
ms.assetid: 75002a82-5300-4758-9fe4-56537af5168c
title: Проектирование приложений COM+
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2a1b28aa9e8b1658855ca0ef5134722d54650962
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104072397"
---
# <a name="designing-com-applications"></a><span data-ttu-id="3f1cf-104">Проектирование приложений COM+</span><span class="sxs-lookup"><span data-stu-id="3f1cf-104">Designing COM+ Applications</span></span>

<span data-ttu-id="3f1cf-105">Независимо от того, разрабатываете ли вы приложение для выполнения интерактивной торговли, отслеживания информации, доступа к данным в устаревших системах, обмена ресурсами, планирования и управления знаниями, или важного бизнес-приложения, вы можете усовершенствовать и оптимизировать разработку среднего уровня, интегрируя службы COM+.</span><span class="sxs-lookup"><span data-stu-id="3f1cf-105">Whether you are designing an application for conducting online commerce, tracking information, accessing data in legacy systems, messaging, resource planning, publishing and knowledge management, or a critical LOB (line of business) application, you can enhance and streamline your middle-tier design by integrating COM+ services.</span></span> <span data-ttu-id="3f1cf-106">Самый распространенный способ сделать это — сгруппировать компоненты в приложения COM+.</span><span class="sxs-lookup"><span data-stu-id="3f1cf-106">The most common way to do this is by grouping components into COM+ applications.</span></span>

<span data-ttu-id="3f1cf-107">Хотя полная проверка методологии для использования COM+ во всех ситуациях выходит за рамки этого документа, в следующих разделах представлены сведения, которые можно использовать при создании приложения COM+.</span><span class="sxs-lookup"><span data-stu-id="3f1cf-107">While a complete methodology review for using COM+ in all situations is beyond the scope of this document, the following topics present information you can use when creating a COM+ application.</span></span>



| <span data-ttu-id="3f1cf-108">Раздел</span><span class="sxs-lookup"><span data-stu-id="3f1cf-108">Topic</span></span>                                                                                                                                     | <span data-ttu-id="3f1cf-109">Описание</span><span class="sxs-lookup"><span data-stu-id="3f1cf-109">Description</span></span>                                                                                                                         |
|-------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="3f1cf-110">Предположения и принципы разработки COM+</span><span class="sxs-lookup"><span data-stu-id="3f1cf-110">COM+ Design Assumptions and Principles</span></span>](com--design-assumptions-and-principles.md)<br/>                                           | <span data-ttu-id="3f1cf-111">Содержит допущения и принципы, необходимые для понимания того, как создать распределенное приложение с помощью COM+.</span><span class="sxs-lookup"><span data-stu-id="3f1cf-111">Introduces the assumptions and principles necessary to understanding how to create a distributed application using COM+.</span></span><br/> |
| [<span data-ttu-id="3f1cf-112">Другие средства Майкрософт для создания распределенных приложений</span><span class="sxs-lookup"><span data-stu-id="3f1cf-112">Other Microsoft Tools for Building Distributed Applications</span></span>](other-microsoft-tools-for-building-distributed-applications.md)<br/> | <span data-ttu-id="3f1cf-113">Предлагает технологии Майкрософт, которые можно использовать совместно с COM+ при создании распределенных приложений.</span><span class="sxs-lookup"><span data-stu-id="3f1cf-113">Suggests Microsoft technologies you can use in conjunction with COM+ when building distributed applications.</span></span><br/>             |
| [<span data-ttu-id="3f1cf-114">Проектирование приложения COM+ с помощью UML</span><span class="sxs-lookup"><span data-stu-id="3f1cf-114">Designing the COM+ Application Using UML</span></span>](designing-the-com--application-using-uml.md)<br/>                                       | <span data-ttu-id="3f1cf-115">Описывает предпочтительный метод проектирования для создания приложений COM+.</span><span class="sxs-lookup"><span data-stu-id="3f1cf-115">Discusses the preferred design method for creating COM+ applications.</span></span> <br/>                                                   |
| [<span data-ttu-id="3f1cf-116">Общие рекомендации по проектированию для использования COM+</span><span class="sxs-lookup"><span data-stu-id="3f1cf-116">General Design Tips for Using COM+</span></span>](general-design-tips-for-using-com-.md)<br/>                                                   | <span data-ttu-id="3f1cf-117">Содержит советы по проектированию приложения COM+.</span><span class="sxs-lookup"><span data-stu-id="3f1cf-117">Presents tips on designing a COM+ application.</span></span> <br/>                                                                          |
| [<span data-ttu-id="3f1cf-118">Оптимизация взаимодействия с уровнем бизнес-логики COM+</span><span class="sxs-lookup"><span data-stu-id="3f1cf-118">Optimizing Interactions with the COM+ Business Logic Tier</span></span>](optimizing-interactions-with-the-com--business-logic-tier.md)<br/>     | <span data-ttu-id="3f1cf-119">Рассматриваются некоторые рекомендации по обмену данными между уровнем бизнес-логики и уровнями представления и данных.</span><span class="sxs-lookup"><span data-stu-id="3f1cf-119">Covers some of the best practices for communication between the business logic tier and the presentation and data tiers.</span></span><br/> |



 

 

 




