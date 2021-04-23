---
description: При разработке приложений COM+ основные задачи включают в себя проектирование компонентов COM для инкапсуляции логики приложения и интеграции этих компонентов в приложение COM+, создание приложения COM+ и администрирование приложения с помощью развертывания и обслуживания.
ms.assetid: 8c6ec901-1eeb-46b0-8a3a-26d8eff99f6d
title: Разработка приложений COM+
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5ee6495b7d8f7b2cc059b113f4250042cfd59b99
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104538585"
---
# <a name="developing-com-applications"></a><span data-ttu-id="94b51-103">Разработка приложений COM+</span><span class="sxs-lookup"><span data-stu-id="94b51-103">Developing COM+ Applications</span></span>

<span data-ttu-id="94b51-104">При разработке приложений COM+ основные задачи включают в себя проектирование компонентов COM для инкапсуляции логики приложения и интеграции этих компонентов в приложение COM+, создание приложения COM+ и администрирование приложения с помощью развертывания и обслуживания.</span><span class="sxs-lookup"><span data-stu-id="94b51-104">When developing COM+ applications, the principal tasks include designing COM components to encapsulate application logic and integrating these components into a COM+ application, creating the COM+ application, and administering the application through deployment and maintenance.</span></span>

## <a name="designing-com-components"></a><span data-ttu-id="94b51-105">Проектирование компонентов COM</span><span class="sxs-lookup"><span data-stu-id="94b51-105">Designing COM Components</span></span>

<span data-ttu-id="94b51-106">Ниже описана общая процедура для хорошего проектирования компонентов.</span><span class="sxs-lookup"><span data-stu-id="94b51-106">The following steps describe a general procedure for good component design:</span></span>

1.  <span data-ttu-id="94b51-107">Определите классы COM и классы реализации.</span><span class="sxs-lookup"><span data-stu-id="94b51-107">Define the COM classes and implementation classes.</span></span>
2.  <span data-ttu-id="94b51-108">Сгруппируйте классы в компоненты.</span><span class="sxs-lookup"><span data-stu-id="94b51-108">Group the classes into components.</span></span>
3.  <span data-ttu-id="94b51-109">Выберите набор служб COM+ для компонента, даже если они не указаны при разработке компонента.</span><span class="sxs-lookup"><span data-stu-id="94b51-109">Select the set of COM+ services for your component, even if you do not specify all of them when developing the component.</span></span> <span data-ttu-id="94b51-110">Эти службы впоследствии можно указать с помощью средства администрирования служб компонентов или модели объектов администрирования COM+ (Дополнительные сведения об объектной модели администрирования COM+ см. в разделе [Автоматизация администрирования com+](automating-com--administration.md) ).</span><span class="sxs-lookup"><span data-stu-id="94b51-110">These services can later be specified using the Component Services administrative tool or the COM+ administration object model (See [Automating COM+ Administration](automating-com--administration.md) for more information about the COM+ administration object model.)</span></span>

## <a name="creating-the-com-application"></a><span data-ttu-id="94b51-111">Создание приложения COM+</span><span class="sxs-lookup"><span data-stu-id="94b51-111">Creating the COM+ Application</span></span>

<span data-ttu-id="94b51-112">После разработки компонентов COM разработчик интегрирует компоненты в приложение COM+ и настраивает приложение.</span><span class="sxs-lookup"><span data-stu-id="94b51-112">After designing the COM components, the developer integrates the components into a COM+ application and configures the application.</span></span> <span data-ttu-id="94b51-113">Процесс описан в следующих шагах:</span><span class="sxs-lookup"><span data-stu-id="94b51-113">The following steps describe the process:</span></span>

