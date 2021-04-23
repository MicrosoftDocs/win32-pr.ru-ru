---
description: Программный интерфейс WPD
ms.assetid: 3e2be15f-7af7-4e76-89b1-f9bc591c4f1b
title: Программный интерфейс WPD
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5c44dbcf731aa46941599b99766e52fa67a5c5a6
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "105712563"
---
# <a name="wpd-application-programming-interface"></a><span data-ttu-id="50952-103">Программный интерфейс WPD</span><span class="sxs-lookup"><span data-stu-id="50952-103">WPD Application Programming Interface</span></span>

<span data-ttu-id="50952-104">Приложения, основанные на портативных устройствах Windows, могут просматривать устройства, отправлять и получать содержимое, а также управлять устройством, например, делать снимки или отправлять текстовые сообщения.</span><span class="sxs-lookup"><span data-stu-id="50952-104">Applications built on Windows Portable Devices can explore a device, send and receive content, and even control the device, for example, take a picture or send a text message.</span></span> <span data-ttu-id="50952-105">Система разработана настолько гибкой, чтобы можно было исследовать различные типы устройств и расширяться, чтобы разработчики драйверов могли определять пользовательские свойства и команды для пользовательских устройств.</span><span class="sxs-lookup"><span data-stu-id="50952-105">The system is designed to be flexible so that many types of devices can be explored, and extensible so that driver developers can define custom properties and commands for custom devices.</span></span>

<span data-ttu-id="50952-106">В следующей таблице описаны основные темы этой документации.</span><span class="sxs-lookup"><span data-stu-id="50952-106">The following table describes the main topics of this documentation.</span></span>



| <span data-ttu-id="50952-107">Раздел</span><span class="sxs-lookup"><span data-stu-id="50952-107">Topic</span></span>                                                                                                                  | <span data-ttu-id="50952-108">Описание</span><span class="sxs-lookup"><span data-stu-id="50952-108">Description</span></span>                                                                                                |
|------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="50952-109">Общие требования для разработки приложений</span><span class="sxs-lookup"><span data-stu-id="50952-109">General Requirements for Application Development</span></span>](general-requirements-for-application-development.md)               | <span data-ttu-id="50952-110">Требования к оборудованию и программному обеспечению для разработки драйверов и приложений с помощью портативных устройств Windows.</span><span class="sxs-lookup"><span data-stu-id="50952-110">Hardware and software requirements to develop drivers and applications using Windows Portable Devices.</span></span>     |
| [<span data-ttu-id="50952-111">Требования к приложениям DRM-Enabled Windows Media</span><span class="sxs-lookup"><span data-stu-id="50952-111">Requirements for Windows Media DRM-Enabled Applications</span></span>](requirements-for-windows-media-drm-enabled-applications.md) | <span data-ttu-id="50952-112">Свойства, необходимые для передачи содержимого, защищенного с помощью DRM Windows Media.</span><span class="sxs-lookup"><span data-stu-id="50952-112">Properties that are required to enable Windows Media DRM-protected content transfers.</span></span>                      |
| [<span data-ttu-id="50952-113">Примеры</span><span class="sxs-lookup"><span data-stu-id="50952-113">Samples</span></span>](sample.md)                                                                                                  | <span data-ttu-id="50952-114">Описание двух классических приложений командной строки, предоставляемых с этим пакетом средств разработки программного обеспечения.</span><span class="sxs-lookup"><span data-stu-id="50952-114">Description of two command-line desktop applications that are supplied with this software development kit.</span></span> |
| [<span data-ttu-id="50952-115">Общие сведения о приложении</span><span class="sxs-lookup"><span data-stu-id="50952-115">Application Overview</span></span>](application-overview.md)                                                                       | <span data-ttu-id="50952-116">Основные понятия, используемые в портативных устройствах Windows.</span><span class="sxs-lookup"><span data-stu-id="50952-116">Key concepts used in Windows Portable Devices.</span></span>                                                             |
| [<span data-ttu-id="50952-117">Руководство по программированию</span><span class="sxs-lookup"><span data-stu-id="50952-117">Programming Guide</span></span>](programming-guide.md)                                                                             | <span data-ttu-id="50952-118">Основные задачи, которые будет выполнять приложение, с пошаговыми инструкциями и фрагментами кода.</span><span class="sxs-lookup"><span data-stu-id="50952-118">Key tasks that an application will perform, with step-by-step instructions and code snippets.</span></span>              |
| [<span data-ttu-id="50952-119">Справочник по программированию</span><span class="sxs-lookup"><span data-stu-id="50952-119">Programming Reference</span></span>](programming-reference.md)                                                                     | <span data-ttu-id="50952-120">Справочное руководство по интерфейсам и типам данных, определенным портативными устройствами Windows.</span><span class="sxs-lookup"><span data-stu-id="50952-120">Reference guide to the interfaces and data types defined by Windows Portable Devices.</span></span>                      |



 

<span data-ttu-id="50952-121">Приложения, созданные на основе Windows Media диспетчер устройств или получения образа Windows, могут получать доступ к портативным устройствам Windows через уровень совместимости.</span><span class="sxs-lookup"><span data-stu-id="50952-121">Applications built on Windows Media Device Manager or Windows Image Acquisition can access Windows Portable Devices through a compatibility layer.</span></span>

<span data-ttu-id="50952-122">Корпорация Майкрософт предоставляет несколько драйверов для стандартных протоколов и устройств, включая устройства передачи мультимедиа (MTP) и устройства класса запоминающих устройств (MSC).</span><span class="sxs-lookup"><span data-stu-id="50952-122">Microsoft provides several drivers for standard protocols and devices, including Media Transport Protocol (MTP) devices and Mass Storage Class (MSC) devices.</span></span> <span data-ttu-id="50952-123">Если вы знакомы с платформой User-Mode Driver Framework, вы можете разрабатывать собственные драйверы для пользовательских устройств.</span><span class="sxs-lookup"><span data-stu-id="50952-123">If you are familiar with the User-Mode Driver Framework, you can develop your own drivers for custom devices.</span></span>

 

 



