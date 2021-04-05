---
title: Публикация служб COM+
description: Службы на основе COM предоставляют прокси-сервер приложений в виде пакета установщика Windows (MSI).
ms.assetid: 38200a22-bea5-4967-a51a-e777b34f299d
ms.tgt_platform: multiple
keywords:
- Публикация служб COM+
- Active Directory, использование, публикация службы, службы COM+
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9044b72b4a604a4d863315963cd097be67f6afce
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/16/2019
ms.locfileid: "104067360"
---
# <a name="publishing-com-services"></a><span data-ttu-id="074f0-105">Публикация служб COM+</span><span class="sxs-lookup"><span data-stu-id="074f0-105">Publishing COM+ Services</span></span>

<span data-ttu-id="074f0-106">Службы на основе COM предоставляют прокси-сервер приложений в виде пакета установщика Windows (MSI).</span><span class="sxs-lookup"><span data-stu-id="074f0-106">COM-based services provide an application-proxy in the form of a Windows installer (MSI) package.</span></span> <span data-ttu-id="074f0-107">Этот MSI-файл содержит имя используемого сервера и другие необходимые элементы, такие как прокси, заглушки и библиотеки типов, необходимые для маршалинга.</span><span class="sxs-lookup"><span data-stu-id="074f0-107">This .msi file contains the server name to be used and other required elements, such as proxy/stubs and type libraries required for marshalling.</span></span> <span data-ttu-id="074f0-108">Оснастка "службы компонентов" автоматически создает эти прокси приложения для серверных приложений COM+.</span><span class="sxs-lookup"><span data-stu-id="074f0-108">The Component Services snap-in auto-generate these application proxies for COM+ Server applications.</span></span>

<span data-ttu-id="074f0-109">Прокси приложения публикуются в объектах политики Active Directory с помощью редактора групповая политика.</span><span class="sxs-lookup"><span data-stu-id="074f0-109">The application proxies are published into policy objects in Active Directory using the Group Policy Editor.</span></span> <span data-ttu-id="074f0-110">В клиентском приложении не требуется вмешательство.</span><span class="sxs-lookup"><span data-stu-id="074f0-110">No special intervention is required in the client application.</span></span> <span data-ttu-id="074f0-111">Учетная запись компьютера или пользователя на клиентском компьютере должна находиться в подразделении, настроенном для использования объекта политики, в котором публикуются прокси приложения.</span><span class="sxs-lookup"><span data-stu-id="074f0-111">The computer/user account on the client computer must be in an OU configured to use the policy object in which the application proxies are published.</span></span> <span data-ttu-id="074f0-112">Связыватель COM автоматически обнаруживает сервер с помощью каталога, когда клиент устанавливает экземпляр объектов.</span><span class="sxs-lookup"><span data-stu-id="074f0-112">The COM binder automatically locates the server by means of the directory when the client establishes an instance of the objects concerned.</span></span>

 

 




