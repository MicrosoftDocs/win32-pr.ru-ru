---
title: Функции администрирования пользователей RAS
description: Используйте следующие функции для управления удаленными пользователями
ms.assetid: e58fa4a6-16d3-4953-bf21-887d08e25af7
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: cf8c1e7df962eff2064dac06da256f3a78e8ed17
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "104488161"
---
# <a name="ras-user-administration-functions"></a><span data-ttu-id="aca85-103">Функции администрирования пользователей RAS</span><span class="sxs-lookup"><span data-stu-id="aca85-103">RAS User Administration Functions</span></span>

<span data-ttu-id="aca85-104">Используйте следующие функции для управления удаленными пользователями:</span><span class="sxs-lookup"><span data-stu-id="aca85-104">Use the following functions to manage dial-up users:</span></span>

-   [<span data-ttu-id="aca85-105">**мпрадминжетпдксервер**</span><span class="sxs-lookup"><span data-stu-id="aca85-105">**MprAdminGetPDCServer**</span></span>](/windows/desktop/api/Mprapi/nf-mprapi-mpradmingetpdcserver)
-   [<span data-ttu-id="aca85-106">**мпрадминсендусермессаже**</span><span class="sxs-lookup"><span data-stu-id="aca85-106">**MprAdminSendUserMessage**</span></span>](/windows/desktop/api/Mprapi/nf-mprapi-mpradminsendusermessage)
-   [<span data-ttu-id="aca85-107">**мпрадминусержетинфо**</span><span class="sxs-lookup"><span data-stu-id="aca85-107">**MprAdminUserGetInfo**</span></span>](/windows/desktop/api/Mprapi/nf-mprapi-mpradminusergetinfo)
-   [<span data-ttu-id="aca85-108">**мпрадминусерсетинфо**</span><span class="sxs-lookup"><span data-stu-id="aca85-108">**MprAdminUserSetInfo**</span></span>](/windows/desktop/api/Mprapi/nf-mprapi-mpradminusersetinfo)

<span data-ttu-id="aca85-109">Чтобы получить список текущих пользователей в определенном домене, используйте функцию [**неткуеридисплайинформатион**](/windows/win32/api/lmaccess/nf-lmaccess-netquerydisplayinformation) .</span><span class="sxs-lookup"><span data-stu-id="aca85-109">To obtain a list of current users on a particular domain, use the [**NetQueryDisplayInformation**](/windows/win32/api/lmaccess/nf-lmaccess-netquerydisplayinformation) function.</span></span> <span data-ttu-id="aca85-110">Прототип этой функции находится в файле заголовка лмакцесс. h.</span><span class="sxs-lookup"><span data-stu-id="aca85-110">The prototype for this function is in the lmaccess.h header file.</span></span>

 

 