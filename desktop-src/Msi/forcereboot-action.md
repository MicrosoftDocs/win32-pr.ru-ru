---
description: Действие Форцеребут запрашивает у пользователя перезагрузку системы во время установки.
ms.assetid: e1bcdd59-8cbc-46f7-b908-c8cbc2ea0539
title: Действие Форцеребут
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 807bab474f1faacfbc7684797b7a0b7b74f354d9
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "105663698"
---
# <a name="forcereboot-action"></a><span data-ttu-id="e3f3c-103">Действие Форцеребут</span><span class="sxs-lookup"><span data-stu-id="e3f3c-103">ForceReboot Action</span></span>

<span data-ttu-id="e3f3c-104">Действие Форцеребут запрашивает у пользователя перезагрузку системы во время установки.</span><span class="sxs-lookup"><span data-stu-id="e3f3c-104">The ForceReboot action prompts the user for a restart of the system during the installation.</span></span> <span data-ttu-id="e3f3c-105">Действие Форцеребут отличается от [действия счедулеребут](schedulereboot-action.md) в том, что действие счедулеребут используется для планирования запроса на перезагрузку в конце установки.</span><span class="sxs-lookup"><span data-stu-id="e3f3c-105">The ForceReboot action is different from the [ScheduleReboot action](schedulereboot-action.md) in that the ScheduleReboot action is used to schedule a prompt to restart at the end of the installation.</span></span>

<span data-ttu-id="e3f3c-106">Если установка имеет пользовательский интерфейс, установщик отображает диалоговое окно для каждого действия Форцеребут, которое предлагает пользователю перезагрузить систему.</span><span class="sxs-lookup"><span data-stu-id="e3f3c-106">If the installation has a user interface, the installer displays a dialog box at each ForceReboot action which prompts the user to restart the system.</span></span> <span data-ttu-id="e3f3c-107">Перед продолжением установки пользователь должен ответить на этот запрос.</span><span class="sxs-lookup"><span data-stu-id="e3f3c-107">The user must respond to this prompt before continuing with the installation.</span></span> <span data-ttu-id="e3f3c-108">Если у установки нет пользовательского интерфейса, система автоматически перезапускается в действии Форцеребут.</span><span class="sxs-lookup"><span data-stu-id="e3f3c-108">If the installation has no user interface, the system automatically restarts at the ForceReboot action.</span></span>

<span data-ttu-id="e3f3c-109">Если установщик определит, что требуется перезагрузка, он автоматически запрашивает у пользователя перезапуск в конце установки, независимо от того, есть ли в последовательности какие-либо действия Форцеребут или Счедулеребут.</span><span class="sxs-lookup"><span data-stu-id="e3f3c-109">If the installer determines that a restart is necessary, it automatically prompts the user to restart at the end of the installation, whether or not there are any ForceReboot or ScheduleReboot actions in the sequence.</span></span> <span data-ttu-id="e3f3c-110">Например, установщик автоматически запрашивает перезагрузку, если требуется заменить все файлы, используемые во время установки.</span><span class="sxs-lookup"><span data-stu-id="e3f3c-110">For example, the installer automatically prompts for a restart if it needs to replace any files used during the installation.</span></span>

<span data-ttu-id="e3f3c-111">Отключите определенные запросы на перезагрузку, задав свойство [**reboot**](reboot.md) .</span><span class="sxs-lookup"><span data-stu-id="e3f3c-111">Suppress certain restart prompts by setting the [**REBOOT**](reboot.md) property.</span></span>

<span data-ttu-id="e3f3c-112">Если установщик Windows обнаруживает действие Форцеребут или [счедулеребут](schedulereboot-action.md) во время [установки нескольких пакетов](multiple-package-installations.md), установщик останавливается и выполняет откат установки.</span><span class="sxs-lookup"><span data-stu-id="e3f3c-112">If the Windows Installer encounters the ForceReboot or [ScheduleReboot](schedulereboot-action.md) action during a [multiple-package installation](multiple-package-installations.md), the installer will stop and roll back the installation.</span></span> <span data-ttu-id="e3f3c-113">Можно установить другие пакеты, принадлежащие многопакетной установке, которые не содержат действие Форцеребут или Счедулеребут.</span><span class="sxs-lookup"><span data-stu-id="e3f3c-113">Other packages belonging to the multiple-package installation, that do not contain a ForceReboot or ScheduleReboot action, can be installed.</span></span>

