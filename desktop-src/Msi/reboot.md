---
description: Свойство REBOOT подавляет некоторые запросы на перезагрузку системы.
ms.assetid: d88752cd-f59d-4214-b5b5-ce126500aa4e
title: Перезагрузка свойства
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4d94b08a04f3e95d873f6fc233185ce623cafc25
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105652005"
---
# <a name="reboot-property"></a><span data-ttu-id="cd402-103">Перезагрузка свойства</span><span class="sxs-lookup"><span data-stu-id="cd402-103">REBOOT property</span></span>

<span data-ttu-id="cd402-104">Свойство **reboot** подавляет некоторые запросы на перезагрузку системы.</span><span class="sxs-lookup"><span data-stu-id="cd402-104">The **REBOOT** property suppresses certain prompts for a restart of the system.</span></span> <span data-ttu-id="cd402-105">Администратор обычно использует это свойство с серией установок для установки нескольких продуктов одновременно с одной перезагрузкой в конце.</span><span class="sxs-lookup"><span data-stu-id="cd402-105">An administrator typically uses this property with a series of installations to install several products at the same time with only one restart at the end.</span></span> <span data-ttu-id="cd402-106">Дополнительные сведения см. в разделе [перезагрузки системы](system-reboots.md).</span><span class="sxs-lookup"><span data-stu-id="cd402-106">For more information, see [System Reboots](system-reboots.md).</span></span>

<span data-ttu-id="cd402-107">Действия [форцеребут](forcereboot-action.md) и [счедулеребут](schedulereboot-action.md) сообщают установщику о необходимости перезапуска системы.</span><span class="sxs-lookup"><span data-stu-id="cd402-107">The [ForceReboot](forcereboot-action.md) and [ScheduleReboot](schedulereboot-action.md) actions inform the installer to prompt the user to restart the system.</span></span> <span data-ttu-id="cd402-108">Установщик также может определить необходимость перезагрузки независимо от того, есть ли в последовательности какие-либо действия Форцеребут или Счедулеребут.</span><span class="sxs-lookup"><span data-stu-id="cd402-108">The installer can also determine that a restart is necessary whether there are any ForceReboot or ScheduleReboot actions in the sequence.</span></span> <span data-ttu-id="cd402-109">Например, установщик автоматически запрашивает перезагрузку, если требуется заменить все файлы, используемые во время установки.</span><span class="sxs-lookup"><span data-stu-id="cd402-109">For example, the installer automatically prompts for a restart if it needs to replace any files in use during the installation.</span></span>

<span data-ttu-id="cd402-110">Вы можете отключить определенные запросы на перезагрузку, задав свойство **reboot** следующим образом.</span><span class="sxs-lookup"><span data-stu-id="cd402-110">You can suppress certain prompts for restarts by setting the **REBOOT** property as follows.</span></span>



| <span data-ttu-id="cd402-111">Значение перезагрузки</span><span class="sxs-lookup"><span data-stu-id="cd402-111">REBOOT value</span></span>   | <span data-ttu-id="cd402-112">Описание</span><span class="sxs-lookup"><span data-stu-id="cd402-112">Description</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                                                                  |
|----------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="cd402-113">Force</span><span class="sxs-lookup"><span data-stu-id="cd402-113">Force</span></span>          | <span data-ttu-id="cd402-114">Всегда запрашивать перезагрузку в конце установки.</span><span class="sxs-lookup"><span data-stu-id="cd402-114">Always prompt for a restart at the end of the installation.</span></span> <span data-ttu-id="cd402-115">Пользовательский интерфейс всегда предлагает пользователю выбрать параметр для перезапуска в конце.</span><span class="sxs-lookup"><span data-stu-id="cd402-115">The UI always prompts the user with an option to restart at the end.</span></span> <span data-ttu-id="cd402-116">Если пользовательский интерфейс отсутствует и это не [многопакетная установка](multiple-package-installations.md), система автоматически перезагружается после завершения установки.</span><span class="sxs-lookup"><span data-stu-id="cd402-116">If there is no user interface, and this is not a [multiple-package installation](multiple-package-installations.md), the system automatically restarts at the end of the installation.</span></span> <span data-ttu-id="cd402-117">Если эта установка выполняется из нескольких пакетов, автоматический перезапуск системы не выполняется, и установщик возвращает сообщение об ошибке " \_ \_ требуется перезагрузка" \_ .</span><span class="sxs-lookup"><span data-stu-id="cd402-117">If this is a multiple-package installation, there is no automatic restart of the system and the installer returns ERROR\_SUCCESS\_REBOOT\_REQUIRED.</span></span> |
| <span data-ttu-id="cd402-118">Подавление</span><span class="sxs-lookup"><span data-stu-id="cd402-118">Suppress</span></span>       | <span data-ttu-id="cd402-119">Подавлять запросы на перезагрузку в конце установки.</span><span class="sxs-lookup"><span data-stu-id="cd402-119">Suppress prompts for a restart at the end of the installation.</span></span> <span data-ttu-id="cd402-120">Установщик по-прежнему запрашивает у пользователя возможность перезапуска во время установки при возникновении [действия форцеребут](forcereboot-action.md).</span><span class="sxs-lookup"><span data-stu-id="cd402-120">The installer still prompts the user with an option to restart during the installation whenever it encounters the [ForceReboot action](forcereboot-action.md).</span></span> <span data-ttu-id="cd402-121">Если пользовательский интерфейс отсутствует, система автоматически перезапускается при каждом Форцеребут.</span><span class="sxs-lookup"><span data-stu-id="cd402-121">If there is no user interface, the system automatically restarts at each ForceReboot.</span></span> <span data-ttu-id="cd402-122">Перезапускается в конце установки (например, из-за попытки установить используемый файл) подавляется.</span><span class="sxs-lookup"><span data-stu-id="cd402-122">Restarts at the end of the installation (for example, caused by an attempt to install a file in use) are suppressed.</span></span>                                    |
| <span data-ttu-id="cd402-123">реаллисуппресс</span><span class="sxs-lookup"><span data-stu-id="cd402-123">ReallySuppress</span></span> | <span data-ttu-id="cd402-124">Отключение всех перезапусков и запросов на перезапуск, инициированных Форцеребут во время установки.</span><span class="sxs-lookup"><span data-stu-id="cd402-124">Suppress all restarts and restart prompts initiated by ForceReboot during the installation.</span></span> <span data-ttu-id="cd402-125">Подавлять все перезапуски и запросы на перезагрузку в конце установки.</span><span class="sxs-lookup"><span data-stu-id="cd402-125">Suppress all restarts and restart prompts at the end of the installation.</span></span> <span data-ttu-id="cd402-126">Как запрос перезапуска, так и сам перезапуск подавляются.</span><span class="sxs-lookup"><span data-stu-id="cd402-126">Both the restart prompt and the restart itself are suppressed.</span></span> <span data-ttu-id="cd402-127">Например, перезагрузка в конце установки, вызванная попыткой установить файл, будет подавлена.</span><span class="sxs-lookup"><span data-stu-id="cd402-127">For example, restarts at the end of the installation, caused by an attempt to install a file in use, are suppressed.</span></span>                                                                                                                    |



 

