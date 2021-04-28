---
description: Удаление драйвера WPDUSB.SYS для переносных устройств Windows
ms.assetid: 3ad0c892-8b19-465d-af2f-9207f98e27b7
title: Удаление драйвера WPDUSB.SYS для переносных устройств Windows
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5931b63c5abb4534b2c8dd6619b4a3ead8b339be
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2021
ms.locfileid: "108116252"
---
# <a name="removal-of-wpdusbsys-driver-for-windows-portable-devices"></a><span data-ttu-id="99b4f-103">Удаление драйвера WPDUSB.SYS для переносных устройств Windows</span><span class="sxs-lookup"><span data-stu-id="99b4f-103">Removal of WPDUSB.SYS Driver for Windows Portable Devices</span></span>

## <a name="affected-platforms"></a><span data-ttu-id="99b4f-104">Затронутые платформы</span><span class="sxs-lookup"><span data-stu-id="99b4f-104">Affected Platforms</span></span>

<span data-ttu-id="99b4f-105">**Клиенты** — Windows 7</span><span class="sxs-lookup"><span data-stu-id="99b4f-105">**Clients** - Windows 7</span></span>  
<span data-ttu-id="99b4f-106">**Серверы** — Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="99b4f-106">**Servers** - Windows Server 2008 R2</span></span>  









## <a name="feature-impact"></a><span data-ttu-id="99b4f-107">Воздействие на функции</span><span class="sxs-lookup"><span data-stu-id="99b4f-107">Feature Impact</span></span>

 <span data-ttu-id="99b4f-108">**Серьезность** — низкая</span><span class="sxs-lookup"><span data-stu-id="99b4f-108">**Severity** - Low</span></span>  
<span data-ttu-id="99b4f-109">**Частота** -низкая</span><span class="sxs-lookup"><span data-stu-id="99b4f-109">**Frequency** - Low</span></span>  





## <a name="description"></a><span data-ttu-id="99b4f-110">Описание</span><span class="sxs-lookup"><span data-stu-id="99b4f-110">Description</span></span>

<span data-ttu-id="99b4f-111">Корпорация Майкрософт заменила компонент режима ядра в стеке драйверов USB для Windows Vista (WPDUSB.SYS) для портативных устройств Windows (WPD) с универсальным драйвером WINUSB.SYS.</span><span class="sxs-lookup"><span data-stu-id="99b4f-111">Microsoft has replaced the kernel mode component of the Windows Vista USB driver stack (WPDUSB.SYS) for Windows Portable Devices (WPD) with the generic WINUSB.SYS driver.</span></span> <span data-ttu-id="99b4f-112">Связь с исходным драйвером WPDUSB.SYS была выполнена с помощью кода закрытого управления вводом-выводом (IOCTL). их поддержка также была удалена.</span><span class="sxs-lookup"><span data-stu-id="99b4f-112">Communication with the original WPDUSB.SYS driver was via private I/O Control (IOCTL) codes; support of these has also been removed.</span></span>

<span data-ttu-id="99b4f-113">Любой потребитель этих кодов IOCTL будет отвечать за правильную интерпретацию и реализацию протокола передачи мультимедиа (MTP).</span><span class="sxs-lookup"><span data-stu-id="99b4f-113">Any consumer of these IOCTL codes would have been responsible for proper interpretation and implementation of the Media Transfer Protocol (MTP).</span></span> <span data-ttu-id="99b4f-114">В Windows Vista не поддерживалось использование этих кодов IOCTL приложениями сторонних производителей.</span><span class="sxs-lookup"><span data-stu-id="99b4f-114">Windows Vista did not support use of these IOCTL codes by third-party applications.</span></span>

## <a name="manifestation-of-impact"></a><span data-ttu-id="99b4f-115">Влияние на манифесты</span><span class="sxs-lookup"><span data-stu-id="99b4f-115">Manifestation of Impact</span></span>

