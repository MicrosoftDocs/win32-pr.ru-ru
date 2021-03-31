---
title: Общие сведения о разработке пользовательского интерфейса
description: В этом разделе описываются три этапа проектирования пользовательского интерфейса и приводятся задачи, которые обычно связаны с каждым этапом.
ms.assetid: ab544cb9-eed3-4575-a8dd-2f5d7b5c575f
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b531fb07a1805c14441c81777bbdddad0739e7cb
ms.sourcegitcommit: e5c43274e96cb8fd1b60fc187ef16723e9258367
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/17/2020
ms.locfileid: "104069483"
---
# <a name="overview-of-the-user-interface-development-process"></a><span data-ttu-id="2cbaf-103">Общие сведения о процессе разработки пользовательского интерфейса</span><span class="sxs-lookup"><span data-stu-id="2cbaf-103">Overview of the User Interface Development Process</span></span>

<span data-ttu-id="2cbaf-104">В этом разделе описываются три этапа проектирования пользовательского интерфейса и приводятся задачи, которые обычно связаны с каждым этапом.</span><span class="sxs-lookup"><span data-stu-id="2cbaf-104">This section outlines the three phases of user interface design and introduces the tasks that are typically associated with each phase.</span></span>

## <a name="the-application-user-interface-and-the-user-experience"></a><span data-ttu-id="2cbaf-105">Пользовательский интерфейс приложения и взаимодействие с пользователем</span><span class="sxs-lookup"><span data-stu-id="2cbaf-105">The Application User Interface and the User Experience</span></span>

<span data-ttu-id="2cbaf-106">Для начала необходимо уточнить условия "Пользовательский интерфейс" и "взаимодействие с пользователем".</span><span class="sxs-lookup"><span data-stu-id="2cbaf-106">To begin, the terms "user interface" and "user experience" must be clarified.</span></span>

<span data-ttu-id="2cbaf-107">Пользовательский интерфейс приложения обычно включает объекты, которые видит пользователь, и взаимодействует с ним непосредственно на экране.</span><span class="sxs-lookup"><span data-stu-id="2cbaf-107">The user interface of an application typically involves those objects that a user sees and interacts with directly on their screen.</span></span> <span data-ttu-id="2cbaf-108">Например, такие объекты включают в себя пространство документа, меню, диалоговые окна, значки, изображения и анимации.</span><span class="sxs-lookup"><span data-stu-id="2cbaf-108">For example, such objects include the document space, menus, dialog boxes, icons, images, and animations.</span></span>

<span data-ttu-id="2cbaf-109">Однако пользовательский интерфейс приложения — лишь один аспект общего взаимодействия с пользователем.</span><span class="sxs-lookup"><span data-stu-id="2cbaf-109">However, the user interface of an application is only one aspect of the overall user experience.</span></span> <span data-ttu-id="2cbaf-110">Другие аспекты взаимодействия с пользователем, которые не видны пользователю, но являются неотъемлемой частью приложения и важны для его удобства использования, включают время запуска, задержки, обработку ошибок и автоматизированные задачи, которые выполняются без прямого взаимодействия с пользователем.</span><span class="sxs-lookup"><span data-stu-id="2cbaf-110">Other aspects of the user experience that are not visible to the user, but are integral to an application and critical to its usability, include start up time, latency, error handling, and automated tasks that are completed without direct user interaction.</span></span>

<span data-ttu-id="2cbaf-111">Как правило, Пользовательский интерфейс требует вмешательства пользователя для выполнения задачи, а удобство работы с пользователем может быть достигнуто без интерфейса пользователя.</span><span class="sxs-lookup"><span data-stu-id="2cbaf-111">In general, a user interface requires action by a user to accomplish a task, while a great user experience can be achieved with no user interface at all.</span></span>

## <a name="user-interface-development"></a><span data-ttu-id="2cbaf-112">Разработка пользовательского интерфейса</span><span class="sxs-lookup"><span data-stu-id="2cbaf-112">User Interface Development</span></span>