## <a name="remarks"></a><span data-ttu-id="cd402-128">Комментарии</span><span class="sxs-lookup"><span data-stu-id="cd402-128">Remarks</span></span>

<span data-ttu-id="cd402-129">Установщик вычисляет только первый символ свойства **reboot** .</span><span class="sxs-lookup"><span data-stu-id="cd402-129">The installer only evaluates the first character of the **REBOOT** property.</span></span>

## <a name="requirements"></a><span data-ttu-id="cd402-130">Требования</span><span class="sxs-lookup"><span data-stu-id="cd402-130">Requirements</span></span>



| <span data-ttu-id="cd402-131">Требование</span><span class="sxs-lookup"><span data-stu-id="cd402-131">Requirement</span></span> | <span data-ttu-id="cd402-132">Значение</span><span class="sxs-lookup"><span data-stu-id="cd402-132">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="cd402-133">Версия</span><span class="sxs-lookup"><span data-stu-id="cd402-133">Version</span></span><br/> | <span data-ttu-id="cd402-134">Установщик Windows 5,0 в Windows Server 2012, Windows 8, Windows Server 2008 R2 или Windows 7.</span><span class="sxs-lookup"><span data-stu-id="cd402-134">Windows Installer 5.0 on Windows Server 2012, Windows 8, Windows Server 2008 R2 or Windows 7.</span></span> <span data-ttu-id="cd402-135">Установщик Windows 4,0 или установщик Windows 4,5 на Windows Server 2008 или Windows Vista.</span><span class="sxs-lookup"><span data-stu-id="cd402-135">Windows Installer 4.0 or Windows Installer 4.5 on Windows Server 2008 or Windows Vista.</span></span> <span data-ttu-id="cd402-136">Установщик Windows в Windows Server 2003 или Windows XP.</span><span class="sxs-lookup"><span data-stu-id="cd402-136">Windows Installer on Windows Server 2003 or Windows XP.</span></span> <span data-ttu-id="cd402-137">Сведения о минимальном пакете обновления Windows, который требуется для установщик Windows версии, см. в [установщик Windows Run-Time требования](windows-installer-portal.md) .</span><span class="sxs-lookup"><span data-stu-id="cd402-137">See the [Windows Installer Run-Time Requirements](windows-installer-portal.md) for information about the minimum Windows service pack that is required by a Windows Installer version.</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="cd402-138">См. также</span><span class="sxs-lookup"><span data-stu-id="cd402-138">See also</span></span>

<dl> <dt>

[<span data-ttu-id="cd402-139">Свойства</span><span class="sxs-lookup"><span data-stu-id="cd402-139">Properties</span></span>](properties.md)
</dt> <dt>

[<span data-ttu-id="cd402-140">**РЕБУТПРОМПТ, свойство**</span><span class="sxs-lookup"><span data-stu-id="cd402-140">**REBOOTPROMPT Property**</span></span>](rebootprompt.md)
</dt> <dt>

[<span data-ttu-id="cd402-141">Перезагрузка системы</span><span class="sxs-lookup"><span data-stu-id="cd402-141">System Reboots</span></span>](system-reboots.md)
</dt> </dl>

 

 




