---
description: Инструкции по использованию API диспетчера авторизации для создания хранилища политик авторизации в скрипте.
ms.assetid: bd9a995a-4195-4da4-a194-472448a0cb08
title: Создание хранилища политики авторизации в скрипте
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: c0cb35e8e998f95e99193d1dc5e8a74838b7efc7
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104155502"
---
# <a name="creating-an-authorization-policy-store-in-script"></a><span data-ttu-id="ae376-103">Создание хранилища политики авторизации в скрипте</span><span class="sxs-lookup"><span data-stu-id="ae376-103">Creating an Authorization Policy Store in Script</span></span>

<span data-ttu-id="ae376-104">Создайте политику авторизации до или во время установки приложения.</span><span class="sxs-lookup"><span data-stu-id="ae376-104">Create an authorization policy before or during the installation of an application.</span></span>

<span data-ttu-id="ae376-105">При использовании API диспетчера авторизации для создания политики авторизации следуйте инструкциям, приведенным в следующих разделах.</span><span class="sxs-lookup"><span data-stu-id="ae376-105">When you use the Authorization Manager API to create an authorization policy, follow the instructions provided in the following topics.</span></span>



| <span data-ttu-id="ae376-106">Раздел</span><span class="sxs-lookup"><span data-stu-id="ae376-106">Topic</span></span>                                                                                                                  | <span data-ttu-id="ae376-107">Описание</span><span class="sxs-lookup"><span data-stu-id="ae376-107">Description</span></span>                                                                                                                                                                                                                                                    |
|------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="ae376-108">Создание объекта хранилища политики авторизации в скрипте</span><span class="sxs-lookup"><span data-stu-id="ae376-108">Creating an Authorization Policy Store Object in Script</span></span>](creating-an-authorization-policy-store-object-in-script.md) | <span data-ttu-id="ae376-109">Хранилище политик авторизации содержит сведения о политике безопасности приложения или группы приложений.</span><span class="sxs-lookup"><span data-stu-id="ae376-109">An authorization policy store contains information about the security policy of an application or group of applications.</span></span>                                                                                                                                       |
| [<span data-ttu-id="ae376-110">Создание объекта приложения в скрипте</span><span class="sxs-lookup"><span data-stu-id="ae376-110">Creating an Application Object in Script</span></span>](creating-an-application-object-in-script.md)                               | <span data-ttu-id="ae376-111">Для каждого приложения, использующего хранилище политик авторизации, необходимо создать объект [**иазаппликатион**](/windows/desktop/api/Azroles/nn-azroles-iazapplication) и сохранить его в хранилище политик.</span><span class="sxs-lookup"><span data-stu-id="ae376-111">For each application that uses an authorization policy store, you must create an [**IAzApplication**](/windows/desktop/api/Azroles/nn-azroles-iazapplication) object and save it to a policy store.</span></span>                                                                                                |
| [<span data-ttu-id="ae376-112">Определение операций в скрипте</span><span class="sxs-lookup"><span data-stu-id="ae376-112">Defining Operations in Script</span></span>](defining-operations-in-script.md)                                                     | <span data-ttu-id="ae376-113">Операция — это функция низкого уровня или метод приложения.</span><span class="sxs-lookup"><span data-stu-id="ae376-113">An operation is a low-level function or method of an application.</span></span>                                                                                                                                                                                              |
| [<span data-ttu-id="ae376-114">Группирование операций в задачи в скрипте</span><span class="sxs-lookup"><span data-stu-id="ae376-114">Grouping Operations into Tasks in Script</span></span>](grouping-operations-into-tasks-in-script.md)                               | <span data-ttu-id="ae376-115">Задача — это высокоуровневое действие, которое необходимо выполнить пользователям приложения.</span><span class="sxs-lookup"><span data-stu-id="ae376-115">A task is a high-level action that users of an application need to complete.</span></span> <span data-ttu-id="ae376-116">Задачи состоят из операций, которые являются функциями низкого уровня и методами приложения.</span><span class="sxs-lookup"><span data-stu-id="ae376-116">Tasks are made up of operations, which are low-level functions and methods of the application.</span></span>                                                                                    |
| [<span data-ttu-id="ae376-117">Группирование задач в роли в скрипте</span><span class="sxs-lookup"><span data-stu-id="ae376-117">Grouping Tasks into Roles in Script</span></span>](grouping-tasks-into-roles-in-script.md)                                         | <span data-ttu-id="ae376-118">Роль представляет категорию пользователей и задачи, которые эти пользователи имеют право выполнять.</span><span class="sxs-lookup"><span data-stu-id="ae376-118">A role represents a category of users and the tasks those users are authorized to perform.</span></span>                                                                                                                                                                     |
| [<span data-ttu-id="ae376-119">Определение групп пользователей в сценарии</span><span class="sxs-lookup"><span data-stu-id="ae376-119">Defining Groups of Users in Script</span></span>](defining-groups-of-users-in-script.md)                                           | <span data-ttu-id="ae376-120">Объект [**иазаппликатионграуп**](/windows/desktop/api/Azroles/nn-azroles-iazapplicationgroup) представляет группу пользователей.</span><span class="sxs-lookup"><span data-stu-id="ae376-120">An [**IAzApplicationGroup**](/windows/desktop/api/Azroles/nn-azroles-iazapplicationgroup) object represents a group of users.</span></span> <span data-ttu-id="ae376-121">Затем роли могут быть назначены этой группе пользователей в совокупности.</span><span class="sxs-lookup"><span data-stu-id="ae376-121">Roles can then be assigned to this group of users collectively.</span></span> <span data-ttu-id="ae376-122">Объект **иазаппликатионграуп** может также включать другие объекты **иазаппликатионграуп** в качестве членов.</span><span class="sxs-lookup"><span data-stu-id="ae376-122">An **IAzApplicationGroup** object can also include other **IAzApplicationGroup** objects as members.</span></span> |
| [<span data-ttu-id="ae376-123">Добавление пользователей в группу приложений в скрипте</span><span class="sxs-lookup"><span data-stu-id="ae376-123">Adding Users to an Application Group in Script</span></span>](adding-users-to-an-application-group-in-script.md)                   | <span data-ttu-id="ae376-124">Группа приложений — это группа пользователей и групп пользователей.</span><span class="sxs-lookup"><span data-stu-id="ae376-124">An application group is a group of users and user groups.</span></span> <span data-ttu-id="ae376-125">Группа приложений может содержать другие группы приложений, поэтому группы пользователей могут быть вложенными.</span><span class="sxs-lookup"><span data-stu-id="ae376-125">An application group can contain other application groups, so groups of users can be nested.</span></span> <span data-ttu-id="ae376-126">Группа приложений представляется объектом [**иазаппликатионграуп**](/windows/desktop/api/Azroles/nn-azroles-iazapplicationgroup) .</span><span class="sxs-lookup"><span data-stu-id="ae376-126">An application group is represented by an [**IAzApplicationGroup**](/windows/desktop/api/Azroles/nn-azroles-iazapplicationgroup) object.</span></span>    |



 

 

 



