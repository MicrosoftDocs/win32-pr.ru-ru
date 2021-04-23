---
description: Классы устройств допускают спецификацию свойств значков, меток и Девицехандлерс для любого устройства этого класса.
ms.assetid: E32C1BA6-B520-4809-A9E9-48813C7EBAA4
title: Указание значка, метки или обработчика устройства для устройства с помощью класса устройств
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 46f81ee6fa469a6bec13abbc1d8a088f5fb334ea
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104997694"
---
# <a name="how-to-specify-an-icon-label-or-device-handler-for-a-device-using-a-device-class"></a><span data-ttu-id="ba8e8-103">Указание значка, метки или обработчика устройства для устройства с помощью класса устройств</span><span class="sxs-lookup"><span data-stu-id="ba8e8-103">How to Specify an Icon, Label, or Device Handler for a Device Using a Device Class</span></span>

<span data-ttu-id="ba8e8-104">Классы устройств допускают спецификацию свойств значков, меток и Девицехандлерс для любого устройства этого класса.</span><span class="sxs-lookup"><span data-stu-id="ba8e8-104">Device classes allow the specification of the Icons, Label, and DeviceHandlers properties for any device of that class.</span></span> <span data-ttu-id="ba8e8-105">Это похоже на использование групп устройств, но классы устройств и их членство определяются оборудованием, а не создаются или назначаются.</span><span class="sxs-lookup"><span data-stu-id="ba8e8-105">This is similar to the use of device groups, but device classes and their memberships are determined by the hardware rather than being created or assigned.</span></span> <span data-ttu-id="ba8e8-106">Имя ключа класса, которое является идентификатором GUID интерфейса самонастраивающийся устройства, находится в разделе ключа **девицеклассес** .</span><span class="sxs-lookup"><span data-stu-id="ba8e8-106">Each class key name, which is the Plug and Play device interface GUID, is found under the **DeviceClasses** key.</span></span> <span data-ttu-id="ba8e8-107">В разделе индивидуальный ключ класса назначьте значения значков, меток и Девицехандлерс.</span><span class="sxs-lookup"><span data-stu-id="ba8e8-107">Under the individual class key, assign the values for Icons, Label, and DeviceHandlers.</span></span>

## <a name="instructions"></a><span data-ttu-id="ba8e8-108">Инструкции</span><span class="sxs-lookup"><span data-stu-id="ba8e8-108">Instructions</span></span>

### <a name="step-1"></a><span data-ttu-id="ba8e8-109">Шаг 1.</span><span class="sxs-lookup"><span data-stu-id="ba8e8-109">Step 1:</span></span>

<span data-ttu-id="ba8e8-110">В следующем примере показаны ключ класса и значения Девицехандлерс для интерфейса Volume.</span><span class="sxs-lookup"><span data-stu-id="ba8e8-110">The following example shows the class key and DeviceHandlers values for the volume interface.</span></span>

```
HKEY_LOCAL_MACHINE
   SOFTWARE
      Microsoft
         Windows
            CurrentVersion
               Explorer
                  AutoplayHandlers
                     DeviceClasses
                        {53f5630d-b6bf-11d0-94f2-00a0c91efb8b}
                           DeviceHandlers [REG_SZ] = GenericVolumeHandler
```

<span data-ttu-id="ba8e8-111">Вы также можете добавить настраиваемые свойства устройства в раздел класс устройства.</span><span class="sxs-lookup"><span data-stu-id="ba8e8-111">You can also add custom device properties under the device class key.</span></span> <span data-ttu-id="ba8e8-112">Затем настраиваемые свойства устройства применяются ко всем устройствам в этом классе.</span><span class="sxs-lookup"><span data-stu-id="ba8e8-112">The custom device properties then apply to all devices in that class.</span></span> <span data-ttu-id="ba8e8-113">Устройства и обработчики устройств всегда должны иметь связанные значки и метки для удовлетворения минимальных требований к удобству использования.</span><span class="sxs-lookup"><span data-stu-id="ba8e8-113">Devices and device handlers should always have associated icons and labels to meet minimum usability requirements.</span></span>

> [!Note]  
> <span data-ttu-id="ba8e8-114">Свойства, определенные на уровне экземпляра устройства, имеют приоритет над свойствами, определенными на уровне группы устройств, которые, в свою очередь, имеют приоритет над свойствами, определенными на уровне класса устройства.</span><span class="sxs-lookup"><span data-stu-id="ba8e8-114">Properties that are defined at the device instance level take precedence over properties defined at the device group level, which in turn take precedence over properties defined at the device class level.</span></span>

 

 

 



