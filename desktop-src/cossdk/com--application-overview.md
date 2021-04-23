---
description: Приложение COM+ — это основная единица администрирования и безопасности служб компонентов, которая состоит из группы COM-компонентов, которые обычно выполняют связанные функции.
ms.assetid: 82e94acb-e7ce-4423-a720-26ee65d0d7b4
title: Общие сведения о приложении COM+
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d3365e0c0e7598d8f1eb2f466e8a2cea2d93edf4
ms.sourcegitcommit: bf526e267d3991892733bdd229c66d5365cf244a
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 02/05/2021
ms.locfileid: "105664787"
---
# <a name="com-application-overview"></a><span data-ttu-id="23f0f-103">Общие сведения о приложении COM+</span><span class="sxs-lookup"><span data-stu-id="23f0f-103">COM+ Application Overview</span></span>

<span data-ttu-id="23f0f-104">Приложение COM+ — это основная единица администрирования и безопасности служб компонентов, которая состоит из группы COM-компонентов, которые обычно выполняют связанные функции.</span><span class="sxs-lookup"><span data-stu-id="23f0f-104">A COM+ application is the primary unit of administration and security for Component Services and consists of a group of COM components that generally perform related functions.</span></span> <span data-ttu-id="23f0f-105">Эти компоненты более подробно состоят из интерфейсов и методов, как показано на следующем рисунке.</span><span class="sxs-lookup"><span data-stu-id="23f0f-105">These components further consist of interfaces and methods, as shown in the following illustration.</span></span>

![Схема, в которой показаны интерфейсы и методы внутри рамок, в порядке последовательного метода внутри компонента внутри приложения COM+.](images/487518b4-0460-4b2d-a834-c4ea57755ffd.png)

<span data-ttu-id="23f0f-107">Средство администрирования служб компонентов можно использовать для создания новых приложений COM+, добавления компонентов в приложения и установки атрибутов для приложения и его компонентов.</span><span class="sxs-lookup"><span data-stu-id="23f0f-107">You can use the Component Services administrative tool to create new COM+ applications, add components to applications, and set the attributes for an application and its components.</span></span>

<span data-ttu-id="23f0f-108">Создавая логические группы COM-компонентов в качестве приложений COM+, вы можете воспользоваться следующими преимуществами COM+:</span><span class="sxs-lookup"><span data-stu-id="23f0f-108">By creating logical groups of COM components as COM+ applications, you can take advantage of the following benefits of COM+:</span></span>

-   <span data-ttu-id="23f0f-109">Область развертывания для COM-компонентов.</span><span class="sxs-lookup"><span data-stu-id="23f0f-109">A deployment scope for COM components.</span></span>
-   <span data-ttu-id="23f0f-110">Общая область конфигурации для COM-компонентов, включая границы безопасности и очереди.</span><span class="sxs-lookup"><span data-stu-id="23f0f-110">A common configuration scope for COM components, including security boundaries and queuing.</span></span>
-   <span data-ttu-id="23f0f-111">Хранение атрибутов компонента, не предоставляемых разработчиком компонентов (например, транзакции и синхронизация).</span><span class="sxs-lookup"><span data-stu-id="23f0f-111">Storage of component attributes not provided by the component developer (for example, transactions and synchronization).</span></span>
-   <span data-ttu-id="23f0f-112">Библиотеки динамической компоновки (DLL) компонента, загруженные в процессы (DLLHost.exe) по запросу.</span><span class="sxs-lookup"><span data-stu-id="23f0f-112">Component dynamic-link libraries (DLLs) loaded into processes (DLLHost.exe) on demand.</span></span>
-   <span data-ttu-id="23f0f-113">Управляемые серверные процессы для размещения компонентов.</span><span class="sxs-lookup"><span data-stu-id="23f0f-113">Managed server processes to host components.</span></span>
-   <span data-ttu-id="23f0f-114">Создание и управление потоками, используемыми компонентами.</span><span class="sxs-lookup"><span data-stu-id="23f0f-114">Creation and management of threads used by components.</span></span>
-   <span data-ttu-id="23f0f-115">Доступ к объекту контекста для распределителя ресурсов, позволяющий автоматически связывать полученные ресурсы с контекстом.</span><span class="sxs-lookup"><span data-stu-id="23f0f-115">Access to the context object for resource dispensers, allowing acquired resources to be automatically associated with the context.</span></span> <span data-ttu-id="23f0f-116">(Дополнительные сведения о COM-компонентах и контекстах см. в разделе [контексты com+](com--contexts.md).)</span><span class="sxs-lookup"><span data-stu-id="23f0f-116">(For more information on COM components and contexts, see [COM+ Contexts](com--contexts.md).)</span></span>

## <a name="related-topics"></a><span data-ttu-id="23f0f-117">См. также</span><span class="sxs-lookup"><span data-stu-id="23f0f-117">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="23f0f-118">Разработка приложений COM+</span><span class="sxs-lookup"><span data-stu-id="23f0f-118">Developing COM+ Applications</span></span>](developing-com--applications.md)
</dt> <dt>

[<span data-ttu-id="23f0f-119">Части приложения COM+</span><span class="sxs-lookup"><span data-stu-id="23f0f-119">Parts of a COM+ Application</span></span>](parts-of-a-com--application.md)
</dt> <dt>

[<span data-ttu-id="23f0f-120">Типы приложений COM+</span><span class="sxs-lookup"><span data-stu-id="23f0f-120">Types of COM+ Applications</span></span>](types-of-com--applications.md)
</dt> </dl>

 

 



