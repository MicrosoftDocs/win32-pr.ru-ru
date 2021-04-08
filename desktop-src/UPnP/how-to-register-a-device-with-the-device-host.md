---
title: Как зарегистрировать устройство с помощью узла устройства
description: Можно зарегистрировать работающее устройство или устройство, не выполняющее запуск.
ms.assetid: 40e30881-d5fb-4cf9-8dd7-0d50d2621d5c
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d3be1561d82741ce33e7eb05e63b015d5cb38f52
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/16/2019
ms.locfileid: "104068013"
---
# <a name="how-to-register-a-device-with-the-device-host"></a><span data-ttu-id="e70e5-103">Как зарегистрировать устройство с помощью узла устройства</span><span class="sxs-lookup"><span data-stu-id="e70e5-103">How to Register a Device with the Device Host</span></span>

<span data-ttu-id="e70e5-104">Можно зарегистрировать работающее устройство или устройство, не выполняющее запуск.</span><span class="sxs-lookup"><span data-stu-id="e70e5-104">You can register either a running device or a non-running device.</span></span>

## <a name="registering-a-running-device"></a><span data-ttu-id="e70e5-105">Регистрация работающего устройства</span><span class="sxs-lookup"><span data-stu-id="e70e5-105">Registering a Running Device</span></span>

<span data-ttu-id="e70e5-106">Устройства регистрируются с помощью интерфейса [**иупнпрегистрар**](/windows/desktop/api/Upnphost/nn-upnphost-iupnpregistrar) .</span><span class="sxs-lookup"><span data-stu-id="e70e5-106">Devices are registered using the [**IUPnPRegistrar**](/windows/desktop/api/Upnphost/nn-upnphost-iupnpregistrar) interface.</span></span> <span data-ttu-id="e70e5-107">Только администраторы могут регистрировать выполняющиеся устройства.</span><span class="sxs-lookup"><span data-stu-id="e70e5-107">Only administrators are allowed to register running devices.</span></span> <span data-ttu-id="e70e5-108">Чтобы зарегистрировать устройство с запущенным объектом управления устройством, приложение должно вызвать [**иупнпрегистрар:: регистерруннингдевице**](/windows/desktop/api/Upnphost/nf-upnphost-iupnpregistrar-registerrunningdevice), передав следующее:</span><span class="sxs-lookup"><span data-stu-id="e70e5-108">To register a device that has a running device control object, an application must invoke [**IUPnPRegistrar::RegisterRunningDevice**](/windows/desktop/api/Upnphost/nf-upnphost-iupnpregistrar-registerrunningdevice), passing the following:</span></span>

-   <span data-ttu-id="e70e5-109">Текст описания устройства.</span><span class="sxs-lookup"><span data-stu-id="e70e5-109">The text of the device's description.</span></span>
-   <span data-ttu-id="e70e5-110">Указатель **IUnknown** на объект управления устройством.</span><span class="sxs-lookup"><span data-stu-id="e70e5-110">An **IUnknown** pointer to the device control object.</span></span>
-   <span data-ttu-id="e70e5-111">Строка инициализации, которая передается в метод [**иупнпдевицеконтрол:: Initialize**](/windows/desktop/api/Upnphost/nf-upnphost-iupnpdevicecontrol-initialize) объекта управления устройством.</span><span class="sxs-lookup"><span data-stu-id="e70e5-111">An initialization string that is passed to the device control object's [**IUPnPDeviceControl::Initialize**](/windows/desktop/api/Upnphost/nf-upnphost-iupnpdevicecontrol-initialize) method.</span></span>
-   <span data-ttu-id="e70e5-112">Расположение каталога ресурсов.</span><span class="sxs-lookup"><span data-stu-id="e70e5-112">The location of the resource directory.</span></span>
-   <span data-ttu-id="e70e5-113">Время существования устройства.</span><span class="sxs-lookup"><span data-stu-id="e70e5-113">The lifetime of the device.</span></span>
-   <span data-ttu-id="e70e5-114">Параметр идентификатора устройства (выходной параметр), который является возвращаемым значением этого вызова; Указатель на идентификатор устройства возвращается в C++.</span><span class="sxs-lookup"><span data-stu-id="e70e5-114">The Device ID parameter (an OUT parameter), which is the return value of this call; a pointer to the Device ID is returned in C++.</span></span>

