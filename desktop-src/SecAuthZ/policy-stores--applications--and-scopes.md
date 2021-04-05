---
description: Хранилища политик авторизации, приложения и области представляют разные уровни Организации политики диспетчера авторизации.
ms.assetid: 235f236d-59c9-4a8c-aec6-60d1ddba4d5d
title: Хранилища политик, приложения и области
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4155d7bf60d34474d52c27efd50d2f53741fa73a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "103897794"
---
# <a name="policy-stores-applications-and-scopes"></a><span data-ttu-id="d31f6-103">Хранилища политик, приложения и области</span><span class="sxs-lookup"><span data-stu-id="d31f6-103">Policy Stores, Applications, and Scopes</span></span>

<span data-ttu-id="d31f6-104">Хранилища политик авторизации, приложения и области представляют разные уровни Организации политики диспетчера авторизации.</span><span class="sxs-lookup"><span data-stu-id="d31f6-104">Authorization policy stores, applications, and scopes represent different levels of organization of Authorization Manager policy.</span></span> <span data-ttu-id="d31f6-105">Хранилище политик может содержать одно или несколько приложений, а приложение может содержать одну или несколько областей.</span><span class="sxs-lookup"><span data-stu-id="d31f6-105">A policy store can contain one or more applications, and an application can contain one or more scopes.</span></span>

