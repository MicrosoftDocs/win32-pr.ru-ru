---
title: Объявление возможностей устройства
description: В этом разделе объясняется, как объявить GUID возможностей устройства.
ms.assetid: C663F8D2-2CB6-4C3C-A1EB-A3D93AA71FC8
ms.topic: article
ms.date: 02/11/2020
ms.openlocfilehash: 0b1f98717c7e9487874aa71691beefbac635660a
ms.sourcegitcommit: 3d718d8f69d3f86eaecf94c5705d761c5a9ef4a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/20/2020
ms.locfileid: "103987971"
---
# <a name="declaring-the-device-capability"></a><span data-ttu-id="ff683-103">Объявление возможностей устройства</span><span class="sxs-lookup"><span data-stu-id="ff683-103">Declaring the Device Capability</span></span>

<span data-ttu-id="ff683-104">В этом разделе объясняется, как объявить GUID возможностей устройства.</span><span class="sxs-lookup"><span data-stu-id="ff683-104">This topic explains how to declare the device capability GUID.</span></span> <span data-ttu-id="ff683-105">Все приложения, предназначенные для настраиваемых драйверов, должны объявлять эту возможность.</span><span class="sxs-lookup"><span data-stu-id="ff683-105">All applications that target custom drivers must declare this capability.</span></span>

<span data-ttu-id="ff683-106">В манифесте приложения необходимо добавить возможность устройства, как показано ниже.</span><span class="sxs-lookup"><span data-stu-id="ff683-106">In your application manifest, you'll need to add a device capability, as follows:</span></span>

<span data-ttu-id="ff683-107">Это пример объявления возможности для пользовательского устройства.</span><span class="sxs-lookup"><span data-stu-id="ff683-107">This is an example of a capability declaration for a custom device.</span></span> <span data-ttu-id="ff683-108">GUID — это идентификатор GUID класса интерфейса устройства.</span><span class="sxs-lookup"><span data-stu-id="ff683-108">The GUID is the GUID of the device interface class.</span></span>

```XML
<DeviceCapability Name="0B1F1048-B64B-FC9A-CED7-7E4FED3A0DEB" />
```

## <a name="related-topics"></a><span data-ttu-id="ff683-109">См. также</span><span class="sxs-lookup"><span data-stu-id="ff683-109">Related topics</span></span>

<span data-ttu-id="ff683-110">[Пример пользовательского доступа к драйверу](https://github.com/microsoftarchive/msdn-code-gallery-microsoft/tree/411c271e537727d737a53fa2cbe99eaecac00cc0/Official%20Windows%20Platform%20Sample/Custom%20driver%20access%20sample), [приложения для устройств UWP для внутренних устройств](/windows-hardware/drivers/devapps/uwp-device-apps-for-specialized-devices), [центр разработки оборудования](/windows-hardware/drivers/)</span><span class="sxs-lookup"><span data-stu-id="ff683-110">[Custom Driver Access Sample](https://github.com/microsoftarchive/msdn-code-gallery-microsoft/tree/411c271e537727d737a53fa2cbe99eaecac00cc0/Official%20Windows%20Platform%20Sample/Custom%20driver%20access%20sample), [UWP device apps for internal devices](/windows-hardware/drivers/devapps/uwp-device-apps-for-specialized-devices), [Hardware Dev Center](/windows-hardware/drivers/)</span></span>
