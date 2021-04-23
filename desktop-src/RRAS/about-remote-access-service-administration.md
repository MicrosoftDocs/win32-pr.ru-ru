---
title: Сведения об администрировании службы удаленного доступа
description: Windows 2000 и более поздние операционные системы предоставляют набор функций для администрирования разрешений пользователей и портов на серверах RAS.
ms.assetid: 95c6dceb-e3a9-421e-b43f-88b18b9e64ff
keywords:
- RRAS службы маршрутизации и удаленного доступа, администрирование RAS
- Служба маршрутизации и удаленного доступа RRAS, администрирование RAS, описание
- Администрирование RAS RRAS
- Администрирование RAS, описание
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 73bdb55049e99b6d3df9980fc35879341b488531
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/16/2019
ms.locfileid: "105672079"
---
# <a name="about-remote-access-service-administration"></a><span data-ttu-id="667fa-107">Сведения об администрировании службы удаленного доступа</span><span class="sxs-lookup"><span data-stu-id="667fa-107">About Remote Access Service Administration</span></span>

<span data-ttu-id="667fa-108">Windows 2000 и более поздние операционные системы предоставляют набор функций для администрирования разрешений пользователей и портов на серверах RAS.</span><span class="sxs-lookup"><span data-stu-id="667fa-108">Windows 2000 and later operating systems provide a set of functions for administering user permissions and ports on RAS servers.</span></span> <span data-ttu-id="667fa-109">С помощью этих функций можно разработать приложение удаленного администрирования сервера для выполнения следующих задач.</span><span class="sxs-lookup"><span data-stu-id="667fa-109">Using these functions, you can develop a RAS server administration application to perform the following tasks:</span></span>

-   <span data-ttu-id="667fa-110">Перечисление пользователей, имеющих указанный набор разрешений RAS</span><span class="sxs-lookup"><span data-stu-id="667fa-110">Enumerate those users who have a specified set of RAS permissions</span></span>
-   <span data-ttu-id="667fa-111">Назначение или Отмена разрешений RAS для указанного пользователя</span><span class="sxs-lookup"><span data-stu-id="667fa-111">Assign or revoke RAS permissions for a specified user</span></span>
-   <span data-ttu-id="667fa-112">Перечисление настроенных портов на сервере удаленного доступа</span><span class="sxs-lookup"><span data-stu-id="667fa-112">Enumerate the configured ports on a RAS server</span></span>
-   <span data-ttu-id="667fa-113">Получение сведений и статистики об указанном порте на сервере удаленного доступа</span><span class="sxs-lookup"><span data-stu-id="667fa-113">Get information and statistics about a specified port on a RAS server</span></span>
-   <span data-ttu-id="667fa-114">Сброс счетчиков статистики для указанного порта</span><span class="sxs-lookup"><span data-stu-id="667fa-114">Reset the statistics counters for a specified port</span></span>
-   <span data-ttu-id="667fa-115">Отключение указанного порта</span><span class="sxs-lookup"><span data-stu-id="667fa-115">Disconnect a specified port</span></span>

<span data-ttu-id="667fa-116">Кроме того, можно установить библиотеку DLL администрирования сервера RAS для аудита подключений пользователей и назначения IP-адресов пользователям, входящим в их набор.</span><span class="sxs-lookup"><span data-stu-id="667fa-116">You can also install a RAS server administration DLL to audit user connections and assign IP addresses to dial-in users.</span></span> <span data-ttu-id="667fa-117">Библиотека DLL экспортирует набор функций, которые сервер удаленного доступа вызывает каждый раз, когда пользователь пытается подключиться или отключиться.</span><span class="sxs-lookup"><span data-stu-id="667fa-117">The DLL exports a set of functions that the RAS server calls whenever a user tries to connect or disconnect.</span></span>

<span data-ttu-id="667fa-118">В этой документации описаны следующие темы:</span><span class="sxs-lookup"><span data-stu-id="667fa-118">This documentation describes the following topics:</span></span>

-   [<span data-ttu-id="667fa-119">Сравнение функций: Windows 2000 и распространяемый компонент RRAS</span><span class="sxs-lookup"><span data-stu-id="667fa-119">Function Comparison: Windows 2000 vs. RRAS Redistributable</span></span>](function-comparison-windows-2000-versus-rras-redistributable.md)
-   [<span data-ttu-id="667fa-120">Администрирование пользователей RAS</span><span class="sxs-lookup"><span data-stu-id="667fa-120">RAS User Administration</span></span>](ras-user-administration.md)
-   [<span data-ttu-id="667fa-121">Администрирование сервера и порта RAS</span><span class="sxs-lookup"><span data-stu-id="667fa-121">RAS Server and Port Administration</span></span>](ras-server-and-port-administration.md)
-   [<span data-ttu-id="667fa-122">Библиотека DLL администрирования RAS</span><span class="sxs-lookup"><span data-stu-id="667fa-122">RAS Administration DLL</span></span>](ras-administration-dll.md)
-   [<span data-ttu-id="667fa-123">Установка реестра DLL администрирования RAS</span><span class="sxs-lookup"><span data-stu-id="667fa-123">RAS Administration DLL Registry Setup</span></span>](ras-administration-dll-registry-setup.md)

 

 




