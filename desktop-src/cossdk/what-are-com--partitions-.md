---
description: Раздел COM+ — это логический контейнер, который позволяет приложениям работать независимо от других конфигураций этих приложений.
ms.assetid: c1290d10-968f-44f0-8099-d69c9e706c9e
title: Что такое разделы COM+?
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 69acdae724bb0c9211d147a985f7571c5e7c052f
ms.sourcegitcommit: bf526e267d3991892733bdd229c66d5365cf244a
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 02/05/2021
ms.locfileid: "104156971"
---
# <a name="what-are-com-partitions"></a><span data-ttu-id="be88d-103">Что такое разделы COM+?</span><span class="sxs-lookup"><span data-stu-id="be88d-103">What Are COM+ Partitions?</span></span>

<span data-ttu-id="be88d-104">Раздел COM+ — это логический контейнер, который позволяет приложениям работать независимо от других конфигураций этих приложений.</span><span class="sxs-lookup"><span data-stu-id="be88d-104">A COM+ partition is a logical container that allows applications to run independently of other configurations of those applications.</span></span> <span data-ttu-id="be88d-105">Каждая конфигурация приложения устанавливается в отдельную секцию и может быть отдельно управляться в соответствии с конкретными потребностями пользователей.</span><span class="sxs-lookup"><span data-stu-id="be88d-105">Each configuration of an application is installed into a separate partition and can be separately managed, according to the specific needs of its users.</span></span>

<span data-ttu-id="be88d-106">Во время активации компонента COM+ служба partitions определяет, какую конфигурацию компонента следует активировать, исходя из удостоверения пользователя, запрашивающего активацию компонента.</span><span class="sxs-lookup"><span data-stu-id="be88d-106">During activation of a COM+ component, the partitions service determines which configuration of the component to activate, based on the identity of the user requesting the component activation.</span></span> <span data-ttu-id="be88d-107">Например, одна организация с двумя отдельными группами, рабочими и обучающими, может реализовать разделы COM+ как способ, позволяющий двум группам использовать разные конфигурации приложения COM+ на одном компьютере.</span><span class="sxs-lookup"><span data-stu-id="be88d-107">For example, a single organization that has two separate groups, Production and Training, could implement COM+ partitions as a way to allow the two groups to use different configurations of a COM+ application on the same computer.</span></span>

<span data-ttu-id="be88d-108">**Windows XP:** Возможность создания, настройки или делегирования разделов COM+ недоступна.</span><span class="sxs-lookup"><span data-stu-id="be88d-108">**Windows XP:** The ability to create, configure, or delegate COM+ partitions is not available.</span></span> <span data-ttu-id="be88d-109">Глобальный раздел является единственным доступным разделом COM+.</span><span class="sxs-lookup"><span data-stu-id="be88d-109">The global partition is the only COM+ partition available.</span></span>

<span data-ttu-id="be88d-110">**Windows 2000:** Служба "разделы COM+" недоступна в Windows 2000.</span><span class="sxs-lookup"><span data-stu-id="be88d-110">**Windows 2000:** The COM+ partitions service is not available in Windows 2000.</span></span>

## <a name="benefits-of-using-com-partitions"></a><span data-ttu-id="be88d-111">Преимущества использования разделов COM+</span><span class="sxs-lookup"><span data-stu-id="be88d-111">Benefits of Using COM+ Partitions</span></span>

<span data-ttu-id="be88d-112">Использование разделов COM+ обеспечивает ряд преимуществ, включая следующие:</span><span class="sxs-lookup"><span data-stu-id="be88d-112">The use of COM+ partitions offers several advantages, including the following:</span></span>

-   <span data-ttu-id="be88d-113">Организации могут снизить совокупную стоимость владения (TCO), используя меньше физических серверов приложений для поддержки пользователей, которым требуется несколько конфигураций приложений.</span><span class="sxs-lookup"><span data-stu-id="be88d-113">Organizations can lower their total cost of ownership (TCO) by using fewer physical application servers to support users who need multiple application configurations.</span></span>
-   <span data-ttu-id="be88d-114">Снижается административная нагрузка.</span><span class="sxs-lookup"><span data-stu-id="be88d-114">Administrative overhead is reduced.</span></span> <span data-ttu-id="be88d-115">Вместо того, чтобы настраивать несколько компьютеров и управлять ими, администраторы должны только настраивать несколько разделов на одном компьютере и управлять ими.</span><span class="sxs-lookup"><span data-stu-id="be88d-115">Instead of having to configure and manage multiple computers, administrators need only configure and manage multiple partitions on the same computer.</span></span> <span data-ttu-id="be88d-116">Кроме того, секции можно управлять программно с помощью добавления нового программного интерфейса COM+.</span><span class="sxs-lookup"><span data-stu-id="be88d-116">Furthermore, partitions can be managed programmatically through the addition of a new COM+ programming interface.</span></span>
-   <span data-ttu-id="be88d-117">Безопасность может быть реализована и управляться на основе секционирования для локальных пользователей, пользователей домена и организационных подразделений (OU).</span><span class="sxs-lookup"><span data-stu-id="be88d-117">Security can be implemented and managed on a partition-by-partition basis for local users, domain users, and organizational units (OUs).</span></span>
-   <span data-ttu-id="be88d-118">Программисты и администраторы могут использовать средства разработки и администрирования корпорации Майкрософт, такие как Windows SDK, Active Directory пользователи и компьютеры, а также средство администрирования служб компонентов, для управления разделами COM+.</span><span class="sxs-lookup"><span data-stu-id="be88d-118">Programmers and administrators can use Microsoft's development and administrative tools—such as the Windows SDK, Active Directory Users and Computers, and Component Services administrative tool—to manage COM+ partitions.</span></span> <span data-ttu-id="be88d-119">Функция partitions полностью интегрирована в эти средства.</span><span class="sxs-lookup"><span data-stu-id="be88d-119">The partitions feature is fully integrated into these tools.</span></span>

