---
description: Можно назначить привилегии учетным записям с помощью оснастки локальной политики безопасности (MMC) (secpol. msc) или путем вызова функции Лсааддаккаунтригхтс.
ms.assetid: F2DAB2E3-8B24-49A3-A2DD-E83B5181E9A2
title: Назначение привилегий учетной записи
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0865a59b8bad75e687fd12f6bfc42c2cd39f664d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "105663952"
---
# <a name="assigning-privileges-to-an-account"></a><span data-ttu-id="6bb9e-103">Назначение привилегий учетной записи</span><span class="sxs-lookup"><span data-stu-id="6bb9e-103">Assigning Privileges to an Account</span></span>

<span data-ttu-id="6bb9e-104">Можно назначить привилегии учетным записям с помощью оснастки локальной политики безопасности (MMC) (secpol. msc) или путем вызова функции [**лсааддаккаунтригхтс**](/windows/desktop/api/ntsecapi/nf-ntsecapi-lsaaddaccountrights) .</span><span class="sxs-lookup"><span data-stu-id="6bb9e-104">You can assign privileges to accounts either by using the Local Security Policy Microsoft Management Console (MMC) snap-in (Secpol.msc) or by calling the [**LsaAddAccountRights**](/windows/desktop/api/ntsecapi/nf-ntsecapi-lsaaddaccountrights) function.</span></span>

<span data-ttu-id="6bb9e-105">Назначение привилегии учетной записи не влияет на существующие токены пользователя.</span><span class="sxs-lookup"><span data-stu-id="6bb9e-105">Assigning a privilege to an account does not affect existing user tokens.</span></span> <span data-ttu-id="6bb9e-106">Пользователь должен выйти из системы и снова войти, чтобы получить маркер доступа с вновь назначенными привилегиями.</span><span class="sxs-lookup"><span data-stu-id="6bb9e-106">A user must log off and then log back on to get an access token with the newly assigned privilege.</span></span>

<span data-ttu-id="6bb9e-107">Чтобы назначить привилегии с помощью оснастки MMC "Локальная политика безопасности", измените список пользователей для каждого из привилегий в разделе **Параметры безопасности/Локальные политики/Назначение прав пользователя**.</span><span class="sxs-lookup"><span data-stu-id="6bb9e-107">To assign privileges by using the Local Security Policy MMC snap-in, edit the list of users for each privilege listed under **Security Settings/Local Policies/User Rights Assignment**.</span></span>

 

 