<span data-ttu-id="99b4f-116">Любое приложение, которое зависит от доступности этих закрытых кодов IOCTL, больше не будет иметь доступа к устройствам MTP, подключенным к USB.</span><span class="sxs-lookup"><span data-stu-id="99b4f-116">Any application that depended on the availability of these private IOCTL codes would no longer have access to USB-connected MTP devices.</span></span>

## <a name="mitigation"></a><span data-ttu-id="99b4f-117">Меры по снижению риска</span><span class="sxs-lookup"><span data-stu-id="99b4f-117">Mitigation</span></span>

<span data-ttu-id="99b4f-118">Пользователи приложения, которые зависят от закрытых кодов IOCTL, должны использовать другое приложение (или обновленную версию приложения) для доступа к устройству MTP, подключенному к USB.</span><span class="sxs-lookup"><span data-stu-id="99b4f-118">Users of an application that depends on the private IOCTL codes must use a different application (or an updated version of the application) to access the USB-connected MTP device.</span></span>

## <a name="solution"></a><span data-ttu-id="99b4f-119">Решение</span><span class="sxs-lookup"><span data-stu-id="99b4f-119">Solution</span></span>

<span data-ttu-id="99b4f-120">Приложения должны использовать API портативных устройств Windows (WPD) для поиска и взаимодействия с любым устройством WPD.</span><span class="sxs-lookup"><span data-stu-id="99b4f-120">Applications should use the Windows Portable Devices (WPD) API to find and interact with any WPD Device.</span></span> <span data-ttu-id="99b4f-121">Несмотря на то что значительный процент устройств WPD применяет MTP для обмена данными с компьютером, WPD не ограничивается только устройствами MTP.</span><span class="sxs-lookup"><span data-stu-id="99b4f-121">Although a significant percentage of WPD devices implement MTP for communication with the PC, WPD is not limited to just MTP devices.</span></span> <span data-ttu-id="99b4f-122">Кроме того, если прямой доступ к устройству через частные запросы IOCTL будет ограничен приложением для взаимодействия только с устройствами, подключенными к USB, использование API-интерфейса WPD расширяет список вариантов подключения до других протоколов связи (например, Wi-Fi).</span><span class="sxs-lookup"><span data-stu-id="99b4f-122">In addition, where direct access to the device via the private IOCTLs would have limited the application to communication with only USB-connected devices, use of the WPD API expands the list of connectivity options to other communication protocols (for example, Wi-Fi).</span></span> <span data-ttu-id="99b4f-123">В редких случаях, когда приложение должно быть совместимым с MTP, API-интерфейс WPD предоставляет сквозной механизм для необработанных команд MTP.</span><span class="sxs-lookup"><span data-stu-id="99b4f-123">In the rare cases when the application must be MTP-aware, the WPD API provides a pass-through mechanism for raw MTP commands.</span></span>

## <a name="leveraging-feature-capabilities"></a><span data-ttu-id="99b4f-124">Использование возможностей функций</span><span class="sxs-lookup"><span data-stu-id="99b4f-124">Leveraging Feature Capabilities</span></span>

<span data-ttu-id="99b4f-125">API-интерфейс WPD поддерживается в Windows XP (с помощью пакета SDK формата Windows), Windows Vista и Windows 7.</span><span class="sxs-lookup"><span data-stu-id="99b4f-125">The WPD API is supported in Windows XP (via the Windows Format SDK), Windows Vista and Windows 7.</span></span> <span data-ttu-id="99b4f-126">В реализации WPD в Windows 7 добавлена поддержка MTP через Bluetooth.</span><span class="sxs-lookup"><span data-stu-id="99b4f-126">The Windows 7 implementation of WPD adds support for MTP over Bluetooth.</span></span>

## <a name="links-to-other-resources"></a><span data-ttu-id="99b4f-127">Ссылки на другие ресурсы</span><span class="sxs-lookup"><span data-stu-id="99b4f-127">Links to Other Resources</span></span>

[<span data-ttu-id="99b4f-128">Портативные устройства Windows</span><span class="sxs-lookup"><span data-stu-id="99b4f-128">Windows Portable Devices</span></span>](../windows-portable-devices.md)

 

 
