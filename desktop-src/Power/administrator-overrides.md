---
description: Переопределения администратора
ms.assetid: 25b6ce86-52c8-4f7f-97af-86b2eaf3e9af
title: Переопределения администратора
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4c43e16c9aa3eb3ab9fd5ee7c8d17b9bb4536315
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "105663140"
---
# <a name="administrator-overrides"></a><span data-ttu-id="93181-103">Переопределения администратора</span><span class="sxs-lookup"><span data-stu-id="93181-103">Administrator Overrides</span></span>

<span data-ttu-id="93181-104">В Windows имеется один список управления доступом (ACL) по умолчанию для всех объектов политики управления питанием.</span><span class="sxs-lookup"><span data-stu-id="93181-104">Windows has a single default access control list (ACL) on all power policy objects.</span></span> <span data-ttu-id="93181-105">Список ACL предоставляет членам группы «Прошедшие проверку» разрешения на чтение, запись и изменение.</span><span class="sxs-lookup"><span data-stu-id="93181-105">The ACL grants read, write, and change permissions to members of the Authenticated Users group.</span></span> <span data-ttu-id="93181-106">Всем остальным пользователям предоставляется разрешение только на чтение.</span><span class="sxs-lookup"><span data-stu-id="93181-106">All other users are granted read-only permission.</span></span> <span data-ttu-id="93181-107">Приложения, которые вызывают функции политики управления питанием, могут определить, имеет ли пользователь разрешения на указанный параметр питания с помощью функции [**поверсеттингакцессчекк**](/windows/desktop/api/PowrProf/nf-powrprof-powersettingaccesscheck) .</span><span class="sxs-lookup"><span data-stu-id="93181-107">Applications that call power policy functions can determine whether a user has permissions for a specified power setting by using the [**PowerSettingAccessCheck**](/windows/desktop/api/PowrProf/nf-powrprof-powersettingaccesscheck) function.</span></span>

<span data-ttu-id="93181-108">Параметры питания могут быть переопределены с помощью групповая политика.</span><span class="sxs-lookup"><span data-stu-id="93181-108">Power settings may be overridden via Group Policy.</span></span> <span data-ttu-id="93181-109">Переопределения можно задать с помощью групповой политики домена или локальной групповой политики.</span><span class="sxs-lookup"><span data-stu-id="93181-109">Overrides can be set through domain group policy or local group policy.</span></span> <span data-ttu-id="93181-110">[**Поверсеттингакцессчекк**](/windows/desktop/api/PowrProf/nf-powrprof-powersettingaccesscheck) выдает сообщение, если указанный параметр питания имеет Переопределение групповой политики.</span><span class="sxs-lookup"><span data-stu-id="93181-110">[**PowerSettingAccessCheck**](/windows/desktop/api/PowrProf/nf-powrprof-powersettingaccesscheck) will report if a specified power setting has a group policy override.</span></span>

<span data-ttu-id="93181-111">Программа командной строки **PowerCfg.exe** отображает сообщение об ошибке, если команду не удается выполнить либо из-за отсутствия у пользователя разрешений на изменение параметра управления питанием, либо из-за того, что параметр питания имеет Переопределение групповой политики.</span><span class="sxs-lookup"><span data-stu-id="93181-111">The command line tool **PowerCfg.exe** displays an error message when a command cannot be completed either because the user did not have permissions to change the power setting or because the power setting has a group policy override.</span></span>

<span data-ttu-id="93181-112">В приложении "Параметры электропитания" на панели управления не предусмотрена поддержка настройки разрешений на доступ политики управления питанием.</span><span class="sxs-lookup"><span data-stu-id="93181-112">The Power Options application in Control Panel does not provide support for configuring power policy access permissions.</span></span> <span data-ttu-id="93181-113">Изменение разрешений должно выполняться с помощью **PowerCfg.exe**.</span><span class="sxs-lookup"><span data-stu-id="93181-113">Changing permissions must be done via **PowerCfg.exe**.</span></span>

 

 



