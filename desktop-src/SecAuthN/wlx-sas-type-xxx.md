---
description: Значения определяют конкретный тип SAS.
ms.assetid: c0a1269b-f9d4-49e1-89ca-526fef148134
title: WLX_SAS_TYPE_XXX (Винвлкс. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0a75c7d7a71855700c4c8c233db3cfc18e06b9d7
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "105647533"
---
# <a name="wlx_sas_type_xxx"></a><span data-ttu-id="5e73e-103">\_тип SAS \_ влкс \_ xxx</span><span class="sxs-lookup"><span data-stu-id="5e73e-103">WLX\_SAS\_TYPE\_XXX</span></span>

<span data-ttu-id="5e73e-104">\[\_ \_ Константа типа SAS влкс \_ xxx больше не доступна для использования в Windows Server 2008 и Windows Vista.\]</span><span class="sxs-lookup"><span data-stu-id="5e73e-104">\[The WLX\_SAS\_TYPE\_XXX constant is no longer available for use as of Windows Server 2008 and Windows Vista.\]</span></span>

<span data-ttu-id="5e73e-105">Значения **\_ типа влкс \_ SAS \_ xxx** определяют конкретный тип SAS.</span><span class="sxs-lookup"><span data-stu-id="5e73e-105">The **WLX\_SAS\_TYPE\_XXX** values define a specific SAS type.</span></span>

> [!Note]  
> <span data-ttu-id="5e73e-106">Библиотеки DLL GINA не учитываются в Windows Vista.</span><span class="sxs-lookup"><span data-stu-id="5e73e-106">GINA DLLs are ignored in Windows Vista.</span></span>

 

<span data-ttu-id="5e73e-107">Все значения от нуля до 127 зарезервированы для типов, определенных корпорацией Майкрософт.</span><span class="sxs-lookup"><span data-stu-id="5e73e-107">All values from zero to 127 are reserved for Microsoft-defined types.</span></span> <span data-ttu-id="5e73e-108">Значения свыше 127 доступны для определяемых пользователем типов.</span><span class="sxs-lookup"><span data-stu-id="5e73e-108">Values above 127 are available for customer-defined types.</span></span> <span data-ttu-id="5e73e-109">Следующие типы передаются в функции, имеющие параметр *двсастипе* .</span><span class="sxs-lookup"><span data-stu-id="5e73e-109">The following types are passed to functions that have a *dwSasType* parameter.</span></span>



| <span data-ttu-id="5e73e-110">Константа</span><span class="sxs-lookup"><span data-stu-id="5e73e-110">Constant</span></span>                                                                                                                                                                                                         | <span data-ttu-id="5e73e-111">Описание</span><span class="sxs-lookup"><span data-stu-id="5e73e-111">Description</span></span>                                                                                                                                              |
|:-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:---------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="WLX_SAS_TYPE_CTRL_ALT_DEL"></span><span id="wlx_sas_type_ctrl_alt_del"></span><dl> <span data-ttu-id="5e73e-112"><dt>**ВЛКС \_ SAS \_ Type \_ CTRL \_ Alt \_ Del**</dt></span><span class="sxs-lookup"><span data-stu-id="5e73e-112"><dt>**WLX\_SAS\_TYPE\_CTRL\_ALT\_DEL**</dt></span></span> </dl>            | <span data-ttu-id="5e73e-113">Указывает, что пользователь ввел стандартную комбинацию клавиш CTRL + ALT + DEL.</span><span class="sxs-lookup"><span data-stu-id="5e73e-113">Indicates a user has typed the standard CTRL+ALT+DEL SAS.</span></span><br/>                                                                                     |
| <span id="WLX_SAS_TYPE_SC_INSERT"></span><span id="wlx_sas_type_sc_insert"></span><dl> <span data-ttu-id="5e73e-114"><dt>**ВЛКС \_ SAS \_ Type \_ SC \_ INSERT**</dt></span><span class="sxs-lookup"><span data-stu-id="5e73e-114"><dt>**WLX\_SAS\_TYPE\_SC\_INSERT**</dt></span></span> </dl>                      | <span data-ttu-id="5e73e-115">Указывает, что [*смарт-карта*](../secgloss/s-gly.md) вставлена в совместимое устройство.</span><span class="sxs-lookup"><span data-stu-id="5e73e-115">Indicates that a [*smart card*](../secgloss/s-gly.md) has been inserted into a compatible device.</span></span><br/> |
| <span id="WLX_SAS_TYPE_SC_REMOVE"></span><span id="wlx_sas_type_sc_remove"></span><dl> <span data-ttu-id="5e73e-116"><dt>**\_тип SAS \_ влкс \_ SC \_ Remove**</dt></span><span class="sxs-lookup"><span data-stu-id="5e73e-116"><dt>**WLX\_SAS\_TYPE\_SC\_REMOVE**</dt></span></span> </dl>                      | <span data-ttu-id="5e73e-117">Указывает, что смарт-карта была удалена из совместимого устройства.</span><span class="sxs-lookup"><span data-stu-id="5e73e-117">Indicates that a smart card has been removed from a compatible device.</span></span><br/>                                                                        |
| <span id="WLX_SAS_TYPE_SCRNSVR_ACTIVITY"></span><span id="wlx_sas_type_scrnsvr_activity"></span><dl> <span data-ttu-id="5e73e-118"><dt>**\_ \_ \_ действие СКРНСВР типа SAS \_ влкс**</dt></span><span class="sxs-lookup"><span data-stu-id="5e73e-118"><dt>**WLX\_SAS\_TYPE\_SCRNSVR\_ACTIVITY**</dt></span></span> </dl> | <span data-ttu-id="5e73e-119">Указывает, что при активной заставке с помощью клавиатуры или мыши произошли действия.</span><span class="sxs-lookup"><span data-stu-id="5e73e-119">Indicates that keyboard or mouse activity occurred while a secure screen saver was active.</span></span><br/>                                                    |
| <span id="WLX_SAS_TYPE_SCRNSVR_TIMEOUT"></span><span id="wlx_sas_type_scrnsvr_timeout"></span><dl> <span data-ttu-id="5e73e-120"><dt>**ВЛКС \_ SAS \_ типа \_ скрнсвр \_ timeout**</dt></span><span class="sxs-lookup"><span data-stu-id="5e73e-120"><dt>**WLX\_SAS\_TYPE\_SCRNSVR\_TIMEOUT**</dt></span></span> </dl>    | <span data-ttu-id="5e73e-121">Указывает, что активация заставки произошел из-за неактивности клавиатуры и мыши.</span><span class="sxs-lookup"><span data-stu-id="5e73e-121">Indicates that screen saver activation has occurred due to keyboard and mouse inactivity.</span></span><br/>                                                     |
| <span id="WLX_SAS_TYPE_TIMEOUT"></span><span id="wlx_sas_type_timeout"></span><dl> <span data-ttu-id="5e73e-122"><dt>**\_ \_ время ожидания типа SAS влкс \_**</dt></span><span class="sxs-lookup"><span data-stu-id="5e73e-122"><dt>**WLX\_SAS\_TYPE\_TIMEOUT**</dt></span></span> </dl>                             | <span data-ttu-id="5e73e-123">Указывает, что в течение указанного периода ожидания не было получено ни одного пользовательского ввода.</span><span class="sxs-lookup"><span data-stu-id="5e73e-123">Indicates that no user input was received within the specified time-out period.</span></span><br/>                                                               |
| <span id="WLX_SAS_TYPE_USER_LOGOFF"></span><span id="wlx_sas_type_user_logoff"></span><dl> <span data-ttu-id="5e73e-124"><dt>**\_тип SAS \_ влкс \_ \_ Выход пользователя**</dt></span><span class="sxs-lookup"><span data-stu-id="5e73e-124"><dt>**WLX\_SAS\_TYPE\_USER\_LOGOFF**</dt></span></span> </dl>                | <span data-ttu-id="5e73e-125">Показывает, что пользователь вышел из системы.</span><span class="sxs-lookup"><span data-stu-id="5e73e-125">Indicates the user is being logged off the system.</span></span><br/>                                                                                            |



## <a name="requirements"></a><span data-ttu-id="5e73e-126">Требования</span><span class="sxs-lookup"><span data-stu-id="5e73e-126">Requirements</span></span>



| <span data-ttu-id="5e73e-127">Требование</span><span class="sxs-lookup"><span data-stu-id="5e73e-127">Requirement</span></span> | <span data-ttu-id="5e73e-128">Значение</span><span class="sxs-lookup"><span data-stu-id="5e73e-128">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="5e73e-129">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="5e73e-129">Minimum supported client</span></span><br/> | <span data-ttu-id="5e73e-130">Только для \[ классических приложений Windows XP\]</span><span class="sxs-lookup"><span data-stu-id="5e73e-130">Windows XP \[desktop apps only\]</span></span><br/>                                         |
| <span data-ttu-id="5e73e-131">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="5e73e-131">Minimum supported server</span></span><br/> | <span data-ttu-id="5e73e-132">\[Только для настольных приложений Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="5e73e-132">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                |
| <span data-ttu-id="5e73e-133">Окончание поддержки клиента</span><span class="sxs-lookup"><span data-stu-id="5e73e-133">End of client support</span></span><br/>    | <span data-ttu-id="5e73e-134">Windows XP</span><span class="sxs-lookup"><span data-stu-id="5e73e-134">Windows XP</span></span><br/>                                                               |
| <span data-ttu-id="5e73e-135">Поддержка конца сервера</span><span class="sxs-lookup"><span data-stu-id="5e73e-135">End of server support</span></span><br/>    | <span data-ttu-id="5e73e-136">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="5e73e-136">Windows Server 2003</span></span><br/>                                                      |
| <span data-ttu-id="5e73e-137">Header</span><span class="sxs-lookup"><span data-stu-id="5e73e-137">Header</span></span><br/>                   | <dl> <span data-ttu-id="5e73e-138"><dt>Винвлкс. h</dt></span><span class="sxs-lookup"><span data-stu-id="5e73e-138"><dt>Winwlx.h</dt></span></span> </dl> |



 

 
