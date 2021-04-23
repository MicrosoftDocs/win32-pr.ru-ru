---
description: Настройка библиотечных приложений
ms.assetid: db375e0f-74ca-44df-918a-b0e48742a594
title: Настройка библиотечных приложений
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e51e00626d42044797881ccb86553ddfda38a089
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104072399"
---
# <a name="configuring-library-applications"></a><span data-ttu-id="4238f-103">Настройка библиотечных приложений</span><span class="sxs-lookup"><span data-stu-id="4238f-103">Configuring Library Applications</span></span>

<span data-ttu-id="4238f-104">Поскольку приложения библиотеки COM+ выполняются в процессе клиента, настраиваемые элементы для библиотечных приложений значительно отличаются от серверных приложений.</span><span class="sxs-lookup"><span data-stu-id="4238f-104">Because COM+ library applications run in the client's process, the configurable elements for library applications are considerably different than for server applications.</span></span> <span data-ttu-id="4238f-105">Вы не можете настроить какой-либо аспект приложения, определяемый ведущим процессом.</span><span class="sxs-lookup"><span data-stu-id="4238f-105">You cannot configure any aspect of the application that is determined by the hosting process.</span></span>

<span data-ttu-id="4238f-106">На уровне приложения несколько параметров ограничены или недоступны для библиотечных приложений.</span><span class="sxs-lookup"><span data-stu-id="4238f-106">At the application level, several settings are either limited or unavailable for library applications.</span></span> <span data-ttu-id="4238f-107">Эти ограничения описаны в следующей таблице.</span><span class="sxs-lookup"><span data-stu-id="4238f-107">These constraints are described in the following table:</span></span>



| <span data-ttu-id="4238f-108">attribute</span><span class="sxs-lookup"><span data-stu-id="4238f-108">Attribute</span></span>                                       | <span data-ttu-id="4238f-109">Описание</span><span class="sxs-lookup"><span data-stu-id="4238f-109">Description</span></span>                                                                                                                                                                                                                                   |
|-------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="4238f-110">Уровень безопасности</span><span class="sxs-lookup"><span data-stu-id="4238f-110">Security level</span></span><br/>                       | <span data-ttu-id="4238f-111">Необходимо выбрать проверки доступа на уровне компонентов.</span><span class="sxs-lookup"><span data-stu-id="4238f-111">You must choose component-level access checks.</span></span> <span data-ttu-id="4238f-112">Приложение библиотеки не может влиять на проверки доступа на уровне процесса.</span><span class="sxs-lookup"><span data-stu-id="4238f-112">The library application cannot influence process-level access checks.</span></span> <span data-ttu-id="4238f-113">См. раздел [Настройка уровня безопасности для проверок доступа](setting-a-security-level-for-access-checks.md).</span><span class="sxs-lookup"><span data-stu-id="4238f-113">See [Setting a Security Level for Access Checks](setting-a-security-level-for-access-checks.md).</span></span><br/>             |
| <span data-ttu-id="4238f-114">Включение или отключение проверки подлинности</span><span class="sxs-lookup"><span data-stu-id="4238f-114">Enabling or disabling authentication</span></span><br/> | <span data-ttu-id="4238f-115">Можно указать, будет ли приложение библиотеки участвовать в проверке подлинности, выполненной ведущим процессом.</span><span class="sxs-lookup"><span data-stu-id="4238f-115">You can indicate whether the library application will participate in authentication performed by the host process.</span></span> <span data-ttu-id="4238f-116">См. раздел [Включение проверки подлинности для библиотечного приложения](enabling-authentication-for-a-library-application.md).</span><span class="sxs-lookup"><span data-stu-id="4238f-116">See [Enabling Authentication for a Library Application](enabling-authentication-for-a-library-application.md).</span></span><br/> |
| <span data-ttu-id="4238f-117">Уровень олицетворения</span><span class="sxs-lookup"><span data-stu-id="4238f-117">Impersonation level</span></span><br/>                  | <span data-ttu-id="4238f-118">Доступ.</span><span class="sxs-lookup"><span data-stu-id="4238f-118">Unavailable.</span></span> <span data-ttu-id="4238f-119">Используется параметр хост-процесса.</span><span class="sxs-lookup"><span data-stu-id="4238f-119">The setting of the host process is used.</span></span> <br/>                                                                                                                                                                             |
| <span data-ttu-id="4238f-120">Удостоверение безопасности</span><span class="sxs-lookup"><span data-stu-id="4238f-120">Security identity</span></span><br/>                    | <span data-ttu-id="4238f-121">Доступ.</span><span class="sxs-lookup"><span data-stu-id="4238f-121">Unavailable.</span></span> <span data-ttu-id="4238f-122">Приложение выполняется с удостоверением хостового процесса.</span><span class="sxs-lookup"><span data-stu-id="4238f-122">The application runs under the identity of the host process.</span></span><br/>                                                                                                                                                          |
| <span data-ttu-id="4238f-123">Завершение работы серверного процесса</span><span class="sxs-lookup"><span data-stu-id="4238f-123">Server process shutdown</span></span><br/>              | <span data-ttu-id="4238f-124">Доступ.</span><span class="sxs-lookup"><span data-stu-id="4238f-124">Unavailable.</span></span><br/>                                                                                                                                                                                                                       |
| <span data-ttu-id="4238f-125">Включить поддержку 3 ГБ</span><span class="sxs-lookup"><span data-stu-id="4238f-125">Enable 3-GB support</span></span><br/>                  | <span data-ttu-id="4238f-126">Доступ.</span><span class="sxs-lookup"><span data-stu-id="4238f-126">Unavailable.</span></span><br/>                                                                                                                                                                                                                       |
| <span data-ttu-id="4238f-127">Запустить в отладчике</span><span class="sxs-lookup"><span data-stu-id="4238f-127">Launch in debugger</span></span><br/>                   | <span data-ttu-id="4238f-128">Доступ.</span><span class="sxs-lookup"><span data-stu-id="4238f-128">Unavailable.</span></span><br/>                                                                                                                                                                                                                       |
| <span data-ttu-id="4238f-129">Включить CRM</span><span class="sxs-lookup"><span data-stu-id="4238f-129">Enable CRM</span></span><br/>                           | <span data-ttu-id="4238f-130">Доступ.</span><span class="sxs-lookup"><span data-stu-id="4238f-130">Unavailable.</span></span><br/>                                                                                                                                                                                                                       |
| <span data-ttu-id="4238f-131">Управление</span><span class="sxs-lookup"><span data-stu-id="4238f-131">Queuing</span></span><br/>                              | <span data-ttu-id="4238f-132">Доступ.</span><span class="sxs-lookup"><span data-stu-id="4238f-132">Unavailable.</span></span><br/>                                                                                                                                                                                                                       |



 

## <a name="related-topics"></a><span data-ttu-id="4238f-133">См. также</span><span class="sxs-lookup"><span data-stu-id="4238f-133">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="4238f-134">Общие сведения о приложении COM+</span><span class="sxs-lookup"><span data-stu-id="4238f-134">COM+ Application Overview</span></span>](com--application-overview.md)
</dt> </dl>

 

 




