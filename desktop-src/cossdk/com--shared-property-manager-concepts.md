---
description: В COM+ общее переходное состояние для объектов управляется с помощью общего диспетчера свойств (SPM). SPM — это распределитель ресурсов, который можно использовать для обмена состояниями между несколькими объектами в процессе сервера.
ms.assetid: 31b50c2a-68b5-4816-9a56-8cd9475e7beb
title: Общие понятия диспетчер свойств COM+
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9be55c4a83aa363c911564aefabbe1d85f3804fb
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "105710779"
---
# <a name="com-shared-property-manager-concepts"></a><span data-ttu-id="6748a-104">Общие понятия диспетчер свойств COM+</span><span class="sxs-lookup"><span data-stu-id="6748a-104">COM+ Shared Property Manager Concepts</span></span>

<span data-ttu-id="6748a-105">В COM+ общее переходное состояние для объектов управляется с помощью общего диспетчера свойств (SPM).</span><span class="sxs-lookup"><span data-stu-id="6748a-105">In COM+, shared transient state for objects is managed by using the shared property manager (SPM).</span></span> <span data-ttu-id="6748a-106">SPM — это распределитель ресурсов, который можно использовать для обмена состояниями между несколькими объектами в процессе сервера.</span><span class="sxs-lookup"><span data-stu-id="6748a-106">The SPM is a resource dispenser that you can use to share state among multiple objects within a server process.</span></span>

<span data-ttu-id="6748a-107">Нельзя использовать глобальные переменные в распределенной среде из-за проблем параллелизма и конфликтов имен.</span><span class="sxs-lookup"><span data-stu-id="6748a-107">You cannot use global variables in a distributed environment because of concurrency and name collision issues.</span></span> <span data-ttu-id="6748a-108">Диспетчер общих свойств устраняет конфликты имен, предоставляя общие группы свойств, которые устанавливают уникальные пространства имен для общих свойств, которые они содержат.</span><span class="sxs-lookup"><span data-stu-id="6748a-108">The shared property manager eliminates name collisions by providing shared property groups, which establish unique namespaces for the shared properties they contain.</span></span> <span data-ttu-id="6748a-109">SPM также реализует блокировки и семафоры для защиты общих свойств от одновременного доступа, что может привести к потере обновлений и покидать свойства в непредсказуемом состоянии.</span><span class="sxs-lookup"><span data-stu-id="6748a-109">The SPM also implements locks and semaphores to help protect shared properties from simultaneous access, which could result in lost updates and leave properties in an unpredictable state.</span></span>

> [!Note]  
> <span data-ttu-id="6748a-110">Общее переходное состояние — это сведения о состоянии, хранящиеся в памяти, которые не сохранятся из-за сбоев системы.</span><span class="sxs-lookup"><span data-stu-id="6748a-110">Shared transient state is state information kept in memory that does not survive system failures.</span></span> <span data-ttu-id="6748a-111">Эти сведения предназначены для совместного использования несколькими объектами в пределах транзакций (но не между процессами).</span><span class="sxs-lookup"><span data-stu-id="6748a-111">The information is designed to be shared by multiple objects across transaction (but not across process) boundaries.</span></span>

 

<span data-ttu-id="6748a-112">Общие свойства, хранящиеся в SPM, доступны только для объектов, выполняющихся в одном процессе.</span><span class="sxs-lookup"><span data-stu-id="6748a-112">Shared properties stored in the SPM are available only to objects running in the same process.</span></span> <span data-ttu-id="6748a-113">Это означает, что объекты, которые будут использовать SPM для хранения значений и которые должны иметь доступ к этим значениям, должны быть установлены как часть одного приложения COM+.</span><span class="sxs-lookup"><span data-stu-id="6748a-113">This means that the objects that will use the SPM for storing values and that will need to have access to these values must be installed as part of the same COM+ application.</span></span> <span data-ttu-id="6748a-114">Системные администраторы могут перемещать классы COM+ из одного пакета в другой после развертывания приложения COM+.</span><span class="sxs-lookup"><span data-stu-id="6748a-114">It is possible for system administrators to move COM+ classes from one package to another after your COM+ application has been deployed.</span></span> <span data-ttu-id="6748a-115">Если вы полагаетесь на несколько объектов, совместно использующих свойства с помощью SPM, необходимо четко документировать, что они должны быть установлены в одном приложении COM+.</span><span class="sxs-lookup"><span data-stu-id="6748a-115">If you rely on several objects sharing properties through the SPM, you should clearly document that they must be installed in the same COM+ application.</span></span>

<span data-ttu-id="6748a-116">Также важно, чтобы свойства общего доступа к компонентам имели один и тот же атрибут активации.</span><span class="sxs-lookup"><span data-stu-id="6748a-116">It's also important for components sharing properties to have the same activation attribute.</span></span> <span data-ttu-id="6748a-117">Если два компонента в одном пакете имеют разные атрибуты активации, они обычно не смогут совместно использовать свойства.</span><span class="sxs-lookup"><span data-stu-id="6748a-117">If two components in the same package have different activation attributes, they generally won't be able to share properties.</span></span> <span data-ttu-id="6748a-118">Например, если один компонент настроен для выполнения в клиентском процессе, а другой настроен для выполнения в серверном процессе, то их объекты обычно выполняются в разных процессах, даже если они находятся в одном пакете.</span><span class="sxs-lookup"><span data-stu-id="6748a-118">For example, if one component is configured to run in a client process and the other is configured to run in a server process, their objects will usually run in different processes even though they're in the same package.</span></span>

<span data-ttu-id="6748a-119">Экземпляры объектов [**шаредпропертиграупманажер**](sharedpropertygroupmanager.md), [**шаредпропертиграуп**](sharedpropertygroup.md)и [**шаредпроперти**](sharedproperty.md) всегда следует создавать из компонентов COM+, а не из базового клиента.</span><span class="sxs-lookup"><span data-stu-id="6748a-119">You should always instantiate the [**SharedPropertyGroupManager**](sharedpropertygroupmanager.md), [**SharedPropertyGroup**](sharedpropertygroup.md), and [**SharedProperty**](sharedproperty.md) objects from COM+ components rather than from a base client.</span></span> <span data-ttu-id="6748a-120">Если базовый клиент создает общие группы свойств и свойства, общие свойства находятся внутри процесса базового клиента, а не в серверном процессе.</span><span class="sxs-lookup"><span data-stu-id="6748a-120">If a base client creates shared property groups and properties, the shared properties are inside the base-client process, not in a server process.</span></span> <span data-ttu-id="6748a-121">Это означает, что объекты COM+ не могут совместно использовать свойства, если только эти объекты не выполняются в клиентском процессе (как правило, это не хорошая идея).</span><span class="sxs-lookup"><span data-stu-id="6748a-121">This means the COM+ objects cannot share the properties unless the objects are also running in the client process (which is generally not a good idea).</span></span>

## <a name="related-topics"></a><span data-ttu-id="6748a-122">См. также</span><span class="sxs-lookup"><span data-stu-id="6748a-122">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="6748a-123">Общие диспетчер свойств COM+</span><span class="sxs-lookup"><span data-stu-id="6748a-123">COM+ Shared Property Manager</span></span>](com--shared-property-manager.md)
</dt> <dt>

[<span data-ttu-id="6748a-124">Общие группы свойств</span><span class="sxs-lookup"><span data-stu-id="6748a-124">Shared Property Groups</span></span>](shared-property-groups.md)
</dt> </dl>

 

 



