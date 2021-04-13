---
description: С помощью диспетчера авторизации можно интегрировать в приложения механизмы управления доступом, основанные на ролях, используя гибкую инфраструктуру. Это позволяет администраторам, использующим такие приложения, управлять доступом с помощью ролей пользователей, связанных с их функциональными обязанностями.
ms.assetid: c6d37b2e-b149-43e2-8155-cb2f669e421c
title: Модель диспетчера авторизации
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3455c9577f24b260bd02f947d0af99ec85570bd5
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "104350612"
---
# <a name="authorization-manager-model"></a><span data-ttu-id="28ab7-104">Модель диспетчера авторизации</span><span class="sxs-lookup"><span data-stu-id="28ab7-104">Authorization Manager Model</span></span>

<span data-ttu-id="28ab7-105">С помощью диспетчера авторизации можно интегрировать в приложения механизмы управления доступом, основанные на ролях, используя гибкую инфраструктуру.</span><span class="sxs-lookup"><span data-stu-id="28ab7-105">Authorization Manager provides a flexible framework for integrating role-based access control into applications.</span></span> <span data-ttu-id="28ab7-106">Это позволяет администраторам, использующим такие приложения, управлять доступом с помощью ролей пользователей, связанных с их функциональными обязанностями.</span><span class="sxs-lookup"><span data-stu-id="28ab7-106">It enables administrators who use those applications to provide access through assigned user roles that relate to job functions.</span></span>

<span data-ttu-id="28ab7-107">Приложения диспетчера авторизации хранят политику авторизации в виде хранилищ авторизации, хранимых в Active Directory или XML-файл и применяющих политику авторизации во время выполнения.</span><span class="sxs-lookup"><span data-stu-id="28ab7-107">Authorization Manager applications store authorization policy in the form of authorization stores that are stored in Active Directory or XML files and apply authorization policy at run time.</span></span>

<span data-ttu-id="28ab7-108">Затем приложения вызывают метод проверки доступа во время выполнения, который проверяет доступ к сведениям о политике в хранилище данных авторизации.</span><span class="sxs-lookup"><span data-stu-id="28ab7-108">Applications then call a run-time access check method that checks access against the policy information in the authorization store.</span></span>

<span data-ttu-id="28ab7-109">Политика авторизации включает следующие компоненты.</span><span class="sxs-lookup"><span data-stu-id="28ab7-109">Authorization policy includes the following parts:</span></span>

-   [<span data-ttu-id="28ab7-110">Хранилища политик, приложения и области</span><span class="sxs-lookup"><span data-stu-id="28ab7-110">Policy Stores, Applications, and Scopes</span></span>](policy-stores--applications--and-scopes.md)
-   [<span data-ttu-id="28ab7-111">Пользователи и группы</span><span class="sxs-lookup"><span data-stu-id="28ab7-111">Users and Groups</span></span>](users-and-groups.md)
-   [<span data-ttu-id="28ab7-112">Операции и задачи</span><span class="sxs-lookup"><span data-stu-id="28ab7-112">Operations and Tasks</span></span>](operations-and-tasks.md)
-   [<span data-ttu-id="28ab7-113">Роли</span><span class="sxs-lookup"><span data-stu-id="28ab7-113">Roles</span></span>](roles.md)
-   [<span data-ttu-id="28ab7-114">Бизнес-правила</span><span class="sxs-lookup"><span data-stu-id="28ab7-114">Business Rules</span></span>](business-rules.md)
-   [<span data-ttu-id="28ab7-115">Коллекции</span><span class="sxs-lookup"><span data-stu-id="28ab7-115">Collections</span></span>](collections.md)

 

 