-   [<span data-ttu-id="d31f6-106">Хранилища политик авторизации</span><span class="sxs-lookup"><span data-stu-id="d31f6-106">Authorization Policy Stores</span></span>](#authorization-policy-stores)
-   [<span data-ttu-id="d31f6-107">Приложения</span><span class="sxs-lookup"><span data-stu-id="d31f6-107">Applications</span></span>](#policy-stores-applications-and-scopes)
-   [<span data-ttu-id="d31f6-108">Области действия</span><span class="sxs-lookup"><span data-stu-id="d31f6-108">Scopes</span></span>](#policy-stores-applications-and-scopes)
-   [<span data-ttu-id="d31f6-109">Делегирование</span><span class="sxs-lookup"><span data-stu-id="d31f6-109">Delegation</span></span>](#delegation)
-   [<span data-ttu-id="d31f6-110">См. также</span><span class="sxs-lookup"><span data-stu-id="d31f6-110">Related topics</span></span>](#related-topics)

## <a name="authorization-policy-stores"></a><span data-ttu-id="d31f6-111">Хранилища политик авторизации</span><span class="sxs-lookup"><span data-stu-id="d31f6-111">Authorization Policy Stores</span></span>

<span data-ttu-id="d31f6-112">В API диспетчера авторизации хранилище политик авторизации представлено объектом [**иазаусоризатионсторе**](/windows/desktop/api/Azroles/nn-azroles-iazauthorizationstore) .</span><span class="sxs-lookup"><span data-stu-id="d31f6-112">In the Authorization Manager API, an authorization policy store is represented by an [**IAzAuthorizationStore**](/windows/desktop/api/Azroles/nn-azroles-iazauthorizationstore) object.</span></span> <span data-ttu-id="d31f6-113">Хранилище политик авторизации содержит определения и назначения приложений, областей, операций, задач, ролей и групп пользователей.</span><span class="sxs-lookup"><span data-stu-id="d31f6-113">The authorization policy store contains definitions and assignments of applications, scopes, operations, tasks, roles, and user groups.</span></span>

<span data-ttu-id="d31f6-114">Хранилище политик авторизации может храниться либо в XML-файле, либо в Active Directory.</span><span class="sxs-lookup"><span data-stu-id="d31f6-114">An authorization policy store can be stored either as an XML file or in Active Directory.</span></span>

<span data-ttu-id="d31f6-115">Приложение должно инициализировать хранилище политики авторизации перед изменением информации в хранилище или с помощью политики магазина для проверки клиентского доступа к ресурсам.</span><span class="sxs-lookup"><span data-stu-id="d31f6-115">An application must initialize an authorization policy store before changing information in the store or using the store policy to check client access to resources.</span></span>

<span data-ttu-id="d31f6-116">Хранилище политик авторизации может содержать один или несколько объектов [**иазаппликатион**](/windows/desktop/api/Azroles/nn-azroles-iazapplication) , каждый из которых представляет политику авторизации для конкретного приложения.</span><span class="sxs-lookup"><span data-stu-id="d31f6-116">An authorization policy store can contain one or more [**IAzApplication**](/windows/desktop/api/Azroles/nn-azroles-iazapplication) objects that each represent authorization policy for a specific application.</span></span>

## <a name="applications"></a><span data-ttu-id="d31f6-117">Приложения</span><span class="sxs-lookup"><span data-stu-id="d31f6-117">Applications</span></span>

<span data-ttu-id="d31f6-118">В API диспетчера авторизации приложение представлено объектом [**иазаппликатион**](/windows/desktop/api/Azroles/nn-azroles-iazapplication) .</span><span class="sxs-lookup"><span data-stu-id="d31f6-118">In the Authorization Manager API, an application is represented by an [**IAzApplication**](/windows/desktop/api/Azroles/nn-azroles-iazapplication) object.</span></span> <span data-ttu-id="d31f6-119">Хранилище политик авторизации может содержать сведения о политике авторизации для многих приложений.</span><span class="sxs-lookup"><span data-stu-id="d31f6-119">An authorization policy store can contain authorization policy information for many applications.</span></span> <span data-ttu-id="d31f6-120">Использование объектов **иазаппликатион** позволяет хранить разные политики авторизации для разных приложений в одном хранилище политик.</span><span class="sxs-lookup"><span data-stu-id="d31f6-120">Using **IAzApplication** objects allows you to store different authorization policy for different applications in a single policy store.</span></span>

<span data-ttu-id="d31f6-121">Хранилище политик авторизации должно содержать по крайней мере одно приложение.</span><span class="sxs-lookup"><span data-stu-id="d31f6-121">An authorization policy store must contain at least one application.</span></span>

## <a name="scopes"></a><span data-ttu-id="d31f6-122">Области действия</span><span class="sxs-lookup"><span data-stu-id="d31f6-122">Scopes</span></span>

<span data-ttu-id="d31f6-123">В API диспетчера авторизации область представляется объектом [**иазскопе**](/windows/desktop/api/Azroles/nn-azroles-iazscope) .</span><span class="sxs-lookup"><span data-stu-id="d31f6-123">In the Authorization Manager API, a scope is represented by an [**IAzScope**](/windows/desktop/api/Azroles/nn-azroles-iazscope) object.</span></span> <span data-ttu-id="d31f6-124">Области предоставляют дополнительный, необязательный уровень организации для политики авторизации.</span><span class="sxs-lookup"><span data-stu-id="d31f6-124">Scopes provide an additional, optional level of organization for an authorization policy.</span></span> <span data-ttu-id="d31f6-125">Приложение может содержать одну или несколько областей, но не должно содержать никаких (диспетчер авторизации предоставляет по умолчанию область уровня приложения).</span><span class="sxs-lookup"><span data-stu-id="d31f6-125">An application can contain one or more scopes, but need not contain any (Authorization Manager provides a default, application-wide scope).</span></span>

<span data-ttu-id="d31f6-126">Область — это подразделение внутри приложения, которое отделяет ресурсы от других ресурсов, используемых приложением.</span><span class="sxs-lookup"><span data-stu-id="d31f6-126">A scope is a subdivision within an application that separates resources from other resources that are used by that application.</span></span> <span data-ttu-id="d31f6-127">Если у вас есть группы диспетчера авторизации, назначения ролей, определения ролей или определения задач, которые не нужно применять ко всему приложению, их можно создать на уровне области.</span><span class="sxs-lookup"><span data-stu-id="d31f6-127">If you have Authorization Manager groups, role assignments, role definitions, or task definitions that you do not want to apply to an entire application, you can create them at the scope level.</span></span>

## <a name="delegation"></a><span data-ttu-id="d31f6-128">Делегирование</span><span class="sxs-lookup"><span data-stu-id="d31f6-128">Delegation</span></span>

<span data-ttu-id="d31f6-129">Хранилища политик авторизации, хранящиеся в Active Directory, поддерживают делегирование администрирования.</span><span class="sxs-lookup"><span data-stu-id="d31f6-129">Authorization policy stores that are stored in Active Directory support delegation of administration.</span></span> <span data-ttu-id="d31f6-130">Администрирование может быть делегировано пользователям и группам на уровне хранилища, приложения или области.</span><span class="sxs-lookup"><span data-stu-id="d31f6-130">Administration can be delegated to users and groups at the store, application, or scope level.</span></span> <span data-ttu-id="d31f6-131">Каждый уровень определяет административные роли для политики на этом уровне.</span><span class="sxs-lookup"><span data-stu-id="d31f6-131">Each level defines administrative roles for the policy at that level.</span></span> <span data-ttu-id="d31f6-132">Чтобы делегировать управление пользователю или группе, назначьте их роли администратора. чтобы разрешить пользователю или группе читать политику, назначьте их роли читателя.</span><span class="sxs-lookup"><span data-stu-id="d31f6-132">To delegate control to a user or group, assign them to the administrator role; to allow a user or group to read the policy, assign them to the reader role.</span></span>

<span data-ttu-id="d31f6-133">Администраторы хранилища, приложения или области могут читать и изменять хранилище политик на делегированном уровне.</span><span class="sxs-lookup"><span data-stu-id="d31f6-133">Administrators of a store, application, or scope can read and modify the policy store at the delegated level.</span></span> <span data-ttu-id="d31f6-134">Читатели могут читать хранилище политик на делегированном уровне, но не изменять хранилище.</span><span class="sxs-lookup"><span data-stu-id="d31f6-134">Readers can read the policy store at the delegated level but cannot modify the store.</span></span>

## <a name="related-topics"></a><span data-ttu-id="d31f6-135">См. также</span><span class="sxs-lookup"><span data-stu-id="d31f6-135">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="d31f6-136">Создание объекта хранилища политики авторизации в C++</span><span class="sxs-lookup"><span data-stu-id="d31f6-136">Creating an Authorization Policy Store Object in C++</span></span>](creating-an-authorization-policy-store-object-in-c--.md)
</dt> <dt>

[<span data-ttu-id="d31f6-137">Создание объекта приложения на C++</span><span class="sxs-lookup"><span data-stu-id="d31f6-137">Creating an Application Object in C++</span></span>](creating-an-application-object-in-c--.md)
</dt> <dt>

[<span data-ttu-id="d31f6-138">Делегирование определения разрешений в C++</span><span class="sxs-lookup"><span data-stu-id="d31f6-138">Delegating the Defining of Permissions in C++</span></span>](delegating-the-defining-of-permissions-in-c--.md)
</dt> </dl>

 

 



