---
title: Использование IMAPI
description: В следующих разделах демонстрируется использование API-интерфейса основного образа.
ms.assetid: c42043db-612f-488f-a6ae-a8caea8ac42b
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ccd44d01e925d07d251e93a29c5268cc7e9c5076
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/16/2019
ms.locfileid: "103889184"
---
# <a name="using-imapi"></a><span data-ttu-id="b3921-103">Использование IMAPI</span><span class="sxs-lookup"><span data-stu-id="b3921-103">Using IMAPI</span></span>

<span data-ttu-id="b3921-104">В следующих разделах демонстрируется использование API-интерфейса основного образа.</span><span class="sxs-lookup"><span data-stu-id="b3921-104">The following topics demonstrate the use of the image mastering API.</span></span>

## <a name="usage-scenarios"></a><span data-ttu-id="b3921-105">Сценарии использования</span><span class="sxs-lookup"><span data-stu-id="b3921-105">Usage Scenarios</span></span>

<span data-ttu-id="b3921-106">В следующей документации приводятся подробные рекомендации по распространенным сценариям IMAPI.</span><span class="sxs-lookup"><span data-stu-id="b3921-106">The following documentation provides detailed guidance for common IMAPI scenarios.</span></span>



| <span data-ttu-id="b3921-107">Сценарий</span><span class="sxs-lookup"><span data-stu-id="b3921-107">Scenario</span></span>                                                                                                         | <span data-ttu-id="b3921-108">Описание</span><span class="sxs-lookup"><span data-stu-id="b3921-108">Description</span></span>                                                                                                                                                           |
|------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="b3921-109">Проверка поддержки диска</span><span class="sxs-lookup"><span data-stu-id="b3921-109">Checking Drive Support</span></span>](checking-drive-support.md)                                                             | <span data-ttu-id="b3921-110">Демонстрируется обнаружение поддержки для накопителя мультимедиа.</span><span class="sxs-lookup"><span data-stu-id="b3921-110">Demonstrates the detection of support for a media drive.</span></span><br/>                                                                                                   |
| [<span data-ttu-id="b3921-111">Проверка поддержки мультимедиа</span><span class="sxs-lookup"><span data-stu-id="b3921-111">Checking Media Support</span></span>](checking-media-support.md)                                                             | <span data-ttu-id="b3921-112">Демонстрируется обнаружение поддержки мультимедиа.</span><span class="sxs-lookup"><span data-stu-id="b3921-112">Demonstrates the detection of support for media.</span></span><br/>                                                                                                           |
| [<span data-ttu-id="b3921-113">Запись образа диска</span><span class="sxs-lookup"><span data-stu-id="b3921-113">Burning a Disc Image</span></span>](burning-a-disc.md)                                                                       | <span data-ttu-id="b3921-114">Демонстрируется основной способ (запись диска) с помощью IMAPI.</span><span class="sxs-lookup"><span data-stu-id="b3921-114">Demonstrates mastering (burning a disc) using IMAPI.</span></span><br/>                                                                                                       |
| [<span data-ttu-id="b3921-115">Добавление загрузочного образа</span><span class="sxs-lookup"><span data-stu-id="b3921-115">Adding a Boot Image</span></span>](adding-a-boot-image.md)                                                                   | <span data-ttu-id="b3921-116">На примере [записи образа диска](burning-a-disc.md) выполняется добавление кода для включения загрузочного образа в раздел загрузки диска.</span><span class="sxs-lookup"><span data-stu-id="b3921-116">Builds on the [Burning a Disc Image](burning-a-disc.md) example by adding code to include a bootable image in the boot section of the disc.</span></span><br/>               |
| [<span data-ttu-id="b3921-117">Создание многосеансового диска</span><span class="sxs-lookup"><span data-stu-id="b3921-117">Creating a Multisession Disc</span></span>](creating-a-multisession-disc.md)                                                 | <span data-ttu-id="b3921-118">Демонстрирует создание многосеансового диска с помощью IMAPI.</span><span class="sxs-lookup"><span data-stu-id="b3921-118">Demonstrates the creation of a multisession disc using IMAPI.</span></span><br/>                                                                                              |
| [<span data-ttu-id="b3921-119">Мониторинг хода выполнения с помощью событий</span><span class="sxs-lookup"><span data-stu-id="b3921-119">Monitoring Progress With Events</span></span>](monitoring-progress-with-events.md)                                           | <span data-ttu-id="b3921-120">Демонстрирует использование конкретных интерфейсов для реализации обработчика событий, чтобы можно было получить сведения о ходе выполнения.</span><span class="sxs-lookup"><span data-stu-id="b3921-120">Demonstrates the use of specific interfaces in order to allow the implementation of an event handler so that progress information may be received.</span></span> <br/>        |
| [<span data-ttu-id="b3921-121">Предотвращение выхода из системы или приостановки во время записи</span><span class="sxs-lookup"><span data-stu-id="b3921-121">Preventing Logoff or Suspend During a Burn</span></span>](preventing-logoff-or-suspend-during-a-burn.md)                     | <span data-ttu-id="b3921-122">Содержит сведения о вопросах разработки приложений, которые необходимо выполнить в отношении сценариев, включающих в себя пользователя "logoff" и "Suspend" в Windows.</span><span class="sxs-lookup"><span data-stu-id="b3921-122">Contains information detailing application development considerations to be made in regards to scenarios involving user 'Logoff' and 'Suspend' in Windows.</span></span><br/> |
| [<span data-ttu-id="b3921-123">Предоставление пользователям разрешений для устройств записи мультимедиа</span><span class="sxs-lookup"><span data-stu-id="b3921-123">Providing User Permissions for Media Burning Devices</span></span>](providing-user-permissions-for-media-burning-devices.md) | <span data-ttu-id="b3921-124">Подробно описывается процесс, необходимый для обеспечения наличия у пользователя достаточных разрешений на использование устройств записи мультимедиа в Windows XP и Windows Server 2003.</span><span class="sxs-lookup"><span data-stu-id="b3921-124">Details the process required to ensure a user has adequate permissions to utilize media burning devices on Windows XP and Windows Server 2003.</span></span><br/>             |



 

