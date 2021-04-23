---
description: Службы COM+ без компонентов
ms.assetid: 5ef67411-334b-476e-b9b7-3677b24ab7df
title: Службы COM+ без компонентов
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d1eeed5a9af96e241d137714d151cc632dd0f20e
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104141839"
---
# <a name="com-services-without-components"></a><span data-ttu-id="eb580-103">Службы COM+ без компонентов</span><span class="sxs-lookup"><span data-stu-id="eb580-103">COM+ Services Without Components</span></span>

<span data-ttu-id="eb580-104">С помощью COM+ 1,5 можно использовать службы, предоставляемые COM+, без необходимости создания компонента для хранения методов, вызывающих эти службы.</span><span class="sxs-lookup"><span data-stu-id="eb580-104">With COM+ 1.5, you can use the services provided by COM+ without needing to build a component to contain the methods that call those services.</span></span> <span data-ttu-id="eb580-105">Это значительно выгодно для разработчиков, которые обычно не используют компоненты, но хотят использовать такие службы COM+, как транзакции или средство регистрации COM+.</span><span class="sxs-lookup"><span data-stu-id="eb580-105">This greatly benefits developers who do not normally use components but want to use COM+ services such as transactions or the COM+ Tracker.</span></span> <span data-ttu-id="eb580-106">Используя службы COM+ без компонентов, разработчики могут избежать издержек при создании компонента, который используется для доступа только к необходимым службам COM+.</span><span class="sxs-lookup"><span data-stu-id="eb580-106">By using COM+ services without components, developers can avoid the overhead of creating a component that is used to access only the COM+ services they need.</span></span>

<span data-ttu-id="eb580-107">Например, среды сценариев, как правило, были наиболее крупными потребителями служб COM+, но они никогда не смогли эффективно использовать эти службы, так как службы, необходимые для объединения в компонент COM+.</span><span class="sxs-lookup"><span data-stu-id="eb580-107">For example, script environments traditionally have been the largest consumers of COM+ services but they were never able to use those services efficiently because the services needed to be bundled within a COM+ component.</span></span> <span data-ttu-id="eb580-108">Это требование к объединению увеличивает затраты на производительность из-за увеличенного взаимодействия и дублирования данных, необходимых для взаимодействия среды сценариев с компонентом.</span><span class="sxs-lookup"><span data-stu-id="eb580-108">This bundling requirement increased performance costs because of the increased communication and duplication of data necessary for the scripting environment to interact with the component.</span></span> <span data-ttu-id="eb580-109">С помощью служб без компонентов такие затраты снижаются.</span><span class="sxs-lookup"><span data-stu-id="eb580-109">By using services without components, such costs are minimized.</span></span>

<span data-ttu-id="eb580-110">В разделах, приведенных в следующей таблице, содержатся сведения об использовании служб COM+ без компонентов в качестве фоновых сведений и задач.</span><span class="sxs-lookup"><span data-stu-id="eb580-110">The topics described in the following table provide background and task information about using COM+ services without components.</span></span> <span data-ttu-id="eb580-111">Эта функция предназначена для опытных Visual C++ разработчиков, которые интересуются производительностью.</span><span class="sxs-lookup"><span data-stu-id="eb580-111">This feature is intended for advanced Visual C++ developers who are concerned about performance.</span></span>



| <span data-ttu-id="eb580-112">Раздел</span><span class="sxs-lookup"><span data-stu-id="eb580-112">Topic</span></span>                                                                                                 | <span data-ttu-id="eb580-113">Описание</span><span class="sxs-lookup"><span data-stu-id="eb580-113">Description</span></span>                                                                                    |
|-------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="eb580-114">Службы COM+ без компонентов концепции</span><span class="sxs-lookup"><span data-stu-id="eb580-114">COM+ Services Without Components Concepts</span></span>](com--services-without-components-concepts.md)<br/> | <span data-ttu-id="eb580-115">Содержит общие сведения об использовании служб COM+ без компонентов.</span><span class="sxs-lookup"><span data-stu-id="eb580-115">Provides an overview of using COM+ services without components.</span></span><br/>                     |
| [<span data-ttu-id="eb580-116">Задачи служб COM+ без компонентов</span><span class="sxs-lookup"><span data-stu-id="eb580-116">COM+ Services Without Components Tasks</span></span>](com--services-without-components-tasks.md)<br/>       | <span data-ttu-id="eb580-117">Содержит инструкции по использованию COM+ для создания и использования служб без компонентов.</span><span class="sxs-lookup"><span data-stu-id="eb580-117">Provides instructions for using COM+ to create and use services without components.</span></span><br/> |



 

 

 




