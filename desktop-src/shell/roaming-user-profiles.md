---
description: Если компьютер работает под Windows 2000 Server или более поздней версии в сети, пользователи могут хранить свои профили на сервере. Эти профили называются перемещаемыми профилями пользователей.
title: Проверка перемещаемых профилей пользователей
ms.topic: article
ms.date: 05/31/2018
ms.assetid: 8af06fdf-be99-4295-8f11-7d7f68e66956
api_name: ''
api_type: ''
api_location: ''
topic_type:
- kbArticle
ms.openlocfilehash: e3b95374b06c4efc665b231b4c7e1f1d81861dea
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "104985629"
---
# <a name="roaming-user-profiles"></a><span data-ttu-id="5a205-104">Проверка перемещаемых профилей пользователей</span><span class="sxs-lookup"><span data-stu-id="5a205-104">Roaming User Profiles</span></span>

<span data-ttu-id="5a205-105">Если компьютер работает под Windows 2000 Server или более поздней версии в сети, пользователи могут хранить свои профили на сервере.</span><span class="sxs-lookup"><span data-stu-id="5a205-105">If a computer is running Windows 2000 Server or later on a network, users can store their profiles on the server.</span></span> <span data-ttu-id="5a205-106">Эти профили называются *перемещаемыми профилями пользователей*.</span><span class="sxs-lookup"><span data-stu-id="5a205-106">These profiles are called *roaming user profiles*.</span></span>

<span data-ttu-id="5a205-107">Перемещаемые профили пользователей имеют следующие преимущества.</span><span class="sxs-lookup"><span data-stu-id="5a205-107">Roaming user profiles have the following advantages:</span></span>

-   <span data-ttu-id="5a205-108">Автоматическая доступность ресурсов.</span><span class="sxs-lookup"><span data-stu-id="5a205-108">Automatic resource availability.</span></span> <span data-ttu-id="5a205-109">Уникальный профиль пользователя автоматически становится доступным при входе на любой компьютер в сети.</span><span class="sxs-lookup"><span data-stu-id="5a205-109">A user's unique profile is automatically available when he or she logs on to any computer on the network.</span></span> <span data-ttu-id="5a205-110">Пользователям не нужно создавать профиль на каждом компьютере, который используется в сети.</span><span class="sxs-lookup"><span data-stu-id="5a205-110">Users do not need to create a profile on each computer they use on a network.</span></span>
-   <span data-ttu-id="5a205-111">Упрощенная замена и резервное копирование компьютера.</span><span class="sxs-lookup"><span data-stu-id="5a205-111">Simplified computer replacement and backup.</span></span> <span data-ttu-id="5a205-112">При необходимости замены компьютера пользователя его можно легко заменить, так как все сведения о профиле пользователя хранятся отдельно в сети независимо от отдельного компьютера.</span><span class="sxs-lookup"><span data-stu-id="5a205-112">When a user's computer must be replaced, it can be replaced easily because all of the user's profile information is maintained separately on the network, independent of an individual computer.</span></span> <span data-ttu-id="5a205-113">Когда пользователь впервые входит в систему на новом компьютере, копия профиля пользователя копируется на новый компьютер.</span><span class="sxs-lookup"><span data-stu-id="5a205-113">When the user logs on to the new computer for the first time, the server copy of the user's profile is copied to the new computer.</span></span>

<span data-ttu-id="5a205-114">Профиль пользователя не загружается автоматически при входе пользователя в систему с помощью функции [**LogonUser**](/windows/win32/api/winbase/nf-winbase-logonusera) .</span><span class="sxs-lookup"><span data-stu-id="5a205-114">The user's profile is not loaded automatically when the user is logged on using the [**LogonUser**](/windows/win32/api/winbase/nf-winbase-logonusera) function.</span></span> <span data-ttu-id="5a205-115">Чтобы программно загрузить перемещаемый профиль пользователя, используйте функцию [**LoadUserProfile**](/windows/desktop/api/Userenv/nf-userenv-loaduserprofilea) .</span><span class="sxs-lookup"><span data-stu-id="5a205-115">To load a roaming user profile programmatically, use the [**LoadUserProfile**](/windows/desktop/api/Userenv/nf-userenv-loaduserprofilea) function.</span></span> <span data-ttu-id="5a205-116">Чтобы выгрузить перемещаемый профиль пользователя, загруженный **LoadUserProfile**, вызовите функцию [**унлоадусерпрофиле**](/windows/desktop/api/Userenv/nf-userenv-unloaduserprofile) .</span><span class="sxs-lookup"><span data-stu-id="5a205-116">To unload a roaming user profile loaded by **LoadUserProfile**, call the [**UnloadUserProfile**](/windows/desktop/api/Userenv/nf-userenv-unloaduserprofile) function.</span></span>

 

 
