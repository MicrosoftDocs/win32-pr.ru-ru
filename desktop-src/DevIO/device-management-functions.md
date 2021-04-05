---
description: В управлении устройствами используются следующие функции.
ms.assetid: 3918ba49-1549-4f0c-b9fd-303ef46b810e
title: Функции управления устройствами
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 587778b489b16355046b0b5af5cbba31c1a39639
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "103990521"
---
# <a name="device-management-functions"></a><span data-ttu-id="5bdf2-103">Функции управления устройствами</span><span class="sxs-lookup"><span data-stu-id="5bdf2-103">Device Management Functions</span></span>

<span data-ttu-id="5bdf2-104">В управлении устройствами используются следующие функции.</span><span class="sxs-lookup"><span data-stu-id="5bdf2-104">The following functions are used in device management.</span></span>



| <span data-ttu-id="5bdf2-105">Функция</span><span class="sxs-lookup"><span data-stu-id="5bdf2-105">Function</span></span>                                                             | <span data-ttu-id="5bdf2-106">Описание</span><span class="sxs-lookup"><span data-stu-id="5bdf2-106">Description</span></span>                                                                           |
|----------------------------------------------------------------------|---------------------------------------------------------------------------------------|
| [<span data-ttu-id="5bdf2-107">**DeviceIoControl**</span><span class="sxs-lookup"><span data-stu-id="5bdf2-107">**DeviceIoControl**</span></span>](/windows/win32/api/ioapiset/nf-ioapiset-deviceiocontrol)                           | <span data-ttu-id="5bdf2-108">Отправляет управляющий код непосредственно в указанный драйвер устройства.</span><span class="sxs-lookup"><span data-stu-id="5bdf2-108">Sends a control code directly to a specified device driver.</span></span>                           |
| [<span data-ttu-id="5bdf2-109">**инсталлневдевице**</span><span class="sxs-lookup"><span data-stu-id="5bdf2-109">**InstallNewDevice**</span></span>](installnewdevice.md)                         | <span data-ttu-id="5bdf2-110">Устанавливает новое устройство.</span><span class="sxs-lookup"><span data-stu-id="5bdf2-110">Installs a new device.</span></span> <span data-ttu-id="5bdf2-111">Пользователю предлагается выбрать устройство.</span><span class="sxs-lookup"><span data-stu-id="5bdf2-111">The user is prompted to select the device.</span></span>                     |
| [<span data-ttu-id="5bdf2-112">**регистердевиценотификатион**</span><span class="sxs-lookup"><span data-stu-id="5bdf2-112">**RegisterDeviceNotification**</span></span>](/windows/desktop/api/Winuser/nf-winuser-registerdevicenotificationa)     | <span data-ttu-id="5bdf2-113">Регистрация устройства или типа устройства, для которых окно будет получать уведомления.</span><span class="sxs-lookup"><span data-stu-id="5bdf2-113">Registers the device or type of device for which a window will receive notifications.</span></span> |
| [<span data-ttu-id="5bdf2-114">**унрегистердевиценотификатион**</span><span class="sxs-lookup"><span data-stu-id="5bdf2-114">**UnregisterDeviceNotification**</span></span>](/windows/desktop/api/Winuser/nf-winuser-unregisterdevicenotification) | <span data-ttu-id="5bdf2-115">Закрывает указанный маркер уведомления устройства.</span><span class="sxs-lookup"><span data-stu-id="5bdf2-115">Closes the specified device notification handle.</span></span>                                      |



 

<span data-ttu-id="5bdf2-116">Для дисководов CD-ROM и DVD используются следующие функции.</span><span class="sxs-lookup"><span data-stu-id="5bdf2-116">The following functions are used with CD-ROM and DVD drives.</span></span>



| <span data-ttu-id="5bdf2-117">Функция</span><span class="sxs-lookup"><span data-stu-id="5bdf2-117">Function</span></span>                                                               | <span data-ttu-id="5bdf2-118">Описание</span><span class="sxs-lookup"><span data-stu-id="5bdf2-118">Description</span></span>                                                                                         |
|------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="5bdf2-119">**кдромдисабледигиталплайбакк**</span><span class="sxs-lookup"><span data-stu-id="5bdf2-119">**CdromDisableDigitalPlayback**</span></span>](/windows/desktop/api/StorProp/nf-storprop-cdromdisabledigitalplayback)     | <span data-ttu-id="5bdf2-120">Отключает цифровое воспроизведение для указанного дисковода компакт-дисков или DVD-дисков.</span><span class="sxs-lookup"><span data-stu-id="5bdf2-120">Disables digital playback for the specified CD-ROM or DVD drive.</span></span>                                    |
| [<span data-ttu-id="5bdf2-121">**кдроменабледигиталплайбакк**</span><span class="sxs-lookup"><span data-stu-id="5bdf2-121">**CdromEnableDigitalPlayback**</span></span>](/windows/desktop/api/StorProp/nf-storprop-cdromenabledigitalplayback)       | <span data-ttu-id="5bdf2-122">Включает цифровое воспроизведение для указанного дисковода компакт-дисков или DVD-дисков.</span><span class="sxs-lookup"><span data-stu-id="5bdf2-122">Enables digital playback for the specified CD-ROM or DVD drive.</span></span>                                     |
| [<span data-ttu-id="5bdf2-123">**кдромисдигиталплайбаккенаблед**</span><span class="sxs-lookup"><span data-stu-id="5bdf2-123">**CdromIsDigitalPlaybackEnabled**</span></span>](/windows/desktop/api/StorProp/nf-storprop-cdromisdigitalplaybackenabled) | <span data-ttu-id="5bdf2-124">Определяет, включено ли цифровое воспроизведение для указанного дисковода компакт-дисков или DVD-дисков.</span><span class="sxs-lookup"><span data-stu-id="5bdf2-124">Determines whether digital playback is enabled for the specified CD-ROM or DVD drive.</span></span>               |
| [<span data-ttu-id="5bdf2-125">**кдромкновнгуддигиталплайбакк**</span><span class="sxs-lookup"><span data-stu-id="5bdf2-125">**CdromKnownGoodDigitalPlayback**</span></span>](/windows/desktop/api/Storprop/nf-storprop-cdromknowngooddigitalplayback) | <span data-ttu-id="5bdf2-126">Определяет, имеет ли указанный дисковод компакт-дисков или DVD-дисков цифровое воспроизведение, которое известно как хорошее.</span><span class="sxs-lookup"><span data-stu-id="5bdf2-126">Determines whether the specified CD-ROM or DVD drive has digital playback that is known to be good.</span></span> |
| [<span data-ttu-id="5bdf2-127">**двдлаунчер**</span><span class="sxs-lookup"><span data-stu-id="5bdf2-127">**DvdLauncher**</span></span>](dvdlauncher.md)                                     | <span data-ttu-id="5bdf2-128">Проверяет, соответствует ли регион носителя в DVD-дисководе региону DVD-дисковода.</span><span class="sxs-lookup"><span data-stu-id="5bdf2-128">Verifies that the media region in the DVD drive matches the DVD drive region.</span></span>                       |



 

 

 