## <a name="sequence-restrictions"></a><span data-ttu-id="e3f3c-114">Ограничения последовательности</span><span class="sxs-lookup"><span data-stu-id="e3f3c-114">Sequence Restrictions</span></span>

<span data-ttu-id="e3f3c-115">Следующие действия обычно выполняются вместе как группа в последовательности действий.</span><span class="sxs-lookup"><span data-stu-id="e3f3c-115">The following actions commonly occur together as a group in the action sequence.</span></span> <span data-ttu-id="e3f3c-116">Рекомендуется, чтобы действие Форцеребут было запланировано после этой группы.</span><span class="sxs-lookup"><span data-stu-id="e3f3c-116">It is recommended that the ForceReboot action be scheduled to come after this group.</span></span> <span data-ttu-id="e3f3c-117">Если действие Форцеребут запланировано перед [действием регистерпродукт](registerproduct-action.md), установщик снова запрашивает источник установочного пакета после перезагрузки.</span><span class="sxs-lookup"><span data-stu-id="e3f3c-117">If the ForceReboot action is scheduled before the [RegisterProduct action](registerproduct-action.md), the installer again requires the source of the installation package after the restart.</span></span> <span data-ttu-id="e3f3c-118">Таким образом, предпочтительная последовательность для Форцеребут сразу после этой последовательности действий.</span><span class="sxs-lookup"><span data-stu-id="e3f3c-118">Therefore, the preferred sequence for ForceReboot is immediately following this action sequence.</span></span>

-   [<span data-ttu-id="e3f3c-119">регистерпродукт</span><span class="sxs-lookup"><span data-stu-id="e3f3c-119">RegisterProduct</span></span>](registerproduct-action.md)
-   [<span data-ttu-id="e3f3c-120">RegisterUser</span><span class="sxs-lookup"><span data-stu-id="e3f3c-120">RegisterUser</span></span>](registeruser-action.md)
-   [<span data-ttu-id="e3f3c-121">публишпродукт</span><span class="sxs-lookup"><span data-stu-id="e3f3c-121">PublishProduct</span></span>](publishproduct-action.md)
-   [<span data-ttu-id="e3f3c-122">публишфеатурес</span><span class="sxs-lookup"><span data-stu-id="e3f3c-122">PublishFeatures</span></span>](publishfeatures-action.md)
-   [<span data-ttu-id="e3f3c-123">креатешорткутс</span><span class="sxs-lookup"><span data-stu-id="e3f3c-123">CreateShortcuts</span></span>](createshortcuts-action.md)
-   [<span data-ttu-id="e3f3c-124">регистермимеинфо</span><span class="sxs-lookup"><span data-stu-id="e3f3c-124">RegisterMIMEInfo</span></span>](registermimeinfo-action.md)
-   [<span data-ttu-id="e3f3c-125">регистерекстенсионинфо</span><span class="sxs-lookup"><span data-stu-id="e3f3c-125">RegisterExtensionInfo</span></span>](registerextensioninfo-action.md)
-   [<span data-ttu-id="e3f3c-126">регистерклассинфо</span><span class="sxs-lookup"><span data-stu-id="e3f3c-126">RegisterClassInfo</span></span>](registerclassinfo-action.md)
-   [<span data-ttu-id="e3f3c-127">регистерпрогидинфо</span><span class="sxs-lookup"><span data-stu-id="e3f3c-127">RegisterProgIdInfo</span></span>](registerprogidinfo-action.md)

<span data-ttu-id="e3f3c-128">Действие Форцеребут должно находиться между [инсталлинитиализе](installinitialize-action.md) и [функции InstallFinalize](installfinalize-action.md) в последовательности действий [таблицы инсталлексекутесекуенце](installexecutesequence-table.md).</span><span class="sxs-lookup"><span data-stu-id="e3f3c-128">The ForceReboot action must come between [InstallInitialize](installinitialize-action.md) and [InstallFinalize](installfinalize-action.md) in the action sequence of the [InstallExecuteSequence table](installexecutesequence-table.md).</span></span>