1.  <span data-ttu-id="94b51-114">Интегрируйте компоненты в приложение COM+.</span><span class="sxs-lookup"><span data-stu-id="94b51-114">Integrate the components into a COM+ application.</span></span> <span data-ttu-id="94b51-115">Компоненты можно интегрировать в существующее приложение COM+ или создать новое (пустое) приложение для компонентов.</span><span class="sxs-lookup"><span data-stu-id="94b51-115">You can integrate the components into an existing COM+ application or create a new (empty) application for the components.</span></span> <span data-ttu-id="94b51-116">(См. раздел [Создание приложений COM+](creating-com--applications.md).)</span><span class="sxs-lookup"><span data-stu-id="94b51-116">(See [Creating COM+ Applications](creating-com--applications.md).)</span></span>
2.  <span data-ttu-id="94b51-117">Укажите правильный набор атрибутов для каждого из классов (если они есть, и если они не указаны в средстве разработки).</span><span class="sxs-lookup"><span data-stu-id="94b51-117">Specify the correct set of attributes for each of the classes (if any, and if not specified in the development tool).</span></span> <span data-ttu-id="94b51-118">Эти атрибуты выражают компоненты, зависящие от любых служб COM+, которые могут полагаться на их реализацию (например, транзакции, компоненты в очереди, безопасность, Группировка объектов и JIT-активацию).</span><span class="sxs-lookup"><span data-stu-id="94b51-118">These attributes express the components dependencies on any COM+ services its implementation might rely on (for example, transactions, Queued Components, Security, Object Pooling, and Just-in-Time Activation).</span></span>
3.  <span data-ttu-id="94b51-119">Настройте платформу безопасности (роли и назначение ролей классам, интерфейсам и методам).</span><span class="sxs-lookup"><span data-stu-id="94b51-119">Set up the security framework (roles and assignment of roles to classes, interfaces, and methods).</span></span>
4.  <span data-ttu-id="94b51-120">Настройте зависящие от среды атрибуты для классов и приложений (например, размер пула объектов по умолчанию).</span><span class="sxs-lookup"><span data-stu-id="94b51-120">Configure environment-specific attributes on classes and applications (the default object pool size, for example).</span></span> <span data-ttu-id="94b51-121">Эти атрибуты, зависящие от среды, впоследствии могут быть установлены (или изменены) системным администратором.</span><span class="sxs-lookup"><span data-stu-id="94b51-121">These environment-specific attributes can later be set (or modified) by the system administrator.</span></span>
5.  <span data-ttu-id="94b51-122">Экспортируйте приложение для распространения и развертывания.</span><span class="sxs-lookup"><span data-stu-id="94b51-122">Export the application for redistribution and deployment.</span></span>

<span data-ttu-id="94b51-123">Более подробные сведения по проектированию распределенных приложений см. в разделе [Разработка приложений COM+](designing-com--applications.md).</span><span class="sxs-lookup"><span data-stu-id="94b51-123">For more detailed information on the steps in designing distributed applications, see [Designing COM+ Applications](designing-com--applications.md).</span></span>

## <a name="administering-com-applications"></a><span data-ttu-id="94b51-124">Администрирование приложений COM+</span><span class="sxs-lookup"><span data-stu-id="94b51-124">Administering COM+ Applications</span></span>

<span data-ttu-id="94b51-125">Как правило, разработчик доставляет частично настроенное приложение COM+ системному администратору.</span><span class="sxs-lookup"><span data-stu-id="94b51-125">Typically, a developer delivers a partially configured COM+ application to the system administrator.</span></span> <span data-ttu-id="94b51-126">Затем администратор может настроить приложение для одной или нескольких конкретных сред (например, путем добавления учетных записей пользователей в роли и имена серверов в кластере приложений).</span><span class="sxs-lookup"><span data-stu-id="94b51-126">The administrator can then customize the application for one or more specific environments (for example, by adding user accounts in roles and server names in an application cluster).</span></span> <span data-ttu-id="94b51-127">К задачам администратора относятся следующие:</span><span class="sxs-lookup"><span data-stu-id="94b51-127">The administrator's tasks include the following:</span></span>

-   <span data-ttu-id="94b51-128">Установка частично настроенного приложения COM+ на административном компьютере.</span><span class="sxs-lookup"><span data-stu-id="94b51-128">Installing the partially configured COM+ application on an administrative computer.</span></span>
-   <span data-ttu-id="94b51-129">Предоставление особых атрибутов среды, таких как члены роли и размер пула объектов.</span><span class="sxs-lookup"><span data-stu-id="94b51-129">Providing environment-specific attributes, such as role members and object pool size.</span></span>
-   <span data-ttu-id="94b51-130">Повторное экспорт полностью настроенного приложения COM+.</span><span class="sxs-lookup"><span data-stu-id="94b51-130">Re-exporting the fully configured COM+ application.</span></span>
-   <span data-ttu-id="94b51-131">Создание прокси приложения (если приложение должно быть доступно удаленно).</span><span class="sxs-lookup"><span data-stu-id="94b51-131">Creating an application proxy (if the application is to be accessed remotely).</span></span>

<span data-ttu-id="94b51-132">После полной настройки приложения для конкретной среды администратор может развернуть его на тестовой или рабочей машине.</span><span class="sxs-lookup"><span data-stu-id="94b51-132">After an application is fully configured for a specific environment, the administrator can then deploy it on test or production machines.</span></span> <span data-ttu-id="94b51-133">Это включает установку полностью настроенного приложения COM+ на одном или нескольких компьютерах.</span><span class="sxs-lookup"><span data-stu-id="94b51-133">This involves installing the fully configured COM+ application on one or more computers.</span></span>

<span data-ttu-id="94b51-134">Подробные сведения о процедурах администрирования COM+ см. в разделе средство администрирования служб компонентов.</span><span class="sxs-lookup"><span data-stu-id="94b51-134">For detailed information on COM+ administration procedures, see the Component Services administrative tool.</span></span>

 

 



