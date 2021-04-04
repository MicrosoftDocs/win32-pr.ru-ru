---
description: Только администратор компьютера или пользователи в группе "журналы производительности" может записывать и просматривать данные счетчиков.
ms.assetid: 85c5f38f-d8d7-4203-adc0-4869d6078351
title: Поддержка ограниченного доступа пользователей
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6a22a1259939cbd2bc77694e962e23f29c82e291
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "103909739"
---
# <a name="limited-user-access-support"></a><span data-ttu-id="73394-103">Поддержка ограниченного доступа пользователей</span><span class="sxs-lookup"><span data-stu-id="73394-103">Limited User Access Support</span></span>

<span data-ttu-id="73394-104">Записывать данные счетчика могут только администраторы компьютера или пользователи из группы пользователей "журналы производительности".</span><span class="sxs-lookup"><span data-stu-id="73394-104">Only the administrator of the computer or users in the Performance Logs User Group can log counter data.</span></span> <span data-ttu-id="73394-105">Пользователи в группе администраторов могут записывать данные счетчика только в том случае, если средство, используемое для записи данных счетчика в журнал, запускается из окна командной строки, открытого с помощью команды **Запуск от имени администратора.**... Все пользователи в интерактивных сеансах входа могут просматривать данные счетчика.</span><span class="sxs-lookup"><span data-stu-id="73394-105">Users in the Administrator group can log counter data only if the tool they use to log counter data is started from a Command Prompt window that is opened with **Run as administrator...**. Any users in interactive logon sessions can view counter data.</span></span> <span data-ttu-id="73394-106">Однако для просмотра данных счетчиков пользователи в неинтерактивных сеансах входа должны входить в группу "пользователи мониторинга производительности".</span><span class="sxs-lookup"><span data-stu-id="73394-106">However, users in non-interactive logon sessions must be in the Performance Monitoring Users group to view counter data.</span></span>

<span data-ttu-id="73394-107">**Windows XP:** Администратор или пользователи в группе администраторов могут записывать и просматривать данные счетчиков без ограничений.</span><span class="sxs-lookup"><span data-stu-id="73394-107">**Windows XP:** The Administrator or users in the Administrator group can log and view counter data without restriction.</span></span>

 

 



