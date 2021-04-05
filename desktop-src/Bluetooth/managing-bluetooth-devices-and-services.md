---
title: Управление устройствами и службами Bluetooth
description: Два основных подхода к программированию Bluetooth для программирования Windows с помощью интерфейса сокетов Windows и управления устройствами напрямую с интерфейсами Bluetooth, не поддерживающими сокеты.
ms.assetid: 0eb7d339-6d23-4313-b1ed-7ab403a5a81d
keywords:
- Управление устройствами и службами Bluetooth
- Устройства и службы Bluetooth, управление
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 61cf3657dff2091eda4b26d14f6504b74f943983
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "104133931"
---
# <a name="managing-bluetooth-devices-and-services"></a><span data-ttu-id="ae7ac-105">Управление устройствами и службами Bluetooth</span><span class="sxs-lookup"><span data-stu-id="ae7ac-105">Managing Bluetooth Devices and Services</span></span>

<span data-ttu-id="ae7ac-106">В этом разделе описывается, как использовать API Bluetooth для непосредственного управления устройствами и службами Bluetooth.</span><span class="sxs-lookup"><span data-stu-id="ae7ac-106">This section describes how to use the Bluetooth API to directly control Bluetooth devices and services.</span></span>

<span data-ttu-id="ae7ac-107">Сведения об использовании интерфейса сокетов Windows для программирования Bluetooth в Windows см. в разделе [Поддержка Bluetooth в Windows Sockets](windows-sockets-support-for-bluetooth.md).</span><span class="sxs-lookup"><span data-stu-id="ae7ac-107">For information about using the Windows Sockets interface to program Bluetooth on Windows, see [Windows Sockets Support for Bluetooth](windows-sockets-support-for-bluetooth.md).</span></span>

> [!Note]  
> <span data-ttu-id="ae7ac-108">Bluetooth не мешает функциям управления питанием прерывать передачу данных Bluetooth.</span><span class="sxs-lookup"><span data-stu-id="ae7ac-108">Bluetooth does not prevent power management features from interrupting Bluetooth transmissions.</span></span> <span data-ttu-id="ae7ac-109">Приложения с поддержкой Bluetooth могут отслеживать сообщения о питании, чтобы предотвратить такое прерывание.</span><span class="sxs-lookup"><span data-stu-id="ae7ac-109">Bluetooth-enabled applications can monitor power messages to prevent such interruption.</span></span> <span data-ttu-id="ae7ac-110">Дополнительные сведения см. [в разделе Использование функции управления питанием](/windows/desktop/Power/using-power-management).</span><span class="sxs-lookup"><span data-stu-id="ae7ac-110">For more information, see [Using Power Management](/windows/desktop/Power/using-power-management).</span></span>

 

<span data-ttu-id="ae7ac-111">Этот раздел содержит следующие подразделы.</span><span class="sxs-lookup"><span data-stu-id="ae7ac-111">This section contains the following topics.</span></span>

| <span data-ttu-id="ae7ac-112">Section</span><span class="sxs-lookup"><span data-stu-id="ae7ac-112">Section</span></span>                                                                               | <span data-ttu-id="ae7ac-113">Содержимое</span><span class="sxs-lookup"><span data-stu-id="ae7ac-113">Content</span></span>                                                                       |
|---------------------------------------------------------------------------------------|-------------------------------------------------------------------------------|
| [<span data-ttu-id="ae7ac-114">Выбор устройства Bluetooth</span><span class="sxs-lookup"><span data-stu-id="ae7ac-114">Selecting a Bluetooth Device</span></span>](selecting-a-bluetooth-device.md)                      | <span data-ttu-id="ae7ac-115">Описывает, как выбрать устройство Bluetooth.</span><span class="sxs-lookup"><span data-stu-id="ae7ac-115">Describes how to select a Bluetooth device.</span></span>                                   |
| [<span data-ttu-id="ae7ac-116">Сообщения Bluetooth и WM \_ девицечанже</span><span class="sxs-lookup"><span data-stu-id="ae7ac-116">Bluetooth and WM\_DEVICECHANGE Messages</span></span>](bluetooth-and-wm-devicechange-messages.md) | <span data-ttu-id="ae7ac-117">Объясняет взаимодействие между сообщениями Bluetooth и **WM \_ девицечанже** .</span><span class="sxs-lookup"><span data-stu-id="ae7ac-117">Explains the interaction between Bluetooth and **WM\_DEVICECHANGE** messages.</span></span> |



 

 

 