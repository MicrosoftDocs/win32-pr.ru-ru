---
description: Обязательный профиль пользователя — это особый тип предварительно настроенного перемещаемого профиля пользователя, который администраторы могут использовать для указания параметров пользователей.
title: Обязательные профили пользователей
ms.topic: article
ms.date: 05/31/2018
ms.assetid: 09616c7f-1cec-48a0-a953-d4ae35fbd2f6
api_name: ''
api_type: ''
api_location: ''
topic_type:
- kbArticle
ms.openlocfilehash: 744d35e92a279c5d8a8e8b239fa64bb1960e011a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104539470"
---
# <a name="mandatory-user-profiles"></a><span data-ttu-id="809a5-103">Обязательные профили пользователей</span><span class="sxs-lookup"><span data-stu-id="809a5-103">Mandatory User Profiles</span></span>

<span data-ttu-id="809a5-104">Обязательный профиль пользователя — это особый тип предварительно настроенного [перемещаемого профиля пользователя](roaming-user-profiles.md) , который администраторы могут использовать для указания параметров пользователей.</span><span class="sxs-lookup"><span data-stu-id="809a5-104">A mandatory user profile is a special type of pre-configured [roaming user profile](roaming-user-profiles.md) that administrators can use to specify settings for users.</span></span> <span data-ttu-id="809a5-105">При наличии обязательных профилей пользователей пользователь может изменить свой рабочий стол, но изменения не сохраняются при выходе пользователя из системы.</span><span class="sxs-lookup"><span data-stu-id="809a5-105">With mandatory user profiles, a user can modify his or her desktop, but the changes are not saved when the user logs off.</span></span> <span data-ttu-id="809a5-106">При следующем входе пользователя в систему загружается обязательный профиль пользователя, созданный администратором.</span><span class="sxs-lookup"><span data-stu-id="809a5-106">The next time the user logs on, the mandatory user profile created by the administrator is downloaded.</span></span> <span data-ttu-id="809a5-107">Существует два типа обязательных профилей: *обычные обязательные* профили и *необязательные* профили.</span><span class="sxs-lookup"><span data-stu-id="809a5-107">There are two types of mandatory profiles: *normal mandatory* profiles and *super-mandatory* profiles.</span></span>

<span data-ttu-id="809a5-108">Профили пользователей становятся обязательными профилями, когда администратор переименовывает файл NTuser. dat (куст реестра) на сервере в NTuser. Man.</span><span class="sxs-lookup"><span data-stu-id="809a5-108">User profiles become mandatory profiles when the administrator renames the NTuser.dat file (the registry hive) on the server to NTuser.man.</span></span> <span data-ttu-id="809a5-109">Расширение. Man заставляет профиль пользователя быть профилем только для чтения.</span><span class="sxs-lookup"><span data-stu-id="809a5-109">The .man extension causes the user profile to be a read-only profile.</span></span>

<span data-ttu-id="809a5-110">Профили пользователей становятся *необязательными* , если имя папки в пути к профилю заканчивается на. Man; Например, \\ \\ Server \\ Share \\ мандаторипрофиле. man \\ .</span><span class="sxs-lookup"><span data-stu-id="809a5-110">User profiles become *super-mandatory* when the folder name of the profile path ends in .man; for example, \\\\server\\share\\mandatoryprofile.man\\.</span></span>

<span data-ttu-id="809a5-111">Необязательные профили пользователей похожи на обычные обязательные профили, за исключением того, что пользователи с необязательными профилями не могут войти в систему, если сервер, на котором хранится обязательный профиль, недоступен.</span><span class="sxs-lookup"><span data-stu-id="809a5-111">Super-mandatory user profiles are similar to normal mandatory profiles, with the exception that users who have super-mandatory profiles cannot log on when the server that stores the mandatory profile is unavailable.</span></span> <span data-ttu-id="809a5-112">Пользователи с обычными обязательными профилями могут войти в систему, используя локально кэшированную копию обязательного профиля.</span><span class="sxs-lookup"><span data-stu-id="809a5-112">Users with normal mandatory profiles can log on with the locally cached copy of the mandatory profile.</span></span>

<span data-ttu-id="809a5-113">Только системные администраторы могут вносить изменения в обязательные профили пользователей.</span><span class="sxs-lookup"><span data-stu-id="809a5-113">Only system administrators can make changes to mandatory user profiles.</span></span>

 

 



