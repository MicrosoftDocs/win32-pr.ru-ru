---
description: Вставьте действие Счедулеребут в последовательность действий, чтобы запросить у пользователя перезагрузку системы в конце установки. Используйте действие Форцеребут, чтобы запросить перезагрузку во время установки.
ms.assetid: 36f24f57-f1f0-4eca-9b6d-1b25fb73fa96
title: Действие Счедулеребут
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 460e3f25283c233fac80b25edd91d4bd102de435
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "103909815"
---
# <a name="schedulereboot-action"></a><span data-ttu-id="d7756-104">Действие Счедулеребут</span><span class="sxs-lookup"><span data-stu-id="d7756-104">ScheduleReboot Action</span></span>

<span data-ttu-id="d7756-105">Вставьте действие Счедулеребут в последовательность действий, чтобы запросить у пользователя перезагрузку системы в конце установки.</span><span class="sxs-lookup"><span data-stu-id="d7756-105">Insert the ScheduleReboot action into the action sequence to prompt the user for a restart of the system at the end of the installation.</span></span> <span data-ttu-id="d7756-106">Используйте [действие форцеребут](forcereboot-action.md) , чтобы запросить перезагрузку во время установки.</span><span class="sxs-lookup"><span data-stu-id="d7756-106">Use the [ForceReboot action](forcereboot-action.md) to prompt for a restart during installation.</span></span>

<span data-ttu-id="d7756-107">Если установка имеет пользовательский интерфейс, установщик отображает окно сообщения и кнопку в конце установки с вопросом, требуется ли перезагрузка системы.</span><span class="sxs-lookup"><span data-stu-id="d7756-107">If the installation has a user interface, the installer displays a message box and button at the end of installation asking whether the user wants to restart the system.</span></span> <span data-ttu-id="d7756-108">Пользователь должен ответить на этот запрос перед завершением установки.</span><span class="sxs-lookup"><span data-stu-id="d7756-108">The user must respond to this prompt before completing installation.</span></span> <span data-ttu-id="d7756-109">Если у установки нет пользовательского интерфейса, система автоматически перезапускается в конце.</span><span class="sxs-lookup"><span data-stu-id="d7756-109">If the installation has no user interface, the system automatically restarts at the end.</span></span>

<span data-ttu-id="d7756-110">Если установщик определит, что требуется перезагрузка, он автоматически запрашивает у пользователя перезапуск в конце установки, независимо от того, есть ли в последовательности какие-либо действия Форцеребут или Счедулеребут.</span><span class="sxs-lookup"><span data-stu-id="d7756-110">If the installer determines that a restart is necessary it automatically prompts the user to restart at the end of the installation, whether or not there are any ForceReboot or ScheduleReboot actions in the sequence.</span></span> <span data-ttu-id="d7756-111">Например, установщик автоматически запрашивает перезагрузку, если требуется заменить все файлы, используемые во время установки.</span><span class="sxs-lookup"><span data-stu-id="d7756-111">For example, the installer automatically prompts for a restart if it needs to replace any files that are in use during installation.</span></span>

<span data-ttu-id="d7756-112">Вы можете отключить определенные запросы на перезагрузку, задав свойство [**reboot**](reboot.md) .</span><span class="sxs-lookup"><span data-stu-id="d7756-112">You can suppress certain prompts for restarts by setting the [**REBOOT**](reboot.md) property.</span></span>

<span data-ttu-id="d7756-113">Если установщик Windows обнаруживает действие [форцеребут](forcereboot-action.md) или счедулеребут во время [установки нескольких пакетов](multiple-package-installations.md), установщик останавливается и выполняет откат установки.</span><span class="sxs-lookup"><span data-stu-id="d7756-113">If the Windows Installer encounters the [ForceReboot](forcereboot-action.md) or ScheduleReboot action during a [multiple-package installation](multiple-package-installations.md), the installer will stop and roll back the installation.</span></span> <span data-ttu-id="d7756-114">Можно установить другие пакеты, принадлежащие многопакетной установке, которые не содержат действие Форцеребут или Счедулеребут.</span><span class="sxs-lookup"><span data-stu-id="d7756-114">Other packages belonging to the multiple-package installation, that do not contain a ForceReboot or ScheduleReboot action, can be installed.</span></span>

## <a name="sequence-restrictions"></a><span data-ttu-id="d7756-115">Ограничения последовательности</span><span class="sxs-lookup"><span data-stu-id="d7756-115">Sequence Restrictions</span></span>

<span data-ttu-id="d7756-116">Ограничения последовательности отсутствуют.</span><span class="sxs-lookup"><span data-stu-id="d7756-116">There are no sequence restrictions.</span></span>

## <a name="actiondata-messages"></a><span data-ttu-id="d7756-117">Сообщения Актиондата</span><span class="sxs-lookup"><span data-stu-id="d7756-117">ActionData Messages</span></span>

<span data-ttu-id="d7756-118">Нет сообщений Актиондата.</span><span class="sxs-lookup"><span data-stu-id="d7756-118">There are no ActionData messages.</span></span>

## <a name="remarks"></a><span data-ttu-id="d7756-119">Комментарии</span><span class="sxs-lookup"><span data-stu-id="d7756-119">Remarks</span></span>

<span data-ttu-id="d7756-120">Например, это действие можно использовать, чтобы заставить установщик запрашивать перезагрузку после установки драйверов, требующих перезагрузки.</span><span class="sxs-lookup"><span data-stu-id="d7756-120">For example, this action can be used to force the installer to prompt for a restart after installing drivers that require a restart.</span></span> <span data-ttu-id="d7756-121">Если установщик пытается заменить используемые файлы, автоматически запрашивает у пользователя перезагрузку, даже если Счедулеребут не используется.</span><span class="sxs-lookup"><span data-stu-id="d7756-121">If the installer attempts to replace files that are in use, it automatically prompts the user to restart even if ScheduleReboot has not been used.</span></span>

<span data-ttu-id="d7756-122">Действие Счедулеребут обычно размещается в конце последовательности, но его можно вставить в любой точке последовательности.</span><span class="sxs-lookup"><span data-stu-id="d7756-122">The ScheduleReboot action is typically placed at the end of the sequence, but it can be inserted at any point in the sequence.</span></span>

## <a name="related-topics"></a><span data-ttu-id="d7756-123">См. также</span><span class="sxs-lookup"><span data-stu-id="d7756-123">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="d7756-124">Перезагрузка системы</span><span class="sxs-lookup"><span data-stu-id="d7756-124">System Reboots</span></span>](system-reboots.md)
</dt> </dl>

 

 



