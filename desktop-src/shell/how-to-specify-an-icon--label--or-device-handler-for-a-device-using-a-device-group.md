---
description: Группы устройств допускают спецификацию свойств значков, меток или Девицехандлерс для любого устройства, которое объявляет саму часть этой группы.
ms.assetid: 84433068-A869-479D-8ADA-E8221B38CCAE
title: Указание значка, метки или обработчика устройства для устройства с помощью группы устройств
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3e534aa6fa1bc7dbfe1bae3a2825a14f18096176
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "103998448"
---
# <a name="how-to-specify-an-icon-label-or-device-handler-for-a-device-using-a-device-group"></a><span data-ttu-id="f59fd-103">Указание значка, метки или обработчика устройства для устройства с помощью группы устройств</span><span class="sxs-lookup"><span data-stu-id="f59fd-103">How to Specify an Icon, Label, or Device Handler for a Device Using a Device Group</span></span>

<span data-ttu-id="f59fd-104">Группы устройств допускают спецификацию свойств значков, меток или Девицехандлерс для любого устройства, которое объявляет саму часть этой группы.</span><span class="sxs-lookup"><span data-stu-id="f59fd-104">Device groups allow the specification of the Icons, Label, or DeviceHandlers properties for any device that declares itself part of that group.</span></span> <span data-ttu-id="f59fd-105">Если группа устройств не является группой устройств, предоставленной системой, ключ, определяющий группу устройств, будет добавлен в раздел **аутоплайхандлерс** \\ **девицеграупс** Key.</span><span class="sxs-lookup"><span data-stu-id="f59fd-105">If the device group is not a system-provided device group, a key that defines the device group will be added under the **AutoplayHandlers**\\**DeviceGroups** key.</span></span> <span data-ttu-id="f59fd-106">Для каждой группы не нужно задавать все три свойства; можно задать только те свойства, которые необходимо настроить.</span><span class="sxs-lookup"><span data-stu-id="f59fd-106">You do not need to set all three properties for each group; you can set only those properties that you want to customize.</span></span> <span data-ttu-id="f59fd-107">Однако устройства и обработчики устройств всегда должны иметь связанные значки и метки для удовлетворения минимальных требований к удобству использования.</span><span class="sxs-lookup"><span data-stu-id="f59fd-107">However, devices and device handlers should always have associated icons and labels to meet minimum usability requirements.</span></span>

## <a name="instructions"></a><span data-ttu-id="f59fd-108">Инструкции</span><span class="sxs-lookup"><span data-stu-id="f59fd-108">Instructions</span></span>


<span data-ttu-id="f59fd-109">В следующем примере используется система с несколькими подключенными дисками ZIP.</span><span class="sxs-lookup"><span data-stu-id="f59fd-109">The following example uses a system with several attached Zip drives.</span></span> <span data-ttu-id="f59fd-110">Не указывая значки, метки и значения Девицехандлерс для каждого диска отдельно, создайте группу устройств с именем Зипдриве и определите в ней эти значения.</span><span class="sxs-lookup"><span data-stu-id="f59fd-110">Without specifying the Icons, Label, and DeviceHandlers values for each drive individually, you create a device group called ZipDrive and define those values within it.</span></span> <span data-ttu-id="f59fd-111">Затем каждый диск ZIP объявляется членом группы Зипдриве.</span><span class="sxs-lookup"><span data-stu-id="f59fd-111">Each Zip drive is then declared a member of the ZipDrive group.</span></span>

<span data-ttu-id="f59fd-112">Сначала определите группу устройств, добавив следующий ключ *зипдриве* и его значения.</span><span class="sxs-lookup"><span data-stu-id="f59fd-112">First, define the device group by adding the following *ZipDrive* key and its values.</span></span>

```
HKEY_LOCAL_MACHINE
   SOFTWARE
      Microsoft
         Windows
            CurrentVersion
               Explorer
                  AutoplayHandlers
                     DeviceGroups
                        ZipDrive
                           Icons [REG_MULTI_SZ] = %SystemRoot%\system32\mydll.dll,-103
                           NoMediaIcons [REG_MULTI_SZ] = %SystemRoot%\system32\mydll.dll,-104
                           Label [REG_SZ] = My Custom Device Label
                           DeviceHandlers [REG_SZ] = MyDeviceHandler
```

<span data-ttu-id="f59fd-113">Затем каждое устройство ZIP-накопителя объявляется как часть группы Зипдриве, наследуя свойства этой группы.</span><span class="sxs-lookup"><span data-stu-id="f59fd-113">Each Zip drive device is then declared as part of the ZipDrive group, inheriting the properties of that group.</span></span> <span data-ttu-id="f59fd-114">В разделе **девицепараметерс** (ключ) экземпляра устройства добавьте значение с именем девицеграуп в качестве типа **reg \_ SZ**.</span><span class="sxs-lookup"><span data-stu-id="f59fd-114">Under the **DeviceParameters** key of the device instance, add a value named DeviceGroup as type **REG\_SZ**.</span></span> <span data-ttu-id="f59fd-115">Запись данных для этого значения — это имя группы устройств.</span><span class="sxs-lookup"><span data-stu-id="f59fd-115">The data entry for this value is the name of the device group.</span></span>

```
HKEY_LOCAL_MACHINE
   SYSTEM
      CurrentControlSet
         Enum
            USB
               Vid_059b&Pid_0031
                  059B003112010E93
                     Device Parameters
                        DeviceGroup [REG_SZ] = ZipDrive
```

<span data-ttu-id="f59fd-116">Кроме того, можно добавить настраиваемые свойства устройств, кроме значков, меток и Девицехандлерс, в ключе группы устройств, а затем применить их ко всем устройствам, принадлежащим к этой группе устройств.</span><span class="sxs-lookup"><span data-stu-id="f59fd-116">You can also add custom device properties other than Icons, Label, and DeviceHandlers under the device group's key and then apply them to all devices that belong to that device group.</span></span>

> [!Note]  
> <span data-ttu-id="f59fd-117">Свойства, определенные на уровне экземпляра устройства, имеют приоритет над свойствами, определенными на уровне группы устройств, которые, в свою очередь, имеют приоритет над свойствами, определенными на уровне класса устройства.</span><span class="sxs-lookup"><span data-stu-id="f59fd-117">Properties that are defined at the device instance level take precedence over properties defined at the device group level, which in turn take precedence over properties defined at the device class level.</span></span>

 

 

 



