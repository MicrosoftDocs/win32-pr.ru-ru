---
description: Система автоматически создает профиль локального пользователя для каждого пользователя, когда пользователь входит в систему в первый раз. Система автоматически сохраняет параметры для рабочей среды каждого пользователя в профиле пользователя на локальном компьютере.
title: Профили локальных пользователей
ms.topic: article
ms.date: 05/31/2018
ms.assetid: 0e6c060e-025e-4d00-9b92-4f3b7bf66dda
api_name: ''
api_type: ''
api_location: ''
topic_type:
- kbArticle
ms.openlocfilehash: ba330189b11875198ce40ffdb9dd34925e3adc4b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "104985668"
---
# <a name="local-user-profiles"></a><span data-ttu-id="38ba7-104">Профили локальных пользователей</span><span class="sxs-lookup"><span data-stu-id="38ba7-104">Local User Profiles</span></span>

<span data-ttu-id="38ba7-105">Для безопасности Windows требуется профиль пользователя для каждой учетной записи пользователя на компьютере.</span><span class="sxs-lookup"><span data-stu-id="38ba7-105">Windows security requires a user profile for each user account on a computer.</span></span> <span data-ttu-id="38ba7-106">Система автоматически создает *профиль локального пользователя* для каждого пользователя, когда пользователь входит в систему в первый раз.</span><span class="sxs-lookup"><span data-stu-id="38ba7-106">The system automatically creates a *local user profile* for each user when the user logs on to the computer for the first time.</span></span> <span data-ttu-id="38ba7-107">Система автоматически сохраняет параметры для рабочей среды каждого пользователя в профиле пользователя на локальном компьютере.</span><span class="sxs-lookup"><span data-stu-id="38ba7-107">The system automatically maintains the settings for each user's work environment in a user profile on the local computer.</span></span>

<span data-ttu-id="38ba7-108">Windows Vista и более поздние версии. Управление профилями пользователей осуществляется с помощью элемента панели управления **учетные записи пользователей** .</span><span class="sxs-lookup"><span data-stu-id="38ba7-108">Windows Vista and later: User profiles are managed through the **User Accounts** control panel item.</span></span>

<span data-ttu-id="38ba7-109">Windows 2000 и Windows XP. чтобы скопировать или удалить профиль пользователя, выберите элемент " **система** " в панели управления, откройте вкладку " **Дополнительно** " и нажмите кнопку " **Параметры** " в области **профиля пользователя** .</span><span class="sxs-lookup"><span data-stu-id="38ba7-109">Windows 2000 and Windows XP: To copy or delete a user profile, select **System** from the Control Panel, then the **Advanced** tab, and then the **Settings** button in the **User Profile** area.</span></span>

<span data-ttu-id="38ba7-110">Профиль пользователя не загружается автоматически при входе пользователя в систему с помощью функции [**LogonUser**](/windows/win32/api/winbase/nf-winbase-logonusera) .</span><span class="sxs-lookup"><span data-stu-id="38ba7-110">The user's profile is not loaded automatically when the user is logged on using the [**LogonUser**](/windows/win32/api/winbase/nf-winbase-logonusera) function.</span></span> <span data-ttu-id="38ba7-111">Чтобы загрузить профиль пользователя программным путем, используйте функцию [**LoadUserProfile**](/windows/desktop/api/Userenv/nf-userenv-loaduserprofilea) .</span><span class="sxs-lookup"><span data-stu-id="38ba7-111">To load a user profile programmatically, use the [**LoadUserProfile**](/windows/desktop/api/Userenv/nf-userenv-loaduserprofilea) function.</span></span> <span data-ttu-id="38ba7-112">Чтобы выгрузить профиль пользователя, загруженный с помощью **LoadUserProfile**, вызовите функцию [**унлоадусерпрофиле**](/windows/desktop/api/Userenv/nf-userenv-unloaduserprofile) .</span><span class="sxs-lookup"><span data-stu-id="38ba7-112">To unload a user profile loaded by **LoadUserProfile**, call the [**UnloadUserProfile**](/windows/desktop/api/Userenv/nf-userenv-unloaduserprofile) function.</span></span>

 

 
