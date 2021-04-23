---
description: С профилями пользователей используются следующие элементы API.
title: Справочник по профилям пользователей
ms.topic: article
ms.date: 05/31/2018
ms.assetid: 86871866-bb90-4287-9640-0a6cd136a800
api_name: ''
api_type: ''
api_location: ''
topic_type:
- kbArticle
ms.openlocfilehash: d5d4c4f585eda66674059f402dbd73f106a3e4f2
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "104986016"
---
# <a name="user-profiles-reference"></a><span data-ttu-id="501ec-103">Справочник по профилям пользователей</span><span class="sxs-lookup"><span data-stu-id="501ec-103">User Profiles Reference</span></span>

<span data-ttu-id="501ec-104">С профилями пользователей используются следующие элементы API.</span><span class="sxs-lookup"><span data-stu-id="501ec-104">The following API elements are used with user profiles.</span></span>

## <a name="functions"></a><span data-ttu-id="501ec-105">Функции</span><span class="sxs-lookup"><span data-stu-id="501ec-105">Functions</span></span>



| <span data-ttu-id="501ec-106">Компонент</span><span class="sxs-lookup"><span data-stu-id="501ec-106">Function</span></span>                                                                   | <span data-ttu-id="501ec-107">Описание</span><span class="sxs-lookup"><span data-stu-id="501ec-107">Description</span></span>                                                                                                   |
|----------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="501ec-108">**креатинвиронментблокк**</span><span class="sxs-lookup"><span data-stu-id="501ec-108">**CreateEnvironmentBlock**</span></span>](/windows/desktop/api/Userenv/nf-userenv-createenvironmentblock)                   | <span data-ttu-id="501ec-109">Извлекает переменные среды для указанного пользователя.</span><span class="sxs-lookup"><span data-stu-id="501ec-109">Retrieves the environment variables for the specified user.</span></span>                                                   |
| [<span data-ttu-id="501ec-110">**креатепрофиле**</span><span class="sxs-lookup"><span data-stu-id="501ec-110">**CreateProfile**</span></span>](/windows/desktop/api/Userenv/nf-userenv-createprofile)                                     | <span data-ttu-id="501ec-111">Создает новый профиль пользователя.</span><span class="sxs-lookup"><span data-stu-id="501ec-111">Creates a new user profile.</span></span> <span data-ttu-id="501ec-112">(Только для Windows Vista и более поздних версий.)</span><span class="sxs-lookup"><span data-stu-id="501ec-112">(Windows Vista and later only.)</span></span>                                                   |
| [<span data-ttu-id="501ec-113">**делетепрофиле**</span><span class="sxs-lookup"><span data-stu-id="501ec-113">**DeleteProfile**</span></span>](/windows/desktop/api/Userenv/nf-userenv-deleteprofilea)                                     | <span data-ttu-id="501ec-114">Удаляет профиль пользователя и все параметры, связанные с пользователем, с указанного компьютера.</span><span class="sxs-lookup"><span data-stu-id="501ec-114">Deletes the user profile and all user-related settings from the specified computer.</span></span>                           |
| [<span data-ttu-id="501ec-115">**дестройенвиронментблокк**</span><span class="sxs-lookup"><span data-stu-id="501ec-115">**DestroyEnvironmentBlock**</span></span>](/windows/desktop/api/Userenv/nf-userenv-destroyenvironmentblock)                 | <span data-ttu-id="501ec-116">Освобождает переменные среды, созданные функцией [**креатинвиронментблокк**](/windows/desktop/api/Userenv/nf-userenv-createenvironmentblock) .</span><span class="sxs-lookup"><span data-stu-id="501ec-116">Frees environment variables created by the [**CreateEnvironmentBlock**](/windows/desktop/api/Userenv/nf-userenv-createenvironmentblock) function.</span></span> |
| [<span data-ttu-id="501ec-117">**експанденвиронментстрингсфорусер**</span><span class="sxs-lookup"><span data-stu-id="501ec-117">**ExpandEnvironmentStringsForUser**</span></span>](/windows/desktop/api/Userenv/nf-userenv-expandenvironmentstringsforusera) | <span data-ttu-id="501ec-118">Развертывает исходную строку с помощью блока среды, установленного для указанного пользователя.</span><span class="sxs-lookup"><span data-stu-id="501ec-118">Expands the source string by using the environment block established for the specified user.</span></span>                  |
| [<span data-ttu-id="501ec-119">**жеталлусерспрофиледиректори**</span><span class="sxs-lookup"><span data-stu-id="501ec-119">**GetAllUsersProfileDirectory**</span></span>](/windows/desktop/api/Userenv/nf-userenv-getallusersprofiledirectorya)         | <span data-ttu-id="501ec-120">Возвращает путь к корню профиля всех пользователей.</span><span class="sxs-lookup"><span data-stu-id="501ec-120">Retrieves the path to the root of the All Users profile.</span></span>                                                      |
| [<span data-ttu-id="501ec-121">**жетдефаултусерпрофиледиректори**</span><span class="sxs-lookup"><span data-stu-id="501ec-121">**GetDefaultUserProfileDirectory**</span></span>](/windows/desktop/api/Userenv/nf-userenv-getdefaultuserprofiledirectorya)   | <span data-ttu-id="501ec-122">Возвращает путь к корню профиля пользователя по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="501ec-122">Retrieves the path to the root of the Default User profile.</span></span>                                                   |
| [<span data-ttu-id="501ec-123">**жетпрофилесдиректори**</span><span class="sxs-lookup"><span data-stu-id="501ec-123">**GetProfilesDirectory**</span></span>](/windows/desktop/api/Userenv/nf-userenv-getprofilesdirectorya)                       | <span data-ttu-id="501ec-124">Возвращает путь к корневому каталогу, в котором хранятся все профили пользователей.</span><span class="sxs-lookup"><span data-stu-id="501ec-124">Retrieves the path to the root directory where all user profiles are stored.</span></span>                                  |
| [<span data-ttu-id="501ec-125">**жетпрофилетипе**</span><span class="sxs-lookup"><span data-stu-id="501ec-125">**GetProfileType**</span></span>](/windows/desktop/api/Userenv/nf-userenv-getprofiletype)                                   | <span data-ttu-id="501ec-126">Возвращает тип профиля, загруженного для текущего пользователя.</span><span class="sxs-lookup"><span data-stu-id="501ec-126">Retrieves the type of profile loaded for the current user.</span></span>                                                    |
| [<span data-ttu-id="501ec-127">**жетусерпрофиледиректори**</span><span class="sxs-lookup"><span data-stu-id="501ec-127">**GetUserProfileDirectory**</span></span>](/windows/desktop/api/Userenv/nf-userenv-getuserprofiledirectorya)                 | <span data-ttu-id="501ec-128">Возвращает путь к корневому каталогу указанного профиля пользователя.</span><span class="sxs-lookup"><span data-stu-id="501ec-128">Retrieves the path to the root directory of the specified user's profile.</span></span>                                     |
| [<span data-ttu-id="501ec-129">**LoadUserProfile**</span><span class="sxs-lookup"><span data-stu-id="501ec-129">**LoadUserProfile**</span></span>](/windows/desktop/api/Userenv/nf-userenv-loaduserprofilea)                                 | <span data-ttu-id="501ec-130">Загружает профиль указанного пользователя.</span><span class="sxs-lookup"><span data-stu-id="501ec-130">Loads the specified user's profile.</span></span>                                                                           |
| [<span data-ttu-id="501ec-131">**унлоадусерпрофиле**</span><span class="sxs-lookup"><span data-stu-id="501ec-131">**UnloadUserProfile**</span></span>](/windows/desktop/api/Userenv/nf-userenv-unloaduserprofile)                             | <span data-ttu-id="501ec-132">Выгружает профиль пользователя, который был загружен функцией [**LoadUserProfile**](/windows/desktop/api/Userenv/nf-userenv-loaduserprofilea) .</span><span class="sxs-lookup"><span data-stu-id="501ec-132">Unloads a user's profile that was loaded by the [**LoadUserProfile**](/windows/desktop/api/Userenv/nf-userenv-loaduserprofilea) function.</span></span>          |



 

<span data-ttu-id="501ec-133">Функция [**креатеусерпрофиликс**](createuserprofileex.md) не поддерживается.</span><span class="sxs-lookup"><span data-stu-id="501ec-133">The [**CreateUserProfileEx**](createuserprofileex.md) function is not supported.</span></span>

## <a name="structures"></a><span data-ttu-id="501ec-134">Структуры</span><span class="sxs-lookup"><span data-stu-id="501ec-134">Structures</span></span>



| <span data-ttu-id="501ec-135">Структура</span><span class="sxs-lookup"><span data-stu-id="501ec-135">Structure</span></span>                          | <span data-ttu-id="501ec-136">Описание</span><span class="sxs-lookup"><span data-stu-id="501ec-136">Description</span></span>                                |
|------------------------------------|--------------------------------------------|
| [<span data-ttu-id="501ec-137">**FILEINFO**</span><span class="sxs-lookup"><span data-stu-id="501ec-137">**PROFILEINFO**</span></span>](/windows/desktop/api/Profinfo/ns-profinfo-profileinfoa) | <span data-ttu-id="501ec-138">Содержит сведения о профиле пользователя.</span><span class="sxs-lookup"><span data-stu-id="501ec-138">Contains information about a user profile.</span></span> |



 

 

 



