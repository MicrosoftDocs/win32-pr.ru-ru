---
description: Восстановление системы автоматически отслеживает и регистрирует ключевые изменения системы на компьютере пользователя. Дополнительные сведения см. в разделе Восстановление системы.
ms.assetid: 5fc345ff-8a47-4372-806f-64b8c271fd2d
title: Точки восстановления системы и установщик Windows
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d7fe9bd4b8e22f5aee7e49d3e4c452378f402e7b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "105673432"
---
# <a name="system-restore-points-and-the-windows-installer"></a><span data-ttu-id="f5fb4-104">Точки восстановления системы и установщик Windows</span><span class="sxs-lookup"><span data-stu-id="f5fb4-104">System Restore Points and the Windows Installer</span></span>

<span data-ttu-id="f5fb4-105">Восстановление системы автоматически отслеживает и регистрирует ключевые изменения системы на компьютере пользователя.</span><span class="sxs-lookup"><span data-stu-id="f5fb4-105">System Restore automatically monitors and records key system changes on a user's computer.</span></span> <span data-ttu-id="f5fb4-106">Дополнительные сведения см. в разделе [Восстановление системы](../sr/system-restore-portal.md).</span><span class="sxs-lookup"><span data-stu-id="f5fb4-106">For more information, see [System Restore](../sr/system-restore-portal.md).</span></span>

<span data-ttu-id="f5fb4-107">Точки восстановления системы создаются системой и также создаются с помощью установщик Windows при установке или удалении программного обеспечения.</span><span class="sxs-lookup"><span data-stu-id="f5fb4-107">System restore points are created by the system and are also created by Windows Installer when software is installed or removed.</span></span>

<span data-ttu-id="f5fb4-108">В Windows XP установщик может создавать контрольные точки во время первой установки приложения и во время его удаления.</span><span class="sxs-lookup"><span data-stu-id="f5fb4-108">On Windows XP, the installer may create checkpoints during the first installation of an application, and during its removal.</span></span> <span data-ttu-id="f5fb4-109">В таких случаях установщик создает контрольные точки только в том случае, если изменение выполняется по крайней мере с [*базовым пользовательским интерфейсом*](b-gly.md).</span><span class="sxs-lookup"><span data-stu-id="f5fb4-109">The installer only creates checkpoints in these cases when the change is run with at least a [*basic UI*](b-gly.md).</span></span> <span data-ttu-id="f5fb4-110">Установки, для которых установлен [уровень пользовательского интерфейса](user-interface-levels.md) "нет", обычно инициируются системой или приложением, которое должно выполнять создание контрольной точки.</span><span class="sxs-lookup"><span data-stu-id="f5fb4-110">Installations having the [user interface level](user-interface-levels.md) set to None are usually initiated by the system or an application that should handle creating a checkpoint.</span></span> <span data-ttu-id="f5fb4-111">Дополнительные сведения см. в разделе [Восстановление системы](../sr/system-restore-portal.md).</span><span class="sxs-lookup"><span data-stu-id="f5fb4-111">For more information, see [System Restore](../sr/system-restore-portal.md).</span></span>

<span data-ttu-id="f5fb4-112">В организациях с большим количеством небольших приложений администраторы могут отключить контрольные точки в установщике, чтобы повысить производительность.</span><span class="sxs-lookup"><span data-stu-id="f5fb4-112">In corporations with many small applications, administrators may decide to disable checkpointing from within the installer to improve performance.</span></span> <span data-ttu-id="f5fb4-113">Дополнительные сведения см. в разделе [лимитсистемресторечеккпоинтинг](limitsystemrestorecheckpointing.md) или [Установка точки восстановления из настраиваемого действия](setting-a-restore-point-from-a-custom-action.md).</span><span class="sxs-lookup"><span data-stu-id="f5fb4-113">For more information, see [LimitSystemRestoreCheckpointing](limitsystemrestorecheckpointing.md) or [Setting a Restore Point from a Custom Action](setting-a-restore-point-from-a-custom-action.md).</span></span>

<span data-ttu-id="f5fb4-114">Начиная с установщик Windows 5,0, свойство [**мсифастинсталл**](msifastinstall.md) может быть установлено, чтобы предотвратить создание точки восстановления системы в процессе установки.</span><span class="sxs-lookup"><span data-stu-id="f5fb4-114">Beginning with Windows Installer 5.0, the [**MSIFASTINSTALL**](msifastinstall.md) property can be set to prevent an installation from generating a system restore point.</span></span>

 

 