## <a name="registering-a-non-running-device"></a><span data-ttu-id="e70e5-115">Регистрация неработающего устройства</span><span class="sxs-lookup"><span data-stu-id="e70e5-115">Registering a Non-Running Device</span></span>

<span data-ttu-id="e70e5-116">По умолчанию только администраторы и интерактивные пользователи могут регистрировать устройства, которые не работают.</span><span class="sxs-lookup"><span data-stu-id="e70e5-116">By default, only administrators and interactive users are allowed to register non-running devices.</span></span> <span data-ttu-id="e70e5-117">Чтобы зарегистрировать устройство в неработающем объекте управления устройством, приложение использует метод [**иупнпрегистрар:: RegisterDevice**](/windows/desktop/api/Upnphost/nf-upnphost-iupnpregistrar-registerdevice) .</span><span class="sxs-lookup"><span data-stu-id="e70e5-117">To register a device with a device control object that is not running, the application uses the [**IUPnPRegistrar::RegisterDevice**](/windows/desktop/api/Upnphost/nf-upnphost-iupnpregistrar-registerdevice) method.</span></span>

<span data-ttu-id="e70e5-118">Чтобы программно зарегистрировать устройство в неработающем объекте управления устройством, приложение должно вызвать [**иупнпрегистрар:: RegisterDevice**](/windows/desktop/api/Upnphost/nf-upnphost-iupnpregistrar-registerdevice) и передать ему следующие параметры:</span><span class="sxs-lookup"><span data-stu-id="e70e5-118">To programmatically register a device with a non-running device control object, the application must invoke [**IUPnPRegistrar::RegisterDevice**](/windows/desktop/api/Upnphost/nf-upnphost-iupnpregistrar-registerdevice) and pass it the following parameters:</span></span>

-   <span data-ttu-id="e70e5-119">Текст описания устройства.</span><span class="sxs-lookup"><span data-stu-id="e70e5-119">The text of the device's description.</span></span>
-   <span data-ttu-id="e70e5-120">Идентификатор ProgID объекта управления устройством.</span><span class="sxs-lookup"><span data-stu-id="e70e5-120">The ProgID of the device control object.</span></span>
-   <span data-ttu-id="e70e5-121">Строка инициализации, которая передается в метод [**иупнпдевицеконтрол:: Initialize**](/windows/desktop/api/Upnphost/nf-upnphost-iupnpdevicecontrol-initialize) объекта управления устройством.</span><span class="sxs-lookup"><span data-stu-id="e70e5-121">An initialization string that is passed to the device control object's [**IUPnPDeviceControl::Initialize**](/windows/desktop/api/Upnphost/nf-upnphost-iupnpdevicecontrol-initialize) method.</span></span>
-   <span data-ttu-id="e70e5-122">Идентификатор контейнера.</span><span class="sxs-lookup"><span data-stu-id="e70e5-122">A container ID.</span></span>
-   <span data-ttu-id="e70e5-123">Расположение каталога ресурсов.</span><span class="sxs-lookup"><span data-stu-id="e70e5-123">The location of the resource directory.</span></span>
-   <span data-ttu-id="e70e5-124">Время существования устройства.</span><span class="sxs-lookup"><span data-stu-id="e70e5-124">The lifetime of the device.</span></span>
-   <span data-ttu-id="e70e5-125">Параметр идентификатора устройства (выходной параметр), который является возвращаемым значением этого вызова; Указатель на идентификатор устройства возвращается в C++.</span><span class="sxs-lookup"><span data-stu-id="e70e5-125">The Device ID parameter (an OUT parameter), which is the return value of this call; a pointer to the Device ID is returned in C++.</span></span>

<span data-ttu-id="e70e5-126">Регистрация неработающих устройств может быть настроена на сохранение во время загрузки системы (при отмене публикации устройств на этапе завершения работы).</span><span class="sxs-lookup"><span data-stu-id="e70e5-126">The registrations of non-running devices can be configured to persist across system boots (the devices are unpublished during the shutdown phase).</span></span> <span data-ttu-id="e70e5-127">Таким образом, если они настроены таким образом, устройства публикуются и объявляются каждый раз при загрузке компьютера.</span><span class="sxs-lookup"><span data-stu-id="e70e5-127">Therefore, if they are configured this way, devices are published and announced every time the computer is booted.</span></span>

 

 




