---
title: Администрирование сервера удаленного доступа
description: Windows NT Server 4,0 предоставляет набор функций для администрирования разрешений пользователей и портов на серверах RAS Windows NT/Windows 2000.
ms.assetid: 0b517c4d-dcae-477b-b274-c3773bd172ef
keywords:
- Администрирование сервера, RAS
- Администрирование, сервер RAS
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e096610e1cfe986c504a017f4d2b0d1033a6e6d0
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/16/2019
ms.locfileid: "104258865"
---
# <a name="ras-server-administration"></a><span data-ttu-id="b8abc-105">Администрирование сервера удаленного доступа</span><span class="sxs-lookup"><span data-stu-id="b8abc-105">RAS Server Administration</span></span>

<span data-ttu-id="b8abc-106">Windows NT Server 4,0 предоставляет набор функций для администрирования разрешений пользователей и портов на серверах RAS Windows NT/Windows 2000.</span><span class="sxs-lookup"><span data-stu-id="b8abc-106">Windows NT Server 4.0 provides a set of functions for administering user permissions and ports on Windows NT/Windows 2000 RAS servers.</span></span> <span data-ttu-id="b8abc-107">Windows 95 не поддерживает эти функции.</span><span class="sxs-lookup"><span data-stu-id="b8abc-107">Windows 95 does not support these functions.</span></span> <span data-ttu-id="b8abc-108">С помощью этих функций можно разработать приложение удаленного администрирования сервера для выполнения следующих задач.</span><span class="sxs-lookup"><span data-stu-id="b8abc-108">Using these functions, you can develop a RAS server administration application to perform the following tasks:</span></span>

-   <span data-ttu-id="b8abc-109">Перечисление пользователей, имеющих указанный набор разрешений RAS</span><span class="sxs-lookup"><span data-stu-id="b8abc-109">Enumerate those users who have a specified set of RAS permissions</span></span>
-   <span data-ttu-id="b8abc-110">Назначение или Отмена разрешений RAS для указанного пользователя</span><span class="sxs-lookup"><span data-stu-id="b8abc-110">Assign or revoke RAS permissions for a specified user</span></span>
-   <span data-ttu-id="b8abc-111">Перечисление настроенных портов на сервере удаленного доступа</span><span class="sxs-lookup"><span data-stu-id="b8abc-111">Enumerate the configured ports on a RAS server</span></span>
-   <span data-ttu-id="b8abc-112">Получение сведений и статистики об указанном порте на сервере удаленного доступа</span><span class="sxs-lookup"><span data-stu-id="b8abc-112">Get information and statistics about a specified port on a RAS server</span></span>
-   <span data-ttu-id="b8abc-113">Сброс счетчиков статистики для указанного порта</span><span class="sxs-lookup"><span data-stu-id="b8abc-113">Reset the statistics counters for a specified port</span></span>
-   <span data-ttu-id="b8abc-114">Отключение указанного порта</span><span class="sxs-lookup"><span data-stu-id="b8abc-114">Disconnect a specified port</span></span>

<span data-ttu-id="b8abc-115">Кроме того, можно установить библиотеку DLL администрирования сервера RAS для аудита подключений пользователей и назначения IP-адресов пользователям, входящим в их набор.</span><span class="sxs-lookup"><span data-stu-id="b8abc-115">You can also install a RAS server administration DLL for auditing user connections and assigning IP addresses to dial-in users.</span></span> <span data-ttu-id="b8abc-116">Библиотека DLL экспортирует набор функций, которые сервер удаленного доступа вызывает каждый раз, когда пользователь пытается подключиться или отключиться.</span><span class="sxs-lookup"><span data-stu-id="b8abc-116">The DLL exports a set of functions that the RAS server calls whenever a user tries to connect or disconnect.</span></span>

 

 




