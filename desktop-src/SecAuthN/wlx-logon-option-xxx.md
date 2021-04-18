---
description: Значения используются параметром Двоптионс параметра Влкслогжедаутсас.
ms.assetid: a146427b-f3f1-4221-b2eb-ee7da451314a
title: WLX_LOGON_OPTION_XXX (Винвлкс. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3fa8909f562b87eb3a8147b0684d9676b9ac55d1
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "104347135"
---
# <a name="wlx_logon_option_xxx"></a><span data-ttu-id="36b34-103">\_параметр входа \_ влкс \_ xxx</span><span class="sxs-lookup"><span data-stu-id="36b34-103">WLX\_LOGON\_OPTION\_XXX</span></span>

<span data-ttu-id="36b34-104">\[Параметр ВЛКС \_ logon \_ \_ xxx константа больше не доступен для использования в Windows Server 2008 и Windows Vista.\]</span><span class="sxs-lookup"><span data-stu-id="36b34-104">\[The WLX\_LOGON\_OPTION\_XXX constant is no longer available for use as of Windows Server 2008 and Windows Vista.\]</span></span>

<span data-ttu-id="36b34-105">Значения **\_ параметра влкс \_ logon \_ xxx** используются параметром *двоптионс* объекта [**влкслогжедаутсас**](/windows/desktop/api/Winwlx/nf-winwlx-wlxloggedoutsas).</span><span class="sxs-lookup"><span data-stu-id="36b34-105">The **WLX\_LOGON\_OPTION\_XXX** values are used by the *dwOptions* parameter of [**WlxLoggedOutSAS**](/windows/desktop/api/Winwlx/nf-winwlx-wlxloggedoutsas).</span></span>

> [!Note]  
> <span data-ttu-id="36b34-106">Библиотеки DLL GINA не учитываются в Windows Vista.</span><span class="sxs-lookup"><span data-stu-id="36b34-106">GINA DLLs are ignored in Windows Vista.</span></span>

 

<span data-ttu-id="36b34-107">При успешном входе библиотека DLL GINA может использовать это значение для указания следующего параметра.</span><span class="sxs-lookup"><span data-stu-id="36b34-107">Upon a successful logon, your GINA DLL can use this value to specify the following option.</span></span>



| <span data-ttu-id="36b34-108">Константа</span><span class="sxs-lookup"><span data-stu-id="36b34-108">Constant</span></span>                                                                                                                                                                                          | <span data-ttu-id="36b34-109">Описание</span><span class="sxs-lookup"><span data-stu-id="36b34-109">Description</span></span>                                                                                                                                                                      |
|:--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="WLX_LOGON_OPT_NO_PROFILE"></span><span id="wlx_logon_opt_no_profile"></span><dl> <span data-ttu-id="36b34-110"><dt>**ВЛКС \_ входа в систему \_ \_ без \_ профиля**</dt></span><span class="sxs-lookup"><span data-stu-id="36b34-110"><dt>**WLX\_LOGON\_OPT\_NO\_PROFILE**</dt></span></span> </dl> | <span data-ttu-id="36b34-111">Указывает, что Winlogon не должен загружать профиль для вошедшего в систему пользователя.</span><span class="sxs-lookup"><span data-stu-id="36b34-111">Specifies that Winlogon must not load a profile for the logged-on user.</span></span> <span data-ttu-id="36b34-112">В этом случае либо библиотека DLL GINA загрузит профиль, либо пользователю не требуется профиль.</span><span class="sxs-lookup"><span data-stu-id="36b34-112">In this case, either your GINA DLL will load the profile or the user does not need a profile.</span></span><br/> |



## <a name="requirements"></a><span data-ttu-id="36b34-113">Требования</span><span class="sxs-lookup"><span data-stu-id="36b34-113">Requirements</span></span>



| <span data-ttu-id="36b34-114">Требование</span><span class="sxs-lookup"><span data-stu-id="36b34-114">Requirement</span></span> | <span data-ttu-id="36b34-115">Значение</span><span class="sxs-lookup"><span data-stu-id="36b34-115">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="36b34-116">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="36b34-116">Minimum supported client</span></span><br/> | <span data-ttu-id="36b34-117">Только для \[ классических приложений Windows XP\]</span><span class="sxs-lookup"><span data-stu-id="36b34-117">Windows XP \[desktop apps only\]</span></span><br/>                                         |
| <span data-ttu-id="36b34-118">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="36b34-118">Minimum supported server</span></span><br/> | <span data-ttu-id="36b34-119">\[Только для настольных приложений Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="36b34-119">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                |
| <span data-ttu-id="36b34-120">Окончание поддержки клиента</span><span class="sxs-lookup"><span data-stu-id="36b34-120">End of client support</span></span><br/>    | <span data-ttu-id="36b34-121">Windows XP</span><span class="sxs-lookup"><span data-stu-id="36b34-121">Windows XP</span></span><br/>                                                               |
| <span data-ttu-id="36b34-122">Поддержка конца сервера</span><span class="sxs-lookup"><span data-stu-id="36b34-122">End of server support</span></span><br/>    | <span data-ttu-id="36b34-123">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="36b34-123">Windows Server 2003</span></span><br/>                                                      |
| <span data-ttu-id="36b34-124">Header</span><span class="sxs-lookup"><span data-stu-id="36b34-124">Header</span></span><br/>                   | <dl> <span data-ttu-id="36b34-125"><dt>Винвлкс. h</dt></span><span class="sxs-lookup"><span data-stu-id="36b34-125"><dt>Winwlx.h</dt></span></span> </dl> |



 

 