## <a name="application-compatibility"></a><span data-ttu-id="b3921-125">Совместимость приложений</span><span class="sxs-lookup"><span data-stu-id="b3921-125">Application Compatibility</span></span>

<span data-ttu-id="b3921-126">В следующей документации содержатся важные сведения, которые необходимо учитывать при разработке приложения, использующего IMAPI.</span><span class="sxs-lookup"><span data-stu-id="b3921-126">The following documentation contains important information to take consideration while developing an application that utilizes IMAPI.</span></span>



| <span data-ttu-id="b3921-127">Руководство</span><span class="sxs-lookup"><span data-stu-id="b3921-127">Guidance</span></span>                                                   | <span data-ttu-id="b3921-128">Описание</span><span class="sxs-lookup"><span data-stu-id="b3921-128">Description</span></span>                                                                                                                                                                                                                                                 |
|------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="b3921-129">Многосеансовый макет IMAPI</span><span class="sxs-lookup"><span data-stu-id="b3921-129">IMAPI Multisession Layout</span></span>](imapi-multisession-layout.md) | <span data-ttu-id="b3921-130">Сведения о структуре дисков, которую использует IMAPI для реализации многосеансовой связи.</span><span class="sxs-lookup"><span data-stu-id="b3921-130">Details the disc layout that IMAPI utilizes to implement multisession.</span></span> <span data-ttu-id="b3921-131">Эти сведения используются для обеспечения взаимодействия между IMAPI и другим программным обеспечением для записи, а также для создания образов многосеансовых дисков, совместимых с IMAPI.</span><span class="sxs-lookup"><span data-stu-id="b3921-131">This information is used to ensure interoperability between IMAPI and other burning software, as well as allow the creation of IMAPI-compatible multisession disc images.</span></span><br/> |



 

 

 





