---
description: Основные рекомендации по проектированию приложений COM+
ms.assetid: 2d08bd05-5b0c-480c-91fd-b2bf321fc21e
title: Основные рекомендации по проектированию приложений COM+
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7b6552022c3a9c2f50172164d1ed60811c5272e0
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104142019"
---
# <a name="basic-guidelines-for-designing-com-applications"></a><span data-ttu-id="ee405-103">Основные рекомендации по проектированию приложений COM+</span><span class="sxs-lookup"><span data-stu-id="ee405-103">Basic Guidelines for Designing COM+ Applications</span></span>

<span data-ttu-id="ee405-104">Чтобы воспользоваться всеми преимуществами COM+, существует несколько основных рекомендаций, которые можно использовать при создании приложения:</span><span class="sxs-lookup"><span data-stu-id="ee405-104">To take full advantage of COM+, there are a few basic guidelines you can use when creating an application:</span></span>

-   <span data-ttu-id="ee405-105">**Моделирование устойчивого состояния в качестве схемы базы данных с помощью выбранного инструмента для работы с базами данных.**</span><span class="sxs-lookup"><span data-stu-id="ee405-105">**Model your durable state as a database schema, using your database tool of choice.**</span></span> <span data-ttu-id="ee405-106">Почти все приложения должны поддерживать устойчивое состояние.</span><span class="sxs-lookup"><span data-stu-id="ee405-106">Almost every application needs to maintain durable state.</span></span> <span data-ttu-id="ee405-107">Базы данных предоставляют службы, необходимые для создания долговременного и масштабируемого хранилища состояния.</span><span class="sxs-lookup"><span data-stu-id="ee405-107">Databases provide the services needed to create durable and scalable storage of state.</span></span> <span data-ttu-id="ee405-108">Таким образом, первым шагом в создании приложения COM+ является моделирование устойчивого состояния приложения в соответствии со схемой базы данных.</span><span class="sxs-lookup"><span data-stu-id="ee405-108">Therefore, the first step in creating a COM+ application is to model the durable state of your application as some sort of database schema.</span></span> <span data-ttu-id="ee405-109">Это не имеет значения, какая база данных используется. Большинство коммерческих баз данных совместимы с COM+.</span><span class="sxs-lookup"><span data-stu-id="ee405-109">It doesn't really matter what database you use; most commercial databases are compatible with COM+.</span></span> <span data-ttu-id="ee405-110">Microsoft SQL Server — хороший пример одного решения, которое можно использовать.</span><span class="sxs-lookup"><span data-stu-id="ee405-110">Microsoft SQL Server is a good example of one solution you could use.</span></span>

-   <span data-ttu-id="ee405-111">**Моделирование логики приложения COM+ как набора интерфейсов COM.**</span><span class="sxs-lookup"><span data-stu-id="ee405-111">**Model the logic of your COM+ application as a set of COM interfaces.**</span></span> <span data-ttu-id="ee405-112">После создания схемы, которая представляет сведения о состоянии приложения, моделируют взаимоизменения, происходящие в приложении как интерфейсы COM.</span><span class="sxs-lookup"><span data-stu-id="ee405-112">Once you have a schema that represents the state information of the application, model the interchanges that happen in the application as COM interfaces.</span></span> <span data-ttu-id="ee405-113">Эти интерфейсы моделируют поведение приложения.</span><span class="sxs-lookup"><span data-stu-id="ee405-113">These interfaces will model the behavior of the application.</span></span> <span data-ttu-id="ee405-114">Это также этап разработки, когда необходимо определить, какие службы COM+ лучше подходят для вашего приложения.</span><span class="sxs-lookup"><span data-stu-id="ee405-114">This is also the development stage when you should determine which COM+ services work best for your application.</span></span>

-   <span data-ttu-id="ee405-115">**Создание библиотек DLL компонентов, содержащих компоненты, которые используют схему физических данных и предоставляют логическое представление данных другим компонентам (первый элемент в этом списке), а также компоненты, которые реализуются с точки зрения логической модели данных (второй элемент в этом списке).**</span><span class="sxs-lookup"><span data-stu-id="ee405-115">**Build component DLLs that contain components that use the physical data schema and expose a logical view of the data to other components (the first item in this list), as well as components that are implemented in terms of the logical data model (the second item in this list).**</span></span> <span data-ttu-id="ee405-116">После того как структура логики и сведения о состоянии, можно начать писать код и теперь создавать COM-компоненты на основе DLL, реализующие интерфейсы, с точки зрения определенной схемы.</span><span class="sxs-lookup"><span data-stu-id="ee405-116">Once you have the structure of the logic and the state information, you can begin to write code and can now write DLL-based COM components that implement the interfaces in terms of the defined schema.</span></span> <span data-ttu-id="ee405-117">Компоненты просто работают как манипуляторы для работы со сведениями о базе данных, а библиотеки DLL компонентов позволяют создать приложение COM+, которое работает и успешно масштабируется.</span><span class="sxs-lookup"><span data-stu-id="ee405-117">Your components simply act as manipulators for working with your database information, and your component DLLs enable you build a COM+ application that works and that scales successfully.</span></span>

-   <span data-ttu-id="ee405-118">**Разверните компоненты в среде COM+, используя выбранные службы COM+.**</span><span class="sxs-lookup"><span data-stu-id="ee405-118">**Deploy the components in the COM+ environment using the COM+ services you've selected.**</span></span> <span data-ttu-id="ee405-119">После построения приложения можно развернуть приложение в сети или кластере серверов.</span><span class="sxs-lookup"><span data-stu-id="ee405-119">Once you have built the application, you can then deploy the application across a network or server cluster.</span></span> <span data-ttu-id="ee405-120">Теперь можно принимать решения на основе доступных ресурсов, а также настраивать каждый компонент для достижения максимальной производительности.</span><span class="sxs-lookup"><span data-stu-id="ee405-120">You can now make decisions based on resources available, and you can tailor each component for maximum performance.</span></span>

## <a name="related-topics"></a><span data-ttu-id="ee405-121">См. также</span><span class="sxs-lookup"><span data-stu-id="ee405-121">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="ee405-122">Предположения и принципы разработки COM+</span><span class="sxs-lookup"><span data-stu-id="ee405-122">COM+ Design Assumptions and Principles</span></span>](com--design-assumptions-and-principles.md)
</dt> <dt>

[<span data-ttu-id="ee405-123">Проектирование приложения COM+ с помощью UML</span><span class="sxs-lookup"><span data-stu-id="ee405-123">Designing the COM+ Application Using UML</span></span>](designing-the-com--application-using-uml.md)
</dt> <dt>

[<span data-ttu-id="ee405-124">Общие рекомендации по проектированию для использования COM+</span><span class="sxs-lookup"><span data-stu-id="ee405-124">General Design Tips for Using COM+</span></span>](general-design-tips-for-using-com-.md)
</dt> <dt>

[<span data-ttu-id="ee405-125">Оптимизация взаимодействия с уровнем бизнес-логики COM+</span><span class="sxs-lookup"><span data-stu-id="ee405-125">Optimizing Interactions with the COM+ Business Logic Tier</span></span>](optimizing-interactions-with-the-com--business-logic-tier.md)
</dt> <dt>

[<span data-ttu-id="ee405-126">Другие средства Майкрософт для создания распределенных приложений</span><span class="sxs-lookup"><span data-stu-id="ee405-126">Other Microsoft Tools for Building Distributed Applications</span></span>](other-microsoft-tools-for-building-distributed-applications.md)
</dt> </dl>

 

 