## <a name="primary-usage-scenario"></a><span data-ttu-id="be88d-120">Основной сценарий использования</span><span class="sxs-lookup"><span data-stu-id="be88d-120">Primary Usage Scenario</span></span>

<span data-ttu-id="be88d-121">Основная причина, по которой клиенты могут развертывать разделы COM+, — это размещение веб-приложений.</span><span class="sxs-lookup"><span data-stu-id="be88d-121">A primary reason for customers to deploy the COM+ partitions feature is to host Web-based applications.</span></span> <span data-ttu-id="be88d-122">Например, предположим, что небольшая программная компания разрабатывает приложение COM+ для использования сотрудниками больницы.</span><span class="sxs-lookup"><span data-stu-id="be88d-122">For example, suppose a small software company develops a COM+ application for use by hospital personnel.</span></span> <span data-ttu-id="be88d-123">Приложение, которое является распределенным веб-приложением, предоставляет способ для больницы хранения и получения медицинских записей о пациентах с помощью базы данных SQL Server.</span><span class="sxs-lookup"><span data-stu-id="be88d-123">The application, which is a distributed Web-based application, provides a way for hospitals to store and retrieve patient medical records using a SQL Server database.</span></span>

<span data-ttu-id="be88d-124">Предположим, что компания программного обеспечения имеет трех клиентов: больницы A, больницы B и больницы C. Хотя каждый клиент запускает клиентскую часть приложения COM+ локально на настольных компьютерах, серверная часть приложения COM+ находится на внутреннем веб-сервере компании Software, и к ним обращаются клиенты через Интернет.</span><span class="sxs-lookup"><span data-stu-id="be88d-124">Suppose the software company has three customers: Hospital A, Hospital B, and Hospital C. While each customer runs the client side of the COM+ application locally on its desktop computers, the server side of the COM+ application resides on the software company's in-house web server and is accessed by its customers via the Web.</span></span>

<span data-ttu-id="be88d-125">Так как каждая из них имеет собственный набор требований к хранению и извлечению, а также собственный набор настраиваемых данных о пациентах, компания программного обеспечения должна предоставить возможность одновременного выполнения нескольких конфигураций серверной части приложения на веб-сервере.</span><span class="sxs-lookup"><span data-stu-id="be88d-125">Because each hospital has its own set of storage and retrieval requirements and its own set of customized patient data, the software company must provide a way for multiple configurations of the server part of the application to be executed simultaneously on the web server.</span></span> <span data-ttu-id="be88d-126">Разделы COM+ предоставляют решение этой проблемы.</span><span class="sxs-lookup"><span data-stu-id="be88d-126">COM+ partitions provide a solution to this problem.</span></span>

<span data-ttu-id="be88d-127">На следующем рисунке показан сценарий partitions для приложения COM+ компании Software.</span><span class="sxs-lookup"><span data-stu-id="be88d-127">The following illustration shows the partitions scenario for the software company's COM+ application.</span></span>

![Схема, на которой показан сценарий секционирования для приложения COM+ с клиентским приложением для серверного приложения в базе данных SQL Server.](images/c4a96ff9-9afd-43c7-807c-4593cb77f51b.png)

## <a name="related-topics"></a><span data-ttu-id="be88d-129">См. также</span><span class="sxs-lookup"><span data-stu-id="be88d-129">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="be88d-130">Ограничения разработки приложений</span><span class="sxs-lookup"><span data-stu-id="be88d-130">Application Design Restrictions</span></span>](application-design-restrictions.md)
</dt> <dt>

[<span data-ttu-id="be88d-131">Компоненты и разделы, помещенные в очередь COM+</span><span class="sxs-lookup"><span data-stu-id="be88d-131">COM+ Queued Components and Partitions</span></span>](com--queued-components-and-partitions.md)
</dt> <dt>

[<span data-ttu-id="be88d-132">Реализация секционирования</span><span class="sxs-lookup"><span data-stu-id="be88d-132">Partition Implementation</span></span>](partition-implementation.md)
</dt> <dt>

[<span data-ttu-id="be88d-133">Регистрация и Активация компонентов в секциях</span><span class="sxs-lookup"><span data-stu-id="be88d-133">Registering and Activating Components in Partitions</span></span>](registering-and-activating-components-in-partitions.md)
</dt> </dl>

 

 



