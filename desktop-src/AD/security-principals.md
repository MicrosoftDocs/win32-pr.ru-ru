---
title: Субъекты безопасности
description: В Windows 2000 субъект безопасности — это пользователь, группа или компьютер \ 8212; сущность, которую распознает система безопасности.
ms.assetid: 213ee563-35cd-43d2-abb2-f66652df5be1
ms.tgt_platform: multiple
keywords:
- субъекты безопасности Active Directory
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4877ed77b365fa4a61444e4936dbe859379ee397
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/16/2019
ms.locfileid: "105654169"
---
# <a name="security-principals"></a><span data-ttu-id="dbbbc-104">Субъекты безопасности</span><span class="sxs-lookup"><span data-stu-id="dbbbc-104">Security Principals</span></span>

<span data-ttu-id="dbbbc-105">В Windows 2000 участник безопасности — это пользователь, группа или компьютер — сущность, которую распознает система безопасности.</span><span class="sxs-lookup"><span data-stu-id="dbbbc-105">In Windows 2000, a security principal is a user, group, or computer — an entity that the security system recognizes.</span></span> <span data-ttu-id="dbbbc-106">Сюда входят пользователи и автономные процессы.</span><span class="sxs-lookup"><span data-stu-id="dbbbc-106">This includes human users as well as autonomous processes.</span></span> <span data-ttu-id="dbbbc-107">Строго говоря, система безопасности не может сообщать о различиях между пользователями, вошедшими в систему, и процессами, выполняющимися на компьютере.</span><span class="sxs-lookup"><span data-stu-id="dbbbc-107">Strictly speaking, the security system cannot tell the difference between users who are logged in and processes running on the computer.</span></span> <span data-ttu-id="dbbbc-108">Он видит как субъекты безопасности с именами участников безопасности.</span><span class="sxs-lookup"><span data-stu-id="dbbbc-108">It sees both as security principals with security principal names.</span></span>

<span data-ttu-id="dbbbc-109">Пользователи, группы и компьютеры создаются и сохраняются как объекты в домен Active Directory Services.</span><span class="sxs-lookup"><span data-stu-id="dbbbc-109">Users, groups, and computers are created and stored as objects in Active Directory Domain Services.</span></span> <span data-ttu-id="dbbbc-110">Существуют также хорошо известные субъекты безопасности, которые представляют собой специальные удостоверения, определенные системой безопасности Windows 2000, такие как "все", "Локальная система", "участник Self", "прошедший проверку пользователь", "Создатель-владелец" и т. д.</span><span class="sxs-lookup"><span data-stu-id="dbbbc-110">There are also well-known security principals that represent special identities defined by the Windows 2000 security system, such as Everyone, Local System, Principal Self, Authenticated User, Creator Owner, and so on.</span></span> <span data-ttu-id="dbbbc-111">Объекты, представляющие хорошо известные субъекты безопасности, такие как анонимный вход в систему, хранятся в контейнере субъектов безопасности WellKnown под контейнером конфигурации.</span><span class="sxs-lookup"><span data-stu-id="dbbbc-111">Objects representing the well-known security principals, such as Anonymous Logon, are stored in the WellKnown Security Principals container beneath the Configuration container.</span></span>

 

 




