---
description: Чтобы обеспечить безопасность установки программного обеспечения на заблокированных компьютерах, придерживайтесь этих рекомендаций при создании пакета установщик Windows.
ms.assetid: 46ee99a9-b77d-4138-98f0-04428e68cf30
title: Защита пакетов на заблокированных компьютерах
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bfe8380ad7e342d35bff80da4d4d86c37759a80a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "103910932"
---
# <a name="securing-packages-on-locked-down-computers"></a><span data-ttu-id="cde16-103">Защита пакетов на заблокированных компьютерах</span><span class="sxs-lookup"><span data-stu-id="cde16-103">Securing Packages on Locked-Down Computers</span></span>

<span data-ttu-id="cde16-104">Соблюдение следующих рекомендаций при создании установщик Windows пакета, который будет использоваться на заблокированных компьютерах, помогает поддерживать безопасную среду во время установки:</span><span class="sxs-lookup"><span data-stu-id="cde16-104">Adherence to the following guidelines when authoring a Windows Installer package that will be used on locked-down computers helps maintain a secure environment during installation:</span></span>

-   <span data-ttu-id="cde16-105">Проверьте пакет на совместимость с [политикой системы](system-policy.md)установщик Windows машины.</span><span class="sxs-lookup"><span data-stu-id="cde16-105">Test your package for compatibility with the Windows Installer machine [System Policy](system-policy.md).</span></span>
-   <span data-ttu-id="cde16-106">Убедитесь, что пакет выполняется на всех [уровнях пользовательского интерфейса](user-interface-levels.md): None, Basic, Limited и Full.</span><span class="sxs-lookup"><span data-stu-id="cde16-106">Make sure you package runs with all [user interface levels](user-interface-levels.md), none, basic, limited, and full.</span></span>
-   <span data-ttu-id="cde16-107">Протестируйте пакет в разделах NTFS с [*повышенными*](e-gly.md) правами и без повышенных привилегий.</span><span class="sxs-lookup"><span data-stu-id="cde16-107">Test your package on NTFS partitions, both with [*elevated*](e-gly.md) and non-elevated privileges.</span></span>
-   <span data-ttu-id="cde16-108">Начиная с установщик Windows 3,0, [исправление контроля учетных записей пользователей (UAC)](user-account-control--uac--patching.md) позволяет пользователям без прав администратора устанавливать исправления в приложениях, установленных в контексте на компьютере.</span><span class="sxs-lookup"><span data-stu-id="cde16-108">Starting with Windows Installer 3.0, [User Account Control (UAC) Patching](user-account-control--uac--patching.md) enables non-administrator users to patch applications installed in the per-machine context.</span></span> <span data-ttu-id="cde16-109">Протестируйте пакет исправлений в Windows Vista и Windows XP для установки пользователями с доступом администратора и пользователями, не являющимися администраторами.</span><span class="sxs-lookup"><span data-stu-id="cde16-109">Test your patch package on Windows Vista and Windows XP for both installation by users with administrator access and by non-administrator users.</span></span>

 

 