## <a name="actiondata-messages"></a><span data-ttu-id="e3f3c-129">Сообщения Актиондата</span><span class="sxs-lookup"><span data-stu-id="e3f3c-129">ActionData Messages</span></span>

<span data-ttu-id="e3f3c-130">Нет сообщений Актиондата.</span><span class="sxs-lookup"><span data-stu-id="e3f3c-130">There are no ActionData messages.</span></span>

## <a name="remarks"></a><span data-ttu-id="e3f3c-131">Комментарии</span><span class="sxs-lookup"><span data-stu-id="e3f3c-131">Remarks</span></span>

<span data-ttu-id="e3f3c-132">Действие Форцеребут всегда должно использоваться с условным оператором, так что установщик запускает перезапуск только при необходимости.</span><span class="sxs-lookup"><span data-stu-id="e3f3c-132">The ForceReboot action must always be used with a conditional statement such that the installer triggers a restart only when necessary.</span></span> <span data-ttu-id="e3f3c-133">Например, перезапуск может потребоваться только в том случае, если заменяется определенный файл или устанавливается определенный компонент.</span><span class="sxs-lookup"><span data-stu-id="e3f3c-133">For example, a restart may only be required if a particular file is replaced or a particular component is installed.</span></span> <span data-ttu-id="e3f3c-134">Каждая установка продукта является уникальной и может потребоваться дополнительное действие, чтобы определить, требуется ли перезагрузка.</span><span class="sxs-lookup"><span data-stu-id="e3f3c-134">Each product installation is unique and a custom action may be required to determine whether a restart is needed.</span></span> <span data-ttu-id="e3f3c-135">Условие в действии Форцеребут обычно использует свойство [**афтерребут**](afterreboot.md) .</span><span class="sxs-lookup"><span data-stu-id="e3f3c-135">The condition on the ForceReboot action commonly makes use of the [**AFTERREBOOT**](afterreboot.md) property.</span></span>

<span data-ttu-id="e3f3c-136">Форцеребут запускает системные операции, созданные предыдущими действиями перед запросом на перезагрузку или перезапуске.</span><span class="sxs-lookup"><span data-stu-id="e3f3c-136">ForceReboot runs system operations generated by any previous actions before prompting for a restart or restarting.</span></span> <span data-ttu-id="e3f3c-137">Например, системные операции, созданные [инсталлфилес](installfiles-action.md) и [вритерегистривалуес](writeregistryvalues-action.md) , выполняются перед перезагрузкой.</span><span class="sxs-lookup"><span data-stu-id="e3f3c-137">For example, the system operations generated by [InstallFiles](installfiles-action.md) and [WriteRegistryValues](writeregistryvalues-action.md) are run before a restart.</span></span>

<span data-ttu-id="e3f3c-138">Действие Форцеребут записывает раздел реестра, который вызывает запуск установщика после перезагрузки.</span><span class="sxs-lookup"><span data-stu-id="e3f3c-138">The ForceReboot action writes a registry key that causes the installer to start after restarting.</span></span> <span data-ttu-id="e3f3c-139">Расположение этого ключа — **hKey \_ Local \_ Machine \\ Software \\ Microsoft \\ Windows \\ CurrentVersion \\ RunOnce**.</span><span class="sxs-lookup"><span data-stu-id="e3f3c-139">The location of this key is **HKEY\_LOCAL\_MACHINE\\SOFTWARE\\Microsoft\\Windows\\CurrentVersion\\RunOnce**.</span></span>

## <a name="related-topics"></a><span data-ttu-id="e3f3c-140">См. также</span><span class="sxs-lookup"><span data-stu-id="e3f3c-140">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="e3f3c-141">Перезагрузка системы</span><span class="sxs-lookup"><span data-stu-id="e3f3c-141">System Reboots</span></span>](system-reboots.md)
</dt> </dl>

 

 



