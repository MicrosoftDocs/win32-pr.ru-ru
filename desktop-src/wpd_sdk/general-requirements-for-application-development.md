---
description: Общие требования для разработки приложений
ms.assetid: 8ac88d6f-fc4b-4253-932d-aaa3c801b18f
title: Общие требования для разработки приложений (API-интерфейс WPD)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d16be9656f72324b8f3687bca72146320561b0d2
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "104265283"
---
# <a name="general-requirements-for-application-development-wpd-api"></a><span data-ttu-id="bc67b-103">Общие требования для разработки приложений (API-интерфейс WPD)</span><span class="sxs-lookup"><span data-stu-id="bc67b-103">General Requirements for Application Development (WPD API)</span></span>

<span data-ttu-id="bc67b-104">Чтобы создать приложение для портативных устройств Windows, на компьютере должен быть установлен [пакет средств разработки программного обеспечения (SDK) для Windows](https://developer.microsoft.com/windows/downloads) .</span><span class="sxs-lookup"><span data-stu-id="bc67b-104">To create a Windows Portable Devices application, you must have the [Windows Software Development Kit (SDK)](https://developer.microsoft.com/windows/downloads) installed on your computer.</span></span> <span data-ttu-id="bc67b-105">Необходимые заголовки и библиотеки отображаются в следующем списке.</span><span class="sxs-lookup"><span data-stu-id="bc67b-105">The required headers and libraries appear in the following list.</span></span>

-   <span data-ttu-id="bc67b-106">Портабледевицегуидс. lib</span><span class="sxs-lookup"><span data-stu-id="bc67b-106">PortableDeviceGuids.lib</span></span>
-   <span data-ttu-id="bc67b-107">Портабледевице. h</span><span class="sxs-lookup"><span data-stu-id="bc67b-107">PortableDevice.h</span></span>
-   <span data-ttu-id="bc67b-108">Портабледевицетипес. h</span><span class="sxs-lookup"><span data-stu-id="bc67b-108">PortableDeviceTypes.h</span></span>
-   <span data-ttu-id="bc67b-109">Портабледевицеапи. h</span><span class="sxs-lookup"><span data-stu-id="bc67b-109">PortableDeviceApi.h</span></span>
-   <span data-ttu-id="bc67b-110">Любые другие необходимые библиотеки и заголовки, необходимые приложению для использования или визуализации файлов мультимедиа.</span><span class="sxs-lookup"><span data-stu-id="bc67b-110">Any other required libraries and headers required by your application to consume or render media files.</span></span>

<span data-ttu-id="bc67b-111">Если приложение поддерживает новые интерфейсы служб устройств, оно также будет включать в себя один или несколько следующих файлов заголовков.</span><span class="sxs-lookup"><span data-stu-id="bc67b-111">If your application supports the new Device Services interfaces, it will also include one or more of the following header files.</span></span>

-   <span data-ttu-id="bc67b-112">Анчорсинкдевицесервице. h</span><span class="sxs-lookup"><span data-stu-id="bc67b-112">AnchorSyncDeviceService.h</span></span>
-   <span data-ttu-id="bc67b-113">Бриджедевицесервице. h</span><span class="sxs-lookup"><span data-stu-id="bc67b-113">BridgeDeviceService.h</span></span>
-   <span data-ttu-id="bc67b-114">Календардевицесервице. h</span><span class="sxs-lookup"><span data-stu-id="bc67b-114">CalendarDeviceService.h</span></span>
-   <span data-ttu-id="bc67b-115">Контактдевицесервице. h</span><span class="sxs-lookup"><span data-stu-id="bc67b-115">ContactDeviceService.h</span></span>
-   <span data-ttu-id="bc67b-116">Девицесервицес. h</span><span class="sxs-lookup"><span data-stu-id="bc67b-116">DeviceServices.h</span></span>
-   <span data-ttu-id="bc67b-117">Фулленумсинкдевицесервице. h</span><span class="sxs-lookup"><span data-stu-id="bc67b-117">FullEnumSyncDeviceService.h</span></span>
-   <span data-ttu-id="bc67b-118">Хинтсдевицесервице. h</span><span class="sxs-lookup"><span data-stu-id="bc67b-118">HintsDeviceService.h</span></span>
-   <span data-ttu-id="bc67b-119">Мессажедевицесервице. h</span><span class="sxs-lookup"><span data-stu-id="bc67b-119">MessageDeviceService.h</span></span>
-   <span data-ttu-id="bc67b-120">Метадатадевицесервице. h</span><span class="sxs-lookup"><span data-stu-id="bc67b-120">MetadataDeviceService.h</span></span>
-   <span data-ttu-id="bc67b-121">Нотесдевицесервице. h</span><span class="sxs-lookup"><span data-stu-id="bc67b-121">NotesDeviceService.h</span></span>
-   <span data-ttu-id="bc67b-122">Рингтонедевицесервице. h</span><span class="sxs-lookup"><span data-stu-id="bc67b-122">RingtoneDeviceService.h</span></span>
-   <span data-ttu-id="bc67b-123">Статусдевицесервице. h</span><span class="sxs-lookup"><span data-stu-id="bc67b-123">StatusDeviceService.h</span></span>
-   <span data-ttu-id="bc67b-124">Синкдевицесервице. h</span><span class="sxs-lookup"><span data-stu-id="bc67b-124">SyncDeviceService.h</span></span>
-   <span data-ttu-id="bc67b-125">Таскдевицесервице. h</span><span class="sxs-lookup"><span data-stu-id="bc67b-125">TaskDeviceService.h</span></span>

<span data-ttu-id="bc67b-126">Из файлов, приведенных в предыдущем списке, Бриджедевицесервице. h и Девицесервице. h требуются для практически любого приложения, поддерживающего службы устройств. другие файлы определяют различные типы служб устройств и будут включаться соответствующим образом.</span><span class="sxs-lookup"><span data-stu-id="bc67b-126">Of the files in the previous list, BridgeDeviceService.h and DeviceService.h are required for almost any application that supports Device Services; the other files define different types of device services and would be included as appropriate.</span></span>

## <a name="related-topics"></a><span data-ttu-id="bc67b-127">См. также</span><span class="sxs-lookup"><span data-stu-id="bc67b-127">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="bc67b-128">**Портативные устройства Windows**</span><span class="sxs-lookup"><span data-stu-id="bc67b-128">**Windows Portable Devices**</span></span>](/windows/desktop/windows-portable-devices)
</dt> </dl>

 

 