<span data-ttu-id="2cbaf-113">Для обеспечения успешного взаимодействия с пользователем требуется сбалансированный подход на протяжении всего жизненного цикла разработки.</span><span class="sxs-lookup"><span data-stu-id="2cbaf-113">Providing a successful user experience requires a balanced approach throughout the development life cycle.</span></span> <span data-ttu-id="2cbaf-114">Чтобы обеспечить этот баланс, необходимо не только сосредоточиться на реализации функций, необходимых для выполнения задачи, но и о том, как задача предоставляется через пользовательский интерфейс.</span><span class="sxs-lookup"><span data-stu-id="2cbaf-114">To ensure this balance, you must not only focus on implementing the functionality required to complete a task but also on how the task is exposed through the user interface.</span></span> <span data-ttu-id="2cbaf-115">Помните, что пользовательский интерфейс должен быть не только функциональным, но и может быть пригоден для использования.</span><span class="sxs-lookup"><span data-stu-id="2cbaf-115">Remember, the user interface must not only be functional, it must also be usable.</span></span>

<span data-ttu-id="2cbaf-116">Ниже описаны типичные этапы процесса двелопмент пользовательского интерфейса:</span><span class="sxs-lookup"><span data-stu-id="2cbaf-116">The following outlines the typical phases of the user interface dvelopment process:</span></span>

### <a name="designing"></a><span data-ttu-id="2cbaf-117">Проектирование</span><span class="sxs-lookup"><span data-stu-id="2cbaf-117">Designing</span></span>

-   <span data-ttu-id="2cbaf-118">Функциональные требования — определите первоначальные требования и цели для приложения.</span><span class="sxs-lookup"><span data-stu-id="2cbaf-118">Functional requirements – Determine the initial requirements and goals for the application.</span></span>
-   <span data-ttu-id="2cbaf-119">Анализ пользователей — определение пользовательских сценариев и понимание потребностей и ожиданий пользователей для каждого сценария.</span><span class="sxs-lookup"><span data-stu-id="2cbaf-119">User analysis – Identify the user scenarios and understand the needs and expectations of users for each scenario.</span></span>
-   <span data-ttu-id="2cbaf-120">Концептуальный дизайн — моделирование базового бизнес-приложения, которое должно поддерживаться приложением.</span><span class="sxs-lookup"><span data-stu-id="2cbaf-120">Conceptual design – Model the underlying business that the application must support.</span></span>
-   <span data-ttu-id="2cbaf-121">Логическое проектирование — проектирование процесса и потока информации приложения.</span><span class="sxs-lookup"><span data-stu-id="2cbaf-121">Logical design – Design the process and information flow of the application.</span></span>
-   <span data-ttu-id="2cbaf-122">Физическая структура — решите, как логическая структура будет реализована на конкретных физических платформах.</span><span class="sxs-lookup"><span data-stu-id="2cbaf-122">Physical design – Decide how the logical design will be implemented on specific physical platforms.</span></span>

### <a name="implementing"></a><span data-ttu-id="2cbaf-123">Использованию</span><span class="sxs-lookup"><span data-stu-id="2cbaf-123">Implementing</span></span>

-   <span data-ttu-id="2cbaf-124">Прототип — разработка бумаги или интерактивного экранного макетов, который сосредоточен на интерфейсе и не включает ненужные элементы визуальной разработки.</span><span class="sxs-lookup"><span data-stu-id="2cbaf-124">Prototype – Develop paper or interactive screen mockups that focus on the interface and don't include distracting visual design elements.</span></span>
-   <span data-ttu-id="2cbaf-125">Конструкция — сборка приложения и подготовка к запросам на изменение структуры.</span><span class="sxs-lookup"><span data-stu-id="2cbaf-125">Construct – Build the application and prepare for design change requests.</span></span>

### <a name="testing"></a><span data-ttu-id="2cbaf-126">Тестирование</span><span class="sxs-lookup"><span data-stu-id="2cbaf-126">Testing</span></span>

-   <span data-ttu-id="2cbaf-127">Тестирование на удобство использования — тестирование приложения с различными пользователями и сценариями.</span><span class="sxs-lookup"><span data-stu-id="2cbaf-127">Usability testing – Test the application with various users and scenarios.</span></span>
-   <span data-ttu-id="2cbaf-128">Тестирование специальных возможностей — тестирование приложения с помощью доступных технологий и автоматизированных средств тестирования.</span><span class="sxs-lookup"><span data-stu-id="2cbaf-128">Accessibility testing – Test the application with accessible technologies and automated test tools.</span></span>

 

 




