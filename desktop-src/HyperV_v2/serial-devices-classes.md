---
description: Последовательные устройства в виртуальной машине состоят из последовательных контроллеров и последовательных портов. Каждая виртуальная машина имеет ровно один последовательный контроллер, и каждый последовательный контроллер имеет ровно два последовательных порта.
ms.assetid: BA24BD74-D80C-4C5C-891F-5F17CDED2EC6
title: Классы последовательных устройств
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 10ae796b86837372d60bba83e51e0190b9c7d3f7
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "105683679"
---
# <a name="serial-devices-classes"></a><span data-ttu-id="7d6e5-104">Классы последовательных устройств</span><span class="sxs-lookup"><span data-stu-id="7d6e5-104">Serial devices classes</span></span>

<span data-ttu-id="7d6e5-105">Последовательные устройства в виртуальной машине состоят из последовательных контроллеров и последовательных портов.</span><span class="sxs-lookup"><span data-stu-id="7d6e5-105">The serial devices in a virtual machine consist of serial controllers and serial ports.</span></span> <span data-ttu-id="7d6e5-106">Каждая виртуальная машина имеет ровно один последовательный контроллер, и каждый последовательный контроллер имеет ровно два последовательных порта.</span><span class="sxs-lookup"><span data-stu-id="7d6e5-106">Each virtual machine has exactly one serial controller, and each serial controller has exactly two serial ports.</span></span>

<span data-ttu-id="7d6e5-107">Параметры контроллера последовательного порта нельзя настраивать; Поэтому с ним не связан ни один экземпляр данных.</span><span class="sxs-lookup"><span data-stu-id="7d6e5-107">The settings for the serial controller are not configurable; therefore, there is no setting data instance associated with it.</span></span> <span data-ttu-id="7d6e5-108">Кроме того, невозможно добавить или удалить последовательные контроллеры или последовательные порты с виртуальной машины.</span><span class="sxs-lookup"><span data-stu-id="7d6e5-108">Also, you cannot add or remove serial controllers or serial ports from a virtual machine.</span></span> <span data-ttu-id="7d6e5-109">Поэтому экземпляры пула ресурсов для последовательных устройств отсутствуют.</span><span class="sxs-lookup"><span data-stu-id="7d6e5-109">Therefore, there are no resource pool instances for serial devices.</span></span>

<span data-ttu-id="7d6e5-110">Ниже перечислены классы WMI виртуализации, связанные с последовательными устройствами.</span><span class="sxs-lookup"><span data-stu-id="7d6e5-110">The following are virtualization WMI classes related to serial devices.</span></span>

## <a name="in-this-section"></a><span data-ttu-id="7d6e5-111">В этом разделе</span><span class="sxs-lookup"><span data-stu-id="7d6e5-111">In this section</span></span>



| <span data-ttu-id="7d6e5-112">Раздел</span><span class="sxs-lookup"><span data-stu-id="7d6e5-112">Topic</span></span>                                                                                      | <span data-ttu-id="7d6e5-113">Описание</span><span class="sxs-lookup"><span data-stu-id="7d6e5-113">Description</span></span>                                                                     |
|--------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------|
| [<span data-ttu-id="7d6e5-114">**Мсвм \_ сериалконтроллер**</span><span class="sxs-lookup"><span data-stu-id="7d6e5-114">**Msvm\_SerialController**</span></span>](msvm-serialcontroller.md)<br/>                         | <span data-ttu-id="7d6e5-115">Представляет возможности и управление последовательным контроллером.</span><span class="sxs-lookup"><span data-stu-id="7d6e5-115">Represents the capabilities and management of the serial controller.</span></span><br/> |
| [<span data-ttu-id="7d6e5-116">**Мсвм \_ SerialPort**</span><span class="sxs-lookup"><span data-stu-id="7d6e5-116">**Msvm\_SerialPort**</span></span>](msvm-serialport.md)<br/>                                     | <span data-ttu-id="7d6e5-117">Представляет последовательный порт, связанный с контроллером последовательного порта.</span><span class="sxs-lookup"><span data-stu-id="7d6e5-117">Represents a serial port associated with the serial controller.</span></span><br/>      |
| [<span data-ttu-id="7d6e5-118">**Мсвм \_ сериалпортонсериалконтроллер**</span><span class="sxs-lookup"><span data-stu-id="7d6e5-118">**Msvm\_SerialPortOnSerialController**</span></span>](msvm-serialportonserialcontroller.md)<br/> | <span data-ttu-id="7d6e5-119">Связывает последовательный порт с последовательным контроллером.</span><span class="sxs-lookup"><span data-stu-id="7d6e5-119">Associates a serial port with a serial controller.</span></span><br/>                   |



 

 

 




